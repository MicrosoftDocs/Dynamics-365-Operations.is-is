---
title: Stjórna ferðum
description: Þetta efnisatriði útskýrir hvernig á að vinna með ferðir. Ferð stendur yfirleitt fyrir skip. Það fer hins vegar eftir þínum starfsháttum og venjum og getur hún staðið fyrir lánardrottin, innkaupapöntun eða eitthvað annað atriði sem passar fyrirtækinu þínu.
author: sherry-zheng
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMTableListPage, ITMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 50b6f306da1d32b1fd98da68bd997de1f1c23ffb
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570947"
---
# <a name="manage-voyages"></a>Stjórna ferðum

[!include [banner](../../includes/banner.md)]

Ferð stendur yfirleitt fyrir skip. Það fer hins vegar eftir þínum starfsháttum og venjum og getur hún staðið fyrir lánardrottin, innkaupapöntun eða eitthvað annað atriði sem passar fyrirtækinu þínu.

Á síðunni **Allar ferðir** er að finna upplýsingar um ferð, afhendingu og kostnað og upplýsingar um vörur, innkaupapantanir og flutningspantanir. Til að opna síðuna **Allar ferðir** skal fara í **Heildarkostnaður \> Ferðir \> Allar ferðir**. Þessi síða sýnir lista yfir allar núverandi ferðir. Hægt er að nota hnappana á aðgerðasvæðinu til að stofna, eyða eða vinna með ferðir. Veljið hvaða ferð sem er á listanum til að skoða upplýsingar um hana.

> [!NOTE]
> Flutningsgámar og fólíó eru tengd við ferð. Innkaupalínur eru tengdar við flutningsgám. Ef slökkt er á flutningsgámum og fólíó er einnig hægt að tengja þau beint við ferð. Auk þess er kostnaði sem færður er inn hér skipt niður á allar viðhengdar innkaupalínur.

## <a name="action-pane"></a>Aðgerðasvæði

Á aðgerðasvæðinu á síðunni **Ferðir** er að finna hnappa sem gerir þér kleift að vinna með valda ferð. Hver hnappur framkvæmir eina aðgerð. Aðgerðarsvæðið inniheldur líka flipa sem hver um sig býður upp á sett af svipuðum hnöppum. Nema þar sem annað er tekið fram, eru allir hnappar og flipar í boði í listayfirliti á síðunni **Allar ferðir** og í ítarlegu yfirliti fyrir eina valda ferð.

### <a name="buttons-that-appear-directly-on-the-action-pane"></a>Hnappar sem birtast á aðgerðasvæðinu

Eftirfarandi tafla lýsir hnöppunum sem eru í boði á aðgerðasvæðinu.

| Hnappur | lýsing |
|---|---|
| Nýjar | Stofna ferð. <!-- KFM: Link to scenario --> |
| Eyða | Eyðið núverandi ferð. Aðeins ferðum með stöðu ferðar sem *Staðfest* er hægt að eyða. Þegar ferð fer úr höfn og vinnur úr vörum í flutningi er ekki lengur hægt að eyða henni. |
| Ritill ferðar | Opnið síðuna **Ritill ferðar** þar sem hægt er að bæta við eða fjarlægja innkaupalína fyrir ferðina, búa til nýjan gám og breyta upplýsingum um sjálfa ferðina. |
| Kostnaður ferðar | Opnið síðuna **Kostnaður ferðar** þar sem hægt er að skoða og bæta ferðakostnaði við allar vörur í ferðinni. Þegar kostnaði ferðar er bætt handvirkt við ferðina er honum sjálfkrafa bætt við síðuna **Fyrirspurn um kostnað** og skipt niður á hverja vöru samkvæmt aðferðinni sem er tilgreind á síðunni **Kostnaður ferðar**. |

### <a name="buttons-on-the-voyage-tab"></a>Hnappar í ferðaflipanum

Eftirfarandi tafla lýsir hnöppunum sem eru í boði í flipanum **Ferð** á aðgerðasvæðinu. Þessi flipi er aðeins í boði þegar verið er að vinna í listayfirlitinu á síðunni **Allar ferðir**.

| Hnappur | lýsing |
|---|---|
| Gámur | Opnið síðu sem sýnir alla flutningsgáma sem tengjast valdri ferð. Það gæti verið einn eða fleiri gámar. |
| Fólíó | Opnið síðu sem sýnir öll fólíó sem tengjast valdri ferð. Það gæti verið eitt fólíó eða mörg fólíó. |

### <a name="buttons-on-the-manage-tab"></a>Hnappar á stjórnunarflipanum

Eftirfarandi tafla lýsir aðgerðunum sem eru í boði í flipanum **Stjórna** á aðgerðasvæðinu.

| Hnappur | lýsing |
|---|---|
| Skjöl móttekin | Uppfærið ferðina þannig að valkosturinn **Skjöl móttekin** sé stilltur á *Já*. Hægt er að nota þennan hnapp til að læsa vöru-og/eða innkaupalínu til að ekki sé hægt að uppfæra hana meira. |
| Í flutningi | Uppfærið reitinn **Staða ferðar** í stöðuna í flutningi sem er að finna á síðunni **[Færibreytur heildarkostnaðar](landed-cost-parameters.md)**. Engar frekari reglur eru í þessu ferli. Einnig er hægt að uppfæra verð sjálfkrafa í stöðuna í flutningi samkvæmt stillingum í [Stjórnstöð rakningar](delivery-information-setup.md).
| Tilbúið fyrir kostnaðarútreikning | Uppfærið reitinn **Staða ferðar** í stöðuna tilbúin fyrir kostnaðarútreikning sem er að finna á síðunni **[Færibreytur heildarkostnaðar](landed-cost-parameters.md)**. Hægt er að kostnaðarreikna ferð þegar unnið hefur verið úr öllum reikningum (bæði birgðareikningar og ferðakostnaðarreikningar) og vörurnar hafa verið mótteknar. Ef áætlaður kostnaður sem tengist ferð hefur ekki verið kostnaðarreiknaður kemur upp villa þegar reynt er að vinna úr kostnaðarútreikningi ferðar. |
| Kostnaðarútreikningur | Hreinsið öll frávik á kostnaðarútreikningi þegar reikningur er til staðar fyrir allar innkaupapantanir og kostnað ferðar. Þegar þessi hnappur er valinn birtist svarglugginn **Uppfærsla ferðar – kostnaðarútreikningur**. Þar er hægt að velja að bóka á venjulegu fjárhagsdagsetningunni eða tilgreina bókunardagsetningu og síðan keyra aðgerðina. Hægt er að keyra aðgerðina aftur eins oft og þörf krefur. Einnig er hægt að nota svargluggann **Uppfærsla ferðar – kostnaðarútreikningur** til að setja upp áætlun til að keyra aðgerðina sem reglubundið verk (runuvinnslu). Við mælum með því að keyra aðgerðina með reglulegu millibili með því að setja hana upp sem runuvinnslu. |
| Bóka innhreyfingalista | Bókið innhreyfingaskjal fyrir allar innkaupapöntunarlínur í ferðinni. Ef ferðir margra fyrirtækja eru notaðar opnast nýr svargluggi fyrir bókun innhreyfingalista fyrir hvert fyrirtæki og verður að vinna úr í hverjum lögaðila fyrir sig. |
| Bóka innhreyfingarskjal afurða | Bókið innhreyfingarskjal afurðar fyrir allar innkaupapöntunarlínur í ferðinni. Ferli innhreyfingarskjals afurðar fyrir innkaupapöntunarlínurnar sem tengjast ferð verða aðeins notaðar ef vörurnar fara **ekki** í gegnum ferli fyrir vörur í flutningi. Ef vörurnar fara í gegnum ferli fyrir vörur í flutningi kemur upp villa þegar reynt er að bóka innhreyfingarskjalið fyrir innkaupapöntunarlínu. Ef ferðir margra fyrirtækja eru notaðar opnast nýr svargluggi fyrir bókun fylgiseðils fyrir hvert fyrirtæki. |
| Bóka reikning | Bókið reikning fyrir allar innkaupapöntunarlínur í ferðinni. Ef vörurnar í ferðinni fara í gegnum vöruflutningsferlið verða innkaupapöntunarlínurnar reikningsfærðar áður en móttökuferlið klárast. Þegar upprunalega innkaupapöntunin er reikningsfærð verða pantanir fyrir vörur í flutningi sem tengjast upprunalegum innkaupapöntunarlínum stofnaðar. Vöruhúsið getur þá móttekið þessar pantanir. Ef sendir margra fyrirtækja eru notaðar opnast nýr svargluggi fyrir bókun reiknings fyrir hvert fyrirtæki. |
| Senda flutningspöntun | Bókið ferð flutningspöntunar fyrir alla flutningspöntunarlínur ferðarinnar. Þegar þessi hnappur er valinn verða aðeins flutningspantanir í boði til uppfærslu. |
| Taka á móti flutningspöntun | Bókið móttöku flutningspöntunar fyrir allar flutningspöntunarlínur ferðarinnar. |
| Taka á móti vörum í flutningi | Takið á móti öllum pöntunarlínum sem eru í flutningi í ferðinni. Þessi hnappur er einn af þremur valmöguleikunum sem eru í boði til að taka á móti vörum í flutningi í ferð. (Hinir tveir valmöguleikarnir eru hnappurinn **Stofna komubók** sem er lýst seinna í þessari töflu og farsímaforriti Vöruhúsakerfis.) Þessi valmöguleiki er einfaldasti valkosturinn og mun afgreiða vörur í flutningi úr flutningsvöruhúsinu og inn í vöruhús áfangastaðar. Ef óskað er eftir frekari stjórn á ferlinu skal nota komubókina eða fartækið til að afgreiða móttöku á vörum. |
| Leita að sjálfvirkum kostnaði | Finna allan kostnað ferðar sem á við. Ef þessi kostnaður hefur þegar verið fundinn eða uppfærður birtast eftirfarandi skilaboð: „Óreikningsfærðar kostnaðarlínur eru til staðar. Á að skrifa yfir þetta? Allur kostnaður sem var ekki tengdur við ferðina þegar hún var búin til verður fundinn. Ekki verður skrifað yfir kostnað ferðar sem er hengdur við ferð og hefur verið reikningsfærður. |
| Stofna komubók | <p>Opnið svargluggann **Stofna komubók** þar sem hægt er að stofna komubók sem tilgreinir staðsetningu. Svarglugginn býður upp á eftirfarandi valkosti:</p><ul><li>**Stofna úr vörum í flutningi** eða **Stofna úr flutningspöntun** – Merkið fyrir þennan valkost breytist eftir því hvort verið sé að nota vöruflutningsferlið. Stillið hann á *Já* til að opna síðu komubókar sem gerir þér kleift að afgreiða venjulega komubók fyrir vörur í flutningi sem tengjast ferðinni. Ef varan hefur þegar verið móttekin í vöruhúsi áfangastaðar verður henni ekki bætt við línur komubókarinnar.</li><li>**Frumstilla magn** – Stillið þennan valkost á *Já* til að frumstilla magnið sem verður móttekið samkvæmt vörumagninu sem er tilgreint í línu ferðarinnar. Ef lína ferðarinnar hefur verið móttekin að hluta til verður þetta magn eftirstandandi magnið. Mælt er með að þessi valkostur sé stilltur á *Já*.</li><li>**Stofna úr pöntunarlínum** – Stillið þennan valkost á *Já* til að nota gildið úr pöntunarlínunum.</li></ul><p>Þessi hnappur er einn af þremur valmöguleikunum sem eru í boði til að taka á móti vörum í ferð. (Aðrir valmöguleikar eru hnappurinn **Taka á móti vörum í flutningi** sem var lýst áður í þessari töflu og farsímaforriti vöruhúsakerfis.)</p> |
| Uppsafnaður kostnaður | Hægt er að safna upp kostnaði þar sem kostnaðargerð er með fjárhagslykilinn tilgreindan fyrir debet. Þessi hnappur er vanalega notaður þegar birgðir eru í flutningi eða þegar vörur hafa verið mótteknar og reikningsfærðar. |
| Samanlagður kostnaður | Flytjið kostnað frá stigi flutningsgáms til stigs ferðar. Hægt er að nota þennan hnapp í aðstæðum samnýttrar þjónustu/sendingar þar sem margar einingar deila flutningsgámi eða kassasvæði. Ferðin er til dæmis með 40 feta flutningsgám og 20 feta flutningsgám og skiptingin er gerð eftir rúmmáli. Í þessu tilviki gæti verið sektað fyrir vörur/einingar sem deila eða nota plássið í 20 feta flutningsgámnum. Til að dreifa kostnaðinum á sanngjarnan hátt gætu sum fyrirtæki viljað flytja kostnaðinn yfir á ferðina og deila honum samkvæmt skiptingaraðferð á stigi ferðar. |
| Breyta sniðmáti ferðar | Opnið svarglugga þar sem hægt er að breyta sniðmáti ferðarinnar. Þegar sniðmáti hefur verið breytt verður ferðakostnaðinum eytt. Þess vegna gæti verið sniðugt að velja **Finna sjálfvirkan kostnað** (sjá lýsinguna fyrr í þessari töflu) eða bæta kostnaði handvirkt við aftur. |

### <a name="buttons-on-the-general-tab"></a>Hnappar á flipanum Almennt

Eftirfarandi tafla lýsir hnöppunum sem eru í boði í flipanum **Almennt** á aðgerðasvæðinu.

| Hnappur | lýsing |
|---|---|
| Komulisti | Opnið lista yfir innhreyfingarskjöl afurða fyrir allar innkaupapöntunarlínur í ferðinni. Ef ferðir margra fyrirtækja eru notaðar opnast nýr listi innhreyfingarskjala fyrir hvert fyrirtæki. Ef ekki hefur verið unnið úr neinum listum yfir innhreyfingarskjöl afurða verður þessi hnappur ekki í boði. |
| Innhreyfingarskjal afurða | Opna færslu fyrir innhreyfingarskjal afurðar fyrir innkaupapöntunarlínurnar sem tengjast ferðinni ef sú færsla er notuð. Ef engin innhreyfingarskjöl afurða hafa verið bókuð verður þessi hnappur ekki í boði. Ferli innhreyfingarskjals afurða verður ekki notað ef verið er að nota vöruflutningsferlið. |
| Vörumóttaka | Opnið komubók vörunnar ef hún er notuð. |
| Rakning | Opnið síðuna **Rakning á innleið** þar sem hægt er að uppfæra væntanlegan afhendingardag vara í flutningsgámi og ferð og uppfærið í kjölfarið væntanlega afhendingardaga innkaupapöntunarlína. |
| Fyrirspurn um kostnað | <p>Opnið síðuna **Fyrirspurn um kostnað** sem sýnir allan kostnað ferðar.</p><p>Veljið **Yfirlit** á aðgerðasvæðinu til að stilla yfirlitið. Hægt er að skoða öll stigin ásamt vörunni og kóða kostnaðargerðar.</p><p>Aðeins kóðar kostnaðargerðar tengjast beint birgðafærslum birtast á síðunni **Fyrirspurn um kostnað**. Með því að fjarlægja kóða kostnaðargerðar er hægt að breyta síðunni með því að flokka saman kostnað. Þessi eiginleiki getur komið sér vel ef þú ert að nota stærðir og liti.</p><p>Síðan **Fyrirspurn um kostnað** sýnir aðeins kóða kostnaðargerðar þar sem reiturinn **Debet** er stilltur á *Vara*.</p> |
| Vöruflutningspantanir | Opnið síðuna **Vöruflutningspantanir** sem sýnir færslur fyrir vörur í flutningi aðeins fyrir valda ferð. |

## <a name="lines-view"></a>Línuyfirlit

Til að opna yfirlitið **Línur** skal opna ferð og síða velja flipann **Línur** uppi hægra megin í síðuhaus ferðar.

### <a name="information-on-the-voyage-header-fasttab"></a>Upplýsingar í flýtiflipanum síðuhaus ferðar

Flýtiflipinn **Síðuhaus ferðar** í yfirlitinu **Línur** fyrir ferð inniheldur grunnupplýsingar sem lýsa ferðinni. Margir reitirnir sem birtast í þessum flýtiflipa birtast einnig í yfirlitinu **Síðuhaus** eins og lýst er síðar í þessu efnisatriði.

### <a name="information-on-the-voyage-lines-fasttab"></a>Upplýsingar í flýtiflipanum línur ferðar

Flýtiflipinn **Línur ferðar** í yfirlitinu **Línur** fyrir ferð tengist upplýsingum ferðar og kostnaðarupplýsingum sem eiga við á stigi ferðar. Hér er hægt að fara yfir flutningsgáma, fólíó og vörur sem eru hengd við ferðina. Verð og vörumagn ferðarinnar er einnig sýnt. Hægt er að skoða hvaða flutningsgám sem er eða fólíó sem er gefið upp með því að velja viðeigandi tengil.

### <a name="information-on-the-line-details-fasttab"></a>Upplýsingar í flýtiflipa línuupplýsinga

Flýtiflipinn **Upplýsingar um línu** í yfirlitinu **Línur** fyrir ferð veitir frekari upplýsingar um línuna sem er valin í flýtiflipanum **Línur ferðar**. Takið eftir að þessi flýtiflipi inniheldur upplýsingar um stöðuna sem hver lína heldur í gámnum og uppgefið magn hennar.

## <a name="header-view"></a>Hausyfirlit

Til að opna yfirlitið **Haus** skal opna ferð og síða velja flipann **Haus** uppi hægra megin í síðuhaus ferðar.

### <a name="settings-on-the-general-fasttab"></a>Stillingar á flýtiflipanum Almennt

Eftirfarandi tafla lýsir reitunum sem eru í boði í flýtiflipanum **Almennt** í yfirlitinu **Haus** fyrir ferð.

| Svæði | lýsing |
|---|---|
| Ferð | Færið inn númer ferðar eða flugs. |
| Bókunartilvísun | Ef farmsendandinn gefur upp tilvísunarnúmer til að auðkenna ferðina (þ.e. innri tilvísun farmsendanda) skal færa það inn. |
| Skip | Færa inn eða velja skip. Ef skipið er ekki gefið upp sem gildi er hægt að færa inn auðkenni skipsins sem frjálsan texta. Í því tilfelli er aðaltaflan ekki uppfærð þannig að hægt er að velja auðkenni skipsins seinna í þessum reit. |
| Ytra kenni ferðar | Færið inn auglýst auðkenni ferðarinnar (t.d. flugnúmerið). |
| Aðalflugfarmbréf/farmbréf | Færið inn númer aðalflugfarmbréfs eða farmbréfs. Hægt er að tilgreina þetta gildi þegar sent er flugleiðis. |
| Grunnflugfarmbréf/farmbréf | Færið inn grunnflugfarmbréf eða farmbréf fyrir flutningsgáminn. |
| Leiga | Veljið þennan gátreit til að gefa til kynna að gámurinn sé leigugámur sem þarf að skila. |
| lýsing | Færið inn lýsingu á ferð til að auðvelda auðkenningu hennar. |
| Staða ferðar | Staða ferðarinnar. Gildin fela í sér *Stofnað*, *Í flutningi*, *Skjöl móttekin* og *Kostnaðarútreikningur*. Þessi reitur er ekki reiknaður samkvæmt reglu. Hann er aðeins uppfærður í gegnum bókunaraðgerðina. Gildið fyrir *Kostnaðarútreikning* gefur til kynna að reikningur fyrir birgðir og allan ferðakostnað hafi verið móttekinn. Ferð getur ekki náð stöðunni *Kostnaðarútreikningur* nema reikningur sé móttekinn. |
| Staða innkaupapöntunar | Hæsta staðan sem hefur verið náð á meðal allra innkaupapantana sem tengjast ferðinni. |
| Skjöl móttekin | Gildi sem segir til um hvort fyrirtækið hefur móttekið öll skjöl sem tengjast ferðinni. Til að breyta gildinu skal velja **Skjöl móttekin** í flokknum **Uppfærsla ferðar** í flipanum **Stjórna** á aðgerðasvæðinu. |
| Flutningsfyrirtæki | Veljið flutningsfyrirtækið fyrir þessa ferð. Þennan reit er hægt að nota til að ákveða sjálfvirkan kostnað. |
| Nafn | Heiti fyrirtækisins sem er valið í reitnum **Flutningsfyrirtæki**. |
| Mæling | Þessi reitur gerir kleift að tilgreina mælingu í sjálfvirkum kostnaði. Mælingar eru oft notaðar af fyrirtækjum sem vita ekki rúmmál eða þyngd á hverri vöru fyrir sig, en þurfa nákvæmari skiptingu en upphæðin eða magnið gefur til kynna. Flutningsmiðlarinn gefur upp þyngd eða rúmmálsmælieiningu og hægt er að setja hana inn á annaðhvort stigi vöru eða innkaupapöntunar. Hægt er að uppfæra hana sjálfkrafa ef færibreytan er valin eða færa hana inn handvirkt. |
| Mælieining | Mælieiningin sem gildir um númerið í reitnum **Mæling**. |
| Fjöldi bretta | Tilgreinið fjölda bretta í línu ferðarinnar. Þessi reitur er sjálfkrafa uppfærður ef valkosturinn **Uppfæra sjálfkrafa fjölda kassa** er stilltur á *Já* í flipanum **Almennt** á síðunni **Færibreytur heildarkostnaðar**. |

### <a name="settings-on-the-delivery-fasttab"></a>Stillingar á flýtiflipanum Afhending

Eftirfarandi tafla lýsir reitunum sem eru í boði í flýtiflipanum **Afhending** í yfirlitinu **Haus** fyrir ferð.

| Svæði | lýsing |
|---|---|
| Tími og dagsetning stofnunar | Dagsetning og tími þegar færsla ferðar var stofnuð. |
| Dagsetning útflutningsverksmiðju | Þessi reitur velur fyrstu dagsetningu útflutningsverksmiðju úr innkaupapöntunum sem tengjast ferðinni. Dagsetning útflutningsverksmiðju er tiltæk í haus innkaupapöntunar og er uppfærð með því að nota eiginleika rakningarstýringar. |
| Sendingardagsetning | Áætluð dagsetning þegar flugvél eða skip yfirgefur upprunastaðinn. |
| Brottfarartími | Brottfarardagsetningin er vanalega dagsetningin þegar flugvél eða skip leggur af stað. Sendingardagsetning og brottfarardagsetning þurfa ekki að vera eins. Reiturinn **Brottfarardagur** er aðeins ætlaður til upplýsinga. Hann er ekki notaður til að áætla væntanlegan afhendingardag. Eiginleiki rakningarstýringar er notaður til að áætla væntanlegan afhendingardag og hægt er að setja upp þennan reit þannig að fyllt sé sjálfkrafa í hann af eiginleika rakningarstýringar. |
| Dagsetning inn í verslun | Þessi reitur velur fyrstu dagsetningu þegar vörur úr innkaupapöntunum sem eru tengdar við ferðina verða tiltækar fyrir sölu. |
| Áætluð afhendingardagsetning | Áætlaður afhendingardagur er venjulega dagsetningin þegar vörurnar eiga að koma í vöruhúsið. Þetta svæði er eingöngu ætlað til upplýsinga. Hann er ekki notaður fyrir aðaláætlanagerð fyrir vörur. Væntanleg afhendingardagsetning á innkaupapöntunarlínunni er notuð fyrir aðaláætlanagerð fyrir vörur í ferð og er uppfærð með því að nota eiginleika rakningarstýringar. Hægt er að setja upp þennan reit þannig að eiginleiki rakningarstýringar fylli í hann. |
| Endanlegur afhendingardagur | Fyrsti afhendingardagurinn samkvæmt vörunum sem eru tengdar við ferðina. |
| Áætlaður komutími til afhendingarhafnar | Færið inn dagsetninguna þegar búist er við því að ferðin berist til afhendingarhafnar samkvæmt upplýsingunum sem voru gefnar upp af flutningsaðilanum. |
| Upprunaleg skjöl móttekin | Færið inn dagsetninguna þegar upprunaleg skjöl voru móttekin. |
| Ráðlegging miðlara | Færið inn dagsetninguna þegar miðlari var spurður álits. |
| Upprunalegt farmbréf sent | Færið inn dagsetninguna þegar upprunalegt farmbréf var sent. |
| Vörur losaðar | Færið inn dagsetninguna þegar vörurnar voru losaðar úr tolli. |
| Fundur viðskiptavinar | Færið inn fundardagsetningu viðskiptavinar, sem er dagsetningin þegar búist er við að viðskiptavinurinn eigni sér vörurnar. |
| Afhent í vöruhúsi | Færið inn dagsetninguna þegar vörurnar voru afhentar í vöruhúsinu. |
| Staðfestingardagsetning | Færið inn staðfestingardagsetninguna. |
| Leiðbeiningar um afhendingu | Færið inn dagsetninguna þegar leiðbeiningar um afhendingu voru mótteknar. |
| Afhendingarmáti | Þessi reitur veitir upplýsingar um aðferðina sem var notuð til að afhenda ferðina og kostnaðarval fyrir sjálfvirkan kostnað sem tengist þeirri afhendingaraðferð. |
| Frá höfn | Afhendingarhöfnin þar sem ferðin hefst. |
| Til hafnar | Afhendingarhöfnin þar sem ferðinni lýkur. Flutningagámarnir geta verið með mismunandi hafnir vegna þess að skipið gæti haft viðdvöl í mörgum höfnum. Með því að staðfesta „til“ höfnina á stigi flutningagáms eru gefnar upp nákvæmar upplýsingar um höfn fyrir hvern flutningsgám í ferð. Sjálfvirkur kostnaður sem tengist farminum er ákveðinn út frá samsetningu af gerð flutningsgámsins, „til“ hafnar og „frá“ hafnar. |
| Staðbundinn miðlari | Þetta svæði er eingöngu ætlað til upplýsinga. Staðbundinn miðlara á að vera hægt að velja úr töflu lánardrottins. |
| Dagsetning staðbundins flutnings | Dagsetningin sem staðbundinn flutningur er bókaður fyrir. Þessi reitur getur hjálpað vöruhúsinu að gera áætlanagerð. |
| Staðbundinn flutningstími | Tímahólfið sem staðbundinn flutningur er bókaður fyrir. Þessi reitur getur hjálpað vöruhúsinu að gera áætlanagerð. |
| Sniðmát ferðar | Ferðasniðmátið sem er tilgreint fyrir ferðina. Sniðmát ferðarinnar er notað til að færa inn „til“ höfn og „frá“ höfn flutningagámsins og ferðarinnar. Þessi gildi hjálpa á móti að greina sjálfvirka kostnaðinn sem tengist ferðinni. |

### <a name="settings-on-the-other-fasttab"></a>Stillingar á flýtiflipanum Annað

Eftirfarandi tafla lýsir reitunum sem eru í boði í flýtiflipanum **Annað** í yfirlitinum **Haus** fyrir ferð.

| Svæði | lýsing |
|---|---|
| Athugasemdir | Færið inn viðbótarupplýsingar sem tengjast ferðinni. |
| Dagsetning mats | Veljið fyrstu dagsetningu útflutningsverksmiðju fyrir innkaupapantanirnar sem tengjast ferðinni. |
| Ferð í biðstöðu | Hægt er að nota þetta til að gefa til kynna hvort sendingin eða ferðin sé þegar farin. Því er aðeins ætlað að veita upplýsingar.  |
| Flutningagámar endurnefndir | Fyrir ferðir sem eru með fleiri en einn gám, fjöldi gáma sem hafa ekki enn verið mótteknir. |

## <a name="voyage-update-periodic-tasks"></a>Reglubundin verk ferðauppfærslu

Einingin **Heildarkostnaður** inniheldur ýmis ferðatengd reglubundin verk sem geta magnuppfært ýmsa þætti ferða. Til að keyra eða áætla þessi reglubundnu verk skal fara í **Heildarkostnaður \> Reglubundin verk \> Uppfærslur ferðar** og síðan velja eina af eftirfarandi verkgerðum:

- **Skjöl móttekin** – Þetta verk gerir þér kleift að stilla **Skjöl móttekin** á *Já* fyrir margar ferðir samtímis. Notið stillingarnar **Sía** til að skilgreina safn ferða sem á að uppfæra.
- **Í flutningi** – Þetta verk gerir þér kleift að stilla reitinn **Ferðastaða** á stöðu fyrir vörur í flutningi sem er komið á á síðunni **[Færibreytur heildarkostnaðar](landed-cost-parameters.md)** fyrir margar ferðir samtímis. Notið stillingarnar **Sía** til að skilgreina safn ferða sem á að uppfæra.
- **Tilbúið fyrir kostnaðarútreikning** – Þetta verk gerir þér kleift að stilla reitinn **Ferðastaða** á stöðuna tilbúið fyrir kostnaðarútreikning sem er komið á á síðunni **[Færibreytur heildarkostnaðar](landed-cost-parameters.md)** fyrir margar ferðir samtímis. Yfirleitt er þetta verk sett upp til að keyra reglubundna áætlun.
- **Kostnaðarútreikningur** – Þetta verk gerir þér kleift að stilla reitinn **Ferðastaða** á stöðu kostnaðarútreiknings sem er sett á á síðunni **[Færibreytur heildarkostnaðar](landed-cost-parameters.md)** fyrir margar ferðir samtímis, svo lengi sem gerður hafi verið kostnaðarútreikningur á þeim en ekki enn verið uppfærðar í ferðinni. Yfirleitt er þetta verk sett upp til að keyra reglubundna áætlun.
