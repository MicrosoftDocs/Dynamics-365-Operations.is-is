---
title: Vottorð einstaklings
description: Þetta efnisatriði lýsir einingu fyrir vottorð einstaklings fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: 4587337d8fd52828309826f3301b6f053b267819
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466521"
---
# <a name="person-certificate"></a>Vottorð einstaklings

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði lýsir einingu fyrir vottorð einstaklings fyrir Dynamics 365 Human Resources.

Raunlægt heiti: mshr_hcmpersoncertificateentity

## <a name="description"></a>lýsing

Þessi eining lýsir faglegum vottorðum umsækjanda.

## <a name="json-representation"></a>JSON-framsetning

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a>Eiginleikar

| Eiginleiki<br>**Efnislegt heiti**<br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Kenni fyrir einingu vottorðs einstaklings**<br>mshr_hcmpersoncertificateentityid<br>*GUID* | Lesa eingöngu<br>Krafa | Kerfismyndað einkvæmt kenni fyrir færslueiningu einstaklingsvottorðs. |
| **Aðilanúmer**<br>mshr_partynumber<br>*Strengur* | Lesa/skrifa<br>Krafa | Kenni aðila (einstaklings) fyrir umsækjanda. |
| **Gildi fyrir auðkenni einstaklings**<br>_mshr_fk_person_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Framandlykill: mshr_dirpersonentityid of mshr_dirpersonentity | Kerfismynduð kenni fyrir færslueiningu aðila (einstaklings). |
| **Gerð vottorðskennis**<br>mshr_certificatetypeid<br>*Strengur* | Lesa/skrifa<br>Krafa |  Kenni vottorðagerðar skilgreint í Human Resources. |
| **Gildi fyrir kenni vottorðagerðar**<br>_mshr_fk_certificatetype_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Framandlykill: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity | Kerfismyndað einkvæmt kenni vottorðagerðar í tengdri einingu. |
| **Upphafsdagsetning**<br>mshr_startdate<br>*Dagsetning og tími* | Lesa/skrifa<br>Krafa | Dagsetningin þegar vottorð var gefið út. |
| **Lokadagsetning**<br>mshr_enddate<br>*Dagsetning og tími* | Lesa/skrifa<br>Valfrjálst | Dagsetningin þegar vottorð rennur út. |
| **Athugasemdir**<br>mshr_notes<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Athugasemdir sem ráðningarstjórar og ráðningaraðilar nota. |
| **Aðalsvæði**<br>mshr_primaryfield<br>*Strengur* | Lesa eingöngu<br>Krafa |  Svæði sem á að nota sem kennimerki einingafærslu. Samsetning aðilanúmers, kennisgerð vottorðs og upphafsdagsetning. |

## <a name="see-also"></a>Sjá einnig

[Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda](hr-admin-integration-ats-api-introduction.md)<br>
[Dæmi um fyrirspurn fyrir umsækjanda til ráðningar](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]