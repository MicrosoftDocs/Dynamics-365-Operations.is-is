---
title: Leiðbeiningar um dreifingu fyrir samþættingarsýni stjórneiningar fyrir Svíþjóð (arfleifð)
description: Þessi grein veitir leiðbeiningar um útfærslu samþættingarsýnis stýrieininga fyrir Svíþjóð frá Retail SDK
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: fcc35a2203641b24fe4edd2ab34f2e4d5db9bb53
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324298"
---
# <a name="deployment-guidelines-for-the-control-unit-integration-sample-for-sweden-legacy"></a>Leiðbeiningar um dreifingu fyrir samþættingarsýni stjórneiningar fyrir Svíþjóð (arfleifð)

[!include [banner](../includes/banner.md)]

Þessi grein veitir leiðbeiningar um uppsetningu samþættingarsýnis stýrieininga fyrir Svíþjóð úr smásöluhugbúnaðarþróunarsettinu (SDK) á sýndarvél þróunaraðila (VM) í Microsoft Dynamics Lífsferilsþjónusta (LCS). Fyrir frekari upplýsingar um þetta sýnishorn af samþættingu ríkisfjármála, sjá [Samþættingarsýni stjórneiningar fyrir Svíþjóð](emea-swe-fi-sample.md). 

Fjármálasamþættingarúrtakið fyrir Svíþjóð er hluti af Retail SDK. Fyrir upplýsingar um hvernig á að setja upp og nota SDK, sjá [Smásala hugbúnaðarþróunarsett (SDK) arkitektúr](../dev-itpro/retail-sdk/retail-sdk-overview.md). Þetta sýnishorn samanstendur af viðbótum fyrir Commerce runtime (CRT), Vélbúnaðarstöð og sölustaður (POS). Til að keyra þetta sýnishorn verður þú að breyta og byggja upp CRT, Vélbúnaðarstöð og POS verkefni. Við mælum með að þú notir óbreytt Retail SDK til að gera þær breytingar sem lýst er í þessari grein. Við mælum líka með því að þú notir heimildastýringarkerfi eins og Azure DevOps þar sem engum skrám hefur verið breytt ennþá.

## <a name="development-environment"></a>Þróunarumhverfi

Fylgdu þessum skrefum til að setja upp þróunarumhverfi svo þú getir prófað og framlengt sýnishornið.

### <a name="enable-crt-extensions"></a>Virkja CRT framlengingar

The CRT framlengingarhlutir eru innifalin í CRT sýnishorn. Til að ljúka eftirfarandi aðferðum skaltu opna **CommerceRuntimeSamples.sln** lausn undir **RetailSdk\\ SampleExtensions\\ CommerceRuntime**.

#### <a name="documentprovidercleancashsample-component"></a>DocumentProvider.CleanCashSample hluti

1. Finndu **Runtime.Extensions.DocumentProvider.CleanCashSample** verkefnið og byggja það.
2. Í **Runtime.Extensions.DocumentProvider.CleanCashSample\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána í CRT viðbætur mappa:

    - **Eining viðskiptaskala:** Afritaðu skrána í **\\ bin\\ ext** möppu undir staðsetningu Internet Information Services (IIS) Commerce Scale Unit.
    - **Staðbundið CRT á Modern POS:** Afritaðu skrána í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavinar.

4. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Eining viðskiptaskala:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningu IIS Commerce Scale Unit.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavinar.

5. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    ```

#### <a name="extension-configuration-file"></a>Stillingarskrá fyrir viðbætur

1. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Eining viðskiptaskala:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningu IIS Commerce Scale Unit.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavinar.

2. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

### <a name="enable-hardware-station-extensions"></a>Virkja viðbætur fyrir vélbúnaðarstöð

Vélbúnaðarstöðvarframlengingarhlutirnir eru innifalin í vélbúnaðarstöðvunum. Til að ljúka eftirfarandi aðferðum skaltu opna **HardwareStationSamples.sln** lausn undir **RetailSdk\\ SampleExtensions\\ Vélbúnaðarstöð**.

#### <a name="cleancash-component"></a>CleanCash hluti

1. Finndu **HardwareStation.Extension.CleanCashSample** verkefnið og byggja það.
2. Í **Extension.CleanCashSample\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.HardwareStation.CleanCashSample.dll** og **Interop.CleanCash\_ 1\_ 1.dll** samsetningarskrár.
3. Afritaðu samsetningarskrárnar í möppuna Vélbúnaðarstöðvarviðbætur:

    - **Sameiginleg vélbúnaðarstöð:** Afritaðu skrárnar í **bin** möppu undir staðsetningu IIS vélbúnaðarstöðvar.
    - **Sérstök vélbúnaðarstöð á Modern POS:** Afritaðu skrárnar á miðlarastað Modern POS viðskiptavinar.

4. Finndu stillingarskrá fyrir viðbótina fyrir viðbætur vélbúnaðarstöðvarinnar. Skráin er nefnd **HardwareStation.Extension.config**.

    - **Sameiginleg vélbúnaðarstöð:** Skráin er undir staðsetningu IIS vélbúnaðarstöðvar.
    - **Sérstök vélbúnaðarstöð á Modern POS:** Skráin er undir miðlarastaðnum Modern POS viðskiptavinar.

5. Bættu eftirfarandi línu við **samsetningu** hluta stillingarskrárinnar.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

### <a name="enable-modern-pos-extension-components"></a>Virkjaðu nútíma POS viðbótahluta

1. Opnaðu **ModernPOS.sln** lausn undir **RetailSdk\\ POS**, og vertu viss um að hægt sé að setja hana saman án villna. Að auki, vertu viss um að þú getir keyrt Modern POS frá Visual Studio með því að nota **Hlaupa** skipun.

    > [!NOTE]
    > Nútíma POS má ekki aðlaga. Þú verður að virkja User Account Control (UAC) og þú verður að fjarlægja áður uppsett tilvik af Modern POS eftir þörfum.

2. Virkjaðu viðbæturnar sem þarf að hlaða með því að bæta við eftirfarandi línum í **extensions.json** skrá.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

    > [!NOTE]
    > Fyrir frekari upplýsingar og fyrir sýnishorn sem sýna hvernig á að innihalda frumkóðamöppur og gera kleift að hlaða viðbótum, sjáðu leiðbeiningarnar í readme.md skránni í **Pos.Extensions** verkefni.

3. Endurbyggðu lausnina.
4. Keyrðu Modern POS í villuleitinni og prófaðu virknina.

### <a name="enable-cloud-pos-extension-components"></a>Virkjaðu Cloud POS viðbótina

1. Opnaðu **CloudPOS.sln** lausn undir **RetailSdk\\ POS**, og vertu viss um að hægt sé að setja hana saman án villna.
2. Virkjaðu viðbæturnar sem þarf að hlaða með því að bæta við eftirfarandi línum í **extensions.json** skrá.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

    > [!NOTE]
    > Fyrir frekari upplýsingar og fyrir sýnishorn sem sýna hvernig á að innihalda frumkóðamöppur og gera kleift að hlaða viðbótum, sjáðu leiðbeiningarnar í readme.md skránni í **Pos.Extensions** verkefni.

3. Endurbyggðu lausnina.
4. Keyrðu lausnina með því að nota **Hlaupa** skipuninni og fylgdu skrefunum í Retail SDK handbókinni.

## <a name="production-environment"></a>Framleiðsluumhverfi

Fyrri aðferð virkjar viðbætur sem eru hluti af samþættingarsýni stjórneininga. Að auki verður þú að fylgja þessum skrefum til að búa til dreifanlega pakka sem innihalda Commerce íhluti og nota þá pakka í framleiðsluumhverfi.

1. Gerðu eftirfarandi breytingar á stillingarskrám pakkans undir **RetailSdk\\ Eignir** mappa:

    - Í **commerceruntime.ext.config** og **CommerceRuntime.MPOSOffline.Ext.config** stillingarskrár skaltu bæta eftirfarandi línum við **samsetningu** kafla.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
        ```

    - Í **HardwareStation.Extension.config** stillingarskrá skaltu bæta eftirfarandi línu við **samsetningu** kafla.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
        ```

2. Gerðu eftirfarandi breytingar á **Customization.settings** stillingarskrá fyrir sérsniðna pakka undir **Byggingarverkfæri** mappa:

    - Bættu við eftirfarandi línu til að innihalda CRT viðbætur í dreifanlegum pökkum.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
        ```

    - Bættu við eftirfarandi línum til að innihalda viðbótina fyrir vélbúnaðarstöðina í pakkanum sem hægt er að nota.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

3. Virkjaðu POS viðbótina með því að bæta við eftirfarandi línum í **extensions.json** skrá undir **RetailSDK\\ POS\\ Framlengingar** möppu.

    ``` json
    {
        "extensionPackages": [
            {
            "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

4. Ræstu MSBuild Command Prompt fyrir Visual Studio gagnsemi, og keyra **msbuild** undir Retail SDK möppunni til að búa til dreianlega pakka.
5. Notaðu pakkana í gegnum LCS eða handvirkt. Fyrir frekari upplýsingar, sjá [Búðu til pakka sem hægt er að nota](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
6. Ljúktu við öll nauðsynleg uppsetningarverk sem lýst er í [Uppsetning samþættingar við stýrieiningar](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units).

## <a name="design-of-the-extensions"></a>Hönnun viðbygginga

### <a name="crt-extension-design"></a>CRT framlengingarhönnun

Tilgangur framlengingarinnar sem er ríkisfjármálaskjalaveita er að búa til þjónustusértæk skjöl og sjá um svör frá stjórneiningunni.

The CRT framlenging er **Runtime.Extensions.DocumentProvider.CleanCashSample**.

Fyrir frekari upplýsingar um hönnun fjárhagslegrar samþættingarlausnar, sjá [Fjárhagsskráningarferli og sýnishorn af samþættingu ríkisfjármála fyrir ríkisfjármálatæki og þjónustu](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Beiðni um stjórnanda

Það er einn **DocumentProviderCleanCash** meðhöndlun beiðni fyrir skjalaveitanda. Þessi meðhöndlun er notuð til að búa til fjárhagsskjöl fyrir stýrieininguna.

Þessi stjórnandi er arfur frá **INAmedRequestHandler** viðmót. The **HandlerName** aðferð er ábyrg fyrir því að skila nafni stjórnanda. Nafn meðhöndlunar ætti að passa við heiti tengiskjalsveitu sem er tilgreint í höfuðstöðvum Commerce.

Tengið styður eftirfarandi beiðnir:

- **GetFiscalDocumentDocumentProviderRequest** – Þessi beiðni inniheldur upplýsingar um hvaða skjal ætti að búa til. Það skilar þjónustusértæku skjali sem ætti að vera skráð í stjórneininguna.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Þessi beiðni skilar lista yfir viðburði til að gerast áskrifandi að. Eins og er eru söluviðburðir og endurskoðunarviðburðir studdir.

#### <a name="configuration"></a>Skilgreining

The **DocumentProviderFiscalCleanCashSample** stillingarskrá er í **Stillingar** möppu framlengingarverkefnisins. Tilgangur þessarar skráar er að gera stillingar fyrir skjalaveituna kleift að stilla frá höfuðstöðvum Commerce. Skráarsniðið er í samræmi við kröfurnar fyrir fjárhagslega samþættingu stillingar. Eftirfarandi stillingum er bætt við:

- Vörpun VSK-kóða

### <a name="hardware-station-extension-design"></a>Hönnun vélbúnaðarstöðvar viðbyggingar

Tilgangur framlengingarinnar sem er fjárhagstengi er að hafa samskipti við stjórneininguna.

Viðbygging Vélbúnaðarstöðvar er **HardwareStation.Extension.CleanCashSample**. Það notar HTTP samskiptareglur til að leggja fram skjöl sem CRT framlenging myndar við stjórneininguna. Það sér einnig um svör sem berast frá stjórnstöðinni.

#### <a name="request-handler"></a>Beiðni um stjórnanda

The **CleanCashHandler** meðhöndlun beiðna er inngangsstaðurinn fyrir meðhöndlun beiðna til stjórnunareiningarinnar.

Umsjónarmaðurinn er arfur frá **INAmedRequestHandler** viðmót. The **HandlerName** aðferð er ábyrg fyrir því að skila nafni stjórnanda. Nafn meðhöndlunar ætti að passa við nafn fjárhagstengis sem er tilgreint í höfuðstöðvum Commerce.

Tengið styður eftirfarandi beiðnir:

- **SubmitDocumentFiscalDeviceRequest** – Þessi beiðni sendir skjöl til stjórnstöðvarinnar og skilar svari frá henni.
- **IsReadyFiscalDeviceRequest** – Þessi beiðni er notuð fyrir heilsufarsskoðun á stjórneiningunni.
- **Frumstilla FiscalDeviceRequest** – Þessi beiðni er notuð til að frumstilla stjórneininguna.

#### <a name="configuration"></a>Skilgreining

Stillingarskráin er í **Stillingar** möppu framlengingarverkefnisins. Tilgangur skrárinnar er að gera stillingar fyrir fjárhagslega tengið kleift að stilla frá höfuðstöðvum Commerce. Skráarsniðið er í samræmi við kröfurnar fyrir fjárhagslega samþættingu stillingar. Eftirfarandi stillingum er bætt við:

- **Tengingarstrengur** – Tengistillingar stýrieiningarinnar.
- **Hlé** – Tíminn, í millisekúndum, sem ökumaður bíður eftir svari frá stjórneiningunni.

## <a name="migrating-from-the-earlier-integration-sample"></a>Flutningur frá fyrra samþættingarúrtaki

Ef þú ert að nota fyrri [sýnishorn fyrir POS samþættingu við stjórneiningar fyrir Svíþjóð](retail-sdk-control-unit-sample.md), þú gætir þurft að flytja úr því yfir í núverandi samþættingarsýni. Til að taka breytinguna og fá tímanlega uppfærslur á eiginleikum fyrir Svíþjóð í framtíðinni gætirðu þurft að uppfæra, gera minniháttar kóða- og stillingarbreytingar í viðbótunum sem þú smíðaðir og endurbyggja lausnirnar þínar. Engar meiriháttar breytingar eru nauðsynlegar á framlengingarlögfræðinni sem þú bjóst til. Fyrra samþættingarsýnishornið og sérstillingarnar þínar munu halda áfram að virka ef engar breytingar eru gerðar frá þinni hlið. Þess vegna getur þú skipulagt, undirbúið og gert upptöku fyrir umhverfið þitt.

### <a name="migration-process"></a>Flutningaferli

Flutningur frá fyrra samþættingarúrtaki yfir í núverandi samþættingarúrtak stýrieiningar ætti að byggjast á hugmyndinni um hægfara uppfærslu. Með öðrum orðum, allar höfuðstöðvar Commerce og Commerce Scale Unit íhlutir ættu nú þegar að vera uppfærðir áður en þú byrjar að uppfæra POS og vélbúnaðarstöðina.

Til að koma í veg fyrir aðstæður þar sem atburður eða viðskipti eru undirrituð tvisvar (þ.e. hann er undirritaður af bæði fyrri framlengingunni og núverandi framlengingu), eða þar sem ekki er hægt að undirrita atburð eða viðskipti vegna þess að uppsetningu vantar, mælum við með að þú slekkur á öllum POS- og vélbúnaðarstöðvum sem nota fyrra sýnishornið og uppfærir þau síðan samtímis. Þessa samtímis uppfærslu er hægt að gera, til dæmis frá verslun fyrir verslun með því að uppfæra virknisnið verslunarinnar og vélbúnaðarsnið vélbúnaðarstöðvarinnar.

Flutningsferlið ætti að samanstanda af eftirfarandi skrefum.

1. Uppfærðu hluta höfuðstöðva viðskipta.
1. Uppfærðu Commerce Scale Unit íhlutina og virkjaðu framlengingar núverandi sýnishorns.
1. Gakktu úr skugga um að allar færslur án nettengingar séu samstilltar frá MPOS tækjum sem eru virkt án nettengingar.
1. Slökktu á öllum tækjum sem nota íhluti fyrra sýnishornsins.
1. Ljúktu við öll nauðsynleg uppsetningarverk sem lýst er í [Uppsetning samþættingar við stýrieiningar](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units).
1. Uppfærðu POS- og vélbúnaðarstöðina, slökktu á viðbótunum sem eru hluti af fyrra sýnishorninu og virkjaðu viðbætur núverandi sýnishorns.

    > [!NOTE]
    > Það fer eftir tegund umhverfisins, þú getur fundið frekari tæknilegar upplýsingar um flutningsferlið í annað hvort [Flutningur í þróunarumhverfi](#migration-in-a-development-environment) kafla eða [Flutningur í framleiðsluumhverfi](#migration-in-a-production-environment) kafla þessarar greinar.

### <a name="migration-in-a-development-environment"></a>Flutningur í þróunarumhverfi

#### <a name="update-crt"></a>Uppfæra CRT

1. Finndu **Runtime.Extensions.DocumentProvider.CleanCashSample** verkefnið og byggja það.
2. Í **Runtime.Extensions.DocumentProvider.CleanCashSample\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána í CRT viðbætur mappa:

    - **Eining viðskiptaskala:** Afritaðu skrána í **\\ bin\\ ext** möppu undir staðsetningu IIS Commerce Scale Unit.
    - **Staðbundið CRT á Modern POS:** Afritaðu skrána í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavinar.

4. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Eining viðskiptaskala:** Skráin er nefnd **CommerceRuntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningu IIS Commerce Scale Unit.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er í **bin\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavinar.

    > [!WARNING]
    > Gerðu **ekki** breyttu CommerceRuntime.config og CommerceRuntime.MPOSOffline.config skránum. Þessar skrár eru ekki ætlaðar fyrir neinar sérstillingar.

5. Finndu og fjarlægðu fyrr CRT eftirnafn úr stillingarskránni fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Ekki klára þetta skref fyrr en þú uppfærir öll POS tæki sem vinna með þetta CRT dæmi.

6. Skráðu núverandi sýnishorn CRT viðbætur í stillingarskrá eftirlengingar með því að bæta við eftirfarandi línum.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

#### <a name="update-hardware-station"></a>Uppfærðu vélbúnaðarstöð

1. Finndu **HardwareStation.Extension.CleanCashSample** verkefnið og byggja það.
2. Í **Extension.CleanCashSample\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.HardwareStation.CleanCashSample.dll** og **Interop.CleanCash\_ 1\_ 1.dll** samsetningarskrár.
3. Afritaðu samsetningarskrárnar í möppuna Vélbúnaðarstöðvarviðbætur:

    - **Sameiginleg vélbúnaðarstöð:** Afritaðu skrárnar í **bin** möppu undir staðsetningu IIS vélbúnaðarstöðvar.
    - **Sérstök vélbúnaðarstöð á Modern POS:** Afritaðu skrárnar á miðlarastað Modern POS viðskiptavinar.

4. Finndu **HardwareStation.Extension.config** eftirnafn stillingarskrá:

    - **Fjarstýrð vélbúnaðarstöð:** Skráin er undir staðsetningu IIS vélbúnaðarstöðvar.
    - **Staðbundin vélbúnaðarstöð á Modern POS:** Skráin er undir miðlarastaðnum Modern POS viðskiptavinar.

    > [!WARNING]
    > Gerðu **ekki** breyttu CommerceRuntime.config og CommerceRuntime.MPOSOffline.config skránum. Þessar skrár eru ekki ætlaðar fyrir neinar sérstillingar.

5. Finndu og fjarlægðu fyrri viðbótina fyrir vélbúnaðarstöðina úr stillingarskránni fyrir viðbótina.

    # <a name="retail-73-and-earlier"></a>[Smásala 7.3 og eldri](#tab/retail-7-3)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Smásala 7.3.1 og síðar](#tab/retail-7-3-1)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Smásala 10.0 og síðar](#tab/retail-10-0)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

6. Bættu eftirfarandi línu við **samsetningu** hluta af stillingarskránni fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

#### <a name="update-modern-pos"></a>Uppfærðu Modern POS

1. Opnaðu **CloudPOS.sln** lausn undir **RetailSdk\\ POS**.
2. Slökktu á fyrri POS viðbótinni með því að fjarlægja eftirfarandi línur úr **extensions.json** skrá.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Virkjaðu núverandi sýnishorn af POS viðbótinni með því að bæta við eftirfarandi línum í **extensions.json** skrá.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>Uppfærðu Cloud POS

1. Opnaðu **ModernPOS.sln** lausn undir **RetailSdk\\ POS**.
2. Slökktu á fyrri POS viðbótinni með því að fjarlægja eftirfarandi línur úr **extensions.json** skrá.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Virkjaðu núverandi sýnishorn af POS viðbótinni með því að bæta við eftirfarandi línum í **extensions.json** skrá.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

### <a name="migration-in-a-production-environment"></a>Flutningur í framleiðsluumhverfi

#### <a name="update-crt"></a>Uppfæra CRT

1. Fjarlægðu það fyrr CRT framlenging frá **CommerceRuntime.ext.config** og **CommerceRuntime.MPOSOffline.Ext.config** stillingarskrár undir **RetailSdk\\ Eignir** möppu.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Ekki klára þetta skref fyrr en þú uppfærir öll POS tæki sem vinna með þetta CRT dæmi.

2. Virkjaðu núverandi sýnishorn CRT framlengingar með því að gera eftirfarandi breytingar á **CommerceRuntime.ext.config** og **CommerceRuntime.MPOSOffline.Ext.config** stillingarskrár undir **RetailSdk\\ Eignir** möppu.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

3. Í **Customization.settings** stillingarskrá fyrir sérsniðna pakka undir **Byggingarverkfæri** möppu skaltu bæta við eftirfarandi línu til að innihalda núverandi sýnishorn CRT framlenging í dreifanlegum pakka.

    ``` xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
    ```

#### <a name="update-hardware-station"></a>Uppfærðu vélbúnaðarstöð

1. Fjarlægðu fyrri viðbyggingu vélbúnaðarstöðvarinnar með því að breyta **HardwareStation.Extension.config** stillingarskrá.

    # <a name="retail-73-and-earlier"></a>[Smásala 7.3 og eldri](#tab/retail-7-3)

    Fjarlægðu eftirfarandi hluta úr **HardwareStation.Shared.config** og **HardwareStation.Dedicated.config** stillingarskrár.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Smásala 7.3.1 og síðar](#tab/retail-7-3-1)

    Fjarlægðu eftirfarandi hluta úr **HardwareStation.Extension.config** stillingarskrá.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Smásala 10.0 og síðar](#tab/retail-10-0)

    Fjarlægðu eftirfarandi hluta úr **HardwareStation.Extension.config** stillingarskrá.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

2. Virkjaðu núverandi sýnishorn vélbúnaðarstöðvarviðbótar með því að bæta eftirfarandi línu við **samsetningu** kafla í **HardwareStation.Extension.config** stillingarskrá.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

3. Gerðu eftirfarandi breytingar á **Customization.settings** stillingarskrá fyrir sérsniðna pakka undir **Byggingarverkfæri** mappa:

    - Fjarlægðu eftirfarandi línu til að útiloka fyrri viðbyggingu Vélbúnaðarstöðvarinnar frá útfæranlegum pakka.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample.dll" />
        ```

    - Bættu við eftirfarandi línum til að innihalda núverandi sýnishorn af vélbúnaðarstöðvum í útbreiðslupökkum.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

#### <a name="update-modern-pos"></a>Uppfærðu Modern POS

1. Opnaðu **CloudPOS.sln** lausn kl **RetailSdk\\ POS**.
2. Slökktu á fyrri POS viðbótinni:

    - Í **tsconfig.json** skrá, bæta við **FiscalRegisterSample** möppu í útilokunarlistann.
    - Fjarlægðu eftirfarandi línur úr **extensions.json** skrá undir **RetailSDK\\ POS\\ Framlengingar** möppu.

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

3. Virkjaðu núverandi sýnishorn af POS viðbótinni með því að bæta við eftirfarandi línum í **extensions.json** skrá undir **RetailSDK\\ POS\\ Framlengingar** möppu.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>Uppfærðu Cloud POS

1. Opnaðu **ModernPOS.sln** lausn undir **RetailSdk\\ POS**.
2. Slökktu á fyrri POS viðbótinni:

    - Í **tsconfig.json** skrá, bæta við **FiscalRegisterSample** möppu í útilokunarlistann.
    - Fjarlægðu eftirfarandi línur úr **extensions.json** skrá undir **RetailSDK\\ POS\\ Framlengingar** möppu.

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

3. Virkjaðu núverandi sýnishorn af POS viðbótinni með því að bæta við eftirfarandi línum í **extensions.json** skrá undir **RetailSDK\\ POS\\ Framlengingar** möppu.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="create-deployable-packages"></a>Búa til virkjanlega pakka

Hlaupa **msbuild** fyrir allt Retail SDK til að búa til dreianlega pakka. Notaðu pakkana í gegnum LCS eða handvirkt. Fyrir frekari upplýsingar, sjá [Smásölu SDK umbúðir](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
