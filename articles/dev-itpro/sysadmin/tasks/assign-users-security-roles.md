---
title: Úthluta notendum á öryggishlutverk
description: Til að fá aðgang að Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, þarf að úthluta notendum á öryggishlutverk.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4c0afd0f5754e59307a82af9c9700b36c31edcc4
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851360"
---
# <a name="assign-users-to-security-roles"></a>Úthluta notendum á öryggishlutverk

[!include [task guide banner](../../includes/task-guide-banner.md)]

Til að fá aðgang að Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, þarf að úthluta notendum á öryggishlutverk. Þessu ferli útskýrt hvernig kerfisstjórum hægt úthluta notendum á hlutverk sjálfkrafa, byggt á viðskiptagögn. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.


## <a name="automatically-assign-users-to-roles"></a>Sjálfkrafa skipa notendum í hlutverkin
1. Farðu í **Skoðunarrúða > Kerfiseiningar > Kerfisstjórnun > Ötyggi > Úthluta notendum á hlutverk**.
2. Í þessu dæmi skal velja yfirmaður Bókhalds. Veljið hlutverk sem nota á fyrir útvinnsluna á reglunni. Í þessu dæmi skal velja yfirmann bókhalds. 
3. Smelltu á **Bæta við reglu** til að opna felligluggann.
4. Á listanum **Velja fyrirspurn** skaltu finna og velja skrána sem óskað er eftir. Velja fyrirspurn fyrir þessa reglu.  
5. Á listanum **Heiti aðildarreglu** skaltu smella á tengilinn í valinni röð.
6. Smelltu á **Breyta fyrirspurn**. Breyta skal fyrirspurninni eftir því sem þörf krefur.  
7. Smellt er á **OK**.

## <a name="exclude-users-from-automatic-role-assignment"></a>Útiloka notendum frá sjálfvirka hlutverkaúthlutun
1. Lokið síðunni.
2. Farðu í **Skoðunarrúða > Kerfiseiningar > Kerfisstjórnun > Ötyggi > Úthluta notendum á hlutverk**.
3. Í þessu dæmi skal velja yfirmaður Bókhalds. Veljið hlutverk. Fyrir þessu dæmi skal velja yfirmann bókhalds.  
4. Í valmyndinni **Notendur sem úthlutað er á hlutverk** skaltu velja **Úthluta / útiloka notendur handvirkt**.
5. Í listanum **Úthluta notendum til eða útiloka notendur frá hlutverki** skaltu merkja valda línu. Velja notanda  
6. Í **Aðgerðarsvæði** velurðu **Útiloka frá hlutverki**.
    
    Smelltu á **Útiloka frá hlutverki** til útiloka valda notendur frá hlutverinu. Til að fjarlægja útilokanir skal velja notendur sem á að fjarlægja útilokanir á og smella síðan á **Endurstilla stöðu**. Þegar fjarlægja útilokun með því að endurstilla stöðu notanda er hlutverki notanda aftur úthlutað sjálfkrafa. Hins vegar notanda er ekki strax þetta hlutverk úthlutað eða útilokað frá hlutverki þegar endurstilla stöðu. Í stað þess, notandinn annað hvort úthlutaður í hlutverkið eða fjarlægð úr hlutverk í næsta sinn sem keyrðar eru reglum fyrir sjálfvirka hlutverkaúthlutun.  
