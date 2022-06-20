---
title: Skuggavörur
description: Þessi grein lýsir því hvernig hægt er að nota Phantom-línugerðina fyrir línurnar í efnisyfirliti (BOM) og formúlu í Dynamics 365 Supply Chain Management.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893324"
---
# <a name="phantom-items"></a>Skuggavörur

[!include [banner](../includes/banner.md)]

Þessi grein lýsir í smáatriðum hvernig hægt er að nota Phantom-línugerðina fyrir línurnar í efnisyfirliti (BOM) og formúlu.

Á mynd 1 er (a) uppskrift fyrir vöru H og hluta F og G, og (b) er leiðarblað fyrir vörur H og hluta F.

![Mynd 1: Verkfræðiuppskrift.](media/product-H-part-F.png)
*Mynd 1: Verkfræðiuppskrift*

Mynd 1 sýnir dæmi um uppskriftaruppbyggingu á tveimur stigum. Lokaafurð H táknar afurð fyrir samsetningu tækis. Samsetning tækis samanstendur af tveimur hlutum, rafeiningu (F) sem er með tvo efnisþætti (A og B) og hópur umbúða (G) sem einnig er með tvo efnisþætti (C og D). Annað efni (E) er notað við almenna samsetningu tækis.

Mynd 1 sýnir verkfræðiuppskrift fyrir vöru H. Þessi uppbygging veitir góða yfirsýn yfir hluta og íhluti heildarvélasamstæðunnar. Þótt hönnuðir afurða gætu viljað sjá uppskriftina með þessum hætti, getur hins vegar verið að þessi uppbygging sýni ekki á réttan hátt hvernig tækið er sett upp í vinnusal.

Til dæmis gefur verkfræðiuppskriftin á mynd 1 til kynna að rafeining F sé sett saman sem aðskilinn hluti á sérstakri verkbeiðni. Í vinnusal getur hins vegar verið að samsetning á rafeiningunni sem hluti af heildarsamsetningu tækisins sé talin æskilegri, en ekki sem aðskilin vinnufyrirmæli.

Hönnunaruppskrfitin gefur einnig til kynna að hluti G sé aðskilinn hluti. Í þessari uppbyggingu táknar hluti G þó ekki efnislegan hluta, heldur safn af umbúðum.

Þess vegna, þrátt fyrir að hönnunaruppskrift sé hagkvæm fyrir hönnun afurðar og viðhaldi á þeirri hönnun, gæti verið að hún sé ekki rökréttasta leiðin til að styðja við framkvæmdarferli á framleiðslu afurðarinnar. Aftur á móti sýnir hönnunaruppskrift bestu leiðina til að búa til afurð.

Mynd 2 sýnir hvernig fyrri verkfræðiuppskrift er færð yfir í framleiðsluuppskrift. Á mynd 2 er (a) uppskrift fyrir vöru H og b er leiðarblað fyrir vöru H.

![Mynd 2: Framleiðsluuppskrift.](media/product-H-part-B.png)
*Mynd 2: Framleiðsluuppskrift*

Í þessari uppbyggingu er hægt að sjá að ekki er minnst á hluta F og G og efnin sem þessir hlutar samanstanda af hefur verið fært upp á næsta stig uppskriftar.

Ólíkt hönnunaruppskriftinni, sem var með tvö aðgerðarskjöl, hefur framleiðsluuppskriftin aðeins eitt aðgerðarskjal. Umbúðaraðgerðin sem tengdist við hluta G, hefur einnig verið færður upp og er nú hluti af aðgerðarskjali fyrir afurð H. Samsetning rafeiningarinnar er fyrsta aðgerðin. Þessi röð er skynsamleg, því að þessi eining er notuð í næstu aðgerð, sem er samsetning tækisins. Síðasta aðgerðin er umbúðaraðgerðin, sem notar tvö umbúðaefni (C og D).

Umbreytingin á milli hönnunaruppskriftar og framleiðsluuppskriftar virkjuð með línugerð skuggauppskriftarinnar. Eins og hugtakið „skuggi“ bendir til hafa hlutar F og G horfið við umbreytingu á milli uppskriftargerðanna tveggja. Í þessu dæmi er skuggalínugerðin notuð á uppskriftarlínurnar fyrir hluta F og G í hönnunaruppskriftinni. Þegar framleiðslu- eða runupöntun er stofnuð er hönnunaruppskriftin afrituð í framleiðslu- eða runupöntunina. Síðan, þegar pöntunin er áætluð, á sér stað umskipti frá verkfræðiuppskrift yfir í framleiðsluuppskrift, eins og sýnt er á mynd 2. Af rekstrarblaðinu á mynd 2 eru umbúðir C og D inntak fyrir aðgerðina.

## <a name="multilevel-phantom-bom-structures"></a>Uppbygging skuggauppskriftar á mörgum stigum

Hægt er að nota Phantom línugerðina í fjölþrepa uppskriftarmannvirkjum, eins og sýnt er á mynd 3. Á mynd 3 er (a) uppskrift fyrir vöru G og (b) er leiðarblað fyrir hluta E og F og vöru G.

![Mynd 3: Verkfræðiuppskrift hluti G.](media/product-G.png)
*Mynd 3: Verkfræðiuppskrift hluti G*

Mynd 4 sýnir framleiðsluuppskrift og leiðarblað ef uppskriftarlínur fyrir hluta E og F eru stilltar þannig að línugerðin sé Phantom. Á mynd 4 er (a) uppskrift fyrir vöru G og (b) er leiðarblað fyrir vöru G.

![Mynd 4: Framleiðsluuppskriftarhluti G.](media/product-G-route-sheet-G.png)
*Mynd 4: Framleiðsluuppskriftarhluti G*

## <a name="phantom-and-route-network"></a>Skugga- og leiðanet

Einnig er hægt að nota skuggauppskriftir fyrir uppskrift sem hefur leiðanet. Í leiðaneti eru ein eða fleiri aðgerðir keyrðar samhliða. Mynd 5 sýnir dæmi um leiðanet sem er notað í fjölþrepa uppskrift. Á mynd 5 er (a) uppskrift fyrir vöru G og hluta F, og (b) er leiðarblað fyrir vöru G og hluta F, sem hefur leiðanet.

![Mynd 5: Verkfræðiuppskrift hluti G, leiðakerfi.](media/product-G-part-F.png)
*Mynd 5: Verkfræðiuppskrift hluti G, leiðakerfi*

Á mynd 6 er (a) uppskrift fyrir vöru G og hluta F, og (b) er leiðarblað fyrir vöru G og hluta F.

![Mynd 6: Framleiðsla BOM hluti G, leiðakerfi.](media/product-G-part-F-with-route-sheet.png)
*Mynd 6: Framleiðsla BOM hluti G, leiðakerfi*


[!INCLUDE[footer-include](../../includes/footer-banner.md)]