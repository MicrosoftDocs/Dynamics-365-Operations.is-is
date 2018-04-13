---
title: "Aðgerðröðun"
description: "Þetta efni inniheldur upplýsingar um aðgerðröðun. Hægt er að nota aðgerðaröðun til að fá almennt mat á framleiðsluferli yfir tíma."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 198073
ms.assetid: 12c28b11-80aa-4668-b15b-724cb24890bd
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 81dec9d988b22959df5421b7b84ef532a28e1228
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="operations-scheduling"></a>Aðgerðröðun

[!INCLUDE [banner](../includes/banner.md)]

Þetta efni inniheldur upplýsingar um aðgerðröðun. Hægt er að nota aðgerðaröðun til að fá almennt mat á framleiðsluferli yfir tíma.

Hægt er að raða framleiðslu á stigi aðgerðina og stigi vinnslu. Öfugt við vinnsluröðun brýtur aðgerðaröðun ekki aðgerðir fyrir framleiðsluleið niður í vinnslur. Ef þú vilt hafa meiri nákvæmni í áætluninni, eins og upplýsingar um gildandi getu, er hægt að keyra vinnsluröðun þegar búið er að keyra aðgerðaröðun. Einnig er hægt að keyra eingöngu vinnsluröðun. Vinnsluröðun er yfirleitt notuð til að raða einstaka vinnslu í vinnusal og fyrir tímamörk sem eru undireins eða til stutts tíma.

## <a name="components-of-operations-scheduling"></a>Hlutar aðgerðaröðunar
Helstu hlutar aðgerðaröðunar eru áætlunarstefna, afkastageta tilfanga og efnisbestun. Með því að nota aðgerðaröðun er hægt að ná eftirfarandi markmiðunum:

-   Stjórna áætlunaraðferð með því að áætla áfram eða afturábak frá tiltekinni dagsetningu.
-   Fínstilla notkun tilfanga með því að áætla framleiðslu á grunni afkasta tilfanga. Þessa nálgun hjálpar við að tilgreina hvenær á að nota önnur tilföng.
-   Fínstilla notkun hráefna með röðun framleiðslu samkvæmt tiltækileika nauðsynlegra hráefna.
-   Raða og samstilla viðmiðunarvara. Dagsetningar tilvísunarframleiðslum eru leiðréttar þegar röðun framleiðslupöntunar breytist.

Þú verður að áætla kostnað við framleiðslupöntun áður en þú getur keyrt aðgerðröðun. Hafi mat ekki verið keyrt verður það gert sjálfkrafa áður en aðgerðaröðun er framkvæmd. Aðgerðarröðun tilgreinir eftirfarandi upplýsingar:

-   Afurð sem er áætlað fyrir framleiðslu
-   Afbrigði vörunnar.
-   Magn sem taka þátt í framleiðslu
-   Dagsetningin og tíminn sem framleiðsla mun hefjast og enda.
-   Frátekin afkastageta fyrir tilföng sem framkvæma verkþættir framleiðslu

Uppsetningartími, vinnslutími eða keyrslutíma eru stillt fyrir aðgerðum í framleiðslunni. Þegar búið er að keyra aðgerðaröðun, er staða framleiðslupöntunar **Raðað**, og öllum aðgerðum eru raðaðar í þeirri röð sem tilgreind er af framleiðsluleið. Hins vegar er aðeins tekið tillit til þess tíma sem aðgerðin varir. Upphafs- og lokatími eru ekki raðaðir.

## <a name="scheduling-direction-and-date"></a>Stefna og dagsetning röðunar
Röðunarstefnan er grunnþáttur röðunarferlisins. Hægt er að raða framleiðslu fram eða aftur í tíma frá hvaða dagsetningu sem er, eftir þörfum.

-   **Áfram frá röðunardagsetning** – þú getur raðað framleiðslu til að byrja eins fljótt og möguleg er. Framleiðslan getur hafist í dag, á morgun eða á hvaða síðari dagsetningu sem er. Framleiðslu er raðað áfram í tímann á fyrstu mögulega lokadag.
-   **Afturábak frá röðunardagsetning** – þú getur raðað framleiðslu til að byrja eins seint og möguleg er. Röðun afturábak er byggt á dagsetningunni þegar framleiðslan verður að vera lokið. Áætlun telur afturábak frá þeim degi til síðustu mögulegu dagsetningar sem framleiðslan getur hafist og enn verið lokið á réttum tíma.

## <a name="resource-scheduling"></a>Röðun tilfanga
Þegar aðgerðaröðun er keyrð er hverri aðgerð í framleiðsluleiðinni raðað fyrir tilföng sem er tilgreind fyrir aðgerðina. Auk þess er tímalengd hverrar aðgerðar tilgreind í framleiðsluleiðinni. Ef á tilfangaflokk er tilgreindur fyrir aðgerð snýr röðun afköstum við fyrir flokkinn. Hins vegar ólíkt vinnsluröðun velur aðgerðaröðun ekki tiltekin tilföng í flokknum. Ef verið er að vinna með takmarkaðri afkastagetu, er áætlun háð tiltækileika tilfanga sem eru nauðsynleg til að ljúka við framleiðsluna. Aðgerðaröðun fer eftir röðun aðgerða sem eru tilgreind á framleiðsluleið. Röðun tekur frá afköst í tilfangaflokka, samkvæmt aðgerðatímar sem eru skilgreindar í framleiðsluleið. Summa tiltæktrar afkastageta á tilföngum sem koma að máli ákvarða afkastagetu fyrir tilfangaflokk. Frátekningar á afkastagetu sem þegar er til fyrir í tilföngum eru álitin ótiltæk afkastagetu. Ef það er ekki nægilegt afköst tiltæk fyrir framleiðslu, getur framleiðslupantanir verið seinkað eða jafnvel stöðvað. Einnig hægt að tilgreina skilvirkni sem búist er við frá tilföng sem tengjast framleiðslunni. Tilgreina skilvirkni í prósentum á tilföng. Skilvirkniprósenta leiðréttir gegnumstreymi tilfanganna. Þessi leiðrétting hefur áhrif á tíma sem er frátekin fyrir tilfang. Afhendingartíma fyrir aðgerðir sem nota tilföng eru einnig breytt til samræmis.

## <a name="operations-scheduling-and-master-planning"></a>Aðgerðaröðun og áætlanagerð
Aðgerðaröðun keyrir líka aðaláætlanagerð, sem ákvarðar hráefnisþarfaútreikninga. Aðgerðaröðun tekur tillit til eftirfarandi upplýsinga:

-   **Framleiðslur sem er ólokið** – Vörur sem eru áætlaðar, losaðar, hafnar
-   **Efnisframboð** – Birgðir, undirframleiðsla, birgjar og lánardrottnar
-   **Tiltæk Afkastageta** – Tilföng sem eru nauðsynleg fyrir framleiðsluna

## <a name="cancellations"></a>Afturkallanir
Þegar aðgerðaröðun er keyrð er hægt að hætta við tilteknum hlutum leiðar. Þessum hluta innihalda biðtíma, uppsetningartíma, vinnslutími, skörunartímans og flutningstíma.

## <a name="finite-materials"></a>takmarkað efni
Ef verið er að vinna með endanlegt magn, er áætlun einnig háð tiltækileika hráefna sem eru nauðsynleg við framleiðsluna. Ef ekki eru til nægilega margir íhlutir fyrir framleiðsluna, má fresta framleiðslunni. Hægt er að byggja röðun á efnisnotkun með því að tilgreina efni sem verður að vera tiltækt fyrir framleiðslu. Þegar þú fínstilla bæði forðagetu og tiltækt hráefni er framleiðslan reiknuð samkvæmt þessar takmarkanir. Ekki er hægt að raða framleiðslupöntun fyrr en afköst og hráefni eru tiltæk á sama tíma og í nauðsynlegu magni.

<a name="see-also"></a>Sjá einnig
--------

[Valkostir aðgerðaröðunar](operation-scheduling-options.md)




