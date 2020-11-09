---
title: Skilgreina sýndareiningar Common Data Service
description: Þetta efnisatriði sýnir hvernig á að skilgreina sýndareiningar fyrir Dynamics 365 Human Resources. Búið til og uppfærið fyrirliggjandi sýndareiningar og greinið tiltækar einingar sem hafa verið búnar til.
author: andreabichsel
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 0d6f79ea569a7a9b0d25e73e8666bf9ba19095d0
ms.sourcegitcommit: a8665c47696028d371cdc4671db1fd8fcf9e1088
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/21/2020
ms.locfileid: "4058155"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="de9e8-104">Skilgreina sýndareiningar Common Data Service</span><span class="sxs-lookup"><span data-stu-id="de9e8-104">Configure Common Data Service virtual entities</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="de9e8-105">Dynamics 365 Human Resources er sýndargagnagjafi í Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="de9e8-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="de9e8-106">Hann býður upp á heildstæðar aðgerðir stofnunar, lesturs, uppfærslu og eyðingar (CRUD) úr Common Data Service og Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="de9e8-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="de9e8-107">Gögn fyrir sýndareiningar eru ekki geymd í Common Data Service, heldur í gagnagrunni forritsins.</span><span class="sxs-lookup"><span data-stu-id="de9e8-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="de9e8-108">Til að virkja CRUD-aðgerðir í Common Data Service, þarf að bjóða upp á einingarnar sem sýndareiningar í Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="de9e8-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="de9e8-109">Þetta gerir þér kleift að framkvæma CRUD-aðgerðir í Common Data Service og Microsoft Power Platform á gögnum sem eru í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="de9e8-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="de9e8-110">Aðgerðirnar styðja einnig sannprófanir á viðskiptagrunni Human Resources til að tryggja heilleika gagna þegar gögn eru skrifuð í einingarnar.</span><span class="sxs-lookup"><span data-stu-id="de9e8-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="de9e8-111">Tiltækar sýndareiningar fyrir Human Resources</span><span class="sxs-lookup"><span data-stu-id="de9e8-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="de9e8-112">Allar einingar Open Data Protocol í Human Resources eru í boði sem sýndareiningar í Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="de9e8-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="de9e8-113">Þetta er einnig tiltækt í Power Platform.</span><span class="sxs-lookup"><span data-stu-id="de9e8-113">They're also available in Power Platform.</span></span> <span data-ttu-id="de9e8-114">Nú er hægt að búa til forrit og upplifanir með gögnum beint úr Human Resources með fullum CRUD-möguleikum án þess að afrita eða samstilla gögn við Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="de9e8-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="de9e8-115">Hægt er að nota Power Apps-gáttir til að smíða útlit vefsvæða sem bjóða upp á samvinnu fyrir viðskiptaferla í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="de9e8-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="de9e8-116">Hægt er að skoða lista yfir sýndareiningar sem eru virkjaðar í umhverfinu og byrja að vinna með einingarnar í [Power Apps](https://make.powerapps.com) í lausninni **Sýndareiningar HR í Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="de9e8-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![Sýndareiningar HR í Dynamics 365 í Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="de9e8-118">Sýndareiningar í samanburði við venjulegar einingar</span><span class="sxs-lookup"><span data-stu-id="de9e8-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="de9e8-119">Sýndareiningar fyrir Human Resources eru ekki þær sömu og venjulegu Common Data Service-einingarnar sem búnar eru til fyrir Human Resources.</span><span class="sxs-lookup"><span data-stu-id="de9e8-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="de9e8-120">Venjulegu einingarnar fyrir Human Resources eru myndaðar sérstaklega og unnið með þær í HCM Common Solution í Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="de9e8-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="de9e8-121">Með venjulegum einingum eru gögnin geymd í Common Data Service og þarfnast samstillingar við gagnagrunn Human Resources-forritsins.</span><span class="sxs-lookup"><span data-stu-id="de9e8-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="de9e8-122">Til að sjá lista yfir venjulegar Common Data Service-einingar fyrir Human Resources skal fara í [Common Data Service einingar](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span><span class="sxs-lookup"><span data-stu-id="de9e8-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="de9e8-123">Setja upp</span><span class="sxs-lookup"><span data-stu-id="de9e8-123">Setup</span></span>

<span data-ttu-id="de9e8-124">Fylgið þessum uppsetningarskrefum til að virkja sýndareiningar í umhverfinu.</span><span class="sxs-lookup"><span data-stu-id="de9e8-124">Follow these setup steps to enable virtual entities in your environment.</span></span> 

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="de9e8-125">Skrá forritið í Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="de9e8-125">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="de9e8-126">Fyrst þarf að skrá forritið inn í Azure-gáttinni þannig að auðkenningarverkvangur Microsoft geti veitt sannvottunar- og leyfisþjónustu fyrir forritið og notendur.</span><span class="sxs-lookup"><span data-stu-id="de9e8-126">First, you need to register the app in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="de9e8-127">Frekari upplýsingar um skráningu forrita í Azure er að finna í [Stuttar leiðbeiningar: Skrá forrit með auðkenningarverkvangi Microsoft](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="de9e8-127">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="de9e8-128">Opnið [Microsoft Azure-gáttina](https://portal.azure.com)</span><span class="sxs-lookup"><span data-stu-id="de9e8-128">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="de9e8-129">Í listanum yfir Azure-þjónustur skal velja **Skráning forrita**.</span><span class="sxs-lookup"><span data-stu-id="de9e8-129">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="de9e8-130">Veljið **Ný skráning**.</span><span class="sxs-lookup"><span data-stu-id="de9e8-130">Select **New registration**.</span></span>

4. <span data-ttu-id="de9e8-131">Í reitinn **Heiti** skal færa inn lýsandi heiti á forritinu.</span><span class="sxs-lookup"><span data-stu-id="de9e8-131">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="de9e8-132">Til dæmis, **Dynamics 365 Human Resources Sýndareiningar**.</span><span class="sxs-lookup"><span data-stu-id="de9e8-132">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="de9e8-133">Í reitinn **Framsenda API** skal færa inn nafnarými vefslóðar fyrir tilvikið af Human Resources.</span><span class="sxs-lookup"><span data-stu-id="de9e8-133">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="de9e8-134">Veldu **Skrá**.</span><span class="sxs-lookup"><span data-stu-id="de9e8-134">Select **Register**.</span></span>

7. <span data-ttu-id="de9e8-135">Þegar skráningu lýkur birtir Azure-gáttin svæðið **Yfirlit** fyrir skráningu forritsins, sem felur í sér **Forritskenni (biðlari)**.</span><span class="sxs-lookup"><span data-stu-id="de9e8-135">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="de9e8-136">Takið niður **Forritskennið (biðlari)** á þessari stundu.</span><span class="sxs-lookup"><span data-stu-id="de9e8-136">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="de9e8-137">Þessar upplýsingar verða færðar inn þegar á að [Skilgreina gagnagjafa sýndareiningar](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="de9e8-137">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="de9e8-138">Á vinstra yfirlitssvæðinu skal velja **Vottorð og leynilyklar**.</span><span class="sxs-lookup"><span data-stu-id="de9e8-138">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="de9e8-139">Í hlutanum **Leynilyklar biðlara** á síðunni skal velja **Nýrr leynilykill biðlara**.</span><span class="sxs-lookup"><span data-stu-id="de9e8-139">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="de9e8-140">Gefið upp lýsingu, veljið tímalengd og veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="de9e8-140">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="de9e8-141">Skráið gildi fyrir leynilykil.</span><span class="sxs-lookup"><span data-stu-id="de9e8-141">Record the secret's value.</span></span> <span data-ttu-id="de9e8-142">Þessar upplýsingar verða færðar inn þegar á að [Skilgreina gagnagjafa sýndareiningar](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="de9e8-142">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="de9e8-143">Gætið þess að taka niður gildi leynilykilsins að svo stöddu.</span><span class="sxs-lookup"><span data-stu-id="de9e8-143">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="de9e8-144">Leynilykillinn er ekki sýndur aftur eftir að farið er af þessari síðu.</span><span class="sxs-lookup"><span data-stu-id="de9e8-144">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="de9e8-145">Setja upp forritið Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="de9e8-145">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="de9e8-146">Setja skal upp forritið Dynamics 365 HR Virtual Entity í Power Apps-umhverfinu til að virkja lausnapakka sýndareiningarinnar í Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="de9e8-146">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="de9e8-147">Opna [Power Platform stjórnendamiðstöð](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="de9e8-147">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="de9e8-148">Í listanum **Umhverfi** er valið Power Apps-umhverfi sem tengist tilviki Human Resources.</span><span class="sxs-lookup"><span data-stu-id="de9e8-148">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="de9e8-149">Í hlutanum **Tilföng** á síðunni skal velja **Dynamics 365-forrit**.</span><span class="sxs-lookup"><span data-stu-id="de9e8-149">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="de9e8-150">Veljið aðgerðina **Setja upp forrit**.</span><span class="sxs-lookup"><span data-stu-id="de9e8-150">Select the **Install app** action.</span></span>

5. <span data-ttu-id="de9e8-151">Veljið **Dynamics 365 HR Virtual Entity** og veljið **Áfram**.</span><span class="sxs-lookup"><span data-stu-id="de9e8-151">Select **Dynamics 365 HR Virtual Entity** , and select **Next**.</span></span>

6. <span data-ttu-id="de9e8-152">Yfirfara og merkja til að samþykkja þjónustuskilmála.</span><span class="sxs-lookup"><span data-stu-id="de9e8-152">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="de9e8-153">Velja **Setja upp**.</span><span class="sxs-lookup"><span data-stu-id="de9e8-153">Select **Install**.</span></span>

<span data-ttu-id="de9e8-154">Uppsetningin tekur örfáar mínútur.</span><span class="sxs-lookup"><span data-stu-id="de9e8-154">The install takes a few minutes.</span></span> <span data-ttu-id="de9e8-155">Þegar henni lýkur skal halda áfram í næsta skref.</span><span class="sxs-lookup"><span data-stu-id="de9e8-155">When it completes, continue to the next steps.</span></span>

![Setja upp forritið Dynamics 365 HR Virtual Entity úr Power Platform-stjórnendamiðstöðinni](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="de9e8-157">Skilgreining gagnagjafa sýndareiningar</span><span class="sxs-lookup"><span data-stu-id="de9e8-157">Configure the virtual entity data source</span></span> 

<span data-ttu-id="de9e8-158">Næsta skref er að skilgreina gagnagjafa sýndareiningar í Power Apps-umhverfinu.</span><span class="sxs-lookup"><span data-stu-id="de9e8-158">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="de9e8-159">Opna [Power Platform stjórnendamiðstöð](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="de9e8-159">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="de9e8-160">Í listanum **Umhverfi** er valið Power Apps-umhverfi sem tengist tilviki Human Resources.</span><span class="sxs-lookup"><span data-stu-id="de9e8-160">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="de9e8-161">Veljið **Vefslóð umhverfis** í hlutanum **Upplýsingar** á síðunni.</span><span class="sxs-lookup"><span data-stu-id="de9e8-161">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="de9e8-162">Í **heilsulausnarmiðstöð** skal velja táknið **Ítarleg leit** efst til hægri á forritssíðunni.</span><span class="sxs-lookup"><span data-stu-id="de9e8-162">In the **Solution Health Hub** , select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="de9e8-163">Á síðunni **Ítarleg leit** , í fellilistanum **Leita að** , skal velja **Finance and Operations Grunnstillingar sýndargagnagjafa**.</span><span class="sxs-lookup"><span data-stu-id="de9e8-163">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="de9e8-164">Veldu **Niðurstöður**.</span><span class="sxs-lookup"><span data-stu-id="de9e8-164">Select **Results**.</span></span>

7. <span data-ttu-id="de9e8-165">Veljið færsluna **Microsoft HR-gagnagjafi**.</span><span class="sxs-lookup"><span data-stu-id="de9e8-165">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="de9e8-166">Færa skal inn nauðsynlegar upplýsingar fyrir skilgreiningu gagnagjafans.</span><span class="sxs-lookup"><span data-stu-id="de9e8-166">Enter the required information for the data source configuration.</span></span>

   - <span data-ttu-id="de9e8-167">**Markvefslóð** : Vefslóð nafnarýmis Human Resources.</span><span class="sxs-lookup"><span data-stu-id="de9e8-167">**Target URL** : The URL of your Human Resources namespace.</span></span>
   - <span data-ttu-id="de9e8-168">**Auðkenni leigjanda** : Azure Active Directory (Azure AD) leigjandakenni.</span><span class="sxs-lookup"><span data-stu-id="de9e8-168">**Tenant ID** : The Azure Active Directory (Azure AD) tenant ID.</span></span>
   - <span data-ttu-id="de9e8-169">**AAD-forritskenni** : Forritskennið (biðlarinn) sem er stofnað fyrir forritið sem er skráð í Microsoft Azure-gáttina.</span><span class="sxs-lookup"><span data-stu-id="de9e8-169">**AAD Application ID** : The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="de9e8-170">Þú fékkst þessar upplýsingar fyrr í skrefinu [Skrá forritið í Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="de9e8-170">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>
   - <span data-ttu-id="de9e8-171">**Leynilykill AAD-forrits** : Leynilykill biðlara sem er stofnað fyrir forritið sem er skráð í Microsoft Azure-gáttina.</span><span class="sxs-lookup"><span data-stu-id="de9e8-171">**AAD Application Secret** : The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="de9e8-172">Þú fékkst þessar upplýsingar fyrr í skrefinu [Skrá forritið í Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="de9e8-172">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

9. <span data-ttu-id="de9e8-173">Veljið **Vista og loka**.</span><span class="sxs-lookup"><span data-stu-id="de9e8-173">Select **Save & Close**.</span></span>

   ![Microsoft HR-gagnagjafi](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="de9e8-175">Veita forritsheimildir í Human Resources</span><span class="sxs-lookup"><span data-stu-id="de9e8-175">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="de9e8-176">Veitið heimildir fyrir tvö Azure AD-forrit í Human Resources:</span><span class="sxs-lookup"><span data-stu-id="de9e8-176">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="de9e8-177">Forritið sem var stofnað fyrir leigjanda í Microsoft Azure gáttinni</span><span class="sxs-lookup"><span data-stu-id="de9e8-177">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="de9e8-178">Forritið Dynamics 365 HR Virtual Entity sem var sett upp í Power Apps-umhverfinu</span><span class="sxs-lookup"><span data-stu-id="de9e8-178">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="de9e8-179">Í Human Resources skal opna síðuna **Azure Active Directory-forrit**.</span><span class="sxs-lookup"><span data-stu-id="de9e8-179">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="de9e8-180">Velja skal **Ný** til að búa til nýja færslu forrits:</span><span class="sxs-lookup"><span data-stu-id="de9e8-180">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="de9e8-181">Í reitinn **Biðlarakenni** skal færa inn kenni biðlara fyrir forritið sem var skráð í Microsoft Azure-gáttina.</span><span class="sxs-lookup"><span data-stu-id="de9e8-181">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="de9e8-182">Í reitinn **Heiti** skal færa inn heiti forritsins sem var skráð í Microsoft Azure-gáttina.</span><span class="sxs-lookup"><span data-stu-id="de9e8-182">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="de9e8-183">Í reitinn **Notandakenni** skal velja notandakenni notanda með stjórnandaheimildir í Human Resources og Power Apps-umhverfinu.</span><span class="sxs-lookup"><span data-stu-id="de9e8-183">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="de9e8-184">Veljið **Ný** til að búa til aðra færslu forrits:</span><span class="sxs-lookup"><span data-stu-id="de9e8-184">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="de9e8-185">**Auðkenni biðlara** : f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="de9e8-185">**Client Id** : f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="de9e8-186">**Heiti** : Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="de9e8-186">**Name** : Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="de9e8-187">Í reitinn **Notandakenni** skal velja notandakenni notanda með stjórnandaheimildir í Human Resources og Power Apps-umhverfinu.</span><span class="sxs-lookup"><span data-stu-id="de9e8-187">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="de9e8-188">Mynda sýndareiningar</span><span class="sxs-lookup"><span data-stu-id="de9e8-188">Generate virtual entities</span></span>

<span data-ttu-id="de9e8-189">Þegar uppsetningu er lokið er hægt að velja sýndareiningarnar sem á að mynda og virkja í Common Data Service-tilvikinu.</span><span class="sxs-lookup"><span data-stu-id="de9e8-189">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="de9e8-190">Í Human Resources skal opna síðuna **Common Data Service (CDS)-samþætting**.</span><span class="sxs-lookup"><span data-stu-id="de9e8-190">In Human Resources, open the **Common Data Service (CDS) integration** page.</span></span>

2. <span data-ttu-id="de9e8-191">Veldu flipann **Sýndareiningar**.</span><span class="sxs-lookup"><span data-stu-id="de9e8-191">Select the **Virtual entities** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="de9e8-192">**Virkjar sýndareininguna** verður stillt á **Já** sjálfkrafa þegar allri nauðsynlegri uppsetningu er lokið.</span><span class="sxs-lookup"><span data-stu-id="de9e8-192">The **Enable the virtual entity** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="de9e8-193">Ef skipting er stillt á **Nei** skal fara yfir skrefin í fyrri hlutum þessa skjals til að tryggja að uppsetningu forútgáfu sé lokið.</span><span class="sxs-lookup"><span data-stu-id="de9e8-193">If the toggle is set to **No** , review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="de9e8-194">Velja skal eininguna eða einingarnar sem á að búa til í Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="de9e8-194">Select the entity or entities you want to generate in Common Data Service.</span></span>

4. <span data-ttu-id="de9e8-195">Velja **Búa til/uppfæra**.</span><span class="sxs-lookup"><span data-stu-id="de9e8-195">Select **Generate/refresh**.</span></span>

![Common Data Service Samþætting](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a><span data-ttu-id="de9e8-197">Athuga einingu um myndunarstöðu</span><span class="sxs-lookup"><span data-stu-id="de9e8-197">Check entity generation status</span></span>

<span data-ttu-id="de9e8-198">Sýndareiningar eru myndaðar í Common Data Service í gegnum ósamstillta bakgrunnsvinnslu.</span><span class="sxs-lookup"><span data-stu-id="de9e8-198">Virtual entities are generated in Common Data Service through an asynchronous background process.</span></span> <span data-ttu-id="de9e8-199">Uppfærslur á ferlinu birtast í aðgerðamiðstöð.</span><span class="sxs-lookup"><span data-stu-id="de9e8-199">Updates on the process display in the action center.</span></span> <span data-ttu-id="de9e8-200">Upplýsingar um ferlið, þar á meðal villukladda, birtast á síðunni **Sjálfvirkni ferlis**.</span><span class="sxs-lookup"><span data-stu-id="de9e8-200">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="de9e8-201">Í Human Resources skal opna síðuna **Sjálfvirkni ferlis**.</span><span class="sxs-lookup"><span data-stu-id="de9e8-201">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="de9e8-202">Veljið flipann **Bakgrunnsvinnslur**.</span><span class="sxs-lookup"><span data-stu-id="de9e8-202">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="de9e8-203">Velið **Virtual einingakönnun async Aðgerðar bakgrunnsvinnsla**.</span><span class="sxs-lookup"><span data-stu-id="de9e8-203">Select **Virtual entity poll async operation background process**.</span></span>

4. <span data-ttu-id="de9e8-204">Veldu **Skoða síðustu niðurstöður**.</span><span class="sxs-lookup"><span data-stu-id="de9e8-204">Select **View most recent results**.</span></span>

<span data-ttu-id="de9e8-205">Hlðarsvæði sýnir nýjustu niðurstöður framkvæmdarinnar fyrir ferlið.</span><span class="sxs-lookup"><span data-stu-id="de9e8-205">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="de9e8-206">Hægt er að skoða kladda vinnslunnar, þar á meðal allar villur sem skilað er frá Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="de9e8-206">You can view the log for the process, including any errors returned from Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="de9e8-207">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="de9e8-207">See also</span></span>

[<span data-ttu-id="de9e8-208">Hvað er Common Data Service?</span><span class="sxs-lookup"><span data-stu-id="de9e8-208">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="de9e8-209">Einingayfirlit</span><span class="sxs-lookup"><span data-stu-id="de9e8-209">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="de9e8-210">Yfirlit einingartengsla</span><span class="sxs-lookup"><span data-stu-id="de9e8-210">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="de9e8-211">Stofna og breyta sýndareiningum sem innihalda gögn frá ytri gagnagjafa</span><span class="sxs-lookup"><span data-stu-id="de9e8-211">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="de9e8-212">Hvað eru Power Apps-gáttir?</span><span class="sxs-lookup"><span data-stu-id="de9e8-212">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="de9e8-213">Yfirlit yfir stofnun forrita í Power Apps</span><span class="sxs-lookup"><span data-stu-id="de9e8-213">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
