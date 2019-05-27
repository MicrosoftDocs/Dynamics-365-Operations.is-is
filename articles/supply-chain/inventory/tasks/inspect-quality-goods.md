---
title: Kanna vörugæði
description: Þessi ferli sýnir hvernig meðhöndla á gæðapöntun.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9e9d750f116db62519ac7148f19bf62050430e9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545406"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="305a8-103">Kanna vörugæði</span><span class="sxs-lookup"><span data-stu-id="305a8-103">Inspect the quality of goods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="305a8-104">Þessi ferli sýnir hvernig meðhöndla á gæðapöntun.</span><span class="sxs-lookup"><span data-stu-id="305a8-104">This procedure shows you how to process a quality order.</span></span> <span data-ttu-id="305a8-105">Hægt er að keyra þessari handbók sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="305a8-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="305a8-106">Áður en byrjað er á þessu dæmaferli, þarf að staðfesta innkaupapöntun "000016" og bóka innhreyfingarskjal afurða.</span><span class="sxs-lookup"><span data-stu-id="305a8-106">Before you start this example procedure, you need to confirm purchase order “000016” and post a product receipt.</span></span> <span data-ttu-id="305a8-107">Þetta stofna sjálfkrafa gæðapöntun.</span><span class="sxs-lookup"><span data-stu-id="305a8-107">This will automatically create a quality order.</span></span> <span data-ttu-id="305a8-108">Gæðaeftirlit eru yfirleitt framkvæmd með því að starfsmaður á sviði gæða.</span><span class="sxs-lookup"><span data-stu-id="305a8-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="305a8-109">Velja gæðapöntun.</span><span class="sxs-lookup"><span data-stu-id="305a8-109">Select a quality order</span></span>
1. <span data-ttu-id="305a8-110">Fara í birgðastjórnun > Reglubundin verkefni >gæðastjórnun > Gæðapantanir.</span><span class="sxs-lookup"><span data-stu-id="305a8-110">Go to Inventory management > Periodic tasks > Quality management > Quality orders.</span></span>
2. <span data-ttu-id="305a8-111">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="305a8-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="305a8-112">Veljið gæðapöntun var stofnuð áður en þetta ferli er hafið.</span><span class="sxs-lookup"><span data-stu-id="305a8-112">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="305a8-113">Skrá niðurstöðu prófunar</span><span class="sxs-lookup"><span data-stu-id="305a8-113">Record test results</span></span>
1. <span data-ttu-id="305a8-114">Smelltu á Niðurstöður.</span><span class="sxs-lookup"><span data-stu-id="305a8-114">Click Results.</span></span>
2. <span data-ttu-id="305a8-115">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="305a8-115">Click Edit.</span></span>
3. <span data-ttu-id="305a8-116">Í reitnum niðurstöðumagn skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="305a8-116">In the Result quantity field, enter a number.</span></span>
4. <span data-ttu-id="305a8-117">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="305a8-117">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="305a8-118">Í reitnum niðurstaða skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="305a8-118">In the Outcome field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="305a8-119">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="305a8-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="305a8-120">Í þessu dæmi niðurstaðan er byggt á fyrirframskilgreindu útkomu.</span><span class="sxs-lookup"><span data-stu-id="305a8-120">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="305a8-121">Vanalega væri skráð nákvæmari niðurstöður prófana, til dæmis stærð eða öðrum vídd.</span><span class="sxs-lookup"><span data-stu-id="305a8-121">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
7. <span data-ttu-id="305a8-122">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="305a8-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="305a8-123">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="305a8-123">Click Save.</span></span>
9. <span data-ttu-id="305a8-124">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="305a8-124">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="305a8-125">Villuprófa gæðapöntunina</span><span class="sxs-lookup"><span data-stu-id="305a8-125">Validate the quality order</span></span>
1. <span data-ttu-id="305a8-126">Smella á Villuleita.</span><span class="sxs-lookup"><span data-stu-id="305a8-126">Click Validate.</span></span>
2. <span data-ttu-id="305a8-127">Í reitnum Samþykkt af skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="305a8-127">In the Validated by field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="305a8-128">Veljið notanda sem framkvæma skoðun.</span><span class="sxs-lookup"><span data-stu-id="305a8-128">Select the user performing the inspection.</span></span>  
3. <span data-ttu-id="305a8-129">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="305a8-129">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="305a8-130">Smellið á Velja.</span><span class="sxs-lookup"><span data-stu-id="305a8-130">Click Select.</span></span>
5. <span data-ttu-id="305a8-131">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="305a8-131">Click OK.</span></span>
6. <span data-ttu-id="305a8-132">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="305a8-132">Close the page.</span></span>

