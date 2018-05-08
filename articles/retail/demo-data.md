---
title: "Útlit sýnigagnaskjás í MPOS/CPOS"
description: "Þetta efnisatriði veitir upplýsingar um útlit afgreiðsluskjás sem er innifalið í sýnigagnasafninu fyrir sölustað (POS) upplifunina í Microsoft Dynamics 365 for Retail."
author: zlinster
manager: AnnBe
ms.date: 10/05/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: zlinster
ms.search.validFrom: 2017-10-05
ms.dyn365.ops.version: Retail April 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 797058bdbbdb63a08eb35034ffe3c913307f38df
ms.openlocfilehash: e812bb13c903e72e31e62effd0c70f9b9d62de55
ms.contentlocale: is-is
ms.lasthandoff: 03/05/2018

---

# <a name="demo-data-screen-layouts-in-mposcpos"></a>Útlit sýnigagnaskjás í MPOS/CPOS

[!include [banner](includes/banner.md)]

Þetta efnisatriði veitir upplýsingar um útlit afgreiðsluskjás sem er innifalið í sýnigagnasafninu fyrir sölustað (POS) upplifunina í Microsoft Dynamics 365 for Retail.

## <a name="overview"></a>Yfirlit

Sýnishorn af útliti skjás sem fylgja með sýnigögnum Retail bjóða upp á efni sem er fínstillt fyrir ýmsa smásöluhluta, hlutverk verslunarstarfsmanns og tæki. Ein gerð útlits getur innihaldið nokkrar útlitsstærðir og samsetningar hnappahnita til að tryggja dekkun þar sem verslunarstarfsmenn fara á milli búnaðar og stöðva. Í þessu efnisatriði er lögð áhersla á muninn á þessum útlitsgerðum, aðgerðunum sem þær bjóða upp á og heildarupplifunin sem þær skila.

![Útlit sýnigagna á milli tækja](../retail/media/demo-screen-layouts-fig-1-1.png)

## <a name="anatomy-of-a-screen-layout-id"></a>Grunnskipulag kennis skjáútlits

Til að finna útlitsgerðir skjás í Retail skal fara í **Smásala**  > **Uppsetningu rásar** > **Uppsetning POS** > **POS** > **Skjáútlit**.

![Síða skjáútlits í Retail](../retail/media/demo-screen-layouts-fig-2-1.png)

Kenni skjáútlits getur haft allt að 10 stafi. Kennið er strengur sem samanstendur af þremur upplýsingahlutum, í þessari röð:

1. Fyrirt.  
2. Útlitsgerð
3. Einstaklingur

### <a name="company"></a>Fyrirt.  

| Stafur | Fyrirt.           |
|--------|-----------------|
| A      | Adventure Works |
| F      | Fabrikam        |
| F      | Contoso         |

### <a name="layout-version"></a>Útlitsgerð

| Útgáfunúmer | lýsing                                                                                |
|----------------|--------------------------------------------------------------------------------------------|
| 3              | Grunnútgáfan sem styður margar skjástærðir fyrir mismunandi tæki og myndhlutföll |
| 3.1            | Grunngerðin sem hefur viðbótarstuðning fyrir **Vörur sem mælt er með** gluggann.        |

### <a name="persona"></a>Einstaklingur

| Skammstöfun | Einstaklingur       | Innihald |
|--------------|---------------|----------|
| CSH          | Gjaldkeri       | Gjaldkeraútlit felur í sér öll viðskiptatengd starfsemi, svo sem viðskiptavina pantanir, skil, afslætti, ógildingu og gjafakort. Þessar útlitsgerðir innihalda einnig dagleg verkefni fyrir birgðastjórnun, svo sem verðathuganir, uppflettingu í birgðum og birgðatalningar. Einnig er boðið upp á grunnstjórnun vakta varðandi byrjunarupphæðir, frestun vakta og tímaklukku. |
| MGR          | Verslunarstjóri | Útlit fyrir verslunarstjóra innihalda öll viðskiptatengda starfsemi sem er að finna í gjaldkeraútlitinu, en einnig fela í sér skattahnekkingar. Þessar útlitsgerðir innihalda einnig dagleg verkefni sem tengjast birgðastjórnun, svo sem verðathuganir, uppfletting í birgðum og birgðatalningu. Í boði er vaktastjórnun til að hefja, fresta og ljúka vöktum. Að auki innihalda útlitsgerðirnar skúffuvalmöguleika fyrir færslur, brottnám, talningu skiptimyntar og peningaflutninga í öryggishólf og banka. Að lokum veita þessar útlitsgerðir aðgang árangursskýrslum og gera mögulegt að prenta út X og Z skýrslur. |
| STK          | Afgreiðslustarfsmaður birgða   | Útlitsgerðir fyrir Afgreiðslustarfsmaður birgða eru fínstilltar fyrir birgðastjórnun. Þær fela í sér aðgang að daglegum verkefnum verðathugunar, uppflettingu í birgðum, tiltekt og móttöku, birgðatalningu og sundurhlutun setts. Þessar útlitsgerðir veita einnig grunnaðgerðir fyrir vaktir varðandi tímaklukku og frestun vakta. Þrátt fyrir að þessar útlitsgerðir séu aðallega ætlaðar fyrir aðgerðir í bakvinnslu, hafa afgreiðslustarfsmenn birgða aðgang að sömu aðgerðum og gjaldkerar á færsluskjáum. |

### <a name="example-layout"></a>Dæmi útlit

Hér er dæmi um kenni skjáútlits fyrir Fabrikam fyrirtækið, útlitsútgáfu 3, og Verslunarstjóri einstaklingur:

F3MGR

Eftirfarandi skýringarmynd sýnir dæmi um Velkomin(n) skjáinn sem birtist Fabrikam verslunarstjóranum.

![Velkomin(n) skjár fyrir Fabrikam verslunarstjórann](../retail/media/demo-screen-layouts-fig-2-2.png)

## <a name="layout-sizes"></a>Útlitsstærðir

### <a name="full-vs-compact-layouts"></a>Fullt útlit á móti þjöppuðu útliti

Útlit skjás getur einnig innihaldið skilgreiningar fyrir bæði heilt tæki og þjappað tæki. Þar af leiðandi getur notanda verið úthlutað á eina tegund skjáútlits sem mun virka í mismunandi stærðar- og skjámyndaþáttum innan verslunarinnar.

- **Modern POS - Fullt** – Fullt útlit hentar yfirleitt best fyrir stærri skjái eins og tölvuskjái eða spjaldtölvur. Notendur geta valið viðmótseiningar sem útlitið inniheldur, tilgreint stærð og staðsetningu þessara eininga og stillt nákvæma eiginleika þeirra. Full útlit styðja bæði þversniðis- og langsniðsskilgreiningar.
- **Modern POS - Þjappað** – Þjappað útlit hentar yfirleitt best fyrir síma eða litlar spjaldtölvur. Hönnunarmöguleikar takmarkast við smækkuð tæki. Notendur geta skilgreint dálka og reiti fyrir móttöku- og samtölusvæði.

### <a name="screen-resolutions-that-are-provided"></a>Skjáupplausnir sem boðið er upp á

Eftirfarandi tafla sýnir þær útlitsstærðir sem eru í boði fyrir hefðbundnar skjáupplausnir.

| Útlitsgerð | Upplausn | Myndhlutfall | Markskjár          |
|-------------|------------|--------------|-------------------------|
| Þjappa\*   | 480 × 853  | 16:9         | Símar                  |
| Fullt        | 1024 × 768 | 4:3          | Spjaldtölvur                 |
| Fullt\*      | 1280 × 720 | 16:9         | Spjaldtölvur                 |
| Fullt        | 1366 × 768 | 16:9         | Spjaldtölvur, stærri skjáir |
| Fullt        | 1440 × 960 | 3:2          | Spjaldtölvur, stærri skjáir |

\* Þessir viðbótar útlitsstærðir eru aðeins tiltækar í Adventure Works og Fabrikam útliti.


>[!TIP]
> POS velur sjálfkrafa útlitsstærðir, byggt á nærtækustu stærð sem er tiltæk fyrir skjáupplausn núverandi skjámyndar forrits. Til að finna skjákenni útlits og upplausn útlits sem eru í notkun núna, skal opna Retail Modern POS (MPOS) eða Retail Cloud POS (CPOS) **Stillingar** síðuna og leita í **Lotuupplýsingar** hlutanum. Þú getur einnig séð raunupplausn glugga fyrir forrit eða vafraramma sem verið er að nota núna. Eftir að þú hefur fengið þessar upplýsingar er hægt að finna uppsprettu útlitsefnis í Retail með því að fara á **Uppsetning rásar** > **Uppsetning POS** > **POS** > **Skjáútlit**.


![Útlit skjáa og útlitsupplausnir/stærðir í Retail og POS](../retail/media/demo-screen-layouts-fig-3-1.png)

## <a name="companies-and-brands"></a>Fyrirtæki og vörumerki

Sérhver ímyndað fyrirtæki er beint að mismunandi smásöluhluta og inniheldur vörulista sem eru stillt fyrir markað fyrirtækisins. Hvert fyrirtæki hefur einstakt vörumerkjaútlit sem fylgir vörum þess. Vörumerkjaþættir innihalda áherslulit, dökkt eða létt þema og meðfylgjandi myndir sem veita raunhæfa upplifun.

### <a name="company-segment-and-visual-characteristics"></a>Fyrirtækjahluti og sjónræn einkenni

| Fyrirt.           | Staður | Hluti        | Áhersla | Þema |
|-----------------|----------|----------------|--------|-------|
| Adventure Works | Seattle  | Íþróttavörur | Blátt   | Dökkt  |
| Fabrikam        | Houston  | Tíska        | Grænt  | Ljóst |
| Contoso         | Boston   | Raftæki    | Rautt    | Dökkt  |


>[!NOTE]
> Adventure Works og Fabrikam eru tvö flaggskip vörumerki. Contoso er í boði, en ekki hefur verið gert ráð fyrir öllum útlitsgerðum.


Eftirfarandi myndir sýna dæmi um velkomin(n) síðu og viðskiptasíðu fyrir sýnifyrirtækin þrjú.

### <a name="adventure-works"></a>Adventure Works

![Sýnigögn velkomin(n) síðu fyrir Adventure Works](../retail/media/demo-screen-layouts-fig-4-1a.png)

![Sýnigögn viðskiptasíðu fyrir Adventure Works](../retail/media/demo-screen-layouts-fig-4-1b.png)

### <a name="fabrikam"></a>Fabrikam

![Sýnigögn velkomin(n) síðu fyrir Fabrikam](../retail/media/demo-screen-layouts-fig-4-2a.png)

![Sýnigögn viðskiptasíðu fyrir Fabrikam](../retail/media/demo-screen-layouts-fig-4-2b.png)

### <a name="contoso"></a>Contoso

![Sýnigögn útlits fyrir Contoso](../retail/media/demo-screen-layouts-fig-4-3.png)

## <a name="user-sign-in-matrix"></a>Notandaskráning í fylki

Náð hefur verið í notendur fyrir mismunandi skjáútlit. Með því að nota eftirfarandi töflu, ættir þú að fá aðgang að öllum skjáunum. Skráðu þig inn með því að nota viðeigandi stjórnandakenni.

| Fyrirt.           | Útlitskenni afgreiðsluskjás | Einstaklingur          | Stjórnandakenni           |
|-----------------|------------------|---------------   |------------------------|
| Adventure Works | A3MGR            | Verslunarstjóri    | 000154, 000137, 000073 |
| Adventure Works | A3CSH            | Gjaldkeri          | 000150, 000175, 000165 |
| Adventure Works | A3STK            | Afgreiðslustarfsmaður birgða      | 000155, 000181, 000152 |
| Fabrikam        | F3MGR            | Verslunarstjóri    | 000160, 000168, 000163 |
| Fabrikam        | F3CSH            | Gjaldkeri          | 000161, 000113, 000114 |
| Fabrikam        | F3STK            | Afgreiðslustarfsmaður birgða      | 000164, 000112, 000123 |
| Contoso         | C3MGR            | Verslunarstjóri    | 000100, 000111         |
| Contoso         | C3CSH            | Gjaldkeri          | 000110, 000120         |
| Contoso         | Ekki tiltækt   | Afgreiðslustarfsmaður birgða      | Ekki tiltækt         |


>[!TIP]
> Til að ná sem bestum árangri skaltu virkja afgreiðslukassa á viðkomandi verslunarsvæði og setja fyrirtækið í félagið einstaklingsins sem þú ætlar að nota þegar þú skráir þig inn. Þannig hjálpar þú að tryggja að sjónrænt útlit og vörumerkjamyndir samræmist upplifuninni. Til dæmis, ef þú hefur áhuga á að sjá Fabrikam útlit fyrir gjaldkeri, þá ættir þú að virkja afgreiðslukassa í Houston versluninni.


<!-- Hiding until the content page is available on CustomerSource -->

<!-- ## Reference icons and images -->

<!-- The screen layouts, button grids, and visual profiles were created using images and icons that can be found in **Retail > Channel setup > POS setup > POS > Images**. -->

<!-- ![Images in Dynamics 365 for Retail](../retail/media/demo-screen-layouts-fig-5-1.png) -->

<!-- Use the [POS Icon and Image Mapping](../retail/media/POS_Icon_and_Image_Mapping.xlsx) reference spreadsheet to locate operation icons, reference photos, swap logos, or provide new images of your own that can be referenced in custom designs. -->

<!-- END HIDDEN CONTENT -->

