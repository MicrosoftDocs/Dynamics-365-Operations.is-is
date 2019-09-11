---
title: Stofna innkaupasamning
description: Þetta efni leiðbeinir við stofnun innkaupasamnings.
author: mkirknel
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec792ca27bf0245ff25e59cfe28122f17caec7fc
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/08/2019
ms.locfileid: "1866851"
---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="8a305-103">Stofna innkaupasamning</span><span class="sxs-lookup"><span data-stu-id="8a305-103">Create a purchase agreement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8a305-104">Þetta efni leiðbeinir við stofnun innkaupasamnings.</span><span class="sxs-lookup"><span data-stu-id="8a305-104">This topic guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="8a305-105">Þetta verk myndi yfirleitt gert af innkaupastjóra.</span><span class="sxs-lookup"><span data-stu-id="8a305-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="8a305-106">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="8a305-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="8a305-107">Þú Þarft að hafa sett upp flokkanir innkaupasamnings áður en byrjað er.</span><span class="sxs-lookup"><span data-stu-id="8a305-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="8a305-108">Þegar Innkaupapöntun er stofnuð og hægt er að nota hana þegar þú stofnar innkaupapöntun, og það afrita skilyrði innkaupasamnings í haus og allar línur í pöntun sem verða fyrir áhrifum af samninginn.</span><span class="sxs-lookup"><span data-stu-id="8a305-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="8a305-109">Stofna nýjan innkaupasamning</span><span class="sxs-lookup"><span data-stu-id="8a305-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="8a305-110">Farðu í **Skoðunarrúðu > Kerfiseiningar > Innkaup og aðföng > Innkaupasamningar > Innkaupasamningar**.</span><span class="sxs-lookup"><span data-stu-id="8a305-110">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase agreements > Purchase agreements**.</span></span>
2. <span data-ttu-id="8a305-111">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="8a305-111">Click **New**.</span></span>
3. <span data-ttu-id="8a305-112">Í reitnum **Lánardrottnalykill** velurðu fellivalmyndina og velur röðina með viðeigandi skrá.</span><span class="sxs-lookup"><span data-stu-id="8a305-112">In the **Vendor account** field, select the drop-down menu and select the row of the desired record.</span></span>
4. <span data-ttu-id="8a305-113">Í reitnum **Flokkun innkaupasamnings** velurðu fellivalmyndina og velur röðina með viðeigandi skrá.</span><span class="sxs-lookup"><span data-stu-id="8a305-113">In the **Purchase agreement classification** field, select the drop-down menu and select the row of the desired record.</span></span>
5. <span data-ttu-id="8a305-114">Útvíkka **Almennt** flýtiflipa.</span><span class="sxs-lookup"><span data-stu-id="8a305-114">Expand the **General** FastTab.</span></span>
6. <span data-ttu-id="8a305-115">Í reitinn **Lokadagur** skal rita dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="8a305-115">In the **Expiration date** field, enter a date.</span></span>

    - <span data-ttu-id="8a305-116">Þessi lokadagur verður sjálfgefið fyrir allar línur ráðstöfunar og ákvarða hve lengi hver tiltekin ráðstöfun er gild.</span><span class="sxs-lookup"><span data-stu-id="8a305-116">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  

7. <span data-ttu-id="8a305-117">Í reitinn **Heiti skjals** skal færa inn heiti fyrir innkaupasamninginn.</span><span class="sxs-lookup"><span data-stu-id="8a305-117">In the **Document title** field, type a name for your purchase agreement.</span></span>

    - <span data-ttu-id="8a305-118">Hafðu reitinn **Sjálfgefin ráðstöfun** að vera stillt á **Ráðstafað afurðarmagn** (eða breyttu honum, ef hann er ekki stilltur á þetta).</span><span class="sxs-lookup"><span data-stu-id="8a305-118">Leave the **Default commitment** field set to **Product quantity commitment** (or change it if it’s not set to this).</span></span>  
    - <span data-ttu-id="8a305-119">Sjálfgefin ráðstöfunargildið ákvarðar valkostirnir þínir á samningslínur.</span><span class="sxs-lookup"><span data-stu-id="8a305-119">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="8a305-120">Ef ný ráðstöfunargerð er þörf þegar verið er að stofna samningslínur, þarftu að breyta sjálfgefin ráðstöfun í haus.</span><span class="sxs-lookup"><span data-stu-id="8a305-120">If you need a new commitment type when you’re creating the agreement lines, you need to change the default commitment on the header.</span></span> <span data-ttu-id="8a305-121">Til eru 4 gerðir ráðstafana: **Ráðstöfun afurðarmagns** - fyrir ákveðið magn afurðar; **Ráðstöfunarvirði afurðar** - fyrir tiltekna gjaldmiðilsupphæð afurðar; **Ráðstöfunarvirði vörutegundar** - fyrir upphæð í tilteknum gjaldmiðli í innkaupaflokki þar sem upphæðin getur verið fyrir vöru í vörulista eða vöru sem er ekki á vörulista; **Ráðstöfunarvirði** - fyrir tiltekna gjaldmiðilsupphæð sem getur verið uppfyllt af hvaða vöru eða af hvaða innkaupategund sem er.</span><span class="sxs-lookup"><span data-stu-id="8a305-121">There are 4 types of commitments: **Product quantity commitment** - for a specific quantity of a product; **Product value commitment** - for a specific currency amount of a product; **Product category value commitment** - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; **Value commitment** - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  

8. <span data-ttu-id="8a305-122">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="8a305-122">Select **OK**.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="8a305-123">Bæta við skuldbindingu</span><span class="sxs-lookup"><span data-stu-id="8a305-123">Add a commitment</span></span>
1. <span data-ttu-id="8a305-124">Veldu **Bæta við línu**.</span><span class="sxs-lookup"><span data-stu-id="8a305-124">Select **Add line**.</span></span>
2. <span data-ttu-id="8a305-125">Í reitnum **Vörunúmer** velurðu skrána sem óskað er eftir af fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="8a305-125">In the **Item number** field, select the desired record from the drop-down menu.</span></span>
3. <span data-ttu-id="8a305-126">Í reitnum **Magn** slærðu inn tölu.</span><span class="sxs-lookup"><span data-stu-id="8a305-126">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="8a305-127">Þetta er heildarmagn sem þú hefur samþykkt að kaupa frá lánardrottni.</span><span class="sxs-lookup"><span data-stu-id="8a305-127">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
4. <span data-ttu-id="8a305-128">Í reitnum **Einingarverð** skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="8a305-128">In the **Unit price** field, enter a number.</span></span>
5. <span data-ttu-id="8a305-129">Útvíkkaðu hlutann **upplýsingar Línu**.</span><span class="sxs-lookup"><span data-stu-id="8a305-129">Expand the **Line details** section.</span></span>
6. <span data-ttu-id="8a305-130">Stilltu valkostinn **Hámarki er framfylgt** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="8a305-130">Set the **Max is enforced** option to **Yes**.</span></span> <span data-ttu-id="8a305-131">Valkosturinn **Hámarki er framfylgt** takmarkar notkun á ráðstöfun.</span><span class="sxs-lookup"><span data-stu-id="8a305-131">The **Max is enforced** option limits the use of the commitment.</span></span> <span data-ttu-id="8a305-132">Aðeins er hægt að kaupa upp að því magni sem er tilgreint er í reitnum **Magn** fyrir línuna.</span><span class="sxs-lookup"><span data-stu-id="8a305-132">You can only purchase up to the quantity that's specified in the **Quantity** field for the line.</span></span>  

## <a name="add-header-conditions"></a><span data-ttu-id="8a305-133">Bæta við fyrirsagnaskilyrði</span><span class="sxs-lookup"><span data-stu-id="8a305-133">Add header conditions</span></span>
1. <span data-ttu-id="8a305-134">Í aðgerðasvæðinu velurðu **Valkostir**.</span><span class="sxs-lookup"><span data-stu-id="8a305-134">On the Action Pane, select **Options**.</span></span>
2. <span data-ttu-id="8a305-135">Veldu **Breyta skjámynd**.</span><span class="sxs-lookup"><span data-stu-id="8a305-135">Select **Change view**.</span></span>
3. <span data-ttu-id="8a305-136">Veldu **Hausyfirlit**.</span><span class="sxs-lookup"><span data-stu-id="8a305-136">Select **Header view**.</span></span>
4. <span data-ttu-id="8a305-137">Útvíkkaðu kaflann **Skilmálar**.</span><span class="sxs-lookup"><span data-stu-id="8a305-137">Expand the **Terms** section.</span></span>
5. <span data-ttu-id="8a305-138">Í reitnum **Greiðsluháttur** velurðu skrána sem óskað er eftir af fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="8a305-138">In the **Method of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="8a305-139">Greiðsluskilmálar úr lykli lánardrottins eru sýnd hér sjálfgefið.</span><span class="sxs-lookup"><span data-stu-id="8a305-139">The payment terms from the vendor account are shown here by default.</span></span>  
6. <span data-ttu-id="8a305-140">Í reitnum **Afhendingarmáti** velurðu skrána sem óskað er eftir af fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="8a305-140">In the **Mode of delivery** field, select the desired record in the drop-down menu.</span></span>
7. <span data-ttu-id="8a305-141">Í reitnum **Afhendingarskilmálar** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="8a305-141">In the **Delivery terms** field, select the drop-down button to open the lookup.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="8a305-142">Vista og virkja samning</span><span class="sxs-lookup"><span data-stu-id="8a305-142">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="8a305-143">Í aðgerðasvæðinu smellirðu á **Innkaupasamningur**.</span><span class="sxs-lookup"><span data-stu-id="8a305-143">On the Action Pane, select **Purchase agreement**.</span></span>
2. <span data-ttu-id="8a305-144">Veldu **Staðfesting**.</span><span class="sxs-lookup"><span data-stu-id="8a305-144">Select **Confirmation**.</span></span> <span data-ttu-id="8a305-145">Stilltu valkostinn **Merkja samning sem gildan** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="8a305-145">Set the **Mark agreement as effective** option to **Yes**.</span></span>  
3. <span data-ttu-id="8a305-146">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="8a305-146">Select **OK**.</span></span>
4. <span data-ttu-id="8a305-147">Í aðgerðasvæðinu smellirðu á **Innkaupasamningur**.</span><span class="sxs-lookup"><span data-stu-id="8a305-147">On the Action Pane, select **Purchase agreement**.</span></span>
5. <span data-ttu-id="8a305-148">Veldu **Staðfestingar innkaupasamnings**.</span><span class="sxs-lookup"><span data-stu-id="8a305-148">Select **Purchase agreement confirmations**.</span></span> <span data-ttu-id="8a305-149">Valkosturinn **Forskoðun/Prenta** gerir kleift að búa til skjal fyrir innkaupasamning sem síðan er hægt að prenta eða senda til lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="8a305-149">The **Preview/Print** option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="8a305-150">Ef þú uppfæra samning síðar og staðfesta hann aftur, verða báðar útgáfur sýnd hér.</span><span class="sxs-lookup"><span data-stu-id="8a305-150">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="8a305-151">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8a305-151">Close the page.</span></span>

