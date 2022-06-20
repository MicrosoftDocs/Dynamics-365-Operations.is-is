---
title: Staða starfs í ráðningarbeiðni
description: Þessi grein lýsir stöðuvalkosti ráðningarbeiðni sem stilltur er fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: 736bdbfb8759ab61202d1f17e3cdc8294be0ba84
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846415"
---
# <a name="recruiting-request-position-status"></a>Staða starfs í ráðningarbeiðni


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þessi grein lýsir stöðuvalkosti ráðningarbeiðni sem stilltur er fyrir Dynamics 365 Human Resources.

Raunlægt heiti: mshr_hcmrecruitingrequestpositionstatus

Þessi upptalning býður upp á valmöguleika fyrir stöðugildi fyrir hverja stöðu í ráðningarbeiðni í einingunni RecruitingRequestPosition.

| Virði | Merkimiði | lýsing |
| --- | --- | --- |
| 200000000 | Opnar | Staðan í ráðningarbeiðninni er opin fyrir ráðningu. Þetta gefur ekki til kynna að engin virk stöðuúthlutun er í gangi fyrir stöðuna. Það kann að vera að starfsmaður sé í stöðunni á ráðningartímanum. Það gefur aðeins til kynna að staðan er tiltækt fyrir ráðningu í samhengi ráðningarbeiðninnar. |
| 200000001 | Útfyllt | Starfskraftur hefur verið valinn fyrir úthlutun á stöðuna. |
| 200000002 | Hætt við | Hætt hefur verið við beiðni um ráðningu fyrir þessa stöðu. |

## <a name="see-also"></a>Sjá einnig

[Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda](hr-admin-integration-ats-api-introduction.md)<br>
[Dæmi um fyrirspurn fyrir ráðningarbeiðni](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
