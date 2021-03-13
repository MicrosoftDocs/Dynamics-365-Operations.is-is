---
title: Innbót birgðasýnileika
description: Þetta efnisatriði lýsir því hvernig á að setja upp og grunnstilla innbót birgðasýnileika fyrir Dynamics 365 Supply Chain Management.
author: sherry-zheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4e6f7e0a3978bbf7e520f8cbcfd27c4cfe507777
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114671"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="e22ae-103">Innbót birgðasýnileika</span><span class="sxs-lookup"><span data-stu-id="e22ae-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="e22ae-104">Innbót birgðasýnileika er sjálfstæð og einstaklega sveigjanleg örþjónusta sem býður upp á rakningu lagerbirgða í rauntíma og veitir þar af leiðandi alhliða yfirlit yfir sýnileika birgða.</span><span class="sxs-lookup"><span data-stu-id="e22ae-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="e22ae-105">Allar upplýsingar sem tengjast birgðum á lager eru fluttar út í þjónustuna í nánast rauntíma í gegnum SQL-samþættingu á lágu stigi.</span><span class="sxs-lookup"><span data-stu-id="e22ae-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="e22ae-106">Ytri kerfi fá aðgang að þjónustunni í gegnum RESTful API til að spyrjast fyrir um lagerbirgðir á uppgefnum víddasamstæðum, sem fær þá lista yfir lausar lagerstöður.</span><span class="sxs-lookup"><span data-stu-id="e22ae-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="e22ae-107">Birgðasýnileiki er örþjónusta byggð á Microsoft Dataverse, sem þýðir að hægt er að stækka hana með því að smíða Power Apps og nota Power BI til að bjóða upp á sérsniðna virkni til að uppfylla kröfur fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="e22ae-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="e22ae-108">Einnig er hægt að uppfæra vísinn til að gera birgðafyrirspurnir.</span><span class="sxs-lookup"><span data-stu-id="e22ae-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="e22ae-109">Birgðasýnileiki býður upp á grunnstillingarvalkosti sem gerir því kleift að samþættast við mörg kerfi þriðja aðila.</span><span class="sxs-lookup"><span data-stu-id="e22ae-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="e22ae-110">Hann styður staðlaða birgðavídd, sérsniðna stækkunarhæfni og staðlað, stillanlegt magn sem er reiknað út.</span><span class="sxs-lookup"><span data-stu-id="e22ae-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="e22ae-111">Þetta efnisatriði lýsir því hvernig á að setja upp og grunnstilla innbót birgðasýnileika fyrir Dynamics 365 Supply Chain Management og hvernig á að nota forritunarviðmót þess (API).</span><span class="sxs-lookup"><span data-stu-id="e22ae-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="e22ae-112">Setja upp innbót birgðasýnileika</span><span class="sxs-lookup"><span data-stu-id="e22ae-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="e22ae-113">Setja þarf upp innbót birgðasýnileika með því að nota Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="e22ae-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="e22ae-114">LCS er samstarfsgátt sem býður upp á umhverfi ásamt safni af reglulega uppfærðum þjónustum sem hjálpa til við að stjórna líftíma forritsins fyrir Dynamics 365 Finance and Operations forritin þín.</span><span class="sxs-lookup"><span data-stu-id="e22ae-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="e22ae-115">Frekari upplýsingar er að finna í [Tilföng Lifecycle Services](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span><span class="sxs-lookup"><span data-stu-id="e22ae-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="e22ae-116">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="e22ae-116">Prerequisites</span></span>

<span data-ttu-id="e22ae-117">Áður en þú setur upp innbót birgðasýnileika þarftu að gera eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="e22ae-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="e22ae-118">Fá LCS-innleiðingarverk með að minnsta kosti einu virku umhverfi í notkun.</span><span class="sxs-lookup"><span data-stu-id="e22ae-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="e22ae-119">Búa til beta-lykla fyrir tilboðin þín í LCS.</span><span class="sxs-lookup"><span data-stu-id="e22ae-119">Generate the beta keys for your offering in LCS.</span></span>
- <span data-ttu-id="e22ae-120">Virkja beta-lykla fyrir tilboðin þín fyrir notendur þína í LCS.</span><span class="sxs-lookup"><span data-stu-id="e22ae-120">Enable the beta keys for your offering for your user in LCS.</span></span>
- <span data-ttu-id="e22ae-121">Hafa skal samband við vöruteymi birgðasýnileika hjá Microsoft og gefa upp umhverfiskenni þar sem á að nota innbót birgðasýnileika.</span><span class="sxs-lookup"><span data-stu-id="e22ae-121">Contact the Microsoft Inventory Visibility product team and provide an environment ID where you want to deploy the Inventory Visibility Add-in.</span></span>

<span data-ttu-id="e22ae-122">Ef einhverjar spurningar vakna um þessi skilyrði er hægt að hafa samband við vöruteymi birgðasýnileika.</span><span class="sxs-lookup"><span data-stu-id="e22ae-122">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="e22ae-123">Setja upp innbótina</span><span class="sxs-lookup"><span data-stu-id="e22ae-123">Install the add-in</span></span>

<span data-ttu-id="e22ae-124">Til að setja upp innbót birgðasýnileika skal gera eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="e22ae-124">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="e22ae-125">Skráðu þig inn í gátt [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="e22ae-125">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="e22ae-126">Á heimasíðunni skal velja verkið þar sem umhverfið er í notkun.</span><span class="sxs-lookup"><span data-stu-id="e22ae-126">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="e22ae-127">Á verksíðunni skal velja umhverfið þar sem á að setja upp innbótina.</span><span class="sxs-lookup"><span data-stu-id="e22ae-127">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="e22ae-128">Á heimasíðu umhverfisins skal fletta niður á hlutann **Innbætur umhverfis**.</span><span class="sxs-lookup"><span data-stu-id="e22ae-128">On the environment page, scroll down until you see the **Environment add-ins** section.</span></span> <span data-ttu-id="e22ae-129">Ef hlutinn er ekki sýnilegur skal ganga úr skugga um að unnið hafi verið úr beta-lyklum forkröfu.</span><span class="sxs-lookup"><span data-stu-id="e22ae-129">If the section isn't visible, make sure the prerequisite beta keys have been fully processed.</span></span>
1. <span data-ttu-id="e22ae-130">Í hlutanum **Innbætur umhverfis** skal velja **Setja upp nýja innbót**.</span><span class="sxs-lookup"><span data-stu-id="e22ae-130">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
    <span data-ttu-id="e22ae-131">![Heimasíða umhverfis í LCS](media/inventory-visibility-environment.png "Heimasíða umhverfis í LCS")</span><span class="sxs-lookup"><span data-stu-id="e22ae-131">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>
1. <span data-ttu-id="e22ae-132">Veldu tengilinn **Setja upp nýja innbót**.</span><span class="sxs-lookup"><span data-stu-id="e22ae-132">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="e22ae-133">Listi yfir tiltækar innbætur opnast.</span><span class="sxs-lookup"><span data-stu-id="e22ae-133">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="e22ae-134">Veldu **Birgðaþjónustu** úr listanum.</span><span class="sxs-lookup"><span data-stu-id="e22ae-134">Select **Inventory service** from the list.</span></span> <span data-ttu-id="e22ae-135">(Athugið að þetta kann nú að vera skráð sem **Innbót birgðasýnileika fyrir Dynamics 365 Supply Chain Management**.)</span><span class="sxs-lookup"><span data-stu-id="e22ae-135">(Note, this may now be listed as **Inventory Visibility Add-in for Dynamics 365 Supply Chain Management**.)</span></span>
1. <span data-ttu-id="e22ae-136">Sláðu inn gildi fyrir eftirfarandi reiti fyrir umhverfið þitt:</span><span class="sxs-lookup"><span data-stu-id="e22ae-136">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="e22ae-137">**AAD-forritskenni**</span><span class="sxs-lookup"><span data-stu-id="e22ae-137">**AAD application ID**</span></span>
    - <span data-ttu-id="e22ae-138">**AAD-leigjandakenni**</span><span class="sxs-lookup"><span data-stu-id="e22ae-138">**AAD tenant ID**</span></span>

    <span data-ttu-id="e22ae-139">![Uppsetningarsíða innbótar](media/inventory-visibility-setup.png "Uppsetningarsíða innbótar")</span><span class="sxs-lookup"><span data-stu-id="e22ae-139">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="e22ae-140">Samþykktu skilmálana með því að velja gátreitinn **Skilmálar**.</span><span class="sxs-lookup"><span data-stu-id="e22ae-140">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="e22ae-141">Velja **Setja upp**.</span><span class="sxs-lookup"><span data-stu-id="e22ae-141">Select **Install**.</span></span> <span data-ttu-id="e22ae-142">Staða innbótarinnar birtist sem **Er í uppsetningu**.</span><span class="sxs-lookup"><span data-stu-id="e22ae-142">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="e22ae-143">Þegar henni er lokið skal uppfæra síðuna til að sjá stöðuna breytast í **Uppsett**.</span><span class="sxs-lookup"><span data-stu-id="e22ae-143">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="get-a-security-service-token"></a><span data-ttu-id="e22ae-144">Sækja merki öryggisþjónustu</span><span class="sxs-lookup"><span data-stu-id="e22ae-144">Get a security service token</span></span>

<span data-ttu-id="e22ae-145">Sækja merki öryggisþjónustu á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="e22ae-145">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="e22ae-146">Skráðu þig inn í Azure-gátt og notaðu hana til að finna `clientId` og `clientSecret` Supply Chain Management forritið.</span><span class="sxs-lookup"><span data-stu-id="e22ae-146">Sign in to Azure Portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="e22ae-147">Sækja Azure Active Directory tákn (`aadToken` ) með því að senda inn HTTP beiðni með eftirfarandi eiginleikum:</span><span class="sxs-lookup"><span data-stu-id="e22ae-147">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="e22ae-148">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="e22ae-148">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="e22ae-149">**Aðferð** - `GET`</span><span class="sxs-lookup"><span data-stu-id="e22ae-149">**Method** - `GET`</span></span>
    - <span data-ttu-id="e22ae-150">**Meginefni (eyðublaðagögn)**:</span><span class="sxs-lookup"><span data-stu-id="e22ae-150">**Body content (form data)**:</span></span>

        | <span data-ttu-id="e22ae-151">lykill</span><span class="sxs-lookup"><span data-stu-id="e22ae-151">key</span></span> | <span data-ttu-id="e22ae-152">gildi</span><span class="sxs-lookup"><span data-stu-id="e22ae-152">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="e22ae-153">client_id</span><span class="sxs-lookup"><span data-stu-id="e22ae-153">client_id</span></span> | <span data-ttu-id="e22ae-154">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="e22ae-154">${aadAppId}</span></span> |
        | <span data-ttu-id="e22ae-155">client_secret</span><span class="sxs-lookup"><span data-stu-id="e22ae-155">client_secret</span></span> | <span data-ttu-id="e22ae-156">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="e22ae-156">${aadAppSecret}</span></span> |
        | <span data-ttu-id="e22ae-157">grant_type</span><span class="sxs-lookup"><span data-stu-id="e22ae-157">grant_type</span></span> | <span data-ttu-id="e22ae-158">client_credentials</span><span class="sxs-lookup"><span data-stu-id="e22ae-158">client_credentials</span></span> |
        | <span data-ttu-id="e22ae-159">tilföng</span><span class="sxs-lookup"><span data-stu-id="e22ae-159">resource</span></span> | <span data-ttu-id="e22ae-160">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="e22ae-160">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="e22ae-161">Þú ættir að fá `aadToken` svar, sem líkist eftirfarandi dæmi.</span><span class="sxs-lookup"><span data-stu-id="e22ae-161">You should receive an `aadToken` in response, which resembles the following example.</span></span>

    ```json
    {
    "token_type": "Bearer",
    "expires_in": "3599",
    "ext_expires_in": "3599",
    "expires_on": "1610466645",
    "not_before": "1610462745",
    "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
    "access_token": "eyJ0eX...8WQ"
    }
    ```

1. <span data-ttu-id="e22ae-162">Búa skal til JSON-beiðni sem líkist eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="e22ae-162">Formulate a JSON request that resembles the following:</span></span>

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    <span data-ttu-id="e22ae-163">Hvar:</span><span class="sxs-lookup"><span data-stu-id="e22ae-163">Where:</span></span>
    - <span data-ttu-id="e22ae-164">Gildið `client_assertion` verður að vera `aadToken` sem var móttekið í fyrra skrefi.</span><span class="sxs-lookup"><span data-stu-id="e22ae-164">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="e22ae-165">Gildið `context` verður að vera umhverfiskenni þar sem á að nota viðbótina.</span><span class="sxs-lookup"><span data-stu-id="e22ae-165">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="e22ae-166">Stillið öll önnur gildi eins og sýnt er í dæminu.</span><span class="sxs-lookup"><span data-stu-id="e22ae-166">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="e22ae-167">Sendið inn HTTP-beiðni með eftirfarandi eiginleikum:</span><span class="sxs-lookup"><span data-stu-id="e22ae-167">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="e22ae-168">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="e22ae-168">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="e22ae-169">**Aðferð** - `POST`</span><span class="sxs-lookup"><span data-stu-id="e22ae-169">**Method** - `POST`</span></span>
    - <span data-ttu-id="e22ae-170">**HTTP** - Inniheldur API-útgáfu (lykilinn er `Api-Version` og gildið er `1.0`)</span><span class="sxs-lookup"><span data-stu-id="e22ae-170">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="e22ae-171">**Meginefni efnis** - Nota skal JSON-beiðni sem var stofnuð í fyrra skrefi.</span><span class="sxs-lookup"><span data-stu-id="e22ae-171">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="e22ae-172">Þú færð `access_token` í staðinn.</span><span class="sxs-lookup"><span data-stu-id="e22ae-172">You will get an `access_token` in response.</span></span> <span data-ttu-id="e22ae-173">Þetta er það sem þú þarft sem handhafalykill til að kalla í API birgðasýnileikans.</span><span class="sxs-lookup"><span data-stu-id="e22ae-173">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="e22ae-174">Eftirfarandi er dæmi.</span><span class="sxs-lookup"><span data-stu-id="e22ae-174">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a><span data-ttu-id="e22ae-175">Fjarlægja innbótina</span><span class="sxs-lookup"><span data-stu-id="e22ae-175">Uninstall the add-in</span></span>

<span data-ttu-id="e22ae-176">Til að fjarlægja innbótina skal velja **Fjarlægja**.</span><span class="sxs-lookup"><span data-stu-id="e22ae-176">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="e22ae-177">Uppfærðu LCS og innbót birgðasýnileika verður fjarlægð.</span><span class="sxs-lookup"><span data-stu-id="e22ae-177">Refresh LCS and the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="e22ae-178">Fjarlægingarferlið fjarlægir innbótarskráninguna og ræsir einnig vinnslu til að hreinsa öll viðskiptagögn sem vistuð eru í þjónustunni.</span><span class="sxs-lookup"><span data-stu-id="e22ae-178">The uninstall process will remove the add-in registration and also start a job to clean up all of the business data stored in the service.</span></span>

## <a name="inventory-visibility-add-in-public-api"></a><span data-ttu-id="e22ae-179">Almennt API innbótar birgðasýnileika</span><span class="sxs-lookup"><span data-stu-id="e22ae-179">Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="e22ae-180">Almennt REST API innbótar birgðasýnileikans kynnir ýmsar tilteknar endastöðvar samþættingar.</span><span class="sxs-lookup"><span data-stu-id="e22ae-180">The public REST API of the of the Inventory Visibility Add-in presents several specific endpoints of integration.</span></span> <span data-ttu-id="e22ae-181">Það styður þrjár aðalsamskiptaleiðir:</span><span class="sxs-lookup"><span data-stu-id="e22ae-181">It supports three main interaction types:</span></span>

- <span data-ttu-id="e22ae-182">Bókun á lager breytist í innbótina úr ytra kerfi.</span><span class="sxs-lookup"><span data-stu-id="e22ae-182">Posting on-hand changes to the add-in from an external system.</span></span>
- <span data-ttu-id="e22ae-183">Fyrirspurn um núverandi lagermagn úr ytra kerfi.</span><span class="sxs-lookup"><span data-stu-id="e22ae-183">Querying current on-hand quantities from an external system.</span></span>
- <span data-ttu-id="e22ae-184">Sjálfvirk samstilling við lager Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e22ae-184">Automatic synchronization with Supply Chain Management on-hand.</span></span>

<span data-ttu-id="e22ae-185">Sjálfvirka samstillingin er ekki hluti af almennu API en er í staðinn meðhöndluð í bakgrunni fyrir umhverfi sem hafa virkjað innbót birgðasýnileika.</span><span class="sxs-lookup"><span data-stu-id="e22ae-185">The automatic synchronization isn't part of the public API but is instead handled in the background for environments that have enabled the Inventory Visibility Add-in.</span></span>

### <a name="authentication"></a><span data-ttu-id="e22ae-186">Sannvottun</span><span class="sxs-lookup"><span data-stu-id="e22ae-186">Authentication</span></span>

<span data-ttu-id="e22ae-187">Öryggismerki verkvangs er notað til að kalla á innbót birgðasýnileika, þannig að nauðsynlegt er að búa til Azure Active Directory merki með því að nota Azure Active Directory-forritið.</span><span class="sxs-lookup"><span data-stu-id="e22ae-187">The platform security token is used to call the Inventory Visibility Add-in, so you must generate an Azure Active Directory token using your Azure Active Directory application.</span></span>

<span data-ttu-id="e22ae-188">Frekari upplýsingar um hvernig á að sækja öryggismerkið er að finna í [Setja upp innbót birgðasýnileika](#install-add-in).</span><span class="sxs-lookup"><span data-stu-id="e22ae-188">For more information about how to get the security token, see [Install the Inventory Visibility Add-in](#install-add-in).</span></span>

### <a name="configure-the-inventory-visibility-api"></a><span data-ttu-id="e22ae-189">Skilgreina API fyrir sýnileika birgða</span><span class="sxs-lookup"><span data-stu-id="e22ae-189">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="e22ae-190">Áður en þjónustan er notuð þarf að ljúka við skilgreiningarnar sem lýst er í eftirfarandi undirköflum.</span><span class="sxs-lookup"><span data-stu-id="e22ae-190">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="e22ae-191">Skilgreiningin kann að vera mismunandi eftir því hverjar upplýsingar um umhverfið þitt eru.</span><span class="sxs-lookup"><span data-stu-id="e22ae-191">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="e22ae-192">Hún inniheldur fyrst og fremst fjóra hluti:</span><span class="sxs-lookup"><span data-stu-id="e22ae-192">It primarily includes four parts:</span></span>

- [<span data-ttu-id="e22ae-193">Deildaskipting</span><span class="sxs-lookup"><span data-stu-id="e22ae-193">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="e22ae-194">Víddarskilgreiningar</span><span class="sxs-lookup"><span data-stu-id="e22ae-194">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="e22ae-195">Lyklun</span><span class="sxs-lookup"><span data-stu-id="e22ae-195">Indexing</span></span>](#indexing)
- [<span data-ttu-id="e22ae-196">Sérsniðin mæling</span><span class="sxs-lookup"><span data-stu-id="e22ae-196">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="e22ae-197">Deildaskipting</span><span class="sxs-lookup"><span data-stu-id="e22ae-197">Partitioning</span></span>

<span data-ttu-id="e22ae-198">Skipting getur haft umtalsverð áhrif á afköst API fyrir sýnileika birgða.</span><span class="sxs-lookup"><span data-stu-id="e22ae-198">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="e22ae-199">Það er góð hugmynd að skilgreina skema sem leyfir smá flokkun á gögnum en leyfir samtímis gagnlegar gagnafyrirspurnir.</span><span class="sxs-lookup"><span data-stu-id="e22ae-199">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="e22ae-200">`organizationId` (`dataAreaId` í Supply Chain Management) verður alltaf hluti af skiptingunni og birgðasýnileiki er sjálfgefið stilltur á skiptingu eftir víddum sem *Svæði + Staðsetning*.</span><span class="sxs-lookup"><span data-stu-id="e22ae-200">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="e22ae-201">Þetta þýðir að alltaf þurfi að senda fyrirspurn á þjónustuna með þessum víddum sem skilgreindar eru í síunum.</span><span class="sxs-lookup"><span data-stu-id="e22ae-201">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="e22ae-202">*Svæði* og *Staðsetning* eru tvær almennar sjálfgefnar víddir í birgðasýnileika.</span><span class="sxs-lookup"><span data-stu-id="e22ae-202">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="e22ae-203">Í Supply Chain Management eru þessar víddir kallaðar *Svæði* (`InventSiteId`) og *Vöruhús* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="e22ae-203">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="e22ae-204">Víddarskilgreiningar</span><span class="sxs-lookup"><span data-stu-id="e22ae-204">Dimension configurations</span></span>

<span data-ttu-id="e22ae-205">Sýnileiki birgða mun bjóða upp á lista yfir almennar sjálfgefnar víddir til að virkja samþættingu margra upprunakerfa.</span><span class="sxs-lookup"><span data-stu-id="e22ae-205">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="e22ae-206">Í eftirfarandi töflu er listi yfir birgðavíddir sem verða sjálfgefin víddarheiti í birgðasýnileika.</span><span class="sxs-lookup"><span data-stu-id="e22ae-206">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="e22ae-207">Tegund víddar</span><span class="sxs-lookup"><span data-stu-id="e22ae-207">Dimension type</span></span> | <span data-ttu-id="e22ae-208">Heiti víddar</span><span class="sxs-lookup"><span data-stu-id="e22ae-208">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="e22ae-209">Afurð</span><span class="sxs-lookup"><span data-stu-id="e22ae-209">Product</span></span> | `ColorId` |
| <span data-ttu-id="e22ae-210">Afurð</span><span class="sxs-lookup"><span data-stu-id="e22ae-210">Product</span></span> | `SizeId` |
| <span data-ttu-id="e22ae-211">Afurð</span><span class="sxs-lookup"><span data-stu-id="e22ae-211">Product</span></span> | `StyleId` |
| <span data-ttu-id="e22ae-212">Afurð</span><span class="sxs-lookup"><span data-stu-id="e22ae-212">Product</span></span> | `ConfigId` |
| <span data-ttu-id="e22ae-213">Rakning</span><span class="sxs-lookup"><span data-stu-id="e22ae-213">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="e22ae-214">Rakning</span><span class="sxs-lookup"><span data-stu-id="e22ae-214">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="e22ae-215">Staður</span><span class="sxs-lookup"><span data-stu-id="e22ae-215">Location</span></span> | `LocationId` |
| <span data-ttu-id="e22ae-216">Staður</span><span class="sxs-lookup"><span data-stu-id="e22ae-216">Location</span></span> | `SiteId` |
| <span data-ttu-id="e22ae-217">Birgðastaða</span><span class="sxs-lookup"><span data-stu-id="e22ae-217">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="e22ae-218">Miðast við vöruhús</span><span class="sxs-lookup"><span data-stu-id="e22ae-218">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="e22ae-219">Miðast við vöruhús</span><span class="sxs-lookup"><span data-stu-id="e22ae-219">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="e22ae-220">Miðast við vöruhús</span><span class="sxs-lookup"><span data-stu-id="e22ae-220">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="e22ae-221">Gerð víddar sem er skráð í fyrri töflu er aðeins til viðmiðunar.</span><span class="sxs-lookup"><span data-stu-id="e22ae-221">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="e22ae-222">Ekki þarf að skilgreina gerð víddar í birgðasýnileika.</span><span class="sxs-lookup"><span data-stu-id="e22ae-222">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="e22ae-223">Ef sérstillt vídd er til staðar og þarf að flytjast yfir í sjálfgefið gildi þegar birgðasýnileiki notar hana, er hægt að skilgreina heiti **Sérsniðinnar víddar** í birgðasýnileika.</span><span class="sxs-lookup"><span data-stu-id="e22ae-223">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="e22ae-224">Ytri kerfi fá aðgang að sýnileika birgða í gegnum RESTful API sem bjóða upp á lagerupplýsingar um uppgefin víddarsett sem senda á fyrirspurn um.</span><span class="sxs-lookup"><span data-stu-id="e22ae-224">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="e22ae-225">Fyrir samþættinguna, gerir birgðasýnileiki þér kleift að stilla *ytri gagnagjafa rásar* og upprunavíddina við *markvíddina* í birgðasýnileika.</span><span class="sxs-lookup"><span data-stu-id="e22ae-225">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="e22ae-226">Markvíddirnar ættu að vera eitt af eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="e22ae-226">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="e22ae-227">Sjálfgefnar víddir í birgðasýnileika</span><span class="sxs-lookup"><span data-stu-id="e22ae-227">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="e22ae-228">Sérsniðnar víddir</span><span class="sxs-lookup"><span data-stu-id="e22ae-228">Custom dimensions</span></span>

<span data-ttu-id="e22ae-229">Tilgangurinn með víddarskilgreiningunni er sá að staðla samþættingu margra kerfa fyrir fyrirspurnina á víddum og bókunartilvikinu með víddum.</span><span class="sxs-lookup"><span data-stu-id="e22ae-229">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="e22ae-230">Lyklun</span><span class="sxs-lookup"><span data-stu-id="e22ae-230">Indexing</span></span>

<span data-ttu-id="e22ae-231">Oftast verður fyrirspurn um birgðir ekki bara um hæsta stig „samtölunnar“, heldur viltu hugsanlega sjá niðurstöður teknar saman eftir birgðavíddum.</span><span class="sxs-lookup"><span data-stu-id="e22ae-231">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="e22ae-232">Sýnileiki birgða veitir sveigjanleika með því að gera þér kleift að setja upp vísa sem byggja á víddinni eða samsetningu víddanna.</span><span class="sxs-lookup"><span data-stu-id="e22ae-232">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="e22ae-233">Sem stendur er aðeins hægt að skilgreina vísa fyrir fimm að hámarki.</span><span class="sxs-lookup"><span data-stu-id="e22ae-233">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="e22ae-234">Þú þarft að íhuga vandlega hvaða vídd eða víddarsamsetningu þú notar fyrir innleiðingu til að tryggja að hún uppfylli þarfir fyrirtækisins þíns.</span><span class="sxs-lookup"><span data-stu-id="e22ae-234">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="e22ae-235">Til dæmis, ef ætlunin er að senda fyrirspurn um afurðir eins og hér segir:</span><span class="sxs-lookup"><span data-stu-id="e22ae-235">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="e22ae-236">Spyrjast fyrir um samanlagðar afurðir á lager af víddunum *Litur* og *Stærð*.</span><span class="sxs-lookup"><span data-stu-id="e22ae-236">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="e22ae-237">Í sumum tilfellum er bara ætlunin að spyrjast fyrir um afurðina í heild sinni.</span><span class="sxs-lookup"><span data-stu-id="e22ae-237">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="e22ae-238">Þú hefðir þá tvær vísanir sem eru skilgreindar á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="e22ae-238">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="e22ae-239">Tómi hornklofinn mun safna saman eftir auðkenni afurðar innan skiptingar.</span><span class="sxs-lookup"><span data-stu-id="e22ae-239">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="e22ae-240">Vísunin skilgreinir hvernig hægt er að flokka niðurstöðurnar samkvæmt fyrirspurnarstillingunni `groupBy`.</span><span class="sxs-lookup"><span data-stu-id="e22ae-240">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="e22ae-241">Í þessu tilfelli, ef þú skilgreinir ekki eitthvað `groupBy` gildi, færðu samtölur eftir `productid`.</span><span class="sxs-lookup"><span data-stu-id="e22ae-241">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="e22ae-242">Annars, ef skilgreint er `groupBy` sem `groupBy=ColorId&groupBy=SizeId` færðu margar línur til baka, sem byggja á mismunandi samsetningu á lit og stærð í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="e22ae-242">Otherwise if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="e22ae-243">Hægt er að setja skilyrði fyrirspurnar í meginmál beiðninnar.</span><span class="sxs-lookup"><span data-stu-id="e22ae-243">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="e22ae-244">Hér er dæmi um fyrirspurn um afurðina með lita- og stærðarsamsetningu.</span><span class="sxs-lookup"><span data-stu-id="e22ae-244">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="custom-measurement"></a><span data-ttu-id="e22ae-245">Sérsniðin mæling</span><span class="sxs-lookup"><span data-stu-id="e22ae-245">Custom measurement</span></span>

<span data-ttu-id="e22ae-246">Sjálfgefið mælingarmagn er tengt við Supply Chain Management, en þú gætir hinsvegar viljað hafa magn sem er gert úr samsetningu sjálfgefinna mælinga.</span><span class="sxs-lookup"><span data-stu-id="e22ae-246">The default measurement quantities are linked to Supply Chain Management, however you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="e22ae-247">Til að gera þetta er hægt að hafa skilgreiningu á sérsniðnu magni, sem verður bætt við úttak lagerfyrirspurnar.</span><span class="sxs-lookup"><span data-stu-id="e22ae-247">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="e22ae-248">Virknin gerir einfaldlega kleift að skilgreina safn mælinga sem verður bætt við og/eða safn mælinga sem verður dregið frá til að búa til sérsniðnu mælinguna.</span><span class="sxs-lookup"><span data-stu-id="e22ae-248">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="e22ae-249">Til dæmis með eftirfarandi fyrirspurnarskilyrði muntu skilgreina magn sérsniðinnar mælingar sem `MyCustomAvailableforReservation` sem tilheyrandi notkunarkerfi notar.</span><span class="sxs-lookup"><span data-stu-id="e22ae-249">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| <span data-ttu-id="e22ae-250">Notkunarkerfi</span><span class="sxs-lookup"><span data-stu-id="e22ae-250">Consumption system</span></span> | <span data-ttu-id="e22ae-251">Reiknaðar mælingar</span><span class="sxs-lookup"><span data-stu-id="e22ae-251">Calculated measurers</span></span> | <span data-ttu-id="e22ae-252">Gagnaveita</span><span class="sxs-lookup"><span data-stu-id="e22ae-252">Data source</span></span> | <span data-ttu-id="e22ae-253">Umbreytir</span><span class="sxs-lookup"><span data-stu-id="e22ae-253">Modifier</span></span> | <span data-ttu-id="e22ae-254">Útreikningsgerð umbreytis</span><span class="sxs-lookup"><span data-stu-id="e22ae-254">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="e22ae-255">samlagning</span><span class="sxs-lookup"><span data-stu-id="e22ae-255">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="e22ae-256">samlagning</span><span class="sxs-lookup"><span data-stu-id="e22ae-256">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="e22ae-257">Frádráttur</span><span class="sxs-lookup"><span data-stu-id="e22ae-257">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="e22ae-258">samlagning</span><span class="sxs-lookup"><span data-stu-id="e22ae-258">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="e22ae-259">Frádráttur</span><span class="sxs-lookup"><span data-stu-id="e22ae-259">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="e22ae-260">samlagning</span><span class="sxs-lookup"><span data-stu-id="e22ae-260">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="e22ae-261">samlagning</span><span class="sxs-lookup"><span data-stu-id="e22ae-261">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="e22ae-262">Frádráttur</span><span class="sxs-lookup"><span data-stu-id="e22ae-262">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="e22ae-263">Frádráttur</span><span class="sxs-lookup"><span data-stu-id="e22ae-263">Subtraction</span></span> |

<span data-ttu-id="e22ae-264">Þannig mun fyrirspurnin um sérsniðna magnmælingu skila eftirfarandi úttaki.</span><span class="sxs-lookup"><span data-stu-id="e22ae-264">With that, the query on the custom measurement quantity will return the following output.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="e22ae-265">`MyCustomAvailableforReservation` úttakið byggir á útreikningsstillingu í sérsniðnum mælingum sem:</span><span class="sxs-lookup"><span data-stu-id="e22ae-265">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="e22ae-266">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="e22ae-266">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="e22ae-267">Bókun lagerbreytinga</span><span class="sxs-lookup"><span data-stu-id="e22ae-267">Posting on-hand changes</span></span>

<span data-ttu-id="e22ae-268">Nákvæm vefslóð sem tilvikið verður bókað á mun ráðast af landsvæði notanda.</span><span class="sxs-lookup"><span data-stu-id="e22ae-268">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="e22ae-269">Hún verður á forminu:</span><span class="sxs-lookup"><span data-stu-id="e22ae-269">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="e22ae-270">Þegar hún er vottuð verður þessi vefslóð notuð ásamt HTTP `POST`-aðferðinni til að senda breytingatilvik lagers á þjónustuna.</span><span class="sxs-lookup"><span data-stu-id="e22ae-270">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="e22ae-271">Sérstakur haus er notaður til að eiga samskipti við Dynamics 365 þjónustuna í gegnum HTTP-beiðnir, þar sem umhverfiskennið er tilgreint fyrir tilvik Supply Chain Management sem gögnin eru tengd við.</span><span class="sxs-lookup"><span data-stu-id="e22ae-271">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="e22ae-272">Dæmi:</span><span class="sxs-lookup"><span data-stu-id="e22ae-272">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="e22ae-273">Fyrirspurn um bókun lagerbreytinga, dæmi 1</span><span class="sxs-lookup"><span data-stu-id="e22ae-273">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="e22ae-274">Þetta dæmi sýnir aðstæður þar sem víddarskilgreining verður sett upp í Power Apps.</span><span class="sxs-lookup"><span data-stu-id="e22ae-274">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="e22ae-275">Notaðu eftirfarandi fyrirspurn til að skilgreina víddarvörpunina í Power Apps:</span><span class="sxs-lookup"><span data-stu-id="e22ae-275">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="e22ae-276">Nú er hægt að tilgreina `dimensionDataSource` og nota sérsniðnar víddir í fyrirspurnum.</span><span class="sxs-lookup"><span data-stu-id="e22ae-276">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="e22ae-277">Kerfið mun umbreyta sérsniðnum víddum í grunnvíddir.</span><span class="sxs-lookup"><span data-stu-id="e22ae-277">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="e22ae-278">Fyrirspurn um bókun lagerbreytinga, dæmi 2</span><span class="sxs-lookup"><span data-stu-id="e22ae-278">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="e22ae-279">Þetta dæmi sýnir aðstæður þar sem engar varpanir eru settar upp fyrir víddarskilgreininguna í Power Apps, þannig að bókunin ætti einnig að nota grunnvíddirnar.</span><span class="sxs-lookup"><span data-stu-id="e22ae-279">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="e22ae-280">Allar víddir verða að vera grunnvíddir þegar reiturinn `dimensionDataSource` er núll, tómur eða með stafabil.</span><span class="sxs-lookup"><span data-stu-id="e22ae-280">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a><span data-ttu-id="e22ae-281">Eiginleikar JSON-skjalareits</span><span class="sxs-lookup"><span data-stu-id="e22ae-281">JSON document field properties</span></span>

<span data-ttu-id="e22ae-282">Reitirnir úr dæmum JSON-fyrirspurna sem boðið var upp á hér á undan eru með eiginleikana sem gefnir eru upp í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="e22ae-282">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="e22ae-283">Kenni svæðis</span><span class="sxs-lookup"><span data-stu-id="e22ae-283">Field ID</span></span> | <span data-ttu-id="e22ae-284">lýsing</span><span class="sxs-lookup"><span data-stu-id="e22ae-284">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="e22ae-285">Einkvæmt auðkenni fyrir tiltekið breytingartilvik.</span><span class="sxs-lookup"><span data-stu-id="e22ae-285">A unique ID for the specific change event.</span></span> <span data-ttu-id="e22ae-286">Þetta auðkenni er notað til að tryggja að ef samskipti við þjónustuna klikka við bókun, myndi endursending á tilvikinu ekki leiða til þess að sama tilvikið yrði talið tvisvar í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="e22ae-286">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="e22ae-287">Kennimerki fyrirtækisins sem tengt er við tilvikið.</span><span class="sxs-lookup"><span data-stu-id="e22ae-287">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="e22ae-288">Þetta varpar í fyrirtækiskenni eða gagnasvæðiskenni Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e22ae-288">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="e22ae-289">Kennimerki afurðar sem um ræðir.</span><span class="sxs-lookup"><span data-stu-id="e22ae-289">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="e22ae-290">Magnið sem á lager þarf að breytast um.</span><span class="sxs-lookup"><span data-stu-id="e22ae-290">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="e22ae-291">Ef til dæmis 10 nýjum beyglum var bætt við hilluna, þá væri þetta gildi 10.</span><span class="sxs-lookup"><span data-stu-id="e22ae-291">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="e22ae-292">Ef 3 beyglur yrðu síðan teknar úr hillunni eða seldar, þá væri þetta gildi -3.</span><span class="sxs-lookup"><span data-stu-id="e22ae-292">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="e22ae-293">Gagnagjafi víddanna sem notaðar eru í breytingartilviki og fyrirspurn bókunar.</span><span class="sxs-lookup"><span data-stu-id="e22ae-293">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="e22ae-294">Ef gagnagjafi er tilgreindur er hægt að nota sérstilltar víddir úr tilgreindum gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="e22ae-294">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="e22ae-295">Með víddaskilgreiningunni getur birgðasýnileiki varpað sérstilltu víddunum í almennu sjálfgefnu víddirnar.</span><span class="sxs-lookup"><span data-stu-id="e22ae-295">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="e22ae-296">Ef `dimensionDataSource` er ekki tilgreint er aðeins hægt að nota almennar sjálfgefnar víddir í fyrirspurnunum.</span><span class="sxs-lookup"><span data-stu-id="e22ae-296">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="e22ae-297">Gagnvirkur poki af lykla-/gildispörum.</span><span class="sxs-lookup"><span data-stu-id="e22ae-297">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="e22ae-298">Þetta mun varpa í sumar víddirnar í Supply Chain Management, en einnig er hægt að bæta við sérstilltum víddum (eins og *Uppruni*) sem kann að gefa til kynna ef tilvikið kom frá Supply Chain Management eða ytra kerfi.</span><span class="sxs-lookup"><span data-stu-id="e22ae-298">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="e22ae-299">Spyrjast fyrir um núverandi lagerbirgðir</span><span class="sxs-lookup"><span data-stu-id="e22ae-299">Querying current on-hand</span></span>

<span data-ttu-id="e22ae-300">Endastöðin til að spyrjast fyrir um núverandi lagerbirgðir verður með svipaða vefslóð:</span><span class="sxs-lookup"><span data-stu-id="e22ae-300">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="e22ae-301">Send verður fyrirspurn á hana með HTTP `POST`-aðferðinni.</span><span class="sxs-lookup"><span data-stu-id="e22ae-301">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="e22ae-302">Núverandi lagerfyrirspurn, dæmi 1</span><span class="sxs-lookup"><span data-stu-id="e22ae-302">Current on-hand query example 1</span></span>

<span data-ttu-id="e22ae-303">Þetta dæmi sýnir aðstæður þar sem búið er að ljúka víddarskilgreiningunni í Power Apps.</span><span class="sxs-lookup"><span data-stu-id="e22ae-303">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="e22ae-304">Notaðu eftirfarandi fyrirspurn til að skilgreina víddarvörpunina í Power Apps:</span><span class="sxs-lookup"><span data-stu-id="e22ae-304">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="e22ae-305">Nú er hægt að tilgreina `dimensionDataSource` og nota sérsniðnar víddir í fyrirspurnum.</span><span class="sxs-lookup"><span data-stu-id="e22ae-305">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="e22ae-306">Kerfið mun umbreyta sérsniðnum víddum í grunnvíddir.</span><span class="sxs-lookup"><span data-stu-id="e22ae-306">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="e22ae-307">Hægt er að tilgreina `DimensionDataSource` í `filters` og tilgreina sérsniðnar víddir bæði í `filters` og `groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="e22ae-307">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="e22ae-308">Kerfið mun umbreyta sérsniðnum víddum í grunnvíddir.</span><span class="sxs-lookup"><span data-stu-id="e22ae-308">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="e22ae-309">Núverandi lagerfyrirspurn, dæmi 2</span><span class="sxs-lookup"><span data-stu-id="e22ae-309">Current on-hand query example 2</span></span>

<span data-ttu-id="e22ae-310">Þetta dæmi sýnir aðstæður þar sem engar varpanir eru settar upp fyrir víddarskilgreininguna í Power Apps, þannig að bókunin ætti einnig að nota grunnvíddirnar.</span><span class="sxs-lookup"><span data-stu-id="e22ae-310">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="e22ae-311">Allar víddir verða að vera grunnvíddir þegar reiturinn `dimensionDataSource`, undir `filters` er núll, tómur eða með stafabil.</span><span class="sxs-lookup"><span data-stu-id="e22ae-311">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a><span data-ttu-id="e22ae-312">Dæmi um niðurstöður</span><span class="sxs-lookup"><span data-stu-id="e22ae-312">Example return result</span></span>

<span data-ttu-id="e22ae-313">Fyrirspurnirnar sem sýndar voru í fyrra dæminu gætu skilað niðurstöðum sem þessari.</span><span class="sxs-lookup"><span data-stu-id="e22ae-313">The queries shown in the previous examples could return a result like this.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="e22ae-314">Athugið að magnreitirnir eru skipulagðir sem orðabók yfir mælingar og tengd gildi þeirra.</span><span class="sxs-lookup"><span data-stu-id="e22ae-314">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>
