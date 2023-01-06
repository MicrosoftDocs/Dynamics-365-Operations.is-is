---
title: Flytja PTC-gögn úr Data Integrator í tvöfalda skráningu
description: Þessi grein lýsir hvernig á að flytja PTC-gögn úr Data Integrator í tvöfalda skráningu.
author: RamaKrishnamoorthy
ms.date: 02/01/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-26
ms.openlocfilehash: bbf5a7c2f409003816e2becf1a58ee7d7d5aafb2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289081"
---
# <a name="migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Flytja PTC-gögn úr Data Integrator í tvöfalda skráningu

[!include [banner](../../includes/banner.md)]

Prospect to cash lausnin sem er í boði fyrir Data Integrator er ekki samhæf við tvöfalda skráningu. Ástæðan fyrir þessu er vísirinn msdynce_AccountNumber á töflu lykla sem fylgdi Prospect to cash lausninni. Ef þessi vísir er til getur þú ekki búið til sama númer viðskiptavinalykils í tveimur mismunandi lögaðilum. Þú getur annaðhvort byrjað frá grunni með tvöfaldri skráningu með því að flytja gögn Prospect to cash úr Data Integrator í tvöfalda skráningu eða þú getur sett upp útgáfuna „dorman“ af Prospect to cash lausninni. Þessi grein fjallar um báðar þessar nálganir.

## <a name="install-the-last-dorman-version-of-the-data-integrator-prospect-to-cash-solution"></a>Settu upp síðustu „dorman“-útgáfu af lausn Prospect to cash fyrir Data Integrator.

**P2C-útgáfa 15.0.0.2** er talin síðasta „dorman“-útgáfa Prospect to cash lausnar fyrir Data Integrator. Hægt er að hlaða niður af [FastTrack for Dynamics 365](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/P2C).

Þú þarft að setja upp handvirkt. Eftir uppsetningu er allt nákvæmlega eins, nema msdynce_AccountNumber-yfirlitið er fjarlægt.

## <a name="steps-to-migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Skref til að flytja PTC-gögn úr Data Integrator í tvöfalda skráningu

Til að flytja PTC-gögn úr Data Integrator í tvöfalda skráningu skal fylgja þessum skrefum.

1. Keyrið Data Integrator-verk PTC til að gera eina fulla samstillingu að lokum. Á þennan hátt er tryggt að bæði kerfi (forrit fjármála- og reksturs og Customer Engagement-forrit) séu með öll gögn.
2. Til að hjálpa til við að koma í veg fyrir hugsanlegt gagnatap er Prospect to cash gögn flutt út úr Microsoft Dynamics 365 Sales í Excel-skrá eða skrá með aðskildum gildum (CSV). Flytja út gögn úr eftirfarandi einingum:

    - [Lykill](#account-table)
    - [Tengiliður](#contact-table)
    - [Reikningur](#invoice-table)
    - Reikningsfæra vörur
    - [Pöntun](#order-table)
    - [Panta vörur](#order-products-table)
    - [Afurðir](#products-table)
    - [Tilboð](#quote-and-quote-product-tables)
    - [Tilboð í afurðir](#quote-and-quote-product-tables)

3. Fjarlægið Prospect to cash lausn úr Sales-umhverfi. Þetta skref fjarlægir dálka og samsvarandi gögn sem viðfangið til að reiðufjárlausn sé kynnt.
4. Setja upp lausn tvöfaldrar skráningar.
5. Stofnið tengingu tvöfaldrar skráningar á milli forriti fjármála- og reksturs og forrits viðskiptavinar fyrir einn eða fleiri lögaðila.
6. Virkið töfluvörpun tvöfaldrar skráningar og keyrið fyrstu samstillinguna fyrir áskild tilvísunargögn. (Frekari upplýsingar er að finna í [Hvað skal hafa í huga við fyrstu samstillingu](initial-sync-guidance.md).) Dæmi um áskilin gögn eru m.a. viðskiptavinaflokkar, greiðsluskilmálar og greiðsluáætlanir. Ekki skal virkja vörpun tvöfaldrar skráningar fyrir töflur sem krefast frumstillingar, t.d. töflur lykla, tilboðs, tilboðslínu, pöntunar og pöntunarlínu.
7. Í forriti viðskiptavinar skal opna **Ítarlegar stillingar \> Kerfisstillingar \> Gagnastjórnun \> Afrita greiningarreglur** og slökkva á öllum reglum.
8. Frumstillið töflurnar sem eru gefnar upp í skrefi tvö. Frekari upplýsingar er að finna í eftirstandandi hlutum í þessari grein.
9. Opnið fjármála- og reksturs-forritið og virkið töfluvarpanir, t.d. töfluvarpanir lykla, tilboðs, tilboðslínu, pöntunar og pöntunarlínu. Keyrið síðan fyrstu samstillingu. (Frekari upplýsingar er að finna [Hvað skal hafa í huga við fyrstu samstillingu](initial-sync-guidance.md).) Þetta ferli mun samstilla viðbótarupplýsingar úr fjármála og rekstrarforritinu, t.d. vinnslustöðu, sendingu og reikningsheimilisfang, svæði og vöruhús.

## <a name="account-table"></a>Lyklatafla

1. Í dálkinn **Fyrirtæki** skal færa inn heiti fyrirtækisins, til dæmis **USMF**.
2. Í dálkinn **Gerð vensla** skal færa inn **Viðskiptavin** sem fast gildi. Ekki er víst að hægt sé að flokka hverja reikningsfærslu sem viðskiptavin í viðskiptagrunni.
3. Í dálkinn **Kenni viðskiptavinaflokks** skal færa inn númer viðskiptavinaflokks úr forriti fjármála- og reksturs. Sjálfgefið gildi úr Prospect to cahs lausn er **10**.
4. Ef notuð er PTC-lausnin án sérstillingar á **Reikningsnúmeri** skal færa inn gildi fyrir **Reikningsnúmer** í dálkinn **Aðilanúmer**. Ef það eru sérstillingar og aðilanúmerið er óþekkt skaltu ná í þær upplýsingar úr forrit fjármála- og rekstursinu.

## <a name="contact-table"></a>Taflan Tengiliður

1. Í dálkinn **Fyrirtæki** skal færa inn heiti fyrirtækisins, til dæmis **USMF**.
2. Stillið eftirfarandi dálka út frá **IsActiveCustomer** gildinu í CSV-skrá:

    - Ef **IsActiveCustomer** er stillt á **Já** í CSV-skrá skal stilla dálkinn **Seljanlegt** á **Já**. Í dálkinn **Kenni viðskiptavinaflokks** skal færa inn númer viðskiptavinaflokks úr forriti fjármála- og reksturs. Sjálfgefið gildi úr Prospect to cahs lausn er **10**.
    - Ef **IsActiveCustomer** er stillt á **Nei** í CSV-skrá skal stilla dálkinn **Seljanlegt** á **Nei** og stilla dálkinn **Tengiliður fyrir** á **Viðskiptavinur**.

3. Ef notuð er PTC-lausnin án sérstillingar á **Númer tengiliðar** skal stilla eftirfarandi dálka:

    - Yfirfærið númer tengiliðar á CSV-skrána (**msdynce\_contactnumber**) á tengiliðanúmerið í töflunni **Tengiliður** (**msdyn\_contactnumber**).
    - Notið gildið úr töflunni **Númer tengiliðar** í dálkinn **Aðilanúmer**.
    - Notið gildin úr töflunni **Númer tengiliðar** í dálkinum **Lykilnúmer/kenni tengiliðar**.

## <a name="invoice-table"></a>Reikningstafla

Vegna þess að gögnin úr töflunni **Reikningur** eru hönnuð til að flæða í eina átt, úr forriti fjármála- og reksturs til forrits viðskiptavinar, gerist ekki þörf á frumstillingu. Keyrið fyrstu samstillingu til að flytja öll áskilin gögn úr forriti fjármála- og reksturs í forrit viðskiptavinar. Frekari upplýsingar má finna á [Hvað skal hafa í huga við fyrstu samstillingu](initial-sync-guidance.md).

## <a name="order-table"></a>Pöntunartafla

1. Í dálkinn **Fyrirtæki** skal færa inn heiti fyrirtækisins, til dæmis **USMF**.
2. Afritið gildi dálksins **Pöntunarkenni** í CSV-skránni í dálkinn **Sölupöntunarnúmer**.
3. Afritið gildi dálksins **Viðskiptavinur** í CSV-skránni í dálkinn **Númer viðskiptavinareiknings**.
4. Afritið gildið úr dálkinum **Sendist til svæðis/lands** í CSV-skránni í dálkinn **Sendist til lands/svæðis**. Dæmi um þetta gildi eru m.a. **US** og **Bandaríkin**.
5. Stillið dálkinn **Umbeðin móttökudagsetning**. Ef ekki er hægt notuð móttökudagsetning skal nota dálkana **Umbeðinn afhendingardag**, **Dagsetningu uppfyllingar** og **Dagsetning innsendingar** í CSV-skránni. Dæmi um þetta gildi er **2020-03-27T00:00:00Z**.
6. Stillið dálkinn **Tungumál**. Dæmi um þetta gildi er **en-us**.
7. Stillið dálkinn **Gerð pöntunar** með því að nota dálkinn **Vörutengd**.

## <a name="order-products-table"></a>Töflur afurðapöntunar

- Í dálkinn **Fyrirtæki** skal færa inn heiti fyrirtækisins, til dæmis **USMF**.

## <a name="products-table"></a>Afurðatöflur

Vegna þess að gögnin úr töflunni **Afurðir** eru hönnuð til að flæða í eina átt, úr forriti fjármála- og reksturs til forrits viðskiptavinar, gerist ekki þörf á frumstillingu. Keyrið fyrstu samstillingu til að flytja öll áskilin gögn úr forriti fjármála- og reksturs í forrit viðskiptavinar. Frekari upplýsingar má finna á [Hvað skal hafa í huga við fyrstu samstillingu](initial-sync-guidance.md).

## <a name="quote-and-quote-product-tables"></a>Töflur tilboðs og afurðartilboðs

Fyrir töfluna **Tilboð** skal fylgja leiðbeiningunum í hlutanum [Pöntunartafla](#order-table) fyrr í þessari grein. Fyrir töfluna **Afurðartilboð** skal fylgja leiðbeiningunum í hlutanum [Tafla afurðapöntunar](#order-products-table).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

