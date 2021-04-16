---
title: Færni í ráðningarbeiðni
description: Þetta efnisatriði lýsir einingu fyrir hæfni í ráðningarbeiðni fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: 9e464ced904eb4358ba5d4e1c6c2c36089bfa0d8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801312"
---
# <a name="recruiting-request-skill"></a>Færni í ráðningarbeiðni

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði lýsir einingu fyrir hæfni í ráðningarbeiðni fyrir Dynamics 365 Human Resources.

Raunlægt heiti: mshr_hcmrecruitingrequestskillentity

### <a name="description"></a>lýsing

Lýsir hæfnikröfum fyrir RecruitingRequest.

### <a name="json-representation"></a>JSON-framsetning

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_skillid": "String",
    "mshr_skilldescription": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_ratingleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratingmodel_id_value": "Guid",
    "mshr_hcmrecruitingrequestskillentityid": "Guid"
}
```

### <a name="properties"></a>Eiginleikar

| Eiginleiki<br>**Efnislegt heiti**<br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Kenni fyrir einingu hæfni í ráðningarbeiðni**<br>mshr_hcmrecruitingrequestskillentityid<br>*GUID* | Lesa eingöngu<br>Krafa | Einkvæmt kerfismyndað kenni fyrir færsluna **Hæfni í ráðningarbeiðni**. |
| **Kenni ráðningarbeiðni**<br>mshr_recruitingrequestid<br>*Strengur* | Einskrifanlegt<br>Krafa | Einkvæmt lesanlegt kenni tengdrar ráðningarbeiðni. |
| **Gildi fyrir kenni ráðningarbeiðni**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br> Framandlykill: mshr_hcmrecruitingrequestentityid of mshr_hcmrecruitingrequestentity eining | Einkvæmt kerfismyndað kenni tengdrar ráðningarbeiðni. |
| **Hæfniskenni**<br>mshr_skillid<br>*Strengur*<br> | Einskrifanlegt<br>Krafa | Einkvæmt lesanlegt kenni áskilinnar hæfni. |
| **Gildi fyrir færniskenni**<br>_mshr_fk_skill_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Framandlykill: mshr_hcmskillentityid of mshr_hcmskillentity eining | Einkvæmt kerfismyndað kenni áskildrar hæfni. |
| **Auðkenni matsstigs**<br>mshr_ratinglevelid<br>*Strengur* | Einskrifanlegt<br>Valfrjálst | Áskilið stiggildi hæfni sem er valið fyrir starfið byggt á matslíkaninu sem úthlutað er á hæfnina. |
| **Gildi fyrir kenni einkunnastigs**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | Lesa eingöngu<br>Valfrjálst<br>Framandlykill: mshr_hcmratinglevelentityid of mshr_hcmratinglevelentity eining | Einkvæmt kerfismyndað kenni fyrir stigið. |
| **Hæfnilýsing**<br>mshr_skilldescription<br>*Strengur* | Lesa eingöngu<br>Krafa | Hæfnislýsing. |
| **Lýsing á hæfnisstigi**<br>mshr_ratingleveldescription<br>*Strengur* | Lesa eingöngu<br>Valfrjálst | Lýsing á völdu hæfnisstigi. |
| **Kenni gagnasvæðis**<br>mshr_dataareaid<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Tilgreinir lögaðilann (fyrirtækið). |
| **Gildi fyrir kenni gagnasvæðis**<br>_mshr_dataareaid_id_value<br>*GUID* | Lesa eingöngu<br>Valfrjálst<br>Framandlykill: cdm_companyid of cdm_company entity | Kerfismyndað GUID-gildi sem tilgreinir lögaðilann (fyrirtækið). |
| **Aðalsvæði**<br>mshr_primaryfield<br>*Strengur* | Lesa eingöngu<br>Krafa | Samsetning á gildi ráðningarbeiðni og kenni hæfni sem önnur aðferð til að auðkenna færsluna. |
| **Kenni matslíkans**<br>mshr_ratingmodelid<br>*Strengur* | Lesa-skrifa<br>Krafa | Matslíkanið sem notað er til að meta hæfnina. |
| **Gildi fyrir kenni matslíkans**<br>_mshr_fk_hcmratingmodel_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Framandlykill: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity eining | Einkvæmt kerfismyndað kenni matslíkansins sem notað er til að meta hæfnina. |

## <a name="see-also"></a>Sjá einnig

[Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda](hr-admin-integration-ats-api-introduction.md)<br>
[Dæmi um fyrirspurn fyrir ráðningarbeiðni](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]