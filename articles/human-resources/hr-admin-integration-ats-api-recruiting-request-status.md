---
title: Staða ráðningarbeiðni
description: Þetta efnisatriði lýsir valmöguleika fyrir stöðu ráðningarbeiðni fyrir Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d845179077fc2e04dfb3bd05eaa70b0a2a016121
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067102"
---
# <a name="recruiting-request-status"></a>Staða ráðningarbeiðni


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði lýsir valmöguleika fyrir stöðu ráðningarbeiðni fyrir Dynamics 365 Human Resources.

Raunlægt heiti: mshr_hcmrecruitingrequeststatus

Þessi upptalning býður upp á valmöguleika fyrir stöðugildi RecruitingRequest.

| Virði | Merkimiði | lýsing |
| --- | --- | --- |
| 200000000 | Drög | Beiðnin er í drögum og er ekki tilbúin fyrir virka ráðningu. |
| 200000001 | Í endurskoðun | Beiðnin hefur verið send og verið er að senda hana til samþykktar af verkflæði. Aðeins í boði þegar verkflæði er virkt. |
| 200000002 | Í biðstöðu | Beiðnin bíður aðgerðar verkflæðis. Aðeins í boði þegar verkflæði er virkt. |
| 200000003 | Hætt við | Hætt var við beiðnina. Aðeins í boði þegar verkflæði er virkt. |
| 200000004 | Hafnað | Beiðninni var hafnað. Aðeins í boði þegar verkflæði er virkt. |
| 200000005 | Í gangi | Öllum verkflæðum er lokið og þau samþykkt og beiðnin er tilbúin fyrir virka ráðningu. |
| 200000006 | Lokað | Ráðningarbeiðnin er lokuð. |

## <a name="see-also"></a>Sjá einnig

[Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda](hr-admin-integration-ats-api-introduction.md)<br>
[Dæmi um fyrirspurn fyrir ráðningarbeiðni](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
