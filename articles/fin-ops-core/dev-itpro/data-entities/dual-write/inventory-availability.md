---
title: Birgðir til ráðstöfunar í tvíritun
description: Í þessu efnisatriði eru veittar upplýsingar um hvernig skuli athuga birgðir til ráðstöfunar í tvíritun.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 227a2062a7985a787f8278c196f7df2fb6f31691
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443873"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="2cb89-103">Birgðir til ráðstöfunar í tvíritun</span><span class="sxs-lookup"><span data-stu-id="2cb89-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2cb89-104">Með því að nota birgðaframboð er hægt að athuga birgðirnar áður en afurð er bætt við síðuna **Tilboð**, **Pantanir** eða **Reikningar** í Microsoft Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="2cb89-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations**, **Orders**, or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="2cb89-105">Til dæmis eru birgðir athugaðar og uppfyllingardagsetning ákvörðuð sem eitt lykilverk í ferlinu [prospect-to-cash](dual-write-prospect-to-cash.md).</span><span class="sxs-lookup"><span data-stu-id="2cb89-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="2cb89-106">Ef ekki eru til nægar birgðir er hægt að áætla afhendingardagsetningu sem byggist á áætlaðri birgðamóttöku og vandamálum.</span><span class="sxs-lookup"><span data-stu-id="2cb89-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="2cb89-107">Einnig er hægt að skoða „hægt að lofa“ upplýsingar um afurðina þar sem hægt er að finna „hægt að lofa“-magnið innan fyrirfram skilgreindra tímamarka.</span><span class="sxs-lookup"><span data-stu-id="2cb89-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="2cb89-108">Lagerbirgðir</span><span class="sxs-lookup"><span data-stu-id="2cb89-108">On-hand inventory</span></span>

<span data-ttu-id="2cb89-109">Í Dynamics 365 Sales hefur verið bætt nýjum **Lagerbirgðir** hnapp við hausinn á síðunum **Tilboð**, **Pantanir** og **Reikningar**.</span><span class="sxs-lookup"><span data-stu-id="2cb89-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="2cb89-110">Þegar þessi hnappur er valinn birtist svargluggi þar sem hægt er að tilgreina fyrirtækið og afurðina sem athuga á lagerbirgðir á.</span><span class="sxs-lookup"><span data-stu-id="2cb89-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="2cb89-111">Þessi gluggi sýnir sömu upplýsingar og [Lagerbirgðir](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="2cb89-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="2cb89-112">Glugginn skilar birgðaupplýsingum úr Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2cb89-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="2cb89-113">Þessar upplýsingar innihalda eftirfarandi magn:</span><span class="sxs-lookup"><span data-stu-id="2cb89-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="2cb89-114">Lagerbirgðir</span><span class="sxs-lookup"><span data-stu-id="2cb89-114">On-hand quantity</span></span>
- <span data-ttu-id="2cb89-115">Frátekið magn á lager</span><span class="sxs-lookup"><span data-stu-id="2cb89-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="2cb89-116">Tiltækt magn á lager</span><span class="sxs-lookup"><span data-stu-id="2cb89-116">Available on-hand quantity</span></span>
- <span data-ttu-id="2cb89-117">Pantað magn</span><span class="sxs-lookup"><span data-stu-id="2cb89-117">Ordered quantity</span></span>
- <span data-ttu-id="2cb89-118">Magn í pöntun</span><span class="sxs-lookup"><span data-stu-id="2cb89-118">On-order quantity</span></span>
- <span data-ttu-id="2cb89-119">Frátekið pantað magn</span><span class="sxs-lookup"><span data-stu-id="2cb89-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="2cb89-120">Heildarmagn tiltækt</span><span class="sxs-lookup"><span data-stu-id="2cb89-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="2cb89-121">ATP-upplýsingar</span><span class="sxs-lookup"><span data-stu-id="2cb89-121">ATP information</span></span>

<span data-ttu-id="2cb89-122">Í Sales hefur nýjum hnappi **ATP-upplýsinga** verið bætt við vörulínur á síðunum **Tilboð**, **Pantanir** og **Reikningar**.</span><span class="sxs-lookup"><span data-stu-id="2cb89-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="2cb89-123">Þegar þessi hnappur er valinn birtist svargluggi þar sem hægt er að tilgreina fyrirtækið, afurðina, birgðasvæðið, vöruhúsið og pöntunarmagnið.</span><span class="sxs-lookup"><span data-stu-id="2cb89-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="2cb89-124">Þessi gluggi hefur sömu stillingarnar og lýst er í [Pöntun lofað](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="2cb89-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="2cb89-125">Glugginn skilar ATP upplýsingum frá Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2cb89-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="2cb89-126">Þessar upplýsingar innihalda eftirfarandi magn:</span><span class="sxs-lookup"><span data-stu-id="2cb89-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="2cb89-127">ATP-magn</span><span class="sxs-lookup"><span data-stu-id="2cb89-127">ATP quantity</span></span>
- <span data-ttu-id="2cb89-128">Magn innhreyfingar</span><span class="sxs-lookup"><span data-stu-id="2cb89-128">Receipt quantity</span></span>
- <span data-ttu-id="2cb89-129">Magn úthreyfingar</span><span class="sxs-lookup"><span data-stu-id="2cb89-129">Issue quantity</span></span>
- <span data-ttu-id="2cb89-130">Lagerbirgðir</span><span class="sxs-lookup"><span data-stu-id="2cb89-130">On-hand quantity</span></span>
