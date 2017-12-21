---
title: Efni Benefits Power BI
description: "Þetta efnisatriði lýsir efni Benefits Power BI. Það lýsir hvernig eigi að fara í skýrslur sem fylgja og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið."
author: jcart1106
manager: AnnBe
ms.date: 12/01/2017
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
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: 25111ac7ae07e04bc81ac23a348464bcbe1393af
ms.contentlocale: is-is
ms.lasthandoff: 12/01/2017

---

# <a name="benefits-power-bi-content"></a>Efni Benefits Power BI

[!include[banner](../includes/banner.md)]

Þetta efnisatriði lýsir efni **Benefits** Microsoft Power BI. Það lýsir hvernig eigi að fara í skýrslur sem fylgja og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið.

## <a name="accessing-the-power-bi-content"></a>Farið í Power BI-efni
Efni **Fríðindi** Power BI er sýnt í vinnusvæðinu **Fríðindastjórnun** ef þú notar eina af eftirtöldum vörum:

- Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition
- Microsoft Dynamics 365 for Talent

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Skýrslur sem eru hafðir með í Power BI-efni
Skýrslur sem fylgja í efni **Benefits** Power BI hafa bæði myndrit og töflur sem innihalda viðbótarupplýsingar. Eftirfarandi tafla lýsir skýrslunum.

| Skýrsla                       | Innihald                                                                                       |
|------------------------------|------------------------------------------------------------------------------------------------|
| Yfirlit yfir fríðindaskráningu  | Mest og minnst notaðar áætlanir, skráning eftir starfsmannahópnum og valdir möguleikar fríðindaáætlana. |
| Fríðindi starfsmanna            | Starfsmannaskráning eftir völdum fríðindum                                                        |
                                                                                             
Hægt er að sía gröf og reiti í þessum skýrslum og festa gröf og reiti á yfirlitið. Nánari upplýsingar um hvernig á að sía og festa í Power BI, sjá [Stofna og Skilgreina Mælaborð](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="extending-the-power-bi-content"></a>Stækkun efnis Power BI
Með því að nota þjónustupakka sem eru í boði í Microsoft Dynamics Lifecycle Services (LCS) er hægt að veita fólki sem skráir sig ekki inn í Finance and Operations öflugri greiningu. Hægt er að breyta þessum þjónustupökkum þannig að þeir innihaldi skýrslur eða myndræna framsetningu og afhenda svo leigjanda Power BI.com þjónustupakkana.

Hægt er að finna efni **Benefits** Power BI í safninu Samnýttar eignir í LCS. Upplýsingar um hvernig á að sækja efnið og innleiða það í fyrirtæki er að finna í [Power BI-efni í LCS frá Microsoft og viðskiptaaðilum þínum](power-bi-content-microsoft-partners.md). Til að sjá sýningarmyndband um hvernig innleiða á Power BI-efnið, sjá [Power BI-efni frá Microsoft og samstarfsaðilum þínum í Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) í Office Mix.

>[!NOTE]
>Þær .pbix skrár sem eru tiltækar í Lifecycle Services eiga aðeins við um Finance and Operations.

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar
Eftirfarandi gögn er notuð til að fylla út skýrslur í Power BI-efninu **Fríðindi**. Þessi tafla sýnir einingar sem efnispakkinn var byggður á.

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

Þessar einingar voru notaðar til að stofna reiknaðar mælieiningar í gagnalíkaninu. Þessar reiknuðu mælieiningar eru síðan notaðar til að reikna út afkastavísa og gera skýrslur sem eru notaðar. Eigi að framkvæma frekari útreikninga í skýrslum og mælaborði má sækja og breyta .pbix skránni úr LCS. Þessi skrá er sjálfgefið gagnalíkan sem var notað til að búa til efnið. Eftir að breytingarnar hafa verið gerðar er hægt að stofna efnispakka fyrirtækis og mælaborð sem innihalda upplýsingar sem hefur verið bætt við.

