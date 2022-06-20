---
title: Yfirlit yfir uppfærslu afskriftarbókar
description: Þessi grein lýsir núverandi bókunarvirkni í fastafjármunum. Þessi virkni er byggð á virkni virðislíkans sem var í boði í fyrri útgáfum, en inniheldur einnig alla virknina sem var áður fyrr einungis til staðar í afskriftarbókum.
author: moaamer
ms.date: 06/20/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: kfend
ms.custom:
- "221624"
- intro-internal
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: moaamer
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 784ec32ae886ef7ea9342b085f893eeeec761961
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855492"
---
# <a name="depreciation-book-upgrade-overview"></a>Yfirlit yfir uppfærslu afskriftarbókar

[!include [banner](../includes/banner.md)]

Þessi grein lýsir núverandi bókunarvirkni í fastafjármunum. Þessi virkni er byggð á virkni virðislíkans sem var í boði í fyrri útgáfum, en inniheldur einnig alla virknina sem var áður fyrr einungis til staðar í afskriftarbókum. Aðgerðin virðislíkön og afskriftarbókar sameinaðar í eitt hugtak sem kallast bók. Virkni bókar gerir þér kleift að nota eitt sett af síðum, fyrirspurnum og skýrslum fyrir alla ferla eignar í fyrirtækinu. Þessi grein veitir nokkur atriði sem þú ættir að íhuga áður en þú uppfærir. 

Uppfærsluferlið færir fyrirliggjandi uppsetningu og allar fyrirliggjandi færslur til uppbyggingar nýju bókarinnar. Virðislíkön haldast eins og þau eru, sem bók sem bókar í fjárhag. Afskriftabækur verða flutt í bók sem hefur Bóka í fjárhag valkostur stilltur á Nei. Færslubókaheiti afskriftabóka verði flutt í færslubókarheitið fjárhags sem er með bókunarlag stillt á Ekkert. Færslur afskriftarbókar verða fluttar í Eignafærsla.

Áður en uppfærslu gagna er keyrð, þarf að skilja kostirnir tveir sem eru tiltækar til uppfærslu færslubókarlínur afskriftarbókar í fylgiskjöl færslu, og númeraröð sem verður notað fyrir fylgiskjalarunu.

Valkostur 1:  **Kerfisskilgreind númeraröð** - Þetta er sjálfgefin stilling til að besta uppfærsluframkvæmd. Uppfærslu notar ekki ramma fyrir númeraraðir, en mun í staðinn úthluta fyliskjölum með samstæðubyggð nálgun. Eftir uppfærslu, verður nýja númeraröð stofnað með **Næsta númerasetti** og byggt upp í samræmi við uppfærða færslu. Að sjálfgefnu, verður notuð númeraröð vera á FADBUpgr\#\#\#\#\#\#\#\#\# sniði. Nokkrar færibreytur eru tiltækar til að leiðrétta sniðið þegar þessi nálgun er notuð:

-   **Númeraraðarkóði** – Kóði til að auðkenna númeraröð. Þessi númeraraðarkóða getur ekki verið til þar sem hún verður stofnuð af uppfærslunni.
    -   Heiti fasta: **NumberSequenceDefaultCode**
    -   Sjálfgefið gildi: "FADBUpgr"
-   **Forskeyti** – Gildi fyrir streng fasta sem verður notað sem forskeyti fyrir fylgiskjalsnúmerin.
    -   Heiti fasta: **NumberSequenceDefaultParameterPrefix**
    -   Sjálfgefið gildi: "FADBUpgr"
-   **Lengd bókstafa og talna** – Lengd hluta sem notar bókstafi og tölur fyrir númeraröð.
    -   Heiti fasta: **NumberSequenceDefaultParameterAlpanumericLength**
    -   Sjálfgildi: 9
-   **Upphafsnúmer** - fyrsta númer sem notað er í númeraröð.
    -   Heiti fasta: **NumberSequenceDefaultParameterStartNumber**
    -   Sjálfgildi: 1

Möguleiki 2: **Fyrirliggjandi notandaskilgreindur númeraröð** - Þennan valkost gerir þér kleift að skilgreina númeraröðina sem nota á fyrir uppfærslu. Íhuga að nota þennan valkost ef þú þarft ítarlega skilgreiningu númeraraðar. Til að nota númeraröð, verður að breyta uppfærsluflokk ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans með eftirfarandi upplýsingar:

-   **Númeraraðarkóði** – Kóði númeraraðar.
    -   Heiti fasta: **NumberSequenceExistingCode**
    -   Sjálfgildi: Engin sjálfgefin, þetta þarf að uppfæra fyrir númeraraðakóða.
-   **Samnýttar númeraröð** – boole-gildi til að greina umfang númeraraðar. Notuð "satt" fyrir samnýttar númeraraðir þvert á öll fyrirtæki og "rangt" fyrir sviðs sem eru sértæk fyrir fyrirtæki. Þegar "rangt" er notað, verður númeraröð með tilgreindu heiti vera til staðar í hvert fyrirtæki sem inniheldur færslur í afskriftabók.lur í afskriftabók. Samnýtt númeraraðir eru til í hverri deildaskiptingu sem inniheldur færslur í afskriftarbók.
    -   Heiti fasti: **NumberSequenceExistingIsShared**
    -   Sjálfgefið gildi: rétt

Færibreyturnar eru staðsett í upphafi ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans flokks. 

*//Skilgreindu æskilega nálgun á úthlutun fylgiskjala* 
 *//satt ef óskað er að nota fyrirliggjandi kóða númeraraðar* 
 *// rangt ef ætlunin er að nota kerfisskilgreindar númeraröð (sjálfgefið)* const boolean NumberSequenceUseExistingCode = rangt;  

*// Ef nota á náglun kerfisskilgreindar númeraröð skal tilgreina færibreytur fyrir númeraröð.*
 *//Nýja númeraröð verður stofnuð með þessar færibreytur.* const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;   

*// Ef á að nota nálgunina fyrirliggjandi númeraraðakóði, skal tilgreina fyrirliggjandi kóða númeraraðar.* 
 *//Úthlutun fylgiskjals mun fara röð eftir röð fyrir núverandi númeraröð.* const str NumberSequenceExistingCode = '‘; *// Tilgreina umfang fyrirliggjandi númeraraðakóða* 
 *//satt ef tilgreind númeraröð er samnýtt* 
*rangt ef tilgreind númeraröð er á hvert fyrirtæki* 
 *//Sjálfgefna kerfisskilgreindar númeraröðinni verður notaður ef númeraraðarkóða með tilgreindu umfangi fannst ekki.* const boolean NumberSequenceExistingIsShared = satt; 

Endurbyggja verksins sem inniheldur flokkinn eftir að fastarnir hafa verið breyttir. 

Þegar notast er við nálgun sem byggist á kerfisskilgreindum númeraröðum, (valkosturinn 1), mun uppfærslan nota vinnslu sem byggist á settum til að úthluta númerum fylgiskjala eins og tilgreint er í færibreytum uppfærsluforskriftar. Hún mun einnig stofna nýja númeraröð með tilgreinda færibreytur eftir úthlutunina. 

Þegar notast er við nálgunina notendaskilgreind fyrirliggjandi númeraröð (valkostur 2) athugar gagnauppfærslan hvort númeraröðið með tilgreindu umfangi er til staðar í gagnagrunni fyrir hverja deildaskiptingu og fyrirtæki með færslum afskriftarbókar. EF það er ekki til staðar, mun uppfærslan nota röð-eftir-röð vinnslu til að úthluta númerum fylgiskjala sem tilgreind eru í númeraröðinni með því að nota ramma númeraraða. Ef númeraröð er ekki til staðar með tilgreindu umfangi, mun uppfærslan nota sjálfgefna kerfisskilgreindu nálgun á númeraraðir til að úthluta númer fylgiskjals, og mun stofna nýja númeraröð með tilgreindum sjálfgefnum færibreytum eftir úthlutunina.

Með hvorri nálguninni mun uppfærsluforskrift gagna einnig nota númeraröðina fyrir reitinn **fylgiskjalarunur** á nýjum heitum færslubók fjárhags sem voru stofnuð úr fyrri færslubókarheitum afskriftarbókar.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
