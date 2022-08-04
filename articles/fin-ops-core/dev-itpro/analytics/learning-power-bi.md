---
title: Power BI-efni um Learning
description: Þessi grein lýsir náminu Power BI efni.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 72b31fd4e204a5472561edfdf848be2dae0f0e5b
ms.sourcegitcommit: 3c4dd125ed321af8a983e89bcb5bd6e5ed04a762
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/28/2022
ms.locfileid: "9206179"
---
# <a name="learning-power-bi-content"></a>Power BI-efni um Learning

[!include [banner](../includes/banner.md)]

Þessi grein lýsir **Að læra** Microsoft Power BI efni.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Skýrslur sem eru hafðar með í Power BI efni

Skýrslur sem eru hafðar með í **Learning** Power BI efni hafa bæði gröf og töflur sem innihalda viðbótarupplýsingar. Eftirfarandi tafla lýsir skýrslunum.

| Skýrsla                | Innihald |
|-----------------------|----------|
| Námsyfirlit     | Yfirlit yfir aðrar skýrslur |
| Greining á námskeiði       | Skráning eftir staðsetningu, þátttakandi eftir stöðu, námskeið eftir gerð á fyrirtæki og námskeiðsviðera eftir starfi |
| Greining skráningar | Skráningarlisti |
| Námskeiðsgerðir          | Námskeiðsgerðir eftir hæfni |
| Greining leiðbeinanda   | Hlutfall námskeiða á leiðbeinendur, fjöldi leiðbeinenda, námskeið eftir leiðbeinanda, námskeið á leiðbeinanda og dagskrá námskeiðs eftir leiðbeinanda |
| Námskeið í boði       | Listi yfir námskeið |
| Hönnun námskeiða        | Dagskrá námskeiðs |

Hægt er að sía gröf og reiti í þessum skýrslum og festa gröf og reiti á yfirlitið. Nánari upplýsingar um hvernig á að sía og festa í Power BI, sjá [Stofna og Skilgreina Mælaborð](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar

Eftirfarandi gögn eru notuð til að fylla út skýrslurnar í **Learning** Power BI efninu. Þessi tafla sýnir einingar sem efnispakkinn var byggður á.

| Eining           | Innihald                                                         | Vensl við aðra lögaðila |
|------------------|------------------------------------------------------------------|-----------------------------------|
| Dagsetning starfsupphafs  | Mótbókanir dagatals til að sneiða skýrslur                                | Dagskrá námskeiðs, þáttakendur námskeiðs |
| Fyrirtæki          | Fyrirtæki til að sía skýrsla eftir                                   | Dagskrá námskeiðs, þáttakendur námskeiðs |
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
