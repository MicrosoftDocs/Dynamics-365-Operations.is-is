---
title: Stofna nýja verðsamning
description: Þetta ferli sýnir hvernig á að stofna viðskiptasamningur þar sem þú skráir inn nýtt söluverð afurðar sem þú hefur ákvarðað með tilteknum viðskiptavin.
author: omulvad
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TradeNonStockedConversion, TradeNonStockedConversionChangeWizard, TradeNonStockedConversionCheckWorksheet, TradeNonStockedConversionWizard, TradeNonStockedRegister
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1e1b48531e7ef7d55774936cb71130d048cdab7
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830457"
---
# <a name="create-a-new-trade-agreement"></a>Stofna nýja verðsamning

[!include [banner](../../includes/banner.md)]

Þetta ferli sýnir hvernig á að stofna viðskiptasamningur þar sem þú skráir inn nýtt söluverð afurðar sem þú hefur ákvarðað með tilteknum viðskiptavin. Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum. Ef þú ert að nota eigin gögn, þarftu áður en byrjað er að þessari handbók að ganga úr skugga um að heiti færslubókar fyrir Verðsamningur er til staðar þar sem Sjálfgefinn tengsl er stillt á "Verð (sala)".


## <a name="create-and-post-a-new-trade-agreement-journal"></a>Stofna og bóka nýja færslubók verðsamnings
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Sala og markaðsstarf > Verð og afslættir > Færslubækur verðsamninga**.
2. Smellt er á **Nýtt**.
3. Í reitnum **Heiti** skal smella á fellilistahnappinn til að opna leitina.
4. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
5. Á **Aðgerðasvæði** er smellt á **Línur**.
6. Í reitnum **Reikningskóði** velurðu „Tafla“.
    
    Í þessu dæmi er verið að uppfæra verð fyrir tiltekinn viðskiptavin, sem þýðir að þarf að velja Töflu. Ef verið var að uppfæra listaverð afurðar, myndirðu velja „Allt“, þannig að nýtt verð myndi gilda fyrir alla viðskiptavini. Ef þú værir að sundurgreina verð milli ólíkra hluta viðskiptavinar þá myndiðu velja Flokk. Til að velja Flokk, verður að hafa að sett upp verðflokka viðskiptavinar.  

7. Í reitnum **Val á lykli** skal smella á fellilistahnappinn til að opna uppflettinguna.
8. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
9. Í reitnum **Vörukóði** velurðu „Tafla“.
    
    Þegar þú færir inn viðskiptasamning af gerðinni „Verð (sala)“ verðurðu að velja einungis „Tafla“ í reitnum **Vörukóði**. Þetta er vegna þess að verð með raungildi og má ekki vera það sama fyrir allar afurðir eða flokka afurða.
    
10. Í reitnum **Vöruvensl** skal smella á fellilistahnappinn til að opna uppflettinguna.
11. Á listanum, veljið afurð sem á að taka með í samningnum. Skrifaðu athugasemd um hvaða vöru sem var valin.  
12. Í reitinn **Frá** slærðu inn lágmarksmagn.
    - Ef viðskiptavinur þarf að panta lágmarksmagn áður en þeir verða gjaldgengir fyrir nýtt verð, þá þarf að tilgreina það magn hér.  
    - Færið inn gildi í svæðinu **Til** til að tilgreina hámarksmagn og ef farið er umfram það mun verð í samningnum ekki vera gilt. Ef þú ert að bjóða verð og afslætti sem byggja á mörgum skilum í magni, þá skaltu tilgreina öll skil í magni sem par af lágmarks- og hámarksmagni í reitunum **Frá** og **Til**, í þessari röð.
13. Í reitinn **Upphæð í gjaldmiðli** skaltu færa inn verð.
14. Undir hlutanum **Upplýsingar**, í reitnum **Frá dags.**, skaltu skrá dags. sem þessi samningur verður ekki gildur frá.
15. Smellt er á **Vista**.
16. Smelltu á **Villuleita**.
17. Smelltu á **Villuleita valdar línur**.
18. Smellt er á **OK**.
19. Smelltu á **Bóka.**
20. Smellt er á **OK**.

## <a name="view-trade-agreements-for-a-product"></a>Skoða viðskiptasamninga fyrir afurð
1. Farðu í **Skoðunarrúða > Kerfiseiningar > Afurðaupplýsingastjórnun > Afurðir > Útgefnar afurðir**.
2. Finna og velja vöru sem verð hefur nýlega verið uppfært verð, á listanum.
3. Í **Aðgerðasvæðinu** smellirðu á **Selja**.
4. Smelltu á **Skoða viðskiptasamninga**.
    
    Fara yfir nákvæmar upplýsingar um verð viðskiptasamnings sem var nýverið stofnaður.    

5. Lokið síðunni.

## <a name="additional-resources"></a>Frekari upplýsingar
### <a name="community-blogs"></a>Samfélagsblogg
- [Söluverð í Dynamics 365 for Finance and Operations](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)
