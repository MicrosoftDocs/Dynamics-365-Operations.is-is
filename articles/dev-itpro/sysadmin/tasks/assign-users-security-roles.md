--- 
title: "Skipa notendum í öryggishlutverk"
description: "Til að fá aðgang að Microsoft Dynamics 365 for Finance and Operations þurfa notendur að fá úthlutað öryggishlutverki."
author: maertenm
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c7f35f57223798e91fc2a81c0821a2dc81512624
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="3325e-103">Úthluta notendum á öryggishlutverk</span><span class="sxs-lookup"><span data-stu-id="3325e-103">Assign users to security roles</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3325e-104">Til að fá aðgang að Microsoft Dynamics 365 for Finance and Operations þurfa notendur að fá úthlutað öryggishlutverki.</span><span class="sxs-lookup"><span data-stu-id="3325e-104">To access Microsoft Dynamics 365 for Finance and Operations, users must be assigned to security roles.</span></span> <span data-ttu-id="3325e-105">Þessu ferli útskýrt hvernig kerfisstjórum hægt úthluta notendum á hlutverk sjálfkrafa, byggt á viðskiptagögn.</span><span class="sxs-lookup"><span data-stu-id="3325e-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="3325e-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="3325e-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="3325e-107">Sjálfkrafa skipa notendum í hlutverkin</span><span class="sxs-lookup"><span data-stu-id="3325e-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="3325e-108">Fara í Kerfisstjórn > Öryggi > Úthluta hlutverkum á notendur.</span><span class="sxs-lookup"><span data-stu-id="3325e-108">Go to System administration > Security > Assign users to roles.</span></span>
2. <span data-ttu-id="3325e-109">Í þessu dæmi skal velja yfirmaður Bókhalds.</span><span class="sxs-lookup"><span data-stu-id="3325e-109">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="3325e-110">Veljið hlutverk sem nota á fyrir útvinnsluna á reglunni.</span><span class="sxs-lookup"><span data-stu-id="3325e-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="3325e-111">Í þessu dæmi skal velja yfirmann bókhalds.</span><span class="sxs-lookup"><span data-stu-id="3325e-111">In this example, select Accounting supervisor.</span></span>  
3. <span data-ttu-id="3325e-112">Smelltu á bæta við reglu til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="3325e-112">Click Add rule to open the drop dialog.</span></span>
4. <span data-ttu-id="3325e-113">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="3325e-113">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3325e-114">Velja fyrirspurn fyrir þessa reglu.</span><span class="sxs-lookup"><span data-stu-id="3325e-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="3325e-115">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="3325e-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="3325e-116">Smellt er á Breyta fyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="3325e-116">Click Edit query.</span></span>
    * <span data-ttu-id="3325e-117">Breyta skal fyrirspurninni eftir því sem þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="3325e-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="3325e-118">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="3325e-118">Click OK.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="3325e-119">Útiloka notendum frá sjálfvirka hlutverkaúthlutun</span><span class="sxs-lookup"><span data-stu-id="3325e-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="3325e-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3325e-120">Close the page.</span></span>
2. <span data-ttu-id="3325e-121">Fara í Kerfisstjórn > Öryggi > Úthluta hlutverkum á notendur.</span><span class="sxs-lookup"><span data-stu-id="3325e-121">Go to System administration > Security > Assign users to roles.</span></span>
3. <span data-ttu-id="3325e-122">Í þessu dæmi skal velja yfirmaður Bókhalds.</span><span class="sxs-lookup"><span data-stu-id="3325e-122">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="3325e-123">Veljið hlutverk.</span><span class="sxs-lookup"><span data-stu-id="3325e-123">Select a role.</span></span> <span data-ttu-id="3325e-124">Fyrir þessu dæmi skal velja yfirmann bókhalds.</span><span class="sxs-lookup"><span data-stu-id="3325e-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="3325e-125">Smelltu á Úthluta / útiloka notendum handvirkt.</span><span class="sxs-lookup"><span data-stu-id="3325e-125">Click Manually assign / exclude users.</span></span>
5. <span data-ttu-id="3325e-126">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="3325e-126">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="3325e-127">Velja notanda</span><span class="sxs-lookup"><span data-stu-id="3325e-127">Select a user.</span></span>  
6. <span data-ttu-id="3325e-128">Smelltu á Útiloka frá hlutverki.</span><span class="sxs-lookup"><span data-stu-id="3325e-128">Click Exclude from role.</span></span>
    * <span data-ttu-id="3325e-129">Smelltu á Útiloka frá hlutverki til útiloka valda notendur úr hlutverinu.</span><span class="sxs-lookup"><span data-stu-id="3325e-129">Click Exclude from role to exclude the selected users from the role.</span></span> <span data-ttu-id="3325e-130">Til að fjarlægja útilokanir, veljið notendur sem á að fjarlægja útilokanir á og smellið síðan á Endurstilla stöðu.</span><span class="sxs-lookup"><span data-stu-id="3325e-130">To remove exclusions, select the users that you want to remove exclusions for, and then click Reset status.</span></span> <span data-ttu-id="3325e-131">Þegar fjarlægja útilokun með því að endurstilla stöðu notanda er hlutverki notanda aftur úthlutað sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="3325e-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="3325e-132">Hins vegar notanda er ekki strax þetta hlutverk úthlutað eða útilokað frá hlutverki þegar endurstilla stöðu.</span><span class="sxs-lookup"><span data-stu-id="3325e-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="3325e-133">Í stað þess, notandinn annað hvort úthlutaður í hlutverkið eða fjarlægð úr hlutverk í næsta sinn sem keyrðar eru reglum fyrir sjálfvirka hlutverkaúthlutun.</span><span class="sxs-lookup"><span data-stu-id="3325e-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  


