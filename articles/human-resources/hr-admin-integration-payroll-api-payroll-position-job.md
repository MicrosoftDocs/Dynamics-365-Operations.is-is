---
title: Launastöðuvinnsla
description: Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir starfseiningu launastöðu í Dynamics 365 Human Resources.
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
ms.openlocfilehash: 842c459acd8b5e1a8b6074243b3afa18dc6a13c5
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314238"
---
# <a name="payroll-position-job"></a>Launastöðuvinnsla

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði lýsir starfseiningu launastöðu fyrir Dynamics 365 Human Resources.

### <a name="description"></a>lýsing

Þessi eining sýnir tengslin milli stöðu og starfs fyrir tiltekið launafyrirkomulag fastra launa.

Efnislegt heiti: mshr_payrollpositionjobentity.

## <a name="properties"></a>Eiginleikar

| Eiginleiki<br>**Efnislegt heiti**<br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Starfsauðkenni**<br>mshr_jobid<br>*Strengur* | Lesa eingöngu<br>Krafa |Kenni starfs. |
| **Gildir frá**<br>mshr_validto<br>*Mótfærð dagsetning og tími* | Lesa eingöngu <br>Krafa | Dagsetningin sem tengsl stöðu og starfs gildir frá. |
| **Gildir til**<br>mshr_validto<br>*Mótfærð dagsetning og tími* | Lesa eingöngu <br>Krafa | Dagsetningin sem staðan og starfssambandið gildir til.  |
| **Auðkenni stöðuheitis**<br>mshr_positionid<br>*Strengur* | Lesa eingöngu<br>Krafa | Auðkenni stöðunnar. |
| **Aðalsvæði**<br>mshr_primaryfield<br>*Strengur* | Krafa<br>Búið til af kerfi |  |
| **Gildi fyrir kenni vinnustöðu**<br>_mshr_fk_positionjob_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Framandlykill:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity |Kenni starfsins sem tengist stöðunni.|
| **Gildi fyrir kenni launafyrirkomulags fastra launa**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Framandlykill: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity  | Kenni launafyrirkomulags fastra launa sem tengist stöðunni. |
| **Einingarkenni fyrir kenni launaeiningar**<br>mshr_payrollpositionjobentityid<br>*Guid* | Krafa<br>Búið til af kerfi. | GUID-gildi myndað af kerfinu til að auðkenna verk á einkvæman hátt.  |

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
