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
ms.openlocfilehash: 54ad5cc8f5f18d57b6713304cceb985acfdc93d1
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055365"
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