---
title: Uppfæra í altæka aðila- og aðsetursbókarlíkanið
description: Í þessu efnisatriði er lýst hvernig á að uppfæra gögn tvöfaldrar skráningar í aðilalíkanið og líkan altækrar aðsetursbókar.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 90ddbe704ab21d62752b581a813601e8986c2103
ms.sourcegitcommit: 180548e3c10459776cf199989d3753e0c1555912
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/28/2021
ms.locfileid: "6112674"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="bfba6-103">Uppfæra í altæka aðila- og aðsetursbókarlíkanið</span><span class="sxs-lookup"><span data-stu-id="bfba6-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="bfba6-104">[Microsoft Azure Data Factory sniðmát](https://aka.ms/dual-write-gab-adf) hjálpar til við að uppfæra fyrirliggjandi töflugögn **Lykils**, **Tengiliðar** og **Lánardrottins** í tvöfaldri skráningu í aðilalíkanið og líkan altækrar aðsetursbókar.</span><span class="sxs-lookup"><span data-stu-id="bfba6-104">The [Microsoft Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="bfba6-105">Sniðmátið afstemmir gögnin úr bæði Finance and Operations-forritum og forritum viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="bfba6-105">The template reconciles the data from both finance and operations apps and customer engagement applications.</span></span> <span data-ttu-id="bfba6-106">Undir lok ferlisins verða reitirnir **Aðili** og **Tengiliður** fyrir **Aðilafærslur** búnir til og tengdir við færslur **Lykils**, **Tengiliðar** og **Lánardrottins** í forritum viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="bfba6-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="bfba6-107">.csv skrá (`FONewParty.csv`) er mynduð til að stofna nýjar **Aðilafærslur** í Finance and Operations-forritinu.</span><span class="sxs-lookup"><span data-stu-id="bfba6-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the finance and operations app.</span></span> <span data-ttu-id="bfba6-108">Í þessu efnisatriði er að finna leiðbeiningar um notkun Data Factory-sniðmáts og uppfærslu gagnanna.</span><span class="sxs-lookup"><span data-stu-id="bfba6-108">This topic provides instructions about how to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="bfba6-109">Ef engar sérstillingar eru til staðar er hægt að nota sniðmátið eins og það er.</span><span class="sxs-lookup"><span data-stu-id="bfba6-109">If you don’t have any customizations, you can use the template as is.</span></span> <span data-ttu-id="bfba6-110">Ef sérstillingar eru fyrir hendi fyrir **Lykil**, **Tengilið** og **Lánardrottin** þarf að breyta sniðmátinu samkvæmt eftirfarandi leiðbeiningum.</span><span class="sxs-lookup"><span data-stu-id="bfba6-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!NOTE]
> <span data-ttu-id="bfba6-111">Sniðmátið uppfærir aðeins **Aðili** gögn.</span><span class="sxs-lookup"><span data-stu-id="bfba6-111">The template only upgrades the **Party** data.</span></span> <span data-ttu-id="bfba6-112">Í síðari útgáfu verða póstföng og rafræn heimilisföng höfð með.</span><span class="sxs-lookup"><span data-stu-id="bfba6-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bfba6-113">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="bfba6-113">Prerequisites</span></span>

<span data-ttu-id="bfba6-114">Eftirfarandi forsendur eru nauðsynlegar til að uppfæra í altæka aðila- og aðsetursbókarlíkanið:</span><span class="sxs-lookup"><span data-stu-id="bfba6-114">The following prerequisites are required to upgrade to the party and global address book model:</span></span>

+ [<span data-ttu-id="bfba6-115">Azure-áskrift</span><span class="sxs-lookup"><span data-stu-id="bfba6-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="bfba6-116">Aðgangur að sniðmáti</span><span class="sxs-lookup"><span data-stu-id="bfba6-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="bfba6-117">Þú verður að vera núverandi viðskiptavinur tvöfaldrar skráningar.</span><span class="sxs-lookup"><span data-stu-id="bfba6-117">You must be an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="bfba6-118">Uppfærsla undirbúin</span><span class="sxs-lookup"><span data-stu-id="bfba6-118">Prepare for the upgrade</span></span>
<span data-ttu-id="bfba6-119">Eftirfarandi aðgerðir eru nauðsynlegar til að undirbúa uppfærsluna:</span><span class="sxs-lookup"><span data-stu-id="bfba6-119">The following activities are needed to prepare for the upgrade:</span></span>

+ <span data-ttu-id="bfba6-120">**Full samstilling**: Bæði umhverfin eru í fullri samstillingarstöðu fyrir **Lykil (viðskiptavinur)**, **Tengilið** og **Lánardrottin**.</span><span class="sxs-lookup"><span data-stu-id="bfba6-120">**Fully synced**: Both environments are in a fully synced state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="bfba6-121">**Samþættingarlyklar**: Töflur **Lykils (viðskiptavinur)**, **Tengiliðar** og **Lánardrottins** í forritum viðskiptavinar nota tilbúna samþættingarlykla sem fylgja með.</span><span class="sxs-lookup"><span data-stu-id="bfba6-121">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="bfba6-122">Ef samþættingarlyklarnir voru sérstilltir þarf að sérstilla sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="bfba6-122">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="bfba6-123">**Aðilanúmer**: Allar færslur **Lykils (viðskiptavinar)**, **Tengiliðar** og **Lánardrottins** sem verða uppfærðar eru með númer **Aðila**.</span><span class="sxs-lookup"><span data-stu-id="bfba6-123">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="bfba6-124">Færslur án númers **Aðila** verða hunsaðar.</span><span class="sxs-lookup"><span data-stu-id="bfba6-124">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="bfba6-125">Ef uppfæra á þær færslur skal bæta númeri **Aðila** við þær áður en uppfærsluferlið er sett í gang.</span><span class="sxs-lookup"><span data-stu-id="bfba6-125">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="bfba6-126">**Stöðvun kerfis**: Í uppfærsluferlinu þarf að slökkva á nettengingu fyrir bæði Finance and Operations umhverfi  og umhverfi viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="bfba6-126">**System outage**: During the upgrade process, you will have to take both the finance and operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="bfba6-127">**Skyndimynd**: Takið skyndimyndir af bæði Finance and Operations-forritum og forritum viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="bfba6-127">**Snapshot**: Take snapshots of both the finance and operations apps and customer engagement apps.</span></span> <span data-ttu-id="bfba6-128">Notið skyndimyndirnar til að endurheimta fyrri stöðu ef á þarf að halda.</span><span class="sxs-lookup"><span data-stu-id="bfba6-128">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="bfba6-129">Nýting</span><span class="sxs-lookup"><span data-stu-id="bfba6-129">Deployment</span></span>

1. <span data-ttu-id="bfba6-130">Sækið sniðmátið úr [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span><span class="sxs-lookup"><span data-stu-id="bfba6-130">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="bfba6-131">Skráðu þig inn á [Microsoft Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="bfba6-131">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="bfba6-132">Stofnið [tilfangaflokk](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span><span class="sxs-lookup"><span data-stu-id="bfba6-132">Create a [resource group](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="bfba6-133">Búið til [geymslureikning](/azure/storage/common/storage-account-create?tabs=azure-portal) í tilfangaflokknum sem var stofnaður.</span><span class="sxs-lookup"><span data-stu-id="bfba6-133">Create a [storage account](/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="bfba6-134">Stofnið [gagnasmiðju](/azure/data-factory/quickstart-create-data-factory-portal) í ofangreindum tilfangaflokki sem var stofnaður.</span><span class="sxs-lookup"><span data-stu-id="bfba6-134">Create a [data factory](/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="bfba6-135">Opnið gagnasmiðjuna og veljið reitinn **Stýra og fylgjast með**.</span><span class="sxs-lookup"><span data-stu-id="bfba6-135">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="bfba6-136">Í flipanum **Stjórna** skal velja **ARM-sniðmát**.</span><span class="sxs-lookup"><span data-stu-id="bfba6-136">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="bfba6-137">Veljið **Flytja inn ARM-sniðmát** til að flytja inn sniðmátið **Aðili**.</span><span class="sxs-lookup"><span data-stu-id="bfba6-137">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="bfba6-138">Flytjið sniðmátið inn í gagnasmiðjuna.</span><span class="sxs-lookup"><span data-stu-id="bfba6-138">Import the template into the data factory.</span></span> <span data-ttu-id="bfba6-139">Færið inn eftirfarandi gildi fyrir **Upplýsingar um verk** og **Upplýsingar um tilvik**.</span><span class="sxs-lookup"><span data-stu-id="bfba6-139">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="bfba6-140">Svæði</span><span class="sxs-lookup"><span data-stu-id="bfba6-140">Field</span></span> | <span data-ttu-id="bfba6-141">Virði</span><span class="sxs-lookup"><span data-stu-id="bfba6-141">Value</span></span>
    ---|---
    <span data-ttu-id="bfba6-142">Áskrift</span><span class="sxs-lookup"><span data-stu-id="bfba6-142">Subscription</span></span> | <span data-ttu-id="bfba6-143">Azure-áskrift</span><span class="sxs-lookup"><span data-stu-id="bfba6-143">Azure subscription</span></span>
    <span data-ttu-id="bfba6-144">Tilfangaflokkur</span><span class="sxs-lookup"><span data-stu-id="bfba6-144">Resource group</span></span> | <span data-ttu-id="bfba6-145">Gefið upp sama tilfang þar sem geymslureikningur er stofnaður fyrir.</span><span class="sxs-lookup"><span data-stu-id="bfba6-145">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="bfba6-146">Svæði</span><span class="sxs-lookup"><span data-stu-id="bfba6-146">Region</span></span> | <span data-ttu-id="bfba6-147">Tilgreina svæði.</span><span class="sxs-lookup"><span data-stu-id="bfba6-147">Specify region.</span></span>
    <span data-ttu-id="bfba6-148">Heiti verksmiðju</span><span class="sxs-lookup"><span data-stu-id="bfba6-148">Factory Name</span></span> | <span data-ttu-id="bfba6-149">Tilgreina heiti verksmiðju.</span><span class="sxs-lookup"><span data-stu-id="bfba6-149">Specify factory name.</span></span>
    <span data-ttu-id="bfba6-150">FO Linked Service_service Principal Key</span><span class="sxs-lookup"><span data-stu-id="bfba6-150">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="bfba6-151">Tilgreinið forritslykilinn.</span><span class="sxs-lookup"><span data-stu-id="bfba6-151">Specify the application's key.</span></span>
    <span data-ttu-id="bfba6-152">Strengur Azure Blob Storage_connection</span><span class="sxs-lookup"><span data-stu-id="bfba6-152">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="bfba6-153">Tengingarstrengur Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="bfba6-153">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="bfba6-154">Dynamics Crm Linked Service_password</span><span class="sxs-lookup"><span data-stu-id="bfba6-154">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="bfba6-155">Aðgangsorðið fyrir notandareikninginn sem tilgreindur var sem notandanafnið.</span><span class="sxs-lookup"><span data-stu-id="bfba6-155">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="bfba6-156">FO Linked Service_properties_type Properties_url</span><span class="sxs-lookup"><span data-stu-id="bfba6-156">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="bfba6-157">FO Linked Service_properties_type Properties_tenant</span><span class="sxs-lookup"><span data-stu-id="bfba6-157">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="bfba6-158">Tilgreinið upplýsingar um leigjanda (heiti léns eða leigjandakenni) sem forritið heyrir undir.</span><span class="sxs-lookup"><span data-stu-id="bfba6-158">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="bfba6-159">FO Linked Service_properties_type Properties_aad Resource Id</span><span class="sxs-lookup"><span data-stu-id="bfba6-159">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="bfba6-160">FO Linked Service_properties_type Properties_service Principal Id</span><span class="sxs-lookup"><span data-stu-id="bfba6-160">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="bfba6-161">Tilgreinið biðlarakenni forritsins.</span><span class="sxs-lookup"><span data-stu-id="bfba6-161">Specify the application's client ID.</span></span>
    <span data-ttu-id="bfba6-162">Dynamics Crm Linked Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="bfba6-162">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="bfba6-163">Notandanafnið sem á að tengja Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="bfba6-163">The username to connect to Dynamics 365.</span></span>

    <span data-ttu-id="bfba6-164">Vísað er í eftirfarandi efnisatriði fyrir frekari upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="bfba6-164">For additional information, refer to the following topics:</span></span> 
    
    - [<span data-ttu-id="bfba6-165">Úthluta sniðmáti forðastjóra á handvirkan hátt fyrir hvert umhverfi</span><span class="sxs-lookup"><span data-stu-id="bfba6-165">Manually promote a Resource Manager template for each environment</span></span>](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [<span data-ttu-id="bfba6-166">Tengdir þjónustueiginleikar</span><span class="sxs-lookup"><span data-stu-id="bfba6-166">Linked service properties</span></span>](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [<span data-ttu-id="bfba6-167">Afrita gögn með Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="bfba6-167">Copy data using Azure Data Factory</span></span>](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. <span data-ttu-id="bfba6-168">Eftir uppsetningu skal staðfesta gagnasöfnin, gagnaflæðið og tengda þjónustu gagnasmiðjunnar.</span><span class="sxs-lookup"><span data-stu-id="bfba6-168">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![Gagnasafn, gagnaflæði og tengd þjónusta](media/data-factory-validate.png)

11. <span data-ttu-id="bfba6-170">Farið í **Stjórna**.</span><span class="sxs-lookup"><span data-stu-id="bfba6-170">Navigate to **Manage**.</span></span> <span data-ttu-id="bfba6-171">Undir **Tengingar** skal velja **Tengd þjónusta**.</span><span class="sxs-lookup"><span data-stu-id="bfba6-171">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="bfba6-172">Veljið **DynamicsCrmLinkedService**.</span><span class="sxs-lookup"><span data-stu-id="bfba6-172">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="bfba6-173">Á skjámyndinni **Breyta tengdri þjónustu (Dynamics CRM)** skal færa inn eftirfarandi gildi.</span><span class="sxs-lookup"><span data-stu-id="bfba6-173">In the **Edit linked service (Dynamics CRM)** form, enter the following values.</span></span>

    <span data-ttu-id="bfba6-174">Svæði</span><span class="sxs-lookup"><span data-stu-id="bfba6-174">Field</span></span> | <span data-ttu-id="bfba6-175">Virði</span><span class="sxs-lookup"><span data-stu-id="bfba6-175">Value</span></span>
    ---|---
    <span data-ttu-id="bfba6-176">Nafn</span><span class="sxs-lookup"><span data-stu-id="bfba6-176">Name</span></span> | <span data-ttu-id="bfba6-177">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="bfba6-177">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="bfba6-178">lýsing</span><span class="sxs-lookup"><span data-stu-id="bfba6-178">Description</span></span> | <span data-ttu-id="bfba6-179">Tengdar þjónustur til að tengjast við CRM-tilvik til að sækja gögn eininga</span><span class="sxs-lookup"><span data-stu-id="bfba6-179">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="bfba6-180">Tengjast með keyrslutíma samþættingar</span><span class="sxs-lookup"><span data-stu-id="bfba6-180">Connect via integration runtime</span></span> | <span data-ttu-id="bfba6-181">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="bfba6-181">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="bfba6-182">Uppsetningargerð</span><span class="sxs-lookup"><span data-stu-id="bfba6-182">Deployment type</span></span> | <span data-ttu-id="bfba6-183">Nettenging</span><span class="sxs-lookup"><span data-stu-id="bfba6-183">Online</span></span>
    <span data-ttu-id="bfba6-184">Uri þjónustu</span><span class="sxs-lookup"><span data-stu-id="bfba6-184">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="bfba6-185">Sannvottunargerð</span><span class="sxs-lookup"><span data-stu-id="bfba6-185">Authentication type</span></span> | <span data-ttu-id="bfba6-186">Office365</span><span class="sxs-lookup"><span data-stu-id="bfba6-186">Office365</span></span>
    <span data-ttu-id="bfba6-187">Notandanafn</span><span class="sxs-lookup"><span data-stu-id="bfba6-187">User name</span></span> |
    <span data-ttu-id="bfba6-188">Aðgangsorð eða Azure-lyklageymsla</span><span class="sxs-lookup"><span data-stu-id="bfba6-188">Password or Azure Key Vault</span></span> | <span data-ttu-id="bfba6-189">Aðgangsorð</span><span class="sxs-lookup"><span data-stu-id="bfba6-189">Password</span></span>
    <span data-ttu-id="bfba6-190">Aðgangsorð</span><span class="sxs-lookup"><span data-stu-id="bfba6-190">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="bfba6-191">Keyra sniðmátið</span><span class="sxs-lookup"><span data-stu-id="bfba6-191">Run the template</span></span>

1. <span data-ttu-id="bfba6-192">Stöðvið eftirfarandi tvöfalda skráningu vörpunar **Lykils**, **Tengiliðar** og **Lánardrottins** með Finance and Operations-forritinu.</span><span class="sxs-lookup"><span data-stu-id="bfba6-192">Stop the following **Account**, **Contact**, and **Vendor** dual-write maps using the Finance and Operations app.</span></span>

    + <span data-ttu-id="bfba6-193">Viðskiptavinir V3 (lyklar)</span><span class="sxs-lookup"><span data-stu-id="bfba6-193">Customers V3(accounts)</span></span>
    + <span data-ttu-id="bfba6-194">Viðskiptavinir V3 (tengiliðir)</span><span class="sxs-lookup"><span data-stu-id="bfba6-194">Customers V3(contacts)</span></span>
    + <span data-ttu-id="bfba6-195">CDS Tengiliðir V2 (tengiliðir)</span><span class="sxs-lookup"><span data-stu-id="bfba6-195">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="bfba6-196">CDS Tengiliðir V2 (tengiliðir)</span><span class="sxs-lookup"><span data-stu-id="bfba6-196">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="bfba6-197">Lánardrottinn V2 (msdyn_vendors)</span><span class="sxs-lookup"><span data-stu-id="bfba6-197">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="bfba6-198">Gangið úr skugga um að varpanir séu fjarlægðar úr `msdy_dualwriteruntimeconfig`-töflunni í Dataverse.</span><span class="sxs-lookup"><span data-stu-id="bfba6-198">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="bfba6-199">Setjið upp [Lausn tvöfaldrar skráningar á aðila og altækri aðsetursbók](https://aka.ms/dual-write-gab) úr AppSource.</span><span class="sxs-lookup"><span data-stu-id="bfba6-199">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="bfba6-200">Í Finance and Operations-forritinu, ef eftirfarandi töflur innihalda gögn, þá skal keyra **Upphaflega samstillingu** fyrir þær.</span><span class="sxs-lookup"><span data-stu-id="bfba6-200">In the finance and operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="bfba6-201">Ávörp</span><span class="sxs-lookup"><span data-stu-id="bfba6-201">Salutations</span></span>
    + <span data-ttu-id="bfba6-202">Persónubundnar manngerðir</span><span class="sxs-lookup"><span data-stu-id="bfba6-202">Personal character types</span></span>
    + <span data-ttu-id="bfba6-203">Kveðjuorð</span><span class="sxs-lookup"><span data-stu-id="bfba6-203">Complimentary closing</span></span>
    + <span data-ttu-id="bfba6-204">Titlar tengiliðar</span><span class="sxs-lookup"><span data-stu-id="bfba6-204">Contact person titles</span></span>
    + <span data-ttu-id="bfba6-205">Hlutverk ákvarðanatöku</span><span class="sxs-lookup"><span data-stu-id="bfba6-205">Decision making roles</span></span>
    + <span data-ttu-id="bfba6-206">Stig viðskiptavildar</span><span class="sxs-lookup"><span data-stu-id="bfba6-206">Loyalty levels</span></span>

5. <span data-ttu-id="bfba6-207">Í forriti viðskiptavinar skal slökkva á eftirfarandi skrefum viðbótar:</span><span class="sxs-lookup"><span data-stu-id="bfba6-207">In the customer engagement app, disable the following plug-in steps.</span></span>

    + <span data-ttu-id="bfba6-208">Reikningsuppfærsla</span><span class="sxs-lookup"><span data-stu-id="bfba6-208">Account Update</span></span>
         + <span data-ttu-id="bfba6-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Uppfærsla reiknings</span><span class="sxs-lookup"><span data-stu-id="bfba6-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="bfba6-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Uppfærsla reiknings</span><span class="sxs-lookup"><span data-stu-id="bfba6-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="bfba6-211">Uppfærsla tengiliðs</span><span class="sxs-lookup"><span data-stu-id="bfba6-211">Contact Update</span></span>
         + <span data-ttu-id="bfba6-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Uppfærsla tengiliðs</span><span class="sxs-lookup"><span data-stu-id="bfba6-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="bfba6-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Uppfærsla tengiliðar</span><span class="sxs-lookup"><span data-stu-id="bfba6-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="bfba6-214">msdyn_party Update</span><span class="sxs-lookup"><span data-stu-id="bfba6-214">msdyn_party Update</span></span>
         + <span data-ttu-id="bfba6-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Uppfærsla msdyn_party</span><span class="sxs-lookup"><span data-stu-id="bfba6-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="bfba6-216">msdyn_vendor Update</span><span class="sxs-lookup"><span data-stu-id="bfba6-216">msdyn_vendor Update</span></span>
         + <span data-ttu-id="bfba6-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Uppfærsla msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="bfba6-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="bfba6-218">Í forriti viðskiptavinar skal slökkva á eftirfarandi verkflæðum:</span><span class="sxs-lookup"><span data-stu-id="bfba6-218">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="bfba6-219">Stofna lánardrottna í reikningstöflu</span><span class="sxs-lookup"><span data-stu-id="bfba6-219">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="bfba6-220">Stofna lánardrottna í reikningstöflu</span><span class="sxs-lookup"><span data-stu-id="bfba6-220">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="bfba6-221">Stofna lánardrottna af gerðinni einstaklingur í tengiliðatöflu</span><span class="sxs-lookup"><span data-stu-id="bfba6-221">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="bfba6-222">Stofna lánardrottna af gerðinni einstaklingur í lánardrottnatöflu</span><span class="sxs-lookup"><span data-stu-id="bfba6-222">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="bfba6-223">Uppfæra lánardrottna í reikningstöflu</span><span class="sxs-lookup"><span data-stu-id="bfba6-223">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="bfba6-224">Uppfæra lánardrottna í lánardrottnatöflu</span><span class="sxs-lookup"><span data-stu-id="bfba6-224">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="bfba6-225">Uppfæra lánardrottna af gerðinni einstaklingur í tengiliðatöflu</span><span class="sxs-lookup"><span data-stu-id="bfba6-225">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="bfba6-226">Uppfæra lánardrottna af gerðinni einstaklingur í lánardrottnatöflu</span><span class="sxs-lookup"><span data-stu-id="bfba6-226">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="bfba6-227">Í gagnasmiðjunni skal keyra sniðmátið með því að velja **Ræsa núna** eins og sýnt er á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="bfba6-227">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="bfba6-228">Þetta ferli gæti tekið nokkrar klukkustundir að ljúka allt eftir því hvert gagnamagnið er.</span><span class="sxs-lookup"><span data-stu-id="bfba6-228">This process might take a few hours to complete based on the data volume.</span></span>

    ![Setja keyrslu af stað](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="bfba6-230">Ef sérstillingar eru fyrir hendi fyrir **Reikning**, **Tengilið** og **Lánardrottin**, þá þarf að breyta sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="bfba6-230">If you have customizations for **Account**, **Contact**, and **Vendor**, then you need to modify the template.</span></span>

8. <span data-ttu-id="bfba6-231">Flytjið inn nýjar færslur **Aðila** í Finance and Operations-forritinu.</span><span class="sxs-lookup"><span data-stu-id="bfba6-231">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="bfba6-232">Sækið `FONewParty.csv`-skrána úr Azure Blob geymslu.</span><span class="sxs-lookup"><span data-stu-id="bfba6-232">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="bfba6-233">Slóðin er `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="bfba6-233">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="bfba6-234">Umbreytið `FONewParty.csv`-skránni í Excel-skrá og flytjið Excel-skrána inn í Finance and Operations-forritið.</span><span class="sxs-lookup"><span data-stu-id="bfba6-234">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the finance and operations app.</span></span> <span data-ttu-id="bfba6-235">Ef csv-innflutningurinn virkar fyrir þig, þá geturðu flutt csv-skrána beint inn.</span><span class="sxs-lookup"><span data-stu-id="bfba6-235">If the csv import works for you, you can import the csv file directly.</span></span> <span data-ttu-id="bfba6-236">Innflutningurinn gæti tekið nokkrar klukkustundir að keyra, en það fer allt eftir gagnamagninu.</span><span class="sxs-lookup"><span data-stu-id="bfba6-236">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="bfba6-237">Frekari upplýsingar er að finna í [Yfirlit yfir inn- og útflutningsvinnslu gagna](../data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="bfba6-237">For more information, see [Data import and export jobs overview](../data-import-export-job.md).</span></span>

    ![Flytja inn Datavers-aðilafærslur](media/data-factory-import-party.png)

9. <span data-ttu-id="bfba6-239">Í forritum viðskiptavinar skal kveikja á eftirfarandi viðbótarskrefum:</span><span class="sxs-lookup"><span data-stu-id="bfba6-239">In the customer engagement apps, enable the following plug-in steps:</span></span>

    + <span data-ttu-id="bfba6-240">Reikningsuppfærsla</span><span class="sxs-lookup"><span data-stu-id="bfba6-240">Account Update</span></span>
         + <span data-ttu-id="bfba6-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Uppfærsla reiknings</span><span class="sxs-lookup"><span data-stu-id="bfba6-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="bfba6-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Uppfærsla reiknings</span><span class="sxs-lookup"><span data-stu-id="bfba6-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="bfba6-243">Uppfærsla tengiliðs</span><span class="sxs-lookup"><span data-stu-id="bfba6-243">Contact Update</span></span>
         + <span data-ttu-id="bfba6-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Uppfærsla tengiliðs</span><span class="sxs-lookup"><span data-stu-id="bfba6-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="bfba6-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Uppfærsla tengiliðar</span><span class="sxs-lookup"><span data-stu-id="bfba6-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="bfba6-246">msdyn_party Update</span><span class="sxs-lookup"><span data-stu-id="bfba6-246">msdyn_party Update</span></span>
         + <span data-ttu-id="bfba6-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Uppfærsla msdyn_party</span><span class="sxs-lookup"><span data-stu-id="bfba6-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="bfba6-248">msdyn_vendor Update</span><span class="sxs-lookup"><span data-stu-id="bfba6-248">msdyn_vendor Update</span></span>
         + <span data-ttu-id="bfba6-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Uppfærsla msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="bfba6-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="bfba6-250">Í forritum viðskiptavinar skal virkja eftirfarandi verkflæði ef slökkt var á þeim í fyrri skrefum:</span><span class="sxs-lookup"><span data-stu-id="bfba6-250">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="bfba6-251">Stofna lánardrottna í reikningstöflu</span><span class="sxs-lookup"><span data-stu-id="bfba6-251">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="bfba6-252">Stofna lánardrottna í reikningstöflu</span><span class="sxs-lookup"><span data-stu-id="bfba6-252">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="bfba6-253">Stofna lánardrottna af gerðinni einstaklingur í tengiliðatöflu</span><span class="sxs-lookup"><span data-stu-id="bfba6-253">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="bfba6-254">Stofna lánardrottna af gerðinni einstaklingur í lánardrottnatöflu</span><span class="sxs-lookup"><span data-stu-id="bfba6-254">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="bfba6-255">Uppfæra lánardrottna í reikningstöflu</span><span class="sxs-lookup"><span data-stu-id="bfba6-255">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="bfba6-256">Uppfæra lánardrottna í lánardrottnatöflu</span><span class="sxs-lookup"><span data-stu-id="bfba6-256">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="bfba6-257">Uppfæra lánardrottna af gerðinni einstaklingur í tengiliðatöflu</span><span class="sxs-lookup"><span data-stu-id="bfba6-257">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="bfba6-258">Uppfæra lánardrottna af gerðinni einstaklingur í lánardrottnatöflu</span><span class="sxs-lookup"><span data-stu-id="bfba6-258">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="bfba6-259">Keyrið varpanir tengdar **Aðilum** eins og lýst er í [Altæk aðila- og aðsetursbók](party-gab.md).</span><span class="sxs-lookup"><span data-stu-id="bfba6-259">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="bfba6-260">Úrræðaleit</span><span class="sxs-lookup"><span data-stu-id="bfba6-260">Troubleshooting</span></span>

1. <span data-ttu-id="bfba6-261">Ef ferlið mistekst skal endurkeyra gagnasmiðjuna og byrja á aðgerðinni sem mistókst.</span><span class="sxs-lookup"><span data-stu-id="bfba6-261">If the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="bfba6-262">Gagnasmiðjan myndar sumar skrár sem hægt er að nota til að staðfesta gögn.</span><span class="sxs-lookup"><span data-stu-id="bfba6-262">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="bfba6-263">Gagnasmiðjan keyrir samkvæmt csv-skránum sem eru afmarkaðar með kommu.</span><span class="sxs-lookup"><span data-stu-id="bfba6-263">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="bfba6-264">Ef reitargildi er með kommu getur það haft áhrif á niðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="bfba6-264">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="bfba6-265">Fjarlægja þarf kommurnar.</span><span class="sxs-lookup"><span data-stu-id="bfba6-265">You need to remove the commas.</span></span>
4. <span data-ttu-id="bfba6-266">Flipinn **Eftirlit** veitir upplýsingar um öll skref og afgreidd gögn.</span><span class="sxs-lookup"><span data-stu-id="bfba6-266">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="bfba6-267">Veljið tiltekið skref til að kemba þau.</span><span class="sxs-lookup"><span data-stu-id="bfba6-267">Select a specific step to debug it.</span></span>

    ![Eftirlitsflipi](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="bfba6-269">Frekari upplýsingar um sniðmátið</span><span class="sxs-lookup"><span data-stu-id="bfba6-269">Learn more about the template</span></span>

<span data-ttu-id="bfba6-270">Þú getur fengið viðbótarupplýsingar um sniðmátið í [Upplýsingaskrá með athugasemdum við sniðmát Azure Data Factory](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span><span class="sxs-lookup"><span data-stu-id="bfba6-270">You can find additional information about the template in [Comments for Azure Data Factory template readme](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span></span>
