---
title: Launaupplýsingar fyrir stöður
description: Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir launaupplýsingar fyrir starfsstöðuna í Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7b23ac5d11b18c77109be21afe1570755dccba20
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019323"
---
# <a name="payroll-position"></a>Launastaða

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir launaupplýsingar fyrir starfsstöðuna í Dynamics 365 Human Resources.

## <a name="properties"></a>Eiginleikar

| Eiginleiki<br>**Efnislegt heiti**<br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Reglulegar árlegar vinnustundir**<br>annualregularhours<br>*Tugabrot* | Lesa eingöngu<br>Krafa | Reglulegar árlegar vinnustundir skilgreindar fyrir stöðuna.  |
| **Einingarkenni fyrir upplýsingar um launastöðu**<br>payrollpositiondetailsentityid<br>*Guid* | Krafa<br>Búið til af kerfi. | GUID-gildi myndað af kerfinu til að auðkenna stöðu á einkvæman hátt.  |
| **Aðalsvæði**<br>mshr_primaryfield<br>*Strengur* | Krafa<br>Búið til af kerfi |  |
| **Gildi fyrir kenni vinnustöðu**<br>_mshr_fk_positionjob_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Framandlykill:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity |Kenni starfsins sem tengist stöðunni.|
| **Gildi fyrir kenni launafyrirkomulags fastra launa**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | Lesa eingöngu<br>Krafa<br>Framandlykill: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity  | Kenni launafyrirkomulags fastra launa sem tengist stöðunni. |
| **Kenni greiðsluferlis**<br>mshr_primaryfield<br>*Strengur* | Lesa eingöngu<br>Krafa | Greiðsluferli skilgreint fyrir stöðuna. |
| **Greitt af lögaðila**<br>paidbylegalentity<br>*Strengur* | Lesa eingöngu<br>Krafa | Lögaðilinn sem er skilgreindur fyrir stöðuna sem ber ábyrgð á launagreiðslum. |
| **Auðkenni stöðuheitis**<br>mshr_positionid<br>*Strengur* | Lesa eingöngu<br>Krafa | Auðkenni stöðunnar. |
| **Gildir til**<br>validto<br>*Mótfærð dagsetning og tími* | Lesa eingöngu<br>Krafa |Dagsetningin sem upplýsingar um stöðuna gilda frá.  |
| **Gildir frá**<br>validfrom<br>*Mótfærð dagsetning og tími* | Lesa eingöngu<br>Krafa |Dagsetningin sem upplýsingar um stöðuna gilda til.  |

**Fyrirspurn**

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
