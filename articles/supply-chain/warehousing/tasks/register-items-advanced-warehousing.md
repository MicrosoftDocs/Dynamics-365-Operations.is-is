--- 
title: "Skrá vörur fyrir vöru með ítarlegt vöruhúsakerfi virkt með því að nota komubók"
description: "Þessi verklýsing sýnir hvernig á að skrá vörur með því að nota vörukomubókina þegar verið er að nota ítarleg vöruhúsakerfisferli."
author: BibiSp
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 050d1fcbc59d9bb3253bfed2433987285423b334
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a>Skrá vörur fyrir vöru með ítarlegt vöruhúsakerfi virkt með því að nota komubók

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að skrá vörur með því að nota vörukomubókina þegar verið er að nota ítarleg vöruhúsakerfisferli. Þetta væri yfirleitt gert með af móttöku starfsmaður. 

Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum. Þú þarft að hafa staðfest innkaupapöntun með opna innkaupapöntunarlínu áður en byrjað er á þessari handbók. Vara í línu verður að vera í birgðum og því verður að nota afurðarafbrigði og má ekki hafa rakningarvíddir. Og varan þarf að vera tengd við vöruhúsakerfisferli með virkan geymsluvíddarflokk. Vöruhús sem er notað verður að vera virkt fyrir vöruhúsakerfisferli og staðsetning sem er notað fyrir móttöku verður að vera númeraplötustýrð. Ef verið er að nota USMF er hægt að nota reikningsskil 1001, Vöruhús 51 og vöru M9200 til að stofna Innkaupapöntun. 

Skráðu niður númer innkaupapöntunarinnar sem er stofnuð og athugaðu einnig vörunúmer og svæði sem voru notuð fyrir innkaupapöntunarlínuna.


## <a name="create-an-item-arrival-journal-header"></a>Stofna haus vörukomubókar
1. Fara á Vörukomu.
2. Smellið á „Nýtt“.
3. Í reitinn Heiti skal slá inn gildi.
    * Ef verið er að nota USMF, er hægt að færa inn vöruhúsakerfi. Ef verið er að nota önnur gögn, verður heiti færslubókar þú hefur valið að hafa eftirfarandi eiginleika: Athuga tiltektarstaðsetningu verður að vera stillt á Nei og biðgeymslustjórnun verður að vera stillt á nei.  
4. Í reitnum Númer skal slá inn gildi.
5. Í reitinn Svæði skal slá inn gildi.
    * Veljið svæðið sem notað er fyrir innkaupapöntunarlínuna. Þetta virkar sem sjálfgefið gildi sem verður sjálfgefið fyrir allar línur í færslubókinni. Ef þú notaðir vöruhús 51 í USMF velurðu svæði 5.  
6. Í reitinn vöruhús skal slá inn gildi.
    * Velja gilt vöruhús fyrir svæðið sem var valið. Þetta virkar sem sjálfgefið gildi sem verður sjálfgefið fyrir allar línur í færslubókinni. Ef verið er að nota dæmagildi í USMF, veljið 51.  
7. Í reitinn staðsetning skal slá inn gildi.
    * Velja gilda staðsetningu í vöruhúsinu sem var valið. Staðsetning verður að vera tengd við forstillingu staðsetningar, sem er númeraplötustýrð. Þetta virkar sem sjálfgefið gildi sem verður sjálfgefið fyrir allar línur í færslubókinni. Ef verið er að nota gildi dæmi í USMF, veljið Bulk-008.  
8. Hægrismellið á felliörina í reitnum Númeraplata og veldu síðan Skoða upplýsingar.
9. Smellið á „Nýtt“.
10. Í reitinn Númeraplata skal slá inn gildi.
    * Skráið niður gildið.  
11. Smellið á „Vista“.
12. Lokið síðunni.
13. Í reitinn Númeraplata skal slá inn gildi.
    * Færið inn gildi í númeraplötu sem nýverið var stofnuð. Þetta virkar sem sjálfgefið gildi sem verður sjálfgefið fyrir allar línur í færslubókinni.  
14. Smellið á „Í lagi“.

## <a name="add-a-line"></a>Bæta við línu
1. Smellið á „Bæta við línu“.
2. Í reitnum Vörunúmer skal slá inn gildi.
    * Færið inn vörunúmerið sem var notað í línu innkaupapöntunarinnar.  
3. Færið inn númer í reitnum „Magn“.
    * Færið inn magnið sem á að skrá.  
    * Reiturinn Dagsetning ákvarðar dagsetninguna sem verður að skrá magn á lager fyrir þessa vöru í birgðum.  
    * Lotukenni er fyllt út af kerfinu ef hægt er að auðkenna það úr uppgefnum upplýsingum. Annars verður að bæta þessu við handvirkt. Þetta er skyldusvæði sem tengir þessa skráningu við tiltekna upprunaskjalslínu.  

## <a name="complete-the-registration"></a>Ljúka við skráninguna
1. Smella á Villuleita.
    * Þetta athugar hvort færslubókin sé tilbúin til bókunar. Ef sannvottun bregst verður að lagfæra villurnar áður en hægt er að bóka færslubókina.  
2. Smellið á „Í lagi“.
    * Athugaðu skilaboðin eftir að smellt er á Í lagi. Það ættu að vera skilaboð sem segja að færslubókin sé í lagi.  
3. Smellið á „Bóka“.
4. Smellið á „Í lagi“.
    * Eftir að smellt hefur verið í lagi, athuga skilaboðastikunni. Það ættu að vera skilaboð sem segja að aðgerðinni sé lokið.  
5. Lokið síðunni.


