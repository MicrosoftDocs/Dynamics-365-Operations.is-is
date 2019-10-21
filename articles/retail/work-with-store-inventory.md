---
title: Birgðastjórnun verslunar
description: Þetta efnisatriði lýsir gerðum af skjölum sem hægt er að nota til að stjórna birgðum.
author: rubencdelgado
manager: AnnBe
ms.date: 04/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c5da94e02b2381bbd058221567172cd428931c45
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024684"
---
# <a name="store-inventory-management"></a>Birgðastjórnun verslunar

[!include [banner](includes/banner.md)]

Þegar unnið er með birgðir í Dynamics 365 Retail og POS forritið er notað, er mikilvægt að hafa í huga að POS veitir takmarkaðan stuðning fyrir birgðavíddir og ákveðnar gerðir af birgðavörum.

POS-lausnin styður ekki eftirfarandi vöruafbrigði:

- Uppskriftarvörur (nema afurðarsett, sem nota suma hluti af uppskriftarrammanum)
- Vörur framleiðsluþyngdar
- Runustýrðar vörur

Sem stendur styður POS-forritið ekki eftirfarandi rakningarvíddir í POS:

- Runurakningarvídd
- Eigandavídd

POS-lausnin veitir takmarkaðan stuðning fyrir eftirfarandi víddir. Takmarkaður stuðningur bendir til þess að POS geti færi sumar þessara vídda sjálfkrafa inn í birgðafærslur sem byggjast á skilgreiningu fyrir uppsetningu vöruhúss/verslunar. POS styður víddirnar ekki að fullu eins og þær eru studdar ef sölufærsla er slegin handvirkt inn í ERP. 

- **Staðsetning vöruhúss** - Notendur hafa ekki möguleikann á að stjórna staðsetningu á viðtökuvöruhúsi fyrir vörur sem eru mótteknar í vöruhúsi verslunar þegar verslunin hefur ekki verið skilgreind til að nota ferli vöruhúsakerfis. Sjálfgefin staðsetning móttöku skilgreind í vöruhúsi verslunar verður notuð fyrir þessar vörur. Ef ferli fyrir vöruhúsakerfi hefur verið virkjað fyrir verslunina, verður takmarkaður stuðningur sem biður notanda um að velja móttökustaðsetningu fyrir allri móttökunni ræstur. Vörur seldar úr versluninni verða alltaf seldar úr sjálfgefinni staðsetningu smásölu eins og hún er skilgreind í uppsetningu vöruhúss. Staðsetningin til að stjórna skilum á birgðum er hægt að stjórna í gegnum sjálfgefna skilgreiningu skilastaðsetningar í vöruhúsi verslunar eða samkvæmt ástæðukóðum skila eins og þeir eru skilgreindir í reglu skilastaðsetningar.
- **Númeraplata** - Númeraplötur eiga aðeins við þegar **Nota ferli vöruhúsakerfis** hefur verið virkjað í vörunni og vöruhúsi verslunar. Á sölustað, ef tekið er á móti birgðum í vöruhúsi verslunar þar sem ferli vöruhúsakerfis hefur verið virkjað, og í staðsetningu sem valin er til að taka á móti vörunni er bundin við staðsetningarforstillingu sem krefst stjórnunar á númeraplötu, mun forrit sölustaðar kerfisbundið bæta númeraplötu við móttökulínuna. Notendur á sölustað hafa ekki möguleika á því að breyta eða stjórna þessum gögnum númeraplötu. Ef þörf er á fullri stjórnun á númeraplötum er mælt með því að verslunin noti farsímaforrit vöruhúsakerfis eða ERP-biðlara bakvinnslu til að stjórna móttöku á þessum vörum.
- **Raðnúmer** - Forrit sölustaðar er með takmarkaðan stuðning fyrir stakt raðnúmer sem á að skrá í sölulínu færslu fyrir pantanir sem eru stofnaðar í sölustað með númeruðum vörum. Þetta raðnúmer er ekki sannprófað gagnvart skráðum raðnúmerum sem eru nú þegar í birgðum. Ef sölupöntun er stofnuð í rás símavers eða uppfyllt í gegnum ERP og mörg raðnúmer eru skráð á staka sölulínu í uppfyllingarferlinu í ERP, verður ekki hægt að nota eða sannprófa þessi raðnúmer ef unnið er úr skilum á sölustað fyrir þessar pantanir.
- **Birgðastaða** - Fyrir vörur sem nota ferli vöruhúsakerfis og þurfa birgðastöðu, verður ekki hægt að stilla eða breyta þessum stöðureit í gegnum forrit sölustaðar. Sjálfgefin birgðastaða eins og hún er skilgreind í skilgreiningu fyrir vöruhús verslunar verður notuð þegar vörur eru mótteknar í birgðum.

> [!NOTE]
> Öll fyrirtæki verða að prófa vöruafbrigðin í gegnum POS í þróun eða prófunarumhverfi áður en þau eru innleidd í framleiðslu. Prófaðu vörurnar þínar með því að framkvæma reglulegar sölufærslur fyrir „staðgreiða og afhenda“ og stofna pantanir viðskiptavinar (ef á við) í gegnum POS með vörunum þínum. Prófun verður að fela í sér að keyra ítarleg bókunarferli uppgjörs í prófunarumhverfinu þínu og staðfesta að engin vandamál séu til staðar.
>
> Stillingar á vörum á þann hátt sem er ekki studdur af POS forritinu, án almennilegrar prófunar, getur leitt til þess að bókunarferli uppgjörs mistakist í framleiðslu án auðveldrar leiðar til að lagfæra vandamálið. Sérstillingar samstarfsaðila eða viðskiptavinar fyrir forritið er einnig hægt að hugleiða til að leyfa þessum bókunarferlum að klára án vandamála. Ef ekki er þörf á sérstillingum þarf fyrirtækið að tryggja að vöruafbrigði varanna þinna hafi verið gerðar á þann hátt sem studd er með stöðluðu POS-forriti/stofnun pöntunar/bókunarferli uppgjörs.

## <a name="purchase-orders"></a>Innkaupapantanir

Innkaupapantanir eru stofnaðar á aðalskrifstofu. Ef vöruhús smásölu er innifalið í haus innkaupapöntunar er hægt að taka við pöntuninni í verslun með því að nota Modern POS (MPOS) eða Cloud POS í gegnum aðgerðina **Tiltekt/móttaka**. Eftir að magn sem er móttekið í verslun er slegið inn í reitinn **Móttaka nú** á sölustað fyrir skjal innkaupapöntunar, er hægt að vista það staðbundið eða ráðstafað. Vistun þessara gagna á staðnum hefur engin áhrif á birgðir á lager. Aðeins ætti að vista ef notandi er ekki tilbúinn til að bóka móttökuna í höfuðstöðvum og þarf aðeins leið til að geyma tímabundið áður innslegnu gögnin **Móttaka nú**. Þetta vistar gögnin staðbundið í gagnagrunni rásar notanda fyrir það sem er móttekið núna. Þegar unnið er úr skjalinu með valkostinum **Ráðstafa** eru gögnin **Móttekið nú** send til höfuðstöðva og móttaka innkaupapöntunar verður bókuð. 

## <a name="transfer-orders"></a>Flutningspantanir

Flutningspöntun getur tilgreint að ákveðin verslun sé staðsetning sem hægt er að senda vörurnar úr eða staðsetning sem birgðir verða mótteknar í. Ef notandi sölustaðar er afhendingarvöruhús fyrir flutningspöntun getur hann slegið inn magnið fyrir **Senda núna** úr sölustað. Gögnin sem afhendingarverslun slær inn er hægt að vista staðbundið eða ráðstafa. Þegar vistað er á staðnum eru engar uppfærslur gerðar á skjali flutningspöntunar í höfuðstöðvum. Aðeins ætti að vista ef notandi er ekki tilbúinn til að bóka afhendingu í höfuðstöðvum og þarf leið til að geyma tímabundið áður innslegnu gögnin **Afhenda núna**. Eftir að verslun er tilbúin til að staðfesta sendingu ætti að velja valkostinn **Ráðstafa**. Þetta bókar sendingu á flutningspöntun í höfuðstöðvum svo að viðtökuvöruhús geti nú móttekið. 

Ef notandi sölustaðar er viðtökuvöruhús fyrir flutningspöntun getur hann slegið inn magnið fyrir **Móttaka núna** úr sölustað. Gögnin sem móttökuverslun slær inn er hægt að vista staðbundið eða ráðstafa. Aðeins ætti að vista ef notandi er ekki tilbúinn til að bóka móttökuna í höfuðstöðvum og þarf leið til að geyma tímabundið áður innslegnu gögnin **Móttaka nú**. Þetta vistar gögnin staðbundið í gagnagrunni rásar notanda fyrir það sem er móttekið núna. Þegar unnið er úr skjalinu með valkostinum **Ráðstafa** eru gögnin **Móttekið nú** send til höfuðstöðva og móttaka flutningspöntunar verður bókuð. Mikilvægt er að hafa í huga að móttökuverslun takmarkast við að geta aðeins ráðstafað mótteknu magni sem jafngildir eða er minna en sent magn. Tilraun til að taka á móti magni flutningspöntunar sem hefur ekki verið afhent leiðir til villu og móttaka verður ekki staðfest í höfuðstöðvum.

## <a name="stock-counts"></a>Birgðatalning

Birgðatalningar geta verið annaðhvort áætlaðar eða óskipulagðar. Áætluð birgðatalning – Þessar birgðatalningar eru gerðar að frumkvæði aðalskrifstofunnar og það er hún sem ákveður hvaða vörur á að telja. Aðalskrifstofa útbýr talningarskjal og sendir versluninni það og þar eru upplýsingar um birgðastöðu færðar inn í MPOS eða Cloud POS. Óundirbúin birgðatalning er hafin í verslun og magn raunbirgða á lager er uppfært í annaðhvort MPOS eða Cloud POS. Ólíkt áætlaðri birgðatalningu hafa óundirbúnar birgðatalningar ekki fyrirfram skilgreindan lista yfir vörur. Þegar birgðatalningu af annarri hvorri gerð er lokið er henni ráðstafað og send til aðalskrifstofu. Á aðalskrifstofu er talningin villuleituð og bókuð sem aukaskref.

## <a name="inventory-lookup"></a>Birgðauppfletting

Núverandi afurðarmagn á lager fyrir margar verslanir og vöruhús er hægt að skoða á síðunni **Uppfletting á birgðum**. Fyrir utan núverandi lagermagn má skoða tiltækt magn loforðs (ATP) um fyrir hverja einstaka verslun. Til að gera það skal velja þá verslun sem á að skoða ATP fyrir og smella svo á **Sýna framboð verslunar**.
