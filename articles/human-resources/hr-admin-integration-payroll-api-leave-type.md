---
title: Leyfisgerð
description: Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir einingu leyfisgerðar í Dynamics 365 Human Resources.
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
ms.openlocfilehash: 5e64b533ad7be23060701e8826a25736a078b59d1ecf824bee0e2dd05c9c78f8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713103"
---
# <a name="leave-type"></a>Leyfisgerð

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði lýsir einingu leyfisgerðar fyrir Dynamics 365 Human Resources.

### <a name="description"></a>lýsing

Þessi eining veitir upplýsingar vegna leyfisgerðar.

Efnislegt heiti: mshr_essleavetypeentity.

## <a name="properties"></a>Eiginleikar

| Eiginleiki</br>**Efnislegt heiti**</br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Kenni leyfisgerðar**</br>mshr_leavetypeid</br>*Strengur* | Lesa eingöngu | Kenni leyfisgerðar. |
| **Lýsing**</br>mshr_description</br>*Strengur* | Lesa eingöngu | Lýsing á leyfisgerð. |
| **Tegund**</br>mshr_category</br>*Valmöguleikar mshr_LeaveTypeCategory* | Lesa eingöngu | Flokkur leyfisgerðar. |
| **Ástæðukóði áskilinn**</br>mshr_isreasoncoderequired</br>*Valmöguleikar mshr_NoYes* | Lesa eingöngu | Skilgreinir hvort ástæðukóði er nauðsynlegur fyrir leyfisgerðina. |
| **Leyfiseining**</br>mshr_leaveamountunit</br>*Valmöguleikar mshr_LeaveAmountUnit* | Lesa eingöngu | Eining þessarar leyfisgerðar. |
| **Virkja hálfan dag**</br>mshr_enablehalfdaydefinition</br>*Valmöguleikar mshr_NoYes* | Skilgreinir hvort hálfur dagur sé virkur fyrir leyfisgerð. |
| **Kenni gagnasvæðis**</br>mshr_dataareaid_id</br>*Strengur* | Lesa eingöngu | Tilgreinir lögaðilann (fyrirtækið). |
| **Eining leyfisgerðar**</br>mshr_essleavetypeentityid</br>*GUID* | Búið til af kerfi | GUID-gildi myndað af kerfinu til að auðkenna leyfisgerð á einkvæman hátt. |

## <a name="example-query"></a>Dæmi um fyrirspurn

**Beiðni**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavetypeentities?$filter=mshr_leavetypeid eq 'PTO'
```

**Svar**

```json
{
    "mshr_leavetypeid": "PTO",
    "mshr_description": "Paid time off",
    "mshr_category": 200000000,
    "mshr_isreasoncoderequired": 200000000,
    "mshr_leaveamountunit": 200000000,
    "mshr_enablehalfdaydefinition": 200000000,
    "mshr_dataareaid": "usmf",
    "mshr_essleavetypeentityid": "00000a6c-0000-0000-0000-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Sjá einnig

[Kynning á API launasamþættingar](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
