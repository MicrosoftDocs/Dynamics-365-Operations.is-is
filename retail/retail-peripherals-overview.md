---
title: "Yfirlit yfir jaðartæki smásölu"
description: "Í þessu efnisatriði er útskýrt hugtök sem tengjast retail jaðartæki. Það lýsir máta jaðartæki má við sölustað (POS) og íhlutirnir eru sem ber ábygð á stjórnun tengingu með Sölustað."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 268444
ms.assetid: 2ea93e43-8019-49a0-a7f8-325565ebc52d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 79a43c35691f16d773b88faad63c4ab79cb93f1f
ms.openlocfilehash: c6fb3922ba2c4b15f1043d0bcbac40ff2da9a469
ms.lasthandoff: 03/31/2017


---

# <a name="retail-peripherals-overview"></a>Yfirlit yfir jaðartæki smásölu

Í þessu efnisatriði er útskýrt hugtök sem tengjast retail jaðartæki. Það lýsir máta jaðartæki má við sölustað (POS) og íhlutirnir eru sem ber ábygð á stjórnun tengingu með Sölustað.

<a name="concepts"></a>Hugtök
--------

### <a name="pos-registers"></a>Afgreiðslukassar

Skoðun: Smellið á **Smásölu og commerce**&gt;**Rásar uppsetningu**&gt;**uppsetning Smásölustaðar**&gt;**Skráir**. Punktur afgreiðslukassa á sölustað er aðila sem er notuð til að skilgreina eiginleika sértækt tilvik á Sölustaðnum. Þessara einkenna með vélbúnaðarreglu eða uppsetningu retail jaðartæki sem verður notaður á afgreiðslukassanum verslunina sem afgreiðslukassinn er varpað á og visual reynslu fyrir notandann sem að afgreiðslukassans.

### <a name="devices"></a>Tæki

Yfirlits: Smellið á **Smásölu og commerce**&gt;**Rásar uppsetningu**&gt;**uppsetning Smásölustaðar**&gt;**Tæki**. Tæki er eining sem stendur fyrir efnislegt tilvik tækis sem er varpað í afgreiðslukassa. Þegar tæki er stofnuð, það er varpað á POS afgreiðslukassa. Tækjaeiningin rekur upplýsingar um þegar afgreiðslukassi er virkjaður, gerð biðlara sem verið er að nota og forritapakka sem hefur verið virkjað á tiltekna tæki. Tæki er hægt að varpa í eftirfarandi forrit: Retail Modern POS, Retail Modern POS-Windows Phone, Retail Modern POS-Android Skýinu Retail POS og Retail Modern POS-iOS.

### <a name="retail-modern-pos"></a>Retail Modern POS

Modern POS er POS forritið fyrir Microsoft Windows. Hægt er að virkja hann á stýrikerfi Windows 10 (OSs).

### <a name="cloud-pos"></a>Cloud POS

Skýi POS er útgáfu vafra byggt á Modern POS forritið er hægt að opna í vafra.

### <a name="modern-pos-for-ios"></a>Modern POS fyrir iOS

Modern POS fyrir iOS er er byggð á iOS útgáfa Modern POS forritið sem hægt er að virkja á iOS tæki.

### <a name="modern-pos-for-android"></a>Modern POS fyrir Android

Modern POS fyrir Android er er byggt á Android útgáfu Modern POS forritsins sem hægt er að virkja á tæki Android.

### <a name="pos-peripherals"></a>POS jaðartæki

POS jaðartæki eru tæki sem sérstaklega eru studd fyrir aðgerðir Sölustaðar. Þessar jaðartæki er yfirleitt skipt niður í tiltekinn klasa. Nánari upplýsingar um þessir klasar sjá hlutann "Tækið klasa" þessa efnisatriðis.

### <a name="hardware-station"></a>Vélbúnaðarstöð

Skoðun: Smellið á **Smásölu og commerce**&gt;**Rásir**&gt;**Smásöluverslanir**&gt;**Allar smásöluverslanir**. Veljið verslun og smellið svo á flipann **vélbúnaðarstöðvar**. Í **vélbúnaðarstöð** stillingin er rásar stig stilling sem er notuð til að skilgreina tilvik þar sem retail jaðarbúnaði viðskiptagrunninn verður virkjuð. Þessi stilling á stigi rásar er notuð til að ákvarða eiginleika retail hardware station. Það er einnig notuð við lista vélbúnaðarstöðvar sem eru í boði fyrir tilvik Modern POS í tilteknu verslun. Retail hardware station eru gerðar í forritið Modern POS fyrir Windows. Retail hardware station getur einnig virkjað óháð sem standa einir forriti Microsoft Internet Information Services (IIS). Í þessu tilfelli er því hægt að nálgast gegnum net.

### <a name="hardware-profile"></a>Vélbúnaðarregla

Yfirlits: Smellið á **Smásölu og commerce**&gt;**Rásar uppsetningu**&gt;**uppsetning Smásölustaðar**&gt;**POS forstillingar**&gt;**vélbúnaðarreglur**. Vélbúnaðarregluna er listi yfir tæki sem eru skilgreindar fyrir afgreiðslukassa Sölustaðar eða vélbúnaðarstöð. Hægt er að varpa vélbúnaðarregluna beint í afgreiðslukassa Sölustaðar eða vélbúnaðarstöð.

## <a name="devices-classes"></a>Tæki klasa
POS jaðartæki er yfirleitt skipt niður í klasa. Þessi hluti lýsir og gefur yfirlit yfir tæki sem Modern POS styður.

### <a name="printer"></a>Prentari

Prentarar hafa venjulegt kvittanaprentara POS og full-page prentara. Prentara eru studd með Hlut Tengja og Embedding fyrir Retail POS (OPOS) og Microsoft Windows viðmót bílstjóra. Allt að tvo prentara má nota á sama tíma. Þessi eiginleiki styður aðstæður þar sem innhreyfingar cash-and-carry viðskiptavina eru prentaðar á kvittanaprentara, en pantanir viðskiptavinar, sem bera nánari upplýsingar, eru prentaðar á full-page prentara. Kvittanaprentara hægt er að tengdir beint við tölvu gegnum USB, tengdar neti með Ethernet eða tengdir með Bluetooth.

### <a name="scanner"></a>Skanni

Allt að tvo strikamerki skannar samþykkja má nota á sama tíma. Þessi eiginleiki styður aðstæður þar sem skanna sem er meira farsími nauðsynlegt er til að skanna stór eða þungar vörur en fastan ívafin skanna notað fyrir flest staðlaða skyrtur í stærðinni vörur, til að flýta útskráningu tíma. Skannar samþykkja getur studdur gegnum OPOS, Alþjóðlegur Windows Svæðis (UWP) eða lyklaborð kortalesara viðmót. Hægt er að nota USB eða Bluetooth tengst skanna tölvu.

### <a name="msr"></a>Kortalesari

Hægt er að setja upp eina USB kortalesari (Kortalesara) með því að nota OPOS lyftara. Ef óskað er að nota standa einir Kortalesara kortamillifærslur millifærslu (EFT) greiðslufærslur verður Kortalesara stjórnað af tengilínu greiðslunnar. Hægt er að nota standa einir MSRs fyrir færslu viðskiptavinar vildarkorts starfsmanns í og gjafakorts kort færslu, óháð tengilínu greiðslunnar.

### <a name="cash-drawer"></a>Peningaskúffa

Tvær peningaskúffur getur stutt á vélbúnaðarreglu. Þessi eiginleiki gerir tvær vaktir virkt á hvern afgreiðslukassa til að vera tiltæk í einu. Ef samnýttrar vaktar eða peningaskúffu sem er notað af mörgum POS fartæki á sama tíma er aðeins ein peningaskúffu er leyft á hverja vélbúnaðarreglu. Peningaskúffur hægt að tengdir beint við tölvu gegnum USB, tengdar neti eða tengdir kvittanaprentarann gegnum RJ12 viðmót. Í sumum tilvikum, peningaskúffur getur einnig að vera tengdur gegnum Bluetooth.

### <a name="line-display"></a>Línuskjár

Birtir eru notaðar til að sýna afurðir stöðu færslu og aðrar upplýsingar sem er gagnlegt til viðskiptavinar við færslu. Sýna eina línu má við tölvu gegnum USB með því að nota OPOS lyftara.

### <a name="signature-capture"></a>Sækja undirskrift

Undirskrift sækja tæki eru tengd beint tölvunni gegnum USB með því að nota OPOS lyftara. Þegar sækja undirskrift er skilgreind viðskiptavinar er beðinn um að undirrita á tækinu. Eftir að undirskrift er veitt, er hann sýndur gjaldkera til að samþykkja.

### <a name="scale"></a>Vigt

Kvarða má við tölvu gegnum USP með því að nota OPOS lyftara. Þegar afurð sem er merkt sem "Weighed" afurð hefur verið bætt við færslu á Sölustað les þyngd frá vigtinni bætir vörunni við færsluna og notar magnið sem kvarðann látið í té.

### <a name="pin-pad"></a>PIN-takkaborð

Persónuleg kenni bremsuklossa (pin-NÚMER) sem eru studdar með OPOS, en þær verða að stjórnað gegnum tengilínu greiðslunnar.

### <a name="secondary-display"></a>Birta aukaáherslu

Þegar önnur birta er skilgreind, Windows birtingu númer 2 er notuð til að sýna grunnupplýsingar. Tilgangur aukaáherslu birta er að styðja nafnauka óháðum (óhs), þar sem ekki í reitinn aukaáherslu birta tekjureglur skilgreinanleg og sýnir takmarkað efni.

### <a name="payment-device"></a>Greiðslutæki

Greiðsla tækið stuðning er innleidd gegnum tengilínu greiðslunnar. Tæki greiðslu hægt er að framkvæma margar aðgerðir sem veita öðrum klasa tækið eða. Til dæmis, hægt greiðslutæki aðgerð sem Kortalesara/kortalesari, línuskjá, sækja undirskrift eða pin-takkaborðinu. Styðja til tæki greiðslu er innleidd óháð stuðning standa einir tæki sem lögð er til fyrir önnur tæki sem eru innifaldar í vélbúnaðarreglu.

## <a name="supported-interfaces"></a>Studd viðmótum
### <a name="opos"></a>OPOS

Til að aðstoða við að tryggja samræmda hægt er að nota stærsta svið tæki með Microsoft Dynamics 365 aðgerða - Smásölu, OLE fyrir POS staðalnúmer er aðal retail jaðartæki pallur sem studd er í Microsoft Dynamics 365 aðgerða - Smásölu. OLE fyrir POS staðlaða var framleidd með í Innanlandsgreiðslur Retail Sambandsríkisins (NRF), sem kemur víddarsamsetningar atvinnugrein staðlaða samskiptum protocols fyrir retail jaðartæki. OPOS er mjög sérstök innleiðingu OLE fyrir staðlaða Sölustaðar. Hann var þróaður í 1990s miður og hefur verið uppfærður nokkrum sinnum frá síðan. OPOS veitir við uppbyggingu tækið bílstjóra sem gerir auðveld samþættingu POS-vélbúnaðarregla við Windows-byggð POS kerfi. OPOS stýrir annast samskiptum milli samhæfar hug- og vélbúnaður Sölustaðar. OPOS control samanstendur af tveimur hlutum:

-   **Control hlut** – control hlut fyrir klasa tæki (t.d. birtir) veitir viðmótið fyrir forritið hugbúnaðinn. Monroe Aðstoðar Þjónustu ([www.monroecs.com](http://www.monroecs.com/)) veitir staðlaður listi eða samsafn af OPOS control hlutir sem eru þekkt sem common control hlutir (CCOs). CCOs sem eru notaðar til að prófa hlutarins af Microsoft Dynamics 365 aðgerða - Retail POS. Þess vegna er prófun hjálpar til við að tryggja samræmda sem, ef Microsoft Dynamics 365 aðgerða - styður Retail tækið klasa gegnum OPOS, margar gerðir smásölutækja getur studdur veitt framleiðanda veitir þjónustuhlut sem er byggð á fyrir OPOS. Ekki þarf að prófa sérstaklega hverja gerð tækis.
-   **Þjónustuhlutur** – þjónustuhlutinn veitir samskipti á milli control hlut (CCO) og tækið. Yfirleitt þjónustuhlut fyrir tæki ákvarðast af framleiðanda tækis. Hins vegar í sumum tilfellum gæti þurft að sækja þjónustuhlutinn frá framleiðanda fyrir vefsvæðið. Til dæmis síðasta fleiri þjónustuhlutur gætu verið tiltækar. Aðsetur framleiðanda á vefsvæði er að finna fylgigögn vélbúnaðarreglu.

[![Stjórna hlutnum og þjónustuhlut](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png) Styðja OPOS innleiðingu OLE fyrir POS hjálpar til við að tryggja samræmda sem, ef tækið framleiðendur og útgefendur POS innleiða staðlaða rétt, POS kerfi og tæki sem studd er hægt að vinna saman, jafnvel þótt þeir voru ekki áður prófað saman. **Athugasemd:** OPOS styður ekki að tryggja samræmda stuðning fyrir öll tæki með OPOS lyftara. Microsoft Dynamics 365 aðgerða - Smásölu verður fyrst styðja sem tækisgerðina eða klasa, gegnum OPOS. Þar að auki þjónustuhluti hugsanlega ekki alltaf að vera uppfærðir með nýjustu útgáfu í CCOs. Það ætti einnig að hafa í huga að, almenna gæði þjónustuhluti breytileg.

### <a name="windows"></a>Windows

Prentun á kvittun á Sölustað er bestuð til OPOS. OPOS tends að mikið hraðar en prentun gegnum Windows. Því er gott að nota OPOS, sérstaklega í smásölu þar sem innhreyfingar 40 dálki eru prentaðar og tíma sem færslan verður að vera fastar. Fyrir flest tæki nota OPOS stýrir. Hins vegar, sum kvittanaprentara OPOS einnig styðja flutningsskrá Windows. Með því að nota Windows-rekill hægt er að nálgast síðasta letur og netlén einn prentari fyrir marga afgreiðslukassa. Hins vegar eru drawbacks með því að nota Windows lyftara. Hér eru nokkur dæmi um þessar drawbacks:

-   Þegar Windows flutningsskrá eru notaðar, eru myndir veitta áður en prentun fer fram. Þess vegna tends prentun að það en það er á prentara sem nota OPOS-eftirlit.
-   Tæki sem eru tengdir gegnum prentara ("daisy-chained") hugsanlega ekki rétt þegar Windows flutningsskrá eru notaðir. Til dæmis peningaskúffu hugsanlega ekki að opna eða prentara fylgiseðils hugsanlega ekki orð sem búist er við.
-   OPOS styður einnig yfirgripsmeiri safn breytur sem tengjast kvittanaprentara smásölu, eins og prentun fylgiseðla eða klipping pappír.

Stýrir OPOS eru tiltækir fyrir Windows-prentara sem verið er að nota prentara á enn vinna rétt með Microsoft Dynamics 365 aðgerða - Retail.

### <a name="universal-windows-platform"></a>Alþjóðlegur Windows Svæðis

UWP, ef jaðartæki smásölu, tengist til að styðja Windows fyrir Plug Play og tæki. Þegar Plug Play og tækið er tengd við útgáfu Windows OS sem styður sem gerð tækis, engin bílstjóra er áskilið fyrir tækið sem nota á sem ætlað. Til dæmis, ef Windows greinir Bluetooth speaker tæki, við OS veit að tækið hafi á **Speaker** klasinn gerð. Þess vegna, og fer það með sem tækið sem á speaker. Engin viðbótaruppsetning er krafist. POS-tæki ef margar USB tæki getur plugged og Windows verður að þekkja þá sem Mannauður Viðmót Tæki (HIDs). Hins vegar það hugsanlega ekki hægt að ákvarða getu sem tækið veitir, þar sem tækið ekki klasa eða gerð tækis. Í Windows 10 tækið klasar strikamerkjaskanna og MSRs hefur verið bætt við. Þess vegna ef tæki sýnir sjálf á Windows 10 sem tækið einnar af þessum klasa, Windows verður listen fyrir tilvik úr tækinu á viðeigandi tímum. Modern POS styður UWP MSRs og skannar samþykkja. Því þegar hún er tilbúin fyrir inntak úr einni af þessum tæki og tæki sem tilheyrir eitt af þessum klasa er tengdur, er hægt að nota. Til dæmis, ef UWP strikamerkjaskanni er plugged í Windows 10 tölvu og strikamerki í er skilgreind fyrir Nútímasölustaði strikamerkjaskanni verður virk á formerki á skjánum. Engin viðbótaruppsetning er krafist. Viðbótar klasar tímapunkti tæki UWP þjónustu er bætt við Windows. Þessir klasar hafa klasar fyrir peningaskúffur og kvittanaprentara. Stuðningur fyrir þessa nýjan klasa tækis í Modern POS er í bið.

### <a name="keyboard-wedge"></a>Lyklaborð kortalesara

Lyklaborð kortalesara tæki senda gögn tölvunni og ef gögnin voru slá á lyklaborði. Þess vegna að sjálfgefnu svæði sem er virk á Sölustaðnum fær gögn sem er skönnuð eða sem var lesið. Í sumum tilvikum, þessi virkni getur valdið rangri gerð gögn til að skanna í svæðið röng. Til dæmis gæti verið að skanna strikamerki í svæði sem er ætluð fyrir innfærslu gagna kreditkorts. Í mörgum tilvikum er viðskiptagrunninn á Sölustað sem ákvarðar hvort gögn sem er skönnuð eða sem var lesið er strikamerki eða greiðslukortalestur. Þess vegna gögnin er meðhöndluð rétt. Hins vegar þegar tæki eru sett upp sem OPOS en lyklaborð kortalesara tæki, er fleiri stjórn á því hvernig gögn úr þessum tæki geta verið notaðar, þar sem fleiri "kallast" um tæki vegna gögn úr. Til dæmis gögn úr strikamerkjaskanni viðurkenndur sjálfkrafa sem strikamerki og tengda færslu í gagnagrunninum finnst betur og hraðar en ef leit almennan streng voru notuð, og mál yfir lyklaborð kortalesara tæki.

### <a name="native-printer"></a>Upprunalegum prentara

Upprunalegum (eða "Tækis" sem gerð nefnist vélbúnaðarreglunni) hægt er að skilgreina prentara til að biðja notandann til að velja prentara sem er skilgreindur fyrir tölvuna. Þegar prentara á í **Tækið** gerð er skilgreind, ef Modern POS finnast prenta skipun, notandi er beðinn um að velja prentara í listanum. Þessi hegðun frábrugðið hegðun fyrir Windows flutningsskrá, þar sem **Windows** tegund prentarinn vélbúnaðarregluna ekki sýna lista yfir prentara. Þess í stað þess að leggja með heiti prentara í á **tækjaheiti** svæði.

### <a name="windows"></a>Windows

Í **Windows** tækið er notuð fyrir aðeins prentara. Þegar Windows-prentara er skilgreind í vélbúnaðarreglu, heiti prentara fyrir tiltekna gefa verður upp. Þegar Modern POS finnast prenta tilvik, ef Windows-prentari sé skilgreint tilvikið skila tilgreinda Windows-prentarans. Notandi ekki beðinn um að velja prentara.

### <a name="network"></a>Net

Hægt er að nota net addressable peningaskúffur kvittanaprentara og afgreiðslustöðvar á neti, annaðhvort beint í gegnum retail hardware station Interprocess Samskiptum (ÓFK) sem er byggð á inn í forritið Modern POS fyrir Windows eða í gegnum retail hardware station IIS fyrir aðrir biðlarar Modern POS.

## <a name="hardware-station-deployment-options"></a>Virkjunarvalkostir hardware station
### <a name="ipc-built-in"></a>ÓFK (innbyggðu)

Vélbúnaðarstöð Interprocess Samskiptum (ÓFK) er byggð á inn í forritið Modern POS fyrir Windows. Tengið vélbúnaðarreglu til að skrá sem á að nota forritið Modern POS fyrir Windows til að nota retail hardware station ÓFK. Stofna vélbúnaðarstöð á síðan á **Dedicated** gerð fyrir verslunina sem afgreiðslukassinn verður notað. Þegar Modern POS er ræst ÓFK vélbúnaðarstöðin verður virkur og POS jaðartæki sem hafa verið skilgreindar er tilbúið til notkunar. Ef þess er tímabundið ekki krafist staðbundna vélbúnaður af einhverri ástæðu, er notuð í **Stjórna vélbúnaðarstöðvar** aðgerð til að slökkva á hardware station getu. Modern POS einnig er hægt að nota retail hardware station ÓFK geti haft samskipti beint jaðartæki net.

### <a name="iis"></a>IIS

Hægt er að nota IIS eða standa einir útgáfu vélbúnaðarstöð á tvo vegu. Lýsiorð "IIS" gefur sem forritið POS tengist retail hardware station með Microsoft Internet Information Services. Forritið POS tengist IIS retail hardware station með vefþjónustu sem keyra á tölvu þar sem tæki er tengt. Þegar IIS er notuð, er hægt að nota retail jaðartæki sem tengjast vélbúnaðarstöð eftir afgreiðslukassa sem er á netinu sama sem retail hardware station IIS. Þar sem aðeins Modern POS fyrir Windows inniheldur innbyggðu stuðning fyrir jaðartæki smásölu, öll forrit öðrum Modern POS verður að nota retail hardware station IIS til samskipta við POS jaðartæki sem eru skilgreindar í vélbúnaðarreglu. Þess vegna sem hvert tilvik retail hardware station IIS krefst tölvu sem keyrir vefþjónusta og forritið samskipti við tæki. Vélbúnaðarstöð IIS er áskilið fyrir allar umsóknir ekki - Windows Modern POS.

#### <a name="dedicated"></a>Sérnýtt

Modern POS notar vélbúnaðarstöðvar yfir í **Dedicated** gerð til að ákvarða jaðartæki tengjast beint á tölvunni þar sem forritið er notað. Hins vegar á **Dedicated** einnig er hægt að nota gerð fyrir vélbúnaðarstöðvar IIS. Við venjulegt, föst POS aðstæður sem notar POS Skýinu sem POS forritið er **Dedicated** hardware station gerð er notuð fyrir IIS vélbúnaðarstöðvar sem virkjuð eru á sömu tölvu sem keyrir POS Skýinu. Frá sjónarhorni jaðartæki smásölu, sérstakan vélbúnaðarstöð IIS hefur betur smásölu jaðarbúnaði stuðning fyrir venjulegt, föst POS aðstæður. Sérnýtta vélbúnaðarstöðvar styðja allar jaðartæki sem eru studdar í vélbúnaðarreglu.

#### <a name="shared"></a>Samnýtt

Samnýtt vélbúnaður stations eru ætlaðar sem nota á mörg POS-tæki með á daginn. Samnýtt vélbúnað stations eru bestuð til að styðja aðeins peningaskúffur, kvittanaprentara, og afgreiðslustöðvar. Beint er hægt að tengja standa einir strikamerkjaskanna, MSRs, birtir, kvarða eða önnur tæki. Annars verður árekstrar verða þegar margar POS til að koma aftur kröfu jaðartæki þær á sama tíma. Hér er hvernig árekstrar eru meðhöndlaðar fyrir tæki studd:

-   **Peningaskúffa** – peningaskúffunni er opnaður með tilvik sem eru sendar á tækinu. Aðeins vandamál sem geta átt sér stað þegar kallað er á peningaskúffu gerist ef peningaskúffu er þegar opin. Ef samnýtta vélbúnaðarstöðvar ætti að stilla peningaskúffu sem **Samnýttum** í vélbúnaðarreglu. Þessi stilling kemur fyrir Sölustað athugun á hvort peningaskúffu er þegar opinn þegar sendir hann opnar skipanir.
-   **Kvittanaprentarann** – Ef tvær innhreyfingu prentun skipanir eru send til retail hardware station samtímis eina skipanir hægt er að glata eftir tækið. Sumar tæki með innri minni eða keyrslutíma sem getur komið í veg fyrir þetta vandamál. Ef prenta skipun er ekki stofnaður, gjaldkeri tekur villuboð og getur prenta skipun frá reyna aftur.
-   **Afgreiðslustöð** – Ef inn gjaldkeri reynir að greiðslumáta í færslu á afgreiðslustöð sem er þegar í notkun, skilaboð sé álíta gjaldkeri afgreiðslustöð er í notkun og biður gjaldkera að reyna aftur síðar. Yfirleitt, gjaldkerar sjá við afgreiðslustöð er þegar í notkun og mun bíða þar til hún er önnur færsla er lokið áður en þeir reyna að greiðslumáta aftur.

Villuleit er áætlað fyrir framtíðarútgáfu sem kannar hvort óstudd tæki eru settir upp fyrir vélbúnaðarregluna sem er varpað á samnýtt vélbúnaðarstöð. Ef einhverjar óstudd tæki finnast fær notandi skilaboð sem tilgreinir sem ekki eru kostnaðarjafnaðar tæki stutt fyrir samnýttar vélbúnaðarstöðvar. Ef samnýtta vélbúnaðarstöðvar á **Velja við greiðslumáta** valkostur er stilltur á **Já** stigi afgreiðslukassa. POS notanda er síðan beðinn um að velja vélbúnaðarstöð við greiðslumáta er valið fyrir færslu á Sölustaðnum. Þegar retail hardware station valinn aðeins við greiðslumáta valið hardware station bætt beint við POS verkflæði fyrir fartæki aðstæður. Sem viðbótar fríðinda, línuskjá greiðslunnar afgreiðslustöðvar er ekki notað fyrir samnýttar aðstæður. Ef greiðslan afgreiðslustöðvar er notað sem við línuskjá, gæti aðrir notendur lokaðar frá með því að nota sem afgreiðslustöð þar til færslan er lokið. Í fartæki aðstæður línur gæti verið bætt við færslu með yfir lengra tímabil. Þess vegna er **Velja við greiðslumáta** valkost er krafist til að tryggja framboð hagkvæmasta tækis.

### <a name="network-peripherals"></a>Jaðartæki net

Merki net fyrir tæki vélbúnaðarreglunni gerir peningaskúffur kvittanaprentara og afgreiðslustöðvar að vera tengdir gegnum tengingu.

#### <a name="modern-pos-for-windows"></a>Modern POS fyrir Windows

Hægt er að tilgreina ip-tölur fyrir jaðartæki net í tveimur tugasætum. Ef Modern POS Windows-biðlari notar eina samstæðu af netinu jaðartæki er ætti að setja ip-tölur fyrir þær tæki með því að nota í **ip-TÖLU skilgreiningu** valkost í Aðgerðarúðunni til að skrá sig.. Ef netið tæki sem verða að vera samnýtt milli afgreiðslukassa Sölustaðar, hægt að varpa vélbúnaðarreglu sem hefur net tæki úthlutað beint í samnýtta vélbúnaðarstöð. Til að úthluta ip-tölur, veljið þá vélbúnaðarstöð í í **Smásöluverslanir** síðunni og nota svo sem **ip-TÖLU skilgreiningu** í í **vélbúnaðarstöðvar** hluta til að tilgreina net tæki sem eru úthlutaðar því vélbúnaðarstöð. Fyrir vélbúnaðarstöðvar sem hafa aðeins net tæki, þarf ekki að virkja vélbúnaðarstöð sjálfa. Í þessu tilfelli retail hardware station áskilið er aðeins til að flokka conceptually net addressable tæki eftir staðsetningu þeirra í smásöluverslunar.

#### <a name="cloud-pos-modern-pos-for-ios-and-modern-pos-for-android"></a>Skýið POS Modern POS fyrir iOS og Modern POS fyrir Android

Viðskiptagrunninn sem keyrir efnislega tengda og netlén addressable jaðartæki eru geymdar í retail hardware station. Þess vegna fyrir öllum biðlurum POS nema Modern POS fyrir Windows vélbúnaðarstöð við IIS verður að vera virkjuð og virka til að virkja Sölustað til samskipta við jaðartæki, óháð því hvort þau jaðartæki eru efnislega tengdir vélbúnaðarstöð eða sendur hann á neti.

## <a name="setup-and-configuration"></a>Uppsetning og skilgreining
### <a name="hardware-station-installation"></a>Hardware station uppsetning

Sjá upplýsingar [Retail hardware station skilgreiningu og uppsetningu](retail-hardware-station-configuration-installation.md).

### <a name="modern-pos-for-windows-setup-and-configuration"></a>Modern POS fyrir Windows uppsetningu og skilgreiningu

Sjá upplýsingar [uppsetningu og skilgreiningu Retail Modern POS](retail-modern-pos-device-activation.md).

### <a name="opos-device-setup-and-configuration"></a>OPOS tækið uppsetningu og skilgreiningu

Nánari upplýsingar um íhluti OPOS í "Studd viðmót" hluta þessa skjals. Venjulega er OPOS flutningsskrá eru veittir af framleiðanda tækis. Þegar bílstjóri OPOS tækið er uppsett skal það bætir lykill Windows stýriskrárinnar í einu af eftirfarandi stöðum:

-   **kerfið 32-bita:** HKEY\_STAÐBUNDNA\_MACHINESOFTWAREOLEforRetailServiceOPOS
-   **kerfið 64-bita:** HKEY\_STAÐBUNDNA\_MACHINESOFTWAREWOW6432NodeOLEforRetailServiceOPOS

Innan staðsetningu ServiceOPOS stýriskrárinnar skilgreindu tæki er raðað eftir OPOS tækið klasa. Margar tækið flutningsskrá eru vistaðar.

## <a name="supported-scenarios-by-hardware-station-type"></a>Studdar áætlanir af gerðinni hardware station
### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a>Biðlari stuðning – ÓFK vélbúnaðarstöð miðað við IIS vélbúnaðarstöð

Eftirfarandi tafla sýnir grannfræði og virkjun aðstæður sem eru studdar.

| Biðlari      | ÓFK vélbúnaðarstöð | Vélbúnaðarstöð IIS |
|-------------|----------------------|----------------------|
| Windows-forriti | Já                  | Já                  |
| Cloud POS   | Ekkert                   | Já                  |
| Android     | Ekkert                   | Já                  |
| iOS         | Ekkert                   | Já                  |

### <a name="network-peripherals"></a>Jaðartæki net

Net jaðartæki getur stutt beint í gegnum retail hardware station sem er byggð á inn í forritið Modern POS fyrir Windows. Fyrir allar aðrar biðlara, verður að virkja vélbúnaðarstöð á IIS.

| Biðlari      | ÓFK vélbúnaðarstöð | Vélbúnaðarstöð IIS |
|-------------|----------------------|----------------------|
| Windows-forriti | Já                  | Já                  |
| Cloud POS   | Ekkert                   | Já                  |
| Android     | Ekkert                   | Já                  |
| iOS         | Ekkert                   | Já                  |

## <a name="supported-device-types-by-hardware-station-type"></a>Studd tækjategundir eftir gerð hardware station
### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Modern POS fyrir Windows með vélbúnaðarstöð er ÓFK (innbyggðu)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Studd tækið klasa</th>
<th>Studd viðmótum</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Prentari</td>
<td><ul>
<li>OPOS</li>
<li>Windows-rekill</li>
<li>Tæki</li>
<li>Net</li>
</ul></td>
</tr>
<tr class="even">
<td>Prentari 2</td>
<td><ul>
<li>OPOS</li>
<li>Windows-rekill</li>
<li>Tæki</li>
<li>Net</li>
</ul></td>
</tr>
<tr class="odd">
<td>Línuskjár</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Tvískiptur skjár</td>
<td>Windows-rekill</td>
</tr>
<tr class="odd">
<td>Kortalesari</td>
<td><ul>
<li>OPOS</li>
<li>UWP (Ekki krafist slíkrar uppsetningar.)</li>
<li>Lyklaborð kortalesara (Ekki krafist slíkrar uppsetningar.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Útgefandi</td>
<td><ul>
<li>OPOS</li>
<li>Net <strong>Athugasemd:</strong> hægt er að setja upp ef Aðeins eitt skúffu <strong>Nota samnýtt vakt</strong> er skilgreindur í skúffu.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Skúffa 2</td>
<td><ul>
<li>OPOS</li>
<li>Net <strong>Athugasemd:</strong> hægt er að setja upp ef Aðeins eitt skúffu <strong>Nota samnýtt vakt</strong> er skilgreindur í skúffu.</li>
</ul></td>
</tr>
<tr class="even">
<td>Skanni</td>
<td><ul>
<li>OPOS</li>
<li>UWP (Ekki krafist slíkrar uppsetningar.)</li>
<li>Lyklaborð kortalesara (Ekki krafist slíkrar uppsetningar.)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Skanni 2</td>
<td><ul>
<li>OPOS</li>
<li>UWP (Ekki krafist slíkrar uppsetningar.)</li>
<li>Lyklaborð kortalesara (Ekki krafist slíkrar uppsetningar.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Vigt</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>PIN-takkaborð</td>
<td>OPOS (Stuðning er veitt með sérsniðinn greiðslutengillinn).</td>
</tr>
<tr class="even">
<td>Sækja undirskrift</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Greiðslustöð</td>
<td><ul>
<li>Styðja sérsniðið tækis</li>
<li>Net (Fyrir nánari upplýsingar eru í fylgigögnum greiðslu connector.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Öllum biðlurum Modern POS með sérstakan IIS vélbúnaðarstöð

**Athugasemd:** Þegar IIS vélbúnaðarstöð er "sérnýtt," er bein tengsl milli biðlara POS og retail hardware station.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Studd tækið klasa</th>
<th>Studd viðmótum</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Prentari</td>
<td><ul>
<li>OPOS</li>
<li>Windows-rekill <strong>Athugasemd:</strong> Fyrir Windows prentarar á neti notanda retail hardware station verður heimild til að prentaranum.</li>
<li>Net</li>
</ul></td>
</tr>
<tr class="even">
<td>Prentari 2</td>
<td><ul>
<li>OPOS</li>
<li>Windows-rekill</li>
<li>Net</li>
</ul></td>
</tr>
<tr class="odd">
<td>Línuskjár</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Kortalesari</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Útgefandi</td>
<td><ul>
<li>OPOS</li>
<li>Net <strong>Athugasemd:</strong> hægt er að setja upp ef Aðeins einn skúffu á vélbúnaðarreglu <strong>Nota samnýtt vakt</strong> er skilgreindur í skúffu.</li>
</ul></td>
</tr>
<tr class="even">
<td>Skúffa 2</td>
<td><ul>
<li>OPOS</li>
<li>Net</li>
</ul></td>
</tr>
<tr class="odd">
<td>Skanni</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Skanni 2</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Vigt</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>PIN-takkaborð</td>
<td>OPOS (Stuðning er veitt með sérsniðinn greiðslutengillinn).</td>
</tr>
<tr class="odd">
<td>Sig. sækja</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Greiðslustöð</td>
<td><ul>
<li>Styðja sérsniðið tækis</li>
<li>Net (Fyrir nánari upplýsingar eru í fylgigögnum greiðslu connector.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Öllum biðlurum Modern POS með samnýtta IIS vélbúnaðarstöð

**Athugasemd:** Þegar vélbúnaðarstöð IIS "samnýtt," margar tæki hægt er að nota retail hardware station á sama tíma. Á þessu dæmi ætti að nota aðeins tæki sem eru taldar upp í eftirfarandi töflu. Ef reynt er að deila tæki sem ekki eru kostnaðarjafnaðar listanum hér, svo sem strikamerkjaskanna og MSRs, villur munu eiga sér stað þegar margar til að koma aftur kröfu sama jaðarbúnaðinum. Í framtíðinni, slíkt afbrigði verður að sérstaklega komið í veg fyrir.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Studd tækið klasa</th>
<th>Studd viðmótum</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Prentari</td>
<td><ul>
<li>OPOS</li>
<li>Windows-rekill <strong>Athugasemd:</strong> Fyrir Windows prentarar á neti notanda retail hardware station verður heimild til að prentaranum.</li>
<li>Net</li>
</ul></td>
</tr>
<tr class="even">
<td>Prentari 2</td>
<td><ul>
<li>OPOS</li>
<li>Windows-rekill</li>
<li>Net</li>
</ul></td>
</tr>
<tr class="odd">
<td>Útgefandi</td>
<td><ul>
<li>OPOS</li>
<li>Net <strong>Athugasemd:</strong> hægt er að setja upp ef Aðeins einn skúffu á vélbúnaðarreglu <strong>Nota samnýtt vakt</strong> er skilgreindur í skúffu.</li>
</ul></td>
</tr>
<tr class="even">
<td>Skúffa 2</td>
<td><ul>
<li>OPOS</li>
<li>Net</li>
</ul></td>
</tr>
<tr class="odd">
<td>Greiðslustöð</td>
<td><ul>
<li>Styðja sérsniðið tækis</li>
<li>Net (Fyrir nánari upplýsingar eru í fylgigögnum greiðslu connector.)</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a>Skilgreining fyrir studd aðstæður
Nánari upplýsingar um hvernig stofna á vélbúnaðarreglur í [Skilgreina og viðhalda rás biðlara, þar á meðal afgreiðslukassa og vélbúnaðarstöðvar](define-maintain-channel-clients-registers-hw-stations.md). **Athugasemd:** Fyrir Microsoft Dynamics 365 Aðgerðir útgáfu 1611, hardware station forstilling er ekki notuð lengur. Eigindir eru áður sett upp í forstillingunni hardware station nú eru hluti af retail hardware station.

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Modern POS fyrir Windows með vélbúnaðarstöð er ÓFK (innbyggðu)

Þessi skilgreining er oftast dæmigert skilgreiningu fyrir venjulegt, föst afgreiðslukassar. Á þessu dæmi, upplýsingar um forstillingu vélbúnaðar varpað beint til að skrá sig.. Afgreiðslustöðvarnúmer kortamillifærslu ætti einnig að setja á afgreiðslukassa sjálfa. Fylgið eftirfarandi skrefum til að setja upp þessari skilgreiningu er.

1.  Stofna vélbúnaðarreglu þar sem allar nauðsynlegar jaðartæki eru skilgreind.
2.  Varpa vélbúnaðarregluna á afgreiðslukassa.
3.  Stofna vélbúnaðarstöð á í **Dedicated** gerð smásöluverslunar þar sem notað verður á afgreiðslukassa. Lýsing er valfrjáls. **Athugasemd:** þarf ekki að stilla aðra eiginleika í retail hardware station. Allar aðrar nauðsynlegar upplýsingar eins og vélbúnaðarreglu, koma úr skrá sjálfa.
4.  Smellið á **Smásölu og commerce**&gt;**Retail ÞAÐ**&gt;**dreifingaráætlun**.
5.  Velja skal **1090** dreifingaráætlun til að samstilla nýja vélbúnaðarreglu fyrir verslun. Smellið á **Keyra nú** að samstilla breytingar á Sölustað.
6.  Velja skal **1040** dreifingaráætlun til að samstilla nýja vélbúnaðarstöð við verslunina. Smellið á **Keyra nú** að samstilla breytingar á Sölustað.
7.  Setja upp og virkja Modern POS fyrir Windows.
8.  Hefja Modern POS fyrir Windows og byrja að nota tengda jaðartæki.

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Öllum biðlurum Modern POS með sérstakan IIS vélbúnaðarstöð

Þessari skilgreiningu er hægt að nota í öllum biðlurum Modern POS með vélbúnaðarstöð sem aðeins ein POS afgreiðslukassa. Fylgið eftirfarandi skrefum til að setja upp þessari skilgreiningu er.

1.  Stofna vélbúnaðarreglu þar sem allar nauðsynlegar jaðartæki eru skilgreind.
2.  Stofna vélbúnaðarstöð á í **Dedicated** gerð smásöluverslunar þar sem notað verður á afgreiðslukassa.
3.  Setja á sérstakan vélbúnaðarstöð eftirfarandi eiginleika:
    -   **Hýsilheiti** – heiti hýsils tölvu þar sem retail hardware station mun keyra. **Athugasemd:** Skýinu POS hægt að leysa **staðarhýslinum** til að ákvarða tölvunni sem keyrir POS Skýinu. Hins vegar skírteinis sem krafist er til að para POS Skýi með retail hardware station verður einnig að hafa "Staðarhýslinum" sem heiti tölvunnar. Til að forðast vandamál er ráðlagt tilkynnir tilvik hver sérstakan vélbúnaðarstöð verslunarinnar, eftir þörfum. Fyrir hverja vélbúnaðarstöð heiti hýsilsins ætti að vera heiti á tiltekinni tölvu þar sem retail hardware station verður virkjað.
    -   **Tengi** – tengið sem nota á fyrir retail hardware station að eiga samskipti við biðlara Modern POS.
    -   **Vélbúnaðarregla** – Ef vélbúnaðarregluna er ekki veitt á vélbúnaðarstöð sjálf, vélbúnaðarreglu sem er úthlutað á afgreiðslukassa verður notuð.
    -   **Verslunarnúmer Kortamillifærslu númer** -Auðkenni afgreiðslustöðvar KORTAMILLIFÆRSLU Er að nota þegar KORTAMILLIFÆRSLU heimildum eru send. Þetta Kenni er veitt með kreditkortagjörvanum.
    -   **Pakkaheiti** – hardware station pakka til að nota þegar í vélbúnaðarstöð er virkjuð.

4.  Smellið á **Smásölu og commerce**&gt;**Retail ÞAÐ**&gt;**dreifingaráætlun**.
5.  Velja skal **1090** dreifingaráætlun til að samstilla nýja vélbúnaðarreglu fyrir verslun. Smellið á **Keyra nú** að samstilla breytingar á Sölustað.
6.  Velja skal **1040** dreifingaráætlun til að samstilla nýja vélbúnaðarstöð við verslunina. Smellið á **Keyra nú** að samstilla breytingar á Sölustað.
7.  Setja upp retail hardware station. Nánari upplýsingar um hvernig á að setja upp retail hardware station í [Retail hardware station skilgreiningu og uppsetningu](retail-hardware-station-configuration-installation.md).
8.  Setja upp og virkja Modern POS. Nánari upplýsingar um hvernig á að setja upp Modern POS í [uppsetningu og skilgreiningu Retail Modern POS](retail-modern-pos-device-activation.md).
9.  Innskráning á Modern POS og veljið **Framkvæma aðgerðir utan skúffu**.
10. Byrja á **Stjórna vélbúnaðarstöðvar** aðgerð.
11. Smellið á **Stjórna**.
12. Í retail hardware station síða, stilla valkost til að kveikja á retail hardware station.
13. Velja vélbúnaðarstöð til að nota og síðan smellt á **Par**.
14. Eftir vélbúnaðarstöðin er pöruð smellið **Loka**.
15. Smella á hardware station val síðunni nýlega valda vélbúnaðarstöð til að gera hana virka.

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Öllum biðlurum Modern POS með samnýtta IIS vélbúnaðarstöð

Þessari skilgreiningu er hægt að nota í öllum biðlurum Modern POS sem deila vélbúnaðarstöðvar með önnur tæki. Fylgið eftirfarandi skrefum til að setja upp þessari skilgreiningu er.

1.  Stofna vélbúnaðarreglu þar sem áskilinn jaðartæki eru skilgreind.
2.  Stofna vélbúnaðarstöð á í **Samnýttum** gerð smásöluverslunar þar sem notað verður á afgreiðslukassa.
3.  Samnýttar vélbúnaðarstöð sett eftirfarandi eiginleika:
    -   **Hýsilheiti** – heiti hýsils tölvu þar sem retail hardware station mun keyra.
    -   **Lýsing** – Texta sem auðkenna vélbúnaðarstöð, eins og **Skilar** eða **Sé verslunar**.
    -   **Tengi** – tengið sem nota á fyrir retail hardware station að eiga samskipti við biðlara Modern POS.
    -   **Vélbúnaðarregla** -Fyrir samnýttar vélbúnaðarstöðvar vélbúnaðarstöð hver ætti að hafa vélbúnaðarreglu. Hægt er að deila vélbúnaðarreglur milli vélbúnaðarstöðvar en þær að vera varpað á hverja vélbúnaðarstöð. Þar að auki er mælt með að nota samnýtta vaktir þegar margar tæki nota sömu samnýttu vélbúnaðarstöð. Til að setja upp samnýttrar vaktar er smellt á **Smásölu og commerce**&gt;**Rásar uppsetningu**&gt;**uppsetning Smásölustaðar**&gt;**POS forstillingar**&gt;**vélbúnaðarreglur**. Velja peningaskúffu fyrir hverja samnýtta vélbúnaðarreglu og setja í **Samnýttum vakt skúffu** valkosturinn að **Já**.
    -   **Verslunarnúmer Kortamillifærslu númer** -Auðkenni afgreiðslustöðvar KORTAMILLIFÆRSLU Er að nota þegar KORTAMILLIFÆRSLU heimildum eru send. Þetta Kenni er veitt með kreditkortagjörvanum.
    -   **Pakkaheiti** – hardware station pakka til að nota þegar í vélbúnaðarstöð er virkjuð.

4.  Endurtakið skref 2 og 3 fyrir hverja viðbótar vélbúnaðarstöð sem krafist er í versluninni.
5.  Smellið á **Smásölu og commerce**&gt;**Retail ÞAÐ**&gt;**dreifingaráætlun**.
6.  Velja skal **1090** dreifingaráætlun til að samstilla nýja vélbúnaðarreglu fyrir verslun. Smellið á **Keyra nú** að samstilla breytingar á Sölustað.
7.  Velja skal **1040** dreifingaráætlun til að samstilla nýja vélbúnaðarstöð við verslunina. Smellið á **Keyra nú** að samstilla breytingar á Sölustað.
8.  Setja upp retail hardware station á hverja hýsitölva sem sett eru upp í skref 2 og 3. Nánari upplýsingar um hvernig á að setja upp retail hardware station í [Retail hardware station skilgreiningu og uppsetningu](retail-hardware-station-configuration-installation.md).
9.  Setja upp og virkja Modern POS. Nánari upplýsingar um hvernig á að setja upp Modern POS í [uppsetningu og skilgreiningu Retail Modern POS](retail-modern-pos-device-activation.md).
10. Innskráning á Modern POS og veljið **Framkvæma aðgerðir utan skúffu**.
11. Byrja á **Stjórna vélbúnaðarstöðvar** aðgerð.

12. Smellið á **Stjórna**.
13. Í retail hardware station síða, stilla valkost til að kveikja á retail hardware station.
14. Velja vélbúnaðarstöð til að nota og síðan smellt á **Par**.
15. Endurtakið skraf 14 fyrir hverja vélbúnaðarstöð sem Modern POS verður að nota.
16. Eftir að allar nauðsynlegar vélbúnaðarstöðvar eru pöruð smellið **Loka**.
17. Smella á hardware station val síðunni nýlega valda vélbúnaðarstöð til að gera hana virka. **Athugasemd:** Ef tæki nota mismunandi vélbúnaðarstöðvar oft ráðlagt skilgreina Modern POS til að senda kvaðningu á gjaldkera til að velja vélbúnaðarstöð þegar þeir byrja á talningu stendur. Smellið á **Smásölu og commerce**&gt;**Rásar uppsetningu**&gt;**uppsetning Smásölustaðar**&gt;**Skráir**. Veljið afgreiðslukassa og stillið í **Velja við greiðslumáta** valkosturinn að **Já**. Nota skal **1090** dreifingaráætlun til að samstilla breytingar á gagnagrunni rásar.

## <a name="extensibility"></a>Stækkunarhæfni
Sjá upplýsingar um aðstæður extensibility fyrir retail hardware station [Vélbúnaðarstöð extensibility](dev-itpro/hardware-station-extensibility.md).

## <a name="security"></a>Öryggi
Samkvæmt gildandi öryggi stöðlum, á að nota eftirfarandi stillingar í framleiðsluumhverfi: **Athugasemd:** uppsetningarforrits hardware station mun sjálfkrafa gera þessar breytingar stýriskrá sem hluti af uppsetningu gegnum sjálfsafgreiðslu.

-   Secure Sockets Layer (SSL) ætti að gera hann óvirkan.
-   Einungis Flutningur Lag Öryggi (TLS) útgáfu 1,2 (eða í gildandi hæsta) ætti virkjuð og notuð. **Athugasemd:** SSL og útgáfu TLS nema TLS 1,2 er óvirkur að Sjálfgefnu. Breyta eða gera þessi gildi, skal fylgja þessum skrefum:
    1.  Styðjið á merki Windows lykill + Rannsókn til að opna í **Keyra** glugga.
    2.  Í því **Opna** ritið **Regedit**, og smellið síðan á **í lagi**.
    3.  Ef að **Lykil Notandastýringin** skilaboðagluggi birtist er smellt á **Já**.
    4.  Í í **Stýriskrána Ritill** glugganum fara **HKEY\_STAÐBUNDNA\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**. Eftirfarandi lyklar hafa verið sjálfkrafa færðar inn til að leyfa aðeins fyrir TLS 1,2:
        -   TLS 1.2Server: Virkjaðar = 1
        -   TLS 1.2Server:DisabledByDefault = 0
        -   TLS 1.2Client: Virkjaðar = 1
        -   TLS 1.2Client:DisabledByDefault = 0
        -   TLS 1.1Server: Virkjaðar = 0
        -   TLS 1.1Client: Virkjaðar = 0
        -   TLS 1.0Server: Virkjaðar = 0
        -   TLS 1.0Client: Virkjaðar = 0
        -   SSL 3.0Server: Virkjaðar = 0
        -   SSL 3.0Client: Virkjaðar = 0
        -   SSL 2.0Server: Virkjaðar = 0
        -   SSL 2.0Client: Virkjaðar = 0
-   Enginn viðbótar net tengi ætti að vera opin, nema þær séu nauðsynlegar ástæðum þekkt er tilgreindur.
-   Tilfanga á Milli uppruna samnýtingu verður gerð óvirk og verður að tilgreina leyfð uppruna sem eru samþykktar.
-   Aðeins traust skírteini yfirvalda ætti að nota til að fá vottorð sem verður notaður í tölvum sem keyra retail hardware station.

**Athugasemd:** er mjög mikilvægt að farið sé yfir öryggi leiðbeiningar fyrir IIS og þarfir Greiðslu Korts Atvinnugrein (PCI).

## <a name="peripheral-simulator"></a>Jaðarbúnaður
Sjá upplýsingar [Retail jaðarbúnaði hermi](retail-peripheral-simulator.md).

## <a name="microsofttested-peripheral-devices"></a>Jaðartæki Microsofttested
### <a name="ipc-built-in-hardware-station"></a>Vélbúnaðarstöð ÓFK (innbyggðu)

Eftirfarandi jaðartæki voru prófaðar með því að nota retail hardware station ÓFK sem byggð er á í Modern POS fyrir Windows.

#### <a name="printer"></a>Prentari

| Framleiðanda | Tegund    | Viðmót | Athugasemdir                |
|--------------|----------|-----------|-------------------------|
| Epson        | Tm T88IV | OPOS      |                         |
| Epson        | TM T88V  | OPOS      |                         |
| Star         | TSP650II | OPOS      |                         |
| Star         | TSP650II | Sérsniðinn    | Tengdar í gegnum netið   |
| Star         | mPOP     | OPOS      | Tengt gegnum Bluetooth |
| HP           | F7M67AA  | OPOS      | Rafhlöðu USB             |

#### <a name="bar-code-scanner"></a>Strikamerkjaskanni

| Framleiðanda  | Tegund         | Viðmót | Athugasemdir |
|---------------|---------------|-----------|----------|
| Motorola      | DS9208        | OPOS      |          |
| Honeywell     | 1900          | UWP       |          |
| Tákn        | LS2208        | OPOS      |          |
| Samþætt HP | E1L07AA       | OPOS      |          |
| Datalogic     | Magellan 8400 | OPOS      |          |

#### <a name="pin-pad"></a>PIN-takkaborð

| Framleiðanda | Tegund  | Viðmót | Athugasemdir                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | Krefst sérsnið tengilínu greiðslunnar |

#### <a name="payment-terminal"></a>Greiðslustöð

| Framleiðanda | Tegund | Viðmót | Athugasemdir                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Equinox      | L5300 | Sérsniðinn    | Krefst sérsnið tengilínu greiðslunnar                                |
| VeriFone     | MX925 | Sérsniðinn    | Krefst sérsniðinn greiðslutengill; tengdar í gegnum netið og USB |
| VeriFone     | MX915 | Sérsniðinn    | Krefst sérsniðinn greiðslutengill; tengdar í gegnum netið og USB |

#### <a name="cash-drawer"></a>Peningaskúffa

| Framleiðanda | Tegund     | Viðmót | Athugasemdir                |
|--------------|-----------|-----------|-------------------------|
| Star         | mPOP      | OPOS      | Tengt gegnum Bluetooth |
| APG          | Atwood    | Sérsniðinn    | Tengdar í gegnum netið   |
| Star         | SMD2 1317 | OPOS      |                         |
| HP           | QT457AA   | OPOS      |                         |

#### <a name="line-display"></a>Línuskjár

| Framleiðanda  | Tegund   | Viðmót | Athugasemdir |
|---------------|---------|-----------|----------|
| HP samþætta | G6U79AA | OPOS      |          |
| Epson         | M58DC   | OPOS      |          |

#### <a name="signature-capture"></a>Sækja undirskrift

| Framleiðanda | Tegund  | Viðmót | Athugasemdir |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>Vigt

| Framleiðanda | Tegund         | Viðmót | Athugasemdir |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OPOS      |          |

#### <a name="msr"></a>Kortalesari

| Framleiðanda | Tegund       | Viðmót | Athugasemdir |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="dedicated-iis-hardware-station"></a>Sérnýtta IIS vélbúnaðarstöð

Eftirfarandi jaðartæki voru prófaðar með því að nota sérstakan (ekki samnýttrar) IIS vélbúnaðarstöð ásamt Modern POS fyrir Windows og Skýi Sölustaðar.

#### <a name="printer"></a>Prentari

| Framleiðanda | Tegund    | Viðmót | Athugasemdir                  |
|--------------|----------|-----------|---------------------------|
| Epson        | Tm T88IV | OPOS      |                           |
| Epson        | TM T88V  | OPOS      |                           |
| Star         | TSP650II | OPOS      |                           |
| Star         | TSP650II | Sérsniðinn    | Tengdar í gegnum netið     |
| Star         | TSP100   | OPOS      | Krefst TSP650II lyftara |
| HP           | F7M67AA  | OPOS      | Rafhlöðu USB               |

#### <a name="bar-code-scanner"></a>Strikamerkjaskanni

| Framleiðanda  | Tegund   | Viðmót | Athugasemdir |
|---------------|---------|-----------|----------|
| Motorola      | DS9208  | OPOS      |          |
| Tákn        | LS2208  | OPOS      |          |
| Samþætt HP | E1L07AA | OPOS      |          |

#### <a name="pin-pad"></a>PIN-takkaborð

| Framleiðanda | Tegund  | Viðmót | Athugasemdir                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | Krefst sérsnið tengilínu greiðslunnar |

#### <a name="payment-terminal"></a>Greiðslustöð

| Framleiðanda | Tegund | Viðmót | Athugasemdir                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Equinox      | L5300 | Sérsniðinn    | Krefst sérsnið tengilínu greiðslunnar                                |
| VeriFone     | MX925 | Sérsniðinn    | Krefst sérsniðinn greiðslutengill; tengdar í gegnum netið og USB |
| VeriFone     | MX915 | Sérsniðinn    | Krefst sérsniðinn greiðslutengill; tengdar í gegnum netið og USB |

#### <a name="cash-drawer"></a>Peningaskúffa

| Framleiðanda | Tegund     | Viðmót | Athugasemdir              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Sérsniðinn    | Tengdar í gegnum netið |
| Star         | SMD2 1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |

#### <a name="line-display"></a>Línuskjár

| Framleiðanda  | Tegund   | Viðmót | Athugasemdir |
|---------------|---------|-----------|----------|
| HP samþætta | G6U79AA | OPOS      |          |
| Epson         | M58DC   | OPOS      |          |

#### <a name="signature-capture"></a>Sækja undirskrift

| Framleiðanda | Tegund  | Viðmót | Athugasemdir |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>Vigt

| Framleiðanda | Tegund         | Viðmót | Athugasemdir |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OPOS      |          |

#### <a name="msr"></a>Kortalesari

| Framleiðanda | Tegund       | Viðmót | Athugasemdir |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="shared-iis-hardware-station"></a>Samnýttar IIS vélbúnaðarstöð

Eftirfarandi jaðartæki voru prófaðar með því að nota samnýtta vélbúnaðarstöð IIS ásamt Modern POS fyrir Windows og Skýi Sölustaðar. **Athugasemd:** Aðeins á prentara, afgreiðslustöð greiðslu og peningaskúffu eru studd.

#### <a name="printer"></a>Prentari

| Framleiðanda | Tegund    | Viðmót | Athugasemdir                  |
|--------------|----------|-----------|---------------------------|
| Epson        | Tm T88IV | OPOS      |                           |
| Epson        | TM T88V  | OPOS      |                           |
| Star         | TSP650II | OPOS      |                           |
| Star         | TSP650II | Sérsniðinn    | Tengdar í gegnum netið     |
| Star         | TSP100   | OPOS      | Krefst TSP650II lyftara |
| HP           | F7M67AA  | OPOS      | Rafhlöðu USB               |

#### <a name="payment-terminal"></a>Greiðslustöð

| Framleiðanda | Tegund | Viðmót | Athugasemdir                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| VeriFone     | MX925 | Sérsniðinn    | Krefst sérsniðinn greiðslutengill; tengdar í gegnum netið og USB |
| VeriFone     | MX915 | Sérsniðinn    | Krefst sérsniðinn greiðslutengill; tengdar í gegnum netið og USB |

#### <a name="cash-drawer"></a>Peningaskúffa

| Framleiðanda | Tegund     | Viðmót | Athugasemdir              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Sérsniðinn    | Tengdar í gegnum netið |
| Star         | SMD2 1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |

## <a name="troubleshooting"></a>Úrræðaleit
### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a>Modern POS kannar retail hardware station hennar listanum fyrir val, en það er hægt að ljúka við upp að para vélbúnaðarstöðina

**Lausn:** Staðfesta eftirfarandi listi yfir hugsanlega mistök punktar:

-   Á tölvunni sem keyrir Modern POS trusts skírteini sem notað er á tölvunni sem keyrir retail hardware station.
    -   Til að sannreyna þessi uppsetning í vefvafra, fara á eftirfarandi SLÓÐ: https://&lt;Tölvuheiti&gt;:&lt;Tengisnúmer&gt;/HardwareStation /, ping-boð.
    -   Þessi SLÓÐ notar á, ping-boð til að staðfesta tölvunni hlýst og vafra gefur til kynna hvort skírteinið trausta. (Til dæmis í Internet Explorer læsa táknið birtist í aðseturslínunni. Þegar smellt er á þetta tákn staðfestir Internet Explorer skírteinið er nú traustur. Hægt er að setja skírteinið á staðbundnu tölvunni með því að skoða upplýsingar um skírteinið sem birtast.)
-   Á tölvunni sem keyrir retail hardware station er tengið sem retail hardware station verður notuð opinn í eldvegg.
-   Vélbúnaðarstöðin hefur rétt sett upp á upplýsingar til að setja Upp upplýsingar um söluaðila verkfæri sem keyrist við lok uppsetningarforrits hardware station.

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a>Modern POS getur ekki séð retail hardware station hennar listanum fyrir val

**Lausn:** Annaðhvort eftirfarandi þáttum getur valdið vandamálið:

-   Retail hardware station hefur ekki verið sett upp rétt í headquarters. Fylgið skrefum fyrr í þessum kafla til að staðfesta station vélbúnaðarreglu og retail hardware station eru rétt inn.
-   Hefur ekki verið keyrt vinnslur til að uppfæra skilgreiningu rásar. Í þessu tilfelli 1070 er vinnsla keyrð fyrir.

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a>Modern POS ekki endurspegla nýjum stillingum skúffu reiðufjár

**Lausn:** yfirstandandi runa Lokast. Breytingar á peningaskúffunni ekki eru kostnaðarjafnaðar uppfærð Modern POS þar til núverandi rununni er lokað.

### <a name="modern-pos-is-reporting-an-issue-with-a-retail-peripheral"></a>Modern POS er skýrslugerð vandamál með retail jaðarbúnaði

**Lausn:** eru sum dæmigert orsökum vandamálið Hér:

-   Gangið úr skugga um að önnur skilgreiningarforritunum bílstjóra tækið er lokað. Ef þessar utilities eru opnar, þær gætu komið í veg fyrir Modern POS eða retail hardware station claiming tækið.
-   Ef retail jaðarbúnaðurinn er samnýtt með mörgum POS-tæki, ganga úr skugga um að sem hún tilheyrir eitt af eftirfarandi tegundum:
    -   Peningaskúffa
    -   Kvittun prentara
    -   Greiðslustöð

    Ef jaðarbúnaðurinn tilheyrir ekki þessara tegunda, ekki retail hardware station hannað til að gera jaðarbúnaðurinn til samnýttar á milli margra POS-tæki.
-   Stundum tækið flutningsskrá getur valdið common control hlutir (CCOs) til að stöðva vinna rétt. Ef nýlega hefur verið sett upp tæki, en það er ekki virki rétt eða álagsritsins öðrum vandamálum, er hægt oft leysa þetta vandamál með hefur verið núllstillt er CCOs. Til að sækja í CCOs, þjónustuheimsókn <http://monroecs.com/oposccos_current.htm>.
-   Ef breytingarnar tíðan jaðarbúnaði við prófun eða úrræðaleit, gæti þurft að endurstilla IIS í stað þess að bíða skyndiminni til að endurnýja sjálfa. Til að endurstilla IIS, skal fylgja þessum skrefum:
    1.  Úr á **Ræsa** valmynd, gerð **CMD**.
    2.  Í leitarniðurstöðum, hægrismellt **skipanakvaðningu**, og smellið síðan á **Keyra sem kerfisstjóri**.
    3.  Í því **skipanakvaðningu** glugga, gerð **iisreset /Restart** og styðjið síðan á Enter.
    4.  Endurræsa Modern POS eftir IIS hefur verið endurræst.
-   Meðan verið er að gera breytingar á tíðan jaðartæki, ef að hefja einnig oft og loka biðlara Sölustaðar, getur ferlið dllhost úr fyrri setu POS interfere með núgildandi lotu. Í þessu tilfelli tæki hugsanlega ekki hægt að nota fyrr en þú lokar hýsli safn kvik tengil (DLL) sem stjórnar fyrri setu. Til að loka DLL host, skal fylgja þessum skrefum:
    1.  Úr á **Ræsa** valmynd, gerð **stjórnanda Verks**.
    2.  Í leitarniðurstöðum, smellið á **stjórnanda Verks**.
    3.  Í stjórnanda Verks, á við **Upplýsingar** flipanum, smellið á haus dálksins sem merktur er **Heiti** til að raða í töflu í stafrófsröð eftir heiti.
    4.  Fletta niður fyrr en hægt er að finna dllhost.exe.
    5.  Veljið hvern DLL-hýsil og smellið síðan á **lokastarf**.
    6.  Endurræsa Modern POS eftir hýsir DLL hefur verið lokað.


<a name="see-also"></a>Sjá einnig
--------

[Jaðarbúnaði hermi smásölu](retail-peripheral-simulator.md)


