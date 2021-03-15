---
title: Menntun í ráðningarbeiðni
description: Þetta efnisatriði lýsir einingu fyrir menntun í ráðningarbeiðni fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: 1767edfe67f9c3af4ac67eb5403d63a7f54dcac8
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126075"
---
# <a name="recruiting-request-education"></a>Menntun í ráðningarbeiðni

Þetta efnisatriði lýsir einingu fyrir menntun í ráðningarbeiðni fyrir Dynamics 365 Human Resources.

Raunlægt heiti: mshr_hcmrecruitingrequesteducationentity

### <a name="description"></a>lýsing

Lýsir menntunarkröfum fyrir RecruitingRequest.

### <a name="json-representation"></a>JSON-framsetning

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_educationdisciplineid": "String",
    "mshr_educationdisciplinedescription": "String",
    "mshr_educationlevelid": "String",
    "mshr_educationleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequesteducationentityid": "Guid"
}
```

### <a name="properties"></a>Eiginleikar

| Eiginleiki<br>**Efnislegt heiti**<br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Kenni fyrir einingu menntunar í ráðningarbeiðni**<br>mshr_hcmrecruitingrequesteducationentityid<br>*GUID* | Lesa eingöngu<br>Krafa | Einkvæmt kerfismyndað kenni fyrir færslu menntunar í ráðningarbeiðni. |
| **Kenni ráðningarbeiðni**<br>mshr_recruitingrequestid<br>*Strengur* | Einskrifanlegt<br>Krafa | Einkvæmt lesanlegt kenni tengdrar ráðningarbeiðni. |
| **Gildi fyrir kenni ráðningarbeiðni**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Framandlykill: mshr_hcmrecruitingrequestentityid of mshr_hcmrecruitingrequestentity | Einkvæmt kerfismyndað kenni tengdrar ráðningarbeiðni. |
| **Kenni menntunarstigs**<br>mshr_educationlevelid<br>*Strengur* | Einskrifanlegt<br>Krafa | Menntunarstig sem er krafist. |
| **Kennisgildi menntunarstigs**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Framandlykill: mshr_hcmeducationlevelentityid of mshr_hcmeducationlevelentity | Einkvæmt kerfismyndað kenni fyrir menntunarstig sem er krafist. |
| **Lýsing á menntunarstigi**<br>mshr_educationleveldescription<br>*Strengur* | Lesa eingöngu<br>Krafa | Lýsing á því stigi sem krafist er fyrir hæfnina. |
| **Kenni námsgreina**<br>mshr_educationdisciplinedescription<br>*Strengur* | Einskrifanlegt<br>Krafa | Svið námsgreinar. |
| **Gildi fyrir kenni námsgreinar**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Ytri lykill: mshr_hcmeducationdisciplineentityid úr einingu mshr_hcmeducationdisciplineentity | Kerfismyndað einkvæmt kenni fyrir grein menntunarsviðs. |
| **Lýsing á námsgrein**<br>mshr_educationdisciplinedescription<br>Strengur | Lesa eingöngu<br>Krafa | Lýsing á sviði námsgreinar. |
| **Kenni gagnasvæðis**<br>mshr_dataareaid<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Tilgreinir lögaðilann (fyrirtækið).|
| **Gildi fyrir kenni gagnasvæðis**<br>_mshr_dataareaid_id_value<br>*GUID* | Lesa eingöngu<br>Valfrjálst<br>Framandlykill: cdm_companyid of cdm_company entity | Kerfismyndað GUID-gildi sem tilgreinir lögaðilann (fyrirtækið). |
| **Aðalsvæði**<br>mshr_primaryfield<br>*Strengur* | Lesa eingöngu<br>Krafa | Samsetning á gildi ráðningarbeiðni og kenni menntunarstigs og kenni námsgreinar sem önnur aðferð til að auðkenna færsluna. |

## <a name="see-also"></a>Sjá einnig

[Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda](hr-admin-integration-ats-api-introduction.md)<br>
[Dæmi um fyrirspurn fyrir ráðningarbeiðni](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]