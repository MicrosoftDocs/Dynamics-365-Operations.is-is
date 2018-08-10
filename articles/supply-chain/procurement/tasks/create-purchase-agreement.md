--- 
title: Stofna innkaupasamning
description: "Þetta ferli leiðbeinir við stofnun innkaupasamnings."
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0d0cc6508071bea3f622bc21f06aa55d2b757b6f
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-agreement"></a>Stofna innkaupasamning

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli leiðbeinir við stofnun innkaupasamnings. Þetta verk myndi yfirleitt gert af innkaupastjóra. Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn. Þú Þarft að hafa sett upp flokkanir innkaupasamnings áður en byrjað er. Þegar Innkaupapöntun er stofnuð og hægt er að nota hana þegar þú stofnar innkaupapöntun, og það afrita skilyrði innkaupasamnings í haus og allar línur í pöntun sem verða fyrir áhrifum af samninginn.


## <a name="create-a-new-purchase-agreement"></a>Stofna nýjan innkaupasamning
1. Fara í Innkaup og uppruni > Innkaupasamningar > Innkaupasamningar.
2. Smellið á „Nýtt“.
3. Í reitnum Lánardrottnalykill skal smella á fellilistahnappinn til að opna leitina.
4. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
5. Í listanum skal smella á tengilinn í valinni línu.
6. Í reitnum Innkaupasamningur skal smella á fellilistahnappinn til að opna leitina.
7. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
8. Í listanum skal smella á tengilinn í valinni línu.
9. Víkkið út almenna hlutann.
10. Dagsetning er rituð í reitinn lokadagur.
    * Þessi lokadagur verður sjálfgefið fyrir allar línur ráðstöfunar og ákvarða hve lengi hver tiltekin ráðstöfun er gild.  
11. Í reitinn Titill skjalsins skal færa inn heiti fyrir innkaupasamninginn.
    * Láta svæðið Sjálfgefin ráðstöfun vera stillt til á ráðstöfun afurðarmagns (eða breyta þeim, ef hann er ekki stillt á þetta).  
    * Sjálfgefin ráðstöfunargildið ákvarðar valkostirnir þínir á samningslínur. Ef ný ráðstöfunargerð er þörf þegar verið er að stofna samningslínur, þarftu að breyta sjálfgefin ráðstöfun í haus.  Til eru 4 Gerðirnar ráðstafana: Ráðstöfun afurðarmagns - fyrir ákveðið magn afurðar; Ráðstöfunarvirði afurðar - fyrir tiltekna gjaldmiðilsupphæð afurðar; Ráðstöfunarvirði vörutegundar - fyrir upphæð í tilteknum gjaldmiðli í innkaupaflokki þar sem upphæðin getur verið fyrir vöru í vörulista eða vöru sem er ekki á vörulista; Ráðstöfunarvirði - fyrir tiltekna gjaldmiðilsupphæð sem getur verið uppfyllt af hvaða vöru eða af hvaða innkaupategund sem er.  
12. Smellið á „Í lagi“.

## <a name="add-a-commitment"></a>Bæta við skuldbindingu
1. Smellið á „Bæta við línu“.
2. Í listanum skal merkja valda línu.
3. Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.
4. Veljið afurð sem á að bæta ráðstöfun við.
5. Í listanum skal smella á tengilinn í valinni línu.
6. Færið inn númer í reitnum „Magn“.
    * Þetta er heildarmagn sem þú hefur samþykkt að kaupa frá lánardrottni.  
7. Færið inn númer í reitnum „Einingarverð“.
8. Víkkið út hlutann „Upplýsingar um línu“.
9. Stilla Valkosturinn Hámark er notað á Já.
    * Valkosturinn Hámark er notað takmarkar notkun á ráðstöfun. Aðeins er hægt að kaupa upp að því magni sem er tilgreint er í Magnsvæðinu fyrir línuna.  
10. draga saman hluta upplýsingar Línu.

## <a name="add-header-conditions"></a>Bæta við fyrirsagnaskilyrði
1. Í aðgerðasvæðinu er smellt á valkostir.
2. Smellið á skoða Breytingu.
3. Smellið á skoða Haus.
4. Víkka út liðnum skilmálar.
5. Í reitnum greiðsluaðferð skal smella á fellilistahnappinn til að opna leitina.
    * Greiðsluskilmálar úr lykli lánardrottins eru sýnd hér sjálfgefið.       
6. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
7. Í listanum skal smella á tengilinn í valinni línu.
8. Í reitnum Afhendingarmáti skal smella á fellilistahnappinn til að opna leitina.
9. Í listanum skal smella á tengilinn í valinni línu.
10. Í reitnum Afhendingarskilmálar skal smella á fellilistahnappinn til að opna leitina.
11. Í listanum skal smella á tengilinn í valinni línu.

## <a name="confirm-and-activate-the-agreement"></a>Vista og virkja samning
1. Í aðgerðasvæðinu er smellt á innkaupasamningur.
2. Smellt er á Staðfestingu.
    * Stilla valkost Merkja samning sem gildan á Já.  
3. Smellt er á Í lagi.
4. Í aðgerðasvæðinu er smellt á innkaupasamningur.
5. Smellt er á Staðfestingar innkaupasamnings.
    * valkostur Forskoðun/Prenta gerir kleift að búa til skjal fyrir innkaupasamning sem síðan er hægt að prenta eða senda til lánardrottins. Ef þú uppfæra samning síðar og staðfesta hann aftur, verða báðar útgáfur sýnd hér.  
6. Lokið síðunni.


