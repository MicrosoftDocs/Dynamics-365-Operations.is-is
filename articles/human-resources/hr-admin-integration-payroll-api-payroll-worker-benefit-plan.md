---
title: Fríðindaáætlun starfskrafts á launaskrá
description: Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir einingu fríðindaáætlunar fyrir starfskraft á launaskrá í Dynamics 365 Human Resources.
author: marcelbf
ms.date: 07/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0837d9a153aba554d0a5293d16afb309bd37963c270da5b67e691558cae63b0a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758713"
---
# <a name="payroll-worker-benefit-plan"></a>Fríðindaáætlun starfskrafts á launaskrá

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði lýsir einingu fyrir fríðindaáætlun starfskrafts fyrir Dynamics 365 Human Resources.

Efnislegt heiti: mshr_payrollworkerbenefitplanentities.

### <a name="description"></a>lýsing

Þessi aðili veitir upplýsingar um fríðindaáætlun fyrir tiltekinn starfsmann.

## <a name="properties"></a>Eiginleikar

| Eiginleiki</br>**Efnislegt heiti**</br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Númer starfsmanns**</br>mshr_personnelnumber</br>*Strengur* | Lesa eingöngu</br>Krafa | Einkvæmt númer starfsmanns. |
| **Kenni lögaðila**</br>mshr_legalentityID</br>*Strengur* | Lesa eingöngu | Tilgreinir lögaðilann (fyrirtækið). |
| **Kenni tímabils**</br>mshr_periodid</br>*Strengur* | Lesa eingöngu | Kenni tímabilsins. |
| **Kenni áætlunar**</br>mshr_planid</br>*Strengur* | Lesa eingöngu | Kenni áætlunarinnar. |
| **Tryggingarvalkostur**</br>mshr_coverageoptionid</br>*Strengur* | Lesa eingöngu | Kenni tryggingarvalkostar. |
| **Upphafsdagur frádráttar**</br>mshr_deductionstartdatetime</br>*Mótfærð dagsetning og tími* | Lesa eingöngu | Upphafsdagur frádráttar. |
| **Lokadagsetning frádráttar**</br>mshr_deductionenddatetime</br>*Mótfærð dagsetning og tími* | Lesa eingöngu | Lokadagsetning frádráttar. |
| **Staða**</br>mshr_status</br>*[Stöðuvalkostir fyrir fríðindaáætlun starfsmanns](hr-admin-integration-payroll-api-benefit-employee-plan-status.md)* | Lesa eingöngu | Staða fyrir fríðindaáætlun. |
| **Gildir frá**</br>mshr_validfrom</br>*Mótfærð dagsetning og tími* | Lesa eingöngu | Tíminn þegar þessi færsla tekur gildi. |
| **Gildir til**</br>mshr_validto</br>*Mótfærð dagsetning og tími* |  Lesa eingöngu | Tíminn sem þessi færsla gildir til. |
| **Kenni áætlunargerðar**</br>mshr_plantypeid</br>*Strengur* | Lesa eingöngu | Kenni áætlunargerðarinnar. |
| **Gerð kóða áætlunargerðar**</br>mshr_plantypecode</br>*[tryggingarvalkostir gerðar fríðindaáætlunar](hr-admin-integration-payroll-api-benefit-plan-type-cover.md)* | Lesa eingöngu | Nákvæmni áætlanagerðar. |
| **Fjöldi launatímabila**</br>mshr_payperiod</br>*Heiltala* | Lesa eingöngu | Fjöldi launatímabila sem táknar hversu oft bætur veitendur eða starfsmenn eru greiddir. Þessi upphæð er notuð til að reikna út árlega upphæð fríðinda starfsmannsins. |
| **Upphæð starfsmanns**</br>mshr_amountemployee</br>*Tugabrot* | Lesa eingöngu | Upphæð eða prósentuhlutfall starfsmanns. |
| **Upphæð vinnuveitanda**</br>mshr_amountemployer</br>*Tugabrot* | Lesa eingöngu | Upphæð eða prósentuhlutfall vinnuveitanda. |
| **Aðalsvæði**</br>mshr_primaryfield</br>*Strengur* | Búið til af kerfi | Aðalsvæði. |
| **Gildi kennis starfskrafts** </br>_mshr_fk_worker_id_value</br>*GUID* | Framandlykill: mshr_hcmworkerbaseentityid of mshr_hcmworkerbaseentity eining. | Einkvæmt kerfismyndað kenni fyrir starfskraftinn. |
| **Gildi fyrir kenni tímabils**</br> _mshr_fk_period_id_value</br>*GUID* | Framandlykill: mshr_benefitperiodentityid of mshr_benefitperiodentity eining. | Einkvæmt kerfismyndað kenni fyrir tímabilið. |
| **Gildi fyrir auðkenni einstaklings**</br> _mshr_fk_plan_id_value</br>*GUID* | Framandlykill: mshr_benefitplanentityid of mshr_benefitplanentity eining. | Einkvæmt kerfismyndað kenni fyrir áætlunina. |
| **Gildi fyrir kenni áætlanagerðar**</br> _mshr_fk_plantype_id_value</br>*GUID* | Framandlykill: mshr_benefitplantypeentityid of mshr_benefitplantypeentity eining. | Einkvæmt kerfismyndað kenni fyrir áætlunina. |
| **Gildi kennis fyirr tryggingarvalkost**</br> _mshr_fk_coverageoption_id_value</br>*GUID* | Framandlykill: mshr_benefitcoverageoptionentityid of mshr_benefitcoverageoptionentity eining. | Einkvæmt kerfismyndað kenni fyrir áætlunina. |
| **Gildi einingarkennis fríðindaáætlunar starfskrafts á launaskrá**</br> mshr_payrollworkerbenefitplanentityid</br>*GUID* | Lesa eingöngu </br> Búið til af kerfi | Einkvæmt kerfismyndað kenni fyrir færsluna. |

## <a name="example-query-for-payroll-worker-benefit-plan"></a>Dæmi um fyrirspurn fyrir fríðindaáætlun starfskrafts á launaskrá

**Beiðni**

```http
GET [Organization URI]/api/data/v9.1/mshr_payrollworkerbenefitplanentities?$filter=mshr_personnelnumber eq '000020'
```

**Svar**

```json
{
    "mshr_personnelnumber": "000020",
    "mshr_legalentityid": "USMF",
    "mshr_periodid": "2021",
    "mshr_planid": "Dental plan",
    "mshr_coverageoptionid": "Emp Only",
    "mshr_deductionstartdatetime": "2021-01-01T06:00:00Z",
    "mshr_deductionenddatetime": "2021-12-31T06:00:00Z",
    "mshr_status": 200000001,
    "mshr_validfrom": "2021-01-01T06:00:00Z",
    "mshr_validto": "2021-12-31T06:00:00Z",
    "mshr_plantypeid": "Dental",
    "mshr_plantypecode": 200000001,
    "mshr_payperiod": 12,
    "mshr_amountemployee": 47,
    "mshr_amountemployer": 57,
    "mshr_primaryfield": "000020 | USMF | 2021 | Dental plan",
    "_mshr_fk_worker_id_value": "000000ae-0000-0000-bfff-004105000000",
    "_mshr_fk_period_id_value": "00000807-0000-0000-ee02-005001000000",
    "_mshr_fk_plan_id_value": "00000c61-0000-0000-0200-005001000000",
    "_mshr_fk_plantype_id_value": "0000057c-0000-0000-0200-005001000000",
    "_mshr_fk_coverageoption_id_value": "00000391-0000-0000-0b00-005001000000",
    "mshr_payrollworkerbenefitplanentityid": "000006c4-0000-0000-bfff-004105000000"
}
```
## <a name="see-also"></a>Sjá einnig

[Kynning á API launasamþættingar](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
