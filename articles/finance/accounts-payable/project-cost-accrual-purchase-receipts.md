---
title: Uppsöfnun á kostnaði verks á innkaupapöntunum
description: Þetta efnisatriði lýsir því hvernig hægt er að rekja uppsafnaðan verkkostnað úr innkaupapöntunum í Microsoft Dynamics 365 Finance.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: roschlom
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 615e22234323e2235fba002c50f9ab9c230c021e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827891"
---
# <a name="project-cost-accrual-on-purchase-receipts"></a><span data-ttu-id="bb33e-103">Uppsöfnun á kostnaði verks á innkaupapöntunum</span><span class="sxs-lookup"><span data-stu-id="bb33e-103">Project cost accrual on purchase receipts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb33e-104">Þetta efnisatriði lýsir því hvernig hægt er að rekja uppsafnaðan verkkostnað úr innkaupapöntunum í Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="bb33e-104">This topic describes how accrued project costs from purchase receipts can be tracked in Microsoft Dynamics 365 Finance.</span></span> 

<span data-ttu-id="bb33e-105">Reikningar fyrir verk berast oft síðar en vörur og þjónusta eru afhent, sem kann að hafa töluverð áhrif á afkastavísa verkefna (Afkastavísa).</span><span class="sxs-lookup"><span data-stu-id="bb33e-105">Invoices for a project often arrive later than the goods and services are delivered, which might have a significant impact on project key performance indicators (KPIs).</span></span> <span data-ttu-id="bb33e-106">Mikilvægt er að það sé hægt að rekja þessar færslur í bæði fjárhags- og verkefnaskýrslum.</span><span class="sxs-lookup"><span data-stu-id="bb33e-106">It important to be able to track these transactions in both financial and project reports.</span></span>

<span data-ttu-id="bb33e-107">Eftirfarandi dæmi lýsir þessum aðstæðum.</span><span class="sxs-lookup"><span data-stu-id="bb33e-107">The following example scenario illustrates this.</span></span> 

<span data-ttu-id="bb33e-108">Contoso Consulting hefur komið á fót nýjum skýjarekstri.</span><span class="sxs-lookup"><span data-stu-id="bb33e-108">Contoso Consulting has started a new cloud deployment project.</span></span> <span data-ttu-id="bb33e-109">Innkaupapöntun er stofnuð til að kaupa tölvu fyrir verkefnið.</span><span class="sxs-lookup"><span data-stu-id="bb33e-109">A purchase order is created to buy a computer for the project.</span></span> <span data-ttu-id="bb33e-110">Tölvan mun kosta $1500 og uppsetningarþjónusta mun kosta $150.</span><span class="sxs-lookup"><span data-stu-id="bb33e-110">The computer will cost $1500 and installation services will cost $150.</span></span> <span data-ttu-id="bb33e-111">Lánardrottinn hefur afhent og sett tölvuna upp, en reikningur hefur ekki enn borist Contoso Consulting.</span><span class="sxs-lookup"><span data-stu-id="bb33e-111">The vendor has delivered and installed the computer, but the invoice has not yet reached Contoso Consulting.</span></span> <span data-ttu-id="bb33e-112">Stjórnanda verksins langar að sjá kostnaðaruppsöfnun verkefnisins upp á $1650 áður en reikningurinn er afhentur.</span><span class="sxs-lookup"><span data-stu-id="bb33e-112">The project manager would like to see project cost accrual of $1650 before the invoice gets delivered.</span></span> <span data-ttu-id="bb33e-113">Þessi kostnaður ætti einnig að endurspeglast í fjárhagsskýrslum fyrirtækisins í mánuðarlok.</span><span class="sxs-lookup"><span data-stu-id="bb33e-113">This cost should also be reflected in the company's month end financial statements.</span></span> 

<span data-ttu-id="bb33e-114">Uppsafnaðan kostnað þarf að skrá bæði á fjárhagslegu stigi og verkstig fyrir skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="bb33e-114">The accrued cost needs to be recorded on both the financial level and project level for reporting purposes.</span></span> <span data-ttu-id="bb33e-115">Hægt er að rekja fjárhagslega uppfærslu afurðarinnar fyrir vöru- og innkaupaflokka.</span><span class="sxs-lookup"><span data-stu-id="bb33e-115">The financial update of the product receipt can be tracked for the item and procurement categories.</span></span> 

<span data-ttu-id="bb33e-116">Fyrir vörur, á síðunni **Færibreytur viðskiptaskulda**, veljið valkostinn **Bóka innhreyfingarskjöl afurða í fjárhag**.</span><span class="sxs-lookup"><span data-stu-id="bb33e-116">For items, on the **Accounts payable parameters** page, select the **Post product receipts to ledger** option.</span></span>
<span data-ttu-id="bb33e-117">[![Síðan Færibreytur viðskiptaskulda](./media/accruals1-1024x409.png)](./media/accruals1.png)</span><span class="sxs-lookup"><span data-stu-id="bb33e-117">[![Accounts payable parameters page](./media/accruals1-1024x409.png)](./media/accruals1.png)</span></span> 

<span data-ttu-id="bb33e-118">Fyrir innkaupategundir, á síðunni **Stefnuregla tegundar** skal velja reglurnar **Innkaup** og síðan **Safna upp innkaupakostnaði á kvittun** fyrir hvern innkaupaflokk.</span><span class="sxs-lookup"><span data-stu-id="bb33e-118">For procurement categories, on the **Category policy rule** page, select **Purchasing** policies, and then select **Accrue purchase expense on receipt** for each procurement category.</span></span>
<span data-ttu-id="bb33e-119">[![Síðan Stefnuregla tegunda](./media/accruals2-1024x569.png)](./media/accruals2.png)</span><span class="sxs-lookup"><span data-stu-id="bb33e-119">[![Category policy rule page](./media/accruals2-1024x569.png)](./media/accruals2.png)</span></span> 

<span data-ttu-id="bb33e-120">Reikningarnir **Útgjöld innkaupa óreikningsfærð** og **Uppsöfnun innkaupa** í **Bókunaruppsetningu** verða notaðir þegar fylgiskjöl sem eru tengd við innhreyfingarskjal afurða eru bókuð.</span><span class="sxs-lookup"><span data-stu-id="bb33e-120">The **Purchase expenditure un-invoiced** and **Purchase accrual** accounts in **Posting setup** will be used when vouchers that are related to the product receipt are posted.</span></span>

<span data-ttu-id="bb33e-121">Notum þetta sama dæmi til að sjá hvernig bókun innhreyfingarskjals afurða hefur áhrif á fjárhag og verkupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="bb33e-121">Using this same scenario, let's see how posting a product receipt will impact General ledger and Project information.</span></span> 

<span data-ttu-id="bb33e-122">**1. skref:** Stofna og staðfesta nýja innkaupapöntun fyrir verkefnið til að skrá innkaup á tölvu fyrir $1500 og uppsetningarþjónustu fyrir $150.</span><span class="sxs-lookup"><span data-stu-id="bb33e-122">**Step 1:** Create and confirm a new purchase order for the project to record the purchase of a computer for $1500 and installation services for $150.</span></span>
<span data-ttu-id="bb33e-123">[![Stofna nýja innkaupapöntun](./media/accruals4-1024x497.png)](./media/accruals4.png)</span><span class="sxs-lookup"><span data-stu-id="bb33e-123">[![Create new purchase order](./media/accruals4-1024x497.png)](./media/accruals4.png)</span></span> 

<span data-ttu-id="bb33e-124">Þegar innkaupapöntun er staðfest eru færslur fyrir ráðstafaðan kostnað stofnaðar fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="bb33e-124">When the purchase order is confirmed, transactions for the committed cost are created for the project.</span></span> 
<span data-ttu-id="bb33e-125">[![Færslur stofnaðar](./media/accruals5-1024x219.png)](./media/accruals5.png)</span><span class="sxs-lookup"><span data-stu-id="bb33e-125">[![Transactions created](./media/accruals5-1024x219.png)](./media/accruals5.png)</span></span> 

> [!NOTE]
> <span data-ttu-id="bb33e-126">Færslur fyrir ráðstafaðan kostnað munu hafa reitinn **Færsluuppruna** stilltan á **Innkaupapöntun**.</span><span class="sxs-lookup"><span data-stu-id="bb33e-126">The transactions for the committed cost will have the **Transaction Origin** field set to **Purchase Order**.</span></span> <span data-ttu-id="bb33e-127">Stofnun og staðfesting innkaupapöntunar stofnar ekki færslur fyrir verkefni.</span><span class="sxs-lookup"><span data-stu-id="bb33e-127">Creating and confirming a purchase order does not create transactions for a project.</span></span> 

<span data-ttu-id="bb33e-128">**2. skref:** Vörur og þjónustu eru afhentar og innhreyfingarskjal afurða er skráð.</span><span class="sxs-lookup"><span data-stu-id="bb33e-128">**Step 2:** Goods and services get delivered and a product receipt is registered.</span></span> 

<span data-ttu-id="bb33e-129">Bókun innhreyfingarskjals afurða er myndað og bókar fylgiskjalið í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="bb33e-129">Posting a product receipt will generate and post a voucher to the ledger.</span></span> <span data-ttu-id="bb33e-130">Fylgiskjal mun skuldfæra innkaupaútgjöld, óreikningsfærðan lykils og kreditfæra lykil uppsafnaðra innkaupa.</span><span class="sxs-lookup"><span data-stu-id="bb33e-130">The voucher will debit the purchase expenditure, un-invoiced account, and credit purchase accrual account.</span></span> 
<span data-ttu-id="bb33e-131">[![Færslur fylgiskjals](./media/accruals6-1024x214.png)](./media/accruals6.png)</span><span class="sxs-lookup"><span data-stu-id="bb33e-131">[![Voucher transactions](./media/accruals6-1024x214.png)](./media/accruals6.png)</span></span>

> [!NOTE]
> <span data-ttu-id="bb33e-132">Bókun innhreyfingarskjals afurða munu nota bókunaruppsetningu fyrir innkaupategundir og afurðir og ekki bókunaruppsetningu verktegundirnar.</span><span class="sxs-lookup"><span data-stu-id="bb33e-132">Posting a product receipt will use the posting setup for procurement categories and products, and not the posting setup for the project categories.</span></span> <span data-ttu-id="bb33e-133">Til að endurspegla rétt fjárhagsleg áhrif uppsöfnunar innkaupa þarf þessi uppsetning að vera samstillt.</span><span class="sxs-lookup"><span data-stu-id="bb33e-133">In order to correctly reflect financial impact of purchase accruals, this setup needs to be aligned.</span></span> 

<span data-ttu-id="bb33e-134">Hægt er að varpa innkaupaflokka sem verktegundir á síðunni **Innkaupategund**.</span><span class="sxs-lookup"><span data-stu-id="bb33e-134">It is possible to map procurement categories to project categories on the **Procurement category** page.</span></span>
<span data-ttu-id="bb33e-135">[![Síðan Heiti innkaupaflokks](./media/accruals7-1024x390.png)](./media/accruals7.png)</span><span class="sxs-lookup"><span data-stu-id="bb33e-135">[![Procurement category page](./media/accruals7-1024x390.png)](./media/accruals7.png)</span></span>

<span data-ttu-id="bb33e-136">**3. skref:** Stofnaðu reikning lánardrottins</span><span class="sxs-lookup"><span data-stu-id="bb33e-136">**Step 3:** Create a draft vendor invoice.</span></span> 

<span data-ttu-id="bb33e-137">Bókun innhreyfingarskjals afurða ekki áhrif á upplýsingar um verk.</span><span class="sxs-lookup"><span data-stu-id="bb33e-137">Posting a product receipt does not impact project information.</span></span> <span data-ttu-id="bb33e-138">Sem hjáleið er hægt að mynda drög að reikningi lánardrottins beint eftir bókun innhreyfingar innkaupapantana.</span><span class="sxs-lookup"><span data-stu-id="bb33e-138">As a workaround, you could generate a draft vendor invoice right after posting the purchase receipt.</span></span> <span data-ttu-id="bb33e-139">Farðu á síðuna **Innkaupapöntun** á &gt; **Reikningsflipanum** &gt; **Mynda** &gt; **Reiknings**.</span><span class="sxs-lookup"><span data-stu-id="bb33e-139">Go to the **Purchase Order** page &gt; **Invoice tab** &gt; **Generate** &gt; **Invoice**.</span></span> <span data-ttu-id="bb33e-140">Þetta stofnar reikningsskjal í bið sem uppfærir verkupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="bb33e-140">This creates a pending invoice document that updates project information.</span></span> 

<span data-ttu-id="bb33e-141">Stofnun á lánardrottinsreikningsdrögum myndar verkfærslur í bið.</span><span class="sxs-lookup"><span data-stu-id="bb33e-141">Creating a draft vendor invoice will generate pending project transactions.</span></span> 
<span data-ttu-id="bb33e-142">[![Verkfærslur í bið](./media/accruals8-1024x225.png)](./media/accruals8.png)</span><span class="sxs-lookup"><span data-stu-id="bb33e-142">[![Pending project transactions](./media/accruals8-1024x225.png)](./media/accruals8.png)</span></span> 

<span data-ttu-id="bb33e-143">Á síðunni **Ráðstafaður kostnaður** verður færslum sem voru stofnaðar í 1. skrefi lokað og nýjar færslur verða stofnaðar til að endurspegla kostnaðarráðstöfun af reikningi lánardrottins í bið.</span><span class="sxs-lookup"><span data-stu-id="bb33e-143">In the **Committed cost** page, records created in step 1 will be closed and new records will be created to reflect cost commitment coming from the pending vendor invoice.</span></span> <span data-ttu-id="bb33e-144">Í reitnum **Færsluuppruni** fyrir ráðstafaðan kostnað verður stillt á **Lánardrottinsreikning**.</span><span class="sxs-lookup"><span data-stu-id="bb33e-144">The **Transaction origin** field for the committed cost will be set to **Vendor invoice**.</span></span>
<span data-ttu-id="bb33e-145">[![Síðan Ráðstafaður kostnaður](./media/accruals9-1024x200.png)](./media/accruals9.png)</span><span class="sxs-lookup"><span data-stu-id="bb33e-145">[![Commited costs page](./media/accruals9-1024x200.png)](./media/accruals9.png)</span></span>

<span data-ttu-id="bb33e-146">Reikningur lánardrottins mun haldast í biðstöðu þar til að sjálfur reikningur lánardrottins berst.</span><span class="sxs-lookup"><span data-stu-id="bb33e-146">The vendor invoice will remain in a pending state until the actual vendor invoice arrives.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]