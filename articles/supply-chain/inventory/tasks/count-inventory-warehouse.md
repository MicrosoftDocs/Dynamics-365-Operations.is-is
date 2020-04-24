---
title: Telja birgðir í vöruhúsi
description: Þetta efni lýsir ferlinu við stofnun og bókun birgðatalningabók til að telja tiltekna vöru á staðsetningu í vöruhúsinu.
author: MarkusFogelberg
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 34013783bab79d80f1dac9a7806042608635e617
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204172"
---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="f2742-103">Telja birgðir í vöruhúsi</span><span class="sxs-lookup"><span data-stu-id="f2742-103">Count inventory in a warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f2742-104">Þetta efni lýsir ferlinu við stofnun og bókun birgðatalningabók til að telja tiltekna vöru á staðsetningu í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="f2742-104">This topic describes the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="f2742-105">Ferlið á við virkni „grunnvöruhúss”, sem er tiltækt í birgðastjórnunareiningunni, ekki við vöruhúsavirknina sem er tiltæk í kerfiseiningunni vöruhúsakerfi.</span><span class="sxs-lookup"><span data-stu-id="f2742-105">The procedure applies to "basic warehousing" functionality, available in the Inventory management module, not to the warehousing functionality that's available in the Warehouse management module.</span></span> <span data-ttu-id="f2742-106">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="f2742-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="f2742-107">Ef verið er að nota eigin gögn, tryggja þarf afurðir og staðsetningar eru uppsettar og að hefur verið stofnað heiti birgðabókar fyrir talningarbækur.</span><span class="sxs-lookup"><span data-stu-id="f2742-107">If you're using your own data, make sure that you have products and locations set up, and that you've created an inventory journal name for counting journals.</span></span> <span data-ttu-id="f2742-108">Birgðatalning er yfirleitt framkvæmd af starfsmanni í vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="f2742-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="f2742-109">Stofna færslubóka fyrir birgðatalningu</span><span class="sxs-lookup"><span data-stu-id="f2742-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="f2742-110">Farðu í **Skoðunarrúða > Kerfi > Birgðastjórnun > Bókarfærslur > Vörutalning > Talning**.</span><span class="sxs-lookup"><span data-stu-id="f2742-110">Go to **Navigation pane > Modules > Inventory management > Journal entries > Item counting > Counting**.</span></span>
2. <span data-ttu-id="f2742-111">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="f2742-111">Select **New**.</span></span>
3. <span data-ttu-id="f2742-112">Í reitnum **Heiti** skaltu velja það dagbókarheiti birgðatalningar sem þú vilt nota af fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="f2742-112">In the **Name** field, select the inventory counting journal name you want to use from the drop-down list.</span></span> <span data-ttu-id="f2742-113">Sum svæði er fyllt út samkvæmt uppsetningu heitis birgðatalningabókar sem er valin.</span><span class="sxs-lookup"><span data-stu-id="f2742-113">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
4. <span data-ttu-id="f2742-114">Í reitnum **Starfskraftur** skaltu smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f2742-114">In the **Worker** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f2742-115">Í listanum skaltu **Velja** starfskraftinn sem þú vilt nota.</span><span class="sxs-lookup"><span data-stu-id="f2742-115">In the list, **Select** the worker you want to use.</span></span>
6. <span data-ttu-id="f2742-116">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f2742-116">Select **OK**.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="f2742-117">Stofna færslubókarlínur</span><span class="sxs-lookup"><span data-stu-id="f2742-117">Create journal lines</span></span>
1. <span data-ttu-id="f2742-118">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="f2742-118">Select **New**.</span></span>
2. <span data-ttu-id="f2742-119">Í reitnum **Vörunúmer** velurðu skrána sem óskað er eftir af fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="f2742-119">In the **Item number** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="f2742-120">Ef verið er að nota sýnigögn fyrirtækisins USMF velja **A0001**.</span><span class="sxs-lookup"><span data-stu-id="f2742-120">If you are using demo data company USMF, select **A0001**.</span></span>  
3. <span data-ttu-id="f2742-121">Í reitnum **Svæði** velurðu skrána sem óskað er eftir af fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="f2742-121">In the **Site** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="f2742-122">Ef verið er að nota sýnigögn fyrirtækisins USMF, veljið svæði **2**.</span><span class="sxs-lookup"><span data-stu-id="f2742-122">If you are using demo data company USMF, select site **2**.</span></span>
4. <span data-ttu-id="f2742-123">Í reitnum **Vöruhús** velurðu skrána sem óskað er eftir af fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="f2742-123">In the **Warehouse** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="f2742-124">Ef verið er að nota sýnigögn fyrirtækisins USMF, skal velja vöruhúsið **24**.</span><span class="sxs-lookup"><span data-stu-id="f2742-124">If you are using demo data company USMF, select warehouse **24**.</span></span>  
5. <span data-ttu-id="f2742-125">Í reitnum **Staðsetning** velurðu skrána sem óskað er eftir af fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="f2742-125">In the **Location** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="f2742-126">Ef verið er að nota sýnigögn fyrirtækisins USMF, velja staðsetningu **BULK-001**.</span><span class="sxs-lookup"><span data-stu-id="f2742-126">If you are using demo data company USMF, select location **BULK-001**.</span></span>  
6. <span data-ttu-id="f2742-127">Í reitinn Talið skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="f2742-127">In the Counted field, enter a number.</span></span> <span data-ttu-id="f2742-128">Ef fært er inn talið númer sem er annað númer en er sýnt í reitnum **Á lager**, er reiturinn **Magn** uppfærður til að sýna misræmið.</span><span class="sxs-lookup"><span data-stu-id="f2742-128">If you enter a counted number that's different to the number shown in the **On-hand** field, the **Quantity** field is updated to show the discrepancy.</span></span>  
7. <span data-ttu-id="f2742-129">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="f2742-129">Select **Save**.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="f2742-130">Bóka færslubók fyrir birgðatalningu</span><span class="sxs-lookup"><span data-stu-id="f2742-130">Post the inventory counting journal</span></span>
1. <span data-ttu-id="f2742-131">Veldu **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="f2742-131">Select **Post**.</span></span> <span data-ttu-id="f2742-132">Þegar birgðatalningabók er bókuð, ef talin upphæð er önnur en upphæð sem skráð er í reitnum **Á lager** er innhreyfing eða úthreyfing birgða bókuð, birgðastigi og birgðagildi breytt og fjárhagsfærslur stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="f2742-132">When you post an inventory counting journal, if the counted amount differs from amount that's reported in the **On-hand** field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>
2. <span data-ttu-id="f2742-133">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f2742-133">Select **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="f2742-134">Skoða birgðafærslur</span><span class="sxs-lookup"><span data-stu-id="f2742-134">View inventory transactions</span></span>
1. <span data-ttu-id="f2742-135">Veldu **Birgðir**.</span><span class="sxs-lookup"><span data-stu-id="f2742-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="f2742-136">Veldu **Færslur**.</span><span class="sxs-lookup"><span data-stu-id="f2742-136">Select **Transactions**.</span></span> <span data-ttu-id="f2742-137">Hér er hægt að sjá tengdar færslur sem stofnast þegar talningarbók birgða er bókuð.</span><span class="sxs-lookup"><span data-stu-id="f2742-137">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

