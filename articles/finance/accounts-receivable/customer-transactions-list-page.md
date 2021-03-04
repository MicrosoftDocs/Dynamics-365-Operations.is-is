---
title: Listasíða með færslum viðskiptavinar
description: Þetta efnisatriði veitir upplýsingar um listasíðu með viðskiptavinafærslum fyrir Microsoft Dynamics 365 Finance.
author: mikefalkner
manager: aolson
ms.date: 08/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 948f83d56e560cc21205294c15de4b2097d2ad2e
ms.sourcegitcommit: e544c51a68ad5daf748c0e877bdbde094ad40bd2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/03/2020
ms.locfileid: "4444600"
---
# <a name="customer-transactions-list-page"></a>Listasíða með færslum viðskiptavinar

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a>Skoða uppgjör

**Skoða uppgjör** hnappinn á aðgerðarsvæðinu veitir skjótan aðgang að uppgjörsferlinu og nákvæmar upplýsingar um uppgjörsfærsluna. Þú getur einnig sýnt fleiri færslur sem tengjast valdri færslu, annaðhvort vegna þess að þær voru hluti af sama uppgjörinu eða vegna þess að þær eru greiðslur sem voru búnar til í sömu greiðslubókinni.

1. Veldu **Viðskiptakröfur \> Allir viðskiptavinir**.
2. Veldu viðskiptavin sem er með færslur og síðan á aðgerðasvæðinu í flipanum **Viðskiptavinur** skaltu smella á **Færslur**.
3. Veldu færslu til að kanna og síðan á aðgerðasvæðinu skaltu smella á **Skoða uppgjör**.

    Svarglugginn **Skoða uppgjör** birtist og sýnir valda færslu og öll skjöl sem hafa verið jöfnuð á móti henni. Þessi svargluggi líkist yfirliti uppgjörsferils, en hann inniheldur öll tengd skjöl.

4. Í svarglugganum er hægt að framkvæma ýmis verk. Veldu eitt eða fleiri fylgiskjöl og veldu síðan einn af eftirfarandi hnöppum:

    - **Skoða tengt** - Sýna allar greiðslubókarfærslur og færslubókarfærslur fyrir viðskiptavininn sem var búinn til í færslubókunum þar sem skjölin sem sýnd eru í listanum voru búin til. Til dæmis, ef greiðsla er sýnd, birtast allar greiðslur í greiðslubókinni þar sem hún var búin til. Ef reikningur eða greiðsla er sýnd og hún var búin til í almennri færslubók, þá birtast öll skjölin í almennu færslubókinni þar sem hún var búin til. Öll uppgjör sem tengjast skjalalista eru einnig sýnd. Við skoðun á tengdum greiðslum breytist merkið á þessum hnappi í **Skoða uppgjör**. Veldu **Skoða uppgjör** til að sýna aðeins færslurnar sem sýndar voru þegar þú opnaðir fyrst svargluggann **Skoða uppgjör**.
    - **Skoða feril** - Skoða uppgjörsferli fyrir fylgiskjölin. Veldu **Loka** til að loka svarglugganum.
    - **Skoða bókhald** - Sýna öll fylgiskjöl sem tengjast völdum skjölum. Veldu **Loka** til að loka svarglugganum.
    - **Flytja út** - Flyttu út valin fylgiskjöl í Microsoft Excel.
    - **Gera upp færslur** - Þessi hnappur birtist aðeins ef upprunalega skjalið sem var valið var ekki að gert upp að fullu. Þegar þú velur þennan hnapp birtist svarglugginn **Gera upp færslur** þar sem þú getur valið færslur til að gera upp.
    - **Afturkalla uppgjör** - Þessi hnappur birtist aðeins ef upprunalega skjalið sem var valið var gert upp að fullu. Þegar þú velur þennan hnapp birtist svarglugginn **Afturkalla uppgjör** þar sem þú getur afturkallað uppgjör sem voru gerð á skjalinu.

## <a name="global-transactions"></a>Alþjóðlegar færslur

Hnappurinn **Alþjóðlegar færslur** birtist einnig á listasíðunni **Færslur viðskiptavina**. Þessi hnappur gerir þér kleift að skoða allar færslur fyrir viðskiptavin yfir alla lögaðila. Listasíðan **Færslur viðskiptavinar** sýnir færslur aðeins fyrir lögaðila sem notandinn hefur aðgang að, byggt á öryggisstillingum notanda.

Listasíðan sýnir allar færslur fyrir viðskiptavini sem hafa sama auðkenni aðila eins og viðskiptavinurinn sem þú byrjaðir með. Til dæmis, ef viðskiptavinur US-001 í einum lögaðila hefur sama auðkenni aðila og viðskiptavinur DE-001 í öðrum lögaðila, eru allar færslur fyrir bæði auðkenni viðskiptavinar sýndar.

Valmyndirnar á listasíðunni **Færslur viðskiptavinar** eru breytilegar, fer eftir lögaðila færslunnar. Til dæmis, ef eiginleiki er aðeins í boði fyrir svissneska lögaðila, birtast aðeins valkostir valmyndarinnar fyrir þá eiginleika þegar svissnesk færsla er valin.

Fylgið eftirfarandi skrefum til að fá aðgang að eiginleikanum.

1. Veldu **Viðskiptakröfur \> Allir viðskiptavinir**.
2. Veldu viðskiptavin og síðan á aðgerðasvæðinu í flipanum **Viðskiptavinur** í flokknum **Færslur** skal velja **Alþjóðlegar færslur**.

## <a name="more-transaction-filters"></a>Fleiri færslusíur 

Sían til að sýna opnar færslur hefur verið skipt út fyrir nýja síu sem leyfir þér að skoða fleiri samsetningar af færslum. Eftirfarandi valkostir eru í boði í reitnum **Sýna**:

- **Allar** - Sýna allar færslur fyrir valinn viðskiptavin (opnar og lokaðar).
- **Lokaðar** - Sýna aðeins færslur sem hafa verið gerðar upp að fullu og lokaðar.
- **Opnar** - Sýna aðeins færslur sem ekki hafa verið gerðar upp að fullu.
- **Opið þ.m.t. lokað á eða eftir dagsetninguna** - Sýna aðeins færslur sem ekki hafa verið gerðar upp að fullu á eða eftir dagsetningu sem þú tilgreinir. Þegar þessi valkostur er valinn er hægt að breyta dagsetningunni sem er sýnd við hliðina á síunni. Færslur sem eru með gildi fyrir **Síðustu uppgjörsdagsetningu** eða eftir dagsetningunni sem þú tilgreinir eru sýndar í listanum, ef þessar færslur eru gerðar upp að fullu frá og með núverandi dagsetningu. Hins vegar sýnir staðan stöðurnar frá og með núverandi degi, ekki frá þeim degi sem valinn er.

Veldu **Fela endurmat á gjaldmiðli** gátreitinn til að fela færslur fyrir umreikning gjaldmiðils.

## <a name="modify-due-dates-and-discount-dates"></a>Breyta gjalddögum og afsláttardagsetningum

Þú getur uppfært gjalddaga og afsláttardagsetningar fyrir opnar færslur viðskiptavinar. Í útgáfu 8.1 er hægt að bæta gjalddögum við listasíðuna **Færslur viðskiptavinar**. Með því að smella á gjalddaga á listasíðunni **Færslur viðskiptavinar** getur þú líka breytt gjalddögum, afsláttardagsetningum, greiðsluskilmálum og skilmálum staðgreiðsluafsláttar í svarglugganum **Uppfæra gjalddaga og dagsetningar staðgreiðsluafsláttar**.

### <a name="activate-the-feature"></a>Virkja eiginleikann

Til að bæta gjalddögum við listasíðuna **Færslur viðskiptavinar** og breyta greiðslustillingum fyrir færslu með því að nota svargluggann **Uppfæra gjalddaga og dagsetningar staðgreiðsluafsláttar** skaltu fylgja þessum skrefum.

1. Veldu **Viðskiptakröfur \> Uppsetning \> færibreytur viðskiptakrafa**.
2. Í flipanum **Uppgjör** skal setja valkostinn **Sýna gjalddaga og leyfa breytingar** á **Já**.
3. Til að virkja þennan valkost hefur nýjum reitum verið bætt við færslur viðskiptavinar. Fylltu verður í þessa reiti þegar ný færsla klárast. Þeir verða einnig útfylltir þegar þú opnar svargluggann **Uppfæra gjalddaga og dagsetningar staðgreiðsluafsláttar**. Þegar þú stillir valkostinn **Sýna gjalddaga og leyfa breytingar** á **Já** munt þú sjá svargluggann **Uppfæra greiðsluupplýsingar**.  Til að uppfæra fyrirliggjandi færslur strax skaltu velja **Uppfæra allar fyrirliggjandi færslur**. Að öðrum kosti, til að fylla út reitina aðeins fyrir nýjar færslur, skaltu velja **Halda áfram án uppfærslu**.

Gjalddaga hefur nú verið bætt við listasíðuna **Færslur viðskiptavinar** og svo þú getir á þægilegri hátt breytt gjalddaganum og dagsetningum staðgreiðsluafsláttar fyrir færslur.

### <a name="modify-the-payment-settings"></a>Breyta greiðslustillingum

Listasíðan **Færslur viðskiptavinar** sýnir allar færslur fyrir viðskiptavin. Þegar þú velur gjalddaga fyrir færslu birtist svarglugginn **Uppfæra gjalddaga og dagsetningar staðgreiðsluafsláttar**. Þessi svargluggi sýnir grunndagsetninguna fyrir gjalddaga og afsláttarútreikninga, gjalddaga, greiðsluskilmála, skilmála staðgreiðsluafsláttar og dagsetningu staðgreiðsluafsláttar.

Hver reitur hefur mismunandi áhrif á færsluna þegar þú breytir honum:

- **Breyta grunndagsetningunni** - Gjalddaga og afsláttardagsetningum er breytt eins og grunndagsetningin sé dagsetning skjalsins.
- **Breyta gjalddaga** - Aðeins gjalddaga er breytt.
- **Breyta afsláttardagsetningum** - Aðeins afsláttardagsetningum er breytt.
- **Breyta greiðsluskilmálum** - Gjalddaga er breytt samkvæmt grunndagsetningu og greiðsluskilmálum.
- **Breyta skilmálum staðgreiðsluafsláttar** - Staðgreiðsluafsláttum er breytt samkvæmt grunndagsetningu og skilmálum staðgreiðsluafsláttar.

Þegar þú hefur lokið við breytingar á greiðslustillingum skaltu velja **Loka** til að vista breytingarnar.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]