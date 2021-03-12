---
title: Reikna út efnisnotkunina
description: Þessi grein gefur upplýsingar um ýmsa valkosti sem tengjast útreikningi á efnisnotkun.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: acccc677c855fc675d52814d7f6f0a5141bbc8af
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001671"
---
# <a name="calculate-material-consumption"></a>Reikna út efnisnotkunina

[!include [banner](../includes/banner.md)]

Þessi grein gefur upplýsingar um ýmsa valkosti sem tengjast útreikningi á efnisnotkun. 

eftirfarandi valkosti sem tengjast útreikningi á hráefnisnotkun eri tiltækir í **Uppsetningu** og **Skrefanotkun** flipana í á **Línuupplýsingar** flýtiflipa í **Uppskrift** síðu.

## <a name="variable-and-constant-consumption"></a>Breytileg og föst notkun
Í **Notkun er** reit er hægt að velja hvort eigi að reikna notkun út sem fast magn eða breytilegt magn. Velja **Fast** ef fast magn eða rúmmál er nauðsynleg fyrir framleiðsluna, óháð því magni sem er framleitt. Velja **Breytilegt**, sem er sjálfgefna stillingin, sé áskilin upphæð efnis í fullbúnu vörunum í hlutfalli við fjölda fullbúnar vörur sem eru framleiddar.

## <a name="calculating-consumption-from-a-formula"></a>Formúla notuð við útreikning notkunar
Í **Formúlu** svæði er hægt að setja upp mismunandi formúlur til að reikna út efnisnotkunina. Ef nota á sjálfgefna gildið **Staðlaða**, notkun er ekki reiknað út frá formúlu. Eftirfarandi formúlur vinna ásamt **Hæð**, **Breidd**, **Dýpt**, **Þéttleiki**, og **Fast** svæði:

-   Hæð \* Fasti
-   Hæð \* Breidd \* Fasti
-   Hæð \* Breidd \* Dýpt \* Fasti
-   (Hæð \* Breidd \* Dýpt / Þéttleiki) \* Fasti

## <a name="rounding-up-and-multiples"></a>Sléttun og margfeldi
Saman leyfa reitirnir **Sléttun** og **Margfeldi** þér að slétta gildi efnisnotkunar . Til dæmis er hægt að slétta gildinu samkvæmt afgreiðslueiningu sem hráefni er tekin til fyrir framleiðslu. Eftirtaldir valkostir eru tiltækir í **Sléttun** svæði: **Magn**, **Mælingu**, og **Notkun**.

### <a name="quantity"></a>Magn

Ef **Magn** er valið sem sléttunar mekanismi, verður magn að vera margfeldi af tilgreindu magni. Til dæmis ef þörf er á heiltölum er **1** tilgreint í svæðinu **Margfeldi**. Tölur eru svo sléttað í magn sem má deila með 1.

### <a name="measurement"></a>Mæling

Yfirleitt, veljið **Mælingu** sem mekanisma sléttunar þegar hráefni kemur í ákveðnum stærðum. Til dæmis er stykki af 2 metra málmröri krafist fyrir fullbúin framleiðsluvara og málmrörið er geymt í 4.5 metra lengdum. Í þessu tilfelli má nota **Mælingu** mekanisma sléttunar til að reikna út hversu mörg málmrör þarf til að framleiða tiltekinn fjölda stykkja fullbúinnar framleiðsluvara. Til dæmis hér, í **Formúlu** er stillt á **Hæð \* Fasti**. Í **Hæð** er stillt á **2** til að tilgreina lengd rörs sem er krafist fyrir fullbúin framleiðsluvara. Í **margfeldi** er stillt á **4.5** til að tilgreina í rör er tekið til í lengdir 4.5 metra. Útreikningurinn er:

1.  Fjöldi margfelda sem er krafist fyrir 10 stykki af fullbúin framleiðsluvara: 10 ÷ 2 = 5 stykki
2.  Samtals notkun:  4,5 × 5 = 22.5 metrar af málmröri

Gert er ráð fyrir að 0.5 metra af röri sé sett í rýrnun fyrir hver fimm stykki af rörum sem eru notaðar.

### <a name="consumption"></a>Notkun

Yfirleitt, veljið **Notkun** sem mekanisma sléttunar þegar hráefni verður að vera tekið til í heilu magni tiltekinnar afgreiðslueiningar vöru. Til dæmis er 2 fjórðungar af málningu notaðir til að framleiða einu stykki hinnar fullbúnu framleiðsluvara, og málning er tekið til í 25 fjórðungsdollum. Í þessu tilfelli er hægt að nota **Notkun** mekanisma sléttunar til að slétta notkun á heilar tölur fyrir 25 fjórðungsdollum. Hér er útreikningur fyrir magn málningar sem er krafist ef framleiða þarf 180 stykki fullbúinnar framleiðsluvara:

1.  Málning þarf án rýrnunar: 180 × 2 = 360 fjórðungar
2.  Fjöldi dósa: 360 ÷ 25 = 14.4 sem er sléttað að 15
3.  Málning sem þarf án rýrnunar: 15 × 25 = 375 fjórðungar

## <a name="step-consumption"></a>Skrefanotkun
Skrefanotkun er notuð til að reikna út fastanotkun í magntímabilum. Ef þú velur **Skrefi notkun** í á **Formúlu** reit á í **Uppsetningu** flipa, er hægt að bæta upplýsingar um skref á í **Skrefanotkun** flipa. Fast notað magn er hægt að stilla í timabilum fyrir framleitt magn. Til dæmis er skrefanotkun sett upp eins og sýnt er í eftirfarandi töflu.

| Frá-röð | Magn |
|-------------|----------|
| 0,00        | 10.0000  |
| 100,00      | 20.0000  |
| 200,00      | 40.0000  |

Magn uppskriftar (BOM) er 1 og framleiðslumagnið er 110. Formúla fyrir notkun er Úr röð (Magn) = Notkun. Þar sem framleiðslumagns er 110 fellur það í "Úr 100 röð." Þessvegna er magnið 20.



