---
title: Yfirlit MyLeaveRequests
description: MyLeaveRequests einingin í Microsoft Dynamics 365 Human Resources býður upp á lista yfir leyfisbeiðnir í kerfinu, umfangsmiklar (takmarkaðar) fyrir beiðnirnar sem eru aðgengilegar núverandi notanda sem fyrirspurnir eininguna.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 41ef8c6fc0e896e7f2cefd94801abab610083b81
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070856"
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
