---
title: Samstilla eftirspurn við verðlagningarkerfi Supply Chain Management
description: Þessi grein lýsir því hvernig á að nota verðlagningarvélina í Microsoft Dynamics 365 Supply Chain Management frá Microsoft Dynamics 365 Sala.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 727e60ceee3f5c8c33d2da93128eedc1dc7bcb9f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288955"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a>Samstilla eftirspurn við verðlagningarkerfi Supply Chain Management

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management felur í sér verðlagningarvél sem sér um viðskiptasamninga, verðskrár, vildarkerfi, kynningar og afslætti. Verðlagningarvélin notar flóknar reglur til að ákvarða besta verðið fyrir tiltekið tilboð eða pöntun. Þegar þú notar tvískrift notarðu annað hvort fasta verðlagningu eða verðlagningarvélina frá Supply Chain Management á **Tilvitnun** og **Panta** síður inn Microsoft Dynamics 365 Sala.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Notaðu verðlagsvélina úr Supply Chain Management í Sales

1. Í Sales ferðu í **Sales \> Pantanir**.
1. Veldu **Nýtt** til að stofna nýja pöntun eða velja fyrirliggjandi pöntun í listanum **Mínar pantanir**.
1. Bæta við nýrri pöntunarlínu.
1. Ef þú ert að búa til nýja pöntun skaltu velja **Verðpöntun** á aðgerðasvæðinu. Ef þú ert að uppfæra fyrirliggjandi pöntun skaltu velja **Endurreikna** í aðgerðarglugganum.
1. Eftirtaldir dálkar eru fylltir út sjálfkrafa:

    - Upplýsingar um upphæð
    - Afsláttar%
    - Afsláttur
    - Upphæð fyrir farm
    - Farmupphæð
    - Heildarskattur
    - Heildarupphæð

> [!NOTE]
> Svipað ferli á við þegar þú býrð til tilboð.

## <a name="how-it-works"></a>Hvernig það virkar

Þegar þú stofnar pöntun í Sölu er sú pöntun samstundis samstillt við Supply Chain Management með því að nota gildin sem þú færðir inn í Sales. Þegar þú velur **Verðpöntun** eða **Verðtilboð** í Sölu, reiknar Supply Chain Management út verðið fyrir hverja pöntunarlínu og heildarpöntunina, byggt á viðskiptasamningsreglum sem eru skilgreindar í Supply Chain Management. Nýju útreiknuðu gildin eru síðan samstillt aftur við sölu.

## <a name="set-trade-agreement-evaluation-options-in-supply-chain-management"></a>Stilltu valmöguleika fyrir mat á viðskiptasamningum í Supply Chain Management

Hægt er að stilla Supply Chain Management til að annað hvort virða eða hunsa viðskiptasamninga þegar hún reiknar út verð pöntunar sem var stofnuð í Sales. Fylgdu þessum skrefum til að setja upp þennan valkost.

1. Skráðu þig inn í Supply Chain Management umhverfið þitt.
1. Opnið **Viðskiptakröfur \> Setja upp \> Færibreytur viðskiptakrafna**.
1. Á **Verð** flipa, á **Viðskiptasamningsmat** Flýtiflipa, bæta við eða fjarlægja línuna fyrir **Handvirk færsla** stefnu eins og þú vilt. Tilvist eða fjarvera þessarar stefnu stjórnar því hvort verðlagningarvél Supply Chain Management muni sjálfkrafa yfirbuga söluverðið sem var slegið inn í Sales.

    - Ef **Handvirk færsla** stefnu *er ekki* til staðar í **Viðskiptasamningsmat** uppsetningu, Supply Chain Management er verðmeistarinn. Þegar notandi velur **Verðpöntun** eða **Verðtilboð** á aðgerðarrúðunni í sölu er verðlagningarvél Supply Chain Management kallað og söluverðið sem var fært í Sales er skrifað yfir, nema það sé jafnt söluverði sem er reiknað í Supply Chain Management.
    - Ef **Handvirk færsla** stefnu *er* til staðar í **Viðskiptasamningsmat** uppsetning, Sala er verðmeistarinn. Komið er í veg fyrir að söluverðið sem var slegið inn í Sölu sé skrifað yfir sjálfkrafa þegar notandi velur **Verðpöntun** eða **Verðtilboð** á aðgerðarrúðunni í sölu.
    - Pöntunarlínur og tilboðslínur sem hafa a **Verð á einingu** og/eða **Afsláttur** verðmæti á *0* (núll) í Sala er meðhöndluð sem sértilvik. Ef viðeigandi viðskiptasamningsverð er tiltækt mun Supply Chain Management gera það *alltaf* beita því á þessum sviðum, óháð því **Viðskiptasamningsmat** uppsetningu.

    Fyrir dæmi um hvert þessara tilvika, sjá sviðsmyndir sem fylgja.

## <a name="example-scenario-1-trade-agreement-evaluation-without-the-manual-entry-option"></a>Dæmi atburðarás 1: Mat á viðskiptasamningi án valkostins Handvirk færslu

Í þessari atburðarás er **Viðskiptasamningsmat** uppsetningu í Supply Chain Management *gerir ekki* fela í sér **Handvirk færsla** stefnu. Sölunotandi slær inn pöntunarlínu sem hefur söluverð sem er ekki núll í sölu og ekkert söluverð er skilgreint fyrir vöruna í Supply Chain Management.

1. Í Sales býr notandi til pöntunarlínu sem hefur a **Verð á einingu** verðmæti 1 Bandaríkjadalur (USD).
1. Pöntunarlínan er samstillt við Supply Chain Management með söluverðinu 1 USD.
1. Í Sales velur notandinn **Verðpöntun** á aðgerðasvæðinu.
1. Aðfangakeðjustjórnun leitar að viðeigandi verði og afslætti og reiknar síðan heildartölur. Vegna þess að varan hefur ekkert söluverð í Supply Chain Management uppfærir útreikningurinn línuna þannig að hún hafi söluverðið 0 USD.
1. Nýtt söluverð línunnar er samstillt aftur við sölu.
1. Niðurstaðan er pöntunarlína í Sölu sem hefur söluverðið 0 USD.

## <a name="example-scenario-2-trade-agreement-evaluation-with-the-manual-entry-option"></a>Dæmi atburðarás 2: Mat á viðskiptasamningi með valkostinum Handvirk færslu

Í þessari atburðarás er **Viðskiptasamningsmat** uppsetningu í Supply Chain Management *gerir* fela í sér **Handvirk færsla** stefnu. Sölunotandi slær inn pöntunarlínu sem hefur söluverð sem er ekki núll í sölu. Aðfangakeðjustjórnun felur í sér viðskiptasamning sem setur söluverð 2 USD fyrir pantaða vöru.

1. Í Sales býr notandi til pöntunarlínu fyrir vöru sem hefur a **Verð á einingu** gildi 1 USD.
1. Pöntunarlínan er samstillt við Supply Chain Management með söluverðinu 1 USD.
1. Í Sales velur notandinn **Verðpöntun** á aðgerðasvæðinu.
1. Vegna þess að **Viðskiptasamningsmat** uppsetning í Supply Chain Management inniheldur **Handvirk færsla** stefnu, breytist söluverðið ekki, jafnvel þó að viðeigandi viðskiptasamningur tilgreini annað söluverð.
1. Söluverð helst óbreytt í Sölu og í Supply Chain Management.

## <a name="example-scenario-3-trade-agreement-evaluation-for-an-item-that-has-a-sales-price-of-zero-in-sales"></a>Dæmi atburðarás 3: Mat á viðskiptasamningi fyrir vöru sem hefur söluverð núll í sölu

Í þessari atburðarás er **Viðskiptasamningsmat** uppsetningu í Supply Chain Management *gerir* fela í sér **Handvirk færsla** stefnu. Sölunotandinn slær inn pöntunarlínu sem hefur söluverðið 0 (núll) í sölu. Aðfangakeðjustjórnun felur í sér viðskiptasamning sem setur söluverð 2 USD fyrir pantaða vöru.

1. Í Sales býr notandi til pöntunarlínu sem hefur a **Verð á einingu** gildi 0 USD og a **Línuafsláttur** gildi 0 USD.
1. Pöntunarlínan er samstillt við Supply Chain Management með söluverðinu 0 USD.
1. Vegna þess að það fékk pöntunarlínu sem hefur söluverðið 0 (núll), kallar Supply Chain Management verðlagningarvélina, jafnvel þó að **Handvirk færsla** valmöguleikinn er virkur. Verðlagsvélin skilar söluverði 2 USD sem er komið á með viðskiptasamningnum og uppfærir pöntunarlínuna í Supply Chain Management.
1. Uppfært söluverð er ekki enn samstillt við pöntunarlínuna í Sölu.
1. Í Sales velur notandinn **Verðpöntun** á aðgerðasvæðinu.
1. Pöntunarlínan í Supply Chain Management heldur söluverði sínu 2 USD, sem er nú samstillt aftur við sölu. Þess vegna er **Verð á einingu** gildi pöntunarlínunnar í Sales er uppfært úr 0 USD í 2 USD.
1. Í Sales slær notandi inn nýtt **Línuafsláttur** gildi 0.50 USD. Sala reiknar nú að **Framlengd upphæð** gildi fyrir línuna er 1.50 USD.
1. Pöntunarlínan er samstillt við Supply Chain Management með a **Línuafsláttur** gildi 0.50 USD.
1. Í Sales velur notandinn **Verðpöntun** á aðgerðasvæðinu.
1. Engin verð eða afslættir breytast fyrir pöntunarlínuna í sölu.

## <a name="limitations"></a>Takmarkanir

Þegar dálkar í Sales eru fylltir út gildir eftirfarandi takmörkun:

- Uppsetning gjalds og úthlutunar gjalds í Supply Chain Management er ekki endurtekin í Sales.
- Verðlagning tekur ekki tillit til sérstakrar smásöluverðlagningar sem er tilgreind í dálknum **Smásölurás** á síðu sölupöntunarlínu í Supply Chain Management.
- Afslættir sem eru skilgreindir í hlutanum **Stjórnun afsláttar** af Supply Chain Management eru ekki skoðaðir.
- Verðlagning tekur ekki mið af sölusamningum.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
