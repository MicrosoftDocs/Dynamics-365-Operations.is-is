---
title: "Skilgreina kostnaðarstýringu"
description: "Þetta grein lýsir umhugsunarefni og ákvarðanir sem þarf að taka í áætlunarferli, áður en hægt er að stilla kostnaðarstjórnun í Microsoft Dynamics AX. Í kostnaðarstjórnunarsvæði, er hægt að geyma upplýsingar um greiðslumáta, ferðabeiðnir, kostnaðarskýrslur og stefnur, meðal annars."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 447ba56a279a29392b00119730c3594fa4ea80f6
ms.contentlocale: is-is
ms.lasthandoff: 04/25/2017


---

# <a name="configure-expense-management"></a>Skilgreina kostnaðarstýringu

[!include[banner](../includes/banner.md)]


Þetta grein lýsir umhugsunarefni og ákvarðanir sem þarf að taka í áætlunarferli, áður en hægt er að stilla kostnaðarstjórnun í Microsoft Dynamics AX. Í kostnaðarstjórnunarsvæði, er hægt að geyma upplýsingar um greiðslumáta, ferðabeiðnir, kostnaðarskýrslur og stefnur, meðal annars. 

Þar sem margar þeirra ákvarðana sem gerðar eru við að áætla samskipan fyrir kostnaðarstýringu byggjast á stigveldi og fjárhagslegu skipulagi fyrirtækisins, verður að vísa til skipulagningarskjala fyrir þau svæði.

## <a name="intercompany-expenses"></a>Kostnaður innan samstæðu
Þegar kostnaður innan samstæðu er virkjaður, er lögaðilum og starfsmönnum leyft að stofna til kostnaðar fyrir hönd, og innheimta greiðslur frá, öðrum lögaðila innan fyrirtækisins. Til dæmis lýkur starfsmaður hjá lögaðila A verki fyrir lögaðilann B. Ef kostnaður innan samstæðu eru virkjaður getur starfsmaðurinn svo skráð tímablað á og verið greitt frá lögaðila B. Ef fyrirtækið hefur ekki marga lögaðila þarf ekki að virkja kostnað innan samstæðu. **Ákvörðun:** Á að virkja kostnað innan samstæðu?

## <a name="financial-management"></a>Fjármálastjórnun
Kostnaðarstýring er samþætt náið með fjárhagslegar umsjón fyrirtækis þíns. Mikið af stillingum fyrir kostnaðarstýringu munu byggjast á ákvörðunum sem teknar voru um fjármál fyrirtækisins. Eftirfarandi kaflar lýsa mismunandi svæðum sem krefjast áætlanagerðar og ákvarðana samkvæmt fjárhagslegum ákvörðunum og leiðbeiningum frá leiðtogateymi fyrirtækisins.

### <a name="per-diems"></a>Dagpeningar

Skilgreina verður dagpeningana sem fyrirtækið veitir starfsmanninum. Þar sem dagpeningar eru vanalega notaðir til að ná yfir útgjöld, eins og fæði, leiguhúsnæði og annan tilfallandi kostnað, er hægt að stofna reglur fyrir dagpeningaheimildir sem fyrirtækið býður. Dagpeningataxti getur byggt á árstíma, ferðastað eða hvoru tveggja. Þegar dagpeningaregla er skilgreind er hægt að tilgreina að prósenta af dagpeningataxta verði haldið eftir ef starfsmaður fær ókeypis fæði eða þjónustu. Einnig er hægt að skilgreina lög af dagpeningataxta til að setja lágmarks- og hámarksfjölda klukkustunda sem hægt er að beita á ferðalög starfsmanns. **Ákvarðanir:**

-   Sjálfgefnar reglur fyrir dagpeninga fyrir fyrsta og síðasta daga:
    -   Hver er lágmarksfjöldi stunda sem starfsmaður getur krafist á dag og fengið dagpeningar fyrir?
    -   Er lækkun á þeirri upphæð sem er í boði fyrir máltíðir fyrir fyrsta og síðasta dag? Ef svo er, hversu hátt er hlutfall lækkunarinnar?
    -   Er lækkun á þeirri upphæð sem er í boði fyrir hótel fyrir fyrsta og síðasta dag? Ef svo er, hversu hátt er hlutfall lækkunarinnar?
    -   Er lækkun á þeirri upphæð sem er í boði fyrir annan kostnað fyrir fyrsta og síðasta dag? Ef svo er, hversu hátt er hlutfall lækkunarinnar?
-   Sjálfgefnar reglur fyrir dagpeninga:
    -   Er prósentulækkun á dagpeningaheimild fyrir hverja máltíð, ef máltíðin er t.d. ókeypis? Ef svo er, hvert er lækkunarhlutfallið fyrir hverja máltíð?
    -   Er lækkun fæðispeninga reiknuð á dag, hverja ferð eða fjölda máltíða á dag?
    -   Eiga dagpeningaupphæðir að vera sléttaðar venjulega eða sléttaðar upp?
    -   Eru dagpeningar reiknaðir á grundvelli 24 klst. tímabils eða almanaksdags?
-   Reglur um dagpeninga samkvæmt staðsetningu:
    -   Er munur á dagpeningataxta eftir staðsetningu og hvaða staðsetningar eru teknar með?
    -   Ef munur er dagpeningataxta eftir staðsetningu, fyrir hverja staðsetningu, á grundvelli hvaða prósentuhlutfallið er veitt fyrir:
        -   fæði
        -   hótel
        -   annar kostnaður

### <a name="expense-management-journals-and-accounts"></a>Útgjaldastýringarbækur og -lyklar

Útgjaldastýring krefst þess að notaðar séu margar færslubækur og lyklar. Það verður til dæmis að ákveða hvort sami lykillinn er notaður fyrir fyrirframgreiðslur og ágreining kreditkorts. **Ákvarðanir:**

-   Hvaða færslubók á að bóka samþykktar útgjaldaskýrslur í?
-   Hvaða lykill er notaður fyrir fyrirframgreiðslur?
-   Á að bóka fyrirframgreiðslur strax?

### <a name="payment-methods"></a>Greiðslumátar

Þegar starfsmönnum er leyft að stofna til kostnaðar fyrir hönd fyrirtækisins, verður að skilgreina greiðslumáta sem starfsmönnum er heimilt að nota. Til dæmis væri hægt að leyfa starfsmönnum að nota reiðufé eða kreditkort fyrirtækisins. Einnig væri hægt að leyfa starfsmönnum að nota persónuleg kreditkort og endurgreiða þeim síðan. Gera verður eftirfarandi ákvarðanir fyrir hvern greiðslumáta sem á að leyfa. **Ákvarðanir:**

-   Hvaða greiðslumátar eru heimilaðir?
-   Hver á útgjöld greiðslumátans?
-   Er gerð mótlykils til staðar? Ef svo er, hver er hún?
-   Ef mótlykill er til staðar, hver er lykillinn?
-   Ef greiðslumátinn er kreditkort, á einungis að nota greiðslumátann með innfluttum kreditkortafærslum?

### <a name="expense-categories-and-shared-categories"></a>Útgjaldaflokkar og samnýttir flokkar

Þegar starfsmenn stofna kostnaðarskýrslu, verða hver útgjöld sem þeir skrá að vera tengd við útgjaldaflokk. Kostnaðartegundir eru afleiddar af samnýttum flokkum sem hægt er að deila með lögaðilum innan fyrirtækisins. Einnig er hægt að samnýta þessar tegundir í verkstjórnun og bókhaldi, allt eftir því hvernig fyrirtækið er skilgreint. Samkvæmt grunni skilgreiningar fyrirtækisins og leiðbeiningr frá framkvæmdahópnum þarf að ákvarða hvort aðeins skuli nota flokkana sem eru notaðir í útgjaldastýringu á útgjöld eða hvort samnýta eigi þá milli Verkefnis og Kostnaðar. Athugaðu að þessar tegundir er hægt að samnýta milli Verks og Kostnaðar eða Verks og Framleiðslu, en ekki á milli Kostnaðar og Framleiðslu. Taka verður eftirfarandi ákvarðanir fyrir hverja kostnaðartegund. **Ákvarðanir:**

-   Hver er kostnaðarflokkurinn? Til dæmis flug, hótel eða vegalengd.
-   Er einnig hægt að nota þessa kostnaðartegund í Verkefnastjórnun og bókhaldi?
-   Hver er kostnaðartegundin?
-   Hver er sjálfgefinn greiðslumáti fyrir kostnaðartegunda?
-   Þarf kostnaður í þessari tegund að vera sundurliðaður?
-   Hver er sjálfgefinn lykill fyrir kostnaðartegundina?
-   Hver er sjálfgefinn VSK-flokkur vöru fyrir kostnaðartegunda?
-   Eru viðbótar greiðslumátar leyfðir fyrir kostnaðartegunda? Ef svo er, hverjir eru þeir?
-   Eru undirtegundir innan þessarar kostnaðartegundar? Ef svo er:
    -   Er einhverjum undirtegundum sleppt úr skattendurgreiðslum?
    -   Hver er VSK-flokkur vöru fyrir undirtegundirnar?

    Ef þessi kostnaðartegund er einnig notuð í verkstjórnun og bókhaldi, þarf að svara eftirstandandi spurningum. Annars er þessum hluta lokið.
-   Hvaða kostnaðarlyklar verða notaðir fyrir eftirfarandi?
    -   Kostnaður
    -   Launaskipting
    -   VÍV - Kostnaðarverðmæti
    -   Kostnaður - Vara
    -   VÍV - Kostnaðarvirði - Vara
    -   Uppsafnað tap
    -   VÍV - Uppsafnað tap
-   Hvaða tekjulyklar verða notaðir fyrir eftirfarandi?
    -   Reikningsfærðar tekjur
    -   Áfallnar tekjur - Söluverðmæti
    -   VÍV - söluvirði
    -   Áfallnar tekjur - Framleiðsla
    -   VÍV - Framleiðsla
    -   Áfallnar tekjur - Hagnaður
    -   VÍV - Hagnaður
    -   Áfallnar tekjur - Áskrift
    -   VÍV - Áskrift

 

### <a name="taxes"></a>Skattar

Fyrir kostnað sem tengist sköttum verður að ákvarða hvað er tekið með eða virkjað í kostnaðarskýrslum. **Ákvarðanir:**

-   Er virðisaukaskattur innifalinn í upphæð kostnaðar?
-   Á að virkja skattendurgreiðslur í útgjöldum?

Athugið að ef, við áætlun í fjárhag, þú hefur ákveðið að nota bandarískan virðisaukaskatt og reglur neysluskatts, sem er gert með því stilla reitinn **Beita skattlagningarreglur virðisaukaskatts** á Já, er hægt að virkja skattendurgreiðslu á útgjöldum.

## <a name="policies"></a>Reglur
Hægt er að stofna kostnaðarskýrslureglur svo að fyrirtækið geti sparað peninga og tíma þegar starfsmenn stofna til útgjalda fyrir hönd þess. Reglur tryggja að starfsmenn séu innan fjárhagsáætlunar, veiti allar nauðsynlegar upplýsingar og eyði aðeins fé eftir þörfum. Taka verður eftirfarandi ákvarðanir fyrir hverja kostnaðarreglu og hverja samþykktarreglu kostnaðarskýrslu sem þú stofnar. **Ákvarðanir:**

-   Hvert er heiti reglunnar?
-   Til hvers er kostnaðarreglan?
-   Ef þú ákvaðst áður að virkja kostnað innan samstæðu, fyrir hvaða fyrirtæki í samstæðunni á þessi regla við?
-   Hvenær verður reglan virk?
-   Hvenær verður úreldist reglan?
-   Hvað er stefnuregla?
-   Hver er útkoma stefnureglunnar?





