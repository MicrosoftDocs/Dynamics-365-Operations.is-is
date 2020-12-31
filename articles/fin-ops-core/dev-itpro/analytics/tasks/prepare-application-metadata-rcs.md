---
title: Undirbúa lýsigögn umsóknar til notkunar í RCS
description: Skrefin í þessu efni útskýra hvernig notandi getur búið til nýjar skilgreiningar rafrænnar skýrslugerðar (ER) sem innihalda lýsigögn forritsins til að setja upp ER-líkanavörpunarskilgreiningar í Regulatory Configuration Service (RCS).
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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dbc1ca45a39f2a5c3309276f9e2f5d2b7d2ba5f7
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684092"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a><span data-ttu-id="f53e2-103">Undirbúa lýsigögn umsóknar til notkunar í RCS</span><span class="sxs-lookup"><span data-stu-id="f53e2-103">Prepare application metadata to be used in RCS</span></span>
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f53e2-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki kerfisstjóra eða þróunaraðila rafrænnar skýrslulausnar getur búið til nýjar skilgreiningar rafrænnar skýrslugerðar (ER) sem innihalda lýsigögn forritsins til að setja upp ER-líkanavörpunarskilgreiningar í Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="f53e2-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains application metadata for designing ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="f53e2-105">Þessi skilgreining verður notuð til að setja upp sýnisskilgreiningu ER-líkanavörpunar sem er búið til í þessu dæmi verður notað til að fá aðgang að utanríkisviðskiptum.</span><span class="sxs-lookup"><span data-stu-id="f53e2-105">This configuration will be used for designing a sample ER model mapping configuration to access foreign trade transactions.</span></span> <span data-ttu-id="f53e2-106">Í þessu dæmi muntu stofna skilgreiningu fyrir sýnifyrirtækið, Litware, Inc. Þessi skref má framkvæma í hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="f53e2-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company.</span></span> <span data-ttu-id="f53e2-107">Til að ljúka þessum skrefum verður fyrst að ljúka skrefunum í efninu [Stofna skilgreiningaveitur og merkja þær sem virkar](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="f53e2-107">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f53e2-108">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="f53e2-108">Prerequisites</span></span>
1.    <span data-ttu-id="f53e2-109">Farðu í **Fyrirtækisstjórnun** > **Vinnusvæði** > **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="f53e2-109">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2.    <span data-ttu-id="f53e2-110">Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt **Virk**.</span><span class="sxs-lookup"><span data-stu-id="f53e2-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="f53e2-111">Ef þú sérð skilgreiningarveituna ekki skaltu klára skrefin í ferlinu [Stofna skilgreiningaveitur og merkja þær sem virkar](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="f53e2-111">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3.    <span data-ttu-id="f53e2-112">Smelltu á **Skilgreiningu lýsigagna**.</span><span class="sxs-lookup"><span data-stu-id="f53e2-112">Click **Metadata configurations**.</span></span> 
4.    <span data-ttu-id="f53e2-113">Gerðu ráð fyrir að RCS verði notað til að setja upp ER-lausn fyrir forritið Finance and Operations, sem verður notuð til að búa til rafræn skjöl sem innihalda upplýsingar úr umdæmi utanríkisviðskipta.</span><span class="sxs-lookup"><span data-stu-id="f53e2-113">Assume that RCS will be used to design an ER solution for a Finance and Operation application that will generate electronic documents that contain information from foreign trade business domain.</span></span> <span data-ttu-id="f53e2-114">Til að tilgreina vörpun milli ER-gagnalíkans og uppruna nauðsynlegra gagna, verðuum við að hafa aðgang að forritslýsigögnum í RCS fyrir forritið Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f53e2-114">To specify the mapping between ER data model and sources of required data, in RCS we need to have access to metadata of the Finance and Operation application.</span></span> <span data-ttu-id="f53e2-115">Þess vegna er hluti af uppsetningu á ER-lausn að við skilgreinum nýja ER-lýsigagnaskilgreiningu sem innihalda öll lýsigögnin sem þarf eins og stendur til að mynda ER-skýrslur fyrir valið viðskiptalén.</span><span class="sxs-lookup"><span data-stu-id="f53e2-115">Therefore, as part of designing ER solution we configure a new ER metadata configuration containing all metadata that is currently required for generation ER reports for selected business domain.</span></span> 

## <a name="add-metadata-configuration"></a><span data-ttu-id="f53e2-116">Bæta við skilgreiningu lýsigagna</span><span class="sxs-lookup"><span data-stu-id="f53e2-116">Add metadata configuration</span></span> 
1.    <span data-ttu-id="f53e2-117">Smellið á **Stofna skilgreiningu** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="f53e2-117">Click **Create configuration** to open the drop dialog.</span></span> 
2.    <span data-ttu-id="f53e2-118">Í reitinn **Heiti** slærðu inn „Lýsigögn utanríkisverslunar“.</span><span class="sxs-lookup"><span data-stu-id="f53e2-118">In the **Name** field, type 'Foreign trade metadata'.</span></span> 
3.    <span data-ttu-id="f53e2-119">Smellið á **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="f53e2-119">Click **Create configuration**.</span></span> 
4.    <span data-ttu-id="f53e2-120">Smellið á **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="f53e2-120">Click **Designer**.</span></span> 
5.    <span data-ttu-id="f53e2-121">Smelltu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="f53e2-121">Click **Add**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f53e2-122">Þú getur valið öll lýsigögn fyrir allt forritið eða fyrir valin líkön eða valdar einingar.</span><span class="sxs-lookup"><span data-stu-id="f53e2-122">You can select all metadata for the entire application or selected models or selected modules.</span></span> <span data-ttu-id="f53e2-123">Hafðu í huga að í þessu dæmi verður eftirfarandi lýsigögnum sjálfkrafa bætt við: töflum yfir skrár, talningum og lengd gagnategunda.</span><span class="sxs-lookup"><span data-stu-id="f53e2-123">Be aware that in this case the following metadata will be automatically added: tables of records, enumerations, and extended data types.</span></span> <span data-ttu-id="f53e2-124">Þegar fleiri tegundir lýsigagna er þörf verður að bæta þeim við á handvirkan hátt.</span><span class="sxs-lookup"><span data-stu-id="f53e2-124">When additional types of metadata are needed, they must be added manually.</span></span> 
 
<span data-ttu-id="f53e2-125">Við erum með lýsigögn sem tengjast utanríkisviðskiptafærslum með því að velja atriði lýsigagna á handvirkan hátt.</span><span class="sxs-lookup"><span data-stu-id="f53e2-125">We have some foreign trade transactions related metadata by selecting metadata items manually.</span></span> 
  
6.    <span data-ttu-id="f53e2-126">Smelltu **Bæta við gagnagjafa**.</span><span class="sxs-lookup"><span data-stu-id="f53e2-126">Click **Add data source**.</span></span> 
7.    <span data-ttu-id="f53e2-127">Smelltu á **Töflufærslur**.</span><span class="sxs-lookup"><span data-stu-id="f53e2-127">Click **Table records**.</span></span> 
8.    <span data-ttu-id="f53e2-128">Notaðu flýtiafmörkun til að sía í reitnum **Heiti** með gildinu „Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="f53e2-128">Use the Quick Filter to filter on the **Name** field with a value of 'Intrastat'.</span></span> 
9.    <span data-ttu-id="f53e2-129">Veldu **Intrastat**-töflu.</span><span class="sxs-lookup"><span data-stu-id="f53e2-129">Select the **Intrastat** table record.</span></span> 
10.    <span data-ttu-id="f53e2-130">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="f53e2-130">Click **OK**.</span></span>
  
<span data-ttu-id="f53e2-131">Við bættum við lýsigögnum um Intrastat-skráatöfluna.</span><span class="sxs-lookup"><span data-stu-id="f53e2-131">We added metadata information about the Intrastat table of records.</span></span> 
  
11.    <span data-ttu-id="f53e2-132">Í trénu víkkarðu út **Töflufærslur Intrastat**\>**Vensl**.</span><span class="sxs-lookup"><span data-stu-id="f53e2-132">In the tree, expand **Table records Intrastat**\>**Relations**.</span></span> 
12.    <span data-ttu-id="f53e2-133">Í trénu velurðu **Töflufærslur Intrastat**\>**Vensl\IntrastatCommodity (Töflufærslur EcoResCategory)**.</span><span class="sxs-lookup"><span data-stu-id="f53e2-133">In the tree, select **Table records Intrastat**\>**Relations\IntrastatCommodity (Table records EcoResCategory)**.</span></span>     
13.    <span data-ttu-id="f53e2-134">Smelltu á **Bæta við lýsigögnum**.</span><span class="sxs-lookup"><span data-stu-id="f53e2-134">Click **Add metadata**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f53e2-135">Bæta verður lýsigögnum um nauðsynleg vensl fyrir valda skráatöflu við á handvirkan hátt.</span><span class="sxs-lookup"><span data-stu-id="f53e2-135">Metadata about required relations for selected table of records must be added manually.</span></span> 
  
16.    <span data-ttu-id="f53e2-136">Smelltu **Bæta við gagnagjafa**.</span><span class="sxs-lookup"><span data-stu-id="f53e2-136">Click **Add data source**.</span></span> 
17.    <span data-ttu-id="f53e2-137">Smelltu á **Upptalning**.</span><span class="sxs-lookup"><span data-stu-id="f53e2-137">Click **Enumeration**.</span></span> 
18.    <span data-ttu-id="f53e2-138">Notaðu flýtiafmörkun til að sía í reitnum **Heiti** með gildinu „IntrastatDirection“.</span><span class="sxs-lookup"><span data-stu-id="f53e2-138">Use the Quick Filter to filter on the **Name** field with a value of 'IntrastatDirection'.</span></span> 
19.    <span data-ttu-id="f53e2-139">Veldu skrána **IntrastatDirection upptalning**.</span><span class="sxs-lookup"><span data-stu-id="f53e2-139">Select the **IntrastatDirection enumeration** record.</span></span> 
20.    <span data-ttu-id="f53e2-140">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="f53e2-140">Click **OK**.</span></span> 
21.    <span data-ttu-id="f53e2-141">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="f53e2-141">Click **Save**.</span></span>  
22.    <span data-ttu-id="f53e2-142">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f53e2-142">Close the page.</span></span> 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a><span data-ttu-id="f53e2-143">Ljúktu drögunum að útgáfu skilgreiningar lýsigagna</span><span class="sxs-lookup"><span data-stu-id="f53e2-143">Complete the draft version of metadata configuration</span></span>
1.    <span data-ttu-id="f53e2-144">Smelltu á **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="f53e2-144">Click **Change status**.</span></span> 
2.    <span data-ttu-id="f53e2-145">Smelltu á **Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="f53e2-145">Click **Complete**.</span></span> 
3.    <span data-ttu-id="f53e2-146">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="f53e2-146">Click **OK**.</span></span> 
4.    <span data-ttu-id="f53e2-147">Veldu fullgerða útgáfu **1**.</span><span class="sxs-lookup"><span data-stu-id="f53e2-147">Select the completed version **1**.</span></span> 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a><span data-ttu-id="f53e2-148">Flyttu út fullgerða útgáfu lýsigagnauppsetningar úr forritinu sem XML-skrá</span><span class="sxs-lookup"><span data-stu-id="f53e2-148">Export the completed version of metadata configuration from application as XML file</span></span>
1.    <span data-ttu-id="f53e2-149">Smelltu á **Skipta út**.</span><span class="sxs-lookup"><span data-stu-id="f53e2-149">Click **Exchange**.</span></span> 
2.    <span data-ttu-id="f53e2-150">Smelltu á **Flytja út sem XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="f53e2-150">Click **Export as XML file**.</span></span> 
3.    <span data-ttu-id="f53e2-151">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="f53e2-151">Click **OK**.</span></span> 
    
<span data-ttu-id="f53e2-152">Uppsett ER lýsigagnaskilgreining er vistuð sem XML-skrá sem hægt er að flytja inn í RCS og notuð sem upplýsingaveita um lýsigögn fyrir viðskiptalén utanríkisviðskipta.</span><span class="sxs-lookup"><span data-stu-id="f53e2-152">The created ER metadata configuration has been saved as XML file that can be imported to RCS and used as the source of information about metadata for the foreign trade business domain.</span></span> <span data-ttu-id="f53e2-153">Samkvæmt þessum upplýsingum getum við tilgreint vörpun á milli lýsigagna forritsins og ER-gagnalíkansins.</span><span class="sxs-lookup"><span data-stu-id="f53e2-153">Based on this information, we can specify the mapping between application metadata and ER data model.</span></span>
