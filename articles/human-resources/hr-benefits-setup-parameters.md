---
title: Stilla færibreytur fríðindastjórnunar og sjálfsafgreiðslu starfsmanna fyrir öll fyrirtæki
description: Skilgreina færibreytur fyrir fríðindastjórnun og sjálfsafgreiðslu starfsmanna í Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 10f5310ba4feba4a196d02c406ff3217637e447e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791486"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a><span data-ttu-id="cc94f-103">Stilla færibreytur fríðindastjórnunar og sjálfsafgreiðslu starfsmanna fyrir öll fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="cc94f-103">Set Benefits management and Employee self-service parameters for all companies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="cc94f-104">Áður en hægt er að setja upp fríðindaáætlanir í Microsoft Dynamics 365 Human Resources þarf að skilgreina færibreytur fyrir fríðindastjórnun.</span><span class="sxs-lookup"><span data-stu-id="cc94f-104">Before you can set up benefit plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="cc94f-105">Þessar færibreytur setja sjálfgefin gildi, ástæðukóða og aðra valkosti.</span><span class="sxs-lookup"><span data-stu-id="cc94f-105">These parameters set default values, reason codes, and other options.</span></span> 

## <a name="configure-general-parameters"></a><span data-ttu-id="cc94f-106">Skilgreina almennar færibreytur</span><span class="sxs-lookup"><span data-stu-id="cc94f-106">Configure general parameters</span></span>

1. <span data-ttu-id="cc94f-107">Í **Fríðindastjórnun** vinnusvæðinu, undir **Uppsetning**, skaltu velja **Samnýttar færibreytur mannauðs**.</span><span class="sxs-lookup"><span data-stu-id="cc94f-107">In the **Benefits management** workspace, under **Setup**, select **Human Resources Shared Parameters**.</span></span>

2. <span data-ttu-id="cc94f-108">Í flipanum **Fríðindastjórnun** skal tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="cc94f-108">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="cc94f-109">Svæði</span><span class="sxs-lookup"><span data-stu-id="cc94f-109">Field</span></span> | <span data-ttu-id="cc94f-110">lýsing</span><span class="sxs-lookup"><span data-stu-id="cc94f-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="cc94f-111">**Land/svæði**</span><span class="sxs-lookup"><span data-stu-id="cc94f-111">**Country/region**</span></span> | <span data-ttu-id="cc94f-112">Reiturinn **Land / svæði** ákvarðar birtingarröð póstnúmera / ríkja.</span><span class="sxs-lookup"><span data-stu-id="cc94f-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="cc94f-113">Valið land birtist fyrst á fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="cc94f-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="cc94f-114">**Ástæðukóði skráningar**</span><span class="sxs-lookup"><span data-stu-id="cc94f-114">**Enrollment reason code**</span></span> | <span data-ttu-id="cc94f-115">Veldu sjálfgefinn ástæðukóða sem á að nota þegar áætlun starfsmanna er búin til við opna skráningu vinnslu.</span><span class="sxs-lookup"><span data-stu-id="cc94f-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="cc94f-116">**Ástæðukóði afturköllunar**</span><span class="sxs-lookup"><span data-stu-id="cc94f-116">**Cancellation reason code**</span></span> | <span data-ttu-id="cc94f-117">Ástæðukóðinn sem á að nota þegar bótaáætlun starfsmanna er felld niður.</span><span class="sxs-lookup"><span data-stu-id="cc94f-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="cc94f-118">Það birtist í valmynd meðan á uppsagnarferlinu stendur.</span><span class="sxs-lookup"><span data-stu-id="cc94f-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="cc94f-119">Notendur geta breytt því **Ástæða kóða fyrir afpöntun** ef nauðsynlegt er.</span><span class="sxs-lookup"><span data-stu-id="cc94f-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="cc94f-120">**Ástæðukóði enduropnunar**</span><span class="sxs-lookup"><span data-stu-id="cc94f-120">**Reopen reason code**</span></span> | <span data-ttu-id="cc94f-121">Ástæðukóðinn sem á að nota þegar bótaáætlun starfsmanna er enduropnuð.</span><span class="sxs-lookup"><span data-stu-id="cc94f-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="cc94f-122">Það birtist í valmynd meðan á uppsagnarferlinu stendur.</span><span class="sxs-lookup"><span data-stu-id="cc94f-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="cc94f-123">Notendur geta breytt **Enduropna ástæðukóða** ef nauðsynlegt er.</span><span class="sxs-lookup"><span data-stu-id="cc94f-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="cc94f-124">**Ástæðukóði viðburðar**</span><span class="sxs-lookup"><span data-stu-id="cc94f-124">**Life event reason code**</span></span> | <span data-ttu-id="cc94f-125">Ástæðukóðinn sem á að nota þegar lífatburður á sér stað.</span><span class="sxs-lookup"><span data-stu-id="cc94f-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="cc94f-126">**Ástæðukóði breytingar á hlutfalli**</span><span class="sxs-lookup"><span data-stu-id="cc94f-126">**Rate change reason code**</span></span> | <span data-ttu-id="cc94f-127">Ástæðukóðinn sem á að nota við að hætta við og opna bótaráætlun starfsmanna meðan á breytingu á gengisbreytingum stendur.</span><span class="sxs-lookup"><span data-stu-id="cc94f-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="cc94f-128">Það gefur til kynna hvaða færslum var breytt með uppfærsluferli gengisbreytinga.</span><span class="sxs-lookup"><span data-stu-id="cc94f-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="cc94f-129">**Fríðindi árslauna**</span><span class="sxs-lookup"><span data-stu-id="cc94f-129">**Benefits annual salary**</span></span> | <span data-ttu-id="cc94f-130">Gerir þér kleift að stilla **Árleg launatengd fríðindi** upphæð fyrir starfsmann.</span><span class="sxs-lookup"><span data-stu-id="cc94f-130">Enables you to set a **Benefits annual salary** amount for an employee.</span></span> <span data-ttu-id="cc94f-131">Human Resources notar **Árleg launatengd fríðindi** upphæð við ákvörðun tryggingaupphæðar, í stað árlega upphæð fastra launa.</span><span class="sxs-lookup"><span data-stu-id="cc94f-131">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> |
   | <span data-ttu-id="cc94f-132">**Hæfur til nýráðningar**</span><span class="sxs-lookup"><span data-stu-id="cc94f-132">**New hire eligible**</span></span> | <span data-ttu-id="cc94f-133">Tilgreinir hvort nýráðningar séu gjaldgengar.</span><span class="sxs-lookup"><span data-stu-id="cc94f-133">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="cc94f-134">**Skráningartímabil nýrrar ráðningar**</span><span class="sxs-lookup"><span data-stu-id="cc94f-134">**New hire enrollment period**</span></span> | <span data-ttu-id="cc94f-135">Tímabilið sem nýskráning á leigu er leyfð.</span><span class="sxs-lookup"><span data-stu-id="cc94f-135">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="cc94f-136">**Athugið**: Þessi stilling gengur framhjá nýjum nýskráningartímabilum sem þú stillir í hæfisreglu áætlunarinnar.</span><span class="sxs-lookup"><span data-stu-id="cc94f-136">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> |
   | <span data-ttu-id="cc94f-137">**Sjálfgefin greiðslutíðni**</span><span class="sxs-lookup"><span data-stu-id="cc94f-137">**Default pay frequency**</span></span> | <span data-ttu-id="cc94f-138">Sjálfgefin greiðslutíðni sem á að nota þegar nýjum starfskröftum er bætt við.</span><span class="sxs-lookup"><span data-stu-id="cc94f-138">The default pay frequency to use when new workers are added.</span></span> |
   | <span data-ttu-id="cc94f-139">**Viðburðir eru virkir**</span><span class="sxs-lookup"><span data-stu-id="cc94f-139">**Life events enabled**</span></span> | <span data-ttu-id="cc94f-140">Virkjar viðburði.</span><span class="sxs-lookup"><span data-stu-id="cc94f-140">Enables life events.</span></span> |
   | <span data-ttu-id="cc94f-141">**Fela eyðublöð eldri fríðinda**</span><span class="sxs-lookup"><span data-stu-id="cc94f-141">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="cc94f-142">Leyfir þér að fela gömul fríðindaeyðublöð.</span><span class="sxs-lookup"><span data-stu-id="cc94f-142">Allows you to hide legacy benefit forms.</span></span> |
   | <span data-ttu-id="cc94f-143">**Staðfesting á fríðindum**</span><span class="sxs-lookup"><span data-stu-id="cc94f-143">**Benefit verification**</span></span> | <span data-ttu-id="cc94f-144">Sannprófunartextinn sem á að nota við sjálfsafgreiðslukassa.</span><span class="sxs-lookup"><span data-stu-id="cc94f-144">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="cc94f-145">**Sjálfvirkt val á fulltrúum**</span><span class="sxs-lookup"><span data-stu-id="cc94f-145">**Auto select designees**</span></span> | <span data-ttu-id="cc94f-146">Tilgreinir hvort sjálfkrafa skuli velja á framfæri og styrkþega miðað við hæfi þeirra fyrir áætlunarkosti.</span><span class="sxs-lookup"><span data-stu-id="cc94f-146">Specifies whether to automatically select dependents and beneficiaries, based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="cc94f-147">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="cc94f-147">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="cc94f-148">Stilla færibreytur sjálfsafgreiðslu starfsmanns</span><span class="sxs-lookup"><span data-stu-id="cc94f-148">Configure Employee self-service parameters</span></span>

1. <span data-ttu-id="cc94f-149">Í **Fríðindastjórnun** vinnusvæðinu, undir **Uppsetning**, skal velja **Færibreytur mannauðs**.</span><span class="sxs-lookup"><span data-stu-id="cc94f-149">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="cc94f-150">Í flipanum **Fríðindastjórnun** skal tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="cc94f-150">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="cc94f-151">Svæði</span><span class="sxs-lookup"><span data-stu-id="cc94f-151">Field</span></span> | <span data-ttu-id="cc94f-152">lýsing</span><span class="sxs-lookup"><span data-stu-id="cc94f-152">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="cc94f-153">**Staðfesting á fríðindum**</span><span class="sxs-lookup"><span data-stu-id="cc94f-153">**Benefit verification**</span></span> | <span data-ttu-id="cc94f-154">Sannprófunartextinn sem á að nota við sjálfsafgreiðslukassa.</span><span class="sxs-lookup"><span data-stu-id="cc94f-154">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="cc94f-155">**Sjálfvirkt val á fulltrúum**</span><span class="sxs-lookup"><span data-stu-id="cc94f-155">**Auto select designees**</span></span> | <span data-ttu-id="cc94f-156">Tilgreinir hvort sjálfkrafa skuli velja á framfæri og styrkþega miðað við hæfi þeirra fyrir áætlunarkosti.</span><span class="sxs-lookup"><span data-stu-id="cc94f-156">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="cc94f-157">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="cc94f-157">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]