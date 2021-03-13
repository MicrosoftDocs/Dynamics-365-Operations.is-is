---
title: Samstilla afurðir með birgðaeiningu úr Supply Chain Management við Field Service
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla vörur við birgðaeiningar úr Dynamics 365 Supply Chain Management við Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: c5be622d6f62d54bcec053b93700ce0c234b8308
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010898"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a>Samstilla afurðir með birgðaeiningu úr Supply Chain Management við Field Service

[!include[banner](../includes/banner.md)]

Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla vörur við birgðaeiningar úr Dynamics 365 Supply Chain Management við Dynamics 365 Field Service.

[![Samstilling viðskiptaferla milli Supply Chain Management og Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Notaða sniðmátið **Afurðir Field Service með birgðaeiningu (Supply Chain Management til Field Service)** byggist á sniðmátinu **Afurðir Field Service (Supply Chain Management til Field Service)**. Frekari upplýsingar er að finna í [Samstilla vörur í Supply Chain Management við vörur í Field Service](field-service-product.md).

Þetta efnisatriði útskýrir muninn milli sniðmátanna tveggja: 
- **Afurðir Field Service við birgðaeiningu (Supply Chain Management við Sales)**
- **Vöruþjónustuvörur (Supply Chain Management til Field Service)** 

## <a name="templates-and-tasks"></a>Sniðmát og verkefni

**Heiti sniðmátsins í Gagnaflutningi:**

- Afurðir Field Service við birgðaeiningu (Supply Chain Management við Sales)

**Heiti verkefnis í gagnasamþættingarverkinu:**

- Afurðir

Sniðmátið **Field Service Products með birgðaeiningu (Supply Chain Management til Field Service)** inniheldur eina vörpun sem er ekki hluti af sniðmátinu **Field Service Products (Supply Chain Management til Field Service)**. Þessi vörpun tryggir að nauðsynleg birgðaeining fyrir samstillingu birgðastöðu sé innifalin.

```plaintext
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi myndir sýna sniðmátsvörpunina í Gagnasamþættingu.

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a>Afurðir Field Service með birgðaeiningu (Supply Chain Management til Field Service): Products

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSProduct1.png)](./media/FSProduct1.png)
