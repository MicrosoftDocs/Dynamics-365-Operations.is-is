---
title: Stofna og viðhalda á birgðalæsing
description: Þessi verklýsing sýnir hvernig á að koma í veg fyrir að efnislegar lagerbirgðir séu frátekinn af önnur upprunaskjöl á útleið með því að nota lokun birgða.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 09789dc0b89f8bd36cca9b3e5be366bf17246243
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "322261"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="8f774-103">Stofna og viðhalda á birgðalæsing</span><span class="sxs-lookup"><span data-stu-id="8f774-103">Create and maintain an inventory blocking</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8f774-104">Þessi verklýsing sýnir hvernig á að koma í veg fyrir að efnislegar lagerbirgðir séu frátekinn af önnur upprunaskjöl á útleið með því að nota lokun birgða.</span><span class="sxs-lookup"><span data-stu-id="8f774-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="8f774-105">Hægt er að keyra ferlið sýnigögn fyrirtækisins USMF með dæmagildum sem eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="8f774-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="8f774-106">Þú þarft að hafa vöru á lager raunbirgðum tiltækt áður en byrjað er að þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="8f774-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="8f774-107">Stofna birgðalæsing</span><span class="sxs-lookup"><span data-stu-id="8f774-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="8f774-108">Fara í birgðastjórnun > Reglubundin verkefni >birgðalæsing.</span><span class="sxs-lookup"><span data-stu-id="8f774-108">Go to Inventory management > Periodic tasks > Inventory blocking.</span></span>
2. <span data-ttu-id="8f774-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="8f774-109">Click New.</span></span>
3. <span data-ttu-id="8f774-110">Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="8f774-110">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="8f774-111">Veljið vöruna sem á að velja af listanum.</span><span class="sxs-lookup"><span data-stu-id="8f774-111">In the list, select the item you want to choose.</span></span> 
    * <span data-ttu-id="8f774-112">Veljið vörunúmer með efnislegar lagerbirgðir sem á að loka.</span><span class="sxs-lookup"><span data-stu-id="8f774-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="8f774-113">Ef verið er að nota USMF er hægt að velja vöru M9201.</span><span class="sxs-lookup"><span data-stu-id="8f774-113">If you’re using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="8f774-114">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="8f774-114">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="8f774-115">Ef verið er að nota vöru M9201, þarf að velja minna en 200.</span><span class="sxs-lookup"><span data-stu-id="8f774-115">If you’re using item M9201, you need to select less than 200.</span></span>  
6. <span data-ttu-id="8f774-116">Víxla útvíkkun á hlutanum birgðavíddir.</span><span class="sxs-lookup"><span data-stu-id="8f774-116">Toggle the expansion of the Inventory dimensions section.</span></span>
7. <span data-ttu-id="8f774-117">Í reitnum vöruhús skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="8f774-117">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="8f774-118">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="8f774-118">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8f774-119">Ef verið er að nota M9201 vöru er hægt að velja vöruhús 51.</span><span class="sxs-lookup"><span data-stu-id="8f774-119">If you’re using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="8f774-120">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="8f774-120">Click Save.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="8f774-121">Uppfæra skilyrðum fyrir birgðalæsing</span><span class="sxs-lookup"><span data-stu-id="8f774-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="8f774-122">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="8f774-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="8f774-123">Uppfæra magnsvæði birgða til að endurspegla magn til að loka.</span><span class="sxs-lookup"><span data-stu-id="8f774-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="8f774-124">Færa inn dagsetningu í svæðinu áætluð dagsetning.</span><span class="sxs-lookup"><span data-stu-id="8f774-124">In the Expected date field, enter a date.</span></span>
    * <span data-ttu-id="8f774-125">Þú vilt kannski tilgreina þegar búist er við að læstar birgðir verða tiltækar til frátektar með því að úthluta væntanleg dagsetning..</span><span class="sxs-lookup"><span data-stu-id="8f774-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="8f774-126">Ef Áætlað innhreyfingar valkostur er valinn fyrir við birgðalæsing, eins og hann er sjálfgefinn þegar handvirkt við er stofnuð lokun, þessi dagsetning birtist á áætlaðrar færslu.</span><span class="sxs-lookup"><span data-stu-id="8f774-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="8f774-127">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="8f774-127">Click Save.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="8f774-128">Fjarlægja birgðalæsingu</span><span class="sxs-lookup"><span data-stu-id="8f774-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="8f774-129">Smellið á Eyða.</span><span class="sxs-lookup"><span data-stu-id="8f774-129">Click Delete.</span></span>
2. <span data-ttu-id="8f774-130">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="8f774-130">Click Yes.</span></span>
3. <span data-ttu-id="8f774-131">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8f774-131">Close the page.</span></span>

