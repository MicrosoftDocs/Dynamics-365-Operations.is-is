---
title: Vörur án birgðastöðu er hægt að skrá út
description: Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar viðskiptavinir geta bætt vörum sem ekki eru til í birgðum við körfuna sína og farið á greiðslusíðuna.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4fa7769044c45faffd9ff61b3de8e6217a5e0354
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018459"
---
# <a name="items-without-inventory-can-be-checked-out"></a>Vörur án birgðastöðu er hægt að skrá út

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar viðskiptavinir geta bætt vörum sem ekki eru til í birgðum við körfuna sína og farið á greiðslusíðuna.

## <a name="description"></a>lýsing

Notendur geta bætt vöru við körfuna sína þótt engar birgðir eru til í versluninni og síðan farið á greiðslusíðuna.

## <a name="resolution"></a>Upplausn

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a>Virkja eiginleikann Sýna villuboðin Ekki til á lager í vefsmið Commerce

Til að virkja eiginleikann **Sýna villuboðin Ekki til á lager** í vefsmið Commerce skal fylgja þessum skrefum.

1. Veljið svæðið sem unnið er á.
1. Í vinstri flettingunni skal velja **Síður**.
1. Veljið **CartPage** til að opna hana.
1. Veljið hólfið **Karfa 1**, veljið **Breyta** og síðan í eiginleikaglugganum skal velja gátreitinn **Sýna villuboðin Ekki til á lager**.
1. Vista og birta síðuna.

## <a name="additional-resources"></a>Frekari upplýsingar

[Nota birgðastillingar](../inventory-settings.md)

[Reikna tiltækar birgðir fyrir smásölurásir](../calculated-inventory-retail-channels.md)

[Skilgreina birgðabiðminni og birgðastöðu](../inventory-buffers-levels.md)
