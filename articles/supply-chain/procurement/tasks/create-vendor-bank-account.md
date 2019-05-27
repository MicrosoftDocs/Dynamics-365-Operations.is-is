---
title: Stofna bankareikning lánardrottins
description: Þessi verklýsing sýnir hvernig á að stofna bankareikning fyrir lánardrottinn.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: deb3587667ac13b95617ec219995bfef931df00c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546134"
---
# <a name="create-a-vendor-bank-account"></a><span data-ttu-id="d098f-103">Stofna bankareikning lánardrottins</span><span class="sxs-lookup"><span data-stu-id="d098f-103">Create a vendor bank account</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d098f-104">Þessi verklýsing sýnir hvernig á að stofna bankareikning fyrir lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="d098f-104">This procedure shows you how to create a bank account for a vendor.</span></span> <span data-ttu-id="d098f-105">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="d098f-105">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="d098f-106">Farið í innkaup og aðföng > Lánardrottnar > Allir lánardrottnar.</span><span class="sxs-lookup"><span data-stu-id="d098f-106">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="d098f-107">Veljið lánardrottinn sem á að stofna bankareikning fyrir, og smellið síðan á tengil á kenni lánardrottnalykils</span><span class="sxs-lookup"><span data-stu-id="d098f-107">Select the vendor that you want to create a bank account for, and then click the link on the Vendor account ID.</span></span>
3. <span data-ttu-id="d098f-108">Í aðgerðasvæðinu er smellt á lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="d098f-108">On the Action Pane, click Vendor.</span></span>
4. <span data-ttu-id="d098f-109">Smellt er á bankareikninga.</span><span class="sxs-lookup"><span data-stu-id="d098f-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="d098f-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d098f-110">Click New.</span></span>
6. <span data-ttu-id="d098f-111">Í reitinn Bankareikningar skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="d098f-111">In the Bank account field, type a value.</span></span>
    * <span data-ttu-id="d098f-112">Þetta Kenni verður notuð til að auðkenna bankareikninginn á lánardrottinsfærslu.</span><span class="sxs-lookup"><span data-stu-id="d098f-112">This ID will be used to identify the bank account on the vendor record.</span></span>  
7. <span data-ttu-id="d098f-113">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="d098f-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="d098f-114">Færa inn eða veljið gildi í svæðinu bankaflokkur.</span><span class="sxs-lookup"><span data-stu-id="d098f-114">In the Bank groups field, enter or select a value.</span></span>
9. <span data-ttu-id="d098f-115">Veljið valkost í svæðinu gerð leiðarnúmers.</span><span class="sxs-lookup"><span data-stu-id="d098f-115">In the Routing number type field, select an option.</span></span>
    * <span data-ttu-id="d098f-116">Þetta er Gerð leiðarnúmers sem notað er fyrir alþjóðlegar greiðslur.</span><span class="sxs-lookup"><span data-stu-id="d098f-116">This is the type of routing number that’s used for international payments.</span></span>  
10. <span data-ttu-id="d098f-117">Í reitinn Bankareikningsnúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="d098f-117">In the Bank account number field, type a value.</span></span>
11. <span data-ttu-id="d098f-118">Í svæðinu SWIFT-kóði færðu inn gildi.</span><span class="sxs-lookup"><span data-stu-id="d098f-118">In the SWIFT code field, type a value.</span></span>
12. <span data-ttu-id="d098f-119">Í reitinn IBAN skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="d098f-119">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="d098f-120">Iban-númeri verður að vera á réttu sniði.</span><span class="sxs-lookup"><span data-stu-id="d098f-120">The IBAN number must be in the correct format.</span></span> <span data-ttu-id="d098f-121">Til dæmis er hægt að nota DE89370400440532013000.</span><span class="sxs-lookup"><span data-stu-id="d098f-121">For example, you could use DE89370400440532013000.</span></span>  
    * <span data-ttu-id="d098f-122">Staða bankareikningsins er Virkur ef Virkri dagsetningu hefur verið náð og lokadagur er ekki liðinn.</span><span class="sxs-lookup"><span data-stu-id="d098f-122">The status of the bank account is Active if the Active date has been reached, and the Expiration date has not been exceeded.</span></span> <span data-ttu-id="d098f-123">Einnig er hann virkur ef svæðin Virka dagsetningu og dagsetning Gildistíma eru auð.</span><span class="sxs-lookup"><span data-stu-id="d098f-123">It’s also active if both the Active date and Expiration date fields are blank.</span></span> <span data-ttu-id="d098f-124">Ef dagsetningarnar í svæðunum Virk dagsetning og Lokadagur eru báðar í framtíðinni er ekki hægt að gera rafrænar greiðslur.</span><span class="sxs-lookup"><span data-stu-id="d098f-124">If the dates in both the Active date and Expiration date fields are in the future electronic payments are not available.</span></span> <span data-ttu-id="d098f-125">Aðrar greiðslugerðir eru mögulegar og bankareikningurinn er virkur.</span><span class="sxs-lookup"><span data-stu-id="d098f-125">Other payment types are available and the bank account is active.</span></span>  
13. <span data-ttu-id="d098f-126">Víkka út hlutann Uppsetning.</span><span class="sxs-lookup"><span data-stu-id="d098f-126">Expand the Setup section.</span></span>
14. <span data-ttu-id="d098f-127">Í svæðinu Textakóði færðu inn gildi.</span><span class="sxs-lookup"><span data-stu-id="d098f-127">In the Text code field, type a value.</span></span>
    * <span data-ttu-id="d098f-128">Þetta svæði tilgreinir kóða sem mun birtast á bankayfirliti viðtakanda.</span><span class="sxs-lookup"><span data-stu-id="d098f-128">This field specifies a code that will appear on the bank statement of the recipient.</span></span>  
15. <span data-ttu-id="d098f-129">Í reitinn skilaboð til banka skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="d098f-129">In the Message to bank field, type a value.</span></span>
16. <span data-ttu-id="d098f-130">Færa inn gildi í tilvísunarsvæði gjaldeyrisviðskipta.</span><span class="sxs-lookup"><span data-stu-id="d098f-130">In the Exchange reference field, type a value.</span></span>
    * <span data-ttu-id="d098f-131">Þetta er Tilvísunarnúmer fyrir hvers kyns framvirkt eða fast gengi.</span><span class="sxs-lookup"><span data-stu-id="d098f-131">This is the reference number for any forward-term or fixed-term rate of exchange.</span></span>  
17. <span data-ttu-id="d098f-132">Í reitinn gjaldmiðill skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="d098f-132">In the Currency field, enter or select a value.</span></span>
    * <span data-ttu-id="d098f-133">Þegar fyrirframkvittanir eru gefin út, gefur þessa kafla yfirlit yfir stöðu þeirra (í bið eða samþykkt).</span><span class="sxs-lookup"><span data-stu-id="d098f-133">When prenotes are issued, this section provides an overview of their status (pending or approved).</span></span>  
18. <span data-ttu-id="d098f-134">Stækka aðsetur Hluti.</span><span class="sxs-lookup"><span data-stu-id="d098f-134">Expand the Address section.</span></span>
19. <span data-ttu-id="d098f-135">Víkkið út hlutann fyrirframkvittun.</span><span class="sxs-lookup"><span data-stu-id="d098f-135">Expand the Prenotes section.</span></span>
20. <span data-ttu-id="d098f-136">Útvíkka hlutann upplýsingar Tengiliðar.</span><span class="sxs-lookup"><span data-stu-id="d098f-136">Expand the Contact information section.</span></span>
21. <span data-ttu-id="d098f-137">Í reitinn Símanúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="d098f-137">In the Telephone field, type a value.</span></span>
22. <span data-ttu-id="d098f-138">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d098f-138">Close the page.</span></span>
23. <span data-ttu-id="d098f-139">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="d098f-139">Click Edit.</span></span>
24. <span data-ttu-id="d098f-140">Stækkið hlutann Greiðslur.</span><span class="sxs-lookup"><span data-stu-id="d098f-140">Expand the Payment section.</span></span>
25. <span data-ttu-id="d098f-141">Í svæðinu bankareikningur, veljið lykil sem hefur verið rétt nýlega stofnuð.</span><span class="sxs-lookup"><span data-stu-id="d098f-141">In the Bank  account field, select the account that you’ve just created.</span></span>
26. <span data-ttu-id="d098f-142">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="d098f-142">Click Save.</span></span>
    * <span data-ttu-id="d098f-143">Aðsetrið má erfa frá bankaflokki, ef slíkt er tilgreint, eða hægt er að bæta honum við hér.</span><span class="sxs-lookup"><span data-stu-id="d098f-143">The address may be inherited from the bank group, if one is specified, or you can add it here.</span></span>  

