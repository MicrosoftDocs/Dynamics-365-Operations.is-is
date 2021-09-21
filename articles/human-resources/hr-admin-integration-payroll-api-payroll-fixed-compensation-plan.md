---
title: Launafyrirkomulag fastra launa
description: Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir einingu launafyrirkomulags fastra launa í Dynamics 365 Human Resources.
author: jcart
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dcb253fabbb183003048119c7a627bf0ab960050
ms.sourcegitcommit: 4d11061f5de0ddba1f968bd5c3fd694a8b104ccc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/26/2021
ms.locfileid: "7429231"
---
# <a name="payroll-fixed-compensation-plan"></a>Launafyrirkomulag fastra launa

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði lýsir einingu fyrir launafyrirkomulag fastra launa fyrir Dynamics 365 Human Resources.

### <a name="description"></a>lýsing

Þessi eining býður upp á áætlun vegna launafyrirkomulags fastra launa fyrir uppgefna stöðu starfsmanns.

Efnislegt heiti: mshr_payrollfixedcompensationplanentity.

## <a name="properties"></a>Eiginleikar

| Eiginleiki</br>**Efnislegt heiti**</br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Kenni áætlunar**</br>mshr_planid</br>*Strengur* | Lesa eingöngu | Tilgreinir launafyrirkomulagið.  |
| **Númer starfsmanns**</br>mshr_personnelnumber</br>*Strengur* | Lesa eingöngu | Einkvæmt númer starfsmanns. |
| **Launataxti**</br>mshr_payrate</br>*Tugabrot* | Lesa eingöngu | Launataxti skilgreindur í launafyrirkomulagi fastra launa. |
| **Auðkenni stöðuheitis**</br>mshr_positionid</br>*Strengur* | Lesa eingöngu | Auðkenni stöðu sem tengist skráningu starfsmanns og launafyrirkomulags fastra launa. |
| **Gildir frá**</br>mshr_validfrom</br>*Mótfærð dagsetning og tími* |  Lesa eingöngu | Sú dagsetning sem föst laun starfsmanns gilda frá.  |
| **Gildir til**</br>mshr_validto</br>*Mótfærð dagsetning og tími* | Lesa eingöngu | Sú dagsetning sem föst laun starfsmanns gilda til. |
| **Greiðslutíðni**</br>mshr_payfrequency</br>*Strengur* | Lesa eingöngu | Tíðnin sem starfsmaðurinn fær greitt.  |
| **Gjaldmiðill**</br>mshr_currency</br>*Strengur* | Lesa eingöngu | Gjaldmiðillinn sem er skilgreindur fyrir launafyrirkomulag fastra launa. |
| **Eining launafyrirkomulags fastra launa**</br>mshr_payrollfixedcompensationplanentityid</br>*GUID* | Búið til af kerfi | GUID-gildi myndað af kerfinu til að auðkenna launafyrirkomulag á einkvæman hátt. |

## <a name="relations"></a>Vensl

|Gildi eiginleika | Tengdur aðili | Yfirlitseiginleiki | Tegund innheimtu |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Employee_id | mshr_FK_PayrollEmployeeEntity_FixedCompPlan |
| _mshr_fk_job_id_value | [mshr_payrollpositionjobentity](hr-admin-integration-payroll-api-payroll-position-job.md) | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_FixedCompPlan |
| _mshr_fk_payrollposition_id_value | [mshr_payrollpositionentity](hr-admin-integration-payroll-api-payroll-position.md) | mshr_FK_PayrollPosition_id | mshr_FK_PayrollPositionEntity_FixedCompPlan |
| _mshr_fk_plan_id_value | mshr_hcmcompfixedplantableentity | mshr_FK_Plan_id | - |
| _mshr_fk_variablecompaward_id_value | [mshr_payrollvariablecompensationawardentity](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_FixedComp |

## <a name="example-query"></a>Dæmi um fyrirspurn

**Beiðni**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**Svar**

```json
{
    "mshr_planid": "GradeC",
    "mshr_personnelnumber": "000041",
    "mshr_payrate": 75200,
    "mshr_positionid": "000276",
    "mshr_validfrom": "2011-04-05T00:00:00Z",
    "mshr_validto": "2154-12-31T00:00:00Z",
    "mshr_payfrequency": "Annual",
    "mshr_currency": "USD",
    "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
    "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
    "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": null
}
```

## <a name="see-also"></a>Sjá einnig

[Kynning á API launasamþættingar](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
