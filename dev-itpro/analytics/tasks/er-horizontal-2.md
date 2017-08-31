--- 
title: "Keyra snið sem notar svæði sem hægt er að stækka lárétt til að bæta gagnvirkt við dálkum í Excel-skýrslum fyrir rafræna skýrslugerð (ER)"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) til að mynda skýrslur sem OPENXML-vinnublöð (Excel) skrár þar sem hægt er að stofna nauðsynlega dálka gagnvirkt sem svið sem má stækka lárétt."
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 4b859151edd28e39c1f97b2f600da6e304b1d065
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="run-a-format-that-uses-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-for-electronic-reporting-er"></a>Keyra snið sem notar svæði sem hægt er að stækka lárétt til að bæta gagnvirkt við dálkum í Excel-skýrslum fyrir rafræna skýrslugerð (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) til að mynda skýrslur sem OPENXML-vinnublöð (Excel) skrár þar sem hægt er að stofna nauðsynlega dálka gagnvirkt sem svið sem má stækka lárétt. Hægt er að framkvæma þessum skrefum í DEMF fyrirtækinu.

Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í á "Rafræn skýrslugerð nota svið sem má stækka lárétt til að bæta við dálkum gagnvirkt við í Excel skýrslum (Hluti 1: hanna skjámynd)" ferli.

Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.


## <a name="find-created-format"></a>Leita að stofnuðu sniði
1. Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.
2. Í trénu skal víkka út 'Financial dimensions sample model'.
3. Í trénu skal velja 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.

## <a name="execute-format-to-create-excel-output"></a>Keyra snið til að stofna Excel-úttak
1. Smellið á „Keyra“.
2. Í reitinn Heiti víddar skal slá inn 'BusinessUnit;CostCenter;Department'.
    * Sláið inn eða veljið gildi í reitnum heiti víddar.  Til að velja allar víddir í núverandi fyrirtæki skal færa inn eftirfarandi:BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
3. Útvíkka Færslur til að taka hluta.
4. Smellt er á Síu.
5. Velja línuna fyrir töflu færslubókar fjárhags og reitinn rununúmer bókarkeyrslu.
6. Í svæðinu Skilyrði skal færa inn '00057..00058'.
    * 00057..00058  
7. Smellið á „Í lagi“.
8. Smellið á „Í lagi“.
    * Fara yfir myndað úttak. Athugið að nýstofnuð Excel-skráin inniheldur sama fjölda dálka sem voru valdar fyrir fjárhagsvíddir. Haus í þeim dálkum táknar heiti fjárhagsvídda. Línur færslanna í þessum dálkum tákna heiti fjárhagsvídda. Keyra þessa skýrslu og veljið mismunandi víddir til að sjá að skýrslan er ekki háð fjölda valinna vídda eða fjölda vídda sem skilgreint er fyrir þetta Dynamics 365 for Finance and Operations, Enterprise edition tilvik.  


