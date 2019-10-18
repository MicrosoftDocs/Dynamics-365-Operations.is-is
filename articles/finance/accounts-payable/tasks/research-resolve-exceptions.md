---
title: Rannsaka/leysa úr undantekningum
description: Reikningsreglur lánardrottins eru keyrðar þegar reikningur lánardrottins er bókaður með því að nota síðuna fyrir reikning Lánardrottins og þegar síðan fyrir brot á reikningsreglum lánardrottins er opnuð.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2f2e7d401e97aeab9dbc74f65e1a0c03eb0c880
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189339"
---
# <a name="researchresolve-exceptions"></a><span data-ttu-id="c6fe6-103">Rannsaka/leysa úr undantekningum</span><span class="sxs-lookup"><span data-stu-id="c6fe6-103">Research/Resolve exceptions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c6fe6-104">Reikningsreglur lánardrottins eru keyrðar þegar reikningur lánardrottins er bókaður með því að nota síðuna fyrir reikning Lánardrottins og þegar síðan fyrir brot á reikningsreglum lánardrottins er opnuð.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-104">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="c6fe6-105">Einnig er hægt að skilgreina verkflæði fyrir reikning lánardrottins til að keyra reikningsreglur lánardrottins í hvert skipti sem er sendur er reikning til verkflæðis.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-105">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

<span data-ttu-id="c6fe6-106">Reikningsreglur lánardrottins eiga ekki við reikninga sem voru stofnaðar í komubók eða reikningabók.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-106">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span> 

<span data-ttu-id="c6fe6-107">Sannprófun á reikningsjöfnun notar ekki reikningsreglur lánardrottins, en er í staðinn sett upp á síðunni færibreytur viðskiptaskulda.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-107">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>

<span data-ttu-id="c6fe6-108">Þessi skráning notar sýnigögn USMF fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="c6fe6-108">This recording uses the USMF demo company.</span></span> <span data-ttu-id="c6fe6-109">hlutverk viðskiptaskuldastjóri eða aðalbókari myndi framkvæma þessi skrefum.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-109">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="c6fe6-110">Áður en hafist er handa þarf að ganga úr skugga um að skilgreiningarlykill reikningsjöfnunar sé valinn.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-110">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="c6fe6-111">Undirbúa stofnun stefna um reikninga lánardrottins</span><span class="sxs-lookup"><span data-stu-id="c6fe6-111">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="c6fe6-112">Fara í Viðskiptaskuldir > Uppsetning > Færibreytur viðskiptaskulda.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-112">Go to Accounts payable > Setup > Accounts payable parameters.</span></span>
2. <span data-ttu-id="c6fe6-113">Smellið á flipann Staðfesting reiknings.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-113">Click the Invoice validation tab.</span></span>
3. <span data-ttu-id="c6fe6-114">Veldu eða hreinsaðu gátreitinn uppfæra sjálfvirkt stöðu fyrirsögn reiknings.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-114">Select or clear the Automatically update invoice header status check box.</span></span>
4. <span data-ttu-id="c6fe6-115">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-115">Click OK.</span></span>
5. <span data-ttu-id="c6fe6-116">Í svæðinu Bóka reikning með misræmi skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-116">In the Post invoice with discrepancies field, select an option.</span></span>
6. <span data-ttu-id="c6fe6-117">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-117">Close the page.</span></span>
7. <span data-ttu-id="c6fe6-118">Fara í Viðskiptaskuldir > Uppsetning reglu > Reikningsreglur lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-118">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
8. <span data-ttu-id="c6fe6-119">Smellt er á Færibreytum.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-119">Click Parameters.</span></span>
9. <span data-ttu-id="c6fe6-120">Smellt er á btnAdd.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-120">Click btnAdd.</span></span>
10. <span data-ttu-id="c6fe6-121">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-121">Close the page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="c6fe6-122">Stofna stefnureglugerðir fyrir reikninga lánardrottins</span><span class="sxs-lookup"><span data-stu-id="c6fe6-122">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="c6fe6-123">Fara í Viðskiptaskuldir > Uppsetning reglu > Stefna fyrir reikning lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-123">Go to Accounts payable > Policy setup > Vendor invoice policy rule types.</span></span>
2. <span data-ttu-id="c6fe6-124">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-124">Click New.</span></span>
3. <span data-ttu-id="c6fe6-125">Í reitinn Nafn reglu skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-125">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="c6fe6-126">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-126">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c6fe6-127">Í reitnum Heiti fyrirspurnar skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-127">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="c6fe6-128">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-128">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="c6fe6-129">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-129">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="c6fe6-130">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-130">Click Save.</span></span>
9. <span data-ttu-id="c6fe6-131">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-131">Close the page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="c6fe6-132">Skilgreina stefna fyrir reikning lánardrottins</span><span class="sxs-lookup"><span data-stu-id="c6fe6-132">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="c6fe6-133">Fara í Viðskiptaskuldir > Uppsetning reglu > Reikningsreglur lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-133">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
2. <span data-ttu-id="c6fe6-134">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-134">Click New.</span></span>
3. <span data-ttu-id="c6fe6-135">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-135">In the Name field, type a value.</span></span>
4. <span data-ttu-id="c6fe6-136">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-136">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c6fe6-137">Útvíkka eða draga saman hlutann fyrirtækisregla</span><span class="sxs-lookup"><span data-stu-id="c6fe6-137">Expand or collapse the Policy organizations section.</span></span>
6. <span data-ttu-id="c6fe6-138">Veljið 'Contoso Entertainment System USA', í trénu.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-138">In the tree, select 'Contoso Entertainment System USA'.</span></span>
7. <span data-ttu-id="c6fe6-139">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-139">Click Add.</span></span>
8. <span data-ttu-id="c6fe6-140">Útvíkka eða draga saman hlutann stefnuregla.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-140">Expand or collapse the Policy rules section.</span></span>
9. <span data-ttu-id="c6fe6-141">Smellt er á Stofna stefnureglu.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-141">Click Create policy rule.</span></span>
10. <span data-ttu-id="c6fe6-142">Í reitinn Lýsing stefnuregla skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-142">In the Policy rule description field, type a value.</span></span>
11. <span data-ttu-id="c6fe6-143">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-143">Click Filter.</span></span>
12. <span data-ttu-id="c6fe6-144">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-144">Click Add.</span></span>
13. <span data-ttu-id="c6fe6-145">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-145">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="c6fe6-146">Í reitnum Tafla skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-146">In the Table field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="c6fe6-147">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-147">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="c6fe6-148">Í reitnum Afleidd tafla skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-148">In the Derived table field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="c6fe6-149">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-149">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="c6fe6-150">Í reitnum Reitur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-150">In the Field field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="c6fe6-151">Í reitinn Reitur skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-151">In the Field field, type a value.</span></span>
20. <span data-ttu-id="c6fe6-152">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-152">Close the page.</span></span>
21. <span data-ttu-id="c6fe6-153">Í reitinn Skilyrði skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-153">In the Criteria field, type a value.</span></span>
22. <span data-ttu-id="c6fe6-154">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-154">Click OK.</span></span>
23. <span data-ttu-id="c6fe6-155">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-155">Click OK.</span></span>
24. <span data-ttu-id="c6fe6-156">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-156">Close the page.</span></span>
25. <span data-ttu-id="c6fe6-157">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c6fe6-157">Close the page.</span></span>

