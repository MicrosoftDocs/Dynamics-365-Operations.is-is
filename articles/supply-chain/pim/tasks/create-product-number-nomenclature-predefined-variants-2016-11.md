---
title: Stofna nafnakerfi afurðarnúmers fyrir fyrirframskilgreind afurðarafbrigði
description: Þetta efni útskýrir hvernig á að setja inn nafnakerfi afurðarnúmers fyrir fyrirframskilgreind afurðarafbrigði og hvernig því er úthlutað á viðeigandi afurðarvíddarflokknum.
author: ShylaThompson
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 073b680c48855b2a8902c19cedfbf98cdbfdf17d
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150052"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="97317-103">Stofna nafnakerfi afurðarnúmers fyrir fyrirframskilgreind afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="97317-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="97317-104">Þetta efni útskýrir hvernig á að setja inn nafnakerfi afurðarnúmers fyrir fyrirframskilgreind afurðarafbrigði og hvernig því er úthlutað á viðeigandi afurðarvíddarflokknum.</span><span class="sxs-lookup"><span data-stu-id="97317-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="97317-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="97317-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="97317-106">Nýtt nafnakerfi afurðarnúmers er úthlutað á afurðavíddaflokkinn Litur og stærð.</span><span class="sxs-lookup"><span data-stu-id="97317-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="97317-107">Þetta verk myndi yfirleitt vera framkvæmt af hálfu vöruhönnuðar.</span><span class="sxs-lookup"><span data-stu-id="97317-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="97317-108">Stofnaðu Nafnakerfi afurðarnúmers</span><span class="sxs-lookup"><span data-stu-id="97317-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="97317-109">Veldu **Skilgreining afurðarafbrigðislíkans**.</span><span class="sxs-lookup"><span data-stu-id="97317-109">Select **Product variant model definition**.</span></span>
2. <span data-ttu-id="97317-110">Veldu **Nafnakerfi afurðar**.</span><span class="sxs-lookup"><span data-stu-id="97317-110">Select **Product nomenclature**.</span></span>
3. <span data-ttu-id="97317-111">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="97317-111">Select **New**.</span></span>
4. <span data-ttu-id="97317-112">Í reitnum **Heiti** er fært inn heiti nafnakerfis sem gerir auðveldara að greina viðmiðunarafurðarvíddarflokk, til dæmis `ColorSize`.</span><span class="sxs-lookup"><span data-stu-id="97317-112">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
5. <span data-ttu-id="97317-113">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="97317-113">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="97317-114">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="97317-114">Select **Add**.</span></span>
7. <span data-ttu-id="97317-115">Veldu númer **afurðarsniðmáts**.</span><span class="sxs-lookup"><span data-stu-id="97317-115">Select **Product master** number.</span></span>
8. <span data-ttu-id="97317-116">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="97317-116">Select **Add**.</span></span>
9. <span data-ttu-id="97317-117">Veldu **Textafasta**.</span><span class="sxs-lookup"><span data-stu-id="97317-117">Select **Text constant**.</span></span>
10. <span data-ttu-id="97317-118">Í reitnum **Texti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="97317-118">In the **Text** field, type a value.</span></span>
11. <span data-ttu-id="97317-119">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="97317-119">Select **Add**.</span></span>
12. <span data-ttu-id="97317-120">Veldu **Litur**.</span><span class="sxs-lookup"><span data-stu-id="97317-120">Select **Color**.</span></span>
13. <span data-ttu-id="97317-121">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="97317-121">Select **Add**.</span></span>
14. <span data-ttu-id="97317-122">Veldu **Textafasta**.</span><span class="sxs-lookup"><span data-stu-id="97317-122">Select **Text constant**.</span></span>
15. <span data-ttu-id="97317-123">Í reitnum **Texti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="97317-123">In the **Text** field, type a value.</span></span>
16. <span data-ttu-id="97317-124">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="97317-124">Select **Add**.</span></span>
17. <span data-ttu-id="97317-125">Veldu **Stærð**.</span><span class="sxs-lookup"><span data-stu-id="97317-125">Select **Size**.</span></span>
18. <span data-ttu-id="97317-126">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="97317-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="97317-127">Úthluta skal nafnakerfi á afurðarsniðmát</span><span class="sxs-lookup"><span data-stu-id="97317-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="97317-128">Veldu **Afurðavíddaflokka**.</span><span class="sxs-lookup"><span data-stu-id="97317-128">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="97317-129">Veldu hópinn **SizeCol afurðarvídd**.</span><span class="sxs-lookup"><span data-stu-id="97317-129">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="97317-130">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="97317-130">Select **Edit**.</span></span>
4. <span data-ttu-id="97317-131">Veldu **Já** í reitnum **Nota nafnakerfi**.</span><span class="sxs-lookup"><span data-stu-id="97317-131">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="97317-132">Í reitnum **Nafnakerfi afurðarafbrigðisnúmers** skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="97317-132">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="97317-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="97317-133">Close the page.</span></span>

