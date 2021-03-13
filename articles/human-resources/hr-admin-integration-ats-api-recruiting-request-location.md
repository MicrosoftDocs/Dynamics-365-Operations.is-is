---
title: Staðsetning í ráðningarbeiðni
description: Þetta efnisatriði lýsir einingu fyrir staðsetningu í ráðningarbeiðni fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: fa153b1cfcbb70294ed6da3618c83396df04f8db
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125234"
---
# <a name="recruiting-request-location"></a>Staðsetning í ráðningarbeiðni

Þetta efnisatriði lýsir einingu fyrir staðsetningu í ráðningarbeiðni fyrir Dynamics 365 Human Resources.

Raunlægt heiti: mshr_hcmrecruitingrequestlocationentity

### <a name="description"></a>lýsing

Listi yfir staðsetningar sem skilgreindir eru sem staðsetningar þar sem ráðnir starfsmenn hefja störf við ráðningu. Þetta eru staðsetningar sem búnar eru til yfir alla lögaðila.

### <a name="json-representation"></a>JSON-framsetning

```
{
    "mshr_recruitingrequestlocationid": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_telephone": "String",
    "mshr_email": "String",
    "mshr_internetaddress": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_dataareaid": "String",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmrecruitingrequestlocationentityid": "Guid"
}
```

### <a name="properties"></a>Eiginleikar

| Eiginleiki<br>**Efnislegt heiti**<br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Staðsetningarkenni**<br>mshr_locationid<br>*Strengur* | Einskrifanlegt<br>Krafa | Kerfismyndað, lesanlegt kenni fyrir staðsetningu ráðningar. |
| **Staðsetning í ráðningarbeiðni**<br>mshr_recruitingrequestlocationid<br>*Strengur* | Einskrifanlegt<br>Krafa | Notandaskilgreint einkvæmt kenni fyrir staðsetningu ráðningar. |
| **Kenni fyrir einingu staðsetningu ráðningarbeiðni**<br>mshr_hcmrecruitingrequestlocationentityid<br>*GUID* | Lesa eingöngu<br>Krafa | Kerfismyndað einkvæmt kenni fyrir staðsetningarfærslu ráðningarbeiðni. |
| **Lýsing**<br>mshr_description<br>*Strengur* | Lesa/skrifa<br>Krafa | Lýsing á staðsetningunni. |
| **Kenni lands/svæðis**<br>mshr_countryregionid<br>*Strengur* | Lesa eingöngu<br>Valfrjálst | Tilgreinir landið eða svæðið þar sem umsækjandi er með ríkisborgararétt. |
| **Kennigildi lands/svæðis**<br>_mshr_fk_countriregion_id_value<br>*GUID* | Lesa eingöngu<br>Valfrjálst<br>Framandlykill: mshr_logisticaddresscountryregionentityid of mshr_logisticsaddresscountryregionentity | Kerfismyndað einkvæmt kenni lands/svæðis aðsetursins. |
| **Póstnúmer**<br>mshr_zipcode<br>*Strengur* | Lesa eingöngu<br>Valfrjálst | Póstnúmer. |
| **Gata**<br>mshr_street<br>*Strengur* | Lesa eingöngu<br>Valfrjálst | Heimilisfang. |
| **Póststöð**<br>mshr_city<br>*Strengur* | Lesa eingöngu<br>Valfrjálst | Borg. |
| **Ríki**<br>mshr_state<br>*Strengur* | Lesa eingöngu<br>Valfrjálst | Fylki eða hérað. |
| **Sýsla**<br>mshr_county<br>*Strengur* | Lesa eingöngu<br>Valfrjálst | Sýsla. |
| **Sími**<br>mshr_telephone<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Símanúmer fyrir staðsetninguna. |
| **Tölvupóstur**<br>mshr_email<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Netfang. |
| **InternetAddress**<br>mshr_internetaddress<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Vefslóð fyrir vefsvæði staðsetningar. |
| **Kenni gagnasvæðis**<br>mshr_dataareaid<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Tilgreinir lögaðilann (fyrirtækið). |
| **Gildi fyrir kenni gagnasvæðis**<br>_mshr_dataareaid_id_value<br>*GUID* | Lesa eingöngu<br>Valfrjálst<br>Framandlykill: cdm_companyid of cdm_company entity | Kerfismyndað GUID-gildi sem tilgreinir lögaðilann (fyrirtækið). |

## <a name="see-also"></a>Sjá einnig

[Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda](hr-admin-integration-ats-api-introduction.md)<br>
[Dæmi um fyrirspurn fyrir ráðningarbeiðni](hr-admin-integration-ats-api-recruiting-request-example-query.md)

