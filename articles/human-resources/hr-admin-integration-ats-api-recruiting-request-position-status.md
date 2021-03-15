---
title: Staða starfs í ráðningarbeiðni
description: Þetta efnisatriði lýsir valmöguleika fyrir stöðu starfs í ráðningarbeiðni fyrir Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3f7bae64f58f0bdc1603b3c1b5493f1ebcfa8de9
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126051"
---
# <a name="recruiting-request-position-status"></a>Staða starfs í ráðningarbeiðni

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