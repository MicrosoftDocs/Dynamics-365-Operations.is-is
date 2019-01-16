---
title: Uppfylling pantana fyrir verslun
description: "Í þessu efnisatriði er að finna yfirlit yfir uppfyllingu pantana fyrir verslun."
author: rubencdelgado
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: rubencdelgado
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: b3eeda217e00b33962561bcb2ee6185275f52fe2
ms.contentlocale: is-is
ms.lasthandoff: 01/04/2019

---

# <a name="store-order-fulfillment"></a>Uppfylling pantana fyrir verslun

[!include [banner](includes/banner.md)]

Margir smásalar vilja hámarka uppfyllingu pöntunar með því að gera verslanir kleift að fylla pantanir. Pöntunaruppfylling á verslunarstiginu getur hjálpað til við að draga úr hárri birgðastöðu fyrir tiltekna verslun, eða gæti verið nauðsynleg út frá skipulagslegu sjónarmiði í þeim tilvikum þar sem verslun hefur auka rúmtak eða er staðsett í minni flutningsfjarlægð frá viðskiptavininn. Til að bregðast við þessari þörf er í boði samræmd pöntunaruppfyllingaraðgerð við sölustað.

Pantanir til að uppfylla í tilteknum verslun er með vörugeymslu verslunarinnar útnefnda á hausnum eða í línum pöntunarinnar.

Pöntunaruppfyllingaraðgerðin í sölustaðnum veitir eitt vinnusvæði í sölustað sem hægt er að nota til að vinna pantanir. Þetta felur í sér allt frá því að samþykkja pöntunina, merkja hana sem senda, eða setja af stað afhendingu í verslun.

## <a name="access-unified-order-fulfillment-in-the-point-of-sale"></a>Ná í samræmda pöntunaruppfyllingu á sölustaðnum

Pöntunaruppfyllingu, [Aðgerðarnúmer 928](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-operations), má nota til að fá aðgang að vinnusvæði uppfyllingar pöntunar fyrir verslun á sölustaðnum.

Pöntunaruppfyllingaraðgerðin hefur ekki sína eigin heimild út-úr-kassanum, en í framtíðinni munu notendur geta notað **Leyfa að sækja pöntun** heimildina til að hefja aðgerðina frá sölustað.

Á verslunarstiginu er skilgreiningarstilling tiltæk til að ákvarða hvort pöntunarlína skuli samþykkt handvirkt innan sölustaðarins. Ef þessi valkostur fyrir skilgreiningu er ekki stilltur verða pöntunarlínur samþykkt sjálfgefið. Ef kveikt er á þessum valkostur fyrir skilgreiningu, verða notendur á sölustaðnum að velja **Leyfa að samþykkja pöntunina** heimild til að samþykkja pantanir sem koma innan frá sölustað.

Einnig er hægt að hafna pöntunarlínum frá sölustað. Það að hafna pöntunarlína táknar að hún verði ekki uppfyllt í þeirri verslun og sendir pöntunarlínuna aftur til endurúthlutunar í aðra verslun eða vöruhús. Heimild til að hafna pöntunarlínur eru veittar með **Leyfi til að hafna pöntun** heimildinni.

## <a name="order-fulfillment-operation-parameters"></a>Færibreytur pöntunaruppfyllingaraðgerða

Pöntunaruppfylling býður upp á út-úr-kassanum færibreytur sem hægt er að beita í aðgerðinni þegar hún er kölluð fram á sölustað. Þegar **Allir pantanir** færibreytur eru skilgreindar, birtast allar pantanir þegar aðgerðin er notuð. **Pantanir til að senda** færibreytan sýnir aðeins pantanir sem verður að senda frá versluninni og **Pantanir til afhendingar** sýnir pantanir sem verða sóttar í verslun.

## <a name="orders-for-fulfillment"></a>Pantanir til uppfyllingar

Pöntunaruppfyllingaraðgerðin sýnir aðeins pantanir sem annaðhvort verður sótt í eða send frá núverandi verslun. Pantanir fyrir aðrar verslanir til að uppfylla eru ekki taldar upp þegar notaður er pöntunaruppfyllingaraðgerðin.

## <a name="line-selection"></a>Línuval

Hægt er að velja línur með því að nota **Velja** aðgerðina í Aðgerðarúðuna. Þegar **Velja** er virkjað er hægt að velja margar línur til vinnslu. Þú getur hreinsað valda línur með því að smella á sömu línu aftur.

## <a name="line-details"></a>Línur, annað

Hægt er að sýna upplýsingar um línur með því að nota hliðargluggavalmynd fyrir línuupplýsingar. Þegar þessi valmynd er notuð verða tiltækir þrír flipar sem sýna aukaupplýsingar fyrir völdu línuna. Fyrsti flipinn, **Línuupplýsingar** sýnir upplýsingar fyrir línuna sjálfa, svo sem magn sem er pantað og er eftir. Viðbótarupplýsingar eru veittar, þar með talið magn sem er tekið til, pakkað og reikningsfært, ásamt flutningsmáta og afhendingaraðsetur. Flipann **Upplýsingar um pöntun** veitir upplýsingar pöntunarhauss, þ.m.t. viðskiptavinur, kenni viðskiptavinar, pöntunarnúmer, heildarupphæð pöntunar og staða. Flipinn **Birgðir** sýnir upplýsingar fyrir völdu línurnar eftir efnislegum tiltækum birgðum, fráteknum birgðum og pöntuðum birgðum.

Ef margar línur eru valdir, þá mun hliðargluggavalmyndin fyrir upplýsingar um pöntunarlínu aðeins benda á að margar línur eru valdir. Til að birta upplýsingar um eina línu skaltu hreinsa línurnar þar til aðeins einn lína er eftir.

## <a name="pending-order-lines"></a>Pantanalínur í bið

Samræmd pöntunaruppfylling felur í sér hæfni til að handvirkt samþykkja pantanir. Sjálfgefið er að pöntunum til uppfyllingar í versluninni eru þegar samþykkt. Hins vegar, ef viðskiptaferli ráða því að starfsmaður í verslunarstigi verður að taka við pantanir, er hægt að kveikja á handvirkt viðtaka á verslunarstigi smásölu. Til að virkja viðtöku pantana skal fara í **Smásala** \> **Rásir** \> **Smásöluverslanir** \> **Allar smásöluverslanir**. Opnaðu þá verslun sem þú vilt og á flipann **Almennt** skaltu finna undirsíðuhausinn **Uppfylling pöntunar**. Þessi undirsíðuhaus hefur **handvirkt samþykki** valkost sem er stillt á **Nei** sjálfgefið. Með því að stilla þennan möguleika á **Já** og samstilla breytingarnar á rásargagnagrunninn geta pöntunarlínur farið í gegnum samþykktarferlið.

Starfsmenn með **leyfa að samþykkja pöntun** heimildina geta opnað pöntunaruppfyllingu og valið línur til samþykktar. Þegar línurnar hafa verið samþykktar breytast staða þeirra frá **Bið** til **Samþykkt** og restin af uppfyllingu pöntun ferlinu getur haldið áfram. Þegar kveikt er á **Handvirk samþykki** verður ekki unnið með pöntun fyrr en þau hafa verið samþykkt.

Pantanir fyrir afendingu í verslun hafa aldrei stöðuna **Bið**. Þetta er gert til að koma í veg fyrir atburðarás þar sem viðskiptavinur kemur í búðina og ekki er unnt að setja pöntunarlínu í ferli vegna þess að starfsmaður með viðeigandi réttindi er ekki tiltækur.

## <a name="accepted-order-lines"></a>Samþykktar pöntunarlínur

Pantanir með línustöðu **Samþykkt** geta haldið áfram í gegnum restina af pöntunaruppfyllingarferlinu á sölustað. Eftir að pöntun hefur verið samþykkt er hægt að framkvæma allar aðgerðir sem eftir eru og beina þeim að pöntunarlínunni.

Til dæmis er hægt að velja samþykkta pöntunarlínu og síðan sækja hana beint án þess að fara í gegnum tiltekt og pökkun.

## <a name="line-actions"></a>Línuaðgerðir

### <a name="pick"></a>Taka til

Flokkurinn **Tiltekt** fyrir aðgerðir er veittur til aðstoðar í því ferli að taka til pöntunarlínur úr hillum. Aðeins má framkvæma tiltektaraðgerðir á pöntunarlínum sem áður hafa verið samþykktar.

**Aðgerð: Tiltekt**

- **Afleidd POS-staða:** Tiltekt
- **Afleidd staða bakvinnslu:** Engin breyting

Eftir að pöntun hefur verið samþykkt geta línur verið valdar og merktar sem **Tiltekt**. Merking línu sem **Tiltekt** er leið til að gefa til kynna að tiltektarvinnuna sé þegar verið að framkvæma á línu. Þetta kemur í veg fyrir að tveir starfsmenn reyni að velja sömu pöntunarlínur á sama tíma.

**Aðgerð: Prenta tiltektarlista**

- **Afleidd staða:** Tiltekt
- **Afleidd staða bakvinnslu:** Engin breyting

Tiltektarlista er hægt að prenta á sölustað til að aðstoða starfsmenn við að framkvæma tiltektarferli. Starfsmaður sem framkvæmir tiltekt getur haft með sér prentaðan tiltektarlista og um leið og vörur eru teknar til, merkir starfsmaðurinn þær sem tilteknar á tiltektarlistanum.

Snið fyrir tiltektarlista er skilgreint í Dynamics 365 for Retail og bætt á forstillingu innhreyfingar. Fyrir nánari upplýsingar um hvernig eigi að setja upp forstillingar innhreyfingar, sjá [Snið og prentun innhreyfingar](https://docs.microsoft.com/dynamics365/unified-operations/retail/receipt-templates-printing).

Ef línur eru valdar og tiltektarlisti er prentaður fyrir þær línur, eru þær sjálfkrafa uppfærðir með **Tiltekt** stöðu.

**Aðgerð: Merkja sem tiltekið**

- **Afleidd staða:** Tiltekið eða að hluta tiltekið
- **Afleidd staða bakvinnslu:** Tiltekið eða að hluta tiltekið

Eftir að efnislega tiltektarferlinu hefur verið framkvæmt má merkja línur sem **Tiltekið**. Að velja línu og merkja það sem **Tiltekið** framkallar símtal í rauntíma til að uppfæra pöntunarlínuna í Dynamics 365 for Retail. Eftir að línan hefur verið merkt sem **Tiltekið** á sölustað er staðan í bakvinnslunni einnig uppfærð í **Tiltekið** og birgðafærslur endurspegla að tilgreint magn hefur verið minnkað.

Þegar pantanir eru unnar yfir tíma, er hægt að vinna að hluta magns fyrir tiltekinn línu. Ef lína er valin og aðgerðin **Merkja sem tiltekið** er framkvæmd, og magnið er meira en einn, er notandinn beðinn um magnið. Eftirstandandi magn til tiltektar er fyllt inn sjálfkrafa. Ef minna en eftirstandandi magn er tilgreint, breytist staða línunnar í **Tiltekið að hluta**. Þegar pöntunarlínan er uppfærð í bakvinnslu, mun það einnig endurspegla tiltekið að hluta stöðuna og magnið sem notandinn hefur fært inn er notaður fyrir birgðauppfærsluna.

Ef pöntunarlína er tiltekin í villu verður afturköllunarferlið að fara fram á pöntunarlínunni í bakvinnslu. Sem stendur er afturköllunaraðgerð fyrir tiltekt ekki studd á sölustað.

Pöntunarlínur frá mismunandi pöntunum er hægt að velja og merkt sem **Tiltekið**, prenta á sama tiltektarlista eða merkt sem **Tiltekið**.

### <a name="pack"></a>Pakki

Pöntunarlínur geta verið pakkaðar hvenær sem er eftir að pöntunarlínan hefur verið samþykkt.

**Aðgerð: Prenta fylgiseðil**

- **Afleidd staða:** Pakkað eða að hluta til pakkað
- **Afleidd staða bakvinnslu:** Afhent eða að hluta til afhent

Þessi aðgerð merkir línur sem pakkað eða að hluta pakkað og prentar fylgiseðil. Hægt er að prenta fylgiseðil til að staðfesta þær vörur sem hafa verið pakkaðar saman. Snið fylgiseðils í skilgreint Dynamics 365 for Retail og bætt við forstillingu innhreyfingar. Fyrir nánari upplýsingar um hvernig eigi að setja upp forstillingar innhreyfingar, sjá [Snið og prentun innhreyfingar](https://docs.microsoft.com/dynamics365/unified-operations/retail/receipt-templates-printing).

**Aðgerð: Merkja sem pakkað**

- **Afleidd staða:** Pakkað eða að hluta til pakkað
- **Afleidd staða bakvinnslu:** Afhent eða að hluta til afhent

**Merkja sem pakkað** aðgerðin er hægt að nota til að gefa til kynna að línur séu pakkaðar án þess að prenta fylgiseðil. Bæði **Prenta fylgiseðil** og **Merkja sem pakkað** leiða til birgðafærslna í bakvinnslu. Pökkunarlínur í sölustað mun leiða til þess að færslubækur fylgiseðils séu búnar til í bakvinnslu.

Ef pöntunarlína er pakkað í villu, verður færslubók fylgiseðils að vera leiðrétt í bakvinnslu.

Aðeins línur í sömu pöntun og með sömu flutningsmáta geta verið pakkaðar á sama tíma.

Eins og er valkosturinn að merkja línur fyrir afhendingu í verslun sem **Pakkað** óvirkur. Þessari getu verður bætt við í framtíðarútgáfu. Stofnunarferli fylgiseðils mun verður bætt til að styðja við innspýtingu flutningsupplýsinga frá þriðja aðila í fylgiseðilsferlið.

### <a name="pick-up"></a>Sækja

Pantanir fyrir afhendingu í verslun geta verið afhent beint þegar þau eru sótt á sölustað. Pantanir afhentar í verslun eru ekki háðar samþykki.

**Aðgerð: Afhending**

- **Afleidd staða:** Reikningsfært eða að hluta til reikningsfært
- **Afleidd staða bakvinnslu:** Reikningsfært eða að hluta til reikningsfært

Ef lína er valin til afhendingar frá sameinaðri pöntunaruppfyllingu, er allt pöntunin hlaðinn inn í sölustað og fullt magn fyrir völdu línu er merkt. Aðrar línur á pöntuninni eru einnig hlaðnir inn í færsluyfirlit sölustaðarins, en með magn merkt sem núll.

Eftir að línur fyrir afhendingu hafa verið hlaðið inn í færsluyfirlitið, getur færslan farið í gegnum sama greiðslumáta eins og venjulega.

Línur sem hafa verið reikningsfærðar að fullu gegnum afhendingu mun ekki lengur birtast í vinnslu sameinaðrar pöntunar. Línur sem hafa verið afhentar að hluta til munu áfram birtast í sameinaðri pöntunaruppfyllingu þar til þær hafa verið afhentar að fullu.

Ef lína er afhent við villu þarf að framkvæma skil til að leiðrétta villuna.

Aðeins er hægt að afhenda línur í sömu pöntun og með sömu sendingarmáta á sama tíma.

### <a name="shipping"></a>Sending

Pöntunarlínur sem hægt er að senda frá versluninni má vinna gegnum samræmda pöntunaruppfyllingu með því að nota aðgerðina **Senda**. Ef handvirkt samþykki pöntunarlínu er skilgreint á rásarstiginu, verða pantanir að vera samþykktar fyrir sendinguna. Eftir að pöntunarlína hefur verið samþykkt og hefur stöðuna **Bið** eða aðra stöðu, er hægt að senda línur.

**Aðgerð: Senda**

- **Afleidd staða:** Reikningsfært eða að hluta til reikningsfært
- **Afleidd staða bakvinnslu:** Reikningsfært eða að hluta til reikningsfært

Línur sem eru sendar frá sameinaðri pöntunaruppfyllingu eru reikningsfærðar frá bakvinnslunni svipað og ef pöntunin er reikningsfærð beint frá bakskrifstofunni. Línur sem eru sendar frá sameinaðri pöntunaruppfyllingu eru ekki hlaðin inn í færsluyfirlit og enginn greiðslumáti er lagður upp á þeim tíma sem línurnar eru sendar.

Pöntunarlínur sem hafa verið sendar að fullu birtast ekki lengur í samræmdu pöntunaruppfyllingu. Línur sem hafa verið sendar að hluta munu áfram birtast í samræmdu pöntunaruppfyllingu þar til þær hafa verið sendar að fullu.

Aðeins línur frá sömu pöntun geta verið sendar á sama tíma. Ef línurnar frá sömu pöntuninni hafa mismunandi flutningsmáta geta þau samt verið valin til sendingar á sama tíma.

### <a name="reject"></a>Hafna

Línur eða línur að hluta má hafna. Þetta gerir þeim kleift að vera endurúthlutað frá bakvinnslunni til annars verslunar eða vöruhús. Línum er aðeins hægt að hafnað ef þeir hafa ekki enn verið tiltekin eða pakkað. Til að hafna línu sem hefur þegar verið tekin til eða pakkað verður afturkalla tiltekt eða pökkun fyrir þessa lína frá bakvinnslunni.

**Aðgerð: Hafna**

- **Afleidd staða:** Hafnað
- **Afleidd staða bakvinnslu:** Engin breyting

Hægt er að skoða þær pöntunarlínur sem hefur verið hafnað á vinnusvæðinu **Vinnsla og fyrirspurnir sölupantana**. Hreinsaðu einstaklingssíuna á vinnusvæðinu til að skoða allar pöntunarlínur, sem hefur verið hafnað, yfir allar verslanir. Flipinn **Pöntunarlínur sem hefur verið hafnað** undir **Pantanir og eftirlætisatriði** hlutanum birtir upplýsingar um pöntunarlínuna. Að auki geta notendurnir smellt á hnappinn **Pöntunarlínur sem hefur verið hafnað** undir **Samantekt** hlutanum til að fara yfir í yfirlit yfir sölupantanir. Þetta sýnir allar pantanir sem hafa einn eða fleiri hafnað pöntunarlínur. Ef Dreifð pantanastjórnun (DOM) er virkjuð, þá verða þessar pantanir sem hefur verið hafnað sjálfkrafa endurúthlutað til viðeigandi verslana til uppfyllingar, en hinsvegar er einnig hægt að endurúthluta þessar pantanalínur handvirkt. Til að gera það skaltu velja línu sem sýnir **Uppfyllingarstöðu** sem **Hafnað** og breyta síðuna/vöruhúsið eftir þörfum. Smelltu á **Uppfæra línu** fellilistann og smelltu á **Endurstilla uppfyllingarstaða** til að breyta uppfyllingarstöðu frá **Hafnað** yfir í **Samþykkt** eða **Í bið**, allt eftir uppsetningu pöntunaruppfyllingarinnar. Eftir að uppfyllingarstaða er endurstillt, þá geta verslunarmennirnir séð pöntunarlínurnar í POS.

## <a name="line-quantity-tracking"></a>Rakning línumagns

Eina pöntunarlínu með magn sem er meiri en einn er hægt að vinna yfir tíma, sem leiðir til margskonar undirstöðu fyrir pöntunarlínur. Til dæmis, ef byggingaraðili hefur verkefni sem krefst 500 plötur, en byggingaraðilinn mun aðeins sækja eða láta senda sér nokkrar plötur í einu á meðan verkefnið stendur, gæti verið magn sem er tekið til, pakkað og sent á sama tíma.

Hvert skipti sem lína er valin mun sú upphæð sem eftir er fyrir línuna verða sjálfkrafa fyllt út til að gera ráð fyrir að verið sé að vinna eftirstandandi magn. Með því að nota dæmið hér að ofan, ef 200 plötur hafa þegar verið tiltekin og línan fyrir plötur er valin fyrir tiltekt, verður það sem eftir er af magni upp á 300 sjálfkrafa fyllt út í magni. Sama gildir ef 200 plötur hafa þegar verið reikningsfærðar. Ef svo er, verður aðeins það magn sem eftir er sjálfkrafa fyllt út.

Halda áfram með dæmið hér að ofan, ef 200 plötur eru merktar sem pakkaðar og sending er valin, verður heildarmagn upp á 500 sjálfkrafa fyllt út. Ef aðeins 200 plötur eru sendar, mun kerfið gera ráð fyrir að verið sé að senda áður pakkaðar plötur og pakkað magn verður minnkað. Ef 201 plötur eru sendar, eru pakkaðar plötur fyrst minnkaðir með því að minnka eftirstandandi eina plötu úr því magni sem eftir er.

## <a name="line-statuses"></a>Línustöður

Pöntunarlínur í sölustað hafa nokkrar stöður til að endurspegla stöðu pöntunarlínunnar. Stöður í sölustað og bakvinnslu eru ekki samsvarandi í öllum tilvikum. Staða pöntunarlínu er hægt að skoða í gegnum sölustaðinn með því að nota pöntunaruppfyllingaraðgerðirnar. Í bakvinnslunni er hægt að skoða pöntunarlínur út frá pöntunarupplýsingum. Hægt er að nálgast upplýsingar um pantanir í gegnum **Smásala** \> **Viðskiptavinir** \> **Allar viðskiptavinapantanir**. Veljið **Kenni pöntunar** til að skoða pöntunarupplýsingar. Frá upplýsingum um pöntun veldu flipann **Sölupöntun** og veldu síðan **Nákvæm staða** undir **Skoða** undirhausnum.

- **Í bið** – Pöntunarlínur sem hafa verið úthlutað til verslunar, en ekki enn samþykktar, hafa stöðuna **Í bið** þegar þau eru skoðuð á sölustað. Línur í bið eftir samþykki á sölustað mun hafa **Pöntun í vinnslu** stöðu í bakvinnslu.
- **Samþykkt** – Pöntunarlínur sem hafa verið samþykktar handvirkt eða samþykktar sjálfkrafa munu hafa stöðuna **Samþykkt** þegar þær eru skoðaðar á sölustað. Línur með **Samþykkt** stöðu verða sýnd sem **Pöntun í vinnslu** í bakvinnslunni.
- **Tiltekt** – Línur sem verið er að taka til á verslunarstiginu hafa stöðuna **Tiltekt**. Sama línur, þegar skoðaðar eru í bakvinnslu, munu birtast sem **Línur í vinnslu**.
- **Tiltekið** og **Tiltekið að hluta** – Línur sem hafa verið teknar til eða að hluta teknar til á sölustað, hafa stöðuna **Tiltekið** eða **Tiltekið að hluta**. Sama línur á bakvinnslunni munu einnig birtast sem **Tiltekið** eða **Tiltekið að hluta**.
- **Pakkað** og **Pakkað að hluta** – Línur sem hafa verið pakkaðar eða að hluta pakkaðar á sölustað hafa stöðuna **Pakkað** eða **Pakkað að hluta**. Sama línur á bakvinnslunni munu einnig sýna sem **Afhent** eða **Að hluta til afhent**.
- **Reikningsfært að hluta** – Línur sem hafa verið sóttar að hluta eða sendar að hluta munu hafa stöðuna **Reikningsfært að hluta** á sölustað og í bakvinnslu.
- **Reikningsfært** – Línur sem hafa verið að fullu reikningsfærðar á sölustað munu ekki lengur birtast til uppfyllingar. Í bakvinnslunni er staða þessara lína **Reikningsfært**.

## <a name="order-fulfillment-filtering"></a>Síun pöntunaruppfyllingar

Pöntunaruppfylling á sölustað felur í sér síun til að hjálpa notandanum að finna auðveldlega það sem þeir þurfa. Hægt er að breyta síum gegnum aðgerðarúðuna neðst á **Sölustaður** skjár. Sjálfgefið er að **Afhendingarmáti** síu er beitt, byggt á því hvernig aðgerðin er sett upp. Ef aðgerðin er sett upp með **Allar pantanir** færibreytunni, þá er þessari sía beitt þegar farið er inn í pöntunaruppfyllingu. Sama gildir um **Sótt í verslun** og **Sent frá verslun** færibreytur. Aðrir síur sem hægt er að beita á yfirlit pöntunaruppfyllingar innihalda:

- Númer viðskiptavinar
- Nafn viðskiptavinar
- Netfang viðskiptavinar
- Pöntunarnúmer
- Afhendingarmáti
- Kvittunarnúmer
- Tilvísunarkenni rásar
- Númer upprunaverslunar
- Staða línu
- Búið til þann
- Afhendingardagur
- Móttökudagsetning

