---
title: Mynda áætlun með skorðum
description: Þetta efni útskýrir hvernig á að stofna áætlun sen tekur tillit bæði til efnis- og afkastahamla.
author: ShylaThompson
manager: tfehr
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8cc44876938074e72526e75f0df5c119cbcfd845
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213424"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="c38fd-103">Mynda áætlun með skorðum</span><span class="sxs-lookup"><span data-stu-id="c38fd-103">Generate a constrained plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c38fd-104">Þetta efni útskýrir hvernig á að stofna áætlun sen tekur tillit bæði til efnis- og afkastahamla.</span><span class="sxs-lookup"><span data-stu-id="c38fd-104">This topic explains how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="c38fd-105">Áætlunin tryggir að framleiðslu hefst ekki fyrr en efni sé tiltækt og tilföng eru ekki yfirbókaður.</span><span class="sxs-lookup"><span data-stu-id="c38fd-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="c38fd-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="c38fd-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c38fd-107">Þetta ferli er ætluð fyrir framleiðslustjóri</span><span class="sxs-lookup"><span data-stu-id="c38fd-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="c38fd-108">Setja upp áætlun með skorðum</span><span class="sxs-lookup"><span data-stu-id="c38fd-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="c38fd-109">Á heimasíðunni velurðu vinnusvæðið **Aðaláætlanagerð**.</span><span class="sxs-lookup"><span data-stu-id="c38fd-109">In the home page, select the **Master planning** workspace.</span></span>
2. <span data-ttu-id="c38fd-110">Veldu **Aðaláætlanagerðir** á listanum yfir tengla lengst til hægri á vinnusvæðinu.</span><span class="sxs-lookup"><span data-stu-id="c38fd-110">Select **Master plans** in the list of links on the far right side of the workspace.</span></span>
3. <span data-ttu-id="c38fd-111">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="c38fd-111">In the list, find and select the desired record.</span></span> <span data-ttu-id="c38fd-112">Dæmi: **StaticPlan**</span><span class="sxs-lookup"><span data-stu-id="c38fd-112">Example: **StaticPlan**</span></span>  
4. <span data-ttu-id="c38fd-113">Veljið **Já** í reitnum **Takmörkuð geta**.</span><span class="sxs-lookup"><span data-stu-id="c38fd-113">Select **Yes** in the **Finite capacity** field.</span></span>
5. <span data-ttu-id="c38fd-114">Í reitnum **Tímamörk takmarkaðrar getu** skal slá inn `30`.</span><span class="sxs-lookup"><span data-stu-id="c38fd-114">In the **Finite capacity time fence** field, enter `30`.</span></span>
6. <span data-ttu-id="c38fd-115">Víkka út hlutann **Tímamörk í dögum**.</span><span class="sxs-lookup"><span data-stu-id="c38fd-115">Expand the **Time fences in days** section.</span></span>
7. <span data-ttu-id="c38fd-116">Veljið **Já** í reitnum **Afkastageta**.</span><span class="sxs-lookup"><span data-stu-id="c38fd-116">Select **Yes** in the **Capacity** field.</span></span>
8. <span data-ttu-id="c38fd-117">Í reitinn **Tímamörk áætlaðrar afkastagetu (dagar)** slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="c38fd-117">In the **Capacity scheduling time fence (days)** field, enter a number.</span></span> <span data-ttu-id="c38fd-118">Dæmi: `60`</span><span class="sxs-lookup"><span data-stu-id="c38fd-118">Example: `60`</span></span>  
9. <span data-ttu-id="c38fd-119">Veljið **Já** í reitnum **Reiknaðar seinkanir**.</span><span class="sxs-lookup"><span data-stu-id="c38fd-119">Select **Yes** in the **Calculated delays** field.</span></span>
10. <span data-ttu-id="c38fd-120">Í reitinn **Tímamörk útreiknaðra seinkana (dagar)** skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="c38fd-120">In the **Calculate delays time fence (days)** field, enter a number.</span></span> <span data-ttu-id="c38fd-121">Dæmi: `60`</span><span class="sxs-lookup"><span data-stu-id="c38fd-121">Example: `60`</span></span> 
11. <span data-ttu-id="c38fd-122">Útvíkkaðu hlutann **Reiknaðar seinkanir**.</span><span class="sxs-lookup"><span data-stu-id="c38fd-122">Expand the **Calculated delays** section.</span></span>
12. <span data-ttu-id="c38fd-123">Veldu **Já** í öllum reitum **Bæta við reiknaðri seinkun á dagsetningu þarfa**.</span><span class="sxs-lookup"><span data-stu-id="c38fd-123">Select **Yes** in all **Add the calculated delay to the requirement date** fields.</span></span>
13. <span data-ttu-id="c38fd-124">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c38fd-124">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="c38fd-125">Stofna áætlun með skorðum</span><span class="sxs-lookup"><span data-stu-id="c38fd-125">Create a constrained plan</span></span>
1. <span data-ttu-id="c38fd-126">Veljið **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="c38fd-126">Select **Run**.</span></span>
2. <span data-ttu-id="c38fd-127">Í reitinn **Aðaláætlun** slærðu inn eða velur áætlunina sem þú hefur sett upp skorður fyrir.</span><span class="sxs-lookup"><span data-stu-id="c38fd-127">In the **Master plan** field, enter or select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="c38fd-128">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="c38fd-128">Select **OK**.</span></span>
4. <span data-ttu-id="c38fd-129">Veldu **Tillögur**.</span><span class="sxs-lookup"><span data-stu-id="c38fd-129">Select **Planned orders**.</span></span>

