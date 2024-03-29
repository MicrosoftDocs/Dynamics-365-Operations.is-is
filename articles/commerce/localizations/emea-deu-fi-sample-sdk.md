---
title: Dreifingarleiðbeiningar fyrir samþættingarsýnishorn ríkisskráningarþjónustu fyrir Þýskaland (arfleifð)
description: Þessi grein veitir leiðbeiningar um að dreifa sýnishorni um samþættingu ríkisfjármála fyrir Þýskaland frá Microsoft Dynamics 365 Commerce Smásöluhugbúnaðarþróunarsett (SDK).
author: EvgenyPopovMBS
ms.date: 08/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 7315b6bb145ccdc5631a558af88de55660ebf877
ms.sourcegitcommit: 0feb5d0b06e04f99903069ff2801577be86b8555
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/18/2022
ms.locfileid: "9313856"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-germany-legacy"></a>Dreifingarleiðbeiningar fyrir samþættingarsýnishorn ríkisskráningarþjónustu fyrir Þýskaland (arfleifð)

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Þú verður að fylgja leiðbeiningunum í þessari grein aðeins ef þú ert að nota Microsoft Dynamics 365 Commerce útgáfu 10.0.28 eða eldri. Frá og með útgáfu Commerce 10.0.29 er samþættingarsýnishorn fyrir skattaskráningarþjónustu fyrir Þýskaland fáanlegt í Commerce hugbúnaðarþróunarsettinu (SDK). Fyrir frekari upplýsingar, sjá [Stilltu rásaríhluti](./emea-deu-fi-sample.md#configure-channel-components).

Þessi grein veitir leiðbeiningar um útfærslu samþættingarsýnis fyrir ríkisskráningarþjónustu fyrir Þýskaland frá Dynamics 365 Commerce Smásölu-SDK á sýndarvél fyrir þróunaraðila (VM) í Microsoft Dynamics Lífsferilsþjónusta (LCS). Fyrir frekari upplýsingar um þetta sýnishorn af samþættingu ríkisfjármála, sjá [Samþættingarsýni skattaskráningarþjónustu fyrir Þýskaland](emea-deu-fi-sample.md). 

Úrtak ríkisfjármálasamþættingar fyrir Þýskaland er hluti af Retail SDK. Fyrir upplýsingar um hvernig á að setja upp og nota SDK, sjá [Smásala hugbúnaðarþróunarsett (SDK) arkitektúr](../dev-itpro/retail-sdk/retail-sdk-overview.md). Þetta sýnishorn samanstendur af viðbótum fyrir Commerce runtime (CRT) og Vélbúnaðarstöð. Til að keyra þetta sýnishorn verður þú að breyta og byggja upp CRT og Vélbúnaðarstöðvarverkefni. Við mælum með að þú notir óbreytt Retail SDK til að gera þær breytingar sem lýst er í þessari grein. Við mælum líka með því að þú notir heimildastýringarkerfi eins og Azure DevOps þar sem engum skrám hefur verið breytt ennþá.

## <a name="development-environment"></a>Þróunarumhverfi

Fylgdu þessum skrefum til að setja upp þróunarumhverfi svo þú getir prófað og framlengt sýnishornið.

### <a name="enable-commerce-runtime-extensions"></a>Virkjaðu Commerce runtime viðbætur

The CRT framlengingarhlutir eru innifalin í CRT sýnishorn. Til að ljúka eftirfarandi aðferðum skaltu opna **CommerceRuntimeSamples.sln** lausn undir **RetailSdk\\ SampleExtensions\\ CommerceRuntime**.

#### <a name="documentproviderefrsample-component"></a>DocumentProvider.EFRSample hluti

1. Finndu **Runtime.Extensions.DocumentProvider.EFRSample** verkefnið og byggja það.
2. Í **Runtime.Extensions.DocumentProvider.EFRSample\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána í CRT viðbætur mappa:

    - **Eining viðskiptaskala:** Afritaðu skrána í **\\ bin\\ ext** möppu undir staðsetningu Internet Information Services (IIS) Commerce Scale Unit.
    - **Staðbundið CRT á Modern POS:** Afritaðu skrána í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavinar.

4. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Eining viðskiptaskala:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningu IIS Commerce Scale Unit.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavinar.

5. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
    ```

#### <a name="documentproviderdatamodelefr-component"></a>DocumentProvider.DataModelEFR hluti

1. Finndu **Runtime.Extensions.DocumentProvider.DataModelEFR** verkefnið og byggja það.
2. Í **Runtime.Extensions.DocumentProvider.DataModelEFR\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána í CRT viðbætur mappa:

    - **Eining viðskiptaskala:** Afritaðu skrána í **\\ bin\\ ext** möppu undir staðsetningu IIS Commerce Scale Unit.
    - **Staðbundið CRT á Modern POS:** Afritaðu skrána í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavinar.

4. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Eining viðskiptaskala:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningu IIS Commerce Scale Unit.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavinar.

5. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="extension-configuration-file"></a>Stillingarskrá fyrir viðbætur

1. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Eining viðskiptaskala:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningu IIS Commerce Scale Unit.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavinar.

2. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsGermany" />
    ```

### <a name="enable-fiscal-connector-extensions"></a>Virkja framlengingu á fjárhagslegum tengingum

Þú getur virkjað framlengingu á fjárhagstengjum á [Vélbúnaðarstöð](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) eða the [POS skrá](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network).

#### <a name="enable-hardware-station-extensions"></a>Virkja viðbætur fyrir vélbúnaðarstöð

Vélbúnaðarstöðvarframlengingarhlutirnir eru innifalin í vélbúnaðarstöðvunum. Til að ljúka eftirfarandi aðferðum skaltu opna **HardwareStationSamples.sln** lausn undir **RetailSdk\\ SampleExtensions\\ Vélbúnaðarstöð**.

##### <a name="efrsample-component"></a>EFRSample hluti

1. Finndu **HardwareStation.Extension.EFRSample** verkefnið og byggja það.
2. Í **Framlenging.EFRSample\\ bin\\ Villuleit** möppu, finndu eftirfarandi samsetningarskrár:

    - Contoso.Commerce.HardwareStation.EFRSample.dll
    - Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll

3. Afritaðu samsetningarskrárnar í möppuna Vélbúnaðarstöðvarviðbætur:

    - **Sameiginleg vélbúnaðarstöð:** Afritaðu skrárnar í **bin** möppu undir staðsetningu IIS vélbúnaðarstöðvar.
    - **Sérstök vélbúnaðarstöð á Modern POS:** Afritaðu skrárnar á miðlarastað Modern POS viðskiptavinar.

4. Finndu stillingarskrá fyrir viðbótina fyrir viðbætur vélbúnaðarstöðvarinnar. Skráin er nefnd **HardwareStation.Extension.config**.

    - **Sameiginleg vélbúnaðarstöð:** Skráin er staðsett undir staðsetningu IIS vélbúnaðarstöðvarinnar.
    - **Sérstök vélbúnaðarstöð á Modern POS:** Skráin er staðsett undir miðlarastaðnum Modern POS viðskiptavinar.

5. Bættu eftirfarandi línu við **samsetningu** hluta stillingarskrárinnar.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample.dll" />
    ```

#### <a name="enable-pos-extensions"></a>Virkja POS viðbætur

Sýnishorn af POS framlengingu er staðsett í **src\\ Fiscal Integration\\ PosFiscalConnectorSample** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla.

Fylgdu þessum skrefum til að nota sýnishorn af POS viðbótum í eldri SDK.

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
1. Í **Pos.Extensions** verkefni, fela í sér **PosFiscalConnector** möppu.
1. Opnaðu **extensions.json** skrá og bættu við **PosFiscalConnector** framlenging.
1. Byggja SDK.

### <a name="production-environment"></a>Framleiðsluumhverfi

Í fyrra ferli virkjaðirðu viðbæturnar sem eru hluti af samþættingarsýnishorni fjárhagsskráningarþjónustunnar. Að auki verður þú að fylgja þessum skrefum til að búa til dreifanlega pakka sem innihalda Commerce íhluti og nota þá pakka í framleiðsluumhverfi.

1. Gerðu eftirfarandi breytingar á stillingarskrám pakkans undir **RetailSdk\\ Eignir** mappa:

    - Í **commerceruntime.ext.config** og **CommerceRuntime.MPOSOffline.Ext.config** stillingarskrár skaltu bæta eftirfarandi línum við **samsetningu** kafla.

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsGermany" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

    - Í **HardwareStation.Extension.config** stillingarskrá skaltu bæta eftirfarandi línum við **samsetningu** kafla.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

2. Gerðu eftirfarandi breytingar á **Customization.settings** stillingarskrá fyrir sérsniðna pakka undir **Byggingarverkfæri** mappa:

    - Bættu við eftirfarandi línum til að innihalda CRT viðbætur í dreifanlegum pökkum.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - Bættu við eftirfarandi línum til að innihalda vélbúnaðarstöðvarviðbæturnar í pakkanum sem hægt er að nota.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

3. Ræstu MSBuild Command Prompt fyrir Visual Studio gagnsemi, og keyra **msbuild** undir Retail SDK möppunni til að búa til dreianlega pakka.
4. Notaðu pakkana í gegnum LCS eða handvirkt. Fyrir frekari upplýsingar, sjá [Búðu til pakka sem hægt er að nota](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. Ljúktu við öll nauðsynleg uppsetningarverk sem lýst er í [Settu upp Commerce fyrir Þýskaland](emea-deu-fi-sample.md#set-up-commerce-for-germany).

## <a name="design-of-extensions"></a>Hönnun viðbygginga

Samþættingarúrtak ríkisskráningarþjónustu fyrir Þýskaland er byggt á [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md). Fyrir frekari upplýsingar um hönnun fjárhagslegrar samþættingarlausnar, sjá [yfirlit yfir sýnishönnun fjárhagslega samþættingar](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>Viðskiptatímaframlengingarhönnun

Tilgangur framlengingarinnar sem er ríkisfjármálaskjalaveita er að búa til þjónustusértæk skjöl og annast svör frá ríkisskráningarþjónustunni.

The CRT framlenging er **Runtime.Extensions.DocumentProvider.EFRSample**. Fyrir frekari upplýsingar um hönnun fjárhagslegrar samþættingarlausnar, sjá [Yfirlit yfir samþættingu ríkisfjármála fyrir viðskiptarásir](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Beiðni um stjórnanda

Það er einn meðhöndlun beiðna fyrir skjalaveituna, **DocumentProviderEFRFiscalDEU**. Þessi meðhöndlun er notuð til að búa til fjárhagsskjöl fyrir fjárhagsskráningarþjónustuna. Það er erft frá **INAmedRequestHandler** viðmót. The **HandlerName** aðferð er ábyrg fyrir því að skila nafni stjórnanda. Nafn meðhöndlunar ætti að passa við heiti tengiskjalsveitu sem er tilgreint í höfuðstöðvum Commerce.

Tengið styður eftirfarandi beiðnir:

- **GetFiscalDocumentDocumentProviderRequest** – Þessi beiðni inniheldur upplýsingar um hvaða skjal ætti að búa til. Það skilar þjónustusértæku skjali sem ætti að vera skráð í skattaskráningarþjónustuna.
- **GetFiscalTransactionExtendedDataDocumentProviderRequest** – Þessi beiðni skilar svarinu ásamt útvíkkuðum gögnum.

#### <a name="configuration"></a>Skilgreining

The **DocumentProviderFiscalEFRSampleGermany** stillingarskrá er staðsett í **Stillingar** möppu framlengingarverkefnisins. Tilgangur þessarar skráar er að gera stillingar fyrir skjalaveituna kleift að stilla frá höfuðstöðvum Commerce. Skráarsniðið er í samræmi við kröfurnar fyrir fjárhagslega samþættingu stillingar.

Eftirfarandi stillingum er bætt við:

- **Kortlagning virðisaukaskattshlutfalla** – Kortlagning skattprósentugilda sem eru sett upp fyrir vsk-kóða við gildi á **TaxG** (skattflokkur) eigind í beiðnum sem sendar eru til ríkisskattstjóra.
- **Skattflokkur fyrir gjafakort og innlán** - Verðmæti **TaxG** eigind í beiðnum sem sendar eru til ríkisfjármála, byggt á rekstri sem felur í sér gjafakort eða innborgun.
- **Kortlagning útboðstegunda** – Kortlagning greiðslumáta við gildi á **BorgaG** (greiðsluhópur) eigind í beiðnum sem sendar eru til ríkisfjármála.
- **Skattflokkur undanþeginn virðisaukaskatti** - Verðmæti **TaxG** eigind í beiðnum sem sendar eru til ríkisfjármála, byggt á rekstri sem er undanþeginn skattskyldu.
- **Láttu gögn viðskiptavina fylgja með** – Ef kveikt er á þessari færibreytu munu beiðnir til fjárhagsþjónustunnar innihalda upplýsingar um viðskiptavini, svo sem nöfn og heimilisföng, í þeim tilvikum þar sem viðskiptavinur er bætt við færslu.

### <a name="hardware-station-extension-design"></a>Hönnun vélbúnaðarstöðvar viðbyggingar

Tilgangur framlengingarinnar sem er fjárhagstengi er að hafa samskipti við skattskráningarþjónustuna.

Viðbygging Vélbúnaðarstöðvar er **HardwareStation.Extension.EFRSample**. Það notar HTTP samskiptareglur til að leggja fram skjöl sem CRT framlenging myndar við skattskráningarþjónustuna. Það annast einnig svör sem berast frá ríkisskráningarþjónustu.

#### <a name="request-handler"></a>Beiðni um stjórnanda

The **EFRHandler** meðhöndlun beiðna er inngangsstaður fyrir meðhöndlun beiðna til skattskráningarþjónustunnar. Þessi stjórnandi er arfur frá **INAmedRequestHandler** viðmót. The **HandlerName** aðferð er ábyrg fyrir því að skila nafni stjórnanda. Nafn meðhöndlunar ætti að passa við nafn fjárhagstengis sem er tilgreint í höfuðstöðvum Commerce.

Tengið styður eftirfarandi beiðnir:

- **SubmitDocumentFiscalDeviceRequest** – Þessi beiðni sendir skjöl til ríkisskráningarþjónustunnar og skilar svari frá henni.
- **IsReadyFiscalDeviceRequest** – Þessi beiðni er notuð við heilsufarsskoðun hjá ríkisskráningarþjónustunni.
- **Frumstilla FiscalDeviceRequest** – Þessi beiðni er notuð til að frumstilla fjárhagsskráningarþjónustuna.

#### <a name="configuration"></a>Skilgreining

Stillingarskráin er staðsett í **Stillingar** möppu framlengingarverkefnisins. Tilgangur skrárinnar er að gera stillingar fyrir fjárhagslega tengið kleift að stilla frá höfuðstöðvum Commerce. Skráarsniðið er í samræmi við kröfurnar fyrir fjárhagslega samþættingu stillingar.

Eftirfarandi stillingum er bætt við:

- **Heimilisfang endapunkts** – Vefslóð ríkisskráningarþjónustunnar.
- **Hlé** – Tíminn, í millisekúndum (ms), sem ökumaður mun bíða eftir svari frá skattskráningarþjónustunni.
- **Sýna tilkynningar um skattaskráningu** – Ef kveikt er á þessari færibreytu munu tilkynningar frá fjárhagsþjónustunni birtast sem notendaskilaboð á POS.

### <a name="pos-fiscal-connector-extension-design"></a>Framlengingarhönnun POS fjárhagstengis

Tilgangur POS fjárhagstengingarviðbótar er að hafa samskipti við fjárhagsskráningarþjónustuna frá POS. Það notar HTTPS samskiptareglur fyrir samskipti.

#### <a name="fiscal-connector-factory"></a>Fiskal tengiverksmiðju

Fjárhagstengjaverksmiðjan kortleggur nafn tengisins við útfærslu fjárhagstengisins og er staðsett í **Pos.Extension\\ Tengi\\ FiscalConnectorFactory.ts** skrá. Nafn tengisins ætti að passa við nafn fjárhagstengis sem tilgreint er í höfuðstöðvum Commerce.

#### <a name="efr-fiscal-connector"></a>EFR fjárhagslega tengi

Fjárhagstenging EFR er staðsett í **Pos.Extension\\ Tengi\\ Efr\\ EfrFiscalConnector.ts** skrá. Það útfærir **IFiscalConnector** viðmót sem styður eftirfarandi beiðnir:

- **FiscalRegisterSubmitDocumentClientRequest** – Þessi beiðni sendir skjöl til ríkisskráningarþjónustunnar og skilar svari frá henni.
- **FiscalRegisterIsReadyClientRequest** – Þessi beiðni er notuð við heilsufarsskoðun hjá ríkisskráningarþjónustunni.
- **FiscalRegisterInitializeClientRequest** – Þessi beiðni er notuð til að frumstilla fjárhagsskráningarþjónustuna.

#### <a name="configuration"></a>Skilgreining

Stillingarskráin er staðsett í **src\\ Fiscal Integration\\ Efr\\ Stillingar\\ Tengi** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla. Tilgangur skrárinnar er að gera stillingar fyrir fjárhagslega tengið kleift að stilla frá höfuðstöðvum Commerce. Skráarsniðið er í samræmi við kröfurnar fyrir fjárhagslega samþættingu stillingar. Eftirfarandi stillingum er bætt við:

- **Heimilisfang endapunkts** – Vefslóð ríkisskráningarþjónustunnar.
- **Hlé** – Tíminn, í millisekúndum, sem tengið mun bíða eftir svari frá skattskráningarþjónustunni.
