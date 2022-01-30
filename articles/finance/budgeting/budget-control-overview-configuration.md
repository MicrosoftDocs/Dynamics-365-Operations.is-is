---
title: Yfirlit fjárhagsáætlunarstýringar
description: Í þessu efnisatriði er kynntur eiginleiki fjárhagsáætlunarstýringar og veittar upplýsingar sem hjálpa til við að stilla fjárhagsáætlunarstýringu til að ná sem mest út úr stjórnun á fjárhagslegum tilföngum fyrirtækisins.
author: panolte
ms.date: 11/08/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "60493"
- intro-internal
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14b852bb4aeca927adeeb2665b9887e467b71158
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2022
ms.locfileid: "7986057"
---
# <a name="budget-control-overview"></a>Yfirlit fjárhagsáætlunarstýringar

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Í þessu efnisatriði er kynntur eiginleiki fjárhagsáætlunarstýringar og veittar upplýsingar sem hjálpa til við að stilla fjárhagsáætlunarstýringu til að ná sem mest út úr stjórnun á fjárhagslegum tilföngum fyrirtækisins.

Fjárhagsáætlunarstýring styður stjórnun fjárhagslegra tilfanga fyrirtækis með bókhaldslykli, verkflæði, notendaflokkum, upprunaskjölum og færslubókum, stillanlegum útreikningi á tiltækum sjóðum, fjárhagsáætlunarferlum og mörkum. Þegar stýringar eru á sínum stað, getur fyrirtæki áætlað, mæla, stjórna og spá fyrir um hennar fjárhagslegar tilföng gegnum fjárhagsársins. 

Eftir að áætlun hefur verið samþykkt í kerfinu geturðu notað fjárhagsáætlanir til að mynda færslur í fjárhagsáætlunarskrá til að skrá útgjöld fjárhagsáætlunar fyrir fyrirtæki. Einnig er hægt að stofna eða flytja inn færslur í fjárhagsáætlunarskrá úr hugbúnaði þriðja aðila án þess að nota virkni fjárhagsáætlunargerðar. 

Hægt er að skrá útgjöld með aðallykla og fjárhagsvíddir. Þú getur skilgreint stýringu á heildarútgjöldum til að mæta reglum og kröfum fyrirtækis, með flokkun samsetningar fjárhagsvídda og aðallykla. 

Eftirfarandi línurit sýnir stað fjárhagsáætlunarstýringar á stigum dæmigert fjárhagsáætlunarferlis

[![Dæmigerð fjárlagagerð.](./media/budgetingcycle-300x198.png)](./media/budgetingcycle.png) 

Hægt er að skilgreina fjárhagsáætlunarstýringar samkvæmt mörgum þáttum:

- **Fjárhagsvíddir**- Hvaða fjárhagsvíddir þarf að nota til að tilkynna fjárhagsáætlun og rauntölur og hvaða fjárhagsvíddir eru nauðsynlegar til að stýra fjárhagsáætlun? Eru tilteknar vöruvíddasamsetningar eða aðallyklar sem krefjast tiltekinnar athygli? Til dæmis er krafist að rekja fjárhagsáætlun í raunupphæðir með kostnaðarstað og forriti? Þarf ferðakostnaður sérstaka athygli?
- **Tími**- Hvaða tímarammann (fjárhagstímabil, fjárhagstímabil til dagsetningar í dag o.s.frv.,) verður notuð til að meta tiltækt fjármagn fjárhagsáætlunar?
- **Upprunaskjöl**- Hvaða upprunaskjöl þarf að meta fyrir fjárhagsáætlunarstýringar? Á að meta skjölin á hverja línu eða fyrir hvert skjal?
- **Útreikning á tiltæku fjármagni**- ættu skjöl eins og innkaupabeiðnir (áætluð fjárúthlutun) og innkaupapantanir (fjárúthlutanir) vera tekið tillit til í útreikningi á tiltæku fjármagni? Ættu skjöl með stöðuna drög að vera höfð með í útreikningi?
- **Hnekkja heimild** - Hverjir hafa heimild til að fara yfir tiltæka fjárhagsáætlun?

Fjárhagsáætlunarstýring er að fullu samþætt við forritið. Þess vegna er hægt að meta tiltæka fjárhagsáætlun fyrir bæði áætluð innkaup og raunverulega innkaup. Fyrirspurnir og skýrslur um fjárhag eru tiltækar. Því geta notendur metið Fjárhagsáætlun samhliða ferli fjárhagsáætlunar og gert leiðréttingar sem þarf, í mynd endurskoðunar fjárhagsáætlunar eða flutninga. Fjárhagsáætlunarstjóri getur einnig flutt fjárhagsáætlun og raunupphæðir í Microsoft Excel til að greina og spá betur eftir þörfum.

## <a name="configuring-budget-control"></a>Skilgreinir fjárhagsáætlunarstýringar

### <a name="budget-cycle-time-span"></a>Tímabil fjárhagsáætlunar

Eftir að grunnáætlanagerð er skilgreind geturðu skilgreint upphafs- og lokatímabil fyrir fjárhagsáætlun og fjárhagsáætlunarstýring á síðunni **Tímabil fjárhagsáætlunar**. Fjárhagsáætlunarferli samsvara oft fjárhagsdagatöl en getur náð yfir á fjárhagsár.

Næstu skref í skilgreiningunni er lokið í flipum sem eru opnaðir á síðunni **Skilgreining fjárhagsáætlunarstýringar**.

### <a name="define-parameters"></a>Skilgreina færibreytur

Byggt á fjárhagsvíddir virkjuð fyrir fjárhagsáætlun, hægt er að nota allar eða hlutmengi fjárhagsvíddirnar fyrir fjárhagsáætlunarstýringu. 

Þar að auki er hægt að tilgreina sjálfgefið tímabil (t.d. **Fjárhagsár**, **Fjárhagsár til dagsins í dag**, **Fjárhagstímabil** eða **Ársfjórðungslegt**) sem fjárhagsáætlunarstýring verður framkvæmd á tímabili tengdrar fjárhagsáætlunar. Einnig er hægt að tilgreina sjálfgefinn stjórnanda fjárhagsáætlunar og þröskuld sem er notaður til að tilkynna notendum þegar þröskuld hefur verið náð. Gildin í þessi svæði eru notuð sem sjálfgefin gildi í hvaða nýja reglu fjárhagsáætlunarstýringar sem er eða fjárhagsáætlunarflokk sem er stofnaður. Hins vegar er hægt að breyta sjálfgefin gildi fyrir einstaka flokka eða reglur. 

Aðferðir sem notaðar eru við að stofna og skrá fjárhagsáætlun í fjárhagsáætlunarskrá spila hlutverk við að ákvarða tímabil sem er valið þegar tiltækt fjármagn fjárhagsáætlunar er metið. Ef árleg upphæð fyrir samsetningu víddargildis er þróuð og nota, þá gæti nálgun sem byggist á fjárhagsárinu eða fjárhagsárs til dagsins í dag verið gáfuleg. Hins vegar ef fyrirtækis stofnar fjárhagsáætlunar eftir fjárhagstímabili eða úthlutar á fjárhagstímabil og vill ítarlegri stýringu, vilja þau kannski íhuga fjárhagsártil dagsins í dag eða ársfjórðungsleg tímabil. 

Þar að auki spilar menning fyrirtækis þíns og hvernig hún tengist fjárhagsáætlun og fjárhagsáætlunarstýringu hlutverk í að skilgreina skilgreininguna.

### <a name="over-budget-permissions"></a>Heimildir yfir fjárhagsáætlun

Næsta á **heimildir Yfir fjárhagsáætlun** flipanum, geturðu tilgreint notendaflokka. Einnig er hægt að tilgreina hvort notendur sem eru meðlimir flokks hafa heimild til að fara fram úr fjárhagsáætlun. Þú getur komið í veg fyrir að notendur fari umfram þröskuld fjárhagsáætlunar sem var stillt á **færibreytur Fjárhagsáætlunar** síðu, eða þú getur komið í veg fyrir að þeir fari umfram fjárhagsáætlun samkvæmt einhverri upphæð, óháð þröskuldi. Byggt á hversu forvirkt fyrirtæki stjórnar sínum útgjöldum, getur þessar heimildir hjálpað til við að stjórna fjárhagslegum tilföng. 

### <a name="budget-funds-available"></a>Tiltækt fjármagn úr fjárhagsáætlun

Næst, á **fjármagn fjárhagsáætlunar sem er tiltækt** síðu er hægt að skilgreina formúlu til að nota við útreikning á tiltækt fjármagn fjárhagsáætlunar. Byggt á því hve íhaldssamur stofnun stjórnar sínu fjármagn , eða í umfjöllun um reglugerðir eða iðnaður kröfur, geta útreikningur innihaldið drög eða óbókað skjal. 

> [!NOTE]
> Ef útreikningnum er breytt í fjárhagsáætlunarlotu munu breytingarnar ekki hafa áhrif á skjöl sem áður stóðust eftirlitseftirlit fjárhagsáætlunar og voru bókuð eða lokið. Eiginleiki sem er nefndur **Fylgstu aðeins með upphæðum í tiltækum útreikningi fjárlaga** gerir þér kleift að breyta hvaða gögnum er rakið í BudgetSourceTracking töflunum. Þegar kveikt er á þessum eiginleika eru upphæðir aðeins geymdar ef þær eru valdar til að nota við útreikning á tiltæku fjármagn fjárhagsáætlunar. Fyrir frekari upplýsingar, sjá [Fjármagn til ráðstöfunar](budget-funds-available.md).

Næst, í **Skjöl og færslubækur** síðu er hægt að velja hvaða upprunaskjöl og færslubækur verður háð athuganir fjárhagsáætlunarstýringar og hvort athugun mun eiga sér stað á stigi innfærslu lína eða fyrir skjalið í heild. 

Stemma ætti af upprunaskjölin sem eru valin með gátreitunum fyrir stöður se innifaldar eru í útreikning tiltæks fjármagns fjárhagsáætlunar. Til dæmis ef valin var **frátekt fjárhagsáætlunar fyrir fjárúthlutun**, skal velja í **Innkaupapantanir** valkost. Þegar athugun á fjárhagsáætlun er gerð fyrir upphæðir og reikninga í innkaupalínu mun eftirlitstegund fjárhagsáætlunar sem er úthlutað frátektinni vera **fjárúthlutun**. Þegar athugun á fjárhagsáætlun er gerð fyrir upphæðir og reikninga í innkaupabeiðni mun eftirlitstegund fjárhagsáætlunar sem er úthlutað frátektinni vera **áætluð fjárúthlutun**. 

Ef **Frátektir fjárhagsáætlunar fyrir fjárúthlutun** og/eða **Frátektir fjárhagsáætlunar fyrir áætlaða fjárúthlutun** eru hafðar með í útreikning á tiltæku fjármagni fjárhagsáætlunar og þarf að koma fram í bókunum í fjárhag skal merkja þetta val í flokknum **Skráningarbókhald** á síðunni **Færibreytur fjárhags**.

### <a name="assign-budget-models"></a>Úthluta fjárhagsáætlunarlíkönum

Næsta, á **Úthluta fjárhagsáætlunarlíkönum** síðu er hægt að úthluta fjárhagsáætlunarlíkönum til tímabil ferlis fjárhagsáætlunar til að vera hafðar með í fjárhagsáætlunarstýringu.

### <a name="define-budget-control-rules"></a>Skilgreina reglur fjárhagsáætlunarstýringar

Næsta, á **skilgreina reglur fjárhagsáætlunarstýringar** síðu er að stofna reglur samkvæmt fjárhagsvíddir sem eru virkjaðar fyrir fjárhagsáætlunarstýringu. Til dæmis, ef áhersla er á útgjöld eða svið útgjalda fyrir deild, þá geturðu notað skilgreiningar á þessum flipa til að skilgreina og meta þessi útgjöld. Hægt er að skilgreina mismunandi þröskulda fyrir hverja reglu fjárhagsáætlunarstýringar. 

> [!Important]
> Fjárhagsáætlunarstýring verður virkjuð fyrir alla aðallykla af gerðinni **Hagnaður og Tap**, **Kostnaður**, **Tekjuafgangur, efnahagsreikningur, Skuld, Eigið fé** eða **eign**. Ef flipinn **Skilgreina reglur fjárhagsáætlunarstýringar** inniheldur reglu sem hefur autt skilyrði verður fjárhagsáætlunarstýring virkjuð fyrir **allar** samsetningar fjárhagsvídda sem innihalda aðallykla þessara gerða. Þess vegna er mikilvægt að búa til reglur fjárhagsáætlunarstýringar og skilgreina svið samsetningar fjárhagsvídda þar sem mikilvægt er að kveikt er á fjárhagsáætlunarstýringu.

### <a name="select-main-accounts"></a>Velja aðallykla

Ef **aðallykils** er ekki valin sem vídd fjárhagsáætlunarstýringar á **Skilgreina færibreytur** síðu en tilteknum útgjöldum er stjórnað, er hægt að velja þær útgjöld á í **Velja aðallykla** flipa. Ef **aðallykils** er valinn sem vídd fjárhagsáætlunarstýringar, er ekki krafist neinna færsla.

### <a name="define-budget-groups"></a>Skilgreina fjárhagsáætlunarflokka

Næsta, á **Skilgreina fjárhagsáætlunarflokkar** flipa er einnig hægt að skilgreina einkvæmt samsetningar fjárhagsvídda þar sem tilföng fjárhagsáætlunar eru hópaðar saman fyrir aðra athugun á fjárhagsáætlun. Hægt er að stofna eina færslu sem inniheldur allt fyrirtækið eða skilgreina margir flokkar til að tákna einstaka deildir eða kostnaðarstaða.

### <a name="define-message-levels"></a>Skilgreina skilaboðastig

Ef ætti að fela viðvörunarboð fjárhagsáætlunarstýringar fyrir einhvern notendaflokk, er hægt að tilgreina þá flokka á **Skilgreina skilaboðastig** síðu. Notendur notendaflokksins munu áfram fá villuboð þegar tiltækt fjármagn fjárhagsáætlunar er komið fram yfir, á grunni heimilda þeirra að fara yfir fjárhagsáætlun.

### <a name="activate-budget-control"></a>Virkja fjárhagsáætlunarstýringu

Eftir að fjárhagsáætlunarstýringar hefur verið skilgreindur, þú getur kveikt og virkja fjárhagsáætlunarstýringu á í **Virkja fjárhagsáætlunarstýringu** flipa.

> [!Important]
> Eftir að fjárhagsáætlunarstýringu hefur verið kveikt á og virkjað, og eftir að færslur hafa verið bókaðar, það ætti ekki að slökkva á miðju ári. Þegar slökkt er á fjárhagsáætlunarstýringu, eru færslur fjárhagsáætlunar ekki skráðar vegna rakningar, og athuganir á fjárhagsáætlun eru ekki lengur framkvæmdar. Þess vegna er skjöl sem þegar hafa verið bókaðar hugsanlega ekki rétt að endurspegla allar upphæðir losunar eða stöður í fyrirspurnum og skýrslum sem tengjast fjárhagsáætlunarstýringu. Þar á meðal talnagögn fjárhagsáætlunarstýringar fyrir hvers kyns forstreymi eða leiðrétta skjöl og færslubækur. 

Athugið einnig að færslur, þar á meðal færslur fjárhagsáætlunarskrár sem hafa verið bókaðar áður en kveikt er á fjárhagsáætlunarstýringu eru ekki taldar með fyrir fjárhagsáætlunarstýringu. Þess vegna er mælt með því að kveikja á fjárhagsáætlunarstýringu aðeins í upphafi nýtt fjárhagsáætlunarferlis. Gangið úr skugga um að færslur fjárhagsáætlunarskrár sem inniheldur upphafsstöður fjárhagsáætlunar fyrir fjárhagsáætlunarstýringu fái staða fjárhagsáætlunar uppfærða eingöngu eftir að kveikt er á fjárhagsáætlunarstýringu. Allar opin skjalið (t.d. Innkaupapöntun) verða athuguð fyrir tiltækt fjármagn fjárhagsáætlunar og fá frátekt fjárhagsáætlunar fyrir fjárhagsáætlunarstýringu, þegar notandi ræsir handvirkt fjárhagsáætlunarstýringu í skjalinu.

## <a name="using-budget-control"></a>Notkun fjárhagsáætlunarstýring
Eftir að kveikt hefur verið á fjárhagsáætlunarstýringu færðu viðvörunar- og villuboð fjárhagsáætlunarstýringar í skjölum og færslubókum sem eru skilgreindar fyrir fjárhagsáætlunarstýringu. Mundu að hægt að skilgreina fjárhagsáætlunarstýringu þannig að notendur eru varaðir við þegar þeir fara yfir fjármagn fjárhagsáætlunar en geta samt haldið áfram að staðfesta eða bóka færslur. Þú getur skoðað nákvæmar upplýsingar um misheppnaðar athuganir á fjárhagsáætlun á síðunni **Villur og aðvaranir fjárhagsáætlunarstýringar**.

Úr þessari síðu geta notendur kafað í **talnagögn fjárhagsáætlunarstýringar eftir tímabili** síðu til að skoða upplýsingar um framboð fjárhagsáætlunar og frátekningar á víddarsamsetningu fjárhagsáætlunarstýringar. Notendur geta einnig kafa í **talnagögn fjárhagsáætlunarstýringar** síðu til að skoða framboð á fjárhagsáætlun fyrir allar samsetningar fjárhagsvídda sem eru notaðar í fjárhagsáætlunarstýringu. 

Ef fjárhagsáætlunarstýring er kveikt fyrir Innkaupapantanir, getur stjórnanda fjárhagsáætlunar notað vinnusvæðið **fjárhagsáætlun og spár** til að skoða biðröð fyrir biðröðinni allar óstaðfestar innkaupapantanir sem eru með viðvaranir frá athugun á fjárhagsáætlun og villuboð. Ef stjórnandi fjárhagsáætlunar er með heimildir vegna skilgreindra fjárhagsáætlana er hægt að staðfesta innkaupapantanir á vinnusvæðinu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
