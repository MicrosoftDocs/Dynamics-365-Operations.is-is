---
title: Stofna lánardrottnalykil
description: Þessi verklýsing sýnir hvernig á að stofna lánardrottnalykill, og bæta við aðsetur og tengslaupplýsingar.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 98a7c6d209400b754064f2176d1ebca291093304
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838047"
---
# <a name="create-a-vendor-account"></a><span data-ttu-id="c19ce-103">Stofna lánardrottnalykil</span><span class="sxs-lookup"><span data-stu-id="c19ce-103">Create a vendor account</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c19ce-104">Þessi verklýsing sýnir hvernig á að stofna lánardrottnalykill, og bæta við aðsetur og tengslaupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="c19ce-104">This procedure shows how to create a vendor account, and add an address and contact information.</span></span> <span data-ttu-id="c19ce-105">Ferli sem sýna ekki hvernig á að fylla út alla reiti fyrir málefni innkaupa og fjármála.</span><span class="sxs-lookup"><span data-stu-id="c19ce-105">The procedure does not show how to populate all fields for purchasing and financial purposes.</span></span> <span data-ttu-id="c19ce-106">Frekari upplýsingar um þessi svæði, vinsamlegast lesið í lýsingum svæða.</span><span class="sxs-lookup"><span data-stu-id="c19ce-106">To learn more about those fields, please read the field descriptions.</span></span> <span data-ttu-id="c19ce-107">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="c19ce-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="c19ce-108">Lánardrottnalykla eru yfirleitt stofnaðar eftir fagmanns á sviði innkaupa eða starfsfólks í viðskiptakröfum.</span><span class="sxs-lookup"><span data-stu-id="c19ce-108">Vendor accounts are typically created by a procurement professional or accounts receivable personnel.</span></span>


## <a name="create-a-vendor-account"></a><span data-ttu-id="c19ce-109">Stofna lánardrottnalykil</span><span class="sxs-lookup"><span data-stu-id="c19ce-109">Create a vendor account</span></span>
1. <span data-ttu-id="c19ce-110">Farið í innkaup og aðföng > Lánardrottnar > Allir lánardrottnar.</span><span class="sxs-lookup"><span data-stu-id="c19ce-110">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="c19ce-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="c19ce-111">Click New.</span></span>
3. <span data-ttu-id="c19ce-112">Í svæðinu Lánardrottnalykill skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="c19ce-112">In the Vendor account field, type a value.</span></span>
    * <span data-ttu-id="c19ce-113">Gildið gæti verið fyllt út sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="c19ce-113">The value may be populated automatically.</span></span> <span data-ttu-id="c19ce-114">Ef svo er má Sleppa þessu skrefi</span><span class="sxs-lookup"><span data-stu-id="c19ce-114">If so, you can skip this step.</span></span>  
    * <span data-ttu-id="c19ce-115">Hægt er að stofna lánardrottnalykla fyrir einstakling eða fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="c19ce-115">You can create vendor accounts for a person or organization.</span></span> <span data-ttu-id="c19ce-116">Þetta hefur áhrif á hvaða svæði eru tiltæk.</span><span class="sxs-lookup"><span data-stu-id="c19ce-116">This will affect which fields are available.</span></span> <span data-ttu-id="c19ce-117">Í þessu dæmi munum við stofna lánardrottinslykil fyrir fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="c19ce-117">In this example, we’ll create a vendor account for an organization.</span></span>   
4. <span data-ttu-id="c19ce-118">Sláið inn eða veldu gildi í reitnum heiti.</span><span class="sxs-lookup"><span data-stu-id="c19ce-118">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="c19ce-119">Ef lánardrottinn er til þegar skráður aðila í kerfinu þínu er hægt nota fellilista og velja þau í þessu svæði og nýja lánardrottnalykil munu erfa aðsetur og upplýsingar tengiliðs sem þegar eru skráðar.</span><span class="sxs-lookup"><span data-stu-id="c19ce-119">If your vendor is an already a registered party in your system you can use drop down and select them in this field and the new vendor account will inherit the address and contact information that’s already registered.</span></span>  
5. <span data-ttu-id="c19ce-120">Sláið inn eða veldu gildi í reitnum hópur.</span><span class="sxs-lookup"><span data-stu-id="c19ce-120">In the Group field, enter or select a value.</span></span>
    * <span data-ttu-id="c19ce-121">Flokkur lánardrottins er notuð til að flokka lánardrottna sem hafa einhverjar eftirfarandi færibreytur: Greiðsluskilmála; jafna tímabil; birgðabókunarfjárhagslyklar, þar á meðal vsk-flokkur; sjálfgefna fjárhagslykla; afurðasíukóðar eða skilgreiningu eftirspurnarspár.</span><span class="sxs-lookup"><span data-stu-id="c19ce-121">The vendor group is used to group vendors that have any of the following parameters in common: Terms of payment , settle period,  inventory posting ledger accounts – including the sales tax group, default ledger accounts, product filter codes, or supply forecast configuration.</span></span>  
6. <span data-ttu-id="c19ce-122">Í reitnum Fjöldi starfsmanna skal færa inn tölu.</span><span class="sxs-lookup"><span data-stu-id="c19ce-122">In the Number of employees field, enter a number.</span></span>
7. <span data-ttu-id="c19ce-123">Í reitnum Númer fyrirtækis skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="c19ce-123">In the Organization number field, type a value.</span></span>

## <a name="add-an-address"></a><span data-ttu-id="c19ce-124">Bæta við aðsetri</span><span class="sxs-lookup"><span data-stu-id="c19ce-124">Add an address</span></span>
1. <span data-ttu-id="c19ce-125">Stækka aðsetur Hluti.</span><span class="sxs-lookup"><span data-stu-id="c19ce-125">Expand the Addresses section.</span></span>
2. <span data-ttu-id="c19ce-126">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c19ce-126">Click Add.</span></span>
3. <span data-ttu-id="c19ce-127">Sláið inn eða veldu gildi í reitnum málefni.</span><span class="sxs-lookup"><span data-stu-id="c19ce-127">In the Purpose field, enter or select a value.</span></span>
    * <span data-ttu-id="c19ce-128">Hægt er að velja fleiri en eitt málefni.</span><span class="sxs-lookup"><span data-stu-id="c19ce-128">You can select one or more purposes.</span></span> <span data-ttu-id="c19ce-129">Þær eru notaðar til að velja rétta aðsetur fyrir ákveðið málefni.</span><span class="sxs-lookup"><span data-stu-id="c19ce-129">These are used to select the correct address for a given purpose.</span></span> <span data-ttu-id="c19ce-130">T.d. ef málefni er „Reikningur" mun það aðsetur vera notað þegar þú sendir reikninga.</span><span class="sxs-lookup"><span data-stu-id="c19ce-130">For example, if the purpose is “Invoice” that address will be used when you send invoices.</span></span>  
4. <span data-ttu-id="c19ce-131">Færa inn gildi í reitnum Nafn eða lýsing.</span><span class="sxs-lookup"><span data-stu-id="c19ce-131">In the Name or description field, type a value.</span></span>
5. <span data-ttu-id="c19ce-132">Slá inn eða velja gildi í reitnum Umræður.</span><span class="sxs-lookup"><span data-stu-id="c19ce-132">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="c19ce-133">Færið inn upplýsingar um aðsetur.</span><span class="sxs-lookup"><span data-stu-id="c19ce-133">Enter the address details.</span></span> <span data-ttu-id="c19ce-134">Land/svæði sem er valið mun ákvarða svæðin sem birtast þér, pg samsvara aðseturssnið fyrir land/svæði.</span><span class="sxs-lookup"><span data-stu-id="c19ce-134">The country/region that you selected will determine the fields you are presented with, corresponding to the address format for the country/region.</span></span>   
6. <span data-ttu-id="c19ce-135">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c19ce-135">Click OK.</span></span>

## <a name="add-contact-information"></a><span data-ttu-id="c19ce-136">Bæta við tengslaupplýsingum</span><span class="sxs-lookup"><span data-stu-id="c19ce-136">Add contact information</span></span>
1. <span data-ttu-id="c19ce-137">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c19ce-137">Click Add.</span></span>
2. <span data-ttu-id="c19ce-138">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="c19ce-138">In the Description field, type a value.</span></span>
3. <span data-ttu-id="c19ce-139">Veljið valkost í svæðinu tegund.</span><span class="sxs-lookup"><span data-stu-id="c19ce-139">In the Type field, select an option.</span></span>
4. <span data-ttu-id="c19ce-140">Færa inn gildi í svæðið númer/aðsetur Tengiliðar.</span><span class="sxs-lookup"><span data-stu-id="c19ce-140">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="c19ce-141">Veljið aðal gátreit ef þetta er aðaltengiliður.</span><span class="sxs-lookup"><span data-stu-id="c19ce-141">You can select the Primary check box if this is the primary contact.</span></span>  
5. <span data-ttu-id="c19ce-142">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="c19ce-142">Click Save.</span></span>
6. <span data-ttu-id="c19ce-143">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c19ce-143">Close the page.</span></span>
7. <span data-ttu-id="c19ce-144">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c19ce-144">Close the page.</span></span>

