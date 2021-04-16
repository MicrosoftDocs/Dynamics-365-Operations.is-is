---
title: Niðurstöður samþættingar umsækjanda
description: Þetta efnisatriði lýsir valkostum fyrir niðurstöðu samþættingar umsækjanda fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: e8e41fe485cc70a668d4610ce6eabba5cd16ac86
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795118"
---
# <a name="applicant-integration-result"></a>Niðurstöður samþættingar umsækjanda

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði lýsir valkostum fyrir niðurstöðu samþættingar umsækjanda fyrir Dynamics 365 Human Resources.

Raunlægt heiti: mshr_hcmapplicantintegrationresult

Þessi tölusetning býður upp á stöðu fyrir færslu umsækjanda.

| Virði | Merkimiði | lýsing |
| --- | --- | --- |
| 200000000 | Ekki farið í ferli | Umsækjandi kemur enn til greina. |
| 200000001 | Ráðin(n) | Umsækjandi hefur verið ráðinn. |
| 200000002 | Ekki ráðnir | Ákvörðun var tekin um að ráða ekki umsækjanda. |
| 200000003 | Hunsað | Umsækjandi kemur ekki lengur til greina. |

## <a name="see-also"></a>Sjá einnig

[Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda](hr-admin-integration-ats-api-introduction.md)<br>
[Dæmi um fyrirspurn fyrir umsækjanda til ráðningar](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]