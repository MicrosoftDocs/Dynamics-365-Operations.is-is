---
title: Franskt Intrastat
description: Þetta efnisatriði inniheldur upplýsingar um Intrastat-skattskýrslu í Frakklandi.
author: anasyash
ms.date: 07/9/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: ''
ms.openlocfilehash: 4d38576e1c6b40242d5c6313fb06f08e170b4466
ms.sourcegitcommit: 7a2001e4d01b252f5231d94b50945fd31562b2bc
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/15/2021
ms.locfileid: "7487901"
---
# <a name="french-intrastat"></a>Franskt Intrastat

[!include[banner](../includes/banner.md)]

Fyrirtæki í Frakklandi sem eru skráð fyrir virðisaukaskatti (VSK) og sem stunda viðskipti við önnur lönd innan Evrópusambandsins (ESB) verða að tilkynna vöru- og þjónustuskipti til og frá Frakklandi. Declaration d'exchanges de biens (yfirlýsing um viðskipti með vörur eða DEB) er samsetning sölulista ESB og Intrastat-skýrslunnar. Þú verður að skila þessari skýrslu mánaðarlega fyrir alla sölu á vörum innan samfélagsins.

Hægt er að búa til DEB-skýrsluna á öðru af tveimur rafrænum textaskrársniðum: SAISUNIC 330 eða INTRACOM-sniði.

Eftirfarandi tafla sýnir reitina sem eru innifaldir í frönsku Intrastat-skattskýrslunni á SAISUNIC 330-sniði. Taflan tilgreinir einnig skýrslustig reitsins. Reiturinn getur verið **4** (einfaldaður), **1** (heildar) eða bæði.

| **Svæði**                   | **Skýrslustig** |
|-----------------------------|------------------|
| Tímabil tilvísunar         | 4, 1              | 
| Fjöldi yfirlýsinga       | 4, 1              |
| Línunúmer                 | 4, 1              |
| ISO-kóði lands (FR)       | 4, 1              | 
| Viðbótarkóði          | 4, 1              | 
| Siren-númer                | 4, 1              | 
| VSK-kóði viðskiptavinar        | 4, 1              | 
| Stefnukóði              | 4, 1              |
| Færslugerð            | 4, 1              | 
| Skyldustig            | 4, 1              |
| Vörukóði              | 1                | 
| NGP innanlands                | 1                | 
| Sýsla (deild)         | 1                |
| Eðli færslu       | 1                | 
| Upprunaland      | 1                | 
| Upprunaland - Innflutningar | 1                | 
| Lokaáfangastaður - Útflutningar | 1                | 
| Reikningsvirði               | 4, 1              | 
| Upplýsingagildi           | 1                |
| Nettóþyngd                  | 1                | 
| Viðbótareiningar            | 1                |
| Flutningskóði              | 1                | 

Eftirfarandi tafla sýnir reitina sem eru innifaldir í frönsku Intrastat-skattskýrslunni á INTRACOM-sniði.
Taflan tilgreinir einnig skýrslustig reitsins. Reiturinn getur verið **4** (einfaldaður), **1** (heildar) eða bæði.

| **Svæði**                   | **Skýrslustig**   | 
|-----------------------------|--------------------|
| Kóði                        | 4, 1               | 
| Fjöldi yfirlýsinga       | 4, 1               |
| Fjöldi lína              | 4, 1               | 
| Sírena                       | 4, 1               |
| Sýsla (deild)         | 1                  |          
| Flutningskóði              | 1                  |          
| Upprunaland           | 1                  |            
| Eðli færslu       | 1                  |             
| Reikningsvirði               | 4, 1               |             
| Afhendingarmátar           | 1                  |           
| Færslugerð            | 4, 1               |            
| Skyldustig            | 4, 1               |           
| Vörukóði              | 1                  |            
| NGP innanlands                | 1                  |            
| Nettóþyngd                  | 1                  |            
| Upplýsingagildi           | 1                  |            
| Viðbótareiningar            | 1                  |            
| Upprunaland - Innflutningar | 1                  |            
| Lokaáfangastaður - Útflutningar | 1                  |            
| VSK-kóði viðskiptavinar        | 4, 1               |            
| Viðbótarkóði          | 4, 1               |           
| Tímabil tilvísunar         | 4, 1               |         

### <a name="set-up-intrastat"></a>Setja upp Intrastat

1.  Í [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index), í sameiginlega eignasafninu, skaltu sækja nýjustu útgáfur af eftirfarandi stillingum fyrir rafræna skýrslugerð fyrir Intrastat-skattskýrsluna:

    - Intrastat-líkan
    - Intrastat-skýrsla
    - Intrastat-INTRACOM (FR)
    - Intrastat-SAISUNIC (FR)

    Frekari upplýsingar eru í [Niðurhal skilgreininga fyrir rafræna skýrslugerð af Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

2.  Í Dynamics 365 Finance skal fara í **Skattur** > **Uppsetning** >  **Erlend viðskipti** > **Færibreytur erlendra viðskipta** og fylgja þessum skrefum:

    1. Í flipanum **Intrasta**, í flýtiflipanum **Rafræn skýrslugerð**, í reitnum **Vörpun skráarsniðs**, skal velja **Intrastat-INTRACOM (FR)** eða **Intrastat-SAISUNIC (FR)**.
    2. Í reitnum **Vörpun skýrslusniðs** skal velja **Intrastat skýrslu**.
    3. Í flýtiflipanum **Stigveldi vörukóða**, í reitnum **Tegundastigveldi**, velja **Intrastat**.
    4. Í flýtiflipanum **Almennt**, í reitnum **Færslukóði**, skal velja kóðann sem er notaður fyrir flutning á vörum.
    5. Í reitnum **Kreditreikningur** skal velja kóðann sem er notaður fyrir vöruskil.
    6. Í reitnum **Skyldustig fyrir útflutning** skal færa inn stig upplýsinga fyrir skýrslu útflutnings. Stigið sem þú velur hefur áhrif á línurnar sem sýndar eru í skýrslunni. Frekari upplýsingar er að finna í töflum í upphafi efnisatriðisins.

3. Farðu í **Fyrirtækisstjórnun** > **Fyrirtæki** > **Lögaðilar**, veldu fyrirtækið þitt og fylgdu síðan þessum skrefum:

    1. Í flýtiflipanum **Skráningarnúmer**, í reitnum **NAF-kóði**, skal færa inn NAF-kóðann. Frekari upplýsingar er að finna í [FR-00003 NAF-kóðar og siret-númer](tasks/fr-00003-naf-codes-siret-numbers.md).
    2. Í flýtiflipanum **Erlend viðskipti og vörustjórnun**, í hlutanum **Intrastat**, skal stilla reitina **VSK-undanþágunúmer útflutnings** og **VSK-undanþágunúmer innflutnings**.
    3. Í flýtiflipanum **Skattskráning**, í reitnum **Skattskráningarnúmer**, skal tilgreina skattskráningarnúmer fyrirtækisins.

4. Til að tilgreina NAF-kóða og skattundanþágunúmer fyrir viðskiptavini skal fara í **Viðskiptakröfur** > **Viðskiptavinir** > **Allir viðskiptavinir** og fylgja þessum skrefum:

    1. Veljið viðskiptavin.
    2. Í flýtiflipanum **Reikningur og afhending**, á síðunni **Söluskattur**, í reitnum **Skattundanþágunúmer**, skal færa inn skattundanþágunúmer viðskiptavinar.
    3. Í flýtiflipann **Lýðfræðiupplýsingar sölu**, í reitinn **Franskt Siret**, skal færa inn Siret-númer fyrirtækisins.
    4. Í reitinn **NAF-kóði** skal færa inn NAF-kóða fyrirtækisins.
    5. Endurtaktu skrefin fyrir aðra viðskiptavini.

5. Til að tilgreina NAF-kóða og skattundanþágunúmer fyrir lánardrottna skal fara í **Viðskiptaskuldir** > **Lánardrottnar** > **Allir lánardrottnar** og fylgja þessum skrefum:

    1. Veljið lánardrottin.
    2. Í flýtiflipanum **Reikningur og afhending**, á síðunni **Söluskattur**, í reitnum **Skattundanþágunúmer**, skal færa inn skattundanþágunúmer lánardrottins.
    3. Í flýtiflipann **Lýðfræðiupplýsingar innkaupa**, í reitinn **Franskt Siret**, skal færa inn Siret-númer fyrirtækisins.
    4. Í reitinn **NAF-kóði** skal færa inn NAF-kóða fyrirtækisins.
    5. Endurtaktu skrefin fyrir aðra lánardrottna.

6. Farðu í **Skattur**  >  **Uppsetning**  >  **Erlend viðskipti**  >  **Intrastat-þjöppun** og veldu reitina sem á að bera saman þegar Intrastat-upplýsingar eru teknar saman. Fyrir franskt Intrastat skal velja **Vinnsla talnagagna**, **Upprunaríki**, **Land/svæði uppruna**, **Afhendingarskilmálar**, **Flutningur**, **Leiðrétting**, **Land/svæði**, **Upprunaland/áfangastaður**, **Stefna**, **Land/svæði sendanda**, **Ríki sendanda**, **Ríki**, **Færslukóði** og **Vara**.

7. Farðu í **Vöruhúsakerfi** > **Uppsetning** > **Vöruhús** > **Vöruhús**, veldu vöruhús og fylgdu síðan þessum skrefum:

    1. Í flýtiflipanum **Aðsetur** skal velja **Ítarlegt** eða **Breyta**.
    2. Í svarglugganum, í reitnum **Borg**, skal velja borg vöruhússins. Fylki borgarinnar verður notað sem sýsla fyrir DEB-skýrsluna.

### <a name="ngp-codes"></a>NGP-kóðar

Í DEB-skýrslunni samanstendur kóðun á vörum af eftirfarandi einingum:

  - Átta stafa CN8-kóðinn sem táknar toll og tölfræðileg nafnakerfi Evrópusambandsins.
  - Ef við á, eintölu nafngift innanlands vörukóða Générale des Produits (NGP).

Árið 2021 á NGP aðeins við um þrjár afurðategundir:

  - Sumar afurðir af kúm, kindum og geitum
  - Herbúnaður
  - Frönsk vín

 Setja þarf upp NGP-kóða og úthluta þeim á tengdar afurðir. Reiturinn **NGP** er síðan sjálfkrafa stilltur á síðuna **Intrastatbók**.

#### <a name="set-up-an-ngp-code"></a>Setja upp NGP-kóða

1. Farðu í **Skattur** > **Uppsetning** > **Erlend viðskipti** > **NGP-kóðar**.
2. Á aðgerðasvæðinu skal velja **Nýr** til að búa til NGP-kóða.
3. Í reitinn **NGP** skal færa inn einstafa kóða.
4. Í reitinn **Lýsing** skal færa inn lýsingu fyrir kóðann.

#### <a name="assign-an-ngp-code-to-a-product"></a>Úthluta NGP-kóða á afurð

1. Opna **Afurðaupplýsingastjórnun** > **Afurðir** > **Útgefnar afurðir**.
2. Í hnitanetinu skal velja afurð.
3. Í flýtiflipanum **Erlend viðskipti**, í hlutanum **Intrastat**, í reitnum **NGP**, skal velja viðeigandi NGP-kóða.

## <a name="intrastat-journal"></a>Intrastatbók

Farðu í **Skattur** > **Skattskýrslur** > **Erlend** **viðskipti** > **Intrastat** til að stjórna færslunum sem eiga við um erlend viðskipti við lönd innan Evrópusambandsins. Frekari upplýsingar er að finna í [Intrastat-yfirlit](emea-intrastat.md).

Dálkurinn **NGP** á við um Frakkland. Hann sýnir NGP-kóða afurðarinnar. Ef NGP á ekki við um afurð er **0** (núll) sýnt. Þú getur breytt NGP-kóðanum. Veldu færsluna og síðan í flipanum **Almennt**, í hlutanum **Kóðar**, í reitnum **NGP**, skal velja nauðsynlegan NGP-kóða.

### <a name="intrastat-transfer"></a>Intrastat-flutningur

Á síðunni **Intrastat** á aðgerðasvæðinu er hægt að velja **Flutningur** til að flytja sjálfkrafa upplýsingarnar um viðskipti innan samfélags úr sölupöntunum, textum með frjálsum texta, innkaupapöntunum, lánardrottnareikningum, innhreyfingarskjölum afurða lánardrottins, verkreikningum og flutningspöntunum. Aðeins skjöl sem hafa ESB-land sem land eða svæði áfangastaðar (fyrir sendingar) eða vörusendingu (fyrir komur) verða flutt.

Þar sem DEB-skýrslan er samsetning af sölulista ESB og Intrastat-skýrslu, felur hún einnig í sér *þríhliða* færslur, þar sem bein afhending er gerð frá einu ESB-landi (aðila A) til annars ESB-lands (aðila C), og franskur lögaðili (aðili B) er á milli í þríhliða samningnum.

### <a name="generate-a-deb-intrastat-report"></a>Búa til DEB (Intrastat) skýrslu

1. Farðu í **Skattur**  >  **Skattskýrslur**  >  **Erlend viðskipti**  >  **Intrastat**.
2. Á aðgerðasvæðinu skal velja **Úttak**  >  **Skýrsla**.
3. Í svarglugganum **Intrastat skýrsla** skal stilla eftirfarandi reiti.

    | Svæði            | lýsing                                                                                                                         |
    |------------------|-------------------------------------------------------------------------------------------------------------------------------------|
    | Frá degi        | Veldu upphafsdagsetningu fyrir skýrsluna.                                                                                               |
    | Til dags.          | Veldu lokadagsetningu fyrir skýrsluna.                                                                                                 |
    | Mynda skrá    | Stilltu þennan valkost á **Já** til að búa til .txt-skrá.                                                                                 |
    | Skrárnafn        | Færðu inn heiti .txt-skráar fyrir Intrastat-skýrsluna.                                                                          |
    | Búa til skýrslu  | Stilltu þennan valkost á **Já** til að búa til .xml-skrá.                                                                                |
    | Heiti skýrsluskráar | Færðu inn nauðsynlegt heiti.                                                                                                            |
    | Aðeins leiðréttingar | Stilltu þennan valkost á **Já** til að tilkynna aðeins leiðréttingar. Stilltu hann á **Nei** til að tilkynna bæði eðlilegar færslur og leiðréttingar.         |
    | Stefna        | Veldu **Komur** til að fá skýrslu um komur innan samfélags. Veldu **Sendingar** til að fá skýrslu um sendingar innan samfélags. |

## <a name="example"></a>Dæmi

Eftirfarandi dæmi sýnir hvernig á að setja upp franskt Intrastat og búa til DEB-skýrsluna. Það notar **DEMF** lögaðilann.

1. Í [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index), í sameiginlega eignasafninu, skaltu sækja nýjustu útgáfur af eftirfarandi stillingum fyrir rafræna skýrslugerð fyrir Intrastat-skattskýrslusniðið:

    - Intrastat-líkan
    - Intrastat-skýrsla
    - Intrastat-INTRACOM (FR)

2. Í Finance skal setja upp færslukóða:

    1. Farðu í **Skattur** > **Uppsetning** > **Erlend viðskipti** > **Færslukóðar**.
    2. Í aðgerðarúðunni velurðu **Nýtt**.
    3. Í reitinn **Færslukóði** skal færa inn **11**.
    4. Í reitinn **Heiti** skal færa inn **Innkaup eða sala**.
    5. Í aðgerðarúðunni skal velja **Vista**.

3.  Settu upp afurðastigveldi:

    1. Farðu í **Afurðaupplýsingastjórnun** > **Uppsetning** > **Flokkar og eigindir** > **Flokkastigveldi**.
    2. Í hnitanetinu skal velja **Intrastat**. Á aðgerðasvæðinu, í flipanum **Flokkastigveldi**, í flokknum **Viðhalda**, skal síðan velja **Breyta**.
    3. Á aðgerðasvæðinu skal velja **Nýr tegundarhnútur**.
    4. Í reitinn **Heiti** skal færa inn **Autres Libournais**.
    5. Í reitinn **Kóði** skal færa inn **2204 21 42**
    6. Í aðgerðarúðunni skal velja **Vista**.

4. Farðu í **Skattur** > **Uppsetning** > **Erlend viðskipti** > **Færibreytur erlendra viðskipta** og fylgdu þessum skrefum:

    1. Í flýtiflipanum **Intrastat**, í flýtiflipanum **Almennt**, í reitnum **Færslukóði**, skal velja **11**.
    2. Í flýtiflipanum **Rafræn skýrslugerð**, í reitnum **Vörpun skráarsniðs**, skal velja **Intrastat-INTRACOM (FR)**.
    3. Í reitnum **Vörpun skýrslusniðs** skal velja **Intrastat skýrslu**.
    4. Í flýtiflipanum **Stigveldi vörukóða**, í reitnum **Tegundastigveldi**, velja **Intrastat**.

5. Settu upp NGP-kóða:

    1. Farðu í **Skattur** > **Uppsetning** > **Erlend viðskipti** > **NGP-kóðar**.
    2. Í aðgerðarúðunni velurðu **Nýtt**.
    3. Í reitinn **NGP** skal færa inn **8**.
    4. Í reitinn **Heiti lýsingar** skal færa inn **NGP 8**.
    5. Í aðgerðarúðunni skal velja **Vista**.

6. Úthlutaðu NGP-kóðanum á afurð:

    1. Opna **Afurðaupplýsingastjórnun** > **Afurðir** > **Útgefnar afurðir**.
    2. Í hnitanetinu skal velja **0001**.
    3. Í flýtiflipanum **Erlend viðskipti**, í reitnum **NGP**, skal velja **8**.
    4. Í reitnum **Vara** skal velja **2204 21 42**.
    5. Í aðgerðarúðunni skal velja **Vista**.

7. Stofnaðu sölupöntun sem inniheldur nýju afurðina:

    1. Farið í **Viðskiptakröfur**  >  **Pantanir**  >  **Allar sölupantanir**.
    2. Í aðgerðarúðunni velurðu **Nýtt**.
    3. Í svarglugganum **Stofna** **sölu** **pöntun**, í hlutanum **Viðskiptavinur**, í reitnum **Viðskiptavina** **lykill**, skal velja **100001**.
    4. Í hlutanum **Aðsetur**, í reitnum **Afhendingaraðsetur**, skal velja plúsmerkið (**+**) til að búa til aðsetur.
    5. Í svarglugganum **Nýtt aðsetur**, í reitinn **Heiti lýsingar**, skal færa inn **Þýskaland**.
    6. Í reitnum **Land/svæði** skal velja **DEU**.
    7. Veldu **Í lagi**.
    8. Í svarglugganum **Stofna sölupöntun** skal velja **Í lagi**.
    9. Í flýtiflipanum **Sölu** **pöntunarlínur**, í reitnum **Vörunúmer**, skal velja **0001**.
    10. Í aðgerðarúðunni skal velja **Vista**.
    11. Á aðgerðasvæðinu, í flipanum **Reikningur**, í flokknum **Búa til** skal velja á **Reikningur**.
    12. Í svarglugganum **Bókun reiknings**, í flýtiflipanum **Færibreytur**, í hlutanum **Færibreyta**, í reitnum **Magn**, skal velja **Allt**. Veldu svo **Í lagi** til að bóka reikninginn.

8.  Stofnaðu DEB-skýrsluna:

    1. Farðu í **Skattur** > **Skattskýrslur** > **Erlend viðskipti** > **Intrastat**:
    2. Á aðgerðasvæðinu. veldu **Flutningur**.
    3. Í svarglugganum **Intrastat (flutningur)**, í hlutanum **Færibreytur**, skal stilla valkostinn **Reikningur viðskiptavinar** á **Já**. Veljið síðan **Í lagi**.
    4. Raðaðu færslunum með reitnum **Dagsetning**. Efsta færslan er niðurstöðufærslan. Reiturinn **NGP** er stilltur sjálfkrafa.
    5. Á aðgerðasvæðinu skal velja **Úttak** &gt; **Skýrsla**.
    6. Í svarglugganum **Intrastat skýrsla**, í flýtiflipanum **Færibreytur**, í hlutanum **Dagsetning**, skal velja mánuð sölupöntunarinnar sem var stofnuð.
    7. Í hlutanum **Valkostir útflutnings** skal stilla valkostinn **Mynda skrá** á **Já**.
    8. Í reitinn **Skráarheiti** skal færa inn nauðsynlegt heiti.
    9. Veldu **Í lagi** og farðu yfir skýrsluna.

