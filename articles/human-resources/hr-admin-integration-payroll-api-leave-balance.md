---
title: Leyfisstaða
description: Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir einingu launastöðu í Dynamics 365 Human Resources.
author: marcelbf
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7d26d9624ae8d99b208f77d12137262983499c51
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8064817"
---
# <a name="leave-balance"></a>Leyfisstaða


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði lýsir einingu leyfisstöðu fyrir Dynamics 365 Human Resources.

### <a name="description"></a>lýsing

Þessi eining sýnir leyfisstöðu á hverja leyfisgerð fyrir tiltekinn starfsmann.

Efnislegt heiti: mshr_essleavebalanceentities.

## <a name="properties"></a>Eiginleikar

| Eiginleiki</br>**Efnislegt heiti**</br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Númer starfsmanns**</br>mshr_personnelnumber</br>*Strengur* | Lesa eingöngu | Einkvæmt númer starfsmanns. |
| **Núverandi staða**</br>mshr_balanceavailable</br>*Tugabrot* | Lesa eingöngu | Núverandi staða starfsmanns. |
| **Gerð**</br>mshr_balanceavailable</br>*Strengur* | Lesa eingöngu | Kenni leyfisgerðar. |
| **Uppsöfnunarhraði**</br>mshr_accrualratedescription</br> | Lesa eingöngu | Tíðni uppsöfnunar. |
| **Síðasta yfirfærsluupphæð**</br>mshr_lastcarryforwardamount</br>*Tugabrot* | Lesa eingöngu | Síðasta yfirfærða upphæð. |
| **Tekið á þessu ári**</br>mshr_takenthisyear</br>*Tugabrot* | Lesa eingöngu | Upphæð leyfis sem hefur verið tekið á þessu ári. |
| **Alls þetta ár**</br>mshr_totalthisyear</br>*Tugabrot* | Lesa eingöngu | Heildarupphæð á þessu ári. |
| **Kenni gagnasvæðis**</br>mshr_dataareaid_id</br>*Strengur* | Lesa eingöngu | Tilgreinir lögaðilann (fyrirtækið). |
| **Aðalsvæði**</br>mshr_primaryfield</br>*GUID* | Lesa eingöngu</br>Búið til af kerfi | |
| **Kenni leyfisgerðar**</br>_mshr_fk_leavetype_id_value</br>*GUID* | Lesa eingöngu</br>Ytri lykill:mshr_essleavetypeentityid of mshr_essleavetypeentity eining  | Kenni leyfisgerðar |
| **Eining leyfisstöðu**</br>mshr_essleavebalanceentityid</br>*GUID* | Búið til af kerfi | GUID-gildi myndað af kerfinu til að auðkenna stöðuna. |

## <a name="example-query"></a>Dæmi um fyrirspurn

**Beiðni**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavebalanceentities?$filter=mshr_personnelnumber eq '000013'
```

**Svar**

```json
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 67.76,
    "mshr_leavetypeid": "PTO",
    "mshr_accrualratedescription": "6.16 hrs / Semimonthly",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 67.76,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | PTO",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-0000-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-2703-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 80,
    "mshr_leavetypeid": "Sick",
    "mshr_accrualratedescription": "80.00 hrs / Annually",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 80,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Sick",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-ee02-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-3003-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 0,
    "mshr_leavetypeid": "Bereavement",
    "mshr_accrualratedescription": "0.00 hrs / Annually",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 0,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Bereavement",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-f402-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-4403-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 66.65,
    "mshr_leavetypeid": "Vacation",
    "mshr_accrualratedescription": "13.33 hrs / Monthly",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 66.65,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Vacation",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-f502-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-1009-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Sjá einnig

[Kynning á API launasamþættingar](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
