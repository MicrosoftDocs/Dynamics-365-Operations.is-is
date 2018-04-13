---
title: "Úthlutunarreglur fjárhags"
description: "Þessi grein gefur upplýsingar um úthlutunarreglur fjárhags. Hún lýsir hinum ýmsu þáttum þessara úthlutunarreglna og úthlutunaraðferðunum sem hægt er að nota fyrir þær."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAllocation, LedgerAllocationBasisRule, LedgerAllocationRequest, LedgerAllocationRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15402
ms.assetid: 8147e148-7c11-45ef-95c6-f9889a875b54
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 63562cde3f2813fdcfc9df7ccbfc623aa2fbe9b1
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="ledger-allocation-rules"></a>Úthlutunarreglur fjárhags

[!INCLUDE [banner](../includes/banner.md)]

Þessi grein gefur upplýsingar um úthlutunarreglur fjárhags. Hún lýsir hinum ýmsu þáttum þessara úthlutunarreglna og úthlutunaraðferðunum sem hægt er að nota fyrir þær.

Úthlutunarreglur fjárhags eru notaðar til að reikna sjálfkrafa og búa til úthlutunarbækur og færslur í lykil fyrir úthlutun á fjárhagsstöðum eða föstum upphæðum Úthlutunaraðferðir geta verið breytilegar eða fastar. Hægt er að nota eftirfarandi úthlutunaraðferðir fyrir úthlutunarreglur fjárhags:

-   **Grunnur** – Þessi breytuaðferð er notuð þegar úthlutun fer eftir raunverulegri fjárhagsstöðu, byggt á skilyrðum síunnar. Til dæmis væri hægt að úthluta auglýsingakostnaði byggt á sölu hverrar deildar í samræmi við heildarsölu deildar.
-   **Föst prósenta** og **Föst þyngd** – Fyrir þessar aðferðir er úthlutunarhlutfall eða þyngd skilgreind beint fyrir regluna. Til dæmis er hægt að úthluta auglýsingakostnaði þannig að Deild A taki 70 prósent auglýsingakostnaðar og Deild B fái 30 prósent.
-   **Jafnt** – Þessi aðferð dreifir upphæð jafnt á hvern skilgreindan áfangastað. Til dæmis, ef áfangastaðir eru skilgreindir fyrir Deild A og Deild B, er hægt að úthluta auglýsingakostnaði þannig Deild A og Deild B fá 50 prósent auglýsingakostnaðar.

Ef úthlutunaraðferð úthlutunarreglunnar er Grunnur verður einnig að skilgreina sérstakar grunnreglur fjárhagsúthlutunar. Ferlið „Vinna úthlutunarbeiðni“ gerir notendum kleift að keyra úthlutunarreglu fjárhags og forskoða meðfylgjandi úthlutunarbókafærslur áður en þær bóka annaðhvort eða eyða reiknuðum úthlutunum.

## <a name="components-of-ledger-allocation-rules"></a>Íhlutir úthlutunarreglna fjárhags
Hver úthlutunarregla hefur fjóra meginþætti: almennt, uppruna, áfangastað og mótbókun. Viðbótaríhlutur, grunnúthlutunarreglur fjárhags, er nauðsynlegur ef Grunnur er notaður seð úthlutunaraðferð. Hver íhlutur veitir mikilvægar upplýsingar sem er krafist til að keyra úthlutanir.

-   **Almennt** – Þessi íhlutur er þar sem notandinn skilgreinir valkosti eins og úthlutunarreglu, stillingar samstæðureglu og hvort reglan sé virk eða ekki.
-   **Uppruni** – Þessi íhlutur er þar sem notandinn tilgreinir upprunagögn fyrir úthlutunina. Hægt er að byggja úthlutun á fjárhagsstöðum (**Gagnagjafi** = **= Fjárhagur**) eða föstum upphæðum (**Gagnagjafi =** = **Fast gildi**). Þegar **Gagnagjafi** er stilltur á **Fjárhag**, verður að skilgreina uppruna síuskilyrða fyrir úthlutunarreglu fjárhags (til dæmis, fyrir auglýsingakostnað).
-   **Viðtökustaður** – Þessi íhlutur skilgreinir hvernig dreifa skal og gera grein fyrir niðurstöðu úthlutunarútreiknings. Til dæmis getur verið ein lína áfangastaðar fyrir hverja deild.
-   **Mótlykill** – Þessi íhlutur skilgreinir hvernig ákvarða skal aðallykla og víddir fyrir mótfærslurnar sem jafna færslur á áfangastað. Þessar færslur eru yfirleitt notaðar í stað lykla og vídda sem eru byggðar á grunni uppruna. Þegar **Gagnagjafi** er stilltur á **Fast gildi**, er ekki hægt að nota **Uppruna** sem valkost.
-   **Grunnreglur fjárhagsúthlutunar** – Þessar reglur nota eigin skilyrði upprunasíu til að ákvarða hvaða fjárhagsstöður á að nota fyrir úthlutun (til dæmis tekjur á deild). Hægt er að nota grunnreglu úthlutunar með mörgum úthlutunarreglum.





