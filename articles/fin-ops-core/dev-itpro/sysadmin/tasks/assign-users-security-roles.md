---
title: Úthluta notendum á öryggishlutverk
description: Til að fá aðgang að forritum Finance and Operations þurfa notendur að fá úthlutað öryggishlutverkum.
author: ChrisGarty
manager: AnnBe
ms.date: 09/16/2019
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
ms.openlocfilehash: a4daecc1acd589cd1656402244e5325382a407e7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180968"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="d5935-103">Úthluta notendum á öryggishlutverk</span><span class="sxs-lookup"><span data-stu-id="d5935-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d5935-104">Til að nota neitt annað en sameiginlega getu verður notendum að vera úthlutað öryggishlutverkum.</span><span class="sxs-lookup"><span data-stu-id="d5935-104">To use anything other than common capabilities, users must be assigned to security roles.</span></span> <span data-ttu-id="d5935-105">Þessu ferli útskýrt hvernig kerfisstjórum geta sjálfvirkt úthlutað notendum á hlutverk, byggt á viðskiptagögnum.</span><span class="sxs-lookup"><span data-stu-id="d5935-105">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="d5935-106">Sjálfkrafa skipa notendum í hlutverkin</span><span class="sxs-lookup"><span data-stu-id="d5935-106">Automatically assign users to roles</span></span>
1. <span data-ttu-id="d5935-107">Farðu í **Skoðunarrúða > Kerfiseiningar > Kerfisstjórnun > Ötyggi > Úthluta notendum á hlutverk**.</span><span class="sxs-lookup"><span data-stu-id="d5935-107">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="d5935-108">Í þessu dæmi skal velja yfirmaður Bókhalds.</span><span class="sxs-lookup"><span data-stu-id="d5935-108">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="d5935-109">Veljið hlutverk sem nota á fyrir útvinnsluna á reglunni.</span><span class="sxs-lookup"><span data-stu-id="d5935-109">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="d5935-110">Í þessu dæmi skal velja yfirmann bókhalds.</span><span class="sxs-lookup"><span data-stu-id="d5935-110">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="d5935-111">Smelltu á **Bæta við reglu** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="d5935-111">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="d5935-112">Á listanum **Velja fyrirspurn** skaltu finna og velja skrána sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="d5935-112">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="d5935-113">Velja fyrirspurn fyrir þessa reglu.</span><span class="sxs-lookup"><span data-stu-id="d5935-113">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="d5935-114">Á listanum **Heiti aðildarreglu** skaltu smella á tengilinn í valinni röð.</span><span class="sxs-lookup"><span data-stu-id="d5935-114">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="d5935-115">Smelltu á **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="d5935-115">Click **Edit query**.</span></span> <span data-ttu-id="d5935-116">Breyta skal fyrirspurninni eftir því sem þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="d5935-116">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="d5935-117">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="d5935-117">Click **OK**.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="d5935-118">Útiloka notendum frá sjálfvirka hlutverkaúthlutun</span><span class="sxs-lookup"><span data-stu-id="d5935-118">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="d5935-119">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d5935-119">Close the page.</span></span>
2. <span data-ttu-id="d5935-120">Farðu í **Skoðunarrúða > Kerfiseiningar > Kerfisstjórnun > Ötyggi > Úthluta notendum á hlutverk**.</span><span class="sxs-lookup"><span data-stu-id="d5935-120">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="d5935-121">Í þessu dæmi skal velja yfirmaður Bókhalds.</span><span class="sxs-lookup"><span data-stu-id="d5935-121">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="d5935-122">Veljið hlutverk.</span><span class="sxs-lookup"><span data-stu-id="d5935-122">Select a role.</span></span> <span data-ttu-id="d5935-123">Fyrir þessu dæmi skal velja yfirmann bókhalds.</span><span class="sxs-lookup"><span data-stu-id="d5935-123">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="d5935-124">Í valmyndinni **Notendur sem úthlutað er á hlutverk** skaltu velja **Úthluta / útiloka notendur handvirkt**.</span><span class="sxs-lookup"><span data-stu-id="d5935-124">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="d5935-125">Í listanum **Úthluta notendum til eða útiloka notendur frá hlutverki** skaltu merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="d5935-125">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="d5935-126">Velja notanda</span><span class="sxs-lookup"><span data-stu-id="d5935-126">Select a user.</span></span>  
6. <span data-ttu-id="d5935-127">Í **Aðgerðarsvæði** velurðu **Útiloka frá hlutverki**.</span><span class="sxs-lookup"><span data-stu-id="d5935-127">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="d5935-128">Smelltu á **Útiloka frá hlutverki** til útiloka valda notendur frá hlutverinu.</span><span class="sxs-lookup"><span data-stu-id="d5935-128">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="d5935-129">Til að fjarlægja útilokanir skal velja notendur sem á að fjarlægja útilokanir á og smella síðan á **Endurstilla stöðu**.</span><span class="sxs-lookup"><span data-stu-id="d5935-129">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="d5935-130">Þegar fjarlægja útilokun með því að endurstilla stöðu notanda er hlutverki notanda aftur úthlutað sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="d5935-130">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="d5935-131">Hins vegar notanda er ekki strax þetta hlutverk úthlutað eða útilokað frá hlutverki þegar endurstilla stöðu.</span><span class="sxs-lookup"><span data-stu-id="d5935-131">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="d5935-132">Í stað þess, notandinn annað hvort úthlutaður í hlutverkið eða fjarlægð úr hlutverk í næsta sinn sem keyrðar eru reglum fyrir sjálfvirka hlutverkaúthlutun.</span><span class="sxs-lookup"><span data-stu-id="d5935-132">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
