---
title: Algengar spurningar um birgðakostnað
description: Þetta efni svarar nokkrum algengum spurningum um birgðakostnað í Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 05/03/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-05-03
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 45f65bd4a5cfb9bd0c4eb03ceb56eca452f6ec95
ms.sourcegitcommit: cbe9493d479f96f271d94599ec1b85131b26169f
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/27/2022
ms.locfileid: "8809304"
---
# <a name="inventory-costing-faq"></a>Algengar spurningar um birgðakostnað

[!include [banner](../includes/banner.md)]

Þetta efni svarar nokkrum algengum spurningum um birgðakostnað í Microsoft Dynamics 365 Supply Chain Management.

## <a name="inventory-close-adjustments-and-recalculation"></a>Birgðalokun, leiðréttingar og endurútreikningur

### <a name="is-the-inventory-close-required"></a>Er þörf á lokun birgða?

Ef þú ætlar að nota birgðageymslueiginleikann er birgðalokun nauðsynleg. Ef þú ætlar ekki að nota birgðageymslueiginleikann, mælum við eindregið með því að þú keyrir birgðann áfram, óháð kostnaðarlíkönunum sem þú notar.

### <a name="how-often-should-the-inventory-close-be-run"></a>Hversu oft ætti að keyra birgðalokun?

Birgðalokun ætti að keyra að minnsta kosti einu sinni á hvert fjárhagstímabil. Til dæmis, ef fjárhagsdagatalið þitt er stillt á almanaksmánuð byggt á fjárhagsdagatali, ættir þú að keyra birgðalokunina einu sinni í mánuði.

### <a name="is-the-inventory-recalculation-required"></a>Er þörf á endurútreikningi birgða?

Nei, ekki er þörf á endurútreikningi birgða. Ef þú notar reglubundið kostnaðarlíkan eins og fyrst inn, fyrst út (FIFO), síðast inn, fyrst út (LIFO) eða vegið meðaltal, ættir þú að íhuga vandlega hvort þú munt keyra endurútreikning birgða. Það getur veitt nákvæmari kostnaðaráætlun í heuristic módelunum sem þú hefur valið.

### <a name="how-often-should-the-inventory-recalculation-be-run"></a>Hversu oft ætti að keyra endurútreikning birgða?

Ef þú ætlar að keyra endurútreikning birgða, mælum við með að þú íhugir að keyra hana daglega sem runuferli. Ef fyrirtæki þitt krefst ekki tíðrar skýrslugerðar um birgðagildi fyrir reglubundin kostnaðarlíkön, geturðu íhugað að keyra birgðaútreikning sjaldnar.

### <a name="when-should-i-use-the-on-hand-inventory-adjustment-on-the-closing-and-adjustments-page"></a>Hvenær ætti ég að nota birgðaleiðréttinguna á síðunni Lokun og leiðréttingar?

Aðeins er hægt að keyra leiðréttingu á lagerbirgðum eftir að birgðalokun er lokið. Það er venjulega keyrt fyrir dagsetninguna eftir síðustu lokun. Leiðréttingin á lager getur aðeins breytt birgðum sem eru enn til staðar frá og með þeim degi þegar þú keyrir leiðréttinguna.

### <a name="when-should-i-use-the-inventory-transaction-adjustment-on-the-closing-and-adjustments-page"></a>Hvenær ætti ég að nota birgðafærsluleiðréttingu á síðunni Lokun og leiðréttingar?

Þú ættir að nota birgðafærsluleiðréttinguna áður en þú keyrir birgðalokun. Það er venjulega notað til að leiðrétta ranga kvittun. Ekki er hægt að bóka leiðréttingu birgðafærslu eftir að birgðalokun hefur verið keyrð og færslan er jöfnuð.

### <a name="are-purchase-order-returns-treated-like-other-issues-during-the-inventory-close"></a>Er skil á innkaupapöntunum meðhöndluð eins og önnur mál við lokun birgða?

Já. Innkaupapöntunarkvittun er útgáfa sem er jöfnuð við innhreyfingu í heuristic líkaninu sem þú velur fyrir vöruna. Ef þú ert að nota reglubundið kostnaðarlíkan geturðu notað merkingu til að hnekkja vitlausum kostnaði.

### <a name="what-happens-to-sales-order-returns-during-the-inventory-close"></a>Hvað verður um skil á sölupöntunum við lokun birgða?

Þegar þú keyrir birgðalokunina er sölupöntunarskil meðhöndluð sem kvittun í birgðum. Útgáfur eru jafnaðar á móti birgðum, byggt á heuristic líkaninu sem þú velur fyrir vöruna.

### <a name="what-cost-price-is-used-on-a-sales-order-return"></a>Hvaða kostnaðarverð er notað við skil á sölupöntun?

Þegar þú býrð til skil sem tengist sölupöntun, gildir **Einingaverð** reiturinn er afritaður úr upprunalegu sölupöntuninni og **Skilakostnaðarverð** reiturinn á skilunum er stilltur á leiðrétt kostnaðarverð frá upprunalegu birgðafærslunni fyrir sölupöntunarlínuna sem verið er að skila. Ef **Gildi opið** valkostur fyrir tengda birgðafærslu er stilltur á *Já*, getur birgðalokun valdið uppfærslum á útgáfukostnaði á upprunalegu sölupöntuninni. The **Skilakostnaðarverð** reiturinn er ekki uppfærður í þessari atburðarás. Hins vegar, þegar þú bókar fylgiseðil fyrir skilapöntun, mun kerfið athuga kostnaðarverðið og nota uppfærðan kostnað á skilabirgðafærslunni.

Fyrir skil á staðlaðri kostnaðarvöru sem tengist sölupöntun mun kerfið nota staðalkostnað frá upphaflegu sölupöntuninni, jafnvel þótt nýr staðalkostnaður sé virkur fyrir vöruna.

Þegar þú býrð til skil sem er ekki tengd sölupöntun, **Skilakostnaðarverð** reiturinn er stilltur á virka vöruverðið sem þú hefur fyrir vöruna á síðunni sem þú ert að búa til skilapöntun fyrir. Ef þú ert ekki með virkt kostnaðarverð í kostnaðarútgáfu fyrir vöruna verður gildið 0 (núll). Ef þú skilur gildið eftir sem 0 (núll), færðu viðvörun sem segir að skilalotaauðkenni eða skilakostnaðarverð sé ekki tilgreint.

### <a name="what-is-the-expected-performance-of-the-inventory-close"></a>Hver er væntanleg frammistaða birgðalokunar?

Margir þættir geta haft áhrif á frammistöðu birgðalokunar. Þessir þættir innihalda heildarfjölda vara, heildarfjölda færslna á tímabilinu, birgðalíkönin sem þú notar og fjölda runuhjálpar sem þú stillir í birgða- og vöruhúsastjórnunarfæribreytum. Þú getur búist við því að lokunin gæti tekið allt að nokkrar mínútur eða allt að nokkrar klukkustundir. Það eru engar sérstakar leiðbeiningar um þann tíma sem lokunin ætti að taka að keyra. Þú ættir að skilgreina óvirkar viðskiptakröfur þínar fyrir frammistöðu birgðalokunar og vinna náið með samstarfsaðila þínum til að skilgreina áætlun um að keyra birgðalokunarferlið. Ef þú finnur fyrir óvænt lítilli frammistöðu birgðalokunarferlisins ættir þú að opna stuðningsmiða.

## <a name="costing-sheet-and-indirect-costs"></a>Kostnaðarblað og óbeinn kostnaður

### <a name="which-costing-models-support-the-costing-sheet"></a>Hvaða kostnaðarlíkön styðja kostnaðarblaðið?

Þó að kostnaðarblaðið sé oftast notað í fyrirtækjum sem nota staðlaða kostnaðarútreikning, þá er hægt að nota það með hvaða kostnaðarlíkan sem er sem er til í Supply Chain Management.

### <a name="can-i-have-multiple-costing-sheets-for-various-parts-of-my-organization"></a>Get ég haft mörg kostnaðarblöð fyrir ýmsa hluta fyrirtækisins?

Nr. Þú getur aðeins haft eitt kostnaðarblað á hvern lögaðila.

### <a name="can-i-have-different-costing-sheets-for-each-site"></a>Get ég haft mismunandi kostnaðarblöð fyrir hverja síðu?

Nei, þú getur ekki haft mismunandi kostnaðarblað fyrir hverja síðu. Þú getur aðeins búið til eitt kostnaðarblað fyrir hvern lögaðila. Hins vegar er hægt að stilla heildarhnúta, kostnaðarhópa eða óbeina kostnaðarhnúta á hverja síðu. Þessi uppsetning er handvirkt ferli og þú verður að viðhalda stigveldinu og vöruúthlutunum á kostnaðarblaðinu þegar skipulags- eða rekstrarbreytingar eiga sér stað. Ef ein vara er framleidd eða keypt á fleiri en einni síðu er engin aðferð sem gerir þér kleift að meðhöndla vöruna á annan hátt á kostnaðarblaðinu fyrir hverja síðu. Athugaðu að auki að allir óbeinn kostnaðarkóðar eru með taxta eða aukagjald sem er skilgreint í kostnaðarútgáfunni þinni. Kostnaðurinn sem þú skilgreinir er alltaf staðbundinn.

### <a name="can-i-deactivate-and-activate-versions-of-the-costing-sheet"></a>Get ég slökkt á og virkjað útgáfur af kostnaðarblaðinu?

Þó að engin nákvæm útgáfusaga sé geymd fyrir kostnaðarblaðið, getur þú gert breytingar á kostnaðarblaðinu og síðan, þegar þú ert tilbúinn, vistað og staðfest það. Það er engin aðferð sem gerir þér kleift að fara aftur í eldri útgáfu af kostnaðarblaðinu eða skoða breytingarnar sem voru gerðar á kostnaðarblaðinu. Ef þú byrjar breytingar og vilt ekki að þær taki gildi geturðu lokað síðunni án þess að vista og staðfesta breytingarnar. Þú verður beðinn um að henda breytingunum.

### <a name="can-i-create-indirect-costs-for-each-item"></a>Get ég búið til óbeinan kostnað fyrir hvern hlut?

Á kostnaðarblaðinu þínu geturðu búið til óbeina kostnaðarkóða þar sem **Tegund hnúts** reiturinn er stilltur á *Aukagjald*, *·*, eða *Byggt á úttakseiningu*. Þú getur síðan skilgreint gjaldið eða álagið þannig að það sé sérstakt fyrir vörunúmer. Á **Gefa** eða **Aukagjald** Flýtiflipi, bættu línu við hnitanetið. Stilltu **Gildir fyrir** sviði til *Tafla* og **Tengsl** reit við tiltekið vörunúmer.

### <a name="can-i-create-an-indirect-cost-that-isnt-related-to-a-specific-item"></a>Get ég búið til óbeinan kostnað sem tengist ekki tiltekinni vöru?

Já. Þú getur búið til óbeinan kostnaðarkóða þar sem **Tegund hnúts** reiturinn er stilltur á *Byggt á úttakseiningu*. Þú getur þá stillt **Undirgerð** sviði til *Magn*, *·*, eða *Bindi* til að tilgreina magn, þyngd eða rúmmál vörunnar sem þú ert að framleiða. Gengið sem þú tilgreinir á **Gefa** Flýtiflipi verður notaður á undirgerðina sem þú valdir. Til dæmis stillir þú **Undirgerð** sviði til *Magn* og **Gefa** sviði til *1.00 USD*, og stofnaðu síðan framleiðslu- eða runupöntun fyrir magnið 10. Í þessu tilviki er óbeini kostnaðurinn sem bætist við fullunna vöru 10.00 USD.

### <a name="can-i-use-the-costing-sheet-to-split-my-production-costs-by-hours-and-materials"></a>Get ég notað kostnaðarblaðið til að skipta framleiðslukostnaði mínum eftir klukkustundum og efni?

Já. Þú getur búið til **Samtals** hnúta á kostnaðarblaðinu þínu til að aðgreina kostnaðinn eftir hvaða flokkun sem þú velur. Til dæmis geturðu búið til einn **Samtals** hnút sem er nefndur *Klukkutímar* og annað sem nefnt er *Efni*. Undir **Klukkutímar** hnút, bættu við hverjum kóðahópi sem tengist tíma þínum. Undir **Efni** hnút, bættu við hverjum kostnaðarflokki sem tengist efninu þínu.

## <a name="dimension-groups"></a>Víddaflokkar

### <a name="can-i-manage-cost-at-the-batch-or-serial-number-level"></a>Get ég stjórnað kostnaði á lotu- eða raðnúmerastigi?

Já, ef þú ert að nota reglubundið kostnaðarlíkan eins og FIFO, LIFO, LIFO dagsetningu, vegið meðaltal eða vegið meðaltal dagsetningu, geturðu virkjað **Fjárhagsskrá** valkostur fyrir **Hópur** eða **Raðnúmer** vídd í rakningarvíddarhópnum til að rekja kostnað á nákvæmu stigi.

### <a name="can-i-manage-costs-at-the-location-level"></a>Get ég stjórnað kostnaði á staðsetningarstigi?

Nei, þú getur ekki virkjað **Fjárhagsskrá** valkostur fyrir **Staðsetning** vídd í geymsluvíddarhópnum. Ef fyrirtæki þitt verður að fylgjast með kostnaði á nákvæmara stigi skaltu íhuga hvort þú getir búið til sýndarvöruhús og veldu síðan **Fjárhagsskrá** valkostur fyrir **Vöruhús** vídd í geymsluvíddarhópnum þínum.

### <a name="should-i-enable-the-use-warehouse-management-processes-option-for-the-storage-dimension-group"></a>Ætti ég að virkja valkostinn Nota vöruhúsastjórnunarferli fyrir geymsluvíddarhópinn?

Ef þú heldur að þú gætir viljað nota háþróaða vöruhússtjórnunareiginleika í framtíðinni, ættir þú að virkja **Notaðu vöruhússtjórnunarferli** valmöguleika. Eftir að þú hefur vistað geymsluvíddarhóp geturðu ekki lengur breytt stillingum á **Notaðu vöruhússtjórnunarferli** valmöguleika fyrir það. Ef þú ákveður að nota vöruhúsastjórnunarferli síðar verður þú að búa til nýtt vöruhús þar sem valkosturinn er virkur. Það er ekkert sjálfvirkt ferli sem hægt er að nota til að færa allar birgðir frá einu vöruhúsi í annað vöruhús eða til að afrita tengdar stillingar í nýtt vöruhús.

### <a name="can-i-enable-the-use-warehouse-management-processes-for-the-storage-dimension-group-even-if-im-not-planning-to-use-advanced-warehousing"></a>Get ég virkjað Nota vöruhúsastjórnunarferli fyrir geymsluvíddarhópinn jafnvel þó ég ætli ekki að nota háþróaða vörugeymslu?

Já, jafnvel þótt þú ætlir ekki að nota háþróaða vöruhússtjórnunareiginleika, geturðu virkjað **Notaðu vöruhússtjórnunarferli** valkostur fyrir geymsluvíddarhópinn. Til að búa til og vinna úr færslum verður þú að klára lágmarksstillingu, svo sem frátekningarstigveldi og einingaraðahópa. Hins vegar eru stillingar fyrir háþróaða vörugeymslu almennt hunsuð þegar þú vinnur handvirkt úr tínslulistum, fylgiseðlum og vörukvittunum (til dæmis á sölupöntunar- og innkaupapöntunarsíðum).

### <a name="when-should-i-enable-the-physical-inventory-option-for-a-storage-or-tracking-dimension-group"></a>Hvenær ætti ég að virkja valkostinn Raunverulegar birgðir fyrir geymslu- eða rakningarvíddarhóp?

Þú ættir að virkja **Líkamsbirgðir** valkostur fyrir geymslu og rekja víddarhópa þegar þú verður að halda ítarlegar birgðaskrár byggðar á þeirri vídd. Venjulega verður hvaða vídd sem er virk líka rakin líkamlega. Þess vegna verða allar móttökur, útgáfur eða hreyfingar á birgðum raktar af völdum vídd. Ef vídd er ekki skylda (til dæmis númeraplötu) geturðu virkjað **Auð kvittun leyfð** og **Autt mál leyfilegt** valkostir til að leyfa notendum að taka á móti, gefa út eða færa birgðir jafnvel þegar víddin er ekki tilgreind.

### <a name="when-should-i-enable-the-financial-inventory-option-for-a-storage-or-tracking-dimension-group"></a>Hvenær ætti ég að virkja valkostinn Fjárhagsbirgðir fyrir geymslu- eða rakningarvíddarhóp?

Þú ættir að virkja **Fjárhagsskrá** valkostur fyrir geymslu og rekja víddarhópa þegar þú verður að halda ítarlegar fjárhagsskýrslur byggðar á þeirri vídd. The **Síða** víddir eru alltaf raktar fjárhagslega, en aðrar víddir eru valfrjálsar fyrir fjárhagslega rakningu. Ef þú notar reglubundið kostnaðarlíkan eins og FIFO, LIFO eða vegið meðaltal, sem gerir **Fjárhagsskrá** valkostur fyrir vídd gefur til kynna að þú munt aðeins gera uppgjör í þeim tilvikum þar sem kvittun og útgáfa hafa sömu víddargildi. Til dæmis, ef þú virkjar **Fjárhagsskrá** valkostur fyrir **Vöruhús** vídd muntu hafa mismunandi kostnað í hverju vöruhúsi og ekki er hægt að gera upp kvittanir og útgáfur frá mismunandi vöruhúsum.

### <a name="can-i-make-changes-to-a-product-storage-or-tracking-dimension-group-after-transactions-exist"></a>Get ég gert breytingar á vöru-, geymslu- eða rakningarvíddarhópi eftir að færslur eru til?

Eftir að þú hefur búið til vörulíkanahóp geturðu breytt stillingum á **Þekjuáætlun eftir vídd**, **kaupverð**, og **Fyrir útsöluverð** reiti ef **Virkur** gátreiturinn er valinn fyrir vídd í vörulíkanahópnum. Engar aðrar breytingar eru leyfðar. Til dæmis geturðu ekki virkjað eða slökkt á **Virkur**, **mál leyfilegt**, **kvittun leyfð**, **·**, og **Fjárhagsskrá** valkostir.

### <a name="can-i-change-the-product-storage-or-tracking-dimension-group-for-a-released-product"></a>Get ég breytt vöru-, geymslu- eða rakningarvíddarhópnum fyrir útgefna vöru?

Ef birgðastaðan fyrir vöru er 0 (núll), og **Gildi opið** valkostur er stilltur á *Nei* fyrir allar birgðafærslur er hægt að breyta geymslu- og rakningarvíddarhópum á útgefnum framleiðslusíðu. Ekki er hægt að breyta vöruvíddarhópnum eftir að færslan er búin til.

## <a name="item-model-groups"></a>Vörulíkanaflokkar

### <a name="when-should-i-enable-the-stocked-product-option"></a>Hvenær ætti ég að virkja valkostinn Birgðavöru?

Þú ættir að virkja **Birgð vara** valkostur fyrir hvaða hlut sem verður rakinn í birgðum þínum. Þegar þessi valkostur er virkur eru ítarlegar birgðafærslur geymdar sem fylgjast með móttöku og útgáfu vörunnar. Þessi valkostur er venjulega virkur fyrir hvaða áþreifanlega hluti sem þú geymir í vöruhúsinu þínu, til dæmis. Þú ættir líka að virkja þennan valmöguleika ef þú ætlar að bæta óáþreifanlegum hlut eins og þjónustuvöru við vörulista (uppskriftir) eða formúlur. Ef þú virkjar ekki **Birgð vara** valkostur, engar birgðafærslur eru raktar í birgðaundirbókinni og kostnaður við hlutina er venjulega gjaldfærður í aðalbókina þína. Þessi valkostur er oft notaður, til dæmis, fyrir verslunarvörur eða þjónustu sem eru ekki innifalin í uppskriftum þínum eða formúlum.

### <a name="when-should-i-enable-the-post-physical-inventory-option"></a>Hvenær ætti ég að virkja valkostinn Bóka efnislegar birgðir?

The **Bókaðu efnislegar birgðir** valmöguleikinn er venjulega virkur þegar **Birgð vara** valmöguleikinn er virkur. Þegar þú virkjar þennan valkost mun kerfið rekja líkamlega uppfærslu á vörunni í birgðafærslunni. Þessi valkostur er notaður í samræmi við færibreytur í Viðskiptaskuldir, Viðskiptakröfur og Framleiðslustýring sem tilgreina að líkamleg uppfærsla ætti að búa til fylgiskjöl. Þú munt venjulega virkja þennan valkost þegar þú vilt að fjárhagsbókin sé uppfærð í hvert skipti sem þú uppfærir birgðann. Ef birgðakeðjustjórnun er ekki skráningarkerfið þitt fyrir fjárhag gætirðu viljað slökkva á þessum valkosti.

### <a name="when-should-i-enable-the-post-financial-inventory-option"></a>Hvenær ætti ég að virkja valkostinn eftir Fjárhagsbirgðir?

The **Bókaðu fjárhagsskrá** valmöguleikinn er venjulega virkur þegar **Birgð vara** valmöguleikinn er virkur. Þessi valkostur er notaður í samræmi við færibreytur í Viðskiptaskuldir, Viðskiptakröfur og Framleiðslustýring sem tilgreina að fjárhagsuppfærslan ætti að búa til fylgiskjal. Þú munt venjulega virkja þennan valkost þegar þú vilt að fjárhagsbókin sé uppfærð í hvert skipti sem þú uppfærir birgðina fjárhagslega (til dæmis með því að reikningsfæra sölupantanir og innkaupapantanir, eða enda framleiðslupöntun). Ef birgðakeðjustjórnun er ekki skráningarkerfið þitt fyrir fjárhag gætirðu viljað slökkva á þessum valkosti.

### <a name="when-should-i-enable-the-post-to-deferred-revenue-account-on-sales-delivery-option"></a>Hvenær ætti ég að virkja valkostinn Bóka á frestað tekjureikning við afhendingu sölu?

Þú notar **Bóka á frestað tekjureikning við afhendingu sölu** valmöguleika til að gefa til kynna hvort þú vilt færa tekjur í fjárhag þegar þú bókar fylgiseðil fyrir sölupöntun. Þessi valkostur er venjulega notaður þegar langur töf er á milli fylgiseðils og reiknings í sölupöntun, eða þegar ekki er hægt að reikningsfæra allar sölupantanir á tímabilinu. Venjulega muntu gera þennan valkost óvirkan ef þú bókar sölupöntunarreikninga þína strax eftir að þú bókar fylgiseðilinn. Þannig forðast þú að búa til aukafjárhagsbókanir sem verða strax bakfærðar þegar þú reikningsfærðir sölupöntun.

### <a name="when-should-i-enable-the-accrue-liability-on-product-receipt-option"></a>Hvenær ætti ég að virkja valkostinn Safna á ábyrgð á vörukvittun?

Í flestum stofnunum viltu virkja **Áfallast ábyrgð við móttöku vöru** valmöguleika fyrir alla vörutegundahópa, óháð því hvort þú ert með vöru á lager eða vöru sem ekki er á lager. Þessi valkostur er notaður til að bóka uppsöfnun í fjárhag, byggt á innhreyfingarverði afurða. Vegna þess að það er venjulega töf á milli bókunar vörukvittunar fyrir innkaupapöntun og bókunar reikningsins, verða flestar stofnanir að viðurkenna skuldina á efnahagsreikningi til að uppfylla staðbundnar reglur eins og almennt viðurkenndar reikningsskilavenjur (GAAP). Ef birgðakeðjustjórnun er ekki skráningarkerfið þitt fyrir fjárhag gætirðu viljað slökkva á þessum valkosti. Ef fyrirtæki þitt notar innkaupaflokka á innkaupapantunum geturðu stjórnað uppsöfnunarkröfunni með því að virkja **Safna á kaupkostnað við móttöku** valmöguleika fyrir flokkastefnureglu um **Innkaupastefnur** síðu.

### <a name="how-can-i-prevent-a-user-from-posting-a-purchase-order-product-receipt-if-a-receipt-registration-isnt-yet-posted"></a>Hvernig get ég komið í veg fyrir að notandi birti innkaupapöntun vörukvittun ef kvittunarskráning hefur ekki enn verið bókuð?

Þú getur komið í veg fyrir að notandi birti vörukvittun innkaupapöntunar ef innkaupapöntunarskráning hefur ekki enn átt sér stað með því að virkja **Skráningarskilyrði** valmöguleika fyrir vörulíkanahópinn. Þessi valkostur er venjulega notaður í fyrirtækjum sem nota tveggja þrepa móttökuferli, eða í tilfellum þar sem þú verður að skrá runu- eða raðnúmer, til dæmis á vörurnar sem þú ert að fá. The **Skráningarskylda** valkostur gildir um *allt* birgðakvittanir fyrir vöru, ekki bara fyrir innkaupapantanir. Til dæmis á það við um birgðabók sem hefur jákvætt magn og framleiðslupöntunarskýrslu sem lokið færslubók.

### <a name="how-can-i-prevent-a-user-from-posting-a-purchase-order-invoice-if-a-product-receipt-isnt-yet-posted"></a>Hvernig get ég komið í veg fyrir að notandi geti bókað innkaupapöntunarreikning ef vörukvittun hefur ekki enn verið bókuð?

Þú getur komið í veg fyrir að notandi geti bókað vörureikning innkaupapöntunar ef innkaupapöntun vörumóttaka hefur ekki enn átt sér stað með því að virkja **Móttökukröfur** valmöguleika fyrir vörulíkanahópinn. Þessi valkostur er venjulega notaður í fyrirtækjum sem krefjast þess að kvittanir séu líkamlega viðurkenndar í aðalbók fyrir uppsöfnun. The **Móttökukrafa** valkostur gildir um *allt* birgðakvittanir fyrir vöru, ekki bara fyrir innkaupapantanir. Til dæmis á það við um birgðabók sem hefur jákvætt magn og framleiðslupöntunarskýrslu sem lokið færslubók. Ef fyrirtækið þitt notar innkaupaflokka á innkaupapantunum geturðu stjórnað kröfunni um kvittun með því að virkja **Móttökukröfur** valmöguleika fyrir flokkastefnureglu um **Innkaupastefnur** síðu.

### <a name="how-can-i-prevent-a-user-from-posting-a-sales-order-packing-slip-if-a-sales-order-picking-list-isnt-yet-posted"></a>Hvernig get ég komið í veg fyrir að notandi geti bókað fylgiseðil sölupöntunar ef sölupöntunartínslulisti er ekki enn bókaður?

Þú getur komið í veg fyrir að notandi geti bókað fylgiseðil eða reikning sölupöntunar ef sölupöntunartínslulisti hefur ekki enn komið fram með því að virkja **Kröfur um val** valmöguleika fyrir vörulíkanahópinn. Þessi valkostur er venjulega notaður í fyrirtækjum sem framkvæma efnislegt tínsluferli í vöruhúsinu (til dæmis með því að nota farsímatæki vöruhússins til að gera tínslu). The **Krafa um val** valkostur gildir um *allt* birgðaútgáfur fyrir vöru, ekki bara fyrir sölupantanir. Til dæmis á það við um birgðabók sem hefur neikvætt magn og færslubók framleiðslupöntunartínslulista.

### <a name="how-can-i-prevent-a-user-from-posting-a-sales-order-invoice-if-the-sales-order-packing-slip-isnt-yet-posted"></a>Hvernig get ég komið í veg fyrir að notandi bóki sölupöntunarreikning ef fylgiseðill sölupöntunar er ekki enn bókaður?

Þú getur komið í veg fyrir að notandi geti bókað sölupöntunarreikning ef fylgiseðill sölupöntunar hefur ekki enn komið fram með því að virkja **Frádráttarkröfur** valmöguleika fyrir vörulíkanahópinn. Þessi valkostur er venjulega notaður í fyrirtækjum sem framkvæma líkamlegt pökkunarferli í vöruhúsinu (til dæmis með því að nota vöruhússtjórnun farsímaforritið til að pakka eða með því að búa til skjal sem verður innifalið með hlutunum sem eru sendar). The **Frádráttarkrafa** valkostur gildir um *allt* birgðaútgáfur fyrir vöru, ekki bara fyrir sölupantanir. Til dæmis á það við um birgðabók sem hefur neikvætt magn og færslubók framleiðslupöntunartínslulista.

### <a name="can-i-prevent-items-that-are-registered-from-being-sold"></a>Get ég komið í veg fyrir að hlutir sem eru skráðir séu seldir?

Þegar vara er skráð í birgðum þínum í Supply Chain Management er magnið efnislega tiltækt til að gefa út í kerfinu. Ef hlutir sem hafa verið skráðir en ekki enn mótteknir ættu *ekki* vera tiltækt til að gefa út á sölupantanir eða framleiðslupantanir, til dæmis, íhugaðu að nota birgðastöðu, birgðalokun, gæðapantanir, sóttkvíspantanir eða frátekningareiginleika til að stjórna viðskiptaferlinu.

## <a name="production-costing"></a>Framleiðsla – kostnaður

### <a name="can-i-use-one-costing-model-for-raw-materials-and-a-different-costing-model-for-finished-goods"></a>Get ég notað eitt kostnaðarlíkan fyrir hráefni og annað kostnaðarlíkan fyrir fullunnar vörur?

Já, þú getur notað mismunandi kostnaðarlíkön fyrir hvern hlut. Það er ekki óalgengt að framleiðendur noti reglubundið kostnaðarlíkan fyrir hráefni og staðalkostnað fyrir hálfunnar og fullunnar vörur.

### <a name="how-can-i-drive-overhead-off-machine-costs"></a>Hvernig get ég keyrt út kostnað af vél?

Til að draga úr kostnaði við vélina þína verður þú að búa til tilföng og tilföngahópa fyrir hverja vél, í samræmi við kröfur fyrirtækisins. Hægt er að úthluta hverjum tilfangi eða tilfangaflokki í kostnaðarflokka til að stjórna kostnaði vélarinnar. Hægt er að tengja hvern kostnaðarflokk við kostnaðarflokk og nota hvern kostnaðarflokk sem grunn við útreikning á óbeinum kostnaði á kostnaðarblaðinu.

### <a name="how-do-i-recognize-cost-that-is-related-to-energy-consumption-for-example-water-energy-or-gas-consumption-on-the-costing-sheet"></a>Hvernig þekki ég kostnað sem tengist orkunotkun (til dæmis vatns-, orku- eða gasnotkun) á kostnaðarblaðinu?

Þú getur almennt greint kostnað sem tengist orkunotkun á einn af tveimur vegu:

- Búðu til línu í uppskriftinni þinni eða formúlunni. Venjulega er þessi lína búin til sem þjónustuvara og þú getur tilgreint mælieiningu sem þú ert að neyta í tengslum við magnið sem þú ert að framleiða. Þannig getur notandinn neytt mismunandi magns meðan á framleiðsluferlinu stendur. Þú getur sjálfkrafa neytt hlutanna byggt á því gildi sem þú velur í **Skola meginreglan** sviði.
- Búðu til óbeinan kostnað á kostnaðarblaðinu þínu. Venjulega er þessi aðferð notuð til að úthluta heildarkostnaði við orkunotkun þína yfir framleiðsluferlið þitt. Þú getur notað kostnaðarflokkinn og frásogsgrundvöllinn til að skala neysluna út frá efni eða vinnu á leiðinni þinni, til dæmis.

Þú ættir að velja besta kostinn, byggt á skýrslugerð, afstemmingu og rekstrarkröfum þínum.

### <a name="can-i-capture-resource-details-in-the-bom-or-formula"></a>Get ég fanga upplýsingar um tilföng í uppskrift eða formúlu?

Tilfangsupplýsingar er aðeins hægt að fanga í leiðaraðgerð. Þó að hægt sé að búa til þjónustuvöru til að tákna tilföng og úthluta kostnaði til að auka kostnaðarútreikning fyrir fullunna vöru, mælum við venjulega ekki með þessari aðferð. Þess í stað mælum við með því að þú stofnir einfalda leið sem hefur eina línu til að rekja tilföngskostnað og stillir aðgerðina þannig að hún sé sjálfkrafa notuð annað hvort í upphafi eða lok framleiðslupöntunarinnar.

### <a name="can-i-view-the-calculation-details-if-the-cost-is-manually-entered"></a>Get ég skoðað útreikningsupplýsingarnar ef kostnaður er færður inn handvirkt?

Nr. Ef þú slærð inn verðið handvirkt á **Vöruverð** síðu, the **Skoða útreikningsupplýsingar** og **Tilkynna upplýsingar um útreikning** hnappar eru ekki tiltækir. Ef þú velur **Kostnaðarsamantekt eftir kostnaðarflokki** hnappur fyrir kostnaðarverð sem er fært inn handvirkt, samantekt lína er sýnd og allur kostnaður er rúllað upp á fullunna vöru.

### <a name="does-the-system-calculate-variances-on-a-production-order-when-i-manually-enter-the-cost"></a>Reiknar kerfið út frávik á framleiðslupöntun þegar ég slær inn kostnaðinn handvirkt?

Já, kerfið reiknar út frávik þegar þú slærð inn staðalkostnað handvirkt. Hins vegar, þegar þú færir inn staðalkostnað handvirkt í stað þess að reikna hann út, telst öll efnis-, leiðar- og óbein kostnaðarnotkun í framleiðslupöntuninni vera staðgöngufrávik. Ef það eru viðbótarfrávik, svo sem neysla á aukaefni eða vinnu, verða þau einnig skráð sem frávik frá framleiðsluuppskrift. Þess vegna mælum við eindregið með því að þú keyrir alltaf útreikning fyrir vörur sem hafa uppskrift, leið eða óbeinan kostnað.

### <a name="how-can-i-carry-the-variances-from-a-subproduction-order-to-the-parent-production-order"></a>Hvernig get ég flutt frávik frá undirframleiðslupöntun yfir í móðurframleiðslupöntun?

Þegar þú notar reglubundið kostnaðarlíkan eins og FIFO, LIFO eða vegið meðaltal, verður kostnaður frá undirframleiðslu færður í heuristic líkaninu sem þú hefur valið fyrir vörurnar. Ef þú krefst raunverulegs kostnaðar, íhugaðu að nota merkingarregluna til að gefa til kynna hvaða undirframleiðsla er gefin út á yfirframleiðslupöntun. Að öðrum kosti skaltu íhuga að nota **Fjárhagsskrá** valkostur fyrir **Hópur** eða **Raðnúmer** vídd í rekjavíddarhópnum, til dæmis.

### <a name="how-does-the-flushing-principle-affect-consumption"></a>Hvernig hefur skolunarreglan áhrif á neyslu?

Skolareglan á uppskrift, formúlu eða leiðarlínu stjórnar tímasetningu og tækni sem er notuð til að neyta vörunnar eða vinnunnar. Ef þú velur *Byrjaðu*, varan eða vinnuafl er sjálfkrafa neytt þegar þú byrjar framleiðslupöntun. Ef þú velur *Klára*, varan eða vinnuafl er sjálfkrafa neytt þegar þú tilkynnir framleiðslupöntun sem lokið. Ef þú velur *Handbók*, notandi verður að velja efni handvirkt eða skrá tímann í verk- eða leiðarkortadagbók. BOMs og formúlur hafa einnig an *Fáanlegt á staðnum* valmöguleika. Ef þessi valkostur er valinn eru vörurnar sjálfkrafa notaðar eftir að þær eru fluttar á framleiðslugólfsstaðsetningu.

### <a name="how-should-i-run-cost-calculations-if-i-have-multi-level-boms-or-formulas"></a>Hvernig ætti ég að keyra kostnaðarútreikninga ef ég er með fjölþrepa uppskriftir eða formúlur?

Almennt mælum við með að þú byrjar á lægsta stigi uppskrifta eða formúla fyrir útreikninginn. Til að gera síun auðveldari þegar þú keyrir kostnaðarútreikninga í fjöldann geturðu notað útreikningahópa til að hjálpa til við að aðgreina vörur. Við mælum líka með því að þú keyrir *Endurreiknaðu uppskriftarstig* reglubundið starf áður en þú byrjar að fjöldakeyra kostnaðarútreikninga. Hver stofnun ætti að íhuga blöndu af vörum og skilgreina stefnu sem uppfyllir sérstakar þarfir vörunnar þinnar og uppskriftar- eða formúluuppbyggingar.

## <a name="transfer-order-costing"></a>Flutningspöntunarkostnaður

### <a name="is-there-a-way-to-allocate-freight-to-a-transfer-order-cost"></a>Er einhver leið til að úthluta frakt til flutningspöntunarkostnaðar?

Þú getur bætt gjöldum við flutningspöntun til að bæta við kostnaði. Gjaldskóðinn skilgreinir debet og kredit fyrir gjaldið sem þú ert að bæta við. Þú verður fyrst að búa til greiðslukóða í **Vörustjórnun** mát. Til að bæta gjaldi við millifærslupöntun velurðu **Gjöld** á millifærslupöntunarlínunni sem þú vilt bæta gjaldi við.

## <a name="variances"></a>Frávik

### <a name="can-i-treat-variances-differently-based-on-the-site-or-warehouse"></a>Get ég meðhöndlað frávik á annan hátt, byggt á síðunni eða vöruhúsi?

Það er enginn möguleiki að stilla fráviksreikninga eftir síðu. Þegar þú notar staðlaðan kostnað fyrir útgefna vöru geturðu valið aðalreikninginn sem er notaður fyrir staðlaða kostnaðarfráviksfærslur á **Birting** síðu. Þú getur valið að stilla reikninga fyrir einn hlut, hóp af hlutum eða alla hluti. Þú getur líka stillt einn kostnaðarflokk, hóp kostnaðarflokka eða alla kostnaðarflokka.

### <a name="can-i-separate-variances-that-are-the-result-of-currency-exchange-rates-from-other-types-of-variances"></a>Get ég aðskilið frávik sem eru afleiðing af gengi gjaldmiðla frá öðrum tegundum frávika?

Ef frávik stafar af gengismun á innkaupapöntunarverði og staðalkostnaði vöru er engin leið að aðgreina gengismun frá öðrum frávikum.

## <a name="reporting"></a>Skýrslugerð

### <a name="how-many-inventory-value-report-configurations-can-i-create-and-use"></a>Hversu margar birgðagildisskýrslustillingar get ég búið til og notað?

Það eru engin takmörk á fjölda birgðagildisskýrslustillinga sem þú getur búið til. Þú ættir að meta sérstakar skýrslukröfur þínar og búa til fjölda stillinga sem þú þarft til að uppfylla þessar kröfur. Þú þarft að minnsta kosti eina birgðagildisskýrslustillingu til að keyra skýrsluna eða skýrslugeymsluvalkostinn.

### <a name="can-i-use-the-inventory-value-report-to-analyze-the-cost-of-an-item-in-each-warehouse"></a>Get ég notað birgðavirðisskýrsluna til að greina kostnað vöru í hverju vöruhúsi?

Já. Þú getur virkjað **Útsýni** eða **Samtals** valmöguleika fyrir hvern **Vöruhús** vídd í uppsetningu birgðavirðisskýrslu. Hins vegar mun skýrslan aðeins sýna gildi fyrir víddir þar sem **Fjárhagsskrá** valkosturinn er virkur fyrir geymsluvíddarhópinn. Fyrir aðrar stærðir mun það sýna auða dálka. Fyrir frekari upplýsingar, sjá [Dæmi um skýrslu um birgðagildi og rökfræði](inventory-value-report-examples.md).

### <a name="how-can-i-view-the-inventory-quantity-as-of-a-specific-date-with-the-weighted-average"></a>Hvernig get ég skoðað birgðamagn frá tiltekinni dagsetningu með vegnu meðaltali?

Þú getur notað **Öldrun birgða** skýrslu, sem felur í sér **Meðaleiningakostnaður** dálk sem sýnir verðmæti birgða frá tiltekinni dagsetningu. Fyrir frekari upplýsingar, sjá [Birgðaöldrun skýrsludæmi og rökfræði](inventory-aging-report.md).

### <a name="how-can-i-view-which-receipt-transactions-are-settled-against-an-issue-transaction"></a>Hvernig get ég skoðað hvaða kvittunarfærslur eru jafnaðar á móti útgáfufærslu?

Hægt er að skoða uppgjör fyrir birgðafærslu með því að velja **Uppgjör** eða **Kostnaðarkönnuður** á **Birgðir** flipann á aðgerðarrúðunni í **Birgðafærsla** eða **Upplýsingar um birgðafærslur** síðu. Ef þú velur kvittun til að skoða vandamálin sem tengjast færslunni sýnir kostnaðarkannarinn ekki upplýsingarnar. Upplýsingar eru aðeins sýndar ef þú velur útgáfufærslu.

### <a name="how-does-the-inventory-value-report-show-items-that-have-a-positive-physical-quantity-and-a-negative-financial-value"></a>Hvernig sýnir birgðavirðisskýrslan hluti sem hafa jákvætt efnislegt magn og neikvætt fjárhagslegt gildi?

Birgðavirðisskýrslan aðskilur efnislegar og fjárhagslegar upphæðir og magn í sína eigin dálka. Gildin sem eru sýnd í skýrslunni eru frá því tímabili sem þú valdir þegar þú keyrðir skýrsluna. Samantektarstigið sem er sýnt fer eftir stillingunum sem þú valdir. Ef vara hefur færslur sem hafa verið mótteknar líkamlega og gefnar út fjárhagslega, eru magn og gildi tekin saman sjálfstætt. Ef þú valdir að skoða smáatriðin sem færslur, eru línur fyrir hverja innhreyfingu og útgáfu sýndar sérstaklega og líkamlegt magn og fjárhagslegt magn og upphæðir, í sömu röð, sýndar. Fyrir frekari upplýsingar, sjá [Dæmi um skýrslu um birgðagildi og rökfræði](inventory-value-report-examples.md).

### <a name="what-is-the-impact-of-storage-and-tracking-dimension-groups-on-the-inventory-value-report"></a>Hvaða áhrif hafa geymslu- og rakningarvíddarhópar á birgðavirðisskýrsluna?

Ef þú virkjar **Fjárhagslegt verðmæti** valmöguleika fyrir vídd í geymslu- eða rakningarvíddarhópi geturðu valið **Útsýni** eða **Samtals** valmöguleika fyrir víddina í birgðagildisskýrslustillingu. Ef þú velur **Útsýni** eða **Samtals** valkostur fyrir vídd þar sem **Fjárhagslegt verðmæti** valkosturinn er ekki valinn, dálkurinn verður auður í skýrsluúttakinu. Ef þú hefur virkjað **Fjárhagslegt verðmæti** valmöguleika fyrir vídd í geymslu- eða rakningarvíddarhópi, og þú velur ekki **Útsýni** eða **Samtals** valmöguleika á uppsetningu birgðavirðisskýrslu mun kerfið taka saman gildin fyrir valdar víddir þar sem þær eru raktar fjárhagslega.

### <a name="can-i-customize-the-power-bi-embedded-reports-for-costing"></a>Get ég sérsniðið Power BI innbyggðar skýrslur fyrir kostnaðarkostnað?

Já, notendur sem hafa réttar öryggisheimildir geta uppfært skýrsluhönnunarstriga fyrir hvaða sem er Power BI innbyggð skýrsla í Supply Chain Management. Fyrir frekari upplýsingar, sjá [Sérsníddu innfelldar skýrslur í greiningarvinnusvæðum](../../fin-ops-core/dev-itpro/analytics/customize-analytical-workspace.md).

### <a name="where-can-i-view-the-variance-analysis-statement"></a>Hvar get ég skoðað fráviksgreiningaryfirlýsinguna?

Þú getur nálgast fráviksgreiningaryfirlýsinguna með því að fara á **Kostnaðarstjórnun \> Fyrirspurnir og skýrslur \> Birgðabókhald – greiningarskýrslur** eða **Kostnaðarstjórnun \> Fyrirspurnir og skýrslur \> Framleiðslubókhald – greiningarskýrslur**. Báðir valkostir opna sömu skýrsluna og skýrslan hefur sömu hegðun.

## <a name="item-prices-and-default-costs"></a>Vöruverð og vanskilakostnaður

### <a name="can-i-maintain-the-cost-for-each-product-variant"></a>Get ég haldið uppi kostnaði fyrir hvert vöruafbrigði?

Já. Þú getur virkjað **Notaðu kostnaðarverð eftir afbrigðum** valmöguleika á **Stjórna kostnaði** Flýtiflipi á **Útgefin vara** síðu til að virkja verðlagningu eftir vöruafbrigðum. (Þessi valkostur er aðeins í boði fyrir vörumeistara.) Síðan, á **Vöruverð** síðu (sem þú getur opnað frá annaðhvort **Kostnaðarútgáfa** síðu eða **Útgefin vara** síðu), getur þú valið **Mál sýna** til að tilgreina hvort þú vilt sýna **Stillingar**, **·**, **·**, eða **Stíll** vídd. Til að vista uppsetninguna og nota valdar stærðir í hvert skipti sem þú opnar síðuna skaltu virkja **Vista uppsetningu** valmöguleika og veldu síðan **Allt í lagi**. Þú getur aðeins slegið inn víddir fyrir vörur þar sem vídirnar eru virkar í vöruvíddarflokknum.

### <a name="can-i-maintain-the-cost-for-each-warehouse"></a>Get ég haldið uppi kostnaði fyrir hvert vöruhús?

Nei, þú getur ekki haldið vöruverði eftir vöruhúsi. Hins vegar er hægt að viðhalda viðskiptasamningum um innkaupaverð eða söluverð eftir vöruhúsum. Fyrst skaltu velja **Fyrir kaupverð** eða **Fyrir útsöluverð** valkostur fyrir vídd á **Geymsluvíddarhópur** síðu. Síðan, þegar þú stofnar viðskiptasamningsbókina og opnar línurnar fyrir víddir, velurðu **Birgðir \> Sýna stærðir** til að velja hvaða vídd á að sýna í ristinni. Til að vista uppsetninguna og nota valdar stærðir í hvert skipti sem þú opnar síðuna skaltu virkja **Vista uppsetningu** valmöguleika og veldu síðan **Allt í lagi**. Þú getur aðeins slegið inn víddir fyrir vörur þar sem vídirnar eru virkar í vöruvíddarflokknum.

### <a name="what-are-price-charges"></a>Hvað eru verðgjöld?

Verðgjöld veita leið til að bæta fastri upphæð við einingarverð vöruverðs eða viðskiptasamnings. Þegar þú slærð inn upphæð í **Verðgjöld** reitnum geturðu líka slegið inn gildi í **Gjaldar magn** sviði. Verðgjöldin eru afskrifuð yfir kostnaðarmagninu sem þú tilgreinir. Virkjaðu **Þ.m.t. í einingaverði** valmöguleika ef þú vilt taka verðgjöldin inn í einingarverð vörunnar. Þessi valkostur er alltaf virkur fyrir staðlaðan kostnað.

### <a name="how-should-i-configure-prices-for-items-that-are-procured-in-multiple-currencies"></a>Hvernig ætti ég að stilla verð fyrir vörur sem eru keyptar í mörgum gjaldmiðlum?

Ef þú slærð inn sjálfgefið verð í **Kaupverð** sviði á **Útgefin vara** síðu er gert ráð fyrir að hún sé í bókhaldsgjaldmiðli höfuðbókarinnar fyrir lögaðilann sem þú ert í. Sömuleiðis, ef þú slærð inn innkaupsverð í kostnaðarútgáfu þar sem **Verðtegund** reiturinn er stilltur á *Kaup*, er gert ráð fyrir að verðið sé í bókhaldsgjaldmiðli lögaðilans þíns. Þegar þú býrð til innkaupapöntun fyrir lánardrottinn sem er með annan gjaldmiðil mun kerfið sjálfkrafa umbreyta gjaldmiðlinum úr bókhaldsgjaldmiðilsupphæðinni í viðskiptagjaldmiðilinn með því að nota gengi sem þú tilgreinir í **Gengistegund bókhaldsgjaldmiðils** reit í bókhaldinu þínu.

Þegar þú býrð til viðskiptasamningsbók geturðu tilgreint gjaldmiðilinn sem þú gefur upp verðið í á hverri línu. Þú getur búið til viðskiptasamninga fyrir marga gjaldmiðla, tiltekna lánardrottna og margar aðrar samsetningar þátta. Ef þú stofnar innkaupapöntun þar sem viðskiptasamningur er til fyrir gjaldmiðilinn sem þú hefur valið mun kerfið nota viðskiptasamninginn sem hefur samsvarandi gjaldmiðil. Þegar þú bókar færslur eins og vörukvittun eða reikninga verður upphæðinni umreiknað í bókhaldsgjaldmiðil fjárhagsins með því að nota bókhaldsgengið sem þú tilgreinir í fjárhagsbókinni.

### <a name="how-should-i-configure-costs-for-items-that-are-procured-in-multiple-currencies"></a>Hvernig ætti ég að stilla kostnað fyrir vörur sem eru keyptar í mörgum gjaldmiðlum?

Ekki er hægt að stilla kostnað í fleiri en einum gjaldmiðli. Kostnaðurinn sem þú tilgreinir fyrir vöruverðið eða sjálfgefinn kostnað sem þú færð inn í **Verð** sviði á **Stjórna kostnaði** Flýtiflipi á **Útgefin vara** síðu eru alltaf gefin upp í bókhaldsgjaldmiðli fjárhagsbókarinnar fyrir lögaðilann sem þú hefur valið.

Ef fyrirtæki þitt notar staðlaða kostnaðarreikning, ættir þú að skilgreina stefnu til að skilgreina kostnað þegar það eru margir gjaldmiðlar. Þú ættir einnig að skilgreina ferli til að uppfæra kostnað reglulega til að draga úr fjölda frávika sem eru bókuð.

### <a name="can-i-use-the-profit-setting-on-the-cost-group-page-to-calculate-sales-prices"></a>Get ég notað Hagnaðarstillinguna á síðunni Kostnaðarflokkur til að reikna út söluverð?

Já, þú getur notað **Hagnaður** stilling á **Kostnaðarhópur** síðu til að bæta við prósentu þegar söluverð er reiknað með því að nota kostnaðarútreikning. Fyrir frekari upplýsingar, sjá [BOM útreikningar](bom-calculations.md).

## <a name="marking"></a>Merking

### <a name="how-does-marking-affect-periodic-costing-models"></a>Hvaða áhrif hefur merking á reglubundnar kostnaðarlíkön?

Ef þú notar reglubundið kostnaðarlíkan eins og FIFO, LIFO eða vegið meðaltal, og þú hefur merkt innhreyfingarfærslu á móti útgáfufærslu, er hormónalíkan vörunnar hunsuð meðan á birgðalokunarferlinu stendur. Þess í stað mun kerfið nota raunkostnað kvittunarinnar fyrir kostnað við útgáfuna.

### <a name="what-happens-during-the-inventory-close-when-i-use-marking"></a>Hvað gerist við lokun birgða þegar ég nota merkingu?

Þegar þú merkir innhreyfingar og útgáfur mun birgðalokun jafna færslurnar sem eru merktar saman. Þegar merking er notuð til að búa til uppgjör, er **Meginregla** sviði á **Uppgjör** síða verður stillt á *Merking*. Ef færsla er merkt áður en hún er líkamlega eða fjárhagslega uppfærð mun útgáfan nota kostnað merktu kvittunarinnar í stað hlaupandi meðalkostnaðar. Ef færslurnar eru merktar eftir fjárhagsuppfærsluna mun birgðalokun og leiðréttingarferli leiðrétta útgáfukostnaðinn þannig að hann passi við innhreyfingarkostnaðinn.

### <a name="can-i-manually-mark-transactions-when-i-use-standard-costing-or-moving-average"></a>Get ég merkt færslur handvirkt þegar ég nota staðlaðan kostnað eða hlaupandi meðaltal?

Nei, þú getur ekki handvirkt merkt kvittanir eða vandamál þegar þú notar staðlaðan kostnað eða hlaupandi meðaltal. Ef færslur (t.d. bein afhending eða pantanir milli fyrirtækja) eru sjálfkrafa merktar, verður merkingarskráin eftir og virkar sem harður fyrirvari. Hins vegar, þegar þú notar staðlaðan kostnað eða hlaupandi meðaltal, hefur merking færslur engin áhrif á kostnað hlutanna.

### <a name="how-does-marking-affect-the-profit-and-loss-statement"></a>Hvaða áhrif hefur merking á rekstrarreikning?

Þegar þú merkir útgáfufærslu á móti kvittun mun kostnaðurinn fyrir útgáfuna passa við völdu kvittunina. Þegar þú birtir málið líkamlega og fjárhagslega mun birtingin hafa áhrif á **Kostnaður við seldar vörur, afhentar** og **Kostnaður seldra vara, reikningsfærður** reikninga sem þú tilgreinir í birgðabókunarsniðinu. Ef viðskipti eru merkt eftir líkamlega eða fjárhagslega uppfærslu, *Birgðalokun og aðlögun* ferli mun búa til leiðréttingu sem hefur samsvarandi fylgiskjal sem aðlagar **Kostnaður seldra vara, reikningsfærður** reikning og mótvægi á reikninginn sem þú tilgreinir fyrir **Kostnaður eininga, reikningsfærður** (birgðahald).

### <a name="how-does-marking-affect-master-planning"></a>Hvaða áhrif hefur merking á aðalskipulag?

The **Hefðbundin uppfærsla** flipann á **Aðalskipulagsfæribreytur** síða inniheldur reit sem er nefndur **Uppfæra merkingu**. Valkosturinn sem þú velur þar er notaður þegar þú staðfestir áætlaða pöntun sem er mynduð af aðalskipulagi. Eftirtaldir valkostir eru í boði:

- *Nei* – Kerfið framkvæmir engar merkingar.
- *Standard* – Kerfið merkir kvittanir gegn útgáfum samkvæmt tengingu. Kröfupöntun er merkt á móti uppfyllingarpöntun. Ef eitthvað magn er eftir á uppfyllingunni er uppfyllingarpöntunin ekki merkt.
- *Framlengdur* – Kerfið merkir bæði kröfupantanir og uppfyllingarpantanir, óháð því hvort eitthvað magn er enn opið á uppfyllingarpöntuninni.

## <a name="negative-inventory"></a><a name="negative-inventory"></a>Neikvæð birgðastaða

### <a name="when-should-i-allow-physical-negative-inventory"></a>Hvenær ætti ég að leyfa líkamlegar neikvæðar birgðir?

Almennt mælum við ekki með því að þú leyfir líkamlegar neikvæðar birgðir, því það er ekki hægt að hafa minna en 0 (núll) af áþreifanlegum hlut í vöruhúsinu þínu. Hins vegar gætu viðskiptaferli sumra atvinnugreina og viðskiptasviðsmynda takmarkað rekstur sem krefst þess að birgðum verði leyft að verða líkamlega neikvæð. Til dæmis gætu smásalar ekki viljað koma í veg fyrir sölu á hlut sem er færð á skrá, jafnvel þegar kerfið gefur til kynna að engir hlutir séu tiltækir. Ferlaframleiðendur gefa annað dæmi. Fyrir þessa framleiðendur getur magnið sem er neytt farið yfir það sem mælt er með í formúlunni. Að öðrum kosti gæti eyðslan verið áætluð í stað þess að vera nákvæm, þannig að eyðslan fari yfir magnið á tilteknum stað, svo sem tanki.

Þegar mögulegt er ættir þú að meta viðskiptaferlið þitt og reyna að bæta það til að tryggja að birgðir geti ekki verið neikvæðar. Ef þú verður að leyfa neikvæðar birgðir ættirðu að hafa skýrt viðskiptaferli til að leiðrétta neikvæðu birgðina, því það getur haft slæm áhrif á kostnaðarkostnað.

### <a name="when-should-i-allow-financial-negative-inventory"></a>Hvenær ætti ég að leyfa fjárhagslega neikvæðar birgðir?

Almennt mælum við með því að flestar stofnanir leyfi fjárhagslega neikvæðar birgðir. (Í flestum tilfellum eru innkaupapöntunarreikningar ekki afgreiddir áður en hægt er að senda vörurnar.) Þú ættir að virkja þennan valkost þegar þú ert með ákveðin viðskiptaferli sem krefjast þess að söluverð endurspegli lokakostnað innkaupapöntunar. Til dæmis gæti þessi krafa átt við í pöntunariðnaði eða á tilteknum svæðum þar sem lögin mæla fyrir um það.

### <a name="what-happens-to-the-cost-of-my-issues-when-the-inventory-is-negative"></a>Hvað verður um kostnaðinn við útgáfur mínar þegar birgðir eru neikvæðar?

Þegar birgðir fyrir vöruna þína eru neikvæðar og þú gefur út fleiri vörur en þú ert með, mun kerfið nota sjálfgefið vöruverð til að reikna út hlaupandi meðaltal ef þú notar reglubundið kostnaðarlíkan eins og FIFO, LIFO eða vegið meðaltal. Ef ekkert sjálfgefið verð er tilgreint fyrir vöruna mun kerfið gefa út birgðann með gildinu 0 (núll). Þessi hegðun getur valdið því að framtíðarútreikningar á hlaupandi meðaltali þínu eða hlaupandi meðaltali verða ónákvæmir.

### <a name="can-i-prevent-items-from-being-picked-packed-or-sold-on-sales-orders-and-production-orders-if-there-isnt-enough-on-hand-inventory"></a>Get ég komið í veg fyrir að vörur séu tíndar, pakkaðar eða seldar í sölupantanir og framleiðslupantanir ef það er ekki nóg lager á lager?

Já. Við mælum með að þú slökktir á **Líkamlega neikvætt** valkostur fyrir vörulíkanaflokkinn til að koma í veg fyrir að vörur séu tíndar, pakkaðar eða seldar í sölupantanir og framleiðslupantanir.

### <a name="can-i-prevent-items-from-being-invoiced-on-a-sales-order-if-no-purchase-orders-have-been-invoiced-for-the-same-item"></a>Get ég komið í veg fyrir að vörur séu reikningsfærðar í sölupöntun ef engar innkaupapantanir hafa verið reikningsfærðar fyrir sömu vöruna?

Já. Við mælum með að þú slökktir á **Fjárhagsleg neikvæð** valkostur fyrir vörulíkanaflokkinn til að koma í veg fyrir að vörur séu reikningsfærðar á sölupöntun ef engar innkaupapantanir hafa verið reikningsfærðar fyrir sömu vöru.

### <a name="how-does-negative-inventory-affect-financial-ratios-such-as-gross-profit-margin"></a>Hvernig hefur neikvæðar birgðir áhrif á kennitölur eins og framlegð?

Þegar þú leyfir birgðum þínum að verða neikvæðar, getur birgðaverðmæti í efnahagsreikningi þínum og kostnaði við seldar vörur í rekstrarreikningi þínum verið vanmetið, sérstaklega ef ekkert sjálfgefið verð er stillt fyrir vörur þínar. Því er hægt að ofmeta reikningsskil og hlutföll eins og framlegð vegna þess að kostnaðurinn er rangur. Ef þú notar reglubundið kostnaðarlíkan eins og FIFO, LIFO eða vegið meðaltal, er hægt að leiðrétta gildi útgáfunnar þegar þú keyrir birgðalokun og leiðréttingarferli eftir að neikvæða birgðamagnið hefur verið leiðrétt. Hins vegar, ef þú notar hlaupandi meðaltal, er engin leið til að endurmeta einstök viðskipti.

### <a name="how-should-i-correct-negative-inventory"></a>Hvernig ætti ég að leiðrétta neikvæðar birgðir?

Við mælum með því að þú fylgist oft með og leiðréttir neikvæðar birgðir þegar kröfur fyrirtækisins eða fyrirtækis þíns segja að þú leyfir birgðum þínum að verða neikvæðar. Hægt er að leiðrétta birgðagildin með því að framkvæma lotutalningu, bóka leiðréttingu eða bóka hreyfibók. Ef þú verður að viðurkenna óvæntan hagnað í birgðum í tilteknum fjárhagsreikningi, ættir þú að ætla að nota hreyfingarbók. Annars, þegar þú notar lotutalningu eða birgðaleiðréttingarferli, mun kerfið bóka birgðaleiðréttinguna á **Birgðakvittun** reikning og mótvægi í **Birgðaútgjöld, hagnaður** reikninga sem þú tilgreinir á birgðabókunarsniðinu.

### <a name="do-i-have-to-create-a-new-item-if-my-inventory-has-gone-negative-and-i-use-moving-average"></a>Þarf ég að búa til nýjan hlut ef birgðirnar mínar hafa orðið neikvæðar og ég nota hlaupandi meðaltal?

Nr. Ef fyrirtækið þitt leyfir birgðum að verða líkamlega neikvæðar og þú notar hlaupandi meðaltal sem birgðalíkan þitt, mun kerfið nota varakostnaðarröðina sem er úthlutað á **Birgða- og vöruhúsastjórnunarfæribreytur** síðu til að ákvarða hvernig kostnaði verður úthlutað á málefnin þín. Almennt mælum við með því að þú forðast að leyfa birgðum þínum að verða líkamlega neikvæð. Fyrir frekari upplýsingar, sjáðu aðrar spurningar í [Neikvæð birgðahald](#negative-inventory) kafla þessa efnis.

## <a name="not-stocked-products"></a>Vörur sem ekki eru á lager

### <a name="can-i-post-sales-order-picking-lists-for-not-stocked-products"></a>Get ég birt sölupöntunarlista fyrir vörur sem ekki eru á lager?

Þegar þú býrð til tínslulista fyrir sölupöntun sem inniheldur vörur sem eru í vörulíkanaflokki sem er ekki á lager, muntu ekki sjá neinar línur fyrir þessar vörur sem ekki eru á lager. Þú getur ekki notað vöruhússtjórnun farsímaforritið til að vinna úr hlutum sem ekki eru á lager.

Þegar þú býrð til fylgiseðil fyrir sölupöntun sem inniheldur vörur sem eru í vörulíkanaflokki sem er ekki á lager skaltu stilla **Magn** sviði til *Valið magn og ekki birgðir vörur* að taka með vörurnar sem ekki eru á lager í skjalagerðinni. Ef þú velur *Allt*, aðeins birgðir vörur verða innifaldar á fylgiseðlinum.

### <a name="should-i-use-a-not-stocked-product-or-a-category-sales-category-or-procurement-category"></a>Ætti ég að nota vöru sem ekki er á lager eða flokk (söluflokkur eða innkaupaflokkur)?

Valið á milli vöru sem ekki er á lager og flokks fer eftir sérstökum viðskiptaþörfum þínum. Vörur sem ekki eru á lager bjóða almennt upp á meiri stjórn á sjálfgefnum gildum, svo sem magni og verði á innkaupapantunum og sölupöntunum. Þess vegna eru vörur sem ekki eru á lager ákjósanlegar í tilfellum þar sem sama vara eða þjónusta er keypt eða seld oftar en einu sinni. Flokkar eru gagnlegir í aðstæðum þar sem verð, hlutir, lýsingar og svo framvegis eru ósamræmi frá færslu til færslu. Einnig er hægt að nota flokka á hvaða vöru sem er til að hjálpa til við að flokka vörutegundina sem verið er að selja eða kaupa.

## <a name="service-items"></a>Þjónustuvara

### <a name="what-is-the-difference-between-a-service-item-and-a-not-stocked-product"></a>Hver er munurinn á þjónustuvöru og vöru sem ekki er á lager?

Þjónustuvara er vörutegund. Þegar þú býrð til nýútgefna vöru geturðu stillt **Vörugerð** reit til annaðhvort *Atriði* eða *Þjónusta*. *Atriði* er venjulega valið til að gefa til kynna að hluturinn sé áþreifanlegur, en *Þjónusta* er venjulega valið til að gefa til kynna að hluturinn sé óefnislegur.

Allar útgefnar vörur, óháð því hvort um er að ræða vöru eða þjónustuvöru, getur verið á lager eða ekki á lager. Stillingunni á lager eða ekki á lager er stjórnað af vörulíkanahópnum sem þú velur fyrir útgefnu vöruna. Þegar þú velur vöruflokk sem er ekki á lager, býr kerfið ekki til birgðafærslur fyrir tengda sölupöntun eða innkaupapöntun, til dæmis.

### <a name="can-i-include-not-stocked-items-in-a-bom"></a>Get ég sett hluti sem ekki eru á lager í uppskrift?

Nei, þú getur ekki látið útgefna vöru fylgja með sem er tengd vörulíkanaflokki þar sem **Á lager** valkosturinn er óvirkur í uppskrift eða formúlu. Það skiptir ekki máli hvort **Vörugerð** reiturinn er stilltur á *Atriði* eða *Þjónusta*. Aðeins hlutir sem eru á lager geta verið með í uppskrift eða formúlulínum.

## <a name="costing-modelspecific-questions"></a>Kostnaðarlíkan-sértækar spurningar

### <a name="which-costing-model-should-i-use"></a>Hvaða kostnaðarlíkan ætti ég að nota?

Kostnaðarlíkönin sem þú ættir að velja fer eftir viðskiptakröfum þínum. Áður en þú velur kostnaðarlíkan til að nota í Supply Chain Management, ættir þú að sannreyna að líkanið sé leyft samkvæmt staðbundnum reglugerðum. Við mælum með að þú staðfestir val þitt hjá löggiltum endurskoðanda á þínu svæði.

### <a name="can-i-use-more-than-one-costing-model-in-my-organization"></a>Get ég notað fleiri en eitt kostnaðarlíkan í fyrirtækinu mínu?

Já. Það eru engin takmörk á fjölda vörulíkanaflokka eða kostnaðarlíkana sem þú getur valið í Supply Chain Management.

### <a name="can-i-use-more-than-one-costing-model-for-each-item"></a>Get ég notað fleiri en eitt kostnaðarlíkan fyrir hvern hlut?

Nr. Þú getur aðeins valið eitt kostnaðarlíkan fyrir hverja útgefna vöru. Þessari hegðun er stjórnað af vörulíkanahópnum. Ef þú verður að nota fleiri en eitt kostnaðarlíkan til að tilkynna um birgðagildi, ættir þú að íhuga að nota alþjóðlegt birgðabókhald viðbótina.

### <a name="when-i-use-manufacturing-execution-which-costing-methodology-should-i-use"></a>Hvaða kostnaðaraðferð ætti ég að nota þegar ég nota framleiðsluframkvæmd?

Kostnaðarlíkönin sem þú ættir að velja fer eftir viðskiptakröfum þínum. Það er enginn sérstakur kostur eða ókostur við að nota hvaða kostnaðarlíkan sem er þegar fyrirtæki þitt notar líka framleiðsluframkvæmd.

### <a name="when-is-fefo-used"></a>Hvenær er FEFO notað?

Fyrst útrunnið, fyrst út (FEFO) er ekki kostnaðaraðferð. Þess í stað er það fyrirvaratækni sem er oft notuð í framleiðslufyrirtækjum. Þú getur virkjað FEFO frátekningar fyrir vörulíkanaflokk með því að virkja **FEFO dagsetningarstýrt** valmöguleika og veldu síðan gildi í **Veldu viðmið** sviði.

### <a name="are-there-performance-benefits-to-selecting-one-costing-model-over-another"></a>Er afköst ávinningur af því að velja eitt kostnaðarlíkan fram yfir annað?

Almennt séð hefur kostnaðarlíkanið sem þú velur fyrir vöru lágmarksáhrif á heildarafköst kerfisins. Hins vegar gæti sá tími sem þarf til að keyra birgðalokun eða endurútreikningsferli verið fyrir áhrifum af birgðakostnaðarlíkaninu sem þú velur. Til dæmis, ef þú notar staðalkostnað eða hlaupandi meðaltal, hefur birgðalokunarferlið lágmarksáhrif á kerfið, vegna þess að það uppfærir ekki hverja birgðafærslu og stofnar uppgjör. Hins vegar getur reglubundið kostnaðarlíkan eins og FIFO, LIFO eða vegið meðaltal aukið þann tíma sem þarf til að ljúka birgðalokunarferlinu. Nánar tiltekið getur lokaferlið verið lengra þegar þú slærð inn háa tölu í **Hámarksfjöldi endurtekningar leyfður á hvert atriði** reit eða lág tala í **Leyfileg lágmarksupphæð** sviði fyrir *Lokaðu birgðum* ferli.

### <a name="when-should-i-use-the-fixed-receipt-price-option"></a>Hvenær ætti ég að nota valkostinn Fast kvittunarverð?

Þegar þú velur **Fast kvittunarverð** gátreitinn á **Vörulíkanahópur** síðu fyrir vöru mun kerfið nota kvittunarverð sem staðalkostnað fyrir birgðakvittunina. Ef munur er á innkaupsverði og sjálfgefnu kostnaðarverði vöru sem er stillt fyrir vöru verður mismunurinn bókaður á **Fastur kvittunarverð hagnaður** eða **Fast verðtap kvittunar** reikning, og á móti á **Föst kvittunarverð á móti** reikning. (Allir þessir reikningar eru tilgreindir á **Birting** síðu.)

Þú ættir að velja **Fast kvittunarverð** gátreitinn þegar þú notar reglubundið kostnaðarlíkan eins og FIFO, LIFO eða vegið meðaltal, og þú krefst þess að frávik innkaupaverðs sé rakið í fjárhagsbókinni ef verð kvittunar er frábrugðið sjálfgefnum vörukostnaði.

### <a name="moving-average"></a>Hlaupandi meðaltal

### <a name="is-moving-average-the-same-as-a-floating-average"></a>Er hlaupandi meðaltal það sama og fljótandi meðaltal?

Hugtökin hlaupandi meðaltal, fljótandi meðaltal og hlaupandi meðaltal eru oft notuð samheiti. Af þessum skilmálum er hlaupandi meðaltal eina opinbera kostnaðarlíkanið sem er fáanlegt í Supply Chain Management. Þó hlaupandi meðaltal sé ekki opinbert kostnaðarlíkan, þá er það tæknin sem er notuð þegar þú notar reglubundið kostnaðarlíkan eins og FIFO, LIFO eða vegið meðaltal. Hugtakið fljótandi meðaltal er ekki notað í Supply Chain Management og gæti haft mismunandi merkingar í öðrum kerfum.

### <a name="how-can-i-accommodate-the-difference-between-the-product-receipt-price-and-invoice-price-when-i-use-moving-average"></a>Hvernig get ég komið til móts við mismuninn á vörukvittunarverði og reikningsverði þegar ég nota hlaupandi meðaltal?

Þegar þú notar hlaupandi meðaltal er efnislegur kostnaður (kvittunarverð) notaður til að reikna út hlaupandi meðaltal fyrir allar útgáfufærslur. Ef munur er á efniskostnaði (kvittunverði) og fjármagnskostnaði (reikningsverði) mun kerfið sjálfkrafa bóka mismuninn á aðalreikninginn sem er tilgreindur fyrir **Verðmunur á hlaupandi meðaltali** birtingartegund á **Birgðir** flipi á **Birgðafærslusnið** síðu.

### <a name="where-is-the-price-difference-for-moving-average-presented-in-the-general-ledger"></a>Hvar er verðmunurinn á hlaupandi meðaltali fram í fjárhag?

Þegar verðmunur er á bókun efnislegrar uppfærslu og fjárhagsuppfærslu fyrir innhreyfingu er mismunurinn bókaður á aðalreikninginn sem tilgreindur er fyrir **Verðmunur á hlaupandi meðaltali** birtingartegund á **Birgðir** flipi á **Birgðafærslusnið** síðu. Fyrir frekari upplýsingar, sjá [Hækkandi meðaltal](moving-average.md).

### <a name="when-i-use-moving-average-what-happens-if-there-is-an-issue-before-the-receipt"></a>Þegar ég nota hlaupandi meðaltal, hvað gerist ef það er vandamál fyrir kvittunina?

Venjulega gæti verið vandamál fyrir móttökuna annaðhvort vegna þess að þú leyfir líkamlegar neikvæðar birgðir fyrir vörulíkanaflokkinn eða vegna þess að útgáfan er afturdagsett. Fyrir frekari upplýsingar, sjá [Neikvætt birgðahald](#negative-inventory) kafla þessa efnis.

Ef þú ert að bakfæra viðskipti, mælum við með því að þú íhugir vandlega viðskiptaferlið þitt og rekstur til að ákvarða hvort það sé leið til að forðast þessa atburðarás. Ef þú afturdagar færslu fyrir vöru sem notar hlaupandi meðaltal mun kerfið úthluta núverandi hlaupandi meðaltali til færslunnar. Síðari mál eru ekki leiðrétt. Fyrir frekari upplýsingar um hreyfanlegt meðaltal með bakdagsettum viðskiptum, sjá [Hækkandi meðaltal](moving-average.md).

### <a name="standard-costing"></a>Staðalkostnaður

### <a name="what-is-the-difference-between-standard-costing-and-fixed-receipt-price"></a>Hver er munurinn á venjulegu kostnaðarverði og föstu kvittunarverði?

Staðalkostnaður krefst þess að þú skilgreinir vöruverð og virkjar kostnaðinn í kostnaðarútgáfu. Sá kostnaður er notaður fyrir allar kvittanir og útgáfur. Frávik fyrir innhreyfingar til birgða eru skráð í fjárhag með því að nota staðlaða kostnaðarfráviksreikninga sem þú tilgreinir á **Staðalkostnaður** flipi á **Birgðafærslusnið** síðu.

Hins vegar, þegar þú notar fast kvittunarverð er aðeins kostnaðurinn fyrir kvittanir fastur og kerfið notar kostnaðinn sem þú tilgreinir á **Stjórna kostnaði** Flýtiflipi á **Útgefin vara** síðu. Mismunur á sjálfgefnu kostnaði og innkaupapöntunarverði mun valda því að frávik innkaupaverðs verður bókað á rekstrarreikninga á föstum innhreyfingarverði. Útgáfur nota ekki fast kvittunarverð. Þess í stað verða útgáfur metnar til hlaupandi meðaltals við birtingu (nema þú notir merkingu), og þau verða endurmetin í það heuristic líkan sem þú velur þegar þú keyrir birgðalokun.

### <a name="can-i-use-fefo-reservations-with-standard-costing"></a>Get ég notað FEFO bókanir með venjulegum kostnaði?

Já, þú getur notað FEFO frátekningar á vörutegundaflokki þegar þú velur staðalkostnað. FEFO frátekningar stjórna frátektarrökfræðinni sem er notuð fyrir líkamlega meðhöndlun hlutanna, en staðalkostnaður stjórnar líkamlegum og fjárhagslegum kostnaði fyrir vöru.

### <a name="can-i-upload-pending-prices"></a>Get ég hlaðið upp verðum í bið?

Já, þú getur notað Excel viðbótina eða Gagnastjórnunarrammann til að hlaða upp verð sem er í bið. Við mælum með að þú notir eftirfarandi einingar:

- Vöruverð í bið (V2)
- Kostnaðarflokkur leiðar í biðstöðu fyrir kostnaðareiningar
- Útreikningsstuðlar kostnaðarblaðshnút (V2)

### <a name="how-often-can-i-update-the-standard-cost-for-an-item"></a>Hversu oft get ég uppfært staðalkostnað fyrir vöru?

Það eru engin takmörk á tíðni sem þú getur virkjað nýjan staðalkostnað á. Ef þú virkjar nýjan kostnað fyrir vöru sama dag og síðasti kostnaður var virkjaður mun kerfið nota nýjasta virkjaða kostnaðinn við nýjar færslur eða uppfærslur (svo sem uppfærslur á núverandi færslum).

### <a name="can-i-deactivate-or-delete-an-activated-cost"></a>Get ég slökkt á eða eytt virkum kostnaði?

Nei, þú getur ekki slökkt á eða eytt virkum kostnaði. Ef þú hefur ranglega virkjað kostnað geturðu virkjað nýjan kostnað sem hefur réttan kostnað.

### <a name="are-calculation-groups-used-with-standard-costing"></a>Eru reiknihópar notaðir með staðalkostnaði?

Hægt er að nota útreikningshópa með hvaða vöru sem er, óháð vörulíkanahópnum sem þú velur. Útreikningsflokkarnir eru notaðir við kostnaðarsamsetningu eða kostnaðarútreikningsferli til að ákvarða stillingarnar sem ætti að nota fyrir vörurnar sem þú ert að keyra útreikninginn fyrir. Fyrir frekari upplýsingar um reiknihópa, sjá [BOM útreikningahópar](bom-calculation-groups.md).

### <a name="when-should-i-use-a-planned-costing-version"></a>Hvenær ætti ég að nota áætlaða kostnaðarútgáfu?

Kostnaðarútgáfur geta verið með tegund af *Staðalkostnaður* eða *Áætlaður kostnaður*. The *Staðalkostnaður* gerð er notuð fyrir þann kostnað sem er virkur í kerfinu og verður bókaður í færslum. The *Áætlaður kostnaður* gerð er notuð til að keyra eftirlíkingar á kostnaði og hefur ekki áhrif á kostnað við viðskipti.

### <a name="can-the-total-cost-from-one-entity-be-transferred-to-another-entity-as-the-selling-cost"></a>Er hægt að færa heildarkostnað frá einni aðila yfir á aðra aðila sem sölukostnað?

Það er engin sjálfvirk leið til að afrita kostnað frá einu fyrirtæki til annars. Að auki er engin sjálfvirk leið til að afrita kostnað frá innkaupsverði í söluverð. Ef fyrirtæki þitt verður að klára eitt af þessum verkefnum skaltu íhuga hvort þú getir notað gagnastjórnunarrammann til að flytja gögnin út úr kostnaðarútgáfunni þinni og hlaða inn í annað fyrirtæki, annað hvort sem söluverð í kostnaðarútgáfunni eða sem viðskiptasamningur. Handvirk meðferð á skránum gæti þurft.

### <a name="what-is-the-best-way-to-copy-planned-costs-to-a-standard-costing-version"></a>Hver er besta leiðin til að afrita fyrirhugaðan kostnað í staðlaða kostnaðarútgáfu?

Þú getur notað **Afrita** hnappinn á **Kostnaðarútgáfur** síðu til að afrita vöruverð, kostnaðarflokkaverð eða óbeinan kostnað frá einni kostnaðarútgáfu í aðra.
