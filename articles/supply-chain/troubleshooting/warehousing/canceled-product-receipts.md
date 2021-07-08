---
title: Innhreyfingarskjöl afurða sem hætt var við uppfæra ekki færslustöðu í skráð
description: Eftir að hætt er við innhreyfingarskjöl afurða í hleðslu á innleið uppfærir kerfið sjálfkrafa stöðu birgðafærslunnar úr móttekið í pantað.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c86457d50a7a9ac2a699a0e0a9c7bdf4cd7c67b
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294099"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a><span data-ttu-id="8dc79-103">Innhreyfingarskjöl afurða sem hætt var við uppfæra ekki færslustöðu í skráð</span><span class="sxs-lookup"><span data-stu-id="8dc79-103">Canceled product receipts don't update transaction status to Registered</span></span>

## <a name="symptoms"></a><span data-ttu-id="8dc79-104">Einkenni</span><span class="sxs-lookup"><span data-stu-id="8dc79-104">Symptoms</span></span>

<span data-ttu-id="8dc79-105">Þegar aðgerðin **Hætta við innhreyfingarskjöl afurða** hefur verið keyrð uppfærir kerfið sjálfkrafa stöðu birgðafærslna úr *Móttekið* í *Pantað*.</span><span class="sxs-lookup"><span data-stu-id="8dc79-105">After you run the **Cancel product receipts** action on an inbound load, the system automatically updates the status of inventory transactions from *Received* to *Ordered*.</span></span>

## <a name="resolution"></a><span data-ttu-id="8dc79-106">Lausn</span><span class="sxs-lookup"><span data-stu-id="8dc79-106">Resolution</span></span>

<span data-ttu-id="8dc79-107">Þegar hætt er við fylgiseðla fyrir hleðslur á útleið helst staða birgðafærslna óbreytt í *Tekið til*.</span><span class="sxs-lookup"><span data-stu-id="8dc79-107">When packing slips are canceled for outbound loads, the status of inventory transactions remains *Picked*.</span></span> <span data-ttu-id="8dc79-108">Hinsvegar þegar hætt er við innhreyfingarskjöl afurða úr hleðslu á innleið er staða birgðafærslna ekki endurheimt í *Skráð*.</span><span class="sxs-lookup"><span data-stu-id="8dc79-108">However, when product receipts from an inbound load are canceled, the status of inventory transactions isn't restored to *Registered*.</span></span> <span data-ttu-id="8dc79-109">Þar af leiðandi, eftir að hætt er við innhreyfingarskjal afurðar úr hleðslu á innleið, verður starfsmaður í vöruhúsi að endurskrá vörumagnið fyrir hleðslurnar.</span><span class="sxs-lookup"><span data-stu-id="8dc79-109">Therefore, after a product receipt from an inbound load is canceled, the warehouse worker must re-register item quantities for the loads.</span></span>

<span data-ttu-id="8dc79-110">Frekari upplýsingar er að finna í [Skrá vörumagn sem kemur með hleðslu á innleið](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).</span><span class="sxs-lookup"><span data-stu-id="8dc79-110">For more information, see [Register item quantities that arrive on an inbound load](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).</span></span>
