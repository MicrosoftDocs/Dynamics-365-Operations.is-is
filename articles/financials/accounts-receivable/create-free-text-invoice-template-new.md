---
title: Stofna sniðmát fyrir reikning með frjálsum texta
description: Þessi aðferð sýnir hvernig á að búa til sniðmát fyrir reikningur með frjálsum texta.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 91f2ec2f8ab21616c6a1b886ee89d6faf84023e4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559504"
---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="7661b-103">Stofna sniðmát fyrir reikning með frjálsum texta</span><span class="sxs-lookup"><span data-stu-id="7661b-103">Create a free text invoice template</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7661b-104">Í þessari sýnikennslu skal nota USMF sýnifyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="7661b-104">For this walkthrough, use the USMF demo company.</span></span> <span data-ttu-id="7661b-105">Þetta ferli er ætluð fyrir notandann sem ber ábyrgð á stjórnun og vinnslu reikninga viðskiptakrafna.</span><span class="sxs-lookup"><span data-stu-id="7661b-105">This procedure is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="7661b-106">Búa til sniðmát</span><span class="sxs-lookup"><span data-stu-id="7661b-106">Create a template</span></span>

1. <span data-ttu-id="7661b-107">Fara í Viðskiptakröfur > Reikningar > Endurteknir reikningar > Sniðmát textareiknings.</span><span class="sxs-lookup"><span data-stu-id="7661b-107">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="7661b-108">Notið þessa skjámynd til að stofna sniðmát sem getur innihaldið línur á reikningi, gjöld, sniðmát fyrir dreifingu á fjárhagsupphæð og upplýsingar um fjárhagslykil.</span><span class="sxs-lookup"><span data-stu-id="7661b-108">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="7661b-109">Smellt er á 'Nýtt' til að búa til nýja sniðmát reiknings með frjáls texti.</span><span class="sxs-lookup"><span data-stu-id="7661b-109">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="7661b-110">Í reitinn Heiti sniðmáts skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7661b-110">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="7661b-111">'Sniðmátsheiti' auðkennir á einkvæman hátt sniðmát reikningur með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="7661b-111">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="7661b-112">Engin tvö sniðmát til að geta haft sama 'sniðmátsheiti'.</span><span class="sxs-lookup"><span data-stu-id="7661b-112">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="7661b-113">Færið inn lýsingu á sniðmát í svæðinu Lýsing..</span><span class="sxs-lookup"><span data-stu-id="7661b-113">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="7661b-114">Útvíkka flipanum reikningslína.</span><span class="sxs-lookup"><span data-stu-id="7661b-114">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="7661b-115">Færið inn lýsingu á reikningslína í svæðinu Lýsing..</span><span class="sxs-lookup"><span data-stu-id="7661b-115">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="7661b-116">Í aðallykill svæðinu, veljið reikning fyrir tekjur.</span><span class="sxs-lookup"><span data-stu-id="7661b-116">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="7661b-117">Þú getur valið mótfærslulykil fyrir lánsfé viðskiptavinar fyrir heildarupphæð reiknings í síðunni bókunarregla Viðskiptavinar .</span><span class="sxs-lookup"><span data-stu-id="7661b-117">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="7661b-118">Í reitnum VSK-flokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="7661b-118">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="7661b-119">VSK-flokkur fyrir núgildandi reikningslínu er sjálfgefinn VSK-flokkur fyrir viðskiptavinalykill.</span><span class="sxs-lookup"><span data-stu-id="7661b-119">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="7661b-120">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="7661b-120">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="7661b-121">Í svæði skattflokkur vöru, velja vsk-flokk vöru fyrir gildandi reikningslínu.</span><span class="sxs-lookup"><span data-stu-id="7661b-121">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="7661b-122">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="7661b-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="7661b-123">Í svæðinu einingarverð, færa inn eða skoða verð á einingu fyrir reikningslínu</span><span class="sxs-lookup"><span data-stu-id="7661b-123">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="7661b-124">Magnið er margfaldað með magnsvæði til að ákvarða endanlegan upphæð línu.</span><span class="sxs-lookup"><span data-stu-id="7661b-124">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="7661b-125">Bæta við nýrri línu við sniðmát reikningur með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="7661b-125">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="7661b-126">Færið inn lýsingu á reikningslína í svæðinu Lýsing..</span><span class="sxs-lookup"><span data-stu-id="7661b-126">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="7661b-127">Í aðallykill svæðinu, veljið reikning fyrir tekjur.</span><span class="sxs-lookup"><span data-stu-id="7661b-127">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="7661b-128">Þú getur valið mótfærslulykil fyrir lánsfé viðskiptavinar fyrir heildarupphæð reiknings í síðunni bókunarregla Viðskiptavinar .</span><span class="sxs-lookup"><span data-stu-id="7661b-128">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="7661b-129">Í reitnum VSK-flokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="7661b-129">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="7661b-130">VSK-flokkur fyrir núgildandi reikningslínu er sjálfgefinn VSK-flokkur fyrir viðskiptavinalykill.</span><span class="sxs-lookup"><span data-stu-id="7661b-130">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="7661b-131">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="7661b-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="7661b-132">Í reitnum VSK-flokkur vöru skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="7661b-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="7661b-133">VSK-flokkur vöru fyrir núgildandi reikningslínuna.</span><span class="sxs-lookup"><span data-stu-id="7661b-133">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="7661b-134">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="7661b-134">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="7661b-135">Færa inn eða skoða fjöldi eininga fyrir reikningslínu</span><span class="sxs-lookup"><span data-stu-id="7661b-135">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="7661b-136">Númerið er margfaldað með svæði einingaverðs til að ákvarða endanlegan upphæð reikningslínu.</span><span class="sxs-lookup"><span data-stu-id="7661b-136">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="7661b-137">Færa inn eða skoða verð á einingu fyrir reikningslínu.</span><span class="sxs-lookup"><span data-stu-id="7661b-137">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="7661b-138">Magnið er margfaldað með gildinu á magnsvæði til að ákvarða endanlegan upphæð línu.</span><span class="sxs-lookup"><span data-stu-id="7661b-138">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="7661b-139">Skoða og breyta dreifingar á fjárhagsupphæð fyrir staka línu og allar línur undirstigs.</span><span class="sxs-lookup"><span data-stu-id="7661b-139">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="7661b-140">Dreifingar á fjárhagsupphæð eru notaðar til að skilgreina hvernig gert verður grein fyrir upphæð, eins og hvernig tekjur, skatta eða gjöld verður að teknir með á reikningi með frjáls texti</span><span class="sxs-lookup"><span data-stu-id="7661b-140">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="7661b-141">Uppfæra dreifing á fjárhagsupphæð fyrir Valið reikningslína.</span><span class="sxs-lookup"><span data-stu-id="7661b-141">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="7661b-142">Smellið á „Loka“.</span><span class="sxs-lookup"><span data-stu-id="7661b-142">Click Close.</span></span>

## <a name="save-a-free-text-invoice-as-a-template"></a><span data-ttu-id="7661b-143">Vistaðu reikningur með frjálsum texta sem sniðmát</span><span class="sxs-lookup"><span data-stu-id="7661b-143">Save a free text invoice as a template</span></span>
<span data-ttu-id="7661b-144">Þú getur líka vistað fyrirliggjandi reikningur með frjálsum texta sem sniðmát.</span><span class="sxs-lookup"><span data-stu-id="7661b-144">You can also save an existing free text invoice as a template.</span></span> <span data-ttu-id="7661b-145">Þegar þú velur Vista í sniðmát á flipanum Reikningur, gefðu upp nafn og lýsingu fyrir sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="7661b-145">When you select Save to template from the Invoice tab, provide a name and a description for the template.</span></span> <span data-ttu-id="7661b-146">Ef sniðmát með nafninu er þegar til, munt þú sjá tilkynningu um að sniðmát með því nafni sé þegar til.</span><span class="sxs-lookup"><span data-stu-id="7661b-146">If a template with the name already exists, you will see a notification that a template with that name already exists.</span></span> <span data-ttu-id="7661b-147">Þú getur ennþá smellt á Í lagi til að skipta því út.</span><span class="sxs-lookup"><span data-stu-id="7661b-147">You can still click on Ok to replace it.</span></span> 
