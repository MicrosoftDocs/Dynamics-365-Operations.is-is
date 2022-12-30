---
title: Heildarkostnaður í samanburði við flutningsstjórnun
description: 'Microsoft Dynamics 365 Supply Chain Management býður upp á tvær mismunandi einingar fyrir vinnu með flutningi: Flutningsstjórnun (TMS) og Heildarkostnað. Þessi grein tekur saman þá virkni sem einingarnar tvær eiga sameiginlegt og helsta muninn á þeim.'
author: Weijiesa
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 40489ff8d8683d19a5f726546cc4c43cc3e7a05d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905922"
---
# <a name="landed-cost-vs-transportation-management"></a>Heildarkostnaður í samanburði við flutningsstjórnun

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management býður upp á tvær mismunandi einingar fyrir vinnu með flutningi: **Flutningsstjórnun** (TMS) og **Heildarkostnað**. Þessi grein tekur saman þá virkni sem einingarnar tvær eiga sameiginlegt og helsta muninn á þeim. Hægt er að nota þessar upplýsingar til að ákveða hvor einingin hentar þínum viðskiptaháttum. Þú gætir fundið fyrir því að einhverjir viðskiptahættir virka betur með flutningsstjórnun á meðan aðrir virka best með heildarkostnaði. Því næst er hægt að nota eina einingu eða að sameina einingarnar tværm, allt eftir þörfum fyrirtækisins.

Þessi grein er ekki ítarleg yfirferð yfir alla eiginleika í hvorri einingu. Þess í stað varpar það ljósi á tiltæka virkni sem tengist flutningi á vörum frá lánardrottni til vöruhúss fyrirtækis þíns þar sem hægt er að nota þær.

## <a name="terminology-reference-data-and-reporting-differences"></a>Hugtök, tilvísunargögn og skýrslumismunur

### <a name="terminology-comparison"></a>Samanburður á hugtakanotkun

Flutningsstjórnun og heildarkostnaður nota mismunandi hugtök fyrir svipaðar aðgerðir. Eftirfarandi tafla tekur saman þessi hugtök og notkun þeirra í einingunum tveimur.

| TMS-öhugtök | Hugtakið heildarkostnaður | Athugasemdir |
|----------|------------------|-------|
| **Sækja**<p>*Farmur* er safn sendinga sem eru fluttar samtímis í sömu flutningseiningunni (t.d. trukk eða skipi). Farmar geta verið annaðhvort á innleið eða útleið.</p> | **Ferð**<p>Yfirleitt er *ferð* eitt skip sem ferðast eftir einni *leið*. Ferð getur aðeins innihaldið *flutningsgáma* og hún getur einnig falið í sér pantanir á innleið frá mismunandi lögaðilum fyrirtækisins. Ferðir geta aðeins verið á innleið.</p> | Flutningsstjórnun notar einnig hugtakið *ferðanúmer* sem vísar í upplýsingareit þar sem hægt er að færa inn kennimerki. Engin virkni tengist hins vegar reit flutningsstjórnunar og hann er ótengdur *ferðahugtakinu* í heildarkostnaði. |
| **Leið**<p>*Leið* er raunslóð flutnings frá uppruna til áfangastaðar.</p> | **Ferðalag**<p>*Ferð* er raunslóð flutnings frá uppruna til áfangastaðar. Úthluta verður hverri ferð á ferðaleið.</p> | |
| **Leiðarhlutar**<p>Leið getur haft marga *leiðarhluta* þar sem hver táknar skref ferðarinnar. Leið getur innihaldið marga flutningsaðila eða þjónustur sem hver um sig er álitin leiðarhluti.</p> | **Leggir**<p>Hver ferðleið getur haft marga *leggi* þar sem hver þeirra táknar hluta leiðarinnar. Leggur getur verið hluti af flutningi, tollavinnu eða öðrum verkþætti.</p> | |
| **Gámar**<p>*Gámur* getur verið hvers kyns pakkning eða umbúðir sem flutningsstjórnun notar.</p> | **Gámar**<p>*Flutningsgámur* er einfaldlega efnislegur flutningsgámur eins og þekkist á gámaskipum.</p> | |
| **Grunnvörukóðar**<p>Í flutningsstjórnun (og öðrum stöðum Supply Chain Management) tákna *vörukóðar* vörugerðir. Þeir geta haft áhrif á gjaldskrár, meðhöndlun hættulegra efna og svo framvegis.</p> | **Grunnvörukóðar**<p>Í heildarkostnaði eru *vörukóðar* notaðir á stigi lögaðilans. Þær eru aðallega notaðar til skýrslugerðar.</p> | Heildarkostnaður getur einnig notað vörukóða sem eru notaðir fyrir flutningstjórnun og aðra staði í Supply Chain Management. Hins vegar eru vörukóðar heildarkostnaðar aðeins notaðir af heildarkostnaði. |

### <a name="some-reference-data-isnt-shared"></a>Sum tilvísunargögn eru ekki samnýtt

Flutningstjórnun og heildarkostnaður deila ekki tilvísunargögnum fyrir einingar á borð við kostnaðaruppsetningu, ferðaleiðir og leggi. Ef báðar einingar eru notaðar verður að endurgera tilvísunargögnin sem ekki hefur verið deilt aftur.

### <a name="intercompany-reports-dont-work-with-goods-in-transit"></a><a name="intercompany-reports"></a>Samstæðuskýrslur virka ekki með vörur í flutningi

Eftirfarandi skýrslur virka ekki saman með eiginleika fyrir vörur í flutningi sem heildarkostnaður býður upp á:

- [Heildarskýrsla vara í flutning innan samstæðu](/dynamicsax-2012/appuser-itpro/intercompany-goods-in-transit-totals-report-intercompanygoodsintransittotals)
- [Heildarskýrsla vara í flutning innan samstæðu](/dynamicsax-2012/appuser-itpro/intercompany-goods-in-transit-totals-report-intercompanygoodsintransittotals)

Þessar skýrslur gera ráð fyrir að vörur séu settar í flutning um leið og gefinn er út fylgiseðill sölu og þær færðar í birgðir úr flutningi við móttöku. Vörur í flutningi eru hins vegar ekki unnar á þennan hátt. Þannig að, ef vörur í flutningi og samstæðueiginleikar er notað saman, verða niðurstöður fyrir báðar þessar skýrslur rangar.

## <a name="using-the-two-modules-together"></a>Einingarnar tvær notaðar saman

Hægt er að nota flutningsstjórnun fyrir aðgerðir bæði á innleið og útleið. Þótt heildarkostnaður bjóði upp á mest af sömu grunnvirkninni og flutningsstjórnun fyrir aðgerðir á innleið, þá bætast samt við einhver virkni. Þess vegna er sniðugt að velta fyrir sér hvort nota skuli flutningsstjórnun fyrir aðgerðir á útleið og heildarkostnað fyrir aðgerðir á innleið.

Almennt er ekki mælt með því að nota báðar einingarnar saman fyrir aðgerðir á innleið. Nota ætti eininguna sem uppfyllir best kröfurnar. Ef einingarnar tvær eru notaðar saman má ekki deila upprunaskjölum á milli þeirra. Til dæmis skal ekki nota sömu innkaupapöntunina fyrir bæði farm í flutningsstjórnun og ferð í heildarkostnaði. Sérstaklega þarf að tryggja að kerfið sé ekki sett upp til að búa sjálfkrafa til farma á innleið. Ef vörur úr innkaupapöntunum eru teknar með í ferð er ekki hægt að afgreiða þær sem hluta af farmi.

## <a name="goods-in-transit"></a>Vörur í flutningi

Einn af aðaleiginleikum heildarkostnaðar er möguleiki hans á að afgreiða vörur í flutningi. Vinnsla á vörum í flutningi gerir þér kleift að eigna þér sendar vörur fjárhagslega áður en efnislega er tekið á móti þeim í vöruhúsi á áfangastað. Vinnsla á vörum í flutningi er oft nauðsynleg í alþjóðlegum viðskiptum.

### <a name="tms-goods-in-transit-features"></a>Eiginleikar flutningsstjórnunar fyrir vörur í flutningi

Sem stendur styður flutningsstjórnun ekki vinnslu á vörum í flutningi.

### <a name="landed-cost-goods-in-transit-features"></a>Eiginleikar heildarkostnaðar fyrir vörur í flutningi

Vinnsla á vörum í flutningi er aðaleiginleiki heildarkostnaðar og býður upp á eftirfarandi virkni:

- **Flutningsvöruhús** – Flutningsvöruhús getur tengst sérhverju vöruhúsi í Supply Chain Management. Vörur eru fluttar í flutningsvöruhús eftir að upprunaleg innkaupapöntun er reikningsfærð. Vörur sem eru efnislega teknar frá þar verða ekki tiltækar fyrir notkun fyrr en þær hafa verið mótteknar í efnislega vöruhúsinu. Þess vegna er hægt að eigna sér vörur fjárhagslega með því að reikningsfæra innkaupapöntunina.
- **Fjárhagslykill fyrir vörur í flutningi** – Heildarkostnaður bætir ákveðnum fjárhagsbókunarlykli við bókunarreglu innkaupapöntunar til að sjá um vinnslu á vörum í flutningi. Þessi fjárhagslykill fyrir vörur í flutningi virkar sem lykill af gerðinni „reikningsfærðar vörur ekki mótteknar“. Þegar upprunalega innkaupapöntunin er reikningsfærð og flutningspöntun er stofnuð, er beinn kostnaður innkaupapöntunar bókaðar á fjárhagslykil fyrir vörur í flutningi þangað til vörurnar eru mótteknar á lokastaðsetningunni.
- **Uppfærslur rakningastjórnunar** – Flutningspantanir styðja virkni rakningastjórnunar í heildarkostnaði. Rakningastjórnun gerir þér kleift að uppfæra væntanlega komudagsetningu á vörum á meðan þær eru í flutningi. Rakningastjórnun uppfærir síðan ferðina og tengdar innkaupapöntunarlínur. Væntanlegur afhendingardagur er þá aðgengilegur fyrir aðaláætlanagerð og vörustjórnun.
- **Ræsing á yfir-/undirfærslum** – Ef frávik á sér stað milli væntanlegra vara í ferðalínu og raunverulegra vara sem eru mótteknar í vöruhúsinu mun heildarkostnaður leysa úr því með því að stofna yfir- og/eða undirfærslur. Síðan er hægt að stjórna þessum færslum samkvæmt því hvernig á að vinna úr þeim, annaðhvort með innkaupapöntun eða hreyfingabók. Yfir- og undirfærslur bjóða upp á tengil aftur í ferðina, upprunalega innkaupapöntun og nýju hreyfingabókina eða innkaupapöntunina fyrir frávikið.
- **Flutningspantanir** – Heildarkostnaður kynnir til sögunnar nýtt upprunaskjal sem er þekkt sem *flutningspöntun*. Flutningspöntun gerir þér kleift að reikningsfæra upprunalega innkaupapöntun til að slá fjárhagslegu eignarhaldi á vörurnar. Þegar innkaupapöntunin er reikningsfærð er nýja upprunaskjalið stofnað fyrir hverja innkaupapöntunarlínu sem er með samsetningu birgðavídda. Vörur eru síðan fluttar efnislega í flutningsvöruhúsið þar sem þær eru efnislega teknar frá gagnvart flutningspöntuninni og ekki er hægt að nota þær fyrr en flutningspantanir hafa verið mótteknar.

## <a name="miscellaneous-charges-and-shipment-costs"></a>Ýmis gjöld og sendingarkostnaður

Einn af mikilvægustu þáttum sendingar og sendingastjórnunar fyrir vörur er skráning sameiginlegs kostnaðar sem tengist sendingum. Þessi sameiginlegi kostnaður er ekki beinn birgðakostnaður sem tengist innkaupapöntun og sendingu eða ferð. Þess í stað er hann viðbótarkostnaður sem kemur til vegna eðli vöruflutninga frá lánardrottni til fyrirtækisins. Þessi kostnaður getur falið í sér flutningskostnað sem tengist sendingu á vörum frá einni staðsetningu til annarrar eða tollum sem tengjast innflutningi á vörum frá erlendum lánardrottni.

Heildarkostnaður sér um þennan kostnað með því að búa til nýja gerð af kostnaðarskipulagi sem er þekkt sem *sjálfvirkur kostnaður*. Flutningsstjórnun sér um þennan kostnað með því að nota virkni ýmissa gjalda.

### <a name="tms-charge-and-cost-features"></a>TMS-gjöld og kostnaðareiginleikar

Flutningsstjórnun notar ýmis gjöld til að halda utan um viðbótarkostnað vegna farma sem er úthlutað til tengdra upprunaskjalslína. Hægt er að stilla þessi ýmis gjöld á annaðhvort stigi innkaupapöntunarlínu eða innkaupapöntunarhauss.

Í flutningsstjórnun er hægt að skipta ýmsum gjöldum, eða deila þeim niður, eftir þyngd, rúmmáli eða magni birgðanna. Hægt er að skipta gjöldum eftir farmi eða aukagjöldum. Frekari þróun verður nauðsynleg til að nota aðrar skiptingaraðgerðir í TMS.

### <a name="landed-cost-charge-and-cost-features"></a>Gjald heildarkostnaðar og kostnaðareiginleikar

Heildarkostnaður býður upp á safn kostnaðaraðgerða sem sjá um viðbótarkostnað sem tengist sendingu á vörum. Þessi kostnaður er þekktur sem sjálfvirkur kostnaður og er hann notaður þegar verið er að reikningsfæra upphaflega sendinguna með því að nota áætlaða kostnaðarupphæð. Hverri kostnaðargerð er stjórnað í eigin bókun. Þegar raunverulegir reikningar fyrir sameiginlegan kostnað eru bókaðir er áætlaður kostnaður uppfærður sjálfkrafa til að endurspegla raunverulegan kostnað.

Þar að auki er hægt að reikningsfæra sameiginlegan kostnað sem tengist sendingu á vörum þegar farið er frá upprunastað eða hvenær sem er eftir að vörurnar hafa verið mótteknar. Þessi möguleiki býður upp á aukinn sveigjanleika fyrir notkun á vörum.

Eftirfarandi listi lýsir nokkrum hugtökum fyrir gjöld og kostnaðareiginleika í Heildarkostnaði:

- **Kostnaðarsvæði** – Kostnaði og gjöldum er hægt að úthluta á mismunandi stig eða *kostnaðarsvæði* í ferð. Hægt er að nota kostnaðinn á stigi ferðar og sundurliða hann eftir vöru í ferðinni. Auk þess er hægt að nota kostnað á stigi gáms, innkaupapöntunar, vöru eða flutningspöntunar. Hægt er að stýra öllum kostnaði vegna gjalda fyrir hvert svæði fyrir sig og sundurliða hann í kostnað á hverja vöru.
- **Skiptingaraðferð** – Nokkrar skiptingaraðferðir eru í boði í heildarkostnaði. Hægt er að skipta gjöldum eftir magni, upphæð í dollurum, virði, þyngd, rúmmáli, mælingu eða rúmmálsmælingu sem skilgreind er af notanda.
- **Stjórnun milli-/frávikslykla** – Gjöld eru sett upp sem eigin gerð kostnaðarkóða í heildarkostnaði. Hver gerð kostnaðarkóða gerir þér kleift að skilgreina millilykil fyrir gjöld áætlaðs kostnaðar og einnig frávikslykla uppsöfnunar og innkaupaverðs fyrir frávik í áætluðum kostnaði í samanburði við raunverulegan kostnað. Þegar áætlaður kostnaður er upphaflega bókaður er kreditfærsla á millilyklinum. Þegar raunverulegir reikningar eru bókaðir er raunverulegur kostnaður bókaður og áætlaður kostnaður er debetfærður af millilyklinum.

## <a name="matching-freight-bills-and-invoices"></a>Jafna farmbréf og reikninga

### <a name="tms-bill-and-invoice-matching-features"></a>Farmbréf og reikningsjöfnunareiginleiki

TMS getur jafnað farmbréf sem innihalda áætlaðan kostnað og reikninga með raunverulegum kostnaði farmsins. Hægt er að fá reikninga rafrænt eða á pappír. Samsvörunarfrávik á milli áætlaðs kostnaðar og raunkostnaðar hefur ekki áhrif á birgðamat.

Frekari upplýsingar eru í [Afstemming farms í flutningsstjórnun](../transportation/reconcile-freight-transportation-management.md).

### <a name="landed-cost-bill-and-invoice-matching-features"></a>Reikningur heildarkostnaðar og reikningsjöfnunareiginleikar

Heildarkostnaður getur jafnað farmbréf við gjöld áætlaðs kostnaðar og getur reikningsfært áætlaðan kostnað fyrir gjöldum raunverulegs kostnaðar. Þegar reikningsfærsla er gerð eru farmgjöldin í reikningabók og áætlaður kostnaður er hreinsaður út af millilyklinum. Þar að auki eru gjöld raunverulegs kostnaðar bókuð á móti kostnaði seldra vara fyrir vöruna ásamt frávikunum á milli áætlaðra gjalda og raunverulegra gjalda. Þessi hegðun leyfir sveigjanleika í reikningsfærsluferlinu.

## <a name="tracking"></a>Rakning

Mikilvægur eiginleiki bæði TMS og heildarkostnaðar er möguleikinn til að rekja vörur og finna út hvar þær eru staddar í ferðinni frá upprunastað til vöruhúss á áfangastað. Rakning gerir þér kleift að fylgjast með og uppfæra hvar vörurnar eru staðsettar og hvenær búist er við því að þær berist í vöruhúsið til notkunar. Ásamt stöðu á vörunum á ferð þeirra býður heildarkostnaður upp á væntanlegar og raunverulegar dagsetningar fyrir hvert skref ferðarinnar.

### <a name="tms-tracking-features"></a>TMS-rakningareiginleikar

TMS býður upp á takmarkaða eiginleika til að rekja farm á innleið. Það sýnir dagsetningar og gerir kleift að nota samþættingu til að finna nákvæma staðsetningu (til dæmis á síðunni **Flutningsstaða**).

Fyrir hvern leiðarhluta er hægt að færa inn áætlaðar tímasetningar og komutíma.

### <a name="landed-cost-tracking-features"></a>Rakningareiginleikar heildarkostnaðar

Heildarkostnaður getur boðið upp á rakningarstýringu fyrir hverja ferð frá upphafsstað til áfangastaðar. Rakningarstýringar stillir stöðu ferðar. Staðan segir til um hvort staða ferðar sé í siglingu, í tollinum eða í afhendingu á staðnum og á leiðinni í vöruhús á áfangastaðnum. Hægt er að stilla stöðuna á stigi innkaupapöntunarlínu, gáms og hauss fyrir ferð. Þannig hefurðu betri stjórn.

Auk þess er staðfest væntanleg dagsetning sem byggir á tilgreindum afhendingartíma sem tengist hverju skrefi ferðar. Staðfestum og áætluðum afhendingardagsetningum er bætt við innkaupapöntunarlínuna og flutningspantanirnar og er hægt að nota fyrir aðaláætlanagerð og vörustjórnun. Til viðbótar við væntanlegu dagsetningarnar er hægt að uppfæra raunverulegu dagsetningarnar. Næstu skref í ferð verða síðan uppfærð í samræmi við þetta.

## <a name="multi-leg-journeys"></a>Ferð með mörgum leggjum

Hugmynd ferðarinnar auðkenna hvar vörurnar eru í ferlinu og stýrir stöðu varanna á meðan þær eru í flutningi. Vörur geta farið í gegnum nokkra leggi ferðar og hægt er að tengja ýmsan kostnað við tiltekinn legg. Sem dæmi má nefna farmkostnað vegna skipasiglingar og staðbundinn flutningskostnað vegna flutnings á vörum frá höfn og til áfangastaðar.

### <a name="tms-multi-leg-journey-features"></a>TMS-eiginleikar ferðar með mörgum leggjum

Í TMS er hægt að brjóta niður leiðir í leiðarhluti til að sýna ferðir með marga leggi. TMS getur úthlutað stundargengi og aukagjöldum á einstaka leiðarhluta.

Frekari upplýsingar eru í [Áætlanagerð farms flutningsleiðir með mörgum stöðvun](../transportation/plan-freight-transportation-routes-multiple-stops.md).

### <a name="landed-cost-multi-leg-journey-features"></a>Eiginleikar heildarkostnaðar fyrir ferðir með mörgum leggjum

Heildarkostnaður býður upp á ramma fyrir flutning á vörum frá upphafspunkti og til áfangastaðar í gegnum röð af leggjum sem eru viðkoma eða skref á leiðinni. Leggirnir eru sameinaðir til að búa til ferðasniðmát sem skilgreina hvernig vörur fara frá lánardrottni til fyrirtækisins.

Í hverjum ferðalegg er hægt að skilgreina enn frekar stöðu hverrar innkaupapöntunarlínu og afhendingartíma sem tengist henni. Samanlagður afhendingartími fyrir alla leggina er notaður til að finna út áætlaðan afhendingardag. Hins vegar er nauðsynlegt að nota vinnslu fyrir vörur í flutningi til þess að ferðir með marga leggi eigi við. Flutningi á vörum í ferð er stjórnað í töflu sem tilheyrir heildarkostnaði.

## <a name="receiving-by-container"></a>Móttaka eftir gámi

Mikilvægt getur verið að stjórna því hvernig vörum er skipt og þær geymdar á skipi. Á skipi er hægt að geyma vörur í einum eða mörgum gámum. Við móttöku á vörum er tekið við þeim í gámum og mismunandi gámar í ferð gætu verið mótteknir á mismunandi tímum eða á mismunandi dögum.

Bæði TMS og heildarkostnaður bjóða upp á virkni fyrir umsjón með móttöku á vörum í gámi. TMS notar farmhugtakið til að stjórna vörum, innkaupapöntunum og flutningspöntunum sem tengjast gámasendingu. TMS styður móttöku sem byggir á pakkaskipulagi sem er móttekið í gegnum ítarlega sendingartilkynningu (ASN). Heildarkostnaður notar hugtak flutningsgáma til að vinna úr innkaupapöntunum og stjórna sameiginlegum kostnaði sem tengist gámi á skipi.

### <a name="tms-receiving-by-container-features"></a>TMS móttaka eftir eiginleikum gáma

TMS styður ASN á innleið, öll afbrigði móttöku í gegnum farsímaforrit vöruhúsakerfis og allar móttökuaðferðir í gegnum biðlara Supply Chain Management.

### <a name="landed-cost-receiving-by-container-features"></a>Eiginleikar heildarkostnaðar fyrir gámamóttöku

Til að styðja við móttöku eftir gámi stofnar heildarkostnaður færslur flutningsgáma og tengir innkaupapantanir við tiltekinn flutningsgám með því að nota gámakenni þess. Hægt er að nota sameiginlegan kostnað fyrir þennan flutningsgám og sundurliða hann þannig að hann tengist viðeigandi innkaupapöntunum.

Hægt er að taka á móti gámum í heildarkostnaði í gegnum nýja gerð móttöku sem er þekkt sem *móttaka á vörum í flutningi* í gegnum komubækur eða í gegnum móttöku í fartæki. Þegar komubækur eru notaðar er hægt að frumstilla magnið úr flutningspöntuninni eða upprunalegri innkaupapöntunarlínu í gámnum. Heildarkostnaður býður upp á tvær vinnugerðir fyrir móttöku í gegnum farsímaforrit vöruhúsakerfis.

Heildarkostnaður býður ekki upp á ASN fyrir rafræna vörumóttöku. Auk þess styður hann ekki flæði farsímaforrit vöruhúsakerfis sem vinna úr móttöku farms, númeraplatna eða blandaðra númeraplatna.

## <a name="rate-shopping-by-vendor"></a>Leit að bestu töxtum eftir lánardrottni

Leit að bestu töxtum gerir fyrirtæki kleift að velja lánardrottin flutnings samkvæmt lægsta verði, fljótlegustu leiðinni eða samsetningu beggja.

### <a name="tms-rate-shopping-features"></a>TMS-eiginleikar fyrir leit að bestu töxtum

TMS gerir þér kleift að finna lausnir á lánardrottnum og leiðum fyrir pantanir á innleið og útleið. Til dæmis er hægt að auðkenna hraðast leið eða ódýrast taxta fyrir sendingu.

TMS býður upp á ítarlega leit að bestu töxtum og fínstillingu farms í gegnum vinnusvæði fyrir taxta leiðar, sveigjanlega taxtamöguleika í gegnum taxtavél, API-taxtavél fyrir samþættingu við ytri aðila og stuðning fyrir rúmmálsþyngdir.

Frekari upplýsingar eru í [Flutningsstjórnunarvélar](../transportation/transportation-management-engines.md).

### <a name="landed-cost-rate-shopping-features"></a>Eiginleikar heildarkostnaðar fyrir leit að bestu töxtum

Heildarkostnaður býður aðeins upp á takmarkaðan stuðning fyrir leit að bestu töxtum eftir lánardrottni. Þó að hægt sé að færa inn gildi fyrir flutningsmiðlara mun heildarkostnaður ekki bera þau saman yfir marga lánardrottna.

## <a name="driver-check-incheck-out-with-appointment-scheduling"></a>Innskráning bílstjóra/útskráningu með tímabókun

Eiginleikar inn-/útskráningar bílstjóra gera kerfinu kleift að fylgjast með komum og koma í veg fyrir troðning á hleðsluhöfnum.

### <a name="tms-driver-check-incheck-out-features"></a>TMS-eiginleikar inn-/útskráningar

TMS gerir þér kleift að skrá *erindi*. Erindi stendur fyrir viðburði sem eiga sér stað á höfn vegna móttöku innkaupapöntunar, sendingu sölupöntunar eða vinnslu á farmi á innleið eða útleið á tiltekinni dagsetningu og tilteknum tíma. Erindi tryggja að hafnir eru tilbúnar fyrir hleðslu og afhleðslu á vörum og þau hjálpa til að koma í veg fyrir kringumstæður þar sem margir flutningsaðilar koma á staðinn á sama tíma.

Kerfið styður við að heimila ökumönnum að skrá sig inn á tilteknar hleðsludyr.

### <a name="landed-cost-driver-check-incheck-out-features"></a>Eiginleikar heildarkostnaðar fyrir inn-/útskráningu bílstjóra

Heildarkostnaður getur geymt áætlanir fyrir dagsetningu og tíma þegar gámur verður afhentur.

## <a name="transfer-orders-and-additional-costs"></a>Flutningspantanir og aukakostnaður

Oft verða fyrirtæki að geta flutt vörur á milli vöruhúsa. Þegar þessi gerð flutnings á sér stað er kostnaður tengdur við hann og gott er að gera sér grein fyrir honum. Í heildarkostnaði er hægt að bæta flutningspöntunum við ferð eða skip til að fylgjast með flutningi á vörum frá einu vöruhúsi eða svæði til annars, áætla afhendingartíma og væntanlegan afhendingardag og bæta sameiginlegum kostnaði við flutning á vörum.

### <a name="tms-transfer-order-cost-features"></a>TMS-eiginleikar fyrir kostnað flutningspöntunar

TMS styður stofnun farmgjalda sem tengjast flutningum. Þótt hægt sé að skoða þessi gjöld úr flutningspöntuninni er heildarkostnaði ekki bætt við kostnað vörunnar. Afstemming farms er studd í gegnum farmbréf sem byggir á þessum gjöldum. Þetta farmbréf er síðan jafnað á móti farmreikningi lánardrottins.

### <a name="landed-cost-transfer-order-cost-features"></a>Eiginleikar heildarkostnaðar fyrir kostnað flutningspöntunar

Heildarkostnaður gerir þér kleift að bæta flutningspöntunum við skip eða ferð. Á þennan hátt er hægt að bæta sendingarkostnaði við ferðina sem birgðajafnanir við móttöku flutningspöntunar. Hægt er að reikningsfæra sameiginlega kostnaðinn fyrir raunverulegum kostnaði og fylgjast með honum varðandi ferð til að uppfæra kostnað seldra vara. Þótt flutningspantanir noti ekki vinnslu á vörum í flutningi í stöðluðu útgáfunni, er hægt að bæta henni við ferðir. Heildarkostnaði er bætt við samtals kostnað fyrir hverja vöru.