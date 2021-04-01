---
title: Stofna innkaupapantanir
description: Þessi skrá lýsir ferlisi og valkosti þegar innkaupapöntun er stofna handvirkt.
author: RichardLuan
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: 93053
ms.assetid: 25b1c9f1-20f8-4cf5-b87c-876e32f68846
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 28407ee694fa788def68aba92366d91248fd6541
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216010"
---
# <a name="create-purchase-orders"></a>Stofna innkaupapantanir

[!include [banner](../includes/banner.md)]

Þessi skrá lýsir ferlisi og valkosti þegar innkaupapöntun er stofna handvirkt.

Þetar þú stofnar innkaupapöntun (PO)m eru allar Almennar upplýsingar um alla pöntunina tilgreindar í haus Innkaupapöntunar, og þá bætirðu við einum eða fleiri Innkaupapöntunarlínur . Þessi skrá lýsir nokkrum mest notuð valkostina sem eru tiltækar.  

Einnig er hægt að stofna innkaupapantanir með því að afrita línur úr annarri skjali Innkaupapöntunar eða sölupöntunar. Í þessu tilfelli er hægt að snúa við formerki í birgðum, eins og þú myndir snúa við formerkinu á reikningi til að tilgreina kredit.  

Þó hægt sé að stofna innkaupapantanir handvirkt, eru þær venjulega myndað úr önnur ferli. Pantanir er hægt að stofna sjálfvirkt á grundvelli annarra skjöl, eins og beiðnum. Einnig má stofna þær sem hluti af áætlanagerðarvinnslu gegnum áætlaðar innkaupapantanir. Ef þú notar innkaupasamninga er hægt að stofna innkaupapantanir með **Úttektarpöntun** aðgerð. Það eru einnig ítarlegri aðferðir til að stofna Innkaupapöntun sjálfkrafa. Til dæmis er hægt að stofna pantanir þegar þú nota beina afhendingu eða pöntunarkeðjur innan samstæðu.

## <a name="creating-a-purchase-order-header"></a>Stofna haus innkaupapöntunar
Þegar ný Innkaupapöntun er stofnuð birtist svargluggi , þar sem hægt er að færa inn algengar upplýsingar fyrir haus Innkaupapöntunar. Þegar smellt er á **í lagi** til að loka svarglugganum, er pöntun stofnuð og síðan er hægt að tilgreina viðbótarupplýsingar í haus.  

Þegar innkaupapöntun er stofnuð verður fyrst að tilgreina gerð hennar. Gerðin **Innkaupapöntun** er oftast notuð. Hins vegar ef kreditreiknings er krafist er hægt að nota gerðina **Skilapöntun**.  

Tilgreina verður birgi í **lánardrottnalykil** svæði. Fyrir þennan reit geturðu leitað annað hvort á lykilinn eða nafn lánardrottins. Ef lánardrottinn afhendir frá mörgum stöðum en notar einn reikningslykill er hægt að velja þann reikningslykill í **Reikningslykill** svæðinu og nota hana síðan með mismunandi lánardrottnalykla. Ef þú þarft að stofna Innkaupapöntun fyrir afurðir sem ekki eru pantað margsinnis, er hægt að nota í **eins-skiptis lánardrottinn** valkost. Þessi valkostur stofnar sjálfkrafa nýjan lánardrottnalykil sem er merkt sem einskiptis lykil, til að styðja síðar hreinsunarferli í **Viðskiptaskuldir** kerfiseiningu. Þegar þú velur lánardrottnalykil, erfa mörg svæði í haus Innkaupapöntunar sjálfgildi úr upplýsingum sem tengist lánardrottnalykli. Til dæmis er sjálfgefið afhendingarsvæði og vöruhús afrituð frá lánardrottnaupplýsingum. Hins vegar er hægt að hnekkja þessi sjálfgefnu gildi ef innkaupin eru ætlaðar fyrir aðra staðsetningu.  

Ef birgir hefur veitt tilvísunarnúmer fyrir pöntunina er hægt að skrá þetta upplýsingar í **tilvísun í Lánardrottin** svæðinu. Fyrir skilapantanir þarf að tilgreina gildi í í **RMA** svæði til að vísa í heimild birgis fyrir vinnslunni á skilunum.  

Ef innkaupasamning er tengdur við pöntun, verður að tilgreina þessar upplýsingar í **Innkaupasamningur** svæði.  

Haus Innkaupapöntunar inniheldur einnig upplýsingar um gjöld sem eiga við alla pöntunina í stað einstakra lína. Gjöld má bæta sjálfkrafa við pöntunina ef sjálfvirk gjöld hafa verið sett upp fyrir lánardrottinn eða fyrir gjaldaflokk lánardrottins. Er hægt einnig bæta handvirkt við gjöld við pöntunarhaus með því að smella á **vinna Með gjöld** í Aðgerðarúðunni.

## <a name="adding-purchase-order-lines"></a>Bæta við innkaupapantanalínum
Innkaupapantanir geta verið fyrir efnislegar afurðir eða þjónustu. Stilling á birgðalíkansflokki ákvarðar hvort við tiltekið vörunúmer eigi við vöru eða þjónustu. Yfirleitt, er varan sem er keypt tilgreint með vörunúmeri. Hins vegar ef pöntunin er fyrir vörur eða þjónustu sem eru notaðar beint, geturðu einnig tilgreina vöru með því að nota innkaupategund.  

Innkaupapantanalínur innihalda mörg svæði, en margar af þessum svæðum hafa sjálfgefið gildi eða gildi sem er erft frá pöntunarhaus. Viðbótarsvæði eru stillt þegar þú velur vöru eða þjónustu. Svæðin sem eru oftast stillt handvirkt innihalda svæðunum fyrir vörunúmer, magn og umbeðinnar afhendingardagsetningu. Einnig er mjög mikilvægar upplýsingar um einingarverð og afslætti, en gildi fyrir þessi svæði eru oft ákvörðuð af viðskiptasamningum eða innkaupasamningum.  

Þegar afurð er valin, er hægt að leita á alla eða hluta afurðarheitis, í stað þess að nota vörunúmer. Ef varan hefur nokkur afbrigði, eins og mismunandi stærðum, er hægt að sjá yfirlit yfir tiltæk afbrigði með því að nota **Bæta við línum** aðgerð eða með því að nota uppflettinguna sem er í boði í **afbrigðanúmer** svæðinu.  

Oft, verður að tilgreina nokkrar vídda fyrir vöruna sem valin er á hverja línu Innkaupapöntunar. Víddir sem þarf að tilgreina eru háð víddaflokkum sem úthlutað hefur verið á afurðarskilgreininguna. Til dæmis þarf oft að tilgreina svæði og vöruhús til að tilgreina staðsetninguna sem varan skal vera afhent til. Afurðarafbrigði eru auðkennd með því að tilgreina númer afbrigðis, eða með því að færa inn gildi fyrir eina eða fleiri afurðarvíddir, eins og lit, stærð, skilgreiningu eða stíl. Rakningarvíddir, eins og runu og raðnúmer, gera kleift að auðkenna hverja birgðalotu. Eftir að pöntun hefur verið stofnað, er hægt að sækja víddargildi í pöntun með því að nota **Skráning** aðgerð. Til dæmis hefurðu pantað magn uppá fimm stykki af vöru. Síðar, skráirðu að þrjár af þessum stykkjum verða svart og tvær verður blátt. Þessari aðferð er annar valkostur við að fanga víddarupplýsingar meðan á komuskráningu stendur.  

Hægt er að athuga upplýsingar um stöðu birgðafærslu fyrir afurðir í birgðum. Til dæmis mætti athuga birgðir á lager til að aðstoða við ákvarða hversu mikið á að panta. Einnig mætti endurskoða birgðastöðu pantaðs magns til að sjá hvort komuskráningu á innleið hafi átt sér stað.  

Innkaupapöntunarlína sem er notað til að skila afurð til lánardrottins hefur neikvætt magn. Hægt er að velja ákveðna lotu til að skila með því að nota **Frátekning** aðgerð.  

Stundum gæti verið óskað að skipta upp magnið sem þú hefur pantað, þannig að mismunandi hlutar hennar eru sendar á mismunandi dagsetningum. Hægt er að setja upp þessara afhendingar með því að nota í **afhendingaráætlunar** aðgerð sem er tiltæk á á **Innkaupapöntunarlínu** valmynd í á yfirlitinu **Línur**.  

Gjöld má sjálfkrafa bæta við pöntunina ef sjálfvirk gjöld hafa verið sett upp fyrir lánardrottinn eða gjaldflokk lánardrottins, og fyrir vöruna eða gjaldflokk vörunnar. Hins eru algengrara að gjöldum er bætt við handvirkt á stigi pöntunarlínu. Til að bæta við gjaldi skal opna **vinna Með gjöld** síðu með því að nota **vinna Með gjöld** aðgerð á í **Fjárhagur** valmynd í yfirlitinu **Línur**. Kosturinn við að bæta gjöldum beint við á stigi pöntunarlínu er að gjöldunum má úthluta sem birgðakostnað. Til að setja upp gjaldakóða fyrir afurðarkostnað lykils, skal nota **Vöru** debet valkost. Þessar gerðir gjalda verður að úthluta úr haus Innkaupapöntunar á línur áður en hægt er að staðfesta pöntunina. Til dæmis viltu kannski úthluta gjöldum byggður á magninu í hverri línu. gjaldaflokkur hefur einnig áhrif á hvernig gjöld eru færð til reiknings. Til dæmis, föst gjöld tilgreina föst upphæð og prósentugjöld er reiknað sem prósenta af nettó upphæð fyrir pöntunarlínuna. Innkaupapantanir er hægt að úthluta á farm og farminum gæti falið í sér mat á áætlaða kostnaðar fyrir flutningskostnaðinn. Hægt er að úthluta þessum kostnaði úr farminum aftur á línur Innkaupapöntunar.

## <a name="purchase-order-actions"></a>Aðgerðir fyrir innkaupapöntun
Eftir að haus og línur hefur verið bætt við Innkaupapöntunina, oft ljúka þarf viðbótarskref áður en pöntunin er tilbúin til að staðfesta. Þar sem svo margir valkostir eru tiltækir, gæti verið gagnlegt að nota [Aðgerðaleit](../../fin-and-ops/get-started/action-search.md) til að finna viðeigandi valmyndaratriði.  

Hægt er að skilgreina vörur í pöntun þannig að þeir hafa fylgivörur. Fylgivörur eru afurðir sem verður eða er hægt að kaupa með aðrar afurðir. fylgivöru gæti verið bætt við án aukagjalda sem meðfylgjandi afurðir, eða hugsanlega er hægt að ákveða hvort á að bæta þeim við pöntunina eða ekki. Hægt er að fara yfir fylgivörur eftir hverja pöntunarlínu sem er bætt við. Hins vegar er sennilega að þér finnist þægilegra að fara yfir og bæta við fylgivöru fyrir allar pöntunarlínur með því að nota í **fylgivörur** síða sem hægt er að opna í Aðgerðarúðu.  

Afslættir eru vanalega bætt við línur um leið og þær eru stofnaðar. Hins vegar, nokkrar afslætti eiga við um alla pöntunina:

-   **heildarafsláttur** aðgerðin reiknar heildarafsláttarhlutfall sem er beitt á alla pöntunina. Ekki rugla afslætti við prósentu staðgreiðsluafsláttar. Staðgreiðsluafslættir eru notaðar þegar reikningur er greiddur, og þær eru háð greiðsluuppgjöri samkvæmt ákveðna dagsetningu.
-   Ef að afsláttur fyrir margar línur á við, þarf að nota **samvalsafsláttur** aðgerð til að reikna og tengja það við pöntun. Samvalsafslættir eru afslættir sem má bjóða ef blanda afurða í pöntun fara yfir sameiginlegan þröskuldi. Aðeins nokkur fyrirtæki nota þessa gerð afsláttar.

Gjöld sem eru með gjaldakóða sem notar debetgerð **Vöru** verður að vera úthlutað á línustigi áður en hægt er að staðfesta pöntunina. Þér gæti þótt það þægilegt að úthluta þessum gjöldum á stigi pöntunarhauss, þannig að hægt er að tilgreina heildarupphæð gjaldsins. Hins vegar í þessu tilfelli verður að úthluta gjöldum niður á hverja línu áður en hægt er að staðfesta pöntunina. Hægt er að nota **Úthluta gjöldum** aðgerðin til skipta upphæðum úr gjöldum sem er úthlutað á stigi pöntunarhauss niður á pöntunarlínur. Gjöld er hægt að skipta samkvæmt nettó upphæð á hverri línu, samkvæmt magn sem hefur verið pantað, eða jafnt þvert á pöntunarlínur. Þegar búið er að úthluta gjöldum á línurnar, er gjaldið fjarlægð úr pöntunarhaus.  

Hægt er að skilgreina innkaupapantanir til að krefjast að fjármagn fjárhagsáætlunar sé úthlutað á pöntunina áður en hægt er að vinna því. Í þessu tilfelli er hægt að nota **athugun á Fjárhagsáætlun** aðgerð til að úthluta fjárhagsáætluninni.  

Þú gætir þurft að fresta lokun Innkaupapöntunar. Til dæmis gætirðu þurft aukalegar upplýsingar um afurðir eða þjónustu, eða gæti þurft að fá heimild fyrir eyðsla. Það eru nokkrar aðferðir til að halda aftur pöntun. Til dæmis er hægt að bíða með að staðfesta pöntunina. Einnig, ef verkflæði breytingastjórnunar er í notkun, ekki senda pöntun til samþykktar. Ef verður að útiloka allar pantanir fyrir tiltekinn lánardrottin, er einnig hægt að merkja lánardrottins sem **í bið** fyrir vinnslu í lánardrottinssniðmát. Einnig eru aðstæður sem gætu komið í veg fyrir vinnsu pöntunar. Til dæmis, vinnslu gæti verið stöðvuð ef farið hefur verið fram yfir lánamark, eða ef nauðsynlegt áætlunarfjármagn  eru ekki tiltæk.

<a name="additional-resources"></a>Frekari upplýsingar
--------

[Yfirlit yfir innkaupapöntun](purchase-order-overview.md)

[Samþykkt og staðfesting innkaupapanta](purchase-order-approval-confirmation.md)

[Innhreyfingarskjal jafnað við innkaupapantanir](product-receipt-against-purchase-orders.md)

[Yfirlit yfir reikninga lánardrottna](../../finance/accounts-payable/vendor-invoices-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]