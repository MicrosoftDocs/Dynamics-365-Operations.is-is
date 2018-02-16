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
ms.sourcegitcommit: a53c1997f74ebe572b17cc3090d2e236b6fe78f6
ms.openlocfilehash: 8a84cfe9b73f0c72f3cb0c3843749754c6b3d538
ms.contentlocale: is-is
ms.lasthandoff: 01/31/2018

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

Sýnin á bak við samþættingu Talents við PowerApps umhverfi er að virkja gagnasamþættingu og flæði viðbóta með því að nota PowerApps verkfæri ofan á Talent gögn. Þess vegna er mikilvægt að skilja tilgang PowerApps umhverfis þegar umhverfi er valið fyrir notkun á Talent. Nánari upplýsingar um PowerApps umhverfi, þ.m.t. umfang umhverfis, aðgang að umhverfi og stofnun og val á umhverfi, sjá [Tilkynningar um PowerApps umhverfi](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/).  Þó að hverjum leigjanda sé sjálfkrafa ráðstafað venjulegu PowerApps umhverfi, gæti verið að það sé ekki besta umhverfið til að nota fyrir uppsetningu á þínum Talent. Taka skal tillit til gagnasamþættinga og prófunaraðferða meðan á þessu skrefi stendur, svo við mælum með því að þú hafir í huga hinar ýmsu afleiðingar á uppsetningunni þinni, þar sem ekki er auðvelt að breyta henni síðar.

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

    1. Skráðu þig inn á [PowerApps](https://preview.web.powerapps.com/home) og veldu umhverfið sem þú stofnaðir í skrefi 2 úr fellilistanum hægra megin á síðunni.
    2. Stækkaðu **Common Data Service** á yfirlitssvæðinu vinstri megin og veldu **Einingar**.
    3. Hægra megi á síðunni skaltu velja sporöskju (**...**) hnappinn og síðan **Hreinsa öll gögn**.
    4. Velja **Eyða gögnum** til að staðfesta að þú viljir fjarlægja gögnin. Þessi aðgerð fjarlægir öll sýnigögnin sem eru innifalin í CDS að sjálfgefnu. Það fjarlægir einnig allar aðrar upplýsingar sem hafa verið slegnar inn í valda gagnagrunninn.
    
Nú er hægt að nota nýja umhverfið.

## <a name="granting-access-to-the-environment"></a>Að veita aðgang að umhverfinu
Kerfisstjórinn sem stofnaði umhverfið mun fá sjálfkrafa aðgang, en það þarf sérstaklega að veita viðbótarnotendum forritsins aðgang. Þetta er hægt að gera með því að [bæta við notendum](../dev-itpro/sysadmin/tasks/create-new-users.md) og að [úthluta þeim hlutverk](../dev-itpro/sysadmin/tasks/assign-users-security-roles.md) innan Core HR umhverfisins. Auk þess er einnig nauðsynlegt að bæta þessum notendum við PowerApps umhverfið þannig að þeir geti nálgast Attract and Onboard forritin.  Bloggfærslan [Kynning á stjórnstöð PowerApps](https://powerapps.microsoft.com/en-us/blog/introducing-admin-center-for-powerapps/) gæti hjálpað þér að ljúka þessum skrefum sem eru sett fram hér:

> 1.    Kerfissstjórinn sem setti upp Talent umhverfið ætti að fara í [PowerApps stjórnstöðina](https://preview.admin.powerapps.com/environments).   
> 2.    Veldu viðkomandi umhverfi.
> 3.    Undir öryggisflipanum skaltu bæta nauðsynlegum notendum við hlutverkið "Umhverfishönnuður".

Athugaðu að þetta síðasta skref að bæta notendum við PowerApps umhverfið er tímabundið. Við munum á endanum bæta við virkni til að gera þetta sjálfvirkt þegar notandanum er bætt við í Core HR.


