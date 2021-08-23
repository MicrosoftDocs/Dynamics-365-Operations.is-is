---
title: Menntun einstaklings
description: Þetta efnisatriði lýsir menntunareiningu einstaklings fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: 5e24188674c7746794c0e531dea21aa9b7f57b3534d4b67298cad19b6bec2a53
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731368"
---
# <a name="person-education"></a>Menntun einstaklings

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði lýsir menntunareiningu einstaklings fyrir Dynamics 365 Human Resources.

Raunlægt heiti: mshr_hcmpersoneducationentity

## <a name="description"></a>lýsing

Þessi eining inniheldur menntunarferil einstaklingsins sem er umsækjandinn. Menntun er tengd við færslu einstaklingsins og gerir kleift að tengja menntunina við annað hlutverk sem er búið til fyrir einstaklinginn auk umsækjandafærslunnar (starfskraftur, verktaki og svo framvegis).

## <a name="json-representation"></a>JSON-framsetning

```json
{
    "mshr_creditbasis": Int,
    "mshr_creditscompleted": Decimal,
    "mshr_creditsearned": Decimal,
    "mshr_creditsneeded": Decimal,
    "mshr_description": "String",
    "mshr_duration": Decimal,
    "mshr_durationunit": Int,
    "mshr_educationdisciplineid": "String",
    "mshr_educationinstitutionid": "String",
    "mshr_educationlevelid": "String",
    "mshr_enddate": "Date",
    "mshr_gradepointaverage": Decimal,
    "mshr_gradescale": "String",
    "mshr_notes": "String",
    "mshr_secondaryemphasis": "String",
    "mshr_startdate": "Date",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_educationinstitution_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmpersoneducationentityid": "Guid"
}
```

## <a name="properties"></a>Eiginleikar

| Eiginleiki<br>**Efnislegt heiti**<br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Kenni menntunareiningar einstaklings**<br>mshr_hcmpersoneducationentityid<br>*GUID* | Lesa eingöngu<br>Krafa | Einkvæmt kerfismyndað kenni fyrir færslu menntunareiningar einstaklingsins. |
| **Aðilanúmer**<br>mshr_partynumber<br>*Strengur* | Lesa/skrifa<br>Krafa | Einkvæmt kenni fyrir færslu aðilans (einstaklingsins) fyrir umsækjandann. |
| **Gildi fyrir auðkenni einstaklings**<br>_mshr_fk_person_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Framandlykill: mshr_dirpersonentityid of mshr_dirpersonentity | Kerfismyndað einkvæmt kenni einstaklingsfærslu umsækjanda. |
| **Inneignargrunnur**<br>mshr_creditbasis<br>*mshr_hcmeducationcreditbasis valkostur stilltur* | Lesa/skrifa<br>Valfrjálst | Einingagrunnur menntunarstigs. |
| **Lokið við inneignir**<br>mshr_creditscompleted<br>*Tugabrot* | Lesa/skrifa<br>Valfrjálst | Fjöldi eininga kláraðar fyrir menntunina. |
| **Áunnir punktar**<br>mshr_creditsearned<br>*Tugabrot* | Lesa/skrifa<br>Valfrjálst | Fjöldi áunninna eininga fyrir færslu menntunar fyrir gráðu í vinnslu. |
| **Einingar sem þarf**<br>mshr_creditsneeded<br>*Tugabrot* | Lesa/skrifa<br>Valfrjálst | Fjöldi eininga sem þarf fyrir yfirstandandi gráðu. |
| **Lýsing**<br>mshr_description<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Lýsing á gráðu umsækjandans. |
| **Kenni menntunarstigs**<br>mshr_educationlevelid<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Kenni menntunarstigsins. | 
| **Gildi menntunarstigs**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | Lesa eingöngu<br>Valfrjálst<br>Ytri lykill: mshr_hcmeducationdegreeentityid úr einingu mshr_hcmeducationdegreeentity | Kerfismyndað kenni fyrir færslu menntagráðu. Þetta kenni sýnir gráðurnar og menntunarstigið sem skilgreint er fyrir fyrirtækið. |
| **Kenni námsgreina**<br>mshr_educationdisciplineid<br>*Strengur* | Lesa/skrifa<br>Krafa<br>Ytri lykill: EducationDiscipline | Kenni námsgreinarinnar. |
| **Gildi fyrir kenni námsgreinar**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Ytri lykill: mshr_hcmeducationdisciplineentityid úr einingu mshr_hcmeducationdisciplineentity | Kerfismyndað einkvæmt kenni námsgreinar menntunarfærslunnar. |
| **Aukaleg áhersla**<br>mshr_secondaryemphasis<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Aukaáhersla áunninnar gráðu. |
| **Kenni menntastofnunar**<br>mshr_educationinstitutionid<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Kenni sóttrar menntastofnunar. |
| **Gildi fyrir kenni menntastofnunar**<br>_mshr_fk_educationinstitution_id_value<br>*GUID* | Lesa eingöngu<br>Valfrjálst<br>Ytri lykill: mshr_hcmeducationinstitutionentityid úr mshr_hcmeducationinstitutionentity | Kerfismyndað kennimerki fræðslustofnunar. |
| **Upphafsdagsetning**<br>mshr_startdate<br>*Dagsetning og tími* | Lesa/skrifa<br>Valfrjálst | Upphafsdagsetning menntunar fyrir áunna gráðu. |
| **Lokadagsetning**<br>mshr_enddate<br>*Dagsetning og tími* | Lesa/skrifa<br>Krafa | Útgáfudagsetning skilríkja. |
| **Lengd**<br>mshr_duration<br>*Tugabrot* | Lesa/skrifa<br>Valfrjálst | Tímalengd menntunarfærslunnar. |
| **Tímalengdareining**<br>mshr_durationunit<br>*mshr_periodunit valkostur stilltur* | Lesa/skrifa<br>Valfrjálst | Tímaeiningin sem tengist lengd menntunarfærslunnar. |
| **Meðaleinkunn**<br>mshr_gradepointaverage<br>*Tugabrot* | Lesa/skrifa<br>Valfrjálst | Áunnin meðaleinkunn gráðunnar. |
| **Einkunnakvarði**<br>mshr_gradescale<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Kvarðinn sem notaður er fyrir meðaleinkunnina. |
| **Athugasemdir**<br>mshr_notes<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Glósur sem ráðningaraðili eða ráðningarstjóri nota. |
| **Aðalsvæði**<br>mshr_primaryfield<br>*Strengur* | Lesa eingöngu<br>Krafa | Svæði notað sem annað aðalkennimerki einingafærslu. Samsetning aðilanúmers, kenni námsgreinar, kenni menntastofnunar og kenni menntunarstigs. |

## <a name="see-also"></a>Sjá einnig

[Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda](hr-admin-integration-ats-api-introduction.md)<br>
[Dæmi um fyrirspurn fyrir umsækjanda til ráðningar](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]