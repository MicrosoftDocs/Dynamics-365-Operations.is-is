---
title: Búa til og uppfæra reglu um skil og endurgreiðslur fyrir rás
description: Þetta efni útskýrir hvernig á að setja upp skil og endurgreiðslu stefnu fyrir rás.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: c2a9325f09ffe43c3436b7e0ca2ab511e1f57f83
ms.sourcegitcommit: 02640a0f63daa9e509146641824ed623c4d69c7f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/16/2020
ms.locfileid: "3265585"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a><span data-ttu-id="702bf-103">Búa til og uppfæra reglu um skil og endurgreiðslur fyrir rás</span><span class="sxs-lookup"><span data-stu-id="702bf-103">Create and update a returns and refunds policy for a channel</span></span>

[!include [banner](includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="702bf-104">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="702bf-104">Overview</span></span>

<span data-ttu-id="702bf-105">Return stefnu rásarinnar í Dynamics 365 Commerce gerir smásöluaðilum kleift að stilla framfylgni þar sem hægt er að leyfa greiðslutilboð til að vinna úr skilum á sölustað (POS) tæki.</span><span class="sxs-lookup"><span data-stu-id="702bf-105">The channel return policy in Dynamics 365 Commerce enables retailers to set enforcements on which payment tenders can be allowed for processing a return on a point of sale (POS) device.</span></span>  

<span data-ttu-id="702bf-106">Þetta efni lýsir þrepunum til að setja upp skil og endurgreiðslu stefnu fyrir rás.</span><span class="sxs-lookup"><span data-stu-id="702bf-106">This topic describes the steps to set up a returns and refunds policy for a channel.</span></span>

<span data-ttu-id="702bf-107">Umfang stefnunnar er sem stendur takmarkað við að setja greiðslutilboð sem hægt er að leyfa fyrir rás.</span><span class="sxs-lookup"><span data-stu-id="702bf-107">The scope of the policy is currently limited to setting the payment tenders that can be allowed for a channel.</span></span> <span data-ttu-id="702bf-108">Listinn „leyfður“ er byggður á greiðslumáta sem notaðir voru við kaupin.</span><span class="sxs-lookup"><span data-stu-id="702bf-108">The "allowed" list is based on the payment methods used to make the purchase.</span></span> <span data-ttu-id="702bf-109">Dæmi:</span><span class="sxs-lookup"><span data-stu-id="702bf-109">For example:</span></span>

- <span data-ttu-id="702bf-110">Ef kaup voru gerð með gjafakorti er verslunin stefna að afgreiða endurgreiðslur aðeins á nýju gjafakorti eða veita lánsfé.</span><span class="sxs-lookup"><span data-stu-id="702bf-110">If a purchase was made using a gift card, the store policy is to process refunds only to a new gift card or to give store credit.</span></span> 
- <span data-ttu-id="702bf-111">Ef sala fer fram með reiðufé eru möguleikarnir sem eru leyfðir til endurgreiðslu reiðufé, gjafakort og viðskiptareikningur en ekki kreditkort.</span><span class="sxs-lookup"><span data-stu-id="702bf-111">If a sale is made using cash, the options allowed for refund are cash, gift card, and customer account, but not credit card.</span></span> 


## <a name="enable-return-policy"></a><span data-ttu-id="702bf-112">Virkja skilareglu</span><span class="sxs-lookup"><span data-stu-id="702bf-112">Enable return policy</span></span>

<span data-ttu-id="702bf-113">Gerðu eftirfarandi til að virkja skilareglu rásarvirkninnar:</span><span class="sxs-lookup"><span data-stu-id="702bf-113">To enable the channel return policy functionality, do the following:</span></span>

1. <span data-ttu-id="702bf-114">Farðu í vinnusvæðið **Eiginleikastjórnun** í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="702bf-114">Go to the **Feature Management** workspace in Dynamics 365 Commerce.</span></span>
2. <span data-ttu-id="702bf-115">Leitaðu að eiginleikanum **Virkja skilareglur rása** á listanum yfir heiti eiginleika.</span><span class="sxs-lookup"><span data-stu-id="702bf-115">Search for the **Enable channel return policies** feature in the list of feature names.</span></span>
3. <span data-ttu-id="702bf-116">Veldu **Virkja núna**.</span><span class="sxs-lookup"><span data-stu-id="702bf-116">Select **Enable now**.</span></span> 

## <a name="configure-return-policy"></a><span data-ttu-id="702bf-117">Stilla skilareglu</span><span class="sxs-lookup"><span data-stu-id="702bf-117">Configure return policy</span></span>

<span data-ttu-id="702bf-118">Fylgdu þessum skrefum til að stilla aftur stefnu fyrir smásöluverslun eða netverslun.</span><span class="sxs-lookup"><span data-stu-id="702bf-118">Follow these steps to configure a return policy for a retail store or online retail channel.</span></span>

1. <span data-ttu-id="702bf-119">Farðu í **Verslun og verslun** \> **Uppsetning rásar** \> **Skilar** \> **Skilastefna rásarinnar**.</span><span class="sxs-lookup"><span data-stu-id="702bf-119">Go to **Retail and Commerce** \> **Channel Setup** \> **Returns** \> **Channel return policy**.</span></span>

2. <span data-ttu-id="702bf-120">Veldu **Nýtt** til að búa til nýtt sniðmát skilareglu.</span><span class="sxs-lookup"><span data-stu-id="702bf-120">Select **New** to create a new return policy template.</span></span> <span data-ttu-id="702bf-121">Veldu sniðmátið í vinstri glugganum til að nota sniðmát sem fyrir er.</span><span class="sxs-lookup"><span data-stu-id="702bf-121">To use an existing template, select the template in the left pane.</span></span> <span data-ttu-id="702bf-122">Fyrir ný sniðmát skaltu bæta við nafni og lýsingu sem mun hjálpa þér að bera kennsl á stefnuna þegar henni er beitt á rásina.</span><span class="sxs-lookup"><span data-stu-id="702bf-122">For new templates, add a name and description that will help you identify the policy when it is being applied to the channel.</span></span>

   <span data-ttu-id="702bf-123">![Bættu við nýrri skilareglu](media/Return-policy-page1.png "Bæta við nýrri skilareglu")</span><span class="sxs-lookup"><span data-stu-id="702bf-123">![Add new return policy](media/Return-policy-page1.png "Add new return rolicy")</span></span>
     
   
3. <span data-ttu-id="702bf-124">Í kaflanum **Leyfðar endurgreiðsluaðferðir**, skilgreina **Leyft** greiðslutilboðum skila sem eru sértæk fyrir hverja greiðslumáta.</span><span class="sxs-lookup"><span data-stu-id="702bf-124">In the **Allowed refund payment methods** section, define **Allowed** return payment tenders that are specific to each payment method.</span></span>
   <span data-ttu-id="702bf-125">![Bæta við greiðslumátum](media/Return-policy-page2.PNG "Stilltu leyfðar greiðslumáta fyrir hverja greiðslugerð")</span><span class="sxs-lookup"><span data-stu-id="702bf-125">![Add payment methods](media/Return-policy-page2.PNG "Set allowed payment methods per payment type")</span></span>
   
    > [!IMPORTANT]
    > - <span data-ttu-id="702bf-126">Greiðslumátarnir eru fengnir af þeim greiðslumáta sem settur er fyrir stofnunina.</span><span class="sxs-lookup"><span data-stu-id="702bf-126">The payment methods are derived from the payment methods set for the organization.</span></span>
    > - <span data-ttu-id="702bf-127">Með því að bæta við leyfðri útboðsgerð fyrir hverja skráða greiðslumáta verður tryggt að hægt sé að skila í leyfilega gerð útboðs.</span><span class="sxs-lookup"><span data-stu-id="702bf-127">Adding an allowed return tender type for each listed payment method will ensure that returns can be made to the allowed return tender type.</span></span>
    
4. <span data-ttu-id="702bf-128">Tengdu sniðmát skilareglu við verslanirnar þar sem það verður notað.</span><span class="sxs-lookup"><span data-stu-id="702bf-128">Associate the return policy template with the stores where it will be used.</span></span> <span data-ttu-id="702bf-129">Veldu **Bæta við** á flipann **Smásölurásir** og tengdu tiltækar rásir.</span><span class="sxs-lookup"><span data-stu-id="702bf-129">Select **Add** in the **Retail Channels** tab and associate the available channels.</span></span> 

    - <span data-ttu-id="702bf-130">Í glugganum **Velja fyrirtækjahnúta** velurðu verslanir, svæði og fyrirtæki sem sniðmátið ætti að vera tengt við.</span><span class="sxs-lookup"><span data-stu-id="702bf-130">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>
    - <span data-ttu-id="702bf-131">Aðeins er hægt að tengja eitt sniðmát skilareglu við hverja verslun.</span><span class="sxs-lookup"><span data-stu-id="702bf-131">Only one return policy template can be associated with each store.</span></span>
    - <span data-ttu-id="702bf-132">Notaðu örvahnappana til að velja verslanir, svæði eða fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="702bf-132">Use the arrow buttons to select stores, regions, or organizations.</span></span>
    - <span data-ttu-id="702bf-133">Gildistaka stefnunnar verður sá dagur sem stefnunum er beitt á rásirnar og rásastörfin eru keyrð.</span><span class="sxs-lookup"><span data-stu-id="702bf-133">The effective date on the policy will be the date on which the policies are applied to the channels and the channel jobs are run.</span></span> 

    <span data-ttu-id="702bf-134">![Svarglugginn Veljið fyrirtækjahnúta](media/Return-policy-page3.PNG "Svarglugginn Veljið fyrirtækjahnúta")</span><span class="sxs-lookup"><span data-stu-id="702bf-134">![Choose organization nodes dialog box](media/Return-policy-page3.PNG "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="702bf-135">Á síðunni **Dreifingaráætlun**, keyrðu **1070** vinnslu til að gera skilaregluna á rásinni tiltæka fyrir POS.</span><span class="sxs-lookup"><span data-stu-id="702bf-135">On the **Distribution schedule** page, run the **1070** job to make the channel return policy available to the POS.</span></span>

## <a name="preview-the-channel-return-policy-in-the-pos"></a><span data-ttu-id="702bf-136">Forskoðaðu aftur skilareglu rásarinnar í POS</span><span class="sxs-lookup"><span data-stu-id="702bf-136">Preview the channel return policy in the POS</span></span>

<span data-ttu-id="702bf-137">Fylgdu skrefunum í báðum eftirfarandi dæmum til að skoða leyfðar gerðir tilboða í POS.</span><span class="sxs-lookup"><span data-stu-id="702bf-137">Follow the steps in either of the following examples to view the allowed return tender types in POS.</span></span>

1. <span data-ttu-id="702bf-138">Skráðu þig inn í POS sem gjaldkera eða stjórnandi.</span><span class="sxs-lookup"><span data-stu-id="702bf-138">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="702bf-139">Undir **Vakt og skúffa**, veldu **Sýna færslubók**.</span><span class="sxs-lookup"><span data-stu-id="702bf-139">Under **Shift and Drawer**, select **Show journal**.</span></span>
3. <span data-ttu-id="702bf-140">Veldu færslu sem er hluti af skilunum.</span><span class="sxs-lookup"><span data-stu-id="702bf-140">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="702bf-141">Veldu hlutina sem á að endurgreiða og veldu greiðslumáta.</span><span class="sxs-lookup"><span data-stu-id="702bf-141">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="702bf-142">Ef valinn greiðslumáti er á leyfilegum lista yfir gerðir skilamáta getur gjaldkeri lokið færslunni.</span><span class="sxs-lookup"><span data-stu-id="702bf-142">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="702bf-143">Ef valin greiðslumáti er ekki leyfilegur birtast villuboð.</span><span class="sxs-lookup"><span data-stu-id="702bf-143">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="702bf-144">Veldu **Upphæð til greiðslu** til að birta lista yfir allar leyfilegar tegundir skilamáta.</span><span class="sxs-lookup"><span data-stu-id="702bf-144">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="702bf-145">-eða-</span><span class="sxs-lookup"><span data-stu-id="702bf-145">-or-</span></span>

1. <span data-ttu-id="702bf-146">Skráðu þig inn í POS sem gjaldkera eða stjórnandi.</span><span class="sxs-lookup"><span data-stu-id="702bf-146">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="702bf-147">Veldu **Skilafærsla** og sláðu inn kvittunarauðkenni með strikamerkjaskönnun eða með handvirkri færslu.</span><span class="sxs-lookup"><span data-stu-id="702bf-147">Select **Return Transaction** and enter the receipt ID using a barcode scan or by manual entry.</span></span> 
3. <span data-ttu-id="702bf-148">Veldu færslu sem er hluti af skilunum.</span><span class="sxs-lookup"><span data-stu-id="702bf-148">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="702bf-149">Veldu hlutina sem á að endurgreiða og veldu greiðslumáta.</span><span class="sxs-lookup"><span data-stu-id="702bf-149">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="702bf-150">Ef valinn greiðslumáti er á leyfilegum lista yfir gerðir skilamáta getur gjaldkeri lokið færslunni.</span><span class="sxs-lookup"><span data-stu-id="702bf-150">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="702bf-151">Ef valin greiðslumáti er ekki leyfilegur birtast villuboð.</span><span class="sxs-lookup"><span data-stu-id="702bf-151">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="702bf-152">Veldu **Upphæð til greiðslu** til að birta lista yfir allar leyfilegar tegundir skilamáta.</span><span class="sxs-lookup"><span data-stu-id="702bf-152">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="702bf-153">![Endurgreiðsla ekki leyfð](media/Return-policy-page6.png "Gerð endurgreiðslu ekki leyfð")</span><span class="sxs-lookup"><span data-stu-id="702bf-153">![Refund not allowed](media/Return-policy-page6.png "Refund type not allowed")</span></span>



<span data-ttu-id="702bf-154">![Listi yfir greiðsluhætti](media/Return-policy-page5.PNG "Gerðir endurgreiðslu ekki leyfð")</span><span class="sxs-lookup"><span data-stu-id="702bf-154">![List of payment methods](media/Return-policy-page5.PNG "Refund types allowed")</span></span>
