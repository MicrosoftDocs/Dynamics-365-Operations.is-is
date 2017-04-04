---
title: "Afskrift bókar uppfærslu yfirlit"
description: "Í fyrri útgáfum, voru tvær mat hugtök fyrir eignir - virðislíkön og afskriftabækur.  Í Microsoft Dynamics 365 for Operations 1611 útgáfu, er aðgerðin virðislíkön og afskriftarbókar sameinaðar í eitt hugtak sem kallast bók. Þetta efnisatriði gefur einhverjar eftirfarandi gott að hafa í huga fyrir uppfærslu."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer
ms.search.scope: Operations, Core
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: bec019d218d80ba059d5a1c232072f46b1ae3ee2
ms.openlocfilehash: d29cb7bc5acc29be93332b4211adebc4486a7a25
ms.lasthandoff: 03/31/2017


---

# <a name="depreciation-book-upgrade-overview"></a>Afskrift bókar uppfærslu yfirlit

Í fyrri útgáfum, voru tvær mat hugtök fyrir eignir - virðislíkön og afskriftabækur.  Í Microsoft Dynamics 365 for Operations 1611 útgáfu, er aðgerðin virðislíkön og afskriftarbókar sameinaðar í eitt hugtak sem kallast bók. Þetta efnisatriði gefur einhverjar eftirfarandi gott að hafa í huga fyrir uppfærslu. 

Uppfærsluferlið færir fyrirliggjandi uppsetningu og allar fyrirliggjandi færslur til uppbyggingar nýju bókarinnar. Virðislíkön haldast eins og þau eru, sem bók sem bókar í fjárhag. Afskriftabækur verða flutt í bók sem hefur **Bóka í fjárhag** valkostur stilltur á **Nei**. Færslubókaheiti afskriftabóka verði flutt í fjárhag færslubókarheiti með bókunarlagi sem stilla á **Ekkert**. Verður að flytja færslur í afskriftabók eignafærslur. 

Áður en uppfærslu gagna er keyrð, þarf að skilja kostirnir tveir sem eru tiltækar til uppfærslu færslubókarlínur afskriftarbókar í fylgiskjöl færslu, og númeraröð sem verður notað fyrir fylgiskjalarunu. 

Valkostur 1: **kerfisskilgreind númeraröð ** -Þetta er sjálfgefin stilling til að besta uppfærsluframkvæmd. Uppfærslu notar ekki ramma fyrir númeraraðir, en mun í staðinn úthluta fyliskjölum með samstæðubyggð nálgun. Eftir uppfærslu, verður að stofna nýja númeraröð með í **Næsta númer setja** hæfilega samkvæmt uppfærðum færslum. Að sjálfgefnu númeraröð sem notuð verður við FADBUpgr\#\#\#\#\#\#\#\#\# sniði. Nokkrar færibreytur eru tiltæk til að leiðrétta snið þegar með því að nota þessa nálgun:

-   **Númeraraðarkóði** – kóða til að tilgreina númeraröðina. Þessi númeraraðarkóða ekki þar sem hún stofnuð með uppfærslunni.
    -   Heiti fasta: **NumberSequenceDefaultCode**
    -   Sjálfgefið gildi: "FADBUpgr"
-   **Forskeyti** – Gildi fyrir streng fasta sem verður notað sem forskeyti fyrir fylgiskjalsnúmerin.
    -   Heiti fasta: **NumberSequenceDefaultParameterPrefix**
    -   Sjálfgefið gildi: "FADBUpgr"
-   **Lengd bókstafa og talna** – Lengd hluta sem notar bókstafi og tölur fyrir númeraröð.
    -   Heiti fasti: ** NumberSequenceDefaultParameterAlpanumericLength **
    -   Sjálfgildi: 9
-   **Upphafsnúmer** - fyrsta númer sem notað er í númeraröð.
    -   Heiti fasti: ** NumberSequenceDefaultParameterStartNumber **
    -   Sjálfgildi: 1

Möguleiki 2: **Fyrirliggjandi notandaskilgreindur númeraröð** -Þessi valkostur gerir notandanum kleift að skilgreina númeraröðina sem nota á fyrir uppfærslu. Íhuga að nota þennan valkost ef ítarlega skilgreiningu númeraraðar. Til að nota númeraröð, verður að breyta uppfærslu klasa ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans með eftirfarandi upplýsingar:

-   **Númeraraðarkóði** – Kóði númeraraðar.
    -   Heiti fasti: ** NumberSequenceExistingCode **
    -   Sjálfgildi: Engin sjálfgefin, þetta þarf að uppfæra fyrir númeraraðakóða.
-   **Samnýttar númeraröð** – boole-gildi til að greina umfang númeraraðar. Notuð "satt" fyrir samnýttar númeraraðir þvert á öll fyrirtæki og "rangt" fyrir sviðs sem eru sértæk fyrir fyrirtæki. Þegar "rangt", númeraröð með tilgreindu heiti verður að vera til í hvert fyrirtæki sem inniheldur færslur í afskriftabók. Samnýttar númeraraðir til í hverri deildaskiptingu sem inniheldur færslur í afskriftabók.
    -   Heiti fasti: ** NumberSequenceExistingIsShared **
    -   Sjálfgefið gildi: rétt

Færibreyturnar eru staðsett í upphafi á ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans klasa. 

*Tilgreina æskilegt vísi nálgun fyrir úthlutun fylgiskjöl*<ph id="t1">
</ph>*/ / satt ef óskað er að nota með fyrirliggjandi kóða númeraraðar*<ph id="t2">
</ph>*/ / false ef ætlunin er að nota kerfisskilgreindar númeraröð (sjálfgefnu)* const boole NumberSequenceUseExistingCode = false;  

*Ef nota kerfisskilgreindar númer röð nálgunin skal tilgreina færibreytur fyrir númeraröð. *<ph id="t3">
</ph>*/ / Verður að stofna nýja númeraröð með þessar færibreytur.* Const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;   

*Ef nota fyrirliggjandi nálgun röð skal tilgreina fyrirliggjandi kóða númeraraðar. *<ph id="t4">
</ph>*/ / Úthlutun fylgiskjals verður fara í röð eftir röð fyrir núverandi númeraröð.* Const str NumberSequenceExistingCode = '; */ / Svið fyrirliggjandi kóða númeraraðarinnar sem á að tilgreina*<ph id="t5">
</ph>*/ / satt ef númeraröðinni sem tilgreind er samnýtt*<ph id="t6">
</ph>*/ / false ef númeraröðinni sem tilgreind er á fyrirtæki*<ph id="t7">
</ph>*/ / sjálfgefnu kerfisskilgreindar númeraröðinni verður notaður ef númeraraðarkóða með tilgreindri afmörkun finnst ekki.* const boolean NumberSequenceExistingIsShared = satt; 

Endurbyggja verksins sem inniheldur flokkinn eftir að fastarnir hafa verið breyttir. 

Þegar kerfið hefur myndað númer röð nálgunin (valkosturinn 1), uppfærslu nota samstæðubyggð úrvinnsla til að úthluta fylgiskjalsnúmer sem tilgreint er í færibreytum uppfærsluforskrift. Hún mun einnig stofna nýja númeraröð með tilgreinda færibreytur eftir úthlutunar. 

Þegar notast er við nálgunina notendaskilgreind fyrirliggjandi númeraröð (valkostur 2) athugar gagnauppfærslan hvort númeraröðið með tilgreindu umfangi er til staðar í gagnagrunni fyrir hverja deildaskiptingu og fyrirtæki með færslum afskriftarbókar. Ef til uppfærslu nota vinnslu röð eftir röð til að úthluta fylgiskjalsnúmer sem tilgreint eftir númeraröð með ramma númeraraðar. Ef númeraröð er ekki með tilgreindri afmörkun, uppfærslu verður notuð sem sjálfgefin kerfisskilgreindar númer röð nálgun til að úthluta númerum fylgiskjali og mun búa til nýja númeraröð með tilgreinda sjálfgefnar færibreytur eftir úthlutunar.

Með hvorri nálguninni mun uppfærsluforskrift gagna einnig nota númeraröðina fyrir reitinn **fylgiskjalarunur** á nýjum heitum færslubók fjárhags sem voru stofnuð úr fyrri færslubókarheitum afskriftarbókar.


