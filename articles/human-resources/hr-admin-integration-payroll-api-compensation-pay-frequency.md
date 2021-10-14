---
title: Greiðslutíðni launa
description: Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir greiðslutíðnieiningu launa í Dynamics 365 Human Resources.
author: marcelbf
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b864d0db8ff1b380749b6099fa74a40045932b67
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559656"
---
# <a name="compensation-pay-frequency"></a>Greiðslutíðni launa

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði lýsir greiðslutíðnieiningu launa í Dynamics 365 Human Resources.

Raunlægt heiti: mshr_hcmpayrateconversionentity.

### <a name="description"></a>Lýsing

Þessi eining veitir upplýsingar um umreikning launataxta fyrir tiltekna greiðslutíðni launa.

## <a name="properties"></a>Eiginleikar

| Eiginleiki</br>**Efnislegt heiti**</br>**_Gerð_** | Nota | Lýsing |
| --- | --- | --- |
| **Umreikningur árlegs launataxta**</br>mshr_annualconversionfactor</br>*Tugabrot* | Lesa eingöngu | Árlegur umbreytingarstuðull greiðslutíðni. |
| **Lýsing**</br>mshr_description</br>*Strengur* | Lesa eingöngu | Lýsing á genginu. |
| **Umreikningur launataxta vinnustundar**</br>mshr_hourlyconversionfactor</br>*Tugabrot* | Lesa eingöngu | Umreiknistuðull vinnustundar fyrir greiðslutíðnina. |
| **Umreikningur mánaðarlegs launataxta**</br>mshr_monthlyconversionfactor</br>*Tugabrot* | Lesa eingöngu | Mánaðarlegur umbreytingarstuðull greiðslutíðni. |
| **Umreikningur launataxta**</br>mshr_payrateconversion</br>*Strengur* | Lesa eingöngu | Einstakur strengur til að bera kennsl á taxta umreiknings. |
| **Tímabil**</br>mshr_period</br>*valkostir tímabils* | Lesa eingöngu | Aðaltímabil tiltekins umreiknings launataxta. |
| **Umreikningur vikulegs launataxta**</br>mshr_weeklyconversionfactor</br>*Tugabrot* | Lesa eingöngu | Vikulegur umreiknistuðull fyrir greiðslutíðnina. |
| **Kenni gagnasvæðis**</br>mshr_dataareaid</br>*Strengur* | Lesa eingöngu | Lögaðilinn (fyrirtækið). |
| **Einingarkenni greiðslutíðni launa**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | Búið til af kerfi | Altækt einkvæmt kennimerki (GUID-gildi) myndað af kerfinu til að auðkenna færslu á einkvæman hátt. |

## <a name="example-query-for-payroll-employee"></a>Dæmi um fyrirspurn fyrir starfsmann á launaskrá

**Beiðni**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_hcmpayrateconversionentities?$filter=mshr_payrateconversion eq 'Annual' and mshr_dataareaid eq 'usmf'
```

**Svar**

```json
{
    "mshr_annualconversionfactor": 1,
    "mshr_description": "Annual",
    "mshr_hourlyconversionfactor": 0.0004807692,
    "mshr_monthlyconversionfactor": 0.0833333333,
    "mshr_payrateconversion": "Annual",
    "mshr_period": 200000000,
    "mshr_weeklyconversionfactor": 0.0192307692,
    "mshr_dataareaid": "usmf",
    "mshr_hcmpayrateconversionentityid": "0000056e-0000-0000-b027-fef003000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Sjá einnig

[Kynning á API launasamþættingar](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
