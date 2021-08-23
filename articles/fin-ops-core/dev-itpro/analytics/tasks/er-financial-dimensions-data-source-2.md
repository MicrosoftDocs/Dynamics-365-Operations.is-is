---
title: Rafræn skýrslugerð Nota Fjárhagsvíddir sem gagnaveita (Hluti 2 - líkanavörpun)
description: Þetta efni útskýrir hvernig á að skilgreina líkan rafrænnar skýrslugerðar til að nota fjárhagsvíddir sem gagnagjafa fyrir skýrslur rafrænnar skýrslugerðar. (Hluti 2)
author: NickSelin
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 921077cb3bc2d01c418f653194e948a2f29cc90dbd562d022ca69aa083a6ef54
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713895"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a>Rafræn skýrslugerð Nota Fjárhagsvíddir sem gagnaveita (Hluti 2 - líkanavörpun)

[!include [banner](../../includes/banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt líkan rafrænnar skýrslugerðar (ER) svo það noti fjárhagsvíddir sem gagnaveitu fyrir rafrænar skýrslur. Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.

Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í ferlinu „Rafræn skýrslugerð notar fjárhagsvíddir sem gagnaveitu (Hluti 1: Hönnun gagnalíkans”.


## <a name="add-required-data-sources-to-model-mapping"></a>Bæta við nauðsynlegar gagnaveitur við líkanavörpun
1. Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.
2. Veljið 'dæmi um líkan fyrir fjárhagsvíddir', í trénu.
3. Smellið á Hönnuður.
4. Smellt er á Varpa líkani á gagnagjafa.
5. Smellið á „Nýtt“.
6. Í reitnum Skilgreining er valið „færsla“.
7. Í reitnum Heiti skal færa inn 'gagnakortalagning vídda'.
8. Í reitnum lýsing skal færa inn 'gagnakortalagning vídda'.
9. Smellið á „Vista“.
10. Smellið á Hönnuður.
11. Í trénu skal velja „Dynamics 365 for Operations\Table“.
12. Smella á bæta Við rót.
13. Í reitnum Heiti skal færa inn ‚Fyrirtæki‘.
14. Í reitinn Tafla skal færa inn ‚CompanyInfo‘.
15. Smellt er á Í lagi.
16. Í trénu skal velja 'Functions\Financial dimensions details'.
17. Smella á bæta Við rót.
    * Þennan gagnagjafa tilgreinir hvernig svið fjárhagsvídda er skilgreint fyrir allar skýrslur sem nota þetta líkan sem gagnagjafa.  
18. Í reitinn Heiti skal slá inn gildi.
19. Velja skal Já í reitnum Óska eftir víddum.
    * Velja skal Já til að leyfa notanda að velja víddir á keyrslutíma á skjámyndinni svargluggai Notanda. Ef stillt á Nei verða allar fjárhagsvíddir núverandi tilviks notaðar sjálfgefið.  
20. Í valreit fjárhagsvídda skal velja lögaðila
    * Veljið Allt til að leyfa notanda að velja víddir sem óskað er eftir fyrir núverandi tilvik í uppflettisvæðinu.  Veljið Lögaðila til að leyfa notanda að velja víddir sem óskað er eftir fyrir fyrirtæki í uppflettisvæðinu.  Velja skal Vídd til að leyfa notanda að velja víddir sem nota stakar víddarsamstæður.  
21. Veljið Já í svæðinu Biðja um aðallykil.
    * Stilltu „Biðja um aðallykil” á Já til að leyfa notendum að velja aðallykilinn sem hluta af listanum yfir víddir.   Ef stillt er á Nei, verður aðallykilinn ekki teknar með á lista yfir víddir og valkosturinn „Er skylda fyrir aðallykil” er virkjaður. Ef „Er skylda fyrir aðallykil” er stillt á já skal hafa aðallykillinn með í lista yfir víddir óháð vali notanda.  
22. Smellt er á Í lagi.
![Hönnuðarsíða ER-líkanavörpunar.](../media/er-financial-dimensions-guides-model-mapping1.png)
23. Í trénu skal velja 'Dynamics 365 for Operations\Table records'.
24. Smella á bæta Við rót.
25. Í svæðið Heiti, færðu inn 'LedgerJournal'.
26. Velja skal Já í reitnum Óska eftir fyrirspurn.
27. Í reitnum Tafla skal færa inn ‚LedgerJournalTable‘.
28. Smellt er á Í lagi.
![Hönnuðarsíða ER-líkanavörpunar.](../media/er-financial-dimensions-guides-model-mapping2.png)

## <a name="map-data-model-elements-to-added-data-sources"></a>Varpa einingum gagnalíkans við gagnaveitur sem bætt var við.
1. Stækkið „færslubók“ í trénu.
2. Í trénu skal víkka út 'Journal\Transaction'.
3. Í trénu skal víkka út 'Journal\Transaction\Dimensions data'.
4. Í trénu skal víkka út 'Dimensions setting'.
5. Í trénu skal víkka út 'LedgerJournal'.
6. Í trénu, útvíkka „LedgerJournal\<Relations“.
7. Í trénu, útvíkka expand „LedgerJournal\<Relations\LedgerJournalTrans“.
8. Í trénu, útvíkka „LedgerJournal\<Relations\LedgerJournalTrans\Voucher“.
9. Í trénu skal velja 'Journal\Transaction\Voucher'.
10. Smelltu á Binda.
11. Í trénu, skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)“.
    * Athugið að fyrir allar tilvísanir í fjárhagsvíddir sem eru stilltar á, til dæmis LedgerDimension, er samsvarandi vara gagnaveitu tiltæk (LedgerDimension.Dimension). Þessi gagnagjafaliður býður upp á fjárhagsvíddir þessara vídda sem eru stilltar sem listi færslunnar.  
12. Í trénu, skal víkka út „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)“.
13. Í trénu skal víkka út „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions“.
14. Í trénu skal víkka út „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value“.
15. Í trénu skal víkka út „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition“.
16. Í trénu, skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name“.
17. Í trénu, skal velja 'Journal\Transaction\Dimensions data\Name'.
18. Smelltu á Binda.
19. Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description“.
20. Í trénu, skal velja 'Journal\Transaction\Dimensions data\Description'.
21. Smelltu á Binda.
22. Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code“.
23. Í trénu, skal velja 'Journal\Transaction\Dimensions data\Code'.
24. Smelltu á Binda.
25. Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions“.
26. Í trénu, skal velja 'Journal\Transaction\Dimensions data'.
27. Smelltu á Binda.
![Hönnuðarsíða ER-líkanavörpunar.](../media/er-financial-dimensions-guides-model-mapping3.png)
28. Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)“.
29. Í trénu, skal velja 'Journal\Transaction\Debit'.
30. Smelltu á Binda.
31. Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)“.
32. Í trénu, skal velja 'Journal\Transaction\Date'.
33. Smelltu á Binda.
34. Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)“.
35. Í trénu, skal velja 'Journal\Transaction\Currency'.
36. Smelltu á Binda.
37. Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)“.
38. Í trénu, skal velja 'Journal\Transaction\Credit'.
39. Smelltu á Binda.
40. Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans“.
41. Í trénu, skal velja 'Journal\Transaction'.
42. Smelltu á Binda.
43. Í trénu, skal velja 'LedgerJournal\Journal batch number(JournalNum)'.
44. Í trénu, skal velja 'Journal\Batch'.
45. Smelltu á Binda.
46. Í trénu, skal velja 'LedgerJournal'.
47. Í trénu, skal velja 'Journal'.
48. Smelltu á Binda.
49. Í trénu, skal víkka út 'Dimensions'.
50. Í trénu, skal víkka út 'Dimensions\Main account and dimensions'.
51. Í trénu, skal víkka út 'Dimensions\Main account and dimensions\Definition'.
52. Í trénu, skal velja 'Dimensions\Main account and dimensions\Definition\Name'.
53. Í trénu, skal velja 'Dimensions setting\Code'.
54. Smelltu á Binda.
55. Í trénu, skal velja 'Dimensions\Main account and dimensions\Definition\Report column name'.
56. Í trénu, skal velja 'Dimensions setting\Name'.
57. Smelltu á Binda.
58. Í trénu, skal velja 'Dimensions\Main account and dimensions'.
59. Í trénu, skal velja 'Dimensions setting'.
60. Smelltu á Binda.
61. Í trénu, skal velja 'Company'.
62. Smellið á „Breyta“.
63. Í svæðinu expressionAsStringText skal færa inn 'Company.'find()'.'name()''.
    * Company.'find()'.'name()'  
64. Smelltu á Vista.
![Hönnuðarsíða ER-líkanavörpunar.](../media/er-financial-dimensions-guides-model-mapping4.png)
65. Lokið síðunni.
66. Smelltu á Vista.
67. Lokið síðunni.

## <a name="complete-this-draft-models-version"></a>Ljúktu við þessa útgáfu af drögum að líkani.
1. Lokið síðunni.
2. Lokið síðunni.
3. Smellið á „Breyta stöðu“.
4. Smelltu á Ljúka.
5. Smellt er á Í lagi.
![Hönnuðarsíða ER-líkanavörpunar.](../media/er-financial-dimensions-guides-model-mapping5.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]