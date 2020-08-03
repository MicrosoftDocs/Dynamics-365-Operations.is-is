---
title: Stilla færibreytur fríðindastjórnunar
description: Stilla færibreytur fyrir ávinningastjórnun í Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 07/16/2020
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
ms.openlocfilehash: 85bbe5d3b422f2f29f1d1fe8ee269b407da691c2
ms.sourcegitcommit: 9dc5c7dd5877cc6e7cd0059d173bcd8052ba13bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/16/2020
ms.locfileid: "3599357"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="469d9-103">Stilla færibreytur fríðindastjórnunar</span><span class="sxs-lookup"><span data-stu-id="469d9-103">Set Benefits management parameters</span></span>

<span data-ttu-id="469d9-104">Áður en þú getur sett upp leyfisáætlanir í Microsoft Dynamics 365 Human Resources verður þú að stilla breytur stjórnunar fríðinda.</span><span class="sxs-lookup"><span data-stu-id="469d9-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="469d9-105">Þessar færibreytur setja sjálfgefin gildi, ástæðukóða og aðra valkosti.</span><span class="sxs-lookup"><span data-stu-id="469d9-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="469d9-106">Skilgreina almennar færibreytur</span><span class="sxs-lookup"><span data-stu-id="469d9-106">Configure general parameters</span></span>

1. <span data-ttu-id="469d9-107">Í **Fríðindastjórnun** vinnusvæðinu, undir **Uppsetning**, skaltu velja **Samnýttar færibreytur mannauðs**.</span><span class="sxs-lookup"><span data-stu-id="469d9-107">In the **Benefits management** workspace, under **Setup**, select **Human Resources Shared Parameters**.</span></span>

2. <span data-ttu-id="469d9-108">Í flipanum **Almennt** skal tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="469d9-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="469d9-109">Svæði</span><span class="sxs-lookup"><span data-stu-id="469d9-109">Field</span></span> | <span data-ttu-id="469d9-110">Lýsing</span><span class="sxs-lookup"><span data-stu-id="469d9-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="469d9-111">**Land/svæði**</span><span class="sxs-lookup"><span data-stu-id="469d9-111">**Country/region**</span></span> | <span data-ttu-id="469d9-112">Reiturinn **Land / svæði** ákvarðar birtingarröð póstnúmera / ríkja.</span><span class="sxs-lookup"><span data-stu-id="469d9-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="469d9-113">Valið land birtist fyrst á fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="469d9-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="469d9-114">**Ástæðukóði skráningar**</span><span class="sxs-lookup"><span data-stu-id="469d9-114">**Enrollment reason code**</span></span> | <span data-ttu-id="469d9-115">Veldu sjálfgefinn ástæðukóða sem á að nota þegar áætlun starfsmanna er búin til við opna skráningu vinnslu.</span><span class="sxs-lookup"><span data-stu-id="469d9-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="469d9-116">**Ástæðukóði afturköllunar**</span><span class="sxs-lookup"><span data-stu-id="469d9-116">**Cancellation reason code**</span></span> | <span data-ttu-id="469d9-117">Ástæðukóðinn sem á að nota þegar bótaáætlun starfsmanna er felld niður.</span><span class="sxs-lookup"><span data-stu-id="469d9-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="469d9-118">Það birtist í valmynd meðan á uppsagnarferlinu stendur.</span><span class="sxs-lookup"><span data-stu-id="469d9-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="469d9-119">Notendur geta breytt því **Ástæða kóða fyrir afpöntun** ef nauðsynlegt er.</span><span class="sxs-lookup"><span data-stu-id="469d9-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="469d9-120">**Ástæðukóði enduropnunar**</span><span class="sxs-lookup"><span data-stu-id="469d9-120">**Reopen reason code**</span></span> | <span data-ttu-id="469d9-121">Ástæðukóðinn sem á að nota þegar bótaáætlun starfsmanna er enduropnuð.</span><span class="sxs-lookup"><span data-stu-id="469d9-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="469d9-122">Það birtist í valmynd meðan á uppsagnarferlinu stendur.</span><span class="sxs-lookup"><span data-stu-id="469d9-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="469d9-123">Notendur geta breytt **Enduropna ástæðukóða** ef nauðsynlegt er.</span><span class="sxs-lookup"><span data-stu-id="469d9-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="469d9-124">**Ástæðukóði viðburðar**</span><span class="sxs-lookup"><span data-stu-id="469d9-124">**Life event reason code**</span></span> | <span data-ttu-id="469d9-125">Ástæðukóðinn sem á að nota þegar lífatburður á sér stað.</span><span class="sxs-lookup"><span data-stu-id="469d9-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="469d9-126">**Ástæðukóði breytingar á hlutfalli**</span><span class="sxs-lookup"><span data-stu-id="469d9-126">**Rate change reason code**</span></span> | <span data-ttu-id="469d9-127">Ástæðukóðinn sem á að nota við að hætta við og opna bótaráætlun starfsmanna meðan á breytingu á gengisbreytingum stendur.</span><span class="sxs-lookup"><span data-stu-id="469d9-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="469d9-128">Það gefur til kynna hvaða færslum var breytt með uppfærsluferli gengisbreytinga.</span><span class="sxs-lookup"><span data-stu-id="469d9-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="469d9-129">**Fríðindi árslauna**</span><span class="sxs-lookup"><span data-stu-id="469d9-129">**Benefits annual salary**</span></span> | <span data-ttu-id="469d9-130">Gerir þér kleift að stilla **Árleg launatengd fríðindi** upphæð fyrir starfsmann.</span><span class="sxs-lookup"><span data-stu-id="469d9-130">Enables you to set a **Benefits annual salary** amount for an employee.</span></span> <span data-ttu-id="469d9-131">Human Resources notar **Árleg launatengd fríðindi** upphæð við ákvörðun tryggingaupphæðar, í stað árlega upphæð fastra launa.</span><span class="sxs-lookup"><span data-stu-id="469d9-131">Human Resources will use the **Benefits annual salary** amount when determing coverage amounts, instead of the fixed compensation annual amount.</span></span> |
   | <span data-ttu-id="469d9-132">**Hæfur til nýráðningar**</span><span class="sxs-lookup"><span data-stu-id="469d9-132">**New hire eligible**</span></span> | <span data-ttu-id="469d9-133">Tilgreinir hvort nýráðningar séu gjaldgengar.</span><span class="sxs-lookup"><span data-stu-id="469d9-133">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="469d9-134">**Skráningartímabil nýrrar ráðningar**</span><span class="sxs-lookup"><span data-stu-id="469d9-134">**New hire enrollment period**</span></span> | <span data-ttu-id="469d9-135">Tímabilið sem nýskráning á leigu er leyfð.</span><span class="sxs-lookup"><span data-stu-id="469d9-135">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="469d9-136">**Athugið**: Þessi stilling gengur framhjá nýjum nýskráningartímabilum sem þú stillir í hæfisreglu áætlunarinnar.</span><span class="sxs-lookup"><span data-stu-id="469d9-136">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> |
   | <span data-ttu-id="469d9-137">**Sjálfgefin greiðslutíðni**</span><span class="sxs-lookup"><span data-stu-id="469d9-137">**Default pay frequency**</span></span> | <span data-ttu-id="469d9-138">Sjálfgefin greiðslutíðni sem á að nota þegar nýjum starfskröftum er bætt við.</span><span class="sxs-lookup"><span data-stu-id="469d9-138">The default pay frequency to use when new workers are added.</span></span> |
   | <span data-ttu-id="469d9-139">**Viðburðir eru virkir**</span><span class="sxs-lookup"><span data-stu-id="469d9-139">**Life events enabled**</span></span> | <span data-ttu-id="469d9-140">Virkjar viðburði.</span><span class="sxs-lookup"><span data-stu-id="469d9-140">Enables life events.</span></span> |
   | <span data-ttu-id="469d9-141">**Fela eyðublöð eldri fríðinda**</span><span class="sxs-lookup"><span data-stu-id="469d9-141">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="469d9-142">Leyfir þér að fela gömul fríðindaeyðublöð.</span><span class="sxs-lookup"><span data-stu-id="469d9-142">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="469d9-143">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="469d9-143">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="469d9-144">Grunnstilla sjálfsafgreiðslufæribreytur starfsmanns</span><span class="sxs-lookup"><span data-stu-id="469d9-144">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="469d9-145">Í **Fríðindastjórnun** vinnusvæðinu, undir **Uppsetning**, skal velja **Færibreytur mannauðs**.</span><span class="sxs-lookup"><span data-stu-id="469d9-145">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="469d9-146">Í flipanum **Sjálfsafgreiðsla starfsmanns** skal tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="469d9-146">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="469d9-147">Svæði</span><span class="sxs-lookup"><span data-stu-id="469d9-147">Field</span></span> | <span data-ttu-id="469d9-148">Lýsing</span><span class="sxs-lookup"><span data-stu-id="469d9-148">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="469d9-149">**Staðfesting á fríðindum**</span><span class="sxs-lookup"><span data-stu-id="469d9-149">**Benefit verification**</span></span> | <span data-ttu-id="469d9-150">Sannprófunartextinn sem á að nota við sjálfsafgreiðslukassa.</span><span class="sxs-lookup"><span data-stu-id="469d9-150">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="469d9-151">**Sjálfvirkt val á fulltrúum**</span><span class="sxs-lookup"><span data-stu-id="469d9-151">**Auto select designees**</span></span> | <span data-ttu-id="469d9-152">Tilgreinir hvort sjálfkrafa skuli velja á framfæri og styrkþega miðað við hæfi þeirra fyrir áætlunarkosti.</span><span class="sxs-lookup"><span data-stu-id="469d9-152">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="469d9-153">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="469d9-153">Select **Save**.</span></span>
