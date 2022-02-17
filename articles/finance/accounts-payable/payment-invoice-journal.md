---
title: Notaðu greiðsluáætlun á reikningsbókina
description: Þetta efnisatriði lýsir því hvernig á að bæta greiðslu við reikningsbók lánardrottins.
author: sunfzam
ms.date: 01/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: bd288ac48ef59d8e2a4e0922aa652276dddb666d
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075739"
---
# <a name="apply-a-payment-schedule-to-the-invoice-journal"></a>Notaðu greiðsluáætlun á reikningsbókina

[!include [banner](../includes/preview-banner.md)]

Í Microsoft Dynamics 365 Finance útgáfu 10.0.25, greiðsluáætlun er nú studd í reikningsbók lánardrottins.

Til að nota þessa virkni verður þú að virkja **Notaðu greiðsluáætlun á reikningabók** eiginleiki í Eiginleikastjórnun.

Eftir að eiginleikinn er virkjaður kemur nýr **Greiðsluáætlun** sviði er bætt við **Reikningardagbók** síðu. Þegar þú býrð til reikningsbókarlínu, ef greiðsluskilmálum er viðhaldið á lánardrottnum og greiðsluskilmálar eru valdir í greiðsluáætlun, **Greiðsluáætlun** reiturinn er uppfærður á **Reikningardagbók** síðu.

Þú getur breytt greiðsluáætluninni sem er notuð í samræmi við viðskiptaþörf þína. Við bókun reikningsbókar lánardrottins verða opnar færslur lánardrottins búnar til í samræmi við greiðsluáætlun.

Til að skoða margar opnar færslur lánardrottins sem voru búnar til úr greiðsluáætlun, farðu á **Viðskiptaskuldir \> Reikningar \> Opnir lánardrottnareikningar**, og sláðu inn reikningsnúmerið eða reikning lánardrottins.

Til að skoða eða stilla greiðsluáætlun, farðu á **Viðskiptaskuldir \> Uppsetning greiðslu \> Greiðsluáætlun**.

Til að stilla greiðsluskilmála og úthluta greiðsluáætlun, farðu á **Viðskiptaskuldir \> Uppsetning greiðslu \> Greiðsluskilmálar**.

Til að viðhalda greiðsluskilmálum lánardrottins, farðu á **Viðskiptaskuldir \> Allir söluaðilar**, veldu lánardrottinsreikninginn og síðan á **Greiðsla** flipann, stilltu **Greiðsluskilmálar** sviði.

Greiðsluáætlunaraðgerðin er einnig fáanleg í **Reikningaskrá söluaðila** ferli. Ef greiðsluáætlun er valin í reikningaskránni munu margar greiðslulínur lánardrottins **ekki** verða til þegar reikningaskrá er bókuð. Greiðslulínur lánardrottins verða búnar til þegar reikningurinn er samþykktur.

## <a name="limitation"></a>Takmörkun

Fyrir reikning lánardrottins í bið, ef greiðsluáætlun er á reikningshaus, er háþróuð síða sem gerir notendum kleift að breyta greiðslulínum. (Til dæmis geta notendur breytt gjalddaga og gildi fyrir hverja greiðslulínu.) Greiðslulínur sem eru búnar til úr reikningsbók munu hafa gildi frá greiðsluáætlun.

Þessi virkni verður tiltæk fyrir reikningabók lánardrottins og reikninga í bið í framtíðarútgáfu.
