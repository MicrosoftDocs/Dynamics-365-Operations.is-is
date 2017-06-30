---
title: "Vinnsluröðun"
description: "Þessi grein veitir upplýsingar um Vinnsluröðun sem er ítarlegri mynd röðunar en aðgerðaröðun. Hægt er að nota Vinnsluröðun til að raða einstakra vinnsla eða verslunarpöntunum, og til að stjórna framleiðsluumhverfi"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19431
ms.assetid: aef37341-91d8-4263-80eb-35d9584be156
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 3c7224390ce336439c2e43188c19b4b93cf793b8
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="job-scheduling"></a>Vinnsluröðun

[!include[banner](../includes/banner.md)]


Þessi grein veitir upplýsingar um Vinnsluröðun sem er ítarlegri mynd röðunar en aðgerðaröðun. Hægt er að nota Vinnsluröðun til að raða einstakra vinnsla eða verslunarpöntunum, og til að stjórna framleiðsluumhverfi

Hægt er að nota Vinnsluröðun til að raða einstakra vinnsla eða verslunarpöntunum, og til að stjórna framleiðsluumhverfi vinnsluröðun sundurliðar hverja aðgerð niður í einstök verk eða vinnslur. Þessum vinnslum er svo úthlutað rekstrartilföngum sem munu framkvæma þær. Vinnsluröðun gerir einnig kleift að samstilla allar vinnslur sem er vísar í úr valið verk. Hægt er að tilgreina upphafs- eða lokadagsetningu og tíma vinnslunnar og keyra svo röðun. Val á röðunarstefnu ræður því hvort tíminn sem tilgreindur er sé upphafs- eða lokatími. Þessi aðgerð er gagnleg þegar, til dæmis, vinnslu getur aðeins keyrt á einni vél í senn, eða þegar óskað er að fínstilla vinnslan er keyrð fyrir hvert tilfang.

## <a name="tasks-in-the-job-scheduling-process"></a>Verkefni í vinnsluröðunarferlinu
vinnsluröðunarferli felur í sér eftirfarandi verkefni:

-   Skipta rekstri í vinnslur.
-   Raða vinnslu á grundvelli dagsetninga og tímasetninga fyrir tilföng sem tilgreindar eru í tengdri aðgerð.
-   Reikna út upphafs- og lokatíma hverrar vinnslu. Hægt er að nota takmarkaða afkastagetu til að tryggja tíma skarast ekki.
-   Ákvarða hvaða tilföng í tilfangaflokki til að keyra vinnslu fyrir. Þetta verk krefst þess að tilfangaflokkur sé tilgreint fyrir aðgerð. Vinnsluröðun velur tilföng eða tilfangaflokka samkvæmt stysta afhendingartíma og tekur einnig tillit til allar fyrri frátekningar á tilföng.
-   Brjóta niður aðgerða í vinnslur þegar vinnsluröðun er keyrð. Vinnslum er raðað eftir dagsetningu og tíma, eftir þeirri röð sem er tilgreind í framleiðsluleiðinni. Uppsetning aðgerðarinnar ákvarðar vinnslur sem eru brotnar niður á meðan á röðuninni stendur. Leiðarflokkur sem er úthlutaður á aðgerð stýrir hvort vinnslur eru myndaðar. Vinnsla er mynduð aðeins ef hún hefur tiltekna tímalengd. Til dæmis er verk fyrir flutningstíma myndað ef flutningstími var tilgreindur fyrir valda aðgerð.

## <a name="scheduling-direction"></a>Stefna röðunar
Hægt er að raða vinnslum áfram eða afturábak.

-   **Áfram** - Notið röðunaraðferðina Áfram til að hefja framleiðsluna eins snemma og hægt er. Þetta er einnig þekkt sem aðferð ýtingar því verið er að ýta framleiðslunni í gegnum framleiðsluferðlið. Framleiðslu er raðað til að byrja og enda á fyrstu mögulegu dagsetningar.
-   **Afturábak**  Notið röðunaraðferðina afturábak til að hefja framleiðsluna eins seint og hægt er. Þetta er einnig þekkt sem aðferð dráttar því hún byggir á dagsetningunni þegar framleiðslan verður að vera lokið. Röðun afturábak telur aftur að síðustu mögulegu dagsetningu sem hefja má framleiðsluna án þess að rjúfa skilafrestinn.

## <a name="finite-capacity"></a>Takmörkuð geta
Hægt er að raða vinnslum með því að nota takmarkaða afkastageta. Þegar takmörkuð afkastageta er notuð má afkastagetu sem áætlað er ekki vera meiri en afkastageta sem er tiltæk fyrir tilfang. Tiltækur tími er skilgreindur sem tímabilið þegar vinnustöðin er opin og þegar engar aðrar frátekningar eru á afkastagetu. Röðun með sem byggist á takmarkaðri afkastagetu tryggir að upphafs- og lokatímar aðgerðar skarist ekki á tiltekinni dagsetningu. Afkastagetan sem þegar er tekin frá er tekin með í reikninginn og tekið er tillit til skörunar milli upphafs og lokatíma. Takmörkuð afkastageta ákvarðar magn afkastagetu sem verður að vera tiltækar fyrir tilföng ná bestu notkun á það tilfang. Þessi ákvörðun er jafnað við útreikning á stysta mögulega afhendingartíma milli aðgerða.

## <a name="finite-materials"></a>takmarkað efni
Vinnsluröðun sem byggir á takmörkuðu efni tryggir að efnin sem þarf séu tiltæk þegar aðgerðin hefst. Þessar takmarkanir eru skilgreindar af þekjureglum fyrir vörur. Röðun notar niðurbrot á þörfum til að ákvarða þegar hlutar vöru eru tiltækar. Ef raðað er án þess að takmörkuð efni séu stillt gerir kerfið ráð fyrir að allar vörur séu tiltækar þegar þeirra er þörf.

## <a name="finite-properties"></a>Takmarkaður eiginleiki
Vinnsluröðun sem bygir á takmörkuðum eiginleikum krefst þess að eiginleikar séu tilgreindir fyrir aðgerðir framleiðsluleiðar. Uppfylla þarf þessa eiginleika til að taka afkastagetu frá.

## <a name="references"></a>Tilvísanir
Vinnsluröðun raðar öllum framleiðslum sem vísað er í úr núverandi framleiðslu. Ef fleiri en ein undirframleiðsla er í framleiðslunni á að raða þeim á sama tíma og  aðalframleiðslunni vegna þess að ekki er hægt að ræsa aðalframleiðslu fyrr en tengdum undirframleiðslum er lokið.

## <a name="schedule-resources"></a>Raða tilföngum
Áætlunarkerfið kannar samsetningar tilfanga til að auðkenna þær samsetningar geta uppfylla þarfir. Hægt er að tilgreina valskilyrði með því að velja eitt af eftirfarandi gildum í **val aðaltifanga** á **færibreytur Röðunar** síðunni:

-   **Tímalengd** – röðunarvélin velur tilfang með stysta afhendingartíma. **Ábending:** Röðun eftir tímalengd getur valdið minnkað afköst þegar sama tilfangaflokkurinn inniheldur mörg tilföng og aukaaðgerðir eru notaðar. Hægt er að raða að hámarki 32 tilföng fyrir hverja aðgerð. Ef farið er umfram þetta magn birtast skilaboð úr Athugasemdakladda og vinnsluröðun finnur ekki næstbesta valkost við tilfang.
-   **Forgangur** – röðunarvélin velur tilfang sem hefur mestan forgang ef tvö eða fleiri tilföng hafa sömu getu og stig. Tilfang hefur lægsta tölulegt gildi í þessu svæði hefur mestan forgang.

Þegar vinnsluröðun er keyrð, áætlar kerfið tilfangaþörf á grundvelli þeirra takmarkana eru skilgreindar færibreytum tilfanga. Hægt er að stýra afkastagetu tilfanga með því að nota stillingar dagatals. Kerfið reiknar álag fyrir tilföng meðan á röðuninni stendur. **Athugasemd** Fyrir framleiðslur sem nota aðgerðir aðgerðaröðunar er hægt að keyra vinnsluröðun á eftir aðgerðaröðun. Ef ekki er verið að nota aðgerðaröðun er hægt að keyra vinnsluröðunina eina og sér.

## <a name="maximum-capacities-for-resources-per-job-order"></a>Hámarksafköstum fyrir tilföng á vinnslupöntun
Tilföng er úthlutað á vinnslum í gegnum vinnsluröðun. Hægt er að koma á fót hámarksafköstum fyrir tilföng á fyrir hverja vinnslupöntun. Til dæmis er hægt að setja kerfið upp með þeim hætti að eigi meira en 50% af heildarafköstum sé raðað fyrir framleiðslupöntun. Þessi uppsetning býður upp á frekari stjórn raða tilföngum á stigi vinnsluröðun. Þess vegna er það hægt að koma í veg fyrir vandamál ef ekki nægilegt afkastageta tiltækt til að framkvæma nokkrar framleiðslur samtímis.

## <a name="resource-efficiency"></a>Skilvirkni tilfanga
Vinnsluröðun tekur tillit til Skilvirkniprósentur sem eru tilgreindar fyrir tilföng. Skilvirkniprósentur minnka eða auka tímann sem tekinn er frá fyrir tilföng. Þar af leiðir að afhendingartími er einnig aukinn eða minnkaður. Eftirfarandi formúla er notuð fyrir útreikninginn: röðunartími = tími x 100 ÷ skilvirkniprósenta Í þessari formúlu, *tími* inniheldur bæti keyrslutími og uppsetningartími.




