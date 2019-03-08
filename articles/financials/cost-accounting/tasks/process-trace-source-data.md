---
title: Vinna úr og rekja upprunagögn
description: Öll gagnavinnsla er keyrð af verkum.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e476416420875ba0f2401cf251d34977ae84b8f5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "322606"
---
# <a name="process-and-trace-source-data"></a><span data-ttu-id="e37ee-103">Vinna úr og rekja upprunagögn</span><span class="sxs-lookup"><span data-stu-id="e37ee-103">Process and trace source data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e37ee-104">Öll gagnavinnsla er keyrð af verkum.</span><span class="sxs-lookup"><span data-stu-id="e37ee-104">All data processing is run by jobs.</span></span> <span data-ttu-id="e37ee-105">Fyrir hvert verk og gagnaveitu er stofnuð færslubók til að skrá að ferlið hafi verið keyrt, og að færslurnar hafi verið unnar í núgildandi verki.</span><span class="sxs-lookup"><span data-stu-id="e37ee-105">For each job and data provider, a journal is created to document that the process has been run, and that the entries were processed in the current job.</span></span> <span data-ttu-id="e37ee-106">Nota þetta ferli til að setja upp gagnaforða og svo rekja uppruna tilgreindrar kostnaðarfærslu.</span><span class="sxs-lookup"><span data-stu-id="e37ee-106">Use this procedure to set up a data source and then  trace the origin of a specific cost entry.</span></span> <span data-ttu-id="e37ee-107">Þessi skráning notar USP2 sýnigagnafyrirtækið USP2.</span><span class="sxs-lookup"><span data-stu-id="e37ee-107">This recording uses the USP2 demo data company USP2.</span></span> <span data-ttu-id="e37ee-108">Áður en þú lýkur þessum verkhluta skaltu vera viss um að spila eftifarandi verkefnaleiðbeiningar „Stofna kostnaðarbókhald fjárhags“, „Skilgreina kostnaðarstýringareiningar“ og „Stjórna gagnaforða fyrir kostnaðarbókhald fjárhags“.</span><span class="sxs-lookup"><span data-stu-id="e37ee-108">Before you complete this task, make sure that you play the following task guides: "Create a cost accounting ledger," "Define cost control units," and "Manage data source for the cost accounting ledger."</span></span>

1. <span data-ttu-id="e37ee-109">Fara í Kostnaðarbókhald > Fjárhags uppsetning > Kostnaðarbókhald fjárhags.</span><span class="sxs-lookup"><span data-stu-id="e37ee-109">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="e37ee-110">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="e37ee-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e37ee-111">Velja kostnaðarbókhald fjárhagur sem búið var til áður.</span><span class="sxs-lookup"><span data-stu-id="e37ee-111">Select the cost accounting ledger that you created earlier.</span></span>  
3. <span data-ttu-id="e37ee-112">Smellt er á Raunverulegar útgáfur.</span><span class="sxs-lookup"><span data-stu-id="e37ee-112">Click Actual versions.</span></span>
4. <span data-ttu-id="e37ee-113">Í Aðgerðarúðunni er smellt á Upprunagögn vinnsla.</span><span class="sxs-lookup"><span data-stu-id="e37ee-113">On the Action Pane, click Source data processing.</span></span>
5. <span data-ttu-id="e37ee-114">Smella á Fjárhagsfærsla flutningabóka</span><span class="sxs-lookup"><span data-stu-id="e37ee-114">Click General ledger entry transfer journals.</span></span>
6. <span data-ttu-id="e37ee-115">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="e37ee-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="e37ee-116">Smellt er á Færslubókarfærslur.</span><span class="sxs-lookup"><span data-stu-id="e37ee-116">Click Journal entries.</span></span>
8. <span data-ttu-id="e37ee-117">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="e37ee-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="e37ee-118">Smellt er á kostnaðarfærslur.</span><span class="sxs-lookup"><span data-stu-id="e37ee-118">Click Cost entries.</span></span>
10. <span data-ttu-id="e37ee-119">Smellt er á Upprunafærslur.</span><span class="sxs-lookup"><span data-stu-id="e37ee-119">Click Source entry.</span></span>
11. <span data-ttu-id="e37ee-120">Í Aðgerðarúðunni er smellt á Upprunagögn vinnsla.</span><span class="sxs-lookup"><span data-stu-id="e37ee-120">On the Action Pane, click Source data processing.</span></span>
12. <span data-ttu-id="e37ee-121">Smella á Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="e37ee-121">Click General ledger.</span></span>
13. <span data-ttu-id="e37ee-122">Sláið inn eða veldu gildi í reitnum Fjárhagsdagatal tímabil.</span><span class="sxs-lookup"><span data-stu-id="e37ee-122">In the Fiscal calendar period field, enter or select a value.</span></span>
    * <span data-ttu-id="e37ee-123">Í þessu dæmi, velja Fjárhags 2017 Tímabil 9.</span><span class="sxs-lookup"><span data-stu-id="e37ee-123">For this example, select Fiscal 2017 Period 9.</span></span>  
14. <span data-ttu-id="e37ee-124">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e37ee-124">Click OK.</span></span>

