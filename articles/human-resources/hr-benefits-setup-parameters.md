---
title: Stilla færibreytur fríðindastjórnunar
description: Stilla færibreytur fyrir ávinningastjórnun í Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3e001c08751ea9c8bcab0e11a04b6cf639e51d1d
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429989"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="5684d-103">Stilla færibreytur fríðindastjórnunar</span><span class="sxs-lookup"><span data-stu-id="5684d-103">Set Benefits management parameters</span></span>

<span data-ttu-id="5684d-104">Áður en þú getur sett upp leyfisáætlanir í Microsoft Dynamics 365 Human Resources verður þú að stilla breytur stjórnunar fríðinda.</span><span class="sxs-lookup"><span data-stu-id="5684d-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="5684d-105">Þessar færibreytur setja sjálfgefin gildi, ástæðukóða og aðra valkosti.</span><span class="sxs-lookup"><span data-stu-id="5684d-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="5684d-106">Skilgreina almennar færibreytur</span><span class="sxs-lookup"><span data-stu-id="5684d-106">Configure general parameters</span></span>

1. <span data-ttu-id="5684d-107">Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Færibreytur**.</span><span class="sxs-lookup"><span data-stu-id="5684d-107">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="5684d-108">Í flipanum **Almennt** skal tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="5684d-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="5684d-109">Svæði</span><span class="sxs-lookup"><span data-stu-id="5684d-109">Field</span></span> | <span data-ttu-id="5684d-110">Lýsing</span><span class="sxs-lookup"><span data-stu-id="5684d-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5684d-111">**Land/svæði**</span><span class="sxs-lookup"><span data-stu-id="5684d-111">**Country/region**</span></span> | <span data-ttu-id="5684d-112">Reiturinn **Land / svæði** ákvarðar birtingarröð póstnúmera / ríkja.</span><span class="sxs-lookup"><span data-stu-id="5684d-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="5684d-113">Valið land birtist fyrst á fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="5684d-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="5684d-114">**Ástæðukóði skráningar**</span><span class="sxs-lookup"><span data-stu-id="5684d-114">**Enrollment reason code**</span></span> | <span data-ttu-id="5684d-115">Veldu sjálfgefinn ástæðukóða sem á að nota þegar áætlun starfsmanna er búin til við opna skráningu vinnslu.</span><span class="sxs-lookup"><span data-stu-id="5684d-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="5684d-116">**Ástæðukóði afturköllunar**</span><span class="sxs-lookup"><span data-stu-id="5684d-116">**Cancellation reason code**</span></span> | <span data-ttu-id="5684d-117">Ástæðukóðinn sem á að nota þegar bótaáætlun starfsmanna er felld niður.</span><span class="sxs-lookup"><span data-stu-id="5684d-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="5684d-118">Það birtist í valmynd meðan á uppsagnarferlinu stendur.</span><span class="sxs-lookup"><span data-stu-id="5684d-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="5684d-119">Notendur geta breytt því **Ástæða kóða fyrir afpöntun** ef nauðsynlegt er.</span><span class="sxs-lookup"><span data-stu-id="5684d-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="5684d-120">**Ástæðukóði enduropnunar**</span><span class="sxs-lookup"><span data-stu-id="5684d-120">**Reopen reason code**</span></span> | <span data-ttu-id="5684d-121">Ástæðukóðinn sem á að nota þegar bótaáætlun starfsmanna er enduropnuð.</span><span class="sxs-lookup"><span data-stu-id="5684d-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="5684d-122">Það birtist í valmynd meðan á uppsagnarferlinu stendur.</span><span class="sxs-lookup"><span data-stu-id="5684d-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="5684d-123">Notendur geta breytt **Enduropna ástæðukóða** ef nauðsynlegt er.</span><span class="sxs-lookup"><span data-stu-id="5684d-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="5684d-124">**Ástæðukóði viðburðar**</span><span class="sxs-lookup"><span data-stu-id="5684d-124">**Life event reason code**</span></span> | <span data-ttu-id="5684d-125">Ástæðukóðinn sem á að nota þegar lífatburður á sér stað.</span><span class="sxs-lookup"><span data-stu-id="5684d-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="5684d-126">**Ástæðukóði breytingar á hlutfalli**</span><span class="sxs-lookup"><span data-stu-id="5684d-126">**Rate change reason code**</span></span> | <span data-ttu-id="5684d-127">Ástæðukóðinn sem á að nota við að hætta við og opna bótaráætlun starfsmanna meðan á breytingu á gengisbreytingum stendur.</span><span class="sxs-lookup"><span data-stu-id="5684d-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="5684d-128">Það gefur til kynna hvaða færslum var breytt með uppfærsluferli gengisbreytinga.</span><span class="sxs-lookup"><span data-stu-id="5684d-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="5684d-129">**Hæfur til nýráðningar**</span><span class="sxs-lookup"><span data-stu-id="5684d-129">**New hire eligible**</span></span> | <span data-ttu-id="5684d-130">Tilgreinir hvort nýráðningar séu gjaldgengar.</span><span class="sxs-lookup"><span data-stu-id="5684d-130">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="5684d-131">**Skráningartímabil nýrrar ráðningar**</span><span class="sxs-lookup"><span data-stu-id="5684d-131">**New hire enrollment period**</span></span> | <span data-ttu-id="5684d-132">Tímabilið sem nýskráning á leigu er leyfð.</span><span class="sxs-lookup"><span data-stu-id="5684d-132">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="5684d-133">**Athugið**: Þessi stilling gengur framhjá nýjum nýskráningartímabilum sem þú stillir í hæfisreglu áætlunarinnar.</span><span class="sxs-lookup"><span data-stu-id="5684d-133">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> | 
   | <span data-ttu-id="5684d-134">**Viðburðir eru virkir**</span><span class="sxs-lookup"><span data-stu-id="5684d-134">**Life events enabled**</span></span> | <span data-ttu-id="5684d-135">Virkjar viðburði.</span><span class="sxs-lookup"><span data-stu-id="5684d-135">Enables life events.</span></span> |
   | <span data-ttu-id="5684d-136">**Fela eyðublöð eldri fríðinda**</span><span class="sxs-lookup"><span data-stu-id="5684d-136">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="5684d-137">Leyfir þér að fela gömul fríðindaeyðublöð.</span><span class="sxs-lookup"><span data-stu-id="5684d-137">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="5684d-138">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5684d-138">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="5684d-139">Grunnstilla sjálfsafgreiðslufæribreytur starfsmanns</span><span class="sxs-lookup"><span data-stu-id="5684d-139">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="5684d-140">Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Færibreytur**.</span><span class="sxs-lookup"><span data-stu-id="5684d-140">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="5684d-141">Í flipanum **Sjálfsafgreiðsla starfsmanns** skal tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="5684d-141">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="5684d-142">Svæði</span><span class="sxs-lookup"><span data-stu-id="5684d-142">Field</span></span> | <span data-ttu-id="5684d-143">Lýsing</span><span class="sxs-lookup"><span data-stu-id="5684d-143">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5684d-144">**Staðfesting á fríðindum**</span><span class="sxs-lookup"><span data-stu-id="5684d-144">**Benefit verification**</span></span> | <span data-ttu-id="5684d-145">Sannprófunartextinn sem á að nota við sjálfsafgreiðslukassa.</span><span class="sxs-lookup"><span data-stu-id="5684d-145">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="5684d-146">**Sjálfvirkt val á fulltrúum**</span><span class="sxs-lookup"><span data-stu-id="5684d-146">**Auto select designees**</span></span> | <span data-ttu-id="5684d-147">Tilgreinir hvort sjálfkrafa skuli velja á framfæri og styrkþega miðað við hæfi þeirra fyrir áætlunarkosti.</span><span class="sxs-lookup"><span data-stu-id="5684d-147">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="5684d-148">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5684d-148">Select **Save**.</span></span>
