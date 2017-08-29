---
title: "Þróun starfsmanns efni Power BI"
description: "Þetta efnisatriði lýsir efni þróunar starfsmanns í Power BI. Það lýsir einnig hvernig eigi að fara í skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið."
author: jcart1106
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations, Talent, Core
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: d25f3be5821a02ea618a2356878bf2904765a6f7
ms.contentlocale: is-is
ms.lasthandoff: 06/13/2017

---

# <a name="employee-development-power-bi-content"></a>Þróun starfsmanns efni Power BI

[!include[banner](../includes/banner.md)]

Þetta efnisatriði lýsir efni **þróunar starfsmanns** í Microsoft Power BI. Það lýsir einnig hvernig eigi að fara í skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið.

## <a name="accessing-the-power-bi-content"></a>Farið í Power BI-efni

Ef verið er að nota Microsoft Dynamics 365 for Finance and Operations, Enterprise útgáfu með uppfærslu í júlí 2017, er hægt að finna efnispakkann **Þróun starfsmanns** í Power BI í safninu Samnýttar eignir Shared í Microsoft Dynamics Lifecycle Services (LCS). Upplýsingar um hvernig á að sækja efnispakkann og tengja hann við gögnin er að finna í [Power BI-efni í LCS frá Microsoft og viðskiptaaðilum þínum](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Skýrslur sem eru hafðir með í Power BI-efni
Skýrslur sem fylgja í efni **Þróun starfsmanns** í Power BI hafa bæði myndrit og töflur sem innihalda viðbótarupplýsingar. Eftirfarandi tafla lýsir skýrslunum.

| Skýrsla                        | Innihald |
|-------------------------------|----------|
| Yfyrilit yfir þróun starfsmanns | Yfirlit yfir aðrar skýrslur |
| Hæfnigreining starfsmanns       | Hæfnisgerðir starfsmanna og hæfni starfsmanns eftir gerð |
| Hæfnigreiningarstig starfsmanns | Hæfnistig starfsmanns eftir deild, starfsmenn eftir gerð hæfni og lægsta og hæsta stig eftir hæfni |
| Hæfniyfirlit                 | Hæfniyfirlit fyrir valinn starfsmann |
| Hæfnigreining                | Hæfni eftir gerð og einkunn |
| Greining á hæfnimati   | Starfsmenn eftir lægstu og hæstu einkunn eftir starfi, einkunnir starfsmanns eftir deild, starfsmenn eftir einkunn og gerð stöðu hæstu og lægstu einkunnir eftir stöðu  |
| Greining á starfsmannaárangri | Starfsmannaeinkunn fyrir valdan einkunn eftir stjórnendum |

Hægt er að sía gröf og reiti í þessum skýrslum og festa gröf og reiti á yfirlitið. Nánari upplýsingar um hvernig á að sía og festa í Power BI, sjá [Stofna og Skilgreina Mælaborð](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar
| Eining                   | Innihald                                                                                                   | Vensl við aðra lögaðila |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Dagsetning starfsupphafs          | Mótbókanir dagatals til að sneiða skýrslur                                                                          | Úthlutun síðustu stöðu, stöðuþróun, starfsmannaþróun, starfsmaður sem er hættur 
| Fyrirt.                    | Fyrirtæki til að sía skýrsla eftir                                                                             | Núverandi starfsmaður, starfsmaður sem er hættur, starfsmannaþróun |
| Núverandi staða         | Stöður frá og með núgildandi dagsetningu, ígildi fulls starfs (FTE), opin staða og virkar-til-óvirkar stöður | Starf, staða |
| Núverandi starfsmaður         | Starfsmenn frá og með núverandi dagsetningu, aldri og starfsmannafjölda                                                         | Fyrirtæki, landfræðileg staðsetning, nafn starfsmanns, heyrir undir, starfsheiti starfsmanns, lýfræði, starf, atvinna, staða |
| Dagsetning                     | Dagar, vikur, mánuðir og ár                                                                             | Úthlutun síðustu stöðu, stöðuþróun, starfsmaður sem er hættur, starfsmannaþróun |
| Lýðfræði             | Fæðingardagur, kyn, þjóðernisuppruni og hjúskapaarstaða                                                   | Núverandi starfsmaður, starfsmaður sem er hættur, starfsmannaþróun |
| Ráðning               | Upphafsdagur, lokadagur og breytingardagur                                                                  | Núverandi starfsmaður, starfsmaður sem er hættur, starfsmannaþróun |
| Landfræðileg staðsetning      | Borg, sýsla, póstnúmer og fylki eða Sveitarfélag                                                           | Núverandi starfsmaður, starfsmaður sem er hættur, starfsmannaþróun |
| Starf                      | Aðgerð, gerð og Titill                                                                                  | Núverandi staða, núverandi starfsmaður |
| Úthlutun síðustu stöðu | Upphafsdagur, lokadagur, breytingardagur og vinnsla                                                           | Dagsetning starfsupphafs, dagsetning, starf, staða |
| Staða                 | Deild, FTE, staða, gerð stöðu og Titill                                                        | Núverandi staða, núverandi starfsmaður |
| Stöðuþróun           | Staða yfir tími, FTE, og vinnsla                                                                          | Dagsetning starfsupphafs, dagsetning, starf, staða |
| Heyrir undir               | Fornafn, eftirnafn, og fullt nafn                                                                       | Núverandi starfsmaður, starfsmaður sem er hættur, starfsmannaþróun |
| Starfsmaður sem er hættur      | Starfsfólk sem er hætt, starfslokadagsetning, Titill, staða, og starf                                             | Fyrirtæki, landfræðileg staðsetning, nafn starfsmanns, heyrir undir, dagsetning starfsupphafs, dagsetning, titill starfsmanns, lýðfræði, atvinna, starf, staða |
| Nafn starfsmanns            | Fornafn, eftirnafn, og fullt nafn                                                                       | Núverandi starfskraftur, starfsmaður sem er hættur, starfsmannaþróun |
| Titill starfsmanns           | Titill og starfsaldursdagsetning                                                                                   | Núverandi starfsmaður, starfsmaður sem er hættur, starfsmannaþróun |
| Starfsmannaþróun           | Starfsfólk yfir tíma, starfsmannafjöldi, fyrirtæki og staða                                                        | Fyrirtæki, landfræðileg staðsetning, nafn starfsmanns, heyrir undir, dagsetning starfsupphafs, dagsetning, titill starfsmanns, lýðfræði, atvinna, starf |
| Starf                      | Aðgerð, gerð og Titill                                                                                      | Núverandi starfsmaður, núverandi staða, starfsmannaleitni, æskileg hæfni starfs, fyrri stöðuúthlutun, stöðuleitni starfsmaður sem er hættur |
| Hæfni fyrir útvalið verk      | Mikilvægi, einkunn, hæfni og hæfnisstig                                                                 | Starf |
| Hæfnigreining starfsmanns  | Vottun, stig, dagsetning stigs og hæfni                                                                    | Nafn starfsmanns, hæfni |  
| Afköst              | Mat, lýsing og matslíkan                                                                      | Núverandi starfsmaður, núverandi staða, starfsmannaleitni, æskileg hæfni starfs, fyrri stöðuúthlutun, stöðuleitni starfsmaður sem er hættur |
|  Hæfni                   | Hæfni, gerð hæfni og mat                                                                              | Hæfnigreining starfsmanns, æskileg hæfni starfs |                                                                                                                        

Þessar einingar voru notaðar til að stofna reiknaðar mælieiningar í gagnalíkaninu. Þessar reiknuðu mælieiningar eru síðan notaðar til að stofna reiknaðar ráðstafanir til að reikna út afkastavísa (KPI ) og skýrslur sem eru notaðar í efnispakka Power BI. Eigi að framkvæma frekari útreikninga í skýrslum og mælaborði má sækja og breyta .pbix skránni úr LCS. Þessi skrá er sjálfgefið gagnalíkan sem var notað til að stofna efnispakka Power BI. Eftir að breytingarnar hafa verið gerðar er hægt að stofna efnispakka fyrirtækis og mælaborð sem innihalda upplýsingar sem hefur verið bætt við.

