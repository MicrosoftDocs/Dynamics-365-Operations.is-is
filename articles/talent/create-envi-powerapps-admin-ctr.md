---
title: "Ekki hægt að stofna umhverfi í stjórnandamiðstöð PowerApps"
description: "Þetta efnisatriði útskýrir hvað eigi að gera ef stjórnandi getur ekki stofnað umhverfi í stjórnandamiðstöð Microsoft PowerApps."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 6f9b7ceef6895b295e6ae5a50d8ac7970497efe5
ms.contentlocale: is-is
ms.lasthandoff: 12/04/2018

---

# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a><span data-ttu-id="dfc18-103">Ekki hægt að stofna umhverfi í stjórnandamiðstöð PowerApps</span><span class="sxs-lookup"><span data-stu-id="dfc18-103">Can't create an environment in the PowerApps Admin center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dfc18-104">**Úthreyfing**</span><span class="sxs-lookup"><span data-stu-id="dfc18-104">**Issue**</span></span>

- <span data-ttu-id="dfc18-105">Stjórnandi leigjanda/umhverfis getur ekki stofnað umhverfi í stjórnandamiðstöð Microsoft PowerApps.</span><span class="sxs-lookup"><span data-stu-id="dfc18-105">The tenant/environment admin can't create an environment in the Microsoft PowerApps Admin center.</span></span>
- <span data-ttu-id="dfc18-106">Leyfi sem gefur notendum réttindi til að framkvæma skrefið fyrir stofnun umhverfis, sem hefur ekki verið úthlutað beint á notandann sem framkvæmir skrefið.</span><span class="sxs-lookup"><span data-stu-id="dfc18-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="dfc18-107">**Lausn**</span><span class="sxs-lookup"><span data-stu-id="dfc18-107">**Solution**</span></span>

<span data-ttu-id="dfc18-108">Gangið úr skugga um að stjórnandi leigjanda hafi úthlutað gildu PowerApps P2-leyfi beint á notandann sem kemur til með að framkvæma skref stofnunar.</span><span class="sxs-lookup"><span data-stu-id="dfc18-108">Make sure that the tenant admin has assigned a valid PowerApps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="dfc18-109">Hér eru þjónustuáætlanir Microsoft Dynamics sem veita þessi réttindi.</span><span class="sxs-lookup"><span data-stu-id="dfc18-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="dfc18-110">Heildarbirgðahaldseining afurðar (SKU)</span><span class="sxs-lookup"><span data-stu-id="dfc18-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="dfc18-111">Þjónustuáætlun PowerApps P2</span><span class="sxs-lookup"><span data-stu-id="dfc18-111">PowerApps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="dfc18-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="dfc18-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="dfc18-113">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="dfc18-113">PowerApps for Dynamics 365</span></span> |
| <span data-ttu-id="dfc18-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="dfc18-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="dfc18-115">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="dfc18-115">PowerApps for Dynamics 365</span></span> |

<span data-ttu-id="dfc18-116">Athugið að ýmsar birgðahaldseiningar Microsoft Office veita réttindin, ásamt sjálfstæðum birgðahaldseiningum PowerApps Plan 2.</span><span class="sxs-lookup"><span data-stu-id="dfc18-116">Note that various Microsoft Office SKUs also provide the right, together with standalone PowerApps Plan 2 SKUs.</span></span> <span data-ttu-id="dfc18-117">Mikilvægt er að hafa í huga að einhver þessara birgðahaldseininga verður að vera til staðar.</span><span class="sxs-lookup"><span data-stu-id="dfc18-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="dfc18-118">Opnið [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="dfc18-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="dfc18-119">Stofnið umhverfið með því að fylgja leiðbeiningunum í [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="dfc18-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

