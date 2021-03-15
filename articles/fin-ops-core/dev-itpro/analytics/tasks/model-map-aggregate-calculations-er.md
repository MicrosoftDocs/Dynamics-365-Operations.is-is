---
title: Nota grunnstillingar líkanavörpunar fyrir samanlagða útreikninga á gagnagrunnsstigi
description: Þetta efnisatriði lýsir því hvernig á að hanna nýja stillingu fyrir líkanavörpun rafrænnar skýrslugerðar og nota innbyggða eiginleika Rafrænnar skýrslugerðar fyrir skilvirka samanlagða útreikninga.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6a392697f6b91bc6555d0d72d09ecd7da32e1a3f
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094266"
---
# <a name="use-model-mapping-configurations-for-aggregate-calculations-at-the-database-level"></a>Nota grunnstillingar líkanavörpunar fyrir samanlagða útreikninga á gagnagrunnsstigi

[!include [banner](../../includes/banner.md)]

Þessi aðferð gefur upplýsingar um hvernig á að hanna nýja stillingu fyrir vörpun rafrænnar skýrslugerðar og nota innbyggðar aðgerðir rafrænnar skýrslugerðar fyrir skilvirka samanlagða útreikninga. Í þessu dæmi muntu stofna skilgreiningu fyrir sýnifyrirtækið, Litware, Inc. 

Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar. Skrefin er hægt að klára með því að nota hvaða gagnasafn sem er.

 Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í ferlinu „Rafræn skýrslugerð bætir virkni samanlagðra útreikninga með því að framkvæma hann á gagnagrunnsstigi (hluti 1, Undirbúningur skilgreininga).“

1. Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.
2. Í trénu skal víkka út 'Intrastat model'.
3. Í trénu skal velja „Intrastat-model\Intrastat-sýnivörpun“.
4. Smellið á Hönnuður.
5. Smellið á Hönnuður.
6. Í trénu skal velja 'Dynamics 365 for Operations\Table records'.
7. Smella á bæta Við rót.
    * Bæta nýjum gagnagjafa við sem stendur fyrir færslur sem þú vilt flokka.  
8. Í reitnum Heiti skal færa inn ‚færslur'.
    * Færslur  
9. Í reitnum Tafla skal færa inn „Intrastat“.
    * Intrastat  
10. Smellið á „Í lagi“.
11. Í trénu skal velja „virkni\Flokka eftir“.
    * Þessi gerð gagnagjafa er notuð til að kynna nýjan gagnagjafa á keyrslutíma til að flokka færslur og reikna út áskilda uppsöfnun.  
12. Smella á bæta Við rót.
13. Í reitnum Heiti skal færa inn „TransactionsGroups“.
    * TransactionsGroups  
14. Smella á Breyta hópi eftir
15. Í trénu skal velja „Færslur“.
    * Veljið viðbættan gagnagjafa af gerðinni „færslulisti“ sem stendur fyrir færslur sem þú vilt flokka.  
16. Smellt er á Bæta reit við
17. Veldu hvað skal flokka
18. Í trénu skal víkka út „Færslur“.
19. Í trénu skal velja „Færslur\Stefna“.
20. Smellt er á Bæta reit við
21. Smellt er á Flokkaðir reitir
    * Veljið reitinn sem á að tilgreina flokkunarstig. Byggt á þessu vali munu gögnin koma aftur á keyrslutíma sem margir færsluflokkar þar sem stefnukóðum verður mætt í Intrastat töflunni.  
22. Í trénu skal velja „Færslur\Reikningsupphæð(AmountMST)“.
    * Veljið svæðið til að skilgreina gögn fyrir útreikning á uppsöfnun.  
23. Smellt er á Bæta reit við
24. Smellt er á Uppsöfnunarreitir
25. Í listanum skal merkja valda línu.
26. Veljið „Samtala“ á svæðinu Aðferð.
    * Veljið uppsöfnunargerð.  
27. Í svæðið Heiti skal slá inn „SumOfAmountMST“.
    * Tilgreinið heiti þessarar uppsöfnunar í stilltum gagnagjafa.  
28. Smelltu á Vista.
    * Athugið að reiturinn „Framkvæmd við“ gefur til kynna að þessi flokkun verði framkvæmd á keyrslutíma í SQL gagnagrunninum.  
29. Lokið síðunni.
30. Smellið á „Í lagi“.
31. Í trénu skal víkka út „Samtölur“.
32. Í trénu skal víkka út „TransactionsGroups“.
33. Í trénu skal víkka út „Færsluflokkar\samanlagðir“.
34. Í trénu skal velja „Færsluflokkar\samanlagðir\SumOfAmountMST“.
35. Í trénu skal velja „Samtölur\Samtala reikningsgildis(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0,0, IntrastatTotals.aggregated.'$AmountMSTRounded‘)“.
36. Smelltu á Binda.
    * Byggt á þessari stillingu, mun þessi gagnagjafi reikna summuna af gildum „AmountMST“ reitsins fyrir hvern færsluflokk. Þessi samanlegðarútreikningur verður tiltækur sem TransactionsGroups.aggregated.TotalAmount-atriði.  
37. Í trénu skal víkka út „TransactionsGroups“.
38. Í trénu skal velja „TransactionsGroups“.
39. Smellið á „Breyta“.
40. Smella á Breyta hópi eftir
41. Í trénu skal víkka út „Færslur“.
42. Í trénu skal velja „Færslur\Reikningsupphæð(AmountMST)“.
43. Smellt er á Bæta reit við
44. Smellt er á Uppsöfnunarreitir
45. Í listanum skal merkja valda línu.
46. Veljið „Hámark“ á svæðinu Aðferð.
47. Í svæðið Heiti skal slá inn „MaxOfAmountMST“.
48. Smellið á „Vista“.
    * Eins og er getur framkvæmd GROUPBY gagnagjafa verið þýdd í SQL gagnagrunnsstig með nokkrum takmörkunum. Þýðingu er hægt að gera fyrir annaðhvort gagnagjafa af gerðinni „Færslulisti“ eða gagnagjafa sem settir eru fram sem tjáning með FILTER aðgerðinni. Það er einnig hægt að gera þegar aðeins ein uppsöfnun er stillt fyrir stakan reit flokkunarfærslna.  
    * Athugaðu að jafnvel þó að fleiri en ein uppsöfnun hafi verið stillt fyrir AmountMST-reitinn, gefur reiturinn „Framkvæmd við“ reiturinn enn frekar til kynna að þessi flokkun verði framkvæmd á keyrslutíma í SQL-gagnagrunninum. Þetta er vegna þess að aðeins ein uppsöfnun er bundin við gagnalíkanahlutann og verður notuð á keyrslutíma til að draga gögn úr þessum gagnagjafa.  
49. Lokið síðunni.
50. Smellið á „Í lagi“.
51. Í trénu skal víkka út „TransactionsGroups“.
52. Í trénu skal víkka út „Færsluflokkar\samanlagðir“.
53. Í trénu skal velja „Færsluflokkar\samanlagðir\MaxOfAmountMST“.
54. Í trénu skal velja „Samtölur\Samtölur tölfræðigilda(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0,0, IntrastatTotals.aggregated.'$StatisticalValueRounded‘)“.
55. Smelltu á Binda.
56. Í trénu skal víkka út „TransactionsGroups“.
57. Í trénu skal velja „TransactionsGroups“.
58. Smella á Breyta.
59. Smella á Breyta hópi eftir
    * Athugaðu að reiturinn „Framkvæmd við“ gefur til kynna að þessi flokkun verði framkvæmd á keyrslutíma í minni vegna þess að báðar uppsafnanir sama svæðis eru bundnar við gagnalíkanahlutana.   
60. Merkið eða afmerkið allar línur í listanum.
61. Smellið á Eyða.
62. Smella á Já.
63. Smellið á Eyða.
64. Smella á Já.
65. Smellt er á Bæta reit við
66. Veldu hvað skal flokka
67. Í trénu skal víkka út „Grunnvörufærsla(Intrastat)“.
68. Smelltu á Vista.
    * Athugaðu að reiturinn „Framkvæmd við“ gefur til kynna að þessi flokkun verði framkvæmd á keyrslutíma í minni þrátt fyrir að engar uppsafnanir séu skilgreindar og valdir gagnagjafar af gerðinni „Töflufærslur“ vísa í sömu „Intrastat“-töflu. Þetta er vegna þess að gagnagjafinn inniheldur nokkra útreiknaða reiti sem ekki er hægt að þýða yfir í SQL gagnagrunnsstig.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]