---
title: Skýrslan „Óbeinn kostnaður í vinnslu“ inniheldur framleiðslupantanir sem var eytt
description: Óbeinn kostnaður í ferli skýrslan birtir upplýsingar um framleiðslupantanir sem voru unnin að hluta til og síðar eytt.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdIndirectCostInProgress
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 707fa9bb30129c3656e10c6756dee770a7712e65
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026610"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a><span data-ttu-id="9fb07-103">Skýrslan „Óbeinn kostnaður í vinnslu“ inniheldur framleiðslupantanir sem var eytt</span><span class="sxs-lookup"><span data-stu-id="9fb07-103">The Indirect costs in process report includes deleted production orders</span></span>

<span data-ttu-id="9fb07-104">KB númer: 4612748</span><span class="sxs-lookup"><span data-stu-id="9fb07-104">KB number: 4612748</span></span>

## <a name="symptoms"></a><span data-ttu-id="9fb07-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="9fb07-105">Symptoms</span></span>

<span data-ttu-id="9fb07-106">**Óbeinn kostnaður í ferli** skýrslan birtir upplýsingar um framleiðslupantanir sem voru unnin að hluta til og síðar eytt.</span><span class="sxs-lookup"><span data-stu-id="9fb07-106">The **Indirect costs in process** report presents information about production orders that were partially processed and later deleted.</span></span>

## <a name="resolution"></a><span data-ttu-id="9fb07-107">Upplausn</span><span class="sxs-lookup"><span data-stu-id="9fb07-107">Resolution</span></span>

<span data-ttu-id="9fb07-108">Þegar framleiðslupöntun er afturkölluð eru allar færslur framleiðslupöntunar einnig afturkallaðar.</span><span class="sxs-lookup"><span data-stu-id="9fb07-108">When you reverse a production order, you also reverse all the transactions of that production order.</span></span> <span data-ttu-id="9fb07-109">Þegar framleiðslupöntuninni er eytt eru allar töflur undirbókar og fjárhags áfram til staðar.</span><span class="sxs-lookup"><span data-stu-id="9fb07-109">When you delete the production order, the subledger tables and general ledger persist all transactions that are related to it.</span></span> <span data-ttu-id="9fb07-110">Skýrslurnar sýna færslurnar í töflum undirbókar.</span><span class="sxs-lookup"><span data-stu-id="9fb07-110">The reports will show the transactions in the subledger tables.</span></span> <span data-ttu-id="9fb07-111">Nettóverðmætið ætti að vera 0,00 fyrir tilteknu framleiðslupöntunina.</span><span class="sxs-lookup"><span data-stu-id="9fb07-111">For the specific production order, the net value should be 0.00.</span></span>
