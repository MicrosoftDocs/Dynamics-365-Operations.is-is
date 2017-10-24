--- 
title: "Setja upp vinnureglur vöruhúss "
description: "Ferli vöruhúsa ekki alltaf hafa vöruhús vinnu."
author: johanhoffmann
manager: AnnBe
ms.date: 06/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b7d579ca7e2b9ca8cbead74b2c2ababfd142f171
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-warehouse-work-policies"></a><span data-ttu-id="6d9c7-103">Setja upp vinnureglur vöruhúss </span><span class="sxs-lookup"><span data-stu-id="6d9c7-103">Set up warehouse work policies</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6d9c7-104">Ferli vöruhúsa ekki alltaf hafa vöruhús vinnu.</span><span class="sxs-lookup"><span data-stu-id="6d9c7-104">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="6d9c7-105">Með því að skilgreina vinnustefnu, sem getur komið í veg fyrir stofnun vinnu fyrir tiltekt hráefnis og frágangur fullbúinna vara fyrir safn af afurðum á tiltekna staði.</span><span class="sxs-lookup"><span data-stu-id="6d9c7-105">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="6d9c7-106">USMF sýniútgáfu fyrirtækis sem er notað til að stofna þessa skráningu.</span><span class="sxs-lookup"><span data-stu-id="6d9c7-106">The USMF demo data company was used to create this recording.</span></span> <span data-ttu-id="6d9c7-107">Þessi leiðarvísi fyrir verk krefst Dynamics AX forritið 7.0.1 eða síðar.</span><span class="sxs-lookup"><span data-stu-id="6d9c7-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>

1. <span data-ttu-id="6d9c7-108">Fara í vöruhúsakerfi > Uppsetning > Vinna > Vinnureglur.</span><span class="sxs-lookup"><span data-stu-id="6d9c7-108">Go to Warehouse management > Setup > Work > Work policies.</span></span>
2. <span data-ttu-id="6d9c7-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="6d9c7-109">Click New.</span></span>
3. <span data-ttu-id="6d9c7-110">Í svæðið Vinnu reglu heiti, skrifa 'Engin frágangsvinna‘</span><span class="sxs-lookup"><span data-stu-id="6d9c7-110">In the Work policy name field, type 'No put-away work'.</span></span>
4. <span data-ttu-id="6d9c7-111">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="6d9c7-111">Click Save.</span></span>
5. <span data-ttu-id="6d9c7-112">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="6d9c7-112">Click Add.</span></span>
6. <span data-ttu-id="6d9c7-113">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="6d9c7-113">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="6d9c7-114">Í Gerð vinnupöntun svæðinu, veljið 'Fullunninna vöru frágangur'.</span><span class="sxs-lookup"><span data-stu-id="6d9c7-114">In the Work order type field, select 'Finished goods put away'.</span></span>
8. <span data-ttu-id="6d9c7-115">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="6d9c7-115">Click Add.</span></span>
9. <span data-ttu-id="6d9c7-116">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="6d9c7-116">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="6d9c7-117">Í Gerð vinnupöntun svæðinu, veljið 'Aukaafurða og hliðarafurða frágangur'.</span><span class="sxs-lookup"><span data-stu-id="6d9c7-117">In the Work order type field, select 'Co-product and by-product put away'.</span></span>
11. <span data-ttu-id="6d9c7-118">Útvíkka hlutann birgðastaðsetning.</span><span class="sxs-lookup"><span data-stu-id="6d9c7-118">Expand the Inventory locations section.</span></span>
12. <span data-ttu-id="6d9c7-119">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="6d9c7-119">Click Add.</span></span>
13. <span data-ttu-id="6d9c7-120">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="6d9c7-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="6d9c7-121">Í vöruhúsalistanum, sláðu inn "51"</span><span class="sxs-lookup"><span data-stu-id="6d9c7-121">In the Warehouse list, enter '51'.</span></span>
15. <span data-ttu-id="6d9c7-122">Sláið inn eða veldu '001‘ í staðsetning reitnum.</span><span class="sxs-lookup"><span data-stu-id="6d9c7-122">In the Location field, enter or select '001'.</span></span>
16. <span data-ttu-id="6d9c7-123">Víkka út hlutann Afurðir.</span><span class="sxs-lookup"><span data-stu-id="6d9c7-123">Expand the Products section.</span></span>
17. <span data-ttu-id="6d9c7-124">Í reitnum afurðaval skal velja valið.</span><span class="sxs-lookup"><span data-stu-id="6d9c7-124">In the Product selection field, select 'Selected'.</span></span>
18. <span data-ttu-id="6d9c7-125">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="6d9c7-125">Click Add.</span></span>
19. <span data-ttu-id="6d9c7-126">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="6d9c7-126">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="6d9c7-127">Í reitinn Vörunúmer skal slá inn eða veldu L0101.</span><span class="sxs-lookup"><span data-stu-id="6d9c7-127">In the Item number field, enter or select 'L0101'.</span></span>
21. <span data-ttu-id="6d9c7-128">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="6d9c7-128">Click Save.</span></span>


