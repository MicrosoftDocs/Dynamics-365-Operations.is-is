---
title: Auðkenna og leysa úr árekstrum innan aðskilnaðar á skyldum
description: Þetta efni útskýrir hvernig skulu auðkenna og leysa úr árekstrum innan aðskilnaðar á skyldum.
author: peakerbl
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0ebd59c7018a50e01253697d792698664a981566
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745814"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Auðkenna og leysa úr árekstrum innan aðskilnaðar á skyldum

[!include [banner](../../includes/banner.md)]

Þetta efni útskýrir hvernig skulu auðkenna og leysa úr árekstrum innan aðskilnaðar á skyldum. Hægt er að setja upp reglur til að aðskilja skyldur sem þarf að framkvæma af mismunandi notendum. Þetta hugtak er kallað Aðskilnaður á skyldum. Þegar skilgreining á öryggishlutverki eða hlutverkaúthlutun notanda brýtur reglurnar er árekstur skráður. Allir árekstrar verða leystir af kerfisstjóra. Ljúktu við eftirfarandi til að auðkenna og leysa úr árekstrum.

Þegar reglu hefur verið bætt við skal staðfesta að öll fyrirliggjandi hlutverk séu samhæf. 

## <a name="verify-that-existing-roles-and-duties-comply-with-new-rules-for-segregation-of-duties"></a>Sannprófa hvort fyrirliggjandi hlutverk og skyldur samræmast nýjum reglum fyrir aðskilnað á skyldum
1. Farið í **Kerfisstjórnun** > **Öryggi** > **Aðskilnaður á skyldum** > **Reglur um aðskilnað á skyldum**.
3. Veldu **Sannreyna skyldur og hlutverk**. Ef einhver hlutverk brjóta valda reglu eru skilaboð birt sem innihalda heiti hlutverks og heiti þeirra skylda sem rekast á. Laga þarf hlutverk sem stangast á með **Öryggisskilgreiningu** og þau mega ekki innihalda skyldur sem stangast á. Ef ekkert hlutverk brýtur valda reglu birtast skilaboð um að öll hlutverk séu í samræmi.   

> [!NOTE]
> Prófunin er aðeins framkvæmd fyrir valda reglu. Mikilvægt er að sannprófa reglufylgni fyrir hverja reglu.   

Þegar hlutverk er stofnað eða því breytt er reglum um aðskilnað á skyldum sjálfkrafa beitt. Ekki er hægt að úthluta skyldum sem stangast á við hlutverk.

Næst skal staðfesta að allar fyrirliggjandi úthlutanir hlutverka séu samhæfar.

## <a name="verify-that-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Sannprófa að hlutverk notanda úthlutun samræmist nýjum reglum fyrir aðskilnað á skyldum
1. Farið í **Kerfisstjórnun > Öryggi > Aðskilnaður á skyldum > Staðfesta samræmi notendahlutverka**.
2. Veljið **Í lagi**. Ef árekstur kemur upp geturðu opnað síðuna Notandi og breytt hlutverkaúthlutun notanda. Árekstrar er einnig skráðir á síðunni **Óleystir árekstrar fyrir aðskilnað á skyldum**.   

Þegar notendum er úthlutað á hlutverk er reglum um aðskilnað á skyldum sjálfkrafa beitt. Ef reynt er að úthluta notanda á hlutverk sem fela í sér skyldur sem stangast á, koma upp villuboð. Þá þarf að leysa úr árekstrinum með því að hafna eða leyfa viðbótarúthlutun hlutverks. Viðbótarhlutverki verður úthlutað eftir að úthlutun er leyfð. 

> [!NOTE]
> Árekstrar eru ekki sem stendur staðfestir fyrir notendur sem úthlutað er hlutverkum sem byggja á flokkum Active Directory Domain.

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Skoða og leysa misræmi í hlutverkaúthlutun notanda
1. Farið í **Kerfisstjórnun** > **Öryggi** > **Aðskilnaður á skyldum** > **Óleystir árekstrar fyrir aðskilnað á skyldum**. 
2. Veljið árekstur og veljið síðan eina af eftirfarandi aðgerðum: 

  - **Hafna verkefni**: – Þetta mun hafna úthlutun notanda á auka öryggishlutverk. Ef þú hafnar sjálfvirkri hlutverkaúthlutun er notandinn merktur sem útilokað frá hlutverki. Útilokuðum notanda er ekki veittur aðgangur sem tengist hlutverkinu og ekki er hægt að úthluta notandanum á hlutverkið fyrr en kerfisstjóri fjarlægir útilokunina. 
-  **Leyfa úthlutun**: Þetta hnekkir árekstrinum og leyfir að notanda sé að auki úthlutað öryggishlutverki. Ef þú hnekkir árekstri verður að færa inn ástæðu í reitnum **Ástæðu fyrir hnekkingu**. Hægt er að skoða allar hnekktar úthlutanir hlutverka á síðunni **Árekstrar í aðskilnaði á skyldum**.  

> [!NOTE]
> Ef nokkrir árekstrar eru á listanum fyrir sama notanda skal velja færslu notanda og leggja mat á úthlutuð hlutverk á síðunni **Notendur**. Til að forðast þennan árekstur skal sannprófa hverja reglu fyrir sig þegar búið er að bæta henni við og breyta.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]