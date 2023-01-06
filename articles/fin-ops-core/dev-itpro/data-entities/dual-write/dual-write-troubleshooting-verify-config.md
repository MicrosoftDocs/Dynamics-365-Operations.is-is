---
title: Staðfesta stillingu tvöfaldrar skráningar í fjármála- og rekstrarforritum og Dataverse
description: Þessi grein útskýrir hvernig þú getur ákvarðað hvort tvískipt skrif eru stillt í forritum  og í Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 4ff7821fce661f174f57fb45667d4ceb3cfcede9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289391"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Staðfesta stillingu tvöfaldrar skráningar í fjármála- og rekstrarforritum og Dataverse

[!include [banner](../../includes/banner.md)]





Þessi grein veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita fjármála- og reksturs og Dataverse. Einkum útskýrir það hvernig þú getur ákvarðað hvort tvískipt skrif eru stillt í forritum fjármála- og reksturs og í Dataverse.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Gakktu úr skugga um að tvöföld skráning sé stillt í forriti fjármála- og reksturs

Til að ákvarða hvort villa sem birtist þegar reynt er að vista línur til að uppfæra eru úr tvöfaldri skráningu skal fyrst staðfesta að tvöföld skráning sé stillt.

+ Ef þú hefur stjórnunarréttindi í forriti fjármála- og reksturs, farðu til **Vinnusvæði \> Gagnastjórnun** og veldu reitinn **Tvöfalt skrif**. Ef upplýsingar um tengt umhverfi og lista yfir töflukort sem eru í keyrslu eru birtar er tvöföld skráning stillt.

    ![Staðfestir forritatengingu fjármála- og reksturs þegar þú hefur stjórnunarréttindi.](media/verify_fin_ops_1.png)

+ Ef þú ert ekki með stjórnandaréttindi muntu fá villuboð, *Ekki er hægt að skrifa gögn í eininguna \<entity name\>*. Í dæminu á eftirfarandi mynd er ekki hægt að stofna viðskiptamannslínu í forriti fjármála- og reksturs vegna þess að tvöföld skráning er grunnstillt en viðskiptavinaflokkur og tilvísunargögn greiðsluskilmála eru ekki til í Dataverse.

    ![Staðfestir forritatengingu fjármála- og reksturs þegar þú hefur ekki stjórnunarréttindi.](media/verify_fin_ops_2.png)

Fyrir upplýsingar um hvernig eigi að laga mál þegar þú býrð til gögn í forriti fjármála- og reksturs, sjá [Úrræðaleita bein samstillingarvandamál](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Gakktu úr skugga um að tvískipt skrif sé stillt í Dataverse

Ef þú sérð reitinn **Fyrirtæki** á síðum í Dataverse þegar þú býrð til gögn, eru tvískipt skrif stillt.

![Staðfestir Dataverse tenginguna.](media/verify_cds.png)

Fyrir upplýsingar um hvernig eigi að laga mál þegar þú býrð til gögn í Dataverse, sjá [Úrræðaleita bein samstillingarvandamál](dual-write-troubleshooting-live-sync.md).

Fyrir upplýsingar um hvernig á að skoða villuupplýsingar ef þú lendir í villum meðan þú býrð til gögn í Dataverse, sjáðu [Kveiktu á og skoðaðu rekja innskráningu viðbótarinnar Dataverse til að skoða villuupplýsingar](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
