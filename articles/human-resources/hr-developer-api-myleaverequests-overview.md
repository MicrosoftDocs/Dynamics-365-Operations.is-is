---
title: Yfirlit MyLeaveRequests
description: MyLeaveRequests einingin í Microsoft Dynamics 365 Human Resources býður upp á lista yfir leyfisbeiðnir í kerfinu, umfangsmiklar (takmarkaðar) fyrir beiðnirnar sem eru aðgengilegar núverandi notanda sem fyrirspurnir eininguna.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fefa436142fb99ed3bfb3d4454046a5d76619daecbf6f05100e8e405fca67d48
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732106"
---
# <a name="myleaverequests-overview"></a>Yfirlit MyLeaveRequests

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