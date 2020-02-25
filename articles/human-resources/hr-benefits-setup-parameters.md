---
title: Stilla færibreytur fríðindastjórnunar
description: Stilla færibreytur fyrir ávinningastjórnun í Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ab9b1fc78ce42479d9265b80337adf899cec3866
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009419"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="c6d59-103">Stilla færibreytur fríðindastjórnunar</span><span class="sxs-lookup"><span data-stu-id="c6d59-103">Set Benefits management parameters</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="c6d59-104">Áður en þú getur sett upp leyfisáætlanir í Microsoft Dynamics 365 Human Resources, þú þarft að stilla breytur stjórnunar fríðinda.</span><span class="sxs-lookup"><span data-stu-id="c6d59-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you need to configure Benefits management parameters.</span></span> <span data-ttu-id="c6d59-105">Þessar færibreytur setja sjálfgefin gildi, ástæðukóða og aðra valkosti.</span><span class="sxs-lookup"><span data-stu-id="c6d59-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="c6d59-106">Skilgreina almennar færibreytur</span><span class="sxs-lookup"><span data-stu-id="c6d59-106">Configure general parameters</span></span>

1. <span data-ttu-id="c6d59-107">Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Færibreytur**.</span><span class="sxs-lookup"><span data-stu-id="c6d59-107">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="c6d59-108">Í flipanum **Almennt** skal tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="c6d59-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="c6d59-109">Svæði</span><span class="sxs-lookup"><span data-stu-id="c6d59-109">Field</span></span> | <span data-ttu-id="c6d59-110">Lýsing</span><span class="sxs-lookup"><span data-stu-id="c6d59-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="c6d59-111">**Land/svæði**</span><span class="sxs-lookup"><span data-stu-id="c6d59-111">**Country/region**</span></span> | <span data-ttu-id="c6d59-112">Reiturinn **Land / svæði** ákvarðar birtingarröð póstnúmera / ríkja.</span><span class="sxs-lookup"><span data-stu-id="c6d59-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="c6d59-113">Valið land birtist fyrst á fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="c6d59-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="c6d59-114">**Ástæðukóði skráningar**</span><span class="sxs-lookup"><span data-stu-id="c6d59-114">**Enrollment reason code**</span></span> | <span data-ttu-id="c6d59-115">Veldu sjálfgefinn ástæðukóða sem á að nota þegar áætlun starfsmanna er búin til við opna skráningu vinnslu.</span><span class="sxs-lookup"><span data-stu-id="c6d59-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="c6d59-116">**Ástæðukóði afturköllunar**</span><span class="sxs-lookup"><span data-stu-id="c6d59-116">**Cancellation reason code**</span></span> | <span data-ttu-id="c6d59-117">Ástæðukóðinn sem á að nota þegar bótaáætlun starfsmanna er felld niður.</span><span class="sxs-lookup"><span data-stu-id="c6d59-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="c6d59-118">Það birtist í valmynd meðan á uppsagnarferlinu stendur.</span><span class="sxs-lookup"><span data-stu-id="c6d59-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="c6d59-119">Notendur geta breytt því **Ástæða kóða fyrir afpöntun** ef nauðsynlegt er.</span><span class="sxs-lookup"><span data-stu-id="c6d59-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="c6d59-120">**Ástæðukóði enduropnunar**</span><span class="sxs-lookup"><span data-stu-id="c6d59-120">**Reopen reason code**</span></span> | <span data-ttu-id="c6d59-121">Ástæðukóðinn sem á að nota þegar bótaáætlun starfsmanna er enduropnuð.</span><span class="sxs-lookup"><span data-stu-id="c6d59-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="c6d59-122">Það birtist í valmynd meðan á uppsagnarferlinu stendur.</span><span class="sxs-lookup"><span data-stu-id="c6d59-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="c6d59-123">Notendur geta breytt **Enduropna ástæðukóða** ef nauðsynlegt er.</span><span class="sxs-lookup"><span data-stu-id="c6d59-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="c6d59-124">**Ástæðukóði viðburðar**</span><span class="sxs-lookup"><span data-stu-id="c6d59-124">**Life event reason code**</span></span> | <span data-ttu-id="c6d59-125">Ástæðukóðinn sem á að nota þegar lífatburður á sér stað.</span><span class="sxs-lookup"><span data-stu-id="c6d59-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="c6d59-126">**Ástæðukóði breytingar á hlutfalli**</span><span class="sxs-lookup"><span data-stu-id="c6d59-126">**Rate change reason code**</span></span> | <span data-ttu-id="c6d59-127">Ástæðukóðinn sem á að nota við að hætta við og opna bótaráætlun starfsmanna meðan á breytingu á gengisbreytingum stendur.</span><span class="sxs-lookup"><span data-stu-id="c6d59-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="c6d59-128">Það gefur til kynna hvaða færslum var breytt með uppfærsluferli gengisbreytinga.</span><span class="sxs-lookup"><span data-stu-id="c6d59-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="c6d59-129">**Hæfur til nýráðningar**</span><span class="sxs-lookup"><span data-stu-id="c6d59-129">**New hire eligible**</span></span> | <span data-ttu-id="c6d59-130">Tilgreinir hvort nýráðningar séu gjaldgengar.</span><span class="sxs-lookup"><span data-stu-id="c6d59-130">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="c6d59-131">**Skráningartímabil nýrrar ráðningar**</span><span class="sxs-lookup"><span data-stu-id="c6d59-131">**New hire enrollment period**</span></span> | <span data-ttu-id="c6d59-132">Tímabilið sem nýskráning á leigu er leyfð.</span><span class="sxs-lookup"><span data-stu-id="c6d59-132">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="c6d59-133">**Athugið**: Þessi stilling gengur framhjá nýjum nýskráningartímabilum sem þú stillir í hæfisreglu áætlunarinnar.</span><span class="sxs-lookup"><span data-stu-id="c6d59-133">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> | 
   | <span data-ttu-id="c6d59-134">**Aukning árslauna**</span><span class="sxs-lookup"><span data-stu-id="c6d59-134">**Annual salary enhancement**</span></span> | <span data-ttu-id="c6d59-135">Tilgreinir hvort reikna eigi sjálfkrafa **Árleg hlunnindi** upphæð í **Upplýsingar um atvinnubætur**.</span><span class="sxs-lookup"><span data-stu-id="c6d59-135">Specifies whether to automatically calculate the **Annual benefit salary** amount in **Employment Benefit Details**.</span></span> <span data-ttu-id="c6d59-136">Það er byggt á starfsmanni **Fast hlutfall bóta**, **Meðaltími** og **Greiðslutíðni**.</span><span class="sxs-lookup"><span data-stu-id="c6d59-136">It's based on the employee’s **Fixed compensation pay rate**, **Average hours**, and **Payment frequency**.</span></span></br></br><span data-ttu-id="c6d59-137">**Meðaltími** x **Fast launagengi** x **Greiðslutíðni** (# launatímabil) = **Árleg hlunnindi**</span><span class="sxs-lookup"><span data-stu-id="c6d59-137">**Average hours** x **Fixed pay rate** x **Payment frequency** (# of pay periods) = **Annual benefit salary**</span></span> </br></br><span data-ttu-id="c6d59-138">Ef eitthvað af gildunum í **Meðaltími**, **Fast hlutfall bóta** eða **Greiðslutíðni** reitir breytast, kerfið reiknar sjálfkrafa út starfsmanninn **Árleg hlunnindi** upphæð miðað við breytt gildi.</span><span class="sxs-lookup"><span data-stu-id="c6d59-138">If any of the values in the **Average hours**, **Fixed compensation pay rate**, or **Payment frequency** fields change, the system automatically recalculates the employee’s **Annual benefit salary** amount based on the changed values.</span></span> <span data-ttu-id="c6d59-139">Kerfið býr til **Dagsetning gildi** skrá til að bera kennsl á nákvæma dagsetningu og tíma breytingin átti sér stað.</span><span class="sxs-lookup"><span data-stu-id="c6d59-139">The system creates a **Date effective** record to identify the exact date and time the change occurred.</span></span> <span data-ttu-id="c6d59-140">Þú getur breytt handvirkt **Árleg hlunnindi** upphæð ef nauðsyn krefur.</span><span class="sxs-lookup"><span data-stu-id="c6d59-140">You can manually edit the **Annual benefit salary** amount if necessary.</span></span> |
   | <span data-ttu-id="c6d59-141">**Viðburðir eru virkir**</span><span class="sxs-lookup"><span data-stu-id="c6d59-141">**Life events enabled**</span></span> | <span data-ttu-id="c6d59-142">Virkjar viðburði.</span><span class="sxs-lookup"><span data-stu-id="c6d59-142">Enables life events.</span></span> |
   | <span data-ttu-id="c6d59-143">**Fela eyðublöð eldri fríðinda**</span><span class="sxs-lookup"><span data-stu-id="c6d59-143">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="c6d59-144">Leyfir þér að fela gömul fríðindaeyðublöð.</span><span class="sxs-lookup"><span data-stu-id="c6d59-144">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="c6d59-145">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="c6d59-145">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="c6d59-146">Grunnstilla sjálfsafgreiðslufæribreytur starfsmanns</span><span class="sxs-lookup"><span data-stu-id="c6d59-146">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="c6d59-147">Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Færibreytur**.</span><span class="sxs-lookup"><span data-stu-id="c6d59-147">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="c6d59-148">Í flipanum **Sjálfsafgreiðsla starfsmanns** skal tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="c6d59-148">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="c6d59-149">Svæði</span><span class="sxs-lookup"><span data-stu-id="c6d59-149">Field</span></span> | <span data-ttu-id="c6d59-150">Lýsing</span><span class="sxs-lookup"><span data-stu-id="c6d59-150">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="c6d59-151">**Staðfesting á fríðindum**</span><span class="sxs-lookup"><span data-stu-id="c6d59-151">**Benefit verification**</span></span> | <span data-ttu-id="c6d59-152">Sannprófunartextinn sem á að nota við sjálfsafgreiðslukassa.</span><span class="sxs-lookup"><span data-stu-id="c6d59-152">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="c6d59-153">**Sjálfvirkt val á fulltrúum**</span><span class="sxs-lookup"><span data-stu-id="c6d59-153">**Auto select designees**</span></span> | <span data-ttu-id="c6d59-154">Tilgreinir hvort sjálfkrafa skuli velja á framfæri og styrkþega miðað við hæfi þeirra fyrir áætlunarkosti.</span><span class="sxs-lookup"><span data-stu-id="c6d59-154">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="c6d59-155">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="c6d59-155">Select **Save**.</span></span>
