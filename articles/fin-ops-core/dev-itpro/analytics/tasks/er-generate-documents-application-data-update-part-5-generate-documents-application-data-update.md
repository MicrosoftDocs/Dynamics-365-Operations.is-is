---
title: Búa til skjöl sem eru með forritsgögnum
description: 'Til að ljúka skrefunum í þessu ferli verður fyrst að ljúka við ferlið, „Rafræn skýrslugerð Búa til skjöl með gagnauppfærslum fyrir forrit (Hluti 4: Breyta sniði)“.'
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d95feb3395c36f9cf8a23770dc3173377067d9b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184877"
---
# <a name="generate-documents-that-have-application-data"></a><span data-ttu-id="7f5be-103">Búa til skjöl sem eru með forritsgögnum</span><span class="sxs-lookup"><span data-stu-id="7f5be-103">Generate documents that have application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7f5be-104">Til að ljúka skrefunum í þessu ferli verður fyrst að ljúka við ferlið, „Rafræn skýrslugerð Búa til skjöl með gagnauppfærslum fyrir forrit (Hluti 4: Breyta sniði)“.</span><span class="sxs-lookup"><span data-stu-id="7f5be-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 4: Modify format)”.</span></span>



<span data-ttu-id="7f5be-105">Skrefin í þessu ferli sýna hvernig skal hanna Rafræna skýrslugerð (ER) grunnstillingar þannig að þær búi til rafræn skjöl og uppfæri gögn fyrir forrit.</span><span class="sxs-lookup"><span data-stu-id="7f5be-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="7f5be-106">Í þessu ferli er Rafræn skýrslugerð grunnstillingar látnar mynda Intrastat skýrsluna og uppfæra hugbúnaðargögn fyrir safnupplýsingar skýrlugerðarferlisins.</span><span class="sxs-lookup"><span data-stu-id="7f5be-106">In this procedure, you execute the ER format configuration to generate the Intrastat report and update application data for archiving details of the reporting process.</span></span>



<span data-ttu-id="7f5be-107">Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="7f5be-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="7f5be-108">Skrefin er hægt að klára með því að nota DEMF gagnasafn.</span><span class="sxs-lookup"><span data-stu-id="7f5be-108">These steps can be completed using the DEMF dataset.</span></span> <span data-ttu-id="7f5be-109">Áður en hafist er handa, vertu viss um að land samhengi fyrir DEMF fyrirtæki úr DEU sé BEL (Belgía).</span><span class="sxs-lookup"><span data-stu-id="7f5be-109">Before you begin, make sure that the country context for the DEMF company is BEL (Belgium).</span></span>


## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="7f5be-110">Setja upp færibreytur erlendra viðskipta</span><span class="sxs-lookup"><span data-stu-id="7f5be-110">Set up foreign trade parameters</span></span>
1. <span data-ttu-id="7f5be-111">Fara í Skattur > Uppsetning > Erlend viðskipti > Færibreytur erlendra viðskipta.</span><span class="sxs-lookup"><span data-stu-id="7f5be-111">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="7f5be-112">Smellt er á flipann Númeraraðir.</span><span class="sxs-lookup"><span data-stu-id="7f5be-112">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="7f5be-113">Skjala upplýsingar um Intrastat skýrslugerð, við þurfum að bera kennsl á skrár fyrir hvert safn sem við búum til.</span><span class="sxs-lookup"><span data-stu-id="7f5be-113">Archiving details of Intrastat reporting process, we need to identify records of each archive we created.</span></span> <span data-ttu-id="7f5be-114">Fyrir það verður að skilgreina sérstök númeraröð.</span><span class="sxs-lookup"><span data-stu-id="7f5be-114">A special number sequence must be configured for that.</span></span>  
3. <span data-ttu-id="7f5be-115">Veljið „Intrastat safnkenni“ tilvísunina“.</span><span class="sxs-lookup"><span data-stu-id="7f5be-115">Select the ‘Intrastat archive ID’ reference.</span></span>
4. <span data-ttu-id="7f5be-116">Í reitinn kóði númeraraðar skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7f5be-116">In the Number sequence code field, type a value.</span></span>
    * <span data-ttu-id="7f5be-117">Í reitnum „Kóði númeraraðar“, skal færa inn eða velja gildið „Fremri_2“.</span><span class="sxs-lookup"><span data-stu-id="7f5be-117">In the ‘Number sequence code’ field, enter or select the value ‘Fore_2’.</span></span>  
5. <span data-ttu-id="7f5be-118">ÚtkljáBreytingar Kóði númeraraðar.</span><span class="sxs-lookup"><span data-stu-id="7f5be-118">ResolveChanges the Number sequence code.</span></span>
6. <span data-ttu-id="7f5be-119">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="7f5be-119">Click Save.</span></span>
7. <span data-ttu-id="7f5be-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7f5be-120">Close the page.</span></span>

## <a name="run-modified-er-format"></a><span data-ttu-id="7f5be-121">Keryra breytt snið Rafræn skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="7f5be-121">Run modified ER format</span></span>
1. <span data-ttu-id="7f5be-122">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="7f5be-122">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="7f5be-123">Í trénu skal víkka út „Intrastat (líkan)“.</span><span class="sxs-lookup"><span data-stu-id="7f5be-123">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="7f5be-124">Í trénu skal velja „Intrastat (líkan)\Intrastat (Snið)“.</span><span class="sxs-lookup"><span data-stu-id="7f5be-124">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="7f5be-125">Smellið á „Keyra“.</span><span class="sxs-lookup"><span data-stu-id="7f5be-125">Click Run.</span></span>
5. <span data-ttu-id="7f5be-126">Í reitinn Færið inn skráarheiti skal rita „intrastat2.xml“.</span><span class="sxs-lookup"><span data-stu-id="7f5be-126">In the Enter file name field, type 'intrastat2.xml'.</span></span>
    * <span data-ttu-id="7f5be-127">intrastat2.xml</span><span class="sxs-lookup"><span data-stu-id="7f5be-127">intrastat2.xml</span></span>  
6. <span data-ttu-id="7f5be-128">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="7f5be-128">Click OK.</span></span>

## <a name="review-er-format-executions-results"></a><span data-ttu-id="7f5be-129">Yfirfara snið Rafræn skýrslugerð niðurstöður framkvæmdar</span><span class="sxs-lookup"><span data-stu-id="7f5be-129">Review ER format execution’s results</span></span>
    * <span data-ttu-id="7f5be-130">Yfirfara myndaða XML-skrá</span><span class="sxs-lookup"><span data-stu-id="7f5be-130">Review the generated XML file.</span></span>  
1. <span data-ttu-id="7f5be-131">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7f5be-131">Close the page.</span></span>
2. <span data-ttu-id="7f5be-132">Fara í Skattur > Yfirlýsingar > Erlend viðskipti > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="7f5be-132">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="7f5be-133">Opnið þessa skjámynd sem inniheldur Intrastat færslur sem hafa verið innifaldar í rafrænt skjal sem er myndað.</span><span class="sxs-lookup"><span data-stu-id="7f5be-133">Open this form containing Intrastat transactions that have been included to the generated electronic document.</span></span>  
3. <span data-ttu-id="7f5be-134">Smellið á Intrastat-safn.</span><span class="sxs-lookup"><span data-stu-id="7f5be-134">Click Intrastat archive.</span></span>
    * <span data-ttu-id="7f5be-135">Þar sem framkvæmt snið Rafræn skýrslugerð inniheldur nú stillingar fyrir gagnauppfærslu fyrir forrit, hafa upplýsingar um Intrastat skýrslugerðina í heild verið skjöluð.</span><span class="sxs-lookup"><span data-stu-id="7f5be-135">Since the executed ER format contains now settings for application data update, the details of the completed Intrastat reporting have been archived.</span></span> <span data-ttu-id="7f5be-136">Í þessari skjámynd er hægt að sjá skráningarhaus safnsins sem stofnað var.</span><span class="sxs-lookup"><span data-stu-id="7f5be-136">In this form, you can see the header record of the created archive.</span></span>  
4. <span data-ttu-id="7f5be-137">Smellið á Details.</span><span class="sxs-lookup"><span data-stu-id="7f5be-137">Click Details.</span></span>
    * <span data-ttu-id="7f5be-138">Í þessari skjámynd er hægt að sjá upplýsingar um safnið sem stofnað var.</span><span class="sxs-lookup"><span data-stu-id="7f5be-138">In this form, you can see the details for the created archive.</span></span>  
5. <span data-ttu-id="7f5be-139">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7f5be-139">Close the page.</span></span>
6. <span data-ttu-id="7f5be-140">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7f5be-140">Close the page.</span></span>
7. <span data-ttu-id="7f5be-141">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7f5be-141">Close the page.</span></span>
