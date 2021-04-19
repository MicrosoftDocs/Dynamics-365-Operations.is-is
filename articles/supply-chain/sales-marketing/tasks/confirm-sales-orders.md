---
title: Staðfesta sölupantanir
description: Þetta ferli sýnir hvernig á að staðfesta sölupantanir.
author: omulvad
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, CustConfirmJournal, SysQueryForm, SysQueryFieldLookUp, SysLookup, SalesParmIdLookup, SalesUnconfirmedOrdersPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e681a822ae1ec628fd20931263a6115b998ffba9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836471"
---
# <a name="confirm-sales-orders"></a>Staðfesta sölupantanir

[!include [banner](../../includes/banner.md)]

Þetta ferli sýnir hvernig á að staðfesta sölupantanir. Þér verður sýnt hvernig á að staðfesta eina pöntun og hvernig staðfesta á margar pantanir í einu. Þessi verkefni eru yfirleitt framkvæmd af sölupantanavinnslu. Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn. Áður en byrjað er, gangið úr skugga um að það eru nokkrar opnar sölupantanir fyrir sama viðskiptavininn. Ef verið er að nota USMF er hægt að velja lykil US-027.


## <a name="confirm-a-single-sales-order"></a>Staðfesta eina sölupöntun.
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Sala og markaðssetning > Sölupantanir > Allar sölupantanir**.
2. Finna og velja pöntunina sem á að staðfesta á listanum.
3. Smelltu á tengil á sölupöntun til að opna valda pöntun.
4. Í **Aðgerðasvæðinu** smellirðu á **Selja**.
5. Smellt er á **Staðfesta sölupantanir**.
6. Útvíkkaðu hlutann **Færibreytur**. Passaðu að valkosturinn **Bókun** sé stilltur á Já.  
7. Stilltu valkostinn **Prenta staðfestingu** á Já. Reiturinn **Athuga lánamark** tilgreinir aðferðina sem er notuð til að reikna út eftirstandandi lánsheimild viðskiptavinar. Sjálfgefið er að hún sé afrituð af síðunni Færibreytur viðskiptakrafna. Ef sleppa á athugun á lánamörkum þegar tiltekinni sölupöntun er staðfest skal stilla **Athuga lánamark** á Engin. Hins vegar ætti að hafa í huga að jafnvel með ef þetta svæði er stillt á Ekkert, verða athugun á lánamörkum samt framkvæmd ef valkosturinn **Áskilið lánamark** er valinn á aðalgögnum viðskiptavinar. 
8. Smellt er á **OK**.
9. Smellið á **Já**.
10. Lokið síðunni.
11. Á **aðgerðasvæðinu** er smellt á **Valkosti**.
12. Smelltu á **Skoða breytingu**.
13. Smelltu á **Skoða haus**. Þegar pöntun er staðfest, er **Staða skjals** stillt á Staðfestingu. 
14. Í **Aðgerðasvæðinu** smellirðu á **Selja**.
15. Smellt er á **Staðfesting sölupöntunar**.
16. Lokið síðunni.

## <a name="confirm-multiple-sales-orders-at-once"></a>Staðfesta margar sölupantanir í einu
1. Farðu í **Sölu og markaðssetningu > Sölupantanir > Staðfesting á pöntun > Staðfesta sölupöntun**.
2. Smellið á **Velja**.
3. í listanum á flipanum **Afmörkun** skaltu finna og velja færsluna sem vísar í reitinn **Viðskiptavinalykill**.
4. Í reitnum **Skilyrði** skal smella á fellilistahnappinn til að opna leitina.
5. Finna og veljið lykil viðskiptavinar sem er með margar pantanir sem óskað er að staðfesta margar í einu, af listanum. Ef verið er að nota USMF er hægt að velja lykil US-027.  
6. Smellt er á **OK**.
    - Flipinn **Yfirlit** sýnir lista yfir pantanir sem uppfylla skilyrði fyrirspurnar. Þær verða teknar með í staðfestingu.  
    - Reiturinn **Safnuppfærsla fyrir** í hlutanum **Færibreytur** tilgreinir færibreytu sem farið er eftir þegar margar pantanir eru teknar saman í eina staðfestingarskjal. Að sjálfgefnu er valkosturinn afritaður úr **Sjálfgildum fyrir stillingu safnuppfærslu** á síðunni **Færibreytur viðskiptakrafna**.  
7. Í reitnum **Safnuppfærsla fyrir** skaltu velja 'Pöntun'. Þær lágmarksfæribreytur sem er krafist til að stofna samantekt eru **Reikningslykill** og **Gjaldmiðill**. Þetta þýðir að safnuppfærslur með mismunandi reikningslykla og mismunandi gjaldmiðla eru ekki leyfðar. Hægt er að setja upp viðbótarfæribreytur á síðunni **Færibreytur safnuppfærslu** sem er aðgengileg af síðunni **Færibreytur viðskiptakrafna**. 
8. Í reitnum **Sölupöntun** skal smella á fellilistahnappinn til að opna leitina.
9. Á listanum, veljið pöntunarnúmer sem á að verða safnpöntunin.
10. Smellið á **Raða**.
11. Smellt er á **OK**.
12. Smellt er á **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]