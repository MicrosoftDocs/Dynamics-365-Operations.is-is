---
title: Stofna skilgreiningar sem byggja á víddum
description: Þessi verklýsing sýnir hvernig á að skilgreina vöru sem byggja á víddum.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, EcoResDimensionBasedConfiguration, ConfigChooseFromRoute, ConfigChooseFromGroup, ConfigChoiceApprove
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9190d6dfd4b3f6cf0634e86845e7de028631bdd4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "328586"
---
# <a name="create-dimension-based-configurations"></a><span data-ttu-id="2a4cd-103">Stofna skilgreiningar sem byggja á víddum</span><span class="sxs-lookup"><span data-stu-id="2a4cd-103">Create dimension-based configurations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2a4cd-104">Þessi verklýsing sýnir hvernig á að skilgreina vöru sem byggja á víddum.</span><span class="sxs-lookup"><span data-stu-id="2a4cd-104">This procedure shows how to define a configuration for a dimension-based product.</span></span> <span data-ttu-id="2a4cd-105">Þetta er síðasta ferli af röðinni sem útskýrir hvernig á að byggja upp samsetningar fyrir víddaskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="2a4cd-105">This is the last procedure in the series that explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="2a4cd-106">Framkvæmd þessa ferlis byggir á gögn sem voru stofnuð í fyrri sjö skráningar.</span><span class="sxs-lookup"><span data-stu-id="2a4cd-106">The execution of this procedure is dependent on the data created in the previous seven recordings.</span></span> <span data-ttu-id="2a4cd-107">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="2a4cd-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-dimension-based-product-master"></a><span data-ttu-id="2a4cd-108">Finna afurðarsniðmát sem byggja á víddum</span><span class="sxs-lookup"><span data-stu-id="2a4cd-108">Find the dimension-based product master</span></span>
1. <span data-ttu-id="2a4cd-109">Smellið á Viðhald útgefinnar afurðar.</span><span class="sxs-lookup"><span data-stu-id="2a4cd-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="2a4cd-110">Smella á Útgefnar afurðir.</span><span class="sxs-lookup"><span data-stu-id="2a4cd-110">Click Released products.</span></span>
3. <span data-ttu-id="2a4cd-111">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="2a4cd-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="2a4cd-112">Veljið sniðmát afurða sem byggja á víddum sem var stofnaður í fyrstu skráningu í þessari röð 8 skráninga.</span><span class="sxs-lookup"><span data-stu-id="2a4cd-112">Select the dimension-based product master that you created in the first recording in this sequence of 8 recordings.</span></span>  

## <a name="create-configurations"></a><span data-ttu-id="2a4cd-113">Stofna skilgreiningar</span><span class="sxs-lookup"><span data-stu-id="2a4cd-113">Create configurations</span></span>
1. <span data-ttu-id="2a4cd-114">Smellt er viðhalda skilgreiningum á tækniaðgerðarúðu.</span><span class="sxs-lookup"><span data-stu-id="2a4cd-114">On the Engineering Action Pane, click Maintain configurations.</span></span>
2. <span data-ttu-id="2a4cd-115">Smellt er á Skilgreina.</span><span class="sxs-lookup"><span data-stu-id="2a4cd-115">Click Configure.</span></span>
3. <span data-ttu-id="2a4cd-116">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="2a4cd-116">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="2a4cd-117">Í reitinn Vörunúmer skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="2a4cd-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="2a4cd-118">Velja einhverja af vörunum í fyrsta afbrigðaflokki.</span><span class="sxs-lookup"><span data-stu-id="2a4cd-118">Select any of the items in the first configuration group.</span></span>  
5. <span data-ttu-id="2a4cd-119">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="2a4cd-119">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="2a4cd-120">Í reitinn Vörunúmer skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="2a4cd-120">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="2a4cd-121">Veljið hvaða vöru sem er úr seinni skilgreiningarflokk.</span><span class="sxs-lookup"><span data-stu-id="2a4cd-121">Select any item from the second configuration group.</span></span>  
7. <span data-ttu-id="2a4cd-122">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="2a4cd-122">Click OK.</span></span>
8. <span data-ttu-id="2a4cd-123">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="2a4cd-123">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="2a4cd-124">Í reitinn skilgreining skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="2a4cd-124">In the Configuration field, type a value.</span></span>
    * <span data-ttu-id="2a4cd-125">Færið inn heiti skilgreiningar sem gerir auðvelt að bera kennsl á skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="2a4cd-125">Enter a configuration name that will make it easy to identify the configuration.</span></span>  
10. <span data-ttu-id="2a4cd-126">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="2a4cd-126">In the Description field, type a value.</span></span>
    * <span data-ttu-id="2a4cd-127">Færið inn lýsingu á skilgreiningu til að lýsa hvað hún inniheldur.</span><span class="sxs-lookup"><span data-stu-id="2a4cd-127">Enter a description of the configuration to explain what it contains.</span></span>  
11. <span data-ttu-id="2a4cd-128">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="2a4cd-128">Click OK.</span></span>

