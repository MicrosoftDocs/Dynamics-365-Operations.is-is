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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 3485e4f284218924cee01e45d5248f5af1a64010
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215954"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a><span data-ttu-id="0ea87-103">Samstilla afurðir með birgðaeiningu úr Supply Chain Management við Field Service</span><span class="sxs-lookup"><span data-stu-id="0ea87-103">Synchronize products with inventory unit from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0ea87-104">Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla vörur við birgðaeiningar úr Dynamics 365 Supply Chain Management við Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="0ea87-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="0ea87-105">[![Samstilling viðskiptaferla milli Supply Chain Management og Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="0ea87-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="0ea87-106">Notaða sniðmátið **Afurðir Field Service með birgðaeiningu (Supply Chain Management til Field Service)** byggist á sniðmátinu **Afurðir Field Service (Supply Chain Management til Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="0ea87-106">The used **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template is based on the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="0ea87-107">Frekari upplýsingar er að finna í [Samstilla vörur í Supply Chain Management við vörur í Field Service](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="0ea87-107">For more information, see [Synchronize products in Supply Chain Management to products in Field Service](field-service-product.md).</span></span>

<span data-ttu-id="0ea87-108">Þetta efnisatriði útskýrir muninn milli sniðmátanna tveggja:</span><span class="sxs-lookup"><span data-stu-id="0ea87-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="0ea87-109">**Afurðir Field Service við birgðaeiningu (Supply Chain Management við Sales)**</span><span class="sxs-lookup"><span data-stu-id="0ea87-109">**Field Service Products with Inventory unit (Supply Chain Management to Sales)**</span></span>
- <span data-ttu-id="0ea87-110">**Vöruþjónustuvörur (Supply Chain Management til Field Service)**</span><span class="sxs-lookup"><span data-stu-id="0ea87-110">**Field Service Products (Supply Chain Management to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="0ea87-111">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="0ea87-111">Templates and tasks</span></span>

<span data-ttu-id="0ea87-112">**Heiti sniðmátsins í Gagnaflutningi:**</span><span class="sxs-lookup"><span data-stu-id="0ea87-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="0ea87-113">Afurðir Field Service við birgðaeiningu (Supply Chain Management við Sales)</span><span class="sxs-lookup"><span data-stu-id="0ea87-113">Field Service Products with Inventory unit (Supply Chain Management to Sales)</span></span>

<span data-ttu-id="0ea87-114">**Heiti verkefnis í gagnasamþættingarverkinu:**</span><span class="sxs-lookup"><span data-stu-id="0ea87-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="0ea87-115">Afurðir</span><span class="sxs-lookup"><span data-stu-id="0ea87-115">Products</span></span>

<span data-ttu-id="0ea87-116">Sniðmátið **Afurðir Field Service með birgðaeiningu (Supply Chain Management til Field Service)** inniheldur eina vörpun sem er ekki innifalin í sniðmátinu **Afurðir Field Service (Supply Chain Management til Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="0ea87-116">The **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Supply Chain Managementto Field Service)** template.</span></span> <span data-ttu-id="0ea87-117">Þessi vörpun tryggir að nauðsynleg birgðaeining fyrir samstillingu birgðastöðu sé innifalin.</span><span class="sxs-lookup"><span data-stu-id="0ea87-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```Text
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="0ea87-118">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="0ea87-118">Template mapping in Data integration</span></span>

<span data-ttu-id="0ea87-119">Eftirfarandi myndir sýna sniðmátsvörpunina í Gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="0ea87-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a><span data-ttu-id="0ea87-120">Afurðir Field Service með birgðaeiningu (Supply Chain Management til Field Service): Products</span><span class="sxs-lookup"><span data-stu-id="0ea87-120">Field Service Products with Inventory unit (Supply Chain Management to Field Service): Products</span></span>

<span data-ttu-id="0ea87-121">[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="0ea87-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
