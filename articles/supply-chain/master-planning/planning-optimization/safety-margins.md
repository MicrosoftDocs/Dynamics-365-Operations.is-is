---
title: Öryggismörk
description: Í þessari grein er því lýst hvernig öryggismörk virka við aðaláætlanagerð.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-9-14
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 87b38276a2723374969a67c5413dde15537d04ec
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740442"
---
# <a name="safety-margins"></a>Öryggismörk

[!include [banner](../../includes/banner.md)]

Í þessari grein er því lýst hvernig öryggismörk virka við aðaláætlanagerð.

## <a name="safety-margins-overview"></a>Yfirlit yfir öryggismörk

Tilgangurinn með öryggismörkum er að virkja uppsetningu sem býður upp á einhvern skipulagstíma utan venjulegs afhendingartíma. Þegar þarf til dæmis að taka hráefni úr pakkningu eða skoða það þegar það kemur frá lánardrottni, er ekki einfaldlega hægt að bæta aukatímanum við afhendingartíma innkaupanna, því að aukalegi skipulagstíminn fer þá til birgja. Í þessu dæmi er hægt að nota innhreyfingarmörkin til að tryggja að birginn afhendi á réttum tíma. Þessi nálgun býður upp á skipulagstíma þannig að hægt sé að afgreiða varninginn innan fyrirtækisins.

Það eru þrjár gerðir öryggismarka:

- **Endurpöntunarmörk** – Skipulagstíminn til að leggja fram birgðapöntun
- **Innhreyfingarmörk** – Skipulagstíminn til að afgreiða birgðir á innleið
- **Úthreyfingarmörk** – Skipulagstíminn til að afgreiða sendingar

Eftirfarandi mynd sýnir hvernig þessi öryggismörk eiga við yfir tíma.

![Öryggismörk.](media/safety-margins-1.png)

Öll mörk eru skilgreind í dögum. Sjálfgefið gildi, *0* (núll), gefur til kynna að engin mörk eru notuð. Ef mörg mörk eru sett upp, bætast þau öll við heildartímann frá *pöntunardagsetningu* birgða til *þarfadagsetningar* eftirspurnar. Til dæmis er uppsetning ekki með neinn afhendingartíma og allar þrjár gerðirnar af mörkum eru stilltar á einn dag. Í slíku tilfelli verða þrír dagar á milli dagsetningar birgðapöntunar og þarfadagsetningar eftirspurnar, þannig að ef pöntunardagsetningin er 1. júlí verður dagsetning þarfa 4. júlí.

### <a name="receipt-margin"></a>Mörk innhreyfinga

Mörk innhreyfinga er líklega mest notuð af öllum þremur öryggismörkunum. Þau eru notuð fyrir *afhendingardaginn* og aftur á bak frá *dagsetningu þarfa*. Með öðrum orðum ættu afurðirnar að fá tiltekinn dagafjölda fyrir innhreyfingarmörk áður en þess gerist þörf.

Eftirfarandi mynd sýnir mörk innhreyfinga.

![Mörk innhreyfinga.](media/safety-margins-2.png)

Mörk innhreyfinga er yfirleitt notuð sem biðtími til að tryggja að tími gefist til vöruhúsaskráningar eða annarra tímafrekra ferla sem eru ekki hluti af almennum afhendingartíma í kerfinu. Fyrir innkaup er einn ávinningur sá að *afhendingardagur* innkaupapöntunarinnar er færður fram eftir þörfum. Ef afhendingartími er aukinn í stað þess að nota öryggismörk verður lánardrottinn samt beðinn um að afhenda á síðustu stundu.

Takið eftir að mörk innhreyfinga breyta ekki *dagsetningu þarfa* fyrir birgðirnar. Þess vegna eru mörk innhreyfinga ekki sýnileg með beinum hætti þegar dagsetningar þarfa fyrir eftirspurn og framboð eru borin saman (til dæmis á síðunni **Nettó þarfir**). Ef mörk innhreyfinga eru t.d. stillt á fjóra daga og innkaupapöntunarlína er áætluð til innhreyfingar þann fimmtánda þess mánaðar, mun aðaláætlanagerðin reikna út að leiðrétt dagsetning innhreyfingar verði þann nítjánda þess mánaðar.

Athugið að mörk innhreyfinga eru ekki notuð þegar lagerbirgðir eru notaðir sem birgðir. Gert er ráð fyrir að allar lagerbirgðir séu lausar strax, óháð því hvenær þær voru mótteknar.

### <a name="reorder-margin"></a>Endurpöntunarmörk

Eftirfarandi mynd sýnir endurpöntunarmörkin.

![Endurpöntunarmörk.](media/safety-margins-3.png)

Endurpöntunarmörkum er bætt við á undan afhendingartíma vörunnar fyrir allar áætlaðar pantanir á meðan aðaláætlanagerð stendur. Þess vegna tryggir það frekari tíma til að leggja fram birgðapöntun. Þessi mörk eru yfirleitt notuð sem biðtími til að tryggja tíma fyrir samþykktarferli eða aðra innri ferla sem eru nauðsynlegir við stofnun birgðapantana. Endurpöntunarmörkin eru sett á milli *pöntunardagsetningar* birgða og *upphafsdagsetningar*.

### <a name="issue-margin"></a>Mörk úthreyfinga

Eftirfarandi mynd sýnir mörk úthreyfinga.

![Mörk úthreyfinga.](media/safety-margins-4.png)

Mörk úthreyfinga eru dregin frá eftirspurnardagsetningu þarfa í aðaláætlanagerð. Það tryggir að þú hafir tíma til að bregðast við og senda eftirspurnarpantanir á innleið. Þessi mörk eru yfirleitt notuð sem biðtími til að tryggja tíma fyrir sendingu og tengda vöruhúsaferli á útleið.

Taktu eftir því að þegar mörk úthreyfinga eru notuð, passa tengdar þarfadagsetningar framboðs og eftirspurnar ekki saman. Í staðinn er munurinn á milli þeirra það sem nemur úthreyfingarmörkum vegna þess að úthreyfingarmörkunum er bætt við milli *þarfadagsetningar* framboðs og *þarfadagsetningar* eftirspurnar.

## <a name="set-up-safety-margins"></a>Setja upp öryggismörk

### <a name="turn-safety-margins-on-or-off"></a>Kveikja eða slökkva á öryggismörkum

Til að nota þennan eiginleika þarf að kveikja á honum fyrir kerfið þitt. (Frá og með útgáfu 10.0.29 af Supply Chain Management er þessi eiginleiki skylda og ekki er hægt að slökkva á honum.) Ef þú ert að keyra útgáfu sem er eldri en 10.0.29, þá geta stjórnendur kveikt eða slökkt á þessum eiginleika með því að leita að eiginleikanum *Hlutfall fyrir fínstillingu áætlanagerðar* á vinnusvæðinu [Eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="define-safety-margins"></a>Skilgreina öryggismörk

Öryggismörk eru með sveigjanlega uppsetningu. Hægt er að stilla þau í bæði *þekjuflokki* og *aðaláætlun*. Mikilvægt er að skilja að mörkin eru lögð ofan á hvert annað. Til dæmis ef innhreyfingarmörk eru tveir dagar í þekjuflokknum og þrír dagar í aðaláætlanagerðinni verða til virk innhreyfingarmörk upp á fimm daga.

Möguleikinn á því að stilla mörkin í aðaláætlanagerðinni getur verið gagnlegt þegar þú vilt líkja eftir lengri afhendingartímum eða óvissu fyrir tiltekinni áætlun, en án þess að hafa áhrif á daglega áætlanagerð.

#### <a name="coverage-group-safety-margins"></a>Öryggismörk þekjuflokks

Til að nota öryggismörk í þekjuflokki skal fylgja þessum skrefum.

1. Fara skal í **Aðaláætlanagerð \> Uppsetning \> Þekjuflokkar**.
1. Í listasvæðinu skal velja þekjuflokk sem óskað er eftir.
1. Í flýtiflipanum **Annað**, í hlutanum **Öryggismörk í dögum**, skal nota eftirfarandi reiti til að stilla nauðsynleg öryggismörk (í dögum):

    - Mörk innhreyfinga bætt við dagsetningu þarfa
    - Mörk úthreyfinga dregin af dagsetningu þarfa
    - Endurpöntunarmagni bætt við afhendingartíma vöru

#### <a name="master-plan-safety-margins"></a>Öryggismörk aðaláætlunar

Til að nota öryggismörk við aðaláætlun skal fylgja þessum skrefum.

1. Farið í **Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Aðaláætlanir**.
1. Í listasvæðinu skal velja aðaláætlun sem óskar er eftir.
1. Í flýtiflipanum **Öryggismörk í dögum** skal nota eftirfarandi reiti til að stilla nauðsynleg öryggismörk (í dögum):

    - Mörk innhreyfinga bætt við dagsetningu þarfa
    - Mörk úthreyfinga dregin af dagsetningu þarfa
    - Endurpöntunarmagni bætt við afhendingartíma vöru

### <a name="define-whether-calculations-are-based-on-calendar-days-or-work-days"></a>Skilgreina hvort útreikningar eru byggðir á almanaksdögum eða vinnudögum

Hægt er að stilla öll öryggismörk þannig að þau séu reiknuð út frá annaðhvort almanaksdögum eða vinnudögum.

1. Farið í **Aðaláætlanagerð \> Uppsetning \> Færibreytur aðaláætlanagerðar**.
1. Í flipanum **Almennt**, í hlutanum **Öryggismörk í dögum**, skal stilla valkostinn **Vinnudagar** á *Já* til að reikna mörk sem byggja á vinnudögum. Stillið valkostinn á *Nei* til að reikna út mörk samkvæmt almanaksdögum.

Til dæmis er dagatal opið frá mánudegi til föstudags og lokað frá laugardegi til sunnudags. Ef um er að ræða innhreyfingarmörk upp á einn dag, mun þarfadagsetning á mánudegi búa til afhendingardag á föstudeginum á undan, því að laugardagur og sunnudagur eru ekki vinnudagar.

Dagatalið sem er notað til að ákvarða vinnudagana veltur á uppsetningu og gerð framboðs.. Hægt er að stýra því með dagatölum þekjuflokksins, vöruhússins og lánardrottins.

> [!NOTE]
> Ef *vöruhús* er ekki hluti af þekjuvíddinni (með öðrum orðum, áætlun byggir aðeins á *svæði*), er dagatal vöruhússins ekki notað.

Kerfið ræður við uppsetningu þar sem eitt eða fleiri dagatöl eru skilgreind. Eftirfarandi undirhlutar lýsa mögulegum samsetningum sem hægt er að nota til að hafa stjórnun á niðurstöðunum.

#### <a name="calendar-that-is-used-for-the-duration"></a>Dagatal sem er notað við lengd

Skilgreindu dagatölin stýra raunverulegum heildartíma afhendingar í almanaksdögum, frá dagsetningu birgðapöntunar til þarfadagsetningar eftirspurnar. Eftirfarandi forgangsröðun dagatals er notuð:

- **Afhendingartími innkaupa** – Aðeins er stuðst við dagatal þekjuflokks.
- **Mörk innhreyfinga** – Dagatal þekjuflokksins er notað, ef það er skilgreint. Annars er dagatal vöruhúss notað.
- **Mörk úthreyfinga** – Dagatal þekjuflokksins er notað, ef það er skilgreint. Annars er dagatal vöruhúss notað.
- **Pöntunarmörk** – Aðeins er stuðst við dagatal þekjuflokks.

#### <a name="calendar-that-is-used-for-the-final-date"></a>Dagatal sem er notað fyrir lokadagsetninguna

Eftirfarandi reglur eru notaðar til að ákvarða hvort áætlunarvélin geti notað tiltekna dagsetningu fyrir tiltekna dagsetningargerð:

- **Dagsetning á innhreyfingu innkaupa** – Dagatal lánardrottins er notað, ef það er skilgreint. Annars er dagatal þekjuflokksins notað, ef það er skilgreint. Ef hvorugt dagatanna er skilgreint er dagatal vöruhúss notað.
- **Innhreyfingardagsetning flutnings** – Dagatal þekjuflokksins er notað, ef það er skilgreint. Annars er dagatal vöruhúss notað.
- **Innhreyfingardagsetning framleiðslu** – Dagatal þekjuflokksins er notað, ef það er skilgreint. Annars er dagatal vöruhúss notað.
- **Opinn dagur á úthreyfingu eftirspurnar** – Dagatal vöruhúss er notað, ef það er skilgreint. Annars er dagatal þekjuflokksins notað.
- **Opinn dagur pöntunar** – Samsetning (sniðmengi) dagatals þekjuflokksins og dagatals lánardrottins er notuð. Bæði dagatöl verða að vera opin til að nota dagsetninguna. Ef aðeins eitt af dagatölum er skilgreint er dagatalið notað eitt og sér.

#### <a name="calendar-setup-overview-matrix"></a>Yfirlit uppsetningar dagatals - fylki

Eftirfarandi mynd sýnir fylki sem tekur saman hvaða dagatöl eiga við þegar öryggismörk eru reiknuð. (Veldu myndina til að opna hana í hágæðum.) Eftirfarandi skammstafanir og litir eru notaðir til að gefa til kynna hvar hver gerð dagatals er tilgreind:

- **Þekjuflokkur (ÞF):** Grænn
- **Vöruhús (VH):** Gulur
- **Lánardrottinn (L):** Blár

[![Yfirlit uppsetningar dagatals - fylki.](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)

## <a name="calculating-delays"></a>Reiknar seinkun

Allar þrjár gerðir öryggismarka eru höfð með þegar kerfið ákveður hvort pöntun sé seinkað.

Til dæmis er vara með afhendingartíma upp á einn dag og innhreyfingarmörk upp á þrjá daga. Sölupöntun fyrir þessa vöru er stillt eins og krafist í dag. Í slíku tilfelli er töfin reiknuð sem *afhendingartími* + *mörk innhreyfinga* = fjórir dagar. Þess vegna, ef í dag er 14. ágúst, leiðir fjögurra daga töf til afhendingar þann 18. ágúst. Eftirfarandi mynd sýnir þetta dæmi.

![Dæmi um útreikning á töfum.](media/safety-margins-delays.png)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]