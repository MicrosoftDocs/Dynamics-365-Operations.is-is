---
title: Úthluta notendum á öryggishlutverk
description: Til að fá aðgang að Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, þarf að úthluta notendum á öryggishlutverk.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55cb085bb5170aa4894a2240a12f6ca451b922fb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "349953"
---
# <a name="assign-users-to-security-roles"></a>Úthluta notendum á öryggishlutverk

[!include [task guide banner](../../includes/task-guide-banner.md)]

Til að fá aðgang að Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, þarf að úthluta notendum á öryggishlutverk. Þessu ferli útskýrt hvernig kerfisstjórum hægt úthluta notendum á hlutverk sjálfkrafa, byggt á viðskiptagögn. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.


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

