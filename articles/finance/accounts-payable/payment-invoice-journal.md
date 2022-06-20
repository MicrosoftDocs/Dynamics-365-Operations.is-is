---
title: Jafna greiðsluáætlun við reikningabók
description: Þessi grein lýsir því hvernig á að bæta greiðslu við reikningsbók lánardrottins.
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
ms.openlocfilehash: f3ae08ea46be66dd8bf26f7f91bd73f6c5b9192f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863131"
---
# <a name="apply-a-payment-schedule-to-the-invoice-journal"></a>Jafna greiðsluáætlun við reikningabók

[!include [banner](../includes/preview-banner.md)]

Í Microsoft Dynamics 365 Fjárhagsútgáfa 10.0.25, greiðsluáætlun er nú studd á **Reikningabók lánardrottins**.

Til að nota þessa virkni verður þú að virkja **Notaðu greiðsluáætlun á reikningabók** eiginleiki í Eiginleikastjórnun.

Eftir að eiginleikinn er virkjaður kemur nýr **Greiðsluáætlun** sviði er bætt við **Reikningardagbók** síðu. Þegar þú býrð til reikningsbókarlínu, ef greiðsluskilmálum er viðhaldið á lánardrottnum og greiðsluskilmálar eru valdir í greiðsluáætlun, **Greiðsluáætlun** reiturinn er uppfærður á **Reikningardagbók** síðu.

Þú getur breytt greiðsluáætluninni sem er notuð í samræmi við viðskiptaþörf þína. Við bókun reikningsbókar lánardrottins verða opnar færslur lánardrottins búnar til í samræmi við greiðsluáætlun.

 - Til að skoða margar opnar færslur lánardrottins sem voru búnar til úr greiðsluáætlun, farðu á **Viðskiptaskuldir \> Reikningar \> Opnir lánardrottnareikningar**, og sláðu inn reikningsnúmerið eða reikning lánardrottins.
 - Til að skoða eða stilla greiðsluáætlun, farðu á **Viðskiptaskuldir \> Uppsetning greiðslu \> Greiðsluáætlun**.
 - Til að stilla greiðsluskilmála og úthluta greiðsluáætlun, farðu á **Viðskiptaskuldir \> Uppsetning greiðslu \> Greiðsluskilmálar**.
 - Til að viðhalda greiðsluskilmálum lánardrottins, farðu á **Viðskiptaskuldir \> Allir söluaðilar**, veldu lánardrottinsreikninginn og síðan á **Greiðsla** flipann, stilltu **Greiðsluskilmálar** sviði.

Greiðsluáætlunaraðgerðin er einnig fáanleg í **Reikningaskrá söluaðila** ferli. Ef greiðsluáætlun er valin í reikningaskránni munu margar greiðslulínur lánardrottins **ekki** verða til þegar reikningaskrá er bókuð. Greiðslulínur lánardrottins verða búnar til þegar reikningurinn er samþykktur.

## <a name="limitation"></a>Takmörkun

Fyrir reikning lánardrottins í bið, ef greiðsluáætlun er á reikningshaus, er háþróuð síða sem gerir notendum kleift að breyta greiðslulínum. (Til dæmis geta notendur breytt gjalddaga og gildi fyrir hverja greiðslulínu.) Greiðslulínur sem eru búnar til úr reikningsbók munu hafa gildi frá greiðsluáætlun.

Þessi virkni verður í boði fyrir **Reikningabók lánardrottins** og **Reikningar í bið** í framtíðarútgáfu.
