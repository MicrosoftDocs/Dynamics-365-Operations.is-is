---
title: Uppfylla sölusamninga
description: Þessi verklýsing sýnir hvernig uppfylla sölusamning með því að tengja sölupantanir við hana.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesTableListPage, SalesTable, AgreementLine, SalesCreateOrder,  SalesEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7549d0c2a3cfa0feb26a641bbc41702b4b21158
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833955"
---
# <a name="fulfill-sales-agreements"></a><span data-ttu-id="1b9a2-103">Uppfylla sölusamninga</span><span class="sxs-lookup"><span data-stu-id="1b9a2-103">Fulfill sales agreements</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1b9a2-104">Þessi verklýsing sýnir hvernig uppfylla sölusamning með því að tengja sölupantanir við hana.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-104">This procedure shows you how to fulfill a sales agreement by associating sales orders with it.</span></span> <span data-ttu-id="1b9a2-105">Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="1b9a2-106">Áður en þessari handbók er ræst, ganga úr skugga um þú sért með virkan sölusamnings af gerðinni "skuldbinding um gildi afurðar".</span><span class="sxs-lookup"><span data-stu-id="1b9a2-106">Before starting this guide, make sure you have an effective sales agreement of type "Product value commitment".</span></span> <span data-ttu-id="1b9a2-107">Einnig er hægt að keyra leiðarvísi fyrir verk kallast "Stofna sölusamninga".</span><span class="sxs-lookup"><span data-stu-id="1b9a2-107">Alternatively, you can run the task guide called "Create sales agreements".</span></span>  




## <a name="release-a-sales-order-from-the-agreement"></a><span data-ttu-id="1b9a2-108">Losa sölupöntun úr samninginn</span><span class="sxs-lookup"><span data-stu-id="1b9a2-108">Release a sales order from the agreement</span></span>
1. <span data-ttu-id="1b9a2-109">Fara í Sölu og markaðssetningu > Sölusamningar > Sölusamninga.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-109">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="1b9a2-110">Opna samning sem á að losa pöntunina gagnvart á listanum.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-110">In the list, open the agreement against which you want to release the order.</span></span>
3. <span data-ttu-id="1b9a2-111">Á Aðgerðasvæðinu skal smellt á sölusamningur.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-111">On the Action Pane, click Sales agreement.</span></span>
4. <span data-ttu-id="1b9a2-112">Smellt er á úttektarpöntun.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-112">Click Release order.</span></span>
    * <span data-ttu-id="1b9a2-113">Eins og texti yfir Stofna úttektarpöntun bendir á, eru upplýsingar sem þarf fyrir sölupöntunarlínur verður mismunandi eftir því hvort samningurinn er byggður á magni eða virði.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-113">As the text on top of the  Create release order page points out, the details required for the sales order lines will differ depending on whether the agreement is quantity- or value-based.</span></span>  
    * <span data-ttu-id="1b9a2-114">Samningurinn í þessari handbók er af gerðinni "skuldbinding um gildi afurðar".</span><span class="sxs-lookup"><span data-stu-id="1b9a2-114">The agreement in this guide is of type "Product value commitment".</span></span> <span data-ttu-id="1b9a2-115">Þetta er ástæðan fyrir því að línuhluti þessarar síðu er auður.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-115">This is why the Lines section of this page is blank.</span></span> <span data-ttu-id="1b9a2-116">Ef skuldbindingin var byggð á magni myndu upplýsingar línunnar vera afritaðar úr samningnum.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-116">If the commitment was based on quantity, the line information would be copied from the agreement.</span></span>  
5. <span data-ttu-id="1b9a2-117">Smellið á „Stofna“.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-117">Click Create.</span></span>
    * <span data-ttu-id="1b9a2-118">Skilaboðin tilkynnir sölupöntun hefur verið stofnuð.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-118">The message informs you that a sales order has been created.</span></span> <span data-ttu-id="1b9a2-119">Þar sem pöntunin inniheldur engar línur þarf að bæta við upplýsingum um pöntunarlínu til að ljúka útgáfuferlinu.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-119">Since the order does not contain any lines, you must add order line details to complete the release process.</span></span>   
6. <span data-ttu-id="1b9a2-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-120">Close the page.</span></span>
7. <span data-ttu-id="1b9a2-121">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-121">Close the page.</span></span>
8. <span data-ttu-id="1b9a2-122">Fara í Sölu og markaðssetningu > sölupöntun > Allar sölupantanir</span><span class="sxs-lookup"><span data-stu-id="1b9a2-122">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
9. <span data-ttu-id="1b9a2-123">Finna og opna pöntun var stofnuð í kjölfar þess að pöntunina var losa í fyrra verki á listanum.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-123">In the list, find and open the order that was created as the result of the order release in the previous task.</span></span>
10. <span data-ttu-id="1b9a2-124">Smella á bæta Við línu.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-124">Click Add line.</span></span>
11. <span data-ttu-id="1b9a2-125">Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-125">In the Item number field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="1b9a2-126">Í svæðinu vörunúmer, Færa inn eða velja vöru sem er tilgreind í tengdum sölusamningnum.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-126">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
13. <span data-ttu-id="1b9a2-127">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="1b9a2-128">Gangið úr skugga um að færa inn magn sem knýr nettóupphæð undir gildi tengt sölusamning.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-128">Make sure that you enter a quantity that brings the Net amount under the value of the associated sales agreement.</span></span>  
    * <span data-ttu-id="1b9a2-129">Athugið þar sem sölupöntunin er tengd við samning, er umsamin afsláttarprósenta beitt í pöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-129">Notice that because the sales order is linked to the agreement, the negotiated discount percent is applied to the order line.</span></span>  
14. <span data-ttu-id="1b9a2-130">Smellið á „Uppfæra línu“.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-130">Click Update line.</span></span>
15. <span data-ttu-id="1b9a2-131">Smellið á „Viðhengi“.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-131">Click Attached.</span></span>
    * <span data-ttu-id="1b9a2-132">Tengdar síða samnings sýnir Kenni og skilmálum samningsins þaðan sem línan er losuð frá.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-132">The Attached agreement page shows the ID and terms of the agreement from which the line is released.</span></span>  
16. <span data-ttu-id="1b9a2-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-133">Close the page.</span></span>
17. <span data-ttu-id="1b9a2-134">Smellið á „Almennt“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-134">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="1b9a2-135">Smelltu á tengdur Sölusamningar</span><span class="sxs-lookup"><span data-stu-id="1b9a2-135">Click Attached sales agreement.</span></span>
19. <span data-ttu-id="1b9a2-136">Víkkið út hlutann „Upplýsingar um línu“.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-136">Expand the Line details section.</span></span>
20. <span data-ttu-id="1b9a2-137">Smelltu á uppfyllingarflipann.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-137">Click the Fulfillment tab.</span></span>
    * <span data-ttu-id="1b9a2-138">Uppfyllingarflipi sýnir yfirlit yfir allar sölupöntunarlínur sem eru tengdar við skuldbindingu, og stöðu uppfyllingar þeirra, sem og upphæð eða magn sem enn hefur ekki verið losuð.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-138">The Fulfillment tab shows a summary of all the sales order lines that are associated with this commitment, and their fulfillment state, as well as the amount or quantity that has not yet been released.</span></span>   
21. <span data-ttu-id="1b9a2-139">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-139">Close the page.</span></span>
22. <span data-ttu-id="1b9a2-140">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-140">Close the page.</span></span>
23. <span data-ttu-id="1b9a2-141">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-141">Close the page.</span></span>

## <a name="apply-sales-agreement-in-the-order-process"></a><span data-ttu-id="1b9a2-142">Jafna sölusamninga í pöntunarferli</span><span class="sxs-lookup"><span data-stu-id="1b9a2-142">Apply sales agreement in the order process</span></span>
1. <span data-ttu-id="1b9a2-143">Fara í Sölu og markaðssetningu > sölupöntun > Allar sölupantanir</span><span class="sxs-lookup"><span data-stu-id="1b9a2-143">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="1b9a2-144">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-144">Click New.</span></span>
3. <span data-ttu-id="1b9a2-145">Í reitnum Reikningur viðskiptavina skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-145">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="1b9a2-146">Finna og velja viðskiptavinar sem tilgreindur er í sölusamningnum á listanum.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-146">In the list, find and select the customer specified on the sales agreement.</span></span>
5. <span data-ttu-id="1b9a2-147">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-147">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="1b9a2-148">Útvíkka eða draga saman hlutann Almennt.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-148">Expand the General section.</span></span>
7. <span data-ttu-id="1b9a2-149">Í reitnum kenni sölusamningur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-149">In the Sales agreement ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="1b9a2-150">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-150">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="1b9a2-151">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-151">Click Yes.</span></span>
10. <span data-ttu-id="1b9a2-152">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-152">Click OK.</span></span>
11. <span data-ttu-id="1b9a2-153">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-153">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="1b9a2-154">Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-154">In the Item number field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="1b9a2-155">Í svæðinu vörunúmer, Færa inn eða velja vöru sem er tilgreind í tengdum sölusamningnum.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-155">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
14. <span data-ttu-id="1b9a2-156">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-156">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="1b9a2-157">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-157">Click Save.</span></span>
16. <span data-ttu-id="1b9a2-158">Smellið á „Tiltekt og pökkun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-158">On the Action Pane, click Pick and pack.</span></span>
17. <span data-ttu-id="1b9a2-159">Smellið á „Bóka fylgiseðil“.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-159">Click Post packing slip.</span></span>
18. <span data-ttu-id="1b9a2-160">Víkkið út færibreytuhlutann.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-160">Expand the Parameters section.</span></span>
19. <span data-ttu-id="1b9a2-161">Velja skal Já í reitnum Bókun.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-161">Select Yes in the Posting field.</span></span>
20. <span data-ttu-id="1b9a2-162">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-162">Click OK.</span></span>
21. <span data-ttu-id="1b9a2-163">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-163">Click OK.</span></span>
22. <span data-ttu-id="1b9a2-164">Smellið á „Almennt“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-164">On the Action Pane, click General.</span></span>
23. <span data-ttu-id="1b9a2-165">Smelltu á tengdur Sölusamningar</span><span class="sxs-lookup"><span data-stu-id="1b9a2-165">Click Attached sales agreement.</span></span>
24. <span data-ttu-id="1b9a2-166">Smelltu á uppfyllingarflipann.</span><span class="sxs-lookup"><span data-stu-id="1b9a2-166">Click the Fulfillment tab.</span></span>

