---
title: Kennitala einstaklings
description: Þetta efnisatriði lýsir einingu fyrir kennitölu einstaklings fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: 0991f5b2e17e64e23f78b346c451f7c43bc20378
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067152"
---
# <a name="person-identification-number"></a>Kennitala einstaklings


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði lýsir einingu fyrir kennitölu einstaklings fyrir Dynamics 365 Human Resources.

Raunlægt heiti: mshr_hcmpersonidentificationnumberentity

## <a name="description"></a>lýsing

Þessi eining útskýrir kennitölur umsækjenda. Hún gerir API-notanda kleift að skrifa auðkennisnúmer eins og kennitölur eða númer vegabréfs í færslu umsækjanda. Kennitölurnar koma upp í starfsmannaskránum, en ekki í færslu umsækjanda. Samþættingarforrit getur skrifað gildin í gagnagrunn Human Resources, en númerin sjást ekki í Human Resources fyrr en búið er að stofna starfsmannaskrá umsækjanda.

## <a name="json-representation"></a>JSON-framsetning

```json
{
    "mshr_entrytype": "String",
    "mshr_description": "String",
    "mshr_expirationdate": "Datetime",
    "mshr_isprimary": Int,
    "mshr_identificationnumber": "String",
    "mshr_partynumber": "String",
    "mshr_identificationtypeid": "String",
    "mshr_issuingagencyid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_issuingagency_id_value": "Guid",
    "_mshr_fk_identificationtype_id_value": "Guid",
    "mshr_hcmpersonidentificationnumberentityid": "Guid",
    "mshr_issueddate": "Datetime"
}
```

## <a name="properties"></a>Eiginleikar

| Eiginleiki<br>**Efnislegt heiti**<br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Einingarkenni fyrir kennitölu einstaklings**<br>mshr_hcmpersonidentificationnumberentityid<br>*GUID* | Lesa eingöngu<br>Krafa<br>Myndað af kerfinu | Einkvæmt aðalkenni fyrir kennitölufærslu einstaklings. |
| **Gerð færslu**<br>mshr_entrytype<br>*Strengur* | Lesa-skrifa<br>Valfrjálst | Frjálst gildi til að vísa í gerð færslu fyrir kennitöluna. |
| **Lýsing**<br>mshr_description<br>*Strengur* | Lesa-skrifa<br>Valfrjálst | Lýsing á kennitölunni. |
| **Útrunnið, dags**<br>mshr_expirationdate<br>*Dagsetning og tími* | Lesa-skrifa<br>Valfrjálst | Dagsetningin sem kennitalan eða tengt skjal rennur út. |
| **Er aðal**<br>mshr_isprimary<br>*Safn valkosta mshr_noyes* | Lesa-skrifa<br>Valfrjálst | Skilgreinir hvort kennitalan er aðalfærsla einstaklingsins fyrir þessa gerð auðkennis. |
| **Auðkennisnúmer**<br>mshr_identificationnumber<br>*Strengur* | Lesa-skrifa<br>Krafa | Kennitalan. |
| **Aðilanúmer**<br>mshr_partynumber<br>*Strengur* | Lesa-skrifa<br>Krafa | Kenni aðilans (einstaklingsins) sem á kennitöluna. |
| **Gildi fyrir auðkenni einstaklings**<br>_mshr_fk_person_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Ytri lykill: mshr_dirpersonentityid úr einingu mshr_dirpersonentity | Einkvæmt kenni aðilans (einstaklingsins). |
| **Kenni auðkennisgerðar**<br>mshr_identificationtypeid<br>*Strengur* | Lesa-skrifa<br>Krafa | Gerð auðkennisnúmers. |
| **Gildi fyrir kenni auðkennisgerðar**<br>_mshr_fk_identificationtype_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Ytri lykill: mshr_hcmidentificationtypeentityid úr einingu mshr_hcmidentificationtypeentity | Kerfismyndað einkvæmt kenni auðkennisgerðar. |
| **Kenni útgáfustofnunar**<br>mshr_issuingagencyid<br>*Strengur* | Lesa-skrifa<br>Valfrjálst | Stofnunin eða fyrirtækið sem gaf út auðkennisnúmerið. |
| **Gildi fyrir kenni útgáfustofnunar**<br>_mshr_fk_issuingagency_id_value<br>*GUID* | Lesa eingöngu<br>Valfrjálst<br>Ytri lykill: mshr_hcmissuingagencyentityid úr einingu mshr_hcmissuingagencyentity | Kerfismyndað einkvæmt kenni stofnunar sem gaf út auðkennisnúmerið. |
| **Aðalsvæði**<br>mshr_primaryfield<br>*Strengur* | Lesa eingöngu<br>Krafa | Svæði sem á að nota sem kennimerki einingafærslu. Samsetning aðilanúmers, kennis auðkennisgerðar og auðkennisnúmers. |
| **Útgáfudagur:**<br>mshr_issuedate<br>*Dagsetning* | Lesa-skrifa<br>Valfrjálst | Útgáfudagsetning auðkennisnúmersins. |

## <a name="see-also"></a>Sjá einnig

[Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda](hr-admin-integration-ats-api-introduction.md)<br>
[Dæmi um fyrirspurn fyrir umsækjanda til ráðningar](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
