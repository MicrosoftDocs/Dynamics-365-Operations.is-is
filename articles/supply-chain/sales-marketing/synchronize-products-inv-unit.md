---
title: Samstilla afurðir með birgðaeiningu úr Finance and Operations við Field Service
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla vörur við birgðaeiningar úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.
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
ms.openlocfilehash: 5d3767c1a499f3d888d8fc2ce06c2837442e39f0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "359245"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a>Samstilla afurðir með birgðaeiningu úr Finance and Operations við Field Service

[!include[banner](../includes/banner.md)]

Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla vörur við birgðaeiningar úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.

[![Samstilling viðskiptaferla milli Finance and Operations og Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Notaða sniðmátið **Afurðir Field Service (Finance and Operations til Field Service)** er byggt á sniðmátinu **Afurðir (Finance and Operations til Sales) - Beint** úr Prospect to Cash. Nánari upplýsingar er að finna í [Afurðir (Finance and Operations til Sales) - Beint](products-template-mapping-direct.md).

Þetta efnisatriði lýsir aðeins muninum á milli sniðmátanna **Afurðir Field Service (Finance and Operations til Field Service)** og **Afurðir Field Service (Finance and Operations til Field Service)**.

## <a name="templates-and-tasks"></a>Sniðmát og verkefni

**Heiti sniðmátsins í Gagnaflutningi:**

- Afurðir Field Service með birgðaeiningu (Finance and Operations til Sales)

**Heiti verkefnis í gagnasamþættingarverkinu:**

- Afurðir

Sniðmátið **Afurðir Field Service með birgðaeiningu (Finance and Operations til Field Service)** inniheldur eina vörpun sem er ekki hluti af sniðmátinu **Afurðir Field Service (Finance and Operations til Field Service)**. Þessi vörpun tryggir að nauðsynleg birgðaeining fyrir samstillingu birgðastöðu sé innifalin.

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi myndir sýna sniðmátsvörpunina í Gagnasamþættingu.

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a>Afurðir Field Service með birgðaeiningu (Finance and Operations til Field Service): Afurðir

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSProduct1.png)](./media/FSProduct1.png)
