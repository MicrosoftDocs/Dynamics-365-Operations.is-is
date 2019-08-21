---
title: Samstilla vinnupantanir með verki úr Field Service við Finance and Operations
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla vinnupantanir með verknúmeri úr Microsoft Dynamics 365 for Field Service við Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 77358513ffdf791ab10d6efe1b84f598ffb5ec26
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843410"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a>Samstilla vinnupantanir með verki úr Field Service við Finance and Operations

[!include[banner](../includes/banner.md)]

Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla vinnupantanir með verknúmeri úr Microsoft Dynamics 365 for Field Service við Microsoft Dynamics 365 for Finance and Operations.

[![Samstilling viðskiptaferla milli Finance and Operations og Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Notaða sniðmátið **Vinnupantanir með Project (Field Service til Fin and Ops)** er byggt á sniðmátinu **Vinnupantanir (Field Service til Fin and Ops)**. Frekari upplýsingar er að finna í [Samstilla vinnupantanir úr Field Service við sölupantanir í Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

Þetta efnisatriði útskýrir muninn milli sniðmátanna tveggja:
- **Vinnupantanir með Project (Field Service til Fin and Ops)**
- **Vinnupantanir (Field Service til Fin and Ops)**

Helsti munurinn er sá að þetta sniðmát inniheldur vörpun verknúmers sem er úthlutað til vinnupöntunar í Field Service, sem tryggir að sölupöntunin sem er búin til í Finance and Operations innihaldi verknúmerið og að reikningsfærsla geti átt sér stað fyrir tengt verk. Að auki notar sniðmátið ítarlega fyrirspurn og síun.

## <a name="templates-and-tasks"></a>Sniðmát og verkefni

**Heiti sniðmátsins í Gagnaflutningi:**

- Vinnupantanir með Project (Field Service til Fin and Ops)

**Heiti verkefnis í gagnasamþættingarverkinu:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>CRM-lausn Field Service
Reitnum **Ytra verk** hefur verið bætt við eininguna Vinnupantanir. Þessi reitur er uppfletting og með því að merkja vinnupöntunina þína með verki mun sölupöntun verða tengd við verk innan Finance and Operations. Þegar **Kerfisstaða** breytist úr Opin - Í vinnslu (690.970.000) yfir í hærri stöðu verður reitnum **Ytra verk** læst og ekki verður hægt að bæta við, fjarlægja eða breyta gildinu.

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi myndir sýna sniðmátsvörpunina í Gagnasamþættingu.

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a>Vinnupantanir með Project (Field Service til Fin and Ops): WorkOrderHeader

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a>Vinnupantanir með Project (Field Service til Fin and Ops): WorkOrderHeaderProject

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a>Vinnupantanir með Project (Field Service til Fin and Ops): WorkOrderProduct

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a>Vinnupantanir með Project (Field Service til Fin and Ops): WorkOrderService

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSWOP4.png)](./media/FSWOP4.png)
