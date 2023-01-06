---
title: Samstilla eftirspurn við verðlagningarkerfi Supply Chain Management
description: Þessi grein lýsir því hvernig hægt er að nota verð vélina í Microsoft Dynamics 365 Supply Chain Management úr Microsoft Dynamics 365 Sales.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288955"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a>Samstilla eftirspurn við verðlagningarkerfi Supply Chain Management

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management felur í sér verðlagningarvél sem sér um viðskiptasamninga, verðskrár, vildarkerfi, kynningar og afslætti. Verðlagningarvélin notar flóknar reglur til að ákvarða besta verðið fyrir tiltekið tilboð eða pöntun. Þegar þú notar tvöfalda skrift notarðu annaðhvort stöðuga verðlagningu eða verðvél frá Supply Chain Management á síðunum **Tilboð** og **Pöntun** í Microsoft Dynamics 365 Sales.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Notaðu verðlagsvélina úr Supply Chain Management í Sales

1. Í Sales ferðu í **Sales \> Pantanir**.
1. Veldu **Nýtt** til að stofna nýja pöntun eða velja fyrirliggjandi pöntun í listanum **Mínar pantanir**.
1. Bæta við nýrri pöntunarlínu.
1. Ef þú ert að búa til nýja pöntun skaltu velja **Verðpöntun** í aðgerðarglugganum. Ef þú ert að uppfæra fyrirliggjandi pöntun skaltu velja **Endurreikna** í aðgerðarglugganum.
1. Eftirtaldir dálkar eru fylltir út sjálfkrafa:

    - Upplýsingar um upphæð
    - Afsláttar%
    - Afsláttur
    - Upphæð fyrir farm
    - Farmupphæð
    - Heildarskattur
    - Heildarupphæð

> [!NOTE]
> Svipað ferli gildir þegar þú býrð til tilboð.

## <a name="how-it-works"></a>Hvernig það virkar

Þegar þú stofnar pöntun í Sales er sú pöntun strax samstillt við Supply Chain Management með því að nota gildin sem færð voru inn í Sales. Þegar þú velur **Pöntunarverð** eða **Verðtilboð** í Sales reiknar Supply Chain Management út verðið fyrir hverja pöntunarlínu og heildarpöntun samkvæmt reglum verðsamnings sem eru skilgreindar í Supply Chain Management. Nýju gildin eru síðan samstillt aftur við sölu.

## <a name="set-trade-agreement-evaluation-options-in-supply-chain-management"></a>Velja valkosti fyrir mat á viðskiptasamningi í Supply Chain Management

Hægt er að skilgreina Supply Chain Management á að annaðhvort fara eftir eða hunsa verðsamningia þegar það reiknar út verð á pöntun sem var stofnuð í Sales. Fylgdu þessum skrefum til að setja upp þennan valkost.

1. Skráðu þig inn á Supply Chain Management-umhverfið þitt.
1. Opnið **Viðskiptakröfur \> Setja upp \> Færibreytur viðskiptakrafna**.
1. Á flipanum **Verð**, á flýtiflipanum **Mat verðsamnings** skal bæta við eða fjarlægja línu fyrir regluna **Handvirk færsla**, eftir þörfum. Hvort sem reglan er til staðar eða ekki stjórnar hún því hvort verðlagningarvél Supply Chain Management muni sjálfkrafa hnekkja söluverðinu sem var slegið inn í Sales.

    - Ef reglan **Handvirk færsla** *er ekki* til staðar í uppsetningu á **Mati verðsamnings** sér Supply Chain Management um verðið. Þegar notandi velur **Pöntunarverð** eða **Verðtilboð** á aðgerðasvæðinu í Sales er kallað á verðlagningarvél Supply Chain Management og skrifað er yfir söluverðið sem slegið var inn í Sales nema það jafngildi söluverðinu sem er reiknað í Supply Chain Management.
    - Ef reglan **Handvirk færsla** *er* til staðar í uppsetningu á **Mati verðsamnings** sér Sales um verðið. Komið er í veg fyrir að skrifað sé sjálfkrafa yfir söluverðið sem var slegið inn í Sales þegar notandi velur **Pöntunarverð** eða **Verðtilboð** á aðgerðasvæðinu í Sales.
    - Pöntunarlínur og tilboðslínur sem eru með gildi fyrir **Verð á einingu** og/eða **Afslátt** upp á *0* (núll) í Sales eru sérstök tilfelli. Ef viðeigandi verð verðsamnings er í boði mun Supply Chain Management *alltaf* nota það á þessa reiti óháð því hver uppsetningin á **Mat verðsamnings** er.

    Dæmi um hvert þessara tilvika er að finna í sviðsmyndunum sem fylgja.

## <a name="example-scenario-1-trade-agreement-evaluation-without-the-manual-entry-option"></a>Dæmi um aðstæður 1: Mat verðsamings án valkostsins Handvirk færsla

Í þessum aðstæðum inniheldur uppsetningin **Mat verðsamnings** í Supply Chain Management *ekki* regluna **Handvirk færsla**. Sölunotandi færir inn í pöntunarlínu sem er með söluverð sem er ekki núll í sölu og ekkert söluverð er skilgreint fyrir vöruna í Supply Chain Management.

1. Í Sales stofnar notandi pöntunarlínu sem er með gildið fyrir **Verð á einingu** sem 1 bandaríkjadalur (USD).
1. Pöntunarlínan er samstillt við Supply Chain Management með söluverð upp á 1 USD.
1. Í Sölu velur notandinn **Verðfyrirmæli** á Aðgerðasvæði.
1. Supply Chain Management leitar að viðeigandi verðum og afsláttum og reiknar svo samtölurnar. Þar sem varan er ekki með neitt söluverð í Supply Chain Management uppfærir útreikningurinn línuna þannig að hún sé með söluverðið 0 USD.
1. Nýtt söluverð línunnar er samstillt aftur til sölu.
1. Niðurstaðan er pöntunarlína í Sölu sem er með söluverð 0 USD.

## <a name="example-scenario-2-trade-agreement-evaluation-with-the-manual-entry-option"></a>Dæmi um aðstæður 2: Mat verðsamnings með valkostinum Handvirk færsla

Í þessum aðstæðum er það uppsetningin **Mat verðsamnings** í Supply Chain Management sem *inniheldur* regluna **Handvirk færsla**. Notandi sölu færir inn pöntunarlínu sem er með söluverð sem er ekki núll í sölu. Supply Chain Management inniheldur verðsamning sem setur á söluverð upp á 2 USD fyrir pantaða vöru.

1. Í Sales stofnar notandi pöntunarlínu fyrir vöru sem er með 1 USD fyrir **Verð á einingu**.
1. Pöntunarlínan er samstillt við Supply Chain Management með söluverð upp á 1 USD.
1. Í Sölu velur notandinn **Verðfyrirmæli** á Aðgerðasvæði.
1. Þar sem uppsetningin **Mat verðsamnings** í Supply Chain Management inniheldur regluna **Handvirk færsla** er söluverðinu ekki breytt, jafnvel þótt viðeigandi verðsamningur tilgreinir annað söluverð.
1. Söluverðið helst óbreytt í Sales og Supply Chain Management.

## <a name="example-scenario-3-trade-agreement-evaluation-for-an-item-that-has-a-sales-price-of-zero-in-sales"></a>Dæmi um aðstæður 3: Mat verðsamnings fyrir vöru sem er með söluverðið núll í Sales.

Í þessum aðstæðum er það uppsetningin **Mat verðsamnings** í Supply Chain Management sem *inniheldur* regluna **Handvirk færsla**. Notandi Sales slær inn pöntunarlínu sem er með söluverðið 0 (núll) í Sales. Supply Chain Management inniheldur verðsamning sem setur söluverðið á 2 USD fyrir pantaða vöru.

1. Í Sales stofnar notandi pöntunarlínu sem er með 0 USD fyrir **Verð á einingu** og 0 USD fyrir **Línuafslátt**.
1. Pöntunarlínan er samstillt við Supply Chain Management með söluverðið 0 USD.
1. Þar sem það fékk pöntunarlínu sem er með söluverð 0 (núll) kallar Supply Chain Management á verðlagningarvélina jafnvel þótt valkosturinn **Handvirk færsla** sé virkur. Verðlagningarvélin skilar söluverðinu 2 USD sem verðsamningurinn setti á og uppfærir pöntunarlínuna í Supply Chain Management.
1. Uppfært söluverð er ekki enn samstillt pöntunarlínunni í sölu.
1. Í Sölu velur notandinn **Verðfyrirmæli** á Aðgerðasvæði.
1. Pöntunarlínan í Supply Chain Management heldur söluverðinu 2 USD, sem er nú samstillt aftur í Sales. Því er gildið fyrir **Verð á einingu** í pöntunarlínunni í Sales uppfært úr 0 USD í 2 USD.
1. Í sölu skráir notandinn nýtt gildi fyrir **Línuafslátt** sem nemur 0,50 USD. Sales reiknar nú út að gildið fyrir **Skráða upphæð** fyrir línuna sé 1,50 USD.
1. Pöntunarlínan er samstillt við Supply Chain Management með gildi fyrir **Línuafslátt** sem nemur 0,50 USD.
1. Í Sölu velur notandinn **Verðfyrirmæli** á Aðgerðasvæði.
1. Engin verð eða afslættir breytast fyrir pöntunarlínuna í sölu.

## <a name="limitations"></a>Takmarkanir

Þegar dálkar í Sales eru fylltir út gildir eftirfarandi takmörkun:

- Uppsetning gjalds og úthlutunar gjalds í Supply Chain Management er ekki endurtekin í Sales.
- Verðlagning tekur ekki tillit til sérstakrar smásöluverðlagningar sem er tilgreind í dálknum **Smásölurás** á síðu sölupöntunarlínu í Supply Chain Management.
- Afslættir sem eru skilgreindir í hlutanum **Stjórnun afsláttar** af Supply Chain Management eru ekki skoðaðir.
- Verðlagning tekur ekki mið af sölusamningum.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
