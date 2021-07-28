---
title: Staðfesta stillingu tvöfaldrar skráningar í Finance and Operations forritum og Dataverse
description: Þetta efni útskýrir hvernig þú getur ákvarðað hvort tvískipt skrif eru stillt í forritum Finance and Operations og í Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: d903d58fbd5e9d6bd9ecf7943d09525446721ba2
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350765"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Staðfesta stillingu tvöfaldrar skráningar í Finance and Operations forritum og Dataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Dataverse. Einkum útskýrir það hvernig þú getur ákvarðað hvort tvískipt skrif eru stillt í forritum Finance and Operations og í Dataverse.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Gakktu úr skugga um að tvískipt skrif sé stillt í forriti Finance and Operations

Til að ákvarða hvort villa sem birtist þegar reynt er að vista línur til að uppfæra eru úr tvöfaldri skráningu skal fyrst staðfesta að tvöföld skráning sé stillt.

+ Ef þú hefur stjórnunarréttindi í forriti Finance and Operations, farðu til **Vinnusvæði \> Gagnastjórnun** og veldu reitinn **Tvöfalt skrif**. Ef upplýsingar um tengt umhverfi og lista yfir töflukort sem eru í keyrslu eru birtar er tvöföld skráning stillt.

    ![Staðfestir Finance and Operations forritatengingu þegar þú hefur stjórnunarréttindi.](media/verify_fin_ops_1.png)

+ Ef þú ert ekki með stjórnandaréttindi muntu fá villuboð, *Ekki er hægt að skrifa gögn í eininguna \<entity name\>*. Í dæminu á eftirfarandi mynd er ekki hægt að stofna viðskiptamannslínu í Finance and Operations forritinu vegna þess að tvöföld skráning er grunnstillt en viðskiptavinaflokkur og tilvísunargögn greiðsluskilmála eru ekki til í Dataverse.

    ![Staðfestir Finance and Operations forritatengingu þegar þú hefur ekki stjórnunarréttindi.](media/verify_fin_ops_2.png)

Fyrir upplýsingar um hvernig eigi að laga mál þegar þú býrð til gögn í forriti Finance and Operations, sjá [Úrræðaleita bein samstillingarvandamál](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Gakktu úr skugga um að tvískipt skrif sé stillt í Dataverse

Ef þú sérð reitinn **Fyrirtæki** á síðum í Dataverse þegar þú býrð til gögn, eru tvískipt skrif stillt.

![Staðfestir Dataverse tenginguna.](media/verify_cds.png)

Fyrir upplýsingar um hvernig eigi að laga mál þegar þú býrð til gögn í Dataverse, sjá [Úrræðaleita bein samstillingarvandamál](dual-write-troubleshooting-live-sync.md).

Fyrir upplýsingar um hvernig á að skoða villuupplýsingar ef þú lendir í villum meðan þú býrð til gögn í Dataverse, sjáðu [Kveiktu á og skoðaðu rekja innskráningu viðbótarinnar Dataverse til að skoða villuupplýsingar](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]