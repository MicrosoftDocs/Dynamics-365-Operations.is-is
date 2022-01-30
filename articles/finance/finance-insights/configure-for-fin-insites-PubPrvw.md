---
title: Stillingar fyrir fjármálainnsýn - útgáfa 10.0.20 og síðar
description: Þetta efnisatriði útskýrir hvernig á að stilla kerfið þitt til að nota þá möguleika sem eru tiltækir í Finance Insights í útgáfu 10.0.20 og síðar.
author: ShivamPandey-msft
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex,nofollow
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-06-03
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 8ff20334445fba1db435d7005c4ca9ba18f97f72
ms.sourcegitcommit: 133aa728b8a795eaeaef22544f76478da2bd1df9
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968963"
---
# <a name="configuration-for-finance-insights---version-10020-and-later"></a>Stillingar fyrir fjármálainnsýn - útgáfa 10.0.20 og síðar

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Fjármálainnsýn sameinar virkni frá Microsoft Dynamics 365 Finance með Dataverse, Azure og AI Builder til að bjóða upp á öflug spáverkfæri fyrir fyrirtæki þitt. Þetta efni útskýrir hvernig á að stilla Dynamics 365 Finance útgáfu 10.0.20 svo að kerfið þitt geti notað þá möguleika sem eru í boði í Finance Insights.

> [!NOTE]
> Skrefum skilgreiningarinnar sem lýst í þessu efnisatriði eiga aðeins við um útgáfu 10.0.20 og nýrri af Finance. Til að setja upp fjármálainnsýn á útgáfu 10.0.19 og eldri skal sjá [Stilling fjármálainnsýnar - útgáfur fram að 10.0.19](configure-for-fin-insites.md).

## <a name="deploy-finance"></a>Uppsetning Finance

Fylgja skal eftirfarandi skrefum til að setja upp umhverfin.

1. Í Microsoft Dynamics Lifecycle Services (LCS) skal stofna eða uppfæra Finance-umhverfi. Umhverfið krefst forritaútgáfu 10.0.20 eða nýrra af Finance and Operations forritum.
2. Umhverfið verður að vera vel tiltækt í Sandbox. (Þessi tegund umhverfis er einnig þekkt sem umhverfi í tveggja laga umhverfi.) Frekari upplýsingar er að finna í [Umhverfisskipulagning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
3. Ef þú ert að stilla fjármálainnsýn í sandkassaumhverfi gætirðu þurft að afrita framleiðslugögn í það umhverfi til að spár virki. Spálíkanið notar gögn til margra ára til að búa til spár. Contoso kynningargögnin innihalda ekki nógu mörg söguleg gögn til að þjálfa spálíkanið á fullnægjandi hátt. 

## <a name="configure-dataverse"></a>Skilgreina Dataverse

Fylgdu eftirfarandi skrefum til að stilla Dataverse fyrir fjármálainnsýn.

1. Í LCS skal opna síðu umhverfis og staðfesta að hlutinn **Power Platform samþætting** sé þegar uppsettur.

    - Ef hann er þegar uppsettur ætti heiti Dataverse umhverfisins sem tengt er við Finance-umhverfið að vera sýnt.
    - Ef það er ekki enn uppsett skaltu fylgja þessum skrefum:

        1. Í hlutanum **Power Platform samþætting** skal velja **Uppsetning**. Uppsetning umhverfisins getur tekið allt að klukkustund.
        2. Ef tókst að setja upp Dataverse-umhverfið ætti heiti Dataverse-umhverfisins sem tengt er við Finance-umhverfið að vera sýnt.

        > [!NOTE]
        > Eftir að uppsetningu umhverfisins er lokið skal **ekki** velja **Tengja við CDS fyrir forrit**. Þessi hnappur er ekki nauðsynlegur fyrir fjármálainnsýn. Ef þú velur hann geturðu ekki stillt nauðsynlegar innbætur við umhverfi í LCS.

## <a name="configure-azure"></a>Stilla Azure

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a>Nota Azure Cloud Shell til að setja upp Data Lake-tilföng fjármálainnsýnar

# <a name="use-a-windows-powershell-script"></a>[Nota Windows PowerShell-forskrift](#tab/use-a-powershell-script)

Boðið er upp á Windows PowerShell-forskrift þannig að auðvelt er að setja upp Azure-tilföng sem eru skilgreind í [Grunnstilla útflutning í Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md). Ef frekar er óskað eftir því að setja upp handvirkt skal sleppa þessu ferli og í staðinn ljúka ferlinu í hlutanum [Handvirk uppsetning](#manual-setup).

> [!NOTE]
> Notið eftirfarandi ferli til að keyra forskrift Windows PowerShell. Uppsetningin virkar hugsanlega ekki ef valkosturinn **Prófaðu þetta** í Azure CLI er notaður eða ef forskriftin er keyrð í tölvunni þinni.

Fylgið þessum skrefum til að nota forskrift Windows PowerShell til að stilla Azure. Réttindi til að búa til Azure-tilfangaflokk, Azure-tilföng og Azure AD-forrit þurfa að vera til staðar. Frekari upplýsingar um nauðsynlegar heimildir má finna á [Athuga Azure AD heimildir](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).

1. Í [Azure-gátt](https://portal.azure.com) skal opna viðkomandi Azure-áskrift.
2. Veljið **Cloud Shell** hægra megin við svæðið **Leita**.
3. Veljið **PowerShell**.
4. Búðu til geymslu ef beðið er um að búa hana til.
5. Á flipanum **Azure CLI** skal velja **Afrita**.
6. Opnið nýja skrá í Notepad og límið inn Windows PowerShell-forskriftina.
7. Vistið skrána sem **ConfigureDataLake.ps1**.
8. Hlaðið upp forskrift Windows PowerShell í lotuna með því að nota valkost valmyndar fyrir upphleðslu í Cloud Shell.
9. Keyrið **.\ConfigureDataLake.ps1** forskriftina.
10. Fylgið kvaðningunum til að keyra forskriftina.
11. Notið upplýsingar úr forskriftinni til að setja upp innbótina Flytja út í Data Lake í LCS.

### <a name="manual-setup"></a>Handvirk uppsetning

#### <a name="add-applications-to-the-azure-ad-tenant"></a>Bæta umsóknum við Azure AD leigjanda

1. Í [Azure-gáttinni](https://portal.azure.com) skal fara á **Azure Active Directory**.
2. Veljið **Stjórna \> Enterprise-forrit**.
3. Leitið að eftirfarandi forritum eftir FORRITSKENNINU.

    | Forrit                              | Auðkenni forrits                               |
    |------------------------------------------|--------------------------------------|
    | Microsoft Dynamics ERP Microservices     | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
    | Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |
    | AI Builder Leyfisþjónusta         | ad40333e-9910-4b61-b281-e3aeeb8c3ef3 |

Ef ekki eitthvað af undanfarandi forritum finnst ekki skal prófa eftirfarandi skref.

1. Í staðbundinni tölvu, í **Upphafsvalmyndinni**, skal leita að **powershell**.
2. Velja skal og halda fingri á (eða hægrismella) **Windows PowerShell** og velja svo **Keyra sem stjórnandi**.
3. Keyrið eftirfarandi skipun til að setja upp **AzureAD** einingun.

    `Install-Module -Name AzureAD`

4. Ef NuGet-veita er nauðsynleg til að halda áfram skal velja **Y** til að setja hana upp.
5. Ef skilaboðin „Ótraust geymslׅa“ birtast skal velja **Y** til að halda áfram.
6. Fyrir hvert forrit sem verður að bæta við þarf að keyra eftirfarandi skipanir til að bæta forritinu við Azure AD. Skráðu þig inn sem stjórnandi Azure AD þegar beðið er um það.

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a>Stofna Azure-tilföng

> [!NOTE]
> Ganga skal úr skugga um að eftirfarandi tilföng séu stofnuð í sama Azure AD-tilviki og Dataverse-umhverfið er í. Ekki er hægt að nota tilföng úr öðru Azure AD-tilviki.

1. Búið til geymslureikning:

    1. Í [Azure Portal](https://portal.azure.com) skal stofna geymslureikning.
    2. Í svarglugganum **Stofna geymslureikning** skal stilla eftirfarandi svæði:

        - **Staðsetning** – velja gagnamiðstöð með umhverfinu.
        - **Afköst** – mælt er með **Hefðbundin**.
        - **Reikningsgerð** – velja þarf **StorageV2**.

    3. Í svarglugganum **Ítarlegir valkostir**, fyrir **Data Lake Storage Gen2**, skal velja **Virkja** undir **Stigveldis nafnabil**. Ef þú virkjar ekki þennan eiginleika geturðu ekki neytt gagna sem Finance and Operations forrit skrifa með því að nota þjónustu eins og Power BI gagnaflæði.
    4. Veljið **yfirfara og búa til**. Þegar uppsetningu er lokið sést nýja tilfangið til staðar á Azure-gáttinni.
    5. Opnaðu geymslureikninginn sem þú stofnaðir.
    6. Á valmyndinni til vinstri skal velja **Aðgangslyklar**.
    7. Afritið og vistið heiti geymslureikningsins. Gefa verður upp gildið síðar þegar leyndarmál lyklageymslu er sett upp.

2. Búið til lyklageymslu:

    1. Í [Azure Portal](https://portal.azure.com) skal stofna lyklageymslu.
    2. Í svarglugganum **Stofna lyklageymslu** á svæðinu **Staðsetning** skal velja gagnamiðstöðina þar sem umhverfið er að finna.
    3. Þegar lyklageymsla hefur verið búin til skal fara í **Yfirlit lyklageymslu** og afrita og vista DNS-heitið. Þetta gildi þarf að gefa upp síðar þegar Data Lake-viðbótin er sett upp.

3. Stofna og skrá Azure AD forrit:

    1. Í [Azure-gáttinni](https://portal.azure.com) skal opna **Azure Active Directory** og velja svo **Forritaskráningar**.
    2. Velja skal **Ný forritaskráning** og stilla eftirfarandi svæði:

        - **Heiti** - Færið inn heiti forritsins.
        - **Forritsgerð** – Veljið **Vef-API**.
        - **Framsenda URI-uppsetningu** – Sláið inn vefslóð fyrir Dynamics 365-tilvikið, til dæmis, `https://yourdynamicsinstance.dynamics.com/auth`.

    3. Opnið forritið sem var búið til og afritið og vistið gildi fyrir **Forritskenni (biðlari)**. Gefa verður upp gildið síðar þegar leyndarmál lyklageymslu er sett upp.
    4. Farið í **API-heimildir** og fylgið eftirfarandi skrefum:

        1. Veljið **Bæta við heimild**.
        2. Veljið **Azure Key Vault**.
        3. Þegar búið er að velja úthlutaðar heimildir skal velja **Notandi\_Eftirlíking**.
        4. Veldu **Bæta við heimildum**.

    5. Á valmyndinni fyrir forritið skal velja **Vottorð \& Leynilykar** og síðan skal fylgja þessum skrefum til að búa til leynilykla lyklageymslu:

        1. Veljið **Nýtt leyniorð biðlara**.
        2. Í reitnum **Lyklalýsing** skal færa inn heiti.
        3. Veljið tímalengd og svo **Bæta við**. Leynilykill er myndaður á svæðinu **Gildi**.
        4. Afritaðu og vistaðu leyniorð biðlara. Gefa verður upp gildið síðar þegar leyndarmál lyklageymslu er sett upp.

4. Stofna leynilykla lyklageymslu:

    1. Opnið lyklageymsluna sem stofnuð var áður og veljið **Leynilyklar**.
    2. Fyrir hvert heiti leynilykils í eftirfarandi töflu skal fylgja þessum skrefum:

        1. Veljið **Mynda/Flytja inn**.
        2. Á síðunni **Stofna leynilykil**, á svæðinu **Valkostir upphleðslu**, skal velja **Handvirkt**.
        3. Búið til leyniheitið og gildið úr töflunni.
        4. Veljið **Virkjað** og veljið síðan **Búa til**. Leynilykillinn er stofnaður og bætt við Lyklageymslu.

        | Leyniheiti                       | Leynilykill                                                                                 |
        |-----------------------------------|----------------------------------------------------------------------------------------------|
        | forrit-auðkenni                            | Forritskenni forritsins sem var stofnað áður.                                      |
        | forrit-leyndarmál                        | Leyndarmál biðlarans sem var vistað áður.                                                    |
        | geymsla-reikningur-heiti              | Heiti geymslureikningsins sem var stofnaður áður, t.d. **storageaccount1**.       |

5. Heimila forriti aðgang að lyklageymslu:

    1. Í [Azure-gátt](https://portal.azure.com) skal opna lyklageymsluna sem var stofnuð áður.
    2. Velja aðgangsstefnur.
    3. Fyrir hvert forrit í eftirfarandi töflu skal fylgja þessum skrefum:

        1. Veljið **Bæta við aðgangsreglu** til að búa til aðgangsreglu.
        2. Á svæðinu **Heimildir leynilykils** skal velja heimildir úr töflunni.
        3. Á svæðinu **Velja aðalreikning** skal leita að birtingarheiti forrits sem birtist í töflunni.
        4. Veljið **Velja**.
        5. Veljið **Bæta við**.
        6. Veldu **Vista**.

        | Forrit                                              | Aðgangsheimildir |
        |----------------------------------------------------------|-------------|
        | Birtingarheiti nýja forritsins sem var búið til | Sækja, listi   |
        | **Microsoft Dynamics ERP Microservices**                 | Sækja, listi   |

6. Úthluta hlutverkum til að fá aðgang að geymslureikningi:

    1. Í [Azure-gáttinni](https://portal.azure.com) skal opna geymslureikninginn sem var stofnaður áður.
    2. Veljið **Aðgangsstýringu (IAM)** og veljið síðan **Hlutverkaúthlutanir**.
    3. Veljið **Bæta við, Bæta við hlutverkaúthlutun**.
    4. Fyrir hvert forrit í eftirfarandi töflu skal fylgja þessum skrefum:

        1. Veljið hlutverkið úr töflunni.
        2. Hafið svæðið **Úthluta aðgangi að** stillt á **Azure AD-notanda, -hóp eða þjónustueiningu**.
        3. Í reitnum **Velja** skal slá inn forritið úr töflunni.
        4. Veldu **Vista**.

        | Forrit                                              | Hlutverk                        |
        |----------------------------------------------------------|-----------------------------|
        | Birtingarheiti nýja forritsins sem var búið til | Eigandi                       |
        | Birtingarheiti nýja forritsins sem var búið til | Framlagsveitandi                 |
        | Birtingarheiti nýja forritsins sem var búið til | Geymslureikningsþátttakandi |
        | Birtingarheiti nýja forritsins sem var búið til | Eigandi Blob-gagna í geymslu     |
        | **AI Builder Leyfisþjónusta**                     | Lesari Blob-gagna í geymslu    |

# <a name="azure-cli"></a>[Azure CLI](#tab/azure-azure-cli)

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

## <a name="configure-the-export-to-data-lake-add-in"></a>Stilla innbótina Flytja út í Data Lake

Fylgið eftirfarandi skrefum til að nota LCS til að bæta útflutningi við Azure Data Lake-innbótinni við umhverfið.

1. Skráðu þig inn á LCS og veldu síðan **Allar upplýsingar**, undir heiti umhverfisins hægra megin á síðunni.
2. Í hlutanum **Innbætur umhverfis** skal velja **Setja upp nýja innbót**.
3. Veljið innbótina **Flytja út í Data Lake**.
4. Sláið inn eftirfarandi gildi.

    | Virði                                                              | lýsing |
    |--------------------------------------------------------------------|-------------|
    | Leigjandakenni Azure-áskriftar þar sem lyklageymsla er staðsett | Auðkenni leigjanda þar sem geymslureikningur, forrit og lyklageymslur eru staðsett. Til að finna þetta gildi skal opna [Azure-gátt](https://portal.azure.com), **Azure Active Directory** og afrita gildi **leigjandakennis**. |
    | Gefðu upp DNS-heiti lyklageymslunnar                             | DNS-heiti lyklageymslu, t.d. `https://customkeyvault.vault.azure.net/`. |
    | Gefðu upp leyndarmálið sem inniheldur heiti geymslureikningsins   | **geymsla-reikningur-heiti** |
    | Leyniheiti fyrir forritskenni sem verður notað til að fá aðgang að Data Lake          | **forrit-auðkenni** |
    | Leyniheiti fyrir leyniorð biðlara í forriti                                  | **forrit-leyndarmál** |

5. Samþykkið skilmálana og veljið svo **Setja upp**.

Viðbótin verður sett upp innan fárra mínútna.

## <a name="configure-the-finance-insights-add-in"></a>Stilla innbót fjármálainnsýnar

> [!NOTE]
> Ef búið er að setja upp innbótina fyrir Fá innsýn skal fjarlægja hana áður en eftirfarandi ferli er klárað.

Fylgið þessum skrefum til að setja upp innbót fjármálainnsýnar.

1. Skráðu þig inn á LCS og veldu síðan **Allar upplýsingar**, undir heiti umhverfisins hægra megin á síðunni.
2. Í hlutanum **Innbætur umhverfis** skal velja **Setja upp nýja innbót**.
3. Veljið innbótina **Fjármálainnsýn**.
4. Samþykkið skilmálana og veljið svo **Setja upp**.

Það gæti tekið nokkrar mínútur að setja innbótina upp.

## <a name="feedback-and-support"></a>Ábendingar og stuðningur

Ef þú hefur áhuga á að veita endurgjöf, eða ef þú þarft aðstoð, sendu tölvupóst á [Innsýn í fjármálum](mailto:fiap@microsoft.com).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
