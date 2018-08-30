---
title: "Laun í efni Power BI"
description: "Þetta efnisatriði lýsir launum í efni Power BI. Það lýsir einnig hvernig eigi að fara í skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið."
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmCompensationWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 93c005d4b85b56f77ddd488c91e477970f4ccd07
ms.contentlocale: is-is
ms.lasthandoff: 03/26/2018

---

# <a name="compensation-power-bi-content"></a>Laun í efni Power BI

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir efninu **Laun** í Microsoft Power BI. Það lýsir einnig hvernig eigi að fara í skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið.

## <a name="accessing-the-power-bi-content"></a>Farið í Power BI-efni
Efnið **Laun** í Power BI er sýnt í vinnusvæðinu **Launastjórnun** ef þú notar eina af eftirtöldum vörum:

- Microsoft Dynamics 365 for Finance and Operations
- Microsoft Dynamics 365 for Talent

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Skýrslur sem eru hafðir með í Power BI-efni
Skýrslur sem fylgja í efni **Laun** í Power BI hafa bæði myndrit og töflur sem innihalda viðbótarupplýsingar. Eftirfarandi tafla lýsir skýrslunum.

| Skýrsla                     | Innihald |
|----------------------------|----------|
| Launayfirlit      | Yfirlit yfir aðrar skýrslur |
| Launagreining      | Starfsmenn á tímakaupi og starfsmenn á launum eftir fyrirtæki, heildarstarfsmannafjöldi eftir launafyrirkomulagi, karlkyns og kvenkyns starfsmenn eftir launafyrirkomulagi og laun starfsmanna eftir deildum. |
| Launagreining eftir stöðu      | Hæsta og lægsta tímakaup og launagreiðslur, stöður með hæstu og lægstu launin og stöður með fullu starfi og hlutastarfi |
| Greining á launafyrirkomulagi | Starfsmannaskráning eftir völdum fríðindum |

Hægt er að sía gröf og reiti í þessum skýrslum og festa gröf og reiti á yfirlitið. Nánari upplýsingar um hvernig á að sía og festa í Power BI, sjá [Stofna og Skilgreina Mælaborð](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar
Eftirfarandi gögn er notuð til að fylla út skýrslur í Power BI-efninu **Laun**. Þessi tafla sýnir einingar sem efnispakkinn var byggður á.

| Eining                   | Innihald                                                                                                   | Vensl við aðra lögaðila |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Dagsetning starfsupphafs          | Mótbókanir dagatals til að sneiða skýrslur                                                                          | Úthlutun síðustu stöðu, stöðuþróun, starfsmannaþróun, starfsmaður sem er hættur |
| Fyrirt.                    | Fyrirtæki til að sía skýrsla eftir                                                                             | Núverandi laun, núverandi starfsmaður, starfsmaður sem er hættur, starfsmannaþróun |
| Laun             | Launataxti og tíðni yfir tíma                                                                           | Núverandi laun, núverandi starfsmaður, starfsmaður sem er hættur, starfsmannaþróun |
| Núverandi laun     | Launataxti og tíðni frá og með núverandi dagsetningu                                                              | Fyrirtæki, laun, lýðfræði, starf, staða |
| Núverandi staða         | Stöður frá og með núgildandi dagsetningu, ígildi fulls starfs (FTE), opin staða og virkar-til-óvirkar stöður | Starf, staða |
| Núverandi starfsmaður         | Starfsmenn frá og með núverandi dagsetningu, aldri og starfsmannafjölda                                                         | Fyrirtæki, laun, landfræðileg staðsetning, nafn starfsmanns, heyrir undir, starfsheiti starfsmanns, lýfræði, starf, atvinna, staða, fríðindi |
| Dagsetning                     | Dagar, vikur, mánuðir og ár                                                                             | Úthlutun síðustu stöðu, stöðuþróun, starfsmaður sem er hættur, starfsmannaþróun |
| Lýðfræði             | Fæðingardagur, kyn, þjóðernisuppruni og hjúskapaarstaða                                                   | Núverandi starfsmaður, starfsmaður sem er hættur, starfsmannaþróun |
| Ráðning               | Upphafsdagur, lokadagur og breytingardagur                                                                  | Núverandi starfsmaður, starfsmaður sem er hættur, starfsmannaþróun |
| Landfræðileg staðsetning      | Borg, sýsla, póstnúmer og fylki eða Sveitarfélag                                                           | Núverandi starfsmaður, starfsmaður sem er hættur, starfsmannaþróun |
| Starf                      | Aðgerð, gerð og Titill                                                                                  | Núverandi staða, núverandi starfsmaður |
| Úthlutun síðustu stöðu | Upphafsdagur, lokadagur, breytingardagur og vinnsla                                                           | Dagsetning starfsupphafs, dagsetning, starf, staða |
| Staða                 | Deild, FTE, staða, gerð stöðu og Titill                                                        | Núverandi staða, núverandi starfsmaður |
| Stöðuþróun           | Staða yfir tími, FTE, og vinnsla                                                                          | Dagsetning starfsupphafs, dagsetning, starf, staða |
| Heyrir undir               | Fornafn, eftirnafn, og fullt nafn                                                                       | Núverandi starfskraftur, starfsmaður sem er hættur, starfsmannaþróun |
| Starfsmaður sem er hættur      | Starfsfólk sem er hætt, starfslokadagsetning, titill, staða og starf                                           | Fyrirtæki, laun, landfræðileg staðsetning, nafn starfsmanns, heyrir undir, dagsetning starfsupphafs, dagsetning, titill starfsmanns, lýðfræði, atvinna, starf, staða, fríðindi |
| Fríðindi                 | Gildisdagsetning, fríðindavalkostur, fríðindaáætlun, og fríðindi gerð                                             | Núverandi nafn, starfsmenn sem eru hættir, starfsmannaþróun |
| Nafn starfsmanns            | Fornafn, eftirnafn, og fullt nafn                                                                       | Núverandi starfsmaður, starfsmaður sem er hættur, starfsmannaþróun |
| Titill starfsmanns           | Titill og starfsaldursdagsetning                                                                                   | Núverandi starfsmaður, starfsmaður sem er hættur, starfsmannaþróun |
| Starfsmannaþróun           | Starfsfólk yfir tíma, starfsmannafjöldi, fyrirtæki og staða                                                        | Fyrirtæki, laun, landfræðileg staðsetning, nafn starfsmanns, heyrir undir, dagsetning starfsupphafs, dagsetning, titill starfsmanns, lýðfræði, atvinna, starf, fríðindi |

