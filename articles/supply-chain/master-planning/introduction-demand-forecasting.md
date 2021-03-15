---
title: Yfirlit eftirspurnarspár
description: Eftirspurnarspá er notuð til að spá fyrir um óháða eftirspurn úr sölupöntunum og háð eftirspurn á hvaða aftengingarpunkti sem er fyrir pantanir viðskiptavina. Lækkunarreglur aukinnar eftirspurnarspáar veita tilvalda lausn fyrir fjöldasérsnið.
author: roxanadiaconu
manager: tfehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27aa2b7a3d595fadfc1af969e45975e95322812f
ms.sourcegitcommit: 3895279cc5c1cf4826143d2ccb95ccceccb0a3c2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2021
ms.locfileid: "5081368"
---
# <a name="demand-forecasting-overview"></a>Yfirlit eftirspurnarspár

[!include [banner](../includes/banner.md)]

Eftirspurnarspá er notuð til að spá fyrir um óháða eftirspurn úr sölupöntunum og háð eftirspurn á hvaða aftengingarpunkti sem er fyrir pantanir viðskiptavina. Lækkunarreglur aukinnar eftirspurnarspáar veita tilvalda lausn fyrir fjöldasérsnið.

Til að mynda grunnlínuspá er yfirlit yfir sögulegar færslur sent í Microsoft Azure Machine Learning sem er hýst á Azure. Þar sem þessi þjónusta er ekki samnýtt á milli notenda, er auðvelt að breyta henni til að uppfylla sérstakar faglegar þarfir. Hægt er að nota Supply Chain Management til að sjá fyrir spána, leiðrétta spá og skoða afkastavísa (KPI) um nákvæmni eftirspurnarspár.

> [!NOTE]
> Microsoft Azure Machine Learning Studio (classic) er nauðsynlegt til að mynd spá með vélnámi. Frá og með janúar 2021 er hún í boði í Austur-Japan, Suður-miðhluta, Suðaustur-Asíu, vesturhluta Bandaríkjanna og Vestur-Evrópu. Uppfærðar upplýsingar um núverandi framboð má finna í [Azure-afurðir eftir svæðum.](https://azure.microsoft.com/global-infrastructure/services/?regions=all&products=machine-learning-studio)

## <a name="key-features-of-demand-forecasting"></a>Lykilaðgerðir eftirspurnarspár

Hér eru sumar aðal aðgerðir eftirspurnarspár:

- Úbúa tölfræðilega grunnlínuspá sem er byggð á sögulegum gögnum.
- Nota gagnvirkt safn spávídda.
- Sjá fyrir eftirspurnarmynstur, °fullvissu bil og leiðréttingar á spá.
- Heimila notkun á leiðréttu spánni í ferli áætlunargerðar.
- Fjarlægja frávik.
- Stofna mælingar nákvæmni eftirspurnarspár.

## <a name="major-themes-in-demand-forecasting"></a>Aðalþemu í eftirspurnarspá

Þrjú aðalþemu sem eru innleidd í°eftirspurnarspár:

- **Einingastig** – eftirspurnarspár eru°uppbyggðar úr einingum og auðvelt að skilgreina. Hægt er að kveikja og slökkva á virkninni með því að breyta skilgreiningarlyklinum á **Viðskipti** &gt; **Birgðaspá** &gt; **Eftirspurnarspár**.
- **Endurnýting stafla Microsoft** – Vélnám sem er nú hluti af Microsoft Cortana Greiningarsafni gerir kleift á fljótlegan og auðveldan hátt að stofna spágreiningartilraunir, svo sem eftirspurnaráætlunartilraunir, með því að nota°algoritma R eða Python forritunartungumál og einfalt draga-sleppa viðmót.
  - Hægt er að hlaða niður Eftirspurnarspátilraunum, breyta þeim til að uppfylla þínar viðskiptaþarfir, °gefa þau út sem vefþjónustu á Azure og nota þau°til að mynda eftirspurnarspár. Tilraunirnar eru tiltækar fyrir niðurhal ef áskrift að Supply Chain Management á skipulagningu framleiðslu hefur verið keypt fyrir notanda á fyrirtækissviði.
  - Hægt er að hlaða niður öllum fyrirliggjandi eftirspurnarspátilraunum úr [Cortana Greiningar Gallery](https://gallery.cortanaanalytics.com/). Aftur á móti, þar sem eftirspurnarspártilraunir eru sjálfkrafa samþættar Supply Chain Management, þurfa viðskiptavinir og samstarfsaðilar að beita samþættingu tilrauna sem þeir hlaða niður úr [Cortana-greiningasafni](https://gallery.cortanaanalytics.com/). Þess vegna eru tilraunir úr [Cortana Greiningar Gallery](https://gallery.cortanaanalytics.com/) ekki jafn einfaldar í notkun og Finance and Operations eftirspurnarspátilraunir. Það°þarf að breyta kóða á tilraununum þannig að þær nota forritunarviðmót (API) Finance and Operations forritsins.
  - Hægt er að stofna eigin tilraunir í Microsoft Azure Machine Learning Studio (hefðbundið), birta þær sem þjónustu á Azure og nota þær til að stofna eftirspurnarspár.
  - Ef ekki er krafist mikilla afkasta eða ef ekki þarf að vinna°mikið af gögnum er hægt að nota ókeypis Vélnáms Lag. Mælt er með að alltaf ræsa úr°þessu lagi,°sérstaklega°við innleiðingu og prófana áfanga. Ef°krafist er meiri afkasta og°viðbótar geymslu, hægt er að nota staðlaða lags Vél Nám. Þetta lag krefst Azure áskriftar og felur í sér auka kostnað. Nánari upplýsingar um verðlagningu Vélnáms er að finna í [Verðlagning vélnámsstúdíós](https://aka.ms/machine-learning-price-info).
- **Lækkun spár á hvaða aftengingarpunkti sem er** – Eftirspurnarspár byggir á þessari virkni, sem gerir kleift að spá bæði háðri og óháðri eftirspurn á hvaða aftengingarpunkti sem er.

## <a name="basic-flow-in-demand-forecasting"></a>Grunnflæði í eftirspurnarspá

Eftirfarandi skýringarmynd sýnir vinnsluflæði fyrir eftirspurnarspá.

[![inngangur skýringarmynd eftirspurnarspár](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Framleiðsla eftirspurnar hefst í Supply Chain Management. Sögulegum færslugögnum úr Supply Chain Management gagnagrunninum er safnað saman og fyllt inn í millistigsvistunartöflu. Þessi millistigvistunartafla er síðar færð í vélnámsþjónustu. Með því að framkvæma lágmarks sérsnið, er hægt að setja ýmsar gagnaveitur í millistigsvistunartöfluna Þessi millistigvistunartafla er síðar færð í vélnámsþjónustu. Með því að framkvæma lágmarks sérsnið, er hægt að setja ýmsar gagnaveitur í millistigsvistunartöfluna Gagnaveiturnar geta meðal annars verið Microsoft Excel skrár, skrár með kommuskiptum gildum (CSV) og gögn úr Microsoft Dynamics AX 2009 og Microsoft Dynamics AX 2012. Þess vegna er hægt að mynda eftirspurnarspár sem íhuga söguleg gögn sem dreifast á milli margra kerfa. Hins vegar aðalgögn eins og vörunúmer og°mælieiningar,°verður að vera það sama milli°mismunandi gagnagjafa.

Ef notaðar eru vélnámstilraunir fyrir eftirspurnarspár leita þær að því sem passar best milli°fimm tímaraðir spáaðferða til að reikna út grunnlínu spár. Færibreytur fyrir þessar spáaðferðir eru meðhöndlaðar í Supply Chain Management.

Spár, söguleg gögn og allar breytingar sem gerðar voru á eftirspurnarspám í fyrri ítrekunum eru svo tiltækar í Supply Chain Management.

Hægt er að nota Supply Chain Management til að sjá fyrir og breyta grunnlínuspám. Handvirkar leiðréttingar°þarf að heimila áður en hægt er að nota spár til að gera áætlanir.

## <a name="limitations"></a>Takmarkanir

Eftirspurnarspá er verkfæri sem auðveldar viðskiptavini í framleiðsluiðnaði að stofna°spáferli. Hún býður upp á grunnaðgerðir lausn eftirspurnarspár og er hönnuð þannig að auðvelt sé að víkka hana út. Eftirspurnarspá hentar hugsanlega ekki vel fyrir viðskiptavini í iðnaði eins og viðskipti, heildsölu, vöruhúsum, flutningi eða annars konar°fagþjónustu.

### <a name="demand-forecast-variant-conversion-limitation"></a>Takmörkun á umreikning afbrigðis eftirspurnarspár

Umreikningur afbrigðis mælieininga er ekki studdur að fullu þegar eftirspurnarspá er mynduð ef mælieiningar lagerbirgða eru aðrar en mælieingar eftirspurnarspár.

Myndun spáa (**Mælieiningar lagerbirgða > Mælieiningar eftirspurnarspár**) notar umreikning mælieininga afurðarinnar. Við hleðslu sögulegra gagna fyrir myndun eftirspurnarspár er umreikningur mælieininga afurðastigs alltaf notaður þegar verið er að umreikna úr mælieiningum birgðavirðis í mælieiningar eftirspurnarspár, jafnvel þótt breytingar séu skilgreindar á afbrigðisstigi.

Fyrsti hluti þess að heimila spár (**Mælieiningar eftirspurnarspár > Mælieiningar birgða**) notar umreikning mælieininga afurðarinnar. Annar hluti þess að heimila spár (**Mælieiningar birgða > Mælieiningar sölu**) notar umreikning mælieininga afbrigðis. Þegar mynduð eftirspurnarspá er heimiluð er umreikningnum í mælieingu birgðavirðis úr mælieiningu eftirspurnarspár lokið með því að nota umreikning mælieiningar afurðastigs. Á sama tíma mun umbreyting milli birgðaeininga og mælieininga sölu virða skilgreinda umreikninga fyrir afbrigðisstig.

Athugið að mælieining eftirspurnarspár þarf ekki að hafa neina sérstaka merkingu. Hægt er að skilgreina hana sem „einingu eftirspurnarspár“. Fyrir hverja afurð er hægt að skilgreina umbreytinguna sem 1:1 með mælieiningu birgða.

## <a name="additional-resources"></a>Frekari upplýsingar

[Uppsetning eftirspurnarspár](demand-forecasting-setup.md)

[Myndun tölfræðilegrar grunnlínuspár](generate-statistical-baseline-forecast.md)

[Gera handvirkar leiðréttingar á grunnlínuspánni](manual-adjustments-baseline-forecast.md)

[Leiðrétt spá heimiluð](authorize-adjusted-forecast.md)

[Eftirlit með nákvæmni spár](monitor-forecast-accuracy.md)

[Fjarlægja einfara úr sögulegum færslugögnum við útreikning á eftirspurnarspá](remove-historical-outliers-calculating-demand-forecast.md)

[Framlengja virkni eftirspurnarspár](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]