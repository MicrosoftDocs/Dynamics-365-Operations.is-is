---
title: Starfsreynsla einstaklins
description: Þetta efnisatriði lýsir einingu fyrir starfsreynslu einstaklings fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: 51dd993e2d43174e96c062e142021cc0f6e3a288
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125282"
---
# <a name="person-professional-experience"></a>Starfsreynsla einstaklins

Þetta efnisatriði lýsir einingu fyrir starfsreynslu einstaklings fyrir Dynamics 365 Human Resources.

Raunlægt heiti: mshr_hcmpersonprofessionalexperienceentity

## <a name="description"></a>lýsing

Þessi eining lýsir starfsreynslu eða starfsferli umsækjanda.

## <a name="json-representation"></a>JSON-framsetning

```json
{
    "mshr_partynumber": "String",
    "mshr_employerposition": "String",
    "mshr_startdate": "Date",
    "mshr_allowcontactemployer": Int,
    "mshr_employerlocation": "String",
    "mshr_employername": "String",
    "mshr_enddate": "Date",
    "mshr_note": "String",
    "mshr_phone": "String",
    "mshr_url": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonprofessionalexperienceentityid": "Guid"
}
```

## <a name="properties"></a>Eiginleikar

| Eiginleiki<br>**Efnislegt heiti**<br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Kenni fyrir einingu starfsreynslu einstaklings**<br>mshr_hcmpersonprofessionalexperienceentityid<br>*GUID* | Lesa eingöngu<br>Krafa | Kerfismyndað einkvæmt kenni fyrir færslueininguna. |
| **Aðilanúmer**<br>mshr_partynumber<br>*Strengur* | Lesa/skrifa<br>Krafa | Einkvæmt kenni einstaklingsfærslu fyrir umsækjanda. |
| **Gildi fyrir auðkenni einstaklings**<br>_mshr_fk_person_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Framandlykill: mshr_dirpersonentityid of mshr_dirpersonentity | Einkvæmt kerfismyndað kenni fyrir færslueiningu einstaklings. |
| **Staða starfsmanns**<br>mshr_employerposition<br>*Strengur* | Lesa/skrifa<br>Krafa | Titill stöðu sem umsækjandi hélt meðan í starfi. |
| **Nafn vinnuveitanda**<br>mshr_employername<br>*Strengur* | Lesa/skrifa<br>Krafa | Nafn vinnuveitanda. |
| **Staðsetning vinnuveitanda**<br>mshr_employerlocation<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Staðsetning starfsmanns. Hámarkslengd: 60. Ekkert sérstakt snið skilgreint eða áskilið. |
| **Sími**<br>mshr_phone<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Símanúmer starfsmanns. |
| **Vefslóð**<br>mshr_url<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Vefslóð fyrir vefsvæði starfsmanns. |
| **Upphafsdagsetning**<br>mshr_startdate<br>*Dagsetning og tími* | Lesa/skrifa<br>Krafa | Upphafsdagsetning ráðningar umsækjanda. |
| **Lokadagsetning**<br>mshr_enddate<br>*Dagsetning og tími* | Lesa/skrifa<br>Valfrjálst | Lokadagur ráðningar umsækjanda eða núll ef umsækjandi starfar enn hér. |
| **Leyfa að hafa samband við starfsmann**<br>mshr_allowcontactemployer<br>*mshr_hrmblankyesno valkostur stilltur* | Lesa/skrifa<br>Valfrjálst | Segir til um hvort umsækjandi leyfir samband við fyrri vinnuveitanda. |
| **Athugasemdir**<br>mshr_note<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Glósur sem ráðningaraðili eða ráðningarstjóri nota. |
| **Aðalsvæði**<br>mshr_primaryfield<br>*Strengur* | Lesa eingöngu<br>Krafa | Svæði notað sem aðalkennimerki einingafærslu. Samsetning aðilanúmers, upphafsdagsetningar, stöðu starfsmanns og nafn starfsmanns. |

## <a name="see-also"></a>Sjá einnig

[Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda](hr-admin-integration-ats-api-introduction.md)<br>
[Dæmi um fyrirspurn fyrir umsækjanda til ráðningar](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

