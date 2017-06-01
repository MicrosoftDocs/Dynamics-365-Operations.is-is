---
title: "Uppfæra fjárhagsáætlunargerð"
description: "Það er verulegur mismunur á fjárhagsáætlunargerð milli Microsoft Dynamics AX 2012 og Microsoft Dynamics 365 for Operations. Sumir eiginleika voru ekki uppfærðir og þurfa þess vegna að vera stilltir aftur. Í þessu efnisatriði er útskýrt hvað verður að vera endurstillt og er einnig lýst nýjum aðgerðum sem ætti að líta á eftir að uppfærslu er lokið."
author: twheeloc
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 272923
ms.assetid: 17cdfe74-bdfd-466a-9bdd-c12583f250c7
ms.search.region: Global
ms.author: ryansand
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: fafa323c3949c09707c81ec41edae25ad2677eeb
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="upgrade-budget-planning"></a>Uppfæra fjárhagsáætlunargerð

[!include[banner](../includes/banner.md)]


Það er verulegur mismunur á fjárhagsáætlunargerð milli Microsoft Dynamics AX 2012 og Microsoft Dynamics 365 for Operations. Sumir eiginleika voru ekki uppfærðir og þurfa þess vegna að vera stilltir aftur. Í þessu efnisatriði er útskýrt hvað verður að vera endurstillt og er einnig lýst nýjum aðgerðum sem ætti að líta á eftir að uppfærslu er lokið.  

Fjárhagsáætlunargerð í Microsoft Dynamics 365 for Operations hefur margar endurbætur sem ekki voru tiltækar í Microsoft Dynamics AX 2012. Í þessu efnisatriði er fjallað um breytingar sem viðskiptavinir sem uppfæra þurfa að velja. Það kemur einnig inn á nýja eiginleika sem ætti að líta á í uppfærsluferlinu. Vegna umfangi breytinganna, verður ekki hægt að opna fyrirliggjandi fjárhagsáætlun fyrr en breytingunum sem lýst er í þessu efnisatriði eru gerðar. Hins vegar ættu skýrslur að halda áfram að virka og ekki er þörf á frekari breytingum.

## <a name="overview-of-changes"></a>Yfirlit yfir breytingar
Margar verulegar breytingar hafa verið gerðar í Fjárhagsáætlun fyrir Dynamics 365 for Operations. Þessum breytingum er ætlað að gera fjárhagsáætlunargerð aðveldari til að skilgreina og endurnýtanlegri, til að minnka árlegt viðhald og uppsetningu. Eftirfarandi svæði í AX 2012 eru ekki lengur til staðar í Dynamics 365 for Operations:

-   Sniðmát fjárhagsáætlunar (Skilgreining fjárhagsáætlunargerðar)
-   Möppur fjárhagsáætlunar (Skilgreining fjárhagsáætlunargerðar)
-   Skorðun á aðstæðum (Skilgreining fjárhagsáætlunargerðar)
-   Sniðmát fyrir stigsreglur fjárhagsáætlunargerðar og sniðmát (Ferli fjárhagsáætlunargerðar)
-   Fylkjasvæði fyrir vinnublaðssniðmát
-   Leiðsagnarforrit fyrir Microsoft Office Excel-fjárhagsáætlun

Ekki er hægt að uppfæra nokkur ný hugtök úr fyrri virkni. Þess vegna þarf að ljúka sumum endurstillingum vegna þessara nýju hugtaka. Eftirfarandi kaflar lýsa til hugtökunum sem hefur verið skipt út fyrir atriði í fyrri lista.

### <a name="columns"></a>Dálkar

Dálkar eru nýtt hugtak sem kemur í stað hluta af Excel-sniðmáti og einnig fylkissvæðum. Dálkar geta staðið fyrir tímabil mánuð, ársfjórðung, ár eða allan tíma. Tímatilvísun er gagnvirk. Hún vísar í hlutfallslegt tímabil eða ár í tengslum við fjárhagsáætlunarferlið. Til dæmis vísar dálkurinn **Fyrra ár Janúar** í fjárhagstímabil 1 fyrir ár -1. Dálkur eru sértækur fyrir aðstæður fjárhagsáætlunargerðar, svo sem rauntölur eða beiðni um fjárhagsáætlun.

### <a name="layouts"></a>Útlit

Útlit eru nýtt hugtak sem koma í stað Excel-sniðmáts. Útlit innihalda dálka sem skilgreina hvaða áætlun eða raungögn og tímabil skuli birta. Útlit eru einnig samnýtt á milli biðlarans og Excel-innbótarinnar. Þar af leiðandi er upplifuninin þegar gögn eru færð inn eða skoðuð í Dynamics 365 for Operations biðlara betri en í AX 2012. Til að færa inn gögn í Dynamics 365 for Operations biðlara er ekki eingöngu takmarkað við að skoða og færa inn eitt dæmi í færsluskjá. Þess í stað gerir samanburðarskjár það mögulegt að skoða og slá inn upphæðir fyrir fjölda tímabila og lykla á sama tíma. Einnig er hægt að skilgreina útlit þannig að hægt er að færa inn og skoða gjaldmiðil, athugasemdir og önnur valfrjáls gögn. Útlit gera þér einnig kleift að skilgreina hvaða fjárhagsvíddir og lýsingarvíddir skuli birta. Útlit innihalda einnig skorður til að tilgreina hvaða dálka í sniðmáti er hægt að breyta og hvaða dálkar eigi að vera tiltækir í Excel. Þegar búið er að skilgreina útlit er sniðmát búið til fyrir það. Þessi sniðmát stofnar samsvarandi Excel sniðmátið. Síðan er hægt að breyta Excel sniðmátinu sem á að innihalda fleiri formúlur og snið og senda það aftur. Útlitum er svo úthlutað á hverja stigsreglu á síðunni **Ferli fjárhagsáætlunargerðar**. Þess vegna eru útlitum skipt út fyrir sniðmát, sem var úthlutað og notuð svipaðan hátt.

### <a name="budget-planning-processes"></a>Ferli fjárhagsáætlunargerðar

Ferli fjárhagsáætlunargerðar eru að mestu hin sömu og AX 2012. Helsta verulega breytingin er að sniðmátum er skipt út fyrir útlit. Ef einhverjar vinnslur voru áður fylltar inn í AX 2012 eru vinnslur uppfærðar í framvindustöðu þannig að hægt er að gera breytingar. Úthluta verður útlit fyrir hvert stig reglu til að ákvarða hvaða aðstæður og tímabil birtast þegar áætlunin er opnuð á biðlara. Útlit ákvarða einnig hvaða Excel-sniðmát er opnað utan Dynamics 365 for Operations svo hægt sé að skoða fjárhagsáætlunina. **Sjálfgefið lykilskipulag** er nýtt nauðsynleg svæði fyrir Ferli fjárhagsáætlunargerðar. Fyrir hvert ferli fjárhagsáætlunargerðar skal úthluta aðallyklaskipulagi sem á að nota fyrir fjárhagsáætlun.

### <a name="attachments"></a>Viðhengi

Í AX 2012 voru réttlætingarskjöl vistuð í viðhengjamöppu. Engin fyrri réttlætingarskjöl eru uppfærð. Réttlætingarskjöl verða geymd í gagnagrunninum. Ef vista á þessar upplýsingar í uppfærðu útgáfunni, er hægt að hlaða upp síðustu réttlætingarskjölum fyrir hverja áætlun sem viðhengi með því að nota í **Jöfnun** hnappinn í Aðgerðarúðunni. Í AX 2012 voru Excel vinnublöð fyrir hverja fjárhagsáætlun stofnuð á grundvelli sniðmáts. Í Dynamics 365 for Operations opna allar áætlanir afrit útlitsins. Hins vegar eru engar breytingar Excel skrána vistaðar. Allar formúlur eða stuðningsupplýsingar sem voru notaðir í áætlun á ári verður bætt í athugasemd, jöfnunarskjal eða eitthvað annað aukaferli.

## <a name="configuring-an-upgraded-environment-from-ax-2012"></a>Skilgreining uppfærðs umhverfi úr AX 2012
Til að hjálpa til við að ákvarða hvernig stilla á uppfærða kerfið nota eftirfarandi dæmi uppfærða fjárhagsáætlunarferli úr sýnigögnum AX 2012. Sjálfgefin skilgreiningargögn fyrir dálka sem stofnaðuð til að aðstoða við uppfærsluferlið. Hægt er að uppfæra eða eyða sjálfgefnu gögnunum ef þau uppfylla ekki skilgreiningarkröfur. **Athugið:** Ný áskilin svæði eru til staðar sem ekki verða stillt í kerfinu. Ef þú festist á síðu, líkt og **Skilgreining fjárhagsáætlunargerðar** og kemst ekki af henni geturðu lokað vafranum og svo opnað hann aftur á annarri síðu ti lað slá inn upplýsingar í réttri röð. Það eru nauðsynleg svæði sem ekki eru stillt. Þar af leiðandi kunna vandamál að koma upp þar til allt hefur verið stillt og öll skyldusvæði valin. Þetta efnisatriði útskýrir hvernig stilla á þessi svæði eins og nauðsynlegt er. Hér eru nokkur dæmi um þessi svæði:

-   **Ferli fjárhagsáætlunargerðar** síðan: **Sjálfgefin lykilskipulagi** svæði
-   **Ferli fjárhagsáætlunargerðar** síðan: **Útlit** reiturinn á flýtiflipa **Reglur og útlit fjárhagsáætlunargerðar**

### <a name="define-columns-and-layouts"></a>Skilgreina dálka og útlit

1.  Á síðunni **Skilgreining fjárhagsáætlunargerðar** er smellt á flipann **Dálkar**. Við uppfærslu eru nýir dálkar stofnaðar sjálfkrafa á grundvelli fjárhagsætlunarlína. Dálkar nota nú kvikar dagsetningar þar sem tími og ár eru jöfnuðu úr fjárhagsárinu sem er skilgreint Ferli fjárhagsáætlunargerðar. **Athugið:** Til að skila betri afköstum meðan á uppfærslu stendur er gert ráð fyrir því öll ferli fjárhagsáætlunar tákni almanaksár, ekki fjárhagsáætlun. Ef reikningsár eru notuð verður að gera breytingar til að varpa dálkum rétt á það fjárhagsár. Til dæmis voru eftirfarandi einingar til í AX 2012:
    -   Aðstæður fjárhagsáætlunargerðar: Rauntölur, Grunnlína, Beiðni um fjárhagsáætlun, Samþykkt fjárhagsáætlunar
    -   Fjárhagsáætlunarlínur fyrir allar aðstæður í 2017 og Rauntölur fyrir bæði 2017 og 2016

    Eftirfarandi dálkar verða stofnaðir í Dynamics 365 for Operations:
    | Dálkheiti    | Aðstæður fjárhagsáætlunargerðar | Tímabil dálka | Mótbókun árs |
    |----------------|----------------------|--------------------|-------------|
    | Janúaraðstæður 1 | Rauntölur              | 1                  | 0           |
    | Janúaraðstæður 2 | Grunnlína             | 1                  | 0           |
    | Janúaraðstæður 3 | Beiðni um fjárhagsáætlun       | 1                  | 0           |
    | Janúaraðstæður 4 | Samþykkt fjárhagsáætlun      | 1                  | 0           |
    | Janúaraðstæður 5 | Rauntölur              | 1                  | -1          |
    | Febrúaraðstæður 1 | Rauntölur              | 1                  | 0           |
    | ...            | ...                  | ...                | ...         |

    Í þessu dæmi er dálkur sem er nefndur **Jan dæmi 1** stofnaður fyrir nýjustu færslugögn fjárhagsáætlunar sem finnast þar sem færslan er til í janúar. Svipaður dálkur er stofnaður fyrir hverjar aðstæður með gögnum. Þegar dálkar eru til staðar fyrir öll tímabil á því ári eru dálkar stofnaðar fyrir fyrri ár.
2.  Breyta nöfnum dálka og lýsingum, og öðrum upplýsingum, annað hvort handvirkt í biðlara eða með því að gera fjöluppfærslu í gegnum Excel-innbót sem bendir á gagnaeiningu dálka fjárhagsáætlunar. Allar síurnar sem voru áður valdar fyrir fylkissvæði eru nú stilltar innan dálka.
3.  Stofna nýtt fjárhagsáætlunarútlit. Útlit vísar í nokkra dálka til þess að skilgreina skjá sem birtist í Excel og á biðlara. Útlit þarf fyrst að tilgreina fjárhagsvíddarsamstæðu til að ákvarða hvaða fjárhagsvíddir er hægt að færa inn. Þegar víddasamstæðan sem er tilgreint er smellt á **Lýsingar** til að velja lýsingarvídd sem taka á með í útlitinu.
4.  Á flýtiflipanum **Útlitseiningar** skal smella á **Bæta við** til að bæta lýsigögnum við hverja línu, eins og gjaldmiðil, athugasemd eða fjárhagsáætlunarklasa sem ákvarðar tekjur gegn útgjaldalínum. Næstu skaltu bæta við dálkum fyrir tímabilið og sviðsmyndum sem eiga við um þetta ferli fjárhagsáætlunar og stig. Gera má þessar breytingar handvirkt á biðlaranum eða í gegnum í Excel innbótinni sem vísar í gagnaeiningu fjárhagsáætlunarútlitseiningarinnar.
5.  Fyrir hverja útlitseiningu skal velja hvort dálkur skuli vera breytanlegur og hvort dálkurinn skuli einnig birtast í Excel-vinnubókinni fyrir útlitið. **Athugið:** Fyrir söguplan gætirðu haft áhuga á útliti sem sýna 12 mánaðardálka fyrir allar aðstæður fjárhagsáætlunargerðar fyrir það ferli.

### <a name="update-budget-planning-processes-to-use-the-appropriate-layout-for-each-budget-stage"></a>Uppfæra ferli fjárhagsáætlunargerðar til að nota viðeigandi útlit fyrir hvert áætlunarstig

1.  Á **Ferli fjárhagsáætlunargerðar** síðunni skal velja það ferli sem á að skilgreina.
2.  Í aðgerðasvæðinu er smellt á **Breyta**.
3.  Tilgreinið sjálfgefið lykilskipulag fyrir þetta fjárhagsáætlunarferli. **Sjálfgefin lykilskipulagi** er nýtt nauðsynlegt svæði sem þarf að stilla.
4.  Á flýtiflipanum **Reglur og útlit fjárhagsáætlunargerðar** á reitnum **Útlit** skaltu velja útlit sem var áður stillt og er viðeigandi fyrir þetta stig.
5.  Haldið áfram að velja sama eða annað útlit fyrir mismunandi fjárhagsáætlunargerð og vista svo breytingarnar.

## <a name="additional-features-to-consider-in-your-budgeting-process"></a>Aukaaðgerðum til að hugleiða í fjárhagsáætlunarferli
### <a name="budget-planning-workspace"></a>Vinnusvæði fjárhagsáætlunargerðar

Þetta vinnusvæði er hannað fyrir eigandi áætlunarinnar og þá sem koma að henni. Það hefur tengla á fjárhagsáætlunarskjöl sem krefjast athygli. Það hefur einnig skýrslur og afkastavísa fyrir fjárhagsáætlunarferlið. Kerfisstjóri getur skilgreint ferli fjárhagsáætlunargerðar fyrir alla notendur á síðunni **Færibreytur fyrir fjárhagsáætlun**. Á **Stillingar vinnusvæðis** flipanum á flýtiflipanum **Fjárhagsáætlunargerð** er svæði þar sem hægt er að velja ferli fjárhagsáætlunargerðar.

### <a name="alternate-layouts"></a>Önnur útlit

Annað útlit er ný aðgerð sem gerir það mögulegt að skoða áætlanir í mismunandi útliti. Hægt er að fá eitt eða fleiri útlit sem valkost. Síðan má skoða fjárhagsáætlun í mánaðarlegu eða ársfjórðungslegu útliti. Annað útlit er stillt á **Reglur og útlit fjárhagsáætlunargerðar** flýtiflipanum á síðunni **Ferli fjárhagsáætlunargerðar**.

### <a name="budget-milestones"></a>Áfangar fjárhagsáætlunar

Sem hluti af fjárhagsáætlunarferlinu, skiptir miklu máli að þú skiljir aðalþætti dagsetningar og tímamörk. Nú er hægt að skilgreina dagsetningar þannig að þær hafa lýsingar. Notendur fjárhagsáætlunar sjá þessa lýsingu þegar þeir opna áætlun til að breyta eða skoða eitthvað sem er tengt við þær.

### <a name="copy-from-budget-plan-allocation"></a>Afrita af fjárhagsáætlunarúthlutun

Ný úthlutunaraðferð gerir það mögulegt að dreifa frá yfiráætlun í undiráætlun án þess að fara í gegnum illisti í stigveldinu. Þessi aðferð er sérstaklega gagnleg fyrir viðskiptavini sem áður stofnuðu fjárhagsvídd fyrir dreifingu og samþykkt fjárhagsáætlunar.

### <a name="generating-budget-plans-from-new-budget-sources"></a>Búa til fjárhagsáætlun úr uppruna fjárhagsáætlunar

Eftirfarandi valkostum var bætt við sem reglubundnar vinnslur. Þessir valkostir gera notendum kleift að mynda fjárhagsáætlun með gögnum úr öðru kerfi sem upphafspunkt:

-   Mynda fjárhagsáætlun úr eftirspurnarspá
-   Mynda fjárhagsáætlun úr birgðaspá
-   Mynda fjárhagsáætlun úr verki
-   Mynda fjárhagsáætlun úr fjárhagsáætlunarskrá

### <a name="more-complete-tracking-of-amounts"></a>Betri rakning upphæða

Í AX 2012 hafði fjárhagsáætlunargerð eina áætlunarupphæð sem var vistuð fyrir hvert gildi. Í Dynamics 365 for Operations hefur gagnalíkanið verið útvíkkað. Nú er bókhaldsgjaldmiðill, færslugjaldmiðill og skýrslugjaldmiðilsupphæð fyrir hvert gildi. Á meðan á uppfærslu stendur eru þessir nýjum dálkar sjálfkrafa fyllt út.

### <a name="do-not-convert-currency-in-aggregation"></a>Ekki umreikna gjaldmiðil í uppsöfnun

Þegar undiráætlun er safnað upp í yfiráætlun eru upphæðir yfirleitt umreiknaðar sjálfkrafa úr færslugjaldmiðli í bókhaldsgjaldmiðil fyrir fyrirtækið. Þegar valkosturinn **Ekki umreikna gjaldmiðil í uppsöfnun** er stilltur á **Nei** er uppsöfnunarupphæðin áfram í upprunalega gjaldmiðlinum. Þar af leiðandi leyfir þessi valkostur nákvæmari leiðréttingar sem verða fyrir áhrifum af sveiflum gengi.

### <a name="looking-back-from-a-budget-plan-to-other-modules-that-contributed-to-the-budget"></a>Farið úr fjárhagsáætlun í aðrar einingar sem hafa áhrif á fjárhagsáætlunina

Fjárhagsáætlanir geta verið myndaðar frá eftirspurn eða birgðaspám, verkum og öðrum svæðum. Fyrirspurnin Fjárhagsáætlanir eftir víddasamstæðum inniheldur nokkra valkosti sem gera kleift að keyra fyrirspurn til að finna gögn sem voru uppruni fjárhagsáætlunar.

### <a name="overwrite-or-append-to-plan-for-allocation-schedules"></a>Skrifa yfir eða bæta við áætlun fyrir úthlutunaráætlanir

Ef margir upprunar eru fyrir upphæðir sem verður að dreifa er hægt að tilgreina að upphæðirnar skuli vera viðbótar. Í þessu tilfelli skrifa upphæðirnar ekki yfir fyrirliggjandi upphæðir. Í staðinn bætast þær við fyrirliggjandi upphæðir.

### <a name="default-financial-dimension-set-for-budget-planning-configuration"></a>Sjálfgefið fjárhagsvíddasamstæða fyrir skilgreiningu fjárhagsáætlunargerðar

Síðan **Skilgreining fjárhagsáætlunargerðar** inniheldur nú svæði þar sem hægt er að tilgreina sjálfgefnu fjárhagsvíddasamstæðuna. Þótt þetta svæði er valfrjálst svæði gæti þess verið krafist fyrir ákveðnar fyrirspurnir. Það getur líka verið nauðsynleg ef óskað er að flokka eða sía skýrslur eftir víddarsamstæðu.

### <a name="data-entities"></a>Gagnaeiningar

Nokkrum gagnaeiningum hefur verið bætt við til að virkja skjót innleiðingu fjárhagsáætlunargerðar. Eigindirnar gera það einnig kleift að gera margar breytingar í Excel. Þar af leiðandi þarf ekki að stofna vörur eina í einu með biðlara. Hér er listi yfir nýjar gagnaeiningar:

-   Einingarheiti
-   Færibreytur fjárhagsáætlunar
-   Færibreyta fjárhagsáætlunar
-   Aðstæður fjárhagsáætlunargerðar
-   Fjárhagsáætlunarstig
-   Verkflæðisstig fjárhagsáætlunar
-   Úthlutunaráætlanir fjárhagsáætlunar
-   Úthlutanir fjárhagsáætlunarstigs
-   Forgangur fjárhagsáætlunargerðar
-   Fjárhagsáætlunardálkar
-   Fjárhagsáætlunarútlitseiningar





