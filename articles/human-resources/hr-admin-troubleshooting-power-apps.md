---
title: Ekki er hægt að stofna umhverfi í stjórnendamiðstöð Power Apps
description: Þessi grein útskýrir hvað eigi að gera ef stjórnandi getur ekki stofnað umhverfi í stjórnandamiðstöð Microsoft Power Apps.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 73c8910900ba6486a8e60a547b07ea0c82a6cb10
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053348"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="5616b-103">Ekki er hægt að stofna umhverfi í stjórnendamiðstöð Power Apps</span><span class="sxs-lookup"><span data-stu-id="5616b-103">Can't create an environment in the Power Apps Admin center</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="5616b-104">**Úthreyfing**</span><span class="sxs-lookup"><span data-stu-id="5616b-104">**Issue**</span></span>

- <span data-ttu-id="5616b-105">Stjórnandi leigjanda/umhverfis getur ekki stofnað umhverfi í stjórnandamiðstöð Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="5616b-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="5616b-106">Notandinn er ekki með leyfi sem veitir rétt til að stofna umhverfi.</span><span class="sxs-lookup"><span data-stu-id="5616b-106">The user doesn't have a license that gives the right to create environments.</span></span>

<span data-ttu-id="5616b-107">**Lausn**</span><span class="sxs-lookup"><span data-stu-id="5616b-107">**Solution**</span></span>

<span data-ttu-id="5616b-108">Gangið úr skugga um að stjórnandi leigjanda hafi úthlutað gildu Power Apps P2-leyfi til notanda sem stofnar umhverfið.</span><span class="sxs-lookup"><span data-stu-id="5616b-108">Make sure the tenant admin has assigned a valid Power Apps P2 license to the user creating the environment.</span></span> <span data-ttu-id="5616b-109">Eftirfarandi Microsoft Dynamics þjónustuáætlanir veita heimildir til að stofna umhverfi:</span><span class="sxs-lookup"><span data-stu-id="5616b-109">The following Microsoft Dynamics service plans provide permissions to create environments:</span></span>

| <span data-ttu-id="5616b-110">Heildarbirgðahaldseining</span><span class="sxs-lookup"><span data-stu-id="5616b-110">Overall product stockkeeping unit (SKU)</span></span>       | <span data-ttu-id="5616b-111">Power Apps P2 þjónustuáætlun</span><span class="sxs-lookup"><span data-stu-id="5616b-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="5616b-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="5616b-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="5616b-113">Power Apps fyrir Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="5616b-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="5616b-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="5616b-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="5616b-115">Power Apps fyrir Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="5616b-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="5616b-116">Athugið að ýmsar birgðahaldseiningar Microsoft Office veita réttindin, ásamt sjálfstæðum birgðahaldseiningum Power Apps Plan 2.</span><span class="sxs-lookup"><span data-stu-id="5616b-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="5616b-117">Mikilvægt er að hafa í huga að einhver þessara birgðahaldseininga verður að vera til staðar.</span><span class="sxs-lookup"><span data-stu-id="5616b-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="5616b-118">Opnið [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="5616b-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="5616b-119">Stofnið umhverfið með því að fylgja leiðbeiningunum í [Ráðstafa Human Resources](/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="5616b-119">Create the environments by following the instructions in [Provision Human Resources](/dynamics365/unified-operations/talent/provisioning-talent).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]