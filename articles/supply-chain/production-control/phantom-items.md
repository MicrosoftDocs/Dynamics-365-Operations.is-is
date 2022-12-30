---
title: Skuggavörur
description: Þessi grein lýsir í smáatriðum hvernig hægt er að nota línugerð skuggavöru fyrir línurnar í uppskriftum og formúlu í Dynamics 365 Supply Chain Management.
author: johanhoffmann
ms.date: 05/05/2022
ms.topic: article
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-05-05
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 64139873216decd8ecb2fcaf1f284e726c53c332
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893324"
---
# <a name="phantom-items"></a>Skuggavörur

[!include [banner](../includes/banner.md)]

Þessi grein lýsir í smáatriðum hvernig hægt er að nota línugerð skuggavöru fyrir línurnar í uppskriftum og formúlu.

Í mynd 1 er (a) uppskrift fyrir afurð H og hluta F og G og (b) leiðarskjalið fyrir afurðir H og hluta F.

![Mynd 1: Hönnunaruppskrift.](media/product-H-part-F.png)
*Mynd 1: Hönnunaruppskrift.*

Mynd 1 sýnir dæmi um skipulag uppskriftar á tveimur stigum. Lokaafurð H táknar afurð fyrir samsetningu tækis. Samsetning tækis samanstendur af tveimur hlutum, rafeiningu (F) sem er með tvo efnisþætti (A og B) og hópur umbúða (G) sem einnig er með tvo efnisþætti (C og D). Annað efni (E) er notað við almenna samsetningu tækis.

Mynd 1 sýnir hönnunaruppskrift fyrir afurð H. Þessi uppbygging veitir góða yfirsýn yfir hluta og íhluti fyrir heildarsamsetningu tækis. Þótt hönnuðir afurða gætu viljað sjá uppskriftina með þessum hætti, getur hins vegar verið að þessi uppbygging sýni ekki á réttan hátt hvernig tækið er sett upp í vinnusal.

Til dæmis bendir hönnunaruppskriftin í mynd 1 til þess að rafeining F sé sett saman sem aðskilinn hluti á aðskildum vinnufyrirmælum. Í vinnusal getur hins vegar verið að samsetning á rafeiningunni sem hluti af heildarsamsetningu tækisins sé talin æskilegri, en ekki sem aðskilin vinnufyrirmæli.

Hönnunaruppskrfitin gefur einnig til kynna að hluti G sé aðskilinn hluti. Í þessari uppbyggingu táknar hluti G þó ekki efnislegan hluta, heldur safn af umbúðum.

Þess vegna, þrátt fyrir að hönnunaruppskrift sé hagkvæm fyrir hönnun afurðar og viðhaldi á þeirri hönnun, gæti verið að hún sé ekki rökréttasta leiðin til að styðja við framkvæmdarferli á framleiðslu afurðarinnar. Aftur á móti sýnir hönnunaruppskrift bestu leiðina til að búa til afurð.

Mynd 2 sýnir hvernig framangreind uppskrift er umbreytt í framleiðsluuppskrift. Á skýringarmynd 2 er (a) uppskrift fyrir afurð H, og (b) er leiðarskjalið fyrir afurð H.

![Mynd 2: Framleiðsluupskrift.](media/product-H-part-B.png)
*Mynd 2: Framleiðsluupskrift*

Í þessari uppbyggingu er hægt að sjá að ekki er minnst á hluta F og G og efnin sem þessir hlutar samanstanda af hefur verið fært upp á næsta stig uppskriftar.

Ólíkt hönnunaruppskriftinni, sem var með tvö aðgerðarskjöl, hefur framleiðsluuppskriftin aðeins eitt aðgerðarskjal. Umbúðaraðgerðin sem tengdist við hluta G, hefur einnig verið færður upp og er nú hluti af aðgerðarskjali fyrir afurð H. Samsetning rafeiningarinnar er fyrsta aðgerðin. Þessi röð er skynsamleg, því að þessi eining er notuð í næstu aðgerð, sem er samsetning tækisins. Síðasta aðgerðin er umbúðaraðgerðin, sem notar tvö umbúðaefni (C og D).

Umbreytingin á milli hönnunaruppskriftar og framleiðsluuppskriftar virkjuð með línugerð skuggauppskriftarinnar. Eins og hugtakið „skuggi“ bendir til hafa hlutar F og G horfið við umbreytingu á milli uppskriftargerðanna tveggja. Í þessu dæmi er skuggalínugerðin notuð á uppskriftarlínurnar fyrir hluta F og G í hönnunaruppskriftinni. Þegar framleiðslu- eða runupöntun er stofnuð er hönnunaruppskriftin afrituð í framleiðslu- eða runupöntunina. Þá, þegar pöntunin er áætluð, á sér stað umbreyting frá hönnunaruppskrift til framleiðsluuppskriftar, eins og sýnt er á mynd 2. Á aðgerðarblaðinu á mynd 2 er umbúðaefni C og D inntak fyrir aðgerðina.

## <a name="multilevel-phantom-bom-structures"></a>Uppbygging skuggauppskriftar á mörgum stigum

Hægt er að nota skuggalínugerð í marglaga hönnunaruppskrift eins og sýnt er á mynd 3. Í mynd 3 er (a) uppskrift fyrir afurð G, og (b) leiðarskjalið fyrir hluta E og F og afurð G.

![Mynd 3: Hönnunaruppskrift hluti G.](media/product-G.png)
*Mynd 3: Hönnunaruppskrift hluti G*.

Mynd 4 sýnir framleiðsluuppskriftina og leiðarskjalið ef uppskriftarlínur fyrir hluta E og F eru stilltar þannig að línugerðin sé skuggalínugerð. Á skýringarmynd 4 er (a) uppskrift fyrir afurð G, og (b) leiðarskjalið fyrir afurð G.

![Mynd 4: Framleiðsluupskrift hluti G.](media/product-G-route-sheet-G.png)
*Mynd 4: Framleiðsluupskrift hluti G*

## <a name="phantom-and-route-network"></a>Skugga- og leiðanet

Einnig er hægt að nota skuggauppskriftir fyrir uppskrift sem hefur leiðanet. Í leiðaneti eru ein eða fleiri aðgerðir keyrðar samhliða. Mynd 5 sýnir dæmi um leiðanet sem er notað í uppskrift á mörgum stigum. Á skýringarmynd 5 (a) er uppskrift fyrir afurð G og hluta F, og (b) leiðarskjalið fyrir afurð G og hluta F, sem er með leiðanet.

![Mynd 5: Hönnunaruppskrift hluti G, leiðarnet.](media/product-G-part-F.png)
*Mynd 5: Hönnunaruppskrift hluti G, leiðarnet*.

Á skýringarmynd 6 (a) er uppskrift fyrir afurð G og hluta F, og (b) leiðarskjalið fyrir afurð G og hluta F.

![Mynd 6: Framleiðsluupskrift hluti G, leiðarnet.](media/product-G-part-F-with-route-sheet.png)
*Mynd 6: Framleiðsluuppskrift hluti G, leiðarnet*


[!INCLUDE[footer-include](../../includes/footer-banner.md)]