---
title: Úthlutun Talent
description: Þetta efnisatriði fer með þig í gegnum úthlutunarferli nýs umhverfis fyrir Microsoft Dynamics 365 for Talent.
author: andreabichsel
manager: AnnBe
ms.date: 05/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: 781487997ceb95f4e3f528f47e8ed2aa5b25fd0e
ms.sourcegitcommit: eb501d8712212a6ed33bec1e3e2c02f994e0a724
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/09/2019
ms.locfileid: "1869937"
---
# <a name="provision-talent"></a>Úthluta Talent

[!include [banner](includes/banner.md)]

Þetta efnisatriði fer með þig í gegnum úthlutunarferli nýs framleiðsluumhverfis fyrir Microsoft Dynamics 365 for Talent. Þetta efnisatriði gerir ráð fyrir að þú hafir keypt Talent í gegnum Cloud Solution Provider (CSP) eða Enterprise Architecture (EA). Ef þú ert með fyrirliggjandi Microsoft Dynamics 365 leyfi sem nú þegar inniheldur þjónustuáætlun Talent og getur ekki lokið við skrefin í þessu efnisatriði, skaltu hafa samband við notendaþjónustu.

Til að byrja, þá ætti stjórnandi á heimsvísu að skrá sig inn í [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) og búa til nýtt Talent verk. Nema vandamál tengd leyfisveitingu hindri þig frá því að úthluta Talent, er ekki þörf á aðstoð frá notendaþjónustu eða Dynamic Service Engineering (DSE) fulltrúum.

## <a name="create-an-lcs-project"></a>Búa til LCS-verk
Til að nota LCS til að stjórna Talent umhverfi þínu, þarftu fyrst að búa til LCS-verk.

1. Skráðu þig inn á [LCS](https://lcs.dynamics.com/Logon/Index) með því að nota reikninginn sem þú notaðir til að gerast áskrifandi að Talent.
2. Velja skal plúsmerki (**+**) til að stofna verk.
3. Velja **Microsoft Dynamics 365 for Talent** sem nafn á verki og útgáfa verks.
4. Veldu **Dynamics 365 for Talent** aðferðafræðina.
5. Velja **Stofna**.

Nánari upplýsingar um hvernig á að hefjast handa í Talent er að sjá í **Talent** aðferðafræðinni sem þú bjóst til í nýju verkinu. Eftir að þú hefur lokið við að búa til verkið skaltu ljúka eftirfarandi ferli til að úthluta Talent umhverfi þínu.

## <a name="provision-a-talent-project"></a>Úthluta Talent verki
Eftir að þú hefur búið til LCS verk, getur þú úthlutað Talent inn í umhverfi.

1. Í LCS verkinu skaltu velja **Talent Stjórnun Forrits** reitinn.
2. Tilgreinið hvort þetta sé sandkassa- eða framleiðslutilvik fyrir Talent. Snemmbúnir forskoðunareiginleikar kunna að vera í boði í Sandkassatilvikum til að leyfa ábendingar og prófanir sem fyrst. 
    > [!NOTE]
    > Gerð Talent-tilviks er aðskilin frá tilviksgerð í PowerApps-umhverfi, sem þú stillir í PowerApps Admin Center.
3. Veldu valkostinn **Hafa sýnigögn með** ef þú vilt að umhverfið þitt innihaldi sama sýnigagnasafnið sem notað er í prufukeyrsluupplifun Talent. Þetta er gagnlegt fyrir langvarandi prufuútgáfu eða þjálfunarumhverfi og ætti aldrei að nota í vinnsluumhverfi.  Athugaðu að þú verður að velja þennan möguleika við upphaflega uppsetningu. Þú getur ekki uppfært fyrirliggjandi uppsetningu seinna.
4. Talent er alltaf úthlutað inn í Microsoft PowerApps umhverfi, til að virkja PowerApps samþættingu og stækkunarhæfni. Lestu kaflann „Val á PowerApps umhverfi“ í þessu efnisatriði áður en þú heldur áfram. Ef þú ert ekki með PowerApps umhverfi skaltu velja Stjórna umhverfum í LCS eða fara í Stjórnandamiðstöð PowerApps. Fylgdu síðan skrefunum til að [Búa til PowerApps umhverfi](https://docs.microsoft.com/powerapps/administrator/create-environment).

    > [!NOTE]
    > Til að skoða núverandi umhverfi eða búa til ný umhverfi, verður leigjanda sem stjórnar, sem úthlutar Talent, að vera úthlutað á PowerApps P2 leyfið. Ef fyrirtækið þitt hefur ekki PowerApps P2 leyfi geturðu fengið slíkt frá þínu CSP eða [PowerApps verðlagsíðunni](https://powerapps.microsoft.com/pricing/).

5. Veljið umhverfið til að úthluta Talent í.
6. Velja **Já** til að samþykkja skilmálana og hefja virkjun.

    Nýja umhverfið þitt birtist á lista yfir umhverfi á yfirlitssvæðinu vinstra megin. Hins vegar getur þú ekki byrjað að nota umhverfið fyrr en virkjunarstaða er uppfærð í **Virkjað**. Þetta ferli tekur venjulega nokkrar mínútur. Ef úthlutunarferlið mistekst þarftu að hafa samband við notendaþjónustu.

7. Velja **Innskráning í Talent** til að nota nýja umhverfið þitt.

    > [!NOTE]
    > Ef þú hefur ekki ennþá skráð þig út á síðustu skilyrðin getur þú virkjað prufutilvik af Talent í verkinu. Þú getur síðan notað þetta tilvik til að prófa lausnina þína þar til þú skráir þig út. Ef þú notar nýtt umhverfi þitt til að prófa þarftu að endurtaka þetta ferli til að búa til framleiðsluumhverfi.

    > Vegna þess að aðeins tvö LCS-umhverfi eru leyfð sem hluti af Talent-áskriftinni getur þú einnig íhugað að nota ókeypis 60 daga [Talent prófunarumhverfi](https://dynamics.microsoft.com/talent/overview/). Þótt prófunarumhverfið sé í eigu notandans sem óskaði eftir því er samt hægt að bjóða öðrum notendum aðgang í gegnum upplifun kerfisstjóra fyrir mannauðskjarna. Prófunarumhverfi innihalda uppskálduð gögn sem hægt er að nota til að skoða forritið á öruggan hátt. Þau eru ætluð til þess að nota sem framleiðsluumhverfi. Athugaðu að þegar prófunarumhverfið rennur út að 60 dögum liðnum verður öllum gögnum í því eytt og ekki verður hægt að endurheimta þau. Þú getur skráð þig fyrir nýju prófunarumhverfi eftir að núverandi umhverfi rennur út.

## <a name="select-a-powerapps-environment"></a>Velja PowerApps umhverfi

Samþætting milli Talent og PowerApps umhverfa leyfir þér að samþætta og útvíkka notkun á Talent gögnum með PowerApps verkfærum. Skilningur á tilgangi PowerApps umhverfi hjálpar ekki aðeins við að búa til forrit til að stækka Talent, heldur hjálpar þér einnig að velja rétta umhverfið þegar þú úthlutar Talent. Frekari upplýsingar um PowerApps umhverfin, þ.á.m. umfang umhverfis, aðgangur að umhverfi og stofnun og val á umhverfi eru í [PowerApps umhverfi kynnt til sögunnar](https://powerapps.microsoft.com/blog/powerapps-environments/). 

Notaðu eftirfarandi leiðbeiningar þegar þú ákveður hvaða PowerApps umhverfi til að virkja Talent inn í: 

1. Í LCS skaltu velja **Stjórna umhverfum**, eða fara beint í stjórnendamiðstöð PowerApps, þar sem þú getur skoðað núverandi umhverfi og stofnað ný umhverfi.
2. Einu Talent umhverfi er varpað á eitt PowerApps umhverfi.
3. PowerApps umhverfi „inniheldur“ Talent forritið, ásamt samsvarandi PowerApps, Flow og Common Data Service forritum. Ef PowerApps umhverfinu er eytt, þá á það einnig við um forritin innan þess. Þegar Talent umhverfi er úthlutað er hægt að veita „Prufuútgáfa“ eða „Framleiðsla“. Veldu tegund umhverfis byggt á því hvernig umhverfið verður notað. 
4. Gagnasamþætting og prófunaraðferðir ætti að hafa í huga, eins og Sandbox, UAT eða Framleiðsla. Mælt er með því að þú hafir í huga ýmsar afleiðingar á uppsetningunni, því það er ekki auðvelt að breyta því síðar hvaða Talent umhverfi er varpað á PowerApps umhverfi.
5. Ekki er hægt að nota eftirfarandi PowerApps umhverfi fyrir Talent og verður síað úr vallistanum innan LCS:
 
    - **Sjálfgefin PowerApps umhverfi** Þó að hverjum leigjanda sé sjálfkrafa úthlutað sjálfgefnu PowerApps umhverfi, mælum við ekki með því að nota það með Talent vegna þess að allir leigunotendur hafa aðgang að PowerApps umhverfi og geta óvart spillt framleiðslugögnum þegar þeir prófa og kanna samþættingar PowerApps eða Flow.
   
    - **Prófunarumhverfi** - Þessi umhverfi eru stofnuð með lokadegi og renna út eftir þann tíma, sem veldur því að umhverfið þitt og öll Talent-tilvik innan þess verða sjálfkrafa fjarlægð.
   
    - **Óstudd svæði** Að svo stöddu er Talent aðeins stutt á eftirfarandi svæðum: Bandaríkjunum, Evrópu, Bretlandi, Ástralíu, Kanada eða Ástralíu.
  
6. Eftir að þú hefur ákveðið rétt umhverfi sem til að nota, getur þú haldið áfram með úthlutunarferlið. 
 
## <a name="grant-access-to-the-environment"></a>Veita aðgang að umhverfinu
Að sjálfgefnu hefur altæki stjórnandinn sem bjó til umhverfið aðgang að því. Hins vegar þarf sérstaklega að veita öðrum notendum forritsins aðgang. Til að veita aðgang er nauðsynlegt að bæta við notendum og úthluta þeim viðeigandi hlutverkum í Core HR-umhverfinu. Altæki stjórnandinn, sem virkjaði Talent, verður einnig að ræsa bæði forritin Attract og Onboard til að ljúka frumstillingunni og virkja aðgang fyrir aðra leigunotendur.  Þar til þetta gerist munu aðrir notendur ekki geta opnað forritin Attract og Onboard og fá upp villur vegna brots á aðgangi. Frekari upplýsingar má finna í [Stofna nýja notendur](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) og [Úthluta notendum á öryggishlutverk](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 
