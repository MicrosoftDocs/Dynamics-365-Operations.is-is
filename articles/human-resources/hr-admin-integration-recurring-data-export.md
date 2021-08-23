---
title: Búa til útflutningsforrit fyrir endurtekin gögn
description: Þessi grein sýnir hvernig á að búa til Microsoft Azure rökfræðiforrit sem flytur út gögn frá Microsoft Dynamics 365 Human Resources á endurtekinni áætlun.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cef9e7f78646a4a5794eb14a9f1ad355768480644504c548afbb32e23fff4cd5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744871"
---
# <a name="create-a-recurring-data-export-app"></a>Búa til útflutningsforrit fyrir endurtekin gögn

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þessi grein sýnir hvernig á að búa til Microsoft Azure rökfræðiforrit sem flytur út gögn frá Microsoft Dynamics 365 Human Resources á endurtekinni áætlun. Kennslan nýtir sér DMF pakka REST forritunarviðmóts mannauðsmála (API) til að flytja gögnin út. Eftir að gögnin hafa verið flutt út vistar rökfræðiforritið útflutta gagnapakkann til Microsoft OneDrive fyrir viðskiptamöppu.

## <a name="business-scenario"></a>Sviðsmynd fyrirtækis

Í einni dæmigerðri atburðarás fyrir Microsoft Dynamics 365 samþættingar, gögn verða að vera flutt út í ofansækin kerfi eftir endurteknum tímaáætlun. Þessi kennsla sýnir hvernig á að flytja út allar starfsmannaskrár úr Microsoft Dynamics 365 Human Resources og vista lista yfir starfsmenn í OneDrive fyrir viðskiptamöppu.

> [!TIP]
> Sértæk gögn sem eru flutt út í þessari kennslu og ákvörðunarstað gagna eru aðeins dæmi. Þú getur auðveldlega breytt þeim til að mæta viðskiptaþörfum þínum.

## <a name="technologies-used"></a>Tækni notuð

Þessi kennsla notar eftirfarandi tækni:

- **[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)**- Aðalgagnagjafi fyrir starfsmenn sem verða fluttir út.
- **[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** - Tæknin sem veitir skipulagningu og tímasetningu endurtekinna útflutnings.

    - **[Tengi](/azure/connectors/apis-list)** - Tæknin sem er notuð til að tengja rökfræðiforritið við nauðsynlega endapunkta.

        - [HTTP með Azure AD](/connectors/webcontents/) tengi
        - [OneDrive fyrir Business](/azure/connectors/connectors-create-api-onedriveforbusiness) tengi

- **[DMF-pakki REST API](../fin-ops-core/dev-itpro/data-entities/data-management-api.md)** - Tæknin sem notuð er til að koma útflutningi af stað og fylgjast með framvindu þess.
- **[OneDrive fyrir viðskipti](https://onedrive.live.com/about/business/)** - Áfangastaðurinn fyrir útfluttu starfsmennina.

## <a name="prerequisites"></a>Forkröfur

Áður en þú byrjar að æfa þig í þessari kennslu verðurðu að hafa eftirfarandi atriði:

- Mannauðsumhverfi sem hefur leyfi stjórnanda á umhverfinu
- [Azure áskrift](https://azure.microsoft.com/free/) til að hýsa rökfræðiforritið

## <a name="the-exercise"></a>Æfingin

Í lok þessarar æfingar muntu hafa rökfræðiforrit sem er tengt mannauðsumhverfi þínu og þínu OneDrive fyrir viðskiptareikning. Rökfræðiforritið mun flytja út gagnapakka frá mannauðsmálum, bíða eftir að útflutningi ljúki, hlaða niður útflutta gagnapakkanum og vista gagnapakkann í OneDrive fyrir viðskiptamöppu sem þú tilgreindi.

Lokið rökfræðiforrit mun líkjast eftirfarandi mynd.

![Yfirlit yfir rökfræðiforrit.](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a>Skref 1: Búðu til gagnaútflutningsverkefni í mannauðsmálum

Í Human Resources skaltu búa til gagnaútflutningsverkefni sem flytur starfsfólk út. Nefnið verkefnið **Flytja út starfskrafta**, og passaðu að valkosturinn **Mynda gagnapakka** sé stilltur á **Já**. Bættu við einni heild (**Starfskraftur**) í verkið og veldu sniðið sem á að flytja út í. (Microsoft Excel snið er notað í þessari kennslu.)

![Gagnaverk vegna útflutnings starfsmanns.](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> Mundu heiti gagnaútflutningsverksins. Þú þarft það þegar þú býrð til rökfræðiforritið í næsta skrefi.

### <a name="step-2-create-the-logic-app"></a>Skref 2: Búðu til rökfræðiforritið

Meginhluti æfingarinnar felur í sér að búa til rökfræðiforritið.

1. Búðu til rökfræðiforrit í Azure-gáttinni.

    ![Stofnsíða rökfræðiforrits.](media/integration-logic-app-creation-1.png)

2. Byrjaðu með autt rökfræðiforrit hjá Logic Apps Designer.
3. Bættu við [Kveikja á endurkomuáætlun](/azure/connectors/connectors-native-recurrence) til að keyra rökfræðiforritið á 24 tíma fresti (eða samkvæmt áætlun að eigin vali).

    ![Endurtekinn svargluggi.](media/integration-logic-app-recurrence-step.png)

4. Kallaðu í [ExportToPackage](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API til að tímasetja útflutning á gagnapakkanum.

    1. Notaðu aðgerðina **Kalla á HTTP-beiðni** frá HTTP með Azure AD-tengi.

        - **Grunnslóð URL:** Slóðin á mannauðssumhverfið þitt (Ekki hafa upplýsingar um slóð / nafnrými.)
        - **Azure AD Slóð tilfanga:** `http://hr.talent.dynamics.com`

        > [!NOTE]
        > Mannauðsþjónustan býður ekki enn upp á tengi sem afhjúpar öll API sem samanstanda af REST API fyrir DMF pakka, svo sem **ExportToPackage**. Í staðinn verður þú að hringja í API með því að nota hráar HTTPS beiðnir í gegnum HTTP með Azure AD-tengi. Þetta tengi notar Azure Active Directory (Azure AD) fyrir sannvottun og heimild til Human Resources.

        ![HTTP með Azure AD-tengli.](media/integration-logic-app-http-aad-connector-step.png)

    2. Skráðu þig inn í mannauðsumhverfið þitt í gegnum HTTP með Azure AD-tengi.
    3. Settu upp HTTP **POST** beiðni um að kalla í **ExportToPackage** DMF REST API.

        - **Aðferð:** POST
        - **Vefslóð beiðninnar:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage
        - **Meginmál beiðnar:**

            ```JSON
            {
                "definitionGroupId":"Export Workers",
                "packageName":"talent_package.zip",
                "executionId":"",
                "reExecute":false,
                "legalEntityId":"USMF"
            }
            ```

        ![Kalla fram aðgerð HTTP-beiðni.](media/integration-logic-app-export-to-package-step.png)

    > [!TIP]
    > Þú gætir viljað endurnefna hvert skref svo það sé meira máli en sjálfgefið nafn, **Kallaðu á HTTP beiðni**. Til dæmis er hægt að endurnefna þetta skref **ExportToPackage**.

5. [Frumstilla breytu](/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) til að geyma framkvæmdastöðuna á **ExportToPackage** beiðni.

    ![Frumstilla breytilega aðgerð.](media/integration-logic-app-initialize-variable-step.png)

6. Bíddu þar til framkvæmdastöðin fyrir gagnaútflutninginn er **Tókst**.

    1. Bættu við [Þar til lykkja](/azure/logic-apps/logic-apps-control-flow-loops#until-loop) sem er endurtekin þar til gildið breytan **ExecutionStatus** er **Tókst**.
    2. Bættu við aðgerðinni **Töf** sem bíður í fimm sekúndur áður en hún kannar núverandi framkvæmdastöðu útflutningsins.

        ![Þar til geymsla endurtekur sig.](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > Stilltu mörkin við **15** til að bíða að hámarki 75 sekúndur (15 endurtekningar × 5 sekúndur) til að útflutningi verði lokið. Ef útflutningur þinn tekur lengri tíma, aðlagaðu mörkin eftir því sem við á.        

    3. Bættu við aðgerðinni **Kalla á HTTP-beiðni** til að kalla í [GetExecutionSummaryStatus](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API, og stilltu breytuna **ExecutionStatus** til að fá svarið **GetExecutionSummaryStatus**.

        > Þetta sýnishorn gerir ekki villu við athugun. **GetExecutionSummaryStatus** API getur skilað afgreiðslustöðum sem ekki ná árangri (það er, aðrar stöður en **Tókst**). Nánari upplýsingar fást í fylgigögnum um [API](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).

        - **Aðferð:** POST
        - **Vefslóð beiðninnar:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus
        - **Meginmál beiðninnar:** body('Invoke\_an\_HTTP\_request‘)?['value']

            > [!NOTE]
            > Þú gætir þurft að slá inn gildið **Meginmál beiðninnar** annaðhvort í kóðaskjá eða í aðgerðir ritstjóra í hönnuðinum.

        ![Kalla fram aðgerð HTTP-beiðni 2.](media/integration-logic-app-get-execution-status-step.png)

        ![Stilla aðgerð breytu.](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > Gildið fyrir aðgerðina **Stilla breytu** (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) mun vera frábrugðið gildi fyrir meginmálsgildið **Kalla á HTTP beiðni 2**, jafnvel þó að hönnuðurinn sýni gildin á sama hátt.

7. Sæktu niðurflutta slóð útflutts pakkans.

    - Bættu við aðgerðinni **Kalla á HTTP beiðni** til að kalla í [GetExportedPackageUrl](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST API.

        - **Aðferð:** POST
        - **Vefslóð beiðninnar:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl
        - **Meginmál beiðnar:** {"executionId": body('GetExportedPackageURL')?['value']}

        ![Aðgerðin GetExportedPackageURL.](media/integration-logic-app-get-exported-package-step.png)

8. Sæktu útflutta pakkann.

    - Bættu við HTTP-beiðninni **GET** (innbyggt [Aðgerð HTTP tengis](/azure/connectors/connectors-native-http)) til að hlaða niður pakkanum af slóðinni sem var skilað í fyrra skrefi.

        - **Aðferð:** GET
        - **URI:** body('Invoke\_an\_HTTP\_request\_3').value

            > [!NOTE]
            > Þú gætir þurft að slá inn gildið **URI** annaðhvort í kóðaskjá eða í aðgerðir ritstjóra í hönnuðinum.

        ![Aðgerðin HTTP GET.](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > Þessi beiðni þarf ekki frekari sannvottun vegna þess að slóðin sem **GetExportedPackageUrl** API skilar samanstendur af samnýttum undirskriftartákni sem veitir aðgang til að hlaða niður skránni.

9. Vistaðu pakkann sem hlaðið var niður með því að nota [OneDrive fyrir viðskipti](/azure/connectors/connectors-create-api-onedriveforbusiness) tengi.

    - Bættu við aðgerðinni OneDrive fyrir viðskipti [Búðu til skrá](/connectors/onedriveforbusinessconnector/#create-file).
    - Tengstu þínu OneDrive fyrir viðskiptareikning, eins og krafist er.

        - **Möppuslóð:** Mappa að eigin vali
        - **Skráarnafn:** starfskraftur\_package.zip
        - **Skráarefni:** Meginmál úr fyrra skrefi (kvikt efni)

        ![Aðgerðin Stofna skrá.](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a>Skref 3: Prófaðu rökfræðiforritið

Til að prófa rökfræðiforritið þitt skaltu velja hnappinn **Hlaupa** í hönnuðinum. Þú munt sjá að skrefin í rökfræðiforritinu byrja að keyra. Eftir 30 til 40 sekúndur ætti rökfræðiforritið að klára að keyra og þitt OneDrive fyrir viðskiptamöppu ætti að innihalda nýja pakkaskrá sem inniheldur útfluttu starfsmennina.

Ef tilkynnt er um bilun í einhverju skrefi, veldu misheppnaða skref hönnuðarins og skoðaðu reitina **Inntök** og **Úttök** fyrir það. Kemba og aðlaga skrefið eins og þarf til að leiðrétta villurnar.

Eftirfarandi mynd sýnir hvernig Logic Apps Designer lítur út þegar öll skref í rökfræðiforritinu ganga vel.

![Árangursrík keyrsla rökfræðiforrits.](media/integration-logic-app-successful-run.png)

## <a name="summary"></a>Samantekt

Í þessari einkatími lærðir þú hvernig á að nota rökfræðiforrit til að flytja gögn úr mannauðsmálum og vista útflutt gögn í OneDrive fyrir viðskiptamöppu. Þú getur breytt skrefunum í þessari kennslu eins og þörf krefur til að henta þínum viðskiptaþörfum.




[!INCLUDE[footer-include](../includes/footer-banner.md)]