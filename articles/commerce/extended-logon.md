---
title: Setja upp aukna innskráningarvirkni fyrir MPOS og sölukerfi í skýinu
description: Þetta efnisatriði nær yfir valmöguleika til að setja upp aukna innskráningu starfsmanns fyrir sölukerfi í skýinu og Retail Modern POS (MPOS).
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 79878e2ffbf219f77f378997c277ced8bb41598c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022950"
---
# <a name="set-up-extended-logon-functionality-for-mpos-and-cloud-pos"></a><span data-ttu-id="359d6-103">Setja upp aukna innskráningarvirkni fyrir MPOS og sölukerfi í skýinu</span><span class="sxs-lookup"><span data-stu-id="359d6-103">Set up extended logon functionality for MPOS and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="359d6-104">Þetta efnisatriði nær yfir valmöguleika til að setja upp aukna innskráningu starfsmanns fyrir sölukerfi í skýinu og Retail Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="359d6-104">This topic covers your options for setting up extended logon for Cloud POS and Retail Modern POS (MPOS).</span></span>

## <a name="setting-up-extended-logon"></a><span data-ttu-id="359d6-105">Setja upp aukna innskráningu starfsmanns</span><span class="sxs-lookup"><span data-stu-id="359d6-105">Setting up extended logon</span></span>

<span data-ttu-id="359d6-106">Hægt er að finna uppsetningu fyrir snimát strikamerkja á **Retail og Commerce** &gt; **Rásaruppsetningu** &gt; **Uppsetning sölustaðar** &gt; **Forstilling sölustaðar** &gt; **Virknireglur**.</span><span class="sxs-lookup"><span data-stu-id="359d6-106">You can find the setup for bar code masks at **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Functionality profiles**.</span></span> <span data-ttu-id="359d6-107">Flýtiflipinn **Aðgerðir** inniheldur eftirfarandi valkosti sem eru tengdir lengdri innskráningu starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="359d6-107">The **Functions** FastTab includes the following options that are related to extended logon.</span></span>

### <a name="staff-bar-code-logon"></a><span data-ttu-id="359d6-108">Strikamerkisinnskráning starfsmanns</span><span class="sxs-lookup"><span data-stu-id="359d6-108">Staff bar code logon</span></span>

<span data-ttu-id="359d6-109">Þegar valkosturinn **Strikamerkisinnskráning starfsmanns** er virkjaður geta starfsmenn sem hafa aukna innskráningu úthlutað á sölustað sinn (POS) skráð sig inn með því að nota strikamerki.</span><span class="sxs-lookup"><span data-stu-id="359d6-109">When the **Staff bar code logon** option is enabled, workers who have an extended logon assigned to their point of sale (POS) credentials can log on by using a bar code.</span></span>

### <a name="staff-bar-code-logon-requires-password"></a><span data-ttu-id="359d6-110">Nota þarf aðgangsorð með strikamerkisskráningu starfsmanns</span><span class="sxs-lookup"><span data-stu-id="359d6-110">Staff bar code logon requires password</span></span>

<span data-ttu-id="359d6-111">Þegar valkosturinn **Strikamerkisinnskráning starfsmanns krefst aðgangsorðs** er virkjaður velur strikamerkisinnskráning starfsmanns aðeins þann starfsmann sem er úthlutað á þá auknu innskráningu sem er sýnd.</span><span class="sxs-lookup"><span data-stu-id="359d6-111">When the **Staff bar code logon requires password** option is enabled, the staff bar code logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="359d6-112">Starfsmenn þurfa samt að færa inn aðgangsorð sitt þegar þessi valkostur er gerður virkur.</span><span class="sxs-lookup"><span data-stu-id="359d6-112">Workers must still enter their password when this option is enabled.</span></span>

### <a name="staff-card-logon"></a><span data-ttu-id="359d6-113">Kortainnskráning starfsmanns</span><span class="sxs-lookup"><span data-stu-id="359d6-113">Staff card logon</span></span>

<span data-ttu-id="359d6-114">Þegar valkosturinn **Kortainnskráning starfsmanns** er virkjaður geta starfsmenn sem hafa aukna innskráningu úthlutað á sölustað sinn (POS) skráð sig inn með því að nota segulrönd.</span><span class="sxs-lookup"><span data-stu-id="359d6-114">When the **Staff card logon** option is enabled, workers who have an extended logon assigned to their POS credentials can log on by using a magnetic stripe.</span></span>

### <a name="staff-card-logon-requires-password"></a><span data-ttu-id="359d6-115">Nota þarf aðgangsorð með kortainnskráningu starfsmanns</span><span class="sxs-lookup"><span data-stu-id="359d6-115">Staff card logon requires password</span></span>

<span data-ttu-id="359d6-116">Þegar valkosturinn **Kortainnskráning starfsmanns krefst aðgangsorðs** er virkjaður velur kortainnskráning starfsmanns aðeins þann starfsmann sem er úthlutað á þá auknu innskráningu sem er sýnd.</span><span class="sxs-lookup"><span data-stu-id="359d6-116">When the **Staff card logon requires password** option is enabled, the staff card logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="359d6-117">Starfsmenn þurfa samt að færa inn aðgangsorð sitt þegar þessi valkostur er gerður virkur.</span><span class="sxs-lookup"><span data-stu-id="359d6-117">Workers must still enter their password when this option is enabled.</span></span>

## <a name="assigning-an-extended-logon"></a><span data-ttu-id="359d6-118">Úthlutun aukinnar innskráningu</span><span class="sxs-lookup"><span data-stu-id="359d6-118">Assigning an extended logon</span></span>

<span data-ttu-id="359d6-119">Að sjálfgefnu geta aðeins stjórnendur úthlutað aukinni innskráningu til starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="359d6-119">By default, only managers can assign extended logon to workers.</span></span> <span data-ttu-id="359d6-120">Til að úthluta aukinni innskráningu á starfsmann er farið á **Aukin innskráning** á Sölustað.</span><span class="sxs-lookup"><span data-stu-id="359d6-120">To assign extended logon, go to **Extended log on** in POS.</span></span> <span data-ttu-id="359d6-121">Síðan skal leita starfsmann með því að færa inn Kenni stjórnanda hans eða hennar í leitarreitnum.</span><span class="sxs-lookup"><span data-stu-id="359d6-121">Then search for a worker by entering his or her operator ID in the search field.</span></span> <span data-ttu-id="359d6-122">Veljið notanda og smellið á **Úthluta**.</span><span class="sxs-lookup"><span data-stu-id="359d6-122">Select the worker, and then click **Assign**.</span></span> <span data-ttu-id="359d6-123">Á næstu síðu skal lesa eða skanna aukna innskráningu til að úthluta á starfsmanninn.</span><span class="sxs-lookup"><span data-stu-id="359d6-123">On the next page, swipe or scan the extended logon to assign to the worker.</span></span> <span data-ttu-id="359d6-124">Ef kortalestur eða skönnun er var lesin verður hnappuinn **Í lagi** tiltækur.</span><span class="sxs-lookup"><span data-stu-id="359d6-124">If the swipe or scan is successfully read, the **OK** button becomes available.</span></span> <span data-ttu-id="359d6-125">Smellið á **Í lagi** til að vista aukna innskráningu fyrir þann starfsmann.</span><span class="sxs-lookup"><span data-stu-id="359d6-125">Click **OK** to save the extended logon for that worker.</span></span>

## <a name="deleting-an-extended-logon"></a><span data-ttu-id="359d6-126">Eyðing aukinnar innskráningar</span><span class="sxs-lookup"><span data-stu-id="359d6-126">Deleting an extended logon</span></span>

<span data-ttu-id="359d6-127">Til að eyða aukinni innskráningu sem er úthlutað á starfsmann, skal leita að starfsmanni með því að nota aðgerðina **Aukin innskráning**.</span><span class="sxs-lookup"><span data-stu-id="359d6-127">To delete the extended logon that is assigned to a worker, search for the worker by using the **Extended log on** operation.</span></span> <span data-ttu-id="359d6-128">Veljið notanda og smellið á **Hætta við úthlutun**.</span><span class="sxs-lookup"><span data-stu-id="359d6-128">Select the worker, and then click **Unassign**.</span></span> <span data-ttu-id="359d6-129">Öll útvíkkuð skilríki sem eru tengd við starfsmanninn eru fjarlægð.</span><span class="sxs-lookup"><span data-stu-id="359d6-129">All extended logon credentials that are associated with that worker are removed.</span></span>

## <a name="extending-extended-logon"></a><span data-ttu-id="359d6-130">Útvíkkun aukinnar innskráningar</span><span class="sxs-lookup"><span data-stu-id="359d6-130">Extending extended logon</span></span>

<span data-ttu-id="359d6-131">Hægt er að auka innskráningarþjónustu til að styðja til viðbótar aukin innskráningartæki, eins og lófaskanna.</span><span class="sxs-lookup"><span data-stu-id="359d6-131">The logon service can be extended to support additional extended logon devices, such as palm scanners.</span></span> <span data-ttu-id="359d6-132">Nánari upplýsingar fást í fylgigögnum um POS.</span><span class="sxs-lookup"><span data-stu-id="359d6-132">For more information, see the POS extensibility documentation.</span></span>

## <a name="using-extended-logon"></a><span data-ttu-id="359d6-133">Notkun aukinnar innskráningar</span><span class="sxs-lookup"><span data-stu-id="359d6-133">Using extended logon</span></span>

<span data-ttu-id="359d6-134">Þegar aukin innskráning er skilgreind og starfsmanni hefur verið úthlutað á strikamerki eða segulrönd, þarf starfsmaðurinn aðeins að renna eða skanna kortið sitt meðan síðan Innskráning á sölustað birtist.</span><span class="sxs-lookup"><span data-stu-id="359d6-134">When extended logon is configured, and a worker has been assigned a bar code or magnetic stripe, the worker just has to swipe or scan his or her card while the POS logon page is displayed.</span></span> <span data-ttu-id="359d6-135">Ef aðgangsorðs er einnig krafist áður en innskráning getur haldið áfram er starfsmaður beðinn um að færa inn aðgangsorð sitt.</span><span class="sxs-lookup"><span data-stu-id="359d6-135">If a password is also required before logon can proceed, the worker is prompted to enter his or her password.</span></span>