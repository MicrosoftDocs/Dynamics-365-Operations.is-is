---
title: Hanna skilgreiningar til að búa til skjöl sem eru með forritsgögnum
description: Þetta efni útskýrir hvernig skal hanna skilgreiningar rafrænnar skýrslugerðar þannig að þær búi til rafrænt skjal. (Hluti 1 - Flytja inn skilgreiningar).
author: NickSelin
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
ms.openlocfilehash: 9d3f528d48f345ec4b5cc2a46d7740cb6d0a36cd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751083"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a><span data-ttu-id="67749-104">Hanna skilgreiningar til að búa til skjöl sem eru með forritsgögnum</span><span class="sxs-lookup"><span data-stu-id="67749-104">Design configurations to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="67749-105">Til að ljúka þessum skrefum í ferlinu verður fyrst að ljúka við ferlið, Rafræn skýrslugerð Búa til skjöl með gagnauppfærslum fyrir forrit (Hluti 1: Flytja inn grunnstillingar).</span><span class="sxs-lookup"><span data-stu-id="67749-105">To complete the steps in this procedure, you must first complete the procedure, ER Generate documents with application data update (Part 1: Import configurations).</span></span>



<span data-ttu-id="67749-106">Skrefin í þessu ferli sýna hvernig skal hanna Rafræna skýrslugerð (ER) grunnstillingar þannig að þær búi til rafræn skjöl.</span><span class="sxs-lookup"><span data-stu-id="67749-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="67749-107">Í þessu ferli keyrirðu innfluttar grunnstillingar sniðs fyrir Rafræn skýrslugerð, sem hafa verið stofnaðar fyrir sýnifyrirtækið, Litware, Inc. til að mynda rafræn skjöl.</span><span class="sxs-lookup"><span data-stu-id="67749-107">In this procedure, you run the ER imported format configuration that has been created for the sample company, Litware, Inc. to generate electronic documents.</span></span>



<span data-ttu-id="67749-108">Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="67749-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="67749-109">Skrefin er hægt að klára með því að nota DEMF gagnasafn.</span><span class="sxs-lookup"><span data-stu-id="67749-109">These steps can be completed using the DEMF dataset.</span></span> 



<span data-ttu-id="67749-110">Áður en hafist er handa, skal breyta löndum samhengi fyrir DEMF fyrirtæki úr DEU (Þýskaland) yfir í BEL (Belgía).</span><span class="sxs-lookup"><span data-stu-id="67749-110">Before you begin, change the country context for the DEMF company from DEU (Germany) to BEL (Belgium).</span></span> <span data-ttu-id="67749-111">Smellið á Fyrirtækjastjórnun > Fyrirtæki > Lögaðilar til að uppfæra landskóðann á aðalaðsetri lögaðilans DEMF.</span><span class="sxs-lookup"><span data-stu-id="67749-111">Click Organization administration > Organizations > Legal entities to update the country code in the primary address of the legal entity DEMF.</span></span> <span data-ttu-id="67749-112">Endurræsið umsókn</span><span class="sxs-lookup"><span data-stu-id="67749-112">Restart your application.</span></span>


## <a name="run-imported-er-format"></a><span data-ttu-id="67749-113">Keyra innflutt Rafræn skýrslugerð snið</span><span class="sxs-lookup"><span data-stu-id="67749-113">Run imported ER format</span></span>
1. <span data-ttu-id="67749-114">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="67749-114">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="67749-115">Í trénu skal víkka út „Intrastat (líkan)“.</span><span class="sxs-lookup"><span data-stu-id="67749-115">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="67749-116">Í trénu skal velja „Intrastat (líkan)\Intrastat (Snið)“.</span><span class="sxs-lookup"><span data-stu-id="67749-116">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="67749-117">Smellið á „Keyra“.</span><span class="sxs-lookup"><span data-stu-id="67749-117">Click Run.</span></span>
    * <span data-ttu-id="67749-118">Keyrið drög að útgáfu Rafræn skýrslugerð grunnstillingar til að mynda Intrastat skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="67749-118">Run the draft version of the ER format configuration to generate the Intrastat report.</span></span>  
5. <span data-ttu-id="67749-119">Í reitinn Færið inn skráarheiti, skal rita „intrastat.xml“.</span><span class="sxs-lookup"><span data-stu-id="67749-119">In the Enter file name field, type 'intrastat.xml'.</span></span>
    * <span data-ttu-id="67749-120">Tilgreinið heiti skrárinnar.</span><span class="sxs-lookup"><span data-stu-id="67749-120">Specify the name of the file.</span></span>  
6. <span data-ttu-id="67749-121">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="67749-121">Click OK.</span></span>
    * <span data-ttu-id="67749-122">Yfirfara myndaða XML-skrá</span><span class="sxs-lookup"><span data-stu-id="67749-122">Review the generated XML file.</span></span>  
7. <span data-ttu-id="67749-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="67749-123">Close the page.</span></span>
8. <span data-ttu-id="67749-124">Fara í Skattur > Yfirlýsingar > Erlend viðskipti > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="67749-124">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="67749-125">Opnið þessa skjámynd til að skoða Intrastat færslur sem eru innifaldar í rafrænt skjalið sem er myndað.</span><span class="sxs-lookup"><span data-stu-id="67749-125">Open this form to view the Intrastat transactions that are included in the generated electronic document.</span></span>  
9. <span data-ttu-id="67749-126">Smellið á Intrastat-safn.</span><span class="sxs-lookup"><span data-stu-id="67749-126">Click Intrastat archive.</span></span>
    * <span data-ttu-id="67749-127">Þar sem keyrt snið Rafræn skýrslugerð inniheldur engar stillingar fyrir uppfærslu gagna forrits, hafa upplýsingar tilbúinnar Instrastat skýrslu ekki verið skjöluð.</span><span class="sxs-lookup"><span data-stu-id="67749-127">Because the executed ER format does not contain any settings for application data update, the details of the completed Intrastat report have not been archived.</span></span>  
10. <span data-ttu-id="67749-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="67749-128">Close the page.</span></span>
11. <span data-ttu-id="67749-129">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="67749-129">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]