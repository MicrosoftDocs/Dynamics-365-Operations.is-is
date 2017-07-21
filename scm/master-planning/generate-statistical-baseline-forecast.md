---
title: "Myndun tölfræðilegrar grunnlínuspár"
description: "Þessi skrá veitir upplýsingar um þær færibreytur og síur sem eru notaðar við útreikning á eftirspurnarspá."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 93646e37ee511d433097bb284fccc73c230aee32
ms.contentlocale: is-is
ms.lasthandoff: 06/13/2017

---

# <a name="generate-a-statistical-baseline-forecast"></a>Myndun tölfræðilegrar grunnlínuspár

[!include[banner](../includes/banner.md)]


Þessi skrá veitir upplýsingar um þær færibreytur og síur sem eru notaðar við útreikning á eftirspurnarspá. 

Þegar grunnlínuspá er stofnuð, verður fyrst að tilgreina færibreytur og síur sem eru notaðar í útreikningi. Til dæmis er hægt að stofna grunnlínu spá mat eftirspurn samkvæmt færslugögn úr á síðastliðnu ári fyrir sérstakt fyrirtæki í komandi mánuði og fyrir valinn vöruflokk. 

Til að mynda eftirspurnarspá er farið í **Aðaláætlanagerð &gt; Spá &gt; Eftirspurnarspá &gt; Mynda tölfræðilega grunnlínuspá**. 

Hægt er að velja spáramma við myndun spár. Tiltæk gildi eru: Dagur, Vika og Mánuður. 

Fjöldi spáramma sem á að reikna út spána fyrir er stilltur á svæðinu **Spátími**. 

Þegar stjórnunarstefna spárinnar er stillt á **Afrita yfir sögulega eftirspurn**, er lokatími sögulegu tímamarkanna hunsaður. Kerfið afritar fjölda ramma sem tilgreindir eru á svæðinu **Spátími** yfir á eftirspurnarspána, frá dagsetningu sem er stillt á svæðinu **Frá dagsetningu** undir **Söguleg tímamörk**. Með því að afrita söguleg eftirspurn frá ákveðnni dagsetningu og áfram, geta framleiðslustjórar gert áætlun fyrir næsta fjórðung á tvo vegu:

-   Með því að afrita eftirspurn úr sama fjórðung síðasta árs.
-   Með því að afrita eftirspurn úr síðasta fjórðungi.

Til að hindra°misskilning í áætlunum um framleiðslu er hægt að frysta ákveðinn fjölda spáramma. Þetta númer er stillt á **Frysta tímamörk** svæði. Á síðunni **Leiðrétt eftirspurnarspá** eru reitirnir fyrir frysta aldursgreiningarramma óvirkir, til veita sjónræn vísbendingu um að ekki ætti að breyta þessum gildum. 

Upphafsdagsetning grunnlínu eftirspurnarspár þarf ekki að vera núgildandi dagsetning eða dagsetning í framtíðinni. Til að setja inn aðra upphafsdagsetningu, notið svæðið **Upphafsdagsetning grunnlínuspár - Upphafsdagsetning**. Til dæmis í. Júní, geta notendur útbúið spá næsta árs. Þar sem spáramma milli lok söguleg eftirspurn og upphafsdagsetning í grunnlíkanasafnið vantar, getur verið að spárnar séu ekki nákvæmar. Ef verið er að nota Microsoft Dynamics 365 for Finance and Operations eftirspurnarspáþjónustu eru fjórar leiðir til að fylla út það sem vantar inn. Hægt er að velja þá aðferð sem óskað er eftir með því að stilla MISSING\_VALUE\_SUBSTITUTION færibreytuna á síðunni **Færibreytur eftirspurnarspár**. 

**Upphafsdagsetning grunnlínuspár** - Svæðið **Frá dagsetningu** verður að vera stillt á upphaf í spáramma, til dæmis á sunnudag í Bandaríkjunum ef spáramminn er vikan. Kerfið leiðréttir sjálfkrafa **Upphafsdagsetning grunnlínuspár** - **Frá dagsetningu** svæði til að passa við upphaf í spáramma. 

Svæðið **Upphafsdagsetning grunnlínuspár** - **Frá dagsetningu** getur verið stillt á dagsetningu sem er liðin. Með öðrum orðum, er hægt að mynda eftirspurnarspár í fortíðinni. Þetta er gagnlegt þar sem hún gerir notendum kleift að aðlaga færibreytur þjónustuspár svo tölfræðileg spá mynduð í fortíðinni samsvari raunverulegri söguleg eftirspurn. Notendur geta haldið svo áfram að nota þessar stillingar færibreyta til að mynda tölfræðilega grunnlínuspá fram í tímann. 

Handvirkar leiðréttingar sem gerðar voru í fyrri ítrekanir eftirspurnarspár er hægt að nota sjálfvirkt á nýju grunnlínuspána ef gátlistinn **Flytja handvirkar leiðréttingar til eftirspurnarspá** er valinn. Handvirkar leiðréttingar er ekki bætt við grunnlínuspá ef gátreiturinn er hreinsaður, - en þeim er ekki eytt. Handvirkar leiðréttingar í spá er aðeins hægt að eyða við innflutning spárinnar, með því að hreinsa gátreitinn **Vista handvirkar leiðréttingar á grunnlínu eftirspurnarspár**. Handvirkar leiðréttingar eru vistaðar á heimildartíma. Þess vegna glatast breytingarnar ef notandi gerir handvirkar leiðréttingar á spá, en heimilar ekki spá aftur í Finance and Operations. Nánari upplýsingar um handvirkar leiðréttingar og hvernig þær virka, sjá [Að heimila leiðréttu spána](authorize-adjusted-forecast.md). 

Myndun eftirspurnarspár getur haft nafn og athugasemdir til að aðstoða notendur að greina spá sem hefur verið mynduð. Þessi gildi eru sýnileg í spámyndunarsögu á síðunni **Myndun tölfræðilegrar grunnlínuspár, saga**. 

Áætlunarhópa innan samstæðu, úthlutunarlykla vöru og öðrum síum er hægt að beita við myndun spár. Hægt er að nota þær til að bæta afköst eða skipta gögnum niður í viðráðanlega búta. Athugið hins vegar að eftirspurnarspár er ekki myndaðar fyrir meðlimir úthlutunarlykils vöru sem ekki er tengt við fjárhagsáætlunarflokkur innan samstæðu, jafnvel þótt úthlutunarlykil vöru er valið í fyrirspurninni. 

**Ábending**: Stundum fá notendur villur við myndun á eftirspurnarspá eða spámyndun er lokið með engum lotukladda. Þetta getur gerst vegna afgangsgagna í fyrirspurninni sem var áður notað fyrir myndun eftirspurnarspár. Til að laga þetta vandamál, smellið á **Velja** til að opna síðuna **Fyrirspurn** svo er smellt á **Endurstilla**, og síðan er grunnlínuspá endurgerð. 

Ef spá er ekki mynduð fyrir stórt safn af vörum en, til dæmis, fyrir eina vöru eða einn úthlutunarlykil vöru í einu, þá er hægt, til að ná betri afköstum, að velja gátreitinn **Nota stillingu til að biðja um svör** á flipanum **Aðaláætlanagerð - Uppsetning - Eftirspurnarspá** - **Færibreytur eftirspurnarspár - Azure vélnám**.

<a name="see-also"></a>Sjá einnig
--------

[Uppsetning eftirspurnarspár](demand-forecasting-setup.md)

[Gera handvirkar leiðréttingar á grunnlínuspánni](manual-adjustments-baseline-forecast.md)

[Heimila leiðrétta spá](authorize-adjusted-forecast.md)




