---
title: Stofna tryggingarvalkosti
description: ''
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
ms.openlocfilehash: 27b43d858a92beac526ac0fc40b544649ef658b0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009356"
---
# <a name="create-coverage-options"></a><span data-ttu-id="38bc6-102">Stofna tryggingarvalkosti</span><span class="sxs-lookup"><span data-stu-id="38bc6-102">Create coverage options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="38bc6-103">Umfjöllunarvalkostir í Microsoft Dynamics 365 Human Resources eru umfjöllunarstig vegna kosninga þátttakenda í bótakerfi eða áætlun, svo sem eingöngu starfsmaður vegna læknisáætlunar, eða 2x laun fyrir líftryggingaráætlun.</span><span class="sxs-lookup"><span data-stu-id="38bc6-103">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program, such as Employee Only for a medical plan, or 2x Salary for a life insurance plan.</span></span> <span data-ttu-id="38bc6-104">Þegar þeir eru skilgreindir eru möguleikar á umfjöllun um ávinning endurnotanlegir og þú getur tengt valkost við eitt eða fleiri áætlanir.</span><span class="sxs-lookup"><span data-stu-id="38bc6-104">Once defined, benefit coverage options are re-usable and you can associate an option with one or more plans.</span></span>

<span data-ttu-id="38bc6-105">Þegar umfjöllunarvalkostirnir eru skilgreindir skaltu hengja umfjöllunarvalkostina við gerð bótaáætlunar.</span><span class="sxs-lookup"><span data-stu-id="38bc6-105">Once the coverage options are defined, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="38bc6-106">Áætlunartegundin er síðan tengd fríðindaáætlun eða áætlun.</span><span class="sxs-lookup"><span data-stu-id="38bc6-106">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="38bc6-107">Umfjöllunarvalkostir sem tengjast áætlunartegundum verða tiltækir öllum áætlunum sem eru búnar til með þeirri áætlunartegund.</span><span class="sxs-lookup"><span data-stu-id="38bc6-107">Coverage options that are associated with a plan type will be available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="38bc6-108">Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Tryggingarvalkostir**.</span><span class="sxs-lookup"><span data-stu-id="38bc6-108">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="38bc6-109">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="38bc6-109">Select **New**.</span></span>

3. <span data-ttu-id="38bc6-110">Tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="38bc6-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="38bc6-111">Svæði</span><span class="sxs-lookup"><span data-stu-id="38bc6-111">Field</span></span> | <span data-ttu-id="38bc6-112">Lýsing</span><span class="sxs-lookup"><span data-stu-id="38bc6-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="38bc6-113">**Tryggingarvalkostur**</span><span class="sxs-lookup"><span data-stu-id="38bc6-113">**Coverage option**</span></span> | <span data-ttu-id="38bc6-114">Einkvæmt heiti tryggingarkosts.</span><span class="sxs-lookup"><span data-stu-id="38bc6-114">A unique coverage option name.</span></span> |
   | <span data-ttu-id="38bc6-115">**Lýsing**</span><span class="sxs-lookup"><span data-stu-id="38bc6-115">**Description**</span></span> | <span data-ttu-id="38bc6-116">Lýsing á tryggingarvalkostinum.</span><span class="sxs-lookup"><span data-stu-id="38bc6-116">A description of the coverage option.</span></span> |
   | <span data-ttu-id="38bc6-117">**Tryggingarkóði**</span><span class="sxs-lookup"><span data-stu-id="38bc6-117">**Coverage code**</span></span> | <span data-ttu-id="38bc6-118">Tryggingarkóðar úthluta lágmarks- og hámarksfjárhæðum fyrir hverja hæfa tegund þeirra sem fjallað er um.</span><span class="sxs-lookup"><span data-stu-id="38bc6-118">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="38bc6-119">Tryggingarkóði gefur til kynna hverjir eru tryggðir eða umfang tryggingr sem leyfilegt er fyrir áætlunartegund.</span><span class="sxs-lookup"><span data-stu-id="38bc6-119">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="38bc6-120">Þú getur tjáð tryggingna sem dollara eða prósentu.</span><span class="sxs-lookup"><span data-stu-id="38bc6-120">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="38bc6-121">Dæmi:</span><span class="sxs-lookup"><span data-stu-id="38bc6-121">For example:</span></span></br></br><span data-ttu-id="38bc6-122">- **Emp+1** - til að vera hæfur verður starfsmaðurinn að vera valinn einn háður (ef fleiri en einn eru valdir, þá fullnægir hann ekki lengur).</span><span class="sxs-lookup"><span data-stu-id="38bc6-122">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="38bc6-123">- **Emp+fjölskylda** - til að vera hæfur verður starfsmaður að velja að minnsta kosti tvo á framfæri.</span><span class="sxs-lookup"><span data-stu-id="38bc6-123">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="38bc6-124">**Hámarksfjöldi**</span><span class="sxs-lookup"><span data-stu-id="38bc6-124">**Maximum number**</span></span> | <span data-ttu-id="38bc6-125">Hámarksfjöldi skjólstæðinga.</span><span class="sxs-lookup"><span data-stu-id="38bc6-125">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="38bc6-126">**Staða**</span><span class="sxs-lookup"><span data-stu-id="38bc6-126">**Status**</span></span> | <span data-ttu-id="38bc6-127">Staða tryggingravalkosts.</span><span class="sxs-lookup"><span data-stu-id="38bc6-127">The status of the coverage option.</span></span> <span data-ttu-id="38bc6-128">Ef staða tryggingarvalkostsins er stillt á Óvirk er ekki hægt að velja tryggingarvalkostinn á áætlunartegundum.</span><span class="sxs-lookup"><span data-stu-id="38bc6-128">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="38bc6-129">**Prósenta**</span><span class="sxs-lookup"><span data-stu-id="38bc6-129">**Percent**</span></span> | <span data-ttu-id="38bc6-130">Prósentuupphæðin.</span><span class="sxs-lookup"><span data-stu-id="38bc6-130">The percent amount.</span></span> <span data-ttu-id="38bc6-131">Þessi reitur er aðeins virkur ef% x Laun var valið í reitnum tryggingarkóða.</span><span class="sxs-lookup"><span data-stu-id="38bc6-131">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="38bc6-132">**Deilir**</span><span class="sxs-lookup"><span data-stu-id="38bc6-132">**Divisor**</span></span> | <span data-ttu-id="38bc6-133">Skiptingin sem á að nota við útreikninginn þegar þú velur tryggingarkóðann% x laun.</span><span class="sxs-lookup"><span data-stu-id="38bc6-133">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="38bc6-134">**Lágmarksprósentuhlutfall**</span><span class="sxs-lookup"><span data-stu-id="38bc6-134">**Percent minimum**</span></span> | <span data-ttu-id="38bc6-135">Lágmarksprósentan þegar þú velur prósentu tryggingarkóða.</span><span class="sxs-lookup"><span data-stu-id="38bc6-135">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="38bc6-136">**Hámarksprósentuhlutfall**</span><span class="sxs-lookup"><span data-stu-id="38bc6-136">**Percent maximum**</span></span> | <span data-ttu-id="38bc6-137">Hámarksprósentan þegar þú velur prósentu tryggingarkóða.</span><span class="sxs-lookup"><span data-stu-id="38bc6-137">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="38bc6-138">Undir **Valmöguleikar persónulegra tengiliða**, hengja viðeigandi valkosti persónulegra tengiliða við hvern tryggingarkost.</span><span class="sxs-lookup"><span data-stu-id="38bc6-138">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="38bc6-139">Undir **Sjálfsafgreiðsla starfsmanns** skal tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="38bc6-139">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="38bc6-140">Svæði</span><span class="sxs-lookup"><span data-stu-id="38bc6-140">Field</span></span> | <span data-ttu-id="38bc6-141">Lýsing</span><span class="sxs-lookup"><span data-stu-id="38bc6-141">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="38bc6-142">**Leyfa upphæð á framlagi starfsmanns**</span><span class="sxs-lookup"><span data-stu-id="38bc6-142">**Allow employee contribution amount**</span></span> | <span data-ttu-id="38bc6-143">Tilgreinir hvort leyfa eigi starfsmönnum að breyta framlagsfjárhæð í sjálfsafgreiðslu bóta þegar þeir velja bætur.</span><span class="sxs-lookup"><span data-stu-id="38bc6-143">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="38bc6-144">Ef þú velur þennan gátreit mun kerfið reikna út breytur bótaáætlunar miðað við framlagsupphæð sem starfsmaður leggur inn í sjálfsafgreiðslu bóta.</span><span class="sxs-lookup"><span data-stu-id="38bc6-144">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="38bc6-145">**Leyfa tryggingarupphæð starfsmanns**</span><span class="sxs-lookup"><span data-stu-id="38bc6-145">**Allow employee coverage amount**</span></span> | <span data-ttu-id="38bc6-146">Tilgreinir hvort leyfa eigi starfsmönnum að breyta tryggingarfjárhæð í sjálfsafgreiðslu bóta þegar þeir velja bætur.</span><span class="sxs-lookup"><span data-stu-id="38bc6-146">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="38bc6-147">Ef þú velur þennan gátreit mun kerfið reikna út breytur bótaáætlunar miðað við tryggingarupphæð sem starfsmaður leggur inn í sjálfsafgreiðslu starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="38bc6-147">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="38bc6-148">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="38bc6-148">Select **Save**.</span></span> 
