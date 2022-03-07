---
title: Rafræn skýrslugerð nota svið sem má stækka lárétt til að bæta við dálkum gagnvirkt við í Excel skýrslum (Hluti 2 - Keyra snið)
description: Í þessu efni er útskýrt hvernig á að skilgreina snið rafrænnar skýrslugerðar til að mynda skýrslur sem OPENXML-vinnublaðaskrár (Excel). (Hluti 2)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22a7b2ce07aa172ab759d6e18d34afd7aa21609acc7fe5fc691244b66c4379a6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712617"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a>Rafræn skýrslugerð nota svið sem má stækka lárétt til að bæta við dálkum gagnvirkt við í Excel skýrslum (Hluti 2 - Keyra snið)

[!include [banner](../../includes/banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) til að mynda skýrslur sem OPENXML-vinnublöð (Excel) skrár þar sem hægt er að stofna nauðsynlega dálka gagnvirkt sem svið sem má stækka lárétt. Hægt er að framkvæma þessum skrefum í DEMF fyrirtækinu.

Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í ferlinu „Rafræn skýrslugerð nota svið sem má stækka lárétt til að bæta við dálkum gagnvirkt við í Excel skýrslum (Hluti 1: hanna skjámynd)”.

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
    * Fara yfir myndað úttak. Athugið að nýstofnuð Excel-skráin inniheldur sama fjölda dálka sem voru valdar fyrir fjárhagsvíddir. Haus í þeim dálkum táknar heiti fjárhagsvídda. Línur færslanna í þessum dálkum tákna heiti fjárhagsvídda. Keyra þessa skýrslu og veljið mismunandi víddir til að sjá að skýrslan er ekki háð fjölda valinna vídda eða fjölda vídda sem skilgreint er fyrir þetta tilvik.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]