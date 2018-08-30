--- 
title: "Breyta og keyra snið til að nota skjalastjórnunarskrár í sniðsúttökum rafrænnar skýrslugerðar"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) svo það noti skrár skjalastjórnunar (viðhengi) í rafrænar skýrslur."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 5effbecf98e633d07f9e5eb22d3df1a12967c1e4
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2018

---
# <a name="modify-and-run-formats-to-use-document-management-files-in-er-output"></a>Breyta og keyra snið til að nota skjalastjórnunarskrár í sniðsúttökum rafrænnar skýrslugerðar

[!include [task guide banner](../../includes/task-guide-banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) svo það noti skrár skjalastjórnunar (viðhengi) í rafrænar skýrslur. Hægt er að framkvæma þessum skrefum í DEMF fyrirtækinu.

Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í á “Rafræn skýrslugerð nota skrár skjalastjórnunar í sniðsúttökum (Hluti 4: keyra snið)” ferli.

Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a>Breyta sniði til að fylla út viðhengi í myndun skilaboða í tvíundar sniði
1. Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.
2. Í trénu, veljið 'Customer invoice model'.
3. Í trénu skal víkka út 'Customer invoice model\Customer invoice model (custom)'.
4. Í trénu, veljið 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.
5. Smellið á Hönnuður.
    * Þú munt fylla út skilaboð reiknings í myndandi úttaki sem XML-skrá með því að nota Unicode-dulritun.  
6. Smelltu á Bæta við rót til að opna felligluggann.
7. Veljið 'Common\File', í trénu.
8. Í reitnum Heiti skal færa inn ‚Xml-skilaboð‘.
    * Xml skilaboð  
9. Í reitinn Kóðun skal slá inn „UTF-8“.
    * UTF-8  
10. Smellið á „Í lagi“.
    * Skilgreina myndun úttaks sem zip-skrá.  
11. Smelltu á Bæta við rót til að opna felligluggann.
12. Í trénu skal velja 'Common\Folder'.
13. Í svæðið Heiti, færðu inn 'úttak zip-skrár'.
    * Úttak Zip-skrár  
14. Smellið á „Í lagi“.
15. Í trénu skal velja „Úttak zip-skrár“.
    * Bæta við viðhengjum við myndandi zip-skrá sem skrár með upphaflegu nöfn og viðauka.  
16. Smelltu á Bæta við til að opna felligluggann.
17. Veljið 'Common\File', í trénu.
18. Í svæðið Heiti, færðu inn 'skrá í viðhengi'.
    * Hengja við skrá  
19. Smellið á „Í lagi“.
20. Í trénu skal velja 'Zip output\Attached file'.
21. Smelltu á Bæta við til að opna felligluggann.
22. Í trénu skal velja 'Text\Base64'.
23. Smellið á „Í lagi“.

## <a name="map-new-format-elements-to-data-model"></a>Varpa nýjum einingum sniðs í gagnalíkan.
1. Smelltu á flipann Vörpun.
2. Í trénu skal víkka út 'model'.
3. Í trénu, stækka 'model\Invoice attachments'.
4. Í trénu skal velja 'Zip output\Attached file\Base64'.
5. Í trénu skal velja 'model\Invoice attachments\File content'.
6. Smelltu á Binda.
7. Í trénu skal velja 'Zip output\Attached file'.
8. Smelltu á Breyta skrárheiti
9. Í trénu skal víkka út 'model'.
10. Í trénu, stækka 'model\Invoice attachments'.
11. Í trénu skal velja 'model\Invoice attachments\File name'.
12. Smellt er á Bæta við gagnagjafa.
13. Smelltu á Vista.
14. Lokið síðunni.
15. Í trénu skal velja 'model\Invoice attachments'.
16. Smelltu á Binda.
17. Smellið á „Vista“.
18. Lokið síðunni.

## <a name="run-the-designed-report-for-the-selected-invoice"></a>Keyra viðkomandi skýrslu fyrir valinn reikning
1. Smellið á „Keyra“.
2. Útvíkka Færslur til að taka () hluta.
3. Smellt er á Síu.
4. Velja línu reikningabókar viðskiptavinar og reitinn sölupöntun.
5. Í forsendusvæðinu, í forsendusvæðinu “sölupöntun”, skal færa inn pöntunarnúmer 000148.
    * 000148  
6. Smellið á „Í lagi“.
7. Smellið á „Í lagi“.
    * Fara yfir myndað úttak. Athugið að auk skilaboð reiknings í xml-sniði, hefur eina skrá verið stofnuð fyrir hverja viðhengi. Viðhegndar skrárnar eru fyllt út með úttaki zip-skrár með tvíundarsniði.  


