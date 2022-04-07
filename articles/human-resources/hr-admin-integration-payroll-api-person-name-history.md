---
title: Ferill einstaklingsheitis
description: Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir ferilseiningu einstaklingsheitis í Dynamics 365 Human Resources.
author: twheeloc
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: db22a602c782cef15b6e5769b9c0726dff158160
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2022
ms.locfileid: "8533599"
---
# <a name="person-name-history"></a>Ferill einstaklingsheitis


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði lýsir ferilseiningu einstaklingsheitis í Dynamics 365 Human Resources.

Raunlægt heiti: mshr_dirpersonnamehistoricalentity.

### <a name="description"></a>Lýsing

Þessi eining veitir upplýsingar um feril heitis fyrir tiltekinn einstakling.

> [!IMPORTANT] 
> Reitirnir **FirstName**, **MiddleName**, **LastName**, **NameValidFrom** og **NameValidTo** eru ekki lengur í boði í launaskráareiningu starfsmanns. Þeir hafa verið fjarlægðir til að tryggja að aðeins einn dagsetningarvirkur gagnagjafi bakki upp þessa einingu.

## <a name="properties"></a>Eiginleikar

| Eiginleiki</br>**Efnislegt heiti**</br>**_Gerð_** | Nota | Lýsing |
| --- | --- | --- |
| **Fornafn**</br>mshr_firstname</br>*Strengur* | Lesa eingöngu | Fornafnið. |
| **Forskeyti eftirnafns**</br>mshr_lastnameprefix</br>*Strengur*) | Lesa eingöngu | Forskeyti eftirnafns. |
| **Eftirnafn**</br>mshr_lastname</br>*Strengur*) | Lesa eingöngu | Eftirnafnið. |
| **Millinafn**</br>mshr_middlename</br>*Strengur*) | Lesa eingöngu | Millinafnið. |
| **Gildir til**</br>mshr_validto</br>*Strengur*) | Lesa eingöngu | Dagsetningin sem nafnið gildir til. |
| **Aðilanúmer**</br>mshr_partynumber</br>*Strengur* | Lesa eingöngu | Einkvæmt notendalesvænt kenni myndað af kerfinu fyrir einstaklinginn. |
| **Aðalsvæði**</br>mshr_primaryfield</br>*Strengur* | Lesa eingöngu | Einkvæmt kenni færslunnar. |
| **Einingarkenni ferils einstaklingsheitis**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | Búið til af kerfi | Altækt einkvæmt kennimerki (GUID-gildi) myndað af kerfinu til að auðkenna færslu á einkvæman hátt. |

## <a name="relations"></a>Vensl

| Gildi eiginleika | Tengdur aðili | Yfirlitseiginleiki | Tegund innheimtu |
| --- | --- | --- | --- |
| Á ekki við | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | Á ekki við | mshr_FK_PayrollEmployeeEntity_Name |

## <a name="example-query-for-payroll-employee"></a>Dæmi um fyrirspurn fyrir starfsmann á launaskrá

**Beiðni**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_dirpersonnamehistoricalentities?$filter=mshr_partynumber eq 'HR000001606'
```

**Svar**

```json
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "middle",
    "mshr_validto": "2021-09-10T21:23:53Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | ",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-c12b-014105000000",
    "mshr_validfrom": null
},
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | 9/10/2021 09:23:54 pm",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-d20b-000010000000",
    "mshr_validfrom": "2021-09-10T21:23:54Z"
}
```

## <a name="see-also"></a>Sjá einnig

[Kynning á API launasamþættingar](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
