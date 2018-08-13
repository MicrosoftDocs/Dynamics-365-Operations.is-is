---
title: "Nám - Power BI efni"
description: "Þetta efnisatriði lýsir efni í Nám - Power BI."
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 0ee0cc2e22609d1a87e7d2b6dcd031606191f879
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="learning-power-bi-content"></a>Nám - Power BI efni

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir efninu **Nám** í Microsoft Power BI.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Skýrslur sem eru hafðir með í Power BI-efni

Skýrslur sem fylgja í efninu **Nám** í Power BI hafa bæði myndrit og töflur sem innihalda viðbótarupplýsingar. Eftirfarandi tafla lýsir skýrslunum.

| Skýrsla                | Innihald |
|-----------------------|----------|
| Námsyfirlit     | Yfirlit yfir aðrar skýrslur |
| Greining á námskeiði       | Skráning eftir staðsetningu, þátttakandi eftir stöðu, námskeið eftir gerð á fyrirtæki og námskeiðsviðera eftir starfi |
| Greining skráningar | Skráningarlisti |
| Námskeiðsgerðir          | Námskeiðsgerðir eftir hæfni |
| Greining leiðbeinanda   | Hlutfall námskeiða á leiðbeinendur, fjöldi leiðbeinenda, námskeið eftir leiðbeinanda, námskeið á leiðbeinanda og dagskrá námskeiðs eftir leiðbeinanda |
| Námskeið í boði       | Listi yfir námskeið |
| Hönnun námskeiða        | Dagskrá námskeiðs |

Hægt er að sía gröf og reiti í þessum skýrslum og festa gröf og reiti á yfirlitið. Nánari upplýsingar um hvernig á að sía og festa í Power BI, sjá [Stofna og Skilgreina Mælaborð](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar

Eftirfarandi gögn er notuð til að fylla út skýrslur í Power BI-efninu **Nám**. Þessi tafla sýnir einingar sem efnispakkinn var byggður á.

| Eining           | Innihald                                                         | Vensl við aðra lögaðila |
|------------------|------------------------------------------------------------------|-----------------------------------|
| Dagsetning starfsupphafs  | Mótbókanir dagatals til að sneiða skýrslur                                | Dagskrá námskeiðs, þáttakendur námskeiðs |
| Fyrirt.            | Fyrirtæki til að sía skýrsla eftir                                   | Dagskrá námskeiðs, þáttakendur námskeiðs |
| Námskeið           | Námskeið, lýsingu, heiti leiðbeinanda, staðsetning, pláss og staða | Dagskrá námskeiðs, þáttakendur námskeiðs, námskeiðshæfni |
| Dagskrá námskeiðs    | Dagskrá, námskeið og upphafs-og lokatími                          | Fyrirtæki, dagsetning starfsupphafs, dagsetning, námskeið |
| Þátttakendur námskeiðs | Heiti, staða, vinnslu og skráningardagur                         | Fyrirtæki, dagsetning starfsupphafs, dagsetning, námskeið, lýðfræði, atvinna, námskeið, nafn starfsmanns, titill starfsmanns, starf, staða |
| Hæfni námskeiðs     | Hæfni, gerð hæfni og stig                                     | Námskeið |
| Dagsetning             | Dagar, vikur, mánuðir og ár                                   | Dagskrá námskeiðs, þáttakendur námskeiðs |
| Lýðfræði     | Fæðingardagur, kyn, þjóðernisuppruni og hjúskapaarstaða         | Dagskrá námskeiðs, þáttakendur námskeiðs |
| Ráðning       | Upphafsdagur, lokadagur og breytingardagur                        | Dagskrá námskeiðs, þáttakendur námskeiðs |
| Starf              | Aðgerð, gerð og Titill                                        | Dagskrá námskeiðs, þáttakendur námskeiðs |
| Staða         | Staða, titill og jafngildi fulls starfs (FTE)                  | Dagskrá námskeiðs, þáttakendur námskeiðs |
| Nafn starfsmanns    | Fornafn, eftirnafn, og fullt nafn                             | Þátttakendur námskeiðs |
| Titill starfsmanns   | Titill og starfsaldursdagsetning                                         | Þátttakendur námskeiðs |

