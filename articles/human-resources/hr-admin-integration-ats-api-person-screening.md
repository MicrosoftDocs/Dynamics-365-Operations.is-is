---
title: Skoðun einstaklings
description: Þessi grein lýsir persónuskimunareiningunni fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: e9b2bbda8f8191f592462f4fbd1902e7274cf7f8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907641"
---
# <a name="person-screening"></a>Skoðun einstaklings


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þessi grein lýsir persónuskimunareiningunni fyrir Dynamics 365 Human Resources.

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
