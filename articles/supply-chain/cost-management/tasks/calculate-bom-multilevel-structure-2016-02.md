---
title: Reikna út uppskrift með notkun uppbyggingar með mörgum stigum (febrúar 2016)
description: Þetta ferli sýnir hvernig reikna skal út kostnað fullunninnar vöru með því að nota niðurbrot á mörgum stigum sem er í kostnaðarskjali.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog, BOMCalcTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bbbc1e3c7941fd12991f1f6eaec4e9daf35fde9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239507"
---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016"></a><span data-ttu-id="9cde2-103">Reikna út uppskrift með notkun uppbyggingar með mörgum stigum (febrúar 2016)</span><span class="sxs-lookup"><span data-stu-id="9cde2-103">Calculate a BOM by using a multilevel structure (February 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9cde2-104">Þetta ferli sýnir hvernig reikna skal út kostnað fullunninnar vöru með því að nota niðurbrot á mörgum stigum sem er í kostnaðarskjali.</span><span class="sxs-lookup"><span data-stu-id="9cde2-104">This procedure shows how to calculate the cost of a finished product by using multilevel explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="9cde2-105">Þetta er sjöunda verkið í línunni Útreikningur uppskrifta.</span><span class="sxs-lookup"><span data-stu-id="9cde2-105">It is the seventh task in the BOM calculation series.</span></span> <span data-ttu-id="9cde2-106">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="9cde2-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="9cde2-107">Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.</span><span class="sxs-lookup"><span data-stu-id="9cde2-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="9cde2-108">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="9cde2-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9cde2-109">Velja vöru BOM_1.</span><span class="sxs-lookup"><span data-stu-id="9cde2-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="9cde2-110">Á Aðgerðasvæðinu skal smella á Stjórna kostnaði.</span><span class="sxs-lookup"><span data-stu-id="9cde2-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="9cde2-111">Smellt er á Verð vöru.</span><span class="sxs-lookup"><span data-stu-id="9cde2-111">Click Item price.</span></span>
5. <span data-ttu-id="9cde2-112">Smellt er á Reikna vörukostnað.</span><span class="sxs-lookup"><span data-stu-id="9cde2-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="9cde2-113">Gæti þurft að smella á þrípunkt (...) til að sjá þennan valkostur í efsta valmynd.</span><span class="sxs-lookup"><span data-stu-id="9cde2-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="9cde2-114">Í svæði Kostnaðarútgáfa, slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="9cde2-114">In the Costing version field, enter or select a value.</span></span>
    * <span data-ttu-id="9cde2-115">Velja kostnaðarútgáfa 20, því að áætlaður kostnaður og niðurbrot eru með mörgum stigum.</span><span class="sxs-lookup"><span data-stu-id="9cde2-115">Select Costing version 20, because it's Planned cost type and Explosion mode is Multilevel.</span></span>   <span data-ttu-id="9cde2-116">Niðurbrot á mörgum stigum er fyrir áætlaður kostnaður og hermun.</span><span class="sxs-lookup"><span data-stu-id="9cde2-116">The Multilevel explosion mode is for planned costs and simulations.</span></span> <span data-ttu-id="9cde2-117">Það er ekki notað fyrir staðalkostnaður.</span><span class="sxs-lookup"><span data-stu-id="9cde2-117">It is not used for standard cost.</span></span>  
7. <span data-ttu-id="9cde2-118">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9cde2-118">Click OK.</span></span>
8. <span data-ttu-id="9cde2-119">Smellt er á Skoða útreikningsupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="9cde2-119">Click View calculation details.</span></span>
    * <span data-ttu-id="9cde2-120">Gæti þurft að smella á þrípunkt (...) til að sjá þennan valkostur í efsta valmynd.</span><span class="sxs-lookup"><span data-stu-id="9cde2-120">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  <span data-ttu-id="9cde2-121">Í þessu tilfelli skal athuga hvernig BOM_2 hefur verið reiknað út með tilliti til hráefni, vinnsla og sameiginlegur kostnaður með samtals 29,40 í staðinn fyrir staðalkostnaðurinn 10, sem var virkjaður í upprunalega verkefnaleiðbeiningar í þessari línur.</span><span class="sxs-lookup"><span data-stu-id="9cde2-121">In this case, notice how BOM_2 has been calculated taking into account the raw material, process, and overhead with a total of 29,40 instead of the standard cost of 10 that was activated in the initial task guide in this series.</span></span>  
9. <span data-ttu-id="9cde2-122">Smellt er á flipann Kostnaðarskjal.</span><span class="sxs-lookup"><span data-stu-id="9cde2-122">Click the Costing sheet tab.</span></span>
    * <span data-ttu-id="9cde2-123">Þegar litið er á flipinn Kostnaðarskjal eru samtölur á hvern kostnaðarflokkur ólíkur miðað við útreikningur sem gerður var í fyrri verkefnaleiðbeiningar.</span><span class="sxs-lookup"><span data-stu-id="9cde2-123">Moving to the Costing sheet tab, the totals per cost group are different compared to the calculation done in previous task guide.</span></span>  
10. <span data-ttu-id="9cde2-124">Á svæðinu Stig skal velja „Mörg stig“.</span><span class="sxs-lookup"><span data-stu-id="9cde2-124">In the Level field, select 'Multi'.</span></span>
    * <span data-ttu-id="9cde2-125">Þegar „Mörg stig“ eru valin eru kostnaður flokkaður samkvæmt samsetningu BOM_2, þar sem 10 kemur úr kostnaðarflokkur M1 (ITEM_C) og 15,60 kemur úr framleiðslu þar sem kostnaðarflokkur er L2.</span><span class="sxs-lookup"><span data-stu-id="9cde2-125">When selecting Multi, the costs are classified according to the composition of BOM_2, where 10 is derived from the M1 cost group (ITEM_C), and 15,60 is derived from its manufacturing where the cost group is L2.</span></span> <span data-ttu-id="9cde2-126">Óbeinn kostnaður er einnig mismunandi.</span><span class="sxs-lookup"><span data-stu-id="9cde2-126">Indirect costs also vary.</span></span>  
11. <span data-ttu-id="9cde2-127">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9cde2-127">Close the page.</span></span>
12. <span data-ttu-id="9cde2-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9cde2-128">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]