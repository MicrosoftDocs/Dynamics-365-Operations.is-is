--- 
title: "Stofna lánardrottnalykil"
description: "Þessi verklýsing sýnir hvernig á að stofna lánardrottnalykill, og bæta við aðsetur og tengslaupplýsingar."
author: mkirknel
manager: AnnBe
ms.date: 06/06/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: aaa5b503af95883c2c7fdfb2ad7f3e3062d28961
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-vendor-account"></a><span data-ttu-id="c8cb3-103">Stofna lánardrottnalykil</span><span class="sxs-lookup"><span data-stu-id="c8cb3-103">Create a vendor account</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c8cb3-104">Þessi verklýsing sýnir hvernig á að stofna lánardrottnalykill, og bæta við aðsetur og tengslaupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-104">This procedure shows how to create a vendor account, and add an address and contact information.</span></span> <span data-ttu-id="c8cb3-105">Ferli sem sýna ekki hvernig á að fylla út alla reiti fyrir málefni innkaupa og fjármála.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-105">The procedure does not show how to populate all fields for purchasing and financial purposes.</span></span> <span data-ttu-id="c8cb3-106">Frekari upplýsingar um þessi svæði, vinsamlegast lesið í lýsingum svæða.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-106">To learn more about those fields, please read the field descriptions.</span></span> <span data-ttu-id="c8cb3-107">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="c8cb3-108">Lánardrottnalykla eru yfirleitt stofnaðar eftir fagmanns á sviði innkaupa eða starfsfólks í viðskiptakröfum.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-108">Vendor accounts are typically created by a procurement professional or accounts receivable personnel.</span></span>


## <a name="create-a-vendor-account"></a><span data-ttu-id="c8cb3-109">Stofna lánardrottnalykil</span><span class="sxs-lookup"><span data-stu-id="c8cb3-109">Create a vendor account</span></span>
1. <span data-ttu-id="c8cb3-110">Farið í innkaup og aðföng > Lánardrottnar > Allir lánardrottnar.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-110">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="c8cb3-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-111">Click New.</span></span>
3. <span data-ttu-id="c8cb3-112">Í svæðinu Lánardrottnalykill skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-112">In the Vendor account field, type a value.</span></span>
    * <span data-ttu-id="c8cb3-113">Gildið gæti verið fyllt út sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-113">The value may be populated automatically.</span></span> <span data-ttu-id="c8cb3-114">Ef svo er má Sleppa þessu skrefi</span><span class="sxs-lookup"><span data-stu-id="c8cb3-114">If so, you can skip this step.</span></span>  
    * <span data-ttu-id="c8cb3-115">Hægt er að stofna lánardrottnalykla fyrir einstakling eða fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-115">You can create vendor accounts for a person or organization.</span></span> <span data-ttu-id="c8cb3-116">Þetta hefur áhrif á hvaða svæði eru tiltæk.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-116">This will affect which fields are available.</span></span> <span data-ttu-id="c8cb3-117">Í þessu dæmi munum við stofna lánardrottinslykil fyrir fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="c8cb3-117">In this example, we’ll create a vendor account for an organization.</span></span>   
4. <span data-ttu-id="c8cb3-118">Sláið inn eða veldu gildi í reitnum heiti.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-118">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="c8cb3-119">Ef lánardrottinn er til þegar skráður aðila í kerfinu þínu er hægt nota fellilista og velja þau í þessu svæði og nýja lánardrottnalykil munu erfa aðsetur og upplýsingar tengiliðs sem þegar eru skráðar.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-119">If your vendor is an already a registered party in your system you can use drop down and select them in this field and the new vendor account will inherit the address and contact information that’s already registered.</span></span>  
5. <span data-ttu-id="c8cb3-120">Sláið inn eða veldu gildi í reitnum hópur.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-120">In the Group field, enter or select a value.</span></span>
    * <span data-ttu-id="c8cb3-121">Flokkur lánardrottins er notuð til að flokka lánardrottna sem hafa einhverjar eftirfarandi færibreytur: Greiðsluskilmála; jafna tímabil; birgðabókunarfjárhagslyklar, þar á meðal vsk-flokkur; sjálfgefna fjárhagslykla; afurðasíukóðar eða skilgreiningu eftirspurnarspár.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-121">The vendor group is used to group vendors that have any of the following parameters in common: Terms of payment , settle period,  inventory posting ledger accounts – including the sales tax group, default ledger accounts, product filter codes, or supply forecast configuration.</span></span>  
6. <span data-ttu-id="c8cb3-122">Í reitnum Fjöldi starfsmanna skal færa inn tölu.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-122">In the Number of employees field, enter a number.</span></span>
7. <span data-ttu-id="c8cb3-123">Í reitnum Númer fyrirtækis skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-123">In the Organization number field, type a value.</span></span>

## <a name="add-an-address"></a><span data-ttu-id="c8cb3-124">Bæta við aðsetri</span><span class="sxs-lookup"><span data-stu-id="c8cb3-124">Add an address</span></span>
1. <span data-ttu-id="c8cb3-125">Stækka aðsetur Hluti.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-125">Expand the Addresses section.</span></span>
2. <span data-ttu-id="c8cb3-126">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-126">Click Add.</span></span>
3. <span data-ttu-id="c8cb3-127">Sláið inn eða veldu gildi í reitnum málefni.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-127">In the Purpose field, enter or select a value.</span></span>
    * <span data-ttu-id="c8cb3-128">Hægt er að velja fleiri en eitt málefni.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-128">You can select one or more purposes.</span></span> <span data-ttu-id="c8cb3-129">Þær eru notaðar til að velja rétta aðsetur fyrir ákveðið málefni.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-129">These are used to select the correct address for a given purpose.</span></span> <span data-ttu-id="c8cb3-130">T.d. ef málefni er „Reikningur" mun það aðsetur vera notað þegar þú sendir reikninga.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-130">For example, if the purpose is “Invoice” that address will be used when you send invoices.</span></span>  
4. <span data-ttu-id="c8cb3-131">Færa inn gildi í reitnum Nafn eða lýsing.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-131">In the Name or description field, type a value.</span></span>
5. <span data-ttu-id="c8cb3-132">Slá inn eða velja gildi í reitnum Umræður.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-132">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="c8cb3-133">Færið inn upplýsingar um aðsetur.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-133">Enter the address details.</span></span> <span data-ttu-id="c8cb3-134">Land/svæði sem er valið mun ákvarða svæðin sem birtast þér, pg samsvara aðseturssnið fyrir land/svæði.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-134">The country/region that you selected will determine the fields you are presented with, corresponding to the address format for the country/region.</span></span>   
6. <span data-ttu-id="c8cb3-135">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-135">Click OK.</span></span>

## <a name="add-contact-information"></a><span data-ttu-id="c8cb3-136">Bæta við tengslaupplýsingum</span><span class="sxs-lookup"><span data-stu-id="c8cb3-136">Add contact information</span></span>
1. <span data-ttu-id="c8cb3-137">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-137">Click Add.</span></span>
2. <span data-ttu-id="c8cb3-138">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-138">In the Description field, type a value.</span></span>
3. <span data-ttu-id="c8cb3-139">Veljið valkost í svæðinu tegund.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-139">In the Type field, select an option.</span></span>
4. <span data-ttu-id="c8cb3-140">Færa inn gildi í svæðið númer/aðsetur Tengiliðar.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-140">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="c8cb3-141">Veljið aðal gátreit ef þetta er aðaltengiliður.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-141">You can select the Primary check box if this is the primary contact.</span></span>  
5. <span data-ttu-id="c8cb3-142">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-142">Click Save.</span></span>
6. <span data-ttu-id="c8cb3-143">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-143">Close the page.</span></span>
7. <span data-ttu-id="c8cb3-144">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c8cb3-144">Close the page.</span></span>


