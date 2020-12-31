---
title: Úthluta notendahlutverkum leigu
description: Þetta efnisatriði lýsir öryggishlutverkum sem eru notuð í Eignarleigu. Það útskýrir einnig hvernig á að úthluta notendum á þau hlutverk.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b31d0880d4f2cd2b8ad2dffcfe279421f935ed35
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4444589"
---
# <a name="assign-lease-user-roles"></a><span data-ttu-id="16850-104">Úthluta notendahlutverkum leigu</span><span class="sxs-lookup"><span data-stu-id="16850-104">Assign lease user roles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16850-105">Þetta efnisatriði lýsir öryggishlutverkum sem eru notuð í Eignarleigu.</span><span class="sxs-lookup"><span data-stu-id="16850-105">This topic describes the security roles that are used in Asset leasing.</span></span> <span data-ttu-id="16850-106">Það útskýrir einnig hvernig á að úthluta notendum á þau hlutverk.</span><span class="sxs-lookup"><span data-stu-id="16850-106">It also explains how to assign users to those roles.</span></span>

<span data-ttu-id="16850-107">Þrjú hlutverk notanda aðgreina aðgang að Eignarleigu.</span><span class="sxs-lookup"><span data-stu-id="16850-107">Three user roles differentiate access in Asset leasing.</span></span> <span data-ttu-id="16850-108">Eitt hlutverk er viðeigandi fyrir umsjón leigusamnings, eitt er viðeigandi til að skoðun leigusamninga og eitt er viðeigandi til að framkvæma skyldur leigutaka.</span><span class="sxs-lookup"><span data-stu-id="16850-108">One role is appropriate for maintaining leases, one is appropriate for viewing leases, and one is appropriate for performing a lease clerk's duties.</span></span> <span data-ttu-id="16850-109">Hvert hlutverk er með ákveðnar heimildir fyrir allar leigusíður og hver býður notendum að skoða, búa til, breyta eða eyða leigusamningum, í samræmi við starfsskyldur sínar.</span><span class="sxs-lookup"><span data-stu-id="16850-109">Each role has specific permissions for all lease pages, and each lets users view, create, edit, or delete leases, according to their job duties.</span></span>

| <span data-ttu-id="16850-110">Hlutverk</span><span class="sxs-lookup"><span data-stu-id="16850-110">Role</span></span>           | <span data-ttu-id="16850-111">lýsing</span><span class="sxs-lookup"><span data-stu-id="16850-111">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="16850-112">Vinna með leigusamning</span><span class="sxs-lookup"><span data-stu-id="16850-112">Maintain Lease</span></span> | <span data-ttu-id="16850-113">Notendur í þessu hlutverki geta bætt við, breytt, eytt og skoðað leigu.</span><span class="sxs-lookup"><span data-stu-id="16850-113">Users in this role can add, edit, delete, and view leases.</span></span> <span data-ttu-id="16850-114">Þetta hlutverk er hannað fyrir daglega notendur sem stofna og bóka mánaðarlegar færslubókarfærslur og bæta við nýjum leigusamningum.</span><span class="sxs-lookup"><span data-stu-id="16850-114">This role is designed for daily users whose tasks include creating and posting monthly journal entries and adding new leases.</span></span> <span data-ttu-id="16850-115">Þetta hlutverk veitir aðgang að allri virkni Eignarleigu.</span><span class="sxs-lookup"><span data-stu-id="16850-115">This role gives access to all Asset leasing functionality.</span></span> |
| <span data-ttu-id="16850-116">Skoða leigusamning</span><span class="sxs-lookup"><span data-stu-id="16850-116">View Lease</span></span>     | <span data-ttu-id="16850-117">Notendur í þessu hlutverki geta aðeins skoðað leiguskrár, áætlanir og keyrt skýrslur.</span><span class="sxs-lookup"><span data-stu-id="16850-117">Users in this role can only view lease records, schedules, and run reports.</span></span> <span data-ttu-id="16850-118">Þeir geta ekki stofnað nýja leigu, breytt fyrirliggjandi leigusamningum eða stofnað færslubókarfærslu gegn leigutekjum.</span><span class="sxs-lookup"><span data-stu-id="16850-118">They can't create new leases, edit existing leases, or create journal entries against leases.</span></span> <span data-ttu-id="16850-119">Hlutverkið er hannað fyrir notendur sem þurfa aðeins að skoða leigusamninga, leiguáætlanir og færslurnar sem eiga sér stað gagnvart þessum leigum.</span><span class="sxs-lookup"><span data-stu-id="16850-119">The role is designed for users who just have to view leases, lease schedules, and the transactions that occur against those leases.</span></span> |
| <span data-ttu-id="16850-120">Afgreiðslustarfsmaður leiguskrifstofu</span><span class="sxs-lookup"><span data-stu-id="16850-120">Lease Clerk</span></span>    | <span data-ttu-id="16850-121">Notendur í þessu hlutverki geta aðeins stofnað nýjar leigur.</span><span class="sxs-lookup"><span data-stu-id="16850-121">Users in this role can only create new leases.</span></span> <span data-ttu-id="16850-122">Þeir geta ekki breytt eða eytt eldri leigusamningum, skoðað leigutímaáætlanir eða birt færslur leigubókar.</span><span class="sxs-lookup"><span data-stu-id="16850-122">They can't edit or delete existing leases, view lease schedules, or post leasing journal entries.</span></span> <span data-ttu-id="16850-123">Þetta hlutverk er hannað fyrir notendur sem vinna við gagnaskráningu.</span><span class="sxs-lookup"><span data-stu-id="16850-123">This role is designed for users who work in a data entry capacity.</span></span> |

<span data-ttu-id="16850-124">Fylgið eftirfarandi skrefum til að úthluta notendum á hlutverk sem eru notuð í eignaleigu.</span><span class="sxs-lookup"><span data-stu-id="16850-124">Follow these steps to assign users to the roles that are used in Asset leasing.</span></span>

1. <span data-ttu-id="16850-125">Fara í **Kerfisstjórn\>öryggi\>úthluta hlutverkum á notendur**.</span><span class="sxs-lookup"><span data-stu-id="16850-125">Go to **System administration \> Security \> Assign users to roles**.</span></span>
2. <span data-ttu-id="16850-126">Veljið **Vinna með leigusamning**, **Afgreiðslustarfsmaður leiguskrifstofu** eða **Skoða leigusamning** og veljið svo **Úthluta/útiloka notendur handvirkt**.</span><span class="sxs-lookup"><span data-stu-id="16850-126">Select the **Maintain lease**, **Lease clerk**, or **View lease** role, and then select **Manually assign/exclude users**.</span></span>
3. <span data-ttu-id="16850-127">Veljið notandann sem á að úthluta hlutverkinu og velja svo **Úthluta hlutverki**.</span><span class="sxs-lookup"><span data-stu-id="16850-127">Select the user to assign to the role, and then select **Assign to role**.</span></span>
