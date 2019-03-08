---
title: Setja upp vinnureglur vöruhúss (umsókn, maí 2016)
description: Ferli vöruhúsa ekki alltaf hafa vöruhús vinnu.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy, WMSLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 34b4255c85bb53f7e238b60559890571070953a6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "335325"
---
# <a name="set-up-warehouse-work-policies-application-may-2016"></a><span data-ttu-id="e2080-103">Setja upp vinnureglur vöruhúss (umsókn, maí 2016)</span><span class="sxs-lookup"><span data-stu-id="e2080-103">Set up warehouse work policies (Application, May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e2080-104">Ferli vöruhúsa ekki alltaf hafa vöruhús vinnu.</span><span class="sxs-lookup"><span data-stu-id="e2080-104">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="e2080-105">Með því að skilgreina vinnustefnu, sem getur komið í veg fyrir stofnun vinnu fyrir tiltekt hráefnis og frágangur fullbúinna vara fyrir safn af afurðum á tiltekna staði.</span><span class="sxs-lookup"><span data-stu-id="e2080-105">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="e2080-106">USMF sýniútgáfu fyrirtækis sem er notað til að stofna þessa skráningu.</span><span class="sxs-lookup"><span data-stu-id="e2080-106">The USMF demo data company was used to create this recording.</span></span> <span data-ttu-id="e2080-107">Þessi leiðarvísi fyrir verk krefst AX forrit 7.0.1 eða síðar.</span><span class="sxs-lookup"><span data-stu-id="e2080-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>

1. <span data-ttu-id="e2080-108">Fara í vöruhúsakerfi > Uppsetning > Vinna > Vinnureglur.</span><span class="sxs-lookup"><span data-stu-id="e2080-108">Go to Warehouse management > Setup > Work > Work policies.</span></span>
2. <span data-ttu-id="e2080-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="e2080-109">Click New.</span></span>
3. <span data-ttu-id="e2080-110">Í svæðið Vinnu reglu heiti, skrifa 'Engin frágangsvinna‘</span><span class="sxs-lookup"><span data-stu-id="e2080-110">In the Work policy name field, type 'No put-away work'.</span></span>
4. <span data-ttu-id="e2080-111">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e2080-111">Click Save.</span></span>
5. <span data-ttu-id="e2080-112">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="e2080-112">Click Add.</span></span>
6. <span data-ttu-id="e2080-113">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="e2080-113">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="e2080-114">Í Gerð vinnupöntun svæðinu, veljið 'Fullunninna vöru frágangur'.</span><span class="sxs-lookup"><span data-stu-id="e2080-114">In the Work order type field, select 'Finished goods put away'.</span></span>
8. <span data-ttu-id="e2080-115">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="e2080-115">Click Add.</span></span>
9. <span data-ttu-id="e2080-116">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="e2080-116">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="e2080-117">Í Gerð vinnupöntun svæðinu, veljið 'Aukaafurða og hliðarafurða frágangur'.</span><span class="sxs-lookup"><span data-stu-id="e2080-117">In the Work order type field, select 'Co-product and by-product put away'.</span></span>
11. <span data-ttu-id="e2080-118">Útvíkka hlutann birgðastaðsetning.</span><span class="sxs-lookup"><span data-stu-id="e2080-118">Expand the Inventory locations section.</span></span>
12. <span data-ttu-id="e2080-119">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="e2080-119">Click Add.</span></span>
13. <span data-ttu-id="e2080-120">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="e2080-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="e2080-121">Í vöruhúsalistanum, sláðu inn "51"</span><span class="sxs-lookup"><span data-stu-id="e2080-121">In the Warehouse list, enter '51'.</span></span>
15. <span data-ttu-id="e2080-122">Sláið inn eða veldu '001‘ í staðsetning reitnum.</span><span class="sxs-lookup"><span data-stu-id="e2080-122">In the Location field, enter or select '001'.</span></span>
16. <span data-ttu-id="e2080-123">Víkka út hlutann Afurðir.</span><span class="sxs-lookup"><span data-stu-id="e2080-123">Expand the Products section.</span></span>
17. <span data-ttu-id="e2080-124">Í reitnum afurðaval skal velja valið.</span><span class="sxs-lookup"><span data-stu-id="e2080-124">In the Product selection field, select 'Selected'.</span></span>
18. <span data-ttu-id="e2080-125">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="e2080-125">Click Add.</span></span>
19. <span data-ttu-id="e2080-126">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="e2080-126">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="e2080-127">Í reitinn Vörunúmer skal slá inn eða veldu L0101.</span><span class="sxs-lookup"><span data-stu-id="e2080-127">In the Item number field, enter or select 'L0101'.</span></span>
21. <span data-ttu-id="e2080-128">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e2080-128">Click Save.</span></span>

