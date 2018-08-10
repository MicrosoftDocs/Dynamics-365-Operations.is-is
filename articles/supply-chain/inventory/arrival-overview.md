---
title: Komuyfirlit
description: "Þetta efnisatriði veitir upplýsingar um komuyfirlitseiginleikann. Komuyfirlitssíðan er hluti þessa eiginleika og sýnir yfirlit yfir allar vörur sem eru væntanlegar."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSArrivalOverview, WMSArrivalOverviewProfile, WMSJournalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9c174dc7bf61ffab0d20c7685a29007e0b6e2e7e
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="arrival-overview"></a>Komuyfirlit

[!include [banner](../includes/banner.md)]

Þetta efnisatriði veitir upplýsingar um komuyfirlitseiginleikann. Komuyfirlitssíðan er hluti þessa eiginleika og sýnir yfirlit yfir allar vörur sem eru væntanlegar.

Síðan **Komuyfirlit** sýnir yfirlit yfir allar væntanlegar vörur. Hún sýnir einnig komur sem hægt er að ræsa byggt á yfirlitinu. Þetta efnisatriði fjallar um móttökuferlið.

## <a name="business-scenario"></a>Dæmi um fyrirtæki
Íhugið eftirfarandi dæmi fyrir ferli á innleið.

[![Dæmi um fyrirtæki](./media/arrival-overview-scenario.png)](./media/arrival-overview-scenario.png)

Sammy, sem starfar í móttöku, vill fá að vita hvað muni berast viðkomandi dag. Á síðunni **Komuyfirlit** getur Sammy séð yfirlit yfir verk í gangi og gróft mati á fjölda, magni, þyngd, mismunandi gerðum o.s.frv. Síðar berast vörur á einu innhliði og Sammy fær lista yfir afhendingu. Á síðunni **Komuyfirlit** getur Sammy framkvæmt eftirfarandi verkefni:

-   Séð samsvarandi innhreyfingarskjal og skráð móttökuna sem **Í vinnslu**. Línurnar sem eru nauðsynleg fyrir skráningu eru sjálfvirkt myndaðar og hægt að fara yfir innhreyfingarskjalið, jafnvel þótt færslan hafi ekki enn verið bókuð sem **Skráð**.
-   Aðgangur að viðkomandi tilvísun komubókar (það er, **Vörumóttaka** færslubókinni eða **Framleiðsluinntak** færslubókinni) og sjá færslubækur sem eru tilbúnar fyrir uppfærslu innhreyfingarskjala.

## <a name="arrival-overview-page"></a>Komuyfirlitssíða
Til að opna síðuna **Komuyfirlit** skal smella á **Birgðastjórnun** &gt; **Pantanir á innleið** &gt; **Komuyfirlit**. Hægt er að skoða lista yfir pantanir sem búist er við að hafa borist. Yfirlitið er skipt upp í haus og línur. Upplýsingar í haus er flokkaðar eftir gerð pöntunar, áætlaðri móttökudagsetningu og afhendingarstað. Þegar hauslína er valin fyrir komu eru allar upplýsingalínur sem tengjast tilvísun innhreyfingarinnar valdar til komu í línuupplýsingahluta síðunnar. Þegar allar tengdar færslubókarlínur hafa verið bókaðar birtast þessar upplýsingar ekki.

### <a name="arrival-overview-profiles"></a>Komuyfirlitsreglur

Síðan **Komuyfirlit** veitir yfirlit yfir vörur sem von er á og áætluðum komudegi. Hægt er að nota ýmsar persónubundnar stillingar við komuferlið. Einstaka notendur geta skilgreint persónulegar stillingar sínar á síðunni **Komuyfirlitsreglur**.

### <a name="set-up-item-arrival"></a>Setja upp vörukomu

Í dæminu okkar vill Sammy setja upp nýja tölvu á staðsetningu sem verður notað til að fá tilbúnar vörur sem koma úr framleiðslu á svæði 1. Á síðunni **Komuyfirlitsreglur** stofnar Sammy nýja uppsetningu sem er nefnd **Framleiðsla á svæði 1** og tilgreinir eftirfarandi stillingar.

1.  Á flýtiflipanum **Komuvalkostir** í reitnum **Svið** skal slá inn upplýsingar um dagabil og vöruhús sem á að taka með í yfirlitinu.
2.  Á flýtiflipanum **Komuvalkostir** í reitnum **Færslubók** skal skrifa móttökuvöruhús, staðsetningu og heiti færslubókar (vara koma/framleiðsluílag).
3.  Á flýtiflipanum **Upplýsingar um fyrirspurn vegna komu** í reitnum **Svæði** í reitnum **Takmarka við svæði** skal slá inn svæði til að takmarka yfirlitssvæðið.
4.  Á flýtiflipanum **Upplýsingar um fyrirspurn vegna komu** í reitnum **Sýndar færslugerðir** skal stilla valkostinn **Framleiðslupantanir** á **Já**.
5.  Á flýtiflipanum **Upplýsingar um fyrirspurn vegna komu** í hópnum **Ýmislegt** skal stilla valkostinn **Uppfæra við ræsingu** á **Já** ef uppfæra á yfirlitið sjálfkrafa við ræsingu. Stillið valkostinn **Uppfæra við breytingu afmörkunar** á **Já** ef uppfæra á yfirlitið sjálfkrafa þegar reitargildum er breytt.

Í þessu dæmi er reiturinn **Heiti komuyfirlitsreglu** á **Komuvalkostir** á síðunni **Komuyfirlit** stilltur á **Framleiðsla á svæði 1**.

### <a name="prerequisites-for-arrival-journals"></a>Forkröfur fyrir komubækur

Til að stofna sjálfkrafa komubækur á síðunni **Komuyfirlit** verður að skilgreina viðeigandi upplýsingar í reitarhópnum **Færslubók** svæðisflokkur á síðunni **Komuvalkostir**.

-   Velja þarf heiti færslubókar til að stofna nýja færslubók.

[![Tilgreina heiti færslubókar](./media/arrival-overview-journal.png)](./media/arrival-overview-journal.png)

-   Ef gildi er tilgreint í reitunum **Vöruhús** og **Staðsetningu** eru þau notuð á færslubókarlínur. Ef gildi eru ekki tilgreind notar kerfið gildið úr víddinni sem er tilgreind á birgðafærslum.

#### <a name="items-that-are-received-from-one-expected-receipt-order"></a>Vörur sem eru mótteknar frá einni áætlaðri innhreyfingu

Á flýtiflipanum **Innhreyfingar** velur Sammy línu og smellir á **Upphafskoma**. Allar tengdar línur sem eru í tilgreinda sviðinu og eru með magni til að skrá eru valdar sjálfkrafa. Vörukomubók er búin til sem hefur jöfnun á milli áætlaðs innhreyfingarmagns og færslubókar. Magnið er sjálfvirkt frumstillt á öllum línum sem eru stofnaðar.

#### <a name="items-that-are-received-from-more-than-one-expected-receipt-order"></a>Vörur sem eru mótteknar frá meira en einni áætlaðri innhreyfingu

Á flýtiflipanum **Innhreyfingar** velur Sammy margar línur og smellir á **Upphafskoma**. Vörukomubók er búin til sem hefur jöfnun á milli alls áætlaðs innhreyfingarmagns og færslubókar. Allar línur eru stofnaðar á einum haus vörukomubókar og magnið er sjálfvirkt frumstillt.

### <a name="receive-items-from-one-or-more-expected-receipt-orders"></a>Móttaka vara frá einni eða fleiri innhreyfingum vara

#### <a name="view-information"></a>Skoða upplýsingar

Til að fá yfirlit yfir áætlaðar innhreyfingar á dagsetningarbili færir Sammy inn eftirfarandi upplýsingar í svæðunum á flýtiflipanum **Komuvalkostir** á síðunni **Komuyfirlit** og smellir svo á **Uppfæra** til að uppfæra yfirlitið:

-   Heiti komuyfirlitsreglu: **Fyrirspurn**
-   Sýna línur: **Allar**
-   Dagar aftur; (autt)
-   Dagar fram að: **0**
-   Vöruhús: **GW, MW**

Sammy getur skoðað eftirfarandi upplýsingar:

-   Allar tengdar innhreyfingar pantana fyrir kerfisdagsetninguna og ótakmarkaðan fjölda daga frá henni (í **InventTrans.StatusDate** bili), og kvittanir fyrir vöruhús GW og MW, óháð stöðu.
-   Nánari línuupplýsingar fyrir fleiri en eina pöntun. Sammy getur valið margar hauslínur á yfirlitinu og svo smellt á **Sýna allt valið** til að skoða allar samsvarandi línuupplýsingar fyrir allar valdar pantanir.
-   Upplýsingar um tiltekna innkaupapöntun. Til að sýna aðeins upplýsingar sem tengjast ákveðnu tilvísunarnúmeri í yfirlitinu getur Sammy slegið inn reikningsnúmer í reitnum **Reikningsnúmer** og raðnúmer í reitnum **Tilvísunarnúmer**.
-   Yfirlit yfir skráningarverkefnin fyrir allar pöntunarlínurnar sem komubókin hefur verið búin til fyrir en hefur ekki enn verið birt. Til að skoða þessar upplýsingar getur Sammy valið **Í vinnslu** á svæðinu **Sýna línur**.

### <a name="update-journals"></a>Uppfæra færslubækur

Til að skrá eina eða fleiri línur sem eru á gjalddaga getur Sammy valið línurnar á yfirlitshnitaneti eða línuhnitaneti og smellt á **Færslubækur** &gt; **Sýna komur úr innhreyfingu**. Hausar komuvara sem samsvara línum sem eru sýndar. Til að uppfæra innhreyfingarskjal kvittunar á skráðum vörum, getur Sammy aðgang að við vöru komu færslubóka sem eru tilbúnar til uppfærslu. Til að fá aðgang að þessum hausum komubóka smellir hann á **Færslubækur** &gt; **Færslubækur sem eru reiðubúnar fyrir innhreyfingarskjal afurða**. Allar hauslínurnar sem eru tilbúnar til uppfærslu innhreyfingarskjals á tiltekið vöruhús eru sýndar. (Hauslínur sem eru sýndar tengjastt ekki dagabilinu).

### <a name="start-an-arrival-registration"></a>Hefja komuskráningu

Með því að velja margar línur á síðunni **Komuyfirlit** getur Sammy ræst meira en eina innhreyfingartilvísun. Þegar hann velur línu úr yfirliti innhreyfinga eru samsvarandi línuupplýsingar valdar. Ef magn fyrir skráningu er til staðar er hnappurinn **Upphafskoma** tiltækur. Sammy getur notað tvær leiðir til að hefja komuskráningu:

-   Til að sía síðuna þannig að hún sýni einungis færslur sem uppfylla ákveðnum skilyrði í reitnum **Tilvísun lánardrottins** skal skanna tilvísunarnúmer frá lánadrottni, eins og til dæmis strikamerki fyrir fylgiseðil.
-   Í yfirlitshlutanum eða upplýsingahluta á síðunni **Komuyfirlit** skaltu velja eða hætta við val færsla fyrir komuskráningu. Þegar Sammy smellir svo á **Upphafskoma** eru völdu færslurnar sjálfkrafa stofnaðar í vörukomubók. Færslurnar eru með línuupplýsingar og öllum einkvæmum reitarupplýsingum er úthlutað.

## <a name="update-arrival-information-and-process-a-product-receipt"></a>Uppfæra komuupplýsingar og vinna innhreyfingarskjal
Þegar allar vörur hafa verið skráðar getur vöruhússtjórinn eða innkaupastjórinn uppfært mótteknar vörur með fylgiseðli til að bæta við efnislegum kostnaði. Fylgið eftirfarandi skrefum til að uppfæra upplýsingar um komu og bóka innhreyfingar vara.

1.  Smellt er á **Birgðastjórnun** &gt; **Pantanir á innleið** &gt; **Komuyfirlit**.
2.  Á síðunni **Komuyfirlit** er smellt á **Færslubækur** &gt; **Færslubækur sem eru reiðubúnar fyrir innhreyfingarskjal afurða** til að birta lista færslubóka sem eru tilbúnar til uppfærslu innhreyfingarskjals.
3.  Veljið færslubækurnar sem þarf að uppfæra og smella síðan á **Aðgerðir** &gt; **Innhreyfingarskjal afurðar**.
4.  Á síðunni **Bókun** skaltu færa inn númer innhreyfingarskjals ef það er ekki þegar til staðar í færslubókinni og smella síðan á **í lagi** til að vinna innhreyfingarskjal.

## <a name="summary"></a>Samantekt
Síðan **Komuyfirlit** getur hjálpað vöruhússtjóra og starfskröftum að sjá yfirlit yfir væntanleg verk sem þarf að vinna sem hluta af vinnslu á innleið. Einnig er hægt að nota síðuna til að hefja komuferlið, til að aðstoða við að tryggja rakningu vara við fyrstu færslu í vöruhúsið.

