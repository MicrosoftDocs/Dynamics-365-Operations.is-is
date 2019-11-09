---
title: Skipta eign
description: Þetta efni útskýrir hvernig skal skipta hlutfalli einnar eignabókar á nýtt eignabók.
author: saraschi2
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4e001a6fdf390c6211ba85aa327b60dcdf16d9e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178253"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="5d5ed-103">Skipta eign</span><span class="sxs-lookup"><span data-stu-id="5d5ed-103">Split a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5d5ed-104">Þetta efni útskýrir hvernig skal skipta hlutfalli einnar eignabókar á nýtt eignabók.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="5d5ed-105">Það notar hlutverk Bókhaldara og sýnigögn USMF.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="5d5ed-106">Búa til nýja eign</span><span class="sxs-lookup"><span data-stu-id="5d5ed-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="5d5ed-107">Í skoðunarrúðnni ferðu í **Kerfseiningar > Fastafjármunir > Fastafjármunir > Fastafjármunir**.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="5d5ed-108">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-108">Select **New**.</span></span>
3. <span data-ttu-id="5d5ed-109">Í reitnum **Eignaflokkur** skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="5d5ed-110">Athugið númer eignar til að nota seinna í ferlinu skipta.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-110">Note the fixed asset number to use in the split process later.</span></span>  
4. <span data-ttu-id="5d5ed-111">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="5d5ed-112">Lokaðu skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="5d5ed-113">Skipta eign</span><span class="sxs-lookup"><span data-stu-id="5d5ed-113">Split a fixed asset</span></span>
1. <span data-ttu-id="5d5ed-114">Finna og veljið tengil í eignir sem skipta á í listanum.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-114">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="5d5ed-115">Veldu **Bækur**.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-115">Select **Books**.</span></span> <span data-ttu-id="5d5ed-116">Veljið bók til að skipta á nýju eignina.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-116">Select the book to split to the new asset.</span></span>  
3. <span data-ttu-id="5d5ed-117">Veljið **Aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-117">Select **Functions**.</span></span>
4. <span data-ttu-id="5d5ed-118">Velu **Skipta eign**.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-118">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="5d5ed-119">Sláðu inn eða veldu gildi í reitnum **Á eign**.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-119">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="5d5ed-120">Í reitnum **Til bókar** skal velja fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-120">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="5d5ed-121">Færa inn dagsetningu í reitinn **Færsludagsetning**.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-121">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="5d5ed-122">Færið inn tölu í reitnum **Prósenta**.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-122">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="5d5ed-123">Sláið inn eða veljið gildi í reitnum **Heiti færslubókar**.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-123">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="5d5ed-124">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-124">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="5d5ed-125">Bókið færslubókarfærsla.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-125">Post the journal transaction</span></span>
1. <span data-ttu-id="5d5ed-126">Í skoðunarrúðnni ferðu í **Kerfseiningar > Fastafjármunir > Dagbókarfærslur > Dagbók fastafjármuna**.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-126">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="5d5ed-127">Veljið færslubók sem er stofnuð með skipta ferlinu á listanum.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-127">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="5d5ed-128">Veldu **Línur**.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-128">Select **Lines**.</span></span>

    - <span data-ttu-id="5d5ed-129">Staðfestið stofnaðar færslubókarlínur .</span><span class="sxs-lookup"><span data-stu-id="5d5ed-129">Verify the journal lines created.</span></span>  
    - <span data-ttu-id="5d5ed-130">Leiðrétting kaupvirðisfærsla er stofnuð fyrir upprunalegu eignina til að minnka virði eftir prósentu sem tilgreind er við að skipta ferlinu.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-130">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  
    - <span data-ttu-id="5d5ed-131">Kaupfærsla er stofnuð fyrir nýju eignina fyrir sömu upphæð.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-131">An Acquisition transaction is created for the new asset for the same amount.</span></span>  

4. <span data-ttu-id="5d5ed-132">Veldu **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="5d5ed-132">Select **Post**.</span></span>
