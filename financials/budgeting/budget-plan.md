---
title: "Fjárhagsáætlunargerð"
description: "Markmiðið þessarar kennslu er að veita leiðsögn í Microsoft Dynamics 365 for Operations fyrir skoðun á uppfærslum á virkni Dynamics á svæðum fjárhagsáætlunargerðar. Tilgangur þessarar kennslu er að sýna dæmu um fljóta uppsetningu fyrir kerfi fjárhagsáætlunargerðar og sýna hvernig fjárhagsáætlunargerð má sinna með því að nota þessa uppsetningu.  Þessi kennsla mun leggja sérstaka áhersla á eftirfarandi viðskiptaferli eða verk -    - að Stofna stigveldisskipan fyrir áætlanagerð og öryggisskilgreining notanda   - Skilgreina aðstæður fjárhagsáætlunargerðar, fjárhagsáætlunardálka, útlit og sniðmát fyrir Excel   - Stofna og virkja ferli fjárhagsáætlunargerðar   - Stofna fjárhagsáætlunarskjal með því að sækja rauntölur úr fjárhag   - Nota úthlutanir til að stilla gögn fjárhagsáætlunarskjals   - Breyta gögnum fjárhagsáætlunarskjals í Excel"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: dbe2b386de9e88af354015705e1444987a3f7e82
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="budget-planning"></a>Fjárhagsáætlunargerð

[!include[banner](../includes/banner.md)]


Markmiðið þessarar kennslu er að veita leiðsögn í Microsoft Dynamics 365 for Operations fyrir skoðun á uppfærslum á virkni Dynamics á svæðum fjárhagsáætlunargerðar. Tilgangur þessarar kennslu er að sýna dæmu um fljóta uppsetningu fyrir kerfi fjárhagsáætlunargerðar og sýna hvernig fjárhagsáætlunargerð má sinna með því að nota þessa uppsetningu.  Þessi kennsla mun leggja sérstaka áhersla á eftirfarandi viðskiptaferli eða verk -    - að Stofna stigveldisskipan fyrir áætlanagerð og öryggisskilgreining notanda   - Skilgreina aðstæður fjárhagsáætlunargerðar, fjárhagsáætlunardálka, útlit og sniðmát fyrir Excel   - Stofna og virkja ferli fjárhagsáætlunargerðar   - Stofna fjárhagsáætlunarskjal með því að sækja rauntölur úr fjárhag   - Nota úthlutanir til að stilla gögn fjárhagsáætlunarskjals   - Breyta gögnum fjárhagsáætlunarskjals í Excel 

<a name="prerequisites"></a>Forkröfur 
------------------

Fyrir þetta kennsluefni þarf að fá aðgang að 365 fyrir Operations með sýnigögnum Contoso og vera úthlutað sem stjórnanda fyrir tilvikið. Ekki nota í einkavafra, - það þarf að skrá sig út úr hvaða reikningi sem er í vafranum ef þörf krefur og skrá svo inn með Dynamics 365 for Operations notendaheimildum kerfisstjóra. Þegar skráð er inn í Microsoft Dynamics 365 for Operations **VERÐUR** að haka í "Halda mér innskráðum" gátreitinn. Þetta stofnar varanlega vafraköku sem Excel-smáforritið þarf. Ef innskráning í Microsoft Dynamics 365 for Operations er gerð gegnum annan vafra en IE, verður þú beðinn um að skrá inn í gegnum Excel-smáforritið. Þegar smellt er á "Skrá inn" í Excel-smáforritinu opnast smelligluggi IE og þegar skráð er inn **VERÐUR**að haka í  "Halda mér undirrituðum" gátreitinn. Ef ekkert gerist þegar smellt er á "Skrá inn" í Excel-smáforritið ætti að hreinsa lotur úr skyndiminni IE.

## <a name="scenario-overview"></a>**Yfirlit yfir aðstæður**
Julia vinnur sem stjórnandi fjármála í Contoso Skemmtana Kerfum í Þýskalandi (DEMF). Þegar fjárhagsárið FY2016 nálgast þarf hún að vinna í uppsetningu fjárhagsáætlunar fyrirtækisins fyrir komandi ár. Undirbúningur fjárhagsáætlunarinnar lítur svona út:

1.  Julia notar rauntölur fyrra árs sem upphafspunkt til að stofna fjárhagsáætlun.
2.  Byggt á rauntölum fyrra árs stofnar hún mat fyrir 12 mánuði komandi árs
3.  Julia endurskoðar fjárhagsáætlunina með Framkvæmdastjóra. Eftir það gerir hún nauðsynlegar leiðréttingar fyrir fjárhagsáætlunargerð og gengur frá undirbúningi fjárhagsáætlunar.

Uppsetningarskema Fjárhagsáætlunargerðar fyrir aðstæðurnar lítur svona út:

![Skema skilgreiningar fjárhagsáætlunargerðar](./media/screenshot1-300x152.png)

Júlía notar eftirfarandi Excel-sniðmát til að undirbúa fjárhagsáætlun:

[![Excel-sniðmát](./media/screenshot2-1024x352.png)](./media/screenshot2.png)

<a name="exercise-1-configuration"></a>Æfing 1: Uppsetning
=========================

## <a name="task-1-create-organizational-hierarchy"></a>**Verkefni 1: Stofna stigveldi fyrirtækisins**
Þar sem allt fjárhagsáætlunarferlið gerist í fjármáladeild, þarf Julia að stofna mjög einfalda stigveldisskipan – samanstendur af aðeins fjármáladeild. 1.1. Fara í stigveldi Fyrirtækis (fyrirtækisstjórnun &gt; Fyrirtæki &gt; stigveldi fyrirtækja) og smella á hnappinn Nýtt

![Stigveldi fyrirtækis](./media/screenshot3.png) 

1.2. Færið inn heiti fyrir stigveldi fyrirtækis og smellið á hnappinn Úthluta málefni

[![Nafn](./media/screenshot4.png)](./media/screenshot4.png) 

1.3. Veljið tilgang Fjárhagsáætlunargerðar, smellið á hnappinn Bæta við og úthlutið nýstofnaðri stigveldisskipan: 

[![Úthluta málefni](./media/screenshot5.png)](./media/screenshot5.png)

1.4. Endurtakið ofantalin skref fyrir málefni öryggisskipulags. Loka skjámyndinni þegar þessu er lokið.

[![Öryggislykill](./media/screenshot6.png)](./media/screenshot6.png)

1.5. Smellið á hnappinn Skoða í skjámyndinni Stigveldi Fyrirtækis. Smella á Breyta í hönnuði Stigveldis og búa til þrepun með því að smella á hnappinn Setja Inn.

[![Setja inn](./media/screenshot7.png)](./media/screenshot7.png) 

1.6. Veljið fjármáladeild fyrir stigveldi fjárhagsáætlunar. 

[![Fjármál](./media/screenshot8.png)](./media/screenshot8.png)

1.7. Þegar því er lokið, smellið á hnappinn Birta og Loka. Velja 1/1/2015 sem gildisdagsetning fyrir stigveldi birtingu.

[![Gildisdagsetning](./media/screenshot9.png)](./media/screenshot9.png)

## <a name="task-2-configure-user-security"></a>Verkefni 2: Setja upp Öryggi notanda
Fjárhagsáætlunargerð notar sérstakar öryggisreglur til að skilgreina aðgang að gögnum fjárhagsáætlunargerðar. Julia þarf að veita sjálfri sér aðgang að fjárhagsáætlunargerðinni. 

2.1. Skipta yfir í DEMF-lögaðilasamhengi : 

[![DEMF](./media/screenshot10.png)](./media/screenshot10.png) 

2.2. Farið á Fjárhagsáætlun &gt; Uppsetning &gt; Fjárhagsáætlunargerð &gt; Skilgreining fjárhagsáætlunargerðar. Í flipanum Færibreytur skal stilla gildi fyrir öryggislíkan á Byggt á öryggisfyrirtækjum 

[![Færibreytur](./media/screenshot11.png)](./media/screenshot11.png) 

2.3. Farið í Kerfisstjórnun &gt; Notendur &gt; Notendur. Veita stjórnanda (Julia Funderburk) hlutverk fjárhagsáætlunarstjóra. 

[![Umsjón með fjárhagsáætlun](./media/screenshot12.png)](./media/screenshot12.png) 

2.4. Veljið hlutverk notanda og smellið á Úthluta fyrirtækjum 

[![Úthluta org](./media/screenshot13.png)](./media/screenshot13.png)

2.5. Veljið "Veita skilgreindum fyrirtækjum aðgengi". Veljið Stigveldi fyrirtækis sem var búið til í fyrsta þrepinu. Veljið fjárhagstengipunkt og smellið á Styrksjóður fyrir börn 

***Mikilvægt!*** *Gangið úr skugga um að vera í DEMF-lögaðilasamhengi þegar þetta er gert, þar sem fyrirtækisöryggi er notað fyrir hvern lögaðila* 

[![Heimila aðgang](./media/screenshot14.png)](./media/screenshot14.png)

## <a name="task-3-create-scenarios"></a>Verkefni 3: Stofna atburðarás
3.1. Farið á Fjárhagsáætlun &gt; Uppsetning &gt; Fjárhagsáætlunargerð &gt; Skilgreining fjárhagsáætlunargerðar. Á síðunni Atburðarás: Takið eftir aðstæðum sem verða notaðar síðar í þessu ferli: Raunupphæðir Fyrra árs og Fjárhagáætlun. 

*Athugið: Hægt að stofna nýja atburðarás fyrir þessa æfingu og nota í staðinn.* 

[![Nýjar aðstæður](./media/screenshot15.png)](./media/screenshot15.png) 

*Athugið: Þar sem Julia notar ekki formleg samþykktarferli fyrir undirbúning fjárhagsáætlunar, munum við hlaupa yfir uppsetningar Verkflæði, Stig og Verkflæðisstig í þessari æfingu og nota fyrirliggjandi uppsetningu fyrir Sjálfvirkt – samþykkja verkflæði. Sjá viðauka fyrir þessa skilgreiningu fyrir verkflæði.*

## <a name="task-4-create-budget-plan-columns"></a>4. verkefni: Stofna fjárhagsáætlunardálka
Dálkar fyrir Fjárhagsáætlunargerð er annað hvort gjaldmiðilsdálkar eða magndálkar sem er hægt að nota í skjalinu fyrir fjárhagsáætlun.u Í dæminu okkar er nauðsynlegt að stofna dálk fyrir rauntölur fyrra árs og 12 dálka sem hver stendur fyrir einn mánuð fjárhagsársins. Hægt er að stofna dálka annaðhvort með því að smella einfaldlega á hnappinn Bæta við og fylla inn í gildi, eða með aðstoð gagnaeiningar. Í þessari æfingu munum við nota gagnaeiningu til að fylla inn i gildin. 

4.1. Í Fjárhagsáætlun&gt;Uppsetningu &gt; Fjárhagsáætlunargerð &gt; Skilgreining fjárhagsáætlunargerðar opnarðu dálkasíðuna. Smellið á hnappinn Office í efra hægra horni í skjámyndinni og veljið Dálka (óafmarkaða) 

[![Ósíaðir dálkar](./media/screenshot16.png)](./media/screenshot16.png) 

4.2. Kerfið mun opna Excel-vinnubókina sem nota á til að fylla út gildi. Ef beðið er um það skal smella á Leyfa breytingar og Treysta þessu forriti 

[![Virkja breytingar](./media/screenshot18.png)](./media/screenshot18.png) 

[![Treysta þessu forrit](./media/screenshot17.png)](./media/screenshot17.png)

4.3. Við munum þurfa fleiri dálka til að fylla gildin inn í. Smellt er á hönnun hægra megin til að bæta dálkum við hnitanetið: 

[![Hönnun](./media/screenshot19.png)](./media/screenshot19.png) 

4.4. Smellið á litla blýantstáknið við PlanColumns til að sjá tiltæka dálka til að bæta við hnitanetið 

[![Breyta](./media/screenshot20.png)](./media/screenshot20.png) 

4.5. Tvísmelltu á hvert tiltækt svæði til að bæta þeim við Valið svæði og smellið á Uppfæra 

![Uppfærsla](./media/screenshot21.png)](./media/screenshot21.png) 

4.6. Bætið við öllum dálkum sem þarf að stofna í Excel-töflu. Nota aðgerð AutoFill í Excel til að bæta línum á fljótlegan hátt. Gangið úr skugga um að línum sé bætt við sem hluta af töflu (þegar flett er lóðrétt, ætti að vera unnt að sjá haus dálks efst á hnitanetinu) 

[![Sjálfvirk útfylling](./media/screenshot22.png)](./media/screenshot22.png) 

4.7. Farðu til baka í Dynamics 365 for Operations og endurræstu síðuna. Birt gildi munu birtast í Dynamics 365 for Operations. 

[![Endurhlaða](./media/screenshot23.png)](./media/screenshot23.png)

## <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>Verkefni 5: Búa til útlit og sniðmát fjárhagsáætlunarskjals
Útlit ákvarðar hvernig hnitanet fyrir fjárhagsáætlunargerðarskjalið lítur út þegar notandi opnar skjal fjárhagsáætlunargerðar. Einnig er hægt að skipta um útlit fyrir skjal fjárhagsáætlunargerðar til að sjá sömu gögn frá mismunandi sjónarhornum. Núna, þegar hún hefur skilgreint dálka til notkunar með fjárhagsáætlunargerðarskjali, þarf Julia að búa til skjal yfir útlit fjárhagsáætlunar, sem myndi líta svipað út og Excel taflan sem hún notar til að stofna fjárhagsáætlunargögn (sjá hlutann Yfirlit yfir aðstæður í þessari æfingu) 

5.1. Í Fjárhagsáætlun &gt; Uppsetningu &gt; Fjárhagsáætlunargerð &gt; Skilgreining fjárhagsáætlunargerðar opnarðu útlitssíðuna. Búa til nýtt útlit fyrir færslu fyrir mánaðarlega fjárhagsáætlun:

-   Taka MA + BU víddasamstæðu til að innifela aðalreikninga og viðskiptaeiningar í útlitinu.
-   Skrá alla fjárhagsáætlunardálka sem voru stofnaðir í fyrra skrefi í hlutanum Einingar. Gera allt nema rauntölur fyrra árs breytanlegt.
-   Smellið á hnappinn Lýsingar til að velja hvaða fjárhagsvíddir skuli birta Lýsingar í hnitanetinu.

[![Lýsingar](./media/screenshot24.png)](./media/screenshot24.png) 

Miðað við skilgreiningu á fjárhagsáætlunarútliti er hægt að stofna Excel sniðmátið sem nota á sem aðra leið til að breyta gögnum fjárhagsáætlunar. Eins og Excel sniðmát þarf að passa við skilgreiningu á uppsetningu fjárhagsáætlunar, er ekki hægt að breyta fjárhagsáætlunaruppsetningu eftir myndun Excel sniðmáts, því ætti að gera þetta verkefni eftir að allir þættir í uppsetningu hafa verið skilgreindir. 

5.2. Fyrir útlit sem var stofnað í skrefi 5.1. skref er smellt á hnappinn Sniðmát &gt; Mynda. Staðfesta viðvörunarboðin. Til að skoða sniðmátið, smellið á Sniðmát &gt; Skoða. 

*Athugasemd: Gangið úr skugga um að velja "Vista sem" og veljið stað þar sem geyma á sniðmát til að breyta henni. Ef notandi velur "Opna" í svarglugganum án þess að vista, verða breytingarnar á skránni ekki vistaðar þegar skránni verður lokað.* 
[![Sniðmátsyfirlit](./media/screenshot25.png)](./media/screenshot25.png) 

5.3. &lt; Valfrjálst skref&gt; Breyta Excel-sniðmáti til að það líti notendavænna út – bæta við formúlum, fyrirsagnasvæðum, sniðum o.s.frv. Vistið breytingarnar og senda skrá yfir á fjárhagsáætlunarútlit með því að smella á Útlit &gt; Senda [![Senda](./media/screenshot26.png)](./media/screenshot26.png)

## <a name="task-6-create-a-budget-planning-process"></a>Verkefni 6: Stofna ferli fjárhagsáætlunargerðar
Julia þarf að stofna og virkja nýja fjárhagsáætlunargerð með því að sameina alla uppsetninguna hér að ofan til að byrja að færa inn fjárhagsáætlanir. Ferli fjárhagsáætlunargerðar skilgreinir hvaða fyrirtækisfjárhagsáætlanir, verkflæði, útlit og sniðmát verður notað til að stofna fjárhagsáætlunargerð. 

6.1. Fara í Fjárhagsáætlun &gt; Uppsetning &gt; Fjárhagsáætlunargerð &gt; Ferli fjárhagsáætlunargerðar og stofna nýja færslu.

-   Ferli fjárhagsáætlunargerðar - DEMF fjárhagsáætlun FY2016
-   Fjárhagsáætlunarhringrás - FY2016
-   Höfuðbók - DEMF
-   Sjálfgefið reikningsskipulag – Framleiðsla P & L
-   Stigveldi fyrirtækis – velja stigveldi sem er stofnað í upphafi verkefnisins
-   Verkflæði fjárhagsáætlunargerðar – úthluta Sjálfvirkt – Samþykkja verkflæði fyrir fjármáladeild
-   Varðandi stigsreglur og sniðmát fjárhagsáætlunargerðar,  fyrir hvert verkflæði Fjárhagsáætlunargerðarstigs skal ákveða hvort aðgerðin Bæta línum við og Breyta línum er leyfð, og hvaða sjálfgefna snið á að nota

*Athugið: Hægt að stofna viðbótar skjalaútlit og úthluta þeim að vera tiltæk í verkflæðisstig fjárhagsáætlunargerðar með því að smella á hnappinn Önnur útlit.* 

[![Annað útlit](./media/screenshot27.png)](./media/screenshot27.png) 

6.2. Veljið Aðgerðir &gt; Virkja til að virkja þetta verkflæði fjárhagsáætlunargerðar 

[![Virkja](./media/screenshot28.png)](./media/screenshot28.png)

<a name="exercise-2-process-simulation"></a>Æfing 2: Eftirlíking af ferli
==============================

## <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>Verkefni 7: Mynda upphafsgögn fyrir fjárhagsáætlunargerð úr Almennri höfuðbók
7.1. Fara í Fjárhagsáætlun &gt; Reglubundið &gt; Mynda fjárhagsáætlun úr Almennri höfuðbók. Fylla út reglubundnar færibreytur og smellið á hnappinn Mynda. 

[![Mynda](./media/screenshot29.png)](./media/screenshot29.png) 

7.2. Fara í Fjárhagsáætlun &gt; Fjárhagsáætlunargerðir til að finna fjárhagsáætlunargerð útbúna með Myndunarferlinu. 

[![Fjárhagsáætlunargerð](./media/screenshot30.png)](./media/screenshot30.png) 

7.3. Opna upplýsingar skjals með því að smella á tengilinn Skjalnúmer. Fjárhagsáætlunargerð birtist eins og skilgreint er í uppsetningu sem stofnuð var í þessari æfingu 

[![Fjárhagsáætlunarskjár](./media/screenshot31.png)](./media/screenshot31.png)

## <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>Verkefni 8: Stofna fjárhagsáætlun fyrir núverandi ár byggt á rauntölum fyrra árs.
Hægt er að nota úthlutunaraðferðir í fjárhagsáætlunargerð til að auðveldlega afrita upplýsingar um fjárhagsáætlanir úr einum aðstæðum í aðrar / dreifa þeim yfir mörg tímabil / úthluta á víddir. Við notum úthlutanir til að stofna fjárhagsáætlun fyrir núverandi ár frá rauntölum fyrra árs. 

8.1. Veljið allar línur á hnitanetinu á fjárhagsáætlunarskjalinu og smellið á hnappinn úthluta fjárhagsáætlun 

[![Allar línur](./media/screenshot32.png)](./media/screenshot32.png) 

8.2. Veljið úthlutunaraðferð, tímabilslykil, aðstæður Uppruna og endastaðar og smellið á Úthlutun 

[![Úthluta](./media/screenshot33.png)](./media/screenshot33.png)

Raunverulegar upphæðir fyrra árs verða afrituð yfir á áætlun núverandi árs og úthluta þeim yfir tímabil með því að nota tímabilslykilinn Sölukúrfa. 

[![Sölukúrfur](./media/screenshot34.png)](./media/screenshot34.png)

## <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>Verkefni 9: Aðlaga fjárhagsáætlunargerðarskjalið með því að nota Excel og ljúka við skjalið
9.1. Smellið á hnappinn Vinnublað til að opna innihald skjalsins í Excel

[![Excel](./media/screenshot35.png)](./media/screenshot35.png)

9.2. Þegar Excel-vinnubók opnast skal leiðrétta númer í fjárhagsáætlunargerðarskjali og smellið á hnappinn Birta.

[![Gefa út](./media/screenshot36.png)](./media/screenshot36.png)

9.3. Farið til baka í fjárhagsáætlunargerðarskjal í Dynamics 365 for Operations. Smellt er á Verkflæði &gt; Senda inn til samþykkja sjálfvirkt fylgiskjalið

[![Sjálfvirk samþykkt](./media/screenshot37.png)](./media/screenshot37.png) 

Þegar verkflæði er lokið breytist stig fjárhagsáætlunargerðarskjala í Samþykkt. [![Samþykkt](./media/screenshot38.png)](./media/screenshot38.png)

<a name="appendix"></a>Viðauki
========

### <a name="auto-approve-workflow-configuration"></a>Samþykkja sjálfvirkt uppsetningu verkflæðis.

A. Fjárhagsáætlun &gt; Uppsetning &gt; Fjárhagsáætlunargerð &gt; Verkflæði fjárhagsáætlunargerðar Búið til nýtt verkflæði með því að nota sniðmátið Verkflæði fyrir fjárhagsáætlunargerð:

[![Stofna nýtt verkflæði](./media/screenshot39.png)](./media/screenshot39.png)

Þetta verkflæði mun aðeins innihalda eitt verkefni - Fjárhagsáætlunargerð stigstilfærslu 

[![Fjárhagsáætlunargerð stigstilfærslu](./media/screenshot40.png)](./media/screenshot40.png) 

Vista og virkja verkflæðið. 

B. Farið á Fjárhagsáætlun &gt; Uppsetning &gt; Fjárhagsáætlunargerð &gt; Skilgreining fjárhagsáætlunargerðar. Í flipanum Stig skal stofna 2 stig – Upphafleg og Sent 

[![Fyrstu og sendar](./media/screenshot41.png)](./media/screenshot41.png)

C. Farið á Fjárhagsáætlun &gt; Uppsetning &gt; Fjárhagsáætlunargerð &gt; Skilgreining fjárhagsáætlunargerðar. Í flipanum Verkflæðisstig skal tengja verkflæðið Samþykkja sjálfvirkt sem var stofnað í þrepi A með stigunum Upphaflegt og Sent 

[![Fjárhagsáætlun og fjárhagsáætlunargerð](./media/screenshot42.png)](./media/screenshot42.png)  




