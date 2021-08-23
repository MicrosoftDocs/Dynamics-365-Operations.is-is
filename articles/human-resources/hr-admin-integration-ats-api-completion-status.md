---
title: Staða á lokið
description: Þetta efnisatriði lýsir valkosti lokastöðu fyrir Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 67e464262897d89f80bd615156d56cc12a822dd4a0dfa6d5eb206c38ddd61ec5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732874"
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