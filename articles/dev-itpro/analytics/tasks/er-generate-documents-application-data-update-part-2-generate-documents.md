--- 
title: "Hanna skilgreiningar til að búa til skjöl sem eru með forritsgögnum"
description: "Til að ljúka þessum skrefum í ferlinu verður fyrst að ljúka við ferlið, Rafræn skýrslugerð Búa til skjöl með gagnauppfærslum fyrir forrit (Hluti 1: Flytja inn grunnstillingar)."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.openlocfilehash: 8376107a33dd83e04f82fcab6847e7f073f08dbc
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2018

---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a><span data-ttu-id="e8ac1-103">Hanna skilgreiningar til að búa til skjöl sem eru með forritsgögnum</span><span class="sxs-lookup"><span data-stu-id="e8ac1-103">Design configurations to generate documents that have application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e8ac1-104">Til að ljúka þessum skrefum í ferlinu verður fyrst að ljúka við ferlið, Rafræn skýrslugerð Búa til skjöl með gagnauppfærslum fyrir forrit (Hluti 1: Flytja inn grunnstillingar).</span><span class="sxs-lookup"><span data-stu-id="e8ac1-104">To complete the steps in this procedure, you must first complete the procedure, ER Generate documents with application data update (Part 1: Import configurations).</span></span>



<span data-ttu-id="e8ac1-105">Skrefin í þessu ferli sýna hvernig skal hanna Rafræna skýrslugerð (ER) grunnstillingar þannig að þær búi til rafræn skjöl.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="e8ac1-106">Í þessu ferli keyrirðu innfluttar grunnstillingar sniðs fyrir Rafræn skýrslugerð, sem hafa verið stofnaðar fyrir sýnifyrirtækið, Litware, Inc. til að mynda rafræn skjöl.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-106">In this procedure, you run the ER imported format configuration that has been created for the sample company, Litware, Inc. to generate electronic documents.</span></span>



<span data-ttu-id="e8ac1-107">Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="e8ac1-108">Skrefin er hægt að klára með því að nota DEMF gagnasafn.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-108">These steps can be completed using the DEMF dataset.</span></span> 



<span data-ttu-id="e8ac1-109">Áður en hafist er handa, skal breyta löndum samhengi fyrir DEMF fyrirtæki úr DEU (Þýskaland) yfir í BEL (Belgía).</span><span class="sxs-lookup"><span data-stu-id="e8ac1-109">Before you begin, change the country context for the DEMF company from DEU (Germany) to BEL (Belgium).</span></span> <span data-ttu-id="e8ac1-110">Smellið á Fyrirtækjastjórnun > Fyrirtæki > Lögaðilar til að uppfæra landskóðann á aðalaðsetri lögaðilans DEMF.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-110">Click Organization administration > Organizations > Legal entities to update the country code in the primary address of the legal entity DEMF.</span></span> <span data-ttu-id="e8ac1-111">Endurræsið umsókn</span><span class="sxs-lookup"><span data-stu-id="e8ac1-111">Restart your application.</span></span>


## <a name="run-imported-er-format"></a><span data-ttu-id="e8ac1-112">Keyra innflutt Rafræn skýrslugerð snið</span><span class="sxs-lookup"><span data-stu-id="e8ac1-112">Run imported ER format</span></span>
1. <span data-ttu-id="e8ac1-113">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-113">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="e8ac1-114">Í trénu skal víkka út „Intrastat (líkan)“.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-114">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="e8ac1-115">Í trénu skal velja „Intrastat (líkan)\Intrastat (Snið)“.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-115">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="e8ac1-116">Smellið á „Keyra“.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-116">Click Run.</span></span>
    * <span data-ttu-id="e8ac1-117">Keyrið drög að útgáfu Rafræn skýrslugerð grunnstillingar til að mynda Intrastat skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-117">Run the draft version of the ER format configuration to generate the Intrastat report.</span></span>  
5. <span data-ttu-id="e8ac1-118">Í reitinn Færið inn skráarheiti, skal rita „intrastat.xml“.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-118">In the Enter file name field, type 'intrastat.xml'.</span></span>
    * <span data-ttu-id="e8ac1-119">Tilgreinið heiti skrárinnar.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-119">Specify the name of the file.</span></span>  
6. <span data-ttu-id="e8ac1-120">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-120">Click OK.</span></span>
    * <span data-ttu-id="e8ac1-121">Yfirfara myndaða XML-skrá</span><span class="sxs-lookup"><span data-stu-id="e8ac1-121">Review the generated XML file.</span></span>  
7. <span data-ttu-id="e8ac1-122">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-122">Close the page.</span></span>
8. <span data-ttu-id="e8ac1-123">Fara í Skattur > Yfirlýsingar > Erlend viðskipti > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-123">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="e8ac1-124">Opnið þessa skjámynd til að skoða Intrastat færslur sem eru innifaldar í rafrænt skjalið sem er myndað.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-124">Open this form to view the Intrastat transactions that are included in the generated electronic document.</span></span>  
9. <span data-ttu-id="e8ac1-125">Smellið á Intrastat-safn.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-125">Click Intrastat archive.</span></span>
    * <span data-ttu-id="e8ac1-126">Þar sem keyrt snið Rafræn skýrslugerð inniheldur engar stillingar fyrir uppfærslu gagna forrits, hafa upplýsingar tilbúinnar Instrastat skýrslu ekki verið skjöluð.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-126">Because the executed ER format does not contain any settings for application data update, the details of the completed Intrastat report have not been archived.</span></span>  
10. <span data-ttu-id="e8ac1-127">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-127">Close the page.</span></span>
11. <span data-ttu-id="e8ac1-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e8ac1-128">Close the page.</span></span>


