--- 
title: Stofna runuvinnslu
description: "Runuvinnsla er flokkur verka sem er sendur til AOS-tilviksins (hugbúnaðarhlutarþjónstilviks) í sjálfvirka vinnslu."
author: maertenm
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 31c8e2ba87ef8c17a3147e1159104585258d4164
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-batch-job"></a>Stofna runuvinnslu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Runuvinnsla er flokkur verka sem er sendur til AOS-tilviksins (hugbúnaðarhlutarþjónstilviks) í sjálfvirka vinnslu. Runuvinnslur er keyrðar með því að nota öryggis- og notendaheimildir þess notanda sem stofnaði verkið. Fylgið eftirfarandi ferli ef stofna á runuvinnslu. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.


## <a name="create-the-batch-job"></a>Stofna runuvinnslu
1. Farið í Kerfisstjórnun > Fyrirspurnir > Runuvinnslur.
2. Smellið á „Nýtt“.
3. Færa inn gildi í reitnum starfslýsing.
4. Færa inn dagsetningu og tíma í reitnum áætluð upphafsdagsetning og -tími.
5. Smellið á „Vista“.

## <a name="create-a-recurrence"></a>Stofna endurtekningu
1. Í aðgerðasvæðinu er smellt á runuvinnsla.
2. Smellið á Endurtekning.
    * Notið þessa valkosti til að færa inn afmörkun og mynstur fyrir endurtekninguna.  
3. Smellið á „Í lagi“.

## <a name="add-alerts"></a>Bæta við viðvaranir
1. Í aðgerðasvæðinu er smellt á runuvinnsla.
2. Smellt er á Viðvörunum.
    * Tilgreina hvort óskað sé eftir að viðvörunarboðin birtist þegar runuvinnsla lýkur, villa er til staðar eða hætt er við. Tilgreinið síðan ef óskað er eftir að viðvaranir birtist sem sprettigluggar.   
3. Smellið á „Í lagi“.


