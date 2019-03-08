---
title: Samstilla kostnaðarflokka verks milli Finance and Operations og Project Service Automation
description: Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla kostnaðarflokka verks milli Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: c4d09fde2cf4335553243c136590f9f3135db97a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "347837"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="a9fdf-103">Samstilla kostnaðarflokka verks milli Finance and Operations og Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a9fdf-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a9fdf-104">Þetta efnisatriði fjallar um sniðmát og undirliggjandi verkefni sem notuð eru til að samstilla kostnaðarflokka verks milli Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="a9fdf-105">Samþætting verkefna fyrir verk, flokkar kostnaðarfærslna, áætlaður tími, kostnaðaráætlun og virknilæsing eru í boði í Microsoft Dynamics 365 for Finance and Operations útgáfu 8.0.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="a9fdf-106">Samþætting á rauntölum er í boði í Microsoft Dynamics 365 for Finance and Operations útgáfu 8.0.1 eða nýrri.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-106">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>
> - <span data-ttu-id="a9fdf-107">Ef þú notar Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0, eftir að hafa sett upp KB 4132657 og KB 4132660 getur þú notað sniðmátin til að samþætta verkefni fyrir verk, kostnaðarfærsluflokka, tímaáætlanir, kostnaðaráætlanir og rauntölur og til að stilla virknilæsingu.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="a9fdf-108">Ef þú verður að endurstilla dreifingu á fjárhagsupphæð mælum við með að þú setjir einnig upp KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a><span data-ttu-id="a9fdf-109">Gagnaflæði fyrir Project Service Automation og Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a9fdf-109">Data flow for Project Service Automation and Finance and Operations</span></span>

<span data-ttu-id="a9fdf-110">Samþættingarlausn Project Service Automation og Finance and Operations notar eiginleika gagnasamþættingar til að samstilla gögn þvert yfir tilvik af Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-110">The Project Service Automation and Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="a9fdf-111">Samþættingarsniðmátin sem eru tiltæk með eiginleika gagnasamþættingar gera gögnum kleift að flæða umi kostnaðarfærsluflokka verks milli Finance and Operations og Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Operations and Project Service Automation.</span></span>

<span data-ttu-id="a9fdf-112">Ef kostnaðarflokkar verks eru „mastered“ í Finance and Operations er samþættingarflæðið fyrst frá Finance and Operations til Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-112">If the project expense categories are mastered in Finance and Operations, the integration flow is first from Finance and Operations to Project Service Automation.</span></span> <span data-ttu-id="a9fdf-113">Ef samþættingarkenni kostnaðarflokka verks eru síðan uppfærðir með samstillingu frá Project Service Automation í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="a9fdf-114">Ef kostnaðarflokkar verks eru "mastered" í Project Service Automation er samþættingarflæðið fyrst frá Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="a9fdf-115">Verkflokkarnir verða þegar að vera skilgreindir í Finance and Operations fyrir samstillingu frá Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-115">The project categories must already be configured in Finance and Operations before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="a9fdf-116">Síðan skal samtilla frá Finance and Operations og baka til Project Service Automation og síðan frá Project Service Automation til Finance and Operations aftur.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-116">Then synchronize from Finance and Operations back to Project Service Automation, and then from Project Service Automation to Finance and Operations again.</span></span> <span data-ttu-id="a9fdf-117">Þannig hjálpar þú að tryggja að flokkarnir séu tengdir og að engar tvítekningar séu búnar til.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="a9fdf-118">Venjulega eru kostnaðarflokkar verks „mastered“ í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-118">Typically, the project expense categories are mastered in Finance and Operations.</span></span> <span data-ttu-id="a9fdf-119">Ef þeir eru hins vegar ekki „mastered“ í Finance and Operations eða ef kostnaðarflokkar hafa þegar verið búnir til í Project Service Automation verður þú fyrst að samstilla með því að nota sniðmát fyrir kostnaðarfærsluflokka verks (PSA til Fin og Ops).</span><span class="sxs-lookup"><span data-stu-id="a9fdf-119">However, if they aren't mastered in Finance and Operations, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="a9fdf-120">Samstilltu síðan með sniðmáti fyrir kostnaðarfærsluflokka verks (Fin and Ops til PSA).</span><span class="sxs-lookup"><span data-stu-id="a9fdf-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="a9fdf-121">Þú ættir þá að keyra samstillingu frá Project Service Automation í Finance and Operations einu sinni enn.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-121">You should then run the synchronization from Project Service Automation to Finance and Operations one more time.</span></span>
>
> <span data-ttu-id="a9fdf-122">Ef þú samstillir fyrst frá Project Service Automation verður að uppfylla eftirfarandi skilyrði í Finance and Operations áður en samstillingin er keyrð:</span><span class="sxs-lookup"><span data-stu-id="a9fdf-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance and Operations before the synchronization is run:</span></span>
>
> - <span data-ttu-id="a9fdf-123">Samnýttur flokkur sem passar við verktegundina sem er sett upp í Project Service Automation verður að vera til og hann verður að vera virkur fyrir bæði **Verk** og **Kostnað**.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="a9fdf-124">Fyrir hvern lögaðila Finance and Operations sem þarf að samþætta við, verða eftirfarandi verktegundir að vera til staðar:</span><span class="sxs-lookup"><span data-stu-id="a9fdf-124">For each Finance and Operations legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="a9fdf-125">**Verktegund** er til staðar.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="a9fdf-126">**Nota í kostnað** er virkt.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="a9fdf-127">**Virkt í færslubók** er virkt.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="a9fdf-128">**Færslugerð** er stillt á **Kostnaður**.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="a9fdf-129">Eftirfarandi skýringarmynd sýnir hvernig gögnin eru samstillt milli Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="a9fdf-130">[![Gagnaflæði fyrir samþættingu Project Service Automation við Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="a9fdf-130">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-and-operations-to-project-service-automation"></a><span data-ttu-id="a9fdf-131">Samstilling á kostnaðarflokki verks frá Finance and Operations í Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a9fdf-131">Project expense category synchronization from Finance and Operations to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="a9fdf-132">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="a9fdf-132">Template and task</span></span>

<span data-ttu-id="a9fdf-133">Til að fá aðgang að tiltækum sniðmátum, í stjórnendamiðstöð Microsoft PowerApps, skal velja **Verk** og síðan í efra hægra horninu skal velja **Nýtt verk** til að velja almenn sniðmát.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-133">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="a9fdf-134">Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla kostnaðarflokka verks frá Finance and Operations til Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="a9fdf-134">The following template and underlying task are used to synchronize project expense categories from Finance and Operations to Project Service Automation:</span></span>

- <span data-ttu-id="a9fdf-135">**Heiti sniðmátsins í gagnasamþættingu:** Kostnaðarfærsluflokkar verks (Fin Ops til PSA)</span><span class="sxs-lookup"><span data-stu-id="a9fdf-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="a9fdf-136">**Heiti verkefnis í verkinu:** Samstilla flokka við PSA</span><span class="sxs-lookup"><span data-stu-id="a9fdf-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="a9fdf-137">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="a9fdf-137">Entity set</span></span>

| <span data-ttu-id="a9fdf-138">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a9fdf-138">Finance and Operations</span></span>            | <span data-ttu-id="a9fdf-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a9fdf-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="a9fdf-140">Samþættingareining fyrir flokka</span><span class="sxs-lookup"><span data-stu-id="a9fdf-140">Integration entity for categories</span></span> | <span data-ttu-id="a9fdf-141">Færsluflokkar</span><span class="sxs-lookup"><span data-stu-id="a9fdf-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="a9fdf-142">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="a9fdf-142">Entity flow</span></span>

<span data-ttu-id="a9fdf-143">Kostnaðarflokkum verks er stjórnað í Finance and Operations og þeir eru samstilltir við Project Service Automation sem færsluflokkar.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-143">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="a9fdf-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="a9fdf-144">Power Query</span></span>

<span data-ttu-id="a9fdf-145">Þegar þú samstillir í Project Service Automation verður þú að nota Microsoft Power Query fyrir Excel til að stilla reikningsgerðina á færsluflokknum.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="a9fdf-146">Sniðmát fyrir kostnaðarfærsluflokka verks (Fin and Ops til PSA) veitir sjálfgefinn dálk og vörpun.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="a9fdf-147">Ef þú býrð til þitt eigið sniðmát þarftu að bæta við skilyrtum dálki í Power Query.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="a9fdf-148">Fylgdu eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-148">Follow these steps.</span></span>

1. <span data-ttu-id="a9fdf-149">Smelltu á örina til að opna vörpunina á verkefni fyrir kostnaðarflokka verks í sniðmáti fyrir kostnaðarfærsluflokka verks (Fin and Ops til PSA).</span><span class="sxs-lookup"><span data-stu-id="a9fdf-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="a9fdf-150">Smelltu á tengilinn **Ítarleg fyrirspurn og síun** til að opna Power Query.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="a9fdf-151">Veldu **Bæta við skilyrtum dálki**.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="a9fdf-152">Sláðu inn heiti á nýja dálknum, t.d. **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="a9fdf-153">Sláðu inn eftirfarandi skilyrði: **ef CATEGORYID er ekki jafnt og núll, þá 19235001, annars núll**.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="a9fdf-154">Smelltu á **Í lagi** í dálkinum.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="a9fdf-155">Vertu viss um að varpa þessum nýja dálki á vörpunarsíðunni.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="a9fdf-156">Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="a9fdf-157">Vörpunin sýnir reitaupplýsingarnar sem verða samstilltar frá Finance and Operations við Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-157">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="a9fdf-158">[![Kortlagning sniðmáts](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="a9fdf-158">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="a9fdf-159">Samstilling á kostnaðarflokki verks frá Project Service Automation í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a9fdf-159">Project expense category synchronization from Project Service Automation to Finance and Operations</span></span>

### <a name="template-and-task"></a><span data-ttu-id="a9fdf-160">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="a9fdf-160">Template and task</span></span>

<span data-ttu-id="a9fdf-161">Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla kostnaðarflokka verks frá Project Service Automation til Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="a9fdf-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="a9fdf-162">**Heiti sniðmátsins í gagnasamþættingu:** Kostnaðarfærsluflokkar verks (PSA til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="a9fdf-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="a9fdf-163">**Heiti verkefnis í verkinu:** Samstilla flokka við Fin Ops</span><span class="sxs-lookup"><span data-stu-id="a9fdf-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="a9fdf-164">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="a9fdf-164">Entity set</span></span>

| <span data-ttu-id="a9fdf-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a9fdf-165">Project Service Automation</span></span> | <span data-ttu-id="a9fdf-166">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a9fdf-166">Finance and Operations</span></span>            |
|----------------------------|-----------------------------------|
| <span data-ttu-id="a9fdf-167">Færsluflokkar</span><span class="sxs-lookup"><span data-stu-id="a9fdf-167">Transaction categories</span></span>     | <span data-ttu-id="a9fdf-168">Samþættingareining fyrir flokka</span><span class="sxs-lookup"><span data-stu-id="a9fdf-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="a9fdf-169">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="a9fdf-169">Entity flow</span></span>

<span data-ttu-id="a9fdf-170">Kostnaðarflokkum verks er stjórnað í Finance and Operations og þeir eru samstilltir við Project Service Automation sem færsluflokkar.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-170">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="a9fdf-171">Samstillingin til baka í Finance and Operations uppfærir verktegundina í Finance and Operations með samþættingarkennið frá Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-171">The synchronization back to Finance and Operations updates the project category in Finance and Operations with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a9fdf-172">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="a9fdf-172">Template mapping in Data integration</span></span>

<span data-ttu-id="a9fdf-173">Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="a9fdf-174">Vörpunin sýnir reitaupplýsingarnar sem verða samstilltar frá Project Service Automation við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="a9fdf-175">[![Kortlagning sniðmáts](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="a9fdf-175">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
