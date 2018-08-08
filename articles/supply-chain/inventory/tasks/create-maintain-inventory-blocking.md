---
title: "Stofna og vinna með birgðalæsingu"
description: "Þessi verklýsing sýnir hvernig á að koma í veg fyrir að efnislegar lagerbirgðir séu frátekinn af önnur upprunaskjöl á útleið með því að nota lokun birgða."
author: perlynne
manager: AnnBe
ms.date: 12/02/2015
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 5c3e05439dec8395066c7cf00afa248571ea0abc
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---
# <a name="create-and-maintain-inventory-blocking"></a><span data-ttu-id="71064-103">Stofna og vinna með birgðalæsingu</span><span class="sxs-lookup"><span data-stu-id="71064-103">Create and maintain inventory blocking</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="71064-104">Þessi verklýsing sýnir hvernig á að koma í veg fyrir að efnislegar lagerbirgðir séu frátekinn af önnur upprunaskjöl á útleið með því að nota lokun birgða.</span><span class="sxs-lookup"><span data-stu-id="71064-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="71064-105">Hægt er að keyra ferlið sýnigögn fyrirtækisins USMF með dæmagildum sem eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="71064-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="71064-106">Þú þarft að hafa vöru á lager raunbirgðum tiltækt áður en byrjað er að þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="71064-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="71064-107">Stofna birgðalæsing</span><span class="sxs-lookup"><span data-stu-id="71064-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="71064-108">Fara í birgðastjórnun > Reglubundin verkefni >birgðalæsing.</span><span class="sxs-lookup"><span data-stu-id="71064-108">Go to Inventory management > Periodic tasks > Inventory blocking.</span></span>
2. <span data-ttu-id="71064-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="71064-109">Click New.</span></span>
3. <span data-ttu-id="71064-110">Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="71064-110">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="71064-111">Veljið vöruna sem á að velja af listanum.</span><span class="sxs-lookup"><span data-stu-id="71064-111">In the list, select the item you want to choose.</span></span>
    * <span data-ttu-id="71064-112">Veljið vörunúmer með efnislegar lagerbirgðir sem á að loka.</span><span class="sxs-lookup"><span data-stu-id="71064-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="71064-113">Ef verið er að nota USMF er hægt að velja vöru M9201.</span><span class="sxs-lookup"><span data-stu-id="71064-113">If you’re using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="71064-114">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="71064-114">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="71064-115">Ef verið er að nota vöru M9201, þarf að velja minna en 200.</span><span class="sxs-lookup"><span data-stu-id="71064-115">If you’re using item M9201, you need to select less than 200.</span></span>  
6. <span data-ttu-id="71064-116">Víxla útvíkkun á hlutanum birgðavíddir.</span><span class="sxs-lookup"><span data-stu-id="71064-116">Toggle the expansion of the Inventory dimensions section.</span></span>
7. <span data-ttu-id="71064-117">Í reitnum vöruhús skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="71064-117">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="71064-118">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="71064-118">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="71064-119">Ef verið er að nota M9201 vöru er hægt að velja vöruhús 51.</span><span class="sxs-lookup"><span data-stu-id="71064-119">If you’re using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="71064-120">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="71064-120">Click Save.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="71064-121">Uppfæra skilyrðum fyrir birgðalæsing</span><span class="sxs-lookup"><span data-stu-id="71064-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="71064-122">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="71064-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="71064-123">Uppfæra magnsvæði birgða til að endurspegla magn til að loka.</span><span class="sxs-lookup"><span data-stu-id="71064-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="71064-124">Færa inn dagsetningu í svæðinu áætluð dagsetning.</span><span class="sxs-lookup"><span data-stu-id="71064-124">In the Expected date field, enter a date.</span></span>
    * <span data-ttu-id="71064-125">Þú vilt kannski tilgreina þegar búist er við að læstar birgðir verða tiltækar til frátektar með því að úthluta væntanleg dagsetning..</span><span class="sxs-lookup"><span data-stu-id="71064-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="71064-126">Ef Áætlað innhreyfingar valkostur er valinn fyrir við birgðalæsing, eins og hann er sjálfgefinn þegar handvirkt við er stofnuð lokun, þessi dagsetning birtist á áætlaðrar færslu.</span><span class="sxs-lookup"><span data-stu-id="71064-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="71064-127">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="71064-127">Click Save.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="71064-128">Fjarlægja birgðalæsingu</span><span class="sxs-lookup"><span data-stu-id="71064-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="71064-129">Smellið á Eyða.</span><span class="sxs-lookup"><span data-stu-id="71064-129">Click Delete.</span></span>
2. <span data-ttu-id="71064-130">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="71064-130">Click Yes.</span></span>
3. <span data-ttu-id="71064-131">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="71064-131">Close the page.</span></span>

