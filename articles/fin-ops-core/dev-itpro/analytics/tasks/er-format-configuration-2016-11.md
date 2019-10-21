---
title: Rafræn skýrslugerð stofna grunnstilling sniðs (nóvember 2016)
description: Þetta efni útskýrir hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað skilgreiningarsnið fyrir rafræna skýrslugerð (ER).
author: NickSelin
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1fd41b1724eb2e0405c0e7a7e0ff0aea4a945e0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184946"
---
# <a name="er-create-a-format-configuration-november-2016"></a>Rafræn skýrslugerð stofna grunnstilling sniðs (nóvember 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þetta efni útskýrir hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað skilgreiningarsnið fyrir rafræna skýrslugerð (ER). Þessa sniðsskilgreiningu mun skilgreina snið rafræn skjöl sem eru notaðar til að vinna greiðslur. Í þessu dæmi stofnar þú skilgreiningu á sniði fyrir dæmi um fyrirtæki, í þessu dæmi Litware, Inc. Til að ljúka þessum skrefum, þarf fyrst að ljúka við skref í ferlinu „Varpa líkani á valda gagnaveitu".


## <a name="create-a-new-format-configuration"></a>Stofna nýja skilgreiningu á sniði
1. Fara í **Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð**.
2. Smellið á **Skilgreiningar skýrslugerðar**.
3. Veljið **Greiðslur (einfaldað líkan)** í trénu.
4. Smellið á **Stofna skilgreiningu** til að opna felligluggann.

 > [!NOTE]
 > Ef þú sérð ekki **Stofna skilgreiningu** verður þú að virkja hönnunarsnið á síðunni **Færibreytur rafrænnar skýrslugerðar**. 
 
5. Í svæðinu **Nýtt** skal færa inn **Snið byggir á gagnalíkani PaymentModel**,
6. Í svæðinu **Heiti** skal slá inn **BACS (UK skáldað)**.
7. Í svæðinu **Lýsing** skal færa inn **BACS greiðslusnið lánardrottins (UK skáldað)**.
    * Virkt skilgreiningarveitu er sjálfkrafa færð inn hér. Þessa veitu mun geta unnið með þessa skilgreiningu. Önnur veitur er hægt að nota þetta skilgreining, en geta ekki unnið með hana.  
    * Hægt er að skilgreina ákveðið snið rafrænt skjal. Þetta svæði er skilið eftir autt ef óskað er að velja snið á tíma keyrslu.  
8. Í svæðinu **Skilgreining gagnalíkans** skal færa inn eða velja gildi.
9. Smellið á **Stofna skilgreiningu**. Ný Skilgreining hefur verið stofnuð. Hægt er að nota sem útgáfuna drög til að vista hannað snið fyrir umsjón með rafrænum skjölum.  

## <a name="design-the-format-of-an-electronic-document"></a>Hannið snið fyrir rafrænt skjal
1. Smellið á **Hönnuður**.
2. Smellið á **Bæta við rót** til að opna felligluggann.
3. Veljið **Common\File** í trénu.
4. Í svæðið **Heiti** skal færa inn **Xml**.
5. Í svæðið **Kóðun** skal færa inn **UTF-8**.
6. Smellið á **Í lagi**.
7. Smellið á **Bæta við**.
8. Í trénu skal velja **XML/Element**.
9. Í svæðið **Heiti** skal færa inn **Skilaboð**.
10. Smellið á **Í lagi**.
11. Í trénu skal velja **Xml\Message**.
12. Smellið á **Bæta við einingu**.
13. Í svæðinu **Heiti** skal færa inn **ProcessingDate**.
14. Smellið á **Í lagi**.
15. Smellið á **Bæta við einingu**.
16. Í svæðið Heiti skal færa inn **MessageId**.
17. Smellið á **Í lagi**.
18. Smellið á **Bæta við einingu**.
19. Í svæðið **Heiti** skal færa inn **Greiðslur**.
20. Smellið á **Í lagi**.
21. Í trénu skal velja **Xml\Message\Payments**.
22. Smellið á **Bæta við einingu**.
23. Í svæðið **Heiti** skal færa inn **Vara**.
24. Smellið á **Í lagi**.
25. Í trénu skal velja **Xml\Message\Payments\Item**.
26. Smellið á **Bæta við**.
27. Í trénu skal velja **XML\Attribute**.
28. Í svæðið Heiti skal færa inn **Auðkenni**.
29. Smellið á **Í lagi**.
30. Smellið á **Bæta við**.
31. Í trénu skal velja **XML/Element**.
32. Í svæðið Heiti skal færa inn **Lánardrottinn**.
33. Smellið á **Í lagi**.
34. Í trénu skal velja **Xml\Message\Payments\Item\Vendor**.
35. Smellið á **Bæta við einingu**.
36. Í svæðið Heiti skal færa inn **Heiti**.
37. Smellið á **Í lagi**.
38. Smellið á **Bæta við einingu**.
39. Í svæðið **Heiti** skal færa inn **Banki**.
40. Smellið á **Í lagi**.
41. Í trénu skal velja **Xml\Message\Payments\Item\Vendor\Bank**.
42. Smellið á **Bæta við einingu**.
43. Í svæðið **Heiti** skal færa inn **RoutingNumber**.
44. Smellið á **Í lagi**.
45. Smellið á **Bæta við einingu**.
46. Í svæðið **Heiti** skal færa inn **AccountNumber**.
47. Smellið á **Í lagi**.
48. Í trénu skal velja **Xml\Message\Payments\Item\Vendor**.
49. Smellið á **Afrit**.
50. Í trénu skal velja **Xml\Message\Payments\Item**.
51. Smellið á **Líma**.
52. Í svæðið **Heiti** skal færa inn **Greiðandi**.
53. Í trénu skal velja **Xml\Message\Payments\Item**.
54. Smellið á **Bæta við einingu**.
55. Í svæðið **Heiti** skal færa inn **Gjaldmiðill**.
56. Smellið á **Í lagi**.
57. Smellið á **Bæta við einingu**.
58. Í svæðið **Heiti** skal færa inn **Lýsing**.
59. Smellið á **Í lagi**.
60. Smellið á **Bæta við einingu**.
61. Í svæðið Heiti skal færa inn **TransDate**.
62. Smellið á **Í lagi**.
63. Smellið á **Bæta við einingu**.
64. Í svæðið Heiti skal færa inn **Upphæð**.
65. Smellið á **Í lagi**.

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a>Undirbúa íhluti sniðs fyrir vörpun í einingar gagnalíkans
1. Í trénu skal velja **Xml\Message\ProcessingDate**.
2. Smellið á **Bæta við** til að opna felligluggann.
3. Í trénu skal velja **Text\DateTime**.
4. Í svæðið **Snið** skal færa inn **áááá-MM-dd**.
5. Smellið á **Í lagi**.
6. Í trénu skal velja **Xml\Message\Payments\Item\TransDate**.
7. Smellið á **Bæta við DateTime**.
8. Í svæðið **Snið** skal færa inn **áááá-MM-dd**.
9. Í svæðisgerðinni **DateTime** skal velja **Dagsetning**.
10. Smellið á **Í lagi**.
11. Í trénu skal velja **Xml\Message\MessageId**.
12. Smellið á **Bæta við** til að opna felligluggann.
13. Í trénu skal velja **Text/String**.
14. Smellið á **Í lagi**.
15. Í trénu skal velja **Xml\Message\Payments\Item\Vendor\Name**.
16. Smellið á **Bæta við streng**.
17. Smellið á **Í lagi**.
18. Í trénu skal velja **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.
19. Smellið á **Bæta við streng**.
20. Smellið á **Í lagi**.
21. Í trénu skal velja **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.
22. Smellið á **Bæta við streng**.
23. Smellið á **Í lagi**.
24. Í trénu skal velja **Xml\Message\Payments\Item\Payer\Name**.
25. Smellið á **Bæta við streng**.
26. Smellið á **Í lagi**.
27. Í trénu skal velja **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.
28. Smellið á **Bæta við streng**.
29. Smellið á **Í lagi**.
30. Í trénu skal velja **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.
31. Smellið á **Bæta við streng**.
32. Smellið á **Í lagi**.
33. Í trénu skal velja **Xml\Message\Payments\Item\Currency**.
34. Smellið á **Bæta við streng**.
35. Smellið á **Í lagi**.
36. Í trénu skal velja **Xml\Message\Payments\Item\Description**.
37. Smellið á **Bæta við streng**.
38. Smellið á **Í lagi**.
39. Í trénu skal velja **Xml\Message\Payments\Item\Amount**.
40. Smellið á **Bæta við streng**.
41. Smellið á **Í lagi**.
42. Smellið á **Vista**.
43. Lokið síðunni.

