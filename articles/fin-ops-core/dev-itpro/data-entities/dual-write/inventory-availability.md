---
title: Birgðir til ráðstöfunar í tvíritun
description: Í þessu efnisatriði eru veittar upplýsingar um athugun á birgðaframboði í tvíritun.
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
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426983"
---
# <a name="inventory-availability"></a><span data-ttu-id="79dc8-103">Birgðir til ráðstöfunar</span><span class="sxs-lookup"><span data-stu-id="79dc8-103">Inventory availability</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="79dc8-104">Með því að nota birgðir til ráðstöfunar er hægt að skoða birgðirnar áður en afurð er bætt við skjámyndirnar **Tilboð**, **Pantanir** eða **Reikningar** í líkanadrifnum forritum í Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="79dc8-104">Using inventory availability, you can check your inventory before you add a product into the **Quotes**, **Orders**, or **Invoices** forms in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="79dc8-105">Birgðaskoðun og ákvörðun á uppfyllingardagsetningu er til dæmis lykilþáttur í ferlinu [prospect-to-cash](dual-write-prospect-to-cash.md).</span><span class="sxs-lookup"><span data-stu-id="79dc8-105">For example, checking inventory and determining a fulfullment date is a key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span> <span data-ttu-id="79dc8-106">Ef ekki eru til nægar birgðir er hægt að áætla afhendingardagsetningu sem byggist á áætlaðri birgðamóttöku og vandamálum.</span><span class="sxs-lookup"><span data-stu-id="79dc8-106">If you don't have enough inventory, you can estimate a delivery date based on projected inventory receipts and issues.</span></span> <span data-ttu-id="79dc8-107">Einnig er hægt að skoða „hægt að lofa“ upplýsingar um afurðina þar sem hægt er að finna „hægt að lofa“-magnið innan fyrirfram skilgreindra tímamarka.</span><span class="sxs-lookup"><span data-stu-id="79dc8-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the pre-defined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="79dc8-108">Lagervörur</span><span class="sxs-lookup"><span data-stu-id="79dc8-108">On-hand Inventory</span></span> 

<span data-ttu-id="79dc8-109">Efst á skjámyndunum **Tilboð**, **Pantanir** eða **Reikningar** í Dynamics 365 Sales er nýjum hnapp **Lagerbirgðir** bætt við.</span><span class="sxs-lookup"><span data-stu-id="79dc8-109">In the header of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **On-hand Inventory** is added.</span></span> <span data-ttu-id="79dc8-110">Þegar smellt er á hnappinn birtist svargluggi og hægt er að tilgreina fyrirtækið og afurðina sem á að skoða lagerbirgðir fyrir.</span><span class="sxs-lookup"><span data-stu-id="79dc8-110">When you click the button, a dialog box appears and you can specify the company and the product for which you want to check the on-hand inventory.</span></span> <span data-ttu-id="79dc8-111">Hann skilar birgðaupplýsingum úr Dynamics 365 Supply Chain Management og sýnir sömu upplýsingar og [Lagerbirgðir](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="79dc8-111">It returns the inventory information from Dynamics 365 Supply Chain Management, and shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span> <span data-ttu-id="79dc8-112">Upplýsingarnar innihalda þetta magn:</span><span class="sxs-lookup"><span data-stu-id="79dc8-112">The information includes these quantities:</span></span>

- <span data-ttu-id="79dc8-113">**Magn á lager**</span><span class="sxs-lookup"><span data-stu-id="79dc8-113">**On-hand Quantity**</span></span>
- <span data-ttu-id="79dc8-114">**Frátekið magn á lager**</span><span class="sxs-lookup"><span data-stu-id="79dc8-114">**Reserved On-hand Quantity**</span></span>
- <span data-ttu-id="79dc8-115">**Tiltækt magn á lager**</span><span class="sxs-lookup"><span data-stu-id="79dc8-115">**Available On-hand Quantity**</span></span>
- <span data-ttu-id="79dc8-116">**Pöntunarmagn**</span><span class="sxs-lookup"><span data-stu-id="79dc8-116">**Orderd Quantity**</span></span>
- <span data-ttu-id="79dc8-117">**Magn í pöntun**</span><span class="sxs-lookup"><span data-stu-id="79dc8-117">**On-order Quantity**</span></span>
- <span data-ttu-id="79dc8-118">**Frátekið pantað magn**</span><span class="sxs-lookup"><span data-stu-id="79dc8-118">**Reserved Ordered Quantity**</span></span>
- <span data-ttu-id="79dc8-119">**Heildarmagn tiltækt**</span><span class="sxs-lookup"><span data-stu-id="79dc8-119">**Total Available Quantity**</span></span>

## <a name="atp-information"></a><span data-ttu-id="79dc8-120">ATP-upplýsingar</span><span class="sxs-lookup"><span data-stu-id="79dc8-120">ATP information</span></span>

<span data-ttu-id="79dc8-121">Í vörulínum skjámyndanna **Tilboð**, **Pantanir** eða **Reikningar** í Dynamics 365 Sales er nýjum hnapp **ATP-upplýsingar** bætt við.</span><span class="sxs-lookup"><span data-stu-id="79dc8-121">On line items of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **ATP Information** is added.</span></span> <span data-ttu-id="79dc8-122">Þegar smellt er á hnappinn birtist svargluggi og hægt er að tilgreina fyrirtækið, afurðina, birgðasvæðið, birgðavöruhúsið og pöntunarmagn.</span><span class="sxs-lookup"><span data-stu-id="79dc8-122">When you click the button, a dialog box appears and you can specify the company, product, inventory Site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="79dc8-123">Hann skilar **ATP-upplýsingar** frá Supply Chain Management og birtir stillingar sem útskýrðar eru í [Pöntun lofað](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="79dc8-123">It returns the **ATP Information** from Supply Chain Management and shows the settings descrbed in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span> <span data-ttu-id="79dc8-124">Upplýsingarnar innihalda **ATP-magn**, **Innhreyfingarmagn**, **Úthreyfingarmagn** og **Magn lagerbirgða**.</span><span class="sxs-lookup"><span data-stu-id="79dc8-124">The information includes **ATP quantity**, **Receipt quantity**, **Issue quantity**, and **On-hand quantity**.</span></span>
