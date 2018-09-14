--- 
title: Setja upp reglur fyrir stigveldi innkaupategunda
description: "Notið þetta ferli til að setja upp reglur til þess að panta afurðir í tegund."
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage, SysPolicy, ProcCategoryAccessPolicyRule, ProcCategoryPolicyRule, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: d1fdf357466de12bd0188fc43cd266c67af762c7
ms.contentlocale: is-is
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a><span data-ttu-id="291a6-103">Setja upp reglur fyrir stigveldi innkaupategunda</span><span class="sxs-lookup"><span data-stu-id="291a6-103">Set up policies for procurement category hierarchies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="291a6-104">Notið þetta ferli til að setja upp reglur til þess að panta afurðir í tegund.</span><span class="sxs-lookup"><span data-stu-id="291a6-104">Use this procedure to set up rules for ordering products in a category.</span></span> <span data-ttu-id="291a6-105">Þessar reglur eru skilgreindar fyrir tiltekna innkaupastefnu.</span><span class="sxs-lookup"><span data-stu-id="291a6-105">The rules are defined for a specific purchasing policy.</span></span> <span data-ttu-id="291a6-106">Regla tegundaraðgangs ákvarðar hvaða innkaupategundir starfsmenn hafa aðgang að þegar þeir stofna beiðnir.</span><span class="sxs-lookup"><span data-stu-id="291a6-106">The category access rule controls which procurement categories employees have access to when they create a requisition.</span></span> <span data-ttu-id="291a6-107">Þegar beiðni er stofnuð skal innkaupastefnu og reglu tegundaraðgangs sem á að nota vera ákvörðuð af lögaðilanum og rekstrareiningum sem starfsmaðurinn tilheyrir.</span><span class="sxs-lookup"><span data-stu-id="291a6-107">When a requisition is being created, the purchasing policy and category access rule that should be applied are determined by the legal entity and the operational unit that the employee belongs to.</span></span> <span data-ttu-id="291a6-108">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="291a6-108">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="291a6-109">Þetta verk myndi venjulega vera framkvæmt af innkaupaaðila.</span><span class="sxs-lookup"><span data-stu-id="291a6-109">This task would typically be carried out by a purchasing manager.</span></span>


## <a name="find-the-procurement-policy"></a><span data-ttu-id="291a6-110">Finna innkaupareglu</span><span class="sxs-lookup"><span data-stu-id="291a6-110">Find the procurement policy</span></span>
1. <span data-ttu-id="291a6-111">Fara í Innkaup og uppruni > Uppsetning > reglur > innkaupareglur.</span><span class="sxs-lookup"><span data-stu-id="291a6-111">Go to Procurement and sourcing > Setup > Policies > Purchasing policies.</span></span>
2. <span data-ttu-id="291a6-112">Smelltu á tengil á innkaupastefnu USMF-stefna.</span><span class="sxs-lookup"><span data-stu-id="291a6-112">Click the link on the Procurement Policy USMF policy.</span></span>
    * <span data-ttu-id="291a6-113">Þetta er reglan sem þú bætir reglu við.</span><span class="sxs-lookup"><span data-stu-id="291a6-113">This is the policy that you’ll add a rule to.</span></span> <span data-ttu-id="291a6-114">Hún verður að vera Virk regla.</span><span class="sxs-lookup"><span data-stu-id="291a6-114">It must be an Active policy.</span></span>  

## <a name="create-a-category-access-rule"></a><span data-ttu-id="291a6-115">Búa til reglu tegundaraðgangs</span><span class="sxs-lookup"><span data-stu-id="291a6-115">Create a category access rule</span></span>
1. <span data-ttu-id="291a6-116">Veldu Stefnuregla tegundaraðgangs</span><span class="sxs-lookup"><span data-stu-id="291a6-116">Select the Category access policy rule.</span></span>
    * <span data-ttu-id="291a6-117">Ef hnappur til að stofna stefnureglu er deyfður er það vegna þess að þegar er til staðar virk stefnuregla fyrir tegundaraðgang.</span><span class="sxs-lookup"><span data-stu-id="291a6-117">If the Create policy rule button is dimmed, it’s because there’s already an active policy rule for Category access.</span></span> <span data-ttu-id="291a6-118">Athuga dagsetningasvæði Virkrar dagsetningar og Lokadags til að ákvarða hvaða það er, svo velja hana og smella á hætta Við stefnureglu.</span><span class="sxs-lookup"><span data-stu-id="291a6-118">Check the Effective and Expiration date fields to determine which it is, then select it, and click Retire policy rule.</span></span> <span data-ttu-id="291a6-119">Ef Stofna stefnureglu hnappur er tiltækur, þarf ekki að gera neitt.</span><span class="sxs-lookup"><span data-stu-id="291a6-119">If the Create policy rule button is available, you don’t need to do anything.</span></span>  
2. <span data-ttu-id="291a6-120">Smellt er á Stofna stefnureglu.</span><span class="sxs-lookup"><span data-stu-id="291a6-120">Click Create policy rule.</span></span>
3. <span data-ttu-id="291a6-121">Færa inn dagsetningu og tíma í svæðinu gildisdagsetningu.</span><span class="sxs-lookup"><span data-stu-id="291a6-121">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="291a6-122">Tíminn má ekki skarast við aðra reglu sem er þegar virk.</span><span class="sxs-lookup"><span data-stu-id="291a6-122">The time must not overlap with another rule that’s already active.</span></span>  
    * <span data-ttu-id="291a6-123">Velja tegund sem reglan mun eiga við.</span><span class="sxs-lookup"><span data-stu-id="291a6-123">Select a category that the rule will apply to.</span></span> <span data-ttu-id="291a6-124">Taka niður athugasemd um það hvaða tegund þetta er – þú þarf hana síðar.</span><span class="sxs-lookup"><span data-stu-id="291a6-124">Make a note of which category this is – you’ll need it later.</span></span> <span data-ttu-id="291a6-125">Þegar flokkur er valinn, eru yfirflokkar eða yfirflokkur einnig settir á valinn tegundaalista.</span><span class="sxs-lookup"><span data-stu-id="291a6-125">When you select a category, its parent category or categories will also be added to the Selected categories list.</span></span>  
    * <span data-ttu-id="291a6-126">Viljirðu að reglan eigi við allar undirtegundir valinnar tegundar, Velja Innifela undirtegundir valkostinn.</span><span class="sxs-lookup"><span data-stu-id="291a6-126">If you want the rule to apply to all subcategories of the selected category, select the Include subcategories check box.</span></span>  
4. <span data-ttu-id="291a6-127">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="291a6-127">Click Add.</span></span>
    * <span data-ttu-id="291a6-128">Ef þú stillir valkostinn yfirskipuð regla á Já, er Stefnureglun sem skilgreind er fyrir yfirtegund er einnig úthlutað til baka í undirtegundir ef engin stefnuregla hefur verið skilgreind fyrir undirtegundir.</span><span class="sxs-lookup"><span data-stu-id="291a6-128">If you set the Include parent rule option to Yes, the policy rule that you define for a parent category is also assigned to its child categories, if no policy rule has been defined for the child categories.</span></span>  
5. <span data-ttu-id="291a6-129">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="291a6-129">Click OK.</span></span>

## <a name="create-a-category-policy-rule"></a><span data-ttu-id="291a6-130">Búa til tegundarstefnureglu</span><span class="sxs-lookup"><span data-stu-id="291a6-130">Create a category policy rule</span></span>
1. <span data-ttu-id="291a6-131">Veldu Stefnuregla tegundar</span><span class="sxs-lookup"><span data-stu-id="291a6-131">Select the Category policy rule</span></span>
    * <span data-ttu-id="291a6-132">Ef hnappinn Stofna stefnureglu er deyfður, skal velja virka stefnureglu og smella á hætta Við stefnureglu.</span><span class="sxs-lookup"><span data-stu-id="291a6-132">If the Create policy rule button is dimmed, select the active policy rule, and then click Retire policy rule.</span></span>  
2. <span data-ttu-id="291a6-133">Smellt er á Stofna stefnureglu.</span><span class="sxs-lookup"><span data-stu-id="291a6-133">Click Create policy rule.</span></span>
3. <span data-ttu-id="291a6-134">Færa inn dagsetningu og tíma í svæðinu gildisdagsetningu.</span><span class="sxs-lookup"><span data-stu-id="291a6-134">In the Effective date field, enter a date and time.</span></span>
4. <span data-ttu-id="291a6-135">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="291a6-135">Click Add.</span></span>
5. <span data-ttu-id="291a6-136">Veljið sömu tegund sem notuð var fyrir reglu tegundaraðgangs.</span><span class="sxs-lookup"><span data-stu-id="291a6-136">Select the same category that you used for the Category access rule.</span></span>
6. <span data-ttu-id="291a6-137">Í reitnum Velja lánardrottin, skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="291a6-137">In the Vendor selection field, select an option.</span></span>
    * <span data-ttu-id="291a6-138">Velja reglu til að stjórna hvers konar lánardrottna má velja fyrir flokkinn þegar beiðnir eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="291a6-138">Select a rule to control which kind of vendors can be selected for the category when requisitions are created.</span></span>  
7. <span data-ttu-id="291a6-139">Smellið á „Loka“.</span><span class="sxs-lookup"><span data-stu-id="291a6-139">Click Close.</span></span>
    * <span data-ttu-id="291a6-140">Þær stefnureglur sem skilgreindar hafa verið hafaverið fyrir beiðnir af gerðinni notkun.</span><span class="sxs-lookup"><span data-stu-id="291a6-140">The policy rules that you have defined have been for requisitions of type Consumption.</span></span> <span data-ttu-id="291a6-141">Ef óskað er að skilgreina reglur fyrir beiðnir af gerðinni Áfylling, myndirðu stofna regla fyrir stefnureglugerð sem kallast "Stefnuregla tegundaraðgangs fyrir áfyllingu".</span><span class="sxs-lookup"><span data-stu-id="291a6-141">If you wanted to define policies for requisitions of type Replenishment, you would create a rule for the Policy rule type called “Replenishment category access policy rule”.</span></span>  


