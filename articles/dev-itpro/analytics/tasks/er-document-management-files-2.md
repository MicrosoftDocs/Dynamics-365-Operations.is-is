--- 
title: "Víkka gagnalíkan til að nota skjalastjórnunarskrár í sniðsúttökum"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) svo það noti skrár skjalastjórnunar (viðhengi) í rafrænar skýrslur."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: bde8c612af22ba6bf4561732399fcf2cb1b5c9b3
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="extend-data-model-to-use-document-management-files-in-format-outputs"></a>Víkka gagnalíkan til að nota skjalastjórnunarskrár í sniðsúttökum

[!include [task guide banner](../../includes/task-guide-banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) svo það noti skrár skjalastjórnunar (viðhengi) í rafrænar skýrslur. Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.

Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í á “Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum (Hluti 1: undirbúa gagnalíkans” verkefnaleiðbeiningar.

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

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-data-sources"></a>Varpa nýjum einingum gagnalíkans á gagnaveitur Dynamics 365 for Finance and Operations
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


