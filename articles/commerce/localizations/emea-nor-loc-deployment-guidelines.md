---
title: Leiðbeiningar um dreifingu fyrir sjóðvélar fyrir Noreg (arfleifð)
description: Þessi grein er dreifingarhandbók sem sýnir hvernig á að virkja Microsoft Dynamics 365 Commerce staðsetning fyrir Noreg.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2018-2-28
ms.openlocfilehash: 7a6450215f152779428d3b0fd83bf09761e2ad98
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894463"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway-legacy"></a>Leiðbeiningar um dreifingu fyrir sjóðvélar fyrir Noreg (arfleifð)

[!include [banner](../includes/banner.md)]

Þessi grein er dreifingarhandbók sem sýnir hvernig á að virkja Microsoft Dynamics 365 Commerce staðsetning fyrir Noreg. Staðsetningin samanstendur af nokkrum framlengingum á viðskiptahlutum. Til dæmis, viðbæturnar gera þér kleift að prenta sérsniðna reiti á kvittanir, skrá viðbótarendurskoðunarviðburði, sölufærslur og greiðslufærslur í sölustað (POS), stafrænt undirrita sölufærslur og prenta X og Z skýrslur á staðbundnu sniði. Fyrir frekari upplýsingar um staðsetningar fyrir Noreg, sjá [Gjaldkassavirkni fyrir Noreg](./emea-nor-cash-registers.md).

Þetta sýnishorn er hluti af smásöluhugbúnaðarþróunarsettinu (SDK). Fyrir upplýsingar um SDK, sjá [Smásala hugbúnaðarþróunarsett (SDK) arkitektúr](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Þetta sýnishorn samanstendur af viðbótum fyrir Commerce runtime (CRT), Retail Server og POS. Til að keyra þetta sýnishorn verður þú að breyta og byggja upp CRT, Retail Server og POS verkefni. Við mælum með því að þú notir óbreytt Retail SDK til að gera þær breytingar sem lýst er í þessari grein. Við mælum líka með því að þú notir heimildastýringarkerfi, eins og Microsoft Visual Studio Online (VSO), þar sem engum skrám hefur verið breytt ennþá.

> [!NOTE]
> Í Commerce 10.0.8 og nýrri er Retail Server þekktur sem Commerce Scale Unit. Vegna þess að þessi grein á við um margar fyrri útgáfur af appinu, *Smásöluþjónn* er notað í gegnum alla greinina.
>
> Sum skref í aðferðunum í þessari grein eru mismunandi eftir því hvaða útgáfu af Commerce þú ert að nota. Fyrir frekari upplýsingar, sjá [Hvað er nýtt eða breytt í Dynamics 365 Retail](../get-started/whats-new.md).

### <a name="using-certificate-profiles-in-commerce-channels"></a>Notkun vottorðasniða í viðskiptarásum

Í Commerce útgáfum 10.0.15 og nýrri geturðu notað [Notendaskilgreind vottorðssnið fyrir smásöluverslanir](./certificate-profiles-for-retail-stores.md) eiginleiki sem styður bilun yfir í offline þegar Key Vault eða Commerce höfuðstöðvar eru ekki tiltækar. Eiginleikinn framlengir [Stjórna leyndarmálum fyrir smásölurásir](../dev-itpro/manage-secrets.md) eiginleiki.

Til að beita þessari virkni í CRT framlengingu, fylgdu þessum skrefum.

1. Búðu til nýtt CRT viðbyggingarverkefni (C# flokks bókasafnsverkefnisgerð). Notaðu sýnishornssniðmátin úr Retail hugbúnaðarþróunarsettinu (SDK) (RetailSDK\SampleExtensions\CommerceRuntime).

2. Bættu við sérsniðnum meðhöndlun fyrir CertificateSignatureServiceRequest í SequentialSignatureRegister verkefninu.

3. Til að lesa leynilegt símtal,`GetUserDefinedSecretCertificateServiceRequest` með því að nota smið með profileId færibreytu. Það mun hefja virknina að vinna með stillingum frá vottorðssniðum. Byggt á stillingunum verður vottorðið sótt annað hvort úr Azure Key Vault eða staðbundinni vélageymslu.

    ```csharp
    GetUserDefinedSecretCertificateServiceRequest getUserDefinedSecretCertificateServiceRequest = new GetUserDefinedSecretCertificateServiceRequest(profileId: "ProfileId", secretName: null, thumbprint: null, expirationInterval: null);
    GetUserDefinedSecretCertificateServiceResponse getUserDefinedSecretCertificateServiceResponse = request.RequestContext.Execute<GetUserDefinedSecretCertificateServiceResponse>(getUserDefinedSecretCertificateServiceRequest);

    X509Certificate2 Certificate = getUserDefinedSecretCertificateServiceResponse.Certificate;
    ```

4. Þegar vottorðið er sótt skaltu halda áfram með gagnaundirritun.

5. Byggja upp CRT framlengingarverkefni.

6. Afritaðu úttaksflokkasafnið og límdu það inn í ...\RetailServer\webroot\bin\Ext til handvirkrar prófunar.

7. Í CommerceRuntime.Ext.config skránni, uppfærðu hluta viðbyggingarsamsetningar með sérsniðnum bókasafnsupplýsingum.

## <a name="development-environment"></a>Þróunarumhverfi

Ljúktu við þessar aðferðir til að setja upp þróunarumhverfi svo þú getir prófað og stækkað sýnishornið.

### <a name="the-crt-extension-components"></a>The CRT framlengingarhlutar

The CRT framlengingaríhlutir eru innifalin í CRT sýnishorn. Til að ljúka eftirfarandi aðferðum skaltu opna CRT lausn, **CommerceRuntimeSamples.sln**, undir **RetailSdk\\ SampleExtensions\\ CommerceRuntime**.

#### <a name="receiptsnorway-component"></a>KvittanirNoregur hluti

1. Finndu **Runtime.Extensions.ReceiptsNorway** verkefni, og byggja það.
2. Í **Viðbætur.KvittanirNoregi\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.Runtime.ReceiptsNorway.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána í CRT viðbætur mappa:

    - **Smásöluþjónn:** Afritaðu samsetninguna til **\\ bin\\ ext** möppu undir staðsetningu Microsoft Internet Information Services (IIS) Retail Server.
    - **Staðbundið CRT á Modern POS:** Afritaðu samsetninguna í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

4. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Smásöluþjónn:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

5. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
    ```

    > [!WARNING]
    > Gerðu **ekki** breyttu commerceruntime.config og CommerceRuntime.MPOSOffline.config skránum. Þessar skrár eru ekki ætlaðar til neinna sérstillinga.

#### <a name="salespaymenttransext-component"></a>SalesPaymentTransExt hluti

1. Finndu **Runtime.Extensions.SalesPaymentTransExt** verkefni, og byggja það.
2. Í **Viðbætur.SalagreiðslaTransExt\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.Runtime.SalesPaymentTransExt.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána í CRT viðbætur mappa:

    - **Smásöluþjónn:** Afritaðu samsetninguna til **\\ bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Afritaðu samsetninguna í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

4. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Smásöluþjónn:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

5. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
    ```

    > [!WARNING]
    > Gerðu **ekki** breyttu commerceruntime.config og CommerceRuntime.MPOSOffline.config skránum. Þessar skrár eru ekki ætlaðar til neinna sérstillinga.

#### <a name="xzreportsnorway-component"></a>XZReportsNorway hluti

1. Finndu **Runtime.Extensions.XZReportsNorway** verkefnið og byggja það.
2. Í **Viðbætur.XZReportsNorway\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.Runtime.XZReportsNorway.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána í CRT viðbætur mappa:

    - **Smásöluþjónn:** Afritaðu samsetninguna til **\\ bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Afritaðu samsetninguna í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

4. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Smásöluþjónn:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

5. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
    ```

    > [!WARNING]
    > Gerðu **ekki** breyttu commerceruntime.config og CommerceRuntime.MPOSOffline.config skránum. Þessar skrár eru ekki ætlaðar til neinna sérstillinga.

# <a name="application-update-4"></a>[Forritsuppfærsla 4](#tab/app-update-4)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent sýnishornshluti

1. Finndu **Runtime.Extensions.RegisterAuditEventSample** verkefnið og byggja það.
2. Í **Viðbætur.RegisterAuditEventSample\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána í CRT viðbætur mappa:

    - **Smásöluþjónn:** Afritaðu samsetninguna til **\\ bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Afritaðu samsetninguna í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

4. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Smásöluþjónn:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

5. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > Gerðu **ekki** breyttu commerceruntime.config og CommerceRuntime.MPOSOffline.config skránum. Þessar skrár eru ekki ætlaðar til neinna sérstillinga.

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSignature sýnishornshluti

1. Finndu **Runtime.Extensions.SalesTransactionSignatureSample** verkefni.
2. Breyttu **App.config** skrá með því að tilgreina þumalfingur, staðsetningu verslunar og heiti verslunar fyrir vottorðið sem ætti að nota til að undirrita sölufærslur.
3. Byggja verkefnið.
4. Í **Viðbætur.SalaviðskiptiUndirskriftSample\\ bin\\ Villuleit** möppu, finndu eftirfarandi skrár:

    - The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** samsetningarskrá
    - The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** stillingarskrá

5. Afritaðu skrárnar í CRT viðbætur mappa:

    - **Smásöluþjónn:** Afritaðu samsetninguna til **\\ bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Afritaðu samsetninguna í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

6. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Smásöluþjónn:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

7. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > Gerðu **ekki** breyttu commerceruntime.config og CommerceRuntime.MPOSOffline.config skránum. Þessar skrár eru ekki ætlaðar til neinna sérstillinga.

# <a name="application-update-5-and-later"></a>[Forritsuppfærsla 5 og síðar](#tab/app-update-5-and-later)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent sýnishornshluti

1. Finndu **Runtime.Extensions.RegisterAuditEventSample** verkefnið og byggja það.
2. Í **Viðbætur.RegisterAuditEventSample\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána í CRT viðbætur mappa:

    - **Smásöluþjónn:** Afritaðu samsetninguna til **\\ bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Afritaðu samsetninguna í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

4. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Smásöluþjónn:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

5. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > Gerðu **ekki** breyttu commerceruntime.config og CommerceRuntime.MPOSOffline.config skránum. Þessar skrár eru ekki ætlaðar til neinna sérstillinga.

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSignature sýnishornshluti

1. Finndu **Runtime.Extensions.SalesTransactionSignatureSample** verkefni.
2. Breyttu **App.config** skrá með því að tilgreina þumalfingur, staðsetningu verslunar og heiti verslunar fyrir vottorðið sem ætti að nota til að undirrita sölufærslur.
3. Byggja verkefnið.
4. Í **Viðbætur.SalaviðskiptiUndirskriftSample\\ bin\\ Villuleit** möppu, finndu eftirfarandi skrár:

    - The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** samsetningarskrá
    - The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** stillingarskrá

5. Afritaðu skrárnar í CRT viðbætur mappa:

    - **Smásöluþjónn:** Afritaðu samsetninguna til **\\ bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Afritaðu samsetninguna í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

6. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Smásöluþjónn:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

7. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > Gerðu **ekki** breyttu commerceruntime.config og CommerceRuntime.MPOSOffline.config skránum. Þessar skrár eru ekki ætlaðar til neinna sérstillinga.

#### <a name="salestransactionsignaturesamplemessages-component"></a>SalesTransactionSignatureSample.Messages hluti

1. Finndu **Runtime.Extensions.SalesTransactionSignatureSample.Skilaboð** verkefni.
2. Í **Viðbætur.SöluviðskiptiUndirskriftSample.Skilaboð\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána í CRT viðbætur mappa:

    - **Smásöluþjónn:** Afritaðu samsetninguna til **\\ bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Afritaðu samsetninguna í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

4. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Smásöluþjónn:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

5. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
    ```

    > [!WARNING]
    > Gerðu **ekki** breyttu commerceruntime.config og CommerceRuntime.MPOSOffline.config skránum. Þessar skrár eru ekki ætlaðar til neinna sérstillinga.

# <a name="retail-731"></a>[Smásala 7.3.1](#tab/retail-7-3-1)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent sýnishornshluti

1. Finndu **Runtime.Extensions.RegisterAuditEventSample** verkefnið og byggja það.
2. Í **Viðbætur.RegisterAuditEventSample\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána í CRT viðbætur mappa:

    - **Smásöluþjónn:** Afritaðu samsetninguna til **\\ bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Afritaðu samsetninguna í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

4. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Smásöluþjónn:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

5. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > Gerðu **ekki** breyttu commerceruntime.config og CommerceRuntime.MPOSOffline.config skránum. Þessar skrár eru ekki ætlaðar til neinna sérstillinga.

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSignature sýnishornshluti

1. Finndu **Runtime.Extensions.SalesTransactionSignatureSample** verkefni.
2. Breyttu **App.config** skrá með því að tilgreina þumalfingur, staðsetningu verslunar og heiti verslunar fyrir vottorðið sem ætti að nota til að undirrita sölufærslur.
3. Byggja verkefnið.
4. Í **Viðbætur.SalaviðskiptiUndirskriftSample\\ bin\\ Villuleit** möppu, finndu eftirfarandi skrár:

    - The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** samsetningarskrá
    - The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** stillingarskrá

5. Afritaðu skrárnar í CRT viðbætur mappa:

    - **Smásöluþjónn:** Afritaðu samsetninguna til **\\ bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Afritaðu samsetninguna í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

6. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Smásöluþjónn:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

7. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > Gerðu **ekki** breyttu commerceruntime.config og CommerceRuntime.MPOSOffline.config skránum. Þessar skrár eru ekki ætlaðar til neinna sérstillinga.

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSignatureRegister.Contracts hluti

1. Finndu **Runtime.Extensions.Sequential SignatureRegister.Contracts** verkefni.
2. Í **Viðbætur.SequentialSignatureRegister.Contracts\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána í CRT viðbætur mappa:

    - **Smásöluþjónn:** Afritaðu samsetninguna til **\\ bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Afritaðu samsetninguna í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

# <a name="retail-732-and-later"></a>[Smásala 7.3.2 og síðar](#tab/retail-7-3-2)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent sýnishornshluti

1. Finndu **Runtime.Extensions.RegisterAuditEventSample** verkefnið og byggja það.
2. Í **Viðbætur.RegisterAuditEventSample\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána í CRT viðbætur mappa:

    - **Smásöluþjónn:** Afritaðu samsetninguna til **\\ bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Afritaðu samsetninguna í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

4. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Smásöluþjónn:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

5. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > Gerðu **ekki** breyttu commerceruntime.config og CommerceRuntime.MPOSOffline.config skránum. Þessar skrár eru ekki ætlaðar til neinna sérstillinga.

#### <a name="sequentialsignatureregister-component"></a>SequentialSignatureRegister hluti

1. Finndu **Runtime.Extensions.SequentialSignatureRegister** verkefni.
2. Breyttu **App.config** skrá með því að tilgreina þumalfingur, staðsetningu verslunar og heiti verslunar fyrir vottorðið sem ætti að nota til að undirrita sölufærslur.
3. Byggja verkefnið.
4. Í **Viðbætur.SequentialSignatureRegister\\ bin\\ Villuleit** möppu, finndu eftirfarandi skrár:

    - The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** samsetningarskrá
    - The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** stillingarskrá

5. Afritaðu skrárnar í CRT viðbætur mappa:

    - **Smásöluþjónn:** Afritaðu samsetninguna til **\\ bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Afritaðu samsetninguna í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

6. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Smásöluþjónn:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

7. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > Gerðu **ekki** breyttu commerceruntime.config og CommerceRuntime.MPOSOffline.config skránum. Þessar skrár eru ekki ætlaðar til neinna sérstillinga.

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSignatureNorway hluti

1. Finndu **Runtime.Extensions.SalesTransactionSignatureNorway** verkefni.
2. Í **Viðbætur.SöluviðskiptiUndirskriftNoregur\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána í CRT viðbætur mappa:

    - **Smásöluþjónn:** Afritaðu samsetninguna til **\\ bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Afritaðu samsetninguna í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

4. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Smásöluþjónn:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

5. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > Gerðu **ekki** breyttu commerceruntime.config og CommerceRuntime.MPOSOffline.config skránum. Þessar skrár eru ekki ætlaðar til neinna sérstillinga.

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSignatureRegister.Contracts hluti

1. Finndu **Runtime.Extensions.Sequential SignatureRegister.Contracts** verkefni.
2. Í **Viðbætur.SequentialSignatureRegister.Contracts\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána í CRT viðbætur mappa:

    - **Smásöluþjónn:** Afritaðu samsetninguna til **\\ bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Afritaðu samsetninguna í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

#### <a name="salespaymenttransextnorway-component"></a>SalesPaymentTransExtNorway hluti

1. Finndu **Runtime.Extensions.SalesPaymentTransExtNorway** verkefnið og byggja það.
2. Í **Viðbætur.SalagreiðslaTransExtNorway\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána í CRT viðbætur mappa:

    - **Smásöluþjónn:** Afritaðu samsetninguna til **\\ bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Afritaðu samsetninguna í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

4. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Smásöluþjónn:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

5. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > Gerðu **ekki** breyttu commerceruntime.config og CommerceRuntime.MPOSOffline.config skránum. Þessar skrár eru ekki ætlaðar til neinna sérstillinga.

# <a name="retail-735-and-later"></a>[Smásala 7.3.5 og síðar](#tab/retail-7-3-5)

#### <a name="registerauditeventnorway-component"></a>RegisterAuditEventNorway hluti

1. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Smásöluþjónn:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

2. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > Gerðu **ekki** breyttu commerceruntime.config og CommerceRuntime.MPOSOffline.config skránum. Þessar skrár eru ekki ætlaðar til neinna sérstillinga.

#### <a name="sequentialsignatureregister-component"></a>SequentialSignatureRegister hluti

1. Finndu **Runtime.Extensions.SequentialSignatureRegister** verkefni.
2. Breyttu **App.config** skrá með því að tilgreina þumalfingur, staðsetningu verslunar og heiti verslunar fyrir vottorðið sem ætti að nota til að undirrita sölufærslur.
3. Byggja verkefnið.
4. Í **Viðbætur.SequentialSignatureRegister\\ bin\\ Villuleit** möppu, finndu eftirfarandi skrár:

    - The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** samsetningarskrá
    - The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** stillingarskrá

5. Afritaðu skrárnar í CRT viðbætur mappa:

    - **Smásöluþjónn:** Afritaðu samsetninguna til **\\ bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Afritaðu samsetninguna í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

6. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Smásöluþjónn:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

7. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > Gerðu **ekki** breyttu commerceruntime.config og CommerceRuntime.MPOSOffline.config skránum. Þessar skrár eru ekki ætlaðar til neinna sérstillinga.

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSignatureNorway hluti

1. Finndu **Runtime.Extensions.SalesTransactionSignatureNorway** verkefni.
2. Í **Viðbætur.SöluviðskiptiUndirskriftNoregur\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána í CRT viðbætur mappa:

    - **Smásöluþjónn:** Afritaðu samsetninguna til **\\ bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Afritaðu samsetninguna í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

4. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Smásöluþjónn:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

5. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > Gerðu **ekki** breyttu commerceruntime.config og CommerceRuntime.MPOSOffline.config skránum. Þessar skrár eru ekki ætlaðar til neinna sérstillinga.

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSignatureRegister.Contracts hluti

1. Finndu **Runtime.Extensions.Sequential SignatureRegister.Contracts** verkefni.
2. Í **Viðbætur.SequentialSignatureRegister.Contracts\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána í CRT viðbætur mappa:

    - **Smásöluþjónn:** Afritaðu samsetninguna til **\\ bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Afritaðu samsetninguna í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

#### <a name="salespaymenttransextnorway-component"></a>SalesPaymentTransExtNorway hluti

1. Finndu **Runtime.Extensions.SalesPaymentTransExtNorway** verkefnið og byggja það.
2. Í **Viðbætur.SalagreiðslaTransExtNorway\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána í CRT viðbætur mappa:

    - **Smásöluþjónn:** Afritaðu samsetninguna til **\\ bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Afritaðu samsetninguna í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

4. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Smásöluþjónn:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

5. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > Gerðu **ekki** breyttu commerceruntime.config og CommerceRuntime.MPOSOffline.config skránum. Þessar skrár eru ekki ætlaðar til neinna sérstillinga.

# <a name="retail-811-and-later"></a>[Smásala 8.1.1 og síðar](#tab/retail-8-1-1)

#### <a name="registerauditeventnorway-component"></a>RegisterAuditEventNorway hluti

1. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Smásöluþjónn:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

2. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > Gerðu **ekki** breyttu commerceruntime.config og CommerceRuntime.MPOSOffline.config skránum. Þessar skrár eru ekki ætlaðar til neinna sérstillinga.

#### <a name="sequentialsignatureregister-component"></a>SequentialSignatureRegister hluti

1. Finndu **Runtime.Extensions.SequentialSignatureRegister** verkefni.
2. Breyttu **App.config** skrá með því að tilgreina þumalfingur, staðsetningu verslunar og heiti verslunar fyrir vottorðið sem ætti að nota til að undirrita sölufærslur.
3. Byggja verkefnið.
4. Í **Viðbætur.SequentialSignatureRegister\\ bin\\ Villuleit** möppu, finndu eftirfarandi skrár:

    - The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** samsetningarskrá
    - The **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** stillingarskrá

5. Afritaðu skrárnar í CRT viðbætur mappa:

    - **Smásöluþjónn:** Afritaðu samsetninguna til **\\ bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Afritaðu samsetninguna í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

6. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Smásöluþjónn:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

7. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > Gerðu **ekki** breyttu commerceruntime.config og CommerceRuntime.MPOSOffline.config skránum. Þessar skrár eru ekki ætlaðar til neinna sérstillinga.

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSignatureNorway hluti

1. Finndu **Runtime.Extensions.SalesTransactionSignatureNorway** verkefni.
2. Í **Viðbætur.SöluviðskiptiUndirskriftNoregur\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána í CRT viðbætur mappa:

    - **Smásöluþjónn:** Afritaðu samsetninguna til **\\ bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Afritaðu samsetninguna í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

4. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Smásöluþjónn:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

5. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > Gerðu **ekki** breyttu commerceruntime.config og CommerceRuntime.MPOSOffline.config skránum. Þessar skrár eru ekki ætlaðar til neinna sérstillinga.

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSignatureRegister.Contracts hluti

1. Finndu **Runtime.Extensions.Sequential SignatureRegister.Contracts** verkefni.
2. Í **Viðbætur.SequentialSignatureRegister.Contracts\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána í CRT viðbætur mappa:

    - **Smásöluþjónn:** Afritaðu samsetninguna til **\\ bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Afritaðu samsetninguna í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

#### <a name="salespaymenttransextnorway-component"></a>SalesPaymentTransExtNorway hluti

1. Finndu **Runtime.Extensions.SalesPaymentTransExtNorway** verkefnið og byggja það.
2. Í **Viðbætur.SalagreiðslaTransExtNorway\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána í CRT viðbætur mappa:

    - **Smásöluþjónn:** Afritaðu samsetninguna til **\\ bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Afritaðu samsetninguna í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

4. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Smásöluþjónn:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

5. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > Gerðu **ekki** breyttu commerceruntime.config og CommerceRuntime.MPOSOffline.config skránum. Þessar skrár eru ekki ætlaðar til neinna sérstillinga.

---

### <a name="the-retail-server-extension-components"></a>Viðbótarhlutir Retail Server

#### <a name="salestransactionsignature-retail-server-sample-component"></a>SalesTransactionSignature Retail Server sýnishornshlutur

1. Í **RetailSDK\\ SampleExtensions\\ RetailServer\\ RetailServer.Extensions.SalesTransactionSignatureSample** möppu, finndu **RetailServer.Extensions.SalesTransactionSignatureSample** verkefnið og byggja það.
2. Í **RetailServer\\ Viðbætur.SalaviðskiptiUndirskriftSample\\ bin\\ Villuleit** möppu, finndu **Contoso.RetailServer.SalesTransactionSignatureSample.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána í Retail Server extensions möppuna.

    # <a name="application-update-4"></a>[Forritsuppfærsla 4](#tab/app-update-4)

    Mappan er **\\ bin** möppu undir staðsetningarsvæði IIS Retail Server.

    # <a name="application-update-5-and-later"></a>[Forritsuppfærsla 5 og síðar](#tab/app-update-5-and-later)

    Mappan er **\\ bin** möppu undir staðsetningarsvæði IIS Retail Server.

    # <a name="retail-731"></a>[Smásala 7.3.1](#tab/retail-7-3-1)

    Mappan er **\\ bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.

    # <a name="retail-732-and-later"></a>[Smásala 7.3.2 og síðar](#tab/retail-7-3-2)

    Mappan er **\\ bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.

    # <a name="retail-735-and-later"></a>[Smásala 7.3.5 og síðar](#tab/retail-7-3-5)

    Mappan er **\\ bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.

    # <a name="retail-811-and-later"></a>[Smásala 8.1.1 og síðar](#tab/retail-8-1-1)

    Mappan er **\\ bin\\ ext** möppu undir staðsetningarsvæði IIS Retail Server.

    ---

4. Finndu stillingarskrána fyrir Retail Server. Skráin er nefnd **web.config**, og það er í rótarmöppunni undir staðsetningu IIS Retail Server vefsvæðisins.
5. Skráðu Retail Server viðbætur í **framlengingSamsetning** hluta stillingaskrárinnar.

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

6. Skráðu ósjálfstæði smásöluþjónaviðbótanna.

    # <a name="application-update-4"></a>[Forritsuppfærsla 4](#tab/app-update-4/)

    1. Í **CommerceRuntime\\ Viðbætur.SalaviðskiptiUndirskriftSample\\ bin\\ Villuleit** möppu, finndu eftirfarandi skrár:

        - The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** samsetningarskrá
        - The **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** stillingarskrá

    2. Afritaðu skrárnar í **\\ bin** möppu undir staðsetningarsvæði IIS Retail Server.
    3. Skráðu þig CRT breyting á stillingarskrá eftirlengingar fyrir CRT. Þessi skrá er nefnd **commerceruntime.ext.config**, og það er í **bin** möppu undir staðsetningarsvæði IIS Retail Server.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        ```

    # <a name="application-update-5-and-later"></a>[Forritsuppfærsla 5 og síðar](#tab/app-update-5-and-later/)

    1. Í **CommerceRuntime\\ Viðbætur.SöluviðskiptiUndirskriftSample.Skilaboð\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** samsetningarskrá.
    2. Afritaðu skrána í **\\ bin** möppu undir staðsetningarsvæði IIS Retail Server.
    3. Skráðu þig CRT breyting á stillingarskrá eftirlengingar fyrir CRT. Þessi skrá er nefnd **commerceruntime.ext.config**, og það er í **bin** möppu undir staðsetningarsvæði IIS Retail Server.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        ```

    # <a name="retail-731"></a>[Smásala 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Engar aðgerðir eru nauðsynlegar.

    # <a name="retail-732-and-later"></a>[Smásala 7.3.2 og síðar](#tab/retail-7-3-2)

    > [!NOTE]
    > Engar aðgerðir eru nauðsynlegar.

    # <a name="retail-735-and-later"></a>[Smásala 7.3.5 og síðar](#tab/retail-7-3-5)

    > [!NOTE]
    > Engar aðgerðir eru nauðsynlegar.

    # <a name="retail-811-and-later"></a>[Smásala 8.1.1 og síðar](#tab/retail-8-1-1)

    > [!NOTE]
    > Engar aðgerðir eru nauðsynlegar.

    ---

### <a name="the-modern-pos-extension-components"></a>Nútíma POS viðbyggingarhlutirnir

#### <a name="implement-the-proxy-code-for-offline-mode"></a>Innleiða umboðskóðann fyrir offline stillingu

Þessi hluti jafngildir Retail Server stjórnandi, en hann stækkar staðbundna CRT sem er notað þegar viðskiptavinurinn er ekki tengdur.

1. Í **customization.settings** skrá, breyttu **@(RetailServerLibraryPathForProxyGeneration)** kafla þannig að það noti nýja Retail Server samsetninguna til að búa til proxy.
2. Innleiða eftirfarandi viðmótsaðferðir í **Store Operations Manager** bekk. Fyrir fyrstu endurtekningu skaltu bæta við eftirfarandi kóða:

    # <a name="application-update-4"></a>[Forritsuppfærsla 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="application-update-5-and-later"></a>[Forritsuppfærsla 5 og síðar](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="retail-731"></a>[Smásala 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Þetta skref á ekki við um þessa útgáfu.

    # <a name="retail-732-and-later"></a>[Smásala 7.3.2 og síðar](#tab/retail-7-3-2)

    > [!NOTE]
    > Þetta skref á ekki við um þessa útgáfu.

    # <a name="retail-735-and-later"></a>[Smásala 7.3.5 og síðar](#tab/retail-7-3-5)

    > [!NOTE]
    > Þetta skref á ekki við um þessa útgáfu.

    # <a name="retail-811-and-later"></a>[Smásala 8.1.1 og síðar](#tab/retail-8-1-1)

    > [!NOTE]
    > Þetta skref á ekki við um þessa útgáfu.

    ---

3. Til að endurskapa proxy-kóðann skaltu búa til **Umboð** möppu frá skipanalínunni með því að nota **msbuild /t:endurbyggja** skipun.
4. Leysið úr **Proxies.RetailProxy** verkefni háð:

    # <a name="application-update-4"></a>[Forritsuppfærsla 4](#tab/app-update-4)

    Opið **RetailSDK\\ Umboð\\ RetailProxy\\ Proxies.RetailProxy.csproj**, bætið við **RetailSDK\\ SampleExtensions\\ CommerceRuntime\\ Viðbætur.SalaviðskiptiUndirskriftSample\\ CommerceRuntime.Extensions.SalesTransactionSignatureSample** verkefni við lausnina og bættu við verkefnatilvísun í **RetailProxy** verkefni til viðmiðunar **SalesTransactionSignatureSample**.

    # <a name="application-update-5-and-later"></a>[Forritsuppfærsla 5 og síðar](#tab/app-update-5-and-later)

    Opið **RetailSDK\\ Umboð\\ RetailProxy\\ Proxies.RetailProxy.csproj**, bætið við **RetailSDK\\ SampleExtensions\\ CommerceRuntime\\ Viðbætur.SöluviðskiptiUndirskriftSample.Skilaboð\\ CommerceRuntime.Extensions.SalesTransactionSignatureSample.Skilaboð** verkefni við lausnina og bættu við verkefnatilvísun í **RetailProxy** verkefni til viðmiðunar **SalesTransactionSignatureSample.Messages**.

    # <a name="retail-731"></a>[Smásala 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Þetta skref á ekki við um þessa útgáfu.

    # <a name="retail-732-and-later"></a>[Smásala 7.3.2 og síðar](#tab/retail-7-3-2)

    > [!NOTE]
    > Þetta skref á ekki við um þessa útgáfu.

    # <a name="retail-735-and-later"></a>[Smásala 7.3.5 og síðar](#tab/retail-7-3-5)

    > [!NOTE]
    > Þetta skref á ekki við um þessa útgáfu.

    # <a name="retail-811-and-later"></a>[Smásala 8.1.1 og síðar](#tab/retail-8-1-1)

    > [!NOTE]
    > Þetta skref á ekki við um þessa útgáfu.

    ---

5. Stilltu viðmótsaðferðirnar í **Store Operations Manager** bekkur:

    # <a name="application-update-4"></a>[Forritsuppfærsla 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="application-update-5-and-later"></a>[Forritsuppfærsla 5 og síðar](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="retail-731"></a>[Smásala 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Þetta skref á ekki við um þessa útgáfu.

    # <a name="retail-732-and-later"></a>[Smásala 7.3.2 og síðar](#tab/retail-7-3-2)

    > [!NOTE]
    > Þetta skref á ekki við um þessa útgáfu.

    # <a name="retail-735-and-later"></a>[Smásala 7.3.5 og síðar](#tab/retail-7-3-5)

    > [!NOTE]
    > Þetta skref á ekki við um þessa útgáfu.

    # <a name="retail-811-and-later"></a>[Smásala 8.1.1 og síðar](#tab/retail-8-1-1)

    > [!NOTE]
    > Þetta skref á ekki við um þessa útgáfu.

    ---

6. Uppfærðu **dllhost.exe.config** skrá þannig að miðlari viðskiptavinarins hleður nýju RetailProxy samsetningunni.

    ``` xml
    <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy" />
    <add key="AdaptorCallerFullTypeName" value="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller" />
    ```

#### <a name="retail-proxy-extension-component-retail-731-and-later"></a>Umboðsviðbót í smásölu (Retail 7.3.1 og nýrri)

Ljúktu aðeins eftirfarandi ferli ef þú ert að nota Retail 7.3.1 og nýrri.

1. Í **RetailSDK\\ SampleExtensions\\ RetailProxy\\ RetailProxy.Extensions.SalesTransactionSignatureSample** möppu, finndu **RetailServer.Extensions.SalesTransactionSignatureSample** verkefni, og byggja það.
2. Í **RetailProxy\\ RetailProxy.Extensions.SalesTransactionSignatureSample\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample** samsetningarskrá.
3. Afritaðu samsetningarskrárnar í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.
4. Skráðu smásölu proxy-breytinguna í stillingarskránni fyrir viðbótina. Skráin er nefnd **RetailProxy.MPOSOffline.ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
    ```

#### <a name="modern-pos-extension-components"></a>Nútímalegir POS framlengingaríhlutir

1. Opnaðu lausnina kl **RetailSdk\\ POS\\ ModernPOS.sln**, og vertu viss um að hægt sé að setja hana saman án villna. Gakktu úr skugga um að þú getir keyrt Modern POS frá Microsoft Visual Studio með því að nota **Hlaupa** skipun.

    > [!NOTE]
    > Ekki má aðlaga nútíma posa. Virkja verður stjórnun notendareikninga (UAC) og fjarlægja verður áður uppsett tilvik af Modern POS eftir þörfum.

2. Láttu eftirfarandi frumkóðamöppur fylgja með í **Pos.Viðbætur** verkefni.

    # <a name="application-update-4"></a>[Forritsuppfærsla 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Forritsuppfærsla 5 og síðar](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Smásala 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Smásala 7.3.2 og síðar](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - Sequential Signature

    # <a name="retail-735-and-later"></a>[Smásala 7.3.5 og síðar](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - Sequential Signature

    # <a name="retail-811-and-later"></a>[Smásala 8.1.1 og síðar](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - Sequential Signature

    ---

3. Virkjaðu að viðbæturnar séu settar saman í **tsconfig.json** með því að fjarlægja eftirfarandi möppur af útilokunarlistanum.

    # <a name="application-update-4"></a>[Forritsuppfærsla 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Forritsuppfærsla 5 og síðar](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Smásala 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Smásala 7.3.2 og síðar](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - Sequential Signature

    # <a name="retail-735-and-later"></a>[Smásala 7.3.5 og síðar](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - Sequential Signature

    # <a name="retail-811-and-later"></a>[Smásala 8.1.1 og síðar](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - Sequential Signature

    ---

4. Virkjaðu að viðbæturnar séu hlaðnar inn **extensions.json** með því að bæta eftirfarandi línum við á viðeigandi stað.

    # <a name="application-update-4"></a>[Forritsuppfærsla 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[Forritsuppfærsla 5 og síðar](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Smásala 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Smásala 7.3.2 og síðar](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Smásala 7.3.5 og síðar](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Smásala 8.1.1 og síðar](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > Frekari upplýsingar og fyrir sýni sem sýna hvernig á að taka með möppur frumkóða og gera kleift að hlaða inn viðbótum er að finna í leiðbeiningunum í readme.md skránni **í Pos.Extensions** verkefninu.

5. Endurbyggja lausnina.
6. Keyra skal Modern POS í kembiforritinu og prófa virknina.

### <a name="cloud-pos-extension-components"></a>Cloud POS viðbót íhlutir

1. Opnaðu lausnina kl **RetailSdk\\ POS\\ CloudPOS.sln**, og vertu viss um að hægt sé að setja hana saman án villna.
2. Láttu eftirfarandi frumkóðamöppur fylgja með í **Pos.Viðbætur** verkefni.

    # <a name="application-update-4"></a>[Forritsuppfærsla 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Forritsuppfærsla 5 og síðar](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Smásala 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Smásala 7.3.2 og síðar](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - Sequential Signature

    # <a name="retail-735-and-later"></a>[Smásala 7.3.5 og síðar](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - Sequential Signature

    # <a name="retail-811-and-later"></a>[Smásala 8.1.1 og síðar](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - Sequential Signature

    ---

3. Virkjaðu að viðbæturnar séu settar saman í **tsconfig.json** með því að fjarlægja eftirfarandi möppur af útilokunarlistanum.

    # <a name="application-update-4"></a>[Forritsuppfærsla 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Forritsuppfærsla 5 og síðar](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Smásala 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Smásala 7.3.2 og síðar](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - Sequential Signature

    # <a name="retail-735-and-later"></a>[Smásala 7.3.5 og síðar](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - Sequential Signature

    # <a name="retail-811-and-later"></a>[Smásala 8.1.1 og síðar](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - Sequential Signature

    ---

4. Virkjaðu að viðbæturnar séu hlaðnar inn **extensions.json** með því að bæta eftirfarandi línum við á viðeigandi stað.

    # <a name="application-update-4"></a>[Forritsuppfærsla 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[Forritsuppfærsla 5 og síðar](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Smásala 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Smásala 7.3.2 og síðar](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Smásala 7.3.5 og síðar](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Smásala 8.1.1 og síðar](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > Frekari upplýsingar og fyrir sýni sem sýna hvernig á að taka með möppur frumkóða og gera kleift að hlaða inn viðbótum er að finna í leiðbeiningunum í readme.md skránni **í Pos.Extensions** verkefninu.

5. Endurbyggja lausnina.
6. Keyrið lausnina með skipuninni **Keyra** og fylgið skrefunum í smásölu SDK handbókinni.
7. Prófaðu virknina.

### <a name="set-up-required-parameters-in-headquarters"></a>Settu upp nauðsynlegar færibreytur í höfuðstöðvum

Fyrir frekari upplýsingar, sjá [Gjaldkassavirkni fyrir Noreg](./emea-nor-cash-registers.md).

## <a name="production-environment"></a>Framleiðsluumhverfi

Fylgdu þessum skrefum til að búa til dreifanlega pakka sem innihalda Commerce íhluti og til að nota þá pakka í framleiðsluumhverfi.

1. Ljúktu við skrefin í [Cloud POS viðbót íhlutir](#cloud-pos-extension-components) eða [Nútímalegir POS framlengingaríhlutir](#modern-pos-extension-components) kafla fyrr í þessari grein.
2. Gera eftirfarandi breytingar á samskipanarskrám pakka í möppunni **RetailSdk\\ Assets**:

    1. Í **commerceruntime.ext.config** og **CommerceRuntime.MPOSOffline.Ext.config** stillingarskrár skaltu bæta eftirfarandi línum við **samsetningu** kafla:

        # <a name="application-update-4"></a>[Forritsuppfærsla 4](#tab/app-update-4)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="application-update-5-and-later"></a>[Forritsuppfærsla 5 og síðar](#tab/app-update-5-and-later)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-731"></a>[Smásala 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-732-and-later"></a>[Smásala 7.3.2 og síðar](#tab/retail-7-3-2)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-735-and-later"></a>[Smásala 7.3.5 og síðar](#tab/retail-7-3-5)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-811-and-later"></a>[Smásala 8.1.1 og síðar](#tab/retail-8-1-1)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        ---

    2. Virkjaðu aðlögun Commerce proxy:

        # <a name="application-update-4"></a>[Forritsuppfærsla 4](#tab/app-update-4)

        Í **dllhost.exe.config** stillingarskrá skaltu bæta eftirfarandi línum við **app Stillingar** undirkafla **stillingar** kafla.

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="application-update-5-and-later"></a>[Forritsuppfærsla 5 og síðar](#tab/app-update-5-and-later)

        Í **dllhost.exe.config** stillingarskrá skaltu bæta eftirfarandi línum við **app Stillingar** undirkafla **stillingar** kafla.

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="retail-731"></a>[Smásala 7.3.1](#tab/retail-7-3-1)

        Í **RetailProxy.MPOSOffline.ext.config** stillingarskrá skaltu bæta eftirfarandi línum við **samsetningu** kafla:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-732-and-later"></a>[Smásala 7.3.2 og síðar](#tab/retail-7-3-2)

        Í **RetailProxy.MPOSOffline.ext.config** stillingarskrá skaltu bæta eftirfarandi línum við **samsetningu** kafla:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-735-and-later"></a>[Smásala 7.3.5 og síðar](#tab/retail-7-3-5)

        Í **RetailProxy.MPOSOffline.ext.config** stillingarskrá skaltu bæta eftirfarandi línum við **samsetningu** kafla:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-811-and-later"></a>[Smásala 8.1.1 og síðar](#tab/retail-8-1-1)

        Í **RetailProxy.MPOSOffline.ext.config** stillingarskrá skaltu bæta eftirfarandi línum við **samsetningu** kafla:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        ---

3. Gerðu eftirfarandi breytingar á **Customization.settings** stillingarskrá fyrir sérsniðna pakka:

    1. Virkjaðu aðlögun Proxy Retail.

        # <a name="application-update-4"></a>[Forritsuppfærsla 4](#tab/app-update-4)

        Bættu eftirfarandi línum við **&lt; ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** kafla.

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="application-update-5-and-later"></a>[Forritsuppfærsla 5 og síðar](#tab/app-update-5-and-later)

        Bættu eftirfarandi línum við **&lt; ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** kafla.

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="retail-731"></a>[Smásala 7.3.1](#tab/retail-7-3-1)

        Bættu eftirfarandi línum við **Atriðahópur** kafla til að innihalda umboðsviðbót smásala í innleiðanlegum pakka:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Smásala 7.3.2 og síðar](#tab/retail-7-3-2)

        Bættu eftirfarandi línum við **Atriðahópur** kafla til að innihalda umboðsviðbót smásala í innleiðanlegum pakka:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Smásala 7.3.5 og síðar](#tab/retail-7-3-5)

        Bættu eftirfarandi línum við **Atriðahópur** kafla til að innihalda umboðsviðbót smásala í innleiðanlegum pakka:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Smásala 8.1.1 og síðar](#tab/retail-8-1-1)

        Bættu eftirfarandi línum við **Atriðahópur** kafla til að innihalda umboðsviðbót smásala í innleiðanlegum pakka:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        ---

    2. Bættu eftirfarandi línum við **Atriðahópur** kafla til að innihalda CRT viðbætur í dreifanlegum pökkum:

        # <a name="application-update-4"></a>[Forritsuppfærsla 4](#tab/app-update-4)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="application-update-5-and-later"></a>[Forritsuppfærsla 5 og síðar](#tab/app-update-5-and-later)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-731"></a>[Smásala 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Smásala 7.3.2 og síðar](#tab/retail-7-3-2)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Smásala 7.3.5 og síðar](#tab/retail-7-3-5)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Smásala 8.1.1 og síðar](#tab/retail-8-1-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        ---

    3. Bættu eftirfarandi línum við **Atriðahópur** kafla til að innihalda Retail Server viðbótina í dreifanlegum pakka:

        # <a name="application-update-4"></a>[Forritsuppfærsla 4](#tab/app-update-4)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        ```

        # <a name="application-update-5-and-later"></a>[Forritsuppfærsla 5 og síðar](#tab/app-update-5-and-later)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        ```

        # <a name="retail-731"></a>[Smásala 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Smásala 7.3.2 og síðar](#tab/retail-7-3-2)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Smásala 7.3.5 og síðar](#tab/retail-7-3-5)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Smásala 8.1.1 og síðar](#tab/retail-8-1-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        ---

4. Breyttu eftirfarandi skrám til að innihalda auðlindaskrárnar fyrir Noreg í dreifanlegum pakka:
    - Pakkar\_ SharedPackagingProjectComponents\Sdk.ModernPos.Shared.csproj
    - Pakkar\RetailServer\Sdk.RetailServerSetup.proj
  
  - Fyrir **Sdk.ModernPos.Shared.csproj** skrá 
    - Bættu línu við **Atriðahópur** kafla
    
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```
    > [!Note]
    > Í stað <File_name>tilgreindu nafn á auðlindaskránni. Það sama á við um önnur dæmi sem gefin eru hér að neðan.
 
    - Bættu línu við **Target Name="CopyPackageFiles"** kafla
       ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\nb-NO" SkipUnchangedFiles="true" />
        ```
  
  - Fyrir **Sdk.RetailServerSetup.proj** skrá 
    - Bættu línu við **Atriðahópur** kafla
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```    
    - Bættu línu við **Target Name="CopyPackageFiles"** kafla
         ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\nb-NO" SkipUnchangedFiles="true" />
        ```    

5. Breyttu stillingarskrá vottorðsins með því að tilgreina þumalfingur, verslunarstaðsetningu og verslunarheiti fyrir vottorðið sem ætti að nota til að undirrita sölufærslur. Afritaðu síðan stillingarskrána í **Heimildir** möppu.

    # <a name="application-update-4"></a>[Forritsuppfærsla 4](#tab/app-update-4)

    Skráin er nefnd **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**, og það er undir **CommerceRuntime\\ Viðbætur.SalaviðskiptiUndirskriftSample\\ bin\\ Villuleit**.

    # <a name="application-update-5-and-later"></a>[Forritsuppfærsla 5 og síðar](#tab/app-update-5-and-later)

    Skráin er nefnd **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**, og það er undir **CommerceRuntime\\ Viðbætur.SalaviðskiptiUndirskriftSample\\ bin\\ Villuleit**.

    # <a name="retail-731"></a>[Smásala 7.3.1](#tab/retail-7-3-1)

    Skráin er nefnd **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**, og það er undir **CommerceRuntime\\ Viðbætur.SalaviðskiptiUndirskriftSample\\ bin\\ Villuleit**.

    # <a name="retail-732-and-later"></a>[Smásala 7.3.2 og síðar](#tab/retail-7-3-2)

    Skráin er nefnd **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**, og það er undir **Viðbætur.SequentialSignatureRegister\\ bin\\ Villuleit**.

    # <a name="retail-735-and-later"></a>[Smásala 7.3.5 og síðar](#tab/retail-7-3-5)

    Skráin er nefnd **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**, og það er undir **Viðbætur.SequentialSignatureRegister\\ bin\\ Villuleit**.

    # <a name="retail-811-and-later"></a>[Smásala 8.1.1 og síðar](#tab/retail-8-1-1)

    Skráin er nefnd **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**, og það er undir **Viðbætur.SequentialSignatureRegister\\ bin\\ Villuleit**.

    ---

6. Uppfærðu stillingarskrá Retail Server. Í **RetailSDK\\ Pakkar\\ RetailServer\\ Kóði\\ web.config** skrá skaltu bæta eftirfarandi línum við **framlengingSamsetning** kafla.

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

7. Hlaupa **msbuild** fyrir allt Retail SDK til að búa til dreianlega pakka.
8. Notaðu pakkana í gegnum Microsoft Dynamics Lifecycle Services (LCS) eða handvirkt. Sjá Create deployable packages [fyrir frekari upplýsingar](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>Virkjaðu stafrænu undirskriftina í ótengdum ham fyrir Modern POS

Til að virkja stafræna undirskrift í ótengdum ham fyrir Modern POS, verður þú að fylgja þessum skrefum eftir að þú hefur virkjað Modern POS á nýju tæki.

1. Skráðu þig inn í POS.
2. Á **Gagnagrunnstengingarstaða** síðu skaltu ganga úr skugga um að ótengdur gagnagrunnur sé að fullu samstilltur. Þegar verðmæti **Niðurhal í bið** sviði er **0** (núll), gagnagrunnurinn er að fullu samstilltur.
3. Skráðu þig út af POS.
4. Bíddu í smá stund þar til ónettengdi gagnagrunnurinn er að fullu samstilltur.
5. Skráðu þig inn í POS.
6. Á **Gagnagrunnstengingarstaða** síðu skaltu ganga úr skugga um að ótengdur gagnagrunnur sé að fullu samstilltur. Þegar verðmæti **Viðskipti í bið í ótengdum gagnagrunni** sviði er **0** (núll), gagnagrunnurinn er að fullu samstilltur.
7. Endurræstu Modern POS.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
