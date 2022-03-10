---
title: Dreifingarleiðbeiningar fyrir samþættingarsýni prentara fyrir Ítalíu (arfleifð)
description: Þetta efni veitir leiðbeiningar um útfærslu á samþættingarsýni prentara fyrir Ítalíu frá Microsoft Dynamics 365 Commerce Smásöluhugbúnaðarþróunarsett (SDK).
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: c820c320410c43cafaae43c59cad04efdee24ab2
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388445"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-italy-legacy"></a>Dreifingarleiðbeiningar fyrir samþættingarsýni prentara fyrir Ítalíu (arfleifð)

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Þetta efni veitir leiðbeiningar um útfærslu á samþættingarsýni prentara fyrir Ítalíu frá Microsoft Dynamics 365 Commerce Smásöluhugbúnaðarþróunarsett (SDK) á sýndarvél þróunaraðila (VM) í Microsoft Dynamics Lífsferilsþjónusta (LCS). Fyrir frekari upplýsingar um þetta sýnishorn af samþættingu ríkisfjármála, sjá [Samþættingarsýni prentara fyrir Ítalíu](emea-ita-fpi-sample.md). 

Fjármálasamþættingarúrtakið fyrir Ítalíu er hluti af Retail SDK. Fyrir upplýsingar um hvernig á að setja upp og nota SDK, sjá [Smásala hugbúnaðarþróunarsett (SDK) arkitektúr](../dev-itpro/retail-sdk/retail-sdk-overview.md). Þetta sýnishorn samanstendur af viðbótum fyrir Commerce runtime (CRT) og Vélbúnaðarstöð. Til að keyra þetta sýnishorn verður þú að breyta og byggja upp CRT og Vélbúnaðarstöðvarverkefni. Við mælum með því að þú notir óbreytt Retail SDK til að gera þær breytingar sem lýst er í þessu efni. Við mælum líka með því að þú notir heimildastýringarkerfi eins og Azure DevOps þar sem engum skrám hefur verið breytt enn.

## <a name="development-environment"></a>Þróunarumhverfi

Fylgdu þessum skrefum til að setja upp þróunarumhverfi svo þú getir prófað og stækkað sýnishornið.

### <a name="commerce-runtime-extension-components"></a>Viðskiptatímaframlengingarhlutar

The CRT framlengingarhlutir eru innifalin í Retail SDK. Til að ljúka eftirfarandi aðferðum skaltu opna **CommerceRuntimeSamples.sln** lausn undir **RetailSdk\\ SampleExtensions\\ CommerceRuntime**.

1. Finndu **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample** verkefnið og byggja það.
2. Í **Extensions.DocumentProvider.EpsonFP90IIISample\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána í CRT viðbætur mappa:

    - **Eining viðskiptaskala:** Afritaðu skrána í **\\ bin\\ ext** möppu undir Internet Information Services (IIS) Commerce Scale Unit staðsetningu.
    - **Staðbundið CRT á Modern POS:** Afritaðu skrána í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

4. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Eining viðskiptaskala:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningu IIS Commerce Scale Unit.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

5. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
    ```

6. Endurræstu Commerce Scale Unit:

    - **Eining viðskiptaskala:** Endurræstu Commerce Scale Unit síðuna frá IIS Manager.
    - **Miðlari viðskiptavina:** Ljúktu við **dllhost.exe** ferli í Task Manager og endurræstu síðan Modern POS.

### <a name="hardware-station-extension-components"></a>Vélbúnaðarstöðvar viðbyggingarhlutir

Viðbótarhlutir vélbúnaðarstöðvar eru innifaldir í smásölu SDK. Til að ljúka eftirfarandi aðferðum skaltu opna **HardwareStationSamples.sln** lausn undir **RetailSdk\\ SampleExtensions\\ Vélbúnaðarstöð**.

1. Finndu **HardwareStation.Extensions.EpsonFP90IIIFiscalDeviceSample** verkefnið og byggja það.
2. Í **Viðbætur.EpsonFP90IIIFiscalDeviceSample\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána á uppsetta vélbúnaðarstöð:

    - **Fjarstýrð vélbúnaðarstöð:** Afritaðu skrána í **bin** möppu undir staðsetningu IIS vélbúnaðarstöðvar.
    - **Staðbundin vélbúnaðarstöð:** Afritaðu skrána á miðlarastað Modern POS viðskiptavinar.

4. Finndu stillingarskrána fyrir viðbætur vélbúnaðarstöðvarinnar. Skráin er nefnd **HardwareStation.Extension.config**:

    - **Fjarstýrð vélbúnaðarstöð:** Skráin er staðsett undir staðsetningu IIS vélbúnaðarstöðvarinnar.
    - **Staðbundin vélbúnaðarstöð:** Skráin er staðsett undir miðlarastað Modern POS viðskiptavinar.

5. Bættu eftirfarandi hluta við **samsetningu** hluta stillingaskrárinnar.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
    ```

6. Endurræstu vélbúnaðarstöðvarþjónustuna:

    - **Fjarstýrð vélbúnaðarstöð:** Endurræstu vélbúnaðarstöðina frá IIS Manager.
    - **Staðbundin vélbúnaðarstöð:** Ljúktu við **dllhost.exe** ferli í Task Manager og endurræstu síðan Modern POS.

## <a name="production-environment"></a>Framleiðsluumhverfi

Til að búa til dreifanlega pakka sem innihalda Commerce íhluti og nota þá pakka í framleiðsluumhverfi skaltu fylgja þessum skrefum.

1. Ljúktu við skrefin sem lýst er í [Þróunarumhverfi](#development-environment) kafla fyrr í þessu efni.
2. Gerðu eftirfarandi breytingar á stillingarskrám pakkans undir **RetailSdk\\ Eignir** mappa:

    1. Í **commerceruntime.ext.config** og **CommerceRuntime.MPOSOffline.Ext.config** stillingarskrár skaltu bæta eftirfarandi línu við **samsetningu** kafla.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
        ```

    1. Í **HardwareStation.Extension.config** stillingarskrá skaltu bæta eftirfarandi línu við **samsetningu** kafla.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
        ```

3. Gerðu eftirfarandi breytingar á **Customization.settings** stillingarskrá fyrir sérsniðna pakka undir **Byggingarverkfæri** mappa:

    1. Bættu við eftirfarandi línu til að innihalda CRT framlengingu í dreifanlegum pökkum.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll"/>
        ```

    1. Bættu við eftirfarandi línu til að innihalda viðbótina fyrir vélbúnaðarstöðina í pakkanum sem hægt er að nota.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll"/>
        ```

4. Gerðu eftirfarandi breytingar á **Sdk.ModernPos.Shared.csproj** skrá undir **Pakkar\_ SharedPackagingProjectComponents** möppu til að innihalda auðlindaskrárnar fyrir Ítalíu í dreifanlegum pakka:

    1. Bæta við **Atriðahópur** kafla sem inniheldur hnúta sem vísa á auðlindaskrárnar fyrir þær þýðingar sem óskað er eftir. Gakktu úr skugga um að þú tilgreinir rétt nafnrými og sýnishorn. Eftirfarandi dæmi bætir við auðlindahnútum fyrir **það** og **það-CH** staðir.

        ```xml
        <ItemGroup>
            <ResourcesIt Include="$(SdkReferencesPath)\it\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
            <ResourcesItCh Include="$(SdkReferencesPath)\it-CH\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
        </ItemGroup>
        ```

    1. Í **Target Name="CopyPackageFiles"** kafla, bætið við einni línu fyrir hvert svæði, eins og sýnt er í eftirfarandi dæmi.

        ```xml
        <Copy SourceFiles="@(ResourcesIt)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\it" SkipUnchangedFiles="true" />
        <Copy SourceFiles="@(ResourcesItCh)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\it-CH" SkipUnchangedFiles="true" />
        ```

5. Gerðu eftirfarandi breytingar á **Sdk.RetailServerSetup.proj** skrá undir **Pakkar\_ SharedPackagingProjectComponents** möppu til að innihalda auðlindaskrárnar fyrir Ítalíu í dreifanlegum pakka:

    1. Bæta við **Atriðahópur** kafla sem inniheldur hnúta sem vísa á auðlindaskrárnar fyrir þær þýðingar sem óskað er eftir. Gakktu úr skugga um að þú tilgreinir rétt nafnrými og sýnishorn. Eftirfarandi dæmi bætir við auðlindahnútum fyrir **það** og **það-CH** staðir.

        ```xml
        <ItemGroup>
            <ResourcesIt Include="$(SdkReferencesPath)\it\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
            <ResourcesItCh Include="$(SdkReferencesPath)\it-CH\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
        </ItemGroup>
        ```

    1. Í **Target Name="CopyPackageFiles"** kafla, bætið við einni línu fyrir hvert svæði, eins og sýnt er í eftirfarandi dæmi.

        ``` xml
        <Copy SourceFiles="@(ResourcesIt)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\it" SkipUnchangedFiles="true" />
        <Copy SourceFiles="@(ResourcesItCh)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\it-CH" SkipUnchangedFiles="true" />
        ```

6. Ræstu MSBuild Command Prompt fyrir Visual Studio gagnsemi, og keyra síðan **msbuild** undir Retail SDK möppunni til að búa til dreianlega pakka.
7. Notaðu pakkana í gegnum LCS eða handvirkt. Fyrir frekari upplýsingar, sjá [Búðu til dreifanlega pakka](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

## <a name="design-of-extensions"></a>Hönnun viðbygginga

### <a name="commerce-runtime-extension-design"></a>Viðskiptatímaframlengingarhönnun

Tilgangur viðbyggingarinnar sem er fjárhagsskjalaveita er að búa til prentarasértæk skjöl og meðhöndla svör frá fjárhagsprentaranum.

The CRT framlenging er **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample**.

Fyrir frekari upplýsingar um hönnun fjárhagslegrar samþættingarlausnar, sjá [Fjárhagsskráningarferli og sýnishorn af samþættingu ríkisfjármála fyrir ríkisfjármálatæki og þjónustu](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Beiðni um stjórnanda

The **DocumentProvider EpsonFP90III** meðhöndlun beiðni er inngangsstaður beiðninnar um að búa til skjöl frá fjárhagsprentaranum.

Umsjónarmaðurinn er arfur frá **INAmedRequestHandler** viðmót. The **HandlerName** aðferð ber ábyrgð á því að skila nafni meðhöndlunar. Nafn meðhöndlunar ætti að passa við heiti tengiskjalsveitu sem er tilgreint í höfuðstöðvum Commerce.

Tengið styður eftirfarandi beiðnir:

- **GetFiscalDocumentDocumentProviderRequest** – Þessi beiðni inniheldur upplýsingar um hvaða skjal ætti að búa til. Það skilar prentarasértæku skjali sem ætti að vera skráð í fjárhagsprentara.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Þessi beiðni skilar lista yfir viðburði til að gerast áskrifandi að. Eins og er eru eftirfarandi atburðir studdir: sala, prentun X skýrslu og prentun Z skýrslu.

#### <a name="configuration"></a>Skilgreining

Stillingarskráin er staðsett í **Stillingar** möppu framlengingarverkefnisins. Tilgangur skrárinnar er að gera stillingar fyrir skjalaveituna kleift að stilla frá höfuðstöðvum Commerce. Skráarsniðið er í samræmi við kröfurnar fyrir fjárhagslega samþættingu stillingar. Eftirfarandi stillingum er bætt við:

- Vörpun VSK-kóða
- Vörpun VSK-hlutfalls
- Vörpun greiðslumáta
- Tegund strikamerkis fyrir númer kvittunar
- Greiðslugerð innborgunar

### <a name="hardware-station-extension-design"></a>Hönnun vélbúnaðarstöðvar viðbyggingar

Tilgangur viðbótarinnar sem er fjárhagstengi er að hafa samskipti við fjárhagsprentarann.

Viðbygging Vélbúnaðarstöðvarinnar er **HardwareStation.Extension.EpsonFP90IIIFiscalDeviceSample**. Þessi viðbót notar HTTP samskiptareglur til að leggja fram skjöl sem CRT framlenging myndar á fjárhagsprentarann. Það sér einnig um svör sem berast frá fjármálaprentara.

#### <a name="request-handler"></a>Beiðni um stjórnanda

The **EpsonFP90III Dæmi** meðhöndlun beiðna er inngangsstaðurinn fyrir meðhöndlun beiðna til ríkisútlæga tækisins.

Umsjónarmaðurinn er arfur frá **INAmedRequestHandler** viðmót. The **HandlerName** aðferð ber ábyrgð á því að skila nafni meðhöndlunar. Nafn meðhöndlunar ætti að passa við nafn fjárhagstengis sem tilgreint er í höfuðstöðvum Commerce.

Tengið styður eftirfarandi beiðnir:

- **Senda innDocumentFiscalDeviceRequest** – Þessi beiðni sendir skjöl til prentara og skilar svari frá fjármálaprentara.
- **IsReadyFiscalDeviceRequest** – Þessi beiðni er notuð fyrir heilsufarsskoðun tækisins.
- **Frumstilla FiscalDeviceRequest** – Þessi beiðni er notuð til að frumstilla prentara.

#### <a name="configuration"></a>Skilgreining

Stillingarskráin er staðsett í **Stillingar** möppu framlengingarverkefnisins. Tilgangur skráarinnar er að gera stillingar fyrir tengið kleift að stilla frá höfuðstöðvum Commerce. Skráarsniðið er í samræmi við kröfurnar fyrir fjárhagslega samþættingu stillingar. Eftirfarandi stillingum er bætt við:

- **Heimilisfang endapunkts** – Vefslóð prentarans.
- **Samstilling dagsetningar og tíma** – Gildi sem tilgreinir hvort samstilla þarf dagsetningu og tíma prentarans við tengda vélbúnaðarstöðina.
