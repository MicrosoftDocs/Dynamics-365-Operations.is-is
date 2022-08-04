---
title: Staðfestu tvöfalda skrifstillingu í fjármála- og rekstrarforritum og Dataverse
description: Þessi grein útskýrir hvernig þú getur ákvarðað hvort tvískrift sé stillt í fjármála- og rekstrarforritum og í Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: d5191f5dd9c3a286abac622aede07d04fb72a8f7
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111393"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Staðfestu tvöfalda skrifstillingu í fjármála- og rekstrarforritum og Dataverse

[!include [banner](../../includes/banner.md)]





Þessi grein veitir upplýsingar um bilanaleit fyrir samþættingu tvískrifa milli fjármála- og rekstrarforrita og Dataverse. Nánar tiltekið útskýrir það hvernig þú getur ákvarðað hvort tvískrift sé stillt í fjármála- og rekstrarforritum og í Dataverse.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Staðfestu að tvískrift sé stillt í fjármála- og rekstrarforriti

Til að ákvarða hvort villa sem birtist þegar reynt er að vista línur til að uppfæra eru úr tvöfaldri skráningu skal fyrst staðfesta að tvöföld skráning sé stillt.

+ Ef þú hefur stjórnandaréttindi í fjármála- og rekstrarappinu skaltu fara á **Vinnurými \> Gagnastjórnun**, og veldu **Tvöfalt skrifa** flísar. Ef upplýsingar um tengt umhverfi og lista yfir töflukort sem eru í keyrslu eru birtar er tvöföld skráning stillt.

    ![Staðfestir tengingu fjármála- og rekstrarapps þegar þú hefur stjórnandaréttindi.](media/verify_fin_ops_1.png)

+ Ef þú ert ekki með stjórnandaréttindi muntu fá villuboð, *Ekki er hægt að skrifa gögn í eininguna \<entity name\>*. Í dæminu í eftirfarandi mynd er ekki hægt að búa til viðskiptavinaröð í fjármála- og rekstrarforritinu, vegna þess að tvískrifað er stillt, en tilvísunargögn viðskiptavinahóps og greiðsluskilmála eru ekki til í Dataverse.

    ![Staðfestir tengingu fjármála- og rekstrarapps þegar þú hefur ekki stjórnandaréttindi.](media/verify_fin_ops_2.png)

Fyrir upplýsingar um hvernig á að laga vandamál þegar þú býrð til gögn í fjármála- og rekstrarforritum, sjá [Leysaðu vandamál í beinni samstillingu](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Gakktu úr skugga um að tvískipt skrif sé stillt í Dataverse

Ef þú sérð reitinn **Fyrirtæki** á síðum í Dataverse þegar þú býrð til gögn, eru tvískipt skrif stillt.

![Staðfestir Dataverse tenginguna.](media/verify_cds.png)

Fyrir upplýsingar um hvernig eigi að laga mál þegar þú býrð til gögn í Dataverse, sjá [Úrræðaleita bein samstillingarvandamál](dual-write-troubleshooting-live-sync.md).

Fyrir upplýsingar um hvernig á að skoða villuupplýsingar ef þú lendir í villum meðan þú býrð til gögn í Dataverse, sjáðu [Kveiktu á og skoðaðu rekja innskráningu viðbótarinnar Dataverse til að skoða villuupplýsingar](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
