---
title: Tengiliður aðila
description: Þessi grein lýsir tengiliðaeiningu aðila fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: f10bb89757419bcb29bfa5a4f44d30a38f41dfb0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909876"
---
# <a name="party-contact"></a>Tengiliður aðila


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þessi grein lýsir tengiliðaeiningu aðila fyrir Dynamics 365 Human Resources.

Raunlægt heiti: mshr_dirpartycontactentities

## <a name="description"></a>lýsing

Þessi eining lýsir samskiptaupplýsingum umsækjanda, þ.á.m. síma, tölvupósti og reikningum á samfélagsmiðlum.

## <a name="json-representation"></a>JSON-framsetning

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_type": Int,
    "mshr_countryregioncode": "String",
    "mshr_locator": "String",
    "mshr_locatorextension": "String",
    "mshr_purpose": "String",
    "mshr_ismobilephone": Int,
    "mshr_isinstantmessage": Int,
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "String",
    "mshr_dirpartycontactentityid": "String"
}
```

## <a name="properties"></a>Eiginleikar

| Eiginleiki<br>**Efnislegt heiti**<br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Kenni einingar fyrir tengil aðila**<br>mshr_dirpartycontactentityid<br>*Strengur* | Lesa eingöngu<br>Krafa | Kerfismyndað einkvæmt kenni fyrir færslueininguna. |
| **Aðilanúmer**<br>mshr_partynumber<br>*Strengur* | Lesa/skrifa<br>Krafa | Kenni fyrir færslu tengds aðila (einstaklings). |
| **Gildi fyrir auðkenni einstaklings**<br>_mshr_fk_person_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Framandlykill: mshr_dirpersonentityid of mshr_dirpersonentity | Kerfismynduð kenni fyrir færslueiningu aðila (einstaklings). |
| **Staðsetningarkenni**<br>mshr_locationid<br>*Strengur* | Lesa/skrifa<br>Krafa | Staðsetningarkenni aðsetursfærslunnar. Setja upp í einingu mshr_logisticspostaladdresslocationcdsentity. |
| **Lýsing**<br>mshr_description<br>*Strengur* | Lesa/skrifa<br>Krafa | Lýsing á samskiptaupplýsingum. |
| **Gerð**<br>mshr_type<br>*mshr_logisticselectronicaddressmethodtype valkostur stilltur* | Lesa/skrifa<br>Krafa | Gerð tengiliðaupplýsinga. |
| **Landskóði/svæðakóði**<br>mshr_countryregioncode<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Land eða svæði aðsetursins. |
| **Slóð**<br>mshr_locator<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Tengiliðaupplýsingar. Ef gerðin er til dæmis **Netfang**  inniheldur þessi reitur netfang umsækjanda. |
| **Viðbót staðsetjara**<br>mshr_locatorextension<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Viðbót staðsetjara. Ef gerðin er til dæmis **Sími** ætti þessi eiginleiki að innihalda viðbót símanúmera. |
| **Er farsími**<br>mshr_ismobile<br>*mshr_noyes valkostur stilltur* | Lesa/skrifa<br>Krafa | Tilgreinir hvort síminn sé farsímanúmer. |
| **Er spjallskilaboð**<br>mshr_isinstantmessage<br>*mshr_noyes valkostur stilltur* | Lesa/skrifa<br>Krafa | Tilgreinir hvort síminn geti tekið við spjallskilaboðum. |
| **Er aðal**<br>mshr_isprimary<br>*mshr_noyes valkostur stilltur* | Lesa/skrifa<br>Krafa | Ákvarðar aðaltengiliðinn tengiliðagerðarinnar. Aðeins má vera ein aðalfærsla á hverja gerð tengiliðar. |
| **Er einka**<br>mshr_isprivate<br>*mshr_noyes valkostur stilltur* | Lesa/skrifa<br>Krafa | Segir til um hvort þetta aðsetur er einkaaðsetur einstaklingsins. |
| **Notkun**<br>mshr_purpose<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Tilgangur/hlutverk tengslaupplýsinga. |
| **Aðalsvæði**<br>mshr_primaryfield<br>*Strengur* | Lesa eingöngu<br>Krafa | Svæði notað sem aðalkennimerki einingafærslu. Samsetning aðilanúmers, gerðar, lýsingu og staðsetjara. |

## <a name="see-also"></a>Sjá einnig

[Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda](hr-admin-integration-ats-api-introduction.md)<br>
[Dæmi um fyrirspurn fyrir umsækjanda til ráðningar](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
