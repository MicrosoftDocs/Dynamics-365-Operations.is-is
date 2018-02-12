---
title: "Úthluta Microsoft Dynamics 365 for Talent"
description: "Þetta efnisatriði fer með þig í gegnum úthlutunarferli nýs umhverfis fyrir Microsoft Dynamics 365 for Talent."
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 6ffb97b53f522cfe8ccd8e89df854cbc557e4f1f
ms.openlocfilehash: fadc373b2c1c06987f22d4d9c20a9ab07b0c85d5
ms.contentlocale: is-is
ms.lasthandoff: 11/20/2017

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a>Úthluta Microsoft Dynamics 365 for Talent
Þetta efnisatriði fer með þig í gegnum úthlutunarferli nýs umhverfis fyrir Microsoft Dynamics 365 for Talent. Þetta efnisatriði gerir ráð fyrir að þú hafir keypt Talent í gegnum Cloud Solution Provider (CSP) eða Enterprise Architecture (EA). Ef þú ert með fyrirliggjandi Microsoft Dynamics 365 leyfi sem nú þegar inniheldur þjónustuáætlun Talent og getur ekki lokið við skrefin í þessu efnisatriði, skaltu hafa samband við notendaþjónustu.

Til að byrja, þá ætti stjórnandi á heimsvísu að skrá sig inn í [Microsoft Dynamics Lifecycle Services](http://lcs.dynamics.com) (LCS) og búa til nýtt Talent verk. Nema vandamál tengd leyfisveitingu hindri þig frá því að úthluta Talent, er ekki þörf á aðstoð frá notendaþjónustu eða Dynamic Service Engineering (DSE) fulltrúum.

## <a name="create-an-lcs-project"></a>Búa til LCS-verk
Til að nota LCS til að stjórna Talent umhverfi þínu, þarftu fyrst að búa til LCS-verk.

1. Skráðu þig inn á [LCS](https://lcs.dynamics.com/Logon/Index) með því að nota reikninginn sem þú notaðir til að gerast áskrifandi að Talent.
2. Velja skal plúsmerki (**+**) til að stofna verk.
3. Velja **Microsoft Dynamics 365 for Talent** sem nafn á verki og útgáfa verks.
4. Velja **Dynamics 365 for Talent** aðferðafræði.
5. Velja **Stofna**.

Nánari upplýsingar um hvernig á að hefjast handa í Talent er að sjá í **Talent** aðferðafræðinni sem þú bjóst til í nýju verkinu. Eftir að þú hefur lokið við að búa til verkið skaltu ljúka eftirfarandi ferli til að úthluta Talent umhverfi þínu.

## <a name="provision-a-talent-project"></a>Úthluta Talent verki
Eftir að þú hefur búið til LCS verk, getur þú úthlutað Talent inn í umhverfi.

1. Í LCS verkinu skaltu velja **Talent Stjórnun Forrits** reitinn.
2. Talent er alltaf úthlutað inn í Microsoft PowerApps umhverfi, til að virkja PowerApps samþættingu og stækkunarhæfni. Ef þú ert ekki nú þegar með PowerApps umhverfi skaltu fylgja skrefunum í „Búa til nýtt PowerApps umhverfi (ef þörf krefur)“ hlutanum í þessum efnisatriði áður en þú heldur áfram.

    > [!NOTE]
    > Til að skoða núverandi umhverfi eða búa til ný umhverfi, verður leigjanda sem stjórnar, sem úthlutar Talent, að vera úthlutað á PowerApps P2 leyfið. Ef fyrirtækið þitt hefur ekki PowerApps P2 leyfi geturðu fengið slíkt frá þínu CSP eða [PowerApps verðlagsíðunni](https://powerapps.microsoft.com/en-us/pricing/).

3. Veldu **Bæta við** og veldu síðan umhverfið sem skal úthulta Talent inn í.
4. Velja **Já** til að samþykkja skilmálana og hefja virkjun.

    Nýja umhverfið þitt birtist á lista yfir umhverfi á yfirlitssvæðinu vinstra megin. Hins vegar getur þú ekki byrjað að nota umhverfið fyrr en virkjunarstaða er uppfærð í **Virkjað**. Þetta ferli tekur alla jafna aðeins nokkrar mínútur. Ef úthlutun mistekst verður þú að hafa samband við notendaþjónustu.

6. Velja **Innskráning í Talent** til að nota nýja umhverfið þitt.

> [!NOTE]
> Ef þú hefur ekki ennþá skráð þig út á síðustu skilyrðin getur þú virkjað prufutilvik af Talent í verkinu. Þú getur síðan notað þetta tilvik til að prófa lausnina þína þar til þú skráir þig út. Ef þú notar nýtt umhverfi þitt til að prófa þarftu að endurtaka þetta ferli til að búa til framleiðsluumhverfi.

## <a name="create-a-new-powerapps-environment-if-required"></a>Búa til nýtt PowerApp umhverfi (ef þörf krefur)
1. Veldu **Stjórna Umhverfi** í LCS. Þú ert tekin í [PowerApps Stjórnendamiðstöð](https://preview.admin.powerapps.com/environments), þar sem þú getur skoðað núverandi umhverfi og búið til ný umhverfi.
2. Velja (**+**) **Nýtt umhverfi** hnappinn.
3. Færið inn einkvæmt heiti fyrir umhverfið og veljið staðsetninguna sem skal virkja á.

    > [!NOTE]
    > Talent er ekki tiltæk fyrir öll svæði. Vertu því viss um að athuga hvort það er í boði áður en þú velur staðsetningu umhverfis þíns.

4. Þegar þú ert spurð(ur) hvort þú vilt búa til gagnagrunn skaltu velja **Búa til gagnagrunn** til að búa til Common Data Service (CDS) gagngrunn sem verður að hýsa hluta af Talent gögnunum þínum. Með því að búa til gagnagrunn, getur þú einnig samþætt PowerApps forrit með Talent.
5. Þú ert spurð(ur) um það aðgangsstig sem þú vilt nota fyrir gagnagrunninn. Við mælum með að þú veljir **Takmarka aðgang**, vegna þess að þessi valkostur kemur í veg fyrir að Talent notendur fái beinan aðgang að viðkvæmum gögnum með því að nota PowerApps forrit.
6. CDS gagnagrunnurinn sem er búin til inniheldur sýnigögn. Þessi sýnigögn eru gagnleg vegna þess að þú getur notað sýnigagnafyrirtækið til að prófa, eða til að búa til verkskráningar eða verkleiðbeiningar. Hins vegar bæta sýnigögnin óvirkum starfsmönnum og uppskálduðum heimilisföngum, meðal annarra upplýsinga, inn í framleiðsluumhverfi þitt. Til að fjarlægja sýnigögnin skaltu fylgja þessum skrefum eftir að þú hefur lokið við að búa til CDS gagnagrunninn:

    > [!IMPORTANT]
    > Ef þú hefur áður búið til CDS gagnagrunn og slegið inn einhver framleiðslugögn fyrirtækis þíns í það skaltu vera meðvitaður um að þessi skref fjarlæga **öll** gögnin í völdu gagnagrunninum, jafnvel framleiðslugögn fyrirtækis þíns.

    1. Skrá inn í [PowerApps](https://preview.web.powerapps.com/home), og fara í umhverfið sem þú stofnaðir í þrepi 2.
    2. Velja **einingar**. Hægra megi á síðunni skaltu velja sporöskju (**...**) hnappinn og síðan **Hreinsa öll gögn**.
    3. Velja **Eyða gögnum** til að staðfesta að þú viljir fjarlægja gögnin. Þessi aðgerð fjarlægir öll sýnigögnin sem eru innifalin í CDS að sjálfgefnu. Það fjarlægir einnig allar aðrar upplýsingar sem hafa verið slegnar inn í valda gagnagrunninn.

Nú er hægt að nota nýja umhverfið.

