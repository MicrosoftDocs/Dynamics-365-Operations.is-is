---
title: "Samstilla kostnaðarflokka verks frá Project Service Automation"
description: "Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla kostnaðarflokka verks milli Microsoft Dynamics 365 for Finance and Operations og Dynamics 365 for Project Service Automation."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: is-is
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="a3231-103">Samstilla kostnaðarflokka verks milli Finance and Operations og Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a3231-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

<span data-ttu-id="a3231-104">Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla kostnaðarflokka verks milli Microsoft Dynamics 365 for Finance and Operations og Dynamics 365 for Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a3231-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Microsoft Dynamics 365 for Finance and Operations and Dynamics 365 for Project Service Automation.</span></span>

> [!NOTE]
> <span data-ttu-id="a3231-105">Samþætting verkefna fyrir verk, flokkar kostnaðarfærslna, áætlaður tími, kostnaðaráætlun og virknilæsing er í boði í Dynamics 365 for Finance and Operations útgáfu 8.0.</span><span class="sxs-lookup"><span data-stu-id="a3231-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a><span data-ttu-id="a3231-106">Gagnaflæði fyrir Project Service Automation og Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a3231-106">Data flow for Project Service Automation and Finance and Operations</span></span>

<span data-ttu-id="a3231-107">Samþættingarlausn Project Service Automation og Finance and Operations notar eiginleika gagnasamþættingar til að samstilla gögn þvert yfir tilvik af Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a3231-107">The Project Service Automation and Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="a3231-108">Samþættingarsniðmátin sem eru tiltæk með eiginleika gagnasamþættingar gera gögnum kleift að flæða umi kostnaðarfærsluflokka verks milli Finance and Operations og Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a3231-108">The integration templates that are available with the Data integration feature enables the flow of data about project expense transaction categories between Finance and Operations and Project Service Automation.</span></span>

<span data-ttu-id="a3231-109">Ef kostnaðarflokkar verks eru "mastered" í Finance and Operations er samþættingarflæðið fyrst frá Finance and Operations til Project Service Automation og síðan uppfærsla á samþættingum auðkenna fyrir kostnaðarflokka verks með því að samstilla frá Project Service Automation við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a3231-109">If the project expense categories are mastered in Finance and Operations, the integration flow is first from Finance and Operations to Project Service Automation, and then updating the project expense categories integration IDs by synchronizing from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="a3231-110">Ef kostnaðarflokkar verks eru "mastered" í Project Service Automation er samþættingarflæðið fyrst frá Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a3231-110">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="a3231-111">Verkflokkarnir verða þegar að vera skilgreindir í Finance and Operations fyrir samstillingu frá Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a3231-111">The project categories must already be configured in Finance and Operations prior to the synchronization from Project Service Automation.</span></span> <span data-ttu-id="a3231-112">Síðan skal samtilla frá Finance and Operations og baka til Project Service Automation og síðan frá Project Service Automation til Finance and Operations aftur.</span><span class="sxs-lookup"><span data-stu-id="a3231-112">Then synchronize from Finance and Operations back to Project Service Automation and then from Project Service Automation to Finance and Operations again.</span></span> <span data-ttu-id="a3231-113">Þetta tryggir að flokkarnir séu tengdir og afrit eru ekki búin til.</span><span class="sxs-lookup"><span data-stu-id="a3231-113">This ensures the categories are linked and duplicates are not created.</span></span>

> [!NOTE]
> <span data-ttu-id="a3231-114">Venjulega verða kostnaðarflokkar verks "mastered" í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a3231-114">Typically, the project expense categories will be mastered in Finance and Operations.</span></span> <span data-ttu-id="a3231-115">Ef þetta eru ekki þínar kringumstæður eða þú ert þegar með kostnaðarflokka stofnaða í Project Service Automation verður þú fyrst að samstilla með því að nota kostnaðarfærsluflokka verks (PSA til Fin and Ops) og þá samstilla með kostnaðarfærsluflokka verks (Fin og Ops til PSA).</span><span class="sxs-lookup"><span data-stu-id="a3231-115">If that is not your situation, or you already have expense categories created in Project Service Automation, you must first sync using the Project expense transaction categories (PSA to Fin and Ops) and then sync using Project expense transaction categories (Fin and Ops to PSA).</span></span> <span data-ttu-id="a3231-116">Þú ættir síðan að keyra samstillingu frá PSA til Fin and Ops einu sinni enn.</span><span class="sxs-lookup"><span data-stu-id="a3231-116">You should then run the sync from PSA to Fin and Ops one more time.</span></span>

> <span data-ttu-id="a3231-117">Ef fyrst er samstillt frá Project Service Automation verða verkflokkarnir að vera þegar uppsettir í Finance and Operations og allir verkflokkar sem þarf að samstilla við kostnaðarfærslur Project Service Automation verða að vera settir upp til að vera **Virkt í færslubókum**.</span><span class="sxs-lookup"><span data-stu-id="a3231-117">If synchronizing first from Project Service Automation, the project categories must already be set up in Finance and Operations and any project categories that need to be synched with the Project Service Automation transaction categories must be set up to be **Active in journals**.</span></span>

<span data-ttu-id="a3231-118">Eftirfarandi skýringarmynd sýnir hvernig gögnin eru samstillt milli Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a3231-118">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="a3231-119">[![Gagnaflæði fyrir samþættingu Project Service Automation við Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="a3231-119">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>


## <a name="templates-and-tasks"></a><span data-ttu-id="a3231-120">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="a3231-120">Templates and tasks</span></span>

<span data-ttu-id="a3231-121">Til að fá aðgang að tiltæku sniðmátunum, í stjórnendamiðstöð Microsoft PowerApps, skal velja **Verk** og síðan í efra hægra horninu skal velja **Nýtt verk** til að velja almenn sniðmát.</span><span class="sxs-lookup"><span data-stu-id="a3231-121">To access available templates, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="a3231-122">Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla kostnaðarflokka verks frá Finance and Operations til Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="a3231-122">The following template and underlying task is used to synchronize project expense categories from Finance and Operations to Project Service Automation:</span></span>

-  <span data-ttu-id="a3231-123">**Heiti sniðmátsins í gagnasamþættingu:** Kostnaðarfærsluflokkar verks (Fin Ops til PSA)</span><span class="sxs-lookup"><span data-stu-id="a3231-123">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
-  <span data-ttu-id="a3231-124">**Heiti verkefnis í verkinu:** Samstilla flokka við PSA</span><span class="sxs-lookup"><span data-stu-id="a3231-124">**Name of the task in the project:** Sync categories to PSA</span></span>

## <a name="entity-set"></a><span data-ttu-id="a3231-125">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="a3231-125">Entity set</span></span>

| <span data-ttu-id="a3231-126">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a3231-126">Finance and Operations</span></span>               | <span data-ttu-id="a3231-127">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a3231-127">Project Service Automation</span></span>    |
|--------------------------------------|-------------------------------|
| <span data-ttu-id="a3231-128">Samþættingareining fyrir flokka</span><span class="sxs-lookup"><span data-stu-id="a3231-128">Integration entity for categories</span></span>    | <span data-ttu-id="a3231-129">Færsluflokkar</span><span class="sxs-lookup"><span data-stu-id="a3231-129">Transaction categories</span></span>        |

## <a name="entity-flow"></a><span data-ttu-id="a3231-130">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="a3231-130">Entity flow</span></span>

<span data-ttu-id="a3231-131">Kostnaðarflokkum verks er stjórnað í Finance and Operations og þeir eru samstilltir við Project Service Automation sem færsluflokkar.</span><span class="sxs-lookup"><span data-stu-id="a3231-131">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span>

## <a name="power-query"></a><span data-ttu-id="a3231-132">Power Query</span><span class="sxs-lookup"><span data-stu-id="a3231-132">Power Query</span></span>

<span data-ttu-id="a3231-133">Þú verður að nota Microsoft Power Query til að stilla reikningsgerðina á færsluflokknum þegar samstillt er við Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a3231-133">You must use Microsoft Power Query to set the billing type on the transaction category when synchronizing to Project Service Automation.</span></span> <span data-ttu-id="a3231-134">Sniðmát kostnaðarfærsluflokka verks (Fin and Ops til PSA) hefur sjálfgefinn dálk og vörpun sem þegar hefur verið veitt.</span><span class="sxs-lookup"><span data-stu-id="a3231-134">The Project expense transaction categories (Fin and Ops to PSA) template has a default column and mapping already provided.</span></span> <span data-ttu-id="a3231-135">Ef þú býrð til þitt eigið sniðmát þarftu að bæta við skilyrtum dálki í Power Query.</span><span class="sxs-lookup"><span data-stu-id="a3231-135">If you create your own template, you must add a conditional column in Power Query.</span></span>
- <span data-ttu-id="a3231-136">Opnaðu snið Advance Query and Filtering innan vörpunar á verkefni fyrir kostnaðarflokka verks.</span><span class="sxs-lookup"><span data-stu-id="a3231-136">Open the Advance Query and Filtering form from within the mapping of project expense categories task.</span></span>
- <span data-ttu-id="a3231-137">Veldu **Bæta við skilyrtum dálki**.</span><span class="sxs-lookup"><span data-stu-id="a3231-137">Select **Add Conditional Column**.</span></span>
- <span data-ttu-id="a3231-138">Gefðu nýja dálkinum heiti á borð við BillingType.</span><span class="sxs-lookup"><span data-stu-id="a3231-138">Give the new column a name, such as BillingType.</span></span>
- <span data-ttu-id="a3231-139">Sláðu inn eftirfarandi skilyrði: ef **CATEGORYID er ekki jafnt og núll þá 19235001, annars núll**.</span><span class="sxs-lookup"><span data-stu-id="a3231-139">Enter the following condition: if **CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
- <span data-ttu-id="a3231-140">Smelltu á **Í lagi** í dálkinum.</span><span class="sxs-lookup"><span data-stu-id="a3231-140">Click **OK** on the column.</span></span>
- <span data-ttu-id="a3231-141">Vertu viss um að varpa þessum nýja dálki á vörpunarsíðunni.</span><span class="sxs-lookup"><span data-stu-id="a3231-141">Be sure to map this new column in the mapping page.</span></span>

<span data-ttu-id="a3231-142">Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="a3231-142">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="a3231-143">Vörpunin sýnir reitaupplýsingarnar sem verða samstilltar frá Finance and Operations við Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a3231-143">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="a3231-144">[![Kortlagning sniðmáts](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="a3231-144">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

<span data-ttu-id="a3231-145">Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla kostnaðarflokka verks frá Project Service Automation til Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="a3231-145">The following template and underlying task is used to synchronize project expense categories from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="a3231-146">-**Heiti sniðmátsins í gagnasamþættingu:** Kostnaðarfærsluflokkar verks (PSA til Fin and Ops) -**Heiti verkefnis í verkinu:** Samstilla flokka við Fin Ops</span><span class="sxs-lookup"><span data-stu-id="a3231-146">-**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops) -**Name of the task in the project:** Sync categories to Fin Ops</span></span>

## <a name="entity-set"></a><span data-ttu-id="a3231-147">Einingastamstæða</span><span class="sxs-lookup"><span data-stu-id="a3231-147">Entity set</span></span>

| <span data-ttu-id="a3231-148">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a3231-148">Project Service Automation</span></span>      | <span data-ttu-id="a3231-149">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a3231-149">Finance and Operations</span></span>             |
|---------------------------------|------------------------------------|
| <span data-ttu-id="a3231-150">Færsluflokkar</span><span class="sxs-lookup"><span data-stu-id="a3231-150">Transaction categories</span></span>          | <span data-ttu-id="a3231-151">Samþættingareining fyrir flokka</span><span class="sxs-lookup"><span data-stu-id="a3231-151">Integration entity for categories</span></span>  | 

## <a name="entity-flow"></a><span data-ttu-id="a3231-152">Einingaflæði</span><span class="sxs-lookup"><span data-stu-id="a3231-152">Entity flow</span></span>

<span data-ttu-id="a3231-153">Kostnaðarflokkum verks er stjórnað í Finance and Operations og þeir eru samstilltir við Project Service Automation sem færsluflokkar.</span><span class="sxs-lookup"><span data-stu-id="a3231-153">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="a3231-154">Samstillingin til baka við Finance and Operations uppfærir auðkenni samþættingarinnar frá Project Service Automation í verkflokki Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a3231-154">The synchronization back to Finance and Operations updates the integration ID from Project Service Automation on the Finance and Operations project category.</span></span>

<span data-ttu-id="a3231-155">Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="a3231-155">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="a3231-156">Vörpunin sýnir reitaupplýsingarnar sem verða samstilltar frá Project Service Automation við Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a3231-156">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="a3231-157">[![Kortlagning sniðmáts](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="a3231-157">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>

