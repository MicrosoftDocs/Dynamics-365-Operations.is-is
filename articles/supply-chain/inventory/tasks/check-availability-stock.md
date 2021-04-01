---
title: Athuga framboð birgðaframboð
description: Þetta ferli sýnir hvernig athuga birgðir á lager og efnislegar lagerbirgðir fyrir ákveðið vörunúmer.
author: ShylaThompson
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand, InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c2153117d9c921b43658edeade49a8403553e371
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238063"
---
# <a name="check-the-availability-of-stock"></a>Athuga framboð birgðaframboð

[!include [banner](../../includes/banner.md)]

Þetta ferli sýnir hvernig athuga birgðir á lager og efnislegar lagerbirgðir fyrir ákveðið vörunúmer. Það sýnir líka hvernig á að fá upplýsingar um framboð tengdar vöru. Lagerbirgðir sem eru efnislegar birgðir eru tiltækar birgðir á lager – sem hafa verið keyptar, mótteknar og skráðar. Lagerbirgðir innihalda tiltækar birgðir á lager, en einnig birgðirnar sem hafa verið pantaðar og er vænst en hafa ekki enn verið mótteknar og skráðar. Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn. Ef verið er að nota USMF má nota dæmagildin sem eru sýndar. Þessi verkefnum myndu venjulega vera framkvæmd af starfsmanni í vöruhúsi.


## <a name="check-on-hand-inventory-for-an-item"></a>Kanna birgðir á lager fyrir vöru
1. Fara í **Skoðunarglugga > Kerfiseiningar > Birgðastjórnun > Fyrirspurnir og skýrslur > Birgðir á lager**.
2. Velurðu **línu vörunúmers**. Til að spyrjast fyrir um birgðir á lager eftir vörunúmeri, veljið línuna þar sem Taflan er stillt á **Birgðir á lager** og reitur er stilltur á **Vörunúmer**.
3. Í reitnum **Skilyrði** velurðu vöruna sem þú vilt gera fyrirspurn um. Ef verið er að nota sýnigögn USMF-fyrirtækis er hægt að velja 'M9201'.  
4. Smellt er á **OK**.
5. Í **Aðgerðasvæði** er smellt á **Víddir**. Flipinn **Víddir** leyfir að velja hversu miklar upplýsingar til að sjá um birgðir á lager. Ef þarf gögn sem tengjast frátekningu, verður að birta birgðavíddir á vörum sem nota ferli ítarlegrar vöruhúsa (WMS).
6. Smellt er á **OK**.
7. Á **Aðgerðasvæðinu** skal smellt á **Tengdar upplýsingar**. Ef það sést ekki, gæti þurft að smella á hnappinn „Úrfellingarmerki“ (…) til að sjá fleiri valkosti aðgerðasvæðis.
8. Smelltu á **Birgðayfirlit**. Flipinn **Birgðayfirlit** veitir birgðaupplýsingar fyrir tiltekna vöru, eins og magn á lager, afhendingartíma og lánardrottnaupplýsingar.  
9. Víkkið út hlutann **Á lager**.
10. Stækkaðu hlutann **Lánardrottnar**.
11. Lokið síðunni.
12. Lokið síðunni.

## <a name="check-physical-on-hand-inventory"></a>Athuga Efnislegar lagerbirgðir
1. Fara í **Skoðunarglugga > Kerfiseiningar > Vöruhússtjórnun > Fyrirspurnir og skýrslur > Efnislegar lagerbirgðir**.
2. Í reitnum **Vörunúmer** skal slá inn gildi. Hægt er að nota svæðin Svæðis og Vöruhúss til að sía listann yfir vörur. 
3. Endurhlaðið síðuna.
4. Í **Aðgerðasvæði** er smellt á **Sýna víddir**. Birtingarflipinn Víddir gerir kleift að velja hversu miklar upplýsingar til að sjá um birgðir á lager.
5. Smellt er á **OK**.
6. Lokið síðunni.

## <a name="check-on-hand-inventory-by-location"></a>Athuga Birgðir eftir staðsetningu
1. Fara í **Skoðunarglugga > Kerfiseiningar > Vöruhússtjórnun > Fyrirspurnir og skýrslur > Á lager eftir staðsetningu**.
2. Í reitinn **Vöruhús** skal slá inn gildi. Ef verið er að nota USMF sýnigögn fyrirtæki er hægt að nota '51'.  
3. Endurhlaðið síðuna.
4. Smelltu á **Sýna víddir**.
5. Smellt er á **OK**.
6. Lokið síðunni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]