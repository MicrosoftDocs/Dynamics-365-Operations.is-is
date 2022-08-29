---
title: Sjálfvirkt framboð með „framleiða eftir pöntun“
description: Þessi grein lýsir því hvernig á að setja upp og nota hinar ýmsu endurbætur sem bætast við með sjálfvirkni eiginleikum Framleiða eftir pöntun.
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
ms.openlocfilehash: 9044acb472548a797ed387b08ca6892459785793
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220750"
---
# <a name="make-to-order-supply-automation"></a>Sjálfvirkt framboð með „framleiða eftir pöntun“

[!include [banner](../includes/banner.md)]

The *Sjálfvirkni framboðs eftir pöntun* eiginleiki bætir nokkrum endurbótum við Microsoft Dynamics 365 Supply Chain Management. Þessar endurbætur gera þér kleift að framkvæma eftirfarandi verkefni:

- Skoðaðu auðlindagetuálag fyrir notendaskilgreint tímabil og virkja því langtímamat á getuálagi.
- Bættu sveigjanleika með því að stjórna tafaþol (neikvæðum dögum) fyrir hverja aðaláætlun.
- Haltu vörum tiltækum fyrir pantanir á síðustu stundu og hámarkaðu notkun núverandi framboðs með því að tengja nýjasta mögulega framboðið við eftirspurn í stað þess að nota fyrsta mögulega framboðið.
- Haltu íhlutaúthlutun sveigjanlegri fyrir framleiðslupantanir eftir styrkingu, svo að kerfið geti fínstillt fyrir breytingar á eftirspurn á síðustu stundu. Með öðrum orðum, takmarkaðu merkingu við eitt stig.
- Stjórna uppfyllingarstefnu fyrir hverja sölupöntun. Sjálfgefnar stillingar eru teknar úr uppsetningu viðskiptavinarins.
- Bættu upplýsingaflæði milli fyrirtækja. Innkaupapantanir eru uppfærðar þannig að þær innihalda reiti fyrir afhendingarmáta, afhendingarskilmála og ytra vörunúmer. Þessi breyting tryggir að nákvæmar upplýsingar um eftirspurn geti streymt til fyrirtækis sem veitir.

Þessi grein lýsir því hvernig á að setja upp og nota hverja aukahlut.

> [!NOTE]
> Allar endurbætur sem lýst er í þessari grein eiga við um kerfi sem nota innbyggt aðalskipulag. Eftirfarandi tvær endurbætur eru einnig studdar af skipulagsfínstillingarviðbótinni fyrir Microsoft Dynamics 365 Supply Chain Management:
>
> - Seinkunarþol á aðalskipulagi
> - Stjórn yfir tengingaröðinni sem er notuð við aðalskipulagningu

## <a name="turn-on-the-make-to-order-supply-automation-feature"></a>Kveiktu á sjálfvirknieiginleika Gera eftir pöntun

Áður en þú getur notað eiginleikann sem lýst er í þessari grein verður þú að kveikja á honum fyrir kerfið þitt. Stjórnendur geta notað [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vinnusvæði, þar sem eiginleikinn er skráður á eftirfarandi hátt:

- **Eining:** *Aðalskipulag*
- **Eiginleikaheiti:** *Sjálfvirkni framboðs eftir pöntun*

## <a name="set-the-number-of-days-to-show-on-capacity-load-page"></a>Stilltu fjölda daga sem á að birtast á síðunni Hleðsla

The **Afkastagetu álag** síða gerir þér kleift að skoða tiltæka getu tilfangs. The *Sjálfvirkni framboðs eftir pöntun* eiginleiki eykur **Afkastagetu álag** síðu með því að bæta við a **Fjöldi daga** sviði. Þú getur notað þennan reit til að takmarka fjölda daga sem **Yfirlit** rist sýnir. Gildið sem þú stillir er vistað í minni. Þess vegna, ef þú yfirgefur síðuna og kemur síðan aftur síðar, **Yfirlit** rist mun samt sýna fjölda daga sem þú tilgreindir síðast.

Til að opna **Afkastagetu álag** síðu svo að þú getir skoðað tiltæka getu fyrir einstaka tilföng skaltu fylgja þessum skrefum.

1. Fara til **Stjórn stofnunarinnar \> Auðlindir \> Auðlindir**.
1. Veldu úrræði til að skoða.
1. Á aðgerðarrúðunni, á **Auðlind** flipa, í **Útsýni** hópur, veldu **Afkastagetu álag**.
1. Nota **Fjöldi daga** sía til að takmarka fjölda daga sem **Yfirlit** rist sýnir.

Til að opna **Afkastagetu álag** síðu svo að þú getir skoðað tiltæka getu fyrir tilfangahóp skaltu fylgja þessum skrefum.

1. Fara á **Fyrirtækisstjórnun \> Tilföng \> Tilfangaflokkar**.
1. Veldu tilfangahóp til að skoða.
1. Á aðgerðarrúðunni, á **Auðlindahópur** flipa, í **Útsýni** hópur, veldu **Afkastagetu álag**.
1. Nota **Fjöldi daga** sía til að takmarka fjölda daga sem **Yfirlit** rist sýnir.

## <a name="apply-a-single-level-of-marking-when-you-firm-planned-orders"></a>Notaðu eitt stig af merkingu þegar þú staðfestir skipulagðar pantanir

*Merking* er notuð til að tengja framboð og eftirspurn. Slíkt er svipað og *þarfarakning*, sem gefur til kynna hvernig aðaláætlanagerð gerir ráð fyrir því að uppfylla eftirspurn. Hins vegar er merking varanlegri en tenging. The *Sjálfvirkni framboðs eftir pöntun* eiginleiki bætir við getu til að takmarka birgðamerkingu á eitt stig þegar fyrirhugaðar pantanir eru staðfestar. Það bætir eftirfarandi nýjum valkostum við **Uppfæra merkingu** sviði í **Stífandi** svargluggi þegar þú ert að staðfesta fyrirhugaða pöntun:

- *Staðall á einu stigi* – Einstigs merking er notuð. Einþreps merking merkir aðeins aðalhlutinn, ekki efnisskrá (BOM) íhluti hans. Þess vegna er hægt að halda íhlutaúthlutun fyrir framleiðslupantanir sveigjanlegan eftir styrkingu. Eins stigs merking gerir kerfinu kleift að hagræða fyrir breytingar á eftirspurn á síðustu stundu. Í *staðall* eins stigs merking, kröfupantanir eru merktar við uppfyllingarpantanir þeirra, en uppfyllingarpantanir eru ekki merktar ef þær hafa eftirstandandi magn.
- *Einhæð stækkuð* – Einstigs merking er notuð. Í *framlengdur* eins stigs merking, kröfupantanir eru merktar við uppfyllingarpantanir þeirra og uppfyllingarpantanir eru alltaf merktar, óháð því hvort eitthvað magn er eftir.

Þessir valkostir eru einnig fáanlegir í **Uppfæra merkingu** sviði á **Hefðbundin uppfærsla** flipi á **Aðalskipulagsbreytur** síðu, þar sem þú skilgreinir sjálfgefið val fyrir **Stífandi** valmynd.

Fyrir frekari upplýsingar, sjá [Birgðamerking með áætlanagerð hagræðingu](planning-optimization/marking.md).

## <a name="set-delay-tolerance-negative-days-at-the-master-plan-level"></a>Stilltu tafaþol (neikvæð dagar) á aðalskipulagsstigi

The *Sjálfvirkni framboðs eftir pöntun* eiginleiki bætir við getu til að stilla tafaþol (neikvæð dagar) á aðalskipulagsstigi. Stillingin er einnig fáanleg á stigi vöruþekju og þekjuhóps. Ef neikvæðum dögum er úthlutað á fleiri en einu stigi notar kerfið eftirfarandi stigveldi til að ákveða hvaða stillingu á að nota:

- Ef neikvæðir dagar eru stilltir á **Aðaláætlanir** síðu, þessi stilling hnekkir öllum öðrum neikvæðum dagastillingum þegar áætlunin keyrir.
- Ef neikvæðir dagar eru stilltir á **Vöruumfjöllun** síðu, þá hnekkir sú stilling stillingu umfjöllunarhóps.
- Neikvæðar dagar sem eru stilltir á **Umfjöllunarhópar** síðu eiga aðeins við ef neikvæðir dagar hafa ekki verið stilltir fyrir viðkomandi vöru eða aðalskipulag.

Til að stilla neikvæða daga fyrir aðalskipulag skaltu fylgja þessum skrefum.

1. Farið í **Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Aðaláætlanir**.
1. Veldu aðaláætlun í listaglugganum eða búðu til nýja.
1. Á **Tímagirðingar í dögum** flýtiflipann, stilltu **Neikvæðar dagar** valmöguleika til *Já*.
1. Í næsta reit skaltu slá inn fjölda neikvæðra daga til að leyfa.

Fyrir frekari upplýsingar um hvernig á að nota neikvæða daga, sjá [Seinkunarþol (neikvæð dagar)](planning-optimization/delay-tolerance.md).

## <a name="control-the-pegging-sequence-used-during-master-planning"></a>Stjórna festingarröðinni sem notuð er við aðalskipulagningu

Aðalskipulag notar a *festingarröð* til að ákvarða hvaða framboð mun standa undir hvaða eftirspurn. The *Sjálfvirkni framboðs eftir pöntun* eiginleiki bætir við nýjum **Notaðu nýjasta mögulega framboðið** valkostur sem gefur þér meiri stjórn á tengingaröðinni. Nýi valkosturinn gerir þér kleift að halda vörum tiltækum fyrir pantanir á síðustu stundu og hámarka notkun núverandi framboðs með því að tengja nýjasta mögulega framboðið við eftirspurn í stað þess að nota fyrsta mögulega framboðið.

Þú getur stillt festingarröðina á aðalskipulagi, vöruþekju eða þekjuhópsstigi. Ef tengiröð er sett upp á fleiri en einu stigi beitir kerfið eftirfarandi stigveldi til að ákveða hvaða stillingu á að nota:

- Ef festingarröð er sett upp á **Aðaláætlanir** síðu, þessi stilling hnekkir öllum öðrum stillingum fyrir tengiröð þegar áætlunin keyrir.
- Ef festingarröð er sett upp á **Vöruumfjöllun** síðu, þá hnekkir sú stilling stillingu umfjöllunarhóps.
- Peggingaröðin sem er sett upp á **Umfjöllunarhópar** síða á aðeins við ef tengiraðarstillingar hafa ekki verið stilltar fyrir viðkomandi vöru eða aðalskipulag.

Fylgdu þessum skrefum til að setja upp tengingu á þekjuhópsstigi.

1. Fara skal í **Aðaláætlanagerð \> Uppsetning \> Þekja \> þekjuflokkar**.
1. Veldu hóp í listaglugganum eða búðu til nýjan.
1. Á **Almennt** Flýtiflipi, í **Pegging röð** kafla, notaðu **Neyta á lager** og **Notaðu nýjasta framboðið** reiti til að stilla tengiröðina þína. Taflan síðar í þessum hluta sýnir hvernig þessar stillingar eru sameinaðar til að skilgreina tengiröðina þína.

Til að setja upp tengingu á vöruþekjustigi skaltu fylgja þessum skrefum.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Veldu vöru í ristinni eða búðu til nýja.
1. Á aðgerðarrúðunni, á **Áætlun** flipa, veldu **Vöruumfjöllun**.
1. The **Vöruumfjöllun** síða veitir línur sem gera þér kleift að skilgreina þekjureglur sem eiga við vöruna í hverju vöruhúsi. Veldu fyrirliggjandi línu í hnitanetinu eða búðu til nýja.
1. Á **Almennt** flipann, veldu **Hneka tengiröð** gátreit.
1. Nota **Neyta á lager** og **Notaðu nýjasta framboðið** reiti til að stilla tengiröðina þína. Taflan síðar í þessum hluta sýnir hvernig þessar stillingar eru sameinaðar til að skilgreina tengiröðina þína.

Til að setja upp tengingu á aðalskipulagsstigi skaltu fylgja þessum skrefum.

1. Farið í **Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Aðaláætlanir**.
1. Veldu aðaláætlun í listaglugganum eða búðu til nýja.
1. Á **Almennt** flýtiflipann, stilltu **Hneka tengiröð** valmöguleika til *Já*.
1. Nota **Neyta á lager** og **Notaðu nýjasta framboðið** reiti til að stilla tengiröðina þína. Taflan síðar í þessum hluta sýnir hvernig þessar stillingar eru sameinaðar til að skilgreina tengiröðina þína.

Eftirfarandi tafla sýnir hvernig **Neyta á lager** og **Notaðu nýjasta framboðið** stillingar eru sameinaðar til að koma á tengingaröðinni þinni.

| | Notaðu nýjustu framboð = Já | Notaðu nýjustu framboð = Nei |
|---|---|---|
| **Neyta á lager** = *Áður en allt framboð* | <ol><li>Á lager</li><li>Núverandi framboð sem getur mætt dagsetningu eftirspurnar</li><li>Núverandi framboð sem getur ekki mætt dagsetningu eftirspurnar, en samt innan neikvæðra daga</li><li>Búa til nýtt framboð (fyrirhuguð pöntun)</li></ol> | <ol><li>Á lager</li><li>Núverandi framboð sem getur mætt dagsetningu eftirspurnar</li><li>Núverandi framboð sem getur ekki mætt dagsetningu eftirspurnar, en samt innan neikvæðra daga</li><li>Búa til nýtt framboð (fyrirhuguð pöntun)</li></ol> |
| **Neyta á lager** = *Eftir allt framboð* | <ol><li>Núverandi framboð sem getur mætt dagsetningu eftirspurnar</li><li>Á lager</li><li>Núverandi framboð sem getur ekki mætt dagsetningu eftirspurnar, en samt innan neikvæðra daga</li><li>Búa til nýtt framboð (fyrirhuguð pöntun)</li></ol> | <ol><li>Núverandi framboð sem getur mætt dagsetningu eftirspurnar</li><li>Núverandi framboð sem getur ekki mætt dagsetningu eftirspurnar, en samt innan neikvæðra daga</li><li>Á lager</li><li>Búa til nýtt framboð (fyrirhuguð pöntun)</li></ol> |

## <a name="review-and-set-the-fulfillment-policy-that-applies-to-each-sales-order"></a>Skoðaðu og stilltu uppfyllingarstefnuna sem á við hverja sölupöntun

Uppfyllingarreglur stjórna því hlutfalli af heildarpöntunarverði eða magni sem þarf að vera frátekið líkamlega áður en hægt er að gefa út sölupöntun í vöruhúsið. Þú getur stillt alþjóðlega sjálfgefna uppfyllingarstefnu og síðan hnekkt henni fyrir tiltekna viðskiptavini eftir þörfum. The *Sjálfvirkni framboðs eftir pöntun* eiginleiki bætir við möguleikanum á að skoða hvaða sjálfgefna stefna gildir í raun um hvaða pöntun sem er og beita pöntunarsértækri hnekkingu eftir þörfum.

- Til að stilla sjálfgefna alþjóðlega uppfyllingarstefnu fyrir sölupantanir, farðu á **Reikningur fáanlegur \> Uppsetning \> Færibreytur viðskiptakrafna**. Síðan, á **Vöruhússtjórnun** flipann, stilltu **Stefna um uppfyllingu sölupöntunar** reitnum við nafnið á stefnunni sem þú vilt nota. 
- Til að stilla viðskiptavinarsértæka uppfyllingarstefnu fyrir sölupantanir skaltu fara á **Reikningur fáanlegur \> Viðskiptavinir \> Allir viðskiptavinir**. Síðan, á **Vöruhús** flipann, stilltu **Uppfyllingarstefna** reitnum við nafnið á stefnunni sem þú vilt nota.

Til að skoða sjálfgefna stefnu sem á við um hvaða pöntun sem er og beita pöntunarsértækri hnekkingu skaltu fylgja þessum skrefum.

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Opnaðu sölupöntunina sem þú vilt skoða eða breyta.
1. Veldu **Fyrirsögn** útsýni.
1. Á **Vöruhús** Flýtiflipa, skoðaðu og breyttu eftirfarandi reitum eftir þörfum:

    - **Stefna um uppfyllingu pantana** – Veldu uppfyllingarstefnuna sem á að nota fyrir valda pöntun. Sjálfgefin stefna verður hnekkt. Til að nota sjálfgefna uppfyllingarstefnu sem er sýnd í **Sjálfgefin uppfyllingarstefna** reit, skildu þennan reit eftir auðan.
    - **Sjálfgefin uppfyllingarstefna** – Þessi reitur sýnir sjálfgefna uppfyllingarstefnu sem gildir ef **Stefna um uppfyllingu pantana** reiturinn er auður. Þetta svæði er aðeins til lestrar. Ef það er autt er engin viðskiptavinasértæk eða alþjóðleg sjálfgefna uppfyllingarstefna skilgreind.

    Ef bæði **Stefna um uppfyllingu pantana** sviði og **Sjálfgefin uppfyllingarstefna** reiturinn er auður, engin uppfyllingarstefna gildir. Hins vegar gætu aðrar takmarkanir verið til staðar og gætu krafist þess að fyrirvara eða önnur skilyrði séu uppfyllt áður en hægt er að losa sölupöntunina.

## <a name="set-the-delivery-mode-and-terms-on-individual-purchase-order-lines"></a>Stilltu afhendingarham og skilmála á einstökum innkaupapöntunarlínum

Allar innkaupapantanir innihalda **Afhendingarskilmálar** og **Afhendingarmáti** stillingar á pöntunarhaus. The *Sjálfvirkni framboðs eftir pöntun* eiginleiki bætir þessum stillingum við hverja pöntunarlínu. Þess vegna er hægt að skilgreina hnekkingar á **Afhendingarskilmálar** og/eða **Afhendingarmáti** gildi fyrir einhverjar eða allar pöntunarlínur eftir þörfum. Fyrir línur þar sem engin hnekking er skilgreind er gildið úr hausnum notað. Þú getur tilgreint hvort breyting á gildi annars eða beggja þessara reita á pöntunarhaus ætti einnig að uppfæra allar línur.

Til að tilgreina hvað ætti að gerast við línustillingar ef notandi breytir **Afhendingarskilmálar** og/eða **Afhendingarmáti** gildi á pöntunarhaus skaltu fylgja þessum skrefum.

1. Opnið **Innkaup og aðföng \> Uppsetning \> Færibreytur innkaupa og aðfanga**.
1. Á **Almennt** flipa, á **Sjálfgefin gildi og færibreytur** flýtiflipann, veldu **Uppfærðu pöntunarlínur** hlekkur.
1. Í **Uppfærðu pöntunarlínur** valmynd, í **Uppfærsla afhendingarskilmála** og **Uppfærslumáti afhendingar** reiti skaltu velja eitt af eftirfarandi gildum:

    - *Aldrei* - Aldrei uppfæra pöntunarlínurnar eftir að stillingum hefur verið breytt á pöntunarhausnum.
    - *Alltaf* – Uppfærðu alltaf allar pöntunarlínur eftir að stillingum hefur verið breytt á pöntunarhaus.
    - *Hvetja* – Ef notandi breytir annarri eða báðum stillingum á pöntunarhausnum, opnaðu gluggabotn sem spyr hvort notandinn vilji uppfæra allar línur þannig að þær passi breytinguna við aðra eða báðar stillingarnar.

Til að stilla afhendingarupplýsingar á innkaupapöntunarhaus skaltu fylgja þessum skrefum.

1. Farðu í **Innkaup og aðföng \> Innkaupapantanir \> Allar innkaupapantanir**.
1. Opnaðu innkaupapöntunina sem þú vilt breyta.
1. Veldu **Fyrirsögn** útsýni.
1. Á **Afhending** flýtiflipann, stilltu **Afhendingarmáti** og **Afhendingarskilmálar** reiti eftir þörfum.
1. Það fer eftir stillingum á **Innkaupa- og innkaupabreytur** síðu gætirðu verið spurður hvort þú viljir beita breytingunum þínum á allar pöntunarlínur.

Fylgdu þessum skrefum til að stilla hnekkingar á afhendingarupplýsingum fyrir innkaupapöntunarlínu.

1. Farðu í **Innkaup og aðföng \> Innkaupapantanir \> Allar innkaupapantanir**.
1. Opnaðu innkaupapöntunina sem þú vilt breyta.
1. Veldu **Línur** útsýni.
1. Á **Innkaupapöntunarlínur** Flýtiflipi, veldu línuna sem á að breyta.
1. Á **Upplýsingar um línu** flýtiflipann, á **Afhending** flipann, stilltu **Afhendingarmáti** og **Afhendingarskilmálar** reiti eftir þörfum. Hreinsaðu einn eða báða reitina til að nota samsvarandi stillingar á hausnum.

Fyrir innbyrðis pantanir, gildi fyrir **Afhendingarmáti** og **Afhendingarskilmálar** reitir á hverri innkaupapöntunarlínu verða samstilltir á milli innkaupapöntunarinnar og tengdrar sölupöntunar hennar.

## <a name="sync-external-item-ids-and-descriptions-for-intercompany-orders"></a>Samstilltu ytri vöruauðkenni og lýsingar fyrir pantanir milli fyrirtækja

Fyrir innbyrðis pantanir, *Sjálfvirkni framboðs eftir pöntun* eiginleiki gerir kleift að samstilla ytri vöruauðkenni og textalýsingar á innkaupapöntunarlínum við tengdar sölupöntunarlínur innan samstæðu, óháð því hvort innkaupapöntunin er fyrir beina afhendingu. Eiginleikinn bætir einnig við möguleikanum á að tilgreina endanlegan ytri viðskiptavinareikning í innkaupapöntun milli fyrirtækja. Kerfið mun þá sjálfkrafa taka utanaðkomandi vöruauðkenni og textalýsingar úr ytri viðskiptamannaskrá í stað (innri) færslu lánardrottins.

Fylgdu þessum skrefum til að setja upp lánardrottin innan samstæðu til að samstilla ytri vöruauðkenni og vöruheiti á milli innkaupapantana innan samstæðu og tengdra samstæðusölupantana.

1. Farið í **Innkaup og aðföng \> Lánardrottnar \> Allir lánardrottnar**.
1. Veljið innbyrðis lánardrottinn sem þú vilt setja upp.
1. Á aðgerðarrúðunni, á **Almennt** flipa, í **Settu upp** hópur, veldu **Millifyrirtæki**.
1. Á **Millifyrirtæki** síðu, á **Reglur um innkaupapöntun** flipa, í **Innkaupapöntun milli fyrirtækja -\> Sölupöntun milli fyrirtækja** kafla, veldu **Ytri vöruauðkenni og vöruheiti** gátreit.

Til að tilgreina endanlega ytri viðskiptavinareikning fyrir innkaupapöntun innan samstæðu skal fylgja þessum skrefum. The **Viðskiptavinareikningur** reiturinn á aðeins við um innkaupapantanir milli fyrirtækja. Notaðu það til að tilgreina reikningsnúmer viðskiptavinarins sem mun að lokum fá vörurnar. Þegar þessi reitur er stilltur munu innkaupapöntunarlínur taka ytri vörulýsingar og númer frá tilgreindum viðskiptamannareikningi í stað samstæðu lánardrottins sem er tilgreindur á innkaupapöntuninni. Ef þú breytir viðskiptamannareikningi síðar verða ytri vörulýsingar og auðkenni uppfærðar þannig að þær passi við gildin fyrir nýja reikninginn. Ytri vörulýsingar og auðkenni fyrir hverja línu verða einnig samstillt við samsvarandi sölupöntun milli fyrirtækja.

1. Farðu í **Innkaup og aðföng \> Innkaupapantanir \> Allar innkaupapantanir**.
1. Opnaðu innkaupapöntunina sem þú vilt setja upp eða búðu til nýja.
1. Veldu **Fyrirsögn** útsýni.
1. Í **Tilvísun** kafla, stilltu **Viðskiptavinareikningur** reitnum á viðkomandi ytri viðskiptavinareikning.

Til að tilgreina ytri vöruauðkenni og textalýsingar fyrir innkaupapöntunarlínu fyrir samstæðupöntun skal fylgja þessum skrefum. Gildin sem þú stillir verða samstillt við tengdar sölupöntunarlínur milli samstæðu, óháð því hvort innkaupapöntunin er fyrir beina afhendingu.

1. Farðu í **Innkaup og aðföng \> Innkaupapantanir \> Allar innkaupapantanir**.
1. Opnaðu innkaupapöntunina sem þú vilt setja upp eða búðu til nýja.
1. Veldu **Línur** útsýni.
1. Á **Innkaupapöntunarlínur** Flýtiflipi, veldu línuna sem á að breyta.
1. Á **Upplýsingar um línu** flýtiflipann, á **Almennt** flipa, í **Pöntunarlína** kafla, í **Texti** reit, gefðu upp ytri lýsingu á vörunni sem er tilgreind á valinni pöntunarlínu. Þetta gildi verður samstillt við tengda sölupöntunarlínu milli fyrirtækja.
1. Í **Tilvísun** kafla, í **Ytri** reit, gefðu upp ytra vöruauðkenni fyrir vöruna sem er tilgreint í valinni pöntunarlínu. Þetta gildi verður samstillt við tengda sölupöntunarlínu milli fyrirtækja.

Fyrir frekari upplýsingar, sjá [Stofna og reikningsfæra innbyrðis sölupöntun fyrir utanaðkomandi viðskiptavin](../sales-marketing/intercompany-sales-order-for-external-customer.md).
