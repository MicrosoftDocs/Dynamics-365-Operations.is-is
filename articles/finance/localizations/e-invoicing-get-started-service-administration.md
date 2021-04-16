---
title: Hafist handa með þjónustu rafrænna reikninga fyrir Brasilíu
description: Þetta efnisatriði útskýrir hvernig á að hefjast handa með rafrænni reikningsfærslu.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ec431cb4a3620459d905f64a80fd820a2113290f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840149"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a><span data-ttu-id="11f86-103">Hafist handa með þjónustu rafrænna reikninga fyrir Brasilíu</span><span class="sxs-lookup"><span data-stu-id="11f86-103">Get started with Electronic invoicing service administration</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="11f86-104">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="11f86-104">Prerequisites</span></span>

<span data-ttu-id="11f86-105">Áður en ferlið í þessu efnisatriði er klárað þurfa eftirfarandi skilyrði að vera til staðar:</span><span class="sxs-lookup"><span data-stu-id="11f86-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="11f86-106">Þú verður að hafa aðgang að reikningi á Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="11f86-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="11f86-107">Þú verður að vera með LCS-verk sem inniheldur útgáfu 10.0.17 eða nýrri af Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="11f86-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="11f86-108">Þar að auki verða þessi forrit að vera sett upp á einni af eftirfarandi Azure-staðsetningum:</span><span class="sxs-lookup"><span data-stu-id="11f86-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="11f86-109">Austurhluti Bandaríkjanna</span><span class="sxs-lookup"><span data-stu-id="11f86-109">East US</span></span>
    - <span data-ttu-id="11f86-110">Vesturhluti Bandaríkjanna</span><span class="sxs-lookup"><span data-stu-id="11f86-110">West US</span></span>
    - <span data-ttu-id="11f86-111">Norðurhluti Evrópusambandsins</span><span class="sxs-lookup"><span data-stu-id="11f86-111">North EU</span></span>
    - <span data-ttu-id="11f86-112">Vesturhluti Evrópusambandsins</span><span class="sxs-lookup"><span data-stu-id="11f86-112">West EU</span></span>

- <span data-ttu-id="11f86-113">Þú verður að hafa aðgang að reikningnum þínum hjá Dynamics 365 Regulatory Configuration Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="11f86-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="11f86-114">Þú verður að virkja altækan eiginleika fyrir RCS-reikninginn þinn í eiginleikastjórnun.</span><span class="sxs-lookup"><span data-stu-id="11f86-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="11f86-115">Frekari upplýsingar er að finna í [Regulatory Configuration Services (RCS) – Altækir eiginleikar](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="11f86-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="11f86-116">Stofna verður lyklageymslu og geymslureikning í Azure.</span><span class="sxs-lookup"><span data-stu-id="11f86-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="11f86-117">Frekari upplýsingar er að finna í [Stofna Azure-geymslureikning og lyklageymslu](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="11f86-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a><span data-ttu-id="11f86-118">Setja upp innbótina fyrir microservices í Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="11f86-118">Install the add-in for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="11f86-119">Skráðu þig inn á LCS-reikninginn þinn.</span><span class="sxs-lookup"><span data-stu-id="11f86-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="11f86-120">Veldu reitinn **Stjórnun forskoðunareiginleika**.</span><span class="sxs-lookup"><span data-stu-id="11f86-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="11f86-121">Í hlutanum **Opnir forskoðunareiginleikar** skal velja **Þjónusta rafrænnar reikningsfærslu**.</span><span class="sxs-lookup"><span data-stu-id="11f86-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="11f86-122">Gangið úr skugga um að valkosturinn **Virkja forskoðunareiginleika** sé stilltur á **Já**.</span><span class="sxs-lookup"><span data-stu-id="11f86-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="11f86-123">Á LCS-stjórnborðinu skal velja LCS-uppsetningarverkið.</span><span class="sxs-lookup"><span data-stu-id="11f86-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="11f86-124">LCS-verkið verður að vera í gangi.</span><span class="sxs-lookup"><span data-stu-id="11f86-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="11f86-125">Í flipanum **Innbætur umhverfis** skal velja **Setja upp nýja innbót**.</span><span class="sxs-lookup"><span data-stu-id="11f86-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="11f86-126">Veljið **Þjónusta rafrænnar reikningsfærslu**.</span><span class="sxs-lookup"><span data-stu-id="11f86-126">Select **e-invoicing Services**.</span></span>
9. <span data-ttu-id="11f86-127">Í reitinn **AAD-forritskenni** skal færa inn **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span><span class="sxs-lookup"><span data-stu-id="11f86-127">In the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="11f86-128">Þetta er fast gildi.</span><span class="sxs-lookup"><span data-stu-id="11f86-128">This is a fixed value.</span></span>
10. <span data-ttu-id="11f86-129">Í reitinn **AAD-leigjandakenni** skal færa inn leigjandakenni Azure-áskriftareiknings.</span><span class="sxs-lookup"><span data-stu-id="11f86-129">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="11f86-130">Farið yfir skilmálana og veljið því næst gátreitinn.</span><span class="sxs-lookup"><span data-stu-id="11f86-130">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="11f86-131">Velja **Setja upp**.</span><span class="sxs-lookup"><span data-stu-id="11f86-131">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a><span data-ttu-id="11f86-132">Setja upp færibreytur fyrir RCS-samþættingu við rafræna reikningsfærslu</span><span class="sxs-lookup"><span data-stu-id="11f86-132">Set up the parameters for RCS integration with Electronic invoicing</span></span>

1. <span data-ttu-id="11f86-133">Skráðu þig inn á RCS-reikninginn þinn.</span><span class="sxs-lookup"><span data-stu-id="11f86-133">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="11f86-134">Í vinnusvæðinu **Rafræn skýrslugerð** í kaflanum **Skyldir tenglar**, velurðu **Færibreytur rafrænnar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="11f86-134">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="11f86-135">Í flipanum **Þjónusta rafrænnar reikningsfærslu**, í reitinn **URI fyrir endastöð þjónustu** skal slá inn viðeigandi endastöð þjónustu fyrir Azure-staðfestninguna þína eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="11f86-135">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="11f86-136">Gagnamiðstöð Azure-staðsetningar</span><span class="sxs-lookup"><span data-stu-id="11f86-136">Datacenter Azure geography</span></span> | <span data-ttu-id="11f86-137">URI fyrir endastöð þjónustu</span><span class="sxs-lookup"><span data-stu-id="11f86-137">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="11f86-138">Austurhluti Bandaríkjanna</span><span class="sxs-lookup"><span data-stu-id="11f86-138">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="11f86-139">Vesturhluti Bandaríkjanna</span><span class="sxs-lookup"><span data-stu-id="11f86-139">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="11f86-140">Norðurhluti Evrópusambandsins</span><span class="sxs-lookup"><span data-stu-id="11f86-140">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="11f86-141">Vesturhluti Evrópusambandsins</span><span class="sxs-lookup"><span data-stu-id="11f86-141">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="11f86-142">Gangið úr skugga um að reiturinn **Forritsauðkenni** sé stilltur á **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="11f86-142">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="11f86-143">Gildið er fast.</span><span class="sxs-lookup"><span data-stu-id="11f86-143">This value is a fixed value.</span></span>
5. <span data-ttu-id="11f86-144">Í reitinn **LCS-umhverfiskenni** skal færa inn auðkenni LCS-umhverfis.</span><span class="sxs-lookup"><span data-stu-id="11f86-144">In the **LCS Environment Id** field, enter the ID of your LCS environment.</span></span>
6. <span data-ttu-id="11f86-145">Veljið **Vista** og lokið síðan skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="11f86-145">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-references"></a><span data-ttu-id="11f86-146">Stofna tilvísanir lyklageymslu</span><span class="sxs-lookup"><span data-stu-id="11f86-146">Create Key Vault references</span></span>

1. <span data-ttu-id="11f86-147">Skráðu þig inn á RCS-reikninginn þinn.</span><span class="sxs-lookup"><span data-stu-id="11f86-147">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="11f86-148">Á vinnusvæðinu **Altækur eiginleiki**, í hlutanum **Umhverfi**, skal velja reitinn **Rafræn reikningsfærsla**.</span><span class="sxs-lookup"><span data-stu-id="11f86-148">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="11f86-149">Á síðunni **Uppsetningar umhverfis**, á aðgerðasvæðinu, skal velja **Þjónustuumhverfi** og síðan velja **Færibreytur lyklageymslu**.</span><span class="sxs-lookup"><span data-stu-id="11f86-149">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="11f86-150">Veljið **Nýr** til að stofna tilvísun lyklageymslu.</span><span class="sxs-lookup"><span data-stu-id="11f86-150">Select **New** to create a key vault reference.</span></span>
5. <span data-ttu-id="11f86-151">Í reitinn **Heiti** skal slá inn heiti á tilvísun lyklageymslu.</span><span class="sxs-lookup"><span data-stu-id="11f86-151">In the **Name** field, enter the name of the key vault reference.</span></span> <span data-ttu-id="11f86-152">Í reitnum **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="11f86-152">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="11f86-153">Í reitinn **URI lyklageymslu** skal líma leyniorð leynilykilinn úr Azure-lyklageymslu.</span><span class="sxs-lookup"><span data-stu-id="11f86-153">In the **Key Vault URI** field, paste the key vault secret from Azure Key Vault.</span></span> <span data-ttu-id="11f86-154">Frekari upplýsingar er að finna í [Stofna Azure-geymslureikning og lyklageymslu](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="11f86-154">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
7. <span data-ttu-id="11f86-155">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="11f86-155">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="11f86-156">Stofna leynilykil geymslureiknings</span><span class="sxs-lookup"><span data-stu-id="11f86-156">Create Storage account secret</span></span>

1. <span data-ttu-id="11f86-157">Á síðunni **Uppsetningar umhverfis**, á aðgerðasvæðinu, skal velja **Þjónustuumhverfi** > **Færibreytur lyklageymslu**.</span><span class="sxs-lookup"><span data-stu-id="11f86-157">On the **Environment setups** page, on the Action Pane, select **Service environment** > **Key Vault parameters**.</span></span>
2. <span data-ttu-id="11f86-158">Veljið **Tilvísun lyklageymslu** og í **Vottorð** hlutanum skal velja **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="11f86-158">Select a **Key Vault reference** and in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="11f86-159">Í reitinn **Heiti** skal færa inn heiti fyrir leynilykil geymslureiknings.</span><span class="sxs-lookup"><span data-stu-id="11f86-159">In the **Name** field, enter the name of the storage account secret.</span></span> <span data-ttu-id="11f86-160">Frekari upplýsingar er að finna í [Stofna Azure-geymslureikning og lyklageymslu](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="11f86-160">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="11f86-161">Í reitnum **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="11f86-161">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="11f86-162">Í reitnum **Gerð** skal velja **Leynilykill**.</span><span class="sxs-lookup"><span data-stu-id="11f86-162">In the **Type** field, select **Secret**.</span></span>
6. <span data-ttu-id="11f86-163">Veljið **Vista** og lokið síðan skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="11f86-163">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="11f86-164">Búa til leynilykil stafræns vottorðs</span><span class="sxs-lookup"><span data-stu-id="11f86-164">Create a digital certificate secret</span></span>

1. <span data-ttu-id="11f86-165">Á síðunni **Uppsetningar umhverfis**, á aðgerðasvæðinu, skal velja **Þjónustuumhverfi** og síðan velja **Færibreytur lyklageymslu**.</span><span class="sxs-lookup"><span data-stu-id="11f86-165">On the **Environment setups** page, on the action Pane, select **Service environment** and then select **Key Vault parameters**.</span></span>
2. <span data-ttu-id="11f86-166">Veljið **Tilvísun lyklageymslu** og svo í **Vottorð** hlutanum skal velja **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="11f86-166">Select a **Key Vault reference** and then in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="11f86-167">Heiti leynilykils stafræna skírteinisins er sleginn í reitinn **Nafn**.</span><span class="sxs-lookup"><span data-stu-id="11f86-167">In the **Name** field, enter the name of the digital certificate secret.</span></span> <span data-ttu-id="11f86-168">Frekari upplýsingar er að finna í [Stofna Azure-geymslureikning og lyklageymslu](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="11f86-168">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="11f86-169">Í reitnum **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="11f86-169">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="11f86-170">Í reitnum **Gerð** skal velja **Vottorð**.</span><span class="sxs-lookup"><span data-stu-id="11f86-170">In the **Type** field, select **Certificate**.</span></span>
6. <span data-ttu-id="11f86-171">Veljið **Vista** og lokið síðan skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="11f86-171">Select **Save**, and then close the page.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="11f86-172">Stofna þjónustuumhverfi</span><span class="sxs-lookup"><span data-stu-id="11f86-172">Create a service environment</span></span>

1. <span data-ttu-id="11f86-173">Skráðu þig inn á RCS-reikninginn þinn.</span><span class="sxs-lookup"><span data-stu-id="11f86-173">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="11f86-174">Á vinnusvæðinu **Altækur eiginleiki**, í hlutanum **Umhverfi**, skal velja reitinn **Rafræn reikningsfærsla**.</span><span class="sxs-lookup"><span data-stu-id="11f86-174">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="11f86-175">Á síðunni **Uppsetningar umhverfis**, á aðgerðasvæðinu, skal velja **Þjónustuumhverfi**.</span><span class="sxs-lookup"><span data-stu-id="11f86-175">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
4. <span data-ttu-id="11f86-176">Velja skal **Nýtt** til að stofna nýtt þjónustuumhverfi.</span><span class="sxs-lookup"><span data-stu-id="11f86-176">Select **New** to create a new service environment.</span></span>
5. <span data-ttu-id="11f86-177">Í reitinn **Heiti** skal slá inn heiti á umhverfi rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="11f86-177">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="11f86-178">Í reitnum **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="11f86-178">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="11f86-179">Í reitnum **SAS-leynilykill geymslu** skal velja heiti leynilykils geymslureikningsins sem þarf að nota til að auðkenna aðgang að geymslureikningnum.</span><span class="sxs-lookup"><span data-stu-id="11f86-179">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
7. <span data-ttu-id="11f86-180">Í hlutanum **Notendur** skal velja **Bæta við** til að bæta við notanda sem hefur heimild til að senda inn rafræna reikninga í gegnum umhverfið og einnig tengjast við geymslureikninginn.</span><span class="sxs-lookup"><span data-stu-id="11f86-180">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
8. <span data-ttu-id="11f86-181">Í reitinn **Notandakenni** skal færa inn samnefni notandans.</span><span class="sxs-lookup"><span data-stu-id="11f86-181">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="11f86-182">Í reitinn **Tölvupóstur** skal færa inn netfang notandans.</span><span class="sxs-lookup"><span data-stu-id="11f86-182">In the **Email** field, enter the user's email address.</span></span>
9. <span data-ttu-id="11f86-183">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="11f86-183">Select **Save**.</span></span>
10. <span data-ttu-id="11f86-184">Ef reikningar fyrir tiltekið land/svæði þurfa vottorðakeðju til að nota stafræna undirskrift, þá skal á aðgerðasvæðinu velja **Færibreytur lyklageymslu** og síðan velja **Vottorðakeðja** og fara í gegnum þessi skref:</span><span class="sxs-lookup"><span data-stu-id="11f86-184">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>
    1. <span data-ttu-id="11f86-185">Veljið **Ný** til að búa til nýja vottorðakeðju.</span><span class="sxs-lookup"><span data-stu-id="11f86-185">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="11f86-186">Í reitinn **Heiti** skal færa inn heiti vottorðakeðjunnar.</span><span class="sxs-lookup"><span data-stu-id="11f86-186">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="11f86-187">Í reitnum **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="11f86-187">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="11f86-188">Í hlutanum **Vottorð** skal velja **Bæta við** til að bæta vottorði við keðjuna.</span><span class="sxs-lookup"><span data-stu-id="11f86-188">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="11f86-189">Notið hnappinn **Upp** eða **Niður** til að breyta stöðu vottorðs í keðjunni.</span><span class="sxs-lookup"><span data-stu-id="11f86-189">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="11f86-190">Veljið **Vista** og lokið síðan skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="11f86-190">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="11f86-191">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="11f86-191">Close the page.</span></span>
11. <span data-ttu-id="11f86-192">Á síðunni **Þjónustuumhverfi**, á aðgerðasvæðinu, skal velja **Birta** til að birta umhverfið í skýinu.</span><span class="sxs-lookup"><span data-stu-id="11f86-192">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="11f86-193">Gildi reitsins **Staða** er breytt í **Birt**.</span><span class="sxs-lookup"><span data-stu-id="11f86-193">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="11f86-194">Búa til tengt forrit</span><span class="sxs-lookup"><span data-stu-id="11f86-194">Create a connected application</span></span>

1. <span data-ttu-id="11f86-195">Á síðunni **Uppsetningar umhverfis**, á aðgerðasvæðinu, skal velja **Tengd forrit**.</span><span class="sxs-lookup"><span data-stu-id="11f86-195">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="11f86-196">Veljið **Nýtt** til að stofna tengt forrit.</span><span class="sxs-lookup"><span data-stu-id="11f86-196">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="11f86-197">Í reitinn **Heiti** skal færa inn heiti forritsins sem á að tengja.</span><span class="sxs-lookup"><span data-stu-id="11f86-197">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="11f86-198">Í reitinn **Forrit** skal færa inn vefslóð fyrir umhverfi Finance and Supply Chain Management sem tengjast á við.</span><span class="sxs-lookup"><span data-stu-id="11f86-198">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="11f86-199">Í reitinn **Leigjandi** skal færa inn leigjanda umhverfis Finance and Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="11f86-199">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="11f86-200">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="11f86-200">Select **Save**.</span></span>
6. <span data-ttu-id="11f86-201">Á aðgerðasvæðinu skal velja **Athuga tengingu** til að prófa tenginguna við umhverfið.</span><span class="sxs-lookup"><span data-stu-id="11f86-201">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="11f86-202">Lokið því næst síðunni.</span><span class="sxs-lookup"><span data-stu-id="11f86-202">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="11f86-203">Tengja tengd forrit við umhverfi</span><span class="sxs-lookup"><span data-stu-id="11f86-203">Link connected applications to environments</span></span>

1. <span data-ttu-id="11f86-204">Á síðunni **Uppsetningar umhverfis** skal velja **Nýtt** til að úthluta tengdu forriti á umhverfi.</span><span class="sxs-lookup"><span data-stu-id="11f86-204">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="11f86-205">Í reitnum **Tengt forrit** skal velja tengt forrit.</span><span class="sxs-lookup"><span data-stu-id="11f86-205">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="11f86-206">Í reitnum **Þjónustuumhverfi** skal velja þjónustuumhverfi.</span><span class="sxs-lookup"><span data-stu-id="11f86-206">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="11f86-207">Veljið **Vista** og lokið síðan skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="11f86-207">Select **Save**, and then close the page.</span></span>

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="11f86-208">Setja upp samþættingu á rafrænni reikningsfærslu í Finance and Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="11f86-208">Set up Electronic invoicing integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a><span data-ttu-id="11f86-209">Kveikið á eiginleika fyrir samþættingu rafrænnar reikningsfærslu</span><span class="sxs-lookup"><span data-stu-id="11f86-209">Turn on the Electronic invoicing integration feature</span></span>

1. <span data-ttu-id="11f86-210">Skráðu þig inn í tilvikið þitt af Finance eða Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="11f86-210">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="11f86-211">Á vinnusvæðinu **Eiginleikastjórnun** skal leita að eiginleikanum **Samþætting rafrænnar reikningsfærslu**.</span><span class="sxs-lookup"><span data-stu-id="11f86-211">In the **Feature management** workspace, search for the **Electronic invoicing integration** feature.</span></span> <span data-ttu-id="11f86-212">Ef þessi eiginleiki birtist ekki á síðunni skal velja **Athuga með uppfærslur**.</span><span class="sxs-lookup"><span data-stu-id="11f86-212">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="11f86-213">Veljið eiginleikann og veljið svo **Virkja núna**.</span><span class="sxs-lookup"><span data-stu-id="11f86-213">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="11f86-214">Setja upp vefslóð fyrir endastöð þjónustu</span><span class="sxs-lookup"><span data-stu-id="11f86-214">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="11f86-215">Farið í **Fyrirtækisstjórnun \> Uppsetning \> Færibreytur rafrænna skjala**.</span><span class="sxs-lookup"><span data-stu-id="11f86-215">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="11f86-216">Í flipanum **Innsendingarþjónusta**, í reitinn **Vefslóð fyrir endastöð þjónustu** skal slá inn viðeigandi endastöð þjónustu fyrir Azure-staðfestinguna þína eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="11f86-216">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="11f86-217">Gagnamiðstöð Azure-staðsetningar</span><span class="sxs-lookup"><span data-stu-id="11f86-217">Datacenter Azure geography</span></span> | <span data-ttu-id="11f86-218">ULR endastöð þjónustu</span><span class="sxs-lookup"><span data-stu-id="11f86-218">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="11f86-219">Austurhluti Bandaríkjanna</span><span class="sxs-lookup"><span data-stu-id="11f86-219">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="11f86-220">Vesturhluti Bandaríkjanna</span><span class="sxs-lookup"><span data-stu-id="11f86-220">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="11f86-221">Norðurhluti Evrópusambandsins</span><span class="sxs-lookup"><span data-stu-id="11f86-221">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="11f86-222">Vesturhluti Evrópusambandsins</span><span class="sxs-lookup"><span data-stu-id="11f86-222">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="11f86-223">Í reitinn **Umhverfi** skal færa inn heiti á þjónustuumhverfi sem er birt í rafrænni reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="11f86-223">In the **Environment** field, enter the name of the service environment published in Electronic invoicing.</span></span>
4. <span data-ttu-id="11f86-224">Veljið **Vista** og lokið síðan skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="11f86-224">Select **Save**, and then close the page.</span></span>

### <a name="enable-flighting-keys"></a><span data-ttu-id="11f86-225">Virkja fluglykla</span><span class="sxs-lookup"><span data-stu-id="11f86-225">Enable Flighting keys</span></span>

<span data-ttu-id="11f86-226">Virkjaðu fluglykla fyrir Microsoft Dynamics 365 Finance eða Microsoft Dynamics 365 Supply Chain Management útgáfu 10.0.17 eða eldri.</span><span class="sxs-lookup"><span data-stu-id="11f86-226">Enable Flight keys for  Microsoft Dynamics 365 Finance or  Microsoft Dynamics 365 Supply Chain Management versions 10.0.17 or earlier.</span></span> 
1. <span data-ttu-id="11f86-227">Framkvæmið eftirfarandi SQL-skipun:</span><span class="sxs-lookup"><span data-stu-id="11f86-227">Execute the following SQL command:</span></span>

    <span data-ttu-id="11f86-228">SETJA INN Í SYSFLIGHTING (ÚTGÁFUHEITI, VIRKJAÐ) GILDI ('BusinessDocumentSubmissionServiceEnabled', 1)</span><span class="sxs-lookup"><span data-stu-id="11f86-228">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span></span>
    
    <span data-ttu-id="11f86-229">SETJA INN Í SYSFLIGHTING (ÚTGÁFUHEITI, VIRKJAÐ) GILDI ('ElectronicInvoicingServiceIntegrationFeature', 1)</span><span class="sxs-lookup"><span data-stu-id="11f86-229">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span></span>

2. <span data-ttu-id="11f86-230">Framkvæma IISreset-skipun fyrir öll AOS.</span><span class="sxs-lookup"><span data-stu-id="11f86-230">Perform an IISreset command for all AOS's.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
