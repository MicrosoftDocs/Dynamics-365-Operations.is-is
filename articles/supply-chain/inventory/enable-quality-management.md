---
title: Virkja stjórnun gæða og ósamkvæmni
description: Í þessu efnisatriði er að finna yfirlit yfir ferlið við uppsetningu og skilgreiningu stjórnunareiginleika gæða og ósamkvæmni í Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67d5da648e31d07d054246f5d308a6c6cdeb506c
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956255"
---
# <a name="enable-quality-and-nonconformance-management"></a><span data-ttu-id="8190d-103">Virkja stjórnun gæða og ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="8190d-103">Enable quality and nonconformance management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8190d-104">Í þessu efnisatriði er að finna yfirlit yfir ferlið við uppsetningu og skilgreiningu stjórnunareiginleika gæða og ósamkvæmni í Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8190d-104">This topic provides an overview of the process for setting up and configuring quality and nonconformance management features in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="enable-quality-and-nonconformance-management"></a><span data-ttu-id="8190d-105"><a name="enable-qm">Virkja stjórnun gæða og ósamkvæmni</a></span><span class="sxs-lookup"><span data-stu-id="8190d-105"><a name="enable-qm"></a>Enable quality and nonconformance management</span></span>

<span data-ttu-id="8190d-106">Fylgið eftirfarandi skrefum til að virkja gæðastjórnun í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="8190d-106">Follow these steps to enable quality management on your system.</span></span>

1. <span data-ttu-id="8190d-107">Farðu í **Birgðastjórnun \> Uppsetning \> Færibreytur birgða- og vöruhúsakerfis**.</span><span class="sxs-lookup"><span data-stu-id="8190d-107">Go to **Inventory management \> Setup \> Inventory and warehouse management parameters**.</span></span>
1. <span data-ttu-id="8190d-108">Í flipanum **Gæðastjórnun** skal stilla valkostinn **Nota gæðastjórnun** á *Já*.</span><span class="sxs-lookup"><span data-stu-id="8190d-108">On the **Quality management** tab, set the **Use quality management** option to *Yes*.</span></span>
1. <span data-ttu-id="8190d-109">Í reitinn **tímagjald** skal færa inn tímagjald fyrir vinnu í gjaldmiðli landsins.</span><span class="sxs-lookup"><span data-stu-id="8190d-109">In the **Hourly rate** field, enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="8190d-110">Tímagjaldið er notuð til að reikna kostnað fyrir aðgerðir sem tengjast ósamkvæmni.</span><span class="sxs-lookup"><span data-stu-id="8190d-110">The hourly rate is used to calculate costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="8190d-111">Tímagjaldið og reiknaður kostnaður veita tilvísunarupplýsingar fyrir ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="8190d-111">The hourly rate and calculated costs provide reference information for a nonconformance.</span></span> <span data-ttu-id="8190d-112">Þau eiga ekki í samskiptum við aðrar aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="8190d-112">They don't interact with other functionality.</span></span>
1. <span data-ttu-id="8190d-113">Veljið **Uppsetning skýrslu**.</span><span class="sxs-lookup"><span data-stu-id="8190d-113">Select **Report setup**.</span></span>
1. <span data-ttu-id="8190d-114">Bætið við nýjum línum fyrir hinar ýmsu skýrslugerðir og veljið gerð skjals sem á að nota fyrir hverja skýrslu.</span><span class="sxs-lookup"><span data-stu-id="8190d-114">Add new lines for the various report types, and select the type of document to use for each report.</span></span>
1. <span data-ttu-id="8190d-115">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8190d-115">Close the page.</span></span>
1. <span data-ttu-id="8190d-116">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8190d-116">Close the page.</span></span>

## <a name="quality-management-configuration-process"></a><span data-ttu-id="8190d-117">Skilgreiningarferli gæðastjórnunar</span><span class="sxs-lookup"><span data-stu-id="8190d-117">Quality management configuration process</span></span>

<span data-ttu-id="8190d-118">Áður en hægt er að byrja að nota eiginleika gæðastjórnunar og búa til gæðapantanir þarf að skilgreina kerfið og forkröfur.</span><span class="sxs-lookup"><span data-stu-id="8190d-118">Before you can start to use the quality management features and generate quality orders, you must configure the system and prerequisites.</span></span> <span data-ttu-id="8190d-119">Hér er listi yfir skrefin sem eru nauðsynleg til að stilla gæðastjórnun.</span><span class="sxs-lookup"><span data-stu-id="8190d-119">Here is a list of the steps that are required to configure quality management.</span></span>

1. <span data-ttu-id="8190d-120">[Virkja stjórnun gæða og ósamkvæmni](#enable-qm)</span><span class="sxs-lookup"><span data-stu-id="8190d-120">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="8190d-121">Valfrjálst: [Stilla prófunartæki](quality-test-instruments.md).</span><span class="sxs-lookup"><span data-stu-id="8190d-121">Optional: [Configure test instruments](quality-test-instruments.md).</span></span>
1. <span data-ttu-id="8190d-122">[Skilgreina próf](quality-tests.md).</span><span class="sxs-lookup"><span data-stu-id="8190d-122">[Configure tests](quality-tests.md).</span></span>
1. <span data-ttu-id="8190d-123">[Skilgreina prófunarbreytur og útkomur](quality-test-variables.md).</span><span class="sxs-lookup"><span data-stu-id="8190d-123">[Configure test variables and outcomes](quality-test-variables.md).</span></span>
1. <span data-ttu-id="8190d-124">[Skilgreina prófunarflokka](quality-test-groups.md).</span><span class="sxs-lookup"><span data-stu-id="8190d-124">[Configure test groups](quality-test-groups.md).</span></span>
1. <span data-ttu-id="8190d-125">Valfrjálst: [Stilla gæðaflokka og tengja við vörur](quality-groups.md).</span><span class="sxs-lookup"><span data-stu-id="8190d-125">Optional: [Configure quality groups, and link to products](quality-groups.md).</span></span>
1. <span data-ttu-id="8190d-126">Valfrjálst: [Stilla gæðatengingar](quality-associations.md).</span><span class="sxs-lookup"><span data-stu-id="8190d-126">Optional: [Configure quality associations](quality-associations.md).</span></span>

<span data-ttu-id="8190d-127">Þegar skilgreiningu er lokið er hægt að byrja að stofna og vinna úr gæðapöntunum.</span><span class="sxs-lookup"><span data-stu-id="8190d-127">After the configuration is completed, you can start to create and process quality orders.</span></span> <span data-ttu-id="8190d-128">Frekari upplýsingar um hvernig á að búa til og vinna með gæðapantanir er að finna í [Gæðapantanir](quality-orders.md).</span><span class="sxs-lookup"><span data-stu-id="8190d-128">For more information about how to create and work with quality orders, see [Quality orders](quality-orders.md).</span></span>

## <a name="nonconformance-management-configuration-process"></a><span data-ttu-id="8190d-129">Skilgreiningarferli fyrir stjórnun ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="8190d-129">Nonconformance management configuration process</span></span>

<span data-ttu-id="8190d-130">Áður en hægt er að byrja að nota eiginleika fyrir stjórnun ósamkvæmni og búa til ósamkvæmni þarf að skilgreina kerfið og forkröfur.</span><span class="sxs-lookup"><span data-stu-id="8190d-130">Before you can start to use the nonconformance management features and generate nonconformances, you must configure the system and prerequisites.</span></span> <span data-ttu-id="8190d-131">Hér er listi yfir skrefin sem eru nauðsynleg til að stilla stjórnun ósamkvæmis.</span><span class="sxs-lookup"><span data-stu-id="8190d-131">Here is a list of the steps that are required to configure nonconformance management.</span></span>

1. <span data-ttu-id="8190d-132">[Virkja stjórnun gæða og ósamkvæmni](#enable-qm)</span><span class="sxs-lookup"><span data-stu-id="8190d-132">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="8190d-133">[Stilla starfskrafta sem bera ábyrgð á að samþykkja ósamkvæmi](quality-responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="8190d-133">[Configure workers who are responsible for approving nonconformances](quality-responsible-workers.md).</span></span>
1. <span data-ttu-id="8190d-134">[Skilgreina gerðir vandamála](quality-problem-types.md).</span><span class="sxs-lookup"><span data-stu-id="8190d-134">[Configure problem types](quality-problem-types.md).</span></span>
1. <span data-ttu-id="8190d-135">[Skilgreina biðgeymslusvæði](quality-quarantine-zones.md).</span><span class="sxs-lookup"><span data-stu-id="8190d-135">[Configure quarantine zones](quality-quarantine-zones.md).</span></span>
1. <span data-ttu-id="8190d-136">[Skilgreina greiningargerðir](quality-diagnostic-types.md).</span><span class="sxs-lookup"><span data-stu-id="8190d-136">[Configure diagnostic types](quality-diagnostic-types.md).</span></span>
1. <span data-ttu-id="8190d-137">[Skilgreina aðgerðir](quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="8190d-137">[Configure operations](quality-operations.md).</span></span>
1. <span data-ttu-id="8190d-138">Valfrjálst: [Stilla gæðagjöld](quality-charges.md).</span><span class="sxs-lookup"><span data-stu-id="8190d-138">Optional: [Configure quality charges](quality-charges.md).</span></span>

<span data-ttu-id="8190d-139">Þegar skilgreiningunni er lokið er hægt að byrja að stofna og vinna úr ósamkvæmi.</span><span class="sxs-lookup"><span data-stu-id="8190d-139">After the configuration is completed, you can start to create and process nonconformances.</span></span> <span data-ttu-id="8190d-140">Nánari upplýsingar um hvernig á að stofna og vinna með ósamkvæmi eru í [Stofna og meðhöndla ósamkvæmi](tasks/create-process-non-conformance.md).</span><span class="sxs-lookup"><span data-stu-id="8190d-140">For more information about how to create and work with nonconformances, see [Create and process nonconformances](tasks/create-process-non-conformance.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8190d-141">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="8190d-141">Additional resources</span></span>

- [<span data-ttu-id="8190d-142">Gæðastjórnunaryfirlit</span><span class="sxs-lookup"><span data-stu-id="8190d-142">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="8190d-143">Virkja stjórnun gæða og ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="8190d-143">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="8190d-144">Gæðastjórnun fyrir vöruhúsaferli</span><span class="sxs-lookup"><span data-stu-id="8190d-144">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
