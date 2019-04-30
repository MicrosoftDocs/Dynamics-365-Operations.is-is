---
title: Samstilla afurðir með birgðaeiningu úr Finance and Operations við Field Service
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla vörur við birgðaeiningar úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
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
ms.openlocfilehash: 080672b9a6acd9fd6137580b5b7e14d12cfccf19
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/14/2019
ms.locfileid: "842463"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a>Samstilla afurðir með birgðaeiningu úr Finance and Operations við Field Service

[!include[banner](../includes/banner.md)]

Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla vörur við birgðaeiningar úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.

[![Samstilling viðskiptaferla milli Finance and Operations og Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Notaða sniðmátið **Afurðir Field Service með birgðaeiningu (Fin and Ops til Field Service)** byggist á sniðmátinu **Afurðir Field Service (Fin and Ops til Field Service)**. Nánari upplýsingar er að finna í [Afurðir Field Service (Finance and Operations til Field Service)](field-service-product.md).

Þetta efnisatriði útskýrir muninn milli sniðmátanna tveggja: 
- **Afurðir Field Service með birgðaeiningu (Fin and Ops til Sales)**
- **Afurðir Field Service (Fin and Ops til Field Service)** 

## <a name="templates-and-tasks"></a>Sniðmát og verkefni

**Heiti sniðmátsins í Gagnaflutningi:**

- Afurðir Field Service með birgðaeiningu (Fin and Ops til Sales)

**Heiti verkefnis í gagnasamþættingarverkinu:**

- Afurðir

Notaða sniðmátið **Afurðir Field Service með birgðaeiningu (Finance and Operations til Field Service)** inniheldur eina vörpun sem er ekki hluti af sniðmátinu **Afurðir Field Service (Fin and Ops til Field Service)**. Þessi vörpun tryggir að nauðsynleg birgðaeining fyrir samstillingu birgðastöðu sé innifalin.

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi myndir sýna sniðmátsvörpunina í Gagnasamþættingu.

### <a name="field-service-products-with-inventory-unit-fin-and-ops-to-field-service-products"></a>Afurðir Field Service (Fin and Ops til Field Service): Afurðir

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSProduct1.png)](./media/FSProduct1.png)
