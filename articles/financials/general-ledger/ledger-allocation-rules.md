---
title: "Úthlutunarreglur fjárhags"
description: "Þessi grein gefur upplýsingar um úthlutunarreglur fjárhags. Hún lýsir hinum ýmsu þáttum þessara úthlutunarreglna og úthlutunaraðferðunum sem hægt er að nota fyrir þær."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAllocation, LedgerAllocationBasisRule, LedgerAllocationRequest, LedgerAllocationRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15402
ms.assetid: 8147e148-7c11-45ef-95c6-f9889a875b54
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: abbeb1bb4481139dff902916362a479f94fb96e5
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---

# <a name="ledger-allocation-rules"></a><span data-ttu-id="1c49b-104">Úthlutunarreglur fjárhags</span><span class="sxs-lookup"><span data-stu-id="1c49b-104">Ledger allocation rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c49b-105">Þessi grein gefur upplýsingar um úthlutunarreglur fjárhags.</span><span class="sxs-lookup"><span data-stu-id="1c49b-105">This article provides information about ledger allocation rules.</span></span> <span data-ttu-id="1c49b-106">Hún lýsir hinum ýmsu þáttum þessara úthlutunarreglna og úthlutunaraðferðunum sem hægt er að nota fyrir þær.</span><span class="sxs-lookup"><span data-stu-id="1c49b-106">It describes the various components of these allocation rules and the allocation methods that can be used for them.</span></span>

<span data-ttu-id="1c49b-107">Úthlutunarreglur fjárhags eru notaðar til að reikna sjálfkrafa og búa til úthlutunarbækur og færslur í lykil fyrir úthlutun á fjárhagsstöðum eða föstum upphæðum</span><span class="sxs-lookup"><span data-stu-id="1c49b-107">Ledger allocation rules are used to automatically calculate and generate allocation journals and account entries for the allocation of ledger balances or fixed amounts.</span></span> <span data-ttu-id="1c49b-108">Úthlutunaraðferðir geta verið breytilegar eða fastar.</span><span class="sxs-lookup"><span data-stu-id="1c49b-108">Allocation methods can be variable or fixed.</span></span> <span data-ttu-id="1c49b-109">Hægt er að nota eftirfarandi úthlutunaraðferðir fyrir úthlutunarreglur fjárhags:</span><span class="sxs-lookup"><span data-stu-id="1c49b-109">The following allocation methods can be used for ledger allocation rules:</span></span>

-   <span data-ttu-id="1c49b-110">**Grunnur** – Þessi breytuaðferð er notuð þegar úthlutun fer eftir raunverulegri fjárhagsstöðu, byggt á skilyrðum síunnar.</span><span class="sxs-lookup"><span data-stu-id="1c49b-110">**Basis** – This variable method is used when the allocation depends on the actual ledger balance, based on filter criteria.</span></span> <span data-ttu-id="1c49b-111">Til dæmis væri hægt að úthluta auglýsingakostnaði byggt á sölu hverrar deildar í samræmi við heildarsölu deildar.</span><span class="sxs-lookup"><span data-stu-id="1c49b-111">For example, advertising expenses can be allocated based on each department's sales in proportion to the total departmental sales.</span></span>
-   <span data-ttu-id="1c49b-112">**Föst prósenta** og **Föst þyngd** – Fyrir þessar aðferðir er úthlutunarhlutfall eða þyngd skilgreind beint fyrir regluna.</span><span class="sxs-lookup"><span data-stu-id="1c49b-112">**Fixed percentage** and **Fixed weight** – For these methods, the allocation percentage or weight is defined directly for the rule.</span></span> <span data-ttu-id="1c49b-113">Til dæmis er hægt að úthluta auglýsingakostnaði þannig að Deild A taki 70 prósent auglýsingakostnaðar og Deild B fái 30 prósent.</span><span class="sxs-lookup"><span data-stu-id="1c49b-113">For example, advertising expenses can be allocated so that Department A receives 70 percent of the advertising expense and Department B receives 30 percent.</span></span>
-   <span data-ttu-id="1c49b-114">**Jafnt** – Þessi aðferð dreifir upphæð jafnt á hvern skilgreindan áfangastað.</span><span class="sxs-lookup"><span data-stu-id="1c49b-114">**Equally** – This method distributes the amount equally to each defined destination.</span></span> <span data-ttu-id="1c49b-115">Til dæmis, ef áfangastaðir eru skilgreindir fyrir Deild A og Deild B, er hægt að úthluta auglýsingakostnaði þannig Deild A og Deild B fá 50 prósent auglýsingakostnaðar.</span><span class="sxs-lookup"><span data-stu-id="1c49b-115">For example, if destinations are defined for Department A and Department B, advertising expenses can be allocated so that both Department A and Department B receive 50 percent of the advertising expense.</span></span>

<span data-ttu-id="1c49b-116">Ef úthlutunaraðferð úthlutunarreglunnar er Grunnur verður einnig að skilgreina sérstakar grunnreglur fjárhagsúthlutunar.</span><span class="sxs-lookup"><span data-stu-id="1c49b-116">If Basis is used as the allocation method for an allocation rule, you must also define separate ledger allocation basis rules.</span></span> <span data-ttu-id="1c49b-117">Ferlið „Vinna úthlutunarbeiðni“ gerir notendum kleift að keyra úthlutunarreglu fjárhags og forskoða meðfylgjandi úthlutunarbókafærslur áður en þær bóka annaðhvort eða eyða reiknuðum úthlutunum.</span><span class="sxs-lookup"><span data-stu-id="1c49b-117">The "Process allocation request" process lets users process the ledger allocation rule and preview the resulting allocation journal entries before they either post or delete the calculated allocations.</span></span>

## <a name="components-of-ledger-allocation-rules"></a><span data-ttu-id="1c49b-118">Íhlutir úthlutunarreglna fjárhags</span><span class="sxs-lookup"><span data-stu-id="1c49b-118">Components of ledger allocation rules</span></span>
<span data-ttu-id="1c49b-119">Hver úthlutunarregla hefur fjóra meginþætti: almennt, uppruna, áfangastað og mótbókun.</span><span class="sxs-lookup"><span data-stu-id="1c49b-119">Each allocation rule has four components: general, source, destination, and offset.</span></span> <span data-ttu-id="1c49b-120">Viðbótaríhlutur, grunnúthlutunarreglur fjárhags, er nauðsynlegur ef Grunnur er notaður seð úthlutunaraðferð.</span><span class="sxs-lookup"><span data-stu-id="1c49b-120">An additional component, ledger allocation bases rules, is required if Basis is used as the allocation method.</span></span> <span data-ttu-id="1c49b-121">Hver íhlutur veitir mikilvægar upplýsingar sem er krafist til að keyra úthlutanir.</span><span class="sxs-lookup"><span data-stu-id="1c49b-121">Each component provides a critical piece of the information that is required in order to process allocations.</span></span>

-   <span data-ttu-id="1c49b-122">**Almennt** – Þessi íhlutur er þar sem notandinn skilgreinir valkosti eins og úthlutunarreglu, stillingar samstæðureglu og hvort reglan sé virk eða ekki.</span><span class="sxs-lookup"><span data-stu-id="1c49b-122">**General** – This component is where the user specifies options such as the allocation method, intercompany rule settings, and whether the rule is active.</span></span>
-   <span data-ttu-id="1c49b-123">**Uppruni** – Þessi íhlutur er þar sem notandinn tilgreinir upprunagögn fyrir úthlutunina.</span><span class="sxs-lookup"><span data-stu-id="1c49b-123">**Source** – This component is where the user specifies the source data for the allocation.</span></span> <span data-ttu-id="1c49b-124">Hægt er að byggja úthlutun á fjárhagsstöðum (**Gagnagjafi** = **= Fjárhagur**) eða föstum upphæðum (**Gagnagjafi =** = **Fast gildi**).</span><span class="sxs-lookup"><span data-stu-id="1c49b-124">Allocation can be based on ledger balances (**Data source** = **Ledger**) or fixed amounts (**Data source** = **Fixed value**).</span></span> <span data-ttu-id="1c49b-125">Þegar **Gagnagjafi** er stilltur á **Fjárhag**, verður að skilgreina uppruna síuskilyrða fyrir úthlutunarreglu fjárhags (til dæmis, fyrir auglýsingakostnað).</span><span class="sxs-lookup"><span data-stu-id="1c49b-125">When **Data source** is set to **Ledger**, source filter criteria must be defined for the ledger allocation rule (for example, for the advertising expenses).</span></span>
-   <span data-ttu-id="1c49b-126">**Viðtökustaður** – Þessi íhlutur skilgreinir hvernig dreifa skal og gera grein fyrir niðurstöðu úthlutunarútreiknings.</span><span class="sxs-lookup"><span data-stu-id="1c49b-126">**Destination** – This component defines how the result of the allocation calculation should be distributed and accounted for.</span></span> <span data-ttu-id="1c49b-127">Til dæmis getur verið ein lína áfangastaðar fyrir hverja deild.</span><span class="sxs-lookup"><span data-stu-id="1c49b-127">For example, there can be one destination line for each department.</span></span>
-   <span data-ttu-id="1c49b-128">**Mótlykill** – Þessi íhlutur skilgreinir hvernig ákvarða skal aðallykla og víddir fyrir mótfærslurnar sem jafna færslur á áfangastað.</span><span class="sxs-lookup"><span data-stu-id="1c49b-128">**Offset** – This component defines how main accounts and dimensions should be determined for the offset entries that balance the destination entries.</span></span> <span data-ttu-id="1c49b-129">Þessar færslur eru yfirleitt notaðar í stað lykla og vídda sem eru byggðar á grunni uppruna.</span><span class="sxs-lookup"><span data-stu-id="1c49b-129">User-defined options are typically used instead of accounts and dimensions that are based on the source.</span></span> <span data-ttu-id="1c49b-130">Þegar **Gagnagjafi** er stilltur á **Fast gildi**, er ekki hægt að nota **Uppruna** sem valkost.</span><span class="sxs-lookup"><span data-stu-id="1c49b-130">When **Data source** is set to **Fixed value**, **Source** can't be used as an option.</span></span>
-   <span data-ttu-id="1c49b-131">**Grunnreglur fjárhagsúthlutunar** – Þessar reglur nota eigin skilyrði upprunasíu til að ákvarða hvaða fjárhagsstöður á að nota fyrir úthlutun (til dæmis tekjur á deild).</span><span class="sxs-lookup"><span data-stu-id="1c49b-131">**Ledger allocation basis rules** – These rules use their own source filter criteria to determine which ledger balances should be used for allocation (for example, the revenue per department).</span></span> <span data-ttu-id="1c49b-132">Hægt er að nota grunnreglu úthlutunar með mörgum úthlutunarreglum.</span><span class="sxs-lookup"><span data-stu-id="1c49b-132">Each allocation basis rule can be used with multiple allocation rules.</span></span>





