--- 
title: "Hanna gagnalíkön sértæk fyrir lén"
description: "Eftirfarandi skref útskýra hvernig notandi úthlutað á hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað nýja skilgreiningarveitu fyrir rafræna skýrslugerð (ER) sem inniheldur gagnalíkan fyrir rafræn greiðsluskjöl."
author: NickSelin
manager: AnnBe
ms.date: 12/21/2016
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: c59bdea789c4eafd2443a5d1cf802768259858c6
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2018

---
# <a name="design-domain-specific-data-models"></a><span data-ttu-id="7a39e-103">Hanna gagnalíkön sértæk fyrir lén</span><span class="sxs-lookup"><span data-stu-id="7a39e-103">Design domain-specific data models</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7a39e-104">Eftirfarandi skref útskýra hvernig notandi úthlutað á hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað nýja skilgreiningarveitu fyrir rafræna skýrslugerð (ER) sem inniheldur gagnalíkan fyrir rafræn greiðsluskjöl.</span><span class="sxs-lookup"><span data-stu-id="7a39e-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="7a39e-105">Þessi gagnalíkan verður notaður síðar sem gagnaveita þegar snið fyrir greiðsluskjölin eru stofnuð.</span><span class="sxs-lookup"><span data-stu-id="7a39e-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>



<span data-ttu-id="7a39e-106">Í þessu dæmi, verður að stofna skilgreiningu fyrir dæmi um fyrirtæki, Litware, Inc. Þessi skref má framkvæma í hvaða fyrirtæki sem er þar sem ER skilgreiningar eru samnýttar á milli fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="7a39e-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="7a39e-107">Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu "Stofna skilgreiningarveitu og merkja hana sem virka".</span><span class="sxs-lookup"><span data-stu-id="7a39e-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

1. <span data-ttu-id="7a39e-108">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="7a39e-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="7a39e-109">Veldu skilgreiningarveitu fyrir dæmi um fyrirtæki, Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="7a39e-109">Select the configuration provider for sample company, ‘Litware, Inc.’</span></span> <span data-ttu-id="7a39e-110">Ef ekki sést þessi skilgreiningarveita, verður fyrst að ljúka við skrefin í ferlinu "Stofna skilgreiningarveitu og merkja hana sem virka".</span><span class="sxs-lookup"><span data-stu-id="7a39e-110">If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
2. <span data-ttu-id="7a39e-111">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="7a39e-111">Click Reporting configurations.</span></span>
    * <span data-ttu-id="7a39e-112">Stofna verður skilgreiningu sem inniheldur gagnalíkan fyrir rafræna greiðsluskjöl.</span><span class="sxs-lookup"><span data-stu-id="7a39e-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="7a39e-113">Þessi gagnalíkan verður notaður síðar sem gagnaveita þegar snið fyrir greiðsluskjölin.</span><span class="sxs-lookup"><span data-stu-id="7a39e-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="7a39e-114">Stofna nýjan skilgreiningu gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="7a39e-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="7a39e-115">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="7a39e-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="7a39e-116">Í svæðið Heiti, færðu inn "Greiðslur (einfaldaður líkan)".</span><span class="sxs-lookup"><span data-stu-id="7a39e-116">In the Name field, type 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="7a39e-117">Greiðslur (einfaldaður líkan)</span><span class="sxs-lookup"><span data-stu-id="7a39e-117">Payments (simplified model)</span></span>  
3. <span data-ttu-id="7a39e-118">Færðu inn 'Skilgreining greiðslulíkans' í svæðinu Lýsingu.</span><span class="sxs-lookup"><span data-stu-id="7a39e-118">In the Description field, type 'Payment model configuration'.</span></span>
    * <span data-ttu-id="7a39e-119">Skilgreining greiðslulíkans</span><span class="sxs-lookup"><span data-stu-id="7a39e-119">Payment model configuration</span></span>  
    * <span data-ttu-id="7a39e-120">Virkt skilgreiningarveitu er sjálfkrafa færð inn hér.</span><span class="sxs-lookup"><span data-stu-id="7a39e-120">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="7a39e-121">Þessa veitu mun geta unnið með þessa skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="7a39e-121">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="7a39e-122">Önnur veitur er hægt að nota þetta skilgreining, en geta ekki unnið með hana.</span><span class="sxs-lookup"><span data-stu-id="7a39e-122">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
4. <span data-ttu-id="7a39e-123">Smellið á hnappinn "Stofna skilgreiningu" að ljúka verkinu fyrir stofnun skilgreiningar</span><span class="sxs-lookup"><span data-stu-id="7a39e-123">Click ‘Create configuration’ button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="7a39e-124">Stofna gagnalíkan</span><span class="sxs-lookup"><span data-stu-id="7a39e-124">Create a data model</span></span>
    * <span data-ttu-id="7a39e-125">Verið er að búa til nýtt gagnalíkan fyrir valda grunnstillingu.</span><span class="sxs-lookup"><span data-stu-id="7a39e-125">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="7a39e-126">Þessi útgáfa skilgreiningarinnar mun hafa stöðuna drög.</span><span class="sxs-lookup"><span data-stu-id="7a39e-126">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="7a39e-127">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="7a39e-127">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="7a39e-128">Skilgreina uppbygging aðila sem er í greiðsluferli</span><span class="sxs-lookup"><span data-stu-id="7a39e-128">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="7a39e-129">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="7a39e-129">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="7a39e-130">Í svæði Nafn færirðu inn „Aðili“.</span><span class="sxs-lookup"><span data-stu-id="7a39e-130">In the Name field, type 'Party'.</span></span>
    * <span data-ttu-id="7a39e-131">Aðili</span><span class="sxs-lookup"><span data-stu-id="7a39e-131">Party</span></span>  
3. <span data-ttu-id="7a39e-132">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="7a39e-132">Click Add.</span></span>
4. <span data-ttu-id="7a39e-133">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="7a39e-133">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="7a39e-134">Í svæðið Heiti, færðu inn ‚Heiti'.</span><span class="sxs-lookup"><span data-stu-id="7a39e-134">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="7a39e-135">Nafn</span><span class="sxs-lookup"><span data-stu-id="7a39e-135">Name</span></span>  
6. <span data-ttu-id="7a39e-136">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="7a39e-136">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="7a39e-137">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="7a39e-137">Click Add.</span></span>
8. <span data-ttu-id="7a39e-138">Í svæði Finna færirðu inn „Aðili“.</span><span class="sxs-lookup"><span data-stu-id="7a39e-138">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="7a39e-139">Aðili</span><span class="sxs-lookup"><span data-stu-id="7a39e-139">Party</span></span>  
9. <span data-ttu-id="7a39e-140">Smelltu á Finna fyrri.</span><span class="sxs-lookup"><span data-stu-id="7a39e-140">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="7a39e-141">Skilgreina skipulag banka fyrir þetta líkan</span><span class="sxs-lookup"><span data-stu-id="7a39e-141">Define the bank structure for this model</span></span>
1. <span data-ttu-id="7a39e-142">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="7a39e-142">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="7a39e-143">Í svæðið Heiti, færðu inn ‚umboðsmaður'.</span><span class="sxs-lookup"><span data-stu-id="7a39e-143">In the Name field, type 'Agent'.</span></span>
    * <span data-ttu-id="7a39e-144">Umboðsmaður</span><span class="sxs-lookup"><span data-stu-id="7a39e-144">Agent</span></span>  
3. <span data-ttu-id="7a39e-145">Veljið 'Færslan' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="7a39e-145">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="7a39e-146">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="7a39e-146">Click Add.</span></span>
5. <span data-ttu-id="7a39e-147">Í svæði Lýsing, færðu inn „Fjárhagsstofnun“ (til dæmis, banki) sem þjónustar lykil fyrir aðila (skuldari/lánardrottinn).</span><span class="sxs-lookup"><span data-stu-id="7a39e-147">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>
    * <span data-ttu-id="7a39e-148">Fjárhagsstofnun (til dæmis, banki) sem þjónustar lykil fyrir aðila (skuldara/lánardrottin).</span><span class="sxs-lookup"><span data-stu-id="7a39e-148">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  
6. <span data-ttu-id="7a39e-149">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="7a39e-149">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="7a39e-150">Í svæðið Heiti, færðu inn ‚Heiti'.</span><span class="sxs-lookup"><span data-stu-id="7a39e-150">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="7a39e-151">Nafn</span><span class="sxs-lookup"><span data-stu-id="7a39e-151">Name</span></span>  
8. <span data-ttu-id="7a39e-152">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="7a39e-152">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="7a39e-153">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="7a39e-153">Click Add.</span></span>
10. <span data-ttu-id="7a39e-154">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="7a39e-154">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="7a39e-155">Í svæðið Heiti, færðu inn ‚SWIFT'.</span><span class="sxs-lookup"><span data-stu-id="7a39e-155">In the Name field, type 'SWIFT'.</span></span>
    * <span data-ttu-id="7a39e-156">SWIFT</span><span class="sxs-lookup"><span data-stu-id="7a39e-156">SWIFT</span></span>  
12. <span data-ttu-id="7a39e-157">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="7a39e-157">Click Add.</span></span>
13. <span data-ttu-id="7a39e-158">Í svæði Lýsing slá inn „Auðkenniskóði banka“.</span><span class="sxs-lookup"><span data-stu-id="7a39e-158">In the Description field, enter 'Bank identification code'.</span></span>
    * <span data-ttu-id="7a39e-159">Bankanúmer</span><span class="sxs-lookup"><span data-stu-id="7a39e-159">Bank identification code</span></span>  
14. <span data-ttu-id="7a39e-160">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="7a39e-160">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="7a39e-161">Í svæðið Heiti, færðu inn 'RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="7a39e-161">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="7a39e-162">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="7a39e-162">RoutingNumber</span></span>  
16. <span data-ttu-id="7a39e-163">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="7a39e-163">Click Add.</span></span>
17. <span data-ttu-id="7a39e-164">Í svæði Lýsing slá inn „Leiðarnúmer“.</span><span class="sxs-lookup"><span data-stu-id="7a39e-164">In the Description field, enter 'Routing number'.</span></span>
    * <span data-ttu-id="7a39e-165">Leiðarnúmer</span><span class="sxs-lookup"><span data-stu-id="7a39e-165">Routing number</span></span>  
18. <span data-ttu-id="7a39e-166">Smelltu á Finna fyrri.</span><span class="sxs-lookup"><span data-stu-id="7a39e-166">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="7a39e-167">Skilgreina skipulag bankareikning fyrir þetta líkan</span><span class="sxs-lookup"><span data-stu-id="7a39e-167">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="7a39e-168">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="7a39e-168">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="7a39e-169">Í reitnum Heiti skal færa inn 'Bankareikningur'.</span><span class="sxs-lookup"><span data-stu-id="7a39e-169">In the Name field, type 'Account'.</span></span>
    * <span data-ttu-id="7a39e-170">Lykill</span><span class="sxs-lookup"><span data-stu-id="7a39e-170">Account</span></span>  
3. <span data-ttu-id="7a39e-171">Veljið 'Færslan' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="7a39e-171">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="7a39e-172">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="7a39e-172">Click Add.</span></span>
5. <span data-ttu-id="7a39e-173">Í svæði Lýsing slá inn „Auðkenning lykils hjá aðila í fjármálastofnun (t.d. banka)“.</span><span class="sxs-lookup"><span data-stu-id="7a39e-173">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>
    * <span data-ttu-id="7a39e-174">Auðkenning lykils hjá aðila í fjármálastofnun (t.d. banka).</span><span class="sxs-lookup"><span data-stu-id="7a39e-174">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  
6. <span data-ttu-id="7a39e-175">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="7a39e-175">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="7a39e-176">Í svæðið Heiti, færðu inn 'Gjaldmiðils'.</span><span class="sxs-lookup"><span data-stu-id="7a39e-176">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="7a39e-177">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="7a39e-177">Currency</span></span>  
8. <span data-ttu-id="7a39e-178">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="7a39e-178">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="7a39e-179">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="7a39e-179">Click Add.</span></span>
10. <span data-ttu-id="7a39e-180">Í svæði Lýsing slá inn „Gjaldmiðilskóði“.</span><span class="sxs-lookup"><span data-stu-id="7a39e-180">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="7a39e-181">Gjaldmiðilskóði</span><span class="sxs-lookup"><span data-stu-id="7a39e-181">Currency code</span></span>  
11. <span data-ttu-id="7a39e-182">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="7a39e-182">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="7a39e-183">Í svæðið Heiti, færðu inn ‚númer'.</span><span class="sxs-lookup"><span data-stu-id="7a39e-183">In the Name field, type 'Number'.</span></span>
    * <span data-ttu-id="7a39e-184">Númer</span><span class="sxs-lookup"><span data-stu-id="7a39e-184">Number</span></span>  
13. <span data-ttu-id="7a39e-185">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="7a39e-185">Click Add.</span></span>
14. <span data-ttu-id="7a39e-186">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="7a39e-186">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="7a39e-187">Í svæðið Heiti, færðu inn ‚IBAN-númer'.</span><span class="sxs-lookup"><span data-stu-id="7a39e-187">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="7a39e-188">IBAN-númer</span><span class="sxs-lookup"><span data-stu-id="7a39e-188">IBAN</span></span>  
16. <span data-ttu-id="7a39e-189">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="7a39e-189">Click Add.</span></span>
17. <span data-ttu-id="7a39e-190">Í svæði Lýsing slá inn „Alþjóðlegt bankareikningsnúmer“.</span><span class="sxs-lookup"><span data-stu-id="7a39e-190">In the Description field, enter 'International bank account number'.</span></span>
    * <span data-ttu-id="7a39e-191">Alþjóðlegt bankareikningsnúmer</span><span class="sxs-lookup"><span data-stu-id="7a39e-191">International bank account number</span></span>  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="7a39e-192">Skilgreina uppbygging greiðsluskilaboða fyrir greiðslugerð kreditfærslu</span><span class="sxs-lookup"><span data-stu-id="7a39e-192">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="7a39e-193">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="7a39e-193">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="7a39e-194">Í svæði Nýr hnútur sem, slá inn „Líkanshnútur“.</span><span class="sxs-lookup"><span data-stu-id="7a39e-194">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="7a39e-195">Í svæðið Heiti, Færðu inn 'CustomerCreditTransferInitiation'.</span><span class="sxs-lookup"><span data-stu-id="7a39e-195">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="7a39e-196">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="7a39e-196">CustomerCreditTransferInitiation</span></span>  
4. <span data-ttu-id="7a39e-197">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="7a39e-197">Click Add.</span></span>
5. <span data-ttu-id="7a39e-198">Í svæði Finna, slá inn „CustomerCreditTransferInitiation“.</span><span class="sxs-lookup"><span data-stu-id="7a39e-198">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="7a39e-199">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="7a39e-199">CustomerCreditTransferInitiation</span></span>  
6. <span data-ttu-id="7a39e-200">Smelltu á Finna fyrri.</span><span class="sxs-lookup"><span data-stu-id="7a39e-200">Click Find previous.</span></span>
7. <span data-ttu-id="7a39e-201">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="7a39e-201">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="7a39e-202">Í svæðið Heiti, færðu inn 'MessageIdentification'.</span><span class="sxs-lookup"><span data-stu-id="7a39e-202">In the Name field, type 'MessageIdentification'.</span></span>
    * <span data-ttu-id="7a39e-203">MessageIdentification</span><span class="sxs-lookup"><span data-stu-id="7a39e-203">MessageIdentification</span></span>  
9. <span data-ttu-id="7a39e-204">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="7a39e-204">Click Add.</span></span>
10. <span data-ttu-id="7a39e-205">Í svæði Lýsing, færið inn Tilvísun frá einum stað til annars, eins og úthlutað er af hálfu leiðbeinandi aðila, (og send til næsta aðila í röðinni) til að auðkenna skilaboðin.</span><span class="sxs-lookup"><span data-stu-id="7a39e-205">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>
    * <span data-ttu-id="7a39e-206">Tilvísun frá einum stað til annars, eins og úthlutað er af hálfu leiðbeinandi aðila, (og send til næsta aðila í röðinni) til að auðkenna skilaboðin.</span><span class="sxs-lookup"><span data-stu-id="7a39e-206">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  
11. <span data-ttu-id="7a39e-207">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="7a39e-207">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="7a39e-208">Í svæðið Heiti, færðu in 'ProcessingDateTime'.</span><span class="sxs-lookup"><span data-stu-id="7a39e-208">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="7a39e-209">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="7a39e-209">ProcessingDateTime</span></span>  
13. <span data-ttu-id="7a39e-210">Velja 'DateTime' í svæðinu gerð Vöru.</span><span class="sxs-lookup"><span data-stu-id="7a39e-210">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="7a39e-211">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="7a39e-211">Click Add.</span></span>
15. <span data-ttu-id="7a39e-212">Í svæðinu Lýsing færa inn „Dagsetningu og tíma sem greiðsluskilaboðin var stofnuð“.</span><span class="sxs-lookup"><span data-stu-id="7a39e-212">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span>
    * <span data-ttu-id="7a39e-213">Dagsetning og tími þegar greiðsluskilaboðin voru stofnuð.</span><span class="sxs-lookup"><span data-stu-id="7a39e-213">Date and time at which the payment message was created.</span></span>  
16. <span data-ttu-id="7a39e-214">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="7a39e-214">Click New to open the drop dialog.</span></span>
    * <span data-ttu-id="7a39e-215">Skilgreina skipulag greiðslufærsla fyrir þetta líkan.</span><span class="sxs-lookup"><span data-stu-id="7a39e-215">Define the payment transaction structure for this model.</span></span>  
17. <span data-ttu-id="7a39e-216">Í svæðið Heiti, færðu inn 'Greiðslur'.</span><span class="sxs-lookup"><span data-stu-id="7a39e-216">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="7a39e-217">Greiðslur</span><span class="sxs-lookup"><span data-stu-id="7a39e-217">Payments</span></span>  
18. <span data-ttu-id="7a39e-218">Veljið í svæðinu gerð Vöru „Skrárlisti".</span><span class="sxs-lookup"><span data-stu-id="7a39e-218">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="7a39e-219">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="7a39e-219">Click Add.</span></span>
20. <span data-ttu-id="7a39e-220">Færið inn 'Greiðslulínur fyrir gildandi skilaboð' í svæðinu Lýsingu.</span><span class="sxs-lookup"><span data-stu-id="7a39e-220">In the Description field, enter 'Payment lines of the current message'.</span></span>
    * <span data-ttu-id="7a39e-221">Greiðslulínur fyrir gildandi skilaboð</span><span class="sxs-lookup"><span data-stu-id="7a39e-221">Payment lines of the current message</span></span>  
21. <span data-ttu-id="7a39e-222">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="7a39e-222">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="7a39e-223">Í svæðið Heiti, færðu inn 'Lánardrottins'.</span><span class="sxs-lookup"><span data-stu-id="7a39e-223">In the Name field, type 'Creditor'.</span></span>
    * <span data-ttu-id="7a39e-224">Lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="7a39e-224">Creditor</span></span>  
23. <span data-ttu-id="7a39e-225">Veljið 'Færslan' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="7a39e-225">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="7a39e-226">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="7a39e-226">Click Add.</span></span>
25. <span data-ttu-id="7a39e-227">Færið inn „Aðili sem á að taka á móti fjárhæð“ í svæðinu Lýsingu.</span><span class="sxs-lookup"><span data-stu-id="7a39e-227">In the Description field, enter 'Party to which an amount of money is due.'.</span></span>
    * <span data-ttu-id="7a39e-228">Aðili sem á að taka á móti fjárhæð.</span><span class="sxs-lookup"><span data-stu-id="7a39e-228">Party to which an amount of money is due.</span></span>  
26. <span data-ttu-id="7a39e-229">Smellt er á Skipta um vörutilvísun.</span><span class="sxs-lookup"><span data-stu-id="7a39e-229">Click Switch item reference.</span></span>
27. <span data-ttu-id="7a39e-230">Í svæði Finna færirðu inn „Aðili“.</span><span class="sxs-lookup"><span data-stu-id="7a39e-230">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="7a39e-231">Aðili</span><span class="sxs-lookup"><span data-stu-id="7a39e-231">Party</span></span>  
28. <span data-ttu-id="7a39e-232">Smellt er á Finna næsta.</span><span class="sxs-lookup"><span data-stu-id="7a39e-232">Click Find next.</span></span>
29. <span data-ttu-id="7a39e-233">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="7a39e-233">Click OK.</span></span>
30. <span data-ttu-id="7a39e-234">Í svæði Finna færirðu inn „Greiðslur“.</span><span class="sxs-lookup"><span data-stu-id="7a39e-234">In the Find field, type 'Payments'.</span></span>
    * <span data-ttu-id="7a39e-235">Greiðslur</span><span class="sxs-lookup"><span data-stu-id="7a39e-235">Payments</span></span>  
31. <span data-ttu-id="7a39e-236">Smellt er á Finna næsta.</span><span class="sxs-lookup"><span data-stu-id="7a39e-236">Click Find next.</span></span>
32. <span data-ttu-id="7a39e-237">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="7a39e-237">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="7a39e-238">Í svæðið Heiti, færðu inn ‚skuldari'.</span><span class="sxs-lookup"><span data-stu-id="7a39e-238">In the Name field, type 'Debtor'.</span></span>
    * <span data-ttu-id="7a39e-239">Skuldari</span><span class="sxs-lookup"><span data-stu-id="7a39e-239">Debtor</span></span>  
34. <span data-ttu-id="7a39e-240">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="7a39e-240">Click Add.</span></span>
35. <span data-ttu-id="7a39e-241">Í svæðinu Lýsing, færðu inn „Aðili sem skuldar lánveitanda (til þrautavara) tiltekna fjárhæð“.</span><span class="sxs-lookup"><span data-stu-id="7a39e-241">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
    * <span data-ttu-id="7a39e-242">Aðili sem skuldar lánveitanda (til þrautavara) tiltekna fjárhæð.</span><span class="sxs-lookup"><span data-stu-id="7a39e-242">Party that owes an amount of money to the (ultimate) creditor.</span></span>  
36. <span data-ttu-id="7a39e-243">Smellt er á Skipta um vörutilvísun.</span><span class="sxs-lookup"><span data-stu-id="7a39e-243">Click Switch item reference.</span></span>
37. <span data-ttu-id="7a39e-244">Í svæði Finna færirðu inn „Aðili“.</span><span class="sxs-lookup"><span data-stu-id="7a39e-244">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="7a39e-245">Aðili</span><span class="sxs-lookup"><span data-stu-id="7a39e-245">Party</span></span>  
38. <span data-ttu-id="7a39e-246">Smellt er á Finna næsta.</span><span class="sxs-lookup"><span data-stu-id="7a39e-246">Click Find next.</span></span>
39. <span data-ttu-id="7a39e-247">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="7a39e-247">Click OK.</span></span>
40. <span data-ttu-id="7a39e-248">Smellt er á Finna næsta.</span><span class="sxs-lookup"><span data-stu-id="7a39e-248">Click Find next.</span></span>
41. <span data-ttu-id="7a39e-249">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="7a39e-249">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="7a39e-250">Í reitnum Heiti skal færa inn ‚Lýsing'.</span><span class="sxs-lookup"><span data-stu-id="7a39e-250">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="7a39e-251">lýsing</span><span class="sxs-lookup"><span data-stu-id="7a39e-251">Description</span></span>  
43. <span data-ttu-id="7a39e-252">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="7a39e-252">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="7a39e-253">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="7a39e-253">Click Add.</span></span>
45. <span data-ttu-id="7a39e-254">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="7a39e-254">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="7a39e-255">Í svæðið Heiti, færðu inn 'Gjaldmiðils'.</span><span class="sxs-lookup"><span data-stu-id="7a39e-255">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="7a39e-256">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="7a39e-256">Currency</span></span>  
47. <span data-ttu-id="7a39e-257">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="7a39e-257">Click Add.</span></span>
48. <span data-ttu-id="7a39e-258">Í svæði Lýsing slá inn „Gjaldmiðilskóði“.</span><span class="sxs-lookup"><span data-stu-id="7a39e-258">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="7a39e-259">Gjaldmiðilskóði</span><span class="sxs-lookup"><span data-stu-id="7a39e-259">Currency code</span></span>  
49. <span data-ttu-id="7a39e-260">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="7a39e-260">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="7a39e-261">Í reitnum Heiti skal færa inn ‚TransactionDate'.</span><span class="sxs-lookup"><span data-stu-id="7a39e-261">In the Name field, type 'TransactionDate'.</span></span>
    * <span data-ttu-id="7a39e-262">TransactionDate</span><span class="sxs-lookup"><span data-stu-id="7a39e-262">TransactionDate</span></span>  
51. <span data-ttu-id="7a39e-263">Velja 'Dagsetning' í svæðinu gerð vöru.</span><span class="sxs-lookup"><span data-stu-id="7a39e-263">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="7a39e-264">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="7a39e-264">Click Add.</span></span>
53. <span data-ttu-id="7a39e-265">Í svæði Lýsing slá inn „Færsludagsetning“.</span><span class="sxs-lookup"><span data-stu-id="7a39e-265">In the Description field, enter 'Transaction date'.</span></span>
    * <span data-ttu-id="7a39e-266">Færsludagsetning</span><span class="sxs-lookup"><span data-stu-id="7a39e-266">Transaction date</span></span>  
54. <span data-ttu-id="7a39e-267">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="7a39e-267">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="7a39e-268">Í reitnum Heiti skal færa inn ‚InstructedAmount'.</span><span class="sxs-lookup"><span data-stu-id="7a39e-268">In the Name field, type 'InstructedAmount'.</span></span>
    * <span data-ttu-id="7a39e-269">InstructedAmount</span><span class="sxs-lookup"><span data-stu-id="7a39e-269">InstructedAmount</span></span>  
56. <span data-ttu-id="7a39e-270">Veljið 'Raunveruleg' í svæðinu gerð vöru.</span><span class="sxs-lookup"><span data-stu-id="7a39e-270">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="7a39e-271">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="7a39e-271">Click Add.</span></span>
58. <span data-ttu-id="7a39e-272">Í svæðinu Lýsing, færðu inn „Peningafjárhæð sem á að færa á milli skuldara og lánardrottins, áður en frádráttur gjalda á sér stað“.</span><span class="sxs-lookup"><span data-stu-id="7a39e-272">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="7a39e-273">Upphæð skal sett fram í þeim gjaldmiðli sem upphafsaðili segir til um.</span><span class="sxs-lookup"><span data-stu-id="7a39e-273">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>
    * <span data-ttu-id="7a39e-274">Peningafjárhæð sem á að færa á milli skuldara og lánardrottins, áður en frádráttur gjalda á sér stað.</span><span class="sxs-lookup"><span data-stu-id="7a39e-274">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="7a39e-275">Upphæð skal sett fram í þeim gjaldmiðli sem upphafsaðili segir til um</span><span class="sxs-lookup"><span data-stu-id="7a39e-275">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  
59. <span data-ttu-id="7a39e-276">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="7a39e-276">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="7a39e-277">Í svæðið Heiti, færðu inn 'End2EndID'.</span><span class="sxs-lookup"><span data-stu-id="7a39e-277">In the Name field, type 'End2EndID'.</span></span>
    * <span data-ttu-id="7a39e-278">End2EndID</span><span class="sxs-lookup"><span data-stu-id="7a39e-278">End2EndID</span></span>  
61. <span data-ttu-id="7a39e-279">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="7a39e-279">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="7a39e-280">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="7a39e-280">Click Add.</span></span>
63. <span data-ttu-id="7a39e-281">Í svæði Lýsing, slá inn „Einkvæmt kenni sem úthlutað er af upphafsaðila“.</span><span class="sxs-lookup"><span data-stu-id="7a39e-281">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="7a39e-282">Þessi auðkenning er færð áfram, óbreytt, í gegnum alla keðjuna, enda á milli</span><span class="sxs-lookup"><span data-stu-id="7a39e-282">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span>
    * <span data-ttu-id="7a39e-283">Einkvæmt kenni sem úthlutað er af upphafsaðila.</span><span class="sxs-lookup"><span data-stu-id="7a39e-283">The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="7a39e-284">Þessi auðkenning er færð áfram, óbreytt, í gegnum alla keðjuna, enda á milli</span><span class="sxs-lookup"><span data-stu-id="7a39e-284">This identification is passed on, unchanged, throughout the entire end-to-end chain.</span></span>  
64. <span data-ttu-id="7a39e-285">Í svæðið Heiti, færðu inn 'PaymentModel'.</span><span class="sxs-lookup"><span data-stu-id="7a39e-285">In the Name field, type 'PaymentModel'.</span></span>
    * <span data-ttu-id="7a39e-286">Heiti PaymentModel stemmir sig af við með fyrirfram skilgreindum viðmót greiðsluskjámyndir.</span><span class="sxs-lookup"><span data-stu-id="7a39e-286">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  
65. <span data-ttu-id="7a39e-287">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="7a39e-287">Click Save.</span></span>
66. <span data-ttu-id="7a39e-288">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7a39e-288">Close the page.</span></span>


