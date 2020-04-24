---
title: Stjórnun afsláttar
description: Í þessu efnisatriði er stjórnun afsláttar fyrir Dynamics 365 Supply Chain Management lýst.
author: t-benebo
manager: tfehr
ms.date: 08/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: t-benebo
ms.search.validFrom: 2018-01-31
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 7fdcf8a7294d8c7579f35bc108bdd3804da9a837
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203248"
---
# <a name="trade-allowance-management"></a>Stjórnun afsláttar

[!include [banner](../includes/banner.md)]

Stjórnun afsláttar hjálpar fyrirtækjum að stjórna sölukynningaráætlunum sem bjóða viðskiptavinum, sem ná settum markmiðum hvað varðar magn og kauphegðun, upp á peningaumbun í formi „árangurstengdra greiðslna.“ Eiginleikinn er hannaður fyrir fyrirtæki sem leggja áherslu á alhliða ferli sem stuðla að hagnaði, frá fjárhagsáætlunargerð og úthlutun úr sölukynningarsjóði til uppsetningar á afsláttarsamningi, til stofnunar og úrvinnslu á kröfum, til greiðsluvinnslu, til greiningar á skilvirkni sölukynningar.


Þessi grein mun veita víðtæka yfirsýn yfir eiginleikann Stjórnun afsláttar og mun kynna þér fyrir dæmigerðum verkefnum sem eru hluti af umsjón sölukynningaráætlunar. Gert er ráð fyrir því að notendur af ýmsu tagi, sem bera ábyrgð á rekstri og ákvarðanatökum, noti þessa virkni til að ná fram markmiðum sínum:

- Úthluta valkvæðum sjóðum á valda reikninga og setja upp afsláttarsamninga fyrir sölukynningar, byggt á endurgreiðslum og eingreiðslum (fyrir samþykkta þjónustu)
- Keyra umsamda sölukynningarsamninga í gegnum yfirstandandi sölur og búa til endurgreiðslukröfur
- Reikna, samþykkja og meðhöndla kröfurnar sem eru búnar til og flytja þær yfir í Viðskiptakröfur sem frádrátt fyrir greiðslujöfnun
- Afstemma skammtímagreiðslu viðskiptavinar við gjaldfallinn frádrátt
- Fylgjast með notkun á sölukynningarsjóði og meta arðsemi og skilvirkni áætlunar

## <a name="audience-and-purpose"></a>Markhópur og tilgangur

Upplýsingar í þessari grein eru ætlaðar stjórnendum viðskipta í stórum fyrritækjum, í stöðum svo sem innkaupastjóri, yfirfjármálastjóri og yfirmaður bókhalds, sem hafa eftirfarandi skyldur:

- Stórar fjárhagsáætlanir og sjóðsúthlutun
- Skipuleggja og greina sölukynningar
- Stjórnun starfsmanna sem vinna með kröfur um endurgreiðslur, stjórna greiðslum á grundvelli smásölutilvika og sem gera upp skammtímagreiðslur og frádrætti

Fólk í þessum hlutverkum leitar leiða til að ná þessum markmiðum:

- Betra að nota markaðskynningarsjóði.
- Að mæta af sveigjanleika mismunandi gerðum markaðskynningaráætlana og afslátta.
- Að draga úr umsýslu og villum sem tengjast eftirliti með árangri af kynningu og úrvinnslu krafa.
- Að bæta sjóðsstreymisspá með því að taka saman gögn fyrir framtíðarskuldir.
- Að mynda mælanlegan grundvöll fyrir yfirstandandi og komandi samninga við viðskiptavini um markaðskynningar.

## <a name="promotional-fund-and-trade-allowance-agreement"></a>Kynningarsjóður og afsláttarsamningur

Afsláttarsamningur er hvatningaráætlun þar sem viðskiptavinum, sem ná markmiðum hvað varðar ákveðið magn og/eða kauphegðun, er boðin peningaumbun í formi árangurstengdra greiðslna. Kynningarsjóðir eru útgjöld í fjárhagsáætlun. Þannig er hægt að halda utan um kynningarherferðir.

### <a name="promotional-fund"></a>Kynningarsjóður

Sjóðum sem er úthlutað í afsláttarsamninga eru skráðir á síðunni **Sjóðir**. Til að opna síðuna **Sjóðir** skal velja **Sala og markaðssetning** \> **Afslættir** \> **Sjóðir** \> **Sjóðir**.

![Síðan Sjóðir](./media/trade-allowance-management-funds-page.png "Síðan Sjóðir")

Á síðunni **Sjóðir** er hægt að skoða upplýsingar um kynningarsjóði.

Flýtiflipinn **Almennt** sýnir tímabilið sem sjóðurinn er í gildi og upphæð hans í fjárhagsáætlun. Til þess að sjóðnum sé úthlutað í kynningarsamninginn verður reiturinn **Staða** að hafa gildið **Samþykkt**.

Flýtiflipinn **Viðskiptavinir** sýnir stigveldi viðskiptavina. Til að velja viðskiptavinina sem eru markhópur sjóðsins skal draga þá til svo þeir séu undir **Viðskiptavinir sjóðs**. Þessi flýtiflipi sýnir einnig hvernig heildarupphæð sjóðsins er dreift.

Flýtiflipinn **Hlutir** sýnir atriðin sem eru hluti af kynningunni.

### <a name="trade-allowance-agreement"></a>Afsláttarsamningur

Eftir að skilgreiningin á sjóðnum er til staðar, er næsta skref í áætlanagerð kynningar að skrá kynningarsamninga (sem eru þekktir sem afsláttarsamningar), úthluta fjármunum og skilgreina frammistöðumarkmið fyrir hvert smásölutilvik.

Afsláttarsamningar eru skráðir á síðunni **Afsláttarsamningar**. Til að opna síðuna **Afsláttarsamningar** skal velja **Sala og markaðssetning** \> **Afslættir** \> **Afsláttarsamningar**.

![Síðan Afsláttarsamningar](./media/trade-allowance-management-agreements-page.png "Síðan Afsláttarsamningar")

#### <a name="header"></a>Haus

Veldu **Haus** til að skipta yfir í Hausyfirlit.

Á flýtiflipanum **Almennt** skilgreina reitirnir **Panta til** og **Panta frá** tímabilið sem samningurinn er í gildi. Samþykkisstaða á **Innri samþykkt** fyrir samninginn gefur til kynna að samningurinn sé ekki ennþá gildur og ekki er hægt að nota hann í sölupöntunarferli.

Kaflinn **Greining** í flýtiflipanum **Almennt** inniheldur mikilvæga reiti sem skilgreina magn og kostnað sem er notað fyrir kynningarmat:

- Reiturinn **Grunneiningar** tilgreinir magn af vörum sem þarf að selja til valdra viðskiptavina áður en kynningin er notuð.
- Gildið **Reiknað sendingarmagn** er reiknað miðað við gildið **Aukningarprósenta** sem er áætluð markhækkun fyrir þessa kynningu.
- Reiturinn **Kostnaður afsláttar** er reiknaður miðað við magn af hinum ýmsu tilvikum í afsláttarsamningnum.

Í flýtiflipanum **Viðskiptavinir**, í listanum til vinstri, getur þú valið og skoðað viðskiptavinaflokka sem eru settir upp sem fyrirfram skilgreind stigveldi. Þú getur þá valið allt stigveldið eða tiltekna lykla sem mörk fyrir afsláttarsamninginn.

Í flýtiflipanum **Hlutir**, eins og í flýtiflipanum **Hlutir** á síðunni **Sjóðir**, eru vörum bætt við samninginn til að tengja sölurnar við afsláttinn sem var samþykktur.

Á flýtiflipanum **Sjóðir** er hægt að skoða kynningarsjóði sem tengjast þessum samningi. Einnig er hægt að skoða úthlutun á tilvikskostnaði samnings. 100 prósent úthlutun á tilvikskostnaði þýðir að þessi kynning verður fjármögnuð eingöngu úr einum sjóði. Önnur leið er að kynningarsamningur getur fengið úthlutun úr nokkrum sjóðum og getur notað sömu eða mismunandi prósentuúthlutun.

#### <a name="lines"></a>Línur

Næst skaltu velja **Línur** til að skipta yfir í línuyfirlit.

Flipinn **Smásölutilvik** sýnir gerðir tilvika sem falla undir samning. Til eru þrjár gerðir: endurgreiðsla, eingreiðsla og af reikningi.

Þegar þú velur smásölutilvik og velur síðan flipann **Upphæðir**, finnast upplýsingar um viðburðinn.

![Línur afsláttarsamninga](./media/trade-allowance-management-agreements-lines.png "Línur afsláttarsamninga")

Í kaflanum **Afsláttarlínur** tilgreinir þú magn eða upphæð á einhverju bili sem viðskiptavinurinn þarf að ná svo skilgreiningar fái umbunina.

Ef um er að ræða smásölutilvik af gerðinni **Endurgreiðsla** þá skilgreinir efri hluti flipans **Upphæðir** reglurnar þegar endurgreiðsla er notuð, búin til og greidd. Til dæmis geta reglurnar tilgreint eftirfarandi skilyrði fyrir endurgreiðslu kröfunnar:

- Það er byggt á stofndegi sölupöntunar (gildið **Gerð útreikningsdagsetningar** er **Stofnað**).
- Það er reiknað út frá upphæð sölupöntunarlínu fyrir afslætti, ekki nettóupphæð, sem felur í sér afslætti (gildið **Tekið frá** er **Brúttó**).
- Það er byggt á magni seldra vara, ekki upphæðar (gildið **Gerð línuskila endurgreidds afsláttar** er **Magn**).
- Það er reiknað á hvert mánaðartímabil (gildið **Safna upp sölu eftir** er **Mánuður**). 
- Það er gert upp sem frádráttur, ekki með því að nota viðskiptaskuldir (gildið **Greiðslugerð** er **Frádráttur viðskiptavinar**).

Ef um er að ræða smásölutilvik af gerðinni **Eingreiðsla** sýnir flipinn **Upphæðir** sýnir magnið sem verður greitt til viðskiptavinar í formi frádráttar þegar viðskiptavinurinn nær ákveðnum árangri. Samþykkisstaðan **Opin** gefur til kynna að eingreiðslan hefur ekki enn verið greidd.

Til að nota samninginn fyrir sölupantanir sem uppfylla skilyrði samningsins, verður staða samningsins að vera **Staðfest**. 

## <a name="perform-sales-under-the-planned-merchandising-event-and-generate-bill-back-claims"></a>Framkvæma sölur sem heyra undir áætluð smásölutilvik og búa til endurgreiðslukröfur

Þegar þú býrð til sölupantanir sem hafa línur sem uppfylla kröfur samningsins geturðu skoðað tengdar upplýsingar á síðunni **Sölupantanir** með því að velja **Sölupöntunarlína** \> **Skoða** \> **Upplýsingar um verð**.

Á síðunni **Upplýsingar um verð** á flýtiflipanum **Eftirágreiddir afslættir** getur sölumaðurinn séð endurgreiðslu út frá gildum afsláttarsamningi (auðkenni eftirágreidds afsláttar er sýnt) og heildarupphæðinni sem er notuð í línunni. Upphæðin birtist einnig í reitnum **Eftirágreiddur afsláttur lánardrottins** í kaflanum **Áætluð framlegð** á síðunni **Verðupplýsingar**.

Þegar sölureikningur er bókaður er samsvarandi endurgreiðslukrafa búin til fyrir hverja reikningslínu.

> [!NOTE]
> Til að sjá síðuna **Verðupplýsingar** á síðunni **Færibreytur viðskiptakrafna** í flipanum **Verð** velurðu gátreitinn **Virkja verðupplýsingar**. I

## <a name="process-claims-and-pass-them-as-deductions-to-ar"></a>Vinna úr kröfum og flytja þær sem frádrátt yfir í viðskiptakröfur

Næsta skref í því ferli við meðhöndlun endurgreiðslna er að endurskoða, reikna út og samþykkja kröfur og síðan umbreyta þeim í frádrátt.

Vinnusvæði endurgreiðslu er þar sem eigandi kynningarsamnings endurskoðar reglulega og vinnur úr kröfunum sem verða til. Það er líka þar sem stjórnendur viðskiptakrafna umbreyta samþykktum kröfum í frádrætti eða reglubundnar greiðslur, fer allt eftir greiðslumáta kröfunnar.

Á síðunni **Vinnusvæði endurgreiðslna** getur þú yfirfarið kröfulínur. Ef kröfur eru með stöðuna **Verða endurreiknaðar** verður að endurreikna þær fyrir öll uppsöfnuð áhrif.

### <a name="recalculate-claims"></a>Endurreikna kröfur

Til að endurreikna kröfurnar, á aðgerðasvæðinu, skal velja **Uppsafna**. Síðan skal í svarglugganum **Uppsafna eftirágreiddan afslátt** velja viðskiptavin.

Í kjölfar endurútreiknings býr forritið til nýjar kröfur fyrir upphæðirnar til að leiðrétta upphaflegu kröfurnar í nothæfa upphæð á hverja einingu. Ein leiðréttingarkrafa er mynduð fyrir hverja einkvæma samsetningu viðskiptavinar, hlutar, gjaldmiðils, mælieiningu, birgðavídda, fjárhagsvídda og VSK-flokks. Þessar leiðréttingarkröfur hafa sömu tilvísun í sölupöntun og númer reiknings eins og kröfurnar sem er verið að leiðrétta (það er þær kröfur sem upphaflega voru búnar til úr söluskjalinu). Ólíkt upphaflegu kröfunni hefur leiðréttingarkrafan ekki gildi í þeim reitum sem sýna upphæðir og magn í upprunalegu sölupöntunarlínunni.

Eftir að endurútreikningi er lokið er staða krafna breytt í **Reiknuð**. Til að samþykkja kröfurnar skaltu velja **Samþykkja** á aðgerðasvæðinu.

### <a name="process-claims-and-pass-them-to-ar"></a>Vinna úr kröfum og fara með þær í viðskiptakröfur

Kröfurnar eru nú tilbúnar til úrvinnslu í viðskiptakröfum. Til að vinna úr þeim skaltu velja **Úrvinnsla** á aðgerðasvæðinu. 

Við vinnslu krafna hefur staðan breyst í **Merkja** og gefur til kynna að bókun færslubókar (færslubókin sem er bókuð er færslubók fyrir uppsafnaðan eftirágreiddan afslátt, eins og tilgreint er í færibreytum viðskiptakrafna) hefur valdið því að eftirfarandi tilvik koma fyrir: 

- Kröfurnar hafa verið fluttar í tímabundna stöðu viðskiptavinar sem frádrættir.
- Uppsöfnunarlykill eftirágreidds afsláttar hefur verið kreditfærður til að tákna framtíðarskuldir fyrir viðskiptavininn.
- Kostnaðarlykill eftirágreidds afsláttar hefur verið debetfærður til að staðfesta kostnaðinn sem stofnað var til í tengslum við sölu.

Til að ljúka ferlinu verður starfsmaður viðskiptakrafna nú að sjá um uppsafnaða frádrætti með því að flytja þá yfir á stöðu viðskiptavina sem kreditnótu (skuld). 

Til að byrja verkefni, á aðgerðasvæðinu á síðunni **Viðskiptavinur**, skaltu velja **Safna** \> **Gera upp færslur**. Síðan, á síðunni **Gera upp færslur**, skaltu velja **Aðgerðir** \> **Endurgreiðsluáætlun**. Þessi síða eftirágreidds afsláttar sýnir allar endurgreiðslukröfur sem áður var unnið úr.

Ef þú vilt búa til kreditnótu skaltu velja gátreitinn **Merkja** fyrir alla línur og velja síðan **Aðgerðir** \> **Stofna kreditnótu**.

Við stofnun kreditnótu er færslubók bókuð. (Færslubókin sem er bókuð er notkunarbók viðskiptakrafna, eins og tilgreint er í færibreytum viðskiptakrafna.) Þess vegna hefur upphæð raunverulegrar skuldar (kredit) verið flutt í stöðu viðskiptavinar. Fjárhagslega þýðir þetta ástand að eftirfarandi atburðir hafi átt sér stað:

- Viðskiptakrafa viðskiptavinar hefur verið kreditfærð.
- Uppsöfnunarlykill eftirágreidds afsláttar hefur verið debetfærður.

Til að samþykkja smásölutilvik af gerðinni **Eingreiðsla** skaltu velja atburðinn á síðunni **Afsláttarsamningar** og síðan á flipanum **Upphæð** skaltu velja **Samþykkja**.

## <a name="settle-the-deduction-that-is-due-and-the-customer-short-pay-by-using-the-deduction-workbench"></a>Gerðu upp frádráttinn sem er á gjalddaga og skammtímagreiðslu viðskiptavinar með því að nota Frádráttarvinnusvæðið

Oft, í aðdraganda endurgreiðslna, velja viðskiptavinir að skammtímagreiða valda reikninga. Til að koma í veg fyrir vandamál við afstemmingu á greiðslu, skráir starfsmaður viðskiptakrafna þessar skammtímagreiðslur sem frádrætti þegar hann eða hún skráir raunverulegar greiðslur viðskiptavinar. Síðan, á Frádráttarvinnusvæðinu, er auðveldlega hægt að jafna þessa frádrætti viðskiptavinar á móti kröfuupphæðum fyrirtækis sem eru komnar á gjalddaga.

Til að skrá skammtímagreiðslu viðskiptavinar í greiðslubókinu skaltu velja **Viðskiptakröfur** \> **Greiðslur** \> **Greiðslubók** og búa til nýja greiðslubók. Í aðgerðasvæðinu er síðan smellt á **Frádrættir**. Á síðunni **Frádráttur** er hægt að búa til og fylgjast með upphæðinni sem var skammtímagreidd.

Yfirmaður söfnunar er nú ábyrgur fyrir því að jafna opnu kreditnótufærsluna og færslu skammtímagreiðslunnar á móti hvort öðru í Frádráttarvinnusvæðinu.

Til að stjórna frádráttum skaltu velja **Sala og markaðssetning** \> **Afslættir** \> **Frádrættir** \> **Frádráttarvinnusvæði**. Efri hluti síðunnar inniheldur línur sem tákna skammtímagreiðslur frá viðskiptavininum. Neðri hluti síðunnar inniheldur opnar kreditfærslur viðskiptavinar. 

Til að jafna frádráttinn á móti opnu færslunni skaltu merkja frádráttarlínuna og síðan á flipanum Opna færslur skaltu merkja línuna. Á aðgerðasvæðinu skal smellt á Vinna með > Samsvörun.

Staða upprunalegu krafanna er nú stillt á **Lokið**.

## <a name="analyze-the-effectiveness-of-the-promotion-and-fund-consumption"></a>Greina skilvirkni kynningar og notkun á fjármagni

Til að fá yfirsýn yfir helstu tölfræði og fjármagnsnotkun áætlunar er hægt að nota nokkrar skýrslur og greiningaryfirlit sem eru í boði í Stjórnun afsláttar.

Á síðunni **Virkni afsláttar** sýnir flipinn **Yfirlit** helstu upplýsingar um afsláttarsamninginn. Hinir fliparnir sýna nánari upplýsingar um tengd skjöl, greiðslur og aðrar atburði sem tengjast áætluninni.

Flipinn **Yfirlit** sýnir heildarmagn vara sem hefur verið selt út frá kynningunni, upphæð sölunnar sem hefur verið reiknsfærð og endurgreiðslur og eingreiðslur sem hafa verið greiddar.

Flipinn **Inneign endurgreiðslu** inniheldur upplýsingar um einstakar endurgreiðslur sem hafa verið kreditfærðar á viðskiptavininn.

Til að fá betra yfirlit yfir greiningu á ýmsum mælikvörðum um árangur fyrir kynninguna geturðu notað Greiningaryfirlitið. Til að fara í Greiningaryfirlitið skaltu smella á **Sala og markaðssetning** \> **Afslættir** \> **Afsláttarsamningar**. Á aðgerðasvæðinu skal smellt á **Greining**.  

Til að fá betra yfirlit yfir greiningu á ýmsum mælikvörðum um árangur fyrir kynninguna geturðu notað Greiningaryfirlitið. Til að fara í Greiningaryfirlitið skaltu smella á **Sala og markaðssetning** \> **Afslættir** \> **Afsláttarsamningar**. Á aðgerðasvæðinu skal smellt á **Greining**. 

