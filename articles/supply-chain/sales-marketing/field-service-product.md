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
ms.openlocfilehash: f5f6d41f3e65a3cf5b8c7c96f54b1c8c6cdfaefb
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249774"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a><span data-ttu-id="e5a0f-103">Samstilla vörur í Supply Chain Management við vörur í Field Service</span><span class="sxs-lookup"><span data-stu-id="e5a0f-103">Synchronize products in Supply Chain Management to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e5a0f-104">Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla vörur úr Dynamics 365 Supply Chain Management við Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="e5a0f-104">This topic discusses the templates and underlying task that are used to synchronize products from Dynamics 365 Supply Chain Management to Dynamics 365  Field Service.</span></span>

<span data-ttu-id="e5a0f-105">Notaða sniðmátið **Afurðir Field Service (Supply Chain Management til Field Service)** er byggt á sniðmátinu **Afurðir (Supply Chain Management til Sales) - Beint** frá Prospect to Cash.</span><span class="sxs-lookup"><span data-stu-id="e5a0f-105">The used **Field Service Products (Supply Chain Management to Field Service)** template is based on the **Products (Supply Chain Management to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="e5a0f-106">Nánari upplýsingar er að finna í [Afurðir (Supply Chain Management til Sales) - Beint](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="e5a0f-106">For more information, see [Products (Supply Chain Management to Sales) – Direct](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="e5a0f-107">Þetta efnisatriði lýsir aðeins muninum á milli sniðmátanna **Afurðir Field Service (Supply Chain Management til Field Service)** og **Afurðir (Supply Chain Management til Sales) - Beint**.</span><span class="sxs-lookup"><span data-stu-id="e5a0f-107">This topic only describes the differences between the **Field Service Products (Supply Chain Management to Field Service)** and **Products (Supply Chain Management to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="e5a0f-108">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="e5a0f-108">Templates and tasks</span></span>

<span data-ttu-id="e5a0f-109">**Heiti sniðmátsins í Gagnaflutningi**</span><span class="sxs-lookup"><span data-stu-id="e5a0f-109">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="e5a0f-110">Vöruþjónustuvörur (Supply Chain Management til Field Service)</span><span class="sxs-lookup"><span data-stu-id="e5a0f-110">Field Service Products (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="e5a0f-111">**Heiti verkefnis í gagnasamþættingarverkinu**</span><span class="sxs-lookup"><span data-stu-id="e5a0f-111">**Name of the task in the Data integration project**</span></span>

- <span data-ttu-id="e5a0f-112">Afurðir - Afurðir</span><span class="sxs-lookup"><span data-stu-id="e5a0f-112">Products - Products</span></span>

<span data-ttu-id="e5a0f-113">Sniðmátið **Afurðir Field Service (Supply Chain Management til Field Service)** inniheldur eina vörpun sem er ekki innifalin í **Afurðir (Supply Chain Management til Sales) - Beint**.</span><span class="sxs-lookup"><span data-stu-id="e5a0f-113">The **Field Service Products (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Products (Supply Chain Management to Sales) – Direct** template.</span></span> <span data-ttu-id="e5a0f-114">Þessi vörpun tryggir að sértæki Field Service reiturinn **Gerð afurðarþjónustu** sem krafist er sé rétt stilltur.</span><span class="sxs-lookup"><span data-stu-id="e5a0f-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="e5a0f-115">Eftirfarandi gildisvörpun er notuð.</span><span class="sxs-lookup"><span data-stu-id="e5a0f-115">The following value mapping is used.</span></span>

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="e5a0f-116">Í Supply Chain Management er gildið **Afurðargerð Field Service** á gagnaeiningunni **Seljanlegar útgefnar afurðir** reiknað út sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="e5a0f-116">In Supply Chain Management, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="e5a0f-117">**Birgðir:** Afurðargerð = Afurð og vörulíkanaflokkur, afurð á lager = rétt</span><span class="sxs-lookup"><span data-stu-id="e5a0f-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="e5a0f-118">**Ekki birgðir:** Afurðargerð = Afurð og vörulíkanaflokkur, afurð á lager = rangt</span><span class="sxs-lookup"><span data-stu-id="e5a0f-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="e5a0f-119">**Þjónusta:** Afurðargerð = Þjónusta</span><span class="sxs-lookup"><span data-stu-id="e5a0f-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e5a0f-120">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="e5a0f-120">Template mapping in Data integration</span></span>

<span data-ttu-id="e5a0f-121">Eftirfarandi myndir sýna sniðmátsvörpunina í Gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="e5a0f-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a><span data-ttu-id="e5a0f-122">Vöruþjónustuvörur (Supply Chain Management til Field Service): Afurðir - Afurðir</span><span class="sxs-lookup"><span data-stu-id="e5a0f-122">Field Service Products (Supply Chain Management to Field Service): Products - Products</span></span>

<span data-ttu-id="e5a0f-123">[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="e5a0f-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>
