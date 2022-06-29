---
title: Uppsetning eftirspurnarspár
description: Þessi grein lýsir uppsetningarverkefnum sem þú verður að framkvæma til að undirbúa eftirspurnarspá.
author: t-benebo
ms.date: 11/23/2021
ms.topic: article
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fae2ac53dec8696075e7506d979c1cf9fb277af5
ms.sourcegitcommit: d98ecbd9457197ec8f8e281f9c2f24dcce7b8269
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/14/2022
ms.locfileid: "8960155"
---
# <a name="demand-forecasting-setup"></a>Uppsetning eftirspurnarspár

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig á að setja upp eftirspurnarspá.  

## <a name="item-allocation-keys"></a>Úthlutunarlyklar vöru

Vöruúthlutunarlyklar stofna vöruflokka. eftirspurnarspá er reiknuð fyrir vöruna og víddir aðeins ef varan er hluti af úthlutunarlykil vöru. Þessari reglu er framfylgt til að flokka mikinn fjölda vara svo hægt sé að búa til eftirspurnarspár hraðar. Spár eru stofnaðar á grundvelli söguleg gögn.

Vara og víddir hennar verður að vera hluti af aðeins einum úthlutunarlykil vöru ef úthlutunarlykill vöru er notaður við stofnun spár.

Til að búa til vöruúthlutunarlykla og bæta birgðahaldseiningu (SKU) við þá skaltu fylgja þessum skrefum.

1. Farðu í **Aðaláætlanagerð \> Uppsetning \> Eftirspurnarspá \> Úthlutunarlyklar vöru**.
1. Veldu annaðhvort vöruúthlutunarlykil á listaglugganum eða veldu **Nýtt** á aðgerðarrúðunni til að búa til nýjan. Á hausnum fyrir nýja eða valda lykilinn skaltu stilla eftirfarandi reiti:

    - **Vöruúthlutunarlykill** – Sláðu inn einstakt nafn fyrir lykilinn.
    - **Nafn** – Sláðu inn lýsandi heiti fyrir lykilinn.

1. Fylgdu einu af þessum skrefum til að bæta hlutum við valda vöruúthlutunarlykil eða fjarlægja hluti:

    - Á **Atriðaúthlutun** flýtiflipann, notaðu **Nýtt** og **Eyða** hnappa á tækjastikunni til að bæta við eða fjarlægja hluti eftir þörfum. Veldu vörunúmerið fyrir hverja línu og úthlutaðu síðan víddargildum í hinum dálkunum eftir þörfum. Veldu **Sýna stærðir** á tækjastikunni til að breyta setti víddardálka sem er sýndur í hnitanetinu. (Gildið í **Hlutfall** dálkurinn er hunsaður þegar eftirspurnarspár eru búnar til.)
    - Ef þú vilt bæta mörgum hlutum við takkann skaltu velja **Úthlutaðu hlutum** á aðgerðarrúðunni til að opna síðu þar sem þú getur fundið og úthlutað mörgum hlutum á valda takkann.

> [!IMPORTANT]
> Gættu þess að hafa aðeins viðeigandi atriði í hverjum vöruúthlutunarlykli. Óþarfa vörur gæti valdið aukinn kostnaði þegar þú notar Microsoft Azure Machine Learning.

## <a name="intercompany-planning-groups"></a>fjárhagsáætlunarflokkar innan samstæðu

Eftirspurnarspá getur búið til spár milli fyrirtækja. Í Dynamics 365 Supply Chain Management, fyrirtæki sem eru skipulögð saman eru flokkuð í sama áætlanahóp á milli fyrirtækja. Til að tilgreina, fyrir hvert fyrirtæki, hvaða vöruúthlutunarlyklar ættu að koma til greina við eftirspurnarspá, tengja vöruúthlutunarlykil við meðlim samstæðuáætlunarhópsins.

> [!IMPORTANT]
> Fínstilling áætlanagerðar styður ekki eins og er áætlunarhópar milli fyrirtækja. Til að gera áætlanagerð milli fyrirtækja sem notar áætlanagerð fínstillingu, settu upp aðalskipulagslotuvinnu sem innihalda aðaláætlanir fyrir öll viðkomandi fyrirtæki.

Fylgdu þessum skrefum til að setja upp áætlunarhópa milli fyrirtækja.

1. Fara til **Aðalskipulag \> Uppsetning \> Skipulagshópar milli fyrirtækja**.
1. Veldu annað hvort skipulagshóp í listaglugganum eða veldu **Nýtt** á aðgerðarrúðunni til að búa til nýjan. Á hausnum fyrir nýja eða valda hópinn skaltu stilla eftirfarandi reiti:

    - **Nafn** – Sláðu inn einstakt heiti fyrir skipulagshópinn.
    - **Lýsing** – Færið inn stutta lýsingu á skipulagshópnum.

1. Á **Meðlimir skipulagshóps milli fyrirtækja** Flýtiflipi, notaðu hnappana á tækjastikunni til að bæta við línu fyrir hvert fyrirtæki (lögaðila) sem ætti að vera hluti af hópnum. Fyrir hverja línu skal stilla eftirfarandi reiti:

    - **Lögaðili** – Veldu nafn fyrirtækis (lögaðila) sem er aðili að völdum hópi.
    - **Tímasetningarröð** – Úthlutaðu röðinni sem fyrirtækið á að vinna í miðað við önnur fyrirtæki. Lág gildi eru unnin fyrst. Þessi röð getur verið mikilvæg þegar eftirspurn eftir einu fyrirtæki hefur áhrif á önnur fyrirtæki. Í þessum tilfellum ætti fyrirtækið sem sinnir eftirspurninni að afgreiða síðast.
    - **Snilldaráætlun** – Veldu aðaláætlunina sem á að virkja fyrir núverandi fyrirtæki.
    - **Sjálfvirk afritun í kyrrstæða áætlun** – Veldu þennan gátreit til að afrita niðurstöðu áætlunarinnar í kyrrstæðu áætlunina.
    - **Sjálfvirk afritun í kraftmikla áætlun** – Veljið þennan gátreit til að afrita niðurstöðu áætlunarinnar í kviku áætlunina.

1. Að sjálfgefnu, ef engin úthlutunarlykla vöru er úthlutað til aðila áætlanahóps, innan samstæðu, er eftirspurnarspá reiknuð fyrir allar vörur sem er úthlutað til allra úthlutunarlykla vöru frá öllum fyrirtækjum. Viðbótar síunarvalkostir fyrir fyrirtæki og vöruúthlutunarlyklar eru fáanlegir í **Búðu til tölfræðilega grunnspá** svargluggi (**Aðalskipulag \> Spá \> Eftirspurnarspá \> Búðu til tölfræðilega grunnspá**). Til að úthluta vöruúthlutunarlyklum til fyrirtækis í völdum áætlunarhópi milli fyrirtækja, velurðu fyrirtækið og síðan á **Meðlimir skipulagshóps milli fyrirtækja** Flýtiflipi, veldu **Vöruúthlutunarlyklar** á tækjastikunni.

> [!IMPORTANT]
> Gættu þess að hafa aðeins viðeigandi vöruúthlutunarlykla í hverjum áætlunarhópi milli fyrirtækja. Óþarfa hlutir gætu valdið auknum kostnaði þegar þú notar Azure Machine Learning.

## <a name="set-up-demand-forecasting-parameters"></a><a name="parameters"></a> Settu upp færibreytur eftirspurnarspár

Nota **Eftirspurnarspábreytur** síðu til að setja upp nokkra valkosti sem stjórna því hvernig eftirspurnarspá mun virka í kerfinu þínu.

### <a name="open-the-demand-forecasting-parameters-page"></a>Opnaðu síðuna Færibreytur eftirspurnarspár

Til að setja upp færibreytur eftirspurnarspár, farðu í **Aðalskipulag \> Uppsetning \> Eftirspurnarspá \> Eftirspurnarspábreytur**. Þar sem eftirspurnarspár keyra þvert á milli fyrirtækja, er uppsetning altæk. Með öðrum orðum, það á við um alla lögaðila (fyrirtæki).

### <a name="general-settings"></a>Almennar stillingar

Nota **Almennt** flipi á **Eftirspurnarspábreytur** síðu til að skilgreina almennar stillingar fyrir eftirspurnarspá.

#### <a name="demand-forecast-unit"></a>Eining eftirspurnarspár

Eftirspurnarspá myndar spá í magni. Þess vegna mælieining sem magn skal sýnt í vera tilgreint í á **eining eftirspurnarspár** svæði. Þessi reitur skilgreinir eininguna sem verður notuð fyrir allar eftirspurnarspár, óháð venjulegum birgðaeiningum fyrir hverja vöru. Með því að nota samræmda spáeiningu hjálpar þú til við að tryggja að samansöfnun og prósentudreifing sé skynsamleg. Nánari upplýsingar um uppsöfnun og prósentudreifingu sjá [gera handvirkar Leiðréttingar á grunnlínuspá](manual-adjustments-baseline-forecast.md).

Fyrir hverja mælieiningu sem er notuð fyrir SKU sem eru innifalin í eftirspurnarspá skal ganga úr skugga um að það sé til umreikningsregla fyrir mælieininguna og almennu spá mælieininguna sem þú velur hér. Þegar þú býrð til spá er listi yfir hluti sem eru ekki með umreikning á mælieiningu skráður. Þess vegna geturðu auðveldlega lagað uppsetninguna. Fyrir frekari upplýsingar um mælieiningar og hvernig á að umreikna á milli þeirra, sjá [Stjórna mælieiningum](../pim/tasks/manage-unit-measure.md).

#### <a name="transaction-types"></a>Færslugerðir

Notaðu reitina á **Tegundir viðskipta** Flýtiflipi til að velja færslugerðir sem eru notaðar þegar tölfræðileg grunnspá er mynduð.

Hægt er að nota eftirspurnarspá til að spá fyrir um bæði háða eftirspurn og óháða eftirspurn. Til dæmis, ef aðeins **Sölupöntun** valkostur er stilltur á *Já*, og allir hlutir sem koma til greina við eftirspurnarspá eru hlutir sem eru seldir, kerfið reiknar út sjálfstæða eftirspurn. Hins vegar er mikilvæg undiríhlutir bætt við úthlutunarlykla vöru og hafðar með í eftirspurnarspá. Í þessu tilviki, ef **Framleiðslulína** valkostur er stilltur á *Já*, er reiknuð háð spá.

Þú getur hnekkt færslutegundum fyrir einn eða fleiri tiltekna vöruúthlutunarlykla með því að nota **Vöruúthlutunarlyklar** flipa. Sá flipi býður upp á svipaða reiti.

#### <a name="choose-how-to-create-the-baseline-forecast"></a>Veldu hvernig á að búa til grunnspá

The **Stefna til að búa til spár** reit gerir þér kleift að velja aðferðina sem er notuð til að búa til grunnspá. Þrjár aðferðir eru í boði:

- *Afrit yfir sögulega eftirspurn* - Búðu til spár með því að afrita bara söguleg gögn.
- *Azure Machine Learning Service* – Notaðu spálíkan sem notar Azure Machine Learning Service. Azure Machine Learning Service er núverandi vélanámslausn fyrir Azure. Þess vegna mælum við með því að þú notir það ef þú vilt nota spálíkan.
- *Azure Machine Learning* – Notaðu spálíkan sem notar Azure Machine Learning Studio (klassískt). Azure Machine Learning Studio (klassískt) hefur verið úrelt og verður brátt fjarlægt úr Azure. Þess vegna mælum við með því að þú veljir *Azure Machine Learning Service* ef þú ert að setja upp eftirspurnarspá í fyrsta skipti. Ef þú ert að nota Azure Machine Learning Studio (klassískt) ættir þú að ætla að skipta yfir í Azure Machine Learning Service eins fljótt og auðið er.

Hægt er að hnekkja spámyndunaraðferðinni fyrir einn eða fleiri tiltekna vöruúthlutunarlykla með því að nota **Vöruúthlutunarlyklar** flipa. Sá flipi býður upp á svipaða reiti.

#### <a name="override-default-forecast-algorithm-parameters-globally"></a>Hnekkja sjálfgefnum reikniritum spár á heimsvísu

Sjálfgefin reiknirit spár færibreytur og gildi eru úthlutað á **Eftirspurnarspábreytur** síða (**Aðalskipulag \> Uppsetning \> Eftirspurnarspá \> Eftirspurnarspábreytur**). Hins vegar geturðu hnekkt þeim á heimsvísu með því að nota **Færibreytur spár reiknirit** Flýtiflipi á **Almennt** flipi á **Eftirspurnarspábreytur** síðu. (Þú getur líka hnekið þeim fyrir sérstaka úthlutunarlykla með því að nota **Vöruúthlutunarlyklar** flipann á **Eftirspurnarspábreytur** síðu.)

Nota **Bæta við** og **Fjarlægja** hnappa á tækjastikunni til að koma á nauðsynlegu safni af hnekkingum á færibreytum. Fyrir hverja færibreytu á listanum skaltu velja gildi í **Nafn** reitnum og sláðu síðan inn viðeigandi gildi í **Gildi** sviði. Allar færibreytur sem eru ekki taldar upp hér munu taka gildi þeirra úr stillingunum á **Eftirspurnarspábreytur** síðu. Fyrir frekari upplýsingar um hvernig á að nota staðlað færibreytusett og velja gildi fyrir þær, sjáðu [Sjálfgefnar færibreytur og gildi fyrir eftirspurnarspárlíkön](#model-parameters) kafla.

### <a name="set-forecast-dimensions"></a>Stilltu spávíddir

Spávídd gefur til kynna upplýsingastig sem skilgreind er fyrir spá. Fyrirtæki, vefsvæði og vöruúthlutunarlykill eru nauðsynlegar spávíddir. Þú getur líka búið til spár á vöruhúsi, birgðastöðu, viðskiptavinaflokki, viðskiptavinareikningi, landi/svæði, ríki og/eða vörustigi og á öllum vöruvíddarstigum. Nota **Spámál** flipann á **Eftirspurnarspábreytur** síðu til að velja sett af spávíddum sem er notað þegar eftirspurnarspáin er búin til.

Hvenær sem er er hægt að bæta spávíddum við listann yfir víddir sem eru notaðar fyrir eftirspurnarspá. Einnig er Hægt að fjarlægja spávídd af listanum. Hins vegar tapast handvirkar leiðréttingar ef verið er að bæta við eða fjarlægja spárvídd.

### <a name="set-up-overrides-for-specific-item-allocation-keys"></a>Setja upp hnekkingar fyrir tiltekna vöruúthlutunarlykla

Ekki virka allir hlutir á sama hátt frá sjónarhóli eftirspurnarspár. Þess vegna er hægt að koma á sértækum úthlutunarlyklum fyrir flestar stillingar sem eru skilgreindar á **Almennt** flipa. Undantekningin er eftirspurnarspáeiningin. Til að setja upp hnekkingar fyrir tiltekinn vöruúthlutunarlykil skaltu fylgja þessum skrefum.

1. Á **Eftirspurnarspábreytur** síðu, á **Vöruúthlutunarlyklar** flipanum, notaðu hnappastikuna til að bæta úthlutunarlyklum hluta við hnitanetið vinstra megin, eða fjarlægja þá, eins og þú þarft. Veldu síðan úthlutunarlykilinn sem þú vilt setja upp hnekkingar fyrir.
1. Á **Tegundir viðskipta** Flýtiflipi, virkjaðu þær tegundir færslu sem þú vilt nota til að búa til tölfræðilega grunnspá fyrir vörur sem tilheyra völdum úthlutunarlykli. Stillingarnar virka alveg eins og þær virka á **Almennt** flipa, en þeir eiga aðeins við um valinn vöruúthlutunarlykil. Allar stillingar hér (bæði *Já* gildi og *Nei* gildi) hnekkja öllum **Tegundir viðskipta** stillingar á **Almennt** flipa.
1. Á **Færibreytur spár reiknirit** Flýtiflipi, veldu spáframleiðslustefnu og hnekkingar færibreytu spáalgríms fyrir vörur sem tilheyra völdum úthlutunarlykli. Þessar stillingar virka alveg eins og þær virka á **Almennt** flipa, en þeir eiga aðeins við um valinn vöruúthlutunarlykil. Nota **Bæta við** og **Fjarlægja** hnappa á tækjastikunni til að skilgreina nauðsynlegt safn af hnekkingum á færibreytum. Fyrir hverja færibreytu á listanum skaltu velja gildi í **Nafn** reitnum og sláðu síðan inn viðeigandi gildi í **Gildi** sviði. Fyrir frekari upplýsingar um hvernig á að nota staðlað færibreytusett og velja gildi fyrir þær, sjáðu [Sjálfgefnar færibreytur og gildi fyrir eftirspurnarspárlíkön](#model-parameters) kafla.

### <a name="set-up-the-connection-to-the-azure-machine-learning-service"></a>Settu upp tenginguna við Azure Machine Learning Service

Nota **Azure Machine Learning Service** flipann til að setja upp tenginguna við Azure Machine Learning Service. Þessi lausn er einn af valkostunum til að búa til grunnspána. Þessar stillingar á þessum flipa hafa aðeins áhrif þegar **Stefna til að búa til spár** reiturinn er stilltur á *Azure Machine Learning Service*.

Fyrir frekari upplýsingar um hvernig á að setja upp Azure Machine Learning Service og nota síðan stillingarnar hér til að tengjast henni, sjáðu [Settu upp Azure Machine Learning Service](#setup-amls) kafla.

### <a name="set-up-the-connection-to-azure-machine-learning-studio-classic"></a>Settu upp tenginguna við Azure Machine Learning Studio (klassískt)

> [!IMPORTANT]
> Azure Machine Learning Studio (klassískt) hefur verið úrelt. Þess vegna geturðu ekki lengur búið til ný vinnusvæði fyrir það í Azure. Það hefur verið skipt út fyrir Azure Machine Learning Service, sem veitir svipaða virkni og fleira. Ef þú ert ekki þegar að nota Azure Machine Learning, ættir þú að byrja að nota Azure Machine Learning Service. Ef þú ert nú þegar með vinnusvæði sem var búið til fyrir Azure Machine Learning Studio (klassískt) geturðu haldið áfram að nota það þar til eiginleikinn er alveg fjarlægður úr Azure. Hins vegar mælum við með að þú uppfærir í Azure Machine Learning Service eins fljótt og auðið er. Þó að forritið haldi áfram að vara þig við því að Azure Machine Learning Studio (klassískt) hafi verið úrelt, mun spániðurstaðan ekki hafa áhrif. Fyrir frekari upplýsingar um nýju Azure Machine Learning Service og hvernig á að setja hana upp, sjáðu [Settu upp Azure Machine Learning Service](#setup-amls) kafla.
>
> Þú getur frjálslega skipt á milli þess að nota nýju og gömlu vélanámslausnirnar með Supply Chain Management svo lengi sem gamla Azure Machine Learning Studio (klassíska) vinnusvæðið þitt er tiltækt.

Ef þú ert nú þegar með tiltækt Azure Machine Learning Studio (klassískt) vinnusvæði geturðu notað það til að búa til spár með því að tengja það við Supply Chain Management. Þú getur komið á þessari tengingu með því að nota **Azure Machine Learning** flipann á **Eftirspurnarspábreytur** síðu. (Stillingarnar á þessum flipa hafa aðeins áhrif þegar **Stefna til að búa til spár** reiturinn er stilltur á *Azure Machine Learning* .) Sláðu inn eftirfarandi upplýsingar fyrir Azure Machine Learning Studio (klassískt) vinnusvæðið þitt:

- API-lykill vefþjónustu (lykill forritunarviðmóts)
- vefslóð endapunkts fyrir vefþjónustu
- Heiti Azure-geymslureiknings
- Lykill fyrir Azure-geymslureikning

> [!NOTE]
> Heiti og lykill fyrir Azure-geymslureikning eru nauðsynleg aðeisn ef þú notar sérsniðinn geymslureikning. Ef þú setur upp útgáfuna á staðnum, verður þú að hafa sérsniðinn geymslureikning í Azure, svo að vélanám hafi aðgang að söguleg gögnum.

## <a name="default-parameters-and-values-for-demand-forecasting-models"></a><a name="model-parameters"></a> Sjálfgefnar færibreytur og gildi fyrir eftirspurnarspárlíkön

Þegar þú notar vélanám til að búa til spááætlunarlíkön þín, stjórnar þú valmöguleikum vélanáms með því að stilla gildi fyrir *færibreytur spár reiknirit*. Þessi gildi eru send frá Supply Chain Management til Azure Machine Learning. Nota **Forspá reiknirit færibreytur** síðu til að stjórna hvaða tegundir gilda ætti að gefa upp og hvaða gildi hver ætti að hafa.

Til að setja upp sjálfgefnar færibreytur og gildi sem notuð eru fyrir eftirspurnarspárlíkön, farðu á **Aðalskipulag \> Uppsetning \> Eftirspurnarspá \> Forspá reiknirit færibreytur**. Staðlað sett af breytum er til staðar. Hver færibreyta hefur eftirfarandi reiti:

- **Nafn** – Heiti færibreytunnar, eins og það er notað af Azure. Venjulega ættir þú ekki að breyta þessu nafni nema þú hafir sérsniðið tilraunina í Azure Machine Learning.
- **Lýsing** – Algengt heiti fyrir færibreytuna. Þetta nafn er notað til að auðkenna færibreytuna á öðrum stöðum í kerfinu (til dæmis á **Eftirspurnarspábreytur** síðu).
- **Gildi** – Sjálfgefið gildi fyrir færibreytuna. Gildið sem þú ættir að slá inn fer eftir færibreytunni sem þú ert að breyta. 
- **Skýring** – Stutt lýsing á færibreytunni og hvernig á að nota hana. Þessi lýsing inniheldur venjulega ráðleggingar um gild gildi fyrir **Gildi** sviði.

Eftirfarandi færibreytur eru sjálfgefnar. (Ef þú verður einhvern tíma að fara aftur í þennan staðlaða lista skaltu velja **Endurheimta** á aðgerðarrúðunni.)

- **Prósentuhlutfall öryggisstigs** – Áreiðanleikabil samanstendur af sviði gilda sem virka sem áreiðanlegt mat fyrir eftirspurnarspána. Til dæmis gefur 95% áreiðanleikastig til kynna að það séu 5% líkur á að framtíðareftirspurnar falli utan sviðs áreiðanleikabils.
- **Þvingaðu fram árstíðarsveiflu** – Tilgreinir hvort neyða eigi líkanið til að nota ákveðna tegund árstíðabundins. Þessi færibreyta á aðeins við um ARIMA og ETS. Valkostir: *AUTO (sjálfgefið)*, *·*, *·*, *·*.
- **Spálíkan** – Tilgreinir hvaða spálíkan á að nota. Valkostir: *ARIMA*, *·*, *·*, *+ARIMA*, *+STL*, *·*. Til að velja fyrirmynd sem hentar best, notaðu *ALLT*.
- **Hámarksfjöldi spáðra gilda** – Tilgreinir hámarksgildið sem á að nota fyrir spár. Snið: + 1E [n] eða föst tala.
- **Lágmarksfjöldi spáðra gilda** – Tilgreinir lágmarksgildið sem á að nota fyrir spár. Snið: - 1E [n] eða föst tala.
- **Gildisskipti vantar** – Tilgreinir hvernig eyður í sögulegum gögnum eru fylltar. Valkostir: *(tölugildi)*, *·*, *·*, *LÍNÆG*, *·*.
- **Umfang gildissviðs vantar** – Tilgreinir hvort gildisbreytingin eigi einungis við um dagsetningasvið sérhverrar uppskiptingareigindar eða fyrir allt gagnasafnið. Eftirfarandi valkostir eru í boði til að setja á dagsetningabilið sem kerfið notar þegar fyllt er upp í bil í sögulegum gögnum:

    - *ALÞJÓÐLEGT* – Kerfið notar allt svið dagsetninga allra granularity eiginleika.
    - *HISTORY_DATE_RANGE* – Kerfið notar ákveðið dagsetningarbil sem er skilgreint af **Frá dags** og **Til dagsins í dag** sviðum í **Sögulegur sjóndeildarhringur** kafla í **Búðu til tölfræðilega grunnspá** valmynd.
    - *GRANULARITY_ATTRIBUTE* – Kerfið notar dagsetningarbil kornunareiginarinnar sem nú er unnin.

    > [!NOTE]
    > Eigind uppskiptingar er samsetning spávídda sem er notuð við gerð spár. Hægt er að skilgreina spávíddir á síðunni **Færibreytur eftirspurnarspár**.

- **Árstíðarbundin vísbending** – Fyrir árstíðabundin gögn, gefðu vísbendingu um spárlíkanið til að bæta nákvæmni spárinnar. Snið: heiltala sem táknar fjölda fötu sem eftirspurnarmynstur endurtekur sig fyrir. Til dæmis, slá inn *6* fyrir gögn sem endurtaka sig á sex mánaða fresti.
- **Prósentuhlutfall stærðar í prófunarsetti** – Hlutfall sögulegra gagna sem nota á sem prófunarsett fyrir útreikning á nákvæmni spár.

Þú getur hnekkt gildunum fyrir þessar færibreytur með því að fara í **Aðalskipulag \> Uppsetning \> Eftirspurnarspá \> Eftirspurnarspábreytur**. Á **Eftirspurnarspábreytur** síðu geturðu hnekið breytunum á eftirfarandi hátt:

- Nota **Almennt** flipa til að hnekkja færibreytum á heimsvísu.
- Nota **Vöruúthlutunarlyklar** flipa til að hnekkja færibreytum fyrir tiltekna vöruúthlutunarlykla. Færibreytur sem eru hnekkt fyrir tiltekinn vöruúthlutunarlykil hafa aðeins áhrif á spá um vörur sem tengjast þeim vöruúthlutunarlykli.

> [!NOTE]
> Á **Færibreytur spár reiknirit** síðu geturðu notað hnappana á aðgerðarrúðunni til að bæta breytum við listann eða fjarlægja færibreytur af listanum. Hins vegar ættir þú venjulega ekki að nota þessa nálgun nema þú hafir sérsniðið tilraunina í Azure Machine Learning.

## <a name="set-up-the-azure-machine-learning-service"></a><a name="setup-amls"></a> Settu upp Azure Machine Learning Service

Supply Chain Management reiknar út eftirspurnarspár með því að nota Azure Machine Learning Service, sem þú verður að setja upp og keyra á þinni eigin Azure áskrift. Þessi hluti lýsir því hvernig á að setja upp Azure Machine Learning Service í Azure og tengja hana síðan við Supply Chain Management umhverfið þitt.

### <a name="enable-the-azure-machine-learning-service-in-feature-management"></a>Virkjaðu Azure Machine Learning Service í eiginleikastjórnun

Áður en þú getur notað Azure Machine Learning Service fyrir eftirspurnarspá verður þú að kveikja á eiginleika í Supply Chain Management til að virkja samþættinguna. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Aðaláætlanagerð*
- **Eiginleikaheiti:** *Azure Machine Learning Service fyrir eftirspurnarspá*

### <a name="set-up-machine-learning-in-azure"></a><a name="ml-workspace"></a> Settu upp vélanám í Azure

Til að gera Azure kleift að nota vélanám til að vinna úr spám þínum, verður þú að setja upp Azure vélnámsvinnusvæði í þessum tilgangi. Þú hefur tvo valkosti:

- Til að setja upp vinnusvæðið með því að keyra skriftu sem er útvegað af Microsoft skaltu fylgja leiðbeiningunum í [Valkostur 1: Keyra skriftu til að setja sjálfkrafa upp vinnusvæðið þitt fyrir vélanám](#ml-workspace-script) kafla, og slepptu síðan áfram í [Settu upp tengingarfæribreytur Azure Machine Learning Service í Supply Chain Management](#demand-forecast-parameters) kafla.
- Til að setja upp vinnusvæðið þitt handvirkt skaltu fylgja leiðbeiningunum í [Valkostur 2: Settu upp vinnusvæðið fyrir vélanám handvirkt](#ml-workspace-manual) kafla, og slepptu síðan áfram í [Settu upp tengingarfæribreytur Azure Machine Learning Service í Supply Chain Management](#demand-forecast-parameters) kafla. Þessi valkostur tekur lengri tíma, en hann gefur þér meiri stjórn.

#### <a name="option-1-run-a-script-to-automatically-set-up-your-machine-learning-workspace"></a><a name="ml-workspace-script"></a> Valkostur 1: Keyra skriftu til að setja sjálfkrafa upp vinnusvæðið þitt fyrir vélanám

Þessi hluti lýsir því hvernig á að setja upp vinnusvæðið fyrir vélanám með því að nota sjálfvirkt skriftu sem er útvegað af Microsoft. Ef þú vilt geturðu sett upp öll tilföng handvirkt með því að fylgja leiðbeiningunum í [Valkostur 2: Settu upp vinnusvæðið fyrir vélanám handvirkt](#ml-workspace-manual) kafla. Þú þarft ekki að klára báða valkostina.

1. Á GitHub, opnaðu [Sniðmát fyrir Dynamics 365 Supply Chain Management eftirspurnarspá með Azure Machine Learning](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service) repository (repo), og hlaðið niður eftirfarandi skrám:

    - quick_setup.ps1
    - sampleInput.csv
    - src/parameters.py
    - src/api_trigger.py
    - src/run.py
    - src/REntryScript/forecast.r

1. Opnaðu PowerShell glugga og keyrðu **quick_setup.ps1** forskrift sem þú hleður niður í fyrra skrefi. Fylgdu leiðbeiningunum á skjánum. Handritið mun setja upp nauðsynlegt vinnusvæði, geymslu, sjálfgefna gagnageymslu og tölvuauðlindir. Hins vegar verður þú samt að búa til nauðsynlegar leiðslur með því að fylgja skrefunum sem eftir eru af þessari aðferð. (Leiðslur bjóða upp á leið til að byrja að spá forskriftir frá Supply Chain Management.)
1. Hladdu upp í Azure Machine Learning Studio **sampleInput.csv** skrá sem þú hleður niður í skrefi 1 í gáminn sem er nefndur *demplan-azureml*. (Quick_setup.ps1 forskriftin bjó til þennan ílát.) Þessi skrá er nauðsynleg til að birta leiðsluna og búa til prófspá. Fyrir leiðbeiningar, sjá [Hladdu upp blokkabubbi](/azure/storage/blobs/storage-quickstart-blobs-portal#upload-a-block-blob).
1. Í Azure Machine Learning Studio, veldu **Minnisbækur** í stýrikerfinu.
1. Finndu eftirfarandi staðsetningu í **Skrár** uppbygging: **Notendur/\[ núverandi notandi\] /src**.
1. Hladdu upp hinum fjórum skrám sem þú hleður niður í skrefi 1 á staðinn sem þú fannst í fyrra skrefi.
1. Veldu **api_trigger.py** skrá sem þú hlóðst upp og keyrðu hana. Það mun búa til leiðslu sem hægt er að kveikja í gegnum API.
1. Vinnusvæðið þitt er nú sett upp. Hoppaðu á undan til [Settu upp tengingarfæribreytur Azure Machine Learning Service í Supply Chain Management](#demand-forecast-parameters) kafla.

#### <a name="option-2-manually-set-up-your-machine-learning-workspace"></a><a name="ml-workspace-manual"></a> Valkostur 2: Settu upp vinnusvæðið fyrir vélanám handvirkt

Þessi hluti lýsir því hvernig á að setja upp vinnusvæðið fyrir vélanám handvirkt. Þú verður aðeins að ljúka verklagsreglunum í þessum hluta ef þú ákvaðst að keyra ekki sjálfvirka uppsetningarforskriftina, eins og lýst er í [Valkostur 1: Keyrðu skriftu til að setja upp vinnusvæðið þitt fyrir vélanám](#ml-workspace-script) kafla.

##### <a name="step-1-create-a-new-workspace"></a><a name="create-workspace"></a> Skref 1: Búðu til nýtt vinnusvæði

Notaðu eftirfarandi aðferð til að búa til nýtt vélrænt vinnusvæði.

1. Skráðu þig inn á Azure gáttina þína.
1. Opnaðu **Vélnám** þjónustu.
1. Veldu **Búa til** á tækjastikunni til að opna **Búa til** galdramaður.
1. Ljúktu við töframanninn með því að fylgja leiðbeiningunum á skjánum. Hafðu eftirfarandi atriði í huga þegar þú vinnur:

    - Notaðu sjálfgefnar stillingar nema aðrir punktar á þessum lista mæli með öðrum stillingum.
    - Vertu viss um að velja landfræðilega svæðið sem passar við svæðið þar sem tilvik þitt af Supply Chain Management er notað. Annars gætu sum gögnin þín farið í gegnum svæðismörk. Fyrir frekari upplýsingar, sjá [persónuverndartilkynningu](#privacy) síðar í þessari grein.
    - Notaðu sérstaka tilföng, svo sem tilfangahópa, geymslureikninga, gámaskrár, Azure lyklahólf og nettilföng.
    - Á **Settu upp tengingarfæribreytur Azure Machine Learning Service** síðu töframannsins, verður þú að gefa upp nafn geymslureiknings. Notaðu reikning sem er tileinkaður eftirspurnarspá. Inntaks- og úttaksgögn eftirspurnarspár verða geymd á þessum geymslureikningi.

Fyrir frekari upplýsingar, sjá [Búðu til vinnusvæðið](/azure/machine-learning/quickstart-create-resources#create-the-workspace).

##### <a name="step-2-configure-storage"></a><a name="config-storage"></a> Skref 2: Stilltu geymslu

Notaðu eftirfarandi aðferð til að setja upp geymsluna þína.

1. Á GitHub, opnaðu [Sniðmát fyrir Dynamics 365 Supply Chain Management eftirspurnarspá með Azure Machine Learning](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service) endurhverfa og hlaðið niður **sampleInput.csv** skrá.
1. Opnaðu geymslureikninginn sem þú bjóst til í [Skref 1: Búðu til nýtt vinnusvæði](#create-workspace) kafla.
1. Fylgdu leiðbeiningunum í [Búðu til ílát](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container) til að búa til ílát sem heitir *demplan-azureml*.
1. Hladdu upp **sampleInput.csv** skrá sem þú hleður niður í skrefi 1 í ílátið sem þú bjóst til. Þessi skrá er nauðsynleg til að birta leiðsluna og búa til prófspá. Fyrir leiðbeiningar, sjá [Hladdu upp blokkabubbi](/azure/storage/blobs/storage-quickstart-blobs-portal#upload-a-block-blob).

##### <a name="step-3-configure-a-default-datastore"></a>Skref 3: Stilltu sjálfgefna gagnageymslu

Notaðu eftirfarandi aðferð til að setja upp sjálfgefna gagnageymsluna þína.

1. Í Azure Machine Learning Studio, veldu **Gagnaverslanir** í stýrikerfinu.
1. Búðu til nýja gagnageymslu af *Azure Blob Geymsla* tegund sem bendir á *demplan-azureml* Blob geymsluílát sem þú bjóst til í [Skref 2: Stilltu geymslu](#config-storage) kafla. (Ef auðkenningartegund nýju gagnageymslunnar er *Reikningslykill*, gefðu upp reikningslykil fyrir stofnaðan geymslureikning. Fyrir leiðbeiningar, sjá [Stjórna aðgangslykla geymslureiknings](/azure/storage/common/storage-account-keys-manage?tabs=azure-portal) .)
1. Gerðu nýju gagnageymsluna þína að sjálfgefna gagnageymslu með því að opna upplýsingar um hana og velja **Stilla sem sjálfgefna gagnageymslu**.

##### <a name="step-4-configure-compute-resources"></a><a name="config-compute-resources"></a> Skref 4: Stilltu tölvuauðlindir

Notaðu eftirfarandi aðferð til að setja upp tölvuforða í Azure Machine Learning Studio til að keyra forskriftir til að búa til spár.

1. Opnaðu upplýsingasíðuna fyrir vélanámsvinnusvæðið sem þú bjóst til í [Skref 1: Búðu til nýtt vinnusvæði](#create-workspace) kafla. Finndu **Vefslóð vinnustofu** gildi og veldu hlekkinn til að opna hann.
1. Veldu **Reikna** á leiðsöguglugganum.
1. Á **Reiknaðu tilvik** flipa, veldu **Nýtt** til að opna töframann sem mun hjálpa þér að búa til nýtt tölvutilvik. Fylgdu leiðbeiningunum á skjánum. Reiknitilvikið verður notað til að búa til eftirspurnarspápípuna (hægt að eyða henni eftir að leiðsla er birt.) Notaðu sjálfgefnar stillingar.
1. Á **Reikna klasa** flipa, veldu **Nýtt** til að opna töframann sem mun hjálpa þér að búa til nýjan tölvuklasa. Fylgdu leiðbeiningunum á skjánum. Reikniklasinn verður notaður til að búa til eftirspurnarspár. Stillingar þess hafa áhrif á frammistöðu og hámarksstig samhliða hlaupsins. Stilltu eftirfarandi reiti, en notaðu sjálfgefnar stillingar fyrir alla aðra reiti:

    - **Nafn** - Koma inn *e2ecpucluster*.
    - **Stærð sýndarvélar** – Stilltu þessa stillingu í samræmi við magn gagna sem þú býst við að nota sem inntak fyrir eftirspurnarspá. Hnútafjöldi ætti ekki að fara yfir 11, vegna þess að einn hnút þarf til að koma af stað myndun eftirspurnarspár og hámarksfjöldi hnúta sem hægt er að nota til að búa til spá er 10. (Þú munt einnig stilla fjölda hnúta í parameters.py skránni í [Skref 5: Búðu til leiðslur](#create-pipelines) kafla.) Á hverjum hnút verða nokkrir verkamannaferli sem keyra spáforskriftir samhliða. Heildarfjöldi starfsmannaferla í starfi þínu verður *Fjöldi kjarna sem hnútur hefur* ×*Fjöldi hnúta*. Til dæmis, ef tölvuklasinn þinn hefur tegund af *Standard\_ D4* (átta kjarna) og að hámarki 11 hnúta, og ef`nodes_count` gildi er stillt á *10* í parameters.py skránni er virkt stig samhliða 80.

##### <a name="step-5-create-pipelines"></a><a name="create-pipelines"></a> Skref 5: Búðu til leiðslur

Leiðslur bjóða upp á leið til að byrja að spá forskriftir frá Supply Chain Management. Notaðu eftirfarandi aðferð til að búa til nauðsynlegar leiðslur.

1. Á GitHub, opnaðu [Sniðmát fyrir Dynamics 365 Supply Chain Management eftirspurnarspá með Azure Machine Learning](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service) repo, og hlaðið niður eftirfarandi skrám:

    - src/parameters.py
    - src/api_trigger.py
    - src/run.py
    - src/REntryScript/forecast.r

1. Í Azure Machine Learning Studio, veldu **Minnisbækur** í stýrikerfinu.
1. Finndu eftirfarandi staðsetningu í **Skrár** uppbygging: **Notendur/\[ núverandi notandi\] /src**.
1. Hladdu upp fjórum skrám sem þú hleður niður í skrefi 1 á staðinn sem þú fannst í fyrra skrefi.
1. Í Azure, opnaðu og skoðaðu **parameters.py** skrá sem þú hlóðst upp. Gakktu úr skugga um að`nodes_count` gildi er einu minna en gildið sem þú stilltir fyrir tölvuklasann í [Skref 4: Stilltu tölvuauðlindir](#config-compute-resources) kafla. Ef`nodes_count` gildi er stærra en eða jafnt og fjölda hnúta í tölvuklasanum, gæti leiðslukeyrslan byrjað. Hins vegar mun það þá hætta að svara á meðan það bíður eftir nauðsynlegum úrræðum. Fyrir frekari upplýsingar um fjölda hnúta, sjáðu [Skref 4: Stilltu tölvuauðlindir](#config-compute-resources) kafla.
1. Veldu **api_trigger.py** skrá sem þú hlóðst upp og keyrðu hana. Það mun búa til leiðslu sem hægt er að kveikja í gegnum API.

### <a name="set-up-a-new-active-directory-application"></a><a name="aad-app"></a> Settu upp nýtt Active Directory forrit

Active Directory forrit er nauðsynlegt til að auðkenna með tilföngum sem eru tileinkuð eftirspurnarspá með því að nota þjónustustjóra. Þess vegna ætti forritið að hafa lægsta réttindi sem þarf til að búa til spána.

1. Skráðu þig inn á Azure gáttina þína.
1. Skráðu nýja umsókn í leigjanda Azure Active Directory (Azure AD). Fyrir leiðbeiningar, sjá [Notaðu gáttina til að búa til Azure AD umsóknar- og þjónustustjóri sem hefur aðgang að auðlindum](/azure/active-directory/develop/howto-create-service-principal-portal).
1. Fylgdu leiðbeiningunum á skjánum þegar þú klárar töframanninn. Notaðu sjálfgefnar stillingar.
1. Veittu nýja Active Directory forritinu þínu aðgang að eftirfarandi tilföngum sem þú bjóst til í [Settu upp vélanám í Azure](#ml-workspace) kafla. Fyrir leiðbeiningar, sjá [Úthlutaðu Azure hlutverkum með því að nota Azure gáttina](/azure/role-based-access-control/role-assignments-portal?tabs=current). Þetta skref gerir kerfinu kleift að flytja inn og flytja út spágögn og koma af stað vélanámsleiðslum frá Supply Chain Management.

    - Framlagshlutverk í vinnusvæði vélanáms
    - Framlagshlutverk á sérstaka geymslureikninginn
    - Storage Blob Data Contributor hlutverk á sérstaka geymslureikninginn

1. Í **Vottorð og leyndarmál** hluta forritsins sem þú bjóst til skaltu búa til leyndarmál fyrir forritið. Fyrir leiðbeiningar, sjá [Bættu við leyndarmáli viðskiptavinar](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret).
1. Skráðu auðkenni forritsins og leyndarmál þess. Þú þarft upplýsingar um þetta forrit síðar, þegar þú setur upp **Eftirspurnarspábreytur** síðu í Supply Chain Management.

### <a name="set-up-azure-machine-learning-service-connection-parameters-in-supply-chain-management"></a><a name="demand-forecast-parameters"></a> Settu upp tengingarfæribreytur Azure Machine Learning Service í Supply Chain Management

Notaðu eftirfarandi aðferð til að tengja Supply Chain Management umhverfið þitt við vélanámsþjónustuna sem þú varst að setja upp í Azure.

1. Skráðu þig inn í Supply Chain Management.
1. Fara til **Aðalskipulag \> Uppsetning \> Eftirspurnarspá \> Eftirspurnarspábreytur**.
1. Á **Almennt** flipa skaltu ganga úr skugga um að **Stefna til að búa til spár** reiturinn er stilltur á *Azure Machine Learning Service*.
1. Á **Vöruúthlutunarlyklar** flipa skaltu ganga úr skugga um að **Stefna til að búa til spár** reiturinn er stilltur á *Azure Machine Learning Service* fyrir hvern úthlutunarlykil sem ætti að nota Azure Machine Learning Service fyrir eftirspurnarspá.
1. Á **Azure Machine Learning Service** flipa, stilltu eftirfarandi reiti:

    - **Auðkenni leigjanda** – Sláðu inn auðkenni fyrir Azure leigjanda þinn. Aðfangakeðjustjórnun mun nota þetta auðkenni til að auðkenna með Azure Machine Learning Service. Þú getur fundið leigjanda auðkenni þitt á **Yfirlit** síðu fyrir Azure AD í Azure gáttinni.
    - **Auðkenni aðalumsóknar þjónustu** – Sláðu inn auðkenni forritsins fyrir forritið sem þú bjóst til í [Active Directory forrit](#aad-app) kafla. Þetta gildi er notað til að heimila API beiðnir til Azure Machine Learning Service.
    - **Leyndarmál þjónustustjóra** – Sláðu inn leyndarmál þjónustuforritsins fyrir forritið sem þú bjóst til í [Active Directory forrit](#aad-app) kafla. Þetta gildi er notað til að afla aðgangslykilsins fyrir öryggisstjórann sem þú bjóst til til að framkvæma viðurkenndar aðgerðir gegn Azure Storage og Azure Machine Language vinnusvæðinu.
    - **Heiti geymslureiknings** – Sláðu inn nafn Azure geymslureikningsins sem þú tilgreindir þegar þú keyrðir uppsetningarhjálpina á Azure vinnusvæðinu þínu. (Nánari upplýsingar er að finna í [Settu upp vélanám í Azure](#ml-workspace) kafla.)
    - **Heimilisfang leiðsluenda** – Sláðu inn vefslóð REST endapunkts leiðslunnar fyrir Azure Machine Learning Service þína. Þú bjóst til þessa leiðslu sem síðasta skrefið þegar þú [setja upp vélanám í Azure](#ml-workspace). Til að fá leiðsluslóðina skaltu skrá þig inn á Azure gáttina þína, velja **Leiðslur** á siglingu. Á **Leiðsla** flipanum skaltu velja endapunkt leiðslunnar sem er nefndur **TriggerDemandForecastGeneration**. Afritaðu síðan REST endapunktinn sem er sýndur.

    ![Færibreytur á Azure Machine Learning Service flipanum á færibreytum eftirspurnarspár síðunni.](media/azure-ml-service-parameters.png "Færibreytur á Azure Machine Learning Service flipanum á færibreytum eftirspurnarspár síðunni")

## <a name="privacy-notice"></a><a name="privacy"></a>Tilkynning um persónuvernd

Þegar þú velur *Azure Machine Learning Service* sem spáframleiðsluáætlun þín sendir Supply Chain Management sjálfkrafa gögn viðskiptavina þinna fyrir sögulega eftirspurn, svo sem samanlagt magn, vöruheiti og vörustærðir þeirra, sendingar- og móttökustaðsetningar, auðkenni viðskiptavina og einnig spábreytur, til landsvæðisins þar sem vélin þín er námsvinnusvæði og tengdur geymslureikningur þess eru staðsettir í þeim tilgangi að spá fyrir um eftirspurn í framtíðinni. Azure Machine Learning Service gæti verið á öðru landfræðilegu svæði en landsvæðinu þar sem Supply Chain Management er beitt. Sumir notendur geta stjórnað því hvort þessi virkni sé virkjuð með því að velja spáframleiðslustefnuna á **Eftirspurnarspábreytur** síðu.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit eftirspurnarspár](introduction-demand-forecasting.md)
- [Myndun tölfræðilegrar grunnlínuspár](generate-statistical-baseline-forecast.md)
- [Gera handvirkar leiðréttingar á grunnlínuspánni](manual-adjustments-baseline-forecast.md)
- [Vefnámskeið: Eftirspurnarspá með Azure Machine Learning Series](https://aka.ms/DemandForecastingwithAzureMachineLearningSeries)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
