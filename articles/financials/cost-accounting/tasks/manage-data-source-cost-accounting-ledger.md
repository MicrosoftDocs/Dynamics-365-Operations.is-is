---
title: Stjórna gagnagjafa fyrir fjárhag kostnaðarbókhalds
description: Nota þetta ferli til að stýra gagnaveitu fjárhags fyrir kostnaðarbókhald fjárhags.
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
ms.openlocfilehash: f53101d73bc69199fafb00de0fa1759d59ea4ce8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543653"
---
# <a name="manage-a-data-source-for-the-cost-accounting-ledger"></a><span data-ttu-id="59f41-103">Stjórna gagnagjafa fyrir fjárhag kostnaðarbókhalds</span><span class="sxs-lookup"><span data-stu-id="59f41-103">Manage a data source for the cost accounting ledger</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="59f41-104">Nota þetta ferli til að stýra gagnaveitu fjárhags fyrir kostnaðarbókhald fjárhags.</span><span class="sxs-lookup"><span data-stu-id="59f41-104">Use this procedure to manage the general ledger data source for a cost accounting ledger.</span></span> <span data-ttu-id="59f41-105">Áður en þú lýkur þessum verkhluta skaltu vera viss um að spila verkefnaleiðbeiningarnar „Stofna kostnaðarbókhald fjárhags“ og „Skilgreina kostnaðarstýringareiningar“.</span><span class="sxs-lookup"><span data-stu-id="59f41-105">Before you complete this task, make sure that you play the "Create a cost accounting ledger" and "Define cost control units" task guides.</span></span> <span data-ttu-id="59f41-106">Þessi skráning notar USP2-sýnigagnafyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="59f41-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="59f41-107">Fara í Kostnaðarbókhald > Fjárhags uppsetning > Kostnaðarbókhald fjárhags.</span><span class="sxs-lookup"><span data-stu-id="59f41-107">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="59f41-108">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="59f41-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="59f41-109">Smellt er á Raunverulegar útgáfur.</span><span class="sxs-lookup"><span data-stu-id="59f41-109">Click Actual versions.</span></span>
4. <span data-ttu-id="59f41-110">Í Aðgerðarrúðunni er smellt á Stjórna.</span><span class="sxs-lookup"><span data-stu-id="59f41-110">On the Action Pane, click Manage.</span></span>
5. <span data-ttu-id="59f41-111">Smella á Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="59f41-111">Click General ledger.</span></span>
6. <span data-ttu-id="59f41-112">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="59f41-112">Click New.</span></span>
7. <span data-ttu-id="59f41-113">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="59f41-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="59f41-114">Í reitinn Gagnaveita skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="59f41-114">In the Data provider field, enter or select a value.</span></span>
    * <span data-ttu-id="59f41-115">Í þessu dæmi skal velja Dynamics 365 for Finance and Operations - Fjárhagsfærslur.</span><span class="sxs-lookup"><span data-stu-id="59f41-115">For this example, select Dynamics 365 for Finance and Operations - General ledger entries.</span></span>  
9. <span data-ttu-id="59f41-116">Sláið inn eða veljið gildi í reitnum Vídd kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="59f41-116">In the Cost element dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="59f41-117">Í þessu dæmi skal velja kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="59f41-117">For this example, select Cost elements.</span></span>  
10. <span data-ttu-id="59f41-118">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="59f41-118">Click Save.</span></span>
11. <span data-ttu-id="59f41-119">Smella á Skilgreina gagnaveitu</span><span class="sxs-lookup"><span data-stu-id="59f41-119">Click Configure data provider.</span></span>
12. <span data-ttu-id="59f41-120">Í svæði Lögaðili skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="59f41-120">In the Legal entity field, enter or select a value.</span></span>
    * <span data-ttu-id="59f41-121">Í þessu dæmi skal velja USP2.</span><span class="sxs-lookup"><span data-stu-id="59f41-121">For this example, select USP2.</span></span>  
13. <span data-ttu-id="59f41-122">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="59f41-122">Click New.</span></span>
14. <span data-ttu-id="59f41-123">Í svæðið Bókunarlag skal velja Núgildandi.</span><span class="sxs-lookup"><span data-stu-id="59f41-123">In the Posting layer field, select Current.</span></span>
15. <span data-ttu-id="59f41-124">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="59f41-124">Click OK.</span></span>

