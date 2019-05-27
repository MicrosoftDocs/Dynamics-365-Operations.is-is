---
title: Stofna sjálfgefna lífferilsstöðu afurðar
description: Þessi aðferð sýnir hvernig á að búa til sjálfgefna lífferilsstöðu afurðar sem og hvernig á að tengja sjálfgefna stöðu við útgefnar afurðir.
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6e7e637157ee06a3d07a1a9c5da71295eb75b424
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564179"
---
# <a name="create-a-default-product-lifecycle-state"></a><span data-ttu-id="cc3f7-103">Stofna sjálfgefna lífferilsstöðu afurðar</span><span class="sxs-lookup"><span data-stu-id="cc3f7-103">Create a default product lifecycle state</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cc3f7-104">Þessi aðferð sýnir hvernig á að búa til sjálfgefna lífferilsstöðu afurðar sem og hvernig á að tengja sjálfgefna stöðu við útgefnar afurðir.</span><span class="sxs-lookup"><span data-stu-id="cc3f7-104">This procedure shows how to create a default product lifecycle state as well as how to associate the default state with released products.</span></span>


## <a name="create-a-default-lifecycle-state"></a><span data-ttu-id="cc3f7-105">Stofna sjálfgefna lífferilsstöðu</span><span class="sxs-lookup"><span data-stu-id="cc3f7-105">Create a default lifecycle state</span></span>
1. <span data-ttu-id="cc3f7-106">Fara í Upplýsingastjórnun afurðar > Uppsetning > Lífferilsstaða afurðar.</span><span class="sxs-lookup"><span data-stu-id="cc3f7-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="cc3f7-107">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="cc3f7-107">Click New.</span></span>
3. <span data-ttu-id="cc3f7-108">Í reitinn Staða skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="cc3f7-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="cc3f7-109">Velja Já í reitnum Hvenær afhent lögaðila er sjálfgefið.</span><span class="sxs-lookup"><span data-stu-id="cc3f7-109">Select Yes in the Default when released to legal entity field.</span></span>
5. <span data-ttu-id="cc3f7-110">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="cc3f7-110">In the Description field, type a value.</span></span>
6. <span data-ttu-id="cc3f7-111">Velja skal Nei í reitinum Er virk fyrir áætlunargerð.</span><span class="sxs-lookup"><span data-stu-id="cc3f7-111">Select No in the Is active for planning field.</span></span>

> [!NOTE]
> <span data-ttu-id="cc3f7-112">Ef ný útgefin afurð á ekki að vera tekin með í aðaláætlanagerð skal velja Nei.</span><span class="sxs-lookup"><span data-stu-id="cc3f7-112">If a new released product should not be included in Master planning, select No.</span></span> <span data-ttu-id="cc3f7-113">Ef hún á að vera tekin með í aðaláætlanagerð skal hafa stýringuna á sjálfgefna gildinu Já.</span><span class="sxs-lookup"><span data-stu-id="cc3f7-113">If it should be included in Master planning, leave the control at its default value Yes.</span></span>  

## <a name="create-a-new-released-product"></a><span data-ttu-id="cc3f7-114">Stofna nýja útgefna afurð</span><span class="sxs-lookup"><span data-stu-id="cc3f7-114">Create a new released product</span></span>
1. <span data-ttu-id="cc3f7-115">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="cc3f7-115">Close the page.</span></span>
2. <span data-ttu-id="cc3f7-116">Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.</span><span class="sxs-lookup"><span data-stu-id="cc3f7-116">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="cc3f7-117">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="cc3f7-117">Click New.</span></span>
4. <span data-ttu-id="cc3f7-118">Í reitinn Afurðarnúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="cc3f7-118">In the Product number field, type a value.</span></span>
5. <span data-ttu-id="cc3f7-119">Sláið inn gildi í reitinn Afurðarheiti.</span><span class="sxs-lookup"><span data-stu-id="cc3f7-119">In the Product name field, type a value.</span></span>
6. <span data-ttu-id="cc3f7-120">Í svæði Leita að nafni skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="cc3f7-120">In the Search name field, type a value.</span></span>
7. <span data-ttu-id="cc3f7-121">Í reitinn Vörulíkanaflokkur skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="cc3f7-121">In the Item model group field, enter or select a value.</span></span>
8. <span data-ttu-id="cc3f7-122">Í reitinn Vöruflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="cc3f7-122">In the Item group field, enter or select a value.</span></span>
9. <span data-ttu-id="cc3f7-123">Í reitinn Geymsluvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="cc3f7-123">In the Storage dimension group field, enter or select a value.</span></span>
10. <span data-ttu-id="cc3f7-124">Í reitinn Rakningarvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="cc3f7-124">In the Tracking dimension group field, enter or select a value.</span></span>
11. <span data-ttu-id="cc3f7-125">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="cc3f7-125">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="cc3f7-126">Sjálfgefin lífferilsstaða afurðar er altæk skilgreining.</span><span class="sxs-lookup"><span data-stu-id="cc3f7-126">The default product lifecycle state is a global definition.</span></span>  

## <a name="change-the-product-to-an-active-state"></a><span data-ttu-id="cc3f7-127">Breyta afurðinni í virka stöðu</span><span class="sxs-lookup"><span data-stu-id="cc3f7-127">Change the product to an active state</span></span>
1. <span data-ttu-id="cc3f7-128">Sláið inn eða veljið gildi í reitnum Lífferilsstaða afurðar.</span><span class="sxs-lookup"><span data-stu-id="cc3f7-128">In the Product lifecycle state field, enter or select a value.</span></span>

> [!NOTE]
> <span data-ttu-id="cc3f7-129">Gerum ráð fyrir að þú hafir sett upp virka stöðu, þú getur nú valið þessa virku stöðu til að heimila að afurðin sé notuð í aðaláætlanagerð og útreikningi á uppskriftastigi.</span><span class="sxs-lookup"><span data-stu-id="cc3f7-129">Assume that you have set up an active state, you can now select the active state to allow the product to be used in Master planning and BOM-level calculation.</span></span> <span data-ttu-id="cc3f7-130">Augljóslega er þetta aðeins skynsamlegt ef allar upplýsingar um afurð sem krafist er fyrir samræmda áætlanagerð eru tilgreindar.</span><span class="sxs-lookup"><span data-stu-id="cc3f7-130">Obviously, this only makes sense if all the product details that are required for consistent planning are specified.</span></span>  

