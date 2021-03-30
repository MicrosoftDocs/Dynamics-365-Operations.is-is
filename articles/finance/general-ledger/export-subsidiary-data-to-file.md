---
title: Flytja út gögn dótturfyrirtækis í skrár
description: Þetta efnisatriði útskýrir hvernig á að undirbúa útflutning gagna úr Microsoft Dynamics 365 Finance og síðan flytja þau inn í sameinaðan lögaðila.
author: jinniew
manager: AnnBe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 33c17cc2c1dcaa57244bf0bfaa661b11b221e2f6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205500"
---
# <a name="export-subsidiary-data-to-files"></a><span data-ttu-id="5dca1-103">Flytja út gögn dótturfyrirtækis í skrár</span><span class="sxs-lookup"><span data-stu-id="5dca1-103">Export subsidiary data to files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5dca1-104">Síðan **Flytja út** (**Kerfisstjórnun \> Vinnusvæði \> Flytja inn/út**) er notuð til að undirbúa útflutning á gögnum dótturfyrirtækis í skrár sem síðan verður hægt að flytja inn í sameinaðan lögaðila.</span><span class="sxs-lookup"><span data-stu-id="5dca1-104">You use the **Export** page (**System administration \> Workspaces \> Import/Export**) to prepare to export subsidiary data to files that can then be imported into a consolidated legal entity.</span></span> <span data-ttu-id="5dca1-105">Frekari upplýsingar um inn- og útflutningsferlið er að finna í [Yfirliti yfir inn- og útflutningsvinnslu gagna](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="5dca1-105">For more information about the import and export processes, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>

1. <span data-ttu-id="5dca1-106">Stofnið lögaðila fyrir sameiningarferlið.</span><span class="sxs-lookup"><span data-stu-id="5dca1-106">Create a legal entity for the consolidation process.</span></span> <span data-ttu-id="5dca1-107">Frekari upplýsingar um hvernig á að stofna lögaðila er að finna í [Stofna lögaðila](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span><span class="sxs-lookup"><span data-stu-id="5dca1-107">For information about how to create legal entities, see [Create a legal entity](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span></span> <span data-ttu-id="5dca1-108">Frekari upplýsingar er að finna í [Undirbúa lögaðila til að nota í sameiningarferlinu](prepare-company-for-consolidation.md) og [Setja upp dótturfyrirtæki lögaðila fyrir sameiningu](set-up-subsidiary-company-for-consolidation.md).</span><span class="sxs-lookup"><span data-stu-id="5dca1-108">For more information, see [Prepare a legal entity for use in the consolidation process](prepare-company-for-consolidation.md) and [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span> 

2. <span data-ttu-id="5dca1-109">Farið í **Sameiningar \> Flytja út stöður fyrirtækis**.</span><span class="sxs-lookup"><span data-stu-id="5dca1-109">Go to **Consolidations \> Export company balances**.</span></span> <span data-ttu-id="5dca1-110">Á síðunni **Flytja út stöður fyrirtækis**, í flipanum **Skilyrði**, skal tilgreina upplýsingar um sameininguna með því að stilla eftirfarandi reiti.</span><span class="sxs-lookup"><span data-stu-id="5dca1-110">On the **Export company balances** page, on the **Criteria** tab, specify the details of the consolidation by setting the following fields.</span></span>

    | <span data-ttu-id="5dca1-111">Svæði</span><span class="sxs-lookup"><span data-stu-id="5dca1-111">Field</span></span>                             | <span data-ttu-id="5dca1-112">lýsing</span><span class="sxs-lookup"><span data-stu-id="5dca1-112">Description</span></span> |
    |-----------------------------------|-------|
    | <span data-ttu-id="5dca1-113">Aðallykill</span><span class="sxs-lookup"><span data-stu-id="5dca1-113">Main account</span></span>                      | <span data-ttu-id="5dca1-114">Tilgreinið lyklana sem á að sameina.</span><span class="sxs-lookup"><span data-stu-id="5dca1-114">Specify the accounts to consolidate.</span></span> <span data-ttu-id="5dca1-115">Til að hafa alla lykla með skal skilja þennan reit eftir auðan.</span><span class="sxs-lookup"><span data-stu-id="5dca1-115">To include all accounts, leave this field blank.</span></span> |
    | <span data-ttu-id="5dca1-116">Nota samstæðulykil</span><span class="sxs-lookup"><span data-stu-id="5dca1-116">Use consolidation account</span></span>         | <span data-ttu-id="5dca1-117">Ef samstæðulyklar hafa verið tilgreindir skal stilla þennan valkost á **Já**.</span><span class="sxs-lookup"><span data-stu-id="5dca1-117">If you've specified consolidation accounts, set this option to **Yes**.</span></span> |
    | <span data-ttu-id="5dca1-118">Velja samstæðulykil frá</span><span class="sxs-lookup"><span data-stu-id="5dca1-118">Select consolidation account from</span></span> | <span data-ttu-id="5dca1-119">Veljið annaðhvort **Aðallykil** eða **Flokk samstæðulykla**.</span><span class="sxs-lookup"><span data-stu-id="5dca1-119">Select either **Main account** or **Consolidation account group**.</span></span> |
    | <span data-ttu-id="5dca1-120">Flokkur samstæðulykla</span><span class="sxs-lookup"><span data-stu-id="5dca1-120">Consolidation account group</span></span>       | <span data-ttu-id="5dca1-121">Veljið flokk samstæðulykla fyrir samstæðulykilinn sem var valinn.</span><span class="sxs-lookup"><span data-stu-id="5dca1-121">Select a consolidation account group for the consolidation account that you selected.</span></span> |
    | <span data-ttu-id="5dca1-122">Samstæðutímabil</span><span class="sxs-lookup"><span data-stu-id="5dca1-122">Consolidation period</span></span>              | <span data-ttu-id="5dca1-123">Tilgreinið „frá“ og „til“ dagsetningar fyrir samstæðuna.</span><span class="sxs-lookup"><span data-stu-id="5dca1-123">Specify "from" and "to" dates for the consolidation.</span></span> |
    | <span data-ttu-id="5dca1-124">Taka raunupphæðir með</span><span class="sxs-lookup"><span data-stu-id="5dca1-124">Include actual amounts</span></span>            | <span data-ttu-id="5dca1-125">Stillið þennan valkost á **Já** til að hafa með raunupphæðir.</span><span class="sxs-lookup"><span data-stu-id="5dca1-125">Set this option to **Yes** to include actual amounts.</span></span> |
    | <span data-ttu-id="5dca1-126">Taka áætlunarupphæðir með</span><span class="sxs-lookup"><span data-stu-id="5dca1-126">Include budget amounts</span></span>            | <span data-ttu-id="5dca1-127">Stillið þennan valkost á **Já** til að hafa upphæðir fjárhagsáætlunar með í samstæðum.</span><span class="sxs-lookup"><span data-stu-id="5dca1-127">Set this option to **Yes** to include budget amounts in consolidations.</span></span> |
    | <span data-ttu-id="5dca1-128">Fjárhagsáætlunarlíkön</span><span class="sxs-lookup"><span data-stu-id="5dca1-128">Budget models</span></span>                     | <span data-ttu-id="5dca1-129">Tilgreinið fjárhagsáætlunarlíkanið sem á að hafa með.</span><span class="sxs-lookup"><span data-stu-id="5dca1-129">Specify the budget model to include.</span></span> |

3. <span data-ttu-id="5dca1-130">Í flipanum **Fjárhagsvíddir** skal tilgreina upplýsingar um samstæðuna:</span><span class="sxs-lookup"><span data-stu-id="5dca1-130">On the **Financial dimensions** tab, specify the details of the consolidation:</span></span>

    - <span data-ttu-id="5dca1-131">Tilgreinið upplýsingar um fjárhagsvíddir sem á að flytja úr færslunum í lyklum dótturfyrirtækis og yfir í færslurnar í sameinuðum lögaðila.</span><span class="sxs-lookup"><span data-stu-id="5dca1-131">Specify the financial dimension information that should be transferred from the transactions in the subsidiary accounts to the transactions in the consolidated legal entity.</span></span>
    - <span data-ttu-id="5dca1-132">Veljið fjárhagsvíddir úr listanum.</span><span class="sxs-lookup"><span data-stu-id="5dca1-132">Select financial dimensions in the list.</span></span>
    - <span data-ttu-id="5dca1-133">Auðkennið rétta forskrift fyrir hverja fjárhagsvídd sem er sameinuð.</span><span class="sxs-lookup"><span data-stu-id="5dca1-133">Identify the correct specification for each financial dimension that is consolidated.</span></span> <span data-ttu-id="5dca1-134">Tiltækir valmöguleikar fela í sér **Vídd**, **Flokkavídd**, **Lyklar fyrirtækis** og **Lykill**.</span><span class="sxs-lookup"><span data-stu-id="5dca1-134">The available options include **Dimension**, **Group dimension**, **Company accounts**, and **Account**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="5dca1-135">Valkosturinn **Flokkavídd** gerir kleift að skilgreina víddargildi sem er notað af fyrirtækjahópnum sem verið er að sameina.</span><span class="sxs-lookup"><span data-stu-id="5dca1-135">The **Group dimension** option lets you define the dimension value that is used by the group of companies that is being consolidated.</span></span>

    - <span data-ttu-id="5dca1-136">Tilgreinið hlutaröðina til að sameina í.</span><span class="sxs-lookup"><span data-stu-id="5dca1-136">Specify the segment order to consolidate in.</span></span>

4. <span data-ttu-id="5dca1-137">Í flipanum **Lögaðilar** skal fylgja þessum skrefum til að tilgreina lögaðilann sem á að flytja út:</span><span class="sxs-lookup"><span data-stu-id="5dca1-137">On the **Legal entities** tab, follow these steps to specify the legal entity that you're exporting:</span></span>

    1. <span data-ttu-id="5dca1-138">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="5dca1-138">Select **New**.</span></span>
    2. <span data-ttu-id="5dca1-139">Í reitinn **Upprunalegur lögaðili** skal færa inn lögaðilann.</span><span class="sxs-lookup"><span data-stu-id="5dca1-139">In the **Source legal entity** field, enter the legal entity.</span></span>

        <span data-ttu-id="5dca1-140">Ef sama skilyrðið er notað á nokkur dótturfyrirtæki sem eru í sama gagnagrunninum, er hægt að flytja gögn úr þessum dótturfyrirtækjum til þess aðskilja útflutningsskrár í einni aðgerð:</span><span class="sxs-lookup"><span data-stu-id="5dca1-140">If the same criteria apply to several subsidiaries that are in the same database, you can transfer data from those subsidiaries to separate export files in a single operation:</span></span>

        1. <span data-ttu-id="5dca1-141">Stofnið línu fyrir hvern lögaðila dótturfyrirtækis þar sem á að flytja út lykla í skrár.</span><span class="sxs-lookup"><span data-stu-id="5dca1-141">Create a line for each subsidiary legal entity for which accounts should be exported to files.</span></span> <span data-ttu-id="5dca1-142">Þessar skrár eru fluttar inn í samstæðufyrirtæki lögaðilanna seinna.</span><span class="sxs-lookup"><span data-stu-id="5dca1-142">These files will be imported into the consolidated legal entity later.</span></span>
        2. <span data-ttu-id="5dca1-143">Fyrir hvert dótturfyrirtæki er fært inn nafn dótturfyrirtækis og nafn útflutningsskrárinnar sem stofnuð verður í útflutningsvinnslunni.</span><span class="sxs-lookup"><span data-stu-id="5dca1-143">For each subsidiary, enter the subsidiary name and the name of the export file that will be created during the export job.</span></span>

    3. <span data-ttu-id="5dca1-144">Í reitnum **Lyklagerð umreikningsmismunar** skal velja **Hagnaður og tap** eða **Efnahagsreikningur**.</span><span class="sxs-lookup"><span data-stu-id="5dca1-144">In **Account type of conversion differences** field, Select **Profit and loss** or **Balance sheet**.</span></span>
    4. <span data-ttu-id="5dca1-145">Færið inn skráarheiti fyrir útflutningsskrána sem verður stofnuð.</span><span class="sxs-lookup"><span data-stu-id="5dca1-145">Enter a file name for the export file that will be created.</span></span>

5. <span data-ttu-id="5dca1-146">Veljið **Í lagi** til að keyra útflutninginn.</span><span class="sxs-lookup"><span data-stu-id="5dca1-146">Select **OK** to run the export.</span></span>

<span data-ttu-id="5dca1-147">Þegar útflutningi er lokið koma upp skilaboð sem sýna fjölda færslna sem var vistaður í hverja skrá.</span><span class="sxs-lookup"><span data-stu-id="5dca1-147">When the export is completed, you receive a message that shows the number of records that were saved in each file.</span></span> <span data-ttu-id="5dca1-148">Síðan er hægt að flytja inn skrárnar í sameinuðu lögaðilanna.</span><span class="sxs-lookup"><span data-stu-id="5dca1-148">You can then import the files into the consolidated legal entity.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]