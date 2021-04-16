---
title: Aðgangsréttindi fyrir stjórnborð kostnaðarhluta
description: Þetta efnisatriði hefur að geyma upplýsingar um aðgangsréttindi fyrir stjórnborð kostnaðarhlutar.
author: AndersGirke
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a3639c05b24de31cfa09d2d9d0cf427122f51eae
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810199"
---
# <a name="access-rights-for-cost-object-controllers"></a><span data-ttu-id="1ce72-103">Aðgangsréttindi fyrir stjórnborð kostnaðarhluta</span><span class="sxs-lookup"><span data-stu-id="1ce72-103">Access rights for cost object controllers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ce72-104">Á vinnusvæðinu **Kostnaðarstýring** er miðpunktur þar sem stjórnendur geta skoðað afköst kostnaðarhluta sinna.</span><span class="sxs-lookup"><span data-stu-id="1ce72-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="1ce72-105">Þetta vinnusvæði gerir stjórnendum kleift að nota gögn kostnaðarbókhalds þrátt fyrir að þeir séu ekki kostnaðarbókarar.</span><span class="sxs-lookup"><span data-stu-id="1ce72-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="1ce72-106">Af öryggisástæðum ættu stjórnendur aðeins að geta séð þau gögn kostnaðarbókhalds sem tengjast þeim kostnaðarhlutum sem þeir bera ábyrgð á.</span><span class="sxs-lookup"><span data-stu-id="1ce72-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="1ce72-107">Það eru fjögur einkvæm hlutverk í kostnaðarbókhaldi.</span><span class="sxs-lookup"><span data-stu-id="1ce72-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="1ce72-108">Heiti hlutverks</span><span class="sxs-lookup"><span data-stu-id="1ce72-108">Role name</span></span>               | <span data-ttu-id="1ce72-109">Leyfi</span><span class="sxs-lookup"><span data-stu-id="1ce72-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="1ce72-110">Aðalbókari kostnaðarbókhalds</span><span class="sxs-lookup"><span data-stu-id="1ce72-110">Cost accounting manager</span></span> | <span data-ttu-id="1ce72-111">Verkþáttur</span><span class="sxs-lookup"><span data-stu-id="1ce72-111">Activity</span></span>     |
| <span data-ttu-id="1ce72-112">Kostnaðarbókari</span><span class="sxs-lookup"><span data-stu-id="1ce72-112">Cost accountant</span></span>         | <span data-ttu-id="1ce72-113">Aðgerðir</span><span class="sxs-lookup"><span data-stu-id="1ce72-113">Operations</span></span>   |
| <span data-ttu-id="1ce72-114">Starfsmaður kostnaðarbókara</span><span class="sxs-lookup"><span data-stu-id="1ce72-114">Cost accountant clerk</span></span>   | <span data-ttu-id="1ce72-115">Aðgerðir</span><span class="sxs-lookup"><span data-stu-id="1ce72-115">Operations</span></span>   |
| <span data-ttu-id="1ce72-116">Stjórnborð kostnaðarhlutar</span><span class="sxs-lookup"><span data-stu-id="1ce72-116">Cost object controller</span></span>  | <span data-ttu-id="1ce72-117">Hópmeðlimir</span><span class="sxs-lookup"><span data-stu-id="1ce72-117">Team members</span></span> |

<span data-ttu-id="1ce72-118">Í þessu efnisatriði er útskýrt hvernig á að úthluta stjórnanda hlutverkinu **Stjórnborð kostnaðarhlutar**.</span><span class="sxs-lookup"><span data-stu-id="1ce72-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="1ce72-119">Þegar hlutverkinu **Stjórnborð kostnaðarhlutar** er úthlutað stjórnanda getur hann framkvæmt eftirfarandi verkefni:</span><span class="sxs-lookup"><span data-stu-id="1ce72-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="1ce72-120">Fengið aðgang að vinnusvæðinu **Kostnaðarstýring** (í biðlaranum).</span><span class="sxs-lookup"><span data-stu-id="1ce72-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="1ce72-121">Kafað ofan í og fengið skoðunaraðgang að þeim síðum sem styðja köfun.</span><span class="sxs-lookup"><span data-stu-id="1ce72-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="1ce72-122">Fengið aðgang að vinnusvæðinu **Kostnaðarstýring** (í fartækjaforritinu).</span><span class="sxs-lookup"><span data-stu-id="1ce72-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="1ce72-123">Hlutverkið **Stjórnborð kostnaðarhlutar** stýrir ekki hvaða kostnaðarhlutum notandi hefur aðgang að og skoðað gögn fyrir.</span><span class="sxs-lookup"><span data-stu-id="1ce72-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="1ce72-124">Öryggi á línustigi fæst í gegnum stigveldi vídda og stigveldi aðgangslista.</span><span class="sxs-lookup"><span data-stu-id="1ce72-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="1ce72-125">Veita aðgangsréttindi</span><span class="sxs-lookup"><span data-stu-id="1ce72-125">Grant access rights</span></span>
<span data-ttu-id="1ce72-126">Eftirfarandi dæmi sýnir hvernig víddarstigveldi getur litið út.</span><span class="sxs-lookup"><span data-stu-id="1ce72-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="1ce72-127">**Upplýsingar um víddarstigveldi**</span><span class="sxs-lookup"><span data-stu-id="1ce72-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="1ce72-128">Heiti víddarstigveldis</span><span class="sxs-lookup"><span data-stu-id="1ce72-128">Dimension hierarchy name</span></span> | <span data-ttu-id="1ce72-129">Vídd</span><span class="sxs-lookup"><span data-stu-id="1ce72-129">Dimension</span></span>    | <span data-ttu-id="1ce72-130">Heiti gerðar víddarstigveldis</span><span class="sxs-lookup"><span data-stu-id="1ce72-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="1ce72-131">Stigveldi aðgangslista</span><span class="sxs-lookup"><span data-stu-id="1ce72-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="1ce72-132">Fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="1ce72-132">Organization</span></span>             | <span data-ttu-id="1ce72-133">Kostnaðarstaðir</span><span class="sxs-lookup"><span data-stu-id="1ce72-133">Cost centers</span></span> | <span data-ttu-id="1ce72-134">Stigveldi víddaflokkunar</span><span class="sxs-lookup"><span data-stu-id="1ce72-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="1ce72-135">**Já**</span><span class="sxs-lookup"><span data-stu-id="1ce72-135">**Yes**</span></span>               |

<span data-ttu-id="1ce72-136">Hægt er að nota flýtiflipann **Notendur** í stigveldishönnuði til að setja eitt eða fleiri notendakenni í hvern hnút.</span><span class="sxs-lookup"><span data-stu-id="1ce72-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|                                   | <span data-ttu-id="1ce72-137">Notendur</span><span class="sxs-lookup"><span data-stu-id="1ce72-137">Users</span></span>            | <span data-ttu-id="1ce72-138">Svið víddarstaks</span><span class="sxs-lookup"><span data-stu-id="1ce72-138">Dimension member ranges</span></span>   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="1ce72-139">**Hnútar**</span><span class="sxs-lookup"><span data-stu-id="1ce72-139">**Nodes**</span></span>                         | <span data-ttu-id="1ce72-140">**Notandakenni**</span><span class="sxs-lookup"><span data-stu-id="1ce72-140">**User ID**</span></span>      | <span data-ttu-id="1ce72-141">**Úr víddarstaki**</span><span class="sxs-lookup"><span data-stu-id="1ce72-141">**From dimension member**</span></span> | <span data-ttu-id="1ce72-142">**Til víddarstaks**</span><span class="sxs-lookup"><span data-stu-id="1ce72-142">**To dimension member**</span></span> |
| <span data-ttu-id="1ce72-143">Fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="1ce72-143">Organization</span></span>                      | <span data-ttu-id="1ce72-144">Benjamin, Claire</span><span class="sxs-lookup"><span data-stu-id="1ce72-144">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="1ce72-145">&nbsp;&nbsp;Stjórnandi</span><span class="sxs-lookup"><span data-stu-id="1ce72-145">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="1ce72-146">Apríl</span><span class="sxs-lookup"><span data-stu-id="1ce72-146">April</span></span>            |                           |                         |
| <span data-ttu-id="1ce72-147">&nbsp;&nbsp;&nbsp;&nbsp;Fjármál</span><span class="sxs-lookup"><span data-stu-id="1ce72-147">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="1ce72-148">Alicia</span><span class="sxs-lookup"><span data-stu-id="1ce72-148">Alicia</span></span>           | <span data-ttu-id="1ce72-149">CC002</span><span class="sxs-lookup"><span data-stu-id="1ce72-149">CC002</span></span>                     | <span data-ttu-id="1ce72-150">CC003</span><span class="sxs-lookup"><span data-stu-id="1ce72-150">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="1ce72-151">CC007</span><span class="sxs-lookup"><span data-stu-id="1ce72-151">CC007</span></span>                     | <span data-ttu-id="1ce72-152">CC007</span><span class="sxs-lookup"><span data-stu-id="1ce72-152">CC007</span></span>                   |
| <span data-ttu-id="1ce72-153">&nbsp;&nbsp;&nbsp;&nbsp;Mannauður</span><span class="sxs-lookup"><span data-stu-id="1ce72-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="1ce72-154">Arnie</span><span class="sxs-lookup"><span data-stu-id="1ce72-154">Arnie</span></span>            | <span data-ttu-id="1ce72-155">CC001</span><span class="sxs-lookup"><span data-stu-id="1ce72-155">CC001</span></span>                     | <span data-ttu-id="1ce72-156">CC001</span><span class="sxs-lookup"><span data-stu-id="1ce72-156">CC001</span></span>                   |
| <span data-ttu-id="1ce72-157">&nbsp;&nbsp;Framleiðsla</span><span class="sxs-lookup"><span data-stu-id="1ce72-157">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="1ce72-158">David</span><span class="sxs-lookup"><span data-stu-id="1ce72-158">David</span></span>            |                           |                         |
| <span data-ttu-id="1ce72-159">&nbsp;&nbsp;&nbsp;&nbsp;Pakkning</span><span class="sxs-lookup"><span data-stu-id="1ce72-159">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="1ce72-160">Ellen</span><span class="sxs-lookup"><span data-stu-id="1ce72-160">Ellen</span></span>            | <span data-ttu-id="1ce72-161">CC005</span><span class="sxs-lookup"><span data-stu-id="1ce72-161">CC005</span></span>                     | <span data-ttu-id="1ce72-162">CC005</span><span class="sxs-lookup"><span data-stu-id="1ce72-162">CC005</span></span>                   |
| <span data-ttu-id="1ce72-163">&nbsp;&nbsp;&nbsp;&nbsp;Smölun</span><span class="sxs-lookup"><span data-stu-id="1ce72-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="1ce72-164">Chris</span><span class="sxs-lookup"><span data-stu-id="1ce72-164">Chris</span></span>            | <span data-ttu-id="1ce72-165">CC006</span><span class="sxs-lookup"><span data-stu-id="1ce72-165">CC006</span></span>                     | <span data-ttu-id="1ce72-166">CC006</span><span class="sxs-lookup"><span data-stu-id="1ce72-166">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="1ce72-167">Kostnaðarbókarar skulu vera í efsta stigi stigveldisins svo þeir geti séð allar færslur í kostnaðarbókhaldi.</span><span class="sxs-lookup"><span data-stu-id="1ce72-167">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="1ce72-168">Áður en hægt er að nota stigveldi aðgangslista og öryggisstillingar þess verður að stilla valkostinn **Virkja skoðunaraðgang fyrir víddarstök kostnaðarhluta** á **Já** á flipanum **Almennt** á síðunni **Færibreytur kostnaðarbókhalds** (**Kostnaðarbókhald** > **Uppsetning** > **Færibreytur**).</span><span class="sxs-lookup"><span data-stu-id="1ce72-168">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="1ce72-169">Stillingar fyrir stigveldi aðgangslista eru notaðar til að stjórna gögnunum sem birtast á eftirfarandi svæðum:</span><span class="sxs-lookup"><span data-stu-id="1ce72-169">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="1ce72-170">Vinnusvæðið **Kostnaðarstýring** (í biðlaranum):</span><span class="sxs-lookup"><span data-stu-id="1ce72-170">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="1ce72-171">Gögn á síðum sem notaðar eru til köfunar</span><span class="sxs-lookup"><span data-stu-id="1ce72-171">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="1ce72-172">Vinnusvæðið **Kostnaðarstýring** (í fartækjaforritinu):</span><span class="sxs-lookup"><span data-stu-id="1ce72-172">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="1ce72-173">Stöður í spjöldum</span><span class="sxs-lookup"><span data-stu-id="1ce72-173">Balances in cards</span></span>

- <span data-ttu-id="1ce72-174">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="1ce72-174">Microsoft Power BI:</span></span>

    - <span data-ttu-id="1ce72-175">Gögn sem eru sýnd í Power BI myndrænum framsetningum</span><span class="sxs-lookup"><span data-stu-id="1ce72-175">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="1ce72-176">Myndræn Power BI gagnaframsetning sem er felld inn í Dynamics 365 Finance biðlarann</span><span class="sxs-lookup"><span data-stu-id="1ce72-176">Data Power BI visualizations that are embedded in the Dynamics 365 Finance client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="1ce72-177">Áður en stigveldi aðgangslista getur haft áhrif á gögnin í Power BI, verður að para saman stigveldi og öryggi á línustigi í Power BI.</span><span class="sxs-lookup"><span data-stu-id="1ce72-177">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="1ce72-178">Nánari upplýsingar eru í [Uppsetning öryggis fyrir þjónustupakka kostnaðarbókhalds](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="1ce72-178">For more information, see [Set up security for Cost accounting content pack](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="1ce72-179">Þetta efnisatriði sýnir nauðsynlegar forsendur þess að hægt sé að nota vinnusvæðið **Kostnaðarstýring**.</span><span class="sxs-lookup"><span data-stu-id="1ce72-179">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="1ce72-180">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="1ce72-180">Additional resources</span></span>

- [<span data-ttu-id="1ce72-181">Vinnusvæði kostnaðarstýringar</span><span class="sxs-lookup"><span data-stu-id="1ce72-181">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="1ce72-182">Víddarstigveldi</span><span class="sxs-lookup"><span data-stu-id="1ce72-182">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="1ce72-183">Uppsetning öryggis fyrir þjónustupakka kostnaðarbókhalds</span><span class="sxs-lookup"><span data-stu-id="1ce72-183">Set up security for Cost accounting content pack</span></span>](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]