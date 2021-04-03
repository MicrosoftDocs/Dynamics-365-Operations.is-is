---
title: Búa til skjöl sem eru með forritsgögnum
description: 'Til að ljúka skrefunum í þessu ferli verður fyrst að ljúka við ferlið, „Rafræn skýrslugerð Búa til skjöl með gagnauppfærslum fyrir forrit (Hluti 4: Breyta sniði)“.'
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c474f4bc7940a429ed62870e00302c93581eb9a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569582"
---
# <a name="generate-documents-that-have-application-data"></a><span data-ttu-id="bd9b4-103">Búa til skjöl sem eru með forritsgögn</span><span class="sxs-lookup"><span data-stu-id="bd9b4-103">Generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bd9b4-104">Til að ljúka skrefunum í þessu ferli verður fyrst að ljúka við ferlið, „Rafræn skýrslugerð Búa til skjöl með gagnauppfærslum fyrir forrit (Hluti 4: Breyta sniði)“.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-104">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 4: Modify format)".</span></span>



<span data-ttu-id="bd9b4-105">Skrefin í þessu ferli sýna hvernig skal hanna Rafræna skýrslugerð (ER) grunnstillingar þannig að þær búi til rafræn skjöl og uppfæri gögn fyrir forrit.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="bd9b4-106">Í þessu ferli er Rafræn skýrslugerð grunnstillingar látnar mynda Intrastat skýrsluna og uppfæra hugbúnaðargögn fyrir safnupplýsingar skýrlugerðarferlisins.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-106">In this procedure, you execute the ER format configuration to generate the Intrastat report and update application data for archiving details of the reporting process.</span></span>



<span data-ttu-id="bd9b4-107">Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="bd9b4-108">Skrefin er hægt að klára með því að nota DEMF gagnasafn.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-108">These steps can be completed using the DEMF dataset.</span></span> <span data-ttu-id="bd9b4-109">Áður en hafist er handa, vertu viss um að land samhengi fyrir DEMF fyrirtæki úr DEU sé BEL (Belgía).</span><span class="sxs-lookup"><span data-stu-id="bd9b4-109">Before you begin, make sure that the country context for the DEMF company is BEL (Belgium).</span></span>


## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="bd9b4-110">Setja upp færibreytur erlendra viðskipta</span><span class="sxs-lookup"><span data-stu-id="bd9b4-110">Set up foreign trade parameters</span></span>
1. <span data-ttu-id="bd9b4-111">Fara í Skattur > Uppsetning > Erlend viðskipti > Færibreytur erlendra viðskipta.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-111">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="bd9b4-112">Smellt er á flipann Númeraraðir.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-112">Click the Number sequences tab.</span></span>

    <span data-ttu-id="bd9b4-113">Skjala upplýsingar um Intrastat skýrslugerð, við þurfum að bera kennsl á skrár fyrir hvert safn sem við búum til.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-113">Archiving details of Intrastat reporting process, we need to identify records of each archive we created.</span></span> <span data-ttu-id="bd9b4-114">Fyrir það verður að skilgreina sérstök númeraröð.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-114">A special number sequence must be configured for that.</span></span>  

3. <span data-ttu-id="bd9b4-115">Veljið „Intrastat safnkenni“ tilvísunina“.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-115">Select the 'Intrastat archive ID' reference.</span></span>
4. <span data-ttu-id="bd9b4-116">Í reitinn kóði númeraraðar skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-116">In the Number sequence code field, type a value.</span></span>

    <span data-ttu-id="bd9b4-117">Í reitnum „Kóði númeraraðar“, skal færa inn eða velja gildið „Fremri_2“.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-117">In the 'Number sequence code' field, enter or select the value 'Fore_2'.</span></span>  

5. <span data-ttu-id="bd9b4-118">ÚtkljáBreytingar Kóði númeraraðar.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-118">ResolveChanges the Number sequence code.</span></span>
6. <span data-ttu-id="bd9b4-119">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-119">Click Save.</span></span>
7. <span data-ttu-id="bd9b4-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-120">Close the page.</span></span>

## <a name="run-modified-er-format"></a><span data-ttu-id="bd9b4-121">Keryra breytt snið Rafræn skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="bd9b4-121">Run modified ER format</span></span>
1. <span data-ttu-id="bd9b4-122">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-122">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="bd9b4-123">Í trénu skal víkka út „Intrastat (líkan)“.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-123">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="bd9b4-124">Í trénu skal velja „Intrastat (líkan)\Intrastat (Snið)“.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-124">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="bd9b4-125">Smella á Keyra.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-125">Click Run.</span></span>
5. <span data-ttu-id="bd9b4-126">Í reitinn Færið inn skráarheiti skal rita „intrastat2.xml“.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-126">In the Enter file name field, type 'intrastat2.xml'.</span></span>
6. <span data-ttu-id="bd9b4-127">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-127">Click OK.</span></span>

## <a name="review-er-format-executions-results"></a><span data-ttu-id="bd9b4-128">Yfirfara snið Rafræn skýrslugerð niðurstöður framkvæmdar</span><span class="sxs-lookup"><span data-stu-id="bd9b4-128">Review ER format execution's results</span></span>
<span data-ttu-id="bd9b4-129">Yfirfara myndaða XML-skrá</span><span class="sxs-lookup"><span data-stu-id="bd9b4-129">Review the generated XML file.</span></span>  
1. <span data-ttu-id="bd9b4-130">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-130">Close the page.</span></span>
2. <span data-ttu-id="bd9b4-131">Fara í Skattur > Yfirlýsingar > Erlend viðskipti > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-131">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>

    <span data-ttu-id="bd9b4-132">Opnið þessa skjámynd sem inniheldur Intrastat færslur sem hafa verið innifaldar í rafrænt skjal sem er myndað.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-132">Open this form containing Intrastat transactions that have been included to the generated electronic document.</span></span>  

3. <span data-ttu-id="bd9b4-133">Smellið á Intrastat-safn.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-133">Click Intrastat archive.</span></span>

    <span data-ttu-id="bd9b4-134">Þar sem framkvæmt snið Rafræn skýrslugerð inniheldur nú stillingar fyrir gagnauppfærslu fyrir forrit, hafa upplýsingar um Intrastat skýrslugerðina í heild verið skjöluð.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-134">Since the executed ER format contains now settings for application data update, the details of the completed Intrastat reporting have been archived.</span></span> <span data-ttu-id="bd9b4-135">Í þessari skjámynd er hægt að sjá skráningarhaus safnsins sem stofnað var.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-135">In this form, you can see the header record of the created archive.</span></span>  

4. <span data-ttu-id="bd9b4-136">Smellið á Details.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-136">Click Details.</span></span>

    <span data-ttu-id="bd9b4-137">Í þessari skjámynd er hægt að sjá upplýsingar um safnið sem stofnað var.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-137">In this form, you can see the details for the created archive.</span></span>  

5. <span data-ttu-id="bd9b4-138">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-138">Close the page.</span></span>
6. <span data-ttu-id="bd9b4-139">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-139">Close the page.</span></span>
7. <span data-ttu-id="bd9b4-140">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="bd9b4-140">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]