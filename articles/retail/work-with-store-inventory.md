---
title: Birgðastjórnun verslunar
description: Þetta efnisatriði lýsir gerðum af skjölum sem hægt er að nota til að stjórna birgðum.
author: rubencdelgado
manager: AnnBe
ms.date: 01/18/2019
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
ms.openlocfilehash: 02f8afbe3bb6f94c66a8b5aa02531c219adc3963
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "339235"
---
# <a name="store-inventory-management"></a>Birgðastjórnun verslunar

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir gerðum af skjölum sem hægt er að nota til að stjórna birgðum.

Hægt er að nota eftirfarandi gerðir af skjölum til að stjórna birgðum fyrirtækisins.

Þegar unnið er með birgðir í Dynamics 365 for Retail og POS forritið er notað, er mikilvægt að hafa í huga að POS veitir takmarkaðan stuðning fyrir birgðavíddir og ákveðnar gerðir af birgðavörum.  

POS-lausnin styður ekki eftirfarandi vöruafbrigði:
- Uppskriftarvörur (nema afurðarsett, sem nota suma hluti af uppskriftarrammanum)
- Vörur framleiðsluþyngdar
- Runustýrðar vörur

Sem stendur styður POS-forritið ekki eftirfarandi rakningarvíddir í POS:
- Runurakningarvídd
- Eigandavídd

POS-lausnin veitir takmarkaðan stuðning fyrir eftirfarandi víddir. Takmarkaður stuðningur bendir til þess að POS geti færi sumar þessara vídda sjálfkrafa inn í birgðafærslur sem byggjast á skilgreiningu fyrir uppsetningu vöruhúss/verslunar. POS styður víddirnar ekki að fullu eins og þær eru studdar ef sölufærsla er slegin handvirkt inn í ERP. 

- Staður
- Númeraplata (á aðeins við þegar **Nota ferli vöruhúsakerfis** hefur verið virkjað í vörunni og vöruhúsi verslunar)
- Raðnúmer
- Birgðastaða

> [!NOTE]
> Öll fyrirtæki verða að prófa vöruafbrigðin í gegnum POS í þróun eða prófunarumhverfi áður en þau eru innleidd í framleiðslu. Prófaðu vörurnar þínar með því að framkvæma reglulegar sölufærslur fyrir „staðgreiða og afhenda“ og stofna pantanir viðskiptavinar (ef á við) í gegnum POS með vörunum þínum. Prófun verður að fela í sér að keyra ítarleg bókunarferli uppgjörs í prófunarumhverfinu þínu og staðfesta að engin vandamál séu til staðar.
> Stillingar á vörum á þann hátt sem er ekki studdur af POS forritinu, án almennilegrar prófunar, getur leitt til þess að bókunarferli uppgjörs mistakist í framleiðslu án auðveldrar leiðar til að lagfæra vandamálið. Sérstillingar samstarfsaðila eða viðskiptavinar fyrir forritið er einnig hægt að hugleiða til að leyfa þessum bókunarferlum að klára án vandamála. Ef ekki er þörf á sérstillingum þarf fyrirtækið að tryggja að vöruafbrigði varanna þinna hafi verið gerðar á þann hátt sem studd er með stöðluðu POS-forriti/stofnun pöntunar/bókunarferli uppgjörs.

## <a name="purchase-orders"></a>Innkaupapantanir

Innkaupapantanir eru stofnaðar á aðalskrifstofu. Ef vöruhús smásölu er innifalið í haus innkaupapöntunar er hægt að taka við pöntuninni í verslun með því að nota Modern POS (MPOS) eða Cloud POS í Microsoft Dynamics 365 for Retail. Eftir að umbeðið magn hefur verið móttekið í versluninni er hægt að vista það staðbundið fyrir frekari breytingar. Einnig er hægt að ráðstafa magninu og senda það á aðalskrifstofu. Á aðalskrifstofunni birtist magn sem var móttekið í verslun í Dynamics 365 for Retail í reitnum **Móttaka núna** á innkaupapöntuninni.

## <a name="transfer-orders"></a>Flutningspantanir

Flutningspöntun getur tilgreint að ákveðin verslun sé staðsetning sem hægt er að senda vörurnar úr. Í þessu tilfelli birtist flutningspöntun í verslun sem beiðni um tiltekt í MPOS eða Cloud POS. Eftir að umbeðið magn hefur verið tekið til er því ráðstafað og sent til aðalskrifstofu. Á aðalskrifstofunni birtist magn sem var móttekið í verslun í Dynamics 365 for Retail í reitnum **Senda núna** á flutningspöntuninni. Flutningspöntun getur tilgreint að ákveðin verslun sé staðsetning sem hægt er að senda vörurnar til. Í þessu tilfelli birtist flutningspöntun í verslun sem beiðni um móttöku í MPOS eða Cloud POS. Eftir að umbeðið magn hefur verið móttekið í versluninni er hægt að vista það staðbundið fyrir frekari breytingar. Einnig er hægt að ráðstafa magninu og senda það á aðalskrifstofu. Á aðalskrifstofunni birtist magn sem var móttekið í verslun í Dynamics 365 for Retail í reitnum **Móttaka núna** á flutningspöntun.

## <a name="stock-counts"></a>Birgðatalning

Birgðatalningar geta verið annaðhvort áætlaðar eða óskipulagðar. Áætluð birgðatalning – Þessar birgðatalningar eru gerðar að frumkvæði aðalskrifstofunnar og það er hún sem ákveður hvaða vörur á að telja. Aðalskrifstofa útbýr talningarskjal og sendir versluninni það og þar eru upplýsingar um birgðastöðu færðar inn í MPOS eða Cloud POS. Óundirbúin birgðatalning er hafin í verslun og magn raunbirgða á lager er uppfært í annaðhvort MPOS eða Cloud POS. Ólíkt áætlaðri birgðatalningu hafa óundirbúnar birgðatalningar ekki fyrirfram skilgreindan lista yfir vörur. Þegar birgðatalningu af annarri hvorri gerð er lokið er henni ráðstafað og send til aðalskrifstofu. Á aðalskrifstofu er talningin villuleituð og bókuð.

## <a name="inventory-lookup"></a>Birgðauppfletting

Gildandi magn vöru á lager fyrir margar verslanir og vöruhús má skoða á síðunni Uppflettisvæði birgða. Fyrir utan núverandi lagermagn má skoða tiltækt magn loforðs (ATP) um fyrir hverja einstaka verslun. Til að gera það skal velja þá verslun sem á að skoða ATP fyrir og smella svo á **Sýna framboð verslunar**.
