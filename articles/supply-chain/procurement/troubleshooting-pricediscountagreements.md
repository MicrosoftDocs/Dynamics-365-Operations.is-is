---
title: Villuleita verð, afslætti, samninga og eftirágreiddan afslátt
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með verð, afslætti, samninga og eftirágreidda afslætti.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 14fdddabde7739cbf9ba0fcee0fa0b8b816e74dd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007367"
---
# <a name="troubleshoot-prices-discounts-agreements-and-rebates"></a><span data-ttu-id="614c4-103">Villuleita verð, afslætti, samninga og eftirágreiddan afslátt</span><span class="sxs-lookup"><span data-stu-id="614c4-103">Troubleshoot prices, discounts, agreements, and rebates</span></span>

<span data-ttu-id="614c4-104">Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með verð, afslætti, samninga og eftirágreidda afslætti.</span><span class="sxs-lookup"><span data-stu-id="614c4-104">This topic describes how to fix issues that you might encounter while you work with prices, discounts, agreements, and rebates.</span></span>

## <a name="i-cant-link-a-purchase-agreement-to-a-purchase-order-line-after-the-purchase-order-is-created"></a><span data-ttu-id="614c4-105">Ekki er hægt að tengja innkaupasamning við innkaupapöntunarlínu eftir að innkaupapöntunin er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="614c4-105">I can't link a purchase agreement to a purchase order line after the purchase order is created.</span></span>

<span data-ttu-id="614c4-106">Innkaupasamningur verður að vera tengdur við innkaupapöntun þegar innkaupapöntunin er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="614c4-106">A purchase agreement must be associated with a purchase order when the purchase order is created.</span></span> <span data-ttu-id="614c4-107">Annars er ekki hægt að tengja innkaupapöntunarlínur við innkaupasamningslínur.</span><span class="sxs-lookup"><span data-stu-id="614c4-107">Otherwise, purchase order lines can't be associated with purchase agreement lines.</span></span>

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a><span data-ttu-id="614c4-108">Hvaða athugun ræsir skilaboðin „Uppfæra verð og afslætti sem færð voru inn handvirkt eða með ytra skjali“?</span><span class="sxs-lookup"><span data-stu-id="614c4-108">What check triggers the "Update prices and discounts entered manually or external document" message?</span></span>

<span data-ttu-id="614c4-109">Þegar sendingardagsetningu er breytt gætu borist skilaboð þar sem stendur „Uppfæra verð og afslætti sem færð voru inn handvirkt eða með ytra skjali.“</span><span class="sxs-lookup"><span data-stu-id="614c4-109">When you change the shipping date, you might receive a message that states, "Update prices and discounts entered manually or external document."</span></span> <span data-ttu-id="614c4-110">Þessi skilaboð berast vegna þess að ef sendingardagsetningunni hefur verið breytt gæti annar verð- eða sölusamningur verið ræstur og valdið breytingu á verði.</span><span class="sxs-lookup"><span data-stu-id="614c4-110">You receive this message because, if the shipping date is changed, a different trade or sales agreement might be triggered and cause a price change.</span></span> <span data-ttu-id="614c4-111">Breyting á sendingardagsetningunni getur einnig haft áhrif á vöruhúsaáætlanir og aðrar tengdar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="614c4-111">A change to the shipping date can also affect warehouse schedules and other related information.</span></span>

<span data-ttu-id="614c4-112">Skilaboðin eru ræst þegar einhverjum dagsetninganna eða færibreytanna er breytt.</span><span class="sxs-lookup"><span data-stu-id="614c4-112">The message is triggered whenever any of the dates or some other parameters are changed.</span></span> <span data-ttu-id="614c4-113">Tilgangur skilaboðanna er að ganga úr skugga um að þú gerir þér grein fyrir verðbreytingum sem geta átt sér stað vegna þessara breytinga.</span><span class="sxs-lookup"><span data-stu-id="614c4-113">The purpose of the message is to make sure that you're aware of price changes that can occur because of those changes.</span></span>

<span data-ttu-id="614c4-114">Skilaboðin eru kvaðning um mat á verðsamningi.</span><span class="sxs-lookup"><span data-stu-id="614c4-114">The message is the trade agreement evaluation (TAE) prompt.</span></span> <span data-ttu-id="614c4-115">Ítarlegri lýsingu má finna í [Reglur um mat á verðsamningi](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).</span><span class="sxs-lookup"><span data-stu-id="614c4-115">For a full description, see [Trade agreement evaluation policies](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).</span></span>

## <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a><span data-ttu-id="614c4-116">Kvittun innkaupapöntunar inniheldur ekki öll gjöld.</span><span class="sxs-lookup"><span data-stu-id="614c4-116">A purchase order receipt doesn't include all charges.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="614c4-117">Framkallaðu vandamálið</span><span class="sxs-lookup"><span data-stu-id="614c4-117">Reproduce the issue</span></span>

<span data-ttu-id="614c4-118">Eftirfarandi ferli sýnir eina leið til að endurtaka málið.</span><span class="sxs-lookup"><span data-stu-id="614c4-118">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="614c4-119">Á síðunni **Færibreytur innkaupa og aðfanga**, í flipanum **Afhending**, skal ganga úr skugga um valkosturinn **Mynda gjöld á innhreyfingarskjali afurða** sé stilltur á *Já*.</span><span class="sxs-lookup"><span data-stu-id="614c4-119">On the **Procurement and sourcing parameters** page, on the **Delivery** tab, make sure that the **Generate charges on product receipt** option is set to *Yes*.</span></span>
1. <span data-ttu-id="614c4-120">Stofna innkaupapöntun sem inniheldur gjöld.</span><span class="sxs-lookup"><span data-stu-id="614c4-120">Create a purchase order that includes charges.</span></span>
1. <span data-ttu-id="614c4-121">Staðfesta innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="614c4-121">Confirm the purchase order.</span></span>
1. <span data-ttu-id="614c4-122">Takið á móti innkaupapöntuninni.</span><span class="sxs-lookup"><span data-stu-id="614c4-122">Receive the purchase order.</span></span>
1. <span data-ttu-id="614c4-123">Skoðið samtölu kvittunarinnar og berið hana saman við samtöluna sem búist var við.</span><span class="sxs-lookup"><span data-stu-id="614c4-123">Look at the receipt total, and compare it to the expected total.</span></span>
1. <span data-ttu-id="614c4-124">Takið eftir að ekki öll gjöld eru tekin með í kvittun innkaupapöntunar.</span><span class="sxs-lookup"><span data-stu-id="614c4-124">Notice that not all the charges are included on the purchase order receipt.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="614c4-125">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="614c4-125">Issue resolution</span></span>

<span data-ttu-id="614c4-126">Úrlausnin fer eftir því hvernig þessi ýmsu gjöld hafa verið sett upp.</span><span class="sxs-lookup"><span data-stu-id="614c4-126">The resolution depends on the way that the miscellaneous charges have been set up.</span></span> <span data-ttu-id="614c4-127">Upplýsingar um hvernig á að setja upp ýmis gjöld til að uppfylla kröfur, er að finna í eftirfarandi bloggfærslu: [Bóka gjöld við móttöku afurðar](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span><span class="sxs-lookup"><span data-stu-id="614c4-127">For information about how to set up miscellaneous charges to meet your requirements, see the following blog post: [Post misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="trade-agreement-prices-and-discounts-arent-applied-on-sales-or-purchase-order-lines-that-are-imported-through-data-management"></a><span data-ttu-id="614c4-128">Verð og afslættir verðsamninga eru ekki notuð á sölu-eða innkaupapöntunarlínum sem eru fluttar inn í gegnum gagnastjórnun.</span><span class="sxs-lookup"><span data-stu-id="614c4-128">Trade agreement prices and discounts aren't applied on sales or purchase order lines that are imported through data management.</span></span>

### <a name="issue-description"></a><span data-ttu-id="614c4-129">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="614c4-129">Issue description</span></span>

<span data-ttu-id="614c4-130">Verðsamningar sem eiga við um sölu- og innkaupapöntunarlínur eru ekki notaðir í línum sem eru fluttar inn í gegnum gagnastjórnun.</span><span class="sxs-lookup"><span data-stu-id="614c4-130">Trade agreements that are applicable to sales or purchase order lines aren't applied on lines that are imported through data management.</span></span> <span data-ttu-id="614c4-131">Hins vegar eru notaðir sömu verðsamningar á sölu- eða innkaupapöntunarlínum sem eru búnar til handvirkt.</span><span class="sxs-lookup"><span data-stu-id="614c4-131">However, the same trade agreements are applied on sales or purchase order lines that are manually created.</span></span>

### <a name="reason-for-the-issue"></a><span data-ttu-id="614c4-132">Ástæða fyrir vandamálinu</span><span class="sxs-lookup"><span data-stu-id="614c4-132">Reason for the issue</span></span>

<span data-ttu-id="614c4-133">Ef innkaupapöntunarlínur sem eru fluttar inn gegnum gagnastjórnun innihalda þegar verðupplýsingar, verður verðsamningurinn ekki endurmetinn fyrir þessar línur.</span><span class="sxs-lookup"><span data-stu-id="614c4-133">If purchase order lines that are imported via data management already include price information, the trade agreement won't be reevaluated for those lines.</span></span> <span data-ttu-id="614c4-134">Til dæmis, ef **Prósenta línuafsláttar** eða eitthvert gildi fyrir verð eða afslátt er sett inn í línu, þá verða verðsamningar ekki skoðaðir fyrir þessa línu.</span><span class="sxs-lookup"><span data-stu-id="614c4-134">For example, if **Line discount percentage** or any of the price and discount values is set for a line, then trade agreements will not be looked up for that line.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="614c4-135">Lausn á vandanum</span><span class="sxs-lookup"><span data-stu-id="614c4-135">Issue workaround</span></span>

<span data-ttu-id="614c4-136">Búist er við þessari hegðun og hún er svipuð bæði fyrir sölupantanir og innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="614c4-136">This behavior is expected, and is similar for both sales orders and purchase orders.</span></span>

<span data-ttu-id="614c4-137">Leið framhjá þessu er að flytja inn innkaupapöntunarlínurnar án þess að setja inn neinar verðupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="614c4-137">As a workaround, import the purchase order lines without setting any price information.</span></span> <span data-ttu-id="614c4-138">Verðsamningarnir verða þá notaðir og innkaupapöntunarlínurnar verða uppfærðar á grundvelli skilgreindra verðsamninga.</span><span class="sxs-lookup"><span data-stu-id="614c4-138">The trade agreements will then be applied, and the purchase order lines will be updated based on the defined trade agreements.</span></span>

## <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a><span data-ttu-id="614c4-139">Eftirágreiddur afsláttur lánardrottins er ekki uppsafnaður samkvæmt reikningum.</span><span class="sxs-lookup"><span data-stu-id="614c4-139">A vendor rebate isn't cumulated based on invoices.</span></span>

### <a name="issue-description"></a><span data-ttu-id="614c4-140">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="614c4-140">Issue description</span></span>

<span data-ttu-id="614c4-141">Ef reikningar sem eru bókaðir eru með mismunandi gjalddögum, koma þessir reikningar ekki fram í eftirágreiddum afslætti lánardrottins sem er myndaður úr þeim.</span><span class="sxs-lookup"><span data-stu-id="614c4-141">If invoices that are posted have different due dates, those invoices aren't reflected in vendor rebates that are generated from them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="614c4-142">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="614c4-142">Issue resolution</span></span>

<span data-ttu-id="614c4-143">Samkvæmt hönnun er gjalddagi ekki tekinn til greina þegar eftirágreiddur afsláttur lánardrottins er reiknaður.</span><span class="sxs-lookup"><span data-stu-id="614c4-143">By design, the due date isn't considered when the vendor rebate is calculated.</span></span> <span data-ttu-id="614c4-144">Íhugið að sérsníða kerfið þannig að gjalddaginn og tengslin við reikninginn séu augljósari með tilliti til raunverulegs eftirágreidds afsláttar lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="614c4-144">Consider customizing the system so that the due date and the relation to the invoice are more apparent with respect to the actual vendor rebate.</span></span>

## <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a><span data-ttu-id="614c4-145">Einingaverð á innkaupapöntunum eru ekki reiknuð út á grundvelli umreiknings einingar.</span><span class="sxs-lookup"><span data-stu-id="614c4-145">Unit prices on purchase orders aren't calculated based on the unit conversion.</span></span>

### <a name="issue-description"></a><span data-ttu-id="614c4-146">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="614c4-146">Issue description</span></span>

<span data-ttu-id="614c4-147">Þegar einingu er breytt í innkaupapöntun eru verð verðsamnings ekki endurreiknuð samkvæmt skilgreiningum einingaumreiknings.</span><span class="sxs-lookup"><span data-stu-id="614c4-147">When a unit is changed on a purchase order, trade agreement prices aren't recalculated according to unit conversion definitions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="614c4-148">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="614c4-148">Issue resolution</span></span>

<span data-ttu-id="614c4-149">Verð eru alltaf fengin úr verðsamningum (eða öðrum verðstillingum í kerfinu, svo sem sölusamningum eða vöruverði) og þeir eru stilltir fyrir einingu.</span><span class="sxs-lookup"><span data-stu-id="614c4-149">Prices are always obtained from trade agreements (or other price settings in the system, such as sales agreements or item prices), and they are set for a unit.</span></span>

<span data-ttu-id="614c4-150">Ef einingunni er breytt í pöntunarlínu, leitar kerfið að verði fyrir nýju eininguna og notar það verð.</span><span class="sxs-lookup"><span data-stu-id="614c4-150">If the unit is changed on an order line, the system looks for a price for the new unit and applies that price.</span></span> <span data-ttu-id="614c4-151">Ef ekkert verð finnst fyrir eininguna setur kerfið ekki verð á.</span><span class="sxs-lookup"><span data-stu-id="614c4-151">If no price is found for the unit, the system doesn't apply a price.</span></span> <span data-ttu-id="614c4-152">Ekki er hægt að nota umreikning einingar til að endurreikna verðið í aðra einingu.</span><span class="sxs-lookup"><span data-stu-id="614c4-152">The unit conversion can't be used to recalculate the price into another unit.</span></span> <span data-ttu-id="614c4-153">Fræðilega séð er verðið fyrir einn kassa af tíu ekki endilega jafnt og tífalt verðið á einum kassa.</span><span class="sxs-lookup"><span data-stu-id="614c4-153">Theoretically, the price for one box of ten might not equal ten times the price of one box.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="614c4-154">Lausn á vandanum</span><span class="sxs-lookup"><span data-stu-id="614c4-154">Issue workaround</span></span>

<span data-ttu-id="614c4-155">Ein leið framhjá þessu vandamáli er að ganga úr skugga um til séu verðsamningar fyrir einingarnar sem búist er við að verði notaðar í pöntunarlínum fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="614c4-155">One way to work around this issue is to make sure that there are trade agreements for the units that you expect will be used on order lines for the item.</span></span>

## <a name="currency-conversion-issues-occur-with-trade-agreements"></a><span data-ttu-id="614c4-156">Vandamál varðandi umreikning gjaldmiðils eiga sér stað með verðsamningum.</span><span class="sxs-lookup"><span data-stu-id="614c4-156">Currency conversion issues occur with trade agreements.</span></span>

<span data-ttu-id="614c4-157">Verð verðsamninga eru ekki endurreiknuð samkvæmt gjaldmiðlinum þegar gjaldmiðillinn er annar í innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="614c4-157">Trade agreement prices aren't recalculated according to the currency when the currency differs on a purchase order.</span></span>

<span data-ttu-id="614c4-158">Eiginleikinn *Almennur gjaldmiðill* gerir kleift að skilgreina verð og afslætti í aðeins einum gjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="614c4-158">The *Generic currency* feature lets you define prices and discounts in only one currency.</span></span> <span data-ttu-id="614c4-159">Síðan er hægt að umbreyta í aðra gjaldmiðla eftir því sem þörf er á.</span><span class="sxs-lookup"><span data-stu-id="614c4-159">You can then convert to other currencies as you require.</span></span> <span data-ttu-id="614c4-160">Þegar búið er að framkvæma umreikninginn getur eiginleikinn sjálfkrafa notað snjallverðsléttun.</span><span class="sxs-lookup"><span data-stu-id="614c4-160">Furthermore, after the conversion is done, the feature can automatically apply smart rounding.</span></span>

## <a name="when-i-open-the-purchase-agreement-page-in-a-line-view-mode-i-cant-personalize-the-page-by-adding-the-price-unit-field-in-the-overview-of-the-line"></a><span data-ttu-id="614c4-161">Þegar ég opna síðu innkaupasamnings í línuskoðunarstillingu, þá get ég ekki sérstillt síðuna með því að bæta við reit verðeiningar í yfirliti línunnar.</span><span class="sxs-lookup"><span data-stu-id="614c4-161">When I open the Purchase agreement page in a line view mode, I can't personalize the page by adding the Price unit field in the overview of the line.</span></span>

<span data-ttu-id="614c4-162">Ekki er hægt að taka með suma samnýtta reiti í sérstillingum samningsrammans.</span><span class="sxs-lookup"><span data-stu-id="614c4-162">Some shared fields in the agreement framework can't be included in personalizations.</span></span> <span data-ttu-id="614c4-163">Þessi takmörkun kemur til vegna gagnalíkansins sem er innleitt.</span><span class="sxs-lookup"><span data-stu-id="614c4-163">This limitation occurs because of the data model that is implemented.</span></span> <span data-ttu-id="614c4-164">Þess vegna er ekki hægt að sérsníða reitinn **Verðeining**.</span><span class="sxs-lookup"><span data-stu-id="614c4-164">Therefore, you can't personalize the **Price unit** field.</span></span>

## <a name="the-maximum-limit-from-a-purchase-agreement-isnt-effective-on-a-purchase-requisition"></a><span data-ttu-id="614c4-165">Hámarkið í innkaupasamningi gildir ekki í innkaupabeiðni.</span><span class="sxs-lookup"><span data-stu-id="614c4-165">The maximum limit from a purchase agreement isn't effective on a purchase requisition.</span></span>

### <a name="issue-description"></a><span data-ttu-id="614c4-166">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="614c4-166">Issue description</span></span>

<span data-ttu-id="614c4-167">Þegar innkaupabeiðni er tengd við innkaupasamning er hámarkið samkvæmt innkaupasamningi ekki virkt í innkaupabeiðninni.</span><span class="sxs-lookup"><span data-stu-id="614c4-167">When a purchase requisition is linked to a purchase agreement, the maximum limit from the purchase agreement isn't effective on the purchase requisition.</span></span> <span data-ttu-id="614c4-168">Sjálfgefnar upplýsingar um verð eru slegnar inn á réttan hátt en hægt er að panta meira en hámarkið samkvæmt innkaupasamningi í innkaupabeiðninni.</span><span class="sxs-lookup"><span data-stu-id="614c4-168">The default price information is correctly entered, but more than the maximum limit from the purchase agreement can be ordered in the purchase requisition.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="614c4-169">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="614c4-169">Issue resolution</span></span>

<span data-ttu-id="614c4-170">Búist er við þessari hegðun.</span><span class="sxs-lookup"><span data-stu-id="614c4-170">This behavior is expected.</span></span> <span data-ttu-id="614c4-171">Vegna þess að beiðnir eru ekki alltaf samþykktar ætti magn eða upphæð ekki að vera geymt í innkaupasamningi.</span><span class="sxs-lookup"><span data-stu-id="614c4-171">Because requisitions aren't always approved, a quantity or amount should not be reserved on the purchase agreement.</span></span> <span data-ttu-id="614c4-172">Þess vegna er ekki hægt að uppfylla hámarkið í innkaupasamningnum.</span><span class="sxs-lookup"><span data-stu-id="614c4-172">Therefore, you won't meet the maximum limit from the purchase agreement.</span></span>

## <a name="trade-agreements-can-be-created-from-rejected-rfqs-therefore-the-system-doesnt-prevent-trade-agreement-journals-from-being-created-if-the-rfq-line-hasnt-been-accepted"></a><span data-ttu-id="614c4-173">Hægt er að stofna verðsamninga úr höfnuðum tilboðsbeiðnum.</span><span class="sxs-lookup"><span data-stu-id="614c4-173">Trade agreements can be created from rejected RFQs.</span></span> <span data-ttu-id="614c4-174">Þess vegna hindrar kerfið ekki að færslubækur verðsamninga séu stofnaðar ef lína tilboðsbeiðni hefur ekki verið samþykkt.</span><span class="sxs-lookup"><span data-stu-id="614c4-174">Therefore, the system doesn't prevent trade agreement journals from being created if the RFQ line hasn't been accepted.</span></span>

<span data-ttu-id="614c4-175">Hægt er að stofna verðsamninga fyrir öll svör fyrir beiðni um tilboð (tilboðsbeiðni), óháð því hvort þau voru samþykkt eða þeim hafnað.</span><span class="sxs-lookup"><span data-stu-id="614c4-175">You can create trade agreements for any replies for a request for quotation (RFQ), regardless of whether they were accepted or rejected.</span></span> <span data-ttu-id="614c4-176">Frekari upplýsingar er að finna í [Yfirlit yfir beiðni um tilboð (tilboðsbeiðni)](request-quotations.md).</span><span class="sxs-lookup"><span data-stu-id="614c4-176">For more information, see [Requests for quotation (RFQs) overview](request-quotations.md).</span></span>

