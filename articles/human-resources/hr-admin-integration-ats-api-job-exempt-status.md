---
title: Undanþágustaða starfs
description: Þetta efnisatriði lýsir valmöguleika undanþágustöðu starfs fyrir Dynamics 365 Human Resources.
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
ms.openlocfilehash: 29d3c4fd37a219b520172c6866c5fec488c698f7
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8064992"
---
# <a name="job-exempt-status"></a>Undanþágustaða starfs


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði lýsir valmöguleika undanþágustöðu starfs fyrir Dynamics 365 Human Resources.

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
