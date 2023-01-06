---
title: Birta færslubókarlínur og skjöl úr Excel
description: Í þessari grein er útskýrt hvernig á að færa inn og birta línur fyrir almennar færslubækur úr Microsoft Excel. Það felur í sér upplýsingar um mismunandi sniðmát sem nota má, eftir gerð þeirra færslna sem verið er að færa inn.
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.custom: 62213
ms.assetid: 211874a7-4bf0-4a0c-96c2-fa05042777d3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ccb3e7a420f7f048ba93b6fadf5491e312e7ce33
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872471"
---
# <a name="publish-journal-lines-and-documents-from-excel"></a>Birta færslubókarlínur og skjöl úr Excel

[!include [banner](../includes/banner.md)]

Í þessari grein er útskýrt hvernig á að færa inn og birta línur fyrir almennar færslubækur úr Microsoft Excel. Það felur í sér upplýsingar um mismunandi sniðmát sem nota má, eftir gerð þeirra færslna sem verið er að færa inn.

Notendur geta fært inn og birt línur fyrir fjárhagsbækur úr Microsoft Excel. Þegar notandi stofnar færslubók, birtir **Opna línur í Excel** hnappurinn sniðmát sem eru í boði. Sniðmát eru hönnuð til að styðja tilteknar aðstæður, hins vegar styður færslubókin ekki allar samsetningar reikningsgerða. Eftirfarandi tafla sýnir sniðmátin sem eru í boði og reikningagerðir sem þau styðja.

| Sniðmát             | Studdar reikningsgerðir | Hvernig sniðmátið er valið                                                          |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| Fjárhagsfærslubókarlínur     | Reikningar: Fjárhagur, Viðskiptavinur, Lánardrottinn, Mótfærslureikningur banka: Fjárhagur, Viðskiptavinur, Lánardrottinn, Samstæðulykill banka er studd.       | Almenn færslubók                                                                         |
| Komubók         | Reikningar: Mótlykill lánardrottins: Fjárhagssamstæða er ekki studd.                                                    | Viðskiptaskuldir, komubók                                                                     |
| Reikningabók          | Reikningar: Mótlykill lánardrottins: Fjárhagssamstæða er studd.                                                      | Færslubók fyrir reikninga viðskiptavinar                                                                      |
| Reikningur frá lánardrottni           |                                                                                                                         | Reikningur frá lánardrottni                                                                          |
| Reikningabók viðskiptavinar | Reikningar: Mótlykill viðskiptamanns: Fjárhagssamstæða er studd.                                                     | Almenn færslubók                                                                         |
| Reikningur með frjálsum texta        |                                                                                                                         | Á **Reikningur með frjálsum texta** síðunni er smellt á **Opna í Excel** (Microsoft Office táknið). |
| Eignabók     | Eign í fjárhag, banki, viðskiptavinur eða lánardrottin. Samstæða er ekki studd.                                               | Eignabók                                                                     |
| Greiðslubók lánardrottins   | Reikningar: Mótlykill lánardrottins: Fjárhagur, samstæðulykill banka er studd.                                                 | Greiðslubók lánardrottins                                                                  |
| Greiðslubók viðskiptavinar | Reikningar: Mótlykill viðskiptamanns: Fjárhagur, samstæðulykill banka er studd.                                               | Greiðslubók viðskiptavinar                                                                |
| Kostnaðarbók verk  | Reikningur: Verkefni, Fjárhagur, Viðskiptavinur, Mótlykill lánardrottins: Verkefni, Fjárhagur´, Viðskiptamaður, Samstæðulykill lánardrottins er studd. | Almenn kostnaðarfærslubók (undir verkefnastjórnun og bókhald)                       |

Þegar línur eru birtar eru þær villuleitaðar til að tryggja að þær samræmist reglum sem eru settar upp í fjárhagsbækur. Eftir að línur eru birtar geta notendur breytt eða birt fylgiskjöl úr Dynamics 365 Finance. 

Til að bæta fjárhagsvíddum við sniðmát eru frekari breytingar nauðsynlegar. Nánari upplýsingar er að finna í [Víddum bætt við Microsoft Excel sniðmát](../../fin-ops-core/dev-itpro/financial/add-dimensions-excel-templates.md). Eftir að víddum er bætt við eininguna, eru þær tiltæk í Excel hönnuði og hægt að bæta þeim við sniðmátið.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
