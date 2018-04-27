--- 
title: "Hanna gagnalíkan til að nota fjárhagsvíddir sem gagnaveitu"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt líkan rafrænnar skýrslugerðar (ER) svo það noti fjárhagsvíddir sem gagnaveitu fyrir rafrænar skýrslur."
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 3e55eedba1955ae79733afee1a0b3c7072147bb5
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="design-data-model-to-use-financial-dimensions-as-a-data-source"></a>Hanna gagnalíkan til að nota fjárhagsvíddir sem gagnaveitu 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt líkan rafrænnar skýrslugerðar (ER) svo það noti fjárhagsvíddir sem gagnaveitu fyrir rafrænar skýrslur. Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.

Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu “Stofna skilgreiningarveitu og merkja hana sem virka”.


## <a name="create-a-new-data-model"></a>Búa til nýtt gagnalíkan
1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
    * Gakktu úr skugga um að „Litware, Inc.“ veitandi sé tiltæk og merkt Virk.  
2. Smelltu á Grunnstillingar skýrslugerðar
3. Smellt er á stofna skilgreiningu til að opna fellilistanum.
4. Í svæðið Heiti, Færðu inn 'Dæmi um líkan fyrir fjárhagsvíddir'.
5. Smelltu á Stofna skilgreiningu.
6. Smellið á Hönnuður.
7. Smellt er á Nýtt til að opna felligluggann.
8. Í reitnum Heiti skal færa inn 'Færsla'.
9. Smelltu á Bæta við.
10. Smellt er á Nýtt til að opna felligluggann.
11. Í reitnum Heiti skal færa inn ‚Fyrirtæki‘.
12. Smelltu á Bæta við.
    * Við bætum nýjum skáarlista við líkanið okkar. Listinn mun sýna (fyrir allar rafrænar skýrslur sem nota þetta líkan sem gagnagjafa) stillingar fyrir valdar fjárhagsvíddir. Hver fjárhagsvídd verða sýnd á þessum lista sem færsla með viðeigandi svæði sem tákna stillingar víddar.  
13. Smellt er á Nýtt til að opna felligluggann.
14. Í reitnum Heiti skal færa inn 'Grunnstilling vídda'.
15. Veljið í svæðinu gerð Vöru „Skrárlisti".
16. Smelltu á Bæta við.
17. Smellt er á Nýtt til að opna felligluggann.
18. Í reitnum Heiti skal færa inn 'kóði'.
19. Veljið 'Strengur' í svæðinu Vöru.
20. Smelltu á Bæta við.
21. Smellt er á Nýtt til að opna felligluggann.
22. Í svæðið Heiti, færðu inn ‚Heiti'.
23. Smelltu á Bæta við.
24. Í trénu skal velja „færsla“.
25. Smellt er á Nýtt til að opna felligluggann.
26. Í reitnum Heiti skal færa inn 'færslubók'.
27. Veljið í svæðinu gerð Vöru „Skrárlisti".
28. Smelltu á Bæta við.
29. Smellt er á Nýtt til að opna felligluggann.
30. Í reitnum Heiti skal færa inn 'runa'.
31. Veljið 'Strengur' í svæðinu Vöru.
32. Smelltu á Bæta við.
33. Smellt er á Nýtt til að opna felligluggann.
34. Í reitnum Heiti skal færa inn ‚færsla'.
35. Veljið í svæðinu gerð Vöru „Skrárlisti".
36. Smelltu á Bæta við.
37. Smellt er á Nýtt til að opna felligluggann.
38. Í reitnum Heiti skal færa inn ‚dagsetning'.
39. Velja 'Dagsetning' í svæðinu gerð vöru.
40. Smelltu á Bæta við.
41. Smellt er á Nýtt til að opna felligluggann.
42. Í reitnum Heiti skal færa inn ‚debetfæra'.
43. Veljið 'Raunveruleg' í svæðinu gerð vöru.
44. Smelltu á Bæta við.
45. Smellt er á Nýtt til að opna felligluggann.
46. Í svæðið Heiti, færðu inn 'kreditfæra'.
47. Smelltu á Bæta við.
48. Smellt er á Nýtt til að opna felligluggann.
49. Í svæðið Heiti, færðu inn 'Gjaldmiðils'.
50. Veljið 'Strengur' í svæðinu Vöru.
51. Smelltu á Bæta við.
52. Smellt er á Nýtt til að opna felligluggann.
53. Í reitnum Heiti skal færa inn ‚fylgiskjal'.
54. Smelltu á Bæta við.
55. Smellt er á Nýtt til að opna felligluggann.
56. Í reitnum Heiti skal færa inn 'gögn um víddir'.
57. Veljið í svæðinu gerð Vöru „Skrárlisti".
58. Smelltu á Bæta við.
    * Við bættum nýjum færslulista við líkanið okkar. Listinn mun sýna (fyrir allar rafrænar skýrslur sem nota þetta líkan sem gagnagjafa) gildi fyrir valdar fjárhagsvíddir. Hver fjárhagsvídd verða sýnd á þessum lista sem færsla með viðeigandi svæði sem tákna Gildi víddar. Heiti víddar verður einnig sýnt í þessari færslu sem svæði til að nota, ef þörf krefur, til að geta valið úr.  
59. Smellt er á Nýtt til að opna felligluggann.
60. Í reitnum Heiti skal færa inn 'kóði'.
61. Veljið 'Strengur' í svæðinu Vöru.
62. Smelltu á Bæta við.
63. Smellt er á Nýtt til að opna felligluggann.
64. Í reitnum Heiti skal færa inn ‚Lýsing'.
65. Smelltu á Bæta við.
66. Smellt er á Nýtt til að opna felligluggann.
67. Í svæðið Heiti, færðu inn ‚Heiti'.
68. Smelltu á Bæta við.
69. Smellið á „Vista“.
70. Lokið síðunni.


