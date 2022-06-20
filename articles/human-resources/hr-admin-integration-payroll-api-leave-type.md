---
title: Leyfisgerð
description: Þessi grein veitir upplýsingar og dæmi um fyrirspurn fyrir einingu leyfistegundarinnar í Dynamics 365 Human Resources.
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
ms.openlocfilehash: 6e7905989df92e943b86f86194c87dcb2a7b1446
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893787"
---
# <a name="leave-type"></a>Leyfisgerð


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þessi grein lýsir leyfisgerðinni fyrir Dynamics 365 Human Resources.

### <a name="description"></a>Lýsing

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
