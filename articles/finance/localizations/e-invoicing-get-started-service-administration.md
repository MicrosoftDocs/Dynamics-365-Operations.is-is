---
title: Hafist handa með þjónustuveitu viðbótar rafrænnar reikningsfærslu
description: Þetta efnisatriði útskýrir hvernig á að hefjast handa með viðbót rafrænnar reikningsfærslu.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
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
ms.openlocfilehash: 111ec65aa826795125d4a9ce835f72e1a0f41b7b
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104393"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a><span data-ttu-id="49628-103">Hafist handa með þjónustuveitu viðbótar rafrænnar reikningsfærslu</span><span class="sxs-lookup"><span data-stu-id="49628-103">Get started with Electronic invoicing add-on service administration</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="49628-104">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="49628-104">Prerequisites</span></span>

<span data-ttu-id="49628-105">Áður en ferlið í þessu efnisatriði er klárað þurfa eftirfarandi skilyrði að vera til staðar:</span><span class="sxs-lookup"><span data-stu-id="49628-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="49628-106">Þú verður að hafa aðgang að reikningi á Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="49628-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="49628-107">Þú verður að vera með LCS-verk sem inniheldur útgáfu 10.0.13 eða nýrri af Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="49628-107">You must have an LCS project that includes version 10.0.13 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="49628-108">Þar að auki verða þessi forrit að vera sett upp á einni af eftirfarandi Azure-staðsetningum:</span><span class="sxs-lookup"><span data-stu-id="49628-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="49628-109">Austurhluti Bandaríkjanna</span><span class="sxs-lookup"><span data-stu-id="49628-109">East US</span></span>
    - <span data-ttu-id="49628-110">Vesturhluti Bandaríkjanna</span><span class="sxs-lookup"><span data-stu-id="49628-110">West US</span></span>
    - <span data-ttu-id="49628-111">Norðurhluti Evrópusambandsins</span><span class="sxs-lookup"><span data-stu-id="49628-111">North EU</span></span>
    - <span data-ttu-id="49628-112">Vesturhluti Evrópusambandsins</span><span class="sxs-lookup"><span data-stu-id="49628-112">West EU</span></span>

- <span data-ttu-id="49628-113">Þú verður að hafa aðgang að reikningnum þínum hjá Dynamics 365 Regulatory Configuration Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="49628-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="49628-114">Þú verður að virkja altækan eiginleika fyrir RCS-reikninginn þinn í eiginleikastjórnun.</span><span class="sxs-lookup"><span data-stu-id="49628-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="49628-115">Frekari upplýsingar er að finna í [Regulatory Configuration Services (RCS) – Altækir eiginleikar](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="49628-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="49628-116">Stofna verður lyklageymslu og geymslureikning í Azure.</span><span class="sxs-lookup"><span data-stu-id="49628-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="49628-117">Frekari upplýsingar er að finna í [Stofna Azure-geymslureikning og lyklageymslu](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="49628-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a><span data-ttu-id="49628-118">Setja upp viðbótina fyrir microservices í Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="49628-118">Install the add-on for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="49628-119">Skráðu þig inn á LCS-reikninginn þinn.</span><span class="sxs-lookup"><span data-stu-id="49628-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="49628-120">Veldu reitinn **Stjórnun forskoðunareiginleika**.</span><span class="sxs-lookup"><span data-stu-id="49628-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="49628-121">Í hlutanum **Opnir forskoðunareiginleikar** skal velja **Þjónusta rafrænnar reikningsfærslu**.</span><span class="sxs-lookup"><span data-stu-id="49628-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="49628-122">Gangið úr skugga um að valkosturinn **Virkja forskoðunareiginleika** sé stilltur á **Já**.</span><span class="sxs-lookup"><span data-stu-id="49628-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>

## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="49628-123">Setja upp færibreytur fyrir RCS-samþættingu við viðbót rafrænnar reikningsfærslu</span><span class="sxs-lookup"><span data-stu-id="49628-123">Set up the parameters for RCS integration with the Electronic invoicing add-on</span></span>

1. <span data-ttu-id="49628-124">Skráðu þig inn á RCS-reikninginn þinn.</span><span class="sxs-lookup"><span data-stu-id="49628-124">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="49628-125">Í vinnusvæðinu **Rafræn skýrslugerð** í kaflanum **Skyldir tenglar**, velurðu **Færibreytur rafrænnar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="49628-125">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="49628-126">Í flipanum **Þjónusta rafrænnar reikningsfærslu**, í reitinn **URI fyrir endastöð þjónustu** skal slá inn viðeigandi endastöð þjónustu fyrir Azure-staðfestninguna þína eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="49628-126">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="49628-127">Gagnamiðstöð Azure-staðsetningar</span><span class="sxs-lookup"><span data-stu-id="49628-127">Datacenter Azure geography</span></span> | <span data-ttu-id="49628-128">URI fyrir endastöð þjónustu</span><span class="sxs-lookup"><span data-stu-id="49628-128">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="49628-129">Austurhluti Bandaríkjanna</span><span class="sxs-lookup"><span data-stu-id="49628-129">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="49628-130">Vesturhluti Bandaríkjanna</span><span class="sxs-lookup"><span data-stu-id="49628-130">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="49628-131">Norðurhluti Evrópusambandsins</span><span class="sxs-lookup"><span data-stu-id="49628-131">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="49628-132">Vesturhluti Evrópusambandsins</span><span class="sxs-lookup"><span data-stu-id="49628-132">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="49628-133">Gangið úr skugga um að reiturinn **Forritsauðkenni** sé stilltur á **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="49628-133">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="49628-134">Gildið er fast.</span><span class="sxs-lookup"><span data-stu-id="49628-134">This value is a fixed value.</span></span>
5. <span data-ttu-id="49628-135">Í reitinn **LCS-umhverfiskenni** skal færa inn auðkenni LCS-áskriftarreiknings.</span><span class="sxs-lookup"><span data-stu-id="49628-135">In the **LCS Environment Id** field, enter the ID of your LCS subscription account.</span></span>
6. <span data-ttu-id="49628-136">Veljið **Vista** og lokið síðan skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="49628-136">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-secret"></a><span data-ttu-id="49628-137">Stofna leynilykil lyklageymslu</span><span class="sxs-lookup"><span data-stu-id="49628-137">Create Key Vault secret</span></span>

1. <span data-ttu-id="49628-138">Skráðu þig inn á RCS-reikninginn þinn.</span><span class="sxs-lookup"><span data-stu-id="49628-138">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="49628-139">Á vinnusvæðinu **Altækur eiginleiki**, undir hlutanum **Umhverfi**, skal velja reitinn **Rafræn reikningsfærsla**.</span><span class="sxs-lookup"><span data-stu-id="49628-139">In the **Globalization feature** workspace, in the **Environment** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="49628-140">Á síðunni **Uppsetningar umhverfis**, á aðgerðasvæðinu, skal velja **Þjónustuumhverfi** og síðan velja **Færibreytur lyklageymslu**.</span><span class="sxs-lookup"><span data-stu-id="49628-140">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="49628-141">Veljið **Nýr** til að stofna leynilykil lyklageymslu.</span><span class="sxs-lookup"><span data-stu-id="49628-141">Select **New** to create a key vault secret.</span></span>
5. <span data-ttu-id="49628-142">Í reitinn **Heiti** skal slá inn heiti á leynilykli lyklageymslu.</span><span class="sxs-lookup"><span data-stu-id="49628-142">In the **Name** field, enter the name of the key vault secret.</span></span> <span data-ttu-id="49628-143">Í reitnum **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="49628-143">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="49628-144">Í reitinn **URI lyklageymslu** skal líma leynilykilinn úr Azure-lyklageymslu.</span><span class="sxs-lookup"><span data-stu-id="49628-144">In the **Key Vault URI** field, paste the secret from Azure Key Vault.</span></span>
7. <span data-ttu-id="49628-145">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="49628-145">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="49628-146">Stofna leynilykil geymslureiknings</span><span class="sxs-lookup"><span data-stu-id="49628-146">Create Storage account secret</span></span>

1. <span data-ttu-id="49628-147">Á síðunni **Færibreytur lyklageymslu**, í hlutanum **Vottorð**, skal velja **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="49628-147">On **Key vault parameters** page, in the **Certificates** section, select **Add**.</span></span>
2. <span data-ttu-id="49628-148">Í reitinn **Heiti** skal færa inn það sama fyrir leynilykil geymslureiknings.</span><span class="sxs-lookup"><span data-stu-id="49628-148">In the **Name** field, enter the same of the storage account secret.</span></span> <span data-ttu-id="49628-149">Í reitnum **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="49628-149">In the **Description** field, enter a description.</span></span>
3. <span data-ttu-id="49628-150">Í reitnum **Gerð** skal velja **Vottorð**.</span><span class="sxs-lookup"><span data-stu-id="49628-150">In the **Type** field, select **Certificate**.</span></span>
4. <span data-ttu-id="49628-151">Veljið **Vista** og lokið síðan skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="49628-151">Select **Save**, and then close the page.</span></span>

## <a name="create-an-electronic-invoicing-add-on-environment"></a><span data-ttu-id="49628-152">Stofna umhverfi fyrir viðbót rafrænnar reikningsfærslu</span><span class="sxs-lookup"><span data-stu-id="49628-152">Create an Electronic invoicing add-on environment</span></span>

1. <span data-ttu-id="49628-153">Skráðu þig inn á RCS-reikninginn þinn.</span><span class="sxs-lookup"><span data-stu-id="49628-153">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="49628-154">Á vinnusvæðinu **Altækur eiginleiki**, undir hlutanum **Umhverfi**, skal velja reitinn **Rafræn reikningsfærsla**.</span><span class="sxs-lookup"><span data-stu-id="49628-154">In the **Globalization feature** workspace, in the **Environment** section, select the **e-Invoicing** tile.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="49628-155">Stofna þjónustuumhverfi</span><span class="sxs-lookup"><span data-stu-id="49628-155">Create a service environment</span></span>

1. <span data-ttu-id="49628-156">Á síðunni **Uppsetningar umhverfis**, á aðgerðasvæðinu, skal velja **Þjónustuumhverfi**.</span><span class="sxs-lookup"><span data-stu-id="49628-156">On the **Environment setups** page, on the action Pane, select **Service environment**.</span></span>
2. <span data-ttu-id="49628-157">Velja skal **Nýtt** til að stofna nýtt þjónustuumhverfi.</span><span class="sxs-lookup"><span data-stu-id="49628-157">Select **New** to create a new service environment.</span></span>
3. <span data-ttu-id="49628-158">Í reitinn **Heiti** skal slá inn heiti á umhverfi rafrænnar reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="49628-158">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="49628-159">Í reitnum **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="49628-159">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="49628-160">Í reitnum **SAS-leynilykill geymslu** skal velja heiti vottorðsins sem þarf að nota til að auðkenna aðgang að geymslureikningnum.</span><span class="sxs-lookup"><span data-stu-id="49628-160">In the **Storage SAS token secret** field, select the name of the certificate that must be used to authenticate access to the storage account.</span></span>
5. <span data-ttu-id="49628-161">Í hlutanum **Notendur** skal velja **Bæta við** til að bæta við notanda sem hefur heimild til að senda inn rafræna reikninga í gegnum umhverfið og einnig tengjast við geymslureikninginn.</span><span class="sxs-lookup"><span data-stu-id="49628-161">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
6. <span data-ttu-id="49628-162">Í reitinn **Notandakenni** skal færa inn samnefni notandans.</span><span class="sxs-lookup"><span data-stu-id="49628-162">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="49628-163">Í reitinn **Tölvupóstur** skal færa inn netfang notandans.</span><span class="sxs-lookup"><span data-stu-id="49628-163">In the **Email** field, enter the user's email address.</span></span>
7. <span data-ttu-id="49628-164">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="49628-164">Select **Save**.</span></span>
8. <span data-ttu-id="49628-165">Ef reikningar fyrir tiltekið land/svæði þurfa vottorðakeðju til að nota stafræna undirskrift, þá skal á aðgerðasvæðinu velja **Færibreytur lyklageymslu** og síðan velja **Vottorðakeðja** og fara í gegnum þessi skref:</span><span class="sxs-lookup"><span data-stu-id="49628-165">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>

    1. <span data-ttu-id="49628-166">Veljið **Ný** til að búa til nýja vottorðakeðju.</span><span class="sxs-lookup"><span data-stu-id="49628-166">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="49628-167">Í reitinn **Heiti** skal færa inn heiti vottorðakeðjunnar.</span><span class="sxs-lookup"><span data-stu-id="49628-167">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="49628-168">Í reitnum **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="49628-168">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="49628-169">Í hlutanum **Vottorð** skal velja **Bæta við** til að bæta vottorði við keðjuna.</span><span class="sxs-lookup"><span data-stu-id="49628-169">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="49628-170">Notið hnappinn **Upp** eða **Niður** til að breyta stöðu vottorðs í keðjunni.</span><span class="sxs-lookup"><span data-stu-id="49628-170">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="49628-171">Veljið **Vista** og lokið síðan skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="49628-171">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="49628-172">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="49628-172">Close the page.</span></span>
9. <span data-ttu-id="49628-173">Á síðunni **Þjónustuumhverfi**, á aðgerðasvæðinu, skal velja **Birta** til að birta umhverfið í skýinu.</span><span class="sxs-lookup"><span data-stu-id="49628-173">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="49628-174">Gildi reitsins **Staða** er breytt í **Birt**.</span><span class="sxs-lookup"><span data-stu-id="49628-174">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="49628-175">Búa til tengt forrit</span><span class="sxs-lookup"><span data-stu-id="49628-175">Create a connected application</span></span>

1. <span data-ttu-id="49628-176">Á síðunni **Uppsetningar umhverfis**, á aðgerðasvæðinu, skal velja **Tengd forrit**.</span><span class="sxs-lookup"><span data-stu-id="49628-176">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="49628-177">Veljið **Nýtt** til að stofna tengt forrit.</span><span class="sxs-lookup"><span data-stu-id="49628-177">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="49628-178">Í reitinn **Heiti** skal færa inn heiti forritsins sem á að tengja.</span><span class="sxs-lookup"><span data-stu-id="49628-178">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="49628-179">Í reitinn **Forrit** skal færa inn vefslóð fyrir umhverfi Finance and Supply Chain Management sem tengjast á við.</span><span class="sxs-lookup"><span data-stu-id="49628-179">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="49628-180">Í reitinn **Leigjandi** skal færa inn leigjanda umhverfis Finance and Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="49628-180">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="49628-181">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="49628-181">Select **Save**.</span></span>
6. <span data-ttu-id="49628-182">Á aðgerðasvæðinu skal velja **Athuga tengingu** til að prófa tenginguna við umhverfið.</span><span class="sxs-lookup"><span data-stu-id="49628-182">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="49628-183">Lokið því næst síðunni.</span><span class="sxs-lookup"><span data-stu-id="49628-183">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="49628-184">Tengja tengd forrit við umhverfi</span><span class="sxs-lookup"><span data-stu-id="49628-184">Link connected applications to environments</span></span>

1. <span data-ttu-id="49628-185">Á síðunni **Uppsetningar umhverfis** skal velja **Nýtt** til að úthluta tengdu forriti á umhverfi.</span><span class="sxs-lookup"><span data-stu-id="49628-185">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="49628-186">Í reitnum **Tengt forrit** skal velja tengt forrit.</span><span class="sxs-lookup"><span data-stu-id="49628-186">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="49628-187">Í reitnum **Þjónustuumhverfi** skal velja þjónustuumhverfi.</span><span class="sxs-lookup"><span data-stu-id="49628-187">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="49628-188">Veljið **Vista** og lokið síðan skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="49628-188">Select **Save**, and then close the page.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="49628-189">Setja upp samþættingu á viðbót rafrænnar reikningsfærslu í Finance and Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="49628-189">Set up the Electronic invoicing add-on integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="49628-190">Kveikið á eiginleika fyrir samþættingu rafrænnar reikningsfærsluviðbótar</span><span class="sxs-lookup"><span data-stu-id="49628-190">Turn on the Electronic invoicing add-on integration feature</span></span>

1. <span data-ttu-id="49628-191">Skráðu þig inn í tilvikið þitt af Finance eða Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="49628-191">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="49628-192">Á vinnusvæðinu **Eiginleikastjórnun** skal leita að eiginleikanum **Samþætting viðbótar rafrænnar reikningsfærslu**.</span><span class="sxs-lookup"><span data-stu-id="49628-192">In the **Feature management** workspace, search for the **Electronic invoicing add-on integration** feature.</span></span> <span data-ttu-id="49628-193">Ef þessi eiginleiki birtist ekki á síðunni skal velja **Athuga með uppfærslur**.</span><span class="sxs-lookup"><span data-stu-id="49628-193">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="49628-194">Veljið eiginleikann og veljið svo **Virkja núna**.</span><span class="sxs-lookup"><span data-stu-id="49628-194">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="49628-195">Setja upp vefslóð fyrir endastöð þjónustu</span><span class="sxs-lookup"><span data-stu-id="49628-195">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="49628-196">Farið í **Fyrirtækisstjórnun \> Uppsetning \> Færibreytur rafrænna skjala**.</span><span class="sxs-lookup"><span data-stu-id="49628-196">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="49628-197">Í flipanum **Innsendingarþjónusta**, í reitinn **Vefslóð fyrir endastöð þjónustu** skal slá inn viðeigandi endastöð þjónustu fyrir Azure-staðfestinguna þína eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="49628-197">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="49628-198">Gagnamiðstöð Azure-staðsetningar</span><span class="sxs-lookup"><span data-stu-id="49628-198">Datacenter Azure geography</span></span> | <span data-ttu-id="49628-199">ULR endastöð þjónustu</span><span class="sxs-lookup"><span data-stu-id="49628-199">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="49628-200">Austurhluti Bandaríkjanna</span><span class="sxs-lookup"><span data-stu-id="49628-200">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="49628-201">Vesturhluti Bandaríkjanna</span><span class="sxs-lookup"><span data-stu-id="49628-201">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="49628-202">Norðurhluti Evrópusambandsins</span><span class="sxs-lookup"><span data-stu-id="49628-202">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="49628-203">Vesturhluti Evrópusambandsins</span><span class="sxs-lookup"><span data-stu-id="49628-203">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="49628-204">Í reitinn **Umhverfi** skal færa inn heiti á umhverfi rafrænnar reikningsfærsluviðbótar.</span><span class="sxs-lookup"><span data-stu-id="49628-204">In the **Environment** field, enter the name of the Electronic invoicing add-on environment.</span></span>
4. <span data-ttu-id="49628-205">Veljið **Vista** og lokið síðan skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="49628-205">Select **Save**, and then close the page.</span></span>
