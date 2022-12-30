---
title: Sjálfvirkt framboð með „framleiða eftir pöntun“
description: Í þessari grein er lýst hvernig á að setja upp og nota ýmsar viðbætur sem bætt er við með því að nota sjálfvirknieiginleikann Framleiða eftir pöntun.
author: t-benebo
ms.date: 07/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-07-27
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: d376c2f4d8514a4e6122e2e94455d57a39d2babf
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740195"
---
# <a name="make-to-order-supply-automation"></a>Sjálfvirkt framboð með „framleiða eftir pöntun“

[!include [banner](../includes/banner.md)]

Eiginleikinn *Sjálfvirkni á framboði vegna framleiðslu eftir pöntun* bætir við nokkrum endurbótum til Microsoft Dynamics 365 Supply Chain Management. Þessar viðbætur gera þér kleift að framkvæma eftirfarandi verk:

- Skoða afkastagetu tilfanga á notandaskilgreindu tímabili og gera því kleift að meta afkastagetu til lengri tíma.
- Auka sveigjanleika með því að stjórna vikmörkum tafar (neikvæðum dögum) fyrir hverja aðaláætlun.
- Hafðu vörur tiltækar fyrir pantanir á síðustu stundu og hámarkaðu nýtingu núverandi framboðs með þarfarakningu nýjasta framboðs við eftirspurn í stað þess að nota fyrsta mögulega framboðið.
- Hafðu úthlutun íhluta sveigjanlega fyrir framleiðslupantanir eftir staðfestingu, þannig að kerfið geti hámarkað eftirspurn eftir breytingum á síðustu stundu. Með öðrum orðum, takmarka merkingu við eitt stig.
- Stjórna uppfyllingarreglu fyrir hverja sölupöntun. Sjálfgefnar stillingar eru fengnar úr uppsetningu viðskiptavinar.
- Bæta upplýsingaflæði innan samstæðu. Innkaupapantanir eru uppfærðar þannig að þær innihalda reiti fyrir afhendingarmáta, afhendingarskilmála og ytri vörunúmer. Þessi breyting tryggir að ítarlegar upplýsingar um eftirspurn geti flætt til veitufyrirtækisins.

Þessi grein lýsir því hvernig á að setja upp og nota hverja endurbót.

## <a name="turn-on-the-make-to-order-supply-automation-feature"></a>Kveikja á eiginleikanum Sjálfvirkni á framboði vegna framleiðslu eftir pöntun

Áður en hægt er að nota eiginleikann sem lýst er í þessari grein verður að kveikja á honum fyrir kerfið þitt. Stjórnendur geta notað vinnusvæði [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) þar sem eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Aðaláætlanagerð*
- **Heiti eiginleika:** *Sjálfvirkt framboð með framleiða eftir pöntun*

## <a name="set-the-number-of-days-to-show-on-capacity-load-page"></a>Setja inn hversu marga daga á að sýna á síðu fyrir Álag

Á síðunni **Álag** er hægt að skoða tiltæka getu tilfangs. Eiginleikinn *Sjálfvirkt framboð með Framleiða eftir pöntun* bætir síðuna **Afkastageta** með því að bæta við reitnum **Fjöldi daga**. Hægt er að nota þennan reit til að takmarka fjölda daga sem hnitanetið **Yfirlit** sýnir. Gildið sem þú stillir er vistað í minni. Þess vegna, ef þú ferð af síðunni og kemur svo aftur sýnir hnitanetið **Skoða** enn sýna þann dagafjölda sem þú tilgreindir síðast.

Fylgdu eftirfarandi skrefum til að opna síðuna **Afkastageta** svo hægt sé að fara yfir tiltæka getu fyrir einstök tilföng.

1. Fara á **Fyrirtækisstjórnun \> Tilföng \> Tilföng**.
1. Velja tilfang til að skoða.
1. Á aðgerðasvæðinu, í flipanum **Tilfang**, í flokknum **Yfirlit**, skal velja **Afkastageta**.
1. Notaðu síuna **Dagafjöldi** til að takmarka fjölda daga sem hnitanetið **Yfirlit** sýnir.

Fylgdu eftirfarandi skrefum til að opna síðuna **Afkastageta** svo hægt sé að fara yfir tiltæka getu fyrir einstaka tilfangaflokka.

1. Fara á **Fyrirtækisstjórnun \> Tilföng \> Tilfangaflokkar**.
1. Velja tilfangaflokk til að skoða.
1. Á aðgerðasvæðinu, í flipanum **Tilfangaflokkur**, í flokknum **Yfirlit**, skal velja **Afkastageta**.
1. Notaðu síuna **Dagafjöldi** til að takmarka fjölda daga sem hnitanetið **Yfirlit** sýnir.

## <a name="apply-a-single-level-of-marking-when-you-firm-planned-orders"></a>Nota eitt stig merkingar þegar áætlaðar pantanir eru staðfestar

*Merking* er notuð til að tengja framboð og eftirspurn. Slíkt er svipað og *þarfarakning*, sem gefur til kynna hvernig aðaláætlanagerð gerir ráð fyrir því að uppfylla eftirspurn. Hins vegar er merking varanlegri en þarfarakning. Eiginleikinn *Framleiðsla eftir pöntun* bætir við möguleikanum á að takmarka merkingar á birgðum við eitt stig þegar áætlaðar pantanir eru staðfestar. Það bætir eftirfarandi nýjum valkostum við reitinn **Uppfæra merkingu** í svarglugganum **Staðfesting** þegar þú staðfestir áætlaða pöntun:

- *Staðlað eitt stig* – Merking fyrir eitt stig notuð. Merking fyrir eitt stig merkir aðeins aðalvöruna, ekki íhluti uppskrift þess (BOM). Því er hægt að halda íhlutum til úthlutunar fyrir framleiðslupantanir breytilegum eftir staðfestingu. Merking fyrir eitt stig gerir kerfinu kleift að fínstilla fyrir breytingar á eftirspurn á síðustu stundu. Í *hefðbundinni* eins stigs merkingu eru þarfapantanir merktar gegn fullnaðarpöntunum þeirra en fullnaðarpantanir eru ekki merktar ef þær hafa eftirstandandi magn.
- *Eitt stig framlengt* – Merking fyrir eitt stig notuð. Í *framlengdri* eins stigs merkingu eru þarfapantanir merktar gegn fullnaðarpöntunum þeirra, og fullnaðarpantanir eru alltaf merktar, burtséð frá því hvort eitthvert magn er eftir.

Þessir valkostir eru einnig tiltækir í reitnum **Uppfæra merkingu** á flipanum **Hefðbundin uppfærsla** á síðunni **Færibreytur áætlanagerðar** þar sem skilgreint er sjálfgefið val í svarglugganum **Staðfesting**.

Frekari upplýsingar eru í [Birgðamerking](planning-optimization/marking.md).

## <a name="set-delay-tolerance-negative-days-at-the-master-plan-level"></a>Stilla vikmörk tafar (neikvæðir dagar) á aðaláætlunarstigi

Eiginleikinn *Sjálfvirkt framboð með framleiða eftir pöntun* bætir við getu til að stilla vikmörk seinkunar (neikvæða daga) á aðaláætlunarstigi. Stillingarnar eru einnig tiltækar á stigum vöruþekju og þekjuflokka. Ef neikvæðum dögum er úthlutað á fleiri en einu stigi beitir kerfið eftirfarandi stigveldi til að ákveða hvaða stillingu á að nota:

- Ef neikvæðir dagar eru skilgreindir á síðunni **Aðaláætlanir**, hnekkir sú stilling allar aðrar neikvæðar dagastillingar þegar áætlunin er keyrð.
- Ef neikvæðir dagar eru stilltir á síðunni **Vöruþekja**, hnekkir sú stilling þekjuflokksstillingunni.
- Neikvæðir dagar sem eru skilgreindir á síðunni **Þekjuflokkar** eiga aðeins við ef neikvæðir dagar hafa ekki verið skilgreindir fyrir viðeigandi vöru eða aðaláætlun.

Til að stilla neikvæða daga fyrir aðaláætlun skal fylgja þessum skrefum.

1. Farið í **Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Aðaláætlanir**.
1. Veljið viðeigandi aðaláætlun á listasvæði eða stofnið nýja.
1. Í flýtiflipanum **Tímamörk í dögum** skal stilla valkostinn **Neikvæður dagafjöldi** á *Já*.
1. Í næsta reitinn, sláðu inn fjölda neikvæðra daga til að leyfa.

Frekari upplýsingar um hvernig á að nota neikvæða daga eru í [Vikmörk tafar (neikvæður dagafjöldi)](planning-optimization/delay-tolerance.md).

## <a name="control-the-pegging-sequence-used-during-master-planning"></a>Stjórna röð þarfarakningar sem er notuð við aðaláætlanagerð

Í aðalskipulagi er notast *röð þarfarakningar* til að ákvarða hvaða framboð mun anna eftirspurn. Eiginleikinn *Sjálfvirkt framboð með framleiða eftir pöntun* bætir við nýjum möguleika á að **Nota nýjustu mögulegu birgðir** sem gefur þér meiri stjórn á röð þarfarakningar. Nýi valkosturinn gerir þér kleift að halda vörum tiltækum fyrir pantanir á síðustu stundu og hámarka nýtingu núverandi framboðs með því að þarfarekja nýjasta mögulega framboðið við eftirspurn í stað þess að nota fyrsta mögulega framboðið.

Hægt er að stilla þarfarakningarröð á stigi aðaláætlunar, vöruþekju eða þekjuflokks. Ef röð þarfarakningar er sett upp á fleiri en einu stigi beitir kerfið eftirfarandi stigveldi til að ákveða hvaða stillingu á að nota:

- Ef röð þarfarakningar er sett upp á síðu **Aðaláætlanir**, hnekkir sú stilling allar aðrar stillingar þarfarakningar þegar áætlunin er keyrð.
- Ef röð þarfarakningar er sett upp á **á síðu atriðaumfjöllunar**, hunsar sú stilling stillingar umfjöllunarhóps.
- Röð þarfarakningar sem er sett upp á síðu **Þekjuflokka** á aðeins við ef stillingar raðar þarfarakningar hafa ekki verið stilltar fyrir viðeigandi vöru eða aðaláætlun.

Til að setja upp þarfarakningu á þekjuflokksstiginu skal fylgja þessum skrefum.

1. Fara skal í **Aðaláætlanagerð \> Uppsetning \> Þekja \> þekjuflokkar**.
1. Veljið viðeigandi flokkur á listasvæði eða stofnið nýjan.
1. Á flýtiflipanum **Almennt** í hlutanum **Röð þarfarakningar** skal nota reitina **Nota birgðir** og **Nota nýjustu birgðir** til að stilla röð þarfarakningar. Taflan síðar í þessum kafla sýnir hvernig þessar stillingar eru samsettar til að skilgreina röð þarfarakningar.

Til að setja upp þarfarakningu á vöruþekjustigi skal fylgja þessum skrefum.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Veldu vöru á hnitanetinu eða stofnaðu nýja.
1. Á aðgerðasvæðinu, í flipanum **Áætlun** skal velja **Vöruþekja**.
1. Á síðunni **Vöruþekja** finna línur þar sem hægt er að skilgreina reglur um þekju sem gilda um vöruna hjá hverjum vöruhúsi fyrir sig. Veldu línu sem er þegar á hnitanetinu eða stofnaðu nýja.
1. Á flipanum **Almennt** skal velja gátreitinn **Hnekkja röð þarfarakningar**.
1. Notaðu reitina **Nota lagerbirgðir** og **Nota nýjustu birgðir** til að stilla röð þarfarakningar. Taflan síðar í þessum kafla sýnir hvernig þessar stillingar eru samsettar til að skilgreina röð þarfarakningar.

Til að setja upp þarfarakningu á aðaláætlunarstiginu skal fylgja þessum skrefum.

1. Farið í **Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Aðaláætlanir**.
1. Veljið viðeigandi aðaláætlun á listasvæði eða stofnið nýja.
1. Á flýtiflipanum **Almennt** skal stilla valkostinn **Hnekkja röð þarfarakningar** á *Já*.
1. Notaðu reitina **Nota lagerbirgðir** og **Nota nýjustu birgðir** til að stilla röð þarfarakningar. Taflan síðar í þessum kafla sýnir hvernig þessar stillingar eru samsettar til að skilgreina röð þarfarakningar.

Eftirfarandi tafla sýnir hvernig nýjustu stillingar **Nota lagerbirgðir** og **Nota nýjustu birgðir** eru samsettar til að setja upp röð þarfarakningar.

| | Nota nýjasta framboðið = Já | Nota nýjasta framboðið = Nei |
|---|---|---|
| **Nota lagerbirgðir** = *Á undan öllum birgðum* | <ol><li>Á lager</li><li>Núverandi framboð sem getur uppfyllt eftirspurnardagsetninguna</li><li>Núverandi framboð sem getur ekki uppfyllt dagsetningu eftirspurnar en er samt innan neikvæðra daga</li><li>Stofna nýtt framboð (áætluð pöntun)</li></ol> | <ol><li>Á lager</li><li>Núverandi framboð sem getur uppfyllt eftirspurnardagsetninguna</li><li>Núverandi framboð sem getur ekki uppfyllt dagsetningu eftirspurnar en er samt innan neikvæðra daga</li><li>Stofna nýtt framboð (áætluð pöntun)</li></ol> |
| **Nota lagerbirgðir** = *Á eftir öllu framboði* | <ol><li>Núverandi framboð sem getur uppfyllt eftirspurnardagsetninguna</li><li>Á lager</li><li>Núverandi framboð sem getur ekki uppfyllt dagsetningu eftirspurnar en er samt innan neikvæðra daga</li><li>Stofna nýtt framboð (áætluð pöntun)</li></ol> | <ol><li>Núverandi framboð sem getur uppfyllt eftirspurnardagsetninguna</li><li>Núverandi framboð sem getur ekki uppfyllt dagsetningu eftirspurnar en er samt innan neikvæðra daga</li><li>Á lager</li><li>Stofna nýtt framboð (áætluð pöntun)</li></ol> |

## <a name="review-and-set-the-fulfillment-policy-that-applies-to-each-sales-order"></a>Farðu yfir og settu þér uppfyllingarstefnu sem gildir um hverja sölupöntun

Uppfyllingarreglan stjórnar prósentu af samtals pöntunarverðinu eða magninu sem þarf að taka efnislega frá áður en má losa sölupöntun í vöruhúsið. Hægt er að setja upp altæka reglu um uppfyllingu og hnekkja hana fyrir tiltekna viðskiptavini eins og þú krefst. Eiginleikinn *Sjálfvirkt framboð með framleiða eftir pöntun* bætir við möguleikanum á að skoða hvaða sjálfgefna regla á við um hvaða pöntun sem er og nota hnekkingu fyrir tiltekna pöntun eftir þörfum.

- Til að setja upp altæka sjálfgefna uppfyllingarstefnu fyrir sölupantanir ferðu í **Viðskiptakröfur \> Uppsetning \> Færibreytur viðskiptakrafna**. Síðan á flipanum **Vöruhúsakerfi** skaltu setja reitinn **Uppfyllingarregla sölupöntunar** í heiti reglunnar sem þú vilt nota. 
- Til að setja upp sértæka uppfyllingarreglu fyrir sölupantanir viðskiptavina ferðu í **Viðskiptakröfur \> Viðskiptavinir \> Allir viðskiptavinir**. Síðan á flipanum **Vöruhús** stillirðu reitinn **Uppfyllingarregla** í heiti reglunnar sem þú vilt nota.

Til að skoða sjálfgefna reglu sem á við um hvaða pöntun sem er og beita hnekkingu fyrir sérstaka pöntun skal fylgja þessum skrefum.

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Opna skal sölupöntun sem á að skoða eða breyta.
1. Veldu yfirlitið **Haus**.
1. Á flýtiflipanum **Vöruhús** skal yfirfara og breyta eftirfarandi reitum eftir þörfum:

    - **Uppfyllingarregla pöntunar** – Veldu uppfyllingarregluna sem á að nota fyrir valda pöntun. Sjálfgefnu reglunni verður hnekkt. Til að nota sjálfgefna uppfyllingarreglu sem er sýnd í reitnum **Sjálfgefin uppfyllingarregla** skal skilja þennan reit eftir autt.
    - **Sjálfgefin uppfyllingarregla** – Þessi reitur sýnir sjálfgefna uppfyllingarreglu sem á við ef reiturinn **Uppfyllingarregla pöntunar** er auður. Þetta svæði er aðeins til lestrar. Ef það er autt merki það að engin regla um uppfyllingu viðskiptavinar eða altæk sjálfgefin regla er skilgreind.

    Ef bæði reiturinn fyrir **Uppfyllingarreglu pöntunar** og reiturinn fyrir **Sjálfgefin uppfyllingarregla** er auður gildir engin uppfyllingarregla. Aðrar takmarkanir gætu þó verið til staðar og þú gætir farið fram á að bókunum eða öðrum skilyrðum sé fullnægt áður en hægt er að ganga frá sölupöntuninni.

## <a name="set-the-delivery-mode-and-terms-on-individual-purchase-order-lines"></a>Stilla afhendingarmáta og skilmála í einstökum innkaupapöntunarlínum

Allar innkaupapantanir innihalda **Afhendingarskilmálar** og stillingar **Afhendingarmáta** pöntunarhausnum. Eiginleikinn *Sjálfvirkni á framboði vegna framleiðslu eftir pöntun* bætir þessum stillingum við hverja pöntunarlínu. Því er hægt að skilgreina hnekkingar **Afhendingarskilmála** og/eða **Afhendingarmáta** fyrir allar eða allar pöntunarlínur eins og krafist er. Fyrir línur þar sem engin hnekking er skilgreind er gildið úr hausnum notað. Þú getur skilgreint hvort breyting á gildi annars eða beggja þessara reita á pöntunarhausnum eigi einnig að uppfæra allar línur.

Til að tilgreina hvernig línustillingar eigi að breytast ef notandi breytir gildinu **Afhendingarskilmálar** og/eða **Afhendingarmáti** á pöntunarhaus fylgdu eftirfarandi skrefum.

1. Opnið **Innkaup og aðföng \> Uppsetning \> Færibreytur innkaupa og aðfanga**.
1. Í flipanum **Almennt** á flýtiflipanum **Sjálfgefin gildi og færibreytur**, skal velja tengilinn **Uppfæra pantanalínur**.
1. Í svarglugganum **Uppfæra pöntunarlínur**, í reitnum **Uppfæra afhendingarskilmála** og **Uppfæra afhendingarmáta**, skal velja eitt af eftirfarandi gildum:

    - *Aldrei* – Aldrei uppfæra pöntunarlínur eftir að stillingunum hefur verið breytt á pöntunarhausnum.
    - *Alltaf* – Uppfærðu alltaf allar pöntunarlínur eftir að stillingunum hefur verið breytt á pöntunarhausnum.
    - *Kvaðning* – Ef notandi breytir einni eða báðum stillingum á pöntunarhausnum skal opna svarglugga sem spyr hvort notandinn vilji uppfæra allar línur þannig að þær samsvari breytingunni í aðra eða báðar stillingarnar.

Til að setja afhendingarupplýsingar á haus innkaupapöntunar skal fylgja eftirfarandi skrefum.

1. Farðu í **Innkaup og aðföng \> Innkaupapantanir \> Allar innkaupapantanir**.
1. Opna skal innkaupapöntunina sem á að breyta.
1. Veldu yfirlitið **Haus**.
1. Á flýtiflipanum **Afhending** stillirðu reitina **Afhendingarmáta** og **Afhendingarskilmála** eftir þörfum.
1. Það fer eftir stillingum á síðunni **Færibreytur innkaupa og aðfanga** verður þú mögulega spurð/ur hvort þú viljir nota breytingar á öllum pöntunarlínum.

Til að setja upp hnekkingar afhendingarupplýsinga fyrir innkaupapöntunarlínur skal fylgja eftirfarandi skrefum.

1. Farðu í **Innkaup og aðföng \> Innkaupapantanir \> Allar innkaupapantanir**.
1. Opna skal innkaupapöntunina sem á að breyta.
1. Veldu yfirlitið **Línur**.
1. Á flýtiflipanum **Innkaupapöntunarlínur** skal velja línuna sem á að breyta.
1. Í flýtiflipanum **Upplýsingar um línu**, í flipanum **Afhending**, skal stilla reitina **Flutningsmáti** og **Afhendingarskilmálar** eftir þörfum. Hreinsa annan eða báða reitina til að nota samsvarandi stillingar í hausnum.

Fyrir pantanir innan samstæðu verða gildi fyrir reitina **Afhendingarmáti** og **Afhendingarskilmálar** í hverri innkaupapöntunarlínu samstillt milli innkaupapöntunar og tengdrar sölupöntunar.

## <a name="sync-external-item-ids-and-descriptions-for-intercompany-orders"></a>Samstilla ytri vörukenni og lýsingar á pöntunum innan samstæðu

Hvað pöntun innan samstæðu varðar virkjar eiginleikinn *Sjálfvirkt framboð með framleiða eftir pöntun* ytri vörukenni og textalýsingar á innkaupapöntunarlínum við tengdar sölupöntunarlínur innan samstæðu, óháð því hvort innkaupapöntunin er til beinnar afhendingar. Þessi eiginleiki bætir einnig við möguleikanum á að tilgreina endanlegan ytri viðskiptavinalykil samstæðuinnkaupapöntun. Kerfið tekur þá sjálfkrafa ytri vörukenni og textalýsingar ytri viðskiptavinafærslu í stað (innri) lánardrottinsfærslu innan samstæðu.

Fylgdu þessum skrefum til að setja upp lánardrottinn innan samstæðu til að samstilla ytri vörukenni og vöruheiti á milli samstæðuinnkaupapantana og tengdra sölupantana innan samstæðu.

1. Farið í **Innkaup og aðföng \> Lánardrottnar \> Allir lánardrottnar**.
1. Velja samstæðulánardrottinn sem á að setja upp.
1. Á aðgerðasvæðinu, í flipanum **Almennt**, í flokknum **Setja upp**, velurðu **Innan samstæðu**.
1. Á síðunni **Innan samstæðu** á flipanum **Reglur innkaupapantana**, í hlutanum **Innkaupapöntun innan samstæðu -\> Sölupöntun innan samstæðu**, skal velja gátreitinn **Ytra vörukenni og vöruheiti**.

Til að tilgreina endanlegan ytri viðskiptavinalykil fyrir samstæðuinnkaupapöntun skal fylgja eftirfarandi skrefum. Reiturinn **Viðskiptavinalykill** á aðeins við um samstæðuinnkaupapantanir. Notaðu hana til að tilgreina lykilnúmer viðskiptavinarins sem mun að lokum fá varninginn. Þegar þessi reitur er stilltur munu innkaupapöntunarlínur fá ytri vörulýsingu og númer frá þessum viðskiptavinalykli frekar en frá samstæðulánardrottinn sem tilgreindur er í innkaupapöntuninni. Ef viðskiptavinalyklinum er breytt seinna verða ytri vörulýsingar og kenni uppfærð til að samsvara nýja lyklinum. Ytri vörulýsingar og auðkenni fyrir hverja línu verða einnig samstillt við samsvarandi samstæðusölupantanir.

1. Farðu í **Innkaup og aðföng \> Innkaupapantanir \> Allar innkaupapantanir**.
1. Opna skal innkaupapöntunina sem á að setja upp, eða stofna nýja.
1. Veldu yfirlitið **Haus**.
1. Í hlutanum **Tilvísun** stillir þú reitinn **Viðskiptavinalykill** á viðeigandi ytri viðskiptavinalykill.

Til að tilgreina ytri vörukenni og textalýsingar fyrir innkaupapöntunarlínu innan samstæðu skal fylgja eftirfarandi skrefum. Gildin sem þú setur verða samstillt við tengda samstæðusölupöntunarlínur, óháð því hvort innkaupapöntunin er til beinnar afhendingar.

1. Farðu í **Innkaup og aðföng \> Innkaupapantanir \> Allar innkaupapantanir**.
1. Opna skal innkaupapöntunina sem á að setja upp, eða stofna nýja.
1. Veldu yfirlitið **Línur**.
1. Á flýtiflipanum **Innkaupapöntunarlínur** skal velja línuna sem á að breyta.
1. Á flýtiflipanum **Upplýsingar um línu**, á flipanum **Almennt**, í hlutanum **Pöntunarlína**, í reitnum **Texti**, skal gefa upp ytri lýsingu á vörunni sem tilgreind er á völdu pöntunarlínunni. Þetta gildi verður samstillt við tengda samstæðusölupöntunarlínu.
1. Í hlutanum **Tilvísun**, í reitnum **Ytri** skaltu gefa upp ytra vörukenn fyrir vöruna sem tilgreind er í völdu pöntunarlínunni. Þetta gildi verður samstillt við tengda samstæðusölupöntunarlínu.

Frekari upplýsingar eru í [Stofna og reikningsfæra samstæðusölupöntun fyrir ytri viðskiptavin](../sales-marketing/intercompany-sales-order-for-external-customer.md).
