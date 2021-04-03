---
title: Birgðir til ráðstöfunar í tvíritun
description: Í þessu efnisatriði eru veittar upplýsingar um hvernig skuli athuga birgðir til ráðstöfunar í tvíritun.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 48e54c043967ea5db15938857bd8f020dd4dfc64
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566740"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="d7114-103">Birgðir til ráðstöfunar í tvíritun</span><span class="sxs-lookup"><span data-stu-id="d7114-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d7114-104">Með því að nota birgðaframboð er hægt að athuga birgðirnar áður en afurð er bætt við síðuna **Tilboð**, **Pantanir** eða **Reikningar** í Microsoft Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="d7114-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations**, **Orders**, or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="d7114-105">Til dæmis eru birgðir athugaðar og uppfyllingardagsetning ákvörðuð sem eitt lykilverk í ferlinu [prospect-to-cash](dual-write-prospect-to-cash.md).</span><span class="sxs-lookup"><span data-stu-id="d7114-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="d7114-106">Ef ekki eru til nægar birgðir er hægt að áætla afhendingardagsetningu sem byggist á áætlaðri birgðamóttöku og vandamálum.</span><span class="sxs-lookup"><span data-stu-id="d7114-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="d7114-107">Einnig er hægt að skoða „hægt að lofa“ upplýsingar um afurðina þar sem hægt er að finna „hægt að lofa“-magnið innan fyrirfram skilgreindra tímamarka.</span><span class="sxs-lookup"><span data-stu-id="d7114-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="d7114-108">Lagerbirgðir</span><span class="sxs-lookup"><span data-stu-id="d7114-108">On-hand inventory</span></span>

<span data-ttu-id="d7114-109">Í Dynamics 365 Sales hefur verið bætt nýjum **Lagerbirgðir** hnapp við hausinn á síðunum **Tilboð**, **Pantanir** og **Reikningar**.</span><span class="sxs-lookup"><span data-stu-id="d7114-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="d7114-110">Þegar þessi hnappur er valinn birtist svargluggi þar sem hægt er að tilgreina fyrirtækið og afurðina sem athuga á lagerbirgðir á.</span><span class="sxs-lookup"><span data-stu-id="d7114-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="d7114-111">Þessi gluggi sýnir sömu upplýsingar og [Lagerbirgðir](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="d7114-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="d7114-112">Glugginn skilar birgðaupplýsingum úr Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d7114-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="d7114-113">Þessar upplýsingar innihalda eftirfarandi magn:</span><span class="sxs-lookup"><span data-stu-id="d7114-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="d7114-114">Lagerbirgðir</span><span class="sxs-lookup"><span data-stu-id="d7114-114">On-hand quantity</span></span>
- <span data-ttu-id="d7114-115">Frátekið magn á lager</span><span class="sxs-lookup"><span data-stu-id="d7114-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="d7114-116">Tiltækt magn á lager</span><span class="sxs-lookup"><span data-stu-id="d7114-116">Available on-hand quantity</span></span>
- <span data-ttu-id="d7114-117">Pantað magn</span><span class="sxs-lookup"><span data-stu-id="d7114-117">Ordered quantity</span></span>
- <span data-ttu-id="d7114-118">Magn í pöntun</span><span class="sxs-lookup"><span data-stu-id="d7114-118">On-order quantity</span></span>
- <span data-ttu-id="d7114-119">Frátekið pantað magn</span><span class="sxs-lookup"><span data-stu-id="d7114-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="d7114-120">Heildarmagn tiltækt</span><span class="sxs-lookup"><span data-stu-id="d7114-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="d7114-121">ATP-upplýsingar</span><span class="sxs-lookup"><span data-stu-id="d7114-121">ATP information</span></span>

<span data-ttu-id="d7114-122">Í Sales hefur nýjum hnappi **ATP-upplýsinga** verið bætt við vörulínur á síðunum **Tilboð**, **Pantanir** og **Reikningar**.</span><span class="sxs-lookup"><span data-stu-id="d7114-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="d7114-123">Þegar þessi hnappur er valinn birtist svargluggi þar sem hægt er að tilgreina fyrirtækið, afurðina, birgðasvæðið, vöruhúsið og pöntunarmagnið.</span><span class="sxs-lookup"><span data-stu-id="d7114-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="d7114-124">Þessi gluggi hefur sömu stillingarnar og lýst er í [Pöntun lofað](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="d7114-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="d7114-125">Glugginn skilar ATP upplýsingum frá Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d7114-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="d7114-126">Þessar upplýsingar innihalda eftirfarandi magn:</span><span class="sxs-lookup"><span data-stu-id="d7114-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="d7114-127">ATP-magn</span><span class="sxs-lookup"><span data-stu-id="d7114-127">ATP quantity</span></span>
- <span data-ttu-id="d7114-128">Magn innhreyfingar</span><span class="sxs-lookup"><span data-stu-id="d7114-128">Receipt quantity</span></span>
- <span data-ttu-id="d7114-129">Magn úthreyfingar</span><span class="sxs-lookup"><span data-stu-id="d7114-129">Issue quantity</span></span>
- <span data-ttu-id="d7114-130">Lagerbirgðir</span><span class="sxs-lookup"><span data-stu-id="d7114-130">On-hand quantity</span></span>

## <a name="how-it-works"></a><span data-ttu-id="d7114-131">Hvernig það virkar</span><span class="sxs-lookup"><span data-stu-id="d7114-131">How it works</span></span>

<span data-ttu-id="d7114-132">Þegar hnappurinn **Lagerbirgðir** er valinn á síðunni **Tilboð**, **Pantanir** eða **Reikningar** er sjálfkrafa komið á tengingu við API fyrir **Lagerbirgðir**.</span><span class="sxs-lookup"><span data-stu-id="d7114-132">When you select the **On-hand Inventory** button on the **Quotes**, **Orders**, or **Invoices** page, a live dual-write call is made to the **Onhand inventory** API.</span></span> <span data-ttu-id="d7114-133">API reiknar lagerbirgðir fyrir viðkomandi afurð.</span><span class="sxs-lookup"><span data-stu-id="d7114-133">The API calculates the on-hand inventory for the given product.</span></span> <span data-ttu-id="d7114-134">Niðurstaðan er geymd í töflunum **InventCDSInventoryOnHandRequestEntity** og **InventCDSInventoryOnHandEntryEntity** og er svo skrifuð í Dataverse með tvöfaldri skráningu.</span><span class="sxs-lookup"><span data-stu-id="d7114-134">The result is stored in the **InventCDSInventoryOnHandRequestEntity** and **InventCDSInventoryOnHandEntryEntity** tables, and then is written to Dataverse by dual-write.</span></span> <span data-ttu-id="d7114-135">Til að nota þessa virkni þarf að keyra eftirfarandi kort með tvöfaldri skráningu.</span><span class="sxs-lookup"><span data-stu-id="d7114-135">To use this functionality, you need to run the following dual-write maps.</span></span> <span data-ttu-id="d7114-136">Sleppa upphaflegri samstillingu þegar kortin eru keyrð.</span><span class="sxs-lookup"><span data-stu-id="d7114-136">Skip initial synchronization when you run the maps.</span></span>

- <span data-ttu-id="d7114-137">Lagerbirgðafærslur CDS-birgða (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="d7114-137">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>
- <span data-ttu-id="d7114-138">Beiðnir um lager CDS-birgða (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="d7114-138">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

## <a name="templates"></a><span data-ttu-id="d7114-139">Sniðmát</span><span class="sxs-lookup"><span data-stu-id="d7114-139">Templates</span></span>
<span data-ttu-id="d7114-140">Eftirfarandi sniðmát eru í boði fyrir birgðagögn á lager.</span><span class="sxs-lookup"><span data-stu-id="d7114-140">The following templates are available for the exposing the onhand inventory data.</span></span>

<span data-ttu-id="d7114-141">Finance and Operations-smáforrit</span><span class="sxs-lookup"><span data-stu-id="d7114-141">Finance and Operations apps</span></span> | <span data-ttu-id="d7114-142">Forrit viðskiptavinatengsla</span><span class="sxs-lookup"><span data-stu-id="d7114-142">Customer engagement app</span></span> | <span data-ttu-id="d7114-143">lýsing</span><span class="sxs-lookup"><span data-stu-id="d7114-143">Description</span></span> 
---|---|---
[<span data-ttu-id="d7114-144">Lagerbirgðafærslur CDS-birgða</span><span class="sxs-lookup"><span data-stu-id="d7114-144">CDS inventory on-hand entries</span></span>](#145) | <span data-ttu-id="d7114-145">msdyn_inventoryonhandentries</span><span class="sxs-lookup"><span data-stu-id="d7114-145">msdyn_inventoryonhandentries</span></span> |
[<span data-ttu-id="d7114-146">Beiðnir um lager CDS-birgða</span><span class="sxs-lookup"><span data-stu-id="d7114-146">CDS inventory on-hand requests</span></span>](#147) | <span data-ttu-id="d7114-147">msdyn_inventoryonhandrequests</span><span class="sxs-lookup"><span data-stu-id="d7114-147">msdyn_inventoryonhandrequests</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

###  <a name="cds-inventory-on-hand-entries-msdyn_inventoryonhandentries"></a><a name="145"></a><span data-ttu-id="d7114-148">Lagerbirgðafærslur CDS-birgða (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="d7114-148">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>

<span data-ttu-id="d7114-149">Þetta sniðmát samstillir gögn á milli Finance and Operations -forrita og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="d7114-149">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="d7114-150">Svæði í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d7114-150">Finance and Operations field</span></span> | <span data-ttu-id="d7114-151">Gerð vörpunar</span><span class="sxs-lookup"><span data-stu-id="d7114-151">Map type</span></span> | <span data-ttu-id="d7114-152">Reitur viðskiptavinatengsla</span><span class="sxs-lookup"><span data-stu-id="d7114-152">Customer engagement field</span></span> | <span data-ttu-id="d7114-153">Sjálfgildi</span><span class="sxs-lookup"><span data-stu-id="d7114-153">Default value</span></span>
---|---|---|---
`REQUESTID` | = | `msdyn_request.msdyn_requestid` |
`INVENTORYSITEID` | = | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | = | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`AVAILABLEONHANDQUANTITY` | > | `msdyn_availableonhandquantity` |
`AVAILABLEORDEREDQUANTITY` | > | `msdyn_availableorderedquantity` |
`ONHANDQUANTITY` | > | `msdyn_onhandquantity` |
`ONORDERQUANTITY` | > | `msdyn_onorderquantity` |
`ORDEREDQUANTITY` | > | `msdyn_orderedquantity` |
`RESERVEDONHANDQUANTITY` | > | `msdyn_reservedonhandquantity` |
`RESERVEDORDEREDQUANTITY` | > | `msdyn_reservedorderedquantity` |
`TOTALAVAILABLEQUANTITY` | > | `msdyn_totalavailablequantity` |
`ATPDATE` | = | `msdyn_atpdate` |
`ATPQUANTITY` | > | `msdyn_atpquantity` |
`PROJECTEDISSUEQUANTITY` | > | `msdyn_projectedissuequantity` |
`PROJECTEDONHANDQUANTITY` | > | `msdyn_projectedonhandquantity` |
`PROJECTEDRECEIPTQUANTITY` | > | `msdyn_projectedreceiptquantity` |
`ORDERQUANTITY` | > | `msdyn_orderquantity` |
`UNAVAILABLEONHANDQUANTITY` | > | `msdyn_unavailableonhandquantity` |

###  <a name="cds-inventory-on-hand-requests-msdyn_inventoryonhandrequests"></a><a name="147"></a><span data-ttu-id="d7114-154">Beiðnir um lager CDS-birgða (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="d7114-154">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

<span data-ttu-id="d7114-155">Þetta sniðmát samstillir gögn á milli Finance and Operations -forrita og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="d7114-155">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="d7114-156">Svæði í Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d7114-156">Finance and Operations field</span></span> | <span data-ttu-id="d7114-157">Gerð vörpunar</span><span class="sxs-lookup"><span data-stu-id="d7114-157">Map type</span></span> | <span data-ttu-id="d7114-158">Reitur viðskiptavinatengsla</span><span class="sxs-lookup"><span data-stu-id="d7114-158">Customer engagement field</span></span> | <span data-ttu-id="d7114-159">Sjálfgildi</span><span class="sxs-lookup"><span data-stu-id="d7114-159">Default value</span></span>
---|---|---|---
`REQUESTID` | = | `msdyn_requestid` |
`PRODUCTNUMBER` | < | `msdyn_product.msdyn_productnumber` |
`ISATPCALCULATION` | << | `msdyn_isatpcalculation` |
`ORDERQUANTITY` | < | `msdyn_orderquantity` |
`INVENTORYSITEID` | < | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | < | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`REFERENCENUMBER` | < | `msdyn_referencenumber` |
`LINECREATIONSEQUENCENUMBER` | < | `msdyn_linecreationsequencenumber` |






[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]