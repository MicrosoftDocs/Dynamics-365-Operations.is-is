--- 
title: "Stofna og flytja út greiðslur lánardrottna með ISO20022-greiðslusniði"
description: "Þetta ferli sýnir hvernig á að stofna greiðslulínur í greiðslubók lánardrottins og mynda greiðsluskrá lánardrottins með því að nota dæmi um ISO2022 millifærsla fjármuna."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7cc90bc86cd489b124a806c480632dd53ba47f3f
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="645da-103">Stofna og flytja út greiðslur lánardrottna með ISO20022-greiðslusniði</span><span class="sxs-lookup"><span data-stu-id="645da-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="645da-104">Þetta ferli sýnir hvernig á að stofna greiðslulínur í greiðslubók lánardrottins og mynda greiðsluskrá lánardrottins með því að nota dæmi um ISO2022 millifærsla fjármuna.</span><span class="sxs-lookup"><span data-stu-id="645da-104">This procedure shows how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span> 

<span data-ttu-id="645da-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er DEMF.</span><span class="sxs-lookup"><span data-stu-id="645da-105">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="645da-106">Þetta fimmta ferli af fimm sem sýna greiðsluferlinu lánardrottins með því að nota grunnstillingar fyrir rafræna skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="645da-106">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="645da-107">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="645da-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-payment-lines"></a><span data-ttu-id="645da-108">Stofna greiðslulínur</span><span class="sxs-lookup"><span data-stu-id="645da-108">Create payment lines</span></span>
1. <span data-ttu-id="645da-109">Fara í Viðskiptaskuldir > Greiðslur > Greiðslubók.</span><span class="sxs-lookup"><span data-stu-id="645da-109">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="645da-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="645da-110">Click New.</span></span>
3. <span data-ttu-id="645da-111">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="645da-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="645da-112">Sláið inn eða veldu gildi í reitnum heiti.</span><span class="sxs-lookup"><span data-stu-id="645da-112">In the Name field, enter or select a value.</span></span>
5. <span data-ttu-id="645da-113">Smellið á „Línur“.</span><span class="sxs-lookup"><span data-stu-id="645da-113">Click Lines.</span></span>
6. <span data-ttu-id="645da-114">Smellt er á Greiðslutillögur</span><span class="sxs-lookup"><span data-stu-id="645da-114">Click Payment proposal.</span></span>
7. <span data-ttu-id="645da-115">Smellt er á Stofna greiðslutillögu</span><span class="sxs-lookup"><span data-stu-id="645da-115">Click Create payment proposal.</span></span>
8. <span data-ttu-id="645da-116">Útvíkka Færslur til að taka hluta.</span><span class="sxs-lookup"><span data-stu-id="645da-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="645da-117">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="645da-117">Click Filter.</span></span>
10. <span data-ttu-id="645da-118">Á listanum, veljið línuna fyrir töflu Lánardrottna reitinn fyrir lánardrottnalykil.</span><span class="sxs-lookup"><span data-stu-id="645da-118">In the list, select the row for Vendors table and Vendor account field.</span></span>
11. <span data-ttu-id="645da-119">Í reitinn Skilyrði skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="645da-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="645da-120">Þú getur notað hvaða skilyrði sem er til að velja lánardrottnafærslur til að greiða, í þessu dæmi notaðu DE-001 sem lánardrottnalykil.</span><span class="sxs-lookup"><span data-stu-id="645da-120">You can apply any criteria for selecting vendor transactions to pay, for this example use DE-001 as a vendor account.</span></span>  
12. <span data-ttu-id="645da-121">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="645da-121">Click OK.</span></span>
13. <span data-ttu-id="645da-122">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="645da-122">Click OK.</span></span>
14. <span data-ttu-id="645da-123">Smellt er á Stofna greiðslur.</span><span class="sxs-lookup"><span data-stu-id="645da-123">Click Create payments.</span></span>

## <a name="generate-an-iso20022-payment-file"></a><span data-ttu-id="645da-124">Mynda ISO20022-greiðsluskrá</span><span class="sxs-lookup"><span data-stu-id="645da-124">Generate an ISO20022 payment file</span></span>


