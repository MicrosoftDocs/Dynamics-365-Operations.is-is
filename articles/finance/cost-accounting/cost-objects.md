---
title: Víddir kostnaðarhluta
description: Þegar kostnaður er greindur, notarðu víddir kostnaðareiningar til að ákvarða hvert kostnaður streymir. Víddir kostnaðarhlutar eru notaðar til að ákvarða hvert á að úthluta kostnaði. Þetta efni inniheldur upplýsingar um víddir kostnaðarhlutar.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimensionMember, CAMCostObject
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a090ecae2aadf1d0e08dd6127f831abdbf4a6b0a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976428"
---
# <a name="cost-object-dimensions"></a><span data-ttu-id="e31ed-105">Víddir kostnaðarhluta</span><span class="sxs-lookup"><span data-stu-id="e31ed-105">Cost object dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e31ed-106">Þegar kostnaður er greindur, notarðu víddir kostnaðareiningar til að ákvarða hvert kostnaður streymir.</span><span class="sxs-lookup"><span data-stu-id="e31ed-106">When you analyze costs, you use cost element dimensions to determine where costs flow to.</span></span> <span data-ttu-id="e31ed-107">Víddir kostnaðarhlutar eru notaðar til að ákvarða hvert á að úthluta kostnaði.</span><span class="sxs-lookup"><span data-stu-id="e31ed-107">You use cost object dimensions to determine where you should assign costs.</span></span> <span data-ttu-id="e31ed-108">Þetta efni inniheldur upplýsingar um víddir kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="e31ed-108">This topic provides information about cost object dimensions.</span></span>

<span data-ttu-id="e31ed-109">Kostnaðarhlutur getur verið hvaða gerð hlutar sem á að áætla, úthluta kostnaði á, eða mæla beint.</span><span class="sxs-lookup"><span data-stu-id="e31ed-109">A cost object can be any type of object that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="e31ed-110">Dæmigerður kostnaðarhlutur inniheldur afurðir, verk, tilföng, deildir, kostnaðarstaði og landfræðileg svæði.</span><span class="sxs-lookup"><span data-stu-id="e31ed-110">Typical cost objects include products, projects, resources, departments, cost centers, and geographical regions.</span></span> <span data-ttu-id="e31ed-111">Stjórnun notar kostnaðarhlutur til að magngreina kostnað, en einnig til að keyra arðsemisgreiningu.</span><span class="sxs-lookup"><span data-stu-id="e31ed-111">Management uses cost objects to quantify costs and also to drive profitability analysis.</span></span>

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a><span data-ttu-id="e31ed-112">Víddir kostnaðahluta og víddarstök kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="e31ed-112">Cost object dimensions and cost object dimension members</span></span>
<span data-ttu-id="e31ed-113">Kostnaðarhlutir eru þekkt sem *víddir kostnaðarhlutar*.</span><span class="sxs-lookup"><span data-stu-id="e31ed-113">Cost objects are known as *cost object dimensions*.</span></span> <span data-ttu-id="e31ed-114">Eftir að búið er að ákvarða hvaða til hvaða einingar vídd kostnaðareiningar vísar til, verður að tilgreina einstaka víddargildi eða flytja þær inn í kostnaðarbókhald úr öðrum upprunakerfum.</span><span class="sxs-lookup"><span data-stu-id="e31ed-114">After you’ve decided which entity the cost object dimension should refer to, you must specify the individual dimension values or import them into Cost accounting from other source systems.</span></span> <span data-ttu-id="e31ed-115">Einstaka víddargildi kallast *víddarstök kostnaðarhlutar*.</span><span class="sxs-lookup"><span data-stu-id="e31ed-115">These individual dimension values are known as *cost object dimension members*.</span></span> <span data-ttu-id="e31ed-116">T.d. á að nota fjárhagsvídd sem nefnist kostnaðarstað sem vídd kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="e31ed-116">For example, you want to use the financial dimension that is named Cost center as the cost object dimension.</span></span> <span data-ttu-id="e31ed-117">Til að sjá hvernig kostnaður streymir til stakar kostnaðarstaðir, þarf að flytja inn víddarstök kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="e31ed-117">To see how costs flow to the individual cost centers, you must import the cost object dimension members.</span></span> <span data-ttu-id="e31ed-118">Í þessu tilfelli eru víddarstök kostnaðarhlutar hin raunverulega kostnaðarstöðum, eins og sala, Framleiðslu, Stjórnun og Landfræðilegum staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="e31ed-118">In this case, the cost object dimension members are the actual cost centers, such as Sales, Production, Administration, and Geographic locations.</span></span> <span data-ttu-id="e31ed-119">Eftirfarandi skjámyndir sýna dæmi um kostnaðarstaður sem vídd kostnaðarhlutar með hennar raunverulegu kostnaðarstaður sem víddarstök kostnaðahlutar.</span><span class="sxs-lookup"><span data-stu-id="e31ed-119">The following screenshot shows an example of Cost Centers as the cost object dimension with its actual cost centers as cost object dimension members.</span></span> 

<span data-ttu-id="e31ed-120">[![Skjámynd sem sýnir kostnaðarstaði sem vídd kostnaðarhlutar](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="e31ed-120">[![Screenshot showing Cost Centers as cost object dimension](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span></span>

## <a name="import-cost-object-dimension-members-through-data-connectors"></a><span data-ttu-id="e31ed-121">Flytja inn víddarstök kostnaðarhlutar með gagnatengjum.</span><span class="sxs-lookup"><span data-stu-id="e31ed-121">Import cost object dimension members through data connectors</span></span>
<span data-ttu-id="e31ed-122">Til þess að auðvelda innflutningi víddarstök kostnaðarhlutar, notarðu gagnatengi til að sækja gildi úr einingum sem á að nota sem víddir kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="e31ed-122">To make the import of cost object dimension members easier, you use data connectors to retrieve the values from the entities that you want to use as cost object dimensions.</span></span> <span data-ttu-id="e31ed-123">Þú getur notað for-uppsett gagnatengi eða sérsniðin gagnatengi sem þú byggir sjálfur.</span><span class="sxs-lookup"><span data-stu-id="e31ed-123">You can use either the pre-built data connectors or custom data connectors that you build.</span></span>



