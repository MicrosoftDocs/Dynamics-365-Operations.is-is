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
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2439d1912b3ca013f4a524f3354923d2a3f76ca
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221282"
---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="7f660-103">Stofna heimildaflokka sölustaða</span><span class="sxs-lookup"><span data-stu-id="7f660-103">Create POS permission groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7f660-104">Þetta efnisatriði útskýrir hvernig á að stofna heimildaflokk sölustaðar.</span><span class="sxs-lookup"><span data-stu-id="7f660-104">This topic explains how to create a POS permission group.</span></span> <span data-ttu-id="7f660-105">Sýnigögn fyrirtækisins til að stofna verkið er USRT.</span><span class="sxs-lookup"><span data-stu-id="7f660-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="7f660-106">Þetta verk er ætluð fyrir hlutverk stjórnanda Commerce aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="7f660-106">This task is intended for the Commerce operations manager role.</span></span>

1. <span data-ttu-id="7f660-107">Í skoðunarrúðunni ferðu í **Einingar > Retail og Commerce > Starfsmenn > Leyfishópar**.</span><span class="sxs-lookup"><span data-stu-id="7f660-107">In the navigation pane, go to **Modules > Retail and Commerce > Employees > Permission groups**.</span></span>
2. <span data-ttu-id="7f660-108">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="7f660-108">Select **New**.</span></span>
3. <span data-ttu-id="7f660-109">Færðu inn gildi í reitnum **Kenni heimildaflokks sölustaðar**.</span><span class="sxs-lookup"><span data-stu-id="7f660-109">In the **POS permission group ID** field, type a value.</span></span>
4. <span data-ttu-id="7f660-110">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7f660-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="7f660-111">Velja skal **Já** í reitnum **Skoða færslur stimpilklukku**.</span><span class="sxs-lookup"><span data-stu-id="7f660-111">Select **Yes** in the **View time clock entries** field.</span></span> <span data-ttu-id="7f660-112">Nú er hægt að virkja eða óvirkja mismunandi heimildir fyrir heimildaflokk Sölustaðar.</span><span class="sxs-lookup"><span data-stu-id="7f660-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="7f660-113">Í sumum heimild hægt að stilla gildi sem verður notað til að meta ef notanda sölustaður getur framkvæmt aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="7f660-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span> <span data-ttu-id="7f660-114">Þessi leiðarvísi fyrir verk virkjar nokkrar heimild sem hugsanlega má veita gjaldkera.</span><span class="sxs-lookup"><span data-stu-id="7f660-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="7f660-115">Velja skal **Já** í reitnum **Leyfa stofnun pöntunar**.</span><span class="sxs-lookup"><span data-stu-id="7f660-115">Select **Yes** in the **Allow create order** field.</span></span>
7. <span data-ttu-id="7f660-116">Velja skal **Já** í reitnum **Leyfa breytingu á pöntun**.</span><span class="sxs-lookup"><span data-stu-id="7f660-116">Select **Yes** in the **Allow edit order** field.</span></span>
8. <span data-ttu-id="7f660-117">Velja skal **Já** í reitnum **Leyfa að pöntun sé sótt**.</span><span class="sxs-lookup"><span data-stu-id="7f660-117">Select **Yes** in the **Allow retrieve order** field.</span></span>
9. <span data-ttu-id="7f660-118">Velja skal **Já** í reitnum **Leyfa breytingu á aðgangsorði**.</span><span class="sxs-lookup"><span data-stu-id="7f660-118">Select **Yes** in the **Allow password change** field.</span></span>
10. <span data-ttu-id="7f660-119">Velja skal **Já** í reitnum **Leyfa blinda lokun**.</span><span class="sxs-lookup"><span data-stu-id="7f660-119">Select **Yes** in the **Allow blind close** field.</span></span>
11. <span data-ttu-id="7f660-120">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="7f660-120">Select **Save**.</span></span> <span data-ttu-id="7f660-121">Eftir að breytingar eru vistaðar þarf að keyra dreifingaráætlun Starfsmanns til að færa breytingar á Commerce-rása.</span><span class="sxs-lookup"><span data-stu-id="7f660-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to commerce channels.</span></span> 
12. <span data-ttu-id="7f660-122">Í skoðunarglugganum ferðu í **Kerfiseiningar > Mannauður > Störf > Störf**.</span><span class="sxs-lookup"><span data-stu-id="7f660-122">In the navigation pane, go to **Modules > Human resources > Jobs > Jobs**.</span></span>
13. <span data-ttu-id="7f660-123">Næsta verður að úthluta heimildaflokk Sölustaðar til Vinnslu.</span><span class="sxs-lookup"><span data-stu-id="7f660-123">Next we will assign the POS permission group to a Job.</span></span> <span data-ttu-id="7f660-124">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="7f660-124">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="7f660-125">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="7f660-125">Select **Edit**.</span></span>
15. <span data-ttu-id="7f660-126">Útvíkkaðu hlutann **Flokkun starfs**.</span><span class="sxs-lookup"><span data-stu-id="7f660-126">Expand the **Job classification** section.</span></span>
16. <span data-ttu-id="7f660-127">Í reitinn Heimildaflokkur sölustaðar skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7f660-127">In the POS permission group field, enter or select a value.</span></span> <span data-ttu-id="7f660-128">Allir starfsmenn í stöðum fyrir þessa vinnslu munu nota stillingar þessa heimildaflokks sölustaðar nema heimildum sölustaðar starfsmanna hafi verið hnekkt á stöðustigi þeirra.</span><span class="sxs-lookup"><span data-stu-id="7f660-128">All Workers in Positions for this Job will use this POS permission group's settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
17. <span data-ttu-id="7f660-129">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="7f660-129">Select **Save**.</span></span> <span data-ttu-id="7f660-130">Eftir að breytingar eru vistaðar þarf að keyra dreifingaráætlun Starfsmanns til að færa breytingar á rása.</span><span class="sxs-lookup"><span data-stu-id="7f660-130">After your changes are saved you need to run the Staff distribution schedule to push the changes to channels.</span></span>  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]