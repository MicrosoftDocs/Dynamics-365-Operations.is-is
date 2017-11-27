---
title: "Stofna fjárhagsáætlun úr færslulyklum og samtölulyklum"
description: "Þessi grein gefur yfirlit yfir ferli þess að búa til fjárhagsáætlanir á grunni heildarreikninga. Hún útskýrir einnig hvernig skuli kveikja á fjárhagsáætlunarstýringu fyrir heildarreikninga, ef fjárhagsáætlunarstýringar er krafist."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3e3c86bd32a05a392fcb82a86f2c461cc3abfb03
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a>Stofna fjárhagsáætlun úr færslulyklum og samtölulyklum

[!include[banner](../includes/banner.md)]


Þessi grein gefur yfirlit yfir ferli þess að búa til fjárhagsáætlanir á grunni heildarreikninga. Hún útskýrir einnig hvernig skuli kveikja á fjárhagsáætlunarstýringu fyrir heildarreikninga, ef fjárhagsáætlunarstýringar er krafist.

Bæði fjárhagsáætlun og skjöl í fjárhagsáætlunarskrá leyfa fjárhagsáætlanagerð á aðallyklum sem hefur°tegund aðallykils°sem **Samtals**. Aðeins er hægt að bóka rauntölur í aðallykla færslur. 

Fyrir°reglubundnu vinnsluna **Mynda fjárhagsáætlun úr fjárhag** í flipanum **Uppruni** er hægt að tilgreina **Samtals** aðallykilgerð sem skilyrði. Í þessu tilfelli verður hver samtal aðallykils tekin með í°markfjárhagsáætlunina og°upphæðin jafngildir heildarupphæð á sviði°valinna°aðallykla. 

Hægt er að virkja°fjárhagsáætlunarstýringu fyrir aðallykla af gerðinni **Samtals**. Þessi virkni er studd gegnum notkun fjárhagsáætlunarflokka. Fyrir hvern samtals aðallykil verður fjárhagsáætlunin sem á að stýra fyrir flokk fjárhagsáætlana að vera stofnuð á **síðunni **Skilgreining fjárhagsáætlunarstýringar. Skilyrði sem er tilgreind verða að vera samtölur aðallykils og svið lykla. Til að hraða stofnun fjárhagsáætlunarflokka er hægt nýta Stýringu fjárhagsáætlunarflokka gagnaeiningar. 

Þegar fjárhagsáætlun er notuð í skýrslugerð, til dæmis í fjárhagsskýrslu, er samtala áætlunarinnar fyrir samtölulykilinn samsett úr eftirfarandi upphæðum:

-   Fjárhagsáætlanirnar sem eru stofnaðar úr hverjum færslufjárhagslykli innan bils samtölulykilsins.
-   Fjárhagsáætlunarupphæðin sem er færð beint inn á samtölulykilinn.

Þetta°gerir kleift að stofna aðskildar fjárhagsáætlanir fyrir mikilvægustu færslulyklana innan bilsins í samtölulyklinum og að bæta eftirstandandi upphæð fjárhagsáætlunar við samtölulykilinn.




