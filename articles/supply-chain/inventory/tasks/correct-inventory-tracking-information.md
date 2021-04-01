---
title: Leiðrétta birgðarakningarupplýsingar
description: Þetta ferli fer í gegnum ferlið fyrir stofnun og bókun á birgðaflutningabók til að leiðrétta rakningarupplýsingar birgða.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 76e73f10df5bb520b6d0d787eda08053a5e33c81
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223411"
---
# <a name="correct-inventory-tracking-information"></a><span data-ttu-id="3dd90-103">Leiðrétta birgðarakningarupplýsingar</span><span class="sxs-lookup"><span data-stu-id="3dd90-103">Correct inventory tracking information</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3dd90-104">Þetta ferli fer í gegnum ferlið fyrir stofnun og bókun á birgðaflutningabók til að leiðrétta rakningarupplýsingar birgða.</span><span class="sxs-lookup"><span data-stu-id="3dd90-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to correct inventory tracking information.</span></span> <span data-ttu-id="3dd90-105">Í þessu dæmi munum við að uppfæra upplýsingar runu sem stjórnað er af vöru með því að breyta ranglega skráð rununúmer í annarri runu.</span><span class="sxs-lookup"><span data-stu-id="3dd90-105">In this example, we'll update the information of a batch controlled item by changing an incorrectly registered batch to another batch.</span></span> <span data-ttu-id="3dd90-106">Hægt er að gilda með þessu ferli í sýnigögn gögn fyrirtækisins USPI eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="3dd90-106">You can walk through this procedure in demo data company USPI, or using your own data.</span></span> <span data-ttu-id="3dd90-107">Ef eigin gögn eru notuð, þarf að hafa vöru sem er runuvirkjaðir og það má ekki vera stjórnað úr staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="3dd90-107">If you use your own data, you need to have an item that's batch-enabled, and it must not be location-controlled.</span></span> <span data-ttu-id="3dd90-108">Þú þarft að hafa með heiti birgðabókarinnar sett upp fyrir birgðaflutning.</span><span class="sxs-lookup"><span data-stu-id="3dd90-108">You also need to have an inventory journal name set up for inventory transfers.</span></span> <span data-ttu-id="3dd90-109">Þessi verkefni eru venjulega framkvæmd af starfsmanni í vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="3dd90-109">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="3dd90-110">Stofna færslubóka fyrir birgðaflutning</span><span class="sxs-lookup"><span data-stu-id="3dd90-110">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="3dd90-111">Fara í Flutningi.</span><span class="sxs-lookup"><span data-stu-id="3dd90-111">Go to Transfer.</span></span>
2. <span data-ttu-id="3dd90-112">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="3dd90-112">Click New.</span></span>
3. <span data-ttu-id="3dd90-113">Sláið inn eða veldu gildi í reitnum heiti.</span><span class="sxs-lookup"><span data-stu-id="3dd90-113">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="3dd90-114">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="3dd90-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="3dd90-115">Stofna færslubókarlínur</span><span class="sxs-lookup"><span data-stu-id="3dd90-115">Create journal lines</span></span>
1. <span data-ttu-id="3dd90-116">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="3dd90-116">Click New.</span></span>
2. <span data-ttu-id="3dd90-117">Í reitinn Vörunúmer skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="3dd90-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="3dd90-118">Ef verið er að nota USPI, veljið M5003 vöru.</span><span class="sxs-lookup"><span data-stu-id="3dd90-118">If you are using USPI, select item M5003.</span></span>  
3. <span data-ttu-id="3dd90-119">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="3dd90-119">In the Quantity field, enter a number.</span></span>
4. <span data-ttu-id="3dd90-120">Smellið á flipann Birgðavíddir.</span><span class="sxs-lookup"><span data-stu-id="3dd90-120">Click the Inventory dimensions tab.</span></span>
5. <span data-ttu-id="3dd90-121">Sláðu inn eða veldu gildi í reitnum rununúmer.</span><span class="sxs-lookup"><span data-stu-id="3dd90-121">In the Batch number field, enter or select a value.</span></span>
6. <span data-ttu-id="3dd90-122">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="3dd90-122">In the Site field, enter or select a value.</span></span>
7. <span data-ttu-id="3dd90-123">Sláðu inn eða veldu gildi í reitnum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="3dd90-123">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="3dd90-124">Sláðu inn eða veldu gildi í reitnum rununúmer.</span><span class="sxs-lookup"><span data-stu-id="3dd90-124">In the Batch number field, enter or select a value.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="3dd90-125">Bóka færslubókina</span><span class="sxs-lookup"><span data-stu-id="3dd90-125">Post the journal</span></span>
1. <span data-ttu-id="3dd90-126">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="3dd90-126">Click Post.</span></span>
2. <span data-ttu-id="3dd90-127">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="3dd90-127">Click OK.</span></span>

## <a name="check-tracing-information"></a><span data-ttu-id="3dd90-128">Skoða upplýsingar um rakningu</span><span class="sxs-lookup"><span data-stu-id="3dd90-128">Check tracing information</span></span>
1. <span data-ttu-id="3dd90-129">Smellið á birgðir.</span><span class="sxs-lookup"><span data-stu-id="3dd90-129">Click Inventory.</span></span>
2. <span data-ttu-id="3dd90-130">Smellt er á Rakningu.</span><span class="sxs-lookup"><span data-stu-id="3dd90-130">Click Trace.</span></span>
3. <span data-ttu-id="3dd90-131">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="3dd90-131">Click OK.</span></span>
    * <span data-ttu-id="3dd90-132">með því að nota þessar upplýsingar rakningu er hægt rekja sig til baka í runu sem þú leiðréttir birgðir fyrir.</span><span class="sxs-lookup"><span data-stu-id="3dd90-132">Using this tracing information you can back trace which batch you corrected inventory from.</span></span>  <span data-ttu-id="3dd90-133">Einnig er hægt að nota síðuna rakningu Vöru til að skoða þessar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="3dd90-133">You can also use the Item tracing page to see this information.</span></span>  
4. <span data-ttu-id="3dd90-134">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3dd90-134">Close the page.</span></span>

## <a name="check-inventory-transactions"></a><span data-ttu-id="3dd90-135">Athuga Birgðafærslur</span><span class="sxs-lookup"><span data-stu-id="3dd90-135">Check inventory transactions</span></span>
1. <span data-ttu-id="3dd90-136">Smellið á birgðir.</span><span class="sxs-lookup"><span data-stu-id="3dd90-136">Click Inventory.</span></span>
2. <span data-ttu-id="3dd90-137">Smella á Færslur.</span><span class="sxs-lookup"><span data-stu-id="3dd90-137">Click Transactions.</span></span>
    * <span data-ttu-id="3dd90-138">Hér er hægt að sjá færslurnar sem voru stofnaðar þegar þitt færslubók var bókuð.</span><span class="sxs-lookup"><span data-stu-id="3dd90-138">Here you can see the transactions that were created when you posted your journal.</span></span>   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]