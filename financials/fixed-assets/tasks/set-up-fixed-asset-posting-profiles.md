--- 
title: "Setja upp bókunarreglur fyrir eignir"
description: "Þessi leiðarvísi fyrir verk setja upp bókunarreglur eigna."
author: saraschi2
manager: AnnBe
ms.date: 02/24/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: f2fd3c8cfa63e11a0bf4e5e095375d024c9d45ce
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-fixed-asset-posting-profiles"></a>Setja upp bókunarreglur fyrir eignir

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þessi leiðarvísi fyrir verk setja upp bókunarreglur eigna.  Það notar Bókari hlutverk og sýnigögn fyrir USMF lögaðila.  Dæmi í leiðarvísi fyrir verk eru fyrir grunn bókunarreglu, þó verður að stofna bókunarreglur fyrir tiltekinn bókhaldslykil og kröfur fyrir fjárhagsskýrslu.

1. Fara í eignir > Uppsetning > Bókunarreglur eigna.
2. Smellið á „Nýtt“.
3. Í reitinn bókunarregla skal færa inn gildi.
4. Sláið inn gildi í reitnum „Lýsing“.
    * Þarf að stofna bókunarreglu fyrir hverja tegund eignafærslu sem verður notuð þegar unnið er með eignir.  Þessi leiðarvísi fyrir verk byrja á ferðinni kaupfærsla.  
5. Smelltu á Bæta við.
6. Sláið inn eða veldu gildi í reitnum Bók.
    * svæðið Flokkanir gerir kleift að skilgreina bókunarreglu niður í Töflu (einum lykli sett upp fyrir hverja eign) eða Flokkur (einum lykli sett upp fyrir hvern eignaflokk).  Í þessum verkefnaleiðbeiningar skilja eftir gildið stillt á „Allt“ til að nota á allar eignir í tilgreindan bók.  
7. Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.
    * Fyrir Kaup, hægt að færa inn mótlykil eða hafa það autt til að fylla út fyrir tiltekna færslu.    
8. Í reitnum færslugerð er valinn leiðrétting kaupa.
    * Fyrir Leiðréttingarfærslna kaupa, nota sömu lyklar sem notað fyrir kaupfærsla.  
9. Smelltu á Bæta við.
10. Sláið inn eða veldu gildi í reitnum Bók.
11. Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.
    * Fyrir leiðréttingar Kaupa hægt að færa inn mótlykil eða skilja eftir autt til að fylla út fyrir tiltekna færslu.    
12. Í reitnum færslugerð er valinn afskrift.
13. Smelltu á Bæta við.
14. Sláið inn eða veldu gildi í reitnum Bók.
15. Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.
16. Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.
17. Í reitnum færslugerð er valinn leiðrétting afskriftar.
    * Fyrir Leiðréttingarfærslna afskrift, nota sömu lyklar sem notað fyrir afskriftarfærsla.  
18. Smelltu á Bæta við.
19. Sláið inn eða veldu gildi í reitnum Bók.
20. Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.
21. Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.
22. Í reitnum færslugerð er valinn afskráning - Sala.
23. Smelltu á Bæta við.
24. Sláið inn eða veldu gildi í reitnum Bók.
25. Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.
    * Fyrir afskráningar, hægt að færa inn mótlykil eða skilja eftir autt til að fylla út fyrir tiltekna færslu.  
26. Í reitnum færslugerð er valinn afskráning - rýrnun.
    * nota sömu lyklar fyrir Losun sölu og Losun rýrnunar.  
27. Smelltu á Bæta við.
28. Sláið inn eða veldu gildi í reitnum Bók.
29. Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.
    * Fyrir afskráningar, hægt að færa inn mótlykil eða skilja eftir autt til að fylla út fyrir tiltekna færslu.  
30. Víkka hlutann Förgun.
    * Setja verður upp bókunarreglur afskráningar fyrir sölu og rýrnun.  byrjað verður á sölufærslu afskráningar  
31. Smelltu á Bæta við.
32. Sláið inn eða veldu gildi í reitnum Bók.
33. í svæðinu Bóka gildi Veljið 'Kaupvirði'.
    * Kaupvirði verður á við um Kaup og leiðréttinggildi kaupa fyrir öll árin.  Einnig er hægt að skilgreina lykla fyrir þessar færslugerð sérstaklega.  
    * Hægt er að setja afskráningarferlið til að nota á mismunandi lykla eftir því hvort afskráning leiðir hagnaður eða taps.  Gerð söluvirði verður stillt á "Allt" til að nota sömu lyklar fyrir allar gerðir afskráningar.  
34. Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.
35. Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.
36. Smelltu á Bæta við.
37. Sláið inn eða veldu gildi í reitnum Bók.
    * Veljið 'Afskriftir (fyrri ár)' í svæðinu Bóka gildi.  
38. Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.
39. Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.
40. Smelltu á Bæta við.
41. Sláið inn eða veldu gildi í reitnum Bók.
42. Veljið 'Afskriftir (fyrri ár)' í svæðinu Bóka gildi.
43. Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.
44. Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.
45. Smelltu á Bæta við.
46. Sláið inn eða veldu gildi í reitnum Bók.
47. Veljið í svæðinu Bóka gildi 'Afskriftaleiðréttingar (fyrra árs)'.
48. Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.
49. Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.
50. Smelltu á Bæta við.
51. Sláið inn eða veldu gildi í reitnum Bók.
52. Veljið í svæðinu Bóka gildi 'Afskriftaleiðréttingar (þessa árs)'.
53. Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.
54. Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.
55. Smelltu á Bæta við.
56. Sláið inn eða veldu gildi í reitnum Bók.
57. Veljið "Bókað nettóvirði" í svæðinu Bóka gildi.
58. Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.
59. Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.
60. Veljið "Rýrnun" í reitnum Sala eða rýrnun.
61. Smelltu á Bæta við.
62. Sláið inn eða veldu gildi í reitnum Bók.
63. í svæðinu Bóka gildi Veljið 'Kaupvirði'.
64. Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.
65. Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.
66. Smelltu á Bæta við.
67. Sláið inn eða veldu gildi í reitnum Bók.
    * Í svæðinu Bóka gildi, veljið "Afskriftir (fyrri ár)".  
68. Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.
69. Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.
70. Smelltu á Bæta við.
71. Sláið inn eða veldu gildi í reitnum Bók.
72. Veljið 'Afskriftir (fyrri ár)' í svæðinu Bóka gildi.
73. Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.
74. Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.
75. Smelltu á Bæta við.
76. Sláið inn eða veldu gildi í reitnum Bók.
77. Veljið í svæðinu Bóka gildi 'Afskriftaleiðréttingar (fyrra árs)'.
78. Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.
79. Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.
80. Smelltu á Bæta við.
81. Sláið inn eða veldu gildi í reitnum Bók.
82. Veljið í svæðinu Bóka gildi 'Afskriftaleiðréttingar (þessa árs)'.
83. Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.
84. Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.
85. Smelltu á Bæta við.
86. Sláið inn eða veldu gildi í reitnum Bók.
87. Veljið "Bókað nettóvirði" í svæðinu Bóka gildi.
88. Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.
89. Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.


