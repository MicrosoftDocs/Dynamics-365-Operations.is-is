---
title: Stillingar fyrir Fjármálainnsýn - á undan útgáfu 10.0.19
description: Þetta efnisatriði útskýrir grunnstillingarskref sem mun gera kerfinu kleift að nota þá eiginleika sem eru í boði í Fjármálainnsýn fyrir útgáfur á undan 10.0.19.
author: ShivamPandey-msft
ms.date: 06/03/2021
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
ms.openlocfilehash: 6b578962839a34a1e2ce0311f7d8e7ee57a10927
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6357439"
---
# <a name="configuration-for-finance-insights-for-private-preview-preview---before-version-10019"></a>Stillingar fyrir Fjármálainnsýn fyrir einkaforskoðun (forútgáfu) - á undan útgáfu 10.0.19

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> Eftirfarandi ferli við uppsetningu fjármálainnsýnar gilda fyrir Microsoft Dynamics 365 Finance á undan útgáfu 10.0.19. Til að setja upp fjármálainnsýn á útgáfu 10.0.20 og nýrri skal sjá [Stilling fjármálainnsýnar (forútgáfa) - útgáfur 10.0.20 og nýrri](configure-for-fin-insites-PubPrvw.md).

Fjármálainnsýn sameinar virkni Microsoft Dynamics 365 Finance við Microsoft Dataverse, Azure og AI Builder til að bjóða upp á öflug spáverkfæri fyrir fyrirtækið. Þetta efnisatriði útskýrir grunnstillingarskref sem mun gera kerfinu kleift að nota þá eiginleika sem eru í boði í Fjármálainnsýn.

## <a name="deploy-dynamics-365-finance"></a>Virkja Dynamics 365 Finance

Virkjaðu umhverfið með því að fylgja þessum skrefum.

1. Í Microsoft Dynamics Lifecycle Services (LCS) skal búa til eða uppfæra Dynamics 365 Finance umhverfi. Umhverfið krefst forritsútgáfu 10.0.11/Verkvangsuppfærslu 35 eða nýrra.
2. Umhverfið verður að vera vel tiltækt í Sandbox. (Þessi tegund umhverfis er einnig þekkt sem umhverfi í tveggja laga umhverfi.) Frekari upplýsingar er að finna í [Umhverfisskipulagning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
3. Ef þú ert að stilla fjármálainnsýn í sandkassaumhverfi gætirðu þurft að afrita framleiðslugögn í það umhverfi til að spár virki. Spálíkanið notar gögn til margra ára til að búa til spár. Contoso sýnigögnin innihalda ekki næg söguleg gögn til að hægt sé að þjálfa spálíkanið á fullnægjandi hátt. 

## <a name="configure-dataverse"></a>Skilgreina Dataverse

Fylgið eftirfarandi skrefum til að stilla Dataverse fyrir Finance insights.

1. Opnið síðu umhverfis í LCS og staðfestið að hlutinn **Power Platform samþætting** sé þegar uppsettur.
    1. Ef hann er þegar uppsettur ætti heiti Dataverse umhverfisins sem tengt er við Dynamics 365 Finance umhverfið að vera sýnt. Afritið heiti Dataverse-umhverfisins.
    2. Ef það er ekki sett upp skal fylgja eftirfarandi skrefum:
        1. Veljið hnappinn **Uppsetning** í hlutanum Power Platform Samþætting. Það getur tekið allt að klukkustund að setja upp umhverfið.
        2. Ef tókst að setja upp Dataverse-umhverfið ætti heiti Dataverse-umhverfisins sem tengt er við Dynamics 365 Finance-umhverfið að vera sýnt. Afritið heiti Dataverse-umhverfisins.
> [!NOTE]
> Að lokinni uppsetningu umhverfisins **SKAL EKKI** velja hnappinn **Tengill á almenna gagnaþjónustu (CDS) fyrir forrit**. Þetta er ekki nauðsynlegt fyrir Finance insights og mun gera möguleikann á að ljúka við nauðsynlegar umhverfisviðbætur í LCS óvirkan.

2. Opnaðu [Power Platform stjórnendamiðstöð ](https://admin.powerplatform.microsoft.com/) og fylgdu þessum skrefum til að búa til nýtt Dataverse -umhverfi í sama Active Directory leigjanda:

    1. Opnið síðuna **Umhverfi**.

        [![Umhverfissíða.](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)

    2. Veljið Dataverse-umhverfið sem búið er til hér að ofan og veljið svo **Stillingar**.
    3. Veljið **Tilföng \> Allar eldri stillingar**.
    4. Á efstu yfirlitsstikunni skal velja **Stillingar** og síðan **Sérstillingar**.
    5. Veljið **Tilföng fyrir þróunaraðila**.
    6. Afritið gildið **Dataverse kenni fyrirtækis**.
    7. Í veffangastikunni vafrans skal gera athugasemd við VEFSLÓÐINA fyrir Dataverse-fyrirtækið. Til dæmis gæti vefslóðin verið `https://org42b2b3d3.crm.dynamics.com`.

3. Ef ætlunin er að nota sjóðstreymisspár eða fjárhagsáætlunarspár skal fylgja þessum skrefum til að uppfæra skýringartextamörk fyrirtækisins í að minnsta kosti 50 megabæt (MB):

    1. Opnið [Power Apps-gáttina](https://make.powerapps.com)
    2. Veljið það umhverfi sem var stofnað og veljið síðan **Ítarlegar stillingar**.
    3. Veljið **Stillingar\> Skilgreining tölvupósts**.
    4. Breytið gildi **Hámarksstærð skráar** reitnum í **51.200**. (Gildið er gefið upp í kílóbætum \[KB\].)
    5. Veljið **Í lagi** til að vista breytingarnar.

## <a name="configure-the-azure-setup"></a>Skilgreina Azure uppsetningu

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a>Sláið inn Dataverse skráarkenni og hlutarkenni Azure AD notandans

1. Sláið inn Dataverse skráasafnskenni:

    1. Opnið [Azure-gáttina](https://portal.azure.com)
    2. Skráðu þig inn með því að nota NOTANDAKENNIÐ sem var notað til að búa til Dataverse-umhverfið.
    3. Opnið **Azure Active Directory**.
    4. Afritið gildið **Leigjandakenni**.

2. Færa inn auðkenni hlutar notanda Azure Active Directory (Azure AD):

    1. Í [Azure-gátt](https://portal.azure.com) skal opna **Notendur** og leita að notandanum eftir netfangi.
    2. Færið inn nafn notanda.
    3. Afritið **Hlutarkenni** gildið.

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a>Nota Azure Cloud Shell til að setja upp Data Lake-tilföng fjármálainnsýnar

# <a name="use-a-windows-powershell-script"></a>[Nota Windows PowerShell-forskrift](#tab/use-a-powershell-script)

Boðið er upp á Windows PowerShell-forskrift þannig að auðvelt er að setja upp Azure-tilföng sem eru skilgreind í [Grunnstilla útflutning í Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md). Ef óskað er eftir því að setja upp handvirkt skal sleppa þessu ferli og halda áfram með ferlið í hlutanum [Handvirk uppsetning](#manual-setup).

> [!NOTE]
> Fylgið skrefunum hér að neðan til að keyra PowerShell-forskrift. Hugsanlega virkar ekki valkosturinn „Prófaðu þetta“ í Azure CLI eða ekki er hægt að keyra þessa forskrift á tölvunni.

Fylgið eftirfarandi skrefum til að grunnstilla Azure með Windows PowerShell-forskriftinni. Réttindi til að búa til Azure-tilfangaflokk, Azure-tilföng og Azure AD-forrit þurfa að vera til staðar. Frekari upplýsingar um nauðsynlegar heimildir má finna á [Athuga Azure AD heimildir](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).

1. Í [Azure-gátt](https://portal.azure.com) skal opna viðkomandi Azure-áskrift. Veljið **Cloud Shell**-hnappinn hægra megin við svæðið **Leita**.
2. Veljið **PowerShell**.
3. Búðu til geymslu, ef beðið er um að gera það.
4. Farið á flipann **Azure CLI** og veljið **Afrita**.  
5. Opnið Notepad og límið inn forskrift PowerShell. Vistið skrána sem ConfigureDataLake.ps1.
6. Hlaðið upp forskrift Windows PowerShell í lotuna með því að nota valkost valmyndar fyrir upphleðslu í Cloud Shell.
7. Keyra skriftuna .\ConfigureDataLake.ps1.
8. Fylgið kvaðningunum til að keyra forskriftina.
9. Notið upplýsingar úr forskriftinni til að setja upp innbótina **Flytja út í Data Lake** í LCS.
10. Notið upplýsingar úr forskriftinni til að virkja einingaverslunina á síðunni **Gagnatengingar** í Finance (**Kerfisstjórnun \> Kerfisfæribreytur \> Gagnatengingar**).

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
> Ganga skal úr skugga um að eftirfarandi tilföng séu stofnuð í sama Azure AD-tilviki og Dataverse-umhverfið. Ekki er hægt að nota tilföng úr öðru Azure AD-tilviki.

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
    | CDS-vefslóð fyrirtækis                                     | Vefslóð Dataverse fyrirtækisins afrituð að ofan. |
    | Auðkenni CDS-fyrirtækis                                               | Kenni Dataverse fyrirtækisins afritað að ofan. |
5. Virkið **Er þetta sjálfgefna umhverfið fyrir leigjandann þinn**.

Það gæti tekið nokkrar mínútur að setja innbótina upp.
    
## <a name="configure-the-entity-store"></a>Grunnstilla einingaverslun

Fylgið eftirfarandi skrefum til að setja upp einingaverslunina í Finance-umhverfinu.

1. Opnið **Kerfisstjórnun\> Uppsetning\> Kerfisfæribreytur \> Gagnatengingar**.
2. Stillið eftirfarandi lyklageymslusvæði:

    - **Forritskenni (biðlari)** – Sláið inn auðkenni forritsbiðlara sem var stofnaður áður.
    - **Leynilykill forrits** – Sláið inn leynilykil sem vistaður var fyrir forritið sem stofnað var áður.
    - **DNS-heiti** – Hægt er að finna heiti lénsheitakerfis á upplýsingasíðu forrits fyrir forritið sem var stofnað áður.
    - **Leynilykilsheiti** – Sláið inn **geymsla-reikningur-tenging-strengur**.
3. Virkið **Kveikja á samþættingu Data Lake**.
4. Veljið **Prófa Azure-lyklageymslu** og staðfestið að engar villur séu til staðar.
5. Veljið **Prófa Azure Storage** og staðfestið að engar villur séu til staðar.

## <a name="feedback-and-support"></a>Ábendingar og stuðningur

Sendið tölvupóst á [Innsýn í greiðslur viðskiptavinar (forskoðun)](mailto:fiap@microsoft.com) ef áhugi er á að senda inn ábendingar eða aðstoð vantar.

## <a name="privacy-notice"></a>Tilkynning um persónuvernd

Forútgáfur (1) kunna að nota minni persónuverndar- og öryggisráðstafanir og þjónusta Dynamics 365 Finance and Operations, (2) eru ekki hluti af þjónustustigssamningi fyrir þessa þjónustu, (3) ættu ekki að vera notaðar til að vinna úr persónulegum gögnum eða öðrum gögnum sem falla undir lögboðnar kröfur eða reglur um samræmi og (4) hafa takmarkaðan stuðning.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
