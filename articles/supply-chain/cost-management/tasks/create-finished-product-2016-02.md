---
title: Stofna tilbúna afurð (aðeins febrúar 2016)
description: Þetta verk einblínir á að búa til tilbúin afurð.
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 44f9693e04160ffe9307de5e454d8269ca883679
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570858"
---
# <a name="create-a-finished-product-february-2016-only"></a><span data-ttu-id="a36f2-103">Stofna tilbúna afurð (aðeins febrúar 2016)</span><span class="sxs-lookup"><span data-stu-id="a36f2-103">Create a finished product (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a36f2-104">Þetta verk einblínir á að búa til tilbúin afurð.</span><span class="sxs-lookup"><span data-stu-id="a36f2-104">This task focuses on creating a finished product.</span></span> <span data-ttu-id="a36f2-105">Þetta er fyrsta verkið í línunni Útreikningur uppskrifta.</span><span class="sxs-lookup"><span data-stu-id="a36f2-105">It is the first task in the BOM calculation series.</span></span> <span data-ttu-id="a36f2-106">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="a36f2-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="a36f2-107">Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.</span><span class="sxs-lookup"><span data-stu-id="a36f2-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="a36f2-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="a36f2-108">Click New.</span></span>
3. <span data-ttu-id="a36f2-109">Í reitinn Afurðarnúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="a36f2-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="a36f2-110">Sláðu inn BOM_1 fyrir kynning.</span><span class="sxs-lookup"><span data-stu-id="a36f2-110">For the demonstration, type BOM_1.</span></span>  
4. <span data-ttu-id="a36f2-111">Í reitinn Vörulíkanaflokkur skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="a36f2-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="a36f2-112">Veldu STD.</span><span class="sxs-lookup"><span data-stu-id="a36f2-112">Select STD.</span></span> <span data-ttu-id="a36f2-113">STD stendur fyrir staðalkostnaður og er mest notaða líkan þegar unnið með kostnaðarútreikningur.</span><span class="sxs-lookup"><span data-stu-id="a36f2-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="a36f2-114">Í reitinn Vöruflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="a36f2-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="a36f2-115">Veljið t.d. Hljóðvinnsla.</span><span class="sxs-lookup"><span data-stu-id="a36f2-115">For example, select Audio.</span></span> <span data-ttu-id="a36f2-116">Þetta hefur engin áhrif á kostnaðarútreikningur.</span><span class="sxs-lookup"><span data-stu-id="a36f2-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="a36f2-117">Í reitinn Geymsluvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="a36f2-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="a36f2-118">Velja SiteWH.</span><span class="sxs-lookup"><span data-stu-id="a36f2-118">Select SiteWH.</span></span> <span data-ttu-id="a36f2-119">Aðeins Svæði og vöruhús verður notað í kynning.</span><span class="sxs-lookup"><span data-stu-id="a36f2-119">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="a36f2-120">Í reitinn Rakningarvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="a36f2-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="a36f2-121">Rakningarvíddir verða ekki notað í þessu dæmi, velja skal Ekkert.</span><span class="sxs-lookup"><span data-stu-id="a36f2-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="a36f2-122">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a36f2-122">Click OK.</span></span>
9. <span data-ttu-id="a36f2-123">Á Aðgerðasvæðinu skal smella á Stjórna birgðum.</span><span class="sxs-lookup"><span data-stu-id="a36f2-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="a36f2-124">Smellt er á sjálfgefnar pöntunarstillingar.</span><span class="sxs-lookup"><span data-stu-id="a36f2-124">Click Default order settings.</span></span>
11. <span data-ttu-id="a36f2-125">Í svæði Sjálfgefin pöntunargerð skal velja „Framleiðsla“.</span><span class="sxs-lookup"><span data-stu-id="a36f2-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="a36f2-126">Vegna þess að þetta er tilbúin afurð sem verður framleidd, velja Framleiðsla.</span><span class="sxs-lookup"><span data-stu-id="a36f2-126">Because this is a finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="a36f2-127">Í svæði „Innkaupasvæði“ slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="a36f2-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="a36f2-128">Fyrir kynning, velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="a36f2-128">For the demonstration, select Site 1.</span></span>  
13. <span data-ttu-id="a36f2-129">Í svæði Birgðasvæði slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="a36f2-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="a36f2-130">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="a36f2-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="a36f2-131">Í svæði Sölusvæði slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="a36f2-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="a36f2-132">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="a36f2-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="a36f2-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a36f2-133">Close the page.</span></span>

