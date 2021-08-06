---
title: Eignir til þjónustu innanhúss
description: Í þessu efnisatriði er lýst hvernig hægt er að nota Microsoft Dynamics 365 Field Service til að þjónusta bæði eignir viðskiptavinar og eigin eignir.
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 9ba92b9bf0e35aa812fc7077d998c8779ebe622e
ms.sourcegitcommit: f65bde9ab0bf4c12a3250e7c9b2abb1555cd7931
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/13/2021
ms.locfileid: "6542344"
---
# <a name="in-house-assets-for-servicing"></a>Eignir til þjónustu innanhúss

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Field Service er hannað til að þjónusta eignir viðskiptavina. Eignastýring fyrir Dynamics 365 Supply Chain Management er hannað til að viðhalda eignum í húsinu. Samþætting þessara tveggja forrita gerir þér kleift að nota Field Service til að þjónusta bæði eignir viðskiptavina og eigin eignir. Þú getur einnig flokkað eignirnar, byggðar á virkri staðsetningu eða stigveldi, og fylgst með þjónustunni á nákvæmu stigi.

Fyrir frekari upplýsingar, sjá [Samþætta Dynamics 365 Field Service og Supply Chain Management](/dynamics365/field-service/supply-chain-field-service-integration).

## <a name="templates"></a>Sniðmát

Eignir í húsi innihalda safn af kjarnatöflukortum sem vinna saman í gagnasamskiptum, eins og sýnt er í eftirfarandi töflu.

| Forrit fyrir Finance and Operations | Forrit viðskiptavinatengsla | lýsing |
|-----------------------------|-----------------------------------|-------------|
[Líftímalíkön eigna í eignastýringu](mapping-reference.md#119) | msdyn_assetlifecyclemodels | |
[Líftímastöður eigna í eignastýringu](mapping-reference.md#120) | msdyn_assetlifecyclestates | |
[Eignagerðir eignastýringar](mapping-reference.md#124) | msdyn_customerassetcategories | |
[Eignir eignastýringar](mapping-reference.md#125) | msdyn_customerassets | |
[Líftímalíkön virkra staðsetninga eignastýringar](mapping-reference.md#134) | msdyn_functionallocationlifecyclemodels | |
[Líftímastöður virkra staðsetninga eignastýringar](mapping-reference.md#135) | msdyn_functionallocationlifecyclestates | |
[Virkar staðsetningagerðir eignastýringar](mapping-reference.md#137) | msdyn_functionallocationtypes | |
[Virkar staðsetningar eignastýringar](mapping-reference.md#136) | msdyn_functionallocations | |
[Framleiðendur eignastýringar](mapping-reference.md#153) | msdyn_manufacturers | |
[Líkön eignastýringar](mapping-reference.md#154) | msdyn_models | |
[Ábyrgð eignastýringar](mapping-reference.md#209) | msdyn_warranties | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
