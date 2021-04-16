---
title: Staðgreiðsluafslættir
description: Staðgreiðsluafslættir eru uppsettir og samnýttir fyrir viðskiptakröfur og Viðskiptaskuldir.  Tiltækur staðgreiðsluafsláttur er hægt að tilgreina á reikning viðskiptavinar eða á reikning lánardrottins og verður tekinn ef reikningurinn er greiddur innan dagsetningu staðgreiðsluafsláttar.
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CashDisc
audience: Application User
ms.reviewer: roschlom
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06a9effdbe2aed6175273332654755b0ebc46659
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830475"
---
# <a name="cash-discounts"></a><span data-ttu-id="35d41-104">Staðgreiðsluafslættir</span><span class="sxs-lookup"><span data-stu-id="35d41-104">Cash discounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="35d41-105">Staðgreiðsluafslættir eru uppsettir og samnýttir fyrir viðskiptakröfur og Viðskiptaskuldir.</span><span class="sxs-lookup"><span data-stu-id="35d41-105">Cash discounts are setup and shared for Accounts payable and Accounts receivable.</span></span>  <span data-ttu-id="35d41-106">Tiltækur staðgreiðsluafsláttur er hægt að tilgreina á reikning viðskiptavinar eða á reikning lánardrottins og verður tekinn ef reikningurinn er greiddur innan dagsetningu staðgreiðsluafsláttar.</span><span class="sxs-lookup"><span data-stu-id="35d41-106">The cash discount available can be defined on the customer invoice or vendor invoice, and will be taken if the invoice is paid within the cash discount date.</span></span> 

## <a name="cash-discounts"></a><span data-ttu-id="35d41-107">Staðgreiðsluafslættir</span><span class="sxs-lookup"><span data-stu-id="35d41-107">Cash discounts</span></span>

<span data-ttu-id="35d41-108">Hægt er að stofna staðgreiðsluafslátt fyrir bæði viðskiptavini eða lánardrottna á síðunni staðgreiðsluafslætti.</span><span class="sxs-lookup"><span data-stu-id="35d41-108">Cash discounts for both customers or vendors can be created in the Cash discounts page.</span></span> <span data-ttu-id="35d41-109">Hægt er að skilgreina einnig , með því að nota Næsta afsláttarkóðasvæði , röð af staðgreiðsluafsláttum sem koma í kjölfar hver annars sem þegar fyrri staðgreiðsluafsláttardagsetningar renna út.</span><span class="sxs-lookup"><span data-stu-id="35d41-109">You can also define, by using the Next discount code field, a series of cash discounts that succeed each other as previous cash discount dates expire.</span></span> <span data-ttu-id="35d41-110">Nánari upplýsingar eru í "Dæmi: Röð af staðgreiðsluafslættum" síðar í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="35d41-110">For more information, see “Example: Series of cash discounts” later in this topic.</span></span> <span data-ttu-id="35d41-111">Ef reikningur, kreditfærsla (annað hvort í greiðslu eða kreditnótu) eða bæði eru færð inn í öðrum gjaldmiðli en bókhaldsgjaldmiðli lögaðilans er staðgreiðsluafsláttur reiknaður með því að nota gengi byggt á dagsetningu greiðslu eða kreditnótu.</span><span class="sxs-lookup"><span data-stu-id="35d41-111">If the invoice, credit transaction (either a payment or a credit note), or both are entered in a currency other than the accounting currency of the legal entity, the cash discount is calculated using the exchange rate based on the date of the payment or credit note.</span></span> <span data-ttu-id="35d41-112">Ef reiknings- og kreditskjalið eru færðar inn í mismunandi lögaðila og ef gjaldmiðlar bókhalds fyrir lögaðila er mismunandi, er gengið tekið úr lögaðili reikningsins, frá og með dagsetningu kreditskjals .</span><span class="sxs-lookup"><span data-stu-id="35d41-112">If the invoice and credit document are entered in different legal entities, and if the accounting currencies for the legal entities differ, the exchange rate is taken from the legal entity of the invoice, as of the date of the credit document.</span></span> <span data-ttu-id="35d41-113">Nánari upplýsingar eru í "Dæmi: gengi fyrir staðgreiðsluafslættum" síðar í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="35d41-113">For more information, see “Example: Exchange rates for cash discounts” later in this topic.</span></span>

## <a name="defaulting-order-of-cash-discount-main-account"></a><span data-ttu-id="35d41-114">Sjálfgefin röðun staðgreiðsluafsláttar fyrir aðallykil</span><span class="sxs-lookup"><span data-stu-id="35d41-114">Defaulting order of cash discount main account</span></span>

<span data-ttu-id="35d41-115">Ef reikningur er jafnaður með fyrirvara svo veittur sé staðgreiðsluafsláttur, þá er afslátturinn bókaður sjálfkrafa í aðallykil staðgreiðsluafsláttar, samkvæmt eftirfarandi sjálfgefinni forgangsröðun :</span><span class="sxs-lookup"><span data-stu-id="35d41-115">If an invoice is settled in time to obtain a cash discount, the cash discount is automatically posted to a cash discount main account according to the following defaulting priority:</span></span>
1.  <span data-ttu-id="35d41-116">Aðallykillinn sem tilgreindur er í svæðinu Annar staðgreiðsluafsláttur á síðu Jafna opnar færslur fyrir viðskiptavini eða á síðu Jafna opnar færslur fyrir lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="35d41-116">The main account specified in the Alternative cash discount account field on the customer Settle open transactions page or the vendor Settle open transactions page.</span></span>
2.  <span data-ttu-id="35d41-117">Aðallykillinn sem er tilgreindur á svæðinu staðgreiðsluafsláttur viðskiptavinar eða svæði staðgreiðsluafsláttur lánardrottins fyrir fjárhagsbókunarflokksins sem er úthlutað fyrir VSK-kóða reikningsins.</span><span class="sxs-lookup"><span data-stu-id="35d41-117">The main account specified in the Customer cash discount field or the Vendor cash discount field of the ledger posting group that is assigned to the sales tax code of the invoice.</span></span> <span data-ttu-id="35d41-118">Setja upp fjárhagsbókunarflokka á síðunni fyrir fjárhagsbókunarflokks og úthluta þeim á vsk-kóða á síðunni vsk-kóða.</span><span class="sxs-lookup"><span data-stu-id="35d41-118">Set up ledger posting groups on the Ledger posting groups page and assign them to sales tax codes in the Sales tax codes page.</span></span>
3.  <span data-ttu-id="35d41-119">Aðal bókunarlykillinn á síðu staðgreiðsluafsláttar í annað hvort svæði aðallykils fyrir afslætti viðskiptavinar eða svæðinu aðallykils fyrir afslætti lánardrottins fyrir kóða staðgreiðsluafsláttar sem er á jafnaða reikningnum.</span><span class="sxs-lookup"><span data-stu-id="35d41-119">The main posting account on the Cash discounts page in either the Main account for customer discounts field or the Main account for vendor discounts field for the cash discount code that is on the settled invoice.</span></span>
4.  <span data-ttu-id="35d41-120">Aðallykill fyrir staðgreiðsluafslátt, eins og skilgreint er í lyklar fyrir sjálfvirkar færslur síðu.</span><span class="sxs-lookup"><span data-stu-id="35d41-120">The main account for cash discounts, as defined in the Accounts for automatic transactions page.</span></span>

## <a name="example-series-of-cash-discounts"></a><span data-ttu-id="35d41-121">Dæmi: Röð af staðgreiðsluafslætti</span><span class="sxs-lookup"><span data-stu-id="35d41-121">Example: Series of cash discounts</span></span>
<span data-ttu-id="35d41-122">Setjið upp þrjá staðgreiðsluafsláttarkóða eins og hér segir:</span><span class="sxs-lookup"><span data-stu-id="35d41-122">Set up three cash discount codes as follows:</span></span>
-   <span data-ttu-id="35d41-123">Kóði 5D10% - 10% staðgreiðsluafsláttur þegar upphæðin er greidd innan 5 daga.</span><span class="sxs-lookup"><span data-stu-id="35d41-123">Code 5D10% – A cash discount of 10% when the amount is paid within 5 days.</span></span>
-   <span data-ttu-id="35d41-124">Kóði 10D5% - 5% staðgreiðsluafsláttur þegar upphæðin er greidd innan 10 daga.</span><span class="sxs-lookup"><span data-stu-id="35d41-124">Code 10D5% – A cash discount of 5% when the amount is paid within 10 days.</span></span>
-   <span data-ttu-id="35d41-125">Kóði 14D2% - 2% staðgreiðsluafsláttur þegar upphæðin er greidd innan 14 daga.</span><span class="sxs-lookup"><span data-stu-id="35d41-125">Code 14D2% – A cash discount of 2% when the amount is paid within 14 days.</span></span>

<span data-ttu-id="35d41-126">Í næsta afsláttarkóðasvæði:</span><span class="sxs-lookup"><span data-stu-id="35d41-126">In the Next discount code field:</span></span>
-   <span data-ttu-id="35d41-127">Fyrir kóðann 5D10% veljið 10D5%.</span><span class="sxs-lookup"><span data-stu-id="35d41-127">For the 5D10% code, select 10D5%.</span></span>
-   <span data-ttu-id="35d41-128">Fyrir kóðann 10D5% veljið 14D2%.</span><span class="sxs-lookup"><span data-stu-id="35d41-128">For the 10D5% code, select 14D2%.</span></span>
-   <span data-ttu-id="35d41-129">Fyrir kóðann 14D2% er reiturinn Næsti afsláttarkóði hafður auður.</span><span class="sxs-lookup"><span data-stu-id="35d41-129">For the 14D2% code, leave the Next discount code field blank.</span></span>

<span data-ttu-id="35d41-130">Í staðgreiðsluafsláttarnir þrír taka við hver af öðrum þegar dagsetning greiðslu líður fram yfir fyrri dagsetningu staðgreiðsluafsláttar á reikningnum.</span><span class="sxs-lookup"><span data-stu-id="35d41-130">The three cash discounts succeed each other as the payment date exceeds the previous cash discount date on the invoice.</span></span> <span data-ttu-id="35d41-131">Einungis einn staðgreiðsluafsláttur er veittur þegar reikningurinn er greiddur, samkvæmt dagsetningu staðgreiðsluafsláttar sem er eftir í röðinni af staðgreiðsluafslætti.</span><span class="sxs-lookup"><span data-stu-id="35d41-131">Only one cash discount is granted when the invoice is paid, based on which cash discount date is meet in the sequence of cash discounts.</span></span>

## <a name="example-exchange-rates-for-cash-discounts"></a><span data-ttu-id="35d41-132">Dæmi: gengi fyrir staðgreiðsluafslátt</span><span class="sxs-lookup"><span data-stu-id="35d41-132">Example: Exchange rates for cash discounts</span></span>
<span data-ttu-id="35d41-133">Bókhaldsgjaldmiðill fyrir við lögaðilann er EUR og eftirfarandi gengi eru tilgreindar fyrir USD:</span><span class="sxs-lookup"><span data-stu-id="35d41-133">Your legal entity’s accounting currency is EUR and the following exchange rates are specified for USD:</span></span>
-   <span data-ttu-id="35d41-134">Febrúar 1 = 110</span><span class="sxs-lookup"><span data-stu-id="35d41-134">February 1 = 110</span></span>
-   <span data-ttu-id="35d41-135">Mars 1 = 80</span><span class="sxs-lookup"><span data-stu-id="35d41-135">March 1 = 80</span></span>

<span data-ttu-id="35d41-136">Reikningur fyrir 1000 USD með skilmála staðgreiðsluafsláttar 20D2% er bókaður á 15. febrúar.</span><span class="sxs-lookup"><span data-stu-id="35d41-136">An invoice for 1000 USD with cash discount terms of 20D2% is posted on February 15.</span></span> <span data-ttu-id="35d41-137">Gjaldmiðilsupphæð reiknings er 1100 EUR.</span><span class="sxs-lookup"><span data-stu-id="35d41-137">The accounting currency amount of the invoice is 1100 EUR.</span></span> <span data-ttu-id="35d41-138">Greiðsla fyrir 980 USD er jöfnuð með reikningi 1. mars.</span><span class="sxs-lookup"><span data-stu-id="35d41-138">A payment for 980 USD is settled with the invoice on March 1.</span></span> <span data-ttu-id="35d41-139">Upphæð staðgreiðsluafsláttar er 20 USD.</span><span class="sxs-lookup"><span data-stu-id="35d41-139">The cash discount amount is 20 USD.</span></span> <span data-ttu-id="35d41-140">Upphæð bókhaldsgjaldmiðils fyrir greiðslu er 784 EUR.</span><span class="sxs-lookup"><span data-stu-id="35d41-140">The accounting currency amount of the payment is 784 EUR.</span></span> <span data-ttu-id="35d41-141">Gjaldmiðilsupphæð staðgreiðsluafsláttar er reiknuð með því að nota gengið frá 1. mars: 20 \* 80 / 100 = 16 EUR.</span><span class="sxs-lookup"><span data-stu-id="35d41-141">The accounting currency amount of the cash discount is calculated by using the exchange rate as of March 1: 20 \* 80 / 100 = 16 EUR.</span></span>

> [!NOTE]
> <span data-ttu-id="35d41-142">Ef Reikna staðgreiðsluafslætti fyrir hlutagreiðslur valkostur er valinn í færibreytum viðskiptakrafa eða færibreytur viðskiptaskulda síðunum, er notað gengi sem er í gildi á þeim degi sem hver hlutagreiðsla er notuð.</span><span class="sxs-lookup"><span data-stu-id="35d41-142">If the Calculate cash discounts for partial payments option is selected in the Accounts receivable parameters or Accounts payable parameters pages, the exchange rate that is in effect on the date of each partial payment is used.</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]