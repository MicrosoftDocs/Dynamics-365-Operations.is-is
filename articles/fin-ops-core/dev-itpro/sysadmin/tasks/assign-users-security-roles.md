---
title: Úthluta notendum á öryggishlutverk
description: Til að fá aðgang að forritum Finance and Operations, þarf að úthluta notendum á öryggishlutverk.
author: ChrisGarty
manager: AnnBe
ms.date: 11/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0744f45ac91dfb9b5aae35091e3675202c9144f9
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143548"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="05098-103">Úthluta notendum á öryggishlutverk</span><span class="sxs-lookup"><span data-stu-id="05098-103">Assign users to security roles</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="05098-104">Til að nota neitt annað en sameiginlega getu verður notendum að vera úthlutað öryggishlutverkum.</span><span class="sxs-lookup"><span data-stu-id="05098-104">To use anything other than common capabilities, users must be assigned to security roles.</span></span> <span data-ttu-id="05098-105">Þessu ferli útskýrt hvernig kerfisstjórum geta sjálfvirkt úthlutað notendum á hlutverk, byggt á viðskiptagögnum.</span><span class="sxs-lookup"><span data-stu-id="05098-105">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="05098-106">Sjálfkrafa skipa notendum í hlutverkin</span><span class="sxs-lookup"><span data-stu-id="05098-106">Automatically assign users to roles</span></span>
1. <span data-ttu-id="05098-107">Farðu í **Skoðunarrúða > Kerfiseiningar > Kerfisstjórnun > Ötyggi > Úthluta notendum á hlutverk**.</span><span class="sxs-lookup"><span data-stu-id="05098-107">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="05098-108">Í þessu dæmi skal velja yfirmaður Bókhalds.</span><span class="sxs-lookup"><span data-stu-id="05098-108">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="05098-109">Veljið hlutverk sem nota á fyrir útvinnsluna á reglunni.</span><span class="sxs-lookup"><span data-stu-id="05098-109">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="05098-110">Í þessu dæmi skal velja yfirmann bókhalds.</span><span class="sxs-lookup"><span data-stu-id="05098-110">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="05098-111">Smelltu á **Bæta við reglu** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="05098-111">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="05098-112">Á listanum **Velja fyrirspurn** skaltu finna og velja skrána sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="05098-112">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="05098-113">Velja fyrirspurn fyrir þessa reglu.</span><span class="sxs-lookup"><span data-stu-id="05098-113">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="05098-114">Á listanum **Heiti aðildarreglu** skaltu smella á tengilinn í valinni röð.</span><span class="sxs-lookup"><span data-stu-id="05098-114">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="05098-115">Smelltu á **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="05098-115">Click **Edit query**.</span></span> <span data-ttu-id="05098-116">Breyta skal fyrirspurninni eftir því sem þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="05098-116">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="05098-117">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="05098-117">Click **OK**.</span></span>
8. <span data-ttu-id="05098-118">Smelltu á **Keyra sjálfvirka hlutverkaúthlutun**.</span><span class="sxs-lookup"><span data-stu-id="05098-118">Click **Run automatic role assignment**.</span></span>
9. <span data-ttu-id="05098-119">Farðu í **Skoðunarrúðu > Kerfiseiningar > Kerfisstjórnun > Notendur > Notendur** (helst á sérstökum vafraflipa).</span><span class="sxs-lookup"><span data-stu-id="05098-119">Go to **Navigation pane > Modules > System administration > Users > Users** (ideally in a separate browser tab).</span></span>
10. <span data-ttu-id="05098-120">Farðu yfir hlutverkin sem úthlutað var ýmsum notendum til að staðfesta að fyrirspurnin um hlutverkaskiptin hafi verið rétt.</span><span class="sxs-lookup"><span data-stu-id="05098-120">Review the roles assigned to various users to confirm that the role assignment query was correct.</span></span> <span data-ttu-id="05098-121">Stilla og keyra aftur ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="05098-121">Adjust and re-run if needed.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="05098-122">Útiloka notendum frá sjálfvirka hlutverkaúthlutun</span><span class="sxs-lookup"><span data-stu-id="05098-122">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="05098-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="05098-123">Close the page.</span></span>
2. <span data-ttu-id="05098-124">Farðu í **Skoðunarrúða > Kerfiseiningar > Kerfisstjórnun > Ötyggi > Úthluta notendum á hlutverk**.</span><span class="sxs-lookup"><span data-stu-id="05098-124">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="05098-125">Í þessu dæmi skal velja yfirmaður Bókhalds.</span><span class="sxs-lookup"><span data-stu-id="05098-125">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="05098-126">Veljið hlutverk.</span><span class="sxs-lookup"><span data-stu-id="05098-126">Select a role.</span></span> <span data-ttu-id="05098-127">Fyrir þessu dæmi skal velja yfirmann bókhalds.</span><span class="sxs-lookup"><span data-stu-id="05098-127">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="05098-128">Í valmyndinni **Notendur sem úthlutað er á hlutverk** skaltu velja **Úthluta / útiloka notendur handvirkt**.</span><span class="sxs-lookup"><span data-stu-id="05098-128">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="05098-129">Í listanum **Úthluta notendum til eða útiloka notendur frá hlutverki** skaltu merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="05098-129">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="05098-130">Velja notanda</span><span class="sxs-lookup"><span data-stu-id="05098-130">Select a user.</span></span>  
6. <span data-ttu-id="05098-131">Í **Aðgerðarsvæði** velurðu **Útiloka frá hlutverki**.</span><span class="sxs-lookup"><span data-stu-id="05098-131">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="05098-132">Smelltu á **Útiloka frá hlutverki** til útiloka valda notendur frá hlutverinu.</span><span class="sxs-lookup"><span data-stu-id="05098-132">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="05098-133">Til að fjarlægja útilokanir skal velja notendur sem á að fjarlægja útilokanir á og smella síðan á **Endurstilla stöðu**.</span><span class="sxs-lookup"><span data-stu-id="05098-133">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="05098-134">Þegar fjarlægja útilokun með því að endurstilla stöðu notanda er hlutverki notanda aftur úthlutað sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="05098-134">When you remove an exclusion by resetting the user's status, the user's role is again assigned automatically.</span></span> <span data-ttu-id="05098-135">Hins vegar notanda er ekki strax þetta hlutverk úthlutað eða útilokað frá hlutverki þegar endurstilla stöðu.</span><span class="sxs-lookup"><span data-stu-id="05098-135">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="05098-136">Í stað þess, notandinn annað hvort úthlutaður í hlutverkið eða fjarlægð úr hlutverk í næsta sinn sem keyrðar eru reglum fyrir sjálfvirka hlutverkaúthlutun.</span><span class="sxs-lookup"><span data-stu-id="05098-136">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
