--- 
title: "Skrá reikning lánardrottins og samsvara við móttekið magn"
description: "Þegar reikningur er móttekinn frá lánardrottni fyrir vörur eða þjónustu á innkaupapöntun gætu viðskiptaferlin krafist þess að vörurnar eða þjónustan séu mótteknar áður en hægt er að samþykkja reikninginn til greiðslu."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2247edfd803ce238b3b7ca57d9d47dda9c3b0cae
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a><span data-ttu-id="6384a-103">Skrá reikning lánardrottins og samsvara við móttekið magn</span><span class="sxs-lookup"><span data-stu-id="6384a-103">Record vendor invoice and match against received quantity</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6384a-104">Þegar reikningur er móttekinn frá lánardrottni fyrir vörur eða þjónustu á innkaupapöntun gætu viðskiptaferlin krafist þess að vörurnar eða þjónustan séu mótteknar áður en hægt er að samþykkja reikninginn til greiðslu.</span><span class="sxs-lookup"><span data-stu-id="6384a-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="6384a-105">Áður en hafist er handa þarf að ganga úr skugga um að skilgreiningarlykill reikningsjöfnunar sé valinn.</span><span class="sxs-lookup"><span data-stu-id="6384a-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="6384a-106">Á síðunni færibreytum viðskiptaskulda, skal tryggja að valkosturinn Virkja sannprófun á reikningsjöfnun sé valinn, svæðið Bóka reikning með misræmi er stillt til að Krefjast samþykkis, og svæðið Línujöfnunarregla er stillt á þríhliða jöfnun.</span><span class="sxs-lookup"><span data-stu-id="6384a-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="6384a-107">Þessi aðferð notar sýnigögn USMF fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="6384a-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="6384a-108">hlutverk viðskiptaskuldastjóri eða aðalbókari myndi framkvæma þessi skrefum.</span><span class="sxs-lookup"><span data-stu-id="6384a-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="6384a-109">Stofna innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="6384a-109">Create a purchase order</span></span>
1. <span data-ttu-id="6384a-110">Fara í Allar innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="6384a-110">Go to All purchase orders.</span></span>
2. <span data-ttu-id="6384a-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="6384a-111">Click New.</span></span>
3. <span data-ttu-id="6384a-112">Í reitnum Lánardrottnalykill skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="6384a-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="6384a-113">Í svæðinu Lánardrottnalykill skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="6384a-113">In the Vendor account field, type a value.</span></span>
5. <span data-ttu-id="6384a-114">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="6384a-114">Click OK.</span></span>
6. <span data-ttu-id="6384a-115">Smellið á „Bæta við línu“.</span><span class="sxs-lookup"><span data-stu-id="6384a-115">Click Add line.</span></span>
7. <span data-ttu-id="6384a-116">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="6384a-116">In the Item number field, type a value.</span></span>
8. <span data-ttu-id="6384a-117">Smellið á „Innkaup“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="6384a-117">On the Action Pane, click Purchase.</span></span>
9. <span data-ttu-id="6384a-118">Smellið á „Staðfesta“.</span><span class="sxs-lookup"><span data-stu-id="6384a-118">Click Confirm.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="6384a-119">Bóka innhreyfingarskjal afurða</span><span class="sxs-lookup"><span data-stu-id="6384a-119">Post a product receipt</span></span>
1. <span data-ttu-id="6384a-120">Smellið á „Móttaka“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="6384a-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="6384a-121">Smellið á „Innhreyfingarskjal“.</span><span class="sxs-lookup"><span data-stu-id="6384a-121">Click Product receipt.</span></span>
3. <span data-ttu-id="6384a-122">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="6384a-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="6384a-123">Í reitinn innhreyfingarskjal afurða skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="6384a-123">In the Product receipt field, type a value.</span></span>
5. <span data-ttu-id="6384a-124">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="6384a-124">Click OK.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="6384a-125">Skráðu og jafnaðu reikningu lánardrottins við innhreyfingarskjal afurða</span><span class="sxs-lookup"><span data-stu-id="6384a-125">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="6384a-126">Smellið á „Reikningur“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="6384a-126">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="6384a-127">Smellið á „Reikningur“.</span><span class="sxs-lookup"><span data-stu-id="6384a-127">Click Invoice.</span></span>
3. <span data-ttu-id="6384a-128">Í reitnum Númer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="6384a-128">In the Number field, type a value.</span></span>
4. <span data-ttu-id="6384a-129">Smellt er á Sjálfgefið úr: Pantað magn til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="6384a-129">Click Default from: Ordered quantity to open the drop dialog.</span></span>
5. <span data-ttu-id="6384a-130">Í reitnum sjálfgefið magn fyrir línur skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="6384a-130">In the Default quantity for lines field, select an option.</span></span>
6. <span data-ttu-id="6384a-131">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="6384a-131">Click OK.</span></span>
7. <span data-ttu-id="6384a-132">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="6384a-132">Click Yes.</span></span>
8. <span data-ttu-id="6384a-133">Smellt er á Jafna innhreyfingarskjöl afurða.</span><span class="sxs-lookup"><span data-stu-id="6384a-133">Click Match product receipts.</span></span>
9. <span data-ttu-id="6384a-134">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="6384a-134">Click OK.</span></span>
10. <span data-ttu-id="6384a-135">Smellið á „Yfirfara“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="6384a-135">On the Action Pane, click Review.</span></span>
11. <span data-ttu-id="6384a-136">Smellið á „Samsvörunarupplýsingar“.</span><span class="sxs-lookup"><span data-stu-id="6384a-136">Click Matching details.</span></span>


