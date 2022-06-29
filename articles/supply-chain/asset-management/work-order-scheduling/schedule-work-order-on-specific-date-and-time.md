---
title: Áætla verkbeiðni á ákveðnum degi og tíma
description: Þessi grein útskýrir hvernig á að skipuleggja verkbeiðni á tiltekinni dagsetningu og tíma í eignastýringu.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e25d1c108e5cc90fcedc7e8f7e4bbc14052719f1
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015957"
---
# <a name="schedule-work-order-on-specific-date-and-time"></a>Áætla verkbeiðni á ákveðnum degi og tíma

[!include [banner](../../includes/banner.md)]

 

Ef þarf að skipuleggja verkbeiðni á tilteknum degi *og* tíma er hægt að hnekkja stöðluðu skipulagningarferli í Eignastjórnun og búa til tiltekna áætlun fyrir verkbeiðni.

1. Smellur **Eignastýring** > **Verkbeiðnir** > **Allar vinnupantanir** eða **Virkar vinnupantanir**.

2. Í verkbeiðnilistanum skaltu smella á verkbeiðnikennið í dálkinum **Verkbeiðni**.

3. Smellið á **Breyta**.

4. Á flýtiflipanum **Haus verkbeiðni** skaltu setja upphafs- og lokadagsetningar og tíma í reitina **Vænt upphaf** og **Vænt lok**.

    ![Mynd 1.](media/05-work-order-scheduling.png)

5. Á flipanum **Almennt** skaltu smella á **Tímasetja** til að nota staðlað tímasetningarferli eða smella á **Senda** ef þú vilt úthluta verkbeiðni til ákveðins starfsmanns.

6. Til að hnekkja fyrirliggjandi frátekna afkastagetu til að tryggja að verkbeiðni sé áætluð á væntu tímabili skaltu gera valið eins og sýnt er á myndinni hér að neðan í glugganum **Skipuleggja verkbeiðni** > kaflanum **Takmörkuð geta**. Þetta þýðir að tímasetningarferlið mun hunsa núverandi frátekna afkastagetu þar sem verkbeiðnin verður að hefjast á áætluðum upphafstíma.

    ![Mynd 2.](media/06-work-order-scheduling.png)

7. Smelltu á **Í lagi** til að hefja röðunina.

8. Ef tímasetningarferlið hefur í för með sér tvöfaldar bókanir sérðu skilaboð á skjánum og þú getur breytt tengdum verkbeiðnum.

>[!NOTE]
>Til þess að tímasetja viðhaldsstarfsmann fyrir verkbeiðnina verður sá viðhaldsstarfsmaður að vera tiltækur á væntum upphafsdegi og -tíma. Framboð starfskrafta er sett upp í [starfsmannadagatal](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md). 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]