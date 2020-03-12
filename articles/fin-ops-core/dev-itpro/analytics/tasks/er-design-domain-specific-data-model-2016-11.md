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
ms.openlocfilehash: d7882a7a17f5736d9d5a11cd91ac963fa89ff12f
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042897"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="c2ffd-103">Rafræn skýrslugerð Hanna lénasértæk gagnalíkön</span><span class="sxs-lookup"><span data-stu-id="c2ffd-103">ER Design domain specific data model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c2ffd-104">Eftirfarandi skref útskýra hvernig notandi úthlutað á hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað nýja skilgreiningarveitu fyrir rafræna skýrslugerð (ER) sem inniheldur gagnalíkan fyrir rafræn greiðsluskjöl.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="c2ffd-105">Þessi gagnalíkan verður notaður síðar sem gagnaveita þegar snið fyrir greiðsluskjölin eru stofnuð.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>

<span data-ttu-id="c2ffd-106">Í þessu dæmi, verður að stofna skilgreiningu fyrir dæmi um fyrirtæki, Litware, Inc. Þessi skref má framkvæma í hvaða fyrirtæki sem er þar sem ER skilgreiningar eru samnýttar á milli fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="c2ffd-107">Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu "Stofna skilgreiningarveitu og merkja hana sem virka".</span><span class="sxs-lookup"><span data-stu-id="c2ffd-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

1. <span data-ttu-id="c2ffd-108">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="c2ffd-109">Veldu skilgreiningarveitu fyrir dæmi um fyrirtæki, Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-109">Select the configuration provider for sample company, ‘Litware, Inc.’</span></span> <span data-ttu-id="c2ffd-110">Ef ekki sést þessi skilgreiningarveita, verður fyrst að ljúka við skrefin í ferlinu "Stofna skilgreiningarveitu og merkja hana sem virka".</span><span class="sxs-lookup"><span data-stu-id="c2ffd-110">If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
    
2. <span data-ttu-id="c2ffd-111">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="c2ffd-111">Click Reporting configurations.</span></span>

    <span data-ttu-id="c2ffd-112">Stofna verður skilgreiningu sem inniheldur gagnalíkan fyrir rafræna greiðsluskjöl.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="c2ffd-113">Þessi gagnalíkan verður notaður síðar sem gagnaveita þegar snið fyrir greiðsluskjölin.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="c2ffd-114">Stofna nýjan skilgreiningu gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="c2ffd-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="c2ffd-115">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="c2ffd-116">Í svæðið Heiti, færðu inn "Greiðslur (einfaldaður líkan)".</span><span class="sxs-lookup"><span data-stu-id="c2ffd-116">In the Name field, type 'Payments (simplified model)'.</span></span>
3. <span data-ttu-id="c2ffd-117">Færðu inn 'Skilgreining greiðslulíkans' í svæðinu Lýsingu.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-117">In the Description field, type 'Payment model configuration'.</span></span>

    <span data-ttu-id="c2ffd-118">Virkt skilgreiningarveitu er sjálfkrafa færð inn hér.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-118">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="c2ffd-119">Þessa veitu mun geta unnið með þessa skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-119">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="c2ffd-120">Önnur veitur er hægt að nota þetta skilgreining, en geta ekki unnið með hana.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-120">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

4. <span data-ttu-id="c2ffd-121">Smellið á hnappinn "Stofna skilgreiningu" að ljúka verkinu fyrir stofnun skilgreiningar</span><span class="sxs-lookup"><span data-stu-id="c2ffd-121">Click ‘Create configuration’ button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="c2ffd-122">Stofna gagnalíkan</span><span class="sxs-lookup"><span data-stu-id="c2ffd-122">Create a data model</span></span>
<span data-ttu-id="c2ffd-123">Verið er að búa til nýtt gagnalíkan fyrir valda grunnstillingu.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-123">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="c2ffd-124">Þessi útgáfa skilgreiningarinnar mun hafa stöðuna drög.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-124">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="c2ffd-125">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-125">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="c2ffd-126">Skilgreina uppbygging aðila sem er í greiðsluferli</span><span class="sxs-lookup"><span data-stu-id="c2ffd-126">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="c2ffd-127">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-127">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="c2ffd-128">Í svæði Nafn færirðu inn „Aðili“.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-128">In the Name field, type 'Party'.</span></span>
3. <span data-ttu-id="c2ffd-129">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-129">Click Add.</span></span>
4. <span data-ttu-id="c2ffd-130">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-130">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="c2ffd-131">Í svæðið Heiti, færðu inn ‚Heiti'.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-131">In the Name field, type 'Name'.</span></span>
6. <span data-ttu-id="c2ffd-132">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-132">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="c2ffd-133">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-133">Click Add.</span></span>
8. <span data-ttu-id="c2ffd-134">Í svæði Finna færirðu inn „Aðili“.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-134">In the Find field, type 'Party'.</span></span>
9. <span data-ttu-id="c2ffd-135">Smelltu á Finna fyrri.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-135">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="c2ffd-136">Skilgreina skipulag banka fyrir þetta líkan</span><span class="sxs-lookup"><span data-stu-id="c2ffd-136">Define the bank structure for this model</span></span>
1. <span data-ttu-id="c2ffd-137">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-137">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="c2ffd-138">Í svæðið Heiti, færðu inn ‚umboðsmaður'.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-138">In the Name field, type 'Agent'.</span></span>
3. <span data-ttu-id="c2ffd-139">Veljið 'Færslan' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-139">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="c2ffd-140">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-140">Click Add.</span></span>
5. <span data-ttu-id="c2ffd-141">Í svæði Lýsing, færðu inn „Fjárhagsstofnun“ (til dæmis, banki) sem þjónustar lykil fyrir aðila (skuldari/lánardrottinn).</span><span class="sxs-lookup"><span data-stu-id="c2ffd-141">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>

    <span data-ttu-id="c2ffd-142">Fjárhagsstofnun (til dæmis, banki) sem þjónustar lykil fyrir aðila (skuldara/lánardrottin).</span><span class="sxs-lookup"><span data-stu-id="c2ffd-142">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  

6. <span data-ttu-id="c2ffd-143">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-143">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="c2ffd-144">Í svæðið Heiti, færðu inn ‚Heiti'.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-144">In the Name field, type 'Name'.</span></span> 
8. <span data-ttu-id="c2ffd-145">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-145">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="c2ffd-146">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-146">Click Add.</span></span>
10. <span data-ttu-id="c2ffd-147">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-147">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="c2ffd-148">Í svæðið Heiti, færðu inn ‚SWIFT'.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-148">In the Name field, type 'SWIFT'.</span></span>
12. <span data-ttu-id="c2ffd-149">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-149">Click Add.</span></span>
13. <span data-ttu-id="c2ffd-150">Í svæði Lýsing slá inn „Auðkenniskóði banka“.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-150">In the Description field, enter 'Bank identification code'.</span></span> 
14. <span data-ttu-id="c2ffd-151">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-151">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="c2ffd-152">Í svæðið Heiti, færðu inn 'RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-152">In the Name field, type 'RoutingNumber'.</span></span>
16. <span data-ttu-id="c2ffd-153">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-153">Click Add.</span></span>
17. <span data-ttu-id="c2ffd-154">Í svæði Lýsing slá inn „Leiðarnúmer“.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-154">In the Description field, enter 'Routing number'.</span></span>
18. <span data-ttu-id="c2ffd-155">Smelltu á Finna fyrri.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-155">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="c2ffd-156">Skilgreina skipulag bankareikning fyrir þetta líkan</span><span class="sxs-lookup"><span data-stu-id="c2ffd-156">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="c2ffd-157">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-157">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="c2ffd-158">Í reitnum Heiti skal færa inn 'Bankareikningur'.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-158">In the Name field, type 'Account'.</span></span> 
3. <span data-ttu-id="c2ffd-159">Veljið 'Færslan' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-159">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="c2ffd-160">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-160">Click Add.</span></span>
5. <span data-ttu-id="c2ffd-161">Í svæði Lýsing slá inn „Auðkenning lykils hjá aðila í fjármálastofnun (t.d. banka)“.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-161">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>

    <span data-ttu-id="c2ffd-162">Auðkenning lykils hjá aðila í fjármálastofnun (t.d. banka).</span><span class="sxs-lookup"><span data-stu-id="c2ffd-162">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  

6. <span data-ttu-id="c2ffd-163">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-163">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="c2ffd-164">Í svæðið Heiti, færðu inn 'Gjaldmiðils'.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-164">In the Name field, type 'Currency'.</span></span> 
8. <span data-ttu-id="c2ffd-165">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-165">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="c2ffd-166">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-166">Click Add.</span></span>
10. <span data-ttu-id="c2ffd-167">Í svæði Lýsing slá inn „Gjaldmiðilskóði“.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-167">In the Description field, enter 'Currency code'.</span></span>
11. <span data-ttu-id="c2ffd-168">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-168">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="c2ffd-169">Í svæðið Heiti, færðu inn ‚númer'.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-169">In the Name field, type 'Number'.</span></span> 
13. <span data-ttu-id="c2ffd-170">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-170">Click Add.</span></span>
14. <span data-ttu-id="c2ffd-171">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-171">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="c2ffd-172">Í svæðið Heiti, færðu inn ‚IBAN-númer'.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-172">In the Name field, type 'IBAN'.</span></span> 
16. <span data-ttu-id="c2ffd-173">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-173">Click Add.</span></span>
17. <span data-ttu-id="c2ffd-174">Í svæði Lýsing slá inn „Alþjóðlegt bankareikningsnúmer“.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-174">In the Description field, enter 'International bank account number'.</span></span>

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="c2ffd-175">Skilgreina uppbygging greiðsluskilaboða fyrir greiðslugerð kreditfærslu</span><span class="sxs-lookup"><span data-stu-id="c2ffd-175">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="c2ffd-176">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-176">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="c2ffd-177">Í svæði Nýr hnútur sem, slá inn „Líkanshnútur“.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-177">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="c2ffd-178">Í svæðið Heiti, Færðu inn 'CustomerCreditTransferInitiation'.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-178">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
4. <span data-ttu-id="c2ffd-179">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-179">Click Add.</span></span>
5. <span data-ttu-id="c2ffd-180">Í svæði Finna, slá inn „CustomerCreditTransferInitiation“.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-180">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span> 
6. <span data-ttu-id="c2ffd-181">Smelltu á Finna fyrri.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-181">Click Find previous.</span></span>
7. <span data-ttu-id="c2ffd-182">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-182">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="c2ffd-183">Í svæðið Heiti, færðu inn 'MessageIdentification'.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-183">In the Name field, type 'MessageIdentification'.</span></span> 
9. <span data-ttu-id="c2ffd-184">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-184">Click Add.</span></span>
10. <span data-ttu-id="c2ffd-185">Í svæði Lýsing, færið inn Tilvísun frá einum stað til annars, eins og úthlutað er af hálfu leiðbeinandi aðila, (og send til næsta aðila í röðinni) til að auðkenna skilaboðin.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-185">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>

    <span data-ttu-id="c2ffd-186">Tilvísun frá einum stað til annars, eins og úthlutað er af hálfu leiðbeinandi aðila, (og send til næsta aðila í röðinni) til að auðkenna skilaboðin.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-186">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  

11. <span data-ttu-id="c2ffd-187">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-187">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="c2ffd-188">Í svæðið Heiti, færðu in 'ProcessingDateTime'.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-188">In the Name field, type 'ProcessingDateTime'.</span></span>
13. <span data-ttu-id="c2ffd-189">Velja 'DateTime' í svæðinu gerð Vöru.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-189">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="c2ffd-190">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-190">Click Add.</span></span>
15. <span data-ttu-id="c2ffd-191">Í svæðinu Lýsing færa inn „Dagsetningu og tíma sem greiðsluskilaboðin var stofnuð“.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-191">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span> 
16. <span data-ttu-id="c2ffd-192">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-192">Click New to open the drop dialog.</span></span>

    <span data-ttu-id="c2ffd-193">Skilgreina skipulag greiðslufærsla fyrir þetta líkan.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-193">Define the payment transaction structure for this model.</span></span>  

17. <span data-ttu-id="c2ffd-194">Í svæðið Heiti, færðu inn 'Greiðslur'.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-194">In the Name field, type 'Payments'.</span></span>
18. <span data-ttu-id="c2ffd-195">Veljið í svæðinu gerð Vöru „Skrárlisti".</span><span class="sxs-lookup"><span data-stu-id="c2ffd-195">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="c2ffd-196">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-196">Click Add.</span></span>
20. <span data-ttu-id="c2ffd-197">Færið inn 'Greiðslulínur fyrir gildandi skilaboð' í svæðinu Lýsingu.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-197">In the Description field, enter 'Payment lines of the current message'.</span></span>
21. <span data-ttu-id="c2ffd-198">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-198">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="c2ffd-199">Í svæðið Heiti, færðu inn 'Lánardrottins'.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-199">In the Name field, type 'Creditor'.</span></span> 
23. <span data-ttu-id="c2ffd-200">Veljið 'Færslan' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-200">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="c2ffd-201">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-201">Click Add.</span></span>
25. <span data-ttu-id="c2ffd-202">Færið inn „Aðili sem á að taka á móti fjárhæð“ í svæðinu Lýsingu.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-202">In the Description field, enter 'Party to which an amount of money is due.'.</span></span> 
26. <span data-ttu-id="c2ffd-203">Smellt er á Skipta um vörutilvísun.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-203">Click Switch item reference.</span></span>
27. <span data-ttu-id="c2ffd-204">Í svæði Finna færirðu inn „Aðili“.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-204">In the Find field, type 'Party'.</span></span>
28. <span data-ttu-id="c2ffd-205">Smellt er á Finna næsta.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-205">Click Find next.</span></span>
29. <span data-ttu-id="c2ffd-206">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-206">Click OK.</span></span>
30. <span data-ttu-id="c2ffd-207">Í svæði Finna færirðu inn „Greiðslur“.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-207">In the Find field, type 'Payments'.</span></span>
31. <span data-ttu-id="c2ffd-208">Smellt er á Finna næsta.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-208">Click Find next.</span></span>
32. <span data-ttu-id="c2ffd-209">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-209">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="c2ffd-210">Í svæðið Heiti, færðu inn ‚skuldari'.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-210">In the Name field, type 'Debtor'.</span></span> 
34. <span data-ttu-id="c2ffd-211">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-211">Click Add.</span></span>
35. <span data-ttu-id="c2ffd-212">Í svæðinu Lýsing, færðu inn „Aðili sem skuldar lánveitanda (til þrautavara) tiltekna fjárhæð“.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-212">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
36. <span data-ttu-id="c2ffd-213">Smellt er á Skipta um vörutilvísun.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-213">Click Switch item reference.</span></span>
37. <span data-ttu-id="c2ffd-214">Í svæði Finna færirðu inn „Aðili“.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-214">In the Find field, type 'Party'.</span></span>
38. <span data-ttu-id="c2ffd-215">Smellt er á Finna næsta.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-215">Click Find next.</span></span>
39. <span data-ttu-id="c2ffd-216">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-216">Click OK.</span></span>
40. <span data-ttu-id="c2ffd-217">Smellt er á Finna næsta.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-217">Click Find next.</span></span>
41. <span data-ttu-id="c2ffd-218">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-218">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="c2ffd-219">Í reitnum Heiti skal færa inn ‚Lýsing'.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-219">In the Name field, type 'Description'.</span></span>
43. <span data-ttu-id="c2ffd-220">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-220">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="c2ffd-221">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-221">Click Add.</span></span>
45. <span data-ttu-id="c2ffd-222">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-222">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="c2ffd-223">Í svæðið Heiti, færðu inn 'Gjaldmiðils'.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-223">In the Name field, type 'Currency'.</span></span>
47. <span data-ttu-id="c2ffd-224">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-224">Click Add.</span></span>
48. <span data-ttu-id="c2ffd-225">Í svæði Lýsing slá inn „Gjaldmiðilskóði“.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-225">In the Description field, enter 'Currency code'.</span></span>
49. <span data-ttu-id="c2ffd-226">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-226">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="c2ffd-227">Í reitnum Heiti skal færa inn ‚TransactionDate'.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-227">In the Name field, type 'TransactionDate'.</span></span> 
51. <span data-ttu-id="c2ffd-228">Velja 'Dagsetning' í svæðinu gerð vöru.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-228">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="c2ffd-229">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-229">Click Add.</span></span>
53. <span data-ttu-id="c2ffd-230">Í svæði Lýsing slá inn „Færsludagsetning“.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-230">In the Description field, enter 'Transaction date'.</span></span> 
54. <span data-ttu-id="c2ffd-231">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-231">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="c2ffd-232">Í reitnum Heiti skal færa inn ‚InstructedAmount'.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-232">In the Name field, type 'InstructedAmount'.</span></span>  
56. <span data-ttu-id="c2ffd-233">Veljið 'Raunveruleg' í svæðinu gerð vöru.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-233">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="c2ffd-234">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-234">Click Add.</span></span>
58. <span data-ttu-id="c2ffd-235">Í svæðinu Lýsing, færðu inn „Peningafjárhæð sem á að færa á milli skuldara og lánardrottins, áður en frádráttur gjalda á sér stað“.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-235">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="c2ffd-236">Upphæð skal sett fram í þeim gjaldmiðli sem upphafsaðili segir til um.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-236">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>

    <span data-ttu-id="c2ffd-237">Peningafjárhæð sem á að færa á milli skuldara og lánardrottins, áður en frádráttur gjalda á sér stað.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-237">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="c2ffd-238">Upphæð skal sett fram í þeim gjaldmiðli sem upphafsaðili segir til um</span><span class="sxs-lookup"><span data-stu-id="c2ffd-238">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  

59. <span data-ttu-id="c2ffd-239">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-239">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="c2ffd-240">Í svæðið Heiti, færðu inn 'End2EndID'.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-240">In the Name field, type 'End2EndID'.</span></span> 
61. <span data-ttu-id="c2ffd-241">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-241">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="c2ffd-242">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-242">Click Add.</span></span>
63. <span data-ttu-id="c2ffd-243">Í svæði Lýsing, slá inn „Einkvæmt kenni sem úthlutað er af upphafsaðila“.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-243">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="c2ffd-244">Þessi auðkenning er færð áfram, óbreytt, í gegnum alla keðjuna, enda á milli</span><span class="sxs-lookup"><span data-stu-id="c2ffd-244">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span> 
64. <span data-ttu-id="c2ffd-245">Í svæðið Heiti, færðu inn 'PaymentModel'.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-245">In the Name field, type 'PaymentModel'.</span></span>

    <span data-ttu-id="c2ffd-246">Heiti PaymentModel stemmir sig af við með fyrirfram skilgreindum viðmót greiðsluskjámyndir.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-246">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  

65. <span data-ttu-id="c2ffd-247">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-247">Click Save.</span></span>
66. <span data-ttu-id="c2ffd-248">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-248">Close the page.</span></span>

