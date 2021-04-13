---
title: Uppsetning tekjuskráningar
description: Þetta efnisatriði lýsir uppsetningarkostum fyrir tekjuskráningu og þýðingu þeirra.
author: kweekley
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 294ad788c97850880b479d3c3c44cc19d55e9a6e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837154"
---
# <a name="revenue-recognition-setup"></a>Uppsetning tekjuskráningar
[!include [banner](../includes/banner.md)]

Nýrri einingu **Tekjuskráningar** hefur verið bætt við sem inniheldur valmyndaratriði fyrir alla uppsetningu sem er nauðsynleg. Þetta efnisatriði lýsir uppsetningarvalkostunum og þýðingu þeirra.

> [!NOTE]
> Ekki er hægt að kveikja á tekjuskráningareiginleikanum í gegnum eiginleikastjórnun. Nota verður skilgreiningarlykil til að kveikja á honum.

> Tekjuskráning, þ.á m. búntaðgerð, er ekki studd fyrir notkun í Commerce-rásum (rafrænum viðskiptum, sölustað, símaveri). Ekki skal bæta vörum, sem skilgreindar eru með tekjuskráningu, við pantanir eða færslur sem stofnaðar eru í Commerce-rásum.

Einingin **Tekjuskráning** er með eftirfarandi uppsetningarvalkosti:

- Færslubækur tekjuskráningar
- Færibreytur fyrir tekjuskráningu
- Tekjuáætlanir 
- Uppsetning birgða

    - Vöruflokkar og útgefnar afurðir
    - Skilgreining tekjuáætlunar
    - Skilgreining tekjuupphæðar

        - Bókunarreglur
        - Búnt

    - Búnthlutir
    - Búntvara

- Verkuppsetning

## <a name="revenue-recognition-journals"></a>Færslubækur tekjuskráningar

Ný færslubókargerð hefur verið kynnt til sögunnar fyrir tekjuskráningu. Færslubókin er áskilin og er notuð í tveimur atburðarrásum.

Fyrri atburðarásin gerist eftir að allar samningsbundnar skyldur eru uppfylltar, þegar frestaðar tekjur eru skráðar með því að stofna tekjuskráningarbók sem byggir á sundurliðun tekjuáætlunarinnar. Færslubókin inniheldur bókhaldsfærslu sem millifærir stöðu úr fjárhagslykli frestaðra tekna í fjárhagslykil tekna.

Seinni atburðarásin gerist þegar færslubók er stofnuð eftir að endurúthlutun á sér stað. Endurúthlutun á sér stað þegar sölupöntunarlínu er bætt við áður reikningsfærða sölupöntun eða þegar ný sölupöntun er stofnuð sem inniheldur línu sem er hluti upprunalega samningsins. Ef reikningur var bókaður áður en nýrri sölupöntunarlínu var bætt við verður að stofna leiðrétta bókhaldsfærslu fyrir bókaðan reikning viðskiptavinar.

Færslubókin er sett upp á síðunni **Færslubókarheiti** (**Tekjuskráning \> Uppsetning \> Færslubókarheiti**). Gerð færslubókar verður að vera stillt á **Tekjuskráning**. Í færslubók tekjuskráningar er hægt að velja bókunarlagið sem á að bóka á.

## <a name="parameters-for-revenue-recognition"></a>Færibreytur fyrir tekjuskráningu

Stillingar tekjuskráningar eru skilgreindar í flipanum **Tekjuskráning** á síðunni **Færibreytur fjárhags** (**Tekjuskráning \> Uppsetning \> Færibreytur fjárhags**). Eftirfarandi stillingar eru tiltækar:

- **Færslubókarheiti tekjuskráningar** – Velja skal færslubókina sem var stofnuð fyrir tekjuskráningu. Færslubókin er nauðsynleg þegar tekjur eru skráðar úr tekjuáætluninni eða þegar sölupöntun sem þegar hefur verið reikningsfærð er endurúthlutað.
- **Virkja úthlutunaraðferð afsláttar** – Stilla skal þennan valkost á **Já** til að ákvarða tekjuupphæð í gegnum úthlutun á sanngjörnu markaðsvirði sem skilgreint er í tekjuupphæð fyrir hverja útgefna afurð. Þessi úthlutun felur í sér úthlutun á öllum línuafsláttum á öllum vörum. Ef þessi valkostur er stilltur á **Nei** notar kerfið miðgildi verðs sem skilgreint er í tekjuupphæð fyrir hverja útgefna afurð. Ef þessi valkostur er stilltur á **Nei**, en ekkert miðgildi verðs er uppsett fyrir útgefnar afurðir, mun úthlutun á tekjuupphæð ekki eiga sér stað.
- **Hafa hausaafslátt með** – Stilla skal þennan valkost á **Já** til að ákvarða tekjuupphæð með úthlutun hausaafsláttar fyrir afurðir. Ef þessi valkostur er stilltur á **Nei** er hausaafsláttur ekki tekinn með við úthlutun tekjuupphæðar.
- **Gera samningsskilmála óvirka** – Stilla skal þennan valkost á **Já** ef gefa má út afurðir sem eru af tekjugerðinni **Stuðningur á samningstíma** jafnvel þótt upphafs- og lokadagsetningar samnings séu ekki skilgreindar fyrir þær. Yfirleitt er krafist upphafs- og lokadagsetningar samnings fyrir vörur af tekjugerðinni **Stuðningur á samningstíma**. Þegar upphafs-og lokadagsetningar samnings eru ekki skilgreindar er sundurliðun tekjuáætlunar í bókun reiknuð með því að nota fjölda tilvika og dagsetningu reikningsins.
- **Bóka leiðréttingar á reikningi fyrir viðskiptakröfur við endurúthlutun** – Við endurúthlutun reikninga sem hafa þegar verið bókaðir þarf að leiðrétta bókhaldsfærsluna fyrir bókaðan reikning. Nota skal þennan valkost til að tilgreina hvernig á að leiðrétta.

    - Stillið þennan valkost á **Nei** til að takmarka bókun leiðréttingarfærslu við fjárhag. Þegar þessi valkostur er stilltur á **Nei** eru engin önnur skjöl stofnuð í Viðskiptakröfur fyrir leiðréttingu innri bókhalds. Þegar reikningur er greiddur notar uppgjörsferlið gömlu bókhaldsfærsluna til að bóka alla staðgreiðsluafslætti eða innleystan hagnað eða tap.
    - Stilla skal þennan valkost á **Já** til að sjálfkrafa stofna bakfærsluskjal og nýjan reikning fyrir leiðréttingarfærsluna í viðskiptakröfum. Þar sem þessi leiðrétting er leiðrétting á innra bókhaldi eru nýju skjölin hvorki send til viðskiptavinar né hann látinn vita af þeim. Bakfærsluskjalið er jafnað við upprunalegan reikning og nýr leiðréttur reikningur er greiddur af viðskiptavininum. Athugið að öll þrjú skjölin eru sýnd á skýrslum, eins og á yfirliti viðskiptavinar.

[![Upplýsingar um uppsetningu](./media/revenue-recognition-setup-info.png)](./media/revenue-recognition-setup-info.png)

## <a name="revenue-schedules"></a>Tekjuáætlanir

Stofna verður tekjuáætlun fyrir hvert tilvik þar sem hægt er að fresta tekjum. Ef fyrirtækið býður t.d. upp á stuðning í sex mánuði, 12 mánuði, 18 mánuði og 24 mánuði verður að stofna tekjuáætlun fyrir hvert tímabil. Uppsetning tekjuáætlunarinnar ákvarðar hvernig tekjum er úthlutað á milli fjölda tímabila sem eru valin. Hún ákvarðar einnig sjálfgefnu dagsetningarnar sem eru færðar inn fyrir tekjuáætlunina sem er stofnuð þegar reikningurinn er bókaður.

Ef tekjur eru skráðar eftir þáttaskilum er mælt með því að stofna tekjuskráningaráætlun fyrir öll þáttaskilin, óháð skráningardagsetningunum. Þegar búið er að stofna áætlanirnar er hægt að breyta þeim þannig að þær endurspegli áætlaðar dagsetningar þáttaskila. Hægt er að setja þessar færslur í bið þar til tilkynnt hefur verið að þáttaskilum hafi verið náð og hægt sé að skrá tekjurnar.

Tekjuáætlanir eru stofnaðar á síðunni **Tekjuáætlanir** (**Tekjuskráning \> Uppsetning \> Tekjuáætlanir**).

[![Tekjuáætlanir](./media/revenue-recognition-revenue-schedules.png)](./media/revenue-recognition-revenue-schedules.png)

Sláið inn lýsandi gildi í reitina **Tekjuáætlun** og **Lýsing**. Eftirfarandi viðbótarstillingar eru notaðar til að stofna tekjuáætlunina þegar reikningurinn er bókaður.

- **Tilvik** – Færa skal inn fjölda mánaða eða tilvika fyrir frestun á tekjum.
- **Sjálfvirk bið** – Velja skal þennan gátreit ef setja á allar línur tekjuáætlunar í bið við bókun reiknings. Biðstöðuna þarf að fjarlægja handvirkt úr hverri línu áætlunarinnar áður en hægt er að skrá frestaðar tekjur línunnar.
- **Sjálfvirkir samningsskilmálar** – Veljið þennan gátreit ef stilla á upphafs-og lokadagsetningar samningsins sjálfkrafa. Þessar dagsetningar eru eingöngu stilltar sjálfkrafa fyrir útgefnar afurðir af tekjugerðinni **Stuðningur á samningstíma**. Upphafsdagsetning samnings er sjálfkrafa stillt á umbeðna sendingardagsetningu sölupöntunarlínu og lokadagsetning samnings er sjálfkrafa stillt á upphafsdagsetningu að viðbættum fjölda mánaða eða tilvika sem er skilgreint í uppsetningu tekjuáætlunar. Til dæmis er afurðin á sölupöntunarlínunni fyrir eins ára ábyrgð. Sjálfgefin tekjuáætlun er **12M** (12 mánuðir) og gátreiturinn **Sjálfvirkir samningsskilmálar** er valinn fyrir þessa tekjuáætlun. Ef sölupöntunarlínan er með umbeðna sendingardagsetningu 16. desember 2019 verður sjálfgefin upphafsdagsetning samnings að 16. desember 2019 og sjálfgefin lokadagsetning samnings verður að 15. desember 2020.
- **Skráningargrunnur** – Skráningargrunnurinn ákvarðar hvernig tekjuupphæð er úthlutað á milli tilvika.

    - **Mánaðarlega eftir dagsetningum** – Upphæðinni er úthlutað samkvæmt raunverulegum dögum í hverjum mánuði.
    - **Mánaðarlega** – Upphæðinni er úthlutað jafnt yfir fjölda mánaða sem er skilgreindur í tilvikunum.
    - **Tilvik** – Upphæðinni er úthlutað jafnt á milli tilvika, en það getur falið í sér aukalegt tímabil ef **Raunveruleg upphafsdagsetning** er valin sem viðtekin skráning.

- **Viðtekin skráning** – Viðtekin skráning ákvarðar sjálfgefnu dagsetningarnar sem eru stilltar í tekjuáætluninni fyrir reikninginn.

    - **Raunveruleg upphafsdagsetning** – Áætlunin er stofnuð með því að nota annaðhvort upphafsdagsetningu samningsins (fyrir vörur með stuðning á samningstíma \[PCS\]) eða reikningsdagsetninguna (fyrir nauðsynlegar og ónauðsynlegar vörur).
    - **Fyrsti dagur mánaðar** – Dagsetning fyrstu áætlunarlínunnar er upphafsdagsetning (eða reikningsdagsetning) samningsins. Hins vegar eru allar síðari áætlunarlínurnar stofnaðar fyrir fyrsta dag mánaðar.
    - **Skipting um miðbik mánaðar** – Dagsetning fyrstu áætlunarlínunnar fer eftir reikningsdagsetningunni. Ef búið er að bóka reikninginn fyrir fimmtánda dag mánaðarins er tekjuáætlunin búin til með fyrsta degi mánaðarins. Ef búið er að bóka reikninginn á sextánda degi mánaðarins eða síðar stofnast tekjuáætlunin með fyrsta degi næsta mánaðar.
    - **Fyrsti dagur næsta mánaðar** – Dagsetning áætlunarinnar er fyrsti dagur næsta mánaðar.

Velja skal hnappinn **Sundurliðun tekjuáætlunar** til að skoða almenn tímabil og prósenturnar sem eru skráðar á hverju tímabili. Sjálfgefið er að gildinu **Skrá prósentu** sé skipt jafnt á milli fjölda tímabila. Ef skráningargrunnurinn er stilltur á annaðhvort **Mánaðarlega** eða **Tilvik** er hægt að breyta skráðri prósentu. Við breytingu á skráðri prósentu koma upp viðvörunarboð um að samtalan jafngildi ekki 100 prósentum. Ef þú færð skilaboðin er hægt að halda áfram að breyta línum. Hins vegar verður heildarupphæðin að vera jöfn 100 áður en síðunni er lokað.

[![Sundurliðun tekjuáætlunar](./media/revenue-recognition-revenue-schedule-details.png)](./media/revenue-recognition-revenue-schedule-details.png)

## <a name="inventory-setup"></a>Uppsetning birgða

Hægt er að skrá tekjur fyrir útgefnar afurðir í sölupöntunum, en ekki með söluflokkum í sölupöntunum eða með reikningum með frjálsum texta ef engar vörur eru í skjalinu. Það sem valið er við uppsetningu útgefinna afurða ákvarðar hvernig tekjur vöru eru skráðar. Til dæmis ákvarðast það af valinu hvort tekjuupphæðinni sé úthlutað og hvort tekjunum sé frestað með tekjuáætlun.

Uppsetningin getur hafist í flýtiflipanum **Tekjuskráning** á síðunni **Vöruflokkur** (**Tekjuskráning \> Uppsetning \> Birgða- og afurðauppsetning \> Vöruflokkur**). Á þessari síðu eru nokkrir uppsetningarreitir. Þessir reitir eru notaðir til að stilla sjálfgefin gildi aðeins fyrir nýjar útgefnar afurðir sem eru stofnaðar í kerfinu. Þegar nýjar afurðir eru stofnaðar eru gildin sem eru sett hér inn sjálfkrafa slegin inn fyrir vöruflokkinn. Hægt er að hnekkja sjálfgildum fyrir útgefnar afurðir á síðunni **Útgefnar afurðir** (**Tekjuskráning \> Uppsetning \> Birgða- og afurðauppsetning \> Útgefnar afurðir**). Sjálfgefin gildi sem eru stillt fyrir útgefnar afurðir eru síðan flutt í sölupöntunina.

## <a name="item-groups-and-released-products"></a>Vöruflokkar og útgefnar afurðir

### <a name="define-the-revenue-schedule"></a>Skilgreina tekjuáætlunina

Tekjum á sölupöntunarlínu er frestað ef tekjuáætlun er skilgreind fyrir útgefna afurð og sjálfgefið notuð á sölupöntunarlínunni. Ef nota á stillinguna sjálfkrafa fyrir afurðina er hægt að skilgreina tekjuáætlunina í flýtiflipanum **Tekjuskráning** á síðunni **Vöruflokkur** (**Tekjuskráning \> Uppsetning \> Birgða- og afurðauppsetning \> Vöruflokkur**). Einnig er hægt að skilgreina stillingu útgefinnar afurðar í flýtiflipanum **Tekjuskráning** á síðunni **Útgefnar afurðir** (**Tekjuskráning \> Uppsetning \> Uppsetning birgða \> Útgefnar afurðir**).

Í reitnum **Tekjuáætlun** er tekjuáætlun valin sem stendur fyrir tímabilið sem á að fresta tekjum yfir. Tekjuáætlunin er sjálfkrafa færð inn í sölupöntunarlínuna og sundurliðun áætlunar er búin til þegar sölupöntunarreikningur er bókaður.

### <a name="define-the-revenue-price"></a>Skilgreina tekjuupphæð

Hægt er að setja upp vöruflokka og útgefnar afurðir með því að nota annaðhvort miðgildisaðferð eða afsláttaraðferð. Báðar aðferðirnar þurfa á ýmsum stillingum að halda á síðunni **Útgefnar afurðir**:

- **Er tekjuúthlutun virk** – Stilla skal þennan valkost á **Já** til að hafa útgefnu afurðina með í útreikningi tekjuúthlutunar. Ef þessi valkostur er stilltur á **Nei** notar útgefin afurð miðgildi ef miðgildi verðs er skilgreint. Ef miðgildi verðs er ekki skilgreint er einingarverðið á sölupöntunarlínunni notað til að bóka í tekjur eða frestaðar tekjur.
- **Tekjugerð** – Veljið tekjugerð sem skilgreinir útgefna afurð:

    - **Nauðsynleg** – Varan er ein helsta tekjulind fyrirtækis. Þetta gildi er sjálfgefin stilling.
    - **Ónauðsynleg** – Varan er ekki ein helsta tekjulind fyrirtækis. Þegar verðstillingar fyrir miðgildi eru notaðar er verðið fest á miðgildi verðs og því næst úthlutað. Til dæmis er nauðsynleg vara með fast verð sem verður að vera skráð fyrir tekjur. Ef afsláttur er til staðar gæti hann verið fjarlægður úr tekjum nauðsynlegrar vöru, en **aðeins** að upphæð fasta verðsins. Afgangurinn af afslættinum er tekinn út úr tekjum fyrir ónauðsynleg atriði. Að öðrum kosti er ekki víst að afslátturinn verði fjarlægður úr tekjum nauðsynlegrar vöru.
    - **Stuðningur á samningstíma** – Varan styður aðrar einingar sem eru innifaldar í sölunni til viðskiptavinarins. Tekjuupphæðinni er dreift á milli nauðsynlegra og ónauðsynlegra afurða sem eru innifaldar í sölunni. Það fer eftir uppsetningu, en PCS-vörur þurfa kannski ekki á skilgreindum upphafs- og lokadagsetningum samnings að halda í sölupöntunarlínunni.

- **Útiloka fjarlægingu** – Stilla skal þennan valkost á **Já** til að gefa til kynna að ekki sé hægt að færa miðgildi vöruverðs niður fyrir lágmarksprósentuna sem er skilgreind eða yfir hámarksprósentuna. Allar tekjuupphæðir verða byggðar á tekjuupphæð annarrar útgefinnar afurðar sem er að finna í sölupöntuninni. Ef þessi valkostur er stilltur á **Nei** er hægt að breyta miðgildi vöruverðs eða taka það út. Athugið að ef fleiri en ein vara er seld með miðgildi verðs uppsett verður að setja upp að minnsta kosti eina útgefna afurð þar sem valkosturinn **Útiloka fjarlægingu** er stilltur á **Nei**. Þannig er að minnsta kosti ein vara til staðar sem hægt er að úthluta verðmismun á.
- **Miðgildi verðs** – Stilla skal þennan valkost á **Já** til að gefa til kynna að leiðrétta eigi tekjuupphæð vöru þannig að hún jafngildi miðgildi verðs ef hún er undir tilgreindum lágmarksvikmörkum eða yfir hámarksvikmörkum, og að upphæð sem tekin er út skuli vera úthlutað til lína sem eru með afurðir þar sem valkosturinn **Útiloka fjarlægingu** er stilltur á **Nei**.

    - **Hámarksvikmörk** – Færið inn prósentu yfir miðgildi verðs sem er leyfð.
    - **Lágmarksvikmörk** – Færið inn prósentu undir miðgildi verðs sem er leyfð.

Þegar búið er að skilgreina stillingar fyrir útgefna afurð þarf að skilgreina handvirkt tekjuupphæð með því að færa inn gangvirði eða miðgildi verðs (ef miðgildisaðferð verðs er notuð) á síðuna **Tekjuupphæðir** (opna skal **Tekjuskráning \> Uppsetning \> Uppsetning birgða \> Útgefnar afurðir** og síðan, á aðgerðasvæðinu, í flipanum **Selja**, í flokknum **Tekjuskráning**, skal velja **Tekjuupphæðir**).

[![Tekjuupphæðir](./media/revenue-recognition-revenue-prices.png)](./media/revenue-recognition-revenue-prices.png)

Tekjuupphæðin sem er skilgreind handvirkt á þessari síðu er notuð til að ákvarða úthlutun tekjuupphæðar á hverja sölupöntun sem byggir á skilyrðinu sem skilgreint er. Hvert skilyrði er borið saman við sölupöntunarlínuna til að ákvarða tekjuupphæðina sem á að nota í úthlutunarferlinu.

- **Vörukóði** og **Vöruvensl** – Hægt er að skilgreina tekjuupphæð fyrir eina afurð eða hóp afurða. Ef valið er **Tafla** í reitnum **Vörukóði** skal velja útgefnu afurðina í reitnum **Vöruvensl**. Ef valið er **Flokkur** í reitnum **Vörukóði** skal velja vöruflokkinn í reitnum **Vöruvensl**.
- **Kóði lykils** og **Númer reiknings/flokks** – Hægt er að skilgreina tekjuupphæð fyrir alla viðskiptavini, einn viðskiptavin eða viðskiptavinahóp. Ef valið er **Allir** í reitnum **Kóði lykils** er verðið notað fyrir alla viðskiptavini. Ef valið er **Tafla** í reitnum **Kóði lykils** skal velja viðskiptavininn í reitnum **Númer reiknings/flokks**. Ef valið er **Flokkur** í reitnum **Kóði lykils** skal velja viðskiptavinahópinn í reitnum **Númer reiknings/flokks**.
- **Gjaldmiðill** – Færa verður inn aðskilda tekjuupphæð fyrir hvern gjaldmiðil sem sölupöntun er færð inn í. Ef sala er t.d. í bandarískum dollurum, kanadískum dollurum og evrum, verður að skilgreina verð tekna í öllum þremur gjaldmiðlunum. Tekjuupphæðin er ekki umreiknuð frá einum gjaldmiðli, svo sem bókhaldsgjaldmiðlinum, yfir í annan færslugjaldmiðil sem verið er að nota.
- **Upphæð eða prósenta af lista** – Tilgreina skal hvort tekjuupphæðin sé uppsett sem upphæð eða sem prósenta af listaverði. Ef valið er **Prósenta af lista** geta notendur fært inn miðgildi verðs sem prósentu af listaverði í stað upphæðar. Gildið **Prósenta af lista** er aðeins notuð fyrir útgefnar afurðir sem eru uppsettar sem PCS-vörur.
- **Upphæð tekjuúthlutunar** – Það fer eftir gildinu sem var valið í reitnum **Upphæð eða prósenta af lista** hvort skuli færa inn upphæð eða prósentu til að sýna tekjuupphæðina sem notuð er til að úthluta tekjunum á milli eininga sölupöntunarinnar.
- **Dagsetning frá** og **Dagsetning til** – Færa skal inn tímabilið þegar tekjuupphæðin er í gildi. Þessir reitir eru valfrjálsir.

Ef valkosturinn **Virkja úthlutunaraðferð afsláttar** á síðunni **Færibreytur fjárhags** er stilltur á **Já** og ef reiturinn **Tekjugerð** fyrir útgefnu afurðina er stilltur á **Stuðningur á samningstíma** þarf líka að tilgreina vörurnar sem útgefna afurðin styður. Þessi uppsetning er gerð á síðunni **Uppsetningargrunnur** (opna skal **Tekjuskráning \> Uppsetning \> Uppsetning birgða \> Útgefnar afurðir** og síðan, á aðgerðasvæðinu, í flipanum **Selja**, í flokknum **Tekjuskráning**, skal velja **Uppsetningargrunnur**).

Á síðunni **Uppsetningargrunnur** skal bæta við færslu fyrir hvern vöruflokk sem varan styður. Þegar tekjuúthlutun á sér stað verður tekjuupphæðinni dreift á milli nauðsynlegra og ónauðsynlegra hluta PCS-vörunnar.

### <a name="posting-profiles"></a>Bókunarreglur

Þrjár aðrar bókunargerðir styðja við möguleikann á frestun tekna. Þessar bókunargerðir eru settar upp í flipanum **Sölupöntun** á síðunni **Bókun** (**Tekjuskráning \> Uppsetning \> Birgða- og afurðauppsetning \> Bókun**).

- **Frestaðar tekjur** – Færa skal inn aðallykil fyrir tekjuupphæðina sem bókar frestaðar tekjur (í stað tekna). Tekjuupphæð er frestað ef sölupöntunarlína er með tekjuáætlun.
- **Frestaður kostnaður seldra vara** – Færa skal inn aðallykil fyrir kostnaðarupphæð seldra vara sem bókar frestaðan kostnað seldra vara ef tekjum er einnig frestað.
- **Hreinsun á tekjum hlutareiknings** – Færa skal inn aðallykil fyrir millireikning sem er annaðhvort notaður þegar sölupöntunin er reikningsfærð að hluta til eða þegar endurúthlutun á sér stað. Staðan á þessum reikningi verður aftur að 0 (núlli) þegar sölupantanirnar eru reikningsfærðar að fullu.

### <a name="bundles"></a>Búnt

Búntvörur eru einkvæmar útgefnar afurðir sem eru settar upp þannig að þær innihaldi hluta. Uppsetningin er gerð með því að nota uppskriftavirknina. Þegar búntvara er færð inn í sölupöntun eru einstakir hlutar notaðir til að ákvarða tekjuupphæðir og tekjuáætlanir. Hins vegar endurspegla skjöl sem eru prentuð fyrir viðskiptavininn, svo sem sölupöntun og reikningur, búntvöruna.

#### <a name="bundle-components"></a>Búnthlutir

Hlutirnir sem teknir eru með í búntið verða að vera settir upp á síðunni **Útgefnar afurðir** (**Tekjuskráning \> Uppsetning \> Birgða-og afurðauppsetning \> Útgefnar afurðir**). Þessir hlutir eru útgefnar afurðir og nauðsynlegt er að setja þá upp á sama hátt og afurðir sem eru hluti af uppskrift. Til dæmis getur útgefin afurð verið vara annaðhvort af gerðinni **Vara** eða **Þjónusta**, en henni verður að vera úthlutað á vörulíkanaflokk þar sem valkosturinn **Afurð í birgðum** er stilltur á **Já**. Frekari upplýsingar er að finna í leiðbeiningum um uppsetningu uppskriftavara.

Einnig þarf að setja upp tekjuskráningu fyrir hluta, rétt eins og þeir væru afurðir sem hægt er að selja stakar með sölupöntun. Til dæmis skal ganga úr skugga um að rétt verðlag sé skilgreint fyrir hvern hluta og að verðgrunnurinn sé settur upp fyrir stykkjavörur.

#### <a name="bundle-items"></a>Búntvörur

Þegar búið er að setja upp búntvöru þarf að stilla tvo reiti á síðunni **Útgefnar afurðir** (**Tekjuskráning \> Uppsetning \> Birgða-og afurðauppsetning \> Útgefnar afurðir**):

- Í flýtiflipanum **Hanna**, í reitnum **Framleiðslugerð**, þarf að setja vöruna upp sem uppskriftarvöru.
- Í flýtiflipanum **Almennt**, í reitnum **Búnt**, þarf að merkja vöruna sem búntvöru.

Hlutunum verður þá að vera úthlutað til yfirbúnt-/yfiruppskriftarvöru á síðunni **Uppskriftarútgáfur** (opna skal **Tekjuskráning \> Uppsetning \> Birgða- og afurðauppsetning \> Útgefnar afurðir** og síðan, á aðgerðasvæðinu, í flipanum **Hanna**, í flokknum **Uppskrift**, skal velja **Uppskriftarútgáfur**). Frekari upplýsingar er að finna í leiðbeiningum um uppsetningu uppskrifta.

[![Útgefnar afurðir, uppskriftaáætlanir](./media/revenue-recognition-bom-scheduleds.jpg)](./media/revenue-recognition-bom-scheduleds.jpg)

Ef yfirvara búnts og búnthlutar eru stilltir á úthlutun verður tekjuupphæðum búnts dreift á milli hlutanna samkvæmt prósentuhluta tekna þeirra.

## <a name="project-setup"></a>Verkuppsetning

Einnig er hægt að nota tekjuskráningu fyrir sölupantanir sem eru stofnaðar í tíma- og efnisverki. Fyrir sölupantanir sem eiga uppruna sinn í verkum þarf aðeins að skilgreina aðallykla í verkbókunarreglum sem eru notaðar til að bóka verkreikninga. Aðallyklar eru skilgreindir á síðunni **Uppsetning fjárhagsbókunar** (**Tekjuskráning \> Uppsetning \> Verkuppsetning \> Uppsetning fjárhagsbókunar**).

- **Frestaðar tekjur reiknings** (undir **Tekjulyklar**) – Færa skal inn aðallykil fyrir tekjuupphæðina sem bókar frestaðar tekjur (í stað tekna). Tekjuupphæð er frestað ef sölupöntunarlína er með tekjuáætlun.
- **Frestaður kostnaður** (undir **Kostnaðarlyklar**) – Færið inn aðallykil fyrir kostnað seldra vara sem bókar frestaðan kostnað seldra vara ef tekjum er einnig frestað.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]