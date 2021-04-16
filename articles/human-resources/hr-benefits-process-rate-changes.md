---
title: Vinna úr breytingum á hlutfalli
description: Vinnu breytinga á ávinningi hlutfall í Microsoft Dynamics 365 Human Resources þegar ný eða núverandi bótakerfi hefur breytingu á stillingum hæfisreglna.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c841f5d5d409c7e73cdc38988f8233747a11f837
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803826"
---
# <a name="process-rate-changes"></a>Vinna úr breytingum á hlutfalli

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Vinnu breytinga á ávinningi hlutfall í Microsoft Dynamics 365 Human Resources þegar ný eða núverandi bótakerfi hefur breytingu á stillingum hæfisreglna. Ef ný hæfisregla er búin til og þeim er úthlutað í áætlunina biður þetta kerfið um að endurkeyra hæfi starfsmanna til að athuga hvort starfsmenn geti nú verið gjaldgengir í áætlunina á grundvelli nýrra hæfiskosta. 

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Í vinnslu**, veldu **Vinnsla uppfærslu á taxtabreytingum**.

2. Í valmyndinni **Keyra uppfærsluferli fríðindataxta**, tilgreindu gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | **Skráningartímabil** | Innritunartímabilið til að vinna úr taxtabreytingum fyrir. |

3. Ef þú vilt keyra ferlið í bakgrunni skaltu velja **Keyra í bakgrunni** og framkvæma eftirfarandi verk:

   1. Færið inn upplýsingar fyrir ferlið.

   2. Veldu til að setja upp endurtekið starf **Endurtekning**, sláðu inn upplýsingar um endurtekningu og veldu **Í lagi**.

   3. Veldu til að setja upp atvinnuviðvörun **Viðvaranir**, veldu viðvaranir sem berast og veldu síðan **Í lagi**.

   4. Veljið **Í lagi**. Ferlið keyrir með breytunum sem þú stillir.

4. Veljið **Í lagi**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]