---
title: Rafræn skýrslugerð notar svið sem má stækka lárétt til að bæta við dálkum gagnvirkt við í Excel skýrslum (Hluti 1 - Hanna snið)
description: Í þessu efni er útskýrt hvernig á að skilgreina snið rafrænnar skýrslugerðar til að mynda skýrslur sem OPENXML-vinnublaðaskrár (Excel). (Hluti 1)
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af3d7bdf6bf0de371fa0896bf5f668c98498640d
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944606"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-1---design-format"></a>Rafræn skýrslugerð notar svið sem má stækka lárétt til að bæta við dálkum gagnvirkt við í Excel skýrslum (Hluti 1 - Hanna snið)

[!include [banner](../../includes/banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) til að mynda skýrslur sem OPENXML-vinnublöð (Excel) skrár þar sem hægt er að stofna nauðsynlega dálka gagnvirkt sem svið sem má stækka lárétt. Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.

Til að ljúka þessum skrefum, verður að ljúka þessum þremur verkefnaleiðbeiningum: 

„ER Stofna skilgreiningaveitu og merkja hana sem virka”

„Rafræn skýrslugerð Nota Fjárhagsvíddir sem gagnaveita (Hluti 1 - hanna gagnalíkan)”

„Rafræn skýrslugerð Nota Fjárhagsvíddir sem gagnaveita (Hluti 2 - líkanavörpun)”

Einnig þarf að hlaða niður og vista staðbundið afrit af sniðinu með sýniskýrslu sem hægt er að finna hér: [Dæmi um fjárhagsvíddir vefþjónustuskýrslu](https://download.microsoft.com/download/3/1/3/313e2090-bc0a-421f-bf96-c58da9bc0dea/SampleFinDimWsReport.xlsx).

Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.


## <a name="create-a-new-report-configuration"></a>Stofna nýja skilgreiningu skýrslu.
1. Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.
2. Veljið 'dæmi um líkan fyrir fjárhagsvíddir', í trénu.
3. Smellt er á stofna skilgreiningu til að opna fellilistanum.
4. Í nýja svæðinu, færðu inn „Snið byggir á gagnalíkaninu dæmalíkan fjárhagsvídda“.
    * Nota líkan sem var stofnað fyrirfram sem gagnagjafa fyrir nýju skýrsluna.  
5. Í reitnum heiti, skal færa inn "Dæmi um skýrslu með sviðum sem er hægt að stækka lárétt".
    * Dæmi um skýrslu með sviðum sem er hægt að stækka lárétt.  
6. Í reitnum lýsing, skal færa inn "Gera Excel úttak með því að bæta við dálkum gagnvirkt."
    * Gera Excel úttak með því að bæta við dálkum gagnvirkt.  
7. Í reitnum skilgriening gagnalíkans er valið „færsla“.
8. Smelltu á Stofna skilgreiningu.

## <a name="design-the-report-format"></a>Hannaðu snið skýrslu
1. Smellið á Hönnuður.
2. Kveiku á víxlhnappnum „Birta upplýsingar”.
3. Í aðgerðasvæðinu er smellt á innflutningur.
4. Smella á Flytja inn úr Excel
5. Smellt er á viðhengi
    * Flytja inn sniðmát skýrslu. Notaðu Excel-skráin sem þú sóttir til þess.  
6. Smellið á Nýtt.
7. Smella á Skrá
8. Lokið síðunni.
9. Sláið inn eða veldu gildi í reitnum sniðmát.
    * Veljið niðurhöluð sniðmát.  
10. Smellið á „Í lagi“.
    * Bæta við nýju sviði til að stofna Excel úttak á gagnvirkan hátt með eins mörgum dálkum og þú valdir (í skjámyndinni svargluggi notanda) fyrir fjárhagsvíddir. Hvert hólf fyrir hvern dálk stendur fyrir heiti stakrar fjárhagsvíddar.  
11. Smelltu á Bæta við til að opna felligluggann.
12. Í trénu skal velja 'Excel\Range'.
13. Færðu inn 'DimNames' í reitnum Excel-svið.
    * DimNames  
14. Í reitnum eftirlíkingarátt, skal velja "lárétt".
15. Smellt er á Í lagi.
16. Í trénu, skal velja „Excel = „SampleFinDimWsReport“\Svið<DimNames>Lárétt“.
17. Smelltu á Flytja upp.
18. Í trénu, skal velja „Excel = „SampleFinDimWsReport“\Hólf<DimNames>“.
19. Smellt er á Klippa.
20. Í trénu, skal velja „Excel = „SampleFinDimWsReport“\Svið<DimNames>Lárétt“.
21. Smellt er á Líma.
22. Í trénu, skal víkka út „Excel = „SampleFinDimWsReport“\Svið<DimNames>: Lárétt“.
23. Í trénu, skal víkka út „Excel = „SampleFinDimWsReport“\Svið<JournalLine>: Lóðrétt“.
24. Í trénu, skal víkka út „Excel = „SampleFinDimWsReport“\Svið<JournalLine>:Lóðrétt\Svið<TransactionLine>: Lóðrétt“.
25. Í trénu, skal velja „Excel = „SampleFinDimWsReport“\Svið<JournalLine>: Lóðrétt\Svið<TransactionLine>: Lóðrétt“.
    * Bæta við nýju sviði til að stofna Excel úttak á gagnvirkan hátt með eins mörgum dálkum og þú valdir (í skjámyndinni svargluggi notanda) fyrir fjárhagsvíddir. Hvert hólf fyrir hvern dálk stendur fyrir gildi hverrar skýrslufærslu stakrar fjárhagsvíddar.  
26. Smellt er á bæta við svið.
27. Færðu inn 'DimValues' í reitnum Excel-svið.
    * DimValues  
28. Í reitnum eftirlíkingarátt, skal velja "lárétt".
29. Smellt er á Í lagi.
30. Í trénu, skal velja „Excel = „SampleFinDimWsReport“\Svið<JournalLine>: Lóðrétt\Svið<TransactionLine>: Lóðrétt\Hólf<DimValues>“.
31. Smellt er á Klippa.
32. Í trénu, skal velja „Excel = „SampleFinDimWsReport“\Svið<JournalLine>: Lóðrétt\Svið<TransactionLine>: Lóðrétt\Svið<DimValues>: Lárétt“.
33. Smellt er á Líma.
34. Í trénu, skal víkka út „Excel = „SampleFinDimWsReport“\Svið<JournalLine>: Lóðrétt\Svið<TransactionLine>: Lóðrétt\Svið<DimValues>: Lárétt“.

## <a name="map-format-elements-to-data-sources"></a>Varpa sniðsíhlutum í gagnagjafa
1. Smelltu á flipann Vörpun.
2. Í trénu, skal víkka út 'model: Data model Financial dimensions sample model'.
3. Í trénu, skal víkka út 'model: Data model Financial dimensions sample model\Journal: Record list'.
4. Í trénu, skal víkka út 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.
5. Í trénu, skal víkka út 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.
6. Í trénu, skal velja „Excel = „SampleFinDimWsReport“\Svið<JournalLine>: Lóðrétt\Svið<TransactionLine>: Lóðrétt\Svið<DimValues>: Lárétt\Hólf<DimValues>“.
7. Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.
8. Smelltu á Binda.
9. Í trénu, skal velja „Excel = „SampleFinDimWsReport“\Svið<JournalLine>: Lóðrétt\Svið<TransactionLine>: Lóðrétt\Svið<DimValues>: Lárétt“.
10. Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.
11. Smelltu á Binda.
12. Í trénu, skal velja „Excel = „SampleFinDimWsReport“\Svið<JournalLine>: Lóðrétt\Svið<TransactionLine>: Lóðrétt\Hólf<Credit>“.
13. Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.
14. Smelltu á Binda.
15. Í trénu, skal velja „Excel = „SampleFinDimWsReport“\Svið<JournalLine>: Lóðrétt\Svið<TransactionLine>: Lóðrétt\Hólf<Debit>“.
16. Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.
17. Smelltu á Binda.
18. Í trénu, skal velja „Excel = „SampleFinDimWsReport“\Svið<JournalLine>: Lóðrétt\Svið<TransactionLine>: Lóðrétt\Hólf<Currency>“.
19. Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.
20. Smelltu á Binda.
21. Í trénu, skal velja „Excel = „SampleFinDimWsReport“\Svið<JournalLine>: Lóðrétt\Svið<TransactionLine>: Lóðrétt\Hólf<TransDate>“.
22. Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.
23. Smelltu á Binda.
24. Í trénu, skal velja „Excel = „SampleFinDimWsReport“\Svið<JournalLine>: Lóðrétt\Svið<TransactionLine>: Lóðrétt\Hólf<TransVoucher>“.
25. Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.
26. Smelltu á Binda.
27. Í trénu, skal velja „Excel = „SampleFinDimWsReport“\Svið<JournalLine>: Lóðrétt\Svið<TransactionLine>: Lóðrétt\Hólf<TransBatch>“.
28. Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.
29. Smelltu á Binda.
30. Í trénu, skal velja „Excel = „SampleFinDimWsReport“\Svið<JournalLine>: Lóðrétt\Svið<TransactionLine>: Lóðrétt“.
31. Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.
32. Smelltu á Binda.
33. Í trénu, skal velja „Excel = „SampleFinDimWsReport“\Svið<JournalLine>: Lóðrétt\Hólf<Batch>“.
34. Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.
35. Smelltu á Binda.
36. Í trénu, skal velja „Excel = „SampleFinDimWsReport“\Svið<JournalLine>: Lóðrétt“.
37. Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list'.
38. Smelltu á Binda.
39. Í trénu, skal víkka út 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.
40. Í trénu, skal velja 'model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String'.
41. Í trénu, skal velja „Excel = „SampleFinDimWsReport“\Svið<DimNames>Lárétt\Hólf<DimNames>“.
42. Smelltu á Binda.
43. Í trénu, skal velja 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.
44. Í trénu, skal velja „Excel = „SampleFinDimWsReport“\Svið<DimNames>Lárétt“.
45. Smelltu á Binda.
46. Í trénu, skal velja „Excel = „SampleFinDimWsReport“\Hólf<CompanyName>“.
47. Í trénu, skal velja 'model: Data model Financial dimensions sample model\Company: String'.
48. Smelltu á Binda.
49. Smellið á „Vista“.
50. Lokið síðunni.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
