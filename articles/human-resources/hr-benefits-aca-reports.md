---
title: Mynda skýrslur fyrir Affordable Care Act (ACA)
description: Skýrslugerð Affordable Care Act býr til eyðublöð 1095-B og 1095-C til stuðnings þeim hluta af Affordable Care Act sem snýr að **umboði vinnuveitanda**.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 055de1f0ff3f8fd4fadba0a685fd703b9d19d918
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805995"
---
# <a name="generate-aca-reports"></a>Mynda ACA-skýrslur

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Skýrslugerð Affordable Care Act býr til eyðublöð 1095-B og 1095-C til stuðnings þeim hluta af Affordable Care Act sem snýr að **umboði vinnuveitanda**.

> [!NOTE]
> ACA-skýrslugerð er aðeins virkjuð fyrir lögaðila í Bandaríkjunum.

## <a name="getting-started"></a>Hafist handa

Til að rekja upplýsingar fyrir eyðublöð 1095-B og 1095-C skal fyrst stofna einn eða fleiri Affordable Care-tryggingaflokka. Affordable Care-tryggingaflokkar tilgreina:

- Tryggingatilboð handa starfsmanni
- Hlutdeild starfsmanns í lægstu mánaðarlegu greiðslu iðgjalds, ef kostnaðurinn er fyrir ofan fátæktarmörk
- Örugg höfn sem er notuð af starfsmanni, ef á við

Affordable Care-tryggingaflokkar gera þér kleift að hafa umsjón með þessum reitum án þess að breyta öllum starfsmannafærslum þar sem skilyrðin eru þau sömu. Það er auðveldlega hægt að úthluta Affordable Care-tryggingaflokkum á einn eða fleiri starfsmenn með valkostinum **Fjöldaúthluta** á síðunni.

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a>Umsjón með mörgum útgáfum tryggingahóps

Hægt er að viðhalda mörgum útgáfum í hvaða tryggingaflokki sem er. Þessi virkni gerir þér kleift að gera breytingar án þess að þurfa að búa til nýjan flokk og endurúthluta starfsmönnum í hann. 

Þegar búið er að stofna ACA-tryggingaflokka er hægt að fjöldaúthluta flokkunum á starfsmenn með valkostinum **Fjöldaúthlutun**. Einnig er hægt að gefa til kynna í hverju tilfelli fyrir sig hvort eigi að rekja og tilkynna ACA-upplýsingar og úthluta starfsmanni á Affordable Care-tryggingaflokk.

Ekki þarf að rekja sumar ACA-tryggingaupplýsingar eins og fyrir starfsmenn í hlutastarfi. Í þessu tilfelli skal stilla reitinn **Telja tryggingu fram** á **Nei**. Þótt þurfi að úthluta hverjum starfsmanni rekjanlegar ACA-upplýsingar í Affordable Care-tryggingaflokk, er enn hægt að breyta eftirfarandi valkostum fyrir mánuði með ólíkum gildum:

- **Tryggingatilboð**
- **Kostnaðarhlutdeild starfsmanns**
- **Örugg höfn**

Til að færa inn undantekningar fyrir gildi Affordable Care-tryggingaflokks skal velja tengilinn **Affordable Care-trygging** á síðunni **Upplýsingar um starfsmann** undir hlutanum **Frekari upplýsingar** í flipanum **Starf**.

## <a name="reporting-health-care-coverage"></a>Skráning sjúkratrygginga

Auk þess að rekja sjúkratryggingu sem boðin er starfsmönnum í fullu starfi, ef vinnuveitandi býður upp á sjálfstryggða sjúkratryggingu kostaða af vinnuveitanda þar sem starfsmaðurinn er skráður (burtséð frá því hvort þeir eru í fullu starfi eða hlutastarfi), þarf að tilkynna frekari upplýsingar á 1095-C. Hver starfsmaður (þ.m.t. skjólstæðingar) sem tryggður er af tryggingum vinnuveitanda verður að vera skráður í skýrslunni fyrir þá mánuði sem hann var tryggður. 

Hægt er að gefa til kynna hvort tilkynna þurfi hverja fríðindaáætlun fyrir sig með því að velja gátreitinn **ACA-tilkynningaskylt**.

Að auki ef starfsmenn hafa valið að einhverjir skjólstæðinga þeirra verði tryggðir undir fríðindum, er hægt að gefa upp dagsetningarnar sem skjólstæðingurinn var tryggður fyrir hvern starfsmann á síðunni **Viðhalda fríðindum**. Til að gefa til kynna að skjólstæðingurinn sé tryggðir undir fríðindum skal velja hnappinn **Breyta** á aðgerðasvæði flýtiflipans **Skjólstæðingar**.

Á síðunni **Tímabilsstjórnun fyrir tryggingar skjólstæðinga** er hægt að tilgreina dagsetningar sem skjólstæðingar voru tryggðir samkvæmt fríðindum. Skráning dagsetninga á þessari síðu mun sjálfkrafa velja gátreitinn **Tryggður** á síðunni **Viðhalda fríðindum**.

## <a name="generate-1095-b-and-1095-c-forms"></a>Búa til eyðublöð 1095-B og 1095-C

Einnig er hægt að búa til eyðublöðin 1095-B og 1095-C innan afurðar og dreifa þeim til allra starfsmanna þinna. Kerfið getur einnig rafrænt búið til 1095-C eyðublöð og 1094-C skilaskrár til skattyfirvalda Bandaríkjanna.  

Þegar eyðublað 1095-C er búið til skal færa inn viðeigandi skattaár og tilgreina ef hylja á kennitölur. Ef eyðublað 1095-C er prentað fyrir fleiri en 500 starfsmenn færðu fleiri en eina PDF-skrá afhenta. Mælt er með því að auka **Hámarksstærð skráar** í glugganum **Færibreytur skjalastjórnunar** í 150 MB.

## <a name="viewing-information"></a>Skoðun upplýsinga

Hægt er að nota síðuna **Affordable Care-trygging fyrir starfsmann** til að sjá hvaða starfsmenn hafa verið settir í hvaða tryggingahóp, hvaða starfsmenn þurfa að ekki að vera í skýrslu og hvaða starfsmenn hafa ekki verið settir í neinn hóp.

Ef einhverjum sjálfgefnum gildum úr Affordable Care-tryggingaflokknum hefur verið hnekkt, birtist stjarna við hliðina á gildinu sem var breytt. Ef gildi fyrir alla 12 mánuðina eru þau sömu og þeim hefur ekki verið hnekkt, mun gildið prentast í dálknum **Allir 12 mánuðirnir**.

Einnig er hægt að nota fyrirspurnargluggann til að komast að því hvaða starfsmenn hafa verið flaggaðir sem ekki ACA-tilkynningaskyldir. Ekki þarf að fylgjast með því hvort þeim var boðin trygging og ekki þarf að gefa út 1095-C til þeirra í árslok. Velja skal **Er ekki ACA-tilkynningaskylt** í reitnum **Sía eftir** til að búa til lista yfir starfsmenn sem fá ekki 1095-C.

Að auki er hægt að skoða starfsmenn sem ekki úthlutað (reiturinn **Telja ACA-tryggingu fram** er auður) eða hefur verið úthlutað í Affordable Care-tryggingaflokk sem er útrunninn fyrir árið sem er valið í reitnum **Ár**.

Hægt er að flytja út lista yfir starfsmenn í Excel sem voru myndaðir með einhverjum af síunarkostunum.

Ef þarf að tilkynna tryggða einstaklinga vegna þess að þú býður upp á sjálfstryggða tryggingu, er hægt að skoða skjólstæðinga sem eru tryggðir undir fríðindaáætlunum merktar sem **ACA-tilkynningaskylt**. Veljið **Skoða tryggingar skjólstæðinga** á aðgerðasvæðinu.

> [!NOTE]
> Aðeins fríðindaáætlanir sem eru merktar **ACA-tilkynningaskylt** birtast í fyrirspurnarglugganum.


[!INCLUDE[footer-include](../includes/footer-banner.md)]