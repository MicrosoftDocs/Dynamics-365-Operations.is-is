---
title: Undanþágustaða starfs
description: Þessi grein lýsir stöðuvalkostinum Starf undanþágu sem er stilltur fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: e59a71264d50cecce4d31dfa26ad7f05ef3f34e4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894673"
---
# <a name="job-exempt-status"></a>Undanþágustaða starfs


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þessi grein lýsir stöðuvalkostinum Starf undanþágu sem er stilltur fyrir Dynamics 365 Human Resources.

Raunlægt heiti: cdm_jobexemptstatus

Þessi upptalning tilgreinir valmöguleika fyrir stöðugildi undanþágu á FLSA-starfi. Boðið er upp á þetta í fyrirliggjandi valmöguleika cdm_jobexemptstatus.

| Virði | Merkimiði | lýsing |
| --- | --- | --- |
| 200000000 | Undanþága | Starfið er með undanþágustöðu samkvæmt FLSA-leiðbeiningum. |
| 200000001 | NonExempt | Starfið er með ekki undanþágustöðu samkvæmt FLSA-leiðbeiningum. |
| 200000002 | Á ekki við | Stöðuleiðbeiningar FLSA eiga ekki við um starfið. |

## <a name="see-also"></a>Sjá einnig

[Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda](hr-admin-integration-ats-api-introduction.md)<br>
[Dæmi um fyrirspurn fyrir ráðningarbeiðni](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
