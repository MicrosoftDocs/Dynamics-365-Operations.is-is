---
title: Færa inn sölusamninga
description: Þessi verklýsing sýnir hvernig stofna á sölusamningi sem bindur sig einum viðskiptavini til að kaupa vöru fyrir samþykkt upphæð yfir tímanum in skiptum fyrir sérstakan afslátt.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 025c9fe2f769f37b63bd79c6c3afedc31a955310
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "346871"
---
# <a name="enter-sales-agreements"></a><span data-ttu-id="d1140-103">Færa inn sölusamninga</span><span class="sxs-lookup"><span data-stu-id="d1140-103">Enter sales agreements</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d1140-104">Þessi verklýsing sýnir hvernig stofna á sölusamningi sem bindur sig einum viðskiptavini til að kaupa vöru fyrir samþykkt upphæð yfir tímanum in skiptum fyrir sérstakan afslátt.</span><span class="sxs-lookup"><span data-stu-id="d1140-104">This procedure shows you how to create a sales agreement that commits one of your customers to buy a product for an agreed amount over time in exchange for special discounts.</span></span> <span data-ttu-id="d1140-105">Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum.</span><span class="sxs-lookup"><span data-stu-id="d1140-105">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-sales-agreement-header"></a><span data-ttu-id="d1140-106">Setja upp Haus sölusamnings</span><span class="sxs-lookup"><span data-stu-id="d1140-106">Set up sales agreement header</span></span>
1. <span data-ttu-id="d1140-107">Fara í Sölu og markaðssetningu > Sölusamningar > Sölusamninga.</span><span class="sxs-lookup"><span data-stu-id="d1140-107">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="d1140-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d1140-108">Click New.</span></span>
3. <span data-ttu-id="d1140-109">Í reitnum Reikningur viðskiptavina skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="d1140-109">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="d1140-110">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="d1140-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d1140-111">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="d1140-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="d1140-112">Í reitnum sölusamningur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="d1140-112">In the Sales agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="d1140-113">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="d1140-113">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="d1140-114">Útvíkka eða draga saman hlutann Almennt.</span><span class="sxs-lookup"><span data-stu-id="d1140-114">Expand the General section.</span></span>
9. <span data-ttu-id="d1140-115">Veljið ‚skuldbinding um gildi afurðar' í svæði Sjálfgefin ráðstöfun.</span><span class="sxs-lookup"><span data-stu-id="d1140-115">In the Default commitment field, select 'Product value commitment'.</span></span>
    * <span data-ttu-id="d1140-116">Ráðstöfunargerð er áskilið skilyrði sem þarf að tengja við samninginn til að skilgreina hvernig verður að uppfylla samnings.</span><span class="sxs-lookup"><span data-stu-id="d1140-116">A commitment type is a mandatory criterion that you must assign to the agreement to define how the agreement contract will be fulfilled.</span></span> <span data-ttu-id="d1140-117">Fjögur áður skilgreindar gerðir gera þér kleift að setja upp markmið viðskiptavinarins um ráðstöfun, sýnt sem magn eða gildi.</span><span class="sxs-lookup"><span data-stu-id="d1140-117">The four predefined types let you set up the customer's commitment target, expressed as a quantity or a value.</span></span> <span data-ttu-id="d1140-118">Aðeins má nota magn ráðstöfunargerðar á tiltekinni vöru, en gerðir byggt á gildi á við um sölu á bæði tilteknar og ótilteknar vörur.</span><span class="sxs-lookup"><span data-stu-id="d1140-118">The quantity commitment type can only be applied to a specific product, but the value-based types are applicable to sales of both specific and non-specific products.</span></span>  
10. <span data-ttu-id="d1140-119">Í svæði lokadags, Stillið dagsetninguna í framtíðar dagsetningu þegar samningnum á að renna út</span><span class="sxs-lookup"><span data-stu-id="d1140-119">In the Expiration date field, set the date to a future date when you want the agreement to expire.</span></span>
11. <span data-ttu-id="d1140-120">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="d1140-120">Click OK.</span></span>

## <a name="set-up-product-value-commitment-lines"></a><span data-ttu-id="d1140-121">Setja upp afurðargildi skuldbindingarlína</span><span class="sxs-lookup"><span data-stu-id="d1140-121">Set up product value commitment lines</span></span>
1. <span data-ttu-id="d1140-122">Smellið á „Bæta við línu“.</span><span class="sxs-lookup"><span data-stu-id="d1140-122">Click Add line.</span></span>
2. <span data-ttu-id="d1140-123">Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="d1140-123">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="d1140-124">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="d1140-124">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="d1140-125">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="d1140-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d1140-126">Gerð ráðstöfunar sem valin er fyrir samninginn hefur áhrif á þær upplýsingar sem þú getur fært inn fyrir samningslínur.</span><span class="sxs-lookup"><span data-stu-id="d1140-126">The type of commitment that you have chosen for the agreement affects the kind of information you can enter for the agreement lines.</span></span> <span data-ttu-id="d1140-127">Til dæmis, fyrir samning sem byggist á virði verður að tilgreina samtals nettóupphæð (í gjaldmiðli sem samið var um) sem viðskiptavinur bindur sig að kaupa vörur fyrir.</span><span class="sxs-lookup"><span data-stu-id="d1140-127">For example, for a value-based agreement you must specify the total net amount (in the agreed currency) for which the customer commits to buys goods from you.</span></span> <span data-ttu-id="d1140-128">Í þessu dæmi Magni og Einingarupplýsingum svæðunum í línunni er ótiltæk þar sem verið er að stofna samning fyrir viðskiptavin sem á að kaupa sérstakt gildi vöru.</span><span class="sxs-lookup"><span data-stu-id="d1140-128">In this example the Quantity and Unit fields on the line are unavailable because you’re creating an agreement for the customer to buy a specific value of a product.</span></span>   
5. <span data-ttu-id="d1140-129">Í svæðinu nettóupphæð slá inn peningaupphæð sem viðskiptavinurinn hefur ákveðið að kaupa.</span><span class="sxs-lookup"><span data-stu-id="d1140-129">In the Net amount field, enter the monetary amount that the customer has committed to buying.</span></span>
6. <span data-ttu-id="d1140-130">Í Afsláttarprósent svæðinu, færið inn gildi prósentu sem á við viðskiptavinarins sölupöntunarlínur sem tengjast þessum samning.</span><span class="sxs-lookup"><span data-stu-id="d1140-130">In the Discount percent field, enter a percentage value that will apply to the customer's sales order lines that are linked to this agreement.</span></span>
7. <span data-ttu-id="d1140-131">Víkkið út hlutann „Upplýsingar um línu“.</span><span class="sxs-lookup"><span data-stu-id="d1140-131">Expand the Line details section.</span></span>
8. <span data-ttu-id="d1140-132">Velja skal Já í Hámark er tryggt svæði.</span><span class="sxs-lookup"><span data-stu-id="d1140-132">Select Yes in the Max is enforced field.</span></span>
    * <span data-ttu-id="d1140-133">Val á Hámark er tryggt þýðir heildarupphæð allra sölupöntunarlínanna sem nota á sérstakt verð skuldbindingar, afslættir og/eða greiðsluskilmála má ekki fara yfir upphæðinni sem er tilgreind á skuldbinding.</span><span class="sxs-lookup"><span data-stu-id="d1140-133">Selecting Max is enforced means that the total amount of all the sales order lines that use the commitment's special prices, discounts and/or payment terms must not exceed the amount specified on the commitment.</span></span>  
    * <span data-ttu-id="d1140-134">Lágmarks- og hámarks losunarupphæðir tilgreina svið gilda sem verður selt á hverja sölupöntun sem notar valinn samning.</span><span class="sxs-lookup"><span data-stu-id="d1140-134">The minimum and maximum release amounts specify a range of values that must be sold on each sales order that uses the selected agreement.</span></span>   
9. <span data-ttu-id="d1140-135">Útvíkka hlutann haus sölusamnings.</span><span class="sxs-lookup"><span data-stu-id="d1140-135">Expand the Sales agreement header section.</span></span>
    * <span data-ttu-id="d1140-136">Nema staða samningurinn er stillt á Virk, geta sölupantanir ekki verið tengd við samning og þar af leiðandi ekki stuðlað að uppfyllingu fyrir þann samning.</span><span class="sxs-lookup"><span data-stu-id="d1140-136">Unless the status of the agreement is set to Effective, sales orders cannot be associated with the agreement and can therefore not contribute to the fulfilment of that agreement.</span></span> <span data-ttu-id="d1140-137">Hægt er að breyta stöðunni handvirkt á þessu stigi.</span><span class="sxs-lookup"><span data-stu-id="d1140-137">You can change the status manually at this stage.</span></span> <span data-ttu-id="d1140-138">Þó væri myndi yfirleitt breyta stöðu þegar samnings fyrir viðskiptavin er staðfest.</span><span class="sxs-lookup"><span data-stu-id="d1140-138">However, the status would normally be changed when you confirm the agreement for the customer.</span></span>  
10. <span data-ttu-id="d1140-139">Á Aðgerðasvæðinu skal smellt á sölusamningur.</span><span class="sxs-lookup"><span data-stu-id="d1140-139">On the Action Pane, click Sales agreement.</span></span>
11. <span data-ttu-id="d1140-140">Smellt er á Staðfestingu.</span><span class="sxs-lookup"><span data-stu-id="d1140-140">Click Confirmation.</span></span>
    * <span data-ttu-id="d1140-141">Gangið úr skugga um að Merkja samning sem virkan valkost er stillt á Já.</span><span class="sxs-lookup"><span data-stu-id="d1140-141">Make sure that the Mark agreement as effective option is set to Yes.</span></span>  
12. <span data-ttu-id="d1140-142">Velja skal Já í svæðinu Prenta skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="d1140-142">Select Yes in the Print report field.</span></span>
13. <span data-ttu-id="d1140-143">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="d1140-143">Click OK.</span></span>
14. <span data-ttu-id="d1140-144">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d1140-144">Close the page.</span></span>
    * <span data-ttu-id="d1140-145">Samningurinn er nú virkt og hægt er að hefja tengingu pantanir viðskiptavinarins við samning, sem mótfærðar á móti skuldbindingarmarkinu.</span><span class="sxs-lookup"><span data-stu-id="d1140-145">The agreement is now effective and you can start linking the customer's orders to the agreement, to offset against the committed target.</span></span>  

