--- 
title: "Nýir notendur stofnaðir"
description: "Notendur eru innri starfsmenn fyrirtækisins, eða ytri viðskiptavinir og lánardrottnar sem þurfa aðgang að kerfinu til að framkvæma vinnslum."
author: maertenm
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 295c355286b3d2df39cf1144ba7bfecdca25f9cb
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2018

---
# <a name="create-new-users"></a><span data-ttu-id="f9a45-103">Nýir notendur stofnaðir</span><span class="sxs-lookup"><span data-stu-id="f9a45-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f9a45-104">Notendur eru innri starfsmenn fyrirtækisins, eða ytri viðskiptavinir og lánardrottnar sem þurfa aðgang að kerfinu til að framkvæma vinnslum.</span><span class="sxs-lookup"><span data-stu-id="f9a45-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="f9a45-105">Kerfisstjórar geta lokið við þetta ferli til að bæta við notendum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="f9a45-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="f9a45-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="f9a45-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="f9a45-107">Bæta við nýr notandi</span><span class="sxs-lookup"><span data-stu-id="f9a45-107">Add a new user</span></span>
1. <span data-ttu-id="f9a45-108">Farið í Kerfisstjórnun > Notendur > Notendur.</span><span class="sxs-lookup"><span data-stu-id="f9a45-108">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="f9a45-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="f9a45-109">Click New.</span></span>
3. <span data-ttu-id="f9a45-110">Í reitnum Notandakenni skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f9a45-110">In the User ID field, type a value.</span></span>
    * <span data-ttu-id="f9a45-111">Færið inn einkvæmt kenni fyrir notandann.</span><span class="sxs-lookup"><span data-stu-id="f9a45-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="f9a45-112">Notandakenni er áskilið.</span><span class="sxs-lookup"><span data-stu-id="f9a45-112">A user ID is required.</span></span>  
4. <span data-ttu-id="f9a45-113">Í reitinn notandanafn skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f9a45-113">In the User name field, type a value.</span></span>
    * <span data-ttu-id="f9a45-114">Færið inn nafn notanda.</span><span class="sxs-lookup"><span data-stu-id="f9a45-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="f9a45-115">Í reitnum Lén skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f9a45-115">In the Domain field, type a value.</span></span>
    * <span data-ttu-id="f9a45-116">Færa skal inn lén notanda.</span><span class="sxs-lookup"><span data-stu-id="f9a45-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="f9a45-117">Í reitnum Gælunafn skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f9a45-117">In the Alias field, type a value.</span></span>
    * <span data-ttu-id="f9a45-118">Færa skal inn auknefni notanda.</span><span class="sxs-lookup"><span data-stu-id="f9a45-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="f9a45-119">Í reitnum Fyrirtæki skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f9a45-119">In the Company field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="f9a45-120">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="f9a45-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="f9a45-121">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="f9a45-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f9a45-122">Veldu fyrirtæki notandans</span><span class="sxs-lookup"><span data-stu-id="f9a45-122">Select the user's company</span></span>  
10. <span data-ttu-id="f9a45-123">Smellt er á Úthluta hlutverkum.</span><span class="sxs-lookup"><span data-stu-id="f9a45-123">Click Assign roles.</span></span>
11. <span data-ttu-id="f9a45-124">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="f9a45-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="f9a45-125">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="f9a45-125">Click OK.</span></span>
13. <span data-ttu-id="f9a45-126">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="f9a45-126">Click Save.</span></span>

## <a name="import-users"></a><span data-ttu-id="f9a45-127">Flytja inn notendur</span><span class="sxs-lookup"><span data-stu-id="f9a45-127">Import users</span></span>
1. <span data-ttu-id="f9a45-128">Smelltu á Flytja inn notendur.</span><span class="sxs-lookup"><span data-stu-id="f9a45-128">Click Import users.</span></span>
2. <span data-ttu-id="f9a45-129">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="f9a45-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="f9a45-130">Smelltu á Flytja inn notendur.</span><span class="sxs-lookup"><span data-stu-id="f9a45-130">Click Import users.</span></span>
4. <span data-ttu-id="f9a45-131">Smellið á „Loka“.</span><span class="sxs-lookup"><span data-stu-id="f9a45-131">Click Close.</span></span>


