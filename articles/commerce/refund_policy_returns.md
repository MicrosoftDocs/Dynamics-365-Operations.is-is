---
title: Búa til og uppfæra reglu um skil og endurgreiðslur fyrir rás
description: Þetta efni útskýrir hvernig á að setja upp skil og endurgreiðslu stefnu fyrir rás.
author: ShalabhjainMSFT
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: e23291130d55fdfb5c2e2077b78c221866d72c5d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792076"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a><span data-ttu-id="2856b-103">Búa til og uppfæra reglu um skil og endurgreiðslur fyrir rás</span><span class="sxs-lookup"><span data-stu-id="2856b-103">Create and update a returns and refunds policy for a channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2856b-104">Return stefnu rásarinnar í Dynamics 365 Commerce gerir smásöluaðilum kleift að stilla framfylgni þar sem hægt er að leyfa greiðslutilboð til að vinna úr skilum á sölustað (POS) tæki.</span><span class="sxs-lookup"><span data-stu-id="2856b-104">The channel return policy in Dynamics 365 Commerce enables retailers to set enforcements on which payment tenders can be allowed for processing a return on a point of sale (POS) device.</span></span>  

<span data-ttu-id="2856b-105">Þetta efni lýsir þrepunum til að setja upp skil og endurgreiðslu stefnu fyrir rás.</span><span class="sxs-lookup"><span data-stu-id="2856b-105">This topic describes the steps to set up a returns and refunds policy for a channel.</span></span>

<span data-ttu-id="2856b-106">Umfang stefnunnar er sem stendur takmarkað við að setja greiðslutilboð sem hægt er að leyfa fyrir rás.</span><span class="sxs-lookup"><span data-stu-id="2856b-106">The scope of the policy is currently limited to setting the payment tenders that can be allowed for a channel.</span></span> <span data-ttu-id="2856b-107">Listinn „leyfður“ er byggður á greiðslumáta sem notaðir voru við kaupin.</span><span class="sxs-lookup"><span data-stu-id="2856b-107">The "allowed" list is based on the payment methods used to make the purchase.</span></span> <span data-ttu-id="2856b-108">Dæmi:</span><span class="sxs-lookup"><span data-stu-id="2856b-108">For example:</span></span>

- <span data-ttu-id="2856b-109">Ef kaup voru gerð með gjafakorti er verslunin stefna að afgreiða endurgreiðslur aðeins á nýju gjafakorti eða veita lánsfé.</span><span class="sxs-lookup"><span data-stu-id="2856b-109">If a purchase was made using a gift card, the store policy is to process refunds only to a new gift card or to give store credit.</span></span> 
- <span data-ttu-id="2856b-110">Ef sala fer fram með reiðufé eru möguleikarnir sem eru leyfðir til endurgreiðslu reiðufé, gjafakort og viðskiptareikningur en ekki kreditkort.</span><span class="sxs-lookup"><span data-stu-id="2856b-110">If a sale is made using cash, the options allowed for refund are cash, gift card, and customer account, but not credit card.</span></span> 


## <a name="enable-return-policy"></a><span data-ttu-id="2856b-111">Virkja skilareglu</span><span class="sxs-lookup"><span data-stu-id="2856b-111">Enable return policy</span></span>

<span data-ttu-id="2856b-112">Gerðu eftirfarandi til að virkja skilareglu rásarvirkninnar:</span><span class="sxs-lookup"><span data-stu-id="2856b-112">To enable the channel return policy functionality, do the following:</span></span>

1. <span data-ttu-id="2856b-113">Farðu í vinnusvæðið **Eiginleikastjórnun** í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2856b-113">Go to the **Feature Management** workspace in Dynamics 365 Commerce.</span></span>
2. <span data-ttu-id="2856b-114">Leitaðu að eiginleikanum **Virkja skilareglur rása** á listanum yfir heiti eiginleika.</span><span class="sxs-lookup"><span data-stu-id="2856b-114">Search for the **Enable channel return policies** feature in the list of feature names.</span></span>
3. <span data-ttu-id="2856b-115">Veldu **Virkja núna**.</span><span class="sxs-lookup"><span data-stu-id="2856b-115">Select **Enable now**.</span></span> 

## <a name="configure-return-policy"></a><span data-ttu-id="2856b-116">Stilla skilareglu</span><span class="sxs-lookup"><span data-stu-id="2856b-116">Configure return policy</span></span>

<span data-ttu-id="2856b-117">Fylgdu þessum skrefum til að stilla aftur stefnu fyrir smásöluverslun eða netverslun.</span><span class="sxs-lookup"><span data-stu-id="2856b-117">Follow these steps to configure a return policy for a retail store or online retail channel.</span></span>

1. <span data-ttu-id="2856b-118">Farðu í **Verslun og verslun** \> **Uppsetning rásar** \> **Skilar** \> **Skilastefna rásarinnar**.</span><span class="sxs-lookup"><span data-stu-id="2856b-118">Go to **Retail and Commerce** \> **Channel Setup** \> **Returns** \> **Channel return policy**.</span></span>

2. <span data-ttu-id="2856b-119">Veldu **Nýtt** til að búa til nýtt sniðmát skilareglu.</span><span class="sxs-lookup"><span data-stu-id="2856b-119">Select **New** to create a new return policy template.</span></span> <span data-ttu-id="2856b-120">Veldu sniðmátið í vinstri glugganum til að nota sniðmát sem fyrir er.</span><span class="sxs-lookup"><span data-stu-id="2856b-120">To use an existing template, select the template in the left pane.</span></span> <span data-ttu-id="2856b-121">Fyrir ný sniðmát skaltu bæta við nafni og lýsingu sem mun hjálpa þér að bera kennsl á stefnuna þegar henni er beitt á rásina.</span><span class="sxs-lookup"><span data-stu-id="2856b-121">For new templates, add a name and description that will help you identify the policy when it is being applied to the channel.</span></span>

   <span data-ttu-id="2856b-122">![Bættu við nýrri skilareglu](media/Return-policy-page1.png "Bæta við nýrri skilareglu")</span><span class="sxs-lookup"><span data-stu-id="2856b-122">![Add new return policy](media/Return-policy-page1.png "Add new return rolicy")</span></span>
     
   
3. <span data-ttu-id="2856b-123">Í kaflanum **Leyfðar endurgreiðsluaðferðir**, skilgreina **Leyft** greiðslutilboðum skila sem eru sértæk fyrir hverja greiðslumáta.</span><span class="sxs-lookup"><span data-stu-id="2856b-123">In the **Allowed refund payment methods** section, define **Allowed** return payment tenders that are specific to each payment method.</span></span>
   <span data-ttu-id="2856b-124">![Bæta við greiðslumátum](media/Return-policy-page2.PNG "Stilltu leyfðar greiðslumáta fyrir hverja greiðslugerð")</span><span class="sxs-lookup"><span data-stu-id="2856b-124">![Add payment methods](media/Return-policy-page2.PNG "Set allowed payment methods per payment type")</span></span>
   
    > [!IMPORTANT]
    > - <span data-ttu-id="2856b-125">Greiðslumátarnir eru fengnir af þeim greiðslumáta sem settur er fyrir stofnunina.</span><span class="sxs-lookup"><span data-stu-id="2856b-125">The payment methods are derived from the payment methods set for the organization.</span></span>
    > - <span data-ttu-id="2856b-126">Með því að bæta við leyfðri útboðsgerð fyrir hverja skráða greiðslumáta verður tryggt að hægt sé að skila í leyfilega gerð útboðs.</span><span class="sxs-lookup"><span data-stu-id="2856b-126">Adding an allowed return tender type for each listed payment method will ensure that returns can be made to the allowed return tender type.</span></span>
    
4. <span data-ttu-id="2856b-127">Tengdu sniðmát skilareglu við verslanirnar þar sem það verður notað.</span><span class="sxs-lookup"><span data-stu-id="2856b-127">Associate the return policy template with the stores where it will be used.</span></span> <span data-ttu-id="2856b-128">Veldu **Bæta við** á flipann **Smásölurásir** og tengdu tiltækar rásir.</span><span class="sxs-lookup"><span data-stu-id="2856b-128">Select **Add** in the **Retail Channels** tab and associate the available channels.</span></span> 

    - <span data-ttu-id="2856b-129">Í glugganum **Velja fyrirtækjahnúta** velurðu verslanir, svæði og fyrirtæki sem sniðmátið ætti að vera tengt við.</span><span class="sxs-lookup"><span data-stu-id="2856b-129">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>
    - <span data-ttu-id="2856b-130">Aðeins er hægt að tengja eitt sniðmát skilareglu við hverja verslun.</span><span class="sxs-lookup"><span data-stu-id="2856b-130">Only one return policy template can be associated with each store.</span></span>
    - <span data-ttu-id="2856b-131">Notaðu örvahnappana til að velja verslanir, svæði eða fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="2856b-131">Use the arrow buttons to select stores, regions, or organizations.</span></span>
    - <span data-ttu-id="2856b-132">Gildistaka stefnunnar verður sá dagur sem stefnunum er beitt á rásirnar og rásastörfin eru keyrð.</span><span class="sxs-lookup"><span data-stu-id="2856b-132">The effective date on the policy will be the date on which the policies are applied to the channels and the channel jobs are run.</span></span> 

    <span data-ttu-id="2856b-133">![Svarglugginn Veljið fyrirtækjahnúta](media/Return-policy-page3.PNG "Svarglugginn Veljið fyrirtækjahnúta")</span><span class="sxs-lookup"><span data-stu-id="2856b-133">![Choose organization nodes dialog box](media/Return-policy-page3.PNG "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="2856b-134">Á síðunni **Dreifingaráætlun**, keyrðu **1070** vinnslu til að gera skilaregluna á rásinni tiltæka fyrir POS.</span><span class="sxs-lookup"><span data-stu-id="2856b-134">On the **Distribution schedule** page, run the **1070** job to make the channel return policy available to the POS.</span></span>

## <a name="preview-the-channel-return-policy-in-the-pos"></a><span data-ttu-id="2856b-135">Forskoðaðu aftur skilareglu rásarinnar í POS</span><span class="sxs-lookup"><span data-stu-id="2856b-135">Preview the channel return policy in the POS</span></span>

<span data-ttu-id="2856b-136">Fylgdu skrefunum í báðum eftirfarandi dæmum til að skoða leyfðar gerðir tilboða í POS.</span><span class="sxs-lookup"><span data-stu-id="2856b-136">Follow the steps in either of the following examples to view the allowed return tender types in POS.</span></span>

1. <span data-ttu-id="2856b-137">Skráðu þig inn í POS sem gjaldkera eða stjórnandi.</span><span class="sxs-lookup"><span data-stu-id="2856b-137">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="2856b-138">Undir **Vakt og skúffa**, veldu **Sýna færslubók**.</span><span class="sxs-lookup"><span data-stu-id="2856b-138">Under **Shift and Drawer**, select **Show journal**.</span></span>
3. <span data-ttu-id="2856b-139">Veldu færslu sem er hluti af skilunum.</span><span class="sxs-lookup"><span data-stu-id="2856b-139">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="2856b-140">Veldu hlutina sem á að endurgreiða og veldu greiðslumáta.</span><span class="sxs-lookup"><span data-stu-id="2856b-140">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="2856b-141">Ef valinn greiðslumáti er á leyfilegum lista yfir gerðir skilamáta getur gjaldkeri lokið færslunni.</span><span class="sxs-lookup"><span data-stu-id="2856b-141">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="2856b-142">Ef valin greiðslumáti er ekki leyfilegur birtast villuboð.</span><span class="sxs-lookup"><span data-stu-id="2856b-142">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="2856b-143">Veldu **Upphæð til greiðslu** til að birta lista yfir allar leyfilegar tegundir skilamáta.</span><span class="sxs-lookup"><span data-stu-id="2856b-143">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="2856b-144">-eða-</span><span class="sxs-lookup"><span data-stu-id="2856b-144">-or-</span></span>

1. <span data-ttu-id="2856b-145">Skráðu þig inn í POS sem gjaldkera eða stjórnandi.</span><span class="sxs-lookup"><span data-stu-id="2856b-145">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="2856b-146">Veldu **Skilafærsla** og sláðu inn kvittunarauðkenni með strikamerkjaskönnun eða með handvirkri færslu.</span><span class="sxs-lookup"><span data-stu-id="2856b-146">Select **Return Transaction** and enter the receipt ID using a barcode scan or by manual entry.</span></span> 
3. <span data-ttu-id="2856b-147">Veldu færslu sem er hluti af skilunum.</span><span class="sxs-lookup"><span data-stu-id="2856b-147">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="2856b-148">Veldu hlutina sem á að endurgreiða og veldu greiðslumáta.</span><span class="sxs-lookup"><span data-stu-id="2856b-148">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="2856b-149">Ef valinn greiðslumáti er á leyfilegum lista yfir gerðir skilamáta getur gjaldkeri lokið færslunni.</span><span class="sxs-lookup"><span data-stu-id="2856b-149">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="2856b-150">Ef valin greiðslumáti er ekki leyfilegur birtast villuboð.</span><span class="sxs-lookup"><span data-stu-id="2856b-150">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="2856b-151">Veldu **Upphæð til greiðslu** til að birta lista yfir allar leyfilegar tegundir skilamáta.</span><span class="sxs-lookup"><span data-stu-id="2856b-151">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="2856b-152">![Endurgreiðsla ekki leyfð](media/Return-policy-page6.png "Gerð endurgreiðslu ekki leyfð")</span><span class="sxs-lookup"><span data-stu-id="2856b-152">![Refund not allowed](media/Return-policy-page6.png "Refund type not allowed")</span></span>



<span data-ttu-id="2856b-153">![Listi yfir greiðsluhætti](media/Return-policy-page5.PNG "Gerðir endurgreiðslu ekki leyfð")</span><span class="sxs-lookup"><span data-stu-id="2856b-153">![List of payment methods](media/Return-policy-page5.PNG "Refund types allowed")</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
