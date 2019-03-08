---
title: Skráning móttöku skilaðra vara
description: Þú getur skráð kvittun skilavara með því að nota skjámynd komuyfirlits eða skráningarblaða.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview, InventTransRegister
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2be628d312e623e8ea6d92eb5edce12334190d9e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "328080"
---
# <a name="register-the-receipt-of-returned-items"></a><span data-ttu-id="f2b6f-103">Skráning móttöku skilaðra vara</span><span class="sxs-lookup"><span data-stu-id="f2b6f-103">Register the receipt of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f2b6f-104">Það eru tvær aðferðir til að skrá kvittun skilavara.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-104">There are two methods for registering the receipt of returned items.</span></span> <span data-ttu-id="f2b6f-105">Fyrri aðferðin er móttökuferli vöruhúss sem notar skjámyndina **Komuyfirlit**.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-105">The first method is a warehouse receiving process that uses the **Arrival overview** form.</span></span> <span data-ttu-id="f2b6f-106">Seinni aðferðin notar skjámyndina **Skráning**.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-106">The second uses the **Registration** form.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-arrival-overview-form"></a><span data-ttu-id="f2b6f-107">Skráning móttöku skilaðra vara í skjámyndinni komuyfirlit</span><span class="sxs-lookup"><span data-stu-id="f2b6f-107">Register the receipt of returned items in the Arrival overview form</span></span>

<span data-ttu-id="f2b6f-108">Þú getur notað skjámyndina **Komuyfirlit** til að bera kennsl á skilaafhendingu eftir númeri vöruskilaheimildar (RMA-númer).</span><span class="sxs-lookup"><span data-stu-id="f2b6f-108">You can use the **Arrival overview** form to identify a return shipment by its Return Material Authorization (RMA) number.</span></span> <span data-ttu-id="f2b6f-109">Ef heiti færslubókar er skilgreint á flipanum **Uppsetning** og færslubókarlínur sem samsvara línunum sem eru valdar í skjámyndinni **Komuyfirlit** eru til verður nýr færslubókarhaus stofnaður þegar þú smellir á **Upphafskoma**.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-109">If a journal name is defined on the **Setup** tab, and journal lines that correspond to the lines selected on the **Arrival overview** form exist, a new journal header is created when you click **Start arrival**.</span></span>

1.  <span data-ttu-id="f2b6f-110">Smelltu á **Birgðastjórnun** \> **Reglubundið** \> **Komuyfirlit**.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-110">Click **Inventory management** \> **Periodic** \> **Arrival overview**.</span></span>

2.  <span data-ttu-id="f2b6f-111">Í reitnum **Heiti uppsetningar** skal velja **Skilapöntun** og smella síðan á **Uppfæra**.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-111">In the **Setup name** field, select **Return order**, and then click **Update**.</span></span>
    

    > [!TIP]
    > <P><span data-ttu-id="f2b6f-112">Hægt er að nota reitinn <STRONG>Svið</STRONG> til að þrengja leitarniðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-112">You can use the <STRONG>Range</STRONG> fields to narrow the search results.</span></span> <span data-ttu-id="f2b6f-113">Þú getur slegið inn eða valið RMA-númerið í reitnum <STRONG>RMA-númer</STRONG> til að fá nákvæma niðurstöðu.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-113">You can type or select the RMA number in the <STRONG>RMA number</STRONG> field for an exact result.</span></span> <span data-ttu-id="f2b6f-114">Til að skilgreina og vista safn af síum sem takmarkar hvaða komur á innleið eru birtar skal smella á flipann <STRONG>Uppsetning</STRONG>. Tiltækar síur eru gerðir, vöruhús og dreifing.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-114">To define and save a set of filters that will restrict which incoming arrivals are displayed, click the <STRONG>Setup</STRONG> tab. The available filters include types, warehouses, and docks.</span></span></P>

    

    > [!WARNING]
    > <P><span data-ttu-id="f2b6f-115">Skilapöntunum er ekki hægt að blanda saman við aðrar komugerðir í skjámyndinni <STRONG>Komuyfirlit</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-115">Return orders cannot be mixed with other arrival types in the <STRONG>Arrival overview</STRONG> form.</span></span> <span data-ttu-id="f2b6f-116">Þess vegna verður tilvísunin alltaf sölupöntun, en ekkert sölupöntunarauðkenni verður tilgreint í færslubókarhausnum.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-116">Therefore, the reference will always be sales order, but no sales order ID will be specified on the journal header.</span></span></P>



3.  <span data-ttu-id="f2b6f-117">Í hnitanetinu **Kvittanir** skaltu finna línuna sem passar við vöruna sem er skilað og vellja síðan gátreitinn í dálkinum **Velja fyrir komu**.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-117">In the **Receipts** grid, locate the line that matches the item being returned, and then select the check box in the **Select for arrival** column.</span></span>

4.  <span data-ttu-id="f2b6f-118">Til að útiloka ákveðnar línur frá vöruskilamóttökunni, eins og vörur í upprunalegu pöntuninni sem voru ekki teknar með í skilaafhendingunni, skal hreinsa tengda gátreitinn **Velja fyrir komu** í töflunni **Línur** í neðri hluta skjámyndarinnar.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-118">To exclude certain lines from the return receipt, such as items from the original order that were not included in the return shipment, clear the associated **Select for arrival** check boxes in the **Lines** table in the lower part of the form.</span></span>

5.  <span data-ttu-id="f2b6f-119">Smelltu á hnappinn **Upphafskoma** til að búa til komubók.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-119">Click the **Start arrival** button to create an arrival journal.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="f2b6f-120">Hægt er að velja margar skilapantanir í einu og hafa þær allar með í einu komuferli.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-120">You can select multiple return orders and include them all in a single arrival process.</span></span> <span data-ttu-id="f2b6f-121">Hver skilapöntunarlína verður afrituð í samsvarandi vörukomubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-121">Each return order line will be copied into a corresponding item arrival journal line.</span></span></P>

    

    > [!NOTE]
    > <P><span data-ttu-id="f2b6f-122">Þú getur einnig handvirkt búið til komubók með skjámyndinni <STRONG>Vörumóttaka</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-122">You can also manually create an arrival journal by using the <STRONG>Item arrival</STRONG> form.</span></span> 



6.  <span data-ttu-id="f2b6f-123">Smelltu á **Birgðastjórnun** \> **Færslubækur** \> **Vörumóttaka** \> **Vörumóttaka**.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-123">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>

7.  <span data-ttu-id="f2b6f-124">Veldu komubókina sem þú stofnaðir rétt í þessu og smelltu síðan á **Línur** til að opna skjámyndina **Færslubókarlínur, staðsetningar**.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-124">Select the arrival journal that you just created and then click **Lines** to open the **Journal lines, locations** form.</span></span>

8.  <span data-ttu-id="f2b6f-125">Á flipanum **Almennt** skal stilla númerið í reitnum **Magn** ef þess er krafist og síðan úthluta ráðstöfunarkóða í reitnum **Ráðstöfunarkóði**.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-125">On the **General** tab, adjust the number in the **Quantity** field, if it is required, and then assign a disposition code in the **Disposition code** field.</span></span>
    
    <span data-ttu-id="f2b6f-126">Að öðrum kosti er hægt að velja gátreitinn **Stjórnun biðgeymslu** til að senda skilavörurnar í skoðunarferli í tengslum við biðgeymslupöntun.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-126">Alternatively, you can select the **Quarantine management** check box to have the returned items sent through an inspection process in the context of a quarantine order.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="f2b6f-127">Ef sendar eru endursendu vörurnar í gegnum biðgeymslu, er ekki hægt að tilgreina ráðstöfunarkóða.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-127">If you send the returned items through quarantine, you cannot specify a disposition code.</span></span></P>



9.  <span data-ttu-id="f2b6f-128">Smellið á hnappinn **Sannprófa**.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-128">Click the **Validate** button.</span></span>

10. <span data-ttu-id="f2b6f-129">Ef engar villur eru í staðfestingarferlinu skaltu smella á **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-129">If there are no errors in the validation process, click **Post**.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-registration-form"></a><span data-ttu-id="f2b6f-130">Skrá skal móttökuna á skilavörum á skjámyndinni Skráning</span><span class="sxs-lookup"><span data-stu-id="f2b6f-130">Register the receipt of returned items in the Registration form</span></span>

<span data-ttu-id="f2b6f-131">Til viðbótar við að nota skjámyndina **Komuyfirlit** getur þú notað skjámyndina **Skráning** til að skrá komu skilavara.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-131">As an alternative to using the **Arrival overview** form, you can use the **Registration** form to register the arrival of returned items.</span></span>

1.  <span data-ttu-id="f2b6f-132">Smelltu á **Sala og markaðssetning** \> **Almennt** \> **Skilapantanir** \> **Allar skilapantanir**.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-132">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span> <span data-ttu-id="f2b6f-133">Stofna nýja skilapöntun eða opna vöruskilapöntunina frá listanum.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-133">Create a new return order or open the return order from the list.</span></span> <span data-ttu-id="f2b6f-134">Á flýtiflipanum **Línur** skal velja skilapöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-134">On the **Lines** FastTab, select the return order line.</span></span> <span data-ttu-id="f2b6f-135">Smelltu á **Uppfæra línu** og smelltu síðan á **Skráning**.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-135">Click **Update line**, and then click **Registration**.</span></span>

2.  <span data-ttu-id="f2b6f-136">Úthlutaðu ráðstöfunarkóða í reitnum **Ráðstöfunarkóði** og smelltu síðan á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-136">Assign a disposition code in the **Disposition code** field, and then click **OK**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="f2b6f-137">Ekki er hægt að senda vöruna til skoðunar sem biðgeymslupöntun með skjámyndinni <STRONG>Skráning</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-137">It is not possible to send the item for inspection as a quarantine order using the <STRONG>Registration</STRONG> form.</span></span></P>



3.  <span data-ttu-id="f2b6f-138">Í hnitanetinu **Færsla** skal velja færsluna sem á að skrá.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-138">In the **Transactions** grid, select the transaction to be registered.</span></span>

4.  <span data-ttu-id="f2b6f-139">Í hnitanetinu **Skrá núna** skal smella á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-139">In the **Register now** grid, click **Add**.</span></span> <span data-ttu-id="f2b6f-140">Endurtaktu fyrri tvö skrefin þar til allar skilavörurnar birtast í hnitanetinu **Skrá núna**.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-140">Repeat the previous two steps until all of the returned items appear in the **Register now** grid.</span></span>

5.  <span data-ttu-id="f2b6f-141">Smelltu á **Bóka allt**.</span><span class="sxs-lookup"><span data-stu-id="f2b6f-141">Click **Post all**.</span></span>

## <a name="see-also"></a><span data-ttu-id="f2b6f-142">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="f2b6f-142">See also</span></span>

<span data-ttu-id="f2b6f-143">[Komuyfirlit (skjámynd)](https://technet.microsoft.com/en-us/library/hh227654\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="f2b6f-143">[Arrival overview (form)](https://technet.microsoft.com/en-us/library/hh227654\(v=ax.60\))</span></span>

  


