---
title: Setja upp sérsniðnar síður fyrir innskráningu notenda
description: Þetta efni lýsir því hvernig á að smíða sérsniðnar síður í Microsoft Dynamics 365 Commerce sem sjá um sérsniðnar innskráningar fyrir notendur Azure Active Directory (Azure AD) leigjendur fyrirtækja til neytenda (B2C).
author: brianshook
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a55da9683c43ac75109fd256e481b02a4d565914
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970079"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a><span data-ttu-id="2afc7-103">Setja upp sérsniðnar síður fyrir innskráningu notenda</span><span class="sxs-lookup"><span data-stu-id="2afc7-103">Set up custom pages for user sign-ins</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="2afc7-104">Þetta efni lýsir því hvernig á að smíða sérsniðnar síður í Microsoft Dynamics 365 Commerce sem sjá um sérsniðnar innskráningar fyrir notendur Azure Active Directory (Azure AD) leigjendur fyrirtækja til neytenda (B2C).</span><span class="sxs-lookup"><span data-stu-id="2afc7-104">This topic describes how to build custom pages in Microsoft Dynamics 365 Commerce that handle customized sign-ins for users of Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants.</span></span>

## <a name="overview"></a><span data-ttu-id="2afc7-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="2afc7-105">Overview</span></span>

<span data-ttu-id="2afc7-106">Til að nota sérsniðnar síður sem eru gerðar í Dynamics 365 Commerce til að takast á við innskráningarflæði notenda verður þú að setja upp Azure AD stefnu sem vísað verður til í viðskiptaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="2afc7-106">To use custom pages that are authored in Dynamics 365 Commerce to handle user sign-in flows, you must set up the Azure AD policies that will be referenced in the Commerce environment.</span></span> <span data-ttu-id="2afc7-107">Þú getur stillt „Skráning og innskráning“, „Forstillingum breytt“ og „Aðgangsorð endurstillt“ Azure AD B2C stefnur með því að nota Azure AD B2C forrit.</span><span class="sxs-lookup"><span data-stu-id="2afc7-107">You can configure the "Sign up and sign in," "Profile editing," and "Password reset" Azure AD B2C policies by using the Azure AD B2C application.</span></span> <span data-ttu-id="2afc7-108">Síðan er hægt að vísa til Azure AD B2C leigjanda og stefnuheita við útvegunarferlið sem er gert fyrir viðskiptaumhverfið með því að nota Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="2afc7-108">The Azure AD B2C tenant and policy names can then be referenced during the provisioning process that is done for the Commerce environment by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="2afc7-109">Hægt er að smíða sérsniðnar viðskiptasíður með því að nota innskráningu, skráningu, breytingu reikningssniðs eða endurstillingu lykilorðs.</span><span class="sxs-lookup"><span data-stu-id="2afc7-109">The custom Commerce pages can be built by using the sign in, sign up, account profile edit, or password reset module.</span></span> <span data-ttu-id="2afc7-110">Síðan ætti að vísa í vefslóðir síðunnar sem eru birtar fyrir þessar sérsniðnu síður Azure AD B2C stefnuskilgreiningar í Azure gáttinni.</span><span class="sxs-lookup"><span data-stu-id="2afc7-110">The page URLs that are published for these custom pages should then be referenced in Azure AD B2C policy configurations in the Azure portal.</span></span>

## <a name="set-up-b2c-policies"></a><span data-ttu-id="2afc7-111">Setja upp B2C reglur</span><span class="sxs-lookup"><span data-stu-id="2afc7-111">Set up B2C policies</span></span>

<span data-ttu-id="2afc7-112">Eftir að þú hefur sett upp þinn Azure AD B2C leigjanda og tengt hann við viðskiptaumhverfi þitt ferðu á síðuna **Azure AD B2C** í Azure gáttinni og síðan á valmyndinni undir **Stefnur** velurðu **Notendastreymi (reglur)**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-112">After you set up your Azure AD B2C tenant and associate it with your Commerce environment, go to the **Azure AD B2C** page in the Azure portal, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

![Skipunin Notandaflæði (stefna) í valmyndinni](./media/B2C_CustomPage_PoliciesMenu.png)

<span data-ttu-id="2afc7-114">Þú getur nú stillt innskráninguna "Skráðu þig inn og skráðu þig inn", "Prófíklippingu" og "Lykilorð endurstillt" innskráningarflæði notenda.</span><span class="sxs-lookup"><span data-stu-id="2afc7-114">You can now configure the "Sign up and sign in," "Profile editing," and "Password reset" user sign-in flows.</span></span>

### <a name="configure-the-sign-up-and-sign-in-policy"></a><span data-ttu-id="2afc7-115">Stilla stefnuna „Skráning og innskráning“</span><span class="sxs-lookup"><span data-stu-id="2afc7-115">Configure the "Sign up and sign in" policy</span></span>

<span data-ttu-id="2afc7-116">Fylgdu þessum skrefum til að stilla stefnuna „Skráning og innskráning“.</span><span class="sxs-lookup"><span data-stu-id="2afc7-116">To configure the "Sign up and sign in" policy, follow these steps.</span></span>

1. <span data-ttu-id="2afc7-117">Veldu **Nýtt notendaflæði** og síðan á flipanum **Ráðlagt** velurðu regluna **Skráning og innskráning**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-117">Select **New user flow**, and then, on the **Recommended** tab, select the **Sign up and sign in** policy.</span></span>
1. <span data-ttu-id="2afc7-118">Sláðu inn heiti fyrir regluna (t.d. **B2C\_1\_SignInSignUp**).</span><span class="sxs-lookup"><span data-stu-id="2afc7-118">Enter a name for the policy (for example, **B2C\_1\_SignInSignUp**).</span></span>
1. <span data-ttu-id="2afc7-119">Í hlutanum **Kennisveitendur** velurðu kennisveitendurna sem nota á fyrir regluna.</span><span class="sxs-lookup"><span data-stu-id="2afc7-119">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="2afc7-120">Að lágmarki verður **Innskráning í gegnum tölvupóst** að vera valin.</span><span class="sxs-lookup"><span data-stu-id="2afc7-120">At a minimum, **Email signup** must be selected.</span></span>
1. <span data-ttu-id="2afc7-121">Í dálkinn **Innheimtueigind** skaltu velja gátreitina fyrir **Netfang**, **Fornafn** og **Eftirnafn**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-121">In the **Collect attribute** column, select the check boxes for **Email Address**, **Given Name**, and **Surname**.</span></span>
1. <span data-ttu-id="2afc7-122">Í dálknum **Skilakrafa** skaltu velja gátreitina fyrir **Netföng**, **Fornafn**, **Kennisveitandi**, **Eftirnafn** og **Hlutakenni notanda**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-122">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>

    ![Eiginleikar og kröfur valdar](./media/B2C_SignInSignUp_Attributes.png)

1. <span data-ttu-id="2afc7-124">Velja skal **Í lagi** til að stofna regluna.</span><span class="sxs-lookup"><span data-stu-id="2afc7-124">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="2afc7-125">Tvísmelltu á nýja regluheitið og veldu síðan í yfirlitsglugganum **Eiginleikar**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-125">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="2afc7-126">Stilltu valkostinn **Virkja JavaScript til að framfylgja blaðsíðuútliti (forsskoðun)** á **Á**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-126">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

    ![Eiginleikasíða fyrir nýju regluna](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> <span data-ttu-id="2afc7-128">Vísað verður að fullu til heitis reglunnar í viðskiptaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="2afc7-128">The policy name will be fully referenced in the Commerce environment.</span></span> <span data-ttu-id="2afc7-129">(Forskeytið **B2C\_1\_** verður með í tilvísuninni.) Ekki er hægt að endurnefna reglur eftir að þær eru búnar til.</span><span class="sxs-lookup"><span data-stu-id="2afc7-129">(The **B2C\_1\_** prefix will be included in the reference.) Policies can't be renamed after they are created.</span></span> <span data-ttu-id="2afc7-130">Ef þú ert að skipta út núverandi reglu fyrir viðskiptaumhverfi þitt geturðu eytt upprunalegu reglunni og byggt upp nýja reglu með sama heiti.</span><span class="sxs-lookup"><span data-stu-id="2afc7-130">If you're replacing an existing policy for your Commerce environment, you can delete the original policy and build a new policy that has the same name.</span></span> <span data-ttu-id="2afc7-131">Að öðrum kosti, ef umhverfið hefur þegar verið útvegað, geturðu sent nýja regluheitið í gegnum þjónustubeiðni.</span><span class="sxs-lookup"><span data-stu-id="2afc7-131">Alternatively, if the environment has already been provisioned, you can submit the new policy name through a service request.</span></span>

<span data-ttu-id="2afc7-132">Þú munt fara aftur í þessa reglu til að klára uppsetninguna eftir að þú hefur smíðað sérsniðnar síður.</span><span class="sxs-lookup"><span data-stu-id="2afc7-132">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="2afc7-133">Lokaðu reglunni í bili til að fara aftur á síðuna **Notendastreymi (reglur)** á Azure gáttinni.</span><span class="sxs-lookup"><span data-stu-id="2afc7-133">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-profile-editing-policy"></a><span data-ttu-id="2afc7-134">Stilla regluna „Forstillingum breytt“</span><span class="sxs-lookup"><span data-stu-id="2afc7-134">Configure the "Profile editing" policy</span></span>

<span data-ttu-id="2afc7-135">Til að skilgreina regluna „Forstillingum breytt“ skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="2afc7-135">To configure the "Profile editing" policy, follow these steps.</span></span>

1. <span data-ttu-id="2afc7-136">Veldu **Nýtt notendaflæði** og síðan á flipanum **Ráðlagt** velurðu regluna **Forstillingum breytt**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-136">Select **New user flow**, and then, on the **Recommended** tab, select the **Profile editing** policy.</span></span>
1. <span data-ttu-id="2afc7-137">Sláðu inn heiti fyrir regluna (t.d. **B2C\_1\_EditProfile**).</span><span class="sxs-lookup"><span data-stu-id="2afc7-137">Enter a name for the policy (for example, **B2C\_1\_EditProfile**).</span></span>
1. <span data-ttu-id="2afc7-138">Í hlutanum **Kennisveitendur** velurðu kennisveitendurna sem nota á fyrir regluna.</span><span class="sxs-lookup"><span data-stu-id="2afc7-138">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="2afc7-139">Að lágmarki verður **Innskráning á staðbundin reikning** að vera valin.</span><span class="sxs-lookup"><span data-stu-id="2afc7-139">At a minimum, **Local Account SignIn** must be selected.</span></span>
1. <span data-ttu-id="2afc7-140">Í dálkinn **Innheimtueigind** skaltu velja gátreitina fyrir **Netföng** og **Eftirnafn**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-140">In the **Collect attribute** column, select the check boxes for **Email Addresses** and **Surname**.</span></span>
1. <span data-ttu-id="2afc7-141">Í dálknum **Skilakrafa** skaltu velja gátreitina fyrir **Netföng**, **Fornafn**, **Kennisveitandi**, **Eftirnafn** og **Hlutakenni notanda**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-141">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="2afc7-142">Velja skal **Í lagi** til að stofna regluna.</span><span class="sxs-lookup"><span data-stu-id="2afc7-142">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="2afc7-143">Tvísmelltu á nýja regluheitið og veldu síðan í yfirlitsglugganum **Eiginleikar**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-143">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="2afc7-144">Stilltu valkostinn **Virkja JavaScript til að framfylgja blaðsíðuútliti (forsskoðun)** á **Á**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-144">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="2afc7-145">Þú munt fara aftur í þessa reglu til að klára uppsetninguna eftir að þú hefur smíðað sérsniðnar síður.</span><span class="sxs-lookup"><span data-stu-id="2afc7-145">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="2afc7-146">Lokaðu reglunni í bili til að fara aftur á síðuna **Notendastreymi (reglur)** á Azure gáttinni.</span><span class="sxs-lookup"><span data-stu-id="2afc7-146">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-password-reset-policy"></a><span data-ttu-id="2afc7-147">Stilltu regluna „Núllstilla lykilorð“</span><span class="sxs-lookup"><span data-stu-id="2afc7-147">Configure the "Password reset" policy</span></span>

<span data-ttu-id="2afc7-148">Til að skilgreina regluna „Aðgangsorð endurstillt“ skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="2afc7-148">To configure the "Password reset" policy, follow these steps.</span></span>

1. <span data-ttu-id="2afc7-149">Veldu **Nýtt notendaflæði** og síðan á flipanum **Forskoða** velurðu regluna **Aðgangsorð endurstill v1.1**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-149">Select **New user flow**, and then, on the **Preview** tab, select the **Password reset v1.1** policy.</span></span>

    ![V1.1 reglan fyrir endurstillingu aðgangsorðs valin á flipanum Forskoða](./media/B2C_ForgetPassword_Menu.png)

1. <span data-ttu-id="2afc7-151">Sláðu inn heiti fyrir regluna (t.d. **B2C\_1\_ForgetPassword**).</span><span class="sxs-lookup"><span data-stu-id="2afc7-151">Enter a name for the policy (for example, **B2C\_1\_ForgetPassword**).</span></span>
1. <span data-ttu-id="2afc7-152">Í hlutanum **Kennisveitendur** velurðu **Endurstilla aðgangsorð með netfangi**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-152">In the **Identity Providers** section, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="2afc7-153">Í dálknum **Skilakrafa** velurðu gátreitina fyrir **Netföng**, **Fornafn**, **Eftirnafn** og **Hlutakenni notanda**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-153">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Surname**, and **User's Object ID**.</span></span>

    ![Valdar kröfur](./media/B2C_ForgetPassword_Attributes.png)

1. <span data-ttu-id="2afc7-155">Velja skal **Í lagi** til að stofna regluna.</span><span class="sxs-lookup"><span data-stu-id="2afc7-155">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="2afc7-156">Tvísmelltu á nýja regluheitið og veldu síðan í yfirlitsglugganum **Eiginleikar**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-156">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="2afc7-157">Stilltu valkostinn **Virkja JavaScript til að framfylgja blaðsíðuútliti (forsskoðun)** á **Á**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-157">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="2afc7-158">Þú munt fara aftur í þessa reglu til að klára uppsetninguna eftir að þú hefur smíðað sérsniðnar síður.</span><span class="sxs-lookup"><span data-stu-id="2afc7-158">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="2afc7-159">Lokaðu reglunni í bili til að fara aftur á síðuna **Notendastreymi (reglur)** á Azure gáttinni.</span><span class="sxs-lookup"><span data-stu-id="2afc7-159">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

## <a name="build-the-custom-pages"></a><span data-ttu-id="2afc7-160">Smíða sérsniðnar síður</span><span class="sxs-lookup"><span data-stu-id="2afc7-160">Build the custom pages</span></span>

<span data-ttu-id="2afc7-161">Fylgdu þessum skrefum til að búa til sérsniðnar síður til að meðhöndla innskráningu notenda.</span><span class="sxs-lookup"><span data-stu-id="2afc7-161">To build the custom pages to handle user sign-ins, follow these steps.</span></span>

1. <span data-ttu-id="2afc7-162">Farðu á síðuna þína í höfundatólum verslunarinnar.</span><span class="sxs-lookup"><span data-stu-id="2afc7-162">In the Commerce authoring tools, go to your site.</span></span>
1. <span data-ttu-id="2afc7-163">Búðu til eftirfarandi fimm sniðmát og fimm blaðsíður:</span><span class="sxs-lookup"><span data-stu-id="2afc7-163">Build the following five templates and five pages:</span></span>

    - <span data-ttu-id="2afc7-164">Sniðmátið **Innskráning** og síðu sem notar innskráningareininguna.</span><span class="sxs-lookup"><span data-stu-id="2afc7-164">A **Sign In** template and page that use the sign in module.</span></span>
    - <span data-ttu-id="2afc7-165">Sniðmátið **Skráning** og síðu sem notar skráningareininguna.</span><span class="sxs-lookup"><span data-stu-id="2afc7-165">A **Sign Up** template and page that use the sign up module.</span></span>
    - <span data-ttu-id="2afc7-166">Sniðmátið **Aðgangsorð endurstillt** og síðu sem notar eininguna aðgangsorð endurstillt.</span><span class="sxs-lookup"><span data-stu-id="2afc7-166">A **Password Reset** template and page that use the password reset module.</span></span>
    - <span data-ttu-id="2afc7-167">Sniðmátið **Staðfesting á endurstillingu aðgangsorðs** og síðu sem notar eininguna staðfesting á endurstillingu aðgangsorðs.</span><span class="sxs-lookup"><span data-stu-id="2afc7-167">A **Password Reset verification** template and page that use the password reset verification module.</span></span>
    - <span data-ttu-id="2afc7-168">Sniðmátið **Forstillingum breytt** og síðu sem notar eininguna lykilforstillingum breytt</span><span class="sxs-lookup"><span data-stu-id="2afc7-168">A **Profile Edit** template and page that use the account profile edit module</span></span>

<span data-ttu-id="2afc7-169">Fylgdu þessum leiðbeiningum þegar þú smíðar síðurnar:</span><span class="sxs-lookup"><span data-stu-id="2afc7-169">When you build the pages, follow these guidelines:</span></span>

- <span data-ttu-id="2afc7-170">Notaðu útlit og stíl fyrir hverja síðu eða einingu sem hentar best viðskiptaþörfum þínum.</span><span class="sxs-lookup"><span data-stu-id="2afc7-170">For each page or module, use the layout and style that best suit your business requirements.</span></span>
- <span data-ttu-id="2afc7-171">Birtu allar síður og vefslóðir sem þarf að nota í uppsetningu Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="2afc7-171">Publish all pages and URLs that must be used in the Azure AD B2C setup.</span></span>
- <span data-ttu-id="2afc7-172">Eftir að síðurnar og vefslóðirnar eru birtar safnarðu vefslóðum sem verður að nota fyrir regluskilgreiningar Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="2afc7-172">After the pages and URLs are published, collect the URLs that must be used for the Azure AD B2C policy configurations.</span></span> <span data-ttu-id="2afc7-173">Viðskeytinu **?preloadscripts=true** verður bætt við hverja vefslóð þegar það er notað.</span><span class="sxs-lookup"><span data-stu-id="2afc7-173">A **?preloadscripts=true** suffix will be added to every URL when it's used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2afc7-174">Ekki endurnýta altækan hausa og síðufætur sem hafa tengda tengla.</span><span class="sxs-lookup"><span data-stu-id="2afc7-174">Don't reuse universal headers and footers that have relative links.</span></span> <span data-ttu-id="2afc7-175">Vegna þess að þessar síður verða hýstar í Azure AD B2C lén þegar þau eru notuð, aðeins hreinar vefslóðir ættu að nota fyrir alla tengla.</span><span class="sxs-lookup"><span data-stu-id="2afc7-175">Because these pages will be hosted in the Azure AD B2C domain when they are used, only absolute URLs should be used for all links.</span></span>

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a><span data-ttu-id="2afc7-176">Stilla Azure AD B2C reglur með sérsniðnum síðuupplýsingum</span><span class="sxs-lookup"><span data-stu-id="2afc7-176">Configure Azure AD B2C policies with custom page information</span></span> 

<span data-ttu-id="2afc7-177">Farðu aftur í Azure gáttina á síðuna **Azure AD B2C** og síðan, á valmyndinni undir **Reglur**, velurðu **Notendastreymi (reglur)**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-177">In the Azure portal, return to the **Azure AD B2C** page, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a><span data-ttu-id="2afc7-178">Uppfærðu regluna „Skráning og innskráning“ með sérsniðnum síðuupplýsingum</span><span class="sxs-lookup"><span data-stu-id="2afc7-178">Update the "Sign up and sign in" policy with custom page information</span></span>

<span data-ttu-id="2afc7-179">Til að uppfæra regluna „Skráning og innskráning“ með sérsniðnum síðuupplýsingum fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="2afc7-179">To update the "Sign up and sign in" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="2afc7-180">Í reglunni **Skráning og innskráning** sem þú stilltir áður skaltu velja í leiðsöguskjánum **Síðuútlit**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-180">In the **Sign in and sign up** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="2afc7-181">Veldu útlitið **Samræmd skráningar- eða innskráningarsíða**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-181">Select the **Unified sign up or sign in page** layout.</span></span>
1. <span data-ttu-id="2afc7-182">Stilltu valkostinn **Nota sérsniðið síðuefni** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-182">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="2afc7-183">Í reitinn **Sérsniðin URI** slærðu inn alla innskráningarslóðina.</span><span class="sxs-lookup"><span data-stu-id="2afc7-183">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="2afc7-184">Hafðu viðskeytið **?preloadscripts=true** með.</span><span class="sxs-lookup"><span data-stu-id="2afc7-184">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="2afc7-185">Til dæmis er slegið inn ``www.<my domain>.com/sign-in?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="2afc7-185">For example, enter ``www.<my domain>.com/sign-in?preloadscripts=true``.</span></span>
1. <span data-ttu-id="2afc7-186">Í reitnum **Útgáfa síðuútlits (forskoða)** velurðu **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-186">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="2afc7-187">Veldu útlitið **Skráningarsíða staðbundins reiknings**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-187">Select the **Local account sign up page** layout.</span></span>
1. <span data-ttu-id="2afc7-188">Stilltu valkostinn **Nota sérsniðið síðuefni** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-188">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="2afc7-189">Í reitinn **Sérsniðin URI** slærðu inn alla skráningarslóðina.</span><span class="sxs-lookup"><span data-stu-id="2afc7-189">In the **Custom page URI** field, enter the full sign-up URL.</span></span> <span data-ttu-id="2afc7-190">Hafðu viðskeytið **?preloadscripts=true** með.</span><span class="sxs-lookup"><span data-stu-id="2afc7-190">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="2afc7-191">Til dæmis er slegið inn ``www.<my domain>.com/sign-up?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="2afc7-191">For example, enter ``www.<my domain>.com/sign-up?preloadscripts=true``.</span></span>
1. <span data-ttu-id="2afc7-192">Í reitnum **Útgáfa síðuútlits (forskoða)** velurðu **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-192">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="2afc7-193">Í hlutanum **Eiginleikar notenda**, fylgdu þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="2afc7-193">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="2afc7-194">Fyrir eigindirnar **Netfang**, **Fornafn** og **Eftirnafn** skaltu velja **Nei** í reitnum **Krefst staðfestingar**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-194">For the **Email Address**, **Given Name**, and **Surname** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="2afc7-195">Fyrir eigindirnar **Fornafn** og **Eftirnafn** skaltu velja **Nei** í reitnum **Valfrjálst**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-195">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

    ![Stillingar reglu fyrir skráningarsíðu staðbundinna reikninga](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a><span data-ttu-id="2afc7-197">Uppfærðu regluna „Forstillingum breytt“ með sérsniðnum síðuupplýsingum</span><span class="sxs-lookup"><span data-stu-id="2afc7-197">Update the "Profile editing" policy with custom page information</span></span>

<span data-ttu-id="2afc7-198">Til að uppfæra regluna „Forstillingum breytt“ með sérsniðnum síðuupplýsingum fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="2afc7-198">To update the "Profile editing" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="2afc7-199">Í reglunni **Forstillingum breytt** sem þú stilltir áður skaltu velja í leiðsöguskjánum **Síðuútlit**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-199">In the **Profile Editing** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="2afc7-200">Veldu útlitið **Síðan Breyta forstillingum**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-200">Select the **Profile edit page** layout.</span></span>
1. <span data-ttu-id="2afc7-201">Stilltu valkostinn **Nota sérsniðið síðuefni** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-201">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="2afc7-202">Í reitinn **Sérsniðin URI** slærðu inn alla slóðina til að breyta forstillingum.</span><span class="sxs-lookup"><span data-stu-id="2afc7-202">In the **Custom page URI** field, enter the full profile edit URL.</span></span> <span data-ttu-id="2afc7-203">Hafðu viðskeytið **?preloadscripts=true** með.</span><span class="sxs-lookup"><span data-stu-id="2afc7-203">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="2afc7-204">Til dæmis er slegið inn ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="2afc7-204">For example, enter ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span></span>
1. <span data-ttu-id="2afc7-205">Í reitnum **Útgáfa síðuútlits (forskoða)** velurðu **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-205">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="2afc7-206">Í hlutanum **Eiginleikar notenda**, fylgdu þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="2afc7-206">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="2afc7-207">Fyrir eigindirnar **Netfang**, **Fornafn** skaltu velja **Nei** í reitnum **Krefst staðfestingar**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-207">For the **Email Address**, **Given Name** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="2afc7-208">Fyrir eigindirnar **Fornafn** og **Eftirnafn** skaltu velja **Nei** í reitnum **Valfrjálst**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-208">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

### <a name="update-the-password-reset-policy-with-custom-page-information"></a><span data-ttu-id="2afc7-209">Uppfærðu regluna „Aðgangsorð endurstillt“ með sérsniðnum síðuupplýsingum</span><span class="sxs-lookup"><span data-stu-id="2afc7-209">Update the "Password reset" policy with custom page information</span></span>

<span data-ttu-id="2afc7-210">Til að uppfæra regluna „Aðgangsorð endurstillt“ með sérsniðnum síðuupplýsingum fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="2afc7-210">To update the "Password reset" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="2afc7-211">Í reglunni **Aðgangsorð endurstillt** sem þú stilltir áður skaltu velja í leiðsöguskjánum **Síðuútlit**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-211">In the **Password Reset** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="2afc7-212">Veldu útlitið **Ný aðgangsorðasíða**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-212">Select the **New password page** layout.</span></span>
1. <span data-ttu-id="2afc7-213">Stilltu valkostinn **Nota sérsniðið síðuefni** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-213">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="2afc7-214">Í reitinn **Sérsniðin URI** slærðu inn alla slóðina til að endurstilla aðgangsorð.</span><span class="sxs-lookup"><span data-stu-id="2afc7-214">In the **Custom page URI** field, enter the full password reset URL.</span></span> <span data-ttu-id="2afc7-215">Hafðu viðskeytið **?preloadscripts=true** með.</span><span class="sxs-lookup"><span data-stu-id="2afc7-215">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="2afc7-216">Til dæmis er slegið inn ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="2afc7-216">For example, enter ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span></span>
1. <span data-ttu-id="2afc7-217">Í reitnum **Útgáfa síðuútlits (forskoða)** velurðu **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-217">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="2afc7-218">Veldu útlitið **Síðan Staðfesting á reikningi**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-218">Select the **Account verification page** layout.</span></span>
1. <span data-ttu-id="2afc7-219">Stilltu valkostinn **Nota sérsniðið síðuefni** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-219">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="2afc7-220">Í reitinn **Sérsniðin URI** slærðu inn alla stafestingarslóðina fyrir endurstillt aðgangsorð.</span><span class="sxs-lookup"><span data-stu-id="2afc7-220">In the **Custom page URI** field, enter the full password reset verification URL.</span></span> <span data-ttu-id="2afc7-221">Hafðu viðskeytið **?preloadscripts=true** með.</span><span class="sxs-lookup"><span data-stu-id="2afc7-221">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="2afc7-222">Til dæmis er slegið inn ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="2afc7-222">For example, enter ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span></span>
1. <span data-ttu-id="2afc7-223">Í reitnum **Útgáfa síðuútlits (forskoða)** velurðu **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-223">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a><span data-ttu-id="2afc7-224">Sérsníða sjálfgefna textastrengi fyrir merki og lýsingar</span><span class="sxs-lookup"><span data-stu-id="2afc7-224">Customize default text strings for labels and descriptions</span></span>

<span data-ttu-id="2afc7-225">Í einingasafninu eru innskráningareiningar forfylltar með sjálfgefnum textastrengjum fyrir merki og lýsingu.</span><span class="sxs-lookup"><span data-stu-id="2afc7-225">In the module library, sign-in modules are prefilled with default text strings for the labels and descriptions.</span></span> <span data-ttu-id="2afc7-226">Þú getur sérsniðið þessa strengi í hugbúnaðarþróunarbúnaðinum (SDK) með því að uppfæra gildin í global.json skránni fyrir innskráningarhlutann.</span><span class="sxs-lookup"><span data-stu-id="2afc7-226">You can customize these strings in the software development kit (SDK) by updating the values in the global.json file for the sign in module.</span></span>

<span data-ttu-id="2afc7-227">Til dæmis er sjálfgefinn texti fyrir tengilinn sem gleymdist lykilorð **Gleymt lykilorð?**.</span><span class="sxs-lookup"><span data-stu-id="2afc7-227">For example, the default text for the forgotten password link is **Forgotten password?**.</span></span> <span data-ttu-id="2afc7-228">Eftirfarandi sýnir þennan sjálfgefna texta á innskráningarsíðunni.</span><span class="sxs-lookup"><span data-stu-id="2afc7-228">The following shows this default text on the sign-in page.</span></span>

![Sjálfgefinn texti fyrir tengilinn við gleymt lykilorð á innskráningarsíðunni](./media/B2C_SignUp_ModuleFace.png)

<span data-ttu-id="2afc7-230">Í global.json skrá fyrir innskráningareiningu einingasafnsins er hægt að breyta textanum í **Manstu ekki aðgangsorðið?** eins og sýnt er á eftirfarandi teikningu.</span><span class="sxs-lookup"><span data-stu-id="2afc7-230">However, in the global.json file for the module library sign-in module, you can edit the text to **Forgot Password?**, as shown in the following illustration.</span></span>

![Uppfærður tenglatexti í global.json skránni í einingunni](./media/B2C_CustomizingStringsForModule.png)

<span data-ttu-id="2afc7-232">Þegar búið er að uppfæra global.json-skrá og birta breytingarnar birtist nýr tengill í innskráningareiningunni í bæði verslun og á innskráningarsíðunni.</span><span class="sxs-lookup"><span data-stu-id="2afc7-232">After you update the global.json file and publish your changes, the new link text appears in the sign-in module in both Commerce and on the live sign-in page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2afc7-233">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="2afc7-233">Additional resources</span></span>

[<span data-ttu-id="2afc7-234">Skilgreina lénsheiti</span><span class="sxs-lookup"><span data-stu-id="2afc7-234">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="2afc7-235">Uppsetning á nýjum leigjanda rafrænna viðskipta</span><span class="sxs-lookup"><span data-stu-id="2afc7-235">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="2afc7-236">Stofna svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="2afc7-236">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="2afc7-237">Tengja svæði Dynamics 365 Commerce við netrás</span><span class="sxs-lookup"><span data-stu-id="2afc7-237">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="2afc7-238">Vinna með skrárnar robots.txt</span><span class="sxs-lookup"><span data-stu-id="2afc7-238">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="2afc7-239">Hlaða upp mörgum URL-framsendingum í einu</span><span class="sxs-lookup"><span data-stu-id="2afc7-239">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="2afc7-240">Setja upp B2C-leigjanda í Commerce</span><span class="sxs-lookup"><span data-stu-id="2afc7-240">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="2afc7-241">Stilla marga B2C leigjendur í viðskiptaumhverfi</span><span class="sxs-lookup"><span data-stu-id="2afc7-241">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="2afc7-242">Bæta við stuðningi fyrir efnisbirtingarnet (CDN)</span><span class="sxs-lookup"><span data-stu-id="2afc7-242">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="2afc7-243">Virkja greiningu á verslun eftir staðsetningu</span><span class="sxs-lookup"><span data-stu-id="2afc7-243">Enable location-based store detection</span></span>](enable-store-detection.md)
