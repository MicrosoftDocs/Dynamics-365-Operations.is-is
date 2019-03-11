---
title: Operations-tilföng
description: Rekstrartilföng framkvæma verkþætti verks eða framleiðsluferlis. Þau geta verið af mismunandi gerðum og geta haft mismunandi getu.
author: sorenva
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifecycleManagementWorkspace, WrkCtrCapability
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e11d64ec37775f4fe2fc113af238a6294b459454
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "366605"
---
# <a name="operations-resources"></a>Operations-tilföng

[!include [banner](../includes/banner.md)]

Rekstrartilföng framkvæma verkþætti verks eða framleiðsluferlis. Þau geta verið af mismunandi gerðum og geta haft mismunandi getu. 

<a name="operations-resources"></a>Operations-tilföng
--------------------

Rekstrartilföng eru vélar, verkfæri, starfsmenn, aðstöðu, efnislegt svæði eða lánardrottnum sem framkvæma verkþætti verks eða framleiðsluferli. Þær geta verið af mismunandi gerðum og geta haft mismunandi getu.

-   **Lánardrottinn**  ytri tilfang sem framkvæmir verkþætti verks eða framleiðsluferli. Sem dæmi má nefna undirverktaki. Með því að tengja tilföng lánardrottins við lánardrottnalykil, er hægt að mynda innkaup fyrir undirverktaka, byggt á uppskriftarlínum eða framleiðslulínum.
-   **Mannauður** – starfsmanns verks eða framleiðslu sem að framkvæma verkþáttinn, annað hvort einir eða sem stjórnandi vélar eða tækis. Ef verið er að nota virknina mannauður er hægt að tengja mannauð við starfsmann. Röðunarvélin getur síðan úthluta tilföngum, byggt á hæfni sem eru skilgreindar fyrir samsvarandi starfsmanns.
-   **Vél** – vél eða öðrum framleiðslutækjum sem krafist er í framleiðslu.
-   **Verkfæri** – verkfæri eða tækið er yfirleitt notað með önnur tilföng til að framkvæma verkþátt í verki eða framleiðslu.
-   **Staðsetning** – efnisleg staðsetning ákveðinnar stærðar sem er krafist til að geta framkvæma aðgerð. Sem dæmi má nefna samsetningarsvæði.
-   **Aðstöðu** – bygging eða fast mannvirki sem er krafist til að framkvæma aðgerð.

## <a name="calendars"></a>Dagatöl
Dagatal er hægt að úthluta á rekstrartilföng og lýsir afkastagetu (í klukkustundum) á það tilfang. Vinnutímar rekstrartilfanga eru ákvarðaðar samkvæmt dagatalið sem er úthlutað á tilfangaflokk sem er rekstrartilföng eru hluti af. Hægt er að setja inn gildisdagsetninguog lokadag fyrir úthlutað dagatali. Síðan má tengja fleiri en eitt dagatal við rekstrartilföng. Hins vegar mega dagsetningar úthlutað dagatöl ekki skarast og rekstrartilföng geta fengið úthlutað aðeins eitt dagatal í einu. **Athugasemd** Ef engin gild verkdagatöl eru til staðar fyrir tilfangaflokkinn, til dæmis ef síðasta úthlutaða dagatalið eða eina dagatalinu sem var úthlutað er útrunnið, er ekki lengur hægt að fá aðgang að rekstrartilföngunum sem var úthlutað til tilfangaflokksins fyrir framleiðsluáætlunar og aðgerðaröðun. Einnig er hægt að úthluta dagatali á tilfangaflokkinn til að tilgreina vinnutíma fyrir bæði tilfangaflokkinn og allar rekstrartilföng sem er úthlutað á tilfangaflokkinn. Afkastageta tilfangaflokks er reiknaður sem samtala afkasta fyrir hverja rekstrartilföng sem er úthlutað á tilfangaflokk. Dagatal sem er úthlutað á tilfangaflokk getur breyst með tímanum.

## <a name="resource-capabilities"></a>Tilfangageta
Geta er hæfni rekstrartilfanga til að framkvæma tiltekinn verkþátt. Hægt er að úthluta einu eða fleiri getum á rekstrartilföng. Röðunarvél úthlutar síðan tilföng með því að láta tilfangaþörfum hverrar aðgerðar samsvara getu fyrir tiltækar rekstrartilföng. Hægt er að úthluta getu á öllum gerðum rekstrartilföngum (**Verkfæri**, **Lánardrottins**, **Vél**, **mannauður**, **Staðsetningu**, eða **Aðstöðu**). Til að úthluta getu á rekstrartilföngum í takmarkaðan tíma, skilgreina skal upphafs og lokadagsetning fyrir úthlutun getunnar. Nánari upplýsingar er að finna í [ tilfangageta](resource-capabilities.md).

## <a name="resource-groups"></a>Tilfangaflokkar
tilfangaflokk er safn rekstrartilfanga sem táknar uppskiptingu sem á að raða tilföngum eftir þegar aðferðin aðgerðaröðun er notuð. Þess vegna samsvara tilfangaflokk yfirleitt efnislegu skipulagi vinnuflokkana, sem eru afmarkaðar með gulum línur í vinnslusal framleiðslu. Tilfangaflokkurinn skilgreinir svæði, framleiðslueiningu og samhengi vöruhúss fyrir rekstrartilföngum sem er úthlutað á hópinn. Þegar þú úthlutar rekstrartilföng á tilfangaflokk, geta tilföngun verið röðuð á svæði þar sem tilfangaflokkurinn er staðsettur. Ekki þarf að úthluta rekstrartilföng sem eru stofnaðar á tilfangaflokk. Hins verður rekstrartilföng að vera úthluta á tilfangaflokk áður en hægt er að raða hana til að framkvæma vinnu. Hægt er að úthluta aðgerðatilfangi til tilfangaflokks í takmarkaðan tíma. Einnig er hægt að úthluta rekstrartilföng á marga tilfangaflokka þannig svo megi deila tilfang milli staða. Hins vegar mega gildisdagsetning- og lokadaga ekki skarast. Með öðrum orðu er Ekki hægt að úthluta rekstrartilföng til tveggja mismunandi tilfangaflokka á sama tíma. Breytingar á úthlutun tilfangaflokks eru virkar aðeins fyrir nýjar úthlutanir tilfanga. Frátekin afkastageta fyrir vinnslur, aðgerða og tímaspá verks sem er þegar raðað verða ekki fyrir áhrifum. **Ábending:** Þegar rekstrartilföngum gerðar **Lánardrottins** er úthlutað á tilfangaflokk, allar rekstrartilföngum sem er úthlutað á þann tilfangaflokk verða að verða af gerðinni **Lánardrottins** og vera tengd sama lánardrottnalykil.

## <a name="production-units"></a>Framleiðslueiningar
Framleiðslueining er stjórnunareining sem er safn forðaflokka. Framleiðslueining getur innihaldið marga forðaflokka, en forðaflokkur getur verið úthlutað á eina framleiðslueiningu. Framleiðslueining endurspeglar sjálft skipulag framleiðslutilfanganna og hefur engin áhrif á færslur eða hvernig þær eru unnar. Tengja valda framleiðslueiningu við svæði. Einnig er hægt er að tengja tiltektarvöruhús og geymsluvöruhús við framleiðslueiningu. Hægt er að nota framleiðslueiningu til að sameina og sía framleiðslutengd gögn. Til dæmis, vinnslusalarstjóri getur séð yfirlit yfir útistandandi vinnuálag og magn sem er í boði fyrir ákveðna framleiðslueiningu. Hægt er að breyta um framleiðslueiningu sem tengist hverjum tilfangaflokki. Einnig er hægt að eyða framleiðslueiningu. Þessar breytingar á framleiðslueiningu gilda þó aðeins fyrir nýjar pantanir sem eru stofnaðar eftir að aðalröðun er keyrð. Ef láta á breytinguna á framleiðslueiningu gilda um fyrirliggjandi pantanir verður að gera þessar breytingar handvirkt.

## <a name="resource-scheduling"></a>Röðun tilfanga
Rekstrartilföng eru úthlutuð á verkþætti þegar verks eða framleiðslu er raðað. tvær röðunaraðferðir eru tiltækar: aðgerðröðun  og vinnsluröðun. Þegar aðgerðaröðun er notuð, er hver aðgerðar eða verkþáttar áætlað á tilfangaflokk sem inniheldur rekstrartilföngum sem samsvara tilfangaþarfir sem tilgreind eru fyrir aðgerðina. Ef tiltekinn rekstrartilföng er áskilið fyrir aðgerðina, tekur röðun frá afköst í sérstakar rekstrartilföng í flokknum. Vinnsluröðun er ítarlegri mynd röðunar en aðgerðaröðun. Hún sundurliðar hverja aðgerð niður í einstök verk eða vinnslur. Þessum vinnslum er svo úthlutað rekstrartilföngum sem munu framkvæma þær. Röðun tekur frá afköst í tilfangaflokka, samkvæmt aðgerðatímar sem eru skilgreindar í framleiðsluleið eða verkþætti verkefna. Ef verið er að vinna með takmarkaðri afkastagetu, er áætlun háð tiltækileika rekstrartilfanga sem eru nauðsynleg til að ljúka við verkþáttinn. Fyrir aðgerðaröðun, eru afkastageta tilfangaflokks summa tiltækrar afkastagetu í rekstrartilföngum sem eru hluti af þeim flokki. Frátekningar á afkastagetu sem þegar er til fyrir í rekstrartilföngum eru álitin ótiltæk afkastagetu. Ef það er ekki nægilegt afköst tiltæk fyrir framleiðslu, getur framleiðslupantanir verið seinkað eða jafnvel stöðvað. Á **Tilföng**síðu er hægt að skilgreina nokkrum eiginleikum sem stjórna hvernig frátekning afkastagetu eru gerðar:

-   **Afkastageta** – Tilgreina afkastageta rekstrartilfanga á klukkustund hvað varðar mælieiningu afkastagetu.
-   **Runuafkastageta** – Tilgreina hámarksfjöldi stykki sem rekstrartilföng geta unnið per keyrslu.
-   **Skilvirkniprósenta** - Tilgreina skilvirkni sem búist er við frá rekstrartilföng. Skilvirkniprósenta leiðréttir gegnumstreymi rekstrartilfanga og hefur áhrif á tíma sem er frátekin fyrir tilfang. Afhendingartíma fyrir aðgerðir sem nota rekstrartilföng eru einnig breytt til samræmis. Hér er formúlan sem er notuð fyrir útreikninginn: röðunartími = tími x 100 ÷ skilvirkniprósenta. *Tími* inniheldur bæði keyrslutíma og uppsetningartíma.
-   **Prósenta aðgerðaröðunar** - Tilgreinið hámarkshlutfall afkastagetu rekstrartilfanga sem á að nota í aðgerðaröðun. til að leyfa sveigjanleika í afkastagetu við aðgerðarröðun á Þetta hlutfall að vera minna en 100%
-   **Takmörkuð afkastageta** **Þessi valkostur stilltur á** ef rekstrartilföng skuli raðað á grundvelli raunverulega afkastagetu sem er tiltækt, og ef taka skal tillit til fyrirliggjandi frátekningar á afkastagetu. Ef þessi valkostur er stilltur á **Nei**,  er gert ráð fyrir að rekstrartilföng hafa ótakmarkaða afköst, og gæti tilföngin því verið yfirbókaður.
-   **Takmarkaður eiginleiki** – þessi valkostur er Stilltur **Já** eigi rekstrartilföng að vera áætluð byggð á raunverulegum afkastagetu sem er tiltæk með tilliti til vinnutíma sem er krafist fyrir röðunareiginleika.
-   **Sértækt** – þessi valkostur er Stilltur **Já** ef þú vilt ekki að rekstrartilföng að vera til staðar fyrir aðra vinnu eða aðgerð þar til núverandi framleiðslunni er lokið. Þetta þýðir að ekki er hægt að nota rekstrartilföng jafnvel þótt eyður séu á keyrslutíma tilfanganna.
-   **Flöskuhálstilfang** – Skilgreina rekstrartilföng sem flöskuhálstilföng. Flöskuhálstilfangi er raðað með því að nota takmarkaða afkastagetu þegar valkostirnir **takmörkuð afköst** og **flöskuhálsröðun** á síðunni **aðaláætlun** eru valin.

Til að raða margar rekstrartilföng á sama tíma til að framkvæma, til dæmis, aðgerð í framleiðslu, verður að tilgreina þarfir fyrir mismunandi tilföng með því að nota aðal-og aukaaðgerðir. Þú getur einnig tekið frá mörgum rekstrartilföngum sem hafa mismunandi afkastagetu. Rekstrartilföng eru áætlaðar fyrir aðalaðgerðin ákvarða tímalengd verkþáttarins.

## <a name="lean-work-cells"></a>Lean-vinnuflokkar
Hægt er að tilgreina að tilfangaflokk er lean-vinnuflokkur. Tilfangaflokkurinn þá er hluti af framleiðsluflæðis. Með því að tilgreina tilfangaflokk sem lean-vinnuflokk, er einnig í komið í veg fyrir að tilfangaflokkinn og úthlutuðum rekstrartilföngum verið úthlutað á aðgerðir í framleiðslupöntun eða tímaspá verks. Fyrir hverja tilfangaflokk sem er lean-vinnuflokkur verður að tilgreina eftirfarandi upplýsingar:

-   **Dagatal** – vinnudagatal vinnuflokksins sem verður að hafa eiginleikann staðlaður vinnudagur.
-   **Inntaksvöruhús og staðsetning** – sjálfgefin staðsetning sem er notuð til að taka til efni fyrir verkþátt.
-   **Úttaksvöruhús og staðsetning** – sjálfgefin staðsetning þar sem allt úttak vinnuflokks er sett.
-   **Kostnaðartegund Keyrslutíma** – Þessi flokkur verður vera skilgreindur fyrir vinnuflokkur ef bein vinnu er rakin í kostnaðarútreikningur.

Til að nota á tilfangaflokk sem lean-vinnuflokkur , er afkastageta vinnuflokks tilgreindur beint á tilfangaflokki. Því þarf Ekki að úthluta rekstrartilföng á tilfangaflokk. aðeins Þegar vinnuflokkur er stjórnað af undirverktaka, þarf rekstrartilföng af gerðinni **Lánardrottins** að vera úthlutað á vinnuflokkinn. Ef rekstrartilföng er úthlutað á tilfangaflokk sem er merkt sem vinnuflokks, verður afkastagetu vinnuflokksins ekki fyrir áhrif.

## <a name="costing-resources"></a>Kostnaðartilföng
Þegar verkþáttur eins og leiðaaðgerð eða tímaspá verks er skilgreind, er hægt að tilgreina þarfir fyrir tiltekinna rekstrartilföng eða tilfangaflokkur. Þó er einnig hægt að tilgreina þarfir fyrir rekstrartilföng af tiltekna gerð, eða rekstrartilföng sem hefur tiltekna getu eða hæfni. Þess vegna er raunveruleg úthlutun tilfanga ekki gerðar fyrr en verkþátturinn er áætlaður og afkastageta er frátekið. Þess vegna á leiðaraðgerð, hægt er að tilgreina þetta mat og uppskriftarútreikningurinn verður að byggja á tilteknum rekstrartilföng. Þessi rekstrartilföng kallast kostnaðartilföng. Er einnig hægt að flytja kostnaðartegundir og aðgerðatímar úr kostnaðartilföng á verkþættinum. Þegar aðgerðinni er raðað, eru matið og uppskriftarútreikningurinn gerðar með því að nota rekstrartilföng sem er í raun raðað.



