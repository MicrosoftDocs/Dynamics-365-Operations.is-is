---
title: Vinna úr breytingum á viðburðum
description: Þetta efnisatriði útskýrir hvernig á að vinna úr breytingum viðburða í Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cb894d9886c095d760efe66abcf773a975a99caa
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067605"
---
# <a name="process-life-event-changes"></a>Vinna úr breytingum á viðburðum


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Vinnsla á atburði í lífi atburða í Microsoft Dynamics 365 Human Resources vegna tveggja viðburðabreytinga:

- Afmælisdagurinn breytist
- Hæfisregla hnekkir breytingum á gildistíma 

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Í vinnslu**, veldu **Vinnsla viðburðabreytinga**.

2. Í valmyndinni **Keyra viðburðabreytingu**, tilgreindu gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | Skráningartímabil | Innritunartímabilið til að vinna úr viðburðabreytingum fyrir. |
   | Lögaðili | Lögaðilinn til að vinna úr viðburðabreytingum fyrir. |

3. Ef þú vilt keyra ferlið í bakgrunni skaltu velja **Keyra í bakgrunni** og framkvæma eftirfarandi verk:

   1. Færið inn upplýsingar fyrir ferlið.

   2. Veldu til að setja upp endurtekið starf **Endurtekning**, sláðu inn upplýsingar um endurtekningu og veldu **Í lagi**.

   3. Veldu til að setja upp atvinnuviðvörun **Viðvaranir**, veldu viðvaranir sem berast og veldu síðan **Í lagi**.

   4. Veljið **Í lagi**. Ferlið keyrir með breytunum sem þú stillir.

4. Veljið **Í lagi**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
