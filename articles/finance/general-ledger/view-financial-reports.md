---
title: Skoða fjárhagsskýrslur
description: Þetta efnisatriði lýsir því hvernig eigi að skoða fjárhagsskýrslur í Microsoft Dynamics 365 Finance. Það felur í sér upplýsingar um þá ýmsu valkosti sem hægt er að nota í fjárhagsskýrslum til að breyta útlit þeirra og gögn sem þeir hafa.
author: kweekley
ms.date: 03/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.custom: 10334
ms.assetid: d20f435f-fb65-4068-ab09-7efc7be683a6
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e744ade8b02b288821dd9142c85092d384db4b2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816956"
---
# <a name="view-financial-reports"></a>Skoða fjárhagsskýrslur

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig eigi að skoða fjárhagsskýrslur. Það felur í sér upplýsingar um þá ýmsu valkosti sem hægt er að nota í fjárhagsskýrslum til að breyta útlit þeirra og gögn sem þeir hafa.

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
Hægt er að nota síur fyrir vídd og eigind eða breyta fjárhagsáætlunaraðstæðum á **Raun eða fjárhagsáætlun** skýrslu. Á Aðgerðasvæðinu skal smellt á **Valkostir skýrslu**, og fylgið svo einn eða fleiri af eftirfarandi skrefum:

-   Til að nota síur fyrir eigind á skýrslu, veljið **bæta Við eigindarsíu**. Velja skal eigindina, færið inn eigindargildi og smellið **í lagi**. Til dæmis, ef þú velur **Lykiltegund** eigindinni skal færa inn **VSK** sem eigindargildi. Til að fjarlægja eigindarsíu er smellt á **Hreinsa**.
-   Til að nota víddarafmörkun á skýrslu, veljið **Bæta við víddarsíu**. Velja víddina, og svo annað hvort færið inn víddarauðkenni eða velja víddina í lista. Til að fjarlægja víddarsíu er smellt á **Hreinsa**.
-   Til að breyta aðstæðunum á **Raun eða fjárhagsáætlun** skýrslu, veljið nýjar aðstæður og smellið **í lagi**. Ef valdar aðstæður eru fyrir annað fjárhagsár verður engum niðurstöðum skilað. Til dæmis, ef skýrsla er búin til fyrir FY2015 og núverandi atburðarás er fyrir FY2015 og nýja valda atburðarásin er fyrir FY2016 verður engum niðurstöðum skilað. Ef þörf er á nýrri atburðarás fyrir mismunandi fjárhagsár skaltu búa til nýja útgáfu af skýrslunni fyrir fjárhagssárið sem tengist atburðarásinni.

Þegar smellt er á **í lagi**, eru alla valkosti sem valin var beitt á skýrslunni. Ef ákveðið er að ekki á að nota valda valkostir er smellt á **hætta Við**.

## <a name="update-a-financial-report"></a>Uppfæra fjárhagsskýrslu
Hægt er að uppfæra (uppfærslu) fjárhagsskýrslu þannig að það sýnir nýjustu gögn fyrir tímabilið og árið sem skýrslan var mynduð fyrir. Til dæmis, ef þú uppfærir fjárhagsskýrslu sem mynduð var fyrir Október 2015 endurspeglar skýrsluna hvers kyns nýjar færslur sem hafa verið bókaðar fyrir 2015 Október. Til að uppfæra fjárhagsskýrslu, á Aðgerðasvæðinu skal smellt á **Endurnýja**. Uppfært skýrsla er aðeins tiltækur sá sem hana uppfærði. Svo annað fólk geti séð sömu gögn verður að birta skýrsluna.

## <a name="publish-a-financial-report"></a>Birta fjárhagsskýrslu
Þegar búið er að uppfæra fjárhagsskýrslu, er hægt að birta það. Önnur fólkið í fyrirtækinu getur skoða hana. Til að birta skýrslu, á Aðgerðasvæðinu skal smellt á **Birta**.

## <a name="display-a-financial-report-in-a-different-currency"></a>Birta fjárhagsskýrslu í öðrum gjaldmiðli
Hægt er að birta fjárhagsskýrslur í hvaða gjaldmiðli skýrsla á hvaða tíma sem er. Til að sýna skýrslu í öðrum gjaldmiðli, á Aðgerðasvæðinu skal smellt **Gjaldmiðli**, og veljið síðan gjaldmiðil. Skýrslan er þýdd yfir í þeim gjaldmiðli og niðurstöðurnar eru birtar. Allar gjaldmiðilskóða eða tákn sem eru hafðar með sem hluti af skýrsluhönnun eru uppfærðar til að endurspegla nýja gjaldmiðli. Þeim gjaldmiðlum sem birtast á listanum eru skýrslugerðargjaldmiðlar sem eru skilgreindir í Finance.

## <a name="display-a-summarized-view-of-the-financial-report"></a>Birta samantekin yfirlit yfir fjárhagsskýrslu
Fjárhagsskýrsla getur innihaldið upplýsingalínur og samantektarlínur. Upplýsingalínur eru línur sem innihalda aðallykla eða víddir. Samantektarlínur eru lýsingar-, samtölu- og útreikningalínur Til að birta einungis samantektarlínur skýrslu er smellt á **Sýna**, og smellið síðan á **Samantektarlínur aðeins**. Skýrslan er dregin saman og birtir aðeins samantektarlínur. Til að skoða upplýsingalínur ásamt samantektarlínur, smellið á **Sýna**, og smellið síðan á **Samantektarlínur aðeins** aftur.

## <a name="print-a-financial-report"></a>Prenta fjárhagsskýrslu
Prentun fjárhagsskýrslu mun búa til PDF-skrá sem síðan er hægt að prenta handvirkt. Til að búa til prentvæna fjárhagsskýrslu, í aðgerðarúðunni, smellið á **Prenta** og fylgið svo einu eða fleiri af eftirfarandi skrefum til að stilla valkosti prentunar:

-   Til að taka með mismunandi stig upplýsinga í útprentaðri skýrslu, stilltu sleða á **Já** eða **Nei**. Ef skýrslu notar skipurit er hægt að velja að taka með allar einingar skipurits eða aðeins núverandi eining skipurits.
-   Ef stilla á síðustærð skal velja síðustærð á listanum.
-   Ef stilla útlit síðu skal velja útlit á listanum. Ef efni skýrslu til að passa við breiddina sem er valin er sleði stilltur á **Já**.
-   Til að stilla spássíu, færið inn efstu, neðst, vinstri og hægri spássíustærð í tommum.

Eftir að þú hefur lokið við stillingar á valkostum prentunar skaltu smella á **Prenta** til að halda áfram og velja svo hvort eigi að sækja skrána eða vista hana í OneDrive eða SharePoint. Ef þú ákveður að þú vilt ekki halda áfram skaltu smella á **Hætta við** í staðinn. Þegar þú heldur áfram birtist skýrslan á þjóninum og þú verður beðinn um að sækja skýrsluna í PDF-sniði. Nú er hægt að skoða skýrsluna í PDF-lesaranum og héðan geturðu valið prentarann til að senda skýrsluna til, og einnig gera frekari leiðréttingar fyrir valkosti prentunar.

## <a name="export-a-financial-report"></a>Flytja út fjárhagsskýrslu
Til að flytja út fjárhagsskýrslu, á Aðgerðasvæðinu skal smellt á **Birta**. Skýrslan er flutt út í Microsoft Excel og vafrinn biður þig að opna eða vista útfluttar skrár. útflutningsstillingar sem eru skilgreindar í skýrsluhönnuninni eru notaðar fyrir útfluttar skýrslu.    

<a name="additional-resources"></a>Frekari tilföng
--------

[Fjárhagsskýrslugerð](../../dev-itpro/analytics/financial-reporting-intro.md)






[!INCLUDE[footer-include](../../includes/footer-banner.md)]