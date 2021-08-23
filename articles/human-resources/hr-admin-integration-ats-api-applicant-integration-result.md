---
title: Niðurstöður samþættingar umsækjanda
description: Þetta efnisatriði lýsir valkostum fyrir niðurstöðu samþættingar umsækjanda fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: 3f173e15d5524dfd4d63113760760b2534cc8769456df621415a11e4053cc6fb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725915"
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