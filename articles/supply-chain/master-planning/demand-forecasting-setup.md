---
title: Uppsetning eftirspurnarspár
description: Þessi grein lýsir uppsetningarverk sem þarf að framkvæma til að undirbúa eftirspurnarspár.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/14/2022
ms.locfileid: "8960155"
---
# <a name="demand-forecasting-setup"></a>Uppsetning eftirspurnarspár

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að setja upp eftirspurnarspá.  

## <a name="item-allocation-keys"></a>Úthlutunarlyklar vöru

Úthlutunarlyklar vöru stofna vöruflokka. eftirspurnarspá er reiknuð fyrir vöruna og víddir aðeins ef varan er hluti af úthlutunarlykil vöru. Þessi regla er notuð til að flokka saman mikinn fjölda af vörum, þannig að hægt er að stofna eftirspurnarspár fljótlegri hátt. Spár eru stofnaðar á grundvelli söguleg gögn.

Vara og víddir hennar verður að vera hluti af aðeins einum úthlutunarlykil vöru ef úthlutunarlykill vöru er notaður við stofnun spár.

Til að búa til úthlutunarlykill vöru og bæta birgðarhaldseiningu (SKU) við þá skal fylgja þessum skrefum.

1. Farðu í **Aðaláætlanagerð \> Uppsetning \> Eftirspurnarspá \> Úthlutunarlyklar vöru**.
1. Veldu úthlutunarlykill vöru á listasvæðinu eða veldu **Nýtt** á aðgerðasvæðinu til að búa til nýjan. Í haus nýja eða valda lykilinn skal stilla eftirfarandi reiti:

    - **Úthlutunarlykill vöru** – Sláið inn einkvæmt heiti fyrir lykilinn.
    - **Heiti** - Færið inn lýsandi heiti á lyklinum.

1. Fylgdu einu af eftirfarandi skrefum til að bæta vörum við valinn úthlutunarlykil vöru eða fjarlægja vörur:

    - Á flýtiflipanum **Úthlutun vöru** notaðu hnappana **Nýtt** og **Eyða** á tækjastikunni til að bæta við eða fjarlægja vörur eftir þörfum. Fyrir hverja línu, veldu vörunúmer og úthlutaðu síðan víddargildum í hinum dálkunum eftir þörfum. Veldu **Birta víddir** á tækjastikunni til að breyta setti af víddardálkunum sem birtast í hnitanetinu. (Gildið í dálk **Prósenta** er hunsað þegar eftirspurnarspár eru búnar til).
    - Ef þú vilt bæta miklum fjölda vara við lykilinn skaltu velja **Úthluta vörum** á aðgerðasvæðinu til að opna síðu þar sem hægt er að leita að og úthluta mörgum vörum á valinn lykil.

> [!IMPORTANT]
> Gætið þess að setja aðeins viðeigandi vörur í hvern úthlutunarlykil vöru. Óþarfa vörur gæti valdið aukinn kostnaði þegar þú notar Microsoft Azure Machine Learning.

## <a name="intercompany-planning-groups"></a>fjárhagsáætlunarflokkar innan samstæðu

Eftirspurnarspá getur myndað spár milli fyrirtækja. Í Dynamics 365 Supply Chain Management, fyrirtæki sem eru áætluð saman eru flokkuð í sama áætlunarhóp innan samstæðunnar. Til að tilgreina, per fyrirtæki, hvaða úthlutunarlykil vöru eigi að taka til greina fyrir eftirspurnarspá, skal tengja úthlutunarlykill vöru við áætlunarflokk meðlims innan samstæðu í áætlunarflokki.

> [!IMPORTANT]
> Fínstilling áætlanagerðar styður ekki við áætlunarhópa innan samstæðu eins og stendur. Til að gera áætlanagerð innan samstæðu sem notar fínstillingu skipulagningar skaltu setja upp runuvinnslu aðaláætlanagerðar sem fela í sér aðaláætlanir fyrir öll viðkomandi fyrirtæki.

Fylgið eftirfarandi skrefum til að setja upp áætlunarhópa innan samstæðu.

1. Farið í **Aðaláætlanagerð \> Uppsetning \> Áætlunarhópar innan samstæðu**.
1. Veldu áætlunarflokk á listasvæðinu eða veldu **Nýtt** á aðgerðasvæðinu til að búa til nýjan. Í haus nýja eða valda flokkinn skal stilla eftirfarandi reiti:

    - **Heiti** – Sláðu inn einkvæmt heiti fyrir áætlunarflokk.
    - **Lýsing** – Færðu inn stutta lýsingu á áætlunarflokki.

1. Á flýtiflipanum **Meðlimur fjárhagsáætlunarflokks innan samstæðu** skal nota hnappana á tækjastikunni til að bæta við línu fyrir hvert fyrirtæki (lögaðila) sem ætti að vera hluti af flokknum. Fyrir hverja línu skal stilla eftirfarandi reiti:

    - **Lögaðili** – Veldu nafn fyrirtækis (lögaðila) sem er meðlimur í völdum flokki.
    - **Tímaröð** - Úthluta röð sem fyrirtækið ætti að vera unnið úr miðað við önnur fyrirtæki. Lág gildi eru unnin fyrst. Þessi röð getur verið mikilvæg þegar eftirspurn eftir einu fyrirtæki hefur áhrif á önnur fyrirtæki. Í slíkum tilvikum ætti að vinna úr fyrirtækið sem svarar eftirspurninni síðast.
    - **Aðaláætlun** – Veljið aðaláætlun til að ræsa fyrir núverandi fyrirtæki.
    - **Sjálfvirkt afrit í fasta áætlun** – Veljið þennan gátreit til að afrita niðurstöðu áætlunarinnar í fasta áætlun.
    - **Sjálfvirkt afrit í breytilega áætlun** – Veljið þennan gátreit til að afrita niðurstöðu áætlunarinnar í breytilega áætlun.

1. Að sjálfgefnu, ef engin úthlutunarlykla vöru er úthlutað til aðila áætlanahóps, innan samstæðu, er eftirspurnarspá reiknuð fyrir allar vörur sem er úthlutað til allra úthlutunarlykla vöru frá öllum fyrirtækjum. Aukalegir Síunarvalkosti fyrir fyrirtæki og úthlutunarlykla vöru eru tiltækar í svarglugganum **Mynda tölfræðilega grunnlínuspá** dialog box (**Aðaláætlanagerð \> Spá \> Eftirspurnarspá \> Mynda tölfræðilega grunnlínuspá**). Til að úthluta úthlutunarlykill vöru til fyrirtækis í völdum áætlunarflokki innan samstæðu skal velja fyrirtækið og síðan á flýtiflipanum **Meðlimir fjárhagsáætlunarflokks innan samstæðu** velja **Úthlutunarlyklar vöru** á tækjastikunni.

> [!IMPORTANT]
> Gætið þess að hafa einungis viðeigandi úthlutunarlykla vöru í hverjum áætlanahópi innan samstæðunnar. Óþarfa vörur gæti valdið aukinn kostnaði þegar þú notar Azure Machine Learning.

## <a name="set-up-demand-forecasting-parameters"></a><a name="parameters"></a>Setja upp færibreytur eftirspurnarspár

Notaðu síðuna fyrir **Færibreytur eftirspurnarspár** til að setja upp nokkra valkosti sem stýra því hvernig eftirspurnarspá virkar í kerfinu.

### <a name="open-the-demand-forecasting-parameters-page"></a>Opna síðu færibreytur eftirspurnarspár

Til að setja upp færibreytur spáa, Fara í **aðaláætlanagerð \> Uppsetning \>  Eftirspurnarspá \> Færibreytur eftirspurnarspár**. Þar sem eftirspurnarspár keyra þvert á milli fyrirtækja, er uppsetning altæk. Það gildir með öðrum orðum um alla lögaðila (fyrirtæki).

### <a name="general-settings"></a>Almennar stillingar

Notaðu flipann **Almennt** á síðunni **Færibreytur eftirspurnarspár** til að skilgreina almennar stillingar fyrir eftirspurnarspá.

#### <a name="demand-forecast-unit"></a>Eining eftirspurnarspár

Eftirspurnarspá myndar spá í magni. Þess vegna mælieining sem magn skal sýnt í vera tilgreint í á **eining eftirspurnarspár** svæði. Í þessum reit er skilgreind sú eining sem verður notuð fyrir allar eftirspurnarspár, óháð venjulegum birgðaeiningum fyrir hverja vöru. Með því að nota samræmda spáeiningu hjálpar þú til við að tryggja að uppsöfnun og prósentudreifing sé skynsamlegt. Nánari upplýsingar um uppsöfnun og prósentudreifingu sjá [gera handvirkar Leiðréttingar á grunnlínuspá](manual-adjustments-baseline-forecast.md).

Fyrir hverja mælieiningu sem er notað fyrir Birgðahaldseiningar sem eru hafðar með í eftirspurnarspá, skal ganga úr skugga um að það sé umreikningsreglu fyrir mælieininguna og almenna mælieiningu eftirspurnarspár sem þú velur hér. Þegar spármyndun er keyrð, er listi yfir vörur sem ekki hafa umreikning mælieiningar skráður. Því getur þú auðveldlega lagfært uppsetninguna. Frekari upplýsingar um mælieiningar og hvernig þeim er breytt er að finna í [Stjórna mælieiningum](../pim/tasks/manage-unit-measure.md).

#### <a name="transaction-types"></a>Færslugerðir

Notaðu reitina á flýtiflipanum **Færslugerðir** til að velja færslugerðir sem eru notaðar þegar tölfræðileg grunnlínuspá er mynduð.

Eftirspurnarspá má nota til að spá bæði háðri eftirspurn og óháð eftirspurn. Til dæmis, ef aðeins valkosturinn **Sölupöntun** er stilltur á *Já* og ef vörur sem teknar eru til greina fyrir eftirspurnarspá eru seldar vörur, reiknar kerfið óháða eftirspurn. Hins vegar er mikilvæg undiríhlutir bætt við úthlutunarlykla vöru og hafðar með í eftirspurnarspá. Í þessu tilfelli, ef valkosturinn **framleiðslulínu** er stilltur á *Já*, er háð spá reiknuð.

Hægt er að hnekkja færslugerðum fyrir einn eða fleiri tiltekna úthlutunarlykill vöru með því að nota flipann **Úthlutunarlyklar vörur**. Þessi flipi gefur upp svipaða reiti.

#### <a name="choose-how-to-create-the-baseline-forecast"></a>Velja hvernig á að búa til grunnlínuspá

Í reitnum **Myndunarstefna spár** er hægt að velja aðferðina sem er notuð til að búa til grunnlínuspá. Þrjár aðferðir eru í boði:

- *Afrita yfir söguleg eftirspurnargögn* – Búa til spár með því að afrita bara söguleg gögn.
- *Azure Machine Learning Service* – Notaðu spárlíkan sem notar Azure Machine Learning Service. Azure Machine Learning Service er núverandi lausn fyrir vélrænt nám fyrir Azure. Því mælum við með að þú notir það ef þú vilt nota forspárlíkan.
- *Azure Machine Learning Service* – Notaðu spárlíkan sem notar Azure Machine Learning Service (klassísk). Azure Machine Learning Studio (klassísk) hefur verið gerð úrelt og verður fljótlega fjarlægt úr Azure. Því mælum við með því að þú veljir *Azure Machine Learning Service* ef þú ert að setja upp eftirspurnarspá í fyrsta skipti. Ef þú ert að nota Azure Machine Learning Studio (klassískt) ættir þú að skipta yfir í Azure Machine Learning Service eins fljótt og auðið er.

Hægt er að hnekkja spámyndunaraðferðinni fyrir einn eða fleiri tiltekna úthlutunarlykill vöru með því að nota flipann **Úthlutunarlyklar vöru**. Þessi flipi gefur upp svipaða reiti.

#### <a name="override-default-forecast-algorithm-parameters-globally"></a>Hnekkja altækt sjálfgefnum færibreytum fyrir spá reiknirita

Sjálfgefnar færibreytur og gildi algríms spár eru úthlutuð á síðunni **Færibreytur eftirspurnarspár** (**Aðaláætlunargerð \> Uppsetning \> Eftirspurnarspár \> Færibreytur eftirspurnarspár**). Hins vegar er hægt að hnekkja þeim altækt með því að nota flýtiflipann **Færibreytur algríms eftirspurnarspár** á flipanum **Almennt** á síðunni **Færibreytur eftirspurnarspár**. (Einnig er hægt að hnekkja þeim fyrir tiltekna úthlutunarlykla með því að nota flipann **Úthlutunarlyklar vöru** á síðunni **Færibreytur eftirspurnarspár**).

Notaðu hnappana **Bæta við** og **Fjarlægja** á tækjastikunni til að setja á áskilið safn af hnekkingu færibreyta. Fyrir hverja færibreytu í listanum skal velja gildi í reitnum **Heiti** og síðan færa inn viðeigandi gildi í reitinn **Gildi**. Allar færibreytur sem ekki eru sýndar hér munu taka gildi sín frá stillingunum á síðunni **Færibreytur eftirspurnarspár**. Frekari upplýsingar um hvernig á að nota stöðluð sett færibreyta og velja gildi fyrir þær eru í hlutanum [Sjálfgefnar færibreytur og gildi fyrir eftirspurnarspárlíkön](#model-parameters).

### <a name="set-forecast-dimensions"></a>Stilla spávíddir

Spávídd gefur til kynna upplýsingastig sem skilgreind er fyrir spá. Fyrirtæki, vefsvæði og úthlutunarlykill vöru eru áskildar spávíddir. Þú getur einnig myndað spár í vöruhús, birgðastaða, viðskiptavinaflokkur, viðskiptavinalykill, land/svæði, ríki og/eða á vörustigi og á öllum vöruvíddarstigum. Notið flipann **Spávíddir** á síðunni **Færibreytur eftirspurnarspár** til að velja sett spávíddir sem notaðar eru þegar eftirspurnarspáin er búin til.

Hægt er að bæta spávíddir við lista yfir víddir sem eru notaðar fyrir eftirspurnarspár á hvaða tímapunkti. Einnig er Hægt að fjarlægja spávídd af listanum. Hins vegar tapast handvirkar leiðréttingar ef verið er að bæta við eða fjarlægja spárvídd.

### <a name="set-up-overrides-for-specific-item-allocation-keys"></a>Setja upp hnekkingar fyrir tiltekna úthlutunarlykill vöru

Ekki allar vörur virka á saman hátt úr sjónarhorn eftirspurnarspár. Því er hægt að setja upp sérstakar hnekkingar úthlutunarlykils fyrir flestar stillingar sem eru skilgreindar á flipanum **Almennt**. Undantekningin er eftirspurnarspáreiningin. Til að setja upp hnekkingar á tilteknum úthlutunarlykill vöru skal fylgja þessum skrefum.

1. Á síðunni **Færibreytur eftirspurnarspár**, á flipanum **Úthlutunarlyklar vöru**, skaltu nota hnappana á tækjastikunni til að bæta við úthlutunarlyklum fyrir vöru í reitinn vinstra megin eða fjarlægja þá, eftir þörfum. Veldu síðan úthlutunarlykill sem á að setja upp hnekkingar fyrir.
1. Á fanum **Færslutegundir** virkjar þú þær tegundir færslna sem þú vilt nota til að búa til tölfræðilega grunnlínuspá fyrir vörur sem tilheyra völdum úthlutunarlykli. Stillingarnar virka rétt eins og þær virka á flipanum **Almennt**, en þær eiga aðeins við um valinn úthlutunarlykill vöru. Allar stillingarnar hér (bæði gildin *Já* og *Nei*) hnekkja allar **Færslugerðir** á flipanum **Almennt**.
1. Á flýtiflipanum **Færibreytur algríms spár** skal velja myndunarstefna spár og spá og hnekkingar færibreyta algríms spár fyrir vörur sem tilheyra völdum úthlutunarlykli. Þessar stillingar virka rétt eins og þær virka á flipanum **Almennt**, en þær eiga aðeins við um valinn úthlutunarlykil vöru. Notaðu hnappana **Bæta við** og **Fjarlægja** á tækjastikunni til að setja á áskilið safn af hnekkingum færibreyta. Fyrir hverja færibreytu í listanum skal velja gildi í reitnum **Heiti** og síðan færa inn viðeigandi gildi í reitinn **Gildi**. Frekari upplýsingar um hvernig á að nota stöðluð sett færibreyta og velja gildi fyrir þær eru í hlutanum [Sjálfgefnar færibreytur og gildi fyrir eftirspurnarspárlíkön](#model-parameters).

### <a name="set-up-the-connection-to-the-azure-machine-learning-service"></a>Setja upp tengingu við Azure Machine Learning Service

Notaðu flipann **Azure Machine Learning Service** til að setja upp tengingu við Azure Machine Learning Service. Þessi lausn er einn af valkostunum til að búa til grunnlínuspána. Þessar stillingar á þessum flipa hafa aðeins áhrif þegar reiturinn **Myndunarstefna spár** er stilltur á *Azure Machine Learning Service*.

Frekari upplýsingar um hvernig á að setja upp Azure Machine Learning Service og síðan nota stillingarnar hér til að tengjast því eru í hlutanum [Setja upp Azure Machine Learning Service](#setup-amls).

### <a name="set-up-the-connection-to-azure-machine-learning-studio-classic"></a>Setja upp tengingu við Azure Machine Learning Studio (hefðbundna útgáfu)

> [!IMPORTANT]
> Azure Machine Learning Studio (klassískt) er orðið úrelt. Því er ekki lengur hægt að búa til ný vinnusvæði fyrir það í Azure. Það hefur verið skipt út fyrir Azure Machine Learning Service, sem veitir svipaða eiginleika og meira til. Ef þú ert ekki þegar að nota Azure Machine Learning ættir þú að byrja að nota Azure Machine Learning Service. Ef þú ert þegar með vinnusvæði sem var búið til fyrir Azure Machine Learning Studio (hefðbundna útgáfu) geturðu haldið áfram að nota það þar til eiginleikinn hefur verið fjarlægður að fullu úr Azure. Hins vegar mælum við með því að þú uppfærir í Azure Machine Learning Service eins fljótt og hægt er. Þó að forritið muni áfram vara þig við því að Azure Machine Learning Studio (hefðbundin útgáfa) er orðið úrel hefur það ekki áhrif á spámyndun. Frekari upplýsingar um hvernig á að setja upp Azure Machine Learning Service eru í hlutanum [Setja upp Azure Machine Learning Service](#setup-amls).
>
> Þú getur skipt frjálst á milli þess að nota nýju og gömlu lausnirnar fyrir vélrænt nám í Supply Chain Management svo lengi sem gamla Azure Machine Learning Studio (hefðbundna útgáfan) vinnusvæðið þitt er tiltækt.

Ef þú ert nú þegar með tiltækt vinnusvæði fyrir Azure Machine Learning Studio (hefðbunda útgáfu) geturðu notað það til að búa til spár með því að tengja það við Supply Chain Management. Hægt er að koma þessari tengingu á með því að nota flipann **Azure Machine Learning** á síðunni **Færibreytur eftirspurnarspár**. (Stillingarnar á þessum flipa hafa aðeins áhrif þegar reiturinn **Myndunarstefna spár** er stilltur á *Azure Machine Learning*). Sláðu inn eftirfarandi upplýsingar fyrir Azure Machine Learning Studio (hefðbundna útgáfu) vinnusvæðið þitt:

- API-lykill vefþjónustu (lykill forritunarviðmóts)
- vefslóð endapunkts fyrir vefþjónustu
- Heiti Azure-geymslureiknings
- Lykill fyrir Azure-geymslureikning

> [!NOTE]
> Heiti og lykill fyrir Azure-geymslureikning eru nauðsynleg aðeisn ef þú notar sérsniðinn geymslureikning. Ef verslunarsvæði á útgáfu er notuð, verður þú að hafa sérsniðinn geymslureikning í Azure, þannig að Machine Learning hafi aðgang að söguleg gögn.

## <a name="default-parameters-and-values-for-demand-forecasting-models"></a><a name="model-parameters"></a>Sjálfgefnar færibreytur og gildi fyrir eftirspurnarspárlíkön

Þegar þú notar vélrænt nám til að búa til spáráætlunarlíkön getur þú stjórnað valkostum vélrænt náms með því að stilla gildi fyrir *færibreytur algríms fyrir spá*. Þessi gildi eru send frá Supply Chain Management til Azure Machine Learning. Notaðu síðuna **Færibreytur algríms fyrir spá** til að stjórna því hvaða tegundir gilda á að gefa upp og hvaða gildi hver og einn ætti að hafa.

Til að setja upp sjálfgefnar færibreytur og gildi sem notuð eru fyrir eftirspurnarspálíkön skaltu fara í **Aðaláætlanagerð \> Uppsetning \> Eftirspurnarspá \> Færibreytur algríms fyrir spár**. Staðlað sett af færibreytum er í boði. Hver færibreyta hefur eftirfarandi svæði:

- **Heiti** – Heiti færibreytunnar eins og hún er notuð af Azure. Yfirleitt ætti ekki að breyta þessu nafni nema þú hafir sérsniðið tilraunina í Azure Machine Learning.
- **Lýsing** – Almennt heiti fyrir færibreytuna. Þetta heiti er notað til að auðkenna færibreytuna í öðrum hlutum kerfisins (til dæmis á síðunni **Færibreytur eftirspurnarspár**).
- **Gildi** – Sjálfgefið gildi færibreytunnar. Gildið sem á að slá inn fer eftir færibreytunni sem verið er að breyta. 
- **Skýring** – Stutt lýsing á færibreytunni og hvernig á að nota hana. Þessi lýsing inniheldur yfirleitt ráðleggingar um gild gildi fyrir reitinn **Gildi**.

Eftirfarandi færibreytur eru sjálfgefið lagðar í té. (Ef þú verður einhvern tíma að snúa aftur í þennan staðlaða lista skaltu velja **Endurheimta** á Aðgerðasvæði.)

- **Prósentuhlutfall öryggisstigs** – Áreiðanleikabil samanstendur af sviði gilda sem virka sem áreiðanlegt mat fyrir eftirspurnarspána. Til dæmis gefur 95% áreiðanleikastig til kynna að það séu 5% líkur á að framtíðareftirspurnar falli utan sviðs áreiðanleikabils.
- **Þvinga árstíðabindingu** – Tilgreinir hvort neyða eigi líkanið til að nota ákveðna tegund árstíðabundnar. Þessi færibreyta á einungis við um ARIMA og ETS. Valkostir: *SJÁLFVIRKT (sjálfgefið)*, *EKKERT*, *TIL VIÐBÓTAR*, *MARGFALDAÐ*.
- **Spágerð** – Tilgreinir hvaða spágerð á að nota. Valkostir: *ARIMA*, *ETS*, *STL*, *ETS+ARIMA*, *ETS+STL*, *ALL*. Til að velja líkanið sem passar best skal nota *ALLT*.
- **Hámarksfjöldi spáðra gilda** – Tilgreinir hámarksgildið sem á að nota fyrir spár. Snið: + 1E [n] eða föst tala.
- **Lágmarksfjöldi spáðra gilda** – Tilgreinir lágmarksgildið sem á að nota fyrir spár. Snið: - 1E [n] eða föst tala.
- **Gildisskipti vantar** – Tilgreinir hvernig eyður í sögulegum gögnum eru fylltar. Valkostir: *(tölugildi)*, *MEAN*, *PREVIOUS*, *INTERPOLATE LINEAR*, *INTERPOLATE POLYNOMIAL*.
- **Umfang gildissviðs vantar** – Tilgreinir hvort gildisbreytingin eigi einungis við um dagsetningasvið sérhverrar uppskiptingareigindar eða fyrir allt gagnasafnið. Eftirfarandi valkostir eru í boði til að setja á dagsetningabilið sem kerfið notar þegar fyllt er upp í bil í sögulegum gögnum:

    - *ALTÆKT* – Kerfið notar fullt dagsetningarsvið yfir allar eigindir uppskiptingar.
    - *HISTORY_DATE_RANGE* – Kerfið notar tiltekið dagsetningabil sem skilgreint er með reitunum **Frá dagsetningu** og **Til dagsetningar** í **Söguleg tímamörk** í svarglugganum **Mynda tölfræðilega grunnlínuspá**.
    - *GRANULARITY_ATTRIBUTE* – Kerfið notar dagsetningabilið fyrir eigind uppskiptingar sem búið er að gera.

    > [!NOTE]
    > Eigind uppskiptingar er samsetning spávídda sem er notuð við gerð spár. Hægt er að skilgreina spávíddir á síðunni **Færibreytur eftirspurnarspár**.

- **Árstíðarbundin vísbending** – Fyrir árstíðabundin gögn, gefðu vísbendingu um spárlíkanið til að bæta nákvæmni spárinnar. Snið: heilttala, sem táknar fjölda ramma sem eftirspurnarmynstur endurtekur sig. Til dæmis skaltu slá inn *6* fyrir gögn sem endurtaka sig á sex mánaða fresti.
- **Prósentuhlutfall stærðar í prófunarsetti** – Hlutfall sögulegra gagna sem nota á sem prófunarsett fyrir útreikning á nákvæmni spár.

Hægt er að hnekkja gildum þessara færibreytur með því að fara í **Aðaláætlanagerð \> Uppsetning \> Eftirspurnarspá \> Færibreytur eftirspurnarspár**. Á síðunni **Færibreytur eftirspurnarspár** er hægt að hnekkja færibreyturnar á eftirfarandi hátt:

- Notaðu flipann **Almennt** til að hnekkja altækt færibreytunum.
- Notaðu flipann **Úthlutunarlykill vöru** til að hnekkja færibreyturnar fyrir tiltekna úthlutunarlykil vöru. Færibreytur sem er hnekkt fyrir tiltekinn vöruúthlutunarlykil hafa eingöngu áhrif á spár fyrir vörur sem eru tengd þeim úthlutunarlykil vöru.

> [!NOTE]
> Á síðunni **Færibreytur algríms fyrir spá** er hægt að nota hnappana á aðgerðasvæðinu til að bæta við færibreytum á listann eða fjarlægja færibreytur af listanum. Hins vegar ættir þú yfirleitt ekki að nota þessa aðferð nema þú hafir sérsniðið tilraunina í Azure Machine Learning.

## <a name="set-up-the-azure-machine-learning-service"></a><a name="setup-amls"></a>Setja upp Azure Machine Learning Service

Supply Chain Management reiknar út eftirspurnarspá með því að nota Azure Machine Learning Service, sem þú verður að setja upp og keyra á þinni eigin Azure-áskrift. Þessi hluti lýsir því hvernig á að setja upp Azure Machine Learning Service í Azure og síðan tengja það við umhverfi þitt í Supply Chain Management.

### <a name="enable-the-azure-machine-learning-service-in-feature-management"></a>Virkja Azure Machine Learning Service í eiginleikastjórnun

Áður en hægt er að nota Azure Machine Learning Service fyrir eftirspurnarspá verður að kveikja á eiginleika í Supply Chain Management til að virkja samþættinguna. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Aðaláætlanagerð*
- **Heiti eiginleika:** *Azure Machine Learning Service fyrir eftirspurnarspá*

### <a name="set-up-machine-learning-in-azure"></a><a name="ml-workspace"></a>Setja upp vélrænt nám í Azure

Til að gera Azure kleift að nota vélrænt nám til að vinna úr spám þínum verður að setja upp vinnusvæði fyrir vélrænt nám í Azure í þessum tilgangi. Þú hefur tvo valkosti:

- Til að setja upp vinnusvæðið með því að keyra forskrift sem Microsoft lætur í té skaltu fylgja leiðbeiningunum í hlutanum [Valkostur 1: Keyra forskrift til að setja sjálfkrafa upp vinnusvæði þitt fyrir vélrænt nám](#ml-workspace-script) og fara svo beint í [Setja upp færibreytur tengingar fyrir Azure Machine Learning Service í Supply Chain Management](#demand-forecast-parameters).
- Til að setja upp vinnusvæðið handvirkt skaltu fylgja leiðbeiningunum í hlutanum [Valkostur 2: Settu upp vinnusvæði fyrir vélrænt nám handvirkt](#ml-workspace-manual) og farðu svo í hlutann [Setja upp færibreytur tengingar fyrir Azure Machine Learning Service í Supply Chain Management](#demand-forecast-parameters). Þessi valkostur tekur meiri tíma en veitir þér meiri stjórn.

#### <a name="option-1-run-a-script-to-automatically-set-up-your-machine-learning-workspace"></a><a name="ml-workspace-script"></a>Valmöguleiki 1: Keyrðu forskrift til að setja sjálfkrafa upp vinnusvæði fyrir vélrænt nám

Þessi hluti lýsir því hvernig á að setja upp vinnusvæði fyrir vélrænt nám með því að nota sjálfvirka forskrift sem Microsoft lætur í té. Ef þú vilt geturðu sett upp öll úrræði handvirkt með því að fylgja leiðbeiningunum í hlutanum [Valkostur 2: Settu upp vinnusvæði fyrir vélrænt nám handvirkt](#ml-workspace-manual). Þú þarft ekki að ljúka báðum valkostunum.

1. Á GitHub skaltu opna gagnageymsluna (altæk geymsla) [Sniðmát fyrir Dynamics 365 Supply Chain Management eftirspurnarspá með Azure Machine Learning](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service) og hlaða niður eftirfarandi skrám:

    - quick_setup.ps1
    - sampleInput.csv
    - src/parameters.py
    - src/api_trigger.py
    - src/run.py
    - src/REntryScript/forecast.r

1. Opna PowerShell glugga og keyra **quick_setup.ps1** forskrift sem þú sóttir í fyrra skrefi. Fylgdu leiðbeiningunum á skjánum. Forskriftin setur upp áskilið vinnusvæði, geymslu, sjálfgefna gagnasafn og reiknar tilföng. Þú verður samt sem áður að búa til nauðsynlegar sölukeðjur með því að fylgja skrefunum sem eru eftir í þessu ferli. (Sölukeðjur eru aðferð við að ræsa uppskriftir spáa frá Supply Chain Management).
1. Í Azure Machine Learning Studio skaltu hlaða upp **sampleInput.csv** skránni sem þú sóttir í skrefi 1 í geyminn sem er nefnt *demplan-azureml*. (The quick_setup.ps1 forskriftin bjó til þennan geymi). Þessi skrá er áskilin til að birta sölukeðjuna og búa til prufuspá. Leiðbeiningar eru í [Hlaða upp Blob-blökk](/azure/storage/blobs/storage-quickstart-blobs-portal#upload-a-block-blob).
1. Í Azure Machine Learning Studio velur þú **Glósubækur** í Skoðaranum.
1. Finnið eftirfarandi staðsetningu í skipulagi **Skrár**: **Notendur/\[núverandi notandi\]/src**.
1. Hladdu upp hinum fjórum skránum sem þú sóttir í skrefi 1 á staðsetninguna sem þú fannst í fyrra skrefi.
1. Veljið skrána **api_trigger.py** sem þú varst að hlaða upp og keyrið hana. Þá verður til sölukeðja sem hægt er að ræsa í gegnum API.
1. Vinnusvæðið hefur verið sett upp. Farðu áfram í hlutann [Setja upp færibreytur tengingar fyrir Azure Machine Learning Service í Supply Chain Management](#demand-forecast-parameters).

#### <a name="option-2-manually-set-up-your-machine-learning-workspace"></a><a name="ml-workspace-manual"></a>Valmöguleiki 2: Settu upp vinnusvæði fyrir vélrænt nám handvirkt

Þessi hluti lýsir því hvernig stilla eigi vinnusvæði fyrir vélrænt nám handvirkt. Þú verður að ljúka ferlinu í þessum hluta ef þú ákvaðst að keyra ekki sjálfvirka forskrift uppsetningar eins og lýst er í hlutanum [Valkostur 1: Keyra forskrift til að setja upp vinnusvæði fyrir vélrænt nám](#ml-workspace-script).

##### <a name="step-1-create-a-new-workspace"></a><a name="create-workspace"></a>Skref 1: Búa til nýtt vinnusvæði

Notaðu eftirfarandi ferli til að stofna nýtt vinnusvæði fyrir vélrænt nám.

1. Skráðu þig inn á Azure-gáttina þína.
1. Opna kennsluþjónustu **vélræns náms**.
1. Veldu **Búa til** á verkfæraslá til að opna leiðsagnarforritið **Stofna**.
1. Ljúktu leiðsagnarforritinu með því að fylgja leiðbeiningunum á skjánum. Hafðu eftirfarandi atriði í huga þegar þú vinnur:

    - Notaðu sjálfgefnar stillingar nema aðrir punktar í listanum mæli með mismunandi stillingum.
    - Gætið þess að velja það landsvæði sem passar við það svæði þar sem þitt tilvik af Supply Chain Management er notað. Annars gæti verið að eitthvað af gögnunum þínum farið yfir svæðismörk. Frekari upplýsingar eru í [persónuverndaryfirlýsing](#privacy) síðar í þessari grein.
    - Notaðu sérstök tilföng, svo sem tilfangaflokka, geymslureikninga, gámaskrár, lyklageymslur Azure og nettilföng.
    - Á síðunni **Setja upp færibreytur tengingar fyrir Azure Machine Learning Service** í leiðsagnarforritinu, verður þú að slá inn heiti geymslureiknings. Notaðu reikning sem er ætlaður fyrir eftirspurnarspá. Inntaks- og úttaksgögn eftirspurnarspár verða geymd á þessum geymslureikningi.

Frekari upplýsingar eru í [Stofna vinnusvæðið](/azure/machine-learning/quickstart-create-resources#create-the-workspace).

##### <a name="step-2-configure-storage"></a><a name="config-storage"></a>Skref 2: Stilla geymslu

Notaðu eftirfarandi ferli til að setja upp geymsluna.

1. Á GitHub skaltu opna altæka geymslu [Sniðmát fyrir Dynamics 365 Supply Chain Management eftirspurnarspá með Azure Machine Learning](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service) og hlaða niður **sampleInput.csv** skránni.
1. Opna geymslureikninginn sem var stofnaður í hlutanum [Skref 1: Búa til nýtt vinnusvæði](#create-workspace).
1. Fylgdu leiðbeiningunum í [Búa til geymi](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container) til að búa til geymi sem er nefnt *demplan-azureml*.
1. Hlaða upp **sampleInput.csv** skránni sem þú sóttir í skrefi 1 í geyminn sem þú varst að búa til. Þessi skrá er áskilin til að birta sölukeðjuna og búa til prufuspá. Leiðbeiningar eru í [Hlaða upp Blob-blökk](/azure/storage/blobs/storage-quickstart-blobs-portal#upload-a-block-blob).

##### <a name="step-3-configure-a-default-datastore"></a>Skref 3: Stilla sjálfgefið gagnasafn

Notaðu eftirfarandi ferli til að setja upp sjálfgefið gagnasafn.

1. Í Azure Machine Learning Studio velur **Gagnasöfn** í Skoðaranum.
1. Búa til nýja gagnageymslu af gerðinni *Azure Blob Storage* sem vísar á *demplan-azureml* Blob geymsluna sem var búið til í hlutanum [2. skrefi: Stilla geymslu](#config-storage). (Ef sannvottunargerð nýja gagnasafnsins er *Reikningslykill* skaltu gefa upp reikningslykil fyrir nýstofnaðan geymslureikning. Leiðbeiningar eru í [Stjórna aðgangslyklum geymslureikningsins](/azure/storage/common/storage-account-keys-manage?tabs=azure-portal).)
1. Gera nýju gagnasafn þína að sjálfgefinni gagnasafni með því að opna upplýsingar um hana og velja **Velja sem sjálfgefið gagnasafn**.

##### <a name="step-4-configure-compute-resources"></a><a name="config-compute-resources"></a>Skref 4: Stilla útreikning aðfanga

Notið eftirfarandi ferli til að setja upp reiknað tilfang í Azure Machine Learning Studio til að keyra forskriftir spármyndunar.

1. Opna upplýsingasíðuna fyrir vinnusvæði vélrænt nám sem var búið til í hlutanum [Skrefi 1: Búa til nýtt vinnusvæði](#create-workspace). Finndu gildi **Vefslóð Studio** og veldu tengilinn til að opna hann.
1. Veldu **reikna** á yfirlitssvæðinu.
1. Á flipanum **Reikna tilvik** skaltu velja **Nýtt** til að opna leiðsagnarforrit sem mun hjálpa þér að búa til nýtt reiknað tilvik. Fylgdu leiðbeiningunum á skjánum. Reiknaða tilvikið verður notað til að búa til sölukeðju eftirspurnarspár (Hægt er að eyða því eftir að sölukeðhan hefur verið birt.) Notaðu sjálfgefnar stillingar.
1. Á flipanum **Reikniklasi** skaltu velja **Nýtt** til að opna leiðsagnarforrit sem mun hjálpa þér að búa til nýjan reikniklasa. Fylgdu leiðbeiningunum á skjánum. Reikniklasinn verður notaður til að búa til eftirspurnarspár. Stillingar þess hafa áhrif á afköst og hámarksstigi samhliða vinnslu keyrslunnar. Stilltu eftirfarandi reiti en notaðu sjálfgefnar stillingar fyrir alla aðra reiti:

    - **Heiti** – Sláðu inn *e2ecpucluster*.
    - **Stærð sýndarvélar** – Breyttu þesasri stillingu í samræmi við gagnamagnið sem þú gerir ráð fyrir að nota sem inntak fyrir eftirspurnarspá. Hnútafjöldinn ætti ekki að vera meiri en 11, því einn hnútur er nauðsynlegur til að koma af stað myndun eftirspurnarspár og hámarksfjöldi hnúta sem hægt er að nota til að búa til spá er 10. (Þú stillir einnig fjölda hnúta í skránni parameters.py í hlutanum [5. skref: Búa til sölukeðjur](#create-pipelines)). Á hverjum hnút verða nokkrir ferlar starfskrafta sem keyra forskriftir spár samhliða. Heildarfjöldi ferla starfskrafta í verki þínu verður *Fjöldi kjarna sem hnútur hefur* × *Fjöldi hnúta*. Til dæmis, ef reikniklasinn þinn er með gerð af *Staðlað\_D4* (átta kjarna) og að hámarki 11 hnúta, og ef `nodes_count` gildið er sett á *10* í parameters.py skránni er virkt stig hliðstæðu 80.

##### <a name="step-5-create-pipelines"></a><a name="create-pipelines"></a>Skref 5: Búa til sölukeðju

Sölukeðjur eru aðferð við að ræsa uppskriftir spáa frá Supply Chain Management. Notaðu eftirfarandi ferli til að stofna nauðsynlegar leiðslur.

1. Á GitHub skaltu opna altæku geymsluna [Sniðmátin fyrir Dynamics 365 Supply Chain Management eftirspurnarspá með Azure Machine Learning](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service) og hlaða niður eftirfarandi skrám:

    - src/parameters.py
    - src/api_trigger.py
    - src/run.py
    - src/REntryScript/forecast.r

1. Í Azure Machine Learning Studio velur þú **Glósubækur** í Skoðaranum.
1. Finnið eftirfarandi staðsetningu í skipulagi **Skrár**: **Notendur/\[núverandi notandi\]/src**.
1. Hladdu upp skránum fjórum sem þú sóttir í skrefi 1 á staðsetninguna sem þú fannst í fyrra skrefi.
1. Í Azure opnar þú og skoðar skrána **parameters.py** sem þú varst að hlaða upp. Gakktu úr skugga um að `nodes_count` gildið sé einu minna en gildið sem þú stilltir fyrir reikniflokkinn í hlutanum [Skref 4: Stilla reiknitilföng](#config-compute-resources). Ef `nodes_count` gildið er hærra en eða jafnt og fjöldi hnúta í reikniflokknum, gæti verið að hægt að ræsa keyrslu sölukeðjunnar. Hins vegar hættir hún þá að svara á meðan hún bíður eftir nauðsynlegum tilföngum. Nánari upplýsingar um fjölda hnúta er að finna í hlutanum [Skref 4: Stilla reiknitilföng](#config-compute-resources).
1. Veljið skrána **api_trigger.py** sem þú varst að hlaða upp og keyrið hana. Þá verður til sölukeðja sem hægt er að ræsa í gegnum API.

### <a name="set-up-a-new-active-directory-application"></a><a name="aad-app"></a>Setja upp ný Active Directory forrit

Active Directory-forrit er áskilið til að sannvotta með þeim tilföngum sem eru eingöngu til eftirspurnarspár með því að nota þjónustueiningu. Þess vegna ætti forritið að hafa lægsta stig réttinda sem þarf til að búa til spána.

1. Skráðu þig inn á Azure-gáttina þína.
1. Skrá nýja umsókn í Azure Active Directory (Azure AD) leigjanda. Frekari leiðbeiningar er að finna í [Nota gáttina til að stofna Azure AD -forrit og þjónustueiningu með aðgang að tilföngum](/azure/active-directory/develop/howto-create-service-principal-portal).
1. Fylgdu leiðbeiningunum á skjánum þegar þú lýkur við leiðsagnarforritið. Nota sjálfgefnar stillingar.
1. Veittu nýja Active Directory-forritinu þínu aðgang að eftirfarandi tilföngum sem þú bjóst til í hlutanum [Setja upp vélrænt nám í Azure](#ml-workspace). Leiðbeiningar eru í [Úthluta Azure-hlutverkum í Azure-gáttinni](/azure/role-based-access-control/role-assignments-portal?tabs=current). Þetta skref mun gera kerfið kleift að flytja inn og út spágögn, og til að setja af stað sölukeðju vélrænt nám frá Supply Chain Management.

    - Hlutverk þátttakanda í vinnusvæði vélræns náms
    - Hlutverk þátttakanda á sérstakan geymslureikning
    - Hlutverk þátttakanda Blob-geymslu á sérstakan geymslureikning

1. Í hlutanum **Vottorð og leynilyklar** í forritinu sem þú bjóst til skaltu búa til leynilykil fyrir forritið. Frekari leiðbeiningar er að finna í [Bæta við leyniorði biðlara](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret).
1. Skrifið niður auðkenni forrits og leynilykil þess. Þú þarft að fá upplýsingar um þetta forrit síðar, þegar þú setur upp síðu **Færibreytur eftirspurnarspár** í Supply Chain Management.

### <a name="set-up-azure-machine-learning-service-connection-parameters-in-supply-chain-management"></a><a name="demand-forecast-parameters"></a>Setja upp færibreytur tengingar fyrir Azure Machine Learning Service í Supply Chain Management

Notið eftirfarandi ferli til að tengja umhverfi Supply Chain Management við þjónustu vélrænt nám sem þú varst að setja upp í Azure.

1. Skráðu þig inn í Supply Chain Management.
1. Fara í **aðaláætlanagerð \> Uppsetning \> Eftirspurnarspá \> Færibreytur eftirspurnarspár**.
1. Á flipanum **Almennt** skal ganga úr skugga um að reiturinn **Myndunarstefna spár** sé stillt á *Azure Machine Learning Service*.
1. Á flipanum **Úthlutunarlyklar vöru** skal ganga úr skugga um að reiturinn **Myndunarstefna spár** sé stilltur á *Azure Machine Learning Service* fyrir hvern úthlutunarlykill vöru sem skal nota eftirspurnarspá.
1. Á flipanum **Azure Machine Learning Service**, stillirðu eftirfarandi reiti:

    - **Auðkenni leigjanda** – Sláðu inn kenni Azure leigjandann þinn. Supply Chain Managementmun nota þessi auðkenni til að auðkenna sig með Azure Machine Learning Service. Þú finnur leigjandakenni þitt á síðunni **Yfirlit** fyrir Azure AD í Azure-gáttinni.
    - **Forritsauðkenni þjónustueiningar** – Sláðu inn kenni forrits fyrir forritið sem var búið til í hlutanum [Active Directory-forrit](#aad-app). Þetta gildi er notað til að auðkenna API-beiðnir til Azure Machine Learning Service.
    - **Leynilykill þjónustueiningar** – Sláðu inn leynilykill þjónustueiningar fyrir forritið sem var búið til í hlutanum [Active Directory-forrit](#aad-app). Þetta gildi er notað til að fá aðgangslykil fyrir öryggisstjóra sem þú bjóst til að framkvæma viðurkenndar aðgerðir gegn Azure Storage og vinnusvæði Azure Machine Language.
    - **Heiti geymslureiknings** – Sláðu inn heiti Azure geymslureiknings sem þú tilgreindir þegar þú keyrðir leiðsagnarforrit á Azure vinnusvæðinu. (Frekari upplýsingar eru hlutanum í [Setja upp vélrænt nám í Azure](#ml-workspace)).
    - **Aðsetur endastöðvar fyrir sölukeðju** – Sláðu inn vefslóð REST-endapunkts fyrir Azure Machine Learning Service. Þú bjóst til þessa sölukeðju sem síðasta skrefið þegar þú [settir upp vélrænt nám í Azure](#ml-workspace). Skráðu þig inn á Azure-gáttina þína og veldu **Sölukeðjurð** á yfirlitinu til að fá vefslóð sölukeðju. Á flipanum **Sölukeðja** er endapunktur leiðslunnar valinn sem er nefndur **TriggerDemandForecastGeneration**. Afritaðu síðan REST endapunktinn sem er sýndur.

    ![Færibreytur á flipanum Azure Machine Learning Service á síðunni Færibreytur eftirspurnarspár.](media/azure-ml-service-parameters.png "Færibreytur á flipanum Azure Machine Learning Service á síðunni Færibreytur eftirspurnarspár")

## <a name="privacy-notice"></a><a name="privacy"></a>Tilkynning um persónuvernd

Þegar þú velur *Azure Machine Learning Service* sem myndunarstefnu spár, sendir Supply Chain Management sjálfkrafa gögn til viðskiptavina þinna fyrir sögulega eftirspurn, svo sem uppsafnað magn, vöruheiti og vörustærðir þeirra, sendingarstaði og staðsetningu innhreyfingar, auðkenni viðskiptavina og einnig færibreytur spár, til landsvæðisins þar sem vinnusvæði vélræns náms vélarinnar er og tengdur geymslureikningur hennar, í þeim tilgangi að spá fyrir um eftirspurn í framtíðinni. Azure Machine Learning Service gæti verið á öðru landsvæði en því landsvæði þar sem Supply Chain Management er sett upp. Sumir notendur geta stjórnað því hvort þessi eiginleiki er virkjaður með því að velja myndunarstefnu spár á síðunni **Færibreytur eftirspurnarspár**.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit eftirspurnarspár](introduction-demand-forecasting.md)
- [Myndun tölfræðilegrar grunnlínuspár](generate-statistical-baseline-forecast.md)
- [Gera handvirkar leiðréttingar á grunnlínuspánni](manual-adjustments-baseline-forecast.md)
- [Vefnámskeið: Eftirspurnarspá með Azure Machine Learning Series.](https://aka.ms/DemandForecastingwithAzureMachineLearningSeries)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
