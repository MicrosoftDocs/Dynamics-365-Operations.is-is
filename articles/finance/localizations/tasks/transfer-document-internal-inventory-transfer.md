---
title: Mynda flutningsskjal fyrir innri birgðaflutning
description: Þetta ferli sýnir hvernig á að stofna flutningsskjöl fyrir hreyfingu á vörum innan fyrirtækis
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4da59781f3357a6713eebba03d87c5127b8cd3b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174905"
---
# <a name="generate-a-transfer-document-for-an-internal-inventory-transfer"></a><span data-ttu-id="da237-103">Mynda flutningsskjal fyrir innri birgðaflutning</span><span class="sxs-lookup"><span data-stu-id="da237-103">Generate a transfer document for an internal inventory transfer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="da237-104">Þetta ferli sýnir hvernig á að stofna flutningsskjöl fyrir hreyfingu á vörum innan fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="da237-104">This procedure shows how to create transfer documents for goods movement inside a company.</span></span> <span data-ttu-id="da237-105">Þetta ferli er aðeins tiltæk fyrir lögaðila með aðalaðsetur í Litháen.</span><span class="sxs-lookup"><span data-stu-id="da237-105">This procedure is only available for legal entities with a primary address in Lithuania.</span></span> <span data-ttu-id="da237-106">Þetta ferli var stofnuð með því að nota sýnigögn fyrirtækisins DEMF með aðalaðsetur í Litháen.</span><span class="sxs-lookup"><span data-stu-id="da237-106">The procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="da237-107">Áður en hægt er að ljúka þessu ferli verður að ljúka ferlinu “Setja upp flutningsskjöl fyrir hreyfingu á vörum innan fyrirtækis”.</span><span class="sxs-lookup"><span data-stu-id="da237-107">Before you can complete this procedure, you must complete the “Set up transfer documents for goods movement inside a company” procedure.</span></span> <span data-ttu-id="da237-108">Þetta ferli er ætluð fyrir bókhaldara birgða.</span><span class="sxs-lookup"><span data-stu-id="da237-108">This procedure is intended for inventory accountants.</span></span> <span data-ttu-id="da237-109">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="da237-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-transfer-order"></a><span data-ttu-id="da237-110">Flutningspöntun stofnuð</span><span class="sxs-lookup"><span data-stu-id="da237-110">Create a transfer order</span></span>
1. <span data-ttu-id="da237-111">Fara í birgðastjórnun > pantanir á Innleið > Flutningspöntun.</span><span class="sxs-lookup"><span data-stu-id="da237-111">Go to Inventory management > Inbound orders > Transfer order.</span></span>
2. <span data-ttu-id="da237-112">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="da237-112">Click New.</span></span>
3. <span data-ttu-id="da237-113">Sláðu inn eða veldu gildi í reitnum Úr vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="da237-113">In the From warehouse field, enter or select a value.</span></span>
4. <span data-ttu-id="da237-114">Sláðu inn eða veldu gildi í reitnum Í vöruhús.</span><span class="sxs-lookup"><span data-stu-id="da237-114">In the To warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="da237-115">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="da237-115">Click Add.</span></span>
6. <span data-ttu-id="da237-116">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="da237-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="da237-117">Í reitinn Vörunúmer skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="da237-117">In the Item number field, enter or select a value.</span></span>

## <a name="enter-transportation-details-for-the-transfer-order"></a><span data-ttu-id="da237-118">Fylla út upplýsingar um Flutning fyrir flutningspöntun</span><span class="sxs-lookup"><span data-stu-id="da237-118">Enter transportation details for the transfer order</span></span>
1. <span data-ttu-id="da237-119">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="da237-119">Click Save.</span></span>
2. <span data-ttu-id="da237-120">Smellið á senda á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="da237-120">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="da237-121">Smelltu á Upplýsingar um flutning.</span><span class="sxs-lookup"><span data-stu-id="da237-121">Click Transportation details.</span></span>
4. <span data-ttu-id="da237-122">Velja skal Já í svæðinu Prenta flutningsupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="da237-122">Select Yes in the Print transportation details field.</span></span>
5. <span data-ttu-id="da237-123">Sláið inn eða veldu gildi í reitnum vörur gefnar út eftir.</span><span class="sxs-lookup"><span data-stu-id="da237-123">In the Goods issued by field, enter or select a value.</span></span>
6. <span data-ttu-id="da237-124">Í reitinn umbúðir skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="da237-124">In the Package field, type a value.</span></span>
7. <span data-ttu-id="da237-125">Í reitinn áhættustig skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="da237-125">In the Risk level of the load field, type a value.</span></span>
8. <span data-ttu-id="da237-126">Sláið inn eða veldu gildi í reitnum flutningsaðili.</span><span class="sxs-lookup"><span data-stu-id="da237-126">In the Carrier field, enter or select a value.</span></span>
9. <span data-ttu-id="da237-127">Sláið inn eða veldu gildi í reitnum líkan.</span><span class="sxs-lookup"><span data-stu-id="da237-127">In the Model field, enter or select a value.</span></span>
10. <span data-ttu-id="da237-128">Færa inn gildi í reitnum Skráningarnúmer.</span><span class="sxs-lookup"><span data-stu-id="da237-128">In the Registration number field, type a value.</span></span>
11. <span data-ttu-id="da237-129">Færa inn gildi í svæðinu skráningarnúmer eftirvagns.</span><span class="sxs-lookup"><span data-stu-id="da237-129">In the Trailer registration number field, type a value.</span></span>
12. <span data-ttu-id="da237-130">Sláið inn eða veldu gildi í reitnum ökumaður.</span><span class="sxs-lookup"><span data-stu-id="da237-130">In the Driver field, enter or select a value.</span></span>
13. <span data-ttu-id="da237-131">Sláið inn gildi í reitinn Nafn ökumanns.</span><span class="sxs-lookup"><span data-stu-id="da237-131">In the Driver name field, type a value.</span></span>
14. <span data-ttu-id="da237-132">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="da237-132">Click Save.</span></span>
15. <span data-ttu-id="da237-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="da237-133">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a><span data-ttu-id="da237-134">Skoða fylgiseðil fyrir óbókaðar flutningspöntun</span><span class="sxs-lookup"><span data-stu-id="da237-134">View the packing slip for the unposted transfer order</span></span>
1. <span data-ttu-id="da237-135">Smella skal á fylgiseðilinn.</span><span class="sxs-lookup"><span data-stu-id="da237-135">Click Packing slip.</span></span>
2. <span data-ttu-id="da237-136">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="da237-136">Click OK.</span></span>
3. <span data-ttu-id="da237-137">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="da237-137">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a><span data-ttu-id="da237-138">Skoða fylgiseðil fyrir bókaðar flutningspöntun</span><span class="sxs-lookup"><span data-stu-id="da237-138">View the packing slip for the posted transfer order</span></span>
1. <span data-ttu-id="da237-139">Í aðgerðasvæðinu er smellt á flutningspöntun.</span><span class="sxs-lookup"><span data-stu-id="da237-139">On the Action Pane, click Transfer order.</span></span>
2. <span data-ttu-id="da237-140">Smellið á senda á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="da237-140">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="da237-141">Smelltu á Senda flutningspöntun</span><span class="sxs-lookup"><span data-stu-id="da237-141">Click Ship transfer order.</span></span>
4. <span data-ttu-id="da237-142">Smellið á flipann „Almennt“.</span><span class="sxs-lookup"><span data-stu-id="da237-142">Click the General tab.</span></span>
5. <span data-ttu-id="da237-143">Í reitnum uppfærsla skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="da237-143">In the Update field, select an option.</span></span>
6. <span data-ttu-id="da237-144">Smellið á flipann „Yfirlit“.</span><span class="sxs-lookup"><span data-stu-id="da237-144">Click the Overview tab.</span></span>
7. <span data-ttu-id="da237-145">Í reitinn fylgiseðill skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="da237-145">In the Packing slip field, type a value.</span></span>
8. <span data-ttu-id="da237-146">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="da237-146">Click OK.</span></span>
9. <span data-ttu-id="da237-147">Smellið á senda á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="da237-147">On the Action Pane, click Ship.</span></span>
10. <span data-ttu-id="da237-148">Smella skal á fylgiseðilinn.</span><span class="sxs-lookup"><span data-stu-id="da237-148">Click Packing slip.</span></span>
11. <span data-ttu-id="da237-149">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="da237-149">Click OK.</span></span>
