---
title: Dreifingarleiðbeiningar fyrir samþættingarsýni prentara fyrir Pólland (gamalt)
description: Þetta efnisatriði veitir leiðbeiningar um útfærslu á samþættingarsýni prentara fyrir Pólland frá Microsoft Dynamics 365 Commerce Smásöluhugbúnaðarþróunarsett (SDK).
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: bff3a6ad74d50e7b706d4df92b17a4a3af36521b
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944816"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-poland-legacy"></a>Dreifingarleiðbeiningar fyrir samþættingarsýni prentara fyrir Pólland (gamalt)

[!include[banner](../includes/banner.md)]

Þetta efnisatriði veitir leiðbeiningar um útfærslu á samþættingarsýni prentara fyrir Pólland frá Microsoft Dynamics 365 Commerce Smásöluhugbúnaðarþróunarsett (SDK) á sýndarvél þróunaraðila (VM) í Microsoft Dynamics Lífsferilsþjónusta (LCS). Fyrir frekari upplýsingar um þetta sýnishorn af samþættingu ríkisfjármála, sjá [Samþættingarsýni prentara fyrir Pólland](emea-pol-fpi-sample.md). 

Fjármálasamþættingarúrtakið fyrir Pólland er hluti af Retail SDK. Fyrir upplýsingar um hvernig á að setja upp og nota SDK, sjá [Smásöluhugbúnaðarþróunarsett (SDK) arkitektúr](../dev-itpro/retail-sdk/retail-sdk-overview.md). Þetta sýnishorn samanstendur af viðbótum fyrir Commerce runtime (CRT) og Vélbúnaðarstöð. Til að keyra þetta sýnishorn verður þú að breyta og byggja upp CRT og Vélbúnaðarstöðvarverkefni. Við mælum með því að þú notir óbreytt Retail SDK til að gera þær breytingar sem lýst er í þessu efni. Við mælum líka með því að þú notir heimildastýringarkerfi eins og Azure DevOps þar sem engum skrám hefur verið breytt enn.

## <a name="development-environment"></a>Þróunarumhverfi

Fylgdu þessum skrefum til að setja upp þróunarumhverfi svo þú getir prófað og stækkað sýnishornið.

### <a name="commerce-runtime-extension-components"></a>Viðskiptatímaframlengingarhlutar

The CRT framlengingarhlutir eru innifalin í Retail SDK. Til að ljúka eftirfarandi aðferðum skaltu opna **CommerceRuntimeSamples.sln** lausn undir **RetailSdk\\ SampleExtensions\\ CommerceRuntime**.

1. Finndu **Runtime.Extensions.DocumentProvider.PosnetSample** verkefni, og byggja það.
2. Í **Extensions.DocumentProvider.PosnetSample\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána í CRT eftirnafn mappa:

    - **Eining viðskiptaskala:** Afritaðu skrána í **\\ bin\\ ext** möppu undir Internet Information Services (IIS) Commerce Scale Unit staðsetningu.
    - **Staðbundið CRT á Modern POS:** Afritaðu skrána í **\\ ext** möppu undir staðnum CRT staðsetningu miðlara viðskiptavina.

4. Finndu stillingarskrá fyrir viðbótina fyrir CRT:

    - **Eining viðskiptaskala:** Skráin er nefnd **commerceruntime.ext.config**, og það er í **bin\\ ext** möppu undir staðsetningu IIS Commerce Scale Unit.
    - **Staðbundið CRT á Modern POS:** Skráin er nefnd **CommerceRuntime.MPOSOffline.Ext.config**, og það er undir staðnum CRT staðsetningu miðlara viðskiptavina.

5. Skráðu þig CRT breyting á stillingarskrá fyrir viðbótina.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
    ```

6. Endurræstu viðskiptaþjónustuna:

    - **Eining viðskiptaskala:** Endurræstu viðskiptaþjónustusíðuna frá IIS Manager.
    - **Miðlari viðskiptavina:** Ljúktu við **dllhost.exe** ferli í Task Manager og endurræstu síðan Modern POS.

### <a name="hardware-station-extension-components"></a>Vélbúnaðarstöðvar viðbyggingarhlutir

Viðbótarhlutir vélbúnaðarstöðvar eru innifaldir í smásölu SDK. Til að ljúka eftirfarandi aðferðum skaltu opna **HardwareStationSamples.sln** lausn undir **RetailSdk\\ SampleExtensions\\ Vélbúnaðarstöð**.

1. Finndu **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample** verkefni, og byggja það.
2. Í **Extension.Posnet.ThermalFVFiscalPrinterSample\\ bin\\ Villuleit** möppu, finndu **Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll** samsetningarskrá.
3. Afritaðu samsetningarskrána á uppsetta vélbúnaðarstöð:

    - **Fjarstýrð vélbúnaðarstöð:** Afritaðu skrána í **bin** möppu undir staðsetningu IIS vélbúnaðarstöðvar. Afritaðu prentara reklasöfnin (**libposcmbth.dll**, **\_ serial.dll**, og **cmbth\_ pl.lng**).

4. Finndu stillingarskrána fyrir viðbætur vélbúnaðarstöðvarinnar. Skráin er nefnd **HardwareStation.Extension.config**:

    - **Fjarstýrð vélbúnaðarstöð:** Skráin er staðsett undir staðsetningu IIS vélbúnaðarstöðvarinnar.

5. Bættu eftirfarandi línu við **samsetningu** hluta stillingaskrárinnar.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
    ```

6. Endurræstu vélbúnaðarstöðvarþjónustuna:

    - **Fjarstýrð vélbúnaðarstöð:** Endurræstu vélbúnaðarstöðina frá IIS Manager.

## <a name="production-environment"></a>Framleiðsluumhverfi

Í fyrra ferli virkjaðirðu viðbæturnar sem eru hluti af samþættingarsýnishorni fjárhagsskráningarþjónustunnar. Að auki verður þú að fylgja þessum skrefum til að búa til dreifanlega pakka sem innihalda Commerce íhluti og nota þá pakka í framleiðsluumhverfi.

1. Gerðu eftirfarandi breytingar á stillingarskrám pakkans undir **RetailSdk\\ Eignir** mappa:

    - Í **commerceruntime.ext.config** og **CommerceRuntime.MPOSOffline.Ext.config** stillingarskrár skaltu bæta eftirfarandi línu við **samsetningu** kafla.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
        ```

    - Í **HardwareStation.Extension.config** stillingarskrá skaltu bæta eftirfarandi línu við **samsetningu** kafla.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
        ```

1. Gerðu eftirfarandi breytingar á **Customization.settings** stillingarskrá fyrir sérsniðna pakka undir **Byggingarverkfæri** mappa:

    - Bættu við eftirfarandi línu til að innihalda CRT framlengingu í dreifanlegum pökkum.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll"/>
        ```

    - Bættu við eftirfarandi línu til að innihalda viðbótina fyrir vélbúnaðarstöðina í pakkanum sem hægt er að nota.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll"/>
        ```

1. Ræstu MSBuild Command Prompt fyrir Visual Studio gagnsemi, og keyra **msbuild** undir Retail SDK möppunni til að búa til dreianlega pakka.
1. Notaðu pakkana í gegnum LCS eða handvirkt. Fyrir frekari upplýsingar, sjá [Búðu til dreifanlega pakka](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

## <a name="design-of-extensions"></a>Hönnun viðbygginga

Samþættingarsýni prentara fyrir Pólland er byggt á [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md). Fyrir frekari upplýsingar um hönnun fjárhagslegrar samþættingarlausnar, sjá [yfirlit yfir sýnishönnun í ríkisfjármálum](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices).

### <a name="commerce-runtime-extension-design"></a>Viðskiptatímaframlengingarhönnun

Tilgangur viðbyggingarinnar sem er fjárhagsskjalaveita er að búa til prentarasértæk skjöl og meðhöndla svör frá fjárhagsprentaranum.

The CRT framlenging er **Runtime.Extensions.DocumentProvider.PosnetSample**. Þessi viðbót býr til sett af prentara-sértækum skipunum á JavaScript Object Notation (JSON) sniði sem eru skilgreindar af POSNET forskrift 19-3678.

Fyrir frekari upplýsingar um hönnun fjárhagslegrar samþættingarlausnar, sjá [Fjárhagsskráningarferli og sýnishorn af samþættingu ríkisfjármála fyrir ríkisfjármálatæki](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices).

#### <a name="request-handler"></a>Beiðni um stjórnanda

The **DocumentProviderPosnetProtocol** meðhöndlun beiðni er inngangsstaður beiðninnar um að búa til skjöl frá fjárhagsprentaranum.

Umsjónarmaðurinn er arfur frá **INAmedRequestHandler** viðmót. The **HandlerName** aðferð ber ábyrgð á því að skila nafni meðhöndlunar. Nafn meðhöndlunar ætti að passa við heiti tengiskjalsveitu sem er tilgreint í höfuðstöðvum Commerce.

Tengið styður eftirfarandi beiðnir:

- **GetFiscalDocumentDocumentProviderRequest** – Þessi beiðni inniheldur upplýsingar um hvaða skjal ætti að búa til. Það skilar prentarasértæku skjali sem ætti að vera skráð í fjárhagsprentara.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Þessi beiðni skilar lista yfir viðburði til að gerast áskrifandi að. Eins og er eru eftirfarandi atburðir studdir: sala, prentun X skýrslu og prentun Z skýrslu.

#### <a name="configuration"></a>Skilgreining

Stillingarskráin er að finna í **Stillingar** möppu framlengingarverkefnisins. Tilgangur skrárinnar er að gera stillingar fyrir skjalaveituna kleift að stilla frá höfuðstöðvum Commerce. Skráarsniðið er í samræmi við kröfurnar fyrir fjárhagslega samþættingu stillingar. Eftirfarandi stillingum er bætt við:

- Vörpun VSK-hlutfalls
- Vörpun greiðslumáta
- Greiðslugerð innborgunar

### <a name="hardware-station-extension-design"></a>Hönnun vélbúnaðarstöðvar viðbyggingar

Tilgangur viðbótarinnar sem er fjárhagstengi er að hafa samskipti við fjárhagsprentarann.

Viðbygging Vélbúnaðarstöðvarinnar er **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample**. Þessi viðbót kallar á aðgerðir POSNET bílstjórans til að senda inn skipanir sem CRT framlenging myndar á fjárhagsprentarann. Það sér einnig um villur í tæki.

#### <a name="request-handler"></a>Beiðni um stjórnanda

The **FiscalPrinterHandler** meðhöndlun beiðna er inngangsstaðurinn til að meðhöndla beiðnina til ríkisútlæga tækisins.

Umsjónarmaðurinn er arfur frá **INAmedRequestHandler** viðmót. The **HandlerName** aðferð ber ábyrgð á því að skila nafni meðhöndlunar. Nafn meðhöndlunar ætti að passa við nafn fjárhagstengis sem tilgreint er í höfuðstöðvum Commerce.

Tengið styður eftirfarandi beiðnir:

- **Senda innDocumentFiscalDeviceRequest** – Þessi beiðni sendir skjöl til prentara og skilar svari frá fjármálaprentara.
- **IsReadyFiscalDeviceRequest** – Þessi beiðni er notuð fyrir heilsufarsskoðun tækisins.
- **Frumstilla FiscalDeviceRequest** – Þessi beiðni er notuð til að frumstilla prentara.

#### <a name="configuration"></a>Skilgreining

Stillingarskráin er staðsett í **Stillingar** möppu framlengingarverkefnisins. Tilgangur skráarinnar er að gera stillingar fyrir tengið kleift að stilla frá höfuðstöðvum Commerce. Skráarsniðið er í samræmi við kröfurnar fyrir fjárhagslega samþættingu stillingar. Eftirfarandi stillingum er bætt við:

- **Tengistrengur** – Strengur sem lýsir upplýsingum um tenginguna við tækið á sniði sem styður ökumanninn. Fyrir frekari upplýsingar, sjá POSNET ökumannsskjölin.
- **Samstilling dagsetningar og tíma** – Gildi sem tilgreinir hvort samstilla þarf dagsetningu og tíma prentarans við tengda vélbúnaðarstöðina.
- **Tímamörk tækisins** – Tíminn, í millisekúndum, sem ökumaðurinn bíður eftir svari frá tækinu. Fyrir frekari upplýsingar, sjá POSNET ökumannsskjölin.