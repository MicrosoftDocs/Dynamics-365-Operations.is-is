---
title: Ráða Power BI-efni
description: Þetta efnisatriði lýsir Power BI-efni ráðningar. Það lýsir einnig hvernig eigi að fara í skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: HcmRecruitmentWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 524b1c29d204c1b013546008b1be7868cbf8db06
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680563"
---
# <a name="recruiting-power-bi-content"></a>Ráða Power BI-efni

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir **Ráðning** Microsoft Power BI efni. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið.

## <a name="accessing-the-power-bi-content"></a>Aðgangur að Power BI efni
**Ráðning** Power BI-efni er sýnt í vinnusvæðinu **Umsjón með ráðningum**.

## <a name="reports-and-visuals-in-the-recruitment-management-workspace"></a>Skýrslur og myndræn framsetning á vinnusvæðinu Umsjón með ráðningum
Vinnusvæðið **Umsjón með ráðningum** inniheldur flipann **Greiningar**. Þessi flipi inniheldur innfellda Power BI-efnið fyrir ráðningu. Það samanstendur af yfirlitsflipa og fleiri flipum sem hafa að geyma upplýsingar. Eftirfarandi tafla lýsir skýrslunum á hverjum flipa.

| Skýrsla               | Innihald |
|----------------------|----------|
| Ráðningayfirlit | Samantekt yfir aðrar skýrslur |
| Greining umsækjanda   | Heildarfjöldi umsækjenda, umsækjendur eftir verki, kvenkyns og karlkyns umsækjendur og umsækjendur eftir staðsetningu |
| Umsækjandastaða     | Umsækjendur eftir gerð og stöðu og stöðu umsækjanda |
| Greining ráðninga  | Nettó hlutfall ráðninga, meðalfjöldi daga til að ráða, prósentuhlutfall vondra ráðninga, ráðningarkostnaður, fjöldi ráðningarverka, eftirstandandi ráðningar og umsækjendur gegn lausum störfum eftir ráðningarverki |

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar
Hægt er að sía gröf og reiti í þessum skýrslum og festa gröf og reiti á yfirlitið. Nánari upplýsingar um hvernig á að sía og festa í Power BI, sjá [Stofna og Skilgreina Mælaborð](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

Eftirfarandi tafla sýnir einingar sem **Ráðning** Power BI efni var byggt á.

| Eining               | Innihald                                                         | Vensl við aðra lögaðila |
|----------------------|------------------------------------------------------------------|-----------------------------------|
| Umsækjandi            | Umsækjendur, ráðnir, ráðningarhlutfall og kostnaður          | Nafn umsækjanda, fyrirtæki, dagsetning starfsupphafs, dagsetning, landfræðileg staðsetning, lýðfræði, starf, miðlar, ráðningarverk |
| Nafn umsækjanda       | Fornanfn umsækjanda, eftirnafn, og fullt nafn                   | Umsækjandi, ráðinn umsækjandi, umsækjandi sem er sagt upp |
| Dagsetning starfsupphafs      | Mótbókanir dagatals til að sneiða skýrslur                                | Umsækjandi, ráðinn umsækjandi, umsækjandi sem er sagt upp |
| Fyrirtæki              | Fyrirtæki til að sía skýrsla eftir                                   | Umsækjandi, ráðinn umsækjandi, umsækjandi sem er sagt upp |
| Dagsetning                 | Dagar, vikur, mánuðir og ár                                   | Umsækjandi, ráðinn umsækjandi, umsækjandi sem er sagt upp |
| Lýðfræði         | Fæðingardagur, kyn, þjóðernisuppruni og hjúskapaarstaða         | Umsækjandi, ráðinn umsækjandi, umsækjandi sem er sagt upp |
| Ráðinn umsækjandi   | Umsækjandi, frammistaða, upphafsdagur og gerð umsækjanda           | Fyrirtæki, dagsetning starfsupphafs, dagsetning, landfræðileg staðsetning, nafn umsækjanda, atvinna, afköst, starf, miðlar, ráðningarverk |
| Ráðning           | Upphafsdagur, lokadagur og breytingardagur                        | Umsækjandi, ráðinn umsækjandi, umsækjandi sem er sagt upp |
| Landfræðileg staðsetning  | Borg, sýsla, póstnúmer og fylki eða Sveitarfélag                 | Umsækjandi, ráðinn umsækjandi, umsækjandi sem er sagt upp |
| Starf                  | Aðgerð, gerð og Titill                                        | Umsækjandi, ráðinn umsækjandi, umsækjandi sem er sagt upp |
| Miðlar                | Uppruni umsækjanda                                             | Umsækjandi, ráðinn umsækjandi, umsækjandi sem er sagt upp |
| Afköst          | Mat, lýsing og matslíkan                            | Umsækjandi, ráðinn umsækjandi, umsækjandi sem er sagt upp |
| Ráðningarverk  | Lýsing á verki, staða verks og opnanir                | Umsækjandi, ráðinn umsækjandi, umsækjandi sem er sagt upp |
| Umsækjandi sem er sagt upp | Umsækendur sem var hafna, ástæða, frammistaða og starfslokadagur | Fyrirtæki, dagsetning starfsupphafs, dagsetning, landfræðileg staðsetning, afköst, lýðfræði, atvinna, miðlar, ráðningarverk, nafn umsækjanda |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]