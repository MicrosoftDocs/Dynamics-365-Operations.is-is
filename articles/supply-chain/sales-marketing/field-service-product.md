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

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a><span data-ttu-id="729f2-103">Samstilla afurðir í Finance and Operations við afurðir í Field Service</span><span class="sxs-lookup"><span data-stu-id="729f2-103">Synchronize products in Finance and Operations to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="729f2-104">Þetta efnisatriði fjallar um sniðmát og undirliggjandi verk sem er notað til að samstilla afurðir úr Microsoft Dynamics 365 for Finance and Operations við Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="729f2-104">This topic discusses the templates and underlying task that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="729f2-105">Notaða sniðmátið **Afurðir Field Service (Fin and Ops til Field Service)** er byggt á sniðmátinu **Afurðir (Fin and Ops til Sales) - Beint** frá Prospect to Cash.</span><span class="sxs-lookup"><span data-stu-id="729f2-105">The used **Field Service Products (Fin and Ops to Field Service)** template is based on the **Products (Fin and Ops to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="729f2-106">Nánari upplýsingar er að finna í [Afurðir (Fin and Ops til Sales) - Beint](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="729f2-106">For more information, see [Products (Fin and Ops to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="729f2-107">Þetta efnisatriði lýsir aðeins muninum á milli sniðmátanna **Afurðir Field Service (Fin and Ops til Field Service)** og **Afurðir (Fin and Ops til Sales) - Beint**.</span><span class="sxs-lookup"><span data-stu-id="729f2-107">This topic only describes the differences between the **Field Service Products (Fin and Ops to Field Service)** and **Products (Fin and Ops to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="729f2-108">Sniðmát og verkefni</span><span class="sxs-lookup"><span data-stu-id="729f2-108">Templates and tasks</span></span>

<span data-ttu-id="729f2-109">**Heiti sniðmátsins í Gagnaflutningi:**</span><span class="sxs-lookup"><span data-stu-id="729f2-109">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="729f2-110">Afurðir Field Service (Fin and Ops til Field Service)</span><span class="sxs-lookup"><span data-stu-id="729f2-110">Field Service Products (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="729f2-111">**Heiti verkefnis í gagnasamþættingarverkinu:**</span><span class="sxs-lookup"><span data-stu-id="729f2-111">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="729f2-112">Afurðir - Afurðir</span><span class="sxs-lookup"><span data-stu-id="729f2-112">Products - Products</span></span>

<span data-ttu-id="729f2-113">Sniðmátið **Afurðir Field Service (Fin and Ops til Field Service)** inniheldur eina vörpun sem ekki er innifalin í sniðmátinu **Afurðir (Fin and Ops til Sales) - Beint**.</span><span class="sxs-lookup"><span data-stu-id="729f2-113">The **Field Service Products (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Products (Fin and Ops to Sales) – Direct** template.</span></span> <span data-ttu-id="729f2-114">Þessi vörpun tryggir að sértæki Field Service reiturinn **Gerð afurðarþjónustu** sem krafist er sé rétt stilltur.</span><span class="sxs-lookup"><span data-stu-id="729f2-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="729f2-115">Eftirfarandi gildisvörpun er notuð.</span><span class="sxs-lookup"><span data-stu-id="729f2-115">The following value mapping is used.</span></span>

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="729f2-116">Í Finance and Operations er gildið **Afurðargerð Field Service** á gagnaeiningunni **Seljanlegar útgefnar afurðir** reiknað út sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="729f2-116">In Finance and Operations, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="729f2-117">**Birgðir:** Afurðargerð = Afurð og vörulíkanaflokkur, afurð á lager = rétt</span><span class="sxs-lookup"><span data-stu-id="729f2-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="729f2-118">**Ekki birgðir:** Afurðargerð = Afurð og vörulíkanaflokkur, afurð á lager = rangt</span><span class="sxs-lookup"><span data-stu-id="729f2-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="729f2-119">**Þjónusta:** Afurðargerð = Þjónusta</span><span class="sxs-lookup"><span data-stu-id="729f2-119">**Service:** Product type = Service</span></span>

