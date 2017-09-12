--- 
title: Skipta eign
description: "Þessi leiðarvísi fyrir verk mun skipta hlutfall eitt eignabók á nýtt eignabók."
author: saraschi2
manager: AnnBe
ms.date: 10/19/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b4c1b39bcae1fa3830f3a217d1ad89e84cd72134
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="c4fa8-103">Skipta eign</span><span class="sxs-lookup"><span data-stu-id="c4fa8-103">Split a fixed asset</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c4fa8-104">Þessi leiðarvísi fyrir verk mun skipta hlutfall eitt eignabók á nýtt eignabók.</span><span class="sxs-lookup"><span data-stu-id="c4fa8-104">This task guide will split a percentage of one asset book to a new asset book.</span></span>  <span data-ttu-id="c4fa8-105">Það notar hlutverk Bókhaldara og sýnigögn USMF.</span><span class="sxs-lookup"><span data-stu-id="c4fa8-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="c4fa8-106">Búa til nýja eign</span><span class="sxs-lookup"><span data-stu-id="c4fa8-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="c4fa8-107">Fara í Eignir > Eignir > Eignir.</span><span class="sxs-lookup"><span data-stu-id="c4fa8-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="c4fa8-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="c4fa8-108">Click New.</span></span>
3. <span data-ttu-id="c4fa8-109">Færa inn eða veljið gildi í svæðinu eignaflokkur.</span><span class="sxs-lookup"><span data-stu-id="c4fa8-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="c4fa8-110">Athugið númer eignar til að nota seinna í ferlinu skipta.</span><span class="sxs-lookup"><span data-stu-id="c4fa8-110">Note the fixed asset number to use in the split process later.</span></span>
5. <span data-ttu-id="c4fa8-111">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="c4fa8-111">In the Name field, type a value.</span></span>
6. <span data-ttu-id="c4fa8-112">Lokaðu skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="c4fa8-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="c4fa8-113">Skipta eign</span><span class="sxs-lookup"><span data-stu-id="c4fa8-113">Split a fixed asset</span></span>
1. <span data-ttu-id="c4fa8-114">Finna og veljið eignir sem skipta á í listanum.</span><span class="sxs-lookup"><span data-stu-id="c4fa8-114">In the list, find and select the fixed asset to split.</span></span>
2. <span data-ttu-id="c4fa8-115">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="c4fa8-115">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="c4fa8-116">Smelltu á bækur.</span><span class="sxs-lookup"><span data-stu-id="c4fa8-116">Click Books.</span></span>
    * <span data-ttu-id="c4fa8-117">Veljið bók til að skipta á nýju eignina.</span><span class="sxs-lookup"><span data-stu-id="c4fa8-117">Select the book to split to the new asset.</span></span>  
4. <span data-ttu-id="c4fa8-118">Smellið á Aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="c4fa8-118">Click Functions.</span></span>
5. <span data-ttu-id="c4fa8-119">Smellt er á skipta Eign.</span><span class="sxs-lookup"><span data-stu-id="c4fa8-119">Click Split fixed asset.</span></span>
6. <span data-ttu-id="c4fa8-120">Sláðu inn eða veldu gildi í reitnum Á eign.</span><span class="sxs-lookup"><span data-stu-id="c4fa8-120">In the To fixed asset field, enter or select a value.</span></span>
7. <span data-ttu-id="c4fa8-121">Í reitnum Á bók skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="c4fa8-121">In the To book field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="c4fa8-122">Færa inn dagsetningu í dagsetningarsvæði Færslunnar.</span><span class="sxs-lookup"><span data-stu-id="c4fa8-122">In the Transaction date field, enter a date.</span></span>
9. <span data-ttu-id="c4fa8-123">Færið inn tölu í svæðinu prósenta.</span><span class="sxs-lookup"><span data-stu-id="c4fa8-123">In the Percent field, enter a number.</span></span>
10. <span data-ttu-id="c4fa8-124">Sláið inn eða veljið gildi í reitnum heiti færslubókar.</span><span class="sxs-lookup"><span data-stu-id="c4fa8-124">In the Journal name field, enter or select a value.</span></span>
11. <span data-ttu-id="c4fa8-125">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c4fa8-125">Click OK.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="c4fa8-126">Bókið færslubókarfærsla.</span><span class="sxs-lookup"><span data-stu-id="c4fa8-126">Post the journal transaction</span></span>
1. <span data-ttu-id="c4fa8-127">Fara í Eignir >°Færslubókarfærslur°> Eignabók.</span><span class="sxs-lookup"><span data-stu-id="c4fa8-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="c4fa8-128">Veljið færslubók sem er stofnuð með skipta ferlinu á listanum.</span><span class="sxs-lookup"><span data-stu-id="c4fa8-128">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="c4fa8-129">Smellið á „Línur“.</span><span class="sxs-lookup"><span data-stu-id="c4fa8-129">Click Lines.</span></span>
    * <span data-ttu-id="c4fa8-130">Staðfestið stofnaðar færslubókarlínur .</span><span class="sxs-lookup"><span data-stu-id="c4fa8-130">Verify the journal lines created.</span></span>  <span data-ttu-id="c4fa8-131">Leiðrétting kaupvirðisfærsla er stofnuð fyrir upprunalegu eignina til að minnka virði eftir prósentu sem tilgreind er við að skipta ferlinu.</span><span class="sxs-lookup"><span data-stu-id="c4fa8-131">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  <span data-ttu-id="c4fa8-132">Kaupfærsla er stofnuð fyrir nýju eignina fyrir sömu upphæð.</span><span class="sxs-lookup"><span data-stu-id="c4fa8-132">An Acquisition transaction is created for the new asset for the same amount.</span></span>  
4. <span data-ttu-id="c4fa8-133">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="c4fa8-133">Click Post.</span></span>


