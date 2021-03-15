---
title: Skilgreina starfsmann
description: Þetta ferli sýnir hvernig á að skilgreina starfsmaður sem sölufulltrúa sem er hæfur fyrir sölulaun fyrir sölu á Sölustað.
author: jblucher
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 73c200f7f6ff0aa5672e50c539bfaa5e30213185
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003604"
---
# <a name="configure-a-worker"></a>Skilgreina starfsmann

[!include [banner](../includes/banner.md)]

Þetta ferli sýnir hvernig á að skilgreina starfsmaður sem sölufulltrúa sem er hæfur fyrir sölulaun fyrir sölu á Sölustað. Þessi aðferð notar USRT sýnigögn fyrirtækisins.


## <a name="create-a-commission-sales-group-for-the-worker"></a>Stofna söluflokk sölulauna fyrir starfsmann.
1. Fara í Sölu og markaðssetningu > Þóknanir > Söluflokkar.
    * Hægt er að úthluta starfsmenn á eina eða fleiri söluflokka. Í POS, er hægt að velja alla söluflokka sem inniheldur starfskrafta úr aðsetursbók verslunarinnar.  
2. Smellið á „Nýtt“.
3. Í reitinn Hópur skal slá inn gildi.
4. Í reitinn Heiti skal slá inn gildi.
5. Smellið á „Vista“.
6. Smellið á „Almennt“ á aðgerðarúðunni.
7. Smellt er á Sölufulltrúa.
    * Söluflokkur getur innihaldið fleiri en einn starfsmann. Sölulaun má skipta á milli starfsmenn byggt á því hvernig þú skilgreina hluta sölulauna.  
8. Sláið inn eða veldu gildi í reitnum heiti.
9. Færið númer inn í svæðið hlutur sölulauna.
10. Smellið á „Vista“.
11. Lokið síðunni.
12. Lokið síðunni.

## <a name="assign-the-workers-default-sales-group"></a>Úthluta sjálfgefnum söluflokki starfsmanns
1. Fara í Retail og Commerce > Starfsmenn > Starfsfólk.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Í listanum skal smella á tengilinn í valinni línu.
4. Smellið á flipann Commerce.
    * Hægt er að úthluta starfsmanni á sjálfgefinn söluflokkur. Sjálfgefinn Söluflokkur verður sjálfkrafa bætt við sölulínur í Sölustað ef valkosturinn er virkjaður í virknireglu fyrir verslunina.  
5. Smellið á „Breyta“.
6. Færa inn eða veljið gildi í reitnum Sjálfgefinn flokkur.
7. Smellið á „Vista“.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]