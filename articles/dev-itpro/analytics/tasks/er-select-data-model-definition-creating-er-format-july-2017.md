--- 
title: "Velja skilgreiningu gagnalíkans þegar snið er búið til fyrir rafræna skýrslugerð (ER)"
description: "Til að ljúka þessum skrefum í ferlinu verður fyrst að ljúka við ferlið Rafræn skýrslugerð Stofna skilgreiningarveitu og merkja hana sem virka."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e560daa19b30c3f12e2b7a414580f89c93dfc31a
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="select-data-model-definition-while-creating-format-for-electronic-reporting-er"></a><span data-ttu-id="19735-103">Velja skilgreiningu gagnalíkans þegar snið er búið til fyrir rafræna skýrslugerð (ER)</span><span class="sxs-lookup"><span data-stu-id="19735-103">Select data model definition while creating format for electronic reporting (ER)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="19735-104">Til að ljúka þessum skrefum í ferlinu verður fyrst að ljúka við ferlið Rafræn skýrslugerð Stofna skilgreiningarveitu og merkja hana sem virka.</span><span class="sxs-lookup"><span data-stu-id="19735-104">To complete the steps in this procedure, you must first complete the procedure, ER Create a configuration provider and mark it as active.</span></span> 

<span data-ttu-id="19735-105">Þetta ferli sýnir hvernig rótaratriði líkans getu verið valið sem skilgreining gagnalíkans fyrir innsetningu Rafræn skýrslugerð (ER) grunnstilling sniðs sem er hönnuð til að búa til rafræn skjöl.</span><span class="sxs-lookup"><span data-stu-id="19735-105">This procedure shows how a model’s root item can be selected as a data model definition for inserting an Electronic reporting (ER) format configuration that is designed to generate electronic documents.</span></span> <span data-ttu-id="19735-106">Í þessu dæmi muntu bæta við nýrri Rafræn skýrslugerð grunnstilling sniðs fyrir sýnifyrirtækið, Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="19735-106">In this procedure, you will add a new ER format configuration for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="19735-107">Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="19735-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="19735-108">Skrefin er hægt að klára með því að nota öll gagnasöfn.</span><span class="sxs-lookup"><span data-stu-id="19735-108">The steps can be completed by using any dataset.</span></span>

1. <span data-ttu-id="19735-109">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="19735-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="19735-110">Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt Virk.</span><span class="sxs-lookup"><span data-stu-id="19735-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="19735-111">Ef þú sérð skilgreiningarveituna ekki, skal klára skrefin í ferlinu, Stofna skilgreiningarveitu og merkja hana sem virka.</span><span class="sxs-lookup"><span data-stu-id="19735-111">If you don’t see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  
2. <span data-ttu-id="19735-112">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="19735-112">Click Reporting configurations.</span></span>

## <a name="add-a-new-er-data-model-configuration"></a><span data-ttu-id="19735-113">Bæta við nýrri grunnstillingu gagnalíkans í Rafræn skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="19735-113">Add a new ER data model configuration</span></span>
1. <span data-ttu-id="19735-114">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="19735-114">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="19735-115">Við bætum við nýju Rafræn skýrslugerð grunnstillingarlíkani sem inniheldur gagnalíkan sem er hannað til notkunar sem gagnaveita fyrir tilbúning skýrslna Rafræn skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="19735-115">We add a new ER model configuration containing a data model that is designed to be used as data source for generation ER reports.</span></span>  
2. <span data-ttu-id="19735-116">Í reitnum Heiti skal færa inn „Greiðslulíkan (ímyndað).</span><span class="sxs-lookup"><span data-stu-id="19735-116">In the Name field, type 'Payment model (fictitious)'.</span></span>
    * <span data-ttu-id="19735-117">Greiðslulíkan (ímyndað)</span><span class="sxs-lookup"><span data-stu-id="19735-117">Payment model (fictitious)</span></span>  
3. <span data-ttu-id="19735-118">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="19735-118">Click Create configuration.</span></span>
4. <span data-ttu-id="19735-119">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="19735-119">Click Designer.</span></span>
    * <span data-ttu-id="19735-120">Opna hönnuður Rafræn skýrslugerð til að tilgreina skipan gagnalíkans þessarar grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="19735-120">Open the ER designer to specify the structure of data model of this configuration.</span></span>  
    * <span data-ttu-id="19735-121">Gera ráð fyrir að við hönnum gagnalíkan fyrir greiðslur viðskiptalén til stuðnings 2 greiðsluaðferðum – kreditfærslum og beingreiðslum.</span><span class="sxs-lookup"><span data-stu-id="19735-121">Assume that we design the data model for payments business domain to support 2 payment methods – credit transfer and direct debit ones.</span></span>  
5. <span data-ttu-id="19735-122">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="19735-122">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="19735-123">Í svæðið Heiti, færðu inn „Greiðslur – kreditfærsla“.</span><span class="sxs-lookup"><span data-stu-id="19735-123">In the Name field, type 'Payments – credit transfer'.</span></span>
    * <span data-ttu-id="19735-124">Greiðslur – kreditfærsla</span><span class="sxs-lookup"><span data-stu-id="19735-124">Payments – credit transfer</span></span>  
7. <span data-ttu-id="19735-125">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="19735-125">Click Add.</span></span>
8. <span data-ttu-id="19735-126">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="19735-126">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="19735-127">Í svæði Nýr hnútur sem, slá inn „Líkanshnútur“.</span><span class="sxs-lookup"><span data-stu-id="19735-127">In the New node as a field, enter 'Model root'.</span></span>
10. <span data-ttu-id="19735-128">Í reitnum Heiti skal færa inn „Greiðslur – beingreiðsla“.</span><span class="sxs-lookup"><span data-stu-id="19735-128">In the Name field, type 'Payments – direct debit'.</span></span>
    * <span data-ttu-id="19735-129">Greiðslur - beingreiðsla</span><span class="sxs-lookup"><span data-stu-id="19735-129">Payments – direct debit</span></span>  
11. <span data-ttu-id="19735-130">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="19735-130">Click Add.</span></span>
12. <span data-ttu-id="19735-131">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="19735-131">Click Save.</span></span>
13. <span data-ttu-id="19735-132">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="19735-132">Close the page.</span></span>
14. <span data-ttu-id="19735-133">Smellið á „Breyta stöðu“.</span><span class="sxs-lookup"><span data-stu-id="19735-133">Click Change status.</span></span>
    * <span data-ttu-id="19735-134">Ljúka við drög útgáfu af líkaninu til að gera það tiltækt í nýjum líkan vörpunum og sniðum.</span><span class="sxs-lookup"><span data-stu-id="19735-134">Complete the draft version of the model to make it available in new model mappings and formats.</span></span>  
15. <span data-ttu-id="19735-135">Smelltu á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="19735-135">Click Complete.</span></span>
16. <span data-ttu-id="19735-136">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="19735-136">Click OK.</span></span>

## <a name="start-to-enter-a-new-er-format-configuration"></a><span data-ttu-id="19735-137">Byrja að færa inn nýja grunnstillingu sniðs í Rafræn skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="19735-137">Start to enter a new ER format configuration</span></span>
1. <span data-ttu-id="19735-138">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="19735-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="19735-139">Í svæði Nýtt skal slá inn „Snið byggir á gagnalíkani Greiðslulíkan (ímyndað)“.</span><span class="sxs-lookup"><span data-stu-id="19735-139">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="19735-140">Í reitinn Skilgreining Gagnalíkans skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="19735-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="19735-141">Athugið að öll rótaratriði hins valda gagnalíkans eru nú tiltæk í valmöguleikum sem skilgreining gagnalíkans.</span><span class="sxs-lookup"><span data-stu-id="19735-141">Note that all root items of the selected data model are currently available for selection as a data model definition.</span></span> <span data-ttu-id="19735-142">Þú getur haldið áfram að hanna eigið snið með með því að nota eitthvað af þeim rótaratriðum gagnalíkans sem er krafist.</span><span class="sxs-lookup"><span data-stu-id="19735-142">You can continue to design your format by using any of the required root items of the data model.</span></span> <span data-ttu-id="19735-143">Það að vörpun líkans fyrir valið rótaratriði vanti mun ekki hindra þig í að halda áfram.</span><span class="sxs-lookup"><span data-stu-id="19735-143">A missing model mapping for the selected root item doesn't prevent you from continuing.</span></span>  
4. <span data-ttu-id="19735-144">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="19735-144">Close the page.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="19735-145">Bæta við nýrri grunnstillingu líkan vörpun í Rafræn skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="19735-145">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="19735-146">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="19735-146">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="19735-147">Í svæði Nýtt skal slá inn „Vörpun líkans byggir á gagnalíkani Greiðslulíkan (ímyndað)“.</span><span class="sxs-lookup"><span data-stu-id="19735-147">In the New field, enter 'Model Mapping based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="19735-148">Í reitnum Heiti skal færa inn „Vörpun greiðslulíkans (ímyndað)“.</span><span class="sxs-lookup"><span data-stu-id="19735-148">In the Name field, type 'Payment model mappings (fictitious)'.</span></span>
    * <span data-ttu-id="19735-149">Varpanir greiðslulíkans (ímynduð)</span><span class="sxs-lookup"><span data-stu-id="19735-149">Payment model mappings (fictitious)</span></span>  
4. <span data-ttu-id="19735-150">Í reitinn Skilgreining Gagnalíkans skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="19735-150">In the Data model definition field, enter or select a value.</span></span>
5. <span data-ttu-id="19735-151">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="19735-151">Click Create configuration.</span></span>

## <a name="design-er-model-mappings"></a><span data-ttu-id="19735-152">Hanna Vörpun líkans í Rafræn skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="19735-152">Design ER model mappings</span></span>
1. <span data-ttu-id="19735-153">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="19735-153">Click Designer.</span></span>
    * <span data-ttu-id="19735-154">Nota hönnuður Rafræn skýrslugerð til að tilgreina líkan varpanir fyrir þau atriði rótar sem er krafist.</span><span class="sxs-lookup"><span data-stu-id="19735-154">Use the ER designer to specify the model mappings for the required root items.</span></span>  
2. <span data-ttu-id="19735-155">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="19735-155">Click Designer.</span></span>
    * <span data-ttu-id="19735-156">Herma eftir stillingum valinna líkan varpanir fyrir valin rótaratriði líkans.</span><span class="sxs-lookup"><span data-stu-id="19735-156">Simulate setting of selected model mapping for the selected model’s root item.</span></span>  
3. <span data-ttu-id="19735-157">Í trénu skal velja „Dynamics 365 for Operations\Tafla færslur“.</span><span class="sxs-lookup"><span data-stu-id="19735-157">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
4. <span data-ttu-id="19735-158">Smella á bæta Við rót.</span><span class="sxs-lookup"><span data-stu-id="19735-158">Click Add root.</span></span>
5. <span data-ttu-id="19735-159">Í svæðið Heiti, færðu inn „Fjárhagur“.</span><span class="sxs-lookup"><span data-stu-id="19735-159">In the Name field, type 'Ledger'.</span></span>
6. <span data-ttu-id="19735-160">Í reitnum Tafla skal færa inn ‚LedgerJournalTrans‘.</span><span class="sxs-lookup"><span data-stu-id="19735-160">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="19735-161">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="19735-161">LedgerJournalTrans</span></span>  
7. <span data-ttu-id="19735-162">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="19735-162">Click OK.</span></span>
8. <span data-ttu-id="19735-163">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="19735-163">Click Save.</span></span>
9. <span data-ttu-id="19735-164">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="19735-164">Close the page.</span></span>
10. <span data-ttu-id="19735-165">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="19735-165">Close the page.</span></span>

## <a name="start-to-enter-another-new-er-format-configuration"></a><span data-ttu-id="19735-166">Byrja að færa inn aðra nýja grunnstillingu sniðs í Rafræn skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="19735-166">Start to enter another new ER format configuration</span></span>
1. <span data-ttu-id="19735-167">Í trénu skal velja „Greiðslulíkan (ímyndað)“.</span><span class="sxs-lookup"><span data-stu-id="19735-167">In the tree, select 'Payment model (fictitious)'.</span></span>
2. <span data-ttu-id="19735-168">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="19735-168">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="19735-169">Í svæði Nýtt skal slá inn „Snið byggir á gagnalíkani Greiðslulíkan (ímyndað)“.</span><span class="sxs-lookup"><span data-stu-id="19735-169">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
4. <span data-ttu-id="19735-170">Í reitinn Skilgreining Gagnalíkans skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="19735-170">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="19735-171">Athugið að aðeins eitt rótaratriði er tiltækt til vörpunar yfir í gagnaveitu forritsins.</span><span class="sxs-lookup"><span data-stu-id="19735-171">Note that now only one root item is available to map to the application data sources.</span></span> <span data-ttu-id="19735-172">Þegar að minnsta kosti ein vörpun líkans er lögð fram, er aðeins hægt að velja þau rótaratriði líkansins sem er varpað yfir í gagnaveitu forritsins, sem skilgreiningu líkans um leið og sniði Rafræn skýrslugerð er bætt við.</span><span class="sxs-lookup"><span data-stu-id="19735-172">When at least one model mapping is introduced, only the model’s root items that are mapped to application data sources can be selected as a model definition while the ER format is added.</span></span>   
5. <span data-ttu-id="19735-173">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="19735-173">Close the page.</span></span>


