---
title: Aðsetur einstaklings
description: Þessi grein lýsir einstaklingsaðfangaeiningunni fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: be5cf649771eaddcb4f2198821530e61b76b2cd2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871017"
---
# <a name="person-address"></a>Aðsetur einstaklings


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þessi grein lýsir einstaklingsaðfangaeiningunni fyrir Dynamics 365 Human Resources.

Raunlægt heiti: mshr_hcmpersonaddressentities

## <a name="description"></a>lýsing

Þessi eining inniheldur lista yfir póstföng fyrir færslur umsækjanda.

## <a name="json-representation"></a>JSON-framsetning

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_roles": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmpersonaddressentityid": "Guid"
}
```

## <a name="properties"></a>Eiginleikar

| Eiginleiki<br>**Efnislegt heiti**<br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Kenni fyrir einingu aðseturs einstaklings**<br>mshr_hcmpersonaddressentityid<br>*Strengur* | Lesa eingöngu<br>Krafa | Kerfismyndað einkvæmt kenni fyrir færslueininguna. |
| **Aðilanúmer**<br>mshr_partynumber<br>*Strengur* | Lesa/skrifa<br>Krafa | Kenni fyrir færslu tengds aðila (einstaklings). |
| **Gildi fyrir auðkenni einstaklings**<br>_mshr_fk_person_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Framandlykill: mshr_dirpersonentityid of mshr_dirpersonentity | Kerfismynduð kenni fyrir færslueiningu aðila (einstaklings). |
| **Staðsetningarkenni**<br>mshr_locationid<br>*Strengur* | Lesa/skrifa<br>Krafa | Staðsetningarkenni aðsetursfærslunnar. Setja upp í einingu mshr_logisticspostaladdresslocationcdsentity. |
| **Lýsing**<br>mshr_description<br>*Strengur* | Lesa/skrifa<br>Krafa | Lýsing á aðsetri umsækjanda. |
| **Hlutverk**<br>mshr_roles<br>*Strengur* | Lesa/skrifa<br>Krafa | Hlutverk sem úthlutað er á þetta aðsetur. Hægt er að úthluta fleiri en einu hlutverki. Hvert hlutverk ætti að vera aðskilið með semíkommu. Gild gildi í einingunni mshr_logisticslocationroleentity. |
| **Gata**<br>mshr_street<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Er götunúmer. |
| **Póststöð**<br>mshr_city<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Borg aðsetursins. Setja upp í einingu mshr_logisticsaddresscityentity. |
| **Ríki**<br>mshr_state<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Ríki fyrir aðsetrið. Setja upp í einingu mshr_logisticsaddressstateentity. |
| **Sýsla**<br>mshr_county<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Sýsla fyrir aðsetrið. Setja upp í einingu mshr_logisticsaddresscountyentity. |
| **Póstnúmer**<br>mshr_zipcode<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Póstnúmer fyrir aðsetrið. Setja upp í einingu mshr_logisticsaddresspostalcodeentity. |
| **Svæðiskenni lands**<br>mshr_countryregionid<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Land eða svæði aðsetursins. |
| **Kennigildi lands/svæðis**<br>_mshr_fk_countriregion_id_value<br>*GUID* | Lesa eingöngu<br>Valfrjálst<br>Framandlykill: mshr_logisticaddresscountryregionentityid of mshr_logisticsaddresscountryregionentity | Kerfismyndað einkvæmt kenni lands/svæðis aðsetursins. |
| **Er aðal**<br>mshr_isprimary<br>*mshr_noyes valkostur stilltur* | Lesa/skrifa<br>Krafa | Segir til um hvort þetta aðsetur er aðalaðsetur einstaklings fyrir skilgreinda hlutverkið. |
| **Er einka**<br>mshr_isprivate<br>*mshr_noyes valkostur stilltur* | Lesa/skrifa<br>Krafa | Segir til um hvort þetta aðsetur er einkaaðsetur einstaklingsins. |
| **Aðalsvæði**<br>mshr_primaryfield<br>*Strengur* | Lesa eingöngu<br>Krafa | Svæði notað sem aðalkennimerki einingafærslu. Samsetning aðilanúmers og staðsetningarkennis. |

## <a name="see-also"></a>Sjá einnig

[Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda](hr-admin-integration-ats-api-introduction.md)<br>
[Dæmi um fyrirspurn fyrir umsækjanda til ráðningar](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
