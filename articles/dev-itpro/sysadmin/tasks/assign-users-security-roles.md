---
title: Úthluta notendum á öryggishlutverk
description: Til að fá aðgang að Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, þarf að úthluta notendum á öryggishlutverk.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab9f2f5ea07ae1d616c48dffa8810b966f7dbb2f
ms.sourcegitcommit: 33e98f89294086334fe9c0a350abb6a52ef9dacb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/28/2019
ms.locfileid: "1711132"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="b0ce8-103">Úthluta notendum á öryggishlutverk</span><span class="sxs-lookup"><span data-stu-id="b0ce8-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b0ce8-104">Til að fá aðgang að Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, þarf að úthluta notendum á öryggishlutverk.</span><span class="sxs-lookup"><span data-stu-id="b0ce8-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="b0ce8-105">Þessu ferli útskýrt hvernig kerfisstjórum hægt úthluta notendum á hlutverk sjálfkrafa, byggt á viðskiptagögn.</span><span class="sxs-lookup"><span data-stu-id="b0ce8-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="b0ce8-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="b0ce8-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="b0ce8-107">Sjálfkrafa skipa notendum í hlutverkin</span><span class="sxs-lookup"><span data-stu-id="b0ce8-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="b0ce8-108">Farðu í **Skoðunarrúða > Kerfiseiningar > Kerfisstjórnun > Ötyggi > Úthluta notendum á hlutverk**.</span><span class="sxs-lookup"><span data-stu-id="b0ce8-108">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="b0ce8-109">Í þessu dæmi skal velja yfirmaður Bókhalds.</span><span class="sxs-lookup"><span data-stu-id="b0ce8-109">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="b0ce8-110">Veljið hlutverk sem nota á fyrir útvinnsluna á reglunni.</span><span class="sxs-lookup"><span data-stu-id="b0ce8-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="b0ce8-111">Í þessu dæmi skal velja yfirmann bókhalds.</span><span class="sxs-lookup"><span data-stu-id="b0ce8-111">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="b0ce8-112">Smelltu á **Bæta við reglu** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="b0ce8-112">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="b0ce8-113">Á listanum **Velja fyrirspurn** skaltu finna og velja skrána sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="b0ce8-113">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="b0ce8-114">Velja fyrirspurn fyrir þessa reglu.</span><span class="sxs-lookup"><span data-stu-id="b0ce8-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="b0ce8-115">Á listanum **Heiti aðildarreglu** skaltu smella á tengilinn í valinni röð.</span><span class="sxs-lookup"><span data-stu-id="b0ce8-115">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b0ce8-116">Smelltu á **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="b0ce8-116">Click **Edit query**.</span></span> <span data-ttu-id="b0ce8-117">Breyta skal fyrirspurninni eftir því sem þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="b0ce8-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="b0ce8-118">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="b0ce8-118">Click **OK**.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="b0ce8-119">Útiloka notendum frá sjálfvirka hlutverkaúthlutun</span><span class="sxs-lookup"><span data-stu-id="b0ce8-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="b0ce8-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b0ce8-120">Close the page.</span></span>
2. <span data-ttu-id="b0ce8-121">Farðu í **Skoðunarrúða > Kerfiseiningar > Kerfisstjórnun > Ötyggi > Úthluta notendum á hlutverk**.</span><span class="sxs-lookup"><span data-stu-id="b0ce8-121">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="b0ce8-122">Í þessu dæmi skal velja yfirmaður Bókhalds.</span><span class="sxs-lookup"><span data-stu-id="b0ce8-122">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="b0ce8-123">Veljið hlutverk.</span><span class="sxs-lookup"><span data-stu-id="b0ce8-123">Select a role.</span></span> <span data-ttu-id="b0ce8-124">Fyrir þessu dæmi skal velja yfirmann bókhalds.</span><span class="sxs-lookup"><span data-stu-id="b0ce8-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="b0ce8-125">Í valmyndinni **Notendur sem úthlutað er á hlutverk** skaltu velja **Úthluta / útiloka notendur handvirkt**.</span><span class="sxs-lookup"><span data-stu-id="b0ce8-125">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="b0ce8-126">Í listanum **Úthluta notendum til eða útiloka notendur frá hlutverki** skaltu merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="b0ce8-126">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="b0ce8-127">Velja notanda</span><span class="sxs-lookup"><span data-stu-id="b0ce8-127">Select a user.</span></span>  
6. <span data-ttu-id="b0ce8-128">Í **Aðgerðarsvæði** velurðu **Útiloka frá hlutverki**.</span><span class="sxs-lookup"><span data-stu-id="b0ce8-128">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="b0ce8-129">Smelltu á **Útiloka frá hlutverki** til útiloka valda notendur frá hlutverinu.</span><span class="sxs-lookup"><span data-stu-id="b0ce8-129">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="b0ce8-130">Til að fjarlægja útilokanir skal velja notendur sem á að fjarlægja útilokanir á og smella síðan á **Endurstilla stöðu**.</span><span class="sxs-lookup"><span data-stu-id="b0ce8-130">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="b0ce8-131">Þegar fjarlægja útilokun með því að endurstilla stöðu notanda er hlutverki notanda aftur úthlutað sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="b0ce8-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="b0ce8-132">Hins vegar notanda er ekki strax þetta hlutverk úthlutað eða útilokað frá hlutverki þegar endurstilla stöðu.</span><span class="sxs-lookup"><span data-stu-id="b0ce8-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="b0ce8-133">Í stað þess, notandinn annað hvort úthlutaður í hlutverkið eða fjarlægð úr hlutverk í næsta sinn sem keyrðar eru reglum fyrir sjálfvirka hlutverkaúthlutun.</span><span class="sxs-lookup"><span data-stu-id="b0ce8-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
