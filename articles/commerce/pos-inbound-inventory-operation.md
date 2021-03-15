---
title: Innleið birgðaaðgerð í POS
description: Þetta efni lýsir getu sölustaðar (POS) á heimleið birgðaaðgerð.
author: hhaines
manager: annbe
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: f3dd442f979c23a87ae4b7e69a37de65d5d9bd70
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972631"
---
# <a name="inbound-inventory-operation-in-pos"></a>Innleið birgðaaðgerð í POS

[!include [banner](includes/banner.md)]

Í Microsoft Dynamics 365 Commerce útgáfu 10.0.10 og síðar, koma aðgerðir á innleið og útleið á sölustað (POS) í stað tiltektar- og móttökuaðgerðar.

> [!NOTE]
> Í Commerce útgáfu 10.0.10 og nýrri, verður öllum nýjum eiginleikum í forriti sölustaðar sem tengjast því að taka á móti birgðum verslunar vegna innkaupapantana og flutningspantana bætt við sölustaðaraðgerðina **Aðgerð á innleið**. Ef þú ert að nota tiltektar- og móttökuaðgerðina í POS mælum við með að þú þróir stefnu til að fara frá þeirri aðgerð yfir í nýju aðgerðirnar á inn- og útleið. Þó að tiltektar- og móttökuaðgerðin verði ekki fjarlægð úr vörunni verða engar frekari fjárfestingar í henni, frá sjónarhorni virkni eða afköstum, eftir útgáfu 10.0.9.

## <a name="prerequisite-configure-an-asynchronous-document-framework"></a>Forsenda: Stilla ósamstilltan skjalaramma

Aðgerðin á innleið felur í sér afköst til að tryggja að notendur sem hafa mikið magn bókana á innhreyfingum í mörgum verslunum eða fyrirtækjum og stór birgðaskjöl geti afgreitt þessi skjöl í Commerce Headquarters án þess að lenda í tímalokun eða bilun. Þessar endurbætur þurfa að nota ósamstilltan skjalaramma.

Þegar ósamstilltur skjalarammi er notaður getur þú framkvæmt breytingar á skjali á innleið úr POS í Commerce Headquarters og síðan haldið áfram í önnur verkefni meðan vinnslan í Commerce Headquarters fer fram í bakgrunni. Þú getur athugað stöðu skjals í gegnum skjalalistasíðuna **Aðgerð á innleið** í POS til að ganga úr skugga um að bókun hafi gengið vel. Í POS-forritinu geturðu einnig notað virkan skjalalista aðgerðar á innleið til að sjá öll skjöl sem ekki var hægt að bóka í Commerce Headquarters. Ef skjal tekst ekki geta notendur POS gert leiðréttingar á því og reynt aftur að vinna úr því í Commerce Headquarters.

> [!IMPORTANT]
> Setja þarf upp ósamstillta skjalaramma áður en fyrirtæki reynir að nota aðgerð á innleið í POS.

Til að stilla ósamstilltan skjalaramma skaltu ljúka eftirfarandi verklagsreglum.

### <a name="create-and-configure-a-number-sequence"></a>Stofna og skilgreina númeraröð

1. Farðu á **Fyrirtækisstjórnun \> Númeraröð \> Númeraröð**.
2. Á síðunni **Númeraraðir** skaltu stofna númeraröð.
3. Í reitina **Kóði númeraraðar** og **Heiti** slærðu inn notendaskilgreind gildi.
4. Á flýtiflipanum **Tilvísanir** velurðu **Bæta við**.
5. Í reitnum **Svæði** velurðu **Viðskiptafæribreytur**.
4. Í reitnum **Tilvísun** velurðu **Skjalakenni smásöluaðgerða**.
5. Á flýtflipanum **Almennt**, í hlutanum **Uppsetning**, stillirðu valkostinn **Samfellt** á **Nei** til að tryggja að engin vandamál séu með afköst.

### <a name="create-and-schedule-two-batch-jobs-for-the-document-processing-and-monitoring-tasks"></a>Búðu til og tímasettu tvær runuvinnslur fyrir skjalavinnslu og eftirlitsverk

> [!NOTE]
> Í Commerce útgáfu 10.0.13 og nýrri þarftu ekki að stilla runuvinnslurnar í gegnum ramma runuvinnsla. Hægt er að stilla runuvinnslu úr valmyndinni **Smásala og viðskipti > Upplýsingatækni smásölu og viðskipta**. Notaðu **Eftirlit smásöluskjalsaðgerðar** og **Vinnsla smásöluskjalsaðgerðar** valkostina til að grunnstilla runuvinnslurnar.

Runuvinnslurnar sem þú býrð til verða notuð til að vinna úr skjölum sem takast ekki eða fá tímalokun. Þau verða einnig notuð þegar fjöldi virkra birgðaskjala sem unnið er úr POS er meiri en kerfisstillt gildi.

1. Farðu í **Kerfisstjórnun \> Fyrirspurnir \> Runuvinnslur**.
2. Á síðunni **Runuvinnsla** stofnarðu tvær runuvinnslur:

    - Stilltu eina vinnslu til að keyra klasann **RetailDocumentOperationMonitorBatch**.
    - Stilltu hina vinnsluna til að keyra klasann **RetailDocumentOperationProcessingBatch**.

2. Tímasettu nýju runuvinnslurnar til að keyra endurtekið. Til dæmis, stilltu áætlunina þannig að vinnslurnar séu keyrðar á fimm mínútna fresti.

## <a name="prerequisite-add-inbound-operation-to-the-pos-screen-layout"></a>Forsenda: Bættu aðgerð á innleið við POS skjámyndina

Áður en fyrirtækið getur notað virknina aðgerð á heimleið verður það að stilla POS-aðgerðina **Aðgerð á innleið** í einni eða fleiri af þínum [POS-skjáuppsetningum](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts). Áður en þú setur nýja aðgerðina í framleiðsluumhverfi, vertu viss um að prófa hana rækilega og þjálfa notendur hennar til að nota hana.

## <a name="overview"></a>Yfirlit

Aðgerðin á innleið gerir notendum POS kleift að framkvæma eftirfarandi verk:

- Fáðu birgðir í lager verslunar úr annaðhvort staðfestum innkaupapöntunargögnum eða sendum flutningspöntunargögnum.
- Skoðaðu upplýsingar um sögulegar innhreyfingar á birgðum í sjö daga eftir að skjalið hefur verið móttekið að fullu.
- Búðu til nýjar beiðnir um flutningspöntun á innleið.

Þegar farið er af stað með aðgerð á innleið úr POS-forritinu birtist listasíðuyfirlit. Þessi skoðun sýnir opna innkaupapöntun og flutningspöntunargögn sem hafa birgðalínur sem áætlað er að berist núverandi verslun. Til að finna og velja tiltekið skjal geta notendur flett listanum eða notað leitaraðgerðina.

Listi yfir birgðaskjal á innleið hefur þrjá flipa:

- **Virk** - Þessi flipi sýnir skjöl sem eru að fullu eða að hluta til opin og sem innihalda línur eða magn á línum sem enn á eftir að taka á móti.
- **Drög** - Þessi flipi sýnir nýjar beiðnir um flutningspantanir á innleið sem verslunin hefur búið til. Samt sem áður hafa skjölin aðeins verið vistuð staðbundið. Þeim hefur ekki enn verið skilað til Commerce Headquarters til vinnslu.
- **Lokið** - Þessi flipi sýnir lista yfir innkaupapöntun eða flutningspöntunargögn sem verslunin hefur móttekið að fullu síðustu sjö daga. Þessi flipi er aðeins til upplýsingar. Allar upplýsingar um skjölin eru skrifvarin gögn fyrir verslunina.

Þegar þú skoðar skjöl á einhverjum flipa getur reiturinn **Staða** hjálpað þér að skilja það stig sem skjalið er í.

- **Drög** - Flutningspöntunarskjalið hefur aðeins verið vistað á staðnum í rásagagnagrunni verslunarinnar. Engar upplýsingar um beiðni um flutningspöntun hafa enn verið sendar í Commerce Headquarters.
- **Umbeðið** - Innkaupapöntunin eða millifærslupöntunin hefur verið stofnuð í Commerce Headquarters og er að fullu opin. Engar innhreyfingar hafa enn verið afgreiddar gagnvart skjalinu. Fyrir skjöl af gerð innkaupapöntunargagna geta móttökur byrjað hvenær sem er meðan staðan er **Umbeðið**.
- **Afhent að hluta** - Flutningspöntunarskjalið er með eina eða fleiri línur eða hluta af línumagni sem hafa verið sendar sem sendar eru af vöruhúsi á útleið. Þessar sendu línur eru tiltækar í gegnum aðgerðina á innleið.
- **Sent að fullu** - Flutningspöntunin hefur fengið allar línur sínar og allt línumagn bókað sem sent af vöruhúsi á útleið. Allt skjalið er tiltækt í gegnum aðgerðina á innleið.
- **Móttekið að hluta** - Sumar af línunum eða línumagninu á innkaupapöntuninni eða flutningspöntunarskjali hafa borist versluninni en sumar línur eru áfram opnar.
- **Móttekið að fullu** - Allar línur og magn á innkaupapöntuninni eða flutningspöntunarskjali hafa borist að fullu. Skjölin eru aðeins aðgengileg á flipanum **Lokið** og eru skrifvarin fyrir notendur verslunarinnar.
- **Í vinnslu** - Þessi staða er notuð til að upplýsa notendur tækisins um að annar notandi sé að vinna í skjalinu.
- **Hlé** - Þessi staða er sýnd eftir **Gera hlé á móttöku** er valinn til að stöðva móttökuferlið tímabundið.
- **Vinnsla í HQ** - Skjalið var sent til Commerce Headquarters úr POS-forritinu en það hefur ekki enn verið sent til Commerce Headquarters. Skjalið fer í gegnum ósamstillta bókunarvinnslu skjala. Eftir að skjalið hefur verið sent í Commerce Headquarters ætti að uppfæra stöðu þess í **Móttekið að fullu** eða **Móttekið að hluta**.
- **Vinnsla mistókst** - Skjalið var sent í Commerce Headquarters og hafnað. Glugginn **Upplýsingar** sýnir ástæðuna fyrir því að bókun tókst ekki. Breyta verður skjalinu til að laga gagnavillur og síðan verður að senda það aftur í Commerce Headquarters til vinnslu.

Þegar þú velur skjalalínu á listanum birtist glugginn **Upplýsingar**. Þessi gluggi sýnir frekari upplýsingar um skjalið, svo sem upplýsingar um sendingu og dagsetningu. Framvindustika sýnir hve margar vörur á enn eftir að vinna. Ef vinnsla skjalsins tókst ekki í Commerce Headquarters sýnir glugginn **Upplýsingar** einnig villuboð sem tengjast biluninni.

Þú getur valið á skjalasíðu skjalalistans **Upplýsingar um pöntun** á forritastikunni til að skoða upplýsingar um skjalið. Þú getur einnig virkjað innhreyfingavinnslu á gjaldgengum skjalalínum.

Á skjalalistasíðuskjánum er einnig hægt að búa til nýja beiðni um flutningspöntunarbeiðni fyrir verslun. Skjölin eru áfram í stöðunni **Drög** og hægt er að breyta þeim eða eyða þar til þeim er skilað til Commerce Headquarters til vinnslu. Eftir að þeim hefur verið skilað til Commerce Headquarters er ekki lengur hægt að breyta flutningspöntunarlínunum úr POS-forritinu.

## <a name="receiving-process"></a>Móttökuferli

Eftir að þú hefur valið innkaupapöntun eða flutnigspöntunarskjal á flipanum **Virkt** geturðu valið **Upplýsingar um pöntun** til að hefja móttökuferlið.

Sjálfgefið er að skjárinn **Móttekið núna** er sýndur. Þessi skoðun er fínstillt fyrir strikamerkjaskönnun. Hana má nota til að búa til lista yfir vörur sem hafa verið skannaðar, svo hægt sé að taka á móti þessum vörum. Til að hefja móttökuferlið geturðu byrjað að skanna strikamerki á vörum.

Þar sem strikamerki á vörum eru skönnuð á skjánum **Móttekið núna** sannprófar forritið vörurnar gegn völdu innkaupa- eða flutningspöntunarskjali, til að ganga úr skugga um að hver skönnuð vara samsvari gildri vöru í skjalinu. Á skjánum **Móttekið núna** er gert ráð fyrir að hver skönnun á strikamerki tákni móttöku magns einnar einingar nema magn sé fellt inn í strikamerkið. Þú getur ítrekað skannað strikamerki í þessari sýn til að búa til lista yfir allar vörur og magn fyrir innhreyfinguna.

### <a name="example-scenario"></a>Dæmi

Notandi fær innkaupapöntun sem inniheldur 10 einingar af strikamerkinu 5657900266. Notandinn getur skannað þetta strikamerki 10 sinnum til að uppfæra reitinn **Móttekið núna** um eina einingu á hverri skönnun. Þegar notandinn hefur lokið að skanna sýnir reiturinn **Móttekur núna** fyrir línu hlutarins að magn upp á 10 var móttekið.

Að öðrum kosti, í atburðarás þar sem vörumagn er mikið, gæti notandi valið að slá inn magnið handvirkt í stað þess að skanna strikamerkið fyrir hvern hlut sem er móttekinn. Í þessu tilfelli getur notandinn skannað strikamerkið einu sinni til að bæta vörunni við listann **Móttekið núna**. Notandinn getur síðan valið tengda línu á skjánum **Móttekið núna** og síðan í glugganum **Upplýsingar** sem birtist hægra megin á síðunni, skaltu uppfæra reitinn **Móttekið magn** fyrir vöruna.

Þó að skjárinn **Móttekið núna** sé fínstilltur fyrir strikamerkjaskönnun geta notendur einnig valið **Taka á móti vöru** á forritastikunni og síðan slegið inn kenni vörunnar eða strikamerkjagögn í gegnum glugga. Þegar varan sem var slegin inn hefur verið staðfest er notandinn beðinn um að slá inn innhreyfingarmagn.

Skjárinn **Móttekið núna** veitir markvissa leið fyrir notendur að sjá hvaða vörur þeir eru að taka við. Að öðrum kosti er hægt að nota skjáinn **Fullur pöntunarlisti**. Þessi skjár sýnir allan listann yfir skjalalínur fyrir valið kaup- eða flutningspöntunarskjal. Notendur geta valið línur handvirkt á listanum og síðan í glugganum **Upplýsingar** skaltu uppfæra reitinn **Móttekið magn** fyrir valda línu. Á skjánum **Fullur pöntunarlisti** geta notendur skannað strikamerki eða þeir geta notað virknina **Taka á móti vöru** til að slá inn vörukenni eða strikamerki og gögn um móttekið magn, án þess að þurfa fyrst að velja samsvarandi vörulínu á listanum.

### <a name="over-receiving-validations"></a>Staðfestingar á ofmóttöku

Villuleitir eiga sér stað í móttökuferli skjalalínanna. Þær fela í sér staðfestingar vegna ofafhendingar. Ef notandi reynir að fá meiri birgðir en pantað var í innkaupapöntun, en annaðhvort er ofafhending ekki stillt eða upphæðin sem er móttekin fer fram úr vikmörkum ofafhendingar sem eru stilltar fyrir innkaupapöntunarlínuna, fær notandinn villu og er ekki leyft að taka á móti umframmagni.

Ofmóttaka er ekki leyfð fyrir flutningspöntunargögn. Notendur munu alltaf fá villur ef þeir reyna að móttaka meira en var sent fyrir flutningspöntunarlínuna.

### <a name="close-purchase-order-lines"></a>Loka innkaupapöntunarlínum

Hægt er að loka eftirstandandi magni í innkaupapöntun á innleið í móttökuferlinu ef farmsendandi hefur staðfest að hann geti ekki sent allt magnið sem beðið var um. Til að gera það þarf að skilgreina fyrirtækið til að leyfa vanafhendingu innkaupapantana. Þar að auki verður að skilgreina vikmarkaprósentu vanafhendingar fyrir innkaupapöntunarlínuna.

Til að skilgreina fyrirtækið þannig að það leyfi vanafhendingu innkaupapantana í höfuðstöðvum Commerce skal farið í **Innkaup og aðföng** > **Uppsetning** > **Færibreytur innkaupa og aðfanga**. Í flipanum **Afhending** skal kveikja á færibreytunni **Samþykkja vanafhendingu**. Keyrið síðan dreifingaráætlunarverkið **1070** (**Skilgreining rásar**) til að samstilla breytingar á stillingum við rásir.

Vikmarkaprósenta vanafhendingar fyrir flutningspöntunarlínu getur verið fyrirframskilgreind á afurðum sem hluti af skilgreiningum afurða í Commerce Headquarters. Að öðrum kosti er hægt að stilla eða skrifa yfir hana í tiltekinni flutningspöntun í gegnum Commerce Headquarters.

Eftir að fyrirtæki lýkur skilgreiningum á vanafhendingu innkaupapöntunar, sjá notendur sölustaðar nýja valkostinn **Loka eftirstandandi magni** í glugganum **Upplýsingar** þegar innkaupapöntunarlína á innleið er valin í aðgerðinni **Birgðir á innleið**. Ef notandinn lokar eftirstandandi magni, framkvæmir sölustaðurinn villuleit til að staðfesta hvort magnið sem var lokað er innan vikmarkaprósentu vanafhendingar sem er skilgreind í innkaupapöntunarlínunni. Ef farið er yfir vikmörk vanafhendingar birtast villuboð og notandinn mun ekki geta lokað eftirstandandi magni fyrr en áður sent magn ásamt magninu **Móttekur núna** uppfyllir eða fer yfir lágmarkið sem þarf að taka á móti samkvæmt vikmarkaprósentu vanafhendingar. 

Með kveikt á valkostinum **Loka eftirstandandi magni** fyrir innkaupapöntunarlínu, þegar notandinn lýkur móttöku með því að nota aðgerðina **Ljúka við móttöku**, er lokunarbeiðni einnig send til Commerce Headquarters og hætt verður við allt magn sem ekki hefur verið móttekið fyrir þessa pöntunarlínu. Á þeim tímapunkti er litið á línuna sem móttekna að fullu. 

### <a name="receiving-location-controlled-items"></a>Móttaka á staðstýrðir vörum

Ef vörurnar sem eru mótteknar eru staðstýrðar geta notendur valið staðsetningu þar sem þeir vilja móttaka vörurnar á meðan á móttökuferlinu stendur. Við mælum með að þú stillir sjálfgefna staðsetningu móttöku fyrir vöruhúsið til að gera þetta ferli skilvirkara. Jafnvel þó að sjálfgefin staðsetning sé stillt geta notendur hnekkt staðsetningu móttöku á völdum línum eins og þeir þurfa.

Aðgerðin virðir stillingar **Auð innhreyfing heimil** á geymsluvíddina **Staðsetningu** og þarf ekki að setja staðsetningarvídd ef auða innhreyfingin er stillt. Ef auðar innhreyfingarstaðsetningar eru ekki leyfðir fyrir vöru sýnir POS-forritið villu og krefst þess að staðsetning sé færð inn áður en hægt er að bóka innhreyfinguna.

### <a name="receive-all"></a>Taka við öllu

Þú getur valið eins og þú þarft **Taka við öllu** á forritastikunni til að uppfæra fljótt magnið **Móttekið núna** fyrir allar skjalalínur að hámarksgildi sem er tiltækt til móttöku fyrir þessar línur.

### <a name="receipt-of-unplanned-items-on-purchase-orders"></a>Kvittun fyrir móttöku óáætlaðra atriða í innkaupapöntunum

Í Commerce útgáfu 10.0.14 og nýrri geta notendur tekið á móti vöru sem ekki var upphaflega á innkaupapöntuninni. Til að virkja þennan valkost skaltu kveikja á **Bæta línum við innkaupapöntun við móttöku sölustaðar**.  

Þessi eiginleiki virkar aðeins fyrir móttöku innkaupapantana. Ekki er hægt að taka á móti vörum gegn flutningspöntunum þegar vörur voru ekki áður pantaðar og sendar úr vöruhúsi á útleið.

Notendur geta ekki bætt nýjum afurðum við innkaupapöntunina meðan á móttöku á sölustað stendur ef innkaupapöntun [breyta verkflæði](https://docs.microsoft.com/dynamics365/supply-chain/procurement/purchase-order-approval-confirmation) er virkjuð í Commerce Headquarters (HQ). Til að virkja breytingastjórnun verður fyrst að samþykkja allar breytingar á innkaupapöntun áður en móttaka er leyfð. Vegna þess að þetta ferli gerir viðtakanda kleift að bæta nýjum línum við innkaupapöntunina mun móttaka mistakast ef verkflæði breytingarstjórnunar er virkt. Ef breytingastjórnun er virkjuð fyrir allar innkaupapantanir eða lánardrottinn sem tengist innkaupapöntuninni sem tekið er á móti í sölustað getur notandinn ekki bætt nýjum afurðum við innkaupapöntunina við móttöku í sölustað.

Ekki er hægt að nota eiginleikann sem bætir við línum til að taka á móti viðbótarmagni afurða sem eru þegar á innkaupapöntuninni. Umframmóttöku er stjórnað í gegnum staðlaða stillingar [umframmóttöku](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation#over-receiving-validations) fyrir vörulínuna á innkaupapöntuninni.

Ef **Bæta línum við innkaupapöntun við móttöku sölustaðar** er virkt og notandi tekur á móti með **Aðgerð á innleið** á sölustað, ef notandi skannar eða slær inn strikamerki eða vörunúmer sem ekki hefur verið skráð sem vara á innkaupapöntuninni, en er viðurkennd sem gild vara, fær notandinn skilaboð um að bæta vörunni við innkaupapöntunina. Ef notandinn bætir vörunni við innkaupapöntunina er magnið sem fært er inn í **Móttaka núna** talið pöntunarmagn fyrir innkaupapöntunarlínuna.

Þegar innkaupapöntunarkvittunin er tilbúin og hún send inn til HQ fyrir vinnslu eru viðbótarlínur stofnaðar í aðalskjali innkaupapöntunar. Á innkaupapöntunarlínunni í HQ verður **Bætt við af móttöku sölustaðar** flagg á flipanum **Almennt** á innkaupapöntunarlínunni. **Bætt við af móttöku sölustaðar** flaggið gefur til kynna að innkaupapöntunarlínunni hafi verið bætt við móttökuferli sölustaðarins og hafi ekki verið lína sem var á innkaupapöntuninni á undan móttöku.

### <a name="cancel-receiving"></a>Hætta við móttöku

Þú ættir aðeins að nota virknina **Hætta við móttöku** á forritastikunni ef þú vilt fara út úr skjalinu og vilt ekki vista neinar breytingar. Til dæmis valdir þú upphaflega rangt skjal og vilt ekki að nein fyrri móttökugögn séu vistuð.

### <a name="pause-receiving"></a>Gera hlé á móttöku

Ef þú ert að taka á móti birgðum geturðu notað virknina **Gera hlé á móttöku** ef þú vilt gera hlé á móttökuferlinu. Til dæmis gætirðu viljað framkvæma aðra aðgerð úr POS, eins og að hringja í sölu viðskiptavina eða seinka bókun á innhreyfingunni.

Þegar þú velur **Gera hlé á móttöku** er stöðu skjalsins er breytt í **Hlé**. Þess vegna munu notendur vita að gögn hafa verið færð inn fyrir skjalið en skjalið hefur ekki enn verið sent. Þegar þú ert tilbúin/n að halda móttökuferlinu áfram skaltu velja skjalið í bið og velja síðan **Upplýsingar um pöntun**. Öllu magni í **Móttekið núna** sem áður var vistað er haldið og hægt að skoða það af skjánum **Fullur pöntunarlisti**.

### <a name="review"></a>Endurskoða

Á undan endanlegri ráðstöfun á innhreyfingunni til Commerce Headquarters, er hægt að nota skoðunarvirknina til að villuleita skjal á innleið. Skoðunin lætur vita um gögn sem annaðhvort vantar eða eru röng og geta valdið villum við úrvinnslu og gefið færi á því að leiðrétta vandamál áður en innhreyfingarbeiðnin er send inn. Til að virkja aðgerðina **Endurskoða** í forritastikunni, skal virkja eiginleikann **Virkja sannprófun í birgðaaðgerðum á innleið og útleið í sölustað** í gegnum vinnusvæðið **Eiginleikastjórnun** í Commerce Headquarters.

Aðgerðin **Endurskoða** villuleitar eftirfarandi atriði í skjali á innleið:

- **Umframmótaka** - móttekið magn er meira en pantað magn. Alvarleiki þessa máls ákvarðast af skilgreiningu umframafhendingar í Commerce Headquarters.
- **Undirmóttaka** – móttekið magn er minna en pantað magn. Alvarleiki þessa máls ákvarðast af skilgreiningu undirafhendingar í Commerce Headquarters.
- **Raðnúmer** – raðnúmerið er ekki gefið upp eða staðfest fyrir raðaða vöru sem þarf raðnúmer til að vera skráð í birgðum.
- **Staðsetning ekki stillt** - staðsetningin er ekki tilgreind fyrir staðsetningarstýrða vöru þar sem auð staðsetning er ekki leyfð.
- **Eyddar línur** – pöntunin er með línur sem notandi Commerce Headquarters, sem forrit sölustaðar þekkir ekki, hefur eytt.

Stillið færibreytuna **Virkja sjálfvirka villuleit** á **Já** í **Færibreytur Commerce** > **Birgðir** > **Birgðir verslunar** til að villuleitin verði keyrð sjálfkrafa þegar **Ljúka við móttöku** er valið.

### <a name="finish-receiving"></a>Ljúka við móttöku

Þegar búið er að slá inn allt magn **Móttekið núna** fyrir afurðir verður að velja **Ljúka móttöku** á forritastikunni til að vinna innhreyfinguna.

Þegar notendur ganga frá innhreyfingu innkaupapöntunar eru þeir beðnir um að slá inn gildi í reitinn **Kvittunarnúmer**, ef þessi aðgerð er stillt. Venjulega jafngildir þetta gildi auðkenni fylgiseðils söluaðilans. **Kvittunarnúmersgögn** verða geymd í dagbók vörukvittunar í Commerce Headquarters. Kvittunarnúmer eru ekki tekin fyrir kvittanir fyrir flutningspöntun.

Þegar vinnsla á samstillingu skjala er notuð er kvittunin send í gegnum ósamstilltan skjalaramma. Tíminn sem skjalið tekur í bókun fer eftir stærð skjalsins (fjölda lína) og almennri vinnsluumferð sem á sér stað á netþjóninum. Yfirleitt á þetta ferli sér stað á nokkrum sekúndum. Ef bókun skjals tekst ekki er notandanum tilkynnt um það á skjalalistanum **Aðgerð á innleið**, þar sem staða skjals verður uppfærð í **Vinnsla mistókst**. Notandinn getur síðan valið bilað skjal í POS til að skoða villuboðin og ástæðuna fyrir biluninni í glugganum **Upplýsingar**. Skjal sem ekki tókst verður ekki bókað og krefst þess að notandinn fari aftur í skjalalínurnar með því að velja **Upplýsingar um pöntun** í POS. Notandinn verður síðan að uppfæra skjalið með leiðréttingum, byggt á villunum. Eftir að skjal hefur verið leiðrétt getur notandinn reynt aftur að vinna það með því að velja **Ljúka uppfyllingu** á forritastikunni.

## <a name="create-an-inbound-transfer-order"></a>Stofna flutningspöntun á innleið

Frá POS geta notendur búið til ný flutningspöntunarskjöl. Til að hefja ferið velurðu **Nýtt** á forritastikunni á meðan þú ert í aðalskjalalistanum **Aðgerð á innleið**. Síðan færðu kvaðningu um að velja **Flytja úr** vöruhús eða verslun sem veitir birgðir til versunar þinnar. Gildin takmarkast við valið sem er skilgreint í stillingu uppfyllingarhóps verslunarinnar. Í flutningsbeiðni á innleið verður núverandi verslun þín alltaf **Flytja til** vöruhúsið fyrir flutningspöntunina. Ekki er hægt að breyta því gildi.

Þú getur slegið inn gildi í reitina **Sendingardagsetning**, **Móttökudagsetning** og **Afhendingarmáti** eftir þörfum. Þú getur líka bætt við athugasemd sem verður geymd ásamt flutningspöntunarhausnum, sem viðhengi við skjalið í Commerce Headquarters.

Þegar hausupplýsingar hafa verið stofnaðar geturðu bætt afurðum við flutningspöntunina. Til að hefja ferlið við að bæta vörum við og umbeðnu magni skaltu velja **Bættu við afurð**. Í glugganum **Upplýsingar**, þú getur líka bætt línusértækri athugasemd við dagbókarlínurnar. Þessar athugasemdir verða geymdar sem viðhengi við línuna.

Eftir að línur eru færðar í flutningspöntunina á innleið verður þú að velja **Vista** til að vista breytingar á skjali staðbundið eða **Senda inn beiðni** til að skila pöntunarupplýsingum til Commerce Headquarters til frekari vinnslu. Ef þú velur **Vista** eru drög að skjali geymd í gagnagrunni rásarinnar og vöruhús á útleið getur ekki keyrt skjalið fyrr en það hefur verið unnið með **Senda inn beiðni**. Þú ættir aðeins að velja **Vista** ef þú ert ekki tilbúin/n að senda beiðnina til Commerce Headquarters til vinnslu.

Ef skjal er vistað á staðnum er hægt að finna það á flipanum **Drög** á skjalalistanum **Aðgerð á innleið**. Meðan skjal er í stöðunni **Drög** er hægt að breyta því með því að velja **Breyta**. Þú getur uppfært, bætt við eða eytt línum eins og þú þarft. Þú getur líka eytt öllu skjalinu meðan það er í stöðunni **Drög** með því að velja **Eyða** á flipanum **Drög**.

Eftir að drögum að skjali hefur verið skilað til Commerce Headquarters birtast þau á flipanum **Virkt** og hafa stöðu **Umbeðið**. Á þessum tímapunkti geta notendur verslunar eða vöruhúss á innleið ekki lengur breytt umbeðnu pöntunarskjali fyrir innleið. Aðeins notendur á útleið vörugeymslu geta breytt skjalinu með því að velja **Aðgerð á útleið** í POS forritinu. Breytingalásinn tryggir að engin árekstrar eiga sér stað vegna þess að beiðandi á innleið breytir flutningspöntuninni um leið og sendandi á útleið er virkt að taka til og senda pöntunina. Ef þörf er á breytingum úr verslun eða vöruhúsi á innleið eftir að flutningspöntunin hefur verið send inn skal hafa samband við sendanda á útleið og biðja viðkomandi að færa inn breytingarnar.

Þegar skjalið er komið í stöðuna **Umbeðið** er það sýnilegt á flipnum **Virkt**. Hins vegar er ekki enn hægt að taka á móti því í verslun eða vöruhús á innleið. Þegar vöruhús á útleið hefur sent hluta eða alla flutningspöntunina getur verslunin eða vöruhúsið á innleið bókað innhreyfingar í POS. Þegar útleiðarhliðin keyrir flutningspöntunargögnin er staða þeirra uppfærð úr **Umbeðið** á **Sent** eða **Sent að hluta**. Þegar skjölin eru komin í stöðuna **Sent** eða **Afhent að hluta** getur verslun eða vöruhús á innleið sent kvittanir á móti þeim með því að nota móttökuferli aðgerðar á innleið.

## <a name="related-topics"></a>Tengd efnisatriði

[Birgðaaðgerð á útleið á sölustað](pos-outbound-inventory-operation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]