---
title: Stofna stigveldi afurðaflokkunar
description: Þessi verklýsing sýnir hvernig á að stofna nýtt tegundastigveldi og tengja gerð stigveldis vörukóða.
author: ShylaThompson
manager: tfehr
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0ff1a2ba20059d3fcb0347220e6e81130e03ac0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203734"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="831db-103">Stofna stigveldi afurðaflokkunar</span><span class="sxs-lookup"><span data-stu-id="831db-103">Create a hierarchy of product classification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="831db-104">Þessi verklýsing sýnir hvernig á að stofna nýtt tegundastigveldi og tengja gerð stigveldis vörukóða.</span><span class="sxs-lookup"><span data-stu-id="831db-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="831db-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="831db-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="831db-106">Þetta ferli er ætluð fyrir stjórnanda tegundar.</span><span class="sxs-lookup"><span data-stu-id="831db-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="831db-107">Stofna nýtt tegundastigveldi</span><span class="sxs-lookup"><span data-stu-id="831db-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="831db-108">Farðu í **Skoðunarrúðu > Kerfi > Afurðaupplýsingastjórnun > Uppsetningu > Flokkar og eigindir > Flokkastigveldi**.</span><span class="sxs-lookup"><span data-stu-id="831db-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="831db-109">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="831db-109">Click **New**.</span></span>
3. <span data-ttu-id="831db-110">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="831db-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="831db-111">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="831db-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="831db-112">Smellið á **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="831db-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="831db-113">Byggja stigveldi</span><span class="sxs-lookup"><span data-stu-id="831db-113">Build the hierarchy</span></span>
1. <span data-ttu-id="831db-114">Smelltu á **Nýjan** flokkahnút.</span><span class="sxs-lookup"><span data-stu-id="831db-114">Click **New** category node.</span></span>
2. <span data-ttu-id="831db-115">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="831db-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="831db-116">Í reitnum **Kóði** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="831db-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="831db-117">Í reitnum **Stutt heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="831db-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="831db-118">Smelltu á **Nýjan** flokkahnút.</span><span class="sxs-lookup"><span data-stu-id="831db-118">Click **New** category node.</span></span>
6. <span data-ttu-id="831db-119">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="831db-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="831db-120">Í reitnum **Kóði** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="831db-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="831db-121">Í reitnum **Stutt heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="831db-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="831db-122">Smelltu á **Nýjan** flokkahnút.</span><span class="sxs-lookup"><span data-stu-id="831db-122">Click **New** category node.</span></span>
10. <span data-ttu-id="831db-123">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="831db-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="831db-124">Í reitnum **Kóði** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="831db-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="831db-125">Í reitnum **Stutt heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="831db-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="831db-126">Smelltu á **Nýjan** flokkahnút.</span><span class="sxs-lookup"><span data-stu-id="831db-126">Click **New** category node.</span></span>
14. <span data-ttu-id="831db-127">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="831db-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="831db-128">Í reitnum **Kóði** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="831db-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="831db-129">Í reitnum **Stutt heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="831db-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="831db-130">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="831db-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="831db-131">Flokka stigveldi</span><span class="sxs-lookup"><span data-stu-id="831db-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="831db-132">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="831db-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="831db-133">Í **Aðgerðarúðu** skal smella á **Flokkastigveldi**.</span><span class="sxs-lookup"><span data-stu-id="831db-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="831db-134">Smelltu á **Tengja stigveldisgerð**.</span><span class="sxs-lookup"><span data-stu-id="831db-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="831db-135">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="831db-135">Click **New**.</span></span>
5. <span data-ttu-id="831db-136">Í reitnum **Gerð flokkastigveldis** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="831db-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="831db-137">Veldu **Vörukóða gerðar tegundarstigveldiskóða fyrir flokkun afurðar**.</span><span class="sxs-lookup"><span data-stu-id="831db-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="831db-138">Í reitnum **Flokkastigveldi** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="831db-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="831db-139">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="831db-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="831db-140">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="831db-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="831db-141">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="831db-141">Close the page.</span></span>

