---
title: "Birta færslubókarlínur og skjöl úr Excel"
description: "Í þessu efnisatriði er útskýrt hvernig á að færa inn og birta línurnar fyrir almennar færslubækur úr Microsoft Excel. Það felur í sér upplýsingar um mismunandi sniðmát sem nota má, eftir gerð þeirra færslna sem verið er að færa inn."
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62213
ms.assetid: 211874a7-4bf0-4a0c-96c2-fa05042777d3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 087339cb3002b42bcb985c2ccfc2d97c752a817c
ms.lasthandoff: 03/31/2017


---

# <a name="publish-journal-lines-and-documents-from-excel"></a>Birta færslubókarlínur og skjöl úr Excel

Í þessu efnisatriði er útskýrt hvernig á að færa inn og birta línurnar fyrir almennar færslubækur úr Microsoft Excel. Það felur í sér upplýsingar um mismunandi sniðmát sem nota má, eftir gerð þeirra færslna sem verið er að færa inn.

Notendur geta fært inn og birta línurnar fyrir fjárhagsbækur úr Microsoft Excel. Þegar notandi stofnar færslubók, er **Opna línur í Excel** hnappinn sniðmát sem eru birtir. Sniðmát eru hannaðar til að styðja við tilteknar aðstæður hins vegar ekki sérhverja samsetningu af gerð lykils er studd í færslubókinni. Eftirfarandi tafla sýnir gerðir lykla sem þeir styðja og sniðmát sem eru tiltækar.
|                          |                                                                                                                         |                                                                                         |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **Template**             | **Gerðir studd**                                                                                             | **Hvernig sniðmátið**                                                          |
| Fjárhagsfærslubókarlínur     | : Fjárhagur, Viðskiptavinar, Lánardrottins, Banka Mótfærsla lykil: Fjárhagur, Viðskiptavinur, Lánardrottinn, Banka innan Samstæðu er studd.       | Almenn færslubók                                                                         |
| Komubók         | : Mótlykill Lánardrottins lykils: Samstæðu Fjárhags er ekki studd.                                                    | AP komubók                                                                     |
| Reikningabók          | Lykla: Lykill Lánardrottins Mótlykill: Fjárhagur Samstæðu er studd.                                                      | Færslubók fyrir reikninga viðskiptavinar                                                                      |
| Reikningur frá lánardrottni           |                                                                                                                         | Reikningur frá lánardrottni                                                                          |
| Reikningabók viðskiptavinar | : Viðskiptavinur Mótlykill lykils: Fjárhagur Samstæðu er studd.                                                     | Almenn færslubók                                                                         |
| Textareikningur        |                                                                                                                         | Á við **textareikning** síðunni er smellt á **Opna í Excel** (Microsoft Office táknið). |
| Eignabók     | Eign fjárhagur, banki, viðskiptavin eða lánardrottin. Samstæða er ekki studd.                                               | Eignabók                                                                     |
| Greiðslubók lánardrottins   | : Mótlykill Lánardrottins lykils: Fjárhagur, Banki innan Samstæðu er studd.                                                 | Greiðslubók lánardrottins                                                                  |
| Greiðslubók viðskiptavinar | : Viðskiptavinur Mótlykill lykils: Fjárhagur, Banki innan Samstæðu er studd.                                               | Greiðslubók viðskiptavinar                                                                |
| Kostnaðarbók verk  | : Verk, Fjárhag Viðskiptavinar, Lánardrottins Mótfærsla lykil: Verk, Fjárhag, Viðskiptavin, Lánardrottinn innan Samstæðu er studd. | Almenn færslubók Kostnaðar (undir verkefnastjórnun og bókhald)                       |

Þegar línur eru birtar þær villuleit til að tryggja að þeir samræmast reglur sem eru settir upp í fjárhagslegar færslubækur. Þegar línur eru birtar geta notendur breyta eða bóka villulaus fylgiskjöl úr Microsoft Dynamics 365 aðgerða. 

Til að bæta fjárhagsvíddir sniðmát frekari breytingar krafist. Frekari upplýsingar, sjá [Bæta víddum við Microsoft Excel sniðmát](\dev-itpro\financial-dimensions\add-dimensions-excel-templates). Eftir víddum er bætt við einingu, þeir eru tiltæk í Excel hönnuði og er bætt við sniðmátið.




