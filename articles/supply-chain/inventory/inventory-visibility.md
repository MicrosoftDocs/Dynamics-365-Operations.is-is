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
ms.openlocfilehash: 4e588be2ac5aae395ca66e3c9a743a67d71db7c0
ms.sourcegitcommit: a3052f76ad71894dbef66566c07c6e2c31505870
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/10/2021
ms.locfileid: "5574223"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="8e4fc-103">Innbót birgðasýnileika</span><span class="sxs-lookup"><span data-stu-id="8e4fc-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="8e4fc-104">Innbót birgðasýnileika er sjálfstæð og einstaklega sveigjanleg örþjónusta sem býður upp á rakningu lagerbirgða í rauntíma og veitir þar af leiðandi alhliða yfirlit yfir sýnileika birgða.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="8e4fc-105">Allar upplýsingar sem tengjast birgðum á lager eru fluttar út í þjónustuna í nánast rauntíma í gegnum SQL-samþættingu á lágu stigi.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="8e4fc-106">Ytri kerfi fá aðgang að þjónustunni í gegnum RESTful API til að spyrjast fyrir um lagerbirgðir á uppgefnum víddasamstæðum, sem fær þá lista yfir lausar lagerstöður.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="8e4fc-107">Birgðasýnileiki er örþjónusta byggð á Microsoft Dataverse, sem þýðir að hægt er að stækka hana með því að smíða Power Apps og nota Power BI til að bjóða upp á sérsniðna virkni til að uppfylla kröfur fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="8e4fc-108">Einnig er hægt að uppfæra vísinn til að gera birgðafyrirspurnir.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="8e4fc-109">Birgðasýnileiki býður upp á grunnstillingarvalkosti sem gerir því kleift að samþættast við mörg kerfi þriðja aðila.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="8e4fc-110">Hann styður staðlaða birgðavídd, sérsniðna stækkunarhæfni og staðlað, stillanlegt magn sem er reiknað út.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="8e4fc-111">Þetta efnisatriði lýsir því hvernig á að setja upp og grunnstilla innbót birgðasýnileika fyrir Dynamics 365 Supply Chain Management og hvernig á að nota forritunarviðmót þess (API).</span><span class="sxs-lookup"><span data-stu-id="8e4fc-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="8e4fc-112">Setja upp innbót birgðasýnileika</span><span class="sxs-lookup"><span data-stu-id="8e4fc-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="8e4fc-113">Setja þarf upp innbót birgðasýnileika með því að nota Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="8e4fc-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="8e4fc-114">LCS er samstarfsgátt sem býður upp á umhverfi ásamt safni af reglulega uppfærðum þjónustum sem hjálpa til við að stjórna líftíma forritsins fyrir Dynamics 365 Finance and Operations forritin þín.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="8e4fc-115">Frekari upplýsingar er að finna í [Tilföng Lifecycle Services](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span><span class="sxs-lookup"><span data-stu-id="8e4fc-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="8e4fc-116">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="8e4fc-116">Prerequisites</span></span>

<span data-ttu-id="8e4fc-117">Áður en þú setur upp innbót birgðasýnileika þarftu að gera eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="8e4fc-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="8e4fc-118">Fá LCS-innleiðingarverk með að minnsta kosti einu virku umhverfi í notkun.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="8e4fc-119">Gangið úr skugga um að skilyrðum fyrir uppsetningu innbóta sem gefnar eru upp í [Yfirliti innbóta](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) sé lokið.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="8e4fc-120">Sýnileiki birgða krefst ekki tengingu tvöföldrar skráningar.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="8e4fc-121">Hafa skal samskipti við teymi birgðasýnileika á [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) til að fá eftirfarandi þrjár áskildar skrár:</span><span class="sxs-lookup"><span data-stu-id="8e4fc-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>

    - `Inventory Visibility Dataverse Solution.zip`
    - `Inventory Visibility Configuration Trigger.zip`
    - <span data-ttu-id="8e4fc-122">`Inventory Visibility Integration.zip` (ef útgáfan af Supply Chain Management sem er keyrð er eldri en útgáfa 10.0.18)</span><span class="sxs-lookup"><span data-stu-id="8e4fc-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>

> [!NOTE]
> <span data-ttu-id="8e4fc-123">Ríkin sem eru studd eins og er eru Kanada, Bandaríkin og Evrópusambandið (ESB).</span><span class="sxs-lookup"><span data-stu-id="8e4fc-123">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="8e4fc-124">Ef einhverjar spurningar vakna um þessi skilyrði er hægt að hafa samband við vöruteymi birgðasýnileika.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-124">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="8e4fc-125">Setja upp Dataverse</span><span class="sxs-lookup"><span data-stu-id="8e4fc-125">Set up Dataverse</span></span>

<span data-ttu-id="8e4fc-126">Fylgdu þessum skrefum til að setja upp Dataverse.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-126">Follow these steps to set up Dataverse.</span></span>

1. <span data-ttu-id="8e4fc-127">Bætið þjónustureglu við leigjandann:</span><span class="sxs-lookup"><span data-stu-id="8e4fc-127">Add a service principle to your tenant:</span></span>

    1. <span data-ttu-id="8e4fc-128">Setjið upp Azure AD PowerShell-einingu v2 eins og lýst er í [Setja upp Azure Active Directory PowerShell fyrir graf](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="8e4fc-128">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).</span></span>
    1. <span data-ttu-id="8e4fc-129">Keyra eftirfarandi PowerShell-skipun.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-129">Run the following PowerShell command.</span></span>

        ```powershell
        Connect-AzureAD # (open a sign in window and sign in as a tenant user)

        New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
        ```

1. <span data-ttu-id="8e4fc-130">Stofnið forritsnotanda fyrir birgðarsýnileika í Dataverse:</span><span class="sxs-lookup"><span data-stu-id="8e4fc-130">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="8e4fc-131">Opnið vefslóð Dataverse umhverfisins.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-131">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="8e4fc-132">Farið í **Ítarleg stilling \> Kerfi \> Öryggi \> Notendur** og stofnið notanda forrits.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-132">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="8e4fc-133">Notið yfirlitsvalmyndina til að breyta síðuyfirlitinu í **Notendur forritsins**.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-133">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="8e4fc-134">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-134">Select **New**.</span></span> <span data-ttu-id="8e4fc-135">Stilla forritskenni á *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-135">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="8e4fc-136">(Auðkenni hlutar verður sjálfkrafa hlaðið þegar breytingarnar eru vistaðar.) Hægt er að sérstilla nafnið.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-136">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="8e4fc-137">Til dæmis er hægt að breyta því í *Birgðasýnileiki*.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-137">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="8e4fc-138">Þegar þessu er lokið skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-138">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="8e4fc-139">Veljið **Úthluta hlutverki** og veljið því næst **Kerfisstjóri**.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-139">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="8e4fc-140">Ef til er hlutverk sem heitir **Common Data Service Notandi** skal líka velja það.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-140">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="8e4fc-141">Frekari upplýsingar eru í [Stofna notanda forrits](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="8e4fc-141">For more information, see [Create an application user](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="8e4fc-142">Flytjið inn `Inventory Visibility Dataverse Solution.zip` skrána sem inniheldur Dataverse skilgreiningar tengdra eininga og Power Apps:</span><span class="sxs-lookup"><span data-stu-id="8e4fc-142">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="8e4fc-143">Opnið síðuna **Lausnir**.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-143">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="8e4fc-144">Velja **Innflutningur**.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-144">Select **Import**.</span></span>

1. <span data-ttu-id="8e4fc-145">Flytjið inn flæði fyrir ræsingu skilgreiningaruppfærslu:</span><span class="sxs-lookup"><span data-stu-id="8e4fc-145">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="8e4fc-146">Opna Microsoft Flow síðuna.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-146">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="8e4fc-147">Gangið úr skugga um að tengingin sem heitir *Dataverse (eldra efni)* sé til.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-147">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="8e4fc-148">(Ef það er ekki til skal stofna það.)</span><span class="sxs-lookup"><span data-stu-id="8e4fc-148">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="8e4fc-149">Flytja inn `Inventory Visibility Configuration Trigger.zip`-skrá.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-149">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="8e4fc-150">Þegar hún hefur verið flutt inn birtist ræsihnappurinn undir **Mín verkflæði**.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-150">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="8e4fc-151">Frumstilla eftirfarandi fjórar breytur út frá umhverfisupplýsingum:</span><span class="sxs-lookup"><span data-stu-id="8e4fc-151">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="8e4fc-152">Azure AD-leigjandakenni</span><span class="sxs-lookup"><span data-stu-id="8e4fc-152">Azure Tenant ID</span></span>
        - <span data-ttu-id="8e4fc-153">Biðlarakenni Azure-forritsins</span><span class="sxs-lookup"><span data-stu-id="8e4fc-153">Azure Application Client ID</span></span>
        - <span data-ttu-id="8e4fc-154">Leynilykill biðlara Azure-forritsins</span><span class="sxs-lookup"><span data-stu-id="8e4fc-154">Azure Application Client Secret</span></span>
        - <span data-ttu-id="8e4fc-155">Endastöð sýnileika birgða</span><span class="sxs-lookup"><span data-stu-id="8e4fc-155">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="8e4fc-156">Frekari upplýsingar um þessa breytu er að finna í hlutanum [Setja upp samþættingu fyrir Sýnileika birgða](#setup-inventory-visibility-integration) seinna í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-156">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="8e4fc-157">![Ræsing skilgreiningar](media/configuration-trigger.png "Ræsing skilgreiningar")</span><span class="sxs-lookup"><span data-stu-id="8e4fc-157">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="8e4fc-158">Veljið **Kveikja á**.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-158">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="8e4fc-159">Setja upp innbótina</span><span class="sxs-lookup"><span data-stu-id="8e4fc-159">Install the add-in</span></span>

<span data-ttu-id="8e4fc-160">Til að setja upp innbót birgðasýnileika skal gera eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="8e4fc-160">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="8e4fc-161">Skráðu þig inn í gátt [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="8e4fc-161">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="8e4fc-162">Á heimasíðunni skal velja verkið þar sem umhverfið er í notkun.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-162">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="8e4fc-163">Á verksíðunni skal velja umhverfið þar sem á að setja upp innbótina.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-163">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="8e4fc-164">Á heimasíðu umhverfisins skal fletta niður á hlutann **Innbætur umhverfis** í hlutanum **Power Platform samþætting** þar sem hægt er að finna heiti Dataverse-umhverfisins.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-164">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="8e4fc-165">Í hlutanum **Innbætur umhverfis** skal velja **Setja upp nýja innbót**.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-165">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="8e4fc-166">![Heimasíða umhverfis í LCS](media/inventory-visibility-environment.png "Heimasíða umhverfis í LCS")</span><span class="sxs-lookup"><span data-stu-id="8e4fc-166">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="8e4fc-167">Veldu tengilinn **Setja upp nýja innbót**.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-167">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="8e4fc-168">Listi yfir tiltækar innbætur opnast.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-168">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="8e4fc-169">Velja **Sýnileiki birgða** í listanum.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-169">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="8e4fc-170">Sláðu inn gildi fyrir eftirfarandi reiti fyrir umhverfið þitt:</span><span class="sxs-lookup"><span data-stu-id="8e4fc-170">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="8e4fc-171">**Auðkenni AAD-forritsins (biðlara)**</span><span class="sxs-lookup"><span data-stu-id="8e4fc-171">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="8e4fc-172">**AAD-leigjandakenni**</span><span class="sxs-lookup"><span data-stu-id="8e4fc-172">**AAD tenant ID**</span></span>

    <span data-ttu-id="8e4fc-173">![Uppsetningarsíða innbótar](media/inventory-visibility-setup.png "Uppsetningarsíða innbótar")</span><span class="sxs-lookup"><span data-stu-id="8e4fc-173">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="8e4fc-174">Samþykktu skilmálana með því að velja gátreitinn **Skilmálar**.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-174">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="8e4fc-175">Velja **Setja upp**.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-175">Select **Install**.</span></span> <span data-ttu-id="8e4fc-176">Staða innbótarinnar birtist sem **Er í uppsetningu**.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-176">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="8e4fc-177">Þegar henni er lokið skal uppfæra síðuna til að sjá stöðuna breytast í **Uppsett**.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-177">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="8e4fc-178">Fjarlægja innbótina</span><span class="sxs-lookup"><span data-stu-id="8e4fc-178">Uninstall the add-in</span></span>

<span data-ttu-id="8e4fc-179">Til að fjarlægja innbótina skal velja **Fjarlægja**.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-179">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="8e4fc-180">Þegar LCS er uppfært verður innbót birgðasýnileikans fjarlægð.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-180">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="8e4fc-181">Fjarlægingarferlið mun fjarlægja innbótarskráninguna og ræsir einnig vinnslu til að hreinsa öll viðskiptagögn sem vistuð eru í þjónustunni.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-181">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="8e4fc-182">Nota gögn lagerbirgða úr Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="8e4fc-182">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="8e4fc-183">Nota samþættingarpakka birgðasýnileika</span><span class="sxs-lookup"><span data-stu-id="8e4fc-183">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="8e4fc-184">Ef keyrð er útgáfa 10.0.17 eða eldri af Supply Chain Management skal hafa samband við stuðningshóp vegna innleiðingar birgðasýnileika á [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) til að fá skráarpakkann.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-184">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="8e4fc-185">Virkjaðu svo pakkann í LCS.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-185">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="8e4fc-186">Ef villa vegna misræmis útgáfu kemur upp í uppsetningunni þarf að flytja inn handvirkt X++ verkið í þróunarumhverfið.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-186">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="8e4fc-187">Síðan skal stofna virkjanlega pakkann í þróunarumhverfinu og setja hann upp í þróunarumhverfinu.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-187">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="8e4fc-188">Kóðinn fylgir með Supply Chain Management útgáfu 10.0.18.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-188">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="8e4fc-189">Ef sú útgáfa eða nýrri er keyrð þarf ekki uppsetningu.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-189">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="8e4fc-190">Gangið úr skugga um að kveikt sé á eftirfarandi eiginleikum í umhverfi Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-190">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="8e4fc-191">(Sjálfgefið er að kveikt sé á þessu.)</span><span class="sxs-lookup"><span data-stu-id="8e4fc-191">(By default, they are turned on.)</span></span>

| <span data-ttu-id="8e4fc-192">Lýsing eiginleika</span><span class="sxs-lookup"><span data-stu-id="8e4fc-192">Feature description</span></span> | <span data-ttu-id="8e4fc-193">Kóðaútgáfa</span><span class="sxs-lookup"><span data-stu-id="8e4fc-193">Code version</span></span> | <span data-ttu-id="8e4fc-194">Skipta milli klasa</span><span class="sxs-lookup"><span data-stu-id="8e4fc-194">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="8e4fc-195">Gera notkun birgðavídda í InventSum-töflu virka eða óvirka</span><span class="sxs-lookup"><span data-stu-id="8e4fc-195">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="8e4fc-196">10.0.11</span><span class="sxs-lookup"><span data-stu-id="8e4fc-196">10.0.11</span></span> | <span data-ttu-id="8e4fc-197">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="8e4fc-197">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="8e4fc-198">Gera notkun birgðavídda í InventSumDelta-töflu virka eða óvirka</span><span class="sxs-lookup"><span data-stu-id="8e4fc-198">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="8e4fc-199">10.0.12</span><span class="sxs-lookup"><span data-stu-id="8e4fc-199">10.0.12</span></span> | <span data-ttu-id="8e4fc-200">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="8e4fc-200">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="8e4fc-201">Setja upp samþættingu fyrir Sýnileika birgða</span><span class="sxs-lookup"><span data-stu-id="8e4fc-201">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="8e4fc-202">Í Supply Chain Management skal opna vinnusvæðið **[Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** og kveikja á eiginleikanum **Samþætting sýnileika birgða**.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-202">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="8e4fc-203">Farið í **Birgðastjórnun \> Uppsetning \> Samþætting færibreyta sýnileika birgða** og færið inn vefslóð umhverfisins þar sem birgðasýnileiki er keyrður.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-203">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="8e4fc-204">Finnið Azure-svæði LCS-umhverfisins og færið síðan inn vefslóðina.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-204">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="8e4fc-205">Vefslóðin er með eftirfarandi skjámynd:</span><span class="sxs-lookup"><span data-stu-id="8e4fc-205">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com/`

    <span data-ttu-id="8e4fc-206">Í Evrópu verður umhverfið til dæmis með eina af eftirfarandi vefslóðum:</span><span class="sxs-lookup"><span data-stu-id="8e4fc-206">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com/`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com/`

    <span data-ttu-id="8e4fc-207">Eftirfarandi svæði eru í boði sem stendur.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-207">The following regions are currently available.</span></span>

    | <span data-ttu-id="8e4fc-208">Azure-svæði</span><span class="sxs-lookup"><span data-stu-id="8e4fc-208">Azure region</span></span> | <span data-ttu-id="8e4fc-209">Stutt heiti svæðis</span><span class="sxs-lookup"><span data-stu-id="8e4fc-209">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="8e4fc-210">Austur-Ástralía</span><span class="sxs-lookup"><span data-stu-id="8e4fc-210">Australia east</span></span> | <span data-ttu-id="8e4fc-211">eau</span><span class="sxs-lookup"><span data-stu-id="8e4fc-211">eau</span></span> |
    | <span data-ttu-id="8e4fc-212">Suðaustur-Ástralía</span><span class="sxs-lookup"><span data-stu-id="8e4fc-212">Australia southeast</span></span> | <span data-ttu-id="8e4fc-213">seau</span><span class="sxs-lookup"><span data-stu-id="8e4fc-213">seau</span></span> |
    | <span data-ttu-id="8e4fc-214">Mið-Kanada</span><span class="sxs-lookup"><span data-stu-id="8e4fc-214">Canada central</span></span> | <span data-ttu-id="8e4fc-215">cca</span><span class="sxs-lookup"><span data-stu-id="8e4fc-215">cca</span></span> |
    | <span data-ttu-id="8e4fc-216">Austur-Kanda</span><span class="sxs-lookup"><span data-stu-id="8e4fc-216">Canada east</span></span> | <span data-ttu-id="8e4fc-217">eca</span><span class="sxs-lookup"><span data-stu-id="8e4fc-217">eca</span></span> |
    | <span data-ttu-id="8e4fc-218">Norður-Evrópa</span><span class="sxs-lookup"><span data-stu-id="8e4fc-218">North Europe</span></span> | <span data-ttu-id="8e4fc-219">neu</span><span class="sxs-lookup"><span data-stu-id="8e4fc-219">neu</span></span> |
    | <span data-ttu-id="8e4fc-220">Vestur-Evrópa</span><span class="sxs-lookup"><span data-stu-id="8e4fc-220">West Europe</span></span> | <span data-ttu-id="8e4fc-221">weu</span><span class="sxs-lookup"><span data-stu-id="8e4fc-221">weu</span></span> |
    | <span data-ttu-id="8e4fc-222">Austurhluti Bandaríkjanna</span><span class="sxs-lookup"><span data-stu-id="8e4fc-222">East US</span></span> | <span data-ttu-id="8e4fc-223">eus</span><span class="sxs-lookup"><span data-stu-id="8e4fc-223">eus</span></span> |
    | <span data-ttu-id="8e4fc-224">Vesturhluti Bandaríkjanna</span><span class="sxs-lookup"><span data-stu-id="8e4fc-224">West US</span></span> | <span data-ttu-id="8e4fc-225">wus</span><span class="sxs-lookup"><span data-stu-id="8e4fc-225">wus</span></span> |

1. <span data-ttu-id="8e4fc-226">Farið í **Birgðastjórnun \> Reglubundið \> Samþætting sýnileika birgða** og virkjið verkið.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-226">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="8e4fc-227">Öll tilvik birgðabreytinga úr Supply Chain Management verða nú bókuð í birgðasýnileika.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-227">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="8e4fc-228">Almennt API innbótar birgðasýnileika</span><span class="sxs-lookup"><span data-stu-id="8e4fc-228">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="8e4fc-229">Almennt REST API innbótar birgðasýnileikans kynnir ýmsar tilteknar endastöðvar samþættingar.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-229">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="8e4fc-230">Það styður þrjár aðalsamskiptaleiðir:</span><span class="sxs-lookup"><span data-stu-id="8e4fc-230">It supports three main interaction types:</span></span>

- <span data-ttu-id="8e4fc-231">Bókun á lagerbirgðum breytist í innbótina úr ytra kerfi</span><span class="sxs-lookup"><span data-stu-id="8e4fc-231">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="8e4fc-232">Fyrirspurn um núverandi lagermagn úr ytra kerfi</span><span class="sxs-lookup"><span data-stu-id="8e4fc-232">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="8e4fc-233">Sjálfvirk samstilling við lagerbirgðir Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="8e4fc-233">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="8e4fc-234">Sjálfvirk samstilling er ekki hluti af almennu API.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-234">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="8e4fc-235">Þess í stað er það meðhöndlað í bakgrunni fyrir umhverfi þar sem innbót birgðasýnileika er virk.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-235">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="8e4fc-236">Sannvottun</span><span class="sxs-lookup"><span data-stu-id="8e4fc-236">Authentication</span></span>

<span data-ttu-id="8e4fc-237">Öryggistákn verkvangsins er notað til að kalla á innbót birgðasýnileika.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-237">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="8e4fc-238">Þess vegna þarf að búa til *Azure Active Directory (Azure AD) tákn* með því að nota Azure AD-forritið.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-238">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="8e4fc-239">Þá þarf að nota Azure AD táknið til að fá *aðgangsmerkið* úr öryggisþjónustunni.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-239">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="8e4fc-240">Sækja merki öryggisþjónustu á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="8e4fc-240">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="8e4fc-241">Skráðu þig inn í Azure-gátt og notaðu hana til að finna `clientId` og `clientSecret` Supply Chain Management forritið.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-241">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="8e4fc-242">Sækja Azure Active Directory tákn (`aadToken` ) með því að senda inn HTTP beiðni með eftirfarandi eiginleikum:</span><span class="sxs-lookup"><span data-stu-id="8e4fc-242">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="8e4fc-243">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="8e4fc-243">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="8e4fc-244">**Aðferð** - `GET`</span><span class="sxs-lookup"><span data-stu-id="8e4fc-244">**Method** - `GET`</span></span>
    - <span data-ttu-id="8e4fc-245">**Meginefni (eyðublaðagögn)**:</span><span class="sxs-lookup"><span data-stu-id="8e4fc-245">**Body content (form data)**:</span></span>

        | <span data-ttu-id="8e4fc-246">lykill</span><span class="sxs-lookup"><span data-stu-id="8e4fc-246">key</span></span> | <span data-ttu-id="8e4fc-247">gildi</span><span class="sxs-lookup"><span data-stu-id="8e4fc-247">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="8e4fc-248">client_id</span><span class="sxs-lookup"><span data-stu-id="8e4fc-248">client_id</span></span> | <span data-ttu-id="8e4fc-249">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="8e4fc-249">${aadAppId}</span></span> |
        | <span data-ttu-id="8e4fc-250">client_secret</span><span class="sxs-lookup"><span data-stu-id="8e4fc-250">client_secret</span></span> | <span data-ttu-id="8e4fc-251">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="8e4fc-251">${aadAppSecret}</span></span> |
        | <span data-ttu-id="8e4fc-252">grant_type</span><span class="sxs-lookup"><span data-stu-id="8e4fc-252">grant_type</span></span> | <span data-ttu-id="8e4fc-253">client_credentials</span><span class="sxs-lookup"><span data-stu-id="8e4fc-253">client_credentials</span></span> |
        | <span data-ttu-id="8e4fc-254">tilföng</span><span class="sxs-lookup"><span data-stu-id="8e4fc-254">resource</span></span> | <span data-ttu-id="8e4fc-255">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="8e4fc-255">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="8e4fc-256">Þú ættir að fá `aadToken` svar, sem líkist eftirfarandi dæmi.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-256">You should receive an `aadToken` in response, which resembles the following example.</span></span>

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

1. <span data-ttu-id="8e4fc-257">Búa skal til JSON-beiðni sem líkist eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="8e4fc-257">Formulate a JSON request that resembles the following:</span></span>

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

    <span data-ttu-id="8e4fc-258">Hvar:</span><span class="sxs-lookup"><span data-stu-id="8e4fc-258">Where:</span></span>
    - <span data-ttu-id="8e4fc-259">Gildið `client_assertion` verður að vera `aadToken` sem var móttekið í fyrra skrefi.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-259">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="8e4fc-260">Gildið `context` verður að vera umhverfiskenni þar sem á að nota viðbótina.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-260">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="8e4fc-261">Stillið öll önnur gildi eins og sýnt er í dæminu.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-261">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="8e4fc-262">Sendið inn HTTP-beiðni með eftirfarandi eiginleikum:</span><span class="sxs-lookup"><span data-stu-id="8e4fc-262">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="8e4fc-263">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="8e4fc-263">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="8e4fc-264">**Aðferð** - `POST`</span><span class="sxs-lookup"><span data-stu-id="8e4fc-264">**Method** - `POST`</span></span>
    - <span data-ttu-id="8e4fc-265">**HTTP** - Inniheldur API-útgáfu (lykilinn er `Api-Version` og gildið er `1.0`)</span><span class="sxs-lookup"><span data-stu-id="8e4fc-265">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="8e4fc-266">**Meginefni efnis** - Nota skal JSON-beiðni sem var stofnuð í fyrra skrefi.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-266">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="8e4fc-267">Þú færð `access_token` í staðinn.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-267">You will get an `access_token` in response.</span></span> <span data-ttu-id="8e4fc-268">Þetta er það sem þú þarft sem handhafalykill til að kalla í API birgðasýnileikans.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-268">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="8e4fc-269">Eftirfarandi er dæmi.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-269">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="8e4fc-270">Skilgreina API fyrir sýnileika birgða</span><span class="sxs-lookup"><span data-stu-id="8e4fc-270">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="8e4fc-271">Áður en þjónustan er notuð þarf að ljúka við skilgreiningarnar sem lýst er í eftirfarandi undirköflum.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-271">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="8e4fc-272">Skilgreiningin kann að vera mismunandi eftir því hverjar upplýsingar um umhverfið þitt eru.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-272">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="8e4fc-273">Hún inniheldur fyrst og fremst fjóra hluti:</span><span class="sxs-lookup"><span data-stu-id="8e4fc-273">It primarily includes four parts:</span></span>

- [<span data-ttu-id="8e4fc-274">Deildaskipting</span><span class="sxs-lookup"><span data-stu-id="8e4fc-274">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="8e4fc-275">Víddarskilgreiningar</span><span class="sxs-lookup"><span data-stu-id="8e4fc-275">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="8e4fc-276">Lyklun</span><span class="sxs-lookup"><span data-stu-id="8e4fc-276">Indexing</span></span>](#indexing)
- [<span data-ttu-id="8e4fc-277">Sérsniðin mæling</span><span class="sxs-lookup"><span data-stu-id="8e4fc-277">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="8e4fc-278">Deildaskipting</span><span class="sxs-lookup"><span data-stu-id="8e4fc-278">Partitioning</span></span>

<span data-ttu-id="8e4fc-279">Skipting getur haft umtalsverð áhrif á afköst API fyrir sýnileika birgða.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-279">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="8e4fc-280">Það er góð hugmynd að skilgreina skema sem leyfir smá flokkun á gögnum en leyfir samtímis gagnlegar gagnafyrirspurnir.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-280">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="8e4fc-281">`organizationId` (`dataAreaId` í Supply Chain Management) verður alltaf hluti af skiptingunni og birgðasýnileiki er sjálfgefið stilltur á skiptingu eftir víddum sem *Svæði + Staðsetning*.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-281">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="8e4fc-282">Þetta þýðir að alltaf þurfi að senda fyrirspurn á þjónustuna með þessum víddum sem skilgreindar eru í síunum.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-282">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="8e4fc-283">*Svæði* og *Staðsetning* eru tvær almennar sjálfgefnar víddir í birgðasýnileika.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-283">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="8e4fc-284">Í Supply Chain Management eru þessar víddir kallaðar *Svæði* (`InventSiteId`) og *Vöruhús* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="8e4fc-284">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="8e4fc-285">Víddarskilgreiningar</span><span class="sxs-lookup"><span data-stu-id="8e4fc-285">Dimension configurations</span></span>

<span data-ttu-id="8e4fc-286">Sýnileiki birgða mun bjóða upp á lista yfir almennar sjálfgefnar víddir til að virkja samþættingu margra upprunakerfa.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-286">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="8e4fc-287">Í eftirfarandi töflu er listi yfir birgðavíddir sem verða sjálfgefin víddarheiti í birgðasýnileika.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-287">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="8e4fc-288">Tegund víddar</span><span class="sxs-lookup"><span data-stu-id="8e4fc-288">Dimension type</span></span> | <span data-ttu-id="8e4fc-289">Heiti víddar</span><span class="sxs-lookup"><span data-stu-id="8e4fc-289">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="8e4fc-290">Afurð</span><span class="sxs-lookup"><span data-stu-id="8e4fc-290">Product</span></span> | `ColorId` |
| <span data-ttu-id="8e4fc-291">Afurð</span><span class="sxs-lookup"><span data-stu-id="8e4fc-291">Product</span></span> | `SizeId` |
| <span data-ttu-id="8e4fc-292">Afurð</span><span class="sxs-lookup"><span data-stu-id="8e4fc-292">Product</span></span> | `StyleId` |
| <span data-ttu-id="8e4fc-293">Afurð</span><span class="sxs-lookup"><span data-stu-id="8e4fc-293">Product</span></span> | `ConfigId` |
| <span data-ttu-id="8e4fc-294">Rakning</span><span class="sxs-lookup"><span data-stu-id="8e4fc-294">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="8e4fc-295">Rakning</span><span class="sxs-lookup"><span data-stu-id="8e4fc-295">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="8e4fc-296">Staður</span><span class="sxs-lookup"><span data-stu-id="8e4fc-296">Location</span></span> | `LocationId` |
| <span data-ttu-id="8e4fc-297">Staður</span><span class="sxs-lookup"><span data-stu-id="8e4fc-297">Location</span></span> | `SiteId` |
| <span data-ttu-id="8e4fc-298">Birgðastaða</span><span class="sxs-lookup"><span data-stu-id="8e4fc-298">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="8e4fc-299">Miðast við vöruhús</span><span class="sxs-lookup"><span data-stu-id="8e4fc-299">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="8e4fc-300">Miðast við vöruhús</span><span class="sxs-lookup"><span data-stu-id="8e4fc-300">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="8e4fc-301">Miðast við vöruhús</span><span class="sxs-lookup"><span data-stu-id="8e4fc-301">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="8e4fc-302">Gerð víddar sem er skráð í fyrri töflu er aðeins til viðmiðunar.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-302">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="8e4fc-303">Ekki þarf að skilgreina gerð víddar í birgðasýnileika.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-303">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="8e4fc-304">Ef sérstillt vídd er til staðar og þarf að flytjast yfir í sjálfgefið gildi þegar birgðasýnileiki notar hana, er hægt að skilgreina heiti **Sérsniðinnar víddar** í birgðasýnileika.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-304">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="8e4fc-305">Ytri kerfi fá aðgang að sýnileika birgða í gegnum RESTful API sem bjóða upp á lagerupplýsingar um uppgefin víddarsett sem senda á fyrirspurn um.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-305">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="8e4fc-306">Fyrir samþættinguna, gerir birgðasýnileiki þér kleift að stilla *ytri gagnagjafa rásar* og upprunavíddina við *markvíddina* í birgðasýnileika.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-306">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="8e4fc-307">Markvíddirnar ættu að vera eitt af eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="8e4fc-307">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="8e4fc-308">Sjálfgefnar víddir í birgðasýnileika</span><span class="sxs-lookup"><span data-stu-id="8e4fc-308">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="8e4fc-309">Sérsniðnar víddir</span><span class="sxs-lookup"><span data-stu-id="8e4fc-309">Custom dimensions</span></span>

<span data-ttu-id="8e4fc-310">Tilgangurinn með víddarskilgreiningunni er sá að staðla samþættingu margra kerfa fyrir fyrirspurnina á víddum og bókunartilvikinu með víddum.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-310">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="8e4fc-311">Lyklun</span><span class="sxs-lookup"><span data-stu-id="8e4fc-311">Indexing</span></span>

<span data-ttu-id="8e4fc-312">Oftast verður fyrirspurn um birgðir ekki bara um hæsta stig „samtölunnar“, heldur viltu hugsanlega sjá niðurstöður teknar saman eftir birgðavíddum.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-312">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="8e4fc-313">Sýnileiki birgða veitir sveigjanleika með því að gera þér kleift að setja upp vísa sem byggja á víddinni eða samsetningu víddanna.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-313">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="8e4fc-314">Sem stendur er aðeins hægt að skilgreina vísa fyrir fimm að hámarki.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-314">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="8e4fc-315">Þú þarft að íhuga vandlega hvaða vídd eða víddarsamsetningu þú notar fyrir innleiðingu til að tryggja að hún uppfylli þarfir fyrirtækisins þíns.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-315">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="8e4fc-316">Til dæmis, ef ætlunin er að senda fyrirspurn um afurðir eins og hér segir:</span><span class="sxs-lookup"><span data-stu-id="8e4fc-316">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="8e4fc-317">Spyrjast fyrir um samanlagðar afurðir á lager af víddunum *Litur* og *Stærð*.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-317">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="8e4fc-318">Í sumum tilfellum er bara ætlunin að spyrjast fyrir um afurðina í heild sinni.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-318">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="8e4fc-319">Þú hefðir þá tvær vísanir sem eru skilgreindar á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="8e4fc-319">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="8e4fc-320">Tómi hornklofinn mun safna saman eftir auðkenni afurðar innan skiptingar.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-320">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="8e4fc-321">Vísunin skilgreinir hvernig hægt er að flokka niðurstöðurnar samkvæmt fyrirspurnarstillingunni `groupBy`.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-321">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="8e4fc-322">Í þessu tilfelli, ef þú skilgreinir ekki eitthvað `groupBy` gildi, færðu samtölur eftir `productid`.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-322">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="8e4fc-323">Annars, ef skilgreint er `groupBy` sem `groupBy=ColorId&groupBy=SizeId` færðu margar línur til baka, sem byggja á mismunandi samsetningu á lit og stærð í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-323">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="8e4fc-324">Hægt er að setja skilyrði fyrirspurnar í meginmál beiðninnar.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-324">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="8e4fc-325">Hér er dæmi um fyrirspurn um afurðina með lita- og stærðarsamsetningu.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-325">Here is a sample query on the product with color and size combination.</span></span>

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

#### <a name="custom-measurement"></a><span data-ttu-id="8e4fc-326">Sérsniðin mæling</span><span class="sxs-lookup"><span data-stu-id="8e4fc-326">Custom measurement</span></span>

<span data-ttu-id="8e4fc-327">Sjálfgefna mælingarmagnið er tengt við Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-327">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="8e4fc-328">Hins vegar gætir þú viljað hafa magn sem er gert úr samsetningu sjálfgefinna mælinga.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-328">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="8e4fc-329">Til að gera þetta er hægt að hafa skilgreiningu á sérsniðnu magni, sem verður bætt við úttak lagerfyrirspurnar.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-329">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="8e4fc-330">Virknin gerir einfaldlega kleift að skilgreina safn mælinga sem verður bætt við og/eða safn mælinga sem verður dregið frá til að búa til sérsniðnu mælinguna.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-330">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="8e4fc-331">Til dæmis með eftirfarandi fyrirspurnarskilyrði muntu skilgreina magn sérsniðinnar mælingar sem `MyCustomAvailableforReservation` sem tilheyrandi notkunarkerfi notar.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-331">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="8e4fc-332">Notkunarkerfi</span><span class="sxs-lookup"><span data-stu-id="8e4fc-332">Consumption system</span></span> | <span data-ttu-id="8e4fc-333">Reiknaðar mælingar</span><span class="sxs-lookup"><span data-stu-id="8e4fc-333">Calculated measurers</span></span> | <span data-ttu-id="8e4fc-334">Gagnaveita</span><span class="sxs-lookup"><span data-stu-id="8e4fc-334">Data source</span></span> | <span data-ttu-id="8e4fc-335">Umbreytir</span><span class="sxs-lookup"><span data-stu-id="8e4fc-335">Modifier</span></span> | <span data-ttu-id="8e4fc-336">Útreikningsgerð umbreytis</span><span class="sxs-lookup"><span data-stu-id="8e4fc-336">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="8e4fc-337">samlagning</span><span class="sxs-lookup"><span data-stu-id="8e4fc-337">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="8e4fc-338">samlagning</span><span class="sxs-lookup"><span data-stu-id="8e4fc-338">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="8e4fc-339">Frádráttur</span><span class="sxs-lookup"><span data-stu-id="8e4fc-339">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="8e4fc-340">samlagning</span><span class="sxs-lookup"><span data-stu-id="8e4fc-340">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="8e4fc-341">Frádráttur</span><span class="sxs-lookup"><span data-stu-id="8e4fc-341">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="8e4fc-342">samlagning</span><span class="sxs-lookup"><span data-stu-id="8e4fc-342">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="8e4fc-343">samlagning</span><span class="sxs-lookup"><span data-stu-id="8e4fc-343">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="8e4fc-344">Frádráttur</span><span class="sxs-lookup"><span data-stu-id="8e4fc-344">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="8e4fc-345">Frádráttur</span><span class="sxs-lookup"><span data-stu-id="8e4fc-345">Subtraction</span></span> |

<span data-ttu-id="8e4fc-346">Þannig mun fyrirspurnin um sérsniðna magnmælingu skila eftirfarandi úttaki.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-346">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="8e4fc-347">`MyCustomAvailableforReservation` úttakið byggir á útreikningsstillingu í sérsniðnum mælingum sem:</span><span class="sxs-lookup"><span data-stu-id="8e4fc-347">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="8e4fc-348">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="8e4fc-348">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="8e4fc-349">Bókun lagerbreytinga</span><span class="sxs-lookup"><span data-stu-id="8e4fc-349">Posting on-hand changes</span></span>

<span data-ttu-id="8e4fc-350">Nákvæm vefslóð sem tilvikið verður bókað á mun ráðast af landsvæði notanda.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-350">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="8e4fc-351">Hún verður á forminu:</span><span class="sxs-lookup"><span data-stu-id="8e4fc-351">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="8e4fc-352">Þegar hún er vottuð verður þessi vefslóð notuð ásamt HTTP `POST`-aðferðinni til að senda breytingatilvik lagers á þjónustuna.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-352">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="8e4fc-353">Sérstakur haus er notaður til að eiga samskipti við Dynamics 365 þjónustuna í gegnum HTTP-beiðnir, þar sem umhverfiskennið er tilgreint fyrir tilvik Supply Chain Management sem gögnin eru tengd við.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-353">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="8e4fc-354">Dæmi:</span><span class="sxs-lookup"><span data-stu-id="8e4fc-354">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="8e4fc-355">Fyrirspurn um bókun lagerbreytinga, dæmi 1</span><span class="sxs-lookup"><span data-stu-id="8e4fc-355">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="8e4fc-356">Þetta dæmi sýnir aðstæður þar sem víddarskilgreining verður sett upp í Power Apps.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-356">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="8e4fc-357">Notaðu eftirfarandi fyrirspurn til að skilgreina víddarvörpunina í Power Apps:</span><span class="sxs-lookup"><span data-stu-id="8e4fc-357">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="8e4fc-358">Nú er hægt að tilgreina `dimensionDataSource` og nota sérsniðnar víddir í fyrirspurnum.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-358">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="8e4fc-359">Kerfið mun umbreyta sérsniðnum víddum í grunnvíddir.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-359">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="8e4fc-360">Fyrirspurn um bókun lagerbreytinga, dæmi 2</span><span class="sxs-lookup"><span data-stu-id="8e4fc-360">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="8e4fc-361">Þetta dæmi sýnir aðstæður þar sem engar varpanir eru settar upp fyrir víddarskilgreininguna í Power Apps, þannig að bókunin ætti einnig að nota grunnvíddirnar.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-361">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="8e4fc-362">Allar víddir verða að vera grunnvíddir þegar reiturinn `dimensionDataSource` er núll, tómur eða með stafabil.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-362">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="8e4fc-363">Eiginleikar JSON-skjalareits</span><span class="sxs-lookup"><span data-stu-id="8e4fc-363">JSON document field properties</span></span>

<span data-ttu-id="8e4fc-364">Reitirnir úr dæmum JSON-fyrirspurna sem boðið var upp á hér á undan eru með eiginleikana sem gefnir eru upp í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-364">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="8e4fc-365">Kenni svæðis</span><span class="sxs-lookup"><span data-stu-id="8e4fc-365">Field ID</span></span> | <span data-ttu-id="8e4fc-366">lýsing</span><span class="sxs-lookup"><span data-stu-id="8e4fc-366">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="8e4fc-367">Einkvæmt auðkenni fyrir tiltekið breytingartilvik.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-367">A unique ID for the specific change event.</span></span> <span data-ttu-id="8e4fc-368">Þetta auðkenni er notað til að tryggja að ef samskipti við þjónustuna klikka við bókun, myndi endursending á tilvikinu ekki leiða til þess að sama tilvikið yrði talið tvisvar í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-368">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="8e4fc-369">Kennimerki fyrirtækisins sem tengt er við tilvikið.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-369">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="8e4fc-370">Þetta varpar í fyrirtækiskenni eða gagnasvæðiskenni Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-370">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="8e4fc-371">Kennimerki afurðar sem um ræðir.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-371">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="8e4fc-372">Magnið sem á lager þarf að breytast um.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-372">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="8e4fc-373">Ef til dæmis 10 nýjum beyglum var bætt við hilluna, þá væri þetta gildi 10.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-373">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="8e4fc-374">Ef 3 beyglur yrðu síðan teknar úr hillunni eða seldar, þá væri þetta gildi -3.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-374">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="8e4fc-375">Gagnagjafi víddanna sem notaðar eru í breytingartilviki og fyrirspurn bókunar.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-375">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="8e4fc-376">Ef gagnagjafi er tilgreindur er hægt að nota sérstilltar víddir úr tilgreindum gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-376">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="8e4fc-377">Með víddaskilgreiningunni getur birgðasýnileiki varpað sérstilltu víddunum í almennu sjálfgefnu víddirnar.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-377">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="8e4fc-378">Ef `dimensionDataSource` er ekki tilgreint er aðeins hægt að nota almennar sjálfgefnar víddir í fyrirspurnunum.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-378">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="8e4fc-379">Gagnvirkur poki af lykla-/gildispörum.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-379">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="8e4fc-380">Þetta mun varpa í sumar víddirnar í Supply Chain Management, en einnig er hægt að bæta við sérstilltum víddum (eins og *Uppruni*) sem kann að gefa til kynna ef tilvikið kom frá Supply Chain Management eða ytra kerfi.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-380">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="8e4fc-381">Spyrjast fyrir um núverandi lagerbirgðir</span><span class="sxs-lookup"><span data-stu-id="8e4fc-381">Querying current on-hand</span></span>

<span data-ttu-id="8e4fc-382">Endastöðin til að spyrjast fyrir um núverandi lagerbirgðir verður með svipaða vefslóð:</span><span class="sxs-lookup"><span data-stu-id="8e4fc-382">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="8e4fc-383">Send verður fyrirspurn á hana með HTTP `POST`-aðferðinni.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-383">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="8e4fc-384">Núverandi lagerfyrirspurn, dæmi 1</span><span class="sxs-lookup"><span data-stu-id="8e4fc-384">Current on-hand query example 1</span></span>

<span data-ttu-id="8e4fc-385">Þetta dæmi sýnir aðstæður þar sem búið er að ljúka víddarskilgreiningunni í Power Apps.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-385">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="8e4fc-386">Notaðu eftirfarandi fyrirspurn til að skilgreina víddarvörpunina í Power Apps:</span><span class="sxs-lookup"><span data-stu-id="8e4fc-386">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="8e4fc-387">Nú er hægt að tilgreina `dimensionDataSource` og nota sérsniðnar víddir í fyrirspurnum.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-387">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="8e4fc-388">Kerfið mun umbreyta sérsniðnum víddum í grunnvíddir.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-388">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="8e4fc-389">Hægt er að tilgreina `DimensionDataSource` í `filters` og tilgreina sérsniðnar víddir bæði í `filters` og `groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-389">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="8e4fc-390">Kerfið mun umbreyta sérsniðnum víddum í grunnvíddir.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-390">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="8e4fc-391">Núverandi lagerfyrirspurn, dæmi 2</span><span class="sxs-lookup"><span data-stu-id="8e4fc-391">Current on-hand query example 2</span></span>

<span data-ttu-id="8e4fc-392">Þetta dæmi sýnir aðstæður þar sem engar varpanir eru settar upp fyrir víddarskilgreininguna í Power Apps, þannig að bókunin ætti einnig að nota grunnvíddirnar.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-392">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="8e4fc-393">Allar víddir verða að vera grunnvíddir þegar reiturinn `dimensionDataSource`, undir `filters` er núll, tómur eða með stafabil.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-393">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="8e4fc-394">Dæmi um niðurstöður</span><span class="sxs-lookup"><span data-stu-id="8e4fc-394">Example return result</span></span>

<span data-ttu-id="8e4fc-395">Fyrirspurnirnar sem sýndar voru í fyrra dæminu gætu skilað niðurstöðum sem þessari.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-395">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="8e4fc-396">Athugið að magnreitirnir eru skipulagðir sem orðabók yfir mælingar og tengd gildi þeirra.</span><span class="sxs-lookup"><span data-stu-id="8e4fc-396">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
