---
title: Undanþágustaða starfs
description: Þetta efnisatriði lýsir valmöguleika undanþágustöðu starfs fyrir Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4765858f389f28467ae2ac71084c15d2ba0cbe8b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798298"
---
# <a name="job-exempt-status"></a>Undanþágustaða starfs

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