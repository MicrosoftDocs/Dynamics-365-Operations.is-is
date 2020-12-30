---
title: Stofna innkaupastefnu
description: Þetta efni sýnir hvernig á að stofna innkaupareglur til samræmis við viðskiptaferli þín fyrir innkaup.
author: mkirknel
manager: tfehr
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicyParameters, SysPolicy, RequisitionPurposeRule
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d4ba2a23f84972391283eaf01cef70a161c75226
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430273"
---
# <a name="create-purchasing-policies"></a><span data-ttu-id="48b30-103">Stofna innkaupastefnu</span><span class="sxs-lookup"><span data-stu-id="48b30-103">Create purchasing policies</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="48b30-104">Þetta efni sýnir hvernig á að stofna innkaupareglur til samræmis við viðskiptaferli þín fyrir innkaup.</span><span class="sxs-lookup"><span data-stu-id="48b30-104">This topic shows you how to create purchasing policies to align with your business processes for purchasing.</span></span> <span data-ttu-id="48b30-105">Áður en hægt er að stofna innkaupastefnur þarf að setja upp færibreytur fyrir innkaupastefnu.</span><span class="sxs-lookup"><span data-stu-id="48b30-105">Before you can create purchasing policies, you must set up the purchasing policy parameters.</span></span> <span data-ttu-id="48b30-106">Hægt er að stofna, breyta og hætta við innkaupastefnu en ekki er hægt að eyða innkaupastefnu.</span><span class="sxs-lookup"><span data-stu-id="48b30-106">It's possible to create, modify, and retire a purchasing policy, but you can't delete a purchasing policy.</span></span> <span data-ttu-id="48b30-107">Þetta verk myndi venjulega vera framkvæmt af innkaupaaðila.</span><span class="sxs-lookup"><span data-stu-id="48b30-107">This procedure would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="48b30-108">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="48b30-108">You can use this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-policy-parameters"></a><span data-ttu-id="48b30-109">Setja upp færibreytur reglna</span><span class="sxs-lookup"><span data-stu-id="48b30-109">Set up policy parameters</span></span>
1. <span data-ttu-id="48b30-110">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Innkaup og aðföng > Uppsetning > Reglur > Innkaupareglur**.</span><span class="sxs-lookup"><span data-stu-id="48b30-110">In the navigation pane, go to **Modules > Procurement and sourcing > Setup > Policies > Purchasing policies**.</span></span>
2. <span data-ttu-id="48b30-111">Á aðgerðasvæðinu skal velja **Færibreytur**.</span><span class="sxs-lookup"><span data-stu-id="48b30-111">On the Action Pane, select **Parameters**.</span></span>
- <span data-ttu-id="48b30-112">Reglugerðir um forgang eiga við um mismunandi stig innan fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="48b30-112">Policy precedence rules apply to different levels in your organization.</span></span> <span data-ttu-id="48b30-113">Skipulagseiningar sem eru sýndar fara eftir því stigveldi fyrirtækis og á hvaða stigi í stigveldi er búið að úthluta tilgangi fyrir innra eftirlit innkaupa.</span><span class="sxs-lookup"><span data-stu-id="48b30-113">The organizational units that are shown depend on your organizational hierarchy, and on which levels in the hierarchy have been assigned the purpose of Procurement internal control.</span></span> <span data-ttu-id="48b30-114">Til dæmis, gæti fyrirtækið verið með lögaðila, kostnaðarstaði, svæði og deildir, en hugsanlega er aðeins sumar þessara eininga með tilgang stigveldis fyrir innra eftirlit innkaupa.</span><span class="sxs-lookup"><span data-stu-id="48b30-114">For example, your organization might have legal entities, cost centers, regions, and departments, but it may be that only some of these have a hierarchy purpose of Procurement internal control.</span></span> <span data-ttu-id="48b30-115">Sjálfgefið er að fyrirtækisins af gerðinni Fyrirtæki tiltæk.</span><span class="sxs-lookup"><span data-stu-id="48b30-115">As a default, the organization of type Company is available.</span></span>  
3. <span data-ttu-id="48b30-116">Veldu flipann **Færibreytur stefnureglugerðar**.</span><span class="sxs-lookup"><span data-stu-id="48b30-116">Select the **Policy rule type parameters** tab.</span></span>
4. <span data-ttu-id="48b30-117">Í trénu ferðu í **Innkaupastefna > Stjórnunarregla innkaupastefnu**.</span><span class="sxs-lookup"><span data-stu-id="48b30-117">In the tree, go to **Purchasing policy > Purchase requisition control rule**.</span></span>
- <span data-ttu-id="48b30-118">Er forgangsröð er skilgreind fyrir lausn reglu á reglustigi.</span><span class="sxs-lookup"><span data-stu-id="48b30-118">You define the order of precedence for policy resolution at the policy level.</span></span> <span data-ttu-id="48b30-119">Hins vegar er hægt að hnekkja forgangsröð einstaka stefnureglugerða fyrir sumar gerðir reglna.</span><span class="sxs-lookup"><span data-stu-id="48b30-119">However, for some policy types, you can override the order of precedence for individual policy rule types.</span></span> <span data-ttu-id="48b30-120">Til dæmis mætti skilgreina forgangsröð fyrir innkaupastefnur í þessari röð: kostnaðarstaður, deild, fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="48b30-120">For example, you might define the order of precedence for purchasing policies to be: cost center, department, company.</span></span> <span data-ttu-id="48b30-121">Fyrir stefnureglu vörulista viltu kannski hafa forgangsröð: deild, kostnaðarstaður, fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="48b30-121">For the catalog policy rule, you might want the order of precedence to be: department, cost center, company.</span></span> <span data-ttu-id="48b30-122">Forgangsröð má breyta fyrir stefnureglu vörulista.</span><span class="sxs-lookup"><span data-stu-id="48b30-122">You can change the order of precedence for the Catalog policy rule.</span></span> <span data-ttu-id="48b30-123">Þegar starfsmaður stofnar beiðni, er vörulistinn sem birtist ákvarðaður af reglunum sem tengjast deild starfsmannsins, síðan kostnaðarstað hans og svo fyrirtæki hans.</span><span class="sxs-lookup"><span data-stu-id="48b30-123">When a worker creates a requisition, the catalog that is displayed is determined by the policies that are associated with the worker's department, then their cost center, and then their company.</span></span>  
- <span data-ttu-id="48b30-124">Ef meira en eitt stjórnunarstig er skráð er hægt að nota örvarnar Upp/Niður til að stilla forgangsröð fyrir reglu innkaupapantanastýringar.</span><span class="sxs-lookup"><span data-stu-id="48b30-124">If there's more than one organizational level listed, you can use the Up/Down arrows to set the order of precedence for the Purchase requisition control rule.</span></span>  
5. <span data-ttu-id="48b30-125">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="48b30-125">Close the page.</span></span>

## <a name="create-a-new-policy"></a><span data-ttu-id="48b30-126">Stofna nýja reglu</span><span class="sxs-lookup"><span data-stu-id="48b30-126">Create a new policy</span></span>
1. <span data-ttu-id="48b30-127">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="48b30-127">Select **New**.</span></span>
2. <span data-ttu-id="48b30-128">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="48b30-128">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="48b30-129">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="48b30-129">In the **Description** field, type a value.</span></span>
- <span data-ttu-id="48b30-130">Stök innkaupastefna geta átt aðeins við um eitt stigveldi fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="48b30-130">A single purchasing policy can only apply to one organization hierarchy.</span></span> <span data-ttu-id="48b30-131">Til dæmis gæti eitt stigveldi kallast "landsvæði" og annað kallast "deild" og hvort þeirra haft með mismunandi innkaupastefna.</span><span class="sxs-lookup"><span data-stu-id="48b30-131">For example, you could have one hierarchy called "Geographic" and one called "Department", and have a different purchasing policy for each.</span></span>  
- <span data-ttu-id="48b30-132">Veljið fyrirtæki sem stefnan á við.</span><span class="sxs-lookup"><span data-stu-id="48b30-132">Select an organization that the policy should apply to.</span></span>  
4. <span data-ttu-id="48b30-133">Veldu örina til að bæta við völdu fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="48b30-133">Select the arrow to add the selected organization.</span></span>
- <span data-ttu-id="48b30-134">Hægt er að endurtaka þetta ferli til að bæta við fleiri fyrirtækjum.</span><span class="sxs-lookup"><span data-stu-id="48b30-134">You can repeat this process to add more organizations.</span></span>  

## <a name="add-a-policy-rule"></a><span data-ttu-id="48b30-135">Bæta við stefnureglu</span><span class="sxs-lookup"><span data-stu-id="48b30-135">Add a policy rule</span></span>
1. <span data-ttu-id="48b30-136">Á listanum **Stefnureglugerð**, velurðu **Málefnisregla beiðni**.</span><span class="sxs-lookup"><span data-stu-id="48b30-136">In the **Policy rule type** list, select **Requisition purpose rule**.</span></span>
- <span data-ttu-id="48b30-137">Þú stofnar reglu sem stillir sjálfgefinn tilgang beiðni á gerðina Notkun en heimilar að velja í staðinn áfyllingargerð.</span><span class="sxs-lookup"><span data-stu-id="48b30-137">You'll create a rule that sets the default requisition purpose to type Consumption but allows the Replenishment type to be selected instead.</span></span>  
2. <span data-ttu-id="48b30-138">Veldu **stefnureglu**.</span><span class="sxs-lookup"><span data-stu-id="48b30-138">Select **Create policy rule**.</span></span>
3. <span data-ttu-id="48b30-139">Velja skal **Já** í reitnum **Leyfa handvirka hnekkingu**.</span><span class="sxs-lookup"><span data-stu-id="48b30-139">Select **Yes** in the **Allow manual override** field.</span></span>
4. <span data-ttu-id="48b30-140">Veljið **Loka**.</span><span class="sxs-lookup"><span data-stu-id="48b30-140">Select **Close**.</span></span>
- <span data-ttu-id="48b30-141">Núna er hægt að setja upp aðrar stefnureglur fyrir innkaupastefnu.</span><span class="sxs-lookup"><span data-stu-id="48b30-141">Now you can set up other policy rules for the purchasing policy.</span></span> <span data-ttu-id="48b30-142">Athugið að stefnureglugerð getur ekki haft reglur um skörun sem eru virkar á sama tíma innan einnar innkaupastefnu.</span><span class="sxs-lookup"><span data-stu-id="48b30-142">Note that a Policy rule type cannot have overlapping rules that are active at the same time within a single procurement policy.</span></span>  

