---
title: Frumstilla birgðastöðu í vöruhúsi
description: Þetta ferli sýnir hvernig á að uppfæra lagerbirgðir handvirkt með því að nota færslubók birgðahreyfinga.
author: perlynne
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0746b799c701c569f0ae5c657ac3302ab6626287
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823482"
---
# <a name="initialize-stock-levels-in-the-warehouse"></a>Frumstilla birgðastöðu í vöruhúsi

[!include [banner](../../includes/banner.md)]

Þetta ferli sýnir hvernig á að uppfæra lagerbirgðir handvirkt með því að nota færslubók birgðahreyfinga. (Einnig er hægt að uppfæra lagerbirgðir með því að flytja inn færslur í gagnaeigind.) Hægt er að keyra þessa handbók í sýnifyrirtækinu USMF, þar sem öll frumskilyrði eins og heiti færslubókar, uppsetning á vörum, bókunarreglur og lyklar eru í boði. Leiðbeiningarnar stinga upp á ákveðnum gildum fyrir vöruna og víddir sem eru notaðar. Ef þú velur aðra vöru gætirðu þurft að færa inn gildi fyrir aðrar víddir.

1. Fara í Birgðastjórnun > Færslubókarfærslur > Vörur > Hreyfing.
2. Smellið á „Nýtt“.
3. Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.
4. Veldu IMov.
    * Það eru góðar starfsvenjur að nota önnur sniðmát fyrir heiti færslubókar fyrir mismunandi viðskiptatilgang.  
5. Í listanum skal smella á tengilinn í valinni línu.
6. Í reitinn Mótlykill skal tilgreina gildin '140200'.
    * Þetta er mótlykill sem verður sjálfgefinn lykill í færslubókarlínum. Það er hægt að hnekkja sjálfgildinu til að úthluta öðrum mótlyklum á hverja línu.  
7. Smellið á „Í lagi“.
8. Smellið á „Nýtt“.
9. Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.
10. Velja vöru A0001.
11. Í listanum skal smella á tengilinn í valinni línu.
12. Smellið á flipann Birgðavíddir.
13. Í reitnum svæði skal smella á fellilistahnappinn til að opna leitina.
14. Velja svæði 1.
15. Í reitnum vöruhús skal smella á fellilistahnappinn til að opna leitina.
16. Velja vöruhús 13.
17. Í listanum skal smella á tengilinn í valinni línu.
18. Í reitnum staðsetning skal smella á fellilistahnappinn til að opna leitina.
19. Velja staðsetningu 13.
20. Færið inn númer í reitnum „Magn“.
21. Smellið á „Vista“.
22. Smellið á „Bóka“.
23. Merkja eða afmerkja í gátreitinn Millifæra allar bókunarvillur í nýja færslubók.
    * Ef þú virkjar þennan valkost verða allar línur sem ekki bókast afritaðar í nýja færslubók. Hægt er að nota upplýsingarnar í skránni til að leiðrétta vandamál og síðan endurbóka línurnar.  
24. Smellið á „Í lagi“.
25. Lokið síðunni.
26. Lokið síðunni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]