---
title: Stofna heimildaflokka sölustaða
description: Þetta efnisatriði útskýrir hvernig á að stofna heimildaflokk sölustaðar.
author: scott-tucker
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e6f9f8f970f336a0cce6bcac78e32a1b7fe0a252
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022907"
---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="95e26-103">Stofna heimildaflokka sölustaða</span><span class="sxs-lookup"><span data-stu-id="95e26-103">Create POS permission groups</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="95e26-104">Þetta efnisatriði útskýrir hvernig á að stofna heimildaflokk sölustaðar.</span><span class="sxs-lookup"><span data-stu-id="95e26-104">This topic explains how to create a POS permission group.</span></span> <span data-ttu-id="95e26-105">Sýnigögn fyrirtækisins til að stofna verkið er USRT.</span><span class="sxs-lookup"><span data-stu-id="95e26-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="95e26-106">Þetta verk er ætluð fyrir hlutverk stjórnanda Commerce aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="95e26-106">This task is intended for the Commerce operations manager role.</span></span>

1. <span data-ttu-id="95e26-107">Í skoðunarrúðunni ferðu í **Einingar > Retail og Commerce > Starfsmenn > Leyfishópar**.</span><span class="sxs-lookup"><span data-stu-id="95e26-107">In the navigation pane, go to **Modules > Retail and Commerce > Employees > Permission groups**.</span></span>
2. <span data-ttu-id="95e26-108">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="95e26-108">Select **New**.</span></span>
3. <span data-ttu-id="95e26-109">Færðu inn gildi í reitnum **Kenni heimildaflokks sölustaðar**.</span><span class="sxs-lookup"><span data-stu-id="95e26-109">In the **POS permission group ID** field, type a value.</span></span>
4. <span data-ttu-id="95e26-110">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="95e26-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="95e26-111">Velja skal **Já** í reitnum **Skoða færslur stimpilklukku**.</span><span class="sxs-lookup"><span data-stu-id="95e26-111">Select **Yes** in the **View time clock entries** field.</span></span> <span data-ttu-id="95e26-112">Nú er hægt að virkja eða óvirkja mismunandi heimildir fyrir heimildaflokk Sölustaðar.</span><span class="sxs-lookup"><span data-stu-id="95e26-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="95e26-113">Í sumum heimild hægt að stilla gildi sem verður notað til að meta ef notanda sölustaður getur framkvæmt aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="95e26-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span> <span data-ttu-id="95e26-114">Þessi leiðarvísi fyrir verk virkjar nokkrar heimild sem hugsanlega má veita gjaldkera.</span><span class="sxs-lookup"><span data-stu-id="95e26-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="95e26-115">Velja skal **Já** í reitnum **Leyfa stofnun pöntunar**.</span><span class="sxs-lookup"><span data-stu-id="95e26-115">Select **Yes** in the **Allow create order** field.</span></span>
7. <span data-ttu-id="95e26-116">Velja skal **Já** í reitnum **Leyfa breytingu á pöntun**.</span><span class="sxs-lookup"><span data-stu-id="95e26-116">Select **Yes** in the **Allow edit order** field.</span></span>
8. <span data-ttu-id="95e26-117">Velja skal **Já** í reitnum **Leyfa að pöntun sé sótt**.</span><span class="sxs-lookup"><span data-stu-id="95e26-117">Select **Yes** in the **Allow retrieve order** field.</span></span>
9. <span data-ttu-id="95e26-118">Velja skal **Já** í reitnum **Leyfa breytingu á aðgangsorði**.</span><span class="sxs-lookup"><span data-stu-id="95e26-118">Select **Yes** in the **Allow password change** field.</span></span>
10. <span data-ttu-id="95e26-119">Velja skal **Já** í reitnum **Leyfa blinda lokun**.</span><span class="sxs-lookup"><span data-stu-id="95e26-119">Select **Yes** in the **Allow blind close** field.</span></span>
11. <span data-ttu-id="95e26-120">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="95e26-120">Select **Save**.</span></span> <span data-ttu-id="95e26-121">Eftir að breytingar eru vistaðar þarf að keyra dreifingaráætlun Starfsmanns til að færa breytingar á Commerce-rása.</span><span class="sxs-lookup"><span data-stu-id="95e26-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to commerce channels.</span></span> 
12. <span data-ttu-id="95e26-122">Í skoðunarglugganum ferðu í **Kerfiseiningar > Mannauður > Störf > Störf**.</span><span class="sxs-lookup"><span data-stu-id="95e26-122">In the navigation pane, go to **Modules > Human resources > Jobs > Jobs**.</span></span>
13. <span data-ttu-id="95e26-123">Næsta verður að úthluta heimildaflokk Sölustaðar til Vinnslu.</span><span class="sxs-lookup"><span data-stu-id="95e26-123">Next we will assign the POS permission group to a Job.</span></span> <span data-ttu-id="95e26-124">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="95e26-124">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="95e26-125">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="95e26-125">Select **Edit**.</span></span>
15. <span data-ttu-id="95e26-126">Útvíkkaðu hlutann **Flokkun starfs**.</span><span class="sxs-lookup"><span data-stu-id="95e26-126">Expand the **Job classification** section.</span></span>
16. <span data-ttu-id="95e26-127">Í reitinn Heimildaflokkur sölustaðar skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="95e26-127">In the POS permission group field, enter or select a value.</span></span> <span data-ttu-id="95e26-128">Allir starfsmenn í stöðum fyrir þessa vinnslu Munu nota stillingar þessa heimildaflokk Sölustaðar nema heimildir Sölustaðar starfsmanna hafi verið hnekkt á stigi Stöðu þeirra.</span><span class="sxs-lookup"><span data-stu-id="95e26-128">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
17. <span data-ttu-id="95e26-129">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="95e26-129">Select **Save**.</span></span> <span data-ttu-id="95e26-130">Eftir að breytingar eru vistaðar þarf að keyra dreifingaráætlun Starfsmanns til að færa breytingar á rása.</span><span class="sxs-lookup"><span data-stu-id="95e26-130">After your changes are saved you need to run the Staff distribution schedule to push the changes to channels.</span></span>  

