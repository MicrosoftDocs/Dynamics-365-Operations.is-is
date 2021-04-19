---
title: Leiðrétta birgðastöðu í vöruhúsi (grunnvöruhús)
description: Þetta ferli fer í gegnum ferlið fyrir stofnun og bókun birgðaleiðréttingabók til að leiðrétta geymslustig afurða í vöruhúsið.
author: MarkusFogelberg
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0bba1df70cd23a29ddffad96a4a581154619dc74
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834146"
---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a><span data-ttu-id="2cc74-103">Leiðrétta birgðastöðu í vöruhúsi (grunnvöruhús)</span><span class="sxs-lookup"><span data-stu-id="2cc74-103">Adjust stock levels in the warehouse (basic warehousing)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2cc74-104">Þetta ferli fer í gegnum ferlið fyrir stofnun og bókun birgðaleiðréttingabók til að leiðrétta geymslustig afurða í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="2cc74-104">This procedure walks you through the process of creating and posting an inventory adjustment journal in order to adjust stock levels of products in the warehouse.</span></span> <span data-ttu-id="2cc74-105">Þú þarft að hafa með heiti birgðabókarinnar sett upp fyrir leiðréttingar á birgðum áður en þetta er hafið.</span><span class="sxs-lookup"><span data-stu-id="2cc74-105">You need to have an inventory journal name set up for inventory adjustments before you start this.</span></span> <span data-ttu-id="2cc74-106">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="2cc74-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="2cc74-107">Þessi verkefni eru venjulega framkvæmd af starfsmanni í vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="2cc74-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-adjustment-journal"></a><span data-ttu-id="2cc74-108">Stofna heiti færslubóka fyrir birgðaleiðréttingu</span><span class="sxs-lookup"><span data-stu-id="2cc74-108">Create an inventory adjustment journal</span></span>
1. <span data-ttu-id="2cc74-109">Fara í Birgðastjórnun > Færslubókarfærslur > Vörur > Birgðaleiðrétting.</span><span class="sxs-lookup"><span data-stu-id="2cc74-109">Go to Inventory management > Journal entries > Items > Inventory adjustment.</span></span>
2. <span data-ttu-id="2cc74-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="2cc74-110">Click New.</span></span>
3. <span data-ttu-id="2cc74-111">Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="2cc74-111">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="2cc74-112">Á listanum smellirðu á heiti færslubókar fyrir birgðaleiðréttingu sem á að nota.</span><span class="sxs-lookup"><span data-stu-id="2cc74-112">In the list, click on the inventory adjustment journal name you want to use.</span></span>
    * <span data-ttu-id="2cc74-113">Sumir aðrir reitir verða fylltir út samkvæmt uppsetningu heitis færslubókar birgðaleiðréttingar sem var valið.</span><span class="sxs-lookup"><span data-stu-id="2cc74-113">Some other fields will be populated based on the setup of the inventory adjustment journal name you select.</span></span>  
5. <span data-ttu-id="2cc74-114">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="2cc74-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="2cc74-115">Stofna færslubókarlínur</span><span class="sxs-lookup"><span data-stu-id="2cc74-115">Create journal lines</span></span>
1. <span data-ttu-id="2cc74-116">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="2cc74-116">Click New.</span></span>
2. <span data-ttu-id="2cc74-117">Í listanum merkirðu við reitinn Vörunúmer.</span><span class="sxs-lookup"><span data-stu-id="2cc74-117">In the list, mark the item number field.</span></span>
3. <span data-ttu-id="2cc74-118">Í reitnum Vörunúmer velurðu vöru.</span><span class="sxs-lookup"><span data-stu-id="2cc74-118">In the Item number field, Select an item.</span></span> <span data-ttu-id="2cc74-119">Ef verið er að nota sýnigagnafyrirtækið USMF skal slá inn 'D0001'.</span><span class="sxs-lookup"><span data-stu-id="2cc74-119">If you are using demo data company USMF, type 'D0001'.</span></span>
4. <span data-ttu-id="2cc74-120">Í reitnum svæði skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="2cc74-120">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="2cc74-121">Í listanum velurðu Svæði.</span><span class="sxs-lookup"><span data-stu-id="2cc74-121">In the list, select a site.</span></span>
6. <span data-ttu-id="2cc74-122">Í reitnum vöruhús skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="2cc74-122">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="2cc74-123">Í listanum velurðu Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="2cc74-123">In the list, select a warehouse.</span></span>
    * <span data-ttu-id="2cc74-124">Ef þú hefur valið vöru með Staðsetningu sem áskilda vídd þarftu að tilgreina staðsetninguna hér.</span><span class="sxs-lookup"><span data-stu-id="2cc74-124">If you have selected an item with Location as a mandatory dimension, you would have to specify the location here.</span></span>  
8. <span data-ttu-id="2cc74-125">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="2cc74-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="2cc74-126">Reiturinn Kostnaðarverð tilgreinir einingarkostnað fyrir innhreyfingar birgða.</span><span class="sxs-lookup"><span data-stu-id="2cc74-126">The cost price field specifies the cost per unit for inventory receipts.</span></span> <span data-ttu-id="2cc74-127">Ef kostnaður er ekki tilgreindur fyrir vörunúmer eða ef þú vildir breyta því handvirkt þá er það gert hér.</span><span class="sxs-lookup"><span data-stu-id="2cc74-127">If the cost is not specified for the item number or if you wanted to change it manually, you would do this here.</span></span>  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a><span data-ttu-id="2cc74-128">Sannprófa og bóka færslubók fyrir leiðréttingu á birgðaskrá</span><span class="sxs-lookup"><span data-stu-id="2cc74-128">Validate and post the inventory adjustment journal</span></span>
1. <span data-ttu-id="2cc74-129">Smella á Villuleita.</span><span class="sxs-lookup"><span data-stu-id="2cc74-129">Click Validate.</span></span>
2. <span data-ttu-id="2cc74-130">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="2cc74-130">Click OK.</span></span>
3. <span data-ttu-id="2cc74-131">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="2cc74-131">Click Post.</span></span>
    * <span data-ttu-id="2cc74-132">Þegar þessi gerð færslubókar er bókuð er innhreyfing birgða eða vandamál bókað, birgðastigi og gildi er breytt og fjárhagsfærslur eru myndaðar.</span><span class="sxs-lookup"><span data-stu-id="2cc74-132">When you post this kind of journal, an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
4. <span data-ttu-id="2cc74-133">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="2cc74-133">Click OK.</span></span>
5. <span data-ttu-id="2cc74-134">Lokaðu skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="2cc74-134">Close the form.</span></span>
6. <span data-ttu-id="2cc74-135">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="2cc74-135">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]