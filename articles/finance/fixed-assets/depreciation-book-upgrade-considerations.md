---
title: Yfirlit yfir uppfærslu afskriftarbókar
description: Í eldri útgáfum, voru tvö matshugtök fyrir eignir, virðislíkön og afskriftabækur.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d42936a94e0f4d50ae227d760d5bee6e1e3a12e6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826979"
---
# <a name="depreciation-book-upgrade-overview"></a>Yfirlit yfir uppfærslu afskriftarbókar

[!include [banner](../includes/banner.md)]

Í eldri útgáfum, voru tvö matshugtök fyrir eignir - virðislíkön og afskriftabækur. Í Microsoft Dynamics 365 for Operations (1611) útgáfu, er aðgerðin virðislíkön og afskriftarbókar sameinaðar í eitt hugtak sem kallast bók. Þetta efnisatriði gefur einhverjar eftirfarandi gott að hafa í huga fyrir uppfærslu. 

Uppfærsluferlið færir fyrirliggjandi uppsetningu og allar fyrirliggjandi færslur til uppbyggingar nýju bókarinnar. Virðislíkön haldast eins og þau eru, sem bók sem bókar í fjárhag. Afskriftabækur verða flutt í bók sem hefur **Bóka í fjárhag** valkostur stilltur á **Nei**. Færslubókaheiti afskriftabóka verði flutt í færslubókarheitið fjárhags sem er með bókunarlag stillt á **Ekkert**. Færslur afskriftarbókar verða fluttar í Eignafærsla. 

Áður en uppfærslu gagna er keyrð, þarf að skilja kostirnir tveir sem eru tiltækar til uppfærslu færslubókarlínur afskriftarbókar í fylgiskjöl færslu, og númeraröð sem verður notað fyrir fylgiskjalarunu. 

Valkostur 1:  **Kerfisskilgreind númeraröð** - Þetta er sjálfgefin stilling til að besta uppfærsluframkvæmd. Uppfærslu notar ekki ramma fyrir númeraraðir, en mun í staðinn úthluta fyliskjölum með samstæðubyggð nálgun. Eftir uppfærslu, verður nýja númeraröð stofnað með **Næsta númerasetti** og byggt upp í samræmi við uppfærða færslu. Að sjálfgefnu, verður notuð númeraröð vera á FADBUpgr\#\#\#\#\#\#\#\#\# sniði. Nokkrar færibreytur eru tiltækar til að leiðrétta sniðið þegar þessi nálgun er notuð:

-   **Númeraraðarkóði** – Kóði til að auðkenna númeraröð. Þessi númeraraðarkóða getur ekki verið til þar sem hún verður stofnuð af uppfærslunni.
    -   Heiti fasta: **NumberSequenceDefaultCode**
    -   Sjálfgefið gildi: "FADBUpgr"
-   **Forskeyti** – Gildi fyrir streng fasta sem verður notað sem forskeyti fyrir fylgiskjalsnúmerin.
    -   Heiti fasta: **NumberSequenceDefaultParameterPrefix**
    -   Sjálfgefið gildi: "FADBUpgr"
-   **Lengd bókstafa og talna** – Lengd hluta sem notar bókstafi og tölur fyrir númeraröð.
    -   Heiti fasti: **NumberSequenceDefaultParameterAlpanumericLength**
    -   Sjálfgildi: 9
-   **Upphafsnúmer** - fyrsta númer sem notað er í númeraröð.
    -   Heiti fasta: **NumberSequenceDefaultParameterStartNumber**
    -   Sjálfgildi: 1

Möguleiki 2: **Fyrirliggjandi notandaskilgreindur númeraröð** - Þennan valkost gerir þér kleift að skilgreina númeraröðina sem nota á fyrir uppfærslu. Íhuga að nota þennan valkost ef þú þarft ítarlega skilgreiningu númeraraðar. Til að nota númeraröð, verður að breyta uppfærsluflokk ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans með eftirfarandi upplýsingar:

-   **Númeraraðarkóði** – Kóði númeraraðar.
    -   Heiti fasti: **NumberSequenceExistingCode**
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