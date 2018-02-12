---
title: "Skoða fjárhagsskýrslur"
description: "Þessi grein útskýrir hvernig á að skoða og kanna fjárhagsskýrslur í Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. Það felur í sér upplýsingar um þá ýmsu valkosti sem hægt er að nota í fjárhagsskýrslum til að breyta útlit þeirra og gögn sem þeir hafa."
author: kweekley
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 10334
ms.assetid: d20f435f-fb65-4068-ab09-7efc7be683a6
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 61763e57a54a24665d7ca899d8a26cf9e4d3984b
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="view-financial-reports"></a>Skoða fjárhagsskýrslur

[!include[banner](../includes/banner.md)]


Þessi grein útskýrir hvernig á að skoða og kanna fjárhagsskýrslur í Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. Það felur í sér upplýsingar um þá ýmsu valkosti sem hægt er að nota í fjárhagsskýrslum til að breyta útlit þeirra og gögn sem þeir hafa.

<a name="financial-reporting-overview"></a>Yfirlit Fjárhagsskýrslugerð
----------------------------

## <a name="open-a-financial-report"></a>Popna fjárhagsskýrslu
Til að opna skýrslu, veljið heiti skýrslu. Í fyrsta sinn sem skýrsla er opnað, er hún sjálfvirkt mynduð fyrir fyrri mánuð. Til dæmis, ef skýrsla er opnuð í fyrsta sinn í Ágúst 2015 er hún mynduð fyrir 31. Júlí 2015. Eftir að skýrsla er opnuð er hægt að hefja skoðun á henni með þvi að kafa niður í sértæka gagnahluta og breyta valkostum skýrslu.

## <a name="drill-down-on-a-financial-report"></a>Kafað í fjárhagsskýrslu
Fjárhagsskýrslur getur innihaldið mörg stig upplýsinga. Fjárhagsleg stig er fyrsta stig sem sést þegar fjárhagsskýrsla er opnuð. Velja gögn til að kafa niður á til að fara á stig lykla. til dæmis til að skoða upplýsingar um lykil fyrir sölu, veljið sölugögnin sem á að skoða. Úr lyklastigi, er hægt að kafa niður til að skoða færslur sem mynda staða lykils. Til eru tvær leiðir til að skoða færslur: skýrslufærslur og færslur fylgiskjals.

-   **Skýrslufærsla** – Færsla birtist í yfirliti sem hefur verið sniðið sem er tekið með í fjárhagsskýrslu. Til að skoða færslur í yfirliti sem hefur verið sniðið til, velja gögn til að kafa niður í og smellið síðan á **Kafa á stig skýrslufærslu**.
-   **Færslur fylgiskjals** – fyrirspurn um færslu fylgiskjals opnast, þar sem hægt er að skoða færslur. Til að skoða færslur í fyrirspurn um færslu fylgiskjals, velja gögn til að kafa niður í og smellið síðan á **opna reikningsfærslur**.

Ef gögnum er fjárhagsáætlunargögn er hægt að velja að opna lykilfærslur fjárhagsáætlunar. Til að loka einhverjum af stigum skýrslu og fara á byrjunarreit, geturðu annað hvort smellt á Esc-takka eða smella á **Loka** hnappinn (**X**) efri hægra megin.

## <a name="change-report-options"></a>Breyta valkostum skýrslu
Hægt er að breyta dagsetningu skýrslunnar, nota síur fyrir vídd og eigind eða breyta fjárhagsáætlunaraðstæðum á **Raun eða fjárhagsáætlun** skýrslu. Á Aðgerðasvæðinu skal smellt á **Valkostir skýrslu**, og fylgið svo einn eða fleiri af eftirfarandi skrefum:

-   Til að Breyta grunntímabilið og grunnári skýrslu, veljið grunntímabil og grunnár, og smella síðan á **í lagi**.
-   Til að nota síur fyrir eigind á skýrslu, veljið **bæta Við eigindarsíu**. Velja skal eigindina, færið inn eigindargildi og smellið **í lagi**. Til dæmis, ef þú velur **Lykiltegund** eigindinni skal færa inn **VSK** sem eigindargildi. Til að fjarlægja eigindarsíu er smellt á **Hreinsa**.
-   Til að nota víddarafmörkun á skýrslu, veljið **Bæta við víddarsíu**. Velja víddina, og svo annað hvort færið inn víddarauðkenni eða velja víddina í lista. Til að fjarlægja víddarsíu er smellt á **Hreinsa**.
-   Til að breyta aðstæðunum á **Raun eða fjárhagsáætlun** skýrslu, veljið nýjar aðstæður og smellið **í lagi**. Ef valdar aðstæður eru fyrir annað ár gætið þess að uppfæra grunnár. Til dæmis, ef núverandi aðstæður eru FY2015 og þú velur nýjar aðstæður sem er fyrir FY2016, skal breyta grunnárið í **2016**.

Þegar smellt er á **í lagi**, eru alla valkosti sem valin var beitt á skýrslunni. Ef ákveðið er að ekki á að nota valda valkostir er smellt á **hætta Við**.

## <a name="update-a-financial-report"></a>Uppfæra fjárhagsskýrslu
Hægt er að uppfæra (uppfærslu) fjárhagsskýrslu þannig að það sýnir nýjustu gögn fyrir tímabilið og árið sem skýrslan var mynduð fyrir. Til dæmis, ef þú uppfærir fjárhagsskýrslu sem mynduð var fyrir Október 2015 endurspeglar skýrsluna hvers kyns nýjar færslur sem hafa verið bókaðar fyrir 2015 Október. Til að uppfæra fjárhagsskýrslu, á Aðgerðasvæðinu skal smellt á **Endurnýja**. Uppfært skýrsla er aðeins tiltækur sá sem hana uppfærði. Svo annað fólk geti séð sömu gögn verður að birta skýrsluna.

## <a name="publish-a-financial-report"></a>Birta fjárhagsskýrslu
Þegar búið er að uppfæra fjárhagsskýrslu, er hægt að birta það. Önnur fólkið í fyrirtækinu getur skoða hana. Til að birta skýrslu, á Aðgerðasvæðinu skal smellt á **Birta**.

## <a name="display-a-financial-report-in-a-different-currency"></a>Birta fjárhagsskýrslu í öðrum gjaldmiðli
Hægt er að birta fjárhagsskýrslur í hvaða gjaldmiðli skýrsla á hvaða tíma sem er. Til að sýna skýrslu í öðrum gjaldmiðli, á Aðgerðasvæðinu skal smellt **Gjaldmiðli**, og veljið síðan gjaldmiðil. Skýrslan er þýdd yfir í þeim gjaldmiðli og niðurstöðurnar eru birtar. Allar gjaldmiðilskóða eða tákn sem eru hafðar með sem hluti af skýrsluhönnun eru uppfærðar til að endurspegla nýja gjaldmiðli. Þeim gjaldmiðlum sem birtast á listanum eru skýrslugerðargjaldmiðlar sem eru skilgreindir í Finance and Operations.

## <a name="display-a-summarized-view-of-the-financial-report"></a>Birta samantekin yfirlit yfir fjárhagsskýrslu
Fjárhagsskýrsla getur innihaldið upplýsingalínur og samantektarlínur. Upplýsingalínur eru línur sem innihalda aðallykla eða víddir. Samantektarlínur eru lýsingar-, samtölu- og útreikningalínur Til að birta einungis samantektarlínur skýrslu er smellt á **Sýna**, og smellið síðan á **Samantektarlínur aðeins**. Skýrslan er dregin saman og birtir aðeins samantektarlínur. Til að skoða upplýsingalínur ásamt samantektarlínur, smellið á **Sýna**, og smellið síðan á **Samantektarlínur aðeins** aftur.

## <a name="open-a-financial-report-from-a-previous-month"></a>Opna fjárhagsskýrslu frá fyrri mánuður
Hægt er að skoða skýrslur fyrir gildandi mánuður eða fyrri mánuðir án þess að endurmynda skýrsluna. Ef opna á skýrslu fyrir fyrri mánuð, smellið á **Sýna**, og smellið síðan á **Fyrri skýrslur**. Listi yfir fyrri mánuðir sem skýrslan hefur verið myndað fyrir birtist. Útvíkka mánuði til að skoða skýrslu fyrir, velja dagsetningu og smellið síðan á **í lagi**. skýrslan fyrir mánuðinn er birt. til að snúa aftur í skýrslu núverandi mánuði , smellið á **hætta Við**.

## <a name="print-a-financial-report"></a>Prenta fjárhagsskýrslu
til að prenta fjárhagsskýrslu, í Aðgerðarúðunni, smellið á  **Prenta**, og fylgið svo einn eða fleiri af eftirfarandi skrefum til að stilla valkosti prentunar:

-   Til að taka með mismunandi stig upplýsinga í útprentaðri skýrslu, stilltu sleða á **Já** eða **Nei**. Ef skýrslu notar skipurit er hægt að velja að taka með allar einingar skipurits eða aðeins núverandi eining skipurits.
-   Ef stilla á síðustærð skal velja síðustærð á listanum.
-   Ef stilla útlit síðu skal velja útlit á listanum. Ef efni skýrslu til að passa við breiddina sem er valin er sleði stilltur á  **Já**.
-   Til að stilla spássíu, færið inn efstu, neðst, vinstri og hægri spássíustærð í tommum.

Eftir að lokið hefur verið við að stilla valkosti prentunar, smellið á **Prenta** til að prenta skýrsluna. Ef ákveðið er að ekki á að prenta skýrsluna, smellt á **hætta Við**. Forskoðun prentuðu skýrslunni er birt. Hægt er að velja prentara til að senda skýrsluna til, og einnig er hægt að stilla valkosti prentunar.

## <a name="export-a-financial-report"></a>Flytja út fjárhagsskýrslu
Til að flytja út fjárhagsskýrslu, á Aðgerðasvæðinu skal smellt á **Birta**. Skýrslan er flutt út í Microsoft Excel og vafrainn biður þig að opna eða vista útfluttar skrár. útflutningsstillingar sem eru skilgreindar í skýrsluhönnuninni eru notaðar fyrir útfluttar skýrslu.    

<a name="see-also"></a>Sjá einnig
--------

[Fjárhagsskýrslur fyrir Microsoft Dynamics AX](../../dev-itpro/analytics/financial-reporting-intro.md)





