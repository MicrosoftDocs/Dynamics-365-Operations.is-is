--- 
title: "Uppsetning afskriftabóka "
description: "Þessi leiðarvísi fyrir verk stofna nýja afskriftabók og tengja hana við eignaflokk."
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3e2c3bfdde6fd06bfe9e22f215f691e0c92fa8ee
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="set-up-depreciation-books"></a><span data-ttu-id="1645e-103">Uppsetning afskriftabóka </span><span class="sxs-lookup"><span data-stu-id="1645e-103">Set up depreciation books</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1645e-104">Þessi leiðarvísi fyrir verk stofna nýja afskriftabók og tengja hana við eignaflokk.</span><span class="sxs-lookup"><span data-stu-id="1645e-104">This task guide will create a new depreciation book and associate it with a fixed asset group.</span></span>  <span data-ttu-id="1645e-105">Það notar Bókari hlutverk og sýnigögn fyrir USMF lögaðila.</span><span class="sxs-lookup"><span data-stu-id="1645e-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-depreciation-book"></a><span data-ttu-id="1645e-106">Stofna afskriftarbók</span><span class="sxs-lookup"><span data-stu-id="1645e-106">Create a depreciation book</span></span>
1. <span data-ttu-id="1645e-107">Fara í Eignir > Uppsetning > Afskriftarbækur.</span><span class="sxs-lookup"><span data-stu-id="1645e-107">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="1645e-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="1645e-108">Click New.</span></span>
3. <span data-ttu-id="1645e-109">Færa inn gildi í svæðinu afskriftarbók.</span><span class="sxs-lookup"><span data-stu-id="1645e-109">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="1645e-110">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="1645e-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1645e-111">Merkja eða afmerkja gátreit Reikna afskrift.</span><span class="sxs-lookup"><span data-stu-id="1645e-111">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="1645e-112">Í reitnum afskriftarregla skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="1645e-112">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="1645e-113">Í listanum skal finna og velja þá afskriftarregla sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="1645e-113">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="1645e-114">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="1645e-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="1645e-115">Í reitnum önnur afskriftarregla skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="1645e-115">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="1645e-116">Á listanum, skal velja viðeigandi afskriftarregla.</span><span class="sxs-lookup"><span data-stu-id="1645e-116">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="1645e-117">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="1645e-117">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1645e-118">Óregluleg afskriftaregla er notuð fyrir aukalega afskrift af eign við óvenjulegar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="1645e-118">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="1645e-119">Til dæmis er hægt að nota þetta til að skrá niðurstöður úr náttúruhamfarir afskrift.</span><span class="sxs-lookup"><span data-stu-id="1645e-119">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="1645e-120">Merkja eða afmerkja gátreit Stofna afskriftaleiðréttingar með grunnleiðréttingar .</span><span class="sxs-lookup"><span data-stu-id="1645e-120">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="1645e-121">Í reitnum dagatal skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="1645e-121">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="1645e-122">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="1645e-122">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="1645e-123">Tengið afskriftarbók við eignaflokkur</span><span class="sxs-lookup"><span data-stu-id="1645e-123">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="1645e-124">Smella á eignaflokkar.</span><span class="sxs-lookup"><span data-stu-id="1645e-124">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="1645e-125">Í reitnum eignaflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="1645e-125">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="1645e-126">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="1645e-126">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="1645e-127">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="1645e-127">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="1645e-128">Veljið valkost í svæðinu afskriftarregla.</span><span class="sxs-lookup"><span data-stu-id="1645e-128">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="1645e-129">Í reitinn líftími skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="1645e-129">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="1645e-130">Sjáðu að svæðisgildi afskriftartímabils er reiknaður eftir uppsetningu líftíma.</span><span class="sxs-lookup"><span data-stu-id="1645e-130">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  


