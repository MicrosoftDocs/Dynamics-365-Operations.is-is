--- 
title: "Staðfesta sölupantanir"
description: "Þetta ferli sýnir hvernig á að staðfesta sölupantanir."
author: omulvad
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, CustConfirmJournal, SysQueryForm, SysQueryFieldLookUp, SysLookup, SalesParmIdLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7cab69222c5004e6a62c632a9e85085403434ffd
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="confirm-sales-orders"></a>Staðfesta sölupantanir

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli sýnir hvernig á að staðfesta sölupantanir. Þér verður sýnt hvernig á að staðfesta eina pöntun og hvernig staðfesta á margar pantanir í einu. Þessum verkefnum myndi venjulega að framkvæma af sölupantanavinnsla. Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn. Áður en byrjað er, gangið úr skugga um að það eru nokkrar opnar sölupantanir fyrir sama viðskiptavininn. Ef verið er að nota USMF er hægt að velja lykil US-027..


## <a name="confirm-a-single-sales-order"></a>Staðfesta eina sölupöntun.
1. Fara í Sölu og markaðssetningu > sölupöntun > Allar sölupantanir
2. Finna og velja pöntunina sem á að staðfesta á listanum.
3. Smelltu á tengil á sölupöntun til að opna valda pöntun.
4. Í aðgerðasvæðinu er smellt á selja.
5. Smellt er á Staðfesta sölupantanir.
6. Útvíkka eða draga saman hlutann Færibreytur.
    * Gangið úr skugga um að Já svæðið í Bókun er virkt.  
7. Stillt Prenta staðfestingu valkost á Já.
    * Svæðið Athuga lánamark tilgreinir aðferðina sem er notuð til að reikna út eftirstandandi lánsheimild viðskiptavinar. Sjálfgefið er að hún sé afrituð af síðunni Færibreytur viðskiptakrafna. Ef sleppa á athugun á lánamörkum þegar tiltekinni sölupöntun er staðfest, lánamörk eru stillt á Engin. Hins vegar ætti að hafa í huga að jafnvel með ef þetta svæði er stillt á Ekkert, verða athugun á lánamörkum samt framkvæmd ef valkosturinn Áskilið lánamark er valinn á aðalgögnum viðskiptavinar.  
8. Smellið á „Í lagi“.
9. Smella á Já.
10. Lokið síðunni.
11. Í aðgerðasvæðinu er smellt á valkostir.
12. Smellið á skoða Breytingu.
13. Smellið á skoða Haus.
    * Þegar pöntun er staðfest, er staða Skjals stillt á Staðfestingu.  
14. Í aðgerðasvæðinu er smellt á selja.
15. Smellt er á Staðfesting sölupöntunar.
16. Lokið síðunni.

## <a name="confirm-multiple-sales-orders-at-once"></a>Staðfesta margar sölupantanir í einu
1. Fara í Sölu og markaðssetningu > sölupantanir > Staðfesting á pöntun > Staðfesta sölupöntun.
2. Smellið á Velja.
3. í listanum á flipanum Afmörkun, Finna og velja færsluna sem vísar í svæðinu viðskiptavinalykill
4. Í reitnum skilyrði skal smella á fellilistahnappinn til að opna leitina.
5. Finna og veljið lykil viðskiptavinar sem er með margar pantanir sem óskað er að staðfesta margar í einu, af listanum.
    * Ef verið er að nota USMF er hægt að velja lykil US-027..  
6. Smellið á „Í lagi“.
    * Flipinn Yfirlit sýnir lista yfir pantanir sem uppfylla skilyrði fyrirspurnar. Þær verða teknar með í staðfestingu.  
    * Safnuppfærsla fyrir svæði tilgreinir færibreytu sem farið er eftir þegar margar pantanir eru teknar saman í eina staðfestingarskjal. Að sjálfgefnu er valkosturinn afrituð úr sjálfgildi fyrir stillingu safnuppfærslu á síðunni færibreytur viðskiptakrafna.  
7. Í Safnuppfærsla fyrir svæði, velja 'Pöntun'.
    * Þær lágmarksfæribreytur sem er krafist til að stofna samantekt eru reikningslykill og gjaldmiðill. Þetta þýðir að safnuppfærslur með mismunandi reikningslykla og mismunandi gjaldmiðla eru ekki leyfðar. Hægt er að setja upp viðbótarfæribreytur færibreytusíðu safnuppfærslu sem er aðgengileg úr síðunni færibreytur viðskiptakrafna.  
8. Í reitnum sölupöntun skal smella á fellilistahnappinn til að opna leitina.
9. Á listanum, veljið pöntunarnúmer sem á að verða safnpöntunin.
10. Smellið á Raða.
11. Smellið á „Í lagi“.
12. Smellið á „Í lagi“.


