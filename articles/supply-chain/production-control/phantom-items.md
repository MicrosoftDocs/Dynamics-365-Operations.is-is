---
title: Skuggavörur
description: Þetta efnisatriði lýsir í smáatriðum hvernig hægt er að nota línugerð skuggavöru fyrir línurnar í uppskriftum og formúlu í Dynamics 365 Supply Chain Management.
author: ShylaThompson
manager: tfehr
ms.date: 06/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: kamaybac
ms.search.validfrom: ''
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: b14bebadd7088c9bbcfb6b1c5df1fe1a3c98694d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430517"
---
# <a name="phantom-items"></a>Skuggavörur

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir í smáatriðum hvernig hægt er að nota línugerð skuggavöru fyrir línurnar í uppskriftum og formúlu. Í eftirfarandi skýringarmynd er (a) uppskrift fyrir afurð H og hluta F og G og (b) leiðarskjalið fyrir afurðir H og hluta F.

![Afurð H og hluti F](media/product-H-part-F.png)


Þessi skýringarmynd sýnir dæmi um skipulag uppskriftar á tveimur stigum. Lokaafurð H táknar afurð fyrir samsetningu tækis. Samsetning tækis samanstendur af tveimur hlutum, rafeiningu (F) sem er með tvo efnisþætti (A og B) og hópur umbúða (G) sem einnig er með tvo efnisþætti (C og D). Annað efni (E) er notað við almenna samsetningu tækis.

![Afurð H og hluti F](media/product-H-part-B.png)

Framangreind skýringarmynd sýnir hönnunaruppskrift fyrir afurð H. Þessi uppbygging veitir góða yfirsýn yfir hluta og íhluti fyrir heildarsamsetningu tækis. Þótt hönnuðir afurða gætu viljað sjá uppskriftina með þessum hætti, getur hins vegar verið að þessi uppbygging sýni ekki á réttan hátt hvernig tækið er sett upp í vinnusal. 

Til dæmis bendir hönnunaruppskriftin í framagreindri skýringamynd til þess að rafeining F sé sett saman sem aðskilinn hluti á aðskildum vinnufyrirmælum. Í vinnusal getur hins vegar verið að samsetning á rafeiningunni sem hluti af heildarsamsetningu tækisins sé talin æskilegri, en ekki sem aðskilin vinnufyrirmæli.

Hönnunaruppskrfitin gefur einnig til kynna að hluti G sé aðskilinn hluti. Í þessari uppbyggingu táknar hluti G þó ekki efnislegan hluta, heldur safn af umbúðum. 

Þess vegna, þrátt fyrir að hönnunaruppskrift sé hagkvæm fyrir hönnun afurðar og viðhaldi á þeirri hönnun, gæti verið að hún sé ekki rökréttasta leiðin til að styðja við framkvæmdarferli á framleiðslu afurðarinnar. Aftur á móti sýnir hönnunaruppskrift bestu leiðina til að búa til afurð.

Eftirfarandi skýringarmynd sýnir hvernig framangreind uppskrift er umbreytt í framleiðsluuppskrift. Í þessari skýringarmynd er (a) uppskrift fyrir afurð H, og (b) er leiðarskjalið fyrir afurð H.

Í þessari uppbyggingu er hægt að sjá að ekki er minnst á hluta F og G og efnin sem þessir hlutar samanstanda af hefur verið fært upp á næsta stig uppskriftar. 

Ólíkt hönnunaruppskriftinni, sem var með tvö aðgerðarskjöl, hefur framleiðsluuppskriftin aðeins eitt aðgerðarskjal. Umbúðaraðgerðin sem tengdist við hluta G, hefur einnig verið færður upp og er nú hluti af aðgerðarskjali fyrir afurð H. Samsetning rafeiningarinnar er fyrsta aðgerðin. Þessi röð er skynsamleg, því að þessi eining er notuð í næstu aðgerð, sem er samsetning tækisins. Síðasta aðgerðin er umbúðaraðgerðin, sem notar tvö umbúðaefni (C og D).

Umbreytingin á milli hönnunaruppskriftar og framleiðsluuppskriftar virkjuð með línugerð skuggauppskriftarinnar. Eins og hugtakið „skuggi“ bendir til hafa hlutar F og G horfið við umbreytingu á milli uppskriftargerðanna tveggja. Í þessu dæmi er skuggalínugerðin notuð á uppskriftarlínurnar fyrir hluta F og G í hönnunaruppskriftinni. Þegar framleiðslu- eða runupöntun er stofnuð er hönnunaruppskriftin afrituð í framleiðslu- eða runupöntunina. Þá, þegar pöntunin er áætluð, á sér stað umbreyting frá hönnunaruppskrift til framleiðsluuppskriftar, eins og sýnt er á framangreindri skýringarmynd. Í aðgerðarskjalinu í annarri skýringarmyndinni er umbúðaefni C og D aðföng fyrir aðgerðina. 

## <a name="multilevel-phantom-bom-structures"></a>Uppbygging skuggauppskriftar á mörgum stigum
Hægt er að nota skuggalínugerð í marglaga hönnunaruppskrift eins og sýnt er á eftirfarandi skýringarmynd. Í þessari skýringarmynd er (a) uppskrift fyrir afurð G, og (b) leiðarskjalið fyrir hluta E og F og afurð G. 

![Afurð G og hluti F með leiðarskjölum](media/product-G-route-sheet-G.png)


Eftirfarandi skýringarmynd sýnir framleiðsluuppskriftina og leiðarskjalið ef uppskriftarlínur fyrir hluta E og F eru stilltar þannig að línugerðin sé skuggalínugerð. Í þessari skýringarmynd er (a) uppskrift fyrir afurð G, og (b) leiðarskjalið fyrir afurð G.

![Afurð G](media/product-G.png)


## <a name="phantom-and-route-network"></a>Skugga- og leiðanet
Einnig er hægt að nota skuggauppskriftir fyrir uppskrift sem hefur leiðanet. Í leiðaneti eru ein eða fleiri aðgerðir keyrðar samhliða. Eftirfarandi skýringarmynd sýnir dæmi um leiðanet sem er notað í uppskrift á mörgum stigum. Í þessari skýringarmynd er (a) uppskrift fyrir afurð G og hluta F, og (b) leiðarskjalið fyrir afurð G og hluta F, sem er með leiðanet.

![Afurð G og hluti F](media/product-G-part-F.png)


Í eftirfarandi skýringarmynd er (a) uppskrift fyrir afurð G og hluta F og (b) leiðarskjalið fyrir afurð G og hluta F.

![Afurð G og hluti F með leiðarskjölum](media/product-G-part-F-with-route-sheet.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]