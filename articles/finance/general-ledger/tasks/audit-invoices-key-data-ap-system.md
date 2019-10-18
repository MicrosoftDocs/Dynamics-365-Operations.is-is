---
title: Endurskoða reikninga og lykilgögn í viðskiptaskuldakerfi
description: Þegar reikningur er móttekinn frá lánardrottni fyrir vörur eða þjónustu á innkaupapöntun gætu viðskiptaferlin krafist þess að vörurnar eða þjónustan séu mótteknar áður en hægt er að samþykkja reikninginn til greiðslu.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c6e8967fe4db67ff98fc7093792bdb82b73a33d9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178229"
---
# <a name="audit-invoices-and-key-data-in-ap-system"></a><span data-ttu-id="f5782-103">Endurskoða reikninga og lykilgögn í viðskiptaskuldakerfi</span><span class="sxs-lookup"><span data-stu-id="f5782-103">Audit invoices and key data in AP system</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f5782-104">Þegar reikningur er móttekinn frá lánardrottni fyrir vörur eða þjónustu á innkaupapöntun gætu viðskiptaferlin krafist þess að vörurnar eða þjónustan séu mótteknar áður en hægt er að samþykkja reikninginn til greiðslu.</span><span class="sxs-lookup"><span data-stu-id="f5782-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="f5782-105">Áður en hafist er handa þarf að ganga úr skugga um að skilgreiningarlykill reikningsjöfnunar sé valinn.</span><span class="sxs-lookup"><span data-stu-id="f5782-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="f5782-106">Á síðunni færibreytum viðskiptaskulda, skal tryggja að valkosturinn Virkja sannprófun á reikningsjöfnun sé valinn, svæðið Bóka reikning með misræmi er stillt til að Krefjast samþykkis, og svæðið Línujöfnunarregla er stillt á þríhliða jöfnun.</span><span class="sxs-lookup"><span data-stu-id="f5782-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="f5782-107">Þessi aðferð notar sýnigögn USMF fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="f5782-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="f5782-108">hlutverk viðskiptaskuldastjóri eða aðalbókari myndi framkvæma þessi skrefum.</span><span class="sxs-lookup"><span data-stu-id="f5782-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="f5782-109">Stofna innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="f5782-109">Create a purchase order</span></span>
1. <span data-ttu-id="f5782-110">Opnið **Allar innkaupapantanir**.</span><span class="sxs-lookup"><span data-stu-id="f5782-110">Go to **All purchase orders**.</span></span>
2. <span data-ttu-id="f5782-111">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="f5782-111">Click **New**.</span></span>
3. <span data-ttu-id="f5782-112">Í svæðinu **Lánardrottnalykill** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f5782-112">In the **Vendor account** field, type a value.</span></span>
4. <span data-ttu-id="f5782-113">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f5782-113">Click **OK**.</span></span>
5. <span data-ttu-id="f5782-114">Smella á **Bæta við línu**.</span><span class="sxs-lookup"><span data-stu-id="f5782-114">Click **Add line**.</span></span>
6. <span data-ttu-id="f5782-115">Í reitnum **Vörunúmer** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f5782-115">In the **Item number** field, type a value.</span></span>
7. <span data-ttu-id="f5782-116">Í aðgerðasvæðinu skal smella á **Innkaup**.</span><span class="sxs-lookup"><span data-stu-id="f5782-116">On the Action Pane, click **Purchase**.</span></span>
8. <span data-ttu-id="f5782-117">Smellið á **Staðfesta**.</span><span class="sxs-lookup"><span data-stu-id="f5782-117">Click **Confirm**.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="f5782-118">Bóka innhreyfingarskjal afurða</span><span class="sxs-lookup"><span data-stu-id="f5782-118">Post a product receipt</span></span>
1. <span data-ttu-id="f5782-119">Í aðgerðasvæðinu skal smella á **Móttaka**.</span><span class="sxs-lookup"><span data-stu-id="f5782-119">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="f5782-120">Smellið á **Innhreyfingarskjal afurða**.</span><span class="sxs-lookup"><span data-stu-id="f5782-120">Click **Product receipt**.</span></span>
3. <span data-ttu-id="f5782-121">Í reitinn **Innhreyfingarskjal afurða** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f5782-121">In the **Product receipt** field, type a value.</span></span>
4. <span data-ttu-id="f5782-122">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f5782-122">Click **OK**.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="f5782-123">Skráðu og jafnaðu reikningu lánardrottins við innhreyfingarskjal afurða</span><span class="sxs-lookup"><span data-stu-id="f5782-123">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="f5782-124">Í aðgerðasvæðinu er smellt á **Reikningur > Reikningur**.</span><span class="sxs-lookup"><span data-stu-id="f5782-124">On the Action Pane, click **Invoice > Invoice**.</span></span>
2. <span data-ttu-id="f5782-125">Í reitinn **Númer** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f5782-125">In the **Number** field, type a value.</span></span>
3. <span data-ttu-id="f5782-126">Smellið á **Sjálfgefið úr: Pantað magn** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="f5782-126">Click **Default from: Ordered quantity** to open the drop dialog.</span></span>
4. <span data-ttu-id="f5782-127">Í reitnum **Sjálfgefið magn fyrir línur** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="f5782-127">In the **Default quantity for lines** field, select an option.</span></span>
5. <span data-ttu-id="f5782-128">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f5782-128">Click **OK**.</span></span>
6. <span data-ttu-id="f5782-129">Smellið á **Já**.</span><span class="sxs-lookup"><span data-stu-id="f5782-129">Click **Yes**.</span></span>
7. <span data-ttu-id="f5782-130">Smellið á **Jafna innhreyfingarskjöl afurða**.</span><span class="sxs-lookup"><span data-stu-id="f5782-130">Click **Match product receipts**.</span></span>
8. <span data-ttu-id="f5782-131">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f5782-131">Click **OK**.</span></span>
9. <span data-ttu-id="f5782-132">Í aðgerðasvæðinu skal smella á **Yfirfara**.</span><span class="sxs-lookup"><span data-stu-id="f5782-132">On the Action Pane, click **Review**.</span></span>
10. <span data-ttu-id="f5782-133">Smellið á **Samsvörunarupplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="f5782-133">Click **Matching details**.</span></span>

