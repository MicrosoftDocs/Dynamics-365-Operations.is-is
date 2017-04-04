---
title: "Reikna út efnisnotkunina"
description: "Þessi grein gefur upplýsingar um ýmsa valkosti sem tengjast útreikningi á efnisnotkun."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 2225707329c67a30d9234bef5282d49834ea042a
ms.lasthandoff: 03/31/2017


---

# <a name="calculate-material-consumption"></a>Reikna út efnisnotkunina

Þessi grein gefur upplýsingar um ýmsa valkosti sem tengjast útreikningi á efnisnotkun. 

eftirfarandi valkosti sem tengjast útreikningi á hráefnisnotkun eri tiltækir í **Uppsetningu** og **Skrefanotkun** flipana í á **Línuupplýsingar** flýtiflipa í **Uppskrift** síðu.

## <a name="variable-and-constant-consumption"></a>Breytileg og föst notkun
Í því **Notkun er** er hægt að velja hvort notkun er reiknaður sem fast magn eða breytileg. Velja **Fasti** ef fast magn eða rúmmál er nauðsynleg fyrir framleiðsluna, óháð því magni sem er framleitt. Velja **Breytilegt**, sem er sjálfgefna stillingin, sé áskilin upphæð efnis í fullbúnu vörunum í hlutfalli við fjölda fullbúnar vörur sem eru framleiddar.

## <a name="calculating-consumption-from-a-formula"></a>Formúla notuð við útreikning notkunar
Í **Formúlu** svæði er hægt að setja upp mismunandi formúlur til að reikna út efnisnotkunina. Ef nota á sjálfgefna gildið **Staðlaða**, notkun er ekki reiknað út frá formúlu. Eftirfarandi formúlur vinna ásamt **Hæð**, **Breidd**, **Dýpt**, **Þéttleiki**, og **Fast** svæði:

-   Hæð \*Fast
-   Hæð \*Breidd \*Fast
-   Hæð \*Breidd \*Dýpt \*Fast
-   (Hæð \*Breidd \*Dýpt / Þéttleiki) \*Fast

## <a name="rounding-up-and-multiples"></a>Sléttun og margfeldi
Saman leyfa reitirnir **Sléttun** og **Margfeldi** þér að slétta gildi efnisnotkunar . Til dæmis er hægt að slétta gildinu samkvæmt afgreiðslueiningu sem hráefni er tekin til fyrir framleiðslu. Eftirtaldir valkostir eru tiltækir í **Sléttun** svæði: **Magn**, **Mælingu**, og **Notkun**.

### <a name="quantity"></a>Magn

Ef **Magn** er valið sem sléttunar mekanismi, verður magn að vera margfeldi af tilgreindu magni. Til dæmis ef þörf er á heiltölum er **1** tilgreint í svæðinu **Margfeldi**. Tölur eru svo sléttað í magn sem má deila með 1.

### <a name="measurement"></a>Mæling

Yfirleitt, veljið **Mælingu** sem mekanisma sléttunar þegar hráefni kemur í ákveðnum stærðum. Til dæmis er stykki af 2 metra málmröri krafist fyrir fullbúin framleiðsluvara og málmrörið er geymt í 4.5 metra lengdum. Í þessu tilfelli má nota **Mælingu** mekanisma sléttunar til að reikna út hversu mörg málmrör þarf til að framleiða tiltekinn fjölda stykkja fullbúinnar framleiðsluvara. Til dæmis, í **Formúlu** er stillt á **Hæð \*Fasti**. Í **Hæð** er stillt á **2** til að tilgreina lengd tube sem er krafist fullbúin framleiðsluvara. Í **margfeldi** er stillt á **4.5** til að tilgreina í rör er tekið til í lengdir 4.5 metra. Útreikningurinn er:

1.  Fjöldi margfelda sem er krafist fyrir 10 stykki af fullbúin framleiðsluvara: 10 ÷ 2 = 5 stykki
2.  Samtals notkun:  4,5 × 5 = 22.5 metrar af málmröri

Gert er ráð fyrir að 0.5 metra af röri sé sett í rýrnun fyrir hver fimm stykki af rörum sem eru notaðar.

### <a name="consumption"></a>Notkun

Yfirleitt, veljið ** Notkun** sem mekanisma sléttunar þegar hráefni verður að vera tekið til í heilu magni tiltekinnar afgreiðslueiningar vöru. Til dæmis er 2 fjórðungar af málningu notaðir til að framleiða einu stykki hinnar fullbúnu framleiðsluvara, og málning er tekið til í 25 fjórðungsdollum. Í þessu tilfelli er hægt að nota **Notkun** mekanisma sléttunar til að slétta notkun á heilar tölur fyrir 25 fjórðungsdollum. Hér er útreikningur fyrir magn málningar sem er krafist ef framleiða þarf 180 stykki fullbúinnar framleiðsluvara:

1.  Málning þarf án rýrnunar: 180 × 2 = 360 fjórðungar
2.  Fjöldi dósa: 360 ÷ 25 = 14.4 sem er sléttað að 15
3.  Málning sem þarf án rýrnunar: 15 × 25 = 375 fjórðungar

## <a name="step-consumption"></a>Skrefanotkun
Skrefanotkun er notuð til að reikna út fastanotkun í magntímabilum. Ef þú velur **Skrefanotkun** á **Formúlu** reit á flipanum **Uppsetning**, er hægt að bæta upplýsingar um skref á flipanum **Skrefanotkun**. Hægt er að setja upp fast notað magn í tímabilum fyrir framleitt magn. Til dæmis er skrefanotkun sett upp eins og sýnt er í eftirfarandi töflu.

| Frá-röð | Magn |
|-------------|----------|
| 0,00        | 10.0000  |
| 100,00      | 20.0000  |
| 200,00      | 40.0000  |

Magn uppskriftar (BOM) er 1 og framleiðslumagnið er 110. Formúla fyrir notkun er Úr röð (Magn) = Notkun. Þar sem framleiðslumagns er 110 fellur það í "Úr 100 röð." Þessvegna er magnið 20.


