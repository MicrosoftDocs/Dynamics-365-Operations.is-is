---
title: Launafyrirkomulag fastra launa
description: Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir einingu launafyrirkomulags fastra launa í Dynamics 365 Human Resources.
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
ms.openlocfilehash: 227082358c59abddd63f4faa4536a8df270a4d80
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059089"
---
# <a name="payroll-fixed-compensation-plan"></a>Launafyrirkomulag fastra launa

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir einingu launafyrirkomulags fastra launa í Dynamics 365 Human Resources.

## <a name="properties"></a>Eiginleikar

| Eiginleiki<br>**Efnislegt heiti**<br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Kenni starfsmanns**<br>mshr_fk_employee_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Framandlykill:mshr_Employee_id of mshr_payrollemployeeentity entity  | Kenni starfsmanns |
| **Launataxti**<br>mshr_payrate<br>*Tugabrot* | Lesa eingöngu<br>Krafa | Launataxti skilgreindur í launafyrirkomulagi fastra launa. |
| **Kenni áætlunar**<br>mshr_planid<br>*Strengur* | Lesa eingöngu<br>Krafa |Tilgreinir launafyrirkomulagið.  |
| **Gildir frá**<br>mshr_validfrom<br>*Mótfærð dagsetning og tími* |  Lesa eingöngu<br>Krafa |Sú dagsetning sem föst laun starfsmanns gilda frá.  |
| **Eining launafyrirkomulags fastra launa**<br>mshr_payrollfixedcompensationplanentityid<br>*GUID* | Krafa<br>Búið til af kerfi | GUID-gildi myndað af kerfinu til að auðkenna launafyrirkomulag á einkvæman hátt. |
| **Greiðslutíðni**<br>mshr_payfrequency<br>*Strengur* | Lesa eingöngu<br>Krafa |Tíðnin sem starfsmaðurinn fær greitt.  |
| **Gildir til**<br>mshr_validto<br>*Mótfærð dagsetning og tími* | Lesa eingöngu <br>Krafa | Sú dagsetning sem föst laun starfsmanns gilda til. |
| **Auðkenni stöðuheitis**<br>mshr_positionid<br>*Strengur* | Lesa eingöngu <br>Krafa | Auðkenni stöðu sem tengist skráningu starfsmanns og launafyrirkomulags fastra launa. |
| **Gjaldmiðill**<br>mshr_currency<br>*Strengur* | Lesa eingöngu <br>Krafa |Gjaldmiðillinn sem er skilgreindur fyrir launafyrirkomulag fastra launa   |
| **Númer starfsmanns**<br>mshr_personnelnumber<br>*Strengur* | Lesa eingöngu<br>Krafa |Einkvæmt númer starfsmanns.  |

**Fyrirspurn**

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
