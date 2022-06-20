---
title: Launafyrirkomulag breytilegra launa
description: Þessi grein veitir upplýsingar og dæmi um fyrirspurn fyrir eininguna Launaskrá breytilega bótaáætlun í Dynamics 365 Human Resources.
author: twheeloc
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-06-15
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5c6190084c3f1ce15d6a4ab8f13843a5da801dd3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868131"
---
# <a name="payroll-variable-compensation-plan"></a>Launafyrirkomulag breytilegra launa


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þessi grein lýsir einingunni Launaskrá breytileg bótaáætlun fyrir Dynamics 365 Human Resources.

### <a name="description"></a>lýsing

Þessi eining býður upp á launafyrirkomulag breytilegra launa sem úthlutað er fyrir uppgefna stöðu starfsmanns.

Efnislegt heiti: mshr_payrollvariablecompensationawardentity.

## <a name="properties"></a>Eiginleikar

| Eiginleiki</br>**Efnislegt heiti**</br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Númer starfsmanns**</br>mshr_personnelnumber</br>*Strengur* | Lesa eingöngu | Einkvæmt númer starfsmanns.  |
| **Dagsetning umbunar**</br>mshr_awarddate</br>*Mótfærð dagsetning og tími* | Lesa eingöngu | Dagsetning umbunar. |
| **Tegund umbunar**</br>mshr_awardtype</br>*[Valmöguleikar mshr_HrmCompVarAwardEmplType](hr-admin-integration-payroll-api-award-type.md)* | Lesa eingöngu | Gerð umbunar sem er skilgreind fyrir launafyrirkomulag breytilegra launa. |
| **Gjaldmiðill**</br>mshr_unitcurrencycode</br>*Strengur* | Lesa eingöngu |Gjaldmiðillinn sem er skilgreindur fyrir launafyrirkomulag breytilegra launa.   |
| **Auðkenni fyrirkomulags fastra launa**</br>mshr_fixedplanid</br>*Strengur* | Lesa eingöngu | Launafyrirkomulag fastra launa sem er notað sem grunnur fyrir útreikninga umbunar. |
| **Einingargildi**</br>mshr_awardamount</br>*Tugabrot* | Lesa eingöngu | Gildi einingarinnar |
| **Gerð ferlis**</br>mshr_processtype</br>*[Valmöguleikar mshr_hrmCompProcessType](hr-admin-integration-payroll-api-process-type.md)* | Lesa eingöngu | Gerð ferlis. |
| **Gerð launafyrirkomulags breytilegra launa**</br>Strengur</br>*mshr_typeid* | Lesa eingöngu | Gerð launafyrirkomulags breytilegra launa. |
| **Auðkenni launafyrirkomulags breytilegra launa**</br>Strengur</br>*mshr_planid* | Lesa eingöngu | Auðkenni launafyrirkomulags breytilegra launa. |
| **Fjöldi eininga**</br>Tugabrot</br>*mshr_numberofunits* | Lesa eingöngu | Einingafjöldi umbunar. |
| **Aðalsvæði**</br>mshr_primaryfield</br>*GUID* | Lesa eingöngu</br>Búið til af kerfi. | |
| **Eining launafyrirkomulags breytilegra launa**</br>mshr_payrollvariablecompensationawardentityid</br>*GUID* | Búið til af kerfi | GUID-gildi myndað af kerfinu til að auðkenna launafyrirkomulag á einkvæman hátt. |

## <a name="relations"></a>Vensl 

|Gildi eiginleika | Tengdur aðili | Yfirlitseiginleiki | Tegund innheimtu |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Employee_id | mshr_FK_PayrollEmployeeEntity_VariableCompAward |
| _mshr_fk_fixedcomp_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedComp_id | mshr_FK_PayrollFixedCompensationPlanEntity_VariableCompAward |

## <a name="example-query"></a>Dæmi um fyrirspurn

**Beiðni**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollvariablecompensationawardentities?$filter=mshr_personnelnumber eq '000046'
```

**Svar**

```json
{
    "mshr_personnelnumber": "000046",
    "mshr_awarddate": "2015-01-15T00:00:00Z",
    "mshr_awardtype": 200000000,
    "mshr_unitcurrencycode": "USD",
    "mshr_fixedplanid": "",
    "mshr_unitvalue": 1,
    "mshr_processtype": 200000003,
    "mshr_typeid": "Bonus",
    "mshr_planid": "MgBonus",
    "mshr_numberofunits": 1500,
    "mshr_primaryfield": "000046 | MgBonus | Bonus | 1/15/2015",
    "_mshr_fk_employee_id_value": "00000666-0000-0000-daff-004105000000",
    "mshr_payrollvariablecompensationawardentityid": "000001a4-0000-0000-0d00-005001000000",
    "_mshr_fk_fixedcomp_id_value": null
}
```

## <a name="see-also"></a>Sjá einnig

[Kynning á API launasamþættingar](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
