---
title: Stofna víddir og flytja inn víddarstök
description: Kostnaðarbókhald er sjálfstæð eining sem krefst notkunar gagna úr öðrum einingum.
author: ShylaThompson
manager: AnnBe
ms.date: 09/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 610a9302610af7a074a91dfc2a8c87725b0a1a82
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009494"
---
# <a name="create-dimensions-and-import-dimension-members"></a><span data-ttu-id="48ea0-103">Stofna víddir og flytja inn víddarstök</span><span class="sxs-lookup"><span data-stu-id="48ea0-103">Create dimensions and import dimension members</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="48ea0-104">Kostnaðarbókhald er sjálfstæð eining sem krefst notkunar gagna úr öðrum einingum.</span><span class="sxs-lookup"><span data-stu-id="48ea0-104">Cost accounting is an independent module that requires data from other modules.</span></span> <span data-ttu-id="48ea0-105">Slík gögn eru flokkuð á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="48ea0-105">This data is categorized into the following:</span></span>

-  <span data-ttu-id="48ea0-106">Kostnaðareiningar</span><span class="sxs-lookup"><span data-stu-id="48ea0-106">Cost elements</span></span>
-  <span data-ttu-id="48ea0-107">Kostnaðarhlutir</span><span class="sxs-lookup"><span data-stu-id="48ea0-107">Cost objects</span></span>
-  <span data-ttu-id="48ea0-108">Tölfræðilegar víddir</span><span class="sxs-lookup"><span data-stu-id="48ea0-108">Statistical dimensions</span></span>

<span data-ttu-id="48ea0-109">**Kostnaðareining** samsvarar afurð sem tengist kostnaði í bókhaldslykum.</span><span class="sxs-lookup"><span data-stu-id="48ea0-109">A **Cost element** corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="48ea0-110">**Kostnaðarhlutur** getur verið hvaða gerð fjárhagsvíddar sem er, svo sem afurð, kostnaðarstaðir og verkefni, sem á að áætla, úthluta kostnaði á, eða mæla beint.</span><span class="sxs-lookup"><span data-stu-id="48ea0-110">A **Cost object** corresponds to any type of financial dimension, such as products, cost centers, and projects that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="48ea0-111">**Tölfræðileg vídd** og stök hennar eru notuð til að skrá ópeningalegar færslur.</span><span class="sxs-lookup"><span data-stu-id="48ea0-111">A **Statistical dimension** and its members are used to register non-monetary entries.</span></span> <span data-ttu-id="48ea0-112">Stök fyrir tölfræðilega vídd má nota sem grunn úthlutunar við kostnaðardreifingu og úthlutun.</span><span class="sxs-lookup"><span data-stu-id="48ea0-112">Statistical dimension members can be used as an allocation base in cost distribution and allocation</span></span> 

<span data-ttu-id="48ea0-113">Eftirfarandi útlínumynd sýnir víddirnar sem eru notaðar við Kostnaðarbókhald.</span><span class="sxs-lookup"><span data-stu-id="48ea0-113">The following diagram illustrates the dimensions that are used in Cost accounting.</span></span>

<span data-ttu-id="48ea0-114">[![Kostnaðarbókhaldsvíddir](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="48ea0-114">[![Cost accounting dimensions](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span></span>

<span data-ttu-id="48ea0-115">Eftir að gögn eru flutt inn í Kostnaðarbókhald getur þú nota þau til að byggja ýmis sjónarhorn sem veita innsýn til stjórnenda á öllum stigum fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="48ea0-115">After the data is imported into Cost accounting, you can use it to build various perspectives that provide insights to managers at all levels of the organization.</span></span> <span data-ttu-id="48ea0-116">Eftirfarandi efnisatriði veita upplýsingar um stofnun vídda og innflutning víddarstaka.</span><span class="sxs-lookup"><span data-stu-id="48ea0-116">The following topics provide information about creating dimensions and importing dimension members.</span></span> 

-  [<span data-ttu-id="48ea0-117">Víddir kostnaðareiningar</span><span class="sxs-lookup"><span data-stu-id="48ea0-117">Cost element dimensions</span></span>](cost-elements.md)
-  [<span data-ttu-id="48ea0-118">Stofna kostnaðareiningar</span><span class="sxs-lookup"><span data-stu-id="48ea0-118">Create cost elements</span></span>](./tasks/create-cost-elements.md)
-  [<span data-ttu-id="48ea0-119">Víddir kostnaðarhlutar</span><span class="sxs-lookup"><span data-stu-id="48ea0-119">Cost object dimensions</span></span>](cost-objects.md)
-  [<span data-ttu-id="48ea0-120">Varpa víddarstökum kostnaðareiningar á almennt safn víddarstaka</span><span class="sxs-lookup"><span data-stu-id="48ea0-120">Map cost element dimension members to a common set of dimension members</span></span>](map-cost-elements-dimension-members.md)
-  [<span data-ttu-id="48ea0-121">Varpa kostnaðareiningarvídd</span><span class="sxs-lookup"><span data-stu-id="48ea0-121">Map a cost element dimension</span></span>](./tasks/map-cost-element-dimension.md)
-  [<span data-ttu-id="48ea0-122">Sniðmát meðlima tölfræðivídda og tölfræðiveita</span><span class="sxs-lookup"><span data-stu-id="48ea0-122">Statistical dimension members and statistical measure provider templates</span></span>](statistical-measure-provider-template.md)






