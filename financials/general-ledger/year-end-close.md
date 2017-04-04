---
title: "Árslokalokun"
description: "Þetta efnisatriði lýsir uppsetningu og skrefum til að keyra lokun árslokaferlinu fjárhags."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerClosingSheet
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 926ee087a0e0c4743f29315b1d82c7d37e95be28
ms.openlocfilehash: 22233cfa1df79076c8ea42f75ea309bac990d574
ms.lasthandoff: 03/31/2017


---

# <a name="year-end-close"></a>Árslokalokun

Þetta efnisatriði lýsir uppsetningu og skrefum til að keyra lokun árslokaferlinu fjárhags. 

Við lok fjárhagsársins þarf að keyra lokun árslokavinnslu til að flytja opnunarstöður í nýtt ár. Flest fyrirtæki keyrir loka árslokaferlinu mörgum sinnum. Í fyrsta sinn er að sækja stöður sem eru færðar inn í nýtt fjárhagsár. Loka árslok síðan má keyra aftur, sem oft eru nauðsynleg til að flytja stöður úr leiðrétta færslur í nýja fjárhagsárið. 

Loka ferli við í árslok, til eru tvær gerðir færslna mögulegt að stofna. Opna færslan mynduð alltaf og er notað til að stofna opnunarstöður í nýtt fjárhagsár. Opna færsluna sýnir stöður fjárhagslykils í efnahagsreikningi í nýtt fjárhagsár og stöðu úr lykilsstöður fjárhags rekstur í fjárhag tekjulykil í nýtt fjárhagsár. Lokun færslu stofnast einnig til að færa stöðu í rekstrarlyklum niður núll í fjárhagsárinu er lokað.

## <a name="prepare-to-run-the-year-end-close"></a>Undirbúa keyrslu á ársloka
Áður en árslokaferlinu birgðalokun er keyrð skal staðfesta stillingar fyrir eftirfarandi: 

Á síðunni **Aðallykill**:

-   Villuleita í **lykilgerð Aðal** hefur verið skilgreind rétt fyrir hvern aðallykil. Aðal lykilgerðin er notuð til að ákvarða hvort stöðu aðallykils verður að vera tekin áfram sem opnunarstöðu eða lokaða óráðstafað eigið fé inn á Opna færslu.
-   Í **Opnunarlykillinn** svæði getur notað til að flytja inn nýjan aðallykil stöðu aðallykils við árslok birgðalokun. Færð er inn nýjan aðallykil í á **Opnunarlykillinn** svæði. Vanalega verður notuð fyrir aðallykla efnahagsreikningur þegar aðallykils er óvirkur og nýjan aðallykil er notað fyrir nýtt fjárhagsár.

Á við **fjárhagsfæribreytur** síðuna undir **fjárhagsárs**:

-   Í **Eyða loka færslna ársins** valkostur er notaður til að tilgreina hvort á að eyða opnunarfærsla kerfismynduð úr fyrri árslok að loka þegar árslok birgðalokun er keyrð á ný. Ef þessi valkostur er stilltur á **Já**fyrri opnunarfærsla er eytt og nýjar opnunarfærsla stofnuð á grundvelli gildandi stöður. Ef þessi valkostur er stilltur á **Nei**helst fyrri opnunarfærsla og viðbótar opnunarfærsla er stofnuð til að flytja stöður áfram frá leiðrétta færslur sem bókaðar eftir að fyrri ársloka.
-   Í **Stofna lokunarfærslur við flutning** valkostur er notaður til að stofna lokunarfærslur í fjárhagsárinu er lokað til að færa stöðu í rekstrarlyklum í núll. Ef þessi valkostur er stilltur á **Já**, opnunarfærsla og Lokun færsla er stofnuð. Ef þessi valkostur er stilltur á **Nei**, aðeins opnunarfærsla er stofnuð í næsta fjárhagsárs til að flytja stöður. Hagnaður og tap lykilsstöður eftir við lok fjárhagsársins.
-   Í **Stilla stöðu fjárhagsárs lokað varanlega** valkostur er notaður til að stilla fjárhagsár varanlega lokaðri stöðu. Nota þessa stillingu varlega, því öll tímabil með varanlega lokaðri stöðu er ekki hægt að enduropna, koma í veg leiðréttingar séu bókaðar á fjárhagsár. Það er besta leiðin til að setja þetta á **Nei**.
-   Í **tiltaka þarf fylgiskjalsnúmer** valkostur er notaður til að skilgreina hvort númer fylgiskjals er krafist þegar árslokaferlinu birgðalokun er keyrð. Er besta leiðin til að krefjast númer fylgiskjals að auðvelt sé að finna á Opna færslu.

Á við **fjárhagsdagatal** síðu:

-   Næsta fjárhagsárs verður að vera til áður en lokið í árslok í gangi. Næsta fjárhagsárs er krafist til að stofna í upphafsstöður opnunarstaða tímabilsins.

Á við **fjárhagsdagatal** síðu:

-   Valfrjálst: Hvert fjárhagstímabil fyrir fjárhagsárið lokað er má stilla **í bið** til að koma í veg fyrir nýjar færslur úr færðar inn. Þegar leiðréttingarfærslur eru auðkenndar á bið tímabilin sem hægt er að enduropna til að bóka leiðréttingarfærslur, jafnvel þó að birgðalokun árslokaferlinu hefur þegar verið keyrt.

## <a name="define-year-end-close-templates"></a>Skilgreina ársloka loka sniðmát
Eftir að kerfið sé skilgreint hægt að keyra lokun árslokaferlinu. Á við **ársloka** síðu er hægt að skilgreina sniðmát fyrir hóp lögaðila sem loka á árslok vinnslu verður að keyra. Sniðmátið verður að endurnýta við hverja árslok lokið, en er hægt að breyta ef fyrirtækið breytingar. 

Fyrst skal skilgreina á **flokksheiti** fyrir sniðmátið og veljið fjárhagsdagatalinu. Heiti flokksins ætti að auðkenna hóp með lögaðila.  Til dæmis sniðmátin kann að setja upp byggt á landafræði við sérstaka flokka stofnuð fyrir American norður-lögaðila EMEA lögaðila og APAC lögaðila. 

Næst skal lögaðila er bætt við sniðmátið. Hægt er að bæta lögaðilum með því að velja stigveldi fyrirtækis eða með því að velja lögaðila. Ef stigveldi fyrirtækisins er valinn eru aðeins lögaðila innan stigveldi sem nota valið fjárhagsdagatal verður bætt við sniðmátið. Ef lögaðila er notuð til að bæta sniðmáti er hægt að bæta aðeins lögaðilum með sama fjárhagsdagatal. Sama fjárhagsdagatal er krafist vegna þess að árslok birgðalokun er keyrð með því að velja fjárhagsár sem getur verið breytilegur úr dagatalinu á dagatalinu. 

Eftir lögaðila er bætt við að skilgreina óráðstafað eigið fé aðallykla fyrir hvern lögaðila. Í **ár síðasta Lokadagsetning loka** svæði verður að vera uppfærð í hvert sinn árslok birgðalokun er keyrð fyrir lögaðila. 

Í **fjárhagsvídd** flipinn er notaður til að skilgreina hvaða fjárhagslegar víddir verða notaðar á Opna færslu. Athugið að verið er að skilgreina stillingar eiga við aðeins valins lögaðila í á **lögaðila** hnitanetinu. Endurtaka verður uppsetningu fyrir hvern lögaðila í hnitanetinu. 

Í **Flytja víddir efnahagsreikningur** er notuð til að skilgreina hvort fjárhagsvíddir í færslur bókaðar á efnahagslykla ætti að viðhalda á Opna færslu. Besta leiðin til að setja þennan valkost til að hún er **Já**. Í **Flytja víddir rekstur** er notuð til að skilgreina hvaða fjárhagsvíddir á færslunum sem bókaðar eru sem hagnaður og tap fluttar í aðallykilinn óráðstafað eigið fé. Auðkenna fyrst fjárhagsvíddir sem eiga við valinn lögaðila. Þetta myndi fela í sér allar fjárhagsvíddir bókuð á móti á árinu, jafnvel þótt fjárhagsvíddinni er ekki hluti af virku lykilskipulagi. Næst skal skilgreina hverrar víddar sem annað hvort **Loka einn** eða **Loka öllum**.  Sjálfgefin **Loka öllum**, upphaflega fjárhagsvíddina sem viðheldur gildi úr bókaðar færslur og notar þau fyrir stofnun opnunar stöðum á tekjulykil. Aðskilin óráðstafað eigið fé upphafsstöður verður stofnuð fyrir hverja einkvæma samsetningu fjárhagsvíddargildi. Ef **Loka einn** er valinn eru allar færslur sem eru bókaðar með sem fjárhagsvídd saman í óráðstafað eigið fé upphafsstaða víddargildisins færður inn í svæði eftir **Loka einn**. Til dæmis, fyrir allar færslur fyrir fjárhagsár voru bókaðar með lykilskipulag aðallykils - Deild. Í fjárhagsvíddinni Deild á sem sniðmát **Loka einn** er valinn og 100 er fært inn gildi. Ef heildartekjum af allar færslur bókaðar á deildir 200 300 og 400 er $100,000 eina opnunarstaða stofnuð fyrir Retained earnings - 100. Ef **Loka einn** og autt gildi fjárhagsvídda, allar færslur verður bókuð í óráðstafað eigið fé gildið víddin er auð. 

Loka árslokaferlinu ekki fylgja eigi stillingunni lykilskipulag. Þetta er vegna þess að lykilskipulag má breyta í gegnum fjárhagsársins og ekki er alltaf hægt að auðkenna viðkomandi lykilskipulag vegna þessara breytinga.  Þegar opnunarfærslur eru stofnaðar stöður verða að vera tekin fram með fjárhagsvíddir eins og skilgreint er í ár lok sniðmát loka. Upphaf stöður færslur gætu hafa fjárhagsvíddir ekki lengur í gildandi lykli skipulag og hluta samsetningarnar sem eru ekki lengur gild í núgildandi lykilskipulag. Ef fyrirtækið vill að útiloka fjárhagsvídd varðveitt tekjukóða stillt upphafsstaða, fjárhagsvídd sem á að vera **Loka einn** og skiljið auð víddargildi.

## <a name="run-the-year-end-close-process"></a>Keyra birgðalokun árslokaferlinu
Eftir að loka ársloka sniðmátin eru stofnaðar, loka árslokaferlinu ræst með því að velja **Keyra fjárhagsár** í Aðgerðarúðunni. Annað hvort að velja allar eða hlutmengi lögaðila úr sniðmáti sem á að keyra birgðalokun við árslok. Þegar í gangi í árslok lokið í fyrsta skipti í fjárhagsári líklega verður að velja öllum lögaðilum til að stofna upphafsstöður fyrir alla lögaðila. Ef afskriftareglur eru keyrð í árslok lokun aftur, má velja að keyra vinnslu fyrir aðeins lögaðila sem leiðréttingarfærslur voru bókaðar. 

Velja fjárhagsár sem óskað er að keyra fyrir lokun árslokavinnsla gegn. Ef fleiri en einn lokunartímabil til á síðasta tímabili fjárhagsársins, sem **heiti Tímabils** svæði verða tiltækar þannig að hægt er að velja hvaða lokunartímabils sem á að bóka færsluna Lokun ef uppsetning er skilgreind til að stofna færslu fyrir Lokun. 

Færið inn fylgiskjals númer, sem eða má ekki vera áskilið, allt eftir uppsetningu í færibreytum fjárhags. Verður að nota sama fylgiskjalsnúmer fyrir alla lögaðila valið fyrir í loka árslokavinnsla. Númer fylgiskjals er ekki mynduð með því að nota númeraröð. Besta leiðin til að færa inn fylgiskjalsnúmer, er jafnvel þótt að það hefur ekki áskilið. Færa inn fylgiskjalsnúmer gerir það auðveldara að finna færsluna Opnunarstöður í nýtt fjárhagsár. Ef fært er inn númer fylgiskjals er ekki verður fylgiskjalið autt fyrir Opna færslu. 

Ef óskað er að bakfæra loka fyrra lokadagsetningu fyrir valið fjárhagsár, setja **Afturkalla fyrri lokun** til **Já**. Árslok birgðalokun verður að bakfæra en ferlinu hægt endurkeyra hvenær. Ef bakfærð árslok birgðalokun, er **Dagsetning fyrir lok síðasta árs loka** verður ekki tiltæk. 

Loka árslokaferlinu sjálfgildi til að keyra í runuhætti. Er besta leiðin til að keyra ferlið í runustillingu til að leyfa notanda að fara aftur í aðrar aðgerðir. Eftir við lok ferli við lokun er lokið, í **ár síðasta Lokadagsetning loka** verður uppfærð með dagsetningu biðlarasetu.

Nánari upplýsingar, sjá [Loka á fjárhags við lok tímabils](close-general-ledger-at-period-end.md).


