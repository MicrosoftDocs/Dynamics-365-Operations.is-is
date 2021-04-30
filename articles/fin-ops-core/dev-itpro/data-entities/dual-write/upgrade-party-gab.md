---
title: Uppfæra í altæka aðila- og aðsetursbókarlíkanið
description: Í þessu efnisatriði er lýst hvernig á að uppfæra gögn tvöfaldrar skráningar í aðilalíkanið og líkan altækrar aðsetursbókar.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 76e64d483e833782733277a64d8dc37cbeba6130
ms.sourcegitcommit: 011468a6cffea8641bebc2922e0676d9f44b36fc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/06/2021
ms.locfileid: "5857371"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="08f20-103">Uppfæra í altæka aðila- og aðsetursbókarlíkanið</span><span class="sxs-lookup"><span data-stu-id="08f20-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="08f20-104">[Sniðmát Azure Data Factory](https://aka.ms/dual-write-gab-adf) hjálpar til við að uppfæra fyrirliggjandi töflugögn **Lykils**, **Tengiliðar** og **Lánardrottins** í tvöfaldri skráningu í aðilalíkanið og líkan altækrar aðsetursbókar.</span><span class="sxs-lookup"><span data-stu-id="08f20-104">The [Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="08f20-105">Sniðmátið afstemmir gögnin úr bæði Finance and Operations-forritum og forritum viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="08f20-105">The template reconciles the data from both Finance and Operations apps and customer engagement applications.</span></span> <span data-ttu-id="08f20-106">Undir lok ferlisins verða reitirnir **Aðili** og **Tengiliður** fyrir **Aðilafærslur** búnir til og tengdir við færslur **Lykils**, **Tengiliðar** og **Lánardrottins** í forritum viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="08f20-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="08f20-107">.csv skrá (`FONewParty.csv`) er mynduð til að stofna nýjar **Aðilafærslur** í Finance and Operations-forritinu.</span><span class="sxs-lookup"><span data-stu-id="08f20-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the Finance and Operations app.</span></span> <span data-ttu-id="08f20-108">Í þessu efnisatriði er að finna leiðbeiningar um notkun Data Factory-sniðmáts og uppfærslu gagnanna.</span><span class="sxs-lookup"><span data-stu-id="08f20-108">This topic provides the instructions to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="08f20-109">Ef engar sérstillingar eru til staðar er hægt að nota sniðmátið eins og það er.</span><span class="sxs-lookup"><span data-stu-id="08f20-109">If you don’t have any customizations, you can use the template as-is.</span></span> <span data-ttu-id="08f20-110">Ef sérstillingar eru fyrir hendi fyrir **Lykil**, **Tengilið** og **Lánardrottin** þarf að breyta sniðmátinu samkvæmt eftirfarandi leiðbeiningum.</span><span class="sxs-lookup"><span data-stu-id="08f20-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!Note]
> <span data-ttu-id="08f20-111">Sniðmátið hjálpar til við að uppfæra eingöngu gögn **Aðila**.</span><span class="sxs-lookup"><span data-stu-id="08f20-111">The template helps to upgrade only the **Party** data.</span></span> <span data-ttu-id="08f20-112">Í síðari útgáfu verða póstföng og rafræn heimilisföng höfð með.</span><span class="sxs-lookup"><span data-stu-id="08f20-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="08f20-113">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="08f20-113">Prerequisites</span></span>

<span data-ttu-id="08f20-114">Þessar forkröfur eru nauðsynlegar:</span><span class="sxs-lookup"><span data-stu-id="08f20-114">These prerequisites are required:</span></span>

+ [<span data-ttu-id="08f20-115">Azure-áskrift</span><span class="sxs-lookup"><span data-stu-id="08f20-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="08f20-116">Aðgangur að sniðmáti</span><span class="sxs-lookup"><span data-stu-id="08f20-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="08f20-117">Þú ert núverandi viðskiptavinur tvöföldrar skráningar.</span><span class="sxs-lookup"><span data-stu-id="08f20-117">You are an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="08f20-118">Uppfærsla undirbúin</span><span class="sxs-lookup"><span data-stu-id="08f20-118">Prepare for the upgrade</span></span>

+ <span data-ttu-id="08f20-119">**Full samstilling**: Bæði umhverfinu eru samstillt að fullu fyrir **Lykil (viðskiptavinur)**, **Tengilið** og **Lánardrottin**.</span><span class="sxs-lookup"><span data-stu-id="08f20-119">**Fully synched**: Both environments are fully synched state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="08f20-120">**Samþættingarlyklar**: Töflur **Lykils (viðskiptavinur)**, **Tengiliðar** og **Lánardrottins** í forritum viðskiptavinar nota tilbúna samþættingarlykla sem fylgja með.</span><span class="sxs-lookup"><span data-stu-id="08f20-120">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="08f20-121">Ef samþættingarlyklarnir voru sérstilltir þarf að sérstilla sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="08f20-121">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="08f20-122">**Aðilanúmer**: Allar færslur **Lykils (viðskiptavinar)**, **Tengiliðar** og **Lánardrottins** sem verða uppfærðar eru með númer **Aðila**.</span><span class="sxs-lookup"><span data-stu-id="08f20-122">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="08f20-123">Færslur án númers **Aðila** verða hunsaðar.</span><span class="sxs-lookup"><span data-stu-id="08f20-123">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="08f20-124">Ef uppfæra á þær færslur skal bæta númeri **Aðila** við þær áður en uppfærsluferlið er sett í gang.</span><span class="sxs-lookup"><span data-stu-id="08f20-124">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="08f20-125">**Stöðvun kerfis**: Í uppfærsluferlinu þarf að slökkva á nettengingu fyrir bæði umhverfi Finance and Operations og umhverfi viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="08f20-125">**System outage**: During the upgrade process, you will have to take both the Finance and Operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="08f20-126">**Skyndimynd**: Takið skyndimyndir af bæði forritum Finance and Operations og viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="08f20-126">**Snapshot**: Take snapshots of both the Finance and Operations and customer engagement apps.</span></span> <span data-ttu-id="08f20-127">Notið skyndimyndirnar til að endurheimta fyrri stöðu ef á þarf að halda.</span><span class="sxs-lookup"><span data-stu-id="08f20-127">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="08f20-128">Nýting</span><span class="sxs-lookup"><span data-stu-id="08f20-128">Deployment</span></span>

1. <span data-ttu-id="08f20-129">Sækið sniðmátið úr [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span><span class="sxs-lookup"><span data-stu-id="08f20-129">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="08f20-130">Skráðu þig inn á [Microsoft Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="08f20-130">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="08f20-131">Stofnið [tilfangaflokk](https://docs.microsoft.com/azure/azure-resource-manager/management/manage-resource-groups-portal).</span><span class="sxs-lookup"><span data-stu-id="08f20-131">Create a [resource group](https://docs.microsoft.com/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="08f20-132">Búið til [geymslureikning](https://docs.microsoft.com/azure/storage/common/storage-account-create?tabs=azure-portal) í tilfangaflokknum sem var stofnaður.</span><span class="sxs-lookup"><span data-stu-id="08f20-132">Create a [storage account](https://docs.microsoft.com/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="08f20-133">Stofnið [gagnasmiðju](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal) í ofangreindum tilfangaflokki sem var stofnaður.</span><span class="sxs-lookup"><span data-stu-id="08f20-133">Create a [data factory](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="08f20-134">Opnið gagnasmiðjuna og veljið reitinn **Stýra og fylgjast með**.</span><span class="sxs-lookup"><span data-stu-id="08f20-134">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="08f20-135">Í flipanum **Stjórna** skal velja **ARM-sniðmát**.</span><span class="sxs-lookup"><span data-stu-id="08f20-135">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="08f20-136">Veljið **Flytja inn ARM-sniðmát** til að flytja inn sniðmátið **Aðili**.</span><span class="sxs-lookup"><span data-stu-id="08f20-136">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="08f20-137">Flytjið sniðmátið inn í gagnasmiðjuna.</span><span class="sxs-lookup"><span data-stu-id="08f20-137">Import the template into the data factory.</span></span> <span data-ttu-id="08f20-138">Færið inn eftirfarandi gildi fyrir **Upplýsingar um verk** og **Upplýsingar um tilvik**.</span><span class="sxs-lookup"><span data-stu-id="08f20-138">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="08f20-139">Svæði</span><span class="sxs-lookup"><span data-stu-id="08f20-139">Field</span></span> | <span data-ttu-id="08f20-140">Virði</span><span class="sxs-lookup"><span data-stu-id="08f20-140">Value</span></span>
    ---|---
    <span data-ttu-id="08f20-141">Áskrift</span><span class="sxs-lookup"><span data-stu-id="08f20-141">Subscription</span></span> | <span data-ttu-id="08f20-142">Azure-áskrift</span><span class="sxs-lookup"><span data-stu-id="08f20-142">Azure subscription</span></span>
    <span data-ttu-id="08f20-143">Tilfangaflokkur</span><span class="sxs-lookup"><span data-stu-id="08f20-143">Resource group</span></span> | <span data-ttu-id="08f20-144">Gefið upp sama tilfang þar sem geymslureikningur er stofnaður fyrir.</span><span class="sxs-lookup"><span data-stu-id="08f20-144">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="08f20-145">Svæði</span><span class="sxs-lookup"><span data-stu-id="08f20-145">Region</span></span> | <span data-ttu-id="08f20-146">Tilgreina svæði.</span><span class="sxs-lookup"><span data-stu-id="08f20-146">Specify region.</span></span>
    <span data-ttu-id="08f20-147">Heiti verksmiðju</span><span class="sxs-lookup"><span data-stu-id="08f20-147">Factory Name</span></span> | <span data-ttu-id="08f20-148">Tilgreina heiti verksmiðju.</span><span class="sxs-lookup"><span data-stu-id="08f20-148">Specify factory name.</span></span>
    <span data-ttu-id="08f20-149">FO Linked Service_service Principal Key</span><span class="sxs-lookup"><span data-stu-id="08f20-149">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="08f20-150">Tilgreinið forritslykilinn.</span><span class="sxs-lookup"><span data-stu-id="08f20-150">Specify the application's key.</span></span>
    <span data-ttu-id="08f20-151">Strengur Azure Blob Storage_connection</span><span class="sxs-lookup"><span data-stu-id="08f20-151">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="08f20-152">Tengingarstrengur Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="08f20-152">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="08f20-153">Dynamics Crm Linked Service_password</span><span class="sxs-lookup"><span data-stu-id="08f20-153">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="08f20-154">Aðgangsorðið fyrir notandareikninginn sem tilgreindur var sem notandanafnið.</span><span class="sxs-lookup"><span data-stu-id="08f20-154">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="08f20-155">FO Linked Service_properties_type Properties_url</span><span class="sxs-lookup"><span data-stu-id="08f20-155">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="08f20-156">FO Linked Service_properties_type Properties_tenant</span><span class="sxs-lookup"><span data-stu-id="08f20-156">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="08f20-157">Tilgreinið upplýsingar um leigjanda (heiti léns eða leigjandakenni) sem forritið heyrir undir.</span><span class="sxs-lookup"><span data-stu-id="08f20-157">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="08f20-158">FO Linked Service_properties_type Properties_aad Resource Id</span><span class="sxs-lookup"><span data-stu-id="08f20-158">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="08f20-159">FO Linked Service_properties_type Properties_service Principal Id</span><span class="sxs-lookup"><span data-stu-id="08f20-159">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="08f20-160">Tilgreinið biðlarakenni forritsins.</span><span class="sxs-lookup"><span data-stu-id="08f20-160">Specify the application's client ID.</span></span>
    <span data-ttu-id="08f20-161">Dynamics Crm Linked Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="08f20-161">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="08f20-162">Notandanafnið sem á að tengja Dynamics.</span><span class="sxs-lookup"><span data-stu-id="08f20-162">The username to connect to Dynamics.</span></span>

    <span data-ttu-id="08f20-163">Frekari upplýsingar er að finna í [Úthluta sniðmáti forðastjóra handvirkt fyrir hvert umhverfi](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Tengdir þjónustueiginleikar](https://docs.microsoft.com/azure/data-factory/connector-dynamics-ax#linked-service-properties) og [Afrita gögn með Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span><span class="sxs-lookup"><span data-stu-id="08f20-163">For more information, see [Manually promote a Resource Manager template for each environment](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Linked service properties](https://docs.microsoft.com/azure/data-factory/connector-dynamics-ax#linked-service-properties), and [Copy data using Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span></span>

10. <span data-ttu-id="08f20-164">Eftir uppsetningu skal staðfesta gagnasöfnin, gagnaflæðið og tengda þjónustu gagnasmiðjunnar.</span><span class="sxs-lookup"><span data-stu-id="08f20-164">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![Gagnasafn, gagnaflæði og tengd þjónusta](media/data-factory-validate.png)

11. <span data-ttu-id="08f20-166">Farið í **Stjórna**.</span><span class="sxs-lookup"><span data-stu-id="08f20-166">Navigate to **Manage**.</span></span> <span data-ttu-id="08f20-167">Undir **Tengingar** skal velja **Tengd þjónusta**.</span><span class="sxs-lookup"><span data-stu-id="08f20-167">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="08f20-168">Veljið **DynamicsCrmLinkedService**.</span><span class="sxs-lookup"><span data-stu-id="08f20-168">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="08f20-169">Á skjámyndinni **Breyta tengdri þjónustu (Dynamics CRM)** skal færa inn eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="08f20-169">In the **Edit linked service (Dynamics CRM)** form, enter the following values:</span></span>

    <span data-ttu-id="08f20-170">Svæði</span><span class="sxs-lookup"><span data-stu-id="08f20-170">Field</span></span> | <span data-ttu-id="08f20-171">Virði</span><span class="sxs-lookup"><span data-stu-id="08f20-171">Value</span></span>
    ---|---
    <span data-ttu-id="08f20-172">Nafn</span><span class="sxs-lookup"><span data-stu-id="08f20-172">Name</span></span> | <span data-ttu-id="08f20-173">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="08f20-173">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="08f20-174">lýsing</span><span class="sxs-lookup"><span data-stu-id="08f20-174">Description</span></span> | <span data-ttu-id="08f20-175">Tengdar þjónustur til að tengjast við CRM-tilvik til að sækja gögn eininga</span><span class="sxs-lookup"><span data-stu-id="08f20-175">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="08f20-176">Tengjast með keyrslutíma samþættingar</span><span class="sxs-lookup"><span data-stu-id="08f20-176">Connect via integration runtime</span></span> | <span data-ttu-id="08f20-177">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="08f20-177">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="08f20-178">Uppsetningargerð</span><span class="sxs-lookup"><span data-stu-id="08f20-178">Deployment type</span></span> | <span data-ttu-id="08f20-179">Nettenging</span><span class="sxs-lookup"><span data-stu-id="08f20-179">Online</span></span>
    <span data-ttu-id="08f20-180">Uri þjónustu</span><span class="sxs-lookup"><span data-stu-id="08f20-180">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="08f20-181">Sannvottunargerð</span><span class="sxs-lookup"><span data-stu-id="08f20-181">Authentication type</span></span> | <span data-ttu-id="08f20-182">Office365</span><span class="sxs-lookup"><span data-stu-id="08f20-182">Office365</span></span>
    <span data-ttu-id="08f20-183">Notandanafn</span><span class="sxs-lookup"><span data-stu-id="08f20-183">User name</span></span> |
    <span data-ttu-id="08f20-184">Aðgangsorð eða Azure-lyklageymsla</span><span class="sxs-lookup"><span data-stu-id="08f20-184">Password or Azure Key Vault</span></span> | <span data-ttu-id="08f20-185">Aðgangsorð</span><span class="sxs-lookup"><span data-stu-id="08f20-185">Password</span></span>
    <span data-ttu-id="08f20-186">Aðgangsorð</span><span class="sxs-lookup"><span data-stu-id="08f20-186">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="08f20-187">Keyra sniðmátið</span><span class="sxs-lookup"><span data-stu-id="08f20-187">Run the template</span></span>

1. <span data-ttu-id="08f20-188">Stöðvið eftirfarandi tvöfalda skráningu **Lykils**, **Tengiliðar** og **Lánardrottins** með Finance and Operations-forritinu.</span><span class="sxs-lookup"><span data-stu-id="08f20-188">Stop the following **Account**, **Contact**, and **Vendor** dual-write using the Finance and Operations app.</span></span>

    + <span data-ttu-id="08f20-189">Viðskiptavinir V3 (lyklar)</span><span class="sxs-lookup"><span data-stu-id="08f20-189">Customers V3(accounts)</span></span>
    + <span data-ttu-id="08f20-190">Viðskiptavinir V3 (tengiliðir)</span><span class="sxs-lookup"><span data-stu-id="08f20-190">Customers V3(contacts)</span></span>
    + <span data-ttu-id="08f20-191">CDS Tengiliðir V2 (tengiliðir)</span><span class="sxs-lookup"><span data-stu-id="08f20-191">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="08f20-192">CDS Tengiliðir V2 (tengiliðir)</span><span class="sxs-lookup"><span data-stu-id="08f20-192">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="08f20-193">Lánardrottinn V2 (msdyn_vendors)</span><span class="sxs-lookup"><span data-stu-id="08f20-193">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="08f20-194">Gangið úr skugga um að varpanir séu fjarlægðar úr `msdy_dualwriteruntimeconfig`-töflunni í Dataverse.</span><span class="sxs-lookup"><span data-stu-id="08f20-194">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="08f20-195">Setjið upp [Lausn tvöfaldrar skráningar á aðila og altækri aðsetursbók](https://aka.ms/dual-write-gab) úr AppSource.</span><span class="sxs-lookup"><span data-stu-id="08f20-195">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="08f20-196">Í Finance and Operations-forritinu, ef eftirfarandi töflur innihalda gögn, þá skal keyra **Upphaflega samstillingu** fyrir þær.</span><span class="sxs-lookup"><span data-stu-id="08f20-196">In the Finance and Operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="08f20-197">Ávörp</span><span class="sxs-lookup"><span data-stu-id="08f20-197">Salutations</span></span>
    + <span data-ttu-id="08f20-198">Persónubundnar manngerðir</span><span class="sxs-lookup"><span data-stu-id="08f20-198">Personal character types</span></span>
    + <span data-ttu-id="08f20-199">Kveðjuorð</span><span class="sxs-lookup"><span data-stu-id="08f20-199">Complimentary closing</span></span>
    + <span data-ttu-id="08f20-200">Titlar tengiliðar</span><span class="sxs-lookup"><span data-stu-id="08f20-200">Contact person titles</span></span>
    + <span data-ttu-id="08f20-201">Hlutverk ákvarðanatöku</span><span class="sxs-lookup"><span data-stu-id="08f20-201">Decision making roles</span></span>
    + <span data-ttu-id="08f20-202">Stig viðskiptavildar</span><span class="sxs-lookup"><span data-stu-id="08f20-202">Loyalty levels</span></span>

5. <span data-ttu-id="08f20-203">Í forriti viðskiptavinar skal slökkva á eftirfarandi viðbótarskrefum.</span><span class="sxs-lookup"><span data-stu-id="08f20-203">In the customer engagement app, disable the following plugin steps.</span></span>

    + <span data-ttu-id="08f20-204">Reikningsuppfærsla</span><span class="sxs-lookup"><span data-stu-id="08f20-204">Account Update</span></span>
         + <span data-ttu-id="08f20-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Uppfærsla reiknings</span><span class="sxs-lookup"><span data-stu-id="08f20-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="08f20-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Uppfærsla reiknings</span><span class="sxs-lookup"><span data-stu-id="08f20-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="08f20-207">Uppfærsla tengiliðs</span><span class="sxs-lookup"><span data-stu-id="08f20-207">Contact Update</span></span>
         + <span data-ttu-id="08f20-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Uppfærsla tengiliðs</span><span class="sxs-lookup"><span data-stu-id="08f20-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="08f20-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Uppfærsla tengiliðar</span><span class="sxs-lookup"><span data-stu-id="08f20-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="08f20-210">msdyn_party Update</span><span class="sxs-lookup"><span data-stu-id="08f20-210">msdyn_party Update</span></span>
         + <span data-ttu-id="08f20-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Uppfærsla msdyn_party</span><span class="sxs-lookup"><span data-stu-id="08f20-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="08f20-212">msdyn_vendor Update</span><span class="sxs-lookup"><span data-stu-id="08f20-212">msdyn_vendor Update</span></span>
         + <span data-ttu-id="08f20-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Uppfærsla msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="08f20-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="08f20-214">Í forriti viðskiptavinar skal slökkva á eftirfarandi verkflæðum:</span><span class="sxs-lookup"><span data-stu-id="08f20-214">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="08f20-215">Stofna lánardrottna í reikningstöflu</span><span class="sxs-lookup"><span data-stu-id="08f20-215">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="08f20-216">Stofna lánardrottna í reikningstöflu</span><span class="sxs-lookup"><span data-stu-id="08f20-216">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="08f20-217">Stofna lánardrottna af gerðinni einstaklingur í tengiliðatöflu</span><span class="sxs-lookup"><span data-stu-id="08f20-217">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="08f20-218">Stofna lánardrottna af gerðinni einstaklingur í lánardrottnatöflu</span><span class="sxs-lookup"><span data-stu-id="08f20-218">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="08f20-219">Uppfæra lánardrottna í reikningstöflu</span><span class="sxs-lookup"><span data-stu-id="08f20-219">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="08f20-220">Uppfæra lánardrottna í lánardrottnatöflu</span><span class="sxs-lookup"><span data-stu-id="08f20-220">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="08f20-221">Uppfæra lánardrottna af gerðinni einstaklingur í tengiliðatöflu</span><span class="sxs-lookup"><span data-stu-id="08f20-221">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="08f20-222">Uppfæra lánardrottna af gerðinni einstaklingur í lánardrottnatöflu</span><span class="sxs-lookup"><span data-stu-id="08f20-222">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="08f20-223">Í gagnasmiðjunni skal keyra sniðmátið með því að velja **Ræsa núna** eins og sýnt er á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="08f20-223">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="08f20-224">Þetta ferli gæti tekið nokkrar klukkustundir að ljúka allt eftir því hvert gagnamagnið er.</span><span class="sxs-lookup"><span data-stu-id="08f20-224">This process might take a few hours to complete based on the data volume.</span></span>

    ![Setja keyrslu af stað](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="08f20-226">Ef sérstillingar eru fyrir hendi fyrir **Reikning**, **Tengilið** og **Lánardrottin**, þá þarf að breyta sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="08f20-226">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template.</span></span>

8. <span data-ttu-id="08f20-227">Flytjið inn nýjar færslur **Aðila** í Finance and Operations-forritinu.</span><span class="sxs-lookup"><span data-stu-id="08f20-227">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="08f20-228">Sækið `FONewParty.csv`-skrána úr Azure Blob geymslu.</span><span class="sxs-lookup"><span data-stu-id="08f20-228">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="08f20-229">Slóðin er `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="08f20-229">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="08f20-230">Umbreytið `FONewParty.csv`-skránni í Excel-skrá og flytjið Excel-skrána inn í Finance and Operations-forritið.</span><span class="sxs-lookup"><span data-stu-id="08f20-230">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the Finance and Operations app.</span></span>  <span data-ttu-id="08f20-231">Ef csv-innflutningurinn virkar fyrir þig, þá geturðu flutt csv-skrá beint inn.</span><span class="sxs-lookup"><span data-stu-id="08f20-231">If the csv import works for you, you can import csv file directly.</span></span> <span data-ttu-id="08f20-232">Innflutningurinn gæti tekið nokkrar klukkustundir að keyra, en það fer allt eftir gagnamagninu.</span><span class="sxs-lookup"><span data-stu-id="08f20-232">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="08f20-233">Frekari upplýsingar er að finna í [Yfirlit yfir inn- og útflutningsvinnslu gagna](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job).</span><span class="sxs-lookup"><span data-stu-id="08f20-233">For more information, see [Data import and export jobs overview](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job).</span></span>

    ![Flytja inn Datavers-aðilafærslur](media/data-factory-import-party.png)

9. <span data-ttu-id="08f20-235">Í forritum viðskiptavinar skal kveikja á eftirfarandi viðbótarskrefum:</span><span class="sxs-lookup"><span data-stu-id="08f20-235">In the customer engagement apps, enable the following plugin steps:</span></span>

    + <span data-ttu-id="08f20-236">Reikningsuppfærsla</span><span class="sxs-lookup"><span data-stu-id="08f20-236">Account Update</span></span>
         + <span data-ttu-id="08f20-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Uppfærsla reiknings</span><span class="sxs-lookup"><span data-stu-id="08f20-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="08f20-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Uppfærsla reiknings</span><span class="sxs-lookup"><span data-stu-id="08f20-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="08f20-239">Uppfærsla tengiliðs</span><span class="sxs-lookup"><span data-stu-id="08f20-239">Contact Update</span></span>
         + <span data-ttu-id="08f20-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Uppfærsla tengiliðs</span><span class="sxs-lookup"><span data-stu-id="08f20-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="08f20-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Uppfærsla tengiliðar</span><span class="sxs-lookup"><span data-stu-id="08f20-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="08f20-242">msdyn_party Update</span><span class="sxs-lookup"><span data-stu-id="08f20-242">msdyn_party Update</span></span>
         + <span data-ttu-id="08f20-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Uppfærsla msdyn_party</span><span class="sxs-lookup"><span data-stu-id="08f20-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="08f20-244">msdyn_vendor Update</span><span class="sxs-lookup"><span data-stu-id="08f20-244">msdyn_vendor Update</span></span>
         + <span data-ttu-id="08f20-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Uppfærsla msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="08f20-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="08f20-246">Í forritum viðskiptavinar skal virkja eftirfarandi verkflæði ef slökkt var á þeim í fyrri skrefum:</span><span class="sxs-lookup"><span data-stu-id="08f20-246">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="08f20-247">Stofna lánardrottna í reikningstöflu</span><span class="sxs-lookup"><span data-stu-id="08f20-247">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="08f20-248">Stofna lánardrottna í reikningstöflu</span><span class="sxs-lookup"><span data-stu-id="08f20-248">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="08f20-249">Stofna lánardrottna af gerðinni einstaklingur í tengiliðatöflu</span><span class="sxs-lookup"><span data-stu-id="08f20-249">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="08f20-250">Stofna lánardrottna af gerðinni einstaklingur í lánardrottnatöflu</span><span class="sxs-lookup"><span data-stu-id="08f20-250">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="08f20-251">Uppfæra lánardrottna í reikningstöflu</span><span class="sxs-lookup"><span data-stu-id="08f20-251">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="08f20-252">Uppfæra lánardrottna í lánardrottnatöflu</span><span class="sxs-lookup"><span data-stu-id="08f20-252">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="08f20-253">Uppfæra lánardrottna af gerðinni einstaklingur í tengiliðatöflu</span><span class="sxs-lookup"><span data-stu-id="08f20-253">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="08f20-254">Uppfæra lánardrottna af gerðinni einstaklingur í lánardrottnatöflu</span><span class="sxs-lookup"><span data-stu-id="08f20-254">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="08f20-255">Keyrið varpanir tengdar **Aðilum** eins og lýst er í [Altæk aðila- og aðsetursbók](party-gab.md).</span><span class="sxs-lookup"><span data-stu-id="08f20-255">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="08f20-256">Úrræðaleit</span><span class="sxs-lookup"><span data-stu-id="08f20-256">Troubleshooting</span></span>

1. <span data-ttu-id="08f20-257">Ef ferlið mistekst skal endurkeyra gagnasmiðjuna og byrja á aðgerðinni sem mistókst.</span><span class="sxs-lookup"><span data-stu-id="08f20-257">In the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="08f20-258">Gagnasmiðjan myndar sumar skrár sem hægt er að nota til að staðfesta gögn.</span><span class="sxs-lookup"><span data-stu-id="08f20-258">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="08f20-259">Gagnasmiðjan keyrir samkvæmt csv-skránum sem eru afmarkaðar með kommu.</span><span class="sxs-lookup"><span data-stu-id="08f20-259">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="08f20-260">Ef reitargildi er með kommu getur það haft áhrif á niðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="08f20-260">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="08f20-261">Fjarlægja þarf kommurnar.</span><span class="sxs-lookup"><span data-stu-id="08f20-261">You need to remove the commas.</span></span>
4. <span data-ttu-id="08f20-262">Flipinn **Eftirlit** veitir upplýsingar um öll skref og afgreidd gögn.</span><span class="sxs-lookup"><span data-stu-id="08f20-262">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="08f20-263">Veljið tiltekið skref til að kemba þau.</span><span class="sxs-lookup"><span data-stu-id="08f20-263">Select a specific step to debug it.</span></span>

    ![Eftirlitsflipi](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="08f20-265">Frekari upplýsingar um sniðmátið</span><span class="sxs-lookup"><span data-stu-id="08f20-265">Learn more about the template</span></span>

<span data-ttu-id="08f20-266">Hægt er að finna athugasemdir um sniðmátið í skránni [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span><span class="sxs-lookup"><span data-stu-id="08f20-266">You can find comments for the template the [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) file.</span></span>
