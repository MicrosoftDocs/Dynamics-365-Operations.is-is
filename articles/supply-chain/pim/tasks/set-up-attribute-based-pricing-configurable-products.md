---
title: Setja upp verð sem byggir á eigindum fyrir skilgreinanlegar afurðir
description: Þetta efni útskýrir hvernig á að setja upp eigindabyggða úthlutun.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7382cdfa11e89896bba9518f36eb6caab56b98f6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213056"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="03eeb-103">Setja upp verð sem byggir á eigindum fyrir skilgreinanlegar afurðir</span><span class="sxs-lookup"><span data-stu-id="03eeb-103">Set up attribute-based pricing for configurable products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="03eeb-104">Þetta efni útskýrir hvernig á að setja upp eigindabyggða úthlutun.</span><span class="sxs-lookup"><span data-stu-id="03eeb-104">This topic explains how to set up attribute-based pricing.</span></span> <span data-ttu-id="03eeb-105">Sem skilyrði, verður að hafa afbrigðalíkan afurðar sem hefur eitt eða fleiri íhluti og eiginleika.</span><span class="sxs-lookup"><span data-stu-id="03eeb-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="03eeb-106">Þessi aðferð notar hágæða hátalara líkanið gögn fyrirtækisins sýnigögn USMF.</span><span class="sxs-lookup"><span data-stu-id="03eeb-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="03eeb-107">Venjulega notar framleiðslustjóri þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="03eeb-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="03eeb-108">Búa til nýtt verðlíkan</span><span class="sxs-lookup"><span data-stu-id="03eeb-108">Create a new price model</span></span>
1. <span data-ttu-id="03eeb-109">Veldu **Skilgreining afurðarafbrigðislíkans** á heimasíðunni.</span><span class="sxs-lookup"><span data-stu-id="03eeb-109">Select **Product variant model definition** on the home page.</span></span>
2. <span data-ttu-id="03eeb-110">Veldu **Afbrigðalíka afurðar** í kaflanum **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="03eeb-110">Select **Product configuration models** in the **links** section.</span></span>
3. <span data-ttu-id="03eeb-111">Á listanum velurðu línuna fyrir **Hágæða hátalara** en velur ekki tengilinn fyrir heitið.</span><span class="sxs-lookup"><span data-stu-id="03eeb-111">In the list, select the **High End Speaker** line, but don't select the link for the name.</span></span>
4. <span data-ttu-id="03eeb-112">Í aðgerðarúðunni skal velja **Tegund**.</span><span class="sxs-lookup"><span data-stu-id="03eeb-112">On the Action Pane, select **Model**.</span></span>
5. <span data-ttu-id="03eeb-113">Veldu **Verðlíkön**.</span><span class="sxs-lookup"><span data-stu-id="03eeb-113">Select **Price models**.</span></span>
6. <span data-ttu-id="03eeb-114">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="03eeb-114">Select **New**.</span></span>
7. <span data-ttu-id="03eeb-115">Í reitinn **Verðlíkan** skal rita gildi.</span><span class="sxs-lookup"><span data-stu-id="03eeb-115">In the **Price model name** field, type a value.</span></span> <span data-ttu-id="03eeb-116">Notið nafn sem gerir auðvelt að bera kennsl á líkan.</span><span class="sxs-lookup"><span data-stu-id="03eeb-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="03eeb-117">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="03eeb-117">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="03eeb-118">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="03eeb-118">Select **Save**.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="03eeb-119">Bæta við verðeiningum</span><span class="sxs-lookup"><span data-stu-id="03eeb-119">Add price elements</span></span>
1. <span data-ttu-id="03eeb-120">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="03eeb-120">Select **Edit**.</span></span> <span data-ttu-id="03eeb-121">Hver íhlutur í framleiðslulíkani getur haft grunnverð einingu og fjölda verðsegðarreglna.</span><span class="sxs-lookup"><span data-stu-id="03eeb-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="03eeb-122">Einnig er hægt að bæta verði í mismunandi gjaldmiðlum.</span><span class="sxs-lookup"><span data-stu-id="03eeb-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="03eeb-123">Í reitinn **Grunnverðssegð** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="03eeb-123">In the **Base price expression** field, type a value.</span></span> <span data-ttu-id="03eeb-124">Til dæmis, skrifið 100.</span><span class="sxs-lookup"><span data-stu-id="03eeb-124">For example, type 100.</span></span> <span data-ttu-id="03eeb-125">Grunnverðssegð getur verið tölugildi eða það getur verið samsett af útreikningi sem felur í sér eina eða fleiri eigindir.</span><span class="sxs-lookup"><span data-stu-id="03eeb-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="03eeb-126">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="03eeb-126">Select **Add**.</span></span>
4. <span data-ttu-id="03eeb-127">Í reitinn **Heiti** skaltu færa inn `Rosewood`.</span><span class="sxs-lookup"><span data-stu-id="03eeb-127">In the **Name** field, type `Rosewood`.</span></span> <span data-ttu-id="03eeb-128">Nafn verð segð gerir auðveldara að verð einingarinnar sem stendur.</span><span class="sxs-lookup"><span data-stu-id="03eeb-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="03eeb-129">Í þessu dæmi er mælt stofna verðeining fyrir Rosewood speaker cabinet ljúka valkost.</span><span class="sxs-lookup"><span data-stu-id="03eeb-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="03eeb-130">Veldu **Breyta ástandi**.</span><span class="sxs-lookup"><span data-stu-id="03eeb-130">Select **Edit condition**.</span></span> <span data-ttu-id="03eeb-131">Skilyrði verð hjálpar til við að tryggja samræmda segðareining verð er innifalinn í söluverði ef tiltekna samsetningu af eigindir eru til staðar.</span><span class="sxs-lookup"><span data-stu-id="03eeb-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="03eeb-132">Í reitinn **ConstraintBody** skal slá inn `CabinetFinish=="Rosewood"`.</span><span class="sxs-lookup"><span data-stu-id="03eeb-132">In the **ConstraintBody** field, enter `CabinetFinish=="Rosewood"`.</span></span>
7. <span data-ttu-id="03eeb-133">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="03eeb-133">Select **OK**.</span></span>
8. <span data-ttu-id="03eeb-134">Í reitinn **Segð** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="03eeb-134">In the **Expression** field, type a value.</span></span> <span data-ttu-id="03eeb-135">Til dæmis, slá inn `50`.</span><span class="sxs-lookup"><span data-stu-id="03eeb-135">For example, type `50`.</span></span> 
9. <span data-ttu-id="03eeb-136">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="03eeb-136">Close the page.</span></span>

