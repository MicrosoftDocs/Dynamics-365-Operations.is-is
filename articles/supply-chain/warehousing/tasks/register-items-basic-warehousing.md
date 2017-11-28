--- 
title: "Skrá vörur fyrir vöru með grunnvöruhúsakerfi virkt með því að nota komubók"
description: "Þessi verklýsing sýnir hvernig á að skrá vörur með því að nota vörukomubókina þegar verið er að nota \"grunnur vöruhús\" í kerfinu birgðastjórnun."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 809a1466b0f4674f503bc654175d8f94b37a6508
ms.openlocfilehash: c7148bd807ef29b0dd89204a0fbe9b8480095aba
ms.contentlocale: is-is
ms.lasthandoff: 11/02/2017

---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-arrival-journal"></a>Skrá vörur fyrir vöru með grunnvöruhúsakerfi virkt með því að nota komubók

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að skrá vörur með því að nota vörukomubókina þegar verið er að nota "grunnur vöruhús" í kerfinu birgðastjórnun. Þetta væri yfirleitt gert með af móttöku starfsmaður. Hægt er að keyra þetta ferli með sýnigögn fyrirtækisins USMF með dæmagildin sem eru sýndar.  Ef þú ert ekki að nota USMF, þarf að hafa staðfest innkaupapöntun með opna innkaupapöntunarlínu áður en byrjað er að þessari handbók. Vara í línu verður að vera í birgðum og því verður að nota afurðarafbrigði og má ekki hafa rakningarvíddir. Og varan þarf að tengjast geymsluvíddaflokk, þar sem svæða og vöruhúsa eru virk.


## <a name="create-item-arrival-journal-header"></a>Stofna haus fyrir vörukomubók
1. Fara í birgðastjórnun > Færslubókarfærslur > Vörukoma > Vörukoma.
2. Smellið á „Nýtt“.
3. Í reitinn Heiti skal slá inn gildi.
    * Ef verið er að nota USMF, er hægt að færa inn vöruhúsakerfi. Ef verið er að nota önnur gögn, verður heiti færslubókar þú hefur valið að hafa eftirfarandi eiginleika: Athuga tiltektarstaðsetningu verður að vera stillt á Nei og biðgeymslustjórnun verður að vera stillt á nei.  
4. Í reitinn fylgiseðill skal slá inn gildi.
    * Þetta er Kenni fylgiseðils af fylgiseðli sem er gefið út af lánardrottni. Bæta við einkvæmt númer.  
5. Veljið innkaupapöntun í númerareitnum.
6. Smellið á „Í lagi“.

## <a name="add-lines-to-item-arrival-journal"></a>Bæta línum við vörukomubók
1. Smellið á Aðgerðir.
2. Smellið á Stofna línur .
    * Línur getur verið fært handvirkt inn í þessa færslubók eða sjálfkrafa stofnuð. Þetta sýnir hvernig á að stofna það sjálfkrafa.  
3. Merkja eða afmerkja gátreit Frumstilla magn.
    * Þetta mun frumstilla magn á færslubókarlínum með magn ekki skráð úr innkaupapöntunarlínunni.  
4. Smellið á „Í lagi“.

## <a name="post-the-journal"></a>Bóka færslubókina
1. Smellið á „Bóka“.
2. Smellið á „Í lagi“.

## <a name="generate-the-product-receipt"></a>Mynda innhreyfingarskjal afurða
1. Smellið á Aðgerðir.
2. Smellið á „Innhreyfingarskjal“.
3. Smellið á „Í lagi“.


