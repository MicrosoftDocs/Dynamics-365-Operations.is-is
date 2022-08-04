---
title: Flytja PTC-gögn úr Data Integrator í tvöfalda skráningu
description: Þessi grein lýsir því hvernig á að flytja Prospect til Cash gögn frá Data Integrator yfir í tvískrif.
author: RamaKrishnamoorthy
ms.date: 02/01/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-26
ms.openlocfilehash: 91cc0e59405bc085e09f01f05ef02e4a0260481e
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111895"
---
# <a name="migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Flytja PTC-gögn úr Data Integrator í tvöfalda skráningu

[!include [banner](../../includes/banner.md)]

Prospect to cash lausnin sem er í boði fyrir Data Integrator er ekki samhæf við tvískrift. Ástæðan fyrir þessu er msdynce_AccountNumber vísitalan á reikningstöflunni sem kom sem hluti af Prospect to cash lausninni. Ef þessi vísitala er til er ekki hægt að stofna sama viðskiptareikningsnúmerið í tveimur mismunandi lögaðilum. Þú getur annað hvort valið að byrja upp á nýtt með dual-write með því að flytja Prospect yfir í peningagögn frá Data Integrator yfir í dual-write eða þú getur sett upp síðustu "dorman" útgáfuna af Prospect to cash lausninni. Þessi grein fjallar um báðar þessar aðferðir.

## <a name="install-the-last-dorman-version-of-the-data-integrator-prospect-to-cash-solution"></a>Settu upp síðustu „dorman“ útgáfuna af Data Integrator Prospect to cash lausninni

**P2C útgáfa 15.0.0.2** er talin síðasta "dorman" útgáfan af gagnasamþættingunni Prospect to cash lausn. Þú getur halað því niður frá [FastTrack for Dynamics 365](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/P2C).

Þú þarft að setja það upp handvirkt. Eftir uppsetningu er allt nákvæmlega eins, nema msdynce_AccountNumber vísitalan er fjarlægð.

## <a name="steps-to-migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Skref til að flytja Prospect yfir í reiðufégögn frá Data Integrator yfir í tvíritun

Til að flytja PTC-gögn úr Data Integrator í tvöfalda skráningu skal fylgja þessum skrefum.

1. Keyrið Data Integrator-verk PTC til að gera eina fulla samstillingu að lokum. Þannig tryggir þú að bæði kerfin (fjármála- og rekstrarforrit og öpp fyrir þátttöku viðskiptavina) hafi öll gögnin.
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
5. Búðu til tvískrifaða tengingu á milli fjármála- og rekstrarforritsins og viðskiptavinaforritsins fyrir einn eða fleiri lögaðila.
6. Virkið töfluvörpun tvöfaldrar skráningar og keyrið fyrstu samstillinguna fyrir áskild tilvísunargögn. (Frekari upplýsingar er að finna í [Hvað skal hafa í huga við fyrstu samstillingu](initial-sync-guidance.md).) Dæmi um áskilin gögn eru m.a. viðskiptavinaflokkar, greiðsluskilmálar og greiðsluáætlanir. Ekki skal virkja vörpun tvöfaldrar skráningar fyrir töflur sem krefast frumstillingar, t.d. töflur lykla, tilboðs, tilboðslínu, pöntunar og pöntunarlínu.
7. Í forriti viðskiptavinar skal opna **Ítarlegar stillingar \> Kerfisstillingar \> Gagnastjórnun \> Afrita greiningarreglur** og slökkva á öllum reglum.
8. Frumstillið töflurnar sem eru gefnar upp í skrefi tvö. Fyrir leiðbeiningar, sjá þá hluta þessarar greinar sem eftir eru.
9. Opnaðu fjármála- og rekstrarappið og virkjaðu töflukortin, svo sem reikninginn, tilboð, tilboðslínu, pöntun og pöntunarlínutöflukort. Keyrið síðan fyrstu samstillingu. (Fyrir frekari upplýsingar, sjá [Hugleiðingar um fyrstu samstillingu](initial-sync-guidance.md) .) Þetta ferli mun samstilla viðbótarupplýsingar úr fjármála- og rekstrarforritinu, svo sem vinnslustöðu, sendingar- og innheimtuheimilisföng, vefsvæði og vöruhús.

## <a name="account-table"></a>Lyklatafla

1. Í dálkinn **Fyrirtæki** skal færa inn heiti fyrirtækisins, til dæmis **USMF**.
2. Í dálkinn **Gerð vensla** skal færa inn **Viðskiptavin** sem fast gildi. Ekki er víst að hægt sé að flokka hverja reikningsfærslu sem viðskiptavin í viðskiptagrunni.
3. Í **Auðkenni viðskiptavinahóps** dálki, sláðu inn númer viðskiptavinahóps úr fjármála- og rekstrarappinu. Sjálfgefið gildi úr Prospect to cahs lausn er **10**.
4. Ef notuð er PTC-lausnin án sérstillingar á **Reikningsnúmeri** skal færa inn gildi fyrir **Reikningsnúmer** í dálkinn **Aðilanúmer**. Ef það eru sérstillingar og þú veist ekki aðilanúmerið skaltu draga þessar upplýsingar úr fjármála- og rekstrarappinu.

## <a name="contact-table"></a>Taflan Tengiliður

1. Í dálkinn **Fyrirtæki** skal færa inn heiti fyrirtækisins, til dæmis **USMF**.
2. Stillið eftirfarandi dálka út frá **IsActiveCustomer** gildinu í CSV-skrá:

    - Ef **IsActiveCustomer** er stillt á **Já** í CSV-skrá skal stilla dálkinn **Seljanlegt** á **Já**. Í **Auðkenni viðskiptavinahóps** dálki, sláðu inn númer viðskiptavinahóps úr fjármála- og rekstrarappinu. Sjálfgefið gildi úr Prospect to cahs lausn er **10**.
    - Ef **IsActiveCustomer** er stillt á **Nei** í CSV-skrá skal stilla dálkinn **Seljanlegt** á **Nei** og stilla dálkinn **Tengiliður fyrir** á **Viðskiptavinur**.

3. Ef notuð er PTC-lausnin án sérstillingar á **Númer tengiliðar** skal stilla eftirfarandi dálka:

    - Yfirfærið númer tengiliðar á CSV-skrána (**msdynce\_contactnumber**) á tengiliðanúmerið í töflunni **Tengiliður** (**msdyn\_contactnumber**).
    - Notið gildið úr töflunni **Númer tengiliðar** í dálkinn **Aðilanúmer**.
    - Notið gildin úr töflunni **Númer tengiliðar** í dálkinum **Lykilnúmer/kenni tengiliðar**.

## <a name="invoice-table"></a>Reikningstafla

Vegna þess að gögn frá **Reikningur** Taflan er hönnuð til að flæða aðra leið, frá fjármála- og rekstrarforritinu til viðskiptavinaforritsins, frumstilling er ekki nauðsynleg. Keyrðu fyrstu samstillingu til að flytja öll nauðsynleg gögn úr fjármála- og rekstrarforritinu yfir í forritið fyrir þátttöku viðskiptavina. Frekari upplýsingar má finna á [Hvað skal hafa í huga við fyrstu samstillingu](initial-sync-guidance.md).

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

Vegna þess að gögn frá **Vörur** Taflan er hönnuð til að flæða aðra leið, frá fjármála- og rekstrarforritinu til viðskiptavinaforritsins, frumstilling er ekki nauðsynleg. Keyrðu fyrstu samstillingu til að flytja öll nauðsynleg gögn úr fjármála- og rekstrarforritinu yfir í forritið fyrir þátttöku viðskiptavina. Frekari upplýsingar má finna á [Hvað skal hafa í huga við fyrstu samstillingu](initial-sync-guidance.md).

## <a name="quote-and-quote-product-tables"></a>Töflur tilboðs og afurðartilboðs

Fyrir **Tilvitnun** töflu, fylgdu leiðbeiningunum í [Panta borð](#order-table) kafla fyrr í þessari grein. Fyrir töfluna **Afurðartilboð** skal fylgja leiðbeiningunum í hlutanum [Tafla afurðapöntunar](#order-products-table).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

