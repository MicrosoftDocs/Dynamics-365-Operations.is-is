--- 
title: "Skrá vörur fyrir virkjaðar vöru grunnvöruhúss með vörukomubók"
description: "Þessi verklýsing sýnir hvernig á að skrá vörur með því að nota vörukomubókina þegar verið er að nota \"grunnur vöruhús\" í kerfinu birgðastjórnun."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder, WMSJournalTable, WMSJournalCreate, PurchEditLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 5c53a38eb6afdf8d3cc1a316c8da5e84549ab60d
ms.contentlocale: is-is
ms.lasthandoff: 10/16/2018

---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-an-item-arrival-journal"></a>Skrá vörur fyrir virkjaðar vöru grunnvöruhúss með vörukomubók

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að skrá vörur með því að nota vörukomubókina þegar verið er að nota "grunnur vöruhús" í kerfinu birgðastjórnun. Þetta væri yfirleitt gert með af móttöku starfsmaður. Hægt er að keyra þetta ferli með sýnigögn fyrirtækisins USMF með dæmagildin sem eru sýndar.  Ef þú ert ekki að nota USMF, þarf að hafa staðfest innkaupapöntun með opna innkaupapöntunarlínu áður en byrjað er að þessari handbók. Vara í línu verður að vera í birgðum og því verður að nota afurðarafbrigði og má ekki hafa rakningarvíddir. Og varan þarf að tengjast geymsluvíddaflokk, þar sem svæða og vöruhúsa eru virk.


## <a name="create-item-arrival-journal-header"></a>Stofna haus fyrir vörukomubók
1. Fara í birgðastjórnun > Færslubókarfærslur > Vörukoma > Vörukoma.
2. Smellið á „Nýtt“.
3. Í reitinn Heiti skal slá inn gildi.
    * Ef verið er að nota USMF, er hægt að færa inn vöruhúsakerfi. Ef verið er að nota önnur gögn, verður færslubókin sem þú velur heitið á að hafa eftirfarandi eiginleika: Athuga tiltektarstaðsetningu verður að vera stillt á Nei og biðgeymslustjórnun verður að vera stillt á Nei.  
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


