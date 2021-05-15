---
title: Setja upp verð sem byggir á eigindum fyrir skilgreinanlegar afurðir
description: Þetta efni útskýrir hvernig á að setja upp eigindabyggða úthlutun.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c30c520e7265c2676937f5191844f6789c364e6
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921242"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="5194b-103">Setja upp verð sem byggir á eigindum fyrir skilgreinanlegar afurðir</span><span class="sxs-lookup"><span data-stu-id="5194b-103">Set up attribute-based pricing for configurable products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5194b-104">Þetta efni útskýrir hvernig á að setja upp eigindabyggða úthlutun.</span><span class="sxs-lookup"><span data-stu-id="5194b-104">This topic explains how to set up attribute-based pricing.</span></span> <span data-ttu-id="5194b-105">Sem skilyrði, verður að hafa afbrigðalíkan afurðar sem hefur eitt eða fleiri íhluti og eiginleika.</span><span class="sxs-lookup"><span data-stu-id="5194b-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="5194b-106">Þessi aðferð notar hágæða hátalara líkanið gögn fyrirtækisins sýnigögn USMF.</span><span class="sxs-lookup"><span data-stu-id="5194b-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="5194b-107">Venjulega notar framleiðslustjóri þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="5194b-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="5194b-108">Búa til nýtt verðlíkan</span><span class="sxs-lookup"><span data-stu-id="5194b-108">Create a new price model</span></span>

1. <span data-ttu-id="5194b-109">Farið í **Afurðarupplýsingastjórnun \> Afurðir \> Afbrigðalíkön afurða**.</span><span class="sxs-lookup"><span data-stu-id="5194b-109">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="5194b-110">Á listanum velurðu línuna fyrir **Hágæða hátalara** en velur ekki tengilinn fyrir heitið.</span><span class="sxs-lookup"><span data-stu-id="5194b-110">In the list, select the **High End Speaker** line, but don't select the link for the name.</span></span>
1. <span data-ttu-id="5194b-111">Í aðgerðarúðunni skal velja **Tegund**.</span><span class="sxs-lookup"><span data-stu-id="5194b-111">On the Action Pane, select **Model**.</span></span>
1. <span data-ttu-id="5194b-112">Veldu **Verðlíkön**.</span><span class="sxs-lookup"><span data-stu-id="5194b-112">Select **Price models**.</span></span>
1. <span data-ttu-id="5194b-113">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="5194b-113">Select **New**.</span></span>
1. <span data-ttu-id="5194b-114">Í reitinn **Verðlíkan** skal rita gildi.</span><span class="sxs-lookup"><span data-stu-id="5194b-114">In the **Price model name** field, type a value.</span></span> <span data-ttu-id="5194b-115">Notið nafn sem gerir auðvelt að bera kennsl á líkan.</span><span class="sxs-lookup"><span data-stu-id="5194b-115">Use a name that makes the model easy to identify.</span></span>  
1. <span data-ttu-id="5194b-116">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5194b-116">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="5194b-117">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5194b-117">Select **Save**.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="5194b-118">Bæta við verðeiningum</span><span class="sxs-lookup"><span data-stu-id="5194b-118">Add price elements</span></span>

1. <span data-ttu-id="5194b-119">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="5194b-119">Select **Edit**.</span></span> <span data-ttu-id="5194b-120">Hver íhlutur í framleiðslulíkani getur haft grunnverð einingu og fjölda verðsegðarreglna.</span><span class="sxs-lookup"><span data-stu-id="5194b-120">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="5194b-121">Einnig er hægt að bæta verði í mismunandi gjaldmiðlum.</span><span class="sxs-lookup"><span data-stu-id="5194b-121">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="5194b-122">Í reitinn **Grunnverðssegð** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5194b-122">In the **Base price expression** field, type a value.</span></span> <span data-ttu-id="5194b-123">Til dæmis, skrifið 100.</span><span class="sxs-lookup"><span data-stu-id="5194b-123">For example, type 100.</span></span> <span data-ttu-id="5194b-124">Grunnverðssegð getur verið tölugildi eða það getur verið samsett af útreikningi sem felur í sér eina eða fleiri eigindir.</span><span class="sxs-lookup"><span data-stu-id="5194b-124">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="5194b-125">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="5194b-125">Select **Add**.</span></span>
4. <span data-ttu-id="5194b-126">Í reitinn **Heiti** skaltu færa inn `Rosewood`.</span><span class="sxs-lookup"><span data-stu-id="5194b-126">In the **Name** field, type `Rosewood`.</span></span> <span data-ttu-id="5194b-127">Nafn verð segð gerir auðveldara að verð einingarinnar sem stendur.</span><span class="sxs-lookup"><span data-stu-id="5194b-127">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="5194b-128">Í þessu dæmi er mælt stofna verðeining fyrir Rosewood speaker cabinet ljúka valkost.</span><span class="sxs-lookup"><span data-stu-id="5194b-128">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="5194b-129">Veldu **Breyta ástandi**.</span><span class="sxs-lookup"><span data-stu-id="5194b-129">Select **Edit condition**.</span></span> <span data-ttu-id="5194b-130">Skilyrði verð hjálpar til við að tryggja samræmda segðareining verð er innifalinn í söluverði ef tiltekna samsetningu af eigindir eru til staðar.</span><span class="sxs-lookup"><span data-stu-id="5194b-130">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="5194b-131">Í reitinn **ConstraintBody** skal slá inn `CabinetFinish=="Rosewood"`.</span><span class="sxs-lookup"><span data-stu-id="5194b-131">In the **ConstraintBody** field, enter `CabinetFinish=="Rosewood"`.</span></span>
7. <span data-ttu-id="5194b-132">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5194b-132">Select **OK**.</span></span>
8. <span data-ttu-id="5194b-133">Í reitinn **Segð** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5194b-133">In the **Expression** field, type a value.</span></span> <span data-ttu-id="5194b-134">Til dæmis, slá inn `50`.</span><span class="sxs-lookup"><span data-stu-id="5194b-134">For example, type `50`.</span></span> 
9. <span data-ttu-id="5194b-135">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5194b-135">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]