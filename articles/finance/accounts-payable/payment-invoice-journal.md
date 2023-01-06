---
title: Jafna greiðsluáætlun við reikningabók
description: Þessi grein lýsir því hvernig á að bæta greiðslu við reikningabók lánardrottins.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863131"
---
# <a name="apply-a-payment-schedule-to-the-invoice-journal"></a>Jafna greiðsluáætlun við reikningabók

[!include [banner](../includes/preview-banner.md)]

Í Microsoft Dynamics 365 Finance-útgáfu 10.0.25 er greiðsluáætlun nú studd í **Reikningabók lánardrottins**.

Til að nota þessa virkni þarf að virkja eiginleikann **Nota greiðsluáætlun í reikningabók** í eiginleikastjórnun.

Þegar eiginleikinn hefur verið virkjaður er nýjum reit fyrir **Greiðsluáætlun** bætt við síðuna **Reikningabók**. Þegar lína reikningabókar er stofnuð, ef greiðsluskilmálum er haldið við í lánardrottni og greiðsluskilmálar eru valdir í greiðsluáætluninni, er reiturinn **Greiðsluáætlun** uppfærður á síðunni **Reikningabók**.

Þú getur breytt greiðsluáætluninni sem er notuð í samræmi við viðskiptakröfu þína. Við bókun reikningabókar lánardrottins verða opnar færslur lánardrottins stofnaðar samkvæmt greiðsluáætluninni.

 - Til að fara yfir margar opnar færslur lánardrottins sem voru stofnaðar úr greiðsluáætluninni skal fara í **Viðskiptaskuldir \> Reikningar \> Opna lánardrottnareikninga** og færa inn númer reiknings eða lánardrottnalykils.
 - Til að fara yfir eða skilgreina greiðsluáætlunina skal fara í **Viðskiptaskuldir \> Greiðsluuppsetning \> Greiðsluáætlun**.
 - Til að skilgreina greiðsluskilmálana og úthluta greiðsluáætlun skal fara í **Viðskiptaskuldir \> Greiðsluuppsetning \> Greiðsluskilmálar**.
 - Til að viðhalda greiðsluskilmálum í lánardrottni skal fara í **Viðskiptaskuldir \> Allir lánardrottnar**, velja lánardrottnalykilinn og síðan í flipanum **Greiðsla** skal stilla reitinn **Greiðsluskilmálar**.

Eiginleiki greiðsluáætlunar er einnig í boði í ferlinu **Komubók lánardrottins**. Ef greiðsluáætlun er valin í komubókinni verða margar greiðslulínur lánardrottins **ekki** búnar til þegar komubókin er bókuð. Greiðslulínur lánardrottins verða útbúnar eftir að reikningurinn hefur verið samþykktur.

## <a name="limitation"></a>Takmörkun

Fyrir lánardrottnareikning í bið, ef greiðsluáætlunin er í reikningshausnum, er ítarleg síða sem gerir notendum kleift að breyta greiðslulínunum. (Notendur geta til dæmis breytt gjalddaga og gildi fyrir hverja greiðslulínu.) Greiðslulínur sem eru búnar til úr reikningabókinni munu fá gildið úr greiðsluáætluninni.

Þessi virkni verður tiltæk fyrir **Reikningabók lánardrottins** og **Biðreikninga** í útgáfu í framtíðinni.
