---
title: Setja upp Azure-tilföng fyrir IoT-gervigreind
description: Þetta efnisatriði útskýrir hvernig á að stofna og skilgreina Microsoft Azure-tilföng sem krafist er fyrir IoT-gervigreind.
author: ''
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bbac1676d28c7285c19ed48f77426a37ce123a29
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982895"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a><span data-ttu-id="a75df-103">Setja upp Azure-tilföng fyrir IoT-gervigreind</span><span class="sxs-lookup"><span data-stu-id="a75df-103">Set up Azure resources for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a75df-104">Þetta efnisatriði útskýrir hvernig á að stofna og skilgreina Microsoft Azure-tilföng sem krafist er fyrir IoT-gervigreind.</span><span class="sxs-lookup"><span data-stu-id="a75df-104">This topic explains how to create and configure the Microsoft Azure resources that you require for IoT Intelligence.</span></span>

## <a name="create-azure-resources"></a><span data-ttu-id="a75df-105">Stofna Azure-tilföng</span><span class="sxs-lookup"><span data-stu-id="a75df-105">Create Azure resources</span></span>

<span data-ttu-id="a75df-106">Fylgdu þessum skrefum til að búa til IoT-miðstöð, Redis-skyndiminni og lyklageymslu sem hægt er að opna með Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a75df-106">Follow these steps to create an IoT hub, a Redis cache, and a key vault that can be accessed by Microsoft Dynamics 365 Supply Chain Management.</span></span>

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a><span data-ttu-id="a75df-107">Gangið úr skugga um að forritskenni Microsoft Dynamics ERP Microservices fyrir fyrsta aðila sé í leigjanda</span><span class="sxs-lookup"><span data-stu-id="a75df-107">Verify that the Microsoft Dynamics ERP Microservices first-party app ID is in your tenant</span></span>

<span data-ttu-id="a75df-108">Til að staðfesta að forritskennið fyrir Microsoft Dynamics ERP Microservices forrit fyrir fyrsta aðila sé í leigjandanum skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="a75df-108">To verify that the app ID for the Microsoft Dynamics ERP Microservices first-party app is in your tenant, follow these steps.</span></span>

1. <span data-ttu-id="a75df-109">Skráðu þig inn á Azure-gáttina á <https://portal.azure.com>.</span><span class="sxs-lookup"><span data-stu-id="a75df-109">Sign in to the Azure portal at <https://portal.azure.com>.</span></span>
2. <span data-ttu-id="a75df-110">Opnið **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="a75df-110">Go to **Azure Active Directory**.</span></span>
3. <span data-ttu-id="a75df-111">Opnaðu **Enterprise-forrit**.</span><span class="sxs-lookup"><span data-stu-id="a75df-111">Go to **Enterprise applications**.</span></span>
4. <span data-ttu-id="a75df-112">Í reitnum **Gerð forrits** skal velja **Microsoft-forrit**.</span><span class="sxs-lookup"><span data-stu-id="a75df-112">In the **Application type** field, select **Microsoft applications**.</span></span>
5. <span data-ttu-id="a75df-113">Í leitarreitinn skal færa inn **Microsoft Dynamics ERP Microservices**.</span><span class="sxs-lookup"><span data-stu-id="a75df-113">In the search field, enter **Microsoft Dynamics ERP Microservices**.</span></span>
6. <span data-ttu-id="a75df-114">Gangið úr skugga um að **Microsoft Dynamics ERP Microservices** sé á listanum.</span><span class="sxs-lookup"><span data-stu-id="a75df-114">Verify that **Microsoft Dynamics ERP Microservices** is in the list.</span></span> <span data-ttu-id="a75df-115">Önnur forrit eru með svipuð heiti.</span><span class="sxs-lookup"><span data-stu-id="a75df-115">Other applications have similar names.</span></span> <span data-ttu-id="a75df-116">Þess vegna skal ganga úr skugga um að rétt forrit sé fundið.</span><span class="sxs-lookup"><span data-stu-id="a75df-116">Therefore, make sure that you find the correct application.</span></span> <span data-ttu-id="a75df-117">Forritskenni er **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="a75df-117">The app ID is **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="a75df-118">Ef forritið er ekki á listanum verður að bæta því við leigjandann þinn:</span><span class="sxs-lookup"><span data-stu-id="a75df-118">If the application isn't in the list, you must add it to your tenant:</span></span>

    1. <span data-ttu-id="a75df-119">Í Azure-gáttinni, á tækjastikunni, skal velja hnappinn til að opna Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="a75df-119">In the Azure portal, on the toolbar, select the button to open Azure Cloud Shell.</span></span>
    2. <span data-ttu-id="a75df-120">Keyrið skipunina **Install-Module AzureAD**.</span><span class="sxs-lookup"><span data-stu-id="a75df-120">Run the command **Install-Module AzureAD**.</span></span> <span data-ttu-id="a75df-121">Sláið inn **Y** til að setja upp eininguna.</span><span class="sxs-lookup"><span data-stu-id="a75df-121">Enter **Y** to install the module.</span></span>
    3. <span data-ttu-id="a75df-122">Keyrið skipunina **Get-InstalledModule -Name "AzureAD"** til að staðfesta að einingin sé uppsett.</span><span class="sxs-lookup"><span data-stu-id="a75df-122">Run the command **Get-InstalledModule -Name "AzureAD"** to verify that the module is installed.</span></span>
    4. <span data-ttu-id="a75df-123">Keyrið skipunina **Connect-AzureAD -Confirm** til að keyra auðkenninguna.</span><span class="sxs-lookup"><span data-stu-id="a75df-123">Run the command **Connect-AzureAD -Confirm** to run the authentication.</span></span>
    5. <span data-ttu-id="a75df-124">Keyrið skipunina **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="a75df-124">Run the command **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="a75df-125">Nú er hægt að endurtaka skref 1 til 6 til að staðfesta að forritskennið sé í leigjandanum.</span><span class="sxs-lookup"><span data-stu-id="a75df-125">You can now repeat steps 1 through 6 to verify that the app ID is in your tenant.</span></span>

### <a name="create-a-key-vault-resource"></a><span data-ttu-id="a75df-126">Stofna tilföng lyklageymslu</span><span class="sxs-lookup"><span data-stu-id="a75df-126">Create a key vault resource</span></span>

<span data-ttu-id="a75df-127">Til að búa til tilföng lyklageymslu skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="a75df-127">To create a key vault resource, follow these steps.</span></span>

1. <span data-ttu-id="a75df-128">Í Azure-gátt skal búa til eða fara í tilfangaflokk.</span><span class="sxs-lookup"><span data-stu-id="a75df-128">In the Azure portal, create or go to a resource group.</span></span>
2. <span data-ttu-id="a75df-129">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="a75df-129">Select **Add**.</span></span>
3. <span data-ttu-id="a75df-130">Á leitarreit á síðunni **Nýtt** skal slá inn **Lyklageymsla**.</span><span class="sxs-lookup"><span data-stu-id="a75df-130">On the **New** page, in the search field, enter **Key vault**.</span></span> <span data-ttu-id="a75df-131">Veldu síðan **Búa til**.</span><span class="sxs-lookup"><span data-stu-id="a75df-131">Then select **Create**.</span></span>
4. <span data-ttu-id="a75df-132">Á síðunni **Búa til lyklageymslu**, í reitnum **Heiti lyklageymslu** skaltu slá inn heiti.</span><span class="sxs-lookup"><span data-stu-id="a75df-132">On the **Create key vault** page, in the **Key vault name** field, enter a name.</span></span>
5. <span data-ttu-id="a75df-133">Farið yfir sjálfgildi og veljið síðan **Fara yfir + Búa til**.</span><span class="sxs-lookup"><span data-stu-id="a75df-133">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="a75df-134">Velja **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="a75df-134">Select **Create**.</span></span>

<span data-ttu-id="a75df-135">Lyklageymslan er búin til í bakgrunni.</span><span class="sxs-lookup"><span data-stu-id="a75df-135">The key vault is created in the background.</span></span>

### <a name="create-an-iot-hub-resource"></a><span data-ttu-id="a75df-136">Búa til tilföng á IoT-miðstöð</span><span class="sxs-lookup"><span data-stu-id="a75df-136">Create an IoT hub resource</span></span>

<span data-ttu-id="a75df-137">Til að búa til tilföng á IoT-miðstöð skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="a75df-137">To create an IoT hub resource, follow these steps.</span></span>

1. <span data-ttu-id="a75df-138">Stofna eða fara í tilfangaflokk.</span><span class="sxs-lookup"><span data-stu-id="a75df-138">Create or go to a resource group.</span></span>
2. <span data-ttu-id="a75df-139">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="a75df-139">Select **Add**.</span></span>
3. <span data-ttu-id="a75df-140">Á leitarreitnum á síðunni **Nýtt** skaltu slá inn **IoT-miðstöð**.</span><span class="sxs-lookup"><span data-stu-id="a75df-140">On the **New** page, in the search field, enter **Iot Hub**.</span></span> <span data-ttu-id="a75df-141">Veldu síðan **Búa til**.</span><span class="sxs-lookup"><span data-stu-id="a75df-141">Then select **Create**.</span></span>
4. <span data-ttu-id="a75df-142">Sláðu inn heiti í reitinn **Heiti IoT-miðstöðvar**.</span><span class="sxs-lookup"><span data-stu-id="a75df-142">In the **IoT hub name** field, enter a name.</span></span>
5. <span data-ttu-id="a75df-143">Farið yfir sjálfgildi og veljið síðan **Fara yfir + Búa til**.</span><span class="sxs-lookup"><span data-stu-id="a75df-143">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="a75df-144">Velja **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="a75df-144">Select **Create**.</span></span>

<span data-ttu-id="a75df-145">IoT-miðstöð er stofnuð í bakgrunni.</span><span class="sxs-lookup"><span data-stu-id="a75df-145">The IoT hub is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="a75df-146">Mælt er með því að aðeins sé búið að stofna eitt tilföng fyrir IoT-miðstöð fyrir hvert umhverfi.</span><span class="sxs-lookup"><span data-stu-id="a75df-146">We recommend that you create only one IoT hub resource per environment.</span></span>

### <a name="create-a-redis-cache-resource"></a><span data-ttu-id="a75df-147">Stofna tilföng fyrir Redis-skyndiminni</span><span class="sxs-lookup"><span data-stu-id="a75df-147">Create a Redis cache resource</span></span>

<span data-ttu-id="a75df-148">Til að stofna tilföng fyrir Redis-skyndiminni skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="a75df-148">To create a Redis cache resource, follow these steps.</span></span>

1. <span data-ttu-id="a75df-149">Stofna eða fara í tilfangaflokk.</span><span class="sxs-lookup"><span data-stu-id="a75df-149">Create or go to a resource group.</span></span>
2. <span data-ttu-id="a75df-150">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="a75df-150">Select **Add**.</span></span>
3. <span data-ttu-id="a75df-151">Á leitarreitnum á síðunni **Nýtt** skaltu slá inn **Azure-skyndiminni fyrir Redis**.</span><span class="sxs-lookup"><span data-stu-id="a75df-151">On the **New** page, in the search field, enter **Azure Cache for Redis**.</span></span> <span data-ttu-id="a75df-152">Veldu síðan **Búa til**.</span><span class="sxs-lookup"><span data-stu-id="a75df-152">Then select **Create**.</span></span>
4. <span data-ttu-id="a75df-153">Í reitinn **DNS-heiti** skal færa inn heiti.</span><span class="sxs-lookup"><span data-stu-id="a75df-153">In the **DNS name** field, enter a name.</span></span>
5. <span data-ttu-id="a75df-154">Farið yfir sjálfgefin gildi og veljið síðan **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="a75df-154">Review the default values, and then select **Create**.</span></span>

<span data-ttu-id="a75df-155">Skyndiminni Redis er búið til í bakgrunni.</span><span class="sxs-lookup"><span data-stu-id="a75df-155">The Redis cache is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="a75df-156">Við mælum með því að aðeins eitt Redis skyndiminni sé stofnað fyrir hvert umhverfi.</span><span class="sxs-lookup"><span data-stu-id="a75df-156">We recommend that you create only one Redis cache per environment.</span></span>

<span data-ttu-id="a75df-157">Öll tilföng hafa nú verið stofnuð.</span><span class="sxs-lookup"><span data-stu-id="a75df-157">All the resources have now been created.</span></span>

## <a name="configure-the-azure-resources"></a><span data-ttu-id="a75df-158">Skilgreina Azure-tilföngin</span><span class="sxs-lookup"><span data-stu-id="a75df-158">Configure the Azure resources</span></span>

### <a name="configure-the-iot-hub"></a><span data-ttu-id="a75df-159">Skilgreina IoT-miðstöð</span><span class="sxs-lookup"><span data-stu-id="a75df-159">Configure the IoT hub</span></span>

<span data-ttu-id="a75df-160">Til að skilgreina IoT-miðstöð skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="a75df-160">To configure the IoT hub, follow these steps.</span></span>

1. <span data-ttu-id="a75df-161">Í tilföngum skal velja tilföng IoT-miðstöðvar.</span><span class="sxs-lookup"><span data-stu-id="a75df-161">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="a75df-162">Á vinstri yfirlitssvæði skal velja **Innbyggðar endastöðvar**.</span><span class="sxs-lookup"><span data-stu-id="a75df-162">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="a75df-163">Undir **neytendahópar** skal líma eftirfarandi neytendahópa.</span><span class="sxs-lookup"><span data-stu-id="a75df-163">Under **Consumer groups**, paste the following consumer groups.</span></span> <span data-ttu-id="a75df-164">Þessir neytendahópar samsvara aðstæðum „úr kassanum“.</span><span class="sxs-lookup"><span data-stu-id="a75df-164">These consumer groups correspond to the out-of-box scenarios.</span></span>

    + <span data-ttu-id="a75df-165">microsoft.dynamics.iotintelligence-1</span><span class="sxs-lookup"><span data-stu-id="a75df-165">microsoft.dynamics.iotintelligence-1</span></span>
    + <span data-ttu-id="a75df-166">microsoft.dynamics.iotintelligence-2</span><span class="sxs-lookup"><span data-stu-id="a75df-166">microsoft.dynamics.iotintelligence-2</span></span>
    + <span data-ttu-id="a75df-167">microsoft.dynamics.iotintelligence-3</span><span class="sxs-lookup"><span data-stu-id="a75df-167">microsoft.dynamics.iotintelligence-3</span></span>

### <a name="configure-the-key-vault"></a><span data-ttu-id="a75df-168">Stilla lyklageymslu</span><span class="sxs-lookup"><span data-stu-id="a75df-168">Configure the key vault</span></span>

<span data-ttu-id="a75df-169">Til að skilgreina lyklageymsluna skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="a75df-169">To configure the key vault, follow these steps.</span></span>

1. <span data-ttu-id="a75df-170">Í tilföngum skal velja tilföng lyklageymslunnar.</span><span class="sxs-lookup"><span data-stu-id="a75df-170">In your resources, select the key vault resource.</span></span>
2. <span data-ttu-id="a75df-171">Á vinstri yfirlitssvæði skal velja **Access-reglur**.</span><span class="sxs-lookup"><span data-stu-id="a75df-171">In the left navigation pane, select **Access policies**.</span></span>
3. <span data-ttu-id="a75df-172">Veljið **Bæta við aðgangsreglu**.</span><span class="sxs-lookup"><span data-stu-id="a75df-172">Select **Add an access policy**.</span></span>
4. <span data-ttu-id="a75df-173">Á síðunni **Bæta við aðgangsreglu**, í reitinum **Heimildir leyniorðs**, skal velja **Sækja** og **Listi**.</span><span class="sxs-lookup"><span data-stu-id="a75df-173">On the **Add access policy** page, in the **Secret permissions** field, select **Get** and **List**.</span></span>
5. <span data-ttu-id="a75df-174">Smelltu á **Velja aðalreikning**.</span><span class="sxs-lookup"><span data-stu-id="a75df-174">Click in the **Select principal**.</span></span>
6. <span data-ttu-id="a75df-175">Í svarglugganum **Aðalreikningur** skal leita að og velja **Microsoft Dynamics ERP Microservices**.</span><span class="sxs-lookup"><span data-stu-id="a75df-175">In the **Principal** dialog box, search for and select **Microsoft Dynamics ERP Microservices**.</span></span> <span data-ttu-id="a75df-176">Veljið síðan **Velja**.</span><span class="sxs-lookup"><span data-stu-id="a75df-176">Then select **Select**.</span></span>
7. <span data-ttu-id="a75df-177">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="a75df-177">Select **Add**.</span></span>
8. <span data-ttu-id="a75df-178">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="a75df-178">Select **Save**.</span></span>

<span data-ttu-id="a75df-179">Forritið hefur nú aðgang að leyniorðum í lyklageymslunni.</span><span class="sxs-lookup"><span data-stu-id="a75df-179">The app now has access to the secrets in the key vault.</span></span>

### <a name="save-the-iot-hub-connection-string-secret"></a><span data-ttu-id="a75df-180">Vista leyniorð fyrir tengistreng IoT-miðstöðvar</span><span class="sxs-lookup"><span data-stu-id="a75df-180">Save the IoT hub connection string secret</span></span>

<span data-ttu-id="a75df-181">Fylgdu þessum skrefum til að vista leyniorðið fyrir tengistreng IoT-miðstöðvar.</span><span class="sxs-lookup"><span data-stu-id="a75df-181">To save the secret for the IoT hub connection string, follow these steps.</span></span>

1. <span data-ttu-id="a75df-182">Í tilföngum skal velja tilföng IoT-miðstöðvar.</span><span class="sxs-lookup"><span data-stu-id="a75df-182">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="a75df-183">Á vinstri yfirlitssvæði skal velja **Innbyggðar endastöðvar**.</span><span class="sxs-lookup"><span data-stu-id="a75df-183">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="a75df-184">Afritið gildið í reitnum **Endastöð samhæf miðstöð tilviks**.</span><span class="sxs-lookup"><span data-stu-id="a75df-184">Copy the value in the **Event Hub-compatible endpoint** field.</span></span>
4. <span data-ttu-id="a75df-185">Opnaðu tilföng lyklageymslu.</span><span class="sxs-lookup"><span data-stu-id="a75df-185">Go to the key vault resource.</span></span>
5. <span data-ttu-id="a75df-186">Á vinstra yfirlitssvæðinu skal velja **Leyniorð**.</span><span class="sxs-lookup"><span data-stu-id="a75df-186">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="a75df-187">Veljið **Mynda/Flytja inn**.</span><span class="sxs-lookup"><span data-stu-id="a75df-187">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="a75df-188">Færið inn lýsandi nafn í reitinn **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="a75df-188">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="a75df-189">Í reitnum **Gildi** skal líma gildi endastöðvar sem var afritað áður.</span><span class="sxs-lookup"><span data-stu-id="a75df-189">In the **Value** field, paste the endpoint value that you copied earlier.</span></span>
9. <span data-ttu-id="a75df-190">Velja **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="a75df-190">Select **Create**.</span></span>

### <a name="save-the-redis-cache-connection-string-secret"></a><span data-ttu-id="a75df-191">Vista leyniorð tengistrengs Redis-skyndiminnis</span><span class="sxs-lookup"><span data-stu-id="a75df-191">Save the Redis cache connection string secret</span></span>

<span data-ttu-id="a75df-192">Til að vista leyniorðið fyrir tengistreng Redis-skyndiminnis skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="a75df-192">To save the secret for the Redis cache connection string, follow these steps.</span></span>

1. <span data-ttu-id="a75df-193">Í tilföngum skal velja tilfang Redis-skyndiminnis.</span><span class="sxs-lookup"><span data-stu-id="a75df-193">In your resources, select the Redis cache resource.</span></span>
2. <span data-ttu-id="a75df-194">Veljið **Aðgangslyklar**.</span><span class="sxs-lookup"><span data-stu-id="a75df-194">Select **Access keys**.</span></span>
3. <span data-ttu-id="a75df-195">Afritið gildið í reitnum **Aðaltengistrengur**.</span><span class="sxs-lookup"><span data-stu-id="a75df-195">Copy the value in the **Primary connection string** field.</span></span>
4. <span data-ttu-id="a75df-196">Opnaðu tilföng lyklageymslu.</span><span class="sxs-lookup"><span data-stu-id="a75df-196">Go to the key vault resource.</span></span>
5. <span data-ttu-id="a75df-197">Á vinstra yfirlitssvæðinu skal velja **Leyniorð**.</span><span class="sxs-lookup"><span data-stu-id="a75df-197">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="a75df-198">Veljið **Mynda/Flytja inn**.</span><span class="sxs-lookup"><span data-stu-id="a75df-198">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="a75df-199">Færið inn lýsandi nafn í reitinn **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="a75df-199">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="a75df-200">Í reitnum **Gildi** skal líma tengistrenginn sem var afritaður áður.</span><span class="sxs-lookup"><span data-stu-id="a75df-200">In the **Value** field, paste the connection string that you copied earlier.</span></span>
9. <span data-ttu-id="a75df-201">Velja **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="a75df-201">Select **Create**.</span></span>

> [!NOTE]
> <span data-ttu-id="a75df-202">Þegar einn af tengistrengnum er uppfærður þarf einnig að uppfæra leynigildin.</span><span class="sxs-lookup"><span data-stu-id="a75df-202">Whenever you update one of the connection strings, you must also update the secret values.</span></span>

<span data-ttu-id="a75df-203">Nú er úthlutun nauðsynlegra Azure-tilfanga lokið.</span><span class="sxs-lookup"><span data-stu-id="a75df-203">You've now finished provisioning the required Azure resources.</span></span> <span data-ttu-id="a75df-204">Næsta skref er að [setja upp IoT-gervigreind viðbótina í Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="a75df-204">The next step is to [install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>
