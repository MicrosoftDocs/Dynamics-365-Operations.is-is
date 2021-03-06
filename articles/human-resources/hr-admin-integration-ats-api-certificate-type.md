---
title: Gerð skírteinis
description: Þetta efnisatriði lýsir einingu vottorðagerðar fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: b8e979f242eb689b730b7f8a8684b3e697adbee6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054693"
---
# <a name="certificate-type"></a>Gerð skírteinis

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði lýsir einingu vottorðagerðar fyrir Dynamics 365 Human Resources.

Raunlægt heiti: mshr_hcmcertificatetypeentity

## <a name="description"></a>lýsing

Þessi eining skilgreinir lista yfir faglegar vottorðagerðir sem settar eru upp í Human Resources. Einingin er ekki sértæk fyrir lögaðila (fyrirtæki).

## <a name="json-representation"></a>JSON-framsetning

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a>Eiginleikar

| Eiginleiki<br>**Efnislegt heiti**<br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Kenni fyrir einingu vottorðagerðar**<br>mshr_hcmcertificatetypeentityid<br>*GUID* | Lesa eingöngu<br>Krafa 
Myndað af kerfinu | Einkvæmt aðalkenni fyrir vottorðagerðina. |
| **Gerð vottorðs**<br>mshr_certificatetype<br>*Strengur* | Lesa/skrifa<br>Krafa | Einkvæmt lesanlegt kenni fyrir vottorðagerðina. |
| **Lýsing**<br>mshr_description<br>*Strengur* | Lesa/skrifa<br>Krafa | Lýsing á vottorðagerð. |
| **Krefjast endurnýjunar**<br>mshr_requirerenewal<br>*mshr_noyes valkostur stilltur* | Lesa/skrifa<br>Valfrjálst | Tilgreinir hvort krafist sé endurnýjunar á vottorði. |

## <a name="see-also"></a>Sjá einnig

[Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda](hr-admin-integration-ats-api-introduction.md)<br>
[Dæmi um fyrirspurn fyrir umsækjanda til ráðningar](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]