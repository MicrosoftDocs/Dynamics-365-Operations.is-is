---
title: Skoðun einstaklings
description: Þetta efnisatriði lýsir einingu einstaklingssíunar fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: 5129348f928fd709a5fabe73917522799a2d47e0
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066294"
---
# <a name="person-screening"></a>Skoðun einstaklings


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði lýsir einingu einstaklingssíunar fyrir Dynamics 365 Human Resources.

Raunlægt heiti: mshr_hcmpersonscreeningentity

## <a name="description"></a>lýsing

Þessi eining lýsir síum sem umsækjandi hefur komist í gegnum eða verður að komast í gegnum til að vera ráðin(n).

## <a name="json-representation"></a>JSON-framsetning

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a>Eiginleikar

| Eiginleiki<br>**Efnislegt heiti**<br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Kenni fyrir einingu einstaklingssíunar**<br>mshr_hcmpersonscreeningentityid<br>*GUID* | Lesa eingöngu<br>Krafa<br>Myndað af kerfinu | Einkvæmt aðalkenni fyrir síunarfærslur einstaklings. |
| **Aðilanúmer**<br>mshr_partynumber<br>*Strengur* | Lesa/skrifa<br>Krafa | Númer aðila (einstaklings) sem tengist umsækjanda. |
| **Gildi fyrir auðkenni einstaklings**<br>_mshr_fk_person_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Framandlykill: mshr_dirpersonentityid of mshr_dirpersonentity | Kerfismynduð kenni fyrir færslueiningu aðila (einstaklings). |
| **Kenni skoðunargerðar**<br>mshr_screeningtypeid<br>*Strengur* | Lesa/skrifa<br>Krafa<br>Ytri lykill: ScreeningType | Kenni síugerðar skilgreint í Human Resources. |
| **Gildi fyrir kenni síugerðar**<br>_mshr_fk_screeningtype_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Framandlykill: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity | Einkvæmt kerfismyndað kenni fyrir færslu síugerðar í tengdri einingu. |
| **Krafa sett fram af**<br>mshr_requiredby<br>*Dagsetning og tími* | Lesa/skrifa<br>Valfrjálst | Dagsetningin sem þarf að klára síunina. |
| **Staða**<br>mshr_status<br>*mshr_hcmcompletionstatus valkostur stilltur*<br>Lesa/skrifa<br>Krafa | Tilgreinir stöðu umsækjanda fyrir síunina. |
| **Lokið þann**<br>mshr_completeddate<br>*Dagsetning og tími* | Lesa/skrifa<br>Valfrjálst | Sagsetning þegarlokið var við skoðun |
| **Athugasemdir**<br>mshr_note<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Athugasemdir sem ráðningarstjórar og ráðningaraðilar nota. |

## <a name="see-also"></a>Sjá einnig

[Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda](hr-admin-integration-ats-api-introduction.md)<br>
[Dæmi um fyrirspurn fyrir umsækjanda til ráðningar](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
