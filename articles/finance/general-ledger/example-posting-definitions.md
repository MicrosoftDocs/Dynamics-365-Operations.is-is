---
title: Dæmi um bókunarskilgreiningar
description: Þessi grein gefur dæmi sem sýna hvernig bókunarskilgreiningar eru notaðar fyrir fjárúthlutun innkaupapöntunar og fjárveiting fjárhagsáætlunar.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 301f15f1d7d8f0e10bbaf2546fcf727aff284624
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/03/2019
ms.locfileid: "2552303"
---
# <a name="posting-definition-examples"></a><span data-ttu-id="8fe62-103">Dæmi um bókunarskilgreiningar</span><span class="sxs-lookup"><span data-stu-id="8fe62-103">Posting definition examples</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8fe62-104">Þessi grein gefur dæmi sem sýna hvernig bókunarskilgreiningar eru notaðar fyrir fjárúthlutun innkaupapöntunar og fjárveiting fjárhagsáætlunar.</span><span class="sxs-lookup"><span data-stu-id="8fe62-104">This article provides examples that show how posting definitions are used for purchase order encumbrances and budget appropriations.</span></span>

<span data-ttu-id="8fe62-105">Áður en í þessu efnisatriði er lesið, ætti að kynna sér bókunarskilgreiningar og skilgreining færslubókunar.</span><span class="sxs-lookup"><span data-stu-id="8fe62-105">Before you read this topic, you should be familiar with posting definitions and transaction posting definitions.</span></span> <span data-ttu-id="8fe62-106">Sjá upplýsingar í [Bókunarskilgreiningar](posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="8fe62-106">For information, see [Posting definitions](posting-definitions.md).</span></span> <span data-ttu-id="8fe62-107">Eftirfarandi dæmi er hægt að setja á upp á **Bókunarskilgreiningar** síðu.</span><span class="sxs-lookup"><span data-stu-id="8fe62-107">The following examples can be set up on the **Posting definitions** page.</span></span> <span data-ttu-id="8fe62-108">hvert Dæmi inniheldur þessum hlutum:</span><span class="sxs-lookup"><span data-stu-id="8fe62-108">Each example contains these sections:</span></span>

-   <span data-ttu-id="8fe62-109">Bókunarskilgreining – jöfnunarskilyrði</span><span class="sxs-lookup"><span data-stu-id="8fe62-109">Posting definition – Match criteria</span></span>
-   <span data-ttu-id="8fe62-110">bókunarskilgreining – Myndað færslur</span><span class="sxs-lookup"><span data-stu-id="8fe62-110">Posting definition – Generated entries</span></span>
-   <span data-ttu-id="8fe62-111">Færslur með lykla, víddargildi og upphæðir</span><span class="sxs-lookup"><span data-stu-id="8fe62-111">Transactions with the accounts, dimension values, and amounts</span></span>
-   <span data-ttu-id="8fe62-112">fjárhagsfærslur myndaðar úr bókunarskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="8fe62-112">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="8fe62-113">Þegar samsvörun á sér stað milli lykla og víddargildi í **skilyrði fyrir samsvörun** rúðunni fyrir bókunarskilgreiningu og lykla og víddargildi á færslunni, myndast fjárhagsfærslur á grundvelli **Myndaðar færslur** rúðunni fyrir bókunarskilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="8fe62-113">When a match occurs between the accounts and dimension values in the **Match criteria** pane for the posting definition and the accounts and dimension values on the transaction, ledger entries are generated based on the **Generated entries** pane for the posting definition.</span></span> 
> [!NOTE]
> <span data-ttu-id="8fe62-114">Til að tengja bókunarskilgreining við tilgreint færslugerð skal nota síðu **Skilgreiningar færslubókunar**.</span><span class="sxs-lookup"><span data-stu-id="8fe62-114">To associate a posting definition with a specific transaction type, use the **Transaction posting definitions** page.</span></span> <span data-ttu-id="8fe62-115">Eftir að tengja bókunarskilgreiningu við færslugerð og veljið **Nota bókunarskilgreiningar** á **fjárhagsfæribreytur** síðu , verða allar færslur af valinni færslugerð að nota bókunarskilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="8fe62-115">After you associate a posting definition with a transaction type and select **Use posting definitions** on the **General ledger parameters** page, all transactions of the selected transaction type must use posting definitions.</span></span>

## <a name="example-purchase-order-encumbrances"></a><span data-ttu-id="8fe62-116">Dæmi: Fjárúthlutun innkaupapöntunar</span><span class="sxs-lookup"><span data-stu-id="8fe62-116">Example: Purchase order encumbrances</span></span>
<span data-ttu-id="8fe62-117">Þegar þú virkjar fjárúthlutunar með því að velja **Virkja ferli fjárúthlutunar** á **fjárhagsfæribreytur** síðu, verður að nota bókunarskilgreiningar til að skrá fjárúthlutanir í fjárhaginn fyrir hvaða lykla sem á að taka frá.</span><span class="sxs-lookup"><span data-stu-id="8fe62-117">When you enable encumbrance processing by selecting **Enable encumbrance process** on the **General ledger parameters** page, posting definitions must be used to record encumbrances to the general ledger for any accounts that should be reserved.</span></span> <span data-ttu-id="8fe62-118">Í flestum tilvikum, alla kostnaðarlykla eru teknar frá á efnahagsreikningi.</span><span class="sxs-lookup"><span data-stu-id="8fe62-118">In most cases, all expense accounts are reserved on the balance sheet.</span></span> 

<span data-ttu-id="8fe62-119">Bókunarskilgreiningar fyrir fjárúthlutanir eru settir upp fyrir í **Innkaup** kerfiseiningu á **Bókunarskilgreiningar** síðunni.</span><span class="sxs-lookup"><span data-stu-id="8fe62-119">Posting definitions for encumbrances are set up for the **Purchasing** module on the **Posting definitions** page.</span></span> <span data-ttu-id="8fe62-120">Svo í **Innkaup** svæði í **bókunarskilgreiningar Færslna** síðu er hægt að velja færslugerð **Innkaupapöntunar** til að tengja bókunarskilgreiningar við innkaupapöntunum.</span><span class="sxs-lookup"><span data-stu-id="8fe62-120">Then, in the **Purchasing** area of the **Transaction posting definitions** page, you can select the **Purchase order** transaction type to associate the posting definition with purchase orders.</span></span> 

<span data-ttu-id="8fe62-121">Allar fylgiskjalafærslur fyrir fjárúthlutanir innkaupapantana að að vera í jafnvægi (debet verða að vera sama og inneign) í hverri einkvmri vídd á fylgiskjal.</span><span class="sxs-lookup"><span data-stu-id="8fe62-121">All voucher transactions for purchase order encumbrances must balance (that is, debits must equal credits) in each unique dimension on a voucher.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="8fe62-122">Bókunarskilgreining – jöfnunarskilyrði</span><span class="sxs-lookup"><span data-stu-id="8fe62-122">Posting definition – Match criteria</span></span>

| <span data-ttu-id="8fe62-123">Lykilskipulag</span><span class="sxs-lookup"><span data-stu-id="8fe62-123">Account structure</span></span>       | <span data-ttu-id="8fe62-124">Samsvarandi lykilnúmer</span><span class="sxs-lookup"><span data-stu-id="8fe62-124">Match account number</span></span> | <span data-ttu-id="8fe62-125">Forgangur</span><span class="sxs-lookup"><span data-stu-id="8fe62-125">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="8fe62-126">Lykilskipulag- P&L</span><span class="sxs-lookup"><span data-stu-id="8fe62-126">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="8fe62-127">1</span><span class="sxs-lookup"><span data-stu-id="8fe62-127">1</span></span>        |

<span data-ttu-id="8fe62-128"><em>Autt gildi í reitnum \**Samsvarandi lykilnúmer</em>* þýðir að allir samsvarandi lyklar í skilgreindu lykilskipulagi eru hluti af samsvörunarreglunni.</span><span class="sxs-lookup"><span data-stu-id="8fe62-128"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="8fe62-129">bókunarskilgreining – Myndað færslur</span><span class="sxs-lookup"><span data-stu-id="8fe62-129">Posting definition – Generated entries</span></span>

| <span data-ttu-id="8fe62-130">Lykilskipulag</span><span class="sxs-lookup"><span data-stu-id="8fe62-130">Account structure</span></span> | <span data-ttu-id="8fe62-131">Myndað lykilnúmer</span><span class="sxs-lookup"><span data-stu-id="8fe62-131">Generated account number</span></span>                    | <span data-ttu-id="8fe62-132">Myndað debet/kredit</span><span class="sxs-lookup"><span data-stu-id="8fe62-132">Generated debit/credit</span></span> |
|-------------------|---------------------------------------------|------------------------|
| <span data-ttu-id="8fe62-133">Staða</span><span class="sxs-lookup"><span data-stu-id="8fe62-133">Balance</span></span>           | <span data-ttu-id="8fe62-134">300143 - -(fjárúthlutunarlykill)</span><span class="sxs-lookup"><span data-stu-id="8fe62-134">300143 - -(Encumbrance account)</span></span>             | <span data-ttu-id="8fe62-135">Sama</span><span class="sxs-lookup"><span data-stu-id="8fe62-135">Same</span></span>                   |
| <span data-ttu-id="8fe62-136">Staða</span><span class="sxs-lookup"><span data-stu-id="8fe62-136">Balance</span></span>           | <span data-ttu-id="8fe62-137">300144 - -(Frátekning fyrir fjárúthlutunarlykill)</span><span class="sxs-lookup"><span data-stu-id="8fe62-137">300144 - -(Reserve for encumbrance account)</span></span> | <span data-ttu-id="8fe62-138">Jafnvægi</span><span class="sxs-lookup"><span data-stu-id="8fe62-138">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="8fe62-139">Færslur með lykla, víddargildi og upphæðir</span><span class="sxs-lookup"><span data-stu-id="8fe62-139">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="8fe62-140">Lyklar og víddargildi koma annað hvort úr dreifing á fjárhagsupphæð sem eru færðar inn fyrir innkaupapöntunarlínu, eða úr lykla og víddir sem eru myndaðar sjálfvirkt á grundvelli sjálfgefnar stillingar fyrir lánardrottna, vörur, flokka og sniðmát víddar.</span><span class="sxs-lookup"><span data-stu-id="8fe62-140">The accounts and dimension values come either from the accounting distributions that you enter for a purchase order line, or from the accounts and dimensions that are automatically generated based on the default settings for vendors, items, categories, and dimension templates.</span></span>

| <span data-ttu-id="8fe62-141">Lykill + víddir</span><span class="sxs-lookup"><span data-stu-id="8fe62-141">Account + dimensions</span></span>           | <span data-ttu-id="8fe62-142">Debet</span><span class="sxs-lookup"><span data-stu-id="8fe62-142">Debit</span></span>  | <span data-ttu-id="8fe62-143">Kredit</span><span class="sxs-lookup"><span data-stu-id="8fe62-143">Credit</span></span> | <span data-ttu-id="8fe62-144">Athugasemd</span><span class="sxs-lookup"><span data-stu-id="8fe62-144">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="8fe62-145">606400-OU\_1-OU\_3566-þjálfun</span><span class="sxs-lookup"><span data-stu-id="8fe62-145">606400-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="8fe62-146">250,00</span><span class="sxs-lookup"><span data-stu-id="8fe62-146">250.00</span></span> |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="8fe62-147">fjárhagsfærslur myndaðar úr bókunarskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="8fe62-147">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="8fe62-148">Fjárhagsfærslur sem myndaðar eru eru stofnaðar til að skrá fjárúthlutanir.</span><span class="sxs-lookup"><span data-stu-id="8fe62-148">Generated ledger entries are created to record the encumbrances.</span></span>

| <span data-ttu-id="8fe62-149">Lykill + víddir</span><span class="sxs-lookup"><span data-stu-id="8fe62-149">Account + dimensions</span></span>           | <span data-ttu-id="8fe62-150">Debet</span><span class="sxs-lookup"><span data-stu-id="8fe62-150">Debit</span></span>  | <span data-ttu-id="8fe62-151">Kredit</span><span class="sxs-lookup"><span data-stu-id="8fe62-151">Credit</span></span> | <span data-ttu-id="8fe62-152">Athugasemd</span><span class="sxs-lookup"><span data-stu-id="8fe62-152">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="8fe62-153">300143-OU\_1-OU\_3566-þjálfun</span><span class="sxs-lookup"><span data-stu-id="8fe62-153">300143-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="8fe62-154">250,00</span><span class="sxs-lookup"><span data-stu-id="8fe62-154">250.00</span></span> |        |         |
| <span data-ttu-id="8fe62-155">300144-OU\_1-OU\_3566-þjálfun</span><span class="sxs-lookup"><span data-stu-id="8fe62-155">300144-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="8fe62-156">250,00</span><span class="sxs-lookup"><span data-stu-id="8fe62-156">250.00</span></span> |         |

<span data-ttu-id="8fe62-157">Í þessu dæmi, hvaða lykil sem er hluti af Lykilskipulagi - P&L samsvarar skilyrði bókunarskilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="8fe62-157">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="8fe62-158">Þess vegna þegar 606500-OU\_1-OU\_3566-Þjálfun er metið, myndaðar færslur eru stofnaðar fyrir reikninga sem eru skilgreindar í **Myndaðar færslur** rúðunni fyrir bókunarskilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="8fe62-158">Therefore, when 606500-OU\_1-OU\_3566-Training is evaluated, generated entries are created for the accounts that are defined in the **Generated entries** pane for the posting definition.</span></span>

## <a name="example-budget-appropriations"></a><span data-ttu-id="8fe62-159">Dæmi: fjárveiting fjárhagsáætlunar</span><span class="sxs-lookup"><span data-stu-id="8fe62-159">Example: Budget appropriations</span></span>
<span data-ttu-id="8fe62-160">Þegar þú leyfa fjárveitingu fjárhagsáætlunar með því að velja **virkja fjárveitingu fjárhagsáætlunar** á **fjárhagsfæribreytur** síðunni, verður að nota bókunarskilgreiningar til að skrá færslur fjárhagsáætlunarskrár í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="8fe62-160">When you enable budget appropriation by selecting **Enable budget appropriation** on the **General ledger parameters** page, posting definitions must be used to record budget register entries to the general ledger.</span></span> <span data-ttu-id="8fe62-161">þegar skilgreining fjárhagsáætlunarstýringar er virk og kveitk á henni, má nota bókunarskilgreiningar og færslu bókunarskilgreiningar til að styðja við skráningu á færslum fyrir greiðsluheimilda, , endurskoðun, flutninga, verk, eignir og framboð og eftirspurnarspár í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="8fe62-161">When a budget control configuration is active and is turned on, posting definitions and transaction posting definitions can be used to support the recording of entries for appropriations, revisions, transfers, projects, fixed assets, and supply and demand forecasts to the general ledger.</span></span> 

<span data-ttu-id="8fe62-162">Til að setja upp bókunarskilgreining fyrir færslur fjárhagsáætlunar í með fjárhagsáætlunargerðina **Upprunalega fjárhagsáætlun**, og sem hefur fjárveiting virkjað, veljið **Fjárhagsáætlun** kerfiseiningu á **Bókunarskilgreiningar** síðu.</span><span class="sxs-lookup"><span data-stu-id="8fe62-162">To set up a posting definition for budget register entries that has a budget type of **Original budget**, and that has appropriations enabled, select the **Budget** module on the **Posting definitions** page.</span></span> <span data-ttu-id="8fe62-163">Síðan, í **Fjárhagsáætlunar** svæði í **skilgreiningar færslubókunar** síðu er hægt er að nota fjárhagsáætlunarkóðana til að tengja bókunarskilgreiningar við færslur fjárhagsáætlunarskrár sem eru með fjárhagsáætlunargerðina **Upprunalega fjárhagsáætlun**.</span><span class="sxs-lookup"><span data-stu-id="8fe62-163">Then, in the **Budget** area of the **Transaction posting definitions** page, you can use budget codes to associate the posting definition with budget register entries that have a budget type of **Original budget**.</span></span> 

<span data-ttu-id="8fe62-164">Þegar fjárveitingar úr fjárhagsáætlun og bókunarskilgreiningar eru virkjaðar, eru færslur fjárhagsáætlunarskrár skráðar fyrir fjárhagsáætlunarstýringu og í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="8fe62-164">When budget appropriations and posting definitions are enabled, the budget register entries are recorded for budget control and in the general ledger.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="8fe62-165">Bókunarskilgreining – jöfnunarskilyrði</span><span class="sxs-lookup"><span data-stu-id="8fe62-165">Posting definition – Match criteria</span></span>

| <span data-ttu-id="8fe62-166">Lykilskipulag</span><span class="sxs-lookup"><span data-stu-id="8fe62-166">Account structure</span></span>       | <span data-ttu-id="8fe62-167">Samsvarandi lykilnúmer</span><span class="sxs-lookup"><span data-stu-id="8fe62-167">Match account number</span></span> | <span data-ttu-id="8fe62-168">Forgangur</span><span class="sxs-lookup"><span data-stu-id="8fe62-168">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="8fe62-169">Lykilskipulag- P&L</span><span class="sxs-lookup"><span data-stu-id="8fe62-169">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="8fe62-170">1</span><span class="sxs-lookup"><span data-stu-id="8fe62-170">1</span></span>        |

<span data-ttu-id="8fe62-171"><em>Autt gildi í reitnum \**Samsvarandi lykilnúmer</em>* þýðir að allir samsvarandi lyklar í skilgreindu lykilskipulagi eru hluti af samsvörunarreglunni.</span><span class="sxs-lookup"><span data-stu-id="8fe62-171"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="8fe62-172">bókunarskilgreining – Myndað færslur</span><span class="sxs-lookup"><span data-stu-id="8fe62-172">Posting definition – Generated entries</span></span>

| <span data-ttu-id="8fe62-173">Lykilskipulag</span><span class="sxs-lookup"><span data-stu-id="8fe62-173">Account structure</span></span> | <span data-ttu-id="8fe62-174">Myndað lykilnúmer</span><span class="sxs-lookup"><span data-stu-id="8fe62-174">Generated account number</span></span>              | <span data-ttu-id="8fe62-175">Myndað debet/kredit</span><span class="sxs-lookup"><span data-stu-id="8fe62-175">Generated debit/credit</span></span> |
|-------------------|---------------------------------------|------------------------|
| <span data-ttu-id="8fe62-176">Lykilskipulag</span><span class="sxs-lookup"><span data-stu-id="8fe62-176">Account structure</span></span> | <span data-ttu-id="8fe62-177">300145 - -(Áætlað tekjur lykill)</span><span class="sxs-lookup"><span data-stu-id="8fe62-177">300145 - -(Estimated revenue account)</span></span> | <span data-ttu-id="8fe62-178">Sama</span><span class="sxs-lookup"><span data-stu-id="8fe62-178">Same</span></span>                   |
| <span data-ttu-id="8fe62-179">Lykilskipulag</span><span class="sxs-lookup"><span data-stu-id="8fe62-179">Account structure</span></span> | <span data-ttu-id="8fe62-180">300146 - -(fjárúthlutunarlykill)</span><span class="sxs-lookup"><span data-stu-id="8fe62-180">300146 - -(Appropriation account)</span></span>     | <span data-ttu-id="8fe62-181">Jafnvægi</span><span class="sxs-lookup"><span data-stu-id="8fe62-181">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="8fe62-182">Færslur með lykla, víddargildi og upphæðir</span><span class="sxs-lookup"><span data-stu-id="8fe62-182">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="8fe62-183">Færa inn lykla, víddargildi og upphæðir fyrir færsla fjárhagsáætlunarlykils við **færsla í fjárhagsáætlunarskrá** síðu.</span><span class="sxs-lookup"><span data-stu-id="8fe62-183">You enter the accounts, dimension values, and amounts for the budget account entry on the **Budget register entry** page.</span></span>

| <span data-ttu-id="8fe62-184">Lykill + víddir</span><span class="sxs-lookup"><span data-stu-id="8fe62-184">Account + dimensions</span></span>           | <span data-ttu-id="8fe62-185">Debet</span><span class="sxs-lookup"><span data-stu-id="8fe62-185">Debit</span></span> | <span data-ttu-id="8fe62-186">Kredit</span><span class="sxs-lookup"><span data-stu-id="8fe62-186">Credit</span></span> | <span data-ttu-id="8fe62-187">Athugasemd</span><span class="sxs-lookup"><span data-stu-id="8fe62-187">Comment</span></span> |
|--------------------------------|-------|--------|---------|
| <span data-ttu-id="8fe62-188">606400-OU\_1-OU\_3566-þjálfun</span><span class="sxs-lookup"><span data-stu-id="8fe62-188">606400-OU\_1-OU\_3566-Training</span></span> |       | <span data-ttu-id="8fe62-189">250,00</span><span class="sxs-lookup"><span data-stu-id="8fe62-189">250.00</span></span> |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="8fe62-190">fjárhagsfærslur myndaðar úr bókunarskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="8fe62-190">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="8fe62-191">Fjárhagsfærslur eru myndaðar til að skrá upprunalega fjárhagsáætlun á hverja vídd.</span><span class="sxs-lookup"><span data-stu-id="8fe62-191">Generated ledger entries are created to record the original budget in each dimension.</span></span>

| <span data-ttu-id="8fe62-192">Lykill + víddir</span><span class="sxs-lookup"><span data-stu-id="8fe62-192">Account + dimensions</span></span>           | <span data-ttu-id="8fe62-193">Debet</span><span class="sxs-lookup"><span data-stu-id="8fe62-193">Debit</span></span>  | <span data-ttu-id="8fe62-194">Kredit</span><span class="sxs-lookup"><span data-stu-id="8fe62-194">Credit</span></span> | <span data-ttu-id="8fe62-195">Athugasemd</span><span class="sxs-lookup"><span data-stu-id="8fe62-195">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="8fe62-196">300145-OU\_1-OU\_3566-þjálfun</span><span class="sxs-lookup"><span data-stu-id="8fe62-196">300145-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="8fe62-197">250,00</span><span class="sxs-lookup"><span data-stu-id="8fe62-197">250.00</span></span> |         |
| <span data-ttu-id="8fe62-198">300146-OU\_1-OU\_3566-þjálfun</span><span class="sxs-lookup"><span data-stu-id="8fe62-198">300146-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="8fe62-199">250,00</span><span class="sxs-lookup"><span data-stu-id="8fe62-199">250.00</span></span> |        |         |

<span data-ttu-id="8fe62-200">Í þessu dæmi, hvaða lykil sem er hluti af Lykilskipulagi - P&L samsvarar skilyrði bókunarskilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="8fe62-200">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="8fe62-201">Þess vegna þegar 606400-OU\_1-OU\_3566-Training er metið, eru myndaðar fjárhagsfærslur stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="8fe62-201">Therefore, when 606400-OU\_1-OU\_3566-Training is evaluated, the generated ledger entries are created.</span></span>




