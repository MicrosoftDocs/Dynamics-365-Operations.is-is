---
title: "Fjárhagsáætlunargerð"
description: "Markmiðið þessa lab er til að gefa með leiðsögn yfirlit yfir Microsoft Dynamics 365 uppfærslur virkni Aðgerða í svæðinu Fjárhagsáætlunargerðar. Tilgangur þessarar kennslu er að sýna dæmu um fljóta uppsetningu fyrir kerfi fjárhagsáætlunargerðar og sýna hvernig fjárhagsáætlunargerð má sinna með því að nota þessa uppsetningu.  Þessi lab mun áhersla sérstaklega á eftirfarandi viðskiptaferli eða verk--Stofna stigveldisskipan fyrir áætlanagerð og öryggisskilgreining notanda - Skilgreining aðstæður fjárhagsáætlunargerðar fjárhagsáætlunardálka, útlit og sniðmát fyrir Excel - Stofnun og virkjun fjárhagsáætlunar fjárhagsáætlunargerðar ferli - að Stofna skjal fjárhagsáætlunargerðar eftir pulling í rauntölur úr fjárhagi - með því að Nota úthlutanir til að leiðrétta gögn skjals fjárhagsáætlunar - Breyta skjali gögn fjárhagsáætlunar í Excel"
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 81b44aa7af3a05ebc28963f406fab98bfbbb340d
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning"></a>Fjárhagsáætlunargerð

Markmiðið þessa lab er til að gefa með leiðsögn yfirlit yfir Microsoft Dynamics 365 uppfærslur virkni Aðgerða í svæðinu Fjárhagsáætlunargerðar. Tilgangur þessarar kennslu er að sýna dæmu um fljóta uppsetningu fyrir kerfi fjárhagsáætlunargerðar og sýna hvernig fjárhagsáætlunargerð má sinna með því að nota þessa uppsetningu.  Þessi lab mun áhersla sérstaklega á eftirfarandi viðskiptaferli eða verk--Stofna stigveldisskipan fyrir áætlanagerð og öryggisskilgreining notanda - Skilgreining aðstæður fjárhagsáætlunargerðar fjárhagsáætlunardálka, útlit og sniðmát fyrir Excel - Stofnun og virkjun fjárhagsáætlunar fjárhagsáætlunargerðar ferli - að Stofna skjal fjárhagsáætlunargerðar eftir pulling í rauntölur úr fjárhagi - með því að Nota úthlutanir til að leiðrétta gögn skjals fjárhagsáætlunar - Breyta skjali gögn fjárhagsáætlunar í Excel 

<a name="prerequisites"></a>Forkröfur 
------------------

Þetta kennsluefni fyrir þarf að fá aðgang að Dynamics 365 fyrir það umhverfi sem Aðgerðir með sýnigögn Contoso og úthlutað á sem kerfisstjóri á tilvikinu. Ekki nota í Einka vafra fyrir lab - útskráning úr öðrum lykli í vafranum ef þörf krefur og skrá inn með Dynamics 365 notendaheimildir lénsstjóra Aðgerðir. Við innskráningu í Dynamics 365 fyrir Aðgerð er **VERÐUR** athuga "Halda mér innskráður" gátreitinn. Þetta stofnar varanlega vafraköku sem Excel-smáforritið þarf. Ef að skrá sig inn á Dynamics 365 fyrir Aðgerðirnar með því að nota vafra en IE, svo er verður beðinn um að skrá sig inn í Excel-Forritið. Þegar smellt er á "Skrá inn" í Excel-smáforritinu opnast smelligluggi IE og þegar skráð er inn **VERÐUR**að haka í  "Halda mér undirrituðum" gátreitinn. Ef ekkert gerist þegar smellt er á "Skrá inn" í Excel-smáforritið ætti að hreinsa lotur úr skyndiminni IE.

## <a name="scenario-overview"></a>**Scenario overview**
Julia vinnur sem stjórnandi fjármála í Contoso Skemmtana Kerfum í Þýskalandi (DEMF). Þegar fjárhagsárið FY2016 nálgast þarf hún að vinna í uppsetningu fjárhagsáætlunar fyrirtækisins fyrir komandi ár. Undirbúningur fjárhagsáætlunarinnar lítur svona út:

1.  Julia notar rauntölur fyrra árs sem upphafspunkt til að stofna fjárhagsáætlun.
2.  Byggt á rauntölum fyrra árs stofnar hún mat fyrir 12 mánuði komandi árs
3.  Julia endurskoðar fjárhagsáætlunina með Framkvæmdastjóra. Eftir það gerir hún nauðsynlegar leiðréttingar fyrir fjárhagsáætlunargerð og gengur frá undirbúningi fjárhagsáætlunar.

Skilgreining skema fyrir aðstæður fjárhagsáætlunargerðar eitthvað sem hér segir:

![Screenshot1](./media/screenshot1-300x152.png)

Julia notar eftirfarandi Excel sniðmát til að útbúa fjárhagsáætlun:

[![](./media/screenshot2-1024x352.png)](./media/screenshot2.png)

<a name="exercise-1-configuration"></a>Æfing 1: Uppsetning
=========================

## <a name="task-1-create-organizational-hierarchy"></a>**Verk 1: Stofna stigveldisskipan**
Þar sem allt fjárhagsáætlunarferlið gerist í fjármáladeild, þarf Julia að stofna mjög einfalda stigveldisskipan – samanstendur af aðeins fjármáladeild. 1.1. Fara í stigveldi Fyrirtækis (fyrirtækisstjórnun &gt;Fyrirtæki &gt;stigveldum fyrirtækja) og smella á hnappinn Nýtt

![Screenshot3](./media/screenshot3.png) 

1.2. Færið inn heiti fyrir stigveldi fyrirtækis og smellið á hnappinn Úthluta málefni

[![Screenshot4](./media/screenshot4.png)](./media/screenshot4.png) 

1.3. Veljið málefni Fjárhagsáætlunargerðar, smellið á hnappinn Bæta og úthluta nýstofnuð stigveldisskipan: 

[![Screenshot5](./media/screenshot5.png)](./media/screenshot5.png)

1.4. Endurtakið ofantalin skref fyrir málefni öryggisskipulags. Loka skjámyndinni þegar þessu er lokið.

[![Screenshot6](./media/screenshot6.png)](./media/screenshot6.png)

1.5. Smellið á hnappinn Skoða í skjámyndinni Stigveldi Fyrirtækis. Smella á Breyta í hönnuði Stigveldis og búa til þrepun með því að smella á hnappinn Setja Inn.

[![Screenshot7](./media/screenshot7.png)](./media/screenshot7.png) 

1.6. Veljið fjármáladeild fyrir stigveldi fjárhagsáætlunar. 

[![Screenshot8](./media/screenshot8.png)](./media/screenshot8.png)

1.7. Þegar því er lokið, smellið á hnappinn Birta og Loka. Velja 1/1/2015 sem gildisdagsetning fyrir stigveldi birtingu.

[![Screenshot9](./media/screenshot9.png)](./media/screenshot9.png)

## <a name="task-2-configure-user-security"></a>Verkefni 2: Setja upp Öryggi notanda
Fjárhagsáætlunargerð notar sérstakar öryggisreglur til að skilgreina aðgang að gögnum fjárhagsáætlunargerðar. Julia þarf að veita sjálfri sér aðgang að fjárhagsáætlunargerðinni. 2.1. Skipta DEMF lögaðila samhengi: [![Screenshot10](./media/screenshot10.png)](./media/screenshot10.png) 2.2. Fara í Fjárhagsáætlun &gt;Uppsetningu &gt;fjárhagsáætlunargerð &gt;skilgreiningu fjárhagsáætlunargerðar. Færibreytur flipanum, gildi stillt á Öryggi líkan Byggt á öryggisfyrirtækjum [![Screenshot11](./media/screenshot11.png)](./media/screenshot11.png) 2.3. Fara í kerfisstjórnun &gt;Notendur &gt;Notendur. Veita stjórnanda (Julia Funderburk) hlutverk fjárhagsáætlunarstjóra. [![Screenshot12](./media/screenshot12.png)](./media/screenshot12.png) 2.4. Tiltekt í hlutverki notanda og smellið á Úthluta fyrirtæki [![Screenshot13](./media/screenshot13.png)](./media/screenshot13.png)2,5. Veljið "Veita skilgreindum fyrirtækjum aðgengi". Veljið Stigveldi fyrirtækis sem var búið til í fyrsta þrepinu. Velja hnút Fjármál og smellið á Styrk með undirgreinum hnappinn ***Important!*** *– Gera tryggja að í samhengi lögaðila DEMF þegar þessu verki, eins og öryggi Skipulags er notað fyrir hvern lögaðila*[![Screenshot14](./media/screenshot14.png)](./media/screenshot14.png)

## <a name="task-3-create-scenarios"></a>Verkefni 3: Stofna atburðarás
3.1. Fara í Fjárhagsáætlun&gt;Uppsetningu &gt;fjárhagsáætlunargerð &gt;skilgreiningu fjárhagsáætlunargerðar. Á síðunni Atburðarás: Takið eftir aðstæðum sem verða notaðar síðar í þessu ferli: Raunupphæðir Fyrra árs og Fjárhagáætlun. *Athugið: Hægt að stofna nýja atburðarás fyrir þessa æfingu og nota í staðinn.* [![Screenshot15](./media/screenshot15.png)](./media/screenshot15.png)*Athugasemd: Julia er ekki með formleg samþykktarferli fyrir undirbúning fjárhagsáætlunar, Verkflæði, Stig mælt hleypur og verkflæðisstiga uppsetningu í þessari lab og nota fyrirliggjandi uppsetningu fyrir Sjálfvirka – samþykkja verkflæði. Sjá viðauka fyrir þessa skilgreiningu fyrir verkflæði.*

## <a name="task-4-create-budget-plan-columns"></a>4. verkefni: Stofna fjárhagsáætlunardálka
Dálkar fyrir Fjárhagsáætlunargerð er annað hvort gjaldmiðilsdálkar eða magndálkar sem er hægt að nota í skjalinu fyrir fjárhagsáætlun.u Í dæminu okkar er nauðsynlegt að stofna dálk fyrir rauntölur fyrra árs og 12 dálka sem hver stendur fyrir einn mánuð fjárhagsársins. Hægt er að stofna dálka annaðhvort með því að smella einfaldlega á hnappinn Bæta við og fylla inn í gildi, eða með aðstoð gagnaeiningar. Í þessari æfingu munum við nota gagnaeiningu til að fylla inn i gildin. 4.1. Í Fjárhagsáætlun&gt;Uppsetningu &gt;fjárhagsáætlunargerð &gt;Fjárhagsáætlunar fjárhagsáætlunargerðar skilgreiningu opna Dálka síðu. Smellið á hnappinn Office í efstu hægri horninu í skjámyndinni og velja Dálkum (unfiltered) [![Screenshot16](./media/screenshot16.png)](./media/screenshot16.png) 4.2. Kerfið mun opna Excel-vinnubókina sem nota á til að fylla út gildi. Ef beðið er um, smellið á að Gera Breytingar og Traust forritið [![Screenshot18](./media/screenshot18.png)](./media/screenshot18.png)[![Screenshot17](./media/screenshot17.png)](./media/screenshot17.png) 4.3. Við höfum þarf frekari dálkar til að fylla á gildi. Smellt er á hægri hlið rúðunni til að bæta dálkum við hnitanetið Hönnun: [![Screenshot19](./media/screenshot19.png)](./media/screenshot19.png) 4.4. Smellið á hnappinn minnstu pencil við PlanColumns til að sjá tiltækar dálkum við hnitanetið [![Screenshot20](./media/screenshot20.png)](./media/screenshot20.png) 4.5. Tvísmellið á hverja tiltæk svæði til að bæta þeim við Valið svæði og smellið á Uppfæra [![Screenshot21](./media/screenshot21.png)](./media/screenshot21.png) 4.6. Bætið við öllum dálkum sem þarf að stofna í Excel-töflu. Nota aðgerð AutoFill í Excel til að bæta línum á fljótlegan hátt. Gangið úr skugga um að í línum er bætt við sem hluta af töflu (þegar lóðrétt fletta, ætti að vera unnt að sjá haus dálks on the top of hnitanetinu) [![Screenshot22](./media/screenshot22.png)](./media/screenshot22.png) 4.7. Snúa aftur í Dynamics 365 aðgerða og endurnýja síðuna. Birta gildi munu birtast í Dynamics 365 aðgerða. [![Screenshot23](./media/screenshot23.png)](./media/screenshot23.png)

## <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>Verkefni 5: Búa til útlit og sniðmát fjárhagsáætlunarskjals
Útlit ákvarðar hvernig hnitanet fyrir fjárhagsáætlunargerðarskjalið lítur út þegar notandi opnar skjal fjárhagsáætlunargerðar. Einnig er hægt að skipta um útlit fyrir skjal fjárhagsáætlunargerðar til að sjá sömu gögn frá mismunandi sjónarhornum. Núna, þegar hún hefur skilgreint dálka til notkunar með fjárhagsáætlunargerðarskjali, þarf Julia að búa til skjal yfir útlit fjárhagsáætlunar, sem myndi líta svipað út og Excel taflan sem hún notar til að stofna fjárhagsáætlunargögn (sjá hlutann Yfirlit yfir aðstæður í þessari æfingu) 5.1. Í Fjárhagsáætlun&gt;Uppsetningu &gt;fjárhagsáætlunargerð &gt;Fjárhagsáætlunar fjárhagsáætlunargerðar skilgreiningu opna Útlit síðu. Búa til nýtt útlit fyrir færslu fyrir mánaðarlega fjárhagsáætlun:

-   Taka MA + BU víddasamstæðu til að innifela aðalreikninga og viðskiptaeiningar í útlitinu.
-   Skrá alla fjárhagsáætlunardálka sem voru stofnaðir í fyrra skrefi í hlutanum Einingar. Gera allt nema rauntölur fyrra árs breytanlegt.
-   Smellið á hnappinn Lýsingar til að velja hvaða fjárhagsvíddir skuli birta Lýsingar í hnitanetinu.

[![Screenshot24](./media/screenshot24.png)](./media/screenshot24.png) Miðað við fjárhagsáætlun útlit skilgreining mælt hægt er að stofna Excel sniðmátið sem nota á sem er önnur leið til að breyta fjárhagsáætlunargögn áætlunar. Eins og Excel sniðmát þarf að passa við skilgreiningu á uppsetningu fjárhagsáætlunar, er ekki hægt að breyta fjárhagsáætlunaruppsetningu eftir myndun Excel sniðmáts, því ætti að gera þetta verkefni eftir að allir þættir í uppsetningu hafa verið skilgreindir. 5.2. Útlit stofnuð í á 5.1. Skref er smellt á hnappinn Sniðmáts &gt;Mynda. Staðfesta viðvörunarboðin. Skoða sniðmát, smella á Sniðmáti &gt;Skoða. *Athugasemd: Gangið úr skugga um að velja "Vista sem" og veljið stað þar sem geyma á sniðmát til að breyta henni. Ef notandi velur "Opin" í svarglugganum án þess að vista gert til að skrá breytingarnar verða ekki varðveitt þegar skráin er lokað.* [![Screenshot25](./media/screenshot25.png)](./media/screenshot25.png) 5.3. &lt;Valfrjálst skref&gt; Breyta Excel sniðmát til að leita að fleiri notanda stutt – bæta samtals formúlur fyrirsagnasvæði, snið o.s.frv. Vista breytingar og senda skrá fjárhagsáætlunarútlit með því að smella Útlit &gt;Senda [![Screenshot26](./media/screenshot26.png)](./media/screenshot26.png)

## <a name="task-6-create-a-budget-planning-process"></a>Verkefni 6: Stofna ferli fjárhagsáætlunargerðar
Julia þarf að stofna og virkja nýja fjárhagsáætlunargerð með því að sameina alla uppsetninguna hér að ofan til að byrja að færa inn fjárhagsáætlanir. Ferli fjárhagsáætlunargerðar skilgreinir hvaða fyrirtækisfjárhagsáætlanir, verkflæði, útlit og sniðmát verður notað til að stofna fjárhagsáætlunargerð. 6.1. Fara í Fjárhagsáætlun &gt;Uppsetningu &gt;fjárhagsáætlunargerð &gt;Fjárhagsáætlunar ferli fjárhagsáætlunargerðar og stofna nýja færslu.

-   Ferli fjárhagsáætlunargerðar - DEMF fjárhagsáætlun FY2016
-   Fjárhagsáætlunarhringrás - FY2016
-   Höfuðbók - DEMF
-   Sjálfgefið reikningsskipulag – Framleiðsla P & L
-   Stigveldi fyrirtækis – velja stigveldi sem er stofnað í upphafi verkefnisins
-   Verkflæði fjárhagsáætlunargerðar – úthluta Sjálfvirkt – Samþykkja verkflæði fyrir fjármáladeild
-   Varðandi stigsreglur og sniðmát fjárhagsáætlunargerðar,  fyrir hvert verkflæði Fjárhagsáætlunargerðarstigs skal ákveða hvort aðgerðin Bæta línum við og Breyta línum er leyfð, og hvaða sjálfgefna snið á að nota

*Athugið: Hægt að stofna viðbótar skjalaútlit og úthluta þeim að vera tiltæk í verkflæðisstig fjárhagsáætlunargerðar með því að smella á hnappinn Önnur útlit.* [![Screenshot27](./media/screenshot27.png)](./media/screenshot27.png) 6.2. Veljið Aðgerðir &gt;Gera til að virkja þetta verkflæði fjárhagsáætlunargerðar [![Screenshot28](./media/screenshot28.png)](./media/screenshot28.png)

<a name="exercise-2-process-simulation"></a>Æfing 2: Eftirlíking af ferli
==============================

## <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>Verkefni 7: Mynda upphafsgögn fyrir fjárhagsáætlunargerð úr Almennri höfuðbók
7.1. Fara í Fjárhagsáætlun &gt;Reglubundið &gt;Mynda fjárhagsáætlun úr fjárhag. Fylla út reglubundnar færibreytur og smellið á hnappinn Mynda. [![Screenshot29](./media/screenshot29.png)](./media/screenshot29.png) 7.2. Fara í Fjárhagsáætlun &gt;fjárhagsáætlunargerðir til að finna stofnaði Mynda ferli fjárhagsáætlunargerðar. [![Screenshot30](./media/screenshot30.png)](./media/screenshot30.png) 7.3. Opna upplýsingar skjals með því að smella á tengilinn Skjalnúmer. Fjárhagsáætlunargerð birtist eins og skilgreint í uppsetningu stofnaðir á meðan þessi lab [![Screenshot31](./media/screenshot31.png)](./media/screenshot31.png)

## <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>Verkefni 8: Stofna fjárhagsáætlun fyrir núverandi ár byggt á rauntölum fyrra árs.
Hægt er að nota úthlutunaraðferðir í fjárhagsáætlunargerð til að auðveldlega afrita upplýsingar um fjárhagsáætlanir úr einum aðstæðum í aðrar / dreifa þeim yfir mörg tímabil / úthluta á víddir. Við notum úthlutanir til að stofna fjárhagsáætlun fyrir núverandi ár frá rauntölum fyrra árs. 8.1. Taka allar línur á hnitanetinu skjal fjárhagsáætlunar og smellið á hnappinn úthluta fjárhagsáætlun [![Screenshot32](./media/screenshot32.png)](./media/screenshot32.png) 8.2. Veljið úthlutunaraðferð tímabilslykil, aðstæður Uppruna og endastaðar og smellið á Úthlutun 

[![Screenshot33](./media/screenshot33.png)](./media/screenshot33.png)

Raunupphæðir fyrra ár afritaðir áætlunar ári gildandi og úthluta þeim á mörg tímabil með því að nota tímabilslykilinn kúrfan Vsk. 

[![Screenshot34](./media/screenshot34.png)](./media/screenshot34.png)

## <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>Verkefni 9: Aðlaga fjárhagsáætlunargerðarskjalið með því að nota Excel og ljúka við skjalið
9.1. Smellið á Hnappinn vinnublað til að skjalið innihaldi opna í Excel

[![Screenshot35](./media/screenshot35.png)](./media/screenshot35.png)

9.2. Þegar Excel-vinnubók opnast skal leiðrétta númer í fjárhagsáætlunargerðarskjali og smellið á hnappinn Birta.

[![Screenshot36](./media/screenshot36.png)](./media/screenshot36.png)

9.3. Skila skjal fjárhagsáætlunargerðar í Dynamics 365 fyrir Aðgerðir. Smellt er á Verkflæði &gt;Senda til að samþykkja Sjálfvirkrar skjalsins

[![Screenshot37](./media/screenshot37.png)](./media/screenshot37.png) 

Þegar verkflæði er lokið breytist stig skjala fjárhagsáætlunargerðar í Samþykkt. [![Screenshot38](./media/screenshot38.png)](./media/screenshot38.png)

<a name="appendix"></a>Viðauki
========

### <a name="auto-approve-workflow-configuration"></a>Samþykkja sjálfvirkt uppsetningu verkflæðis.

A. Fjárhagsáætlun &gt;Uppsetningu &gt;fjárhagsáætlunargerð &gt;nýtt verkflæði með því að nota sniðmát verkflæði fjárhagsáætlunargerðar til að Stofna verkflæði fyrir Fjárhagsáætlun:

[![Screenshot39](./media/screenshot39.png)](./media/screenshot39.png)

Þetta verkflæði inniheldur aðeins eitt verk – fjárhagsáætlunargerð stigstilfærslu 

[![Screenshot40](./media/screenshot40.png)](./media/screenshot40.png) 

Vista og virkja verkflæðið. 

B. Fara í Fjárhagsáætlun &gt;Uppsetningu &gt;fjárhagsáætlunargerð &gt;skilgreiningu fjárhagsáætlunargerðar. Stofna 2 stig – Upphafleg og Sent í Stiganna flipa 

[![Screenshot41](./media/screenshot41.png)](./media/screenshot41.png)

C. Fara í Fjárhagsáætlun &gt;Uppsetningu &gt;fjárhagsáætlunargerð &gt;skilgreiningu fjárhagsáætlunargerðar. Í flipanum Verkflæðisstiga Tengja verkflæðið Sjálfvirk – samþykkja stofnaður í skrefi með í stiganna Upphafleg og Sent 

[![Screenshot42](./media/screenshot42.png)](./media/screenshot42.png)  


