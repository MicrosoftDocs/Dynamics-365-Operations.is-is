---
title: " Stofna pantanir fyrir símaver"
description: Þetta ferli fer í gegnum hvernig er flett upp viðskiptavinur, ný pöntun er stofnuð, leita að afurð og innheimta greiðslu frá viðskiptavini.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ecf6fe97287fcfb3c070215b563542878175789c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264285"
---
# <a name="create-call-center-orders"></a><span data-ttu-id="bc235-103"> Stofna pantanir fyrir símaver</span><span class="sxs-lookup"><span data-stu-id="bc235-103">Create call center orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc235-104">Þetta ferli fer í gegnum hvernig er flett upp viðskiptavinur, ný pöntun er stofnuð, leita að afurð og innheimta greiðslu frá viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="bc235-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="bc235-105">Þessi aðferð notar sýnigögn fyrirtækis USRT og er ætlaður fyrir Afgreiðslumaður sölupöntunar.</span><span class="sxs-lookup"><span data-stu-id="bc235-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="bc235-106">Frumskilyrði: Notandinn sem klárar ferlið er settur upp sem notandi símavers og Fabrikam hálfsárs Vörulisti er birt með minnst einn frumkóða á honum.</span><span class="sxs-lookup"><span data-stu-id="bc235-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="bc235-107">Fárið í **Smásala og viðskipti \> Viðskiptavinir \> Þjónusta við viðskiptavini**.</span><span class="sxs-lookup"><span data-stu-id="bc235-107">Go to **Retail and Commerce \> Customers \> Customer service**.</span></span>
2. <span data-ttu-id="bc235-108">Færa inn leitarskilyrði til að fletta upp viðskiptavinar í svæðinu **SearchText.**</span><span class="sxs-lookup"><span data-stu-id="bc235-108">For **SearchText**, enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="bc235-109">Til að fá þetta dæmi skal slá inn „Karen“ og velja **Tab**.</span><span class="sxs-lookup"><span data-stu-id="bc235-109">For this example procedure, enter "Karen" and select **Tab**.</span></span>  
3. <span data-ttu-id="bc235-110">Velja Leita.</span><span class="sxs-lookup"><span data-stu-id="bc235-110">Select Search.</span></span>
    * <span data-ttu-id="bc235-111">Þar sem það er aðeins einn viðskiptavinur með heitinu Karen í sýnigögn verður hann sjálfvirkt valinn.</span><span class="sxs-lookup"><span data-stu-id="bc235-111">Since there is only one customer named "Karen" in demo data, the result will be automatically selected.</span></span>  
4. <span data-ttu-id="bc235-112">Veldu **Ný sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="bc235-112">Select **New sales order**.</span></span>
5. <span data-ttu-id="bc235-113">Útvíkka eða draga saman haushlutann **sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="bc235-113">Expand or collapse the **Sales order** header section.</span></span>
6. <span data-ttu-id="bc235-114">Veljið frumkóða fyrir vörulistann.</span><span class="sxs-lookup"><span data-stu-id="bc235-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="bc235-115">Ef engin virkir frumkóðar eru til staðar er hægt að sleppa þessu þrepi.</span><span class="sxs-lookup"><span data-stu-id="bc235-115">If there are no active source codes you can skip this step.</span></span>  
7. <span data-ttu-id="bc235-116">Veldu **Bæta við línu**.</span><span class="sxs-lookup"><span data-stu-id="bc235-116">Select **Add line**.</span></span>
8. <span data-ttu-id="bc235-117">Færið inn leitarorð í svæðið **Númer vöru**.</span><span class="sxs-lookup"><span data-stu-id="bc235-117">For **Item number**, enter the item search term.</span></span>
    * <span data-ttu-id="bc235-118">Fyrir Þetta sýnishorn ferlis að færa inn hluta vörunúmer '8111' og styðjið á flipanum. Þá birtist leitarglugginn.</span><span class="sxs-lookup"><span data-stu-id="bc235-118">For this sample procedure, enter a partial item number of '8111' and press tab. This action will bring up the item search window.</span></span>  
9. <span data-ttu-id="bc235-119">Velja afurðar til að bæta við sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="bc235-119">Select the product to add to the sales order.</span></span>
10. <span data-ttu-id="bc235-120">Færið inn sölumagn</span><span class="sxs-lookup"><span data-stu-id="bc235-120">Enter the sales quantity.</span></span>
11. <span data-ttu-id="bc235-121">Velja **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="bc235-121">Select **Create**.</span></span>
12. <span data-ttu-id="bc235-122">Veljið **Ljúka** til að fanga greiðslu viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="bc235-122">Select **Complete** to capture the customer payment.</span></span>
13. <span data-ttu-id="bc235-123">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="bc235-123">Select **Add**.</span></span>
    * <span data-ttu-id="bc235-124">Bæta Við tengli er í flipanum Greiðslur. Útvíkka flipanum Greiðslur ef hún er dregin saman.</span><span class="sxs-lookup"><span data-stu-id="bc235-124">The Add link is in the Payments tab. Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="bc235-125">Veldu greiðslumáti</span><span class="sxs-lookup"><span data-stu-id="bc235-125">Select the payment method.</span></span>
    * <span data-ttu-id="bc235-126">Veljið greiðslumáta reiðufjár fyrir þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="bc235-126">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="bc235-127">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="bc235-127">Close the page.</span></span>
16. <span data-ttu-id="bc235-128">Færa skal inn upphæðina.</span><span class="sxs-lookup"><span data-stu-id="bc235-128">Enter the amount.</span></span>
    * <span data-ttu-id="bc235-129">Fyrir þetta ferli skal færa upphæð jafnt og stöðu pöntunar sem hægt er að sjá í samantekt sölupöntunar síðunni vinstra megin við svæðið upphæð.</span><span class="sxs-lookup"><span data-stu-id="bc235-129">For this procedure, enter an amount equal to the order balance that can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="bc235-130">Þessi aðgerð leyfir notandanum að ljúka pöntun sem að fullu greitt.</span><span class="sxs-lookup"><span data-stu-id="bc235-130">This action will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="bc235-131">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="bc235-131">Select **OK**.</span></span>
18. <span data-ttu-id="bc235-132">Veldu **Senda**.</span><span class="sxs-lookup"><span data-stu-id="bc235-132">Select **Submit**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bc235-133">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="bc235-133">Additional resources</span></span>

[<span data-ttu-id="bc235-134">Sérstilla tölvupósta vegna færslna eftir afhendingarmáta</span><span class="sxs-lookup"><span data-stu-id="bc235-134">Customize transactional emails by mode of delivery</span></span>](../customize-email-delivery-mode.md)

[<span data-ttu-id="bc235-135">Breyta afhendingarmáta á sölustað</span><span class="sxs-lookup"><span data-stu-id="bc235-135">Change mode of delivery in POS</span></span>](../pos-change-delivery-mode.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]