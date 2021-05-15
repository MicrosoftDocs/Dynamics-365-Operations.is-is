---
title: Stofna nafnakerfi afurðarnúmers fyrir fyrirframskilgreind afurðarafbrigði
description: Þetta efni útskýrir hvernig á að setja inn nafnakerfi afurðarnúmers fyrir fyrirframskilgreind afurðarafbrigði og hvernig því er úthlutað á viðeigandi afurðarvíddarflokknum.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4bb73854f52525c0722683086d1b4f1dd7173306
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920658"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="7ac06-103">Stofna nafnakerfi afurðarnúmers fyrir fyrirframskilgreind afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="7ac06-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7ac06-104">Þetta efni útskýrir hvernig á að setja inn nafnakerfi afurðarnúmers fyrir fyrirframskilgreind afurðarafbrigði og hvernig því er úthlutað á viðeigandi afurðarvíddarflokknum.</span><span class="sxs-lookup"><span data-stu-id="7ac06-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="7ac06-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="7ac06-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="7ac06-106">Nýtt nafnakerfi afurðarnúmers er úthlutað á afurðavíddaflokkinn Litur og stærð.</span><span class="sxs-lookup"><span data-stu-id="7ac06-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="7ac06-107">Þetta verk myndi yfirleitt vera framkvæmt af hálfu vöruhönnuðar.</span><span class="sxs-lookup"><span data-stu-id="7ac06-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="7ac06-108">Stofnaðu Nafnakerfi afurðarnúmers</span><span class="sxs-lookup"><span data-stu-id="7ac06-108">Create a product number nomenclature</span></span>

1. <span data-ttu-id="7ac06-109">Farið í **Afurðaupplýsingastjórnun \> Uppsetning \> Nafnakerfi afurðar**.</span><span class="sxs-lookup"><span data-stu-id="7ac06-109">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="7ac06-110">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="7ac06-110">Select **New**.</span></span>
1. <span data-ttu-id="7ac06-111">Í reitnum **Heiti** er fært inn heiti nafnakerfis sem gerir auðveldara að greina viðmiðunarafurðarvíddarflokk, til dæmis `ColorSize`.</span><span class="sxs-lookup"><span data-stu-id="7ac06-111">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
1. <span data-ttu-id="7ac06-112">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7ac06-112">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="7ac06-113">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="7ac06-113">Select **Add**.</span></span>
1. <span data-ttu-id="7ac06-114">Veldu númer **afurðarsniðmáts**.</span><span class="sxs-lookup"><span data-stu-id="7ac06-114">Select **Product master** number.</span></span>
1. <span data-ttu-id="7ac06-115">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="7ac06-115">Select **Add**.</span></span>
1. <span data-ttu-id="7ac06-116">Veldu **Textafasta**.</span><span class="sxs-lookup"><span data-stu-id="7ac06-116">Select **Text constant**.</span></span>
1. <span data-ttu-id="7ac06-117">Í reitnum **Texti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7ac06-117">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="7ac06-118">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="7ac06-118">Select **Add**.</span></span>
1. <span data-ttu-id="7ac06-119">Veldu **Litur**.</span><span class="sxs-lookup"><span data-stu-id="7ac06-119">Select **Color**.</span></span>
1. <span data-ttu-id="7ac06-120">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="7ac06-120">Select **Add**.</span></span>
1. <span data-ttu-id="7ac06-121">Veldu **Textafasta**.</span><span class="sxs-lookup"><span data-stu-id="7ac06-121">Select **Text constant**.</span></span>
1. <span data-ttu-id="7ac06-122">Í reitnum **Texti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7ac06-122">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="7ac06-123">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="7ac06-123">Select **Add**.</span></span>
1. <span data-ttu-id="7ac06-124">Veldu **Stærð**.</span><span class="sxs-lookup"><span data-stu-id="7ac06-124">Select **Size**.</span></span>
1. <span data-ttu-id="7ac06-125">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7ac06-125">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="7ac06-126">Úthluta skal nafnakerfi á afurðarsniðmát</span><span class="sxs-lookup"><span data-stu-id="7ac06-126">Assign the nomenclature to a product master</span></span>

1. <span data-ttu-id="7ac06-127">Veldu **Afurðavíddaflokka**.</span><span class="sxs-lookup"><span data-stu-id="7ac06-127">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="7ac06-128">Veldu hópinn **SizeCol afurðarvídd**.</span><span class="sxs-lookup"><span data-stu-id="7ac06-128">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="7ac06-129">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="7ac06-129">Select **Edit**.</span></span>
4. <span data-ttu-id="7ac06-130">Veldu **Já** í reitnum **Nota nafnakerfi**.</span><span class="sxs-lookup"><span data-stu-id="7ac06-130">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="7ac06-131">Í reitnum **Nafnakerfi afurðarafbrigðisnúmers** skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7ac06-131">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="7ac06-132">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7ac06-132">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]