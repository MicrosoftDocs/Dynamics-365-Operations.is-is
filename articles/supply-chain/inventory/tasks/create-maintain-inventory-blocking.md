---
title: Stofna og viðhalda á birgðalæsing
description: Þessi verklýsing sýnir hvernig á að koma í veg fyrir að efnislegar lagerbirgðir séu frátekinn af önnur upprunaskjöl á útleið með því að nota lokun birgða.
author: perlynne
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2408addea3615ffe6dbc4db8baecfdef6a65e839
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145825"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="3628d-103">Stofna og viðhalda á birgðalæsing</span><span class="sxs-lookup"><span data-stu-id="3628d-103">Create and maintain an inventory blocking</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3628d-104">Þessi verklýsing sýnir hvernig á að koma í veg fyrir að efnislegar lagerbirgðir séu frátekinn af önnur upprunaskjöl á útleið með því að nota lokun birgða.</span><span class="sxs-lookup"><span data-stu-id="3628d-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="3628d-105">Hægt er að keyra ferlið sýnigögn fyrirtækisins USMF með dæmagildum sem eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="3628d-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="3628d-106">Þú þarft að hafa vöru á lager raunbirgðum tiltækt áður en byrjað er að þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="3628d-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="3628d-107">Stofna birgðalæsing</span><span class="sxs-lookup"><span data-stu-id="3628d-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="3628d-108">Í **skoðunarrúðunni** ferðu í **Kerfiseiningar > Birgðastýring > Reglubundin verk > Birgðalæsing**.</span><span class="sxs-lookup"><span data-stu-id="3628d-108">In the **Navigation pane**, go to **Modules > Inventory management > Periodic tasks > Inventory blocking**.</span></span>
2. <span data-ttu-id="3628d-109">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="3628d-109">Click **New**.</span></span>
3. <span data-ttu-id="3628d-110">Í reitnum **Vörunúmer** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="3628d-110">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="3628d-111">Veljið vöruna sem á að velja af listanum.</span><span class="sxs-lookup"><span data-stu-id="3628d-111">In the list, select the item you want to choose.</span></span> <span data-ttu-id="3628d-112">Veljið vörunúmer með efnislegar lagerbirgðir sem á að loka.</span><span class="sxs-lookup"><span data-stu-id="3628d-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="3628d-113">Ef þú ert að nota USMF er hægt að velja vöru M9201.</span><span class="sxs-lookup"><span data-stu-id="3628d-113">If you're using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="3628d-114">Í reitnum **Magn** slærðu inn tölu.</span><span class="sxs-lookup"><span data-stu-id="3628d-114">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="3628d-115">Ef þú ert að nota vöru M9201, þarf að velja minna en 200.</span><span class="sxs-lookup"><span data-stu-id="3628d-115">If you're using item M9201, you need to select less than 200.</span></span>
6. <span data-ttu-id="3628d-116">Útvíkkaðu flýtiflipann **Birgðavíddir**.</span><span class="sxs-lookup"><span data-stu-id="3628d-116">Expand the **Inventory dimensions** fastTab.</span></span>
7. <span data-ttu-id="3628d-117">Í reitnum **Vöruhús** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="3628d-117">In the **Warehouse** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="3628d-118">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="3628d-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="3628d-119">Ef þú ert að nota M9201 vöru er hægt að velja vöruhús 51.</span><span class="sxs-lookup"><span data-stu-id="3628d-119">If you're using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="3628d-120">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="3628d-120">Click **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="3628d-121">Uppfæra skilyrðum fyrir birgðalæsing</span><span class="sxs-lookup"><span data-stu-id="3628d-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="3628d-122">Á flýtiflipanum **Almennt**, í reitnum **Magn** skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="3628d-122">In the **General** fastTab, in the **Quantity** field, enter a number.</span></span> <span data-ttu-id="3628d-123">Uppfæra magnsvæði birgða til að endurspegla magn til að loka.</span><span class="sxs-lookup"><span data-stu-id="3628d-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="3628d-124">Í reitnum **Væntanleg dagsetning** skal færa inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="3628d-124">In the **Expected date** field, enter a date.</span></span> <span data-ttu-id="3628d-125">Þú vilt kannski tilgreina þegar búist er við að læstar birgðir verða tiltækar til frátektar með því að úthluta væntanleg dagsetning..</span><span class="sxs-lookup"><span data-stu-id="3628d-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="3628d-126">Ef Áætlað innhreyfingar valkostur er valinn fyrir við birgðalæsing, eins og hann er sjálfgefinn þegar handvirkt við er stofnuð lokun, þessi dagsetning birtist á áætlaðrar færslu.</span><span class="sxs-lookup"><span data-stu-id="3628d-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="3628d-127">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="3628d-127">Click **Save**.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="3628d-128">Fjarlægja birgðalæsingu</span><span class="sxs-lookup"><span data-stu-id="3628d-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="3628d-129">Í **Aðgerðasvæðinu** skal smella á **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="3628d-129">On the **Action pane**, click **Delete**.</span></span>
2. <span data-ttu-id="3628d-130">Smellið á **Já**.</span><span class="sxs-lookup"><span data-stu-id="3628d-130">Click **Yes**.</span></span>
3. <span data-ttu-id="3628d-131">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3628d-131">Close the page.</span></span>

