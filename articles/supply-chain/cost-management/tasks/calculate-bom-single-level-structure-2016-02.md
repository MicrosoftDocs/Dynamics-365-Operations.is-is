---
title: Reikna út uppskrift og nota uppbygging með einu stigi (febrúar 2016)
description: Þetta ferli sýnir hvernig reikna út kostnað fullunnin vara með því að nota niðurbrot á einu stigi sem er í kostnaðarskjali.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1968703c7e9662b5cccdb71d049010bb4bd4534
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836505"
---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a><span data-ttu-id="2e2ed-103">Reikna út uppskrift og nota uppbygging með einu stigi (febrúar 2016)</span><span class="sxs-lookup"><span data-stu-id="2e2ed-103">Calculate a BOM by using a single level structure (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2e2ed-104">Þetta ferli sýnir hvernig reikna út kostnað fullunnin vara með því að nota niðurbrot á einu stigi sem er í kostnaðarskjali.</span><span class="sxs-lookup"><span data-stu-id="2e2ed-104">This procedure shows how to calculate the cost of a finished product by using single level explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="2e2ed-105">Þetta er sjötta verkið í línunni Útreikningur uppskrifta.</span><span class="sxs-lookup"><span data-stu-id="2e2ed-105">This is the sixth task in the BOM calculation series.</span></span> <span data-ttu-id="2e2ed-106">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="2e2ed-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="2e2ed-107">Farðu í Losaðar afurðir.</span><span class="sxs-lookup"><span data-stu-id="2e2ed-107">Go to Released products.</span></span>
2. <span data-ttu-id="2e2ed-108">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="2e2ed-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2e2ed-109">Velja vöru BOM_1.</span><span class="sxs-lookup"><span data-stu-id="2e2ed-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="2e2ed-110">Á Aðgerðasvæðinu skal smella á Stjórna kostnaði.</span><span class="sxs-lookup"><span data-stu-id="2e2ed-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="2e2ed-111">Smellt er á Verð vöru.</span><span class="sxs-lookup"><span data-stu-id="2e2ed-111">Click Item price.</span></span>
5. <span data-ttu-id="2e2ed-112">Smellt er á Reikna vörukostnað.</span><span class="sxs-lookup"><span data-stu-id="2e2ed-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="2e2ed-113">Gæti þurft að smella á þrípunkt (...) til að sjá þennan valkostur í efsta valmynd.</span><span class="sxs-lookup"><span data-stu-id="2e2ed-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="2e2ed-114">Í svæði Kostnaðarútgáfa, smella á fellilistahnapp til að opna uppflettingu.</span><span class="sxs-lookup"><span data-stu-id="2e2ed-114">In the Costing version field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2e2ed-115">Í þessu sýnishorni, velja 10.</span><span class="sxs-lookup"><span data-stu-id="2e2ed-115">For this demo, select 10.</span></span> <span data-ttu-id="2e2ed-116">Þetta er sama kostnaðarútgáfa notuð til að bæta kostnaðarverði við íhluti.</span><span class="sxs-lookup"><span data-stu-id="2e2ed-116">This is the same costing version used for adding the cost price to the components.</span></span>  
7. <span data-ttu-id="2e2ed-117">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="2e2ed-117">Click OK.</span></span>
8. <span data-ttu-id="2e2ed-118">Smellt er á Skoða útreikningsupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="2e2ed-118">Click View calculation details.</span></span>
    * <span data-ttu-id="2e2ed-119">Gæti þurft að smella á þrípunkt (...) til að sjá þennan valkostur í efsta valmynd.</span><span class="sxs-lookup"><span data-stu-id="2e2ed-119">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>    <span data-ttu-id="2e2ed-120">Hér er samsetning kostnaðarins:  •    10 kemur úr ITEM_A, 10 úr ITEM_B, 10 úr BOM_2.</span><span class="sxs-lookup"><span data-stu-id="2e2ed-120">Here's the composition of the cost:  •    10 is derived from ITEM_A, 10 from ITEM_B, 10 from BOM_2.</span></span> <span data-ttu-id="2e2ed-121">Í þessu tilfelli eru engar upplýsingar fyrir BOM_2 því að fært inn sem staðalkostnaður af 10 en ekki gert í gegnum útreikningur.</span><span class="sxs-lookup"><span data-stu-id="2e2ed-121">In this case there are no details for BOM_2 because it was entered as a standard cost of 10 but not done through calculation.</span></span>  <span data-ttu-id="2e2ed-122">•  7 kemur úr uppsetningartíma, sem er fastur kostnaður, og 7 til viðbótar kemur úr keyrsluaaðgerð (Vinnsla).</span><span class="sxs-lookup"><span data-stu-id="2e2ed-122">•  7 is derived from the setup time, which is a constant cost, and additional 7 is derived from the run-time operation (Process).</span></span>  <span data-ttu-id="2e2ed-123">•  Einnig eru aðrar upphæðir sem samsvara óbeinum kostnaði.</span><span class="sxs-lookup"><span data-stu-id="2e2ed-123">•   There are also other amounts that correspond to indirect costs.</span></span>  
9. <span data-ttu-id="2e2ed-124">@SysTaskRecorder:_RequestClose</span><span class="sxs-lookup"><span data-stu-id="2e2ed-124">@SysTaskRecorder:_RequestClose</span></span>

