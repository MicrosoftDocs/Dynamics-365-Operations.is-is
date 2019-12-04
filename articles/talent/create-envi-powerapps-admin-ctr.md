---
title: Ekki er hægt að stofna umhverfi í stjórnendamiðstöð Power Apps
description: Þetta efnisatriði útskýrir hvað eigi að gera ef stjórnandi getur ekki stofnað umhverfi í stjórnandamiðstöð Microsoft Power Apps.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5923c59ab5dde13fed0483972e76634031404fd8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773220"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="7ff2e-103">Ekki er hægt að stofna umhverfi í stjórnendamiðstöð Power Apps</span><span class="sxs-lookup"><span data-stu-id="7ff2e-103">Can't create an environment in the Power Apps Admin center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7ff2e-104">**Úthreyfing**</span><span class="sxs-lookup"><span data-stu-id="7ff2e-104">**Issue**</span></span>

- <span data-ttu-id="7ff2e-105">Stjórnandi leigjanda/umhverfis getur ekki stofnað umhverfi í stjórnandamiðstöð Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="7ff2e-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="7ff2e-106">Leyfi sem gefur notendum réttindi til að framkvæma skrefið fyrir stofnun umhverfis, sem hefur ekki verið úthlutað beint á notandann sem framkvæmir skrefið.</span><span class="sxs-lookup"><span data-stu-id="7ff2e-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="7ff2e-107">**Lausn**</span><span class="sxs-lookup"><span data-stu-id="7ff2e-107">**Solution**</span></span>

<span data-ttu-id="7ff2e-108">Gangið úr skugga um að stjórnandi leigjanda hafi úthlutað gildu Power Apps P2-leyfi beint á notandann sem kemur til með að framkvæma skref stofnunar.</span><span class="sxs-lookup"><span data-stu-id="7ff2e-108">Make sure that the tenant admin has assigned a valid Power Apps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="7ff2e-109">Hér eru þjónustuáætlanir Microsoft Dynamics sem veita þessi réttindi.</span><span class="sxs-lookup"><span data-stu-id="7ff2e-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="7ff2e-110">Heildarbirgðahaldseining afurðar (SKU)</span><span class="sxs-lookup"><span data-stu-id="7ff2e-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="7ff2e-111">Power Apps P2 þjónustuáætlun</span><span class="sxs-lookup"><span data-stu-id="7ff2e-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="7ff2e-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="7ff2e-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="7ff2e-113">Power Apps fyrir Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="7ff2e-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="7ff2e-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="7ff2e-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="7ff2e-115">Power Apps fyrir Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="7ff2e-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="7ff2e-116">Athugið að ýmsar birgðahaldseiningar Microsoft Office veita réttindin, ásamt sjálfstæðum birgðahaldseiningum Power Apps Plan 2.</span><span class="sxs-lookup"><span data-stu-id="7ff2e-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="7ff2e-117">Mikilvægt er að hafa í huga að einhver þessara birgðahaldseininga verður að vera til staðar.</span><span class="sxs-lookup"><span data-stu-id="7ff2e-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="7ff2e-118">Opnið [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="7ff2e-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="7ff2e-119">Stofnið umhverfið með því að fylgja leiðbeiningunum í [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="7ff2e-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
