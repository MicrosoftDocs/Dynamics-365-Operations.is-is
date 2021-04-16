---
title: Undirbúa forritasértæk lýsigögn fyrir RCS og ER
description: Þetta efni útskýrir hvernig á að undirbúa forritasértæk lýsigögn fyrir Regulatory Configuration Service (RCS) og Rafræna skýrslugerð (ER).
author: NickSelin
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: f0501fd67da0cbc5c10171b55004cb7f4fd4fd16
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743704"
---
# <a name="prepare-application-specific-metadata-for-rcs-and-er"></a><span data-ttu-id="0b106-103">Undirbúa forritasértæk lýsigögn fyrir RCS og ER</span><span class="sxs-lookup"><span data-stu-id="0b106-103">Prepare application-specific metadata for RCS and ER</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0b106-104">Þetta efni fer með þig í gegnum dæmi um eftirfarandi verk:</span><span class="sxs-lookup"><span data-stu-id="0b106-104">This topic walks you through examples of the following tasks:</span></span>

- [<span data-ttu-id="0b106-105">Undirbúa lýsigögn forrits sem hægt er að nota í RCS</span><span class="sxs-lookup"><span data-stu-id="0b106-105">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)
- [<span data-ttu-id="0b106-106">Aðgangur að lýsigögnum forrits með ER-skilgreiningu</span><span class="sxs-lookup"><span data-stu-id="0b106-106">Access application metadata by using an ER configuration</span></span>](#access-application-metadata-by-using-an-er-configuration)
- [<span data-ttu-id="0b106-107">Aðgangur að lýsigögnum forrits með tengdum forritum</span><span class="sxs-lookup"><span data-stu-id="0b106-107">Access application metadata by using connected applications</span></span>](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a><span data-ttu-id="0b106-108">Undirbúa lýsigögn forrits sem hægt er að nota í RCS</span><span class="sxs-lookup"><span data-stu-id="0b106-108">Prepare application metadata that can be used in RCS</span></span>

<span data-ttu-id="0b106-109">Eftirfarandi ferli sýnir hvernig notandi sem er með hlutverkið **Kerfisstjóri** eða **Þróunaraðili rafrænnar skýrslulausnar** getur búið til skilgreiningar rafrænnar skýrslugerðar (ER) sem innihalda lýsigögn fyrir forritið og sem eru notuð til að setja upp skilgreiningar ER-líkanavörpunar í Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="0b106-109">The following procedure shows how a user who has the **System Administrator** or **Electronic Reporting Developer** role can create an Electronic reporting (ER) configuration that contains metadata for the application, and that is used to design ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="0b106-110">Sýnisskilgreining ER-líkanavörpunar sem er búið til í þessu dæmi verður notað til að fá aðgang að utanríkisviðskiptum.</span><span class="sxs-lookup"><span data-stu-id="0b106-110">The sample ER model mapping configuration that is created in this example will be used to access foreign trade transactions.</span></span>

<span data-ttu-id="0b106-111">Í þessu dæmi viltu nota RCS til að setja upp ER-lausn fyrir forritið, sem verður notuð til að búa til rafræn skjöl sem innihalda upplýsingar úr umdæmi utanríkisviðskipta.</span><span class="sxs-lookup"><span data-stu-id="0b106-111">For this example, you want to use RCS to design an ER solution for the application that will be used to generate electronic documents that contain information from the foreign trade business domain.</span></span> <span data-ttu-id="0b106-112">Til að tilgreina vörpun milli ER-gagnalíkans og uppruna nauðsynlegra gagna, verður þú að hafa aðgang að forritslýsigögnum í RCS.</span><span class="sxs-lookup"><span data-stu-id="0b106-112">To specify the mapping between the ER data model and the sources of required data, you must have access to application metadata in RCS.</span></span> <span data-ttu-id="0b106-113">Þess vegna verður þú að skilgreina nýja ER lýsigagnaskilgreiningu sem inniheldur öll lýsigögnin sem þarf eins og stendur til að mynda ER-skýrslur fyrir valið viðskiptalén sem hluta af ferlinu við að setja upp ER-lausnina.</span><span class="sxs-lookup"><span data-stu-id="0b106-113">Therefore, as part of the process of designing the ER solution, you must configure a new ER metadata configuration that contains all the metadata that is currently required in order to generate ER reports for the selected business domain.</span></span>

> [!NOTE]
> <span data-ttu-id="0b106-114">Í þessu dæmi muntu stofna skilgreiningu fyrir sýnifyrirtækið, Litware, Inc. Þessi skref má framkvæma í hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="0b106-114">In this example, you will create a configuration for the sample company, Litware, Inc. These steps can be performed in any company.</span></span>

1. <span data-ttu-id="0b106-115">Fara í **Fyrirtækisstjórnun \> Vinnusvæði \> Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="0b106-115">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="0b106-116">Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt **Virk**.</span><span class="sxs-lookup"><span data-stu-id="0b106-116">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="0b106-117">Ef þú sérð skilgreiningarveituna ekki skaltu klára skrefin í ferlinu [Stofna skilgreiningaveitur og merkja þær sem virkar](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="0b106-117">If you don't see this configuration provider, complete the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="0b106-118">Veldu **Skilgreiningar lýsigagna**.</span><span class="sxs-lookup"><span data-stu-id="0b106-118">Select **Metadata configurations**.</span></span>
4. <span data-ttu-id="0b106-119">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="0b106-119">Select **Create configuration**.</span></span>
5. <span data-ttu-id="0b106-120">Í fellilistanum, í reitnum **Heiti** slærðu inn heiti.</span><span class="sxs-lookup"><span data-stu-id="0b106-120">In the drop-down dialog box, in the **Name** field, enter a name.</span></span> <span data-ttu-id="0b106-121">Fyrir þetta dæmi skaltu slá inn **Lýsigögn utanríkisviðskipta**.</span><span class="sxs-lookup"><span data-stu-id="0b106-121">For this example, enter **Foreign trade metadata**.</span></span>
6. <span data-ttu-id="0b106-122">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="0b106-122">Select **Create configuration**.</span></span>
7. <span data-ttu-id="0b106-123">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="0b106-123">Select **Designer**.</span></span>
8. <span data-ttu-id="0b106-124">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="0b106-124">Select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0b106-125">Þú getur valið öll lýsigögn annaðhvort fyrir allt forritið eða fyrir valdin líkön eða einingar.</span><span class="sxs-lookup"><span data-stu-id="0b106-125">You can select all metadata either for the whole application, or for selected models or modules.</span></span> <span data-ttu-id="0b106-126">Í báðum dæmum skaltu hafa í huga að eftirfarandi lýsigögnum verður sjálfkrafa bætt við: töflum yfir skrám, talningum og lengd gagnategunda (EDT).</span><span class="sxs-lookup"><span data-stu-id="0b106-126">In both cases, be aware that the following metadata will be automatically added: tables of records, enumerations, and extended data types (EDTs).</span></span> <span data-ttu-id="0b106-127">Þegar fleiri tegundir lýsigagna eru nauðsynlegar verður að bæta þeim handvirkt við.</span><span class="sxs-lookup"><span data-stu-id="0b106-127">When additional types of metadata are required, they must be manually added.</span></span>

    <span data-ttu-id="0b106-128">Þú verður að bæta við lýsigögnum sem tengjast utanríkisviðskiptadæealum og velja lýsigögn á handvirkan hátt.</span><span class="sxs-lookup"><span data-stu-id="0b106-128">You must add some metadata that is related to foreign trade transactions and manually select metadata items.</span></span>

9. <span data-ttu-id="0b106-129">Veldu **Bæta við gagnasafni \> Töflufærslur**.</span><span class="sxs-lookup"><span data-stu-id="0b106-129">Select **Add data source \> Table records**.</span></span>
10. <span data-ttu-id="0b106-130">Sía á gildi **Intrastat** í reitnum **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="0b106-130">Filter on a value of **Intrastat** in the **Name** field.</span></span>
11. <span data-ttu-id="0b106-131">Veldu **Intrastat**-töflu.</span><span class="sxs-lookup"><span data-stu-id="0b106-131">Select the **Intrastat** table record.</span></span>
12. <span data-ttu-id="0b106-132">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0b106-132">Select **OK**.</span></span>

    <span data-ttu-id="0b106-133">Þú verður að bæta við lýsigögnum um Intrastat-skráatöfluna.</span><span class="sxs-lookup"><span data-stu-id="0b106-133">You must add metadata information about the Intrastat table of records.</span></span>

13. <span data-ttu-id="0b106-134">Í trénu skaltu velja **Töflufærslur Intrastat \> \>Vensl \> IntrastatCommodity (Töflufærslur EcoResCategory)**.</span><span class="sxs-lookup"><span data-stu-id="0b106-134">In the tree, select **Table records Intrastat \> \>Relations \> IntrastatCommodity (Table records EcoResCategory)**.</span></span>
14. <span data-ttu-id="0b106-135">Veldu **Bæta við lýsigögnum**.</span><span class="sxs-lookup"><span data-stu-id="0b106-135">Select **Add metadata**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0b106-136">Lýsigögn um nauðsynleg vensl fyrir valda skráatöflu verður að bæta við á handvirkan hátt.</span><span class="sxs-lookup"><span data-stu-id="0b106-136">Metadata about required relations for the selected table of records must be added manually.</span></span>

15. <span data-ttu-id="0b106-137">Veldu **Bæta við gagnagjafa**.</span><span class="sxs-lookup"><span data-stu-id="0b106-137">Select **Add data source**.</span></span>
16. <span data-ttu-id="0b106-138">Veldu **Upptalningu**.</span><span class="sxs-lookup"><span data-stu-id="0b106-138">Select **Enumeration**.</span></span>
17. <span data-ttu-id="0b106-139">Sía á gildi **IntrastatDirection** í reitnum **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="0b106-139">Filter on a value of **IntrastatDirection** in the **Name** field.</span></span>
18. <span data-ttu-id="0b106-140">Veldu upptalningarskrána **IntrastatDirection**.</span><span class="sxs-lookup"><span data-stu-id="0b106-140">Select the **IntrastatDirection** enumeration record.</span></span>
19. <span data-ttu-id="0b106-141">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0b106-141">Select **OK**.</span></span>
20. <span data-ttu-id="0b106-142">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="0b106-142">Select **Save**.</span></span>
21. <span data-ttu-id="0b106-143">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="0b106-143">Close the page.</span></span>
22. <span data-ttu-id="0b106-144">Ljúktu drögunum að útgáfu skilgreiningar lýsigagnanna:</span><span class="sxs-lookup"><span data-stu-id="0b106-144">Complete the draft version of the metadata configuration:</span></span>

    1. <span data-ttu-id="0b106-145">Velduð **Breyta stöðu \> Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="0b106-145">Select **Change status \> Complete**.</span></span>
    2. <span data-ttu-id="0b106-146">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0b106-146">Select **OK**.</span></span>
    3. <span data-ttu-id="0b106-147">Veldu fullgerða útgáfu 1.</span><span class="sxs-lookup"><span data-stu-id="0b106-147">Select the completed version 1.</span></span>

23. <span data-ttu-id="0b106-148">Flyttu út fullgerða útgáfu lýsigagnauppsetningar úr forritinu sem XML-skrá:</span><span class="sxs-lookup"><span data-stu-id="0b106-148">Export the completed version of the metadata configuration from the application as an XML file:</span></span>

    1. <span data-ttu-id="0b106-149">Veldu **Gengi \> Flytja út sem XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="0b106-149">Select **Exchange \> Export as XML file**.</span></span>
    2. <span data-ttu-id="0b106-150">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0b106-150">Select **OK**.</span></span>

<span data-ttu-id="0b106-151">ER-lýsigagnasskilgreiningin sem þú bjóst til er vistuð sem skráin **Foreign trade metadata.xml**.</span><span class="sxs-lookup"><span data-stu-id="0b106-151">The ER metadata configuration that you created is saved as the **Foreign trade metadata.xml** file.</span></span> <span data-ttu-id="0b106-152">Núna geturðu flutt þær inn í RCS, þannig að hægt sé að nota þær sem uppruna lýsigagna fyrir utanríkisviðskiptalén.</span><span class="sxs-lookup"><span data-stu-id="0b106-152">You can now import it into RCS, so that it can be used as the source of metadata for the foreign trade business domain.</span></span> <span data-ttu-id="0b106-153">Samkvæmt þessum upplýsingum er hægt að tilgreina vörpun á milli lýsigagna forritsins og ER-gagnalíkansins.</span><span class="sxs-lookup"><span data-stu-id="0b106-153">Based on this information, you can specify the mapping between application metadata and the ER data model.</span></span>

## <a name="access-application-metadata-by-using-an-er-configuration"></a><span data-ttu-id="0b106-154">Aðgangur að lýsigögnum forrits með ER-skilgreiningu</span><span class="sxs-lookup"><span data-stu-id="0b106-154">Access application metadata by using an ER configuration</span></span>

<span data-ttu-id="0b106-155">Eftirfarandi ferli sýnir hvernig RCS-notandi sem er með hlutverkið **Kerfisstjóri** eða **Þróunaraðili rafrænnar skýrsluhönnunar** getur sett upp nýja ER-líkanavörpun með því að nota lýsigögn úr forritinu.</span><span class="sxs-lookup"><span data-stu-id="0b106-155">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata from the application.</span></span> <span data-ttu-id="0b106-156">Farið verður í lýsigögn forrits með því að nota skilgreiningar ER-lýsigagna sem innihalda sýnishorn af lýsigögnum til að fá aðgang að utanríkisviðskiptum.</span><span class="sxs-lookup"><span data-stu-id="0b106-156">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span>

<span data-ttu-id="0b106-157">Áður en hægt er að ljúka þessu verður fyrst að ljúka eftirfarandi ferlum:</span><span class="sxs-lookup"><span data-stu-id="0b106-157">Before you can complete this procedure, you must first complete the following procedures:</span></span>

- [<span data-ttu-id="0b106-158">Stofna skilgreiningarveitendur og merkja þá sem virka</span><span class="sxs-lookup"><span data-stu-id="0b106-158">Create configuration providers and mark them as active</span></span>](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [<span data-ttu-id="0b106-159">Undirbúa lýsigögn forrits sem hægt er að nota í RCS</span><span class="sxs-lookup"><span data-stu-id="0b106-159">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)

1. <span data-ttu-id="0b106-160">Farðu í **Öll vinnusvæði \> Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="0b106-160">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="0b106-161">Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt **Virk**.</span><span class="sxs-lookup"><span data-stu-id="0b106-161">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="0b106-162">Ef þú sérð skilgreiningarveituna ekki skaltu klára skrefin í ferlinu [Stofna skilgreiningaveitur og merkja þær sem virkar](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="0b106-162">If you don't see this configuration provider, complete the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="0b106-163">Flyttu inn lýsigögn rafrænnar skýrslugerðar sem inniheldur lýsigögn fyrir forritið og sem eru stillt til að búa til rafræn skjöl fyrir lén utanríkisviðskipta.</span><span class="sxs-lookup"><span data-stu-id="0b106-163">Import the ER metadata configuration that contains metadata for the application, and that is configured to generate electronic documents for the foreign trade business domain.</span></span> <span data-ttu-id="0b106-164">Þú stofnaðir þessa skilgreiningu ER-lýsigagna og fluttir það sem XML-skrá í [Undirbúa lýsigögn forrits sem hægt er að nota í RCS-ferlinu](#prepare-application-metadata-that-can-be-used-in-rcs) fyrr í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="0b106-164">You created this ER metadata configuration and exported it as an XML file in the [Prepare application metadata that can be used in RCS](#prepare-application-metadata-that-can-be-used-in-rcs) procedure earlier in this topic.</span></span>

    1. <span data-ttu-id="0b106-165">Veldu **Skilgreiningar lýsigagna**.</span><span class="sxs-lookup"><span data-stu-id="0b106-165">Select **Metadata configurations**.</span></span>
    2. <span data-ttu-id="0b106-166">Veldu **Gengi**.</span><span class="sxs-lookup"><span data-stu-id="0b106-166">Select **Exchange**.</span></span>
    3. <span data-ttu-id="0b106-167">Veldu **Hlaða úr XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="0b106-167">Select **Load from XML file**.</span></span>
    4. <span data-ttu-id="0b106-168">Flettu til að velja skrána **Foreign trade metadata.xml**.</span><span class="sxs-lookup"><span data-stu-id="0b106-168">Browse to select the **Foreign trade metadata.xml** file.</span></span>
    5. <span data-ttu-id="0b106-169">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0b106-169">Select **OK**.</span></span>
    6. <span data-ttu-id="0b106-170">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="0b106-170">Close the page.</span></span>

4. <span data-ttu-id="0b106-171">Stofnaðu nýja skilgreiningu gagnalíkans:</span><span class="sxs-lookup"><span data-stu-id="0b106-171">Create a data model configuration:</span></span>

    1. <span data-ttu-id="0b106-172">Veldu **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="0b106-172">Select **Reporting configurations**.</span></span>
    2. <span data-ttu-id="0b106-173">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="0b106-173">Select **Create configuration**.</span></span>
    3. <span data-ttu-id="0b106-174">Í fellilistanum, í reitnum **Heiti** slærðu inn **Líkan utanríkisverslunar**.</span><span class="sxs-lookup"><span data-stu-id="0b106-174">In the drop-down dialog box, in the **Name** field, enter **Foreign trade model**.</span></span>
    4. <span data-ttu-id="0b106-175">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="0b106-175">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="0b106-176">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="0b106-176">Select **Designer**.</span></span>
    6. <span data-ttu-id="0b106-177">Veldu **Nýtt** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="0b106-177">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="0b106-178">Í reitnum **Heiti** skaltu færa inn **Rót**.</span><span class="sxs-lookup"><span data-stu-id="0b106-178">In the **Name** field, type **Root**.</span></span>
        2. <span data-ttu-id="0b106-179">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="0b106-179">Select **Add**.</span></span>
    
    7. <span data-ttu-id="0b106-180">Veldu **Nýtt** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="0b106-180">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="0b106-181">Í reitinn **Heiti** slærðu inn **Færsla**.</span><span class="sxs-lookup"><span data-stu-id="0b106-181">In the **Name** field, type **Transaction**.</span></span>
        2. <span data-ttu-id="0b106-182">Í reitnum **Gerð vöru** velurðu **Skráalisti**.</span><span class="sxs-lookup"><span data-stu-id="0b106-182">In the **Item type** field, select **Record list**.</span></span>
        3. <span data-ttu-id="0b106-183">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="0b106-183">Select **Add**.</span></span>
 
    8. <span data-ttu-id="0b106-184">Veldu **Nýtt** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="0b106-184">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="0b106-185">Í reitinn **Heiti** slærðu inn **Grunnvörukóði**.</span><span class="sxs-lookup"><span data-stu-id="0b106-185">In the **Name** field, type **Commodity code**.</span></span>
        2. <span data-ttu-id="0b106-186">Í reitnum **Gerð vöru** velurðu **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="0b106-186">In the **Item type** field, select **String**.</span></span>
        3. <span data-ttu-id="0b106-187">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="0b106-187">Select **Add**.</span></span>

    9. <span data-ttu-id="0b106-188">Veldu **Nýtt** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="0b106-188">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="0b106-189">Í reitinn Heiti slærðu inn **Reikningsfærð upphæð**.</span><span class="sxs-lookup"><span data-stu-id="0b106-189">In the Name field, type **Invoiced amount**.</span></span>
        2. <span data-ttu-id="0b106-190">Í reitnum **Gerð vöru** velurðu **Rauntala**.</span><span class="sxs-lookup"><span data-stu-id="0b106-190">In the **Item type** field, select **Real**.</span></span>
        3. <span data-ttu-id="0b106-191">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="0b106-191">Select **Add**.</span></span>

    10. <span data-ttu-id="0b106-192">Veldu **Nýtt** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="0b106-192">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="0b106-193">Í reitinn **Heiti** slærðu inn **Dags.**.</span><span class="sxs-lookup"><span data-stu-id="0b106-193">In the **Name** field, type **Date**.</span></span>
        2. <span data-ttu-id="0b106-194">Í reitnum **Gerð vöru** velurðu **Dags.**.</span><span class="sxs-lookup"><span data-stu-id="0b106-194">In the **Item type** field, select **Date**.</span></span>
        3. <span data-ttu-id="0b106-195">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="0b106-195">Select **Add**.</span></span>
 
    11. <span data-ttu-id="0b106-196">Veldu **Bæta við \> Rótartilvísun**.</span><span class="sxs-lookup"><span data-stu-id="0b106-196">Select **Add \> Root reference**.</span></span>
    12. <span data-ttu-id="0b106-197">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0b106-197">Select **OK**.</span></span>
    13. <span data-ttu-id="0b106-198">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="0b106-198">Select **Save**.</span></span>
    14. <span data-ttu-id="0b106-199">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="0b106-199">Close the page.</span></span>
    15. <span data-ttu-id="0b106-200">Velduð **Breyta stöðu \> Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="0b106-200">Select **Change status \> Complete**.</span></span>
    16. <span data-ttu-id="0b106-201">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0b106-201">Select **OK**.</span></span>

5. <span data-ttu-id="0b106-202">Stofna skilgreiningu líkanavörpunar:</span><span class="sxs-lookup"><span data-stu-id="0b106-202">Create a model mapping configuration:</span></span>

    1. <span data-ttu-id="0b106-203">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="0b106-203">Select **Create configuration**.</span></span>
    2. <span data-ttu-id="0b106-204">Í fellilistanum, í reitnum **Nýtt**, slærðu inn **Vörpun líkans byggir á gagnalíkani utanríkisverslunarlíkans**.</span><span class="sxs-lookup"><span data-stu-id="0b106-204">In the drop-down dialog box, in the **New** field, enter **Model Mapping based on data model Foreign trade model**.</span></span>
    3. <span data-ttu-id="0b106-205">Í reitnum **Heiti** slærðu inn **Vörpun utanríkisverslunar**.</span><span class="sxs-lookup"><span data-stu-id="0b106-205">In the **Name** field, enter **Foreign trade mapping**.</span></span>
    4. <span data-ttu-id="0b106-206">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="0b106-206">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="0b106-207">Á flýtiflipanum **Forkröfur** velurðu **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="0b106-207">On the **Prerequisites** FastTab, select **Edit**.</span></span>
    6. <span data-ttu-id="0b106-208">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="0b106-208">Select **New**.</span></span>
    7. <span data-ttu-id="0b106-209">Í reitnum **Gerð forkröfuíhlutar** velurðu **Skilgreining**.</span><span class="sxs-lookup"><span data-stu-id="0b106-209">In the **Prerequisite component type** field, select **Configuration**.</span></span>
    8. <span data-ttu-id="0b106-210">Veldu skilgreininguna **Lýsigögn utanríkisviðskipta**.</span><span class="sxs-lookup"><span data-stu-id="0b106-210">Select the **Foreign trade metadata** configuration.</span></span>
    9. <span data-ttu-id="0b106-211">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="0b106-211">Select **Save**.</span></span> <span data-ttu-id="0b106-212">Athugaðu að tilvísuninni er bætt við í útgáfu 1 af skilgreiningunni **Lýsigögn utanríkisviðskipta**.</span><span class="sxs-lookup"><span data-stu-id="0b106-212">Notice that the reference is added to version 1 of the **Foreign trade metadata** configuration.</span></span> <span data-ttu-id="0b106-213">Lýsigögn forrits úr þessari skilgreiningu verða boðin á meðan líkanavörpunin er sett upp.</span><span class="sxs-lookup"><span data-stu-id="0b106-213">Application metadata from this configuration will be offered while the model mapping is designed.</span></span>
    10. <span data-ttu-id="0b106-214">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="0b106-214">Close the page.</span></span>
    11. <span data-ttu-id="0b106-215">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="0b106-215">Select **Designer**.</span></span>
    12. <span data-ttu-id="0b106-216">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="0b106-216">Select **Designer**.</span></span>
    13. <span data-ttu-id="0b106-217">Í trénu velurðu **Dynamics 365 for Operations \> Töflufærslur**.</span><span class="sxs-lookup"><span data-stu-id="0b106-217">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
    14. <span data-ttu-id="0b106-218">Veljið **Bæta við rót**.</span><span class="sxs-lookup"><span data-stu-id="0b106-218">Select **Add root**.</span></span>
    15. <span data-ttu-id="0b106-219">Í reitinn **Heiti** skal færa inn **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="0b106-219">In the **Name** field, enter **Intrastat**.</span></span>
    16. <span data-ttu-id="0b106-220">Veldu **Intrastat**-töflufærslur.</span><span class="sxs-lookup"><span data-stu-id="0b106-220">Select **Intrastat** table records.</span></span>
    17. <span data-ttu-id="0b106-221">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0b106-221">Select **OK**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="0b106-222">Einu 2 töflurnar eru boðnar, þar sem aðeins tveimur töflum var bætt við í sett af lýsigögnum sem eru í notkun.</span><span class="sxs-lookup"><span data-stu-id="0b106-222">Only two tables are offered, because only two tables were added to the set of metadata that is currently used.</span></span>

    18. <span data-ttu-id="0b106-223">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="0b106-223">Select **Bind**.</span></span>
    19. <span data-ttu-id="0b106-224">Í trénu velurðu **Intrastat \> AmountMST**.</span><span class="sxs-lookup"><span data-stu-id="0b106-224">In the tree, select **Intrastat \> AmountMST**.</span></span>
    20. <span data-ttu-id="0b106-225">Í trénu velurðu **Færsla = Intrastat \> Reikningsfærð upphæð**.</span><span class="sxs-lookup"><span data-stu-id="0b106-225">In the tree, select **Transaction = Intrastat \> Invoiced amount**.</span></span>
    21. <span data-ttu-id="0b106-226">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="0b106-226">Select **Bind**.</span></span>
    22. <span data-ttu-id="0b106-227">Í trénu velurðu **Intrastat \> TransDate**.</span><span class="sxs-lookup"><span data-stu-id="0b106-227">In the tree, select **Intrastat \> TransDate**.</span></span>
    23. <span data-ttu-id="0b106-228">Í trénu velurðu **Færsla = Intrastat \> Dags.**.</span><span class="sxs-lookup"><span data-stu-id="0b106-228">In the tree, select **Transaction = Intrastat \> Date**.</span></span>
    24. <span data-ttu-id="0b106-229">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="0b106-229">Select **Bind**.</span></span>
    25. <span data-ttu-id="0b106-230">Í trénu víkkarðu út **Intrastat \> \>Vensl \> IntrastatCommodity \> Kóði**.</span><span class="sxs-lookup"><span data-stu-id="0b106-230">In the tree, select **Intrastat \> \>Relations \> IntrastatCommodity \> Code**.</span></span>
    26. <span data-ttu-id="0b106-231">Í trénu velurðu **Færsla = Intrastat \> Grunnvörukóði**.</span><span class="sxs-lookup"><span data-stu-id="0b106-231">In the tree, select **Transaction = Intrastat \> Commodity code**.</span></span>
    27. <span data-ttu-id="0b106-232">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="0b106-232">Select **Bind**.</span></span>
    28. <span data-ttu-id="0b106-233">Veldu **Staðfesta**.</span><span class="sxs-lookup"><span data-stu-id="0b106-233">Select **Validate**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="0b106-234">Eftir að staðfestingu er lokið hefur þér tekist að binda þætti gagnalíkans við atriði gagnagjafa sem er lýst með því að nota upplýsingar um lýsigögn forrits tilvísaðri skilgreiningu ER-lýsigagna.</span><span class="sxs-lookup"><span data-stu-id="0b106-234">After validation is completed, you've successfully bound elements of the data model to items of the data sources that are described by using details of the application metadata from the referenced ER metadata configuration.</span></span>

    29. <span data-ttu-id="0b106-235">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="0b106-235">Select **Save**.</span></span>

<span data-ttu-id="0b106-236">Þegar þú þarft þess geturðu framlengt núverandi safn lýsigagna í forritinu.</span><span class="sxs-lookup"><span data-stu-id="0b106-236">As you require, you can extend the existing set of metadata in the application.</span></span> <span data-ttu-id="0b106-237">Síðan geturðu flutt út nýlokna útgáfu af skilgreiningu ER-lýsigagna, flutt hana inn í RCS og uppfært forkröfur þess að skilgreind líkanavörpun vísi í nýja útgáfu af innfluttri skilgreiningu lýsigagna.</span><span class="sxs-lookup"><span data-stu-id="0b106-237">You can then export the new completed version of the ER metadata configuration, import it into RCS, and update the prerequisites of the configured model mapping configuration to refer to a new version of the imported metadata configuration.</span></span>

> [!NOTE]
> <span data-ttu-id="0b106-238">Þessi aðferð til að sækja upplýsingar um lýsigögn hugbúnaðar er eina tiltæka aðferðin fyrir forrit sem eru notuð staðbundið (það er að segja, þegar uppsetningarlíkan staðbundinna eða innanhúss viðskiptagagna \[LBD\] er notað fyrir forritið).</span><span class="sxs-lookup"><span data-stu-id="0b106-238">This method for getting information about application metadata is the only available method for applications that are locally deployed (that is, when a local business data \[LBD\], or on-premises, deployment model is used for the application).</span></span>

## <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="0b106-239">Aðgangur að lýsigögnum forrits með tengdum forritum</span><span class="sxs-lookup"><span data-stu-id="0b106-239">Access application metadata by using connected applications</span></span>

<span data-ttu-id="0b106-240">Eftirfarandi ferli sýnir hvernig RCS-notandi sem er með hlutverkið **Kerfisstjóri** eða **Þróunaraðili rafrænnar skýrsluhönnunar** getur sett upp nýja ER-líkanavörpun með því að nota lýsigögn úr forritinu.</span><span class="sxs-lookup"><span data-stu-id="0b106-240">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata of the application.</span></span> <span data-ttu-id="0b106-241">Lýsigögn hugbúnaðar verða skoðuð á netinu með því að nota RCS -tengda forritið.</span><span class="sxs-lookup"><span data-stu-id="0b106-241">Application metadata will be accessed online by using RCS connected application.</span></span> <span data-ttu-id="0b106-242">Dæmi um ER-líkanavörpun verður skilgreint til að fá aðgang að utanríkisviðskiptafærslum.</span><span class="sxs-lookup"><span data-stu-id="0b106-242">A sample ER model mapping will be configured to access foreign trade transactions.</span></span>

<span data-ttu-id="0b106-243">Til að ljúka þessu ferli verður fyrst að ljúka ferlinu [Stofna skilgreiningarveitur og merkja þær sem virkar](tasks/er-configuration-provider-mark-it-active-2016-11.md) í RCS.</span><span class="sxs-lookup"><span data-stu-id="0b106-243">To complete this procedure, you must first complete the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure in RCS.</span></span> <span data-ttu-id="0b106-244">Ef þú hefur ekki þegar lokið við ferlið [Aðgangur að lýsigögnum forrits með ER-skilgreiningu](#access-application-metadata-by-using-an-er-configuration) fyrri í þessu efnisatriði, skaltu fara á síðuna [Verkefnaleiðbeiningar rafrænnar skýrslugerðar fyrir Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) til að sækja eftirfarandi ER-skilgreiningarskrár fyrirfram og vista þær staðbundið: **Foreign trade metadata.xml**, **Foreign trade model.xml** og **Foreign trade mapping.xml**.</span><span class="sxs-lookup"><span data-stu-id="0b106-244">If you haven't yet completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, go to [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page to download the following ER configuration files in advance and save them locally: **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml**.</span></span>


### <a name="get-required-er-configurations"></a><span data-ttu-id="0b106-245">Sækja umbeðnar ER-skilgreiningar</span><span class="sxs-lookup"><span data-stu-id="0b106-245">Get required ER configurations</span></span>

<span data-ttu-id="0b106-246">Ef þú hefur þegar lokið við í ferlið [Fá aðgang að lýsigögnum hugbúnaðar með notkun á ER-skilgreiningum](#access-application-metadata-by-using-an-er-configuration) fyrr í þessu efnisatriði, hefurðu nú þegar allar umbeðnar ER-skilgreiningar (skilgreiningar lýsigagna utanríkisviðskipta, líkans og vörpunar) í gildandi RCS-tilviki.</span><span class="sxs-lookup"><span data-stu-id="0b106-246">If you've already completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, you already have all the required ER configurations (the foreign trade metadata, model, and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="0b106-247">Í því tilfelli getur þú sleppt þessu ferli.</span><span class="sxs-lookup"><span data-stu-id="0b106-247">In that case, you can skip this procedure.</span></span>

1. <span data-ttu-id="0b106-248">Farðu í **Öll vinnusvæði \> Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="0b106-248">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="0b106-249">Veldu **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="0b106-249">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="0b106-250">Hladdu inn skilgreiningarskránum **Foreign trade metadata.xml**, **Foreign trade model.xml**, og **Foreign trade mapping.xml** sem endurtaka eftirfarandi keðju skrefa fyrir hverja þeirra:</span><span class="sxs-lookup"><span data-stu-id="0b106-250">Load the **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml** configuration files repeating the following chain of steps for each of them:</span></span>

    1. <span data-ttu-id="0b106-251">Veldu **Gengi**.</span><span class="sxs-lookup"><span data-stu-id="0b106-251">Select **Exchange**.</span></span>
    2. <span data-ttu-id="0b106-252">Veldu **Hlaða úr XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="0b106-252">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="0b106-253">Veldu **Fletta** og veldu skrá.</span><span class="sxs-lookup"><span data-stu-id="0b106-253">Select **Browse**, and select a file.</span></span>
    4. <span data-ttu-id="0b106-254">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0b106-254">Select **OK**.</span></span>

### <a name="register-the-connection-with-the-application"></a><span data-ttu-id="0b106-255">Skráðu tenginguna við forritið</span><span class="sxs-lookup"><span data-stu-id="0b106-255">Register the connection with the application</span></span>

1. <span data-ttu-id="0b106-256">Farðu í **Öll vinnusvæði \> Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="0b106-256">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="0b106-257">Veldu **Tengd forrit**.</span><span class="sxs-lookup"><span data-stu-id="0b106-257">Select **Connected applications**.</span></span>
3. <span data-ttu-id="0b106-258">Gakktu úr skugga um að skilgreint forrit sé byggt á Microsoft Azure og að það sé almennt aðgengilegt RCS-notendum.</span><span class="sxs-lookup"><span data-stu-id="0b106-258">Make sure that the configured application is based on Microsoft Azure, and that it is accessible in general to RCS users.</span></span> <span data-ttu-id="0b106-259">Núverandi RCS-notandi verður að hafa aðgang að skilgreinda forritinu sem verið er að skrá sem notandi þessa forrits í hlutverki sem veitir honum réttindi til að fá aðgang að lýsigögnum forritsins.</span><span class="sxs-lookup"><span data-stu-id="0b106-259">The current RCS user must have access to the configured application being registered as a user of this application in a role that gives them privileges to access the application's metadata.</span></span>
4. <span data-ttu-id="0b106-260">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="0b106-260">Select **New**.</span></span>
5. <span data-ttu-id="0b106-261">Í reitnum **Heiti** slærðu inn **MyConnectedApp** sem heiti tengds forrits.</span><span class="sxs-lookup"><span data-stu-id="0b106-261">In the **Name** field, enter **MyConnectedApp** as the name of the connected application.</span></span>
6. <span data-ttu-id="0b106-262">Í reitnum **Forrit** skaltu tilgreina slóð forritsins.</span><span class="sxs-lookup"><span data-stu-id="0b106-262">In the **Application** field, specify the URL of the application.</span></span>
7. <span data-ttu-id="0b106-263">Í reitnum **Leigjandi** skaltu tilgreina forritaveituna.</span><span class="sxs-lookup"><span data-stu-id="0b106-263">In the **Tenant** field, specify the provider of the application.</span></span>
8. <span data-ttu-id="0b106-264">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="0b106-264">Select **Save**.</span></span> 
9. <span data-ttu-id="0b106-265">Þegar þú skoðar tengingu við skilgreint forrit skaltu á síðunni **Tengja við ytra forrit** velja tengilinn **Velja hér til að tengja við valið ytra forrit**.</span><span class="sxs-lookup"><span data-stu-id="0b106-265">When you check the connection to the configured application, on the **Connect to remote application** page, select the **Select here to connect to selected remote application** link.</span></span> 
10. <span data-ttu-id="0b106-266">Veldu **Athuga tengingu** til að sannreyna aðgang að skilgreindu forriti.</span><span class="sxs-lookup"><span data-stu-id="0b106-266">Select **Check connection** to validate access to the configured application.</span></span>
11. <span data-ttu-id="0b106-267">Veljið **Loka**.</span><span class="sxs-lookup"><span data-stu-id="0b106-267">Select **Close**.</span></span>

<span data-ttu-id="0b106-268">Þegar þú hefur lokið þessu ferli og tengingarvottun tekist verða upplýsingar um útgáfu og leigjendur uppfærðar fyrir skilgreint forrit í núverandi hnitaneti.</span><span class="sxs-lookup"><span data-stu-id="0b106-268">After you complete this procedure and validation of the connection succeeds, the version and tenant details for the configured application will be updated in the current grid.</span></span>

### <a name="review-the-existing-model-mapping-configuration"></a><span data-ttu-id="0b106-269">Yfirfara fyrirliggjandi skilgreiningu fyrir líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="0b106-269">Review the existing model mapping configuration</span></span>

1. <span data-ttu-id="0b106-270">Farðu í **Öll vinnusvæði \> Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="0b106-270">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="0b106-271">Veldu **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="0b106-271">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="0b106-272">Í trénu skaltu velja **Líkan utanríkisviðskipta \> Vörpun utanríkisviðskipta**.</span><span class="sxs-lookup"><span data-stu-id="0b106-272">In the tree, select **Foreign trade model \> Foreign trade mapping**.</span></span>
4. <span data-ttu-id="0b106-273">Veldu flýtiflipann **Forkröfur**.</span><span class="sxs-lookup"><span data-stu-id="0b106-273">Select the **Prerequisites** FasTab.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0b106-274">Eins og er vísar þessi vörpun í skilgreiningu lýsigagna.</span><span class="sxs-lookup"><span data-stu-id="0b106-274">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="0b106-275">Lýsigögn forrits úr þessari skilgreiningu verða boðin á meðan þessi líkanavörpunin er sett upp.</span><span class="sxs-lookup"><span data-stu-id="0b106-275">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

4. <span data-ttu-id="0b106-276">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="0b106-276">Select **Designer**.</span></span>
5. <span data-ttu-id="0b106-277">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="0b106-277">Select **Designer**.</span></span>
6. <span data-ttu-id="0b106-278">Í trénu velurðu **Dynamics 365 for Operations \> Töflufærslur**.</span><span class="sxs-lookup"><span data-stu-id="0b106-278">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
7. <span data-ttu-id="0b106-279">Veljið **Bæta við rót**.</span><span class="sxs-lookup"><span data-stu-id="0b106-279">Select **Add root**.</span></span>
8. <span data-ttu-id="0b106-280">Sláið inn eða veldu gildi í reitnum **Tafla**.</span><span class="sxs-lookup"><span data-stu-id="0b106-280">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0b106-281">Eins og er vísar þessi vörpun í skilgreiningu lýsigagna.</span><span class="sxs-lookup"><span data-stu-id="0b106-281">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="0b106-282">Lýsigögn forrits úr þessari skilgreiningu verða boðin á meðan þessi líkanavörpunin er sett upp.</span><span class="sxs-lookup"><span data-stu-id="0b106-282">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

9. <span data-ttu-id="0b106-283">Veldu **Hætta við**.</span><span class="sxs-lookup"><span data-stu-id="0b106-283">Select **Cancel**.</span></span>

### <a name="assign-the-connected-application-to-a-model-mapping"></a><span data-ttu-id="0b106-284">Úthluta tengdu forriti á líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="0b106-284">Assign the connected application to a model mapping</span></span>

1. <span data-ttu-id="0b106-285">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="0b106-285">Select **Edit**.</span></span>
2. <span data-ttu-id="0b106-286">Í reitnum **Tengt forritasvæði** velurðu forritið **MyConnectedApp**.</span><span class="sxs-lookup"><span data-stu-id="0b106-286">In the **Connected application field**, select the **MyConnectedApp** application.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0b106-287">Þessi vörpun í lýsigögn valins tengds forrits.</span><span class="sxs-lookup"><span data-stu-id="0b106-287">This mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="0b106-288">Ef vöpun vísar í lýsigagnaskilgreininguna um leið og tengt forrit verða lýsigögn tengds forrits notuð.</span><span class="sxs-lookup"><span data-stu-id="0b106-288">If a mapping refers to the metadata configuration and the connected application at the same time, the metadata of the connected application will be used.</span></span>

3. <span data-ttu-id="0b106-289">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="0b106-289">Select **Designer**.</span></span>
4. <span data-ttu-id="0b106-290">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="0b106-290">Select **Designer**.</span></span>
5. <span data-ttu-id="0b106-291">Í trénu velurðu **Dynamics 365 for Operations \> Töflufærslur**.</span><span class="sxs-lookup"><span data-stu-id="0b106-291">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
6. <span data-ttu-id="0b106-292">Veljið **Bæta við rót**.</span><span class="sxs-lookup"><span data-stu-id="0b106-292">Select **Add root**.</span></span>
7. <span data-ttu-id="0b106-293">Sláið inn eða veldu gildi í reitnum **Tafla**.</span><span class="sxs-lookup"><span data-stu-id="0b106-293">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0b106-294">Á þessum tímapunkti eru fleiri en tvær forritstöflur boðnar þar sem þessi vörpun notar öll lýsigögn tengds forrits sem hefur verið úthlutað á það.</span><span class="sxs-lookup"><span data-stu-id="0b106-294">At this point, more than two application tables are offered, because this mapping uses all the metadata of the connected application that has been assigned to it.</span></span>

8. <span data-ttu-id="0b106-295">Veldu **Hætta við**.</span><span class="sxs-lookup"><span data-stu-id="0b106-295">Select **Cancel**.</span></span>
9. <span data-ttu-id="0b106-296">Veldu **Staðfesta**.</span><span class="sxs-lookup"><span data-stu-id="0b106-296">Select **Validate**.</span></span>

<span data-ttu-id="0b106-297">Núna hefur þú bundið þætti gagnalíkansins við atriði gagnagjafa sem er lýst með því að nota upplýsingar um lýsigögn forrits úr tengdu forriti sem hefue verið úthlutað á þessa vörpun.</span><span class="sxs-lookup"><span data-stu-id="0b106-297">You've now bound elements of the data model to items of the data sources that are described by using details of the metadata of the connected application that has been assigned to this mapping.</span></span>

<span data-ttu-id="0b106-298">Þegar þú verður að meta þessa líkanavörpun með því að nota lýsigögn annarrar útgáfu forrits skaltu skrá annað tengt forrit, úthluta því á þessa líkanavörpun og sannprófa það gegn nýjum lýsigögnunum.</span><span class="sxs-lookup"><span data-stu-id="0b106-298">When you must evaluate this model mapping by using the metadata of a different version of the application, register another connected application, assign it to this model mapping, and validate it against the new metadata.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0b106-299">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="0b106-299">Additional resources</span></span>

<span data-ttu-id="0b106-300">Að öðrum kosti getur þú spilað verkleiðbeiningarnar **Undirbúa lýsigögn forrits sem hægt er að nota í RCS** í forritinu ásamt **Fá aðgang að lýsigögnum forrits með því að nota ER-stillingu** og **Fá aðgang að lýsigögnum forrits með því að nota tengd forrit** í RCS.</span><span class="sxs-lookup"><span data-stu-id="0b106-300">Alternatively, you can play the **Prepare application metadata that can be used in RCS** task guide in the application as as well as the **Access application metadata by using an ER configuration** and **Access application metadata by using connected applications** task guides in RCS.</span></span> <span data-ttu-id="0b106-301">Hægt er að sækja þessar verkleiðbeiningar af síðunni [Verkleiðbeiningar fyrir rafræna skýrslugerð Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739).</span><span class="sxs-lookup"><span data-stu-id="0b106-301">These task guides can be downloaded from the [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]