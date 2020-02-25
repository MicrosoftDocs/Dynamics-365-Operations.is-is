---
title: Búa til útflutningsforrit fyrir endurtekin gögn
description: Þessi grein sýnir hvernig á að búa til Microsoft Azure rökfræðiforrit sem flytur út gögn frá Microsoft Dynamics 365 Human Resources á endurtekinni áætlun.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: edd4b999624a845fc145ed9ff348ae9cba782719
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009368"
---
# <a name="create-a-recurring-data-export-app"></a><span data-ttu-id="38f62-103">Búa til útflutningsforrit fyrir endurtekin gögn</span><span class="sxs-lookup"><span data-stu-id="38f62-103">Create a recurring data export app</span></span>

<span data-ttu-id="38f62-104">Þessi grein sýnir hvernig á að búa til Microsoft Azure rökfræðiforrit sem flytur út gögn frá Microsoft Dynamics 365 Human Resources á endurtekinni áætlun.</span><span class="sxs-lookup"><span data-stu-id="38f62-104">This article shows how to create a Microsoft Azure logic app that exports data from Microsoft Dynamics 365 Human Resources on a recurring schedule.</span></span> <span data-ttu-id="38f62-105">Kennslan nýtir sér DMF pakka REST forritunarviðmóts mannauðsmála (API) til að flytja gögnin út.</span><span class="sxs-lookup"><span data-stu-id="38f62-105">The tutorial takes advantage of Human Resources' DMF package REST application programming interface (API) to export the data.</span></span> <span data-ttu-id="38f62-106">Eftir að gögnin hafa verið flutt út vistar rökfræðiforritið útflutta gagnapakkann til Microsoft OneDrive fyrir viðskiptamöppu.</span><span class="sxs-lookup"><span data-stu-id="38f62-106">After the data has been exported, the logic app saves the exported data package to a Microsoft OneDrive for Business folder.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="38f62-107">Sviðsmynd fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="38f62-107">Business scenario</span></span>

<span data-ttu-id="38f62-108">Í einni dæmigerðri atburðarás fyrir Microsoft Dynamics 365 samþættingar, gögn verða að vera flutt út í ofansækin kerfi eftir endurteknum tímaáætlun.</span><span class="sxs-lookup"><span data-stu-id="38f62-108">In one typical business scenario for Microsoft Dynamics 365 integrations, data must be exported to a downstream system on a recurring schedule.</span></span> <span data-ttu-id="38f62-109">Þessi kennsla sýnir hvernig á að flytja út allar starfsmannaskrár úr Microsoft Dynamics 365 Human Resources og vista lista yfir starfsmenn í OneDrive fyrir viðskiptamöppu.</span><span class="sxs-lookup"><span data-stu-id="38f62-109">This tutorial shows how to export all worker records from Microsoft Dynamics 365 Human Resources and save the list of workers in a OneDrive for Business folder.</span></span>

> [!TIP]
> <span data-ttu-id="38f62-110">Sértæk gögn sem eru flutt út í þessari kennslu og ákvörðunarstað gagna eru aðeins dæmi.</span><span class="sxs-lookup"><span data-stu-id="38f62-110">The specific data that is exported in this tutorial and the destination of the exported data are only examples.</span></span> <span data-ttu-id="38f62-111">Þú getur auðveldlega breytt þeim til að mæta viðskiptaþörfum þínum.</span><span class="sxs-lookup"><span data-stu-id="38f62-111">You can easily change them to meet your business needs.</span></span>

## <a name="technologies-used"></a><span data-ttu-id="38f62-112">Tækni notuð</span><span class="sxs-lookup"><span data-stu-id="38f62-112">Technologies used</span></span>

<span data-ttu-id="38f62-113">Þessi kennsla notar eftirfarandi tækni:</span><span class="sxs-lookup"><span data-stu-id="38f62-113">This tutorial uses the following technologies:</span></span>

- <span data-ttu-id="38f62-114">**[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)**- Aðalgagnagjafi fyrir starfsmenn sem verða fluttir út.</span><span class="sxs-lookup"><span data-stu-id="38f62-114">**[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – The master data source for workers that will be exported.</span></span>
- <span data-ttu-id="38f62-115">**[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** - Tæknin sem veitir skipulagningu og tímasetningu endurtekinna útflutnings.</span><span class="sxs-lookup"><span data-stu-id="38f62-115">**[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – The technology that provides orchestration and scheduling of the recurring export.</span></span>

    - <span data-ttu-id="38f62-116">**[Tengi](https://docs.microsoft.com/azure/connectors/apis-list)** - Tæknin sem er notuð til að tengja rökfræðiforritið við nauðsynlega endapunkta.</span><span class="sxs-lookup"><span data-stu-id="38f62-116">**[Connectors](https://docs.microsoft.com/azure/connectors/apis-list)** – The technology that is used to connect the logic app to the required endpoints.</span></span>

        - <span data-ttu-id="38f62-117">[HTTP með Azure AD](https://docs.microsoft.com/connectors/webcontents/) tengi</span><span class="sxs-lookup"><span data-stu-id="38f62-117">[HTTP with Azure AD](https://docs.microsoft.com/connectors/webcontents/) connector</span></span>
        - <span data-ttu-id="38f62-118">[OneDrive fyrir Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) tengi</span><span class="sxs-lookup"><span data-stu-id="38f62-118">[OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) connector</span></span>

- <span data-ttu-id="38f62-119">**[DMF-pakki REST API](../dev-itpro/data-entities/data-management-api.md)** - Tæknin sem notuð er til að koma útflutningi af stað og fylgjast með framvindu þess.</span><span class="sxs-lookup"><span data-stu-id="38f62-119">**[DMF package REST API](../dev-itpro/data-entities/data-management-api.md)** – The technology that is used to trigger the export and monitor its progress.</span></span>
- <span data-ttu-id="38f62-120">**[OneDrive fyrir viðskipti](https://onedrive.live.com/about/business/)** - Áfangastaðurinn fyrir útfluttu starfsmennina.</span><span class="sxs-lookup"><span data-stu-id="38f62-120">**[OneDrive for Business](https://onedrive.live.com/about/business/)** – The destination for the exported workers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="38f62-121">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="38f62-121">Prerequisites</span></span>

<span data-ttu-id="38f62-122">Áður en þú byrjar að æfa þig í þessari kennslu verðurðu að hafa eftirfarandi atriði:</span><span class="sxs-lookup"><span data-stu-id="38f62-122">Before you begin the exercise in this tutorial, you must have the following items:</span></span>

- <span data-ttu-id="38f62-123">Mannauðsumhverfi sem hefur leyfi stjórnanda á umhverfinu</span><span class="sxs-lookup"><span data-stu-id="38f62-123">A Human Resources environment that has admin-level permissions in the environment</span></span>
- <span data-ttu-id="38f62-124">[Azure áskrift](https://azure.microsoft.com/free/) til að hýsa rökfræðiforritið</span><span class="sxs-lookup"><span data-stu-id="38f62-124">An [Azure subscription](https://azure.microsoft.com/free/) to host the logic app</span></span>

## <a name="the-exercise"></a><span data-ttu-id="38f62-125">Æfingin</span><span class="sxs-lookup"><span data-stu-id="38f62-125">The exercise</span></span>

<span data-ttu-id="38f62-126">Í lok þessarar æfingar muntu hafa rökfræðiforrit sem er tengt mannauðsumhverfi þínu og þínu OneDrive fyrir viðskiptareikning.</span><span class="sxs-lookup"><span data-stu-id="38f62-126">At the end of this exercise, you will have a logic app that is connected to your Human Resources environment and your OneDrive for Business account.</span></span> <span data-ttu-id="38f62-127">Rökfræðiforritið mun flytja út gagnapakka frá mannauðsmálum, bíða eftir að útflutningi ljúki, hlaða niður útflutta gagnapakkanum og vista gagnapakkann í OneDrive fyrir viðskiptamöppu sem þú tilgreindi.</span><span class="sxs-lookup"><span data-stu-id="38f62-127">The logic app will export a data package from Human Resources, wait for the export to be completed, download the exported data package, and save the data package in the OneDrive for Business folder that you specified.</span></span>

<span data-ttu-id="38f62-128">Lokið rökfræðiforrit mun líkjast eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="38f62-128">The completed logic app will resemble the following illustration.</span></span>

![Yfirlit yfir rökfræðiforrit](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a><span data-ttu-id="38f62-130">Skref 1: Búðu til gagnaútflutningsverkefni í mannauðsmálum</span><span class="sxs-lookup"><span data-stu-id="38f62-130">Step 1: Create a data export project in Human Resources</span></span>

<span data-ttu-id="38f62-131">Í Human Resources skaltu búa til gagnaútflutningsverkefni sem flytur starfsfólk út.</span><span class="sxs-lookup"><span data-stu-id="38f62-131">In Human Resources, create a data export project that exports workers.</span></span> <span data-ttu-id="38f62-132">Nefnið verkefnið **Flytja út starfskrafta**, og passaðu að valkosturinn **Mynda gagnapakka** sé stilltur á **Já**.</span><span class="sxs-lookup"><span data-stu-id="38f62-132">Name the project **Export Workers**, and make sure that the **Generate data package** option is set to **Yes**.</span></span> <span data-ttu-id="38f62-133">Bættu við einni heild (**Starfskraftur**) í verkið og veldu sniðið sem á að flytja út í.</span><span class="sxs-lookup"><span data-stu-id="38f62-133">Add a single entity (**Worker**) to the project, and select the format to export in.</span></span> <span data-ttu-id="38f62-134">(Microsoft Excel snið er notað í þessari kennslu.)</span><span class="sxs-lookup"><span data-stu-id="38f62-134">(Microsoft Excel format is used in this tutorial.)</span></span>

![Verkefni útflutnings starfsmanna](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> <span data-ttu-id="38f62-136">Mundu heiti gagnaútflutningsverksins.</span><span class="sxs-lookup"><span data-stu-id="38f62-136">Remember the name of the data export project.</span></span> <span data-ttu-id="38f62-137">Þú þarft það þegar þú býrð til rökfræðiforritið í næsta skrefi.</span><span class="sxs-lookup"><span data-stu-id="38f62-137">You will need it when you create the logic app in the next step.</span></span>

### <a name="step-2-create-the-logic-app"></a><span data-ttu-id="38f62-138">Skref 2: Búðu til rökfræðiforritið</span><span class="sxs-lookup"><span data-stu-id="38f62-138">Step 2: Create the logic app</span></span>

<span data-ttu-id="38f62-139">Meginhluti æfingarinnar felur í sér að búa til rökfræðiforritið.</span><span class="sxs-lookup"><span data-stu-id="38f62-139">The bulk of the exercise involves creating the logic app.</span></span>

1. <span data-ttu-id="38f62-140">Búðu til rökfræðiforrit í Azure-gáttinni.</span><span class="sxs-lookup"><span data-stu-id="38f62-140">In the Azure portal, create a logic app.</span></span>

    ![Búðu til síðu með rökfræðiforriti](media/integration-logic-app-creation-1.png)

2. <span data-ttu-id="38f62-142">Byrjaðu með autt rökfræðiforrit hjá Logic Apps Designer.</span><span class="sxs-lookup"><span data-stu-id="38f62-142">In the Logic Apps Designer, start with a blank logic app.</span></span>
3. <span data-ttu-id="38f62-143">Bættu við [Kveikja á endurkomuáætlun](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence) til að keyra rökfræðiforritið á 24 tíma fresti (eða samkvæmt áætlun að eigin vali).</span><span class="sxs-lookup"><span data-stu-id="38f62-143">Add a [Recurrence Schedule trigger](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence) to run the logic app every 24 hours (or according to a schedule of your choice).</span></span>

    ![Endurtekinn svargluggi](media/integration-logic-app-recurrence-step.png)

4. <span data-ttu-id="38f62-145">Kallaðu í [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API til að tímasetja útflutning á gagnapakkanum.</span><span class="sxs-lookup"><span data-stu-id="38f62-145">Call the [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API to schedule the export of your data package.</span></span>

    1. <span data-ttu-id="38f62-146">Notaðu aðgerðina **Kalla á HTTP-beiðni** frá HTTP með Azure AD-tengi.</span><span class="sxs-lookup"><span data-stu-id="38f62-146">Use the **Invoke an HTTP request** action from the HTTP with Azure AD connector.</span></span>

        - <span data-ttu-id="38f62-147">**Grunnslóð URL:** Slóðin á mannauðssumhverfið þitt (Ekki hafa upplýsingar um slóð / nafnrými.)</span><span class="sxs-lookup"><span data-stu-id="38f62-147">**Base Resource URL:** The URL of your Human Resources environment (Don't include path/namespace information.)</span></span>
        - <span data-ttu-id="38f62-148">**Azure AD Slóð tilfanga:** `http://hr.talent.dynamics.com`</span><span class="sxs-lookup"><span data-stu-id="38f62-148">**Azure AD Resource URI:** `http://hr.talent.dynamics.com`</span></span>

        > [!NOTE]
        > <span data-ttu-id="38f62-149">Mannauðsþjónustan býður ekki enn upp á tengi sem afhjúpar öll API sem samanstanda af REST API fyrir DMF pakka, svo sem **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="38f62-149">The Human Resources service doesn't yet provide a connector that exposes all the APIs that make up the DMF package REST API, such as **ExportToPackage**.</span></span> <span data-ttu-id="38f62-150">Í staðinn verður þú að hringja í API með því að nota hráar HTTPS beiðnir í gegnum HTTP með Azure AD-tengi.</span><span class="sxs-lookup"><span data-stu-id="38f62-150">Instead, you must call the APIs by using raw HTTPS requests through the HTTP with Azure AD connector.</span></span> <span data-ttu-id="38f62-151">Þetta tengi notar Azure Active Directory (Azure AD) fyrir sannvottun og heimild til Human Resources.</span><span class="sxs-lookup"><span data-stu-id="38f62-151">This connector uses Azure Active Directory (Azure AD) for authentication and authorization to Human Resources.</span></span>

        ![HTTP með Azure AD-tengi](media/integration-logic-app-http-aad-connector-step.png)

    2. <span data-ttu-id="38f62-153">Skráðu þig inn í mannauðsumhverfið þitt í gegnum HTTP með Azure AD-tengi.</span><span class="sxs-lookup"><span data-stu-id="38f62-153">Sign in to your Human Resources environment through the HTTP with Azure AD connector.</span></span>
    3. <span data-ttu-id="38f62-154">Settu upp HTTP **POST** beiðni um að kalla í **ExportToPackage** DMF REST API.</span><span class="sxs-lookup"><span data-stu-id="38f62-154">Set up an HTTP **POST** request to call the **ExportToPackage** DMF REST API.</span></span>

        - <span data-ttu-id="38f62-155">**Aðferð:** POST</span><span class="sxs-lookup"><span data-stu-id="38f62-155">**Method:** POST</span></span>
        - <span data-ttu-id="38f62-156">**Vefslóð beiðninnar:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span><span class="sxs-lookup"><span data-stu-id="38f62-156">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span></span>
        - <span data-ttu-id="38f62-157">**Meginmál beiðnar:**</span><span class="sxs-lookup"><span data-stu-id="38f62-157">**Body of the request:**</span></span>

            ```JSON
            {
                "definitionGroupId":"Export Workers",
                "packageName":"talent_package.zip",
                "executionId":"",
                "reExecute":false,
                "legalEntityId":"USMF"
            }
            ```

        ![Bjóddu aðgerð á HTTP beiðni](media/integration-logic-app-export-to-package-step.png)

    > [!TIP]
    > <span data-ttu-id="38f62-159">Þú gætir viljað endurnefna hvert skref svo það sé meira máli en sjálfgefið nafn, **Kallaðu á HTTP beiðni**.</span><span class="sxs-lookup"><span data-stu-id="38f62-159">You might want to rename each step so that it's more meaningful than the default name, **Invoke an HTTP request**.</span></span> <span data-ttu-id="38f62-160">Til dæmis er hægt að endurnefna þetta skref **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="38f62-160">For example, you can rename this step **ExportToPackage**.</span></span>

5. <span data-ttu-id="38f62-161">[Frumstilla breytu](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) til að geyma framkvæmdastöðuna á **ExportToPackage** beiðni.</span><span class="sxs-lookup"><span data-stu-id="38f62-161">[Initialize a variable](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) to store the execution status of the **ExportToPackage** request.</span></span>

    ![Frumstilla breytilega aðgerð](media/integration-logic-app-initialize-variable-step.png)

6. <span data-ttu-id="38f62-163">Bíddu þar til framkvæmdastöðin fyrir gagnaútflutninginn er **Tókst**.</span><span class="sxs-lookup"><span data-stu-id="38f62-163">Wait until the execution status of the data export is **Succeeded**.</span></span>

    1. <span data-ttu-id="38f62-164">Bættu við [Þar til lykkja](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop) sem er endurtekin þar til gildið breytan **ExecutionStatus** er **Tókst**.</span><span class="sxs-lookup"><span data-stu-id="38f62-164">Add an [Until loop](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop) that repeats until the value of the **ExecutionStatus** variable is **Succeeded**.</span></span>
    2. <span data-ttu-id="38f62-165">Bættu við aðgerðinni **Töf** sem bíður í fimm sekúndur áður en hún kannar núverandi framkvæmdastöðu útflutningsins.</span><span class="sxs-lookup"><span data-stu-id="38f62-165">Add a **Delay** action that waits five seconds before it polls for the current execution status of the export.</span></span>

        ![Þangað til lykkjuílát](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > <span data-ttu-id="38f62-167">Stilltu mörkin við **15** til að bíða að hámarki 75 sekúndur (15 endurtekningar × 5 sekúndur) til að útflutningi verði lokið.</span><span class="sxs-lookup"><span data-stu-id="38f62-167">Set the limit count to **15** to wait a maximum of 75 seconds (15 iterations × 5 seconds) for the export to be completed.</span></span> <span data-ttu-id="38f62-168">Ef útflutningur þinn tekur lengri tíma, aðlagaðu mörkin eftir því sem við á.</span><span class="sxs-lookup"><span data-stu-id="38f62-168">If your export takes more time, adjust the limit count as appropriate.</span></span>        

    3. <span data-ttu-id="38f62-169">Bættu við aðgerðinni **Kalla á HTTP-beiðni** til að kalla í [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API, og stilltu breytuna **ExecutionStatus** til að fá svarið **GetExecutionSummaryStatus**.</span><span class="sxs-lookup"><span data-stu-id="38f62-169">Add an **Invoke HTTP request** action to call the [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API, and set the **ExecutionStatus** variable to the result of the **GetExecutionSummaryStatus** response.</span></span>

        > <span data-ttu-id="38f62-170">Þetta sýnishorn gerir ekki villu við athugun.</span><span class="sxs-lookup"><span data-stu-id="38f62-170">This sample doesn't do error checking.</span></span> <span data-ttu-id="38f62-171">**GetExecutionSummaryStatus** API getur skilað afgreiðslustöðum sem ekki ná árangri (það er, aðrar stöður en **Tókst**).</span><span class="sxs-lookup"><span data-stu-id="38f62-171">The **GetExecutionSummaryStatus** API can return non-successful terminal states (that is, states other than **Succeeded**).</span></span> <span data-ttu-id="38f62-172">Nánari upplýsingar fást í fylgigögnum um [API](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).</span><span class="sxs-lookup"><span data-stu-id="38f62-172">For more information, see the [API documentation](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).</span></span>

        - <span data-ttu-id="38f62-173">**Aðferð:** POST</span><span class="sxs-lookup"><span data-stu-id="38f62-173">**Method:** POST</span></span>
        - <span data-ttu-id="38f62-174">**Vefslóð beiðninnar:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span><span class="sxs-lookup"><span data-stu-id="38f62-174">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span></span>
        - <span data-ttu-id="38f62-175">**Meginmál beiðninnar:** body('Invoke\_an\_HTTP\_request')?['value']</span><span class="sxs-lookup"><span data-stu-id="38f62-175">**Body of the request:** body('Invoke\_an\_HTTP\_request')?['value']</span></span>

            > [!NOTE]
            > <span data-ttu-id="38f62-176">Þú gætir þurft að slá inn gildið **Meginmál beiðninnar** annaðhvort í kóðaskjá eða í aðgerðir ritstjóra í hönnuðinum.</span><span class="sxs-lookup"><span data-stu-id="38f62-176">You might have to enter the **Body of the request** value either in code view or in the function editor in the designer.</span></span>

        ![Bjóddu aðgerð á HTTP 2 beiðni](media/integration-logic-app-get-execution-status-step.png)

        ![Stilla aðgerð breytu](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > <span data-ttu-id="38f62-179">Gildið fyrir aðgerðina **Stilla breytu** (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) mun vera frábrugðið gildi fyrir meginmálsgildið **Kalla á HTTP beiðni 2**, jafnvel þó að hönnuðurinn sýni gildin á sama hátt.</span><span class="sxs-lookup"><span data-stu-id="38f62-179">The value for the **Set variable** action (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) will differ from the value for the **Invoke an HTTP request 2** body value, even though the designer will show the values in the same way.</span></span>

7. <span data-ttu-id="38f62-180">Sæktu niðurflutta slóð útflutts pakkans.</span><span class="sxs-lookup"><span data-stu-id="38f62-180">Get the download URL of the exported package.</span></span>

    - <span data-ttu-id="38f62-181">Bættu við aðgerðinni **Kalla á HTTP beiðni** til að kalla í [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST API.</span><span class="sxs-lookup"><span data-stu-id="38f62-181">Add an **Invoke HTTP request** action to call the [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST API.</span></span>

        - <span data-ttu-id="38f62-182">**Aðferð:** POST</span><span class="sxs-lookup"><span data-stu-id="38f62-182">**Method:** POST</span></span>
        - <span data-ttu-id="38f62-183">**Vefslóð beiðninnar:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span><span class="sxs-lookup"><span data-stu-id="38f62-183">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span></span>
        - <span data-ttu-id="38f62-184">**Meginmál beiðninnar:** {"executionId": body('GetExportedPackageURL')?['gildi']}</span><span class="sxs-lookup"><span data-stu-id="38f62-184">**Body of the request:** {"executionId": body('GetExportedPackageURL')?['value']}</span></span>

        ![Aðgerðin GetExportedPackageURL](media/integration-logic-app-get-exported-package-step.png)

8. <span data-ttu-id="38f62-186">Sæktu útflutta pakkann.</span><span class="sxs-lookup"><span data-stu-id="38f62-186">Download the exported package.</span></span>

    - <span data-ttu-id="38f62-187">Bættu við HTTP-beiðninni **GET** (innbyggt [Aðgerð HTTP tengis](https://docs.microsoft.com/azure/connectors/connectors-native-http)) til að hlaða niður pakkanum af slóðinni sem var skilað í fyrra skrefi.</span><span class="sxs-lookup"><span data-stu-id="38f62-187">Add an HTTP **GET** request (a built-in [HTTP connector action](https://docs.microsoft.com/azure/connectors/connectors-native-http)) to download the package from the URL that was returned in the previous step.</span></span>

        - <span data-ttu-id="38f62-188">**Aðferð:** GET</span><span class="sxs-lookup"><span data-stu-id="38f62-188">**Method:** GET</span></span>
        - <span data-ttu-id="38f62-189">**URI:** body('Invoke\_an\_HTTP\_request\_3').value</span><span class="sxs-lookup"><span data-stu-id="38f62-189">**URI:** body('Invoke\_an\_HTTP\_request\_3').value</span></span>

            > [!NOTE]
            > <span data-ttu-id="38f62-190">Þú gætir þurft að slá inn gildið **URI** annaðhvort í kóðaskjá eða í aðgerðir ritstjóra í hönnuðinum.</span><span class="sxs-lookup"><span data-stu-id="38f62-190">You might have to enter the **URI** value either in code view or in the function editor in the designer.</span></span>

        ![Aðgerðin HTTP GET](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > <span data-ttu-id="38f62-192">Þessi beiðni þarf ekki frekari sannvottun vegna þess að slóðin sem **GetExportedPackageUrl** API skilar samanstendur af samnýttum undirskriftartákni sem veitir aðgang til að hlaða niður skránni.</span><span class="sxs-lookup"><span data-stu-id="38f62-192">This request doesn't require any additional authentication, because the URL that the **GetExportedPackageUrl** API returns includes a shared access signatures token that grants access to download the file.</span></span>

9. <span data-ttu-id="38f62-193">Vistaðu pakkann sem hlaðið var niður með því að nota [OneDrive fyrir viðskipti](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) tengi.</span><span class="sxs-lookup"><span data-stu-id="38f62-193">Save the downloaded package by using the [OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) connector.</span></span>

    - <span data-ttu-id="38f62-194">Bættu við aðgerðinni OneDrive fyrir viðskipti [Búðu til skrá](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file).</span><span class="sxs-lookup"><span data-stu-id="38f62-194">Add a OneDrive for Business [Create File](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file) action.</span></span>
    - <span data-ttu-id="38f62-195">Tengstu þínu OneDrive fyrir viðskiptareikning, eins og krafist er.</span><span class="sxs-lookup"><span data-stu-id="38f62-195">Connect to your OneDrive for Business account, as required.</span></span>

        - <span data-ttu-id="38f62-196">**Möppuslóð:** Mappa að eigin vali</span><span class="sxs-lookup"><span data-stu-id="38f62-196">**Folder Path:** A folder of your choice</span></span>
        - <span data-ttu-id="38f62-197">**Skráarnafn:** starfskraftur\_package.zip</span><span class="sxs-lookup"><span data-stu-id="38f62-197">**File Name:** worker\_package.zip</span></span>
        - <span data-ttu-id="38f62-198">**Skráarefni:** Meginmál úr fyrra skrefi (kvikt efni)</span><span class="sxs-lookup"><span data-stu-id="38f62-198">**File Content:** The body from the previous step (dynamic content)</span></span>

        ![Stofna skráaraðgerð](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a><span data-ttu-id="38f62-200">Skref 3: Prófaðu rökfræðiforritið</span><span class="sxs-lookup"><span data-stu-id="38f62-200">Step 3: Test the logic app</span></span>

<span data-ttu-id="38f62-201">Til að prófa rökfræðiforritið þitt skaltu velja hnappinn **Hlaupa** í hönnuðinum.</span><span class="sxs-lookup"><span data-stu-id="38f62-201">To test your logic app, select the **Run** button in the designer.</span></span> <span data-ttu-id="38f62-202">Þú munt sjá að skrefin í rökfræðiforritinu byrja að keyra.</span><span class="sxs-lookup"><span data-stu-id="38f62-202">You will see that the steps of the logic app start to run.</span></span> <span data-ttu-id="38f62-203">Eftir 30 til 40 sekúndur ætti rökfræðiforritið að klára að keyra og þitt OneDrive fyrir viðskiptamöppu ætti að innihalda nýja pakkaskrá sem inniheldur útfluttu starfsmennina.</span><span class="sxs-lookup"><span data-stu-id="38f62-203">After 30 to 40 seconds, the logic app should finish running, and your OneDrive for Business folder should include a new package file that contains the exported workers.</span></span>

<span data-ttu-id="38f62-204">Ef tilkynnt er um bilun í einhverju skrefi, veldu misheppnaða skref hönnuðarins og skoðaðu reitina **Inntök** og **Úttök** fyrir það.</span><span class="sxs-lookup"><span data-stu-id="38f62-204">If a failure is reported for any step, select the failed step in the designer, and examine the **Inputs** and **Outputs** fields for it.</span></span> <span data-ttu-id="38f62-205">Kemba og aðlaga skrefið eins og þarf til að leiðrétta villurnar.</span><span class="sxs-lookup"><span data-stu-id="38f62-205">Debug and adjust the step as required to correct the errors.</span></span>

<span data-ttu-id="38f62-206">Eftirfarandi mynd sýnir hvernig Logic Apps Designer lítur út þegar öll skref í rökfræðiforritinu ganga vel.</span><span class="sxs-lookup"><span data-stu-id="38f62-206">The following illustration shows what the Logic Apps Designer looks like when all the steps of the logic app run successfully.</span></span>

![Árangursrík rökfræðiforrit keyrt](media/integration-logic-app-successful-run.png)

## <a name="summary"></a><span data-ttu-id="38f62-208">Samantekt</span><span class="sxs-lookup"><span data-stu-id="38f62-208">Summary</span></span>

<span data-ttu-id="38f62-209">Í þessari einkatími lærðir þú hvernig á að nota rökfræðiforrit til að flytja gögn úr mannauðsmálum og vista útflutt gögn í OneDrive fyrir viðskiptamöppu.</span><span class="sxs-lookup"><span data-stu-id="38f62-209">In this tutorial, you learned how to use a logic app to export data from Human Resources and save the exported data to a OneDrive for Business folder.</span></span> <span data-ttu-id="38f62-210">Þú getur breytt skrefunum í þessari kennslu eins og þörf krefur til að henta þínum viðskiptaþörfum.</span><span class="sxs-lookup"><span data-stu-id="38f62-210">You can modify the steps of this tutorial as required to suit your business needs.</span></span>


