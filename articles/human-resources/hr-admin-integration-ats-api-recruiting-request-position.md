---
title: Staða í ráðningarbeiðni
description: Þessi grein lýsir stöðueiningunni um ráðningarbeiðni fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: 0996532edf09ea5159e143d92fb2a93c4d6f826d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904247"
---
# <a name="recruiting-request-position"></a>Staða í ráðningarbeiðni


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þessi grein lýsir stöðueiningunni um ráðningarbeiðni fyrir Dynamics 365 Human Resources.

Raunlægt heiti: mshr_hcmrecruitingrequestpositionentity

### <a name="description"></a>lýsing

Lýsir stöðunni eða stöðunum sem á að ráða í fyrir ráðningarbeiðni. Að bæta stöðu við ráðningarbeiðnina er valfrjálst. Eiginleikar stöðunnar eru skrifvarðir þar sem stöðueiginleikarnir eiga ekki að vera öðruvísi á ráðningarbeiðninni en þeir eru í aðalfærslu stöðunnar. Ef breyta þarf eiginleikunum ætti að gera það í aðalfærslu stöðunnar áður en stöðunni er bætt við ráðningarbeiðnina.

### <a name="json-representation"></a>JSON-framsetning
```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_positionid": "String",
    "mshr_description": "String",
    "mshr_positiontypeid": "String",
    "mshr_status": Int,
    "mshr_departmentnumber": "String",
    "mshr_reportstopositionid": "String",
    "mshr_reportstopersonnelnumber": "String",
    "mshr_financialdimension": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_position_id_value": "Guid",
    "_mshr_fk_positiontype_id_value": "Guid",
    "_mshr_fk_department_id_value": "Guid",
    "_mshr_fk_reportstoposition_id_value": "Guid",
    "_mshr_fk_reportstoworker_id_value": "Guid",
    "mshr_hcmrecruitingrequestpositionentityid": "Guid"
}
```

### <a name="properties"></a>Eiginleikar

| Eiginleiki<br>**Efnislegt heiti**<br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Einingarkenni fyrir stöðu ráðningarbeiðni**<br>mshr_hcmrecruitingrequestpositionentityid<br>*GUID* | Lesa eingöngu<br>Krafa |    Kerfismyndað kenni fyrir stöðufærslu ráðningarbeiðni. |
| **Kenni ráðningarbeiðni**<br>mshr_recruitingrequestid<br>*Strengur* | Einskrifanlegt<br>Krafa | Einkvæmt lesanlegt kenni ráðningarbeiðninnar. |
| **Gildi fyrir kenni ráðningarbeiðni**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Framandlykill: mshr_hcmrecruitingrequestentityid of mshr_hcmrecruitingrequestentity eining | Kerfismyndað kenni ráðningarbeiðni þar sem stöðunni er úthlutað. |
| **Auðkenni stöðuheitis**<br>mshr_positionid<br>*Strengur* | Einskrifanlegt<br>Krafa | Einkvæmt lesanlegt kenni stöðunnar. |
| **Gildi fyrir staðsetningarkenni**<br>_mshr_fk_position_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Ytri lykill: mshr_hcmpositionv2entityid úr einingu mshr_hcmpositionv2entity | Kerfismyndað kenni stöðunnar. |
| **Lýsing**<br>mshr_description<br>*Strengur* | Lesa eingöngu<br>Krafa | Lýsing á stöðunni. |
| **Kenni stöðugerðar**<br>mshr_positiontypeid<br>*Strengur* | Lesa eingöngu<br>Valfrjálst | Einkvæmt lesanlegt kenni stöðugerðar fyrir þessa stöðu. |
| **Gildi fyrir kenni staðsetningargerðar**<br>_mshr_fk_positiontype_id_value<br>*GUID* | Lesa eingöngu<br>Valfrjálst<br>Ytri lykill: mshr_hcmpositiontypeentityid úr einingu mshr_hcmpositiontypeentity | Kerfismyndað einkvæmt lesanlegt kenni stöðugerðar fyrir þessa stöðu. |
| **Staða**<br>mshr_status<br>Valkostir *RecruitingRequestPositionStatus* | Lesa/skrifa<br>Krafa | Staða stöðu fyrir ráðningarbeiðnina. |
| **Deildarnúmer**<br>mshr_departmentnumber<br>*Strengur* | Lesa eingöngu<br>Valfrjálst<br> | Deildarnúmer stöðunnar. |
| **Gildi deildarkennis**<br>_mshr_fk_department_id_value<br>*GUID* | Lesa eingöngu<br>Valfrjálst<br>Framandlykill: mshr_omdepartmententityid of mshr_omdepartmententity eining | Kerfismyndað einkvæmt kenni deildar fyrir stöðuna. |
| **Skýrslur eftir stöðu**<br>mshr_reportstopositionid<br>*Strengur* | Lesa eingöngu<br>Krafa | Lesanlegt kenni stöðu þar sem ráðna staðan sendir tilkynningar til í stigveldi fyrirtækisins. |
| **Gildi fyrir stöðukenni tilkynninga**<br>_mshr_fk_reportstoposition_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Ytri lykill: mshr_hcmpositionv2entityid úr einingu mshr_hcmpositionv2entity | Kerfismyndað kenni stöðu sem ráðna staðan sendir tilkynningar til. |
| **Númer starfsmanns**<br>mshr_reportstopersonnelnumber<br>*Strengur* | Lesa eingöngu<br>Krafa | Kenni starfsmanns sem ráðinn umsækjandi heyrir undir. |
| **Gildi fyrir starfsmannakenni tilkynninga**<br>_mshr_fk_reportstoworker_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Framandlykill: mshr_hcmworkerbaseentityid of mshr_hcmworkerbaseentity eining | Kerfismyndað kenni starfsmanns sem ráðinn umsækjandi heyrir undir. |
| **Fjárhagsvídd**<br>mshr_financialdimension<br>*Strengur* | Lesa eingöngu<br>Valfrjálst | Fjárhagsvíddin (til dæmis kostnaðarstaður) sem úthlutað er á stöðuna. Fjárhagsvíddinni er úthlutað fyrir hverja stöðu á hvern lögaðila. Kostnaðarstaðir sem eru skilgreindir í víddunum eru aðgengilegar í gegnum einingu mshr_dimattributeomcostcenterentity. |
| **Kenni gagnasvæðis**<br>mshr_dataareaid<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Tilgreinir lögaðilann (fyrirtækið) fyrir stöðu ráðningarbeiðninnar. |
| **Gildi fyrir kenni gagnasvæðis**<br>_mshr_dataareaid_id_value<br>*GUID* | Lesa eingöngu<br>Valfrjálst<br>Framandlykill: cdm_companyid of cdm_company entity | GUID-gildi myndað af kerfinu sem tilgreinir lögaðilann (fyrirtækið) fyrir stöðu ráðningarbeiðninnar. |
| **Aðalsvæði**<br>mshr_primaryfield<br>*Strengur* | Lesa eingöngu<br>Krafa | Samsetning á gildi ráðningarbeiðni og stöðukennis sem önnur aðferð til að auðkenna færsluna. |

## <a name="see-also"></a>Sjá einnig

[Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda](hr-admin-integration-ats-api-introduction.md)<br>
[Dæmi um fyrirspurn fyrir ráðningarbeiðni](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
