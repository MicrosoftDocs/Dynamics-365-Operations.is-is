--- 
title: "Keyra snið til að nota skjalastjórnunarskrár fyrir snið frálags í rafrænni skýrslugerð (ER)"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) svo það noti skrár skjalastjórnunar (viðhengi) í rafrænar skýrslur."
author: NickSelin
manager: AnnBe
ms.date: 10/31/2016
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
ms.openlocfilehash: 419c3e305dfdd7d8612340b4a8e8e54e13c6362b
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="run-format-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a>Keyra snið til að nota skjalastjórnunarskrár fyrir snið frálags í rafrænni skýrslugerð (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) svo það noti skrár skjalastjórnunar (viðhengi) í rafrænar skýrslur. Hægt er að framkvæma þessum skrefum í DEMF fyrirtækinu.

Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í á “Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum (Hluti 3: stofna snið)” ferli.

Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a>Bæta þarf við nauðsynlegum viðhengi fyrir sölupöntun eins reiknings
1. Farið í Viðskiptakröfur > Reikningar > Opna reikninga viðskiptavina.
2. Nota flýtiafmörkun til að finna færslur Til dæmis sía á reitnum reikningur með gildinu 'CIV-000148'.
    * CIV-000148  
3. Smellið til að fylgja tenglinum í valdan reikning.
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
    * Í forsendusvæðinu “sölupöntun”, skal færa inn pöntunarnúmer 000148.  
10. Smellið á „Í lagi“.
11. Smellið á „Í lagi“.
    * Fara yfir myndað úttak. Athugið að fyrir hvert viðhengi hefur verið stofnað einu xml-hnútur. Innihald viðhengis er notað til að fylla út í úttak XML í MIME (base64) textasnið.  


