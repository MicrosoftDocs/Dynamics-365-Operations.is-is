---
title: Stofna skilgreiningum á líkanavörpun fyrir rafræna skýrslugerð
description: Notaðu þessa aðferð til að hanna nýja stillingu fyrir líkanavörpun rafrænnar skýrslugerðar og nota innbyggða eiginleika Rafrænnar skýrslugerðar fyrir skilvirka samanlagða útreikninga.
author: NickSelin
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a614ce0f055691e36c1aab5d84d4fc3355026f1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752557"
---
# <a name="create-electronic-reporting-er-model-mapping-configurations"></a><span data-ttu-id="5038b-103">Stofna skilgreiningum á líkanavörpun fyrir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="5038b-103">Create Electronic reporting (ER) model mapping configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5038b-104">Notaðu þessa aðferð til að hanna nýja stillingu fyrir líkanavörpun rafrænnar skýrslugerðar og nota innbyggða eiginleika Rafrænnar skýrslugerðar fyrir skilvirka samanlagða útreikninga.</span><span class="sxs-lookup"><span data-stu-id="5038b-104">Use this procedure to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="5038b-105">Í þessu ferli stofnar þú skilgreiningu fyrir sýnifyrirtæki, Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="5038b-105">In this procedure, you will create a configuration for sample company, Litware, Inc.</span></span> 

<span data-ttu-id="5038b-106">Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="5038b-106">This procedure is created for uses with the assigned role of System administrator or Electronic reporting developer.</span></span>

<span data-ttu-id="5038b-107">Skrefin er hægt að klára með því að nota hvaða gagnasafn sem er.</span><span class="sxs-lookup"><span data-stu-id="5038b-107">These steps can be completed using any dataset.</span></span> <span data-ttu-id="5038b-108">Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu “Stofna skilgreiningarveitu og merkja hana sem virka”.</span><span class="sxs-lookup"><span data-stu-id="5038b-108">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>

1. <span data-ttu-id="5038b-109">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="5038b-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="5038b-110">Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt Virk.</span><span class="sxs-lookup"><span data-stu-id="5038b-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="5038b-111">Ef þú sérð skilgreiningarveituna ekki, skal klára skrefin í ferlinu, „Stofna skilgreiningarveitu og merkja hana sem virka”.</span><span class="sxs-lookup"><span data-stu-id="5038b-111">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>  
2. <span data-ttu-id="5038b-112">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="5038b-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="5038b-113">Smellt er á Sýna síur.</span><span class="sxs-lookup"><span data-stu-id="5038b-113">Click Show filters.</span></span>
4. <span data-ttu-id="5038b-114">Í svæðinu „Nafn“ skal færa inn síugildið „Intrastat“ og nota virknitáknið „byrjar á“.</span><span class="sxs-lookup"><span data-stu-id="5038b-114">In the "Name" field, enter the filter value, "Intrastat" and use the filter operator "begins with".</span></span>
    * <span data-ttu-id="5038b-115">Notið þessa síu til að finna skilgreiningu á gagnalíkaninu „Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="5038b-115">Apply this filter to find the 'Intrastat' data model configuration.</span></span> <span data-ttu-id="5038b-116">Þetta líkan kann þegar að vera til í grunnstillingatrénu.</span><span class="sxs-lookup"><span data-stu-id="5038b-116">This model may already exist in the configurations tree.</span></span> <span data-ttu-id="5038b-117">Ef það gerist skal sleppa næsta undirverkefni.</span><span class="sxs-lookup"><span data-stu-id="5038b-117">If it does, skip the next sub-task.</span></span>   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a><span data-ttu-id="5038b-118">Sækja skilgreiningar Intrastat-líkansins sem Microsoft útvegar</span><span class="sxs-lookup"><span data-stu-id="5038b-118">Get the Intrastat model configuration provided by Microsoft</span></span>
1. <span data-ttu-id="5038b-119">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5038b-119">Close the page.</span></span>
2. <span data-ttu-id="5038b-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5038b-120">Close the page.</span></span>
3. <span data-ttu-id="5038b-121">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="5038b-121">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
4. <span data-ttu-id="5038b-122">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="5038b-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5038b-123">Velja skal Microsoft reitinn.</span><span class="sxs-lookup"><span data-stu-id="5038b-123">Select the Microsoft provider tile.</span></span>  
5. <span data-ttu-id="5038b-124">Smella á Geymslur.</span><span class="sxs-lookup"><span data-stu-id="5038b-124">Click Repositories.</span></span>
    * <span data-ttu-id="5038b-125">Smella skal á Geymslur í Microsoft reitinum.</span><span class="sxs-lookup"><span data-stu-id="5038b-125">Click Repositories in the Microsoft provider tile.</span></span>  
6. <span data-ttu-id="5038b-126">Smellt er á Sýna síur.</span><span class="sxs-lookup"><span data-stu-id="5038b-126">Click Show filters.</span></span>
7. <span data-ttu-id="5038b-127">Í svæðið „Slá inn heiti“ skal slá inn síugildið „tilföng“ og nota virknitáknið „inniheldur“.</span><span class="sxs-lookup"><span data-stu-id="5038b-127">In the "Type name" field, enter the filter value, "resources" and use the filter operator "contains".</span></span> 
8. <span data-ttu-id="5038b-128">Smellt er á Opin.</span><span class="sxs-lookup"><span data-stu-id="5038b-128">Click Open.</span></span>
9. <span data-ttu-id="5038b-129">Í trénu skal velja „Intrastat líkan“.</span><span class="sxs-lookup"><span data-stu-id="5038b-129">In the tree, select 'Intrastat model'.</span></span>
10. <span data-ttu-id="5038b-130">Smelltu á Flytja inn.</span><span class="sxs-lookup"><span data-stu-id="5038b-130">Click Import.</span></span>
11. <span data-ttu-id="5038b-131">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="5038b-131">Click Yes.</span></span>
    * <span data-ttu-id="5038b-132">Þú fluttir inn grunnstillingu líkans fyrir Rafræna skýrslugerð sem inniheldur gagnalíkan sem skal nota til að læra hvernig hægt er að nota virknina Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="5038b-132">You imported the ER model configuration that contains the data model that you will use to explore how the new ER functionality can be used.</span></span>  
12. <span data-ttu-id="5038b-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5038b-133">Close the page.</span></span>
13. <span data-ttu-id="5038b-134">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5038b-134">Close the page.</span></span>
14. <span data-ttu-id="5038b-135">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="5038b-135">Click Reporting configurations.</span></span>

## <a name="add-a-new-model-mapping-configuration"></a><span data-ttu-id="5038b-136">Bæta við nýrri grunnstillingu líkanavörpunar</span><span class="sxs-lookup"><span data-stu-id="5038b-136">Add a new model mapping configuration</span></span>
1. <span data-ttu-id="5038b-137">Í trénu skal velja „Intrastat líkan“.</span><span class="sxs-lookup"><span data-stu-id="5038b-137">In the tree, select 'Intrastat model'.</span></span>
2. <span data-ttu-id="5038b-138">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="5038b-138">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="5038b-139">Í svæðið Nýtt skal slá inn „Vörpun líkans byggð á gagnalíkaninu Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="5038b-139">In the New field, enter 'Model Mapping based on data model Intrastat'.</span></span>
4. <span data-ttu-id="5038b-140">Í svæðið Heiti skal slá inn „Intrastat sýnivörpun“.</span><span class="sxs-lookup"><span data-stu-id="5038b-140">In the Name field, type 'Intrastat sample mapping'.</span></span>
    * <span data-ttu-id="5038b-141">Intrastat sýnivörpun</span><span class="sxs-lookup"><span data-stu-id="5038b-141">Intrastat sample mapping</span></span>  
5. <span data-ttu-id="5038b-142">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="5038b-142">Click Create configuration.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]