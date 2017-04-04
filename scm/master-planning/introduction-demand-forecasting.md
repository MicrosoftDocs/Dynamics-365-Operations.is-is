---
title: "Yfirlit yfir eftirspurnarspár"
description: "Eftirspurnarspá er notuð til að spá fyrir um óháða eftirspurn úr sölupöntunum og háð eftirspurn á hvaða aftengingarpunkti sem er fyrir pantanir viðskiptavina. Stækkuð eftirspurnarspár lækkun reglur veita tilvalið lausn fyrir fjöldainngöngu sérsnið."
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
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 9152616b81e7873426f296376b5e57c94439379d
ms.lasthandoff: 03/31/2017


---

# <a name="demand-forecasting-overview"></a>Yfirlit yfir eftirspurnarspár

Eftirspurnarspá er notuð til að spá fyrir um óháða eftirspurn úr sölupöntunum og háð eftirspurn á hvaða aftengingarpunkti sem er fyrir pantanir viðskiptavina. Stækkuð eftirspurnarspár lækkun reglur veita tilvalið lausn fyrir fjöldainngöngu sérsnið.

Til að mynda grunnlínuspá, yfirlit yfir færslur eru sendar Microsoft Azure Námsvélarþjónusta sem er hýst á Azure. Þar sem þessi þjónusta er ekki samnýtt á milli notenda, er auðvelt að breyta henni til að uppfylla sérstakar faglegar þarfir. Hægt er að nota Dynamics 365 aðgerða til að spá visualize leiðrétta spá og skoða afkastavísar (Afkastavísa) um nákvæmni eftirspurnarspár.

## <a name="key-features-of-demand-forecasting"></a>Lykilaðgerðir eftirspurnarspár
Hér eru sumar aðal aðgerðir eftirspurnarspár:

-   Úbúa tölfræðilega grunnlínuspá sem er byggð á sögulegum gögnum.
-   Nota gagnvirkt safn spávídda.
-   Sjá fyrir eftirspurnarmynstur, °fullvissu bil og leiðréttingar á spá.
-   Heimila notkun á leiðréttu spánni í ferli áætlunargerðar.
-   Fjarlægja frávik.
-   Stofna mælingar nákvæmni eftirspurnarspár.

## <a name="major-themes-in-demand-forecasting"></a>Aðalþemu í eftirspurnarspá
Þrjú aðalþemu sem eru innleidd í°eftirspurnarspár:

-   **Einingastig** – eftirspurnarspár eru°uppbyggðar úr einingum og auðvelt að skilgreina. Hægt er að slökkva virkni í og út með því að breyta skilgreiningarlykillinn á **Viðskipti**&gt;**Birgðaspá**&gt;**eftirspurnarspár**.
-   **Endurnýtingu stafla Microsoft** – Microsoft ræstur Vél Nám svæðis í Febrúar 2015. Vél Nám sem er nú hluti af Microsoft Cortana Greiningar Suite gerir kleift að fljótlegt og auðvelt stofna predictive analysis experiments experiments eftirspurn mat, svo sem með algorithms Rannsókn eða Python forritun tungumálum og einfalda draga og sleppa viðmót.
    -   Hægt er að sækja Dynamics 365 fyrir Aðgerðir experiments Eftirspurnarspár, breyta þeim að uppfylla ykkar gefa þau út og vefþjónustu á Azure og nota þau til að mynda eftirspurnarspár. Experiments sem eru tiltækar fyrir niðurhalið ef verið er að kaupa Dynamics 365 fyrir Aðgerðir áskriftar fyrir skipuleggjandi framleiðslu sem notandi á enterprise.
    -   Hægt er að hlaða niður öllum fyrirliggjandi eftirspurnarspátilraunum úr [Cortana Greiningar Gallery](https://gallery.cortanaanalytics.com/). Meðan Dynamics 365 fyrir Aðgerðir experiments Eftirspurnarspár eru sjálfkrafa samþætta við Dynamics 365 fyrir Aðgerðir, viðskiptaaðilar og viðskiptavinir verða að meðhöndla samþætting experiments sem þeir sækja úr í [Cortana Greiningar Gallery](https://gallery.cortanaanalytics.com/). Þess vegna experiments úr á [Cortana Greiningar Gallery](https://gallery.cortanaanalytics.com/) ekki eru kostnaðarjafnaðar sem straightforward til Dynamics 365 Aðgerðir experiments Eftirspurnarspár. Verður að breyta kóða á experiments þannig að þeir nota Dynamics 365 Aðgerðir forrits forritun viðmót (API).
    -   Hægt er að stofna eigin°tilraunir í Microsoft Azure Vélnámsveri, birta þær sem þjónustu á Azure og nota þær til að stofna eftirspurnarspár.
    -   Ef ekki er krafist mikilla afkasta eða ef ekki þarf að vinna°mikið af gögnum er hægt að nota ókeypis Vélnáms Lag. Mælt er með að alltaf ræsa úr°þessu lagi,°sérstaklega°við innleiðingu og prófana áfanga. Ef°krafist er meiri afkasta og°viðbótar geymslu, hægt er að nota staðlaða lags Vél Nám. Þetta lag krefst Azure áskriftar og felur í sér auka kostnað. Sjá nánari upplýsingar um verðlagningu Vél Nám <http://aka.ms/machine-learning-price-info>.
-   **Lækkun hvenær decoupling spár** – Eftirspurnarspár í Dynamics 365 fyrir Aðgerðir sem byggja á þessa virkni, sem gerir kleift að bæði háð og óháð eftirspurn hvenær decoupling spár.

## <a name="basic-flow-in-demand-forecasting"></a>Grunnflæði í eftirspurnarspá
Eftirfarandi skýringarmynd sýnir vinnsluflæði fyrir eftirspurnarspá. 

[![eftirspurn eftirspurnarspár kynningu skýringarmynd](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Eftirspurnarspá myndun hefst í Dynamics 365 aðgerða. Söguleg færslugögn úr Dynamics 365 fyrir gagnagrunn hugbúnaðargögn Aðgerðir er safnað saman og fyllir stigtafla. Þessi sviðsetningatöflu er seinna millibúnaðarforriti Vél Nám þjónustu. Með því að framkvæma lágmarksréttindi sérsnið, getur plug mismunandi gagnagjafa í sviðsetningatöflunni. Gagnagjafa geta Microsoft Excel skrár skrár csv-(CSV) og gögn úr Microsoft Dynamics AX 2009 og Microsoft Dynamics AX 2012. Þess vegna er hægt að mynda eftirspurnarspár íhuga söguleg gögn sem er dreifast á milli margra kerfum. Hins vegar aðalgögn eins og vörunúmer og°mælieiningar,°verður að vera það sama milli°mismunandi gagnagjafa.

Ef Dynamics 365 nota Aðgerðir Vél Nám experiments Eftirspurnarspár fyrir þær leita bestu laga milli fimm tímaraðir spá aðferðir til að reikna út grunnlínu eftirspurnarspár. Færibreytur fyrir þessar eftirspurnarspár aðferðir eru meðhöndlaðar í Dynamics 365 aðgerða. 

Spár söguleg gögn og allar breytingar sem gerðar voru á eftirspurnarspár í fyrri ítrekanir tiltækir svo í Dynamics 365 aðgerða. 

Hægt er að nota Dynamics 365 aðgerða visualize og breyta grunnlínu spár. Handvirkar leiðréttingar°þarf að heimila áður en hægt er að nota spár til að gera áætlanir.

## <a name="limitations"></a>Takmarkanir
Eftirspurnarspá í Dynamics 365 aðgerða er verkfæri sem auðveldar viðskiptavini í framleiðsluumhverfi atvinnugrein stofna eftirspurnarspár ferli. Hún býður upp á grunnaðgerðir lausn eftirspurnarspár og er hannaður þannig að hægt sé að auka. Eftirspurnaráætlun spá hugsanlega ekki að besta blaðinu viðskiptavina í atvinnugreina svo smásölu, wholesale, vöruhús, flutning eða öðrum fagþjónusta.

<a name="see-also"></a>Sjá einnig
--------

[Demand forecasting setup](demand-forecasting-setup.md)

[Generating a statistical baseline forecast](generate-statistical-baseline-forecast.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)

[Monitoring forecast accuracy](monitor-forecast-accuracy.md)

[Remove outliers from historical transaction data when calculating a demand forecast](remove-historical-outliers-calculating-demand-forecast.md)


