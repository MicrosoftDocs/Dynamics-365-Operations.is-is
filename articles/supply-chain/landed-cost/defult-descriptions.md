---
title: Sjálfgefnar lýsingar fyrir fjárhag
description: Hægt er að nota sjálfgefnar lýsingar til að uppfæra lýsingarreitinn í bókun fylgiskjala í fjárhag.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: d5a38af57d614ae2c93b0af74ec4a1c085519d46
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841898"
---
# <a name="default-descriptions-for-the-general-ledger"></a><span data-ttu-id="57c56-103">Sjálfgefnar lýsingar fyrir fjárhag</span><span class="sxs-lookup"><span data-stu-id="57c56-103">Default descriptions for the general ledger</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="57c56-104">Hægt er að nota sjálfgefnar lýsingar til að uppfæra reitinn **Lýsing** í bókun fylgiskjala í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="57c56-104">Default descriptions can be used to update the **Description** field in voucher postings to the general ledger.</span></span> <span data-ttu-id="57c56-105">Verið er að auka þessa virkni þannig að hún virki með Heildarkostnaður.</span><span class="sxs-lookup"><span data-stu-id="57c56-105">This functionality has been enhanced to work with Landed cost.</span></span>

<span data-ttu-id="57c56-106">Til að setja upp sjálfgefnar lýsingar fyrir fjárhagsbókanir skal fara í **Stjórnun fyrirtækis \> Uppsetning \> Sjálfgefnar lýsingar**.</span><span class="sxs-lookup"><span data-stu-id="57c56-106">To set up default descriptions for ledger postings, go to **Organizational administration \> Setup \> Default descriptions**.</span></span>

<span data-ttu-id="57c56-107">Í eftirfarandi töflu er listi yfir ný gildi sem hefur verið bætt við reitinn **Lýsing** á síðunni **Sjálfgefnar lýsingar** til að styðja við heildarkostnað.</span><span class="sxs-lookup"><span data-stu-id="57c56-107">The following table lists the new values that have been added for the **Description** field on the **Default descriptions** page to support Landed cost.</span></span>

| <span data-ttu-id="57c56-108">Gerð lýsingar</span><span class="sxs-lookup"><span data-stu-id="57c56-108">Description type</span></span> | <span data-ttu-id="57c56-109">Athugasemdir</span><span class="sxs-lookup"><span data-stu-id="57c56-109">Notes</span></span> |
|---|---|
| <span data-ttu-id="57c56-110">Flytja inn kostnað – uppsafnaður kostnaður</span><span class="sxs-lookup"><span data-stu-id="57c56-110">Import costing – Cost accrual</span></span> | <span data-ttu-id="57c56-111">Þegar innkaupapöntunarreikningur er bókaður er kostnaðaruppsöfnun unnin fyrir áætlun ferðakostnaðar.</span><span class="sxs-lookup"><span data-stu-id="57c56-111">When a purchase order invoice is posted, a cost accrual is processed for estimate voyage costs.</span></span> <span data-ttu-id="57c56-112">Hægt er að tilgreina sjálfgefnar lýsingar til að bæta ferðanúmeri við lýsinguna.</span><span class="sxs-lookup"><span data-stu-id="57c56-112">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="57c56-113">Nota *%4* fyrir sendingarnúmerið.</span><span class="sxs-lookup"><span data-stu-id="57c56-113">Use *%4* for the shipment number.</span></span> |
| <span data-ttu-id="57c56-114">Flytja inn kostnaðarútreikning – vöruflutningspöntun</span><span class="sxs-lookup"><span data-stu-id="57c56-114">Import costing – Goods in transit order</span></span> | <span data-ttu-id="57c56-115">Ef verið er að nota vinnslu fyrir vörur í flutningi verður innkaupapöntunarreikningurinn bókaður og vörurnar eru bókaðar á vöruflutningalykil.</span><span class="sxs-lookup"><span data-stu-id="57c56-115">If you're using in-transit processing, the purchase order invoice is posted, and the goods are posted to a goods in transit account.</span></span> <span data-ttu-id="57c56-116">Hægt er að tilgreina sjálfgefnar lýsingar til að bæta pöntunarnúmeri í flutningi við lýsinguna.</span><span class="sxs-lookup"><span data-stu-id="57c56-116">Default descriptions can be specified to add the in-transit order number to the description.</span></span> <span data-ttu-id="57c56-117">Nota *%4* fyrir númer pöntunar í flutningi.</span><span class="sxs-lookup"><span data-stu-id="57c56-117">Use *%4* for the in-transit order number.</span></span> |
| <span data-ttu-id="57c56-118">Birgðir - lokun - Leiðrétting</span><span class="sxs-lookup"><span data-stu-id="57c56-118">Inventory – close – adjustment</span></span> | <span data-ttu-id="57c56-119">Þegar reikningur viðskiptaskulda er afgreiddur fyrir kostnað ferðar er unnið úr leiðréttingu á birgðaskrá til að áætla kostnað ferðarinnar.</span><span class="sxs-lookup"><span data-stu-id="57c56-119">When the accounts payable (AP) invoice is processed for a voyage cost, an inventory adjustment is processed to estimate voyage costs.</span></span> <span data-ttu-id="57c56-120">Hægt er að tilgreina sjálfgefnar lýsingar til að bæta ferðanúmeri við lýsinguna.</span><span class="sxs-lookup"><span data-stu-id="57c56-120">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="57c56-121">Nota *%4* fyrir sendingarnúmerið.</span><span class="sxs-lookup"><span data-stu-id="57c56-121">Use *%4* for the shipment number.</span></span> |

<span data-ttu-id="57c56-122">Frekari upplýsingar um hvernig á að vinna með síðuna **Sjálfgefnar lýsingar** er að finna í [Setja upp sjálfgefnar lýsingar fyrir sjálfvirka bókun](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).</span><span class="sxs-lookup"><span data-stu-id="57c56-122">For more information about how to work with the **Default descriptions** page, see [Set up default descriptions for automatic posting](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).</span></span>
