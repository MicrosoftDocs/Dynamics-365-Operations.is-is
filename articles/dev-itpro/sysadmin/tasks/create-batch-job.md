---
title: Stofna runuvinnslu
description: Runuvinnsla er flokkur verka sem er sendur til AOS-tilviksins (hugbúnaðarhlutarþjónstilviks) í sjálfvirka vinnslu.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fbb844ebcf8d4b47b127132a5bf0ea45fa40f747
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "313360"
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

