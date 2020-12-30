---
title: Ekki er hægt að stofna umhverfi í stjórnendamiðstöð Power Apps
description: Þessi grein útskýrir hvað eigi að gera ef stjórnandi getur ekki stofnað umhverfi í stjórnandamiðstöð Microsoft Power Apps.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 68e6dbcbbc9811211570e968047f5faa8a2c8bd0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419001"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="ef9bd-103">Ekki er hægt að stofna umhverfi í stjórnendamiðstöð Power Apps</span><span class="sxs-lookup"><span data-stu-id="ef9bd-103">Can't create an environment in the Power Apps Admin center</span></span>

<span data-ttu-id="ef9bd-104">**Úthreyfing**</span><span class="sxs-lookup"><span data-stu-id="ef9bd-104">**Issue**</span></span>

- <span data-ttu-id="ef9bd-105">Stjórnandi leigjanda/umhverfis getur ekki stofnað umhverfi í stjórnandamiðstöð Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="ef9bd-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="ef9bd-106">Leyfi sem gefur notendum réttindi til að framkvæma skrefið fyrir stofnun umhverfis, sem hefur ekki verið úthlutað beint á notandann sem framkvæmir skrefið.</span><span class="sxs-lookup"><span data-stu-id="ef9bd-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="ef9bd-107">**Lausn**</span><span class="sxs-lookup"><span data-stu-id="ef9bd-107">**Solution**</span></span>

<span data-ttu-id="ef9bd-108">Gangið úr skugga um að stjórnandi leigjanda hafi úthlutað gildu Power Apps P2-leyfi beint á notandann sem kemur til með að framkvæma skref stofnunar.</span><span class="sxs-lookup"><span data-stu-id="ef9bd-108">Make sure that the tenant admin has assigned a valid Power Apps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="ef9bd-109">Hér eru þjónustuáætlanir Microsoft Dynamics sem veita þessi réttindi.</span><span class="sxs-lookup"><span data-stu-id="ef9bd-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="ef9bd-110">Heildarbirgðahaldseining afurðar (SKU)</span><span class="sxs-lookup"><span data-stu-id="ef9bd-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="ef9bd-111">Power Apps P2 þjónustuáætlun</span><span class="sxs-lookup"><span data-stu-id="ef9bd-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="ef9bd-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="ef9bd-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="ef9bd-113">Power Apps fyrir Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="ef9bd-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="ef9bd-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="ef9bd-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="ef9bd-115">Power Apps fyrir Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="ef9bd-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="ef9bd-116">Athugið að ýmsar birgðahaldseiningar Microsoft Office veita réttindin, ásamt sjálfstæðum birgðahaldseiningum Power Apps Plan 2.</span><span class="sxs-lookup"><span data-stu-id="ef9bd-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="ef9bd-117">Mikilvægt er að hafa í huga að einhver þessara birgðahaldseininga verður að vera til staðar.</span><span class="sxs-lookup"><span data-stu-id="ef9bd-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="ef9bd-118">Opnið [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="ef9bd-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="ef9bd-119">Stofnið umhverfið með því að fylgja leiðbeiningunum í [Ráðstafa Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="ef9bd-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
