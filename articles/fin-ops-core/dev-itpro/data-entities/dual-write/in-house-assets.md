---
title: Eignir til þjónustu innanhúss
description: Þessi grein lýsir því hvernig þú getur notað Microsoft Dynamics 365 Field Service að þjónusta bæði eignir viðskiptavina og eignir innanhúss.
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: b3e741c85fcad2abc18879280ef7332ae091c984
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289251"
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
