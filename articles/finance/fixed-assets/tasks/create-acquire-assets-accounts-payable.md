---
title: Stofna og komast yfir eignir viðskiptaskuldir
description: Þessi leiðarvísir fer í gegnum stofnun og kaup eignar með innkaupaferlið.
author: saraschi2
manager: AnnBe
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb7c92fcab622109b01590d4acadce0d707d3d2d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227089"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a><span data-ttu-id="92feb-103">Stofna og komast yfir eignir viðskiptaskuldir</span><span class="sxs-lookup"><span data-stu-id="92feb-103">Create and acquire assets from Accounts payable</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="92feb-104">Þessi leiðarvísir fer í gegnum stofnun og kaup eignar með innkaupaferlið.</span><span class="sxs-lookup"><span data-stu-id="92feb-104">This task guide will walk through creation and acquisition of a fixed asset with the purchasing process.</span></span>  <span data-ttu-id="92feb-105">Hann notar Bókari og starfsmaður viðskiptaskulda Og USMF sýnigögn fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="92feb-105">It uses the Accountant and Accounts payable clerks and the demo company USMF .</span></span>


## <a name="set-fixed-assets-parameters"></a><span data-ttu-id="92feb-106">Stilla færibreytur eigna</span><span class="sxs-lookup"><span data-stu-id="92feb-106">Set Fixed assets parameters</span></span>
1. <span data-ttu-id="92feb-107">Í **skoðunarrúðnni** ferðu í **Kerfseiningar > Fastafjármunir > Uppsetning > Eignafæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="92feb-107">In the **Navigation pane**, go to **Modules > Fixed assets > Setup > Fixed assets parameters**.</span></span>
2. <span data-ttu-id="92feb-108">Útvíkkaðu flýtiflipann **Innkaupapantanir**.</span><span class="sxs-lookup"><span data-stu-id="92feb-108">Expand the **Purchase orders** fastTab.</span></span>
3. <span data-ttu-id="92feb-109">Hakaðu við gátreitinn **Leyfa eignakaup úr Innkaupum**.</span><span class="sxs-lookup"><span data-stu-id="92feb-109">Check the **Allow asset acquisition from Purchasing** checkbox.</span></span>
4. <span data-ttu-id="92feb-110">Merktu við gátreitinn **Stofna eign við bókun innhreyfingarskjals afurða eða reiknings**.</span><span class="sxs-lookup"><span data-stu-id="92feb-110">Check the **Create asset during product receipt or invoice posting** checkbox.</span></span>

## <a name="create-a-new-vendor-invoice"></a><span data-ttu-id="92feb-111">Nýtt reikningur lánardrottins búið til.</span><span class="sxs-lookup"><span data-stu-id="92feb-111">Create a new vendor invoice</span></span>
1. <span data-ttu-id="92feb-112">Í **Skoðunarrúðu** ferðu í **Kerfiseiningar > Viðskiptaskuldir > Vinnusvæði > Reikningsfærsla lánardrottins**.</span><span class="sxs-lookup"><span data-stu-id="92feb-112">In the **Navigation pane**, go to **Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="92feb-113">Smelltu á **Nýr reikningur lánardrottins**.</span><span class="sxs-lookup"><span data-stu-id="92feb-113">Click **New vendor invoice**.</span></span>
3. <span data-ttu-id="92feb-114">Í reitnum **Reikningslykill** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="92feb-114">In the **Invoice account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="92feb-115">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="92feb-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="92feb-116">Í reitinn **Númer** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="92feb-116">In the **Number** field, type a value.</span></span>
6. <span data-ttu-id="92feb-117">Í reitinn **Bókunardagssetning** skal rita dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="92feb-117">In the **Posting date** field, enter a date.</span></span>
7. <span data-ttu-id="92feb-118">Smella á **Bæta við línu**.</span><span class="sxs-lookup"><span data-stu-id="92feb-118">Click **Add line**.</span></span>
8. <span data-ttu-id="92feb-119">Í reitnum **Vörunúmer** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="92feb-119">In the **Item number** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="92feb-120">Hægt er að nota annað hvort vörur ekki á lager eða innkaupaflokkar fyrir eignakaup.</span><span class="sxs-lookup"><span data-stu-id="92feb-120">Either non-stocked items or procurement categories can be used for fixed asset acquisition.</span></span>  
9. <span data-ttu-id="92feb-121">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="92feb-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="92feb-122">Í reitnum **Magn** slærðu inn tölu.</span><span class="sxs-lookup"><span data-stu-id="92feb-122">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="92feb-123">Einnar reikningslínu stofnar einungis eina eign, óháð magni.</span><span class="sxs-lookup"><span data-stu-id="92feb-123">One invoice line will only create one fixed asset, regardless of quantity.</span></span> <span data-ttu-id="92feb-124">Svæðisgildi fyrir magns reiknings verða flutt í magn eignar.</span><span class="sxs-lookup"><span data-stu-id="92feb-124">The invoice quantity field value will be transferred to the fixed asset quantity.</span></span>  
11. <span data-ttu-id="92feb-125">Í reitnum **Einingarverð** skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="92feb-125">In the **Unit price** field, enter a number.</span></span>
12. <span data-ttu-id="92feb-126">Útvíkkaðu flýtiflipann **Upplýsingar um línur**.</span><span class="sxs-lookup"><span data-stu-id="92feb-126">Expand the **Line details** fastTab.</span></span>
13. <span data-ttu-id="92feb-127">Smelltu á flipann **Eignir**.</span><span class="sxs-lookup"><span data-stu-id="92feb-127">Click the **Fixed assets** tab.</span></span>
14. <span data-ttu-id="92feb-128">Hakaðu við gátreitinn **Stofna nýja eign**.</span><span class="sxs-lookup"><span data-stu-id="92feb-128">Check the **Create a new fixed asset** checkbox.</span></span>
15. <span data-ttu-id="92feb-129">Í reitnum **Eignaflokkur** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="92feb-129">In the **Fixed asset group** field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="92feb-130">Veljið eignaflokk til að nota á þegar ný eign er stofnuð, á listanum.</span><span class="sxs-lookup"><span data-stu-id="92feb-130">In the list, select the fixed asset group to be used when creating the new fixed asset.</span></span>
17. <span data-ttu-id="92feb-131">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="92feb-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="92feb-132">Smelltu á **bóka.**</span><span class="sxs-lookup"><span data-stu-id="92feb-132">Click **Post**.</span></span> <span data-ttu-id="92feb-133">Eign verður stofnuð og keypt þegar reikningur er bókaður.</span><span class="sxs-lookup"><span data-stu-id="92feb-133">The fixed asset will be created and acquired when the invoice is posted.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]