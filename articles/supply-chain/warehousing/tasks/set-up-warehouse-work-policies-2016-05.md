--- 
title: "Setja upp vinnureglur vöruhúss (umsókn, maí 2016)"
description: "Ferli vöruhúsa ekki alltaf hafa vöruhús vinnu."
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorkPolicy, WMSLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 34b4255c85bb53f7e238b60559890571070953a6
ms.contentlocale: is-is
ms.lasthandoff: 10/16/2018

---
# <a name="set-up-warehouse-work-policies-application-may-2016"></a><span data-ttu-id="a0f2b-103">Setja upp vinnureglur vöruhúss (umsókn, maí 2016)</span><span class="sxs-lookup"><span data-stu-id="a0f2b-103">Set up warehouse work policies (Application, May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a0f2b-104">Ferli vöruhúsa ekki alltaf hafa vöruhús vinnu.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-104">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="a0f2b-105">Með því að skilgreina vinnustefnu, sem getur komið í veg fyrir stofnun vinnu fyrir tiltekt hráefnis og frágangur fullbúinna vara fyrir safn af afurðum á tiltekna staði.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-105">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="a0f2b-106">USMF sýniútgáfu fyrirtækis sem er notað til að stofna þessa skráningu.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-106">The USMF demo data company was used to create this recording.</span></span> <span data-ttu-id="a0f2b-107">Þessi leiðarvísi fyrir verk krefst Dynamics AX forritið 7.0.1 eða síðar.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>

1. <span data-ttu-id="a0f2b-108">Fara í vöruhúsakerfi > Uppsetning > Vinna > Vinnureglur.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-108">Go to Warehouse management > Setup > Work > Work policies.</span></span>
2. <span data-ttu-id="a0f2b-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-109">Click New.</span></span>
3. <span data-ttu-id="a0f2b-110">Í svæðið Vinnu reglu heiti, skrifa 'Engin frágangsvinna‘</span><span class="sxs-lookup"><span data-stu-id="a0f2b-110">In the Work policy name field, type 'No put-away work'.</span></span>
4. <span data-ttu-id="a0f2b-111">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-111">Click Save.</span></span>
5. <span data-ttu-id="a0f2b-112">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-112">Click Add.</span></span>
6. <span data-ttu-id="a0f2b-113">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-113">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="a0f2b-114">Í Gerð vinnupöntun svæðinu, veljið 'Fullunninna vöru frágangur'.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-114">In the Work order type field, select 'Finished goods put away'.</span></span>
8. <span data-ttu-id="a0f2b-115">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-115">Click Add.</span></span>
9. <span data-ttu-id="a0f2b-116">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-116">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="a0f2b-117">Í Gerð vinnupöntun svæðinu, veljið 'Aukaafurða og hliðarafurða frágangur'.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-117">In the Work order type field, select 'Co-product and by-product put away'.</span></span>
11. <span data-ttu-id="a0f2b-118">Útvíkka hlutann birgðastaðsetning.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-118">Expand the Inventory locations section.</span></span>
12. <span data-ttu-id="a0f2b-119">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-119">Click Add.</span></span>
13. <span data-ttu-id="a0f2b-120">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="a0f2b-121">Í vöruhúsalistanum, sláðu inn "51"</span><span class="sxs-lookup"><span data-stu-id="a0f2b-121">In the Warehouse list, enter '51'.</span></span>
15. <span data-ttu-id="a0f2b-122">Sláið inn eða veldu '001‘ í staðsetning reitnum.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-122">In the Location field, enter or select '001'.</span></span>
16. <span data-ttu-id="a0f2b-123">Víkka út hlutann Afurðir.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-123">Expand the Products section.</span></span>
17. <span data-ttu-id="a0f2b-124">Í reitnum afurðaval skal velja valið.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-124">In the Product selection field, select 'Selected'.</span></span>
18. <span data-ttu-id="a0f2b-125">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-125">Click Add.</span></span>
19. <span data-ttu-id="a0f2b-126">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-126">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="a0f2b-127">Í reitinn Vörunúmer skal slá inn eða veldu L0101.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-127">In the Item number field, enter or select 'L0101'.</span></span>
21. <span data-ttu-id="a0f2b-128">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-128">Click Save.</span></span>


