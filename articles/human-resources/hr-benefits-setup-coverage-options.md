---
title: Stofna tryggingarvalkosti
description: Umfjöllunarvalkostir í Microsoft Dynamics 365 Human Resources eru umfjöllunarstig fyrir kosningu þátttakenda í bótakerfi eða áætlun.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d9f67a97ec57bade840e1035c6011b94427a77c4
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055581"
---
# <a name="create-coverage-options"></a><span data-ttu-id="caf75-103">Stofna tryggingarvalkosti</span><span class="sxs-lookup"><span data-stu-id="caf75-103">Create coverage options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="caf75-104">Umfjöllunarvalkostir í Microsoft Dynamics 365 Human Resources eru umfjöllunarstig fyrir kosningu þátttakenda í bótakerfi eða áætlun.</span><span class="sxs-lookup"><span data-stu-id="caf75-104">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program.</span></span> <span data-ttu-id="caf75-105">Til dæmis gætu umfjöllunarkostirnir falið í sér **Aðeins starfsmaður** vegna læknisáætlunar, eða **2x laun** vegna líftryggingaráætlunar.</span><span class="sxs-lookup"><span data-stu-id="caf75-105">For example, coverage options could include **Employee Only** for a medical plan, or **2x Salary** for a life insurance plan.</span></span> <span data-ttu-id="caf75-106">Þegar það er skilgreint geturðu notað valkosti um umfjöllun um fríðindi.</span><span class="sxs-lookup"><span data-stu-id="caf75-106">Once defined, you can reuse benefit coverage options.</span></span> <span data-ttu-id="caf75-107">Þú getur tengt valkost við eina eða fleiri áætlanir.</span><span class="sxs-lookup"><span data-stu-id="caf75-107">You can associate an option with one or more plans.</span></span>

<span data-ttu-id="caf75-108">Þegar þú hefur skilgreint umfjöllunarvalkostina skaltu hengja þá við gerð bótaáætlunar.</span><span class="sxs-lookup"><span data-stu-id="caf75-108">After you define coverage options, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="caf75-109">Áætlunartegundin er síðan tengd fríðindaáætlun eða áætlun.</span><span class="sxs-lookup"><span data-stu-id="caf75-109">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="caf75-110">Umfjöllunarvalkostir sem tengjast áætlunartegundum eru tiltækir öllum áætlunum sem eru búnar til með þeirri áætlunartegund.</span><span class="sxs-lookup"><span data-stu-id="caf75-110">Coverage options that are associated with a plan type are available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="caf75-111">Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Tryggingarvalkostir**.</span><span class="sxs-lookup"><span data-stu-id="caf75-111">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="caf75-112">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="caf75-112">Select **New**.</span></span>

3. <span data-ttu-id="caf75-113">Tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="caf75-113">Specify values for the following fields:</span></span>

   | <span data-ttu-id="caf75-114">Svæði</span><span class="sxs-lookup"><span data-stu-id="caf75-114">Field</span></span> | <span data-ttu-id="caf75-115">Lýsing</span><span class="sxs-lookup"><span data-stu-id="caf75-115">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="caf75-116">**Tryggingarvalkostur**</span><span class="sxs-lookup"><span data-stu-id="caf75-116">**Coverage option**</span></span> | <span data-ttu-id="caf75-117">Einkvæmt heiti tryggingarkosts.</span><span class="sxs-lookup"><span data-stu-id="caf75-117">A unique coverage option name.</span></span> |
   | <span data-ttu-id="caf75-118">**Lýsing**</span><span class="sxs-lookup"><span data-stu-id="caf75-118">**Description**</span></span> | <span data-ttu-id="caf75-119">Lýsing á tryggingarvalkostinum.</span><span class="sxs-lookup"><span data-stu-id="caf75-119">A description of the coverage option.</span></span> |
   | <span data-ttu-id="caf75-120">**Tryggingarkóði**</span><span class="sxs-lookup"><span data-stu-id="caf75-120">**Coverage code**</span></span> | <span data-ttu-id="caf75-121">Tryggingarkóðar úthluta lágmarks- og hámarksfjárhæðum fyrir hverja hæfa tegund þeirra sem fjallað er um.</span><span class="sxs-lookup"><span data-stu-id="caf75-121">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="caf75-122">Tryggingarkóði gefur til kynna hverjir eru tryggðir eða umfang tryggingr sem leyfilegt er fyrir áætlunartegund.</span><span class="sxs-lookup"><span data-stu-id="caf75-122">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="caf75-123">Þú getur tjáð tryggingna sem dollara eða prósentu.</span><span class="sxs-lookup"><span data-stu-id="caf75-123">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="caf75-124">Dæmi:</span><span class="sxs-lookup"><span data-stu-id="caf75-124">For example:</span></span></br></br><span data-ttu-id="caf75-125">- **Emp+1** - til að vera hæfur verður starfsmaðurinn að vera valinn einn háður (ef fleiri en einn eru valdir, þá fullnægir hann ekki lengur).</span><span class="sxs-lookup"><span data-stu-id="caf75-125">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="caf75-126">- **Emp+fjölskylda** - til að vera hæfur verður starfsmaður að velja að minnsta kosti tvo á framfæri.</span><span class="sxs-lookup"><span data-stu-id="caf75-126">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="caf75-127">**Hámarksfjöldi**</span><span class="sxs-lookup"><span data-stu-id="caf75-127">**Maximum number**</span></span> | <span data-ttu-id="caf75-128">Hámarksfjöldi skjólstæðinga.</span><span class="sxs-lookup"><span data-stu-id="caf75-128">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="caf75-129">**Staða**</span><span class="sxs-lookup"><span data-stu-id="caf75-129">**Status**</span></span> | <span data-ttu-id="caf75-130">Staða tryggingravalkosts.</span><span class="sxs-lookup"><span data-stu-id="caf75-130">The status of the coverage option.</span></span> <span data-ttu-id="caf75-131">Ef staða tryggingarvalkostsins er stillt á Óvirk er ekki hægt að velja tryggingarvalkostinn á áætlunartegundum.</span><span class="sxs-lookup"><span data-stu-id="caf75-131">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="caf75-132">**Prósenta**</span><span class="sxs-lookup"><span data-stu-id="caf75-132">**Percent**</span></span> | <span data-ttu-id="caf75-133">Prósentuupphæðin.</span><span class="sxs-lookup"><span data-stu-id="caf75-133">The percent amount.</span></span> <span data-ttu-id="caf75-134">Þessi reitur er aðeins virkur ef% x Laun var valið í reitnum tryggingarkóða.</span><span class="sxs-lookup"><span data-stu-id="caf75-134">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="caf75-135">**Deilir**</span><span class="sxs-lookup"><span data-stu-id="caf75-135">**Divisor**</span></span> | <span data-ttu-id="caf75-136">Skiptingin sem á að nota við útreikninginn þegar þú velur tryggingarkóðann% x laun.</span><span class="sxs-lookup"><span data-stu-id="caf75-136">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="caf75-137">**Lágmarksprósentuhlutfall**</span><span class="sxs-lookup"><span data-stu-id="caf75-137">**Percent minimum**</span></span> | <span data-ttu-id="caf75-138">Lágmarksprósentan þegar þú velur prósentu tryggingarkóða.</span><span class="sxs-lookup"><span data-stu-id="caf75-138">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="caf75-139">**Hámarksprósentuhlutfall**</span><span class="sxs-lookup"><span data-stu-id="caf75-139">**Percent maximum**</span></span> | <span data-ttu-id="caf75-140">Hámarksprósentan þegar þú velur prósentu tryggingarkóða.</span><span class="sxs-lookup"><span data-stu-id="caf75-140">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="caf75-141">Undir **Valmöguleikar persónulegra tengiliða**, hengja viðeigandi valkosti persónulegra tengiliða við hvern tryggingarkost.</span><span class="sxs-lookup"><span data-stu-id="caf75-141">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="caf75-142">Undir **Sjálfsafgreiðsla starfsmanns** skal tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="caf75-142">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="caf75-143">Svæði</span><span class="sxs-lookup"><span data-stu-id="caf75-143">Field</span></span> | <span data-ttu-id="caf75-144">Lýsing</span><span class="sxs-lookup"><span data-stu-id="caf75-144">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="caf75-145">**Leyfa upphæð á framlagi starfsmanns**</span><span class="sxs-lookup"><span data-stu-id="caf75-145">**Allow employee contribution amount**</span></span> | <span data-ttu-id="caf75-146">Tilgreinir hvort leyfa eigi starfsmönnum að breyta framlagsfjárhæð í sjálfsafgreiðslu bóta þegar þeir velja bætur.</span><span class="sxs-lookup"><span data-stu-id="caf75-146">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="caf75-147">Ef þú velur þennan gátreit mun kerfið reikna út breytur bótaáætlunar miðað við framlagsupphæð sem starfsmaður leggur inn í sjálfsafgreiðslu bóta.</span><span class="sxs-lookup"><span data-stu-id="caf75-147">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="caf75-148">**Leyfa tryggingarupphæð starfsmanns**</span><span class="sxs-lookup"><span data-stu-id="caf75-148">**Allow employee coverage amount**</span></span> | <span data-ttu-id="caf75-149">Tilgreinir hvort leyfa eigi starfsmönnum að breyta tryggingarfjárhæð í sjálfsafgreiðslu bóta þegar þeir velja bætur.</span><span class="sxs-lookup"><span data-stu-id="caf75-149">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="caf75-150">Ef þú velur þennan gátreit mun kerfið reikna út breytur bótaáætlunar miðað við tryggingarupphæð sem starfsmaður leggur inn í sjálfsafgreiðslu starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="caf75-150">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="caf75-151">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="caf75-151">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]