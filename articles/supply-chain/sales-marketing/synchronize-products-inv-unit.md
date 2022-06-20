---
title: Samstilla afurðir með birgðaeiningu úr Supply Chain Management við Field Service
description: Þessi grein fjallar um sniðmát og undirliggjandi verkefni sem eru notuð til að samstilla vörur við birgðaeiningu frá Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.
author: Henrikan
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5f7658eacd20aa69a64d6288e9d29e53b6ccb002
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887255"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a>Samstilla afurðir með birgðaeiningu úr Supply Chain Management við Field Service

[!include[banner](../includes/banner.md)]

Þessi grein fjallar um sniðmát og undirliggjandi verkefni sem eru notuð til að samstilla vörur við birgðaeiningu frá Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.

[![Samstilling viðskiptaferla milli Supply Chain Management og Field Service.](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Notaða sniðmátið **Afurðir Field Service með birgðaeiningu (Supply Chain Management til Field Service)** byggist á sniðmátinu **Afurðir Field Service (Supply Chain Management til Field Service)**. Frekari upplýsingar er að finna í [Samstilla vörur í Supply Chain Management við vörur í Field Service](field-service-product.md).

Þessi grein lýsir aðeins muninum á sniðmátunum tveimur: 
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

[![Sniðmátsvörpun í Gagnasamþættingu.](./media/FSProduct1.png)](./media/FSProduct1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]