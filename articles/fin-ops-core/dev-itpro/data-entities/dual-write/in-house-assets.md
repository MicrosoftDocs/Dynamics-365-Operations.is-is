---
title: Eignir í húsi til þjónustu
description: Þetta efni lýsir því hvernig þú getur notað Microsoft Dtnamics 365 Field Service til að þjónusta bæði eignir viðskiptavina og eigin eignir.
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 040f9d26a137ebce1edc6adf28ff226b3a81e1ae
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748594"
---
# <a name="in-house-assets-for-servicing"></a><span data-ttu-id="bd32c-103">Eignir til þjónustu innanhúss</span><span class="sxs-lookup"><span data-stu-id="bd32c-103">In-house assets for servicing</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="bd32c-104">Microsoft Dynamics 365 Field Service er hannað til að þjónusta eignir viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="bd32c-104">Microsoft Dynamics 365 Field Service is designed to service customer assets.</span></span> <span data-ttu-id="bd32c-105">Eignastýring fyrir Dynamics 365 Supply Chain Management er hannað til að viðhalda eignum í húsinu.</span><span class="sxs-lookup"><span data-stu-id="bd32c-105">Asset management for Dynamics 365 Supply Chain Management is designed to maintain in-house assets.</span></span> <span data-ttu-id="bd32c-106">Samþætting þessara tveggja forrita gerir þér kleift að nota Field Service til að þjónusta bæði eignir viðskiptavina og eigin eignir.</span><span class="sxs-lookup"><span data-stu-id="bd32c-106">Integration of these two apps lets you use Field Service to service both customer assets and in-house assets.</span></span> <span data-ttu-id="bd32c-107">Þú getur einnig flokkað eignirnar, byggðar á virkri staðsetningu eða stigveldi, og fylgst með þjónustunni á nákvæmu stigi.</span><span class="sxs-lookup"><span data-stu-id="bd32c-107">You can also classify the assets, based on functional location or hierarchy, and track the servicing at a detailed level.</span></span>

<span data-ttu-id="bd32c-108">Fyrir frekari upplýsingar, sjá [Samþætta Dynamics 365 Field Service og Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span><span class="sxs-lookup"><span data-stu-id="bd32c-108">For more information, see [Integrate Dynamics 365 Field Service and Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span></span>

## <a name="templates"></a><span data-ttu-id="bd32c-109">Sniðmát</span><span class="sxs-lookup"><span data-stu-id="bd32c-109">Templates</span></span>

<span data-ttu-id="bd32c-110">Eignir í húsi innihalda safn af kjarnatöflukortum sem vinna saman í gagnasamskiptum, eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="bd32c-110">In-house-assets include a collection of core table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="bd32c-111">Finance and Operations-smáforrit</span><span class="sxs-lookup"><span data-stu-id="bd32c-111">Finance and Operations apps</span></span> | <span data-ttu-id="bd32c-112">Líkanadrifin forrit í Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="bd32c-112">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="bd32c-113">lýsing</span><span class="sxs-lookup"><span data-stu-id="bd32c-113">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="bd32c-114">Líftímalíkön eigna í eignastýringu</span><span class="sxs-lookup"><span data-stu-id="bd32c-114">Asset management asset lifecycle models</span></span> | <span data-ttu-id="bd32c-115">msdyn\_assetlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="bd32c-115">msdyn\_assetlifecyclemodels</span></span> | |
| <span data-ttu-id="bd32c-116">Líftímastöður eigna í eignastýringu</span><span class="sxs-lookup"><span data-stu-id="bd32c-116">Asset management asset lifecycle states</span></span> | <span data-ttu-id="bd32c-117">msdyn\_assetlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="bd32c-117">msdyn\_assetlifecyclestates</span></span> | |
| <span data-ttu-id="bd32c-118">Eignir eignastýringar</span><span class="sxs-lookup"><span data-stu-id="bd32c-118">Asset management assets</span></span> | <span data-ttu-id="bd32c-119">msdyn\_customerassets</span><span class="sxs-lookup"><span data-stu-id="bd32c-119">msdyn\_customerassets</span></span> | |
| <span data-ttu-id="bd32c-120">Eignagerðir eignastýringar</span><span class="sxs-lookup"><span data-stu-id="bd32c-120">Asset management asset types</span></span> | <span data-ttu-id="bd32c-121">msdyn\_customerassetcategories</span><span class="sxs-lookup"><span data-stu-id="bd32c-121">msdyn\_customerassetcategories</span></span> | |
| <span data-ttu-id="bd32c-122">Líftímalíkön virkra staðsetninga eignastýringar</span><span class="sxs-lookup"><span data-stu-id="bd32c-122">Asset management functional location lifecycle models</span></span> | <span data-ttu-id="bd32c-123">msdyn\_functionallocationlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="bd32c-123">msdyn\_functionallocationlifecyclemodels</span></span> | |
| <span data-ttu-id="bd32c-124">Líftímastöður virkra staðsetninga eignastýringar</span><span class="sxs-lookup"><span data-stu-id="bd32c-124">Asset management functional location lifecycle states</span></span> | <span data-ttu-id="bd32c-125">msdyn\_functionallocationlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="bd32c-125">msdyn\_functionallocationlifecyclestates</span></span> | |
| <span data-ttu-id="bd32c-126">Virkar staðsetningar eignastýringar</span><span class="sxs-lookup"><span data-stu-id="bd32c-126">Asset management functional locations</span></span> | <span data-ttu-id="bd32c-127">msdyn\_functionallocations</span><span class="sxs-lookup"><span data-stu-id="bd32c-127">msdyn\_functionallocations</span></span> | |
| <span data-ttu-id="bd32c-128">Virkar staðsetningagerðir eignastýringar</span><span class="sxs-lookup"><span data-stu-id="bd32c-128">Asset management functional location types</span></span> | <span data-ttu-id="bd32c-129">msdyn\_functionallocationtypes</span><span class="sxs-lookup"><span data-stu-id="bd32c-129">msdyn\_functionallocationtypes</span></span> | |
| <span data-ttu-id="bd32c-130">Framleiðendur eignastýringar</span><span class="sxs-lookup"><span data-stu-id="bd32c-130">Asset management manufacturers</span></span> | <span data-ttu-id="bd32c-131">msdyn\_manufacturers</span><span class="sxs-lookup"><span data-stu-id="bd32c-131">msdyn\_manufacturers</span></span> | |
| <span data-ttu-id="bd32c-132">Líkön eignastýringar</span><span class="sxs-lookup"><span data-stu-id="bd32c-132">Asset management models</span></span> | <span data-ttu-id="bd32c-133">msdyn\_models</span><span class="sxs-lookup"><span data-stu-id="bd32c-133">msdyn\_models</span></span> | |
| <span data-ttu-id="bd32c-134">Ábyrgð eignastýringar</span><span class="sxs-lookup"><span data-stu-id="bd32c-134">Asset management warranty</span></span> | <span data-ttu-id="bd32c-135">msdyn\_warranties</span><span class="sxs-lookup"><span data-stu-id="bd32c-135">msdyn\_warranties</span></span> | |

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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]