---
title: Gerð skírteinis
description: Þessi grein lýsir vottorðsgerðinni fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: bfe7f06176098a504f8d2ad1c1431a6f60fe059c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886190"
---
# <a name="certificate-type"></a>Gerð skírteinis


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þessi grein lýsir vottorðsgerðinni fyrir Dynamics 365 Human Resources.

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
