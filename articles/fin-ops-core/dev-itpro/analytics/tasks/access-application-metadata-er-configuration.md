---
title: Fá aðgang að lýsigögnum hugbúnaðar með notkun á grunnstillingum rafrænnar skýrslugerðar
description: Skrefin í þessu efni útskýra hvernig notandi Regulatory Configuration Service (RCS) getur sett upp nýja líkanavörpun rafrænnar skýrslugerðar með notkun á lýsigögnum í Finance and Operations
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2bfe007995c894d6cc86d07ef2b52da65e32e950
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182739"
---
# <a name="access-application-metadata-by-using-er-configuration"></a><span data-ttu-id="af406-103">Fá aðgang að lýsigögnum hugbúnaðar með notkun á grunnstillingum rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="af406-103">Access application metadata by using ER configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="af406-104">Eftirfarandi skref útskýra hvernig notandi Regulatory Configuration Service í hlutverki kerfisstjóra eða þróunaraðila rafrænnar skýrslulausnar getur sett upp nýja líkanavörpun rafrænnar skýrslugerðar með því að nota lýsigögn forritsins.</span><span class="sxs-lookup"><span data-stu-id="af406-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using the application metadata.</span></span> <span data-ttu-id="af406-105">Farið verður í lýsigögn forrits með því að nota skilgreiningar ER-lýsigagna sem innihalda sýnishorn af lýsigögnum til að fá aðgang að utanríkisviðskiptum.</span><span class="sxs-lookup"><span data-stu-id="af406-105">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span> <span data-ttu-id="af406-106">Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í RCS í efnisatriðinu, ferlinu [Stofna skilgreiningarveitendur og merkja þá sem virka](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="af406-106">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> <span data-ttu-id="af406-107">Síðan lýkurðu við skrefin í efninu, [(ER) Undirbúa lýsigögn hugbúnaðar sem á að nota í RCS](prepare-application-metadata-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="af406-107">Then complete the steps in the topic, [(ER) Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="af406-108">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="af406-108">Prerequisites</span></span>
1. <span data-ttu-id="af406-109">Farðu í **Öll vinnusvæði** > **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="af406-109">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="af406-110">Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt **Virk**.</span><span class="sxs-lookup"><span data-stu-id="af406-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="af406-111">Ef þú sérð skilgreiningarveituna ekki skaltu klára skrefin í ferlinu [Stofna skilgreiningaveitur og merkja þær sem virkar](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="af406-111">If you don’t see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="import-metadata-configuration"></a><span data-ttu-id="af406-112">Flytja inn skilgreiningu lýsigagna</span><span class="sxs-lookup"><span data-stu-id="af406-112">Import metadata configuration</span></span> 
1. <span data-ttu-id="af406-113">Smelltu á **Skilgreiningu lýsigagna**.</span><span class="sxs-lookup"><span data-stu-id="af406-113">Click **Metadata configurations**.</span></span> 
2. <span data-ttu-id="af406-114">Flyttu inn lýsigögn rafrænnar skýrslugerðar sem inniheldur lýsigögn sem hafa verið stillt til að búa til rafræn skjöl fyrir utanríkisviðskipta.</span><span class="sxs-lookup"><span data-stu-id="af406-114">Import the ER metadata configuration that contains metadata that has been configured to generate electronic documents for foreign trade business.</span></span> <span data-ttu-id="af406-115">Þessi lýsigagnastilling rafrænnar skýrslugerðar hefur verið flutt út sem XML-skrá á meðan skrefin í ferlinu [(ER) Undirbúa umsóknardagatalið sem á að nota í RCS](prepare-application-metadata-rcs.md) hefur verið lokið.</span><span class="sxs-lookup"><span data-stu-id="af406-115">This ER metadata configuration has been exported as XML file while the steps in the [(ER) Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md) procedure have been completed.</span></span> 
3. <span data-ttu-id="af406-116">Smelltu á **Skipta út**.</span><span class="sxs-lookup"><span data-stu-id="af406-116">Click **Exchange**.</span></span> 
4. <span data-ttu-id="af406-117">Smelltu á **Hlaða úr XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="af406-117">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="af406-118">Smelltu á **Skoða** og veldu skrána „Foreign trade metadata.xml“.</span><span class="sxs-lookup"><span data-stu-id="af406-118">Click **Browse** and select the ‘Foreign trade metadata.xml’ file.</span></span> 
6. <span data-ttu-id="af406-119">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="af406-119">Click **OK**.</span></span> 
7. <span data-ttu-id="af406-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="af406-120">Close the page.</span></span> 

## <a name="create-data-model-configuration"></a><span data-ttu-id="af406-121">Stofna nýja skilgreiningu gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="af406-121">Create data model configuration</span></span>
1. <span data-ttu-id="af406-122">Smellið á **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="af406-122">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="af406-123">Smellið á **Stofna skilgreiningu** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="af406-123">Click **Create configuration** to open the drop dialog.</span></span> 
3. <span data-ttu-id="af406-124">Í reitinn **Heiti** slærðu inn „Líkan utanríkisverslunar“.</span><span class="sxs-lookup"><span data-stu-id="af406-124">In the **Name** field, type 'Foreign trade model'.</span></span> 
4. <span data-ttu-id="af406-125">Smellið á **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="af406-125">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="af406-126">Smellið á **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="af406-126">Click **Designer**.</span></span> 
6. <span data-ttu-id="af406-127">Smelltu á **Nýtt** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="af406-127">Click **New** to open the drop dialog.</span></span> 
7. <span data-ttu-id="af406-128">Í reitnum **Heiti** skaltu færa inn „Rót“.</span><span class="sxs-lookup"><span data-stu-id="af406-128">In the **Name** field, type 'Root'.</span></span> 
8. <span data-ttu-id="af406-129">Smelltu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="af406-129">Click **Add**.</span></span> 
9. <span data-ttu-id="af406-130">Smelltu á **Nýtt** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="af406-130">Click **New** to open the drop dialog.</span></span> 
10. <span data-ttu-id="af406-131">Í reitinn **Heiti** slærðu inn „Færsla“.</span><span class="sxs-lookup"><span data-stu-id="af406-131">In the **Name** field, type 'Transaction'.</span></span> 
11. <span data-ttu-id="af406-132">Í reitnum **Gerð vöru** velurðu **Skráalisti**.</span><span class="sxs-lookup"><span data-stu-id="af406-132">In the **Item type** field, select **Record list**.</span></span> 
12. <span data-ttu-id="af406-133">Smelltu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="af406-133">Click **Add**.</span></span> 
13. <span data-ttu-id="af406-134">Smelltu á **Nýtt** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="af406-134">Click **New** to open the drop dialog.</span></span> 
14. <span data-ttu-id="af406-135">Í reitinn **Heiti** slærðu inn „Grunnvörukóði“.</span><span class="sxs-lookup"><span data-stu-id="af406-135">In the **Name** field, type 'Commodity code'.</span></span> 
15. <span data-ttu-id="af406-136">Í reitnum **Gerð vöru** velurðu **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="af406-136">In the **Item type** field, select **String**.</span></span> 
16. <span data-ttu-id="af406-137">Smelltu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="af406-137">Click **Add**.</span></span> 
17. <span data-ttu-id="af406-138">Smelltu á **Nýtt** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="af406-138">Click **New** to open the drop dialog.</span></span> 
18. <span data-ttu-id="af406-139">Í reitinn **Heiti** slærðu inn „Reikningsfærð upphæð“.</span><span class="sxs-lookup"><span data-stu-id="af406-139">In the **Name** field, type 'Invoiced amount'.</span></span> 
19. <span data-ttu-id="af406-140">Í reitnum **Gerð vöru** velurðu **Rauntala**.</span><span class="sxs-lookup"><span data-stu-id="af406-140">In the **Item type** field, select **Real**.</span></span> 
20. <span data-ttu-id="af406-141">Smelltu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="af406-141">Click **Add**.</span></span> 
21. <span data-ttu-id="af406-142">Smelltu á **Nýtt** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="af406-142">Click **New** to open the drop dialog.</span></span> 
22. <span data-ttu-id="af406-143">Í reitinn **Heiti** slærðu inn „Dags.“.</span><span class="sxs-lookup"><span data-stu-id="af406-143">In the **Name** field, type 'Date'.</span></span> 
23. <span data-ttu-id="af406-144">Í reitnum **Gerð vöru** velurðu **Dags.**.</span><span class="sxs-lookup"><span data-stu-id="af406-144">In the **Item type** field, select **Date**.</span></span> 
24. <span data-ttu-id="af406-145">Smelltu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="af406-145">Click **Add**.</span></span> 
25. <span data-ttu-id="af406-146">Smelltu á **Rótartilvísun**.</span><span class="sxs-lookup"><span data-stu-id="af406-146">Click **Root reference**.</span></span> 
26. <span data-ttu-id="af406-147">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="af406-147">Click **OK**.</span></span> 
27. <span data-ttu-id="af406-148">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="af406-148">Click **Save**.</span></span> 
28. <span data-ttu-id="af406-149">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="af406-149">Close the page.</span></span> 
29. <span data-ttu-id="af406-150">Smelltu á **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="af406-150">Click **Change status**.</span></span> 
30. <span data-ttu-id="af406-151">Smelltu á **Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="af406-151">Click **Complete**.</span></span> 
31. <span data-ttu-id="af406-152">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="af406-152">Click **OK**.</span></span> 

## <a name="create-model-mapping-configuration"></a><span data-ttu-id="af406-153">Búa til skilgreiningu líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="af406-153">Create model mapping configuration</span></span> 
1. <span data-ttu-id="af406-154">Smellið á **Stofna skilgreiningu** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="af406-154">Click **Create configuration** to open the drop dialog.</span></span> 
2. <span data-ttu-id="af406-155">Í reitinn **Nýtt** slærðu inn „Vörpun líkans byggir á gagnalíkani Líkan utanríkisverslunar“.</span><span class="sxs-lookup"><span data-stu-id="af406-155">In the **New** field, enter 'Model Mapping based on data model Foreign trade model'.</span></span> 
3. <span data-ttu-id="af406-156">Í reitinn **Heiti** slærðu inn „Vörpun utanríkisverslunar“.</span><span class="sxs-lookup"><span data-stu-id="af406-156">In the **Name** field, type 'Foreign trade mapping'.</span></span> 
4. <span data-ttu-id="af406-157">Smellið á **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="af406-157">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="af406-158">Stækkaðu hlutann **Skilyrði**.</span><span class="sxs-lookup"><span data-stu-id="af406-158">Expand the **Prerequisites** section.</span></span> 
6. <span data-ttu-id="af406-159">Smellið á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="af406-159">Click **Edit**.</span></span> 
7. <span data-ttu-id="af406-160">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="af406-160">Click **New**.</span></span> 
8. <span data-ttu-id="af406-161">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="af406-161">In the list, mark the selected row.</span></span> 
9. <span data-ttu-id="af406-162">Í reitnum **Gerð forkröfuíhlutar** velurðu **Skilgreining**.</span><span class="sxs-lookup"><span data-stu-id="af406-162">In the **Prerequisite component type** field, select **Configuration**.</span></span> 
10. <span data-ttu-id="af406-163">Veldu skilgreininguna **Lýsigögn utanríkisviðskipta**.</span><span class="sxs-lookup"><span data-stu-id="af406-163">Select **Foreign trade metadata** configuration.</span></span> 
11. <span data-ttu-id="af406-164">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="af406-164">Click **Save**.</span></span> 
12. <span data-ttu-id="af406-165">Við bættum tilvísuninni við í útgáfu 1 af skilgreiningunni „Lýsigögn utanríkisviðskipta“.</span><span class="sxs-lookup"><span data-stu-id="af406-165">We added the reference to the version 1 of the ‘Foreign trade metadata’ configuration.</span></span> <span data-ttu-id="af406-166">Lýsigögn forrits úr þessari skilgreiningu verða boðin á meðan verið er að setja þessa líkanavörpun upp.</span><span class="sxs-lookup"><span data-stu-id="af406-166">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 
13. <span data-ttu-id="af406-167">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="af406-167">Close the page.</span></span> 
14. <span data-ttu-id="af406-168">Smellið á **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="af406-168">Click **Designer**.</span></span> 
15. <span data-ttu-id="af406-169">Smellið á **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="af406-169">Click **Designer**.</span></span> 
16. <span data-ttu-id="af406-170">Í trénu velurðu **Dynamics 365 for Operations\Töflufærslur**.</span><span class="sxs-lookup"><span data-stu-id="af406-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
17. <span data-ttu-id="af406-171">Smelltu á **Bæta rót við**.</span><span class="sxs-lookup"><span data-stu-id="af406-171">Click **Add root**.</span></span> 
18. <span data-ttu-id="af406-172">Í reitinn **Heiti** slærðu inn „Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="af406-172">In the **Name** field, type 'Intrastat'.</span></span> 
19. <span data-ttu-id="af406-173">Veldu **Intrastat**-töflufærslur.</span><span class="sxs-lookup"><span data-stu-id="af406-173">Select **Intrastat** table records.</span></span> 
20. <span data-ttu-id="af406-174">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="af406-174">Click **OK**.</span></span> 

> [!NOTE]
> <span data-ttu-id="af406-175">Einu 2 töflurnar voru boðnar þar sem aðeins 2 töflum var bætt í sett af lýsigögnum sem eru í notkun.</span><span class="sxs-lookup"><span data-stu-id="af406-175">The only 2 tables were offered as the only 2 tables were added into the set of metadata which is currently in use.</span></span> 

21. <span data-ttu-id="af406-176">Smelltu á **Binda**.</span><span class="sxs-lookup"><span data-stu-id="af406-176">Click **Bind**.</span></span> 
22. <span data-ttu-id="af406-177">Í trénu víkkarðu út **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="af406-177">In the tree, expand **Intrastat**.</span></span> 
23. <span data-ttu-id="af406-178">Í trénu velurðu **Intrastat\AmountMST**.</span><span class="sxs-lookup"><span data-stu-id="af406-178">In the tree, select **Intrastat\AmountMST**.</span></span> 
24. <span data-ttu-id="af406-179">Í trénu víkkarðu út **Færsla = Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="af406-179">In the tree, expand **Transaction = Intrastat**.</span></span> 
25. <span data-ttu-id="af406-180">Í trénu velurðu **Færsla = Intrastat\Reikningsfærð upphæð**.</span><span class="sxs-lookup"><span data-stu-id="af406-180">In the tree, select **Transaction = Intrastat\Invoiced amount**.</span></span> 
26. <span data-ttu-id="af406-181">Smelltu á **Binda**.</span><span class="sxs-lookup"><span data-stu-id="af406-181">Click **Bind**.</span></span> 
27. <span data-ttu-id="af406-182">Í trénu velurðu **Intrastat\TransDate**.</span><span class="sxs-lookup"><span data-stu-id="af406-182">In the tree, select **Intrastat\TransDate**.</span></span> 
28. <span data-ttu-id="af406-183">Í trénu velurðu **Færsla = Intrastat\Dags.**.</span><span class="sxs-lookup"><span data-stu-id="af406-183">In the tree, select **Transaction = Intrastat\Date**.</span></span> 
29. <span data-ttu-id="af406-184">Smelltu á **Binda**.</span><span class="sxs-lookup"><span data-stu-id="af406-184">Click **Bind**.</span></span> 
30. <span data-ttu-id="af406-185">Í trénu víkkarðu út **Intrastat\>Vensl**.</span><span class="sxs-lookup"><span data-stu-id="af406-185">In the tree, expand **Intrastat\>Relations**.</span></span> 
31. <span data-ttu-id="af406-186">Í trénu víkkarðu út **Intrastat\>Vensl\IntrastatCommodity**.</span><span class="sxs-lookup"><span data-stu-id="af406-186">In the tree, expand **Intrastat\>Relations\IntrastatCommodity**.</span></span> 
32. <span data-ttu-id="af406-187">Í trénu víkkarðu út **Intrastat\>Vensl\IntrastatCommodity\Kóði**.</span><span class="sxs-lookup"><span data-stu-id="af406-187">In the tree, select **Intrastat\>Relations\IntrastatCommodity\Code**.</span></span> 
33. <span data-ttu-id="af406-188">Í trénu velurðu **Færsla = Intrastat\Grunnvörukóði**.</span><span class="sxs-lookup"><span data-stu-id="af406-188">In the tree, select **Transaction = Intrastat\Commodity code**.</span></span> 
34. <span data-ttu-id="af406-189">Smelltu á **Binda**.</span><span class="sxs-lookup"><span data-stu-id="af406-189">Click **Bind**.</span></span> 
35. <span data-ttu-id="af406-190">Smelltu á **Villuleita**.</span><span class="sxs-lookup"><span data-stu-id="af406-190">Click **Validate**.</span></span> 

> [!NOTE]
> <span data-ttu-id="af406-191">Okkur tókst að binda þætti gagnalíkans við atriði gagnagjafa sem er lýst með því að nota upplýsingar um lýsigögn forrits úr þeirri skilgreiningu lýsigagna rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="af406-191">We have successfully bound elements of data model with items of data sources that are described by using details of application metadata from the referred ER metadata configuration.</span></span> 
36. <span data-ttu-id="af406-192">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="af406-192">Click **Save**.</span></span> 
37. <span data-ttu-id="af406-193">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="af406-193">Close the page.</span></span> 
38. <span data-ttu-id="af406-194">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="af406-194">Close the page.</span></span> 
39. <span data-ttu-id="af406-195">Þegar þess er þörf geturðu lengt núverandi lýsigagnasett og flutt síðan út nýja lokna útgáfu af ER lýsigögnum.</span><span class="sxs-lookup"><span data-stu-id="af406-195">When needed, you can extend the existing set of metadata and then export the new completed version of ER metadata configuration.</span></span> <span data-ttu-id="af406-196">Þú getur síðan flutt það inn í RCS og uppfært forsendur fyrir samstillta gerð kortagerðar með vísan til nýrrar útgáfu af innfluttum lýsigagnasamsetningum.</span><span class="sxs-lookup"><span data-stu-id="af406-196">You can then import it to RCS, and update the prerequisites of the configured model mapping configuration referring to a new version of imported metadata configuration.</span></span> 

> [!NOTE]
> <span data-ttu-id="af406-197">Þessi leið til að sækja upplýsingar um lýsigögn hugbúnaðar er sú eina sem er í boði fyrir staðbundið uppsett forrit (þegar uppsetningarlíkan staðbundinna eða innanhúss viðskiptagagna (LBD) er notað).</span><span class="sxs-lookup"><span data-stu-id="af406-197">This way of getting information about application metadata is the only one available for locally deployed applications (when local business data (LBD), or on-premises, deployment model is used).</span></span>
        
