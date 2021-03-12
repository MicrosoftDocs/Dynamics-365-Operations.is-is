---
title: Bæta frammistöðu aðaláætlunargerðar
description: Þetta efni útskýrir hinar ýmsu valkosti sem geta hjálpað þér að bæta árangur aðaláætlunargerðar eða úrræðaleita vandamál.
author: t-benebo
manager: tfehr
ms.date: 12/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 380329cbeaa1fc2a2691c8165bc57483d1420aa1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005078"
---
# <a name="improve-master-planning-performance"></a>Bæta frammistöðu aðaláætlunargerðar

[!include [banner](../includes/banner.md)]

Þetta efni útskýrir hinar ýmsu valkosti sem geta hjálpað þér að bæta árangur aðaláætlunargerðar eða úrræðaleita vandamál. Það felur í sér upplýsingar um færibreytur og stillingar, ásamt ráðlögðum skilgreiningum og aðgerðum. Það felur einnig í sér samantekt á öllum mikilvægum færibreytum sem þú ættir að íhuga þegar þú ert með tímafrekar aðaláætlunargerðarvinnslur.

Þetta efni er ætlað fyrir kerfisstjóra eða tölvuþjónustumenn sem hafa getu til úrræðaleitar. Það er einnig ætlað fyrir framleiðslu- eða framkvæmdaáætlanagerð, þar sem það inniheldur upplýsingar um færibreytur sem tengjast viðskiptaáætlunarþörfum. 

## <a name="parameters-related-to-master-planning-performance"></a>Færibreytur sem tengjast frammistöðu aðaláætlanagerðar

Ýmsar færibreytur hafa áhrif á keyrslutíma aðaláætlunargerðar og taka ætti tillit til þeirra.

### <a name="number-of-threads"></a>Fjöldi þráða

Færibreytan **Fjöldi þráða** gerir þér kleift að breyta röðunarferlinu til að auðvelda að auka afköst þess í tilteknu gagnasafni. Þessi færibreyta tilgreinir heildarfjölda þráða sem verða notaðir til að keyra aðaláætlanagerð. Hún veldur samhliðun keyrslu aðaláætlunargerðar, sem lækkar keyrslutímann. 

Þú getur stillt færibreytuna **Fjöldi þráða** í valmyndinni **Keyrsla aðaláætlanagerðar**. Til að opna þessa valmynd skaltu fara í **Aðaláætlanagerð \> Aðaláætlanagerð \> Keyra \> Aðaláætlanagerð** eða velja **Keyra** á vinnusvæðinu **Aðaláætlanagerð**. Til að ákvarða besta gildið fyrir þessa færibreytu verður þú að treysta á happa- og glappaferli. Hins vegar getur þú notað eftirfarandi formúlur til að reikna út upphafsgildi:

- **Ef iðnaðurinn þinn er að framleiða:** (Fjöldi þráða) = (Fjöldi pantanatillaga ÷ 1.000)
- **Annars:** (Fjöldi þráða) = (Fjöldi vara ÷ 1.000)

Fjöldi hjálparatriða sem eru notuð í aðaláætlanagerð verður að vera minni en eða jafnt og hámarksfjöldi þráða sem leyfðar eru á runuþjóninum. Ef fjöldi hjálparatriða fer yfir fjölda þráða á runuþjóninum munu aukaþræðirnir ekki vinna neitt.

> [!NOTE]
> Stilling færibreytunnar **Fjöldi þráða** á **0** (núll) eykur keyrslutíma aðaláætlanagerðar. Þess vegna mælum við með að þú stillir alltaf gildi sem er hærra en 0.

### <a name="number-of-tasks-in-helper-task-bundle"></a>Fjöldi verka í hjálparverkbúnti

Með því að breyta stillingunni **Fjöldi verka í verkbúnti** (það er að segja, stærð búnts) gætirðu hugsanlega dregið úr keyrslutíma. Þessi stilling stjórnar fjölda vara sem eru áætlaðar saman á einni hjálparvél.

Þú getur stillt færibreytuna **Fjöldi verka í verkbúnti** í hlutanum **Frammistaða** á flipanum **Almennt** á síðunni **Færibreytur aðaláætlanagerðar** (**Aðaláætlanagerð \> Uppsetning \> Færibreytur aðaláætlanagerðar**). Besta gildi fyrir þessa færibreytu fer eftir gögnum þínum. Þess vegna mælum við með að þú byrjir á gildinu **1** og notir síðan happa- og glappaferli til að ákvarða besta gildið fyrir uppsetninguna.

Almennt mælum við með að þú aukir fjölda verka þegar fjöldi varanna er mjög stór (í hundruðum þúsunda). Annars ættirðu að draga úr fjölda verka. Í eftirfarandi tilteknum atvinnugreinum skaltu íhuga þessar ráðleggingar:

- Í smásölu- og dreifingariðnaði, þar sem margar sjálfstæðar vörur eru notaðar, skaltu nota mörg hjálparatriði þar sem engin fylgni er á milli vara. 
- Í framleiðsluiðnaðinum, þar sem margar eru uppskriftir (BOM) og samnýttir undiríhlutir, skaltu nota færri hajálparatriði þar sem fylgi milli vara gæti valdið biðtíma.

> [!TIP]
> Ef þú hefur frammistöðuvandamál mælum við með því að þú lækkir stillinguna **Fjöldi hjálparatriða í verkbúnti** í **1**. Síðan geturðu hafið happa- og glappaferlið til að finna besta gildið fyrir uppsetninguna. Almennt munu frammistöðuvandamál koma fram þegar ein vara tekur lengri tíma í vinnslu en þær sem eftir eru. Í þessu tilviki munt þú sjá að tvö síðari verkin sem hafa stöðuna **Þekja** í keyrslu aðaláætlanagerðar taka töluvert mismunandi tíma í keyrslu. Í afar alvarlegum tilvikum gæti þessi munur jafnvel verið 30 mínútur. Þú getur sleppt þeim tíma sem verk taka í keyrslu með því að skoða tímalengd hvers verks.

### <a name="use-of-cache"></a>Notkun skyndiminnis

Færibreytan **Notkun skyndiminnis** gerir þér kleift að breyta röðunarferlinu til að auðvelda frammistöðu þess í tilteknu gagnasafni. Til dæmis getur þú breytt því til að ná eftirfarandi niðurstöðum:

- Ef ofter er sett í skyndiminni er safnað fleiri gögnum í gagnaminnið. Búist er við að gögnin verði notuð aftur seinna. Ef gögnin eru í minni gætir þú vistað einhverjar gagnagrunnsbeiðnir. Hins vegar hækka minnisþarfirnar ef oftar er sett í skyndiminni.
- Ef sjaldar er sett í skyndiminni gæti þurft að sækja sömu gögnin oftar úr gagnagrunninum. Að auki geymir Application Object Server (AOS) litlar upplýsingar í minni í gegnum ferlið.

Það er erfitt að spá fyrir um hvaða valkostur verði betri, þar sem hvert tilfelli fer ekki aðeins eftir gögnunum heldur einnig vélbúnaði. Til dæmis, þar sem minni vistun í skyndiminni veldur viðbótarálagi á gagnagrunnsþjóninum, er líklega ekki góð hugmynd að nota þennan valkost ef þegar er yfirálag á gagnagrunninum.

Þú getur stillt færibreytuna **Notkun á skyndiminni** í hlutanum **Frammistaða** á flipanum **Almennt** á síðunni **Færibreytur aðaláætlanagerðar** (**Aðaláætlanagerð \> Uppsetning \> Færibreytur aðaláætlanagerðar**). Skilvirkni skyndiminnis fer ákaflega eftir viðskiptavinagögnunum. Til dæmis, ef afritaðra upplýsinga er aldrei þörf eyðir þú bara minni ef þú geymir gögn til loka röðunarferlisins. Í þessu tilviki, ef þú skilgreinir minna skyndiminni, gæti frammistaða aukist vegna þess að AOS krefst minna minnis og þjónstilföng losna fyrir önnur verk.

> [!TIP]
> Almennt mælum við með að þú stillir færibreytuna **Notkun skyndiminnis** á **Hámark** þar sem færibreytan er ætluð sem afkastaaukandi eiginleiki. Við mælum með að þú stillir færibreytuna á **Lágmark** ef þú keyrir inninhúss og ert með takmarkað minni (u.þ.b. 2 gígabæt \[GB\]).

### <a name="number-of-orders-in-firming-bundle"></a>Fjöldi pantana í staðfestingarbúnti

Færibreyta **Fjöldi pantana í staðfestingarbúnti** tilgreinir heildarfjölda pantana sem verða unnar í einu af hverjum þræði/runu. Hún veldur samhliðun ferlis sjálfvirkar staðfestingar.

Þú getur stillt færibreytuna **Fjöldi pantana í staðfestingarbúnti** í hlutanum **Frammistaða** á flipanum **Almennt** á síðunni **Færibreytur aðaláætlanagerðar** (**Aðaláætlanagerð \> Uppsetning \> Færibreytur aðaláætlanagerðar**). Samhliðun ferlis sjálfvirkrar staðfestingar er byggð á pöntunum sem verður að vinna saman. Til dæmis, ef þessi færibreyta er stillt á **50** mun hver þráður eða runuverk tína til 50 pantanir í einu og vinna þær saman. Við mælum með að þú notir happa- og glappaferlið til að finna besta gildið. Hins vegar getur þú notað eftirfarandi formúlu til að reikna út upphafsgildi:

(Fjöldi pantana á búnt) = (Fjöldi eftirspurnarþátta ÷ Fjöldi þráða)

> [!NOTE]
> Ef þú stillir færibreytuna **Fjöldi pantana í staðfestingarbúnti** á **0** (núll) mun engin samhliðun verða á ferli sjálfvirkrar staðfestingar. Allt ferlið mun keyra á einu runuverki og hafa uppsafnaðan keyrslutíma. Þess vegna mun keyrslutími aðaláætlanagerðar aukast. Af þessum sökum mælum við með því að þú stillir þessa færibreytu á gildi sem er hærra en **0** (núll).

### <a name="time-fences"></a>Tímamörk

Tímamörkin tilgreina hversu langt fram í framtíðina útreikningar og aðrar þarfir þurfa að vera reiknuð með aðaláætlunargerðinni. Því stærri sem tímamörkin eru, því lengur mun það taka fyrir aðaláætlunargerðina að keyra. Þess vegna skaltu stilla tímamörk í samræmi við þarfir fyrirtækisins. Nánari upplýsingar um tímamörkin er að finna í [Setja upp aðaláætlunargerð](master-planning-setup.md).

### <a name="actions"></a>Aðgerðir

Meðal tímamarkanna geturðu einnig fundið færibreytuna **Aðgerðaboð**. Útreikningur á aðgerðaboðum veldur lengri tíma keyrslutíma á aðaláætlunargerð. Ef aðgerðaboð eru ekki reglulega greind og beitt (daglega, vikulega og svo framvegis) skaltu íhuga að slökkva á útreikningi meðan á keyrslu aðaláætlunargerðar stendur. Til að slökkva á útreikningi skaltu á síðunni **Aðaláætlanir** (**Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Aðaláætlanir**) stilla tímamörkin **Aðgerðaboð** á **0** (núll). Gakktu einnig úr skugga um að slökkt sé á stillingunni **Aðgerðaboð** í öllum þekjuflokkunum.

### <a name="futures"></a>Framvirkir samningar

Útreikningur á framvirkum samningum veldur lengri keyrslutíma á aðaláætlunargerð. Ef þú ert ekki að skipuleggja BOM, eða ef ekki þarf að birta tafir frá framboði til eftirspurnar við áætlanagerð, skaltu íhuga að slökkva á útreikningum á framvirkum samningum á meðan aðaláætlanagerð stendur. Til að slökkva á útreikningum skaltu stilla tímamörkin **Framvirkir samningar** á **0** (núll) fyrir aðaláætlanagerðina sem þú ert að keyra. Gakktu einnig úr skugga um að slökkt sé á stillingunni **Framvirkir samningar** í öllum þekjuflokkunum.

## <a name="one-heavy-routine-at-a-time"></a>Ein þung rútína í einu

Þegar þú raðar aðaláætlanagerð skaltu ekki raða annarri runuvinnslu um leið. Passaðu sérstaklega að þú raðir ekki öðrum þungum rútínum, eins og birgðum nálægt, á sama tíma.

## <a name="review-the-session-log"></a>Yfirfara lotukladda

Kerfið getur safnað viðbótarupplýsingum um þau verk sem keyra á meðan aðaláætlanagerð stendur. Til að kerfið safni þessum upplýsingum skaltu kveikja á stillingunni **Rekja vinnslutíma** í valmyndinni **Keyra aðaláætlanagerð**. Upplýsingarnar sem er safnað geta hjálpað þér að finna flöskuháls í keyrslunni. Til dæmis, þegar færibreytan **Fjöldi verka í hjálparverkbúnti** er stillt á **1** geturðu bent á vöruna sem er með lengsta keyrslutímann. Þú getur einnig borið saman keyrslutíma fyrir hina ýmsu þræði sem hafa stöðuna **Þekja** og borið saman lengd hvers verks.

Til að endurskoða keyrslur aðaláætlanagerðar í kerfinu skaltu fylgja einum af þessum skrefum.

- Á vinnusvæðinu **Aðaláætlanagerð** skaltu velja aðaláætlun í fellilistanum og síðan í glugganum **Aðaláætlanagerð** velja **Saga**. Veldu vinnslu, veldu **Fyrirspurnir** á flýtiflipanum og veldu síðan **Lengd vinnsluverka**.
- Á síðunni **Aðaláætlanir** skaltu velja áætlun í vinstri glugganum og síðan **Saga** á flýtiflipanum. Veldu vinnslu, veldu **Fyrirspurnir** á flýtiflipanum og veldu síðan **Lengd vinnsluverka**.

Þegar þú skoðar lotukladdann skaltu skoða eftirfarandi:

- **Uppfærsla** ætti ekki að taka langan tíma (almennt ætti hún að taka allt að 30 mínútur), hins vegar er hann einþráða.
- **Afrita áætlun** ætti ekki að taka langan tíma (það ætti að taka um eina mínútu).
- **Sjálfvirk staðfesting** tekur yfirleitt um 30 mínútur. Hins vegar getur hún tekið allt að margar klukkustundir, allt eftir fjölda pantana og flækjustigs á vörum.
- **Sjálfvirk staðfesting** ætti að taka minni tíma en **Þekja**.
- **Þekja** ætti að taka lengstan tíma miðað við restina.
- **Aðgerð** og **Framvirk boð** geta tekið langan tíma, allt eftir gögnum og fjölda BOMs.

## <a name="filtering-of-items"></a>Afmörkun á vörum

Síur sem eru notaðar í svarglugganum **Keyra aðaláætlanagerð** hafa áhrif á lengd keyrslu aðaláætlanagerðar. Farðu í **Aðaláætlanagerð \> Aðaláætlanagerð \> Keyra \> Aðaláætlanagerð** eða veldu **Keyra** í vinnusvæðinu **Aðaláætlanagerð**. Til að útiloka vörur frá keyrslunni mælum við með að þú afmarkir eftir líftímastöðu vörunnar (ekki eftir vörunúmerum). Þegar þú afmarkar eftir líftímastöðu mun uppfærsluferlið taka minni tíma en þegar þú afarmarkar eftir vörunúmerum.

## <a name="automatically-filter-by-items-with-direct-demand"></a>Sía sjálfkrafa eftir atriðum með beinni eftirspurn

Til að bæta tímalengd aðalskipulags geturðu valið að taka aðeins til hluti með beina eftirspurn. Þessa síu er aðeins hægt að nota til að ljúka aðalskipulagningu og engar aðrar síur eru notaðar í reitnum **Færslur til að fela í sér**. Aðaláætlunargerð keyrð með síum mun hunsa stillinguna **Sía sjálfkrafa eftir atriðum með beinni eftirspurn**.

Reitinn **Sía sjálfkrafa eftir atriðum með beinni eftirspurn** er að finna á síðunni **Færibreytur áætlanagerðar** og hægt er að nota hann bæði með forvinnslu og eftirvinnslu.

### <a name="pre-processing"></a>Forvinnsla í gangi
Færibreytan **Forvinnsla: Sía sjálfkrafa eftir atriðum með beinni eftirspurn** tryggir að forvinnslufasi aðalskipulagningar feli aðeins í sér atriði sem uppfylla að minnsta kosti eitt af eftirfarandi skilyrðum:
  - Atriðið er með væntanlega kvittun eða útgáfu, svo sem innkaupapöntun, sölupöntun, tilvitnun, flutningspöntun eða framleiðslupöntun. 
  - Atriðið er með umfjöllun um hlutina með öryggisbirgðum (lágmarkskröfur á lager).
  - Spáaeftirspurn eftir daginn í dag er til fyrir atriðið.
  - Spáaframboð eftir daginn í dag er til fyrir atriðið.
  - Atriðið nær yfir allar samfellulínur úr símaverseiningunni sem enn er ekki búin til.

> [!NOTE]
> Atriði sem er með efnislega tiltækar lagerbirgðir sýnir ekki þarfafærslu vegna þess að engin eftirspurn er eftir atriðinu.

### <a name="post-processing"></a>Eftirvinnsla
Valkosturinn **Eftirvinnsla: Sía sjálfkrafa eftir atriðum með beinni eftirspurn** er aðeins viðeigandi ef þú stillir **Þörf skv. uppskriftarútgáfu** í þekjuflokkunum þínum. Annars þarftu ekki að virkja færibreytuna. 

Áður en þekjuskrefið hefst er fyrirframþekjuskref þar sem atriði með virkjaðri þekjustillingunni **Þörf skv. uppskriftarútgáfu** verður endurunnið. Þetta er gert til að tryggja að atriði úr nauðsynlegri útskriftarútgáfu séu fyrirhuguð. Atriði sem eru talin hafa eftirspurn við forvinnslu hafa ekki lengur neina eftirspurn og ætti því að vera útilokuð úr keyrslu áætlanagerðar.

## <a name="performance-checklist-summary"></a>Tékklistasamantekt frammistöðu

- **Fjöldi þráða** – Stilltu á gildi sem er hærra en **0** (núll).
- **Fjöldi verka í hjálparverkabúnti** – Stilltu á gildi sem er hærra en **0** (núll). (Notaðu formúlurnar sem eru gefnar fyrr í þessu efni.)
- **Notkun skyndiminnis** – Stilltu á **Hámark** nema kerfið hafi lítið minni.
- **Fjöldi pantana í staðfestingarbúnti** – Stilltu á gildi sem er hærra en **0** (núll). (Notaðu formúluna sem er gefin fyrr í þessu efni.)
- **Tímamörk** – Stilltu eftir þörfum fyrirtækisins.
- **Aðgerðir og framvirkir samningar** – Slökktu á aðgerðum og framvirkum samningum ef þú notar þau ekki.
- **Ein þung rútína í einu** – Keyrðu ekki aðaláætlanagerð ásamt öðrum þungum rútínum.
- **Yfirfara lotukladda**.
- **Afmörkun á vörum** – Notaðu líftímastöðuna til að útiloka vörur frá aðaláætlanagerð. (Ekki nota vörunúmerin.)
