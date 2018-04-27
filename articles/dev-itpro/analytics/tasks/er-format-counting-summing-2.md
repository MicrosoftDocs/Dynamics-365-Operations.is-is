--- 
title: "Grunnstilla útreikninga fyrir talningu og samlagningu"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) til að telja og taka saman á grundvelli gagna textaúttaks sem þegar var myndað."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.openlocfilehash: d41ce101c0b038627e2baf6b5eac2410095af7ce
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="configure-computations-to-do-counting-and-summing"></a>Grunnstilla útreikninga fyrir talningu og samlagningu

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) til að telja og taka saman á grundvelli gagna textaúttaks sem þegar var myndað. Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.

Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í á “Rafræn skýrslugerð skilgreingasnið sér um að telja og taka saman (Hluti 1: stofna snið)” ferli.

Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a>Stofna skilgreiningu á sniði til að bæta við upplýsingar um talningu og samlagningu
1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
2. Smelltu á Grunnstillingar skýrslugerðar
3. Í trénu skal víkka út 'Intrastat model'.
4. Í trénu skal velja 'Intrastat model\Intrastat (DE)'.
    * Gefum okkur að sérsníða þurfi sniðið sem Microsoft útvegar með því að bæta línum með samantektarupplýsingum við lok intrastat-skýrslu. Þú gerir það með því að sækja okkar eigin tilvik af intrastat-skilgreiningu úr Microsoft-tilvikinu til að gera breytingar.  
5. Smellt er á stofna skilgreiningu til að opna fellilistanum.
6. Í svæðinu Nýtt, veljið 'Leiða af nafni: Intrastat (DE), Microsoft'.
7. Í svæðið Heiti, sláðu inn „Intrastat (DE) með talningu & samlagningu“.
8. Smelltu á Stofna skilgreiningu.

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a>Skilgreina þessa skýrslu til að gera talningu og samlagningu á grundvelli upplýsinga um úttak.
1. Smellið á Hönnuður.
2. Veldu Já í reitnum safna saman upplýsingum um framleiðslu.
    * Þetta flagg virkjar ferlið við að safna saman úttaksupplýsingum til að mynda intrastat-skrána á keyrslutima.  
    * Þú þarft að telja fyrir mismunandi intrastat-stefnur, svo bæta skal sérstakri tölusetningu fyrir líkan við lista gagnaveitu fyrir þessa skilgreiningu sniðs.  
3. Smelltu á flipann Vörpun.
4. Smelltu á Bæta við rót til að opna felligluggann.
5. Í trénu skal velja 'Data model\Enumeration '.
6. Í reitnum Heiti skal færa inn ‚Stefna'.
7. Sláið inn eða veldu gildi í reitnum tölusetning líkans.
    * Veldu gildið Stefna.  
8. Smellið á „Í lagi“.
9. Smelltu á Bæta við rót til að opna felligluggann.
10. Veljið 'Functions\Calculated svæðið', í trénu.
11. Í svæðið Heiti, færðu inn '$BlockName'.
12. Smellt er á Breyta formúla.
13. Í reitinn Formúla skal færa inn '"block"'.
14. Smellið á „Vista“.
15. Lokið síðunni.
16. Smellið á „Í lagi“.
17. Smelltu á Bæta við rót til að opna felligluggann.
18. Veljið 'Functions\Calculated svæðið', í trénu.
19. Í svæðið Heiti, færðu inn '$RecName'.
20. Smellt er á Breyta formúla.
21. Í reitinn Formúla skal færa inn '"record"'.
22. Smellið á „Vista“.
23. Lokið síðunni.
24. Smellið á „Í lagi“.
25. Smelltu á Bæta við rót til að opna felligluggann.
26. Veljið 'Functions\Calculated svæðið', í trénu.
27. Í svæðið Heiti, færðu inn '$InvName'.
28. Smellt er á Breyta formúla.
29. Í reitinn Formúla skal færa inn '"InvoicedAmountEUR"'.
30. Smellið á „Vista“.
31. Lokið síðunni.
32. Smellið á „Í lagi“.
33. Í trénu skal velja 'Intrastat\Data'.
34. Smeltu á hnappinn breyta fyrir reitinn ‘heiti lykils fyrir söfnuð gögn’.
35. Smellt er á Bæta við gagnagjafa.
    * $BlockName  
36. Smellið á „Vista“.
37. Lokið síðunni.
38. Smellið á hnappinn Breyta fyrir reitinn gildi lykils uppsafnaðra gagna
39. Í reitinn Formúlu skal færa inn 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.
    * IF(Intrastat.CommodityRecord.Direction=Direction.Import, “Import”, “Export”)  
40. Smellið á „Vista“.
41. Lokið síðunni.
    * Telja línur í þessari röð. Niðurstöður verður notað með heitinu "útiloka" aðskilið fyrir mismunandi stefnur. Gildið “Innflutningur” verður notað fyrir allar intrastat-færslur fyrir komur. Gildið “Útflutningur” verður notað fyrir allar intrastat-færslur fyrir sendingar. Líttu á þetta sem sýndar Excel-töflu. Fyrir hverja færslu er lína þar sem fyrsta “blokk” dálkinn er fyllt út með gildunum “Innflutningur” og “Útflutning” til samræmis.  
42. Í trénu skal víkka út 'Intrastat\Data: Sequence'.
43. Í trénu skal velja 'Intrastat\Data: Sequence\Arrivals?'.
44. Smeltu á hnappinn breyta fyrir reitinn ‘heiti lykils fyrir söfnuð gögn’.
    * Telja línur í þessari röð. Niðurstöðurnar eru geymdar í minni með því að nota skrána “færsla”.  
45. Í trénu skal velja '$RecName'.
46. Smellt er á Bæta við gagnagjafa.
47. Smellið á „Vista“.
48. Lokið síðunni.
49. Smeltu á hnappinn breyta fyrir reitinn "gildi lykils fyrir söfnuð gögn".
50. Í Formúlu svæðinu, færið inn 'Intrastat.CommodityRecord.CommodityCode'.
51. Smellið á „Vista“.
52. Lokið síðunni.
    * Telja línur í þessari röð. Niðurstöður verður notað með heitinu “færsla” aðskilið fyrir mismunandi vörukóða. Líttu á þetta sem sýndar Excel-töflu. Fyrir hverja færslu er lína þar sem fyrsta “blokk” dálkinn er fyllt út með gildunum "Innflutningur" og “Útflutning” til samræmis og næsta blokkin “færsla” er fyllt með gildi vörukóða.  
53. Í trénu skal velja 'Intrastat\Data: Sequence\Dispatches?'.
54. Smeltu á hnappinn breyta fyrir reitinn ‘heiti lykils fyrir söfnuð gögn’.
55. Í trénu skal velja '$RecName'.
56. Smellt er á Bæta við gagnagjafa.
57. Smellið á „Vista“.
58. Lokið síðunni.
59. Smeltu á hnappinn breyta fyrir reitinn "gildi lykils fyrir söfnuð gögn".
60. Í Formúlu svæðinu, færið inn 'Intrastat.CommodityRecord.CommodityCode'.
61. Smelltu á Vista.
62. Lokið síðunni.
63. Í trénu skal víkka út 'Intrastat\Data: Sequence\Dispatches: Sequence?'.
64. Í trénu skal víkka út 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record = Intrastat.CommodityRecord'.
65. Smellið á flipann snið.
66. Í trénu skal velja 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.
67. Smelltu á flipann Vörpun.
68. Smeltu á hnappinn breyta fyrir reitinn ‘heiti lykils fyrir söfnuð gögn’.
69. Í trénu skal velja '$InvName'.
70. Smellt er á Bæta við gagnagjafa.
71. Smellið á „Vista“.
72. Lokið síðunni.
    * Taka saman gildi reikningsfærð upphæð fyrir línur í þessari röð. Niðurstöður verður notað með heitinu “InvoicedAmountEUR” aðskilið fyrir mismunandi intrastat-stefnur og vörukóða. Líttu á þetta sem sýndarsköpun í Excel-töflu. Fyrir hverja færslu er lína þar sem fyrsta “blokk” dálkinn er fyllt út með gildunum “Innflutningur” og “Útflutning” til samræmis. Önnur blokk "færsla" er fyllt út með gildi vörukóða og þriðja dálkinn "InvoicedAmountEUR" er fyllt út með gildi upphæðar reiknings.  
73. Í trénu skal víkka út 'Intrastat\Data\Arrivals?'.
74. Í trénu skal víkka út 'Intrastat\Data\Arrivals?\Record = Intrastat.CommodityRecord'.
75. Smellið á flipann snið.
76. Í trénu skal velja 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.
77. Smelltu á flipann Vörpun.
78. Smeltu á hnappinn breyta fyrir reitinn ‘heiti lykils fyrir söfnuð gögn’.
79. Í trénu skal velja '$InvName'.
80. Smellt er á Bæta við gagnagjafa.
81. Smellið á „Vista“.
82. Lokið síðunni.
83. Smellið á „Vista“.
84. Lokið síðunni.


