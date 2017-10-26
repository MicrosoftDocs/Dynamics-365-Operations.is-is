---
title: "Mælikvarðar vinnuafls Power BI-efni"
description: "Þetta efnisatriði lýsir efni mælieininga vinnuafls í Power BI. Það lýsir einnig hvernig eigi að fara í skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið."
author: jcart1106
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations, Talent, Core
ms.custom: 264084
ms.assetid: 8e700583-3a7d-4f5f-9ac8-58c4feed1a02
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a5b680b406f9be3e80b43259993a3e441391ec60
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="workforce-metrics-power-bi-content"></a>Mælikvarðar vinnuafls Power BI-efni

[!include[banner](../includes/banner.md)]

Þetta efnisatriði lýsir efni **mælieininga vinnuafls** í Microsoft Power BI. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið.

## <a name="accessing-the-power-bi-content"></a>Farið í Power BI-efni
Efnið **Mælieiningar vinnuafls** í Power BI birtist í vinnusvæðinu **Starfsmannastjórnun** ef þú notar eina af þessum vörum:

- Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (júlí 2017)
- Microsoft Dynamics 365 for Talent

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mælikvarðar sem eru hafðir með í Power BI-efni
Eftirfarandi tafla sýnir mæligögn sem eru sýnd í hverri skýrslu.

| Skýrsla                                           | Einingar                                                                                                                                                                                                            |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fólksmælikvarðar                                   | Yfirlit yfir aðrar skýrslur                                                                                                                           |
| Starfsmannafjöldi eftir fyrirtæki, Deild, Staðsetning | Starfsmannafjöldi eftir fyrirtæki, starfsmannafjöldi eftir deild, starfsmannafjöldi eftir staðsetningu og heildarstarfsmannafjöldi                                                                                                                           |
| Greiningarverk starfsmannafjölda, skref, stjórnun            | Starfsmannafjöldi eftir verki, starfsmannafjöldi eftir skrefi, starfsmannafjöldi eftir stjórnanda og heildarstarfsmannafjöldi                                                                                                                                      |
| Leitnisgreining starfsmannafjölda                         | Starfsmannafjöldi þetta ár samanborið við síðasta ár eftir fyrirtæki og starfsmannavelta síðustu 12 mánaða                                                                                                                        |
| FTE-greining                                     | Heildar fullt jafngildi (FTE), heildarúthlutað FTE, FTE eftir deild, FTE síðustu 12 mánaða og FTE eftir vinnslu |
| Lýðfræði mannafla                           | Starfsmannafjöldi eftir aldri og kyni, starfsmannafjöldi eftir þjóðerni, starfsmannafjöldi eftir uppgjafahermennskustöðu, starfsmannafjöldi eftir hjúskaparstöðu, fjöldi nemenda í fullu námi, meðaltal lengdar í starfi, meðalaldur, hlutfall kvenna og karla og tungumál sem starfsmenn tala |
| Stöðugreining                                | Opnar stöður eftir deild, stöður til ráðningar, virkar-til-óvirkar stöður og stöður eftir deild                                                                                                   |
| Slitgreining                               | Slit þetta ár andstætt síðasta ári, slit, fyrirliggjandi starfsmenn eftir aldri og kyni, meðallengd starfsmanna sem hætta, starfsmenn sem fara þennan mánuð og starfsmenn sem hætta eftir ástæðu                                                                   |
| Fólk eftir deild                             | Starfsmenn með númeri starfsmanns eftir deild, stöðu og upphafs- og lokadagsetningu úthlutunar                                                                                                                       |
| Starfsaldursgreining                               | Meðaltal starfstíma, meðaltal starfsreynslu eftir fyrirtæki og starfsaldri                                                                                                                                                              |
| Starfsafmæli                           | Starfsafmæli í þessum mánuði, starfsafmæli næsta mánuð, starfsmenn eftir árum í þjónustu og starfsafmælum, ár í þjónustu með deild                                                                                                                                                                    |
| Afmæli starfsmanna                               | Afmæli í þessum mánuði, afmæli í næsta mánuði, afmælisdagar starfsmanna og afmæli eftir mánuði og deild                                                                                                                                                                    |
| Fjöldaráðningarverk                               | Heildarfjöldi fjöldaráðningar, fjöldaráðning eftir stöðu, fjöldaráðning eftir deild og eiganda, fjöldaráðningarverk eftir vinnslu og fjöldaráðningarverkum                                                                                                                                                                    |

Hægt er að sía gröf og reiti í þessum skýrslum og festa gröf og reiti á yfirlitið. Nánari upplýsingar um hvernig á að afmarka og festa í Power BI, sjá [Stofna og Skilgreina Mælaborð](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="extending-the-power-bi-content"></a>Stækkun efnis Power BI
Með því að nota þjónustupakka sem eru í boði í Microsoft Dynamics Lifecycle Services (LCS) er hægt að veita fólki sem skráir sig ekki inn í Finance and Operations öflugri greiningu. Hægt er að breyta þessum þjónustupökkum þannig að þeir innihaldi skýrslur eða myndræna framsetningu og afhenda svo leigjanda Power BI.com þjónustupakkana.

Hægt er að finna efni **Mælieiningar vinnuafls** í Power BI í safninu Samnýttar eignir í LCS. Upplýsingar um hvernig á að sækja efnið og innleiða það í fyrirtæki er að finna í [Power BI-efni í LCS frá Microsoft og viðskiptaaðilum þínum](power-bi-content-microsoft-partners.md). Til að sjá sýningarmyndband um hvernig innleiða á Power BI-efnið, sjá [Power BI-efni frá Microsoft og samstarfsaðilum þínum í Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) í Office Mix.

Gangið úr skugga um að hlaða niður efninu **Mælieiningar vinnuafls** í Power BI sem á við um útgáfu Microsoft Dynamics 365 sem verið er að nota.

>[!NOTE]
>Þær .pbix skrár sem eru tiltækar í Lifecycle Services eiga aðeins við um Finance and Operations.

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar
Eftirfarandi tafla sýnir einingar sem efnið var byggt á.

| Eining                   | Innihald                                                                            | Vensl við aðra lögaðila |
|--------------------------|-------------------------------------------------------------------------------------|-----------------------------------|
| Dagsetning starfsupphafs          | Mótbókanir dagatals til að sneiða skýrslur                                                   | Úthlutun síðustu stöðu, stöðuþróun, starfsmannaþróun, starfsmaður sem er hættur |
| Fyrirt.                    | Fyrirtæki til að sía skýrsla eftir                                                      | Núverandi starfsmaður, starfsmaður sem er hættur, starfsmannaþróun |
| Núverandi staða         | Stöður frá og með núgildandi dagsetningu, ígildi fulls starfs (FTE), opin staða og virkar-til-óvirkar stöður | Starf, staða |
| Núverandi starfsmaður         | Starfsmenn frá og með núverandi dagsetningu, aldri og starfsmannafjölda                                  | Fyrirtæki, landfræðileg staðsetning, nafn starfsmanns, heyrir undir, starfsheiti starfsmanns, lýfræði, starf, atvinna, staða |
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

Þessar einingar voru notaðar til að stofna reiknaðar mælieiningar í gagnalíkaninu. Þessar reiknuðu mælieiningar eru síðan notaðar til að stofna reiknaðar ráðstafanir til að reikna út afkastavísa (KPI ) og skýrslur sem eru notaðar í efnispakka Power BI. Eigi að framkvæma frekari útreikninga í skýrslum og mælaborði má sækja og breyta .pbix skránni úr LCS. Þessi skrá er sjálfgefið gagnalíkan sem var notað til að stofna efnispakka Power BI. Eftir að breytingarnar hafa verið gerðar er hægt að stofna efnispakka fyrirtækis og mælaborð sem innihalda upplýsingar sem hefur verið bætt við.
