---
title: Skoðunargerðir
description: Þetta efnisatriði lýsir einingu skoðunargerðar fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: d3a45d802ab6b574338a09e77d432357cb9df507
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465919"
---
# <a name="screening-types"></a>Skoðunargerðir

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði lýsir einingu skoðunargerðar fyrir Dynamics 365 Human Resources.

Raunlægt heiti: mshr_hcmscreeningtypeentity

## <a name="description"></a>lýsing

Þessi eining lýsir skoðunargerðum sem settar eru upp af fyrirtækinu á undan ráðningu og fyrir yfirstandandi skoðunarferli starfsmanns.

## <a name="json-representation"></a>JSON-framsetning

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a>Eiginleikar

| Eiginleiki<br>**Efnislegt heiti**<br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Kenni fyrir einingu skoðunargerðar**<br>mshr_hcmscreeningtypeentityid<br>*GUID* | Lesa eingöngu<br>Krafa<br>Myndað af kerfinu | Einkvæmt aðalkenni fyrir færslu skoðunargerðar. |
| **Kenni skoðunargerðar**<br>mshr_screeningtypeid<br>*Strengur* | Lesa/skrifa<br>Krafa | Notandaskilgreint einkvæmt kenni fyrir skoðunargerðina. |
| **Lýsing**<br>mshr_description<br>*Strengur* | Lesa/skrifa<br>Krafa | Lýsing á skoðunargerðinni. |
| **Tíðnieining**<br>mshr_frequencyunit<br>*mshr_hcmfrequencyunit valkostur stilltur* | Lesa/skrifa<br>Krafa | Lýsir því hversu fljótt þarf að ljúka skoðun fyrir úthlutaðan einstakling. |
| **Mynda úr**<br>mshr_generatefrom<br>*mshr_hcmfrequencygeneratefrom valkostur stilltur* | Lesa-skrifa<br>Krafa | Ef tíðnigildið er eitthvað annað gildi en „Aðeins einu sinni“, ákvarðar GenerateForm-gildið dagsetninguna þegar á reikna út næsta skoðunartilvik. |
| **Tímabil**<br>mshr_frequencyinterval<br>*Heiltala* | Lesa-skrifa<br>Krafa | Ef tíðnigildið er eitthvað annað gildi en „Aðeins einu sinni“ þarf að skilgreina tímabil fyrir tímaeiningar á milli skoðunartilvika. |

## <a name="see-also"></a>Sjá einnig

[Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda](hr-admin-integration-ats-api-introduction.md)<br>
[Dæmi um fyrirspurn fyrir umsækjanda til ráðningar](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]