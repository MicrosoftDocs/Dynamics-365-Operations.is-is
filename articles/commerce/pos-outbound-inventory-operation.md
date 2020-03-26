---
title: Útleið birgðaaðgerð í POS
description: Þetta efni lýsir getu sölustaðar (POS) á útleið birgðaaðgerð.
author: hhaines
manager: annbe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 26d8d67ac6d2fde0753104483fd2127f9acbaa05
ms.sourcegitcommit: 437170338c49b61bba58f822f8494095ea1308c2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/12/2020
ms.locfileid: "3123923"
---
# <a name="outbound-inventory-operation-in-pos"></a>Útleið birgðaaðgerð í POS

[!include [banner](includes/banner.md)]


Í Microsoft Dynamics 365 Commerce útgáfu 10.0.10 og síðar, koma aðgerðir á innleið og útleið á sölustað (POS) í stað tiltektar- og móttökuaðgerðar.

> [!NOTE]
> Í útgáfu 10.0.10 og nýrri verður öllum nýjum eiginleikum í POS-forritinu sem tengjast því að taka á móti birgðum verslunar gegn innkaupapöntunum og millifærslupöntunum bætt við aðgerðina Aðgerð á innleið. Ef þú ert að nota tiltektar- og móttökuaðgerðina í POS mælum við með að þú þróir stefnu til að fara frá þeirri aðgerð yfir í nýju aðgerðirnar á inn- og útleið. Þó að tiltektar- og móttökuaðgerðin verði ekki fjarlægð úr vörunni verða engar frekari fjárfestingar í henni, frá sjónarhorni virkni eða afköstum, eftir útgáfu 10.0.9.

## <a name="prerequisite-configure-an-asynchronous-document-framework"></a>Forsenda: Stilla ósamstilltan skjalaramma

Aðgerðin á útleið felur í sér afköst til að tryggja að notendur sem hafa mikið magn bókana á innhreyfingum í mörgum verslunum eða fyrirtækjum og stór birgðaskjöl geti afgreitt þessi skjöl í Commerce Headquarters án þess að lenda í tímalokun eða bilun. Þessar endurbætur þurfa að nota ósamstilltan skjalaramma.

Þegar ósamstilltur skjalarammi er notaður getur þú framkvæmt breytingar á skjali á útleið úr POS í Commerce Headquarters og síðan haldið áfram í önnur verkefni meðan vinnslan í Commerce Headquarters fer fram í bakgrunni. Þú getur athugað stöðu skjalsins í gegnum skjalalistasíðuna **Aðgerð á útleið** í POS til að ganga úr skugga um að bókun hafi gengið vel. Í POS-forritinu geturðu einnig notað virkan skjalalista aðgerðar á útleið til að sjá öll skjöl sem ekki var hægt að bóka í Commerce Headquarters. Ef skjal tekst ekki geta notendur POS gert leiðréttingar á því og reynt aftur að vinna úr því í Commerce Headquarters.

> [!IMPORTANT]
> Setja þarf upp ósamstillta skjalaramma áður en fyrirtæki reynir að nota aðgerð á útleið í POS.

Til að stilla ósamstilltan skjalaramma skaltu ljúka eftirfarandi verklagsreglum.

### <a name="create-and-configure-a-number-sequence"></a>Stofna og skilgreina númeraröð

1. Farðu á **Fyrirtækisstjórnun \> Númeraröð \> Númeraraðir**.
2. Á síðunni **Númeraraðir** skaltu stofna númeraröð.
3. Í reitina **Kóði númeraraðar** og **Heiti** slærðu inn notendaskilgreind gildi.
4. Á flýtiflipanum **Tilvísanir** velurðu **Bæta við**.
5. Í reitnum **Svæði** velurðu **Viðskiptafæribreytur**.
6. Í reitnum **Tilvísun** velurðu **Skjalakenni smásöluaðgerða**.
7. Á flýtflipanum **Almennt**, í hlutanum **Uppsetning**, stillirðu valkostinn **Samfellt** á **Nei** til að tryggja að engin vandamál séu með afköst.

### <a name="create-and-schedule-two-batch-jobs-for-the-document-processing-and-monitoring-tasks"></a>Búðu til og tímasettu tvær runuvinnslur fyrir skjalavinnslu og eftirlitsverk

Runuvinnslurnar sem þú býrð til verða notuð til að vinna úr skjölum sem takast ekki eða fá tímalokun. Þau verða einnig notuð þegar fjöldi virkra birgðaskjala sem unnið er úr POS er meiri en kerfisstillt gildi.

1. Farðu í **Kerfisstjórnun \> Fyrirspurnir \> Runuvinnslur**.
2. Á síðunni **Runuvinnsla** stofnarðu tvær runuvinnslur:

    - Stilltu eina vinnslu til að keyra klasann **RetailDocumentOperationMonitorBatch**.
    - Stilltu hina vinnsluna til að keyra klasann **RetailDocumentOperationProcessingBatch**.

3. Tímasettu nýju runuvinnslurnar til að keyra endurtekið. Til dæmis, stilltu áætlunina þannig að vinnslurnar séu keyrðar á fimm mínútna fresti.

## <a name="prerequisite-add-outbound-operation-to-the-pos-screen-layout"></a>Forsenda: Bættu aðgerð á útleið við POS skjámyndina

Áður en fyrirtækið getur notað virknina aðgerð á útleið verður það að stilla POS-aðgerðina **Aðgerð á útleið** í einni eða fleiri af þínum [POS-skjáuppsetningum](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts). Áður en þú setur nýja aðgerðina í framleiðsluumhverfi, vertu viss um að prófa hana rækilega og þjálfa notendur hennar til að nota hana.

## <a name="overview"></a>Yfirlit

Aðgerðin á útleið gerir notendum POS kleift að framkvæma eftirfarandi verk:

- Bóka sendingar fyrir flutningspöntunargögn í tilvikum þar sem verslun notandans er tilnefnt vöruhús á útleið.
- Skoða upplýsingar um sögulegar flutningspöntunarsendingar sem voru bókaðar af versluninni.
- Búðu til nýjar beiðnir um flutningspöntun á útleið.

Þegar farið er af stað með aðgerð á útleið úr POS-forritinu birtist listasíðuyfirlit. Þessi skoðun sýnir opna flutningspöntunarskjöl sem hafa birgðalínur sem núverandi verslun notanda er ætlað að senda og uppfylla. Til að finna og velja tiltekið skjal geta notendur flett listanum eða notað leitaraðgerðina.

Listi yfir birgðaskjal á útleið hefur þrjá flipa.

- **Virkt** - Þessi flipi sýnir flutningspantanir sem hafa stöðu **Umbeðið** eða **Afhent að hluta**. Pantanirnar innihalda línur eða magn á línum sem verður að senda með núverandi verslun notandans. Þessi flipi sýnir einnig pantanir sem hafa stöðu **Vinnsla í HQ** (það er, þær bíða staðfestingar um að bókun hafi tekist frá Commerce Headquarters) eða **Vinnsla mistókst** (þ.e.a.s. bókun í Commerce Headquarters tókst ekki og notandinn verður að leiðrétta gögn og reyna aftur að senda pantanirnar).
- **Drög** - Þessi flipi sýnir nýjar beiðnir um flutningspantanir á útleið sem verslun notanda hefur búið til. Samt sem áður hafa skjölin aðeins verið vistuð staðbundið. Þeim hefur ekki enn verið skilað til Commerce Headquarters til vinnslu.
- **Lokið** - Þessi flipi sýnir lista yfir flutningspöntunargögn sem verslunin hefur sent að fullu síðustu sjö daga. Þessi flipi er aðeins til upplýsingar. Allar upplýsingar um skjölin eru skrifvarin gögn fyrir verslunina.

Þegar þú skoðar skjöl á einhverjum flipa getur reiturinn **Staða** hjálpað þér að skilja það stig sem skjalið er í.

- **Drög** - Flutningspöntunarskjalið hefur aðeins verið vistað á staðnum í rásagagnagrunni verslunarinnar. Engar upplýsingar um beiðni um flutningspöntun hafa enn verið sendar í Commerce Headquarters.
- **Umbeðið** - Innkaupapöntunin eða millifærslupöntunin hefur verið stofnuð í Commerce Headquarters og er að fullu opin. Núverandi verslun notandans hefur ekki enn afgreitt neinar sendingar gegn skjalinu.
- **Afhent að hluta** - Flutningspöntunarskjalið er með eina eða fleiri línur eða hluta af línumagni sem hafa verið sendar sem sendar eru af vöruhúsi á útleið. Þessar sendu línur eru tiltækar í gegnum aðgerðina á innleið.
- **Sent að fullu** - Flutningspöntunin hefur fengið allar línur sínar og allt línumagn bókað sem sent af vöruhúsi á útleið.
- **Í vinnslu** - Þessi staða er notuð til að upplýsa notendur tækisins um að annar notandi sé að vinna í skjalinu.
- **Hlé** - Þessi staða er sýnd eftir **Gera hlé á móttöku** er valinn til að stöðva móttökuferlið tímabundið.
- **Vinnsla í HQ** - Skjalið var sent til Commerce Headquarters úr POS-forritinu en það hefur ekki enn verið sent til Commerce Headquarters. Skjalið fer í gegnum ósamstillta bókunarvinnslu skjala. Eftir að skjalið hefur verið sent í Commerce Headquarters ætti að uppfæra stöðu þess í **Móttekið að fullu** eða **Móttekið að hluta**.
- **Vinnsla mistókst** - Skjalið var sent í Commerce Headquarters og hafnað. Glugginn **Upplýsingar** sýnir ástæðuna fyrir því að bókun tókst ekki. Breyta verður skjalinu til að laga gagnavillur og síðan verður að senda það aftur í Commerce Headquarters til vinnslu.

Þegar þú velur skjalalínu á listanum birtist glugginn **Upplýsingar**. Þessi gluggi sýnir frekari upplýsingar um skjalið, svo sem upplýsingar um sendingu og dagsetningu. Framvindustika sýnir hve margar vörur á enn eftir að vinna. Ef vinnsla skjalsins tókst ekki í Commerce Headquarters sýnir glugginn **Upplýsingar** einnig villuboð sem tengjast biluninni.

Þú getur valið á skjalasíðu skjalalistans **Upplýsingar um pöntun** á forritastikunni til að skoða upplýsingar um skjalið. Þú getur einnig virkjað innhreyfingavinnslu á gjaldgengum skjalalínum.

Á skjalalistasíðuskjánum er einnig hægt að búa til nýja beiðni um flutningspöntun á útleið fyrir verslun.

## <a name="transfer-order-shipping-process"></a>Móttökuferli sendingarpöntunar

Eftir að þú hefur valið flutnigspöntunarskjal á flipanum **Virkt** geturðu valið **Upplýsingar um pöntun** til að hefja uppfyllingarferlið. Skjárinn **Fullur pöntunarlisti** birtist. Þessi síða sýnir allar skjalalínur sem innihalda vöruna. Hún sýnir einnig upplýsingar um pantað magn.

Hver skönnun á strikamerki uppfærir magnið í reitnum **Sendingar núna** um eina einingu. Einnig er hægt að færa inn sendingarmagn með því að velja **Senda afurð** á forritastikunni, slá inn vörukenni og slá síðan inn magnið. Ef varan er staðsetningarstýrð geturðu staðfest eða stillt sendingarstað fyrir skjalalínuna.

Í skjánum **Fullur pöntunarlisti** er hægt að velja línu handvirkt á listanum og uppfæra síðan magnið **Sendingar núna** fyrir valda línu í glugganum **Upplýsingar**.

### <a name="over-delivery-shipping-validations"></a>Staðfestingar á sendingum ofafhendingar

Villuleitir eiga sér stað í móttökuferli skjalalínanna. Þær fela í sér staðfestingar vegna ofafhendingar. Ef notandi reynir að fá meiri birgðir en pantað var í innkaupapöntun, en annaðhvort er ofafhending ekki stillt eða magnið sem er móttekið fer fram úr vikmörkum ofafhendingar sem eru stilltar fyrir innkaupapöntunarlínuna, fær notandinn villu og er ekki leyft að taka á móti umframmagni.

### <a name="shipping-location-controlled-items"></a>Sending á staðstýrðir vörum

Ef vörurnar sem eru sendarr eru staðstýrðar geta notendur valið staðsetningu sem þeir vilja gefa út birgðir á meðan á sendingarferlinu stendur. Við mælum með að þú stillir sjálfgefna staðsetingu úthreyfinga fyrir vöruhúsið til að gera þetta ferli skilvirkara. Jafnvel þó að sjálfgefin staðsetning sé stillt geta notendur hnekkt staðsetningu útgáfunnar á völdum línum eins og þeir þurfa.

Aðgerðin virðir stillingar **Auð innhreyfing heimil** á geymsluvíddina **Staðsetningu** og þarf ekki að setja staðsetningarvídd ef auða innhreyfingin er stillt. Ef auðar innhreyfingarstaðsetningar eru ekki leyfðir fyrir vöru sýnir POS-forritið villu og krefst þess að staðsetning sé færð inn áður en hægt er að bóka innhreyfinguna.

### <a name="ship-all"></a>Senda allt

Þú getur valið eins og þú þarft **Senda allt** á forritastikunni til að uppfæra fljótt magnið **Sendingar núna** fyrir allar skjalalínur að hámarksgildi sem er tiltækt til að uppfylla fyrir þessar línur.

### <a name="cancel-fulfillment"></a>Hætta við uppfyllingu

Þú ættir aðeins að nota virknina **Hætta við uppfyllingu** á forritastikunni ef þú vilt fara út úr skjalinu og vilt ekki vista neinar breytingar. Til dæmis valdir þú upphaflega rangt skjal og vilt ekki að nein fyrri sendingargögn séu vistuð.

### <a name="pause-fulfillment"></a>Gera hlé á uppfyllingu

Ef þú ert að uppfylla flutningspöntunina geturðu notað virknina **Gera hlé á uppfyllingu** ef þú vilt gera hlé á ferlinu. Til dæmis gætirðu viljað framkvæma aðra aðgerð úr POS, eins og að hringja í sölu viðskiptavina eða seinka bókun sendingarinnar í Commerce Headquarters.

Þegar þú velur **Gera hlé á uppfyllingu** er stöðu skjalsins er breytt í **Hlé**. Þess vegna mun notandi vita að gögn hafa verið færð inn í skjalið en skjalið hefur ekki enn verið sent. Þegar þú ert tilbúin/n að halda uppfyllingarferlinu áfram skaltu velja skjalið í bið og velja síðan **Upplýsingar um pöntun**. Öllu magni í **Sendingar núna** sem áður var vistað verður haldið og hægt að skoða það af skjánum **Fullur pöntunarlisti**.

### <a name="finish-fulfillment"></a>Ljúka við uppfyllingu

Þegar búið er að slá inn allt magn **Sendingar núna** fyrir afurðir verður að velja **Ljúka uppfyllingu** á forritastikunni.

Þegar vinnsla á samstillingu skjala er notuð er kvittunin send í gegnum ósamstilltan skjalaramma. Tíminn sem skjalið tekur í bókun fer eftir stærð skjalsins (fjölda lína) og almennri vinnsluumferð sem á sér stað á netþjóninum. Yfirleitt á þetta ferli sér stað á nokkrum sekúndum. Ef bókun skjals tekst ekki er notandanum tilkynnt um það á skjalalistanum **Aðgerð á útleið** á flipanum **Virkt**, þar sem staða skjals verður uppfærð í **Vinnsla mistókst**. Notandinn getur síðan valið bilað skjal í POS til að skoða villuboðin og ástæðuna fyrir biluninni í glugganum **Upplýsingar**. Skjal sem ekki tókst verður ekki bókað og krefst þess að notandinn fari aftur í skjalalínurnar með því að velja **Upplýsingar um pöntun** í POS. Notandinn verður síðan að uppfæra skjalið með leiðréttingum, byggt á villunum. Eftir að skjal hefur verið leiðrétt getur notandinn reynt aftur að vinna það með því að velja **Ljúka uppfyllingu** á forritastikunni.

## <a name="create-an-outbound-transfer-order"></a>Stofna flutningspöntun á útleið

Frá POS geta notendur búið til ný flutningspöntunarskjöl. Til að hefja ferið velurðu **Nýtt** á forritastikunni á meðan þú ert í aðalskjalalistanum **Aðgerð á útleið**. Síðan færðu kvaðningu um að velja **Flytja til** vöruhús eða verslun sem núverandi verslun þín mun senda birgðir til. Gildin takmarkast við valið sem er skilgreint í stillingu uppfyllingarhóps verslunarinnar. Í flutningsbeiðni á útleið verður núverandi verslun þín alltaf **Flytja frá** vöruhúsið fyrir flutningspöntunina. Ekki er hægt að breyta því gildi.

Þú getur slegið inn gildi í reitina **Sendingardagsetning**, **Móttökudagsetning** og **Afhendingarmáti** eftir þörfum. Þú getur líka bætt við athugasemd sem verður geymd ásamt flutningspöntunarhausnum, sem viðhengi við skjalið í Commerce Headquarters.

Þegar hausupplýsingar hafa verið stofnaðar geturðu bætt afurðum við flutningspöntunina. Til að hefja ferlið við að bæta vörum við og umbeðnu magni skaltu skanna strikamerki eða velja **Bættu við afurð**.

Eftir að línur eru færðar í útflutningspöntunina verður þú að velja **Vista** til að vista breytingar á skjali staðbundið eða **Senda inn beiðni** til að skila pöntunarupplýsingum til Commerce Headquarters til frekari vinnslu. Ef þú velur **Vista** eru drög að skjali geymd í gagnagrunni rásarinnar og vöruhús á útleið getur ekki keyrt skjalið fyrr en það hefur verið unnið með **Senda inn beiðni**. Þú ættir aðeins að velja **Vista** ef þú ert ekki tilbúin/n að senda beiðnina til Commerce Headquarters til vinnslu.

Ef skjal er vistað á staðnum er hægt að finna það á flipanum **Drög** á skjalalistanum **Aðgerð á innleið**. Meðan skjal er í stöðunni **Drög** er hægt að breyta því með því að velja **Breyta**. Þú getur uppfært, bætt við eða eytt línum eins og þú þarft. Þú getur líka eytt öllu skjalinu meðan það er í stöðunni **Drög** með því að velja **Eyða** á flipanum **Drög**.

Eftir að drögum að skjali hefur verið skilað til Commerce Headquarters birtast þau á flipanum **Virkt** og hafa stöðu **Umbeðið**. Á þessum tímapunkti geta aðeins notendur á útleið vörugeymslu breytt skjalinu með því að velja **Aðgerð á útleið** í POS forritinu. Notendur í vöruhúsi á innleið geta skoðað flutningspöntunina á flipanum **Virkt** í skjalalistanum **Aðgerð á innleið**, en þeir geta ekki breytt eða eytt þeim. Breytingalásinn tryggir að engin árekstrar eiga sér stað vegna þess að beiðandi á innleið breytir flutningspöntuninni um leið og sendandi á útleið er virkt að taka til og senda pöntunina. Ef þörf er á breytingum úr verslun eða vöruhúsi á innleið eftir að flutningspöntunin hefur verið send inn skal hafa samband við sendanda á útleið og biðja viðkomandi að færa inn breytingarnar.

Þegar skjalið er komið í stöðuna **Umbeðið** er það tilbúið til fullnustuvinnslu af vöruhúsi á útleið. Þegar sendingin er afgreidd með aðgerð á útleið er staða flutningspöntunargagna uppfærð úr **Umbeðið** á **Sent að fullu** eða **Afhent að hluta**. Þegar skjölin eru komin í stöðuna **Sent að fullu** eða **Afhent að hluta** getur verslun eða vöruhús á innleið sent kvittanir á móti þeim með því að nota móttökuferli aðgerðar á innleið.

Flutningsskipanir sem eru að fullu sendar eru fluttar á flipann **Lokið** á skjalalistanum **Aðgerð á útleið**. Þar eru þær áfram sýnilegar notendum verslunar eða vöruhúss á útleið, í skrifvarnarham, í sjö daga.

## <a name="related-topics"></a>Tengd efnisatriði

[Innleið birgðaaðgerð í POS](pos-inbound-inventory-operation.md)
