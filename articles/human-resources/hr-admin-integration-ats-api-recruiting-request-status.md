---
title: Staða ráðningarbeiðni
description: Þetta efnisatriði lýsir valmöguleika fyrir stöðu ráðningarbeiðni fyrir Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 55ed9c391a1b5f86c3c443b9fceeee5c2301444d
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125955"
---
# <a name="recruiting-request-status"></a>Staða ráðningarbeiðni

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