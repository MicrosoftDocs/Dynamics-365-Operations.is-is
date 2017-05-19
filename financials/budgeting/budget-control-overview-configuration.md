---
title: "Yfirlit fjárhagsáætlunarstýringar "
description: "Þessi grein kynnir fjárhagsáætlunarstýringar og veitir upplýsingar um hjálp við að skilgreina fjárhagsáætlunarstýringu í Microsoft Dynamics 365 fyrir Operations þannig að hægt er að stjórna fjármagni."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 60493
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 4caef8eb4d11ad5d2ba1ce0e23d869c0b26b5466
ms.contentlocale: is-is
ms.lasthandoff: 04/25/2017


---

# <a name="budget-control-overview"></a>Yfirlit fjárhagsáætlunarstýringar 

[!include[banner](../includes/banner.md)]


Þessi grein kynnir fjárhagsáætlunarstýringar og veitir upplýsingar um hjálp við að skilgreina fjárhagsáætlunarstýringu í Microsoft Dynamics 365 fyrir Operations þannig að hægt er að stjórna fjármagni.

<a name="overview"></a>Yfirlit
--------

Fjárhagsáætlunarstýring í Microsoft Dynamics 365 for Operations styður Stjórnun fjárhagsleg tilföng fyrirtækis með bókhaldslykill, verkflæði, notendaflokkur, upprunaskjal og færslubók, skilgreinanlega sjóður, tiltækt útreikningur, ferli fjárhagsáætlunar, og mörk. Þegar stýringar eru á sínum stað, getur fyrirtæki áætlað, mæla, stjórna og spá fyrir um hennar fjárhagslegar tilföng gegnum fjárhagsársins. 

Eftir að áætlun hefur verið samþykkt í Dynamics 365 fyrir Operations, geturðu notað fjárhagsáætlanir til að mynda færslur í fjárhagsáætlunarskrá til að skrá útgjöld fjárhagsáætlunar fyrir fyrirtæki. Einnig er hægt að stofna eða flytja inn færslur í fjárhagsáætlunarskrá úr hugbúnaði þriðja aðila án þess að nota virkni fjárhagsáætlunargerðar. 

Hægt er að skrá útgjöld með aðallykla og fjárhagsvíddir. Þú getur skilgreint stýringu á heildarútgjöldum til að mæta reglum og kröfum fyrirtækis, með flokkun samsetningar fjárhagsvídda og aðallykla. 

Eftirfarandi línurit sýnir stað fjárhagsáætlunarstýringar á stigum dæmigert fjárhagsáætlunarferlis

[![BudgetingCycle](./media/budgetingcycle-300x198.png)](./media/budgetingcycle.png) 

Hægt er að skilgreina fjárhagsáætlunarstýringar samkvæmt mörgum þáttum:

-   **Fjárhagsvíddir**- Hvaða fjárhagsvíddir þarf að nota fyrir fjárhagsáætlun og rauntölur og hvaða fjárhagsvíddir eru nauðsynlegar til að stýra fjárhagsáætlun? Eru tilteknar vöruvíddasamsetningar eða aðallykla sem krefjast tiltekna athygli? Til dæmis er krafist að rekja fjárhagsáætlun í raunupphæðir með kostnaðarstað og forriti? Þurfa ferðakostnaður sérstaka athygli
-   **Tími**- Hvaða tímarammann (fjárhagstímabil, fjárhagstímabil til dagsetningar í dag o.s.frv.,) verður notuð til að meta tiltækt fjármagn fjárhagsáætlunar?
-   **Upprunaskjöl**- Hvaða upprunaskjöl þarf að meta fyrir fjárhagsáætlunarstýringar? Á að meta skjölin á hverja línu eða fyrir hvert skjal?
-   **Útreikning á tiltæku fjármagni**- ættu skjöl eins og innkaupabeiðnir (áætluð fjárúthlutun) og innkaupapantanir (fjárúthlutanir) vera tekið tillit til í útreikningi á tiltæku fjármagni? Ættu skjölum með stöðuna drög að vera höfð í huga í útreikningi?
-   **Hnekkja heimild** - Hver hafa heimild til að fara yfir tiltæka fjárhagsáætlun?

Fjárhagsáætlunarstýring er fyllilega samþætt við Dynamics 365 for Operations. Þess vegna er hægt að meta tiltæka fjárhagsáætlun fyrir bæði áætluð innkaup og raunverulega innkaup. Fyrirspurnir og skýrslur um fjárhag eru tiltækar. Því geta noendur metið Fjárhagsáætlun samhliða ferli fjárhagsáætlunar og gert leiðréttingar sem þarf, í mynd endurskoðunar fjárhagsáætlunar eða flutninga. Fjárhagsáætlunarstjóri getur einnig flytja fjárhagsáætlunar og raunupphæðir í Microsoft Excel til að greina og spá betur eftir þörfum.

## <a name="configuring-budget-control"></a>Skilgreinir fjárhagsáætlunarstýringar
### <a name="budget-cycle-time-span"></a>Tímabil fjárhagsáætlunar

Eftir að grunnáætlanagerð er skilgreint geturðu skilgreint upphafs- og lokatímabil fyrir fjárhagsáætlun og fjárhagsáætlunarstýring á **tímabil fjárhagsáætlunar** síðu. Fjárhagsáætlunarferli samsvara oft fjárhagsdagatöl en getur náð yfir á fjárhagsár.

Næstu skref í skilgreiningu er lokið á mismunandi flipum á **skilgreiningu fjárhagsáætlunarstýringar** síðu.

### <a name="define-parameters"></a>Skilgreina færibreytur

Byggt á fjárhagsvíddir virkjuð fyrir fjárhagsáætlun, hægt er að nota allar eða hlutmengi fjárhagsvíddirnar fyrir fjárhagsáætlunarstýringu. 

Þar að auki er hægt að tilgreina sjálfgefið tímabil (t.d. **fjárhagsár**, **fjárhagsárs til dagsetningarí dag**, **fjárhagstímabil**, eða **Ársfjórðungslega**) fjárhagsáætlunarstýringu verður framkvæmd á í tengdu tímabili fjárhagsáætlunar. Einnig er hægt að tilgreina sjálfgefinn stjórnanda fjárhagsáætlunar og þröskuld sem er notaður til að tilkynna notendum þegar þröskuld hefur verið náð. Gildin í þessi svæði eru notuð sem sjálfgefin gildi í hvaða nýja reglu fjárhagsáætlunarstýringar sem er eða fjárhagsáætlunarflokk sem er stofnaður. Hins vegar er hægt að breyta sjálfgefin gildi fyrir einstaka flokka eða reglur. 

Aðferðir sem notaðar eru við að stofna og skrá fjárhagsáætlun í fjárhagsáætlunarskrá spila hlutverk við að ákvarða tímabil sem er valið þegar tiltækt fjármagn fjárhagsáætlunar er metið. Ef árleg upphæð fyrir samsetningu víddargildis er þróuð og nota, þá gæti nálgun sem byggist á fjárhagsárinu eða fjárhagsárs til dagsins í dag verið gáfuleg. Hins vegar ef fyrirtækis stofnar fjárhagsáætlunar eftir fjárhagstímabili eða úthlutar á fjárhagstímabil og vill ítarlegri stýringu, vilja þau kannski íhuga fjárhagsártil dagsins í dag eða ársfjórðungsleg tímabil. 

Þar að auki spilar menning fyrirtækis þíns og hvernig hún tengist fjárhagsáætlun og fjárhagsáætlunarstýringu hlutverk í að skilgreina skilgreininguna.

### <a name="over-budget-permissions"></a>Heimildir yfir fjárhagsáætlun

Næsta á **heimildir Yfir fjárhagsáætlun** flipanum, geturðu tilgreint notendaflokka. Einnig er hægt að tilgreina hvort notendur sem eru meðlimir flokks hafa heimild til að fara fram úr fjárhagsáætlun. Þú getur komið í veg fyrir að notendur fari umfram þröskuld fjárhagsáætlunar sem var stillt á **færibreytur Fjárhagsáætlunar** síðu, eða þú getur komið í veg fyrir að þeir fari umfram fjárhagsáætlun samkvæmt einhverri upphæð, óháð þröskuldi. Byggt á hversu forvirkt fyrirtæki stjórnar sínum útgjöldum, getur þessar heimildir hjálpað til við að stjórna fjárhagslegum tilföng. 

### <a name="budget-funds-available"></a>Tiltækt fjármagn úr fjárhagsáætlun

Næst, á **fjármagn fjárhagsáætlunar sem er tiltækt** síðu er hægt að skilgreina formúlu til að nota við útreikning á tiltækt fjármagn fjárhagsáætlunar. Byggt á því hve íhaldssamur stofnun stjórnar sínu fjármagn , eða í umfjöllun um reglugerðir eða iðnaður kröfur, geta útreikningur innihaldið drög eða óbókað skjal. 

> [!NOTE] 
> Ef þessum útreikningi er breytt við ferli fjárhagsáætlunar, munu breytingarnar ekki hafa áhrif á nein skjöl sem áður hafa staðist athuganir fjárhagsáætlunarstýringar og sem hafa verið bókaðar eða lokið.

### <a name="documents-and-journals"></a>Skjöl og færslubækur

Næst, í **Skjöl og færslubækur** síðu er hægt að velja hvaða upprunaskjöl og færslubækur verður háð athuganir fjárhagsáætlunarstýringar og hvort athugun mun eiga sér stað á stigi innfærslu lína eða fyrir skjalið í heild. 

Stemma ætti af upprunaskjölin sem eru valin með gátreitunum fyrir stöður se innifaldar eru í útreikning tiltæks fjármagns fjárhagsáætlunar. Til dæmis ef valin var **frátekt fjárhagsáætlunar fyrir fjárúthlutun**, skal velja í **Innkaupapantanir** valkost. Þegar athugun á fjárhagsáætlun er gerð fyrir upphæðir og reikninga í innkaupalínu mun eftirlitstegund fjárhagsáætlunar sem er úthlutað frátektinni vera **fjárúthlutun**. Þegar athugun á fjárhagsáætlun er gerð fyrir upphæðir og reikninga í innkaupabeiðni mun eftirlitstegund fjárhagsáætlunar sem er úthlutað frátektinni vera **áætluð fjárúthlutun**. 

Ef **frátektir Fjárhagsáætlunar fyrir fjárúthlutunar** og/eða **frátektir Fjárhagsáætlunar fyrir áætlaða fjárúthlutun** eru hafðar með í útreikning á tiltæku fjármagni og þarf að vera speglað með bókanir í fjárhag, eiga skráningarbókhald að vera virkar á **færibreytur fjárhags** síðu.  

### <a name="assign-budget-models"></a>Úthluta fjárhagsáætlunarlíkönum

Næsta, á **Úthluta fjárhagsáætlunarlíkönum** síðu er hægt að úthluta fjárhagsáætlunarlíkönum til tímabil ferlis fjárhagsáætlunar til að vera hafðar með í fjárhagsáætlunarstýringu.

### <a name="define-budget-control-rules"></a>Skilgreina reglur fjárhagsáætlunarstýringar

Næsta, á **skilgreina reglur fjárhagsáætlunarstýringar** síðu er að stofna reglur samkvæmt fjárhagsvíddir sem eru virkjaðar fyrir fjárhagsáætlunarstýringu. Til dæmis, ef áhersla er á útgjöld eða svið útgjalda fyrir deild, þá geturðu notað skilgreiningar á þessum flipa til að skilgreina og meta þessi útgjöld. Hægt er að skilgreina mismunandi þröskulda fyrir hverja reglu fjárhagsáætlunarstýringar. 

> [!Important]
> Fjárhagsáætlunarstýring verður virkjuð fyrir alla aðallykla af gerðinni **Hagnaður og Tap**, **Kostnaður**, **Tekjuafgangur, efnahagsreikningur, Skuld, Eigið fé** eða **eign**. Ef þessi flipi inniheldur reglu sem hefur autt skilyrði , verður fjárhagsáætlunarstýring virk fyrir **allar** samsetningar fjárhagsvídda sem innihalda aðallykla þessara gerða. Þess vegna er mikilvægt að búa til reglur fjárhagsáætlunarstýringar og skilgreina svið samsetningar fjárhagsvídda þar sem mikilvægt er að kveikt er á fjárhagsáætlunarstýringu.  

### <a name="select-main-accounts"></a>Velja aðallykla

Ef **aðallykils** er ekki valin sem vídd fjárhagsáætlunarstýringar á **Skilgreina færibreytur** síðu en tilteknum útgjöldum er stjórnað, er hægt að velja þær útgjöld á í **Velja aðallykla** flipa. Ef **aðallykils** er valinn sem vídd fjárhagsáætlunarstýringar, er ekki krafist neinna færsla.  

### <a name="define-budget-groups"></a>Skilgreina fjárhagsáætlunarflokka

Næsta, á **Skilgreina fjárhagsáætlunarflokkar** flipa er einnig hægt að skilgreina einkvæmt samsetningar fjárhagsvídda þar sem tilföng fjárhagsáætlunar eru hópaðar saman fyrir aðra athugun á fjárhagsáætlun. Hægt er að stofna eina færslu sem inniheldur allt fyrirtækið eða skilgreina margir flokkar til að tákna einstaka deildir eða kostnaðarstaða.  

### <a name="define-message-levels"></a>Skilgreina skilaboðastig

Ef ætti að fela viðvörunarboð fjárhagsáætlunarstýringar fyrir einhvern notendaflokk, er hægt að tilgreina þá flokka á **Skilgreina skilaboðastig** síðu. Notendur notendaflokksins munu áfram fá villuboð þegar tiltækt fjármagn fjárhagsáætlunar er komið fram yfir, á grunni heimilda þeirra að fara yfir fjárhagsáætlun.

### <a name="activate-budget-control"></a>Virkja fjárhagsáætlunarstýringu

Eftir að fjárhagsáætlunarstýringar hefur verið skilgreindur, þú getur kveikt og virkja fjárhagsáætlunarstýringu á í **Virkja fjárhagsáætlunarstýringu** flipa. Útgafan í Drögum verða þá virkar.
> [!Important]
> Eftir að fjárhagsáætlunarstýringu hefur verið kveikt á og virkjað, og eftir að færslur hafa verið bókaðar, það ætti ekki að slökkva á miðju ári. Þegar slökkt er á fjárhagsáætlunarstýringu, eru færslur fjárhagsáætlunar ekki skráðar vegna rakningar, og athuganir á fjárhagsáætlun eru ekki lengur framkvæmdar. Þess vegna er skjöl sem þegar hafa verið bókaðar hugsanlega ekki rétt að endurspegla allar upphæðir losunar eða stöður í fyrirspurnum og skýrslum sem tengjast fjárhagsáætlunarstýringu. Þar á meðal talnagögn fjárhagsáætlunarstýringar fyrir hvers kyns forstreymi eða leiðrétta skjöl og færslubækur. 

Athugið einnig að færslur, þar á meðal færslur fjárhagsáætlunarskrár sem hafa verið bókaðar áður en kveikt er á fjárhagsáætlunarstýringu eru ekki taldar með fyrir fjárhagsáætlunarstýringu. Þess vegna er mælt með því að kveikja á fjárhagsáætlunarstýringu aðeins í upphafi nýtt fjárhagsáætlunarferlis. Gangið úr skugga um að færslur fjárhagsáætlunarskrár sem inniheldur upphafsstöður fjárhagsáætlunar fyrir fjárhagsáætlunarstýringu fái staða fjárhagsáætlunar uppfærða eingöngu eftir að kveikt er á fjárhagsáætlunarstýringu. Allar opin skjalið (t.d. Innkaupapöntun) verða athuguð fyrir tiltækt fjármagn fjárhagsáætlunar og fá frátekt fjárhagsáætlunar fyrir fjárhagsáætlunarstýringu, þegar notandi ræsir handvirkt fjárhagsáætlunarstýringu í skjalinu.

## <a name="using-budget-control"></a>Notkun fjárhagsáætlunarstýring
Eftir að kveikt hefur verið á fjárhagsáætlunarstýringu, notendur fá viðvörunar- og villuboð fjárhagsáætlunarstýringar í skjöl og færslubækur sem eru skilgreindar fyrir fjárhagsáætlunarstýringu. Munið að hægt að skilgreina fjárhagsáætlunarstýringu svo að notendur eru varaðir við þegar þeir fara yfir fjármagn fjárhagsáætlunar en geta samt að halda áfram að staðfesta eða bóka færsluna. Notendur geta skoðað nákvæmar upplýsingar um misheppnaðar athuganir á fjárhagsáætlun á **villur Fjárhagsáætlunarstýringar og viðvaranir** síðu.   

Úr þessari síðu geta notendur kafað í **talnagögn fjárhagsáætlunarstýringar eftir tímabili** síðu til að skoða upplýsingar um framboð fjárhagsáætlunar og frátekningar á víddarsamsetningu fjárhagsáætlunarstýringar. Notendur geta einnig kafa í **talnagögn fjárhagsáætlunarstýringar** síðu til að skoða framboð á fjárhagsáætlun fyrir allar samsetningar fjárhagsvídda sem eru notaðar í fjárhagsáætlunarstýringu. 

Ef fjárhagsáætlunarstýring er kveikt fyrir Innkaupapantanir, getur stjórnanda fjárhagsáætlunar notað vinnusvæðið **fjárhagsáætlun og spár** til að skoða biðröð fyrir biðröðinni allar óstaðfestar innkaupapantanir sem eru með viðvaranir frá athugun á fjárhagsáætlun og villuboð. Hafi stjórnanda fjárhagsáætlunar heimildir yfir fjárhagsáætlun skilgreindar hann getur staðfesta Innkaupapöntun beint í vinnusvæðið.    




