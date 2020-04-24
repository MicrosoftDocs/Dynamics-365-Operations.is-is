---
title: Stofna lánardrottnalykil
description: Þessi verklýsing sýnir hvernig á að stofna lánardrottnalykill, og bæta við aðsetur og tengslaupplýsingar.
author: mkirknel
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aca23db2a0cc86a2c12ea74d3b1e491643b7efec
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207693"
---
# <a name="create-a-vendor-account"></a><span data-ttu-id="e25e1-103">Stofna lánardrottnalykil</span><span class="sxs-lookup"><span data-stu-id="e25e1-103">Create a vendor account</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e25e1-104">Þessi verklýsing sýnir hvernig á að stofna lánardrottnalykill, og bæta við aðsetur og tengslaupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="e25e1-104">This procedure shows how to create a vendor account, and add an address and contact information.</span></span> <span data-ttu-id="e25e1-105">Ferli sem sýna ekki hvernig á að fylla út alla reiti fyrir málefni innkaupa og fjármála.</span><span class="sxs-lookup"><span data-stu-id="e25e1-105">The procedure does not show how to populate all fields for purchasing and financial purposes.</span></span> <span data-ttu-id="e25e1-106">Frekari upplýsingar um þessi svæði, vinsamlegast lesið í lýsingum svæða.</span><span class="sxs-lookup"><span data-stu-id="e25e1-106">To learn more about those fields, please read the field descriptions.</span></span> <span data-ttu-id="e25e1-107">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="e25e1-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="e25e1-108">Lánardrottnalykla eru yfirleitt stofnaðar eftir fagmanns á sviði innkaupa eða starfsfólks í viðskiptakröfum.</span><span class="sxs-lookup"><span data-stu-id="e25e1-108">Vendor accounts are typically created by a procurement professional or accounts receivable personnel.</span></span>


## <a name="create-a-vendor-account"></a><span data-ttu-id="e25e1-109">Stofna lánardrottnalykil</span><span class="sxs-lookup"><span data-stu-id="e25e1-109">Create a vendor account</span></span>
1. <span data-ttu-id="e25e1-110">Farði í **Skoðunarrúðuna > Kerfiseiningar > Innkaup og aðföng > Lánardrottnar > Allir lánardrottnar**.</span><span class="sxs-lookup"><span data-stu-id="e25e1-110">Go to **Navigation pane > Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="e25e1-111">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="e25e1-111">Click **New**.</span></span>
3. <span data-ttu-id="e25e1-112">Í svæðinu **Lánardrottnalykill** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e25e1-112">In the **Vendor account** field, type a value.</span></span>
    - <span data-ttu-id="e25e1-113">Gildið gæti verið fyllt út sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="e25e1-113">The value may be populated automatically.</span></span> <span data-ttu-id="e25e1-114">Ef svo er má Sleppa þessu skrefi</span><span class="sxs-lookup"><span data-stu-id="e25e1-114">If so, you can skip this step.</span></span>  
    - <span data-ttu-id="e25e1-115">Hægt er að stofna lánardrottnalykla fyrir einstakling eða fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="e25e1-115">You can create vendor accounts for a person or organization.</span></span> <span data-ttu-id="e25e1-116">Þetta hefur áhrif á hvaða svæði eru tiltæk.</span><span class="sxs-lookup"><span data-stu-id="e25e1-116">This will affect which fields are available.</span></span> <span data-ttu-id="e25e1-117">Í þessu dæmi munum við stofna lánardrottinslykil fyrir fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="e25e1-117">In this example, we'll create a vendor account for an organization.</span></span>   
4. <span data-ttu-id="e25e1-118">Sláið inn eða veldu gildi í reitnum **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="e25e1-118">In the **Name** field, enter or select a value.</span></span> <span data-ttu-id="e25e1-119">Ef lánardrottinn er til þegar skráður aðili í kerfinu er hægt nota fellilista og velja þau í þessum reit og nýr lánardrottnalykill mun erfa aðsetur og upplýsingar tengiliðs sem þegar eru skráðar.</span><span class="sxs-lookup"><span data-stu-id="e25e1-119">If your vendor is an already a registered party in your system you can use drop down and select them in this field and the new vendor account will inherit the address and contact information that's already registered.</span></span>
5. <span data-ttu-id="e25e1-120">Sláið inn eða veldu gildi í reitnum **Hópur**.</span><span class="sxs-lookup"><span data-stu-id="e25e1-120">In the **Group** field, enter or select a value.</span></span> <span data-ttu-id="e25e1-121">Flokkur lánardrottins er notuð til að flokka lánardrottna sem hafa einhverjar eftirfarandi færibreytur: Greiðsluskilmála; jafna tímabil; birgðabókunarfjárhagslyklar, þar á meðal vsk-flokkur; sjálfgefna fjárhagslykla; afurðasíukóðar eða skilgreiningu eftirspurnarspár.</span><span class="sxs-lookup"><span data-stu-id="e25e1-121">The vendor group is used to group vendors that have any of the following parameters in common: Terms of payment, settle period, inventory posting ledger accounts – including the sales tax group, default ledger accounts, product filter codes, or supply forecast configuration.</span></span>
6. <span data-ttu-id="e25e1-122">Í reitinn **Fjöldi starfsmanna** skal færa inn tölu.</span><span class="sxs-lookup"><span data-stu-id="e25e1-122">In the **Number of employees** field, enter a number.</span></span>
7. <span data-ttu-id="e25e1-123">Í reitinn **Númer fyrirtækis** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e25e1-123">In the **Organization number** field, type a value.</span></span>

## <a name="add-an-address"></a><span data-ttu-id="e25e1-124">Bæta við aðsetri</span><span class="sxs-lookup"><span data-stu-id="e25e1-124">Add an address</span></span>
1. <span data-ttu-id="e25e1-125">Útvíkkaðu hlutann **Aðsetur**.</span><span class="sxs-lookup"><span data-stu-id="e25e1-125">Expand the **Addresses** section.</span></span>
2. <span data-ttu-id="e25e1-126">Smelltu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="e25e1-126">Click **Add**.</span></span>
3. <span data-ttu-id="e25e1-127">Sláið inn eða veldu gildi í reitnum **Málefni**.</span><span class="sxs-lookup"><span data-stu-id="e25e1-127">In the **Purpose** field, enter or select a value.</span></span> <span data-ttu-id="e25e1-128">Hægt er að velja fleiri en eitt málefni.</span><span class="sxs-lookup"><span data-stu-id="e25e1-128">You can select one or more purposes.</span></span> <span data-ttu-id="e25e1-129">Þær eru notaðar til að velja rétta aðsetur fyrir ákveðið málefni.</span><span class="sxs-lookup"><span data-stu-id="e25e1-129">These are used to select the correct address for a given purpose.</span></span> <span data-ttu-id="e25e1-130">T.d. ef málefni er „Reikningur" mun það aðsetur vera notað þegar þú sendir reikninga.</span><span class="sxs-lookup"><span data-stu-id="e25e1-130">For example, if the purpose is "Invoice" that address will be used when you send invoices.</span></span>
4. <span data-ttu-id="e25e1-131">Í reitinn **Nafn eða lýsing** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e25e1-131">In the **Name or description** field, type a value.</span></span>
5. <span data-ttu-id="e25e1-132">Í reitinn **Land/svæði** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="e25e1-132">In the **Country/region** field, enter or select a value.</span></span> <span data-ttu-id="e25e1-133">Færið inn upplýsingar um aðsetur.</span><span class="sxs-lookup"><span data-stu-id="e25e1-133">Enter the address details.</span></span> <span data-ttu-id="e25e1-134">Land/svæði sem er valið mun ákvarða svæðin sem birtast þér, pg samsvara aðseturssnið fyrir land/svæði.</span><span class="sxs-lookup"><span data-stu-id="e25e1-134">The country/region that you selected will determine the fields you are presented with, corresponding to the address format for the country/region.</span></span> 
6. <span data-ttu-id="e25e1-135">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="e25e1-135">Click **OK**.</span></span>

## <a name="add-contact-information"></a><span data-ttu-id="e25e1-136">Bæta við tengslaupplýsingum</span><span class="sxs-lookup"><span data-stu-id="e25e1-136">Add contact information</span></span>
1. <span data-ttu-id="e25e1-137">Útvíkkaðu kaflann **Tengslaupplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="e25e1-137">Expand the **Contact information** section.</span></span>
2. <span data-ttu-id="e25e1-138">Smelltu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="e25e1-138">Click **Add**.</span></span>
3. <span data-ttu-id="e25e1-139">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e25e1-139">In the **Description** field, type a value.</span></span>
4. <span data-ttu-id="e25e1-140">Í reitnum **Tegund** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="e25e1-140">In the **Type** field, select an option.</span></span>
5. <span data-ttu-id="e25e1-141">Í reitinn **Númer/aðsetur tengiliðar** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e25e1-141">In the **Contact number/address** field, type a value.</span></span> <span data-ttu-id="e25e1-142">Veljið aðal gátreit ef þetta er aðaltengiliður.</span><span class="sxs-lookup"><span data-stu-id="e25e1-142">You can select the Primary check box if this is the primary contact.</span></span>  
6. <span data-ttu-id="e25e1-143">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e25e1-143">Click **Save**.</span></span>
7. <span data-ttu-id="e25e1-144">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e25e1-144">Close the page.</span></span>
8. <span data-ttu-id="e25e1-145">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e25e1-145">Close the page.</span></span>

