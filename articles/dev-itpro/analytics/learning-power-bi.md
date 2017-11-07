---
title: "Nám - Power BI efni"
description: "Þetta efnisatriði lýsir efni í Nám - Power BI. Það lýsir einnig hvernig eigi að fara í skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið."
author: jcart1106
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Talent, Core
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0136080b12c6c2bd8e65063e99278f163212178c
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="learning-power-bi-content"></a>Nám - Power BI efni

[!include[banner](../includes/banner.md)]

Þetta efnisatriði lýsir efninu **Nám** í Microsoft Power BI. Það lýsir einnig hvernig eigi að fara í efnið og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið.

## <a name="accessing-the-power-bi-content"></a>Farið í Power BI-efni

Ef þú notar Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (júlí 2017) er hægt að finna Power BI efni um **Kennslu** í skjalasafni um samnýttar eignir í Microsoft Dynamics Lifecycle Services (LCS). Upplýsingar um hvernig á að sækja efnið og innleiða það í fyrirtæki er að finna í [Power BI-efni í LCS frá Microsoft og viðskiptaaðilum þínum](power-bi-content-microsoft-partners.md). Til að sjá sýningarmyndband um hvernig innleiða á Power BI-efnið, sjá [Power BI-efni frá Microsoft og samstarfsaðilum þínum í Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) í Office Mix.

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

Þessar einingar voru notaðar til að stofna reiknaðar mælieiningar í gagnalíkaninu. Þessar reiknuðu mælieiningar eru síðan notaðar til að reikna út afkastavísa og gera skýrslur sem eru notaðar. Eigi að framkvæma frekari útreikninga í skýrslum og mælaborði má sækja og breyta .pbix skránni úr LCS. Þessi skrá er sjálfgefið gagnalíkan sem var notað til að búa til efnið. Eftir að breytingarnar hafa verið gerðar er hægt að stofna efnispakka fyrirtækis og mælaborð sem innihalda upplýsingar sem hefur verið bætt við.

