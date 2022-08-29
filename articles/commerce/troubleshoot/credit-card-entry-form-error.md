---
title: Síða fyrir innslátt kreditkorts sýnir villu í greiðsluferlinu
description: Þessi grein veitir leiðbeiningar um bilanaleit sem geta hjálpað þegar hlutinn Greiðslumáti er ekki hlaðinn og sýnir villuboð.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 25f0dde83efff7c1d9a2a456270f5d48047f44ba
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269756"
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
