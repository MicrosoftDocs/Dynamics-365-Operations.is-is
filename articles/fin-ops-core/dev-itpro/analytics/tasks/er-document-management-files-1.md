---
title: Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum(Hluti 1 - Undirbúa gagnalíkan)
description: Í þessu efni er útskýrt hvernig á að skilgreina snið rafrænnar skýrslugerðar til að nota skrár skjalastjórnunar (viðhengi) í úttaki rafrænnar skýrslugerðar. (Hluti 1)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6b265c9af0635e6c9fb6295f7e8e4e353b2a5ba5
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754939"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a><span data-ttu-id="705a3-104">Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum(Hluti 1 - Undirbúa gagnalíkan)</span><span class="sxs-lookup"><span data-stu-id="705a3-104">ER Use Document Management files in format outputs (Part 1 - Prepare data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="705a3-105">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) svo það noti skrár skjalastjórnunar (viðhengi) í rafrænar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="705a3-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="705a3-106">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="705a3-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="705a3-107">Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu „Stofna skilgreiningarveitu og merkja hana sem virka”.</span><span class="sxs-lookup"><span data-stu-id="705a3-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="705a3-108">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="705a3-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="705a3-109">Fá aðgang að lista yfir skilgreiningar sem Microsoft veitir</span><span class="sxs-lookup"><span data-stu-id="705a3-109">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="705a3-110">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="705a3-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="705a3-111">Gakktu úr skugga um að „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="705a3-111">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="705a3-112">veitandi sé tiltæk og merkt Virk.</span><span class="sxs-lookup"><span data-stu-id="705a3-112">provider is available and marked as active.</span></span>  

2. <span data-ttu-id="705a3-113">Velja Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="705a3-113">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="705a3-114">veita.</span><span class="sxs-lookup"><span data-stu-id="705a3-114">provider.</span></span>
3. <span data-ttu-id="705a3-115">Smella á Geymslur.</span><span class="sxs-lookup"><span data-stu-id="705a3-115">Click Repositories.</span></span>

    <span data-ttu-id="705a3-116">Sleppa önnur þrep í núverandi undirverki ef gagnasafn af gerð 'Rekstrartilföngum' er þegar til.</span><span class="sxs-lookup"><span data-stu-id="705a3-116">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  

4. <span data-ttu-id="705a3-117">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="705a3-117">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="705a3-118">Í reitnum gerð gagnasafns fyrir skilgreiningar, færðu inn "rekstrartilföng".</span><span class="sxs-lookup"><span data-stu-id="705a3-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="705a3-119">Smellið á Stofna gagnasafn.</span><span class="sxs-lookup"><span data-stu-id="705a3-119">Click Create repository.</span></span>
7. <span data-ttu-id="705a3-120">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="705a3-120">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="705a3-121">Sækja Líkan Reiknings viðskiptavinar-skilgreiningar sem Microsoft veitir</span><span class="sxs-lookup"><span data-stu-id="705a3-121">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="705a3-122">Smellt er á Sýna síur.</span><span class="sxs-lookup"><span data-stu-id="705a3-122">Click Show filters.</span></span>
2. <span data-ttu-id="705a3-123">Nota eftirfarandi síur: færið Inn gildi síu "Rekstrartilföngum" síu á svæðið "Heiti" með því að nota í "byrjar á" virknitákn síu; Færa inn gildi síu "" á reitnum "Lýsing" með því að nota "byrjar á" virknitákn síu.</span><span class="sxs-lookup"><span data-stu-id="705a3-123">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="705a3-124">Smellt er á Sýna síur.</span><span class="sxs-lookup"><span data-stu-id="705a3-124">Click Show filters.</span></span>
4. <span data-ttu-id="705a3-125">Smellt er á Opin.</span><span class="sxs-lookup"><span data-stu-id="705a3-125">Click Open.</span></span>
5. <span data-ttu-id="705a3-126">Í trénu, veljið 'Customer invoice model'.</span><span class="sxs-lookup"><span data-stu-id="705a3-126">In the tree, select 'Customer invoice model'.</span></span>

    <span data-ttu-id="705a3-127">Velja skilgreiningu líkans 'líkan reiknings viðskiptavinar' til að flytja það inn.</span><span class="sxs-lookup"><span data-stu-id="705a3-127">Select the model configuration 'Customer invoice model' to import it.</span></span>  

6. <span data-ttu-id="705a3-128">Smelltu á Flytja inn.</span><span class="sxs-lookup"><span data-stu-id="705a3-128">Click Import.</span></span>

    <span data-ttu-id="705a3-129">Smelltu á innflutning fyrir útgáfu 1 fyrir valda skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="705a3-129">Click Import for version 1 of the selected configuration.</span></span>  

7. <span data-ttu-id="705a3-130">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="705a3-130">Click Yes.</span></span>
8. <span data-ttu-id="705a3-131">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="705a3-131">Close the page.</span></span>
9. <span data-ttu-id="705a3-132">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="705a3-132">Close the page.</span></span>
10. <span data-ttu-id="705a3-133">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="705a3-133">Click Reporting configurations.</span></span>
11. <span data-ttu-id="705a3-134">Í trénu, veljið 'Customer invoice model'.</span><span class="sxs-lookup"><span data-stu-id="705a3-134">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="705a3-135">Stofna afleitt líkan til að styðja aðgang að skrám Skjalastjórnunar.</span><span class="sxs-lookup"><span data-stu-id="705a3-135">Create the derived model to support access to the Document Management files.</span></span>
<span data-ttu-id="705a3-136">Þú munt stofna okkar eigin skilgreiningu á líkani reiknings viðskiptavinar og fá það úr skilgreiningu sem Microsoft veitir.</span><span class="sxs-lookup"><span data-stu-id="705a3-136">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="705a3-137">Þú munt nota þessa skilgreiningu til að innleiða aðgang að skrám Skjalastjórnunar og gera þau tiltæk fyrir rafræn skjöl sem þú munt stofna á grundvelli þessa líkans.</span><span class="sxs-lookup"><span data-stu-id="705a3-137">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="705a3-138">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="705a3-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="705a3-139">Í svæðinu Nýtt, veljið 'Leiða af nafni: líkan reiknings viðskiptavinar, Microsoft'.</span><span class="sxs-lookup"><span data-stu-id="705a3-139">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="705a3-140">Í svæðið Heiti, Færðu inn 'líkan reiknings viðskiptavinar (sérstillt)'.</span><span class="sxs-lookup"><span data-stu-id="705a3-140">In the Name field, type 'Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="705a3-141">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="705a3-141">Click Create configuration.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]