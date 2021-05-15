---
title: Stuðningur skattaeiginleika fyrir flutningspantanir
description: Þetta efnisatriði útskýrir nýjan stuðning skattaeiginleika fyrir flutningspantanir með því að nota skattaútreikningsþjónustuna.
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d1b99046b0e439c9dadbb240050e270a7b2a6914
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920956"
---
# <a name="tax-feature-support-for-transfer-orders"></a><span data-ttu-id="1144c-103">Stuðningur skattaeiginleika fyrir flutningspantanir</span><span class="sxs-lookup"><span data-stu-id="1144c-103">Tax feature support for transfer orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1144c-104">Þetta efni inniheldur upplýsingar um samþættingu skattaútreiknings og bókunar í flutningspöntunum.</span><span class="sxs-lookup"><span data-stu-id="1144c-104">This topic provides information about tax calculation and posting integration in transfer orders.</span></span> <span data-ttu-id="1144c-105">Þessi virkni gerir kleift að setja upp skattaútreikning og bókun í flutningspöntunum fyrir birgðaflutninga.</span><span class="sxs-lookup"><span data-stu-id="1144c-105">This functionality lets you set up tax calculation and posting in transfer orders for stock transfers.</span></span> <span data-ttu-id="1144c-106">Samkvæmt VSK-reglugerðum Evrópusambandsins er litið á birgðaflutninga sem framboð og kaup innan sambandsins.</span><span class="sxs-lookup"><span data-stu-id="1144c-106">Under European Union (EU) value-added tax (VAT) regulations, stock transfers are considered intra-community supply and intra-community acquisitions.</span></span>

<span data-ttu-id="1144c-107">Til að grunnstilla og nota þessa virkni þarf að ljúka þremur meginskrefum:</span><span class="sxs-lookup"><span data-stu-id="1144c-107">To configure and use this functionality, you must complete three main steps:</span></span>

1. <span data-ttu-id="1144c-108">**RCS-uppsetning:** í Regulatory Configuration Service skal setja upp skattaeiginleika, skattkóða og gildissvið skattkóða fyrir ákvörðun skattkóða í flutningspöntunum.</span><span class="sxs-lookup"><span data-stu-id="1144c-108">**RCS setup:** In Regulatory Configuration Service, set up the tax feature, tax codes, and tax codes applicability for tax code determination in transfer orders.</span></span>
2. <span data-ttu-id="1144c-109">**Fjárhagsuppsetning:** Í Microsoft Dynamics 365 Finance skal kveikja á eiginleikanum **Skattar í flutningspöntun**, setja upp færibreytur skattþjónustu fyrir birgðir og setja upp grunnfæribreytur skatts.</span><span class="sxs-lookup"><span data-stu-id="1144c-109">**Finance setup:** In Microsoft Dynamics 365 Finance, turn on the **Tax in transfer order** feature, set up the tax service parameters for inventory, and set up core tax parameters.</span></span>
3. <span data-ttu-id="1144c-110">**Uppsetning birgða:** Setjið upp skilgreiningu birgða fyrir færslur flutningspöntunar.</span><span class="sxs-lookup"><span data-stu-id="1144c-110">**Inventory setup:** Set up the inventory configuration for transfer order transactions.</span></span>

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a><span data-ttu-id="1144c-111">Setja upp RCS fyrir skattfærslur og færslur flutningspöntunar</span><span class="sxs-lookup"><span data-stu-id="1144c-111">Set up RCS for tax and transfer order transactions</span></span>

<span data-ttu-id="1144c-112">Fylgið þessum skrefum til að setja upp skattinn sem tengist flutningspöntun.</span><span class="sxs-lookup"><span data-stu-id="1144c-112">Follow these steps to set up the tax that is involved in a transfer order.</span></span> <span data-ttu-id="1144c-113">Í dæminu sem er sýnt hér er flutningspöntunin frá Hollandi og Belgíu.</span><span class="sxs-lookup"><span data-stu-id="1144c-113">In the example that is shown here, the transfer order is from the Netherlands to Belgium.</span></span>

1. <span data-ttu-id="1144c-114">Á síðunni **Skattaeiginleikar**, í flipanum **Útgáfur**, skal velja drög að eiginleikaútgáfu og síðan velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="1144c-114">On the **Tax features** page, on the **Versions** tab, select the draft feature version, and then select **Edit**.</span></span>

    ![Breyta valið](../media/image1.png)

2. <span data-ttu-id="1144c-116">Á síðunni **Uppsetning skattaeiginleika**, í flipanum **Skattkóðar**, skal velja **Bæta við** til að stofna nýja skattkóða.</span><span class="sxs-lookup"><span data-stu-id="1144c-116">On the **Tax features setup** page, on the **Tax codes** tab, select **Add** to create new tax codes.</span></span> <span data-ttu-id="1144c-117">Fyrir þetta dæmi eru þrír skattkóðar stofnaður: **NL-Exempt**, **BE-RC-21** og **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="1144c-117">For this example, three tax codes are created: **NL-Exempt**, **BE-RC-21**, and **BE-RC+21**.</span></span>

    - <span data-ttu-id="1144c-118">Þegar flutningspöntun er send úr vöruhúsi í Hollandi er notaður skattkóði fyrir undanskilinn virðisaukaskatt Hollands (**NL-Exempt**).</span><span class="sxs-lookup"><span data-stu-id="1144c-118">When a transfer order is shipped from a warehouse in the Netherlands, the Netherlands VAT exempted tax code (**NL-Exempt**) is applied.</span></span>
      
        <span data-ttu-id="1144c-119">Búið til skattkóðann **NL-Exempt**.</span><span class="sxs-lookup"><span data-stu-id="1144c-119">Create the tax code **NL-Exempt**.</span></span>
        1. <span data-ttu-id="1144c-120">Veljið **Bæta við**, sláið inn **NL-Exempt** í reitinn **Skattkóði**.</span><span class="sxs-lookup"><span data-stu-id="1144c-120">Select **Add**, enter **NL-Exempt** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="1144c-121">Veljið **Eftir nettóupphæð** í reitnum **Skatthlutur**.</span><span class="sxs-lookup"><span data-stu-id="1144c-121">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="1144c-122">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="1144c-122">Select **Save**.</span></span>
        4. <span data-ttu-id="1144c-123">Veljið **Bæta við** í töflunni **Taxti**.</span><span class="sxs-lookup"><span data-stu-id="1144c-123">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="1144c-124">Skiptið **Er undanskilið** í **Já** í hlutanum **Almennt**.</span><span class="sxs-lookup"><span data-stu-id="1144c-124">Swtich **Is Exempt** to **Yes** in the **General** section.</span></span>

        ![Skattkóði NL-Exempt](../media/image2.png)

    - <span data-ttu-id="1144c-126">Þegar flutningspöntun er móttekin í belgísku vöruhúsi er leið bakfærðs gjalds notað með því að nota skattkóðana **BE-RC-21** og **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="1144c-126">When a transfer order is received at a Belgium warehouse, the reverse charge mechanism is applied by using the **BE-RC-21** and **BE-RC+21** tax codes.</span></span>
        
        <span data-ttu-id="1144c-127">Búið til skattkóðann **BE-RC-21**.</span><span class="sxs-lookup"><span data-stu-id="1144c-127">Create the tax code **BE-RC-21**.</span></span>      
        1. <span data-ttu-id="1144c-128">Veljið **Bæta við**, sláið inn **BE-RC-21** í reitinn **Skattkóði**.</span><span class="sxs-lookup"><span data-stu-id="1144c-128">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="1144c-129">Veljið **Eftir nettóupphæð** í reitnum **Skatthlutur**.</span><span class="sxs-lookup"><span data-stu-id="1144c-129">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="1144c-130">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="1144c-130">Select **Save**.</span></span>
        4. <span data-ttu-id="1144c-131">Veljið **Bæta við** í töflunni **Taxti**.</span><span class="sxs-lookup"><span data-stu-id="1144c-131">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="1144c-132">Sláið inn **-21** í reitinn **Skatthlutfall**.</span><span class="sxs-lookup"><span data-stu-id="1144c-132">Enter **-21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="1144c-133">Skiptið **Er bakfært gjald** í **Já** í hlutanum **Almennt**.</span><span class="sxs-lookup"><span data-stu-id="1144c-133">Swtich **Is Reverse Charge** to **Yes** in the **General** section.</span></span>
        7. <span data-ttu-id="1144c-134">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="1144c-134">Select **Save**.</span></span>

        ![BE-RC-21 skattkóði fyrir bakfærð gjöld](../media/image3.png)
        
        <span data-ttu-id="1144c-136">Búið til skattkóðann **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="1144c-136">Create the tax code **BE-RC+21**.</span></span>
        1. <span data-ttu-id="1144c-137">Veljið **Bæta við**, sláið inn **BE-RC-21** í reitinn **Skattkóði**.</span><span class="sxs-lookup"><span data-stu-id="1144c-137">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="1144c-138">Veljið **Eftir nettóupphæð** í reitnum **Skatthlutur**.</span><span class="sxs-lookup"><span data-stu-id="1144c-138">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="1144c-139">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="1144c-139">Select **Save**.</span></span>
        4. <span data-ttu-id="1144c-140">Veljið **Bæta við** í töflunni **Taxti**.</span><span class="sxs-lookup"><span data-stu-id="1144c-140">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="1144c-141">Sláið inn **21** í reitinn **Skatthlutfall**.</span><span class="sxs-lookup"><span data-stu-id="1144c-141">Enter **21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="1144c-142">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="1144c-142">Select **Save**.</span></span>

        ![BE-RC+21 skattkóði fyrir bakfærð gjöld](../media/image4.png)

3. <span data-ttu-id="1144c-144">Skilgreinið gildissvið skattkóðanna.</span><span class="sxs-lookup"><span data-stu-id="1144c-144">Define the applicability of the tax codes.</span></span>

    1. <span data-ttu-id="1144c-145">Veljið **Stjórna dálkum** og veljið síðan dálka sem á að nota til að búa til töflu gildissviðs.</span><span class="sxs-lookup"><span data-stu-id="1144c-145">Select **Manage columns**, and then select columns that should be used to build the applicability table.</span></span>

        > [!NOTE]
        > <span data-ttu-id="1144c-146">Gangið úr skugga um að bæta dálkunum **Viðskiptaferli** og **Skattstefnur** við töfluna.</span><span class="sxs-lookup"><span data-stu-id="1144c-146">Be sure to add the **Business process** and **Tax directions** columns to the table.</span></span> <span data-ttu-id="1144c-147">Báðir dálkarnir eru nauðsynlegir fyrir virknina fyrir skatt í flutningspöntunum.</span><span class="sxs-lookup"><span data-stu-id="1144c-147">Both columns are essential to the functionality for tax in transfer orders.</span></span>

    2. <span data-ttu-id="1144c-148">Bætið við gildissviðsreglum.</span><span class="sxs-lookup"><span data-stu-id="1144c-148">Add applicability rules.</span></span> <span data-ttu-id="1144c-149">Ekki skilja reitina **Skattkóðar**, **Skattflokkur** og **Vöruskattflokkur** eftir auða.</span><span class="sxs-lookup"><span data-stu-id="1144c-149">Don't leave the **Tax codes**, **Tax group**, and **Item tax group** fields blank.</span></span>
        
        <span data-ttu-id="1144c-150">Bæta við nýrri reglu fyrir sendingu flutningspöntunar.</span><span class="sxs-lookup"><span data-stu-id="1144c-150">Add a new rule for transfer order shipment.</span></span>
        1. <span data-ttu-id="1144c-151">Veljið **Bæta við** í töflunni **Gildissviðsreglur**.</span><span class="sxs-lookup"><span data-stu-id="1144c-151">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="1144c-152">Í reitnum **Viðskiptaferli** skal velja **Birgðir** til að reglan gildi um flutningspöntun.</span><span class="sxs-lookup"><span data-stu-id="1144c-152">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="1144c-153">Í reitinn **Senda frá landi/svæði** skal færa inn **NLD**.</span><span class="sxs-lookup"><span data-stu-id="1144c-153">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="1144c-154">Í reitinn **Senda til lands/svæðis** skal færa inn **BEL**.</span><span class="sxs-lookup"><span data-stu-id="1144c-154">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="1144c-155">Í reitnum **Skattstefnan** skal velja **Úttak** til að reglan gildi um sendingu flutningspöntunar.</span><span class="sxs-lookup"><span data-stu-id="1144c-155">In the **Tax direction** field, select **Output** to make the rule applicable to transfer order shipment.</span></span>
        6. <span data-ttu-id="1144c-156">Í reitnum **Skattkóðar** skal velja **NL-Exempt**.</span><span class="sxs-lookup"><span data-stu-id="1144c-156">In the **Tax codes** field, select **NL-Exempt**.</span></span>
        7. <span data-ttu-id="1144c-157">Í reitinn **Skattflokkur** og **VSK-flokkur vöru** skal færa inn viðeigandi VSK-flokk og VSK-flokk vöru sem eru skilgreindir í kerfi Finance.</span><span class="sxs-lookup"><span data-stu-id="1144c-157">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>
        
        <span data-ttu-id="1144c-158">Bætið við annarri reglu fyrir móttöku flutningspöntunar.</span><span class="sxs-lookup"><span data-stu-id="1144c-158">Add another rule for transfer order receipt.</span></span>
        1. <span data-ttu-id="1144c-159">Veljið **Bæta við** í töflunni **Gildissviðsreglur**.</span><span class="sxs-lookup"><span data-stu-id="1144c-159">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="1144c-160">Í reitnum **Viðskiptaferli** skal velja **Birgðir** til að reglan gildi um flutningspöntun.</span><span class="sxs-lookup"><span data-stu-id="1144c-160">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="1144c-161">Í reitinn **Senda frá landi/svæði** skal færa inn **NLD**.</span><span class="sxs-lookup"><span data-stu-id="1144c-161">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="1144c-162">Í reitinn **Senda til lands/svæðis** skal færa inn **BEL**.</span><span class="sxs-lookup"><span data-stu-id="1144c-162">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="1144c-163">Í reitnum **Skattstefnan** skal velja **Inntak** til að reglan gildi um móttöku flutningspöntunar.</span><span class="sxs-lookup"><span data-stu-id="1144c-163">In the **Tax direction** field, select **Input** to make the rule applicable to transfer order receipt.</span></span>
        6. <span data-ttu-id="1144c-164">Í reitnum **Skattkóðar** skal velja **BE-RC+21** og **BE-RC-21**.</span><span class="sxs-lookup"><span data-stu-id="1144c-164">In the **Tax codes** field, select **BE-RC+21** and **BE-RC-21**.</span></span>
        7. <span data-ttu-id="1144c-165">Í reitinn **Skattflokkur** og **VSK-flokkur vöru** skal færa inn viðeigandi VSK-flokk og VSK-flokk vöru sem eru skilgreindir í kerfi Finance.</span><span class="sxs-lookup"><span data-stu-id="1144c-165">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>

        ![Gildissviðsreglur](../media/image5.png)

4. <span data-ttu-id="1144c-167">Ljúka og birta nýja útgáfu nýs skattaeiginleika.</span><span class="sxs-lookup"><span data-stu-id="1144c-167">Complete and publish the new tax feature version.</span></span>

    <span data-ttu-id="1144c-168">[![Stöðu nýju útgáfunnar breytt](../media/image6.png)](../media/image6.png)</span><span class="sxs-lookup"><span data-stu-id="1144c-168">[![Changing the status of the new version](../media/image6.png)](../media/image6.png)</span></span>

## <a name="set-up-finance-for-transfer-order-transactions"></a><span data-ttu-id="1144c-169">Setja upp Finance fyrir færslur flutningspöntunar</span><span class="sxs-lookup"><span data-stu-id="1144c-169">Set up Finance for transfer order transactions</span></span>

<span data-ttu-id="1144c-170">Fylgið þessum skrefum til að virkja og setja upp skatta fyrir flutningspantanir.</span><span class="sxs-lookup"><span data-stu-id="1144c-170">Follow these steps to enable and set up taxes for transfer orders.</span></span>

1. <span data-ttu-id="1144c-171">Í Finance skal opna **Vinnusvæði** \> **Eiginleikastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="1144c-171">In Finance, go to **Workspaces** \> **Feature management**.</span></span>
2. <span data-ttu-id="1144c-172">Í listanum skal finna og velja eiginleikann **Skattar í flutningspöntun** og síðan velja **Virkja núna** til að kveikja á honum.</span><span class="sxs-lookup"><span data-stu-id="1144c-172">In the list, find and select the **Tax in transfer order** feature, and then select **Enable now** to turn it on.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="1144c-173">Eiginleikinn **Skattur í flutningspöntun** er algjörlega háður skattþjónustunni.</span><span class="sxs-lookup"><span data-stu-id="1144c-173">The **Tax in transfer order** feature is fully dependent on the tax service.</span></span> <span data-ttu-id="1144c-174">Þess vegna er aðeins hægt að kveikja á honum þegar búið er að setja upp skattþjónustuna.</span><span class="sxs-lookup"><span data-stu-id="1144c-174">Therefore, it can be turned on only after you've installed the tax service.</span></span>

    ![Skattur í flutningspöntunareiginleika](../media/image7.png)

3. <span data-ttu-id="1144c-176">Virkið skattþjónustuna og veljið viðskiptaferlið **Birgðir**.</span><span class="sxs-lookup"><span data-stu-id="1144c-176">Enable the tax service, and select the **Inventory** business process.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="1144c-177">Ljúka þarf þessu skrefi fyrir hvern lögaðila í Finance þar sem skattþjónustan og virknin fyrir skatt í flutningspöntunum eiga að vera tiltækar.</span><span class="sxs-lookup"><span data-stu-id="1144c-177">You must complete this step for each legal entity in Finance where you want the tax service and the functionality for tax in transfer orders to be available.</span></span>

    1. <span data-ttu-id="1144c-178">Farið í **Skattur** \> **Uppsetning** \> **Skattaskilgreining** \> **Uppsetning skattþjónustu**.</span><span class="sxs-lookup"><span data-stu-id="1144c-178">Go to **Tax** \> **Setup** \> **Tax configuration** \> **Tax service setup**.</span></span>
    2. <span data-ttu-id="1144c-179">Í reitnum **Viðskiptaferli** skal velja **Birgðir**.</span><span class="sxs-lookup"><span data-stu-id="1144c-179">In the **Business process** field, select **Inventory**.</span></span>

    ![Reitur viðskiptaferlis stilltur](../media/image8.png)

4. <span data-ttu-id="1144c-181">Gangið úr skugga um að leið bakfærðs gjalds sé uppsett.</span><span class="sxs-lookup"><span data-stu-id="1144c-181">Verify that the reverse charge mechanism is set up.</span></span> <span data-ttu-id="1144c-182">Farið í **Fjárhagur** \> **Uppsetning** \> **Færibreytur** og síðan, í flipanum **Bakfært gjald**, skal staðfesta að valkosturinn **Virkja bakfært gjald** sé stilltur á **Já**.</span><span class="sxs-lookup"><span data-stu-id="1144c-182">Go to **General ledger** \> **Setup** \> **Parameters**, and then, on the **Reverse charge** tab, verify that the **Enable reverse charge** option is set to **Yes**.</span></span>

    ![Virkja valkost bakfærðra gjalda](../media/image9.png)

5. <span data-ttu-id="1144c-184">Gangið úr skugga um að tengdir skattkóðar, skattflokkar, skattflokkar vöru og skráningarnúmer virðisaukaskatts hafi verið sett upp í Finance samkvæmt leiðsögn skattþjónustunnar.</span><span class="sxs-lookup"><span data-stu-id="1144c-184">Verify that the related tax codes, tax groups, item tax groups, and VAT registration numbers have been set up in Finance according to the tax service guidance.</span></span>
6. <span data-ttu-id="1144c-185">Setja upp bráðabirgðareikning flutnings.</span><span class="sxs-lookup"><span data-stu-id="1144c-185">Set up an interim transit account.</span></span> <span data-ttu-id="1144c-186">Þetta þrep er aðeins áskilið þegar skatturinn sem er notaður í flutningspöntun á ekki við um leið skattundanþágu eða bakfærðs gjalds.</span><span class="sxs-lookup"><span data-stu-id="1144c-186">This step is required only when the tax that is applied to a transfer order isn't applicable to a tax exempted or reverse charge mechanism.</span></span>

    1. <span data-ttu-id="1144c-187">Opnið **Skattur** \> **Uppsetning** \> **Söluskattur** \> **Fjárhagsbókunarflokkar**.</span><span class="sxs-lookup"><span data-stu-id="1144c-187">Go to **Tax** \> **Setup** \> **Sales tax** \> **Ledger posting groups**.</span></span>
    2. <span data-ttu-id="1144c-188">Í reitnum **Bráðabirgðaflutningur** skal velja fjárhagslykil.</span><span class="sxs-lookup"><span data-stu-id="1144c-188">In the **Interim transit** field, select a ledger account.</span></span>

    ![Bráðabirgðareikningur flutnings valinn](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a><span data-ttu-id="1144c-190">Setja upp grunnbirgðir fyrir færslur flutningspöntunar</span><span class="sxs-lookup"><span data-stu-id="1144c-190">Set up basic inventory for transfer order transactions</span></span>

<span data-ttu-id="1144c-191">Fylgið þessum skrefum til að setja upp grunnbirgðir til að virkja færslur flutningspöntunar.</span><span class="sxs-lookup"><span data-stu-id="1144c-191">Follow these steps to set up basic inventory to enable transfer order transactions.</span></span>

1. <span data-ttu-id="1144c-192">Búið til senda-til og senda-frá svæði fyrir vöruhúsin í mismunandi löndum eða svæðum og bætið við aðalaðsetrinu fyrir hvert svæði.</span><span class="sxs-lookup"><span data-stu-id="1144c-192">Create ship-from and ship-to sites for your warehouses in different countries or regions, and add the primary address for each site.</span></span>

    1. <span data-ttu-id="1144c-193">Farðu í **Vöruhúsakerfi** \> **Setja upp** \> **Vöruhús** \> **Svæði**.</span><span class="sxs-lookup"><span data-stu-id="1144c-193">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Sites**.</span></span>
    2. <span data-ttu-id="1144c-194">Veljið **Nýtt** til að búa til nýtt svæði sem verður úthlutað á vöruhúsið síðar.</span><span class="sxs-lookup"><span data-stu-id="1144c-194">Select **New** to create the site that you will assign to a warehouse later.</span></span>
    3. <span data-ttu-id="1144c-195">Endurtakið skref 2 fyrir öll önnur svæði sem þarf að búa til.</span><span class="sxs-lookup"><span data-stu-id="1144c-195">Repeat step 2 for all the other sites that you must create.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1144c-196">Eitt svæðanna sem var búið til ætti að kalla **Flutningur**.</span><span class="sxs-lookup"><span data-stu-id="1144c-196">One of the sites that you create should be named **Transit**.</span></span> <span data-ttu-id="1144c-197">Í síðari skrefum þessa ferlis verður þessu svæði úthlutað á flutningsvöruhúsið þannig að hægt sé að bóka skatttengd fylgiskjöl birgða í „senda“ og „móttaka“ færslum fyrir flutningspantanir.</span><span class="sxs-lookup"><span data-stu-id="1144c-197">In later steps of this procedure, you will assign this site to the transit warehouse, so that tax-related inventory vouchers can be posted in "ship" and "receive" transactions for transfer orders.</span></span> <span data-ttu-id="1144c-198">Aðsetur flutningasvæðis tengist ekki skattaútreikningum.</span><span class="sxs-lookup"><span data-stu-id="1144c-198">The address of the transit site is irrelevant to tax calculation.</span></span> <span data-ttu-id="1144c-199">Þess vegna er hægt að skilja hann eftir auðan.</span><span class="sxs-lookup"><span data-stu-id="1144c-199">Therefore, you can leave it blank.</span></span>

    ![Uppsetning svæða](../media/image11.png)

2. <span data-ttu-id="1144c-201">Búið til vöruhús fyrir senda-til, flutning og senda-til.</span><span class="sxs-lookup"><span data-stu-id="1144c-201">Create ship-from, transit, and ship-to warehouses.</span></span> <span data-ttu-id="1144c-202">Allar upplýsingar um aðsetur sem er viðhaldið í vöruhúsi munu hnekkja aðsetri svæðis í skattaútreikningum.</span><span class="sxs-lookup"><span data-stu-id="1144c-202">Any address information that is maintained in a warehouse will override the site address during tax calculation.</span></span>

    1. <span data-ttu-id="1144c-203">Farðu í **Vöruhúsakerfi** \> **Uppsetning** \> **Vöruhús** \> **Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="1144c-203">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Warehouses**.</span></span>
    2. <span data-ttu-id="1144c-204">Veljið **Nýtt** til að stofna vöruhús og úthluta því á samsvarandi svæði.</span><span class="sxs-lookup"><span data-stu-id="1144c-204">Select **New** to create a warehouse, and assign it to the corresponding site.</span></span>
    3. <span data-ttu-id="1144c-205">Endurtakið skref 2 til að búa til vöruhús fyrir hvert svæði eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="1144c-205">Repeat step 2 to create a warehouse for each site as required.</span></span>

    ![Setja upp vöruhús](../media/image12.png)

    > [!NOTE]
    > <span data-ttu-id="1144c-207">Fyrir senda-til vöruhús þarf að velja flutningsvöruhús í reitnum **Flutningsvöruhús** fyrir færslur flutningspöntunar.</span><span class="sxs-lookup"><span data-stu-id="1144c-207">For a ship-from warehouse, a transit warehouse must be selected in the **Transit warehouse** field for transfer order transactions.</span></span>
    >
    > ![Val á flutningsvöruhúsi](../media/image13.png)

3. <span data-ttu-id="1144c-209">Gangið úr skugga um að skilgreining birgðabókunar sé sett upp fyrir færslur flutningspöntunar.</span><span class="sxs-lookup"><span data-stu-id="1144c-209">Verify that the inventory posting configuration is set up for transfer order transactions.</span></span>

    1. <span data-ttu-id="1144c-210">Opnið **Birgðastjórnun** \> **Uppsetning** \> **Bókun** \> **Bókun**.</span><span class="sxs-lookup"><span data-stu-id="1144c-210">Go to **Inventory management** \> **Setup** \> **Posting** \> **Posting**.</span></span>
    2. <span data-ttu-id="1144c-211">Í flipanum **Birgðir** skal ganga úr skugga um að fjárhagslykill sé settur upp fyrri bæði bókanir á **Úthreyfingu birgða** og **Innhreyfingu birgða**.</span><span class="sxs-lookup"><span data-stu-id="1144c-211">On the **Inventory** tab, verify that a ledger account is set up for both **Inventory issue** and **Inventory receipt** posting.</span></span>

        ![Uppsetning á bókun innhreyfinga og úthreyfinga birgða](../media/image14.png)

    3. <span data-ttu-id="1144c-213">Gangið úr skugga um að fjárhagslykillinn sé settur upp fyrir bókun á **Millieining, lánardrottnar**.</span><span class="sxs-lookup"><span data-stu-id="1144c-213">Verify that a ledger account is set up for **Inter-unit payable** posting.</span></span>

        ![Bókun millieiningar lánardrottins sett upp](../media/image15.png)

    4. <span data-ttu-id="1144c-215">Gangið úr skugga um að fjárhagslykillinn sé settur upp fyrir bókun á **Millieining, viðskiptavinir**.</span><span class="sxs-lookup"><span data-stu-id="1144c-215">Verify that a ledger account is set up for **Inter-unit receivable** posting.</span></span>

        ![Bókun millieiningar viðskiptavinar sett upp](../media/image16.png)
