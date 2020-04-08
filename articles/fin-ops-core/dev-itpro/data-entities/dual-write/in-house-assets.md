---
title: Eignir í húsi til þjónustu
description: Þetta efni lýsir því hvernig þú getur notað Microsoft Dtnamics 365 Field Service til að þjónusta bæði eignir viðskiptavina og eigin eignir.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: d931811e9fbea3c10f83b048a3c3fbeda5396d39
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112460"
---
# <a name="in-house-assets-for-servicing"></a><span data-ttu-id="fe02a-103">Eignir í húsi til þjónustu</span><span class="sxs-lookup"><span data-stu-id="fe02a-103">In-house assets for servicing</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="fe02a-104">Microsoft Dynamics 365 Field Service er hannað til að þjónusta eignir viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="fe02a-104">Microsoft Dynamics 365 Field Service is designed to service customer assets.</span></span> <span data-ttu-id="fe02a-105">Eignastýring fyrir Dynamics 365 Supply Chain Management er hannað til að viðhalda eignum í húsinu.</span><span class="sxs-lookup"><span data-stu-id="fe02a-105">Asset management for Dynamics 365 Supply Chain Management is designed to maintain in-house assets.</span></span> <span data-ttu-id="fe02a-106">Samþætting þessara tveggja forrita gerir þér kleift að nota Field Service til að þjónusta bæði eignir viðskiptavina og eigin eignir.</span><span class="sxs-lookup"><span data-stu-id="fe02a-106">Integration of these two apps lets you use Field Service to service both customer assets and in-house assets.</span></span> <span data-ttu-id="fe02a-107">Þú getur einnig flokkað eignirnar, byggðar á virkri staðsetningu eða stigveldi, og fylgst með þjónustunni á nákvæmu stigi.</span><span class="sxs-lookup"><span data-stu-id="fe02a-107">You can also classify the assets, based on functional location or hierarchy, and track the servicing at a detailed level.</span></span>

<span data-ttu-id="fe02a-108">Fyrir frekari upplýsingar, sjá [Samþætta Dynamics 365 Field Service og Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span><span class="sxs-lookup"><span data-stu-id="fe02a-108">For more information, see [Integrate Dynamics 365 Field Service and Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span></span>

## <a name="templates"></a><span data-ttu-id="fe02a-109">Sniðmát</span><span class="sxs-lookup"><span data-stu-id="fe02a-109">Templates</span></span>

<span data-ttu-id="fe02a-110">Eignir í húsi innihalda safn af grunneiningaspjöldum sem virka saman á meðan samskipti við lánardrottna eru í gangi, eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="fe02a-110">In-house-assets include a collection of core entity maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="fe02a-111">Finance and Operations-smáforrit</span><span class="sxs-lookup"><span data-stu-id="fe02a-111">Finance and Operations apps</span></span> | <span data-ttu-id="fe02a-112">Líkanadrifin forrit í Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="fe02a-112">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="fe02a-113">lýsing</span><span class="sxs-lookup"><span data-stu-id="fe02a-113">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="fe02a-114">Líftímalíkön eigna í eignastýringu</span><span class="sxs-lookup"><span data-stu-id="fe02a-114">Asset management asset lifecycle models</span></span> | <span data-ttu-id="fe02a-115">msdyn\_assetlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="fe02a-115">msdyn\_assetlifecyclemodels</span></span> | |
| <span data-ttu-id="fe02a-116">Líftímastöður eigna í eignastýringu</span><span class="sxs-lookup"><span data-stu-id="fe02a-116">Asset management asset lifecycle states</span></span> | <span data-ttu-id="fe02a-117">msdyn\_assetlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="fe02a-117">msdyn\_assetlifecyclestates</span></span> | |
| <span data-ttu-id="fe02a-118">Eignir eignastýringar</span><span class="sxs-lookup"><span data-stu-id="fe02a-118">Asset management assets</span></span> | <span data-ttu-id="fe02a-119">msdyn\_customerassets</span><span class="sxs-lookup"><span data-stu-id="fe02a-119">msdyn\_customerassets</span></span> | |
| <span data-ttu-id="fe02a-120">Eignagerðir eignastýringar</span><span class="sxs-lookup"><span data-stu-id="fe02a-120">Asset management asset types</span></span> | <span data-ttu-id="fe02a-121">msdyn\_customerassetcategories</span><span class="sxs-lookup"><span data-stu-id="fe02a-121">msdyn\_customerassetcategories</span></span> | |
| <span data-ttu-id="fe02a-122">Líftímalíkön virkra staðsetninga eignastýringar</span><span class="sxs-lookup"><span data-stu-id="fe02a-122">Asset management functional location lifecycle models</span></span> | <span data-ttu-id="fe02a-123">msdyn\_functionallocationlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="fe02a-123">msdyn\_functionallocationlifecyclemodels</span></span> | |
| <span data-ttu-id="fe02a-124">Líftímastöður virkra staðsetninga eignastýringar</span><span class="sxs-lookup"><span data-stu-id="fe02a-124">Asset management functional location lifecycle states</span></span> | <span data-ttu-id="fe02a-125">msdyn\_functionallocationlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="fe02a-125">msdyn\_functionallocationlifecyclestates</span></span> | |
| <span data-ttu-id="fe02a-126">Virkar staðsetningar eignastýringar</span><span class="sxs-lookup"><span data-stu-id="fe02a-126">Asset management functional locations</span></span> | <span data-ttu-id="fe02a-127">msdyn\_functionallocations</span><span class="sxs-lookup"><span data-stu-id="fe02a-127">msdyn\_functionallocations</span></span> | |
| <span data-ttu-id="fe02a-128">Virkar staðsetningagerðir eignastýringar</span><span class="sxs-lookup"><span data-stu-id="fe02a-128">Asset management functional location types</span></span> | <span data-ttu-id="fe02a-129">msdyn\_functionallocationtypes</span><span class="sxs-lookup"><span data-stu-id="fe02a-129">msdyn\_functionallocationtypes</span></span> | |
| <span data-ttu-id="fe02a-130">Framleiðendur eignastýringar</span><span class="sxs-lookup"><span data-stu-id="fe02a-130">Asset management manufacturers</span></span> | <span data-ttu-id="fe02a-131">msdyn\_manufacturers</span><span class="sxs-lookup"><span data-stu-id="fe02a-131">msdyn\_manufacturers</span></span> | |
| <span data-ttu-id="fe02a-132">Líkön eignastýringar</span><span class="sxs-lookup"><span data-stu-id="fe02a-132">Asset management models</span></span> | <span data-ttu-id="fe02a-133">msdyn\_models</span><span class="sxs-lookup"><span data-stu-id="fe02a-133">msdyn\_models</span></span> | |
| <span data-ttu-id="fe02a-134">Ábyrgð eignastýringar</span><span class="sxs-lookup"><span data-stu-id="fe02a-134">Asset management warranty</span></span> | <span data-ttu-id="fe02a-135">msdyn\_warranties</span><span class="sxs-lookup"><span data-stu-id="fe02a-135">msdyn\_warranties</span></span> | |

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [lifecycle models](includes/AssetManagementAssetLifecycleModels-msdyn-assetlifecyclemodels.md)]

[!include [lifecycle states](includes/AssetManagementAssetLifecycleStates-msdyn-assetlifecyclestates.md)]

[!include [assets](includes/AssetManagementAssets-msdyn-customerassets.md)]

[!include [asset types](includes/AssetManagementAssetTypes-msdyn-customerassetcategories.md)]

[!include [functional location lifecycle models](includes/AssetManagementFunctionalLocationLifecycleModels-msdyn-functionallocationlifecyclemodels.md)]

[!include [functional location lifecycle states](includes/AssetManagementFunctionalLocationLifecycleStates-msdyn-functionallocationlifecyclestates.md)]

[!include [functional locations](includes/AssetManagementFunctionalLocations-msdyn-functionallocations.md)]

[!include [functional location types](includes/AssetManagementFunctionalLocationTypes-msdyn-functionallocationtypes.md)]

[!include [manufacturers](includes/AssetManagementManufacturers-msdyn-manufacturers.md)]

[!include [models](includes/AssetManagementModels-msdyn-models.md)]

[!include [warranty](includes/AssetManagementWarranty-msdyn-warranties.md)]