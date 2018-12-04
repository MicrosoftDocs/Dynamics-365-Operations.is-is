---
title: "Skilgreina kostnaðarstýringu"
description: "Þessi grein lýsir því sem þarf að hafa í huga og ákvörðunum sem þarf að taka í áætlunarferli áður en hægt er að skilgreina kostnaðarstýringu í Microsoft Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: c87909d9eb3a4d717e0c40289353da0267a51f60
ms.contentlocale: is-is
ms.lasthandoff: 03/26/2018

---

# <a name="configure-expense-management"></a>Skilgreina kostnaðarstýringu

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því sem þarf að hafa í huga og ákvörðunum sem þarf að taka í áætlunarferli áður en hægt er að skilgreina kostnaðarstýringu í Microsoft Dynamics 365 for Finance and Operations. Í kostnaðarstýringu, er hægt að geyma upplýsingar um greiðslumáta, ferðabeiðnir, kostnaðarskýrslur og stefnur og svo framvegis.

Þar sem margar þeirra ákvarðana sem gerðar eru við að áætla samskipan fyrir kostnaðarstýringu byggjast á stigveldi og fjárhagslegu skipulagi fyrirtækisins, verður að vísa til skipulagningarskjala fyrir þau svæði.

## <a name="intercompany-expenses"></a>Kostnaður innan samstæðu

Þegar kostnaður innan samstæðu er virkjaður, er lögaðilum og starfsmönnum leyft að stofna til kostnaðar fyrir hönd annars lögaðila og innheimta greiðslur frá lögaðila innan fyrirtækisins. Til dæmis lýkur starfsmaður í lögaðila A verkefni fyrir lögaðila B og verkefnið felur í sér ferðatengdan kostnað. Ef kostnaður innan samstæðu er virkjaður getur starfsmaðurinn svo skráð kostnaðarskýrslu sem mun bóka kostnaðinn á lögaðila B, og lögaðili A verður að greiða útgjöldin. Ef fyrirtækið hefur ekki marga lögaðila þarf ekki að virkja kostnað innan samstæðu.

**Ákvörðun:** Á að virkja kostnað innan samstæðu?

## <a name="financial-management"></a>Fjármálastjórnun

Kostnaðarstýring er samþætt náið með fjárhagslegar umsjón fyrirtækis þíns. Mikið af stillingum fyrir kostnaðarstýringu munu byggjast á ákvörðunum sem teknar voru um fjármál fyrirtækisins. Eftirfarandi kaflar lýsa ýmislegum svæðum sem krefjast áætlanagerðar og ákvarðana samkvæmt fjárhagslegum ákvörðunum og leiðbeiningum frá leiðtogateymi fyrirtækisins.

### <a name="per-diems"></a>Dagpeningar

Skilgreina verður dagpeningana sem fyrirtækið veitir starfsmanninum. Þar sem dagpeningar eru vanalega notaðir til að ná yfir útgjöld, eins og fæði, leiguhúsnæði og annan tilfallandi kostnað, er hægt að stofna reglur fyrir dagpeningaheimildir sem fyrirtækið býður. dagpeningataxti getur byggt á árstíma, ferðastað eða hvoru tveggja. Þegar dagpeningaregla er skilgreind er hægt að tilgreina að prósenta af dagpeningataxta verði haldið eftir ef starfsmaður fær ókeypis fæði eða þjónustu. Einnig er hægt að skilgreina lög af dagpeningataxta til að setja lágmarks- og hámarksfjölda klukkustunda sem hægt er að beita á ferðalög starfsmanns.

**Ákvarðanir:**

- Sjálfgefnar reglur fyrir dagpeninga fyrir fyrsta og síðasta daga:

    - Hver er lágmarksfjöldi stunda sem starfsmaður getur krafist á dag og fengið dagpeningar fyrir?
    - Er lækkun á þeirri upphæð sem er í boði fyrir máltíðir fyrir fyrsta dag og síðasta dag? Ef lækkun er til staðar hversu hátt er hlutfall lækkunarinnar?
    - Er lækkun á þeirri upphæð sem er í boði fyrir hótel fyrir fyrsta dag og síðasta dag? Ef lækkun er til staðar hversu hátt er hlutfall lækkunarinnar?
    - Er lækkun á þeirri upphæð sem er í boði fyrir annan kostnað sem hlýst á fyrsta og síðasta degi? Ef lækkun er til staðar hversu hátt er hlutfall lækkunarinnar?

- Sjálfgefnar reglur fyrir dagpeninga:

    - Er prósentulækkun á dagpeningaheimild fyrir hverja máltíð, ef máltíðin er t.d. ókeypis? Ef lækkun er til staðar hversu há er prósenta lækkunar fyrir hverja máltíð?
    - Er lækkun fæðispeninga reiknuð á dag, hverja ferð eða fjölda máltíða á dag?
    - Eiga dagpeningaupphæðir að vera sléttaðar á venjulegan hátt eða sléttaðar upp?
    - Eru dagpeningar reiknaðir á grundvelli 24 klst. tímabils eða almanaksdags?

- Reglur um dagpeninga samkvæmt staðsetningu:

    - Eru dagpeningar breytilegir eftir staðsetningu? Hvaða staðsetningar eru innifaldar?
    - Ef munur er dagpeningum eftir staðsetningu, fyrir hverja staðsetningu, hvaða prósentutala er veitt fyrir eftirfarandi kostnað:

        - Fæði
        - Hótel
        - Annar kostnaður

### <a name="expense-management-journals-and-accounts"></a>Útgjaldastýringarbækur og -lyklar

Útgjaldastýring krefst þess að notaðar séu margar færslubækur og lyklar. Það verður til dæmis að ákveða hvort sami lykillinn er notaður fyrir fyrirframgreiðslur og ágreining kreditkorts.

**Ákvarðanir:**

- Hvaða færslubók á að bóka samþykktar útgjaldaskýrslur í?
- Hvaða lykill er notaður fyrir fyrirframgreiðslur?
- Á að bóka fyrirframgreiðslur strax?

### <a name="payment-methods"></a>Greiðslumátar

Þegar starfsmönnum er leyft að stofna til kostnaðar fyrir hönd fyrirtækisins, verður að skilgreina greiðslumáta sem starfsmönnum er heimilt að nota. Til dæmis væri hægt að leyfa starfsmönnum að nota reiðufé eða kreditkort fyrirtækisins. Einnig væri hægt að leyfa starfsmönnum að nota persónuleg kreditkort og endurgreiða þeim síðan. Gera verður eftirfarandi ákvarðanir fyrir hvern greiðslumáta sem á að leyfa.

**Ákvarðanir:**

- Hvaða greiðslumátar eru heimilaðir?
- Hver á útgjöld greiðslumátans?
- Er gerð mótlykils til staðar? Ef mótlykilsgerð er til staðar, hver er hún?
- Ef mótlykill er til staðar, hver er lykillinn?
- Ef greiðslumátinn er kreditkort, á einungis að nota greiðslumátann með innfluttum kreditkortafærslum?

### <a name="expense-categories-and-shared-categories"></a>Útgjaldaflokkar og samnýttir flokkar

Þegar starfsmenn stofna kostnaðarskýrslu, verða hver útgjöld sem þeir skrá að vera tengd við útgjaldaflokk. Kostnaðartegundir eru afleiddar af samnýttum flokkum sem hægt er að deila með lögaðilum innan fyrirtækisins. Einnig er hægt að samnýta þessar tegundir í verkstjórnun og bókhaldi, allt eftir því hvernig fyrirtækið er skilgreint. Samkvæmt grunni skilgreiningar fyrirtækisins og leiðbeiningum frá framkvæmdahópnum þarf að ákvarða hvort aðeins skuli nota flokkana sem eru notaðir í Útgjaldastýringu á Útgjaldastýringu eða hvort samnýta eigi þá milli Verkefnastjórnunar og bókhalds og Útgjaldastýringu. Athugaðu að þessar tegundir er hægt að samnýta milli Verks og Kostnaðar eða Verks og Framleiðslu, en ekki á milli Kostnaðar og Framleiðslu. Taka verður eftirfarandi ákvarðanir fyrir hverja kostnaðartegund.

**Ákvarðanir:**

- Hver er kostnaðarflokkurinn? Dæmi eru flokkar fyrir flug, hótel eða vegalengd.
- Er einnig hægt að nota kostnaðartegundina í Verkefnastjórnun og bókhaldi?
- Hver er kostnaðartegundin?
- Hver er sjálfgefinn greiðslumáti fyrir kostnaðartegunda?
- Þarf að skilgreina kostnað í kostnaðarflokknum?
- Hver er sjálfgefinn lykill fyrir kostnaðartegundina?
- Hver er sjálfgefinn VSK-flokkur vöru fyrir kostnaðartegunda?
- Eru viðbótar greiðslumátar leyfðir fyrir kostnaðartegunda? Ef viðbótargreiðslumátar eru heimilaðir, hverjir eru þeir?
- Eru undirtegundir í þessari kostnaðartegund? Ef undirflokkar eru til staðar þarf einnig að taka eftirfarandi ákvarðanir:

    - Er einhverjum undirtegundum sleppt úr skattendurgreiðslum?
    - Hver er VSK-flokkur vöru fyrir undirtegundirnar?

Ef kostnaðartegundin er einnig notuð í verkstjórnun og bókhaldi, þarf að svara eftirstandandi spurningum. Annars skaltu færa þig yfir í næsta kafla.

- Hvaða kostnaðarlyklar verða notaðir fyrir eftirfarandi kkostnað?

    - Kostnaður
    - Launaskipting
    - VÍV - Kostnaðarverðmæti
    - Kostnaður - Vara
    - VÍV - Kostnaðarvirði - Vara
    - Uppsafnað tap
    - VÍV - Uppsafnað tap

- Hvaða tekjulyklar verða notaðir fyrir eftirfarandi?

    - Reikningsfærðar tekjur
    - Áfallnar tekjur - Söluverðmæti
    - VÍV - söluvirði
    - Áfallnar tekjur - Framleiðsla
    - VÍV - Framleiðsla
    - Áfallnar tekjur - Hagnaður
    - VÍV - Hagnaður
    - Áfallnar tekjur - Áskrift
    - VÍV - Áskrift

### <a name="taxes"></a>Skattar

Fyrir kostnað sem tengist sköttum verður að ákvarða hvað er tekið með eða virkjað í kostnaðarskýrslum.

**Ákvarðanir:**

- Er virðisaukaskattur innifalinn í upphæð kostnaðar?
- Á að virkja skattendurgreiðslur í útgjöldum?

    > [!NOTE]
    > Ef þú hefur við áætlun í fjárhag ákveðið að nota bandarískan virðisaukaskatt og reglur neysluskatts er ekki hægt að virkja skattendurgreiðslu á útgjöldum. (Til að nota bandarískar söluskatts- og neysluskattareglur skal stilla **Nota skattareglur virðisaukaskatts** valkostinn á **Já**.)

## <a name="policies"></a>Reglur

Með því að stofna kostnaðarskýrslureglur getur fyrirtækið sparað peninga og tíma þegar starfsmenn stofna til útgjalda fyrir hönd þess. Reglur hjálpa til við að tryggja að starfsmenn séu innan fjárhagsáætlunar, veiti allar nauðsynlegar upplýsingar og eyði aðeins fé eftir þörfum. Taka verður eftirfarandi ákvarðanir fyrir hverja kostnaðarreglu og hverja samþykktarreglu kostnaðarskýrslu sem þú stofnar.

**Ákvarðanir:**

- Hvert er heiti reglunnar?
- Til hvers er kostnaðarreglan?
- Ef þú ákvaðst áður að virkja kostnað innan samstæðu, fyrir hvaða fyrirtæki í samstæðunni á þessi regla við?
- Hvenær verður reglan virk?
- Hvenær verður úreldist reglan?
- Hvað er stefnuregla?
- Hver er útkoma stefnureglunnar?

