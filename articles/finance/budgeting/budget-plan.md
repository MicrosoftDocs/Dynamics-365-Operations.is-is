---
title: Fjárhagsáætlunargerð
description: Markmið þessarar kennslu er að veita leiðsögn í fyrir skoðun á uppfærslum á virkni Microsoft Dynamics 365 Finance á svæðum fjárhagsáætlunargerðar. Tilgangur þessarar kennslu er að sýna dæmu um fljóta uppsetningu fyrir kerfi fjárhagsáætlunargerðar og sýna hvernig fjárhagsáætlunargerð má sinna með því að nota þessa uppsetningu.
author: ShylaThompson
ms.date: 06/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f6223cce4a960d3fa3db1f3a17b324201085ea04
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822228"
---
# <a name="budget-planning"></a>Fjárhagsáætlunargerð

[!include [banner](../includes/banner.md)]

Markmið þessarar kennslu er að veita leiðsögn í fyrir skoðun á uppfærslum á virkni Microsoft Dynamics 365 Finance á svæðum fjárhagsáætlunargerðar. Tilgangur þessarar kennslu er að sýna dæmu um fljóta uppsetningu fyrir kerfi fjárhagsáætlunargerðar og sýna hvernig fjárhagsáætlunargerð má sinna með því að nota þessa uppsetningu.  Þessi æfing mun leggja sérstaka áherslu á eftirfarandi viðskiptaferla eða verk:
- Búa til stigveldi fyrirtækis fyrir fjárhagsáætlun og grunnstilla öryggi notenda
- Skilgreina aðstæður fjárhagsáætlunargerðar, fjárhagsáætlunarsúlur, útlit og Excel sniðmát
- Búa til og virkja ferli fjárhagsáætlunargerðar
- Búa til fjárhagsáætlunarskjal með því að draga í rauntölur frá fjárhag
- Nota úthlutanir til að lagfæra gögn fjárhagsáætlunarskjals
- Breyta gögnum fjárhagsáætlunarskjals í Excel 

<a name="prerequisites"></a>Forkröfur 
------------------

Fyrir þetta kennsluefni þarf að fá aðgang að umhverfi Microsoft Dynamics 365 Finance með sýnigögnum Contoso og fá stjórnendaréttindi fyrir þetta tilvik. Ekki nota í einkavafra, - það þarf að skrá sig út úr hvaða reikningi sem er í vafranum ef þörf krefur og skrá svo inn með notendaheimildum kerfisstjóra. Við innskráningu **VERÐUR** að haka í gátreitinn „Halda mér innskráðum“. Þetta stofnar varanlega vafraköku sem Excel-smáforritið þarf. Ef innskráning í forrit er gerð í gegnum annan vafra en IE kemur upp kvaðning um að skrá inn í Excel-smáforritið. Þegar smellt er á „Skrá inn“ í Excel-smáforritinu opnast smelligluggi IE og þegar skráð er inn **VERÐUR** að haka í gátreitinn „Halda mér innskráðri/-um“. Ef ekkert gerist þegar smellt er á "Skrá inn" í Excel-smáforritið ætti að hreinsa lotur úr skyndiminni IE.

## <a name="scenario-overview"></a>**Yfirlit yfir aðstæður**
Julia vinnur sem stjórnandi fjármála í Contoso Entertainment Systems í Þýskalandi (DEMF). Þegar fjárhagsárið FY2016 nálgast þarf hún að vinna í uppsetningu fjárhagsáætlunar fyrirtækisins fyrir komandi ár. Undirbúningur fjárhagsáætlunarinnar lítur svona út:

1.  Julia notar rauntölur fyrra árs sem upphafspunkt til að stofna fjárhagsáætlun.
2.  Byggt á rauntölum fyrra árs stofnar hún mat fyrir 12 mánuði komandi árs
3.  Julia endurskoðar fjárhagsáætlunina með framkvæmdastjóranum. Eftir það gerir hún nauðsynlegar leiðréttingar fyrir fjárhagsáætlunargerð og gengur frá undirbúningi fjárhagsáætlunar.

Uppsetningarskema Fjárhagsáætlunargerðar fyrir aðstæðurnar lítur svona út:

![Skemaskilgreiningar fjárhagsáætlunargerðar](./media/screenshot1-300x152.png)

Júlía notar eftirfarandi Excel-sniðmát til að undirbúa fjárhagsáætlun:

[![Excel-sniðmát](./media/screenshot2-1024x352.png)](./media/screenshot2.png)

## <a name="exercise-1-configuration"></a>Æfing 1: Uppsetning

### <a name="task-1-create-organizational-hierarchy"></a>**Verkefni 1: Stofna stigveldi fyrirtækisins**
Þar sem allt fjárhagsáætlunarferlið gerist í fjármáladeild, þarf Julia að stofna mjög einfalda stigveldisskipan – samanstendur af aðeins fjármáladeild. 

1.1. Farðu í stigveldi fyrirtækis (Fyrirtækisstjórnun &gt; Fyrirtæki &gt; Stigveldi fyrirtækja) og smelltu á hnappinn Nýtt.

![Stigveldi fyrirtækis](./media/screenshot3.png) 

1.2. Færið inn heiti fyrir stigveldi fyrirtækis í heitisreitnum og smellið á hnappinn Úthluta málefni.

1.3. Veljið tilgang fjárhagsáætlunargerðar, smellið á hnappinn Bæta við og úthlutið nýstofnaðri stigveldisskipan. 

[![Úthluta málefni](./media/screenshot5.png)](./media/screenshot5.png)

1.4. Endurtakið ofantalin skref fyrir málefni öryggisskipulags. Loka skjámyndinni þegar þessu er lokið.

1.5. Í skjámyndinni Stigveldi fyrirtækis skaltu smella á Skoða. Smelltu á Breyta í hönnuði stigveldis og stofnaðu stigveldi með því að smella á Setja inn.

[![Setja inn](./media/screenshot7.png)](./media/screenshot7.png) 

1.6. Veljið fjármáladeild fyrir stigveldi fjárhagsáætlunar. 

[![Fjármál](./media/screenshot8.png)](./media/screenshot8.png)

1.7. Þegar því er lokið smellirðu á Birta og Loka. Veldu 1/1/2015 sem gildisdagsetningu fyrir stigveldisbirtingu.

[![Gildisdagsetning](./media/screenshot9.png)](./media/screenshot9.png)

### <a name="task-2-configure-user-security"></a>Verkefni 2: Setja upp Öryggi notanda
Fjárhagsáætlunargerð notar sérstakar öryggisreglur til að skilgreina aðgang að gögnum fjárhagsáætlunargerðar. Julia þarf að veita sjálfri sér aðgang að fjárhagsáætlunargerðinni. 

2.1. Skipta yfir í DEMF-lögaðilasamhengi. 


2.2. Farið á Fjárhagsáætlun &gt; Uppsetning &gt; Fjárhagsáætlunargerð &gt; Skilgreining fjárhagsáætlunargerðar. Í flipanum Færibreytur skal stilla gildi fyrir öryggislíkan á Byggt á öryggisfyrirtækjum. 

[![Færibreytur](./media/screenshot11.png)](./media/screenshot11.png) 

2.3. Farið í Kerfisstjórnun &gt; Notendur &gt; Notendur. Veita stjórnanda (Julia Funderburk) hlutverk fjárhagsáætlunarstjóra. 

[![Umsjón með fjárhagsáætlun](./media/screenshot12.png)](./media/screenshot12.png) 

2.4. Veljið hlutverk notanda og smellið á Úthluta fyrirtækjum. 

[![Úthluta fyrirtækjum](./media/screenshot13.png)](./media/screenshot13.png)

2.5. Veljið "Veita skilgreindum fyrirtækjum aðgengi". Veldu Stigveldi fyrirtækis sem var búið til í fyrsta þrepinu. Veldu fjárhagstengipunkt og smelltu á hnappinn Leyfa með undirgreinum. 

***Mikilvægt!** _ _Gangið úr skugga um að vera í DEMF-lögaðilasamhengi þegar þetta er gert, þar sem fyrirtækisöryggi er notað fyrir hvern lögaðila* 

### <a name="task-3-create-scenarios"></a>Verkefni 3: Stofna atburðarás
3.1. Farið á Fjárhagsáætlun&gt;Uppsetning &gt; Fjárhagsáætlunargerð &gt; Skilgreining fjárhagsáætlunargerðar. Á síðunni Atburðarás: Takið eftir aðstæðum sem verða notaðar síðar í þessu ferli: Raunupphæðir Fyrra árs og Fjárhagáætlun. 

*Athugið: Hægt að stofna nýja atburðarás fyrir þessa æfingu og nota í staðinn.* 

[![Nýjar aðstæður](./media/screenshot15.png)](./media/screenshot15.png) 

*Athugið: Þar sem Julia notar ekki formleg samþykktarferli fyrir undirbúning fjárhagsáætlunar, munum við hlaupa yfir uppsetningar Verkflæði, Stig og Verkflæðisstig í þessari æfingu og nota fyrirliggjandi uppsetningu fyrir Sjálfvirkt – samþykkja verkflæði. Sjá viðauka fyrir þessa skilgreiningu fyrir verkflæði.*

### <a name="task-4-create-budget-plan-columns"></a>4. verkefni: Stofna fjárhagsáætlunardálka
Dálkar fyrir Fjárhagsáætlunargerð er annað hvort gjaldmiðilsdálkar eða magndálkar sem er hægt að nota í skjalinu fyrir fjárhagsáætlun.u Í dæminu okkar er nauðsynlegt að stofna dálk fyrir rauntölur fyrra árs og 12 dálka sem hver stendur fyrir einn mánuð fjárhagsársins. Hægt er að stofna dálka annaðhvort með því að smella einfaldlega á hnappinn Bæta við og fylla inn í gildi, eða með aðstoð gagnaeiningar. Í þessari æfingu munum við nota gagnaeiningu til að fylla inn i gildin. 

4.1. Í Fjárhagsáætlun&gt;Uppsetningu &gt; Fjárhagsáætlunargerð &gt; Skilgreining fjárhagsáætlunargerðar opnarðu dálkasíðuna. Smelltu á hnappinn Office í efra hægra horni í skjámyndinni og veljið Dálka (óafmarkaða). 

[![Ósíaðir dálkar](./media/screenshot16.png)](./media/screenshot16.png) 

4.2. Kerfið mun opna Excel-vinnubókina sem á að nota til að fylla út gildi. Ef beðið er um það skal smella á Leyfa breytingar og Treysta þessu forriti. 

4.3. Við munum þurfa fleiri dálka til að fylla gildin inn í. Smellt er á hönnun hægra megin til að bæta dálkum við hnitanetið. 

[![Hönnun](./media/screenshot19.png)](./media/screenshot19.png) 

4.4. Smellið á litla blýantstáknið við PlanColumns til að sjá tiltæka dálka til að bæta við hnitanetið. 

[![Breyta](./media/screenshot20.png)](./media/screenshot20.png) 

4.5. Tvísmelltu á hvert tiltækt svæði til að bæta þeim við Valið svæði og smellið á Uppfæra. 

4.6. Bætið við öllum dálkum sem þarf að stofna í Excel-töflunni. Notaðu aðgerð AutoFill í Excel til að bæta línum á fljótlegan hátt. Gangið úr skugga um að línum sé bætt við sem hluta af töflu (þegar flett er lóðrétt, ætti að vera unnt að sjá haus dálks efst á hnitanetinu). 

4.7. Farðu til baka í forritið og endurræstu síðuna. Birt gildi munu birtast. 

[![Endurhlaða](./media/screenshot23.png)](./media/screenshot23.png)

### <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>Verkefni 5: Búa til útlit og sniðmát fjárhagsáætlunarskjals
Útlit ákvarðar hvernig hnitanet fyrir fjárhagsáætlunargerðarskjalið lítur út þegar notandi opnar skjal fjárhagsáætlunargerðar. Einnig er hægt að skipta um útlit fyrir skjal fjárhagsáætlunargerðar til að sjá sömu gögn frá mismunandi sjónarhornum. Núna, þegar hún hefur skilgreint dálka til notkunar með fjárhagsáætlunargerðarskjali, þarf Julia að búa til skjal yfir útlit fjárhagsáætlunar, sem myndi líta svipað út og Excel taflan sem hún notar til að stofna fjárhagsáætlunargögn (sjá hlutann Yfirlit yfir aðstæður í þessari æfingu) 

5.1. Í Fjárhagsáætlun&gt;Uppsetningu &gt; Fjárhagsáætlunargerð &gt; Skilgreining fjárhagsáætlunargerðar opnarðu útlitssíðuna. Búa til nýtt útlit fyrir færslu fyrir mánaðarlega fjárhagsáætlun:

-   Taka MA + BU víddasamstæðu til að innifela aðalreikninga og viðskiptaeiningar í útlitinu.
-   Skrá alla fjárhagsáætlunardálka sem voru stofnaðir í fyrra skrefi í hlutanum Einingar. Gera allt nema rauntölur fyrra árs breytanlegt.
-   Smellið á hnappinn Lýsingar til að velja hvaða fjárhagsvíddir skuli birta Lýsingar í hnitanetinu.

[![Lýsingar](./media/screenshot24.png)](./media/screenshot24.png) 

Miðað við skilgreiningu á fjárhagsáætlunarútliti er hægt að stofna Excel sniðmátið sem nota á sem aðra leið til að breyta gögnum fjárhagsáætlunar. Eins og Excel sniðmát þarf að passa við skilgreiningu á uppsetningu fjárhagsáætlunar, er ekki hægt að breyta fjárhagsáætlunaruppsetningu eftir myndun Excel sniðmáts, því ætti að gera þetta verkefni eftir að allir þættir í uppsetningu hafa verið skilgreindir. 

5.2. Fyrir útlit sem var stofnað í skrefi 5.1. skref er smellt á hnappinn Sniðmát &gt; Mynda. Staðfesta viðvörunarboðin. Til að skoða sniðmátið, smellið á Sniðmát &gt; Skoða. 

*Athugasemd: Gangið úr skugga um að velja "Vista sem" og veljið stað þar sem geyma á sniðmát til að breyta henni. Ef notandi velur "Opna" í svarglugganum án þess að vista, verða breytingarnar á skránni ekki vistaðar þegar skránni verður lokað.* 
[![Sniðmátsyfirlit](./media/screenshot25.png)](./media/screenshot25.png) 

5.3. &lt; Valfrjálst skref&gt; Breytið Excel-sniðmáti til að það líti notendavænna út – bæta við formúlum, fyrirsagnasvæðum, sniðum o.s.frv. Vistið breytingarnar og hlaðið skránni upp á fjárhagsáætlunarútlit með því að smella á Útlit &gt; Hlaða upp. 


### <a name="task-6-create-a-budget-planning-process"></a>Verkefni 6: Stofna ferli fjárhagsáætlunargerðar
Julia þarf að stofna og virkja nýja fjárhagsáætlunargerð með því að sameina alla uppsetninguna hér að ofan til að byrja að færa inn fjárhagsáætlanir. Ferli fjárhagsáætlunargerðar skilgreinir hvaða fyrirtækisfjárhagsáætlanir, verkflæði, útlit og sniðmát verður notað til að stofna fjárhagsáætlunargerð. 

6.1. Farðu í Fjárhagsáætlun &gt; Uppsetning &gt; Fjárhagsáætlunargerð &gt; Ferli fjárhagsáætlunargerðar og stofnaðu nýja færslu.

-   Ferli fjárhagsáætlunargerðar - DEMF fjárhagsáætlun FY2016
-   Fjárhagsáætlunarhringrás - FY2016
-   Höfuðbók - DEMF
-   Sjálfgefið reikningsskipulag – Framleiðsla P&L
-   Stigveldi fyrirtækis – velja stigveldi sem er stofnað í upphafi verkefnisins
-   Verkflæði fjárhagsáætlunargerðar – úthluta Sjálfvirkt – Samþykkja verkflæði fyrir fjármáladeild
-   Varðandi stigsreglur og sniðmát fjárhagsáætlunargerðar, fyrir hvert verkflæði Fjárhagsáætlunargerðarstigs skal ákveða hvort aðgerðin Bæta línum við og Breyta línum er leyfð, og hvaða sjálfgefna snið á að nota

*Athugið: Hægt að stofna viðbótar skjalaútlit og úthluta þeim að vera tiltæk í verkflæðisstig fjárhagsáætlunargerðar með því að smella á hnappinn Önnur útlit.* 

[![Annað útlit](./media/screenshot27.png)](./media/screenshot27.png) 

6.2. Veljið Aðgerðir &gt; Virkja til að virkja þetta verkflæði fjárhagsáætlunargerðar. 

[![Virkja](./media/screenshot28.png)](./media/screenshot28.png)

## <a name="exercise-2-process-simulation"></a>Æfing 2: Eftirlíking af ferli

### <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>Verkefni 7: Mynda upphafsgögn fyrir fjárhagsáætlunargerð úr Almennri höfuðbók
7.1. Fara í Fjárhagsáætlun &gt; Reglubundið &gt; Mynda fjárhagsáætlun úr Almennri höfuðbók. Fylla út reglubundnar færibreytur og smellið á Mynda. 

7.2. Farðu í Fjárhagsáætlun &gt; Fjárhagsáætlunargerðir til að finna fjárhagsáætlunargerð útbúna með Myndunarferlinu. 

[![Fjárhagsáætlunargerð](./media/screenshot30.png)](./media/screenshot30.png) 

7.3. Opna upplýsingar skjals með því að smella á tengilinn Skjalnúmer. Fjárhagsáætlunargerð birtist eins og skilgreint er í uppsetningu sem stofnuð var í þessari æfingu. 

[![Fjárhagsáætlunarskjár](./media/screenshot31.png)](./media/screenshot31.png)

### <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>Verkefni 8: Stofna fjárhagsáætlun fyrir núverandi ár byggt á rauntölum fyrra árs.
Hægt er að nota úthlutunaraðferðir í fjárhagsáætlunargerð til að auðveldlega afrita upplýsingar um fjárhagsáætlanir úr einum aðstæðum í aðrar / dreifa þeim yfir mörg tímabil / úthluta á víddir. Við notum úthlutanir til að stofna fjárhagsáætlun fyrir núverandi ár frá rauntölum fyrra árs. 

8.1. Veljið allar línur á hnitanetinu á fjárhagsáætlunarskjalinu og smellið á úthluta fjárhagsáætlun. 

[![Allar línur](./media/screenshot32.png)](./media/screenshot32.png) 

8.2. Veljið úthlutunaraðferð, tímabilslykil, aðstæður Uppruna og endastaðar og smellið á Úthlutun. 

[![Úthluta](./media/screenshot33.png)](./media/screenshot33.png)

Raunverulegar upphæðir fyrra árs verða afrituð yfir á áætlun núverandi árs og úthluta þeim yfir tímabil með því að nota tímabilslykilinn Sölukúrfa. 

[![Sölukúrfur](./media/screenshot34.png)](./media/screenshot34.png)

### <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>Verkefni 9: Aðlaga fjárhagsáætlunargerðarskjalið með því að nota Excel og ljúka við skjalið
9.1. Smellið á hnappinn Vinnublað til að opna innihald skjalsins í Excel.

9.2. Þegar Excel-vinnubókin opnast skal leiðrétta númer í fjárhagsáætlunargerðarskjalinu og smella á hnappinn Birta.

9.3. Farðu til baka í skjal fjárhagsáætlunargerðar. Smellt er á Verkflæði &gt; Senda til að samþykkja skjalið sjálfvirkt.

[![Sjálfvirk samþykkt](./media/screenshot37.png)](./media/screenshot37.png) 

Þegar verkflæði lýkur breytist stig fjárhagsáætlunargerðarskjala í Samþykkt. [![Samþ.](./media/screenshot38.png)](./media/screenshot38.png)

## <a name="appendix"></a>Viðauki

### <a name="auto-approve-workflow-configuration"></a>Samþykkja sjálfvirkt uppsetningu verkflæðis.

A. Fjárhagsáætlun &gt; Uppsetning &gt; Fjárhagsáætlunargerð &gt; Vinnuflæði við fjárhagsáætlun. Búðu til nýtt verkflæði með sniðmáti verkflæðis fjárhagsáætlunargerðar:

[![Stofna nýtt verkflæði](./media/screenshot39.png)](./media/screenshot39.png)

Þetta verkflæði mun aðeins innihalda eitt verk - Fjárhagsáætlunargerð stigstilfærslu. 

[![Fjárhagsáætlunargerð stigstilfærslu](./media/screenshot40.png)](./media/screenshot40.png) 

Vista og virkja verkflæðið. 

B. Farið á Fjárhagsáætlun &gt; Uppsetning &gt; Fjárhagsáætlunargerð &gt; Skilgreining fjárhagsáætlunargerðar. Á flipanum Stig skal stofna 2 stig – Upphafleg og Sent inn. 

[![Fyrstu og sendar](./media/screenshot41.png)](./media/screenshot41.png)

C. Farið á Fjárhagsáætlun &gt; Uppsetning &gt; Fjárhagsáætlunargerð &gt; Skilgreining fjárhagsáætlunargerðar. Í flipanum Verkflæðisstig skal tengja verkflæðið Samþykkja sjálfvirkt sem var stofnað í þrepi A með stigunum Upphaflegt og Sent inn.

[![Fjárhagsáætlun og fjárhagsáætlunargerð](./media/screenshot42.png)](./media/screenshot42.png)  





[!INCLUDE[footer-include](../../includes/footer-banner.md)]