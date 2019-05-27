---
title: Bókunarskilgreiningar
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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5fb08a86639e9a9a79dca5fc1200e73e5870432
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564694"
---
# <a name="posting-definition-examples"></a><span data-ttu-id="d0e63-103">Dæmi um bókunarskilgreiningar </span><span class="sxs-lookup"><span data-stu-id="d0e63-103">Posting definition examples</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0e63-104">Þessi grein gefur dæmi sem sýna hvernig bókunarskilgreiningar eru notaðar fyrir fjárúthlutun innkaupapöntunar og fjárveiting fjárhagsáætlunar.</span><span class="sxs-lookup"><span data-stu-id="d0e63-104">This article provides examples that show how posting definitions are used for purchase order encumbrances and budget appropriations.</span></span>

<span data-ttu-id="d0e63-105">Áður en í þessu efnisatriði er lesið, ætti að kynna sér bókunarskilgreiningar og skilgreining færslubókunar.</span><span class="sxs-lookup"><span data-stu-id="d0e63-105">Before you read this topic, you should be familiar with posting definitions and transaction posting definitions.</span></span> <span data-ttu-id="d0e63-106">Sjá upplýsingar í [Bókunarskilgreiningar](posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="d0e63-106">For information, see [Posting definitions](posting-definitions.md).</span></span> <span data-ttu-id="d0e63-107">Eftirfarandi dæmi er hægt að setja á upp á **Bókunarskilgreiningar** síðu.</span><span class="sxs-lookup"><span data-stu-id="d0e63-107">The following examples can be set up on the **Posting definitions** page.</span></span> <span data-ttu-id="d0e63-108">hvert Dæmi inniheldur þessum hlutum:</span><span class="sxs-lookup"><span data-stu-id="d0e63-108">Each example contains these sections:</span></span>

-   <span data-ttu-id="d0e63-109">Bókunarskilgreining – jöfnunarskilyrði</span><span class="sxs-lookup"><span data-stu-id="d0e63-109">Posting definition – Match criteria</span></span>
-   <span data-ttu-id="d0e63-110">bókunarskilgreining – Myndað færslur</span><span class="sxs-lookup"><span data-stu-id="d0e63-110">Posting definition – Generated entries</span></span>
-   <span data-ttu-id="d0e63-111">Færslur með lykla, víddargildi og upphæðir</span><span class="sxs-lookup"><span data-stu-id="d0e63-111">Transactions with the accounts, dimension values, and amounts</span></span>
-   <span data-ttu-id="d0e63-112">fjárhagsfærslur myndaðar úr bókunarskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="d0e63-112">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="d0e63-113">Þegar samsvörun á sér stað milli lykla og víddargildi í **skilyrði fyrir samsvörun** rúðunni fyrir bókunarskilgreiningu og lykla og víddargildi á færslunni, myndast fjárhagsfærslur á grundvelli **Myndaðar færslur** rúðunni fyrir bókunarskilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="d0e63-113">When a match occurs between the accounts and dimension values in the **Match criteria** pane for the posting definition and the accounts and dimension values on the transaction, ledger entries are generated based on the **Generated entries** pane for the posting definition.</span></span> 
> [!NOTE]
> <span data-ttu-id="d0e63-114">Til að tengja bókunarskilgreining við tilgreint færslugerð skal nota síðu **Skilgreiningar færslubókunar**.</span><span class="sxs-lookup"><span data-stu-id="d0e63-114">To associate a posting definition with a specific transaction type, use the **Transaction posting definitions** page.</span></span> <span data-ttu-id="d0e63-115">Eftir að tengja bókunarskilgreiningu við færslugerð og veljið **Nota bókunarskilgreiningar** á **fjárhagsfæribreytur** síðu , verða allar færslur af valinni færslugerð að nota bókunarskilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="d0e63-115">After you associate a posting definition with a transaction type and select **Use posting definitions** on the **General ledger parameters** page, all transactions of the selected transaction type must use posting definitions.</span></span>

## <a name="example-purchase-order-encumbrances"></a><span data-ttu-id="d0e63-116">Dæmi: Fjárúthlutun innkaupapöntunar</span><span class="sxs-lookup"><span data-stu-id="d0e63-116">Example: Purchase order encumbrances</span></span>
<span data-ttu-id="d0e63-117">Þegar þú virkjar fjárúthlutunar með því að velja **Virkja ferli fjárúthlutunar** á **fjárhagsfæribreytur** síðu, verður að nota  bókunarskilgreiningar til að skrá fjárúthlutanir í fjárhaginn fyrir hvaða lykla sem á að taka frá.</span><span class="sxs-lookup"><span data-stu-id="d0e63-117">When you enable encumbrance processing by selecting **Enable encumbrance process** on the **General ledger parameters** page, posting definitions must be used to record encumbrances to the general ledger for any accounts that should be reserved.</span></span> <span data-ttu-id="d0e63-118">Í flestum tilvikum, alla kostnaðarlykla eru teknar frá á efnahagsreikningi.</span><span class="sxs-lookup"><span data-stu-id="d0e63-118">In most cases, all expense accounts are reserved on the balance sheet.</span></span> 

<span data-ttu-id="d0e63-119">Bókunarskilgreiningar fyrir fjárúthlutanir eru settir upp fyrir í **Innkaup** kerfiseiningu á **Bókunarskilgreiningar** síðunni.</span><span class="sxs-lookup"><span data-stu-id="d0e63-119">Posting definitions for encumbrances are set up for the **Purchasing** module on the **Posting definitions** page.</span></span> <span data-ttu-id="d0e63-120">Svo í **Innkaup** svæði í **bókunarskilgreiningar Færslna** síðu er hægt að velja færslugerð **Innkaupapöntunar**  til að tengja bókunarskilgreiningar við innkaupapöntunum.</span><span class="sxs-lookup"><span data-stu-id="d0e63-120">Then, in the **Purchasing** area of the **Transaction posting definitions** page, you can select the **Purchase order** transaction type to associate the posting definition with purchase orders.</span></span> 

<span data-ttu-id="d0e63-121">Allar fylgiskjalafærslur fyrir fjárúthlutanir innkaupapantana að að vera í jafnvægi (debet verða að vera sama og inneign) í hverri einkvmri vídd á fylgiskjal.</span><span class="sxs-lookup"><span data-stu-id="d0e63-121">All voucher transactions for purchase order encumbrances must balance (that is, debits must equal credits) in each unique dimension on a voucher.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="d0e63-122">Bókunarskilgreining – jöfnunarskilyrði</span><span class="sxs-lookup"><span data-stu-id="d0e63-122">Posting definition – Match criteria</span></span>

| <span data-ttu-id="d0e63-123">Lykilskipulag</span><span class="sxs-lookup"><span data-stu-id="d0e63-123">Account structure</span></span>       | <span data-ttu-id="d0e63-124">Samsvarandi lykilnúmer</span><span class="sxs-lookup"><span data-stu-id="d0e63-124">Match account number</span></span> | <span data-ttu-id="d0e63-125">Forgangur </span><span class="sxs-lookup"><span data-stu-id="d0e63-125">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="d0e63-126">Lykilskipulag- P&L</span><span class="sxs-lookup"><span data-stu-id="d0e63-126">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="d0e63-127">1</span><span class="sxs-lookup"><span data-stu-id="d0e63-127">1</span></span>        |

<span data-ttu-id="d0e63-128"><em>Autt gildi í reitnum \**Samsvarandi lykilnúmer</em>* þýðir að allir samsvarandi lyklar í skilgreindu lykilskipulagi eru hluti af samsvörunarreglunni.</span><span class="sxs-lookup"><span data-stu-id="d0e63-128"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="d0e63-129">bókunarskilgreining – Myndað færslur</span><span class="sxs-lookup"><span data-stu-id="d0e63-129">Posting definition – Generated entries</span></span>

| <span data-ttu-id="d0e63-130">Lykilskipulag</span><span class="sxs-lookup"><span data-stu-id="d0e63-130">Account structure</span></span> | <span data-ttu-id="d0e63-131">Myndað lykilnúmer</span><span class="sxs-lookup"><span data-stu-id="d0e63-131">Generated account number</span></span>                    | <span data-ttu-id="d0e63-132">Myndað debet/kredit</span><span class="sxs-lookup"><span data-stu-id="d0e63-132">Generated debit/credit</span></span> |
|-------------------|---------------------------------------------|------------------------|
| <span data-ttu-id="d0e63-133">Staða</span><span class="sxs-lookup"><span data-stu-id="d0e63-133">Balance</span></span>           | <span data-ttu-id="d0e63-134">300143 - -(fjárúthlutunarlykill)</span><span class="sxs-lookup"><span data-stu-id="d0e63-134">300143 - -(Encumbrance account)</span></span>             | <span data-ttu-id="d0e63-135">Sama</span><span class="sxs-lookup"><span data-stu-id="d0e63-135">Same</span></span>                   |
| <span data-ttu-id="d0e63-136">Staða</span><span class="sxs-lookup"><span data-stu-id="d0e63-136">Balance</span></span>           | <span data-ttu-id="d0e63-137">300144 - -(Frátekning fyrir fjárúthlutunarlykill)</span><span class="sxs-lookup"><span data-stu-id="d0e63-137">300144 - -(Reserve for encumbrance account)</span></span> | <span data-ttu-id="d0e63-138">Jafnvægi</span><span class="sxs-lookup"><span data-stu-id="d0e63-138">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="d0e63-139">Færslur með lykla, víddargildi og upphæðir</span><span class="sxs-lookup"><span data-stu-id="d0e63-139">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="d0e63-140">Lyklar og víddargildi koma annað hvort úr dreifing á fjárhagsupphæð sem eru færðar inn fyrir innkaupapöntunarlínu, eða úr lykla og víddir sem eru myndaðar sjálfvirkt á grundvelli sjálfgefnar stillingar fyrir lánardrottna, vörur, flokka og sniðmát víddar.</span><span class="sxs-lookup"><span data-stu-id="d0e63-140">The accounts and dimension values come either from the accounting distributions that you enter for a purchase order line, or from the accounts and dimensions that are automatically generated based on the default settings for vendors, items, categories, and dimension templates.</span></span>

| <span data-ttu-id="d0e63-141">Lykill + víddir</span><span class="sxs-lookup"><span data-stu-id="d0e63-141">Account + dimensions</span></span>           | <span data-ttu-id="d0e63-142">Debet</span><span class="sxs-lookup"><span data-stu-id="d0e63-142">Debit</span></span>  | <span data-ttu-id="d0e63-143">Kredit</span><span class="sxs-lookup"><span data-stu-id="d0e63-143">Credit</span></span> | <span data-ttu-id="d0e63-144">Athugasemd</span><span class="sxs-lookup"><span data-stu-id="d0e63-144">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="d0e63-145">606400-OU\_1-OU\_3566-þjálfun</span><span class="sxs-lookup"><span data-stu-id="d0e63-145">606400-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="d0e63-146">250,00</span><span class="sxs-lookup"><span data-stu-id="d0e63-146">250.00</span></span> |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="d0e63-147">fjárhagsfærslur myndaðar úr bókunarskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="d0e63-147">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="d0e63-148">Fjárhagsfærslur sem myndaðar eru eru stofnaðar til að skrá fjárúthlutanir.</span><span class="sxs-lookup"><span data-stu-id="d0e63-148">Generated ledger entries are created to record the encumbrances.</span></span>

| <span data-ttu-id="d0e63-149">Lykill + víddir</span><span class="sxs-lookup"><span data-stu-id="d0e63-149">Account + dimensions</span></span>           | <span data-ttu-id="d0e63-150">Debet</span><span class="sxs-lookup"><span data-stu-id="d0e63-150">Debit</span></span>  | <span data-ttu-id="d0e63-151">Kredit</span><span class="sxs-lookup"><span data-stu-id="d0e63-151">Credit</span></span> | <span data-ttu-id="d0e63-152">Athugasemd</span><span class="sxs-lookup"><span data-stu-id="d0e63-152">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="d0e63-153">300143-OU\_1-OU\_3566-þjálfun</span><span class="sxs-lookup"><span data-stu-id="d0e63-153">300143-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="d0e63-154">250,00</span><span class="sxs-lookup"><span data-stu-id="d0e63-154">250.00</span></span> |        |         |
| <span data-ttu-id="d0e63-155">300144-OU\_1-OU\_3566-þjálfun</span><span class="sxs-lookup"><span data-stu-id="d0e63-155">300144-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="d0e63-156">250,00</span><span class="sxs-lookup"><span data-stu-id="d0e63-156">250.00</span></span> |         |

<span data-ttu-id="d0e63-157">Í þessu dæmi, hvaða lykil sem er hluti af Lykilskipulagi - P & L samsvarar skilyrði bókunarskilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="d0e63-157">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="d0e63-158">Þess vegna þegar 606500-OU\_1-OU\_3566-Þjálfun er metið, myndaðar færslur eru stofnaðar fyrir reikninga sem eru skilgreindar í **Myndaðar færslur** rúðunni fyrir bókunarskilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="d0e63-158">Therefore, when 606500-OU\_1-OU\_3566-Training is evaluated, generated entries are created for the accounts that are defined in the **Generated entries** pane for the posting definition.</span></span>

## <a name="example-budget-appropriations"></a><span data-ttu-id="d0e63-159">Dæmi: fjárveiting fjárhagsáætlunar</span><span class="sxs-lookup"><span data-stu-id="d0e63-159">Example: Budget appropriations</span></span>
<span data-ttu-id="d0e63-160">Þegar þú leyfa fjárveitingu fjárhagsáætlunar með því að velja **virkja fjárveitingu fjárhagsáætlunar** á **fjárhagsfæribreytur** síðunni, verður að nota bókunarskilgreiningar til að skrá færslur fjárhagsáætlunarskrár í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="d0e63-160">When you enable budget appropriation by selecting **Enable budget appropriation** on the **General ledger parameters** page, posting definitions must be used to record budget register entries to the general ledger.</span></span> <span data-ttu-id="d0e63-161">þegar skilgreining fjárhagsáætlunarstýringar er virk og kveitk á henni, má nota bókunarskilgreiningar og færslu bókunarskilgreiningar til að styðja við skráningu á færslum fyrir greiðsluheimilda, , endurskoðun, flutninga, verk, eignir og framboð og eftirspurnarspár í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="d0e63-161">When a budget control configuration is active and is turned on, posting definitions and transaction posting definitions can be used to support the recording of entries for appropriations, revisions, transfers, projects, fixed assets, and supply and demand forecasts to the general ledger.</span></span> 

<span data-ttu-id="d0e63-162">Til að setja upp bókunarskilgreining fyrir færslur fjárhagsáætlunar í með fjárhagsáætlunargerðina **Upprunalega fjárhagsáætlun**, og sem hefur fjárveiting virkjað, veljið **Fjárhagsáætlun** kerfiseiningu á **Bókunarskilgreiningar** síðu.</span><span class="sxs-lookup"><span data-stu-id="d0e63-162">To set up a posting definition for budget register entries that has a budget type of **Original budget**, and that has appropriations enabled, select the **Budget** module on the **Posting definitions** page.</span></span> <span data-ttu-id="d0e63-163">Síðan, í **Fjárhagsáætlunar** svæði í **skilgreiningar færslubókunar** síðu er hægt er að nota fjárhagsáætlunarkóðana til að tengja bókunarskilgreiningar við færslur fjárhagsáætlunarskrár sem eru með fjárhagsáætlunargerðina **Upprunalega fjárhagsáætlun**.</span><span class="sxs-lookup"><span data-stu-id="d0e63-163">Then, in the **Budget** area of the **Transaction posting definitions** page, you can use budget codes to associate the posting definition with budget register entries that have a budget type of **Original budget**.</span></span> 

<span data-ttu-id="d0e63-164">Þegar fjárveitingar úr fjárhagsáætlun og bókunarskilgreiningar eru virkjaðar, eru færslur fjárhagsáætlunarskrár skráðar fyrir fjárhagsáætlunarstýringu og í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="d0e63-164">When budget appropriations and posting definitions are enabled, the budget register entries are recorded for budget control and in the general ledger.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="d0e63-165">Bókunarskilgreining – jöfnunarskilyrði</span><span class="sxs-lookup"><span data-stu-id="d0e63-165">Posting definition – Match criteria</span></span>

| <span data-ttu-id="d0e63-166">Lykilskipulag</span><span class="sxs-lookup"><span data-stu-id="d0e63-166">Account structure</span></span>       | <span data-ttu-id="d0e63-167">Samsvarandi lykilnúmer</span><span class="sxs-lookup"><span data-stu-id="d0e63-167">Match account number</span></span> | <span data-ttu-id="d0e63-168">Forgangur </span><span class="sxs-lookup"><span data-stu-id="d0e63-168">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="d0e63-169">Lykilskipulag- P&L</span><span class="sxs-lookup"><span data-stu-id="d0e63-169">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="d0e63-170">1</span><span class="sxs-lookup"><span data-stu-id="d0e63-170">1</span></span>        |

<span data-ttu-id="d0e63-171"><em>Autt gildi í reitnum \**Samsvarandi lykilnúmer</em>* þýðir að allir samsvarandi lyklar í skilgreindu lykilskipulagi eru hluti af samsvörunarreglunni.</span><span class="sxs-lookup"><span data-stu-id="d0e63-171"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="d0e63-172">bókunarskilgreining – Myndað færslur</span><span class="sxs-lookup"><span data-stu-id="d0e63-172">Posting definition – Generated entries</span></span>

| <span data-ttu-id="d0e63-173">Lykilskipulag</span><span class="sxs-lookup"><span data-stu-id="d0e63-173">Account structure</span></span> | <span data-ttu-id="d0e63-174">Myndað lykilnúmer</span><span class="sxs-lookup"><span data-stu-id="d0e63-174">Generated account number</span></span>              | <span data-ttu-id="d0e63-175">Myndað debet/kredit</span><span class="sxs-lookup"><span data-stu-id="d0e63-175">Generated debit/credit</span></span> |
|-------------------|---------------------------------------|------------------------|
| <span data-ttu-id="d0e63-176">Lykilskipulag</span><span class="sxs-lookup"><span data-stu-id="d0e63-176">Account structure</span></span> | <span data-ttu-id="d0e63-177">300145 - -(Áætlað tekjur lykill)</span><span class="sxs-lookup"><span data-stu-id="d0e63-177">300145 - -(Estimated revenue account)</span></span> | <span data-ttu-id="d0e63-178">Sama</span><span class="sxs-lookup"><span data-stu-id="d0e63-178">Same</span></span>                   |
| <span data-ttu-id="d0e63-179">Lykilskipulag</span><span class="sxs-lookup"><span data-stu-id="d0e63-179">Account structure</span></span> | <span data-ttu-id="d0e63-180">300146 - -(fjárúthlutunarlykill)</span><span class="sxs-lookup"><span data-stu-id="d0e63-180">300146 - -(Appropriation account)</span></span>     | <span data-ttu-id="d0e63-181">Jafnvægi</span><span class="sxs-lookup"><span data-stu-id="d0e63-181">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="d0e63-182">Færslur með lykla, víddargildi og upphæðir</span><span class="sxs-lookup"><span data-stu-id="d0e63-182">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="d0e63-183">Færa inn lykla, víddargildi og upphæðir fyrir færsla fjárhagsáætlunarlykils við **færsla í fjárhagsáætlunarskrá** síðu.</span><span class="sxs-lookup"><span data-stu-id="d0e63-183">You enter the accounts, dimension values, and amounts for the budget account entry on the **Budget register entry** page.</span></span>

| <span data-ttu-id="d0e63-184">Lykill + víddir</span><span class="sxs-lookup"><span data-stu-id="d0e63-184">Account + dimensions</span></span>           | <span data-ttu-id="d0e63-185">Debet</span><span class="sxs-lookup"><span data-stu-id="d0e63-185">Debit</span></span> | <span data-ttu-id="d0e63-186">Kredit</span><span class="sxs-lookup"><span data-stu-id="d0e63-186">Credit</span></span> | <span data-ttu-id="d0e63-187">Athugasemd</span><span class="sxs-lookup"><span data-stu-id="d0e63-187">Comment</span></span> |
|--------------------------------|-------|--------|---------|
| <span data-ttu-id="d0e63-188">606400-OU\_1-OU\_3566-þjálfun</span><span class="sxs-lookup"><span data-stu-id="d0e63-188">606400-OU\_1-OU\_3566-Training</span></span> |       | <span data-ttu-id="d0e63-189">250,00</span><span class="sxs-lookup"><span data-stu-id="d0e63-189">250.00</span></span> |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="d0e63-190">fjárhagsfærslur myndaðar úr bókunarskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="d0e63-190">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="d0e63-191">Fjárhagsfærslur eru myndaðar til að skrá upprunalega fjárhagsáætlun á hverja vídd.</span><span class="sxs-lookup"><span data-stu-id="d0e63-191">Generated ledger entries are created to record the original budget in each dimension.</span></span>

| <span data-ttu-id="d0e63-192">Lykill + víddir</span><span class="sxs-lookup"><span data-stu-id="d0e63-192">Account + dimensions</span></span>           | <span data-ttu-id="d0e63-193">Debet</span><span class="sxs-lookup"><span data-stu-id="d0e63-193">Debit</span></span>  | <span data-ttu-id="d0e63-194">Kredit</span><span class="sxs-lookup"><span data-stu-id="d0e63-194">Credit</span></span> | <span data-ttu-id="d0e63-195">Athugasemd</span><span class="sxs-lookup"><span data-stu-id="d0e63-195">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="d0e63-196">300145-OU\_1-OU\_3566-þjálfun</span><span class="sxs-lookup"><span data-stu-id="d0e63-196">300145-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="d0e63-197">250,00</span><span class="sxs-lookup"><span data-stu-id="d0e63-197">250.00</span></span> |         |
| <span data-ttu-id="d0e63-198">300146-OU\_1-OU\_3566-þjálfun</span><span class="sxs-lookup"><span data-stu-id="d0e63-198">300146-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="d0e63-199">250,00</span><span class="sxs-lookup"><span data-stu-id="d0e63-199">250.00</span></span> |        |         |

<span data-ttu-id="d0e63-200">Í þessu dæmi, hvaða lykil sem er hluti af Lykilskipulagi - P & L samsvarar skilyrði bókunarskilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="d0e63-200">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="d0e63-201">Þess vegna þegar 606400-OU\_1-OU\_3566-Training er metið, eru myndaðar fjárhagsfærslur stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="d0e63-201">Therefore, when 606400-OU\_1-OU\_3566-Training is evaluated, the generated ledger entries are created.</span></span>





