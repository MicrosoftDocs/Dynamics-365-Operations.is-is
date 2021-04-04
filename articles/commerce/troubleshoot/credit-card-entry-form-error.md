---
title: Síða fyrir innslátt kreditkorts sýnir villu í greiðsluferlinu
description: Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar greiðslumátahlutinn hleðst ekki og hann sýnir villuboð.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: f0751fc76e6eb4320f766886b4c1efcb1042e996
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585370"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a>Síða fyrir innslátt kreditkorts sýnir villu í greiðsluferlinu

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur reynst hjálpleg þegar hlutinn **Greiðslumáti** hleðst ekki og hann sýnir villuboð.

## <a name="description"></a>lýsing

Þegar greiðsluferlissíða netverslunar er opnuð hleðst hlutinn **Greiðslumáti** ekki og eftirfarandi villuboð koma upp: „Eitthvað fór úrskeiðis. Reyna skal aftur síðar.

![Villa greiðslueiningar](media/payment-module-error.jpg)

## <a name="resolution"></a>Upplausn

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a>Bíða eftir því að skyndiminni Commerce Scale Unit renni út

Stillingar greiðsluþjónustunnar á greiðsluferlissíðu netverslunar eru vistaðar í skyndiminni á Commerce Scale Unit og geta tekið allt að 15 mínútur að birtast á svæði rafrænna viðskipta. Þessar stillingar greiðsluþjónustunnar fela í sér breytingar á reikningskenni söluaðila, API-lykli í skýinu og ýmsar skilgreiningarstillingar sem tengjast greiðslumátanum.

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp netrás](../channel-setup-online.md)
