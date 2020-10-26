---
title: Skrá vörur fyrir virkjaðar vöru grunnvöruhúss með vörukomubók
description: Þessi verklýsing sýnir hvernig á að skrá vörur með því að nota vörukomubókina þegar verið er að nota „grunnur vöruhús” í kerfinu birgðastjórnun.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, WMSJournalTable, WMSJournalCreate, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1745642dd270e62557b8624cc9daf85d13da044e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982577"
---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-an-item-arrival-journal"></a><span data-ttu-id="9bbc8-103">Skrá vörur fyrir virkjaðar vöru grunnvöruhúss með vörukomubók</span><span class="sxs-lookup"><span data-stu-id="9bbc8-103">Register items for a basic warehousing enabled item using an item an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9bbc8-104">Þessi verklýsing sýnir hvernig á að skrá vörur með því að nota vörukomubókina þegar verið er að nota „grunnur vöruhús” í kerfinu birgðastjórnun.</span><span class="sxs-lookup"><span data-stu-id="9bbc8-104">This procedure shows you how to register items using the item arrival journal when you are using "basic warehousing" in the Inventory management module.</span></span> <span data-ttu-id="9bbc8-105">Þetta væri yfirleitt gert með af móttöku starfsmaður.</span><span class="sxs-lookup"><span data-stu-id="9bbc8-105">This would usually be done by a receiving clerk.</span></span> <span data-ttu-id="9bbc8-106">Hægt er að keyra þetta ferli með sýnigögn fyrirtækisins USMF með dæmagildin sem eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="9bbc8-106">You can run this procedure in demo data company USMF with the example values that are shown.</span></span>  <span data-ttu-id="9bbc8-107">Ef þú ert ekki að nota USMF, þarf að hafa staðfest innkaupapöntun með opna innkaupapöntunarlínu áður en byrjað er að þessari handbók.</span><span class="sxs-lookup"><span data-stu-id="9bbc8-107">If you are not using USMF, you need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="9bbc8-108">Varan á línunni verðu að vera á lager.</span><span class="sxs-lookup"><span data-stu-id="9bbc8-108">The item on the line must be stocked.</span></span> <span data-ttu-id="9bbc8-109">Og varan þarf að tengjast geymsluvíddaflokk, þar sem svæða og vöruhúsa eru virk.</span><span class="sxs-lookup"><span data-stu-id="9bbc8-109">And the item needs to be associated with a storage dimension group, where site and warehouse are active.</span></span>


## <a name="create-item-arrival-journal-header"></a><span data-ttu-id="9bbc8-110">Stofna haus fyrir vörukomubók</span><span class="sxs-lookup"><span data-stu-id="9bbc8-110">Create item arrival journal header</span></span>
1. <span data-ttu-id="9bbc8-111">Fara í birgðastjórnun > Færslubókarfærslur > Vörukoma > Vörukoma.</span><span class="sxs-lookup"><span data-stu-id="9bbc8-111">Go to Inventory management > Journal entries > Item arrival > Item arrival.</span></span>
2. <span data-ttu-id="9bbc8-112">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="9bbc8-112">Click New.</span></span>
3. <span data-ttu-id="9bbc8-113">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9bbc8-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="9bbc8-114">Ef verið er að nota USMF, er hægt að færa inn vöruhúsakerfi.</span><span class="sxs-lookup"><span data-stu-id="9bbc8-114">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="9bbc8-115">Ef verið er að nota önnur gögn, verður færslubókin sem þú velur heitið á að hafa eftirfarandi eiginleika: Athuga tiltektarstaðsetningu verður að vera stillt á Nei og biðgeymslustjórnun verður að vera stillt á Nei.</span><span class="sxs-lookup"><span data-stu-id="9bbc8-115">If you're using other data, the journal whose name you choose has to have the following properties: cheque picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="9bbc8-116">Í reitinn fylgiseðill skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9bbc8-116">In the Packing slip field, type a value.</span></span>
    * <span data-ttu-id="9bbc8-117">Þetta er Kenni fylgiseðils af fylgiseðli sem er gefið út af lánardrottni.</span><span class="sxs-lookup"><span data-stu-id="9bbc8-117">This is the packing slip ID from the packing slip issued by the vendor.</span></span> <span data-ttu-id="9bbc8-118">Bæta við einkvæmt númer.</span><span class="sxs-lookup"><span data-stu-id="9bbc8-118">Add a unique number.</span></span>  
5. <span data-ttu-id="9bbc8-119">Veljið innkaupapöntun í númerareitnum.</span><span class="sxs-lookup"><span data-stu-id="9bbc8-119">In the Number field, In the Number field, select the purchase order..</span></span>
6. <span data-ttu-id="9bbc8-120">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9bbc8-120">Click OK.</span></span>

## <a name="add-lines-to-item-arrival-journal"></a><span data-ttu-id="9bbc8-121">Bæta línum við vörukomubók</span><span class="sxs-lookup"><span data-stu-id="9bbc8-121">Add lines to item arrival journal</span></span>
1. <span data-ttu-id="9bbc8-122">Smellið á Aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="9bbc8-122">Click Functions.</span></span>
2. <span data-ttu-id="9bbc8-123">Smellið á Stofna línur .</span><span class="sxs-lookup"><span data-stu-id="9bbc8-123">Click Create lines.</span></span>
    * <span data-ttu-id="9bbc8-124">Línur getur verið fært handvirkt inn í þessa færslubók eða sjálfkrafa stofnuð.</span><span class="sxs-lookup"><span data-stu-id="9bbc8-124">The lines can be entered manually into this journal or created automatically.</span></span> <span data-ttu-id="9bbc8-125">Þetta sýnir hvernig á að stofna það sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="9bbc8-125">This will show you how to create this automatically.</span></span>  
3. <span data-ttu-id="9bbc8-126">Merkja eða afmerkja gátreit Frumstilla magn.</span><span class="sxs-lookup"><span data-stu-id="9bbc8-126">Check or uncheck the Initialize quantity checkbox.</span></span>
    * <span data-ttu-id="9bbc8-127">Þetta mun frumstilla magn á færslubókarlínum með magn ekki skráð úr innkaupapöntunarlínunni.</span><span class="sxs-lookup"><span data-stu-id="9bbc8-127">This will initialize the quantity on the journal lines with the quantity not registered from the purchase order line.</span></span>  
4. <span data-ttu-id="9bbc8-128">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9bbc8-128">Click OK.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="9bbc8-129">Bóka færslubókina</span><span class="sxs-lookup"><span data-stu-id="9bbc8-129">Post the journal</span></span>
1. <span data-ttu-id="9bbc8-130">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="9bbc8-130">Click Post.</span></span>
2. <span data-ttu-id="9bbc8-131">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9bbc8-131">Click OK.</span></span>

## <a name="generate-the-product-receipt"></a><span data-ttu-id="9bbc8-132">Mynda innhreyfingarskjal afurða</span><span class="sxs-lookup"><span data-stu-id="9bbc8-132">Generate the product receipt</span></span>
1. <span data-ttu-id="9bbc8-133">Smellið á Aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="9bbc8-133">Click Functions.</span></span>
2. <span data-ttu-id="9bbc8-134">Smellið á „Innhreyfingarskjal“.</span><span class="sxs-lookup"><span data-stu-id="9bbc8-134">Click Product receipt.</span></span>
3. <span data-ttu-id="9bbc8-135">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9bbc8-135">Click OK.</span></span>

