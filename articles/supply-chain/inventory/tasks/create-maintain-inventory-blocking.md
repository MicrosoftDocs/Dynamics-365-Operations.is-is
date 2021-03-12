---
title: Stofna og viðhalda á birgðalæsing
description: Þessi verklýsing sýnir hvernig á að koma í veg fyrir að efnislegar lagerbirgðir séu frátekinn af önnur upprunaskjöl á útleið með því að nota lokun birgða.
author: perlynne
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eab6730daa2eb7df0f91d99d1026d4736285fef9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000060"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="cff2b-103">Stofna og viðhalda á birgðalæsing</span><span class="sxs-lookup"><span data-stu-id="cff2b-103">Create and maintain an inventory blocking</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cff2b-104">Þessi verklýsing sýnir hvernig á að koma í veg fyrir að efnislegar lagerbirgðir séu frátekinn af önnur upprunaskjöl á útleið með því að nota lokun birgða.</span><span class="sxs-lookup"><span data-stu-id="cff2b-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="cff2b-105">Hægt er að keyra ferlið sýnigögn fyrirtækisins USMF með dæmagildum sem eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="cff2b-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="cff2b-106">Þú þarft að hafa vöru á lager raunbirgðum tiltækt áður en byrjað er að þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="cff2b-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="cff2b-107">Stofna birgðalæsing</span><span class="sxs-lookup"><span data-stu-id="cff2b-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="cff2b-108">Í **skoðunarrúðunni** ferðu í **Kerfiseiningar > Birgðastýring > Reglubundin verk > Birgðalæsing**.</span><span class="sxs-lookup"><span data-stu-id="cff2b-108">In the **Navigation pane**, go to **Modules > Inventory management > Periodic tasks > Inventory blocking**.</span></span>
2. <span data-ttu-id="cff2b-109">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="cff2b-109">Click **New**.</span></span>
3. <span data-ttu-id="cff2b-110">Í reitnum **Vörunúmer** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="cff2b-110">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="cff2b-111">Veljið vöruna sem á að velja af listanum.</span><span class="sxs-lookup"><span data-stu-id="cff2b-111">In the list, select the item you want to choose.</span></span> <span data-ttu-id="cff2b-112">Veljið vörunúmer með efnislegar lagerbirgðir sem á að loka.</span><span class="sxs-lookup"><span data-stu-id="cff2b-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="cff2b-113">Ef þú ert að nota USMF er hægt að velja vöru M9201.</span><span class="sxs-lookup"><span data-stu-id="cff2b-113">If you're using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="cff2b-114">Í reitnum **Magn** slærðu inn tölu.</span><span class="sxs-lookup"><span data-stu-id="cff2b-114">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="cff2b-115">Ef þú ert að nota vöru M9201, þarf að velja minna en 200.</span><span class="sxs-lookup"><span data-stu-id="cff2b-115">If you're using item M9201, you need to select less than 200.</span></span>
6. <span data-ttu-id="cff2b-116">Útvíkkaðu flýtiflipann **Birgðavíddir**.</span><span class="sxs-lookup"><span data-stu-id="cff2b-116">Expand the **Inventory dimensions** fastTab.</span></span>
7. <span data-ttu-id="cff2b-117">Í reitnum **Vöruhús** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="cff2b-117">In the **Warehouse** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="cff2b-118">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="cff2b-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="cff2b-119">Ef þú ert að nota M9201 vöru er hægt að velja vöruhús 51.</span><span class="sxs-lookup"><span data-stu-id="cff2b-119">If you're using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="cff2b-120">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="cff2b-120">Click **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="cff2b-121">Uppfæra skilyrðum fyrir birgðalæsing</span><span class="sxs-lookup"><span data-stu-id="cff2b-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="cff2b-122">Á flýtiflipanum **Almennt**, í reitnum **Magn** skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="cff2b-122">In the **General** fastTab, in the **Quantity** field, enter a number.</span></span> <span data-ttu-id="cff2b-123">Uppfæra magnsvæði birgða til að endurspegla magn til að loka.</span><span class="sxs-lookup"><span data-stu-id="cff2b-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="cff2b-124">Í reitnum **Væntanleg dagsetning** skal færa inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="cff2b-124">In the **Expected date** field, enter a date.</span></span> <span data-ttu-id="cff2b-125">Þú vilt kannski tilgreina þegar búist er við að læstar birgðir verða tiltækar til frátektar með því að úthluta væntanleg dagsetning..</span><span class="sxs-lookup"><span data-stu-id="cff2b-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="cff2b-126">Ef Áætlað innhreyfingar valkostur er valinn fyrir við birgðalæsing, eins og hann er sjálfgefinn þegar handvirkt við er stofnuð lokun, þessi dagsetning birtist á áætlaðrar færslu.</span><span class="sxs-lookup"><span data-stu-id="cff2b-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="cff2b-127">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="cff2b-127">Click **Save**.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="cff2b-128">Fjarlægja birgðalæsingu</span><span class="sxs-lookup"><span data-stu-id="cff2b-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="cff2b-129">Í **aðgerðasvæðinu** er smellt á **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="cff2b-129">On the **Action Pane**, click **Delete**.</span></span>
2. <span data-ttu-id="cff2b-130">Smellið á **Já**.</span><span class="sxs-lookup"><span data-stu-id="cff2b-130">Click **Yes**.</span></span>
3. <span data-ttu-id="cff2b-131">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="cff2b-131">Close the page.</span></span>

