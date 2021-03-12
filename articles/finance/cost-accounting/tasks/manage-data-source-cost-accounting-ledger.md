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
ms.search.form: CAMAXGeneralLedgerEntryProviderConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7246d42b42404f0f1215bbf14b8ad168fe12691c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990718"
---
# <a name="manage-a-data-source-for-the-cost-accounting-ledger"></a><span data-ttu-id="9e5ce-103">Stjórna gagnagjafa fyrir fjárhag kostnaðarbókhalds</span><span class="sxs-lookup"><span data-stu-id="9e5ce-103">Manage a data source for the cost accounting ledger</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9e5ce-104">Nota þetta ferli til að stýra gagnaveitu fjárhags fyrir kostnaðarbókhald fjárhags.</span><span class="sxs-lookup"><span data-stu-id="9e5ce-104">Use this procedure to manage the general ledger data source for a cost accounting ledger.</span></span> <span data-ttu-id="9e5ce-105">Áður en þú lýkur þessum verkhluta skaltu vera viss um að spila verkefnaleiðbeiningarnar „Stofna kostnaðarbókhald fjárhags“ og „Skilgreina kostnaðarstýringareiningar“.</span><span class="sxs-lookup"><span data-stu-id="9e5ce-105">Before you complete this task, make sure that you play the "Create a cost accounting ledger" and "Define cost control units" task guides.</span></span> <span data-ttu-id="9e5ce-106">Þessi skráning notar USP2-sýnigagnafyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="9e5ce-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="9e5ce-107">Fara í Kostnaðarbókhald > Fjárhags uppsetning > Kostnaðarbókhald fjárhags.</span><span class="sxs-lookup"><span data-stu-id="9e5ce-107">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="9e5ce-108">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="9e5ce-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9e5ce-109">Smellt er á Raunverulegar útgáfur.</span><span class="sxs-lookup"><span data-stu-id="9e5ce-109">Click Actual versions.</span></span>
4. <span data-ttu-id="9e5ce-110">Í Aðgerðarrúðunni er smellt á Stjórna.</span><span class="sxs-lookup"><span data-stu-id="9e5ce-110">On the Action Pane, click Manage.</span></span>
5. <span data-ttu-id="9e5ce-111">Smella á Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="9e5ce-111">Click General ledger.</span></span>
6. <span data-ttu-id="9e5ce-112">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="9e5ce-112">Click New.</span></span>
7. <span data-ttu-id="9e5ce-113">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9e5ce-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="9e5ce-114">Í reitinn Gagnaveita skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="9e5ce-114">In the Data provider field, enter or select a value.</span></span>
    * <span data-ttu-id="9e5ce-115">Í þessu dæmi skal velja Dynamics 365 Finance - Fjárhagsfærslur.</span><span class="sxs-lookup"><span data-stu-id="9e5ce-115">For this example, select Dynamics 365 Finance - General ledger entries.</span></span>  
9. <span data-ttu-id="9e5ce-116">Sláið inn eða veljið gildi í reitnum Vídd kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="9e5ce-116">In the Cost element dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="9e5ce-117">Í þessu dæmi skal velja kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="9e5ce-117">For this example, select Cost elements.</span></span>  
10. <span data-ttu-id="9e5ce-118">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="9e5ce-118">Click Save.</span></span>
11. <span data-ttu-id="9e5ce-119">Smella á Skilgreina gagnaveitu</span><span class="sxs-lookup"><span data-stu-id="9e5ce-119">Click Configure data provider.</span></span>
12. <span data-ttu-id="9e5ce-120">Í svæði Lögaðili skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="9e5ce-120">In the Legal entity field, enter or select a value.</span></span>
    * <span data-ttu-id="9e5ce-121">Í þessu dæmi skal velja USP2.</span><span class="sxs-lookup"><span data-stu-id="9e5ce-121">For this example, select USP2.</span></span>  
13. <span data-ttu-id="9e5ce-122">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="9e5ce-122">Click New.</span></span>
14. <span data-ttu-id="9e5ce-123">Í svæðið Bókunarlag skal velja Núgildandi.</span><span class="sxs-lookup"><span data-stu-id="9e5ce-123">In the Posting layer field, select Current.</span></span>
15. <span data-ttu-id="9e5ce-124">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9e5ce-124">Click OK.</span></span>

