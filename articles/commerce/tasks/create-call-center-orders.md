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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1675d21f1e4176839feace76359afdbdc336c99
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022909"
---
# <a name="create-call-center-orders"></a><span data-ttu-id="99cd2-103"> Stofna pantanir fyrir símaver</span><span class="sxs-lookup"><span data-stu-id="99cd2-103">Create call center orders</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="99cd2-104">Þetta ferli fer í gegnum hvernig er flett upp viðskiptavinur, ný pöntun er stofnuð, leita að afurð og innheimta greiðslu frá viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="99cd2-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="99cd2-105">Þessi aðferð notar sýnigögn fyrirtækis USRT og er ætlaður fyrir Afgreiðslumaður sölupöntunar.</span><span class="sxs-lookup"><span data-stu-id="99cd2-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="99cd2-106">Frumskilyrði: Notandinn sem klárar ferlið er settur upp sem notandi símavers og Fabrikam hálfsárs Vörulisti er birt með minnst einn frumkóða á honum.</span><span class="sxs-lookup"><span data-stu-id="99cd2-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="99cd2-107">Fara í Retail og Commerce > viðskiptavinur > viðskiptavinur þjónusta.</span><span class="sxs-lookup"><span data-stu-id="99cd2-107">Go to Retail and Commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="99cd2-108">Færa inn leitarskilyrði til að fletta upp viðskiptavinar í svæðinu SearchText.</span><span class="sxs-lookup"><span data-stu-id="99cd2-108">In the SearchText field, enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="99cd2-109">Fyrir þetta dæmi í ferlinu 'karen' og stutt er á flipann.</span><span class="sxs-lookup"><span data-stu-id="99cd2-109">For this example procedure type in 'karen' and press tab.</span></span>  
3. <span data-ttu-id="99cd2-110">Smellið á leita.</span><span class="sxs-lookup"><span data-stu-id="99cd2-110">Click Search.</span></span>
    * <span data-ttu-id="99cd2-111">Þar sem það er aðeins einn viðskiptavin með heitinu Karen í sýnigögn þær verða sjálfvirkt valinn.</span><span class="sxs-lookup"><span data-stu-id="99cd2-111">Since there is only one customer named Karen in demo data they will be automatically selected.</span></span>  
4. <span data-ttu-id="99cd2-112">Smelltu á Ný sölupöntun</span><span class="sxs-lookup"><span data-stu-id="99cd2-112">Click New sales order.</span></span>
5. <span data-ttu-id="99cd2-113">Útvíkka eða draga saman hlutann sölupöntunarhaus.</span><span class="sxs-lookup"><span data-stu-id="99cd2-113">Expand or collapse the Sales order header section.</span></span>
6. <span data-ttu-id="99cd2-114">Veljið frumkóða fyrir vörulistann.</span><span class="sxs-lookup"><span data-stu-id="99cd2-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="99cd2-115">Ef engin virk frumkóðar eru hægt að loka á upprunareit og sleppa þessu þrepi.</span><span class="sxs-lookup"><span data-stu-id="99cd2-115">If there are no active Source codes you can close the Source field and skip this step.</span></span>  
7. <span data-ttu-id="99cd2-116">Smellið á „Bæta við línu“.</span><span class="sxs-lookup"><span data-stu-id="99cd2-116">Click Add line.</span></span>
8. <span data-ttu-id="99cd2-117">Færið inn leitarorð í svæðið númer vöru.</span><span class="sxs-lookup"><span data-stu-id="99cd2-117">In the Item number field, enter the item search term.</span></span>
    * <span data-ttu-id="99cd2-118">Fyrir Þetta sýnishorn ferlis að færa inn hluta vörunúmer '8111' og styðjið á flipanum. Þetta mun birtast glugganum leit að vöru.</span><span class="sxs-lookup"><span data-stu-id="99cd2-118">For this sample procedure enter a partial item number of '8111' and press tab. This will pop up the item search window.</span></span>  
9. <span data-ttu-id="99cd2-119">Velja afurðar til að bæta við sölupöntun</span><span class="sxs-lookup"><span data-stu-id="99cd2-119">Select the product to add to the sales order</span></span>
10. <span data-ttu-id="99cd2-120">Færið inn sölumagn</span><span class="sxs-lookup"><span data-stu-id="99cd2-120">Enter the sales quantity.</span></span>
11. <span data-ttu-id="99cd2-121">Smellið á Stofna.</span><span class="sxs-lookup"><span data-stu-id="99cd2-121">Click Create.</span></span>
12. <span data-ttu-id="99cd2-122">Smellið á Ljúka til að fanga greiðslu viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="99cd2-122">Click Complete to capture the customer payment.</span></span>
13. <span data-ttu-id="99cd2-123">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="99cd2-123">Click Add.</span></span>
    * <span data-ttu-id="99cd2-124">Bæta Við tengli er í flipanum Greiðslur. Útvíkka flipanum Greiðslur ef hún er dregin saman.</span><span class="sxs-lookup"><span data-stu-id="99cd2-124">The Add link is in the Payments tab. Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="99cd2-125">Veldu greiðslumáti</span><span class="sxs-lookup"><span data-stu-id="99cd2-125">Select the payment method.</span></span>
    * <span data-ttu-id="99cd2-126">Veljið greiðslumáta reiðufjár fyrir þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="99cd2-126">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="99cd2-127">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="99cd2-127">Close the page.</span></span>
16. <span data-ttu-id="99cd2-128">Færa skal inn upphæðina.</span><span class="sxs-lookup"><span data-stu-id="99cd2-128">Enter the amount.</span></span>
    * <span data-ttu-id="99cd2-129">Fyrir Þetta ferli skal færa upphæð jafnt og stöðu pöntunar sem hægt er að sjá í samantekt sölupöntunar síðunni vinstra megin við svæðið upphæð.</span><span class="sxs-lookup"><span data-stu-id="99cd2-129">For this procedure enter an amount equal to the order balance which can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="99cd2-130">Þetta leyfir notandanum að ljúka sem að fullu greitt.</span><span class="sxs-lookup"><span data-stu-id="99cd2-130">This will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="99cd2-131">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="99cd2-131">Click OK.</span></span>
18. <span data-ttu-id="99cd2-132">Smelltu á Senda.</span><span class="sxs-lookup"><span data-stu-id="99cd2-132">Click Submit.</span></span>
