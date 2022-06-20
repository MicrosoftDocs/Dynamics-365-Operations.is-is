---
title: Myndun tölfræðilegrar grunnlínuspár
description: Þessi skrá veitir upplýsingar um þær færibreytur og síur sem eru notaðar við útreikning á eftirspurnarspá.
author: t-benebo
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c45d763a1f3d199c91f3cf6181c22f4b8130fabc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844939"
---
# <a name="generate-a-statistical-baseline-forecast"></a>Myndun tölfræðilegrar grunnlínuspár

[!include [banner](../includes/banner.md)]

Þessi skrá veitir upplýsingar um þær færibreytur og síur sem eru notaðar við útreikning á eftirspurnarspá. 

Þegar grunnlínuspá er stofnuð, verður fyrst að tilgreina færibreytur og síur sem eru notaðar í útreikningi. Til dæmis er hægt að stofna grunnlínu spá mat eftirspurn samkvæmt færslugögn úr á síðastliðnu ári fyrir sérstakt fyrirtæki í komandi mánuði og fyrir valinn vöruflokk. 

Til að mynda eftirspurnarspá er farið í **Aðaláætlanagerð &gt; Spá &gt; Eftirspurnarspá &gt; Mynda tölfræðilega grunnlínuspá**. 

Hægt er að velja spáramma við myndun spár. Tiltæk gildi eru: Dagur, Vika og Mánuður. 

Fjöldi spáramma sem á að reikna út spána fyrir er stilltur á svæðinu **Spátími**. 

Þegar stjórnunarstefna spárinnar er stillt á **Afrita yfir sögulega eftirspurn**, er lokatími sögulegu tímamarkanna hunsaður. Kerfið afritar fjölda ramma sem tilgreindir eru á svæðinu **Spátími** yfir á eftirspurnarspána, frá dagsetningu sem er stillt á svæðinu **Frá dagsetningu** undir **Söguleg tímamörk**. Með því að afrita söguleg eftirspurn frá ákveðnni dagsetningu og áfram, geta framleiðslustjórar gert áætlun fyrir næsta fjórðung á tvo vegu:

-   Með því að afrita eftirspurn úr sama fjórðung síðasta árs.
-   Með því að afrita eftirspurn úr síðasta fjórðungi.

Til að hindra°misskilning í áætlunum um framleiðslu er hægt að frysta ákveðinn fjölda spáramma. Þetta númer er stillt á **Frysta tímamörk** svæði. Á síðunni **Leiðrétt eftirspurnarspá** eru reitirnir fyrir frysta aldursgreiningarramma óvirkir, til veita sjónræn vísbendingu um að ekki ætti að breyta þessum gildum. 

Upphafsdagsetning grunnlínu eftirspurnarspár þarf ekki að vera núgildandi dagsetning eða dagsetning í framtíðinni. Til að setja inn aðra upphafsdagsetningu, notið svæðið **Upphafsdagsetning grunnlínuspár - Upphafsdagsetning**. Til dæmis í. Júní, geta notendur útbúið spá næsta árs. Þar sem spáramma milli lok söguleg eftirspurn og upphafsdagsetning í grunnlíkanasafnið vantar, getur verið að spárnar séu ekki nákvæmar. Ef verið er að nota þjónustuna Eftirspurnarspár, eru fjórir möguleikar á því að fylla út það sem vantar inn. Hægt er að velja þá aðferð sem óskað er eftir með því að stilla MISSING\_VALUE\_SUBSTITUTION færibreytuna á síðunni **Færibreytur eftirspurnarspár**. 

> [!NOTE]
> Gildisskipti vantar virkar aðeins fyrir eyður í gögnum á milli upphafs- og lokadagsetninga sögulegra gagna. Það mun ekki fylla út gögn fyrir eða eftir síðasta efnislegagagnapunkt, það virkar aðeins sem framreikningur á milli núverandi raungagnapunkta. 

Reiturinn **Upphafsdagsetning grunnlínuspár** - **Frá dagsetningu** verður að vera stillt á upphaf í spáramma, til dæmis á sunnudag í Bandaríkjunum ef spáramminn er vikan. Kerfið leiðréttir sjálfkrafa **Upphafsdagsetning grunnlínuspár** - **Frá dagsetningu** svæði til að passa við upphaf í spáramma. 

Svæðið **Upphafsdagsetning grunnlínuspár** - **Frá dagsetningu** getur verið stillt á dagsetningu sem er liðin. Með öðrum orðum, er hægt að mynda eftirspurnarspár í fortíðinni. Þetta er gagnlegt þar sem hún gerir notendum kleift að stilla færibreytur þjónustuspár svo tölfræðileg spá mynduð í fortíðinni samsvari raunverulegri söguleg eftirspurn. Notendur geta haldið svo áfram að nota þessar stillingar færibreyta til að mynda tölfræðilega grunnlínuspá fram í tímann. 

Handvirkar leiðréttingar sem gerðar voru í fyrri ítrekunum eftirspurnarspár er hægt að nota sjálfvirkt á nýju grunnlínuspána ef gátlistinn **Flytja handvirkar leiðréttingar til eftirspurnarsp** á er valinn. Handvirkar leiðréttingar er ekki bætt við grunnlínuspá ef gátreiturinn er hreinsaður, - en þeim er ekki eytt. Handvirkar leiðréttingar í spá er aðeins hægt að eyða við innflutning spárinnar, með því að hreinsa gátreitinn **Vista handvirkar leiðréttingar á grunnlínu eftirspurnarspár**. Handvirkar leiðréttingar eru vistaðar á heimildartíma. Þess vegna glatast breytingarnar ef notandi gerir handvirkar leiðréttingar á spá, en heimilar ekki spá aftur í Supply Chain Management. Nánari upplýsingar um handvirkar leiðréttingar og hvernig þær virka, sjá [Heimila leiðrétta spá](authorize-adjusted-forecast.md). 

Myndun eftirspurnarspár getur haft nafn og athugasemdir til að aðstoða notendur að greina spá sem hefur verið mynduð. Þessi gildi eru sýnileg í spámyndunarsögu á síðunni **Myndun tölfræðilegrar grunnlínuspár, saga**. 

Áætlunarhópa innan samstæðu, úthlutunarlykla vöru og öðrum síum er hægt að beita við myndun spár. Hægt er að nota þær til að bæta afköst eða skipta gögnum niður í viðráðanlega búta. Athugið hins vegar að eftirspurnarspár er ekki myndaðar fyrir meðlimir úthlutunarlykils vöru sem ekki er tengt við fjárhagsáætlunarflokkur innan samstæðu, jafnvel þótt úthlutunarlykil vöru er valið í fyrirspurninni. 

> [!TIP]
> Stundum fá notendur villur við myndun á eftirspurnarspá eða spámyndun er lokið með engum lotukladda. Þetta getur gerst vegna afgangsgagna í fyrirspurninni sem var áður notað fyrir myndun eftirspurnarspár. Til að leysa þetta vandamál smellirðu á **Velja** til að opna síðuna **Fyrirspurn**, velur **Endurstilla** og síðan endurstillirðu grunnlínuspána. 

Ef spá er ekki mynduð fyrir stórt safn af vörum en, til dæmis, fyrir eina vöru eða einn úthlutunarlykil vöru í einu, þá er hægt, til að ná betri afköstum, að velja gátreitinn **Nota stillingu til að biðja um svör** á flipanum **Aðaláætlanagerð - Uppsetning - Eftirspurnarspá** - **Færibreytur eftirspurnarspár - Azure vélnám**.

> [!NOTE]
> Hugsanlega flöt spá getur verið vegna sögulegra gagna sem þurfa að vera með lengri sögulegan tímaramma (að lágmarki 3 tímabil til að hægt sé að velja mynstur, eins og 3 ár með mánaðarlegri spá). Til að fá betri niðurstöður er hægt að prófa að breyta uppskiptingu tímabilsins eða auka tímabilið.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Uppsetning eftirspurnarspár](demand-forecasting-setup.md)

- [Gera handvirkar leiðréttingar á grunnlínuspánni](manual-adjustments-baseline-forecast.md)

- [Leiðrétt spá heimiluð](authorize-adjusted-forecast.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]