---
title: "Mynda tölfræðilega grunnlínuspá"
description: "Þessi skrá veitir upplýsingar um þær færibreytur og síur sem eru notaðar við útreikning á eftirspurnarspá."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c0c918b94fe96d123bb6c25c42fe168a026cd8a9
ms.lasthandoff: 03/31/2017


---

# <a name="generate-a-statistical-baseline-forecast"></a>Mynda tölfræðilega grunnlínuspá

Þessi skrá veitir upplýsingar um þær færibreytur og síur sem eru notaðar við útreikning á eftirspurnarspá. 

Þegar grunnlínuspá er stofnuð, verður fyrst að tilgreina færibreytur og síur sem eru notaðar í útreikningi. Til dæmis er hægt að stofna grunnlínu spá mat eftirspurn samkvæmt færslugögn úr á síðastliðnu ári fyrir sérstakt fyrirtæki í komandi mánuði og fyrir valinn vöruflokk. 

Til að mynda á eftirspurnarspá, farið **Aðalröðun áætlanagerð &gt;Eftirspurnarspár &gt;eftirspurnarspár &gt;Mynda tölfræðilega grunnlínuspá**. 

Hægt er að velja spáramma við myndun spár. Tiltæk gildi eru: Dagur, Vika og Mánuður. 

Fjöldi spáramma sem á að reikna út spána fyrir er stilltur á svæðinu** Spátími**. 

Þegar stjórnunarstefna spárinnar er stillt á **Afrita yfir sögulega eftirspurn**, er lokatími sögulegu tímamarkanna hunsaður. Kerfið afritar fjölda aldursgreiningarramma sem er tilgreind í í **tímaflöt Spár** spár eftirspurn, frá dagsetningu sett í svæðið við **Upphafsdagsetning** svæðinu undir **Sögulegu tímamarkanna**. Með því að afrita söguleg eftirspurn frá ákveðnni dagsetningu og áfram, geta framleiðslustjórar gert áætlun fyrir næsta fjórðung á tvo vegu:

-   Með því að afrita eftirspurn úr sama fjórðung síðasta árs.
-   Með því að afrita eftirspurn úr síðasta fjórðungi.

Til að hindra°misskilning í áætlunum um framleiðslu er hægt að frysta ákveðinn fjölda spáramma. Þetta númer er stillt á **Frysta tímamörk** svæði. Á síðunni **Leiðrétt eftirspurnarspá **eru reitirnir fyrir frysta aldursgreiningarramma óvirkir, til veita sjónræn vísbendingu um að ekki ætti að breyta þessum gildum. 

Upphafsdagsetning grunnlínu eftirspurnarspár þarf ekki að vera núgildandi dagsetning eða dagsetning í framtíðinni. Til að setja inn aðra upphafsdagsetningu, notið svæðið **Upphafsdagsetning grunnlínuspár - Upphafsdagsetning**. Til dæmis í. Júní, geta notendur útbúið spá næsta árs. Þar sem spáramma milli lok söguleg eftirspurn og upphafsdagsetning í grunnlíkanasafnið vantar, getur verið að spárnar séu ekki nákvæmar. Ef verið er að nota Microsoft Dynamics 365 fyrir Aðgerðir þjónusta Eftirspurnarspár eru fjórar sem hægt er að fylla út vantar göt vegu. Hægt er að velja þá aðferð sem óskað er með því að stilla það VANTAR\_GILDI\_færibreyta SKIPTI á á **færibreytur Eftirspurnarspár** síðu. 

Í **upphafsdagsetning grunnlínuspár** - **Frá dagsetningu** hefur svæði sé stillt á upphaf í spáramma, til dæmis í Bandaríkjunum er Sunnudegi sé eftirspurnarspár aldursgreiningarramma vikunnar. Kerfið leiðréttir sjálfkrafa í **upphafsdagsetning grunnlínuspár** - **Frá dagsetningu** svæði til að passa við upphaf í spáramma. 

Í **upphafsdagsetning grunnlínuspár** - **Frá dagsetningu** getur svæðið verið stillt á dagsetningu í fortíðinni. Með öðrum orðum, er hægt að mynda eftirspurnarspár í fortíðinni. Þetta er gagnlegt þar sem hún gerir notendum kleift að aðlaga færibreytur þjónustuspár svo tölfræðileg spá mynduð í fortíðinni samsvari raunverulegri söguleg eftirspurn. Notendur geta haldið svo áfram að nota þessar stillingar færibreyta til að mynda tölfræðilega grunnlínuspá fram í tímann. 

Handvirkar leiðréttingar sem gerðar voru í fyrri ítrekanir eftirspurnarspár er hægt að nota sjálfvirkt á nýju grunnlínuspána ef gátlistinn**Flytja handvirkar leiðréttingar til eftirspurnarspá** er valinn. Handvirkar leiðréttingar er ekki bætt við grunnlínuspá ef gátreiturinn er hreinsaður, - en þeim er ekki eytt. Handvirkar leiðréttingar í spá er aðeins hægt að eyða við innflutning spárinnar, með því að hreinsa gátreitinn **Vista handvirkar leiðréttingar á grunnlínu eftirspurnarspár**. Handvirkar leiðréttingar eru vistaðar á heimildartíma. Þess vegna ef notandi gerir handvirkar leiðréttingar á spá en ekki heimila spá aftur í Dynamics 365 aðgerða breytingarnar sem fyrir eru glatast. Nánari upplýsingar um handvirkar leiðréttingar og hvernig þeir vinna í [Heimilun leiðréttu spána](authorize-adjusted-forecast.md). 

Myndun eftirspurnarspár getur haft nafn og athugasemdir til að aðstoða notendur að greina spá sem hefur verið mynduð. Þessi gildi eru sýnileg í spámyndunarsögu á síðunni **Myndun tölfræðilegrar grunnlínuspár, saga**. 

Áætlunarhópa innan samstæðu, úthlutunarlykla vöru og öðrum síum er hægt að beita við myndun spár. Hægt er að nota þær til að bæta afköst eða skipta gögnum niður í viðráðanlega búta. Athugið hins vegar að eftirspurnarspár er ekki myndaðar fyrir meðlimir úthlutunarlykils vöru sem ekki er tengt við fjárhagsáætlunarflokkur innan samstæðu, jafnvel þótt úthlutunarlykil vöru er valið í fyrirspurninni. 

**Ábending**: Stundum fá notendur villur við myndun á eftirspurnarspá eða spámyndun er lokið með engum lotukladda. Þetta getur gerst vegna afgangsgagna í fyrirspurninni sem var áður notað fyrir myndun eftirspurnarspár. Til að laga þetta vandamál, smellið á **Velja** til að opna síðuna **Fyrirspurn** svo er smellt á **Endurstilla**, og síðan er grunnlínuspá endurgerð. 

Ef spá er ekki mynduð fyrir stóra safn vörur en, til dæmis, fyrir eina vöru eða úthlutunarlykil vöru í eina í einu, og svo til að ná betri afköstum, er hægt að velja á **Notkun beiðni svar ham** gátreitinn í **Sniðmát fjárhagsáætlunargerðar - Uppsetning - eftirspurnarspá** - **færibreytur - Azure Vél Nám Eftirspurnarspár** flipanum.

<a name="see-also"></a>Sjá einnig
--------

[Demand forecasting setup](demand-forecasting-setup.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)


