---
title: Skrá sem lokið í ekki númeraplötustýrð staðsetningu (Notkun, maí 2016)
description: Þessi verkefnaleiðbeiningar sýnir dæmi um skýrslugerð sem lokið á staðsetningu sem ekki – númeraplötustýrð.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdParmCostEstimation, ProdParmStartUp, ProdParmReportFinished, WHSWorkTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a9010b95cfd0528cd3b532627d19a3b340bdca4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430027"
---
# <a name="report-as-finished-to-a-non-license-plate-controlled-location--application-may-2016"></a><span data-ttu-id="4fa4f-103">Skrá sem lokið í ekki númeraplötustýrð staðsetningu (Notkun, maí 2016)</span><span class="sxs-lookup"><span data-stu-id="4fa4f-103">Report as finished to a non-license plate controlled location  (Application, May 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4fa4f-104">Þessi verkefnaleiðbeiningar sýnir dæmi um skýrslugerð sem lokið á staðsetningu sem ekki – númeraplötustýrð.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-104">This task guide shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="4fa4f-105">Gildandi vinnureglu er skilyrði fyrir þetta verk.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-105">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="4fa4f-106">Fyrri verkefnaleiðbeiningar sýna uppsetningu vinnureglu.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-106">A previous task guide showed the setup of the work policy.</span></span> <span data-ttu-id="4fa4f-107">Þessi leiðarvísi fyrir verk krefst AX forrit 7.0.1 eða síðar.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>




## <a name="set-up-an-output-location"></a><span data-ttu-id="4fa4f-108">Setja upp staðsetningu úttaks</span><span class="sxs-lookup"><span data-stu-id="4fa4f-108">Set up an output location</span></span>
1. <span data-ttu-id="4fa4f-109">Fara á fyrirtækisstjórnun > Tilföng >Tilfangaflokka.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-109">Go to Organization administration > Resources > Resource groups.</span></span>
2. <span data-ttu-id="4fa4f-110">Á listanum, veljið tilfangaflokk 5102</span><span class="sxs-lookup"><span data-stu-id="4fa4f-110">In the list, select resource group '5102'.</span></span>
3. <span data-ttu-id="4fa4f-111">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-111">Click Edit.</span></span>
4. <span data-ttu-id="4fa4f-112">Í úttaksvöruhús svæðinu veljið 51.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-112">In the Output warehouse field, enter '51'.</span></span>
5. <span data-ttu-id="4fa4f-113">Í staðsetning úttaks svæðinu sláið inn 001.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-113">In the Output location field, enter '001'.</span></span>
    * <span data-ttu-id="4fa4f-114">Staðsetning 001 ekki númeraplötustýrð staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-114">Location 001 isn't a license plate–controlled location.</span></span> <span data-ttu-id="4fa4f-115">Hægt er að setja upp staðsetningu úttaks ekki númeraplötu aðeins ef gildandi vinnureglu er til fyrir staðsetningarinnar.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-115">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span>  

## <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="4fa4f-116">Stofna framleiðslupöntun og skrá sem lokið.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-116">Create a production order and report it as finished</span></span>
1. <span data-ttu-id="4fa4f-117">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-117">Close the page.</span></span>
2. <span data-ttu-id="4fa4f-118">Fara í Framleiðslustýringar > Framleiðslupantanir > Allar framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-118">Go to Production control > Production orders > All production orders.</span></span>
3. <span data-ttu-id="4fa4f-119">Smella á Ný framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-119">Click New production order.</span></span>
4. <span data-ttu-id="4fa4f-120">Í vörunúmer svæðið sláið inn L0101.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-120">In the Item number field, enter 'L0101'.</span></span>
5. <span data-ttu-id="4fa4f-121">Smellið á Stofna.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-121">Click Create.</span></span>
6. <span data-ttu-id="4fa4f-122">Á Aðgerðasvæðinu skal smellt á framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-122">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="4fa4f-123">Smellt er á Mat.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-123">Click Estimate.</span></span>
8. <span data-ttu-id="4fa4f-124">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-124">Click OK.</span></span>
9. <span data-ttu-id="4fa4f-125">Smellt er á Byrja.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-125">Click Start.</span></span>
10. <span data-ttu-id="4fa4f-126">Smellt er á flipannAlmennt.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-126">Click the General tab.</span></span>
11. <span data-ttu-id="4fa4f-127">Veljið ‚Aldrei‘ í reitnum Sjálfvirk uppskriftarnotkun.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-127">In the Automatic BOM consumption field, select 'Never'.</span></span>
12. <span data-ttu-id="4fa4f-128">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-128">Click OK.</span></span>
13. <span data-ttu-id="4fa4f-129">Smellið á Bóka sem tilbúið.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-129">Click Report as finished.</span></span>
14. <span data-ttu-id="4fa4f-130">Smellt er á flipannAlmennt.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-130">Click the General tab.</span></span>
15. <span data-ttu-id="4fa4f-131">Velja skal Já í reitnum leyfa villu.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-131">Select Yes in the Accept error field.</span></span>
16. <span data-ttu-id="4fa4f-132">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-132">Click OK.</span></span>
17. <span data-ttu-id="4fa4f-133">Í aðgerðasvæðinu er smellt á vöruhús.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-133">On the Action Pane, click Warehouse.</span></span>
18. <span data-ttu-id="4fa4f-134">Smellt er á Upplýsingar um vinnu</span><span class="sxs-lookup"><span data-stu-id="4fa4f-134">Click Work details.</span></span>
    * <span data-ttu-id="4fa4f-135">Þegar framleiðslupöntunin var skráð sem lokið, engin vinna var mynduð fyrir frágangur.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-135">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="4fa4f-136">Þetta gerist vegna þess að vinna regla er skilgreind sem kemur í veg fyrir vinnu búnar til þegar afurð L0101 er skráð sem lokið á staðsetningu 001.</span><span class="sxs-lookup"><span data-stu-id="4fa4f-136">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span>  

