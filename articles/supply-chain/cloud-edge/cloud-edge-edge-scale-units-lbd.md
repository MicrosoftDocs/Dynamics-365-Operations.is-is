---
title: Nota jaðareiningakvarða í sérsniðnum vélbúnaði með LBD (forskoðun)
description: Þetta efnisatriði útskýrir hvernig hægt er að úthluta kvörðunareiningu jaðars á staðnum með því að nota sérsniðinn vélbúnað og uppsetningu sem byggir á staðbundnum viðskiptagögnum (LBD).
author: cabeln
ms.date: 04/22/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0ebbdaab9d6f040497d3158db2712e102b6e9aa8
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678982"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd-preview"></a>Nota jaðareiningakvarða í sérsniðnum vélbúnaði með LBD (forskoðun)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)] <!--KFM: Until 11/1/2021 -->

Kvörðunareiningar jaðars gegna mikilvægu hlutverki í dreifingu á blandaðri grannfræði fyrir aðfangakeðjustjórnun. Í blandaðri grannfræði er hægt að dreifa vinnuálagi á milli skýjamiðstöðvar Supply Chain Management og annarra kvörðunareininga í skýinu eða á jaðrinum.

Hægt er að setja upp kvörðunareiningar jaðars með því að búa til staðbundin viðskiptagögn (LBD) í [innanhússumhverfi](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) og stilla það svo þannig að það virki sem kvörðunareining í dreifðri blandaðri grannfræði þinni fyrir aðfangakeðjustjórnun. Þetta er gert með því að tengja LBD-umhverfið á staðnum við umhverfi Supply Chain Management í skýinu, sem hefur verið stillt þannig að það virki sem miðstöð.  

Jaðarkvörðunareiningar eru sem stendur í forútgáfu. Þú mátt því aðeins nota umhverfi af þessari gerð í samræmi við [skilmála forútgáfunnar](https://aka.ms/scmcnepreviewterms).

Þetta efnisatriði lýsir því hvernig á að setja upp LBD-umhverfi á staðnum sem jaðarkvörðunareiningu og síðan tengja það við miðstöð.

## <a name="deployment-overview"></a>Yfirlit uppsetningar

Hér er yfirlit uppsetningarferlisins.

1. **Virkja LBD-hólf í LBD-verkinu þínu í Microsoft Dynamics Lifecycle Services (LCS).**

    Í forútgáfunni miðast jaðarkvörðunareiningar LBD við LBD-viðskiptavini. Aukalegt 60 daga takmarkað hólf LBD-sandkassa verður í boði í tilteknum kringumstæðum viðskiptavinar.

1. **Setja upp og nota LBD-umhverfi með *tómum* gagnagrunni.**

    Notaðu LCS til að útfæra LBD-umhverfið með nýjustu grannfræði og tómum gagnagrunni. Frekari upplýsingar er að finna í hlutanum [Setja upp og nota LBD-umhverfi með tómum gagnagrunni](#set-up-deploy) síðar í þessu efnisatriði. Þú verður að nota útgáfu 10.0.19 af Supply Chain Management með verkvangsuppfærslu 43 eða nýrri í umhverfum miðstöðvar og kvörðunareiningar.

1. **Hlaða markpökkum upp í eignir LBD-verks í LCS.**

    Undirbúðu forrit, verkvang og sérstillingarpakka sem þú notar í miðstöðinni og jaðarkvörðunareiningu. Frekari upplýsingar er að finna í hlutanum [Hlaða markpökkum upp í eignir LBD-verks í LCS](#upload-packages) síðar í þessu efnisatriði.

1. **Þjónusta LBD-umhverfið með markpökkunum.**

    Þetta skref tryggir að sama smíði og sérstillingar séu notaðar í miðstöðinni og spoke. Nánari upplýsingar er að finna í hlutanum [Þjónusta LBD-umhverfi með markpökkum](#service-target-packages) síðar í þessu efnisatriði.

1. **Klára grunnstillingu kvörðunareiningar og úthlutun vinnuálags.**

    Frekari upplýsingar er að finna í hlutanum [Úthluta LBD-jaðarkvörðunareiningu á miðstöð](#assign-edge-to-hub) síðar í þessu efnisatriði.

Í eftirstandandi hlutum þessa efnisatriðis er að finna frekari upplýsingar um hvernig á að ljúka þessum skrefum.

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a>Setja upp og nota LBD-umhverfi með tómum gagnagrunni

Þetta skref býr til virkt LBD-umhverfi. Hins vegar hefur umhverfið ekki endilega sömu forrits- og verkvangsútgáfur og umhverfi miðstöðvarinnar. Að auki vantar enn sérstillingarnar og þær hafa ekki enn verið virkjaðar sem kvörðunareining.

1. Fylgdu leiðbeiningunum í [Setja upp og innleiða umhverfi á staðnum (verkvangsuppfærsla 41 og nýrri)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Þú verður að nota útgáfu 10.0.19 af Supply Chain Management með verkvangsuppfærslu 43 eða nýrri í umhverfum miðstöðvar og kvörðunareiningar

    > [!IMPORTANT]
    > Lestu afganginn af þessum hluta **áður en** þú lýkur við skrefin í því efnisatriði.

1. Keyrðu eftirfarandi forskrift áður en þú lýsir grunnstillingu þinni í tölvukerfinu\\ConfigTemplate.xml-skránni:

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Þessi forskrift fjarlægir allar stillingar sem ekki er þörf á til að setja inn kvörðunareiningar jaðars.

1. Settu upp gagnagrunn sem inniheldur tóm gögn eins og lýst er í [Grunnstilla gagnagrunna](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb). Nota tómu skrána data.bak fyrir fyrsta skrefið.
1. Settu upp forskriftina fyrir uppsetningu. Frekari upplýsingar er að finna í [Forskriftir fyrir og eftir uppsetningu umboðsmanns á staðnum](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md).

    1. Afritaðu innihaldið úr möppunni **ScaleUnit** í **Forskriftir tölvukerfis** yfir í möppuna **Forskriftir** í samnýttri skráageymslu umboðsmanns sem var sett upp í umhverfinu. Dæmigerð slóð er \\\\lbdiscsi01\\agent\\Scripts.
    2. Búðu til **PreDeployment.ps1** forskrift sem mun kalla fram forskriftirnar með því að nota nauðsynlegar færibreytur. Forskrift fyrir uppsetningu verður að vera sett í möppuna **Forskriftir** í samnýttri skráageymslu umboðsmanns. Annars er ekki hægt að keyra hana. Dæmigerð slóð er \\\\lbdiscsi01\\agent\\Scripts\\PreDeployment.ps1.

        Innihald forskriftarinnar PreDeployment.ps1 mun líkjast eftirfarandi dæmi.

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        & $agentShare\Scripts\Configure-CloudandEdge.ps1 -AgentShare $agentShare -InstanceId '@A' -DatabaseServer 'lbdsqla01.contoso.com' -DatabaseName 'AXDB'
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

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a>Hlaða markpökkum upp í eignir LBD-verks í LCS

Þetta skref undirbýr forritsútgáfu, verkvangsútgáfu og sérstillingar sem verða færðar yfir í kvörðunareiningarumhverfi LBD.

1. Hlaða skal upp sama sameinaða forrits-/verkvangspakkanum og var notaður í umhverfi miðstöðvarinnar í eignasafn LCS-verks á staðnum.
1. Fáðu afrit af sérsniðna virkjanlega pakkanum sem var notaður í umhverfi miðstöðvarinnar og hladdu honum upp í eignasafn LCS-verks á staðnum.

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a>Þjónusta LBD-umhverfið með markpökkum

Þetta skref samræmir útgáfu forrits, útgáfu verkvangs og sérstillingar í umhverfi LBD-kvörðunareiningar við miðstöðina.

1. Þjónustaðu LBD-umhverfið með samsetta forrits-/verkvangspakkanum sem þú hlóðst upp í skrefinu á undan.
1. Þjónustaðu LBD-umhverfið með sérstillta virkjanlega pakkanum sem þú hlóðst upp í skrefinu á undan.

    ![Velja Viðhalda og > Nota uppfærslur í LCS.](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "Valið er Viðhalda > Nota uppfærslur í LCS")

    ![Sérstillingarpakkinn valinn.](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "Sérstillingarpakkinn þinn valinn")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a>Úthluta LBD-kvörðunareiningu jaðars á miðstöð

Þótt kvörðunareiningar jaðars séu enn í forútgáfu þarftu samt að nota [uppsetning kvörðunareiningar og grunnstillingarverkfæri](https://github.com/microsoft/SCMScaleUnitDevTools) sem eru í boði í GitHub til að úthluta LBD-kvörðunareiningu jaðars á miðstöð. Ferlið gerir LBD-stillingu kleift að virka sem kvörðunareining jaðars og tengir hana við miðstöðina. Ferlið er svipað og að stilla heildræna uppsetningu umhverfis.

1. Sæktu nýjustu útgáfu [SCMScaleUnitDevTools](https://github.com/microsoft/SCMScaleUnitDevTools/releases) og afþjappaðu efni skráarinnar.
1. Taktu afrit af `UserConfig.sample.xml` skránni og skírðu hana `UserConfig.xml`.
1. Búðu til Microsoft Azure Active Directory (Azure AD) forrit í Azure AD leigjandanum þínum eins og minnst er á í [Leiðarvísir fyrir uppsetningu kvörðunareiningar og vinnuálags](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#aad-application-registrations).
    1. Þegar það hefur verið búið til skal fara í skjámynd Azure AD forritanna (SysAADClientTable) í miðstöðinni.
    1. Búðu til nýja færslu og stilltu **Biðlarakennið** á auðkenni forritsins sem þú bjóst til. Stilltu **Heitið** á *ScaleUnits* og **Notandakennið** á *Stjórnanda*.

1. Búa til Active Directory Federation Service (AD FS) forrit eins og minnst er á í [Leiðarvísir fyrir uppsetningu kvörðunareiningar og vinnuálags](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#adfs-application-registrations).
    1. Þegar það hefur verið búið til skal fara í skjámynd Azure AD forritanna (SysAADClientTable) í kvörðunareiningu jaðars.
    1. Búðu til nýja færslu og stilltu **Biðlarakennið** á auðkenni forritsins sem þú bjóst til. Stilltu **Notandakennið** á *Stjórnanda*.

1. Breyttu `UserConfig.xml` skránni.
    1. Í `InterAOSAADConfiguration` hlutanum skal færa inn upplýsingarnar úr Azure AD forritinu sem þú bjóst til hér á undan.
        - Í `AppId` einingunni skal færa inn forritskenni Azure-forritsins.
        - Í `AppSecret` einingunni skal færa inn leynilykil Azure-forritsins.
        - Einingin `Authority` verður að innihalda vefslóðina sem tilgreinir öryggi leigjandans þíns.

        ```xml
        <InterAOSAADConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopty56TGUedDTVhtER-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </InterAOSAADConfiguration>
        ```

    1. Í `ScaleUnitConfiguration` hlutanum fyrir fyrra `ScaleUnitInstance` skal breyta `AuthConfiguration` hlutanum.
        - Í `AppId` einingunni skal færa inn forritskenni Azure-forritsins.
        - Í `AppSecret` einingunni skal færa inn leynilykil Azure-forritsins.
        - Einingin `Authority` verður að innihalda vefslóðina sem tilgreinir öryggi leigjandans þíns.

        ```xml
        <AuthConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopdz.6d3DTVOtf9Lo-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </AuthConfiguration>
        ```

    1. Fyrir þetta sama `ScaleUnitInstance` skal að auki stilla eftirfarandi gildi:
        - Í `Domain` einingunni skal tilgreina vefslóð miðstöðvarinnar. Til dæmis: `https://cloudhub.sandbox.operations.dynamics.com/`
        - Í `EnvironmentType` einingunni skal tryggja að gildið `LCSHosted` sé stillt.

    1. Í `ScaleUnitConfiguration` hlutanum fyrir seinna `ScaleUnitInstance` skal breyta `AuthConfiguration` hlutanum.
        - Í `AppId` einingunni skal færa inn forritskenni AD FS-forritsins.
        - Í `AppSecret` einingunni skal færa inn leynilykil ADFS-forritsins.
        - Einingin `Authority` verður að innihalda vefslóð AD FS-tilviksins.

        ```xml
        <AuthConfiguration>
            <AppId>26b16f25-21d8-4d36-987b-62df292895aa</AppId>
            <AppSecret>iZFfObgI6lLtY9kEbBjEFV98NqI5_YZ0e5SBcWER</AppSecret>
            <Authority>https://adfs.contoso.com/adfs</Authority>
        </AuthConfiguration>
        ```

    1. Fyrir þetta sama `ScaleUnitInstance` skal að auki stilla eftirfarandi gildi:
        - Í `Domain` einingunni skal tilgreina vefslóð jaðarkvörðunareiningarinnar. Til dæmis: https://ax.contoso.com/
        - Í `EnvironmentType` einingunni skal tryggja að gildi LBD sé stillt.
        - Í `ScaleUnitId` einingunni skal setja inn sama gildið og tilgreint var fyrir `InstanceId` þegar `Configure-CloudandEdge.ps1` var grunnstillt á undan uppsetningu forskriftar.

        > [!NOTE]
        > Ef þú notar ekki sjálfgefna auðkennið (@A) skaltu tryggja að þú uppfærir ScaleUnitId fyrir hvert ConfiguredWorkload undir vinnuálagshlutanum.

1. Opnaðu PowerShell og farðu í möppuna sem inniheldur `UserConfig.xml` skrána.

1. Keyrðu verkfærið með þessari skipun.

    ```powershell
    .\CLI.exe
    ```

    > [!NOTE]
    > Eftir hverja aðgerð þarf að opna verkfærið á nýjan leik.

1. Í verkfærinu skal velja **2. Undirbúa umhverfi undir uppsetningu vinnuálags**. Síðan skal keyra eftirfarandi skref:
    1. Veldu **1. Undirbúa miðstöðina**.
    1. Veldu **2. Undirbúa kvörðunareininguna**.

    > [!NOTE]
    > Ef þú ert ekki að keyra þessa skipun úr uppsetning frá grunni og hún mistekst skaltu framkvæma eftirfarandi aðgerðir:
    >
    > - Fjarlægðu allar möppur úr `aos-storage` möppunni (nema fyrir `GACAssemblies`).
    > - Keyrðu eftirfarandi SQL-skipun í viðskiptagagnagrunninum (AXDB):
    >
    > ```sql 
    > delete from storagefoler
    > ```

1. Keyrðu eftirfarandi SQL-skipanir í viðskiptagagnagrunninum (AXDB):

    ```sql
    delete from FEATUREMANAGEMENTMETADATA
    delete from FEATUREMANAGEMENTSTATE
    delete from NUMBERSEQUENCESCOPE
    ```

1. Staðfestu að breytingarakning hafi verið virkjuð í viðskiptagagnagrunninum (AXDB)
    1. Ræstu SQL Server Management Studio (SSMS).
    1. Hægrismelltu á viðskiptagagnagrunninn þinn (AXDB) og veldu eiginleika.
    1. Í glugganum sem opnast skal velja **Breyta rakningu** og gera eftirfarandi stillingar:

        - **Breyta rakningu:** *Satt*
        - **Varðveislutímabil:** *7*
        - **Varðveislueiningar:** *Dagar*
        - **Sjálfvirk hreinsun:** *Satt*

1. Í verkfærinu skal velja **3. Setja upp vinnuálag**. Síðan skal keyra eftirfarandi skref:
    1. Veldu **1. Setja upp í miðstöð**.
    1. Veldu **2. Setja upp í kvörðunareiningu**.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
