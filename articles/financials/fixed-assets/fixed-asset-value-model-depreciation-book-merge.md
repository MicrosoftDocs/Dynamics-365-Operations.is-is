---
title: "Samruni virðislíkön eigna og afskriftarbækur"
description: "Í eldri útgáfum, voru tvö matshugtök fyrir eignir -  virðislíkön og afskriftabækur. Í Microsoft Dynamics 365 for Operations (1611) útgáfu, er virkni fyrir virðislíkön og afskriftarbókar sameinaðar í eitt hugtak sem kallast bók."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221564
ms.assetid: 7c68eb7c-8b1a-4dd9-afb8-04b4040e305e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7a5f833fd7a897d00f8232873c81736a8de65812
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="fixed-asset-value-model-and-depreciation-book-merge"></a>Samruni virðislíkön eigna og afskriftarbækur

[!include[banner](../includes/banner.md)]


Í eldri útgáfum, voru tvö matshugtök fyrir eignir -  virðislíkön og afskriftabækur. Í Microsoft Dynamics 365 for Operations (1611) útgáfu, er virkni fyrir virðislíkön og afskriftarbókar sameinaðar í eitt hugtak sem kallast bók.

Ný virkni bókar er byggð á fyrri virkni virðislíkans en inniheldur einnig allar aðgerðir sem var áður veitt í eingöngu í afskriftarbók. [![Bók sem samruni virðislíkans og afskriftarbókar](./media/fixed-assets.png)](./media/fixed-assets.png) Vegna þessa samruna, geturðu nú notað eitt sett af síðum, fyrirspurnir og skýrslur fyrir öll eignaferli. Töflurnar í þessu efnisatriði lýsa fyrri virkni fyrir afskriftabækur og virðislíkön með nýjar aðgerðir fyrir afskriftabækur.

## <a name="setup"></a>Uppsetning
Sjálfgefið er að bækur bóka bæði í fjárhag (GL) og undirbók eignar. Bækur hafa nýja **Bóka í fjárhag** valkost sem gerir kleift að gera bókun á Fjárhag óvirka og bóka aðeins í undirbók eignar. Þessi virkni svipar fyrri hegðun bókana fyrir afskriftabækur. Uppsetning heiti færslubóka hefur nýja bókunarlag sem nefnist Ekkert. Þessi bókunarlag var bætt sérstaklega við fyrir eignafærslur. Til að bóka færslur fyrir bækur sem ekki bóka í fjárhag, verður að nota heiti færslubókar sem er með bókunarlag stillt á **Ekkert**.

|                                                  |                                 |                                 |                                                         |
|--------------------------------------------------|---------------------------------|---------------------------------|---------------------------------------------------------|
|                                                  | Afskriftabók               | Virðislíkan                     | Bók (Nýtt)                                              |
| Bóka í fjárhag                                   | Aldrei                           | Alltaf                          | Valkostur að bóka á Fjárhag                                |
| Bókunarlög                                   | Ekki tiltækt                  | 3: Núgildandi, aðgerðir, og skattur | 11: núgildandi, Aðgerðir, Skatt, 7 sérsniðna lögum og Ekkert |
| Færslubókanöfn                                    | Færslubókarheiti afskriftarbókar | Fjárhagur - Færslubókanöfn              | Fjárhagur - Færslubókanöfn                                      |
| Afleiddar bækur                                    | Ekki leyfð                     | Leyfð                         | Leyfð                                                 |
| Hnekking afskriftarreglu á stigi eignar | Leyfð                         | Ekki leyfð                     | Leyfð                                                 |

## <a name="processes"></a>Ferli
Ferli nota nú almenna síðuna. Sum ferla eru eingöngu leyfð ef **Bóka í fjárhag** valkostur er stilltur á **Nei** í uppsetningu bókar.

|                                |                           |                     |                                          |
|--------------------------------|---------------------------|---------------------|------------------------------------------|
|                                | Afskriftabók         | Virðislíkan         | Bók (Nýtt)                               |
| Innsláttur færslu              | Færslubók afskriftabókar | Eignabók | Eignabók                      |
| Viðbótarafskriftir             | Leyfð                   | Ekki leyft         | Leyfð                                  |
| Eyða sögulegum færslum | Leyfð                   | Ekki leyft         | Leyft, nema verið sé að bóka í Fjárhags |
| Fjöldauppfærsla                    | Leyfð                   | Ekki leyft         | Leyft, nema verið sé að bóka í Fjárhags |

## <a name="inquiries-and-reports"></a>Fyrirspurnir og skýrslur
Fyrirspurnir og skýrslur styðja allar bækurnar . Skýrslur sem ekki með í eftirfarandi töflu studdu áður bæði afskriftarbækur og virðislíkön, og munu núna halda áfram til að styðja allar gerðir bóka. **Bókunarlag** svæði hefur einnig verið bætt við skýrslur, þannig að auðveldara er að bera kennst á færslubókanir.

|                                       |                                |                          |                          |
|---------------------------------------|--------------------------------|--------------------------|--------------------------|
|                                       | Afskriftabók              | Virðislíkan              | Bók (Nýtt)               |
| Fyrirspurnir                             | Afskriftabókarfærslur | Eignafærslur | Eignafærslur |
| Eignayfirlit                 | Ekki leyfð                    | Leyfð                  | Leyfð                  |
| Eignagrunnur                     | Leyfð                        | Ekki leyfð              | Leyfð                  |
| Hæfi eignar á miðjum fjórðungi | Leyfð                        | Ekki leyfð              | Leyfð                  |

## <a name="upgrade"></a>Uppfæra
Uppfærsluferlið færir fyrirliggjandi uppsetningu og allar fyrirliggjandi færslur til uppbyggingar nýju bókarinnar. Virðislíkön haldast eins og þau eru, sem bók sem bókar í fjárhag. Hins vegar verða afskriftabækur flutt í bók sem hefur **Bóka í fjárhag** valkostur stilltur á **Nei**. Færslubókaheiti afskriftabóka verði flutt í færslubókarheitið fjárhags sem er með bókunarlag stillt á **Ekkert**.




