---
title: Starfsmaður á launaskrá
description: Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir einingu launastöðu starfsmanns í Dynamics 365 Human Resources.
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
ms.openlocfilehash: 20e74e97f98d0bc0fd454d54cbf969d4f1b46c7c98b2949b0ed8cfe671312dd2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768192"
---
# <a name="payroll-employee"></a>Starfsmaður á launaskrá

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði lýsir starfsmannaeiningu launaskrár fyrir Dynamics 365 Human Resources.

Efnislegt heiti: mshr_payrollemployeeentity.

### <a name="description"></a>lýsing

Þessi eining veitir upplýsingar um starfsmanninn. Stilla þarf [samþættingarfæribreytur launaskrár](hr-admin-integration-payroll-api-parameters.md) áður en þessi eining er notuð.

>[!IMPORTANT] 
>Reitirnir **FirstName**, **MiddleName**, **LastName**, **NameValidFrom** og **NameValidTo** eru ekki lengur í boði í þessari einingu. Þetta tryggir að það er aðeins ein dagsetning fyrir skilvirka gagnasöfnun sem bakkar þennan aðila.
>Þessir reitir verða tiltækir í **DirPersonNameHistoricalEntity**, sem var gefið út í verkvangsuppfærslu 43. Það eru OData-tengsl frá **PayrollEmployeeEntity** til **DirPersonNameHistoricalEntity** í reitnum **Einstaklingur**. 

## <a name="properties"></a>Eiginleikar

| Eiginleiki<br>**Efnislegt heiti**<br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Númer starfsmanns**<br>mshr_personnelnumber<br>*Strengur* | Lesa eingöngu | Einkvæmt númer starfsmanns. |
| **Aðalsvæði**<br>mshr_primaryfield<br>*Strengur* | Lesa eingöngu<br>Búið til af kerfi |  |
| **Kenni lögaðila**<br>mshr_legalentityID<br>*Strengur* | Lesa eingöngu | Tilgreinir lögaðilann (fyrirtækið). |
| **Kyn**<br>mshr_gender<br>[Valkostir mshr_hcmpersongender](hr-admin-integration-payroll-api-gender.md) | Lesa eingöngu | KynKyn starfsmannsins. |
| **Einingarkenni launa starfsmanns**<br>mshr_payrollemployeeentityid<br>*GUID* | Krafa<br>Búið til af kerfi | GUID-gildi myndað af kerfinu til að auðkenna starfsmann á einkvæman hátt. |
| **Upphafsdagur starfs**<br>mshr_employmentstartdate<br>*Mótfærð dagsetning og tími* | Lesa eingöngu | Upphafsdagsetning starfs starfsmanns. |
| **Kenni auðkennisgerðar**<br>mshr_identificationtypeid<br>*Strengur* |Lesa eingöngu | Gerð auðkennis sem er skilgreint fyrir starfsmanninn. |
| **Dagsetning starfsloka**<br>mshr_employmentenddate<br>*Mótfærð dagsetning og tími* | Lesa eingöngu |Starfslok starfsmanns.  |
| **Kenni gagnasvæðis**<br>mshr_dataareaid_id<br>*GUID* | Lesa eingöngu <br>Búið til af kerfi | Kerfismyndað GUID-gildi sem tilgreinir lögaðilann (fyrirtækið). |
| **Gildir til**<br>mshr_namevalidto<br>*Mótfærð dagsetning og tími* |  Lesa eingöngu | Dagsetningin sem starfsmannaupplýsingarnar gilda til. |
| **Fæðingardagur**<br>mshr_birthdate<br>*Mótfærð dagsetning og tími* | Lesa eingöngu | Fæðingardagur starfsmanns |
| **Auðkennisnúmer til**<br>mshr_identificationnumber<br>*Strengur* | Lesa eingöngu |Auðkennisnúmerið sem er skilgreint fyrir starfsmanninn.  |

## <a name="example-query-for-payroll-employee"></a>Dæmi um fyrirspurn fyrir starfsmann á launaskrá

**Beiðni**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_identificationtypeid eq @idtype and mshr_namevalidfrom le @asofdate and mshr_namevalidto ge @asofdate&@personnelnumber='000041'&@idtype='SSN'&@asofdate=2021-04-01
```

**Svar**

```json
{
    "mshr_legalentityid": "USMF",
    "mshr_personnelnumber": "000041",
    "mshr_employmentstartdate": "2011-04-05T07:00:00Z",
    "mshr_employmentenddate": "2154-12-31T23:59:59Z",
    "mshr_birthdate": "1987-09-12T00:00:00Z",
    "mshr_gender": 200000002,
    "mshr_identificationtypeid": "SSN",
    "mshr_identificationnumber": "888-99-9342",
    "mshr_dataareaid": "USMF",
    "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
    "_mshr_fk_worker_id_value": "000000ad-0000-0000-d5ff-004105000000",
    "_mshr_fk_employment_id_value": "00000d0d-0000-0000-0600-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
    "mshr_payrollemployeeentityid": "00000d3c-0000-0000-d5ff-004105000000",
    "_mshr_dataareaid_id_value": null
}
```
## <a name="see-also"></a>Sjá einnig

[Kynning á API launasamþættingar](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
