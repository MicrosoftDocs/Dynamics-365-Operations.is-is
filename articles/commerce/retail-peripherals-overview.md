---
title: Jaðarbúnaður
description: Þessi grein útskýrir hugtökin sem tengjast Commerce jaðartækjum.
author: BrianShook
ms.date: 09/08/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: josaw
ms.custom:
- "268444"
- intro-internal
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: b3113626b18ad7f074c808d7631d13b09071bef2
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459995"
---
# <a name="peripherals"></a>Jaðarbúnaður

[!include[banner](includes/banner.md)]

Þessi grein útskýrir hugtökin sem tengjast jaðartækjum geyma. Það lýsir mismunandi máta sem hægt er að tengja jaðartæki við sölustað (POS) og íhlutunum sem bera ábygð á stjórnun tengingar með POS.

## <a name="concepts"></a>Hugtök

### <a name="pos-registers"></a>Afgreiðslukassar

Leiðsögn: Farðu á **Verslun og verslun \> Rásaruppsetning \> POS uppsetning \> Skrár**. Punktur afgreiðslukassa á sölustað er eining sem er notuð til að skilgreina eiginleika sértækts tilviks í POS. Þessir eiginleikar taka til vélbúnaðarsniðs eða uppsetningar fyrir jaðarbúnað sem verður notað hjá afgreiðslukassanum, verslunina sem afgreiðslukassinn er varpaður á og sjónræna upplifun fyrir notandann sem skráir sig inn í þann kassa.

### <a name="devices"></a>Tæki

Leiðsögn: Farðu á **Verslun og verslun \> Rásaruppsetning \> POS uppsetning \> Tæki**. Tæki er eining sem stendur fyrir efnislegt tilvik tækis sem er varpað í afgreiðslukassa. Þegar tæki er stofnað, er það varpað á afgreiðslukassa. Tækjaeiningin rekur upplýsingar um þegar afgreiðslukassi er virkjaður, gerð biðlara sem verið er að nota og forritapakka sem hefur verið virkjað á tiltekna tæki. 

Hægt er að kortleggja tæki á eftirfarandi forritagerðir:Retail Modern POS, Retail Cloud POS,Retail Modern POS –Android, og Retail Modern POS - iOS.

### <a name="modern-pos"></a>Modern POS

Modern POS er POS-forritið fyrir Microsoft Windows. Það er hægt að nota það á Windows 10 og Windows 11 stýrikerfi.

### <a name="cloud-pos"></a>Sölustaður í skýi

Cloud POS er vafrabyggð útgáfa á Modern POS-forritinu sem hægt er að opna í vafra.

### <a name="modern-pos-for-ios"></a>Modern POS fyrir iOS

Modern POS fyrir iOS er iOS-byggð útgáfa á Modern POS-forritinu sem hægt er að virkja á iOS-tækjum.

### <a name="modern-pos-for-android"></a>Modern POS fyrir Android

Modern POS fyrir Android er Android-byggð útgáfa á Modern POS-forritinu sem hægt er að virkja á Android-tækjum.

### <a name="pos-peripherals"></a>POS-jaðarbúnaður

POS-jaðartæki eru tæki sem sérstaklega eru studd fyrir aðgerðir POS. Þessum jaðartækjum er yfirleitt skipt niður í tiltekna klasa. Fyrir frekari upplýsingar um þessa flokka, sjá "Tækjaflokkar" hluta þessarar greinar.

### <a name="hardware-station"></a>Vélbúnaðarstöð

Leiðsögn: Farðu á **Verslun og verslun \> Rásir \> Búðir \> Allar verslanir**. Veldu verslun og veldu síðan **Vélbúnaðarstöðvar** Hraðflipi. Stillingin **Vélbúnaðarstöð** er stilling á rásarstigi sem er notuð til að skilgreina tilvik þar sem rök jaðarbúnaðar verða notuð. Þessi stilling á stigi rásar er notuð til að ákvarða eiginleika vélbúnaðarstöðvar smásölu. Hún er einnig notuð til að lista vélbúnaðarstöðvar sem eru í boði fyrir tilvik Modern POS í tiltekinni verslun. Vélbúnaðarstöð er innbyggð í forrit Modern POS fyrir Windows og Android. Einnig er hægt að nota vélbúnaðarstöð óháð sem sjálfstætt forrit Microsoft Internet Information Services (IIS). Í þessu tilviki er aðgangur að því í gegnum netið.

### <a name="hardware-profile"></a>Vélbúnaðarregla

Leiðsögn: Farðu á **Verslun og verslun \> Rásaruppsetning \> POS uppsetning \> POS snið \> Vélbúnaðarsnið**. Vélbúnaðarregla er listi yfir tæki sem eru grunnstillt fyrir afgreiðslukassa eða vélbúnaðarstöð. Vélbúnaðarreglum er úthlutað beint á afgreiðslukassa eða vélbúnaðarstöð.

## <a name="devices-classes"></a>Tækjaklasar
POS-jaðarbúnaði er yfirleitt skipt niður í klasa. Þessi hluti lýsir og gefur yfirlit yfir tæki sem Modern POS styður.

### <a name="printer"></a>Prentari

Prentarar eru meðal annars venjulegur kvittanaprentari POS og heilsíðuprentarar. Prentarar eru studdir í gegnum Object Linking og Embedding fyrir Retail POS (OPOS) og Microsoft Windows ökumannsviðmót. Allt að tvo prentara má nota á sama tíma. Þessi eiginleiki styður aðstæður þar sem kvittanir viðskiptavina með reiðufé eru prentaðar á kvittanaprentara, en pantanir viðskiptavina sem bera nánari upplýsingar, eru prentaðar á heilsíðuprentara. Kvittanaprentara er hægt að tengja beint við tölvu gegnum USB, tengja neti við Ethernet eða tengja við Bluetooth.

### <a name="scanner"></a>Skanni

Allt að tvo prentara má nota á sama tíma. Þessi eiginleiki styður aðstæður þar sem skanni sem er meira farsími er nauðsynlegur til að skanna stórar eða þungar vörur, en fastur ívafinn skanni er notaður fyrir flestar vörur í staðlaðri stærð, til að flýta greiðsluferli. Skannar geta verið studdir í OPOS, Universal Windows Platform (UWP) eða viðmótum lyklaborð kortalesara. Hægt er að nota USB eða Bluetooth til að tengja skanna við tölvu.

### <a name="msr"></a>Kortalesari

Hægt er að setja upp einn USB kortalesara (MSR) með því að nota OPOS-rekla. Ef óskað er að nota sjálfstæðan kortalesara fyrir kortamillifærslur (EFT) á greiðslufærslum verður Kortalesara að vera stjórnað af tengilínu greiðslunnar. Hægt er að nota sjálfstæða kortalesara fyrir vildarkortsfærslu viðskiptavinar, innskráningu starfsmanns og gjafakortsfærslu, óháð tengilínu greiðslunnar.

### <a name="cash-drawer"></a>Peningaskúffa

Tvær peningaskúffur geta verið studdar á vélbúnaðarreglu. Þessi eiginleiki gerir tvær virkar vaktir virkar á hvern afgreiðslukassa til að vera tiltækar í einu. Ef samnýtt vakt eða peningaskúffa sem er notað af mörgum POS fartæki á sama tíma er aðeins ein peningaskúffu er leyft á hverja vélbúnaðarreglu. Peningaskúffur er hægt að tengja beint við tölvu gegnum USB, tengja við net eða tengja við kvittanaprentara með RJ12-viðmóti. Í sumum tilvikum, geta peningaskúffur einnig að vera tengdur gegnum Bluetooth.

### <a name="line-display"></a>Línuskjár

Línubirtingar eru notaðar til að sýna afurðir, færslustöður og aðrar gagnlegar upplýsingar til viðskiptavinar við færslu. Ein línubirting getur verið tengd við tölvu gegnum USB með því að nota OPOS-rekla.

### <a name="signature-capture"></a>Sækja undirskrift

Undirskriftatæki eru tengd beint tölvunni gegnum USB með því að nota OPOS-rekla. Þegar sækja undirskrift er skilgreind er viðskiptavinur beðinn um að undirrita á tækinu. Eftir að undirskrift er veitt, er hún sýnd gjaldkera til að samþykkja.

### <a name="scale"></a>Kvarði

Vigt má tengja við tölvu gegnum USB með því að nota OPOS-rekla. Þegar afurð sem er merkt sem „Vigtuð" afurð hefur verið bætt við færslu, les POS þyngdina af vigtinni, bætir afurðinni við færsluna og notar magnið sem vigtin gaf upp.

### <a name="pin-pad"></a>PIN-takkaborð

Takkaborð fyrir persónuleg auðkennisnúmer (PIN) eru studd með OPOS, en það verður að stjórna þeim í gegnum greiðslutengi.

### <a name="secondary-display"></a>Aukabirting

Þegar aukabirting er skilgreind, Windows birtingu númer 2 er notuð til að sýna grunnupplýsingar. Sjálfgefið er að aukaskjárinn er ekki stillanlegur og sýnir takmarkað efni. Tilgangur aukaskjásins er að styðja við sjálfstæða hugbúnaðarframleiðanda (ISV) viðbót. 

### <a name="payment-device"></a>Greiðslutæki

Stuðningur við greiðslutæki er innleiddur gegnum greiðslutengi. Greiðslutæki geta framkvæmt eina eða margar aðgerðir sem aðrir tækjaklasar veita. Til dæmis, getur greiðslutæki virkað sem MSR/kortalesari, línuskjár, sækja undirskrift eða PIN-takkaborð. Stuðningu við greiðslutæki er innleiddur óháð stuðningi sjálfstæðra tæka sem lögð er til fyrir önnur tæki sem eru innifaldar í vélbúnaðarreglu.

## <a name="supported-interfaces"></a>Studd viðmót
### <a name="opos"></a>OPOS

Til að aðstoða við að tryggja að hægt sé að nota stærsta svið tækja með Commerce, er OLE fyrir POS atvinnustaðallinn aðalverkvangur jaðarbúnaðar sem er studdur. OLE fyrir POS staðallinn var framleiddur af National Retail Federation (NRF), sem kemur á samskiptareglum víddarsamsetningar atvinnugrein staðlaða samskiptum fyrir jaðartæki. OPOS er víðnotuð innleiðing á OLE fyrir POS-staðlinum. Hann var þróaður í um miðjan tíunda áratuginn og hefur verið uppfærður nokkrum sinnum síðan. OPOS veitir uppbyggingu tækjaekils sem auðveldar samþættingu POS-vélbúnaðarregla við Windows-byggð POS-kerfi. OPOS-stýringar annast samskiptum milli samhæfanlegs vélbúnaðar og hugbúnaður POS. OPOS-stýring samanstendur af tveimur hlutum:

-   **Stýringarhlutur** – Stýringarhlutur fyrir tækjaklasa (t.d. línubirting) veitir viðmót fyrir hugbúnaðarforritið. Monroe Consulting Services ([www.monroecs.com](http://www.monroecs.com/)) veitir staðlaðan listi eða samsafn af OPOS stýrihlutir sem eru þekkt sem almennir stýringarhlutir (CCOs). CCOs eru notaðir til að prófa POS-íhluti Commerce. Þess vegna hjálpar prófun til við að tryggja að ef Commerce styður tækjaklasa gegnum OPOS, geta margar gerðir smásölutækja verið studdur að ví tilskildu að framleiðanda veitir þjónustuhlut sem er byggð á fyrir OPOS. Ekki þarf að prófa sérstaklega hverja gerð tækis.
-   **Þjónustuhlutur** – Þjónustuhlutur veitir samskipti milli Stýringar hlutur (CCO) og tæki. Yfirleitt er þjónustuhlutur fyrir tæki veittur af framleiðanda tækis. Hins vegar gæti í sumum tilfellum þurft að sækja þjónustuhlutinn frá vefsvæði framleiðanda. Til dæmis gæti nýrri þjónustuhlutur verið tiltækur. Til að finna aðsetur framleiðanda á vefsvæði skal sjá fylgigögn vélbúnaðarreglu.

[![Stýringarhlutur og þjónustuhlutur.](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png) Stuðningur fyrir OPOS-innleiðingu á OLE fyrir POS hjálpar til við að tryggja að ef tækjaframleiðendur og útgefendur POS innleiða staðalinn rétt geta POS-kerfi og studd tæki unnið saman, jafnvel þótt þau hafi ekki verið áður prófuð saman. 

> [!NOTE]
> OPOS-stuðningur tryggir ekki samræmdan stuðning fyrir öll tæki með OPOS-reklum. Commerce verður fyrst að styðja þá tækjagerð eða klasa, gegnum OPOS. Þar að auki eru þjónustuhlutir hugsanlega ekki alltaf uppfærðir með nýjustu útgáfu af CCOs. Það ætti einnig að hafa í huga að, almenna gæði þjónustuhluta eru breytileg.

### <a name="windows"></a>Gluggar

Prentun á kvittun á POS er bestuð fyrir OPOS. OPOS hættir til að vera mikið hraðara en prentun gegnum Windows. Því er gott að nota OPOS, sérstaklega í umhverfi þar sem 40-dálka kvittanir eru prentaðar og færslutími verður að vera hraður. Fyrir flest tæki notarðu OPOS stýringar. Hins vegar, styðja sumir OPOS-kvittanaprentarar einnig Windows-rekla. Með því að nota Windows-rekill hægt er að nálgast síðasta letur og netlén einn prentari fyrir marga afgreiðslukassa. Hins vegar eru vankantar á því að nota Windows-rekla. Hér eru nokkur dæmi um þessa vankanta:

-   Þegar Windows-reklar eru notaðir, myndir eru samhæfðar áður en prentun hefst. Þess vegna hættir prentun til að vera hægari en hún er á prentara sem nota OPOS-stýringar.
-   Tæki sem eru tengd gegnum prentara ("daisy-chained") virka hugsanlega ekki rétt þegar Windows-reklar eru notaðir. Til dæmis gæti peningaskúffan ekki opnast eða kvittunarprentarinn virkar ekki eins og þú bjóst við.
-   OPOS styður einnig yfirgripsmeiri safn af breytum sem tengjast kvittanaprentara, eins og prentun fylgiseðla eða klipping pappír.
-   Windows prentarar eru ekki studdir í gegnum IIS vélbúnaðarstöðina. 

Ef OPOS-stýringar eru tiltækar fyrir Windows-prentara sem verið er að nota ætti prentara samt að virka rétt með Commerce.

### <a name="plug-and-play-devices"></a>Plug and play tæki

Þegar plug and play tæki er tengt við Windows stýrikerfisútgáfu sem styður þessa tegund tækis þarf engan rekil til að tækið sé notað eins og ætlað er. Til dæmis, ef Windows skynjar Bluetooth hátalara tæki, veit stýrikerfið að tækið er með „Högtalara“ flokksgerðina og meðhöndlar það tæki sem hátalara. Engrar frekari uppsetningar er krafist. 

Þegar um POS jaðartæki er að ræða, er hægt að tengja mörg USB tæki í og viðurkenna af Windows OS sem Human Interface Devices (HID). Hins vegar gæti Windows ekki getað ákvarðað möguleikana sem tækið býður upp á, vegna þess að tækið tilgreinir ekki flokk eða gerð tækis. Í Windows 10 hefur tækjaklösum fyrir strikamerkjaskanna og kortalesara verið bætt við. Þess vegna ef tæki sýnir sig í Windows 10 sem tæki eins af þessum klösum mun Windows hlusta eftir tilvikum úr tækinu á viðeigandi tímum.

Modern POS styður UWP-kortalesara og skanna. Þess vegna, þegar Modern POS er tilbúið fyrir inntak frá einu af þessum tækjum, og tæki sem tilheyrir einum af tækjaflokkunum er tengt, er hægt að nota það tæki. Til dæmis, ef stinga og spila strikamerkjaskanni er tengt við Windows 10 tölvu, og strikamerki innskráning er stillt fyrir Modern POS, verður strikamerki skanni virkur á innskráningarsíðunni. Engrar frekari uppsetningar er krafist.

Verið er að bæta við fleiri flokkum POS jaðartækja við Windows, svo sem flokkum fyrir peningaskúffur og kvittunarprentara. Stuðningur fyrir þessa nýja tækjaklasa í Modern POS er í bið.

> [!NOTE] 
> Ákveðin USB-tæki geta orðið óviðbragðslaus eða óáreiðanleg þegar þeim er stjórnað af Windows 10 orkustjórnunareiginleika sem kallast [USB Selective Suspend](/windows-hardware/drivers/usbcon/usb-selective-suspend). Ef USB-jaðartæki bregst ekki, gæti verið nauðsynlegt að slökkva á sértæka biðaðgerðinni fyrir það tæki. Fyrir frekari upplýsingar, sjá [Virkja Selective Suspend](/windows-hardware/drivers/usbcon/usb-selective-suspend#enabling-selective-suspend). 

### <a name="keyboard-wedge"></a>Lyklaborðstenging

Lyklaborðstengingartæki senda gögn í tölvuna eins og þau gögn hafi verið slegin inn á lyklaborð. Þess vegna er sjálfgefið að svæði sem er virkt í POS móttekur gögn sem er skönnuð eða sem var lesið. Í sumum tilvikum getur þessi virkni valdið því að röng gagnagerð er skönnuð á rangt svæði. Til dæmis gæti strikamerki verið skannað inn í svæði sem er ætlað fyrir innfærslu gagna kreditkorts. Í mörgum tilfellum er rökfræði við POS sem ákvarðar hvort gögnin sem eru skannuð eða strokuð séu strikamerki eða strok af korti. Þess vegna eru gögnin meðhöndluð rétt. Hins vegar, þegar tæki eru sett upp sem OPOS í stað lyklaborðsfleygbúnaðar, þá er meiri stjórn á því hvernig hægt er að neyta gagna frá þessum tækjum, því meira er "þekkt" um tækið sem gögnin koma frá. Til dæmis eru gögn úr strikamerkjaskanni sjálfkrafa viðurkennd sem strikamerki og tengd færsla í gagnagrunninum finnst betur og hraðar en ef almennan strengjaleit voru notuð, eins og tilfelli lyklaborðtengingartækja.

> [!NOTE]
> Þegar lyklaborðstenging við skanna er notuð á sölustað þarf að forrita hana til að senda boð til baka eða tilvik **Færslulykils** á eftir síðasta skannað staf. Ef þessi skilgreining er ekki gerð mun lyklaborðstenging við skanna ekki virka á réttan hátt. Skoðið fylgigögnin sem tækjaframleiðandi veitir til að fá upplýsingar um hvernig á að bæta við tilviki vegna boða sem send eru til baka.  

### <a name="device-printers"></a>Tæki prentarar

Hægt er að stilla prentara af gerðinni "Tæki" til að biðja notandann um að velja prentara sem er stilltur fyrir tölvuna. Þegar prentari af gerðinni "Tæki" er stilltur, ef Modern POS rekst á prentskipun, verður notandinn beðinn um að velja prentara á lista. Þessi hegðun er frábrugðin hegðun Windows ökumanna, vegna þess að "Windows" prentarategundin, vélbúnaðarsniðið sýnir notandanum ekki lista yfir prentara. Þess í stað krefst hún þess að nefndur prentari sé veittur í svæðinu **tækjaheiti**.

### <a name="network"></a>Net

Hægt er að nota netslóðartengdar peningaskúffur, kvittanaprentara og afgreiðslustöðvar á neti, annaðhvort beint í gegnum vélbúnaðarstöð Interprocess Communications (IPC) sem er innbyggð í forritið Modern POS fyrir Windows eða í gegnum vélbúnaðarstöðina IIS fyrir aðra biðlarar Modern POS.

## <a name="hardware-station-deployment-options"></a>Notkunarvalkostir vélbúnaðarstöðvar

### <a name="dedicated"></a>Sérnýtt

Modern POS viðskiptavinir fyrir Windows og Android fela í sér **Sérnýtt** eða innbyggðar vélbúnaðarstöðvar. Þessir viðskiptavinir geta haft samskipti beint við jaðartæki með viðskiptatækni sem er innbyggð í forritin. Forritið Android styður aðeins nettæki. Fyrir frekari upplýsingar um jaðarstuðning við Android skaltu fara í greinnina [Setja upp forrit POS Hybrid á Android og iOS](./dev-itpro/hybridapp.md).

Til að nota sérstaka vélbúnaðarstöðina skaltu fylgja þessum skrefum.

1. Úthlutaðu vélbúnaðarsniði til skráar sem mun nota Modern POS fyrir Windows eða Android umsókn.
1. Búðu til vélbúnaðarstöð af gerðinni "Dedicated" fyrir verslunina þar sem skráin verður notuð. 
1. Opnaðu Modern POS í stillingu án skúffu og notaðu **Stjórna vélbúnaðarstöðvum** aðgerð til að kveikja á getu vélbúnaðarstöðvarinnar. Sérstök vélbúnaðarstöð verður sjálfkrafa virk. 
1. Skráðu þig út af Modern POS. Skráðu þig svo inn aftur og opnaðu vakt. Jaðartækin sem eru stillt í vélbúnaðarsniðinu verða nú nothæf. 

### <a name="shared"></a>Deilt

Einnig stundum nefnd „IIS“ vélbúnaðarstöðin, „IIS“ sem gefur til kynna að POS forritið tengist vélbúnaðarstöðinni í gegnum Microsoft Internet Information Services. Forritið POS tengist IIS vélbúnaðarstöð smásölu með vefþjónustu sem keyra á tölvu þar sem tæki er tengt. Þegar samnýtt vélbúnaðarstöð er notuð, er hægt að nota jaðartæki sem tengjast vélbúnaðarstöð eftir afgreiðslukassa sem er á sama neti og IIS vélbúnaðarstöð smásölu. Þar sem aðeins Modern POS fyrir Windows og Android innihalda innbyggðan stuðning fyrir jaðartæki, verða öll önnur forrit Modern POS að nota IIS vélbúnaðarstöð smásölu til samskipta við POS jaðartæki sem eru skilgreindar í vélbúnaðarreglu. Þess vegna krefst hvert tilvik IIS vélbúnaðarstöðvar smásölu tölvu sem keyrir vefþjónusta og forrits sem hefur samskipti við tæki. 

Sameiginlegu vélbúnaðarstöðina er hægt að nota til að leyfa mörgum viðskiptavinum sölustaða að deila jaðartækjum eða hægt að nota til að stjórna tilteknu setti jaðartækja fyrir einn sölustað. 

Þegar vélbúnaðarstöð er notuð til að styðja við samnýtingu jaðartækja milli margra POS viðskiptavina, ætti aðeins að nota peningaskúffur, kvittunarprentara og greiðslumiðstöðvar. Ekki er hægt að tengja sjálfstæða strikamerkjaskanna, kortalesara, línubirtingar, vigtir eða önnur tæki á beinan hátt. Annars verða árekstrar þegar mörg POS-tæki reyna að gera kröfu til þessara jaðartækja á sama tíma. Svona er stjórnað átökum fyrir studd tæki:

-   **Peningaskúffa** – Peningaskúffan er opnuð með tilviki sem er sent á tækið. Vandamál geta komið upp ef hringt er í peningaskúffu á meðan skúffan er þegar opin. Peningaskúffu sem er notuð í sameiginlegri uppsetningu vélbúnaðarstöðvar ætti að vera stillt á **Deilt** í vélbúnaðarsniðinu. Þessi stilling kemur í veg fyrir að POS athugi hvort peningaskúffan sé þegar opin þegar hún sendir opnunarskipanir.
-   **Kvittanaprentarann** – Ef tvær prentskipanir kvittunar eru sendar samtímis til vélbúnaðarstöðvar smásölu kann önnur skipunina að glatast, en það fer eftir tæki. Sumar tæki eru með innri minni eða keyrslutíma sem getur komið í veg fyrir þetta vandamál. Ef prentskipun er ekki stofnaður, fær gjaldkeri villuboð og getur reynt að prenta skipunina aftur úr POS.
-   **Afgreiðslustöð** – Ef gjaldkerinn reynir að hefja færslu á afgreiðslustöð sem er þegar í notkun, tilkynna skilaboð honum að afgreiðslustöðin sé í notkun og biður gjaldkerann að reyna aftur síðar. Yfirleitt geta gjaldkerar séð að afgreiðslustöð er þegar í notkun og munu bíða þar til að annarri færsla er lokið áður en þeir reyna að hefja greiðslu aftur.

Villuleit er áætlað fyrir framtíðarútgáfu sem kannar hvort óstudd tæki eru settir upp fyrir vélbúnaðarregluna sem er varpað á samnýtt vélbúnaðarstöð. Ef einhver óstudd tæki finnast fær notandi skilaboð sem tilgreina að tækin eru ekki studd fyrir samnýttar vélbúnaðarstöðvar. Í tilviki samnýttra vélbúnaðarstöðva ætti að stilla valkostinn **Velja við greiðslumáta** á **Já** á stigi afgreiðslukassa. POS notanda er síðan beðinn um að velja vélbúnaðarstöð þegar greiðslumáti er valinn fyrir færslu í POS. Þegar vélbúnaðarstöð smásölu er aðeins valin við greiðslumáta er vali á vélbúnaðarstöð bætt beint við POS verkflæði fyrir fartækjaaðstæður. Sem viðbótar fríðinda, línuskjá greiðslunnar afgreiðslustöðvar er ekki notað fyrir samnýttar aðstæður. Ef afgreiðslustöðin er notað sem línuskjár, gæti aðrir notendur verið útilokaðir frá notkun á þeirri afgreiðslustöð þar til færslunni er lokið. Í fartækjaaðstæður gæti línum verið bætt við færslu með yfir lengra tímabil. Þess vegna er valkostsins **Velja við greiðslumáta** krafist til að tryggja framboð hagkvæmasta tækis.

### <a name="network-peripherals"></a>Net jaðarbúnaðar

Merki net fyrir tæki vélbúnaðarreglunni auðveldar að peningaskúffur, kvittanaprentara og afgreiðslustöðvar séu tengdir gegnum nettengingu.

#### <a name="modern-pos-for-windows"></a>Modern POS fyrir Windows

Hægt er að tilgreina IP-tölur fyrir netjaðarbúnað á tveimur stöðum. Ef Modern POS Windows-biðlari notar eina samstæðu af netjaðartækja ætti að setja upp IP-tölur fyrir þau tæki með því að nota valkostinn **Grunnstilling IP-tölu** í Aðgerðarúðunni fyrir sjálfan afgreiðslukassann. Í tilviki nettækja sem verða samnýtt milli afgreiðslukassa er hægt að varpa vélbúnaðarreglu sem hefur nettæki úthlutað beint í samnýtta vélbúnaðarstöð. Til að úthluta IP-tölum, veljið þá vélbúnaðarstöð á síðunni **Verslanir** og nota síðan valkostinn **Grunnstilling IP-tölu** í hlutanum **Vélbúnaðarstöðvar** til að tilgreina nettæki sem eru úthlutaðar þeirri vélbúnaðarstöð. Fyrir vélbúnaðarstöðvar sem hafa aðeins nettæki, þarf ekki að virkja vélbúnaðarstöð sjálfa. Í þessu tilfelli er vélbúnaðarstöð smásölu aðeins áskilið til að flokka í raun netslóðartengd tæki eftir staðsetningu þeirra í verslunar.

#### <a name="cloud-pos-and-modern-pos-for-ios"></a>Cloud POS og Modern POS fyrir IOS

Rökin sem keyrir efnislega tengda og netléntengd jaðartæki eru geymd í vélbúnaðarstöð smásölu. Þess vegna fyrir alla biðlara POS nema Modern POS fyrir Windows og Android verður vélbúnaðarstöð við IIS að vera virkjuð og virk til að virkja POS til samskipta við jaðartæki, óháð því hvort þau jaðartæki eru efnislega tengdir vélbúnaðarstöð eða sendur hann á neti.

## <a name="setup-and-configuration"></a>Uppsetning og skilgreining
### <a name="hardware-station-installation"></a>Uppsetning vélbúnaðarstöðvar

Fyrir leiðbeiningar um hvernig á að setja upp IIS vélbúnaðarstöð, sjá [Stilla og setja upp vélbúnaðarstöð](retail-hardware-station-configuration-installation.md).

### <a name="modern-pos-for-windows-setup-and-configuration"></a>Uppsetning og skilgreining á Modern POS fyrir Windows

Nánari upplýsingar er að finna í [Skilgreina, setja upp og virkja Modern POS (MPOS)](retail-modern-pos-device-activation.md).

### <a name="modern-pos-for-android-and-ios-setup-and-configuration"></a>Uppsetning og skilgreining á Modern POS fyrir Android og iOS

Nánari upplýsingar er að finna í [Setja upp POS Hybrid-forrit í Android og iOS](./dev-itpro/hybridapp.md).

### <a name="opos-device-setup-and-configuration"></a>Uppsetning og skilgreining á OPOS-tæki

Nánari upplýsingar um íhluti OPOS er að finna í "Studd viðmót" hluta þessa skjals. Venjulega eru OPOS-reklar veittir af framleiðanda tækis. Þegar OPOS-tækjarekill hefur verið uppsettur bætir hann við lykli við Windows-stýriskrárinnar í einu af eftirfarandi stöðum:

-   **32 bita kerfi:** HKEY\_ STAÐBÆR\_ VÉL\HUGBÚNAÐUR\OLEforRetail\ServiceOPOS
-   **64 bita kerfi:** HKEY\_ STAÐBÆR\_ VÉL\SOFTWARE\WOW6432Node\OLEforRetail\ServiceOPOS

Innan staðsetningu ServiceOPOS stýriskrárinnar er skilgreindum tækjum raðað eftir OPOS-tækjaklasa. Margir tækjareklar eru vistaðir.

## <a name="supported-scenarios-by-hardware-station-type"></a>Studdar aðstæður eftir gerð vélbúnaðarstöðvar
### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a>Biðlarastuðningur – IPC vélbúnaðarstöð miðað við IIS vélbúnaðarstöð

Eftirfarandi tafla sýnir grannfræði og virkjun aðstæður sem eru studdar.

| Biðlari      | IPC vélbúnaðarstöð | IIS vélbúnaðarstöð |
|-------------|----------------------|----------------------|
| Windows-forrit | Já                  | Já                  |
| Sölustaður í skýi   | Nei                   | Já                  |
| Android     | Já                  | Já                  |
| iOS         | Nei                   | Já                  |

### <a name="network-peripherals"></a>Net jaðarbúnaðar

Netjaðartæki geta verið studd beint í gegnum vélabúnaðarstöð sem er byggð inn í forritið Modern POS fyrir forrit Windows og Android. Fyrir alla aðra biðlara, verður að virkja vélbúnaðarstöð á IIS.

| Biðlari      | IPC vélbúnaðarstöð | IIS vélbúnaðarstöð |
|-------------|----------------------|----------------------|
| Windows-forrit | Já                  | Já                  |
| Sölustaður í skýi   | Nei                   | Já                  |
| Android     | Já                  | Já                  |
| iOS         | Nei                   | Já                  |

## <a name="supported-device-types-by-hardware-station-type"></a>Studdar tækjagerðir eftir gerð vélbúnaðarstöðvar
### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Modern POS fyrir Windows með (innbyggðri) IPS vélbúnaðarstöð

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Studdur tækjaklasi</th>
<th>Studd viðmót</th>
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
<li>UWP (Engin uppsetning nauðsynleg.)</li>
<li>Lyklaborð kortalesara (Ekki krafist slíkrar uppsetningar.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Skúffa</td>
<td><ul>
<li>OPOS</li>
<li>Net </br><strong>Athugið</strong>: Aðeins er hægt að setja upp eina skúffu ef <strong>Nota samnýtt vakt</strong> er skilgreindur í skúffu.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Skúffa 2</td>
<td><ul>
<li>OPOS</li>
<li>Net </br><strong>Athugið</strong>: Aðeins er hægt að setja upp eina skúffu ef <strong>Nota samnýtt vakt</strong> er skilgreindur í skúffu.</li>
</ul></td>
</tr>
<tr class="even">
<td>Skanni</td>
<td><ul>
<li>OPOS</li>
<li>UWP (Engin uppsetning nauðsynleg.)</li>
<li>Lyklaborð kortalesara (Ekki krafist slíkrar uppsetningar.)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Skanni 2</td>
<td><ul>
<li>OPOS</li>
<li>UWP (Engin uppsetning nauðsynleg.)</li>
<li>Lyklaborð kortalesara (Ekki krafist slíkrar uppsetningar.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Vigt</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>PIN-takkaborð</td>
<td>OPOS (Stuðningur er veittur með sérsniðinn greiðslutengillinn).</td>
</tr>
<tr class="even">
<td>Sækja undirskrift</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Greiðslustöð</td>
<td><ul>
<li>Stuðningur við sérsniðið tæki</li>
<li>Net (Sjá fylgiskjal greiðslutengis fyrir frekari upplýsingar.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-committed-shared-iis-hardware-station"></a>Allir biðlarar Modern POS með ráðstafaða „samnýtta” IIS vélbúnaðarstöð

> [!NOTE]
> Þegar IIS vélbúnaðarstöðin er "skuldbundin" er eitt-á-mann samband milli POS biðlarans og vélbúnaðarstöðvarinnar.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Studdur tækjaklasi</th>
<th>Studd viðmót</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Prentari</td>
<td><ul>
<li>OPOS</li>
<li>Net</li>
</ul></td>
</tr>
<tr class="even">
<td>Prentari 2</td>
<td><ul>
<li>OPOS</li>
<li>Net</li>
</ul></td>
</tr>
<tr class="odd">
<td>Línubirting</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Kortalesari</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Skúffa</td>
<td><ul>
<li>OPOS</li>
<li>Net </br><strong>Athugið</strong>: Aðeins er hægt að setja upp eina skúffu á vélbúnaðarreglu ef <strong>Nota samnýtt vakt</strong> er skilgreindur í skúffu.</li>
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
<td>OPOS (Stuðningur er veittur með sérsniðinn greiðslutengillinn).</td>
</tr>
<tr class="odd">
<td>Undirskr. sækja</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Greiðslustöð</td>
<td><ul>
<li>Stuðningur við sérsniðið tæki</li>
<li>Net (Sjá fylgiskjal greiðslutengis fyrir frekari upplýsingar.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-share-an-iis-hardware-station"></a>Allir nútíma POS viðskiptavinir sem deila IIS vélbúnaðarstöð

> [!NOTE]
> Þegar vélbúnaðarstöð IIS er „samnýtt“, geta mörg tæki notað vélbúnaðarstöð á sama tíma. Fyrir þessar aðstæður á aðeins að nota þau tæki sem eru talin upp í eftirfarandi töflu. Ef reynt er að deila tæki sem ekki eru skráð á listanum hér, eins og strikamerkjaskanna og kortalesara munu villur eiga sér stað þegar mörg tæki reyna að gera kröfu á sama jaðarbúnaðinum. Í framtíðinni, verður sérstaklega komið í veg fyrir slíka grunnstillingu.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Studdur tækjaklasi</th>
<th>Studd viðmót</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Prentari</td>
<td><ul>
<li>OPOS</li>
<li>Net</li>
</ul></td>
</tr>
<tr class="even">
<td>Prentari 2</td>
<td><ul>
<li>OPOS</li>
<li>Net</li>
</ul></td>
</tr>
<tr class="odd">
<td>Skúffa</td>
<td><ul>
<li>OPOS</li>
<li>Net </br><strong>Athugið</strong>: Aðeins er hægt að setja upp eina skúffu á vélbúnaðarreglu ef <strong>Nota samnýtt vakt</strong> er skilgreindur í skúffu.</li>
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
<li>Stuðningur við sérsniðið tæki</li>
<li>Net (Sjá fylgiskjal greiðslutengis fyrir frekari upplýsingar.)</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a>Skilgreining fyrir studdar aðstæður
Nánari upplýsingar um hvernig á að búa til vélbúnaðarsnið, sjá [Tengja jaðarbúnað við sölustað (POS)](define-maintain-channel-clients-registers-hw-stations.md). 

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Modern POS fyrir Windows með (innbyggðri) IPS vélbúnaðarstöð

Þessi skilgreining er oftast dæmigert skilgreiningu fyrir venjulegt, föst afgreiðslukassar. Á þessu dæmi, upplýsingar um forstillingu vélbúnaðar varpað beint á sjálfan afgreiðslukassann. Afgreiðslustöðvarnúmer kortamillifærslu ætti einnig að setja á afgreiðslukassa sjálfa. Fylgið eftirfarandi skrefum til að setja upp þessa skilgreiningu.

1.  Stofna vélbúnaðarreglu þar sem allar nauðsynlegar jaðartæki eru skilgreind.
2.  Varpa vélbúnaðarregluna á afgreiðslukassa.
3.  Stofnaðu vélbúnaðarstöð af gerðinni **Sérhæfð** fyrir verslunina sem POS-afgreiðslukassinn verður notaður. Lýsing er valkvæð. 

    > [!NOTE]
    > Það þarf ekki að stilla aðra eiginleika í vélbúnaðarstöðinni. Allar aðrar nauðsynlegar upplýsingar eins og vélbúnaðarreglu, koma úr sjálfum afgreiðslukassanum.

4.  Farðu í **Retail og Commerce \> Upplýsingatækni í Retail og Commerce \> Dreifingaráætlun**.
5.  Velja skal **1090** dreifingaráætlun til að samstilla nýja vélbúnaðarreglu fyrir verslun. Veldu **Hlaupa núna** til að samstilla breytingar á POS.
6.  Velja skal **1040** dreifingaráætlun til að samstilla nýja vélbúnaðarstöð fyrir verslun. Veldu **Hlaupa núna** til að samstilla breytingar á POS.
7.  Setja upp og virkja Modern POS fyrir Windows.
8.  Hefja Modern POS fyrir Windows og byrja að nota tengda jaðartæki.

### <a name="modern-pos-for-android-with-an-ipc-built-in-hardware-station"></a>Modern POS fyrir Android með (innbyggðri) IPS vélbúnaðarstöð

**Nýtt fyrir 10.0.8** - Epson netprentarar og peningaskúffur tengdir þessum prenturum í gegnum DK tengi eru nú studdir fyrir Modern POS fyrir Android app. Nánari upplýsingar er að finna í greininni [Setja upp forrit POS Hybrid á Android og iOS](./dev-itpro/hybridapp.md).

### <a name="all-modern-pos-clients-that-have-a-committed-shared-iis-hardware-station"></a>Allir biðlarar Modern POS með ráðstafaða „samnýtta” IIS vélbúnaðarstöð

Þessa skilgreiningu er hægt að nota í öllum biðlurum Modern POS með vélbúnaðarstöð sem aðeins notuð í einum POS afgreiðslukassa. Fylgið eftirfarandi skrefum til að setja upp þessa skilgreiningu.

1.  Stofna vélbúnaðarreglu þar sem allar nauðsynlegar jaðartæki eru skilgreind.
2.  Stofnaðu vélbúnaðarstöð af gerðinni **Sérhæfð** fyrir verslunina sem POS-afgreiðslukassinn verður notaður.
3.  Stilltu á sérstakan vélbúnaðarstöð eftirfarandi eiginleika:
    -   **Hýsilheiti** – Heiti hýsils tölvu þar sem vélbúnaðarstöðin mun keyra. 
    
        > [!NOTE]
        > Cloud POS getur leyst **staðarhýsilinn** til að ákvarða staðbundnu tölvuna sem keyrir Cloud POS. Hins vegar verður skírteini sem krafist er til að para Cloud POS með vélbúnaðarstöðinni einnig að hafa "Staðarhýslinum" sem heiti tölvunnar. Til að forðast vandamál er ráðlagt að tilkynna tilvik hverrar sérstakrar vélbúnaðarstöðar verslunarinnar, eftir þörfum. Fyrir hverja vélbúnaðarstöð heiti hýsilsins ætti að vera heiti á tiltekinni tölvu þar sem vélbúnaðarstöðin verður virkjað.
    
    -   **Tengi** – Tengið sem nota á fyrir vélbúnaðarstöð til að eiga samskipti við biðlara Modern POS.
    -   **Vélbúnaðarregla** – Ef vélbúnaðarregluna er ekki veitt á vélbúnaðarstöð sjálf, vélbúnaðarreglu sem er úthlutað á afgreiðslukassa verður notuð.
    -   **Verslunarnúmer Kortamillifærslu númer** -Auðkenni afgreiðslustöðvar KORTAMILLIFÆRSLU Er að nota þegar KORTAMILLIFÆRSLU heimildum eru send. Þetta Kenni er veitt með kreditkortagjörvanum.
    -   **Pakkaheiti** – Vélbúnaðarstöðvarpakkinn sem á að nota þegar vélbúnaðarstöð er virkjuð.

4.  Farðu í **Retail og Commerce \> Upplýsingatækni í Retail og Commerce \> Dreifingaráætlun**.
5.  Velja skal **1090** dreifingaráætlun til að samstilla nýja vélbúnaðarreglu fyrir verslun. Veldu **Hlaupa núna** til að samstilla breytingar á POS.
6.  Velja skal **1040** dreifingaráætlun til að samstilla nýja vélbúnaðarstöð fyrir verslun. Veldu **Hlaupa núna** til að samstilla breytingar á POS.
7.  Setja upp vélbúnaðarstöð. Nánari upplýsingar um hvernig á að setja upp vélbúnaðarstöð er að finna í [Skilgreina og setja upp vélbúnaðarstöð Retail](retail-hardware-station-configuration-installation.md).
8.  Setja upp og virkja Modern POS. Nánari upplýsingar um hvernig á að setja upp Modern POS er að finna í [Skilgreina, setja upp og virkja Modern POS (MPOS)](retail-modern-pos-device-activation.md).
9.  Innskráning á Modern POS og veljið **Framkvæma aðgerðir utan skúffu**.
10. Byrja á **Stjórna vélbúnaðarstöðvar** aðgerð.
11. Veldu **Stjórna**.
12. Í stjórnunarsíðu vélbúnaðarstöðvar skal stilla valkost til að kveikja á vélbúnaðarstöðinni.
13. Veldu vélbúnaðarstöðina sem á að nota og veldu síðan **Par**.
14. Eftir að vélbúnaðarstöðin hefur verið pöruð skaltu velja **Loka**.
15. Á síðunni fyrir val á vélbúnaðarstöð skaltu velja nýlega valda vélbúnaðarstöðina til að gera hana virka.

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Allir biðlarar Modern POS með samnýtta IIS vélbúnaðarstöð

Þessa skilgreiningu er hægt að nota í öllum biðlurum Modern POS sem deila vélbúnaðarstöðvum með öðrum tækjum. Fylgið eftirfarandi skrefum til að setja upp þessa skilgreiningu.

1.  Stofna vélbúnaðarreglu þar sem nauðsynleg jaðartæki eru skilgreind.
2.  Stofnaðu vélbúnaðarstöð af gerðinni **Samnýtt** fyrir verslunina sem POS-afgreiðslukassinn verður notaður.
3.  Stilltu á samnýttri vélbúnaðarstöð eftirfarandi eiginleika:
    -   **Hýsilheiti** – Heiti hýsils tölvu þar sem vélbúnaðarstöðin mun keyra.
    -   **Lýsing** – Texta sem auðkenna vélbúnaðarstöð, eins og **Skil** eða **Framhlið verslunar**.
    -   **Tengi** – Tengið sem nota á fyrir vélbúnaðarstöð til að eiga samskipti við biðlara Modern POS.
    -   **Vélbúnaðarregla** - Fyrir samnýttar vélbúnaðarstöðvar ætti hver vélbúnaðarstöð að hafa vélbúnaðarreglu. Hægt er að deila vélbúnaðarreglum milli vélbúnaðarstöðva en þeim verður að vera varpað á hverja vélbúnaðarstöð. Þar að auki er mælt með að nota samnýtta vaktir þegar margar tæki nota sömu samnýttu vélbúnaðarstöð. Til að setja upp sameiginlega vakt skaltu fara á **Verslun og verslun \> Rásaruppsetning \> POS uppsetning \> POS snið \> Vélbúnaðarsnið**. Velja peningaskúffu fyrir hverja samnýtta vélbúnaðarreglu og stilla valkostinn **Samnýttum vakt skúffu** á **Já**.
    -   **Verslunarnúmer Kortamillifærslu númer** -Auðkenni afgreiðslustöðvar KORTAMILLIFÆRSLU Er að nota þegar KORTAMILLIFÆRSLU heimildum eru send. Þetta Kenni er veitt með kreditkortagjörvanum.
    -   **Pakkaheiti** – Vélbúnaðarstöðvarpakkinn sem á að nota þegar vélbúnaðarstöð er virkjuð.

4.  Endurtakið skref 2 og 3 fyrir hverja viðbótar vélbúnaðarstöð sem krafist er í versluninni.
5.  Farðu í **Retail og Commerce \> Upplýsingatækni í Retail og Commerce \> Dreifingaráætlun**.
6.  Velja skal **1090** dreifingaráætlun til að samstilla nýja vélbúnaðarreglu fyrir verslun. Veldu **Hlaupa núna** til að samstilla breytingar á POS.
7.  Velja skal **1040** dreifingaráætlun til að samstilla nýja vélbúnaðarstöð fyrir verslun. Veldu **Hlaupa núna** til að samstilla breytingar á POS.
8.  Setja upp vélbúnaðarstöð á hverri hýsitölvu sem sett er upp í skrefum 2 og 3. Nánari upplýsingar um hvernig á að setja upp vélbúnaðarstöð er að finna í [Skilgreina og setja upp vélbúnaðarstöð Retail](retail-hardware-station-configuration-installation.md).
9.  Setja upp og virkja Modern POS. Nánari upplýsingar um hvernig á að setja upp Modern POS er að finna í [Skilgreina, setja upp og virkja Modern POS (MPOS)](retail-modern-pos-device-activation.md).
10. Innskráning á Modern POS og veljið **Framkvæma aðgerðir utan skúffu**.
11. Byrja á **Stjórna vélbúnaðarstöðvar** aðgerð.

12. Veldu **Stjórna**.
13. Í stjórnunarsíðu vélbúnaðarstöðvar skal stilla valkost til að kveikja á vélbúnaðarstöðinni.
14. Veldu vélbúnaðarstöðina sem á að nota og veldu síðan **Par**.
15. Endurtakið skref 14 fyrir hverja vélbúnaðarstöð sem Modern POS notar.
16. Eftir að allar nauðsynlegar vélbúnaðarstöðvar hafa verið pöraðar skaltu velja **Loka**.
17. Á síðunni fyrir val á vélbúnaðarstöð skaltu velja nýlega valda vélbúnaðarstöðina til að gera hana virka. 

> [!NOTE]
> Ef tæki nota mismunandi vélbúnaðarstöðvar oft er ráðlagt að skilgreina Modern POS til að senda kvaðningu á gjaldkera til að velja vélbúnaðarstöð þegar þeir byrja á greiðslumátaferli. Opnaðu **Smásala og viðskipti \> Uppsetning rásar \> Uppsetning sölustaðar \> Afgreiðslukassar**. Veljið afgreiðslukassa og stillið valkostinn **Velja við greiðslumáta** á **Já**. Notaðu **1090** dreifingaráætlun til að samstilla breytingar við gagnagrunn rásar.

## <a name="extensibility"></a>Stækkunarhæfni
Sjá upplýsingar um aðstæður stækkunarhæfni fyrir vélabúnaðarstöð í [Samþætta POS við nýjan vélbúnað og mynda uppsetningarforrit viðbótar](dev-itpro/hardware-device-extension.md).

## <a name="security"></a>Öryggi
Samkvæmt gildandi öryggisstöðlum á að nota eftirfarandi stillingar í framleiðsluumhverfi: 

### <a name="hardware-station-installer"></a>Uppsetningarforrit vélbúnaðarstöðvar
Uppsetningarforrit vélbúnaðarstöðvar mun sjálfkrafa gera þessar breytingar á stýriskrá sem hluti af uppsetningu gegnum sjálfsafgreiðslu.

-   Secure Sockets Layer (SSL) ætti að gera óvirkt.
-   Einungis Transport Layer Security (TLS) útgáfu 1,2 (eða í gildandi hæsta) ætti að vera virkjuð og notuð. 

### <a name="ssl-and-tls"></a>SSL og TLS
Sjálfgefið er að SSL og allar útgáfur af TLS nema TLS 1.2 eru gerðar óvirkar. Fylgið eftirfarandi skrefum til að breyta eða virkja þessi gildi:
    1.  Styðjið á merki Windows lykill + Rannsókn til að opna í **Keyra** glugga.
    2.  Í **Opið** reit, tegund **Regedit**, og veldu síðan **Allt í lagi**.
    3.  Ef að **Stjórnun notendareiknings** skilaboðakassi birtist, veldu **Já**.
    4.  Í glugganum **Stýriskrána Ritill** fara í **HKEY\_STAÐBUNDNA\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**. Eftirfarandi lyklar hafa verið sjálfkrafa færðar inn til að leyfa aðeins fyrir TLS 1,2:
        -   TLS 1.2Server:Enabled=1
        -   TLS 1.2Server:DisabledByDefault=0
        -   TLS 1.2Client:Enabled=1
        -   TLS 1.2Client:DisabledByDefault=0
        -   TLS 1.1Server:Enabled=0
        -   TLS 1.1Client:Enabled=0
        -   TLS 1.0Server:Enabled=0
        -   TLS 1.0Client:Enabled=0
        -   SSL 3.0Server:Enabled=0
        -   SSL 3.0Client:Enabled=0
        -   SSL 2.0Server:Enabled=0
        -   SSL 2.0Client:Enabled=0
-   Engar viðbótarnetgáttir ættu að vera opnar, nema þeirra sé krafist af þekktum, tilgreindum ástæðum.
-   Gera verður tilfangasamnýtingu á milli uppruna óvirka og verður að tilgreina leyfð uppruna sem eru samþykktar.
-   Aðeins traust skírteini yfirvalda ætti að nota til að fá vottorð sem verður notaður í tölvum sem keyra vélbúnaðarstöðina.

> [!NOTE]
> Afar mikilvægt er að farið sé yfir öryggisleiðbeiningar fyrir IIS og þarfir greiðslukortageirans (PCI).

## <a name="peripheral-simulator"></a>Líkt eftir jaðarbúnaði
Sjá upplýsingar [Jaðarhermibúnaður fyrir Commerce](dev-itpro/retail-peripheral-simulator.md).

## <a name="microsoft-tested-peripheral-devices"></a>Jaðartæki Microsoft-tested
### <a name="ipc-built-in-hardware-station"></a>IPC (innbyggð) vélbúnaðarstöð

Eftirfarandi jaðartæki voru prófuð með því að nota IPC vélbúnaðarstöð sem er innbyggð í Modern POS fyrir Windows.

#### <a name="printer"></a>Prentari

| Framleiðandi | Líkan    | Viðmót | Athugasemdir                |
| ------------ | -------- | --------- | ----------------------- |
| Epson        | TM-T88V  | OPOS      |                         |
| Epson        | TM-T88IV | OPOS      |                         |
| HP           | H300     | OPOS      | Rafhlöðu USB             |
| Star         | TSP650II | Sérsnið    | Tengt gegnum netkerfi   |
| Star         | mPOP     | OPOS      | Tengt gegnum Bluetooth |
| Toshiba      | HSP100   | OPOS      |                         |
| Toshiba      | HSP150   | OPOS      |                         |

> [!NOTE]
> Star TSP 100 prentarinn er ekki studdur fyrir innbyggða vélbúnaðarstöðina. Innbyggða vélbúnaðarstöðin notar 64-bita ferli sem er ekki samhæft við núverandi Star TP 100 rekla. 

#### <a name="bar-code-scanner"></a>Strikamerkjaskanni

| Framleiðandi  | Líkan         | Viðmót | Athugasemdir |
| ------------- | ------------- | --------- | -------- |
| Datalogic     | Magellan 8400 | OPOS      |          |
| Honeywell     | 1900          | UWP       |          |
| HP Samþætt | E1L07AA       | OPOS      |          |
| Tákn        | LS2208        | OPOS      |          |

#### <a name="payment-terminals-and-pin-pads"></a>Greiðslustöðvar og PIN-blokkar

Dynamics 365 Commerce veitir út-af-kassa lausn fyrir samþættingu við Adyen fyrir greiðsluþjónustu. The [Dynamics 365 greiðslutengi fyrir Adyen](dev-itpro/adyen-connector.md) notar tæki-agnostic [Adyen Payment Terminal forritunarviðmót (API)](https://www.adyen.com/blog/introducing-the-terminal-api) og getur haft samskipti við allar greiðslustöðvar sem þetta API styður. Fyrir heildarlista yfir studdar greiðslustöðvar, sjá [Adyen POS útstöðvar](https://www.adyen.com/pos-payments/terminals).

Þú getur líka notað aðrar greiðslumiðlar með Dynamics 365 Commerce með því að búa til sérsniðið tengi. Hægt er að nota hvaða greiðslustöð sem er studd af greiðsluveitunni með Dynamics 365 Commerce. Á sama hátt,Dynamics 365 Commerce gerir ráð fyrir samþættingarlíkönum greiðslutækja sem er studd af greiðsluveitanda, svo sem staðbundin IP, skýja-API eða bein tenging (til dæmis með USB) við POS. Fyrir frekari upplýsingar, sjá [Búðu til enda-til-enda greiðslusamþættingu fyrir greiðslustöð](dev-itpro/end-to-end-payment-extension.md).

#### <a name="cash-drawer"></a>Peningaskúffa

| Framleiðandi | Líkan     | Viðmót | Athugasemdir                |
|--------------|-----------|-----------|-------------------------|
| Star         | mPOP      | OPOS      | Tengt gegnum Bluetooth |
| APG          | Atwood    | Sérsniðinn    | Tengt gegnum netkerfi   |
| Star         | SMD2-1317 | OPOS      |                         |
| HP           | QT457AA   | OPOS      |                         |
| Epson        |           | Sérsniðinn    | Tengt Epson prentara í gegnum netgátt |

#### <a name="line-display"></a>Línubirting

| Framleiðandi | Líkan    | Viðmót | Athugasemdir |
| ------------ | -------- | --------- | -------- |
| Epson        | DM-D110  | OPOS      |          |
| HP           | T-röð | OPOS      |          |

#### <a name="signature-capture"></a>Sækja undirskrift

| Framleiðandi | Líkan  | Viðmót | Athugasemdir |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>Vigt

| Framleiðandi | Tegund         | Viðmót | Athugasemdir |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OPOS      |          |

#### <a name="msr"></a>Kortalesari

| Framleiðandi | Tegund       | Viðmót | Athugasemdir |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="dedicated-iis-hardware-station"></a>Sérhæft IIS vélbúnaðarstöð

Eftirfarandi jaðartæki voru prófuð með því að nota sérhæfða (ekki samnýtta) IPC vélbúnaðarstöð sem ásamt Modern POS fyrir Windows og Cloud POS.

#### <a name="printer"></a>Prentari

| Framleiðandi | Líkan    | Viðmót | Athugasemdir                |
| ------------ | -------- | --------- | ----------------------- |
| Epson        | TM-T88V  | OPOS      |                         |
| Epson        | TM-T88IV | OPOS      |                         |
| HP           | H300     | OPOS      | Rafhlöðu USB             |
| Star         | TSP650II | Sérsnið    | Tengt gegnum netkerfi   |
| Star         | mPOP     | OPOS      | Tengt gegnum Bluetooth |
| Toshiba      | HSP100   | OPOS      |                         |
| Toshiba      | HSP150   | OPOS      |                         |

#### <a name="bar-code-scanner"></a>Strikamerkjaskanni

| Framleiðandi  | Líkan         | Viðmót | Athugasemdir |
| ------------- | ------------- | --------- | -------- |
| Datalogic     | Magellan 8400 | OPOS      |          |
| HP Samþætt | E1L07AA       | OPOS      |          |
| Tákn        | LS2208        | OPOS      |          |

#### <a name="payment-terminals-and-pin-pads"></a>Greiðslustöðvar og PIN-blokkar

Dynamics 365 Commerce veitir út-af-kassa lausn fyrir samþættingu við Adyen fyrir greiðsluþjónustu. The [Dynamics 365 greiðslutengi fyrir Adyen](dev-itpro/adyen-connector.md) notar tæki-agnostic [Adyen Payment Terminal API](https://www.adyen.com/blog/introducing-the-terminal-api) og getur haft samskipti við allar greiðslustöðvar sem þetta API styður. Fyrir heildarlista yfir studdar greiðslustöðvar, sjá [Adyen POS útstöðvar](https://www.adyen.com/pos-payments/terminals).

Þú getur líka notað aðrar greiðslumiðlar með Dynamics 365 Commerce með því að búa til sérsniðið tengi. Hægt er að nota hvaða greiðslustöð sem er studd af greiðsluveitunni með Dynamics 365 Commerce. Á sama hátt,Dynamics 365 Commerce gerir ráð fyrir samþættingarlíkönum greiðslutækja sem er studd af greiðsluveitanda, svo sem staðbundin IP, skýja-API eða bein tenging (til dæmis með USB) við POS. Fyrir frekari upplýsingar, sjá [Búðu til enda-til-enda greiðslusamþættingu fyrir greiðslustöð](dev-itpro/end-to-end-payment-extension.md).

#### <a name="cash-drawer"></a>Peningaskúffa

| Framleiðandi | Líkan     | Viðmót | Athugasemdir              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Sérsniðinn    | Tengt gegnum netkerfi |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |
| Epson        |           | Sérsniðinn    | Tengt Epson prentara í gegnum netgátt |

#### <a name="line-display"></a>Línubirting

| Framleiðandi  | Tegund   | Viðmót | Athugasemdir |
|---------------|---------|-----------|----------|
| HP Samþætt | G6U79AA | OPOS      |          |
| Epson         | M58DC   | OPOS      |          |

#### <a name="signature-capture"></a>Sækja undirskrift

| Framleiðandi | Tegund  | Viðmót | Athugasemdir |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>Vigt

| Framleiðandi | Tegund         | Viðmót | Athugasemdir |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OPOS      |          |

#### <a name="msr"></a>Kortalesari

| Framleiðandi | Tegund       | Viðmót | Athugasemdir |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="shared-iis-hardware-station"></a>Samnýtt IIS vélbúnaðarstöð

Eftirfarandi jaðartæki voru prófuð með því að nota samnýtta (ekki sérhæfða) IPC vélbúnaðarstöð ásamt Modern POS fyrir Windows og Cloud POS. 

> [!NOTE]
> Aðeins prentari, greiðslustöð og peningaskúffa eru studd.

#### <a name="printer"></a>Prentari

| Framleiðandi | Líkan    | Viðmót | Athugasemdir                |
| ------------ | -------- | --------- | ----------------------- |
| Epson        | TM-T88V  | OPOS      |                         |
| Epson        | TM-T88IV | OPOS      |                         |
| HP           | H300     | OPOS      | Rafhlöðu USB             |
| Star         | mPOP     | OPOS      | Tengt gegnum Bluetooth |
| Toshiba      | HSP100   | OPOS      |                         |
| Toshiba      | HSP150   | OPOS      |                         |

#### <a name="payment-terminal"></a>Greiðslustöð

Dynamics 365 Commerce veitir út-af-kassa lausn fyrir samþættingu við Adyen fyrir greiðsluþjónustu. The [Dynamics 365 greiðslutengi fyrir Adyen](dev-itpro/adyen-connector.md) notar tæki-agnostic [Adyen Payment Terminal API](https://www.adyen.com/blog/introducing-the-terminal-api) og getur haft samskipti við allar greiðslustöðvar sem þetta API styður. Fyrir heildarlista yfir studdar greiðslustöðvar, sjá [Adyen POS útstöðvar](https://www.adyen.com/pos-payments/terminals).

Þú getur líka notað aðrar greiðslumiðlar með Dynamics 365 Commerce með því að búa til sérsniðið tengi. Hægt er að nota hvaða greiðslustöð sem er studd af greiðsluveitunni með Dynamics 365 Commerce. Á sama hátt,Dynamics 365 Commerce gerir ráð fyrir samþættingarlíkönum greiðslutækja sem er studd af greiðsluveitanda, svo sem staðbundin IP, skýja-API eða bein tenging (til dæmis með USB) við POS. Fyrir frekari upplýsingar, sjá [Búðu til enda-til-enda greiðslusamþættingu fyrir greiðslustöð](dev-itpro/end-to-end-payment-extension.md).

#### <a name="cash-drawer"></a>Peningaskúffa

| Framleiðandi | Líkan     | Viðmót | Athugasemdir              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Sérsniðinn    | Tengt gegnum netkerfi |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |
| Epson        |           | Sérsniðinn    | Tengt Epson prentara í gegnum netgátt |


## <a name="troubleshooting"></a>Úrræðaleit
### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a>Modern POS getur fundið vélbúnaðarstöðina á lista sínum yfir val, en það getur ekki lokið við pörun

**Lausn:** Staðfesta eftirfarandi lista yfir hugsanlega bilunarpunkta:

-   Tölvan sem keyrir Modern POS treystir skírteini sem er notað er á tölvunni sem keyrir vélbúnaðarstöðina.
    -   Til að sannreyna þessa uppsetningu í vafra skaltu fara á eftirfarandi slóð: https://&lt;Computer Name&gt;:&lt;Port Number&gt;/HardwareStation/ping.
    -   Þessi SLÓÐ notar ping-boð til að staðfesta að hægt sé að fara í tölvuna og vafrinn gefur til kynna hvort skírteininu sé treyst. (Til dæmis í Internet Explorer, lástákn birtist á veffangastikunni. Þegar þú velur þetta tákn,Internet Explorer staðfestir hvort vottorðinu sé treyst. Hægt er að setja skírteinið upp á staðbundnu tölvunni með því að skoða upplýsingar um skírteinið sem birtast.)
-   Á tölvunni sem keyrir vélbúnaðarstöðina er tengið sem verður notað af vélbúnaðarstöðinni opinn í eldvegg.
-   Vélbúnaðarstöðin hefur rétt sett upp upplýsingar söluaðila með verkfærinu Setja upp upplýsingar um söluaðila sem keyrist við lok uppsetningarforrits vélbúnaðarstöðvar.

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a>Modern POS getur ekki fundið vélbúnaðarstöðina á lista sínum yfir val

**Lausn:** Annaðhvort eftirfarandi þáttum getur valdið vandamálið:

-   Vélbúnaðarstöðin hefur ekki verið sett upp rétt í höfuðstöðvunum. Fyrir frekari upplýsingar, sjá [Stilltu og settu upp Retail vélbúnaðarstöð](retail-hardware-station-configuration-installation.md#troubleshooting). 
-   Vinnslur hafa ekki verið keyrðar til að uppfæra skilgreiningu rásar. Í þessu tilfelli er vinnsla 1070 keyrð fyrir grunnstillingu rásar.

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a>Modern POS endurspegla ekki nýjum stillingum peningaskúffu

**Lausn:** Loka núverandi runu. Breytingar á peningaskúffunni eru ekki uppfærðar í Modern POS fyrr en núverandi rununni er lokað.

### <a name="modern-pos-is-reporting-an-issue-with-a-peripheral"></a>Modern POS tilkynnir vandamál með jaðarbúnaði

**Lausn:** Hér eru sumar dæmigerðar orsakir vandamálsins:

-   Gangið úr skugga um að aðrar grunnstillingarþjónustur tækirrekils séu lokað. Ef þessar þjónustur eru opnar, þær gætu komið í veg fyrir Modern POS eða vélbúnaðarstöð geri krafa á tækið.
-   Ef jaðarbúnaður er samnýttur með mörgum POS-tæki, ganga úr skugga um að sem hún tilheyrir eitt af eftirfarandi tegundum:
    -   Peningaskúffa
    -   Kvittanaprentari
    -   Greiðslustöð

    Ef jaðarbúnaðurinn tilheyrir ekki þessara tegunda, er vélbúnaðarstöðin ekki hönnuð til að virkja að jaðarbúnaðurinn sé samnýttar á milli margra POS-tæki.
-   Stundum geta tækisreklar valdið því að almennir stýrihlutir (CCOs) hætti að vinna rétt. Ef nýlega hefur verið sett upp tæki, en það er ekki virki rétt eða tekið er eftir öðrum vandamálum, er oft hægt að leysa þetta vandamál með því að enduruppsetja almenna stýrihluti. Til að sækja almenna stýrihluti skal fara á <http://monroecs.com/oposccos_current.htm>.
-   Ef þú gerir tíðar breytingar á jaðarbúnaði við prófun eða úrræðaleit, gæti þurft að endurstilla IIS í stað þess að bíða eftir að skyndiminni endurræsi sig. Það er gert með því að fylgja þessum skrefum:
    1.  Úr valmyndinni **Ræsa** skal rita **CMD**.
    2.  Í leitarniðurstöðum skaltu hægrismella **Skipunarlína**, og veldu síðan **Keyra sem stjórnandi**.
    3.  Í glugganum **skipunarkvaðning**, sláið inn **iisreset/Restart** og styðjið á færslulykilinn.
    4.  Endurræsa Modern POS eftir IIS hefur verið endurræst.
-   Þegar tíðar breytingar eru gerðar á jaðartæki, ef POS-biðlari er einnig ræstur og lokað oft, getur ferlið dllhost úr fyrri setu POS skarast við núgildandi lotu. Í þessu tilfelli tæki hugsanlega ekki hægt að nota fyrr en þú lokar hýsli safn kvik tengil (DLL) sem stjórnar fyrri setu. Til að loka DLL host, skal fylgja þessum skrefum:
    1.  Úr valmyndinni **Ræsa** skal rita **Verkstjórnandi**.
    2.  Veldu í leitarniðurstöðum **Verkefnastjóri**.
    3.  Í Task manager, á **Upplýsingar** flipanum, veldu dálkhausinn sem er merktur **Nafn** að raða töflunni í stafrófsröð eftir nafni.
    4.  Flettu niður þar til þú finnur dllhost.exe.
    5.  Veldu hvern DLL gestgjafa og veldu síðan **Loka verkefni**.
    6.  Endurræsa Modern POS eftir hýsir DLL hefur verið lokað.


## <a name="additional-resources"></a>Frekari upplýsingar

[Jaðarhermibúnaður fyrir Commerce](dev-itpro/retail-peripheral-simulator.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
