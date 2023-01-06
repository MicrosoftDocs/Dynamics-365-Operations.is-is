---
title: Mælikvarðar vinnuafls Power BI efni
description: Þessi grein lýsir Mælikvarðar vinnuafls Power BI efni.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 264084
ms.assetid: 8e700583-3a7d-4f5f-9ac8-58c4feed1a02
ms.search.form: HcmWorkforceWorkspace
ms.openlocfilehash: 9d5c156eda3559394cb2723f0492b0ab575d815d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289817"
---
# <a name="workforce-metrics-power-bi-content"></a>Mælikvarðar vinnuafls Power BI efni

[!include [banner](../includes/banner.md)]

Þessi grein lýsir **Mælikvarðar vinnuafls** Microsoft Power BI efni. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið.

## <a name="accessing-the-power-bi-content"></a>Aðgangur að Power BI efni
**Mælikvarðar vinnuafls** Power BI efni birtist á vinnusvæðinu **Starfsmannastjórnun** ef þú notar eina af þessum vörum:

- Microsoft Dynamics 365 Finance
- Microsoft Dynamics 365 Human Resources

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mælikvarðar sem eru hafðir með í Power BI efni
Eftirfarandi tafla sýnir mæligögn sem eru sýnd í hverri skýrslu.

| Skýrsla                                           | Einingar |
|--------------------------------------------------|---------|
| Fólksmælikvarðar                                   | Yfirlit yfir aðrar skýrslur |
| Starfsmannafjöldi eftir fyrirtæki, Deild, Staðsetning | Starfsmannafjöldi eftir fyrirtæki, starfsmannafjöldi eftir deild, starfsmannafjöldi eftir staðsetningu og heildarstarfsmannafjöldi |
| Greiningarverk starfsmannafjölda, skref, stjórnun            | Starfsmannafjöldi eftir verki, starfsmannafjöldi eftir skrefi, starfsmannafjöldi eftir stjórnanda og heildarstarfsmannafjöldi |
| Leitnisgreining starfsmannafjölda                         | Starfsmannafjöldi þetta ár samanborið við síðasta ár eftir fyrirtæki og starfsmannavelta síðustu 12 mánaða |
| FTE-greining                                     | Heildar fullt jafngildi (FTE), heildarúthlutað FTE, FTE eftir deild, FTE síðustu 12 mánaða og FTE eftir vinnslu |
| Lýðfræði mannafla                           | Starfsmannafjöldi eftir aldri og kyni, starfsmannafjöldi eftir þjóðerni, starfsmannafjöldi eftir uppgjafahermennskustöðu, starfsmannafjöldi eftir hjúskaparstöðu, fjöldi nemenda í fullu námi, meðaltal lengdar í starfi, meðalaldur, hlutfall kvenna og karla og tungumál sem starfsmenn tala |
| Stöðugreining                                | Opnar stöður eftir deild, stöður til ráðningar, virkar-til-óvirkar stöður og stöður eftir deild |
| Slitgreining                               | Slit þetta ár andstætt síðasta ári, slit, fyrirliggjandi starfsmenn eftir aldri og kyni, meðallengd starfsmanna sem hætta, starfsmenn sem fara þennan mánuð og starfsmenn sem hætta eftir ástæðu |
| Fólk eftir deild                             | Starfsmenn með númeri starfsmanns eftir deild, stöðu og upphafs- og lokadagsetningu úthlutunar |
| Starfsaldursgreining                               | Meðaltal starfstíma, meðaltal starfsreynslu eftir fyrirtæki og starfsaldri |
| Starfsafmæli                           | Starfsafmæli í þessum mánuði, starfsafmæli næsta mánuð, starfsmenn eftir árum í þjónustu og starfsafmælum, ár í þjónustu með deild |
| Afmæli starfsmanna                               | Afmæli í þessum mánuði, afmæli í næsta mánuði, afmælisdagar starfsmanna og afmæli eftir mánuði og deild |
| Fjöldaráðningarverk                               | Heildarfjöldi fjöldaráðningar, fjöldaráðning eftir stöðu, fjöldaráðning eftir deild og eiganda, fjöldaráðningarverk eftir vinnslu og fjöldaráðningarverkum |

Hægt er að sía gröf og reiti í þessum skýrslum og festa gröf og reiti á yfirlitið. Nánari upplýsingar um hvernig á að sía og festa í Power BI, sjá [Stofna og Skilgreina Mælaborð](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

Vertu viss um að hlaða niður Power BI-efninu **Mælikvarðar vinnuafls** sem á við um útgáfuna á Microsoft Dynamics 365 sem verið er að nota.

> [!NOTE]
> Þær .pbix skrár sem eru tiltækar í Lifecycle Services eiga aðeins við um forrit fjármála- og reksturs.

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar
Eftirfarandi tafla sýnir einingar sem efnið var byggt á.

| Eining                   | Innihald                                                                            | Vensl við aðra lögaðila |
|--------------------------|-------------------------------------------------------------------------------------|-----------------------------------|
| Dagsetning starfsupphafs          | Mótbókanir dagatals til að sneiða skýrslur                                                   | Úthlutun síðustu stöðu, stöðuþróun, starfsmannaþróun, starfsmaður sem er hættur |
| Fyrirt.                  | Fyrirtæki til að sía skýrsla eftir                                                      | Núverandi starfsmaður, starfsmaður sem er hættur, starfsmannaþróun |
| Núverandi staða         | Stöður frá og með núgildandi dagsetningu, ígildi fulls starfs (FTE), opin staða og virkar-til-óvirkar stöður | Starf, staða |
| Núverandi starfsmaður         | Starfsmenn frá og með núverandi dagsetningu, aldri og starfsmannafjölda                                  | Fyrirtæki, Landfræðileg staðsetning, Nafn starfsmanns, Skýrslur til, Titill starfsmanns, Lýðfræði, Starf, Atvinna, Staða |
| Dagsetning                     | Dagar, vikur, mánuðir og ár                                                      | Úthlutun síðustu stöðu, stöðuþróun, starfsmaður sem er hættur, starfsmannaþróun |
| Lýðfræði             | Fæðingardagur, kyn, þjóðernisuppruni og hjúskapaarstaða                            | Núverandi starfsmaður, starfsmaður sem er hættur, starfsmannaþróun |
| Ráðning               | Upphafsdagur, lokadagur og breytingardagur                                           | Núverandi starfsmaður, starfsmaður sem er hættur, starfsmannaþróun |
| Landfræðileg staðsetning      | Borg, sýsla, póstnúmer og fylki eða Sveitarfélag                                    | Núverandi starfsmaður, starfsmaður sem er hættur, starfsmannaþróun |
| Starf                      | Aðgerð, gerð og Titill                                                           | Núverandi staða, núverandi starfsmaður |
| Úthlutun síðustu stöðu | Upphafsdagur, lokadagur, breytingardagur og vinnsla                                    | Dagsetning starfsupphafs, dagsetning, starf, staða |
| Staða                 | Deild, FTE, staða, gerð stöðu og Titill                                 | Núverandi staða, núverandi starfsmaður |
| Stöðuþróun           | Staða yfir tími, FTE, og vinnsla                                                   | Dagsetning starfsupphafs, dagsetning, starf, staða |
| Heyrir undir               | Fornafn, eftirnafn, og fullt nafn                                                | Núverandi starfsmaður, starfsmaður sem er hættur, starfsmannaþróun |
| Starfsmaður sem er hættur      | Starfsfólk sem er hætt, starfslokadagsetning, Titill, staða, og starf                      | Fyrirtæki, landfræðileg staðsetning, nafn starfsmanns, heyrir undir, dagsetning starfsupphafs, dagsetning, titill starfsmanns, lýðfræði, atvinna, starf, staða |
| Nafn starfsmanns            | Fornafn, eftirnafn, og fullt nafn                                                | Núverandi starfskraftur, starfsmaður sem er hættur, starfsmannaþróun |
| Titill starfsmanns           | Titill og starfsaldursdagsetning                                                            | Núverandi starfsmaður, starfsmaður sem er hættur, starfsmannaþróun |
| Starfsmannaþróun           | Starfsfólk yfir tíma, starfsmannafjöldi, fyrirtæki og staða                                 | Fyrirtæki, landfræðileg staðsetning, nafn starfsmanns, heyrir undir, dagsetning starfsupphafs, dagsetning, titill starfsmanns, lýðfræði, atvinna, starf |
| Fjöldaráðningarverk        | Fjöldi fjöldaráðningaverka, eigandi verks og staða verks                     | Fyrirtæki, fjöldaráðningarlína |
| Fjöldaráðningarlína           | Deild, starfsheiti og staða                                           | Dagsetning, starf, fjöldaráðningarverk |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
