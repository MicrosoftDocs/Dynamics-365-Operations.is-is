---
title: Skilgreina líkanavörpun rafrænnar skýrslugerðar og velja gagnagjafa
description: Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur valið gagnaveitur fyrir gagnalíkan rafrænnar skýrslugerðar.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d57c191761b8e2367ff8806c1cd98d6d83559e3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682118"
---
# <a name="define-er-model-mappings-and-select-data-sources-for-them"></a>Skilgreina líkanavörpun rafrænnar skýrslugerðar og velja gagnagjafa

[!include [banner](../../includes/banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur valið gagnaveitur fyrir Rafræna skýrslugerð (ER) gagnalíkan. Gagnaveita verður bundin vup einstaka íhluti fyrir valið gagnalíkan á þegar það var hannað og fylla viðskiptagögn á það gagnalíkan þegar það var keyrt. Í þessu dæmi er valinn gagnagjafi fyrir fyrirliggjandi gagnalíkan sem hefur verið stofnað fyrir sýnisfyrirtæki, í þessu dæmi Litware, Inc. Til að ljúka þessum skrefum, þarf fyrst að ljúka við skrefin í ferlinu "Stofna nýtt gagnalíkan".


## <a name="open-the-electronic-reporting-configurations-tree"></a>Opna grunnstillingatré Rafræn skýrslugerð
1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
2. Smelltu á Grunnstillingar skýrslugerðar

## <a name="insert-a-new-model-mapping"></a>Setja inn nýja líkanavörpun
1. Veljið 'Greiðslur (einfaldað líkan)', í trénu.
2. Smellið á Hönnuður.
3. Smellt er á Varpa líkani á gagnagjafa.
4. Smellið á „Nýtt“.
    * Þetta stofnar nýja færslu sem mun varpa gagnalíkani á gagnagjafa. Í þessu dæmi, verður að varpa gagnalíkani í gagnagjafa fyrir viðkomandi greiðslugerð: kreditfærslu.     Mögulegt er að hanna fleiri en eina vörpun fyrir tiltekið gagnalíkan. Til dæmis væri hægt að stofna vörpun fyrir mismunandi gerðir greiðslna, eins og fyrir beingreiðsla eða kreditfærsla. Í þessu dæmi muntu stofna vörpun fyrir kreditfærslur.  
5. Í reitinn Heiti skal slá inn 'CT vörpun'.
    * Vörpun CT  
6. Í reitinn Lýsing skal slá inn ‚CT vörpun greiðslulíkans'.
    * CT vörpun greiðslulíkans  
7. Í svæði Skilgreining skal slá inn 'CustomerCreditTransferInitiation'.
    * CustomerCreditTransferInitiation  
8. „Leysa úr“ breytir skilgreiningu.
9. Smellið á „Vista“.

## <a name="define-required-data-sources-for-the-current-model-mapping"></a>Skilgreina nauðsynlega gagnaveitur fyrir gildandi líkanavörpun
1. Smellið á Hönnuður.
2. Í trénu skal velja 'Dynamics 365 for Operations\Table records'.
3. Smella á bæta Við rót.
    * Færið inn gagnagjafa til að hafa aðgang að greiðslufærslum.  
4. Í reitnum Heiti skal færa inn ‚færslur'.
    * Færslur  
5. Í reitnum Merki skal færa inn ‚Færslur‘.
    * Færslur  
6. Færið inn 'Fjárhagsbókarlínur' í svæðinu Hjálp.
    * Fjárhagsfærslubókarlínur  
7. Velja skal Já í reitnum Óska eftir fyrirspurn.
    * Velja skal Já.  
8. Í reitnum Tafla skal færa inn ‚LedgerJournalTrans‘.
    * LedgerJournalTrans  
9. Smellið á „Í lagi“.
    * Veljið töflunni LedgerJournalTrans sem gagnaveita fyrir gildandi gagnalíkan.  
10. Veljið 'Functions\Calculated svæðið', í trénu.
11. Smelltu á Bæta við.
    * Smella á bæta Við til að bæta við nýju reiknuðu svæði.  
12. Í reitnum Heiti skal færa inn '$EndToEndID'.
    * $EndToEndID  
13. Smellt er á Breyta formúla.
14. Veljið 'String\CONCATENATE', í trénu.
15. Smelltu á Bæta við Aðgerð.
16. Í trénu skal víkka út „Færslur“.
17. Veljið 'Transactions\Voucher', í trénu.
18. Smellt er á Bæta við gagnagjafa.
19. Í svæði Formúla slá inn 'CONCATENATE(Transactions.Voucher, "-", '.
    * Sláðu inn [ , "-", ] aftast í formúlu.  
20. Í trénu skal velja „String/TEXT“.
21. Smelltu á Bæta við Aðgerð.
22. Veljið 'Transactions\Record-ID(RecId)', í trénu.
23. Smellt er á Bæta við gagnagjafa.
24. Í svæði Formúla slá inn 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.
    * Sláðu inn [))] aftast í formúlu.  
25. Smellið á „Vista“.
    * Gangið úr skugga um að engar villur hafi fundist fyrir formúluna sem er stofnuð. Sjá flipann VILLUR undir ritilstýringu formúlu.  
26. Lokið síðunni.
27. Smellið á „Í lagi“.
    * Bættu reiknuð svæði við þennan gagnagjafa.  
28. Smelltu á Bæta við.
    * Smella á bæta Við til að bæta við nýju reiknuðu svæði.  
29. Í reitnum Heiti skal færa inn ‚$Amount'.
    * $Amount  
30. Smellt er á Breyta formúla.
31. Í trénu skal víkka út „Færslur“.
32. Veljið 'Transactions\Debit(AmountCurDebit)', í trénu.
33. Smellt er á Bæta við gagnagjafa.
34. Í svæði Formúla slá inn 'Transactions.AmountCurDebit - '.
    * Sláðu inn [ - ] aftast í formúlu.  
35. Í trénu, veljið 'Transactions\Credit(AmountCurCredit)'.
36. Smellt er á Bæta við gagnagjafa.
37. Smellið á „Vista“.
38. Lokið síðunni.
39. Smellið á „Í lagi“.
    * Þetta bætir $Amount reiknaða svæðið við vilda gagnaveitu fyrir núverandi gagnalíkan.  
40. Í trénu skal velja „Færslur\$Upphæð“.
41. Í trénu skal víkka út „Færslur“.
42. Í tré skal víkka eða draga saman „Færslur\$Upphæð“.
43. Í tré skal víkka eða draga saman 'Transactions'.
44. Í trénu skal velja 'Dynamics 365 for Operations\Table records'.
45. Smella á bæta Við rót.
    * Færið inn gagnaveitu til að hafa aðgang að upplýsingar bankareiknings fyrirtækis.  
46. Í reitnum Heiti skal færa inn 'BankAccount'.
    * BankAccount  
47. Færið inn 'Bankareikning' í svæðinu Merki.
    * Bankareikningur  
48. Færið inn 'Bankareikning' í svæðinu Hjálp.
    * Bankareikningur  
49. Velja skal Já í reitnum Óska eftir fyrirspurn.
    * Velja skal Já.  
50. Í reitnum Tafla skal færa inn 'BankAccountTable'.
    * BankAccountTable  
51. Smellið á „Í lagi“.
    * Veljið BankAccountTable töfluna sem gagnaveita fyrir gildandi gagnalíkan.  
52. Smella á bæta Við rót.
    * Færið inn gagnaveitu til að hafa aðgang að upplýsingar um fyrirmæli fyrirtækis.  
53. Í reitnum Heiti skal færa inn ‚Fyrirtæki‘.
    * Fyrirt.    
54. Í reitinn Merki skal slá inn gildi.
    * Fyrirtækið  
55. Í reitinn Hjálp skal færa inn ‚Fyrirtækjaupplýsingar‘.
    * Fyrirtækið  
56. Velja skal Já í reitnum Óska eftir fyrirspurn.
    * Velja skal Já.  
57. Í reitinn Tafla skal færa inn ‚CompanyInfo‘.
    * CompanyInfo  
58. Smellið á „Í lagi“.
    * Veljið CompanyInfo töfluna sem gagnaveita fyrir gildandi gagnalíkan.  
59. Veljið 'Functions\Calculated svæðið', í trénu.
60. Smella á bæta Við rót.
    * Setja inn reiknuð svæði sem nýja gagnaveita.  
61. Í svæðið Heiti, færðu in 'ProcessingDateTime'.
    * ProcessingDateTime  
62. Í svæðið Merki skal færa inn ' Vinnsludagsetning & tími '.
    * Vinnsludagsetning & tími  
63. Smellt er á Breyta formúla.
64. Í tré skal velja 'Date/time\SESSIONNOW'.
65. Smelltu á Bæta við Aðgerð.
66. Smellið á „Vista“.
67. Lokið síðunni.
68. Smellið á „Í lagi“.
    * Bæta ProcessingDateTime reiknaða svæðisins við sem gagnaveita fyrir gildandi gagnalíkan.  
69. Smellið á „Vista“.
70. Lokið síðunni.
71. Lokið síðunni.
72. Lokið síðunni.

