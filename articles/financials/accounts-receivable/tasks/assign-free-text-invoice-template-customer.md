--- 
title: "Úthluta sniðmáti reiknings með frjálsum texta á viðskiptavin"
description: "Þetta verk sýnir hvernig á að tengja við sniðmát reiknings með frjáls texti við viðskiptavinar."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3bcb59c6edd04877dc2a052002be513205ae840a
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="assign-a-free-text-invoice-template-to-a-customer"></a><span data-ttu-id="d034f-103">Úthluta sniðmáti reiknings með frjálsum texta á viðskiptavin</span><span class="sxs-lookup"><span data-stu-id="d034f-103">Assign a free text invoice template to a customer</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d034f-104">Þetta verk sýnir hvernig á að tengja við sniðmát reiknings með frjáls texti við viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="d034f-104">This task demonstrates how to assign a free text invoice template to a customer.</span></span> <span data-ttu-id="d034f-105">Þetta verk notar USMF sýnigögn fyrirtækið og er ætlaður fyrir notandann sem er ábyrgur fyrir stjórnun og vinnslu viðskiptakröfureikninga.</span><span class="sxs-lookup"><span data-stu-id="d034f-105">This task uses the USMF demo company and is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="d034f-106">Farið í Viðskiptakröfur > Viðskiptavinir > Allir viðskiptavinir.</span><span class="sxs-lookup"><span data-stu-id="d034f-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="d034f-107">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="d034f-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d034f-108">Smellið á „Reikningur“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="d034f-108">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="d034f-109">Smellt er á Endurteknir reikningar</span><span class="sxs-lookup"><span data-stu-id="d034f-109">Click Recurring invoices.</span></span>
    * <span data-ttu-id="d034f-110">Notið þessa síðu til að úthluta sniðmát reikningur með frjálsum texta til viðskiptavina og tilgreina hve oft reikningar verða send til viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="d034f-110">Use this page to assign free text invoice templates to customers and specify how frequently invoices will be sent to the customer.</span></span>  
5. <span data-ttu-id="d034f-111">Smella á Nýtt til að úthluta nýja sniðmát til viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="d034f-111">Click New to assign a new template to the customer.</span></span>
6. <span data-ttu-id="d034f-112">Velja skal sniðmát reikningur með frjálsum texta sem á að úthluta viðskiptavininum.</span><span class="sxs-lookup"><span data-stu-id="d034f-112">Select the free text invoice template you want to assign to the customer.</span></span>
7. <span data-ttu-id="d034f-113">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="d034f-113">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="d034f-114">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="d034f-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="d034f-115">Færa inn dagsetningu þegar fyrsti reikningurinn verður myndaður.</span><span class="sxs-lookup"><span data-stu-id="d034f-115">Enter the date when the first invoice will be generated.</span></span>
    * <span data-ttu-id="d034f-116">Færa inn endurtekna lokadag.</span><span class="sxs-lookup"><span data-stu-id="d034f-116">Enter a recurring end date.</span></span>  
    * <span data-ttu-id="d034f-117">Veljið eina af eftirfarandi: Engin lokadagsetning – Reikningar verða myndaðir óráðinn tíma þar til sniðmátið er fjarlægð úr viðskiptavinalykli.</span><span class="sxs-lookup"><span data-stu-id="d034f-117">Select one of the following: No end date – Invoices will be generated indefinitely until the template is removed from the customer account.</span></span>  <span data-ttu-id="d034f-118">Lokadagur Víxils – Velja þennan valkostur og færðu inn lokadagsetning sem stofna má reikningur.</span><span class="sxs-lookup"><span data-stu-id="d034f-118">Billing end date – Select this option and enter the last date that the invoice can be generated.</span></span>  
    * <span data-ttu-id="d034f-119">Hámarksheildarupphæð sem myndun reikninga stöðvast eftir.</span><span class="sxs-lookup"><span data-stu-id="d034f-119">Maximum cumulative amount after which invoice generation will stop.</span></span>  
    * <span data-ttu-id="d034f-120">Færa inn hámarksheildarupphæð sem hægt er að ná með völdu sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="d034f-120">Enter the maximum cumulative amount that can be reached using the selected template.</span></span> <span data-ttu-id="d034f-121">Til dæmis, ef fært er inn 1000,00 og mynda mánaðarlegar reikninga fyrir 100,00 hverja reikninga mun stöðva myndun sína eftir að tíunda reikningurinn er myndaður.</span><span class="sxs-lookup"><span data-stu-id="d034f-121">For example, if you enter 1,000.00 and generate monthly invoices for 100.00 each, invoices will stop generating after the tenth invoice is generated.</span></span>  
    * <span data-ttu-id="d034f-122">Mynda endurtekna reikninga með því að nota sjálfgefin gildi úr sniðmát textareiknings eða reikning viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="d034f-122">Generate recurring invoices by using the default values from either free text invoice template or the customer account.</span></span>  
    * <span data-ttu-id="d034f-123">Velja hvort eigi að nota sniðmát textareiknings eða reikning viðskiptavinar til að ákvarða sjálfgefin gildi fyrir tungumál, bókun forstillingu, vsk-flokk, vsk-flokkur vöru, listakóði, land/svæði fyrir afhendingu, gjaldmiðill, greiðsluskilmála, greiðslumáta, greiðsluskilgreiningar, greiðsluáætlun, staðgreiðsluafsláttur, fjárhagsvíddir og gíróseðils þegar reikningar eru stofnaðir.</span><span class="sxs-lookup"><span data-stu-id="d034f-123">Select whether to use the free text invoice template or the customer account to determine the default values for the language, posting profile, sales tax group, item sales tax group, list code, country/region for delivery, currency, terms of payment, method of payment, payment specification, payment schedule, cash discount, financial dimensions, and giro money transfer slip when invoices are created.</span></span>  
10. <span data-ttu-id="d034f-124">Veljið endurtekningarmynstri.</span><span class="sxs-lookup"><span data-stu-id="d034f-124">Select the recurrence pattern.</span></span>
    * <span data-ttu-id="d034f-125">Daglega – veldu þennan valkost og færðu inn fjölda daga í reitnum Eftir</span><span class="sxs-lookup"><span data-stu-id="d034f-125">Daily – Select this option and enter the number of days in the Per field.</span></span> <span data-ttu-id="d034f-126">Til dæmis, ef fært er inn 15 er reikningurinn verður myndaður 15 daga fresti fyrir þennan viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="d034f-126">For example, if you enter 15, an invoice will be generated every 15 days for this customer.</span></span>  <span data-ttu-id="d034f-127">Vikulega– veldu þennan valkost og færðu inn fjölda vikna í reitnum Eftir</span><span class="sxs-lookup"><span data-stu-id="d034f-127">Weekly - Select this option and enter the number of weeks in the Per field.</span></span> <span data-ttu-id="d034f-128">Til dæmis, ef fært er inn 2 er reikningurinn verður myndaður á tveggja vikna fresti fyrir þennan viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="d034f-128">For example, if you enter 2, an invoice will be generated every two weeks for this customer.</span></span>  <span data-ttu-id="d034f-129">Mánaðarlega – veldu þennan valkost og færðu inn fjölda mánaða í reitnum Eftir</span><span class="sxs-lookup"><span data-stu-id="d034f-129">Monthly - Select this option and enter the number of months in the Per field.</span></span> <span data-ttu-id="d034f-130">Til dæmis, ef fært er inn 6 er reikningurinn verður myndaður á sex mánaða fresti fyrir þennan viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="d034f-130">For example, if you enter 6, an invoice will be generated every six months for this customer.</span></span>  <span data-ttu-id="d034f-131">Árlega – veldu þennan valkost og færðu inn fjölda ára í reitnum Eftir</span><span class="sxs-lookup"><span data-stu-id="d034f-131">Yearly – Select this option and enter the number of years in the Per field.</span></span> <span data-ttu-id="d034f-132">Til dæmis, ef fært er inn 2 er reikningurinn verður myndaður á tveggja ára fresti fyrir þennan viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="d034f-132">For example, if you enter 2, an invoice will be generated every two years for this customer.</span></span>  
11. <span data-ttu-id="d034f-133">Í reitinn Á, skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="d034f-133">In the Per field, enter a number.</span></span>


