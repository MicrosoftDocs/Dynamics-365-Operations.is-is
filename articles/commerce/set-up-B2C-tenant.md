---
title: Setja upp B2C-leigjanda í Commerce
description: Þetta efni lýsir því hvernig á að setja upp þitt Azure Active Directory (Azure AD) leigjendur fyrirtækja til neytenda (B2C) til að auðkenna notendasíðu í Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: 68e72bc17005c11f28f572114357f906098cc045
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993345"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a><span data-ttu-id="6e797-103">Setja upp B2C-leigjanda í Commerce</span><span class="sxs-lookup"><span data-stu-id="6e797-103">Set up a B2C tenant in Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6e797-104">Þetta efni lýsir því hvernig á að setja upp þitt Azure Active Directory (Azure AD) leigjendur fyrirtækja til neytenda (B2C) til að auðkenna notendasíðu í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6e797-104">This topic describes how to set up your Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants for user site authentication in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6e797-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="6e797-105">Overview</span></span>

<span data-ttu-id="6e797-106">Dynamics 365 Commerce notar Azure AD B2C til að styðja persónuskilríki notenda og staðfesting.</span><span class="sxs-lookup"><span data-stu-id="6e797-106">Dynamics 365 Commerce uses Azure AD B2C to support user credential and authentication flows.</span></span> <span data-ttu-id="6e797-107">Notandi getur skráð sig, skráð sig inn og endurstillt lykilorð sitt í gegnum þessa flæði.</span><span class="sxs-lookup"><span data-stu-id="6e797-107">A user can sign up, sign in, and reset their password through these flows.</span></span> <span data-ttu-id="6e797-108">Azure AD B2C geymir viðkvæmar sannvottunarupplýsingar notanda, svo sem notandanafn og lykilorð.</span><span class="sxs-lookup"><span data-stu-id="6e797-108">Azure AD B2C stores sensitive user authentication information, such as username and password.</span></span> <span data-ttu-id="6e797-109">Notendaskráin í leigjanda B2C mun geyma annað hvort skrá yfir B2C staðbundna reikninga eða skrá yfir fyrirtækjasamfélag B2C.</span><span class="sxs-lookup"><span data-stu-id="6e797-109">The user record in the B2C tenant will store either a B2C local account record or a B2C social identity provider record.</span></span> <span data-ttu-id="6e797-110">Þessar B2C skrár munu tengjast aftur viðskiptamannaskránni í Commerce-umhverfi.</span><span class="sxs-lookup"><span data-stu-id="6e797-110">These B2C records will link back to the customer record in the Commerce environment.</span></span>

## <a name="create-or-link-to-an-existing-aad-b2c-tenant-in-the-azure-portal"></a><span data-ttu-id="6e797-111">Búðu til eða tengdu fyrirliggjandi AAD B2C leigjanda í Azure-gáttinni</span><span class="sxs-lookup"><span data-stu-id="6e797-111">Create or link to an existing AAD B2C tenant in the Azure portal</span></span>

1. <span data-ttu-id="6e797-112">Skráðu þig inn á [Azure-gáttina](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="6e797-112">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="6e797-113">Úr Azure-vefsíðugáttinni velurðu **Stofna tilföng**.</span><span class="sxs-lookup"><span data-stu-id="6e797-113">From the Azure portal menu, select **Create a resource**.</span></span> <span data-ttu-id="6e797-114">Athugaðu að nota áskriftina og skrána sem verða tengd Commerce-umhverfi þínu.</span><span class="sxs-lookup"><span data-stu-id="6e797-114">Be sure to use the subscription and directory that will be connected with your Commerce environment.</span></span>

    ![Búðu til tilföng í Azure Portal](./media/B2CImage_1.png)

1. <span data-ttu-id="6e797-116">Farðu í **Auðkenni \> Azure Active Directory B2C**.</span><span class="sxs-lookup"><span data-stu-id="6e797-116">Go to **Identity \> Azure Active Directory B2C**.</span></span>
1. <span data-ttu-id="6e797-117">Þegar þú ert á síðunni **Stofna nýjan B2C leigjanda eða tengil á núverandi leigjanda** notarðu einn af valkostunum hér að neðan sem best hentar þörfum fyrirtækisins þíns:</span><span class="sxs-lookup"><span data-stu-id="6e797-117">Once on the **Create New B2C Tenant or Link to existing Tenant** page, use one of the options below that best suits your company's needs:</span></span>

    - <span data-ttu-id="6e797-118">**Stofna nýjan Azure AD B2C leigjandi**: Notaðu þennan valkost til að búa til nýjan AAD B2C leigjanda.</span><span class="sxs-lookup"><span data-stu-id="6e797-118">**Create a new Azure AD B2C Tenant**: Use this option to create a new AAD B2C tenant.</span></span>
        1. <span data-ttu-id="6e797-119">Veldu **Stofna nýjan Azure AD B2C-leigjanda**.</span><span class="sxs-lookup"><span data-stu-id="6e797-119">Select **Create a new Azure AD B2C Tenant**.</span></span>
        1. <span data-ttu-id="6e797-120">Undir **Heiti fyrirtækisins** slærðu inn heiti fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="6e797-120">Under **Organization name**, enter the organization name.</span></span>
        1. <span data-ttu-id="6e797-121">Undir **Upphaflegt lén** slærðu inn upphaflegt lén.</span><span class="sxs-lookup"><span data-stu-id="6e797-121">Under **Initial domain name**, enter the initial domain name.</span></span>
        1. <span data-ttu-id="6e797-122">Fyrir **Land eða svæði** velurðu landið eða svæðið.</span><span class="sxs-lookup"><span data-stu-id="6e797-122">For **Country or region**, select the country or region.</span></span>
        1. <span data-ttu-id="6e797-123">Veldu **Stofna** til að stofna leigjanda.</span><span class="sxs-lookup"><span data-stu-id="6e797-123">Select **Create** to create the tenant.</span></span>

     ![Stofna nýjan Azure AD-leigjanda](./media/B2CImage_2.png)

     - <span data-ttu-id="6e797-125">**Tengja fyrirliggjandi Azure AD B2C leigjandi við Azure áskriftina mína**: Notaðu þennan valkost ef þú ert þegar með Azure AD B2C leigjanda sem þú vilt tengjast.</span><span class="sxs-lookup"><span data-stu-id="6e797-125">**Link an existing Azure AD B2C Tenant to my Azure subscription**: Use this option if you already have an Azure AD B2C tenant you want to link to.</span></span>
        1. <span data-ttu-id="6e797-126">Veldu **Tengja núverandi Azure AD B2C leigjandi við Azure áskriftina mína**.</span><span class="sxs-lookup"><span data-stu-id="6e797-126">Select **Link an existing Azure AD B2C Tenant to my Azure subscription**.</span></span>
        1. <span data-ttu-id="6e797-127">Fyrir **Azure AD B2C leigjandi**, veldu viðeigandi B2C leigjanda.</span><span class="sxs-lookup"><span data-stu-id="6e797-127">For **Azure AD B2C Tenant**, select the appropriate B2C tenant.</span></span> <span data-ttu-id="6e797-128">Ef skilaboðin „Engir hæfir B2C leigjendur fundust“ birtast í valröðinni, þá ert þú ekki með núverandi gjaldgengan B2C leigjanda og verður að búa til nýjan.</span><span class="sxs-lookup"><span data-stu-id="6e797-128">If the message "No eligible B2C Tenants found" appears in the selection box, you do not have an existing eligible B2C tenant and will need to create a new one.</span></span>
        1. <span data-ttu-id="6e797-129">Fyrir **Tilfangaflokkur**, veldu **Stofna nýtt**.</span><span class="sxs-lookup"><span data-stu-id="6e797-129">For **Resource group**, select **Create new**.</span></span> <span data-ttu-id="6e797-130">Sláðu inn **Heiti** fyrir tilfangaflokkinn sem mun innihalda leigjandann, veldu **Staðsetning tilfangaflokks** og veldu síðan **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="6e797-130">Enter a **Name** for the resource group that will contain the tenant, select the **Resource group location**, and then select **Create**.</span></span>

    ![Tengja núverandi Azure AD B2C leigjandi við Azure áskrift](./media/B2CImage_3.png)

1. <span data-ttu-id="6e797-132">Þegar nýja Azure AD B2C skráin er búin til (þetta getur tekið smá stund), tengill á nýju skráasafnið birtist á yfirlitinu.</span><span class="sxs-lookup"><span data-stu-id="6e797-132">Once the new Azure AD B2C directory is created (this may take a few moments), a link to the new directory will appear on the dashboard.</span></span> <span data-ttu-id="6e797-133">Þessi hlekkur mun vísa þér á síðuna „Velkomin/n í Azure Active Directory B2C“.</span><span class="sxs-lookup"><span data-stu-id="6e797-133">This link will direct you to the "Welcome to Azure Active Directory B2C" page.</span></span>

    ![Hlekkur á nýja AAD skrá](./media/B2CImage_4.png)

> [!NOTE]
> <span data-ttu-id="6e797-135">Ef þú ert með margar áskriftir á Azure reikningnum þínum eða hefur sett upp leigjanda B2C án þess að tengjast virkri áskrift mun borði með **Úrræðaleit** vísa þér til að tengja leigjanda við áskrift.</span><span class="sxs-lookup"><span data-stu-id="6e797-135">If you have multiple subscriptions within your Azure account or have set up the B2C tenant without linking to an active subscription, a **Troubleshoot** banner will direct you to link the tenant to a subscription.</span></span> <span data-ttu-id="6e797-136">Veldu úrræðaleit og fylgdu leiðbeiningunum til að leysa áskriftarmálið.</span><span class="sxs-lookup"><span data-stu-id="6e797-136">Select the troubleshooting message and follow the instructions to resolve the subscription issue.</span></span>

<span data-ttu-id="6e797-137">Eftirfarandi mynd sýnir dæmi um borða með Azure AD B2C **Úrræðaleit**.</span><span class="sxs-lookup"><span data-stu-id="6e797-137">The following image shows an example of an Azure AD B2C **Troubleshoot** banner.</span></span>

![Viðvörun sem sýnir skráarsafn hefur enga virka áskrift](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a><span data-ttu-id="6e797-139">Stofna B2C forrit</span><span class="sxs-lookup"><span data-stu-id="6e797-139">Create the B2C application</span></span>

<span data-ttu-id="6e797-140">Þegar B2C leigjandinn hefur verið stofnaður muntu búa til B2C forrit innan leigjandans til að hafa samskipti við aðgerðir Commerce.</span><span class="sxs-lookup"><span data-stu-id="6e797-140">Once the B2C tenant has been created, you will create a B2C application within the tenant to interact with the Commerce actions.</span></span>

<span data-ttu-id="6e797-141">Til að stofna B2C forrit skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="6e797-141">To create the B2C application, follow these steps.</span></span>

1. <span data-ttu-id="6e797-142">Í Azure-gáttinni skal velja **Applications(Legacy)** og síðan velja **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="6e797-142">In the Azure portal, select **Applications(Legacy)** and then select **Add**.</span></span>
1. <span data-ttu-id="6e797-143">Undir **Heiti** slærðu inn heiti viðeigandi AAD B2C forrits.</span><span class="sxs-lookup"><span data-stu-id="6e797-143">Under **Name**, enter the name of the desired AAD B2C application.</span></span>
1. <span data-ttu-id="6e797-144">Undir **Vefforrit/Vef-API**, fyrir **Hafa vefforrit með/vef-API**, veldu **Já**.</span><span class="sxs-lookup"><span data-stu-id="6e797-144">Under **Web App/Web API**, for **Include web app / web API**, select **Yes**.</span></span>
1. <span data-ttu-id="6e797-145">Fyrir **Leyfa óbeint flæði**, veldu **Já** (sjálfgefið gildi).</span><span class="sxs-lookup"><span data-stu-id="6e797-145">For **Allow implicit flow**, select **Yes** (the default value).</span></span>
1. <span data-ttu-id="6e797-146">Undir **Svarslóð**, sláðu inn sérstakar svarslóðir þínar.</span><span class="sxs-lookup"><span data-stu-id="6e797-146">Under **Reply URL**, enter your dedicated reply URLs.</span></span> <span data-ttu-id="6e797-147">Sjáðu [Svarslóðir](#reply-urls) hér að neðan til að fá upplýsingar um svarslóðir og hvernig eigi að forsníða þær hér.</span><span class="sxs-lookup"><span data-stu-id="6e797-147">See [Reply URLs](#reply-urls) below for information on reply URLs and how to format them here.</span></span>
1. <span data-ttu-id="6e797-148">Fyrir **Hafa native-bliðara með**, veldu **Nei** (sjálfgefið gildi).</span><span class="sxs-lookup"><span data-stu-id="6e797-148">For **Include native client**, select **No** (the default value).</span></span>
1. <span data-ttu-id="6e797-149">Velja **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="6e797-149">Select **Create**.</span></span>

### <a name="reply-urls"></a><span data-ttu-id="6e797-150">Svarslóðir</span><span class="sxs-lookup"><span data-stu-id="6e797-150">Reply URLs</span></span>

<span data-ttu-id="6e797-151">Svarvefslóðir eru mikilvægar þar sem þær gefa upp heimildarlista skilalén þegar vefsvæðið kallar á Azure AD B2C til að sannvotta notanda.</span><span class="sxs-lookup"><span data-stu-id="6e797-151">Reply URLs are important as they provide an allow list of the return domains when your site calls Azure AD B2C to authenticate a user.</span></span> <span data-ttu-id="6e797-152">Þetta heimilar endursendingu staðfests notanda til baka á lén sem hann er að skrá sig inn á (vefsvæðið þitt).</span><span class="sxs-lookup"><span data-stu-id="6e797-152">This permits the return of the authenticated user back to the domain from which they are signing into (your site domain).</span></span> 

<span data-ttu-id="6e797-153">Í reitnum **Svarslóð** á skjánum **Azure AD B2c - Forrit \> Nýtt forrit** þarftu að bæta við aðskildum línum fyrir bæði lén vefsvæðisins og (þegar umhverfi þitt er útvegað) Commerce-myndaðri vefslóðinni.</span><span class="sxs-lookup"><span data-stu-id="6e797-153">In the **Reply URL** box on the **Azure AD B2c - Applications \> New application** screen, you need to add separate lines for both your site domain and (once your environment is provisioned) the Commerce-generated URL.</span></span> <span data-ttu-id="6e797-154">Þessar vefslóðir verða alltaf að nota gilt slóðarsnið og verða að vera eingöngu grunnslóðir (engin skástrik eða slóðir fyrir aftan).</span><span class="sxs-lookup"><span data-stu-id="6e797-154">These URLs must always use a valid URL format and must be base URLs only (no trailing forward slashes or paths).</span></span> <span data-ttu-id="6e797-155">Strengurinn ``/_msdyn365/authresp`` þarf síðan að vera bætt aftan við grunnslóðina, eins og í eftirfarandi dæmum.</span><span class="sxs-lookup"><span data-stu-id="6e797-155">The string ``/_msdyn365/authresp`` then needs to be appended to the base URLs, as in the following examples.</span></span>

- <span data-ttu-id="6e797-156">``https://www.fabrikam.com/_msdyn365/authresp`` (Lénið ætti að passa fullkomlega við lén rafrænna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="6e797-156">``https://www.fabrikam.com/_msdyn365/authresp`` (The domain should match the e-commerce domain completely.</span></span> <span data-ttu-id="6e797-157">Ef um er að ræða mörg lén þarf að bæta við þessari vefslóð fyrir hvert lén.)</span><span class="sxs-lookup"><span data-stu-id="6e797-157">If you have multiple domains, you need to add this URL for each domain.)</span></span>
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="create-user-flow-policies"></a><span data-ttu-id="6e797-158">Stofna notandaflæðisstefnu</span><span class="sxs-lookup"><span data-stu-id="6e797-158">Create user flow policies</span></span>

<span data-ttu-id="6e797-159">Notendastreymi eru reglurnar sem Azure AD B2C notar til að bjóða upp á örugga innskráningu, skráningu, breyta prófíl og gleyma aðgangsorðum notenda.</span><span class="sxs-lookup"><span data-stu-id="6e797-159">User flows are the policies Azure AD B2C uses to provide secure sign in, sign up, edit profile, and forget password user experiences.</span></span> <span data-ttu-id="6e797-160">Dynamics 365 Commerce notar þessi flæði til að framkvæma stefnuaðgerðir til að hafa samskipti við Azure AD B2C leigjanda.</span><span class="sxs-lookup"><span data-stu-id="6e797-160">Dynamics 365 Commerce uses these flows to perform the policy actions to interact with the Azure AD B2C tenant.</span></span> <span data-ttu-id="6e797-161">Þegar notandi hefur samskipti við þessar reglur er honum vísað í Azure AD B2C-leigjanda til að framkvæma aðgerðirnar.</span><span class="sxs-lookup"><span data-stu-id="6e797-161">When a user interacts with these policies, they are redirected to the Azure AD B2C tenant to perform the actions.</span></span>

<span data-ttu-id="6e797-162">Azure AD B2C býður upp á þrjár gerðir af grunnflæðum notenda:</span><span class="sxs-lookup"><span data-stu-id="6e797-162">Azure AD B2C provides three basic user flow types:</span></span>
- <span data-ttu-id="6e797-163">Skráðu þig og skráðu þig inn</span><span class="sxs-lookup"><span data-stu-id="6e797-163">Sign up and sign in</span></span>
- <span data-ttu-id="6e797-164">Forstillingum breytt</span><span class="sxs-lookup"><span data-stu-id="6e797-164">Profile editing</span></span>
- <span data-ttu-id="6e797-165">Aðgangsorð endurstillt</span><span class="sxs-lookup"><span data-stu-id="6e797-165">Password reset</span></span>

<span data-ttu-id="6e797-166">Þú getur valið að nota sjálfgefna flæði notenda frá Azure AD, sem birtir síðu sem hýst er af AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="6e797-166">You can choose to use the default user flows provided by Azure AD, which will display a page hosted by AAD B2C.</span></span> <span data-ttu-id="6e797-167">Að öðrum kosti geturðu búið til HTML síðu til að stjórna útliti og viðmóti þessara reynsluflæði notenda.</span><span class="sxs-lookup"><span data-stu-id="6e797-167">Alternately, you can create an HTML page to control the look and feel of these user flow experiences.</span></span> 

<span data-ttu-id="6e797-168">Til að sérsníða stefnusíður notenda fyrir Dynamics 365 Commerce, sjáðu [Setja upp sérsniðnar síður fyrir notendanafn](custom-pages-user-logins.md).</span><span class="sxs-lookup"><span data-stu-id="6e797-168">To customize the user policy pages for Dynamics 365 Commerce, see [Set up custom pages for user logins](custom-pages-user-logins.md).</span></span> <span data-ttu-id="6e797-169">Sjá frekari upplýsingar í [Sérsniðið viðmót notendaupplifana í Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span><span class="sxs-lookup"><span data-stu-id="6e797-169">For additional information, see [Customize the interface of user experiences in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span></span>

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a><span data-ttu-id="6e797-170">Búðu til skráningu og skráðu þig inn í notendaflæðisstefnu</span><span class="sxs-lookup"><span data-stu-id="6e797-170">Create a sign up and sign in user flow policy</span></span>

<span data-ttu-id="6e797-171">Til að stofna innskráningu og skrá inn notendaflæðisstefnu skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="6e797-171">To create a sign up and sign in user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="6e797-172">Veldu í Azure-gáttinni **Notendastreymi (reglur)** í vinstri glugganum.</span><span class="sxs-lookup"><span data-stu-id="6e797-172">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="6e797-173">Á síðunni **Azure AD B2C - Notendastreymi (reglur)** velurðu **Nýtt notendaflæði**.</span><span class="sxs-lookup"><span data-stu-id="6e797-173">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="6e797-174">Á flipanum **Ráðlagt**, velurðu **Skráðu þig og skráðu þig inn**.</span><span class="sxs-lookup"><span data-stu-id="6e797-174">On the **Recommended** tab, select **Sign up and sign in**.</span></span>
1. <span data-ttu-id="6e797-175">Undir **Heiti** slærðu inn heiti stefnu.</span><span class="sxs-lookup"><span data-stu-id="6e797-175">Under **Name**, enter a policy name.</span></span> <span data-ttu-id="6e797-176">Þetta nafn mun birtast á eftir með forskeyti sem vefsíðan úthlutar (til dæmis „B2C_1_“).</span><span class="sxs-lookup"><span data-stu-id="6e797-176">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="6e797-177">Undir **Kennisveitendur**, veldu viðeigandi gátreit.</span><span class="sxs-lookup"><span data-stu-id="6e797-177">Under **Identity providers**, select the appropriate check box.</span></span>
1. <span data-ttu-id="6e797-178">Undir **Fjölþættri sannvottun**, veldu viðeigandi val fyrir þitt fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="6e797-178">Under **Multifactor Authentication**, select the appropriate choice for your company.</span></span> 
1. <span data-ttu-id="6e797-179">Undir **Eiginleikar og kröfur notanda**, veldu valkosti til að safna eiginleikum eða skila kröfum eftir því sem við á.</span><span class="sxs-lookup"><span data-stu-id="6e797-179">Under **User attributes and claims**, select options to collect attributes or return claims as appropriate.</span></span> <span data-ttu-id="6e797-180">Commerce krefst eftirfarandi sjálfgefinna valkosta:</span><span class="sxs-lookup"><span data-stu-id="6e797-180">Commerce requires the following default options:</span></span>

    | <span data-ttu-id="6e797-181">**Innheimtueigind**</span><span class="sxs-lookup"><span data-stu-id="6e797-181">**Collect  attribute**</span></span> | <span data-ttu-id="6e797-182">**Skila kröfu**</span><span class="sxs-lookup"><span data-stu-id="6e797-182">**Return  claim**</span></span> |
    | ---------------------- | ----------------- |
    | <span data-ttu-id="6e797-183">Tölvupóstfang</span><span class="sxs-lookup"><span data-stu-id="6e797-183">Email Address</span></span>          | <span data-ttu-id="6e797-184">Netföng</span><span class="sxs-lookup"><span data-stu-id="6e797-184">Email Addresses</span></span>   |
    | <span data-ttu-id="6e797-185">Fornafn</span><span class="sxs-lookup"><span data-stu-id="6e797-185">Given Name</span></span>             | <span data-ttu-id="6e797-186">Fornafn</span><span class="sxs-lookup"><span data-stu-id="6e797-186">Given Name</span></span>        |
    |                        | <span data-ttu-id="6e797-187">Auðkennisveitandi</span><span class="sxs-lookup"><span data-stu-id="6e797-187">Identity Provider</span></span> |
    | <span data-ttu-id="6e797-188">Eftirnafn</span><span class="sxs-lookup"><span data-stu-id="6e797-188">Surname</span></span>                | <span data-ttu-id="6e797-189">Eftirnafn</span><span class="sxs-lookup"><span data-stu-id="6e797-189">Surname</span></span>           |
    |                        | <span data-ttu-id="6e797-190">ObjectId notanda</span><span class="sxs-lookup"><span data-stu-id="6e797-190">User’s Object ID</span></span>  |

1. <span data-ttu-id="6e797-191">Velja **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="6e797-191">Select **Create**.</span></span>

<span data-ttu-id="6e797-192">Eftirfarandi mynd er dæmi um Azure AD B2C skráningu og innskráningu í notendaflæði.</span><span class="sxs-lookup"><span data-stu-id="6e797-192">The following image is an example of the Azure AD B2C sign up and sign in user flow.</span></span>

![Stefnustillingar skráningar og innskráningar](./media/B2CImage_11.png)

<span data-ttu-id="6e797-194">Eftirfarandi mynd sýnir valkostinn **Keyra notendaflæði** í Azure AD B2C skráningu og innskráningu í notendaflæði.</span><span class="sxs-lookup"><span data-stu-id="6e797-194">The following image shows the **Run user flow** option in the Azure AD B2C sign up and sign in user flow.</span></span>

![Keyra valkost notendaflæðis í stefnuflæði](./media/B2CImage_23.png)
   
### <a name="create-a-profile-editing-user-flow-policy"></a><span data-ttu-id="6e797-196">Búðu til forstillingum breytt fyrir notendaflæði</span><span class="sxs-lookup"><span data-stu-id="6e797-196">Create a profile editing user flow policy</span></span>

<span data-ttu-id="6e797-197">Til að stofna notendaflæðisreglu forstillingabreytinga skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="6e797-197">To create a profile editing user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="6e797-198">Veldu í Azure-gáttinni **Notendastreymi (reglur)** í vinstri glugganum.</span><span class="sxs-lookup"><span data-stu-id="6e797-198">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="6e797-199">Á síðunni **Azure AD B2C - Notendastreymi (reglur)** velurðu **Nýtt notendaflæði**.</span><span class="sxs-lookup"><span data-stu-id="6e797-199">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="6e797-200">Á flipanum **Ráðlagt** velurðu **Forstillingum breytt**.</span><span class="sxs-lookup"><span data-stu-id="6e797-200">On the **Recommended** tab, select **Profile editing**.</span></span>
1. <span data-ttu-id="6e797-201">Undir **Heiti**, sláðu inn notendaflæði forstillingabreytingar.</span><span class="sxs-lookup"><span data-stu-id="6e797-201">Under **Name**, enter the profile editing user flow.</span></span> <span data-ttu-id="6e797-202">Þetta nafn mun birtast á eftir með forskeyti sem vefsíðan úthlutar (til dæmis „B2C_1_“).</span><span class="sxs-lookup"><span data-stu-id="6e797-202">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="6e797-203">Undir **Kennisveitendur**, veldu **Innskráning á staðbundinn reikning**.</span><span class="sxs-lookup"><span data-stu-id="6e797-203">Under **Identity providers**, select **Local Account SignIn**.</span></span>
1. <span data-ttu-id="6e797-204">Undir **Eiginleikar notanda** skal velja eftirfarandi gátreiti:</span><span class="sxs-lookup"><span data-stu-id="6e797-204">Under **User attributes**, select the following check boxes:</span></span>
    - <span data-ttu-id="6e797-205">**Netföng** (aðeins **Skilakrafa**)</span><span class="sxs-lookup"><span data-stu-id="6e797-205">**Email Addresses** (**Return claim** only)</span></span>
    - <span data-ttu-id="6e797-206">**Fornafn** (**Innheimtueigind** og **Skila kröfu**)</span><span class="sxs-lookup"><span data-stu-id="6e797-206">**Given Name** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="6e797-207">**Kennisveitandi** (aðeins **Skilakrafa**)</span><span class="sxs-lookup"><span data-stu-id="6e797-207">**Identity Provider** (**Return claim** only)</span></span>
    - <span data-ttu-id="6e797-208">**Eftirnafn** (**Innheimtueigind** og **Skilakrafa**)</span><span class="sxs-lookup"><span data-stu-id="6e797-208">**Surname** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="6e797-209">**ObjectId notanda** (aðeins **Skilakrafa**)</span><span class="sxs-lookup"><span data-stu-id="6e797-209">**User's Object ID** (**Return claim** only)</span></span>
1. <span data-ttu-id="6e797-210">Velja **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="6e797-210">Select **Create**.</span></span>

<span data-ttu-id="6e797-211">Eftirfarandi mynd sýnir dæmi um Azure AD B2C notendaflæði forstillingabreytingar.</span><span class="sxs-lookup"><span data-stu-id="6e797-211">The following image shows an example of the Azure AD B2C profile editing user flow.</span></span>

![Stofna notendaflæðið Forstillingum breytt](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a><span data-ttu-id="6e797-213">Stofna notendaflæðisreglu endurstillingar aðgangsorðs</span><span class="sxs-lookup"><span data-stu-id="6e797-213">Create a password reset user flow policy</span></span>

<span data-ttu-id="6e797-214">Til að stofna notendaflæðisreglu endurstillingar aðgangsorðs skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="6e797-214">To create a password reset user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="6e797-215">Veldu í Azure-gáttinni **Notendastreymi (reglur)** í vinstri glugganum.</span><span class="sxs-lookup"><span data-stu-id="6e797-215">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="6e797-216">Á síðunni **Azure AD B2C - Notendastreymi (reglur)** velurðu **Nýtt notendaflæði**.</span><span class="sxs-lookup"><span data-stu-id="6e797-216">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="6e797-217">Á flipanum **Ráðlagt** velurðu **Aðgangsorð endurstillt**.</span><span class="sxs-lookup"><span data-stu-id="6e797-217">On the **Recommended** tab, select **Password Reset**.</span></span>
1. <span data-ttu-id="6e797-218">Undir **Heiti**, slærðu inn heiti fyrir notandastreymi aðgangsorðs með lykilorði.</span><span class="sxs-lookup"><span data-stu-id="6e797-218">Under **Name**, enter a name for the password reset user flow.</span></span>
1. <span data-ttu-id="6e797-219">Undir **Kennisveitendur** velurðu **Endurstilla aðgangsorð með netfangi**.</span><span class="sxs-lookup"><span data-stu-id="6e797-219">Under **Identity providers**, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="6e797-220">Velja **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="6e797-220">Select **Create**.</span></span>
1. <span data-ttu-id="6e797-221">Undir **Forritskröfur** skal velja eftirfarandi gátreiti:</span><span class="sxs-lookup"><span data-stu-id="6e797-221">Under **Application claims**, select the following check boxes:</span></span>
    - <span data-ttu-id="6e797-222">**Netföng**</span><span class="sxs-lookup"><span data-stu-id="6e797-222">**Email addresses**</span></span>
    - <span data-ttu-id="6e797-223">**Fornafn**</span><span class="sxs-lookup"><span data-stu-id="6e797-223">**Given Name**</span></span>
    - <span data-ttu-id="6e797-224">**Eftirnafn**</span><span class="sxs-lookup"><span data-stu-id="6e797-224">**Surname**</span></span>
    - <span data-ttu-id="6e797-225">**ObjectId notanda**</span><span class="sxs-lookup"><span data-stu-id="6e797-225">**User's Object ID**</span></span>
1. <span data-ttu-id="6e797-226">Velja **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="6e797-226">Select **Create**.</span></span>

<span data-ttu-id="6e797-227">Eftirfarandi mynd sýnir hvar á að stilla **Núllstilla lykilorð með póstfangi** í Azure AD B2C lykilorð endurstillir notendaflæði.</span><span class="sxs-lookup"><span data-stu-id="6e797-227">The following image shows where to set **Reset Password using mail address** in the Azure AD B2C password reset user flow.</span></span>

![Stilltu „Núllstilla lykilorð með póstfangi“ í stefnu um endurstillingu lykilorðs](./media/B2CImage_13.png)

## <a name="add-social-identity-providers-optional"></a><span data-ttu-id="6e797-229">Bæta við kennitöluveitendum (valfrjálst)</span><span class="sxs-lookup"><span data-stu-id="6e797-229">Add social identity providers (Optional)</span></span>

<span data-ttu-id="6e797-230">Kennitöluveitendur leyfa notendum að nota samfélagsreikninga sína til staðfestingar.</span><span class="sxs-lookup"><span data-stu-id="6e797-230">Social identity providers allow users to use their social accounts for authentication.</span></span> <span data-ttu-id="6e797-231">Valfrjálst er að bæta við sannvottun fyrir kennisveitanda í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6e797-231">Adding social identity provider authentication is optional in Dynamics 365 Commerce.</span></span> 

<span data-ttu-id="6e797-232">Ef staðfesting á kennitöluveitanda er ekki bætt við er sjálfgefið að Azure AD B2C forstillingar verði aðalforstillingar fyrir notandagrunn þinn.</span><span class="sxs-lookup"><span data-stu-id="6e797-232">If social identity provider authentication is not added, the default Azure AD B2C profiles will be the main profiles for your user base.</span></span> <span data-ttu-id="6e797-233">Notendur munu velja eigið notandanafn (valin netföng) og setja lykilorð.</span><span class="sxs-lookup"><span data-stu-id="6e797-233">Users will select their own username (their preferred email address) and set a password.</span></span> <span data-ttu-id="6e797-234">Azure AD B2C staðfestir notendur beint.</span><span class="sxs-lookup"><span data-stu-id="6e797-234">Azure AD B2C will authenticate users directly.</span></span> 

<span data-ttu-id="6e797-235">Ef staðfesting á kennitöluveitanda bætist við og notandi velur einn af þeim kennitöluveitendum sem eru í boði er eining samt stofnuð í Azure AD B2C leigjandi.</span><span class="sxs-lookup"><span data-stu-id="6e797-235">If social identity provider authentication is added and a user chooses one of the social identity providers offered, an entity is still created in the Azure AD B2C tenant.</span></span> <span data-ttu-id="6e797-236">Azure AD B2C mun síðan staðfesta persónuskilríki notandans hjá kennitöluveitanda.</span><span class="sxs-lookup"><span data-stu-id="6e797-236">Azure AD B2C will then authenticate the user's credentials with the social identity provider.</span></span>

> [!NOTE]
> <span data-ttu-id="6e797-237">Innskráning kennisveitanda stofnar skrá í B2C leigjandanum, en á öðru sniði en staðbundnir reikningar þar sem það mun kalla tilvísun ytri kennitöluveitanda til staðfestingar.</span><span class="sxs-lookup"><span data-stu-id="6e797-237">The identity provider sign in creates a record in the B2C tenant, but in a different format than local accounts since it will call the external social identity provider reference for authentication.</span></span> <span data-ttu-id="6e797-238">Notandinn getur notað sama netfang á milli kennitöluveitenda, sem þýðir að notandanafn tölvupóstsins sem notað er til sannvottunar er hugsanlega ekki einkvæmt fyrir leigjanda.</span><span class="sxs-lookup"><span data-stu-id="6e797-238">The user can use the same email address across social identity providers, meaning that the email username used for authentication may not be unique to the tenant.</span></span> <span data-ttu-id="6e797-239">Azure AD B2C mun einungis framfylgja því að notendur hafi einkvæmt netfang á B2C reikningum.</span><span class="sxs-lookup"><span data-stu-id="6e797-239">Azure AD B2C will only enforce that users have a unique email address on local B2C accounts.</span></span>

<span data-ttu-id="6e797-240">Áður en þú getur bætt við kennitöluveitanda til að staðfesta, verður þú að fara í gátt kennisveitanda og setja upp umsókn um kennisveitanda samkvæmt leiðbeiningunum í Azure AD B2C skjöl.</span><span class="sxs-lookup"><span data-stu-id="6e797-240">Before you can add a social identity provider for authentication, you must go to the identity provider's portal and set up an identity provider application as instructed in the Azure AD B2C documentation.</span></span> <span data-ttu-id="6e797-241">Hér fyrir neðan er listi yfir tengla á fylgiskjölin.</span><span class="sxs-lookup"><span data-stu-id="6e797-241">A list of links to the documentation is provided below.</span></span>

- [<span data-ttu-id="6e797-242">Amazon</span><span class="sxs-lookup"><span data-stu-id="6e797-242">Amazon</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [<span data-ttu-id="6e797-243">Azure AD (Stakur leigjandi)</span><span class="sxs-lookup"><span data-stu-id="6e797-243">Azure AD (Single Tenant)</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [<span data-ttu-id="6e797-244">Microsoft-reikningur</span><span class="sxs-lookup"><span data-stu-id="6e797-244">Microsoft Account</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [<span data-ttu-id="6e797-245">Facebook</span><span class="sxs-lookup"><span data-stu-id="6e797-245">Facebook</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [<span data-ttu-id="6e797-246">GitHub</span><span class="sxs-lookup"><span data-stu-id="6e797-246">GitHub</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [<span data-ttu-id="6e797-247">Google</span><span class="sxs-lookup"><span data-stu-id="6e797-247">Google</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [<span data-ttu-id="6e797-248">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="6e797-248">LinkedIn</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [<span data-ttu-id="6e797-249">OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="6e797-249">OpenID Connect</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [<span data-ttu-id="6e797-250">Twitter</span><span class="sxs-lookup"><span data-stu-id="6e797-250">Twitter</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a><span data-ttu-id="6e797-251">Bættu við og settu upp kennisveitanda</span><span class="sxs-lookup"><span data-stu-id="6e797-251">Add and set up a social identity provider</span></span>

<span data-ttu-id="6e797-252">Fylgdu þessum skrefum til að bæta við og setja upp kennisveitanda.</span><span class="sxs-lookup"><span data-stu-id="6e797-252">To add and set up a social identity provider, follow these steps.</span></span>  

1. <span data-ttu-id="6e797-253">Farðu á Azure gáttina **Persónuaðilum**.</span><span class="sxs-lookup"><span data-stu-id="6e797-253">In the Azure portal, navigate to **Identity Providers**.</span></span>
1. <span data-ttu-id="6e797-254">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="6e797-254">Select **Add**.</span></span> <span data-ttu-id="6e797-255">Skjárinn **Bæta við kennisveitanda** birtist.</span><span class="sxs-lookup"><span data-stu-id="6e797-255">The **Add identity provider** screen appears.</span></span>
1. <span data-ttu-id="6e797-256">Undir **Heiti**, slærðu inn nafnið sem á að birtast notendum á innskráningarskjánum.</span><span class="sxs-lookup"><span data-stu-id="6e797-256">Under **Name**, enter the name to be displayed to users on your sign in screen.</span></span>
1. <span data-ttu-id="6e797-257">Undir **Gerð auðkennisveitanda**, veldu auðkennisveitanda af listanum.</span><span class="sxs-lookup"><span data-stu-id="6e797-257">Under **Identity provider type**, select an identity provider from the list.</span></span>
1. <span data-ttu-id="6e797-258">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6e797-258">Select **OK**.</span></span>
1. <span data-ttu-id="6e797-259">Veldu **Setja þennan kennisveitanda upp** til að fá aðgang að skjánum **Setja upp kennisveitanda**.</span><span class="sxs-lookup"><span data-stu-id="6e797-259">Select **Set up this identity provider** to access the **Set up the social identity provider** screen.</span></span>
1. <span data-ttu-id="6e797-260">Undir **Biðlarakenni**, sláðu inn biðlarakennið eins og það er fengið úr forritsuppsetningu kennisveitandans.</span><span class="sxs-lookup"><span data-stu-id="6e797-260">Under **Client ID**, enter the client ID as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="6e797-261">Undir **Leynilykill biðlara**, sláðu inn leynilykill biðlara eins og það er fengið úr forritsuppsetningu kennisveitandans.</span><span class="sxs-lookup"><span data-stu-id="6e797-261">Under **Client secret**, enter the client secret as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="6e797-262">Festu notendaflæði fyrir innskráningarreglur við innskráningu:</span><span class="sxs-lookup"><span data-stu-id="6e797-262">Attach user flow for sign in sign up policies:</span></span>
1. <span data-ttu-id="6e797-263">Fara til **Azure AD B2C - Notendastreymi (reglur) \> {innskráningarstefna þín fyrir innskráningu} \> Kennisveitendur**.</span><span class="sxs-lookup"><span data-stu-id="6e797-263">Go to **Azure AD B2C – User flows (policies) \> {your sign-in sign-up policy} \> Identity providers**.</span></span>
1. <span data-ttu-id="6e797-264">Til að festa notendaflæðisstefnu fyrir skráningu/innskráningu velurðu alla kennisveitendur sem þú hefur sett upp fyrir reikninginn.</span><span class="sxs-lookup"><span data-stu-id="6e797-264">To attach the sign in/sign up user flow policy, select each identity provider you have set up for your account.</span></span> <span data-ttu-id="6e797-265">Til að prófa þetta velurðu **Keyra notendaflæði** fyrir hvern kennisveitanda.</span><span class="sxs-lookup"><span data-stu-id="6e797-265">To test these, select **Run user flow** for each identity provider.</span></span> <span data-ttu-id="6e797-266">Nýr flipi sýnir innskráningarsíðuna sem sýnir nýjan valkassa fyrir kennisveitanda.</span><span class="sxs-lookup"><span data-stu-id="6e797-266">A new tab will display the sign-in page displaying the new identity provider selection box.</span></span>

<span data-ttu-id="6e797-267">Eftirfarandi mynd sýnir dæmi um skjáina **Bæta við kennisveitanda** og **Setja upp kennitöluveitanda** í Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="6e797-267">The following image shows examples of the **Add identity provider** and **Set up the social identity provider** screens in Azure AD B2C.</span></span>

![Að bæta við kennitöluveitanda fyrir forritið](./media/B2CImage_14.png)

<span data-ttu-id="6e797-269">Eftirfarandi mynd sýnir dæmi um hvernig eigi að velja kennisveitendur á síðunni Azure AD B2C **Kennisveitendur**.</span><span class="sxs-lookup"><span data-stu-id="6e797-269">The following image shows an example of how to select identity providers on the Azure AD B2C **Identity Providers** page.</span></span>

![Veldu hvern félagslegan auðkennisaðila til að gera kleift að nota fyrir stefnu þína](./media/B2CImage_16.png)

<span data-ttu-id="6e797-271">Eftirfarandi mynd sýnir dæmi um sjálfgefinn innskráningarskjá með innskráningarhnappi fyrir kennitöluveitanda sýndan.</span><span class="sxs-lookup"><span data-stu-id="6e797-271">The following image shows an example of a default sign-in screen with a social identity provider sign-in button displayed.</span></span>

![Dæmi um sjálfgefinn innskráningarskjá með innskráningarhnappi fyrir kennitöluveitanda sýndan](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a><span data-ttu-id="6e797-273">Uppfærðu höfuðstöðvar verslunar með nýju Azure AD B2C upplýsingum</span><span class="sxs-lookup"><span data-stu-id="6e797-273">Update Commerce headquarters with the new Azure AD B2C information</span></span>

<span data-ttu-id="6e797-274">Þegar Azure AD B2C úthlutunarskrefum hér að ofan er lokið verður Azure AD B2C umsókn að vera skráð á þitt Dynamics 365 Commerce umhverfi.</span><span class="sxs-lookup"><span data-stu-id="6e797-274">Once the Azure AD B2C provisioning steps above are completed, the Azure AD B2C application must be registered in your Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="6e797-275">Til að uppfæra höfuðstöðvar með nýjum Azure AD B2C upplýsingum, fylgdu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="6e797-275">To update headquarters with the new Azure AD B2C information, follow these steps.</span></span>

1. <span data-ttu-id="6e797-276">Farðu í **Samnýttar færibreytur Commerce** og veldu **Kennisveitendur** í vinstri valmyndinni.</span><span class="sxs-lookup"><span data-stu-id="6e797-276">In Commerce, go to **Commerce Shared Parameters** and select **Identity Providers** in the left menu.</span></span>
1. <span data-ttu-id="6e797-277">Undir **Kennisveitendur** gerirðu eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="6e797-277">Under **Identity Providers**, do the following:</span></span>
    1. <span data-ttu-id="6e797-278">Í reitinn **Útgefandi** slærðu inn vefslóð útgefanda kennisveitanda.</span><span class="sxs-lookup"><span data-stu-id="6e797-278">In the **Issuer** box, enter the identity provider issuer URL.</span></span> <span data-ttu-id="6e797-279">Til að finna slóð útgefanda skal sjá [Fá slóð útgefanda](#obtain-issuer-url) hér að neðan.</span><span class="sxs-lookup"><span data-stu-id="6e797-279">To find your issuer URL, see [Obtain issuer URL](#obtain-issuer-url) below.</span></span>
    1. <span data-ttu-id="6e797-280">Í reitinn **Heiti** skal færa inn heiti fyrir útgefendaskrána.</span><span class="sxs-lookup"><span data-stu-id="6e797-280">In the **Name** box, enter a name for your issuer record.</span></span>
    1. <span data-ttu-id="6e797-281">Í reitnum **Gerð** slærðu inn **Azure AD B2C (id_token)**.</span><span class="sxs-lookup"><span data-stu-id="6e797-281">In the **Type** box, enter **Azure AD B2C (id_token)**.</span></span>
1. <span data-ttu-id="6e797-282">Undir **Treystandi aðilar**, með valinn hlut B2C kennisveitanda hér að ofan, gerðu eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="6e797-282">Under **Relying Parties**, with the above B2C identity provider item selected, do the following:</span></span>
    1. <span data-ttu-id="6e797-283">Í reitinn **ClientID** slærðu inn B2C forritsauðkenni þitt.</span><span class="sxs-lookup"><span data-stu-id="6e797-283">In the **ClientID** box, enter your B2C application ID.</span></span> <span data-ttu-id="6e797-284">Þú getur fundið þetta í reitnum **Kenni forrits** á eiginleikasíðu B2C forritsins.</span><span class="sxs-lookup"><span data-stu-id="6e797-284">You can find this in the **Application ID** box of your B2C application's properties page.</span></span>
    1. <span data-ttu-id="6e797-285">Í reitnum **Gerð** slærðu inn **Opinbert**.</span><span class="sxs-lookup"><span data-stu-id="6e797-285">In the **Type** box, enter **Public**.</span></span>
    1. <span data-ttu-id="6e797-286">Í reitnum **Notandagerð** slærðu inn **Viðskiptavinur**.</span><span class="sxs-lookup"><span data-stu-id="6e797-286">In the **User Type** box, enter **Customer**.</span></span>
1. <span data-ttu-id="6e797-287">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="6e797-287">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="6e797-288">Í leitarreit Commerce leitarðu að **Dreifingaráætlun**</span><span class="sxs-lookup"><span data-stu-id="6e797-288">In the Commerce search box, search for **Distribution schedule**</span></span>
1. <span data-ttu-id="6e797-289">Í vinstri valmyndinni á síðunni **Dreifingaráætlanir** velurðu vinnsluna **1110 altæk stilling**.</span><span class="sxs-lookup"><span data-stu-id="6e797-289">In the left navigation menu of the **Distribution schedules** page, select job **1110 Global configuration**.</span></span>
1. <span data-ttu-id="6e797-290">Í aðgerðarúðunni skal velja **Keyra núna**.</span><span class="sxs-lookup"><span data-stu-id="6e797-290">On the action pane, select **Run Now**.</span></span>

### <a name="obtain-issuer-url"></a><span data-ttu-id="6e797-291">Fá slóð útgefanda</span><span class="sxs-lookup"><span data-stu-id="6e797-291">Obtain issuer URL</span></span>

<span data-ttu-id="6e797-292">Fylgdu þessum skrefum til að fá vefslóð útgefanda kennisveitanda.</span><span class="sxs-lookup"><span data-stu-id="6e797-292">To obtain your identity provider issuer URL, follow these steps.</span></span>

1. <span data-ttu-id="6e797-293">Búðu til veffang lýsigagna á eftirfarandi sniði með B2C leigjanda þínum og stefnu: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span><span class="sxs-lookup"><span data-stu-id="6e797-293">Create a metadata address URL in the following format using your B2C tenant and policy: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span></span>
    - <span data-ttu-id="6e797-294">Dæmi: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span><span class="sxs-lookup"><span data-stu-id="6e797-294">Example: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span></span>
1. <span data-ttu-id="6e797-295">Sláðu inn veffang lýsigagna í veffangastiku vafrans.</span><span class="sxs-lookup"><span data-stu-id="6e797-295">Enter the metadata address URL into a browser address bar.</span></span>
1. <span data-ttu-id="6e797-296">Í lýsigögnum, afritarðu veffang útgefanda kennisveitanda (gildið fyrir **"útgefandi"**).</span><span class="sxs-lookup"><span data-stu-id="6e797-296">In the metadata, copy the identity provider issuer URL (the value for **"issuer"**).</span></span>
    - <span data-ttu-id="6e797-297">Dæmi: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span><span class="sxs-lookup"><span data-stu-id="6e797-297">Example: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span></span>

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a><span data-ttu-id="6e797-298">Stilla B2C leigjanda þinn í Commerce vefsvæðishönnuði</span><span class="sxs-lookup"><span data-stu-id="6e797-298">Configure your B2C tenant in Commerce site builder</span></span>

<span data-ttu-id="6e797-299">Þegar uppsetningu á Azure AD B2C leigjandi er lokið, þú verður að stilla B2C leigjanda í vefsvæðishönnuði Commerce.</span><span class="sxs-lookup"><span data-stu-id="6e797-299">Once setup of your Azure AD B2C tenant is completed, you must configure the B2C tenant in Commerce site builder.</span></span> <span data-ttu-id="6e797-300">Stillingarþrepin fela í sér að safna upplýsingum um B2C umsóknir úr Azure-gáttinni, færa þær B2C forritaupplýsingar inn í vefsvæðishönnuð og tengja síðan B2C forritið við vefsvæðið og rás.</span><span class="sxs-lookup"><span data-stu-id="6e797-300">Configuration steps include collecting B2C application information from the Azure portal, entering that B2C application information into site builder, and then associating the B2C application with your site and channel.</span></span>

### <a name="collect-the-required-application-information"></a><span data-ttu-id="6e797-301">Safnaðu nauðsynlegum upplýsingum um forritið</span><span class="sxs-lookup"><span data-stu-id="6e797-301">Collect the required application information</span></span>

<span data-ttu-id="6e797-302">Fylgdu þessum skrefum til að safna nauðsynlegum forritsupplýsingum.</span><span class="sxs-lookup"><span data-stu-id="6e797-302">To collect the required application information, follow these steps.</span></span>

1. <span data-ttu-id="6e797-303">Í Azure gáttinni ferðu í **Heim \> Azure AD B2C - Forrit**.</span><span class="sxs-lookup"><span data-stu-id="6e797-303">In the Azure portal, go to **Home \> Azure AD B2C - Applications**.</span></span>
1. <span data-ttu-id="6e797-304">Veldu forritið þitt og veldu síðan í vinstri glugganum **Eiginleikar** til að fá upplýsingar um forritið.</span><span class="sxs-lookup"><span data-stu-id="6e797-304">Select your application, and then in the left navigation pane select **Properties** to obtain the application details.</span></span>
1. <span data-ttu-id="6e797-305">Úr reitnum **Kenni forrits**, safnaðu forritskenni B2C forritsins sem búið var til í B2C leigjanda þínum.</span><span class="sxs-lookup"><span data-stu-id="6e797-305">From the **Application ID** box, collect the application ID of the B2C application created in your B2C tenant.</span></span> <span data-ttu-id="6e797-306">Þetta verður síðar fært inn sem **GUID biðlara** í vefsvæðishönnuði.</span><span class="sxs-lookup"><span data-stu-id="6e797-306">This will later be entered as the **Client GUID** in site builder.</span></span>
1. <span data-ttu-id="6e797-307">Undir **Svarslóðinni**, safnarðu svarslóðum.</span><span class="sxs-lookup"><span data-stu-id="6e797-307">Under **Reply URL**, collect the reply URL.</span></span>
1. <span data-ttu-id="6e797-308">Farðu í **Heim \> Azure AD B2C - Notendastreymi (reglur)**, og safnaðu síðan nöfnum hverrar notendastreymisstefnu.</span><span class="sxs-lookup"><span data-stu-id="6e797-308">Go to **Home \> Azure AD B2C – User flows (policies)**, and then collect the names of each user flow policy.</span></span>

<span data-ttu-id="6e797-309">Eftirfarandi mynd sýnir dæmi um síðuna **Azure AD B2C - Forrit**.</span><span class="sxs-lookup"><span data-stu-id="6e797-309">The following image shows an example of the **Azure AD B2C - Applications** page.</span></span>

![Farðu í B2C forritið í leigjanda þínum](./media/B2CImage_19.png)

<span data-ttu-id="6e797-311">Eftirfarandi mynd sýnir dæmi um forritasíðuna **Eiginleikar** í Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="6e797-311">The following image shows an example of an application **Properties** page in Azure AD B2C.</span></span> 

![Afritaðu auðkenni forritsins úr eiginleikum B2C forritsins](./media/B2CImage_21.png)

<span data-ttu-id="6e797-313">Eftirfarandi mynd sýnir dæmi um reglur notendaflæðis á síðunni **Azure AD B2C - Notendastreymi (reglur)**.</span><span class="sxs-lookup"><span data-stu-id="6e797-313">The following image shows an example of user flow policies on the **Azure AD B2C – User flows (policies)** page.</span></span>

![Safnaðu heitum á hverju B2C stefnuflæði](./media/B2CImage_22.png)

### <a name="enter-your-aad-b2c-tenant-application-information-into-commerce"></a><span data-ttu-id="6e797-315">Sláðu inn forritsupplýsingar AAD B2C leigjanda inn í Commerce</span><span class="sxs-lookup"><span data-stu-id="6e797-315">Enter your AAD B2C tenant application information into Commerce</span></span>

<span data-ttu-id="6e797-316">Þú verður að slá inn upplýsingar um Azure AD B2C leigjandi í vefsvæðishönnuð Commerce áður en B2C leigjandi er tengdur við vefsvæðin þín.</span><span class="sxs-lookup"><span data-stu-id="6e797-316">You must enter details of the Azure AD B2C tenant into Commerce site builder before associating the B2C tenant with your site(s).</span></span>

<span data-ttu-id="6e797-317">Fylgdu þessum skrefum til að bæta forritsupplýsingum um AAD B2C leigjanda í Commerce.</span><span class="sxs-lookup"><span data-stu-id="6e797-317">To add your AAD B2C tenant application information to Commerce, follow these steps.</span></span>

1. <span data-ttu-id="6e797-318">Skráðu þig inn sem stjórnandi í vefsvæðishönnuði Commerce fyrir umhverfi þitt.</span><span class="sxs-lookup"><span data-stu-id="6e797-318">Sign in as an administrator to Commerce site builder for your environment.</span></span>
1. <span data-ttu-id="6e797-319">Í vinstri yfirlitsglugganum velurðu **Leigjandastillingar** til að stækka hann.</span><span class="sxs-lookup"><span data-stu-id="6e797-319">In the left navigation pane, select **Tenant Settings**  to expand it.</span></span>
1. <span data-ttu-id="6e797-320">Undir **Leigjandastillingar** velurðu **B2C stillinngar**.</span><span class="sxs-lookup"><span data-stu-id="6e797-320">Under **Tenant Settings**, select **B2C Settings**.</span></span> 
1. <span data-ttu-id="6e797-321">Í aðalglugganum við hliðina á **B2C forrit**, veldu **Stjórna**.</span><span class="sxs-lookup"><span data-stu-id="6e797-321">In the main window next **B2C Applications**, select **Manage**.</span></span> <span data-ttu-id="6e797-322">(Ef leigjandi þinn birtist í B2C forritalistanum var kerfisstjórinn þegar búinn að bæta honum við.</span><span class="sxs-lookup"><span data-stu-id="6e797-322">(If your tenant appears in the B2C Applications list, then it was already added by an administrator.</span></span> <span data-ttu-id="6e797-323">Staðfestu að hlutirnir í skrefi 6 hér að neðan samsvari B2C forritinu þínu.)</span><span class="sxs-lookup"><span data-stu-id="6e797-323">Verify that the items in step 6 below match your B2C Application.)</span></span>
1. <span data-ttu-id="6e797-324">Veljið **Bæta við B2C forriti**.</span><span class="sxs-lookup"><span data-stu-id="6e797-324">Select **Add B2C Application**.</span></span>
1. <span data-ttu-id="6e797-325">Sláðu inn eftirfarandi nauðsynlega hluti í glugganum sem birtist, með gildum úr B2C leigjanda þínum og forriti.</span><span class="sxs-lookup"><span data-stu-id="6e797-325">Enter the following required items in the form displayed, using values from your B2C tenant and application.</span></span> <span data-ttu-id="6e797-326">Reitir sem ekki er krafist (þeir sem eru án stjörnu) kunna að vera auðir.</span><span class="sxs-lookup"><span data-stu-id="6e797-326">Fields that are not required (those without an asterisk) may be left blank.</span></span>

    - <span data-ttu-id="6e797-327">**Heiti forrits**: Heiti B2C forritsins, til dæmis „Fabrikam B2C“.</span><span class="sxs-lookup"><span data-stu-id="6e797-327">**Application Name**: The name for your B2C Application, for example "Fabrikam B2C".</span></span>
    - <span data-ttu-id="6e797-328">**Nafn leigjanda**: Heiti B2C leigjanda (til dæmis er notað „fabrikam“ ef lénið birtist sem „fabrikam.onmicrosoft.com“ fyrir B2C leigjandann).</span><span class="sxs-lookup"><span data-stu-id="6e797-328">**Tenant Name**: The name of your B2C tenant (for example, use "fabrikam" if the domain appears as "fabrikam.onmicrosoft.com" for the B2C tenant).</span></span> 
    - <span data-ttu-id="6e797-329">**Gleymdu auðkenni lykilorðsstefnu**: Notandastraumur fyrir gleymt lykilorð notendastreymis, til dæmis „B2C_1_PasswordReset“.</span><span class="sxs-lookup"><span data-stu-id="6e797-329">**Forget Password Policy ID**: The forget password user flow policy ID, for example "B2C_1_PasswordReset".</span></span>
    - <span data-ttu-id="6e797-330">**Auðkenni kennsluskilríkja við innskráningu**: Auðkenni skráningar og innskráningarflæði notendastreymis, til dæmis „B2C_1_signup_signin“.</span><span class="sxs-lookup"><span data-stu-id="6e797-330">**Signup Signin Policy ID**: The sign up and sign in user flow policy ID, for example "B2C_1_signup_signin".</span></span>
    - <span data-ttu-id="6e797-331">**GUID biðlara**: Auðkenni B2C forritsins, til dæmis „22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6”.</span><span class="sxs-lookup"><span data-stu-id="6e797-331">**Client GUID**: The B2C application ID, for example "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".</span></span>
    - <span data-ttu-id="6e797-332">**Breyta auðkenni prófílstefnu**: Auðkenni sniðs sem breytir notendastreymi, til dæmis „B2C_1A_ProfileEdit“.</span><span class="sxs-lookup"><span data-stu-id="6e797-332">**Edit Profile Policy ID**: The profile editing user flow policy ID, for example "B2C_1A_ProfileEdit".</span></span>

1. <span data-ttu-id="6e797-333">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6e797-333">Select **OK**.</span></span> <span data-ttu-id="6e797-334">Þú ættir nú að sjá nafn B2C forritsins þíns birtast á listanum.</span><span class="sxs-lookup"><span data-stu-id="6e797-334">You should now see the name of your B2C application appear in the list.</span></span>
1. <span data-ttu-id="6e797-335">Veldu **Vista** til að vista breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="6e797-335">Select **Save** to save your changes.</span></span>

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a><span data-ttu-id="6e797-336">Tengdu B2C forritið við síðuna þína og rás</span><span class="sxs-lookup"><span data-stu-id="6e797-336">Associate the B2C application to your site and channel</span></span>

> [!WARNING]
> <span data-ttu-id="6e797-337">Ef vefsvæðið þitt er nú þegar tengt B2C forriti, með því að breyta í annað B2C forrit, verður að fjarlægja núverandi tilvísanir sem settar hafa verið upp fyrir notendur sem þegar hafa skráð sig í þessu umhverfi.</span><span class="sxs-lookup"><span data-stu-id="6e797-337">If your site is already associated with a B2C application, changing to a different B2C application will remove the current references established for users already signed up in this environment.</span></span> <span data-ttu-id="6e797-338">Ef það hefur breyst verða engin skilríki sem eru tengd B2C forritinu sem nú er úthlutað tiltæk fyrir notendur.</span><span class="sxs-lookup"><span data-stu-id="6e797-338">If changed, any credentials associated with the currently-assigned B2C application will not be available to users.</span></span> 
> 
> <span data-ttu-id="6e797-339">Uppfærðu aðeins B2C forritið ef þú ert að setja upp B2C forrit rásarinnar í fyrsta skipti eða ef þú ætlar að láta notendur skrá sig með nýjum skilríkjum á þessa rás með nýju B2C forritinu.</span><span class="sxs-lookup"><span data-stu-id="6e797-339">Only update the B2C application if you are setting up the channel's B2C application for the first time or if you intend to have users re-sign up with new credentials to this channel with the new B2C application.</span></span> <span data-ttu-id="6e797-340">Gætið varúðar þegar rásir eru tengdar við B2C forrit og nafnið forrit greinilega.</span><span class="sxs-lookup"><span data-stu-id="6e797-340">Take caution when associating channels to B2C applications, and name applications clearly.</span></span> <span data-ttu-id="6e797-341">Ef rás er ekki tengd B2C forriti í skrefunum hér að neðan verða notendur sem skrá sig inn á þá rás fyrir síðuna þína færðir inn í B2C forritið sem birtist sem **sjálfgefið** í listanum **Leigjandastillingar \> B2C stillingar** yfir B2C forrit.</span><span class="sxs-lookup"><span data-stu-id="6e797-341">If a channel is not associated to a B2C application in the steps below, users signing into that channel for your site will be entered into the B2C application showing as **default** in the **Tenant Settings \> B2C Settings** list of B2C applications.</span></span>

<span data-ttu-id="6e797-342">Til að tengja B2C forritið við síðuna þína og rás skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="6e797-342">To associate the B2C application to your site and channel, follow these steps.</span></span>

1. <span data-ttu-id="6e797-343">Farðu á vefsvæðið í vefsvæðishönnuði Commerce.</span><span class="sxs-lookup"><span data-stu-id="6e797-343">Navigate to your site in Commerce site builder.</span></span>
1. <span data-ttu-id="6e797-344">Í vinstri yfirlitsglugganum velurðu **Svæðisstillingar** til að stækka hann.</span><span class="sxs-lookup"><span data-stu-id="6e797-344">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="6e797-345">Undir **Vefsvæðisstillingar** velurðu **Rásir**.</span><span class="sxs-lookup"><span data-stu-id="6e797-345">Below **Site Settings**, select **Channels**.</span></span>
1. <span data-ttu-id="6e797-346">Í aðalglugganum undir **Rásir** velurðu rásina þína.</span><span class="sxs-lookup"><span data-stu-id="6e797-346">In the main window under **Channels**, select your channel.</span></span>
1. <span data-ttu-id="6e797-347">Veldu rásina fyrir rásina til hægri, veldu nafn B2C forritsins úr fellivalmyndinni **Velja B2C forrit**.</span><span class="sxs-lookup"><span data-stu-id="6e797-347">In the channel properties pane on the right, select your B2C application name from the **Select B2C Application** drop down menu.</span></span>
1. <span data-ttu-id="6e797-348">Veldu **Loka** og veldu síðan **Vista og birta**.</span><span class="sxs-lookup"><span data-stu-id="6e797-348">Select **Close**, and then select **Save and Publish**.</span></span>

## <a name="additional-b2c-information"></a><span data-ttu-id="6e797-349">Frekari B2C upplýsingar</span><span class="sxs-lookup"><span data-stu-id="6e797-349">Additional B2C information</span></span>

### <a name="customer-migration"></a><span data-ttu-id="6e797-350">Flutningur viðskiptavina</span><span class="sxs-lookup"><span data-stu-id="6e797-350">Customer migration</span></span>

<span data-ttu-id="6e797-351">Ef þú ert að íhuga að flytja skrár viðskiptavina frá fyrri vettvangi fyrir persónuskilaboð, vinsamlegast vinndu með Dynamics 365 Commerce teymi til að fara yfir fólksflutningaþörf þína.</span><span class="sxs-lookup"><span data-stu-id="6e797-351">If you are considering migrating customer records from a previous identity provider platform, please work with the Dynamics 365 Commerce team to review your customer migration needs.</span></span>

<span data-ttu-id="6e797-352">Fyrir aukaleg Azure AD B2C skjöl um flutning viðskiptavina, sjá [Flytja notendur til Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span><span class="sxs-lookup"><span data-stu-id="6e797-352">For additional Azure AD B2C documentation on customer migration, see [Migrate users to Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span></span>

### <a name="custom-policies"></a><span data-ttu-id="6e797-353">Sérsniðnar stefnur</span><span class="sxs-lookup"><span data-stu-id="6e797-353">Custom policies</span></span>

<span data-ttu-id="6e797-354">Fyrir frekari upplýsingar um sérsníða Azure AD B2C samskipti og stefnuflæði umfram það sem boðið er upp á við B2C stöðluðu stefnur, sjá [Sérsniðnar stefnur í Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span><span class="sxs-lookup"><span data-stu-id="6e797-354">For additional information regarding customizing Azure AD B2C interactions and policy flows beyond what is offered by B2C standard policies, see [Custom policies in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span></span> 

### <a name="secondary-admin"></a><span data-ttu-id="6e797-355">Annar stjórnandi</span><span class="sxs-lookup"><span data-stu-id="6e797-355">Secondary admin</span></span>

<span data-ttu-id="6e797-356">Hægt er að bæta við valfrjálsum aukaforritareikningi í hlutanum **Notendur** af B2C leigjanda þínum.</span><span class="sxs-lookup"><span data-stu-id="6e797-356">An optional, secondary administrator account can be added in the **Users** section of your B2C tenant.</span></span> <span data-ttu-id="6e797-357">Þetta getur verið beinn reikningur eða almennur reikningur.</span><span class="sxs-lookup"><span data-stu-id="6e797-357">This can be a direct account or a general account.</span></span> <span data-ttu-id="6e797-358">Ef þú þarft að deila reikningi þvert á teymi, þá er einnig hægt að stofna sameiginlegan reikning.</span><span class="sxs-lookup"><span data-stu-id="6e797-358">If you need to share an account across team resources, a common account can also be created.</span></span> <span data-ttu-id="6e797-359">Vegna næmni gagnanna sem geymd eru í Azure AD B2C, ætti að fylgjast náið með sameiginlegum reikningi samkvæmt öryggisvenjum fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="6e797-359">Due to the sensitivity of the data stored in Azure AD B2C, a common account should be monitored closely per your company's security practices.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6e797-360">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="6e797-360">Additional resources</span></span>

[<span data-ttu-id="6e797-361">Skilgreina lénsheiti</span><span class="sxs-lookup"><span data-stu-id="6e797-361">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="6e797-362">Uppsetning á nýjum leigjanda rafrænna viðskipta</span><span class="sxs-lookup"><span data-stu-id="6e797-362">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="6e797-363">Stofna svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="6e797-363">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="6e797-364">Tengja svæði Dynamics 365 Commerce við netrás</span><span class="sxs-lookup"><span data-stu-id="6e797-364">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="6e797-365">Vinna með skrárnar robots.txt</span><span class="sxs-lookup"><span data-stu-id="6e797-365">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

<span data-ttu-id="6e797-366">[Hlaða upp mörgum URL-framsendingum í einu](upload-bulk-redirects.md)Tengja svæði Dynamics 365 Commerce við netrás</span><span class="sxs-lookup"><span data-stu-id="6e797-366">[Upload URL redirects in bulk](upload-bulk-redirects.md)Associate a Dynamics 365 Commerce site with an online channel</span></span>

[<span data-ttu-id="6e797-367">Setja upp sérsniðnar síður fyrir innskráningu notenda</span><span class="sxs-lookup"><span data-stu-id="6e797-367">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="6e797-368">Skilgreina marga B2C-leigjendur í Commerce-umhverfi</span><span class="sxs-lookup"><span data-stu-id="6e797-368">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="6e797-369">Bæta við stuðningi fyrir efnisbirtingarnet (CDN)</span><span class="sxs-lookup"><span data-stu-id="6e797-369">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="6e797-370">Virkja greiningu á verslun eftir staðsetningu</span><span class="sxs-lookup"><span data-stu-id="6e797-370">Enable location-based store detection</span></span>](enable-store-detection.md)
