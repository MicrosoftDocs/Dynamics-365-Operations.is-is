---
title: "Yfirlit yfir „Innkaup og aðföng“"
description: "Þessi grein gefur yfirlit yfir þá virkni sem er fáanleg í Innkaupa- og aðfangakerfi."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58021
ms.assetid: eea24e23-a803-4de0-a218-6485757cde1b
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 758c516b378b4858c248fbca2befc6b9c47cc32a
ms.lasthandoff: 03/31/2017


---

# <a name="procurement-and-sourcing-overview"></a>Yfirlit yfir „Innkaup og aðföng“

Þessi grein gefur yfirlit yfir þá virkni sem er fáanleg í Innkaupa- og aðfangakerfi.

Innkaup og aðföng fjallar um öll skrefin frá því að greind er þörf fyrir vöru og þjónustu þar til afurð er keypt, innhreyfingar, reikningsfærslur og vinnsla á greiðslu með lánardrottnum. Hægt er að stilla innkaupaferli að þörfum tiltekins fyrirtækis með því að skilgreina innkaupa reglur og verkflæði.

## <a name="identifying-a-need-for-product-and-services"></a>Auðkenna þörf fyrir vöru og þjónustu
Þörf fyrir vöru eða þjónustu gætu komið upp úr *innkaupabeiðnir*, til dæmis þegar starfsmaður krefst afurðar. *Vörulistar *hægt er að setja upp til að leiðbeina um val á tiltækum afurðum til að velja úr, eða beiðnir er hægt að gera fyrir afurðir sem eru°ekki enn tiltækar í vörulista,og innkaupadeild heimilað að hafa í huga hvernig hægt sé að útvega afurðina.  

*Eyðsluþak *til að hafa hemil á útgjöldum í innkaupum, og°*innkaupaverkflæði *bætir við kostinum á að krefjast samþykkis áður en pöntun er gerð. Einnig er hægt að tilgreina úthlutun fjármagns fjárhagsáætlunar, ef þörf krefur.  
  
Deild innkaupa auðkennir birgja fyrir afurðir og þjónustu og þetta getur falið í sér°*beiðni um tilboð *senda mörgum mögulegum lánardrottnum. Hægt er að deila upplýsingum um vöru sem beðið er um og mögulegir lánadrottnar geta skoðað þær til að sjá ef þeir geta afhent°afurð sem passar við þær. Lánardrottnar skila tilboðum sínum sem eru síðan endurskoðuð af innkaupadeild áður en valinn er birgir sem óskað er eftir að°kaupa af.  

Innkaupapantanir innihalda valkost til að senda inn *innkaupafyrirspurn *til lánardrottins sem valkost í stað ítarlegrar beiðni um tilboðsferli. Hægt er að nota innkaupafyrirspurn til að auðvelda skilmála á borð við verð, afslætti og afhendingardagsetningu fyrir pöntunina. Ef lánardrottna eru settar upp til að nota í **Lánardrottins** portal * * aðgerðum fyrirspurn er óvirkur. Í staðinn er pöntun samnýtt í** Lánardrottins** gáttinni, og þegar°*staðfesting beiðni* er send getur lánardrottinn staðfest pöntunina beint.  

*Vörulistar lánardrottna *er hægt að nota til að safna upplýsingum um vöruúrval sem lánardrottnar geta útvegað. Lánardrottnar geta birt sína eigin vörulista þannig að það er auðveldara að halda vörulista°uppfærðum. Mögulegt er að tengja°*samþykktur listi lánardrottins* við afurð,°og það getur hjálpað til við val á lánardrottni þegar nýjar innkaupapantanir eru opnaðar, og koma í veg fyrir að nota°lánardrottna sem ekki var ætlunin að nota.

## <a name="procurement"></a>Innkaup
*Innkaupapantanir *er hægt að stofna á marga vegu þar á meðal:

-   Sem niðurstaða áætlanagerð sem hefur fundið við eftirspurn sem krefst innkaup. Þetta ferli myndar áætlaðar pantanir, og þegar þær eru losaðar innkaupapantanir eru myndaðar.
-   Gegnum°vinnslu innkaupabeiðna sem leiða til innkaupa.
-   Gegnum vinnslu innkaupasamninga, þar sem innkaupapantanir eru stofnaðar sem losaðar pantanir úr samningum. Þetta er yfirleitt notað þegar innkaupasamningar eru notaðir til að tákna standandi pantanir.
-   Handvirkt, þegar innkaupapöntun er stofnuð sem er ekki byggð á öðru skjali.

Innkaupapantanir sem eru skilgreindar með *innkaupa samþykktarverkflæði* krefjast samþykkis áður en þær eru skráðar sem samþykktar og þetta er krafist áður en hægt er að vinna pöntunina frekar.  

Innkaupapantanir eru *staðfestar* til að tákna að til samnings hafi verið stofnað með lánardrottni. Innkaupapöntun mun síðan miða áfram í áföngum gegnum mismunandi aðila°fram að því að hún verður að lokum°reikningsfærð eða hætt við hana.  

Þegar innkaupapöntun er stofnuð mörg svæði eru prepopulated með gildum sem eru sjálfgefnar úr upplýsingunum sem geymdar eru um lánardrottinn í á **Lánardrottna** síðu. Þetta þýðir að það eru takmarkaður fjölda svæða sem nauðsynleg eru að fylla inn í í innkaupapöntun, en þó er hægt að velja að hnekkja sjálfgefnum gildum.

### <a name="prices-and-discounts"></a>Verð og afsláttur

Verð og afsláttur°inniheldur upplýsingar um verð, afslætti og skilmála fyrir eftirágreiddan afslátt sem þeir bjóða. Verð og afslætti má setja fram sem *viðskipti* *samninga*. Viðskiptasamningar tákna verðlista lánardrottins með verði eða afslætti°og hefur ákveðnar dagsetningar sem samningurinn gildir. Verð og afslætti má semja um og tákna með *innkaupasamningar *með skilyrðum eins og skuldbinding til að kaupa ákveðið magn eða fyrir ákveðna upphæð og er forsenda fyrir umsamda greiðsluskilmála. *Samningar um eftirágreiddan afslátt *er hægt að stofna með lánardrottnum þar sem innkaup á tilteknum vörum eða vöruflokkum geta virkjað eftirágreiddan afslátt lánardrottins°sem ræðst af°upphæð innkaupa- eða magni.

### <a name="delivery-options"></a>Afhendingarkostir

Það eru mismunandi kostir fyrir afhendingarferlið sem tengist innkaupapöntun. Hægt er að skipta pöntuðum afurðum í *afhendingar* áætlanir þar sem hlutar af pöntuðu magni er hægt að áætla til afhendingar á mismunandi dagsetningum. Afhending geta einnig innihaldið *beina afhendingu* upprunnið úr sölupöntun, sem myndar sjálfkrafa°fylgiseðil á sölupöntun á sama tíma og innhreyfingarskjal afurða er skráð á innkaupapöntuninni. Innkaupapantanir getur einnig verið hluti af *pöntun innan samstæðu *keðju, einnig nefnt innkaupapöntunum innan samstæðu, þar sem vörur eru pantaðar frá samsvarandi sölupöntun innan samstæðu. Í þessum aðstæðum eru sum skref sjálfvirk milli tveggja tengdra samstæðupantana.

### <a name="supplementary-items"></a>Fylgivörur

Hægt er að setja upp vörur til að innihalda *fylgivörur*. Þetta er til að leggja til afurðir sem eru tengdar vörunni sem verið er að panta. Aukaafurðirnar gæti verið krafist, eða kann að vera valfrjáls. Í sumum tilvikum er hægt að bæta við fylgivörum sem ókeypis afurðum sem fylgja kaupum á öðrum afurðum.

### <a name="purchase-order-charges"></a>Gjaldfærslur vegna innkaupapöntunar

Gjaldfærslum kann að vera úthlutað til innkaupapöntunarinnar. Þetta getur gerst sjálfkrafa í gegnum uppsetningu á sjálfvirkum gjaldfærslum eða með því að°bæta gjöldum handvirkt. Hægt er að tengja gjaldfærslur við pöntunina bæði á stigi pöntunarhauss og pöntunarlínu. Hægt er að setja upp bókhald gjaldfærslna á mismunandi vegu. Til dæmis er hægt að setja upp gjald sem er bókað sem kostnaður vöru. Ef þetta er gert þarf að úthluta gjaldfærslu á stigi pöntunarlínu áður en hægt er að staðfesta pöntunina. Það er valkostur sem geta hjálpað til við úthluta gjöldum úr haus í línur.

## <a name="product-receipt-and-invoicing"></a>Innhreyfingarskjal afurða og reikningur.
Innkaupapantanir sem fela í sér efnislegar afurðir krefjast yfirleitt að *komuskráningar* gerist innan vöruhúss og eftir það er *innhreyfingarskjal afurða * skráð fyrir°pöntunina. Innkaupapantanir með vörur sem uppfylla innkaupabeiðnir er hægt að stilla þannig að starfsmaðurinn°sem hefur beðið um vörurnar þarf einnig að veita *staðfestingu á innhreyfingu*.  

Sumar innkaupapantanir innihalda afurðir sem era þjónusta eða aðrar afurðir sem ekki eru efnislegar þar sem ekki er þörf á innhreyfingu í vöruhúsi. Hægt er að stofna afurðir semþjónustu eða *innkaupategundir *er hægt að nota beint á innkaupapöntun fyrir slíkar pantanir. Með þessar pantanir er bókhald á innhreyfingarskjali afurða stundum sleppt og pöntunin er reikningsfærð beint eða þá að skráning innhreyfinga afurða er gerð í innkaupapöntun án fyrri komuskráningu.  

Kvittun fyrir vörur getur leitt af sér sjálfvirka notkun fyrir°skilgreindan tilgang. Þar á meðal óbeina notkun með beina afhendingu, notkun fyrir verkefni, eða bóka afurðina sem eignir.  

Þegar* lánardrottnareikninga* berast frá lánardrottni geta þær fyrst verið skráðar í *komubók *óháð innkaupapöntun og svo síðar samþykkt sem°færsla°móti innkaupapöntun. Skráning reiknings lánardrottins við innkaupapöntun felur í sér að jafna innhreyfingarskjals afurða við reikninginn.  

*Dreifingar á fjárhagsupphæð* er hægt að tilgreina á innkaupapöntun til að lýsa því hvernig bókhald ætti að gera innan fjárhagsins og getur einnig skilgreint hvernig úthlutun fjárhagsáætlunar fæst þegar þetta er haft með í stillingum.  

Reikningsfærðar innkaupapantanir munu skrá skuld í lánardrottnareikning innan viðskiptaskulda, þaðan sem *l*á*nardrottnagreiðslan *getur verið unnin.

## <a name="vendor-performance"></a>Afköst lánardrottins
Afköst og endurskoðun innkaupa er studdur gegnum *innkaupa- og viðskiptaskuldaskýrslur,* sem innihalda eyðslugreiningu og frammistöðugreiningu lánardrottins.


