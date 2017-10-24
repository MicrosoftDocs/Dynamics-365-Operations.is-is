--- 
title: "Mynda rafræn skjöl fyrir greiðslur með því að nota skilgreiningu sniðs í rafrænni skýrslugerð (ER)"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur notað skilgreiningarsnið fyrir rafræna skýrslugerð (ER) til að búa til rafræn skjöl til að vinna úr greiðslum."
author: NickSelin
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a5d958d3b55bfa76f3cfbb3c1a289e4e89c49146
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="generate-electronic-documents-for-payments-using-a-format-configuration-for-electronic-reporting-er"></a><span data-ttu-id="90913-103">Mynda rafræn skjöl fyrir greiðslur með því að nota skilgreiningu sniðs í rafrænni skýrslugerð (ER)</span><span class="sxs-lookup"><span data-stu-id="90913-103">Generate electronic documents for payments using a format configuration for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="90913-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur notað skilgreiningarsnið fyrir rafræna skýrslugerð (ER) til að búa til rafræn skjöl til að vinna úr greiðslum.</span><span class="sxs-lookup"><span data-stu-id="90913-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can use a new Electronic reporting (ER) format configuration to generate electronic documents for processing payments.</span></span> <span data-ttu-id="90913-105">Hægt er að framkvæma þessum skrefum í GBSI dæmi fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="90913-105">These steps can be performed in the GBSI sample company.</span></span>

<span data-ttu-id="90913-106">Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu "Stofna skilgreiningu með snið á greiðsluskjali".</span><span class="sxs-lookup"><span data-stu-id="90913-106">To complete these steps, you must first complete the steps in the “Create a configuration with format of payment document” procedure.</span></span>


## <a name="change-the-configuration-of-the-electronic-payment-method"></a><span data-ttu-id="90913-107">Breyta grunnstillingu rafrænu greiðsluaðferðinni</span><span class="sxs-lookup"><span data-stu-id="90913-107">Change the configuration of the electronic payment method</span></span>
1. <span data-ttu-id="90913-108">Fara í Viðskiptakröfur > Greiðsluuppsetning > Greiðsluhættir.</span><span class="sxs-lookup"><span data-stu-id="90913-108">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="90913-109">Víxla hlutanum Skráarsnið til að víkka, ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="90913-109">Toggle the File format section to expand it, if needed.</span></span>
3. <span data-ttu-id="90913-110">Nota Síu á Flýtiræsistikunni til að leita að færslum.</span><span class="sxs-lookup"><span data-stu-id="90913-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="90913-111">Til dæmis síu á í Greiðsluaðferðarsvæðinu með gildið rafræna</span><span class="sxs-lookup"><span data-stu-id="90913-111">For example, filter on the Method of payment field with a value of 'Electronic'.</span></span>
4. <span data-ttu-id="90913-112">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="90913-112">Click Edit.</span></span>
5. <span data-ttu-id="90913-113">Stilla Almenn rafræn skýrslugerð reitinn á Já.</span><span class="sxs-lookup"><span data-stu-id="90913-113">Set the General electronic reporting field to Yes.</span></span>
    * <span data-ttu-id="90913-114">Veldu já til að nota almenna rafræna skýrslumynstrið fyrir myndun greiðsluskráa.</span><span class="sxs-lookup"><span data-stu-id="90913-114">Select Yes to use the General electronic reporting pattern for payment files generation.</span></span>  
6. <span data-ttu-id="90913-115">Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="90913-115">In the Name field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="90913-116">Velja BACS (UK upphugsað) skilgreining á sniði.</span><span class="sxs-lookup"><span data-stu-id="90913-116">Select BACS (UK fictitious) format configuration.</span></span>
8. <span data-ttu-id="90913-117">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="90913-117">Click Save.</span></span>
9. <span data-ttu-id="90913-118">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="90913-118">Close the page.</span></span>

## <a name="test-the-format-of-generated-payment-files"></a><span data-ttu-id="90913-119">Prófa snið greiðsluskráa</span><span class="sxs-lookup"><span data-stu-id="90913-119">Test the format of generated payment files</span></span>
1. <span data-ttu-id="90913-120">Fara í Viðskiptaskuldir > Greiðslur > Greiðslubók.</span><span class="sxs-lookup"><span data-stu-id="90913-120">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="90913-121">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="90913-121">Click New.</span></span>
3. <span data-ttu-id="90913-122">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="90913-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="90913-123">Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="90913-123">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="90913-124">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="90913-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="90913-125">Velja VendPay</span><span class="sxs-lookup"><span data-stu-id="90913-125">Select VendPay.</span></span>  
6. <span data-ttu-id="90913-126">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="90913-126">Click Save.</span></span>
7. <span data-ttu-id="90913-127">Smellið á „Línur“.</span><span class="sxs-lookup"><span data-stu-id="90913-127">Click Lines.</span></span>
8. <span data-ttu-id="90913-128">Í reitinn fyrirtæki skal slá inn „DEMF“.</span><span class="sxs-lookup"><span data-stu-id="90913-128">In the Company field, type 'DEMF'.</span></span>
    * <span data-ttu-id="90913-129">DEMF</span><span class="sxs-lookup"><span data-stu-id="90913-129">DEMF</span></span>  
9. <span data-ttu-id="90913-130">Á Svæðinu reikningur skal tilgreina gildin „DE-01001“.</span><span class="sxs-lookup"><span data-stu-id="90913-130">In the Account field, specify the values 'DE-01001'.</span></span>
    * <span data-ttu-id="90913-131">DE - 01001</span><span class="sxs-lookup"><span data-stu-id="90913-131">DE-01001</span></span>  
10. <span data-ttu-id="90913-132">Slá inn „greiðsla“ í reitinn Lýsing.</span><span class="sxs-lookup"><span data-stu-id="90913-132">In the Description field, type 'Payment'.</span></span>
    * <span data-ttu-id="90913-133">Greiðsla</span><span class="sxs-lookup"><span data-stu-id="90913-133">Payment</span></span>  
11. <span data-ttu-id="90913-134">Í reitnum Debet skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="90913-134">In the Debit field, enter a number.</span></span>
    * <span data-ttu-id="90913-135">1000</span><span class="sxs-lookup"><span data-stu-id="90913-135">1000</span></span>  
12. <span data-ttu-id="90913-136">Smellið á flipann Greiðslu.</span><span class="sxs-lookup"><span data-stu-id="90913-136">Click the Payment tab.</span></span>
13. <span data-ttu-id="90913-137">Í reitnum greiðsluaðferð skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="90913-137">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="90913-138">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="90913-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="90913-139">Velja rafrænt gildi.</span><span class="sxs-lookup"><span data-stu-id="90913-139">Select the Electronic value.</span></span>  
15. <span data-ttu-id="90913-140">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="90913-140">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="90913-141">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="90913-141">Click Save.</span></span>
17. <span data-ttu-id="90913-142">Smelltu á Mynda greiðslur.</span><span class="sxs-lookup"><span data-stu-id="90913-142">Click Generate payments.</span></span>
18. <span data-ttu-id="90913-143">Í reitnum greiðsluaðferð skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="90913-143">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="90913-144">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="90913-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="90913-145">Velja rafrænt gildi.</span><span class="sxs-lookup"><span data-stu-id="90913-145">Select the Electronic value.</span></span>  
20. <span data-ttu-id="90913-146">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="90913-146">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="90913-147">Velja rafrænt gildi.</span><span class="sxs-lookup"><span data-stu-id="90913-147">Select the Electronic value.</span></span>  
21. <span data-ttu-id="90913-148">Í reitinn Skráarheiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="90913-148">In the File name field, type a value.</span></span>
    * <span data-ttu-id="90913-149">Til dæmis, skrifið „greiðsla“.</span><span class="sxs-lookup"><span data-stu-id="90913-149">For example, type 'payments'.</span></span>  
22. <span data-ttu-id="90913-150">Í reitnum Bankareikningur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="90913-150">In the Bank account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="90913-151">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="90913-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="90913-152">Velja GBSI OPER gildi.</span><span class="sxs-lookup"><span data-stu-id="90913-152">Select the value GBSI OPER.</span></span>  
24. <span data-ttu-id="90913-153">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="90913-153">Click OK.</span></span>
25. <span data-ttu-id="90913-154">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="90913-154">Click OK.</span></span>
    * <span data-ttu-id="90913-155">Greina stofnaða greiðsluskrá á XML-sniði.</span><span class="sxs-lookup"><span data-stu-id="90913-155">Analyze the created payment file in XML format.</span></span> <span data-ttu-id="90913-156">Bera saman við hannað útlit skjals og færslueigindir skilgreinda greiðslu.</span><span class="sxs-lookup"><span data-stu-id="90913-156">Compare it with the designed document layout and defined payment transaction attributes.</span></span>  


