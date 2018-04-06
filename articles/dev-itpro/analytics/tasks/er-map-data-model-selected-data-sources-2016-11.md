--- 
title: "Varpa gagnalíkani á valdar gagnaveitur fyrir rafræna skýrslugerð (ER)"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar getur varpað gagnalíkani rafrænnar skýrslugerðar (ER) á valdar gagnaveitur Dynamics 365 for Finance and Operations, Enterprise edition (nóvember 2016)."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 13b7fe7f7bfe24bd275428e931993aa46ecb9945
ms.contentlocale: is-is
ms.lasthandoff: 03/26/2018

---
# <a name="map-a-data-model-to-selected-data-sources-for-electronic-reporting-er"></a>Varpa gagnalíkani á valdar gagnaveitur fyrir rafræna skýrslugerð (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar getur varpað gagnalíkani rafrænnar skýrslugerðar (ER) á valdar gagnveitur Dynamics 365 for Finance and Operations. Þessi líkanavörpun verður síðar notuð sem gagnaveita í skilgreiningu sniðs sem verður notað til að stjórna skjölum rafrænna greiðsla. Í þessu dæmi er varpað gagnalíkani fyrir dæmi um fyrirtæki, Litware, Inc. til gagnagjafa. Til að ljúka þessum skrefum, verður fyrst að ljúka skrefum í ferlinu "Velja gagnaveita fyrir líkanavörpun".


## <a name="open-er-configurations-tree"></a>Opna grunnstillingatré rafrænnar skýrslugerðar
1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
2. Smellt er á Skilgreiningum.

## <a name="select-created-model-mapping"></a>Veljið stofnuð líkanavörpun
1. Veljið 'Greiðslur (einfaldað líkan)', í trénu.
    * Gangið úr skugga um að skilgreiningarlíkanið "Greiðslur (einfaldað líkan)" hefur verið stofnuð fyrirfram. Að öðrum kosti skal stoppa núna og koma aftur eftir að lokið við verkefnaleiðbeiningar „Mynda nýja grunnstillingu með gagnalíkan af völdu léni“.  
2. Smellt er á hönnuður Líkana.
3. Smellt er á Varpa líkani á gagnagjafa.
4. Veljið færsluna 'CT vörpun'.
    * Vörpun CT  

## <a name="bind-created-data-sources-to-data-model-elements"></a>Binda stofnaða gagnaveitur við þætti gagnalíkans
1. Smellið á Hönnuður.
2. Í trénu, skal velja 'Processing date & time(ProcessingDateTime)'.
3. Veljið ‚Processing date(ProcessingDateTime)', í trénu.
4. Smelltu á Binda.
5. Veljið ‚Payment message identification(MessageIdentification)', í trénu.
6. Í trénu skal víkka út „Færslur“.
7. Veljið ''Transactions\Journal batch number(JournalNum)'., í trénu.
8. Smelltu á Binda.
9. Í trénu skal velja „Greiðslur“.
10. Í trénu skal velja „Færslur“.
11. Smelltu á Binda.
12. Í trénu, útvíkka ' Greiðslur = Færslur.
13. Í trénu, útvíkka ' Payments = Transactions\Creditor'.
14. Í trénu, útvíkka ' Payments = Transactions\Creditor\Account'.
15. Í trénu, skal velja ' Payments = Transactions\Creditor\Account\Currency code(Currency)'.
16. Útvíkka 'Transactions\vendBankAccountInTransactionCompany()', í trénu.
17. Veljið 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)', í trénu.
18. Smelltu á Binda.
19. Í trénu, skal velja ' Payments = Transactions\Creditor\Account\IBAN code(IBAN)'.
20. Veljið 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)', í trénu.
21. Smelltu á Binda.
22. Í trénu, skal velja ' Payments = Transactions\Creditor\Account\Number'.
23. Veljið 'Transactions\vendBankAccountInTransactionCompany () \Bank lykil number(AccountNum)', í trénu.
24. Smelltu á Binda.
25. Í trénu, útvíkka ' Payments = Transactions\Creditor\Agent'.
26. Í trénu, skal velja ' Payments = Transactions\Creditor\Agent\Name'.
27. Veljið '\Name Transactions\vendBankAccountInTransactionCompany ()', í trénu.
28. Smelltu á Binda.
29. Í trénu, skal velja ' Payments = Transactions\Creditor\Agent\Routing number(RoutingNumber)'.
30. Veljið 'Transactions\vendBankAccountInTransactionCompany () \Routing number(RegistrationNum)', í trénu.
31. Smelltu á Binda.
32. Í trénu, skal velja ' Payments = Transactions\Creditor\Agent\SWIFT code(SWIFT)'.
33. Veljið 'Transactions\vendBankAccountInTransactionCompany () \SWIFT code(SWIFTNo)', í trénu.
34. Smelltu á Binda.
35. Í trénu, skal velja ' Payments = Transactions\Creditor\Name'.
36. Útvíkka 'Transactions\findVendTable()', í trénu.
37. Veljið ‚Transactions\findVendTable()\name()', í trénu.
38. Smelltu á Binda.
39. Í trénu, skal velja ' Payments = Transactions\Currency code(Currency)'.
40. Í trénu skal víkka út „Færslur\>Tengsl“.
41. Í trénu skal víkka út „Færslur\>Tengsl\Gjaldmiðill tafla(Gjaldmiðill)“.
42. Í trénu skal velja „Færslur\>Tengsl\Gjaldmiðill tafla(Gjaldmiðill)\Gjaldmiðill kóði(CurrencyCodeISO)“.
43. Smelltu á Binda.
44. Í trénu, útvíkka ' Payments= Transactions\Debtor'.
45. Í trénu, útvíkka 'Payments= Transactions\Debtor\Account'.
46. Í trénu, skal velja ' Payments= Transactions\Debtor\Account\Currency code(Currency)'.
47. Veljið 'Bank Account(BankAccount)', í trénu.
48. Útvíkka 'Bank Account(BankAccount)', í trénu.
49. Veljið 'Bank Account(BankAccount)\Currency(CurrencyCode)', í trénu.
50. Smelltu á Binda.
51. Í trénu, skal velja ' Bank Account(BankAccount) \IBAN'.
52. Í trénu, skal velja ' Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.
53. Smelltu á Binda.
54. Í trénu, skal velja ' Payments= Transactions\Debtor\Account\Number'.
55. Veljið 'Bank Account(BankAccount)\Bank account number(AccountNum)‘, í trénu.
56. Smelltu á Binda.
57. Í trénu, útvíkka ' Payments= Transactions\Debtor\Agent'.
58. Í trénu, skal velja ' Payments= Transactions\Debtor\Agent\Name'.
59. Í trénu skal velja 'Bank Account(BankAccount)\Name'.
60. Smelltu á Binda.
61. Í trénu, skal velja ' Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.
62. Í trénu skal velja 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.
63. Smelltu á Binda.
64. Í trénu, skal velja ' Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.
65. Í trénu, skal velja 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.
66. Smelltu á Binda.
67. Í trénu, skal velja ' Payments= Transactions\Debtor\Name'.
68. Í trénu skal velja 'Company information(Company)'.
69. Útvíkka, í trénu 'Company information(Company)'.
70. Veljið 'Company information(Company)\Name‘, í trénu.
71. Smelltu á Binda.
72. Í trénu, skal velja ' Payments= Transactions\Description'.
73. Veljið 'Transactions\Description(Txt)', í trénu.
74. Smelltu á Binda.
75. Í trénu, skal velja ''Payments= Transactions\End to end identification code(End2EndID)'.
76. Í trénu skal velja „Færslur\$EndToEndID“.
77. Smelltu á Binda.
78. Í trénu, skal velja ''Payments= Transactions\Instructed amount(InstructedAmount)'.
79. Í trénu skal velja „Færslur\$Upphæð“.
80. Smelltu á Binda.
81. Í trénu skal velja 'Payments= Transactions\Transaction date(TransactionDate)'.
82. Veljið 'Transactions\Date(TransDate)', í trénu.
83. Smelltu á Binda.

## <a name="validate-created-mapping"></a>Villuleita stofnaða vörpun
1. Smella á Villuleita.
    * Sannprófa nýja vörpun til að tryggja að allar bindingar séu í lagi.  
2. Með því að smella á örina má stækka eða fella saman hlutann Villulisti.
3. Smellið á „Vista“.
4. Lokið síðunni.
5. Lokið síðunni.
6. Lokið síðunni.

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a>Breyta stöðu gildandi útgáfu skilgreiningar líkans
1. Smellið á „Breyta stöðu“.
    * Breyta stöðu hannaðrar grunnstillingar líkans - úr Drög í Lokið til að gera tiltækur fyrir hönnun greiðslusniðs.  
2. Smelltu á Ljúka.
    * Velja Lokið.  
3. Sláið inn gildi í reitnum „Lýsing“.
    * Til dæmis „Útgáfa 1“.  
4. Smellið á „Í lagi“.
5. Velja lokna útgáfu af núgildandi skilgreiningu.
    * Athugið að stofnuð skilgreining er vistuð sem lokin útgáfa 1.  


