---
title: Samstilla vörur í Supply Chain Management við vörur í Field Service
description: Þessi grein fjallar um sniðmát og undirliggjandi verkefni sem eru notuð til að samstilla vörur frá Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.
author: Henrikan
ms.date: 04/09/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 114550f01f3aed197480fb6830fe913dbfa7b570
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860552"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a>Samstilla vörur í Supply Chain Management við vörur í Field Service

[!include[banner](../includes/banner.md)]

Þessi grein fjallar um sniðmát og undirliggjandi verkefni sem eru notuð til að samstilla vörur frá Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.

Notaða sniðmátið **Afurðir Field Service (Supply Chain Management til Field Service)** er byggt á sniðmátinu **Afurðir (Supply Chain Management til Sales) - Beint** frá Prospect to Cash. Nánari upplýsingar er að finna í [Afurðir (Supply Chain Management til Sales) - Beint](/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Þessi grein lýsir aðeins muninum á milli **Field Service Products (Aðfangakeðjustjórnun til Field Service)** og **Vörur (stjórnun aðfangakeðju til sölu) - Bein** sniðmát.

## <a name="templates-and-tasks"></a>Sniðmát og verkefni

**Heiti sniðmátsins í Gagnaflutningi**

- Vöruþjónustuvörur (Supply Chain Management til Field Service)

**Heiti verkefnis í gagnasamþættingarverkinu**

- Afurðir - Afurðir

Sniðmátið **Afurðir Field Service (Supply Chain Management til Field Service)** inniheldur eina vörpun sem er ekki innifalin í **Afurðir (Supply Chain Management til Sales) - Beint**. Þessi vörpun tryggir að sértæki Field Service reiturinn **Gerð afurðarþjónustu** sem krafist er sé rétt stilltur.

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

Eftirfarandi gildisvörpun er notuð.

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

Í Supply Chain Management er gildið **Afurðargerð Field Service** á gagnaeiningunni **Seljanlegar útgefnar afurðir** reiknað út sem hér segir:

- **Birgðir:** Afurðargerð = Afurð og vörulíkanaflokkur, afurð á lager = rétt
- **Ekki birgðir:** Afurðargerð = Afurð og vörulíkanaflokkur, afurð á lager = rangt
- **Þjónusta:** Afurðargerð = Þjónusta

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi myndir sýna sniðmátsvörpunina í Gagnasamþættingu.

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a>Vöruþjónustuvörur (Supply Chain Management til Field Service): Afurðir - Afurðir

[![Sniðmátsvörpun í Gagnasamþættingu.](./media/FSProduct.png)](./media/FSProduct.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]