--- 
title: "Stofna bankareikning lánardrottins"
description: "Þessi verklýsing sýnir hvernig á að stofna bankareikning fyrir lánardrottinn."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2bdd1264f92b73aed2eeb6ab13e435bb3c0dde19
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-vendor-bank-account"></a><span data-ttu-id="99034-103">Stofna bankareikning lánardrottins</span><span class="sxs-lookup"><span data-stu-id="99034-103">Create a vendor bank account</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="99034-104">Þessi verklýsing sýnir hvernig á að stofna bankareikning fyrir lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="99034-104">This procedure shows you how to create a bank account for a vendor.</span></span> <span data-ttu-id="99034-105">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="99034-105">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="99034-106">Farið í innkaup og aðföng > Lánardrottnar > Allir lánardrottnar.</span><span class="sxs-lookup"><span data-stu-id="99034-106">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="99034-107">Veljið lánardrottinn sem á að stofna bankareikning fyrir, og smellið síðan á tengil á kenni lánardrottnalykils</span><span class="sxs-lookup"><span data-stu-id="99034-107">Select the vendor that you want to create a bank account for, and then click the link on the Vendor account ID.</span></span>
3. <span data-ttu-id="99034-108">Í aðgerðasvæðinu er smellt á lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="99034-108">On the Action Pane, click Vendor.</span></span>
4. <span data-ttu-id="99034-109">Smellt er á bankareikninga.</span><span class="sxs-lookup"><span data-stu-id="99034-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="99034-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="99034-110">Click New.</span></span>
6. <span data-ttu-id="99034-111">Í reitinn Bankareikningar skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="99034-111">In the Bank account field, type a value.</span></span>
    * <span data-ttu-id="99034-112">Þetta Kenni verður notuð til að auðkenna bankareikninginn á lánardrottinsfærslu.</span><span class="sxs-lookup"><span data-stu-id="99034-112">This ID will be used to identify the bank account on the vendor record.</span></span>  
7. <span data-ttu-id="99034-113">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="99034-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="99034-114">Færa inn eða veljið gildi í svæðinu bankaflokkur.</span><span class="sxs-lookup"><span data-stu-id="99034-114">In the Bank groups field, enter or select a value.</span></span>
9. <span data-ttu-id="99034-115">Veljið valkost í svæðinu gerð leiðarnúmers.</span><span class="sxs-lookup"><span data-stu-id="99034-115">In the Routing number type field, select an option.</span></span>
    * <span data-ttu-id="99034-116">Þetta er Gerð leiðarnúmers sem notað er fyrir alþjóðlegar greiðslur.</span><span class="sxs-lookup"><span data-stu-id="99034-116">This is the type of routing number that’s used for international payments.</span></span>  
10. <span data-ttu-id="99034-117">Í reitinn Bankareikningsnúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="99034-117">In the Bank account number field, type a value.</span></span>
11. <span data-ttu-id="99034-118">Í svæðinu SWIFT-kóði færðu inn gildi.</span><span class="sxs-lookup"><span data-stu-id="99034-118">In the SWIFT code field, type a value.</span></span>
12. <span data-ttu-id="99034-119">Í reitinn IBAN skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="99034-119">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="99034-120">Iban-númeri verður að vera á réttu sniði.</span><span class="sxs-lookup"><span data-stu-id="99034-120">The IBAN number must be in the correct format.</span></span> <span data-ttu-id="99034-121">Til dæmis er hægt að nota DE89370400440532013000.</span><span class="sxs-lookup"><span data-stu-id="99034-121">For example, you could use DE89370400440532013000.</span></span>  
    * <span data-ttu-id="99034-122">Staða bankareikningsins er Virkur ef Virkri dagsetningu hefur verið náð og lokadagur er ekki liðinn.</span><span class="sxs-lookup"><span data-stu-id="99034-122">The status of the bank account is Active if the Active date has been reached, and the Expiration date has not been exceeded.</span></span> <span data-ttu-id="99034-123">Einnig er hann virkur ef svæðin Virka dagsetningu og dagsetning Gildistíma eru auð.</span><span class="sxs-lookup"><span data-stu-id="99034-123">It’s also active if both the Active date and Expiration date fields are blank.</span></span> <span data-ttu-id="99034-124">Ef dagsetningarnar í svæðunum Virk dagsetning og Lokadagur eru báðar í framtíðinni er ekki hægt að gera rafrænar greiðslur.</span><span class="sxs-lookup"><span data-stu-id="99034-124">If the dates in both the Active date and Expiration date fields are in the future electronic payments are not available.</span></span> <span data-ttu-id="99034-125">Aðrar greiðslugerðir eru mögulegar og bankareikningurinn er virkur.</span><span class="sxs-lookup"><span data-stu-id="99034-125">Other payment types are available and the bank account is active.</span></span>  
13. <span data-ttu-id="99034-126">Víkka út hlutann Uppsetning.</span><span class="sxs-lookup"><span data-stu-id="99034-126">Expand the Setup section.</span></span>
14. <span data-ttu-id="99034-127">Í svæðinu Textakóði færðu inn gildi.</span><span class="sxs-lookup"><span data-stu-id="99034-127">In the Text code field, type a value.</span></span>
    * <span data-ttu-id="99034-128">Þetta svæði tilgreinir kóða sem mun birtast á bankayfirliti viðtakanda.</span><span class="sxs-lookup"><span data-stu-id="99034-128">This field specifies a code that will appear on the bank statement of the recipient.</span></span>  
15. <span data-ttu-id="99034-129">Í reitinn skilaboð til banka skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="99034-129">In the Message to bank field, type a value.</span></span>
16. <span data-ttu-id="99034-130">Færa inn gildi í tilvísunarsvæði gjaldeyrisviðskipta.</span><span class="sxs-lookup"><span data-stu-id="99034-130">In the Exchange reference field, type a value.</span></span>
    * <span data-ttu-id="99034-131">Þetta er Tilvísunarnúmer fyrir hvers kyns framvirkt eða fast gengi.</span><span class="sxs-lookup"><span data-stu-id="99034-131">This is the reference number for any forward-term or fixed-term rate of exchange.</span></span>  
17. <span data-ttu-id="99034-132">Í reitinn gjaldmiðill skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="99034-132">In the Currency field, enter or select a value.</span></span>
    * <span data-ttu-id="99034-133">Þegar fyrirframkvittanir eru gefin út, gefur þessa kafla yfirlit yfir stöðu þeirra (í bið eða samþykkt).</span><span class="sxs-lookup"><span data-stu-id="99034-133">When prenotes are issued, this section provides an overview of their status (pending or approved).</span></span>  
18. <span data-ttu-id="99034-134">Stækka aðsetur Hluti.</span><span class="sxs-lookup"><span data-stu-id="99034-134">Expand the Address section.</span></span>
19. <span data-ttu-id="99034-135">Víkkið út hlutann fyrirframkvittun.</span><span class="sxs-lookup"><span data-stu-id="99034-135">Expand the Prenotes section.</span></span>
20. <span data-ttu-id="99034-136">Útvíkka hlutann upplýsingar Tengiliðar.</span><span class="sxs-lookup"><span data-stu-id="99034-136">Expand the Contact information section.</span></span>
21. <span data-ttu-id="99034-137">Í reitinn Símanúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="99034-137">In the Telephone field, type a value.</span></span>
22. <span data-ttu-id="99034-138">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="99034-138">Close the page.</span></span>
23. <span data-ttu-id="99034-139">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="99034-139">Click Edit.</span></span>
24. <span data-ttu-id="99034-140">Stækkið hlutann Greiðslur.</span><span class="sxs-lookup"><span data-stu-id="99034-140">Expand the Payment section.</span></span>
25. <span data-ttu-id="99034-141">Í svæðinu bankareikningur, veljið lykil sem hefur verið rétt nýlega stofnuð.</span><span class="sxs-lookup"><span data-stu-id="99034-141">In the Bank  account field, select the account that you’ve just created.</span></span>
26. <span data-ttu-id="99034-142">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="99034-142">Click Save.</span></span>
    * <span data-ttu-id="99034-143">Aðsetrið má erfa frá bankaflokki, ef slíkt er tilgreint, eða hægt er að bæta honum við hér.</span><span class="sxs-lookup"><span data-stu-id="99034-143">The address may be inherited from the bank group, if one is specified, or you can add it here.</span></span>  


