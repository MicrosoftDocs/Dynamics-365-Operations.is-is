---
title: Rafræn skýrslugerð Nota Fjárhagsvíddir sem gagnaveita (Hluti 4 - keyra skýrslu)
description: Þetta efni útskýrir hvernig á að skilgreina líkan rafrænnar skýrslugerðar til að nota fjárhagsvíddir sem gagnagjafa fyrir skýrslur rafrænnar skýrslugerðar. (Hluti 4)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1fe332de84339d3369ba495ca13f50c4901f366
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092276"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a>Rafræn skýrslugerð Nota Fjárhagsvíddir sem gagnaveita (Hluti 4 - keyra skýrslu)

[!include [banner](../../includes/banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt líkan rafrænnar skýrslugerðar (ER) svo það noti fjárhagsvíddir sem gagnaveitu fyrir rafrænar skýrslur. Hægt er að framkvæma þessum skrefum í DEMF fyrirtækinu.

Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í ferlinu „ER Nota fjárhagsvíddir sem gagnaveitu (Hluti 3: hanna skýrslu)”. Einnig þarf að skilgreina sjálfgefnar gerðir skjala á færibreytusíðu Rafrænnar skýrslugerðar. Sjálfgefið gerðir skjala eru einnig stilltar þegar þú sækir og flytja inn hvers kyns grunnstillingar ræfrænna skýrslna (ER). 


## <a name="run-report"></a>Keyra skýrslu.
1. Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.
2. Í trénu skal víkka út 'Financial dimensions sample model'.
3. Í trénu skal velja 'Financial dimensions sample model\Ledger journal report'.
4. Smella á Keyra.
![Skilgreiningarsíða í ER](../media/er-financial-dimensions-guides-run1.png)
5. Sláið inn eða veljið gildi í reitnum heiti víddar.
    * Til að velja allar víddir í núverandi fyrirtæki skal færa inn eftirfarandi upplýsingar:  
![Skilgreiningarsíða í ER](../media/er-financial-dimensions-guides-run2.png)
6. Útvíkka Færslur til að taka hluta.
7. Smellt er á Síu.
8. Velja línuna fyrir töflu færslubókar fjárhags og reitinn rununúmer bókarkeyrslu.
9. Í svæðinu Skilyrði skal færa inn '00057'.
10. Smellt er á Í lagi.
11. Smellt er á Í lagi.
![Skilgreiningarsíða í ER](../media/er-financial-dimensions-guides-run3.png)
    * Fara yfir myndað úttak. Fyrir hverja færslu fyrir valda runu eru birtar fjárhagsvíddir úr viðeigandi víddarmengjum. Keyra þessa skýrslu og veljið mismunandi víddir til að sjá að skýrslan er ekki háð fjölda valinna vídda eða fjölda vídda sem skilgreint er fyrir þetta tilvik.  
![Skilgreiningarsíða í ER](../media/er-financial-dimensions-guides-run4.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]