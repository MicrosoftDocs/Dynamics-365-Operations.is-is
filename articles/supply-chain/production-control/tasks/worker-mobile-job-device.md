---
title: Skilgreina starfsmann með fartæki
description: Þetta efni útskýrir hvernig á að úthluta rétt hlutverk notandareikningurinn starfsmanns og virkja síðan starfsmanns til að gera skráningu í vinnslusalarstjórnun.
author: ShylaThompson
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8573909476009d5f37a3c0d02ac57b0d518dc267
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148746"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="c40b0-103">Skilgreina starfsmann með fartæki</span><span class="sxs-lookup"><span data-stu-id="c40b0-103">Configure a worker using the mobile job device</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c40b0-104">Þetta efni útskýrir hvernig á að úthluta rétt hlutverk notandareikningurinn starfsmanns og virkja síðan starfsmanns til að gera skráningu í vinnslusalarstjórnun.</span><span class="sxs-lookup"><span data-stu-id="c40b0-104">This topic explains how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a><span data-ttu-id="c40b0-105">Gakktu úr skugga um að starfsmanni sé úthlutað ákveðið hlutverk</span><span class="sxs-lookup"><span data-stu-id="c40b0-105">Verify that a worker is assigned a certain role</span></span>

<span data-ttu-id="c40b0-106">Fyrir þetta dæmi, staðfestið að notandinn „SHANNON“ hefur hlutverk stjórnanda vélarinnar áður en þú stillir starfsmannareikninginn.</span><span class="sxs-lookup"><span data-stu-id="c40b0-106">For this example, verify that user "SHANNON" is assigned the machine operator role before you configure the worker account.</span></span>

1. <span data-ttu-id="c40b0-107">Farðu í **Skoðunarrúðu > Kerfiseiningar > Kerfisstjórnun > Notendur > Notendur**.</span><span class="sxs-lookup"><span data-stu-id="c40b0-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="c40b0-108">Leitaðu að notanda í hraðsíunni.</span><span class="sxs-lookup"><span data-stu-id="c40b0-108">Search for a user in the quick filter.</span></span> <span data-ttu-id="c40b0-109">Í þessu dæmi skal færa inn `shannon`.</span><span class="sxs-lookup"><span data-stu-id="c40b0-109">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="c40b0-110">Veldu tengilinn í **notandanafn** dálkur notendareikningsins sem birtist.</span><span class="sxs-lookup"><span data-stu-id="c40b0-110">Select the link in the **User ID** column of the user account that appears.</span></span>
4. <span data-ttu-id="c40b0-111">Í trénu **Notendahlutverk** velurðu **Hlutverk > Starfsmaður á vél**.</span><span class="sxs-lookup"><span data-stu-id="c40b0-111">In the **User's roles** tree, select **Roles > Machine operator**.</span></span>
5. <span data-ttu-id="c40b0-112">Lokaðu **upplýsingar um notendur** og **notendur** síður til að fara aftur á heimasíðuna.</span><span class="sxs-lookup"><span data-stu-id="c40b0-112">Close the **user details** and **users** pages to return to the home page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="c40b0-113">Skilgreina notandareikning starfkrafts</span><span class="sxs-lookup"><span data-stu-id="c40b0-113">Configure worker account</span></span>
1. <span data-ttu-id="c40b0-114">Fara til **Skoðunargluggi > Kerfiseiningar > Mannauður > Starfskraftar > Starfskraftar**.</span><span class="sxs-lookup"><span data-stu-id="c40b0-114">Go to **Navigation pane > Modules > Human resources > Workers > Workers**.</span></span>
2. <span data-ttu-id="c40b0-115">Leitaðu að notanda í hraðsíunni.</span><span class="sxs-lookup"><span data-stu-id="c40b0-115">Search for a user in the quick filter.</span></span> <span data-ttu-id="c40b0-116">Í þessu dæmi skal færa inn `shannon`.</span><span class="sxs-lookup"><span data-stu-id="c40b0-116">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="c40b0-117">Veldu tengilinn í **Heiti** dálkur notendareikningsins sem birtist.</span><span class="sxs-lookup"><span data-stu-id="c40b0-117">Select the link in the **Name** column of the user account that appears.</span></span>
4. <span data-ttu-id="c40b0-118">Veldu flipann **Tímaskráning**.</span><span class="sxs-lookup"><span data-stu-id="c40b0-118">Select the **Time registration** tab.</span></span>
5. <span data-ttu-id="c40b0-119">Veldu **Virkja á skráningarstöðvum**.</span><span class="sxs-lookup"><span data-stu-id="c40b0-119">Select **Activate on registration terminals**.</span></span>
6. <span data-ttu-id="c40b0-120">Færðu inn eða veldu gildi í eftirfarandi svæði:</span><span class="sxs-lookup"><span data-stu-id="c40b0-120">Enter or select values in the following fields:</span></span>  

    - <span data-ttu-id="c40b0-121">**Reikniflokkur**</span><span class="sxs-lookup"><span data-stu-id="c40b0-121">**Calculation group**</span></span>  
    - <span data-ttu-id="c40b0-122">**Sjálfgefinn útreikningaflokkur**</span><span class="sxs-lookup"><span data-stu-id="c40b0-122">**Default calculation group**</span></span>  
    - <span data-ttu-id="c40b0-123">**Samþykkisflokkur**</span><span class="sxs-lookup"><span data-stu-id="c40b0-123">**Approval group**</span></span>  
    - <span data-ttu-id="c40b0-124">**Stöðluð forstilling**</span><span class="sxs-lookup"><span data-stu-id="c40b0-124">**Standard profile**</span></span>  
    - <span data-ttu-id="c40b0-125">**Forstillingarflokkur**</span><span class="sxs-lookup"><span data-stu-id="c40b0-125">**Profile group**</span></span>  

7. <span data-ttu-id="c40b0-126">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="c40b0-126">Select **OK**.</span></span>
8. <span data-ttu-id="c40b0-127">Veldu **Breyta** til að færa inn númer korti fyrir nýja starfsmaður sem sinnir tímaskráningu.</span><span class="sxs-lookup"><span data-stu-id="c40b0-127">Select **Edit** to enter a badge number for the new time registration worker.</span></span> <span data-ttu-id="c40b0-128">Færðu inn gildi í reitnum **Kortkenni**.</span><span class="sxs-lookup"><span data-stu-id="c40b0-128">Enter a value in the **Badge ID** field.</span></span>
9. <span data-ttu-id="c40b0-129">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="c40b0-129">Select **Save**.</span></span>
10. <span data-ttu-id="c40b0-130">Lokaðu **Upplýsingar um starfsmann** og **Verkamenn**.</span><span class="sxs-lookup"><span data-stu-id="c40b0-130">Close the **Worker details** and **Workers** pages.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="c40b0-131">Úthluta starfskrafti á tækjaflokk.</span><span class="sxs-lookup"><span data-stu-id="c40b0-131">Assign worker to device group</span></span>
1. <span data-ttu-id="c40b0-132">Fara í **Framleiðslustýringar > Uppsetning > Framkvæmd framleiðslu > Skilgreina verkspjald fyrir tæki**.</span><span class="sxs-lookup"><span data-stu-id="c40b0-132">Go to **Production control > Setup > Manufacturing execution > Configure job card for devices**.</span></span>
2. <span data-ttu-id="c40b0-133">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="c40b0-133">Select **Add**.</span></span>
3. <span data-ttu-id="c40b0-134">Á listanum, skal velja viðeigandi strafskraft.</span><span class="sxs-lookup"><span data-stu-id="c40b0-134">In the list, select the desired worker.</span></span> <span data-ttu-id="c40b0-135">Í þessu dæmi, velja **SHANNON**.</span><span class="sxs-lookup"><span data-stu-id="c40b0-135">For this example, select **SHANNON**.</span></span>
4. <span data-ttu-id="c40b0-136">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="c40b0-136">Select **OK**.</span></span>
5. <span data-ttu-id="c40b0-137">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="c40b0-137">Select **Edit**.</span></span>
6. <span data-ttu-id="c40b0-138">Í svæðið **eining Framleiðslu** er hægt að setja síu sjálfgefið fyrir starfsmann.</span><span class="sxs-lookup"><span data-stu-id="c40b0-138">In the **Production unit** field, you can set the default filter for the worker.</span></span> <span data-ttu-id="c40b0-139">Þetta mun tryggja að eingöngu vinnslur fyrir valda framleiðslueiningu eru birtar þegar starfsmaður skráir sig inn á tækinu.</span><span class="sxs-lookup"><span data-stu-id="c40b0-139">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span> <span data-ttu-id="c40b0-140">Færa inn æskilegt gildi.</span><span class="sxs-lookup"><span data-stu-id="c40b0-140">Enter the desired value.</span></span>
7. <span data-ttu-id="c40b0-141">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c40b0-141">Close the page.</span></span>

