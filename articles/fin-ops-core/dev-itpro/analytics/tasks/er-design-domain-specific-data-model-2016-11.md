---
title: Rafræn skýrslugerð Hanna lénasértæk gagnalíkön
description: Í þessu efnisatriði er útskýrt hvernig á að stofna nýja skilgreiningu rafrænnar skýrslugerðar sem inniheldur gagnalíkan fyrir skjöl rafrænna greiðslna.
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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1eb2c6e5b5f186fb6db7c32a9982807274e5ea1b
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092692"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="c2638-103">Rafræn skýrslugerð Hanna lénasértæk gagnalíkön</span><span class="sxs-lookup"><span data-stu-id="c2638-103">ER Design domain specific data model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c2638-104">Eftirfarandi skref útskýra hvernig notandi úthlutað á hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað nýja skilgreiningarveitu fyrir rafræna skýrslugerð (ER) sem inniheldur gagnalíkan fyrir rafræn greiðsluskjöl.</span><span class="sxs-lookup"><span data-stu-id="c2638-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="c2638-105">Þessi gagnalíkan verður notaður síðar sem gagnaveita þegar snið fyrir greiðsluskjölin eru stofnuð.</span><span class="sxs-lookup"><span data-stu-id="c2638-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>

<span data-ttu-id="c2638-106">Í þessu dæmi, verður að stofna skilgreiningu fyrir dæmi um fyrirtæki, Litware, Inc. Þessi skref má framkvæma í hvaða fyrirtæki sem er þar sem ER skilgreiningar eru samnýttar á milli fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="c2638-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="c2638-107">Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu „Stofna skilgreiningarveitu og merkja hana sem virka”.</span><span class="sxs-lookup"><span data-stu-id="c2638-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

1. <span data-ttu-id="c2638-108">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="c2638-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="c2638-109">Veldu skilgreiningarveitu fyrir dæmi um fyrirtæki, „Litware, Inc”.</span><span class="sxs-lookup"><span data-stu-id="c2638-109">Select the configuration provider for sample company, 'Litware, Inc.'</span></span> <span data-ttu-id="c2638-110">Ef ekki sést þessi skilgreiningarveita, verður fyrst að ljúka við skrefin í ferlinu „Stofna skilgreiningarveitu og merkja hana sem virka”.</span><span class="sxs-lookup"><span data-stu-id="c2638-110">If you don't see this configuration provider, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>  
    
2. <span data-ttu-id="c2638-111">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="c2638-111">Click Reporting configurations.</span></span>

    <span data-ttu-id="c2638-112">Stofna verður skilgreiningu sem inniheldur gagnalíkan fyrir rafræna greiðsluskjöl.</span><span class="sxs-lookup"><span data-stu-id="c2638-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="c2638-113">Þessi gagnalíkan verður notaður síðar sem gagnaveita þegar snið fyrir greiðsluskjölin.</span><span class="sxs-lookup"><span data-stu-id="c2638-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="c2638-114">Stofna nýjan skilgreiningu gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="c2638-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="c2638-115">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="c2638-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="c2638-116">Í svæðið Heiti, færðu inn "Greiðslur (einfaldaður líkan)".</span><span class="sxs-lookup"><span data-stu-id="c2638-116">In the Name field, type 'Payments (simplified model)'.</span></span>
3. <span data-ttu-id="c2638-117">Færðu inn 'Skilgreining greiðslulíkans' í svæðinu Lýsingu.</span><span class="sxs-lookup"><span data-stu-id="c2638-117">In the Description field, type 'Payment model configuration'.</span></span>

    <span data-ttu-id="c2638-118">Virkt skilgreiningarveitu er sjálfkrafa færð inn hér.</span><span class="sxs-lookup"><span data-stu-id="c2638-118">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="c2638-119">Þessa veitu mun geta unnið með þessa skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="c2638-119">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="c2638-120">Önnur veitur er hægt að nota þetta skilgreining, en geta ekki unnið með hana.</span><span class="sxs-lookup"><span data-stu-id="c2638-120">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

4. <span data-ttu-id="c2638-121">Smellið á hnappinn "Stofna skilgreiningu" að ljúka verkinu fyrir stofnun skilgreiningar</span><span class="sxs-lookup"><span data-stu-id="c2638-121">Click 'Create configuration' button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="c2638-122">Stofna gagnalíkan</span><span class="sxs-lookup"><span data-stu-id="c2638-122">Create a data model</span></span>
<span data-ttu-id="c2638-123">Verið er að búa til nýtt gagnalíkan fyrir valda grunnstillingu.</span><span class="sxs-lookup"><span data-stu-id="c2638-123">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="c2638-124">Þessi útgáfa skilgreiningarinnar mun hafa stöðuna drög.</span><span class="sxs-lookup"><span data-stu-id="c2638-124">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="c2638-125">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="c2638-125">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="c2638-126">Skilgreina uppbygging aðila sem er í greiðsluferli</span><span class="sxs-lookup"><span data-stu-id="c2638-126">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="c2638-127">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2638-127">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="c2638-128">Í svæði Nafn færirðu inn „Aðili“.</span><span class="sxs-lookup"><span data-stu-id="c2638-128">In the Name field, type 'Party'.</span></span>
3. <span data-ttu-id="c2638-129">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2638-129">Click Add.</span></span>
4. <span data-ttu-id="c2638-130">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2638-130">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="c2638-131">Í svæðið Heiti, færðu inn ‚Heiti'.</span><span class="sxs-lookup"><span data-stu-id="c2638-131">In the Name field, type 'Name'.</span></span>
6. <span data-ttu-id="c2638-132">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="c2638-132">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="c2638-133">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2638-133">Click Add.</span></span>
8. <span data-ttu-id="c2638-134">Í svæði Finna færirðu inn „Aðili“.</span><span class="sxs-lookup"><span data-stu-id="c2638-134">In the Find field, type 'Party'.</span></span>
9. <span data-ttu-id="c2638-135">Smelltu á Finna fyrri.</span><span class="sxs-lookup"><span data-stu-id="c2638-135">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="c2638-136">Skilgreina skipulag banka fyrir þetta líkan</span><span class="sxs-lookup"><span data-stu-id="c2638-136">Define the bank structure for this model</span></span>
1. <span data-ttu-id="c2638-137">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2638-137">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="c2638-138">Í svæðið Heiti, færðu inn ‚umboðsmaður'.</span><span class="sxs-lookup"><span data-stu-id="c2638-138">In the Name field, type 'Agent'.</span></span>
3. <span data-ttu-id="c2638-139">Veljið 'Færslan' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="c2638-139">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="c2638-140">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2638-140">Click Add.</span></span>
5. <span data-ttu-id="c2638-141">Í svæði Lýsing, færðu inn „Fjárhagsstofnun“ (til dæmis, banki) sem þjónustar lykil fyrir aðila (skuldari/lánardrottinn).</span><span class="sxs-lookup"><span data-stu-id="c2638-141">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>

    <span data-ttu-id="c2638-142">Fjárhagsstofnun (til dæmis, banki) sem þjónustar lykil fyrir aðila (skuldara/lánardrottin).</span><span class="sxs-lookup"><span data-stu-id="c2638-142">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  

6. <span data-ttu-id="c2638-143">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2638-143">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="c2638-144">Í svæðið Heiti, færðu inn ‚Heiti'.</span><span class="sxs-lookup"><span data-stu-id="c2638-144">In the Name field, type 'Name'.</span></span> 
8. <span data-ttu-id="c2638-145">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="c2638-145">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="c2638-146">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2638-146">Click Add.</span></span>
10. <span data-ttu-id="c2638-147">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2638-147">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="c2638-148">Í svæðið Heiti, færðu inn ‚SWIFT'.</span><span class="sxs-lookup"><span data-stu-id="c2638-148">In the Name field, type 'SWIFT'.</span></span>
12. <span data-ttu-id="c2638-149">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2638-149">Click Add.</span></span>
13. <span data-ttu-id="c2638-150">Í svæði Lýsing slá inn „Auðkenniskóði banka“.</span><span class="sxs-lookup"><span data-stu-id="c2638-150">In the Description field, enter 'Bank identification code'.</span></span> 
14. <span data-ttu-id="c2638-151">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2638-151">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="c2638-152">Í svæðið Heiti, færðu inn 'RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="c2638-152">In the Name field, type 'RoutingNumber'.</span></span>
16. <span data-ttu-id="c2638-153">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2638-153">Click Add.</span></span>
17. <span data-ttu-id="c2638-154">Í svæði Lýsing slá inn „Leiðarnúmer“.</span><span class="sxs-lookup"><span data-stu-id="c2638-154">In the Description field, enter 'Routing number'.</span></span>
18. <span data-ttu-id="c2638-155">Smelltu á Finna fyrri.</span><span class="sxs-lookup"><span data-stu-id="c2638-155">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="c2638-156">Skilgreina skipulag bankareikning fyrir þetta líkan</span><span class="sxs-lookup"><span data-stu-id="c2638-156">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="c2638-157">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2638-157">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="c2638-158">Í reitnum Heiti skal færa inn 'Bankareikningur'.</span><span class="sxs-lookup"><span data-stu-id="c2638-158">In the Name field, type 'Account'.</span></span> 
3. <span data-ttu-id="c2638-159">Veljið 'Færslan' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="c2638-159">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="c2638-160">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2638-160">Click Add.</span></span>
5. <span data-ttu-id="c2638-161">Í svæði Lýsing slá inn „Auðkenning lykils hjá aðila í fjármálastofnun (t.d. banka)“.</span><span class="sxs-lookup"><span data-stu-id="c2638-161">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>

    <span data-ttu-id="c2638-162">Auðkenning lykils hjá aðila í fjármálastofnun (t.d. banka).</span><span class="sxs-lookup"><span data-stu-id="c2638-162">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  

6. <span data-ttu-id="c2638-163">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2638-163">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="c2638-164">Í svæðið Heiti, færðu inn 'Gjaldmiðils'.</span><span class="sxs-lookup"><span data-stu-id="c2638-164">In the Name field, type 'Currency'.</span></span> 
8. <span data-ttu-id="c2638-165">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="c2638-165">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="c2638-166">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2638-166">Click Add.</span></span>
10. <span data-ttu-id="c2638-167">Í svæði Lýsing slá inn „Gjaldmiðilskóði“.</span><span class="sxs-lookup"><span data-stu-id="c2638-167">In the Description field, enter 'Currency code'.</span></span>
11. <span data-ttu-id="c2638-168">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2638-168">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="c2638-169">Í svæðið Heiti, færðu inn ‚númer'.</span><span class="sxs-lookup"><span data-stu-id="c2638-169">In the Name field, type 'Number'.</span></span> 
13. <span data-ttu-id="c2638-170">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2638-170">Click Add.</span></span>
14. <span data-ttu-id="c2638-171">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2638-171">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="c2638-172">Í svæðið Heiti, færðu inn ‚IBAN-númer'.</span><span class="sxs-lookup"><span data-stu-id="c2638-172">In the Name field, type 'IBAN'.</span></span> 
16. <span data-ttu-id="c2638-173">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2638-173">Click Add.</span></span>
17. <span data-ttu-id="c2638-174">Í svæði Lýsing slá inn „Alþjóðlegt bankareikningsnúmer“.</span><span class="sxs-lookup"><span data-stu-id="c2638-174">In the Description field, enter 'International bank account number'.</span></span>

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="c2638-175">Skilgreina uppbygging greiðsluskilaboða fyrir greiðslugerð kreditfærslu</span><span class="sxs-lookup"><span data-stu-id="c2638-175">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="c2638-176">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2638-176">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="c2638-177">Í svæði Nýr hnútur sem, slá inn „Líkanshnútur“.</span><span class="sxs-lookup"><span data-stu-id="c2638-177">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="c2638-178">Í svæðið Heiti, Færðu inn 'CustomerCreditTransferInitiation'.</span><span class="sxs-lookup"><span data-stu-id="c2638-178">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
4. <span data-ttu-id="c2638-179">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2638-179">Click Add.</span></span>
5. <span data-ttu-id="c2638-180">Í svæði Finna, slá inn „CustomerCreditTransferInitiation“.</span><span class="sxs-lookup"><span data-stu-id="c2638-180">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span> 
6. <span data-ttu-id="c2638-181">Smelltu á Finna fyrri.</span><span class="sxs-lookup"><span data-stu-id="c2638-181">Click Find previous.</span></span>
7. <span data-ttu-id="c2638-182">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2638-182">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="c2638-183">Í svæðið Heiti, færðu inn 'MessageIdentification'.</span><span class="sxs-lookup"><span data-stu-id="c2638-183">In the Name field, type 'MessageIdentification'.</span></span> 
9. <span data-ttu-id="c2638-184">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2638-184">Click Add.</span></span>
10. <span data-ttu-id="c2638-185">Í svæði Lýsing, færið inn Tilvísun frá einum stað til annars, eins og úthlutað er af hálfu leiðbeinandi aðila, (og send til næsta aðila í röðinni) til að auðkenna skilaboðin.</span><span class="sxs-lookup"><span data-stu-id="c2638-185">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>

    <span data-ttu-id="c2638-186">Tilvísun frá einum stað til annars, eins og úthlutað er af hálfu leiðbeinandi aðila, (og send til næsta aðila í röðinni) til að auðkenna skilaboðin.</span><span class="sxs-lookup"><span data-stu-id="c2638-186">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  

11. <span data-ttu-id="c2638-187">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2638-187">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="c2638-188">Í svæðið Heiti, færðu in 'ProcessingDateTime'.</span><span class="sxs-lookup"><span data-stu-id="c2638-188">In the Name field, type 'ProcessingDateTime'.</span></span>
13. <span data-ttu-id="c2638-189">Velja 'DateTime' í svæðinu gerð Vöru.</span><span class="sxs-lookup"><span data-stu-id="c2638-189">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="c2638-190">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2638-190">Click Add.</span></span>
15. <span data-ttu-id="c2638-191">Í svæðinu Lýsing færa inn „Dagsetningu og tíma sem greiðsluskilaboðin var stofnuð“.</span><span class="sxs-lookup"><span data-stu-id="c2638-191">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span> 
16. <span data-ttu-id="c2638-192">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2638-192">Click New to open the drop dialog.</span></span>

    <span data-ttu-id="c2638-193">Skilgreina skipulag greiðslufærsla fyrir þetta líkan.</span><span class="sxs-lookup"><span data-stu-id="c2638-193">Define the payment transaction structure for this model.</span></span>  

17. <span data-ttu-id="c2638-194">Í svæðið Heiti, færðu inn 'Greiðslur'.</span><span class="sxs-lookup"><span data-stu-id="c2638-194">In the Name field, type 'Payments'.</span></span>
18. <span data-ttu-id="c2638-195">Veljið í svæðinu gerð Vöru „Skrárlisti".</span><span class="sxs-lookup"><span data-stu-id="c2638-195">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="c2638-196">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2638-196">Click Add.</span></span>
20. <span data-ttu-id="c2638-197">Færið inn 'Greiðslulínur fyrir gildandi skilaboð' í svæðinu Lýsingu.</span><span class="sxs-lookup"><span data-stu-id="c2638-197">In the Description field, enter 'Payment lines of the current message'.</span></span>
21. <span data-ttu-id="c2638-198">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2638-198">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="c2638-199">Í svæðið Heiti, færðu inn 'Lánardrottins'.</span><span class="sxs-lookup"><span data-stu-id="c2638-199">In the Name field, type 'Creditor'.</span></span> 
23. <span data-ttu-id="c2638-200">Veljið 'Færslan' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="c2638-200">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="c2638-201">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2638-201">Click Add.</span></span>
25. <span data-ttu-id="c2638-202">Færið inn „Aðili sem á að taka á móti fjárhæð“ í svæðinu Lýsingu.</span><span class="sxs-lookup"><span data-stu-id="c2638-202">In the Description field, enter 'Party to which an amount of money is due.'.</span></span> 
26. <span data-ttu-id="c2638-203">Smellt er á Skipta um vörutilvísun.</span><span class="sxs-lookup"><span data-stu-id="c2638-203">Click Switch item reference.</span></span>
27. <span data-ttu-id="c2638-204">Í svæði Finna færirðu inn „Aðili“.</span><span class="sxs-lookup"><span data-stu-id="c2638-204">In the Find field, type 'Party'.</span></span>
28. <span data-ttu-id="c2638-205">Smellt er á Finna næsta.</span><span class="sxs-lookup"><span data-stu-id="c2638-205">Click Find next.</span></span>
29. <span data-ttu-id="c2638-206">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="c2638-206">Click OK.</span></span>
30. <span data-ttu-id="c2638-207">Í svæði Finna færirðu inn „Greiðslur“.</span><span class="sxs-lookup"><span data-stu-id="c2638-207">In the Find field, type 'Payments'.</span></span>
31. <span data-ttu-id="c2638-208">Smellt er á Finna næsta.</span><span class="sxs-lookup"><span data-stu-id="c2638-208">Click Find next.</span></span>
32. <span data-ttu-id="c2638-209">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2638-209">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="c2638-210">Í svæðið Heiti, færðu inn ‚skuldari'.</span><span class="sxs-lookup"><span data-stu-id="c2638-210">In the Name field, type 'Debtor'.</span></span> 
34. <span data-ttu-id="c2638-211">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2638-211">Click Add.</span></span>
35. <span data-ttu-id="c2638-212">Í svæðinu Lýsing, færðu inn „Aðili sem skuldar lánveitanda (til þrautavara) tiltekna fjárhæð“.</span><span class="sxs-lookup"><span data-stu-id="c2638-212">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
36. <span data-ttu-id="c2638-213">Smellt er á Skipta um vörutilvísun.</span><span class="sxs-lookup"><span data-stu-id="c2638-213">Click Switch item reference.</span></span>
37. <span data-ttu-id="c2638-214">Í svæði Finna færirðu inn „Aðili“.</span><span class="sxs-lookup"><span data-stu-id="c2638-214">In the Find field, type 'Party'.</span></span>
38. <span data-ttu-id="c2638-215">Smellt er á Finna næsta.</span><span class="sxs-lookup"><span data-stu-id="c2638-215">Click Find next.</span></span>
39. <span data-ttu-id="c2638-216">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="c2638-216">Click OK.</span></span>
40. <span data-ttu-id="c2638-217">Smellt er á Finna næsta.</span><span class="sxs-lookup"><span data-stu-id="c2638-217">Click Find next.</span></span>
41. <span data-ttu-id="c2638-218">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2638-218">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="c2638-219">Í reitnum Heiti skal færa inn ‚Lýsing'.</span><span class="sxs-lookup"><span data-stu-id="c2638-219">In the Name field, type 'Description'.</span></span>
43. <span data-ttu-id="c2638-220">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="c2638-220">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="c2638-221">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2638-221">Click Add.</span></span>
45. <span data-ttu-id="c2638-222">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2638-222">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="c2638-223">Í svæðið Heiti, færðu inn 'Gjaldmiðils'.</span><span class="sxs-lookup"><span data-stu-id="c2638-223">In the Name field, type 'Currency'.</span></span>
47. <span data-ttu-id="c2638-224">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2638-224">Click Add.</span></span>
48. <span data-ttu-id="c2638-225">Í svæði Lýsing slá inn „Gjaldmiðilskóði“.</span><span class="sxs-lookup"><span data-stu-id="c2638-225">In the Description field, enter 'Currency code'.</span></span>
49. <span data-ttu-id="c2638-226">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2638-226">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="c2638-227">Í reitnum Heiti skal færa inn ‚TransactionDate'.</span><span class="sxs-lookup"><span data-stu-id="c2638-227">In the Name field, type 'TransactionDate'.</span></span> 
51. <span data-ttu-id="c2638-228">Velja 'Dagsetning' í svæðinu gerð vöru.</span><span class="sxs-lookup"><span data-stu-id="c2638-228">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="c2638-229">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2638-229">Click Add.</span></span>
53. <span data-ttu-id="c2638-230">Í svæði Lýsing slá inn „Færsludagsetning“.</span><span class="sxs-lookup"><span data-stu-id="c2638-230">In the Description field, enter 'Transaction date'.</span></span> 
54. <span data-ttu-id="c2638-231">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2638-231">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="c2638-232">Í reitnum Heiti skal færa inn ‚InstructedAmount'.</span><span class="sxs-lookup"><span data-stu-id="c2638-232">In the Name field, type 'InstructedAmount'.</span></span>  
56. <span data-ttu-id="c2638-233">Veljið 'Raunveruleg' í svæðinu gerð vöru.</span><span class="sxs-lookup"><span data-stu-id="c2638-233">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="c2638-234">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2638-234">Click Add.</span></span>
58. <span data-ttu-id="c2638-235">Í svæðinu Lýsing, færðu inn „Peningafjárhæð sem á að færa á milli skuldara og lánardrottins, áður en frádráttur gjalda á sér stað“.</span><span class="sxs-lookup"><span data-stu-id="c2638-235">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="c2638-236">Upphæð skal sett fram í þeim gjaldmiðli sem upphafsaðili segir til um.</span><span class="sxs-lookup"><span data-stu-id="c2638-236">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>

    <span data-ttu-id="c2638-237">Peningafjárhæð sem á að færa á milli skuldara og lánardrottins, áður en frádráttur gjalda á sér stað.</span><span class="sxs-lookup"><span data-stu-id="c2638-237">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="c2638-238">Upphæð skal sett fram í þeim gjaldmiðli sem upphafsaðili segir til um</span><span class="sxs-lookup"><span data-stu-id="c2638-238">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  

59. <span data-ttu-id="c2638-239">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2638-239">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="c2638-240">Í svæðið Heiti, færðu inn 'End2EndID'.</span><span class="sxs-lookup"><span data-stu-id="c2638-240">In the Name field, type 'End2EndID'.</span></span> 
61. <span data-ttu-id="c2638-241">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="c2638-241">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="c2638-242">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2638-242">Click Add.</span></span>
63. <span data-ttu-id="c2638-243">Í svæði Lýsing, slá inn „Einkvæmt kenni sem úthlutað er af upphafsaðila“.</span><span class="sxs-lookup"><span data-stu-id="c2638-243">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="c2638-244">Þessi auðkenning er færð áfram, óbreytt, í gegnum alla keðjuna, enda á milli</span><span class="sxs-lookup"><span data-stu-id="c2638-244">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span> 
64. <span data-ttu-id="c2638-245">Í svæðið Heiti, færðu inn 'PaymentModel'.</span><span class="sxs-lookup"><span data-stu-id="c2638-245">In the Name field, type 'PaymentModel'.</span></span>

    <span data-ttu-id="c2638-246">Heiti PaymentModel stemmir sig af við með fyrirfram skilgreindum viðmót greiðsluskjámyndir.</span><span class="sxs-lookup"><span data-stu-id="c2638-246">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  

65. <span data-ttu-id="c2638-247">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="c2638-247">Click Save.</span></span>
66. <span data-ttu-id="c2638-248">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c2638-248">Close the page.</span></span>

