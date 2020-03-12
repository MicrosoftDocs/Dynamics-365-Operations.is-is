---
title: Fjarlægðir eða úreltir eiginleikar verkvangs
description: Þetta efnisatriði lýsir eiginleikum sem hafa verið fjarlægðir eða sem verða fjarlægðir í verkvangsuppfærslum á forritum Finance and Operations.
author: sericks007
manager: AnnBe
ms.date: 02/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 66e1420c7053c0df9f42b15c55aba1a8c869f02a
ms.sourcegitcommit: 2cc3b89efdd90f8d80883b7a271d7885282ba3e8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087884"
---
# <a name="removed-or-deprecated-platform-features"></a><span data-ttu-id="55e6c-103">Fjarlægðir eða úreltir eiginleikar verkvangs</span><span class="sxs-lookup"><span data-stu-id="55e6c-103">Removed or deprecated platform features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="55e6c-104">Þetta efnisatriði lýsir eiginleikum sem hafa verið fjarlægðir eða sem verða fjarlægðir í verkvangsuppfærslum á forritum Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="55e6c-104">This topic describes features that have been removed, or that are planned for removal in platform updates of Finance and Operations apps.</span></span>

- <span data-ttu-id="55e6c-105">*Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.</span><span class="sxs-lookup"><span data-stu-id="55e6c-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="55e6c-106">*Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="55e6c-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="55e6c-107">Þessi listi er ætlað að hjálpa þér að íhuga þessar fjarlægingar og úreldingar fyrir eigin áætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="55e6c-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="55e6c-108">Ítarlegar upplýsingar um hluti í forritum Finance and Operations má finna í [Tæknilegum tilvísunarskýrslum](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="55e6c-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="55e6c-109">Hægt er að bera saman mismunandi útgáfur þessara skýrslna til að fá upplýsingar um hluti sem hefur verið breytt eða hafa verið fjarlægðir í hverri útgáfu forrita Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="55e6c-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="55e6c-110">Update 32 fyrir verkvang</span><span class="sxs-lookup"><span data-stu-id="55e6c-110">Platform update 32</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="55e6c-111">Gluggi fyrir breytingu á verkflæðisbeiðni inniheldur ekki lengur fellivalmynd fyrir val á notendum</span><span class="sxs-lookup"><span data-stu-id="55e6c-111">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="55e6c-112">**Ástæða úreldingar/fjarlægingar**</span><span class="sxs-lookup"><span data-stu-id="55e6c-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="55e6c-113">Þetta var öryggisatriði vegna þess að beiðni um breytingar var hægt að senda í ógáti til notanda.</span><span class="sxs-lookup"><span data-stu-id="55e6c-113">This was a security issue because the request for change could be sent to an unintended user.</span></span> <span data-ttu-id="55e6c-114">Þetta var einnig nothæfismál vegna þess að það neyddi notandann til að ákvarða hver upphafsmaður verkflæðisins var og velja þá handvirkt.</span><span class="sxs-lookup"><span data-stu-id="55e6c-114">This was also a usability issue because it forced the user to determine who the workflow originator was and manually select them.</span></span>  |
| <span data-ttu-id="55e6c-115">**Skipt út fyrir aðra eiginleika?**</span><span class="sxs-lookup"><span data-stu-id="55e6c-115">**Replaced by another feature?**</span></span>   | <span data-ttu-id="55e6c-116">Nr</span><span class="sxs-lookup"><span data-stu-id="55e6c-116">No</span></span> |
| <span data-ttu-id="55e6c-117">**Afurðasvæði sem haft er áhrif á**</span><span class="sxs-lookup"><span data-stu-id="55e6c-117">**Product areas affected**</span></span>         | <span data-ttu-id="55e6c-118">Verkflæði</span><span class="sxs-lookup"><span data-stu-id="55e6c-118">Workflow</span></span> |
| <span data-ttu-id="55e6c-119">**Dreifingarvalkostur**</span><span class="sxs-lookup"><span data-stu-id="55e6c-119">**Deployment option**</span></span>              | <span data-ttu-id="55e6c-120">Öll</span><span class="sxs-lookup"><span data-stu-id="55e6c-120">All</span></span> |
| <span data-ttu-id="55e6c-121">**Staða**</span><span class="sxs-lookup"><span data-stu-id="55e6c-121">**Status**</span></span>                         | <span data-ttu-id="55e6c-122">Listi notendavalsins var fjarlægður úr valmyndinni um breytingu á beiðni í uppfærslu á verkvangi 32.</span><span class="sxs-lookup"><span data-stu-id="55e6c-122">The user selection drop-down list was removed from the request change dialog box in Platform update 32.</span></span> <span data-ttu-id="55e6c-123">Beiðnir um breytingu verða sjálfkrafa sendar til höfundar eins og til er ætlast.</span><span class="sxs-lookup"><span data-stu-id="55e6c-123">Request change requests will be automatically sent to the originator as intended.</span></span> <span data-ttu-id="55e6c-124">Fyrir frekari upplýsingar um þessa virkni, sjá [Verkþættir í samþykktarferli verkflæðis](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span><span class="sxs-lookup"><span data-stu-id="55e6c-124">For more information about this functionality, see [Actions in workflow approval processes](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="55e6c-125">Fyrri tilkynningar um eiginleika sem voru fjarlægðir eða úreltir</span><span class="sxs-lookup"><span data-stu-id="55e6c-125">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="55e6c-126">Til að læra meira um eiginleika sem hafa verið fjarlægðir eða úreltir í fyrri útgáfum, sjá [Fjarlægir eða úreltir eiginleikar í fyrri útgáfum](../migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="55e6c-126">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../migration-upgrade/deprecated-features.md).</span></span>

