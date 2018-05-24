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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 343e372ad9e29372649e975a5bee16e8913b66c8
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a>Úthluta Microsoft Dynamics 365 for Talent

[!include [banner](includes/banner.md)]

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
2. Talent er alltaf úthlutað inn í Microsoft PowerApps umhverfi, til að virkja PowerApps samþættingu og stækkunarhæfni. Lestu kaflann „Val á PowerApps umhverfi“ í þessu efnisatriði áður en þú heldur áfram. 
3. Ef þú ert ekki nú þegar með PowerApps umhverfi skaltu fylgja skrefunum í „Búa til nýtt PowerApps umhverfi (ef þörf krefur)“ hlutanum í þessum efnisatriði áður en þú heldur áfram.

    > [!NOTE]
    > Til að skoða núverandi umhverfi eða búa til ný umhverfi, verður leigjanda sem stjórnar, sem úthlutar Talent, að vera úthlutað á PowerApps P2 leyfið. Ef fyrirtækið þitt hefur ekki PowerApps P2 leyfi geturðu fengið slíkt frá þínu CSP eða [PowerApps verðlagsíðunni](https://powerapps.microsoft.com/en-us/pricing/).

4. Veldu **Bæta við** og veldu síðan umhverfið sem skal úthulta Talent inn í.
5. Veldu valkostinn „Hafa sýnigögn með“ ef þú vilt að umhverfið þitt innihaldi sama sýnigagnasafnið sem notað er í prufukeyrsluupplifun Talent.  Þetta er gagnlegt fyrir langvarandi prufuútgáfu eða þjálfunarumhverfi og ætti aldrei að nota í vinnsluumhverfi.  Athugaðu að þú verður að velja þennan möguleika við upphaflega uppsetningu og getur ekki seinna meir uppfært uppsetningu sem fyrir er.
6. Velja **Já** til að samþykkja skilmálana og hefja virkjun.

    Nýja umhverfið þitt birtist á lista yfir umhverfi á yfirlitssvæðinu vinstra megin. Hins vegar getur þú ekki byrjað að nota umhverfið fyrr en virkjunarstaða er uppfærð í **Virkjað**. Þetta ferli tekur alla jafna aðeins nokkrar mínútur. Ef úthlutunarferlið mistekst þarftu að hafa samband við notendaþjónustu.

7. Velja **Innskráning í Talent** til að nota nýja umhverfið þitt.

> [!NOTE]
> Ef þú hefur ekki ennþá skráð þig út á síðustu skilyrðin getur þú virkjað prufutilvik af Talent í verkinu. Þú getur síðan notað þetta tilvik til að prófa lausnina þína þar til þú skráir þig út. Ef þú notar nýtt umhverfi þitt til að prófa þarftu að endurtaka þetta ferli til að búa til framleiðsluumhverfi.

> [!NOTE]
> Þar sem aðeins tvö LCS-umhverfi eru leyfð sem hluti af Talent-áskriftinni getur þú einnig íhugað að nota ókeypis 60 daga [Talent prófunarumhverfi](https://dynamics.microsoft.com/en-us/talent/overview/). Þótt prófunarumhverfið sé í eigu notandans sem óskaði eftir því er samt hægt að bjóða öðrum notendum aðgang í gegnum upplifun kerfisstjóra fyrir mannauðskjarna. Prófunarumhverfi innihalda uppskálduð gögn sem hægt er að nota til að skoða forritið á öruggan hátt. Þau eru ætluð til þess að nota sem framleiðsluumhverfi. Athugaðu að þegar prófunarumhverfið rennur út að 60 dögum liðnum verður öllum gögnum í því eytt og ekki verður hægt að endurheimta þau. Þú getur skráð þig fyrir nýju prófunarumhverfi eftir að núverandi umhverfi rennur út.

## <a name="select-a-powerapps-environment"></a>Velja PowerApps umhverfi

Samþætting milli Talent og PowerApps umhverfa leyfir þér að samþætta og útvíkka notkun á Talent gögnum með PowerApps verkfærum. Skilningur á tilgangi PowerApps umhverfi hjálpar ekki aðeins við að búa til forrit til að stækka Talent, heldur einnig til að hjálpa þér að velja rétta umhverfið þegar þú úthlutar Talent. Frekari upplýsingar um PowerApps umhverfin, þ.á.m. umfang umhverfis, aðgangur að umhverfi og stofnun og val á umhverfi eru í [PowerApps umhverfi kynnt til sögunnar](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/). 

Notaðu eftirfarandi leiðbeiningar þegar þú ákveður hvaða PowerApps umhverfi til að virkja Talent inn í: 
1. Í LCS skaltu velja „Stjórna umhverfum“, eða fara beint í stjórnendamiðstöð PowerApps, þar sem þú getur skoðað núverandi umhverfi og stofnað ný umhverfi.
2. Einu Talent umhverfi er varpað á eitt PowerApps umhverfi.
3. PowerApps umhverfi „inniheldur“ Talent forritið, ásamt samsvarandi PowerApps, Flow og CDS forritum. Ef PowerApps umhverfinu er eytt, þá á það einnig við um forritin innan þess.
4. Gagnasamþætting og prófunaraðferðir ætti að hafa í huga, til dæmis: Sandbox, UAT, Framleiðsla. Þess vegna mælum við með því að þú hafir í huga ýmsar afleiðingar á uppsetningunni, því það er ekki auðvelt að breyta því síðar hvaða Talent umhverfi er varpað á PowerApps umhverfi.
5. Ekki er hægt að nota eftirfarandi PowerApps umhverfi fyrir Talent og verður síað úr vallistanum innan LCS:
 
    **CDS 2.0 umhverfi** CDS 2.0 verður gerð aðgengileg 21. mars 2018; hins vegar styður Talent ekki enn CDS 2.0. Þó að þú getir skoðað og búið til CDS 2.0 gagnagrunna í stjórnunarmiðstöð PowerApps, þá munu þeir ekki vera nothæfir í Talent. Valmöguleikinn á að nota CDS 2.0 umhverfi í Talent uppsetningum verður í boði seinna meir.
   
   > [!Note]
   > Til að greina á milli CDS 1.0 og 2.0 umhverfi í stjórnunargáttinni skaltu velja umhverfi og skoða **Upplýsingar**. CDS 2.0 umhverfi vísa öll til þeirrar staðreyndar að „Þú getur stjórnað þessum stillingum í stjórnunarmiðstöð Dynamics 365,“ bendir á útgáfutilvik og hefur engan gagnagrunnsflipa. 
 
   **Sjálfgefin PowerApps umhverfi** Þó að hverjum leigjanda sé sjálfkrafa úthlutað sjálfgefnu PowerApps umhverfi, mælum við ekki með því að nota það með Talent þar sem allir leigunotendur hafa aðgang að PowerApps umhverfi og geta óvart spillt framleiðslugögnum þegar þeir prófa og kanna samþættingar PowerApps eða Flow.
   
   <strong>Prufukeyrsla umhverfa</strong> Umhverfi með heiti eins og „TestDrive - alias@domain„ eru búin til með 60 daga gildistíma og lýkur eftir þann tíma og veldur því að umhverfinu þínu verði eytt sjálfkrafa.
   
   **Óstudd svæði** Að svo stöddu er Talent aðeins stutt á eftirfarandi svæðum: Bandaríkjunum, Evrópu eða Ástralíu.
  
6. Það þarf ekki að grípa til neinnar sérstakrar aðgerðar þegar þú hefur ákveðið rétt umhverfi til notkunar. Halda áfram með ráðstöfunarferlinu. 
 
## <a name="create-a-new-powerapps-environment-if-required"></a>Búa til nýtt PowerApp umhverfi (ef þörf krefur)

Keyra PowerShell forskrift til að búa til nýtt PowerApps umhverfi fyrir Talent í samhengi við stjórnanda leigjandans sem hefur PowerApps áskrift 2 leyfi. Forskriftin gerir eftirfarandi skref sjálfvirk:


 + Stofnun á PowerApps umhverfi
 + Stofnun á CDS 1.0 gagnagrunni
 + Hreinsar öll sýnigögn í gagnagrunni CDS 1.0


Ljúktu eftirfarandi leiðbeiningum til að keyra forskriftina:

1. Sækja skrána ProvisionCDSEnvironment.zip frá eftirfarandi staðsetningu: [ProvisionCDSEnvironment scripts](https://go.microsoft.com/fwlink/?linkid=870436)  

2. Frá niðurhalsmöppunni skaltu hægrismella á ProvisionCDSEnvironment.zip skrána sem sótt var rétt í þessu og velja **Eiginleikar**.  Ef athugasemd um öryggi er neðst í glugganum sem segir „Þessi skrá kom frá annarri tölvu og gæti verið lokað á til að vernda þessa tölvu“ skaltu merkja gátreitinn sem **Opna fyrir**, síðan smella á **Nota** og síðan **Í lagi**.

3. Afþjappaðu öllu innihaldi ProvisionCDSEnviroinment.zip skráarinnar í möppu, annarri en rótarmöppunni þinni.

4. Keyrðu Windows PowerShell eða Windows PowerShell ISE forritið sem stjórnandi.

   Farðu í efnisatriðið [Stilla notkunarreglu](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-executionpolicy?view=powershell-6) til að fræðast meira um stillingu notkunarreglu þannig að hægt sé að keyra forskriftir. Við mælum með því að nota eftirfarandi, „Set-ExecutionPolicy -ExecutionPolicy Unrestricted -Scope Process“, en vertu viss um að fylgja öryggisstefnu fyrirtækisins og lokaðu PowerShell glugganum þegar lokið. 
  
5. Innan PowerShell, flettu að möppunni þar sem þú afþjappaðir skránni og keyrðu eftirfarandi skipun, skiptu út gildum eins og er leiðbeint hér að neðan:
 
   ```.\ProvisionCDSEnvironment -EnvironmentName MyNewEnvironment -Location YourLocation```

    
   **MyNewEmvironment** ætti að vera skipt út fyrir umhverfisheiti þitt. Þetta heiti birtist í LCS og verður sýnilegt þegar notendur velja hvaða Talent umhverfi skuli nota. 

   **Þín staðsetning** ætti að vera skipt út fyrir eitt af studdu svæðunum fyrir Talent: Bandaríkjunum, Evrópu, Ástralíu. 

   **-Verbose** er valfrjálst og mun veita nákvæmar upplýsingar til að senda til stuðnings ef vandamál koma upp.

6. Halda áfram með ráðstöfunarferlinu.
 

## <a name="grant-access-to-the-environment"></a>Veita aðgang að umhverfinu
Að sjálfgefnu hefur altæki stjórnandinn sem bjó til umhverfið aðgang að því. Hins vegar þarf sérstaklega að veita öðrum notendum forritsins aðgang. Til að veita aðgang skal [bæta við notendur](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) og [úthluta þeim viðeigandi hlutverkum](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles) í kjarnaumhverfi mannauðs. Altæki stjórnandinn, sem virkjaði Talent, verður einnig að ræsa bæði forritin Attract og Onboard til að ljúka frumstillingunni og virkja aðgang fyrir aðra leigunotendur.  Þar til þetta gerist munu aðrir notendur ekki geta opnað forritin Attract og Onboard og fá upp villur vegna brots á aðgangi.


