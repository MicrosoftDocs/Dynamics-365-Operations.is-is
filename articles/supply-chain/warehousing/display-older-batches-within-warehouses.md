---
title: "Stilla skjá eldri keyrsla innan vöruhúss á fartæki"
description: "Þetta efnisatriði lýsir því hvernig eigi að setja upp fartæki svo það birti lista yfir staðsetningar með eldri runum en núverandi staðsetning á vinnulínu."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cd0a9c2e9fbfea987b045e301fb73a505a0f2a4e
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a>Stilla skjá eldri keyrsla innan vöruhúss á fartæki

[!include[banner](../includes/banner.md)]

Skilgreiningin **Birta eldri runur innan vöruhússins** gefur kost á að birta lista yfir staðsetningar með eldri runum en núverandi staðsetning á vinnulínunni. Listinn yfir staðsetningar sem eru birtar inniheldur upplýsingar um eldri runur á staðsetningunni með lokatíma og efnislegum birgðum hverrar runu. Hægt er að velja tiltekt frá nýrri staðsetningu eða að halda áfram tiltekt frá gildandi staðsetningu. 
- Tiltekt frá nýrri staðsetningu - Ef valin er ný staðsetning fyrir tiltekt verður núverandi vinnulína uppfærð til að nota nýju staðsetninguna og vinna heldur áfram sem fyrr með nýju staðsetningunni. Svo nýja staðsetningin sé gild verður hún að hafa nægt tiltækt magn fyrir alla vinnulínuna. Ef nauðsynlegt magn er ekki tiltækt verður vinnulínan ekki uppfærð og listinn birtist. 
- Halda áfram tiltekt frá núverandi staðsetningu - Ef haldið er áfram með gildandi staðsetningu vinnulínu heldur tiltekt á magni fyrir vinnulínuna áfram frá upphaflegri staðsetningu.

## <a name="where-it-applies"></a>Þar sem það á við
Birta eldri runur innan vöruhússins er grunnstillt í valmyndaratriðum fartækis og hefur áhrif á tiltekt á neðangreindum runum vara.

## <a name="set-up-display-older-batches-within-warehouse"></a>Setja upp Birta eldri runur innan vöruhúss
Stillingin **Birta eldri runur innan vöruhússins** er í boði í valmyndaratriðum fartækja þegar valkosturinn **Tína elstu runu** er stilltur á **Vara við**.

- Undir **Vöruhúsastjórnun** > **Uppsetning** > **Fartæki** > **Valmyndaratriði fartækis** stillirðu **Nota fyrirliggjandi verk** á **Já** fyrir valmyndaratriðið, og velur **Vara við** í reitnum **Tína elsta runu**. 


