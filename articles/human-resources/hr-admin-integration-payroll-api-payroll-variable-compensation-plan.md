---
title: Launafyrirkomulag breytilegra launa
description: Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir einingu launafyrirkomulags breytilegra launa í Dynamics 365 Human Resources.
author: marcelbf
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-15
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5dc096c08ed808f577c8cdc96ca84000a0b80679
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314410"
---
# <a name="payroll-variable-compensation-plan"></a>Launafyrirkomulag breytilegra launa

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði lýsir einingu fyrir launafyrirkomulag breytilegra launa fyrir Dynamics 365 Human Resources.

### <a name="description"></a>lýsing

Þessi eining býður upp á launafyrirkomulag breytilegra launa sem úthlutað er fyrir uppgefna stöðu starfsmanns.

Efnislegt heiti: mshr_payrollvariablecompensationawardentity.

## <a name="properties"></a>Eiginleikar

| Eiginleiki</br>**Efnislegt heiti**</br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Númer starfsmanns**</br>mshr_personnelnumber</br>*Strengur* | Lesa eingöngu</br>Krafa |Einkvæmt númer starfsmanns.  |
| **Dagsetning umbunar**</br>mshr_awarddate</br>*Mótfærð dagsetning og tími* | Lesa eingöngu</br>Krafa | Dagsetning umbunar. |
| **Tegund umbunar**</br>mshr_awardtype</br>*[Valmöguleikar mshr_HrmCompVarAwardEmplType](hr-admin-integration-payroll-api-award-type.md)* | Lesa eingöngu</br>Krafa | Gerð umbunar sem er skilgreind fyrir launafyrirkomulag breytilegra launa. |
| **Gjaldmiðill**</br>mshr_unitcurrencycode</br>*Strengur* | Lesa eingöngu </br>Krafa |Gjaldmiðillinn sem er skilgreindur fyrir launafyrirkomulag breytilegra launa.   |
| **Auðkenni fyrirkomulags fastra launa**</br>mshr_fixedplanid</br>*Strengur* | Lesa eingöngu | Launafyrirkomulag fastra launa sem er notað sem grunnur fyrir útreikninga umbunar. |
| **Einingargildi**</br>mshr_awardamount</br>*Tugabrot* | Lesa eingöngu | Gildi einingarinnar |
| **Gerð ferlis**</br>mshr_processtype</br>*[Valmöguleikar mshr_hrmCompProcessType](hr-admin-integration-payroll-api-process-type.md)* | Lesa eingöngu | Gerð ferlis. |
| **Gerð launafyrirkomulags breytilegra launa**</br>Strengur</br>*mshr_typeid* | Lesa eingöngu | Gerð launafyrirkomulags breytilegra launa. |
| **Auðkenni launafyrirkomulags breytilegra launa**</br>Strengur</br>*mshr_planid* | Lesa eingöngu | Auðkenni launafyrirkomulags breytilegra launa. |
| **Aðalsvæði**</br>mshr_primaryfield</br>*GUID* | Lesa eingöngu</br>Búið til af kerfi. | |
| **Kenni starfsmanns**</br>mshr_fk_employee_id_value</br>*GUID* | Lesa eingöngu</br>Krafa</br>Framandlykill:mshr_Employee_id of mshr_payrollemployeeentity entity  | Kenni starfsmanns. |
| **Eining launafyrirkomulags breytilegra launa**</br>mshr_payrollvariablecompensationawardentityid</br>*GUID* | Krafa</br>Búið til af kerfi | GUID-gildi myndað af kerfinu til að auðkenna launafyrirkomulag á einkvæman hátt. |


## <a name="example-query"></a>Dæmi um fyrirspurn

**Beiðni**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollvariablecompensationawardentities?$filter=mshr_personnelnumber eq '000001'
```

**Svar**

```json
{
    "mshr_personnelnumber": "000001",
    "mshr_awarddate": "2015-01-15T00:00:00Z",
    "mshr_awardtype": 200000000,
    "mshr_unitcurrencycode": "USD",
    "mshr_fixedplanid": "",
    "mshr_awardamount": 1,
    "mshr_processtype": 200000003,
    "mshr_typeid": "Bonus",
    "mshr_planid": "MgBonus",
    "mshr_primaryfield": "000001 | MgBonus | Bonus | 1/15/2015",
    "_mshr_fk_employee_id_value": "00000655-0000-0000-adff-004105000000",
    "mshr_payrollvariablecompensationawardentityid": "000001a1-0000-0000-adff-004105000000",
    "_mshr_fk_fixedcomp_id_value": null
}
```

## <a name="see-also"></a>Sjá einnig

[Kynning á API launasamþættingar](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
