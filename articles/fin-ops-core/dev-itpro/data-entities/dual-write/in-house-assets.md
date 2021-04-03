---
title: Eignir í húsi til þjónustu
description: Þetta efni lýsir því hvernig þú getur notað Microsoft Dtnamics 365 Field Service til að þjónusta bæði eignir viðskiptavina og eigin eignir.
author: RamaKrishnamoorthy
manager: AnnBe
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
ms.openlocfilehash: d4d681b2362c90b69007ea44c01c886f96cc1db1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568079"
---
# <a name="in-house-assets-for-servicing"></a>Eignir til þjónustu innanhúss

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Field Service er hannað til að þjónusta eignir viðskiptavina. Eignastýring fyrir Dynamics 365 Supply Chain Management er hannað til að viðhalda eignum í húsinu. Samþætting þessara tveggja forrita gerir þér kleift að nota Field Service til að þjónusta bæði eignir viðskiptavina og eigin eignir. Þú getur einnig flokkað eignirnar, byggðar á virkri staðsetningu eða stigveldi, og fylgst með þjónustunni á nákvæmu stigi.

Fyrir frekari upplýsingar, sjá [Samþætta Dynamics 365 Field Service og Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).

## <a name="templates"></a>Sniðmát

Eignir í húsi innihalda safn af kjarnatöflukortum sem vinna saman í gagnasamskiptum, eins og sýnt er í eftirfarandi töflu.

| Finance and Operations-smáforrit | Líkanadrifin forrit í Dynamics 365 | lýsing |
|-----------------------------|-----------------------------------|-------------|
| Líftímalíkön eigna í eignastýringu | msdyn\_assetlifecyclemodels | |
| Líftímastöður eigna í eignastýringu | msdyn\_assetlifecyclestates | |
| Eignir eignastýringar | msdyn\_customerassets | |
| Eignagerðir eignastýringar | msdyn\_customerassetcategories | |
| Líftímalíkön virkra staðsetninga eignastýringar | msdyn\_functionallocationlifecyclemodels | |
| Líftímastöður virkra staðsetninga eignastýringar | msdyn\_functionallocationlifecyclestates | |
| Virkar staðsetningar eignastýringar | msdyn\_functionallocations | |
| Virkar staðsetningagerðir eignastýringar | msdyn\_functionallocationtypes | |
| Framleiðendur eignastýringar | msdyn\_manufacturers | |
| Líkön eignastýringar | msdyn\_models | |
| Ábyrgð eignastýringar | msdyn\_warranties | |

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