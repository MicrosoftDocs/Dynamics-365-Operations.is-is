--- 
title: "Færa inn sölusamninga"
description: "Þessi verklýsing sýnir hvernig stofna á sölusamningi sem bindur einum viðskiptavini til að kaupa vöru fyrir samþykkt upphæð yfir tímanum í skiptum fyrir sérstakan afslátt."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 099447252fe8fae5d44cf6cba87e8fbe0fd924e0
ms.contentlocale: is-is
ms.lasthandoff: 07/28/2017

---
# <a name="enter-sales-agreements"></a>Færa inn sölusamninga

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli sýnir hvernig stofna á sölusamningi sem bindur einum viðskiptavini þinna til að kaupa vöru fyrir

samþykkt upphæð yfir tímanum í skiptum fyrir sérstakan afslátt. Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum.


## <a name="set-up-sales-agreement-header"></a>Setja upp Haus sölusamnings
1. Fara í Sölu og markaðssetningu > Sölusamningar > Sölusamninga.
2. Smellið á „Nýtt“.
3. Í reitnum Reikningur viðskiptavina skal smella á fellilistahnappinn til að opna leitina.
4. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
5. Í listanum skal smella á tengilinn í valinni línu.
6. Í reitnum sölusamningur skal smella á fellilistahnappinn til að opna leitina.
7. Í listanum skal smella á tengilinn í valinni línu.
8. Útvíkka eða draga saman hlutann Almennt.
9. Veljið ‚skuldbinding um gildi afurðar' í svæði Sjálfgefin ráðstöfun.
    * Ráðstöfunargerð er áskilið skilyrði sem þarf að tengja við samninginn til að skilgreina hvernig verður að uppfylla samnings. Fjögur áður skilgreindar gerðir gera þér kleift að setja upp markmið viðskiptavinarins um ráðstöfun, sýnt sem magn eða gildi. Aðeins má nota magn ráðstöfunargerðar á tiltekinni vöru, en gerðir byggt á gildi á við um sölu á bæði tilteknar og ótilteknar vörur.  
10. Í svæði lokadags, Stillið dagsetninguna í framtíðar dagsetningu þegar samningnum á að renna út
11. Smellið á „Í lagi“.

## <a name="set-up-product-value-commitment-lines"></a>Setja upp afurðargildi skuldbindingarlína
1. Smellið á „Bæta við línu“.
2. Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.
3. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
4. Í listanum skal smella á tengilinn í valinni línu.
    * Gerð ráðstöfunar sem valin er fyrir samninginn hefur áhrif á þær upplýsingar sem þú getur fært inn fyrir samningslínur. Til dæmis, fyrir samning sem byggist á virði verður að tilgreina samtals nettóupphæð (í gjaldmiðli sem samið var um) sem viðskiptavinur bindur sig að kaupa vörur fyrir. Í þessu dæmi Magni og Einingarupplýsingum svæðunum í línunni er ótiltæk þar sem verið er að stofna samning fyrir viðskiptavin sem á að kaupa sérstakt gildi vöru.   
5. Í svæðinu nettóupphæð slá inn peningaupphæð sem viðskiptavinurinn hefur ákveðið að kaupa.
6. Í Afsláttarprósent svæðinu, færið inn gildi prósentu sem á við viðskiptavinarins sölupöntunarlínur sem tengjast þessum samning.
7. Víkkið út hlutann „Upplýsingar um línu“.
8. Velja skal Já í Hámark er tryggt svæði.
    * Val á Hámark er tryggt þýðir heildarupphæð allra sölupöntunarlínanna sem nota á sérstakt verð skuldbindingar, afslættir og/eða greiðsluskilmála má ekki fara yfir upphæðinni sem er tilgreind á skuldbinding.  
    * Lágmarks- og hámarks losunarupphæðir tilgreina svið gilda sem verður selt á hverja sölupöntun sem notar valinn samning.   
9. Útvíkka hlutann haus sölusamnings.
    * Nema staða samningurinn er stillt á Virk, geta sölupantanir ekki verið tengd við samning og þar af leiðandi ekki stuðlað að uppfyllingu fyrir þann samning. Hægt er að breyta stöðunni handvirkt á þessu stigi. Þó væri myndi yfirleitt breyta stöðu þegar samnings fyrir viðskiptavin er staðfest.  
10. Á Aðgerðasvæðinu skal smellt á sölusamningur.
11. Smellt er á Staðfestingu.
    * Gangið úr skugga um að Merkja samning sem virkan valkost er stillt á Já.  
12. Velja skal Já í svæðinu Prenta skýrsluna.
13. Smellið á „Í lagi“.
14. Lokið síðunni.
    * Samningurinn er nú virkt og hægt er að hefja tengingu pantanir viðskiptavinarins við samning, sem mótfærðar á móti skuldbindingarmarkinu.  


