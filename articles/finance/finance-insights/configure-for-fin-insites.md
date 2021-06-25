---
title: Stilling fyrir fjármálainnsýn - útgáfur fram að 10.0.19
description: Þetta efnisatriði útskýrir grunnstillingarskref sem mun gera kerfinu kleift að nota þá eiginleika sem eru í boði í Fjármálainnsýn fyrir útgáfur fram að 10.0.19.
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
ms.openlocfilehash: 6ad06bb6d041fc060b3a99538f6d4d0af333180f
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186421"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="13679-103">Stillingar fyrir Fjármálainnsýn (forútgáfa)</span><span class="sxs-lookup"><span data-stu-id="13679-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="13679-104">Eftirfarandi ferli við uppsetningu fjármálainnsýnar gilda fyrir Microsoft Dynamics 365 Finance útgáfur fram að 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="13679-104">The following procedures for setting up Finance insights are valid for Microsoft Dynamics 365 Finance versions up to 10.0.19.</span></span> <span data-ttu-id="13679-105">Til að setja upp fjármálainnsýn á útgáfu 10.0.20 og nýrri skal sjá [Stilling fjármálainnsýnar (forútgáfa) - útgáfur 10.0.20 og nýrri](configure-for-fin-insites-PubPrvw.md).</span><span class="sxs-lookup"><span data-stu-id="13679-105">To set up Finance insights on version 10.0.20 and later, see [Configuration for Finance Insights (preview) - versions 10.0.20 and beyond](configure-for-fin-insites-PubPrvw.md).</span></span>

<span data-ttu-id="13679-106">Fjármálainnsýn sameinar virkni Microsoft Dynamics 365 Finance við Microsoft Dataverse, Azure og AI Builder til að bjóða upp á öflug spáverkfæri fyrir fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="13679-106">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Microsoft Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="13679-107">Þetta efnisatriði útskýrir grunnstillingarskref sem mun gera kerfinu kleift að nota þá eiginleika sem eru í boði í Fjármálainnsýn.</span><span class="sxs-lookup"><span data-stu-id="13679-107">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="13679-108">Virkja Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="13679-108">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="13679-109">Virkjaðu umhverfið með því að fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="13679-109">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="13679-110">Í Microsoft Dynamics Lifecycle Services (LCS) skal búa til eða uppfæra Dynamics 365 Finance umhverfi.</span><span class="sxs-lookup"><span data-stu-id="13679-110">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="13679-111">Umhverfið krefst forritsútgáfu 10.0.11/Verkvangsuppfærslu 35 eða nýrra.</span><span class="sxs-lookup"><span data-stu-id="13679-111">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="13679-112">Umhverfið verður að vera vel tiltækt í Sandbox.</span><span class="sxs-lookup"><span data-stu-id="13679-112">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="13679-113">(Þessi tegund umhverfis er einnig þekkt sem umhverfi í tveggja laga umhverfi.) Frekari upplýsingar er að finna í [Umhverfisskipulagning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="13679-113">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="13679-114">Ef þú ert að stilla fjármálainnsýn í sandkassaumhverfi gætirðu þurft að afrita framleiðslugögn í það umhverfi til að spár virki.</span><span class="sxs-lookup"><span data-stu-id="13679-114">If you are configuring Finance insights in a Sandbox environment, you might need to copy production data to that environment for predictions to work.</span></span> <span data-ttu-id="13679-115">Spálíkanið notar gögn til margra ára til að búa til spár.</span><span class="sxs-lookup"><span data-stu-id="13679-115">The prediction model uses multiple years of data to build predictions.</span></span> <span data-ttu-id="13679-116">Contoso sýnigögnin innihalda ekki næg söguleg gögn til að hægt sé að þjálfa spálíkanið á fullnægjandi hátt.</span><span class="sxs-lookup"><span data-stu-id="13679-116">The Contoso demo data doesn’t contain enough historical data to train the prediction model adequately.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="13679-117">Skilgreina Dataverse</span><span class="sxs-lookup"><span data-stu-id="13679-117">Configure Dataverse</span></span>

<span data-ttu-id="13679-118">Fylgið eftirfarandi skrefum til að stilla Dataverse fyrir Finance insights.</span><span class="sxs-lookup"><span data-stu-id="13679-118">Use the following steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="13679-119">Opnið síðu umhverfis í LCS og staðfestið að hlutinn **Power Platform samþætting** sé þegar uppsettur.</span><span class="sxs-lookup"><span data-stu-id="13679-119">Open the environment page in LCS and verify that the **Power Platform Integration** section is already setup.</span></span>
    1. <span data-ttu-id="13679-120">Ef hann er þegar uppsettur ætti heiti Dataverse umhverfisins sem tengt er við Dynamics 365 Finance umhverfið að vera sýnt.</span><span class="sxs-lookup"><span data-stu-id="13679-120">If it is already set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="13679-121">Afritið heiti Dataverse-umhverfisins.</span><span class="sxs-lookup"><span data-stu-id="13679-121">Copy the Dataverse environment name.</span></span>
    2. <span data-ttu-id="13679-122">Ef það er ekki sett upp skal fylgja eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="13679-122">If it is not set up, follow these steps:</span></span>
        1. <span data-ttu-id="13679-123">Veljið hnappinn **Uppsetning** í hlutanum Power Platform Samþætting.</span><span class="sxs-lookup"><span data-stu-id="13679-123">Select the **Setup** button in the Power Platform Integration section.</span></span> <span data-ttu-id="13679-124">Það getur tekið allt að klukkustund að setja upp umhverfið.</span><span class="sxs-lookup"><span data-stu-id="13679-124">It may take up to an hour for the environment to be set up.</span></span>
        2. <span data-ttu-id="13679-125">Ef tókst að setja upp Dataverse-umhverfið ætti heiti Dataverse-umhverfisins sem tengt er við Dynamics 365 Finance-umhverfið að vera sýnt.</span><span class="sxs-lookup"><span data-stu-id="13679-125">If the Dataverse environment is successfully set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="13679-126">Afritið heiti Dataverse-umhverfisins.</span><span class="sxs-lookup"><span data-stu-id="13679-126">Copy the Dataverse environment name.</span></span>
> [!NOTE]
> <span data-ttu-id="13679-127">Að lokinni uppsetningu umhverfisins **SKAL EKKI** velja hnappinn **Tengill á almenna gagnaþjónustu (CDS) fyrir forrit**.</span><span class="sxs-lookup"><span data-stu-id="13679-127">After completing the environment set up, **DO NOT** select the **Link to CDS for Apps** button.</span></span> <span data-ttu-id="13679-128">Þetta er ekki nauðsynlegt fyrir Finance insights og mun gera möguleikann á að ljúka við nauðsynlegar umhverfisviðbætur í LCS óvirkan.</span><span class="sxs-lookup"><span data-stu-id="13679-128">This is not needed for Finance Insights and will disable the ability to complete the required Environment Add-ins in LCS.</span></span>

2. <span data-ttu-id="13679-129">Opnaðu [Power Platform stjórnendamiðstöð ](https://admin.powerplatform.microsoft.com/) og fylgdu þessum skrefum til að búa til nýtt Dataverse -umhverfi í sama Active Directory leigjanda:</span><span class="sxs-lookup"><span data-stu-id="13679-129">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Dataverse environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="13679-130">Opnið síðuna **Umhverfi**.</span><span class="sxs-lookup"><span data-stu-id="13679-130">Open the **Environments** page.</span></span>

        <span data-ttu-id="13679-131">[![Umhverfissíða](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="13679-131">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="13679-132">Veljið Dataverse-umhverfið sem búið er til hér að ofan og veljið svo **Stillingar**.</span><span class="sxs-lookup"><span data-stu-id="13679-132">Select the Dataverse environment created above and then select **Settings**.</span></span>
    3. <span data-ttu-id="13679-133">Veljið **Tilföng \> Allar eldri stillingar**.</span><span class="sxs-lookup"><span data-stu-id="13679-133">Select **Resources \> All Legacy Settings**.</span></span>
    4. <span data-ttu-id="13679-134">Á efstu yfirlitsstikunni skal velja **Stillingar** og síðan **Sérstillingar**.</span><span class="sxs-lookup"><span data-stu-id="13679-134">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    5. <span data-ttu-id="13679-135">Veljið **Tilföng fyrir þróunaraðila**.</span><span class="sxs-lookup"><span data-stu-id="13679-135">Select **Developer Resources**.</span></span>
    6. <span data-ttu-id="13679-136">Afritið gildið **Dataverse kenni fyrirtækis**.</span><span class="sxs-lookup"><span data-stu-id="13679-136">Copy the **Dataverse organization ID** value.</span></span>
    7. <span data-ttu-id="13679-137">Í veffangastikunni vafrans skal gera athugasemd við VEFSLÓÐINA fyrir Dataverse-fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="13679-137">In the browser's address bar, make a note of the URL for the Dataverse organization.</span></span> <span data-ttu-id="13679-138">Til dæmis gæti vefslóðin verið `https://org42b2b3d3.crm.dynamics.com`.</span><span class="sxs-lookup"><span data-stu-id="13679-138">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

3. <span data-ttu-id="13679-139">Ef ætlunin er að nota sjóðstreymisspár eða fjárhagsáætlunarspár skal fylgja þessum skrefum til að uppfæra skýringartextamörk fyrirtækisins í að minnsta kosti 50 megabæt (MB):</span><span class="sxs-lookup"><span data-stu-id="13679-139">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="13679-140">Opnið [Power Apps-gáttina](https://make.powerapps.com)</span><span class="sxs-lookup"><span data-stu-id="13679-140">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="13679-141">Veljið það umhverfi sem var stofnað og veljið síðan **Ítarlegar stillingar**.</span><span class="sxs-lookup"><span data-stu-id="13679-141">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="13679-142">Veljið **Stillingar\> Skilgreining tölvupósts**.</span><span class="sxs-lookup"><span data-stu-id="13679-142">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="13679-143">Breytið gildi **Hámarksstærð skráar** reitnum í **51.200**.</span><span class="sxs-lookup"><span data-stu-id="13679-143">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="13679-144">(Gildið er gefið upp í kílóbætum \[KB\].)</span><span class="sxs-lookup"><span data-stu-id="13679-144">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="13679-145">Veljið **Í lagi** til að vista breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="13679-145">Select **OK** to save your changes.</span></span>

## <a name="configure-the-azure-setup"></a><span data-ttu-id="13679-146">Skilgreina Azure uppsetningu</span><span class="sxs-lookup"><span data-stu-id="13679-146">Configure the Azure setup</span></span>

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="13679-147">Sláið inn Dataverse skráarkenni og hlutarkenni Azure AD notandans</span><span class="sxs-lookup"><span data-stu-id="13679-147">Enter the Dataverse directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="13679-148">Sláið inn Dataverse skráasafnskenni:</span><span class="sxs-lookup"><span data-stu-id="13679-148">Enter the Dataverse directory ID:</span></span>

    1. <span data-ttu-id="13679-149">Opnið [Azure-gáttina](https://portal.azure.com)</span><span class="sxs-lookup"><span data-stu-id="13679-149">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="13679-150">Skráðu þig inn með því að nota NOTANDAKENNIÐ sem var notað til að búa til Dataverse-umhverfið.</span><span class="sxs-lookup"><span data-stu-id="13679-150">Sign in by using the user ID that was used to create the Dataverse environment.</span></span>
    3. <span data-ttu-id="13679-151">Opnið **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="13679-151">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="13679-152">Afritið gildið **Leigjandakenni**.</span><span class="sxs-lookup"><span data-stu-id="13679-152">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="13679-153">Færa inn auðkenni hlutar notanda Azure Active Directory (Azure AD):</span><span class="sxs-lookup"><span data-stu-id="13679-153">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="13679-154">Í [Azure-gátt](https://portal.azure.com) skal opna **Notendur** og leita að notandanum eftir netfangi.</span><span class="sxs-lookup"><span data-stu-id="13679-154">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="13679-155">Færið inn nafn notanda.</span><span class="sxs-lookup"><span data-stu-id="13679-155">Select the user's name.</span></span>
    3. <span data-ttu-id="13679-156">Afritið **Hlutarkenni** gildið.</span><span class="sxs-lookup"><span data-stu-id="13679-156">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="13679-157">Nota Azure Cloud Shell til að setja upp Data Lake-tilföng fjármálainnsýnar</span><span class="sxs-lookup"><span data-stu-id="13679-157">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="13679-158">Nota Windows PowerShell-forskrift</span><span class="sxs-lookup"><span data-stu-id="13679-158">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="13679-159">Boðið er upp á Windows PowerShell-forskrift þannig að auðvelt er að setja upp Azure-tilföng sem eru skilgreind í [Grunnstilla útflutning í Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="13679-159">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="13679-160">Ef óskað er eftir því að setja upp handvirkt skal sleppa þessu ferli og halda áfram með ferlið í hlutanum [Handvirk uppsetning](#manual-setup).</span><span class="sxs-lookup"><span data-stu-id="13679-160">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="13679-161">Fylgið skrefunum hér að neðan til að keyra PowerShell-forskrift.</span><span class="sxs-lookup"><span data-stu-id="13679-161">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="13679-162">Hugsanlega virkar ekki valkosturinn „Prófaðu þetta“ í Azure CLI eða ekki er hægt að keyra þessa forskrift á tölvunni.</span><span class="sxs-lookup"><span data-stu-id="13679-162">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="13679-163">Fylgið eftirfarandi skrefum til að grunnstilla Azure með Windows PowerShell-forskriftinni.</span><span class="sxs-lookup"><span data-stu-id="13679-163">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="13679-164">Réttindi til að búa til Azure-tilfangaflokk, Azure-tilföng og Azure AD-forrit þurfa að vera til staðar.</span><span class="sxs-lookup"><span data-stu-id="13679-164">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="13679-165">Frekari upplýsingar um nauðsynlegar heimildir má finna á [Athuga Azure AD heimildir](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="13679-165">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="13679-166">Í [Azure-gátt](https://portal.azure.com) skal opna viðkomandi Azure-áskrift.</span><span class="sxs-lookup"><span data-stu-id="13679-166">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="13679-167">Veljið **Cloud Shell**-hnappinn hægra megin við svæðið **Leita**.</span><span class="sxs-lookup"><span data-stu-id="13679-167">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="13679-168">Veljið **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="13679-168">Select **PowerShell**.</span></span>
3. <span data-ttu-id="13679-169">Búðu til geymslu, ef beðið er um að gera það.</span><span class="sxs-lookup"><span data-stu-id="13679-169">Create storage if you're prompted to do so.</span></span>
4. <span data-ttu-id="13679-170">Farið á flipann **Azure CLI** og veljið **Afrita**.</span><span class="sxs-lookup"><span data-stu-id="13679-170">Go to the **Azure CLI** tab and select **Copy**.</span></span>  
5. <span data-ttu-id="13679-171">Opnið Notepad og límið inn forskrift PowerShell.</span><span class="sxs-lookup"><span data-stu-id="13679-171">Open Notepad and paste the PowerShell script.</span></span> <span data-ttu-id="13679-172">Vistið skrána sem ConfigureDataLake.ps1.</span><span class="sxs-lookup"><span data-stu-id="13679-172">Save the file as ConfigureDataLake.ps1.</span></span>
6. <span data-ttu-id="13679-173">Hlaðið upp forskrift Windows PowerShell í lotuna með því að nota valkost valmyndar fyrir upphleðslu í Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="13679-173">Upload the Windows PowerShell script to the session using the menu option for upload in Cloud Shell.</span></span>
7. <span data-ttu-id="13679-174">Keyra skriftuna .\ConfigureDataLake.ps1.</span><span class="sxs-lookup"><span data-stu-id="13679-174">Run the script .\ConfigureDataLake.ps1.</span></span>
8. <span data-ttu-id="13679-175">Fylgið kvaðningunum til að keyra forskriftina.</span><span class="sxs-lookup"><span data-stu-id="13679-175">Follow the prompts to run the script.</span></span>
9. <span data-ttu-id="13679-176">Notið upplýsingar úr forskriftinni til að setja upp innbótina **Flytja út í Data Lake** í LCS.</span><span class="sxs-lookup"><span data-stu-id="13679-176">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
10. <span data-ttu-id="13679-177">Notið upplýsingar úr forskriftinni til að virkja einingaverslunina á síðunni **Gagnatengingar** í Finance (**Kerfisstjórnun \> Kerfisfæribreytur \> Gagnatengingar**).</span><span class="sxs-lookup"><span data-stu-id="13679-177">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="13679-178">Handvirk uppsetning</span><span class="sxs-lookup"><span data-stu-id="13679-178">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="13679-179">Bæta umsóknum við Azure AD leigjanda</span><span class="sxs-lookup"><span data-stu-id="13679-179">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="13679-180">Í [Azure-gáttinni](https://portal.azure.com) skal fara á **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="13679-180">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="13679-181">Veljið **Stjórna \> Enterprise-forrit**.</span><span class="sxs-lookup"><span data-stu-id="13679-181">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="13679-182">Leitið að eftirfarandi forritum eftir FORRITSKENNINU.</span><span class="sxs-lookup"><span data-stu-id="13679-182">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="13679-183">Forrit</span><span class="sxs-lookup"><span data-stu-id="13679-183">Application</span></span>                              | <span data-ttu-id="13679-184">Auðkenni forrits</span><span class="sxs-lookup"><span data-stu-id="13679-184">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="13679-185">Microsoft Dynamics ERP Microservices</span><span class="sxs-lookup"><span data-stu-id="13679-185">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="13679-186">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="13679-186">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="13679-187">Microsoft Dynamics ERP Microservices CDS</span><span class="sxs-lookup"><span data-stu-id="13679-187">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="13679-188">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="13679-188">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="13679-189">Heimildaþjónusta AI Builder</span><span class="sxs-lookup"><span data-stu-id="13679-189">AI Builder Authorization Service</span></span>         | <span data-ttu-id="13679-190">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="13679-190">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="13679-191">Ef ekki eitthvað af undanfarandi forritum finnst ekki skal prófa eftirfarandi skref.</span><span class="sxs-lookup"><span data-stu-id="13679-191">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="13679-192">Á staðbundnu vélinni skal velja **Upphafsvalmyndina** og leita að **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="13679-192">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="13679-193">Velja skal og halda fingri á (eða hægrismella) **Windows PowerShell** og velja svo **Keyra sem stjórnandi**.</span><span class="sxs-lookup"><span data-stu-id="13679-193">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="13679-194">Keyrið eftirfarandi skipun til að setja upp **AzureAD** einingun.</span><span class="sxs-lookup"><span data-stu-id="13679-194">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="13679-195">Ef NuGet-veita er nauðsynleg til að halda áfram skal velja **Y** til að setja hana upp.</span><span class="sxs-lookup"><span data-stu-id="13679-195">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="13679-196">Ef skeytið „Ótraust geymslׅa“ birtist skal velja **Y** til að halda áfram.</span><span class="sxs-lookup"><span data-stu-id="13679-196">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="13679-197">Fyrir hvert forrit sem verður að bæta við þarf að keyra eftirfarandi skipanir til að bæta forritinu við Azure AD.</span><span class="sxs-lookup"><span data-stu-id="13679-197">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="13679-198">Skráðu þig inn sem stjórnandi Azure AD þegar beðið er um það.</span><span class="sxs-lookup"><span data-stu-id="13679-198">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="13679-199">Stofna Azure-tilföng</span><span class="sxs-lookup"><span data-stu-id="13679-199">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="13679-200">Ganga skal úr skugga um að eftirfarandi tilföng séu stofnuð í sama Azure AD-tilviki og Dataverse-umhverfið.</span><span class="sxs-lookup"><span data-stu-id="13679-200">Make sure that you create the following resources in the same Azure AD instance as the Dataverse environment.</span></span> <span data-ttu-id="13679-201">Ekki er hægt að nota tilföng úr öðru Azure AD-tilviki.</span><span class="sxs-lookup"><span data-stu-id="13679-201">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="13679-202">Búa til nýjan geymslureikning:</span><span class="sxs-lookup"><span data-stu-id="13679-202">Create a new storage account:</span></span>

    1. <span data-ttu-id="13679-203">Í [Azure Portal](https://portal.azure.com) skal stofna geymslureikning.</span><span class="sxs-lookup"><span data-stu-id="13679-203">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="13679-204">Í svarglugganum **Stofna geymslureikning** skal stilla eftirfarandi svæði:</span><span class="sxs-lookup"><span data-stu-id="13679-204">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="13679-205">**Staðsetning** – velja gagnamiðstöð með umhverfinu.</span><span class="sxs-lookup"><span data-stu-id="13679-205">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="13679-206">**Afköst** – mælt er með **Hefðbundin**.</span><span class="sxs-lookup"><span data-stu-id="13679-206">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="13679-207">**Reikningsgerð** – velja þarf **StorageV2**.</span><span class="sxs-lookup"><span data-stu-id="13679-207">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="13679-208">Í svarglugganum **Ítarlegir valkostir**, fyrir **Data Lake Storage Gen2**, skal velja **Virkja** undir **Stigveldis nafnabil**.</span><span class="sxs-lookup"><span data-stu-id="13679-208">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="13679-209">Ef þessi eiginleiki er gerður óvirkur er ekki hægt að nota gögn sem Finance and Operations-forrit skrifa með þjónustu á borð við Power BI-gagnaflæði.</span><span class="sxs-lookup"><span data-stu-id="13679-209">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="13679-210">Veljið **yfirfara og búa til**.</span><span class="sxs-lookup"><span data-stu-id="13679-210">Select **Review and create**.</span></span> <span data-ttu-id="13679-211">Þegar uppsetningu er lokið verður nýja tilfangið til staðar á Azure-gáttinni.</span><span class="sxs-lookup"><span data-stu-id="13679-211">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="13679-212">Opnaðu geymslureikninginn sem þú stofnaðir.</span><span class="sxs-lookup"><span data-stu-id="13679-212">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="13679-213">Á valmyndinni til vinstri skal velja **Aðgangslyklar**.</span><span class="sxs-lookup"><span data-stu-id="13679-213">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="13679-214">Afritið og vistið tengingarstreng fyrir annaðhvort **Key1** eða **Key2**.</span><span class="sxs-lookup"><span data-stu-id="13679-214">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="13679-215">Afrita og vista heiti geymslureiknings.</span><span class="sxs-lookup"><span data-stu-id="13679-215">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="13679-216">Búa til nýja lyklageymslu:</span><span class="sxs-lookup"><span data-stu-id="13679-216">Create a new key vault:</span></span>

    1. <span data-ttu-id="13679-217">Í [Azure Portal](https://portal.azure.com) skal stofna lyklageymslu.</span><span class="sxs-lookup"><span data-stu-id="13679-217">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="13679-218">Í svarglugganum **Stofna lyklageymslu** á svæðinu **Staðsetning** skal velja gagnamiðstöðina þar sem umhverfið er að finna.</span><span class="sxs-lookup"><span data-stu-id="13679-218">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="13679-219">Eftir að lyklageymsla er stofnuð skal velja hana á listanum og síðan velja **Leynilyklar**.</span><span class="sxs-lookup"><span data-stu-id="13679-219">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="13679-220">Veljið **Mynda/Flytja inn**.</span><span class="sxs-lookup"><span data-stu-id="13679-220">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="13679-221">Á síðunni **Stofna leynilykil**, á svæðinu **Valkostir upphleðslu**, skal velja **Handvirkt**.</span><span class="sxs-lookup"><span data-stu-id="13679-221">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="13679-222">Færa skal inn heiti fyrir leynilykilinn.</span><span class="sxs-lookup"><span data-stu-id="13679-222">Enter a name for the secret.</span></span> <span data-ttu-id="13679-223">Gerið athugasemd við heitið vegna þess að það verður að nota það síðar.</span><span class="sxs-lookup"><span data-stu-id="13679-223">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="13679-224">Á svæðinu **Gildi** skal færa inn tengingarstreng sem fenginn var úr geymslureikningi í fyrra ferli.</span><span class="sxs-lookup"><span data-stu-id="13679-224">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="13679-225">Veljið **Virkjað** og veljið síðan **Búa til**.</span><span class="sxs-lookup"><span data-stu-id="13679-225">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="13679-226">Leynilykillinn er stofnaður og bætt við Lyklageymslu.</span><span class="sxs-lookup"><span data-stu-id="13679-226">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="13679-227">Opnið **Lyklageymsluyfirlit** og skráið niður DNS-heitið.</span><span class="sxs-lookup"><span data-stu-id="13679-227">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="13679-228">Stofna og skrá Azure AD forrit:</span><span class="sxs-lookup"><span data-stu-id="13679-228">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="13679-229">Í [Azure-gáttinni](https://portal.azure.com) skal opna **Azure Active Directory** og velja svo **Forritaskráningar**.</span><span class="sxs-lookup"><span data-stu-id="13679-229">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="13679-230">Velja skal **Ný forritaskráning** og stilla eftirfarandi svæði:</span><span class="sxs-lookup"><span data-stu-id="13679-230">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="13679-231">**Heiti** - Færið inn heiti forritsins.</span><span class="sxs-lookup"><span data-stu-id="13679-231">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="13679-232">**Forritsgerð** – Veljið **Vef-API**.</span><span class="sxs-lookup"><span data-stu-id="13679-232">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="13679-233">**Framsenda URI-uppsetningu** – Sláið inn vefslóð fyrir Dynamics 365-tilvikið, til dæmis, `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="13679-233">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="13679-234">Opnið forritið sem var búið til og afritið og vistið gildi fyrir **Forritskenni (biðlari)**.</span><span class="sxs-lookup"><span data-stu-id="13679-234">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="13679-235">Gefa verður upp gildið síðar þegar lyklageymslan er sett upp.</span><span class="sxs-lookup"><span data-stu-id="13679-235">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="13679-236">Farið í **API-heimildir** og fylgið eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="13679-236">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="13679-237">Veljið **Bæta við heimild**.</span><span class="sxs-lookup"><span data-stu-id="13679-237">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="13679-238">Veljið **Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="13679-238">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="13679-239">Þegar búið er að velja úthlutaðar heimildir skal velja **Notandi\_Eftirlíking**.</span><span class="sxs-lookup"><span data-stu-id="13679-239">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="13679-240">Veldu **Bæta við heimildum**.</span><span class="sxs-lookup"><span data-stu-id="13679-240">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="13679-241">Á valmyndinni fyrir forritið skal velja **Vottorð \& Leynilykar** og síðan skal fylgja þessum skrefum til að búa til leynilykla lyklageymslu:</span><span class="sxs-lookup"><span data-stu-id="13679-241">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="13679-242">Veljið **Nýtt leyniorð biðlara**.</span><span class="sxs-lookup"><span data-stu-id="13679-242">Select **New client secret**.</span></span>
        2. <span data-ttu-id="13679-243">Í reitnum **Lyklalýsing** skal færa inn heiti.</span><span class="sxs-lookup"><span data-stu-id="13679-243">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="13679-244">Veljið tímalengd og svo **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="13679-244">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="13679-245">Leynilykill er myndaður á svæðinu **Gildi**.</span><span class="sxs-lookup"><span data-stu-id="13679-245">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="13679-246">Afritaðu og vistaðu leynigildið.</span><span class="sxs-lookup"><span data-stu-id="13679-246">Copy and save the secret value.</span></span>

4. <span data-ttu-id="13679-247">Stofna leynilykla lyklageymslu:</span><span class="sxs-lookup"><span data-stu-id="13679-247">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="13679-248">Opnið lyklageymsluna sem stofnuð var áður og veljið **Leynilyklar**.</span><span class="sxs-lookup"><span data-stu-id="13679-248">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="13679-249">Fyrir hvert heiti leynilykils í eftirfarandi töflu skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="13679-249">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="13679-250">Veljið **Mynda/Flytja inn**.</span><span class="sxs-lookup"><span data-stu-id="13679-250">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="13679-251">Á síðunni **Stofna leynilykil**, á svæðinu **Valkostir upphleðslu**, skal velja **Handvirkt**.</span><span class="sxs-lookup"><span data-stu-id="13679-251">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="13679-252">Búa skal til heiti leynilykils og gildi úr eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="13679-252">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="13679-253">Veljið **Virkjað** og veljið síðan **Búa til**.</span><span class="sxs-lookup"><span data-stu-id="13679-253">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="13679-254">Leynilykillinn er stofnaður og bætt við Lyklageymslu.</span><span class="sxs-lookup"><span data-stu-id="13679-254">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="13679-255">Leyniheiti</span><span class="sxs-lookup"><span data-stu-id="13679-255">Secret name</span></span>                       | <span data-ttu-id="13679-256">Leynilykill</span><span class="sxs-lookup"><span data-stu-id="13679-256">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="13679-257">forrit-auðkenni</span><span class="sxs-lookup"><span data-stu-id="13679-257">app-id</span></span>                            | <span data-ttu-id="13679-258">Forritskenni forritsins sem var stofnað áður</span><span class="sxs-lookup"><span data-stu-id="13679-258">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="13679-259">forrit-leyndarmál</span><span class="sxs-lookup"><span data-stu-id="13679-259">app-secret</span></span>                        | <span data-ttu-id="13679-260">Leyndarmál biðlarans sem var vistað áður</span><span class="sxs-lookup"><span data-stu-id="13679-260">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="13679-261">geymsla-reikningur-heiti</span><span class="sxs-lookup"><span data-stu-id="13679-261">storage-account-name</span></span>              | <span data-ttu-id="13679-262">Heiti geymslureikningsins sem var stofnaður áður, t.d. **storageaccount1**</span><span class="sxs-lookup"><span data-stu-id="13679-262">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="13679-263">geymsla-reikningur-tenging-strengur</span><span class="sxs-lookup"><span data-stu-id="13679-263">storage-account-connection-string</span></span> | <span data-ttu-id="13679-264">Tengingarstrengurinn sem var afritaður af síðunni **Aðgangslyklar** fyrir geymslureikninginn</span><span class="sxs-lookup"><span data-stu-id="13679-264">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="13679-265">Heimila forriti aðgang að lyklageymslu:</span><span class="sxs-lookup"><span data-stu-id="13679-265">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="13679-266">Í [Azure-gátt](https://portal.azure.com) skal opna lyklageymsluna sem var stofnuð áður.</span><span class="sxs-lookup"><span data-stu-id="13679-266">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="13679-267">Velja aðgangsstefnur.</span><span class="sxs-lookup"><span data-stu-id="13679-267">Select the access policies.</span></span>
    3. <span data-ttu-id="13679-268">Fyrir hvert forrit í eftirfarandi töflu skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="13679-268">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="13679-269">Veljið **Bæta við aðgangsreglu** til að búa til aðgangsreglu.</span><span class="sxs-lookup"><span data-stu-id="13679-269">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="13679-270">Á svæðinu **Heimildir leynilykils** skal velja heimildir úr eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="13679-270">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="13679-271">Á svæðinu **Velja aðalreikning** skal leita að birtingarheiti forrits sem birtist í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="13679-271">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="13679-272">Veljið **Velja**.</span><span class="sxs-lookup"><span data-stu-id="13679-272">Select **Select**.</span></span>
        5. <span data-ttu-id="13679-273">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="13679-273">Select **Add**.</span></span>
        6. <span data-ttu-id="13679-274">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="13679-274">Select **Save**.</span></span>

        | <span data-ttu-id="13679-275">Forrit</span><span class="sxs-lookup"><span data-stu-id="13679-275">Application</span></span>                                              | <span data-ttu-id="13679-276">Aðgangsheimildir</span><span class="sxs-lookup"><span data-stu-id="13679-276">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="13679-277">Birtingarheiti nýja forritsins sem var búið til</span><span class="sxs-lookup"><span data-stu-id="13679-277">The display name of the new application that you created</span></span> | <span data-ttu-id="13679-278">Sækja, listi</span><span class="sxs-lookup"><span data-stu-id="13679-278">Get, List</span></span>   |
        | <span data-ttu-id="13679-279">**Microsoft Dynamics ERP Microservices**</span><span class="sxs-lookup"><span data-stu-id="13679-279">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="13679-280">Sækja, listi</span><span class="sxs-lookup"><span data-stu-id="13679-280">Get, List</span></span>   |

6. <span data-ttu-id="13679-281">Úthluta hlutverkum til að fá aðgang að geymslureikningi:</span><span class="sxs-lookup"><span data-stu-id="13679-281">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="13679-282">Í [Azure-gáttinni](https://portal.azure.com) skal opna geymslureikninginn sem var stofnaður áður.</span><span class="sxs-lookup"><span data-stu-id="13679-282">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="13679-283">Veljið **Aðgangsstýringu (IAM)** og veljið síðan **Hlutverkaúthlutanir**.</span><span class="sxs-lookup"><span data-stu-id="13679-283">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="13679-284">Veljið **Bæta við, Bæta við hlutverkaúthlutun**.</span><span class="sxs-lookup"><span data-stu-id="13679-284">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="13679-285">Fyrir hvert forrit í eftirfarandi töflu skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="13679-285">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="13679-286">Velja skal hlutverkið úr eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="13679-286">Select the role from the following table.</span></span>
        2. <span data-ttu-id="13679-287">Hafið svæðið **Úthluta aðgangi að** stillt á **Azure AD-notanda, -hóp eða þjónustueiningu**.</span><span class="sxs-lookup"><span data-stu-id="13679-287">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="13679-288">Á svæðinu **Velja** skal slá inn forrit úr eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="13679-288">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="13679-289">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="13679-289">Select **Save**.</span></span>

        | <span data-ttu-id="13679-290">Forrit</span><span class="sxs-lookup"><span data-stu-id="13679-290">Application</span></span>                                              | <span data-ttu-id="13679-291">Hlutverk</span><span class="sxs-lookup"><span data-stu-id="13679-291">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="13679-292">Birtingarheiti nýja forritsins sem var búið til</span><span class="sxs-lookup"><span data-stu-id="13679-292">The display name of the new application that you created</span></span> | <span data-ttu-id="13679-293">Eigandi</span><span class="sxs-lookup"><span data-stu-id="13679-293">Owner</span></span>                       |
        | <span data-ttu-id="13679-294">Birtingarheiti nýja forritsins sem var búið til</span><span class="sxs-lookup"><span data-stu-id="13679-294">The display name of the new application that you created</span></span> | <span data-ttu-id="13679-295">Framlagsveitandi</span><span class="sxs-lookup"><span data-stu-id="13679-295">Contributor</span></span>                 |
        | <span data-ttu-id="13679-296">Birtingarheiti nýja forritsins sem var búið til</span><span class="sxs-lookup"><span data-stu-id="13679-296">The display name of the new application that you created</span></span> | <span data-ttu-id="13679-297">Geymslureikningsþátttakandi</span><span class="sxs-lookup"><span data-stu-id="13679-297">Storage Account Contributor</span></span> |
        | <span data-ttu-id="13679-298">Birtingarheiti nýja forritsins sem var búið til</span><span class="sxs-lookup"><span data-stu-id="13679-298">The display name of the new application that you created</span></span> | <span data-ttu-id="13679-299">Eigandi Blob-gagna í geymslu</span><span class="sxs-lookup"><span data-stu-id="13679-299">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="13679-300">**Heimildaþjónusta AI Builder**</span><span class="sxs-lookup"><span data-stu-id="13679-300">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="13679-301">Lesari Blob-gagna í geymslu</span><span class="sxs-lookup"><span data-stu-id="13679-301">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="13679-302">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="13679-302">Azure CLI</span></span>](#tab/azure-azure-cli)

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



## <a name="configure-the-data-lake"></a><span data-ttu-id="13679-303">Skilgreina Data Lake</span><span class="sxs-lookup"><span data-stu-id="13679-303">Configure the data lake</span></span>

<span data-ttu-id="13679-304">Fylgið eftirfarandi skrefum til að nota LCS til að bæta Azure Data Lake-innbótinni við umhverfið.</span><span class="sxs-lookup"><span data-stu-id="13679-304">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="13679-305">Skráðu þig inn á LCS og veldu síðan **Allar upplýsingar**, undir heiti umhverfisins hægra megin á síðunni.</span><span class="sxs-lookup"><span data-stu-id="13679-305">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="13679-306">Í hlutanum **Innbætur umhverfis** skal velja **Setja upp nýja innbót**.</span><span class="sxs-lookup"><span data-stu-id="13679-306">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="13679-307">Veljið innbótina **Flytja út í Data Lake**.</span><span class="sxs-lookup"><span data-stu-id="13679-307">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="13679-308">Sláið inn eftirfarandi gildi.</span><span class="sxs-lookup"><span data-stu-id="13679-308">Enter the following values.</span></span>

    | <span data-ttu-id="13679-309">Virði</span><span class="sxs-lookup"><span data-stu-id="13679-309">Value</span></span>                                                              | <span data-ttu-id="13679-310">lýsing</span><span class="sxs-lookup"><span data-stu-id="13679-310">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="13679-311">Leigjandakenni Azure-áskriftar þar sem lyklageymsla er staðsett</span><span class="sxs-lookup"><span data-stu-id="13679-311">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="13679-312">Auðkenni leigjanda þar sem geymslureikningur, forrit og lyklageymslur eru staðsett.</span><span class="sxs-lookup"><span data-stu-id="13679-312">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="13679-313">Til að finna þetta gildi skal opna [Azure-gátt](https://portal.azure.com), **Azure Active Directory** og afrita gildi **leigjandakennis**.</span><span class="sxs-lookup"><span data-stu-id="13679-313">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="13679-314">Gefðu upp DNS-heiti lyklageymslunnar</span><span class="sxs-lookup"><span data-stu-id="13679-314">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="13679-315">DNS-heiti lyklageymslu, t.d. `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="13679-315">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="13679-316">(Þetta gildi samsvarar DNS-heitinu sem er notað í einingaversluninni.)</span><span class="sxs-lookup"><span data-stu-id="13679-316">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="13679-317">Gefðu upp leyndarmálið sem inniheldur heiti geymslureikningsins</span><span class="sxs-lookup"><span data-stu-id="13679-317">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="13679-318">**geymsla-reikningur-heiti**</span><span class="sxs-lookup"><span data-stu-id="13679-318">**storage-account-name**</span></span> |
    | <span data-ttu-id="13679-319">Leyniheiti fyrir forritskenni sem verður notað til að fá aðgang að Data Lake</span><span class="sxs-lookup"><span data-stu-id="13679-319">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="13679-320">**forrit-auðkenni**</span><span class="sxs-lookup"><span data-stu-id="13679-320">**app-id**</span></span> |
    | <span data-ttu-id="13679-321">Leyniheiti sem verður notað með forritskenni</span><span class="sxs-lookup"><span data-stu-id="13679-321">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="13679-322">**forrit-leyndarmál**</span><span class="sxs-lookup"><span data-stu-id="13679-322">**app-secret**</span></span> |

5. <span data-ttu-id="13679-323">Samþykkið skilmálana og veljið **Setja upp**.</span><span class="sxs-lookup"><span data-stu-id="13679-323">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="13679-324">Viðbótin verður sett upp innan fárra mínútna.</span><span class="sxs-lookup"><span data-stu-id="13679-324">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="13679-325">Skilgreina AI Builder</span><span class="sxs-lookup"><span data-stu-id="13679-325">Configure AI Builder</span></span>

1. <span data-ttu-id="13679-326">Skráðu þig inn á LCS og opnaðu síðuna **Umhverfisupplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="13679-326">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="13679-327">Flettu að hlutanum **Innbætur umhverfis**.</span><span class="sxs-lookup"><span data-stu-id="13679-327">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="13679-328">Þú ættir að sjá innbæturnar sem eru þegar settar upp í þessu umhverfi.</span><span class="sxs-lookup"><span data-stu-id="13679-328">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="13679-329">Ef innbótin **Flytja út í Data Lake** er ekki á meðal þeirra skal skilgreina þessa innbót.</span><span class="sxs-lookup"><span data-stu-id="13679-329">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="13679-330">Veljið innbótina **Fá innsýn**.</span><span class="sxs-lookup"><span data-stu-id="13679-330">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="13679-331">Sláið inn eftirfarandi gildi á upplýsingasíðu innbótarinnar **Fá innsýn**.</span><span class="sxs-lookup"><span data-stu-id="13679-331">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="13679-332">Virði</span><span class="sxs-lookup"><span data-stu-id="13679-332">Value</span></span>                                                    | <span data-ttu-id="13679-333">lýsing</span><span class="sxs-lookup"><span data-stu-id="13679-333">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="13679-334">CDS-vefslóð fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="13679-334">CDS Organization URL</span></span>                                     | <span data-ttu-id="13679-335">Vefslóð Dataverse fyrirtækisins afrituð að ofan.</span><span class="sxs-lookup"><span data-stu-id="13679-335">The Dataverse organization URL copied from above.</span></span> |
    | <span data-ttu-id="13679-336">Auðkenni CDS-fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="13679-336">CDS Org ID</span></span>                                               | <span data-ttu-id="13679-337">Kenni Dataverse fyrirtækisins afritað að ofan.</span><span class="sxs-lookup"><span data-stu-id="13679-337">The Dataverse organization ID copied from above.</span></span> |
5. <span data-ttu-id="13679-338">Virkið **Er þetta sjálfgefna umhverfið fyrir leigjandann þinn**.</span><span class="sxs-lookup"><span data-stu-id="13679-338">Enable **Is this the default environment for you Tenant**.</span></span>
    
## <a name="configure-the-entity-store"></a><span data-ttu-id="13679-339">Grunnstilla einingaverslun</span><span class="sxs-lookup"><span data-stu-id="13679-339">Configure the entity store</span></span>

<span data-ttu-id="13679-340">Fylgið eftirfarandi skrefum til að setja upp einingaverslunina í Finance-umhverfinu.</span><span class="sxs-lookup"><span data-stu-id="13679-340">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="13679-341">Opnið **Kerfisstjórnun\> Uppsetning\> Kerfisfæribreytur \> Gagnatengingar**.</span><span class="sxs-lookup"><span data-stu-id="13679-341">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="13679-342">Stillið eftirfarandi lyklageymslusvæði:</span><span class="sxs-lookup"><span data-stu-id="13679-342">Set the following key vault fields:</span></span>

    - <span data-ttu-id="13679-343">**Forritskenni (biðlari)** – Sláið inn auðkenni forritsbiðlara sem var stofnaður áður.</span><span class="sxs-lookup"><span data-stu-id="13679-343">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="13679-344">**Leynilykill forrits** – Sláið inn leynilykil sem vistaður var fyrir forritið sem stofnað var áður.</span><span class="sxs-lookup"><span data-stu-id="13679-344">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="13679-345">**DNS-heiti** – Hægt er að finna heiti lénsheitakerfis á upplýsingasíðu forrits fyrir forritið sem var stofnað áður.</span><span class="sxs-lookup"><span data-stu-id="13679-345">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="13679-346">**Leynilykilsheiti** – Sláið inn **geymsla-reikningur-tenging-strengur**.</span><span class="sxs-lookup"><span data-stu-id="13679-346">**Secret name** – Enter **storage-account-connection-string**.</span></span>
3. <span data-ttu-id="13679-347">Virkið **Kveikja á samþættingu Data Lake**.</span><span class="sxs-lookup"><span data-stu-id="13679-347">Enable **Enable Data Lake integration**.</span></span>
4. <span data-ttu-id="13679-348">Veljið **Prófa Azure-lyklageymslu** og staðfestið að engar villur séu til staðar.</span><span class="sxs-lookup"><span data-stu-id="13679-348">Select **Test Azure Key Vault** and verify there are no errors.</span></span>
5. <span data-ttu-id="13679-349">Veljið **Prófa Azure Storage** og staðfestið að engar villur séu til staðar.</span><span class="sxs-lookup"><span data-stu-id="13679-349">Select **Test Azure storage** and verify there are no errors.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="13679-350">Ábendingar og stuðningur</span><span class="sxs-lookup"><span data-stu-id="13679-350">Feedback and support</span></span>

<span data-ttu-id="13679-351">Sendið tölvupóst á [Innsýn í greiðslur viðskiptavinar (forskoðun)](mailto:fiap@microsoft.com) ef áhugi er á að senda inn ábendingar eða aðstoð vantar.</span><span class="sxs-lookup"><span data-stu-id="13679-351">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="13679-352">Tilkynning um persónuvernd</span><span class="sxs-lookup"><span data-stu-id="13679-352">Privacy notice</span></span>

<span data-ttu-id="13679-353">Forútgáfur (1) kunna að nota minni persónuverndar- og öryggisráðstafanir og þjónusta Dynamics 365 Finance and Operations, (2) eru ekki hluti af þjónustustigssamningi fyrir þessa þjónustu, (3) ættu ekki að vera notaðar til að vinna úr persónulegum gögnum eða öðrum gögnum sem falla undir lögboðnar kröfur eða reglur um samræmi og (4) hafa takmarkaðan stuðning.</span><span class="sxs-lookup"><span data-stu-id="13679-353">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
