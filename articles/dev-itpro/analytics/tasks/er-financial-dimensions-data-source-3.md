--- 
title: "Hanna skýrslu til að nota fjárhagsvíddir sem gagnaveitu í rafrænni skýrslugerð (ER)"
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: c67bf235f3514a19893bcefcaae6e3bb11bbb151
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="design-a-report-to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a>Hanna skýrslu til að nota fjárhagsvíddir sem gagnaveitu í rafrænni skýrslugerð (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt líkan rafrænnar skýrslugerðar (ER) svo það noti fjárhagsvíddir sem gagnaveitu fyrir rafrænar skýrslur. Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.

Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í á "Rafræn skýrslugerð notar fjárhagsvíddir sem gagnaveitu (Hluti 2: líkanavörpun) ferli.


## <a name="design-a-report-to-present-financial-dimensions"></a>Hannaðu skýrslu til að birta fjárhagsvíddir
1. Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.
2. Veljið 'dæmi um líkan fyrir fjárhagsvíddir', í trénu.
3. Smellt er á stofna skilgreiningu til að opna fellilistanum.
4. Í nýja svæðinu, færðu inn „Snið byggir á gagnalíkaninu dæmalíkan fjárhagsvídda“.
    * Nota líkan sem var stofnað fyrirfram sem gagnagjafa fyrir nýju skýrsluna.  
5. Í svæðið Heiti, færðu inn 'skýrsla um færslubók fjárhags'.
6. Í reitnum skilgriening gagnalíkans er valið „færsla“.
7. Smelltu á Stofna skilgreiningu.
8. Smellið á Hönnuður.
9. Smelltu á Bæta við rót til að opna felligluggann.
10. Í trénu skal velja „XML/Element“.
11. Í reitnum Heiti skal færa inn ‚rót'.
12. Smellt er á Í lagi.
13. Smelltu á Bæta við til að opna felligluggann.
14. Í trénu skal velja „XML/Attribute“.
15. Í reitnum Heiti skal færa inn ‚Fyrirtæki‘.
16. Smellt er á Í lagi.
17. Smelltu á Bæta við til að opna felligluggann.
18. Í trénu skal velja „XML/Element“.
19. Í reitnum Heiti skal færa inn 'færslubók'.
20. Smellt er á Í lagi.
21. Í trénu, skal velja 'Root: XML Element\Journal: XML Element'.
22. Smelltu á Bæta við til að opna felligluggann.
23. Í trénu skal velja „XML/Attribute“.
24. Í reitnum Heiti skal færa inn 'runa'.
25. Smellt er á Í lagi.
26. Smelltu á Bæta við til að opna felligluggann.
27. Í trénu skal velja „XML/Element“.
28. Í reitnum Heiti skal færa inn ‚færsla'.
29. Smellt er á Í lagi.
30. Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.
31. Smelltu á Bæta við til að opna felligluggann.
32. Í trénu skal velja „XML/Attribute“.
33. Í reitnum Heiti skal færa inn ‚fylgiskjal'.
34. Smellið á „Í lagi“.
35. Smella á Bæta við eigind.
36. Í reitnum Heiti skal færa inn ‚dagsetning'.
37. Smellið á „Í lagi“.
38. Smella á Bæta við eigind.
39. Í svæðið Heiti, færðu inn 'Gjaldmiðils'.
40. Smellið á „Í lagi“.
41. Smella á Bæta við eigind.
42. Í svæðið Heiti, færðu inn 'Dt'.
43. Smellið á „Í lagi“.
44. Smella á Bæta við eigind.
45. Í reitinn Heiti skal slá inn 'Ct'.
46. Smellið á „Í lagi“.
47. Smelltu á Bæta við til að opna felligluggann.
48. Í trénu skal velja „XML/Element“.
49. Í reitnum Heiti skal færa inn 'víddir'.
50. Smellt er á Í lagi.
51. Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.
52. Smelltu á Bæta við til að opna felligluggann.
53. Í trénu skal velja „XML/Attribute“.
54. Í reitnum Heiti skal færa inn 'kóði'.
55. Smellið á „Í lagi“.
56. Smella á Bæta við eigind.
57. Í svæðið Heiti, færðu inn 'Gildi'.
58. Smellið á „Í lagi“.
59. Smella á Bæta við eigind.
60. Í svæðið Heiti, færðu inn 'lýsing'.
61. Smellið á „Í lagi“.

## <a name="map-report-elements-to-data-sources"></a>Varpa skýrslueiningum í gagnagjafa
1. Smelltu á flipann Vörpun.
2. Í trénu, skal víkka út 'model: Data model Financial dimensions sample model'.
3. Í trénu, skal víkka út 'model: Data model Financial dimensions sample model\Journal: Record list'.
4. Í trénu, skal víkka út 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.
5. Í trénu, skal víkka út 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.
6. Í trénu, skal velja ' Rót: XML Element\Journal: xml-Eininguna '.
7. Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.
8. Smelltu á Binda.
9. Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.
10. Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.
11. Smelltu á Binda.
12. Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.
13. Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.
14. Smelltu á Binda.
15. Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.
16. Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.
17. Smelltu á Binda.
18. Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.
19. Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.
20. Smelltu á Binda.
21. Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.
22. Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.
23. Smelltu á Binda.
24. Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.
25. Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.
26. Smelltu á Binda.
27. Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.
28. Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.
29. Smelltu á Binda.
30. Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.
31. Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.
32. Smelltu á Binda.
33. Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.
34. Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.
35. Smelltu á Binda.
36. Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.
37. Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.
38. Smelltu á Binda.
39. Í trénu, skal velja 'Root: XML Element\Journal: XML Element'.
40. Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list'.
41. Smelltu á Binda.
42. Í trénu, skal velja 'Root: XML Element\Company: XML Attribute'.
43. Í trénu, skal velja 'model: Data model Financial dimensions sample model\Company: String'.
44. Smelltu á Binda.
45. Smellið á „Vista“.
46. Lokið síðunni.


