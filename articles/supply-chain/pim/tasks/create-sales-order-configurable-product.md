---
title: Stofna sölupöntun fyrir skilgreinanlega afurð
description: Þetta verkefni sýnir hvernig á að nota grunnstillingarsniðmát fyrir afurð á sölupöntun.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 988d87757019d20dcaf675af925166ed376685f5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430325"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a>Stofna sölupöntun fyrir skilgreinanlega afurð

[!include [banner](../../includes/banner.md)]

Þetta verkefni sýnir hvernig á að nota grunnstillingarsniðmát fyrir afurð á sölupöntun. Þetta dæmi notar D0006 líkanið í USMF sýnigögnum fyrirtækis. Venjulega notar sölupantanavinnsla þetta ferli.


## <a name="create-a-sales-order"></a>Stofna sölupöntun
1. Smellt er á Vinnsla og fyrirspurnir sölupantana.
2. Smellið á „Nýtt“.
3. Smellt er á sölupöntun.
4. Í reitnum Viðskiptavinalykill velurðu US-001. 
5. Smellið á „Í lagi“.
6. Í svæðið vörunúmer veldu 'D0006'.
    * Fyrir þetta verk þarf að velja samskipanlega afurð.  
7. Smellt er á Afurð og framboð.
8. Smellt er á Skilgreina línu.
    * Athugið að verði hefur verið breytt, byggt á stillingunni sem var valin, og að Taka köplum svæðið er núna stillt á Satt.  
    * Athugið sjálfgefna verð- og stillingar sem eru valdar fyrir á köplum.  
9. Smellt er á Hlaða sniðmáti.
    * Þetta dæmi sýnir hvernig hægt er að nota sniðmát til að velja forskilgreind afbrigði. Ef þetta ferli er notað sem verkleiðbeiningar og til að sjá hin eigindagildin sem eru tiltæk verður að smella á hnappinn Aflæsa.  
10. Smellið á „Í lagi“.
11. Smellið á „Í lagi“.
12. Víkkið út hlutann „Upplýsingar um línu“.
13. Smellið á flipann Afurðar.
    * Afbrigði vörunnar er nú skráður undir afurðarvíddum.  
14. Lokið síðunni.

## <a name="select-the-product-configuration"></a>Veljið vöruafbrigði.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]