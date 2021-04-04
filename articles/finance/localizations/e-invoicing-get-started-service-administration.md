---
title: Hafist handa með þjónustuveitu viðbótar rafrænnar reikningsfærslu
description: Þetta efnisatriði útskýrir hvernig á að hefjast handa með viðbót rafrænnar reikningsfærslu.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 05b00380cec7511adad2467d3f252799a4aaee5c
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592527"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a><span data-ttu-id="9ecb5-103">Hafist handa með þjónustuveitu viðbótar rafrænnar reikningsfærslu</span><span class="sxs-lookup"><span data-stu-id="9ecb5-103">Get started with Electronic invoicing add-on service administration</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="9ecb5-104">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="9ecb5-104">Prerequisites</span></span>

<span data-ttu-id="9ecb5-105">Áður en ferlið í þessu efnisatriði er klárað þurfa eftirfarandi skilyrði að vera til staðar:</span><span class="sxs-lookup"><span data-stu-id="9ecb5-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="9ecb5-106">Þú verður að hafa aðgang að reikningi á Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="9ecb5-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="9ecb5-107">Þú verður að vera með LCS-verk sem inniheldur útgáfu 10.0.17 eða nýrri af Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="9ecb5-108">Þar að auki verða þessi forrit að vera sett upp á einni af eftirfarandi Azure-staðsetningum:</span><span class="sxs-lookup"><span data-stu-id="9ecb5-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="9ecb5-109">Austurhluti Bandaríkjanna</span><span class="sxs-lookup"><span data-stu-id="9ecb5-109">East US</span></span>
    - <span data-ttu-id="9ecb5-110">Vesturhluti Bandaríkjanna</span><span class="sxs-lookup"><span data-stu-id="9ecb5-110">West US</span></span>
    - <span data-ttu-id="9ecb5-111">Norðurhluti Evrópusambandsins</span><span class="sxs-lookup"><span data-stu-id="9ecb5-111">North EU</span></span>
    - <span data-ttu-id="9ecb5-112">Vesturhluti Evrópusambandsins</span><span class="sxs-lookup"><span data-stu-id="9ecb5-112">West EU</span></span>

- <span data-ttu-id="9ecb5-113">Þú verður að hafa aðgang að reikningnum þínum hjá Dynamics 365 Regulatory Configuration Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="9ecb5-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="9ecb5-114">Þú verður að virkja altækan eiginleika fyrir RCS-reikninginn þinn í eiginleikastjórnun.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="9ecb5-115">Frekari upplýsingar er að finna í [Regulatory Configuration Services (RCS) – Altækir eiginleikar](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="9ecb5-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="9ecb5-116">Stofna verður lyklageymslu og geymslureikning í Azure.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="9ecb5-117">Frekari upplýsingar er að finna í [Stofna Azure-geymslureikning og lyklageymslu](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="9ecb5-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a><span data-ttu-id="9ecb5-118">Setja upp viðbótina fyrir microservices í Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="9ecb5-118">Install the add-on for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="9ecb5-119">Skráðu þig inn á LCS-reikninginn þinn.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="9ecb5-120">Veldu reitinn **Stjórnun forskoðunareiginleika**.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="9ecb5-121">Í hlutanum **Opnir forskoðunareiginleikar** skal velja **Þjónusta rafrænnar reikningsfærslu**.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="9ecb5-122">Gangið úr skugga um að valkosturinn **Virkja forskoðunareiginleika** sé stilltur á **Já**.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="9ecb5-123">Á LCS-stjórnborðinu skal velja LCS-uppsetningarverkið.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="9ecb5-124">LCS-verkið verður að vera í gangi.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="9ecb5-125">Í flipanum **Innbætur umhverfis** skal velja **Setja upp nýja innbót**.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="9ecb5-126">Veljið **Rafrænar reikningsfærsluþjónustur** og í reitinn **AAD-forritskenni** skal færa inn **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-126">Select **e-invoicing Services** and in the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="9ecb5-127">Þetta er fast gildi.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-127">This is a fixed value.</span></span>
10. <span data-ttu-id="9ecb5-128">Í reitinn **AAD-leigjandakenni** skal færa inn leigjandakenni Azure-áskriftareiknings.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-128">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="9ecb5-129">Farið yfir skilmálana og veljið því næst gátreitinn.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-129">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="9ecb5-130">Velja **Setja upp**.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-130">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="9ecb5-131">Setja upp færibreytur fyrir RCS-samþættingu við viðbót rafrænnar reikningsfærslu</span><span class="sxs-lookup"><span data-stu-id="9ecb5-131">Set up the parameters for RCS integration with the Electronic invoicing add-on</span></span>

1. <span data-ttu-id="9ecb5-132">Skráðu þig inn á RCS-reikninginn þinn.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-132">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="9ecb5-133">Í vinnusvæðinu **Rafræn skýrslugerð** í kaflanum **Skyldir tenglar**, velurðu **Færibreytur rafrænnar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-133">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="9ecb5-134">Í flipanum **Þjónusta rafrænnar reikningsfærslu**, í reitinn **URI fyrir endastöð þjónustu** skal slá inn viðeigandi endastöð þjónustu fyrir Azure-staðfestninguna þína eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-134">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="9ecb5-135">Gagnamiðstöð Azure-staðsetningar</span><span class="sxs-lookup"><span data-stu-id="9ecb5-135">Datacenter Azure geography</span></span> | <span data-ttu-id="9ecb5-136">URI fyrir endastöð þjónustu</span><span class="sxs-lookup"><span data-stu-id="9ecb5-136">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="9ecb5-137">Austurhluti Bandaríkjanna</span><span class="sxs-lookup"><span data-stu-id="9ecb5-137">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="9ecb5-138">Vesturhluti Bandaríkjanna</span><span class="sxs-lookup"><span data-stu-id="9ecb5-138">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="9ecb5-139">Norðurhluti Evrópusambandsins</span><span class="sxs-lookup"><span data-stu-id="9ecb5-139">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="9ecb5-140">Vesturhluti Evrópusambandsins</span><span class="sxs-lookup"><span data-stu-id="9ecb5-140">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="9ecb5-141">Gangið úr skugga um að reiturinn **Forritsauðkenni** sé stilltur á **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-141">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="9ecb5-142">Gildið er fast.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-142">This value is a fixed value.</span></span>
5. <span data-ttu-id="9ecb5-143">Í reitinn **LCS-umhverfiskenni** skal færa inn auðkenni LCS-áskriftarreiknings.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-143">In the **LCS Environment Id** field, enter the ID of your LCS subscription account.</span></span>
6. <span data-ttu-id="9ecb5-144">Veljið **Vista** og lokið síðan skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-144">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-secret"></a><span data-ttu-id="9ecb5-145">Stofna leynilykil lyklageymslu</span><span class="sxs-lookup"><span data-stu-id="9ecb5-145">Create Key Vault secret</span></span>

1. <span data-ttu-id="9ecb5-146">Skráðu þig inn á RCS-reikninginn þinn.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-146">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="9ecb5-147">Á vinnusvæðinu **Altækur eiginleiki**, í hlutanum **Umhverfi**, skal velja reitinn **Viðbót rafrænnar reikningsfærslu**.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-147">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>
3. <span data-ttu-id="9ecb5-148">Á síðunni **Uppsetningar umhverfis**, á aðgerðasvæðinu, skal velja **Þjónustuumhverfi** og síðan velja **Færibreytur lyklageymslu**.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-148">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="9ecb5-149">Veljið **Nýr** til að stofna leynilykil lyklageymslu.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-149">Select **New** to create a key vault secret.</span></span>
5. <span data-ttu-id="9ecb5-150">Í reitinn **Heiti** skal slá inn heiti á leynilykli lyklageymslu.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-150">In the **Name** field, enter the name of the key vault secret.</span></span> <span data-ttu-id="9ecb5-151">Í reitnum **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-151">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="9ecb5-152">Í reitinn **URI lyklageymslu** skal líma leynilykilinn úr Azure-lyklageymslu.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-152">In the **Key Vault URI** field, paste the secret from Azure Key Vault.</span></span>
7. <span data-ttu-id="9ecb5-153">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-153">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="9ecb5-154">Stofna leynilykil geymslureiknings</span><span class="sxs-lookup"><span data-stu-id="9ecb5-154">Create Storage account secret</span></span>

1. <span data-ttu-id="9ecb5-155">Farið í **Kerfisstjórnun** > **Uppsetning** > **Færibreytur lyklageymslu** og veljið leynilykil lyklageymslu.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-155">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="9ecb5-156">Í hlutanum **Vottorð** skal velja **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-156">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="9ecb5-157">Í reitinn **Heiti** skal færa inn heiti leynilykils geymslureikningsins og í reitinn **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-157">In the **Name** field, enter the name of the storage account secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="9ecb5-158">Í reitnum **Gerð** skal velja **Vottorð**.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-158">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="9ecb5-159">Veljið **Vista** og lokið síðan skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-159">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="9ecb5-160">Búa til leynilykil stafræns vottorðs</span><span class="sxs-lookup"><span data-stu-id="9ecb5-160">Create a digital certificate secret</span></span>

1. <span data-ttu-id="9ecb5-161">Farið í **Kerfisstjórnun** > **Uppsetning** > **Færibreytur lyklageymslu** og veljið leynilykil lyklageymslu.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-161">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="9ecb5-162">Í hlutanum **Vottorð** skal velja **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-162">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="9ecb5-163">Í reitinn **Heiti** skal færa inn heiti leynilykils stafræns vottorðs og í reitinn **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-163">In the **Name** field, enter the name of the digital certificate secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="9ecb5-164">Í reitnum **Gerð** skal velja **Vottorð**.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-164">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="9ecb5-165">Veljið **Vista** og lokið síðan skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-165">Select **Save**, and then close the page.</span></span>

## <a name="create-an-electronic-invoicing-add-on-environment"></a><span data-ttu-id="9ecb5-166">Stofna umhverfi fyrir viðbót rafrænnar reikningsfærslu</span><span class="sxs-lookup"><span data-stu-id="9ecb5-166">Create an Electronic invoicing add-on environment</span></span>

1. <span data-ttu-id="9ecb5-167">Skráðu þig inn á RCS-reikninginn þinn.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-167">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="9ecb5-168">Á vinnusvæðinu **Altækur eiginleiki**, í hlutanum **Umhverfi**, skal velja reitinn **Viðbót rafrænnar reikningsfærslu**.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-168">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="9ecb5-169">Stofna þjónustuumhverfi</span><span class="sxs-lookup"><span data-stu-id="9ecb5-169">Create a service environment</span></span>

1. <span data-ttu-id="9ecb5-170">Á síðunni **Uppsetningar umhverfis**, á aðgerðasvæðinu, skal velja **Þjónustuumhverfi**.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-170">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
2. <span data-ttu-id="9ecb5-171">Velja skal **Nýtt** til að stofna nýtt þjónustuumhverfi.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-171">Select **New** to create a new service environment.</span></span>
3. <span data-ttu-id="9ecb5-172">Í reitinn **Heiti** skal slá inn heiti á umhverfi rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-172">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="9ecb5-173">Í reitnum **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-173">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="9ecb5-174">Í reitnum **SAS-leynilykill geymslu** skal velja heiti leynilykils geymslureikningsins sem þarf að nota til að auðkenna aðgang að geymslureikningnum.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-174">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
5. <span data-ttu-id="9ecb5-175">Í hlutanum **Notendur** skal velja **Bæta við** til að bæta við notanda sem hefur heimild til að senda inn rafræna reikninga í gegnum umhverfið og einnig tengjast við geymslureikninginn.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-175">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
6. <span data-ttu-id="9ecb5-176">Í reitinn **Notandakenni** skal færa inn samnefni notandans.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-176">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="9ecb5-177">Í reitinn **Tölvupóstur** skal færa inn netfang notandans.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-177">In the **Email** field, enter the user's email address.</span></span>
7. <span data-ttu-id="9ecb5-178">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-178">Select **Save**.</span></span>
8. <span data-ttu-id="9ecb5-179">Ef reikningar fyrir tiltekið land/svæði þurfa vottorðakeðju til að nota stafræna undirskrift, þá skal á aðgerðasvæðinu velja **Færibreytur lyklageymslu** og síðan velja **Vottorðakeðja** og fara í gegnum þessi skref:</span><span class="sxs-lookup"><span data-stu-id="9ecb5-179">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>

    1. <span data-ttu-id="9ecb5-180">Veljið **Ný** til að búa til nýja vottorðakeðju.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-180">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="9ecb5-181">Í reitinn **Heiti** skal færa inn heiti vottorðakeðjunnar.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-181">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="9ecb5-182">Í reitnum **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-182">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="9ecb5-183">Í hlutanum **Vottorð** skal velja **Bæta við** til að bæta vottorði við keðjuna.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-183">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="9ecb5-184">Notið hnappinn **Upp** eða **Niður** til að breyta stöðu vottorðs í keðjunni.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-184">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="9ecb5-185">Veljið **Vista** og lokið síðan skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-185">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="9ecb5-186">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-186">Close the page.</span></span>
9. <span data-ttu-id="9ecb5-187">Á síðunni **Þjónustuumhverfi**, á aðgerðasvæðinu, skal velja **Birta** til að birta umhverfið í skýinu.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-187">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="9ecb5-188">Gildi reitsins **Staða** er breytt í **Birt**.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-188">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="9ecb5-189">Búa til tengt forrit</span><span class="sxs-lookup"><span data-stu-id="9ecb5-189">Create a connected application</span></span>

1. <span data-ttu-id="9ecb5-190">Á síðunni **Uppsetningar umhverfis**, á aðgerðasvæðinu, skal velja **Tengd forrit**.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-190">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="9ecb5-191">Veljið **Nýtt** til að stofna tengt forrit.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-191">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="9ecb5-192">Í reitinn **Heiti** skal færa inn heiti forritsins sem á að tengja.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-192">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="9ecb5-193">Í reitinn **Forrit** skal færa inn vefslóð fyrir umhverfi Finance and Supply Chain Management sem tengjast á við.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-193">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="9ecb5-194">Í reitinn **Leigjandi** skal færa inn leigjanda umhverfis Finance and Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-194">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="9ecb5-195">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-195">Select **Save**.</span></span>
6. <span data-ttu-id="9ecb5-196">Á aðgerðasvæðinu skal velja **Athuga tengingu** til að prófa tenginguna við umhverfið.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-196">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="9ecb5-197">Lokið því næst síðunni.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-197">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="9ecb5-198">Tengja tengd forrit við umhverfi</span><span class="sxs-lookup"><span data-stu-id="9ecb5-198">Link connected applications to environments</span></span>

1. <span data-ttu-id="9ecb5-199">Á síðunni **Uppsetningar umhverfis** skal velja **Nýtt** til að úthluta tengdu forriti á umhverfi.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-199">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="9ecb5-200">Í reitnum **Tengt forrit** skal velja tengt forrit.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-200">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="9ecb5-201">Í reitnum **Þjónustuumhverfi** skal velja þjónustuumhverfi.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-201">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="9ecb5-202">Veljið **Vista** og lokið síðan skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-202">Select **Save**, and then close the page.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="9ecb5-203">Setja upp samþættingu á viðbót rafrænnar reikningsfærslu í Finance and Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="9ecb5-203">Set up the Electronic invoicing add-on integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="9ecb5-204">Kveikið á eiginleika fyrir samþættingu rafrænnar reikningsfærsluviðbótar</span><span class="sxs-lookup"><span data-stu-id="9ecb5-204">Turn on the Electronic invoicing add-on integration feature</span></span>

1. <span data-ttu-id="9ecb5-205">Skráðu þig inn í tilvikið þitt af Finance eða Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-205">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="9ecb5-206">Á vinnusvæðinu **Eiginleikastjórnun** skal leita að eiginleikanum **Samþætting viðbótar rafrænnar reikningsfærslu**.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-206">In the **Feature management** workspace, search for the **Electronic invoicing add-on integration** feature.</span></span> <span data-ttu-id="9ecb5-207">Ef þessi eiginleiki birtist ekki á síðunni skal velja **Athuga með uppfærslur**.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-207">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="9ecb5-208">Veljið eiginleikann og veljið svo **Virkja núna**.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-208">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="9ecb5-209">Setja upp vefslóð fyrir endastöð þjónustu</span><span class="sxs-lookup"><span data-stu-id="9ecb5-209">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="9ecb5-210">Farið í **Fyrirtækisstjórnun \> Uppsetning \> Færibreytur rafrænna skjala**.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="9ecb5-211">Í flipanum **Innsendingarþjónusta**, í reitinn **Vefslóð fyrir endastöð þjónustu** skal slá inn viðeigandi endastöð þjónustu fyrir Azure-staðfestinguna þína eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-211">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="9ecb5-212">Gagnamiðstöð Azure-staðsetningar</span><span class="sxs-lookup"><span data-stu-id="9ecb5-212">Datacenter Azure geography</span></span> | <span data-ttu-id="9ecb5-213">ULR endastöð þjónustu</span><span class="sxs-lookup"><span data-stu-id="9ecb5-213">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="9ecb5-214">Austurhluti Bandaríkjanna</span><span class="sxs-lookup"><span data-stu-id="9ecb5-214">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="9ecb5-215">Vesturhluti Bandaríkjanna</span><span class="sxs-lookup"><span data-stu-id="9ecb5-215">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="9ecb5-216">Norðurhluti Evrópusambandsins</span><span class="sxs-lookup"><span data-stu-id="9ecb5-216">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="9ecb5-217">Vesturhluti Evrópusambandsins</span><span class="sxs-lookup"><span data-stu-id="9ecb5-217">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="9ecb5-218">Í reitinn **Umhverfi** skal færa inn heiti á umhverfi rafrænnar reikningsfærsluviðbótar.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-218">In the **Environment** field, enter the name of the Electronic invoicing add-on environment.</span></span>
4. <span data-ttu-id="9ecb5-219">Veljið **Vista** og lokið síðan skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="9ecb5-219">Select **Save**, and then close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
