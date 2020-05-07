---
title: Stofna ítarlega samninga fyrir greiðslur sem miðast við framvindu
description: Þetta efnisatriði útskýrir hvernig á að búa til verksamninga svo að þú getir búið til reikninga fyrir viðskiptavini, miðað við prósentuhlutfall lokinna verka.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 90cae104d0abad909606ef6a0e0c45ed95e74de2
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282831"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="0a0e3-103">Stofna ítarlega samninga fyrir greiðslur sem miðast við framvindu</span><span class="sxs-lookup"><span data-stu-id="0a0e3-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a0e3-104">Þetta efnisatriði útskýrir hvernig á að búa til verksamninga svo að þú getir stofnað reikninga fyrir viðskiptavini, miðað við prósentuhlutfall lokinna verka.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="0a0e3-105">Reikningsupphæðir eru sjálfkrafa reiknaðar út fyrir tegundir fjárhagsáætlunar vinnu sem er sett upp fyrir verk.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="0a0e3-106">Tímasetning reikningsins er stillt þegar samið er um verksamninginn við viðskiptavininn.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="0a0e3-107">Notið aðferðirnar í þessu efnisatriði til þess að setja upp samning, tengt verk, og reikningsreglur sem nota á við útreikning reikningsupphæða fyrir tegundir fjárhagsáætlunar vinnu sem er sett upp fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="0a0e3-108">Þegar þú hefur stofnað samninginn og verkið, er hægt að setja upp upplýsingarnar um verkið.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="0a0e3-109">Til dæmis er hægt að skilgreina aðgerðir og úthluta starfsmönnum til verksins.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="0a0e3-110">Dæmi</span><span class="sxs-lookup"><span data-stu-id="0a0e3-110">Example</span></span>

<span data-ttu-id="0a0e3-111">Fyrirtæki notanda er fyrirtæki í hugbúnaðarþróun.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-111">Your organization is a software development firm.</span></span> <span data-ttu-id="0a0e3-112">Þú samþykkir að þróa launabókhaldspakka fyrir viðskiptavin vegna heildargjalda sem nema 20.000 bandaríkjadölum (USD).</span><span class="sxs-lookup"><span data-stu-id="0a0e3-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="0a0e3-113">Fyrirtækið samþykkir að senda reikning til viðskiptavinarins samhliða því að það lýkur tilteknu hlutfalli verksins.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="0a0e3-114">Þú setur upp eftirfarandi verkflokka fyrir verkið, þannig að þú getir notað þá í reikningagerð:</span><span class="sxs-lookup"><span data-stu-id="0a0e3-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="0a0e3-115">Ráðgjöf</span><span class="sxs-lookup"><span data-stu-id="0a0e3-115">Consulting</span></span>
- <span data-ttu-id="0a0e3-116">Hönnun</span><span class="sxs-lookup"><span data-stu-id="0a0e3-116">Design</span></span>
- <span data-ttu-id="0a0e3-117">Uppsetning</span><span class="sxs-lookup"><span data-stu-id="0a0e3-117">Installation</span></span>

<span data-ttu-id="0a0e3-118">Þú setur einnig upp reglur sem reikna sjálfkrafa upphæð reiknings fyrir hlutfall vinnu við verk sem er lokið í hverjum flokki fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="0a0e3-119">Stjórnandi fjárhagsáætlunar stofnar fjárhagsáætlun fyrir verkflokkana.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="0a0e3-120">Upphæð lokinnar vinnu er sjálfkrafa reiknað sem hlutfall raunvinnu samanborið við upphæðir fjárhagsáætlunarinnar.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0a0e3-121">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="0a0e3-121">Prerequisites</span></span>

<span data-ttu-id="0a0e3-122">Áður en þú stofnar verk sem notar reikningsreglur verður þú að setja upp númeraröð fyrir reikningsreglur og þóknunarbók sem er notuð til að bóka útskriftir samkvæmt framvindu.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="0a0e3-123">Opnaðu **Verkefnastjórnun og bókhald** \> **Uppsetning** \> **Færibreytur verkefnastjórnunar og bókhalds**.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="0a0e3-124">Á síðunni **Verkefnastjórnun og bókhaldsfæribreytur** á flipanum **Númeraraðir** setur þú upp númeraröðina sem skal nota þegar reikningsreglur eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="0a0e3-125">Opnaðu **Verkefnastjórnun og bókhald** \> **Færslubækur** \> **Gjald**.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="0a0e3-126">Á síðunni **Gjaldabók** velurðu **Nýtt** og slærð inn heiti færslubókarinnar.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="0a0e3-127">Stofna samning fyrir framvinduútskriftir</span><span class="sxs-lookup"><span data-stu-id="0a0e3-127">Create a contract for progress billings</span></span>

<span data-ttu-id="0a0e3-128">Notið þessa aðferð til þess að stofna verksamning fyrir fastverðsverk.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="0a0e3-129">Stofnaður er verkreikningur þegar vinnan sem lokið er fyrir verkið nær tilteknu hlutfalli.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="0a0e3-130">Opnaðu **Verkefnastjórnun og bókhald** \> **Verk** \> **Verksamningar**.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="0a0e3-131">Veldu **Nýtt** á síðunni **Verksamningar**.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="0a0e3-132">Stillið eftirfarandi svæði í svarglugganum **Nýr verksamningur**:</span><span class="sxs-lookup"><span data-stu-id="0a0e3-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="0a0e3-133">**Nafn**</span><span class="sxs-lookup"><span data-stu-id="0a0e3-133">**Name**</span></span>
    - <span data-ttu-id="0a0e3-134">**Gerð fjármögnunar**</span><span class="sxs-lookup"><span data-stu-id="0a0e3-134">**Funding type**</span></span>
    - <span data-ttu-id="0a0e3-135">**Fjármögnunaraðili**</span><span class="sxs-lookup"><span data-stu-id="0a0e3-135">**Funding source**</span></span>
    - <span data-ttu-id="0a0e3-136">**Sölugjaldmiðill** Sjálfgefið er að þessi gjaldmiðill sé notaður fyrir reikninga viðskiptavina sem tengjast verksamningnum.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="0a0e3-137">Hins vegar er hægt að breyta sölugjaldmiðlinum á tilteknum reikningi viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="0a0e3-138">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-138">Select **OK**.</span></span> <span data-ttu-id="0a0e3-139">Upplýsingarnar eru afritaðar í haus síðunnar **Verksamningar**.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="0a0e3-140">Á síðunni **Verksamningar** skal ljúka við að fylla út í nauðsynlegar upplýsingar fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="0a0e3-141">Stofna verk fyrir framvinduútskriftir</span><span class="sxs-lookup"><span data-stu-id="0a0e3-141">Create a project for progress billings</span></span>

<span data-ttu-id="0a0e3-142">Fylgdu eftirfarandi skrefum til að stofna verk og undirverk af hvaða toga sem tengjast verksamningi.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="0a0e3-143">Opnaðu **Verkefnastjórnun og bókhald** \> **Verk** \> **Öll verk**.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="0a0e3-144">Á síðunni **Öll verk** velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="0a0e3-145">Í svarglugganum **Nýtt verk** í svæðinu **Gerð verk** velurðu **Tími og efni**.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="0a0e3-146">Veljið verkflokk.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-146">Select a project group.</span></span> <span data-ttu-id="0a0e3-147">Verkflokkur skilgreinir bókunarupplýsingar verka sem eru tengd við flokkinn.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="0a0e3-148">Velja **Stofna verk**.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-148">Select **Create project**.</span></span>
6. <span data-ttu-id="0a0e3-149">Eftir að búið er að stofna verkið, skal stilla verkstigið á **Í vinnslu**.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="0a0e3-150">Stofna áætlun fyrir verk</span><span class="sxs-lookup"><span data-stu-id="0a0e3-150">Create a budget for a project</span></span>

<span data-ttu-id="0a0e3-151">Tegundir fjárhagsáætlunar eru notaðar til að reikna sjálfkrafa út reikningsupphæðir fyrir hlutfall þeirrar vinnu sem er lokið fyrir hverja flokka.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="0a0e3-152">Fylgdu þessum skrefum til að stofna fjárhagsáætlunarflokka fyrir áætlaðan kostnað.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="0a0e3-153">Opnaðu **Verkefnastjórnun og bókhald** \> **Verk** \> **Öll verk**.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="0a0e3-154">Á síðunni **Öll verk** velurðu og opnar verkið sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="0a0e3-155">Á síðunni **Verk** á Aðgerðasvæðinu á flipanum **Áætlun** í hópnum **Fjárhagsáætlun** velurðu **Fjárhagsáætlun verks**.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="0a0e3-156">Á síðunni **Fjárhagsáætlun verks** skaltu færa inn áætlaðan kostnað fyrir hvern flokk í verkinu.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="0a0e3-157">Stofna reikningsreglur fyrir framvinduútskriftir</span><span class="sxs-lookup"><span data-stu-id="0a0e3-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="0a0e3-158">Opnaðu **Verkefnastjórnun og bókhald** \> **Verk** \> **Verksamningar**.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="0a0e3-159">Veldu og opnaðu verksamning á síðunni **Verksamningar**.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="0a0e3-160">Á síðu verksamningsins á flýtiflipanum **Reikningsreglur** velurðu **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="0a0e3-161">Á síðunni **Reikningsregla** á svæðinu **Línugerð** velurðu **Framvinda**.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="0a0e3-162">Á flýtiflipanum **Upplýsingar um reikningsreglulínu** á svæðinu **Samningsvirði** slærðu inn heildarvirði samningsins.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="0a0e3-163">Á svæðinu **Flokkur** skal velja flokkinn til að bóka þóknunarfærsluna í.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="0a0e3-164">Á svæðinu **Verk** er valið verk sem notar þessa reikningsreglu.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="0a0e3-165">Valfrjálst: Hægt er að úthluta reikningsreglunni til annarra verka.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="0a0e3-166">Á flýtiflipanum **Verk** í hlutanum **Tiltæk verk** velurðu verk og síðan hægri örvarhnappinn til að bæta verkinu við hlutan **Valin verk**.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="0a0e3-167">Valfrjálst: Reikna út hlutfall upphæðar sem viðskiptavinurinn heldur eftir af greiðslum á reikningi.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="0a0e3-168">Á flýtiflipanum **Varðveisluskilmála greiðslu** skal velja uppruna fjármögnunar og síðan færa varðveisluprósentuna inn á svæðinu **Varðveisluprósenta**.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="0a0e3-169">Þessi skref eru endurtekin til að stofna fleiri reikningsreglur fyrir verksamninginn.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-169">Repeat these steps to create additional billing rules for the project contract.</span></span>
