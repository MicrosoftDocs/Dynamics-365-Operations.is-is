---
title: Setja upp bókunarreglur fyrir eignir
description: Þessi leiðarvísi fyrir verk setja upp bókunarreglur eigna.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07961d8613b6b5e0e1c5dc6a91b554305dcb17f5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444444"
---
# <a name="set-up-fixed-asset-posting-profiles"></a>Setja upp bókunarreglur fyrir eignir

[!include [banner](../../includes/banner.md)]

Þessi leiðarvísi fyrir verk setja upp bókunarreglur eigna.  Það notar Bókari hlutverk og sýnigögn fyrir USMF lögaðila.  Dæmi í leiðarvísi fyrir verk eru fyrir grunn bókunarreglu, þó verður að stofna bókunarreglur fyrir tiltekinn bókhaldslykil og kröfur fyrir fjárhagsskýrslu.

1. Í skoðunarrúðnni ferðu í **Kerfseiningar > Fastafjármunir > Uppsetning > Bókunarreglur fastafjármuna**.
2. Smellt er á **Nýtt**.
3. Í reitinn **bókunarregla** skal færa inn gildi.
4. Í reitinn **Lýsing** skal slá inn gildi. Þarf að stofna bókunarreglu fyrir hverja tegund eignafærslu sem verður notuð þegar unnið er með eignir. Þessi leiðarvísi fyrir verk byrja á ferðinni kaupfærsla.  
5. Smellið á **Bæta við** á tækjastikunni.
6. Sláið inn eða veldu gildi í reitnum **Bók**. svæðið **Flokkanir** gerir kleift að skilgreina bókunarreglu niður í Töflu (einum lykli sett upp fyrir hverja eign) eða Flokkur (einum lykli sett upp fyrir hvern eignaflokk). Í þessum verkefnaleiðbeiningar skal skilja eftir gildið stillt á „Allt“ til að nota á allar eignir í tilgreinda bók.  
7. Í reitnum **Aðallykill** skal skilgreina æskileg gildi. Fyrir Kaup, hægt að færa inn mótlykil eða hafa það autt til að fylla út fyrir tiltekna færslu.    
8. Í fellivalmyndinni undir flýtiflipanum **Fjárhagslyklar**, veldu „Aðlögun yfirtöku“. Fyrir Leiðréttingarfærslna kaupa, nota sömu lyklar sem notað fyrir kaupfærsla.  
9. Smelltu á **Bæta við**.
10. Sláið inn eða veldu gildi í reitnum **Bók**.
11. Í reitnum **Aðallykill** skal skilgreina æskileg gildi. Fyrir leiðréttingar Kaupa hægt að færa inn mótlykil eða skilja eftir autt til að fylla út fyrir tiltekna færslu.    
12. Í fellivalmyndinni undir flýtiflipanum **Fjárhagslyklar**, veldu „Afskrift“.
13. Smelltu á **Bæta við**.
14. Sláið inn eða veldu gildi í reitnum **Bók**.
15. Í reitnum **Aðallykill** skal skilgreina æskileg gildi.
16. Í reitnum **Mótlykill** skal skilgreina æskileg gildi.
17. Í fellivalmyndinni undir flýtiflipanum **Fjárhagslyklar**, veldu „Aðlögun afskrifta“. Fyrir Leiðréttingarfærslna afskrift, nota sömu lyklar sem notað fyrir afskriftarfærsla.  
18. Smelltu á **Bæta við**.
19. Sláið inn eða veldu gildi í reitnum **Bók**.
20. Í reitnum **Aðallykill** skal skilgreina æskileg gildi.
21. Í reitnum **Mótlykill** skal skilgreina æskileg gildi.
22. Í fellivalmyndinni undir flýtiflipanum **Fjárhagslyklar**, veldu „Losun - sala“.
23. Smelltu á **Bæta við**.
24. Sláið inn eða veldu gildi í reitnum **Bók**.
25. Í reitnum **Aðallykill** skal skilgreina æskileg gildi. Fyrir afskráningar, hægt að færa inn mótlykil eða skilja eftir autt til að fylla út fyrir tiltekna færslu.  
26. Í fellivalmyndinni undir flýtiflipanum **Fjárhagslyklar**, veldu „Losun - henda“. Nota sömu lyklar fyrir Losun sölu og Losun rýrnunar.  
27. Smelltu á **Bæta við**.
28. Sláið inn eða veldu gildi í reitnum **Bók**.
29. Í reitnum **Aðallykill** skal skilgreina æskileg gildi. Fyrir afskráningar, hægt að færa inn mótlykil eða skilja eftir autt til að fylla út fyrir tiltekna færslu.  
30. Útvíkka **Losun** flýtiflipa. Setja verður upp bókunarreglur afskráningar fyrir sölu og rýrnun.  byrjað verður á sölufærslu afskráningar  
31. Smelltu á **Bæta við**.
32. Sláið inn eða veldu gildi í reitnum **Bók**.
33. í svæðinu **Bóka gildi** Veljið 'Kaupvirði'.
    * Kaupvirði verður á við um Kaup og leiðréttinggildi kaupa fyrir öll árin. Einnig er hægt að skilgreina lykla fyrir þessar færslugerð sérstaklega.  
    * Hægt er að setja afskráningarferlið til að nota á mismunandi lykla eftir því hvort afskráning leiðir hagnaður eða taps. Gerð söluvirði verður stillt á „Allt” til að nota sömu lyklar fyrir allar gerðir afskráningar.  
34. Í reitnum **Aðallykill** skal skilgreina æskileg gildi.
35. Í reitnum **Mótlykill** skal skilgreina æskileg gildi.
36. Smelltu á **Bæta við**.
37. Sláið inn eða veldu gildi í reitnum **Bók**.
38. Veljið 'Afskriftir (fyrri ár)' í svæðinu **Bóka gildi**.  
38. Í reitnum **Aðallykill** skal skilgreina æskileg gildi.
39. Í reitnum **Mótlykill** skal skilgreina æskileg gildi.
40. Smelltu á **Bæta við**.
41. Sláið inn eða veldu gildi í reitnum **Bók**.
42. Veljið 'Afskriftir (fyrri ár)' í svæðinu **Bóka gildi**.
43. Í reitnum **Aðallykill** skal skilgreina æskileg gildi.
44. Í reitnum **Mótlykill** skal skilgreina æskileg gildi.
45. Smelltu á **Bæta við**.
46. Sláið inn eða veldu gildi í reitnum **Bók**.
47. Veljið í svæðinu **Bóka gildi** 'Afskriftaleiðréttingar (fyrra árs)'.
48. Í reitnum **Aðallykill** skal skilgreina æskileg gildi.
49. Í reitnum **Mótlykill** skal skilgreina æskileg gildi.
50. Smelltu á **Bæta við**.
51. Sláið inn eða veldu gildi í reitnum **Bók**.
52. Veljið í svæðinu **Bóka gildi** 'Afskriftaleiðréttingar (þessa árs)'.
53. Í reitnum **Aðallykill** skal skilgreina æskileg gildi.
54. Í reitnum **Mótlykill** skal skilgreina æskileg gildi.
55. Smelltu á **Bæta við**.
56. Sláið inn eða veldu gildi í reitnum **Bók**.
57. Veljið "Bókað nettóvirði" í svæðinu **Bóka gildi**.
58. Í reitnum **Aðallykill** skal skilgreina æskileg gildi.
59. Í reitnum **Mótlykill** skal skilgreina æskileg gildi.
60. Veljið "Rýrnun" í reitnum **Sala eða rýrnun**.
61. Smelltu á **Bæta við**.
62. Sláið inn eða veldu gildi í reitnum **Bók**.
63. í svæðinu **Bóka gildi** Veljið 'Kaupvirði'.
64. Í reitnum **Aðallykill** skal skilgreina æskileg gildi.
65. Í reitnum **Mótlykill** skal skilgreina æskileg gildi.
66. Smelltu á **Bæta við**.
67. Sláið inn eða veldu gildi í reitnum **Bók**.
67. Í svæðinu **Bóka gildi**, veljið "Afskriftir (fyrri ár)".  
68. Í reitnum **Aðallykill** skal skilgreina æskileg gildi.
69. Í reitnum **Mótlykill** skal skilgreina æskileg gildi.
70. Smelltu á **Bæta við**.
71. Sláið inn eða veldu gildi í reitnum **Bók**.
72. Veljið 'Afskriftir (fyrri ár)' í svæðinu **Bóka gildi**.
73. Í reitnum **Aðallykill** skal skilgreina æskileg gildi.
74. Í reitnum **Mótlykill** skal skilgreina æskileg gildi.
75. Smelltu á **Bæta við**.
76. Sláið inn eða veldu gildi í reitnum **Bók**.
77. Veljið í svæðinu **Bóka gildi** 'Afskriftaleiðréttingar (fyrra árs)'.
78. Í reitnum **Aðallykill** skal skilgreina æskileg gildi.
79. Í reitnum **Mótlykill** skal skilgreina æskileg gildi.
80. Smelltu á **Bæta við**.
81. Sláið inn eða veldu gildi í reitnum **Bók**.
82. Veljið í svæðinu **Bóka gildi** 'Afskriftaleiðréttingar (þessa árs)'.
83. Í reitnum **Aðallykill** skal skilgreina æskileg gildi.
84. Í reitnum **Mótlykill** skal skilgreina æskileg gildi.
85. Smelltu á **Bæta við**.
86. Sláið inn eða veldu gildi í reitnum **Bók**.
87. Veljið "Bókað nettóvirði" í svæðinu **Bóka gildi**.
88. Í reitnum **Aðallykill** skal skilgreina æskileg gildi.
89. Í reitnum **Mótlykill** skal skilgreina æskileg gildi.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]