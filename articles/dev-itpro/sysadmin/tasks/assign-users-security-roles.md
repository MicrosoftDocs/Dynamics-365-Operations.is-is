---
title: Úthluta notendum á öryggishlutverk
description: Til að fá aðgang að Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, þarf að úthluta notendum á öryggishlutverk.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 55cb085bb5170aa4894a2240a12f6ca451b922fb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "349953"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="3cce7-103">Úthluta notendum á öryggishlutverk</span><span class="sxs-lookup"><span data-stu-id="3cce7-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3cce7-104">Til að fá aðgang að Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, þarf að úthluta notendum á öryggishlutverk.</span><span class="sxs-lookup"><span data-stu-id="3cce7-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="3cce7-105">Þessu ferli útskýrt hvernig kerfisstjórum hægt úthluta notendum á hlutverk sjálfkrafa, byggt á viðskiptagögn.</span><span class="sxs-lookup"><span data-stu-id="3cce7-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="3cce7-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="3cce7-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="3cce7-107">Sjálfkrafa skipa notendum í hlutverkin</span><span class="sxs-lookup"><span data-stu-id="3cce7-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="3cce7-108">Fara í Kerfisstjórn > Öryggi > Úthluta hlutverkum á notendur.</span><span class="sxs-lookup"><span data-stu-id="3cce7-108">Go to System administration > Security > Assign users to roles.</span></span>
2. <span data-ttu-id="3cce7-109">Í þessu dæmi skal velja yfirmaður Bókhalds.</span><span class="sxs-lookup"><span data-stu-id="3cce7-109">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="3cce7-110">Veljið hlutverk sem nota á fyrir útvinnsluna á reglunni.</span><span class="sxs-lookup"><span data-stu-id="3cce7-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="3cce7-111">Í þessu dæmi skal velja yfirmann bókhalds.</span><span class="sxs-lookup"><span data-stu-id="3cce7-111">In this example, select Accounting supervisor.</span></span>  
3. <span data-ttu-id="3cce7-112">Smelltu á bæta við reglu til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="3cce7-112">Click Add rule to open the drop dialog.</span></span>
4. <span data-ttu-id="3cce7-113">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="3cce7-113">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3cce7-114">Velja fyrirspurn fyrir þessa reglu.</span><span class="sxs-lookup"><span data-stu-id="3cce7-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="3cce7-115">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="3cce7-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="3cce7-116">Smellt er á Breyta fyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="3cce7-116">Click Edit query.</span></span>
    * <span data-ttu-id="3cce7-117">Breyta skal fyrirspurninni eftir því sem þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="3cce7-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="3cce7-118">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="3cce7-118">Click OK.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="3cce7-119">Útiloka notendum frá sjálfvirka hlutverkaúthlutun</span><span class="sxs-lookup"><span data-stu-id="3cce7-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="3cce7-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3cce7-120">Close the page.</span></span>
2. <span data-ttu-id="3cce7-121">Fara í Kerfisstjórn > Öryggi > Úthluta hlutverkum á notendur.</span><span class="sxs-lookup"><span data-stu-id="3cce7-121">Go to System administration > Security > Assign users to roles.</span></span>
3. <span data-ttu-id="3cce7-122">Í þessu dæmi skal velja yfirmaður Bókhalds.</span><span class="sxs-lookup"><span data-stu-id="3cce7-122">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="3cce7-123">Veljið hlutverk.</span><span class="sxs-lookup"><span data-stu-id="3cce7-123">Select a role.</span></span> <span data-ttu-id="3cce7-124">Fyrir þessu dæmi skal velja yfirmann bókhalds.</span><span class="sxs-lookup"><span data-stu-id="3cce7-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="3cce7-125">Smelltu á Úthluta / útiloka notendum handvirkt.</span><span class="sxs-lookup"><span data-stu-id="3cce7-125">Click Manually assign / exclude users.</span></span>
5. <span data-ttu-id="3cce7-126">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="3cce7-126">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="3cce7-127">Velja notanda</span><span class="sxs-lookup"><span data-stu-id="3cce7-127">Select a user.</span></span>  
6. <span data-ttu-id="3cce7-128">Smelltu á Útiloka frá hlutverki.</span><span class="sxs-lookup"><span data-stu-id="3cce7-128">Click Exclude from role.</span></span>
    * <span data-ttu-id="3cce7-129">Smelltu á Útiloka frá hlutverki til útiloka valda notendur úr hlutverinu.</span><span class="sxs-lookup"><span data-stu-id="3cce7-129">Click Exclude from role to exclude the selected users from the role.</span></span> <span data-ttu-id="3cce7-130">Til að fjarlægja útilokanir, veljið notendur sem á að fjarlægja útilokanir á og smellið síðan á Endurstilla stöðu.</span><span class="sxs-lookup"><span data-stu-id="3cce7-130">To remove exclusions, select the users that you want to remove exclusions for, and then click Reset status.</span></span> <span data-ttu-id="3cce7-131">Þegar fjarlægja útilokun með því að endurstilla stöðu notanda er hlutverki notanda aftur úthlutað sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="3cce7-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="3cce7-132">Hins vegar notanda er ekki strax þetta hlutverk úthlutað eða útilokað frá hlutverki þegar endurstilla stöðu.</span><span class="sxs-lookup"><span data-stu-id="3cce7-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="3cce7-133">Í stað þess, notandinn annað hvort úthlutaður í hlutverkið eða fjarlægð úr hlutverk í næsta sinn sem keyrðar eru reglum fyrir sjálfvirka hlutverkaúthlutun.</span><span class="sxs-lookup"><span data-stu-id="3cce7-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  

