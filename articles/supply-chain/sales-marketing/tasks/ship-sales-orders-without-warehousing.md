--- 
title: "Senda sölupantanir án vöruhúsa"
description: "Þessi handbók sýnir hvernig á að uppfæra sölupöntun þegar vörur eru sendar til viðskiptavinarins."
author: omulvad
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8e7d2198b4976a6f60f05690d7b6f11f3da55e28
ms.openlocfilehash: a98e58b26432ee01e62d60f81a768f14568e34e4
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---
# <a name="ship-sales-orders-without-warehousing"></a>Senda sölupantanir án vöruhúsa

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þessi handbók sýnir hvernig á að uppfæra sölupöntun þegar vörur eru sendar til viðskiptavinarins. Leiðbeiningarnar eiga við um flæði uppfyllingar sem er ekki sett upp fyrir vöruhúsakerfi (hvorki grunnur eða ítarlegt vöruhús), og krefst þar af leiðandi ekki að afurð tiltektarlista sé skráð fyrir sendingu. Hægt er að keyra þetta ferli á eigin gögn eða í sýnigögn USMF fyrirtækis. Í báðum tilvikum, áður en þú ræsir þetta verk, skal stofna sölupöntun fyrir afurð á lager sem hefur magn sem er meira en 1. Til að forðast bókunarvillu þarf að athuga að afurðamagn á lager á því svæði og vöruhúsi sem var valið í pöntuninni nái yfir pöntunarmagnið.


## <a name="post-packing-slip-for-an-order"></a>Bóka fylgiseðil fyrir pöntun
1. Fara í Sölu og markaðssetningu > sölupöntun > Allar sölupantanir
2. Í listanum skal finna og velja pöntun sem var stofnuð fyrir þetta verk.
3. Í listanum skal smella á tengilinn í valinni línu.
4. Í aðgerðasvæðinu er smellt á Taka til og pakka.
5. Smellt er á Bóka fylgiseðil.
6. Útvíkka eða draga saman hlutann Færibreytur.
7. Veljið „Allt“ á svæðinu „Magn“.
    * Aðrir valkostir eru Afhenda núna og Tekið til. Ef senda á pöntunarlínuna að hluta til og reiturinn Afhenda nú í pöntunarlínunni inniheldur magn, myndirðu velja Afhenda nú. Ef flæði uppfyllingar fyrirtækis þíns felur í sér tiltektarlista sem aðskilda ferli sem er stjórnað af og skráð með tiltektarlista, myndirðu velja Tiltekið.  
    * Athuga að valkosturinn Bókun sé stilltur á Já.  
8. Stilla valkostinn Prenta fylgiseðla á Já.
    * Yfirlitsflipinn inniheldur lista yfir fylgiseðla til að mynda í þessari bókun. Ef þú ert að senda einstaka pöntun verður yfirleitt einn fylgiseðil. Hins vegar ef pöntunarlínur eru til sendingar frá mismunandi svæðum verður bókun sjálfkrafa skipt í viðeigandi fjölda skjala. Þetta er áskilið skilyrði sem ekki er hægt að breyta. Á svipaðan hátt verður bókun einnig skipt upp í mörg skjöl ef senda á línur pöntunar á mismunandi afhendingaraðsetur og sendingarreglan er sett upp til að krefjast skiptingar.  
9. Á flipanum Lína velurðu röð fyrir pöntunarlínuna sem á að senda.
10. Í reitnum Uppfæra skal slá inn tölu sem er lægri en upphaflegt magn.
11. Smellið á „Í lagi“.
12. Smella á Já.
13. Lokið síðunni.
14. Í aðgerðasvæðinu er smellt á valkostir.
15. Smellið á skoða Breytingu.
16. Smellið á skoða Haus.
    * Ef allar línur í pöntun hafa verið afgreiddar að fullu breytist staða pöntunar úr Opið í Afhent.  
    * Í þessu dæmi hefur pöntunarlínan verið send að hluta. Þess vegna helst pöntunarstaðan opin.     
    * Reiturinn Staða skjals er stilltur á fylgiseðil þar sem að minnsta kosti ein af pöntunarlínunum hefur verið send.  
17. Smellið á „Almennt“ á aðgerðarúðunni.
18. Smellt er á Línumagn.
19. Lokið síðunni.
20. Smellið á „Tiltekt og pökkun“ á aðgerðarúðunni.
21. Smella skal á fylgiseðilinn.
    * Síðan Færslubók fylgiseðla inniheldur öll skjöl fylgiseðla sem voru mynduð fyrir pöntunina. Hægt er að fara yfir nákvæmar upplýsingar um hvert skjal og prenta þær, ef þörf er á.  


