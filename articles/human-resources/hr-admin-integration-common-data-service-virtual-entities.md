---
title: Skilgreina Dataverse-sýndartöflur
description: Þetta efnisatriði sýnir hvernig á að skilgreina sýndartöflur fyrir Dynamics 365 Human Resources. Búið til og uppfærið fyrirliggjandi sýndartöflur og greinið tiltækar töflur sem hafa verið búnar til.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 04997aba427ae6013c8154593b09ae1a45a580c3
ms.sourcegitcommit: 9283caad2d0636f98579c995784abec19fda2e3f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935754"
---
# <a name="configure-dataverse-virtual-tables"></a><span data-ttu-id="ffa62-104">Skilgreina Dataverse-sýndartöflur</span><span class="sxs-lookup"><span data-stu-id="ffa62-104">Configure Dataverse virtual tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ffa62-105">Dynamics 365 Human Resources er sýndargagnagjafi í Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ffa62-105">Dynamics 365 Human Resources is a virtual data source in Microsoft Dataverse.</span></span> <span data-ttu-id="ffa62-106">Hann býður upp á heildstæðar aðgerðir stofnunar, lesturs, uppfærslu og eyðingar (CRUD) úr Dataverse og Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="ffa62-106">It provides full create, read, update, and delete (CRUD) operations from Dataverse and Microsoft Power Platform.</span></span> <span data-ttu-id="ffa62-107">Gögn fyrir sýndartöflur eru ekki geymd í Dataverse, heldur í gagnagrunni forritsins.</span><span class="sxs-lookup"><span data-stu-id="ffa62-107">The data for virtual tables isn't stored in Dataverse, but in the application database.</span></span>

<span data-ttu-id="ffa62-108">Til að virkja CRUD-aðgerðir í einingum Human Resources úr Dataverse þarf að bjóða upp á einingarnar sem sýndartöflur í Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ffa62-108">To enable CRUD operations on Human Resources entities from Dataverse, you must make the entities available as virtual tables in Dataverse.</span></span> <span data-ttu-id="ffa62-109">Þetta gerir þér kleift að framkvæma CRUD-aðgerðir í Dataverse og Microsoft Power Platform á gögnum sem eru í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ffa62-109">This lets you perform CRUD operations from Dataverse and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="ffa62-110">Aðgerðirnar styðja einnig sannprófanir á viðskiptagrunni Human Resources til að tryggja heilleika gagna þegar gögn eru skrifuð í einingarnar.</span><span class="sxs-lookup"><span data-stu-id="ffa62-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

> [!NOTE]
> <span data-ttu-id="ffa62-111">Mannauðseiningar samsvara Dataverse töflum.</span><span class="sxs-lookup"><span data-stu-id="ffa62-111">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="ffa62-112">Frekari upplýsingar um Dataverse (áður Common Data Service) og uppfærslur á hugtökum er að finna í [Hvað er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="ffa62-112">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

## <a name="available-virtual-tables-for-human-resources"></a><span data-ttu-id="ffa62-113">Tiltækar sýndartöflur fyrir Human Resources</span><span class="sxs-lookup"><span data-stu-id="ffa62-113">Available virtual tables for Human Resources</span></span>

<span data-ttu-id="ffa62-114">Allar einingar Open Data Protocol (OData) í Human Resources eru í boði sem sýndartöflur í Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ffa62-114">All Open Data Protocol (OData) entities in Human Resources are available as virtual tables in Dataverse.</span></span> <span data-ttu-id="ffa62-115">Þetta er einnig tiltækt í Power Platform.</span><span class="sxs-lookup"><span data-stu-id="ffa62-115">They're also available in Power Platform.</span></span> <span data-ttu-id="ffa62-116">Nú er hægt að búa til forrit og upplifanir með gögnum beint úr Human Resources með fullum CRUD-möguleikum án þess að afrita eða samstilla gögn við Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ffa62-116">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Dataverse.</span></span> <span data-ttu-id="ffa62-117">Hægt er að nota Power Apps-gáttir til að smíða útlit vefsvæða sem bjóða upp á samvinnu fyrir viðskiptaferla í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ffa62-117">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="ffa62-118">Hægt er að skoða lista yfir sýndartöflur sem eru virkjaðar í umhverfinu og byrja að vinna með töflurnar í [Power Apps](https://make.powerapps.com) í lausninni **Sýndartöflur HR í Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="ffa62-118">You can view the list of virtual tables enabled in the environment, and begin working with the tables in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Tables** solution.</span></span>

![Sýndartöflur HR í Dynamics 365 í Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a><span data-ttu-id="ffa62-120">Sýndartöflur í samanburði við venjulegar töflur</span><span class="sxs-lookup"><span data-stu-id="ffa62-120">Virtual tables versus native tables</span></span>

<span data-ttu-id="ffa62-121">Sýndartöflur fyrir Human Resources eru ekki þær sömu og venjulegu Dataverse-töflurnar sem búnar eru til fyrir Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ffa62-121">Virtual tables for Human Resources aren't the same as the native Dataverse tables created for Human Resources.</span></span> 

<span data-ttu-id="ffa62-122">Venjulegu töflurnar fyrir Human Resources eru myndaðar sérstaklega og unnið með þær í lausn HCM Common í Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ffa62-122">The native tables for Human Resources are generated separately and maintained in the HCM Common solution in Dataverse.</span></span> <span data-ttu-id="ffa62-123">Með venjulegum töflum eru gögnin geymd í Dataverse og þarfnast samstillingar við gagnagrunn Human Resources-forritsins.</span><span class="sxs-lookup"><span data-stu-id="ffa62-123">With native tables, the data is stored in Dataverse and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="ffa62-124">Til að sjá lista yfir venjulegar Dataverse-töflur fyrir Human Resources skal fara í [Dataverse-töflur](./hr-developer-entities.md).</span><span class="sxs-lookup"><span data-stu-id="ffa62-124">For a list of the native Dataverse tables for Human Resources, see [Dataverse tables](./hr-developer-entities.md).</span></span>

## <a name="setup"></a><span data-ttu-id="ffa62-125">Setja upp</span><span class="sxs-lookup"><span data-stu-id="ffa62-125">Setup</span></span>

<span data-ttu-id="ffa62-126">Fylgið þessum uppsetningarskrefum til að virkja sýndartöflur í umhverfinu.</span><span class="sxs-lookup"><span data-stu-id="ffa62-126">Follow these setup steps to enable virtual tables in your environment.</span></span>

### <a name="enable-virtual-tables-in-human-resources"></a><span data-ttu-id="ffa62-127">Virkja sýndartöflur í Human Resources</span><span class="sxs-lookup"><span data-stu-id="ffa62-127">Enable virtual tables in Human Resources</span></span>

<span data-ttu-id="ffa62-128">Fyrst þarf að virkja sýndartöflur í vinnusvæðinu **Eiginleikastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="ffa62-128">First, you must enable virtual tables in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="ffa62-129">Veldu í Human Resources **Kerfisstjórnun**.</span><span class="sxs-lookup"><span data-stu-id="ffa62-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="ffa62-130">Veldu reitinn **Stjórnun eiginleika**.</span><span class="sxs-lookup"><span data-stu-id="ffa62-130">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="ffa62-131">Veldu **Stuðningur sýndartöflu fyrir HR í Dataverse** og veldu því næst **Virkja**.</span><span class="sxs-lookup"><span data-stu-id="ffa62-131">Select **Virtual table support for HR in Dataverse**, and then select **Enable**.</span></span>

<span data-ttu-id="ffa62-132">Frekari upplýsingar um virkjun og óvirkjun eiginleika er að finna í [Vinna með eiginleika](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="ffa62-132">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="ffa62-133">Skrá forritið í Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="ffa62-133">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="ffa62-134">Skrá þarf Human Resources tilvikið inn í Azure-gáttinni þannig að auðkenningarverkvangur Microsoft geti veitt sannvottunar- og leyfisþjónustu fyrir forritið og notendur.</span><span class="sxs-lookup"><span data-stu-id="ffa62-134">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="ffa62-135">Frekari upplýsingar um skráningu forrita í Azure er að finna í [Stuttar leiðbeiningar: Skrá forrit með auðkenningarverkvangi Microsoft](/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="ffa62-135">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="ffa62-136">Opnið [Microsoft Azure-gáttina](https://portal.azure.com)</span><span class="sxs-lookup"><span data-stu-id="ffa62-136">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="ffa62-137">Í listanum yfir Azure-þjónustur skal velja **Skráning forrita**.</span><span class="sxs-lookup"><span data-stu-id="ffa62-137">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="ffa62-138">Veljið **Ný skráning**.</span><span class="sxs-lookup"><span data-stu-id="ffa62-138">Select **New registration**.</span></span>

4. <span data-ttu-id="ffa62-139">Í reitinn **Heiti** skal færa inn lýsandi heiti á forritinu.</span><span class="sxs-lookup"><span data-stu-id="ffa62-139">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="ffa62-140">Til dæmis **Dynamics 365 Human Resources Sýndartöflur**.</span><span class="sxs-lookup"><span data-stu-id="ffa62-140">For example, **Dynamics 365 Human Resources Virtual Tables**.</span></span>

5. <span data-ttu-id="ffa62-141">Í reitinn **Framsenda API** skal færa inn nafnarými vefslóðar fyrir tilvikið af Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ffa62-141">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="ffa62-142">Veldu **Skrá**.</span><span class="sxs-lookup"><span data-stu-id="ffa62-142">Select **Register**.</span></span>

7. <span data-ttu-id="ffa62-143">Þegar skráningu lýkur birtir Azure-gáttin svæðið **Yfirlit** fyrir skráningu forritsins, sem felur í sér **Forritskenni (biðlari)**.</span><span class="sxs-lookup"><span data-stu-id="ffa62-143">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="ffa62-144">Takið niður **Forritskennið (biðlari)** á þessari stundu.</span><span class="sxs-lookup"><span data-stu-id="ffa62-144">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="ffa62-145">Þessar upplýsingar verða færðar inn þegar á að [Skilgreina gagnagjafa sýndartöflu](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="ffa62-145">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

8. <span data-ttu-id="ffa62-146">Á vinstra yfirlitssvæðinu skal velja **Vottorð og leynilyklar**.</span><span class="sxs-lookup"><span data-stu-id="ffa62-146">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="ffa62-147">Í hlutanum **Leynilyklar biðlara** á síðunni skal velja **Nýrr leynilykill biðlara**.</span><span class="sxs-lookup"><span data-stu-id="ffa62-147">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="ffa62-148">Gefið upp lýsingu, veljið tímalengd og veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="ffa62-148">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="ffa62-149">Skráðu gildi leyndarmálsins úr **Gildi** eiginleika töflunnar.</span><span class="sxs-lookup"><span data-stu-id="ffa62-149">Record the secret's value from the **Value** property of the table.</span></span> <span data-ttu-id="ffa62-150">Þessar upplýsingar verða færðar inn þegar á að [Skilgreina gagnagjafa sýndartöflu](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="ffa62-150">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="ffa62-151">Gætið þess að taka niður gildi leynilykilsins að svo stöddu.</span><span class="sxs-lookup"><span data-stu-id="ffa62-151">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="ffa62-152">Leynilykillinn er ekki sýndur aftur eftir að farið er af þessari síðu.</span><span class="sxs-lookup"><span data-stu-id="ffa62-152">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a><span data-ttu-id="ffa62-153">Setja upp forritið Dynamics 365 Virtual Table</span><span class="sxs-lookup"><span data-stu-id="ffa62-153">Install the Dynamics 365 HR Virtual Table app</span></span>

<span data-ttu-id="ffa62-154">Setja skal upp forritið Dynamics 365 HR Virtual Table í Power Apps-umhverfinu til að virkja lausnapakka sýndartöflunnar í Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ffa62-154">Install the Dynamics 365 HR Virtual Table app in your Power Apps environment to deploy the virtual table solution package to Dataverse.</span></span>

1. <span data-ttu-id="ffa62-155">Í Human Resources skal opna síðuna **Microsoft Dataverse-samþætting**.</span><span class="sxs-lookup"><span data-stu-id="ffa62-155">In Human Resources, open the **Microsoft Dataverse integration** page.</span></span>

2. <span data-ttu-id="ffa62-156">Veljið flipann **Sýndartöflur**.</span><span class="sxs-lookup"><span data-stu-id="ffa62-156">Select the **Virtual tables** tab.</span></span>

3. <span data-ttu-id="ffa62-157">Veljið **Setja upp sýndartöfluforrit**.</span><span class="sxs-lookup"><span data-stu-id="ffa62-157">Select **Install virtual table app**.</span></span>

### <a name="configure-the-virtual-table-data-source"></a><span data-ttu-id="ffa62-158">Skilgreina gagnagjafa sýndartöflu</span><span class="sxs-lookup"><span data-stu-id="ffa62-158">Configure the virtual table data source</span></span>

<span data-ttu-id="ffa62-159">Næsta skref er að skilgreina gagnagjafa sýndartöflu í Power Apps-umhverfinu.</span><span class="sxs-lookup"><span data-stu-id="ffa62-159">The next step is to configure the virtual table data source in the Power Apps environment.</span></span>

1. <span data-ttu-id="ffa62-160">Opna [Power Platform stjórnendamiðstöð](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="ffa62-160">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="ffa62-161">Í listanum **Umhverfi** er valið Power Apps-umhverfi sem tengist tilviki Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ffa62-161">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="ffa62-162">Veljið **Vefslóð umhverfis** í hlutanum **Upplýsingar** á síðunni.</span><span class="sxs-lookup"><span data-stu-id="ffa62-162">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="ffa62-163">Í **heilsulausnarmiðstöð** skal velja táknið **Ítarleg leit** efst til hægri á forritssíðunni.</span><span class="sxs-lookup"><span data-stu-id="ffa62-163">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="ffa62-164">Á síðunni **Ítarleg leit**, í fellilistanum **Leita að**, skal velja **Finance and Operations Grunnstillingar sýndargagnagjafa**.</span><span class="sxs-lookup"><span data-stu-id="ffa62-164">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="ffa62-165">Uppsetning sýndartöfluforritsins úr fyrra uppsetningarskrefi getur tekið nokkrar mínútur.</span><span class="sxs-lookup"><span data-stu-id="ffa62-165">The installation of the virtual table app from the previous setup step can take a few minutes.</span></span> <span data-ttu-id="ffa62-166">Ef **Finance and Operations Skilgreiningar sýndargagnagjafa** eru ekki í boði í listanum skal hinkra smástund og svo uppfæra listann.</span><span class="sxs-lookup"><span data-stu-id="ffa62-166">If **Finance and Operations Virtual Data Source Configurations** isn't available in the list, wait for a minute and refresh the list.</span></span>

6. <span data-ttu-id="ffa62-167">Veldu **Niðurstöður**.</span><span class="sxs-lookup"><span data-stu-id="ffa62-167">Select **Results**.</span></span>

7. <span data-ttu-id="ffa62-168">Veljið færsluna **Microsoft HR-gagnagjafi**.</span><span class="sxs-lookup"><span data-stu-id="ffa62-168">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="ffa62-169">Færa skal inn nauðsynlegar upplýsingar fyrir skilgreiningu gagnagjafans:</span><span class="sxs-lookup"><span data-stu-id="ffa62-169">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="ffa62-170">**Markvefslóð**: Vefslóð nafnarýmis Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ffa62-170">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="ffa62-171">Snið URL viðtöku er:</span><span class="sxs-lookup"><span data-stu-id="ffa62-171">The format of the target URL is:</span></span>
     
     <span data-ttu-id="ffa62-172">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="ffa62-172">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="ffa62-173">Dæmi:</span><span class="sxs-lookup"><span data-stu-id="ffa62-173">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="ffa62-174">Gætið þess að taka „**/**“ stafinn með í lok vefslóðarinnar til að forðast villu.</span><span class="sxs-lookup"><span data-stu-id="ffa62-174">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="ffa62-175">**Auðkenni leigjanda**: Azure Active Directory (Azure AD) leigjandakenni.</span><span class="sxs-lookup"><span data-stu-id="ffa62-175">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="ffa62-176">**AAD-forritskenni**: Forritskennið (biðlarinn) sem er stofnað fyrir forritið sem er skráð í Microsoft Azure-gáttina.</span><span class="sxs-lookup"><span data-stu-id="ffa62-176">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="ffa62-177">Þú fékkst þessar upplýsingar fyrr í skrefinu [Skrá forritið í Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="ffa62-177">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="ffa62-178">**Leynilykill AAD-forrits**: Leynilykill biðlara sem er stofnað fyrir forritið sem er skráð í Microsoft Azure-gáttina.</span><span class="sxs-lookup"><span data-stu-id="ffa62-178">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="ffa62-179">Þú fékkst þessar upplýsingar fyrr í skrefinu [Skrá forritið í Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="ffa62-179">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![Microsoft HR-gagnagjafi](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="ffa62-181">Veljið **Vista og loka**.</span><span class="sxs-lookup"><span data-stu-id="ffa62-181">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="ffa62-182">Veita forritsheimildir í Human Resources</span><span class="sxs-lookup"><span data-stu-id="ffa62-182">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="ffa62-183">Veitið heimildir fyrir tvö Azure AD-forrit í Human Resources:</span><span class="sxs-lookup"><span data-stu-id="ffa62-183">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="ffa62-184">Forritið sem var stofnað fyrir leigjanda í Microsoft Azure gáttinni</span><span class="sxs-lookup"><span data-stu-id="ffa62-184">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="ffa62-185">Forritið Dynamics 365 HR Virtual Table sem var sett upp í Power Apps-umhverfinu</span><span class="sxs-lookup"><span data-stu-id="ffa62-185">The Dynamics 365 HR Virtual Table app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="ffa62-186">Í Human Resources skal opna síðuna **Azure Active Directory-forrit**.</span><span class="sxs-lookup"><span data-stu-id="ffa62-186">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="ffa62-187">Velja skal **Ný** til að búa til nýja færslu forrits:</span><span class="sxs-lookup"><span data-stu-id="ffa62-187">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="ffa62-188">Í reitinn **Biðlarakenni** skal færa inn kenni biðlara fyrir forritið sem var skráð í Microsoft Azure-gáttina.</span><span class="sxs-lookup"><span data-stu-id="ffa62-188">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="ffa62-189">Í reitinn **Heiti** skal færa inn heiti forritsins sem var skráð í Microsoft Azure-gáttina.</span><span class="sxs-lookup"><span data-stu-id="ffa62-189">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="ffa62-190">Í reitinn **Notandakenni** skal velja notandakenni notanda með stjórnandaheimildir í Human Resources og Power Apps-umhverfinu.</span><span class="sxs-lookup"><span data-stu-id="ffa62-190">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="ffa62-191">Veljið **Ný** til að búa til aðra færslu forrits:</span><span class="sxs-lookup"><span data-stu-id="ffa62-191">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="ffa62-192">**Auðkenni biðlara**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="ffa62-192">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="ffa62-193">**Heiti**: Dynamics 365 HR Virtual Table</span><span class="sxs-lookup"><span data-stu-id="ffa62-193">**Name**: Dynamics 365 HR Virtual Table</span></span>
    - <span data-ttu-id="ffa62-194">Í reitinn **Notandakenni** skal velja notandakenni notanda með stjórnandaheimildir í Human Resources og Power Apps-umhverfinu.</span><span class="sxs-lookup"><span data-stu-id="ffa62-194">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-tables"></a><span data-ttu-id="ffa62-195">Mynda sýndartöflur</span><span class="sxs-lookup"><span data-stu-id="ffa62-195">Generate virtual tables</span></span>

<span data-ttu-id="ffa62-196">Þegar uppsetningu er lokið er hægt að velja sýndartöflurnar sem á að mynda og virkja í Dataverse-tilvikinu.</span><span class="sxs-lookup"><span data-stu-id="ffa62-196">When setup completes, you can select the virtual tables you want to generate and enable in your Dataverse instance.</span></span>

1. <span data-ttu-id="ffa62-197">Í Human Resources skal opna síðuna **Microsoft Dataverse-samþætting**.</span><span class="sxs-lookup"><span data-stu-id="ffa62-197">In Human Resources, open the **Microsoft Dataverse integration** page.</span></span>

2. <span data-ttu-id="ffa62-198">Veljið flipann **Sýndartöflur**.</span><span class="sxs-lookup"><span data-stu-id="ffa62-198">Select the **Virtual tables** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="ffa62-199">**Virkjar sýndartöflur** verður stillt á **Já** sjálfkrafa þegar allri nauðsynlegri uppsetningu er lokið.</span><span class="sxs-lookup"><span data-stu-id="ffa62-199">The **Enable virtual tables** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="ffa62-200">Ef skipting er stillt á **Nei** skal fara yfir skrefin í fyrri hlutum þessa skjals til að tryggja að uppsetningu forútgáfu sé lokið.</span><span class="sxs-lookup"><span data-stu-id="ffa62-200">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="ffa62-201">Veljið töfluna eða töflurnar sem á að búa til í Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ffa62-201">Select the table or tables you want to generate in Dataverse.</span></span>

4. <span data-ttu-id="ffa62-202">Velja **Búa til/uppfæra**.</span><span class="sxs-lookup"><span data-stu-id="ffa62-202">Select **Generate/refresh**.</span></span>

![Dataverse Samþætting](./media/hr-admin-integration-dataverse-integration.png)

## <a name="check-table-generation-status"></a><span data-ttu-id="ffa62-204">Athuga myndunarstöðu töflu</span><span class="sxs-lookup"><span data-stu-id="ffa62-204">Check table generation status</span></span>

<span data-ttu-id="ffa62-205">Sýndartöflur eru myndaðar í Dataverse í gegnum ósamstillta bakgrunnsvinnslu.</span><span class="sxs-lookup"><span data-stu-id="ffa62-205">Virtual tables are generated in Dataverse through an asynchronous background process.</span></span> <span data-ttu-id="ffa62-206">Uppfærslur á ferlinu birtast í aðgerðamiðstöð.</span><span class="sxs-lookup"><span data-stu-id="ffa62-206">Updates on the process display in the action center.</span></span> <span data-ttu-id="ffa62-207">Upplýsingar um ferlið, þar á meðal villukladda, birtast á síðunni **Sjálfvirkni ferlis**.</span><span class="sxs-lookup"><span data-stu-id="ffa62-207">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="ffa62-208">Í Human Resources skal opna síðuna **Sjálfvirkni ferlis**.</span><span class="sxs-lookup"><span data-stu-id="ffa62-208">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="ffa62-209">Veljið flipann **Bakgrunnsvinnslur**.</span><span class="sxs-lookup"><span data-stu-id="ffa62-209">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="ffa62-210">Veljið **Bakgrunnsvinnsla á ósamstilltri aðgerð sýndartöflukönnunar**.</span><span class="sxs-lookup"><span data-stu-id="ffa62-210">Select **Virtual table poll async operation background process**.</span></span>

4. <span data-ttu-id="ffa62-211">Veldu **Skoða síðustu niðurstöður**.</span><span class="sxs-lookup"><span data-stu-id="ffa62-211">Select **View most recent results**.</span></span>

<span data-ttu-id="ffa62-212">Hlðarsvæði sýnir nýjustu niðurstöður framkvæmdarinnar fyrir ferlið.</span><span class="sxs-lookup"><span data-stu-id="ffa62-212">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="ffa62-213">Hægt er að skoða kladda vinnslunnar, þar á meðal allar villur sem skilað er frá Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ffa62-213">You can view the log for the process, including any errors returned from Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="ffa62-214">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="ffa62-214">See also</span></span>

[<span data-ttu-id="ffa62-215">Hvað er Dataverse?</span><span class="sxs-lookup"><span data-stu-id="ffa62-215">What is Dataverse?</span></span>](/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="ffa62-216">Töflur í Dataverse</span><span class="sxs-lookup"><span data-stu-id="ffa62-216">Tables in Dataverse</span></span>](/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="ffa62-217">Yfirlit töflutengsla</span><span class="sxs-lookup"><span data-stu-id="ffa62-217">Table relationships overview</span></span>](/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="ffa62-218">Stofna og breyta sýndartöflum sem innihalda gögn frá ytri gagnagjafa</span><span class="sxs-lookup"><span data-stu-id="ffa62-218">Create and edit virtual tables that contain data from an external data source</span></span>](/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="ffa62-219">Hvað eru Power Apps-gáttir?</span><span class="sxs-lookup"><span data-stu-id="ffa62-219">What is Power Apps portals?</span></span>](/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="ffa62-220">Yfirlit yfir stofnun forrita í Power Apps</span><span class="sxs-lookup"><span data-stu-id="ffa62-220">Overview of creating apps in Power Apps</span></span>](/powerapps/maker/)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
