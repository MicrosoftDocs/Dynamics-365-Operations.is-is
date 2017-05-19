---
title: "Umbúðaefni og gjöld"
description: "Umbúðaefnisgjald er greitt með ákveðnu millibili til endurvinnslufyrirtækis. Upphæð byggð á þyngdareiningu er greidd fyrir hvern þann efnivið sem umbúðaeining samanstendur af. Umbúðaefnisgjald er reiknað út og tilkynnt en engar fjárhagsfærslur eru bókaðar þar sem gjöldin eru ekki reiknuð sem skattur sem greiða skal yfirvöldum."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventPackagingGroup, InventPackagingMaterialCode, InventPackagingMaterialFee, InventPackagingMaterialTrans, InventPackagingMaterialTransPurch, InventPackagingUnit
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2194
ms.assetid: 040b65dc-43c9-4256-b69f-b2d6e736fbe9
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: d8296dd0347a325a9ff3bd06f558d161ab4030dc
ms.contentlocale: is-is
ms.lasthandoff: 04/25/2017


---

# <a name="packing-materials-and-fees"></a>Umbúðaefni og gjöld

[!include[banner](../includes/banner.md)]


Umbúðaefnisgjald er greitt með ákveðnu millibili til endurvinnslufyrirtækis. Upphæð byggð á þyngdareiningu er greidd fyrir hvern þann efnivið sem umbúðaeining samanstendur af. Umbúðaefnisgjald er reiknað út og tilkynnt en engar fjárhagsfærslur eru bókaðar þar sem gjöldin eru ekki reiknuð sem skattur sem greiða skal yfirvöldum.

Þyngd umbúðaefnis og gjöld eru reiknuð bæði fyrir sölu- og innkaupapantanalínur.

Þú Getur skilgreina einn eða fleiri umbúðaeining fyrir vöru, fyrir pökkunarflokk vörum eða fyrir öll atriði. Umbúðaeining samanstendur af ýmsum umbúðaefnum, þyngd þess, og vörufjölda sem tilheyrir umbúðaeiningu. Umbúðaefniskóða er úthlutað á hverja gerð umbúðaefnis sem  er skilgreint. Byggt á umbúðaefniskóðanum, er hægt að tilgreina verð fyrir tiltekið tímabil. Umbúðaefnisgjald er reiknað á grundvelli þessara upplýsinga.

| **Ábending**                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Jafnvel þótt fyrirtækið greiði ekki umbúðaefnisgjald er hægt að nota aðgerðina til að reikna talnagögn fyrir umbúðaþyngd. |

## <a name="setup-requirements-for-packing-material-fees"></a>Uppsetningarþarfir fyrir umbúðaefnisgjald
Áður en reiknað er þyngd umbúðaefnis, umbúðaefnisgjald eða bæði þarf að stofna eftirfarandi grunngögn:

-   Umbúðaflokkar - stofna umbúðaflokka til að úthluta á vörur.
-   Umbúðefnakóðar – Stofnið umbúðaefniskóða fyrir hverja gerð umbúðaefnis sem er skilgreint.
-   Umbúðaeiningar - tilgreina umbúðaeiningu fyrir vörur, fyrir umbúðaflokk eða allar vörur. Fyrir hverja efniseiningu skal skilgreina hvaða umbúðaefni hún innifelur, úthluta þyngd, og reitnum umbúðaeiningarstuðull, færið inn umreiknistuðullinn úr birgðaeiningunni.
-   Umbúðaefnisgjald - Tilgreinið umbúðaefnisgjald á hvern umbúðaefniskóða. Tilgreinið fyrir hverja efnisgerð gildistíma, verð á efni, gjaldmiðil og einingu.

## <a name="packing-units-on-sales-order-lines"></a>Umbúðaeiningar í sölupöntunarlínum
Þegar sölupöntunarlína er stofnuð er athugun framkvæmd til að sjá hvort umbúðaeiningar hafi verið tilgreindar fyrir vöruna. Ef svo er mun sölupöntunarlínan uppfærast sjálfkrafa af kerfinu með tilgreindri umbúðaeiningu og magni umbúðaeiningar. Magn umbúðaeiningar er reiknað á grundvelli pantaðs magns deilt með fjölda vara í valinni pökkunareiningu. Hafi pökkunareining ekki verið tilgreind er hægt að færa inn umbúðaeiningu og magn handvirkt á sölupöntunarlínu. Einnig er mögulegt að breyta pökkunareiningu og magni hennar þegar sölupöntunarlína er bókuð. Þetta á við ef sölupöntunarlína er aðeins afhent eða reikningsfærð að hluta. Þegar þú reikningsfærir sölupöntun er stofnuð nýja umbúðaefnisfærslu Umbúðaefnisfærslur innihalda þyngd umbúðaefnis fyrir sölulínuna. Einnig er hægt að breyta færslum eftir reikningsfærslu og stofna síðan nýjar færslur.

## <a name="packing-units-on-purchase-order-lines"></a>Umbúðaeiningar í innkaupapöntunarlínum
Umbúðaefnisfærslur fyrir innkaupapöntunarlínu eru ekki stofnaðar af kerfinu. Þú Stofna færslur fyrir reikningsfærðar innkaupapöntunarlínur handvirkt í **umbúðaefnisfærslur** síðu.

## <a name="set-up-customer-packagingmaterialfee-license-numbers"></a>Setja upp leyfiskóða fyrir pökkunarefnisgjöld handa viðskiptavini
Ef viðskiptavinir greiða gjöld vegna pökkunarefnis skal tilgreina leyfisnúmer umbúðaefnisgjalds viðskiptavinarins í síðunni **viðskiptavinur**. Þegar leyfisnúmer hefur verið úthlutað viðskiptavini, eru gjöld vegna pökkunarefnis reiknuð sjálfkrafa þegar sölupantanir eru reikningsfærðar. Að lokinni reikningsfærslu er gátreiturinn  **Reikna gjald** hreinsaður í síðunni **umbúðaefnisfærslur** þar sem ekki er þörf á að prenta og reikna út skýrsluna . Mögulegt er að prenta þyngd umbúða á reikninginn og tilkynna viðskiptavini að hann greiði viðkomandi gjöld. 

Ef fyrirtækið þitt greiðir gjöld fyrir umbúðir skal ekki fylla inn leyfiskóða viðskiptavinar. Að lokinni reikningsfærslu er gátreiturinn  **Reikna gjald** valinn í síðunni **umbúðaefnisfærslur**. Þetta gefur til kynna að gjöldin eru reiknuð þegar skýrsla er stofnuð. Mögulegt er að prenta þyngd umbúða á reikninginn og gefa til kynna að fyrirtæki þitt greiði viðkomandi gjöld.

## <a name="print-packaging-material-weights-on-invoices"></a>Prenta þyngd pökkunarefnis á reikninga
Mögulegt er að prenta þyngd umbúða og gefa til kynna á reikningnum hver greiðir umbúðagjöld. Þyngd er dregin saman fyrir hvern pökkunarkóða.
 





