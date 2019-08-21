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
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 89e492ef5030dd28020094152259b615010aa676
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851312"
---
# <a name="create-new-users"></a><span data-ttu-id="b5583-103">Nýir notendur stofnaðir</span><span class="sxs-lookup"><span data-stu-id="b5583-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b5583-104">Notendur eru innri starfsmenn fyrirtækisins, eða ytri viðskiptavinir og lánardrottnar sem þurfa aðgang að kerfinu til að framkvæma vinnslum.</span><span class="sxs-lookup"><span data-stu-id="b5583-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="b5583-105">Kerfisstjórar geta lokið við þetta ferli til að bæta við notendum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="b5583-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="b5583-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="b5583-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="b5583-107">Bæta við nýr notandi</span><span class="sxs-lookup"><span data-stu-id="b5583-107">Add a new user</span></span>
1. <span data-ttu-id="b5583-108">Farið í Kerfisstjórnun > Notendur > Notendur.</span><span class="sxs-lookup"><span data-stu-id="b5583-108">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="b5583-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="b5583-109">Click New.</span></span>
3. <span data-ttu-id="b5583-110">Í reitnum Notandakenni skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b5583-110">In the User ID field, type a value.</span></span>
    * <span data-ttu-id="b5583-111">Færið inn einkvæmt kenni fyrir notandann.</span><span class="sxs-lookup"><span data-stu-id="b5583-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="b5583-112">Notandakenni er áskilið.</span><span class="sxs-lookup"><span data-stu-id="b5583-112">A user ID is required.</span></span>  
4. <span data-ttu-id="b5583-113">Í reitinn notandanafn skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b5583-113">In the User name field, type a value.</span></span>
    * <span data-ttu-id="b5583-114">Færið inn nafn notanda.</span><span class="sxs-lookup"><span data-stu-id="b5583-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="b5583-115">Í reitnum Lén skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b5583-115">In the Domain field, type a value.</span></span>
    * <span data-ttu-id="b5583-116">Færa skal inn lén notanda.</span><span class="sxs-lookup"><span data-stu-id="b5583-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="b5583-117">Í reitnum Gælunafn skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b5583-117">In the Alias field, type a value.</span></span>
    * <span data-ttu-id="b5583-118">Færa skal inn auknefni notanda.</span><span class="sxs-lookup"><span data-stu-id="b5583-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="b5583-119">Í reitnum Fyrirtæki skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="b5583-119">In the Company field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="b5583-120">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="b5583-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="b5583-121">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="b5583-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b5583-122">Veldu fyrirtæki notandans</span><span class="sxs-lookup"><span data-stu-id="b5583-122">Select the user's company</span></span>  
10. <span data-ttu-id="b5583-123">Smellt er á Úthluta hlutverkum.</span><span class="sxs-lookup"><span data-stu-id="b5583-123">Click Assign roles.</span></span>
11. <span data-ttu-id="b5583-124">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="b5583-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="b5583-125">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b5583-125">Click OK.</span></span>
13. <span data-ttu-id="b5583-126">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b5583-126">Click Save.</span></span>

## <a name="import-users"></a><span data-ttu-id="b5583-127">Flytja inn notendur</span><span class="sxs-lookup"><span data-stu-id="b5583-127">Import users</span></span>
1. <span data-ttu-id="b5583-128">Smelltu á Flytja inn notendur.</span><span class="sxs-lookup"><span data-stu-id="b5583-128">Click Import users.</span></span>
2. <span data-ttu-id="b5583-129">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="b5583-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="b5583-130">Smelltu á Flytja inn notendur.</span><span class="sxs-lookup"><span data-stu-id="b5583-130">Click Import users.</span></span>
4. <span data-ttu-id="b5583-131">Smellið á „Loka“.</span><span class="sxs-lookup"><span data-stu-id="b5583-131">Click Close.</span></span>

