---
title: "Upplýsingakóðar"
description: "Þessi grein veitir yfirlit yfir upplýsingakóða, flokka upplýsingakóða og hvernig skal nota þá."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 22761
ms.assetid: 99877dba-a6e3-4d88-ba0a-ee5913aea17e
ms.search.region: global
ms.search.industry: Retail
ms.author: sijoshi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d463d4ac9b4258c2282dc70547145ce38e4e8e98
ms.lasthandoff: 03/31/2017


---

# <a name="info-codes"></a>Upplýsingakóðar

[!include[banner](includes/banner.md)]


Þessi grein veitir yfirlit yfir upplýsingakóða, flokka upplýsingakóða og hvernig skal nota þá.

Upplýsingakóðarnir veita þér leið til að fanga gögn úr afgreiðslukassa (POS). Hægt er að nota ástæðukóða til að biðja gjaldkera að færa inn upplýsingar í ýmsar aðgerðir á Sölustað, eins og sala á vöru, vöruveltu eða val viðskiptavini. Gjaldkerar geta valið inntak úr lista eða færa hann inn sem kóða, númer, dagsetningu eða texta. Hægt er að úthluta upplýsingakóðum til forskilgreindra verslunaraðgerða, smásöluvara, greiðslumáta, viðskiptavina eða tiltekinna aðgerða á sölustað. Hægt er að nota ástæðukóða til að gera eftirfarandi:
-   Safna aukaupplýsingum þegar færsla er gerð, eins og við flugnúmer eða ástæðukóða fyrir skil.
-   Biðja gjaldkera afgreiðslukassans um að velja úr lista yfir verð fyrir tilteknar vörur.
-   Tengja undirkóða við upplýsingakóða sem hvetur gjaldkera um innlegg við framkvæmd á ákveðinni virkni. Til dæmis þegar viðskiptavinur skilar vöru, hægt að biðja gjaldkera til að óska eftir því hvers vegna vörunni er skilað. Síðan er hægt að nota undirkóða til að birta lista af ástæðum sem gjaldkeri getur valið úr.
-   Selja vöru sem reglulega sölu, afsláttarsölur eða ókeypis afurðar.
-   Hvetur gjaldkera til að færa inn gildi eða velja úr lista yfir undirkóða þegar þeir opna afgreiðslukassaskúffu án þess að söluaðgerð sé framkvæmd.

## <a name="info-codes-group-in-retail-and-commerce"></a>Upplýsingakóða hópur°í Smásölu og viðskipti
Í Dynamics 365 for Operations  , er hægt að stofna flokka upplýsingakóða. Upplýsingarkóðaflokkar bæta sveigjanleika með því að gera þér kleift að skilgreina færri upplýsingakóða og nota þá síðan á fjölbreyttari hátt. Hægt er að nota flokkar upplýsingakóða á eftirfarandi hátt:
-   Skilgreina færri upplýsingakóðum og auðveldlega aftur að nota þær. Upplýsingakóðar sem eru í upplýsingakóðaflokkum hafa engin fyrirfram skilgreind tengsl við aðra upplýsingakóða. Hægt er að hafa sama upplýsingakóðann í mörgum upplýsingakóðahópum og nota svo forgangsröðun til að birta sömu upplýsingakóða í þeirri röð sem gengur upp í tilteknum aðstæðum.
-   Tengdu upplýsingakóða við aðra upplýsingakóða eða hópa upplýsingakóða til að safna upplýsingum um afurð eða færslu án þess að þurfa að skilgreina sérstakan upplýsingakóða eða tengdan upplýsingakóða fyrir hverja atburðarás.

## <a name="info-code-examples"></a>Dæmi um upplýsingakóða
**Dæmi 1: Endurnýta upplýsingakóða** Hægt er að tengja upplýsingakóða þannig að þegar einn upplýsingakóði er ræstur er annar upplýsingakóði ræstur beint á eftir honum. Til dæmis þegar tilteknar vörur eru seldar, er hægt að hvetja gjaldkera til að spyrja viðskiptavininn ef hann vill kaupa rafhlöður og ábyrgð á vöruna. Fyrir aðrar vörur er hægt að hvetja gjaldkera til að spyrja viðskiptavininn ef hann vill kaupa rafhlöður og einnig að fá upplýsingar um póstnúmer hans. Ef stofna á tengdum upplýsingakóðum fyrir þessar aðstæður eru setja verður upp hvert afbrigði af upplýsingakóðann þannig gjaldkeri er beðinn um að biðja um hægri upplýsingar. Ef notaðir eru flokkar upplýsingakóða er hægt að setja upp einu sinni algenga upplýsingakóða, eins og að spyrja um rafhlöður, og nota þá áfram í mörgum upplýsingakóðahópum. Einnig er hægt að nota forgangsröðun í upplýsingakóðaflokkum til að auðkenna röðina sem kvaðningar eru birtar. **Dæmi 2: Tengja upplýsingakóða við upplýsingakóðahópa** Þegar þú selur tilteknar vörur, t.d. fartæki, viltu alltaf safna tilteknum upplýsingum, eins og símanúmeri, kenni fartækisbúnaðar (MEID) og raðnúmeri. Hins vegar einnig á að safna upplýsingum á fyrir spjaldtölvunni samanborið við farsíma. Þú getur sett upp upplýsingakóðahóp sem inniheldur kvaðningar fyrir símanúmer, MEID og raðnúmer og síðan tengja upplýsingakóðahópinn við einstaka upplýsingakóða.. Þegar afurðabundnar upplýsingakóðinn er ræstur, upplýsingakóðaflokks getur ræstar áfram til að gera það kleift að safna sameiginleg gögn án þess að þurfa til þess að skilgreina margar söfn tengdum upplýsingakóðum fyrir hverja tækis.

 
-






