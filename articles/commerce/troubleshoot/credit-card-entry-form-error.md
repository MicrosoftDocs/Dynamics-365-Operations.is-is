---
title: Síða fyrir innslátt kreditkorts sýnir villu í greiðsluferlinu
description: Þessi grein veitir leiðbeiningar um bilanaleit sem geta hjálpað þegar hlutinn Greiðslumáti er ekki hlaðinn og sýnir villuboð.
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
ms.openlocfilehash: 6d1f7ba2d1a63430431af94ed4bed3222c85f14d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910444"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a>Síða fyrir innslátt kreditkorts sýnir villu í greiðsluferlinu

[!include [banner](../../includes/banner.md)]

Þessi grein veitir leiðbeiningar um bilanaleit sem geta hjálpað þegar **Greiðslumáti** hluti er ekki hlaðinn og sýnir villuboð.

## <a name="description"></a>lýsing

Þegar greiðsluferlissíða netverslunar er opnuð hleðst hlutinn **Greiðslumáti** ekki og eftirfarandi villuboð koma upp: „Eitthvað fór úrskeiðis. Reyna skal aftur síðar.

![Villa greiðslueiningar.](media/payment-module-error.jpg)

## <a name="resolution"></a>Lausn

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a>Bíða eftir því að skyndiminni Commerce Scale Unit renni út

Stillingar greiðsluþjónustunnar á greiðsluferlissíðu netverslunar eru vistaðar í skyndiminni á Commerce Scale Unit og geta tekið allt að 15 mínútur að birtast á svæði rafrænna viðskipta. Þessar stillingar greiðsluþjónustunnar fela í sér breytingar á reikningskenni söluaðila, API-lykli í skýinu og ýmsar skilgreiningarstillingar sem tengjast greiðslumátanum.

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp netrás](../channel-setup-online.md)
