---
title: Staða starfs í ráðningarbeiðni
description: Þetta efnisatriði lýsir valmöguleika fyrir stöðu starfs í ráðningarbeiðni fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: 7e59e9381fb15b339095d6a71296813e0141e9ab
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5789733"
---
# <a name="recruiting-request-position-status"></a>Staða starfs í ráðningarbeiðni

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði lýsir valmöguleika fyrir stöðu starfs í ráðningarbeiðni fyrir Dynamics 365 Human Resources.

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