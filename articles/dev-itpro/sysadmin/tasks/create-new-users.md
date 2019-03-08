---
title: Nýir notendur stofnaðir
description: Notendur eru innri starfsmenn fyrirtækisins, eða ytri viðskiptavinir og lánardrottnar sem þurfa aðgang að kerfinu til að framkvæma vinnslum.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 12cf223d262c4e0f2a195e95c83a00fc1a3f07e5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "361959"
---
# <a name="create-new-users"></a><span data-ttu-id="e109e-103">Nýir notendur stofnaðir</span><span class="sxs-lookup"><span data-stu-id="e109e-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e109e-104">Notendur eru innri starfsmenn fyrirtækisins, eða ytri viðskiptavinir og lánardrottnar sem þurfa aðgang að kerfinu til að framkvæma vinnslum.</span><span class="sxs-lookup"><span data-stu-id="e109e-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="e109e-105">Kerfisstjórar geta lokið við þetta ferli til að bæta við notendum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="e109e-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="e109e-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="e109e-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="e109e-107">Bæta við nýr notandi</span><span class="sxs-lookup"><span data-stu-id="e109e-107">Add a new user</span></span>
1. <span data-ttu-id="e109e-108">Farið í Kerfisstjórnun > Notendur > Notendur.</span><span class="sxs-lookup"><span data-stu-id="e109e-108">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="e109e-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="e109e-109">Click New.</span></span>
3. <span data-ttu-id="e109e-110">Í reitnum Notandakenni skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e109e-110">In the User ID field, type a value.</span></span>
    * <span data-ttu-id="e109e-111">Færið inn einkvæmt kenni fyrir notandann.</span><span class="sxs-lookup"><span data-stu-id="e109e-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="e109e-112">Notandakenni er áskilið.</span><span class="sxs-lookup"><span data-stu-id="e109e-112">A user ID is required.</span></span>  
4. <span data-ttu-id="e109e-113">Í reitinn notandanafn skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e109e-113">In the User name field, type a value.</span></span>
    * <span data-ttu-id="e109e-114">Færið inn nafn notanda.</span><span class="sxs-lookup"><span data-stu-id="e109e-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="e109e-115">Í reitnum Lén skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e109e-115">In the Domain field, type a value.</span></span>
    * <span data-ttu-id="e109e-116">Færa skal inn lén notanda.</span><span class="sxs-lookup"><span data-stu-id="e109e-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="e109e-117">Í reitnum Gælunafn skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e109e-117">In the Alias field, type a value.</span></span>
    * <span data-ttu-id="e109e-118">Færa skal inn auknefni notanda.</span><span class="sxs-lookup"><span data-stu-id="e109e-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="e109e-119">Í reitnum Fyrirtæki skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="e109e-119">In the Company field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="e109e-120">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="e109e-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="e109e-121">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="e109e-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e109e-122">Veldu fyrirtæki notandans</span><span class="sxs-lookup"><span data-stu-id="e109e-122">Select the user's company</span></span>  
10. <span data-ttu-id="e109e-123">Smellt er á Úthluta hlutverkum.</span><span class="sxs-lookup"><span data-stu-id="e109e-123">Click Assign roles.</span></span>
11. <span data-ttu-id="e109e-124">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="e109e-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="e109e-125">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e109e-125">Click OK.</span></span>
13. <span data-ttu-id="e109e-126">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e109e-126">Click Save.</span></span>

## <a name="import-users"></a><span data-ttu-id="e109e-127">Flytja inn notendur</span><span class="sxs-lookup"><span data-stu-id="e109e-127">Import users</span></span>
1. <span data-ttu-id="e109e-128">Smelltu á Flytja inn notendur.</span><span class="sxs-lookup"><span data-stu-id="e109e-128">Click Import users.</span></span>
2. <span data-ttu-id="e109e-129">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="e109e-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="e109e-130">Smelltu á Flytja inn notendur.</span><span class="sxs-lookup"><span data-stu-id="e109e-130">Click Import users.</span></span>
4. <span data-ttu-id="e109e-131">Smellið á „Loka“.</span><span class="sxs-lookup"><span data-stu-id="e109e-131">Click Close.</span></span>

