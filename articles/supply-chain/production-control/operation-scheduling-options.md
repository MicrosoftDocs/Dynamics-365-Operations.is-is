---
title: Kostir aðgerðaröðunar
description: Þetta efnisatriði lýsir valkostum í aðgerðaröðun. Hægt er að nota aðgerðaröðun til að fá almennt mat á framleiðsluferli yfir tíma.
author: ChristianRytt
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 198123
ms.assetid: d680d7be-da64-4132-89fe-ad2fa59afb77
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 32d15a4c2f2ec550d4a0b5436add2963b5636acf8f2b8ba8231ceeab16bb0929
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776315"
---
# <a name="operations-scheduling-options"></a>Kostir aðgerðaröðunar

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir valkostum í aðgerðaröðun. Hægt er að nota aðgerðaröðun til að fá almennt mat á framleiðsluferli yfir tíma.

Aðgerðaröðun reiknar eftirfarandi upplýsingar fyrir framleiðslupöntun:

-   Upphafs-og lokadagsetningar eru valdar fyrir framleiðslupöntunar og hverja aðgerð.
-   Tilföng eru úthlutuð á aðgerðir.

Margar stillingar ákvarða hvernig framleiðsluáætlun eru reiknaðir. Þú skilgreina stillingarnar á **Aðgerðaröðun** síðuna. Eftirfarandi upplýsingar lýsa röðunarvalkostum.

## <a name="operations-scheduling"></a>Aðgerðröðun
### <a name="scheduling-direction"></a>Stefna röðunar

Röðunarstefnan er grunnþáttur röðunarferlisins. Hægt er að raða framleiðslu fram eða aftur í tíma frá hvaða dagsetningu sem er, eftir tíma og áætlunarþörfum.

-   **Röðun áfram**– þú getur raðað framleiðslu til að byrja eins fljótt og möguleg er. Framleiðslan getur hafist í dag, á morgun eða á hvaða síðari dagsetningu sem er. áætlað er að framleiðslan hefjist á fyrstu mögulegu dagsetningu og er áætluð fram í tímann á fyrstu mögulegu lokadagsetningu.
-   **Röðun afturábak** – þú getur raðað framleiðslu til að byrja eins seint og möguleg er. Áætlunin byggist á dagsetningunni sem ljúka á framleiðslunni og telur afturábak að síðustu mögulegu dagsetningu sem hefja má framleiðsluna án þess að rjúfa skilafrestinn.

Eftirtaldir valkostir eru í boði:

-   **Áfram frá í dag** - Raðað áfram frá núgildandi dagsetningu. (Núgildandi dagsetning er kerfisdagsetning.)
-   **Áfram frá áætluðu upphafi** - Raða áfram frá fyrri upphafsdagsetningu. Ef engin röðun hefur verið framkvæmd áður er áætlunin röðuð frá deginum í dag.
-   **Áfram frá röðunardagsetningu** – Raðað áfram frá þeirri dagsetningu sem tilgreind er á **Röðunardagsetningu** svæði. Ef enginn röðunardagsetning er tilgreind er áætlunin röðuð frá deginum í dag.
-   **Aftur frá afhendingardegi** – Raðað afturábak frá afhendingardegi sem tilgreindur er fyrir framleiðslupöntun. Ef þetta er valið og engin afhendingardagsetning tilgreind verður afhendingardagsetning sett á gildandi dagsetningu.
-   **Aftur frá áætluðum lokum** – Raðað aftur frá áðurreiknaðri lokadagsetningu. Ef engin röðun hefur verið framkvæmd áður er lokadagsetningin gildandi dagsetning.
-   **Áftur frá röðunardagsetningu** – Raðað aftur frá þeirri dagsetningu sem tilgreind er á **Röðunardagsetningu** svæði. Ef ekki er valin röðunardagsetning er gildandi dagsetning notuð. Aftur frá röðunardagsetningu er reiknað fyrir framleiðslupöntun síðast þegar þarfir voru reiknaðar. Ef engin dagsetning er tilgreind fyrir framleiðslupöntunina er núverandi dagsetning kerfis notuð.
-   **Aftur frá komandi degi** - Áætlað aftur frá komandi degi reiknuðum fyrir framleiðslupöntun síðast þegar þarfir voru reiknaðar. Ef engin komandi dagsetning er tilgreind fyrir framleiðslupöntunina er núverandi dagsetning kerfis notuð.
-   **Raða eins og síðast** - Við aðgerðaröðun og vinnsluröðun eru valdar röðunarstefnur og röðunardagsetningar vistaðar. Hægt er velja þennan kost fyrir næstu röðun. Ef engin fyrri röðun er til fyrir framleiðslupöntunina er röðunin afturvirk frá núverandi dagsetningu (kerfis).
-   **Áfram frá morgundegi** - Raðað frá núgildandi degi að einum degi viðbættum.
-   **Aftur frá fyrri vinnslu** - Þessi aðgerð skiptir eingöngu máli við vinnsluröðun. Ef þessi röðunarstefna er valin fyrir aðgerðaröðun verður framleiðslupöntun raðað áfram frá núgildandi dagsetningu. Aðeins einni vinnslu er raðað í vinnsluröðun og öllum öðrum vinnslum framleiðslunnar er raðað samkvæmt henni.
-   **Aftur frá fyrri vinnslu** - Þessi aðgerð skiptir eingöngu máli við vinnsluröðun. Ef þessi röðunarstefna er valin fyrir aðgerðaröðun verður pöntunartillögu raðað afturábak frá núgildandi dagsetningu. Aðeins einni vinnslu er raðað í vinnsluröðun og öllum öðrum vinnslum framleiðslunnar er raðað samkvæmt henni.

### <a name="scheduling-date"></a>Röðunardagsetning

Dagsetning notuð fyrir **Áfram frá röðunardagsetningu** og **Aftur frá röðunardagsetningu** röðunarstefnur. Röðun er þá framkvæmd aftur eða fram í tíma frá þessari dagsetningu. Sjá fyrri hluta, „Röðunarstefna“, fyrir frekari upplýsingar,

### <a name="recalculate-bom-levels"></a>Endurreikna uppskriftarstig

Þegar valið er **Endurreikna uppskriftarstig**, eru völdu uppskriftastig (BOM) endurreiknuð til að aðstoða við að tryggja réttri röð.

## <a name="limitations"></a>Takmarkanir
### <a name="finite-capacity"></a>Takmörkuð geta

Röðun er háð því að tilföng sem eru nauðsynlegar til að ljúka framleiðslu séu tiltækar. Ef afkastageta er ekki nægileg er hægt að fresta framleiðslunni eða jafnvel stöðva hana. ef takmörkuð afkastageta er notuð fyrir aðgerðarröðun eru fyrirliggjandi frátekningar á afkastagetu sem gerðar eru á forða teknar með og sú afkastageta er séð sem ótiltæk. framleiðslupöntun er áætluð út frá því að tilföng sem eru nauðsynlegar séu tiltækar. Aðgerðaröðun notar tilgreinda röð aðgerða til að ákvarða röð aðgerða í framleiðsluleiðinni. Aðgerðaröðun tekur frá afköst í tilfangaflokka, samkvæmt aðgerðatímar sem eru skilgreindar í framleiðsluleið. Afkastageta tilfangaflokka er summa tiltækrar afkastagetu í öllum tilföngum í tilfangaflokkum.

### <a name="finite-material"></a>Endanlegt magn

Röðun er einnig háð því efni sem er tiltækt fyrir framleiðslu. Ónógar íhlut framboð getur líka valdið seinkanir framleiðslu. Röðun getur einnig byggt á efnisnotkun. Einungis tilgreina efni sem verður að vera tiltækt fyrir framleiðslu í staðinn fyrir efni sem ekki eru mikilvæg. Þessi gerð röðunar kallast raða með takmörkuðu efni. Þegar tilgreina takmarkað efni er framleiðslu raðað samkvæmt hvort efni sé tiltækt. **Athugið:** Þegar bæði afkastageta og efni er fínstillt er framleiðslan reiknuð til að hún uppfylli bæði skilyrðin. Bæði tiltækileiki afkastageta og efni er íhugað og framleiðslupöntun rekstur er ekki hægt að tímasetja að hefjast þar til afkastageta og efni eru tiltæk á sama tíma og í því magni sem þarf. Veljið þennan gátreit til að miða eigi við að hráefni sé takmarkað þegar raðað er. Ef hráefni er takmarkað verður tekið tillit til umfangs efnis á þeim tíma. Með öðrum orðum tekur röðun tillit til komandi dagsetninga sem eru reiknaðar fyrir vörurnar. Röðun frátekur hráefni og brýtur niður núgildandi framleiðslu. Ef raðað er í nokkur skipti er það einungis fyrsta röðunin sem brýtur niður og tekur frá. Ef gerðar eru breytingar í framleiðsluuppskrift eða leið keyrir næsta röðun niðurbrot. Fyrir niðurbrot er gert ráð fyrir að þörf sé á efni samdægurs. Þar sem framleiðslu er ekki raðað á sama tíma og niðurbrot aðalröðunar er núgildandi dagsetning notuð sem besta mat um hvenær vörur verða til reiðu. Niðurbrotið athugar þá hvenær vörurnar verða tiltækar. Ef vörurnar eru tiltækar, er mögulegt að mæta framleiðsluþörfinni. Ef vörurnar eru ekki tiltækar á núgildandi dagsetningu er tillaga mynduð og mótfærsla valið fyrir tillögu. Ef sjálfvirk staðfesting er sett upp fyrir pöntunartillögu er hún staðfest sjálfkrafa fyrir innkaup eða framleiðslu. Framleiðslustaðan breytist sjálfkrafa í þá stöðu sem tilgreind er í svæðinu **Umbeðin framleiðslustaða** í reitnum í **Þekjuflokkar** svarglugga. Ef gátreitur er auður er gengið út frá því að efni sé til. Röðun tekur því ekki tillit til þess hvort efni sé tiltækt á þeim tíma sem þörf er.

### <a name="finite-property"></a>Takmarkaður eiginleiki

Veljið þennan gátreit ef vinnsluröðun á að taka mið af eignaþörfum.

### <a name="keep-production-unit"></a>Halda framleiðslueiningu

Velja hvort skuli röðunarvélin raða aðeins tilföng sem þegar eru tilgreindar á framleiðslueiningunni.

### <a name="keep-warehouse-from-resource"></a>Halda vöruhúsi úr tilföngum

Veljið hvort röðunarvélin ætti að áætla aðeins tilföng sem eru tengdar við ílagsvöruhús sem tilgreindur er í tilföngunum.

## <a name="references"></a>Tilvísanir
### <a name="schedule-references"></a>Raða tilvísunum

Þegar tilvísanir háðir framleiðslupantanir, þeir eru einnig þekkt sem undirframleiðslu. Hægt er að raða undirframleiðslur sem hluti af röðun á framleiðslupöntun. Veljið þennan gátreit ef eigi að byggja röðun undirframleiðslu á röðun á aðalframleiðslunni. Í tengslum við aðal framleiðslu er yfirliggjandi framleiðslum raðað áfram og undirliggjandi raðað afturábak. Hægt er að skoða tilvísun fyrir framleiðslupöntun í **tilvísunarstig** reit á síðunni **Framleiðslupöntun**.

### <a name="synchronize-references"></a>Stilla tilvísanir saman

Einnig er hægt að samstilla tilvísanir við framleiðslupöntun. Ef þessi valkostur er valinn eru dagsetningar undirframleiðslunnar fluttar og stilltar þegar röðun framleiðslupöntunar er breytt. Ef framleiðslupöntunin hefur eina eða fleiri undirframleiðslur, gætir þú ef vill viljað áætla undirframleiðslur með aðalframleiðslunni. Í þessu tilfelli ekki er hægt að ræsa aðalframleiðslu fyrr en tengdum undirframleiðslum er lokið. Af þeim sökum Veljið þennan gátreit ef eigi að byggja röðun undirframleiðslu á upphafs- og lokatíma á valinni framleiðslu. Einungis er hægt að velja þennan gátreit ef reiturinn **raða tilvísunum** er einnig valinn.

## <a name="cancellation"></a>Afturköllun
### <a name="cancel-queue-time"></a>Rjúfa biðtíma

Veljið þennan gátreit til að sleppa biðtíma í áætlunargerð.

### <a name="cancel-setup"></a>Rjúfa uppsetningu

Veljið þennan gátreit til að sleppa uppsetningartíma í áætlunargerð.

### <a name="cancel-process"></a>Rjúfa vinnslu

Veljið þennan gátreit til að sleppa keyrslutíma í áætlunargerð.

### <a name="cancel-overlap"></a>Rjúfa skörun

Veljið þennan gátreit til að sleppa tíma sem skarast í áætlunargerð.

### <a name="cancel-transport"></a>Rjúfa flutning

Veljið þennan gátreit til að sleppa flutningstíma í áætlunargerð.

## <a name="set-default"></a>Setja sjálfgildi
Hægt að vista gildandi gildi sem sjálfgildi. Tveir kostir eru í boði:

-   Nota sem sjálfgefið fyrir mig
-   Nota sem sjálfgefið fyrir alla


## <a name="additional-resources"></a>Frekari upplýsingar

[Aðgerðaröðun](operations-scheduling.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]