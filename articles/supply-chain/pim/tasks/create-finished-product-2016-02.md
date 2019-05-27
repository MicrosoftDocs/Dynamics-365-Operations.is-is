---
title: Stofna tilbúin afurð (febrúar 2016)
description: Þetta verk einblínir á að búa til tilbúin afurð.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 44b3bf17c69f37e7a96c75345a3e4f27ba9eab50
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568444"
---
# <a name="create-a-finished-product-february-2016"></a><span data-ttu-id="61c29-103">Stofna tilbúin afurð (febrúar 2016)</span><span class="sxs-lookup"><span data-stu-id="61c29-103">Create a finished product (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="61c29-104">Þetta verk einblínir á að búa til tilbúin afurð.</span><span class="sxs-lookup"><span data-stu-id="61c29-104">This task focuses on creating a finished product.</span></span> <span data-ttu-id="61c29-105">Þetta er fyrsta verkið í línunni Útreikningur uppskrifta.</span><span class="sxs-lookup"><span data-stu-id="61c29-105">It is the first task in the BOM calculation series.</span></span> <span data-ttu-id="61c29-106">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="61c29-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="61c29-107">Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.</span><span class="sxs-lookup"><span data-stu-id="61c29-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="61c29-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="61c29-108">Click New.</span></span>
3. <span data-ttu-id="61c29-109">Í reitinn Afurðarnúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="61c29-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="61c29-110">Sláðu inn BOM_1 fyrir kynning.</span><span class="sxs-lookup"><span data-stu-id="61c29-110">For the demonstration, type BOM_1.</span></span>  
4. <span data-ttu-id="61c29-111">Í reitinn Vörulíkanaflokkur skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="61c29-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="61c29-112">Veldu STD.</span><span class="sxs-lookup"><span data-stu-id="61c29-112">Select STD.</span></span> <span data-ttu-id="61c29-113">STD stendur fyrir staðalkostnaður og er mest notaða líkan þegar unnið með kostnaðarútreikningur.</span><span class="sxs-lookup"><span data-stu-id="61c29-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="61c29-114">Í reitinn Vöruflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="61c29-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="61c29-115">Veljið t.d. Hljóðvinnsla.</span><span class="sxs-lookup"><span data-stu-id="61c29-115">For example, select Audio.</span></span> <span data-ttu-id="61c29-116">Þetta hefur engin áhrif á kostnaðarútreikningur.</span><span class="sxs-lookup"><span data-stu-id="61c29-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="61c29-117">Í reitinn Geymsluvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="61c29-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="61c29-118">Velja SiteWH.</span><span class="sxs-lookup"><span data-stu-id="61c29-118">Select SiteWH.</span></span> <span data-ttu-id="61c29-119">Aðeins Svæði og vöruhús verður notað í kynning.</span><span class="sxs-lookup"><span data-stu-id="61c29-119">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="61c29-120">Í reitinn Rakningarvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="61c29-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="61c29-121">Rakningarvíddir verða ekki notað í þessu dæmi, velja skal Ekkert.</span><span class="sxs-lookup"><span data-stu-id="61c29-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="61c29-122">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="61c29-122">Click OK.</span></span>
9. <span data-ttu-id="61c29-123">Á Aðgerðasvæðinu skal smella á Stjórna birgðum.</span><span class="sxs-lookup"><span data-stu-id="61c29-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="61c29-124">Smellt er á sjálfgefnar pöntunarstillingar.</span><span class="sxs-lookup"><span data-stu-id="61c29-124">Click Default order settings.</span></span>
11. <span data-ttu-id="61c29-125">Í svæði Sjálfgefin pöntunargerð skal velja „Framleiðsla“.</span><span class="sxs-lookup"><span data-stu-id="61c29-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="61c29-126">Vegna þess að þetta er tilbúin afurð sem verður framleidd, velja Framleiðsla.</span><span class="sxs-lookup"><span data-stu-id="61c29-126">Because this is a finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="61c29-127">Í svæði „Innkaupasvæði“ slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="61c29-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="61c29-128">Fyrir kynning, velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="61c29-128">For the demonstration, select Site 1.</span></span>  
13. <span data-ttu-id="61c29-129">Í svæði Birgðasvæði slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="61c29-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="61c29-130">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="61c29-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="61c29-131">Í svæði Sölusvæði slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="61c29-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="61c29-132">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="61c29-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="61c29-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="61c29-133">Close the page.</span></span>

