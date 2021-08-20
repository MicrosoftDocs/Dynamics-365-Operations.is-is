---
title: Setja upp aðaláætlanagerð
description: Þetta efni lýsir ýmsum mikilvægum áætlunum og breytum sem eru notaðar til að setja upp aðaláætlanagerð.
author: t-benebo
ms.date: 07/01/2019
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
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: c06e8cc3ba37baae803bfe8d79b8e111f9e53ac3576ed8004f592cff70a358ff
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758569"
---
# <a name="set-up-master-planning"></a>Setja upp aðaláætlanagerð

[!include [banner](../includes/banner.md)]

Þetta efni lýsir ýmsum mikilvægum áætlunum og breytum sem eru notaðar til að setja upp aðaláætlanagerð. Hún felur í sér yfirlit yfir þær gerðir áætlana sem eru notaðar af aðaláætlanagerð og útskýrir hvaða áætlunarstefnu ætti að nota, allt eftir þörfum fyrirtækisins. Hún lýsir einnig helstu færibreytum sem hafa áhrif á áætlunina og útskýrir hvernig þessar færibreytur hafa áhrif á áætlaðar pantanir sem eru leiðbeinandi.

## <a name="types-of-master-plans"></a>Tegundir aðaláætlana

Aðaláætlanagerð hefur tvær gerðir áætlana: fastar og kvikar. Hver gerð er sett upp fyrir aðra notkun. Til að ná bestum árangri mælum við með að þú notir viðeigandi áætlun fyrir aðstæður þínar.

### <a name="static-plan"></a>Föst áætlun

Föst áætlun helst óbreytt, óháð breytingum á framboði og eftirspurn, þar til að næsta aðaláætlanagerð er keyrð.

Fasta áætlunin er notuð til að samþykkja og staðfesta pantanir sem eru leiðbeinandi. Hún er aðgerðaáætlun sem ýmsir starfsmenn fyrirtækisins (eins og kaupendur eða framleiðslustjórar) geta notað til grundvallar ákvörðunum sínum og til að framkvæma dagleg verk og verkþætti.

Föst áætlunin styður einnig endurnýjun. Algerlega ný bestuð áætlun er reiknuð í hvert skipti sem aðaláætlanagerð er keyrð og núverandi pöntunum sem ekki hafa verið samþykktar er eytt.

### <a name="dynamic-plan"></a>Kvik áætlun

Kvik áætlun hefst venjulega sem afrit af föstu áætluninni, en hana má uppfæra í hvert skipti sem aðalgögnin breytast. Til dæmis er ný sölupöntun stofnuð ef gögnin breytast.

Kvik áætlun er notuð fyrir tilfallandi áætlanagerð. Hún gerir fyrirtækinu kleift að fylgjast með breytingum í pöntunum og vöruframboði án þess að hafa áhrif á föstu áætlunina sem aðrir starfsmenn nota í sínu verkferli. Hún er sérstaklega notuð fyrir afhendingargetu (CTP). Kvik áætlun er sjálfgefin áætlun þegar nettó þarfir eru opnaðar af pöntunarsíðum (eins og sölupöntun, innkaupapöntun eða framleiðslupöntunarsíður).

Kvik áætlun notar nettó breytingu. Þess vegna hjálpar hún við að tryggja hraðari keyrslutíma.

## <a name="strategies-for-using-master-plans"></a>Aðferðir fyrir notkun aðaláætlana

Hægt er að nota annaðhvort eina áætlun eða tvær áætlanir í aðaláætlanagerð. Stefnan sem þú notar er háð þörfum fyrirtækisins.

### <a name="one-plan-strategy"></a>Einnar áætlunar stefna

Fyrir einnar áætlunar stefnuna notarðu sömu aðaláætlun fyrir föstu áætlunina og kviku áætlunina. Þessi stefna er notuð fyrir aðstæður Gera á lager, þar sem þú þarft yfirleitt ekki að líkja eftir áætlun sem uppfyllir pöntun.

Einnar áætlunar stefnan er yfirleitt notuð í smásölu- og dreifingariðnaði, eða þar sem afhendingardags. sölu eru staðfestar á grundvelli þjónustustigssamninga (SLAs) eða afhendingartíma. Fyrir áætlunina er hægt að nota stjórnun afhendingadagsetningar án CTP.

Ef þú verður að gera hermingu er hægt að keyra áætlunina aftur fyrir þau atriði sem þarfnast hermingarinnar. Áætlaðar pantanir sem panta hermingarferli eru yfirleitt staðfestar.

### <a name="two-plan-strategy"></a>Tveggja áætlana stefna

Fyrir tveggja áætlana stefnuna þú fasta áætlun og aðra kvika áætlun. Tveggja áætlana stefnan er yfirleitt notuð fyrir aðstæður sem snúast um að skilgreina fyrir pöntun og framleiða eftir pöntun, þar sem þú verður að gera hermingu á sölutilboði og reikna út nákvæmar afhendingardagsetningar fyrir sölupantanir, en útreikningarnir mega ekki að hafa áhrif á daglegar aðgerðir. Þessar heringar eru alltaf gerðar í kviku áætluninni. Tveggja áætlana stenan er gagnleg í bílaiðnaði og framleiðslu á upprunalegum búnaði (OEM), til dæmis.

Fyrir tveggja áætlana stefnuna er hægt að nota CTP stjórnun afhendingadagsetningar. Þegar CTP er notað, kveikir það sjálfvirkt á keyrslunni í kviku áætluninni.

### <a name="setting-up-the-plans"></a>Uppsetning áætlana

Hægt er að stofna áætlanir á síðunni **Aðaláætlanir** (**Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Aðaláætlanir**).

Hægt er að tilgreina hvaða áætlanir verða notaðar fyrir föstu áætlunina og kviku áætlunina með því að stilla reitina **Gildandi föst aðaláætlun** og **Gildandi kvik aðaláætlun** á síðunni **Færibreytur áætlanagerðar** (**Aðaláætlanagerð \> Uppsetning \> Færibreytur áætlanagerðar**). Til að nota einnar áætlunar stefnu skaltu velja sömu áætlun í reitunum **Gildandi föst aðaláætlun** og **Gildandi kvik aðaláætlun**.

## <a name="types-of-planning-methods"></a>Gerðir áætlunarsaðferða

Hægt er að nota þrjár útreikningsaðferðir til að keyra aðaláætlanagerð: endurnýjun og nettóbreytingu. Hver aðferð framleiðir mismunandi áætlun þegar hún er keyrð.

Þú tilgreinir áætlunaraðferðina í valmyndinni **Keyrsla aðaláætlanagerðar**. Til að opna þessa valmynd skaltu fara í **Aðaláætlanagerð \> Aðaláætlanagerð \> Keyra \> Aðaláætlanagerð** eða velja **Keyra** á vinnusvæðinu **Aðaláætlanagerð**.

### <a name="regeneration"></a>Endurgerð

Endurnýjun áætlunaraðferðar eyðir gildandi áætluðum pöntunum nema þær séu staðfestar. Hún myndar nýjar áætlaðar pantanir, byggt á öllum þörfum. Endurnýjun er eina áætlanagerðin sem er í boði fyrir fastar áætlanir.

- Breytingar á framboði eru teknar til greina. Þessar breytingar eru meðal annars breytingar á spánni.
- Þessi aðferð virðir þekjukóðann **Tímabil**.
- Þessi aðferð styður virknina vörustaðgengill (PI).

### <a name="net-change"></a>Nettó breyting

Nettóbreytingaráætlanagerðin myndar áætlaðar pantanir til að ná til þeirra þarfa sem hafa verið búnar til eða breytt frá síðustu keyrslu aðaláætlanagerðar. Ekki er tekið tillit til breytinga á framboði þegar þessi aðferð er keyrð. Kerfið lítur ekki á nein ný aðföng og áður stofnuðum áætluðum pöntunum er ekki eytt ef þeirra er ekki lengur þörf. Nettóbreyting áætlanagerðar keyrir hraðar en endurnýjunaraðferðin. Hún er aðeins í boði fyrir kvikar áætlanir.

- Aðgerðadagsetningar og framvirkar dagsetningar eru uppfærðar fyrir allar þarfir.
- Þessi aðferð virðir ekki þekjukóðann **Tímabil**.
- Þessi aðferð uppfyllir ekki spána, jafnvel þótt hún sé valin á áætluninni.
- Þessi aðferð styður ekki virknina vörustaðgengill (PI).

### <a name="net-change-minimized"></a>Nettó breyting lágmörkuð

Lágmörkuð nettóbreytingaráætlanagerð myndar áætlaðar pantanir sem ná aðeins yfir þær þarfir sem hafa verið stofnaðar eða breytt frá síðustu áætlunarkeyrslu aðaláætlanagerðar. Fyrir þessa aðferð, ólíkt netbreytingaraðferðinni, eru aðgerðadagsetningar og framvirkar dags. aðeins uppfærðar fyrir nýjar eða breyttar þarfir. Þessi skipulagsaðferð er aðeins tiltæk fyrir kvikar áætlanir.

## <a name="types-of-scheduling-methods"></a>Gerðir röðunaraðferða

Fyrir hverja áætlun þarftu fyrir hverja áætlun að velja þá röðunaraðferð sem er notuð fyrir framleiðslupantanir á flýtiflipanum **Almennt** á síðunni **Aðaláætlanir** (**Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Aðaláætlanir**). Hægt er að raða framleiðslu á stigi aðgerðina og stigi vinnslu.

### <a name="operations-scheduling"></a>Aðgerðaröðun

Hægt er að nota aðgerðaröðun til að fá almennt mat á framleiðsluferli yfir tíma. Aðgerðaröðun brýtur ekki aðgerðir fyrir framleiðsluleið niður í vinnslur. Nánari upplýsingar um rekstraráætlun er að finna í [Aðerðaröðun](/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling).

### <a name="job-scheduling"></a>Vinnsluröðun

Vinnsluröðun er nákvæmari röðunaraðferð, þar sem hverri aðgerð er skipt í niður í einstaka verkefni eða störf. Vinnsluröðun inniheldur upplýsingar um getu. Hún er yfirleitt notuð til að raða einstaka vinnslu í vinnusal og fyrir tímamörk sem eru undireins eða til stutts tíma. Nánari upplýsingar um vinnsluröðun er að finna í [Vinnsluröðun](/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).

## <a name="time-fences-in-days"></a>Tímamörk í dögum

Fyrir hverja áætlun er hægt að velja hversu langt í framtíðina þarf að reikna út hinar ýmsu þarfir og önnur atriði með aðaláætlunargerðinni. Tímabilið er þekkt sem *tímamörk*. Til að ná sem bestum árangri í aðaláætlanagerð mælum við með að þú stillir hin ýmsu tímamörk til að uppfylla þarfir fyrirtækisins. Fyrir hverja áætlun er hægt að finna tímamörk á flýtiflipanum **Tímamörk í dögum** á síðunni **Aðaláætlanir** (**Aðaláætlanagerð \> Uppsetning \> Áætlun \> Aðaláætlanir**).

> [!NOTE]
> Tímamörkin gefa til kynna hversu langt fram í framtíðina ýmsar þarfir og önnur atriði eru reiknuð með aðaláætlunargerðinni. Tímamörkin sem voru valin á þessari síðu munu hnekkja tímamörkunum sem eru skilgreind í tryggingarhópnum. Þetta þýðir að ef valkostur tímamarka er stilltur á já og dagar eru skilgreindir, munu tímamörkin vera hnekkt sem skilgreind eru í þekjuflokknum. Þegar stillt er á Nei verða tímamörkin skilgreind í tryggingarhópnum. Að lokum, ef þú vilt ekki eða þarft að nota valkost (til dæmis, þú vilt ekki nota aðgerðaskeyti) skaltu stilla hann á **Já** og stilla síðan tímamörkin á **0** (núll) daga.

### <a name="coverage"></a>Þekja

Þekjutímamörk standa fyrir röðunartímabilið, eða hversu langt þarf að fylgja eftirspurninni. Með öðrum orðum gefur það til kynna áætlanagerð sjóndeildarhrings.

Með því að stilla valkostinn **Þekja** á **Já** geturðu hnekkt þekjutímamörkunum sem eru skilgreind fyrir vöruna á meðan röðun stendur. Í þessu tilfelli skal færa inn fjölda þeirra daga þegar útreikningur röðunar á að ná yfir þarfir. Þekjutímamörk eru framreiknuð frá gildandi dagsetningu. Alltaf er unnið úr þörfum sem koma upp fyrir gildandi dagsetningu.

> [!NOTE]
> Til að ná sem bestum árangri í aðaláætlanagerð mælum við með að þú stillir hin þekjutímamörk á áætlanagerð sjóndeildarhrings.

### <a name="freeze"></a>Frysta

Frystistímamörk standa fyrir tímabilið þegar fyrirliggjandi áætluðum pöntunum er ekki breytt þegar ný aðalröðun er keyrð. Áætlaðar pantanir eru frystar og engar nýjar áætlaðar pantanir verða ráðlagðar.

Með því að stilla valkostinn **Frysta** á **Já** geturðu hnekkt frystitímamörkunum sem eru skilgreind fyrir vöruna á meðan röðun stendur. Í þessu tilfelli skal færa inn fjölda daga sem frysta á verkþáttaáætlun. Mundu að á þessu tímabili eru engar nýjar áætlaðar pantanir eru stofnaðar og ekki er hægt að breyta áætluðum pöntunum sem eru til nú þegar.

### <a name="firming"></a>Staðfesting

Staðfestingartímamörkin gefa til kynna tímarammann þar sem áætluðum pöntunum er sjálfvirkt breytt í framleiðslu- og innkaupapantanir. Þetta ferli er einnig þekkt sem *sjálfvirk staðfesting á áætluðum pöntunum*.

Með því að stilla valkostinn **Staðfesting** á **Já** geturðu hnekkt staðfestingartímamörkunum sem eru skilgreind fyrir vöruna á meðan röðun stendur. Í þessu tilfelli skal færa inn fjölda þeirra daga þegar innkaupa- og framleiðslutillögur eru sjálfkrafa staðfestar. Staðfestingartímamörkin eru framreiknuð frá dagsetningu aðalröðunar. Sjálfvirk staðfesting áætlaðrar innkaupapöntunar getur aðeins farið fram ef varan er tengd lánardrottni.

### <a name="forecast-plan"></a>Spáráætlun

Tímamörk spáráætlunar gefa til kynna hversu langt í framtíðina aðaláætlanagerð stofnar áætlaðar pantanir fyrir hluti sem eru með spáða eftirspurn.

Með því að stilla valkostinn **Spáráætlun** á **Já** geturðu hnekkt tímamörkum spáráætlunar sem eru skilgreind fyrir vöruna á meðan röðun stendur. Í þessu tilfelli skal færa inn fjölda daga þegar söluspá úr spááætlun á að vera tekin með í aðaláætlanagerð.

### <a name="capacity"></a>Afkastaveita

Tímamörk getu gefa til kynna hversu langt í framtíðinni kerfið telur hámarksgetu tilfanga þegar það raðar pöntunum. Með öðrum orðum, áætlunin raðar framleiðslupöntunum með því að nota framleiðsluleiðina fyrir vörurnar, og hún tekur tillit til tilfanga framleiðsluleiðarinnar og hámarksafkastagetu hvers tilfangs.

Með því að stilla valkostinn **Geta** á **Já** geturðu hnekkt getutímamörkunum sem eru skilgreind fyrir vöruna á meðan röðun stendur. Í þessu tilviku slærðu inn þann dagafjölda sem afkastageta ætti að vera áætluð fyrir framleiðslutillögur. Röðun notar virka framleiðsluleið vörunnar og afturraðar frá þarfadagsetningu. Ef þarfadagsetningin fyrir áætlaða framleiðslupöntun fellur utan afkastagetutímamarkanna er biðtíminn ákveðinn út frá afhendingartíma vörunnar. Getutímamörk eru framreiknuð frá gildandi dagsetningu.

### <a name="action-message"></a>Aðgerðaboð

Aðgerðaboð leggja til breytingar sem hægt er að gera á núverandi birgðapöntunum til að hjálpa til við að fínstilla birgðaáætlunina. Til dæmis gætu þau mælt með því að þú flýtir eða frestir pöntunum eða að þú hækkir eða lækkir pöntunarmagnið.

Með því að stilla valkostinn **Aðgerðaboð** á **Já** geturðu hnekkt tímamörkum aðgerðaboða sem eru skilgreind fyrir vöruna á meðan röðun stendur. Í þessu tilfelli skal færa inn fjölda þeirra daga þegar aðalröðun ætti að mynda aðgerðaboð fyrir þarfir. Tímamörk aðgerðaboða eru framreiknuð frá gildandi dagsetningu.

Nánari upplýsingar um aðgerðaboð eru í [Aðgerðaboð](/dynamics365/unified-operations/supply-chain/master-planning/action-messages).

> [!NOTE]
> Útreikningur á aðgerðaboðum veldur lengri tíma keyrslutíma á aðaláætlunargerð. Ef aðgerðaboð eru ekki reglulega greind og beitt (daglega, vikulega og svo framvegis) skaltu íhuga að slökkva á útreikningi meðan á keyrslu aðaláætlunargerðar stendur. Til að slökkva á útreikningi skaltu á síðunni **Aðaláætlanir** stilla tímamörkin **Aðgerðaboð** á **0** (núll) fyrir aðaláætlunina sem þú ert að keyra. Gakktu einnig úr skugga um að slökkt sé á stillingunni **Aðgerðaboð** í öllum þekjuflokkunum.

### <a name="calculated-delays"></a>Reiknaðar seinkanir

Þú getur tilgreint hversu langt í framtíðinni mögulegar tafir á áætluðum pöntunum eru greindar og tilkynntar. Þannig geturðu raðað hugsanlegum (seinkuðum) afhendingardagsetningum.

Ef ekki er hægt að uppfylla áætlaða pöntun fyrir umbeðinn dag er hún áætluð fyrir fyrsta uppfyllingardag fyrir færslu, samkvæmt afhendingartímum og efni og getu til ráðstöfunar.

### <a name="approved-requisitions-time-fence"></a>Samþykkt tímamörk beiðna (dagar)

Þú getur sett upp aðaláætlanagerð til að stofna áætlaðar pantanir fyrir eftirspurn beiðna. Stilltu valkostinn **Inniheldur beiðnir** á **Já** á flýtiflipanum **Almennt** á síðunni **Aðaláætlanir**. Síðan, þegar tilgangur viðurkenndrar beiðni er áfylling, stofnar aðaláætlunargerðin sjálfvirkt samsvarandi áætlaða pöntun til að uppfylla hana. Áfyllingaraðferðin ræðst af framboðsreglum sem hafa verið settar upp fyrir vörur innan fyrirtækisins. Þegar áfyllingarbeiðni er stofnuð og samþykkt, er engra frekari aðgerða notenda þörf.

Með því að stilla valkostinn **Samþykkt tímamörk beiðni** á **Já** á flýtiflipanum **Tímamörk í dögum**, er hægt að hnekkja viðurkenndum beiðnum tímamarka sem eru skilgreind fyrir vöruna á meðan röðun stendur. Í þessu tilfelli skráirðu fjölda liðinna daga sem eftirspurn úr samþykktum beiðnum, sem hafa tilganginn áfyllingar, ætti að vera innifalin í röðun. Til dæmis er hægt að tilgreina að aðeins óuppfylltar, komnar framyfir eftirspurnir úr samþykktum beiðnum sem voru stofnaðar á síðustu 10 dögum eigi við og séu áætlaðar.

### <a name="sequencing"></a>Röðun

Röðun gerir ráð fyrir að áætluðum pöntunum sé raðað á grundvelli raðgreiningareiginda sem tengjast kláraðri vöru. Hún er oft notuð til að undirbúa framleiðslupantanir fyrir umbúðir. Til dæmis er hægt að nota hana til að pakka kössum í ákveðinni röð, byggt á lit og stærð.

Með því að stilla valkostinn **Röðun** á **Já** er hægt að tilgreina hversu langt í framtíðina þarf að raða aðgerðum eða vinnslum. Hafðu í huga að því lengur sem tímamörkin eru, því lengur mun það taka fyrir aðaláætlunargerðina að keyra.

### <a name="calculated-delays"></a>Reiknaðar seinkanir

Tafvalkostir hjálpa til við að tryggja að pantanir hafi mögulegar áætlaðar dagsetningar. Eftirfarandi valkostir eru í boði á flýtiflipanum **Reiknaðar tafir** á síðunni **Aðaláætlanir**:

- **Gakktu úr skugga um að áætlaðar pantanir séu ekki stofnaðar fyrir keyrsludagsetningu aðaláætlanagerðar** - Stilltu þennan valkost á **Já** til að tryggja að ekki sé hægt að raða pöntunum fyrir liðnar dagsetningar.
- **Bæta reiknaðri seinkun við á þarfadagsetningu** (undir **Áætlaðar innkaupapantanir**) - Stilltu þennan valkost á **Já** til að bæta reiknaðri töf við þarfirnar.
- **Bæta reiknaðri seinkun við á þarfadagsetningu** (undir **Framleiðslutillögur**) - Stilltu þennan valkost á **Já** til að bæta reiknaðri töf við þarfirnar.
- **Bæta reiknaðri seinkun við á þarfadagsetningu** (undir **Áætlaður flutningur**) - Stilltu þennan valkost á **Já** til að bæta reiknaðri töf við þarfirnar.
- **Bæta reiknaðri seinkun við á þarfadagsetningu** (undir **Áætlað kanban**) - Stilltu þennan valkost á **Já** til að bæta reiknaðri töf við þarfirnar.

Þegar þú stillir valkostina **Bæta reiknaðri töf við á þarfadagsetningu** á **Já** til að bæta við töfum á þarfirnar telur kerfið umfang tilfanganna til greina og stofnar mögulegar áætlaðar pantanir. Endurreikningur á áætluðum pöntunardagsetningum eykur keyrslutíma fyrir aðaláætlunargerð. Ef þú þarft þess vegna ekki að nota tafir skaltu velja valkostina **Nei**.

## <a name="positive-and-negative-days"></a>Jákvæðir og neikvæðir dagar

Jákvæðir og neikvæðir dagar hafa áhrif á hvernig aðaláætlanagerð leggur til áætlaðar pantanir og aðgerðir. Jákvæðir og neikvæðir dagar eru stilltir á vöruþekjuflokkinn í vörunni. Þú getur skilgreint mismunandi þekjuflokka og stillt færibreytur þeirra á síðunni **Þekjuflokkar** (**Aðaláætlanagerð \> Uppsetning \> Þekja \> Þekjuflokkar**).

### <a name="positive-days"></a>Jákvæðir dagar

Jákvæðar dagar benda til hversu langt í framtíðina aðaláætlunargerð telur núverandi birgðir eða kvittanir uppfylli framtíðareftirspurn. Til dæmis, ef jákvæðir dagar eru stilltir á **100** er hægt að nota núverandi birgðir til að uppfylla eftirspurn á næstu 100 dögum. Ef gerð er pöntun eftir 150 daga frá núverandi dagsetningu, mun aðaláætlananagerð stofna áætlaða pöntun til að fullnægja þeirri eftirspurn, jafnvel þó að lagerbirgðir fyrir hlutinn geti fullnægt pöntuninni. Þegar vörur sem eru fljótar að seljast og hafa stuttan afhendingartíma eru annars vegar viltu kannski ekki nota lagerbirgðir fyrir pöntun sem er langt fram í tímann. Í þessu tilfelli með vöru sem selst fljótt munu núverandi lagerbirgðir klárast hratt og fleiri pantanir kynnu að vera gerðar í framtíðinni til að uppfylla framtíðareftirspurn á réttum tíma, sem væri mögulegt vegna stutts afhendingartíma vörunnar.

Jákvæðir dagar hafa einnig áhrif á aðgerðaboðin. Til dæmis gæti kerfið mælt með því að þú aukir innkaupatillögu svo að hún innihaldi eftirspurn sem er innan fjölda jákvæðra daga í framtíðinni. Ef jákvæðir dagar eru stilltir á **100** og ef það er eftirspurn eftir vöru 30 daga frá núverandi degi mun kerfið búa til áætlaða pöntun til að fullnægja þeirri eftirspurn. Ef það er eftirspurn eftir sömu vöru eftir 90 dögum frá núverandi degi, mun kerfið mæla með því að þú auki magnið pöntunarinnar eftir 30 daga frá núverandi degi svo að pöntunin nái einnig til eftirspurnar eftir 90 daga. Hins vegar, ef eftirspurn er eftir vörunni eftir 150 daga frá núverandi degi, mun kerfið ekki mæla með því að þú aukir magn pöntunarinnar sem var þegar var áætluð. Í staðinn verður ný áætluð pöntun stofnuð.

Að jafnaði eru jákvæðir dagar stilltir á tölu sem er á milli lengstu afhendingartíma varanna og þekjutímamarkanna. Við mælum með að þú úthlutir vörum sem eru reglulega keyptar eða framleiddar í þekjuflokk þar sem jákvæðir dagar eru jafnframt afhendingartími vörunnar.

### <a name="negative-days"></a>Neikvæður dagafjöldi

Neikvæðar dagar gefa til kynna hversu seint kvittanir eru leyfðar. Þær tákna fjölda daga sem þú ert tilbúin/n að bíða áður en þú pantar nýja áfyllingu þegar þú ert með neikvæðan lager eða hefur ekki næga birgðir. Neikvæðir dagar svara spurningunni: Ættum við að stofna nýja innkaupapöntun fyrir vöruna, eða ættum við að nota fyrirliggjandi kaup, jafnvel þó að við vitum að vara verði sein?

Til dæmis hefur þú sölupöntun á vöru 15 daga eftir núverandi dagsetningu. Þú hefur einnig innkaupapöntun á sömu vöru. Þessi innkaupapöntun verður móttekin eftir 20 daga frá núverandi degi. Viltu að kerfið stofni innkaupapöntun fyrir þá söluáætlun, eða viltu nota fyrirliggjandi pöntun, jafnvel þótt þú getir ekki uppfyllt sölupöntunina á réttum tíma? Ef neikvæðir dagar eru stilltir á minna en **5** til að gefa til kynna að vörunni geti seinkað um að hámarki fimm daga, stofnar kerfið nýja innkaupatillögu til að fullnægja sölupöntuninni. Ef neikvæðir dagar eru stilltir á hærra en **5** notar kerfið fyrirliggjandi pöntun á vörunni.

Neikvæðir dagar hafa einnig áhrif á árangur aðaláætlunargerðar. Ef neikvæðir dagar eru stilltir á háa tölu verða mörg aðgerðaskilaboð mynduð.

Við mælum með að þú stillir neikvæða daga á tölu sem er lægri en afhendingartími vörunnar.

### <a name="dynamic-negative-days"></a>Kvikir neikvæðir dagar

Kvikir neikvæðir dagar taka tillit til afhendingartíma vörunnar og neikvæðra daga sem þú tilgreindir. Kerfið mun stofna nýtja innkaupatillögu á grundvelli tímamarka neikvæðra daga sem er reiknuð með því að nota eftirfarandi formúlu:

Afhendingartími + Neikvæðir dagar + Núverandi dags. – Þarfadags.

Kerfið notar aðeins áætlaðar birgðapantanir sem eru innan þessa tímabils og það stofnar nýja áætlaða pöntun utan þess. Kosturinn við kvika neikvæða daga er að þeir munu innihalda staka afhendingartíma, til að endurnota fyrirliggjandi pantanir og forðast stofnun á nýjum áætluðum pöntunum sem munu enda með síðari dag vegna tafa sem stafa af afhendingartíma. 

Nánari upplýsingar er að finna í [Neikvæðir dagar og kvikir neikvæðir dagar](/dynamics365/unified-operations/supply-chain/master-planning/more-about-dynamic-negative-days).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]