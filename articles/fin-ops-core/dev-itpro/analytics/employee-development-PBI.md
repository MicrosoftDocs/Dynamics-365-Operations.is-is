---
title: Starfsmannaþróun Power BI efni
description: Þessi grein lýsir þróun starfsmanna Power BI efni.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 67fd3b5907cb52dc1f10d754e12316e21876e888
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850988"
---
# <a name="employee-development-power-bi-content"></a>Starfsmannaþróun Power BI efni

[!include [banner](../includes/banner.md)]

Þessi grein lýsir **Þróun starfsmanna** Microsoft Power BI efni.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Skýrslur sem eru hafðar með í Power BI efni
Skýrslur sem eru hafðar með í **Starfsmannaþróun** Power BI efni hafa bæði gröf og töflur sem innihalda viðbótarupplýsingar. Eftirfarandi tafla lýsir skýrslunum.

| Skýrsla                        | Innihald |
|-------------------------------|----------|
| Yfyrilit yfir þróun starfsmanns | Yfirlit yfir aðrar skýrslur |
| Hæfnigreining starfsmanns       | Hæfnisgerðir starfsmanna og hæfni starfsmanns eftir gerð |
| Hæfnigreiningarstig starfsmanns | Hæfnistig starfsmanns eftir deild, starfsmenn eftir gerð hæfni og lægsta og hæsta stig eftir hæfni |
| Hæfniyfirlit                 | Hæfniyfirlit fyrir valinn starfsmann |
| Hæfnigreining                | Hæfni eftir gerð og einkunn |
| Greining á hæfnimati   | Starfsmenn eftir lægstu og hæstu einkunn eftir starfi, einkunnir starfsmanns eftir deild, starfsmenn eftir einkunn og gerð stöðu hæstu og lægstu einkunnir eftir stöðu |
| Greining á starfsmannaárangri | Starfsmannaeinkunn fyrir valdan einkunn eftir stjórnendum |

Hægt er að sía gröf og reiti í þessum skýrslum og festa gröf og reiti á yfirlitið. Nánari upplýsingar um hvernig á að sía og festa í Power BI, sjá [Stofna og Skilgreina Mælaborð](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar

| Eining                   | Innihald                                                                                                   | Vensl við aðra lögaðila |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Dagsetning starfsupphafs          | Mótbókanir dagatals til að sneiða skýrslur                                                                          | Úthlutun síðustu stöðu, stöðuþróun, starfsmannaþróun, starfsmaður sem er hættur |
| Fyrirt.                  | Fyrirtæki til að sía skýrsla eftir                                                                             | Núverandi starfsmaður, starfsmaður sem er hættur, starfsmannaþróun |
| Núverandi staða         | Stöður frá og með núgildandi dagsetningu, ígildi fulls starfs (FTE), opin staða og virkar-til-óvirkar stöður | Starf, staða |
| Núverandi starfsmaður         | Starfsmenn frá og með núverandi dagsetningu, aldri og starfsmannafjölda                                                         | Fyrirtæki, Landfræðileg staðsetning, Nafn starfsmanns, Skýrslur til, Titill starfsmanns, Lýðfræði, Starf, Atvinna, Staða |
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
| Starf                      | Aðgerð, gerð og Titill                                                                                  | Núverandi starfsmaður, núverandi staða, starfsmannaleitni, æskileg hæfni starfs, fyrri stöðuúthlutun, stöðuleitni starfsmaður sem er hættur |
| Hæfni fyrir útvalið verk      | Mikilvægi, einkunn, hæfni og hæfnisstig                                                                 | Starf |
| Hæfnigreining starfsmanns  | Vottun, stig, dagsetning stigs og hæfni                                                                    | Nafn starfsmanns, hæfni |
| Afköst              | Mat, lýsing og matslíkan                                                                      | Núverandi starfsmaður, núverandi staða, starfsmannaleitni, æskileg hæfni starfs, fyrri stöðuúthlutun, stöðuleitni starfsmaður sem er hættur |
| Hæfni                    | Hæfni, gerð hæfni og mat                                                                              | Hæfnigreining starfsmanns, æskileg hæfni starfs |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]