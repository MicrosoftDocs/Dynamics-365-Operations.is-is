--- 
title: "Undirbúa gagnalíkan til að nota skjalastjórnunarskrár í sniðsúttökum rafrænnar skýrslugerðar"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) svo það noti skrár skjalastjórnunar (viðhengi) í rafrænar skýrslur."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: fcafaf17315f54594116a143f36e924bc705d839
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2018

---
# <a name="prepare-data-models-to-use-document-management-files-in-er-output"></a><span data-ttu-id="8598f-103">Undirbúa gagnalíkan til að nota skjalastjórnunarskrár í sniðsúttökum rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="8598f-103">Prepare data models to use Document Management files in ER output</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8598f-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) svo það noti skrár skjalastjórnunar (viðhengi) í rafrænar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="8598f-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="8598f-105">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="8598f-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="8598f-106">Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu "Stofna skilgreiningarveitu og merkja hana sem virka".</span><span class="sxs-lookup"><span data-stu-id="8598f-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="8598f-107">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="8598f-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="8598f-108">Fá aðgang að lista yfir skilgreiningar sem Microsoft veitir</span><span class="sxs-lookup"><span data-stu-id="8598f-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="8598f-109">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="8598f-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="8598f-110">Gakktu úr skugga um að „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="8598f-110">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="8598f-111">veitandi sé tiltæk og merkt Virk.</span><span class="sxs-lookup"><span data-stu-id="8598f-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="8598f-112">Velja Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="8598f-112">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="8598f-113">veita.</span><span class="sxs-lookup"><span data-stu-id="8598f-113">provider.</span></span>
3. <span data-ttu-id="8598f-114">Smella á Geymslur.</span><span class="sxs-lookup"><span data-stu-id="8598f-114">Click Repositories.</span></span>
    * <span data-ttu-id="8598f-115">Sleppa önnur þrep í núverandi undirverki ef gagnasafn af gerð 'Rekstrartilföngum' er þegar til.</span><span class="sxs-lookup"><span data-stu-id="8598f-115">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="8598f-116">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="8598f-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="8598f-117">Í reitnum gerð gagnasafns fyrir skilgreiningar, færðu inn "rekstrartilföng".</span><span class="sxs-lookup"><span data-stu-id="8598f-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="8598f-118">Smellið á Stofna gagnasafn.</span><span class="sxs-lookup"><span data-stu-id="8598f-118">Click Create repository.</span></span>
7. <span data-ttu-id="8598f-119">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="8598f-119">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="8598f-120">Sækja Líkan Reiknings viðskiptavinar-skilgreiningar sem Microsoft veitir</span><span class="sxs-lookup"><span data-stu-id="8598f-120">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="8598f-121">Smellt er á Sýna síur.</span><span class="sxs-lookup"><span data-stu-id="8598f-121">Click Show filters.</span></span>
2. <span data-ttu-id="8598f-122">Nota eftirfarandi síur: færið Inn gildi síu "Rekstrartilföngum" síu á svæðið "Heiti" með því að nota í "byrjar á" virknitákn síu; Færa inn gildi síu "" á reitnum "Lýsing" með því að nota "byrjar á" virknitákn síu.</span><span class="sxs-lookup"><span data-stu-id="8598f-122">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="8598f-123">Smellt er á Sýna síur.</span><span class="sxs-lookup"><span data-stu-id="8598f-123">Click Show filters.</span></span>
4. <span data-ttu-id="8598f-124">Smellt er á Opin.</span><span class="sxs-lookup"><span data-stu-id="8598f-124">Click Open.</span></span>
5. <span data-ttu-id="8598f-125">Í trénu, veljið 'Customer invoice model'.</span><span class="sxs-lookup"><span data-stu-id="8598f-125">In the tree, select 'Customer invoice model'.</span></span>
    * <span data-ttu-id="8598f-126">Velja skilgreiningu líkans 'líkan reiknings viðskiptavinar' til að flytja það inn.</span><span class="sxs-lookup"><span data-stu-id="8598f-126">Select the model configuration 'Customer invoice model' to import it.</span></span>  
6. <span data-ttu-id="8598f-127">Smelltu á Flytja inn.</span><span class="sxs-lookup"><span data-stu-id="8598f-127">Click Import.</span></span>
    * <span data-ttu-id="8598f-128">Smelltu á innflutning fyrir útgáfu 1 fyrir valda skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="8598f-128">Click Import for version 1 of the selected configuration.</span></span>  
7. <span data-ttu-id="8598f-129">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="8598f-129">Click Yes.</span></span>
8. <span data-ttu-id="8598f-130">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8598f-130">Close the page.</span></span>
9. <span data-ttu-id="8598f-131">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8598f-131">Close the page.</span></span>
10. <span data-ttu-id="8598f-132">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="8598f-132">Click Reporting configurations.</span></span>
11. <span data-ttu-id="8598f-133">Í trénu, veljið 'Customer invoice model'.</span><span class="sxs-lookup"><span data-stu-id="8598f-133">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="8598f-134">Stofna afleitt líkan til að styðja aðgang að skrám Skjalastjórnunar.</span><span class="sxs-lookup"><span data-stu-id="8598f-134">Create the derived model to support access to the Document Management files.</span></span>
    * <span data-ttu-id="8598f-135">Þú munt stofna okkar eigin skilgreiningu á líkani reiknings viðskiptavinar og fá það úr skilgreiningu sem Microsoft veitir.</span><span class="sxs-lookup"><span data-stu-id="8598f-135">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="8598f-136">Þú munt nota þessa skilgreiningu til að innleiða aðgang að skrám Skjalastjórnunar og gera þau tiltæk fyrir rafræn skjöl sem þú munt stofna á grundvelli þessa líkans.</span><span class="sxs-lookup"><span data-stu-id="8598f-136">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="8598f-137">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="8598f-137">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="8598f-138">Í svæðinu Nýtt, veljið 'Leiða af nafni: líkan reiknings viðskiptavinar, Microsoft'.</span><span class="sxs-lookup"><span data-stu-id="8598f-138">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="8598f-139">Í svæðið Heiti, Færðu inn 'líkan reiknings viðskiptavinar (sérstillt)'.</span><span class="sxs-lookup"><span data-stu-id="8598f-139">In the Name field, type 'Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="8598f-140">Líkan Reiknings viðskiptavinar (sérstillt)</span><span class="sxs-lookup"><span data-stu-id="8598f-140">Customer invoice model (custom)</span></span>  
4. <span data-ttu-id="8598f-141">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="8598f-141">Click Create configuration.</span></span>


