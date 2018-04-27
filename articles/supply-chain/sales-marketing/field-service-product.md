---
title: "Samstilla afurðir í Finance and Operations við afurðir í Field Service"
description: "Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem er notað til að samstilla afurðir úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08cfd2cfa24bef0f0c92126f5d1052a12ceba37a
ms.openlocfilehash: 699830ce6cd993f3dd3fd4ff744ce5a8b9645c32
ms.contentlocale: is-is
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a>Samstilla afurðir í Finance and Operations við afurðir í Field Service

[!include[banner](../includes/banner.md)]

Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem er notað til að samstilla afurðir úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.

Notaða sniðmátið **Afurðir Field Service (Fin and Ops til Field Service)** er byggt á sniðmátinu **Afurðir (Fin and Ops til Sales) - Beint** frá Prospect to Cash. Nánari upplýsingar er að finna í [Afurðir (Fin and Ops til Sales) - Beint](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Þetta efnisatriði lýsir aðeins muninum á milli sniðmátanna **Afurðir Field Service (Fin and Ops til Field Service)** og **Afurðir (Fin and Ops til Sales) - Beint**.

## <a name="templates-and-tasks"></a>Sniðmát og verkefni

**Heiti sniðmátsins í Gagnaflutningi:**

- Afurðir Field Service (Fin and Ops til Field Service)

**Heiti verkefnis í gagnasamþættingarverkinu:**

- Afurðir - Afurðir

Sniðmátið **Afurðir Field Service (Fin and Ops til Field Service)** inniheldur eina vörpun sem ekki er innifalin í sniðmátinu **Afurðir (Fin and Ops til Sales) - Beint**. Þessi vörpun tryggir að sértæki Field Service reiturinn **Gerð afurðarþjónustu** sem krafist er sé rétt stilltur.

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

Eftirfarandi gildisvörpun er notuð.

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

Í Finance and Operations er gildið **Afurðargerð Field Service** á gagnaeiningunni **Seljanlegar útgefnar afurðir** reiknað út sem hér segir:

- **Birgðir:** Afurðargerð = Afurð og vörulíkanaflokkur, afurð á lager = rétt
- **Ekki birgðir:** Afurðargerð = Afurð og vörulíkanaflokkur, afurð á lager = rangt
- **Þjónusta:** Afurðargerð = Þjónusta

