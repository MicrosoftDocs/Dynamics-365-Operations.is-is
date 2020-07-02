---
title: Nýir notendur stofnaðir
description: Notendur eru innri starfsmenn fyrirtækisins, eða ytri viðskiptavinir og lánardrottnar sem þurfa aðgang að kerfinu til að framkvæma vinnslum.
author: maertenm
manager: AnnBe
ms.date: 06/08/2020
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
ms.openlocfilehash: d126b449074663772549b96b86acb53db971a5d4
ms.sourcegitcommit: 7d943499f302298c6ff127f56cecc34af6cee289
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/08/2020
ms.locfileid: "3435585"
---
# <a name="create-new-users"></a><span data-ttu-id="64b15-103">Nýir notendur stofnaðir</span><span class="sxs-lookup"><span data-stu-id="64b15-103">Create new users</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="64b15-104">Notendur eru innri starfsmenn fyrirtækisins, eða ytri viðskiptavinir og lánardrottnar sem þurfa aðgang að kerfinu til að keyra vinnslur.</span><span class="sxs-lookup"><span data-stu-id="64b15-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="64b15-105">Úthlutaðu notanda leyfi (aðeins nýjar tegundir leyfis)</span><span class="sxs-lookup"><span data-stu-id="64b15-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="64b15-106">Fyrir viðskiptavini sem eru á einni af nýju leyfistegundunum sem bætt var við í október 2019, verða notendur að hafa úthluta leyfi.</span><span class="sxs-lookup"><span data-stu-id="64b15-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="64b15-107">Notendur sem er úthlutað leyfi bætast sjálfkrafa við sem kerfisnotendur sem hafa engin hlutverk í fyrsta skipti sem þeir skrá sig inn.</span><span class="sxs-lookup"><span data-stu-id="64b15-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span>

<span data-ttu-id="64b15-108">Kerfisstjórar geta það [úthluta leyfi til notenda](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) í [stjórnunarmiðstöð Microsoft 365](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="64b15-108">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a><span data-ttu-id="64b15-109">Úthlutaðu ytri notanda leyfi (aðeins nýjar tegundir leyfis)</span><span class="sxs-lookup"><span data-stu-id="64b15-109">Associate an external user with a license (new license types only)</span></span>
<span data-ttu-id="64b15-110">Notendur utan leigjandans sem umhverfinu var dreift í þurfa að vera fulltrúar í hýsingaraðilum leigjanda (Azure Active Directory (Azure AD)) svo að hægt sé að fá þeim leyfi.</span><span class="sxs-lookup"><span data-stu-id="64b15-110">Users external to the tenant that the environment was deployed into need to be represented in the host tenant directory (Azure Active Directory (Azure AD)) so that they can be assigned licenses.</span></span> <span data-ttu-id="64b15-111">Þessum utanaðkomandi notendum ætti að bæta við leigjandann í Azure AD sem gestanotendum og úthluta þeim síðan viðeigandi leyfum.</span><span class="sxs-lookup"><span data-stu-id="64b15-111">Those external users should be added to the tenant in Azure AD as guest users and then assigned the appropriate licenses.</span></span> <span data-ttu-id="64b15-112">Nánari upplýsingar er að finna í [Bæta Azure Active Directory B2B samvinnunotendum við í Azure-gáttinni](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span><span class="sxs-lookup"><span data-stu-id="64b15-112">For more information, see [Add Azure Active Directory B2B collaboration users in the Azure portal](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="64b15-113">Bæta við nýr notandi</span><span class="sxs-lookup"><span data-stu-id="64b15-113">Add a new user</span></span>
1. <span data-ttu-id="64b15-114">Farðu í **Kerfisstjórnun \> Notendur \> Notendur**.</span><span class="sxs-lookup"><span data-stu-id="64b15-114">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="64b15-115">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="64b15-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="64b15-116">Í reitnum **Notandakenni** er fært inn einkvæmt kenni fyrir notandann.</span><span class="sxs-lookup"><span data-stu-id="64b15-116">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="64b15-117">Notandakenni er áskilið.</span><span class="sxs-lookup"><span data-stu-id="64b15-117">A user ID is required.</span></span>  
4. <span data-ttu-id="64b15-118">Í reitnum **Notandanafn** skal færa inn notandaheiti.</span><span class="sxs-lookup"><span data-stu-id="64b15-118">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="64b15-119">Í reitinn **Lén** er lén notanda fært inn.</span><span class="sxs-lookup"><span data-stu-id="64b15-119">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="64b15-120">Í reitinn **Samheiti** skal slá inn samheiti notandans.</span><span class="sxs-lookup"><span data-stu-id="64b15-120">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="64b15-121">Í reitnum **Fyrirtæki** skal velja óskað fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="64b15-121">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="64b15-122">Á flýtiflipanum **Hlutverk notanda** velurðu **Úthluta hlutverkum** til að úthluta notendum á öryggishlutverk.</span><span class="sxs-lookup"><span data-stu-id="64b15-122">On the **User's roles** FastTab, select **Assign roles** to assign users to security roles.</span></span> <span data-ttu-id="64b15-123">Nánari upplýsingar er að finna á [Úthluta notendum á öryggishlutverk](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="64b15-123">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span>
9. <span data-ttu-id="64b15-124">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="64b15-124">Select **OK**.</span></span>
10. <span data-ttu-id="64b15-125">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="64b15-125">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="64b15-126">Flytja inn notendur</span><span class="sxs-lookup"><span data-stu-id="64b15-126">Import users</span></span>
1. <span data-ttu-id="64b15-127">Farðu í **Kerfisstjórnun \> Notendur \> Notendur**.</span><span class="sxs-lookup"><span data-stu-id="64b15-127">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="64b15-128">Á Aðgerðasvæðinu skal velja **Flytja inn notendur**.</span><span class="sxs-lookup"><span data-stu-id="64b15-128">On the Action Pane, select **Import users**.</span></span>
3. <span data-ttu-id="64b15-129">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="64b15-129">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="64b15-130">Veldu **Flytja inn notendur**.</span><span class="sxs-lookup"><span data-stu-id="64b15-130">Select **Import users**.</span></span>
5. <span data-ttu-id="64b15-131">Veljið **Loka**.</span><span class="sxs-lookup"><span data-stu-id="64b15-131">Select **Close**.</span></span>

