---
title: "Yfirlit eftirspurnarspár"
description: "Eftirspurnarspá er notuð til að spá fyrir um óháða eftirspurn úr sölupöntunum og háð eftirspurn á hvaða aftengingarpunkti sem er fyrir pantanir viðskiptavina. Stækkuð eftirspurnarspár lækkunarreglur í Microsoft Dynamics AX veita tilvalda lausn fyrir fjöldasérsnið."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 86f2f556d1b2d8711e7419b4e85904e297097380
ms.contentlocale: is-is
ms.lasthandoff: 04/25/2017


---

# <a name="demand-forecasting-overview"></a>Yfirlit eftirspurnarspár

[!include[banner](../includes/banner.md)]


Eftirspurnarspá er notuð til að spá fyrir um óháða eftirspurn úr sölupöntunum og háð eftirspurn á hvaða aftengingarpunkti sem er fyrir pantanir viðskiptavina. Stækkuð eftirspurnarspár lækkunarreglur í Microsoft Dynamics AX veita tilvalda lausn fyrir fjöldasérsnið.

Til að mynda grunnlínuspá, yfirlit yfir færslur eru sendar Microsoft Azure Námsvélarþjónusta sem er hýst á Azure. Þar sem þessi þjónusta er ekki samnýtt á milli notenda, er auðvelt að breyta henni til að uppfylla sérstakar faglegar þarfir. Hægt er að nota Dynamics 365 fyrir Operations til að sjá°fyrir spána, leiðrétta spá og skoða afkastavísa (KPI) um nákvæmni eftirspurnarspár.

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

-   **Einingastig** – eftirspurnarspár eru°uppbyggðar úr einingum og auðvelt að skilgreina. Hægt er að kveikja og slökkva á virkninni með því að breyta skilgreiningarlyklinum á **Viðskipti** &gt; **Birgðaspá** &gt; **Eftirspurnarspár**.
-   **Endurnýting stafla Microsoft**– Microsoft°ýtti úr vör vélnámssvæði í Febrúar 2015. Vélnám sem er nú hluti af Microsoft Cortana Greiningarsafni gerir kleift á fljótlegan og auðveldan hátt að stofna spágreiningartilraunir, svo sem eftirspurnaráætlunartilraunir, með því að nota°algoritma R eða Python forritunartungumál og einfalt draga-sleppa viðmót.
    -   Hægt er að hlaða niður Dynamics 365 for Operations Eftirspurnarspátilraunum, breyta þeim til að uppfylla þínar viðskiptaþarfir, °gefa þau út sem vefþjónustu á Azure og nota þau°til að mynda eftirspurnarspár. Tilraunirnar eru tiltækar fyrir niðurhal ef áskrift að Dynamics 365 for Operations á skipulagningu framleiðslu hefur verið keypt sem notandi á°fyrirtækissviði.
    -   Hægt er að hlaða niður öllum fyrirliggjandi eftirspurnarspátilraunum úr [Cortana Greiningar Gallery](https://gallery.cortanaanalytics.com/). Aftur á móti, þar sem Dynamics 365 fyrir Operations Eftirspurnarspátilraunir eru°sjálfkrafa samþættar Dynamics 365 for Operations, þurfa°viðskiptavinir og samstarfsaðilar að beita samþættingu°tilrauna sem þeir hlaða niður úr [Cortana Greiningar Gallery](https://gallery.cortanaanalytics.com/). Þess vegna eru tilraunir úr [Cortana Greiningar Gallery ](https://gallery.cortanaanalytics.com/) ekki jafn einfaldar í notkun og Dynamics 365 for Operations eftirspurnarspátilraunir. Það°þarf að breyta kóða á tilraununum þannig að þær nota forritunarviðmót (API) Dynamics 365 for Operations forritsins.
    -   Hægt er að stofna eigin°tilraunir í Microsoft Azure Vélnámsveri, birta þær sem þjónustu á Azure og nota þær til að stofna eftirspurnarspár.
    -   Ef ekki er krafist mikilla afkasta eða ef ekki þarf að vinna°mikið af gögnum er hægt að nota ókeypis Vélnáms Lag. Mælt er með að alltaf ræsa úr°þessu lagi,°sérstaklega°við innleiðingu og prófana áfanga. Ef°krafist er meiri afkasta og°viðbótar geymslu, hægt er að nota staðlaða lags Vél Nám. Þetta lag krefst Azure áskriftar og felur í sér auka kostnað. Sjá nánari upplýsingar um verðlagningu Vél Nám <http://aka.ms/machine-learning-price-info>.
-   **Lækkun spár á hvaða aftengingarpunkti sem er** – Eftirspurnarspár í Dynamics 365 for Operations byggir á þessari virkni, sem gerir kleift að spá bæði háðri og óháðri eftirspurn á hvaða aftengingarpunkti sem er.

## <a name="basic-flow-in-demand-forecasting"></a>Grunnflæði í eftirspurnarspá
Eftirfarandi skýringarmynd sýnir vinnsluflæði fyrir eftirspurnarspá. 

[![inngangur skýringarmynd eftirspurnarspár](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Myndun eftirspurnarspár hefst í Dynamics 365 for Operations. Söguleg færslugögn úr Dynamics 365 for Operations gagnagrunninum er safnað saman og fyllir millistigsvistunartöflu. Þessi millistigvistunartafla er síðar færð í vélnámsþjónustu. Með því að framkvæma lágmarks sérsnið, er hægt að setja ýmsar gagnaveitur í millistigsvistunartöfluna Þessi millistigvistunartafla er síðar færð í vélnámsþjónustu. Með því að framkvæma lágmarks sérsnið, er hægt að setja ýmsar gagnaveitur í millistigsvistunartöfluna Gagnaveiturnar geta meðal annars verið Microsoft°Excel skrár, skrár með kommuskiptum gildum (CSV) og gögn úr Microsoft Dynamics AX 2009 og Microsoft Dynamics AX 2012.  Þess vegna er hægt að mynda eftirspurnarspár sem íhuga söguleg gögn sem dreifast á milli margra kerfa. Hins vegar aðalgögn eins og vörunúmer og°mælieiningar,°verður að vera það sama milli°mismunandi gagnagjafa.

Ef notaðar°eru vélnámstilraunir fyrir eftirspurnarspár í Dynamics 365 for Operations leita þær að því sem passar best milli°fimm tímaraðir spáaðferða til að reikna út grunnlínu spár. Færibreytur fyrir þessar spáaðferðir eru meðhöndlaðar í Dynamics 365 for Operations. 

Spár,°söguleg gögn og allar breytingar sem gerðar voru á eftirspurnarspám í fyrri umferðum eru svo tiltæk í Dynamics 365 for Operations. 

Hægt er að nota Dynamics 365 for Operations til að sjá fyrir og breyta grunnlínuspám. Handvirkar leiðréttingar°þarf að heimila áður en hægt er að nota spár til að gera áætlanir.

## <a name="limitations"></a>Takmarkanir
Eftirspurnarspá í Dynamics 365 for Operations er verkfæri sem auðveldar viðskiptavini í framleiðsluiðnaði að stofna°spáferli. Hún býður upp á grunnaðgerðir lausn eftirspurnarspár og er hönnuð þannig að auðvelt sé að víkka hana út. Eftirspurnarspá hentar hugsanlega ekki vel fyrir viðskiptavini í iðnaði eins og smásölu, heildsölu, vöruhúsum, flutningi eða annars konar°fagþjónustu.

<a name="see-also"></a>Sjá einnig
--------

[Uppsetning eftirspurnarspár](demand-forecasting-setup.md)

[Mynda tölfræðilega grunnlínuspá](generate-statistical-baseline-forecast.md)

[Gera handvirkar leiðréttingar á grunnlínuspánni](manual-adjustments-baseline-forecast.md)

[Heimila leiðrétta spá](authorize-adjusted-forecast.md)

[Fylgjast með nákvæmni spár](monitor-forecast-accuracy.md)

[Fjarlægja frávik úr sögulegum færslugögn við útreikning á eftirspurnarspá](remove-historical-outliers-calculating-demand-forecast.md)




