---
title: "Birta færslubókarlínur og skjöl úr Excel"
description: "Í þessu efnisatriði er útskýrt hvernig á að færa inn og birta línur fyrir almennar færslubækur úr Microsoft Excel. Það felur í sér upplýsingar um mismunandi sniðmát sem nota má, eftir gerð þeirra færslna sem verið er að færa inn."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a43bf66de7602aa9fb47925996ec5b979e1f8dac
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="publish-journal-lines-and-documents-from-excel"></a>Birta færslubókarlínur og skjöl úr Excel

[!include[banner](../includes/banner.md)]


Í þessu efnisatriði er útskýrt hvernig á að færa inn og birta línur fyrir almennar færslubækur úr Microsoft Excel. Það felur í sér upplýsingar um mismunandi sniðmát sem nota má, eftir gerð þeirra færslna sem verið er að færa inn.

Notendur geta fært inn og birt línur fyrir fjárhagsbækur úr Microsoft Excel. Þegar notandi stofnar færslubók, birtir **Opna línur í Excel** hnappurinn sniðmát sem eru í boði. Sniðmát eru hönnuð til að styðja tilteknar aðstæður, hins vegar styður færslubókin ekki allar samsetningar reikningsgerða. Eftirfarandi tafla sýnir sniðmátin sem eru í boði og reikningagerðir sem þau styðja.
|                          |                                                                                                                         |                                                                                         |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **Sniðmát**             | **Studdar reikningsgerðir**                                                                                             | **Hvernig sniðmátið er valið**                                                          |
| Fjárhagsfærslubókarlínur     | Reikningar: Fjárhagur, Viðskiptavinur, Lánardrottinn, Mótfærslureikningur banka: Fjárhagur, Viðskiptavinur, Lánardrottinn, Samstæðulykill banka er studd.       | Almenn færslubók                                                                         |
| Komubók         | Reikningar: Mótlykill lánardrottins: Fjárhagssamstæða er ekki studd.                                                    | Viðskiptaskuldir, komubók                                                                     |
| Reikningabók          | Reikningar: Mótlykill lánardrottins: Fjárhagssamstæða er studd.                                                      | Færslubók fyrir reikninga viðskiptavinar                                                                      |
| Reikningur frá lánardrottni           |                                                                                                                         | Reikningur frá lánardrottni                                                                          |
| Reikningabók viðskiptavinar | Reikningar: Mótlykill viðskiptamanns: Fjárhagssamstæða er studd.                                                     | Almenn færslubók                                                                         |
| Textareikningur        |                                                                                                                         | Á **Reikningur með frjálsum texta** síðunni er smellt á **Opna í Excel** (Microsoft Office táknið). |
| Eignabók     | Eign í fjárhag, banki, viðskiptavinur eða lánardrottin. Samstæða er ekki studd.                                               | Eignabók                                                                     |
| Greiðslubók lánardrottins   | Reikningar: Mótlykill lánardrottins: Fjárhagur, samstæðulykill banka er studd.                                                 | Greiðslubók lánardrottins                                                                  |
| Greiðslubók viðskiptavinar | Reikningar: Mótlykill viðskiptamanns: Fjárhagur, samstæðulykill banka er studd.                                               | Greiðslubók viðskiptavinar                                                                |
| Kostnaðarbók verk  | Reikningur: Verkefni, Fjárhagur, Viðskiptavinur, Mótlykill lánardrottins: Verkefni, Fjárhagur´, Viðskiptamaður, Samstæðulykill lánardrottins er studd. | Almenn kostnaðarfærslubók (undir verkefnastjórnun og bókhald)                       |

Þegar línur eru birtar eru þær villuleitaðar til að tryggja að þær samræmist reglum sem eru settar upp í fjárhagsbækur. Eftir að línur eru birtar geta notendur breytt eða birt fylgiskjöl úr Microsoft Dynamics 365 for Operations. 

Til að bæta fjárhagsvíddum við sniðmát eru frekari breytingar nauðsynlegar. Nánari upplýsingar er að finna í [Víddum bætt við Microsoft Excel-sniðmát](/dynamics365/operations/dev-itpro/financial/add-dimensions-excel-templates). Eftir að víddum er bætt við eininguna, eru þær tiltæk í Excel hönnuði og hægt að bæta þeim við sniðmátið.





