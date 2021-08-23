---
title: Leyfisbeiðni
description: Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir einingu leyfisbeiðni í Dynamics 365 Human Resources.
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
ms.openlocfilehash: c6c772c26e8a789a54c9eeb36c1cab576a7f94cb3ede547db46fe18a2e89c8ce
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762023"
---
# <a name="leave-request"></a>Leyfisbeiðni

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði lýsir einingu leyfisbeiðni fyrir Dynamics 365 Human Resources.

### <a name="description"></a>lýsing

Þessi eining veitir upplýsingar vegna leyfisbeiðni.

Efnislegt heiti: mshr_essleaverequestentity.

## <a name="properties"></a>Eiginleikar

| Eiginleiki</br>**Efnislegt heiti**</br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Beiðnikenni**</br>mshr_requestid</br>*Strengur* | Lesa eingöngu | Beiðnikennið. |
| **Kenni leyfisgerðar**</br>mshr_leavetypeid</br>*Strengur* | Lesa eingöngu | Kenni leyfisgerðar. |
| **Dagsetning**</br>mshr_leavedate</br>*Mótfærð dagsetning og tími* | Lesa eingöngu | Dagsetning leyfisbeiðni. |
| **Upphæð**</br>mshr_amount</br>*Tugabrot* | Lesa eingöngu | Upphæð leyfisbeiðni. |
| **Hálfsdagsgerð**</br>mshr_halfdaydefinition</br>*Valmöguleiki mshr_LeaveHalfDayDefinition* | Lesa eingöngu | Gerð hálfsdagsleyfis. |
| **Athugasemd**</br>mshr_comment</br>*Strengur* | Lesa eingöngu | Athugasemd vegna beiðninnar. |
| **Staða**</br>mshr_status</br>*Valmöguleikar mshr_status* | Lesa eingöngu | Staða beiðninnar. |
| **Dagsetning**</br>mshr_requestdate</br>*Mótfærð dagsetning og tími* | Lesa eingöngu | Dagsetning beiðninnar. |
| **Númer starfsmanns**</br>mshr_personnelnumber</br>*Strengur* | Lesa eingöngu | Einkvæmt númer starfsmanns. |
| **Kenni ástæðukóða**</br>mshr_reasoncodeid</br>*Strengur* | Lesa eingöngu | Kenni ástæðukóða. |
| **Kenni gagnasvæðis**</br>mshr_dataareaid</br>*Strengur* | Lesa eingöngu | Tilgreinir lögaðilann (fyrirtækið). |
| **Aðalsvæði**</br>mshr_primaryfield</br>*GUID* | Lesa eingöngu</br>Búið til af kerfi | |
| **Eining leyfisgerðar**</br>mshr_essleaverequestentityid</br>*GUID* | Búið til af kerfi | GUID-gildi myndað af kerfinu til að auðkenna leyfisbeiðni á einkvæman hátt. |

## <a name="example-query"></a>Dæmi um fyrirspurn

**Beiðni**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleaverequestentities?$filter=mshr_personnelnumber eq '000020'
```

**Svar**

```json
{
    "mshr_requestid": "USMF-000001",
    "mshr_leavetype": "PTO",
    "mshr_leavedate": "2017-01-02T00:00:00Z",
    "mshr_amount": 8,
    "mshr_halfdaydefinition": 200000000,
    "mshr_comment": "Taking a week off to relax",
    "mshr_status": 200000009,
    "mshr_requestdate": "2017-07-31T00:00:00Z",
    "mshr_personnelnumber": "000020",
    "mshr_reasoncodeid": "",
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "USMF-000001 | PTO | 1/2/2017",
    "mshr_essleaverequestentityid": "000004dd-0000-0000-0f00-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Sjá einnig

[Kynning á API launasamþættingar](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
