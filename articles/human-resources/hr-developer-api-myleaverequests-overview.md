---
title: Yfirlit MyLeaveRequests
description: MyLeaveRequests einingin í Microsoft Dynamics 365 Human Resources veitir lista yfir leyfisbeiðnir.
author: twheeloc
ms.date: 02/03/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 20cc53ec3bcf38444ccf75f81e28d5efd9fc4537
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717056"
---
# <a name="myleaverequests-overview"></a>Yfirlit MyLeaveRequests


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

MyLeaveRequests einingin í Microsoft Dynamics 365 Human Resources býður upp á lista yfir leyfisbeiðnir í kerfinu, umfangsmiklar (takmarkaðar) fyrir beiðnirnar sem eru aðgengilegar núverandi notanda sem fyrirspurnir eininguna.

## <a name="key"></a>Lykill

  | Nafn eiginleika | Gagnagerð |
  |---------------|-----------|
  | dataAreaId    | Strengur    |
  | RequestId     | Strengur    |
  | LeaveType     | Strengur    |
  | LeaveDate     | Dagsetning      |
  
## <a name="properties"></a>Eiginleikar

  | Nafn eiginleika     | Gagnagerð | Krafa |
  |-------------------|-----------|----------|
  | dataAreaId        | Strengur    | X        |
  | RequestId         | Strengur    | X        |
  | LeaveType         | Strengur    | X        |
  | LeaveDate         | Dagsetning      | X        |
  | ReasonCodeId      | Strengur    |          |
  | PersonnelNumber   | Strengur    | X        |
  | RequestDate       | Dagsetning      | X        |
  | Athugasemd           | Strengur    |          |
  | Staða            | Upptalning      | X        |
  | Upphæð            | Rauntala      |          |
  | HalfDayDefinition | Upptalning      |          |

## <a name="actions"></a>Aðgerðir

 | Heiti aðgerðar                               | Lýsing                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [senda inn](hr-developer-api-myleaverequests-submit.md)   | Sendu beiðnina sem á að vinna úr með verkflæði. |

## <a name="see-also"></a>Sjá einnig

- [Senda leyfisbeiðni í verkflæði](hr-developer-api-myleaverequests-submit.md)
- [Sannvottun](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
