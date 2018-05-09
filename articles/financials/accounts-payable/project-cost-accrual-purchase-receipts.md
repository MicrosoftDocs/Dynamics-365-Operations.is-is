---
title: "Uppsöfnun á kostnaði verks á innkaupapöntunum"
description: "Þetta efnisatriði lýsir því hvernig hægt er að rekja uppsafnaðan verkkostnað úr innkaupapöntunum í Microsoft Dynamics 365 for Finance and Operations."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 91c605eedeb84243c15cf372e4f25fb7587a00e1
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="project-cost-accrual-on-purchase-receipts"></a><span data-ttu-id="0c5cc-103">Uppsöfnun á kostnaði verks á innkaupapöntunum</span><span class="sxs-lookup"><span data-stu-id="0c5cc-103">Project cost accrual on purchase receipts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c5cc-104">Þetta efnisatriði lýsir því hvernig hægt er að rekja uppsafnaðan verkkostnað úr innkaupapöntunum í Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-104">This topic describes how accrued project costs from purchase receipts can be tracked in Microsoft Dynamics 365 for Finance and Operations.</span></span> 

<span data-ttu-id="0c5cc-105">Reikningar fyrir verk berast oft síðar en vörur og þjónusta eru afhent, sem kann að hafa töluverð áhrif á afkastavísa verkefna (Afkastavísa).</span><span class="sxs-lookup"><span data-stu-id="0c5cc-105">Invoices for a project often arrive later than the goods and services are delivered, which might have a significant impact on project key performance indicators (KPIs).</span></span> <span data-ttu-id="0c5cc-106">Mikilvægt er að það sé hægt að rekja þessar færslur í bæði fjárhags- og verkefnaskýrslum.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-106">It important to be able to track these transactions in both financial and project reports.</span></span>

<span data-ttu-id="0c5cc-107">Eftirfarandi dæmi lýsir þessum aðstæðum.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-107">The following example scenario illustrates this.</span></span> 

<span data-ttu-id="0c5cc-108">Contoso Consulting hefur komið á fót nýjum skýjarekstri.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-108">Contoso Consulting has started a new cloud deployment project.</span></span> <span data-ttu-id="0c5cc-109">Innkaupapöntun er stofnuð til að kaupa tölvu fyrir verkefnið.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-109">A purchase order is created to buy a computer for the project.</span></span> <span data-ttu-id="0c5cc-110">Tölvan mun kosta $1500 og uppsetningarþjónusta mun kosta $150.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-110">The computer will cost $1500 and installation services will cost $150.</span></span> <span data-ttu-id="0c5cc-111">Lánardrottinn hefur afhent og sett tölvuna upp, en reikningur hefur ekki enn borist Contoso Consulting.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-111">The vendor has delivered and installed the computer, but the invoice has not yet reached Contoso Consulting.</span></span> <span data-ttu-id="0c5cc-112">Stjórnanda verksins langar að sjá kostnaðaruppsöfnun verkefnisins upp á $1650 áður en reikningurinn er afhentur.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-112">The project manager would like to see project cost accrual of $1650 before the invoice gets delivered.</span></span> <span data-ttu-id="0c5cc-113">Þessi kostnaður ætti einnig að endurspeglast í fjárhagsskýrslum fyrirtækisins í mánuðarlok.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-113">This cost should also be reflected in the company's month end financial statements.</span></span> 

<span data-ttu-id="0c5cc-114">Uppsafnaðan kostnað þarf að skrá bæði á fjárhagslegu stigi og verkstig fyrir skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-114">The accrued cost needs to be recorded on both the financial level and project level for reporting purposes.</span></span> <span data-ttu-id="0c5cc-115">Í Finance and Operations er hægt að rekja fjárhagslega uppfærslu afurðarinnar fyrir vöru- og innkaupaflokka.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-115">In Finance and Operations, the financial update of the product receipt can be tracked for the item and procurement categories.</span></span> 

<span data-ttu-id="0c5cc-116">Fyrir vörur, á síðunni **Færibreytur viðskiptaskulda**, veljið valkostinn **Bóka innhreyfingarskjöl afurða í fjárhag**.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-116">For items, on the **Accounts payable parameters** page, select the **Post product receipts to ledger** option.</span></span>
<span data-ttu-id="0c5cc-117">[![uppsafnanir1](./media/accruals1-1024x409.png)](./media/accruals1.png)</span><span class="sxs-lookup"><span data-stu-id="0c5cc-117">[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png)</span></span> 

<span data-ttu-id="0c5cc-118">Fyrir innkaupategundir, á síðunni **Stefnuregla tegundar** skal velja reglurnar **Innkaup** og síðan **Safna upp innkaupakostnaði á kvittun** fyrir hvern innkaupaflokk.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-118">For procurement categories, on the **Category policy rule** page, select **Purchasing** policies, and then select **Accrue purchase expense on receipt** for each procurement category.</span></span>
<span data-ttu-id="0c5cc-119">[![uppsafnanir2](./media/accruals2-1024x569.png)](./media/accruals2.png)</span><span class="sxs-lookup"><span data-stu-id="0c5cc-119">[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png)</span></span> 

<span data-ttu-id="0c5cc-120">Reikningarnir **Útgjöld innkaupa óreikningsfærð** og **Uppsöfnun innkaupa** í **Bókunaruppsetningu** verða notaðir þegar fylgiskjöl sem eru tengd við innhreyfingarskjal afurða eru bókuð.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-120">The **Purchase expenditure un-invoiced** and **Purchase accrual** accounts in **Posting setup** will be used when vouchers that are related to the product receipt are posted.</span></span>
<span data-ttu-id="0c5cc-121">[![uppsafnanir3](./media/accruals3-1024x429.png)](./media/accruals3.png)</span><span class="sxs-lookup"><span data-stu-id="0c5cc-121">[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png)</span></span> 

<span data-ttu-id="0c5cc-122">Notum þetta sama dæmi til að sjá hvernig bókun innhreyfingarskjals afurða hefur áhrif á fjárhag og verkupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-122">Using this same scenario, let's see how posting a product receipt will impact General ledger and Project information.</span></span> 

<span data-ttu-id="0c5cc-123">**1. skref:** Stofna og staðfesta nýja innkaupapöntun fyrir verkefnið til að skrá innkaup á tölvu fyrir $1500 og uppsetningarþjónustu fyrir $150.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-123">**Step 1:** Create and confirm a new purchase order for the project to record the purchase of a computer for $1500 and installation services for $150.</span></span>
<span data-ttu-id="0c5cc-124">[![uppsafnanir4](./media/accruals4-1024x497.png)](./media/accruals4.png)</span><span class="sxs-lookup"><span data-stu-id="0c5cc-124">[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png)</span></span> 

<span data-ttu-id="0c5cc-125">Þegar innkaupapöntun er staðfest eru færslur fyrir ráðstafaðan kostnað stofnaðar fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-125">When the purchase order is confirmed, transactions for the committed cost are created for the project.</span></span> 
<span data-ttu-id="0c5cc-126">[![uppsafnanir5](./media/accruals5-1024x219.png)](./media/accruals5.png)</span><span class="sxs-lookup"><span data-stu-id="0c5cc-126">[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png)</span></span> 

> [!NOTE]
> <span data-ttu-id="0c5cc-127">Færslur fyrir ráðstafaðan kostnað munu hafa reitinn **Færsluuppruna** stilltan á **Innkaupapöntun**.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-127">The transactions for the committed cost will have the **Transaction Origin** field set to **Purchase Order**.</span></span> <span data-ttu-id="0c5cc-128">Stofnun og staðfesting innkaupapöntunar stofnar ekki færslur fyrir verkefni.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-128">Creating and confirming a purchase order does not create transactions for a project.</span></span> 

<span data-ttu-id="0c5cc-129">**2. skref:** Vörur og þjónustu eru afhentar og innhreyfingarskjal afurða er skráð.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-129">**Step 2:** Goods and services get delivered and a product receipt is registered.</span></span> 

<span data-ttu-id="0c5cc-130">Bókun innhreyfingarskjals afurða er myndað og bókar fylgiskjalið í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-130">Posting a product receipt will generate and post a voucher to the ledger.</span></span> <span data-ttu-id="0c5cc-131">Fylgiskjal mun skuldfæra innkaupaútgjöld, óreikningsfærðan lykils og kreditfæra lykil uppsafnaðra innkaupa.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-131">The voucher will debit the purchase expenditure, un-invoiced account, and credit purchase accrual account.</span></span> 
<span data-ttu-id="0c5cc-132">[![uppsafnanir6](./media/accruals6-1024x214.png)](./media/accruals6.png)</span><span class="sxs-lookup"><span data-stu-id="0c5cc-132">[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)</span></span>

> [!NOTE]
> <span data-ttu-id="0c5cc-133">Bókun innhreyfingarskjals afurða munu nota bókunaruppsetningu fyrir innkaupategundir og afurðir og ekki bókunaruppsetningu verktegundirnar.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-133">Posting a product receipt will use the posting setup for procurement categories and products, and not the posting setup for the project categories.</span></span> <span data-ttu-id="0c5cc-134">Til að endurspegla rétt fjárhagsleg áhrif uppsöfnunar innkaupa þarf þessi uppsetning að vera samstillt.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-134">In order to correctly reflect financial impact of purchase accruals, this setup needs to be aligned.</span></span> 

<span data-ttu-id="0c5cc-135">Hægt er að varpa innkaupaflokka sem verktegundir á síðunni **Innkaupategund**.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-135">It is possible to map procurement categories to project categories on the **Procurement category** page.</span></span>
<span data-ttu-id="0c5cc-136">[![uppsafnanir7](./media/accruals7-1024x390.png)](./media/accruals7.png)</span><span class="sxs-lookup"><span data-stu-id="0c5cc-136">[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)</span></span>

<span data-ttu-id="0c5cc-137">**3. skref:** Stofnaðu reikning lánardrottins</span><span class="sxs-lookup"><span data-stu-id="0c5cc-137">**Step 3:** Create a draft vendor invoice.</span></span> 

<span data-ttu-id="0c5cc-138">Í Finance and Operations hefur bókun innhreyfingarskjals afurða ekki áhrif á upplýsingar um verk.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-138">In Finance and Operations, posting a product receipt does not impact project information.</span></span> <span data-ttu-id="0c5cc-139">Sem hjáleið er hægt að mynda drög að reikningi lánardrottins beint eftir bókun innhreyfingar innkaupapantana.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-139">As a workaround, you could generate a draft vendor invoice right after posting the purchase receipt.</span></span> <span data-ttu-id="0c5cc-140">Farðu á síðuna **Innkaupapöntun** á &gt;**Reikningsflipanum**&gt;**Mynda**&gt;**Reiknings**.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-140">Go to the **Purchase Order** page &gt; **Invoice tab** &gt; **Generate** &gt; **Invoice**.</span></span> <span data-ttu-id="0c5cc-141">Þetta stofnar reikningsskjal í bið sem uppfærir verkupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-141">This creates a pending invoice document that updates project information.</span></span> 

<span data-ttu-id="0c5cc-142">Stofnun á lánardrottinsreikningsdrögum myndar verkfærslur í bið.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-142">Creating a draft vendor invoice will generate pending project transactions.</span></span> 
<span data-ttu-id="0c5cc-143">[![uppsafnanir8](./media/accruals8-1024x225.png)](./media/accruals8.png)</span><span class="sxs-lookup"><span data-stu-id="0c5cc-143">[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png)</span></span> 

<span data-ttu-id="0c5cc-144">Á síðunni **Ráðstafaður kostnaður** verður færslum sem voru stofnaðar í 1. skrefi lokað og nýjar færslur verða stofnaðar til að endurspegla kostnaðarráðstöfun af reikningi lánardrottins í bið.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-144">In the **Committed cost** page, records created in step 1 will be closed and new records will be created to reflect cost commitment coming from the pending vendor invoice.</span></span> <span data-ttu-id="0c5cc-145">Í reitnum **Færsluuppruni** fyrir ráðstafaðan kostnað verður stillt á **Lánardrottinsreikning**.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-145">The **Transaction origin** field for the committed cost will be set to **Vendor invoice**.</span></span>
<span data-ttu-id="0c5cc-146">[![uppsafnanir9](./media/accruals9-1024x200.png)](./media/accruals9.png)</span><span class="sxs-lookup"><span data-stu-id="0c5cc-146">[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)</span></span>

<span data-ttu-id="0c5cc-147">Reikningur lánardrottins mun haldast í biðstöðu þar til að sjálfur reikningur lánardrottins berst.</span><span class="sxs-lookup"><span data-stu-id="0c5cc-147">The vendor invoice will remain in a pending state until the actual vendor invoice arrives.</span></span>




