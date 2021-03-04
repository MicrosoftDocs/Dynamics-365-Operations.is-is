---
title: Uppsetning eftirspurnarspár
description: Þetta efnisatriði lýsir uppsetningarverk sem þarf að framkvæma til að undirbúa eftirspurnarspár.
author: roxanadiaconu
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72653
ms.assetid: c5fa4b09-512d-4349-ac51-cc13da69a160
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6d0de588d54948d89f636cadeb66c3d9e6878015
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430577"
---
# <a name="demand-forecasting-setup"></a>Uppsetning eftirspurnarspár

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir uppsetningarverk sem þarf að framkvæma til að undirbúa eftirspurnarspár.  

Meðal þessara verka í uppsetningu er að setja upp eftirfarandi gögn og færibreytur:

## <a name="item-allocation-key"></a>Úthlutunarlykill vöru
eftirspurnarspá er reiknuð fyrir vöruna og víddir aðeins ef varan er hluti af úthlutunarlykil vöru. Þessi regla er notuð til að flokka saman mikinn fjölda af vörum, þannig að hægt er að stofna eftirspurnarspár fljótlegri hátt. Prósenta fyrir úthlutunarlykil vöru er hunsuð þegar eftirspurnarspár er mynduð. Spár eru stofnaðar á grundvelli söguleg gögn. 

Vara og víddir hennar verður að vera hluti af aðeins einum úthlutunarlykil vöru ef úthlutunarlykill vöru er notaður við stofnun spár. 

Til að bæta birgðahaldseining (SKU) við vöruúthlutunarlykil fara í **aðaláætlanagerð** &gt; **Uppsetningu** &gt; **eftirspurnarspár** &gt; **úthlutunarlykla Vöru**. Nota skal **Úthluta vörum** síðu til að úthluta vörum á úthlutunarlykil.

## <a name="intercompany-planning-groups"></a>Áætlunarhópar innan samstæðu
Eftirspurnarspá myndar spár milli fyrirtækja. Í Dynamics 365 Supply Chain Management, fyrirtæki sem eru áætluð saman eru flokkuð í einn áætlunarhóp innan samstæðunnar. Til að tilgreina, per fyrirtæki, hvaða úthlutunarlykil vöru eigi að taka til greina fyrir eftirspurnarspá, skal tengja úthlutunarlykill vöru við áætlunarflokk meðlims innan samstæðu í áætlunarflokki með því að fara í **aðaláætlanagerð** &gt; **Uppsetningu** &gt; **áætlunarflokkar innan Samstæðu**. 

Að sjálfgefnu, ef engin úthlutunarlykla vöru er úthlutað til aðila áætlanahóps, innan samstæðu, er eftirspurnarspá reiknuð fyrir allar vörur sem er úthlutað til allra úthlutunarlykla vöru frá öllum fyrirtækjum. Aukalegir Síunarvalkosti fyrir fyrirtæki og úthlutunarlykla vöru eru tiltækar í **Mynda tölfræðilega grunnlínuspá** síðu. 

Endurskoða vörufjölda sem á að spá fyrir. Óþarfa vörur gæti valdið aukinn kostnaði þegar þú notar Microsoft Azure Machine Learning.

## <a name="demand-forecasting-parameters"></a>Færibreytur eftirspurnarspár
Til að setja upp færibreytur spáa, Fara í **aðaláætlanagerð** &gt; **Uppsetning** &gt; **Færibreytur eftirspurnarspár** Þar sem eftirspurnarspár keyra þvert á milli fyrirtækja, er uppsetning altæk. Með öðrum orðum, gildur uppsetning um öll fyrirtækjum. 

Eftirspurnarspá myndar spá í magni. Þess vegna mælieining sem magn skal sýnt í vera tilgreint í á **eining eftirspurnarspár** svæði. Mælieiningin verður að vera einkvæmt, til að aðstoða við að tryggja að uppsöfnun og prósentudreifingu sé rökleg. Nánari upplýsingar um uppsöfnun og prósentudreifingu sjá [gera handvirkar Leiðréttingar á grunnlínuspá](manual-adjustments-baseline-forecast.md). Fyrir hverja mælieiningu sem er notað fyrir Birgðahaldseiningar sem eru hafðar með í eftirspurnarspá, skal ganga úr skugga um að það sé umreikningsreglu fyrir mælieininguna og almenna mælieiningu eftirspurnarspár. Þegar spármyndun er keyrð, er listi yfir vörur sem ekki hafa umreikning mælieiningar skráður, þannig að hægt er að leiðrétta uppsetningu auðveldlega. 

Eftirspurnarspá má nota til að spá bæði háð og óháð eftirspurn. Til dæmis, ef aðeins **sölupöntun** gátreitur er valinn og ef vörur sem teknar eru til greina fyrir eftirspurnarspá eru seldar vörur, reiknar kerfið óháða eftirspurn. Hins vegar er mikilvæg undiríhlutir bætt við úthlutunarlykla vöru og hafðar með í eftirspurnarspá. Í þessu tilfelli, ef **framleiðslulínu** gátreitur er valinn, er háð spá reiknuð. 

Tvær aðferðir eru við að stofna grunnlínuspá. Hægt er að nota spárlíkön yfir söguleg gögn eða einfaldlega er hægt að afrita yfir söguleg gögn til spárinnar. **myndunarstefna Spár** svæði gerir kleift að velja á milli þessara tveggja aðferða. Til að nota spárlíkön skal velja **Azure Machine Learning**. 

Með því að smella **Spávíddir** í vinstri rúðunni í **færibreytur Eftirspurnarspár** síðu, er einnig hægt að velja safn spávídda til að nota þegar sem eftirspurnarspá er mynduð. Spávídd gefur til kynna upplýsingastig sem skilgreind er fyrir spá. Fyrirtæki, svæði, og úthlutunarlykill vöru eru áskilið spávídd, en þú getur einnig myndað spár í vöruhús, birgðastaða, viðskiptavinaflokkur, viðskiptavinalykill, land/svæði, staða, og vara plús allar vöruvíddarstig. 

Hægt er að bæta spávíddir við lista yfir víddir sem eru notaðar fyrir eftirspurnarspár á hvaða tímapunkti. Einnig er Hægt að fjarlægja spávídd af listanum. Hins vegar tapast handvirkar leiðréttingar ef verið er að bæta við eða fjarlægja spárvídd. 

Ekki allar vörur haga sér á saman hátt úr sjónarhorn eftirspurnarspár. Hægt er að flokka líkar vörur í einni vöruúthlutunarlykill og hægt er að stilla færibreytur eins og færslugerðir og stillingar spáraðferðar á hvern úthlutunarlykil vöru. Smellt er á **úthlutunarlykla vöru** í vinstri rúðu í **færibreytur eftirspurnarspár** síðu. 

Til að búa til spá notar Supply Chain Management Machine Learning-vefþjónustu. Til að tengja við þjónustuna, verður að gefa upp eftirfarandi upplýsingar ef innskráningu er í Microsoft Azure Machine Learning Studio (hefðbundið):

-   API-lykill vefþjónustu (lykill forritunarviðmóts)
-   vefslóð endapunkts fyrir vefþjónustu
-   Heiti Azure-geymslureiknings
-   Lykill fyrir Azure-geymslureikning

> [!NOTE]
> Heiti og lykill fyrir Azure-geymslureikning eru nauðsynleg aðeisn ef þú notar sérsniðinn geymslureikning. Ef verslunarsvæðis á útgáfu er notuð, verður þú að hafa sérsniðinn geymslureikning í Azure, þannig að Machine Learning hafi aðgang að söguleg gögn. 

Til að stofna spár um eftirspurn, er hægt að virkja eigin þjónustu með því að nota Machine Learning Studio eða Supply Chain Management Eftirspurnarspártilraunir. Leiðbeiningar fyrir virkjun eftirspurnarspártilrauna Finance and Operations sem vefþjónustu eru tiltækar í Supply Chain Management. Á **Færibreytur eftirspurnarspár** síða, smellt er á **Azure Machine Learning** flipa.

## <a name="settings-for-the-demand-forecasting-machine-learning-service"></a>Stillingar fyrir námsvélaþjónustu eftirspurnarspár
Til að skoða færibreytur sem hægt er að skilgreina fyrir á Eftirspurnarspárþjónustu, er farið í **aðaláætlanagerð** &gt; **Uppsetningu** &gt; **eftirspurnarspár** &gt; **færibreytur reiknirita fyrir Spá**. Í **færibreytur reiknirita** fyrir Spá síðu birtist sjálfgefin gildi fyrir færibreyturnar. Hægt er að skrifa yfir þessar færibreytur á **færibreytur Eftirspurnarspár** síðu. Nota **Almennt** flipann til að skrifa yfir færibreytur altækt eða nota **úthlutunarlykla Vöru** flipa til að skrifa yfir færibreytur á hvern úthlutunarlykil vöru. Færibreytur sem er skrifað yfir fyrir vöruúthlutunarlykil hafa eingöngu áhrif á spár fyrir vörur sem eru tengd þeim úthlutunarlykil vöru.

### <a name="forecast-algorithm-parameters"></a>Færibreytur reiknirita fyrir spá

Á flipanum **Úthlutunarlyklar** er hægt að stilla **Færibreytur reiknirita fyrir spá** fyrir hvern úthlutunarlykil. Eftirtaldir valkostir eru í boði.
- **Prósentuhlutfall öryggisstigs**: Áreiðanleikabil samanstendur af sviði gilda sem virka sem áreiðanlegt mat fyrir eftirspurnarspána. Til dæmis gefur 95% áreiðanleikastig til kynna að það séu 5% líkur á að framtíðareftirspurnar falli utan sviðs áreiðanleikabils.
- **Þvinga árstíðabindingu**: Tilgreinir hvort neyða eigi líkanið til að nota ákveðna tegund árstíðabundnar. Á við einungis um ARIMA og ETS. Valkostir: AUTO (sjálfgefið), NONE, ADDITIVE, MULTIPLICATIVE.
- **Spárlíkan**: Valkostir: ARIMA, ETS, STL, ETS + ARIMA, ETS + STL, ALL. Til að velja besta líkanið skaltu velja **ALL**.
- **Hámarksfjöldi spáðra gilda**: Tilgreinir hámarksgildið sem á að nota fyrir spár. Snið: + 1E[n] eða föst tala.
- **Lágmarksfjöldi spáðra gilda**: Tilgreinir lágmarksgildið sem á að nota fyrir spár. Snið: -1E[n] eða föst tala.
- **Gildisskipti vantar**: Tilgreinir hvernig eyður í sögulegum gögnum eru fylltar. Valkostir: tölugildi, MEAN, PREVIOUS, INTERPOLATE LINEAR, INTERPOLATE POLYNOMIAL.
- **Umfang gildissviðs vantar**: Tilgreinir hvort gildisbreytingin eigi einungis við um gagnasvið sérhverrar uppskiptingareigindar eða fyrir allt gagnasafnið. Valkostir: GRANULARITY_ATTRIBUTE (sjálfgefið), GLOBAL.
- **Árstíðarbundin vísbending**: Fyrir árstíðabundin gögn, gefðu vísbendingu um spárlíkanið til að bæta nákvæmni spárinnar. Snið: heiltala tala, sem táknar fjölda ramma sem eftirspurnarmynstur endurtekur sig. Til dæmis skaltu slá inn „6“ fyrir gögn sem endurtaka sig á 6 mánaða fresti.
- **Prósentuhlutfall stærðar í prófunarsetti**: Hlutfall sögulegra gagna sem nota á sem prófunarsett fyrir útreikning á nákvæmni spár. 

<a name="additional-resources"></a>Frekari upplýsingar
--------

[Yfirlit eftirspurnarspár](introduction-demand-forecasting.md)

[Myndun tölfræðilegrar grunnlínuspár](generate-statistical-baseline-forecast.md)

[Gera handvirkar leiðréttingar á grunnlínuspánni](manual-adjustments-baseline-forecast.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]