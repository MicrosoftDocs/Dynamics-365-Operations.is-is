---
title: Auðkenna og leysa úr árekstrum innan aðskilnaðar á skyldum
description: Þetta efni útskýrir hvernig skulu auðkenna og leysa úr árekstrum innan aðskilnaðar á skyldum.
author: maertenm
manager: AnnBe
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69dabb44ef08bf798b86cd031536146880c8fd40
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982479"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Auðkenna og leysa úr árekstrum innan aðskilnaðar á skyldum

[!include [banner](../../includes/banner.md)]

Þetta efni útskýrir hvernig skulu auðkenna og leysa úr árekstrum innan aðskilnaðar á skyldum. Hægt er að setja upp reglur til að aðskilja verk sem þarf að framkvæma af mismunandi notendum. Þetta hugtak er kallað Aðskilnaður á skyldum. Þegar skilgreining á öryggishlutverki eða hlutverkaúthlutun notanda brýtur reglurnar er árekstur skráður. Allir árekstrar verða leystir af kerfisstjóra. Ljúktu við eftirfarandi til að auðkenna og leysa úr árekstrum. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.


## <a name="verify-whether-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Sannprófa hvort hlutverk notanda úthlutun samræmist nýjum reglum fyrir aðskilnað á skyldum
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Kerfisstjórnun > Öryggi > Aðskilnaður á skyldum > Sannreyna skal samræmi notendahlutaverka**.
2. Veljið **Í lagi**. Ef árekstur kemur upp geturðu opnað síðuna Notandi og breytt hlutverkaúthlutun notanda. Ef árekstur kemur upp geturðu opnað síðuna **Notandi** og breytt hlutverkaúthlutun notanda. Árekstrar er einnig skráðir á síðunni **Árekstrar við aðskilnað á skyldum**. Til að keyra sannprófun sem runuvinnslu skal velja **Runuvinnsla** og stilla síðan aðrar færibreytur runu. Þegar keyrslunni er lokið geturðu yfirfarið áreksturinn á síðunni **Árekstrar aðskilnaðar á skyldum**.  

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Skoða og leysa misræmi í hlutverkaúthlutun notanda
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Kerfisstjórnun > Öryggi > Aðskilnaður á skyldum > Árekstrar við aðskilnað á skyldum.** Veldu árekstur og veldu síðan einn af eftirfarandi hnöppum: **Hafna verkefni – Hafna úthlutun notanda á auka öryggishlutverk**. Ef þú hafnar sjálfvirkri hlutverkaúthlutun er notandinn merktur sem útilokað frá hlutverki. Útilokuðum notanda er ekki veittur aðgangur sem tengist hlutverkinu og ekki er hægt að úthluta notandanum á hlutverkið þar til kerfisstjóri fjarlægir útilokunina. Leyfa verkefni – **Hnekkja** árekstri og leyfa notandanum til að úthluta á bæði öryggishlutverk. Ef þú hnekkir árekstri verður að færa inn ástæðu í reitnum **Ástæðu fyrir hnekkingu**.  
2. Lokið síðunni.
3. Farðu í **Skoðunarrúðu > Kerfiseiningar > Kerfisstjórnun > Öryggi > Aðskilnaður á skyldum > Óleystir árekstrar í aðskilnaði á skyldum.** Veldu árekstur og veldu síðan einn af eftirfarandi hnöppum: **Hafna verkefni – Hafna úthlutun notanda á auka öryggishlutverk**. Ef þú hafnar sjálfvirkri hlutverkaúthlutun er notandinn merktur sem útilokað frá hlutverki. Útilokuðum notanda er ekki veittur aðgangur sem tengist hlutverkinu og ekki er hægt að úthluta notandanum á hlutverkið þar til kerfisstjóri fjarlægir útilokunina. Leyfa verkefni – **Hnekkja** árekstri og leyfa notandanum til að úthluta á bæði öryggishlutverk. Ef þú hnekkir árekstri verður að færa inn ástæðu í reitnum **Ástæðu fyrir hnekkingu**.    
4. Lokið síðunni.

## <a name="verify-whether-existing-roles-comply-with-new-rules-for-segregation-of-duties"></a>Sannprófa hvort fyrirliggjandi hlutverk samræmast nýjum reglum fyrir aðskilnað á skyldum
1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Kerfisstjórnun > Öryggi > Aðskilnaður á skyldum > Reglur varðandi aðskilnaði á skyldum.** Velja reglu.  
2. Veldu **Sannreyna skyldur og hlutverk**. Ef einhver fyrirliggjandi hlutverk brjóta valda reglu eru skilaboð birt sem innihalda heiti hlutverks og heiti þeirra skylda sem rekast á. Kerfisstjórinn þarf annaðhvort að gefa til kynna mildun á öryggishættunni eða breyta hlutverki þannig að hún brjóti ekki reglur um aðskilnað á skyldum. Ef ekkert hlutverk brýtur valda reglu birtast skilaboð um að öll hlutverk séu í samræmi.  

