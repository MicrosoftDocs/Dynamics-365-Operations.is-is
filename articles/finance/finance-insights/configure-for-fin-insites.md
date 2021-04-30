---
title: Stillingar fyrir Fjármálainnsýn (forútgáfa)
description: Þetta efnisatriði útskýrir grunnstillingarskref sem mun gera kerfinu kleift að nota þá eiginleika sem eru í boði í Fjármálainnsýn.
author: ShivamPandey-msft
ms.date: 11/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 54117c009cfeb7307938cc6bd43e774ccfedcfb1
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908831"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="63ac0-103">Stillingar fyrir Fjármálainnsýn (forútgáfa)</span><span class="sxs-lookup"><span data-stu-id="63ac0-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="63ac0-104">Fjármálainnsýn sameinar virkni Microsoft Dynamics 365 Finance við Microsoft Dataverse, Azure og AI Builder til að bjóða upp á öflug spáverkfæri fyrir fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="63ac0-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Microsoft Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="63ac0-105">Þetta efnisatriði útskýrir grunnstillingarskref sem mun gera kerfinu kleift að nota þá eiginleika sem eru í boði í Fjármálainnsýn.</span><span class="sxs-lookup"><span data-stu-id="63ac0-105">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="63ac0-106">Virkja Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="63ac0-106">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="63ac0-107">Virkjaðu umhverfið með því að fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="63ac0-107">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="63ac0-108">Í Microsoft Dynamics Lifecycle Services (LCS) skal búa til eða uppfæra Dynamics 365 Finance umhverfi.</span><span class="sxs-lookup"><span data-stu-id="63ac0-108">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="63ac0-109">Umhverfið krefst forritsútgáfu 10.0.11/Verkvangsuppfærslu 35 eða nýrra.</span><span class="sxs-lookup"><span data-stu-id="63ac0-109">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="63ac0-110">Umhverfið verður að vera vel tiltækt í Sandbox.</span><span class="sxs-lookup"><span data-stu-id="63ac0-110">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="63ac0-111">(Þessi tegund umhverfis er einnig þekkt sem umhverfi í tveggja laga umhverfi.) Frekari upplýsingar er að finna í [Umhverfisskipulagning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="63ac0-111">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="63ac0-112">Ef verið er að nota Contoso-sýnigögnin þarf viðbótarsýnigögn til að nota greiðsluspá viðskiptavinar, sjóðstreymisspár og fjárhagsáætlunarspár.</span><span class="sxs-lookup"><span data-stu-id="63ac0-112">If you're using Contoso demo data, you will require additional sample data to use the Customer payment predictions, Cash flow forecasts, and Budget forecasts features.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="63ac0-113">Skilgreina Dataverse</span><span class="sxs-lookup"><span data-stu-id="63ac0-113">Configure Dataverse</span></span>

<span data-ttu-id="63ac0-114">Hægt er að ljúka við handvirk grunnstillingarskref sem fylgja, eða hægt er að hraða skilgreiningarferlinu með því að nota Windows PowerShell-forskrift sem er gefin upp.</span><span class="sxs-lookup"><span data-stu-id="63ac0-114">You can complete the manual configuration steps that follow, or you can speed up the configuration process by using the Windows PowerShell script that is provided.</span></span> <span data-ttu-id="63ac0-115">Þegar PowerShell-forskrift hefur verið keyrð mun það gefa upp gildi sem eru notuð til að skilgreina Fjármálainnsýn.</span><span class="sxs-lookup"><span data-stu-id="63ac0-115">When the PowerShell script has finished running, it will give you values to use to configure Finance insights.</span></span> 

> [!NOTE]
> <span data-ttu-id="63ac0-116">Opnaðu PowerShell í tölvunni til að keyra skriftuna.</span><span class="sxs-lookup"><span data-stu-id="63ac0-116">Open PowerShell on your PC to run the script.</span></span> <span data-ttu-id="63ac0-117">Þú gætir þurft PowerShell útgáfu 5.</span><span class="sxs-lookup"><span data-stu-id="63ac0-117">You may need PowerShell version 5.</span></span> <span data-ttu-id="63ac0-118">Valkosturinn „Prófaðu þetta“ í Microsoft Azure CLI virkar hugsanlega ekki.</span><span class="sxs-lookup"><span data-stu-id="63ac0-118">The Microsoft Azure CLI "Try it" option may not work.</span></span>

# <a name="manual-configuration-steps"></a>[<span data-ttu-id="63ac0-119">Handvirk grunnstillingarskref</span><span class="sxs-lookup"><span data-stu-id="63ac0-119">Manual configuration steps</span></span>](#tab/configuration-steps)

1. <span data-ttu-id="63ac0-120">Opnaðu [Power Platform stjórnendamiðstöð ](https://admin.powerplatform.microsoft.com/) og fylgdu þessum skrefum til að búa til nýtt Dataverse -umhverfi í sama Active Directory leigjanda:</span><span class="sxs-lookup"><span data-stu-id="63ac0-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Dataverse environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="63ac0-121">Opnið síðuna **Umhverfi**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-121">Open the **Environments** page.</span></span>

        <span data-ttu-id="63ac0-122">[![Umhverfissíða](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="63ac0-122">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="63ac0-123">Veljið **Nýtt umhverfi**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-123">Select **New environment**.</span></span>
    3. <span data-ttu-id="63ac0-124">Í reitnum **Gerð** skal velja **Sandkassi**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-124">In the **Type** field, select **Sandbox**.</span></span>
    4. <span data-ttu-id="63ac0-125">Stillið **Búa til gagnagrunn** valkostinn á **Já**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-125">Set the **Create Database** option to **Yes**.</span></span>
    5. <span data-ttu-id="63ac0-126">Veljið **Næst**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-126">Select **Next**.</span></span>
    6. <span data-ttu-id="63ac0-127">Velja tungumál og gjaldmiðil fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="63ac0-127">Select the language and currency for your organization.</span></span>
    7. <span data-ttu-id="63ac0-128">Samþykkið sjálfgildin fyrir önnur svæði.</span><span class="sxs-lookup"><span data-stu-id="63ac0-128">Accept the default values for the other fields.</span></span>
    8. <span data-ttu-id="63ac0-129">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-129">Select **Save**.</span></span>
    9. <span data-ttu-id="63ac0-130">Endurhlaða þarf síðuna **Umhverfi** .</span><span class="sxs-lookup"><span data-stu-id="63ac0-130">Refresh the **Environments** page.</span></span>
    10. <span data-ttu-id="63ac0-131">Bíða skal þar til gildið fyrir reitinn **Staða** er uppfært í **Tilbúið**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-131">Wait until the value of the **State** field is updated to **Ready**.</span></span>
    11. <span data-ttu-id="63ac0-132">Skráið niður Dataverse kenni fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="63ac0-132">Make a note of the Dataverse organization ID.</span></span>
    12. <span data-ttu-id="63ac0-133">Veljið umhverfi og svo **Stillingar**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-133">Select the environment, and then select **Settings**.</span></span>
    13. <span data-ttu-id="63ac0-134">Veljið **Tilföng \> Allar eldri stillingar**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-134">Select **Resources \> All Legacy Settings**.</span></span>
    14. <span data-ttu-id="63ac0-135">Á efstu yfirlitsstikunni skal velja **Stillingar** og síðan **Sérstillingar**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-135">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    15. <span data-ttu-id="63ac0-136">Veljið **Tilföng fyrir þróunaraðila**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-136">Select **Developer Resources**.</span></span>
    16. <span data-ttu-id="63ac0-137">Afritið gildið **Dataverse kenni fyrirtækis**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-137">Copy the **Dataverse organization ID** value.</span></span>
    17. <span data-ttu-id="63ac0-138">Í veffangastikunni vafrans skal gera athugasemd við VEFSLÓÐINA fyrir Dataverse-fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="63ac0-138">In the browser's address bar, make a note of the URL for the Dataverse organization.</span></span> <span data-ttu-id="63ac0-139">Til dæmis gæti vefslóðin verið `https://org42b2b3d3.crm.dynamics.com`.</span><span class="sxs-lookup"><span data-stu-id="63ac0-139">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

2. <span data-ttu-id="63ac0-140">Ef ætlunin er að nota sjóðstreymisspár eða fjárhagsáætlunarspár skal fylgja þessum skrefum til að uppfæra skýringartextamörk fyrirtækisins í að minnsta kosti 50 megabæt (MB):</span><span class="sxs-lookup"><span data-stu-id="63ac0-140">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="63ac0-141">Opnið [Power Apps-gáttina](https://make.powerapps.com)</span><span class="sxs-lookup"><span data-stu-id="63ac0-141">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="63ac0-142">Veljið það umhverfi sem var stofnað og veljið síðan **Ítarlegar stillingar**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-142">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="63ac0-143">Veljið **Stillingar\> Skilgreining tölvupósts**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-143">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="63ac0-144">Breytið gildi **Hámarksstærð skráar** reitnum í **51.200**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-144">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="63ac0-145">(Gildið er gefið upp í kílóbætum \[KB\].)</span><span class="sxs-lookup"><span data-stu-id="63ac0-145">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="63ac0-146">Veljið **Í lagi** til að vista breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="63ac0-146">Select **OK** to save your changes.</span></span>

# <a name="windows-powershell-configuration-script"></a>[<span data-ttu-id="63ac0-147">Forskrift Windows PowerShell-skilgreiningar</span><span class="sxs-lookup"><span data-stu-id="63ac0-147">Windows PowerShell configuration script</span></span>](#tab/powershell-configuration-script)

```azurecli-interactive
Write-Output 'The following modules need to be present for execution of this script:'
Write-Output '  Microsoft.PowerApps.Administration.PowerShell'
Write-Output '  Microsoft.PowerApps.PowerShell'
Write-Output '  Microsoft.Xrm.Tooling.CrmConnector.PowerShell'

try {
    $moduleConsent = Read-Host 'Is it ok to install or update these modules as needed? (yes/no)'
    if ($moduleConsent -ne 'yes' -and $moduleConsent -ne 'y') {
        Write-Warning 'User declined to install required modules.'
        return
    }

    $module = 'Microsoft.PowerApps.Administration.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '2.0.61' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '2.0.61' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.PowerApps.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '1.0.9' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '1.0.9' -AllowClobber -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.Xrm.Tooling.CrmConnector.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '3.3.0.892' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '3.3.0.892' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    Write-Output '================================================================================='

    $useMfa = $false
    $useMfaPrompt = Read-Host "Does your organization require the use of multi-factor authentication? (yes/no)"
    if ($useMfaPrompt -eq 'yes' -or $useMfaPrompt -eq 'y') {
        $useMfa = $true
    }
    if(-not $useMfa) {
        $credential = Get-Credential -Message 'Power Apps Credential'
    }

    $orgFriendlyName = Read-Host "Enter the name of the CDS Organization to use or create: (blank for 'FinanceInsightsOrg')"
    if ($orgFriendlyName.Trim() -eq '') {
        $orgFriendlyName = 'FinanceInsightsOrg'
    }

    $isDefaultOrgPrompt = Read-Host ("Is '" + $orgFriendlyName + "' the default organization for your tenant? (yes/no)")
    if ($isDefaultOrgPrompt -eq 'yes' -or $isDefaultOrgPrompt -eq 'y') {
        $isDefaultOrg = $true
    }

    if ($credential) {
        Add-PowerAppsAccount -Username $credential.UserName -Password $credential.Password
    }
    else {
        Add-PowerAppsAccount
    }

    if ($isDefaultOrg) {
        $orgMatch = ('(default)')
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { $_.IsDefault -eq $true })
    }
    else {
        $orgMatch = ('{0} (*)' -f $orgFriendlyName)
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.IsDefault -eq $false -and ($_.DisplayName -eq $orgFriendlyName -or $_.DisplayName -like $orgMatch)) })
    }

    $getCrmOrgParams = @{ 'OnlineType' = 'Office365' }
    if ($credential) {
        $getCrmOrgParams.Credential = $credential
    }

    if ($null -eq $environment) {
        Write-Output '================================================================================='
        Write-Output 'PowerApps environment not found. A new one will be provisioned.'

        $invalid = 'invalid'

        $location = $invalid
        $cdsLocations = (Get-AdminPowerAppEnvironmentLocations | Select-Object LocationName).LocationName
        while (-not ($location -in $cdsLocations)) {
            $location = (Read-Host -Prompt "Enter the location in which to create the new PowerApps environment: ('help' to see values)")
            if ($location -eq 'help') {
                $cdsLocations
            }
        }

        $currency = $invalid
        $cdsCurrencies = (Get-AdminPowerAppCdsDatabaseCurrencies -Location $location | Select-Object CurrencyName).CurrencyName
        while ($currency -ne '' -and -not ($currency -in $cdsCurrencies)) {
            $currency = (Read-Host -Prompt "Enter the currency to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($currency -eq 'help') {
                $cdsCurrencies
            }
        }

        $language = $invalid
        $cdsLanguages = (Get-AdminPowerAppCdsDatabaseLanguages -Location $location | Select-Object LanguageName, LanguageDisplayName)
        while ($language -ne '' -and -not ($language -in $cdsLanguages.LanguageName)) {
            $language = (Read-Host -Prompt "Enter the language name to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($language -eq 'help') {
                $cdsLanguages | Format-Table -Property LanguageName, LanguageDisplayName
            }
        }

        Write-Output 'Provisioning PowerApps environment. This may take several minutes.'

        $sleep = 15

        $envParams = @{ 'DisplayName' = $orgFriendlyName; 'EnvironmentSku' = 'Sandbox'; 'ProvisionDatabase' = $true; 'Location' = $location; 'WaitUntilFinished' = $true }
        if ($language.Trim() -ne '') {
            $envParams.LanguageName = $language
        }
        if ($currency.Trim() -ne '') {
            $envParams.CurrencyName = $currency
        }
        $newEnvResult = New-AdminPowerAppEnvironment @envParams
        if (($null -eq $newEnvResult) -or ($newEnvResult.CommonDataServiceDatabaseProvisioningState -ne 'Succeeded')) {
            Write-Warning 'Failed to create to PowerApps environment'
            if ($null -ne $newEnvResult) {
                $newEnvResult
            }
        }
        else {
            $environment = $null
            $retryCount = 0
            while (($null -eq $environment) -and ($retryCount -lt 5)) {
                Start-Sleep -Seconds $sleep
                $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.DisplayName -like $orgMatch) })
            }
            Write-Output ("Provisioned PowerApps environment with name: '" + $environment.DisplayName + "'")
        }

        Write-Output 'Waiting for CDS organization provisioning. This may take several minutes.'
        if (-not $credential) {
            $sleep = 120
            Write-Output 'You may be prompted for credentials multiple times while checking the status of the provisioning.'
        }

        while ($null -eq $crmOrg) {
            Start-Sleep -Seconds $sleep
            $crmOrg = (Get-CrmOrganizations @getCrmOrgParams) | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }
    else {
        $crmOrgs = Get-CrmOrganizations @getCrmOrgParams
        if ($UseDefaultOrganization -eq $true) {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -match $orgMatch }
        }
        else {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }

    Write-Output '================================================================================='
    Write-Output 'Values for PowerAI LCS Add-In:'
    Write-Output ("  CDS organization url:             " + $crmOrg.WebApplicationUrl)
    Write-Output ("  CDS organization ID:              " + $crmOrg.OrganizationId)
}
catch {
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $_.Exception.InnerException
    while ($null -ne $inner) {
        Write-Output 'Inner Exception:'
        Write-Error $_.Exception.Message
        Write-Warning $_.Exception.StackTrace
        $inner = $inner.InnerException
    }
}
```
---

## <a name="configure-the-azure-setup"></a><span data-ttu-id="63ac0-148">Skilgreina Azure uppsetningu</span><span class="sxs-lookup"><span data-stu-id="63ac0-148">Configure the Azure setup</span></span>

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="63ac0-149">Sláið inn Dataverse skráarkenni og hlutarkenni Azure AD notandans</span><span class="sxs-lookup"><span data-stu-id="63ac0-149">Enter the Dataverse directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="63ac0-150">Sláið inn Dataverse skráasafnskenni:</span><span class="sxs-lookup"><span data-stu-id="63ac0-150">Enter the Dataverse directory ID:</span></span>

    1. <span data-ttu-id="63ac0-151">Opnið [Azure-gáttina](https://portal.azure.com)</span><span class="sxs-lookup"><span data-stu-id="63ac0-151">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="63ac0-152">Skráðu þig inn með því að nota NOTANDAKENNIÐ sem var notað til að búa til Dataverse-umhverfið.</span><span class="sxs-lookup"><span data-stu-id="63ac0-152">Sign in by using the user ID that was used to create the Dataverse environment.</span></span>
    3. <span data-ttu-id="63ac0-153">Opnið **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-153">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="63ac0-154">Afritið gildið **Leigjandakenni**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-154">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="63ac0-155">Færa inn auðkenni hlutar notanda Azure Active Directory (Azure AD):</span><span class="sxs-lookup"><span data-stu-id="63ac0-155">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="63ac0-156">Í [Azure-gátt](https://portal.azure.com) skal opna **Notendur** og leita að notandanum eftir netfangi.</span><span class="sxs-lookup"><span data-stu-id="63ac0-156">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="63ac0-157">Færið inn nafn notanda.</span><span class="sxs-lookup"><span data-stu-id="63ac0-157">Select the user's name.</span></span>
    3. <span data-ttu-id="63ac0-158">Afritið **Hlutarkenni** gildið.</span><span class="sxs-lookup"><span data-stu-id="63ac0-158">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="63ac0-159">Nota Azure Cloud Shell til að setja upp Data Lake-tilföng fjármálainnsýnar</span><span class="sxs-lookup"><span data-stu-id="63ac0-159">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="63ac0-160">Nota Windows PowerShell-forskrift</span><span class="sxs-lookup"><span data-stu-id="63ac0-160">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="63ac0-161">Boðið er upp á Windows PowerShell-forskrift þannig að auðvelt er að setja upp Azure-tilföng sem eru skilgreind í [Grunnstilla útflutning í Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="63ac0-161">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="63ac0-162">Ef óskað er eftir því að setja upp handvirkt skal sleppa þessu ferli og halda áfram með ferlið í hlutanum [Handvirk uppsetning](#manual-setup).</span><span class="sxs-lookup"><span data-stu-id="63ac0-162">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="63ac0-163">Fylgið skrefunum hér að neðan til að keyra PowerShell-forskrift.</span><span class="sxs-lookup"><span data-stu-id="63ac0-163">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="63ac0-164">Hugsanlega virkar ekki valkosturinn „Prófaðu þetta“ í Azure CLI eða ekki er hægt að keyra þessa forskrift á tölvunni.</span><span class="sxs-lookup"><span data-stu-id="63ac0-164">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="63ac0-165">Fylgið eftirfarandi skrefum til að grunnstilla Azure með Windows PowerShell-forskriftinni.</span><span class="sxs-lookup"><span data-stu-id="63ac0-165">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="63ac0-166">Réttindi til að búa til Azure-tilfangaflokk, Azure-tilföng og Azure AD-forrit þurfa að vera til staðar.</span><span class="sxs-lookup"><span data-stu-id="63ac0-166">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="63ac0-167">Frekari upplýsingar um nauðsynlegar heimildir má finna á [Athuga Azure AD heimildir](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="63ac0-167">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="63ac0-168">Í [Azure-gátt](https://portal.azure.com) skal opna viðkomandi Azure-áskrift.</span><span class="sxs-lookup"><span data-stu-id="63ac0-168">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="63ac0-169">Veljið **Cloud Shell**-hnappinn hægra megin við svæðið **Leita**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-169">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="63ac0-170">Veljið **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-170">Select **PowerShell**.</span></span>
3. <span data-ttu-id="63ac0-171">Búðu til geymslu, ef beðið er um að gera það.</span><span class="sxs-lookup"><span data-stu-id="63ac0-171">Create storage, if you're prompted to do so.</span></span> <span data-ttu-id="63ac0-172">Því næst skal hlaða upp Windows PowerShell-forskrift á lotuna.</span><span class="sxs-lookup"><span data-stu-id="63ac0-172">Then upload the Windows PowerShell script to the session.</span></span>
4. <span data-ttu-id="63ac0-173">Keyra forskrift.</span><span class="sxs-lookup"><span data-stu-id="63ac0-173">Run the script.</span></span>
5. <span data-ttu-id="63ac0-174">Fylgið kvaðningunum til að keyra forskriftina.</span><span class="sxs-lookup"><span data-stu-id="63ac0-174">Follow the prompts to run the script.</span></span>
6. <span data-ttu-id="63ac0-175">Notið upplýsingar úr forskriftinni til að setja upp innbótina **Flytja út í Data Lake** í LCS.</span><span class="sxs-lookup"><span data-stu-id="63ac0-175">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
7. <span data-ttu-id="63ac0-176">Notið upplýsingar úr forskriftinni til að virkja einingaverslunina á síðunni **Gagnatengingar** í Finance (**Kerfisstjórnun \> Kerfisfæribreytur \> Gagnatengingar**).</span><span class="sxs-lookup"><span data-stu-id="63ac0-176">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="63ac0-177">Handvirk uppsetning</span><span class="sxs-lookup"><span data-stu-id="63ac0-177">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="63ac0-178">Bæta umsóknum við Azure AD leigjanda</span><span class="sxs-lookup"><span data-stu-id="63ac0-178">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="63ac0-179">Í [Azure-gáttinni](https://portal.azure.com) skal fara á **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-179">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="63ac0-180">Veljið **Stjórna \> Enterprise-forrit**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-180">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="63ac0-181">Leitið að eftirfarandi forritum eftir FORRITSKENNINU.</span><span class="sxs-lookup"><span data-stu-id="63ac0-181">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="63ac0-182">Forrit</span><span class="sxs-lookup"><span data-stu-id="63ac0-182">Application</span></span>                              | <span data-ttu-id="63ac0-183">Auðkenni forrits</span><span class="sxs-lookup"><span data-stu-id="63ac0-183">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="63ac0-184">Microsoft Dynamics ERP Microservices</span><span class="sxs-lookup"><span data-stu-id="63ac0-184">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="63ac0-185">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="63ac0-185">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="63ac0-186">Microsoft Dynamics ERP Microservices CDS</span><span class="sxs-lookup"><span data-stu-id="63ac0-186">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="63ac0-187">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="63ac0-187">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="63ac0-188">Heimildaþjónusta AI Builder</span><span class="sxs-lookup"><span data-stu-id="63ac0-188">AI Builder Authorization Service</span></span>         | <span data-ttu-id="63ac0-189">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="63ac0-189">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="63ac0-190">Ef ekki eitthvað af undanfarandi forritum finnst ekki skal prófa eftirfarandi skref.</span><span class="sxs-lookup"><span data-stu-id="63ac0-190">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="63ac0-191">Á staðbundnu vélinni skal velja **Upphafsvalmyndina** og leita að **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-191">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="63ac0-192">Velja skal og halda fingri á (eða hægrismella) **Windows PowerShell** og velja svo **Keyra sem stjórnandi**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-192">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="63ac0-193">Keyrið eftirfarandi skipun til að setja upp **AzureAD** einingun.</span><span class="sxs-lookup"><span data-stu-id="63ac0-193">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="63ac0-194">Ef NuGet-veita er nauðsynleg til að halda áfram skal velja **Y** til að setja hana upp.</span><span class="sxs-lookup"><span data-stu-id="63ac0-194">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="63ac0-195">Ef skeytið „Ótraust geymslׅa“ birtist skal velja **Y** til að halda áfram.</span><span class="sxs-lookup"><span data-stu-id="63ac0-195">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="63ac0-196">Fyrir hvert forrit sem verður að bæta við þarf að keyra eftirfarandi skipanir til að bæta forritinu við Azure AD.</span><span class="sxs-lookup"><span data-stu-id="63ac0-196">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="63ac0-197">Skráðu þig inn sem stjórnandi Azure AD þegar beðið er um það.</span><span class="sxs-lookup"><span data-stu-id="63ac0-197">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="63ac0-198">Stofna Azure-tilföng</span><span class="sxs-lookup"><span data-stu-id="63ac0-198">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="63ac0-199">Ganga skal úr skugga um að eftirfarandi tilföng séu stofnuð í sama Azure AD-tilviki og Dataverse-umhverfið.</span><span class="sxs-lookup"><span data-stu-id="63ac0-199">Make sure that you create the following resources in the same Azure AD instance as the Dataverse environment.</span></span> <span data-ttu-id="63ac0-200">Ekki er hægt að nota tilföng úr öðru Azure AD-tilviki.</span><span class="sxs-lookup"><span data-stu-id="63ac0-200">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="63ac0-201">Búa til nýjan geymslureikning:</span><span class="sxs-lookup"><span data-stu-id="63ac0-201">Create a new storage account:</span></span>

    1. <span data-ttu-id="63ac0-202">Í [Azure Portal](https://portal.azure.com) skal stofna geymslureikning.</span><span class="sxs-lookup"><span data-stu-id="63ac0-202">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="63ac0-203">Í svarglugganum **Stofna geymslureikning** skal stilla eftirfarandi svæði:</span><span class="sxs-lookup"><span data-stu-id="63ac0-203">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="63ac0-204">**Staðsetning** – velja gagnamiðstöð með umhverfinu.</span><span class="sxs-lookup"><span data-stu-id="63ac0-204">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="63ac0-205">**Afköst** – mælt er með **Hefðbundin**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-205">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="63ac0-206">**Reikningsgerð** – velja þarf **StorageV2**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-206">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="63ac0-207">Í svarglugganum **Ítarlegir valkostir**, fyrir **Data Lake Storage Gen2**, skal velja **Virkja** undir **Stigveldis nafnabil**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-207">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="63ac0-208">Ef þessi eiginleiki er gerður óvirkur er ekki hægt að nota gögn sem Finance and Operations-forrit skrifa með þjónustu á borð við Power BI-gagnaflæði.</span><span class="sxs-lookup"><span data-stu-id="63ac0-208">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="63ac0-209">Veljið **yfirfara og búa til**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-209">Select **Review and create**.</span></span> <span data-ttu-id="63ac0-210">Þegar uppsetningu er lokið verður nýja tilfangið til staðar á Azure-gáttinni.</span><span class="sxs-lookup"><span data-stu-id="63ac0-210">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="63ac0-211">Opnaðu geymslureikninginn sem þú stofnaðir.</span><span class="sxs-lookup"><span data-stu-id="63ac0-211">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="63ac0-212">Á valmyndinni til vinstri skal velja **Aðgangslyklar**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-212">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="63ac0-213">Afritið og vistið tengingarstreng fyrir annaðhvort **Key1** eða **Key2**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-213">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="63ac0-214">Afrita og vista heiti geymslureiknings.</span><span class="sxs-lookup"><span data-stu-id="63ac0-214">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="63ac0-215">Búa til nýja lyklageymslu:</span><span class="sxs-lookup"><span data-stu-id="63ac0-215">Create a new key vault:</span></span>

    1. <span data-ttu-id="63ac0-216">Í [Azure Portal](https://portal.azure.com) skal stofna lyklageymslu.</span><span class="sxs-lookup"><span data-stu-id="63ac0-216">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="63ac0-217">Í svarglugganum **Stofna lyklageymslu** á svæðinu **Staðsetning** skal velja gagnamiðstöðina þar sem umhverfið er að finna.</span><span class="sxs-lookup"><span data-stu-id="63ac0-217">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="63ac0-218">Eftir að lyklageymsla er stofnuð skal velja hana á listanum og síðan velja **Leynilyklar**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-218">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="63ac0-219">Veljið **Mynda/Flytja inn**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-219">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="63ac0-220">Á síðunni **Stofna leynilykil**, á svæðinu **Valkostir upphleðslu**, skal velja **Handvirkt**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-220">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="63ac0-221">Færa skal inn heiti fyrir leynilykilinn.</span><span class="sxs-lookup"><span data-stu-id="63ac0-221">Enter a name for the secret.</span></span> <span data-ttu-id="63ac0-222">Gerið athugasemd við heitið vegna þess að það verður að nota það síðar.</span><span class="sxs-lookup"><span data-stu-id="63ac0-222">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="63ac0-223">Á svæðinu **Gildi** skal færa inn tengingarstreng sem fenginn var úr geymslureikningi í fyrra ferli.</span><span class="sxs-lookup"><span data-stu-id="63ac0-223">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="63ac0-224">Veljið **Virkjað** og veljið síðan **Búa til**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-224">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="63ac0-225">Leynilykillinn er stofnaður og bætt við Lyklageymslu.</span><span class="sxs-lookup"><span data-stu-id="63ac0-225">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="63ac0-226">Opnið **Lyklageymsluyfirlit** og skráið niður DNS-heitið.</span><span class="sxs-lookup"><span data-stu-id="63ac0-226">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="63ac0-227">Stofna og skrá Azure AD forrit:</span><span class="sxs-lookup"><span data-stu-id="63ac0-227">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="63ac0-228">Í [Azure-gáttinni](https://portal.azure.com) skal opna **Azure Active Directory** og velja svo **Forritaskráningar**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-228">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="63ac0-229">Velja skal **Ný forritaskráning** og stilla eftirfarandi svæði:</span><span class="sxs-lookup"><span data-stu-id="63ac0-229">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="63ac0-230">**Heiti** - Færið inn heiti forritsins.</span><span class="sxs-lookup"><span data-stu-id="63ac0-230">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="63ac0-231">**Forritsgerð** – Veljið **Vef-API**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-231">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="63ac0-232">**Framsenda URI-uppsetningu** – Sláið inn vefslóð fyrir Dynamics 365-tilvikið, til dæmis, `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="63ac0-232">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="63ac0-233">Opnið forritið sem var búið til og afritið og vistið gildi fyrir **Forritskenni (biðlari)**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-233">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="63ac0-234">Gefa verður upp gildið síðar þegar lyklageymslan er sett upp.</span><span class="sxs-lookup"><span data-stu-id="63ac0-234">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="63ac0-235">Farið í **API-heimildir** og fylgið eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="63ac0-235">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="63ac0-236">Veljið **Bæta við heimild**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-236">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="63ac0-237">Veljið **Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-237">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="63ac0-238">Þegar búið er að velja úthlutaðar heimildir skal velja **Notandi\_Eftirlíking**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-238">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="63ac0-239">Veldu **Bæta við heimildum**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-239">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="63ac0-240">Á valmyndinni fyrir forritið skal velja **Vottorð \& Leynilykar** og síðan skal fylgja þessum skrefum til að búa til leynilykla lyklageymslu:</span><span class="sxs-lookup"><span data-stu-id="63ac0-240">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="63ac0-241">Veljið **Nýtt leyniorð biðlara**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-241">Select **New client secret**.</span></span>
        2. <span data-ttu-id="63ac0-242">Í reitnum **Lyklalýsing** skal færa inn heiti.</span><span class="sxs-lookup"><span data-stu-id="63ac0-242">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="63ac0-243">Veljið tímalengd og svo **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-243">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="63ac0-244">Leynilykill er myndaður á svæðinu **Gildi**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-244">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="63ac0-245">Afritaðu og vistaðu leynigildið.</span><span class="sxs-lookup"><span data-stu-id="63ac0-245">Copy and save the secret value.</span></span>

4. <span data-ttu-id="63ac0-246">Stofna leynilykla lyklageymslu:</span><span class="sxs-lookup"><span data-stu-id="63ac0-246">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="63ac0-247">Opnið lyklageymsluna sem stofnuð var áður og veljið **Leynilyklar**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-247">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="63ac0-248">Fyrir hvert heiti leynilykils í eftirfarandi töflu skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="63ac0-248">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="63ac0-249">Veljið **Mynda/Flytja inn**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-249">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="63ac0-250">Á síðunni **Stofna leynilykil**, á svæðinu **Valkostir upphleðslu**, skal velja **Handvirkt**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-250">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="63ac0-251">Búa skal til heiti leynilykils og gildi úr eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="63ac0-251">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="63ac0-252">Veljið **Virkjað** og veljið síðan **Búa til**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-252">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="63ac0-253">Leynilykillinn er stofnaður og bætt við Lyklageymslu.</span><span class="sxs-lookup"><span data-stu-id="63ac0-253">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="63ac0-254">Leyniheiti</span><span class="sxs-lookup"><span data-stu-id="63ac0-254">Secret name</span></span>                       | <span data-ttu-id="63ac0-255">Leynilykill</span><span class="sxs-lookup"><span data-stu-id="63ac0-255">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="63ac0-256">forrit-auðkenni</span><span class="sxs-lookup"><span data-stu-id="63ac0-256">app-id</span></span>                            | <span data-ttu-id="63ac0-257">Forritskenni forritsins sem var stofnað áður</span><span class="sxs-lookup"><span data-stu-id="63ac0-257">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="63ac0-258">forrit-leyndarmál</span><span class="sxs-lookup"><span data-stu-id="63ac0-258">app-secret</span></span>                        | <span data-ttu-id="63ac0-259">Leyndarmál biðlarans sem var vistað áður</span><span class="sxs-lookup"><span data-stu-id="63ac0-259">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="63ac0-260">geymsla-reikningur-heiti</span><span class="sxs-lookup"><span data-stu-id="63ac0-260">storage-account-name</span></span>              | <span data-ttu-id="63ac0-261">Heiti geymslureikningsins sem var stofnaður áður, t.d. **storageaccount1**</span><span class="sxs-lookup"><span data-stu-id="63ac0-261">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="63ac0-262">geymsla-reikningur-tenging-strengur</span><span class="sxs-lookup"><span data-stu-id="63ac0-262">storage-account-connection-string</span></span> | <span data-ttu-id="63ac0-263">Tengingarstrengurinn sem var afritaður af síðunni **Aðgangslyklar** fyrir geymslureikninginn</span><span class="sxs-lookup"><span data-stu-id="63ac0-263">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="63ac0-264">Heimila forriti aðgang að lyklageymslu:</span><span class="sxs-lookup"><span data-stu-id="63ac0-264">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="63ac0-265">Í [Azure-gátt](https://portal.azure.com) skal opna lyklageymsluna sem var stofnuð áður.</span><span class="sxs-lookup"><span data-stu-id="63ac0-265">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="63ac0-266">Velja aðgangsstefnur.</span><span class="sxs-lookup"><span data-stu-id="63ac0-266">Select the access policies.</span></span>
    3. <span data-ttu-id="63ac0-267">Fyrir hvert forrit í eftirfarandi töflu skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="63ac0-267">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="63ac0-268">Veljið **Bæta við aðgangsreglu** til að búa til aðgangsreglu.</span><span class="sxs-lookup"><span data-stu-id="63ac0-268">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="63ac0-269">Á svæðinu **Heimildir leynilykils** skal velja heimildir úr eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="63ac0-269">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="63ac0-270">Á svæðinu **Velja aðalreikning** skal leita að birtingarheiti forrits sem birtist í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="63ac0-270">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="63ac0-271">Veljið **Velja**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-271">Select **Select**.</span></span>
        5. <span data-ttu-id="63ac0-272">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-272">Select **Add**.</span></span>
        6. <span data-ttu-id="63ac0-273">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-273">Select **Save**.</span></span>

        | <span data-ttu-id="63ac0-274">Forrit</span><span class="sxs-lookup"><span data-stu-id="63ac0-274">Application</span></span>                                              | <span data-ttu-id="63ac0-275">Aðgangsheimildir</span><span class="sxs-lookup"><span data-stu-id="63ac0-275">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="63ac0-276">Birtingarheiti nýja forritsins sem var búið til</span><span class="sxs-lookup"><span data-stu-id="63ac0-276">The display name of the new application that you created</span></span> | <span data-ttu-id="63ac0-277">Sækja, listi</span><span class="sxs-lookup"><span data-stu-id="63ac0-277">Get, List</span></span>   |
        | <span data-ttu-id="63ac0-278">**Microsoft Dynamics ERP Microservices**</span><span class="sxs-lookup"><span data-stu-id="63ac0-278">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="63ac0-279">Sækja, listi</span><span class="sxs-lookup"><span data-stu-id="63ac0-279">Get, List</span></span>   |

6. <span data-ttu-id="63ac0-280">Úthluta hlutverkum til að fá aðgang að geymslureikningi:</span><span class="sxs-lookup"><span data-stu-id="63ac0-280">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="63ac0-281">Í [Azure-gáttinni](https://portal.azure.com) skal opna geymslureikninginn sem var stofnaður áður.</span><span class="sxs-lookup"><span data-stu-id="63ac0-281">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="63ac0-282">Veljið **Aðgangsstýringu (IAM)** og veljið síðan **Hlutverkaúthlutanir**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-282">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="63ac0-283">Veljið **Bæta við, Bæta við hlutverkaúthlutun**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-283">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="63ac0-284">Fyrir hvert forrit í eftirfarandi töflu skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="63ac0-284">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="63ac0-285">Velja skal hlutverkið úr eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="63ac0-285">Select the role from the following table.</span></span>
        2. <span data-ttu-id="63ac0-286">Hafið svæðið **Úthluta aðgangi að** stillt á **Azure AD-notanda, -hóp eða þjónustueiningu**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-286">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="63ac0-287">Á svæðinu **Velja** skal slá inn forrit úr eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="63ac0-287">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="63ac0-288">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-288">Select **Save**.</span></span>

        | <span data-ttu-id="63ac0-289">Forrit</span><span class="sxs-lookup"><span data-stu-id="63ac0-289">Application</span></span>                                              | <span data-ttu-id="63ac0-290">Hlutverk</span><span class="sxs-lookup"><span data-stu-id="63ac0-290">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="63ac0-291">Birtingarheiti nýja forritsins sem var búið til</span><span class="sxs-lookup"><span data-stu-id="63ac0-291">The display name of the new application that you created</span></span> | <span data-ttu-id="63ac0-292">Eigandi</span><span class="sxs-lookup"><span data-stu-id="63ac0-292">Owner</span></span>                       |
        | <span data-ttu-id="63ac0-293">Birtingarheiti nýja forritsins sem var búið til</span><span class="sxs-lookup"><span data-stu-id="63ac0-293">The display name of the new application that you created</span></span> | <span data-ttu-id="63ac0-294">Framlagsveitandi</span><span class="sxs-lookup"><span data-stu-id="63ac0-294">Contributor</span></span>                 |
        | <span data-ttu-id="63ac0-295">Birtingarheiti nýja forritsins sem var búið til</span><span class="sxs-lookup"><span data-stu-id="63ac0-295">The display name of the new application that you created</span></span> | <span data-ttu-id="63ac0-296">Geymslureikningsþátttakandi</span><span class="sxs-lookup"><span data-stu-id="63ac0-296">Storage Account Contributor</span></span> |
        | <span data-ttu-id="63ac0-297">Birtingarheiti nýja forritsins sem var búið til</span><span class="sxs-lookup"><span data-stu-id="63ac0-297">The display name of the new application that you created</span></span> | <span data-ttu-id="63ac0-298">Eigandi Blob-gagna í geymslu</span><span class="sxs-lookup"><span data-stu-id="63ac0-298">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="63ac0-299">**Heimildaþjónusta AI Builder**</span><span class="sxs-lookup"><span data-stu-id="63ac0-299">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="63ac0-300">Lesari Blob-gagna í geymslu</span><span class="sxs-lookup"><span data-stu-id="63ac0-300">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="63ac0-301">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="63ac0-301">Azure CLI</span></span>](#tab/azure-azure-cli)

```
function New-FinanceDataLakeAzureResources {
    Assert-ScriptSetup

    $ClientAppName = 'Finance Data Lake Application'
    $DefaultSecretExpiryInYear = 1
    $MicrosoftDynamicsERPMicroservicesAppId = '0cdb527f-a8d1-4bf8-9436-b352c68682b2'
    $MicrosoftDynamicsERPMicroservicesCDSAppId = '703e2651-d3fc-48f5-942c-74274233dba8'
    $AIBuilderAuthorizationServiceAppId = 'ad40333e-9910-4b61-b281-e3aeeb8c3ef3'
    $KeyVaultServicePrincipalAppId = 'cfa8b339-82a2-471a-a3c9-0fc0be7a4093'
    $GraphServicePrincipalAppId = '00000003-0000-0000-c000-000000000000'

    Import-Module AzureAD.Standard.Preview
    $connectAzureADParameters = @{ 'Identity' = $true; 'TenantId' = $env:ACC_TID }
    $azContext = AzureAD.Standard.Preview\Connect-AzureAD @connectAzureADParameters
    $userContext = ConvertFrom-Json ((az ad signed-in-user show) -join '')
    $user = Get-AzureADUser -Filter ("UserPrincipalName eq '" + $userContext.UserPrincipalName + "'")

    Set-AzureSubscription
    
    $resourceGroup = $null
    $ResourceGroupName = 'D365FinanceInsightsDataLake'
    $ResourceGroupNameSuffix = ''
    $FullResourceGroupName = ''
    Write-Output ("The default Azure Resource Group name is '{0}'" -f $ResourceGroupName)
    while (-not ($resourceGroup)) {
        $ResourceGroupNameSuffix = (Read-Host -Prompt "Enter optional Azure Resource Group name suffix: (leave blank for no suffix)")
        if ([string]::IsNullOrWhitespace($ResourceGroupNameSuffix))
        {
            $FullResourceGroupName = $ResourceGroupName
        }
        else
        {
            if ($ResourceGroupNameSuffix -notmatch "^[A-Za-z0-9]+$") {
                Write-Warning "The Azure Resource Group name suffix can only include alphanumeric characters."
                continue
            }

            if ($ResourceGroupNameSuffix.Length -gt 60) {
                Write-Warning "The Azure Resource Group name suffix cannot be longer than 60 characters."
                continue
            }

            $FullResourceGroupName = $ResourceGroupName + $ResourceGroupNameSuffix
        }
        
        $resourceGroup = Get-AzResourceGroup -Name $FullResourceGroupName -ErrorAction SilentlyContinue

        if (-not ($resourceGroup)) {
            Write-Output ("Your new Azure Resource Group name is '{0}'" -f $FullResourceGroupName)
            $resourceLocation = ''
            $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
            while ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations))) {
                $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
                if ($resourceLocation -eq 'help') {
                    Write-Output ("List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
                elseif ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations)))
                {
                    Write-Warning ("The provided location is not available for resource group. List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
            }
            $resourceGroup = New-AzResourceGroup -Name $FullResourceGroupName -Location $resourceLocation
            Write-Output ("Created Azure Resource Group '{0}'" -f $resourceGroup.ResourceGroupName)
        }
        else {
            Write-Output ("Found Azure Resource Group '{0}'" -f ($resourceGroup.ResourceGroupName))
        }
    }

    Write-Output '================================================================================='
    $MicrosoftDynamicsERPMicroservicesAppObjectId = Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId
    Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Out-Null
    $aibuilderAuthorizationServiceObjectId = Create-ADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId
    Write-Output ('=================================================================================')

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $ClientAppName + "'")
    if (-not ($clientAppSPN)) {
        $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        if (-not $keyVaultPrincipal)
        {
            New-AzureADServicePrincipal -AppId $KeyVaultServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Key Vault principal to AAD"
            $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        }
        $keyVaultAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $keyVaultAccess.ResourceAppId = $keyVaultPrincipal.AppId
        $keyVaultAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $keyVaultPrincipal.Oauth2Permissions.Id, "Scope")

        $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        if (-not $graphPrincipal)
        {
            New-AzureADServicePrincipal -AppId $GraphServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Graph principal to AAD"
            $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        }
        $userRead = $graphPrincipal.Oauth2Permissions | Where-Object { $_.Type -eq "User" -and $_.Value -eq "User.Read" }
        $graphAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $graphAccess.ResourceAppId = $graphPrincipal.AppId
        $graphAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $userRead.Id, "Scope")

        $clientApp = New-AzureADApplication -DisplayName $ClientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($ClientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $ClientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($DefaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    try {
        $deployment = New-AzResourceGroupDeployment -ResourceGroupName $FullResourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId -Force -ErrorAction Stop
    }
    catch {
        $ErrorMessage = $_.Exception.Message
        if ($ErrorMessage.Contains("not allowed to be updated"))
        {
            Write-Error ($ErrorMessage)
            Write-Warning "Some items in the existing resource group $FullResourceGroupName could not be updated. To resolve the issue, remove the existing resource group $FullResourceGroupName and run the script again."
        }
        else {
            throw
        }

    }
    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
        
        $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
        $tenantId = (Get-AzContext).Tenant.Id

        Write-Output "Values for LCS Data Lake Add-In:"
        Write-Output ("  Tenant ID:                         " + $tenantId)
        Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
        Write-Output "  Storage account secret name:       storage-account-name"
        Write-Output "  Application ID secret name:        app-id"
        Write-Output "  Application Secret secret name:    app-secret"
        Write-Warning "Copy this information for the LCS Add-in for easy access. Azure Cloud Shell will eventually time out and close."

        Write-Output '================================================================================='
        Write-Output "Values for System parameters > Data connections:"
        Write-Output ("  Application ID:                    " + $clientAppId)
        Write-Output ("  Application Secret:                " + $ClientAppSecret)
        Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
        Write-Output "  Secret name:                       storage-account-connection-string"
        Write-Warning "Copy this information for the System parameters for easy access. Azure Cloud Shell will eventually time out and close."
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $FullResourceGroupName)
    }
}

function Assert-ScriptSetup {
    if ($PSVersionTable.PSEdition -ne 'Core' -or -not $env:ACC_TID) { 
        throw "This script needs to be uploaded and run from Azure Cloud Shell (PowerShell)." 
    }
    
    if ((Get-AzContext) -eq $null -and (Connect-AzAccount) -eq $null) {
        throw 'Unable to connect to Azure account.'
    }
}

function Set-AzureSubscription {
    $azSubscription = $null
    while (-not ($azSubscription)) {
        $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (leave blank for default)")
        if ([string]::IsNullOrWhitespace($subscriptionId)){
            break
        }
        elseif (-not [guid]::TryParse($subscriptionId, $([ref][guid]::Empty))) {
                Write-Warning "Azure Subscription ID must be a valid GUID."
                continue
        }

        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }
}

function Create-ADServicePrincipal {
    param (
        [string] $AppId
    )

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AppId | Out-Null
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
        Write-Host ("Added AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }
    else {
        Write-Host ("Found AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }

    return $service.ObjectId
}

$azureTemplate = @"
{
    "contentVersion": "1.0.0.0",
    "parameters": {
      "aibuilderAppObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of the AI Builder application."
        }
      },
      "clientAppId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the application ID of client application."
        }
      },
      "clientAppSecret": {
        "type": "String",
        "metadata": {
          "description": "Specifies the Azure App ID client secret to in azure key vault."
        }
      },
      "clientAppSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of a client application service principal."
        }
      },
      "userSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of tenant admin service principal."
        }
      },
      "microserviceSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of Microsoft Dynamics ERP Microservices service principal."
        }
      },
      "storageAccountType": {
        "type": "string",
        "defaultValue": "Standard_LRS",
        "allowedValues": [
          "Standard_LRS",
          "Standard_GRS",
          "Standard_ZRS",
          "Premium_LRS"
        ],
        "metadata": {
          "description": "Storage Account type"
        }
      }
    },
    "variables": {
      "storageAccountApiVersion": "2019-06-01",
      "keyVaultApiVersion": "2018-02-14",
      "secretsPermissions": [
        "list",
        "get"
      ],
      "location": "[resourceGroup().location]",
      "storageAccountName": "[concat('store', uniquestring(resourceGroup().id))]",
      "keyVaultName": "[concat('keyvault', uniquestring(resourceGroup().id))]",
      "owner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '8e3af657-a8ff-443c-a75c-2fe8c4bcb635')]",
      "contributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b24988ac-6180-42a0-ab88-20f7382dd24c')]",
      "storageAccountContributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '17d1049b-9a84-46fb-8f53-869881c3d3ab')]",
      "storageBlobDataOwner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b7e6dc6d-f1e8-4753-8033-0f276bb0955b')]",
      "storageBlobDataReader": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '2a2b9908-6ea1-4ae2-8e65-a410df84e7d1')]"
    },
    "resources": [
      {
        "type": "Microsoft.Storage/storageAccounts",
        "apiVersion": "[variables('storageAccountApiVersion')]",
        "name": "[variables('storageAccountName')]",
        "location": "[variables('location')]",
        "sku": {
          "name": "[parameters('storageAccountType')]"
        },
        "kind": "StorageV2",
        "properties": {
          "accessTier": "Hot",
          "supportsHttpsTrafficOnly": true,
          "isHnsEnabled": true
        },
        "resources": [
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'1')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('owner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'2')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('contributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'3')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageAccountContributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'4')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataOwner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'5')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataReader')]",
              "principalId": "[parameters('aibuilderAppObjectId')]"
            }
          }
        ]
      },
      {
        "type": "Microsoft.KeyVault/vaults",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "name": "[variables('keyVaultName')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName'))]"
        ],
        "tags": {
        },
        "properties": {
          "enabledForDeployment": false,
          "enabledForTemplateDeployment": false,
          "enabledForDiskEncryption": false,
          "enableRbacAuthorization": false,
          "accessPolicies": [
            {
              "objectId": "[parameters('clientAppSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('microserviceSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('userSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            }
          ],
          "tenantId": "[subscription().tenantId]",
          "sku": {
            "name": "Standard",
            "family": "A"
          },
          "enableSoftDelete": false,
          "networkAcls": {
            "defaultAction": "Allow",
            "bypass": "AzureServices"
          }
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-id')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppId')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-secret')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppSecret')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-name')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[variables('storageAccountName')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-connection-string')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[concat('DefaultEndpointsProtocol=https;AccountName=', variables('storageAccountName'), ';AccountKey=', listKeys(resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName')), variables('storageAccountApiVersion')).keys[0].value, ';EndpointSuffix=core.windows.net')]"
        }
      }
    ],
    "outputs": {
      "storageAccountName": {
        "type": "string",
        "value": "[variables('storageAccountName')]"
      },
      "keyVaultName": {
        "type": "string",
        "value": "[variables('keyVaultName')]"
      }
    }
  }
"@

try {
  Start-Transcript -path (Join-Path $HOME Provision-FinInsights-Azure.log)
  New-FinanceDataLakeAzureResources
}
catch {
  Write-Error $_.Exception.Message

  if ($PSItem.Exception.StackTrace -ne $null)
  {
      Write-Warning $_.Exception.StackTrace
  }

  $inner = $_.Exception.InnerException
  while ($null -ne $inner) {
    Write-Output 'Inner Exception:'
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $inner.InnerException
  }
}
finally {
  Stop-Transcript
}

```
---



## <a name="configure-the-data-lake"></a><span data-ttu-id="63ac0-302">Skilgreina Data Lake</span><span class="sxs-lookup"><span data-stu-id="63ac0-302">Configure the data lake</span></span>

<span data-ttu-id="63ac0-303">Fylgið eftirfarandi skrefum til að nota LCS til að bæta Azure Data Lake-innbótinni við umhverfið.</span><span class="sxs-lookup"><span data-stu-id="63ac0-303">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="63ac0-304">Skráðu þig inn á LCS og veldu síðan **Allar upplýsingar**, undir heiti umhverfisins hægra megin á síðunni.</span><span class="sxs-lookup"><span data-stu-id="63ac0-304">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="63ac0-305">Í hlutanum **Innbætur umhverfis** skal velja **Setja upp nýja innbót**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-305">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="63ac0-306">Veljið innbótina **Flytja út í Data Lake**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-306">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="63ac0-307">Sláið inn eftirfarandi gildi.</span><span class="sxs-lookup"><span data-stu-id="63ac0-307">Enter the following values.</span></span>

    | <span data-ttu-id="63ac0-308">Virði</span><span class="sxs-lookup"><span data-stu-id="63ac0-308">Value</span></span>                                                              | <span data-ttu-id="63ac0-309">lýsing</span><span class="sxs-lookup"><span data-stu-id="63ac0-309">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="63ac0-310">Leigjandakenni Azure-áskriftar þar sem lyklageymsla er staðsett</span><span class="sxs-lookup"><span data-stu-id="63ac0-310">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="63ac0-311">Auðkenni leigjanda þar sem geymslureikningur, forrit og lyklageymslur eru staðsett.</span><span class="sxs-lookup"><span data-stu-id="63ac0-311">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="63ac0-312">Til að finna þetta gildi skal opna [Azure-gátt](https://portal.azure.com), **Azure Active Directory** og afrita gildi **leigjandakennis**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-312">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="63ac0-313">Gefðu upp DNS-heiti lyklageymslunnar</span><span class="sxs-lookup"><span data-stu-id="63ac0-313">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="63ac0-314">DNS-heiti lyklageymslu, t.d. `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="63ac0-314">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="63ac0-315">(Þetta gildi samsvarar DNS-heitinu sem er notað í einingaversluninni.)</span><span class="sxs-lookup"><span data-stu-id="63ac0-315">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="63ac0-316">Gefðu upp leyndarmálið sem inniheldur heiti geymslureikningsins</span><span class="sxs-lookup"><span data-stu-id="63ac0-316">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="63ac0-317">**geymsla-reikningur-heiti**</span><span class="sxs-lookup"><span data-stu-id="63ac0-317">**storage-account-name**</span></span> |
    | <span data-ttu-id="63ac0-318">Leyniheiti fyrir forritskenni sem verður notað til að fá aðgang að Data Lake</span><span class="sxs-lookup"><span data-stu-id="63ac0-318">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="63ac0-319">**forrit-auðkenni**</span><span class="sxs-lookup"><span data-stu-id="63ac0-319">**app-id**</span></span> |
    | <span data-ttu-id="63ac0-320">Leyniheiti sem verður notað með forritskenni</span><span class="sxs-lookup"><span data-stu-id="63ac0-320">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="63ac0-321">**forrit-leyndarmál**</span><span class="sxs-lookup"><span data-stu-id="63ac0-321">**app-secret**</span></span> |

5. <span data-ttu-id="63ac0-322">Samþykkið skilmálana og veljið **Setja upp**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-322">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="63ac0-323">Viðbótin verður sett upp innan fárra mínútna.</span><span class="sxs-lookup"><span data-stu-id="63ac0-323">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="63ac0-324">Skilgreina AI Builder</span><span class="sxs-lookup"><span data-stu-id="63ac0-324">Configure AI Builder</span></span>

1. <span data-ttu-id="63ac0-325">Skráðu þig inn á LCS og opnaðu síðuna **Umhverfisupplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-325">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="63ac0-326">Flettu að hlutanum **Innbætur umhverfis**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-326">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="63ac0-327">Þú ættir að sjá innbæturnar sem eru þegar settar upp í þessu umhverfi.</span><span class="sxs-lookup"><span data-stu-id="63ac0-327">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="63ac0-328">Ef innbótin **Flytja út í Data Lake** er ekki á meðal þeirra skal skilgreina þessa innbót.</span><span class="sxs-lookup"><span data-stu-id="63ac0-328">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="63ac0-329">Veljið innbótina **Fá innsýn**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-329">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="63ac0-330">Sláið inn eftirfarandi gildi á upplýsingasíðu innbótarinnar **Fá innsýn**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-330">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="63ac0-331">Virði</span><span class="sxs-lookup"><span data-stu-id="63ac0-331">Value</span></span>                                                    | <span data-ttu-id="63ac0-332">lýsing</span><span class="sxs-lookup"><span data-stu-id="63ac0-332">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="63ac0-333">CDS-vefslóð fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="63ac0-333">CDS Organization URL</span></span>                                     | <span data-ttu-id="63ac0-334">Vefslóð Dataverse-fyrirtækis Dataverse-tilviksins.</span><span class="sxs-lookup"><span data-stu-id="63ac0-334">The Dataverse organization URL of the Dataverse instance.</span></span> <span data-ttu-id="63ac0-335">Til að finna þetta gildi skal opna [Power Apps-gátt](https://make.powerapps.com), velja hnappinn **Stillingar** (gírtáknið) efst til hægri, velja **Ítarlegar stillingar** og afrita vefslóðina.</span><span class="sxs-lookup"><span data-stu-id="63ac0-335">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Advanced settings**, and copy the URL.</span></span> <span data-ttu-id="63ac0-336">(Slóðin endar á „dynamics.com“.)</span><span class="sxs-lookup"><span data-stu-id="63ac0-336">(The URL ends with "dynamics.com.")</span></span> |
    | <span data-ttu-id="63ac0-337">Auðkenni CDS-fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="63ac0-337">CDS Org ID</span></span>                                               | <span data-ttu-id="63ac0-338">Umhverfiskenni Dataverse tilviksins.</span><span class="sxs-lookup"><span data-stu-id="63ac0-338">The environment ID of the Dataverse instance.</span></span> <span data-ttu-id="63ac0-339">Til að finna þetta gildi skal opna [Power Apps-gátt](https://make.powerapps.com), velja hnappinn **Stillingar** (gírtáknið) efst til hægri, velja **Sérstillingar \> Þróunartilföng \> Tilvísunarupplýsingar tilviks** og afrita gildið í **Auðkenni**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-339">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Customizations \> Developer resources \> Instance Reference Information**, and copy the **ID** value.</span></span> |
    | <span data-ttu-id="63ac0-340">Leigjandakenni CDS (skráasafnskenni úr AAD)</span><span class="sxs-lookup"><span data-stu-id="63ac0-340">CDS Tenant ID (Directory ID from AAD)</span></span>               | <span data-ttu-id="63ac0-341">Auðkenni leigjanda Dataverse tilviksins</span><span class="sxs-lookup"><span data-stu-id="63ac0-341">The tenant ID of the Dataverse instance.</span></span> <span data-ttu-id="63ac0-342">Til að finna þetta gildi skal opna [Azure-gátt](https://portal.azure.com), **Azure Active Directory** og afrita gildi **leigjandakennis**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-342">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="63ac0-343">Veita notanda hlutarkenni sem er með stjórnandahlutverk</span><span class="sxs-lookup"><span data-stu-id="63ac0-343">Provide user object ID who has system administrator role</span></span> | <span data-ttu-id="63ac0-344">Auðkenni Azure AD-notandahlutarins í Dataverse.</span><span class="sxs-lookup"><span data-stu-id="63ac0-344">The Azure AD user object ID of the user in Dataverse.</span></span> <span data-ttu-id="63ac0-345">Þessi notandi verður að vera kerfisstjóri Dataverse-tilviks.</span><span class="sxs-lookup"><span data-stu-id="63ac0-345">This user must be a system administrator of the Dataverse instance.</span></span> <span data-ttu-id="63ac0-346">Til að finna þetta gildi skal opna [Azure-gátt](https://portal.azure.com), opna **Azure Active Directory \> Notendur**, velja notandann og síðan, í **Auðkenni** , afrita gildið fyrir **Hlutarkenni**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-346">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory \> Users**, select the user, and then, in the **Identity** section, copy the **Object ID** value.</span></span> |
    | <span data-ttu-id="63ac0-347">Er þetta sjálfgefna CDS-umhverfið fyrir leigjandann?</span><span class="sxs-lookup"><span data-stu-id="63ac0-347">Is this the default CDS environment for the tenant?</span></span>      | <span data-ttu-id="63ac0-348">Ef Dataverse-tilvik var fyrsta framleiðslutilvikið sem var stofnað skal velja þennan gátreit.</span><span class="sxs-lookup"><span data-stu-id="63ac0-348">If the Dataverse instance was the first production instance that was created, select this check box.</span></span> <span data-ttu-id="63ac0-349">Ef Dataverse tilvik var búið til handvirkt skal hreinsa þennan gátreit.</span><span class="sxs-lookup"><span data-stu-id="63ac0-349">If the Dataverse instance was manually created, clear this check box.</span></span> |

## <a name="configure-the-entity-store"></a><span data-ttu-id="63ac0-350">Grunnstilla einingaverslun</span><span class="sxs-lookup"><span data-stu-id="63ac0-350">Configure the entity store</span></span>

<span data-ttu-id="63ac0-351">Fylgið eftirfarandi skrefum til að setja upp einingaverslunina í Finance-umhverfinu.</span><span class="sxs-lookup"><span data-stu-id="63ac0-351">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="63ac0-352">Opnið **Kerfisstjórnun\> Uppsetning\> Kerfisfæribreytur \> Gagnatengingar**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-352">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="63ac0-353">Stillið **Virkja Data Lake-samþættingu** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-353">Set the **Enable Data Lake integration** option to **Yes**.</span></span>
3. <span data-ttu-id="63ac0-354">Stillið eftirfarandi lyklageymslusvæði:</span><span class="sxs-lookup"><span data-stu-id="63ac0-354">Set the following key vault fields:</span></span>

    - <span data-ttu-id="63ac0-355">**Forritskenni (biðlari)** – Sláið inn auðkenni forritsbiðlara sem var stofnaður áður.</span><span class="sxs-lookup"><span data-stu-id="63ac0-355">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="63ac0-356">**Leynilykill forrits** – Sláið inn leynilykil sem vistaður var fyrir forritið sem stofnað var áður.</span><span class="sxs-lookup"><span data-stu-id="63ac0-356">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="63ac0-357">**DNS-heiti** – Hægt er að finna heiti lénsheitakerfis á upplýsingasíðu forrits fyrir forritið sem var stofnað áður.</span><span class="sxs-lookup"><span data-stu-id="63ac0-357">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="63ac0-358">**Leynilykilsheiti** – Sláið inn **geymsla-reikningur-tenging-strengur**.</span><span class="sxs-lookup"><span data-stu-id="63ac0-358">**Secret name** – Enter **storage-account-connection-string**.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="63ac0-359">Ábendingar og stuðningur</span><span class="sxs-lookup"><span data-stu-id="63ac0-359">Feedback and support</span></span>

<span data-ttu-id="63ac0-360">Sendið tölvupóst á [Innsýn í greiðslur viðskiptavinar (forskoðun)](mailto:fiap@microsoft.com) ef áhugi er á að senda inn ábendingar eða aðstoð vantar.</span><span class="sxs-lookup"><span data-stu-id="63ac0-360">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="63ac0-361">Tilkynning um persónuvernd</span><span class="sxs-lookup"><span data-stu-id="63ac0-361">Privacy notice</span></span>

<span data-ttu-id="63ac0-362">Forútgáfur (1) kunna að nota minni persónuverndar- og öryggisráðstafanir og þjónusta Dynamics 365 Finance and Operations, (2) eru ekki hluti af þjónustustigssamningi fyrir þessa þjónustu, (3) ættu ekki að vera notaðar til að vinna úr persónulegum gögnum eða öðrum gögnum sem falla undir lögboðnar kröfur eða reglur um samræmi og (4) hafa takmarkaðan stuðning.</span><span class="sxs-lookup"><span data-stu-id="63ac0-362">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
