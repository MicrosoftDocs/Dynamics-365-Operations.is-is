---
title: Leiðbeiningar um dreifingu fyrir samþættingarsýni skattaskráningarþjónustu fyrir Austurríki (arfleifð)
description: Þessi grein veitir leiðbeiningar um að dreifa ríkisfjármálasamþættingarsýninu fyrir Austurríki frá Microsoft Dynamics 365 Commerce Smásöluhugbúnaðarþróunarsett (SDK).
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 94fe6817358ae18126a30794fd52fe5eb01a5265
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885438"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-austria-legacy"></a>Leiðbeiningar um dreifingu fyrir samþættingarsýni skattaskráningarþjónustu fyrir Austurríki (arfleifð)

[!include [banner](../includes/banner.md)]

Þessi grein veitir leiðbeiningar um útfærslu samþættingarsýnis fyrir skattaskráningarþjónustu fyrir Austurríki frá Microsoft Dynamics 365 Commerce Smásöluhugbúnaðarþróunarsett (SDK) á sýndarvél þróunaraðila (VM) í Microsoft Dynamics Lífsferilsþjónusta (LCS). Fyrir frekari upplýsingar um þetta sýnishorn af samþættingu ríkisfjármála, sjá [Samþættingarsýni fyrir ríkisskattaskráningarþjónustu fyrir Austurríki](emea-aut-fi-sample.md). 

Fjármálasamþættingarúrtakið fyrir Austurríki er hluti af Retail SDK. Fyrir upplýsingar um hvernig á að setja upp og nota SDK, sjá [Smásala hugbúnaðarþróunarsett (SDK) arkitektúr](../dev-itpro/retail-sdk/retail-sdk-overview.md). Fjármálasamþættingarúrtakið samanstendur af framlengingum fyrir viðskiptatímann (CRT), Vélbúnaðarstöð og sölustaður (POS). Til að keyra þetta sýnishorn verður þú að breyta og byggja upp CRT, Vélbúnaðarstöð og POS verkefni. Við mælum með því að þú notir óbreytt Retail SDK til að gera þær breytingar sem lýst er í þessari grein. Við mælum líka með því að þú notir heimildastýringarkerfi eins og Azure DevOps þar sem engum skrám hefur verið breytt ennþá.

## <a name="development-environment"></a>Þróunarumhverfi

Fylgdu þessum skrefum til að setja upp þróunarumhverfi svo þú getir prófað og stækkað sýnishornið.

### <a name="enable-commerce-runtime-extensions"></a>Virkja Commerce runtime viðbætur

The CRT framlengingaríhlutir eru innifalin í CRT sýnishorn. Til að ljúka eftirfarandi aðferðum skaltu opna **CommerceRuntimeSamples.sln** lausn undir **RetailSdk\\ SampleExtensions\\ CommerceRuntime**.

#### <a name="documentproviderefrsample-component"></a>DocumentProvider.EFRSample hluti

1. Finndu **Runtime.Extensions.DocumentProvider.EFRSample** verkefnið og byggja það.
2. Í **Runtime.Extensions.DocumentProvider.EFRSample\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána í CRT viðbætur mappa:

    - **Eining viðskiptaskala:** Afritaðu skrána í **\\ bin\\ ext** möppu undir Internet Information Services (IIS) Commerce Scale Unit staðsetningu.
    - **Staðbundið CRT á Modern POS:** Afritaðu skrána í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

4. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Eining viðskiptaskala:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningu IIS Commerce Scale Unit.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

5. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
    ```

#### <a name="documentproviderdatamodelefr-component"></a>DocumentProvider.DataModelEFR hluti

1. Finndu **Runtime.Extensions.DocumentProvider.DataModelEFR** verkefnið og byggja það.
2. Í **Runtime.Extensions.DocumentProvider.DataModelEFR\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána í CRT viðbætur mappa:

    - **Commerce Scale Unit:** Afritaðu skrána í hólfið **\\\\ ext** möppuna undir staðsetningu IIS Commerce Scale Unit.
    - **Staðbundið CRT á Modern POS:** Afritaðu skrána í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

4. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Eining viðskiptaskala:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningu IIS Commerce Scale Unit.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

5. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="extension-configuration-file"></a>Stillingarskrá fyrir viðbætur

1. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Eining viðskiptaskala:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningu IIS Commerce Scale Unit.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

2. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
    ```

### <a name="enable-fiscal-connector-extensions"></a>Virkja framlengingu á fjárhagstengi

Þú getur virkjað framlengingu á fjárhagstengi á [Vélbúnaðarstöð](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) eða the [POS skrá](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network).

#### <a name="enable-hardware-station-extensions"></a>Virkja viðbætur fyrir vélbúnaðarstöð

Viðbótarhlutir vélbúnaðarstöðvar eru innifaldir í sýnishornum fyrir vélbúnaðarstöð. Til að ljúka eftirfarandi aðferðum skaltu opna **HardwareStationSamples.sln** lausn undir **RetailSdk\\ SampleExtensions\\ Vélbúnaðarstöð**.

##### <a name="efrsample-component"></a>EFRSample hluti

1. Finndu **HardwareStation.Extension.EFRSample** verkefni, og byggja það.
2. Í **Framlenging.EFRSample\\ bin\\ Villuleit** möppu, finndu eftirfarandi samsetningarskrár:

    - Contoso.Commerce.HardwareStation.EFRSample.dll
    - Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll

3. Afritaðu samsetningarskrárnar í möppuna Vélbúnaðarstöðvarviðbætur:

    - **Sameiginleg vélbúnaðarstöð:** Afritaðu skrárnar í **bin** möppu undir staðsetningu IIS vélbúnaðarstöðvar.
    - **Sérstök vélbúnaðarstöð á Modern POS:** Afritaðu skrárnar á miðlarastað Modern POS viðskiptavinar.

4. Finna skilgreiningarskrá nafnaukans fyrir viðbætur Vélbúnaðarstöðvarinnar. Skráin heitir **HardwareStation.Extension.config**.

    - **Sameiginleg vélbúnaðarstöð:** Skráin er staðsett undir staðsetningu IIS vélbúnaðarstöðvarinnar.
    - **Sérstök vélbúnaðarstöð á Modern POS:** Skráin er staðsett undir miðlarastað Modern POS viðskiptavinar.

5. Bætið eftirfarandi línu við **samsetningarhluta** skilgreiningarskrárinnar.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample.dll" />
    ```

#### <a name="enable-pos-extensions"></a>Virkja POS viðbætur

Sýnishorn af POS framlengingu er staðsett í **src\\ Fiscal Integration\\ PosFiscalConnectorSample** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla.

Fylgdu þessum skrefum til að nota sýnishorn af POS viðbótinni í eldri SDK.

1. Afritaðu **Pos.Extension** möppu í POS **Framlengingar** möppu eldri SDK (til dæmis,`C:\RetailSDK\src\POS\Extensions`).
1. Endurnefna afritið af **Pos.Extension** möppu **PosFiscalConnector**.
1. Fjarlægðu eftirfarandi möppur og skrár úr **PosFiscalConnector** mappa:

    - karfa
    - DataService
    - devDependencies
    - Söfn
    - obj
    - Contoso.PosFiscalConnectorSample.Pos.csproj
    - RetailServerEdmxModel.g.xml
    - tsconfig.json

1. Opnaðu **CloudPos.sln** eða **ModernPos.sln** lausn.
1. Í **Pos.Viðbætur** verkefni, fela í sér **PosFiscalConnector** möppu.
1. Opnaðu **extensions.json** skrá og bættu við **PosFiscalConnector** framlenging.
1. Byggja SDK.

### <a name="enable-modern-pos-extension-components"></a>Virkja nútíma íhluti posaviðauka

1. **Opnaðu ModernPOS.sln** lausnina undir **RetailSdk\\ POS** og gakktu úr skugga um að hægt sé að þýða hana án villna. Að auki skal ganga úr skugga um að hægt sé að keyra Modern POS úr Visual Studio með því að nota skipunina **Keyra**.

    > [!NOTE]
    > Ekki má aðlaga nútíma posa. Virkja verður stjórnun notendareikninga (UAC) og fjarlægja verður áður uppsett tilvik af Modern POS eftir þörfum.

2. Gerðu kleift að hlaða viðbótunum með því að bæta við eftirfarandi línum í **extensions.json** skrá.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > Frekari upplýsingar og fyrir sýni sem sýna hvernig á að taka með möppur frumkóða og gera kleift að hlaða inn viðbótum er að finna í leiðbeiningunum í readme.md skránni **í Pos.Extensions** verkefninu.

3. Endurbyggja lausnina.
4. Keyra skal Modern POS í kembiforritinu og prófa virknina.

### <a name="enable-cloud-pos-extension-components"></a>Virkja cloud POS viðbótaríhluti

1. **Opnaðu CloudPOS.sln** lausnina undir **RetailSdk\\ POS** og gakktu úr skugga um að hægt sé að þýða hana án villna.
2. Gerðu kleift að hlaða viðbótunum með því að bæta við eftirfarandi línum í **extensions.json** skrá.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > Frekari upplýsingar og fyrir sýni sem sýna hvernig á að taka með möppur frumkóða og gera kleift að hlaða inn viðbótum er að finna í leiðbeiningunum í readme.md skránni **í Pos.Extensions** verkefninu.

3. Endurbyggja lausnina.
4. Keyrið lausnina með skipuninni **Keyra** og fylgið skrefunum í smásölu SDK handbókinni.

## <a name="production-environment"></a>Framleiðsluumhverfi

Fyrri aðferðin gerir viðbætur sem eru hluti af samþættingarúrtaki fjárhagsskráningarþjónustu virkjað. Að auki verður að fylgja þessum skrefum til að búa til virkjanlega pakka sem innihalda viðskiptaíhluti og nota þá pakka í framleiðsluumhverfi.

1. Gera eftirfarandi breytingar á samskipanarskrám pakka í möppunni **RetailSdk\\ Assets**:

    - Í skilgreiningarskránum commerceruntime.ext.config og CommerceRuntime.MPOSOffline.Ext.config **skal bæta eftirfarandi línum við samsetningarhlutann** **.** **·**

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
        ```

    - Í skilgreiningarskránni HardwareStation.Extension.config **er eftirfarandi línu bætt við samsetningarhlutann** **.**

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

2. Gera eftirfarandi breytingar í **customization.settings sérsniðssamstillingarskrá customization.settings** pakkans **undir BuildTools** möppunni:

    - Bættu við eftirfarandi línum til að innihalda CRT viðbætur í dreifanlegum pökkum.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - Bættu við eftirfarandi línu til að innihalda viðbótina fyrir vélbúnaðarstöðina í pakkanum sem hægt er að nota.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

3. Ræsa skipanakvaðningu MSBuild fyrir Visual Studio forrit og keyra **msbuild** undir möppunni Retail SDK til að búa til virkjanlega pakka.
4. Notaðu pakkana með LCS eða handvirkt. Sjá Create deployable packages [fyrir frekari upplýsingar](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. Ljúktu við öll nauðsynleg uppsetningarverk sem lýst er í [Settu upp Commerce fyrir Austurríki](emea-aut-fi-sample.md#set-up-commerce-for-austria).

## <a name="design-of-extensions"></a>Hönnun viðbygginga

Samþættingarúrtak ríkisskráningarþjónustu fyrir Austurríki byggist á [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md). Fyrir frekari upplýsingar um hönnun fjárhagslegrar samþættingarlausnar, sjá [yfirlit yfir sýnishönnun fjárhagslega samþættingar](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>Viðskiptatímaframlengingarhönnun

Tilgangur framlengingarinnar sem er ríkisfjármálaskjalaveita er að búa til þjónustusértæk skjöl og annast svör frá ríkisskráningarþjónustunni.

The CRT framlenging er **Runtime.Extensions.DocumentProvider.EFRSample**.

#### <a name="request-handler"></a>Biðja um rekil

Það eru tveir beiðnaraðilar fyrir skjalaveitendur:

- **DocumentProviderEFRFiscalAUT** – Þessi meðhöndlun er notuð til að búa til fjárhagsskjöl fyrir fjárhagsskráningarþjónustuna.
- **DocumentProviderEFRNonFiscalAUT** – Þessi meðhöndlun er notuð til að búa til skjöl sem ekki eru fjárhagsleg skjöl fyrir skattaskráningarþjónustuna.

Þessir meðhöndlarar eru í arf frá **INAmedRequestHandler** viðmót. HandlerName **aðferðin** ber ábyrgð á að skila nafni rekilsins. Heiti rekils ætti að samsvara heiti tengiskjalsveitunnar sem er tilgreint í höfuðstöðvum Commerce.

Tengið styður eftirfarandi beiðnir:

- **GetFiscalDocumentDocumentProviderRequest** – Þessi beiðni inniheldur upplýsingar um hvaða skjal á að mynda. Það skilar þjónustusértæku skjali sem ætti að vera skráð í ríkisskráningarþjónustunni.
- **GetNonFiscalDocumentDocumentProviderRequest** – Þessi beiðni inniheldur upplýsingar um hvaða skjal sem ekki er ríkisfjármál ætti að búa til. Það skilar þjónustusértæku skjali sem ætti að vera skráð í ríkisskráningarþjónustunni.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Þessi beiðni skilar lista yfir tilvik sem á að gerast áskrifandi að. Eins og er, eru eftirfarandi atburðir studdir: sala, prentun X skýrslu, prentun Z skýrslu, innlán á viðskiptareikningi, pöntun viðskiptavina, endurskoðunarviðburði og viðskipti sem ekki eru sölu.
- **Get FiscalRegisterResponseToSaveDocumentProviderRequest** – Þessi beiðni skilar svari frá skattskráningarþjónustunni. Þetta svar er sett í röð til að mynda streng þannig að það sé tilbúið til vistunar.

#### <a name="configuration"></a>Skilgreining

Stillingarskrárnar eru staðsettar í **Stillingar** mappa viðbyggingarverkefnisins:

- **DocumentProviderFiscalEFRSampleAustria** – Fyrir ríkisfjármálaskjöl.
- **DocumentProviderNonFiscalEFRSampleAustria** – Fyrir skjöl sem ekki eru í ríkisfjármálum.

Tilgangur þessara skráa er að gera stillingar fyrir skjalaveituna kleift að stilla frá höfuðstöðvum Commerce. Skráarsniðið er í takt við þarfir fyrir skilgreiningu fjárhagssamþættingar. Eftirfarandi stillingu er bætt við:

- Vörpun VSK-hlutfalls

### <a name="hardware-station-extension-design"></a>Viðaukahönnun vélbúnaðarstöðvar

Tilgangurinn með framlengingunni á fjárhagstenginu er að hafa samskipti við ríkisskráningarþjónustuna. Viðbygging vélbúnaðarstöðvar er nefnd **HardwareStation.Extension.EFRSample**. Það notar HTTP eða HTTPS samskiptareglur til að leggja fram skjöl sem CRT framlenging myndar við skattskráningarþjónustuna. Það sér einnig um svör sem berast frá ríkisskráningarþjónustu.

#### <a name="request-handler"></a>Biðja um rekil

The **EFRHandler** meðhöndlun beiðna er inngangsstaður fyrir meðhöndlun beiðna til skattskráningarþjónustunnar.

Rekillinn erfist frá viðmótinu **INamedRequestHandler**. HandlerName **aðferðin** ber ábyrgð á að skila nafni rekilsins. Heiti rekils ætti að samsvara heiti fjárhagstengisins sem er tilgreint í höfuðstöðvum Commerce.

Tengið styður eftirfarandi beiðnir:

- **Senda innDocumentFiscalDeviceRequest** – Þessi beiðni sendir skjöl til ríkisskráningarþjónustunnar og skilar svari frá henni.
- **IsReadyFiscalDeviceRequest** – Þessi beiðni er notuð við heilsufarsskoðun hjá ríkisskráningarþjónustunni.
- **Frumstilla FiscalDeviceRequest** – Þessi beiðni er notuð til að frumstilla fjárhagsskráningarþjónustuna.

#### <a name="configuration"></a>Skilgreining

Stillingarskráin er staðsett í **Stillingar** möppu framlengingarverkefnisins. Tilgangur skrárinnar er að virkja stillingar fyrir fjárhagstengið sem skilgreina á úr höfuðstöðvum Commerce. Skráarsniðið er í takt við þarfir fyrir skilgreiningu fjárhagssamþættingar. Eftirfarandi stillingum er bætt við:

- **Heimilisfang endapunkts** – Vefslóð ríkisskráningarþjónustunnar.
- **Hlé** – Tíminn, í millisekúndum, sem ökumaður bíður eftir svari frá skattskráningarþjónustunni.

### <a name="pos-fiscal-connector-extension-design"></a>Hönnun POS fjárhagstengisframlengingar

Tilgangur POS fjárhagstengiviðbótar er að hafa samskipti við fjárhagsskráningarþjónustuna frá POS. Það notar HTTPS samskiptareglur fyrir samskipti.

#### <a name="fiscal-connector-factory"></a>Fiskal tengiverksmiðju

Fjárhagstengjaverksmiðjan kortleggur nafn tengisins við útfærslu fjárhagstengisins og er staðsett í **Pos.Extension\\ Tengi\\ FiscalConnectorFactory.ts** skrá. Nafn tengisins ætti að passa við nafn fjárhagstengis sem er tilgreint í höfuðstöðvum Commerce.

#### <a name="efr-fiscal-connector"></a>EFR fjárhagslega tengi

Fjárhagstenging EFR er staðsett í **Pos.Extension\\ Tengi\\ Efr\\ EfrFiscalConnector.ts** skrá. Það útfærir **IFiscalConnector** viðmót sem styður eftirfarandi beiðnir:

- **FiscalRegisterSubmitDocumentClientRequest** – Þessi beiðni sendir skjöl til ríkisskráningarþjónustunnar og skilar svari frá henni.
- **FiscalRegisterIsReadyClientRequest** – Þessi beiðni er notuð við heilsufarsskoðun hjá ríkisskráningarþjónustunni.
- **FiscalRegisterInitializeClientRequest** – Þessi beiðni er notuð til að frumstilla fjárhagsskráningarþjónustuna.

#### <a name="configuration"></a>Skilgreining

Stillingarskráin er staðsett í **src\\ FiscalIntegration\\ Efr\\ Stillingar\\ Tengi** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla. Tilgangur skrárinnar er að virkja stillingar fyrir fjárhagstengið sem skilgreina á úr höfuðstöðvum Commerce. Skráarsniðið er í takt við þarfir fyrir skilgreiningu fjárhagssamþættingar. Eftirfarandi stillingum er bætt við:

- **Heimilisfang endapunkts** – Vefslóð ríkisskráningarþjónustunnar.
- **Hlé** – Tíminn, í millisekúndum, sem tengið bíður eftir svari frá skattskráningarþjónustunni.
