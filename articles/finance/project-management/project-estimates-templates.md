---
title: Samstilla verkáætlanir beint frá Project Service Automation við Finance and Operations
description: Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla tímaáætlun verks og kostnaðaráætlun verks beint frá Microsoft Dynamics 365 Project Service Automation til Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: ebf0fce60ad006e798aa4f404fbffcf10a0b31f9
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770290"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="067c3-103">Samstilla verkáætlanir beint frá Project Service Automation við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="067c3-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="067c3-104">Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla tímaáætlun verks og kostnaðaráætlun verks beint frá Dynamics 365 Project Service Automation til Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="067c3-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="067c3-105">Samþætting verkefna fyrir verk, flokkar kostnaðarfærslna, áætlaður tími, kostnaðaráætlun og virknilæsing er í boði í útgáfu 8.0.</span><span class="sxs-lookup"><span data-stu-id="067c3-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="067c3-106">Samþætting á rauntölum er í boði í útgáfu 8.0.1 eða nýrri.</span><span class="sxs-lookup"><span data-stu-id="067c3-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="067c3-107">Gagnaflæði fyrir Project Service Automation til Finance</span><span class="sxs-lookup"><span data-stu-id="067c3-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="067c3-108">Samþættingarlausn Project Service Automation við Finance notar eiginleika gagnasamþættingar til að samstilla gögn þvert yfir tilvik af Project Service Automation og Finance.</span><span class="sxs-lookup"><span data-stu-id="067c3-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="067c3-109">Samþættingarsniðmátin sem eru tiltæk með eiginleika gagnasamþættingar gera gögnum kleift að flæða varðandi áætlaðan tíma verks og kostnaðarmat verks frá Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="067c3-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="067c3-110">Eftirfarandi skýringarmynd sýnir hvernig gögnin eru samstillt milli Project Service Automation og Finance.</span><span class="sxs-lookup"><span data-stu-id="067c3-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="067c3-111">[![Gagnaflæði fyrir samþættingu Project Service Automation við Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="067c3-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="067c3-112">Áætlaðar verkstundir</span><span class="sxs-lookup"><span data-stu-id="067c3-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="067c3-113">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="067c3-113">Template and tasks</span></span>

<span data-ttu-id="067c3-114">Til að fá aðgang að tiltækum sniðmátum, í stjórnendamiðstöð Microsoft Power Apps, skal velja **Verk** og síðan í efra hægra horninu skal velja **Nýtt verk** til að velja almenn sniðmát.</span><span class="sxs-lookup"><span data-stu-id="067c3-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="067c3-115">Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla áætlaðan tíma verks frá Project Service Automation við Finance:</span><span class="sxs-lookup"><span data-stu-id="067c3-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="067c3-116">**Heiti sniðmátsins í gagnasamþættingu:** Áætlaður tími verks (PSA til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="067c3-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="067c3-117">**Heiti verkefna í verkinu:**</span><span class="sxs-lookup"><span data-stu-id="067c3-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="067c3-118">Færslutengsl</span><span class="sxs-lookup"><span data-stu-id="067c3-118">Transaction relationships</span></span>
    - <span data-ttu-id="067c3-119">Kostnaðaráætlanir</span><span class="sxs-lookup"><span data-stu-id="067c3-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="067c3-120">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="067c3-120">Entity set</span></span>

| <span data-ttu-id="067c3-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="067c3-121">Project Service Automation</span></span> | <span data-ttu-id="067c3-122">Fjármál</span><span class="sxs-lookup"><span data-stu-id="067c3-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="067c3-123">Verkefni</span><span class="sxs-lookup"><span data-stu-id="067c3-123">Project tasks</span></span>              | <span data-ttu-id="067c3-124">Samþættingareining fyrir áætlaðar verkstundir</span><span class="sxs-lookup"><span data-stu-id="067c3-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="067c3-125">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="067c3-125">Entity flow</span></span>

<span data-ttu-id="067c3-126">Áætluðum tíma verks er stjórnað í Project Service Automation og hann er samstilltur við Finance sem tímaspá verks.</span><span class="sxs-lookup"><span data-stu-id="067c3-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="067c3-127">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="067c3-127">Prerequisites</span></span>

<span data-ttu-id="067c3-128">Áður en samstilling á áætluðum tíma verks getur átt sér stað verður þú að samstilla flokka fyrir verk, verkefni verks og kostnaðarfærslur verks.</span><span class="sxs-lookup"><span data-stu-id="067c3-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="067c3-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="067c3-129">Power Query</span></span>

<span data-ttu-id="067c3-130">Þú verður að nota Microsoft Power Query fyrir Excel í sniðmáti fyrir áætlaðan tíma verks til að ljúka þessum verkefnum:</span><span class="sxs-lookup"><span data-stu-id="067c3-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="067c3-131">Settu á sjálfgefið kenni spárlíkans sem verður notað þegar samþættingin býr til nýja tímaspá.</span><span class="sxs-lookup"><span data-stu-id="067c3-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="067c3-132">Síaðu út allar sértækar færslur tilfanga í verkinu sem munu ekki standast samþættinguna í tímaspár.</span><span class="sxs-lookup"><span data-stu-id="067c3-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="067c3-133">Síaðu út allar auðar línur færsluflokks.</span><span class="sxs-lookup"><span data-stu-id="067c3-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="067c3-134">Ef ekki tekst að ljúka þessu verki getur það leitt til rangra tímaspáa.</span><span class="sxs-lookup"><span data-stu-id="067c3-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="067c3-135">Settu á sjálfgefið spárlíkanskenni</span><span class="sxs-lookup"><span data-stu-id="067c3-135">Set the default forecast model ID</span></span>

<span data-ttu-id="067c3-136">Til að uppfæra sjálfgefið spárlíkanskenni í sniðmátinu skal smella á örina **Varpa** til að opna vörpunina.</span><span class="sxs-lookup"><span data-stu-id="067c3-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="067c3-137">Veldu síðan tengilinn **Ítarleg fyrirspurn og síun**.</span><span class="sxs-lookup"><span data-stu-id="067c3-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="067c3-138">Ef þú notar sniðmát fyrir sjálfgefnar tímaáætlanir verks (PSA til Fin and Ops) skaltu velja **Innslegið skilyrði** í listanum yfir **Notuð skref**.</span><span class="sxs-lookup"><span data-stu-id="067c3-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="067c3-139">Í færslunni **Aðgerð** skaltu skipta út **O\_forecast** fyrir heitið á spárlíkanskenni sem ætti að nota með samþættingunni.</span><span class="sxs-lookup"><span data-stu-id="067c3-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="067c3-140">Sjálfgefið sniðmát er með spárlíkanskenni frá sýnigögnunum.</span><span class="sxs-lookup"><span data-stu-id="067c3-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="067c3-141">Ef þú ert að búa til nýtt sniðmát þarftu að bæta við þessum dálki.</span><span class="sxs-lookup"><span data-stu-id="067c3-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="067c3-142">Veldu **Bæta við skilyrtum dálki** í Power Query og gefðu nýja dálknum heiti á borð við **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="067c3-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="067c3-143">Sláðu inn skilyrði fyrir dálkinn þar sem ef verkefni verks er ekki núll, þá \<sláðu inn spárlíkanskennið\>; annars núll.</span><span class="sxs-lookup"><span data-stu-id="067c3-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="067c3-144">Sía út sértækar færslur tilfangs</span><span class="sxs-lookup"><span data-stu-id="067c3-144">Filter out resource-specific records</span></span>

<span data-ttu-id="067c3-145">Sniðmát fyrir tímaáætlanir verks (PSA til Fin and Ops) hefur sjálfgefna síu sem fjarlægir allar sértækar færslur tilfangs.</span><span class="sxs-lookup"><span data-stu-id="067c3-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="067c3-146">Ef þú býrð til þitt eigið sniðmát þarftu að bæta við þessari síu.</span><span class="sxs-lookup"><span data-stu-id="067c3-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="067c3-147">Veldu tengilinn **Ítarleg fyrirspurn og síun** til að sía dálkinn **msdyn\_islinetask** þannig að aðeins **Rangar** færslur eru hafðar með.</span><span class="sxs-lookup"><span data-stu-id="067c3-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="067c3-148">Síaðu út auðar línur færsluflokks</span><span class="sxs-lookup"><span data-stu-id="067c3-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="067c3-149">Þú verður að bæta við síu til að fjarlægja allar línur sem eru með tómum færsluflokkum.</span><span class="sxs-lookup"><span data-stu-id="067c3-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="067c3-150">Þetta verkefni er nauðsynlegt óháð því hvort þú notir sjálfgefið sniðmát eða býrð til þitt eigið sniðmát.</span><span class="sxs-lookup"><span data-stu-id="067c3-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="067c3-151">Þessi sía fjarlægir allar samantektarlínur frá Project Service Automation sem gætu valdið því að tímaspár í Finance verði rangar.</span><span class="sxs-lookup"><span data-stu-id="067c3-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="067c3-152">Veldu tengilinn **Ítarleg fyrirspurn og síun** til að sía út núllfærslur í dálknum **msdyn\_færsluflokks\_gildi**.</span><span class="sxs-lookup"><span data-stu-id="067c3-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="067c3-153">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="067c3-153">Template mapping in Data integration</span></span>

<span data-ttu-id="067c3-154">Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="067c3-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="067c3-155">Vörpunin sýnir reitaupplýsingarnar sem verða samstilltar frá Project Service Automation við Finance.</span><span class="sxs-lookup"><span data-stu-id="067c3-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="067c3-156">[![Kortlagning sniðmáts](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="067c3-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="067c3-157">Kostnaðaráætlanir verks</span><span class="sxs-lookup"><span data-stu-id="067c3-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="067c3-158">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="067c3-158">Template and tasks</span></span>

<span data-ttu-id="067c3-159">Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla áætlaðan kostnað verks frá Project Service Automation við Finance:</span><span class="sxs-lookup"><span data-stu-id="067c3-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="067c3-160">**Heiti sniðmátsins í gagnasamþættingu:** Kostnaðaráætlanir verks (PSA til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="067c3-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="067c3-161">**Heiti verkefna í verkinu:**</span><span class="sxs-lookup"><span data-stu-id="067c3-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="067c3-162">Færslutengsl</span><span class="sxs-lookup"><span data-stu-id="067c3-162">Transaction relationships</span></span> 
    - <span data-ttu-id="067c3-163">Kostnaðaráætlanir</span><span class="sxs-lookup"><span data-stu-id="067c3-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="067c3-164">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="067c3-164">Entity set</span></span>

| <span data-ttu-id="067c3-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="067c3-165">Project Service Automation</span></span> | <span data-ttu-id="067c3-166">Fjármál</span><span class="sxs-lookup"><span data-stu-id="067c3-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="067c3-167">Færslutengingar</span><span class="sxs-lookup"><span data-stu-id="067c3-167">Transaction Connections</span></span>    | <span data-ttu-id="067c3-168">Samþættingareining fyrir vensl verkfærsla</span><span class="sxs-lookup"><span data-stu-id="067c3-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="067c3-169">Meta línur</span><span class="sxs-lookup"><span data-stu-id="067c3-169">Estimate Lines</span></span>             | <span data-ttu-id="067c3-170">Samþættingareining fyrir áætlaðan verkkostnað</span><span class="sxs-lookup"><span data-stu-id="067c3-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="067c3-171">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="067c3-171">Entity flow</span></span>

<span data-ttu-id="067c3-172">Kostnaðaráætlunum verks er stjórnað í Project Service Automation og þær eru samstilltar við Finance sem kostnaðarspár verks.</span><span class="sxs-lookup"><span data-stu-id="067c3-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="067c3-173">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="067c3-173">Prerequisites</span></span>

<span data-ttu-id="067c3-174">Áður en samstilling á kostnaðaráætlunum verks getur átt sér stað verður þú að samstilla flokka fyrir verk, verkefni verks og kostnaðarfærslur verks.</span><span class="sxs-lookup"><span data-stu-id="067c3-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="067c3-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="067c3-175">Power Query</span></span>

<span data-ttu-id="067c3-176">Þú verður að nota Power Query í sniðmáti fyrir kostnaðaráætlanir verks til að ljúka þessum verkefnum:</span><span class="sxs-lookup"><span data-stu-id="067c3-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="067c3-177">Sía til að innihalda aðeins færslulínur kostnaðaráætlunar.</span><span class="sxs-lookup"><span data-stu-id="067c3-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="067c3-178">Settu á sjálfgefið kenni spárlíkans sem verður notað þegar samþættingin býr til nýja tímaspá.</span><span class="sxs-lookup"><span data-stu-id="067c3-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="067c3-179">Umbreyta reikningsgerðunum.</span><span class="sxs-lookup"><span data-stu-id="067c3-179">Transform the billing types.</span></span>
- <span data-ttu-id="067c3-180">Umbreyta færslugerðunum.</span><span class="sxs-lookup"><span data-stu-id="067c3-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="067c3-181">Sía til að innihalda aðeins línur kostnaðaráætlunar</span><span class="sxs-lookup"><span data-stu-id="067c3-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="067c3-182">Sniðmát fyrir kostnaðaráætlanir verks (PSA til Fin and Ops) hefur sjálfgefna síu sem inniheldur aðeins kostnaðarlínur í samþættingunni.</span><span class="sxs-lookup"><span data-stu-id="067c3-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="067c3-183">Ef þú býrð til þitt eigið sniðmát þarftu að bæta við þessari síu.</span><span class="sxs-lookup"><span data-stu-id="067c3-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="067c3-184">Veldu verkefnið **Færslutengsl** og smelltu síðan á örina **Varpa** til að opna vörpunina.</span><span class="sxs-lookup"><span data-stu-id="067c3-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="067c3-185">Veldu tengilinn **Ítarleg fyrirspurn og síun**.</span><span class="sxs-lookup"><span data-stu-id="067c3-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="067c3-186">Síaðu dálkinn **msdyn\_transactiontype1** þannig að hann innihaldi aðeins **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="067c3-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="067c3-187">Settu á sjálfgefið spárlíkanskenni</span><span class="sxs-lookup"><span data-stu-id="067c3-187">Set the default forecast model ID</span></span>

<span data-ttu-id="067c3-188">Til að uppfæra sjálfgefið spárlíkanskenni í sniðmátinu skal velja verkefnið **Kostnaðaráætlanir** og smella síðan á örina **Varpa** til að opna vörpunina.</span><span class="sxs-lookup"><span data-stu-id="067c3-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="067c3-189">Veldu tengilinn **Ítarleg fyrirspurn og síun**.</span><span class="sxs-lookup"><span data-stu-id="067c3-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="067c3-190">Ef þú notar sniðmát fyrir sjálfgefnar kostnaðaráætlanir verks (PSA til Fin and Ops) í Power Query skaltu fyrst velja **Innslegið skilyrði** úr hlutanum **Notuð skref**.</span><span class="sxs-lookup"><span data-stu-id="067c3-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="067c3-191">Í færslunni **Aðgerð** skaltu skipta út **O\_forecast** fyrir heitið á spárlíkanskenni sem ætti að nota með samþættingunni.</span><span class="sxs-lookup"><span data-stu-id="067c3-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="067c3-192">Sjálfgefið sniðmát er með spárlíkanskenni frá sýnigögnunum.</span><span class="sxs-lookup"><span data-stu-id="067c3-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="067c3-193">Ef þú ert að búa til nýtt sniðmát þarftu að bæta við þessum dálki.</span><span class="sxs-lookup"><span data-stu-id="067c3-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="067c3-194">Veldu **Bæta við skilyrtum dálki** í Power Query og gefðu nýja dálknum heiti á borð við **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="067c3-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="067c3-195">Sláðu inn skilyrðið fyrir dálkinn þar sem ef kenni línuáætlunar er ekki núll, þá skal \<slá inn spárlíkanskennið\>; annars núll.</span><span class="sxs-lookup"><span data-stu-id="067c3-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="067c3-196">Umbryta reikningsgerðunum</span><span class="sxs-lookup"><span data-stu-id="067c3-196">Transform the billing types</span></span>

<span data-ttu-id="067c3-197">Sniðmát fyrir kostnaðaráætlanir verks (PSA til Fin and Ops) inniheldur skilyrtan dálk sem er notaður til að umbreyta reikningsgerðunum sem eru mótteknar frá Project Service Automation meðan á samþættingu stendur.</span><span class="sxs-lookup"><span data-stu-id="067c3-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="067c3-198">Ef þú býrð til þitt eigið sniðmát þarftu að bæta við þessum skilyrta dálki.</span><span class="sxs-lookup"><span data-stu-id="067c3-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="067c3-199">Veldu tengilinn **Ítarleg fyrirspurn og síun** og veldu síðan **Bæta við skilyrtum dálki**.</span><span class="sxs-lookup"><span data-stu-id="067c3-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="067c3-200">Sláðu inn heiti á nýja dálknum, t.d. **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="067c3-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="067c3-201">Sláðu síðan inn eftirfarandi skilyrði:</span><span class="sxs-lookup"><span data-stu-id="067c3-201">Then enter the following condition:</span></span>

<span data-ttu-id="067c3-202">Ef **msdyn\_billingtype** = 192350000, þá **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="067c3-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="067c3-203">annars ef **msdyn\_billingtype** = 192350001, þá **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="067c3-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="067c3-204">annars ef **msdyn\_billingtype** = 192350002, þá **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="067c3-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="067c3-205">annars **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="067c3-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="067c3-206">Umbreyta færslugerðunum</span><span class="sxs-lookup"><span data-stu-id="067c3-206">Transform the transaction types</span></span>

<span data-ttu-id="067c3-207">Sniðmát fyrir kostnaðaráætlanir verks (PSA til Fin and Ops) inniheldur skilyrtan dálk sem er notaður til að umbreyta færslugerðunum sem eru mótteknar frá Project Service Automation meðan á samþættingu stendur.</span><span class="sxs-lookup"><span data-stu-id="067c3-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="067c3-208">Ef þú býrð til þitt eigið sniðmát þarftu að bæta við þessum skilyrta dálki.</span><span class="sxs-lookup"><span data-stu-id="067c3-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="067c3-209">Veldu tengilinn **Ítarleg fyrirspurn og síun** og veldu síðan **Bæta við skilyrtum dálki**.</span><span class="sxs-lookup"><span data-stu-id="067c3-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="067c3-210">Færa inn heiti á nýja dálknum, t.d. **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="067c3-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="067c3-211">Sláðu síðan inn eftirfarandi skilyrði:</span><span class="sxs-lookup"><span data-stu-id="067c3-211">Then enter the following condition:</span></span>

<span data-ttu-id="067c3-212">Ef **msdyn\_transactiontypecode** = 192350000, þá **Kostnaður**</span><span class="sxs-lookup"><span data-stu-id="067c3-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="067c3-213">annars ef **msdyn\_transactiontypecode** = 192350005, þá **Sala**</span><span class="sxs-lookup"><span data-stu-id="067c3-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="067c3-214">annars **núll**</span><span class="sxs-lookup"><span data-stu-id="067c3-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="067c3-215">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="067c3-215">Template mapping in Data integration</span></span>

<span data-ttu-id="067c3-216">Eftirfarandi skýringarmyndir sýna dæmi um vörpunarsniðmát í gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="067c3-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="067c3-217">Vörpunin sýnir reitaupplýsingarnar sem verða samstilltar frá Project Service Automation við Finance.</span><span class="sxs-lookup"><span data-stu-id="067c3-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="067c3-218">[![Kortlagning sniðmáts](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="067c3-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="067c3-219">[![Kortlagning sniðmáts](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="067c3-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
