---
title: Stjórna notendum og hlutverkum rafrænna viðskipta
description: Þetta efni útskýrir hvernig á að veita notendum aðgang að höfundarumhverfi fyrir Microsoft Dynamics 365 Commerce síðuna.
author: bicyclingfool
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23977ddc8ef67389d088ca52c1a1bc6a9b2f7fb4
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697682"
---
# <a name="manage-e-commerce-users-and-roles"></a><span data-ttu-id="45865-103">Stjórna notendum og hlutverkum rafrænna viðskipta</span><span class="sxs-lookup"><span data-stu-id="45865-103">Manage e-Commerce users and roles</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="45865-104">Þetta efni útskýrir hvernig á að veita notendum aðgang að höfundarumhverfi fyrir Microsoft Dynamics 365 Commerce síðuna.</span><span class="sxs-lookup"><span data-stu-id="45865-104">This topic explains how to grant users access to the authoring environment for your Microsoft Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="45865-105">Til að aðstoða við að stjórna aðgangi notenda og veita notendum leyfi til að framkvæma tiltekin verk notar höfundarumhverfi svæðisins öryggishópa sem þú býrð til í Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="45865-105">To help control user access and grant users permission to perform specific tasks, the site authoring environment uses security groups that you create in Microsoft Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="45865-106">Þú úthlutar fyrst nýjum eða núverandi öryggishópi frá Azure AD á hvert hlutverk í höfundarumhverfinu.</span><span class="sxs-lookup"><span data-stu-id="45865-106">You first assign a new or existing security group from Azure AD to each role in the authoring environment.</span></span> <span data-ttu-id="45865-107">Þú veitir eða afturkallar síðan leyfi fyrir einstaka notendur með því að annaðhvort bæta þeim notendum við viðeigandi öryggishóp eða fjarlægja þá úr öryggishópi.</span><span class="sxs-lookup"><span data-stu-id="45865-107">You then grant or revoke permissions for individual users by either adding those users to an appropriate security group or removing them from a security group.</span></span>

## <a name="overview-of-roles-in-the-authoring-environment"></a><span data-ttu-id="45865-108">Yfirlit yfir hlutverk í höfundarumhverfinu</span><span class="sxs-lookup"><span data-stu-id="45865-108">Overview of roles in the authoring environment</span></span>

<span data-ttu-id="45865-109">The Dynamics 365 for Commerce höfundarumhverfi styður eftirfarandi hlutverk.</span><span class="sxs-lookup"><span data-stu-id="45865-109">The Dynamics 365 for Commerce authoring environment supports the following roles.</span></span>

| <span data-ttu-id="45865-110">Hlutverk</span><span class="sxs-lookup"><span data-stu-id="45865-110">Role</span></span>                 | <span data-ttu-id="45865-111">Lýsing</span><span class="sxs-lookup"><span data-stu-id="45865-111">Description</span></span> |
|----------------------|-------------|
| <span data-ttu-id="45865-112">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="45865-112">System Administrator</span></span> | <span data-ttu-id="45865-113">Notendur sem hafa þetta hlutverk hafa öll réttindi fyrir öll verkfæri og fyrir allar einkunnir og umsagnir.</span><span class="sxs-lookup"><span data-stu-id="45865-113">Users who have this role have all privileges for all tools, and for all ratings and reviews.</span></span> <span data-ttu-id="45865-114">Þeir geta einnig búið til svæði.</span><span class="sxs-lookup"><span data-stu-id="45865-114">They can also create sites.</span></span> |
| <span data-ttu-id="45865-115">Stjórnandi</span><span class="sxs-lookup"><span data-stu-id="45865-115">Administrator</span></span>   | <span data-ttu-id="45865-116">Notendur sem hafa þetta hlutverk hafa öll réttindi fyrir öll verkfæri og RnR í tilteknu vefsvæði.</span><span class="sxs-lookup"><span data-stu-id="45865-116">Users who have this role have all privileges for all tools and RnR in a given site structure.</span></span> |
| <span data-ttu-id="45865-117">Vefframleiðandi</span><span class="sxs-lookup"><span data-stu-id="45865-117">Web Producer</span></span>         | <span data-ttu-id="45865-118">Notendur sem hafa þetta hlutverk geta búið til síður, brot og sniðmát, hlaðið upp og stjórnað eignum og auðgað vörur og flokka.</span><span class="sxs-lookup"><span data-stu-id="45865-118">Users who have this role can create pages, fragments and templates, upload and manage assets, and enrich products and categories.</span></span> |
| <span data-ttu-id="45865-119">Lesari</span><span class="sxs-lookup"><span data-stu-id="45865-119">Reader</span></span>               | <span data-ttu-id="45865-120">Notendur sem hafa þetta hlutverk geta skoðað síður, sniðmát, eignir, brot, skipulag og stillingar en mega ekki gera breytingar.</span><span class="sxs-lookup"><span data-stu-id="45865-120">Users who have this role can view pages, templates, assets, fragments, layouts and settings, but may not make changes.</span></span> |
| <span data-ttu-id="45865-121">RNR stjórnandi</span><span class="sxs-lookup"><span data-stu-id="45865-121">RnR Moderator</span></span>        | <span data-ttu-id="45865-122">Notendur sem hafa þetta hlutverk geta stjórnað afurðaumsögnum.</span><span class="sxs-lookup"><span data-stu-id="45865-122">Users who have this role can moderate product reviews.</span></span> |

## <a name="system-administrator-role"></a><span data-ttu-id="45865-123">Hlutverk kerfisstjóra</span><span class="sxs-lookup"><span data-stu-id="45865-123">System Administrator role</span></span>

<span data-ttu-id="45865-124">Þegar þú veitir Dynamics 365 Commerce í Microsoft Dynamics LCS (Lifecycle Services) umhverfi ertu beðin/n um að bjóða upp á öryggishóp fyrir hlutverkið **Kerfisstjóri**.</span><span class="sxs-lookup"><span data-stu-id="45865-124">When you provision Dynamics 365 Commerce in the Microsoft Dynamics Lifecycle Services (LCS) environment, you're asked to provide a security group for the **System Administrator** role.</span></span> <span data-ttu-id="45865-125">Þessu hlutverki er síðan sjálfkrafa beitt á allar síður sem þú býrð til í umhverfinu sem þú ert að stilla.</span><span class="sxs-lookup"><span data-stu-id="45865-125">This role is then automatically applied to all sites that you create in the environment that you're configuring.</span></span> <span data-ttu-id="45865-126">Aðeins er hægt að uppfæra öryggishópinn fyrir þetta hlutverk í LCS.</span><span class="sxs-lookup"><span data-stu-id="45865-126">The security group for this role can be updated only in LCS.</span></span> <span data-ttu-id="45865-127">Á síðunni **Vefumsjón** fyrir öll svæði birtist hann sem skrifvarinn og er einungis til upplýsinga.</span><span class="sxs-lookup"><span data-stu-id="45865-127">On the **Site Administration** page for all sites, it appears as read-only and is for informational purposes only.</span></span>

## <a name="administrator-role"></a><span data-ttu-id="45865-128">Hlutverk stjórnanda</span><span class="sxs-lookup"><span data-stu-id="45865-128">Administrator role</span></span>

<span data-ttu-id="45865-129">Þegar þú býrð til nýja síðu í Commerce ertu beðinn um að útvega öryggishóp fyrir hlutverkið **Stjórnandi**.</span><span class="sxs-lookup"><span data-stu-id="45865-129">When you create a new site in Commerce, you're asked to provide a security group for the **Administrator** role.</span></span> <span data-ttu-id="45865-130">Sjá töfluna fyrr í þessu efni fyrir yfirlit yfir heimildir sem þetta hlutverk veitir.</span><span class="sxs-lookup"><span data-stu-id="45865-130">See the table earlier in this topic for an overview of the permissions that this role grants.</span></span>

## <a name="add-or-update-security-groups"></a><span data-ttu-id="45865-131">Bættu við eða uppfærðu öryggishópa</span><span class="sxs-lookup"><span data-stu-id="45865-131">Add or update security groups</span></span>

<span data-ttu-id="45865-132">Eftir að vefsvæðið þitt er búið til eru aðeins notendur sem eru í öryggishópunum sem tengjast hlutverkunum **Kerfisstjóri** og **Stjórnandi** geta nálgast höfundarumhverfi fyrir þá síðu.</span><span class="sxs-lookup"><span data-stu-id="45865-132">After your site is created, only users who are in the security groups that are associated with the **System Administrator** and **Administrator** roles can access the authoring environment for that site.</span></span> <span data-ttu-id="45865-133">Til að tengja notendur við hlutverkin **Vefframleiðandi**, **RnR stjórnandi** og **Lesari** verður þú að úthluta öryggishópum í þessi hlutverk.</span><span class="sxs-lookup"><span data-stu-id="45865-133">To assign users to the **Web Producer**, **RnR Moderator**, and **Reader** roles, you must assign security groups to those roles.</span></span> <span data-ttu-id="45865-134">Fylgdu þessum skrefum til að bæta öryggishópi við hlutverk eða uppfæra öryggishóp sem nú er úthlutað til hlutverks.</span><span class="sxs-lookup"><span data-stu-id="45865-134">To add a security group to a role, or to update a security group that is currently assigned to a role, follow these steps.</span></span>

1. <span data-ttu-id="45865-135">Farðu á svæðið sem á að uppfæra.</span><span class="sxs-lookup"><span data-stu-id="45865-135">Go to the site that you want to update.</span></span>
1. <span data-ttu-id="45865-136">Í **Svæðisstjórnun** opnarðu síðuna **Öryggi**.</span><span class="sxs-lookup"><span data-stu-id="45865-136">In **Site management**, open the **Security** page.</span></span>
1. <span data-ttu-id="45865-137">Veldu hlutverkið sem á að breyta.</span><span class="sxs-lookup"><span data-stu-id="45865-137">Select the role to modify.</span></span>
1. <span data-ttu-id="45865-138">Bættu öryggishópum við hlutverk, eða fjarlægðu öryggishópa úr hlutverkum.</span><span class="sxs-lookup"><span data-stu-id="45865-138">Add security groups to roles, or remove security groups from roles.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="45865-139">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="45865-139">Additional resources</span></span>

[<span data-ttu-id="45865-140">Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar</span><span class="sxs-lookup"><span data-stu-id="45865-140">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="45865-141">Hugsanleg leitarvélabestun (SEO) fyrir vefsvæðið þitt</span><span class="sxs-lookup"><span data-stu-id="45865-141">Search engine optimization (SEO) considerations for your site</span></span>](search-engine-optimization-considerations.md)

[<span data-ttu-id="45865-142">Stjórna öryggisreglu fyrir efni (CSP)</span><span class="sxs-lookup"><span data-stu-id="45865-142">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
