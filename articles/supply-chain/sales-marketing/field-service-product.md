---
title: Samstilla vörur í Supply Chain Management við vörur í Field Service
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla vörur úr Dynamics 365 Supply Chain Management við Dynamics 365 Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: c87e4cbfa375ef99d00c9a145c190af78e912d56
ms.sourcegitcommit: d8a2301eda0e5d0a6244ebbbe4459ab6caa88a95
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029406"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a>Samstilla vörur í Supply Chain Management við vörur í Field Service

[!include[banner](../includes/banner.md)]

Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla vörur úr Dynamics 365 Supply Chain Management við Dynamics 365 Field Service.

Notaða sniðmátið **Afurðir Field Service (Supply Chain Management til Field Service)** er byggt á sniðmátinu **Afurðir (Supply Chain Management til Sales) - Beint** frá Prospect to Cash. Nánari upplýsingar er að finna í [Afurðir (Supply Chain Management til Sales) - Beint](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Þetta efnisatriði lýsir aðeins muninum á milli sniðmátanna **Afurðir Field Service (Supply Chain Management til Field Service)** og **Afurðir (Supply Chain Management til Sales) - Beint**.

## <a name="templates-and-tasks"></a>Sniðmát og verkefni

**Heiti sniðmátsins í Gagnaflutningi**

- Vöruþjónustuvörur (Supply Chain Management til Field Service)

**Heiti verkefnis í gagnasamþættingarverkinu**

- Afurðir - Afurðir

Sniðmátið **Afurðir Field Service (Supply Chain Management til Field Service)** inniheldur eina vörpun sem er ekki innifalin í **Afurðir (Supply Chain Management til Sales) - Beint**. Þessi vörpun tryggir að sértæki Field Service reiturinn **Gerð afurðarþjónustu** sem krafist er sé rétt stilltur.

```Text
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

Eftirfarandi gildisvörpun er notuð.

```Text
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

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSProduct.png)](./media/FSProduct.png)
