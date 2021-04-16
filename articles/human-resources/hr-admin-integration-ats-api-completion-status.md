---
title: Staða á lokið
description: Þetta efnisatriði lýsir valkosti lokastöðu fyrir Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f1b0c61ac9d9dc611d2a4700a1a004e3d15b4445
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798370"
---
# <a name="completion-status"></a>Staða á lokið

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði lýsir valkosti lokastöðu fyrir Dynamics 365 Human Resources.

Raunlægt heiti: mshr_hcmcompletionstatus

Þessi tölusetning býður upp á valkost stöðugilda fyrir síun umsækjanda. 

| Virði | Merkimiði | lýsing |
| --- | --- | --- |
| 200000000 | Ekki tilbúið | Umsækjandi hefur ekki enn lokið síun. |
| 200000001 | Staðið | Umsækjandi komst í gegnum síuna. |
| 200000002 | Fella | Umsækjandi komst ekki í gegnum síuna. |

## <a name="see-also"></a>Sjá einnig

[Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda](hr-admin-integration-ats-api-introduction.md)<br>
[Dæmi um fyrirspurn fyrir umsækjanda til ráðningar](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]