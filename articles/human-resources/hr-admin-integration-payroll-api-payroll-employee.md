---
title: Starfsmaður á launaskrá
description: Þessi grein veitir upplýsingar og dæmi um fyrirspurn fyrir starfseininguna launaskrá í Dynamics 365 Human Resources.
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
ms.openlocfilehash: b07fbc76b997600b2c076c00a63d1f6d865326d0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872211"
---
# <a name="payroll-employee"></a>Starfsmaður á launaskrá


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þessi grein lýsir starfseiningunni launaskrá fyrir Dynamics 365 Human Resources.

Efnislegt heiti: mshr_payrollemployeeentity.

### <a name="description"></a>lýsing

Þessi eining veitir upplýsingar um starfsmanninn. Stilla þarf [samþættingarfæribreytur launaskrár](hr-admin-integration-payroll-api-parameters.md) áður en þessi eining er notuð.

>[!IMPORTANT] 
>Reitirnir **FirstName**, **MiddleName**, **LastName**, **NameValidFrom** og **NameValidTo** eru ekki lengur í boði í þessari einingu. Þetta tryggir að það er aðeins ein dagsetning fyrir skilvirka gagnasöfnun sem bakkar þennan aðila.
>Þessir reitir verða tiltækir í **DirPersonNameHistoricalEntity**, sem var gefið út í verkvangsuppfærslu 43. Það eru OData-tengsl frá **PayrollEmployeeEntity** til **DirPersonNameHistoricalEntity**. 

## <a name="properties"></a>Eiginleikar

| Eiginleiki</br>**Efnislegt heiti**</br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Kenni lögaðila**</br>mshr_legalentityID</br>*Strengur* | Lesa eingöngu | Tilgreinir lögaðilann (fyrirtækið). |
| **Númer starfsmanns**</br>mshr_personnelnumber</br>*Strengur* | Lesa eingöngu | Einkvæmt númer starfsmanns. |
| **Upphafsdagur starfs**</br>mshr_employmentstartdate</br>*Mótfærð dagsetning og tími* | Lesa eingöngu | Upphafsdagsetning starfs starfsmanns. |
| **Dagsetning starfsloka**</br>mshr_employmentenddate</br>*Mótfærð dagsetning og tími* | Lesa eingöngu |Starfslok starfsmanns.  |
| **Fæðingardagur**</br>mshr_birthdate</br>*Mótfærð dagsetning og tími* | Lesa eingöngu | Fæðingardagur starfsmanns. |
| **Kyn**</br>mshr_gender</br>[Valkostir mshr_hcmpersongender](hr-admin-integration-payroll-api-gender.md) | Lesa eingöngu | KynKyn starfsmannsins. |
| **Starfsgerð**</br>mshr_employmenttype</br>[Valmöguleikar mshr_hcmemploymenttype](hr-admin-integration-payroll-api-hcmemploymenttype.md) | Lesa eingöngu | Starfsgerðin. |
| **Kenni auðkennisgerðar**</br>mshr_identificationtypeid</br>*Strengur* |Lesa eingöngu | Gerð auðkennis sem er skilgreint fyrir starfsmanninn. |
| **Auðkennisnúmer til**</br>mshr_identificationnumber</br>*Strengur* | Lesa eingöngu |Auðkennisnúmerið sem er skilgreint fyrir starfsmanninn. |
| **Tilbúið til greiðslu**</br>mshr_readytopay</br>[Safn valkosta mshr_noyes](hr-admin-integration-payroll-api-no-yes.md) | Lesa eingöngu | Gefur til kynna ef starfsmaðurinn er merktur sem tilbúinn til að greiða. |
| **Einingarkenni launa starfsmanns**</br>mshr_payrollemployeeentityid</br>*GUID* | Búið til af kerfi | Altækt einkvæmt kennimerki (GUID-gildi) myndað af kerfinu til að auðkenna starfsmann á einkvæman hátt. |

## <a name="relations"></a>Vensl

|Gildi eiginleika | Tengdur aðili | Yfirlitseiginleiki | Tegund innheimtu |
| --- | --- | --- | --- |
| _mshr_fk_employment_id_value | mshr_hcmemploymentdetailentity | mshr_FK_Employment_id | mshr_FK_HcmEmploymentDetailEntity_PayrollEmployee |
| _mshr_fk_fixedcompplan_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Employee |
| _mshr_fk_name_id_value | mshr_dirpersonnamehistoricalentity | mshr_FK_Name_id | - |
| _mshr_fk_worker_id_value | mshr_hcmworkerbaseentity | mshr_FK_Worker_id | mshr_FK_HcmWorkerBaseEntity_PayrollEmployee |
| _mshr_fk_workerbankaccount_id_value | mshr_hcmworkerbankaccountentity | mshr_FK_WorkerBankAccount_id | mshr_FK_HcmWorkerBankAccountEntity_PayrollEmployee |
| _mshr_fk_variablecompaward_id_value | [mshr_payrollvariablecompensationawardentity](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_Employee |
| _mshr_fk_address_id_value | [mshr_payrollworkeraddressentity](hr-admin-integration-payroll-api-payroll-worker-address.md) | mshr_FK_Address_id | mshr_FK_PayrollWorkerAddressEntity_Worker |

## <a name="example-query-for-payroll-employee"></a>Dæmi um fyrirspurn fyrir starfsmann á launaskrá

**Beiðni**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq '000041'
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
    "mshr_employmenttype": 200000000,
    "mshr_identificationtypeid": "SSN",
    "mshr_identificationnumber": "888-99-9342",
    "mshr_readytopay": 200000000,
    "mshr_dataareaid": "USMF",
    "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
    "_mshr_fk_employment_id_value": "00000d4e-0000-0000-0600-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "00000598-0000-0000-4cd0-fda002000000",
    "_mshr_fk_name_id_value": "00000832-0000-0000-d700-014105000000",
    "_mshr_fk_worker_id_value": "000000af-0000-0000-d5ff-004105000000",
    "_mshr_fk_workerbankaccount_id_value": "000006f2-0000-0000-b7ff-004105000000",
    "mshr_payrollemployeeentityid": "00000666-0000-0000-d5ff-004105000000",
    "_mshr_fk_address_id_value": null,
    "_mshr_fk_variablecompaward_id_value": null,
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Sjá einnig

[Kynning á API launasamþættingar](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
