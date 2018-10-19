--- 
title: "Stofna nafnakerfi afurðarnúmers fyrir fyrirframskilgreind afurðarafbrigði"
description: "Þessari handbók sýnir hvernig á að setja inn nafnakerfi afurðarnúmers fyrir fyrirframskilgreind afurðarafbrigði og hvernig því er úthlutað á viðeigandi afurðarvíddarflokknum."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 4b49e96677b94d5f669ea41861f64e62e118938c
ms.contentlocale: is-is
ms.lasthandoff: 10/16/2018

---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="9c1d2-103">Stofna nafnakerfi afurðarnúmers fyrir fyrirframskilgreind afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="9c1d2-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9c1d2-104">Þessari handbók sýnir hvernig á að setja inn nafnakerfi afurðarnúmers fyrir fyrirframskilgreind afurðarafbrigði og hvernig því er úthlutað á viðeigandi afurðarvíddarflokknum.</span><span class="sxs-lookup"><span data-stu-id="9c1d2-104">This guide shows you how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="9c1d2-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="9c1d2-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="9c1d2-106">Nýtt nafnakerfi afurðarnúmers er úthlutað á afurðavíddaflokkinn Litur og stærð.</span><span class="sxs-lookup"><span data-stu-id="9c1d2-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="9c1d2-107">Þetta verk myndi yfirleitt vera framkvæmt af hálfu vöruhönnuðar.</span><span class="sxs-lookup"><span data-stu-id="9c1d2-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="9c1d2-108">Stofnaðu Nafnakerfi afurðarnúmers</span><span class="sxs-lookup"><span data-stu-id="9c1d2-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="9c1d2-109">Smellið á Skilgreining afurðarafbrigðislíkans</span><span class="sxs-lookup"><span data-stu-id="9c1d2-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="9c1d2-110">Smelltu á Nafnakerfi afurðar.</span><span class="sxs-lookup"><span data-stu-id="9c1d2-110">Click Product nomenclature.</span></span>
3. <span data-ttu-id="9c1d2-111">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="9c1d2-111">Click New.</span></span>
4. <span data-ttu-id="9c1d2-112">Í reitnum Heiti er fært inn heiti nafnakerfis sem gerir auðveldara að greina viðmiðunarafurðarvíddarflokk, til dæmis ColorSize...</span><span class="sxs-lookup"><span data-stu-id="9c1d2-112">In the Name field, enter a nomenclature name that helps to identify the target product dimension group, for example, ColorSize..</span></span>
5. <span data-ttu-id="9c1d2-113">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="9c1d2-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="9c1d2-114">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="9c1d2-114">Click Add.</span></span>
7. <span data-ttu-id="9c1d2-115">Smelltu á Númer afurðarsniðmáts.</span><span class="sxs-lookup"><span data-stu-id="9c1d2-115">Click Product master number.</span></span>
8. <span data-ttu-id="9c1d2-116">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="9c1d2-116">Click Add.</span></span>
9. <span data-ttu-id="9c1d2-117">Smelltu á Textafasta.</span><span class="sxs-lookup"><span data-stu-id="9c1d2-117">Click Text constant.</span></span>
10. <span data-ttu-id="9c1d2-118">Í reitinn Texti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9c1d2-118">In the Text field, type a value.</span></span>
11. <span data-ttu-id="9c1d2-119">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="9c1d2-119">Click Add.</span></span>
12. <span data-ttu-id="9c1d2-120">Smelltu á lit.</span><span class="sxs-lookup"><span data-stu-id="9c1d2-120">Click Color.</span></span>
13. <span data-ttu-id="9c1d2-121">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="9c1d2-121">Click Add.</span></span>
14. <span data-ttu-id="9c1d2-122">Smelltu á Textafasta.</span><span class="sxs-lookup"><span data-stu-id="9c1d2-122">Click Text constant.</span></span>
15. <span data-ttu-id="9c1d2-123">Í reitinn Texti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9c1d2-123">In the Text field, type a value.</span></span>
16. <span data-ttu-id="9c1d2-124">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="9c1d2-124">Click Add.</span></span>
17. <span data-ttu-id="9c1d2-125">Smelltu á Stærð.</span><span class="sxs-lookup"><span data-stu-id="9c1d2-125">Click Size.</span></span>
18. <span data-ttu-id="9c1d2-126">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9c1d2-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="9c1d2-127">Úthluta skal nafnakerfi á afurðarsniðmát</span><span class="sxs-lookup"><span data-stu-id="9c1d2-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="9c1d2-128">Smelltu á Afurðavíddaflokka.</span><span class="sxs-lookup"><span data-stu-id="9c1d2-128">Click Product dimension groups.</span></span>
2. <span data-ttu-id="9c1d2-129">Velja skal afurðavíddaflokkinn SizeCol.</span><span class="sxs-lookup"><span data-stu-id="9c1d2-129">Select the SizeCol product dimension group.</span></span>
3. <span data-ttu-id="9c1d2-130">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="9c1d2-130">Click Edit.</span></span>
4. <span data-ttu-id="9c1d2-131">Velja skal Já í reitnum Nota nafnakerfi.</span><span class="sxs-lookup"><span data-stu-id="9c1d2-131">Select Yes in the Use nomenclature field.</span></span>
5. <span data-ttu-id="9c1d2-132">Í reitnum Nafnakerfi afurðarafbrigðisnúmers skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="9c1d2-132">In the Product variant number nomenclature field, enter or select a value.</span></span>
6. <span data-ttu-id="9c1d2-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9c1d2-133">Close the page.</span></span>


