---
title: Samstilla afurðir í Finance and Operations við afurðir í Field Service
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla vörur úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.
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
ms.openlocfilehash: 3f26240ec289f5ddcc2682e598bbf93f516b99af
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562696"
---
# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a><span data-ttu-id="58471-103">Samstilla afurðir úr Finance and Operations við afurðir í Field Service</span><span class="sxs-lookup"><span data-stu-id="58471-103">Synchronize products in Finance and Operations to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="58471-104">Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla vörur úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="58471-104">This topic discusses the templates and underlying task that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="58471-105">Notaða sniðmátið **Afurðir Field Service (Fin and Ops til Field Service)** er byggt á sniðmátinu **Afurðir (Fin and Ops til Sales) - Beint** frá Prospect to Cash.</span><span class="sxs-lookup"><span data-stu-id="58471-105">The used **Field Service Products (Fin and Ops to Field Service)** template is based on the **Products (Fin and Ops to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="58471-106">Nánari upplýsingar er að finna í [Afurðir (Fin and Ops til Sales) - Beint](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="58471-106">For more information, see [Products (Fin and Ops to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="58471-107">Þetta efnisatriði lýsir aðeins muninum á milli sniðmátanna **Afurðir Field Service (Fin and Ops til Field Service)** og **Afurðir (Fin and Ops til Sales) - Beint**.</span><span class="sxs-lookup"><span data-stu-id="58471-107">This topic only describes the differences between the **Field Service Products (Fin and Ops to Field Service)** and **Products (Fin and Ops to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="58471-108">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="58471-108">Templates and tasks</span></span>

<span data-ttu-id="58471-109">**Heiti sniðmátsins í Gagnaflutningi:**</span><span class="sxs-lookup"><span data-stu-id="58471-109">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="58471-110">Afurðir Field Service (Fin and Ops til Field Service)</span><span class="sxs-lookup"><span data-stu-id="58471-110">Field Service Products (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="58471-111">**Heiti verkefnis í gagnasamþættingarverkinu:**</span><span class="sxs-lookup"><span data-stu-id="58471-111">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="58471-112">Afurðir - Afurðir</span><span class="sxs-lookup"><span data-stu-id="58471-112">Products - Products</span></span>

<span data-ttu-id="58471-113">Sniðmátið **Afurðir Field Service (Fin and Ops til Field Service)** inniheldur eina vörpun sem ekki er innifalin í sniðmátinu **Afurðir (Fin and Ops til Sales) - Beint**.</span><span class="sxs-lookup"><span data-stu-id="58471-113">The **Field Service Products (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Products (Fin and Ops to Sales) – Direct** template.</span></span> <span data-ttu-id="58471-114">Þessi vörpun tryggir að sértæki Field Service reiturinn **Gerð afurðarþjónustu** sem krafist er sé rétt stilltur.</span><span class="sxs-lookup"><span data-stu-id="58471-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="58471-115">Eftirfarandi gildisvörpun er notuð.</span><span class="sxs-lookup"><span data-stu-id="58471-115">The following value mapping is used.</span></span>

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="58471-116">Í Finance and Operations er gildið **Afurðargerð Field Service** á gagnaeiningunni **Seljanlegar útgefnar afurðir** reiknað út sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="58471-116">In Finance and Operations, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="58471-117">**Birgðir:** Afurðargerð = Afurð og vörulíkanaflokkur, afurð á lager = rétt</span><span class="sxs-lookup"><span data-stu-id="58471-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="58471-118">**Ekki birgðir:** Afurðargerð = Afurð og vörulíkanaflokkur, afurð á lager = rangt</span><span class="sxs-lookup"><span data-stu-id="58471-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="58471-119">**Þjónusta:** Afurðargerð = Þjónusta</span><span class="sxs-lookup"><span data-stu-id="58471-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="58471-120">Sniðmátsvörpun í Gagnasamþættingu</span><span class="sxs-lookup"><span data-stu-id="58471-120">Template mapping in Data integration</span></span>

<span data-ttu-id="58471-121">Eftirfarandi myndir sýna sniðmátsvörpunina í Gagnasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="58471-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-fin-and-ops-to-field-service-products---products"></a><span data-ttu-id="58471-122">Field Service Afurðir (Fin og Ops to Field Service): Afurðir - Afurðir</span><span class="sxs-lookup"><span data-stu-id="58471-122">Field Service Products (Fin and Ops to Field Service): Products - Products</span></span>

<span data-ttu-id="58471-123">[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="58471-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>
