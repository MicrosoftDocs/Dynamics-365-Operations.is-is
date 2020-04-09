---
title: Skrá söluþóknun
description: Þetta efni útskýrir hvernig söluumboð eru reiknuð og skráð.
author: omulvad
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8f9cb895f733442e95cd7008c63942463bbd2cba
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148516"
---
# <a name="register-sales-commissions"></a><span data-ttu-id="47954-103">Skrá söluþóknun</span><span class="sxs-lookup"><span data-stu-id="47954-103">Register sales commissions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="47954-104">Þetta efni útskýrir hvernig söluumboð eru reiknuð og skráð.</span><span class="sxs-lookup"><span data-stu-id="47954-104">This topic explains how sales commissions are calculated and registered.</span></span> <span data-ttu-id="47954-105">Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum.</span><span class="sxs-lookup"><span data-stu-id="47954-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="47954-106">Áður en þessari handbók er ræst þarf að keyra leiðbeiningar sem kallast "Setja upp reglur um söluþóknun" til að tryggja að allar nauðsynlegar uppsetningar á útreikningi sölulauna séu til staðar.</span><span class="sxs-lookup"><span data-stu-id="47954-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="47954-107">Athugið þær tölur viðskiptavina og vara sem voru valdar fyrir sölulaunaferlið og notið þær þegar beðið er um að stofna sölupöntun í þessari handbók.</span><span class="sxs-lookup"><span data-stu-id="47954-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="47954-108">Reikningsfæra sölupöntun sem uppfyllir skilyrði sölumanns fyrir þóknun</span><span class="sxs-lookup"><span data-stu-id="47954-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="47954-109">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Sala og markaðssetning > Sölupantanir > Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="47954-109">In the navigation pane, go to **Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="47954-110">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="47954-110">Select **New**.</span></span>
3. <span data-ttu-id="47954-111">Í reitnum **Viðskiptavinalykill** velurðu skrána sem óskað er eftir af fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="47954-111">In the **Customer account** field, select the desired record from the drop-down menu.</span></span>
4. <span data-ttu-id="47954-112">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="47954-112">Select **OK**.</span></span>
5. <span data-ttu-id="47954-113">Í aðgerðasvæðinu velurðu **Valkostir**.</span><span class="sxs-lookup"><span data-stu-id="47954-113">On the Action Pane, select **Options**.</span></span>
6. <span data-ttu-id="47954-114">Veldu **Breyta skjámynd**.</span><span class="sxs-lookup"><span data-stu-id="47954-114">Select **Change view**.</span></span>
7. <span data-ttu-id="47954-115">Veldu **Hausyfirlit**.</span><span class="sxs-lookup"><span data-stu-id="47954-115">Select **Header view**.</span></span>
8. <span data-ttu-id="47954-116">Útvíkkaðu kaflann **Uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="47954-116">Expand the **Setup** section.</span></span>

    - <span data-ttu-id="47954-117">Gildið í reitnum **Söluflokkur** stendur fyrir flokk sem hefur fengið einum eða fleiri sölumönnum úthlutað.</span><span class="sxs-lookup"><span data-stu-id="47954-117">The value in the **Sales group** field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="47954-118">Fólk innan flokksins eru þau sem fá sölulaun þegar pöntunin er reikningsfærð, samkvæmt fyrirframskilgreindum taxta og dreifingu.</span><span class="sxs-lookup"><span data-stu-id="47954-118">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   
    - <span data-ttu-id="47954-119">Gildi er afritað af viðskiptavinakortinu en hægt er að breyta því ef óskað er.</span><span class="sxs-lookup"><span data-stu-id="47954-119">The value is copied from the Customer card, but you can change it if you wish.</span></span>  
    - <span data-ttu-id="47954-120">Söluflokkurinn er einnig afritaður í sölupöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="47954-120">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="47954-121">Hægt er að breyta þannig að hún sé önnur en sú sem er í haus og/eða á milli lína.</span><span class="sxs-lookup"><span data-stu-id="47954-121">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    - <span data-ttu-id="47954-122">Gildið í svæðinu **Sölulaunaflokkur** stendur fyrir flokk sem var stofnaður fyrir einn eða fleiri viðskiptavini vegna rakningar á sölulaunum.</span><span class="sxs-lookup"><span data-stu-id="47954-122">The value in the **Commission group** field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   
    - <span data-ttu-id="47954-123">Gildi er afritað af viðskiptavinakortinu en hægt er að breyta því ef óskað er.</span><span class="sxs-lookup"><span data-stu-id="47954-123">The value is copied from the Customer card, but you can change it if you wish.</span></span>   

9. <span data-ttu-id="47954-124">Í aðgerðasvæðinu velurðu **Valkostir**.</span><span class="sxs-lookup"><span data-stu-id="47954-124">On the Action Pane, select **Options**.</span></span>
10. <span data-ttu-id="47954-125">Veldu **Breyta skjámynd**.</span><span class="sxs-lookup"><span data-stu-id="47954-125">Select **Change view**.</span></span>
11. <span data-ttu-id="47954-126">Veldu **Línusýn**.</span><span class="sxs-lookup"><span data-stu-id="47954-126">Select **Line view**.</span></span>
12. <span data-ttu-id="47954-127">Í fellivalmyndinni í reitnum **Vörunúmer** skaltu velja vöruna sem þú hefur sett upp fyrir þóknun.</span><span class="sxs-lookup"><span data-stu-id="47954-127">In the drop down menu of the **Item number** field, select the item you have set up for commissions.</span></span> 
13. <span data-ttu-id="47954-128">Í reitnum **Magn** slærðu inn tölu.</span><span class="sxs-lookup"><span data-stu-id="47954-128">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="47954-129">Athugið nettóupphæð línunnar.</span><span class="sxs-lookup"><span data-stu-id="47954-129">Take note of the line's Net amount.</span></span> <span data-ttu-id="47954-130">Hún stendur fyrir sölutekjur sem í þessu dæmi eru grunnurinn fyrir útreikning þóknunar.</span><span class="sxs-lookup"><span data-stu-id="47954-130">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
14. <span data-ttu-id="47954-131">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="47954-131">Select **Save**.</span></span>
15. <span data-ttu-id="47954-132">Í aðgerðasvæðinu velurðu **Reikning**.</span><span class="sxs-lookup"><span data-stu-id="47954-132">On the Action Pane, select **Invoice**.</span></span>
16. <span data-ttu-id="47954-133">Veldu **Reikning**.</span><span class="sxs-lookup"><span data-stu-id="47954-133">Select **Invoice**.</span></span>
17. <span data-ttu-id="47954-134">Útvíkkaðu hlutann **Færibreytur**.</span><span class="sxs-lookup"><span data-stu-id="47954-134">Expand the **Parameters** section.</span></span>
18. <span data-ttu-id="47954-135">Í reitnum **Magn** velurðu **Allt**.</span><span class="sxs-lookup"><span data-stu-id="47954-135">In the **Quantity** field, select **All**.</span></span>
19. <span data-ttu-id="47954-136">Veldu **Já** í reitnum **Bókun**.</span><span class="sxs-lookup"><span data-stu-id="47954-136">Select **Yes** in the **Posting** field.</span></span>
20. <span data-ttu-id="47954-137">Veldu **Í lagi**, veldu síðan **Í lagi** í næsta glugga.</span><span class="sxs-lookup"><span data-stu-id="47954-137">Select **OK**, then select **OK** in the next pane.</span></span> <span data-ttu-id="47954-138">Það gæti tekið um það bil mínútu að bóka færsluna.</span><span class="sxs-lookup"><span data-stu-id="47954-138">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="47954-139">Heimila vinnslu að ljúka og ekki loka síðunni.</span><span class="sxs-lookup"><span data-stu-id="47954-139">Allow the processing to complete and don't close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="47954-140">Fara yfir skráðar söluþóknanir</span><span class="sxs-lookup"><span data-stu-id="47954-140">Review the registered sales commissions</span></span>
1. <span data-ttu-id="47954-141">Á aðgerðarúðunni skal velja **Reikning** og svo **Reikning** aftur.</span><span class="sxs-lookup"><span data-stu-id="47954-141">On the Action Pane, select **Invoice**, then select **Invoice** again.</span></span>
2. <span data-ttu-id="47954-142">Á aðgerðarúðunni skal velja **Reikning** og svo **Þóknunarfærslur**.</span><span class="sxs-lookup"><span data-stu-id="47954-142">On the Action Pane, select **Invoice**, then select **Commission transactions**.</span></span>

    - <span data-ttu-id="47954-143">Flipinn **Yfirlit** birtir línur sem sýna upphæðir sölulauna sem greiða á sölufulltrúum sem eru tengdir reikningsfærðu sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="47954-143">The **Overview** tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="47954-144">Endurskoðum nú upplýsingarnar.</span><span class="sxs-lookup"><span data-stu-id="47954-144">Let's review the details.</span></span>  
    - <span data-ttu-id="47954-145">Ef handbókin "Setja upp reglur söluþóknunar" var notuð til að setja upp flokk **Sölulauna** eru tveir sölumenn til að móttaka sölulaun og sölulaununum er skipt jafnt á milli þeirra.</span><span class="sxs-lookup"><span data-stu-id="47954-145">If you used the "Set up sales commission rules" guide to set up the **Commission sales** group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    - <span data-ttu-id="47954-146">Í þessu dæmi er heildarupphæð þóknun reiknuð sem hlutfall sölutekna (nettóupphæð pöntunarlínu).</span><span class="sxs-lookup"><span data-stu-id="47954-146">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>  
3. <span data-ttu-id="47954-147">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="47954-147">Close the page.</span></span>
4. <span data-ttu-id="47954-148">Veldu **Fylgiskjal**.</span><span class="sxs-lookup"><span data-stu-id="47954-148">Select **Voucher**.</span></span> <span data-ttu-id="47954-149">Hægt er að skoða færslur fylgiskjala fyrir upphæðir sölulauna sem hafa verið bókaðar í forskilgreindu þóknunarkostnaður og þóknun lykla lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="47954-149">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  

