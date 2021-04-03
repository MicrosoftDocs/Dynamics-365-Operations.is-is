---
title: Setja upp sérsniðnar síður fyrir innskráningu notenda
description: Þetta efnisatriði lýsir því hvernig á að búa til sérsmíðaðar síður í Microsoft Dynamics 365 Commerce sem meðhöndla sérstilltar innskráningar fyrir notendur Azure Active Directory (Azure AD) sem eru B2C leigjendur.
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
ms.openlocfilehash: 3328fad5328ae1954a6749f9a5eebcb71c723698
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477949"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a><span data-ttu-id="61838-103">Setja upp sérsniðnar síður fyrir innskráningu notenda</span><span class="sxs-lookup"><span data-stu-id="61838-103">Set up custom pages for user sign-ins</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="61838-104">Þetta efnisatriði lýsir því hvernig á að búa til sérsmíðaðar síður í Microsoft Dynamics 365 Commerce sem meðhöndla sérstilltar innskráningar fyrir notendur Azure Active Directory (Azure AD) sem eru B2C leigjendur.</span><span class="sxs-lookup"><span data-stu-id="61838-104">This topic describes how to build custom pages in Microsoft Dynamics 365 Commerce that handle customized sign-ins for users of Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants.</span></span>

<span data-ttu-id="61838-105">Til að nota sérsniðnar síður sem eru gerðar í Dynamics 365 Commerce til að takast á við innskráningarflæði notenda verður þú að setja upp Azure AD stefnu sem vísað verður til í viðskiptaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="61838-105">To use custom pages that are authored in Dynamics 365 Commerce to handle user sign-in flows, you must set up the Azure AD policies that will be referenced in the Commerce environment.</span></span> <span data-ttu-id="61838-106">Þú getur stillt „Skráning og innskráning“, „Forstillingum breytt“ og „Aðgangsorð endurstillt“ Azure AD B2C stefnur með því að nota Azure AD B2C forrit.</span><span class="sxs-lookup"><span data-stu-id="61838-106">You can configure the "Sign up and sign in," "Profile editing," and "Password reset" Azure AD B2C policies by using the Azure AD B2C application.</span></span> <span data-ttu-id="61838-107">Síðan er hægt að vísa til Azure AD B2C leigjanda og stefnuheita við útvegunarferlið sem er gert fyrir viðskiptaumhverfið með því að nota Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="61838-107">The Azure AD B2C tenant and policy names can then be referenced during the provisioning process that is done for the Commerce environment by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="61838-108">Hægt er að smíða sérsniðnar viðskiptasíður með því að nota innskráningu, skráningu, breytingu reikningssniðs eða endurstillingu lykilorðs.</span><span class="sxs-lookup"><span data-stu-id="61838-108">The custom Commerce pages can be built by using the sign in, sign up, account profile edit, or password reset module.</span></span> <span data-ttu-id="61838-109">Síðan ætti að vísa í vefslóðir síðunnar sem eru birtar fyrir þessar sérsniðnu síður Azure AD B2C stefnuskilgreiningar í Azure gáttinni.</span><span class="sxs-lookup"><span data-stu-id="61838-109">The page URLs that are published for these custom pages should then be referenced in Azure AD B2C policy configurations in the Azure portal.</span></span>

## <a name="set-up-b2c-policies"></a><span data-ttu-id="61838-110">Setja upp B2C reglur</span><span class="sxs-lookup"><span data-stu-id="61838-110">Set up B2C policies</span></span>

<span data-ttu-id="61838-111">Eftir að þú hefur sett upp þinn Azure AD B2C leigjanda og tengt hann við viðskiptaumhverfi þitt ferðu á síðuna **Azure AD B2C** í Azure gáttinni og síðan á valmyndinni undir **Stefnur** velurðu **Notendastreymi (reglur)**.</span><span class="sxs-lookup"><span data-stu-id="61838-111">After you set up your Azure AD B2C tenant and associate it with your Commerce environment, go to the **Azure AD B2C** page in the Azure portal, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

![Skipunin Notandaflæði (stefna) í valmyndinni](./media/B2C_CustomPage_PoliciesMenu.png)

<span data-ttu-id="61838-113">Þú getur nú stillt innskráninguna "Skráðu þig inn og skráðu þig inn", "Prófíklippingu" og "Lykilorð endurstillt" innskráningarflæði notenda.</span><span class="sxs-lookup"><span data-stu-id="61838-113">You can now configure the "Sign up and sign in," "Profile editing," and "Password reset" user sign-in flows.</span></span>

### <a name="configure-the-sign-up-and-sign-in-policy"></a><span data-ttu-id="61838-114">Stilla stefnuna „Skráning og innskráning“</span><span class="sxs-lookup"><span data-stu-id="61838-114">Configure the "Sign up and sign in" policy</span></span>

<span data-ttu-id="61838-115">Fylgdu þessum skrefum til að stilla stefnuna „Skráning og innskráning“.</span><span class="sxs-lookup"><span data-stu-id="61838-115">To configure the "Sign up and sign in" policy, follow these steps.</span></span>

1. <span data-ttu-id="61838-116">Veldu **Nýtt notendaflæði** og síðan á flipanum **Ráðlagt** velurðu regluna **Skráning og innskráning**.</span><span class="sxs-lookup"><span data-stu-id="61838-116">Select **New user flow**, and then, on the **Recommended** tab, select the **Sign up and sign in** policy.</span></span>
1. <span data-ttu-id="61838-117">Sláðu inn heiti fyrir regluna (t.d. **B2C\_1\_SignInSignUp**).</span><span class="sxs-lookup"><span data-stu-id="61838-117">Enter a name for the policy (for example, **B2C\_1\_SignInSignUp**).</span></span>
1. <span data-ttu-id="61838-118">Í hlutanum **Kennisveitendur** velurðu kennisveitendurna sem nota á fyrir regluna.</span><span class="sxs-lookup"><span data-stu-id="61838-118">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="61838-119">Að lágmarki verður **Innskráning í gegnum tölvupóst** að vera valin.</span><span class="sxs-lookup"><span data-stu-id="61838-119">At a minimum, **Email signup** must be selected.</span></span>
1. <span data-ttu-id="61838-120">Í dálkinn **Innheimtueigind** skaltu velja gátreitina fyrir **Netfang**, **Fornafn** og **Eftirnafn**.</span><span class="sxs-lookup"><span data-stu-id="61838-120">In the **Collect attribute** column, select the check boxes for **Email Address**, **Given Name**, and **Surname**.</span></span>
1. <span data-ttu-id="61838-121">Í dálknum **Skilakrafa** skaltu velja gátreitina fyrir **Netföng**, **Fornafn**, **Kennisveitandi**, **Eftirnafn** og **Hlutakenni notanda**.</span><span class="sxs-lookup"><span data-stu-id="61838-121">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>

    ![Eiginleikar og kröfur valdar](./media/B2C_SignInSignUp_Attributes.png)

1. <span data-ttu-id="61838-123">Velja skal **Í lagi** til að stofna regluna.</span><span class="sxs-lookup"><span data-stu-id="61838-123">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="61838-124">Tvísmelltu á nýja regluheitið og veldu síðan í yfirlitsglugganum **Eiginleikar**.</span><span class="sxs-lookup"><span data-stu-id="61838-124">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="61838-125">Stilltu valkostinn **Virkja JavaScript til að framfylgja blaðsíðuútliti (forsskoðun)** á **Á**.</span><span class="sxs-lookup"><span data-stu-id="61838-125">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

    ![Eiginleikasíða fyrir nýju regluna](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> <span data-ttu-id="61838-127">Vísað verður að fullu til heitis reglunnar í viðskiptaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="61838-127">The policy name will be fully referenced in the Commerce environment.</span></span> <span data-ttu-id="61838-128">(Forskeytið **B2C\_1\_** verður með í tilvísuninni.) Ekki er hægt að endurnefna reglur eftir að þær eru búnar til.</span><span class="sxs-lookup"><span data-stu-id="61838-128">(The **B2C\_1\_** prefix will be included in the reference.) Policies can't be renamed after they are created.</span></span> <span data-ttu-id="61838-129">Ef þú ert að skipta út núverandi reglu fyrir viðskiptaumhverfi þitt geturðu eytt upprunalegu reglunni og byggt upp nýja reglu með sama heiti.</span><span class="sxs-lookup"><span data-stu-id="61838-129">If you're replacing an existing policy for your Commerce environment, you can delete the original policy and build a new policy that has the same name.</span></span> <span data-ttu-id="61838-130">Að öðrum kosti, ef umhverfið hefur þegar verið útvegað, geturðu sent nýja regluheitið í gegnum þjónustubeiðni.</span><span class="sxs-lookup"><span data-stu-id="61838-130">Alternatively, if the environment has already been provisioned, you can submit the new policy name through a service request.</span></span>

<span data-ttu-id="61838-131">Þú munt fara aftur í þessa reglu til að klára uppsetninguna eftir að þú hefur smíðað sérsniðnar síður.</span><span class="sxs-lookup"><span data-stu-id="61838-131">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="61838-132">Lokaðu reglunni í bili til að fara aftur á síðuna **Notendastreymi (reglur)** á Azure gáttinni.</span><span class="sxs-lookup"><span data-stu-id="61838-132">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-profile-editing-policy"></a><span data-ttu-id="61838-133">Stilla regluna „Forstillingum breytt“</span><span class="sxs-lookup"><span data-stu-id="61838-133">Configure the "Profile editing" policy</span></span>

<span data-ttu-id="61838-134">Til að skilgreina regluna „Forstillingum breytt“ skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="61838-134">To configure the "Profile editing" policy, follow these steps.</span></span>

1. <span data-ttu-id="61838-135">Veldu **Nýtt notendaflæði** og síðan á flipanum **Ráðlagt** velurðu regluna **Forstillingum breytt**.</span><span class="sxs-lookup"><span data-stu-id="61838-135">Select **New user flow**, and then, on the **Recommended** tab, select the **Profile editing** policy.</span></span>
1. <span data-ttu-id="61838-136">Sláðu inn heiti fyrir regluna (t.d. **B2C\_1\_EditProfile**).</span><span class="sxs-lookup"><span data-stu-id="61838-136">Enter a name for the policy (for example, **B2C\_1\_EditProfile**).</span></span>
1. <span data-ttu-id="61838-137">Í hlutanum **Kennisveitendur** velurðu kennisveitendurna sem nota á fyrir regluna.</span><span class="sxs-lookup"><span data-stu-id="61838-137">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="61838-138">Að lágmarki verður **Innskráning á staðbundin reikning** að vera valin.</span><span class="sxs-lookup"><span data-stu-id="61838-138">At a minimum, **Local Account SignIn** must be selected.</span></span>
1. <span data-ttu-id="61838-139">Í dálkinn **Innheimtueigind** skaltu velja gátreitina fyrir **Netföng** og **Eftirnafn**.</span><span class="sxs-lookup"><span data-stu-id="61838-139">In the **Collect attribute** column, select the check boxes for **Email Addresses** and **Surname**.</span></span>
1. <span data-ttu-id="61838-140">Í dálknum **Skilakrafa** skaltu velja gátreitina fyrir **Netföng**, **Fornafn**, **Kennisveitandi**, **Eftirnafn** og **Hlutakenni notanda**.</span><span class="sxs-lookup"><span data-stu-id="61838-140">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="61838-141">Velja skal **Í lagi** til að stofna regluna.</span><span class="sxs-lookup"><span data-stu-id="61838-141">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="61838-142">Tvísmelltu á nýja regluheitið og veldu síðan í yfirlitsglugganum **Eiginleikar**.</span><span class="sxs-lookup"><span data-stu-id="61838-142">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="61838-143">Stilltu valkostinn **Virkja JavaScript til að framfylgja blaðsíðuútliti (forsskoðun)** á **Á**.</span><span class="sxs-lookup"><span data-stu-id="61838-143">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="61838-144">Þú munt fara aftur í þessa reglu til að klára uppsetninguna eftir að þú hefur smíðað sérsniðnar síður.</span><span class="sxs-lookup"><span data-stu-id="61838-144">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="61838-145">Lokaðu reglunni í bili til að fara aftur á síðuna **Notendastreymi (reglur)** á Azure gáttinni.</span><span class="sxs-lookup"><span data-stu-id="61838-145">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-password-reset-policy"></a><span data-ttu-id="61838-146">Stilltu regluna „Núllstilla lykilorð“</span><span class="sxs-lookup"><span data-stu-id="61838-146">Configure the "Password reset" policy</span></span>

<span data-ttu-id="61838-147">Til að skilgreina regluna „Aðgangsorð endurstillt“ skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="61838-147">To configure the "Password reset" policy, follow these steps.</span></span>

1. <span data-ttu-id="61838-148">Veldu **Nýtt notendaflæði** og síðan á flipanum **Forskoða** velurðu regluna **Aðgangsorð endurstill v1.1**.</span><span class="sxs-lookup"><span data-stu-id="61838-148">Select **New user flow**, and then, on the **Preview** tab, select the **Password reset v1.1** policy.</span></span>

    ![V1.1 reglan fyrir endurstillingu aðgangsorðs valin á flipanum Forskoða](./media/B2C_ForgetPassword_Menu.png)

1. <span data-ttu-id="61838-150">Sláðu inn heiti fyrir regluna (t.d. **B2C\_1\_ForgetPassword**).</span><span class="sxs-lookup"><span data-stu-id="61838-150">Enter a name for the policy (for example, **B2C\_1\_ForgetPassword**).</span></span>
1. <span data-ttu-id="61838-151">Í hlutanum **Kennisveitendur** velurðu **Endurstilla aðgangsorð með netfangi**.</span><span class="sxs-lookup"><span data-stu-id="61838-151">In the **Identity Providers** section, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="61838-152">Í dálknum **Skilakrafa** velurðu gátreitina fyrir **Netföng**, **Fornafn**, **Eftirnafn** og **Hlutakenni notanda**.</span><span class="sxs-lookup"><span data-stu-id="61838-152">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Surname**, and **User's Object ID**.</span></span>

    ![Valdar kröfur](./media/B2C_ForgetPassword_Attributes.png)

1. <span data-ttu-id="61838-154">Velja skal **Í lagi** til að stofna regluna.</span><span class="sxs-lookup"><span data-stu-id="61838-154">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="61838-155">Tvísmelltu á nýja regluheitið og veldu síðan í yfirlitsglugganum **Eiginleikar**.</span><span class="sxs-lookup"><span data-stu-id="61838-155">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="61838-156">Stilltu valkostinn **Virkja JavaScript til að framfylgja blaðsíðuútliti (forsskoðun)** á **Á**.</span><span class="sxs-lookup"><span data-stu-id="61838-156">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="61838-157">Þú munt fara aftur í þessa reglu til að klára uppsetninguna eftir að þú hefur smíðað sérsniðnar síður.</span><span class="sxs-lookup"><span data-stu-id="61838-157">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="61838-158">Lokaðu reglunni í bili til að fara aftur á síðuna **Notendastreymi (reglur)** á Azure gáttinni.</span><span class="sxs-lookup"><span data-stu-id="61838-158">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

## <a name="build-the-custom-pages"></a><span data-ttu-id="61838-159">Smíða sérsniðnar síður</span><span class="sxs-lookup"><span data-stu-id="61838-159">Build the custom pages</span></span>

<span data-ttu-id="61838-160">Fylgdu þessum skrefum til að búa til sérsniðnar síður til að meðhöndla innskráningu notenda.</span><span class="sxs-lookup"><span data-stu-id="61838-160">To build the custom pages to handle user sign-ins, follow these steps.</span></span>

1. <span data-ttu-id="61838-161">Farðu á síðuna þína í höfundatólum verslunarinnar.</span><span class="sxs-lookup"><span data-stu-id="61838-161">In the Commerce authoring tools, go to your site.</span></span>
1. <span data-ttu-id="61838-162">Búðu til eftirfarandi fimm sniðmát og fimm blaðsíður:</span><span class="sxs-lookup"><span data-stu-id="61838-162">Build the following five templates and five pages:</span></span>

    - <span data-ttu-id="61838-163">Sniðmátið **Innskráning** og síðu sem notar innskráningareininguna.</span><span class="sxs-lookup"><span data-stu-id="61838-163">A **Sign In** template and page that use the sign in module.</span></span>
    - <span data-ttu-id="61838-164">Sniðmátið **Skráning** og síðu sem notar skráningareininguna.</span><span class="sxs-lookup"><span data-stu-id="61838-164">A **Sign Up** template and page that use the sign up module.</span></span>
    - <span data-ttu-id="61838-165">Sniðmátið **Aðgangsorð endurstillt** og síðu sem notar eininguna aðgangsorð endurstillt.</span><span class="sxs-lookup"><span data-stu-id="61838-165">A **Password Reset** template and page that use the password reset module.</span></span>
    - <span data-ttu-id="61838-166">Sniðmátið **Staðfesting á endurstillingu aðgangsorðs** og síðu sem notar eininguna staðfesting á endurstillingu aðgangsorðs.</span><span class="sxs-lookup"><span data-stu-id="61838-166">A **Password Reset verification** template and page that use the password reset verification module.</span></span>
    - <span data-ttu-id="61838-167">Sniðmátið **Forstillingum breytt** og síðu sem notar eininguna lykilforstillingum breytt</span><span class="sxs-lookup"><span data-stu-id="61838-167">A **Profile Edit** template and page that use the account profile edit module</span></span>

<span data-ttu-id="61838-168">Fylgdu þessum leiðbeiningum þegar þú smíðar síðurnar:</span><span class="sxs-lookup"><span data-stu-id="61838-168">When you build the pages, follow these guidelines:</span></span>

- <span data-ttu-id="61838-169">Notaðu útlit og stíl fyrir hverja síðu eða einingu sem hentar best viðskiptaþörfum þínum.</span><span class="sxs-lookup"><span data-stu-id="61838-169">For each page or module, use the layout and style that best suit your business requirements.</span></span>
- <span data-ttu-id="61838-170">Birtu allar síður og vefslóðir sem þarf að nota í uppsetningu Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="61838-170">Publish all pages and URLs that must be used in the Azure AD B2C setup.</span></span>
- <span data-ttu-id="61838-171">Eftir að síðurnar og vefslóðirnar eru birtar safnarðu vefslóðum sem verður að nota fyrir regluskilgreiningar Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="61838-171">After the pages and URLs are published, collect the URLs that must be used for the Azure AD B2C policy configurations.</span></span> <span data-ttu-id="61838-172">Viðskeytinu **?preloadscripts=true** verður bætt við hverja vefslóð þegar það er notað.</span><span class="sxs-lookup"><span data-stu-id="61838-172">A **?preloadscripts=true** suffix will be added to every URL when it's used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="61838-173">Ekki endurnýta altækan hausa og síðufætur sem hafa tengda tengla.</span><span class="sxs-lookup"><span data-stu-id="61838-173">Don't reuse universal headers and footers that have relative links.</span></span> <span data-ttu-id="61838-174">Vegna þess að þessar síður verða hýstar í Azure AD B2C lén þegar þau eru notuð, aðeins hreinar vefslóðir ættu að nota fyrir alla tengla.</span><span class="sxs-lookup"><span data-stu-id="61838-174">Because these pages will be hosted in the Azure AD B2C domain when they are used, only absolute URLs should be used for all links.</span></span>

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a><span data-ttu-id="61838-175">Stilla Azure AD B2C reglur með sérsniðnum síðuupplýsingum</span><span class="sxs-lookup"><span data-stu-id="61838-175">Configure Azure AD B2C policies with custom page information</span></span> 

<span data-ttu-id="61838-176">Farðu aftur í Azure gáttina á síðuna **Azure AD B2C** og síðan, á valmyndinni undir **Reglur**, velurðu **Notendastreymi (reglur)**.</span><span class="sxs-lookup"><span data-stu-id="61838-176">In the Azure portal, return to the **Azure AD B2C** page, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a><span data-ttu-id="61838-177">Uppfærðu regluna „Skráning og innskráning“ með sérsniðnum síðuupplýsingum</span><span class="sxs-lookup"><span data-stu-id="61838-177">Update the "Sign up and sign in" policy with custom page information</span></span>

<span data-ttu-id="61838-178">Til að uppfæra regluna „Skráning og innskráning“ með sérsniðnum síðuupplýsingum fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="61838-178">To update the "Sign up and sign in" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="61838-179">Í reglunni **Skráning og innskráning** sem þú stilltir áður skaltu velja í leiðsöguskjánum **Síðuútlit**.</span><span class="sxs-lookup"><span data-stu-id="61838-179">In the **Sign in and sign up** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="61838-180">Veldu útlitið **Samræmd skráningar- eða innskráningarsíða**.</span><span class="sxs-lookup"><span data-stu-id="61838-180">Select the **Unified sign up or sign in page** layout.</span></span>
1. <span data-ttu-id="61838-181">Stilltu valkostinn **Nota sérsniðið síðuefni** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="61838-181">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="61838-182">Í reitinn **Sérsniðin URI** slærðu inn alla innskráningarslóðina.</span><span class="sxs-lookup"><span data-stu-id="61838-182">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="61838-183">Hafðu viðskeytið **?preloadscripts=true** með.</span><span class="sxs-lookup"><span data-stu-id="61838-183">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="61838-184">Til dæmis er slegið inn ``www.<my domain>.com/sign-in?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="61838-184">For example, enter ``www.<my domain>.com/sign-in?preloadscripts=true``.</span></span>
1. <span data-ttu-id="61838-185">Í reitnum **Útgáfa síðuútlits (forskoða)** velurðu **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="61838-185">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="61838-186">Veldu útlitið **Skráningarsíða staðbundins reiknings**.</span><span class="sxs-lookup"><span data-stu-id="61838-186">Select the **Local account sign up page** layout.</span></span>
1. <span data-ttu-id="61838-187">Stilltu valkostinn **Nota sérsniðið síðuefni** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="61838-187">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="61838-188">Í reitinn **Sérsniðin URI** slærðu inn alla skráningarslóðina.</span><span class="sxs-lookup"><span data-stu-id="61838-188">In the **Custom page URI** field, enter the full sign-up URL.</span></span> <span data-ttu-id="61838-189">Hafðu viðskeytið **?preloadscripts=true** með.</span><span class="sxs-lookup"><span data-stu-id="61838-189">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="61838-190">Til dæmis er slegið inn ``www.<my domain>.com/sign-up?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="61838-190">For example, enter ``www.<my domain>.com/sign-up?preloadscripts=true``.</span></span>
1. <span data-ttu-id="61838-191">Í reitnum **Útgáfa síðuútlits (forskoða)** velurðu **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="61838-191">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="61838-192">Í hlutanum **Eiginleikar notenda**, fylgdu þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="61838-192">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="61838-193">Fyrir eigindirnar **Netfang**, **Fornafn** og **Eftirnafn** skaltu velja **Nei** í reitnum **Krefst staðfestingar**.</span><span class="sxs-lookup"><span data-stu-id="61838-193">For the **Email Address**, **Given Name**, and **Surname** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="61838-194">Fyrir eigindirnar **Fornafn** og **Eftirnafn** skaltu velja **Nei** í reitnum **Valfrjálst**.</span><span class="sxs-lookup"><span data-stu-id="61838-194">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

    ![Stillingar reglu fyrir skráningarsíðu staðbundinna reikninga](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a><span data-ttu-id="61838-196">Uppfærðu regluna „Forstillingum breytt“ með sérsniðnum síðuupplýsingum</span><span class="sxs-lookup"><span data-stu-id="61838-196">Update the "Profile editing" policy with custom page information</span></span>

<span data-ttu-id="61838-197">Til að uppfæra regluna „Forstillingum breytt“ með sérsniðnum síðuupplýsingum fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="61838-197">To update the "Profile editing" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="61838-198">Í reglunni **Forstillingum breytt** sem þú stilltir áður skaltu velja í leiðsöguskjánum **Síðuútlit**.</span><span class="sxs-lookup"><span data-stu-id="61838-198">In the **Profile Editing** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="61838-199">Veldu útlitið **Síðan Breyta forstillingum**.</span><span class="sxs-lookup"><span data-stu-id="61838-199">Select the **Profile edit page** layout.</span></span>
1. <span data-ttu-id="61838-200">Stilltu valkostinn **Nota sérsniðið síðuefni** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="61838-200">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="61838-201">Í reitinn **Sérsniðin URI** slærðu inn alla slóðina til að breyta forstillingum.</span><span class="sxs-lookup"><span data-stu-id="61838-201">In the **Custom page URI** field, enter the full profile edit URL.</span></span> <span data-ttu-id="61838-202">Hafðu viðskeytið **?preloadscripts=true** með.</span><span class="sxs-lookup"><span data-stu-id="61838-202">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="61838-203">Til dæmis er slegið inn ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="61838-203">For example, enter ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span></span>
1. <span data-ttu-id="61838-204">Í reitnum **Útgáfa síðuútlits (forskoða)** velurðu **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="61838-204">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="61838-205">Í hlutanum **Eiginleikar notenda**, fylgdu þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="61838-205">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="61838-206">Fyrir eigindirnar **Netfang**, **Fornafn** skaltu velja **Nei** í reitnum **Krefst staðfestingar**.</span><span class="sxs-lookup"><span data-stu-id="61838-206">For the **Email Address**, **Given Name** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="61838-207">Fyrir eigindirnar **Fornafn** og **Eftirnafn** skaltu velja **Nei** í reitnum **Valfrjálst**.</span><span class="sxs-lookup"><span data-stu-id="61838-207">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

### <a name="update-the-password-reset-policy-with-custom-page-information"></a><span data-ttu-id="61838-208">Uppfærðu regluna „Aðgangsorð endurstillt“ með sérsniðnum síðuupplýsingum</span><span class="sxs-lookup"><span data-stu-id="61838-208">Update the "Password reset" policy with custom page information</span></span>

<span data-ttu-id="61838-209">Til að uppfæra regluna „Aðgangsorð endurstillt“ með sérsniðnum síðuupplýsingum fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="61838-209">To update the "Password reset" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="61838-210">Í reglunni **Aðgangsorð endurstillt** sem þú stilltir áður skaltu velja í leiðsöguskjánum **Síðuútlit**.</span><span class="sxs-lookup"><span data-stu-id="61838-210">In the **Password Reset** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="61838-211">Veldu útlitið **Ný aðgangsorðasíða**.</span><span class="sxs-lookup"><span data-stu-id="61838-211">Select the **New password page** layout.</span></span>
1. <span data-ttu-id="61838-212">Stilltu valkostinn **Nota sérsniðið síðuefni** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="61838-212">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="61838-213">Í reitinn **Sérsniðin URI** slærðu inn alla slóðina til að endurstilla aðgangsorð.</span><span class="sxs-lookup"><span data-stu-id="61838-213">In the **Custom page URI** field, enter the full password reset URL.</span></span> <span data-ttu-id="61838-214">Hafðu viðskeytið **?preloadscripts=true** með.</span><span class="sxs-lookup"><span data-stu-id="61838-214">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="61838-215">Til dæmis er slegið inn ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="61838-215">For example, enter ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span></span>
1. <span data-ttu-id="61838-216">Í reitnum **Útgáfa síðuútlits (forskoða)** velurðu **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="61838-216">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="61838-217">Veldu útlitið **Síðan Staðfesting á reikningi**.</span><span class="sxs-lookup"><span data-stu-id="61838-217">Select the **Account verification page** layout.</span></span>
1. <span data-ttu-id="61838-218">Stilltu valkostinn **Nota sérsniðið síðuefni** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="61838-218">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="61838-219">Í reitinn **Sérsniðin URI** slærðu inn alla stafestingarslóðina fyrir endurstillt aðgangsorð.</span><span class="sxs-lookup"><span data-stu-id="61838-219">In the **Custom page URI** field, enter the full password reset verification URL.</span></span> <span data-ttu-id="61838-220">Hafðu viðskeytið **?preloadscripts=true** með.</span><span class="sxs-lookup"><span data-stu-id="61838-220">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="61838-221">Til dæmis er slegið inn ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="61838-221">For example, enter ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span></span>
1. <span data-ttu-id="61838-222">Í reitnum **Útgáfa síðuútlits (forskoða)** velurðu **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="61838-222">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a><span data-ttu-id="61838-223">Sérsníða sjálfgefna textastrengi fyrir merki og lýsingar</span><span class="sxs-lookup"><span data-stu-id="61838-223">Customize default text strings for labels and descriptions</span></span>

<span data-ttu-id="61838-224">Í einingasafninu eru innskráningareiningar forfylltar með sjálfgefnum textastrengjum fyrir merki og lýsingu.</span><span class="sxs-lookup"><span data-stu-id="61838-224">In the module library, sign-in modules are prefilled with default text strings for the labels and descriptions.</span></span> <span data-ttu-id="61838-225">Þú getur sérsniðið þessa strengi í hugbúnaðarþróunarbúnaðinum (SDK) með því að uppfæra gildin í global.json skránni fyrir innskráningarhlutann.</span><span class="sxs-lookup"><span data-stu-id="61838-225">You can customize these strings in the software development kit (SDK) by updating the values in the global.json file for the sign in module.</span></span>

<span data-ttu-id="61838-226">Til dæmis er sjálfgefinn texti fyrir tengilinn sem gleymdist lykilorð **Gleymt lykilorð?**.</span><span class="sxs-lookup"><span data-stu-id="61838-226">For example, the default text for the forgotten password link is **Forgotten password?**.</span></span> <span data-ttu-id="61838-227">Eftirfarandi sýnir þennan sjálfgefna texta á innskráningarsíðunni.</span><span class="sxs-lookup"><span data-stu-id="61838-227">The following shows this default text on the sign-in page.</span></span>

![Sjálfgefinn texti fyrir tengilinn við gleymt lykilorð á innskráningarsíðunni](./media/B2C_SignUp_ModuleFace.png)

<span data-ttu-id="61838-229">Í global.json skrá fyrir innskráningareiningu einingasafnsins er hægt að breyta textanum í **Manstu ekki aðgangsorðið?** eins og sýnt er á eftirfarandi teikningu.</span><span class="sxs-lookup"><span data-stu-id="61838-229">However, in the global.json file for the module library sign-in module, you can edit the text to **Forgot Password?**, as shown in the following illustration.</span></span>

![Uppfærður tenglatexti í global.json skránni í einingunni](./media/B2C_CustomizingStringsForModule.png)

<span data-ttu-id="61838-231">Þegar búið er að uppfæra global.json-skrá og birta breytingarnar birtist nýr tengill í innskráningareiningunni í bæði verslun og á innskráningarsíðunni.</span><span class="sxs-lookup"><span data-stu-id="61838-231">After you update the global.json file and publish your changes, the new link text appears in the sign-in module in both Commerce and on the live sign-in page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="61838-232">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="61838-232">Additional resources</span></span>

[<span data-ttu-id="61838-233">Skilgreina lénsheiti</span><span class="sxs-lookup"><span data-stu-id="61838-233">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="61838-234">Uppsetning á nýjum leigjanda rafrænna viðskipta</span><span class="sxs-lookup"><span data-stu-id="61838-234">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="61838-235">Stofna svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="61838-235">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="61838-236">Tengja svæði Dynamics 365 Commerce við netrás</span><span class="sxs-lookup"><span data-stu-id="61838-236">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="61838-237">Vinna með skrárnar robots.txt</span><span class="sxs-lookup"><span data-stu-id="61838-237">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="61838-238">Hlaða upp mörgum URL-framsendingum í einu</span><span class="sxs-lookup"><span data-stu-id="61838-238">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="61838-239">Setja upp B2C-leigjanda í Commerce</span><span class="sxs-lookup"><span data-stu-id="61838-239">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="61838-240">Stilla marga B2C leigjendur í viðskiptaumhverfi</span><span class="sxs-lookup"><span data-stu-id="61838-240">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="61838-241">Bæta við stuðningi fyrir efnisbirtingarnet (CDN)</span><span class="sxs-lookup"><span data-stu-id="61838-241">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="61838-242">Virkja greiningu á verslun eftir staðsetningu</span><span class="sxs-lookup"><span data-stu-id="61838-242">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
