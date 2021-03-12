---
title: Stjórna mælieiningu
description: Þessi ferli sýnir hvernig á að skilgreina mælieiningu, veita þýðingar fyrir eininguna og lýsingu hennar, og skilgreina umreikningsreglur fyrir tengdar einingar.
author: sorenva
manager: tfehr
ms.date: 07/08/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 71b478ca294719c20af9de16c27139aeca36bf07
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992296"
---
# <a name="manage-unit-of-measure"></a><span data-ttu-id="09263-103">Stjórna mælieiningu</span><span class="sxs-lookup"><span data-stu-id="09263-103">Manage unit of measure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="09263-104">Þessi ferli sýnir hvernig á að skilgreina mælieiningu, veita þýðingar fyrir eininguna og lýsingu hennar, og skilgreina umreikningsreglur fyrir tengdar einingar.</span><span class="sxs-lookup"><span data-stu-id="09263-104">This procedure shows how to define a unit of measure, provide translations for the unit and it's description, and define conversion rules for related units.</span></span> <span data-ttu-id="09263-105">Hægt er að fara í gegnum þetta ferli með því að nota sýnigögn eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="09263-105">You can walk through this procedure using demo data, or using your own data.</span></span>

1. <span data-ttu-id="09263-106">Farðu í **Skoðunarrúða > Kerfiseiningar > Afurðaupplýsingastjórnun > Afurðir > Viðhald útgefinna afurða**.</span><span class="sxs-lookup"><span data-stu-id="09263-106">Go to **Navigation pane > Modules > Product information management > Released product maintenance**.</span></span>
2. <span data-ttu-id="09263-107">Smelltu á **Einingar**.</span><span class="sxs-lookup"><span data-stu-id="09263-107">Click **Units**.</span></span>

## <a name="create-a-unit-of-measure"></a><span data-ttu-id="09263-108">Stofna mælieiningu</span><span class="sxs-lookup"><span data-stu-id="09263-108">Create a unit of measure</span></span>
1. <span data-ttu-id="09263-109">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="09263-109">Click **New**.</span></span>
2. <span data-ttu-id="09263-110">Í reitnum **Eining** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="09263-110">In the **Unit** field, type a value.</span></span> <span data-ttu-id="09263-111">Færið inn Kenni eða tákn sem nota á þegar vísað er í mælieiningu.</span><span class="sxs-lookup"><span data-stu-id="09263-111">Enter the ID or symbol to use when referring to the unit of measure.</span></span>  
3. <span data-ttu-id="09263-112">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="09263-112">In the **Description** field, type a value.</span></span> <span data-ttu-id="09263-113">Færið inn lýsandi heiti fyrir mælieiningu á tungumáli kerfisins.</span><span class="sxs-lookup"><span data-stu-id="09263-113">Enter a descriptive name for the unit of measure in the system language.</span></span>  
4. <span data-ttu-id="09263-114">Í reitnum **Einingaflokkur** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="09263-114">In the **Unit class** field, select an option.</span></span> <span data-ttu-id="09263-115">Mælieiningaflokkurinn skilgreinir hvaða röklegu flokkun, eins og svæði, fjöldi eða magni, mælieiningin er hluti af.</span><span class="sxs-lookup"><span data-stu-id="09263-115">The unit class defines what logical grouping, such as area, mass, or quantity, the unit of measure is part of.</span></span>  
5. <span data-ttu-id="09263-116">Í reitinn **Nákvæmni aukastafa** skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="09263-116">In the **Decimal precision** field, enter a number.</span></span> <span data-ttu-id="09263-117">Tilgreina fjölda aukastafa sem verður að slétta umreiknaðar mælieiningu í þegar útreikningi er lokið fyrir mælieiningu.</span><span class="sxs-lookup"><span data-stu-id="09263-117">Specify the number of decimals that the converted unit of measure must be rounded to when a calculation is completed for the unit of measure.</span></span>  
6. <span data-ttu-id="09263-118">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="09263-118">Click **Save**.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="09263-119">Skilgreina þýðingar eininga</span><span class="sxs-lookup"><span data-stu-id="09263-119">Define unit translations</span></span>
1. <span data-ttu-id="09263-120">Á **Aðgerðasvæði** er smellt á **Einingatexti**.</span><span class="sxs-lookup"><span data-stu-id="09263-120">On the **Action Pane**, click **Unit texts**.</span></span>
2. <span data-ttu-id="09263-121">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="09263-121">Click **New**.</span></span> <span data-ttu-id="09263-122">Einingatexti skal nota til að stofna þýðing fyrir Kenni eða tákn sem standa fyrir mælieiningu sem nota á á ytri skjöl í tungumálum fyrir viðskiptavin eða lánardrottin.</span><span class="sxs-lookup"><span data-stu-id="09263-122">Use unit text to create a translation of the ID or a symbol representing the unit of measure for use on external documents in customer- or vendor-specific languages.</span></span>  
3. <span data-ttu-id="09263-123">Í reitnum **Tungumál** skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="09263-123">In the **Language** field, enter or select a value.</span></span>
4. <span data-ttu-id="09263-124">Í reitnum **Texti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="09263-124">In the **Text** field, type a value.</span></span>
5. <span data-ttu-id="09263-125">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="09263-125">Click **Save**.</span></span>
6. <span data-ttu-id="09263-126">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="09263-126">Close the page.</span></span>
7. <span data-ttu-id="09263-127">Í **aðgerðasvæðinu** er smellt á **Þýddar lýsingar á einingum**.</span><span class="sxs-lookup"><span data-stu-id="09263-127">On the **Action Pane**, click **Translated unit descriptions**.</span></span>
8. <span data-ttu-id="09263-128">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="09263-128">Click **New**.</span></span> <span data-ttu-id="09263-129">Skilgreina lýsingar fyrir tiltekin tungumál fyrir mælieiningu.</span><span class="sxs-lookup"><span data-stu-id="09263-129">Define language-specific descriptions for the unit of measure.</span></span>  
9. <span data-ttu-id="09263-130">Í reitnum **Tungumál** skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="09263-130">In the **Language** field, enter or select a value.</span></span>
10. <span data-ttu-id="09263-131">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="09263-131">In the **Description** field, type a value.</span></span>
11. <span data-ttu-id="09263-132">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="09263-132">Click **Save**.</span></span>
12. <span data-ttu-id="09263-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="09263-133">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="09263-134">Skilgreina umreikningsreglur eininga</span><span class="sxs-lookup"><span data-stu-id="09263-134">Define unit conversion rules</span></span>
1. <span data-ttu-id="09263-135">Á **Aðgerðasvæðinu** er smellt á **Umreikningur eininga**.</span><span class="sxs-lookup"><span data-stu-id="09263-135">On the **Action Pane**, click **Unit conversions**.</span></span> <span data-ttu-id="09263-136">Skilgreina reglur til að umreikna mælieininguna í og frá öðrum mælieiningar í völdu einingaflokknum.</span><span class="sxs-lookup"><span data-stu-id="09263-136">Define rules for converting the unit of measure to and from other units of measure in the selected unit class.</span></span>  
2. <span data-ttu-id="09263-137">Smelltu á **Nýtt** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="09263-137">Click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="09263-138">Í reitnum **Stuðull** skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="09263-138">In the **Factor** field, enter a number.</span></span> <span data-ttu-id="09263-139">Umreiknistuðull milli Frá einingu og Til einingar.</span><span class="sxs-lookup"><span data-stu-id="09263-139">Conversion factor between the From unit and the To unit.</span></span> <span data-ttu-id="09263-140">til dæmis er umreiknistuðullinn úr sentímetrum í metra 100 þar sem 100 sentímetrar eru í einum metra.</span><span class="sxs-lookup"><span data-stu-id="09263-140">For example, the conversion factor from centimeter to meter is 100 because there are 100 centimeters in one meter.</span></span>  
4. <span data-ttu-id="09263-141">Í reitnum **Til einingar** skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="09263-141">In the **To unit** field, enter or select a value.</span></span>
5. <span data-ttu-id="09263-142">Í reitnum **Sléttun** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="09263-142">In the **Rounding** field, select an option.</span></span> <span data-ttu-id="09263-143">Skilgreina hvernig slétta skal umbreytt gildi.</span><span class="sxs-lookup"><span data-stu-id="09263-143">Define how the converted value should be rounded.</span></span>  
6. <span data-ttu-id="09263-144">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="09263-144">Click **OK**.</span></span>
7. <span data-ttu-id="09263-145">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="09263-145">Close the page.</span></span>

