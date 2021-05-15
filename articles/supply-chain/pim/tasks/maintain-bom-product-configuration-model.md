---
title: Vinna með uppskrift fyrir afbrigðalíkan afurðar
description: Keyra þetta ferli krefst fyrirliggjandi skilgreiningu afbrigðalíkan afurðar.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b4ad73265e321b6339c061a7866b55cb2769954b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921318"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="055f7-103">Vinna með uppskrift fyrir afbrigðalíkan afurðar</span><span class="sxs-lookup"><span data-stu-id="055f7-103">Maintain BOM for a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="055f7-104">Keyra þetta ferli krefst fyrirliggjandi skilgreiningu afbrigðalíkan afurðar.</span><span class="sxs-lookup"><span data-stu-id="055f7-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="055f7-105">Hágæða hátalara líkan í fyrirtækinu sýnigögn USMF er notað til að stofna þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="055f7-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>

## <a name="add-a-bom-line"></a><span data-ttu-id="055f7-106">Bæta við uppskriftarlína</span><span class="sxs-lookup"><span data-stu-id="055f7-106">Add a BOM line</span></span>

1. <span data-ttu-id="055f7-107">Farið í **Afurðarupplýsingastjórnun \> Afurðir \> Afbrigðalíkön afurða**.</span><span class="sxs-lookup"><span data-stu-id="055f7-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="055f7-108">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="055f7-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="055f7-109">Veljið hágæða hátalara fyrir þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="055f7-109">Select the High end speaker for this procedure.</span></span>  
1. <span data-ttu-id="055f7-110">Í listanum skal velja tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="055f7-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="055f7-111">Stækka hlutann **Uppskriftarlínur**.</span><span class="sxs-lookup"><span data-stu-id="055f7-111">Expand the **BOM lines** section.</span></span>
1. <span data-ttu-id="055f7-112">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="055f7-112">Select **Add**.</span></span>
1. <span data-ttu-id="055f7-113">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="055f7-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="055f7-114">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="055f7-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="055f7-115">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="055f7-115">Select **Save**.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="055f7-116">Bæta við uppskriftarlínuupplýsingar</span><span class="sxs-lookup"><span data-stu-id="055f7-116">Add BOM line details</span></span>

1. <span data-ttu-id="055f7-117">Veljið **Upplýsingar um uppskriftarlínu**.</span><span class="sxs-lookup"><span data-stu-id="055f7-117">Select **BOM line details**.</span></span>
2. <span data-ttu-id="055f7-118">Í reitinn **Vörunúmer** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="055f7-118">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="055f7-119">Til dæmis er hægt að velja M0055 vöru.</span><span class="sxs-lookup"><span data-stu-id="055f7-119">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="055f7-120">Fyrir hvern línueiginleika Uppskriftar, er hægt að velja hvort hún tekur fast gildi eða er varpað á eigind.</span><span class="sxs-lookup"><span data-stu-id="055f7-120">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="055f7-121">Veljið gátreitinn **Stilla**.</span><span class="sxs-lookup"><span data-stu-id="055f7-121">Select the **Set** check box.</span></span>
4. <span data-ttu-id="055f7-122">Velja skal *Já* í reitnum **Útreikningur**.</span><span class="sxs-lookup"><span data-stu-id="055f7-122">Select *Yes* in the **Calculation** field.</span></span>
    * <span data-ttu-id="055f7-123">Ef **Útreikningur** eiginleikinn er stilltur á *Já* er uppskriftarlínunni tekin með í útreikningi kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="055f7-123">Setting the **Calculation** property to *Yes* ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="055f7-124">Veljið flipann **Uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="055f7-124">Select the **Setup** tab.</span></span>
6. <span data-ttu-id="055f7-125">Veljið gátreitinn **Stilla**.</span><span class="sxs-lookup"><span data-stu-id="055f7-125">Select the **Set** check box.</span></span>
7. <span data-ttu-id="055f7-126">Í reitnum **Magn** slærðu inn tölu.</span><span class="sxs-lookup"><span data-stu-id="055f7-126">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="055f7-127">Magn svæðið ákvarðar hversu mikið vörunnar sem verða innifalin í Uppskriftinni.</span><span class="sxs-lookup"><span data-stu-id="055f7-127">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="055f7-128">Þetta gæti verið að augljós umsækjanda fyrir eigindarvörpun.</span><span class="sxs-lookup"><span data-stu-id="055f7-128">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="055f7-129">Veljið flipann **Vídd**.</span><span class="sxs-lookup"><span data-stu-id="055f7-129">Select the **Dimension** tab.</span></span>
    * <span data-ttu-id="055f7-130">Staðfesta ef einhver afurðarvíddum eru virk og þess vegna verður að hafa gildi eða eigind sem er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="055f7-130">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="055f7-131">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="055f7-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]