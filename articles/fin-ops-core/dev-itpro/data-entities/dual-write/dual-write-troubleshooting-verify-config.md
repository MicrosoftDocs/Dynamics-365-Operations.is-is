---
title: Staðfesta stillingu tvöfaldrar skráningar í fjármála- og rekstrarforritum og Dataverse
description: Þessi grein útskýrir hvernig þú getur ákvarðað hvort tvískrift sé stillt í Finance and Operations forritum og í Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 7131e6c2c4ca4d9c6bb84ad74bf425faf28bd92c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884460"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Staðfesta stillingu tvöfaldrar skráningar í fjármála- og rekstrarforritum og Dataverse

[!include [banner](../../includes/banner.md)]





Þessi grein veitir upplýsingar um bilanaleit fyrir tvískrifa samþættingu milli Finance and Operations forrita og Dataverse. Nánar tiltekið útskýrir það hvernig þú getur ákvarðað hvort tvískrift sé stillt í Finance and Operations forritum og í Dataverse.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Staðfestu að tvískrift sé stillt í Finance and Operations app

Til að ákvarða hvort villa sem birtist þegar reynt er að vista línur til að uppfæra eru úr tvöfaldri skráningu skal fyrst staðfesta að tvöföld skráning sé stillt.

+ Ef þú hefur stjórnandaréttindi í Finance and Operations appinu skaltu fara á **Vinnurými \> Gagnastjórnun**, og veldu **Tvöfalt skrifa** flísar. Ef upplýsingar um tengt umhverfi og lista yfir töflukort sem eru í keyrslu eru birtar er tvöföld skráning stillt.

    ![Staðfestir tengingu Finance and Operations appsins þegar þú hefur stjórnandaréttindi.](media/verify_fin_ops_1.png)

+ Ef þú ert ekki með stjórnandaréttindi muntu fá villuboð, *Ekki er hægt að skrifa gögn í eininguna \<entity name\>*. Í dæminu í eftirfarandi mynd er ekki hægt að búa til viðskiptavinalínu í Finance and Operations appinu, vegna þess að tvískrifað er, en tilvísunargögn viðskiptavinahóps og greiðsluskilmála eru ekki til í Dataverse.

    ![Staðfestir tengingu Finance and Operations appsins þegar þú hefur ekki stjórnandaréttindi.](media/verify_fin_ops_2.png)

Fyrir upplýsingar um hvernig á að laga vandamál þegar þú býrð til gögn í Finance and Operations forritum, sjá [Lestu vandamál við samstillingu í beinni](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Gakktu úr skugga um að tvískipt skrif sé stillt í Dataverse

Ef þú sérð reitinn **Fyrirtæki** á síðum í Dataverse þegar þú býrð til gögn, eru tvískipt skrif stillt.

![Staðfestir Dataverse tenginguna.](media/verify_cds.png)

Fyrir upplýsingar um hvernig eigi að laga mál þegar þú býrð til gögn í Dataverse, sjá [Úrræðaleita bein samstillingarvandamál](dual-write-troubleshooting-live-sync.md).

Fyrir upplýsingar um hvernig á að skoða villuupplýsingar ef þú lendir í villum meðan þú býrð til gögn í Dataverse, sjáðu [Kveiktu á og skoðaðu rekja innskráningu viðbótarinnar Dataverse til að skoða villuupplýsingar](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]