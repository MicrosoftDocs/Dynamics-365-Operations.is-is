---
title: Færa inn og bera saman tilboð vegna tilboðsbeiðna og gera samninga
description: Þessi grein útskýrir hvernig á að slá inn svör við beiðni um tilboð (RFQ), skora og bera saman tilboð og síðan úthluta samningnum til eins af söluaðilum.
author: GalynaFedorova
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchRFQCaseTable, PurchRFQReplyTable, PurchRFQCompare, PurchRFQEditLines, PurchRFQEditLinesParameters, PurchTable, PurchTablePart, PurchRFQCompareLinePrices, PurchRFQCompareRFQ
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d3ef754f2d5d58254a7c6f0e572115f8a2981ad9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893382"
---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a>Færa inn og bera saman tilboð vegna tilboðsbeiðna og gera samninga

[!include [banner](../../includes/banner.md)]

Þessi grein útskýrir hvernig á að slá inn svör við beiðni um tilboð (RFQ), skora og bera saman tilboð og síðan úthluta samningnum til eins af söluaðilum. Hægt er að nota þetta ferli í sýnigögn fyrirtækisins **USMF**.

Áður en byrjað er verður að hafa beiðni um tilboð með tveimur línum og sem hefur verið sent til a.m.k. tveggja lánardrottna. Til að stofna þessa tilboðsbeiðni skal ljúka ferlinu [Stofna beiðni um tilboð](create-request-quotation.md). Einnig þarf að setja upp skilyrði fyrir stigagjöf áður en lokið er við þetta ferli.

Hægt er að færa inn tilboðið sem annaðhvort lánardrottin eða innkaupastjóri. Frekari upplýsingar, sjá [Setja upp og vinna með samstarf lánardrottna](../set-up-maintain-vendor-collaboration.md).

## <a name="enter-a-reply-as-a-vendor"></a>Færa inn svar sem lánardrottin

1. Farið í **Samstarf lánardrottna \> Vinnusvæði \> Tilboð lánardrottins**.
2. Í listanum **Nýtt boð um kauptilboð** skal finna tilboðsbeiðni sem var send rétt í þessu. Velja skal tilboðsbeiðnina til að fara yfir það sem óskað eftir.
3. Velja skal **Viðhengi tilboðsbeiðni** til að yfirfara öll viðhengi sem var bætt við.
4. Velja skal **Tilboð** til að gera reitina breytanlega. Takið eftir að reiturinn **Framvinda tilboðs** er stilltur á **Lánardrottinn er að uppfæra**.
5. Í haus og línum skal færa inn gildin úr tilboðssvarinu.
6. Ef bæta þarf einhverjum viðhengjum við tilboðið skal velja **Viðhengi kauptilboða**.
7. Velja skal flýtiflipann **Vörur til leiðsagnar við tilboð** til að skoða hvort einhver skjöl séu nauðsynleg.
8. Velja skal flýtiflipann **Breytingar** til að skoða hvort tilboðsbeiðninni hafi verið breytt.
9. Velja skal flýtiflipann **Spurningalisti**. Svara þarf öllum spurningalistum sem birtast hér.
10. Velja skal flýtiflipann **Upplýsingar um línu** til að skoða ítarlegar upplýsingar um línuna.
11. Eingöngu skal velja **Endurstilla frá tilboðsbeiðni** ef nauðsynlegt er að endurstilla gildin sem hafa verið færð inn sem upprunaleg gildi tilboðsbeiðni.
12. Hægt er að vista tilboðið hvenær sem er og vinna frekar úr því síðar svo lengi sem að lokadagur og tími séu ekki liðnir. Í slíku tilfelli er hægt að finna tilboðið í listanum **Tilboð í vinnslu** á vinnusvæðinu **Tilboð lánardrottins**.
13. Þegar hægt er að senda tilboðið skal velja **Senda inn**. Ef ekki á að gera tilboð skal velja **Hafna**. Innsend kauptilboð eru tiltæk í listanum **Innsend kauptilboð** á vinnusvæðinu **Tilboð lánardrottins**.  
14. Þegar kauptilboðið hefur verið sent inn er hægt að afturkalla það hvenær sem er fyrir lokadag og tíma. Athugið að þegar kauptilboð er afturkallað er það ekki meðhöndlað sem innsent. Þegar innkaupadeild samþykkir eða hafnar kauptilboðinu birtist það annaðhvort í listanum **Veitt kauptilboð** eða **Týnd kauptilboð** á vinnusvæðinu **Tilboð lánardrottins**.  

## <a name="enter-a-reply-from-a-vendor-as-a-procurement-professional"></a>Færa inn svar frá lánardrottni sem innkaupastjóri

1. Ganga skal úr skugga um að heimild til að breyta tilboðum lánardrottna sé uppsett. Opnið **Innkaup og aðföng \> Uppsetning \> Færibreytur innkaupa og aðfanga**. Í flipanum **Beiðnir um tilboð** skal stilla valkostinn **Innkaupaaðili getur breytt tilboðum lánardrottna** í **Já**.
2. Fara í **innkaup og aðföng \> Beiðnir um tilboð \> Allar beiðnir um tilboð**.
3. Veljið tilboðsbeiðni sem er með stöðuna **Sent** og veljið síðan tengilinn í reitnum **Tilfelli um tilboðsbeiðni**.
4. Veljið **Vinna með svör**. Síðan sem birtist sýnir tilboðsbeiðni fyrir hvern lánardrottin sem boðið að senda tilboð.
5. Veljið tilboðsbeiðni sem hefur ekki verið svarað. (Reiturinn **Framvinda svars** ætti að vera stilltur á **Ekki hafið**.)
6. Veljið **Breyta \> Breyta svari við tilboðsbeiðni**. Síðan **Svar við tilboðsbeiðni** birtist. Sem innkaupastjóri er nú hægt að færa inn svarið fyrir hönd lánardrottins. Takið eftir að reiturinn **Framvinda tilboðs** er stilltur á **Innkaupaaðili er að uppfæra**.  
7. Færið inn tilboðsgögnin. Þegar því er lokið skal velja **Senda inn**.

## <a name="score-the-bids"></a>Gefa kauptilboðum stig

1. Á síðunni **Allar beiðnir um tilboð** skal velja tilfelli tilboðsbeiðni þar sem á að gefa svörum stig.
2. Veljið **Vinna með svör**.
3. Veljið svarið til að gefa stig.
4. Veljið **Haus** svo hægt sé að skoða stigagjöfina fyrir tilboðið.
5. Í flýtiflipanum **Stigagjöf kauptilboða** skal færa inn tölu í reitinn **Stigagjöf** fyrir eitt af skilyrðum fyrir stigagjöf. Ef bendli er haldið yfir skilyrði fyrir stigagjöf sýnir ábending skalann sem stigagjöfin verður að vera innan. Í þessari sýniútgáfu er hægt að færa inn tölu á bilinu 1 til 5 fyrir hvert þessara skilyrða fyrir stigagjöf.  
6. Endurtakið skref 5 fyrir annað skilyrði fyrir stigagjöf.
7. Ef tilfelli tilboðsbeiðni er með spurningalista sem var sendur til lánardrottna er hægt að færa inn svör lánardrottna í flýtiflipanum **Spurningalistar**.
8. Lokið síðunni.
9. Endurtakið skref 1 til 8 fyrir öll hin kauptilboðin.

## <a name="compare-the-replies"></a>Bera saman svör

1. Í aðgerðarúðunni, í flipanum **Almennt**, skal velja **Bera saman svör**.
2. Færið númer inn í svæðið **sæti**.  
    - Þessi síða sýnir kauptilboðin, ásamt upplýsingum fyrir haus og línu, og einnig heildarstigagjöfina á hausstigi. Hægt er að bera saman línurnar með því að raða hnitanetinu þannig samanburðarhæfar línur séu hlið við hlið. Eftirfarandi upplýsingar eru einnig innifaldar:
    - **Magn** - Magnið sem lánardrottinn gaf upp. Þetta magn er hugsanlega ekki sama magnið og er tilgreint í tilboðsbeiðninni.
    - **Nettóupphæð** - Verðið sem lánardrottinn gaf upp fyrir vörurnar í línunni, að frádegnum öllum afsláttum.
    - **Frávik** – Fjöldi daga sem munar á afhendingardagsetningu í tilboðshaus eða tilboðslínu og umbeðnum afhendingardegi í haus eða línu tilboðsbeiðni. Fyrir hvert tilboð er hægt að færa inn forgangsröðun:  
3. Veljið haus línu fyrir hitt tilboðið sem þú ætlar að gefa stig.
4. Færið númer inn í svæðið **sæti**.
5. Veljið **Vista**.

## <a name="reject-a-bid"></a>Hafna tilboði

1. Veljið haus línu fyrir hitt tilboðið sem þú ætlar að hafna. Eingöngu er hægt að samþykkja, hafna eða skila einu tilboði eða línunum í einu tilboði í einu.
2. Veldu gátreitinn **Merkja**.  
    - Ef gátreiturinn **Merkja** er valinn í haus tilboðsins verða allar línurnar einnig merktar. Til að hafna eða samþykkja aðeins nokkrar af línunum í tilboðinu er hægt að merkja aðeins þær línur. Að auki er hægt að samþykkja eitt tilboð lánardrottins fyrir sumar línur tilboðsbeiðni og úthluta síðan öðrum línum tilboðsbeiðni til annars lánardrottins. Hins vegar verður að gera eitt tilboð í einu.  
    - Ef aðrar línur eru til staðar er hægt að samþykkja annaðhvort upprunalegu kauptilboðslínuna eða hina línuna, en ekki báðar.  
3. Veljið **Hafna**.
4. Veljið **Færibreytur** og síðan, í reitinn **Ástæða höfnunar**, skal færa inn eða velja ástæðu fyrir höfnun á tilboðinu. Ástæðan er geymd í svarinu.  
5. Veljið **Í lagi**.
6. Veljið **Í lagi**.

## <a name="accept-a-bid"></a>Samþykkja tilboð

1. Veljið tilboð sem á að samþykkja og smellið síðan á tengilinn í reitnum **Beiðni um tilboð**. Ef þú ert á síðunni **Bera saman svör við beiðnum um tilboð** er undirstrikaða tilboðið með áhersluna það tilboð sem kerfið hefur í huga í samþykktaraðgerðinni. Aðeins er hægt að samþykkja línur úr einu tilboði í einu.  
2. Í aðgerðarúðunni skal velja **Svara**.
3. Veljið **Samþykkja**. Ef eingöngu tilteknar línur voru merktar mun samþykktaraðgerðin eingöngu hafa þær línur með. Ef á að samþykkja allar línur í tilboðinu þarf ekki að merkja línurnar.  
4. Veljið **Færibreytur** og síðan, í reitinn **Ástæða samþykktar**, skal færa inn eða velja ástæðu fyrir samþykkt á tilboðinu. Ástæðan er geymd í kauptilboðinu.  
5. Veljið **Í lagi**.
6. Veljið **Í lagi**. Þegar valið er **Í lagi** er innkaupapöntun mynduð sem byggist á línunum sem eru hafðar með í samþykkt tilboðsbeiðni. Ef önnur tilboð eru til staðar sem ekki hefur verið unnið úr (samþykkt, hafnað eða skila) biður kerfið notandann um að hafna þeim.  

## <a name="view-the-purchase-order-that-is-generated"></a>Skoða innkaupapöntun sem er búin til

Í aðgerðarúðunni, í flipanum **Almennt**, skal velja **Innkaupapöntun**. Síðan sem birtist sýnir innkaupapöntunina sem var búin til þegar tilboðið var samþykkt.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]