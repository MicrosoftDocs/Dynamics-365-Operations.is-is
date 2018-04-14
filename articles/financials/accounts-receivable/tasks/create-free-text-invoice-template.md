--- 
title: "Stofna sniðmát fyrir reikning með frjálsum texta"
description: "Þessi skráning notar sýnigögn USMF fyrirtækis"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/11/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d785922d1c6775d95ad5697eb6a872434e59c8e4
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="47573-103">Stofna sniðmát fyrir reikning með frjálsum texta</span><span class="sxs-lookup"><span data-stu-id="47573-103">Create a free text invoice template</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="47573-104">Þessi skráning notar sýnigögn USMF fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="47573-104">This recording uses the USMF demo company.</span></span> <span data-ttu-id="47573-105">Skráningin er ætluð fyrir notandann sem er ábyrgur fyrir stjórnun og vinnslu viðskiptakröfureikninga.</span><span class="sxs-lookup"><span data-stu-id="47573-105">The recording is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="47573-106">Fara í Viðskiptakröfur > Reikningar > Endurteknir reikningar > Sniðmát textareiknings.</span><span class="sxs-lookup"><span data-stu-id="47573-106">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="47573-107">Notið þessa skjámynd til að stofna sniðmát sem getur innihaldið línur á reikningi, gjöld, sniðmát fyrir dreifingu á fjárhagsupphæð og upplýsingar um fjárhagslykil.</span><span class="sxs-lookup"><span data-stu-id="47573-107">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="47573-108">Smellt er á 'Nýtt' til að búa til nýja sniðmát reiknings með frjáls texti.</span><span class="sxs-lookup"><span data-stu-id="47573-108">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="47573-109">Í reitinn Heiti sniðmáts skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="47573-109">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="47573-110">'Sniðmátsheiti' auðkennir á einkvæman hátt sniðmát reikningur með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="47573-110">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="47573-111">Engin tvö sniðmát til að geta haft sama 'sniðmátsheiti'.</span><span class="sxs-lookup"><span data-stu-id="47573-111">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="47573-112">Færið inn lýsingu á sniðmát í svæðinu Lýsing..</span><span class="sxs-lookup"><span data-stu-id="47573-112">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="47573-113">Útvíkka flipanum reikningslína.</span><span class="sxs-lookup"><span data-stu-id="47573-113">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="47573-114">Færið inn lýsingu á reikningslína í svæðinu Lýsing..</span><span class="sxs-lookup"><span data-stu-id="47573-114">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="47573-115">Í aðallykill svæðinu, veljið reikning fyrir tekjur.</span><span class="sxs-lookup"><span data-stu-id="47573-115">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="47573-116">Þú getur valið mótfærslulykil fyrir lánsfé viðskiptavinar fyrir heildarupphæð reiknings í síðunni bókunarregla Viðskiptavinar .</span><span class="sxs-lookup"><span data-stu-id="47573-116">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="47573-117">Í reitnum VSK-flokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="47573-117">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="47573-118">VSK-flokkur fyrir núgildandi reikningslínu er sjálfgefinn VSK-flokkur fyrir viðskiptavinalykill.</span><span class="sxs-lookup"><span data-stu-id="47573-118">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="47573-119">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="47573-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="47573-120">Í svæði skattflokkur vöru, velja vsk-flokk vöru fyrir gildandi reikningslínu.</span><span class="sxs-lookup"><span data-stu-id="47573-120">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="47573-121">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="47573-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="47573-122">Í svæðinu einingarverð, færa inn eða skoða verð á einingu fyrir reikningslínu</span><span class="sxs-lookup"><span data-stu-id="47573-122">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="47573-123">Magnið er margfaldað með magnsvæði til að ákvarða endanlegan upphæð línu.</span><span class="sxs-lookup"><span data-stu-id="47573-123">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="47573-124">Bæta við nýrri línu við sniðmát reikningur með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="47573-124">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="47573-125">Færið inn lýsingu á reikningslína í svæðinu Lýsing..</span><span class="sxs-lookup"><span data-stu-id="47573-125">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="47573-126">Í aðallykill svæðinu, veljið reikning fyrir tekjur.</span><span class="sxs-lookup"><span data-stu-id="47573-126">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="47573-127">Þú getur valið mótfærslulykil fyrir lánsfé viðskiptavinar fyrir heildarupphæð reiknings í síðunni bókunarregla Viðskiptavinar .</span><span class="sxs-lookup"><span data-stu-id="47573-127">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="47573-128">Í reitnum VSK-flokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="47573-128">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="47573-129">VSK-flokkur fyrir núgildandi reikningslínu er sjálfgefinn VSK-flokkur fyrir viðskiptavinalykill.</span><span class="sxs-lookup"><span data-stu-id="47573-129">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="47573-130">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="47573-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="47573-131">Í reitnum VSK-flokkur vöru skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="47573-131">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="47573-132">VSK-flokkur vöru fyrir núgildandi reikningslínuna.</span><span class="sxs-lookup"><span data-stu-id="47573-132">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="47573-133">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="47573-133">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="47573-134">Færa inn eða skoða fjöldi eininga fyrir reikningslínu</span><span class="sxs-lookup"><span data-stu-id="47573-134">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="47573-135">Númerið er margfaldað með svæði einingaverðs til að ákvarða endanlegan upphæð reikningslínu.</span><span class="sxs-lookup"><span data-stu-id="47573-135">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="47573-136">Færa inn eða skoða verð á einingu fyrir reikningslínu.</span><span class="sxs-lookup"><span data-stu-id="47573-136">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="47573-137">Magnið er margfaldað með gildinu á magnsvæði til að ákvarða endanlegan upphæð línu.</span><span class="sxs-lookup"><span data-stu-id="47573-137">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="47573-138">Skoða og breyta dreifingar á fjárhagsupphæð fyrir staka línu og allar línur undirstigs.</span><span class="sxs-lookup"><span data-stu-id="47573-138">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="47573-139">Dreifingar á fjárhagsupphæð eru notaðar til að skilgreina hvernig gert verður grein fyrir upphæð, eins og hvernig tekjur, skatta eða gjöld verður að teknir með á reikningi með frjáls texti</span><span class="sxs-lookup"><span data-stu-id="47573-139">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="47573-140">Uppfæra dreifing á fjárhagsupphæð fyrir Valið reikningslína.</span><span class="sxs-lookup"><span data-stu-id="47573-140">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="47573-141">Smellið á „Loka“.</span><span class="sxs-lookup"><span data-stu-id="47573-141">Click Close.</span></span>


