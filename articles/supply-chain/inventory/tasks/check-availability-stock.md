--- 
title: "Athuga framboð birgðaframboð"
description: "Þessi ferli sýnir hvernig athuga birgðir á lager og efnislegar lagerbirgðir fyrir ákveðið vörunúmer."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand
audience: Application User
ms.reviewer: 
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: 
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 62338fe11c30781f264e626fad835a2ba9dca837
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="check-the-availability-of-stock"></a>Athuga framboð birgðaframboð

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi ferli sýnir hvernig athuga birgðir á lager og efnislegar lagerbirgðir fyrir ákveðið vörunúmer. Hún líka sýnir hvernig á að fá upplýsingar um framboð tengdar vöru. Lagerbirgðir sem eru efnislegar birgðir eru tiltækar birgðir á lager – sem hefur verið keypt, móttekin og skráð. Lagerbirgðir inniheldur tiltækar birgðir á lager, en einnig birgðirnar sem hefur verið pöntuð er vænst en hefur enn ekki verið móttekin og skráð. Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn. Ef verið er að nota USMF má nota dæmagildin sem eru sýndar. Þessum verkefnum myndi venjulega að framkvæma með starfsmaður í vöruhúsi.


## <a name="check-on-hand-inventory-for-an-item"></a>Kanna birgðir á lager fyrir vöru
1. Fara í birgðastjórnun > Fyrirspurnir og skýrslur > Birgðir á lager.
2. Velurðu línu vörunúmers.
    * Til að spyrjast fyrir um birgðir á lager eftir vörunúmeri, veljið línuna þar sem Taflan er stillt á birgðum á lager og reitur er stillt á vörunúmer.  
3. Í svæðinu skilyrði, Veldu vöru sem þú vilt telja.
    * Ef verið er að nota sýnigögn USMF-fyrirtækis er hægt að velja 'M9201'.  
4. Smellið á „Í lagi“.
5. Smellt er á Víddir.
    * Flipinn Víddir leyfir að velja hversu miklar upplýsingar til að sjá um birgðir á lager. Ef þarf gögn sem tengjast frátekningu, verður að birta birgðavíddir á vörum sem nota ferli ítarlegrar vöruhúsa (WHS).  
6. Smellið á „Í lagi“.
7. Á Aðgerðasvæðinu skal smellt á Tengdar upplýsingar.
    * Ef það sést ekki, gæti þurft að smella á hnappinn Ellipsis (...) til að sjá valkostir frekari aðgerða.  
8. Smellt er á birgðayfirlitið.
    * yfirlitsflipann Framboð veitir birgðaupplýsingar fyrir tiltekna vöru, eins og magn á lager, afhendingartíma og lánardrottnaupplýsingar.  
9. Víkkið út hlutann Á lager.
10. Stækka hlutann Lánardrottinn.
11. Lokið síðunni.
12. Lokið síðunni.

## <a name="check-physical-on-hand-inventory"></a>Athuga Efnislegar lagerbirgðir
1. Fara í vöruhúsakerfi > Fyrirspurnir og skýrslur > Efnislegar birgðir á lager.
2. Í reitnum Vörunúmer skal slá inn gildi.
    * Hægt er að nota svæðin Svæðis og Vöruhúss til að sía listann yfir vörur.  
3. Endurhlaðið síðuna.
4. Smellt er á Sýna víddir.
    * Birtingarflipinn Víddir gerir kleift að velja hversu miklar upplýsingar til að sjá um birgðir á lager.  
5. Smellið á „Í lagi“.
6. Lokið síðunni.

## <a name="check-on-hand-inventory-by-location"></a>Athuga Birgðir eftir staðsetningu
1. Fara í vöruhúsakerfi > Fyrirspurnir og skýrslur > Á lager eftir staðsetningu.
2. Í reitinn vöruhús skal slá inn gildi.
    * Ef verið er að nota USMF sýnigögn fyrirtæki er hægt að nota '51'.  
3. Endurhlaðið síðuna.
4. Smellt er á Sýna víddir.
5. Smellið á „Í lagi“.
6. Lokið síðunni.


