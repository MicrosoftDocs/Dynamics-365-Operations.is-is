---
title: Skrá vörur fyrir virkjaðar vöru grunnvöruhúss með vörukomubók
description: Þessi verklýsing sýnir hvernig á að skrá vörur með því að nota vörukomubókina þegar verið er að nota „grunnur vöruhús” í kerfinu birgðastjórnun.
author: Mirzaab
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, WMSJournalTable, WMSJournalCreate, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76dd2bfd57db7dfd5c2baf59a864e59a509a64e0
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577793"
---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-an-item-arrival-journal"></a>Skrá vörur fyrir virkjaðar vöru grunnvöruhúss með vörukomubók

[!include [banner](../../includes/banner.md)]

Þessi verklýsing sýnir hvernig á að skrá vörur með því að nota vörukomubókina þegar verið er að nota „grunnur vöruhús” í kerfinu birgðastjórnun. Þetta væri yfirleitt gert með af móttöku starfsmaður. Hægt er að keyra þetta ferli með sýnigögn fyrirtækisins USMF með dæmagildin sem eru sýndar.  Ef þú ert ekki að nota USMF, þarf að hafa staðfest innkaupapöntun með opna innkaupapöntunarlínu áður en byrjað er að þessari handbók. Varan á línunni verðu að vera á lager. Og varan þarf að tengjast geymsluvíddaflokk, þar sem svæða og vöruhúsa eru virk.


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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]