---
title: Yfirlit eftirspurnarspár
description: Eftirspurnarspá er notuð til að spá fyrir um óháða eftirspurn úr sölupöntunum og háð eftirspurn á hvaða aftengingarpunkti sem er fyrir pantanir viðskiptavina. Lækkunarreglur aukinnar eftirspurnarspáar veita tilvalda lausn fyrir fjöldasérsnið.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b71fde2d1b56b237dec2a08d3bd27e8ba6c35fef
ms.sourcegitcommit: 574d4dda83dcab94728a3d35fc53ee7e2b90feb0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595547"
---
# <a name="demand-forecasting-overview"></a>Yfirlit eftirspurnarspár

[!include [banner](../includes/banner.md)]

Eftirspurnarspá er notuð til að spá fyrir um óháða eftirspurn úr sölupöntunum og háð eftirspurn á hvaða aftengingarpunkti sem er fyrir pantanir viðskiptavina. Lækkunarreglur aukinnar eftirspurnarspáar veita tilvalda lausn fyrir fjöldasérsnið.

Til að mynda grunnlínuspá, yfirlit yfir færslur eru sendar Microsoft Azure Námsvélarþjónusta sem er hýst á Azure. Þar sem þessi þjónusta er ekki samnýtt á milli notenda, er auðvelt að breyta henni til að uppfylla sérstakar faglegar þarfir. Hægt er að nota Finance and Operations til að sjá fyrir spána, leiðrétta spá og skoða afkastavísa (KPI) um nákvæmni eftirspurnarspár.

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
    -   Hægt er að hlaða niður eftirspurnarspátilraunum Finance and Operations, breyta þeim til að uppfylla þínar viðskiptaþarfir, gefa þær út sem vefþjónustu á Azure og nota þær til að mynda eftirspurnarspár. Tilraunirnar eru tiltækar fyrir niðurhal ef áskrift að Finance and Operations fyrir skipulagningu framleiðslu hefur verið keypt af notanda á fyrirtækissviði.
    -   Hægt er að hlaða niður öllum fyrirliggjandi eftirspurnarspátilraunum úr [Cortana Greiningar Gallery](https://gallery.cortanaanalytics.com/). Aftur á móti, þar sem eftirspurnarspártilraunir Finance andr Operations eru sjálfkrafa samþættar Finance and Operations, þurfa viðskiptavinir og samstarfsaðilar að beita samþættingu tilrauna sem þeir hlaða niður úr [Cortana-greiningasafni](https://gallery.cortanaanalytics.com/). Þess vegna eru tilraunir úr [Cortana-greiningarsafni](https://gallery.cortanaanalytics.com/) ekki jafneinfaldar í notkun og eftirspurnarspátilraunir Finance and Operations. Það þarf að breyta kóða á tilraununum þannig að þær noti forritunarviðmót (API) Finance and Operations.
    -   Hægt er að stofna eigin°tilraunir í Microsoft Azure Vélnámsveri, birta þær sem þjónustu á Azure og nota þær til að stofna eftirspurnarspár.
    -   Ef ekki er krafist mikilla afkasta eða ef ekki þarf að vinna°mikið af gögnum er hægt að nota ókeypis Vélnáms Lag. Mælt er með að alltaf ræsa úr°þessu lagi,°sérstaklega°við innleiðingu og prófana áfanga. Ef°krafist er meiri afkasta og°viðbótar geymslu, hægt er að nota staðlaða lags Vél Nám. Þetta lag krefst Azure áskriftar og felur í sér auka kostnað. Nánari upplýsingar um verðlagningu Vélnáms er að finna í [Verðlagning vélnámsstúdíós](https://aka.ms/machine-learning-price-info).
-   **Lækkun spár á hvaða aftengingarpunkti sem er** – Eftirspurnarspár í Finance and Operations byggja á þessari virkni, sem gerir kleift að spá bæði háðri og óháðri eftirspurn á hvaða aftengingarpunkti sem er.

## <a name="basic-flow-in-demand-forecasting"></a>Grunnflæði í eftirspurnarspá
Eftirfarandi skýringarmynd sýnir vinnsluflæði fyrir eftirspurnarspá. 

[![inngangur skýringarmynd eftirspurnarspár](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Myndun eftirspurnarspár hefst í Finance and Operations. Sögulegum færslugögnum úr Finance and Operations gagnagrunninum er safnað saman og fyllt inn í millistigsvistunartöflu. Þessi millistigvistunartafla er síðar færð í vélnámsþjónustu. Með því að framkvæma lágmarks sérsnið, er hægt að setja ýmsar gagnaveitur í millistigsvistunartöfluna Þessi millistigvistunartafla er síðar færð í vélnámsþjónustu. Með því að framkvæma lágmarks sérsnið, er hægt að setja ýmsar gagnaveitur í millistigsvistunartöfluna Gagnaveiturnar geta meðal annars verið Microsoft Excel skrár, skrár með kommuskiptum gildum (CSV) og gögn úr Microsoft Dynamics AX 2009 og Microsoft Dynamics AX 2012. Þess vegna er hægt að mynda eftirspurnarspár sem íhuga söguleg gögn sem dreifast á milli margra kerfa. Hins vegar aðalgögn eins og vörunúmer og°mælieiningar,°verður að vera það sama milli°mismunandi gagnagjafa.

Ef notaðar eru vélnámstilraunir fyrir eftirspurnarspár í Finance and Operations leita þær að því sem passar best milli fimm tímaraða spáaðferða til að reikna út grunnlínuspá. Færibreytur fyrir þessar spáaðferðir eru meðhöndlaðar í Finance and Operations. 

Spár, söguleg gögn og allar breytingar sem gerðar voru á eftirspurnarspám í fyrri ítrekunum eru svo tiltækar í Finance and Operations. 

Hægt er að nota Finance and Operations til að sjá fyrir og breyta grunnlínuspám. Handvirkar leiðréttingar°þarf að heimila áður en hægt er að nota spár til að gera áætlanir.

## <a name="limitations"></a>Takmarkanir
Eftirspurnarspá í Finance and Operations er verkfæri sem auðveldar viðskiptavini í framleiðsluiðnaði að stofna spáferli. Hún býður upp á grunnaðgerðir lausn eftirspurnarspár og er hönnuð þannig að auðvelt sé að víkka hana út. Eftirspurnarspá hentar hugsanlega ekki vel fyrir viðskiptavini í iðnaði eins og smásölu, heildsölu, vöruhúsum, flutningi eða annars konar°fagþjónustu.

<a name="additional-resources"></a>Frekari upplýsingar
--------

[Uppsetning eftirspurnarspár](demand-forecasting-setup.md)

[Mynda tölfræðilega grunnlínuspá](generate-statistical-baseline-forecast.md)

[Gera handvirkar leiðréttingar á grunnlínuspánni](manual-adjustments-baseline-forecast.md)

[Heimila leiðrétta spá](authorize-adjusted-forecast.md)

[Fylgjast með nákvæmni spár](monitor-forecast-accuracy.md)

[Fjarlægja frávik úr sögulegum færslugögn við útreikning á eftirspurnarspá](remove-historical-outliers-calculating-demand-forecast.md)

[Framlengja virkni eftirspurnarspár](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)



