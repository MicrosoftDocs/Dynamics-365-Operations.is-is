---
title: Eiginleikar sem hafa verið fjarlægðir eða eru úreltir í Dynamics 365 Commerce
description: Þetta efnisatriði lýsir eiginleikum sem hafa verið fjarlægðir eða sem verða fjarlægðir úr Dynamics 365 Commerce.
author: josaw
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: c47c5430a8f5d67e13c95db609a95d5ad66933ae
ms.sourcegitcommit: a8b6cd799eddaf5be9aec9ea3c2b55e2c3231652
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/05/2020
ms.locfileid: "3335277"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a><span data-ttu-id="931d4-103">Eiginleikar sem hafa verið fjarlægðir eða eru úreltir í Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="931d4-103">Removed or deprecated features in Dynamics 365 Commerce</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="931d4-104">Þetta efnisatriði lýsir eiginleikum sem hafa verið fjarlægðir eða sem verða fjarlægðir úr Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="931d4-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Commerce.</span></span>

- <span data-ttu-id="931d4-105">*Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.</span><span class="sxs-lookup"><span data-stu-id="931d4-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="931d4-106">*Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="931d4-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="931d4-107">Þessi listi er ætlað að hjálpa þér að íhuga þessar fjarlægingar og úreldingar fyrir eigin áætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="931d4-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="931d4-108">Ítarlegar upplýsingar um hluti í forritum Finance and Operations má finna í [Tæknilegum tilvísunarskýrslum](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="931d4-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="931d4-109">Hægt er að bera saman mismunandi útgáfur þessara skýrslna til að fá upplýsingar um hluti sem hefur verið breytt eða hafa verið fjarlægðir í hverri útgáfu forrita Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="931d4-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a><span data-ttu-id="931d4-110">Eiginleikar sem eru úreltir eða hafa verið fjarlægðir í Commerce 10.0.10 útgáfu</span><span class="sxs-lookup"><span data-stu-id="931d4-110">Features removed or deprecated in the Commerce 10.0.10 release</span></span>
### <a name="pos-operation-803---picking-and-receiving"></a><span data-ttu-id="931d4-111">POS-aðgerð 803 - Tiltekt og móttaka</span><span class="sxs-lookup"><span data-stu-id="931d4-111">POS operation 803 - Picking and receiving</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="931d4-112">**Ástæða úreldingar/fjarlægingar**</span><span class="sxs-lookup"><span data-stu-id="931d4-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="931d4-113">Tiltektar- og móttökuaðgerðir verða úreltar vegna endurhönnunar.</span><span class="sxs-lookup"><span data-stu-id="931d4-113">Picking and receiving operations is being deprecated due to new operation redesign.</span></span> |
| <span data-ttu-id="931d4-114">**Skipt út fyrir aðra eiginleika?**</span><span class="sxs-lookup"><span data-stu-id="931d4-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="931d4-115">Já.</span><span class="sxs-lookup"><span data-stu-id="931d4-115">Yes.</span></span> <span data-ttu-id="931d4-116">Þeim er skipt út fyrir tvær nýjar sölustaðaaðgerðir: aðgerð á innleið (804) og aðgerð á útleið (805).</span><span class="sxs-lookup"><span data-stu-id="931d4-116">It is replaced by two new POS operations: inbound operation (804) and outbound operation (805).</span></span>|
| <span data-ttu-id="931d4-117">**Afurðasvæði sem haft er áhrif á**</span><span class="sxs-lookup"><span data-stu-id="931d4-117">**Product areas affected**</span></span>         | <span data-ttu-id="931d4-118">Sölustaður (POS) forrit</span><span class="sxs-lookup"><span data-stu-id="931d4-118">Point of sale (POS) application</span></span> |
| <span data-ttu-id="931d4-119">**Dreifingarvalkostur**</span><span class="sxs-lookup"><span data-stu-id="931d4-119">**Deployment option**</span></span>              | <span data-ttu-id="931d4-120">Allir</span><span class="sxs-lookup"><span data-stu-id="931d4-120">All</span></span> |
| <span data-ttu-id="931d4-121">**Staða**</span><span class="sxs-lookup"><span data-stu-id="931d4-121">**Status**</span></span>                         | <span data-ttu-id="931d4-122">Úrelt: Frá og með útgáfu 10.0.10 verða eiginleikar tiltektar-og móttökuaðgerða ekki lengur uppfærðir.</span><span class="sxs-lookup"><span data-stu-id="931d4-122">Deprecated: As of release 10.0.10, the picking and receiving operation will no longer receive any new feature updates.</span></span> <span data-ttu-id="931d4-123">Aðeins alvarlegar villuleiðréttingar verða gerðar fyrir þessa aðgerð í síðari útgáfum.</span><span class="sxs-lookup"><span data-stu-id="931d4-123">Only critical bug fixes will be done for this operation in future releases.</span></span> <span data-ttu-id="931d4-124">Allir viðskiptavinir eru hvattir til að fara í nýja [Aðgerðir á innleið](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) og [Aðgerðir á útleið](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), sem halda áfram að vera hluti af langtímastefnu okkar fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="931d4-124">All customers are encouraged to move to the new [Inbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) and [Outbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), which will continue to be part of our long-term product roadmap.</span></span> |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a><span data-ttu-id="931d4-125">Eiginleikar sem eru úreltir eða hafa verið fjarlægðir í Commerce 10.0.7 útgáfa</span><span class="sxs-lookup"><span data-stu-id="931d4-125">Features removed or deprecated in the Commerce 10.0.7 release</span></span>
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a><span data-ttu-id="931d4-126">Forritaskil Commerce GetProductAvailabilities og GetAvailableInventoryNearby</span><span class="sxs-lookup"><span data-stu-id="931d4-126">Commerce GetProductAvailabilities and GetAvailableInventoryNearby API's</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="931d4-127">**Ástæða úreldingar/fjarlægingar**</span><span class="sxs-lookup"><span data-stu-id="931d4-127">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="931d4-128">Ný forritaskil hafa verið búin til og koma í stað GetProductAvailabilities GetAvailableInventoryNearby.</span><span class="sxs-lookup"><span data-stu-id="931d4-128">New optimized APIs have been created to replace the GetProductAvailabilities and GetAvailableInventoryNearby APIs.</span></span> |
| <span data-ttu-id="931d4-129">**Skipt út fyrir aðra eiginleika?**</span><span class="sxs-lookup"><span data-stu-id="931d4-129">**Replaced by another feature?**</span></span>   | <span data-ttu-id="931d4-130">Já: Þeim er skipt út fyrir forritaskilin GetEstimatedAvailabilty og GetEstimatedProductWarehouseAvailability.</span><span class="sxs-lookup"><span data-stu-id="931d4-130">Yes: It is replaced by GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs.</span></span> |
| <span data-ttu-id="931d4-131">**Afurðasvæði sem haft er áhrif á**</span><span class="sxs-lookup"><span data-stu-id="931d4-131">**Product areas affected**</span></span>         | <span data-ttu-id="931d4-132">SDK-forrit rafrænna viðskipta</span><span class="sxs-lookup"><span data-stu-id="931d4-132">e-Commerce application SDK</span></span> |
| <span data-ttu-id="931d4-133">**Dreifingarvalkostur**</span><span class="sxs-lookup"><span data-stu-id="931d4-133">**Deployment option**</span></span>              | <span data-ttu-id="931d4-134">Allir</span><span class="sxs-lookup"><span data-stu-id="931d4-134">All</span></span> |
| <span data-ttu-id="931d4-135">**Staða**</span><span class="sxs-lookup"><span data-stu-id="931d4-135">**Status**</span></span>                         | <span data-ttu-id="931d4-136">Úrelt: Frá og með útgáfu 10.0.7 verða ekki lengur fjárfest í GetProductAvailabilities og GetAvailableInventoryNearby.</span><span class="sxs-lookup"><span data-stu-id="931d4-136">Deprecated: As of release 10.0.7, there will no longer be engineering investments made for GetProductAvailabilities and GetAvailableInventoryNearby.</span></span> <span data-ttu-id="931d4-137">Fyrirtæki sem nota þessi API í innleiðingu rafrænna viðskipta ættu að skipta yfir í GetEstimatedAvailabilty og GetEstimatedProductWarehouseAvailability API og virkja [Eiginleika fínstillts útreiknings vöruframboðs](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="931d4-137">Organizations that use these APIs in their e-Commerce deployments should convert to the new GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs and enable the [Optimized product availability calculation feature](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span></span>  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="931d4-138">Fyrri tilkynningar um eiginleika sem voru fjarlægðir eða úreltir</span><span class="sxs-lookup"><span data-stu-id="931d4-138">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="931d4-139">Til að læra meira um eiginleika sem hafa verið fjarlægðir eða úreltir í fyrri útgáfum, sjá [Fjarlægir eða úreltir eiginleikar í fyrri útgáfum](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="931d4-139">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span></span>
