---
title: Setja upp og vinna með endurtekna reikninga
description: Í þessari grein er því lýst hvernig endurtekinn reikningur er sett upp og unnið. Þú getur notað endurtekinn reikningur ef þú þarft að senda viðskiptavinur reikning fyrir sama upphæð reglulega.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: roschlom
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76dd6b21207b61dfb96e4d9538b5e6ffc1c6b02d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835125"
---
# <a name="set-up-and-process-recurring-invoices"></a><span data-ttu-id="3f4f9-104">Setja upp og vinna með endurtekna reikninga</span><span class="sxs-lookup"><span data-stu-id="3f4f9-104">Set up and process recurring invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3f4f9-105">Í þessari grein er því lýst hvernig endurtekinn reikningur er sett upp og unnið.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-105">This article explains how to set up and process recurring invoices.</span></span> <span data-ttu-id="3f4f9-106">Þú getur notað endurtekinn reikningur ef þú þarft að senda viðskiptavinur reikning fyrir sama upphæð reglulega.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-106">You can use recurring invoices if you must invoice customers for the same amount on a regular basis.</span></span>

<a name="create-a-recurring-free-text-invoice-template"></a><span data-ttu-id="3f4f9-107">Stofna sniðmát fyrir endurtekna textareikninga</span><span class="sxs-lookup"><span data-stu-id="3f4f9-107">Create a recurring free text invoice template</span></span>
---------------------------------------------

<span data-ttu-id="3f4f9-108">Til að reikningsfæra viðskiptavini fyrir sömu þjónustu reglulega, verður að skilgreina sniðmát textareiknings sem hægt er að endurnýta til að stofna reikninga.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-108">To invoice customers for the same services on a regular basis, you must define a free text invoice template that can be reused to create the invoices.</span></span> <span data-ttu-id="3f4f9-109">Sniðmátið inniheldur eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="3f4f9-109">This template contains the following information:</span></span>

-   <span data-ttu-id="3f4f9-110">Hausupplýsingar, eins og skattaflokk, greiðsluskilmála og greiðsluhátt</span><span class="sxs-lookup"><span data-stu-id="3f4f9-110">Header information, such as tax groups, terms of payment, and the method of payment</span></span>
-   <span data-ttu-id="3f4f9-111">Línuupplýsingar, eins og í þjónustulýsingu, tekjulykla, einingarverð og reikningsupphæð</span><span class="sxs-lookup"><span data-stu-id="3f4f9-111">Line information, such as the service description, revenue accounts, unit price, and invoice amount</span></span>
-   <span data-ttu-id="3f4f9-112">Gjöld fyrir sendingu eða meðhöndlun</span><span class="sxs-lookup"><span data-stu-id="3f4f9-112">Charges for shipping or handling</span></span>
-   <span data-ttu-id="3f4f9-113">Dreifingar fjárhagsupphæða með fjárhagsvíddaupplýsingum, eins og kostnaðarstöðum og viðskiptaeiningum</span><span class="sxs-lookup"><span data-stu-id="3f4f9-113">Accounting distributions together with financial dimension information, such as cost centers and business units</span></span>

<span data-ttu-id="3f4f9-114">Í rauninni er verið að stofna heilan reikning og vista hann sem sniðmát.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-114">In effect, you're creating an entire invoice and saving it as a template.</span></span> <span data-ttu-id="3f4f9-115">Hægt er að setja upp sniðmát sem nota síðuna **Endurteknir reikningar**.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-115">You can set up the templates using the **Recurring invoices** page.</span></span>

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a><span data-ttu-id="3f4f9-116">Úthluta viðskiptavini sniðmáti textareiknings og færa inn upplýsingar um endurtekningu</span><span class="sxs-lookup"><span data-stu-id="3f4f9-116">Assign a free text invoice template to a customer and enter recurrence details</span></span>
<span data-ttu-id="3f4f9-117">Eftir að sniðmát er stofnað, verður að úthluta sniðmáti til viðskiptavina sem óskað er að reikningsfæra.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-117">After the template is created, you must assign the template to the customers that you want to invoice.</span></span> <span data-ttu-id="3f4f9-118">Að auki þarf að tilgreina hvenær og hversu oft reikningurinn verður notaður.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-118">Additionally, you must specify when and how often the invoice will be used.</span></span> <span data-ttu-id="3f4f9-119">Sniðmátum er hægt að úthluta á flipanum **Reikningur** á síðunni **Viðskiptavinir**.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-119">You can assign the templates on the **Invoice** tab of the **Customers** page.</span></span> <span data-ttu-id="3f4f9-120">Bættu sniðmátinu á listanum og uppfærðu eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="3f4f9-120">Add the template to the list, and update the following information:</span></span>

-   <span data-ttu-id="3f4f9-121">Upphafsdagsetningin og hugsanlega lokadagsetningin fyrir endurtekinn reikning</span><span class="sxs-lookup"><span data-stu-id="3f4f9-121">The start date and, optionally, the end date for the recurring billing</span></span>
-   <span data-ttu-id="3f4f9-122">Tíðni endurtekinnar reikningsreglu (t.d. daglega eða einu sinni í mánuði)</span><span class="sxs-lookup"><span data-stu-id="3f4f9-122">The frequency of the recurring billing (for example, every day or once a month)</span></span>
-   <span data-ttu-id="3f4f9-123">Hámarksupphæð innheimtu (ef þessara upplýsinga er krafist)</span><span class="sxs-lookup"><span data-stu-id="3f4f9-123">The maximum billing amount (if this information is required)</span></span>

<span data-ttu-id="3f4f9-124">Viðskiptavinur getur haft mörg sniðmát sem hafa mismunandi tíðnir.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-124">A customer can have multiple templates that have different frequencies.</span></span>

## <a name="generate-the-recurring-invoices"></a><span data-ttu-id="3f4f9-125">Búa til endurtekna reikninga</span><span class="sxs-lookup"><span data-stu-id="3f4f9-125">Generate the recurring invoices</span></span>
<span data-ttu-id="3f4f9-126">Á síðunni **Endurteknir reikningar** er verk sem vinnur úr endurteknum reikningum.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-126">On the **Recurring invoices** page, there is a task that processes recurring invoice templates.</span></span> <span data-ttu-id="3f4f9-127">Þú tilgreinir dagsetningu reiknings og sniðmát til að mynda reikninga úr.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-127">You specify the invoice date and the template to generate the invoices from.</span></span> <span data-ttu-id="3f4f9-128">Reikningar verða myndaðir og úthlutað á eitt kenni endurtekningar fyrir hvern flokk af reikningum sem eru unnir.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-128">Invoices will be generated and assigned a single recurrence ID number for each group of invoices that is processed.</span></span>

<a name="post-recurring-free-text-invoices"></a><span data-ttu-id="3f4f9-129">Bóka endurtekna textareikninga</span><span class="sxs-lookup"><span data-stu-id="3f4f9-129">Post recurring free text invoices</span></span>
---------------------------------

<span data-ttu-id="3f4f9-130">Eftir að endurteknir reikningar eru búnir til birtast kenni endurtekinna reikninga í bókunarverki á síðunni **Endurteknir reikningar**.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-130">After recurring invoices are generated, the invoice recurrence IDs appear in a posting task on the **Recurring invoices** page.</span></span> <span data-ttu-id="3f4f9-131">Hægt er að skoða alla reikninga fyrir kenni endurtekningar með því að smella á tengilinn.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-131">You can view all of the invoices for a recurrence ID by clicking the link.</span></span> <span data-ttu-id="3f4f9-132">Við endurskoðun reikninga fyrir kenni endurtekningar er hægt að eyða einstökum reikningum.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-132">During your review of the invoices for the recurrence ID, you can delete individual invoices.</span></span> <span data-ttu-id="3f4f9-133">Endurtekningarstillingar viðskiptavinar verða endurstilltar fyrir sniðmátið, þannig að hægt er að endurmynda það síðar.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-133">The customer's recurrence settings will be reset for that template, so that it can be regenerated later.</span></span> <span data-ttu-id="3f4f9-134">Hægt er að bóka einn, marga eða alla reikninga fyrir endurtekningu.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-134">You can post one, many, or all of the invoices for a recurrence ID.</span></span> <span data-ttu-id="3f4f9-135">Ef verkflæði eru virkjuð þarf að smella á **Senda** áður en hægt er að bóka reikninga.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-135">If workflows are enabled, you must click **Submit** before you can post the invoices.</span></span>

<a name="print-recurring-free-text-invoices"></a><span data-ttu-id="3f4f9-136">Prenta endurtekna textareikninga</span><span class="sxs-lookup"><span data-stu-id="3f4f9-136">Print recurring free text invoices</span></span>
----------------------------------

<span data-ttu-id="3f4f9-137">Eftir að endurteknir reikningar hafa verið bókaðir er hægt að prenta reikningana úr listasíðu textareikningsins.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-137">After recurring invoices are posted, you can print the invoices from the free text invoice list page.</span></span> <span data-ttu-id="3f4f9-138">Hægt er að prenta reikninga sem eru valdar, eða hægt er að velja bil reikninga sem á að prenta.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-138">You can print the invoices that are selected, or you can select a range of invoices to print.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]