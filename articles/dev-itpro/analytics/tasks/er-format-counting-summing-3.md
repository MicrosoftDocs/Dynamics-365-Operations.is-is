---
title: Rafræn skýrslugerð skilgreingasnið sér um að telja og leggja saman (Hluti 3 - Nota útreikninga til að búa til úttak)
description: Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) til að telja og taka saman á grundvelli gagna textaúttaks sem þegar var myndað.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c870c134a9dae81cd619268bed7ce545bdd5f52
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544611"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3-use-computations-to-make-the-output"></a>Rafræn skýrslugerð skilgreingasnið sér um að telja og leggja saman (Hluti 3: Nota útreikninga til að búa til úttak)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) til að telja og taka saman á grundvelli gagna textaúttaks sem þegar var myndað. Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.

Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í á "Rafræn skýrslugerð skilgreingasnið sér um að telja og taka saman (Hluti 2: skilgreina útreikninga)" ferli.

Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.


## <a name="configure-this-report-to-use-counting-and-summing-info"></a>Skilgreina þessa skýrslu til að nota upplýsingar um talningu og samlagningu
1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
2. Smelltu á Grunnstillingar skýrslugerðar
3. Í trénu skal víkka út 'Intrastat model'.
4. Í trénu skal víkka út 'Intrastat model\Intrastat (DE)'.
5. Í trénu skal velja „Intrastat model\Intrastat (DE)\Intrastat (DE) með talningu & samlagningu“.
6. Smellið á Hönnuður.
7. Smelltu á flipann Vörpun.
8. Smelltu á Bæta við rót til að opna felligluggann.
    * Bæta við nýjum gagnagjafa til að fá lista yfir blokkir sem voru lagðar á minni.  
9. Veljið 'Functions\Calculated svæðið', í trénu.
10. Í svæðið Heiti, færðu inn '$BlocksList'.
    * $BlocksList  
11. Smellt er á Breyta formúla.
12. Í trénu skal velja 'Data collection functions\COLLECTEDLIST'.
13. Smelltu á Bæta við Aðgerð.
14. Smellt er á Bæta við gagnagjafa.
15. Í Formúlu svæðinu, færið inn 'COLLECTEDLIST('$BlockName', '.
    * COLLECTEDLIST('$BlockName',  
16. Í Formúlu svæðinu, færið inn 'COLLECTEDLIST('$BlockName', "*")'.
    * COLLECTEDLIST('$BlockName', "*")  
17. Smellið á „Vista“.
    * Mynstrið “*” þýðir að allar blokkir verða teknar með í lista fyrir þessa færslu.  
18. Lokið síðunni.
19. Smellið á „Í lagi“.
20. Smellið á flipann snið.
21. Í trénu skal velja 'Intrastat\Data'.
22. Smelltu á Bæta við til að opna felligluggann.
23. Í trénu skal velja 'Text\Sequence'.
24. Í svæðið Heiti, færðu inn 'Samtölur eftir blokkum'.
    * Samtölur eftir blokkum  
25. Í reitnum sérstafir skal velja "ný lína - Windows (CR LF)".
26. Smellt er á Í lagi.
27. Í trénu skal velja 'Intrastat\Data\Totals by blocks'.
28. Smelltu á Bæta við til að opna felligluggann.
29. Í trénu skal velja ‚Texti/Strengur'.
30. Í svæðið Heiti, færðu inn "kóði blokkar"
    * Kóði blokkar  
31. Smellið á „Í lagi“.
32. Smella á bæta Við Streng.
33. Í svæðið Heiti, færðu inn 'talning lína'.
    * Talning lína  
34. Smellið á „Í lagi“.
35. Smella á bæta Við Streng.
36. Í svæðið Heiti, færðu inn 'heildarupphæð'.
    * Heildarfjöldi  
37. Smellið á „Í lagi“.
38. Smelltu á flipann Vörpun.
39. Í trénu skal velja '$BlocksList'.
40. Smelltu á Binda.
    * Stofna línu fyrir hverja blokk sem er lögð á minni.  
41. Smellið á flipann snið.
42. Í trénu skal velja 'Intrastat\Data\Totals by blocks\Block code'.
43. Smelltu á flipann Vörpun.
44. Smellt er á Breyta formúla.
45. Í reitinn Formúla skal færa inn „„Kenni blokkar: “ & “.
    * „Kenni blokkar: “ &  
46. Í trénu skal víkka út '$BlocksList'.
47. Í trénu skal velja '$BlocksList\Value'.
48. Smellt er á Bæta við gagnagjafa.
49. Smellið á „Vista“.
50. Lokið síðunni.
51. Smellið á flipann snið.
52. Í trénu skal velja 'Intrastat\Data\Totals by blocks\Lines counting'.
53. Smelltu á flipann Vörpun.
54. Smellt er á Breyta formúla.
    * Stofna úttak fyrir fjölda lína fyrir hverja blokk sem er sýnd í þessari skýrslu.  
55. Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& “.
    * „Fjöldi lína í þessari blokk“ &  
56. Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& TEXT(“.
    * „fjöldi lína í þessari blokk:“ .& TEXT(  
57. Í trénu skal velja 'Data collection functions\COUNTIFS'.
58. Smelltu á Bæta við Aðgerð.
59. Smellt er á Bæta við gagnagjafa.
60. Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& TEXT(COUNTIFS(„$BlockName“, “.
    * „Fjöldi lína í þessari blokk: “ & TEXT(COUNTIFS(„$BlockName“,  
61. Í trénu skal víkka út '$BlocksList'.
62. Í trénu skal velja '$BlocksList\Value'.
63. Smellt er á Bæta við gagnagjafa.
64. Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& TEXT(COUNTIFS(„$BlockName“, „$BlocksList“.Value, “.
    * „Fjöldi lína í þessari blokk: “ & TEXT(COUNTIFS(„$BlockName“, „$BlocksList“.Value,  
65. Í trénu skal velja '$RecName'.
66. Smellt er á Bæta við gagnagjafa.
67. Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& TEXT(COUNTIFS(„$BlockName“, „$BlocksList“.Value, „$RecName“, „*“))“.
    * „Fjöldi lína í þessari blokk: “ & TEXT(COUNTIFS(„$BlockName“, „$BlocksList“.Value, „$RecName“, „*“))  
68. Smellið á „Vista“.
69. Lokið síðunni.
70. Smellið á flipann snið.
71. Í trénu skal velja 'Intrastat\Data\Totals by blocks\Total amount'.
72. Smelltu á flipann Vörpun.
73. Smellt er á Breyta formúla.
    * Stofna úttak sem verður heildarupphæð reikningsfærðrar upphæðar fyrir hverja blokk sem er sýnd í þessari skýrslu.  
74. Í reitnum formúla skal færa inn „„Samtala reikningsfærðra upphæða:"  TEXT(SUMIFS(„$InvName“, „$BlockName“, „$BlocksList“.Value, „$RecName“, „*“))“.
    * „Samtala reikningsfærðra upphæða:"  TEXT(SUMIFS(„$InvName“, „$BlockName“, „$BlocksList“.Value, „$RecName“, „*“))  
75. Smellið á „Vista“.
76. Lokið síðunni.
77. Smellið á „Vista“.
78. Lokið síðunni.

