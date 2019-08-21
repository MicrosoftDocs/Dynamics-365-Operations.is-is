---
title: Stofna og komast yfir eignir viðskiptaskuldir
description: Þessi leiðarvísir fer í gegnum stofnun og kaup eignar með innkaupaferlið.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2626877c907994d03cdae960c8501a858ca214bd
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840026"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a><span data-ttu-id="46a1e-103">Stofna og komast yfir eignir viðskiptaskuldir</span><span class="sxs-lookup"><span data-stu-id="46a1e-103">Create and acquire assets from Accounts payable</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="46a1e-104">Þessi leiðarvísir fer í gegnum stofnun og kaup eignar með innkaupaferlið.</span><span class="sxs-lookup"><span data-stu-id="46a1e-104">This task guide will walk through creation and acquisition of a fixed asset with the purchasing process.</span></span>  <span data-ttu-id="46a1e-105">Hann notar Bókari og starfsmaður viðskiptaskulda Og USMF sýnigögn fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="46a1e-105">It uses the Accountant and Accounts payable clerks and the demo company USMF .</span></span>


## <a name="set-fixed-assets-parameters"></a><span data-ttu-id="46a1e-106">Stilla færibreytur eigna</span><span class="sxs-lookup"><span data-stu-id="46a1e-106">Set Fixed assets parameters</span></span>
1. <span data-ttu-id="46a1e-107">Fara í Eignir > Uppsetning > Færibreytur eigna.</span><span class="sxs-lookup"><span data-stu-id="46a1e-107">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="46a1e-108">Útvíkka eða draga saman hlutanum innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="46a1e-108">Expand or collapse the Purchase orders section.</span></span>
3. <span data-ttu-id="46a1e-109">Merkja við Innkaupagátreit Leyfa eignakaup úr .</span><span class="sxs-lookup"><span data-stu-id="46a1e-109">Check the Allow asset acquisition from Purchasing checkbox.</span></span>
4. <span data-ttu-id="46a1e-110">Merktu við gátreið Stofna eign á meðan innhreyfingarskjal afurða eða bókun reiknings.</span><span class="sxs-lookup"><span data-stu-id="46a1e-110">Check the Create asset during product receipt or invoice posting checkbox.</span></span>

## <a name="create-a-new-vendor-invoice"></a><span data-ttu-id="46a1e-111">Nýtt reikningur lánardrottins búið til.</span><span class="sxs-lookup"><span data-stu-id="46a1e-111">Create a new vendor invoice</span></span>
1. <span data-ttu-id="46a1e-112">Fara í Viðskiptaskuldir > Vinnusvæði > Færsla fyrir reikning lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="46a1e-112">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="46a1e-113">Smellt er á Nýtt reikning lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="46a1e-113">Click New vendor invoice.</span></span>
3. <span data-ttu-id="46a1e-114">Í reitnum reikningslykill skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="46a1e-114">In the Invoice account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="46a1e-115">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="46a1e-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="46a1e-116">Í reitnum Númer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="46a1e-116">In the Number field, type a value.</span></span>
6. <span data-ttu-id="46a1e-117">Dagsetning er rituð í reitinn Bókunardagssetning.</span><span class="sxs-lookup"><span data-stu-id="46a1e-117">In the Posting date field, enter a date.</span></span>
7. <span data-ttu-id="46a1e-118">Smellið á „Bæta við línu“.</span><span class="sxs-lookup"><span data-stu-id="46a1e-118">Click Add line.</span></span>
8. <span data-ttu-id="46a1e-119">Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="46a1e-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="46a1e-120">Hægt er að nota annað hvort vörur ekki á lager eða innkaupaflokkar fyrir eignakaup.</span><span class="sxs-lookup"><span data-stu-id="46a1e-120">Either non-stocked items or procurement categories can be used for fixed asset acquisition.</span></span>  
9. <span data-ttu-id="46a1e-121">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="46a1e-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="46a1e-122">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="46a1e-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="46a1e-123">Einnar reikningslínu stofnar einungis eina eign, óháð magni.</span><span class="sxs-lookup"><span data-stu-id="46a1e-123">One invoice line will only create one fixed asset, regardless of quantity.</span></span>  <span data-ttu-id="46a1e-124">Svæðisgildi fyrir magns reiknings verða flutt í magn eignar.</span><span class="sxs-lookup"><span data-stu-id="46a1e-124">The invoice quantity field value will be transferred to the fixed asset quantity.</span></span>  
11. <span data-ttu-id="46a1e-125">Færið inn númer í reitnum „Einingarverð“.</span><span class="sxs-lookup"><span data-stu-id="46a1e-125">In the Unit price field, enter a number.</span></span>
12. <span data-ttu-id="46a1e-126">Útvíkka eða draga saman hluta upplýsingar Línu.</span><span class="sxs-lookup"><span data-stu-id="46a1e-126">Expand or collapse the Line details section.</span></span>
13. <span data-ttu-id="46a1e-127">Smellið á flipann eigna.</span><span class="sxs-lookup"><span data-stu-id="46a1e-127">Click the Fixed assets tab.</span></span>
14. <span data-ttu-id="46a1e-128">Merktu við gátreit Stofna nýja eign.</span><span class="sxs-lookup"><span data-stu-id="46a1e-128">Check the Create a new fixed asset checkbox.</span></span>
15. <span data-ttu-id="46a1e-129">Í reitnum eignaflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="46a1e-129">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="46a1e-130">Veljið eignaflokk til að nota á þegar ný eign er stofnuð, á listanum.</span><span class="sxs-lookup"><span data-stu-id="46a1e-130">In the list, select the fixed asset group to be used when creating the new fixed asset.</span></span>
17. <span data-ttu-id="46a1e-131">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="46a1e-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="46a1e-132">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="46a1e-132">Click Post.</span></span>
    * <span data-ttu-id="46a1e-133">Eign verður stofnuð og keypt þegar reikningur er bókaður.</span><span class="sxs-lookup"><span data-stu-id="46a1e-133">The fixed asset will be created and acquired when the invoice is posted.</span></span>  

