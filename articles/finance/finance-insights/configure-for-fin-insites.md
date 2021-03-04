---
title: Stillingar fyrir Fjármálainnsýn (forútgáfa)
description: Þetta efnisatriði útskýrir grunnstillingarskref sem mun gera kerfinu kleift að nota þá eiginleika sem eru í boði í Fjármálainnsýn.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 38cdeb9110691e594b4b90fc5bc79e369c9f4707
ms.sourcegitcommit: 1cfd6e0c808341b0f5bafbde7d04b0255b27352f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/02/2020
ms.locfileid: "4664091"
---
# <a name="configuration-for-finance-insights-preview"></a>Stillingar fyrir Fjármálainnsýn (forútgáfa)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Fjármálainnsýn sameinar virkni Microsoft Dynamics 365 Finance við Common Data Service, Azure og AI Builder til að bjóða upp á öflug spáverkfæri fyrir fyrirtækið. Þetta efnisatriði útskýrir grunnstillingarskref sem mun gera kerfinu kleift að nota þá eiginleika sem eru í boði í Fjármálainnsýn.

## <a name="deploy-dynamics-365-finance"></a>Virkja Dynamics 365 Finance

Virkjaðu umhverfið með því að fylgja þessum skrefum.

1. Í Microsoft Dynamics Lifecycle Services (LCS) skal búa til eða uppfæra Dynamics 365 Finance umhverfi. Umhverfið krefst forritsútgáfu 10.0.11/Verkvangsuppfærslu 35 eða nýrra.
2. Umhverfið verður að vera vel tiltækt í Sandbox. (Þessi tegund umhverfis er einnig þekkt sem umhverfi í tveggja laga umhverfi.) Frekari upplýsingar er að finna í [Umhverfisskipulagning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
3. Ef verið er að nota Contoso-sýnigögnin þarf viðbótarsýnigögn til að nota greiðsluspá viðskiptavinar, sjóðstreymisspár og fjárhagsáætlunarspár. 

## <a name="configure-common-data-service"></a>Skilgreina Common Data Service

Hægt er að ljúka við handvirk grunnstillingarskref sem fylgja, eða hægt er að hraða skilgreiningarferlinu með því að nota Windows PowerShell-forskrift sem er gefin upp. Þegar PowerShell-forskrift hefur verið keyrð mun það gefa upp gildi sem eru notuð til að skilgreina Fjármálainnsýn. 

> [!NOTE]
> Opnaðu PowerShell í tölvunni til að keyra skriftuna. Þú gætir þurft PowerShell útgáfu 5. Valkosturinn „Prófaðu þetta“ í Microsoft Azure CLI virkar hugsanlega ekki.

# <a name="manual-configuration-steps"></a>[Handvirk grunnstillingarskref](#tab/configuration-steps)

1. Opnaðu [Power Platform stjórnendamiðstöð ](https://admin.powerplatform.microsoft.com/) og fylgdu þessum skrefum til að búa til nýtt Common Data Service -umhverfi í sama Active Directory leigjanda:

    1. Opnið síðuna **Umhverfi**.

        [![Umhverfissíða](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)

    2. Veljið **Nýtt umhverfi**.
    3. Í reitnum **Gerð** skal velja **Sandkassi**.
    4. Stillið **Búa til gagnagrunn** valkostinn á **Já**.
    5. Veljið **Næst**.
    6. Velja tungumál og gjaldmiðil fyrirtækisins.
    7. Samþykkið sjálfgildin fyrir önnur svæði.
    8. Veljið **Vista**.
    9. Endurhlaða þarf síðuna **Umhverfi** .
    10. Bíða skal þar til gildið fyrir reitinn **Staða** er uppfært í **Tilbúið**.
    11. Skráið niður Common Data Service kenni fyrirtækis.
    12. Veljið umhverfi og svo **Stillingar**.
    13. Veljið **Tilföng \> Allar eldri stillingar**.
    14. Á efstu yfirlitsstikunni skal velja **Stillingar** og síðan **Sérstillingar**.
    15. Veljið **Tilföng fyrir þróunaraðila**.
    16. Stilla skal reitinn **Auðkenni tilvísunarupplýsingar tilviks** á gildi Common Data Service-fyrirtækiskennis sem skráð var áður.
    17. Í veffangastikunni vafrans skal gera athugasemd við VEFSLÓÐINA fyrir Common Data Service-fyrirtækið. Til dæmis gæti vefslóðin verið `https://org42b2b3d3.crm.dynamics.com`.

2. Ef ætlunin er að nota sjóðstreymisspár eða fjárhagsáætlunarspár skal fylgja þessum skrefum til að uppfæra skýringartextamörk fyrirtækisins í að minnsta kosti 50 megabæt (MB):

    1. Opnið [Power Apps-gáttina](https://make.powerapps.com)
    2. Veljið það umhverfi sem var stofnað og veljið síðan **Ítarlegar stillingar**.
    3. Veljið **Stillingar\> Skilgreining tölvupósts**.
    4. Breytið gildi **Hámarksstærð skráar** reitnum í **51.200**. (Gildið er gefið upp í kílóbætum \[KB\].)
    5. Veljið **Í lagi** til að vista breytingarnar.

# <a name="windows-powershell-configuration-script"></a>[Forskrift Windows PowerShell-skilgreiningar](#tab/powershell-configuration-script)

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

## <a name="configure-the-azure-setup"></a>Skilgreina Azure uppsetningu

### <a name="enter-the-common-data-service-directory-id-and-the-users-azure-ad-object-id"></a>Sláið inn Common Data Service skráarkenni og hlutarkenni Azure AD notandans

1. Sláið inn Common Data Service skráasafnskenni:

    1. Opnið [Azure-gáttina](https://portal.azure.com)
    2. Skráðu þig inn með því að nota NOTANDAKENNIÐ sem var notað til að búa til Common Data Service-umhverfið.
    3. Opnið **Azure Active Directory**.
    4. Afritið gildið **Leigjandakenni**.

2. Færa inn auðkenni hlutar notanda Azure Active Directory (Azure AD):

    1. Í [Azure-gátt](https://portal.azure.com) skal opna **Notendur** og leita að notandanum eftir netfangi.
    2. Færið inn nafn notanda.
    3. Afritið **Hlutarkenni** gildið.

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a>Nota Azure Cloud Shell til að setja upp Data Lake-tilföng fjármálainnsýnar

# <a name="use-a-windows-powershell-script"></a>[Nota Windows PowerShell-forskrift](#tab/use-a-powershell-script)

Boðið er upp á Windows PowerShell-forskrift þannig að auðvelt er að setja upp Azure-tilföng sem eru skilgreind í [Grunnstilla útflutning í Azure Data Lake](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/configure-export-data-lake). Ef óskað er eftir því að setja upp handvirkt skal sleppa þessu ferli og halda áfram með ferlið í hlutanum [Handvirk uppsetning](#manual-setup).

> [!NOTE]
> Fylgið skrefunum hér að neðan til að keyra PowerShell-forskrift. Hugsanlega virkar ekki valkosturinn „Prófaðu þetta“ í Azure CLI eða ekki er hægt að keyra þessa forskrift á tölvunni.

Fylgið eftirfarandi skrefum til að grunnstilla Azure með Windows PowerShell-forskriftinni. Réttindi til að búa til Azure-tilfangaflokk, Azure-tilföng og Azure AD-forrit þurfa að vera til staðar. Frekari upplýsingar um nauðsynlegar heimildir má finna á [Athuga Azure AD heimildir](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).

1. Í [Azure-gátt](https://portal.azure.com) skal opna viðkomandi Azure-áskrift. Veljið **Cloud Shell**-hnappinn hægra megin við svæðið **Leita**.
2. Veljið **PowerShell**.
3. Búðu til geymslu, ef beðið er um að gera það. Því næst skal hlaða upp Windows PowerShell-forskrift á lotuna.
4. Keyra forskrift.
5. Fylgið kvaðningunum til að keyra forskriftina.
6. Notið upplýsingar úr forskriftinni til að setja upp innbótina **Flytja út í Data Lake** í LCS.
7. Notið upplýsingar úr forskriftinni til að virkja einingaverslunina á síðunni **Gagnatengingar** í Finance (**Kerfisstjórnun \> Kerfisfæribreytur \> Gagnatengingar**).

### <a name="manual-setup"></a>Handvirk uppsetning

#### <a name="add-applications-to-the-azure-ad-tenant"></a>Bæta umsóknum við Azure AD leigjanda

1. Í [Azure-gáttinni](https://portal.azure.com) skal fara á **Azure Active Directory**.
2. Veljið **Stjórna \> Enterprise-forrit**.
3. Leitið að eftirfarandi forritum eftir FORRITSKENNINU.

    | Forrit                              | Auðkenni forrits                               |
    |------------------------------------------|--------------------------------------|
    | Microsoft Dynamics ERP Microservices     | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
    | Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |
    | Heimildaþjónusta AI Builder         | ad40333e-9910-4b61-b281-e3aeeb8c3ef3 |

Ef ekki eitthvað af undanfarandi forritum finnst ekki skal prófa eftirfarandi skref.

1. Á staðbundnu vélinni skal velja **Upphafsvalmyndina** og leita að **PowerShell**.
2. Velja skal og halda fingri á (eða hægrismella) **Windows PowerShell** og velja svo **Keyra sem stjórnandi**.
3. Keyrið eftirfarandi skipun til að setja upp **AzureAD** einingun.

    `Install-Module -Name AzureAD`

4. Ef NuGet-veita er nauðsynleg til að halda áfram skal velja **Y** til að setja hana upp.
5. Ef skeytið „Ótraust geymslׅa“ birtist skal velja **Y** til að halda áfram.
6. Fyrir hvert forrit sem verður að bæta við þarf að keyra eftirfarandi skipanir til að bæta forritinu við Azure AD. Skráðu þig inn sem stjórnandi Azure AD þegar beðið er um það.

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a>Stofna Azure-tilföng

> [!NOTE]
> Ganga skal úr skugga um að eftirfarandi tilföng séu stofnuð í sama Azure AD-tilviki og Common Data Service-umhverfið. Ekki er hægt að nota tilföng úr öðru Azure AD-tilviki.

1. Búa til nýjan geymslureikning:

    1. Í [Azure Portal](https://portal.azure.com) skal stofna geymslureikning.
    2. Í svarglugganum **Stofna geymslureikning** skal stilla eftirfarandi svæði:

        - **Staðsetning** – velja gagnamiðstöð með umhverfinu.
        - **Afköst** – mælt er með **Hefðbundin**.
        - **Reikningsgerð** – velja þarf **StorageV2**.

    3. Í svarglugganum **Ítarlegir valkostir**, fyrir **Data Lake Storage Gen2**, skal velja **Virkja** undir **Stigveldis nafnabil**. Ef þessi eiginleiki er gerður óvirkur er ekki hægt að nota gögn sem Finance and Operations-forrit skrifa með þjónustu á borð við Power BI-gagnaflæði.
    4. Veljið **yfirfara og búa til**. Þegar uppsetningu er lokið verður nýja tilfangið til staðar á Azure-gáttinni.
    5. Opnaðu geymslureikninginn sem þú stofnaðir.
    6. Á valmyndinni til vinstri skal velja **Aðgangslyklar**.
    7. Afritið og vistið tengingarstreng fyrir annaðhvort **Key1** eða **Key2**.
    8. Afrita og vista heiti geymslureiknings.

2. Búa til nýja lyklageymslu:

    1. Í [Azure Portal](https://portal.azure.com) skal stofna lyklageymslu.
    2. Í svarglugganum **Stofna lyklageymslu** á svæðinu **Staðsetning** skal velja gagnamiðstöðina þar sem umhverfið er að finna.
    3. Eftir að lyklageymsla er stofnuð skal velja hana á listanum og síðan velja **Leynilyklar**.
    4. Veljið **Mynda/Flytja inn**.
    5. Á síðunni **Stofna leynilykil**, á svæðinu **Valkostir upphleðslu**, skal velja **Handvirkt**.
    6. Færa skal inn heiti fyrir leynilykilinn. Gerið athugasemd við heitið vegna þess að það verður að nota það síðar.
    7. Á svæðinu **Gildi** skal færa inn tengingarstreng sem fenginn var úr geymslureikningi í fyrra ferli.
    8. Veljið **Virkjað** og veljið síðan **Búa til**. Leynilykillinn er stofnaður og bætt við Lyklageymslu.
    9. Opnið **Lyklageymsluyfirlit** og skráið niður DNS-heitið.

3. Stofna og skrá Azure AD forrit:

    1. Í [Azure-gáttinni](https://portal.azure.com) skal opna **Azure Active Directory** og velja svo **Forritaskráningar**.
    2. Velja skal **Ný forritaskráning** og stilla eftirfarandi svæði:

        - **Heiti** - Færið inn heiti forritsins.
        - **Forritsgerð** – Veljið **Vef-API**.
        - **Framsenda URI-uppsetningu** – Sláið inn vefslóð fyrir Dynamics 365-tilvikið, til dæmis, `https://yourdynamicsinstance.dynamics.com/auth`.

    3. Opnið forritið sem var búið til og afritið og vistið gildi fyrir **Forritskenni (biðlari)**. Gefa verður upp gildið síðar þegar lyklageymslan er sett upp.
    4. Farið í **API-heimildir** og fylgið eftirfarandi skrefum:

        1. Veljið **Bæta við heimild**.
        2. Veljið **Azure Key Vault**.
        3. Þegar búið er að velja úthlutaðar heimildir skal velja **Notandi\_Eftirlíking**.
        4. Veldu **Bæta við heimildum**.

    5. Á valmyndinni fyrir forritið skal velja **Vottorð \& Leynilykar** og síðan skal fylgja þessum skrefum til að búa til leynilykla lyklageymslu:

        1. Veljið **Nýtt leyniorð biðlara**.
        2. Í reitnum **Lyklalýsing** skal færa inn heiti.
        3. Veljið tímalengd og svo **Bæta við**. Leynilykill er myndaður á svæðinu **Gildi**.
        4. Afritaðu og vistaðu leynigildið.

4. Stofna leynilykla lyklageymslu:

    1. Opnið lyklageymsluna sem stofnuð var áður og veljið **Leynilyklar**.
    2. Fyrir hvert heiti leynilykils í eftirfarandi töflu skal fylgja þessum skrefum:

        1. Veljið **Mynda/Flytja inn**.
        2. Á síðunni **Stofna leynilykil**, á svæðinu **Valkostir upphleðslu**, skal velja **Handvirkt**.
        3. Búa skal til heiti leynilykils og gildi úr eftirfarandi töflu.
        4. Veljið **Virkjað** og veljið síðan **Búa til**. Leynilykillinn er stofnaður og bætt við Lyklageymslu.

        | Leyniheiti                       | Leynilykill                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | forrit-auðkenni                            | Forritskenni forritsins sem var stofnað áður                                      |
        | forrit-leyndarmál                        | Leyndarmál biðlarans sem var vistað áður                                                    |
        | geymsla-reikningur-heiti              | Heiti geymslureikningsins sem var stofnaður áður, t.d. **storageaccount1**       |
        | geymsla-reikningur-tenging-strengur | Tengingarstrengurinn sem var afritaður af síðunni **Aðgangslyklar** fyrir geymslureikninginn |

5. Heimila forriti aðgang að lyklageymslu:

    1. Í [Azure-gátt](https://portal.azure.com) skal opna lyklageymsluna sem var stofnuð áður.
    2. Velja aðgangsstefnur.
    3. Fyrir hvert forrit í eftirfarandi töflu skal fylgja þessum skrefum:

        1. Veljið **Bæta við aðgangsreglu** til að búa til aðgangsreglu.
        2. Á svæðinu **Heimildir leynilykils** skal velja heimildir úr eftirfarandi töflu.
        3. Á svæðinu **Velja aðalreikning** skal leita að birtingarheiti forrits sem birtist í eftirfarandi töflu.
        4. Veljið **Velja**.
        5. Veljið **Bæta við**.
        6. Veljið **Vista**.

        | Forrit                                              | Aðgangsheimildir |
        |----------------------------------------------------------|-------------|
        | Birtingarheiti nýja forritsins sem var búið til | Sækja, listi   |
        | **Microsoft Dynamics ERP Microservices**                 | Sækja, listi   |

6. Úthluta hlutverkum til að fá aðgang að geymslureikningi:

    1. Í [Azure-gáttinni](https://portal.azure.com) skal opna geymslureikninginn sem var stofnaður áður.
    2. Veljið **Aðgangsstýringu (IAM)** og veljið síðan **Hlutverkaúthlutanir**.
    3. Veljið **Bæta við, Bæta við hlutverkaúthlutun**.
    4. Fyrir hvert forrit í eftirfarandi töflu skal fylgja þessum skrefum:

        1. Velja skal hlutverkið úr eftirfarandi töflu.
        2. Hafið svæðið **Úthluta aðgangi að** stillt á **Azure AD-notanda, -hóp eða þjónustueiningu**.
        3. Á svæðinu **Velja** skal slá inn forrit úr eftirfarandi töflu.
        4. Veljið **Vista**.

        | Forrit                                              | Hlutverk                        |
        |----------------------------------------------------------|-----------------------------|
        | Birtingarheiti nýja forritsins sem var búið til | Eigandi                       |
        | Birtingarheiti nýja forritsins sem var búið til | Framlagsveitandi                 |
        | Birtingarheiti nýja forritsins sem var búið til | Geymslureikningsþátttakandi |
        | Birtingarheiti nýja forritsins sem var búið til | Eigandi Blob-gagna í geymslu     |
        | **Heimildaþjónusta AI Builder**                     | Lesari Blob-gagna í geymslu    |

# <a name="azure-cli"></a>[Azure CLI](#tab/azure-azure-cli)

```
function New-FinanceDataLakeAzureResources {
    $defaultSecretExpiryInYear = 1

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

    $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (blank for default)")
    if ($subscriptionId.Trim() -ne '') {
        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }

    $resourceGroupName = (Read-Host -Prompt "Enter the Azure Resource Group name: (blank for 'FinanceDataLake')")
    if ($null -eq $resourceGroupName -or $resourceGroupName.Trim() -eq '') {
        $resourceGroupName = 'FinanceDataLake'
    }
    $resourceGroup = Get-AzResourceGroup -Name $resourceGroupName -ErrorAction SilentlyContinue

    if (-not ($resourceGroup)) {
        $resourceLocation = ''
        $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
        while ($resourceLocation.Trim() -eq '' -or (-not ($resourceLocation -in $azResourceLocations))) {
            $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
            if ($resourceLocation -eq 'help') {
                $azResourceLocations
                $resourceLocation = ''
            }
        }
        $resourceGroup = New-AzResourceGroup -Name $resourceGroupName -Location $resourceLocation
    }
    else {
        $resourceLocation = $resourceGroup.Location
    }

    $clientAppName = (Read-Host -Prompt "Enter the name of the application registration: (blank for 'Finance Data Lake Application')")
    if ($clientAppName.Trim() -eq '') {
        $clientAppName = 'Finance Data Lake Application'
    }

    Write-Output '================================================================================='

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $MicrosoftDynamicsERPMicroservicesAppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId | Format-Table -AutoSize
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $MicrosoftDynamicsERPMicroservicesAppId + "'")
        Write-Output ("Added AAD Enterprise Application 'Microsoft Dynamics ERP Microservices' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesAppId)
    }
    else {
        Write-Output ("Found AAD Enterprise Application 'Microsoft Dynamics ERP Microservices' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesAppId)
    }
    $MicrosoftDynamicsERPMicroservicesAppObjectId = $service.ObjectId

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $MicrosoftDynamicsERPMicroservicesCDSAppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Format-Table -AutoSize
        Write-Output ("Added AAD Enterprise Application 'Microsoft Dynamics ERP Microservices CDS' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesCDSAppId)
    }
    else {
        Write-Output ("Found AAD Enterprise Application 'Microsoft Dynamics ERP Microservices CDS' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesCDSAppId)
    }

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AIBuilderAuthorizationServiceAppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId | Format-Table -AutoSize
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AIBuilderAuthorizationServiceAppId + "'")
        Write-Output ("Added AAD Enterprise Application 'AI Builder Authorization Service' with Application ID {0}" -f $AIBuilderAuthorizationServiceAppId)
    }
    else {
        Write-Output ("Found AAD Enterprise Application 'AI Builder Authorization Service' with Application ID {0}" -f $AIBuilderAuthorizationServiceAppId)
    }
    $aibuilderAuthorizationServiceObjectId = $service.ObjectId

    Write-Output '================================================================================='

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $clientAppName + "'")
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

        $clientApp = New-AzureADApplication -DisplayName $clientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($clientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $clientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $clientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $clientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($defaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    $deployment = New-AzResourceGroupDeployment -ResourceGroupName $resourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId

    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $resourceGroupName)
    }

    Write-Output '================================================================================='

    $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
    Write-Output "Values for LCS Data Lake Add-In:"
    Write-Output ("  Tenant ID:                         " + $subscriptionContext.Context.Subscription.TenantId)
    Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
    Write-Output "  Storage account secret name:       storage-account-name"
    Write-Output "  Application ID secret name:        app-id"
    Write-Output "  Application Secret secret name:    app-secret"
    Write-Warning "Copy this information for the LCS Add-in as it is not saved. Azure Cloud Shell will eventually time out and close."

    Write-Output '================================================================================='
    Write-Output "Values for System parameters > Data connections:"
    Write-Output ("  Application ID:                    " + $clientAppId)
    Write-Output ("  Application Secret:                " + $ClientAppSecret)
    Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
    Write-Output "  Secret name:                       storage-account-connection-string"
    Write-Warning "Copy this information for the System parameters as it is not saved. Azure Cloud Shell will eventually time out and close."
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
  New-FinanceDataLakeAzureResources
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

## <a name="configure-the-entity-store"></a>Grunnstilla einingaverslun

Fylgið eftirfarandi skrefum til að setja upp einingaverslunina í Finance-umhverfinu.

1. Opnið **Kerfisstjórnun\> Uppsetning\> Kerfisfæribreytur \> Gagnatengingar**.
2. Stillið **Virkja Data Lake-samþættingu** á **Já**.
3. Stillið eftirfarandi lyklageymslusvæði:

    - **Forritskenni (biðlari)** – Sláið inn auðkenni forritsbiðlara sem var stofnaður áður.
    - **Leynilykill forrits** – Sláið inn leynilykil sem vistaður var fyrir forritið sem stofnað var áður.
    - **DNS-heiti** – Hægt er að finna heiti lénsheitakerfis á upplýsingasíðu forrits fyrir forritið sem var stofnað áður.
    - **Leynilykilsheiti** – Sláið inn **geymsla-reikningur-tenging-strengur**.

## <a name="configure-the-data-lake"></a>Skilgreina Data Lake

Fylgið eftirfarandi skrefum til að nota LCS til að bæta Azure Data Lake-innbótinni við umhverfið.

1. Skráðu þig inn á LCS og veldu síðan **Allar upplýsingar**, undir heiti umhverfisins hægra megin á síðunni.
2. Í hlutanum **Innbætur umhverfis** skal velja **Setja upp nýja innbót**.
3. Veljið innbótina **Flytja út í Data Lake**.
4. Sláið inn eftirfarandi gildi.

    | Virði                                                              | lýsing |
    |--------------------------------------------------------------------|-------------|
    | Leigjandakenni Azure-áskriftar þar sem lyklageymsla er staðsett | Auðkenni leigjanda þar sem geymslureikningur, forrit og lyklageymslur eru staðsett. Til að finna þetta gildi skal opna [Azure-gátt](https://portal.azure.com), **Azure Active Directory** og afrita gildi **leigjandakennis**. |
    | Gefðu upp DNS-heiti lyklageymslunnar                             | DNS-heiti lyklageymslu, t.d. `https://customkeyvault.vault.azure.net/`. (Þetta gildi samsvarar DNS-heitinu sem er notað í einingaversluninni.) |
    | Gefðu upp leyndarmálið sem inniheldur heiti geymslureikningsins   | **geymsla-reikningur-heiti** |
    | Leyniheiti fyrir forritskenni sem verður notað til að fá aðgang að Data Lake          | **forrit-auðkenni** |
    | Leyniheiti sem verður notað með forritskenni                                 | **forrit-leyndarmál** |

5. Samþykkið skilmálana og veljið **Setja upp**.

Viðbótin verður sett upp innan fárra mínútna.

## <a name="configure-ai-builder"></a>Skilgreina AI Builder

1. Skráðu þig inn á LCS og opnaðu síðuna **Umhverfisupplýsingar**.
2. Flettu að hlutanum **Innbætur umhverfis**. Þú ættir að sjá innbæturnar sem eru þegar settar upp í þessu umhverfi. Ef innbótin **Flytja út í Data Lake** er ekki á meðal þeirra skal skilgreina þessa innbót.
3. Veljið innbótina **Fá innsýn**.
4. Sláið inn eftirfarandi gildi á upplýsingasíðu innbótarinnar **Fá innsýn**.

    | Virði                                                    | lýsing |
    |----------------------------------------------------------|-------------|
    | CDS-vefslóð fyrirtækis                                     | Vefslóð Common Data Service-fyrirtækis Common Data Service-tilviksins. Til að finna þetta gildi skal opna [Power Apps-gátt](https://make.powerapps.com), velja hnappinn **Stillingar** (gírtáknið) efst til hægri, velja **Ítarlegar stillingar** og afrita vefslóðina. (Slóðin endar á „dynamics.com“.) |
    | Auðkenni CDS-fyrirtækis                                               | Umhverfiskenni Common Data Service tilviksins. Til að finna þetta gildi skal opna [Power Apps-gátt](https://make.powerapps.com), velja hnappinn **Stillingar** (gírtáknið) efst til hægri, velja **Sérstillingar \> Þróunartilföng \> Tilvísunarupplýsingar tilviks** og afrita gildið í **Auðkenni**. |
    | Leigjandakenni CDS (skráasafnskenni úr AAD)               | Auðkenni leigjanda Common Data Service tilviksins Til að finna þetta gildi skal opna [Azure-gátt](https://portal.azure.com), **Azure Active Directory** og afrita gildi **leigjandakennis**. |
    | Veita notanda hlutarkenni sem er með stjórnandahlutverk | Auðkenni Azure AD-notandahlutarins í Common Data Service. Þessi notandi verður að vera kerfisstjóri Common Data Service-tilviks. Til að finna þetta gildi skal opna [Azure-gátt](https://portal.azure.com), opna **Azure Active Directory \> Notendur**, velja notandann og síðan, í **Auðkenni** , afrita gildið fyrir **Hlutarkenni**. |
    | Er þetta sjálfgefna CDS-umhverfið fyrir leigjandann?      | Ef Common Data Service-tilvik var fyrsta framleiðslutilvikið sem var stofnað skal velja þennan gátreit. Ef Common Data Service tilvik var búið til handvirkt skal hreinsa þennan gátreit. |

## <a name="feedback-and-support"></a>Ábendingar og stuðningur

Sendið tölvupóst á [Innsýn í greiðslur viðskiptavinar (forskoðun)](mailto:fiap@microsoft.com) ef áhugi er á að senda inn ábendingar eða aðstoð vantar.

## <a name="privacy-notice"></a>Tilkynning um persónuvernd

Forútgáfur (1) kunna að nota minni persónuverndar- og öryggisráðstafanir og þjónusta Dynamics 365 Finance and Operations, (2) eru ekki hluti af þjónustustigssamningi fyrir þessa þjónustu, (3) ættu ekki að vera notaðar til að vinna úr persónulegum gögnum eða öðrum gögnum sem falla undir lögboðnar kröfur eða reglur um samræmi og (4) hafa takmarkaðan stuðning.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]