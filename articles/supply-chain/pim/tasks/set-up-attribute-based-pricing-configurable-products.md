--- 
title: "Setja upp verð sem byggir á eigindum fyrir skilgreinanlegar afurðir"
description: "Þessi verklýsing sýnir hvernig á að setja upp eigindabyggða úthlutun."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 8568b5f4933ae58bc2d55a169c798668e03bed2a
ms.contentlocale: is-is
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="a8557-103">Setja upp verð sem byggir á eigindum fyrir skilgreinanlegar afurðir</span><span class="sxs-lookup"><span data-stu-id="a8557-103">Set up attribute-based pricing for configurable products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a8557-104">Þessi verklýsing sýnir hvernig á að setja upp eigindabyggða úthlutun.</span><span class="sxs-lookup"><span data-stu-id="a8557-104">This procedure shows how to set up attribute-based pricing.</span></span> <span data-ttu-id="a8557-105">Sem skilyrði, verður að hafa afbrigðalíkan afurðar sem hefur eitt eða fleiri íhluti og eiginleika.</span><span class="sxs-lookup"><span data-stu-id="a8557-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="a8557-106">Þessi aðferð notar hágæða hátalara líkanið gögn fyrirtækisins sýnigögn USMF.</span><span class="sxs-lookup"><span data-stu-id="a8557-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="a8557-107">Venjulega notar framleiðslustjóri þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="a8557-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="a8557-108">Búa til nýtt verðlíkan</span><span class="sxs-lookup"><span data-stu-id="a8557-108">Create a new price model</span></span>
1. <span data-ttu-id="a8557-109">Smellið á Skilgreining afurðarafbrigðislíkans</span><span class="sxs-lookup"><span data-stu-id="a8557-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="a8557-110">Smella á Afbrigðalíkan afurðar</span><span class="sxs-lookup"><span data-stu-id="a8557-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="a8557-111">Á listanum velurðu línuna fyrir hágæða hátalara, en smelltu ekki á tengilinn fyrir heitið.</span><span class="sxs-lookup"><span data-stu-id="a8557-111">In the list, select the High End Speaker line, but don’t click the link for the name.</span></span>
4. <span data-ttu-id="a8557-112">Í aðgerðasvæðinu er smellt á líkan.</span><span class="sxs-lookup"><span data-stu-id="a8557-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="a8557-113">Smelltu á Söluverðslíkön.</span><span class="sxs-lookup"><span data-stu-id="a8557-113">Click Price models.</span></span>
6. <span data-ttu-id="a8557-114">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="a8557-114">Click New.</span></span>
7. <span data-ttu-id="a8557-115">Sláið inn gildi í reitinn Verðlíkan.</span><span class="sxs-lookup"><span data-stu-id="a8557-115">In the Price model name field, type a value.</span></span>
    * <span data-ttu-id="a8557-116">Notið nafn sem gerir auðvelt að bera kennsl á líkan.</span><span class="sxs-lookup"><span data-stu-id="a8557-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="a8557-117">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="a8557-117">In the Description field, type a value.</span></span>
9. <span data-ttu-id="a8557-118">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="a8557-118">Click Save.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="a8557-119">Bæta við verðeiningum</span><span class="sxs-lookup"><span data-stu-id="a8557-119">Add price elements</span></span>
1. <span data-ttu-id="a8557-120">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="a8557-120">Click Edit.</span></span>
    * <span data-ttu-id="a8557-121">Hver íhlutur í framleiðslulíkani getur haft grunnverð einingu og fjölda verðsegðarreglna.</span><span class="sxs-lookup"><span data-stu-id="a8557-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="a8557-122">Einnig er hægt að bæta verði í mismunandi gjaldmiðlum.</span><span class="sxs-lookup"><span data-stu-id="a8557-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="a8557-123">Í reitinn Svæði grunnverðs skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="a8557-123">In the Base price expression field, type a value.</span></span>
    * <span data-ttu-id="a8557-124">Til dæmis, skrifið 100.</span><span class="sxs-lookup"><span data-stu-id="a8557-124">For example, type 100.</span></span>   <span data-ttu-id="a8557-125">Grunnverðssegð getur verið tölugildi eða það getur verið samsett af útreikningi sem felur í sér eina eða fleiri eigindir.</span><span class="sxs-lookup"><span data-stu-id="a8557-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="a8557-126">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="a8557-126">Click Add.</span></span>
4. <span data-ttu-id="a8557-127">I retinum skal færa inn ‚Rosewood‘.</span><span class="sxs-lookup"><span data-stu-id="a8557-127">In the Name field, type ‘Rosewood’.</span></span>
    * <span data-ttu-id="a8557-128">Nafn verð segð gerir auðveldara að verð einingarinnar sem stendur.</span><span class="sxs-lookup"><span data-stu-id="a8557-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="a8557-129">Í þessu dæmi er mælt stofna verðeining fyrir Rosewood speaker cabinet ljúka valkost.</span><span class="sxs-lookup"><span data-stu-id="a8557-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="a8557-130">Breyta skilyrði.</span><span class="sxs-lookup"><span data-stu-id="a8557-130">Click Edit condition.</span></span>
    * <span data-ttu-id="a8557-131">Skilyrði verð hjálpar til við að tryggja samræmda segðareining verð er innifalinn í söluverði ef tiltekna samsetningu af eigindir eru til staðar.</span><span class="sxs-lookup"><span data-stu-id="a8557-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="a8557-132">Í reitnum ConstraintBody skal slá inn 'CabinetFinish=="Rosewood"'.</span><span class="sxs-lookup"><span data-stu-id="a8557-132">In the ConstraintBody field, enter 'CabinetFinish=="Rosewood"'.</span></span>
7. <span data-ttu-id="a8557-133">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a8557-133">Click OK.</span></span>
8. <span data-ttu-id="a8557-134">Í reitinn Framsetning skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="a8557-134">In the Expression field, type a value.</span></span>
    * <span data-ttu-id="a8557-135">Til dæmis, skrifið 50.</span><span class="sxs-lookup"><span data-stu-id="a8557-135">For example, type 50.</span></span>  
9. <span data-ttu-id="a8557-136">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a8557-136">Close the page.</span></span>
10. <span data-ttu-id="a8557-137">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a8557-137">Close the page.</span></span>


