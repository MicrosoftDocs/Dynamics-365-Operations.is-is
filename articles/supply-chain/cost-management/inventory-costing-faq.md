---
title: Algengar spurningar um birgðakostnað
description: Í þessari grein er svarað nokkrum algengum spurningum um birgðakostnað í Microsoft Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: 5a1d86e7e9cca159d0a820680714a08dc73c0688
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068394"
---
# <a name="inventory-costing-faq"></a>Algengar spurningar um birgðakostnað

[!include [banner](../includes/banner.md)]

Í þessari grein er svarað nokkrum algengum spurningum um birgðakostnað í Microsoft Dynamics 365 Supply Chain Management.

## <a name="inventory-close-adjustments-and-recalculation"></a>Birgðar lokun, leiðrétting og endurútreikningur

### <a name="is-the-inventory-close-required"></a>Er birgðalokunin nauðsynleg?

Ef nota á safnvistunareiginleika birgða er birgðalokun áskilin. Ef þú hyggst ekki nota safnvistunareiginleika birgða mælum við eindregið með því að þú keyrir samt birgðalokun án tillits til kostnaðarlíkananna sem þú notar.

### <a name="how-often-should-the-inventory-close-be-run"></a>Hversu oft ætti að keyra birgðalokun?

Keyra skal birgðalokun a.m.k. einu sinni á hverju reikningstímabili. Ef færslubók er til dæmis stillt á fjárhagsdagatal sem byggir á almanaksmánuði ættir þú að keyra birgðalokun einu sinni í mánuði.

### <a name="is-the-inventory-recalculation-required"></a>Er endurútreikningur birgða nauðsynlegur?

Nei, endurútreikningur á birgðum er ekki nauðsynlegur. Ef þú notar reglulegt kostnaðarlíkan, svo sem fyrst inn, fyrst út (FIFO), síðast inn, fyrst út (LIFO) eða vegið meðaltal, ættir þú að íhuga vandlega hvort endurútreikningur birgða eigi að fara fram. Það getur veitt nákvæmari kostnaðarútreikninga í nálgunarlíkönum sem þú hefur valið.

### <a name="how-often-should-the-inventory-recalculation-be-run"></a>Hversu oft ætti að keyra endurútreikning birgða?

Ef þú ætlar að framkvæma endurútreikning birgða mælum við með því að þú íhugir að keyra þær daglega sem runuvinnslu. Ef fyrirtækið þitt gerir ekki kröfu um tíðar skýrslur um birgðavirði fyrir regluleg kostnaðarlíkön getur þú íhugað að framkvæma birgðaútreikninginn sjaldnar.

### <a name="when-should-i-use-the-on-hand-inventory-adjustment-on-the-closing-and-adjustments-page"></a>Hvenær ætti ég að nota birgðaleiðréttingu lagerbirgða á síðunni Lokun og leiðrétting?

Aðeins er hægt að keyra birgðaleiðréttingu lagerbirgða eftir að birgðalokun er lokið. Hún er yfirleitt keyrð eftir síðustu lokun. Birgðaleiðrétting getur aðeins breytt birgðum sem eru enn á lager frá og með þeim degi þegar leiðréttingin er keyrð.

### <a name="when-should-i-use-the-inventory-transaction-adjustment-on-the-closing-and-adjustments-page"></a>Hvenær ætti ég að nota leiðréttingu á birgðafærslum á síðunni Lokun og leiðrétting?

Þú ættir að nota leiðréttingu birgðafærslna áður en birgðalokun er keyrð. Hún er yfirleitt notuð til að leiðrétta ranga innhreyfingu. Þú getur ekki bókað leiðréttingu á birgðafærslu eftir að birgðalokun er keyrð og færslan er jöfnuð.

### <a name="are-purchase-order-returns-treated-like-other-issues-during-the-inventory-close"></a>Eru vöruskilapantana innkaupa meðhöndluð eins og aðrar úthreyfingar á meðan birgðalokun stendur yfir eða þegar birgðir lokast?

Já. Kvittun fyrir innkaupapöntun er úthreyfing sem er jöfnuð við innhreyfingu í nálgunarlíkaninu sem þú velur fyrir vöruna. Ef þú ert að nota reglulegt kostnaðarlíkan getur þú notað merkinguna til að hnekkja kostnaði við nálgun.

### <a name="what-happens-to-sales-order-returns-during-the-inventory-close"></a>Hvað verður um sölupöntunarskil við birgðalokun?

Þegar þú keyrir birgðalokun er skil á sölupöntunum meðhöndluð sem innhreyfing inn í birgðir. Innhreyfingar eru jafnaðar á móti birgðunum, byggt á nálgunarlíkaninu sem þú velur fyrir vöruna.

### <a name="what-cost-price-is-used-on-a-sales-order-return"></a>Hvaða kostnaðarverð er notað við skil á sölupöntun?

Þegar þú stofnar skilagrein sem tengist sölupöntun er verðgildi reitsins **Einingarverð** afritað úr upprunalegu sölupöntuninni og reiturinn **Skilakostnaðarverð** er stillt á aðlagað kostnaðarverð úr upprunalegu birgðafærslunni fyrir sölupöntunarlínuna sem verið er að skila. Ef valkosturinn **Opið gildi** tengdrar birgðafærslu er stilltur á *Já*, getur birgðalokun valdið uppfærslum á útgáfukostnaði upprunalegu sölupöntunarinnar. Reiturinn **Skilakostnaðarverð** er ekki uppfærður við þessar aðstæður. Hins vegar þegar fylgiseðilinn fyrir vöruskilapöntunina er bókaður mun kerfið athuga kostnaðarverð og nota uppfærðan kostnað á birgðafærslu skila.

Fyrir skil á staðlaðri kostnaðarvöru sem tengist sölupöntun mun kerfið nota staðlaða kostnaðinn frá þeim tíma sem upprunalegu sölupöntunin er gerð, jafnvel þótt nýr staðlaður kostnaður sé virkur fyrir vöruna.

Þegar þú stofnar skil sem tengjast ekki sölupöntun er reiturinn **Skilakostnaðarverð** stillt á virkt vöruverð sem þú ert með fyrir vöruna á vefsvæðinu sem þú ert að búa til skilapöntunina fyrir. Ef þú ert ekki með virkt kostnaðarverð í kostnaðarútgáfu vörunnar verður gildið 0 (núll). Ef þú skilur gildið eftir sem 0 (núll) færðu viðvörun sem segir að lotukenni skila eða kostnaðarverð sé ekki tilgreint.

### <a name="what-is-the-expected-performance-of-the-inventory-close"></a>Hver eru áætluð afköst birgðalokunar?

Margir þættir geta haft áhrif á afköst birgðalokunar. Meðal þessara þátta eru heildarfjöldi vara, heildarfjöldi færslna á tímabilinu, birgðalíkönin sem þú notar og fjöldi aukahjálpara runu sem þú stillir í færibreytum birgða- og vöruhúsakerfis. Þú getur búist við því að lokunin gæti tekið aðeins nokkrar mínútur eða um nokkrar klukkustundir. Engar sérstakar leiðbeiningar eru til um þann tíma sem keyrsla lokunar skuli taka. Þú ættir að skilgreina viðskiptakröfur þínar sem ekki eru sértækar fyrir afköst birgðalokunar og vinna náið með samstarfsaðila þínum til að skilgreina áætlunina fyrir keyrslu birgðalokununarferli. Ef þú sérð óvænt litlum árangri við afköst birgðalokununarferlis ættir þú að opna þjónustubeiðni.

## <a name="costing-sheet-and-indirect-costs"></a>Kostnaðarskjal og óbeinn kostnaður

### <a name="which-costing-models-support-the-costing-sheet"></a>Hvaða kostningslíkön styðja kostnaðarskjalið?

Þó að kostnaðarblaðið sé yfirleitt notað í fyrirtækjum sem nota staðlaða kostnaðarútreikning, geturðu notað það með öllum kostnaðarlíkönum sem eru í boði í Supply Chain Management.

### <a name="can-i-have-multiple-costing-sheets-for-various-parts-of-my-organization"></a>Get ég notað mörg kostnaðarskjöl fyrir mismunandi hluta fyrirtækisins?

Nr. Aðeins er hægt að vera með eitt kostnaðarskjal fyrir hvern lögaðila.

### <a name="can-i-have-different-costing-sheets-for-each-site"></a>Get ég haft mismunandi kostnaðarskjöl fyrir hvert vefsvæði?

Nei, þú getur ekki verið með mismunandi kostnaðarskjöl fyrir hvert vefsvæði. Einungis er hægt að stofna eitt kostnaðarskjal fyrir hvern lögaðila. Hins vegar er hægt að stilla heildar hnúta, kostnaðarhópa eða óbeina kostnaðarhnúta fyrir hvert vefsvæði. Þessi stilling er handvirkt ferli og þú verður að viðhalda stigveldi og vöruúthlutunum á kostnaðarskjalinu þegar skipulags- eða rekstrarbreytingar eiga sér stað. Ef ein vara er framleiddur eða keyptur á fleiri en einu vefsvæði er ekkert ferli sem gerir þér kleift að meðhöndla vöruna á annan hátt á kostnaðarskjalin fyrir hvert vefsvæði. Athugaðu einnig að allir óbeinir kostnaðarhnútar eru með verð eða aukagjald sem er skilgreint í kostnaðarútgáfu þinni. Kostnaðurinn sem þú skilgreinir er alltaf sértækur fyrir vefsvæðið þitt.

### <a name="can-i-deactivate-and-activate-versions-of-the-costing-sheet"></a>Get ég afvirkjað og virkjað útgáfur af kostnaðarskjalinu?

Þrátt fyrir að ekki sé haldin ítarleg útgáfuferill fyrir kostnaðarskjalið er hægt að gera breytingar á kostnaðarskjalinu og vista og staðfesta það svo þegar allt er til reiðu. Það er enginn ferli sem leyfir þér að fara aftur í eldri útgáfu af kostnaðarskjalinu eða skoða breytingarnar sem voru gerðar á kostnaðarskjalinu. Ef þú byrjar á breytingum og vilt ekki að þær taki gildi geturðu lokað síðunni án þess að vista og staðfesta breytingarnar. Þú verður beðin/n um að fleygja breytingum.

### <a name="can-i-create-indirect-costs-for-each-item"></a>Get ég stofnað til óbeins kostnaðar fyrir hverja vöru?

Á kostnaðarskjali þínu getur þú búið til óbeina kostnaðarkóða þar sem reiturinn **Hnútagerð** er stilltur á *Aukagjald*, *Verð* eða *Byggir á úttakseiningu*. Þá er hægt að skilgreina verð eða aukagjald þannig að það sé tilgreint í vörunúmeri. Á flýtiflipanum **Verð** eða **Aukagjald** skaltu bæta við línu á hnitanetið. Stilltu reitinn **Gildir fyrir** á *töflu* og reitinn **Tengsl** við tiltekið vörunúmer.

### <a name="can-i-create-an-indirect-cost-that-isnt-related-to-a-specific-item"></a>Get ég stofnað til óbeins kostnaðar sem tengist ekki tiltekinni vöru?

Já. Hægt er að búa til óbeinan kostnaðarkóða þar sem reiturinn **Hnútagerð** er stilltur á *Byggir á úttakseiningu*. Þú getur síðan stillt reitinn **Undirgerð** á *Magn*, *Þyngd* eða *Rúmmál* til að tilgreina magn, þyngd eða rúmmál vörunnar sem þú ert að framleiða. Verðið sem þú tilgreinir í flýtiflipanum **Verð** verður notað á undirtegundina sem þú valdir. Til dæmis stillir þú reitinn **Undirtegund** á *Magn* og reitinn **Verð** á *1,00 USD* og býrð síðan til framleiðslu eða runupöntun fyrir magnið 10. Í þessu tilviki er óbeinn kostnaður sem bætist við fullunnin vara 10,00 USD.

### <a name="can-i-use-the-costing-sheet-to-split-my-production-costs-by-hours-and-materials"></a>Get ég notað kostnaðarskjal til að skipta framleiðslukostnaði mínum eftir tímum og efnum?

Já. Þú getur búið ti hnúta **Samtals** á kostnaðarskjali þitt til að aðskilja kostnaðinn eftir flokkum að eigin vali. Til dæmis er hægt að stofna einn hnút **Samtals** sem er nefndur *Klukkustundir* og annan sem er nefndur *Efni*. Undir hnútnum **Klukkustundir** bætir þú við hverjum kóðaflokki sem tengist klukkustundum þínum. Undir hnútnum **Efni** bætir þú við hverjum kostnaðarflokki sem tengist efnunum þínum.

## <a name="dimension-groups"></a>Víddaflokkar

### <a name="can-i-manage-cost-at-the-batch-or-serial-number-level"></a>Get ég stjórnað kostnaði á runu- eða raðnúmerastiginu?

Já, ef þú ert að nota reglulegt kostnaðarlíkan eins og FIFO, LIFO, LIFO dagsetning, vegið meðaltal eða vegið meðaltal dagsetninga geturðu virkjað valkostinn **Fjárhagslegar birgðir** fyrir víddina **Runa** eða **Raðnúmer** í rakningarvíddarhópnum til að rekja kostnað á ítarlegu stigi.

### <a name="can-i-manage-costs-at-the-location-level"></a>Get ég stjórnað kostnaði á staðsetningastigi?

Nei, þú getur ekki virkjað valkostinn **Fjárhagslegar birgðir** fyrir víddina **Birgðir** í geymsluvíddaflokknum. Ef fyrirtækið þitt verður að rekja kostnað á ítarlegra stigi, íhugaðu þá hvort þú getir búið til sýndarvöruhús og veldu síðan valkostinn **Fjárhagslegar birgðir** fyrir víddina **Vöruhús** í geymsluvíddarhópnum þínum.

### <a name="should-i-enable-the-use-warehouse-management-processes-option-for-the-storage-dimension-group"></a>Ætti ég að virkja valkostinn vöruhúsakerfisferli fyrir geymsluvíddarflokkinn?

Ef þú heldur að þú viljir nota vöruhúsakerfisferli (WMS) í framtíðinni ættir þú að virkja valkostinn **Nota vöruhúsakerfisferli**. Eftir að þú vistar geymsluvíddarflokk geturðu ekki lengur breytt stillingum valkostsins **Nota vöruhúsakerfisferli** fyrir hann. Ef þú ákveður að nota vöruhúsakerfisferli síðar verður þú að búa til nýtt vöruhús þar sem valkosturinn er virkur. Það er ekkert sjálfvirkt ferli sem þú getur notað til að færa allar birgðir úr einu vöruhúsi í annað vöruhús, eða til að afrita tengdar stillingar yfir í nýtt vöruhús.

### <a name="can-i-enable-the-use-warehouse-management-processes-for-the-storage-dimension-group-even-if-im-not-planning-to-use-warehouse-management-processes-wms"></a>Get ég virkjað vöruhúsakerfisferli fyrir geymsluvíddarflokkinn jafnvel þótt ég hyggist ekki nota vöruhúsakerfisferli (WMS)?

Já, jafnvel þótt þú ætlir ekki að nota vöruhúsakerfisferli (WMS) geturðu virkjað valkostinn **Nota vöruhúsakerfisferli** fyrir geymsluvíddarflokkinn. Til að búa til og vinna úr færslum þarftu að ljúka lágmarksstillingum, svo sem frátekningarstigveldi og röðunarflokkar einingar. Hins vegar eru stillingar fyrir WMS almennt hunsaðar þegar þú vinnur handvirkt úr tiltektarlistum, fylgiseðlum og innhreyfingarskjölum (til dæmis á síðum sölupöntunar og innkaupapöntunar).

### <a name="when-should-i-enable-the-physical-inventory-option-for-a-storage-or-tracking-dimension-group"></a>Hvenær ætti ég að virkja valkostinn Efnislegar birgðir fyrir geymslu- eða rakningarvíddaflokk?

Þú ættir að virkja valkostinn **Efnislegar birgðir** fyrir geymslu- og rakningarvíddarhópa þegar þú verður að halda ítarlegar birgðaupplýsingar byggðar á þeirri vídd. Yfirleitt verða allar virkar víddir einnig raktar efnislega. Þess vegna munu allar innhreyfingar, úthreyfingar eða hreyfingar vörubirgða vera raktar af völdu víddinni. Ef stærð er ekki áskilin (til dæmis númeraplatan) er hægt að virkja valkostinum **Auð innhreyfing heimil** og **Auð úthreyfing leyfð** til að leyfa notendum að taka á móti, gefa út eða færa birgðir jafnvel þótt víddin sé ekki tilgreind.

### <a name="when-should-i-enable-the-financial-inventory-option-for-a-storage-or-tracking-dimension-group"></a>Hvenær ætti ég að virkja valkostinn Fjárhagslegar birgðir fyrir geymslu- eða rakningarvíddaflokk?

Þú ættir að virkja valkostinn **Fjárhagslegar birgðir** fyrir geymslu- eða rakningarvíddaflokk þegar þú verður að halda ítarlegar fjárhagslegar skrár byggðar á þeirri vídd. Stærðir **Vefsvæðisins** eru alltaf raktar fjárhagslega en aðrar víddir eru valfrjálsar til fjárhagslegrar rakningar. Ef þú notar reglulegt kostnaðarlíkan eins og FIFO, LIFO eða vegið meðaltal og virkjar valksotinn **Fjárhagslegar birgðir** fyrir vídd gefur það til kynna að þú munir aðeins gera uppgjör í þeim tilvikum þar sem inn- og úthreyfing hafa sömu víddargildi. Til dæmis, ef þú virkjar valkostinn **Fjárhagslegar birgðir** fyrir víddina **Vöruhús+a**, verður kostnaður mismunandi í hverju vöruhúsi og ekki er hægt að ganga frá inn- og úthreyfingum öðru vöruhúsi.

### <a name="can-i-make-changes-to-a-product-storage-or-tracking-dimension-group-after-transactions-exist"></a>Get ég gert breytingar á vöru, geymslu eða rakningarvíddarflokk eftir að færslur eru til?

Eftir að þú hefur búið til vörulíkanaflokk getur þú breytt stillingu reitanna **Þekjuáætlun eftir vídd**, **Vegna innkaupsverðs** og **Vegna söluverðs** ef hakað er í gátreitinn **Virkt** fyrir vídd í vörulíkanaflokknum. Aðrar breytingar eru ekki leyfilegar. Til dæmis er ekki hægt að virkja eða slökkva á valkostunum **Virkt**, **Auð úthreyfing leyfð**, **Auð innhreyfing leyfð**, **Efnislegar birgðir** og **Fjárhagslegar birgðir**.

### <a name="can-i-change-the-product-storage-or-tracking-dimension-group-for-a-released-product"></a>Get ég breytt vöru-, geymslu- eða rakningarvíddarflokki fyrir útgefna vöru?

Ef lagerbirgðir vöru eru 0 (núll) og valkosturinn **Opið** er stilltur á *Nei* fyrir allar birgðafærslur er hægt að breyta geymslu- og rakningarvíddarflokkum á síðunni fyrir útgefnar framleiðslupantanir. Ekki er hægt að breyta vöruvíddarhópnum eftir að færslan er búin til.

## <a name="item-model-groups"></a>Vörulíkanaflokkar

### <a name="when-should-i-enable-the-stocked-product-option"></a>Hvenær ætti ég að virkja valkostinn Vara á lager?

Þú ættir að virkja valkostinn **Vara á lager** fyrir allar vörur sem verða raktar í birgðum þínum. Þegar þessi valkostur er virkjaður er haldið utan um ítarlegar birgðafærslur sem halda utan um inn- og úthreyfingar vörunnar. Þessi valkostur er yfirleitt virkur fyrir allar efnislegar vörur sem þú geymir í vöruhúsi þínu, til dæmis. Þú ættir einnig að virkja þennan valkost ef þú hyggst bæta óefnislegum vörum eins og þjónustuvöru við uppskriftirnar eða formúlurnar. Ef þú virkjar ekki valkostinn **Vara á lager** eru engar birgðafærslur raktar í undirbók birgða og kostnaður við vörurnar yfirleitt greiddur inn á fjárhag. Þessi valkostur er til dæmis oft notaður fyrir vörur eða þjónustu verslunar sem er ekki innifalin í uppkriftum þínum eða formúlum.

### <a name="when-should-i-enable-the-post-physical-inventory-option"></a>Hvenær ætti ég að virkja valkostinn Bóka efnislegar birgðir?

Valkosturinn **Bóka efnislegar birgðir** er yfirleitt virkjaður þegar valkosturinn **Vara á lager** er virkjaður. Þegar þú virkjar þennan valkost mun kerfið rekja raunverulegar uppfærslum á vörunni í birgðafærslunni. Þessi valkostur er notaður í samhæfingu við færibreytur í viðskiptaskuldum, viðskiptakröfum og Framleiðslustýringu sem tilgreina að raunveruleg uppfærsla ætti að búa til afsláttarmiða. Þú virkjar þennan valkost yfirleitt þegar þú vilt að fjárhagur sé uppfærð í hvert sinn sem þú raunverulega uppfærir birgðirnar. Ef Supply Chain Management er skráarkerfi þitt fyrir Financials gætirðu viljað gera þennan valkost óvirkan.

### <a name="when-should-i-enable-the-post-financial-inventory-option"></a>Hvenær ætti ég að virkja valkostinn Fjárhagslegar birgðir?

Valkosturinn **Bóka fjárhagslegar birgðir** er yfirleitt virkjaður þegar valkosturinn **Vara á lager** er virkjaður. Þessi valkostur er notaður í samhæfingu við færibreytur í viðskiptaskuldum, viðskiptakröfum og Framleiðslustýringu sem tilgreina að fjármála uppfærsla ætti að búa til afsláttarmiða. Þú virkjar þennan valkost yfirleitt þegar þú vilt að fjárhagur sé uppfærð í hvert sinn sem þú fjárhagslega uppfærir birgðirnar (t.d. með reikningsfærslu sölupantana og innkaupapantana eða til að ljúka framleiðslupöntun). Ef Supply Chain Management er skráarkerfi þitt fyrir Financials gætirðu viljað gera þennan valkost óvirkan.

### <a name="when-should-i-enable-the-post-to-deferred-revenue-account-on-sales-delivery-option"></a>Hvenær ætti ég að virkja valkostinn Bóka á lykil fyrir frestaðar tekjur á söluafhendingu?

Þú notar valmöguleikann **Bóka á lykil fyrir frestaðar tekjur á söluafhendingu** til að gefa til kynna hvort þú viljir færa tekjur í fjárhagur þegar þú setur inn fylgiseðil fyrir sölupöntun. Þessi valkostur er yfirleitt notaður þegar langt bil er á milli fylgiseðils og reiknings á sölupöntun eða þegar ekki er hægt að reikningsfæra allar sölupantanir á tímabilinu. Venjulega gerir þú þennan valkost óvirkan ef þú bókar sölupöntunarreikningana þína strax eftir að þú bókar fylgiseðilinn. Á þennan hátt er hægt að komast hjá því að búa til fjárhagsbókunarfærslur sem verða umsvifalaust bakfærðar þegar sölupöntun er reikningsfærð.

### <a name="when-should-i-enable-the-accrue-liability-on-product-receipt-option"></a>Hvenær ætti ég að virkja valkostinn Safna upp skuld á innhreyfingarskjali?

Í flestum fyrirtækjum munt þú vilja virkja valkostinn **Safna upp skuld á innhreyfingarskjali** fyrir alla vörulíkanaflokka, óháð því hvort þú ert með vöru á lager eða ekki. Þessi valmöguleiki er notaður til að bóka uppsöfnun í fjárhagur, miðað við verð innhreyfingarskjals afurða. Vegna þess að það er yfirleitt bil á milli bókunar innhreyfingarskjals fyrir innkaupapöntun og bókunar reiknings verða flest fyrirtæki að taka ábyrgð á efnahagsreikningi til að uppfylla gildandi reglur á hverjum stað eins og almennt samþykkt bókhaldsvenjum (GAAP). Ef Supply Chain Management er skráarkerfi þitt fyrir Financials gætirðu viljað gera þennan valkost óvirkan. Ef fyrirtæki notar innkaupaflokka í innkaupapöntunum er hægt að stýra uppsöfnunarkröfunni með því að virkja valkostinn **Safna upp innkaupakostnaði á kvittun** fyrir stefnureglu tegunda á síðunni **Innkaupareglur**.

### <a name="how-can-i-prevent-a-user-from-posting-a-purchase-order-product-receipt-if-a-receipt-registration-isnt-yet-posted"></a>Hvernig get ég komið í veg fyrir að notandi bóki innhreyfingarskjal afurðar á innkaupapöntun ef skráning innhreyfingarskjala er ekki enn bókuð?

Þú getur komið í veg fyrir að notandi bóki innhreyfingarskjal á innkaupapöntun ef skráning innkaupapöntunar hefur ekki enn farið fram með því að virkja valkostinn **Skráningarkröfur** fyrir vörulíkanaflokkinn. Þessi valkostur er yfirleitt notaður hjá fyrirtækjum sem nota tveggja skrefa móttökuferli eða í aðstæðum þar sem þú verður að skrá runu- eða raðnúmer, til dæmis fyrir vörurnar sem þú tekur á móti. Valkosturinn **Skráningarkröfur** á við um *allar* innhreyfing birgða fyrir vöru, ekki bara innkaupapantanir. Til dæmis á það við um birgðabók sem hefur jákvætt magn og skýrslu um framleiðslupöntun sem tilbúna færslubók.

### <a name="how-can-i-prevent-a-user-from-posting-a-purchase-order-invoice-if-a-product-receipt-isnt-yet-posted"></a>Hvernig get ég komið í veg fyrir að notandi bóki innhreyfingarskjal ef innhreyfingarskjal er ekki enn bókað?

Þú getur komið í veg fyrir að notandi bóki innhreyfingarskjal afurðar ef innhreyfingarskjal afurðar hefur ekki enn komið fram með því að virkja valkostinn **Kröfur mótteknar** fyrir vörulíkanaflokkinn. Þessi valkostur er yfirleitt notaður í fyrirtækjum sem krefjast þess að innhreyfing séu raunverulegar færðar í fjárhag til uppsöfnunar. Valkosturinn **Kröfur mótteknar** á við um *allar* innhreyfing birgða fyrir vöru, ekki bara innkaupapantanir. Til dæmis á það við um birgðabók sem hefur jákvætt magn og skýrslu um framleiðslupöntun sem tilbúna færslubók. Ef fyrirtæki notar innkaupaflokka í innkaupapöntunum er hægt að stýra kröfunni fyrir skjali með því að virkja valkostinn **Kröfur mótteknar** fyrir stefnureglu tegunda á síðunni **Innkaupareglur**.

### <a name="how-can-i-prevent-a-user-from-posting-a-sales-order-packing-slip-if-a-sales-order-picking-list-isnt-yet-posted"></a>Hvernig get ég komið í veg fyrir að notandi bóki fylgiseðil sölupöntunar ef ekki er búið að birta tiltektarlista vegna sölupöntunar?

Þú getur komið í veg fyrir að notandi bóki fylgiseðil eða reikning sölupöntunar ef tiltektarlisti sölupöntunar hefur ekki enn farið fram með því að virkja valkostinn **Tiltektarkröfur** fyrir vörulíkanaflokkinn. Þessi valkostur er yfirleitt notaður í fyrirtækjum sem sinna efnislegri tiltekt í vöruhúsinu (til dæmis með því að nota fartæki vöruhúss við tiltekt). Valkosturinn **Kröfur tiltektar** á við um *allar* úthreyfingar birgða fyrir vöru, ekki bara sölupantanir. Til dæmis á það við um birgðabók sem hefur neikvætt magn og færslubók tiltektarlista framleiðslupöntunar.

### <a name="how-can-i-prevent-a-user-from-posting-a-sales-order-invoice-if-the-sales-order-packing-slip-isnt-yet-posted"></a>Hvernig get ég komið í veg fyrir að notandi bóki sölupöntunarreikning ef ekki er búið að bóka fylgiseðil sölupöntunar?

Þú getur komið í veg fyrir að notandi bóki sölupöntunarreikning ef fylgiseðill sölupöntunar hefur ekki enn farið fram með því að virkja valkostinn **Frádráttarkröfur** fyrir vörulíkanaflokkinn. Þessi valkostur er yfirleitt notaður í fyrirtækjum sem sinna efnislegu pökkunarferli í vöruhúsinu (t.d. með því að nota farsímaforrit vöruhúsastjórnunar við pökkun eða búa til skjal sem verður sent með vörunum). Valkosturinn **Tiltektarkröfur** á við um *allar* úthreyfingar birgða fyrir vöru, ekki bara sölupantanir. Til dæmis á það við um birgðabók sem hefur neikvætt magn og færslubók tiltektarlista framleiðslupöntunar.

### <a name="can-i-prevent-items-that-are-registered-from-being-sold"></a>Get ég komið í veg fyrir að skráðar vörur séu seldar?

Þegar vara er skráð í birgðir í Supply Chain Management er magnið efnislega tiltækt til að gefa út í kerfinu. Ef vara sem hafa verið skráðir en hafa ekki enn verið mótteknir ætti *ekki* að vera hægt að gefa út sölupantanir eða framleiðslupantanir, til dæmis, íhuga að nota birgðastöðu, birgðalæsingu, gæðapantanir, biðgeymslupantanir eða frátekningareiginleika til að hafa umsjón með viðskiptaferlinu.

## <a name="production-costing"></a>Framleiðsla – kostnaður

### <a name="can-i-use-one-costing-model-for-raw-materials-and-a-different-costing-model-for-finished-goods"></a>Get ég notað eitt kostnaðarlíkan fyrir hráefni og annað kostnaðarlíkan fyrir fullunnar vörur?

Já, þú getur notað mismunandi kostnaðarlíkön fyrir hverja vöru. Það er ekki óalgengt að framleiðendur noti reglulegt kostnaðarlíkan fyrir hráefni og staðlaðan kostnað fyrir hálfunnar og fullunnar vörur.

### <a name="how-can-i-drive-overhead-off-machine-costs"></a>Hvernig get ég losað vélarkostnað við sameiginlegur kostnað?

Til að losa vélakostnað við sameiginlegur kostnaður verður þú að búa til tilföng og tilfangaflokkur fyrir hverja vél í samræmi við viðskiptakröfur þínar. Hvert tilfang eða tilfangaflokkur getur verið úthlutað til kostnaðarflokka til að stjórna kostnaði við vélina. Hægt er að tengja hvern kostnaðartegund við kostnaðarflokk og nota hvern kostnaðarflokk til grundvallar útreiknings á óbeinum kostnaði á kostnaðarskjalinu.

### <a name="how-do-i-recognize-cost-that-is-related-to-energy-consumption-for-example-water-energy-or-gas-consumption-on-the-costing-sheet"></a>Hvernig þekki ég kostnað sem tengist orkunotkun (til dæmis vatns-, orku- eða gasnotkun) á kostnaðarskjalinu?

Yfirleitt er hægt að þekkja kostnað sem tengist orkunotkun á tvo vegu:

- Búðu til línu í uppskriftinni þinni eða formúlunni. Venjulega er þessi lína búin til sem þjónustuvara og þú getur tilgreint mælieininguna sem þú ert að nota í tengslum við magnið sem þú ert að framleiða. Þannig getur notandinn notað mismikils magns meðan á framleiðsluferlinu stendur. Þú getur sjálfkrafa notað hlutanna miðað við gildið sem er valið í reitnum **Losunarregla**.
- Stofnaðu óbeinan kostnað á kostnaðarskjalið þitt. Venjulega er þessi aðferð notuð til að úthluta heildarkostnaði orkunotkunar í framleiðsluferlinu. Hægt er að nota kostnaðarflokkinn og hagnýtingargrunn til að kvarða notkunina út frá efnum eða vinnu í leið þinni, til dæmis.

Þú ættir að velja besta valkostinn, byggðan á kröfum þínum um skýrslugerð, afstemmingu og rekstur.

### <a name="can-i-capture-resource-details-in-the-bom-or-formula"></a>Get ég fangað upplýsingar í uppskriftinni eða formúlunni?

Aðeins er hægt að fanga upplýsingar um tilföng í leiðaraðgerð. Þrátt fyrir að þú getir búið til þjónustuvöru til að tákna tilfangd og úthlutað kostnaði til að auka kostnaðarútreikning fyrir fullunna vöru mælum við yfirleitt ekki með þessari aðferð. Þess í stað mælum við með því að þú búir til einfalda leið sem hefur eina línu til að fylgjast með tilfangakostnaði og stillir aðgerðina þannig að hennar sé sjálfkrafa notað við upphaf eða lok framleiðslupöntunar.

### <a name="can-i-view-the-calculation-details-if-the-cost-is-manually-entered"></a>Get ég skoðað útreikningsupplýsingar ef kostnaðurinn er sleginn inn handvirkt?

Nr. Ef þú slærð handvirkt verðið á síðunni **Vöruverð** eru hnapparnir **Skoða útreikningsupplýsingar** og **Skrá upplýsingar útreiknings** ekki tiltækir. Ef þú velur hnappinn **Kostnaður tekinn eftir kostnaðarflokki** fyrir kostnaðarverð sem er slegið inn handvirkt, birtist samantekin lína og öllum kostnaði er velt upp að fullunninni góðri vöru.

### <a name="does-the-system-calculate-variances-on-a-production-order-when-i-manually-enter-the-cost"></a>Reiknar kerfið frávik á framleiðslupöntun þegar ég slæ inn kostnaðinn handvirkt?

Já, kerfið reiknar út frávik þegar þú slærð inn staðalkostnað handvirkt. Hins vegar, þegar þú slærð inn staðalkostnað í stað þess að reikna hann út, er litið á allt efni, leið og óbeina kostnaðar notkun í framleiðslupöntun sem frávik. Ef viðbótarfrávik koma fram, svo sem notkun efna eða vinnuafls til viðbótar verða þau einnig skráð sem frávik frá framleiðsluuppskrift. Því mælum við eindregið með því að þú gangir alltaf frá útreikningum fyrir hluti sem eru með uppskrift, leið eða óbeinan kostnað.

### <a name="how-can-i-carry-the-variances-from-a-subproduction-order-to-the-parent-production-order"></a>Hvernig get ég borið frávik undirframleiðslupöntunar saman við yfirframleiðslupöntunar?

Þegar þú notar reglulegt kostnaðarlíkan eins og FIFO, LIFO eða vegið meðaltal er kostnaður vegna undirframleiðslu viðurkenndur í nálgunarlíkaninu sem þú valdir fyrir vörurnar. Ef þú þarfnast raunverulegs kostnaðar skaltu íhuga að nota merkingarregluna til að gefa til kynna hvaða undirframleiðsla er gefin út á yfirframleiðslupöntun. Að öðrum kosti skaltu íhuga að nota valkostinn **Fjárhagslegar birgðir** fyrir víddina **Runa** eða **Raðnúmer** í rakningarvíddarflokknum, til dæmis.

### <a name="how-does-the-flushing-principle-affect-consumption"></a>Hvernig hefur losunarreglan áhrif á notkun?

Losunarregla í uppskrift, formúlu eða leiðarlínu stjórnar tímasetningu og tækni sem er notuð til að nota hlutinn eða vinnuna. Ef þú velur *Ræsa* er varan eða vinnan sjálfkrafa notuð þegar þú ræsir framleiðslupöntunina. Ef þú velur *Ljúka* er varan eða vinnan sjálfkrafa notuð þegar þú lýkur framleiðslupöntunina. Ef valið er *Handvirkt* verður notandi að velja efni handvirkt, eða skrá tímann í verkbók eða færslubók leiðarspjalda. Uppskriftir og formúlur hafa einnig valkost *Tiltækt á staðnum*. Ef þessi kostur er valinn eru vörurnar sjálfkrafa notaðar eftir að þau eru flutt á staðsetningu á framleiðslugólfið.

### <a name="how-should-i-run-cost-calculations-if-i-have-multi-level-boms-or-formulas"></a>Hvernig á ég að keyra kostnaðarútreikninga ef ég er með fjölþrepa uppskriftir eða formúlur?

Almennt er mælt með því að byrja á lægsta stigi uppskriftar eða formúlu fyrir útreikninginn. Til að auðvelda síun þegar fjöldakeyrðir kostnaðarútreikningar eru gerðir er hægt að nota reikniflokka til að hjálpa til við að aðskilja vörur. Einnig er mælt með því að endurreikna *Endurreikna uppskriftarstig* en hafist er handa við útreikninga á fjölda-keyrðum kostnaði. Hver fyrirtæki ætti að íhuga samsetningu vara og skilgreina áætlun sem uppfyllir sértækar þarfir vörunnar þinnar og uppskriftar- eða formúluuppbyggingu.

## <a name="transfer-order-costing"></a>Kostnaðarútreikningur flutningspöntunar

### <a name="is-there-a-way-to-allocate-freight-to-a-transfer-order-cost"></a>Er til leið til að úthluta farmi í kostnað flutningspöntunar?

Þú getur bætt gjöldum við flutningspöntun til að bæta við kostnaði. Gjaldakóði skilgreinir debet- og kredit fyrir gjald sem þú bætir við. Fyrst verður að búa til gjaldkóða í einingunni **Birgðastjórnun**. Til að bæta gjald við flutningspöntun er valið **Gjöld** á flutningspöntunarlínunni sem þú vilt bæta gjaldi við.

## <a name="variances"></a>Frávik

### <a name="can-i-treat-variances-differently-based-on-the-site-or-warehouse"></a>Get ég meðhöndlað frávik á annan hátt, á grundvelli vefsvæðisins eða vöruhússins?

Enginn valkostur er til staðar til að stilla fráviksreikninga eftir svæðum. Þegar hefðbundinn kostnaður er notaður fyrir útgefna vöru er hægt að velja aðallykilubb sem er notaður fyrir hefðbundnar bókanir á fráviki kostnaðar á síðunni **Bókanir**. Þú getur valið að stilla reikningana fyrir eina vöru, flokk vara eða allar vörur. Þú getur einnig stillt einn kostnaðarhóp, hóp kostnaðarhópa eða alla kostnaðarhópa.

### <a name="can-i-separate-variances-that-are-the-result-of-currency-exchange-rates-from-other-types-of-variances"></a>Get ég aðskilið frávik sem eru afleiðing af gengi gjaldmiðla frá öðrum tegundum frávika?

Ef frávik er afleiðing gengismunar á milli verðs innkaupapöntunar og staðlaðs kostnaðar fyrir vöru er engin leið að skilja gengismuninn frá öðrum frávikum.

## <a name="reporting"></a>Skýrslugerð

### <a name="how-many-inventory-value-report-configurations-can-i-create-and-use"></a>Hversu margar birgðavirðisskýrslugerðir get ég búið til og notað?

Engin takmörk eru á fjölda skilgreininga birgðavirðisskýrslna sem er hægt að búa til. Þú ættir að meta sérstakar skýrslukröfur þínar og búa til þann fjölda stillinga sem þarf til að uppfylla þessar kröfur. Þú þarft að minnsta kosti eina stillingu fyrir birgðavirðisskýrslu til að keyra skýrsluna eða geymsluvalkost skýrslu.

### <a name="can-i-use-the-inventory-value-report-to-analyze-the-cost-of-an-item-in-each-warehouse"></a>Get ég notað birgðavirðisskýrsluna til að greina kostnað vöru í hverju vöruhúsi?

Já. Þú getur virkjað valkostinn **Skoða** eða **Samtals** fyrir hverja vídd **Vöruhús** í stillingu birgðavirðisskýrslu. Hins vegar mun skýrslan aðeins sýna gildi fyrir víddir þar sem valkosturinn **Fjárhagslegar birgðir** er virkur fyrir geymsluvíddarhópinn. Fyrir aðrar víddir mun það sýna auða dálka. Frekari upplýsingar eru í [Dæmi og rök fyrir birgðavirðisskýrslu](inventory-value-report-examples.md).

### <a name="how-can-i-view-the-inventory-quantity-as-of-a-specific-date-with-the-weighted-average"></a>Hvernig get ég litið á birgðamagn sem tiltekna dagsetningu með vegnu meðaltali?

Hægt er að nota skýrsluna **Aldursdreifing birgða**, sem inniheldur dálkinn **Meðalkostnaður vöru** sem sýnir gildi birgða frá og með tiltekinni dagsetningu. Frekari upplýsingar eru í [Dæmi og rök fyrir aldursgreiningarskýrslu birgða](inventory-aging-report.md).

### <a name="how-can-i-view-which-receipt-transactions-are-settled-against-an-issue-transaction"></a>Hvernig get ég skoðað hvaða innhreyfingarfærslur eru afgreiddar gegn úthreyfingarfærslu?

Hægt er að skoða uppgjör vegna birgðafærslu með því að velja **Uppgjör** eða **Kostnaðarkanni** á flipanum **Birgðir** á aðgerðasvæði síðunnar **Birgðafærsla** eða **Upplýsingar um birgðafærslu**. Ef þú velur kvittun til að skoða úthreyfingar sem tengjast færslunni sýnir kostnaðarkanninn ekki upplýsingarnar. Upplýsingar eru aðeins sýndar ef þú velur úthreyfingarfærsla.

### <a name="how-does-the-inventory-value-report-show-items-that-have-a-positive-physical-quantity-and-a-negative-financial-value"></a>Hvernig sýnir birgðavirðisskýrslan vörur sem hafa jákvætt efnislegt magn og neikvætt fjárhagslegt gildi?

Birgðavirðisskýrslan aðgreinir efnislegar og fjárhagslegar fjárhæðir og magn í eigin dálka. Gildin sem koma fram í skýrslunni eru þau sömu og fyrir tímabilið sem þú valdir þegar þú keyrðir skýrsluna. Hversu mikil samantekt er sýnd fer eftir því hvaða stillingar eru valdar. Ef hlutur hefur færslur sem hafa verið gefnar út efnislega og fjárhagslega eru magn og gildi eru teknar saman sjálfstætt. Ef valið er að skoða upplýsingastig sem færslur eru línur fyrir hverja innhreyfingu og úthreyfingu sýndar sérstaklega og efnislegt og fjárhagslegt magn og upphæðir, tilgreint í sömu röð, sýndar. Frekari upplýsingar eru í [Dæmi og rök fyrir birgðavirðisskýrslu](inventory-value-report-examples.md).

### <a name="what-is-the-impact-of-storage-and-tracking-dimension-groups-on-the-inventory-value-report"></a>Hver eru áhrif geymslu- og rakningarvíddarflokka á birgðavirðisskýrsluna?

Ef þú virkjar valkostinn **Fjárhagslegt gildi** fyrir vídd í geymslu- eða rakningarvíddarflokki, getur þú valið valkostinn **Skoða** eða **Samtals** fyrir víddina í stillingum birgðavirðisskýrslu. Ef valkosturinn **Skoða** eða **Samtals** er valinn fyrir vídd þar sem valkosturinn **Fjárhagslegt gildi** er ekki valinn verður dálkurinn auður í skýrslunni. Ef þú hefur virkjað valkostinn **Fjárhagslegt gildi** fyrir vídd í geymslu- eða rakningarflokki, og þú velur ekki valkostinn **Skoða** eða **Samtals** á stillingu birgðavirðisskýrslu, mun kerfið taka saman gildi fyrir valdar víddir sem eru raktar fjárhagslega.

### <a name="can-i-customize-the-power-bi-embedded-reports-for-costing"></a>Er hægt að sérsníða Power BI Embedded skýrslur fyrir kostnaðarútreikning?

Já, notendur sem hafa fullnægjandi öryggisheimildir geta uppfært vinnusvæði skýrsluhönnunar fyrir allar Power BI Embedded skýrslur í Supply Chain Management. Frekari upplýsingar eru í [Sérstilla innfelldar skýrslur í greiningarvinnusvæði](../../fin-ops-core/dev-itpro/analytics/customize-analytical-workspace.md).

### <a name="where-can-i-view-the-variance-analysis-statement"></a>Hvar get ég skoðað yfirlit fráviksgreiningar?

Þú getur fengið aðgang að greiningarskýrslu frávika með því að fara í **Kostnaðarstjórnun \> Fyrirspurnir og skýrslur \> Birgðabókhald – greiningarskýrsla** eða **Kostnaðarstjórnun \> Fyrirspurnir og skýrslur \> Framleiðslubókhald – Greiningarskýrslur**. Báðir valkostirnir opna sömu skýrslu og skýrslan hefur sömu hegðun.

## <a name="item-prices-and-default-costs"></a>Vöruverð og sjálfgefinn kostnaður

### <a name="can-i-maintain-the-cost-for-each-product-variant"></a>Get ég viðhaldið kostnaðinum fyrir hvert vöruafbrigði?

Já. Þú getur virkjað valkostinn **Nota kostnaðarverð eftir afbrigði** á flýtiflipanum **Stjórna kostnaði** á síðunni **Útgefin vara** til að virkja verðlagningu með afurðarafbrigði. (Þessi valkostur er aðeins í boði fyrir afurðarsniðmát). Á síðunni **Vöruverðe** (sem þú getur opnað annað hvort á síðunni **Kostnaðarútgáfa** eða síðunni **Losuð vara**) er síðan hægt að velja **Víddabirting** til að skilgreina hvort sýna eigi víddina **Stillingar**, **Stærð**, **Lit** eða **Stíl**. Til að vista uppsetningu og nota valdar víddir í hvert sinn sem þú opnar síðuna, virkjaðu valkostinn **Vista uppsetningu** og veldu síðan **Í lagi**. Þú getur aðeins slegið inn víddir fyrir vörur þar sem stærðirnar eru virkar í afurðavíddarhópnum.

### <a name="can-i-maintain-the-cost-for-each-warehouse"></a>Get ég viðhaldið kostnaðinum fyrir hvert vöruhús?

Nei, þú getur ekki unnið með vöruverðinu eftir vöruhúsum. Hins vegar er hægt að vinna með viðskiptasamningum um kaupverð eða söluverð eftir vöruhúsum. Veldu fyrst valkostinn **Fyrir innkaupverð** eða **Fyrir söluverð** á síðunni **Geymsluvíddarflokkur**. Síðan, þegar þú býrð til verðsamningsbók og opnar línurnar fyrir víddirnar, velurðu **Birgðir \> Sýna víddir** til að velja hvaða vídd á að vera sýnd á hnitanetinu. Til að vista uppsetningu og nota valdar víddir í hvert sinn sem þú opnar síðuna, virkjaðu valkostinn **Vista uppsetningu** og veldu síðan **Í lagi**. Þú getur aðeins slegið inn víddir fyrir vörur þar sem stærðirnar eru virkar í afurðavíddarhópnum.

### <a name="what-are-price-charges"></a>Hvað eru verðgjöld?

Verðgjöld eru leið til að bæta fastri upphæð við einingarverð vörunnar eða verðsamning. Þegar upphæð er færð inn í reitinn **Verðgjöld** er einnig hægt að færa inn gildi í reitinn **Gjaldamagn**. Verðgjöldin eru afskrifuð miðað við það gjaldamagn sem þú tilgreinir. Virkja valkostinn **Innifalið í einingarverðii** ef þú vilt setja verðgjöld í einingarverð vörunnar. Þessi valkostur er alltaf virkur fyrir staðalkostnað.

### <a name="how-should-i-configure-prices-for-items-that-are-procured-in-multiple-currencies"></a>Hvernig á ég að stilla verð fyrir vörur sem eru keyptar inn í mörgum gjaldmiðlum?

Ef þú slærð inn sjálfgefið verð í reitinn **Innkaupaverð** á síðunni **Losuð vara** er gert ráð fyrir því að það sé í bókhaldsgjaldmiðli fjárhagsins fyrir lögaðilann sem þú hefur opnað. Sömuleiðis ef þú slærð inn innkaupsverð í kostnaðarútgáfu þar sem reiturinn **Verðtegund** er stilltur á *Innkaup* er gert ráð fyrir að verð sé í bókhaldsgjaldmiðli lögaðila. Þegar þú stofnar innkaupapöntun fyrir lánardrottinn sem er með annan gjaldmiðil mun kerfið sjálfkrafa umreikna gjaldmiðlinum úr bókhaldsgjaldmiðlinum í gjaldmiðil færslu með því að nota gengið sem þú tilgreinir í reitnum **Gengisgerð bókhaldsgjaldmiðilsins** í fjárhag þínum.

Þegar stofnuð er verðsamningsbók er hægt að tilgreina gjaldmiðilinn sem er tilgreindur í verði hverrar línu. Þú getur útbúið verðsamninga fyrir marga gjaldmiðla, tiltekna lánardrottna og margar aðrar samsetningar af þáttum. Ef þú býrð til innkaupapöntun þar sem verðsamningur er til fyrir gjaldmiðilinn sem þú hefur valið notar kerfið verðsamninginn sem er með samsvarandi gjaldmiðil. Þegar þú bókar færslur eins og innhreyfingarskjöl eða reikninga verður upphæðinni umbreytt í bókhaldsgjaldmiðil fjárhags með því að nota gengi bókhaldsgjaldmiðils sem er tilgreint í fjárhagnum.

### <a name="how-should-i-configure-costs-for-items-that-are-procured-in-multiple-currencies"></a>Hvernig á ég að stilla kostnað fyrir vörur sem eru keyptar í mörgum gjaldmiðlum?

Ekki er hægt að stilla kostnað í fleiri en einum gjaldmiðli. Kostnaður sem þú tilgreinir fyrir vöruverð sjálfgefinn kostnað sem þú slærð inn í reitinn **Verð** á flýtiflipanum **Stjórna kostnaði** á síðunni **Losuð vara** er alltaf tilgreindur í bókhaldsgjaldmiðli fjárhags fyrir þann lögaðila sem þú hefur valið.

Ef fyrirtækið þitt notar hefðbundinn kostnaðarútreikning ættir þú að skilgreina áætlun til að skilgreina kostnaðinn þegar margir gjaldmiðlar eru til staðar. Þú ættir einnig að skilgreina ferli til að uppfæra kostnaðinn reglulega til að draga úr þeim frávikum sem eru bókuð.

### <a name="can-i-use-the-profit-setting-on-the-cost-group-page-to-calculate-sales-prices"></a>Get ég notað Hagnaðarstillinguna á síðunni Kostnaðarflokkur til að reikna út söluverð?

Já, þú getur notað stillinguna **Hagnaður** á síðunni **Kostnaðarflokkur** til að bæta við prósentuhlutfalli þegar söluverð er reiknað með kostnaðarútreikningi. Frekari upplýsingar eru í [Útreikningur uppskrifta](bom-calculations.md).

## <a name="marking"></a>Merking

### <a name="how-does-marking-affect-periodic-costing-models"></a>Hvernig hefur merking áhrif á regluleg kostnaðarlíkön?

Ef þú notar reglulegt kostnaðarlíkan eins og FIFO, LIFO eða vegið meðaltal, og þú hefur merkt innhreyfingarfærslu gegn úthreyfingarfærslu, er nálgunarlíkan vöru hunsað í birgðalokunarferlinu. Þess í stað mun kerfið nota raunkostnað við úthreyfingu fyrir kostnað við úthreyfingar.

### <a name="what-happens-during-the-inventory-close-when-i-use-marking"></a>Hvað gerist við birgðalokun þegar ég nota merkinguna?

Þegar þú merkir inn- og úthreyfingar, mun birgðalokun gera upp færslurnar sem eru merktar saman. Þegar merking er notuð til að stofna uppgjörið er reiturinn **Meginregla** á síðunni **Uppgjör** stilltur á *Merking*. Ef færsla eru merkt áður en þau eru uppfærð efnislega eða fjárhagslega mun úthreyfing nota kostnað merktu úthreyfingar í stað keyrslu á meðalkostnaði. Ef færslurnar eru merktar eftir fjárhagslega uppfærslu mun birgðalokunar- og aðlögunarferlið aðlaga kostnað úthreyfingar svo að hann samsvari kostnaði innhreyfingar.

### <a name="can-i-manually-mark-transactions-when-i-use-standard-costing-or-moving-average"></a>Get ég merkt handvirkt færslur þegar ég nota staðalkostnað eða hlaupandi meðaltal?

Nei, þú getur ekki merkt handvirkt inn- eða úthreyfingar þegar þú notar staðalkostnað eða hlaupandi meðaltal. Ef færslur (til dæmis beinar afhending eða pantanir innan samstæðu) eru merktar sjálfkrafa verður merkingafærslan óbreytt og virkar sem bundin frátekning. Hins vegar, þegar þú notar hefðbundinn kostnaðarútreikning eða hlaupandi meðaltal, hefur merking færslna engin áhrif á kostnað varanna.

### <a name="how-does-marking-affect-the-profit-and-loss-statement"></a>Hvernig hefur merking áhrif á rekstraryfirlit?

Þegar þú merkir við úthreyfingarfærslu gegn innhreyfingu mun kostnaður vegna hennar stemma við valda innhreyfingu. Þegar þú bókar úthreyfingu efnislega og fjárhagslega mun bókunin hafa áhrif **Kostnaður seldra vara móttekinna** og **Reikningsfærður kostnaður seldra vara** reikninga sem þú tilgreinir í bókunarreglu birgða. Ef færsla er merkt eftir efnislegri eða fjárhagslega uppfærslu, mun *Birgðalokunar- og aðlögunarferlið* búa til leiðréttingu sem er með samsvarandi afsláttarmiða sem breytir **Kostnaður seldra vara móttekinn** reiknings og hliðrar til reikningsins sem þú tilgreinir fyrir **Reikningsfærður kostnaður seldra vara** (birgða).

### <a name="how-does-marking-affect-master-planning"></a>Hvernig hefur merking áhrif á aðaláætlanagerð?

Flipinn **Stöðluð uppfærsla** á síðunni **Færibreytur aðaláætlanagerðar** inniheldur reit sem er nefndur **Uppfæra merkingu**. Sá kostur sem valinn er þar er notaður þegar valin er áætluð pöntun sem er búin til af aðaláætlanagerð. Eftirtaldir valkostir eru í boði:

- *Nei* – Kerfið framkvæmir enga merkingu.
- *Staðlað* – Kerfið merkir innhreyfingar gegn úthreyfingum samkvæmt þarfarakningu. Þarfapöntun er merkt gagnvart fullnaðarpöntun. Ef eitthvert magn er eftir í fullnaði er fullnaðarpöntunin ekki merkt.
- *Framlengt* – Kerfið merkir bæði þarfapantanir og fullnaðarpantanir, burtséð frá því hvort eitthvert magn er opið í fullnaðarpöntuninni.

## <a name="negative-inventory"></a><a name="negative-inventory"></a>Neikvæð birgðastaða

### <a name="when-should-i-allow-physical-negative-inventory"></a>Hvenær ætti ég að leyfa efnislega neikvæðar birgðir?

Almennt mælum við ekki með því að þú leyfir neikvæðar efnislegar birgðir þar sem það er ekki hægt að hafa minna en 0 (núll) af efnislegri vöru í vöruhúsi þínu. Hins vegar gætu viðskiptaferli sumra iðngreina og viðskiptaaðstæður takmarkað rekstur sem krefst þess að birgðirnar verði leyfðar að verða efnislega neikvæðar. Til dæmis gætu smásalar ekki viljað koma í veg fyrir sölu á vöru sem er komið með að afgreiðslukassa, jafnvel þegar kerfið gefur til kynna að engar vörur séu tiltækar. Framleiðendur ferla eru annað dæmi. Fyrir þessa framleiðendur, magn sem er notað getur farið yfir það sem mælt er með í formúlunni. Að öðrum kosti má áætla notkun í stað þess að fá nákvæma tölu, þannig að notkun fari yfir magnið á tilteknum staðsetningum, svo sem í geymi.

Þegar mögulegt er ættir þú að meta viðskiptaferlið þitt og reyna að bæta það til að tryggja að birgðir geti ekki verið neikvæðar. Ef þú verður að leyfa neikvæðar birgðir ættir þú að hafa skýrt viðskiptaferli til að leiðrétta neikvæðar birgðir því það getur haft neikvæð áhrif á kostnaðarútreikninga.

### <a name="when-should-i-allow-financial-negative-inventory"></a>Hvenær ætti ég að leyfa fjárhagslega neikvæðar birgðir?

Almennt er mælt með því að flestar fyrirtæki leyfi neikvæðar fjárhagslegar birgðir. (Í flestum tilvikum eru innkaupapöntunarreikningar ekki afgreiddir áður en hægt er að senda hlutina.) Þú ættir að virkja þennan valkost þegar þú ert með tiltekna viðskiptaferla sem krefjast þess að söluverðið endurspegli endanlegan kostnað innkaupapöntunar. Til dæmis gæti þessi krafa átt við í iðnaði þar sem er framleitt eftir pöntun eða á tilteknum svæðum þar sem lög kveða á um slíkt.

### <a name="what-happens-to-the-cost-of-my-issues-when-the-inventory-is-negative"></a>Hvað verður um kostnað úthreyfinga minna þegar birgðirnar eru neikvæðar?

Þegar birgðirnar fyrir vöruna þína eru neikvæðar, og þú gefur út fleiri vörur en þú hefur efnislega, mun kerfið nota sjálfgefna vöruverðið til að reikna út hlaupandi meðaltal ef þú notar reglulegt kostnaðarlíkan eins og FIFO, LIFO eða vegið meðaltal. Ef ekkert sjálfgefið verð er tilgreint fyrir hlutinn mun kerfið gefa út birgðirnar með gildi sem nemur 0 (núll). Þessi hegðun getur valdið því að seinni útreikningar á meðaltali eða hlaupandi meðaltali verði ónákvæmir í framtíðinni.

### <a name="can-i-prevent-items-from-being-picked-packed-or-sold-on-sales-orders-and-production-orders-if-there-isnt-enough-on-hand-inventory"></a>Get ég komið í veg fyrir að hlutir séu sóttir, pakkaðir eða seldir í sölupöntunum og framleiðslupöntunum ef lagerbirgðir eru ekki nægar?

Já. Við mælum með því að þú gerir valkostinn **Neikvæðar efnislegar** óvirkan fyrir vörulíkanahópinn til að koma í veg fyrir að vörur séu tíndar, pakkað eða seldir í sölupöntunum og framleiðslupöntunum.

### <a name="can-i-prevent-items-from-being-invoiced-on-a-sales-order-if-no-purchase-orders-have-been-invoiced-for-the-same-item"></a>Get ég komið í veg fyrir að vörur séu reikningsfærðir á sölupöntun ef engin innkaupapöntun hefur verið reikningsfærð fyrir sama hlut?

Já. Við mælum með því að þú gerir valkostinn **Fjárhagslega neikvæðar** óvirkan fyrir vörulíkanahópinn óvirkan til að koma í veg fyrir að vörur séu reikningsfærðar á sölupöntun ef engar innkaupapantanir hafa verið reikningsfærðar fyrir sömu vöru.

### <a name="how-does-negative-inventory-affect-financial-ratios-such-as-gross-profit-margin"></a>Hvernig hefur neikvæðar birgðir áhrif á fjárhagsleg hlutföll eins og brúttó hagnaðarhlutfall?

Þegar þú leyfir birgðum þínum að vera neikvæðar er hægt að vanmeta birgðavirði í efnahagsreikningi þínum og kostnað seldra vara í rekstraryfirliti þínum, sérstaklega ef ekkert sjálfgefið verð er stillt fyrir vörurnar.. Því er hægt að ofmeta fjárhagsskýrslugerð og hlutfall eins og vegið hagnaðarhlutfall, vegna þess að kostnaðurinn er rangur. Ef þú notar reglulegt kostnaðarlíkan eins og FIFO, LIFO eða vegið meðaltal er hægt að stilla gildi úthreyfinga þegar þú keyrir birgðalokun og aðlögunarferli eftir að magn neikvæðra birgða hefur verið leiðrétt. Hins vegar, ef þú notar hlaupandi meðaltal, er engin leið til að endurmeta einstakar færslur.

### <a name="how-should-i-correct-negative-inventory"></a>Hvernig á ég að lagfæra neikvæðar birgðir?

Mælt er með því að þú fylgist reglulega með og leiðréttir neikvæðar birgðir þegar kröfur fyrirtækisins eða viðskiptakröfur kveða á um að þú leyfir birgðum þínum að verða neikvæðar. Hægt er að leiðrétta birgðavirði með því að framkvæma lotutalningu, bóka leiðréttingu eða bóka hreyfingabók. Ef þú verður að færa inn óvæntan hagnað í birgðum á tilteknum fjárhagslykli ættir þú að nota hreyfingabók. Að öðrum kosti þegar þú notar ferli regluleg talningu eða leiðrétting á birgðaskrá, mun kerfið bóka leiðréttingu á birgðaskrá í lykilinn **Innhreyfing birgða** og hliðra í lyklum **Birgðaútgjöld, hagnaður** sem þú tilgreinir í birgðabókunarreglu.

### <a name="do-i-have-to-create-a-new-item-if-my-inventory-has-gone-negative-and-i-use-moving-average"></a>Þarf ég að stofna nýja vöru ef birgðirnar eru orðnar neikvæðar og ég nota hlaupandi meðaltal?

Nr. Ef fyrirtækið þitt leyfir birgðum þínum að verða efnislega neikvætt og þú ert að nota hlaupandi meðaltal sem birgðalíkanið þitt mun kerfið nota varakostnaðarröð sem er úthlutað á síðunni fyrir **Stjórnfæribreytur birgða og vöruhúss** til að ákvarða hvernig kostnaði verður úthlutað til úthreyfinga þinna. Almennt er mælt með því að þú forðist að leyfa birgðum þínum að verða efnislega neikvæðar. Frekari upplýsingar er í öðrum spurningum í kaflanum [Neikvæð birgðastaða](#negative-inventory) í þessari grein.

## <a name="not-stocked-products"></a>Afurðir sem ekki eru til á lager

### <a name="can-i-post-sales-order-picking-lists-for-not-stocked-products"></a>Get ég birt tiltektarlista sölupantana fyrir vörur sem ekki á lager?

Þegar þú útbýrð tiltektarlisti fyrir sölupöntun sem inniheldur vörur sem eru í vörulíkanahópi sem er ekki á lager sérðu engar línur fyrir þessa hluti sem eru ekki á lager. Ekki er hægt að nota farsímaforrit vöruhúsakerfis til vinnslu á vörum sem eru ekki á lager.

Þegar þú útbýrð fylgiseðil fyrir sölupöntun sem inniheldur vörur sem eru í vörulíkanasamstæðu sem er ekki á lager, stillir þú reitinn **Magn** fyrir *Tiltektarmagn og vörur sem ekki á lager* til að innifela vörurnar sem eru ekki á lager í stofnun skjalsins. Ef valið er *Allt*, eru aðeins birgðir á lager innifaldar í fylgiseðlinum.

### <a name="should-i-use-a-not-stocked-product-or-a-category-sales-category-or-procurement-category"></a>Ætti ég að nota vöru sem er ekki á lager eða flokk (söluflokk eða innkaupaflokk)?

Valið á milli vöru sem er ekki á lager og flokks fer eftir sértækum viðskiptakröfum þínum. Vörur sem eru ekki á lager bjóða almennt upp á meiri stjórn á sjálfgefnum gildum, svo sem magni og verði á innkaupapantanir og sölupantanir. Þess vegna eru vörur sem ekki eru á lager ákjósanlegri við aðstæður þar sem sama varan eða þjónustan er keypt eða seld oftar en einu sinni. Flokkar eru gagnlegir við aðstæður þar sem verð, vörur, lýsingar og svo framvegis eru í ósamræmi frá færslu til færslu. Einnig er hægt að nota flokka á hvaða vöru sem er til að flokka vörutegundina sem verið er að selja eða kaupa.

## <a name="service-items"></a>Þjónustuvara

### <a name="what-is-the-difference-between-a-service-item-and-a-not-stocked-product"></a>Hver er munurinn á þjónustuvöru og vöru sem ekki er á lager?

Þjónustuvara er gerð vöru. Þegar nýlosuð vara er stofnuð er hægt að stilla reitinn fyrir **Vörutegund** á annaðhvort *Vara* eða *Þjónusta*. *Vara* er yfirleitt valinn til að gefa til kynna að varan sé efnisleg, en *Þjónusta* er yfirleitt valin til að gefa til kynna að varan sé óefnislegur.

Allar losaðar vörur, sama hvort um er að ræða vöru eða þjónustu, geta verið á lager eða ekki á lager. Stillingin á lager eða ekki á lager er stjórnað af vörulíkanahópnum sem þú velur fyrir losaða vöru. Þegar þú velur vöruflokk sem er ekki á lager býr kerfið ekki til birgðafærslur fyrir tengda sölupöntun eða innkaupapöntun, til dæmis.

### <a name="can-i-include-not-stocked-items-in-a-bom"></a>Get ég haft með vörur sem eru ekki á lager í uppskrift?

Nei, þú getur ekki tekið með losaða vöru út og er tengd við vörulíkansflokk þar sem valkosturinn **Á lager** er óvirkur í uppskrift eða formúlu. Það skiptir ekki máli hvort reiturinn **Vörutegund** er stilltur á *Vöru* eða *Þjónusta*. Aðeins hlutir sem eru á lager geta verið með í uppskrift eða formúlulínum.

## <a name="costing-modelspecific-questions"></a>Spurningar um líkön kostnaðarútreiknings

### <a name="which-costing-model-should-i-use"></a>Hvaða kostnaðarlíkan ætti ég að nota?

Kostnaðarlíkönin sem þú ættir að velja fara eftir viðskiptakröfum þínum. Áður en þú velur kostnaðarlíkan til að nota í Supply Chain Management skaltu staðfesta að líkanið sé leyft samkvæmt gildandi reglum á hverjum stað. Við mælum með því að þú staðfestir valið hjá löggiltum endurskoðanda á þínu svæði.

### <a name="can-i-use-more-than-one-costing-model-in-my-organization"></a>Get ég notað fleiri en eitt kostnaðarlíkan í fyrirtæki mínu?

Já. Engin takmörk eru fyrir því hversu marga vörulíkanaflokkur eða kostnaðarlíkön er hægt að velja í Supply Chain Management.

### <a name="can-i-use-more-than-one-costing-model-for-each-item"></a>Get ég notað fleiri en eitt kostnaðarlíkan fyrir hverja vöru?

Nr. Aðeins er hægt að velja eitt kostnaðarlíkan fyrir hverja losaða vöru. Þessari hegðun er stjórnað af vörulíkanaflokknum. Ef nota þarf fleiri en eitt kostnaðarlíkan til að greina frá birgðavirði skal nota viðbótina Global Inventory Accounting.

### <a name="when-i-use-manufacturing-execution-which-costing-methodology-should-i-use"></a>Þegar ég nota framkvæmd framleiðslu, hvaða aðferð kostnaðarútreiknings ætti ég að nota?

Kostnaðarlíkönin sem þú ættir að velja fara eftir viðskiptakröfum þínum. Það er enginn sérstakur kostur eða ókostur við að nota hvaða kostnaðarlíkan sem er þegar fyrirtækið þitt notar einnig framkvæmd framleiðslu.

### <a name="when-is-fefo-used"></a>Hvenær er FEFO notað?

Fyrst útrunnið fyrst út (FEFO) er ekki aðferð kostnaðarútreiknings. Þess í stað er þetta frátekningartækni sem er oft notuð hjá framleiðslufyrirtækjum. Hægt er að virkja FEFO frátekningar fyrir vörulíkanaflokk með því að virkja valkostinn **Dagsetningarstýrt samkvæmt FEFO** og velja síðan gildi í reitknum **Tiltektarskilyrði**.

### <a name="are-there-performance-benefits-to-selecting-one-costing-model-over-another"></a>Er einhver ávinningur fyrir afköst að velja eitt kostnaðarlíkan fram yfir annað?

Almennt hefur kostnaðarlíkanið sem þú velur fyrir vöru lítil áhrif á heildarafköst kerfisins. Hins vegar gæti birgðakostnaðarlíkanið sem þú velur haft áhrif á tímann sem er áskilinn til að keyra birgðalokun eða endurútreikningsferlið. Ef þú notar til dæmis staðalkostnað eða hlaupandi meðaltal hefur birgðalokunarferlið lítil áhrif á kerfið vegna þess að það uppfærir ekki hverja birgðafærslu og býr til jöfnun. Hins vegar getur reglulegt kostnaðarlíkan eins og FIFO, LIFO eða vegið meðaltal aukið þann tíma sem þarf til að ljúka birgðalokununarferlinu. Nánar tiltekið getur lokunarferlið verið lengra þegar þú slærð inn háa tölu í reitinn **Hámarksfjöldi ítrekana sem leyfður er á vöru** eða lága tölu í reitinn **Lágmarksupphæð sem leyfður er** í ferlinu *Birgðalokun*.

### <a name="when-should-i-use-the-fixed-receipt-price-option"></a>Hvenær ætti ég að nota valkostinn Fast kostnaðarverð?

Þegar þú velur gátreitinn **Fast verð innhreyfingar** á síðunni **Vörulíkanaflokkur** fyrir vöru mun kerfið nota verð innhreyfingar sem hefðbundinn kostnað fyrir innhreyfing birgða. Ef mismunur er á innkaupaverði og sjálfgefnu kostnaðarverði vöru verður mismunurinn birtur á lyklinum **Hagnaður fasts innhreyfingarverð** eða **Tap á föstu verði innhreyfingar** og vegið upp á móti við lykilinn **Mótbókun fasts innhreyfingarverðs**. (Allir þessir reikningar eru tilgreindir á síðunni **Bókun**).

Þú ættir að velja gátreitinn **Fast verð innhreyfingar** þegar þú notar reglulegt kostnaðarlíkan eins og FIFO, LIFO eða vegið meðaltal og þú gerir kröfu um að frávik innkaupaverðs sé rakið í fjárhagnum ef verð innhreyfingar er frábrugðið sjálfgefnum kostnaði vöru.

### <a name="moving-average"></a>Hlaupandi meðaltal

### <a name="is-moving-average-the-same-as-a-floating-average"></a>Er hlaupandi meðaltal það sama og fljótandi meðaltal?

Hugtökin hreyfanlegt meðaltal, fljótandi meðaltal og hlaupandi meðaltal eru oft notuð samheiti. Af þessum hugtökum, hlaupandi meðaltal er eina opinbera kostnaðarlíkanið sem er í boði í Supply Chain Management. Þó að hlaupandi meðaltal sé ekki opinbert kostnaðarlíkan er það tæknin sem er notuð þegar notað er reglulegt kostnaðarlíkan eins og FIFO, LIFO eða vegið meðaltal. Hugtakið fljótandi meðaltal er ekki notað í Supply Chain Management og gæti haft mismunandi merkingar í öðrum kerfum.

### <a name="how-can-i-accommodate-the-difference-between-the-product-receipt-price-and-invoice-price-when-i-use-moving-average"></a>Hvernig get ég komið til móts við mismuninn á milli verð innhreyfingarskjals vöru og reikningsverðs þegar ég nota hlaupandi meðaltal?

Þegar þú notar hlaupandi meðaltal er raunkostnaður (kvittunarverð) notaður til að reikna hreyfanlegt meðaltal fyrir allar úthreyfingarfærslur. Ef munur er á efnislegum kostnaði (kostnaðarverði) og fjármagnskostnaði (reikningsverði) mun kerfið sjálfkrafa bóka mismuninn á aðallyklinum sem tilgreindur er fyrir bókunarregluna **Verðmunur á hlaupandi meðaltali** á flipanum **Birgðir** á síðunni **Birgðabókunarregla**.

### <a name="where-is-the-price-difference-for-moving-average-presented-in-the-general-ledger"></a>Hvar er verðmunurinn á hlaupandi meðaltali sem kemur fram í fjárhagnum?

Þegar verðmunur er á því að bóka efnislega uppfærslu og fjárhagslega uppfærslu fyrir innhreyfingu er munurinn settur á aðallykil sem er tilgreindur fyrir bókunargerðina **Verðmunur á hlaupandi meðaltali** á flipanum **Birgðir** á síðunni **Birgðarbókunarregla**. Frekari upplýsingar eru í [Hlaupandi meðaltal](moving-average.md).

### <a name="when-i-use-moving-average-what-happens-if-there-is-an-issue-before-the-receipt"></a>Þegar ég nota hlaupandi meðaltal, hvað gerist ef úthreyfing verður á undan innhreyfingu?

Venjulega gæti úthreyfing orðið áður en innhreyfing er móttekin, annaðhvort vegna þess að þú leyfir neikvæðar efnislegar birgðir fyrir vörulíkanið eða vegna þess að úthreyfingin er bakfært. Frekari upplýsingar eru í kaflanum [Neikvæð birgðastaða](#negative-inventory) í þessari grein.

Ef þú ert að bakfæra færslur mælum við með því að þú íhugir vandlega viðskiptaferli þitt og rekstur til að komast að því hvort hægt sé að komast hjá slíku. Ef þú tekur bakfærir af færslu fyrir vöru sem notar hlaupandi meðaltal mun kerfið úthluta núverandi hlaupandi meðaltali í færsluna. Síðari vandamál eru ekki leiðrétt. Frekari upplýsingar um hlaupandi meðaltal með bakfærðum færslum er að finna á [Hlaupandi meðaltal](moving-average.md).

### <a name="standard-costing"></a>Staðalkostnaður

### <a name="what-is-the-difference-between-standard-costing-and-fixed-receipt-price"></a>Hver er munurinn á staðalkostnaði og föstu verði innhreyfingar?

Staðalkostnaður krefst þess að þú skilgreinir vöruverð og virkjir kostnaðinn í kostnaðarútgáfu. Sá kostnaður er notaður í allar inn- og úthreyfingar. Frávik innhreyfinga í birgðir eru skráð í fjárhag því að nota staðlaða kostnaðarfrávikslykla sem þú tilgreinir á flipanum fyrir **Staðalkostnaður** á flipanum **Birgðarbókunarregla**.

Þegar þú notar fast verð innhreyfingar, er aðeins kostnaður innhreyfinga fastur og kerfið notar þann kostnað sem þú tilgreinir á flýtiflipanum **Stjórna kostnaði** á síðunni **Losuð vara**. Mismunur á sjálfgefnum kostnaði og verði innkaupapöntunar veldur því að frávik innkaupaverðs er bókað á rekstrarreikningi fasta verðs innhreyfingar. Úthreyfingar nota ekki fast verð kvittunar. Í staðinn verða úthreyfingar metin að hlaupandi meðaltali við bókun (nema þú notir merkingu), og þau verða endurmetin að nálgunarlíkaninu sem þú velur þegar þú keyrir birgðalokun.

### <a name="can-i-use-fefo-reservations-with-standard-costing"></a>Get ég notað FEFO bókanir með staðalkostnaði?

Já, þú getur notað FEFO bókanir í vörulíkanaflokki þegar þú velur staðalkostnað. FEFO bókanir stjórna frátekningarökum sem eru notuð fyrir efnislega meðhöndlun á vörum, en hefðbundin kostnaðarstýring stýrir efnislegum og fjárhagslegum kostnaði vöru.

### <a name="can-i-upload-pending-prices"></a>Get ég sett inn verð í bið?

Já, þú getur notað Excel viðbótina eða Yfirlit gagnastjórnunarramma til að hlaða upp biðverði. Mælt er með því að nota eftirfarandi einingar:

- Biðvöruverð (V2)
- Kostnaðarflokkur leiðar í biðstöðu fyrir kostnaðareiningar
- Reikningsþættir kostnaðarskjalshnútar (V2)

### <a name="how-often-can-i-update-the-standard-cost-for-an-item"></a>Hversu oft get ég uppfært staðalkostnað fyrir vöru?

Engin takmörk eru á því hversu oft er hægt að virkja nýjan staðalkostnað. Ef þú virkjar nýjan kostnað fyrir vöru sama dag og síðasti kostnaður var virkjaður mun kerfið nota nýjasta virkjaða kostnaðinn við nýjar færslur eða uppfærslur (svo sem uppfærslur á núverandi færslum).

### <a name="can-i-deactivate-or-delete-an-activated-cost"></a>Get ég afvirkjað eða eytt virkum kostnaði?

Nei, þú getur ekki afvirkjað eða eytt virkum kostnaði. Ef kostnaður er ranglega gerður virkur getur þú virkjað nýjan kostnað með rétta kostnaðinum.

### <a name="are-calculation-groups-used-with-standard-costing"></a>Eru notaðir reikniflokkar með staðalkostnaði?

Hægt er að nota reikniflokka með hvaða vöru sem er, án tillits til þess hvaða vörulíkanaflokk þú velur. Reikniflokkar eru notaðir við samantekt eða kostnaðarútreikning til að ákvarða stillingarnar sem á að nota fyrir þá vörur sem þú ert að keyra útreikninginn fyrir. Frekari upplýsingar um reikniflokka eru í [Reikniflokkar uppskrifta](bom-calculation-groups.md).

### <a name="when-should-i-use-a-planned-costing-version"></a>Hvenær ætti ég að nota áætlaða kostnaðarútgáfu?

Kostnaðarútgáfur geta haft ákveðna gerð af *Staðalkostnaður* eða *Áætluðum kostnaði*. Gerðin *Staðalkostnaður* er notuð fyrir þann kostnað sem er virkur í kerfinu og verður bókaður í færslum. Gerðin *Áætlaður kostnaður* er notuð til að keyra hermun á kostnaði og hefur ekki áhrif á færslukostnað.

### <a name="can-the-total-cost-from-one-entity-be-transferred-to-another-entity-as-the-selling-cost"></a>Er hægt að færa heildarkostnað frá einni einingu til annars sem sölukostnað?

Það er engin sjálfvirk leið til að afrita kostnað frá einu fyrirtæki til annars. Þar að auki er engin sjálfvirk leið til að afrita kostnað frá kaupverði til söluverðs. Ef fyrirtækið verður að ljúka einu af þessum verkum skaltu íhuga hvort þú getir notað Yfirlit gagnastjórnunarramma til að flytja gögnin út úr kostnaðarútgáfunni og hlaða þeim upp í annað fyrirtæki, annaðhvort sem söluverði í kostnaðarútgáfunni eða sem verðsamningi. Handvirk stjórnun skránna gæti verið nauðsynleg.

### <a name="what-is-the-best-way-to-copy-planned-costs-to-a-standard-costing-version"></a>Hver er besta leiðin til að afrita áætlaðan kostnað í staðlaða kostnaðarútgáfu?

Hægt er að nota hnappinn **Afrita** á síðunni **Kostnaðarútgáfur** til að afrita vöruverð, verð kostnaðartegunda eða óbeinan kostnað frá einni kostnaðarútgáfu til annarrar.
