--- 
title: "Stofna skilgreiningu sniðs fyrir rafræna skýrslugerð (ER)"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað skilgreiningarsnið fyrir rafræna skýrslugerð (ER)."
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: c46b222cb12d0432609c47f89afc522e02c41ab6
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-format-configuration-for-electronic-reporting-er"></a>Stofna skilgreiningu sniðs fyrir rafræna skýrslugerð (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað skilgreiningarsnið fyrir rafræna skýrslugerð (ER). Þessa sniðsskilgreiningu mun skilgreina snið rafræn skjöl sem eru notaðar til að vinna greiðslur. Í þessu dæmi stofnar þú skilgreiningu á sniði fyrir dæmi um fyrirtæki, í þessu dæmi Litware, Inc. Til að ljúka þessum skrefum, þarf fyrst að ljúka við skref í ferlinu „Varpa líkani á valda gagnaveitu".


## <a name="create-a-new-format-configuration"></a>Stofna nýja skilgreiningu á sniði
1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
2. Smelltu á Grunnstillingar skýrslugerðar
3. Veljið 'Greiðslur (einfaldað líkan)', í trénu.
4. Smellt er á stofna skilgreiningu til að opna fellilistanum.
5. Í nýja svæðinu, færðu inn „Snið byggir á gagnalíkani PaymentModel“.
6. Í reitinn Heiti skal slá inn 'BACS (UK uppspunnið)'.
    * BACS (UK Upphugsað)  
7. Færið inn 'BACS greiðslusnið lánardrottins (UK uppspunnið)' í svæðinu Lýsingu.
    * Greiðslusnið lánardrottins BACS (UK Upphugsað)  
    * Virkt skilgreiningarveitu er sjálfkrafa færð inn hér. Þessa veitu mun geta unnið með þessa skilgreiningu. Önnur veitur er hægt að nota þetta skilgreining, en geta ekki unnið með hana.  
    * Hægt er að skilgreina ákveðið snið rafrænt skjal. Þetta svæði er skilið eftir autt ef óskað er að velja snið á tíma keyrslu.  
8. Í reitinn Skilgreining Gagnalíkans skal slá inn eða velja gildi.
9. Smelltu á Stofna skilgreiningu.
    * Ný Skilgreining hefur verið stofnuð. Hægt er að nota sem útgáfuna drög til að vista hannað snið fyrir umsjón með rafrænum skjölum.  

## <a name="design-format-of-electronic-document"></a>Hanna snið rafrænts skjals
1. Smellið á Hönnuður.
2. Smelltu á Bæta við rót til að opna felligluggann.
3. Veljið 'Common\File', í trénu.
4. Í reitnum Heiti skal færa inn ‚Xml‘.
    * Xml  
5. Í reitinn Kóðun skal slá inn „UTF-8“.
    * UTF-8  
6. Smellið á „Í lagi“.
7. Smelltu á Bæta við til að opna felligluggann.
8. Í trénu skal velja „XML/Element“.
9. Í reitnum Heiti skal færa inn ‚Skilaboð‘.
    * Skilaboð  
10. Smellið á „Í lagi“.
11. Í trénu skal velja 'Xml\Message'.
12. Smella á bæta Við einingu.
13. Í reitnum Heiti skal færa inn ‚ProcessingDate‘.
    * ProcessingDate  
14. Smellið á „Í lagi“.
15. Smella á bæta Við einingu.
16. Í svæðið Heiti, færðu inn 'MessageId'.
    * MessageId  
17. Smellið á „Í lagi“.
18. Smella á bæta Við einingu.
19. Í svæðið Heiti, færðu inn 'Greiðslur'.
    * Greiðslur  
20. Smellið á „Í lagi“.
21. Í trénu skal velja 'Xml\Message\Payments'.
22. Smella á bæta Við einingu.
23. Í reitnum Heiti skal færa inn ‚Atriði.
    * vara  
24. Smellið á „Í lagi“.
25. Í trénu skal velja 'Xml\Message\Payments\Item'.
26. Smelltu á Bæta við til að opna felligluggann.
27. Í trénu skal velja „XML/Attribute“.
28. Í reitnum Heiti skal færa inn ‚Id‘.
    * Auðkenni  
29. Smellið á „Í lagi“.
30. Smelltu á Bæta við til að opna felligluggann.
31. Í trénu skal velja „XML/Element“.
32. Í reitnum Heiti skal færa inn ‚lánardrottinn‘.
    * Lánardrottinn  
33. Smellið á „Í lagi“.
34. Í trénu skal velja 'Xml\Message\Payments\Item\Vendor'.
35. Smella á bæta Við einingu.
36. Í svæðið Heiti, færðu inn ‚Heiti'.
    * Nafn  
37. Smellið á „Í lagi“.
38. Smella á bæta Við einingu.
39. Í reitnum Heiti skal færa inn ‚Banki'.
    * Banki  
40. Smellið á „Í lagi“.
41. Í trénu skal velja 'Xml\Message\Payments\Item\Vendor\Bank'.
42. Smella á bæta Við einingu.
43. Í svæðið Heiti, færðu inn 'RoutingNumber'.
    * RoutingNumber  
44. Smellið á „Í lagi“.
45. Smella á bæta Við einingu.
46. Í svæðið Heiti, færðu inn ‚AccountNumber'.
    * AccountNumber  
47. Smellið á „Í lagi“.
48. Í trénu skal velja 'Xml\Message\Payments\Item\Vendor'.
49. Smellið á Afrit.
50. Í trénu skal velja 'Xml\Message\Payments\Item'.
51. Smellt er á Líma.
52. Í reitnum Heiti skal færa inn ‚Greiðandi‘.
    * Greiðandi  
53. Í trénu skal velja 'Xml\Message\Payments\Item'.
54. Smella á bæta Við einingu.
55. Í svæðið Heiti, færðu inn 'Gjaldmiðils'.
    * Gjaldmiðill  
56. Smellið á „Í lagi“.
57. Smella á bæta Við einingu.
58. Í reitnum Heiti skal færa inn ‚Lýsing'.
    * lýsing  
59. Smellið á „Í lagi“.
60. Smella á bæta Við einingu.
61. Í svæðið Heiti, færðu inn ‚TransDate'.
    * TransDate  
62. Smellið á „Í lagi“.
63. Smella á bæta Við einingu.
64. Í reitnum Heiti skal færa inn ‚Upphæð'.
    * Upphæð  
65. Smellið á „Í lagi“.

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a>Undirbúa íhluti sniðs fyrir vörpun í einingar gagnalíkans
1. Í trénu skal velja 'Xml\Message\ProcessingDate'.
2. Smelltu á Bæta við til að opna felligluggann.
3. Í trénu skal velja 'Text\DateTime'.
4. Í svæðinu Snið 'áááá-MM-dd' skal fært inn.
    * áááá-MM-dd  
5. Smellið á „Í lagi“.
6. Í trénu skal velja 'Xml\Message\Payments\Item\TransDate'.
7. Smella á Bæta við dagsetning/tími.
8. Í svæðinu Snið 'áááá-MM-dd' skal fært inn.
    * áááá-MM-dd  
9. Í svæði Gerð dagsetning/tími skal velja „Dagsetning“.
10. Smellið á „Í lagi“.
11. Í trénu skal velja 'Xml\Message\MessageId'.
12. Smelltu á Bæta við til að opna felligluggann.
13. Í trénu skal velja ‚Texti/Strengur'.
14. Smellt er á Í lagi.
15. Í trénu skal velja 'Xml\Message\Payments\Item\Vendor\Name'.
16. Smella á bæta Við Streng.
17. Smellt er á Í lagi.
18. Í trénu skal velja 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.
19. Smella á bæta Við Streng.
20. Smellt er á Í lagi.
21. Í trénu skal velja 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.
22. Smella á bæta Við Streng.
23. Smellt er á Í lagi.
24. Í trénu skal velja 'Xml\Message\Payments\Item\Payer\Name'.
25. Smella á bæta Við Streng.
26. Smellt er á Í lagi.
27. Í trénu skal velja 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.
28. Smella á bæta Við Streng.
29. Smellt er á Í lagi.
30. Í trénu skal velja 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.
31. Smella á bæta Við Streng.
32. Smellt er á Í lagi.
33. Í trénu skal velja 'Xml\Message\Payments\Item\Currency'.
34. Smella á bæta Við Streng.
35. Smellt er á Í lagi.
36. Í trénu skal velja 'Xml\Message\Payments\Item\Description'.
37. Smella á bæta Við Streng.
38. Smellt er á Í lagi.
39. Í trénu skal velja 'Xml\Message\Payments\Item\Amount'.
40. Smella á bæta Við Streng.
41. Smellt er á Í lagi.
42. Smellið á „Vista“.
43. Lokið síðunni.


