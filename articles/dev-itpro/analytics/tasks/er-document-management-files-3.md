---
title: Búa til snið til að nota skjalastjórnunarskrár í sniðsúttökum rafrænnar skýrslugerðar
description: Eftirfarandi skref útskýra hvernig notandi með hlutverk kerfisstjóra eða þróunaraðila rafrænnar skýrslugerðar getur stillg snið rafrænnar skýrslugerðar til að nota skjalastjórnunarskrár í rafrænum skýrslum.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 05c0c4a38f34774e7018504c5e3fab834a2ec1b1
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850280"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3-create-format"></a>Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum (Hluti 3: stofna snið)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) svo það noti skrár skjalastjórnunar (viðhengi) í rafrænar skýrslur. Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.

Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í á “Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum (Hluti 2: framlengja gagnalíkans” ferli.

Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.


## <a name="create-a-format-to-process-invoices"></a>Stofna snið til að vinna reikninga
1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
2. Smelltu á Grunnstillingar skýrslugerðar
3. Í trénu, veljið 'Customer invoice model'.
4. Í trénu, veljið 'Customer invoice model\Customer invoice model (custom)'.
    * Þú munt stofna snið til að stofna rafræn skilaboð með upplýsingar um allar skrám sem hafa verið tengdar við sölupöntun sem er tengt við rafrænt unninn reikning.  
5. Smellt er á stofna skilgreiningu til að opna fellilistanum.
6. Í nýja svæðinu, færðu inn „Snið byggir á gagnalíkani líkan reikningur viðskiptavinar (sérstillt)“.
7. Í svæðið Heiti skal færa inn 'dæmi um skilaboð Rafrænn reikningur'.
    * Dæmi um skilaboð Rafræns reiknings  
8. Í reitinn Skilgreining Gagnalíkans skal slá inn eða velja gildi.
    * InvoiceCustomer  
9. Smelltu á Stofna skilgreiningu.

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a>Breyta sniði til að fylla út viðhengi í myndun skilaboða í MIME-sniði
1. Smellið á Hönnuður.
2. Smelltu á Bæta við rót til að opna felligluggann.
3. Í trénu skal velja „XML/Element“.
4. Í reitnum Heiti skal færa inn ‚reikningur'.
    * Reikningur  
5. Smellið á „Í lagi“.
6. Smelltu á Bæta við til að opna felligluggann.
7. Í trénu skal velja „XML/Attribute“.
8. Í svæðið Heiti, færðu inn 'SalesOrder'.
    * SalesOrder  
9. Smellið á „Í lagi“.
10. Smella á Bæta við eigind.
11. Í svæðið Heiti, færðu inn 'InvoiceNumber'.
    * InvoiceNumber  
12. Smellið á „Í lagi“.
13. Smella á Bæta við eigind.
14. Í svæðið Heiti, færðu inn 'InvoiceAmount'.
    * InvoiceAmount  
15. Smellið á „Í lagi“.
16. Smelltu á Bæta við til að opna felligluggann.
17. Í trénu skal velja „XML/Element“.
18. Í svæðið Heiti, færðu inn 'EnclosedDocs'.
    * EnclosedDocs  
19. Smellið á „Í lagi“.
20. Í trénu skal velja 'Invoice\EnclosedDocs'.
21. Smella á bæta Við einingu.
22. Í svæðið Heiti, færðu inn 'skjal'.
    * Skjal  
23. Smellið á „Í lagi“.
24. Í trénu skal velja 'Invoice\EnclosedDocs\Document'.
25. Smelltu á Bæta við til að opna felligluggann.
26. Í trénu skal velja „XML/Attribute“.
27. Í svæðið Heiti, færðu inn 'FileName'.
    * Skráarheiti  
28. Smellið á „Í lagi“.
29. Smelltu á Bæta við til að opna felligluggann.
30. Í trénu skal velja „XML/Element“.
31. Í svæðið Heiti, færðu inn 'FileContent'.
    * FileContent  
32. Smellið á „Í lagi“.
33. Í trénu skal velja 'Invoice\EnclosedDocs\Document\FileContent'.
34. Smelltu á Bæta við til að opna felligluggann.
35. Í trénu skal velja 'Text\Base64'.
36. Smellið á „Í lagi“.

## <a name="map-format-elements-to-data-model-as-data-source"></a>Varpa sniðsíhlutum í gagnalíkan sem gagnaveitu
1. Í trénu skal velja 'Invoice\SalesOrder'.
2. Smelltu á flipann Vörpun.
3. Í trénu skal víkka út 'model'.
4. Í trénu skal velja 'model\Sales order number(SalesId)'.
5. Smelltu á Binda.
6. Í trénu skal velja 'Invoice\InvoiceNumber'.
7. Í trénu skal víkka út 'model\Base invoice(InvoiceBase)'.
8. Í trénu skal velja 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.
9. Smelltu á Binda.
10. Í trénu skal velja 'Invoice\InvoiceAmount'.
11. Í trénu skal velja 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.
12. Smelltu á Binda.
13. Í trénu, stækka 'model\Invoice attachments'.
14. Í trénu skal velja 'model\Invoice attachments\File content'.
15. Í trénu skal velja 'Invoice\EnclosedDocs\Document\FileContent\Base64'.
16. Smelltu á Binda.
17. Í trénu skal velja 'model\Invoice attachments\File name'.
18. Í trénu skal velja 'Invoice\EnclosedDocs\Document\FileName'.
19. Smelltu á Binda.
20. Í trénu skal velja 'model\Invoice attachments'.
21. Í trénu skal velja 'Invoice\EnclosedDocs\Document'.
22. Smelltu á Binda.
23. Smellið á „Vista“.
24. Lokið síðunni.

