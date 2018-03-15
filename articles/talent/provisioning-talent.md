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
ms.sourcegitcommit: 8b59ea6a2ac8c1c4e5df6e251fa3390639ff3f30
ms.openlocfilehash: e6266ef5890b5caaf33db76eeccfc8a7a6888a11
ms.contentlocale: is-is
ms.lasthandoff: 03/02/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a>Úthluta Microsoft Dynamics 365 for Talent

[!include[banner](includes/banner.md)]

[!include[banner](includes/banner.md)]

Þetta efnisatriði fer með þig í gegnum úthlutunarferli nýs framleiðsluumhverfis fyrir Microsoft Dynamics 365 for Talent. Þetta efnisatriði gerir ráð fyrir að þú hafir keypt Talent í gegnum Cloud Solution Provider (CSP) eða Enterprise Architecture (EA). Ef þú ert með fyrirliggjandi Microsoft Dynamics 365 leyfi sem nú þegar inniheldur þjónustuáætlun Talent og getur ekki lokið við skrefin í þessu efnisatriði, skaltu hafa samband við notendaþjónustu.

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

    Nýja umhverfið þitt birtist á lista yfir umhverfi á yfirlitssvæðinu vinstra megin. Hins vegar getur þú ekki byrjað að nota umhverfið fyrr en virkjunarstaða er uppfærð í **Virkjað**. Þetta ferli tekur alla jafna aðeins nokkrar mínútur. Ef úthlutunarferlið mistekst þarftu að hafa samband við notendaþjónustu.

6. Velja **Innskráning í Talent** til að nota nýja umhverfið þitt.

> [!NOTE]
> Ef þú hefur ekki ennþá skráð þig út á síðustu skilyrðin getur þú virkjað prufutilvik af Talent í verkinu. Þú getur síðan notað þetta tilvik til að prófa lausnina þína þar til þú skráir þig út. Ef þú notar nýtt umhverfi þitt til að prófa þarftu að endurtaka þetta ferli til að búa til framleiðsluumhverfi.

> [!NOTE]
> Talent umhverfum sem er úthlutað í gegnum LCS innihalda ekki sýnigögn sem eru stillt fyrir Mannauðsverk eða sem eru sértæk fyrir Talent. Ef þú þarft umhverfi sem inniheldur sýnigögn mælum við með að þú skráir þig fyrir ókeypis 60 daga [Talent prófunarumhverfi](https://dynamics.microsoft.com/en-us/talent/overview/). Þótt prófunarumhverfið sé í eigu notandans sem óskaði eftir því er samt hægt að bjóða öðrum notendum aðgang í gegnum upplifun kerfisstjóra fyrir mannauðskjarna. Prófunarumhverfi innihalda uppskálduð gögn sem hægt er að nota til að skoða forritið á öruggan hátt. Þau eru ætluð til þess að nota sem framleiðsluumhverfi. Athugaðu að þegar prófunarumhverfið rennur út að 60 dögum liðnum verður öllum gögnum umhverfisins eytt og ekki verður hægt að endurheimta þau. Þú getur skráð þig fyrir nýju prófunarumhverfi eftir að núverandi umhverfi rennur út.

## <a name="create-a-new-powerapps-environment-if-required"></a>Búa til nýtt PowerApp umhverfi (ef þörf krefur)
Samþætting milli Talent og PowerApps umhverfa leyfir þér að samþætta og útvíkka notkun á Talent gögnum með PowerApps verkfærum. Skilningur á tilgangi PowerApps umhverfanna mun auðvelda þér að smíða forrit sem mætir þínum þörfum við útvíkkun á Talent. Frekari upplýsingar um PowerApps umhverfin, þ.á.m. umfang umhverfis, aðgangur að umhverfi og stofnun og val á umhverfi eru í [PowerApps umhverfi kynnt til sögunnar](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/). Hverjum leigjanda er sjálfkrafa úthlutað sjálfgefið PowerApps umhverfi sem er ekki endilega umhverfið sem hentar best þinni nýtingu á Talent. Hafa skal í huga gagnasamþættingu og prófunaráætlanir í þessu skrefi og því er ráðlagt að hafa í huga afleiðingarnar sem geta haft áhrif á uppsetninguna því ekki er auðvelt að breyta sumum ákvörðunum eftir á. 

Þótt hverjum leigjanda sé sjálfkrafa úthlutað sjálfgefið PowerApps umhverfi er það ekki endilega umhverfið sem hentar best þinni nýtingu á Talent. Hafa skal í huga gagnasamþættingu og prófunaráætlanir í þessu skrefi. Því er mælt með að hafa í huga hinar ýmsu afleiðingar fyrir þína nýtingu vegna þess að það er ekki auðvelt að breyta PowerApps umhverfinu eftir á.

1. Veljið **Stjórna umhverfi** í LCS. Þú ert tekin í [Stjórnendamiðstöð PowerApps](https://preview.admin.powerapps.com/environments) þar sem þú getur skoðað núverandi umhverfi og búið til ný umhverfi.
2. Veljið **Nýtt umhverfi**.
3. Færið inn einkvæmt heiti fyrir umhverfið og veljið staðsetninguna sem skal virkja á.

    > [!NOTE]
    > Talent er ekki tiltæk fyrir öll svæði. Vertu því viss um að athuga hvort það er í boði áður en þú velur staðsetningu umhverfis þíns.

4. Þegar þú ert spurð(ur) hvort þú vilt búa til gagnagrunn skaltu velja **Búa til gagnagrunn** til að búa til Common Data Service (CDS) gagngrunn sem verður að hýsa hluta af Talent gögnunum þínum. Með því að búa til gagnagrunn, getur þú einnig samþætt PowerApps forrit með Talent.
5. Þú ert spurð(ur) um það aðgangsstig sem á að nota fyrir gagnagrunninn. Við mælum með að þú veljir **Takmarka aðgang**, vegna þess að þessi valkostur kemur í veg fyrir að Talent notendur fái beinan aðgang að viðkvæmum gögnum með því að nota PowerApps forrit.
6. CDS gagnarunnurinn sem er búinn til inniheldur sýnigögn sem bæta óvirkum starfsmönnum og uppskálduðum heimilisföngum, ásamt öðrum upplýsingum, inn í framleiðsluumhverfi þitt. Til að fjarlægja sýnigögnin skaltu fylgja þessum skrefum eftir að þú hefur lokið við að búa til CDS gagnagrunninn:

    > [!IMPORTANT]
    > Ef þú hefur áður búið til CDS gagnagrunn og slegið einhver framleiðslugögn fyrirtækis þíns inn í hann munu þessi skref fjarlæga **öll** gögnin í völdum gagnagrunni, jafnvel framleiðslugögn fyrirtækis þíns.

    1. Skráðu þig inn á [PowerApps](https://preview.web.powerapps.com/home).
    2. Í efra hægra horni fellilistans skal velja umhverfið sem var búið til í skrefi 2.
    3. Á yfirlitssvæðinu vinstra megin skal útvíkka **Common Data Service** og síðan velja **Einingar**.
    4. Hægra megi á síðunni skaltu velja sporöskju (**...**) hnappinn og síðan **Hreinsa öll gögn**.
    5. Velja **Eyða gögnum** til að staðfesta að þú viljir fjarlægja gögnin. Þessi aðgerð fjarlægir öll sýnigögnin sem eru innifalin í CDS að sjálfgefnu. Það fjarlægir einnig allar aðrar upplýsingar sem hafa verið slegnar inn í valda gagnagrunninn.

Nú er hægt að nota nýja umhverfið.

## <a name="grant-access-to-the-environment"></a>Veita aðgang að umhverfinu
Að sjálfgefnu hefur altæki stjórnandinn sem bjó til umhverfið aðgang að því. Hins vegar þarf sérstaklega að veita öðrum notendum forritsins aðgang. Til að veita aðgang skal [bæta við notendur](../dev-itpro/sysadmin/tasks/create-new-users.md) og [úthluta þeim viðeigandi hlutverkum](../dev-itpro/sysadmin/tasks/assign-users-security-roles.md) í kjarnaumhverfi mannauðs. Einnig þarf að bæta þessum notendum við PowerApps umhverfið svo þeir hafi aðgang að Attract and Onboard forritum. Ferlinu er lýst hér. Ef þú þarft hjálp til að ljúka skrefunum kíktu þá á bloggfærsluna [Kynning á stjórnendamiðstöð PowerApps](https://powerapps.microsoft.com/en-us/blog/introducing-admin-center-for-powerapps/).

Altæki stjórnandinn sem setti upp Talent umhverfið lauk þessu ferli.

1. Opnið [Stjórnendamiðstöð PowerApps](https://preview.admin.powerapps.com/environments).
2. Veljið viðeigandi umhverfi.
3. Í flipanum **Öryggi** skal bæta nauðsynlegum notendum við hlutverk **Umhverfisstjórnanda**.

Athugið að þetta lokaskref þar sem notendum er bætt handvirkt við PowerApps umhverfið er tímabundið. Það klárast að lokum sjálfkrafa þegar notendum er bætt við mannauðskjarnann.

