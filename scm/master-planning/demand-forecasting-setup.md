---
title: "Uppsetning eftirspurnarspár"
description: "Þetta efnisatriði lýsir uppsetningarverk sem þarf að framkvæma til að undirbúa eftirspurnarspár."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72653
ms.assetid: c5fa4b09-512d-4349-ac51-cc13da69a160
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f629329f4f50bd7c8edcfd70641bace01a1c53aa
ms.lasthandoff: 03/31/2017


---

# <a name="demand-forecasting-setup"></a>Uppsetning eftirspurnarspár

Þetta efnisatriði lýsir uppsetningarverk sem þarf að framkvæma til að undirbúa eftirspurnarspár.  

Meðal þessara verka í uppsetningu er að setja upp eftirfarandi gögn og færibreytur:

## <a name="item-allocation-key"></a>Úthlutunarlykill vöru
eftirspurnarspá er reiknuð fyrir vöruna og víddir aðeins ef varan er hluti af úthlutunarlykil vöru. Þessi regla er tryggt mikill flokkur af vörum, þannig að hægt er að stofna eftirspurnarspár fljótlegri hátt. Vara lykill úthlutunarprósentu er hunsuð þegar eftirspurnarspár er mynduð. Spár eru stofnaðar á grundvelli söguleg gögn. 

Vara og víddir hennar verður að vera hluti af aðeins einum úthlutunarlykil vöru ef úthlutunarlykill vöru er notaður við stofnun spár. 

Til að bæta birgðahaldseining (SKU) vöruúthlutunarlykil fara **Aðalröðun áætlanagerð**&gt;**Uppsetningu**&gt;**eftirspurnarspár**&gt;**úthlutunarlykla Vöru**. Nota skal **Úthluta vörum** síðu til að úthluta vörum á úthlutunarlykil.

## <a name="intercompany-planning-groups"></a>Áætlunarhópar innan samstæðu
Eftirspurnarspá myndar spár milli fyrirtækja. Í Microsoft Dynamics 365 fyrir Aðgerðir, fyrirtæki sem eru áætlaðar saman eru flokkaðar í eina áætlunarhóp samstæðunnar. Tengja úthlutunarlykil vöru er tilgreint fyrir hvert fyrirtæki sem vöruúthlutunarlykla takmarkaðra fyrir eftirspurnarspá, í áætlanahóps innan samstæðunnar með því að **Aðalröðun áætlanagerð**&gt;**Uppsetningu**&gt;**fjárhagsáætlunarflokka innan Samstæðu**. 

Að sjálfgefnu ef engin úthlutunarlykla vöru er úthlutað til aðila áætlanahóps, innan samstæðu á eftirspurnarspá er reiknuð fyrir allar vörur sem eru úthlutaðar öllum úthlutunarlyklum vöru úr öllum Dynamics 365 fyrir fyrirtæki Aðgerðir. Aukalegir Síunarvalkosti fyrir fyrirtæki og úthlutunarlykla vöru eru tiltækar í **Mynda tölfræðilega grunnlínuspá** síðu. 

Endurskoða vörufjölda sem á að spá fyrir. Óþarfa vörur gæti valdið aukinn kostnaði þegar þú notar Microsoft Azure Machine Learning.

## <a name="demand-forecasting-parameters"></a>Færibreytur eftirspurnarspár
Til að setja upp færibreytur eftirspurnarspár, farið **Aðalröðun áætlanagerð**&gt;**Uppsetningu**&gt;**færibreytur Eftirspurnarspár**. Þar sem eftirspurnarspár keyra þvert á milli fyrirtækja, er uppsetning altæk. Með öðrum orðum, gildur uppsetning um öll fyrirtækjum. 

Eftirspurnarspá myndar spá í magni. Þess vegna mælieining sem magn skal sýnt í vera tilgreint í á **eining eftirspurnarspár** svæði. Mælieiningin verður að vera einkvæmt, til að aðstoða við að tryggja að uppsöfnun og prósentudreifingu sé rökleg. Nánari upplýsingar um uppsöfnun og prósentudreifingu sjá [gera handvirkar Leiðréttingar á grunnlínuspá](manual-adjustments-baseline-forecast.md). Fyrir hverja mælieiningu sem er notað fyrir Birgðahaldseiningar sem eru hafðar með í eftirspurnarspá, skal ganga úr skugga um að það sé umreikningsreglu fyrir mælieininguna og almenna mælieiningu eftirspurnarspár. Þegar spármyndun er keyrð, er listi yfir vörur sem ekki hafa umreikning mælieiningar skráður, þannig að hægt er að leiðrétta uppsetningu auðveldlega. 

Eftirspurnarspá má nota til að spá bæði háð og óháð eftirspurn. Til dæmis, ef aðeins **sölupöntun** gátreitur er valinn og ef vörur sem teknar eru til greina fyrir eftirspurnarspá eru seldar vörur, reiknar kerfið óháða eftirspurn. Hins vegar er mikilvæg undiríhlutir bætt við úthlutunarlykla vöru og hafðar með í eftirspurnarspá. Í þessu tilfelli, ef **framleiðslulínu** gátreitur er valinn, er háð spá reiknuð. 

Það eru tvær aðferðir til að stofna grunnlínuspá í Dynamics 365 fyrir Aðgerðir. Hægt er að nota spárlíkön yfir söguleg gögn eða einfaldlega er hægt að afrita yfir söguleg gögn til spárinnar. **myndunarstefna Spár** svæði gerir kleift að velja á milli þessara tveggja aðferða. til að nota spárlíkön skal Velja **Azure Machine Learning**. 

Með því að smella **Spávíddir** í vinstri rúðunni í **færibreytur Eftirspurnarspár** síðu, er einnig hægt að velja safn spávídda til að nota þegar sem eftirspurnarspá er mynduð. Spávídd gefur til kynna upplýsingastig sem skilgreind er fyrir spá. Fyrirtæki, svæði, og úthlutunarlykill vöru eru áskilið spávídd, en þú getur einnig myndað spár í  vöruhús, birgðastaða, viðskiptavinaflokkur, viðskiptavinalykill, land/svæði, staða, og vara plús allar vöruvíddarstig. 

Hægt er að bæta spávíddir við lista yfir víddir sem eru notaðar fyrir eftirspurnarspár á hvaða tímapunkti. Einnig er Hægt að fjarlægja spávídd af listanum. Hins vegar tapast handvirkar leiðréttingar ef verið er að bæta við eða fjarlægja spárvídd. 

Ekki allar vörur haga sér á saman hátt úr sjónarhorn eftirspurnarspár. Hægt er að flokka líkar vörur í einni vöruúthlutunarlykill og hægt er að stilla færibreytur eins og færslugerðir og stillingar spáraðferðar á hvern úthlutunarlykil vöru. Smellt er á **úthlutunarlykla vöru **í vinstri rúðu í **færibreytur eftirspurnarspár ** síðu. 

Til að búa til spá Dynamics 365 fyrir Aðgerðir sem notar vefþjónustu Vél Nám. Til að tengja við þjónustuna, gefa verður upp Dynamics 365 aðgerða eftirfarandi upplýsingar ef innskráning á Microsoft Azure Vél Nám Studio:

-   API-lykill vefþjónustu (lykill forritunarviðmóts)
-   vefslóð endapunkts fyrir vefþjónustu
-   Heiti Azure-geymslureiknings
-   Lykill fyrir Azure-geymslureikning

**Athugasemd** Heiti og lykill fyrir Azure-geymslureikning eru nauðsynleg aðeisn ef þú notar sérsniðinn geymslureikning. Ef útgáfu verslunarsvæðis á að virkja þarf reikning sérsniðna geymslu Azure, þannig að þjónustu Smásöluvélar Nám aðgang söguleg gögn. 

Stofna spár um eftirspurn, er hægt að virkja eigin þjónustu með því að nota Studio Nám Vél eða Dynamics 365 Aðgerðir experiments eftirspurnarspár. Leiðbeiningar fyrir virkjun Dynamics 365 fyrir Aðgerðir eftirspurnarspár experiments vefþjónustu sem eru tiltækar Dynamics 365 fyrir Aðgerðir. Á **Færibreytur eftirspurnarspár** síða, smellt er á **Azure Machine Learning** flipa.

## <a name="settings-for-the-dynamics-365-for-operations-demand-forecasting-machine-learning-service"></a>Stillingar fyrir Dynamics 365 aðgerða eftirspurnarspár þjónustu smásöluvélar nám eftirspurn
Til að skoða færibreytur sem hægt er að skilgreina fyrir Dynamics 365 fyrir Aðgerðir eftirspurn eftirspurnarspár þjónustu, er farið **Áætlanagerð**&gt;**Uppsetningu**&gt;**eftirspurnarspár**&gt;**færibreytur reiknirita fyrir Spá**. Í **færibreytur reiknirita fyrir Spá** síðu birtist sem sjálfgefin gildi fyrir færibreyturnar. Hægt er að skrifa yfir þessar færibreytur á í **færibreytur Eftirspurnarspár** síðu. Nota **Almennt** flipann til að skrifa yfir færibreytur altækt eða nota **úthlutunarlykla Vöru** flipa til að skrifa yfir færibreytur á hvern úthlutunarlykil vöru. Færibreytur sem er skrifað yfir fyrir vöruúthlutunarlykil hafa eingöngu áhrif á spár fyrir vörur sem eru tengd þeim úthlutunarlykil vöru.

<a name="see-also"></a>Sjá einnig
--------

[Introduction to demand forecasting](introduction-demand-forecasting.md)

[Generating a statistical baseline forecast](generate-statistical-baseline-forecast.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)


