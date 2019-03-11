---
title: Samstilla vinnupantanir með verki úr Field Service við Finance and Operations
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla vinnupantanir með verknúmeri úr Microsoft Dynamics 365 for Field Service við Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 6b61411a5a235e2d0aad8bb25ae4a3bfcf1248d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "329851"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a>Samstilla vinnupantanir með verki úr Field Service við Finance and Operations

[!include[banner](../includes/banner.md)]

Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla vinnupantanir með verknúmeri úr Microsoft Dynamics 365 for Field Service við Microsoft Dynamics 365 for Finance and Operations.

[![Samstilling viðskiptaferla milli Finance and Operations og Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Notaða sniðmátið **Afurðir Field Service (Finance and Operations til Field Service)** er byggt á sniðmátinu **Afurðir (Finance and Operations til Sales) - Beint** úr Prospect to Cash. Nánari upplýsingar er að finna í [Afurðir (Finance and Operations til Sales) - Beint](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Þetta efnisatriði lýsir aðeins muninum á milli sniðmátanna **Afurðir Field Service (Finance and Operations til Field Service)** og **Afurðir Field Service (Finance and Operations til Field Service)**.

Helsti munurinn er sá að þetta sniðmát inniheldur vörpun verknúmers sem er úthlutað til vinnupöntunar í Field Service, sem tryggir að sölupöntunin sem er búin til í Finance and Operations innihaldi verknúmerið og að reikningsfærsla geti átt sér stað fyrir tengt verk. Að auki notar sniðmátið ítarlega fyrirspurn og síun.

## <a name="templates-and-tasks"></a>Sniðmát og verkefni

**Heiti sniðmátsins í Gagnaflutningi:**

- Vinnupantanir með verki (Field Service til Finance and Operations)

**Heiti verkefnis í gagnasamþættingarverkinu:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>CRM-lausn Field Service
Reitnum **Ytra verk** hefur verið bætt við eininguna Vinnupantanir. Þessi reitur er uppfletting og með því að merkja vinnupöntunina þína með verki mun sölupöntun verða tengd við verk innan Finance and Operations. Þegar **Kerfisstaða** breytist úr Opin - Í vinnslu (690.970.000) yfir í hærri stöðu verður reitnum **Ytra verk** læst og ekki verður hægt að bæta við, fjarlægja eða breyta gildinu.

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi myndir sýna sniðmátsvörpunina í Gagnasamþættingu.

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a>Vinnupantanir með verk (Field Service til Finance and Operations): WorkOrderHeader

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a>Vinnupantanir með verk (Field Service til Finance and Operations): WorkOrderHeaderProject

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a>Vinnupantanir með verk (Field Service til Finance and Operations): WorkOrderProduct

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a>Vinnupantanir með verk (Field Service til Finance and Operations): WorkOrderService

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSWOP4.png)](./media/FSWOP4.png)
