---
title: Starfsmaður á launaskrá
description: Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir einingu launastöðu starfsmanns í Dynamics 365 Human Resources.
author: jcart
manager: tfehr
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
ms.openlocfilehash: d3977b758f65875a36749a49459c2a81459a7b69
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882010"
---
# <a name="payroll-employee"></a>Starfsmaður á launaskrá

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir einingu launastöðu starfsmanns í Dynamics 365 Human Resources.

## <a name="properties"></a>Eiginleikar

| Eiginleiki<br>**Efnislegt heiti**<br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Númer starfsmanns**<br>mshr_personnelnumber<br>*Strengur* | Lesa eingöngu<br>Krafa | Einkvæmt númer starfsmanns. |
| **Aðalsvæði**<br>mshr_primaryfield<br>*Strengur* | Krafa<br>Búið til af kerfi |  |
| **Eftirnafn**<br>mshr_lastname<br>*Strengur* | Skrifvarið<br>Krafa | Eftirnafn starfsmanns. |
| **Kenni lögaðila**<br>mshr_legalentityID<br>*Strengur* | Lesa eingöngu<br>Krafa | Tilgreinir lögaðilann (fyrirtækið). |
| **Gildir frá**<br>mshr_namevalidfrom<br>*Mótfærð dagsetning og tími* | Lesa eingöngu <br>Krafa | Dagsetningin sem starfsmannaupplýsingarnar gilda frá.  |
| **Kyn**<br>mshr_gender<br>*Int32* | Lesa eingöngu<br>Krafa | KynKyn starfsmannsins. |
| **Einingarkenni launa starfsmanns**<br>mshr_payrollemployeeentityid<br>*GUID* | Krafa<br>Búið til af kerfi | GUID-gildi myndað af kerfinu til að auðkenna starfsmann á einkvæman hátt. |
| **Upphafsdagur starfs**<br>mshr_employmentstartdate<br>*Mótfærð dagsetning og tími* | Lesa eingöngu<br>Krafa | Upphafsdagsetning starfs starfsmanns. |
| **Kenni auðkennisgerðar**<br>mshr_identificationtypeid<br>*Strengur* |Lesa eingöngu<br>Krafa | Gerð auðkennis sem er skilgreint fyrir starfsmanninn. |
| **Dagsetning starfsloka**<br>mshr_employmentenddate<br>*Mótfærð dagsetning og tími* | Lesa eingöngu<br>Krafa |Starfslok starfsmanns.  |
| **Kenni gagnasvæðis**<br>mshr_dataareaid_id<br>*GUID* | Krafa <br>Búið til af kerfi | Kerfismyndað GUID-gildi sem tilgreinir lögaðilann (fyrirtækið). |
| **Gildir til**<br>mshr_namevalidto<br>*Mótfærð dagsetning og tími* |  Lesa eingöngu<br>Krafa | Dagsetningin sem starfsmannaupplýsingarnar gilda til. |
| **Fæðingardagur**<br>mshr_birthdate<br>*Mótfærð dagsetning og tími* | Lesa eingöngu <br>Krafa | Fæðingardagur starfsmanns |
| **Auðkennisnúmer til**<br>mshr_identificationnumber<br>*Strengur* | Lesa eingöngu <br>Krafa |Auðkennisnúmerið sem er skilgreint fyrir starfsmanninn.  |
| **Fornafn**<br>mshr_firstname<br>*Strengur* | Lesa eingöngu<br>Krafa | Fornafn starfsmanns. |
| **Millinafn**<br>mshr_middlename<br>*Strengur* | Lesa eingöngu<br>Krafa |Millinafn starfsmanns.  |

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
            "mshr_firstname": "Cassie",
            "mshr_middlename": "Lassie",
            "mshr_lastname": "Hicks",
            "mshr_namevalidfrom": "2021-03-12T20:34:25Z",
            "mshr_namevalidto": "2154-12-31T23:59:59Z",
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
