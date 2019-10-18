---
title: Nýir notendur stofnaðir
description: Notendur eru innri starfsmenn fyrirtækisins, eða ytri viðskiptavinir og lánardrottnar sem þurfa aðgang að kerfinu til að framkvæma vinnslum.
author: maertenm
manager: AnnBe
ms.date: 08/30/2019
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
ms.openlocfilehash: 4a5635f96132b2e52227b569e7e480fa55e82d61
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180945"
---
# <a name="create-new-users"></a><span data-ttu-id="c0b25-103">Nýir notendur stofnaðir</span><span class="sxs-lookup"><span data-stu-id="c0b25-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]
[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="c0b25-104">Notendur eru innri starfsmenn fyrirtækisins, eða ytri viðskiptavinir og lánardrottnar sem þurfa aðgang að kerfinu til að keyra vinnslur.</span><span class="sxs-lookup"><span data-stu-id="c0b25-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="c0b25-105">Úthlutaðu notanda leyfi (aðeins nýjar tegundir leyfis)</span><span class="sxs-lookup"><span data-stu-id="c0b25-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="c0b25-106">Fyrir viðskiptavini sem eru á einni af nýju leyfistegundunum sem bætt var við í október 2019, verða notendur að hafa úthluta leyfi.</span><span class="sxs-lookup"><span data-stu-id="c0b25-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="c0b25-107">Notendur sem er úthlutað leyfi bætast sjálfkrafa við sem kerfisnotendur sem hafa engin hlutverk í fyrsta skipti sem þeir skrá sig inn.</span><span class="sxs-lookup"><span data-stu-id="c0b25-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span> <span data-ttu-id="c0b25-108">Notendur sem ekki er úthlutað leyfi fá viðvörunarskilaboð.</span><span class="sxs-lookup"><span data-stu-id="c0b25-108">Users who aren't associated with a licence receive a warning message.</span></span>

<span data-ttu-id="c0b25-109">Kerfisstjórar geta það [úthluta leyfi til notenda](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) í [stjórnunarmiðstöð Microsoft 365](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="c0b25-109">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="c0b25-110">Bæta við nýr notandi</span><span class="sxs-lookup"><span data-stu-id="c0b25-110">Add a new user</span></span>
1. <span data-ttu-id="c0b25-111">Farðu í **Kerfisstjórnun \> Notendur \> Notendur**.</span><span class="sxs-lookup"><span data-stu-id="c0b25-111">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="c0b25-112">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="c0b25-112">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="c0b25-113">Í reitnum **Notandakenni** er fært inn einkvæmt kenni fyrir notandann.</span><span class="sxs-lookup"><span data-stu-id="c0b25-113">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="c0b25-114">Notandakenni er áskilið.</span><span class="sxs-lookup"><span data-stu-id="c0b25-114">A user ID is required.</span></span>  
4. <span data-ttu-id="c0b25-115">Í reitnum **Notandanafn** skal færa inn notandaheiti.</span><span class="sxs-lookup"><span data-stu-id="c0b25-115">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="c0b25-116">Í reitinn **Lén** er lén notanda fært inn.</span><span class="sxs-lookup"><span data-stu-id="c0b25-116">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="c0b25-117">Í reitinn **Samheiti** skal slá inn samheiti notandans.</span><span class="sxs-lookup"><span data-stu-id="c0b25-117">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="c0b25-118">Í reitnum **Fyrirtæki** skal velja óskað fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="c0b25-118">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="c0b25-119">Á flýtiflipanum **Hlutverk notanda** velurðu **Úthluta hlutverkum** til að [úthluta notendum á öryggishlutverk](assign-users-security-roles.md)</span><span class="sxs-lookup"><span data-stu-id="c0b25-119">On the **User's roles** FastTab, select **Assign roles** to [assign users to security roles](assign-users-security-roles.md)</span></span>
9. <span data-ttu-id="c0b25-120">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="c0b25-120">Select **OK**.</span></span>
10. <span data-ttu-id="c0b25-121">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="c0b25-121">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="c0b25-122">Flytja inn notendur</span><span class="sxs-lookup"><span data-stu-id="c0b25-122">Import users</span></span>
1. <span data-ttu-id="c0b25-123">Á Aðgerðasvæðinu skal velja **Flytja inn notendur**.</span><span class="sxs-lookup"><span data-stu-id="c0b25-123">On the Action Pane, select **Import users**.</span></span>
2. <span data-ttu-id="c0b25-124">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="c0b25-124">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="c0b25-125">Veldu **Flytja inn notendur**.</span><span class="sxs-lookup"><span data-stu-id="c0b25-125">Select **Import users**.</span></span>
4. <span data-ttu-id="c0b25-126">Veljið **Loka**.</span><span class="sxs-lookup"><span data-stu-id="c0b25-126">Select **Close**.</span></span>

