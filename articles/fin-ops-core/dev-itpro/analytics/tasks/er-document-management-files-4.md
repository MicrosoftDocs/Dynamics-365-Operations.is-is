---
title: Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum (Hluti 4 - keyra snið)
description: Þessi grein útskýrir hvernig á að skilgreina snið rafrænnar skýrslugerðar til að nota skrár skjalastjórnunar í úttaki rafrænnar skýrslugerðar. (Hluti 4)
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
ms.openlocfilehash: 3d4e26d15ea287c99cac85bf383e09c15729d37a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290965"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4---run-format"></a>Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum (Hluti 4 - keyra snið)

[!include [banner](../../includes/banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) svo það noti skrár skjalastjórnunar (viðhengi) í rafrænar skýrslur. Hægt er að framkvæma þessum skrefum í DEMF fyrirtækinu.

Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í ferlinu „Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum (Hluti 3: stofna snið)”.

Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a>Bæta þarf við nauðsynlegum viðhengi fyrir sölupöntun eins reiknings
1. Farið í Viðskiptakröfur > Reikningar > Opna reikninga viðskiptavina.
2. Nota flýtiafmörkun til að finna færslur Til dæmis sía á reitnum reikningur með gildinu 'CIV-000148'.
    * CIV-000148  
3. Smellið til að fylgja tengli í valdinn reikning.
    * CIV-000148  
4. Smellið til að velja tengilinn í reitnum sölupöntun.
    * 000148  
5. Í reitnum Línur eða haus skal velja valkostinn haus.
    * Veljið Haus til að gefa til kynna að þetta verði markið til að bæta við viðhengjum.  
6. Smellt er á Hengja við.
    * Bæta nokkrar skrár við sem viðhengi fyrir þessa sölupöntun. Nota skrár af skjalagerðir sem eru studdar af Skjalastjórnun (með skráarendingar DOCX, DPF XML, JPG, o.s.frv.). Flettið og veljið skrár til að hengja við og vinna meira með tengdum reikningi í rafræn skilaboð rafrænnar skýrslugerðar.  
7. Smellið á „Nýtt“.
8. Smella á Skrá
9. Smellið á „Nýtt“.
10. Smella á Skrá
11. Lokið síðunni.
12. Lokið síðunni.
13. Lokið síðunni.
14. Lokið síðunni.

## <a name="run-the-designed-report-for-the-selected-invoice"></a>Keyra viðkomandi skýrslu fyrir valinn reikning
1. Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.
2. Í trénu, veljið 'Customer invoice model'.
3. Í trénu skal víkka út 'Customer invoice model\Customer invoice model (custom)'.
4. Í trénu, veljið 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.
5. Smellið á „Keyra“.
6. Útvíkka Færslur til að taka () hluta.
7. Smellt er á Síu.
8. Velja línu reikningabókar viðskiptavinar og reitinn sölupöntun.
9. Í svæðinu Skilyrði skal færa inn '000148'.
    * Í forsendusvæðinu „sölupöntun” skal færa inn pöntunarnúmer 000148.  
10. Smellt er á Í lagi.
11. Smellt er á Í lagi.
    * Fara yfir myndað úttak. Athugið að fyrir hvert viðhengi hefur verið stofnað einu xml-hnútur. Innihald viðhengis er notað til að fylla út í úttak XML í MIME (base64) textasnið.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
