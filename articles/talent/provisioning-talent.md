---
title: Úthlutun Talent
description: Þetta efnisatriði fer með þig í gegnum úthlutunarferli nýs umhverfis fyrir Microsoft Dynamics 365 Talent.
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
ms.openlocfilehash: d06c0d14fb99e5544a5da05078f5b3a559f9e806
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025510"
---
# <a name="provision-talent"></a>Úthluta Talent

Þetta efnisatriði fer með þig í gegnum úthlutunarferli nýs framleiðsluumhverfis fyrir Microsoft Dynamics 365 Talent. Þetta efnisatriði gerir ráð fyrir að þú hafir keypt Talent í gegnum Cloud Solution Provider (CSP) eða Enterprise Architecture (EA). Ef þú ert með fyrirliggjandi Microsoft Dynamics 365 leyfi sem nú þegar inniheldur þjónustuáætlun Talent og getur ekki lokið við skrefin í þessu efnisatriði, skaltu hafa samband við notendaþjónustu.

Til að byrja, þá ætti stjórnandi á heimsvísu að skrá sig inn í [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) og búa til nýtt Talent verk. Nema vandamál tengd leyfisveitingu hindri þig frá því að úthluta Talent, er ekki þörf á aðstoð frá notendaþjónustu eða Dynamic Service Engineering (DSE) fulltrúum.

## <a name="create-an-lcs-project"></a>Búa til LCS-verk
Til að nota LCS til að stjórna Talent umhverfi þínu, þarftu fyrst að búa til LCS-verk.

1. Skráðu þig inn á [LCS](https://lcs.dynamics.com/Logon/Index) með því að nota reikninginn sem þú notaðir til að gerast áskrifandi að Talent.
2. Velja skal plúsmerki (**+**) til að stofna verk.
3. Velja **Microsoft Dynamics 365 Talent** sem nafn á verki og útgáfa verks.
4. Veldu **Dynamics 365 Talent** aðferðafræðina.
5. Velja **Stofna**.

Nánari upplýsingar um hvernig á að hefjast handa í Talent er að sjá í **Talent** aðferðafræðinni sem þú bjóst til í nýju verkinu. Eftir að þú hefur lokið við að búa til verkið skaltu ljúka eftirfarandi ferli til að úthluta Talent umhverfi þínu.

## <a name="provision-a-talent-project"></a>Úthluta Talent verki
Eftir að þú hefur búið til LCS verk, getur þú úthlutað Talent inn í umhverfi.

1. Í LCS verkinu skaltu velja **Talent Stjórnun Forrits** reitinn.
2. Tilgreinið hvort þetta sé sandkassa- eða framleiðslutilvik fyrir Talent. Snemmbúnir forskoðunareiginleikar kunna að vera í boði í Sandkassatilvikum til að leyfa ábendingar og prófanir sem fyrst. 

    > [!NOTE]
    > Ekki er hægt að breyta tilviksgerð Talent þegar hún hefur verið stillt. Gakktu úr skugga um að rétt tilviksgerð sé valin áður en haldið er áfram.

    > [!NOTE]
    > Gerð Talent-tilviks er aðskilin frá tilviksgerð í Microsoft Power Apps-umhverfi, sem þú stillir í Power Apps Admin Center.
3. Veldu valkostinn **Hafa sýnigögn með** ef þú vilt að umhverfið þitt innihaldi sama sýnigagnasafnið sem notað er í prufukeyrsluupplifun Talent. Þetta er gagnlegt fyrir langvarandi prufuútgáfu eða þjálfunarumhverfi og ætti aldrei að nota í vinnsluumhverfi.  Athugaðu að þú verður að velja þennan möguleika við upphaflega uppsetningu. Þú getur ekki uppfært fyrirliggjandi uppsetningu seinna.
4. Talent er alltaf úthlutað inn í Microsoft Power Apps umhverfi, til að virkja Power Apps samþættingu og stækkunarhæfni. Lestu kaflann „Val á Power Apps umhverfi“ í þessu efnisatriði áður en þú heldur áfram. Ef þú ert ekki með Power Apps umhverfi skaltu velja Stjórna umhverfum í LCS eða fara í Stjórnandamiðstöð Power Apps. Fylgdu síðan skrefunum til að [Stofna Power Apps umhverfi](https://docs.microsoft.com/powerapps/administrator/create-environment).

    > [!NOTE]
    > Til að skoða núverandi umhverfi eða búa til ný umhverfi, verður leigjanda sem stjórnar, sem úthlutar Talent, að vera úthlutað á Power Apps P2 leyfið. Ef fyrirtækið þitt hefur ekki Power Apps P2 leyfi geturðu fengið slíkt frá þínu CSP eða [Power Apps verðlagsíðunni](https://powerapps.microsoft.com/pricing/).

5. Veljið umhverfið til að úthluta Talent í.
6. Velja **Já** til að samþykkja skilmálana og hefja virkjun.

    Nýja umhverfið þitt birtist á lista yfir umhverfi á yfirlitssvæðinu vinstra megin. Hins vegar getur þú ekki byrjað að nota umhverfið fyrr en virkjunarstaða er uppfærð í **Virkjað**. Þetta ferli tekur venjulega nokkrar mínútur. Ef úthlutunarferlið mistekst þarftu að hafa samband við notendaþjónustu.

7. Velja **Innskráning í Talent** til að nota nýja umhverfið þitt.

    > [!NOTE]
    > Ef þú hefur ekki ennþá skráð þig út á síðustu skilyrðin getur þú virkjað prufutilvik af Talent í verkinu. Þú getur síðan notað þetta tilvik til að prófa lausnina þína þar til þú skráir þig út. Ef þú notar nýtt umhverfi þitt til að prófa þarftu að endurtaka þetta ferli til að búa til framleiðsluumhverfi.

    > Vegna þess að aðeins tvö LCS-umhverfi eru leyfð sem hluti af Talent-áskriftinni getur þú einnig íhugað að nota ókeypis 60 daga [Talent prófunarumhverfi](https://dynamics.microsoft.com/talent/overview/). Þótt prófunarumhverfið sé í eigu notandans sem óskaði eftir því er samt hægt að bjóða öðrum notendum aðgang í gegnum upplifun kerfisstjóra fyrir Human Resources. Prófunarumhverfi innihalda uppskálduð gögn sem hægt er að nota til að skoða forritið á öruggan hátt. Þau eru ætluð til þess að nota sem framleiðsluumhverfi. Athugaðu að þegar prófunarumhverfið rennur út að 60 dögum liðnum verður öllum gögnum í því eytt og ekki verður hægt að endurheimta þau. Þú getur skráð þig fyrir nýju prófunarumhverfi eftir að núverandi umhverfi rennur út.

## <a name="select-a-power-apps-environment"></a>Velja Power Apps-umhverfi

Samþætting milli Talent og Power Apps-umhverfa leyfir þér að samþætta og útvíkka notkun á Talent gögnum með Power Apps-verkfærum. Skilningur á tilgangi Power Apps-umhverfi hjálpar ekki aðeins við að búa til forrit til að stækka Talent, heldur hjálpar þér einnig að velja rétta umhverfið þegar þú úthlutar Talent. Frekari upplýsingar um Power Apps-umhverfin, þ.á.m. umfang umhverfis, aðgangur að umhverfi og stofnun og val á umhverfi eru í [Umhverfi Power Apps kynnt til sögunnar](https://powerapps.microsoft.com/blog/powerapps-environments/). 

Notaðu eftirfarandi leiðbeiningar þegar þú ákveður hvaða Power Apps-umhverfi til að virkja Talent inn í: 

1. Í LCS skaltu velja **Stjórna umhverfum**, eða fara beint í stjórnendamiðstöð Power Apps, þar sem þú getur skoðað núverandi umhverfi og stofnað ný umhverfi.
2. Einu Talent umhverfi er varpað á eitt Power Apps-umhverfi.
3. Power Apps-umhverfi inniheldur Talent ásamt samsvarandi forritum Power Apps, Power Automate og Common Data Service. Ef Power Apps-umhverfinu er eytt, þá á það einnig við um forritin innan þess. Þegar Talent umhverfi er úthlutað er hægt að veita annaðhvort umhverfið **Prufuútgáfa** eða **Framleiðsla**. Veldu tegund umhverfis byggt á því hvernig umhverfið verður notað. 
4. Gagnasamþætting og prófunaraðferðir ætti að hafa í huga, eins og Sandbox, UAT eða Framleiðsla. Mælt er með því að þú hafir í huga ýmsar afleiðingar á uppsetningunni, því það er ekki auðvelt að breyta því síðar hvaða Talent umhverfi er varpað á Power Apps-umhverfi.
5. Ekki er hægt að nota eftirfarandi Power Apps-umhverfi fyrir Talent og verður síað úr vallistanum innan LCS:
 
    - **Sjálfgefin Power Apps-umhverfi** - Þó að hverjum leigjanda sé sjálfkrafa úthlutað sjálfgefnu Power Apps-umhverfi, mælum við ekki með því að nota það með Talent vegna þess að allir leigunotendur hafa aðgang að Power Apps-umhverfi og geta óvart spillt framleiðslugögnum þegar þeir prófa og kanna samþættingar Power Apps eða Power Automate.
   
    - **Prófunarumhverfi** - Þessi umhverfi eru stofnuð með lokadegi og renna út eftir þann tíma, sem veldur því að umhverfið þitt og öll Talent-tilvik innan þess verða sjálfkrafa fjarlægð.
   
    - **Óstudd svæði** Að svo stöddu er Talent aðeins stutt á eftirfarandi svæðum: Bandaríkjunum, Evrópu, Bretlandi, Ástralíu, Kanada eða Ástralíu.
  
6. Eftir að þú hefur ákveðið rétt umhverfi sem til að nota, getur þú haldið áfram með úthlutunarferlið. 
 
## <a name="grant-access-to-the-environment"></a>Veita aðgang að umhverfinu
Að sjálfgefnu hefur altæki stjórnandinn sem bjó til umhverfið aðgang að því. Hins vegar þarf sérstaklega að veita öðrum notendum forritsins aðgang. Til að veita aðgang er nauðsynlegt að bæta við notendum og úthluta þeim viðeigandi hlutverkum í Human Resources-umhverfinu. Altæki stjórnandinn, sem virkjaði Talent, verður einnig að ræsa bæði Attract og Onboard til að ljúka frumstillingunni og virkja aðgang fyrir aðra leigunotendur.  Þar til þetta gerist munu aðrir notendur ekki geta opnað Attract og Onboard og fá upp villur vegna brots á aðgangi. Frekari upplýsingar má finna í [Stofna nýja notendur](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) og [Úthluta notendum á öryggishlutverk](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 
