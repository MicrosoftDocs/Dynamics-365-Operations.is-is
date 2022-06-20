---
title: Launastöðuvinnsla
description: Þessi grein veitir upplýsingar og dæmi um fyrirspurn fyrir starfseininguna Launastöðu í Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
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
ms.openlocfilehash: fa347f4b99adc7c29d69daf62ad2bbfc14726a19
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864084"
---
# <a name="payroll-position-job"></a>Launastöðuvinnsla


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þessi grein lýsir starfseiningunni launaskrá fyrir Dynamics 365 Human Resources.

### <a name="description"></a>Lýsing

Þessi eining sýnir tengslin milli stöðu og starfs fyrir tiltekið launafyrirkomulag fastra launa.

Efnislegt heiti: mshr_payrollpositionjobentity.

## <a name="properties"></a>Eiginleikar

| Eiginleiki</br>**Efnislegt heiti**</br>**_Gerð_** | Nota | Lýsing |
| --- | --- | --- |
| **Auðkenni stöðuheitis**</br>mshr_positionid</br>*Strengur* | Lesa eingöngu | Auðkenni stöðunnar. |
| **Gildir frá**</br>mshr_validto</br>*Mótfærð dagsetning og tími* | Lesa eingöngu | Dagsetningin sem tengsl stöðu og starfs gildir frá. |
| **Gildir til**</br>mshr_validto</br>*Mótfærð dagsetning og tími* | Lesa eingöngu | Dagsetningin sem tengsl stöðu og starfs gildir til. |
| **Starfsauðkenni**</br>mshr_jobid</br>*Strengur* | Lesa eingöngu | Kenni starfs. |
| **Aðalsvæði**</br>mshr_primaryfield</br>*Strengur* | Búið til af kerfi | Aðalreiturinn. |
| **Einingarkenni fyrir kenni launaeiningar**</br>mshr_payrollpositionjobentityid</br>*Guid* | Búið til af kerfi. | Altækt einkvæmt kennimerki (GUID-gildi) myndað af kerfinu til að auðkenna starf á einkvæman hátt. |

## <a name="relations"></a>Vensl

| Gildi eiginleika | Tengdur aðili | Yfirlitseiginleiki | Tegund innheimtu |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | mshr_payrollfixedcompensationplanentity | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Job |
| _mshr_fk_jobdetail_id_value | mshr_hcmjobdetailentity | mshr_FK_JobDetail_id | Á ekki við |
| _mshr_fk_payroll_id_value | mshr_payrollpositionentity | mshr_FK_Payroll_id | mshr_FK_PayrollPositionEntity_Job |

## <a name="example-query"></a>Dæmi um fyrirspurn

**Beiðni**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionjobentities?$filter=mshr_positionid eq '000276'
```

**Svar**

```json
{
    "mshr_positionid": "000276",
    "mshr_validfrom": "2016-07-06T18:11:33Z",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_jobid": "Accountant",
    "mshr_primaryfield": "000276 | Accountant | 7/6/2016 06:11:33 pm",
    "_mshr_fk_jobdetail_id_value": "00000b8d-0000-0000-b0ff-004105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000058a-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": "00000427-0000-0000-df00-014105000000",
    "mshr_payrollpositionjobentityid": "00000906-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>Sjá einnig

[Kynning á API launasamþættingar](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
