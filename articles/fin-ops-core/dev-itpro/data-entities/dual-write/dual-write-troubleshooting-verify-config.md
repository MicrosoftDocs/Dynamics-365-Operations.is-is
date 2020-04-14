---
title: Gakktu úr skugga um að tvískipt skrif sé stillt í forritum Finance and Operations og Common Data Service
description: Þetta efni útskýrir hvernig þú getur ákvarðað hvort tvískipt skrif eru stillt í forritum Finance and Operations og í Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2f2ba2564ad3e8e444e27fcc0c586ddf252afabd
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172646"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-common-data-service"></a>Gakktu úr skugga um að tvískipt skrif sé stillt í forritum Finance and Operations og Common Data Service

[!include [banner](../../includes/banner.md)]



Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Common Data Service. Einkum útskýrir það hvernig þú getur ákvarðað hvort tvískipt skrif eru stillt í forritum Finance and Operations og í Common Data Service.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Gakktu úr skugga um að tvískipt skrif sé stillt í forriti Finance and Operations

Til að ákvarða hvort villurnar sem þú sérð þegar þú reynir að vista skrár til uppfærslu koma frá tvískiptri skrifun, staðfestu fyrst að tvískipt skrif er stillt.

+ Ef þú hefur stjórnunarréttindi í forriti Finance and Operations, farðu til **Vinnusvæði \> Gagnastjórnun** og veldu reitinn **Tvöfalt skrif**. Ef upplýsingar um tengd umhverfi og listi yfir heildarkort sem eru í gangi birtast er tvískipt skrifað.

    ![Staðfestir Finance and Operations forritatengingu þegar þú hefur stjórnunarréttindi](media/verify_fin_ops_1.png)

+ Ef þú ert ekki með adminaréttindi færðu villuboð, *Ekki tókst að skrifa gögn í einingu \<heiti einingar\>*. Í dæminu á eftirfarandi mynd, þú getur ekki búið til viðskiptavinaskrá í forritinu Finance and Operations, vegna þess að tvískipt skrif er stillt, en viðmiðunargögn viðskiptavinahópsins og greiðsluskilmálar eru ekki til Common Data Service.

    ![Staðfestir Finance and Operations forritatengingu þegar þú hefur ekki stjórnunarréttindi](media/verify_fin_ops_2.png)

Fyrir upplýsingar um hvernig eigi að laga mál þegar þú býrð til gögn í forriti Finance and Operations, sjá [Úrræðaleita bein samstillingarvandamál](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-common-data-service"></a>Gakktu úr skugga um að tvískipt skrif sé stillt í Common Data Service

Þegar þú býrð til gögn, ef þú sérð reitinn **Fyrirtæki** á síðum í Common Data Service, tvískipt skrif er stillt.

![Staðfestir Common Data Service tenginguna](media/verify_cds.png)

Fyrir upplýsingar um hvernig eigi að laga mál þegar þú býrð til gögn í Common Data Service, sjá [Úrræðaleita bein samstillingarvandamál](dual-write-troubleshooting-live-sync.md).

Fyrir upplýsingar um hvernig á að skoða villuupplýsingar ef þú lendir í villum meðan þú býrð til gögn í Common Data Service, sjáðu [Kveiktu á og skoðaðu rekja innskráningu viðbótarinnar Common Data Service til að skoða villuupplýsingar](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).
