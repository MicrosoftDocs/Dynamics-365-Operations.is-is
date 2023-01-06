---
title: Samruni virðislíkön eigna og afskriftarbækur
description: Í eldri útgáfum, voru tvö matshugtök fyrir eignir - virðislíkön og afskriftabækur. Í Microsoft Dynamics 365 for Operations (1611) útgáfu, er virkni fyrir virðislíkön og afskriftarbókar sameinaðar í eitt hugtak sem kallast bók.
author: moaamer
ms.date: 10/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 221564
ms.assetid: 7c68eb7c-8b1a-4dd9-afb8-04b4040e305e
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f4f06b7916fb2eeed802b2dce95edfce448dcd97
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880846"
---
# <a name="fixed-asset-value-model-and-depreciation-book-merge"></a>Sameining virðislíkana eigna og afskriftarbókar

[!include [banner](../includes/banner.md)]

Þessi grein lýsir núverandi virkni bókar í eignum. Þessi virkni er byggð á virkni virðislíkans sem var í boði í fyrri útgáfum, en inniheldur einnig alla virknina sem var áður fyrr einungis til staðar í afskriftarbókum.

Virkni bókar gerir þér kleift að nota eitt sett af síðum, fyrirspurnum og skýrslum fyrir alla ferla eignar í fyrirtækinu. Töflurnar í þessari grein lýsa fyrri virkni fyrir afskriftabækur og virðislíkön saman með núverandi virkni fyrir bækur.

## <a name="setup"></a>Uppsetning
Sjálfgefið er að bækur bóka bæði í fjárhag (GL) og undirbók eignar. Bækur hafa nýja **Bóka í fjárhag** valkost sem gerir kleift að gera bókun á Fjárhag óvirka og bóka aðeins í undirbók eignar. Þessi virkni svipar fyrri hegðun bókana fyrir afskriftabækur. Uppsetning heiti færslubóka hefur nýja bókunarlag sem nefnist Ekkert. Þessi bókunarlag var bætt sérstaklega við fyrir eignafærslur. Til að bóka færslur fyrir bækur sem ekki bóka í fjárhag, verður að nota heiti færslubókar sem er með bókunarlag stillt á **Ekkert**.


| &nbsp;                                           | Afskriftabók               | Virðislíkan                     | Bók (Nýtt)                                              |
|--------------------------------------------------|---------------------------------|---------------------------------|---------------------------------------------------------|
| Bóka í fjárhag                                   | Aldrei                           | Alltaf                          | Valkostur að bóka í fjárhag                                |
| Bókunarlög                                   | Á ekki við                  | 3: Núgildandi, aðgerðir, og skattur | 11: núgildandi, Aðgerðir, Skatt, 7 sérsniðna lögum og Ekkert |
| Færslubókanöfn                                    | Færslubókarheiti afskriftarbókar | Fjárhagur - Færslubókaheiti              | Fjárhagur - Færslubókaheiti                                      |
| Afleiddar bækur                                    | Ekki leyfð                     | Leyfð                         | Leyfð                                                 |
| Hnekking afskriftarreglu á stigi eignar | Leyfð                         | Ekki leyfð                     | Leyfð                                                 |

## <a name="processes"></a>Ferli
Ferli nota nú almenna síðuna. Sum ferla eru eingöngu leyfð ef **Bóka í fjárhag** valkostur er stilltur á **Nei** í uppsetningu bókar.

| &nbsp;                                           | Afskriftabók               | Virðislíkan                     | Bók (Nýtt)                                              |
|--------------------------------|---------------------------|---------------------|------------------------------------------|
| Innsláttur færslu              | Færslubók afskriftabókar | Eignabók | Eignabók                      |
| Viðbótarafskriftir             | Leyfð                   | Ekki leyft         | Leyfð                                  |
| Eyða sögulegum færslum | Leyfð                   | Ekki leyft         | Leyft, nema verið sé að bóka í Fjárhags |
| Fjöldauppfærsla                    | Leyfð                   | Ekki leyft         | Leyft, nema verið sé að bóka í Fjárhags |

## <a name="inquiries-and-reports"></a>Fyrirspurnir og skýrslur
Fyrirspurnir og skýrslur styðja allar bækurnar . Skýrslur sem ekki með í eftirfarandi töflu studdu áður bæði afskriftarbækur og virðislíkön, og munu núna halda áfram til að styðja allar gerðir bóka. **Bókunarlag** svæði hefur einnig verið bætt við skýrslur, þannig að auðveldara er að bera kennst á færslubókanir.

| &nbsp;                                           | Afskriftabók               | Virðislíkan                     | Bók (Nýtt)                                              |
|---------------------------------------|--------------------------------|--------------------------|--------------------------|
| Fyrirspurnir                             | Afskriftabókarfærslur | Eignafærslur | Eignafærslur |
| Eignayfirlit                 | Ekki leyfð                    | Leyfð                  | Leyfð                  |
| Eignagrunnur                     | Leyfð                        | Ekki leyfð              | Leyfð                  |
| Hæfi eignar á miðjum fjórðungi | Leyfð                        | Ekki leyfð              | Leyfð                  |

## <a name="upgrade"></a>Uppfæra
Uppfærsluferlið færir fyrirliggjandi uppsetningu og allar fyrirliggjandi færslur til uppbyggingar nýju bókarinnar. Virðislíkön haldast eins og þau eru, sem bók sem bókar í fjárhag. Hins vegar verða afskriftabækur flutt í bók sem hefur **Bóka í fjárhag** valkostur stilltur á **Nei**. Færslubókaheiti afskriftabóka verði flutt í færslubókarheitið fjárhags sem er með bókunarlag stillt á **Ekkert**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
