--- 
title: "Skipa notendum í öryggishlutverk"
description: "Til að fá aðgang að Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition verður að hafa úthlutað notendum öryggishlutverk."
author: maertenm
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: b951bbf935645460f7be1df656ca2c5269a020ec
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="assign-users-to-security-roles"></a>Skipa notendum í öryggishlutverk

[!include[task guide banner](../../includes/task-guide-banner.md)]

Til að fá aðgang að Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition verður að hafa úthlutað notendum öryggishlutverk. Þessu ferli útskýrt hvernig kerfisstjórum hægt úthluta notendum á hlutverk sjálfkrafa, byggt á viðskiptagögn. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.


## <a name="automatically-assign-users-to-roles"></a>Sjálfkrafa skipa notendum í hlutverkin
1. Fara í Kerfisstjórn > Öryggi > Úthluta hlutverkum á notendur.
2. Í þessu dæmi skal velja yfirmaður Bókhalds.
    * Veljið hlutverk sem nota á fyrir útvinnsluna á reglunni. Í þessu dæmi skal velja yfirmann bókhalds.  
3. Smelltu á bæta við reglu til að opna felligluggann.
4. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Velja fyrirspurn fyrir þessa reglu.  
5. Í listanum skal smella á tengilinn í valinni línu.
6. Smellt er á Breyta fyrirspurn.
    * Breyta skal fyrirspurninni eftir því sem þörf krefur.  
7. Smellið á „Í lagi“.

## <a name="exclude-users-from-automatic-role-assignment"></a>Útiloka notendum frá sjálfvirka hlutverkaúthlutun
1. Lokið síðunni.
2. Fara í Kerfisstjórn > Öryggi > Úthluta hlutverkum á notendur.
3. Í þessu dæmi skal velja yfirmaður Bókhalds.
    * Veljið hlutverk. Fyrir þessu dæmi skal velja yfirmann bókhalds.  
4. Smelltu á Úthluta / útiloka notendum handvirkt.
5. Í listanum skal merkja valda línu.
    * Velja notanda  
6. Smelltu á Útiloka frá hlutverki.
    * Smelltu á Útiloka frá hlutverki til útiloka valda notendur úr hlutverinu. Til að fjarlægja útilokanir, veljið notendur sem á að fjarlægja útilokanir á og smellið síðan á Endurstilla stöðu. Þegar fjarlægja útilokun með því að endurstilla stöðu notanda er hlutverki notanda aftur úthlutað sjálfkrafa. Hins vegar notanda er ekki strax þetta hlutverk úthlutað eða útilokað frá hlutverki þegar endurstilla stöðu. Í stað þess, notandinn annað hvort úthlutaður í hlutverkið eða fjarlægð úr hlutverk í næsta sinn sem keyrðar eru reglum fyrir sjálfvirka hlutverkaúthlutun.  


