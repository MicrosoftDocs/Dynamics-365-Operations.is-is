---
title: Vinna úr fríðindahæfni
description: Þessi grein útskýrir hvernig á að keyra hæfisferlið fyrir innritun.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 69ea23e4051a6975a5892cd027777c5a88472509
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112993"
---
# <a name="process-enrollment-eligibility"></a>Vinna úr fríðindahæfni

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

2.  Í forminu **Afgreiða niðurstöður** eru eftirfarandi reitir tilgreindir:

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

