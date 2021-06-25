---
title: Stilling fjármálainnsýnar fyrir opna forútgáfu (forútgáfa) - útgáfa 10.0.20 og nýrri
description: Í þessu efnisatriði er útskýrt hvernig á að stilla kerfið þitt til að nota möguleikana sem eru tiltækir í fjármálainnsýn fyrir opna forútgáfu í útgáfu 10.0.20 og nýrri.
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
ms.search.validFrom: 2021-06-03
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 613bd4816e2f0c4fbb56cf79779a08c6a09592bd
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222613"
---
# <a name="configuration-for-finance-insights-for-public-preview-preview---version-10020-and-later"></a><span data-ttu-id="39bfa-103">Stilling fjármálainnsýnar fyrir opna forútgáfu (forútgáfa) - útgáfa 10.0.20 og nýrri</span><span class="sxs-lookup"><span data-stu-id="39bfa-103">Configuration for Finance insights for public preview (preview) - version 10.0.20 and later</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="39bfa-104">Fjármálainnsýn sameinar virkni Microsoft Dynamics 365 Finance við Dataverse, Azure og AI Builder til að bjóða upp á öflug spáverkfæri fyrir fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="39bfa-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="39bfa-105">Í þessu efnisatriði er útskýrt hvernig á að stilla Dynamics 365 Finance útgáfu 10.0.20 þannig að kerfið þitt geti notað möguleikana sem eru tiltækir í opinni forútgáfu fjármálainnsýnar.</span><span class="sxs-lookup"><span data-stu-id="39bfa-105">This topic explains how to configure Dynamics 365 Finance version 10.0.20 so that your system can use the capabilities that are available in Finance insights public preview.</span></span>

> [!NOTE]
> <span data-ttu-id="39bfa-106">Skrefum skilgreiningarinnar sem lýst í þessu efnisatriði eiga aðeins við um útgáfu 10.0.20 og nýrri af Finance.</span><span class="sxs-lookup"><span data-stu-id="39bfa-106">The configuration steps that are described in this topic apply only to Finance version 10.0.20 and later.</span></span> <span data-ttu-id="39bfa-107">Til að setja upp fjármálainnsýn á útgáfu 10.0.19 og eldri skal sjá [Stilling fjármálainnsýnar - útgáfur fram að 10.0.18](configure-for-fin-insites.md).</span><span class="sxs-lookup"><span data-stu-id="39bfa-107">'To set up Finance insights on version 10.0.19 and earlier, see [Configuration for Finance insights - versions up to 10.0.18](configure-for-fin-insites.md).</span></span>

## <a name="deploy-finance"></a><span data-ttu-id="39bfa-108">Uppsetning Finance</span><span class="sxs-lookup"><span data-stu-id="39bfa-108">Deploy Finance</span></span>

<span data-ttu-id="39bfa-109">Fylgja skal eftirfarandi skrefum til að setja upp umhverfin.</span><span class="sxs-lookup"><span data-stu-id="39bfa-109">Follow these steps to deploy the environments.</span></span>

1. <span data-ttu-id="39bfa-110">Í Microsoft Dynamics Lifecycle Services (LCS) skal stofna eða uppfæra Finance-umhverfi.</span><span class="sxs-lookup"><span data-stu-id="39bfa-110">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Finance environment.</span></span> <span data-ttu-id="39bfa-111">Umhverfið krefst forritsútgáfu 10.0.20 eða nýrri af Finance and Operations forritum.</span><span class="sxs-lookup"><span data-stu-id="39bfa-111">The environment requires app version 10.0.20 or later of Finance and Operations apps.</span></span>
2. <span data-ttu-id="39bfa-112">Umhverfið verður að vera vel tiltækt í Sandbox.</span><span class="sxs-lookup"><span data-stu-id="39bfa-112">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="39bfa-113">(Þessi tegund umhverfis er einnig þekkt sem umhverfi í tveggja laga umhverfi.) Frekari upplýsingar er að finna í [Umhverfisskipulagning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="39bfa-113">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="39bfa-114">Ef þú ert að stilla fjármálainnsýn í sandkassaumhverfi gætirðu þurft að afrita framleiðslugögn í það umhverfi til að spár virki.</span><span class="sxs-lookup"><span data-stu-id="39bfa-114">If you are configuring Finance insights in a Sandbox environment, you might need to copy production data to that environment for predictions to work.</span></span> <span data-ttu-id="39bfa-115">Spálíkanið notar gögn til margra ára til að búa til spár.</span><span class="sxs-lookup"><span data-stu-id="39bfa-115">The prediction model uses multiple years of data to build predictions.</span></span> <span data-ttu-id="39bfa-116">Contoso sýnigögnin innihalda ekki næg söguleg gögn til að hægt sé að þjálfa spálíkanið á fullnægjandi hátt.</span><span class="sxs-lookup"><span data-stu-id="39bfa-116">The Contoso demo data doesn’t contain enough historical data to train the prediction model adequately.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="39bfa-117">Skilgreina Dataverse</span><span class="sxs-lookup"><span data-stu-id="39bfa-117">Configure Dataverse</span></span>

<span data-ttu-id="39bfa-118">Fylgdu eftirfarandi skrefum til að stilla Dataverse fyrir fjármálainnsýn.</span><span class="sxs-lookup"><span data-stu-id="39bfa-118">Follow these steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="39bfa-119">Í LCS skal opna síðu umhverfis og staðfesta að hlutinn **Power Platform samþætting** sé þegar uppsettur.</span><span class="sxs-lookup"><span data-stu-id="39bfa-119">In LCS, open the environment page, and verify that the **Power Platform Integration** section is already set up.</span></span>

    - <span data-ttu-id="39bfa-120">Ef hann er þegar uppsettur ætti heiti Dataverse umhverfisins sem tengt er við Finance-umhverfið að vera sýnt.</span><span class="sxs-lookup"><span data-stu-id="39bfa-120">If it's already set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>
    - <span data-ttu-id="39bfa-121">Ef það er ekki enn uppsett skaltu fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="39bfa-121">If it isn't yet set up, follow these steps:</span></span>

        1. <span data-ttu-id="39bfa-122">Í hlutanum **Power Platform samþætting** skal velja **Uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-122">In the **Power Platform Integration** section, select **Setup**.</span></span> <span data-ttu-id="39bfa-123">Uppsetning umhverfisins getur tekið allt að klukkustund.</span><span class="sxs-lookup"><span data-stu-id="39bfa-123">Setup of the environment might take up to an hour.</span></span>
        2. <span data-ttu-id="39bfa-124">Ef tókst að setja upp Dataverse-umhverfið ætti heiti Dataverse-umhverfisins sem tengt er við Finance-umhverfið að vera sýnt.</span><span class="sxs-lookup"><span data-stu-id="39bfa-124">If the Dataverse environment is successfully set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>

        > [!NOTE]
        > <span data-ttu-id="39bfa-125">Eftir að uppsetningu umhverfisins er lokið skal **ekki** velja **Tengja við CDS fyrir forrit**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-125">After you complete the environment setup, do **not** select **Link to CDS for Apps**.</span></span> <span data-ttu-id="39bfa-126">Þessi hnappur er ekki nauðsynlegur fyrir fjármálainnsýn.</span><span class="sxs-lookup"><span data-stu-id="39bfa-126">This button isn't required for Finance insights.</span></span> <span data-ttu-id="39bfa-127">Ef þú velur hann geturðu ekki stillt nauðsynlegar innbætur við umhverfi í LCS.</span><span class="sxs-lookup"><span data-stu-id="39bfa-127">If you select it, you won't be able to configure the required environment add-ins in LCS.</span></span>

## <a name="configure-azure"></a><span data-ttu-id="39bfa-128">Stilla Azure</span><span class="sxs-lookup"><span data-stu-id="39bfa-128">Configure Azure</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="39bfa-129">Nota Azure Cloud Shell til að setja upp Data Lake-tilföng fjármálainnsýnar</span><span class="sxs-lookup"><span data-stu-id="39bfa-129">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="39bfa-130">Nota Windows PowerShell-forskrift</span><span class="sxs-lookup"><span data-stu-id="39bfa-130">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="39bfa-131">Boðið er upp á Windows PowerShell-forskrift þannig að auðvelt er að setja upp Azure-tilföng sem eru skilgreind í [Grunnstilla útflutning í Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="39bfa-131">A Windows PowerShell script has been provided so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="39bfa-132">Ef frekar er óskað eftir því að setja upp handvirkt skal sleppa þessu ferli og í staðinn ljúka ferlinu í hlutanum [Handvirk uppsetning](#manual-setup).</span><span class="sxs-lookup"><span data-stu-id="39bfa-132">If you prefer to do the setup manually, skip this procedure, and complete the procedure in the [Manual setup](#manual-setup) section instead.</span></span>

> [!NOTE]
> <span data-ttu-id="39bfa-133">Notið eftirfarandi ferli til að keyra forskrift Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="39bfa-133">Use the following procedure to run the Windows PowerShell script.</span></span> <span data-ttu-id="39bfa-134">Uppsetningin virkar hugsanlega ekki ef valkosturinn **Prófaðu þetta** í Azure CLI er notaður eða ef forskriftin er keyrð í tölvunni þinni.</span><span class="sxs-lookup"><span data-stu-id="39bfa-134">The setup might not work if you use the **Try it** option in Azure CLI or if you run the script on your computer.</span></span>

<span data-ttu-id="39bfa-135">Fylgið þessum skrefum til að nota forskrift Windows PowerShell til að stilla Azure.</span><span class="sxs-lookup"><span data-stu-id="39bfa-135">Follow these steps to use the Windows PowerShell script to configure Azure.</span></span> <span data-ttu-id="39bfa-136">Réttindi til að búa til Azure-tilfangaflokk, Azure-tilföng og Azure AD-forrit þurfa að vera til staðar.</span><span class="sxs-lookup"><span data-stu-id="39bfa-136">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="39bfa-137">Frekari upplýsingar um nauðsynlegar heimildir má finna á [Athuga Azure AD heimildir](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="39bfa-137">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="39bfa-138">Í [Azure-gátt](https://portal.azure.com) skal opna viðkomandi Azure-áskrift.</span><span class="sxs-lookup"><span data-stu-id="39bfa-138">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span>
2. <span data-ttu-id="39bfa-139">Veljið **Cloud Shell** hægra megin við svæðið **Leita**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-139">Select **Cloud Shell** to the right of the **Search** field.</span></span>
3. <span data-ttu-id="39bfa-140">Veljið **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-140">Select **PowerShell**.</span></span>
4. <span data-ttu-id="39bfa-141">Búðu til geymslu ef beðið er um að búa hana til.</span><span class="sxs-lookup"><span data-stu-id="39bfa-141">Create storage if you're prompted to create it.</span></span>
5. <span data-ttu-id="39bfa-142">Á flipanum **Azure CLI** skal velja **Afrita**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-142">On the **Azure CLI** tab, select **Copy**.</span></span>
6. <span data-ttu-id="39bfa-143">Opnið nýja skrá í Notepad og límið inn Windows PowerShell-forskriftina.</span><span class="sxs-lookup"><span data-stu-id="39bfa-143">In Notepad, open a new file, and paste in the Windows PowerShell script.</span></span>
7. <span data-ttu-id="39bfa-144">Vistið skrána sem **ConfigureDataLake.ps1**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-144">Save the file as **ConfigureDataLake.ps1**.</span></span>
8. <span data-ttu-id="39bfa-145">Hlaðið upp forskrift Windows PowerShell í lotuna með því að nota valkost valmyndar fyrir upphleðslu í Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="39bfa-145">Upload the Windows PowerShell script to the session by using the menu option for upload in Cloud Shell.</span></span>
9. <span data-ttu-id="39bfa-146">Keyrið **.\ConfigureDataLake.ps1** forskriftina.</span><span class="sxs-lookup"><span data-stu-id="39bfa-146">Run the **.\ConfigureDataLake.ps1** script.</span></span>
10. <span data-ttu-id="39bfa-147">Fylgið kvaðningunum til að keyra forskriftina.</span><span class="sxs-lookup"><span data-stu-id="39bfa-147">Follow the prompts to run the script.</span></span>
11. <span data-ttu-id="39bfa-148">Notið upplýsingar úr forskriftinni til að setja upp innbótina Flytja út í Data Lake í LCS.</span><span class="sxs-lookup"><span data-stu-id="39bfa-148">Use the information from the script output to install the Export to Data Lake add-in in LCS.</span></span>

### <a name="manual-setup"></a><span data-ttu-id="39bfa-149">Handvirk uppsetning</span><span class="sxs-lookup"><span data-stu-id="39bfa-149">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="39bfa-150">Bæta umsóknum við Azure AD leigjanda</span><span class="sxs-lookup"><span data-stu-id="39bfa-150">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="39bfa-151">Í [Azure-gáttinni](https://portal.azure.com) skal fara á **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-151">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="39bfa-152">Veljið **Stjórna \> Enterprise-forrit**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-152">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="39bfa-153">Leitið að eftirfarandi forritum eftir FORRITSKENNINU.</span><span class="sxs-lookup"><span data-stu-id="39bfa-153">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="39bfa-154">Forrit</span><span class="sxs-lookup"><span data-stu-id="39bfa-154">Application</span></span>                              | <span data-ttu-id="39bfa-155">Auðkenni forrits</span><span class="sxs-lookup"><span data-stu-id="39bfa-155">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="39bfa-156">Microsoft Dynamics ERP Microservices</span><span class="sxs-lookup"><span data-stu-id="39bfa-156">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="39bfa-157">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="39bfa-157">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="39bfa-158">Microsoft Dynamics ERP Microservices CDS</span><span class="sxs-lookup"><span data-stu-id="39bfa-158">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="39bfa-159">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="39bfa-159">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="39bfa-160">Heimildaþjónusta AI Builder</span><span class="sxs-lookup"><span data-stu-id="39bfa-160">AI Builder Authorization Service</span></span>         | <span data-ttu-id="39bfa-161">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="39bfa-161">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="39bfa-162">Ef ekki eitthvað af undanfarandi forritum finnst ekki skal prófa eftirfarandi skref.</span><span class="sxs-lookup"><span data-stu-id="39bfa-162">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="39bfa-163">Í staðbundinni tölvu, í **Upphafsvalmyndinni**, skal leita að **powershell**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-163">On your local computer, on the **Start** menu, search for **powershell**.</span></span>
2. <span data-ttu-id="39bfa-164">Velja skal og halda fingri á (eða hægrismella) **Windows PowerShell** og velja svo **Keyra sem stjórnandi**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-164">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="39bfa-165">Keyrið eftirfarandi skipun til að setja upp **AzureAD** einingun.</span><span class="sxs-lookup"><span data-stu-id="39bfa-165">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="39bfa-166">Ef NuGet-veita er nauðsynleg til að halda áfram skal velja **Y** til að setja hana upp.</span><span class="sxs-lookup"><span data-stu-id="39bfa-166">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="39bfa-167">Ef skilaboðin „Ótraust geymslׅa“ birtast skal velja **Y** til að halda áfram.</span><span class="sxs-lookup"><span data-stu-id="39bfa-167">If you receive an "Untrusted repository" message, select **Y** to continue.</span></span>
6. <span data-ttu-id="39bfa-168">Fyrir hvert forrit sem verður að bæta við þarf að keyra eftirfarandi skipanir til að bæta forritinu við Azure AD.</span><span class="sxs-lookup"><span data-stu-id="39bfa-168">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="39bfa-169">Skráðu þig inn sem stjórnandi Azure AD þegar beðið er um það.</span><span class="sxs-lookup"><span data-stu-id="39bfa-169">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="39bfa-170">Stofna Azure-tilföng</span><span class="sxs-lookup"><span data-stu-id="39bfa-170">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="39bfa-171">Ganga skal úr skugga um að eftirfarandi tilföng séu stofnuð í sama Azure AD-tilviki og Dataverse-umhverfið er í.</span><span class="sxs-lookup"><span data-stu-id="39bfa-171">Make sure that you create the following resources in the same Azure AD instance that the Dataverse environment is in.</span></span> <span data-ttu-id="39bfa-172">Ekki er hægt að nota tilföng úr öðru Azure AD-tilviki.</span><span class="sxs-lookup"><span data-stu-id="39bfa-172">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="39bfa-173">Búið til geymslureikning:</span><span class="sxs-lookup"><span data-stu-id="39bfa-173">Create a storage account:</span></span>

    1. <span data-ttu-id="39bfa-174">Í [Azure Portal](https://portal.azure.com) skal stofna geymslureikning.</span><span class="sxs-lookup"><span data-stu-id="39bfa-174">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="39bfa-175">Í svarglugganum **Stofna geymslureikning** skal stilla eftirfarandi svæði:</span><span class="sxs-lookup"><span data-stu-id="39bfa-175">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="39bfa-176">**Staðsetning** – velja gagnamiðstöð með umhverfinu.</span><span class="sxs-lookup"><span data-stu-id="39bfa-176">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="39bfa-177">**Afköst** – mælt er með **Hefðbundin**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-177">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="39bfa-178">**Reikningsgerð** – velja þarf **StorageV2**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-178">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="39bfa-179">Í svarglugganum **Ítarlegir valkostir**, fyrir **Data Lake Storage Gen2**, skal velja **Virkja** undir **Stigveldis nafnabil**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-179">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="39bfa-180">Ef þessi eiginleiki er ekki gerður virkur er ekki hægt að nota gögn sem Finance and Operations-forrit skrifa með þjónustu á borð við Power BI-gagnaflæði.</span><span class="sxs-lookup"><span data-stu-id="39bfa-180">If you don't enable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="39bfa-181">Veljið **yfirfara og búa til**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-181">Select **Review and create**.</span></span> <span data-ttu-id="39bfa-182">Þegar uppsetningu er lokið sést nýja tilfangið til staðar á Azure-gáttinni.</span><span class="sxs-lookup"><span data-stu-id="39bfa-182">When the deployment is completed, the new resource is shown in the Azure portal.</span></span>
    5. <span data-ttu-id="39bfa-183">Opnaðu geymslureikninginn sem þú stofnaðir.</span><span class="sxs-lookup"><span data-stu-id="39bfa-183">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="39bfa-184">Á valmyndinni til vinstri skal velja **Aðgangslyklar**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-184">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="39bfa-185">Afritið og vistið heiti geymslureikningsins.</span><span class="sxs-lookup"><span data-stu-id="39bfa-185">Copy and save the name of the storage account.</span></span> <span data-ttu-id="39bfa-186">Gefa verður upp gildið síðar þegar leyndarmál lyklageymslu er sett upp.</span><span class="sxs-lookup"><span data-stu-id="39bfa-186">You will have to provide this value later, when you set up key vault secrets.</span></span>

2. <span data-ttu-id="39bfa-187">Búið til lyklageymslu:</span><span class="sxs-lookup"><span data-stu-id="39bfa-187">Create a key vault:</span></span>

    1. <span data-ttu-id="39bfa-188">Í [Azure Portal](https://portal.azure.com) skal stofna lyklageymslu.</span><span class="sxs-lookup"><span data-stu-id="39bfa-188">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="39bfa-189">Í svarglugganum **Stofna lyklageymslu** á svæðinu **Staðsetning** skal velja gagnamiðstöðina þar sem umhverfið er að finna.</span><span class="sxs-lookup"><span data-stu-id="39bfa-189">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="39bfa-190">Þegar lyklageymsla hefur verið búin til skal fara í **Yfirlit lyklageymslu** og afrita og vista DNS-heitið.</span><span class="sxs-lookup"><span data-stu-id="39bfa-190">After key vault is created, go to **Key Vault Overview**, and copy and save the DNS name.</span></span> <span data-ttu-id="39bfa-191">Þetta gildi þarf að gefa upp síðar þegar Data Lake-viðbótin er sett upp.</span><span class="sxs-lookup"><span data-stu-id="39bfa-191">You will have to provide this value later, when you set up the Data Lake add-in.</span></span>

3. <span data-ttu-id="39bfa-192">Stofna og skrá Azure AD forrit:</span><span class="sxs-lookup"><span data-stu-id="39bfa-192">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="39bfa-193">Í [Azure-gáttinni](https://portal.azure.com) skal opna **Azure Active Directory** og velja svo **Forritaskráningar**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-193">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="39bfa-194">Velja skal **Ný forritaskráning** og stilla eftirfarandi svæði:</span><span class="sxs-lookup"><span data-stu-id="39bfa-194">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="39bfa-195">**Heiti** - Færið inn heiti forritsins.</span><span class="sxs-lookup"><span data-stu-id="39bfa-195">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="39bfa-196">**Forritsgerð** – Veljið **Vef-API**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-196">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="39bfa-197">**Framsenda URI-uppsetningu** – Sláið inn vefslóð fyrir Dynamics 365-tilvikið, til dæmis, `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="39bfa-197">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="39bfa-198">Opnið forritið sem var búið til og afritið og vistið gildi fyrir **Forritskenni (biðlari)**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-198">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="39bfa-199">Gefa verður upp gildið síðar þegar leyndarmál lyklageymslu er sett upp.</span><span class="sxs-lookup"><span data-stu-id="39bfa-199">You will have to provide this value later, when you set up key vault secrets.</span></span>
    4. <span data-ttu-id="39bfa-200">Farið í **API-heimildir** og fylgið eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="39bfa-200">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="39bfa-201">Veljið **Bæta við heimild**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-201">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="39bfa-202">Veljið **Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-202">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="39bfa-203">Þegar búið er að velja úthlutaðar heimildir skal velja **Notandi\_Eftirlíking**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-203">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="39bfa-204">Veldu **Bæta við heimildum**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-204">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="39bfa-205">Á valmyndinni fyrir forritið skal velja **Vottorð \& Leynilykar** og síðan skal fylgja þessum skrefum til að búa til leynilykla lyklageymslu:</span><span class="sxs-lookup"><span data-stu-id="39bfa-205">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="39bfa-206">Veljið **Nýtt leyniorð biðlara**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-206">Select **New client secret**.</span></span>
        2. <span data-ttu-id="39bfa-207">Í reitnum **Lyklalýsing** skal færa inn heiti.</span><span class="sxs-lookup"><span data-stu-id="39bfa-207">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="39bfa-208">Veljið tímalengd og svo **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-208">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="39bfa-209">Leynilykill er myndaður á svæðinu **Gildi**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-209">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="39bfa-210">Afritaðu og vistaðu leyniorð biðlara.</span><span class="sxs-lookup"><span data-stu-id="39bfa-210">Copy and save the client secret value.</span></span> <span data-ttu-id="39bfa-211">Gefa verður upp gildið síðar þegar leyndarmál lyklageymslu er sett upp.</span><span class="sxs-lookup"><span data-stu-id="39bfa-211">You will have to provide this value later, when you set up key vault secrets.</span></span>

4. <span data-ttu-id="39bfa-212">Stofna leynilykla lyklageymslu:</span><span class="sxs-lookup"><span data-stu-id="39bfa-212">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="39bfa-213">Opnið lyklageymsluna sem stofnuð var áður og veljið **Leynilyklar**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-213">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="39bfa-214">Fyrir hvert heiti leynilykils í eftirfarandi töflu skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="39bfa-214">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="39bfa-215">Veljið **Mynda/Flytja inn**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-215">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="39bfa-216">Á síðunni **Stofna leynilykil**, á svæðinu **Valkostir upphleðslu**, skal velja **Handvirkt**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-216">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="39bfa-217">Búið til leyniheitið og gildið úr töflunni.</span><span class="sxs-lookup"><span data-stu-id="39bfa-217">Create the secret name and value from the table.</span></span>
        4. <span data-ttu-id="39bfa-218">Veljið **Virkjað** og veljið síðan **Búa til**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-218">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="39bfa-219">Leynilykillinn er stofnaður og bætt við Lyklageymslu.</span><span class="sxs-lookup"><span data-stu-id="39bfa-219">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="39bfa-220">Leyniheiti</span><span class="sxs-lookup"><span data-stu-id="39bfa-220">Secret name</span></span>                       | <span data-ttu-id="39bfa-221">Leynilykill</span><span class="sxs-lookup"><span data-stu-id="39bfa-221">Secret value</span></span>                                                                                 |
        |-----------------------------------|----------------------------------------------------------------------------------------------|
        | <span data-ttu-id="39bfa-222">forrit-auðkenni</span><span class="sxs-lookup"><span data-stu-id="39bfa-222">app-id</span></span>                            | <span data-ttu-id="39bfa-223">Forritskenni forritsins sem var stofnað áður.</span><span class="sxs-lookup"><span data-stu-id="39bfa-223">The app ID of the application that you created earlier.</span></span>                                      |
        | <span data-ttu-id="39bfa-224">forrit-leyndarmál</span><span class="sxs-lookup"><span data-stu-id="39bfa-224">app-secret</span></span>                        | <span data-ttu-id="39bfa-225">Leyndarmál biðlarans sem var vistað áður.</span><span class="sxs-lookup"><span data-stu-id="39bfa-225">The client secret that you saved earlier.</span></span>                                                    |
        | <span data-ttu-id="39bfa-226">geymsla-reikningur-heiti</span><span class="sxs-lookup"><span data-stu-id="39bfa-226">storage-account-name</span></span>              | <span data-ttu-id="39bfa-227">Heiti geymslureikningsins sem var stofnaður áður, t.d. **storageaccount1**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-227">The name of the storage account that you created earlier, such as **storageaccount1**.</span></span>       |

5. <span data-ttu-id="39bfa-228">Heimila forriti aðgang að lyklageymslu:</span><span class="sxs-lookup"><span data-stu-id="39bfa-228">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="39bfa-229">Í [Azure-gátt](https://portal.azure.com) skal opna lyklageymsluna sem var stofnuð áður.</span><span class="sxs-lookup"><span data-stu-id="39bfa-229">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="39bfa-230">Velja aðgangsstefnur.</span><span class="sxs-lookup"><span data-stu-id="39bfa-230">Select the access policies.</span></span>
    3. <span data-ttu-id="39bfa-231">Fyrir hvert forrit í eftirfarandi töflu skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="39bfa-231">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="39bfa-232">Veljið **Bæta við aðgangsreglu** til að búa til aðgangsreglu.</span><span class="sxs-lookup"><span data-stu-id="39bfa-232">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="39bfa-233">Á svæðinu **Heimildir leynilykils** skal velja heimildir úr töflunni.</span><span class="sxs-lookup"><span data-stu-id="39bfa-233">In the **Secret permissions** field, select the permissions from the table.</span></span>
        3. <span data-ttu-id="39bfa-234">Á svæðinu **Velja aðalreikning** skal leita að birtingarheiti forrits sem birtist í töflunni.</span><span class="sxs-lookup"><span data-stu-id="39bfa-234">In the **Select principal** field, search for the application display name from the table.</span></span>
        4. <span data-ttu-id="39bfa-235">Veljið **Velja**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-235">Select **Select**.</span></span>
        5. <span data-ttu-id="39bfa-236">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-236">Select **Add**.</span></span>
        6. <span data-ttu-id="39bfa-237">Veldu **Vista**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-237">Select **Save**.</span></span>

        | <span data-ttu-id="39bfa-238">Forrit</span><span class="sxs-lookup"><span data-stu-id="39bfa-238">Application</span></span>                                              | <span data-ttu-id="39bfa-239">Aðgangsheimildir</span><span class="sxs-lookup"><span data-stu-id="39bfa-239">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="39bfa-240">Birtingarheiti nýja forritsins sem var búið til</span><span class="sxs-lookup"><span data-stu-id="39bfa-240">The display name of the new application that you created</span></span> | <span data-ttu-id="39bfa-241">Sækja, listi</span><span class="sxs-lookup"><span data-stu-id="39bfa-241">Get, List</span></span>   |
        | <span data-ttu-id="39bfa-242">**Microsoft Dynamics ERP Microservices**</span><span class="sxs-lookup"><span data-stu-id="39bfa-242">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="39bfa-243">Sækja, listi</span><span class="sxs-lookup"><span data-stu-id="39bfa-243">Get, List</span></span>   |

6. <span data-ttu-id="39bfa-244">Úthluta hlutverkum til að fá aðgang að geymslureikningi:</span><span class="sxs-lookup"><span data-stu-id="39bfa-244">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="39bfa-245">Í [Azure-gáttinni](https://portal.azure.com) skal opna geymslureikninginn sem var stofnaður áður.</span><span class="sxs-lookup"><span data-stu-id="39bfa-245">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="39bfa-246">Veljið **Aðgangsstýringu (IAM)** og veljið síðan **Hlutverkaúthlutanir**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-246">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="39bfa-247">Veljið **Bæta við, Bæta við hlutverkaúthlutun**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-247">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="39bfa-248">Fyrir hvert forrit í eftirfarandi töflu skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="39bfa-248">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="39bfa-249">Veljið hlutverkið úr töflunni.</span><span class="sxs-lookup"><span data-stu-id="39bfa-249">Select the role from the table.</span></span>
        2. <span data-ttu-id="39bfa-250">Hafið svæðið **Úthluta aðgangi að** stillt á **Azure AD-notanda, -hóp eða þjónustueiningu**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-250">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="39bfa-251">Í reitnum **Velja** skal slá inn forritið úr töflunni.</span><span class="sxs-lookup"><span data-stu-id="39bfa-251">In the **Select** field, enter the application from the table.</span></span>
        4. <span data-ttu-id="39bfa-252">Veldu **Vista**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-252">Select **Save**.</span></span>

        | <span data-ttu-id="39bfa-253">Forrit</span><span class="sxs-lookup"><span data-stu-id="39bfa-253">Application</span></span>                                              | <span data-ttu-id="39bfa-254">Hlutverk</span><span class="sxs-lookup"><span data-stu-id="39bfa-254">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="39bfa-255">Birtingarheiti nýja forritsins sem var búið til</span><span class="sxs-lookup"><span data-stu-id="39bfa-255">The display name of the new application that you created</span></span> | <span data-ttu-id="39bfa-256">Eigandi</span><span class="sxs-lookup"><span data-stu-id="39bfa-256">Owner</span></span>                       |
        | <span data-ttu-id="39bfa-257">Birtingarheiti nýja forritsins sem var búið til</span><span class="sxs-lookup"><span data-stu-id="39bfa-257">The display name of the new application that you created</span></span> | <span data-ttu-id="39bfa-258">Framlagsveitandi</span><span class="sxs-lookup"><span data-stu-id="39bfa-258">Contributor</span></span>                 |
        | <span data-ttu-id="39bfa-259">Birtingarheiti nýja forritsins sem var búið til</span><span class="sxs-lookup"><span data-stu-id="39bfa-259">The display name of the new application that you created</span></span> | <span data-ttu-id="39bfa-260">Geymslureikningsþátttakandi</span><span class="sxs-lookup"><span data-stu-id="39bfa-260">Storage Account Contributor</span></span> |
        | <span data-ttu-id="39bfa-261">Birtingarheiti nýja forritsins sem var búið til</span><span class="sxs-lookup"><span data-stu-id="39bfa-261">The display name of the new application that you created</span></span> | <span data-ttu-id="39bfa-262">Eigandi Blob-gagna í geymslu</span><span class="sxs-lookup"><span data-stu-id="39bfa-262">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="39bfa-263">**Heimildaþjónusta AI Builder**</span><span class="sxs-lookup"><span data-stu-id="39bfa-263">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="39bfa-264">Lesari Blob-gagna í geymslu</span><span class="sxs-lookup"><span data-stu-id="39bfa-264">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="39bfa-265">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="39bfa-265">Azure CLI</span></span>](#tab/azure-azure-cli)

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

## <a name="configure-the-export-to-data-lake-add-in"></a><span data-ttu-id="39bfa-266">Stilla innbótina Flytja út í Data Lake</span><span class="sxs-lookup"><span data-stu-id="39bfa-266">Configure the Export to Data Lake add-in</span></span>

<span data-ttu-id="39bfa-267">Fylgið eftirfarandi skrefum til að nota LCS til að bæta útflutningi við Azure Data Lake-innbótinni við umhverfið.</span><span class="sxs-lookup"><span data-stu-id="39bfa-267">Follow these steps to use LCS to add the Export to Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="39bfa-268">Skráðu þig inn á LCS og veldu síðan **Allar upplýsingar**, undir heiti umhverfisins hægra megin á síðunni.</span><span class="sxs-lookup"><span data-stu-id="39bfa-268">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="39bfa-269">Í hlutanum **Innbætur umhverfis** skal velja **Setja upp nýja innbót**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-269">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="39bfa-270">Veljið innbótina **Flytja út í Data Lake**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-270">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="39bfa-271">Sláið inn eftirfarandi gildi.</span><span class="sxs-lookup"><span data-stu-id="39bfa-271">Enter the following values.</span></span>

    | <span data-ttu-id="39bfa-272">Virði</span><span class="sxs-lookup"><span data-stu-id="39bfa-272">Value</span></span>                                                              | <span data-ttu-id="39bfa-273">lýsing</span><span class="sxs-lookup"><span data-stu-id="39bfa-273">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="39bfa-274">Leigjandakenni Azure-áskriftar þar sem lyklageymsla er staðsett</span><span class="sxs-lookup"><span data-stu-id="39bfa-274">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="39bfa-275">Auðkenni leigjanda þar sem geymslureikningur, forrit og lyklageymslur eru staðsett.</span><span class="sxs-lookup"><span data-stu-id="39bfa-275">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="39bfa-276">Til að finna þetta gildi skal opna [Azure-gátt](https://portal.azure.com), **Azure Active Directory** og afrita gildi **leigjandakennis**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-276">To obtain this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="39bfa-277">Gefðu upp DNS-heiti lyklageymslunnar</span><span class="sxs-lookup"><span data-stu-id="39bfa-277">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="39bfa-278">DNS-heiti lyklageymslu, t.d. `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="39bfa-278">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> |
    | <span data-ttu-id="39bfa-279">Gefðu upp leyndarmálið sem inniheldur heiti geymslureikningsins</span><span class="sxs-lookup"><span data-stu-id="39bfa-279">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="39bfa-280">**geymsla-reikningur-heiti**</span><span class="sxs-lookup"><span data-stu-id="39bfa-280">**storage-account-name**</span></span> |
    | <span data-ttu-id="39bfa-281">Leyniheiti fyrir forritskenni sem verður notað til að fá aðgang að Data Lake</span><span class="sxs-lookup"><span data-stu-id="39bfa-281">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="39bfa-282">**forrit-auðkenni**</span><span class="sxs-lookup"><span data-stu-id="39bfa-282">**app-id**</span></span> |
    | <span data-ttu-id="39bfa-283">Leyniheiti fyrir leyniorð biðlara í forriti</span><span class="sxs-lookup"><span data-stu-id="39bfa-283">Secret name for App client secret</span></span>                                  | <span data-ttu-id="39bfa-284">**forrit-leyndarmál**</span><span class="sxs-lookup"><span data-stu-id="39bfa-284">**app-secret**</span></span> |

5. <span data-ttu-id="39bfa-285">Samþykkið skilmálana og veljið svo **Setja upp**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-285">Agree to the terms, and then select **Install**.</span></span>

<span data-ttu-id="39bfa-286">Viðbótin verður sett upp innan fárra mínútna.</span><span class="sxs-lookup"><span data-stu-id="39bfa-286">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-the-finance-insights-add-in"></a><span data-ttu-id="39bfa-287">Stilla innbót fjármálainnsýnar</span><span class="sxs-lookup"><span data-stu-id="39bfa-287">Configure the Finance insights add-in</span></span>

> [!NOTE]
> <span data-ttu-id="39bfa-288">Ef búið er að setja upp innbótina fyrir Fá innsýn skal fjarlægja hana áður en eftirfarandi ferli er klárað.</span><span class="sxs-lookup"><span data-stu-id="39bfa-288">If you previously installed the Get insights add-in, uninstall it before you complete the following procedure.</span></span>

<span data-ttu-id="39bfa-289">Fylgið þessum skrefum til að setja upp innbót fjármálainnsýnar.</span><span class="sxs-lookup"><span data-stu-id="39bfa-289">Follow these steps to install the Finance insights add-in.</span></span>

1. <span data-ttu-id="39bfa-290">Skráðu þig inn á LCS og veldu síðan **Allar upplýsingar**, undir heiti umhverfisins hægra megin á síðunni.</span><span class="sxs-lookup"><span data-stu-id="39bfa-290">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="39bfa-291">Í hlutanum **Innbætur umhverfis** skal velja **Setja upp nýja innbót**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-291">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="39bfa-292">Veljið innbótina **Fjármálainnsýn**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-292">Select the **Finance insights** add-in.</span></span>
4. <span data-ttu-id="39bfa-293">Samþykkið skilmálana og veljið svo **Setja upp**.</span><span class="sxs-lookup"><span data-stu-id="39bfa-293">Agree to the terms, and then select **Install**.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="39bfa-294">Ábendingar og stuðningur</span><span class="sxs-lookup"><span data-stu-id="39bfa-294">Feedback and support</span></span>

<span data-ttu-id="39bfa-295">Ef þú vilt koma ábendingu á framfæri eða þarft aðstoð skaltu senda tölvupóst á [Fjármálainnsýn (forútgáfu)](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="39bfa-295">If you're interested in providing feedback, or if you require support, send an email to [Finance insights (Preview)](mailto:fiap@microsoft.com).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
