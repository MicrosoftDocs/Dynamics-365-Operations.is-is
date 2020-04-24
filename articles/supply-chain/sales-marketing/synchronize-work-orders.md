---
title: Samstilla vinnupantanir við verk (úr Field Service í Supply Chain Management
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla vinnupantanir með verknúmeri úr Dynamics 365 Field Service við Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5ebf23c5c831e9dad5d13c72f82eb3eeb30da853
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215862"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a>Samstilla vinnupantanir við verk (úr Field Service í Supply Chain Management

[!include[banner](../includes/banner.md)]

Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla vinnupantanir með verknúmeri úr Dynamics 365 Field Service við Dynamics 365 Supply Chain Management.

[![Samstilling viðskiptaferla milli Supply Chain Management og Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Notaða sniðmátið **Vinnupantanir með Project (Field Service til Supply Chain Management)** er byggt á sniðmátinu **Vinnupantanir (Field Service til Supply Chain Management)**. Frekari upplýsingar er að finna í [Samstilla vinnupantanir úr Field Service við sölupantanir í Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

Þetta efnisatriði útskýrir muninn milli sniðmátanna tveggja:
- **Verkbeiðnir við verk úr (Field Service í Supply Chain Management)**
- **Verkbeiðnir verk úr (Field Service í Supply Chain Management)**

Helsti munurinn er sá að þetta sniðmát inniheldur vörpun verknúmers sem er úthlutað til vinnupöntunar í Field Service, sem tryggir að sölupöntunin sem er búin til í Supply Chain Management innihaldi verknúmerið og að reikningsfærsla geti átt sér stað fyrir tengt verk. Að auki notar sniðmátið ítarlega fyrirspurn og síun.

## <a name="templates-and-tasks"></a>Sniðmát og verkefni

**Heiti sniðmátsins í Gagnaflutningi:**

- Verkbeiðnir við verk úr (Field Service í Supply Chain Management)

**Heiti verkefnis í gagnasamþættingarverkinu:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>CRM-lausn Field Service
Reitnum **Ytra verk** hefur verið bætt við eininguna Vinnupantanir. Þessi reitur er uppfletting og með því að merkja vinnupöntunina þína með verki mun sölupöntun verða tengd við verk innan Supply Chain Management. Þegar **Kerfisstaða** breytist úr Opin - Í vinnslu (690.970.000) yfir í hærri stöðu, verður reitnum **Ytra verk** læst og ekki verður hægt að bæta við, fjarlægja eða breyta gildinu.

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi myndir sýna sniðmátsvörpunina í Gagnasamþættingu.

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a>Verkbeiðnir við verk úr (Field Service í Supply Chain Management): WorkOrderHeader

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a>Verkbeiðnir við verk úr (Field Service í Supply Chain Management): WorkOrderHeaderProject

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a>Verkbeiðnir við verk úr (Field Service í Supply Chain Management): WorkOrderProduct

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a>Verkbeiðnir við verk úr (Field Service í Supply Chain Management): WorkOrderService

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSWOP4.png)](./media/FSWOP4.png)
