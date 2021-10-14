---
title: Launaupplýsingar fyrir stöður
description: Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir launaupplýsingar fyrir starfsstöðuna í Dynamics 365 Human Resources.
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
ms.openlocfilehash: 76131b6cc7ee58d4a095da4ac56cd97124e42587
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559363"
---
# <a name="payroll-position"></a>Launastaða

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði lýsir einingu launastöðu í Dynamics 365 Human Resources.

Efnislegt heiti: mshr_payrollpositionentity.

### <a name="description"></a>lýsing

Þessi eining veitir upplýsingar tengdar stöðum fyrir tiltekinn starfsmann.

Efnislegt heiti: mshr_payrollpositionentity.

## <a name="properties"></a>Eiginleikar

| Eiginleiki</br>**Efnislegt heiti**</br>**_Gerð_** | Nota | Lýsing |
| --- | --- | --- |
| **Auðkenni stöðuheitis**</br>mshr_positionid</br>*Strengur* | Lesa eingöngu | Auðkenni stöðunnar. |
| **Kenni greiðsluferlis**</br>mshr_paycycleid</br>*Strengur* | Lesa eingöngu | Greiðsluferli sem er skilgreint fyrir stöðuna. |
| **Reglulegar árlegar vinnustundir**</br>annualregularhours</br>*Tugabrot* | Lesa eingöngu | Reglulegar árlegar vinnustundir sem eru skilgreindar fyrir stöðuna. |
| **Greitt af lögaðila**</br>paidbylegalentity</br>*Strengur* | Lesa eingöngu | Lögaðilinn sem er skilgreindur fyrir stöðuna og sem ber ábyrgð á launagreiðslum. |
| **Gildir til**</br>validto</br>*Mótfærð dagsetning og tími* | Lesa eingöngu | Dagsetningin sem upplýsingar um stöðuna gilda til. |
| **Gildir frá**</br>validfrom</br>*Mótfærð dagsetning og tími* | Lesa eingöngu | Dagsetningin sem upplýsingar um stöðuna gilda frá. |
| **Aðalsvæði**</br>mshr_primaryfield</br>*Strengur* | Búið til af kerfi | Aðalreiturinn. |
| **Einingarkenni fyrir upplýsingar um launastöðu**</br>payrollpositiondetailsentityid</br>*Guid* | Krafa</br>Búið til af kerfi. | Altækt einkvæmt kennimerki (GUID-gildi) myndað af kerfinu til að auðkenna stöðu á einkvæman hátt. |

## <a name="relations"></a>Vensl

| Gildi eiginleika | Tengdur aðili | Yfirlitseiginleiki | Tegund innheimtu |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_PayrollPosition |
| _mshr_fk_hcmpositionhierarchy_id_value | mshr_hcmpositionhierarchyentity | mshr_FK_HcmPositionHierarchy_id | Á ekki við |
| _mshr_fk_job_id_value | mshr_payrollpositionjobentity | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_Payroll |
| _mshr_fk_positionassignmentv2_id_value | mshr_hcmpositionworkerassignmentv2entity | mshr_FK_PositionAssignmentV2_id | Á ekki við |

## <a name="example-query"></a>Dæmi um fyrirspurn

**Beiðni**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

**Svar**

```json
{
    "mshr_positionid": "000276",
    "mshr_paycycleid": "w",
    "mshr_annualregularhours": 3000,
    "mshr_paidbylegalentity": "USMF",
    "mshr_validfrom": "2021-03-14T00:00:00Z",
    "mshr_validto": "2154-12-31T00:00:00Z",
    "mshr_primaryfield": "000276 | 3/14/2021",
    "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
    "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>Sjá einnig

[Kynning á API launasamþættingar](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
