---
title: Leiðbeiningar um dreifingu fyrir samþættingarsýni stjórneiningar fyrir Svíþjóð (arfleifð)
description: Þessi grein veitir leiðbeiningar um innleiðingu samþættingarsýnis stýrieininga fyrir Svíþjóð frá Retail SDK
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 05a49de43282c449c7b99072d8ac3ac4a5f2a67f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870548"
---
# <a name="deployment-guidelines-for-the-control-unit-integration-sample-for-sweden-legacy"></a>Leiðbeiningar um dreifingu fyrir samþættingarsýni stjórneiningar fyrir Svíþjóð (arfleifð)

[!include [banner](../includes/banner.md)]

Þessi grein veitir leiðbeiningar um uppsetningu samþættingarsýnis stýrieininga fyrir Svíþjóð úr smásöluhugbúnaðarþróunarsettinu (SDK) á sýndarvél þróunaraðila (VM) í Microsoft Dynamics Lífsferilsþjónusta (LCS). Fyrir frekari upplýsingar um þetta sýnishorn af samþættingu ríkisfjármála, sjá [Samþættingarsýni stjórneiningar fyrir Svíþjóð](emea-swe-fi-sample.md). 

Úrtak ríkisfjármálasamþættingar fyrir Svíþjóð er hluti af Retail SDK. Fyrir upplýsingar um hvernig á að setja upp og nota SDK, sjá [Smásala hugbúnaðarþróunarsett (SDK) arkitektúr](../dev-itpro/retail-sdk/retail-sdk-overview.md). Þetta sýnishorn samanstendur af viðbótum fyrir Commerce runtime (CRT), Vélbúnaðarstöð og sölustaður (POS). Til að keyra þetta sýnishorn verður þú að breyta og byggja upp CRT, Vélbúnaðarstöð og POS verkefni. Við mælum með því að þú notir óbreytt Retail SDK til að gera þær breytingar sem lýst er í þessari grein. Við mælum líka með því að þú notir heimildastýringarkerfi eins og Azure DevOps þar sem engum skrám hefur verið breytt ennþá.

## <a name="development-environment"></a>Þróunarumhverfi

Fylgdu þessum skrefum til að setja upp þróunarumhverfi svo þú getir prófað og stækkað sýnishornið.

### <a name="enable-crt-extensions"></a>Virkja CRT framlengingar

The CRT framlengingaríhlutir eru innifalin í CRT sýnishorn. Til að ljúka eftirfarandi aðferðum skaltu opna **CommerceRuntimeSamples.sln** lausn undir **RetailSdk\\ SampleExtensions\\ CommerceRuntime**.

#### <a name="documentprovidercleancashsample-component"></a>DocumentProvider.CleanCashSample hluti

1. Finndu **Runtime.Extensions.DocumentProvider.CleanCashSample** verkefni, og byggja það.
2. Í **Runtime.Extensions.DocumentProvider.CleanCashSample\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána í CRT viðbætur mappa:

    - **Eining viðskiptaskala:** Afritaðu skrána í **\\ bin\\ ext** möppu undir Internet Information Services (IIS) Commerce Scale Unit staðsetningu.
    - **Staðbundið CRT á Modern POS:** Afritaðu skrána í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

4. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Eining viðskiptaskala:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningu IIS Commerce Scale Unit.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

5. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    ```

#### <a name="extension-configuration-file"></a>Stillingarskrá fyrir viðbætur

1. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Eining viðskiptaskala:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningu IIS Commerce Scale Unit.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

2. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

### <a name="enable-hardware-station-extensions"></a>Virkja viðbætur fyrir vélbúnaðarstöð

Viðbótarhlutir vélbúnaðarstöðvar eru innifaldir í sýnishornum fyrir vélbúnaðarstöð. Til að ljúka eftirfarandi aðferðum skaltu opna **HardwareStationSamples.sln** lausn undir **RetailSdk\\ SampleExtensions\\ Vélbúnaðarstöð**.

#### <a name="cleancash-component"></a>CleanCash hluti

1. Finndu **HardwareStation.Extension.CleanCashSample** verkefni, og byggja það.
2. Í **Framlenging.CleanCashSample\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.HardwareStation.CleanCashSample.dll** og **Interop.CleanCash\_ 1\_ 1.dll** samsetningarskrár.
3. Afritaðu samsetningarskrárnar í möppuna Vélbúnaðarstöðvarviðbætur:

    - **Sameiginleg vélbúnaðarstöð:** Afritaðu skrárnar í **bin** möppu undir staðsetningu IIS vélbúnaðarstöðvar.
    - **Sérstök vélbúnaðarstöð á Modern POS:** Afritaðu skrárnar á miðlarastað Modern POS viðskiptavinar.

4. Finna skilgreiningarskrá nafnaukans fyrir viðbætur Vélbúnaðarstöðvarinnar. Skráin heitir **HardwareStation.Extension.config**.

    - **Samnýtt vélbúnaðarstöð:** Skráin er undir staðsetningu IIS vélbúnaðarstöðvarinnar.
    - **Hollur vélbúnaður stöð á Modern POS:** Skráin er undir Modern POS viðskiptavinur miðlari staðsetningu.

5. Bætið eftirfarandi línu við **samsetningarhluta** skilgreiningarskrárinnar.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

### <a name="enable-modern-pos-extension-components"></a>Virkja nútíma íhluti posaviðauka

1. **Opnaðu ModernPOS.sln** lausnina undir **RetailSdk\\ POS** og gakktu úr skugga um að hægt sé að þýða hana án villna. Að auki skal ganga úr skugga um að hægt sé að keyra Modern POS úr Visual Studio með því að nota skipunina **Keyra**.

    > [!NOTE]
    > Ekki má aðlaga nútíma posa. Virkja verður stjórnun notendareikninga (UAC) og fjarlægja verður áður uppsett tilvik af Modern POS eftir þörfum.

2. Virkja nafnaukana sem þarf að hlaða inn með því að bæta við eftirfarandi línum í nafnaukaskránni **extensions.json**.

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
    > Frekari upplýsingar og fyrir sýni sem sýna hvernig á að taka með möppur frumkóða og gera kleift að hlaða inn viðbótum er að finna í leiðbeiningunum í readme.md skránni **í Pos.Extensions** verkefninu.

3. Endurbyggja lausnina.
4. Keyra skal Modern POS í kembiforritinu og prófa virknina.

### <a name="enable-cloud-pos-extension-components"></a>Virkja cloud POS viðbótaríhluti

1. **Opnaðu CloudPOS.sln** lausnina undir **RetailSdk\\ POS** og gakktu úr skugga um að hægt sé að þýða hana án villna.
2. Virkja nafnaukana sem þarf að hlaða inn með því að bæta við eftirfarandi línum í nafnaukaskránni **extensions.json**.

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
    > Frekari upplýsingar og fyrir sýni sem sýna hvernig á að taka með möppur frumkóða og gera kleift að hlaða inn viðbótum er að finna í leiðbeiningunum í readme.md skránni **í Pos.Extensions** verkefninu.

3. Endurbyggja lausnina.
4. Keyrið lausnina með skipuninni **Keyra** og fylgið skrefunum í smásölu SDK handbókinni.

## <a name="production-environment"></a>Framleiðsluumhverfi

Fyrra ferli gerir viðaukana sem eru íhlutir samþættingarsýnis stjórneiningarinnar mögulegar. Að auki verður að fylgja þessum skrefum til að búa til virkjanlega pakka sem innihalda viðskiptaíhluti og nota þá pakka í framleiðsluumhverfi.

1. Gera eftirfarandi breytingar á samskipanarskrám pakka í möppunni **RetailSdk\\ Assets**:

    - Í skilgreiningarskránum commerceruntime.ext.config og CommerceRuntime.MPOSOffline.Ext.config **skal bæta eftirfarandi línum við samsetningarhlutann** **.** **·**

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
        ```

    - Í skilgreiningarskránni HardwareStation.Extension.config **er eftirfarandi línu bætt við samsetningarhlutann** **.**

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
        ```

2. Gera eftirfarandi breytingar í **customization.settings sérsniðssamstillingarskrá customization.settings** pakkans **undir BuildTools** möppunni:

    - Bætið við eftirfarandi línu til að hafa viðbæturnar með CRT í virkjanlegum pökkum.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
        ```

    - Bætið við eftirfarandi línum til að hafa viðbót vélbúnaðarstöðvarinnar með í virkjupökkunum.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

3. Virkja nafnauka sölustaðar með því að bæta við eftirfarandi línum í **extensions.json-skránni** undir möppunni **RetailSDK\\ POS\\ Extensions**.

    ``` json
    {
        "extensionPackages": [
            {
            "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

4. Ræsa skipanakvaðningu MSBuild fyrir Visual Studio forrit og keyra **msbuild** undir möppunni Retail SDK til að búa til virkjanlega pakka.
5. Notaðu pakkana með LCS eða handvirkt. Sjá Create deployable packages [fyrir frekari upplýsingar](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
6. Ljúkið við öll nauðsynleg uppsetningarverk sem lýst er í [Uppsetning samþættingar við stjórneiningar](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units).

## <a name="design-of-the-extensions"></a>Hönnun viðbætur

### <a name="crt-extension-design"></a>CRT viðaukahönnun

Tilgangur viðbótarinnar sem er fjármálaskjalsveita er að búa til þjónustutengd skjöl og meðhöndla svör frá stjórneiningunni.

Viðbótin CRT er **Runtime.Extensions.DocumentProvider.CleanCashSample**.

Nánari upplýsingar um hönnun fjárhagssamþættingarlausnarinnar eru í [Fjárhagsskráningarferli og fjárhagssamþættingarsýni fyrir fjárhagstæki og þjónustu](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Biðja um rekil

Það er einn **DocumentProviderCleanCash** beiðnistjóri fyrir skjalaveituna. Þessi rekill er notaður til að búa til fjárhagsskjöl fyrir stjórneininguna.

Þessi rekill erfist frá viðmótinu **INamedRequestHandler**. HandlerName **aðferðin** ber ábyrgð á að skila nafni rekilsins. Heiti rekils ætti að samsvara heiti tengiskjalsveitunnar sem er tilgreint í höfuðstöðvum Commerce.

Tengið styður eftirfarandi beiðnir:

- **GetFiscalDocumentDocumentProviderRequest** – Þessi beiðni inniheldur upplýsingar um hvaða skjal á að mynda. Það skilar þjónustutengdu skjali sem ætti að skrá í stjórneininguna.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Þessi beiðni skilar lista yfir tilvik sem á að gerast áskrifandi að. Eins og er eru söluviðburðir og endurskoðunarviðburðir studdir.

#### <a name="configuration"></a>Skilgreining

Skilgreiningarskráin **DocumentProviderFiscalCleanCashSample** er í skilgreiningarmöppu **nafnaukaverksins**. Tilgangur þessarar skrár er að virkja stillingar fyrir skjalaveituna sem skilgreina á úr höfuðstöðvum Commerce. Skráarsniðið er í takt við þarfir fyrir skilgreiningu fjárhagssamþættingar. Eftirfarandi stillingum er bætt við:

- Vörpun VSK-kóða

### <a name="hardware-station-extension-design"></a>Viðaukahönnun vélbúnaðarstöðvar

Tilgangur nafnaukans sem er fjárhagstengi er að hafa samskipti við stjórneininguna.

Viðauki vélbúnaðarstöðvarinnar er **HardwareStation.Extension.CleanCashSample**. Það notar HTTP-samskiptareglurnar til að senda skjöl sem viðbótin CRT myndar til stjórneiningarinnar. Hún sér einnig um svörin sem berast frá stjórneiningunni.

#### <a name="request-handler"></a>Biðja um rekil

**CleanCashHandler** beiðnistjórinn er inngangsstaður fyrir meðhöndlun beiðna í stjórneininguna.

Rekillinn erfist frá viðmótinu **INamedRequestHandler**. HandlerName **aðferðin** ber ábyrgð á að skila nafni rekilsins. Heiti rekils ætti að samsvara heiti fjárhagstengisins sem er tilgreint í höfuðstöðvum Commerce.

Tengið styður eftirfarandi beiðnir:

- **SubmitDocumentFiscalDeviceRequest** – Þessi beiðni sendir skjöl til stjórnstöðvarinnar og skilar svari frá henni.
- **IsReadyFiscalDeviceRequest** – Þessi beiðni er notuð við heilsufarsskoðun á stjórneiningunni.
- **InitializeFiscalDeviceRequest** – Þessi beiðni er notuð til að frumstilla stjórneininguna.

#### <a name="configuration"></a>Skilgreining

Skilgreiningarskráin er í skilgreiningarmöppunni **í** nafnaukaverkinu. Tilgangur skrárinnar er að virkja stillingar fyrir fjárhagstengið sem skilgreina á úr höfuðstöðvum Commerce. Skráarsniðið er í takt við þarfir fyrir skilgreiningu fjárhagssamþættingar. Eftirfarandi stillingum er bætt við:

- **Tengingarstrengur** – Tengingarstillingar stjórneiningar.
- **Tímamörk** – Tíminn, í millisekúndum, sem rekillinn bíður eftir svari frá stjórneiningunni.

## <a name="migrating-from-the-earlier-integration-sample"></a>Flutningur úr fyrra samþættingarsýni

Ef þú ert að nota fyrra [sýni fyrir samþættingu posa við stjórneiningar fyrir Svíþjóð](retail-sdk-control-unit-sample.md) gætirðu þurft að flytja þig úr því í núverandi samþættingarsýni. Til að taka breytinguna upp og fá tímanlega uppfærslur fyrir aðgerðirnar fyrir Svíþjóð í framtíðinni gætirðu þurft að uppfæra, gera minniháttar kóða- og skilgreiningarbreytingar í viðbótunum sem þú byggðir og endurbyggja lausnirnar. Ekki er þörf á meiri háttar breytingum í viðbótagrunninum sem þú bjóst til. Fyrra samþættingarsýnið og sérsniðnar þínar munu halda áfram að virka ef engar breytingar eru gerðar frá hliðinni. Þess vegna getur þú skipulagt, undirbúið þig fyrir og gert upptöku fyrir umhverfið þitt.

### <a name="migration-process"></a>Flutningsferli

Flutningur úr fyrra samþættingarsýni yfir í gildandi samþættingarsýni stjórneininga ætti að byggjast á hugmyndinni um stigvaxandi uppfærslu. Með öðrum orðum, nú þegar ætti að uppfæra alla íhluti Commerce og Commerce Scale Unit áður en byrjað er að uppfæra íhluti posa- og vélbúnaðarstöðvarinnar.

Til að koma í veg fyrir aðstæður þar sem atburður eða færsla er undirrituð tvisvar (þ.e. hún er undirrituð bæði af fyrri viðbótinni og gildandi viðbót) eða þar sem ekki er hægt að undirrita atburð eða færslu vegna þeirrar stillingar sem vantar, mælum við með að þú slökkvir á öllum posa- og vélbúnaðarstöðvum sem nota fyrra sýnið, og uppfæra þær síðan samtímis. Þessa samtímis uppfærslu er hægt að gera, til dæmis í verslun í verslun með því að uppfæra virkniforstillingu verslunarinnar og vélbúnaðarforstillingu Vélbúnaðarstöðvarinnar.

Flutningsferlið ætti að samanstanda af eftirfarandi skrefum.

1. Uppfæra íhluti höfuðstöðva Commerce.
1. Uppfæra íhluti Commerce Scale Unit og virkja viðbætur gildandi sýnis.
1. Gakktu úr skugga um að allar færslur utan nets séu samstilltar frá MPOS-tækjum sem eru virkjuð utan nets.
1. Slökktu á öllum tækjum sem nota íhluti fyrra sýnisins.
1. Ljúkið við öll nauðsynleg uppsetningarverk sem lýst er í [Uppsetning samþættingar við stjórneiningar](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units).
1. Uppfæra íhluti posa- og vélbúnaðarstöðvarinnar, gera viðbæturnar sem eru hluti af fyrra sýni óvirkar og virkja viðbætur gildandi sýnis.

    > [!NOTE]
    > Það fer eftir tegund umhverfisins, þú getur fundið fleiri tæknilegar upplýsingar um flutningsferlið í annaðhvort [Migration í þróunarumhverfishlutanum](#migration-in-a-development-environment)[eða flutningi í framleiðsluumhverfishluta](#migration-in-a-production-environment) þessarar greinar.

### <a name="migration-in-a-development-environment"></a>Fólksflutningar í þróunarumhverfi

#### <a name="update-crt"></a>Uppfæra CRT

1. Finndu **Runtime.Extensions.DocumentProvider.CleanCashSample** verkefni, og byggja það.
2. Í **Runtime.Extensions.DocumentProvider.CleanCashSample\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána í CRT viðbætur mappa:

    - **Commerce Scale Unit:** Afritaðu skrána í hólfið **\\\\ ext** möppuna undir staðsetningu IIS Commerce Scale Unit.
    - **Staðbundið CRT á Modern POS:** Afritaðu skrána í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

4. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Commerce Scale Unit:** Skráin heitir **CommerceRuntime.ext.config** og er í möppunni hólfið **\\ ext** mappan undir staðsetningu IIS Commerce Scale Unit.
    - **Staðbundið CRT í Modern POS:** Skráin heitir **CommerceRuntime.MPOSOffline.Ext.config** og er í möppunni hólfið **\\ ext** undir staðbundnum CRT biðlaramiðlarastað.

    > [!WARNING]
    > Ekki **breyta** skránum CommerceRuntime.config og CommerceRuntime.MPOSOffline.config. Þessar skrár eru ekki ætlaðar til neinna sérstillinga.

5. Finna og fjarlægja fyrri CRT nafnauka úr skilgreiningarskrá nafnaukans.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Ekki ljúka þessu skrefi fyrr en þú uppfærir öll posatæki sem vinna með þetta CRT tilvik.

6. Skrá gildandi sýnishornsviðbætur CRT í skilgreiningarskrá nafnaukans með því að bæta við eftirfarandi línum.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

#### <a name="update-hardware-station"></a>Uppfæra vélbúnaðarstöð

1. Finndu **HardwareStation.Extension.CleanCashSample** verkefni, og byggja það.
2. Í **Framlenging.CleanCashSample\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.HardwareStation.CleanCashSample.dll** og **Interop.CleanCash\_ 1\_ 1.dll** samsetningarskrár.
3. Afritaðu samsetningarskrárnar í möppuna Vélbúnaðarstöðvarviðbætur:

    - **Sameiginleg vélbúnaðarstöð:** Afritaðu skrárnar í **bin** möppu undir staðsetningu IIS vélbúnaðarstöðvar.
    - **Sérstök vélbúnaðarstöð á Modern POS:** Afritaðu skrárnar á miðlarastað Modern POS viðskiptavinar.

4. **Finna skilgreiningarskrána HardwareStation.Extension.config** extension:

    - **Fjartengd vélbúnaðarstöð:** Skráin er undir staðsetningu IIS vélbúnaðarstöðvarinnar.
    - **Staðbundin vélbúnaðarstöð á Modern POS:** Skráin er undir Modern POS biðlaramiðlaranum.

    > [!WARNING]
    > Ekki **breyta** skránum CommerceRuntime.config og CommerceRuntime.MPOSOffline.config. Þessar skrár eru ekki ætlaðar til neinna sérstillinga.

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
    > Ekki ljúka þessu skrefi fyrr en þú uppfærir öll posatæki sem vinna með þetta CRT tilvik.

2. Virkjaðu núverandi sýnishorn CRT framlengingar með því að gera eftirfarandi breytingar á **CommerceRuntime.ext.config** og **CommerceRuntime.MPOSOffline.Ext.config** stillingarskrár undir **RetailSdk\\ Eignir** möppu.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

3. Í **Customization.settings** stillingarskrá fyrir sérsniðna pakka undir **Byggingarverkfæri** möppu skaltu bæta við eftirfarandi línu til að innihalda núverandi sýnishorn CRT framlenging í dreifanlegum pakka.

    ``` xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
    ```

#### <a name="update-hardware-station"></a>Uppfæra vélbúnaðarstöð

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

2. Virkjaðu núverandi sýnishorn af vélbúnaðarstöðvum með því að bæta eftirfarandi línu við **samsetningu** kafla í **HardwareStation.Extension.config** stillingarskrá.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

3. Gera eftirfarandi breytingar í **customization.settings sérsniðssamstillingarskrá customization.settings** pakkans **undir BuildTools** möppunni:

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

    - Í **tsconfig.json** skrá, bæta við **FiscalRegisterSample** möppu á útilokunarlistann.
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

    - Í **tsconfig.json** skrá, bæta við **FiscalRegisterSample** möppu á útilokunarlistann.
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

Hlaupa **msbuild** fyrir allt Retail SDK til að búa til dreianlega pakka. Notaðu pakkana með LCS eða handvirkt. Fyrir frekari upplýsingar, sjá [Smásölu SDK umbúðir](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
