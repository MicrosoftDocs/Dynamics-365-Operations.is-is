---
title: Stofna nýja afurð í Commerce
description: Þetta efni lýsir því hvernig á að stofna nýja afurð í Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: eb2dd36c6149f2aa40305cd57eac060b232b09e5
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138562"
---
# <a name="create-a-new-product-in-commerce"></a><span data-ttu-id="5f309-103">Stofna nýja afurð í Commerce</span><span class="sxs-lookup"><span data-stu-id="5f309-103">Create a new product in Commerce</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5f309-104">Þetta efni lýsir því hvernig á að stofna nýja afurð í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5f309-104">This topic describes how to create a new product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5f309-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="5f309-105">Overview</span></span>

<span data-ttu-id="5f309-106">Afurð er fyrst og fremst skilgreind af afurðarnúmeri, heiti og lýsingu.</span><span class="sxs-lookup"><span data-stu-id="5f309-106">A product is primarily defined by a product number, name, and description.</span></span> <span data-ttu-id="5f309-107">Hins vegar þarf fleiri upplýsingar til að hægt sé að lýsa afurð eða þjónustu:</span><span class="sxs-lookup"><span data-stu-id="5f309-107">However, other data is also required in order to describe a product or service:</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="5f309-108">Stofna nýja afurð</span><span class="sxs-lookup"><span data-stu-id="5f309-108">Create a new product</span></span>

1. <span data-ttu-id="5f309-109">Í Skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Afurðir og flokkar \> Afurðir eftir flokki**.</span><span class="sxs-lookup"><span data-stu-id="5f309-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Products by category**.</span></span>
1. <span data-ttu-id="5f309-110">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="5f309-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="5f309-111">Í fellilistanum **Gerð afurðar** velurðu annaðhvort **Vara** eða **Þjónusta**.</span><span class="sxs-lookup"><span data-stu-id="5f309-111">In the **Product type** drop-down list, select either **Item** or **Service**.</span></span>
1. <span data-ttu-id="5f309-112">Í fellilistanum **Undirgerð afurðar** velurðu annaðhvort **Afurð** (ef afurðin hefur engin afbrigði) eða **Afurðasniðmát** (ef afurðin verður með afbrigði).</span><span class="sxs-lookup"><span data-stu-id="5f309-112">In the **Product subtype** drop-down list, select either **Product** (if the product will have no variants) or **Product master** (if the product will have variants).</span></span>
1. <span data-ttu-id="5f309-113">Í reitinn **Afurðanúmer** slærðu inn afurðarnúmer ef slíkt hefur ekki þegar verið sett inn.</span><span class="sxs-lookup"><span data-stu-id="5f309-113">In the **Product number** box, enter a product number if one is not already prepopulated.</span></span>
1. <span data-ttu-id="5f309-114">Í reitinn **Heiti afurðar** slærðu inn afurðarheiti.</span><span class="sxs-lookup"><span data-stu-id="5f309-114">In the **Product name** box, enter a product name.</span></span>
1. <span data-ttu-id="5f309-115">Í reitinn **Leitarheiti** slærðu inn leitarheiti.</span><span class="sxs-lookup"><span data-stu-id="5f309-115">In the **Search name** box, enter a search name.</span></span>
1. <span data-ttu-id="5f309-116">Í fellilistanum **Smásöluflokkur** velurðu viðeigandi flokk.</span><span class="sxs-lookup"><span data-stu-id="5f309-116">In the **Retail category** drop-down list, select an appropriate category.</span></span>
1. <span data-ttu-id="5f309-117">Ef afurðin er sett velurðu **Já** fyrir **Afurðasett**.</span><span class="sxs-lookup"><span data-stu-id="5f309-117">If the product is a kit, select **Yes** for **Product kit**.</span></span>
1. <span data-ttu-id="5f309-118">Ef undirtegund afurðarinnar er afurðarsniðmát skaltu stilla **Afurðavíddaflokkur** til að innihalda studd afbrigði.</span><span class="sxs-lookup"><span data-stu-id="5f309-118">If the product subtype is product master, set the **Product dimension group** to include the supported variants.</span></span> <span data-ttu-id="5f309-119">Valkostirnir eru meðal annars **Litur**, **Stærð**, **Stíll** og **Stilling**.</span><span class="sxs-lookup"><span data-stu-id="5f309-119">Options include **Color**, **Size**, **Style**, and **Configuration**.</span></span> <span data-ttu-id="5f309-120">Þú gætir þurft að búa til fleiri afurðavíddaflokka ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="5f309-120">You may need to create additional product dimension groups if needed.</span></span>
1. <span data-ttu-id="5f309-121">Í fellilistanum **Afbrigðistækni** velurðu viðeigandi valkost.</span><span class="sxs-lookup"><span data-stu-id="5f309-121">In the **Configuration technology** drop-down list, select an appropriate option.</span></span>
1. <span data-ttu-id="5f309-122">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f309-122">Select **OK**.</span></span>

<span data-ttu-id="5f309-123">Eftirfarandi mynd sýnir dæmi um afurð sem er bætt við.</span><span class="sxs-lookup"><span data-stu-id="5f309-123">The following image shows an example product being added.</span></span>

![Stofna afurð](media/create-new-product.png)

<span data-ttu-id="5f309-125">Þegar afurð er bætt við er hægt að stilla viðbótargögn fyrir hana, svo sem **Afurðarlýsing**, **Afbrigðaflokkar**, **Víddarflokkar**, **Afurðaeigindir** og **Skyldar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="5f309-125">Once a product is added, additional data can be set for it, such as **Product description**, **Variant groups**, **Dimension groups**, **Product attributes**, and **Related products**.</span></span>

<span data-ttu-id="5f309-126">Eftirfarandi mynd sýnir viðbótarupplýsingar afurðar.</span><span class="sxs-lookup"><span data-stu-id="5f309-126">The following image shows a product's additional details.</span></span>

![Upplýsingar um afurð](media/create-new-product-2.png)

### <a name="create-product-variants"></a><span data-ttu-id="5f309-128">Stofna afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="5f309-128">Create product variants</span></span>

<span data-ttu-id="5f309-129">Ef undirtegund afurðarinnar er **Afurðarsniðmát** verður að búa til sérstök afbrigði.</span><span class="sxs-lookup"><span data-stu-id="5f309-129">If the product subtype is **Product master**, specific variants will need to be created.</span></span> 

<span data-ttu-id="5f309-130">Til að stofna afurðarafbrigði skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="5f309-130">To create product variants, follow these steps.</span></span>

1. <span data-ttu-id="5f309-131">Í aðgerðasvæðinu velurðu **Afurðarafbrigði**.</span><span class="sxs-lookup"><span data-stu-id="5f309-131">On the action pane, select **Product variants**.</span></span>
1. <span data-ttu-id="5f309-132">Ef afbrigðishópar hafa verið valdir á aðgerðarglugganum, veldu \**Tillögur um afbrigði*.</span><span class="sxs-lookup"><span data-stu-id="5f309-132">If variant groups have been selected on the action pane, select \**Variant suggestions*.</span></span>
1. <span data-ttu-id="5f309-133">Veldu afbrigði sem þú vilt styðja fyrir afurðina.</span><span class="sxs-lookup"><span data-stu-id="5f309-133">Select the variants you would like to support for the product.</span></span>
1. <span data-ttu-id="5f309-134">Velja **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="5f309-134">Select **Create**.</span></span>

## <a name="release-a-product"></a><span data-ttu-id="5f309-135">Losaðu afurð</span><span class="sxs-lookup"><span data-stu-id="5f309-135">Release a product</span></span>

<span data-ttu-id="5f309-136">Til að selja afurð verður hún fyrst að verða gefin út til lögaðila.</span><span class="sxs-lookup"><span data-stu-id="5f309-136">To sell a product it must first be released to a legal entity.</span></span>

1. <span data-ttu-id="5f309-137">Af afurðasíðunni velurðu **Losa afurðir**.</span><span class="sxs-lookup"><span data-stu-id="5f309-137">From the product page, select **Release products**.</span></span>

    ![Losa afurð](media/create-new-product-3.png)

1. <span data-ttu-id="5f309-139">Veldu afurðina til að losa og veldu síðan **Næst**.</span><span class="sxs-lookup"><span data-stu-id="5f309-139">Select the product to release, and then select **Next**.</span></span>

    ![Veldu afurð til að losa](media/create-new-product-4.png)

1. <span data-ttu-id="5f309-141">Veldu flokk afurðarafbrigða til að losa og veldu síðan **Næst**.</span><span class="sxs-lookup"><span data-stu-id="5f309-141">Select the set of product variants to release, and then select **Next**.</span></span>

    ![Veldu afbrigði til að losa](media/create-new-product-5.png)

1. <span data-ttu-id="5f309-143">Veldu lögaðilann og veldu síðan **Næst**.</span><span class="sxs-lookup"><span data-stu-id="5f309-143">Select the legal entity, and then select **Next**.</span></span>

    ![Velja lögaðila](media/create-new-product-6.png)

1. <span data-ttu-id="5f309-145">Veljið **Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="5f309-145">Select **Finish**.</span></span>

    ![Ljúktu losun afurðar](media/create-new-product-7.png)

## <a name="configure-a-released-product"></a><span data-ttu-id="5f309-147">Samskipaðu losaða afurð</span><span class="sxs-lookup"><span data-stu-id="5f309-147">Configure a released product</span></span>

<span data-ttu-id="5f309-148">Þegar afurð er losuð þarf hún síðan frekari stillingar sem fela í sér að bæta við verði við afurðina.</span><span class="sxs-lookup"><span data-stu-id="5f309-148">Once a product is released, it will then require further configuration that includes adding a price to the product.</span></span>

1. <span data-ttu-id="5f309-149">Í Skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Afurðir og flokkar \> Losaðar afurðir eftir flokki**.</span><span class="sxs-lookup"><span data-stu-id="5f309-149">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="5f309-150">Veldu afurðaflokkshnút fyrir afurðina sem var losuð og veldu síðan afurðina af afurðalistanum.</span><span class="sxs-lookup"><span data-stu-id="5f309-150">Select the product category node for the product that was released, and then select the product from the product list.</span></span>
1. <span data-ttu-id="5f309-151">Í aðgerðaglugganum velurðu **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="5f309-151">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="5f309-152">Í kaflanum **Kaupa** stillirðu alla nauðsynlega eiginleika, þ.m.t. **Eining**, **Verð** og **Magn**.</span><span class="sxs-lookup"><span data-stu-id="5f309-152">In the **Purchase** section, configure any required properties including **Unit**, **Price**,  and **Quantity**.</span></span>
1. <span data-ttu-id="5f309-153">Í aðgerðarglugganum velurðu **Staðfesta** til að tryggja að engar villur hafi verið tilkynntar vegna reita sem vantar.</span><span class="sxs-lookup"><span data-stu-id="5f309-153">On the action pane, select **Validate** to ensure that no errors are reported for missing fields.</span></span>
1. <span data-ttu-id="5f309-154">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="5f309-154">On the action pane, select **Save**.</span></span>

<span data-ttu-id="5f309-155">Eftirfarandi mynd sýnir dæmi um stillingu á losaðri afurð.</span><span class="sxs-lookup"><span data-stu-id="5f309-155">The following image shows an example configuration for a released product.</span></span>

![Samskipaðu losaða afurð](media/create-new-product-8.png)

## <a name="additional-resources"></a><span data-ttu-id="5f309-157">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="5f309-157">Additional resources</span></span>

[<span data-ttu-id="5f309-158">Stofna lögaðila</span><span class="sxs-lookup"><span data-stu-id="5f309-158">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="5f309-159">Stofna afbrigðaflokk</span><span class="sxs-lookup"><span data-stu-id="5f309-159">Create a variant group</span></span>](create-variant-group.md) 