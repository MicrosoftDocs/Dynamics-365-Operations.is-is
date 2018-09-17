--- 
title: "Bera kennsl og leysa úr árekstrum fyrir aðskilnað á skyldum"
description: "Hægt er að setja upp reglur til að aðskilja verk sem þarf að framkvæma af mismunandi notendum."
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c3a366ea4b558ba4e4af7336992dbb091b0b1414
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Bera kennsl og leysa úr árekstrum fyrir aðskilnað á skyldum

[!include [task guide banner](../../includes/task-guide-banner.md)]

Hægt er að setja upp reglur til að aðskilja verk sem þarf að framkvæma af mismunandi notendum. Þetta hugtak er kallað Aðskilnaður á skyldum. Þegar skilgreining á öryggishlutverki eða hlutverkaúthlutun notanda brýtur reglurnar er árekstur skráður. Allir árekstrar verða leystir af kerfisstjóra. Ljúktu við eftirfarandi til að auðkenna og leysa úr árekstrum. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.


## <a name="verify-whether-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Sannprófa hvort hlutverk notanda úthlutun samræmist nýjum reglum fyrir aðskilnað á skyldum
1. Farið í kerfisstjórnun > Öryggi > Aðskilnaður á skyldum > Staðfesta samræmi notendahlutverka.
2. Smellið á „Í lagi“.
    * Tilkynning birtir niðurstöður villuleitar.     Ef árekstur kemur upp geturðu opnað síðuna Notandi og breytt  hlutverkaúthlutun notanda. Árekstrar er einnig skráðir á síðunni Árekstrar við aðskilnað á skyldum.     Til að keyra sannprófun sem runuvinnslu skal velja Runuvinnsla og stilla síðan aðrar færibreytur runu. Þegar keyrslunni er lokið geturðu yfirfarið áreksturinn á síðunni Árekstrar aðskilnaðar á skyldum.  

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Skoða og leysa misræmi í hlutverkaúthlutun notanda
1. Farið í kerfisstjórnun > Öryggi > Aðskilnaður á skyldum > Árekstur í aðskilnaði á skyldum.
    * Veldu árekstur og smelltu svo á einn af eftirfarandi hnöppum: Hafna verkefni – Hafna úthlutun notanda á auka öryggishlutverk. Ef þú hafnar sjálfvirkri hlutverkaúthlutun er notandinn merktur sem útilokað frá hlutverki. Útilokuðum notanda er ekki veittur aðgangur sem tengist hlutverkinu og ekki er hægt að úthluta notandanum á hlutverkið þar til kerfisstjóri fjarlægir útilokunina.     Leyfa verkefni – Hnekkja árekstri og leyfa notandanum til að úthluta á bæði öryggishlutverk. Ef þú hnekkir árekstri verður að færa inn ástæðu í reitnum Ástæðu fyrir hnekkingu.  
2. Lokið síðunni.
3. Farið í kerfisstjórnun > Öryggi > Aðskilnaður á skyldum > Óleystir árekstrar í aðskilnaði á skyldum.
    * Veldu árekstur og smelltu svo á einn af eftirfarandi hnöppum: Hafna verkefni – Hafna úthlutun notanda á auka öryggishlutverk. Ef þú hafnar sjálfvirkri hlutverkaúthlutun er notandinn merktur sem útilokað frá hlutverki. Útilokuðum notanda er ekki veittur aðgangur sem tengist hlutverkinu og ekki er hægt að úthluta notandanum á hlutverkið þar til kerfisstjóri fjarlægir útilokunina.     Leyfa verkefni – Hnekkja árekstri og leyfa notandanum til að úthluta á bæði öryggishlutverk. Ef þú hnekkir árekstri verður að færa inn ástæðu í reitnum Ástæðu fyrir hnekkingu.    
4. Lokið síðunni.

## <a name="verify-whether-existing-roles-comply-with-new-rules-for-segregation-of-duties"></a>Sannprófa hvort fyrirliggjandi hlutverk samræmast nýjum reglum fyrir aðskilnað á skyldum
1. Farið í kerfisstjórnun > Öryggi > Aðskilnaður á skyldum > Reglur varðandi aðskilnaði á skyldum.
    * Velja reglu.  
2. Smella á Staðfesta skyldur og hlutverk.
    * Ef einhver fyrirliggjandi hlutverk brjóta valda reglu eru skilaboð birt sem innihalda heiti hlutverks og heiti þeirra skylda sem rekast á. Kerfisstjórinn þarf annaðhvort að gefa til kynna mildun á öryggishættunni eða breyta hlutverki þannig að hún brjóti ekki reglur um aðskilnað á skyldum.     Ef ekkert hlutverk brýtur valda reglu birtast skilaboð um að öll hlutverk séu í samræmi.  


