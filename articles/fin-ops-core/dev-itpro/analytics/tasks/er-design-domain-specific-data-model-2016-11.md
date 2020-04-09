---
title: Rafræn skýrslugerð Hanna lénasértæk gagnalíkön
description: Eftirfarandi skref útskýra hvernig notandi úthlutað á hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað nýja skilgreiningarveitu fyrir rafræna skýrslugerð (ER) sem inniheldur gagnalíkan fyrir rafræn greiðsluskjöl.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f2b93f74a121de4c23eb5dddfb94c6596b78544d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142663"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="8f223-103">Rafræn skýrslugerð Hanna lénasértæk gagnalíkön</span><span class="sxs-lookup"><span data-stu-id="8f223-103">ER Design domain specific data model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8f223-104">Eftirfarandi skref útskýra hvernig notandi úthlutað á hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað nýja skilgreiningarveitu fyrir rafræna skýrslugerð (ER) sem inniheldur gagnalíkan fyrir rafræn greiðsluskjöl.</span><span class="sxs-lookup"><span data-stu-id="8f223-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="8f223-105">Þessi gagnalíkan verður notaður síðar sem gagnaveita þegar snið fyrir greiðsluskjölin eru stofnuð.</span><span class="sxs-lookup"><span data-stu-id="8f223-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>

<span data-ttu-id="8f223-106">Í þessu dæmi, verður að stofna skilgreiningu fyrir dæmi um fyrirtæki, Litware, Inc. Þessi skref má framkvæma í hvaða fyrirtæki sem er þar sem ER skilgreiningar eru samnýttar á milli fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="8f223-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="8f223-107">Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu „Stofna skilgreiningarveitu og merkja hana sem virka”.</span><span class="sxs-lookup"><span data-stu-id="8f223-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

1. <span data-ttu-id="8f223-108">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="8f223-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="8f223-109">Veldu skilgreiningarveitu fyrir dæmi um fyrirtæki, „Litware, Inc”.</span><span class="sxs-lookup"><span data-stu-id="8f223-109">Select the configuration provider for sample company, 'Litware, Inc.'</span></span> <span data-ttu-id="8f223-110">Ef ekki sést þessi skilgreiningarveita, verður fyrst að ljúka við skrefin í ferlinu „Stofna skilgreiningarveitu og merkja hana sem virka”.</span><span class="sxs-lookup"><span data-stu-id="8f223-110">If you don't see this configuration provider, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>  
    
2. <span data-ttu-id="8f223-111">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="8f223-111">Click Reporting configurations.</span></span>

    <span data-ttu-id="8f223-112">Stofna verður skilgreiningu sem inniheldur gagnalíkan fyrir rafræna greiðsluskjöl.</span><span class="sxs-lookup"><span data-stu-id="8f223-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="8f223-113">Þessi gagnalíkan verður notaður síðar sem gagnaveita þegar snið fyrir greiðsluskjölin.</span><span class="sxs-lookup"><span data-stu-id="8f223-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="8f223-114">Stofna nýjan skilgreiningu gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="8f223-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="8f223-115">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="8f223-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="8f223-116">Í svæðið Heiti, færðu inn "Greiðslur (einfaldaður líkan)".</span><span class="sxs-lookup"><span data-stu-id="8f223-116">In the Name field, type 'Payments (simplified model)'.</span></span>
3. <span data-ttu-id="8f223-117">Færðu inn 'Skilgreining greiðslulíkans' í svæðinu Lýsingu.</span><span class="sxs-lookup"><span data-stu-id="8f223-117">In the Description field, type 'Payment model configuration'.</span></span>

    <span data-ttu-id="8f223-118">Virkt skilgreiningarveitu er sjálfkrafa færð inn hér.</span><span class="sxs-lookup"><span data-stu-id="8f223-118">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="8f223-119">Þessa veitu mun geta unnið með þessa skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="8f223-119">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="8f223-120">Önnur veitur er hægt að nota þetta skilgreining, en geta ekki unnið með hana.</span><span class="sxs-lookup"><span data-stu-id="8f223-120">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

4. <span data-ttu-id="8f223-121">Smellið á hnappinn "Stofna skilgreiningu" að ljúka verkinu fyrir stofnun skilgreiningar</span><span class="sxs-lookup"><span data-stu-id="8f223-121">Click 'Create configuration' button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="8f223-122">Stofna gagnalíkan</span><span class="sxs-lookup"><span data-stu-id="8f223-122">Create a data model</span></span>
<span data-ttu-id="8f223-123">Verið er að búa til nýtt gagnalíkan fyrir valda grunnstillingu.</span><span class="sxs-lookup"><span data-stu-id="8f223-123">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="8f223-124">Þessi útgáfa skilgreiningarinnar mun hafa stöðuna drög.</span><span class="sxs-lookup"><span data-stu-id="8f223-124">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="8f223-125">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="8f223-125">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="8f223-126">Skilgreina uppbygging aðila sem er í greiðsluferli</span><span class="sxs-lookup"><span data-stu-id="8f223-126">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="8f223-127">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="8f223-127">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="8f223-128">Í svæði Nafn færirðu inn „Aðili“.</span><span class="sxs-lookup"><span data-stu-id="8f223-128">In the Name field, type 'Party'.</span></span>
3. <span data-ttu-id="8f223-129">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="8f223-129">Click Add.</span></span>
4. <span data-ttu-id="8f223-130">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="8f223-130">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="8f223-131">Í svæðið Heiti, færðu inn ‚Heiti'.</span><span class="sxs-lookup"><span data-stu-id="8f223-131">In the Name field, type 'Name'.</span></span>
6. <span data-ttu-id="8f223-132">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="8f223-132">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="8f223-133">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="8f223-133">Click Add.</span></span>
8. <span data-ttu-id="8f223-134">Í svæði Finna færirðu inn „Aðili“.</span><span class="sxs-lookup"><span data-stu-id="8f223-134">In the Find field, type 'Party'.</span></span>
9. <span data-ttu-id="8f223-135">Smelltu á Finna fyrri.</span><span class="sxs-lookup"><span data-stu-id="8f223-135">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="8f223-136">Skilgreina skipulag banka fyrir þetta líkan</span><span class="sxs-lookup"><span data-stu-id="8f223-136">Define the bank structure for this model</span></span>
1. <span data-ttu-id="8f223-137">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="8f223-137">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="8f223-138">Í svæðið Heiti, færðu inn ‚umboðsmaður'.</span><span class="sxs-lookup"><span data-stu-id="8f223-138">In the Name field, type 'Agent'.</span></span>
3. <span data-ttu-id="8f223-139">Veljið 'Færslan' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="8f223-139">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="8f223-140">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="8f223-140">Click Add.</span></span>
5. <span data-ttu-id="8f223-141">Í svæði Lýsing, færðu inn „Fjárhagsstofnun“ (til dæmis, banki) sem þjónustar lykil fyrir aðila (skuldari/lánardrottinn).</span><span class="sxs-lookup"><span data-stu-id="8f223-141">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>

    <span data-ttu-id="8f223-142">Fjárhagsstofnun (til dæmis, banki) sem þjónustar lykil fyrir aðila (skuldara/lánardrottin).</span><span class="sxs-lookup"><span data-stu-id="8f223-142">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  

6. <span data-ttu-id="8f223-143">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="8f223-143">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="8f223-144">Í svæðið Heiti, færðu inn ‚Heiti'.</span><span class="sxs-lookup"><span data-stu-id="8f223-144">In the Name field, type 'Name'.</span></span> 
8. <span data-ttu-id="8f223-145">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="8f223-145">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="8f223-146">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="8f223-146">Click Add.</span></span>
10. <span data-ttu-id="8f223-147">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="8f223-147">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="8f223-148">Í svæðið Heiti, færðu inn ‚SWIFT'.</span><span class="sxs-lookup"><span data-stu-id="8f223-148">In the Name field, type 'SWIFT'.</span></span>
12. <span data-ttu-id="8f223-149">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="8f223-149">Click Add.</span></span>
13. <span data-ttu-id="8f223-150">Í svæði Lýsing slá inn „Auðkenniskóði banka“.</span><span class="sxs-lookup"><span data-stu-id="8f223-150">In the Description field, enter 'Bank identification code'.</span></span> 
14. <span data-ttu-id="8f223-151">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="8f223-151">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="8f223-152">Í svæðið Heiti, færðu inn 'RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="8f223-152">In the Name field, type 'RoutingNumber'.</span></span>
16. <span data-ttu-id="8f223-153">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="8f223-153">Click Add.</span></span>
17. <span data-ttu-id="8f223-154">Í svæði Lýsing slá inn „Leiðarnúmer“.</span><span class="sxs-lookup"><span data-stu-id="8f223-154">In the Description field, enter 'Routing number'.</span></span>
18. <span data-ttu-id="8f223-155">Smelltu á Finna fyrri.</span><span class="sxs-lookup"><span data-stu-id="8f223-155">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="8f223-156">Skilgreina skipulag bankareikning fyrir þetta líkan</span><span class="sxs-lookup"><span data-stu-id="8f223-156">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="8f223-157">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="8f223-157">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="8f223-158">Í reitnum Heiti skal færa inn 'Bankareikningur'.</span><span class="sxs-lookup"><span data-stu-id="8f223-158">In the Name field, type 'Account'.</span></span> 
3. <span data-ttu-id="8f223-159">Veljið 'Færslan' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="8f223-159">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="8f223-160">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="8f223-160">Click Add.</span></span>
5. <span data-ttu-id="8f223-161">Í svæði Lýsing slá inn „Auðkenning lykils hjá aðila í fjármálastofnun (t.d. banka)“.</span><span class="sxs-lookup"><span data-stu-id="8f223-161">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>

    <span data-ttu-id="8f223-162">Auðkenning lykils hjá aðila í fjármálastofnun (t.d. banka).</span><span class="sxs-lookup"><span data-stu-id="8f223-162">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  

6. <span data-ttu-id="8f223-163">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="8f223-163">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="8f223-164">Í svæðið Heiti, færðu inn 'Gjaldmiðils'.</span><span class="sxs-lookup"><span data-stu-id="8f223-164">In the Name field, type 'Currency'.</span></span> 
8. <span data-ttu-id="8f223-165">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="8f223-165">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="8f223-166">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="8f223-166">Click Add.</span></span>
10. <span data-ttu-id="8f223-167">Í svæði Lýsing slá inn „Gjaldmiðilskóði“.</span><span class="sxs-lookup"><span data-stu-id="8f223-167">In the Description field, enter 'Currency code'.</span></span>
11. <span data-ttu-id="8f223-168">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="8f223-168">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="8f223-169">Í svæðið Heiti, færðu inn ‚númer'.</span><span class="sxs-lookup"><span data-stu-id="8f223-169">In the Name field, type 'Number'.</span></span> 
13. <span data-ttu-id="8f223-170">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="8f223-170">Click Add.</span></span>
14. <span data-ttu-id="8f223-171">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="8f223-171">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="8f223-172">Í svæðið Heiti, færðu inn ‚IBAN-númer'.</span><span class="sxs-lookup"><span data-stu-id="8f223-172">In the Name field, type 'IBAN'.</span></span> 
16. <span data-ttu-id="8f223-173">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="8f223-173">Click Add.</span></span>
17. <span data-ttu-id="8f223-174">Í svæði Lýsing slá inn „Alþjóðlegt bankareikningsnúmer“.</span><span class="sxs-lookup"><span data-stu-id="8f223-174">In the Description field, enter 'International bank account number'.</span></span>

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="8f223-175">Skilgreina uppbygging greiðsluskilaboða fyrir greiðslugerð kreditfærslu</span><span class="sxs-lookup"><span data-stu-id="8f223-175">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="8f223-176">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="8f223-176">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="8f223-177">Í svæði Nýr hnútur sem, slá inn „Líkanshnútur“.</span><span class="sxs-lookup"><span data-stu-id="8f223-177">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="8f223-178">Í svæðið Heiti, Færðu inn 'CustomerCreditTransferInitiation'.</span><span class="sxs-lookup"><span data-stu-id="8f223-178">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
4. <span data-ttu-id="8f223-179">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="8f223-179">Click Add.</span></span>
5. <span data-ttu-id="8f223-180">Í svæði Finna, slá inn „CustomerCreditTransferInitiation“.</span><span class="sxs-lookup"><span data-stu-id="8f223-180">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span> 
6. <span data-ttu-id="8f223-181">Smelltu á Finna fyrri.</span><span class="sxs-lookup"><span data-stu-id="8f223-181">Click Find previous.</span></span>
7. <span data-ttu-id="8f223-182">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="8f223-182">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="8f223-183">Í svæðið Heiti, færðu inn 'MessageIdentification'.</span><span class="sxs-lookup"><span data-stu-id="8f223-183">In the Name field, type 'MessageIdentification'.</span></span> 
9. <span data-ttu-id="8f223-184">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="8f223-184">Click Add.</span></span>
10. <span data-ttu-id="8f223-185">Í svæði Lýsing, færið inn Tilvísun frá einum stað til annars, eins og úthlutað er af hálfu leiðbeinandi aðila, (og send til næsta aðila í röðinni) til að auðkenna skilaboðin.</span><span class="sxs-lookup"><span data-stu-id="8f223-185">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>

    <span data-ttu-id="8f223-186">Tilvísun frá einum stað til annars, eins og úthlutað er af hálfu leiðbeinandi aðila, (og send til næsta aðila í röðinni) til að auðkenna skilaboðin.</span><span class="sxs-lookup"><span data-stu-id="8f223-186">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  

11. <span data-ttu-id="8f223-187">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="8f223-187">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="8f223-188">Í svæðið Heiti, færðu in 'ProcessingDateTime'.</span><span class="sxs-lookup"><span data-stu-id="8f223-188">In the Name field, type 'ProcessingDateTime'.</span></span>
13. <span data-ttu-id="8f223-189">Velja 'DateTime' í svæðinu gerð Vöru.</span><span class="sxs-lookup"><span data-stu-id="8f223-189">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="8f223-190">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="8f223-190">Click Add.</span></span>
15. <span data-ttu-id="8f223-191">Í svæðinu Lýsing færa inn „Dagsetningu og tíma sem greiðsluskilaboðin var stofnuð“.</span><span class="sxs-lookup"><span data-stu-id="8f223-191">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span> 
16. <span data-ttu-id="8f223-192">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="8f223-192">Click New to open the drop dialog.</span></span>

    <span data-ttu-id="8f223-193">Skilgreina skipulag greiðslufærsla fyrir þetta líkan.</span><span class="sxs-lookup"><span data-stu-id="8f223-193">Define the payment transaction structure for this model.</span></span>  

17. <span data-ttu-id="8f223-194">Í svæðið Heiti, færðu inn 'Greiðslur'.</span><span class="sxs-lookup"><span data-stu-id="8f223-194">In the Name field, type 'Payments'.</span></span>
18. <span data-ttu-id="8f223-195">Veljið í svæðinu gerð Vöru „Skrárlisti".</span><span class="sxs-lookup"><span data-stu-id="8f223-195">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="8f223-196">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="8f223-196">Click Add.</span></span>
20. <span data-ttu-id="8f223-197">Færið inn 'Greiðslulínur fyrir gildandi skilaboð' í svæðinu Lýsingu.</span><span class="sxs-lookup"><span data-stu-id="8f223-197">In the Description field, enter 'Payment lines of the current message'.</span></span>
21. <span data-ttu-id="8f223-198">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="8f223-198">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="8f223-199">Í svæðið Heiti, færðu inn 'Lánardrottins'.</span><span class="sxs-lookup"><span data-stu-id="8f223-199">In the Name field, type 'Creditor'.</span></span> 
23. <span data-ttu-id="8f223-200">Veljið 'Færslan' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="8f223-200">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="8f223-201">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="8f223-201">Click Add.</span></span>
25. <span data-ttu-id="8f223-202">Færið inn „Aðili sem á að taka á móti fjárhæð“ í svæðinu Lýsingu.</span><span class="sxs-lookup"><span data-stu-id="8f223-202">In the Description field, enter 'Party to which an amount of money is due.'.</span></span> 
26. <span data-ttu-id="8f223-203">Smellt er á Skipta um vörutilvísun.</span><span class="sxs-lookup"><span data-stu-id="8f223-203">Click Switch item reference.</span></span>
27. <span data-ttu-id="8f223-204">Í svæði Finna færirðu inn „Aðili“.</span><span class="sxs-lookup"><span data-stu-id="8f223-204">In the Find field, type 'Party'.</span></span>
28. <span data-ttu-id="8f223-205">Smellt er á Finna næsta.</span><span class="sxs-lookup"><span data-stu-id="8f223-205">Click Find next.</span></span>
29. <span data-ttu-id="8f223-206">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="8f223-206">Click OK.</span></span>
30. <span data-ttu-id="8f223-207">Í svæði Finna færirðu inn „Greiðslur“.</span><span class="sxs-lookup"><span data-stu-id="8f223-207">In the Find field, type 'Payments'.</span></span>
31. <span data-ttu-id="8f223-208">Smellt er á Finna næsta.</span><span class="sxs-lookup"><span data-stu-id="8f223-208">Click Find next.</span></span>
32. <span data-ttu-id="8f223-209">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="8f223-209">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="8f223-210">Í svæðið Heiti, færðu inn ‚skuldari'.</span><span class="sxs-lookup"><span data-stu-id="8f223-210">In the Name field, type 'Debtor'.</span></span> 
34. <span data-ttu-id="8f223-211">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="8f223-211">Click Add.</span></span>
35. <span data-ttu-id="8f223-212">Í svæðinu Lýsing, færðu inn „Aðili sem skuldar lánveitanda (til þrautavara) tiltekna fjárhæð“.</span><span class="sxs-lookup"><span data-stu-id="8f223-212">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
36. <span data-ttu-id="8f223-213">Smellt er á Skipta um vörutilvísun.</span><span class="sxs-lookup"><span data-stu-id="8f223-213">Click Switch item reference.</span></span>
37. <span data-ttu-id="8f223-214">Í svæði Finna færirðu inn „Aðili“.</span><span class="sxs-lookup"><span data-stu-id="8f223-214">In the Find field, type 'Party'.</span></span>
38. <span data-ttu-id="8f223-215">Smellt er á Finna næsta.</span><span class="sxs-lookup"><span data-stu-id="8f223-215">Click Find next.</span></span>
39. <span data-ttu-id="8f223-216">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="8f223-216">Click OK.</span></span>
40. <span data-ttu-id="8f223-217">Smellt er á Finna næsta.</span><span class="sxs-lookup"><span data-stu-id="8f223-217">Click Find next.</span></span>
41. <span data-ttu-id="8f223-218">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="8f223-218">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="8f223-219">Í reitnum Heiti skal færa inn ‚Lýsing'.</span><span class="sxs-lookup"><span data-stu-id="8f223-219">In the Name field, type 'Description'.</span></span>
43. <span data-ttu-id="8f223-220">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="8f223-220">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="8f223-221">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="8f223-221">Click Add.</span></span>
45. <span data-ttu-id="8f223-222">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="8f223-222">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="8f223-223">Í svæðið Heiti, færðu inn 'Gjaldmiðils'.</span><span class="sxs-lookup"><span data-stu-id="8f223-223">In the Name field, type 'Currency'.</span></span>
47. <span data-ttu-id="8f223-224">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="8f223-224">Click Add.</span></span>
48. <span data-ttu-id="8f223-225">Í svæði Lýsing slá inn „Gjaldmiðilskóði“.</span><span class="sxs-lookup"><span data-stu-id="8f223-225">In the Description field, enter 'Currency code'.</span></span>
49. <span data-ttu-id="8f223-226">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="8f223-226">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="8f223-227">Í reitnum Heiti skal færa inn ‚TransactionDate'.</span><span class="sxs-lookup"><span data-stu-id="8f223-227">In the Name field, type 'TransactionDate'.</span></span> 
51. <span data-ttu-id="8f223-228">Velja 'Dagsetning' í svæðinu gerð vöru.</span><span class="sxs-lookup"><span data-stu-id="8f223-228">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="8f223-229">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="8f223-229">Click Add.</span></span>
53. <span data-ttu-id="8f223-230">Í svæði Lýsing slá inn „Færsludagsetning“.</span><span class="sxs-lookup"><span data-stu-id="8f223-230">In the Description field, enter 'Transaction date'.</span></span> 
54. <span data-ttu-id="8f223-231">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="8f223-231">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="8f223-232">Í reitnum Heiti skal færa inn ‚InstructedAmount'.</span><span class="sxs-lookup"><span data-stu-id="8f223-232">In the Name field, type 'InstructedAmount'.</span></span>  
56. <span data-ttu-id="8f223-233">Veljið 'Raunveruleg' í svæðinu gerð vöru.</span><span class="sxs-lookup"><span data-stu-id="8f223-233">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="8f223-234">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="8f223-234">Click Add.</span></span>
58. <span data-ttu-id="8f223-235">Í svæðinu Lýsing, færðu inn „Peningafjárhæð sem á að færa á milli skuldara og lánardrottins, áður en frádráttur gjalda á sér stað“.</span><span class="sxs-lookup"><span data-stu-id="8f223-235">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="8f223-236">Upphæð skal sett fram í þeim gjaldmiðli sem upphafsaðili segir til um.</span><span class="sxs-lookup"><span data-stu-id="8f223-236">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>

    <span data-ttu-id="8f223-237">Peningafjárhæð sem á að færa á milli skuldara og lánardrottins, áður en frádráttur gjalda á sér stað.</span><span class="sxs-lookup"><span data-stu-id="8f223-237">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="8f223-238">Upphæð skal sett fram í þeim gjaldmiðli sem upphafsaðili segir til um</span><span class="sxs-lookup"><span data-stu-id="8f223-238">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  

59. <span data-ttu-id="8f223-239">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="8f223-239">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="8f223-240">Í svæðið Heiti, færðu inn 'End2EndID'.</span><span class="sxs-lookup"><span data-stu-id="8f223-240">In the Name field, type 'End2EndID'.</span></span> 
61. <span data-ttu-id="8f223-241">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="8f223-241">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="8f223-242">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="8f223-242">Click Add.</span></span>
63. <span data-ttu-id="8f223-243">Í svæði Lýsing, slá inn „Einkvæmt kenni sem úthlutað er af upphafsaðila“.</span><span class="sxs-lookup"><span data-stu-id="8f223-243">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="8f223-244">Þessi auðkenning er færð áfram, óbreytt, í gegnum alla keðjuna, enda á milli</span><span class="sxs-lookup"><span data-stu-id="8f223-244">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span> 
64. <span data-ttu-id="8f223-245">Í svæðið Heiti, færðu inn 'PaymentModel'.</span><span class="sxs-lookup"><span data-stu-id="8f223-245">In the Name field, type 'PaymentModel'.</span></span>

    <span data-ttu-id="8f223-246">Heiti PaymentModel stemmir sig af við með fyrirfram skilgreindum viðmót greiðsluskjámyndir.</span><span class="sxs-lookup"><span data-stu-id="8f223-246">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  

65. <span data-ttu-id="8f223-247">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="8f223-247">Click Save.</span></span>
66. <span data-ttu-id="8f223-248">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8f223-248">Close the page.</span></span>

