---
title: "Ráða Power BI-efni"
description: "Þetta efnisatriði lýsir ráðningum í Power BI. Það lýsir einnig hvernig eigi að fara í skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið."
author: jcart1106
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a02dab349da0709b8d9250dba0a2ca1e03b6a527
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="recruiting-power-bi-content"></a>Ráða Power BI-efni

[!include[banner](../includes/banner.md)]

Þetta efnisatriði lýsir efninu **Ráðningar** í Microsoft Power BI. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið.

## <a name="accessing-the-power-bi-content"></a>Farið í Power BI-efni
Ef þú notar Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (júlí 2017) er **Ráðning** Power BI efni sýnt í vinnusvæðinu **Umsjón með ráðningum**. 

## <a name="reports-and-visuals-in-the-recruitment-management-workspace"></a>Skýrslur og myndræn framsetning á vinnusvæðinu Umsjón með ráðningum
**Umsjón með ráðningum** inniheldur **Greiningar**-flipa. Þessi flipi inniheldur innfellda Power BI-efnið fyrir mannaráðningar. Það samanstendur af yfirlitsflipa og fleiri flipum sem hafa að geyma upplýsingar. Eftirfarandi tafla lýsir skýrslunum á hverjum flipa.

| Skýrsla               | Innihald |
|----------------------|----------|
| Ráðningayfirlit | Samantekt yfir aðrar skýrslur |
| Greining umsækjanda   | Heildarfjöldi umsækjenda, umsækjendur eftir verki, kvenkyns og karlkyns umsækjendur og umsækjendur eftir staðsetningu |
| Umsækjandastaða     | Umsækjendur eftir gerð og stöðu og stöðu umsækjanda |
| Greining ráðninga  | Nettó hlutfall ráðninga, meðalfjöldi daga til að ráða, prósentuhlutfall vondra ráðninga, ráðningarkostnaður, fjöldi ráðningarverka, eftirstandandi ráðningar og umsækjendur gegn lausum störfum eftir ráðningarverki |

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar
Hægt er að sía gröf og reiti í þessum skýrslum og festa gröf og reiti á yfirlitið. Nánari upplýsingar um hvernig á að sía og festa í Power BI, sjá [Stofna og Skilgreina Mælaborð](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

Eftirfarandi tafla sýnir þær einingar sem Power BI efnið **Ráðningar** var byggt á.

| Eining               | Innihald                                                         | Vensl við aðra lögaðila |
|----------------------|------------------------------------------------------------------|-----------------------------------|
| Umsækjandi            | Umsækjendur, ráðnir, ráðningarhlutfall og kostnaður          | Nafn umsækjanda, fyrirtæki, dagsetning starfsupphafs, dagsetning, landfræðileg staðsetning, lýðfræði, starf, miðlar, ráðningarverk |
| Nafn umsækjanda       | Fornanfn umsækjanda, eftirnafn, og fullt nafn                   | Umsækjandi, ráðinn umsækjandi, umsækjandi sem er sagt upp |
| Dagsetning starfsupphafs      | Mótbókanir dagatals til að sneiða skýrslur                                | Umsækjandi, ráðinn umsækjandi, umsækjandi sem er sagt upp |
| Fyrirt.                | Fyrirtæki til að sía skýrsla eftir                                   | Umsækjandi, ráðinn umsækjandi, umsækjandi sem er sagt upp |
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

Þessar einingar voru notaðar til að stofna reiknaðar mælieiningar. Þessar reiknuðu mælieiningar eru síðan notaðar til að reikna út afkastavísa og gera skýrslur sem eru notaðar. Viljir þú hafa fleiri útreikninga í skýrslum og mælaborði getur þú sótt og breytt Recruiting.pbix skránni í Microsoft Dynamics Lifecycle Services (LCS). Þessi skrá er sjálfgefið gagnalíkan sem var notað til að búa til efnið. Eftir að breytingarnar hafa verið gerðar er hægt að stofna efnispakka fyrirtækis og mælaborð sem innihalda upplýsingar sem hefur verið bætt við.
