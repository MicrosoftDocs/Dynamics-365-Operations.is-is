---
title: Samþætta við LinkedIn Talent Hub
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp samþættingu milli Microsoft Dynamics 365 Human Resources og LinkedIn Talent Hub.
author: jaredha
manager: tfehr
ms.date: 10/20/2020
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
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6f70e3a6ccf9770c75334d355db5e9df9ee912dd
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527886"
---
# <a name="integrate-with-linkedin-talent-hub"></a><span data-ttu-id="9ebc4-103">Samþætta við LinkedIn Talent Hub</span><span class="sxs-lookup"><span data-stu-id="9ebc4-103">Integrate with LinkedIn Talent Hub</span></span>

[!include [banner](includes/preview-feature.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="9ebc4-104">[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) er verkvangur rakningakerfis umsækjenda (ATS).</span><span class="sxs-lookup"><span data-stu-id="9ebc4-104">[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) is an applicant tracking system (ATS) platform.</span></span> <span data-ttu-id="9ebc4-105">Það gerir þér kleift að finna, hafa umsjón með og ráða starfsmenn, allt á einum stað.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-105">It lets you source, manage, and hire employees all in one place.</span></span> <span data-ttu-id="9ebc4-106">Með því að samþætta Microsoft Dynamics 365 Human Resources við LinkedIn Talent Hub er auðveldlega hægt að stofna starfsmannafærslur í Human Resources fyrir umsækjendur sem hafa verið ráðnir í stöðu.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-106">By integrating Microsoft Dynamics 365 Human Resources with LinkedIn Talent Hub, you can easily create employee records in Human Resources for applicants who have been hired for a position.</span></span>

## <a name="setup"></a><span data-ttu-id="9ebc4-107">Setja upp</span><span class="sxs-lookup"><span data-stu-id="9ebc4-107">Setup</span></span>

<span data-ttu-id="9ebc4-108">Kerfisstjóri þarf að ljúka uppsetningarverkum til að virkja samþættingu við LinkedIn Talent Hub.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-108">A system administrator must complete setup tasks to enable integration with LinkedIn Talent Hub.</span></span> <span data-ttu-id="9ebc4-109">Fyrst þarf að setja upp notanda og öryggishlutverk í Power Apps umhverfinu til að veita LinkedIn Talent Hub viðeigandi heimildir til að skrifa gögn inn í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-109">First, in the Power Apps environment, you must set up a user and security role to grant LinkedIn Talent Hub the appropriate permissions to write data into Human Resources.</span></span>

### <a name="link-your-environment-to-linkedin-talent-hub"></a><span data-ttu-id="9ebc4-110">Tengja umhverfið við LinkedIn Talent Hub</span><span class="sxs-lookup"><span data-stu-id="9ebc4-110">Link your environment to LinkedIn Talent Hub</span></span>

1. <span data-ttu-id="9ebc4-111">Opnaðu [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).</span><span class="sxs-lookup"><span data-stu-id="9ebc4-111">Open [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).</span></span>

2. <span data-ttu-id="9ebc4-112">Í fellivalmynd notandans skal velja **Stillingar vöru**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-112">On the user drop-down menu, select **Product Settings**.</span></span>

3. <span data-ttu-id="9ebc4-113">Á yfirlitssvæðinu vinstra megin, í hlutanum **Ítarlegt**, skal velja **Samþættingar**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-113">In the left navigation pane, in the **Advanced** section, select **Integrations**.</span></span>

4. <span data-ttu-id="9ebc4-114">Veljið **Heimila** fyrir Microsoft Dynamics 365 Human Resources-samþættingu.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-114">Select **Authorize** for the Microsoft Dynamics 365 Human Resources integration.</span></span>

5. <span data-ttu-id="9ebc4-115">Á **Dynamics 365 Human Resources** síðunni skal velja umhverfið sem á að tengja LinkedIn Talent Hub við og síðan velja **Tengill**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-115">On the **Dynamics 365 Human Resources** page, select the environment to link LinkedIn Talent Hub to, and then select **Link**.</span></span>

    ![Innleiðing LinkedIn Talent Hub](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > <span data-ttu-id="9ebc4-117">Aðeins er hægt að tengja við umhverfi þar sem notandareikningurinn er með stjórendaaðgang að bæði umhverfi Human Resources og tengdu Power Apps-umhverfi.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-117">You can link only to environments where your user account has administrator access to both the Human Resources environment and the associated Power Apps environment.</span></span> <span data-ttu-id="9ebc4-118">Ef engin umhverfi eru skráð á síðu Human Resources skal ganga úr skugga um að þú sért með heimiluð umhverfi Human Resources í leigjandanum og að notandinn sem þú skráðir inn á tengda síðu sé með stjórnendaheimildir fyrir bæði umhverfi Human Resources og Power Apps-umhverfi.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-118">If no environments are listed on the Human Resources link page, make sure that you have licensed Human Resources environments on the tenant, and that the user that you signed in to the link page as has administrator permissions to both the Human Resources environment and the Power Apps environment.</span></span>

### <a name="create-a-power-apps-security-role"></a><span data-ttu-id="9ebc4-119">Stofna Power Apps öryggishlutverk</span><span class="sxs-lookup"><span data-stu-id="9ebc4-119">Create a Power Apps security role</span></span>

1. <span data-ttu-id="9ebc4-120">Opna [Power Platform stjórnendamiðstöð](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="9ebc4-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="9ebc4-121">Í listanum **Umhverfi** skal velja umhverfið sem tengist umhverfi Human Resources sem á að tengja við tilvikið af LinkedIn Talent Hub.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-121">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="9ebc4-122">Veldu **Stillingar**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-122">Select **Settings**.</span></span>

4. <span data-ttu-id="9ebc4-123">Stækkaðu hnútinn **Notendur + Heimildir** og veldu **Öryggishlutverk**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-123">Expand the **Users + Permissions** node, and select **Security Roles**.</span></span>

5. <span data-ttu-id="9ebc4-124">Á síðunni **Öryggishlutverk**, í tækjastikunni, skal velja **Nýtt hlutverk**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-124">On the **Security Roles** page, on the toolbar, select **New role**.</span></span>

6. <span data-ttu-id="9ebc4-125">Í flipanum **Upplýsingar** skal færa inn heiti fyrir hlutverkið, eins og **HRIS-samþætting LinkedIn Talent Hub**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-125">On the **Details** tab, enter a name for the role, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>

7. <span data-ttu-id="9ebc4-126">Í flipanum **Sérstilling** skal velja heimildina **Lesaðgangur** á fyrirtækisstigi fyrir eftirfarandi einingar:</span><span class="sxs-lookup"><span data-stu-id="9ebc4-126">On the **Customization** tab, select organization-level **Read** permission for the following entities:</span></span>

    - <span data-ttu-id="9ebc4-127">Eining</span><span class="sxs-lookup"><span data-stu-id="9ebc4-127">Entity</span></span>
    - <span data-ttu-id="9ebc4-128">Svæði</span><span class="sxs-lookup"><span data-stu-id="9ebc4-128">Field</span></span>
    - <span data-ttu-id="9ebc4-129">Skyldleiki</span><span class="sxs-lookup"><span data-stu-id="9ebc4-129">Relationship</span></span>

8. <span data-ttu-id="9ebc4-130">Vistið og lokið öryggishlutverkinu.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-130">Save and close the security role.</span></span>

### <a name="create-a-power-apps-application-user"></a><span data-ttu-id="9ebc4-131">Stofna notanda fyrir Power Apps-forrit</span><span class="sxs-lookup"><span data-stu-id="9ebc4-131">Create a Power Apps application user</span></span>

<span data-ttu-id="9ebc4-132">Notandi forritsins verður að vera stofnaður fyrir breyti LinkedIn Talent Hub til að veita breytinum heimildir til að skrifa færslur umsækjanda inn í Power Apps-umhverfið.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-132">An application user must be created for the LinkedIn Talent Hub adapter to grant permissions to the adapter to write candidate records into the Power Apps environment.</span></span>

1. <span data-ttu-id="9ebc4-133">Opna [Power Platform stjórnendamiðstöð](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="9ebc4-133">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="9ebc4-134">Í listanum **Umhverfi** skal velja umhverfið sem tengist umhverfi Human Resources sem á að tengja við tilvikið af LinkedIn Talent Hub.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-134">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="9ebc4-135">Veldu **Stillingar**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-135">Select **Settings**.</span></span>

4. <span data-ttu-id="9ebc4-136">Stækkaðu hnútinn **Notendur + Heimildir** og veldu **Notendur**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-136">Expand the **Users + Permissions** node, and select **Users**.</span></span>

5. <span data-ttu-id="9ebc4-137">Veljið **Stjórna notendum í Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-137">Select **Manage users in Dynamics 365**.</span></span>

6. <span data-ttu-id="9ebc4-138">Notið fellivalmyndina fyrir ofan listann til að breyta yfirlitinu úr sjálfgefnu yfirliti **Virkjaðir notendur** í **Forritsnotendur**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-138">Use the drop-down menu above the list to change the view from the default **Enabled Users** view to **Application Users**.</span></span>

    ![Yfirlit forritsnotenda](./media/hr-admin-integration-power-apps-application-users.jpg)

7. <span data-ttu-id="9ebc4-140">Á tækjastikunni skal velja **Nýr**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-140">On the toolbar, select **New**.</span></span>

8. <span data-ttu-id="9ebc4-141">Á síðunni **Nýr notandi** skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="9ebc4-141">On the **New user** page, follow these steps:</span></span>

    1. <span data-ttu-id="9ebc4-142">Breytið gildinu á reitnum **Gerð notanda** í **Forritsnotandi**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-142">Change the value of the **User type** field to **Application User**.</span></span>
    2. <span data-ttu-id="9ebc4-143">Stillið reitinn **Notandanafn** á **HRIS-samþætting HR LinkedIn Dynamics365**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-143">Set the **User Name** field to **Dynamics365 HR LinkedIn HRIS Integration**.</span></span>
    3. <span data-ttu-id="9ebc4-144">Stilltu reitinn **Forritskenni** á **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-144">Set the **Application ID** field to **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    4. <span data-ttu-id="9ebc4-145">Færið inn eitthvað gildi í reitina **Fornafn**, **Eftirnafn** og **Aðalnetfang**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-145">Enter any value in the **First Name**, **Last Name**, and **Primary Email** fields.</span></span>
    5. <span data-ttu-id="9ebc4-146">Á tækjastikunni skal velja **Vista \& Loka**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-146">On the toolbar, select **Save \& Close**.</span></span>

### <a name="assign-a-security-role-to-the-new-user"></a><span data-ttu-id="9ebc4-147">Öryggishlutverki úthlutað á nýjan notanda</span><span class="sxs-lookup"><span data-stu-id="9ebc4-147">Assign a security role to the new user</span></span>

<span data-ttu-id="9ebc4-148">Þegar búið er að vista og loka nýja forritsnotandanum í hlutanum hér að ofan er þér vísað aftur á síðuna **Listi yfir notendur**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-148">After you save and close the new application user in the previous section, you're returned to the **Users list** page.</span></span>

1. <span data-ttu-id="9ebc4-149">Á síðunni **Listi yfir notendur** skal breyta yfirlitinu í **Forritsnotendur**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-149">On the **Users list** page, change the view to **Application Users**.</span></span>

2. <span data-ttu-id="9ebc4-150">Veldu forritsnotandann sem þú stofnaðir í hlutanum hér á undan.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-150">Select the application user that you created in the previous section.</span></span>

3. <span data-ttu-id="9ebc4-151">Á tækjastikunni skal velja **Stjórna hlutverkum**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-151">On the toolbar, select **Manage Roles**.</span></span>

4. <span data-ttu-id="9ebc4-152">Veldu öryggishlutverkið sem þú stofnaðir fyrr í samþættingunni.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-152">Select the security role that you created earlier for the integration.</span></span>

5. <span data-ttu-id="9ebc4-153">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-153">Select **OK**.</span></span>

### <a name="add-an-azure-active-directory-app-in-human-resources"></a><span data-ttu-id="9ebc4-154">Bæta Azure Active Directory-forriti við Human Resources</span><span class="sxs-lookup"><span data-stu-id="9ebc4-154">Add an Azure Active Directory app in Human Resources</span></span>

1. <span data-ttu-id="9ebc4-155">Í Dynamics 365 Human Resources skal opna síðuna **Azure Active Directory forrit**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-155">In Dynamics 365 Human Resources, open the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="9ebc4-156">Bættu nýrri færslu við listann og stilltu eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="9ebc4-156">Add a new record to the list, and set the following fields:</span></span>

    - <span data-ttu-id="9ebc4-157">**Biðlarakenni**: Sláðu inn **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-157">**Client ID**: Enter **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    - <span data-ttu-id="9ebc4-158">**Heiti**: Sláðu inn heiti á Power Apps öryggishlutverkinu sem þú stofnaður hér á undan, t.d. **Samþætting LinkedIn Talent Hub HRIS**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-158">**Name**: Enter the name of the Power Apps security role that you created earlier, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>
    - <span data-ttu-id="9ebc4-159">**Notandakenni**: Velja skal notanda sem er með heimildir til að skrifa gögn inn í starfsmannastjórnun.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-159">**User ID**: Select a user who has permissions to write data in Personnel Management.</span></span>

### <a name="create-the-entity-in-common-data-service"></a><span data-ttu-id="9ebc4-160">Búa til eininguna í Common Data Service</span><span class="sxs-lookup"><span data-stu-id="9ebc4-160">Create the entity in Common Data Service</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9ebc4-161">Samþættingin við LinkedIn Talent Hub veltur á sýndareiningum í Common Data Service fyrir Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-161">The integration with LinkedIn Talent Hub depends on virtual entities in Common Data Service for Human Resources.</span></span> <span data-ttu-id="9ebc4-162">Sem skilyrði fyrir þessu skrefi í uppsetningunni, verður þú að skilgreina sýndareiningar.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-162">As a prerequisite for this step in the setup, you must configure virtual entities.</span></span> <span data-ttu-id="9ebc4-163">Upplýsingar um hvernig á að skilgreina sýndareiningar er að finna í [Skilgreina Common Data Service sýndareiningar](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span><span class="sxs-lookup"><span data-stu-id="9ebc4-163">For information about how to configure virtual entities, see [Configure Common Data Service virtual entities](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span></span>

1. <span data-ttu-id="9ebc4-164">Í Human Resources skal opna síðuna **Common Data Service (CDS)-samþætting**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-164">In Human Resources, open the **Common Data Service (CDS) integration** page.</span></span>

2. <span data-ttu-id="9ebc4-165">Veldu flipann **Sýndareiningar**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-165">Select the **Virtual entities** tab.</span></span>

3. <span data-ttu-id="9ebc4-166">Síaðu einingalistann eftir einingarmerki til að finna **Útfluttan umsækjanda LinkedIn**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-166">Filter the entity list by entity label to find **LinkedIn exported candidate**.</span></span>

4. <span data-ttu-id="9ebc4-167">Veldu eininguna og síðan **Búa til/uppfæra**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-167">Select the entity, and then select **Generate/refresh**.</span></span>

## <a name="exporting-candidate-records"></a><span data-ttu-id="9ebc4-168">Skrár umsækjanda fluttar út</span><span class="sxs-lookup"><span data-stu-id="9ebc4-168">Exporting candidate records</span></span>

<span data-ttu-id="9ebc4-169">Þegar uppsetningu er lokið geta ráðningaraðilar og starfsfólk Human Resources notað virknina **Flytja út HRIS** í LinkedIn Talent Hub til að flytja út færslur ráðinna umsækjenda úr LinkedIn Talent Hub í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-169">After the setup is completed, recruiters and Human resources (HR) professionals can use the **Export to HRIS** function in LinkedIn Talent Hub to export hired candidate records from LinkedIn Talent Hub to Human Resources.</span></span>

### <a name="export-records-from-linkedin-talent-hub"></a><span data-ttu-id="9ebc4-170">Flytja út færslur úr LinkedIn Talent Hub</span><span class="sxs-lookup"><span data-stu-id="9ebc4-170">Export records from LinkedIn Talent Hub</span></span>

<span data-ttu-id="9ebc4-171">Þegar umsækjandi hefur farið í gegnum ráðningarferlið og hefur verið ráðinn, geturðu flutt út skrár umsækjanda úr LinkedIn Talent Hub í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-171">After a candidate has moved through the recruiting process and has been hired, you can export the candidate record from LinkedIn Talent Hub to Human Resources.</span></span>

1. <span data-ttu-id="9ebc4-172">Í LinkedIn Talent Hub skal opna verkið sem þú réðst nýja starfsmanninn í.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-172">In LinkedIn Talent Hub, open the project that you hired the new employee for.</span></span>

2. <span data-ttu-id="9ebc4-173">Veldu skrá umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-173">Select a candidate record.</span></span>

3. <span data-ttu-id="9ebc4-174">Veldu **Breyta stigi** og síðan **Ráðinn**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-174">Select **Change stage**, and then select **Hired**.</span></span>

4. <span data-ttu-id="9ebc4-175">Í úrfellingarmerki (**...**) fyrir umsækjandann skal velja **Flytja yfir í HRIS**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-175">On the ellipsis menu (**...**) for the candidate, select **Export to HRIS**.</span></span>

5. <span data-ttu-id="9ebc4-176">Á svæðinu **Flytja yfir í HRIS** skal færa inn upplýsingarnar sem þarf að flytja út:</span><span class="sxs-lookup"><span data-stu-id="9ebc4-176">In the **Export to HRIS** pane, enter the information that must be exported:</span></span>

    - <span data-ttu-id="9ebc4-177">Í reitnum **HRIS-veitandi** skal velja **Microsoft Dynamics 365 Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-177">In the **HRIS provider** field, select **Microsoft Dynamics 365 Human Resources**.</span></span>
    - <span data-ttu-id="9ebc4-178">Í reitnum **Upphafsdagsetning** skal velja gildi fyrir nýja starfsmanninn.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-178">In the **Start date** field, select a value for the new employee.</span></span>
    - <span data-ttu-id="9ebc4-179">Í reitinn **Starfsheiti** skal færa inn starfsheiti fyrir vinnu nýja starfsmannsins.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-179">In the **Job title** field, enter a job title for the new employee's job.</span></span>
    - <span data-ttu-id="9ebc4-180">Í reitinn **Staðsetning** skal færa inn staðsetninguna þar sem starfsmaðurinn verður.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-180">In the **Location** field, enter the location where the employee will be based.</span></span>
    - <span data-ttu-id="9ebc4-181">Færðu inn eða staðfestu netfang starfsmannsins.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-181">Enter or verify the employee's email address.</span></span>

![Flytja yfir á HRIS-svæðið í LinkedIn Talent Hub](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a><span data-ttu-id="9ebc4-183">Ljúka við innleiðingu í Human Resources</span><span class="sxs-lookup"><span data-stu-id="9ebc4-183">Complete onboarding in Human Resources</span></span>

<span data-ttu-id="9ebc4-184">Færslur umsækjanda sem eru fluttar úr LinkedIn Talent Hub í Human Resources birtast í hlutanum **Umsækjendur til að ráða** á síðunni **Starfsmannastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-184">Candidate records that are exported from LinkedIn Talent Hub to Human Resources appear in the **Candidates to hire** section of the **Personnel management** page.</span></span>

1. <span data-ttu-id="9ebc4-185">Í Human Resources skal opna síðuna **Starfsmannastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-185">In Human Resources, open the **Personnel management** page.</span></span>

2. <span data-ttu-id="9ebc4-186">Í hlutanum **Umsækjendur til að ráða** skal velja **Ráða** fyrir valinn umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-186">In the **Candidates to hire** section, select **Hire** for the selected candidate.</span></span>

3. <span data-ttu-id="9ebc4-187">Í svarglugganum **Ráða nýjan starfsmann** skal fara yfir færsluna og bæta við nauðsynlegum upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-187">In the **Hire new worker** dialog box, review the record, and add any required information.</span></span> <span data-ttu-id="9ebc4-188">Einnig er hægt að velja staðsetningarnúmerið sem umsækjandinn hefur verið ráðinn fyrir.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-188">You can also select the position number that the candidate has been hired for.</span></span>

<span data-ttu-id="9ebc4-189">Þegar búið er að færa inn nauðsynlegar upplýsingar er hægt að halda áfram með hefðbundin ferli til að búa til starfsmannafærslur og starfsmannaráðningar.</span><span class="sxs-lookup"><span data-stu-id="9ebc4-189">After the required information has been entered, you can continue with your standard processes for creating employee records and onboarding employees.</span></span>

<span data-ttu-id="9ebc4-190">Eftirfarandi upplýsingar eru fluttar inn og teknar með í nýju starfsmannafærsluna:</span><span class="sxs-lookup"><span data-stu-id="9ebc4-190">The following details are imported and included on the new employee record:</span></span>

- <span data-ttu-id="9ebc4-191">Fornafn</span><span class="sxs-lookup"><span data-stu-id="9ebc4-191">First name</span></span>
- <span data-ttu-id="9ebc4-192">Eftirnafn</span><span class="sxs-lookup"><span data-stu-id="9ebc4-192">Last name</span></span>
- <span data-ttu-id="9ebc4-193">Upphafsdagur starfs</span><span class="sxs-lookup"><span data-stu-id="9ebc4-193">Employment start date</span></span>
- <span data-ttu-id="9ebc4-194">Tölvupóstfang</span><span class="sxs-lookup"><span data-stu-id="9ebc4-194">Email address</span></span>
- <span data-ttu-id="9ebc4-195">Símanúmer</span><span class="sxs-lookup"><span data-stu-id="9ebc4-195">Phone number</span></span>

## <a name="see-also"></a><span data-ttu-id="9ebc4-196">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="9ebc4-196">See also</span></span>

[<span data-ttu-id="9ebc4-197">Skilgreina Common Data Service sýndareiningar</span><span class="sxs-lookup"><span data-stu-id="9ebc4-197">Configure Common Data Service virtual entities</span></span>](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="9ebc4-198">Hvað er Common Data Service?</span><span class="sxs-lookup"><span data-stu-id="9ebc4-198">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)
