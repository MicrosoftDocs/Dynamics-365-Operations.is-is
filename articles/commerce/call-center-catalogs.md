---
title: Vörulistar símavers
description: Þetta efnisatriði lýsir sértækri virkni símavera fyrir vörulista í Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 05/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailMCRChannelDetailPage, RetailCatalogDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e4d2b1f4b7fb9394f54674f9622c8a8edd435311
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022878"
---
# <a name="call-center-catalogs"></a>Vörulistar símavers

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir sértækri virkni símavera sem tengist eiginleikum vörulista í Dynamics 365 Commerce.

Vörulistaeiginleikar sem finnast í Commerce koma að margskonar notum. Upphaflega voru vörulistaeiginleikarnir stofnaðir til að styðja við samþættingu rafrænna viðskipta þriðja aðila. Uppsetning vörulista heimilaði fyrirtækjum að búa til flokkun á vörum og eiginleikum sem hægt væri að birta út á við til notkunar í rafrænni viðskiptalausn þriðja aðila.

Þegar notendaþjónustu fyrir rás símavers var bætt við var vörulistahugtakið útvíkkað til að bæta við viðbótareiginleikum fyrir stuðning og stjórn á eiginleikum tengdum hefðbundnum markaðssetningarvörulistum sem selur beint til neytenda. Fyrirtæki sem selur beint til neytenda mun oft framleiða prentaðar vörulistar, sem síðan eru sendar til eins eða fleiri hluta viðskiptavina. Þessar vörulistar innihalda yfirleitt sérstakar kynningar eða tilboð sem aðeins öðlast gildi ef viðskiptavinurinn gefur upp auðkenniskóða við stofnun pöntunar.

Markaðsfyrirtæki sem selja beint til neytenda eru mjög upptekin af því að rekja svörun tengda vörulistunum til að tryggja að kostnaður við framleiðslu þeirra og póstsendingu sé réttlætanleg. Til að fylgjast með svöruninni er kóðinn venjulega prentaður á bakhlið vörulistans og síðan er beðið um kóðann og hann notaður þegar vörulistamóttakandi hringir til að leggja inn pöntun í síma (eða nú til dags er vanalegra að kóðinn sé sleginn inn þegar viðskiptavinurinn leggur inn pöntun á netinu). Þó að mismunandi iðnaðarhugtök séu notaðar til að bera kennsl á þennan rakningarkóða vörulista (þar með talið lykilkóði, kynningarkóði, vörulistakóði, frumkóði), vísum við til kóðans í Commerce sem **Frumkóðakenni**.

## <a name="basic-catalog-setup"></a>Grunnuppsetning vörulista

Farðu í **Retail og Commerce** \> **Vörulistar og vöruúrval** \> **Allir vörulistar** til að grunnstilla vörulistann þinn.

Þegar þú býrð til nýjan vörulista þarftu fyrst að tengja vörulistann við einn eða fleiri sölurásir. Þetta er gert á flýtiflipanum **Commerce-rásir** í skjámyndinni **Uppsetning vörulista**. Smella á **Bæta við** og velja einn eða fleiri sölurásir. Aðeins er hægt að nota vörur sem tengjast [vöruúrval](https://docs.microsoft.com/dynamics365/unified-operations/retail/assortments) völdu rásarinnar þinnar þegar þú býrð til vörulistann.

Til að bæta vöru við vörulista þarf yfirlitsstigveldi að vera valið. Yfirlitsstigveldið mun styðja við skipan flokkanna fyrir vörulistann. Þú verður að velja úr einu af yfirlitsstigveldunum sem tengjast smásölurásunum sem eru valdar á flýtiflipanum **Commerce-sölurás** á síðunni **Vörulisti**. Ef yfirlitsrás var ekki tengd við rás áður skal fara í **Retail og Commerce** \> **Rásaruppsetning** \> **Rásarflokkar og afurðareigindir** til að tengja sjálfgildi yfirlitsstigveldis við sérhverja sölurás þína.

Á **Vörulistar** valmyndarflipanum á **Uppsetning vörulista** síðunni er smellt á **Bæta við vörum** til að grunnstilla vörur sem bæta á við vörulista, eða veldu hnút í yfirlitsstigveldinu (velja hnút mun breyta skjáframsetningunni og gera þér kleift að bæta vörum beint við flokk innan vörulistans).

Smelltu á efsta hnútinn í yfirlitsstigveldinu til að fara aftur í aðal hausyfirlit vörulistans. Grunnstilla upphafs- og lokadagsetningu eins og nauðsyn krefur á **Almennt** flýtiflipanum.

Áður en vörulistinn er tiltækur til notkunar verður hann að vera birtur. Smelltu **Sannprófa vörulista** á **Vörulistar** valmyndinni til að setja sannprófun í ferli. Þetta er nauðsynlegt aðgerð og sannprófar að uppsetningin sem krafist er sé rétt. Smella á **Skoða niðurstöður** til að sjá upplýsingar um sannprófun. Ef villur finnast verður þú að leiðrétta gögnin og keyra sannprófun aftur þar til sannprófunin er fullnægjandi.

Eftir að sannprófun er staðfest, skal smella á **verkflæði** á valmyndinni til að hefja samþykktarverkflæði. Smella á **Senda inn** á **Verkflæði** valmyndina til að framkvæma ferlið. Grunnstilla skrefin og samþykkta notendur fyrir verkflæðið frá **Retail og Commerce** \> **Uppsetning höfuðstöðva** \> **Verkflæði Commerce**. Verkflæðið mun skilgreina þau skref sem þarf að framkvæma til að fá vörulistann í **Samþykkt** stöðu. Þegar vörulistinn er í **Samþykkt** stöðu getur þú smellt á **Birta** valkostinn á **Vörulistar** valmyndinni til að ljúka ferlinu. Eftir að vörulistinn er í **Birtur** stöðu, er hægt að nota hann í ferli sem nær yfir pöntunarfærslu í símaveri og sendingu vörulista.

## <a name="use-catalogs-to-drive-sales-order-pricing-and-promotions"></a>Notaðu vörulista til að keyra verðlagningu sölupöntunar og kynningartilboð

Aðalástæða þess að skilgreina vörulista til notkunar með símaveri er að geta grunnstillt tiltekið verð og kynningartilboð fyrir þann vörulista. Viðskiptavinir sem panta frá þessum vörulista fá þessa verð og kynningartilboð í pöntunarfærslu símarvers ef **frumkóðakenni** vörulistans er notaður í pöntunarhaus eða línum.

Til að grunnstilla tiltekið verð vörulista skal velja **Verðflokkar** valkostinn úr **Vörulistar** flipanum til að tengja einn eða fleiri verðflokka við vörulistann. Allar viðskiptasamningar, verðleiðréttingarbækur og sérstakir afslættir (þröskuldur, magn, blanda og samsvörun) sem hafa verið tengd sömu verðflokki verður beitt þegar viðskiptavinir panta frá þessum vörulista.

Á **Frumkóðar** flýtiflipanum skal smella á **Bæta við** til að bæta við einum eða fleiri kennimerkjum fyrir **Frumkóðakenni** í þennan vörulista. Þetta er kóðinn sem verður notaður á sölupöntunarhausinn (og línur) á meðan pöntunarfærsla í símaveri á sér stað. Þessi kóði er notuð til að tengja sölupöntunina við vörulistann og að lokum við verðflokka og öll sérstakt verð og kynningartilboð sem hafa verið grunnstillt.

## <a name="use-the-source-id-to-track-costs-and-response-rates"></a>Notaðu frumkennið til að fylgjast með kostnaði og svarhlutfalli

Þegar þú skilgreinir **Frumkóðakenni**, getur þú valið um að tengja þetta kenni við **Markhópskenni**. **Markhópskenni** er hægt að skilgreina í **Retail og Commerce** \> **Viðskiptavinir** \> **Markhópur**. Markhópurinn listi yfir viðskiptavini og/eða viðföng sem tilheyra notandaskilgreindum hluta. Tenging gagna um viðskiptavini eða viðföng við frumkóðakenni gerir viðtakendur vörulistans sýnilegri. Ef viðskiptavinur er tengdur við markhóp og sá markhópur er tengdur við virkt frumkóðakenni/vörulista, munu notendur símavers geta séð hvaða vörulista viðskiptavinur hefur fengið með því að velja **Frumkóðar** valkostinn á valmyndinni á **Viðskiptavinir** valmyndaflipanum á **Notendaþjónusta** síðunni. Meðan á pöntunarfærslu stendur geta notendur símavers einnig séð sértæka vörulista sem viðskiptavinur voru sendir í **Uppruni** fellilistanum á sölupöntunarhausnum. Að breyta afmörkun frá **Allir** til **Miðaðir** leyfir notandanum að sjá tiltekna virka vörulista sem viðskiptavinurinn var sendur. Þetta er gagnlegt í aðstæðum þar sem viðskiptavinurinn kann að hafa gleymt vörulistanum sínum eða getur ekki fundið eða lesið vörulistakóðann þegar þeir hringja til að stofna sölupöntun.

Það er hægt að tengja mörg frumkóðakenni við vörulista. Þetta er oft þarft þegar fyrirtæki vill fylgjast með svörunarhlutfallinu eftir mismunandi hlutum. Fyrirtækið mun setja sérstaka vörulistakóða á mismunandi hluta viðskiptavina, sem gerir kleift að fylgjast með svörunarhlutfalli niður á hlutastigið, innan tiltekins vörulistatilviks.

Ef valið er tiltekin **Frumkóðakenni** skrá og smellt á **Upplýsingar** valkostinn á **Frumkóðar** flýtiflipanum, birtast viðbótarreitir þar sem hægt er að ná í söluspár, póstkostnað og póstdagsetningar. Þessi gögn eru gagnleg til að gera nákvæma greiningu á skilvirkni vörulista. Notendur geta farið aftur á þessa síðu með tímanum og notað **Frumkóðagreining** og **Bera saman kynningartilboð** hnappana til að kalla fram greiningarskýrslur sem byggjast á fyrirliggjandi sölugögnum og bera saman kostnað og fjárhagsáætlun við rauntölur.

## <a name="configure-catalog-specific-order-and-item-scripts"></a>Grunnstilla pöntun sem tengist tilgreindum vörulista og vöruforskriftir

Þegar notandi símavers býr til sölupöntun, getur hann notað forskriftir á skjánum. Þessar forskriftir, sem eru byggðar á texta, kunna að veita viðbótarupplýsingar sem notandinn ætti að koma á framfæri við viðskiptavininn, eða það kann að vera innri athugasemdir/áminningar sem notandi símavers ætti að endurskoða og bregðast við um leið og hann býr til sölupöntunina.

Það er oft gagnlegt að hafa mismunandi forskriftir fyrir mismunandi vörulista. Á **Forskriftir** flýtiflipanum er hægt að tengja fyrirfram skilgreindar forskriftir við vörulista. Notaðu **Tímasetning** reitinn til að ákvarða hvort forskriftin skuli birtast í upphafi pöntunarinnar (um leið og frumkóðinn er sleginn inn á pöntunarhausinn) eða í lok pöntunarinnar (í samantektarskjámynd sölupöntunarinnar).

Þegar valinn er hnútur í stigveldi vörulistans og unnið með gögnin á **Vörur** flýtiflipanum, er einnig hægt að tengja forskriftir sem eru sértækar fyrir vörulista eða vörur með því að nota **Forskriftir** aðgerðina.

## <a name="configure-catalog-specific-up-sell-and-cross-sell-items"></a>Grunnstilla söluviðauka sem tengist tilteknum vörulista og viðbótarsöluvörur

Hægt er að tengja tillögur um söluviðauka/viðbótarsölu við vöru, í vöruuppsetningunni. En í sumum tilfellum gæti fyrirtæki viljað kynna sértæka söluviðauka/viðbótarsöluvörur fyrir viðskiptavinum sem panta tiltekna vöru úr tilteknum vörulista. Í **Vörur** flýtiflipanum skal velja vöru og smella á **söluviðauki/viðbótarsöluvörur** til að grunnstilla vörur sem eiga að vera söluviðauki/viðbótarsala til viðskiptavina sem kaupa völdu vöruna úr vörulistanum. Á meðan á pöntunarfærslu í símaveri stendur, mun sérstakur söluviðauki/viðbótarsöluvörur birtast á skjánum í staðinn fyrir venjulegar söluviðauki/viðbótarsöluvörur sem kunna að hafa verið grunnstillt fyrir þá vöru í venjulegri vörugrunnstillingu.

Söluviðauki/viðbótarsöluvörur geta einnig nýtt sér forskriftareiginleikana til að sýna tiltekin skilaboð sem notandi mun sjá þegar söluviðauki/viðbótarsöluvara birtist við pöntunarfærsluna. Forskriftir sem er bundnar við söluviðauki/viðbótarsöluvörur, sem eru grunnstilltar sérstaklega fyrir vöru í vörulista, munu aðeins birtar þegar frumkóði þess vörulista er notaður í pöntunarfærslu í símaveri.

## <a name="catalog-page-analysis"></a>Greining vörulistasíðu

Á flipanum **Vörulistar**, eru valmöguleikar í boði til að stilla **Vörulistasíður**. Þessi eiginleiki gerir þér kleift að skilgreina tilteknar síður og síðugerðir fyrir prentaða vörulistann og kostnaðinn sem þeim tengist.

Þegar vörur í vörulista eru grunnstilltar, skal nota **Útlit vörusíðu** aðgerðina til að skilgreina tilteknu síðurnar, prósentuhlutfall af síðunni, og upplýsingar um stöðu síðunnar fyrir vöruna. Grunnstilling þessara gagna gerir notendum kleift að nýta sér **Greiningarskýrslu vörulistasvæðis**. Hægt er að finna þessa skýrslu með því að fara í skýrsluna **Retail og Commerce** \> **Skýrslur símavers** \> **Greining vörulistasvæðis**. Þessi skýrsla greinir sölur samanborið við vörulistann (sölupantanir þar sem frumkenni fyrir vörulistann var bundinn við pöntunarhaus eða línu) og við tengd prósent þeirra af síðunni og kostnað, til að gefa hefðbundna bein markaðssetning skýrslu með **fertommugreiningu**.

## <a name="catalog-requests"></a>Vörulistabeiðnir

Þar sem vörulistar eru grunnstilltir og birtir í Commerce, er hægt að nota eiginleikann **Senda vörulista**. Þessi eiginleiki er tiltækur á síðunum **Viðskiptavinur leit** og **Viðskiptavinur þjónusta**. Eftir að þú hefur valið viðskiptavinarskrá í gegnum **Viðskiptavinur leit** eða þegar þú skoðar völdu viðskiptavinareikning frá **Viðskiptavinur þjónusta**, geta notendur valið **Senda vörulista** valkostinn sem opnar svarglugga sem gerir notandanum kleift að velja úr lista yfir allar birtar og virkar vörulistar. Notandi getur valið vörulista og magn, og tiltekið frumkóðakenni til að senda. Þegar þeir smella á **Senda** hnappinn er beiðni geymd, sem síðan er hægt að stjórna með því að prenta **Vörulistabeiðnir** skýrsluna. Hægt er að finna þessa skýrslu með því að fara í **Retail og Commerce** \> **Skýrslur símavers** \> **Skýrsla vörulistabeiðna**. Það skráir allar vörulistabeiðnir, þar með talið nafn viðskiptavinar og heimilisfang viðskiptavinar sem óskaði eftir vörulistanum. Hægt er að nota skýrsluna innbyrðis eða gögnin geta verið send til þriðja aðila sem styður ytri ferli sem fela í sér að senda vörulistann efnislega til viðskiptavinarins.

## <a name="additional-features"></a>Viðbótareiginleikar

Á **Vörulistar** flipanum eru valkostir til að grunnstilla **Greiðsluáætlun** og **Ókeypis vörur** einnig tiltækir. Ef frumkóðakenni sem tengist vörulistanum er beitt meðan á pöntunarfærslu í símveri stendur, mun viðskiptavinurinn vera gjaldgengur fyrir ókeypis vörurnar eða notkun á tiltekinna greiðsluáætlanir fyrir vörulista, eins og þær er skilgreindur. Ef nauðsynlegt er að takmarka notandann til að geta aðeins valið úr greiðsluáætlanir sem tengjast vörulistanum þeirra og ekki öllum virkum greiðsluáætlanir í kerfinu, er hægt að velja gátreitinn **Leyfa aðeins vörulistaáætlanir** fyrir eitt eða fleiri af frumkóðakenni sem eru skilgreind til að framfylgja þeim takmörkunum.

## <a name="additional-notes"></a>Viðbótarathugasemdir

Eins og er, þegar frumkóðakenni er beitt á sölupöntun í símaveri, er það notað til að keyra verð, kynningartilboð, forskriftir og söluviðauki/viðbótarsala sem eru sértæk fyrir vörulista. Kerfið mun ekki banna eða koma í veg fyrir að vara sem er ekki í vörulistanum sé pantað í sölupöntuninni. Ef hlutur er pantaður, sem er ekki hluti af vörulistanum, notar kerfið fyrst **Verðflokkur** sem er skilgreindur á símaversrásinni (**Retail og Commerce** \> **Rásir** \> **Símaver** \> **Öll símaver**) fyrir vöruverð eða kynningartilboð. Ef ekkert tiltekið rásarverð finnst verður grunnsöluverð vörunnar notað.
