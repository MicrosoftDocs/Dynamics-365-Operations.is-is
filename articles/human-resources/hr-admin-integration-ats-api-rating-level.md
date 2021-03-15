---
title: Matsstig
description: Þetta efnisatriði lýsir einingu matsstig fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: 1ad37c7a5b961bb03d37775168dac91e606d2b08
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125258"
---
# <a name="rating-level"></a>Matsstig

Þetta efnisatriði lýsir einingu matsstig fyrir Dynamics 365 Human Resources.

Raunlægt heiti: mshr_hcmratinglevelentity

## <a name="description"></a>lýsing

Þessi eining býður upp á tiltæk matsstig fyrir hæfni. Matsstig gilda yfir alla lögaðila.

## <a name="json-representation"></a>JSON-framsetning

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a>Eiginleikar

| Eiginleiki<br>**Efnislegt heiti**<br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Kenni fyrir einingu matsstigs**<br>mshr_hcmratinglevelentityid<br>*GUID* | Lesa eingöngu<br>Krafa<br>Myndað af kerfinu | Einkvæmt kerfismyndað auðkenni fyrir stigið. |
| **Auðkenni matsstigs**<br>mshr_ratinglevelid<br>*Strengur* | Lesa/skrifa<br>Krafa | Notandalesvænt einkvæmt kenni fyrir stigið. |
| **Kenni matslíkans**<br>mshr_ratingmodelid<br>*Strengur* | Lesa/skrifa<br>Krafa | Matslíkanið sem matsstigið tilheyrir. |
| **Kenni fyrir einingu matslíkans**<br>_mshr_fk_ratingmodelentity_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Framandlykill: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity | Kerfismyndað kenni fyrir matslíkanið sem matsstigið tilheyrir. |
| **Lýsing**<br>mshr_description<br>*Strengur* | Lesa/skrifa<br>Krafa | Lýsing á matsstiginu. |
| **Stuðull**<br>mshr_factor<br>*Heiltala* | Lesa/skrifa<br>Krafa | Stuðullinn fyrir matsstigið. Þegar vörur eru bornar saman við annan fjölda matsstiga er stuðullinn notaður til að staðla skorið. Gildið verður að vera heiltala á bilinu 0 til 9. |
| **Ábending**<br>mshr_note<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Allar athugsemdir sem tengjast matsstiginu. |
| **Aðalsvæði**<br>mshr_primaryfield<br>*Strengur* | Lesa eingöngu<br>Krafa | Svæði sem á að nota sem kennimerki einingafærslu. Samsetning af kenni matsstigs og kenni matslíkans. |

## <a name="see-also"></a>Sjá einnig

[Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda](hr-admin-integration-ats-api-introduction.md)<br>
[Dæmi um fyrirspurn fyrir umsækjanda til ráðningar](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]