---
title: Vinna úr fríðindahæfni
description: Þessi grein útskýrir hvernig á að keyra hæfisferlið fyrir innritun.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bd05585f691a4c6aa55a7aec7ceaaf0273f0abcb
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9323482"
---
# <a name="process-enrollment-eligibility"></a>Vinna úr fríðindahæfni

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þessi grein útskýrir hvernig á að keyra hæfisferlið fyrir innritun.

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Í vinnslu**, veldu **Vinnsla hæfis fyrir innritun**.

2. Í valmyndinni **Keyra hæfisferli við innritun**, tilgreindu gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | **Skráningartímabil** | Innritunartímabilið til að vinna úr hæfi innritunar. |
   | **Lögaðili** | Lögaðilinn til að vinna úr hæfi innritunar fyrir. |
   | **Starfskraftur** | Starfskrafturinn til að vinna úr hæfi innritunar fyrir. Ef þú skilur þennan reit eftir auðan verður vinnufærni allra starfsmanna afgreidd. |
   | **Fríðindaáætlun** | Fríðindaáætlun til að vinna úr hæfi innritunar fyrir.

3. Ef þú vilt keyra ferlið í bakgrunni skaltu velja **Keyra í bakgrunni** og framkvæma eftirfarandi verk:

   1. Færið inn upplýsingar fyrir ferlið.

   2. Veldu til að setja upp endurtekið starf **Endurtekning**, sláðu inn upplýsingar um endurtekningu og veldu **Í lagi**.

   3. Veldu til að setja upp atvinnuviðvörun **Viðvaranir**, veldu viðvaranir sem berast og veldu síðan **Í lagi**.

   4. Veljið **Í lagi**. Ferlið keyrir með breytunum sem þú stillir.

4. Veljið **Í lagi**.

## <a name="view-process-results"></a>Skoða niðurstöður vinnslu

Þessi grein útskýrir hvernig á að skoða niðurstöður vinnslu.

1.  Í vinnusvæðinu **Fríðindastjórnun**, undir **Í vinnslu**, veldu **Niðurstöður vinnslu**.

2.  Á síðunni **Vinna úr niðurstöðum** eru eftirfarandi reitir tilgreindir:

   | Svæði | lýsing |
   | --- | --- |
   | **Vinnslukenni** | Einstakt auðkenni fyrir samsetningu starfsmanns, lögaðila og vinnslu keyrslu. |
   | **Gerð ferlis** | Þetta greinir ferlið sem var keyrt. Til dæmis:  Skráning. |
   | **Tímastilling** | Tíminn sem hæfisferlið var keyrt. |
   | **Lögaðili** | Lögaðilinn sem er tilgreindur við innritunarferlið. |
   | **Starfsmaður** | Starfsmaðurinn sem var unninn. |
   | **Fyrirkomulag | Fríðindaátlunin sem reynt var að taka þátt í. |
   | **Hæfnisregla** | Hæfisreglan sem var afgreidd. Ef villa kom upp áður en hæfni var keyrð verður þetta tómt. Til dæmis: Ef ekki hafa verið skilgreindar bætur fyrir starfsmann mun hæfisferlið ekki keyra og þessi reitur verður skilinn auður. |
   | **Niðurstöður** | Þetta verður gjaldgeng eða óhæfur. Niðurstaðan verður óhæf ef starfsmaðurinn uppfyllti ekki skilyrði fyrir hæfisreglu, ef starfsmanninn vantar nauðsynlegar upplýsingar, svo sem launatíðni eða fastar bætur, eða ef það vantar upplýsingar í bótakerfið sem kemur í veg fyrir að starfsmenn séu skráðir. |
   | **Niðurstöðuskilaboð** | Gefur til kynna hvers vegna starfsmaður er óhæfur til fríðindaáætlunar eða ef hæfisreglan var samþykkt. |



[!INCLUDE[footer-include](../includes/footer-banner.md)]
