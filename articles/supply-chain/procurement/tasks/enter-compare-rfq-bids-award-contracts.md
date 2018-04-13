--- 
title: "Færa inn og bera saman tilboð vegna tilboðsbeiðna og gera samninga"
description: "Þessi verklýsing sýnir hvernig á að færa inn svör við Tilboðsbeiðni, gefa stig og bera saman tilboð, og veita síðan einum lánardrottninum kauptilboðið."
author: mkirknel
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5dea9d7bfb1bf7b11f6c49cccaab1b73d4e58d16
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a>Færa inn og bera saman tilboð vegna tilboðsbeiðna og gera samninga

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að færa inn svör við Tilboðsbeiðni, gefa stig og bera saman tilboð, og veita síðan einum lánardrottninum kauptilboðið. Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF. Áður en byrjað er, verður að hafa beiðni um TILBOÐ með tveimur línum sem hefur verið send til a.m.k. tveimur lánardrottnum. Hægt er að keyra ferlinu "Stofna beiðni um tilboð" sem forsendu til að stofna þessi. Það Þarf að vera uppsettur skilyrði fyrir stigagjöf áður en þessari ferli er keyrð.


## <a name="enter-a-reply-from-a-vendor"></a>Færa skal inn svar frá lánardrottni.
1. Fara í innkaup og aðföng  > Beiðnir um tilboð  > Allar beiðnir um tilboð.
2. Veljið beiðni um TILBOÐ sem er með stöðuna Sent og smella á tengilinn fyrir málsnúmer Beiðni um tilboð.
    * Beiðni um TILBOÐ hefði átt að senda til í það minnsta 2 lánardrottna .  
3. Smellt er á Hausnum til að fara í lista yfir lánardrottna.
4. Velja skal lánardrottin til að sem færa á svar inn fyrir á beiðni um tilboð.
5. Smella á Færa inn svar
6. Smellið á Svara á aðgerðarúðunni.
7. Smella á Afrita gögn til að svara.
    * Þessi aðgerð mun afrita valda gögn, t.d. magnið frá BUT-verki í svar við tilboðsbeiðni. Einnig hægt að sleppa þessari aðgerð og fylla inn í öll svæði fyrir svör handvirkt þegar svari er breytt.  
8. Smellið á „Breyta“.
9. Færið inn númer í reitnum „Einingarverð“.
10. Velja hina tilboðslínuna.
11. Færið inn númer í reitnum „Einingarverð“.

## <a name="score-the-bid"></a>Gefa kauptilboði stig.
1. Smellt er á Hausnum til að fara í stigagjöf tilboða.
2. Útvíkka stigagjöf fyrir Kauptilboðið hluta.
3. Færið inn númer fyrir eitt skilyrði fyrir stigagjöf í svæðinu Stigagjöf.
    * Ef þú hefur músabendil yfir skilyrði fyrir stigagjöf kemur ábending sem sýnir bil sem þarf hafa stig innan. Hægt er að bæta tölu á bilinu 1 til 5 við hvert þessara skilyrða í þessari sýnigögn.  
4. Veljið annað skilyrði fyrir stigagjöf.
5. Í reitinn Stigafjöldi skal slá inn númer.
6. Útvikka liðnum Spurningalisti.
    * Ef BUT-verk er með spurningalista sem var send til lánardrottna er hægt að færa inn svör þeirra í hlutanum spurningalisti.  
7. Lokið síðunni.

## <a name="enter-a-reply-for-another-vendor"></a>Færa inn svar fyrir aðra lánardrottins
1. Veljið næsta lánardrottins með því að hreinsa lánardrottin sem verið var að færa inn svar fyrir og velja svo línu fyrir næsta lánardrottin.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Smella á Færa inn svar
4. Smella á Afrita gögn til að svara.
5. Smellið á „Breyta“.
6. Færið inn númer í reitnum „Einingarverð“.
7. Velja hina tilboðslínuna.
8. Færið inn númer í reitnum „Einingarverð“.

## <a name="score-the-second-bid"></a>Gefa öðru kauptilboði stig.
1. Smellt er á Hausnum til að fara í stigagjöf tilboða.
2. Í reitinn Stigafjöldi skal slá inn númer.
3. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
4. Í reitinn Stigafjöldi skal slá inn númer.

## <a name="compare-the-replies"></a>Bera saman svör
1. Smellið á „Almennt“ á aðgerðarúðunni.
2. Smella á Bera saman svör
3.  - Færið númer inn í svæðið stigagjöf.
    * Þessi síða sýnir tilboð með haus og línur, og heildarstigafjölda á hausstigi. Hægt er að bera saman línum með því að raða í hnitanetinu þannig samanburðarhæfar línur eru hlið við hlið. Upplýsingar innihalda einnig: Magn: magn sem uppgefið er af lánardrottni. Þetta gæti ekki verið það sama og magnið í beiðninni um tilboð.   Nettóupphæð – Verð gefið upp af lánardrottni, að frádregnum öllum afsláttum, fyrir vörurnar á línunni.   Frávik – Fjöldi daga sem munar á afhendingardagsetningu í tilboðshaus eða tilboðslínu og umbeðnum afhendingardegi í RFQ-haus eða RFQ-línu.   Fyrir hvert tilboð er hægt að færa inn forgangsröðun:  
4. Veljið haus línu fyrir hitt tilboðið sem þú ætlar að gefa stig.
5.  - Færið númer inn í svæðið stigagjöf.
6. Smellið á „Vista“.

## <a name="reject-a-bid"></a>Hafna tilboði
1. Veljið haus línu fyrir hitt tilboðið sem þú ætlar að hafna.
    * Aðeins er hægt að samþykkja, hafna eða skila einu tilboði eða línu innan eins kauptilboðs í einu.  
2. Veldu gátreitinn Merkja.
    * Ef Merkja gátreitur er merktur á hausi kauptilboðs þá verða allar línurnar merktar líka. Einnig mætti velja að merkja hlutmengi línanna innan kauptilboðs til að hafna eða samþykkja þær. Hægt er að samþykkja kauptilboð eins lánardrottins í sumar línur í beiðni um tilboð og síðan veita öðrum línum í beiðni um tilboð til annars lánardrottins, hins vegar þarf að gera þetta í 2 skrefum, eitt tilboð í einu. Ef aðrar línur eru til staðar er aðeins hægt að samþykkja annaðhvort upprunalegu kauptilboðslínunni eða valkostarlínu, en ekki bæði.  
3. Smellt er á Hafna.
4. Smelltu á Færibreytur til að opna felligluggann.
5. Sláið inn eða veldu gildi í reitnum ástæða fyrir höfnun.
    * Ástæðan fyrir höfnun verður geymd í svarinu.  
6. Smellið á „Í lagi“.
7. Smellið á „Í lagi“.
8. Lokið síðunni.
9. Lokið síðunni.
10. Endurhlaðið síðuna.

## <a name="accept-a-bid"></a>Samþykkja tilboð
1. Veljið tilboð sem á að samþykkja og smellið síðan á tengilinn í svæðinu Beiðni um tilboð.
2. Smellið á Svara á aðgerðarúðunni.
3. Smellið á Samþykkja.
    * Ef merkt hefur verið við tilteknar línur en ekki aðrar þá mun samþykktaraðgerðin aðeins innihalda merktar línur. Ef óskað er að samþykkja allar línur á kauptilboði þá þarft ekki að merkja línur.  
4. Smelltu á Færibreytur til að opna felligluggann.
    * Þannig er hægt að skrá ástæðu fyrir samþykkt tilboðsins. Ástæðan verður geymd í tilboðinu.  
5. Í reitinn ástæða samþykkis skal slá inn eða velja gildi.
6. Smellið á „Í lagi“.
7. Smellið á „Í lagi“.
    * Þegar smellt er á í lagi myndar þetta innkaupapöntun byggða á línum sem eru innifaldar í samþykkt á beiðni um TILBOÐ. Ef önnur tilboð sem hafa ekki verið unnar eru til staðar (samþykkt, hafnað eða skilað) mun kerfið biðja notandann um að hafna eftirstandandi tilboðum.  

## <a name="view-the-purchase-order-thats-been-generated"></a>Skoða innkaupapöntun sem hefur verið mynduð.
1. Smellið á „Almennt“ á aðgerðarúðunni.
2. Smellt er á Innkaupapöntunarlína.
    * Hér er hægt að sjá innkaupapöntun sem var mynduð þegar tilboðið var samþykkt.  
3. Lokið síðunni.
4. Lokið síðunni.
5. Lokið síðunni.
6. Lokið síðunni.


