---
title: Nota jaðareiningakvarða í sérsniðnum vélbúnaði með LBD
description: Þetta efnisatriði útskýrir hvernig hægt er að úthluta kvörðunareiningu jaðars á staðnum með því að nota sérsniðinn vélbúnað og uppsetningu sem byggir á staðbundnum viðskiptagögnum (LBD).
author: cabeln
ms.date: 01/24/2022
ms.topic: article
ms.prod: dynamics-365
ms.service: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 37bc8678d4e04afebbebaaa893a484866a8643ce
ms.sourcegitcommit: 23588e66e25c05e989f3212ac519d7016820430a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2022
ms.locfileid: "8565548"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd"></a>Nota jaðareiningakvarða í sérsniðnum vélbúnaði með LBD

[!include [banner](../includes/banner.md)]

Kvörðunareiningar jaðars gegna mikilvægu hlutverki í dreifingu á blandaðri grannfræði fyrir aðfangakeðjustjórnun. Í blandaðri grannfræði er hægt að dreifa vinnuálagi á milli skýjamiðstöðvar Supply Chain Management og annarra kvörðunareininga í skýinu eða á jaðrinum.

Hægt er að setja upp kvörðunareiningar jaðars með því að búa til staðbundin viðskiptagögn (LBD) í [innanhússumhverfi](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) og stilla það svo þannig að það virki sem kvörðunareining í dreifðri blandaðri grannfræði þinni fyrir aðfangakeðjustjórnun. Þetta er gert með því að tengja LBD-umhverfið á staðnum við umhverfi Supply Chain Management í skýinu, sem hefur verið stillt þannig að það virki sem miðstöð.  

Þetta efnisatriði lýsir því hvernig á að setja upp LBD-umhverfi á staðnum sem jaðarkvörðunareiningu og síðan tengja það við miðstöð.

## <a name="infrastructure-considerations"></a>Innviðasjónarmið

Edge mælikvarða einingar keyra á staðnum umhverfi, þannig að innviðakröfur eru nokkuð svipaðar. Hins vegar er ákveðinn munur sem ætti að hafa í huga:

- Jaðarkvarðaeiningar nota ekki fjárhagsskýrslugerð, svo þær þurfa ekki fjárhagsskýrsluhnúta.
- Vinnuálag framleiðslu og vörugeymsla er ekki tölvufrekt, svo íhugaðu að stærð reiknikraftinn þinn fyrir AOS hnúta í samræmi við það.

## <a name="deployment-overview"></a>Yfirlit uppsetningar

Hér er yfirlit uppsetningarferlisins.

1. **Virkja LBD-hólf í LBD-verkinu þínu í Microsoft Dynamics Lifecycle Services (LCS).**

1. **Setja upp og nota LBD-umhverfi með *tómum* gagnagrunni.**

    Notaðu LCS til að útfæra LBD-umhverfið með nýjustu grannfræði og tómum gagnagrunni. Frekari upplýsingar er að finna í hlutanum [Setja upp og nota LBD-umhverfi með tómum gagnagrunni](#set-up-deploy) síðar í þessu efnisatriði. Þú verður að nota Supply Chain Management útgáfu 10.0.21 eða nýrri yfir miðstöð og mælieiningaumhverfi.

1. **Hlaða markpökkum upp í eignir LBD-verks í LCS.**

    Undirbúðu forrit, verkvang og sérstillingarpakka sem þú notar í miðstöðinni og jaðarkvörðunareiningu. Frekari upplýsingar er að finna í hlutanum [Hlaða markpökkum upp í eignir LBD-verks í LCS](#upload-packages) síðar í þessu efnisatriði.

1. **Þjónusta LBD-umhverfið með markpökkunum.**

    Þetta skref tryggir að sama smíði og sérstillingar séu notaðar í miðstöðinni og spoke. Nánari upplýsingar er að finna í hlutanum [Þjónusta LBD-umhverfi með markpökkum](#service-target-packages) síðar í þessu efnisatriði.

1. **Klára grunnstillingu kvörðunareiningar og úthlutun vinnuálags.**

    Frekari upplýsingar er að finna í hlutanum [Úthluta LBD-jaðarkvörðunareiningu á miðstöð](#assign-edge-to-hub) síðar í þessu efnisatriði.

Í eftirstandandi hlutum þessa efnisatriðis er að finna frekari upplýsingar um hvernig á að ljúka þessum skrefum.

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a>Setja upp og nota LBD-umhverfi með tómum gagnagrunni

Þetta skref býr til virkt LBD-umhverfi. Hins vegar hefur umhverfið ekki endilega sömu forrits- og verkvangsútgáfur og umhverfi miðstöðvarinnar. Að auki vantar enn sérstillingarnar og þær hafa ekki enn verið virkjaðar sem kvörðunareining.

1. Fylgdu leiðbeiningunum í [Setja upp og innleiða umhverfi á staðnum (verkvangsuppfærsla 41 og nýrri)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Þú verður að nota Supply Chain Management útgáfu 10.0.21 eða nýrri yfir miðstöð og mælieiningaumhverfi. Að auki verður þú að nota útgáfu 2.12.0 eða nýrri af innviðaforskriftunum. 

    > [!IMPORTANT]
    > Lestu afganginn af þessum hluta **áður en** þú lýkur við skrefin í því efnisatriði.

1. Keyrðu eftirfarandi forskrift áður en þú lýsir grunnstillingu þinni í tölvukerfinu\\ConfigTemplate.xml-skránni:

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Þessi forskrift fjarlægir allar stillingar sem ekki er þörf á til að setja inn kvörðunareiningar jaðars.

1. Settu upp gagnagrunn sem inniheldur tóm gögn eins og lýst er í [Grunnstilla gagnagrunna](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb). Nota tómu skrána data.bak fyrir fyrsta skrefið.
1. Eftir að þú hefur lokið við [Stilla gagnagrunna](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) skref, keyrðu eftirfarandi skriftu til að stilla Scale Unit Alm Orchestrator gagnagrunninn.

    > [!NOTE]
    > Ekki stilla fjárhagsskýrslugagnagrunninn á meðan [Stilla gagnagrunna](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) skref.

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName EdgeScaleUnit
    ```

    Initialize-Database.ps1 forskriftin framkvæmir eftirfarandi aðgerðir:

    1. Búðu til tóman gagnagrunn sem heitir **ScaleUnitAlmDb**.
    2. Settu notendur á gagnagrunnshlutverk, byggt á eftirfarandi töflu.

        | Notandi            | Gerð | Gagnagrunnshlutverk |
        |-----------------|------|---------------|
        | svc-LocalAgent$ | gMSA | db\_ eiganda     |

1. Haltu áfram að fylgja leiðbeiningunum í [Settu upp og settu upp umhverfi á staðnum (Platform update 41 og síðar)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md).
1. Eftir að þú hefur lokið við [Stilla AD FS](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) skref, fylgdu þessum skrefum:

    1. Búðu til nýtt Active Directory Federation Services (AD FS) forrit sem gerir Alm Orchestration þjónustunni kleift að eiga samskipti við Application Object Server (AOS).

        ```powershell
        # Host URL is your DNS record\host name for accessing the AOS
        .\Create-ADFSServerApplicationForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -HostUrl 'https://ax.d365ffo.onprem.contoso.com'
        ```

    1. Búðu til nýtt Azure Active Directory (Azure AD) forrit sem gerir Alm Orchestration þjónustunni kleift að eiga samskipti við Scale Unit Management þjónustuna.

        ```powershell
        # Example .\Create-SumAADApplication.ps1 -ConfigurationFilePath ..\ConfigTemplate.xml -TenantId '6240a19e-86f1-41af-91ab-dbe29dbcfb95' -ApplicationDisplayName 'EdgeAgent-SUMCommunication-EN01'
        .\Create-SumAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                       -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                       -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
        ```

1. Haltu áfram að fylgja leiðbeiningunum í [Settu upp og settu upp umhverfi á staðnum (Platform update 41 og síðar)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Þegar þú verður að slá inn stillingu fyrir staðbundinn umboðsmann skaltu ganga úr skugga um að þú virkjar Edge Scale Unit Features og gefur upp allar nauðsynlegar færibreytur.

    ![Virkja Edge Scale Unit eiginleika.](media/EnableEdgeScaleUnitFeatures.png "Virkja Edge Scale Unit eiginleika.")

1. Áður en þú setur upp umhverfið þitt frá LCS skaltu setja upp fordreifingarforskriftina. Frekari upplýsingar er að finna í [Forskriftir fyrir og eftir uppsetningu umboðsmanns á staðnum](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md).

    1. Afritaðu Configure-CloudAndEdge.ps1 forskriftina úr **ScaleUnit** mappa inn **Innviðaforskriftir** til **Handrit** möppu í umboðsskjalageymsluhlutdeild sem var sett upp í umhverfinu. Dæmigerð slóð er \\\\lbdiscsi01\\agent\\Scripts.
    2. Búðu til **PreDeployment.ps1** forskrift sem mun kalla fram forskriftirnar með því að nota nauðsynlegar færibreytur. Forskrift fyrir uppsetningu verður að vera sett í möppuna **Forskriftir** í samnýttri skráageymslu umboðsmanns. Annars er ekki hægt að keyra hana. Dæmigerð slóð er \\\\lbdiscsi01\\agent\\Scripts\\PreDeployment.ps1.

        Innihald forskriftarinnar PreDeployment.ps1 mun líkjast eftirfarandi dæmi.

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        . $PSScriptRoot\Configure-CloudAndEdge.ps1 -AgentShare $agentShare -InstanceId '@A'
        ```

        > [!NOTE]
        > Færibreytan InstanceId á aðeins að vera tveir stafir. Fyrri stafurinn er @ og sá seinni getur verið hvaða hástafur sem er í enska stafrófinu.
        >
        > - Gild gildi:
        >   - @D
        >   - @X
        > - Ekki gild gildi:
        >   - @a
        >   - @4
        >   - @#

1. Settu upp umhverfið með því að nota nýjustu grunngrannfræði sem er í boði.
1. Eftir að umhverfið þitt hefur verið dreift skaltu fylgja þessum skrefum:

    1. Keyrðu eftirfarandi SQL skipanir á viðskiptagagnagrunninum þínum (AXDB).

        ```sql
        ALTER TABLE dbo.NUMBERSEQUENCETABLE ENABLE CHANGE_TRACKING WITH (TRACK_COLUMNS_UPDATED = ON)
        delete from NumberSequenceTable
        delete from NumberSequenceReference
        delete from NumberSequenceScope
        delete from FeatureManagementMetadata
        delete from FeatureManagementState
        delete from SysFeatureStateV0
        ```

    1. Auka samhliða hámarkslotulotu í gildi sem er meira en 4.

        ```sql
        Update batchserverconfig set maxbatchsessions = '<Replace with number of concurrent batch tasks you want>'
        ```

    1. Staðfestu að breytingarakning hafi verið virkjuð á viðskiptagagnagrunninum þínum (AXDB).

        1. Opnaðu SQL Server Management Studio (SSMS).
        1. Veldu og haltu (eða hægrismelltu) viðskiptagagnagrunninum þínum (AXDB) og veldu síðan **Eiginleikar**.
        1. Í glugganum sem birtist skaltu velja **Breyta mælingar**, og stilltu síðan eftirfarandi gildi:

            - **Breyta rakningu:** *Satt*
            - **Varðveislutímabil:** *7*
            - **Varðveislueiningar:** *Dagar*
            - **Sjálfvirk hreinsun:** *Satt*

    1. Bættu AD FS forritaauðkenninu sem þú bjóst til áðan (með því að nota Create-ADFSServerApplicationForEdgeScaleUnits.ps1 forskriftina) við Azure AD forritatöflu í kvarðaeiningunni þinni. Þú getur lokið þessu skrefi handvirkt í gegnum notendaviðmótið (UI). Að öðrum kosti geturðu klárað það í gegnum gagnagrunninn með því að nota eftirfarandi forskrift.

        ```sql
        DECLARE @ALMOrchestratorId NVARCHAR(76) = '<Replace with the ADFS Application ID created in a previous step>';

        IF NOT EXISTS (SELECT TOP 1 1 FROM SysAADClientTable WHERE AADClientId = @ALMOrchestratorId)
        BEGIN
            INSERT INTO SysAADClientTable (AADClientId, UserId, Name, ModifiedBy, CreatedBy)
            VALUES (@ALMOrchestratorId, 'ScaleUnitManagement', 'Scale Unit Management', 'Admin', 'Admin');
        END
        ```

## <a name="set-up-an-azure-key-vault-and-an-azure-ad-application-to-enable-communication-between-scale-units"></a><a name="set-up-keyvault"></a> Settu upp Azure lykilhólf og Azure AD forrit til að gera samskipti milli mælieininga kleift

1. Eftir að umhverfið þitt hefur verið notað skaltu búa til viðbótar Azure AD forrit til að virkja traust samskipti milli miðstöðvarinnar og mælieiningarinnar.

    ```powershell
    .\Create-SpokeToHubAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                          -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                          -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
    ```

1. Eftir að þú hefur búið til forritið verður þú að búa til biðlaraleyndarmál og vista upplýsingarnar í Azure lyklahólfi. Að auki verður þú að veita aðgang að Azure AD forrit sem var búið til, þannig að það getur sótt leyndarmálin sem eru geymd í lyklageymslunni. Til þæginda mun eftirfarandi handrit sjálfkrafa framkvæma allar nauðsynlegar aðgerðir.

    ```powershell
    .\Create-SpokeToHubAADAppSecrets.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                         -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                         -SubscriptionName '<Any subscription within your tenant>' `
                                         -ResourceGroupName '<Any resource group within your subscription>' `
                                         -KeyVaultName '<Any key vault within your resource group>' `
                                         -Location '<Any Azure location where Azure Key Vault is available>' `
                                         -LCSEnvironmentId '<The LCS environment ID of your deployed scale unit>' `
    ```

    > [!NOTE]
    > Ef engin lyklahólf sem hefur tilgreint **KeyVaultName** gildi er til, forskriftin býr sjálfkrafa til einn.

1. Bætið við Azure AD auðkenni forrits sem þú varst að búa til (þegar þú notar Create-SpokeToHubAADApplication.ps1 forskriftina) í Azure AD forritatöflu í miðstöðinni þinni. Þú getur lokið þessu skrefi handvirkt í gegnum notendaviðmótið.

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a>Hlaða markpökkum upp í eignir LBD-verks í LCS

Þetta skref undirbýr forritsútgáfu, verkvangsútgáfu og sérstillingar sem verða færðar yfir í kvörðunareiningarumhverfi LBD.

1. Hlaða skal upp sama sameinaða forrits-/verkvangspakkanum og var notaður í umhverfi miðstöðvarinnar í eignasafn LCS-verks á staðnum.
1. Fáðu afrit af sérsniðna virkjanlega pakkanum sem var notaður í umhverfi miðstöðvarinnar og hladdu honum upp í eignasafn LCS-verks á staðnum.

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a>Þjónusta LBD-umhverfið með markpökkum

Þetta skref samræmir útgáfu forrits, útgáfu verkvangs og sérstillingar í umhverfi LBD-kvörðunareiningar við miðstöðina.

1. Þjónustaðu LBD-umhverfið með samsetta forrits-/verkvangspakkanum sem þú hlóðst upp í skrefinu á undan.
1. Þjónustaðu LBD-umhverfið með sérstillta virkjanlega pakkanum sem þú hlóðst upp í skrefinu á undan.

    ![Að beita uppfærslum í LCS.](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "Að beita uppfærslum í LCS")

    ![Sérstillingarpakkinn valinn.](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "Sérstillingarpakkinn þinn valinn")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a>Úthluta LBD-kvörðunareiningu jaðars á miðstöð

Þú stillir og stjórnar brúnkvarðaeiningunni þinni í gegnum mælikvarðastjórnunargáttina. Fyrir frekari upplýsingar, sjá [Hafa umsjón með mælieiningum og vinnuálagi með því að nota gáttina Scale Unit Manager](./cloud-edge-landing-page.md#scale-unit-manager-portal).

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
