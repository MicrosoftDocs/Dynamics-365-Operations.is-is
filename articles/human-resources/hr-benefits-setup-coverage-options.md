---
title: Stofna tryggingarvalkosti
description: Umfjöllunarvalkostir í Microsoft Dynamics 365 Human Resources eru umfjöllunarstig vegna kosninga þátttakenda í bótakerfi eða áætlun, svo sem eingöngu starfsmaður vegna læknisáætlunar, eða 2x laun fyrir líftryggingaráætlun.
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
ms.openlocfilehash: 0af2b6ae0853b4c7f64c4d4f04299c87089d622b
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092707"
---
# <a name="create-coverage-options"></a><span data-ttu-id="f26fc-103">Stofna tryggingarvalkosti</span><span class="sxs-lookup"><span data-stu-id="f26fc-103">Create coverage options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="f26fc-104">Umfjöllunarvalkostir í Microsoft Dynamics 365 Human Resources eru umfjöllunarstig vegna kosninga þátttakenda í bótakerfi eða áætlun, svo sem eingöngu starfsmaður vegna læknisáætlunar, eða 2x laun fyrir líftryggingaráætlun.</span><span class="sxs-lookup"><span data-stu-id="f26fc-104">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program, such as Employee Only for a medical plan, or 2x Salary for a life insurance plan.</span></span> <span data-ttu-id="f26fc-105">Þegar þeir eru skilgreindir eru möguleikar á umfjöllun um ávinning endurnotanlegir og þú getur tengt valkost við eitt eða fleiri áætlanir.</span><span class="sxs-lookup"><span data-stu-id="f26fc-105">Once defined, benefit coverage options are re-usable and you can associate an option with one or more plans.</span></span>

<span data-ttu-id="f26fc-106">Þegar umfjöllunarvalkostirnir eru skilgreindir skaltu hengja umfjöllunarvalkostina við gerð bótaáætlunar.</span><span class="sxs-lookup"><span data-stu-id="f26fc-106">Once the coverage options are defined, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="f26fc-107">Áætlunartegundin er síðan tengd fríðindaáætlun eða áætlun.</span><span class="sxs-lookup"><span data-stu-id="f26fc-107">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="f26fc-108">Umfjöllunarvalkostir sem tengjast áætlunartegundum verða tiltækir öllum áætlunum sem eru búnar til með þeirri áætlunartegund.</span><span class="sxs-lookup"><span data-stu-id="f26fc-108">Coverage options that are associated with a plan type will be available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="f26fc-109">Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Tryggingarvalkostir**.</span><span class="sxs-lookup"><span data-stu-id="f26fc-109">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="f26fc-110">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="f26fc-110">Select **New**.</span></span>

3. <span data-ttu-id="f26fc-111">Tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="f26fc-111">Specify values for the following fields:</span></span>

   | <span data-ttu-id="f26fc-112">Svæði</span><span class="sxs-lookup"><span data-stu-id="f26fc-112">Field</span></span> | <span data-ttu-id="f26fc-113">Lýsing</span><span class="sxs-lookup"><span data-stu-id="f26fc-113">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f26fc-114">**Tryggingarvalkostur**</span><span class="sxs-lookup"><span data-stu-id="f26fc-114">**Coverage option**</span></span> | <span data-ttu-id="f26fc-115">Einkvæmt heiti tryggingarkosts.</span><span class="sxs-lookup"><span data-stu-id="f26fc-115">A unique coverage option name.</span></span> |
   | <span data-ttu-id="f26fc-116">**Lýsing**</span><span class="sxs-lookup"><span data-stu-id="f26fc-116">**Description**</span></span> | <span data-ttu-id="f26fc-117">Lýsing á tryggingarvalkostinum.</span><span class="sxs-lookup"><span data-stu-id="f26fc-117">A description of the coverage option.</span></span> |
   | <span data-ttu-id="f26fc-118">**Tryggingarkóði**</span><span class="sxs-lookup"><span data-stu-id="f26fc-118">**Coverage code**</span></span> | <span data-ttu-id="f26fc-119">Tryggingarkóðar úthluta lágmarks- og hámarksfjárhæðum fyrir hverja hæfa tegund þeirra sem fjallað er um.</span><span class="sxs-lookup"><span data-stu-id="f26fc-119">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="f26fc-120">Tryggingarkóði gefur til kynna hverjir eru tryggðir eða umfang tryggingr sem leyfilegt er fyrir áætlunartegund.</span><span class="sxs-lookup"><span data-stu-id="f26fc-120">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="f26fc-121">Þú getur tjáð tryggingna sem dollara eða prósentu.</span><span class="sxs-lookup"><span data-stu-id="f26fc-121">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="f26fc-122">Dæmi:</span><span class="sxs-lookup"><span data-stu-id="f26fc-122">For example:</span></span></br></br><span data-ttu-id="f26fc-123">- **Emp+1** - til að vera hæfur verður starfsmaðurinn að vera valinn einn háður (ef fleiri en einn eru valdir, þá fullnægir hann ekki lengur).</span><span class="sxs-lookup"><span data-stu-id="f26fc-123">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="f26fc-124">- **Emp+fjölskylda** - til að vera hæfur verður starfsmaður að velja að minnsta kosti tvo á framfæri.</span><span class="sxs-lookup"><span data-stu-id="f26fc-124">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="f26fc-125">**Hámarksfjöldi**</span><span class="sxs-lookup"><span data-stu-id="f26fc-125">**Maximum number**</span></span> | <span data-ttu-id="f26fc-126">Hámarksfjöldi skjólstæðinga.</span><span class="sxs-lookup"><span data-stu-id="f26fc-126">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="f26fc-127">**Staða**</span><span class="sxs-lookup"><span data-stu-id="f26fc-127">**Status**</span></span> | <span data-ttu-id="f26fc-128">Staða tryggingravalkosts.</span><span class="sxs-lookup"><span data-stu-id="f26fc-128">The status of the coverage option.</span></span> <span data-ttu-id="f26fc-129">Ef staða tryggingarvalkostsins er stillt á Óvirk er ekki hægt að velja tryggingarvalkostinn á áætlunartegundum.</span><span class="sxs-lookup"><span data-stu-id="f26fc-129">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="f26fc-130">**Prósenta**</span><span class="sxs-lookup"><span data-stu-id="f26fc-130">**Percent**</span></span> | <span data-ttu-id="f26fc-131">Prósentuupphæðin.</span><span class="sxs-lookup"><span data-stu-id="f26fc-131">The percent amount.</span></span> <span data-ttu-id="f26fc-132">Þessi reitur er aðeins virkur ef% x Laun var valið í reitnum tryggingarkóða.</span><span class="sxs-lookup"><span data-stu-id="f26fc-132">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="f26fc-133">**Deilir**</span><span class="sxs-lookup"><span data-stu-id="f26fc-133">**Divisor**</span></span> | <span data-ttu-id="f26fc-134">Skiptingin sem á að nota við útreikninginn þegar þú velur tryggingarkóðann% x laun.</span><span class="sxs-lookup"><span data-stu-id="f26fc-134">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="f26fc-135">**Lágmarksprósentuhlutfall**</span><span class="sxs-lookup"><span data-stu-id="f26fc-135">**Percent minimum**</span></span> | <span data-ttu-id="f26fc-136">Lágmarksprósentan þegar þú velur prósentu tryggingarkóða.</span><span class="sxs-lookup"><span data-stu-id="f26fc-136">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="f26fc-137">**Hámarksprósentuhlutfall**</span><span class="sxs-lookup"><span data-stu-id="f26fc-137">**Percent maximum**</span></span> | <span data-ttu-id="f26fc-138">Hámarksprósentan þegar þú velur prósentu tryggingarkóða.</span><span class="sxs-lookup"><span data-stu-id="f26fc-138">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="f26fc-139">Undir **Valmöguleikar persónulegra tengiliða**, hengja viðeigandi valkosti persónulegra tengiliða við hvern tryggingarkost.</span><span class="sxs-lookup"><span data-stu-id="f26fc-139">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="f26fc-140">Undir **Sjálfsafgreiðsla starfsmanns** skal tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="f26fc-140">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="f26fc-141">Svæði</span><span class="sxs-lookup"><span data-stu-id="f26fc-141">Field</span></span> | <span data-ttu-id="f26fc-142">Lýsing</span><span class="sxs-lookup"><span data-stu-id="f26fc-142">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f26fc-143">**Leyfa upphæð á framlagi starfsmanns**</span><span class="sxs-lookup"><span data-stu-id="f26fc-143">**Allow employee contribution amount**</span></span> | <span data-ttu-id="f26fc-144">Tilgreinir hvort leyfa eigi starfsmönnum að breyta framlagsfjárhæð í sjálfsafgreiðslu bóta þegar þeir velja bætur.</span><span class="sxs-lookup"><span data-stu-id="f26fc-144">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="f26fc-145">Ef þú velur þennan gátreit mun kerfið reikna út breytur bótaáætlunar miðað við framlagsupphæð sem starfsmaður leggur inn í sjálfsafgreiðslu bóta.</span><span class="sxs-lookup"><span data-stu-id="f26fc-145">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="f26fc-146">**Leyfa tryggingarupphæð starfsmanns**</span><span class="sxs-lookup"><span data-stu-id="f26fc-146">**Allow employee coverage amount**</span></span> | <span data-ttu-id="f26fc-147">Tilgreinir hvort leyfa eigi starfsmönnum að breyta tryggingarfjárhæð í sjálfsafgreiðslu bóta þegar þeir velja bætur.</span><span class="sxs-lookup"><span data-stu-id="f26fc-147">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="f26fc-148">Ef þú velur þennan gátreit mun kerfið reikna út breytur bótaáætlunar miðað við tryggingarupphæð sem starfsmaður leggur inn í sjálfsafgreiðslu starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="f26fc-148">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="f26fc-149">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="f26fc-149">Select **Save**.</span></span> 
