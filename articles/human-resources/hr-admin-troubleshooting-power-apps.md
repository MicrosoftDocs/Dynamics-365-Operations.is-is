---
title: Ekki er hægt að stofna umhverfi í stjórnendamiðstöð Power Apps
description: Þessi grein útskýrir hvað eigi að gera ef stjórnandi getur ekki stofnað umhverfi í stjórnandamiðstöð Microsoft Power Apps.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 664c644c9b34e3489b4134040e165d26202dbd38
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112965"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="50cf7-103">Ekki er hægt að stofna umhverfi í stjórnendamiðstöð Power Apps</span><span class="sxs-lookup"><span data-stu-id="50cf7-103">Can't create an environment in the Power Apps Admin center</span></span>

<span data-ttu-id="50cf7-104">**Úthreyfing**</span><span class="sxs-lookup"><span data-stu-id="50cf7-104">**Issue**</span></span>

- <span data-ttu-id="50cf7-105">Stjórnandi leigjanda/umhverfis getur ekki stofnað umhverfi í stjórnandamiðstöð Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="50cf7-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="50cf7-106">Notandinn er ekki með leyfi sem veitir rétt til að stofna umhverfi.</span><span class="sxs-lookup"><span data-stu-id="50cf7-106">The user doesn't have a license that gives the right to create environments.</span></span>

<span data-ttu-id="50cf7-107">**Lausn**</span><span class="sxs-lookup"><span data-stu-id="50cf7-107">**Solution**</span></span>

<span data-ttu-id="50cf7-108">Gangið úr skugga um að stjórnandi leigjanda hafi úthlutað gildu Power Apps P2-leyfi til notanda sem stofnar umhverfið.</span><span class="sxs-lookup"><span data-stu-id="50cf7-108">Make sure the tenant admin has assigned a valid Power Apps P2 license to the user creating the environment.</span></span> <span data-ttu-id="50cf7-109">Eftirfarandi Microsoft Dynamics þjónustuáætlanir veita heimildir til að stofna umhverfi:</span><span class="sxs-lookup"><span data-stu-id="50cf7-109">The following Microsoft Dynamics service plans provide permissions to create environments:</span></span>

| <span data-ttu-id="50cf7-110">Heildarbirgðahaldseining</span><span class="sxs-lookup"><span data-stu-id="50cf7-110">Overall product stockkeeping unit (SKU)</span></span>       | <span data-ttu-id="50cf7-111">Power Apps P2 þjónustuáætlun</span><span class="sxs-lookup"><span data-stu-id="50cf7-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="50cf7-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="50cf7-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="50cf7-113">Power Apps fyrir Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="50cf7-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="50cf7-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="50cf7-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="50cf7-115">Power Apps fyrir Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="50cf7-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="50cf7-116">Athugið að ýmsar birgðahaldseiningar Microsoft Office veita réttindin, ásamt sjálfstæðum birgðahaldseiningum Power Apps Plan 2.</span><span class="sxs-lookup"><span data-stu-id="50cf7-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="50cf7-117">Mikilvægt er að hafa í huga að einhver þessara birgðahaldseininga verður að vera til staðar.</span><span class="sxs-lookup"><span data-stu-id="50cf7-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="50cf7-118">Opnið [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="50cf7-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="50cf7-119">Stofnið umhverfið með því að fylgja leiðbeiningunum í [Ráðstafa Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="50cf7-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
