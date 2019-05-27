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
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2019
ms.locfileid: "1535860"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="c1ed3-103">Samstilla afurðir með birgðaeiningu úr Finance and Operations við Field Service</span><span class="sxs-lookup"><span data-stu-id="c1ed3-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c1ed3-104">Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla vörur við birgðaeiningar úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="c1ed3-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="c1ed3-105">[![Samstilling viðskiptaferla milli Finance and Operations og Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="c1ed3-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="c1ed3-106">Notaða sniðmátið **Afurðir Field Service með birgðaeiningu (Fin and Ops til Field Service)** byggist á sniðmátinu **Afurðir Field Service (Fin and Ops til Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="c1ed3-106">The used **Field Service Products with Inventory unit (Fin and Ops to Field Service)** template is based on the **Field Service Products (Fin and Ops to Field Service)** template.</span></span> <span data-ttu-id="c1ed3-107">Nánari upplýsingar er að finna í [Afurðir Field Service (Finance and Operations til Field Service)](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="c1ed3-107">For more information, see [Field Service Products (Finance and Operations to Field Service)](field-service-product.md).</span></span>

<span data-ttu-id="c1ed3-108">Þetta efnisatriði útskýrir muninn milli sniðmátanna tveggja:</span><span class="sxs-lookup"><span data-stu-id="c1ed3-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="c1ed3-109">**Afurðir Field Service með birgðaeiningu (Fin and Ops til Sales)**</span><span class="sxs-lookup"><span data-stu-id="c1ed3-109">**Field Service Products with Inventory unit (Fin and Ops to Sales)**</span></span>
- <span data-ttu-id="c1ed3-110">**Afurðir Field Service (Fin and Ops til Field Service)**</span><span class="sxs-lookup"><span data-stu-id="c1ed3-110">**Field Service Products (Fin and Ops to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="c1ed3-111">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="c1ed3-111">Templates and tasks</span></span>

<span data-ttu-id="c1ed3-112">**Heiti sniðmátsins í Gagnaflutningi:**</span><span class="sxs-lookup"><span data-stu-id="c1ed3-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="c1ed3-113">Afurðir Field Service með birgðaeiningu (Fin and Ops til Sales)</span><span class="sxs-lookup"><span data-stu-id="c1ed3-113">Field Service Products with Inventory unit (Fin and Ops to Sales)</span></span>

<span data-ttu-id="c1ed3-114">**Heiti verkefnis í gagnasamþættingarverkinu:**</span><span class="sxs-lookup"><span data-stu-id="c1ed3-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="c1ed3-115">Afurðir</span><span class="sxs-lookup"><span data-stu-id="c1ed3-115">Products</span></span>

<span data-ttu-id="c1ed3-116">Notaða sniðmátið **Afurðir Field Service með birgðaeiningu (Finance and Operations til Field Service)** inniheldur eina vörpun sem er ekki hluti af sniðmátinu **Afurðir Field Service (Fin and Ops til Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="c1ed3-116">The **Field Service Products with Inventory unit (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Fin and Ops to Field Service)** template.</span></span> <span data-ttu-id="c1ed3-117">Þessi vörpun tryggir að nauðsynleg birgðaeining fyrir samstillingu birgðastöðu sé innifalin.</span><span class="sxs-lookup"><span data-stu-id="c1ed3-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c1ed3-118">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="c1ed3-118">Template mapping in Data integration</span></span>

<span data-ttu-id="c1ed3-119">Eftirfarandi myndir sýna sniðmátsvörpunina í Gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="c1ed3-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-fin-and-ops-to-field-service-products"></a><span data-ttu-id="c1ed3-120">Afurðir Field Service (Fin and Ops til Field Service): Afurðir</span><span class="sxs-lookup"><span data-stu-id="c1ed3-120">Field Service Products with Inventory unit (Fin and Ops to Field Service): Products</span></span>

<span data-ttu-id="c1ed3-121">[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="c1ed3-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
