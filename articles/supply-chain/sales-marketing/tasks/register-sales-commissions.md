--- 
title: "Skrá söluþóknun"
description: "Þessi verklýsing sýnir hvernig sölulaun eru reiknuð og skráð."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d21f9047dcea0af59c24339ebb57e8eabe3950d4
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="register-sales-commissions"></a><span data-ttu-id="c735b-103">Skrá söluþóknun</span><span class="sxs-lookup"><span data-stu-id="c735b-103">Register sales commissions</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c735b-104">Þessi verklýsing sýnir hvernig sölulaun eru reiknuð og skráð.</span><span class="sxs-lookup"><span data-stu-id="c735b-104">This procedure shows you how sales commissions are calculated and registered.</span></span> <span data-ttu-id="c735b-105">Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum.</span><span class="sxs-lookup"><span data-stu-id="c735b-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="c735b-106">Áður en þessari handbók er ræst þarf að keyra leiðbeiningar sem kallast "Setja upp reglur um söluþóknun" til að tryggja að allar nauðsynlegar uppsetningar á útreikningi sölulauna séu til staðar.</span><span class="sxs-lookup"><span data-stu-id="c735b-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="c735b-107">Athugið þær tölur viðskiptavina og vara sem voru valdar fyrir sölulaunaferlið og notið þær þegar beðið er um að stofna sölupöntun í þessari handbók.</span><span class="sxs-lookup"><span data-stu-id="c735b-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="c735b-108">Reikningsfæra sölupöntun sem uppfyllir skilyrði sölumanns fyrir þóknun</span><span class="sxs-lookup"><span data-stu-id="c735b-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="c735b-109">Fara í Sölu og markaðssetningu > sölupöntun > Allar sölupantanir</span><span class="sxs-lookup"><span data-stu-id="c735b-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="c735b-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="c735b-110">Click New.</span></span>
3. <span data-ttu-id="c735b-111">Í reitnum Reikningur viðskiptavina skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="c735b-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="c735b-112">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="c735b-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c735b-113">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="c735b-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c735b-114">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c735b-114">Click OK.</span></span>
7. <span data-ttu-id="c735b-115">Í aðgerðasvæðinu er smellt á valkostir.</span><span class="sxs-lookup"><span data-stu-id="c735b-115">On the Action Pane, click Options.</span></span>
8. <span data-ttu-id="c735b-116">Smellið á skoða Breytingu.</span><span class="sxs-lookup"><span data-stu-id="c735b-116">Click Change view.</span></span>
9. <span data-ttu-id="c735b-117">Smellið á skoða Haus.</span><span class="sxs-lookup"><span data-stu-id="c735b-117">Click Header view.</span></span>
10. <span data-ttu-id="c735b-118">Víkka út hlutann Uppsetning.</span><span class="sxs-lookup"><span data-stu-id="c735b-118">Expand the Setup section.</span></span>
    * <span data-ttu-id="c735b-119">Gildið í reitnum Söluflokkur stendur fyrir flokk með einn eða fleiri sölumenn sem úthlutað.</span><span class="sxs-lookup"><span data-stu-id="c735b-119">The value in the Sales group field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="c735b-120">Fólk innan flokksins eru þau sem fá sölulaun þegar pöntunin er reikningsfærð, samkvæmt fyrirframskilgreindum taxta og dreifingu.</span><span class="sxs-lookup"><span data-stu-id="c735b-120">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   <span data-ttu-id="c735b-121">Gildi er afritað af viðskiptavinakortinu en hægt er að breyta því ef óskað er.</span><span class="sxs-lookup"><span data-stu-id="c735b-121">The value is copied from the Customer card, but you can change it if you wish.</span></span>  <span data-ttu-id="c735b-122">Söluflokkurinn er einnig afritaður í sölupöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="c735b-122">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="c735b-123">Hægt er að breyta þannig að hún sé önnur en sú sem er í haus og/eða á milli lína.</span><span class="sxs-lookup"><span data-stu-id="c735b-123">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    * <span data-ttu-id="c735b-124">Gildið í svæðinu Sölulaunaflokkur stendur fyrir flokk sem var stofnaður fyrir einn eða fleiri vegna rakningar á sölulaunum.</span><span class="sxs-lookup"><span data-stu-id="c735b-124">The value in the Commission group field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   <span data-ttu-id="c735b-125">Gildi er afritað af viðskiptavinakortinu en hægt er að breyta því ef óskað er.</span><span class="sxs-lookup"><span data-stu-id="c735b-125">The value is copied from the Customer card, but you can change it if you wish.</span></span>   
11. <span data-ttu-id="c735b-126">Í aðgerðasvæðinu er smellt á valkostir.</span><span class="sxs-lookup"><span data-stu-id="c735b-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="c735b-127">Smellið á skoða Breytingu.</span><span class="sxs-lookup"><span data-stu-id="c735b-127">Click Change view.</span></span>
13. <span data-ttu-id="c735b-128">Smellið á Línuyfirlit.</span><span class="sxs-lookup"><span data-stu-id="c735b-128">Click Line view.</span></span>
14. <span data-ttu-id="c735b-129">Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="c735b-129">In the Item number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="c735b-130">Á listanum, skal velja vöru sem er uppsett fyrir þóknanir.</span><span class="sxs-lookup"><span data-stu-id="c735b-130">In the list, select the item you have set up for commissions.</span></span> 
16. <span data-ttu-id="c735b-131">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="c735b-131">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="c735b-132">Athugið nettóupphæð línunnar.</span><span class="sxs-lookup"><span data-stu-id="c735b-132">Take note of the line's Net amount.</span></span> <span data-ttu-id="c735b-133">Hún stendur fyrir sölutekjur sem í þessu dæmi eru grunnurinn fyrir útreikning þóknunar.</span><span class="sxs-lookup"><span data-stu-id="c735b-133">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
17. <span data-ttu-id="c735b-134">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="c735b-134">Click Save.</span></span>
18. <span data-ttu-id="c735b-135">Smellið á „Reikningur“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="c735b-135">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="c735b-136">Smellið á „Reikningur“.</span><span class="sxs-lookup"><span data-stu-id="c735b-136">Click Invoice.</span></span>
20. <span data-ttu-id="c735b-137">Víkkið út færibreytuhlutann.</span><span class="sxs-lookup"><span data-stu-id="c735b-137">Expand the Parameters section.</span></span>
21. <span data-ttu-id="c735b-138">Veljið „Allt“ á svæðinu „Magn“.</span><span class="sxs-lookup"><span data-stu-id="c735b-138">In the Quantity field, select 'All'.</span></span>
22. <span data-ttu-id="c735b-139">Velja skal Já í reitnum Bókun.</span><span class="sxs-lookup"><span data-stu-id="c735b-139">Select Yes in the Posting field.</span></span>
23. <span data-ttu-id="c735b-140">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c735b-140">Click OK.</span></span>
24. <span data-ttu-id="c735b-141">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c735b-141">Click OK.</span></span>
    * <span data-ttu-id="c735b-142">Það gæti tekið um það bil mínútu að bóka færsluna.</span><span class="sxs-lookup"><span data-stu-id="c735b-142">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="c735b-143">Heimila vinnslu að ljúka og ekki loka síðunni.</span><span class="sxs-lookup"><span data-stu-id="c735b-143">Allow the processing to complete and don’t close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="c735b-144">Fara yfir skráðar söluþóknanir</span><span class="sxs-lookup"><span data-stu-id="c735b-144">Review the registered sales commissions</span></span>
1. <span data-ttu-id="c735b-145">Smellið á „Reikningur“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="c735b-145">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="c735b-146">Smellið á „Reikningur“.</span><span class="sxs-lookup"><span data-stu-id="c735b-146">Click Invoice.</span></span>
3. <span data-ttu-id="c735b-147">Smellið á „Reikningur“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="c735b-147">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="c735b-148">Smelltu á Þóknunarfærslur.</span><span class="sxs-lookup"><span data-stu-id="c735b-148">Click Commission transactions.</span></span>
    * <span data-ttu-id="c735b-149">Yfirlitsflipinn birtir línur sem sýna upphæðir sölulauna sem greiða á sölufulltrúum sem eru tengdir reikningsfærðu sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="c735b-149">The Overview tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="c735b-150">Endurskoðum nú upplýsingarnar.</span><span class="sxs-lookup"><span data-stu-id="c735b-150">Let's review the details.</span></span>     
    * <span data-ttu-id="c735b-151">Ef handbókin "Setja upp reglur sölu þóknun" var notuð til að setja upp sölulaunaflokk eru tveir sölumenn til að móttaka sölulaun og sölulaununum er skipt skipt jafnt á milli þeirra.</span><span class="sxs-lookup"><span data-stu-id="c735b-151">If you used the "Set up sales commission rules" guide to set up the Commission sales group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    * <span data-ttu-id="c735b-152">Í þessu dæmi er heildarupphæð þóknun reiknuð sem hlutfall sölutekna (nettóupphæð pöntunarlínu).</span><span class="sxs-lookup"><span data-stu-id="c735b-152">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>   
5. <span data-ttu-id="c735b-153">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c735b-153">Close the page.</span></span>
6. <span data-ttu-id="c735b-154">Smellt er á Fylgiskjalið.</span><span class="sxs-lookup"><span data-stu-id="c735b-154">Click Voucher.</span></span>
    * <span data-ttu-id="c735b-155">Hægt er að skoða færslur fylgiskjala fyrir upphæðir sölulauna sem hafa verið bókaðar í forskilgreindu þóknunarkostnaður og þóknun lykla lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="c735b-155">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  


