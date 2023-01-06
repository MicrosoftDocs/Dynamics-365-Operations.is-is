---
title: Búa til samstæðureikningsskil
description: Þessi grein lýsir ýmsum sviðum þar sem þú gætir búið til samstæðureikningsskil.
author: aprilolson
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: c6a132b742414a3dab635634c7bb5ba0dbea527d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846800"
---
# <a name="generate-consolidated-financial-statements"></a>Búa til samstæðureikningsskil

[!include [banner](../includes/banner.md)]

Þessi grein lýsir ýmsum sviðum þar sem þú gætir búið til samstæðureikningsskil.

## <a name="single-level-and-multilevel-consolidations-across-legal-entities"></a>Samstæður á einu eða mörgum stigum yfir lögaðila
Einfaldasta aðferðin til að sameina með Financial reporting er að nota skipurit til að safna gögnum yfir fyrirtæki sem hafa sama bókhaldslykil og fjárhagstímabil. Hér eru hástigs skrefin til að sameina með skipuriti.

1. Búðu til línuskilgreiningu og vertu viss um að allir viðeigandi lyklar í öllum fyrirtækjum séu með í línunum.
2. Búðu til dálkskilgreiningu sem inniheldur alla dálka sem eru nauðsynlegir fyrir skýrsluna sem þú ert að búa til.
3. Búðu til skipurit sem inniheldur skýrslugerðarhnút fyrir hvert fyrirtæki sem þú notar í samstæðuskýrslum.

> [!TIP]
> Nánari upplýsingar um hvernig á að búa til og stjórna línuskilgreiningum, dálkskilgreiningum og skipuritum er að finna í [Fjárhagsskýrsluhlutar](../../fin-ops-core/dev-itpro/analytics/financial-report-components.md).

Eftirfarandi skýringarmynd sýnir hvernig hægt er að nota skilgreiningu skipurits í Financial reporting til að greina hvert fyrirtæki sem verður sameinað.

![Skilgreining skipurits.](./media/reporting-tree-definition.png "Skilgreining skipurits")

Eins og samstæðuskýrslan á eftirfarandi skýringarmynd sýnir, þegar skipurit er notað saman með skýrsluskilgreiningu, er hægt að skoða hvert fyrirtæki sérstaklega. Sameinaðar upphæðir eru sýndar á samantektarstiginu.

![Sameina fjárhæð yfirlitsstigs.](./media/consolidate-amount-summary-level.png "Sameina fjárhæð yfirlitsstigs")

Einnig er hægt að búa til skipurit á mörgum stigum sem inniheldur eins mörg stig og þörf er á. Eftirfarandi skýringarmynd sýnir skilgreiningu skipurits á mörgum stigum sem hefur samantekt eftir heimssvæði.

![Margþrepa skilgreining á skýrslugerðartré með samantekt eftir svæðum.](./media/multilevel-reporting-tree-definition-roll-ups-worldwide-region.png "Margþrepa skilgreining á skýrslugerðartré með samantekt eftir svæðum")

Eftirfarandi skýringarmynd sýnir skilgreiningu skipurits á mörgum stigum sem hefur samantekt eftir virkni.

![Margþrepa skilgreining á skýrslugerðartré með samantekt eftir aðgerð.](./media/multilevel-reporting-tree-definition-roll-ups-by-function.png "Margþrepa skilgreining á skýrslugerðartré með samantekt eftir aðgerð")

### <a name="viewing-companies-side-by-side"></a>Fyrirtæki skoðuð hlið við hlið
Margir viðskiptavinir vilja fá skýrslur þar sem fyrirtækin birtast hlið við hlið, og þar sem dálkur sýnir uppsafnaða samtölu. Auðvelt er að ná þessu sniði þegar skipuritið hefur verið búið til. Hér eru skrefin á hærri stigum til að skoða fyrirtæki hlið við hlið á samstæðureikningsskilum.

1. Búðu til dálkskilgreiningu sem inniheldur dálk **Fjárhagsvíddar** fyrir hvert fyrirtæki.
2. Notaðu reitinn **Eining skipurits** til að velja tréð og einingu skipurits fyrir hvern dálk.
3. Valfrjálst: Bæta við fyrirsögnum og samtöludálkum.

Eftirfarandi skýringarmynd sýnir dálkskilgreiningu í hlið við hlið sniði.

![Dálkaskilgreining í hlið við hlið-sniði.](./media/column-definition-side-by-side-format.png "Dálkaskilgreining í hlið við hlið-sniði")

## <a name="consolidations-that-use-organization-structures-that-are-created-from-legal-entities"></a>Samstæður sem nota skipulag fyrirtækis sem er búið til út frá lögaðilum
Stigveldi fyrirtækis sem inniheldur víddir eða lögaðila búa til gagnvirkt skilgreiningar skipurits í fjárhagsskýrslugerð. Auðveld leið til að einfalda samstæður er að bæta stigveldi fyrirtækis við skýrsluna þína í Financial reporting. Á grundvelli skýrsludagsetningar mun Financial reporting velja stigveldi fyrirtækis á eða fyrir gildistökudag, eins og sýnt er á eftirfarandi skýringarmynd.

![Gagnvirkt stofna skilgreiningu skipurits.](./media/dynamically-create-reporting-tree-definitions.png "Gagnvirkt stofna skilgreiningu skipurits")

## <a name="consolidations-that-involve-eliminations"></a>Samstæður sem fela í sér losun
Losunarfærslur eru algengur hluti samstæðuferlisins. Í þessu dæmi eru fimm lyklar losaðir við samstæðu: 142600, 211400, 401420, 401180 og 510820. Fyrirtæki gætu sett upp lyklana sína innan samstæðu á annan hátt. Til dæmis velja sum fyrirtæki síðasta tölustafinn sem 9 ef lykillinn er notaður í færslum innan samstæðu. Óháð aðferðinni, ef þú þekkir lyklana innan samstæðu, geturðu sýnt losanir á samstæðureikningsskilum.

Eftirfarandi skýringarmynd sýnir dálkskilgreiningu fyrir sameinaðan rekstrarreikning. Þrír rekstrarreikningar innan samstæðu eru skilgreindir fyrir hvert fyrirtæki með því að nota víddarsíuna. Dálkar F, G og H innihalda aðeins losunarlykla fyrir USMF, USRT og DEMF fyrirtæki. Þessir dálkar eru settir upp þannig að þeir eru **ekki** prentaðir á fjárhagsskýrsluna.

![Dálkaskilgreining samstæðureikningsskila.](./media/column-definition-consolidated-income-statement.png "Dálkaskilgreining samstæðureikningsskila")

Þegar skýrslan er mynduð eru losunarupphæðir reiknaðar í dálkum F, G og H, og þær eru teknar saman í dálki I. Dálkur J sýnir sameinaða upphæð. Þessar samstæðuupphæðir útiloka losanir fyrir USMF-, USRT- og DEMF-fyrirtækin.

> [!TIP]
> Búðu til aðra skýrslu sem sýnir aðeins losunarfærslur og notaðu hana í skýrsluhóp sem inniheldur sameinuðu skýrsluna þína. Þannig hefur þú allar nauðsynlegar upplýsingar til að búa til allar færslur í færslubók sem þörf er á.

Eftirfarandi skýringarmynd sýnir sameinuðu skýrsluna.

![Rekstrarreikningur sameinaðrar skýrslu.](./media/consolidated-report-income-statement.png "Rekstrarreikningur sameinaðrar skýrslu")

Hvort sem þú notar lykla, víddir eða bæði, gerir Financial reporting þér kleift að sía út losunarfærslur með möguleika á því að sía eftir vídd.

## <a name="minority-interest"></a>Hlutdeild minnihluta
Fyrirtæki kann að eiga aðeins hluta af öðru fyrirtæki. Við þessar aðstæður, þegar þú býrð til sameinaða skýrslu, er mikilvægt að þú takir eingöngu tillit til þess hlutfalls sem fyrirtækið á. Financial reporting getur sýnt hlutdeild minnihluta með ýmsum hætti, fer eftir kjörstillingu notanda. Ein leið er að nota samantekið hlutfall í skilgreiningu skipurits. Önnur leið er að sýna minnihlutaeign sem aðskilda línu í skýrslu.

### <a name="using-the-reporting-tree-definition"></a>Nota skilgreiningu skipurits
Í skilgreiningu skipurits skal slá inn hlutfall eignarhalds í dálknum **Samantekin %** (dálki H), eins og sýnt er á eftirfarandi skýringarmynd. Þegar skýrslan er búin til verður þetta hlutfall notað til að reikna út sameinuðu upphæðina. Í þessu dæmi á Contoso aðeins 80 prósent af Contoso í Þýskalandi. Þú getur slegið inn annaðhvort **80** eða **.8** í dálknum **Samantekin %** og 80 prósent verða tekin saman upp á samstæðustigið.

> [!NOTE]
> Þú getur notað þetta eignarhlutfall í hvaða skýrslugerðareiningu sem er, ekki bara á fyrirtækjastigi. 

![Nota skilgreiningarprósentu skipurits.](./media/Using-reporting-tree-definition-percentage.png "Nota skilgreiningarprósentu skipurits")

Þegar skýrslan er búin til birtir skýrslan um Contoso Þýskaland 100 prósent af söluupphæðinni og 80 prósent af upphæðinni verður úthlutað og tekin saman upp á samstæðustig fyrir sölu.

Ef þú átt minna en 1 prósent í fyrirtæki getur þú valið gátreitinn **Leyfa samantekt minni en 1%** í flipanum **Viðbótarvalkostir** á síðunni **Skýrslustillingar** eins og sýnt er á eftirfarandi skýringarmynd. Í þessu tilviki verða gildi í dálknum **Samantekin %** í skipuritinu meðhöndluð sem minna en 1 prósent. Ef þú til dæmis slærð inn **.8** verður 0,8 prósent tekið saman upp á samstæðustigið, ekki 80 prósent. Að öðrum kosti getur þú fengið sömu niðurstöðu með því að skilja gátreitinn **Leyfa samantekt minni en 1%** eftir auðan og slá inn **.008** í dálkinn **Samantekin %**.

![Valkostir skýrslugerðarstillinga.](./media/reporting-setting-options.png "Valkostir skýrslugerðarstillinga")

### <a name="showing-ownership-as-a-separate-row-on-the-consolidated-report"></a>Sýnir eignarhald sem aðskilda línu í sameinuðu skýrslunni
Annar möguleiki fyrir minnihlutahópa er að sýna 100 prósent af dótturfélaginu fyrir hverja línu í skýrslunni en draga minnihlutann frá nettótekjum.

Eins og fram kemur á eftirfarandi skýringarmynd er hægt að nota **IF THEN ELSE** fullyrðingu og dálktakmörkun í línuskilgreiningunni til að reikna út hlutdeild minnihlutans í fjárhagsskýrslum.

![Sýnir eignarhald sem aðskilda línu í sameinuðu skýrslunni.](./media/Showing-ownership-separate-row-consolidated-report.png "Sýnir eignarhald sem aðskilda línu í sameinuðu skýrslunni")

## <a name="multiple-charts-of-accounts-across-legal-entities"></a>Margar bókhaldslyklar yfir lögaðila
Oft hafa ólíkir lögaðilar ólíka bókhaldslykla en vilja samt búa til samstæðureikningsskil. Við þessar aðstæður er hægt að nota Financial reporting til að sameina gögnin, svo að þú getir búið til fjárhagsskýrslur. Hér eru hástigs skrefin til að sameina þegar ólíkir bókhaldslyklar eru til yfir lögaðila.

1. Búðu til línuskilgreiningu sem hefur marga tengla við fjárhagsvíddir. Það ætti að vera einn tengill fyrir hvern bókhaldslykil.
2. Notaðu takmörkun skýrslugerðareiningar í dálkskilgreiningunni til að úthluta hvert fyrirtæki í viðeigandi dálk.


Hægt er að bæta mörgum tenglum fjárhagsvídda við hverja línu í línuskilgreiningunni fyrir alla einkvæma bókhaldslykla fyrirtækis. Í eftirfarandi skýringarmynd notar USMF-fyrirtækið reikningasafnið í fyrsta dálknum **Tengill í fjárhagsvíddir** (dálkur J) og DEMF-fyrirtækið notar lyklana í seinni dálknum **Tengill í fjárhagsvíddir** (dálkur K).

> [!TIP]
> Nánari upplýsingar um hólfið **Tengill í fjárhagsvíddir** er að finna í Tilgreina tengil í hólf fjárhagsvíddar.

![Velja fyrsta tengil reikninga í fjárhagsvídd.](./media/set-accounts-first-Link-to-Financial-Dimensions.png "Veldu fyrsta tengil reikninga í fjárhagsvídd")

Hægt er að nota skipurit til að skilgreina hvaða tengill í fjárhagsvíddir úr línuskilgreiningunni er notaður með hverju fyrirtæki fyrir sig. Veldu línuskilgreiningu í dálki E, og veldu síðan viðeigandi línutengil í dálki F, eins og sýnt er á eftirfarandi skýringarmynd.

![Skilgreining á línu fjárhagsvíddar notuð.](./media/link-financial-dimensions-row-definition-used.png "Skilgreining á línu fjárhagsvíddar notuð")

> [!TIP]
> Þegar þú býrð til tengla við fjárhagsvíddir skaltu nota lýsinguna til að bera kennsl á þau fyrirtæki sem hver tengill á við. Þannig getur þú auðveldlega valið rétt fyrirtæki þegar þú stofnar skipurit. Í dálkskilgreiningunni leyfir reiturinn **Skýrslueining** þér að takmarka hvern dálk við einingu í skipuritinu svo þú getir skoðað gögn hlið við hlið. Ef þú gefur ekki upp tiltekið fyrirtæki fyrir dálk verða sameinuð gögn sýnd fyrir öll fyrirtæki.

## <a name="different-fiscal-calendars-across-multiple-legal-entities"></a>Mismunandi fjárhagsdagatöl yfir marga lögaðila
Mismunandi lögaðilar gætu haft mismunandi fjárhagsdagatöl en þurfa samt ennþá að búa til samstæðureikningsskil. Það eru tvær leiðir til að sameina þegar mismunandi fjárhagstímabil eru fyrir hendi hjá lögaðilum:

- Búðu til dálkskilgreiningu og notaðu tímabilið og árið til að varpa viðeigandi tímabilum fyrir hvert fyrirtæki.
- Í **Stillingar** \> **Annað** \> **Aukavalkostir**, veldu hvort eigi að sameina með því að nota lokadag tímabils eða númer tímabils.

Þegar þú hannar dálkskilgreiningu fyrir mörg fyrirtæki með mismunandi fjárhagstímabilum er mikilvægt að þú íhugir hvaða fyrirtæki verði úthlutað í reitinn **Nafn fyrirtækis** í skýrsluskilgreiningunni. Fjárhagsdagatal fyrirtækis verður notað sem grunnfjárhagsdagatal fyrir skýrsluskilgreininguna. Til dæmis sýnir eftirfarandi tafla fjárhagstímabils sem var sett upp fyrir USMF- og INMF-fyrirtækin. Fyrir sameinaðar skýrslur viltu nota fjárhagsdagatal sem USMF notar. „Vörpunar“dálkurinn sýnir sambærilegt tímabil og ár fyrir hvert fyrirtæki ef skýrsla er búin til fyrir 30. júní 2018.

| Fyrirtæki   | Fjárhagsár                                  | Vörpun                     |
|-----------|----------------------------------------------|-----------------------------|
| USMF      | Fjárhagsár, 1. júlí til 30. júní          | Tímabil 12, fjárhagsár 2018 | 
| INMF      | Almanaksár, 1. janúar til 31. desember | Tímabil 6, fjárhagsár 2018  |

Í eftirfarandi skýringarmynd er USMF-fyrirtæki tilgreint í reitnum **Heiti fyrirtækis** í skýrsluskilgreiningunni. Þess vegna verður fjárhagsdagatal USMF-fyrirtækisins notað sem grunnfjárhagsdagatal. Í þessu dæmi, þegar skýrsla er búin til fyrir 30. júní 2018, mun USMF-fyrirtækið nota GRUNNtímabilið, sem er skilgreint sem tímabil 12 í skýrsluskilgreiningunni. INMF-fyrirtækið mun nota GRUNN-6, sem er tímabil 6. Báðir dálkar munu innihalda gögn fyrir júní 2018.

![Grunntímabil skýrslu.](./media/report-base-period.png "Grunntímabil skýrslu")

Eftirfarandi skýringarmynd sýnir valkosti í skýrsluskilgreiningu sem leyfir þér að velja hvort númer eða lokadagur tímabils er notað fyrir samstæðuna.

![Valkostir fyrir númer tímabils í skýrsluskilgreiningu.](./media/options-report-definition-period-number.png "Valkostir fyrir númer tímabils í skýrsluskilgreiningu")

## <a name="business-unit-consolidations"></a>Samstæður viðskiptaeiningar
Þessi grein hefur lagt áherslu á að nota skilgreiningu skipurits og stigveldi fyrirtækis í Financial reporting með samstæður í huga. Einnig er hægt að nota skipurit til að búa til skýrslur um samstæður viðskiptaeininga, svo sem skýrslur um sölu eða rekstur á heimsvísu. Þessar skýrslur eru algengar kröfur. Til að búa þær til skaltu velja fyrirtæki og vídd fyrir hverja einingu sem þú vilt sameina. Til dæmis, í eftirfarandi skýringarmynd, en samantekt á viðskiptaeiningu gerð með því að endurtaka hvert fyrirtæki í dálknum **Fyrirtæki** (dálkur A) og að greina hóp af víddargildum deildar á hvert fyrirtæki í dálknum **Víddir** (dálkur D).

![Skýrslur um samstæðu viðskiptaeiningar.](./media/business-unit-consolidation-reports.png "Skýrslur um samstæðu viðskiptaeiningar")

## <a name="consolidations-that-involve-multiple-reporting-currencies"></a>Samstæður sem fela í sér marga skýrslugjaldmiðla
Financial reporting býður upp á aukinn sveigjanleika þegar þú skoðar raungögn, gögn fjárhagsáætlunar, gögn fjárhagsáætlunarstýringar og gögn fjárhagsáætlunargerðar í mörgum gjaldmiðlum. Með því að færa yfir lykiluppsetningargögn þarftu ekki að gera neinar viðbótaruppsetningar í Financial reporting til að skoða hvaða skýrslu sem er, í hvaða gjaldmiðli sem er, hvenær sem er, fyrir hvaða notanda sem er.

### <a name="prerequisites"></a>Frumskilyrði
Til að reikna rétta út umreiknaðar stöður gerir Financial reporting kröfu um að flokknum **Lykill óráðstafaðs eigin fjár** sé úthlutað á lykli óráðstafaðs eigin fjár í listanum **Aðallykill**. Financial reporting styður ekki að bókað sé í lykli óráðstafaðs eigin fjár. Ef færslurnar eru bókaðar í lykli óráðstafaðs eigin fjár munu umreiknuðu stöðurnar ekki reiknast rétt. Við mælum með því að notendur setji upp aukalegan lykil óráðstafaðs eigin fjár til að bóka leiðréttingar í lykli óráðstafaðs eigin fjár.

Í aðallyklinum verða reitirnir **Gerð gengis fyrir fjárhagsskýrslugerð** og **Umreikningsgerð gjaldmiðils** í flýtiflipanum **Fjárhagsskýrslugerð** að vera stilltir fyrir hvern lykil fyrir sig eins og sýnt er á eftirfarandi skýringarmynd. Þú getur lokið þessu verkefni frá einum lykli til annars, eða þú getur notað lyklasniðmátin til að auðveldlega rúlla breytingum áfram.

- Í reitnum **Gerð gengis fyrir fjárhagsskýrslu** skal velja gerð gengis sem inniheldur gjaldmiðla og gengi til að nota fyrir lykilinn. Þessi tafla gjaldmiðla og gengis verður notuð fyrir raunveruleg gögn í Financial reporting.
- Í reitnum **Umreikningsgerð gjaldmiðils** skal velja aðferðina sem er notuð til að reikna út gengi fyrir lykilinn. Þessi gjaldmiðilsaðferð er notuð bæði fyrir raunveruleg gögn og gögn fjárhagsáætlunar í Financial reporting.

![Aðallyklar fjárhagsskýrslugerðar.](./media/Financial-reporting-main-accounts.png "Aðallyklar fjárhagsskýrslugerðar")

Fyrir gögn fjárhagsáætlunar, fjárhagsáætlunarstýringar og fjárhagsáætlunargerðar er gerð gengis skilgreint á síðunni **Fjárhagur**. Sú tafla verður notuð til að kalla fram gengin og umreikningsgerð gjaldmiðils sem er úthlutað á lykilinn verður notuð.

### <a name="currency-translation-methods"></a>Aðferðir við umreikning gjaldmiðils
Það eru fjórar leiðir til að reikna gengi í Financial reporting:

- **Vegið meðaltal** - Þessi aðferð er notuð oftast fyrir rekstrarreikninga. Hún notar eftirfarandi formúlu:

    (Gengi × dagar í gildi) ÷ dagar í tímabili

- **Meðaltal** - Þessi aðferð er önnur aðferð fyrir rekstrarreikninga. Hún notar eftirfarandi formúlu:

    Samtals gengi ÷ fjöldi gengja

- **Núgildandi** - Þessi aðferð er notuð oftast fyrir efnahagslykla. Gengið sem er notað er gengið á eða fyrir dagsetningu skýrslunnar eða dálksins í Financial reporting.
- **Færsludagsetning** - Þessi aðferð er notuð fyrir eignareikninga. Gengið sem er notað er gengið á þeim degi sem eignin var keypt. Ef gengi er ekki skráð fyrir þann dag, er undanfarandi gengi sem var skráð næst kaupdegi eignar notað.

### <a name="report-designer-options-for-currency-translation"></a>Valkostir skýrsluhönnunar fyrir umreikning gjaldmiðils
Í Financial reporting má sjá hvaða skýrslu sem er í hvaða fjölda skýrslugjaldmiðla sem er. Eftirfarandi reitir í skýrsluskilgreiningunni styðja þessa getu:

- Kafli **Gjaldmiðilsupplýsinga** á síðunni **Skýrsluskilgreiningar**. Þessi kafli sýnir gjaldmiðilinn sem gildin eru sýnd í þegar skýrsla er búin til.
- Nýr **Taka með alla skýrslugjaldmiðla** gátreitur. Þegar þessi gátreitur er valinn verður skýrslu fyrir hvern skýrslugjaldmiðil bætt við skýrsluröðina eftir að skýrslan sem notar virka gjaldmiðil fyrirtækisins er búin til. Ef gátreiturinn er hreinsaður geturðu samt valið skýrslugjaldmiðil í vefskoðaranum. Í þessu tilviki verður aðeins unnið úr skýrslugjaldmiðlinum þegar þú velur hann.

Valkostirnir í skýrsluskilgreiningunni auðvelda þér að umreikna skýrslu í alla skýrslugjaldmiðlana þína. Þess vegna gæti verið að þú getir fjarlægt tvítekna skýrsluskilgreiningu þar sem munurinn liggur í gjaldmiðlunum sem eru notaðir. Ef þú þarft skýrslu sem sýnir marga gjaldmiðla hlið við hlið getur þú haldið áfram að nota reitinn **Birtingarmynd gjaldmiðils** á síðunni **Dálkskilgreining** til að umreikna aðeins þann dálk skýrslunnar í annan skýrslugjaldmiðil.

### <a name="currency-translation-adjustment"></a>Leiðrétting á umreikningi gjaldmiðils
Leiðrétting á umreikningi gjaldmiðils (CTA) er munurinn á gengjunum sem eru notuð til að reikna út efnahagslykla og genginu sem notað er í rekstrarreikninga. Þessi munur veldur því að mismunur verður á efnahagslyklum. Þú getur notað Financial reporting til að reikna út CTA á tvenna vegu:

- Notaðu síðuna **Sléttunarleiðréttingar** í línuskilgreiningunni eins og sýnt er á eftirfarandi skýringarmynd.

    ![Sléttunarleiðréttingar á leiðréttingu á umreikningi gjaldmiðils.](./media/Currency-translation-adjustment-rounding-adjustments.png "Sléttunarleiðréttingar á leiðréttingu á umreikningi gjaldmiðils")

    Þegar þú tilgreinir línu sem ætti að sýna sléttunarleiðréttinguna (CTA), línu heildareigna, línu heildarskulda og eigin fjár, og mörkin sem þér líður vel með, mun Financial reporting reikna út mismuninn og koma honum fyrir í æskilegri línu. Lína sem heitir **Sléttunarleiðréttingar** verður búin til og sýnd við köfun eins og sýnt er á eftirfarandi skýringarmynd.

    ![Köfun sléttunarleiðréttingar.](./media/rounding-adjustment-drill-down.png "Köfun sléttunarleiðréttingar")

- Koma öllum lyklum fyrir á bili, frá eignum til útgjalda. Eins og sést á eftirfarandi skýringarmynd verður munurinn sama upphæð og upphæð sléttunarleiðréttingarinnar (CTA). Þess vegna er hægt að nota það sem athugun á heildarupphæð til að tryggja að síða sléttunarleiðréttingar sé ekki með neinar lyklastöður sem gleymdust.

    ![Athugun á skjámynd sléttunarleiðréttingar.](./media/rounding-adjustment-form-check.png "Athugun á skjámynd sléttunarleiðréttingar")

### <a name="balance-calculation-approach"></a>Nálgun á stöðuútreikningi
Til að fá rétt umreiknaðar upphæðir þegar gjaldmiðlar eru notaðir, notar Financial reporting eftirfarandi útreikningsaðferðir fyrir stöðurnar:

- **Vegið meðaltal og meðaltal** - Hvert tímabil er reiknað við vegið meðaltal þess og er lagt saman fyrir dálka eins og ársfjórðung og það sem af er ári.
- **Sögulegur** - Allir lyklar sem nota sögulegar aðferðir við umreikninga fara alltaf aftur til baka á færsludagsetningu. Ef kaupdagur tengist færslunni er sú dagsetning notuð til að fá gengið. Hvert tímabil er síðan lagt saman og geymt til að bæta útreikningstímann.
- **Núgildandi** - Reiknaðir dálkar og samtöludálkar, svo sem dálkar fyrir ársfjórðung og það sem af er ári eru reiknaðir á gengi þeirrar stundar sem ákvarðast í dálknum eða skýrslunni. Til dæmis mun dálkurinn **Ársfjórðungur 1** nota gengið þann 31. mars ef almanaksár er notað.

## <a name="additional-resources"></a>Frekari upplýsingar

Nánari upplýsingar um samstæðuumreikning og umreikning gjaldmiðils er að finna í yfirefni þessarar greinar, [Yfirlit yfir fjárhagssamstæður og umreikninga gjaldmiðils](./financial-consolidations-currency-translation.md).

Nánari upplýsingar um hvernig á að slá inn upplýsingar um samstæður á netinu er að finna í [Sameiningar fjárhags á netinu](./consolidate-online.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
