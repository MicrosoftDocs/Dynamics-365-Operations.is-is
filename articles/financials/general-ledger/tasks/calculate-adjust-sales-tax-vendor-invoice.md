--- 
title: "Reikna og stilla virðisaukaskatt á reikningi lánardrottins"
description: "Ef upphaflega upprunaskjal sýnir mismunandi skattupphæðir útreiknaðar, er hægt að leiðrétta þessar upphæðir fyrir bókun."
author: ShylaThompson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 1af9228e5efd2cd6e414eebf766bb3475b44a360
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="f31b1-103">Reikna og stilla virðisaukaskatt á reikningi lánardrottins</span><span class="sxs-lookup"><span data-stu-id="f31b1-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f31b1-104">Ef upphaflega upprunaskjal sýnir mismunandi skattupphæðir útreiknaðar, er hægt að leiðrétta þessar upphæðir fyrir bókun.</span><span class="sxs-lookup"><span data-stu-id="f31b1-104">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="f31b1-105">Þetta verkefni notar DEMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="f31b1-105">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="f31b1-106">Fara í Viðskiptaskuldir > Reikningar > Reikningabók.</span><span class="sxs-lookup"><span data-stu-id="f31b1-106">Go to Accounts payable > Invoices > Invoice journal.</span></span>
2. <span data-ttu-id="f31b1-107">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="f31b1-107">Click New.</span></span>
3. <span data-ttu-id="f31b1-108">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="f31b1-108">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f31b1-109">Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f31b1-109">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f31b1-110">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="f31b1-110">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f31b1-111">Smellið á Línur.</span><span class="sxs-lookup"><span data-stu-id="f31b1-111">Click Lines.</span></span>
7. <span data-ttu-id="f31b1-112">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="f31b1-112">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="f31b1-113">Í reitnum Lykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="f31b1-113">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="f31b1-114">Í reitinn Reikningur skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f31b1-114">In the Invoice field, type a value.</span></span>
10. <span data-ttu-id="f31b1-115">Í reitnum Kredit skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="f31b1-115">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="f31b1-116">Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="f31b1-116">In the Offset account field, specify the desired values.</span></span>
12. <span data-ttu-id="f31b1-117">Smellt er á vsk.</span><span class="sxs-lookup"><span data-stu-id="f31b1-117">Click Sales tax.</span></span>
13. <span data-ttu-id="f31b1-118">Færið inn tölu í reitinn Heildarupphæð eiginlegs virðisaukaskatts.</span><span class="sxs-lookup"><span data-stu-id="f31b1-118">In the Total actual sales tax amount field, enter a number.</span></span>
14. <span data-ttu-id="f31b1-119">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="f31b1-119">Click OK.</span></span>
15. <span data-ttu-id="f31b1-120">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="f31b1-120">Click Save.</span></span>
16. <span data-ttu-id="f31b1-121">Smellt er á vsk.</span><span class="sxs-lookup"><span data-stu-id="f31b1-121">Click Sales tax.</span></span>
17. <span data-ttu-id="f31b1-122">Á flipanum Leiðrétting er hægt að leiðrétta vsk-upphæðir fyrir hvern vsk-kóða.</span><span class="sxs-lookup"><span data-stu-id="f31b1-122">On the Adjustment tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
18. <span data-ttu-id="f31b1-123">Smella á Endurstilla rauntölur út frá reiknuðum upphæðum.</span><span class="sxs-lookup"><span data-stu-id="f31b1-123">Click Reset actual from calculated amounts.</span></span>
19. <span data-ttu-id="f31b1-124">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="f31b1-124">Click OK.</span></span>
20. <span data-ttu-id="f31b1-125">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="f31b1-125">Click Save.</span></span>


