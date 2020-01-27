---
title: Gera handvirkar leiðréttingar á grunnlínuspánni
description: Þetta efnisatriði útskýrir hvernig á að gera handvirkar leiðréttingar á grunnlínuspá og skoða upplýsingar um spá.
author: roxanadiaconu
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c9963a54a052549a6bfeabcb3d91b7b0f3cf68e
ms.sourcegitcommit: 34395464ec80cea800b953eae49af579d436fc1b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/07/2020
ms.locfileid: "2935417"
---
# <a name="make-manual-adjustments-to-the-baseline-forecast"></a>Gera handvirkar leiðréttingar á grunnlínuspánni

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að gera handvirkar leiðréttingar á grunnlínuspá og skoða upplýsingar um spá. 

Áður en handvirkar leiðréttingar eru gerðar er mikilvægt að skilja nokkur hugtök útskýrð í mismunandi síður.

## <a name="grid-on-the-adjusted-demand-forecast-page"></a>Hnitanetið á leiðréttri eftirspurnarspársíðu
**Leiðrétt eftirspurnarspá** síða inniheldur hnitanet sem hefur eftirfarandi skipulag:

-   Fyrsti dálkurinn sýnir vörur, úthlutunarlykla vöru, fyrirtæki og svo framvegis sem spáin hefur verið myndaður fyrir. Undirfyrirsögn síðu gefur lýsingu á gildandi spávíddir sem birtast í hnitanetinu. Til dæmis, ef undirfyrirsögn síðu er **Fyrirtæki / Svæði / úthlutunarlykill Vöru**, og ein hausalínan í hnitanetinu er **USMF / 1 / D\_Alloc** sýnir sú lína spána fyrir USMF fyrirtækis , svæði 1, og **D\_Alloc** úthlutunarlykil vöru.
-   Síðari dálkar tákna spárammana sem spáin hefur verið myndaður fyrir. Hver dálkhaus er fyrsta dagsetning spáramma sem dálkurinn sýnir.
-   Gildin í reitirnir standa fyrir spá fyrir eina vöru, úthlutunarlykill vöru og svo framvegis fyrir tiltekna spáramma.

## <a name="forecast-aggregation-and-de-aggregation"></a>uppsöfnun Spár og af-uppsöfnun
Undirfyrirsögn síðu sýnir stigið fyrir uppsöfnun spár. 

Til dæmis, ef undirfyrirsögn síðu er **Fyrirtæki / Svæði / úthlutunarlykil / Vörunúmer / Litur / Stærð / Skilgreiningu / Stíll**, er engin uppsöfnun spár og spá er sýnd á stigi vöru víddar hennar. Ef breyta á uppsöfnun er að nota í **Breytingu spávíddir** síðu sem hægt er að opna úr hugbúnaðarvalmyndinni. 

Til að breyta spánni, smellið á eitthvað hólf sem er tiltækt, og slá inn leiðrétt spárgildi. Nýju hólf verður strax feitletrað til að tilgreina að spá sem hún sýnir er ekki spáin sem þjónusta eftirspurnarspár stofnaði, en hefur verið leiðrétt handvirkt. 

Ef þú breytir uppsöfnun til að sýna fleiri uppsöfnuð gögn, er hægt að nota síðuna **eftirspurnarspálínur** síðu til sjá einstaka spárlínur sem mynda uppsafnaða spá. 

Til dæmis, þú hefur búið spá á stigi vörunnar, en þú veist að eftirspurn eftir þessari vöru mun aukast á öllum staðsetningum vegna kynningar eða annan svipaðan viðburð. Í þessu tilfelli er hægt að stilla uppsöfnun á **Fyrirtæki / Vöru úthlutun skilgreiningarlykils / Vöru** á **Breyta spávíddum** síðu. Hægt er að leiðrétta altæka spá fyrir vöruna yfir öll svæði í **Leiðrétt eftirspurnarspá** hnitanetinu. Til að sjá áhrifin af breytingu þinni yfir öll svæði, opna í **eftirspurnarspálínur** síðu. Á þessari síðu birtist ein lína fyrir vöruna fyrir hvert svæði, leiðrétt spármagn og upprunalet spármagn. 

Þegar spáð magn er leiðrétt á uppsöfnuðum stigum notar kerfið vegna úthlutun til að dreifa breytingu á milli lína sem stofna uppsöfnunina. 

Einnig er hægt að gera handvirkar leiðréttingar á á **eftirspurnarspálínur** síðu með því að breyta annað hvort **Heildarmagn** gildi eða **Magn** hólfum í af-uppsöfnunar hnitanetinu.

## <a name="viewing-details-of-the-forecast"></a>Skoða upplýsingar um spá
Hægt er að opna **upplýsingar eftirspurnarspár** síðu til að skoða frekari upplýsingar um spá. 

**upplýsingar eftirspurnarspár** síða sýnir eftirfarandi upplýsingar í myndrænu og töflulegu sniði:

-   Söguleg eftirspurn sem spáreru byggðar á.
-   Núverandi spá sem er notað með aðaláætlanagerð.
-   Ný gildi eftirspurnarspár og upphæðir sem þeir hafa verið breytt handvirkt eftir.
-   Áreiðanleikabil fyrir spáð gildi.
-   Spárlíkan sem var notað til að búa til spá. Ef verið er að skoða uppsöfnuð gögn , sérðu lista yfir allar aðferðir sem voru notaðir fyrir allar uppsafnaðar tímaraðir.
-   Innri nákvæmni líkans (MAPE). Nánari upplýsingar um nákvæmni eftirspurnarspár í [Eftirlit með nákvæmni spár](monitor-forecast-accuracy.md).

**Athugasemdir :**

-   Ef þú virkjar **Spá fyrir um líkanaval í Upplýsingum um eftirspurnarspá** úr Stjórnun eiginleika muntu geta valið spárlíkönin til að hafa með í sögulegri spá á síðunni **Upplýsingar um eftirspurnarspá**.
-   Áreiðanleikabil sem birtist í á **Spá** hluta síðan sýnir mismuninn á milli efri mörk áreiðanleikabils og neðri mörk áreiðanleikabils. Til að sjá gildi fyrir efri og neðri mörk , settu músabendil yfir línurit í á **söguleg eftirspurn og spá myndrænt** hluta.
-   Ef notuð er eftirspurnarspá í Microsoft Azure Machine Learning er hægt að tilgreina prósentu áreiðanleikastigs sem mynduð spá á að hafa. Áreiðanleikabil samanstendur af sviði gilda sem virka sem áreiðanlegt mat fyrir eftirspurnarspána. Til dæmis gefur 95% áreiðanleikastig til kynna að það séu 5% líkur á að eftirspurnarspá falli utan sviðs áreiðanleikabils.

Einnig er hægt að gera handvirkar leiðréttingar á spá í **upplýsingar eftirspurnarspár** síðu með því að breyta gildum í á **Spá** línunni í á **Spá** hluta.

<a name="additional-resources"></a>Frekari upplýsingar
--------

[Eftirlit með nákvæmni spár](monitor-forecast-accuracy.md)

[Myndun tölfræðilegrar grunnlínuspár](generate-statistical-baseline-forecast.md)



