---
title: Samstilla verkáætlanir beint frá Project Service Automation við Finance and Operations
description: Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla tímaáætlun verks og kostnaðaráætlun verks beint frá Microsoft Dynamics 365 for Project Service Automation til Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 21338b889e0377dbfd5adfd461ea81b39a75baf8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556553"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="f6451-103">Samstilla verkáætlanir beint frá Project Service Automation við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f6451-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f6451-104">Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla tímaáætlun verks og kostnaðaráætlun verks beint frá Microsoft Dynamics 365 for Project Service Automation til Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f6451-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="f6451-105">Samþætting verkefna fyrir verk, flokkar kostnaðarfærslna, áætlaður tími, kostnaðaráætlun og virknilæsing er í boði í Microsoft Dynamics 365 for Finance and Operations útgáfu 8.0.</span><span class="sxs-lookup"><span data-stu-id="f6451-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="f6451-106">Samþætting á rauntölum er í boði í Microsoft Dynamics 365 for Finance and Operations útgáfu 8.0.1 eða nýrri.</span><span class="sxs-lookup"><span data-stu-id="f6451-106">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>
> - <span data-ttu-id="f6451-107">Ef þú notar Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0, eftir að hafa sett upp KB 4132657 og KB 4132660 getur þú notað sniðmátin til að samþætta verkefni fyrir verk, kostnaðarfærsluflokka, tímaáætlanir, kostnaðaráætlanir og rauntölur og til að stilla virknilæsingu.</span><span class="sxs-lookup"><span data-stu-id="f6451-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="f6451-108">Ef þú verður að endurstilla dreifingu á fjárhagsupphæð mælum við með að þú setjir einnig upp KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="f6451-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="f6451-109">Gagnaflæði fyrir Project Service Automation til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f6451-109">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="f6451-110">Samþættingarlausn Project Service Automation við Finance and Operations notar eiginleika gagnasamþættingar til að samstilla gögn þvert yfir tilvik af Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f6451-110">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="f6451-111">Samþættingarsniðmátin sem eru tiltæk með eiginleika gagnasamþættingar gera gögnum kleift að flæða varðandi áætlaðan tíma verks og kostnaðarmat verks frá Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f6451-111">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="f6451-112">Eftirfarandi skýringarmynd sýnir hvernig gögnin eru samstillt milli Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f6451-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="f6451-113">[![Gagnaflæði fyrir samþættingu Project Service Automation við Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="f6451-113">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="f6451-114">Áætlaðar verkstundir</span><span class="sxs-lookup"><span data-stu-id="f6451-114">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="f6451-115">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="f6451-115">Template and tasks</span></span>

<span data-ttu-id="f6451-116">Til að fá aðgang að tiltækum sniðmátum, í stjórnendamiðstöð Microsoft PowerApps, skal velja **Verk** og síðan í efra hægra horninu skal velja **Nýtt verk** til að velja almenn sniðmát.</span><span class="sxs-lookup"><span data-stu-id="f6451-116">To access the available templates, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="f6451-117">Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla áætlaðan tíma verks frá Project Service Automation við Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="f6451-117">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="f6451-118">**Heiti sniðmátsins í gagnasamþættingu:** Áætlaður tími verks (PSA til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="f6451-118">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="f6451-119">**Heiti verkefna í verkinu:**</span><span class="sxs-lookup"><span data-stu-id="f6451-119">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="f6451-120">Færslutengsl</span><span class="sxs-lookup"><span data-stu-id="f6451-120">Transaction relationships</span></span>
    - <span data-ttu-id="f6451-121">Kostnaðaráætlanir</span><span class="sxs-lookup"><span data-stu-id="f6451-121">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="f6451-122">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="f6451-122">Entity set</span></span>

| <span data-ttu-id="f6451-123">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f6451-123">Project Service Automation</span></span> | <span data-ttu-id="f6451-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f6451-124">Finance and Operations</span></span>                        |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="f6451-125">Verkefni</span><span class="sxs-lookup"><span data-stu-id="f6451-125">Project tasks</span></span>              | <span data-ttu-id="f6451-126">Samþættingareining fyrir áætlaðar verkstundir</span><span class="sxs-lookup"><span data-stu-id="f6451-126">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="f6451-127">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="f6451-127">Entity flow</span></span>

<span data-ttu-id="f6451-128">Áætluðum tíma verks er stjórnað í Project Service Automation og hann er samstilltur við Finance and Operations sem tímaspá verks.</span><span class="sxs-lookup"><span data-stu-id="f6451-128">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance and Operations as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="f6451-129">Frumskilyrði</span><span class="sxs-lookup"><span data-stu-id="f6451-129">Prerequisites</span></span>

<span data-ttu-id="f6451-130">Áður en samstilling á áætluðum tíma verks getur átt sér stað verður þú að samstilla flokka fyrir verk, verkefni verks og kostnaðarfærslur verks.</span><span class="sxs-lookup"><span data-stu-id="f6451-130">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="f6451-131">Power Query</span><span class="sxs-lookup"><span data-stu-id="f6451-131">Power Query</span></span>

<span data-ttu-id="f6451-132">Þú verður að nota Microsoft Power Query fyrir Excel í sniðmáti fyrir áætlaðan tíma verks til að ljúka þessum verkefnum:</span><span class="sxs-lookup"><span data-stu-id="f6451-132">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="f6451-133">Settu á sjálfgefið kenni spárlíkans sem verður notað þegar samþættingin býr til nýja tímaspá.</span><span class="sxs-lookup"><span data-stu-id="f6451-133">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="f6451-134">Síaðu út allar sértækar færslur tilfanga í verkinu sem munu ekki standast samþættinguna í tímaspár.</span><span class="sxs-lookup"><span data-stu-id="f6451-134">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="f6451-135">Síaðu út allar auðar línur færsluflokks.</span><span class="sxs-lookup"><span data-stu-id="f6451-135">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="f6451-136">Ef ekki tekst að ljúka þessu verki getur það leitt til rangra tímaspáa.</span><span class="sxs-lookup"><span data-stu-id="f6451-136">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="f6451-137">Settu á sjálfgefið spárlíkanskenni</span><span class="sxs-lookup"><span data-stu-id="f6451-137">Set the default forecast model ID</span></span>

<span data-ttu-id="f6451-138">Til að uppfæra sjálfgefið spárlíkanskenni í sniðmátinu skal smella á örina **Varpa** til að opna vörpunina.</span><span class="sxs-lookup"><span data-stu-id="f6451-138">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="f6451-139">Veldu síðan tengilinn **Ítarleg fyrirspurn og síun**.</span><span class="sxs-lookup"><span data-stu-id="f6451-139">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="f6451-140">Ef þú notar sniðmát fyrir sjálfgefnar tímaáætlanir verks (PSA til Fin and Ops) skaltu velja **Innslegið skilyrði** í listanum yfir **Notuð skref**.</span><span class="sxs-lookup"><span data-stu-id="f6451-140">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="f6451-141">Í færslunni **Aðgerð** skaltu skipta út **O\_forecast** fyrir heitið á spárlíkanskenni sem ætti að nota með samþættingunni.</span><span class="sxs-lookup"><span data-stu-id="f6451-141">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="f6451-142">Sjálfgefið sniðmát er með spárlíkanskenni frá sýnigögnunum.</span><span class="sxs-lookup"><span data-stu-id="f6451-142">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="f6451-143">Ef þú ert að búa til nýtt sniðmát þarftu að bæta við þessum dálki.</span><span class="sxs-lookup"><span data-stu-id="f6451-143">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="f6451-144">Veldu **Bæta við skilyrtum dálki** í Power Query og gefðu nýja dálknum heiti á borð við **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="f6451-144">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="f6451-145">Sláðu inn skilyrði fyrir dálkinn þar sem ef verkefni verks er ekki núll, þá \<sláðu inn spárlíkanskennið\>; annars núll.</span><span class="sxs-lookup"><span data-stu-id="f6451-145">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="f6451-146">Sía út sértækar færslur tilfangs</span><span class="sxs-lookup"><span data-stu-id="f6451-146">Filter out resource-specific records</span></span>

<span data-ttu-id="f6451-147">Sniðmát fyrir tímaáætlanir verks (PSA til Fin and Ops) hefur sjálfgefna síu sem fjarlægir allar sértækar færslur tilfangs.</span><span class="sxs-lookup"><span data-stu-id="f6451-147">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="f6451-148">Ef þú býrð til þitt eigið sniðmát þarftu að bæta við þessari síu.</span><span class="sxs-lookup"><span data-stu-id="f6451-148">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="f6451-149">Veldu tengilinn **Ítarleg fyrirspurn og síun** til að sía dálkinn **msdyn\_islinetask** þannig að aðeins **Rangar** færslur eru hafðar með.</span><span class="sxs-lookup"><span data-stu-id="f6451-149">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="f6451-150">Síaðu út auðar línur færsluflokks</span><span class="sxs-lookup"><span data-stu-id="f6451-150">Filter out empty transaction category rows</span></span>

<span data-ttu-id="f6451-151">Þú verður að bæta við síu til að fjarlægja allar línur sem eru með tómum færsluflokkum.</span><span class="sxs-lookup"><span data-stu-id="f6451-151">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="f6451-152">Þetta verkefni er nauðsynlegt óháð því hvort þú notir sjálfgefið sniðmát eða býrð til þitt eigið sniðmát.</span><span class="sxs-lookup"><span data-stu-id="f6451-152">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="f6451-153">Þessi sía fjarlægir allar samantektarlínur frá Project Service Automation sem gætu valdið því að tímaspár í Finance and Operations verði rangar.</span><span class="sxs-lookup"><span data-stu-id="f6451-153">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance and Operations to be incorrect.</span></span> <span data-ttu-id="f6451-154">Veldu tengilinn **Ítarleg fyrirspurn og síun** til að sía út núllfærslur í dálknum **msdyn\_færsluflokks\_gildi**.</span><span class="sxs-lookup"><span data-stu-id="f6451-154">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="f6451-155">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="f6451-155">Template mapping in Data integration</span></span>

<span data-ttu-id="f6451-156">Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="f6451-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="f6451-157">Vörpunin sýnir reitaupplýsingarnar sem verða samstilltar frá Project Service Automation við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f6451-157">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="f6451-158">[![Kortlagning sniðmáts](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="f6451-158">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="f6451-159">Kostnaðaráætlanir verks</span><span class="sxs-lookup"><span data-stu-id="f6451-159">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="f6451-160">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="f6451-160">Template and tasks</span></span>

<span data-ttu-id="f6451-161">Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla áætlaðan kostnað verks frá Project Service Automation við Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="f6451-161">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="f6451-162">**Heiti sniðmátsins í gagnasamþættingu:** Kostnaðaráætlanir verks (PSA til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="f6451-162">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="f6451-163">**Heiti verkefna í verkinu:**</span><span class="sxs-lookup"><span data-stu-id="f6451-163">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="f6451-164">Færslutengsl</span><span class="sxs-lookup"><span data-stu-id="f6451-164">Transaction relationships</span></span> 
    - <span data-ttu-id="f6451-165">Kostnaðaráætlanir</span><span class="sxs-lookup"><span data-stu-id="f6451-165">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="f6451-166">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="f6451-166">Entity set</span></span>

| <span data-ttu-id="f6451-167">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f6451-167">Project Service Automation</span></span> | <span data-ttu-id="f6451-168">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f6451-168">Finance and Operations</span></span>                                   |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="f6451-169">Færslutengingar</span><span class="sxs-lookup"><span data-stu-id="f6451-169">Transaction Connections</span></span>    | <span data-ttu-id="f6451-170">Samþættingareining fyrir vensl verkfærsla</span><span class="sxs-lookup"><span data-stu-id="f6451-170">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="f6451-171">Meta línur</span><span class="sxs-lookup"><span data-stu-id="f6451-171">Estimate Lines</span></span>             | <span data-ttu-id="f6451-172">Samþættingareining fyrir áætlaðan verkkostnað</span><span class="sxs-lookup"><span data-stu-id="f6451-172">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="f6451-173">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="f6451-173">Entity flow</span></span>

<span data-ttu-id="f6451-174">Kostnaðaráætlunum verks er stjórnað í Project Service Automation og þær eru samstilltar við Finance and Operations sem kostnaðarspár verks.</span><span class="sxs-lookup"><span data-stu-id="f6451-174">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance and Operations as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="f6451-175">Frumskilyrði</span><span class="sxs-lookup"><span data-stu-id="f6451-175">Prerequisites</span></span>

<span data-ttu-id="f6451-176">Áður en samstilling á kostnaðaráætlunum verks getur átt sér stað verður þú að samstilla flokka fyrir verk, verkefni verks og kostnaðarfærslur verks.</span><span class="sxs-lookup"><span data-stu-id="f6451-176">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="f6451-177">Power Query</span><span class="sxs-lookup"><span data-stu-id="f6451-177">Power Query</span></span>

<span data-ttu-id="f6451-178">Þú verður að nota Power Query í sniðmáti fyrir kostnaðaráætlanir verks til að ljúka þessum verkefnum:</span><span class="sxs-lookup"><span data-stu-id="f6451-178">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="f6451-179">Sía til að innihalda aðeins færslulínur kostnaðaráætlunar.</span><span class="sxs-lookup"><span data-stu-id="f6451-179">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="f6451-180">Settu á sjálfgefið kenni spárlíkans sem verður notað þegar samþættingin býr til nýja tímaspá.</span><span class="sxs-lookup"><span data-stu-id="f6451-180">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="f6451-181">Umbreyta reikningsgerðunum.</span><span class="sxs-lookup"><span data-stu-id="f6451-181">Transform the billing types.</span></span>
- <span data-ttu-id="f6451-182">Umbreyta færslugerðunum.</span><span class="sxs-lookup"><span data-stu-id="f6451-182">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="f6451-183">Sía til að innihalda aðeins línur kostnaðaráætlunar</span><span class="sxs-lookup"><span data-stu-id="f6451-183">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="f6451-184">Sniðmát fyrir kostnaðaráætlanir verks (PSA til Fin and Ops) hefur sjálfgefna síu sem inniheldur aðeins kostnaðarlínur í samþættingunni.</span><span class="sxs-lookup"><span data-stu-id="f6451-184">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="f6451-185">Ef þú býrð til þitt eigið sniðmát þarftu að bæta við þessari síu.</span><span class="sxs-lookup"><span data-stu-id="f6451-185">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="f6451-186">Veldu verkefnið **Færslutengsl** og smelltu síðan á örina **Varpa** til að opna vörpunina.</span><span class="sxs-lookup"><span data-stu-id="f6451-186">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="f6451-187">Veldu tengilinn **Ítarleg fyrirspurn og síun**.</span><span class="sxs-lookup"><span data-stu-id="f6451-187">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="f6451-188">Síaðu dálkinn **msdyn\_transactiontype1** þannig að hann innihaldi aðeins **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="f6451-188">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="f6451-189">Settu á sjálfgefið spárlíkanskenni</span><span class="sxs-lookup"><span data-stu-id="f6451-189">Set the default forecast model ID</span></span>

<span data-ttu-id="f6451-190">Til að uppfæra sjálfgefið spárlíkanskenni í sniðmátinu skal velja verkefnið **Kostnaðaráætlanir** og smella síðan á örina **Varpa** til að opna vörpunina.</span><span class="sxs-lookup"><span data-stu-id="f6451-190">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="f6451-191">Veldu tengilinn **Ítarleg fyrirspurn og síun**.</span><span class="sxs-lookup"><span data-stu-id="f6451-191">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="f6451-192">Ef þú notar sniðmát fyrir sjálfgefnar kostnaðaráætlanir verks (PSA til Fin and Ops) í Power Query skaltu fyrst velja **Innslegið skilyrði** úr hlutanum **Notuð skref**.</span><span class="sxs-lookup"><span data-stu-id="f6451-192">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="f6451-193">Í færslunni **Aðgerð** skaltu skipta út **O\_forecast** fyrir heitið á spárlíkanskenni sem ætti að nota með samþættingunni.</span><span class="sxs-lookup"><span data-stu-id="f6451-193">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="f6451-194">Sjálfgefið sniðmát er með spárlíkanskenni frá sýnigögnunum.</span><span class="sxs-lookup"><span data-stu-id="f6451-194">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="f6451-195">Ef þú ert að búa til nýtt sniðmát þarftu að bæta við þessum dálki.</span><span class="sxs-lookup"><span data-stu-id="f6451-195">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="f6451-196">Veldu **Bæta við skilyrtum dálki** í Power Query og gefðu nýja dálknum heiti á borð við **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="f6451-196">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="f6451-197">Sláðu inn skilyrðið fyrir dálkinn þar sem ef kenni línuáætlunar er ekki núll, þá skal \<slá inn spárlíkanskennið\>; annars núll.</span><span class="sxs-lookup"><span data-stu-id="f6451-197">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="f6451-198">Umbryta reikningsgerðunum</span><span class="sxs-lookup"><span data-stu-id="f6451-198">Transform the billing types</span></span>

<span data-ttu-id="f6451-199">Sniðmát fyrir kostnaðaráætlanir verks (PSA til Fin and Ops) inniheldur skilyrtan dálk sem er notaður til að umbreyta reikningsgerðunum sem eru mótteknar frá Project Service Automation meðan á samþættingu stendur.</span><span class="sxs-lookup"><span data-stu-id="f6451-199">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="f6451-200">Ef þú býrð til þitt eigið sniðmát þarftu að bæta við þessum skilyrta dálki.</span><span class="sxs-lookup"><span data-stu-id="f6451-200">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="f6451-201">Veldu tengilinn **Ítarleg fyrirspurn og síun** og veldu síðan **Bæta við skilyrtum dálki**.</span><span class="sxs-lookup"><span data-stu-id="f6451-201">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="f6451-202">Sláðu inn heiti á nýja dálknum, t.d. **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="f6451-202">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="f6451-203">Sláðu síðan inn eftirfarandi skilyrði:</span><span class="sxs-lookup"><span data-stu-id="f6451-203">Then enter the following condition:</span></span>

<span data-ttu-id="f6451-204">Ef **msdyn\_billingtype** = 192350000, þá **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="f6451-204">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="f6451-205">annars ef **msdyn\_billingtype** = 192350001, þá **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="f6451-205">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="f6451-206">annars ef **msdyn\_billingtype** = 192350002, þá **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="f6451-206">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="f6451-207">annars **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="f6451-207">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="f6451-208">Umbreyta færslugerðunum</span><span class="sxs-lookup"><span data-stu-id="f6451-208">Transform the transaction types</span></span>

<span data-ttu-id="f6451-209">Sniðmát fyrir kostnaðaráætlanir verks (PSA til Fin and Ops) inniheldur skilyrtan dálk sem er notaður til að umbreyta færslugerðunum sem eru mótteknar frá Project Service Automation meðan á samþættingu stendur.</span><span class="sxs-lookup"><span data-stu-id="f6451-209">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="f6451-210">Ef þú býrð til þitt eigið sniðmát þarftu að bæta við þessum skilyrta dálki.</span><span class="sxs-lookup"><span data-stu-id="f6451-210">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="f6451-211">Veldu tengilinn **Ítarleg fyrirspurn og síun** og veldu síðan **Bæta við skilyrtum dálki**.</span><span class="sxs-lookup"><span data-stu-id="f6451-211">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="f6451-212">Færa inn heiti á nýja dálknum, t.d. **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="f6451-212">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="f6451-213">Sláðu síðan inn eftirfarandi skilyrði:</span><span class="sxs-lookup"><span data-stu-id="f6451-213">Then enter the following condition:</span></span>

<span data-ttu-id="f6451-214">Ef **msdyn\_transactiontypecode** = 192350000, þá **Kostnaður**</span><span class="sxs-lookup"><span data-stu-id="f6451-214">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="f6451-215">annars ef **msdyn\_transactiontypecode** = 192350005, þá **Sala**</span><span class="sxs-lookup"><span data-stu-id="f6451-215">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="f6451-216">annars **núll**</span><span class="sxs-lookup"><span data-stu-id="f6451-216">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="f6451-217">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="f6451-217">Template mapping in Data integration</span></span>

<span data-ttu-id="f6451-218">Eftirfarandi skýringarmyndir sýna dæmi um vörpunarsniðmát í gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="f6451-218">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="f6451-219">Vörpunin sýnir reitaupplýsingarnar sem verða samstilltar frá Project Service Automation við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f6451-219">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="f6451-220">[![Kortlagning sniðmáts](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="f6451-220">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="f6451-221">[![Kortlagning sniðmáts](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="f6451-221">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
