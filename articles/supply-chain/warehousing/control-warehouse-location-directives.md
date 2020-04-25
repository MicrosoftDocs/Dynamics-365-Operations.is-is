---
title: Stýra vöruhúsavinnu með vinnusniðmát og staðsetningarleiðbeiningar
description: Þetta efnisatriði lýsir hvernig eigi að nota vinnusniðmát og staðsetningarleiðbeiningar til að ákvarða hvernig og hvar vinna verður framkvæmd í vöruhúsinu.
author: perlynne
manager: tfehr
ms.date: 02/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aae57af04be8bcc6da2e5635b5ffa96d9fac147c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205737"
---
# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>Stýra vöruhúsavinnu með vinnusniðmát og staðsetningarleiðbeiningar

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir hvernig eigi að nota vinnusniðmát og staðsetningarleiðbeiningar til að ákvarða hvernig og hvar vinna verður framkvæmd í vöruhúsinu.

Leiðbeiningar sem starfsmenn vöruhúss fá í farsíma ákvarðast af sniðmáti vinnu sem er sett upp í Microsoft Dynamics 365 Supply Chain Management til að skilgreina hin ýmsu vöruhúsaferli og verkefni. Vinnusniðmát ákvarða vinnuna fyrir hvert vöruhúsaferli. Með því að tengja staðsetningarleiðbeiningar við vinnusniðmát getur hjálpað að tryggja að vinna á sér stað á ákveðnum efnislegum svæðum vöruhúss.

## <a name="work-templates"></a>Vinnusniðmát
**Vinnusniðmát** síðu gerir það mögulegt að skilgreina vinnsluaðgerðir sem þarf að framkvæma í vöruhúsinu. Yfirleitt samanstanda vinnsluaðgerðir vöruhúss af aðgerðarpari: starfsmanns í vöruhúsi tekur til lagerbirgðir á einni staðsetningu og setur síðan tíndu birgðirnar niður á annarri staðsetningu. 

Vinnusniðmát samanstendur af haus og tengdar línur Hvert vinnusniðmát er fyrir tiltekna *gerð vinnupöntunar*. Margar gerðir vinnupöntunar tengjast upprunaskjöl, eins og innkaupa- eða sölupantanir. Hins vegar, aðrar gerðir vinnupöntunar standa fyrir aðskilin vöruhúsaferli, eins og reglulega talningu. *kenni vinnuhópa* leyfir þér að skipuleggja vinnu í flokka. 

stillingarnar í skilgreiningu vinnuhauss má nota til að ákvarða þegar á að stofna nýja vinnu. Til dæmis er hægt að setja inn hámarksfjölda tiltektarlína og hámark áætlaðs tínslutíma. Svo ef vinnu fyrir tiltektarferli sölupöntunar fer fram yfir annaðhvort þessara gilda, er þeirri vinnu skipt í tvær einingar vinnu. 

Vinnulínum tákna efnislega verkin sem nauðsynleg eru til að vinna úr vinnunni. Til dæmis, fyrir vöruhúsaferli á útleið, gæti verið vinnulína til að taka til vörur innan vöruhús og aðra línu til að setja þær vörur yfir í sviðsetningarsvæðið. Svo getur verið til viðbótar lína til að taka til vörur frá sviðsetningu, og aðra línu fyrir setja vörurnar í vörubíl sem hluti af ferlinu við að hlaða. Hægt er að setja inn *leiðbeiningarkóði* á línum vinnusniðmáts. leiðbeiningakóða er tengd staðsetningarleiðbeiningar og þar af leiðandi hjálpar til við að tryggja að vöruhúsavinna er unnin á réttum stað í vöruhúsinu. 

Hægt er að setja upp fyrirspurn til að stýra hvenær tiltekna vinnusniðmátið er notað. Til dæmis er hægt að setja takmörkun þannig að hægt er að nota tiltekið sniðmát fyrir vinnu eingöngu í ákveðnu vöruhúsi. Einnig gætirðu haft nokkur sniðmát sem eru notaðar til að stofna vinnu sölupöntunarferli á útleið , eftir uppruna sölu. Kerfið notar **Raðnúmer** svæði til að ákvarða röð tiltæk vinnusniðmát eru metin í. Þess vegna, ef þú ert með mjög nákvæma fyrirspurn fyrir tiltekið vinnusniðmát , ætti að gefa því lágt raðnúmer. Sú Fyrirspurn verður síðan metnar á undan aðrar, almennari fyrirspurnir. 

Til að stöðva eða gera hlé á vinnuferli, geturðu notað að **Stöðva vinnu** stillingu á vinnulínunni. Í því tilfelli fær starfsmaður sem framkvæmir vinnuna ekki beiðnir um að framkvæma næsta vinnulínuskref. Til að fara í næsta skref, þarf sá starfsmaður eða annars starfsmanns að velja vinnuna aftur. Hægt er að aðskilja verk innan með vinnueiningar með því að nota annað *kenni vinnuklasa* á línum vinnusniðmáts.

## <a name="location-directives"></a>Staðsetningarleiðbeiningar
Staðsetningarleiðbeiningar eru reglur sem hjálpa við auðkenningu tiltektar- og frágangsstaðsetninga fyrir birgðahreyfingar. Til dæmis, í sölupöntunarfærslu, ákvarða staðsetningarleiðbeiningar hvar vörurnar verða teknar til og hvar tilteknar vörur verða að setja. Staðsetningarleiðbeiningar samanstanda af haus tengdar línur, og þær eru stofnaðar á **staðsetningarleiðbeiningar** síðu. 

Í haus verður hver staðsetningarleiðbeining að vera tengd við *gerð verkpöntunar* sem tilgreinir gerð birgðafærslu sem leiðbeiningarnar verður notuð fyrir, eins og sölupantanir, áfyllingu eða tiltekt hráefnis. *vinnutegund* tilgreinir hvort staðsetningarleiðbeininga verður notuð fyrir tiltekt eða setja, eða fyrir eitthvað annað vöruhúsaferli, eins og talningu eða birgðastöðubreytingu. Einnig þarf að tilgreina *svæði* og *vöruhús*. *leiðbeiningarkóði* sem þú tilgreina í haus er hægt að nota til að tengja staðsetningarleiðbeiningu við eitt eða fleiri vinnusniðmát . 

Eins og fyrir Vinnusniðmát, er hægt er að setja upp fyrirspurn til að ákvarða hvenær tiltekna staðsetningarleiðbeiningar er notað. Til dæmis er hægt að tilgreina að þegar e-commerce er uppruni sölupöntunar, verður að taka birgðir frá sérstöku svæði í vöruhúsinu. Kerfið notar **Raðnúmer** svæði til að ákvarða röð tiltækar staðsetningarleiðbeiningar eru metnar í. 

Línur staðsetningarleiðbeiningar setja frekari takmarkanir á notkun staðsetningaleitarreglna. Hægt er að tilgreina lágmarksmagn og hámarksmagnið sem á við leiðbeiningarnar eiga að gilda um, og hægt er að tilgreina að leiðbeiningarnar eigi að vera fyrir tiltekna birgðaeiningu. Til dæmis, ef mælieiningin er bretti þá er hægt að setja vörur í brettum á tilteknum stað. Einnig er hægt að tilgreina hvort magnið sé hægt að skipta á mörgum staðsetningar. Líkt og staðsetningarleiðbeiningar haus, hver lína staðsetningarleiðbeiningar hefur raðnúmer sem ákvarðar röð sem línurnar eru metnar í. 

Staðsetningarleiðbeiningar hafa eina viðbótar upplýsingastig: *aðgerðir í staðsetningarleiðbeiningum*. Hægt er að skilgreina margar aðgerðir í staðsetningarleiðbeiningum fyrir hverja línu. Einu sinni enn, númeraröð er notuð til að ákvarða röðun sem aðgerðir eru metnar í. Á þessu stigi er hægt að setja upp fyrirspurn til að skilgreina hvernig á að finna bestu staðsetningu í vöruhúsinu. Einnig er hægt að nota forskilgreint **Stjórnunarstefnu** stillingar til að finna bestu staðsetningu.

## <a name="location-directives-configuration-details"></a>Upplýsingar um skilgreiningu staðsetningarleiðbeininga 

 ### <a name="sequence-number"></a>Raðnúmer
 
Þessi tala sýnir röðina sem unnið er úr staðsetningarleiðbeiningu fyrir valda gerð pöntunar. Hægt er að breyta henni með **Færa upp** og **Færa niður** á valmyndinni.
 
 ### <a name="work-type"></a>Vinnugerð
 
Þetta er gerð vinnu sem á að framkvæma. Gerð vinnu sem eru tiltækir byggist á gerð þeirrar birgðafærslu sem valin er í á **Gerðir vinnupöntunar** svæði.
-   **Frágangur** - verktegund sem jafngildir **Frágangi** merkir að staðsetningarleiðbeiningar finna ákjósanlegustu staðsetninguna til að setja eða staðsetja birgðir á innleið í kerfið, annað hvort frá móttöku, framleiðslu eða birgðirleiðréttingum. Það er einnig hægt að nota til að skilgreina frágang á staðsetningarstig eða útskot fyrir endanlegan afhendingarstað.
-   **Tiltekt** - verktegund sem jafngildir **Tiltekt** merkir að vöruhúsið finnur ákjósanlegustu staðsetninguna til að efnislega taka frá birgðir frá (stofna vinnu). Hægt er að ljúka frágangi (loka vinnulínu frágangs), jafnvel þótt verkið sé ekki lokið. Notandinn getur lokið raunverulegri tínsu, sem er skref í frágangi. Notandinn getur síðan hætt við í farsíma og lokið verkinu síðar. Hins vegar er verkhausinn lokaður þegar frágangi er lokið. 
-   **Talning, Leiðréttingar, Sérsnið, Breyting á birgðastöðu, Röðun númeraplötu, prentun, Stöðubreyting, Pakka í faldaðar númeraplötur** - Þetta er ekki hægt að nota í neinni uppsetningarleiðbeiningu. Þetta er fasttexti þannig að engin sía er tengd við gerð vinnupöntunar. 

### <a name="directive-code"></a>Leiðbeiningarkóði

Veljið kóða staðsetningarleiðbeininga til að tengja við vinnusniðmát eða áfyllingarsniðmát . Á skjámyndinni **Leiðbeiningarkóði** er hægt að búa til nýja kóða sem hægt er að nota sem tengingar milli áfyllingarsniðmáts vinnusniðmáts og staðsetningarleiðbeiningar. Þetta er einnig hægt að nota til að koma á tengingu milli hvaða línu í vinnusniðmáti og staðsetningarleiðbeiningar (eins og útskot eða staðsetningarstig).

Athugaðu að ef kóði er stilltur, þegar vinna er búin til, mun kerfið ekki leita að staðsetningarleiðbeiningunni eftir röð, heldur verður leitað eftir leiðbeiningarkóða. Þetta þýðir að þú getur tilgreint enn frekar hvað staðsetningarsniðmát er notað í tilteknu skrefi í vinnusniðmáti, svo sem flutningur á efni. 

### <a name="site"></a>Svæði

Svæði er áskilinn reitur vegna þess að staðsetningarleiðbeiningar þurfa síðuna og vörugeymsluna sem hún gildir fyrir. 

### <a name="warehouse"></a>Vöruhús

Vörugeymsla er áskilinn reitur vegna þess að staðsetningarleiðbeiningar þurfa síðuna og vörugeymsluna sem hún gildir fyrir.

### <a name="multiple-sku"></a>Margar birgðahaldseiningar

Þetta leyfir margar birgðahaldseiningar (BHE) á staðsetningu, svo sem útskotinu. Ef þú velur **Margar birgðahaldseiningar**, verður frágangsstaðsetningin tilgreind í vinnunni (sem er gert ráð fyrir), en hún mun aðeins geta meðhöndlað frágang á mörgum vörum (ef vinnan inniheldur mismunandi birgðahaldseiningar sem þarf að taka til og ganga frá, ekki frágangur á einni birgðahaldseiningu). Ef þú velur ekki **Margar birgðahaldseiningar** verður frágangsstaðsetningin aðeins tilgreind ef frágangurinn er með aðeins eina gerð af birgðahaldseiningu. Til að nota báðar aðgerðirnar þarftu að tilgreina tvær línur, eina þar sem margar birgðahaldseiningar eru virkar og eina þar sem margar birgðahaldseiningar eru ekki virkar. Þær þurfa að hafa sama skipulag og uppsetningu. Fyrir frágangsaðgerðir þarf að hafa staðsetningarleiðbeiningar sem eru eins, jafnvel þótt þú gerir ekki greinarmun ekki á milli stakra og margra birgðahaldseininga á vinnukenninu. Þú þarft einnig að setja upp fyrir frágang, ef þú ert með pöntun með fleiri en einni vöru.

### <a name="sequence-number"></a>Raðnúmer

Slá skal inn röðina sem línur staðsetningarleiðbeiningar eru unnar fyrir valda vinnutegund. Einnig er hægt að breyta röðinni, ef þörf krefur, með **Færa upp** og **Færa niður**.

### <a name="fromto-quantity"></a>Frá/til magn

Þetta veitir möguleika á að tilgreina magnbil þegar á að velja röðina á hnitanetinu í miðjunni. Þú getur tilgreint Frá/til bilið á magni í viðkomandi einingu.

### <a name="unit"></a>Eining

Hægt er að tilgreina lágmarksmagn og hámarksmagnið sem á við leiðbeiningarnar eiga að gilda um, og hægt er að tilgreina að leiðbeiningarnar eigi að vera fyrir tiltekna birgðaeiningu. Einingareiturinn í línunni er aðeins notaður fyrir magnáætlun.

Þegar athugað er hvort lína staðsetningarleiðbeiningar eigi við mun það byggjast á magninu í viðkomandi einingu sem er tilgreint í línu staðsetningarleiðbeiningar. Í hvert sinn sem línu staðsetningarleiðbeiningar er náð mun kerfið reyna að umbreyta eftirspurnareiningunni í einingu sem er tilgreind í línunni. Ef umbreyting mælieiningar er ekki til, mun það halda áfram í næstu línu. 

### <a name="locate-quantity"></a>Finna magn

Þessi valkostur er aðeins notaður þegar frágangur/staðsetningarmagn er sett í vöruhús. Hann er aðeins fyrir vinnutegund frágangs. Gildu gildin eru:

-   **Magn númeraplötu** - Við mat á því hvort magnið er innan „Frá“ og „Til“ magnbilsins skal nota magnið á númeraplötunni sem berst.
-   **Einingamælt magn** - Við mat á því hvort magnið er innan „Frá“ og „Til“ magnbilsins skal nota magnið sem er einingamælt við tilgreinda færslu.
-   **Eftirstandandi magn** - Við mat á því hvort magnið er innan „Frá“ og „Til“ magnbilsins skal nota magnið sem á eftir að taka á móti í innkaupapöntunarlínu sem verið er að skrá inn.
-   **Væntanlegt magn** - Við mat á því hvort magnið er innan „Frá“ og „Til“ magnbilsins skal nota heildarmagn innkaupapöntunarlínunnar, burtséð frá því hvað hefur þegar verið tekið á móti.

### <a name="restrict-by-unit"></a>Takmarka eftir einingu

Þetta gerir kleyft að lína staðsetningarleiðbeiningar miðist sérstaklega við mælieiningu eða margar mælieiningar. Þegar magn er tekið frá, ef þú vilt aðeins taka frá bretti í tilteknum staðsetningum, þá myndi röðin í hnitanetinu í miðjunni takmarka þessa tilteknu röð við „PL“ þannig að allt magn sem er minna en eitt bretti myndi ekki velja röðina. Veldu **Takmarka eftir einingu** til að setja upp einingarnar. Þú getur einnig takmarkað línuna við fleiri en eina einingu. Þetta virkar eingöngu með staðsetningarleiðbeiningum af tiltektargerð. 

### <a name="round-up-to-unit"></a>Slétta upp í einingu

Þetta svæði vinnur með svæðinu **Takmarka eftir einingu**. Ef línan **Takmarka eftir einingu** fyrir staðsetningarleiðbeiningu er stillt á „kassi“, gefur valið **Slétta upp í einingu** til kynna að vinnan sem er búin til út frá leiðbeiningu fyrir tiltekt á hráefni eigi að vera sléttuð upp í heila afgreiðslueiningu (tilgreint í **Takmarka eftir einingu**). Athugaðu að þetta virkar eingöngu fyrir tiltekt á hráefni og aðeins með staðsetningarleiðbeiningum af tiltektargerð.

### <a name="locate-packing-qty"></a>Staðsetja umbúðamagn

Ef umbúðamagn er tilgreint í sölupöntun, flutningspöntun eða framleiðslupöntun takmarkar það kerfið til að velja aðeins staðsetningar með umbúðamagni í staðsetningunni. Þetta virkar eingöngu með staðsetningarleiðbeiningum af tiltektargerð.

### <a name="allow-split"></a>Leyfa að skipta

Þetta tilgreinir hvort staðsetningarleiðbeiningu sé heimilt að skipta niður magninu sem berst eða magninu sem tekið er frá í mörgum staðsetningum í vöruhúsi, eða ef staðsetja þarf allt magnið á eina staðsetningu eða taka það frá á einni staðsetningu til að geta búið til vinnu. 

### <a name="sequence-number"></a>Raðnúmer

Þessi tala er röðin sem staðsetningarleiðbeiningar eru unnar fyrir valda vinnutegund. Hægt er að breyta röð, ef þörf krefur. Vertu hins vegar varkár þegar raðnúmer eru notuð, þar sem vinnsla mun alltaf vera keyrð í röð. 

### <a name="name"></a>Nafn

Færðu inn nafn á aðgerð staðsetningarleiðbeiningar. Vertu nákvæm/ur þegar þú gefur aðgerðinni nafn.

### <a name="fixed-location-usage"></a>Notkun fastrar staðsetningar 

-   **Fastar og lausar staðsetningar** - staðsetningarleiðbeiningin tekur tillit til allra staðsetninga.
-   **Aðeins fastar staðsetningar fyrir afurðina** - staðsetningarleiðbeiningin tekur aðeins tillit til fastra staðsetninga fyrir afurðir.
-   **Aðeins fastar staðsetningar fyrir afurðinarafbrigðið** - staðsetningarleiðbeiningin tekur aðeins tillit til fastra staðsetninga fyrir afurðarafbrigði.

### <a name="allow-negative-inventory"></a>Heimila neikvæðar birgðir

Veldu til að heimila neikvæða birgðastöðu á tilgreindri staðsetningu vöruhúss í staðsetningarleiðbeiningum. 

### <a name="batch-enabled"></a>Runa virk 

Veldu til að nota runuáætlanir fyrir vörurnar sem eru með runur virkar. Ef komið er að línu þar sem **Runa virk** er stillt með vöru sem ekki er með runu, mun ferlið halda áfram í næstu aðgerðalínu. 

### <a name="strategy"></a>Stjórnunarstefna

-   **Sameina** - Þessi aðferð er notuð til að sameina vörur í tiltekinni staðsetningu þegar líkar vörur eru þegar fyrir hendi. Þetta virkar aðeins fyrir frágangsgerð staðsetningarleiðbeiningar. Algeng uppsetning fyrir frágang verður að sameina í fyrstu aðgerðalínunni og síðan reyna frágang í annarri línunni án sameiningar. Sameining á vörum gerir seinni tiltektir skilvirkari.
-   **Jafna umbúðamagn** - Með þessari stefnu er að finna staðsetningu sem inniheldur leyfismerki með nákvæmu magni sem krafist er. Það er ekki hægt að nota það með staðsetningum sem ekki er stjórnað af númeraplötum. Þessi stefna virkar eingöngu fyrir staðsetningarleiðbeiningu af vinnutegundinni Tiltekt.
-   **Frátekt á FEFO-runu** - Þessi aðferð er notuð þegar birgðir eru staðsettar með lokadag runu og er úthlutað fyrir frátekningu á runu. Aðeins er hægt að nota þessa stjórnunarstefnu fyrir vörur með virka runu. Þetta virkar eingöngu fyrir staðsetningarleiðbeiningu af vinnutegundinni Tiltekt. 
-   **Slétta upp í heila númeraplötu** - Þessi aðferð er notuð til að slétta upp birgðamagnið til að samræma magn á númeraplötu (LP) sem er úthlutað á vörur sem á að taka til. Aðeins er hægt að nota þessa aðferð fyrir áfyllingargerð staðsetningarleiðbeiningar af tiltektargerð. 
-   **Tóm staðsetning með engin verk á innleið** - Þessi aðferð er notuð til að finna tómar staðsetningar. Staðsetning telst autt ef það hefur engar efnislegar birgðir og engin áætluð vinna innleið. Þessi aðferð er aðeins notuð fyrir frágangsgerð staðsetningarleiðbeiningar. 

### <a name="example-of-the-use-of-location-directives"></a>Dæmi um notkun staðsetningarleiðbeiningar

Í þessu dæmi skal íhuga innkaupapöntunarferli þar sem staðsetningarleiðbeiningar verða að finna lausa afkastagetu í vöruhúsi fyrir birgðavara sem hafa einungis verið skráð í móttökusvæðinu. Fyrst þarftu að finna laust pláss innan vöruhússins með því að sameina við fyrirliggjandi lagerbirgðir. Ef sameining er ekki möguleg, þarftu að finna tóma staðsetningu. 

Fyrir þessa atburðarás verður þú að skilgreina tvær aðgerðir staðsetningarleiðbeiningar. Fyrsta aðgerð í röðinni verður að nota í **Sameina** stjórnunarstefnu og annar ætti að nota í **Autt staðsetning með engu verki á innleið** stjórnunarstefnu. Nema þú skilgreinir þriðju aðgerð til að meðhöndla aðstæður yfirflæðis eru tvær niðurstöður mögulegar þegar engin afkastageta er í vöruhúsinu: hægt er að stofna vinnu jafnvel þótt engin staðsetningar eru skilgreindar eða ferli verkstofnunar getur mistekist. Niðurstaðan er ákvarðaður með uppsetningu á **staðsetningarleiðbeiningum** síðuna, þar sem hægt er að ákveða hvort að velja **Stöðva vinnu á misheppnuðum staðsetningarleiðbeiningum** valkost fyrir hverja gerð vinnupöntunar.
