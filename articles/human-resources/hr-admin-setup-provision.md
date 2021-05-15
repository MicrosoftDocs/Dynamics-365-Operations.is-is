---
title: Ráðstafa mannauði
description: Þessi grein fer með þig í gegnum úthlutunarferli nýs framleiðsluumhverfis fyrir Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fee496157db581bf77f444674ca858aa4383e27c
ms.sourcegitcommit: 54d3ec0c006bfa9d2b849590205be08551c4e0f0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/30/2021
ms.locfileid: "5963216"
---
# <a name="provision-human-resources"></a>Ráðstafa mannauði

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Þessi grein fer með þig í gegnum úthlutunarferli nýs framleiðsluumhverfis fyrir Microsoft Dynamics 365 Human Resources. Þeessi grein gerir ráð fyrir að þú hafir keypt Human Resources í gegnum Cloud Solution Provider (CSP) eða Enterprise Architecture (EA). Ef þú ert með fyrirliggjandi Microsoft Dynamics 365 leyfi sem nú þegar inniheldur þjónustuáætlun Human Resources og getur ekki lokið við skrefin í þessari grein, skaltu hafa samband við notendaþjónustu.

Til að byrja, þá ætti stjórnandi á heimsvísu að skrá sig inn í [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) og búa til nýtt Human Resources verk. Nema vandamál tengd leyfisveitingu hindri þig frá því að úthluta Human Resources, er ekki þörf á aðstoð frá notendaþjónustu eða Dynamic Service Engineering (DSE) fulltrúum.

## <a name="plan-human-resources-environments"></a>Skipuleggja umhverfi Human Resources

Áður en fyrsta Human Resources-umhverfið er búið til ætti að kortleggja vel og vandlega þarfir umhverfisins fyrir verkið. Grunnáskrift að Human Resources felur í sér tvö umhverfi: vinnsluumhverfi og sandkassaumhverfi. Það fer eftir margbreytileika verksins hvort þurfi að kaupa fleiri sandkassaumhverfi til að styðja verkþætti verksins. 

Nokkur atriði sem hafa áhrif á hvort nota eigi fleiri umhverfi eða ekki eru m.a. eftirfarandi:

- **Gagnaflutningur**: Hugsanlega þarf að huga að viðbótarumhverfi fyrir gagnaflutningsaðgerðir svo hægt sé að nota sandkassaumhverfið sem vettvang prófunar í gegnum verkið. Að vera með viðbótarumhverfi gerir gagnaflutningsaðgerðum kleift að halda áfram á meðan prófanir og grunnstillingar gerast samtímis í öðru umhverfi.
- **Samþætting**: Hugsanlega þarf annað umhverfi til að grunnstilla og prófa samþættingar. Þetta gæti falið í sér venjulega samþættingu á borð við samþættingar Ceridian Dayforce LinkedIn Talent Hub eða sérstilltar samþættingar á borð við launaskrár, rakningarkerfi umsækjanda eða fríðindakerfi og þjónustuaðilar.
- **Þjálfun**: Hugsanlega þarf aðskilið umhverfi sem er grunnstillt með safni þjálfunargagna til að geta þjálfað starfsmenn í notkun á nýja kerfinu. 
- **Fjölþrepa verk**: Hugsanlega þarf annað umhverfi til að styðja grunnstillingu, gagnaflutning, prófun eða aðra verkþætti í verkþrepi sem er áætlað eftir fyrstu keyrslu verksins.

 > [!IMPORTANT]
 > Mælt er með að nota vinnsluumhverfið í gegnum verkið sem umhverfi GOLD-grunnstillingar. Þetta er mikilvægt vegna þess að ekki er hægt að afrita sandkassaumhverfi í vinnsluumhverfi. Þar af leiðandi, þegar keyrsla er framkvæmd, er GOLD-umhverfið orðið vinnsluumhverfið og flutningsaðgerðir verða kláraðar í þessu umhverfi.</br></br>
 > Mælt er með að nota sandkassann eða annað umhverfi til að framkvæma hermiflutning á undan keyrslunni. Hægt er að gera þetta með því að uppfæra vinnsluumhverfið með GOLD-grunnstillingunni inn í sandkassaumhverfið.</br></br>
 > Mælt er með að halda utan um ítarlegan gátlista flutnings sem inniheldur alla gagnapakkana sem þarf til að flytja lokagögnin í vinnsluumhverfið á meðan flutningur keyrslunnar stendur yfir.</br></br>
 > Einnig er mælt með að nota sandkassaumhverfið í gegnum verkið sem prófunarumhverfi. Ef þörf er á fleiri umhverfum getur fyrirtækið keypt þau gegn viðbótarkostnaði.</br></br>

## <a name="create-an-lcs-project"></a>Búa til LCS-verk

Til að nota LCS til að stjórna Human Resources umhverfi þínu, þarftu fyrst að búa til LCS-verk.

1. Skráðu þig inn á [LCS](https://lcs.dynamics.com/Logon/Index) með því að nota reikninginn sem þú notaðir til að gerast áskrifandi að Human Resources.

   > [!NOTE]
   > Til að tryggja árangursríka úthlutun verður reikningurinn sem þú notar til að úthluta umhverfi Human Resources að vera úthlutað á annaðhvort hlutverkið **Kerfisstjóri** eða **Kerfisstillir** í Power Apps-umhverfinu sem tengist umhverfi Human Resources. Frekari upplýsingar um úthlutun öryggishlutverka til notenda í Power Platform er að finna í [Skilgreina öryggi notanda við tilföng](https://docs.microsoft.com/power-platform/admin/database-security).

2. Velja skal plúsmerki (**+**) til að stofna verk.

3. Velja **Microsoft Dynamics 365 Human Resources** sem nafn á verki og útgáfa verks.

4. Veldu **Dynamics 365 Human Resources** aðferðafræðina.

5. Velja **Stofna**.

Nánari upplýsingar um hvernig á að hefjast handa í Human Resources er að sjá í **Human Resources** aðferðafræðinni sem þú bjóst til í nýju verkinu. Eftir að þú hefur lokið við að búa til verkið skaltu ljúka eftirfarandi ferli til að úthluta Human Resources umhverfi þínu.

## <a name="provision-a-human-resources-project"></a>Ráðstafa verki í Human Resources

Eftir að þú hefur búið til LCS verk, getur þú úthlutað Human Resources inn í umhverfi.

1. Í LCS verkinu skaltu velja **Human Resources Stjórnun Forrits** reitinn.

2. Tilgreinið hvort þetta umhverfi sé sandkassa- eða framleiðslutilvik fyrir Mannauð. Snemmbúnir forskoðunareiginleikar kunna að vera í boði í Sandkassatilvikum til að leyfa ábendingar og prófanir sem fyrst.
   
    > [!NOTE]
    > Ekki er hægt að breyta tilviksgerð Human Resources þegar hún hefur verið stillt. Gakktu úr skugga um að rétt tilviksgerð sé valin áður en haldið er áfram.</br></br>
    > Gerð Human Resources-tilviks er aðskilin frá tilviksgerð í Microsoft Power Apps-umhverfi, sem þú stillir í Power Apps Admin Center.
    
3. Veldu valkostinn **Hafa sýnigögn með** ef þú vilt að umhverfið þitt innihaldi sama sýnigagnasafnið sem notað er í prufukeyrsluupplifun Human Resources. Sýnigögn eru gagnleg fyrir langvarandi prufuútgáfu eða þjálfunarumhverfi og ætti aldrei að nota í vinnsluumhverfi. Þú verður að velja þennan möguleika við upphaflega uppsetningu. Þú getur ekki uppfært núverandi uppsetningu seinna.

4. Human Resources er alltaf úthlutað inn í Microsoft Power Apps umhverfi, til að virkja Power Apps samþættingu og stækkunarhæfni. Lestu kaflann „Val á Power Apps umhverfi“ í þessari grein áður en þú heldur áfram. Ef þú ert ekki með Power Apps umhverfi skaltu velja Stjórna umhverfum í LCS eða fara í Stjórnandamiðstöð Power Apps. Fylgdu síðan skrefunum til að [Stofna Power Apps umhverfi](/powerapps/administrator/create-environment).

5. Veljið umhverfið til að úthluta Human Resources í.

6. Velja **Já** til að samþykkja skilmálana og hefja virkjun.

   Nýja umhverfið þitt birtist á lista yfir umhverfi á yfirlitssvæðinu vinstra megin. Hins vegar getur þú ekki byrjað að nota umhverfið fyrr en virkjunarstaða er uppfærð í **Virkjað**. Þetta ferli tekur venjulega nokkrar mínútur. Ef úthlutunarferlið mistekst þarftu að hafa samband við notendaþjónustu.

7. Veldu **Innskráning í Mannauð** til að nota nýja umhverfið þitt.

    > [!NOTE]
    > Ef þú hefur ekki ennþá skráð þig út á síðustu skilyrðin getur þú virkjað prufutilvik af Human Resources í verkinu. Þú getur síðan notað þetta tilvik til að prófa lausnina þína þar til þú skráir þig út. Ef þú notar nýtt umhverfi þitt til að prófa þarftu að endurtaka þetta ferli til að búa til framleiðsluumhverfi.

    > Þú gætir íhugað að nýta ókeypis 60 daga [Prófunarumhverfi Human Resources](https://go.microsoft.com/fwlink/p/?LinkId=2115962). Þótt prófunarumhverfið sé í eigu notandans sem óskaði eftir því er samt hægt að bjóða öðrum notendum aðgang í gegnum upplifun kerfisstjóra fyrir Human Resources. Prófunarumhverfi innihalda uppskálduð gögn sem hægt er að nota til að skoða forritið á öruggan hátt. Þau eru ætluð til þess að nota sem framleiðsluumhverfi. Athugaðu að þegar prófunarumhverfið rennur út að 60 dögum liðnum verður öllum gögnum í því eytt og ekki verður hægt að endurheimta þau. Þú getur skráð þig fyrir nýju prófunarumhverfi eftir að núverandi umhverfi rennur út.

## <a name="select-a-power-apps-environment"></a>Velja Power Apps-umhverfi

Þú getur samþætt og aukið notkun Human Resources gagna með Power Apps verkfærum. Frekari upplýsingar um Power Apps-umhverfin, þ.á.m. umfang umhverfis, aðgangur að umhverfi og stofnun og val á umhverfi eru í [Umhverfi Power Apps kynnt til sögunnar](https://powerapps.microsoft.com/blog/powerapps-environments/). 

Notaðu eftirfarandi leiðbeiningar þegar þú ákveður hvaða Power Apps-umhverfi til að virkja Human Resources inn í: 

1. Veljið **Stjórna umhverfi** í LCS. Einnig er hægt að fara beint í stjórnendamiðstöð Power Apps, þar sem þú getur skoðað núverandi umhverfi og stofnað ný.

2. Einu Human Resources umhverfi er varpað á eitt Power Apps-umhverfi.

3. Power Apps-umhverfi inniheldur Human Resources ásamt samsvarandi forritum Power Apps, Power Automate og Dataverse. Ef Power Apps-umhverfinu er eytt, þá á það einnig við um forritin innan þess. Þegar Human Resources umhverfi er úthlutað er hægt að veita annaðhvort umhverfið **Prufuútgáfa** eða **Framleiðsla**. Veldu tegund umhverfis byggt á því hvernig umhverfið verður notað. 

4. Gagnasamþætting og prófunaraðferðir ætti að hafa í huga, eins og Sandbox, UAT eða Framleiðsla. Hugsaðu vandlega út í afleiðingar uppsetningarinnar því að ekki er auðvelt að breyta því hvaða umhverfi Human Resources er varpað í Power Apps-umhverfi.

5. Þú getur ekki notað eftirfarandi Power Apps-umhverfi fyrir Human Resources. Þau eru síuð úr lista yfir valkosti innan LCS:
 
    - **Sjálfgefið Power Apps-umhverfi** - Þótt hverjum leigjanda sé sjálfkrafa úthlutað sjálfgefnu Power Apps-umhverfi mælum við ekki með því að þau séu notuð með Human Resources. Allir leigunotendur hafa aðgang að Power Apps-umhverfinu og gætu óvart skemmt framleiðslugögn þegar þeir prófa og kanna með Power Apps eða Power Automate-samþættingar.
   
    - **Prófunarumhverfi** - Þessi umhverfi eru búin til með lokadagsetningu. Þegar umhverfið rennur út verður það og öll tilvik Human Resources innan þess fjarlægð sjálfkrafa.
   
    - **Óstudd svæði** - Umhverfið verður að vera á studdri staðsetningu. Frekari upplýsingar er að finna í [Landfræðilegar staðsetningar sem eru studdar](hr-admin-setup-provision.md#supported-geographies).

6. Eftir að þú hefur ákveðið rétt umhverfi sem til að nota, getur þú haldið áfram með úthlutunarferlið. 

### <a name="supported-geographies"></a>Studdar staðsetningar

Human Resources styður eftirfarandi landfræðilegar staðsetningar eins og er:

- Bandaríkin
- Evrópa
- Bretland
- Ástralía
- Kanada
- Asía 

Þegar Human Resources umhverfi er stofnað er Power Apps valið sem umhverfi til að tengja við Human Resources umhverfið. Umhverfi Human Resources er síðan úthlutað á sömu Azure-staðsetningu og valið Power Apps-umhverfi. Hægt er að velja hvar umhverfi Human Resources og gagnagrunnur eru efnislega til staðar með því að velja landafræðilega staðsetningu þegar Power Apps-umhverfið er búið til sem verður tengt við umhverfi Human Resources.

Hægt er að velja *Landfræðilega staðsetningu* Azure þar sem umhverfinu er úthlutað, en ekki er hægt að velja tiltekið *svæði* Azure. Sjálfvirkni ákvarðar tiltekna svæðið innan landfræðilegrar staðsetningar þar sem umhverfið er stofnað til að fínstilla álagsjöfnun og afköst. Upplýsingar um landfræðilegar staðsetningar og svæði Azure er að finna í fylgigögnum á [Landfræðilegar staðsetningar Azure](https://azure.microsoft.com/global-infrastructure/geographies).

Gögnin fyrir umhverfi Human Resources mun alltaf verið haldið innan staðsetningar Azure þar sem það er búið til. Hins vegar verður það ekki alltaf í sama Azure-svæðinu. Í tilgangi endurheimtar eftir áfall verða gögnin afrituð á bæði aðalsvæði Azure og varasvæði innan staðsetningarinnar.

 > [!NOTE]
 > Ekki er hægt að flytja Human Resources-umhverfi frá einu Azure-svæði til annars.

## <a name="grant-access-to-the-environment"></a>Veita aðgang að umhverfinu

Að sjálfgefnu hefur altæki stjórnandinn sem bjó til umhverfið aðgang að því. Þú verður að veita sérstaklega aðgang til viðbótarnotenda forritsins. Þú verður að bæta við notendum og úthluta þeim viðeigandi hlutverkum í umhverfi Human Resources. Altæki stjórnandinn, sem virkjaði Human Resources, verður einnig að ræsa bæði Attract og Onboard til að ljúka frumstillingunni og virkja aðgang fyrir aðra leigunotendur. Þar til þetta gerist munu aðrir notendur ekki geta opnað Attract og Onboard og fá upp villur vegna brots á aðgangi. Frekari upplýsingar má finna í [Stofna nýja notendur](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) og [Úthluta notendum á öryggishlutverk](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
