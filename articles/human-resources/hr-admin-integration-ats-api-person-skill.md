---
title: Hæfni einstaklings
description: Þessi grein lýsir persónukunnáttueiningunni fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: 713fde6d05904f96f7b17721e15805e07159cf78
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891322"
---
# <a name="person-skill"></a>Hæfni einstaklings


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þessi grein lýsir persónukunnáttueiningunni fyrir Dynamics 365 Human Resources.

Raunlægt heiti: mshr_hcmpersonskillentity

## <a name="description"></a>lýsing

Þessi eining lýsir hæfni umsækjanda.

## <a name="json-representation"></a>JSON-framsetning

```json
{
    "mshr_certifier": "String",
    "mshr_partynumber": "String",
    "mshr_levelid": "String",
    "mshr_ratinglevelexaminer": "String",
    "mshr_skillid": "String",
    "mshr_ratingid": "String",
    "mshr_leveltype": Int,
    "mshr_yearsofexperience": Decimal,
    "mshr_verified": Int,
    "mshr_leveldate": "Date",
    "mshr_primaryfield": "String",
    "_mshr_fk_certifier_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratinglevelexaminer_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "mshr_hcmpersonskillentityid": "Guid"
}
```

## <a name="properties"></a>Eiginleikar

| Eiginleiki<br>**Efnislegt heiti**<br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Kenni fyrir einingu hæfni umsækjanda**<br>mshr_hcmpersonskillentityid<br>*GUID* | Lesa eingöngu<br>Krafa | Kerfismyndað einkvæmt kenni fyrir færslueininguna. |
| **Aðilanúmer**<br>mshr_partynumber<br>*Strengur* | Lesa/skrifa<br>Krafa |   Kenni fyrir færslu tengds aðila (einstaklings). |
| **Gildi fyrir auðkenni einstaklings**<br>_mshr_fk_person_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Framandlykill: mshr_dirpersonentityid of mshr_dirpersonentity | Kerfismynduð kenni fyrir færslueiningu aðila (einstaklings). |
| **Vottunaraðili**<br>mshr_certifier<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Starfsmannanúmer starfsmannsins sem vottaði þessa hæfni. |
| **Kennisgildi vottunaraðila**<br>_mshr_fk_certifier_id_value<br>*GUID* | Lesa eingöngu<br>Valfrjálst<br>Framandlykill: mshr_hcmworkerentityid of mshr_hcmworkerentity | Einkvæmt kerfismyndað kenni starfsmannaskráar fyrir starfsmanninn sem vottaði hæfnina. |
| **Hæfniskenni**<br>mshr_skillid<br>*Strengur* | Lesa/skrifa<br>Krafa | Kenni hæfninnar sem er skilgreind í Human Resources. |
| **Gildi fyrir færniskenni**<br>_mshr_fk_skill_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Framandlykill: mshr_hcmskillentityid of mshr_hcmskillentity | Kerfismyndað kenni valinnar hæfni. |
| **Lengd ferils í árum**<br>mshr_yearsofexperience<br>*Tugabrot* | Lesa/skrifa<br>Valfrjálst | Reynsla í árum sem umsækjandi hefur í þessari hæfni. |
| **Einkunnarkenni**<br>mshr_ratingid<br>*Strengur* | Lesa/skrifa<br>Krafa | Gerð matsstigs. Fyrir þessa einingu er gildið **Hæfni**. |
| **Stigsgerð**<br>mshr_leveltype<br>*mshr_hrmskillleveltype valkostur stilltur* | Lesa/skrifa<br>Krafa | Gerð flokkunar fyrir stigið sem úthlutað er á hæfnina. |
| **Stigskenni**<br>mshr_levelid<br>*Strengur* | Lesa/skrifa<br>Krafa | Kenni matsstigs sem umsækjandi hefur fyrir þessa hæfni. |
| **Gildi fyrir kenni einkunnastigs**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Framandlykill: mshr_hcmratinglevelentityid of mshr_hcmratinglevelentity | Kerfismyndað kenni matsstigsins. |
| **Dagsetning stigs**<br>mshr_leveldate<br>*Dagsetning og tími* | Lesa/skrifa<br>Krafa | Dagsetningin þegar umsækjandi var metinn í hæfninni. |
| **Prófdómari matsstigs**<br>mshr_ratinglevelexaminer<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Starfsmannanúmer starfsmannsins sem gaf umsækjanda einkunn. |
| **Gildi fyrir kenni prófdómara matsstigsins**<br>_mshr_fk_ratinglevelexaminer_id_value<br>*GUID* | Lesa eingöngu<br>Valfrjálst<br>Framandlykill: mshr_hcmworkerentityid of mshr_hcmworkerentity | Kerfismyndað kenni starfsmannsins sem skoðaði hæfnisstig umsækjanda. |
| **Staðfest**<br>mshr_verified<br>*mshr_noyes valkostur stilltur* | Lesa/skrifa<br>Krafa | Tilgreinir hvort hæfnistigið hafi verið staðfest. |
| **Aðalsvæði**<br>mshr_primaryfield<br>*Strengur* | Lesa eingöngu<br>Krafa | Svæði sem á að nota sem kennimerki einingafærslu. Samsetning aðilanúmers, stigagerðar, hæfniskennis og dagsetningarstigs |

## <a name="see-also"></a>Sjá einnig

[Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda](hr-admin-integration-ats-api-introduction.md)<br>
[Dæmi um fyrirspurn fyrir umsækjanda til ráðningar](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
