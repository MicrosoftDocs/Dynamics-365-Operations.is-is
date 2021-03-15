---
title: Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum(Hluti 2 - framlengja gagnalíkan)
description: Í þessu efni er útskýrt hvernig á að skilgreina snið rafrænnar skýrslugerðar til að nota skrár skjalastjórnunar (viðhengi) í úttaki rafrænnar skýrslugerðar. (Hluti 2)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd06cdfd9bae57577c2e3ec97848e319b197f41
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092592"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a>Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum(Hluti 2 - framlengja gagnalíkan)

[!include [banner](../../includes/banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) svo það noti skrár skjalastjórnunar (viðhengi) í rafrænar skýrslur. Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.

Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í verkleiðbeiningunum „Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum (Hluti 1: undirbúa gagnalíkan)”.

Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a>Framlengja gagnalíkan til að birta skrár Skjalastjórnunar í því
1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
2. Smelltu á Grunnstillingar skýrslugerðar
3. Í trénu, veljið 'Customer invoice model'.
4. Í trénu, veljið 'Customer invoice model\Customer invoice model (custom)'.
5. Smellið á Hönnuður.
6. Í trénu skal velja select 'Customer invoice(InvoiceCustomer)'.
    * Við munum útvíkka þetta gagnalíkan til að birta það í öllum skrám sem hafa verið tengdar við sölupöntun sem er tengt við rafrænt unninn reikning.  
7. Smellt er á Nýtt til að opna felligluggann.
8. Í svæðið Heiti, færðu inn 'viðhengi reiknings'.
    * Viðhengi reiknings  
9. Veljið í svæðinu gerð Vöru „Skrárlisti".
10. Smelltu á Bæta við.
11. Smellt er á Nýtt til að opna felligluggann.
12. Í svæðið Heiti, færðu inn 'innihald skráa'.
    * Innihald skráar  
13. Velja 'geymir' í svæðinu gerð Vöru.
14. Smelltu á Bæta við.
15. Smellt er á Nýtt til að opna felligluggann.
16. Í svæðið Heiti, færðu inn 'skrárnafn'.
    * Skrárnafn  
17. Veljið 'Strengur' í svæðinu Vöru.
18. Smelltu á Bæta við.

## <a name="map-new-data-model-elements-to-data-sources"></a>Varpa nýjum einingum gagnalíkans við gagnaveitur
1. Smellt er á Varpa líkani á gagnagjafa.
2. Nota flýtiafmörkun á skilgreiningarreit með gildið 'InvoiceCustomer'.
    * InvoiceCustomer  
    * Við vörpum nýjum líkanaeiningum á viðkomandi gagnaveitur.  
3. Smellið á Hönnuður.
4. Í trénu skal velja „viðhengi reiknings“.
5. Í trénu skal víkka út "viðhengi reiknings".
6. Í trénu skal velja 'Invoice attachments\File name'.
7. Smellið á „Breyta“.
8. Í svæði Formúla slá inn „CustInvoiceJour.„>Relations“.SalesTable.„<Relations“.„<Documents“.„originalFileName()““.
    * CustInvoiceJour.„>Relations“.SalesTable.„<Relations“.„<Documents“.„originalFileName()“  
9. Smellið á „Vista“.
10. Lokið síðunni.
11. Í trénu skal velja 'Invoice attachments\File content'.
12. Smellið á „Breyta“.
13. Í svæði Formúla slá inn „CustInvoiceJour.„>Relations“.SalesTable.„<Relations“.„<Documents“.„getFileContentAsContainer()““.
    * CustInvoiceJour.„>Relations“.SalesTable.„<Relations“.„<Documents“.„getFileContentAsContainer()“  
14. Smellið á „Vista“.
15. Lokið síðunni.
16. Í trénu skal velja „viðhengi reiknings“.
17. Smellið á „Breyta“.
18. Í Formúlureitinn skal slá inn „CustInvoiceJour.“>Relations“.SalesTable.„<Relations“.„<Documents““.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'  
19. Smellið á „Vista“.
20. Lokið síðunni.
21. Smellið á „Vista“.
22. Lokið síðunni.
23. Lokið síðunni.
24. Lokið síðunni.
25. Smellið á „Breyta stöðu“.
26. Smelltu á Ljúka.
27. Smellið á „Í lagi“.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]