---
title: Úthluta forskoðunarumhverfi fyrir Commerce
description: Þetta efni útskýrir hvernig á að úthluta forskoðunarumhverfi Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b77d2cbbc100aeae5dcd53ddbe69ff2e4435da13
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934749"
---
# <a name="provision-a-commerce-preview-environment"></a><span data-ttu-id="e03ab-103">Úthluta forskoðunarumhverfi fyrir Commerce</span><span class="sxs-lookup"><span data-stu-id="e03ab-103">Provision a Commerce preview environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="e03ab-104">Þetta efni útskýrir hvernig á að úthluta forskoðunarumhverfi Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e03ab-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="e03ab-105">Áður en þú byrjar, mælum við með að þú rennir að minnsta kosti í gegnum allt efnið til að fá hugmynd um hvað ferlið felur í sér og hvað efnið inniheldur.</span><span class="sxs-lookup"><span data-stu-id="e03ab-105">Before you begin, we recommend that you at least skim through this whole topic to get an idea of what the process entails and what this topic contains.</span></span>

> [!NOTE]
> <span data-ttu-id="e03ab-106">Ef þér hefur ekki verið veittur aðgangur að forskoðun Dynamics 365 Commerce ennþá geturðu beðið um forsýningaraðgang af [Vefsíðu Commerce](https://aka.ms/Dynamics365CommerceWebsite).</span><span class="sxs-lookup"><span data-stu-id="e03ab-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="e03ab-107">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="e03ab-107">Overview</span></span>

<span data-ttu-id="e03ab-108">Til að úthluta forskoðunarumhverfi Commerce með góðum árangri verður þú að búa til verk sem hefur tiltekið vöruheiti og tegund.</span><span class="sxs-lookup"><span data-stu-id="e03ab-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="e03ab-109">Umhverfið og Retail Cloud Scale Unit (RCSU) hafa einnig nokkrar sérstakar færibreytur sem þú þarft að nota við úthlutun rafrænna viðskipta síðar.</span><span class="sxs-lookup"><span data-stu-id="e03ab-109">The environment and Retail Cloud Scale Unit (RCSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="e03ab-110">Leiðbeiningarnar í þessu efni lýsa öllum nauðsynlegum skrefum sem þú verður að ljúka og breytunum sem þú verður að nota.</span><span class="sxs-lookup"><span data-stu-id="e03ab-110">The instructions in this topic describe all the required steps that you must complete and the parameters that you must use.</span></span>

<span data-ttu-id="e03ab-111">Eftir árangursríka úthlutun á forskoðunarumhverfi Commerce þarf að ljúka nokkrum eftirúthlutunarskrefum til að undirbúa það.</span><span class="sxs-lookup"><span data-stu-id="e03ab-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="e03ab-112">Sum skref eru valkvæð, eftir þeim þáttum kerfisins þú vilt meta.</span><span class="sxs-lookup"><span data-stu-id="e03ab-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="e03ab-113">Þú getur alltaf klárað valfrjálsu skrefin seinna.</span><span class="sxs-lookup"><span data-stu-id="e03ab-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="e03ab-114">Fyrir upplýsingar um hvernig skuli stilla þér forskoðunarumhverfi Commerce eftir að því hefur verið úthlutað skal sjá [Stilla forskoðunarumhverfi Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="e03ab-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="e03ab-115">Upplýsingar um hvernig eigi að stilla valfrjálsa eiginleika fyrir forskoðunarumhverfi Commerce er að finna í [Stilla valfrjálsa eiginleika fyrir forskoðunarumhverfi Commerce](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="e03ab-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="e03ab-116">Láttu Microsoft vita ef þú hefur einhverjar spurningar um ráðstöfunarskrefin eða lendir í einhverjum vandræðum í [Microsoft Dynamics 365 Commerce forskoða Yammer hóp](https://aka.ms/Dynamics365CommercePreviewYammer).</span><span class="sxs-lookup"><span data-stu-id="e03ab-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e03ab-117">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="e03ab-117">Prerequisites</span></span>

<span data-ttu-id="e03ab-118">Eftirfarandi forsendur verða að vera til áður en þú getur veitt forskoðunarumhverfi Commerce:</span><span class="sxs-lookup"><span data-stu-id="e03ab-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="e03ab-119">Þú hefur aðgang að Microsoft Dynamics Lifecycle Services (LCS)-gáttinni.</span><span class="sxs-lookup"><span data-stu-id="e03ab-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="e03ab-120">Þú fékkst samþykkt inn í Dynamics 365 Commerce Forskoða kerfi.</span><span class="sxs-lookup"><span data-stu-id="e03ab-120">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="e03ab-121">Þú hefur nauðsynlegar heimildir til að búa til verk fyrir **Væntanlegar forsölur** eða **Flytja, búa til lausnir og læra**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-121">You have the required permissions to create a project for **Prospective presales** or **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="e03ab-122">Þú ert meðlimur í hlutverkinu **Umhverfisstjóri** eða **Eigandi verks** í verkinu þar sem þú munt að sjá um umhverfið</span><span class="sxs-lookup"><span data-stu-id="e03ab-122">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="e03ab-123">Þú hefur stjórnandaaðgang að Microsoft Azure-áskriftinni þinni eða ert í sambandi við áskriftarstjórann sem getur lokið skrefunum tveimur sem krefjast stjórnunarheimilda fyrir þína hönd.</span><span class="sxs-lookup"><span data-stu-id="e03ab-123">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="e03ab-124">Þú hefur leigjandakenni þitt fyrir Azure Active Directory (Azure AD) í boði.</span><span class="sxs-lookup"><span data-stu-id="e03ab-124">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="e03ab-125">Þú hefur búið til Azure AD-öryggishóp sem hægt er að nota sem kerfisstjórahóp netverslunar og þú ert með kenni hans tiltækt.</span><span class="sxs-lookup"><span data-stu-id="e03ab-125">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="e03ab-126">Þú hefur búið til Azure AD-öryggishóp sem hægt er að nota sem stjórnandahóp einkunna og umsagna og þú ert með kenni hans tiltækt.</span><span class="sxs-lookup"><span data-stu-id="e03ab-126">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="e03ab-127">(Þessi öryggishópur getur verið sá sami og kerfisstjórinn fyrir netkerfi.)</span><span class="sxs-lookup"><span data-stu-id="e03ab-127">(This security group can be the same as the e-Commerce system admin group.)</span></span>

### <a name="find-your-azure-ad-tenant-id"></a><span data-ttu-id="e03ab-128">Finndu Azure AD-leigjandakenni þitt</span><span class="sxs-lookup"><span data-stu-id="e03ab-128">Find your Azure AD tenant ID</span></span>

<span data-ttu-id="e03ab-129">Leigjandakenni þitt fyrir Azure AD er alþjóðlegt auðkenni (GUID) sem líkist þessu dæmi: **72f988bf-86f1-41af-91ab-2d7cd011db47**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-129">Your Azure AD tenant ID is a globally unique identifier (GUID) that resembles this example: **72f988bf-86f1-41af-91ab-2d7cd011db47**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-the-azure-portal"></a><span data-ttu-id="e03ab-130">Finndu Azure AD-leigjandakenni þitt með því að nota Azure-gáttina</span><span class="sxs-lookup"><span data-stu-id="e03ab-130">Find your Azure AD tenant ID by using the Azure portal</span></span>

1. <span data-ttu-id="e03ab-131">Skráðu þig inn á [Azure-gáttina](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="e03ab-131">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="e03ab-132">Gangið úr skugga um að rétt skráasafn sé valið.</span><span class="sxs-lookup"><span data-stu-id="e03ab-132">Make sure that the correct directory is selected.</span></span>
1. <span data-ttu-id="e03ab-133">Á valmyndinni til vinstri velurðu **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-133">On the menu on the left, select **Azure Active Directory**.</span></span>
1. <span data-ttu-id="e03ab-134">Undir **Stjórna** velurðu **Eiginleika**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-134">Under **Manage**, select **Properties**.</span></span> <span data-ttu-id="e03ab-135">Leigjandakenni þitt fyrir Azure AD birtist undir **Skráasafnskenni**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-135">Your Azure AD tenant ID appears under **Directory ID**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-openid-connect-metadata"></a><span data-ttu-id="e03ab-136">Finndu leigjandakenni þitt fyrir Azure AD með því að nota OpenID Connect-lýsigögn</span><span class="sxs-lookup"><span data-stu-id="e03ab-136">Find your Azure AD tenant ID by using OpenID Connect metadata</span></span>

<span data-ttu-id="e03ab-137">Búðu til OpenID-slóð með því að skipta út **\{YOUR\_DOMAIN\}** með léninu þínu, eins og `microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="e03ab-137">Create an OpenID URL by replacing **\{YOUR\_DOMAIN\}** with your domain, such as `microsoft.com`.</span></span> <span data-ttu-id="e03ab-138">Til dæmis, mun `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` verða `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.</span><span class="sxs-lookup"><span data-stu-id="e03ab-138">For example, `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` will become `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.</span></span>

1. <span data-ttu-id="e03ab-139">Farðu á OpenID-slóðina sem inniheldur lénið þitt.</span><span class="sxs-lookup"><span data-stu-id="e03ab-139">Go to the OpenID URL that contains your domain.</span></span>

    <span data-ttu-id="e03ab-140">Hægt er að finna leigjandakenni Azure AD í mörgum eiginleikagildum.</span><span class="sxs-lookup"><span data-stu-id="e03ab-140">You can find you Azure AD tenant ID in multiple property values.</span></span>

1. <span data-ttu-id="e03ab-141">Finndu **authorization\_endpoint** og dragðu út GUID sem birtist strax á eftir `login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="e03ab-141">Find **authorization\_endpoint**, and extract the GUID that appears immediately after `login.microsoftonline.com/`.</span></span>

### <a name="find-your-azure-ad-security-group-id"></a><span data-ttu-id="e03ab-142">Finndu þitt Azure AD-kenni öryggishóps</span><span class="sxs-lookup"><span data-stu-id="e03ab-142">Find your Azure AD security group ID</span></span>

<span data-ttu-id="e03ab-143">Kenni þitt fyrir Azure AD-öryggishóp er GUID sem líkist þessu dæmi: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-143">The ID of your Azure AD security group is a GUID that resembles this example: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.</span></span>

<span data-ttu-id="e03ab-144">Þessi aðferð gerir ráð fyrir að þú sért meðlimur í hópnum sem þú ert að reyna að finna kenni fyrir.</span><span class="sxs-lookup"><span data-stu-id="e03ab-144">This procedure assumes that you're a member of the group that you're trying to find the ID for.</span></span>

1. <span data-ttu-id="e03ab-145">Opnaðu [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer#).</span><span class="sxs-lookup"><span data-stu-id="e03ab-145">Open the [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer#).</span></span>
1. <span data-ttu-id="e03ab-146">Veldu **Skráðu inn með Microsoft** og skráðu þig inn með skilríkjum þínum.</span><span class="sxs-lookup"><span data-stu-id="e03ab-146">Select **Sign In with Microsoft**, and sign in by using your credentials.</span></span>
1. <span data-ttu-id="e03ab-147">Vinstra megin velurðu **sýna fleiri sýni**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-147">On the left, select **show more samples**.</span></span>
1. <span data-ttu-id="e03ab-148">Í hægri glugganum virkjarðu **Hópar**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-148">In the right pane, enable **Groups**.</span></span>
1. <span data-ttu-id="e03ab-149">Lokaðu hægri glugganum.</span><span class="sxs-lookup"><span data-stu-id="e03ab-149">Close the right pane.</span></span>
1. <span data-ttu-id="e03ab-150">Veldu **alla hópa sem ég tilheyri**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-150">Select **all groups I belong to**.</span></span>
1. <span data-ttu-id="e03ab-151">Í reitnum **Forskoðun svara** skaltu finna hópinn þinn.</span><span class="sxs-lookup"><span data-stu-id="e03ab-151">In the **Response Preview** field, find your group.</span></span> <span data-ttu-id="e03ab-152">Kenni öryggishópsins birtist undir eiginleikanum **kenni**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-152">The security group ID appears under the **id** property.</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="e03ab-153">Úthluta forskoðunarumhverfi þínu fyrir Commerce</span><span class="sxs-lookup"><span data-stu-id="e03ab-153">Provision your Commerce preview environment</span></span>

<span data-ttu-id="e03ab-154">Þessar aðferðir útskýra hvernig á að bjóða upp á forskoðunarumhverfi Commerce.</span><span class="sxs-lookup"><span data-stu-id="e03ab-154">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="e03ab-155">Þegar þú hefur lokið við þau er forskoðunarumhverfi Commerce tilbúið til uppsetningar.</span><span class="sxs-lookup"><span data-stu-id="e03ab-155">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="e03ab-156">Allar þær aðgerðir sem er lýst hér fara fram í LCS-gáttinni.</span><span class="sxs-lookup"><span data-stu-id="e03ab-156">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e03ab-157">Forskoðunaraðgangur er bundinn við LCS-reikninginn og -stofnunina sem þú tilgreindir í forskoðunarforritinu.</span><span class="sxs-lookup"><span data-stu-id="e03ab-157">Preview access is tied to the LCS account and organization that you specified in your preview application.</span></span> <span data-ttu-id="e03ab-158">Þú verður að nota sama reikning til að veita forskoðunarumhverfi Commerce.</span><span class="sxs-lookup"><span data-stu-id="e03ab-158">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="e03ab-159">Ef þú verður að nota annan LCS-reikning eða -leigjanda fyrir forskoðunarumhverfi Commerce verður þú að láta Microsoft í té þessar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="e03ab-159">If you must use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="e03ab-160">Sjá upplýsingar um tengilið í kaflanum [Stuðningur við forskoðunarumhverfi í Commerce](#commerce-preview-environment-support) síðar í þessu efni.</span><span class="sxs-lookup"><span data-stu-id="e03ab-160">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="grant-access-to-e-commerce-applications"></a><span data-ttu-id="e03ab-161">Veita aðgang að forritum með rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="e03ab-161">Grant access to e-Commerce applications</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e03ab-162">Sá sem skráir sig inn verður að vera Azure AD-leigjandastjóri sem hefur Azure AD-kenni leigjanda.</span><span class="sxs-lookup"><span data-stu-id="e03ab-162">The person who signs in must be an Azure AD tenant admin who has the Azure AD tenant ID.</span></span> <span data-ttu-id="e03ab-163">Ef þessu skrefi er ekki lokið án villu munu eftirstandandi úthlutunarskrefi ekki takast.</span><span class="sxs-lookup"><span data-stu-id="e03ab-163">If this step isn't successfully completed, the remaining provisioning steps will fail.</span></span>

<span data-ttu-id="e03ab-164">Fylgdu þessum skrefum til að heimila forritum rafrænna viðskipta að fá aðgang að Azure-áskriftinni.</span><span class="sxs-lookup"><span data-stu-id="e03ab-164">To authorize e-Commerce applications to access your Azure subscription, follow these steps.</span></span>

1. <span data-ttu-id="e03ab-165">Settu saman vefslóð á eftirfarandi sniði:</span><span class="sxs-lookup"><span data-stu-id="e03ab-165">Assemble a URL in the following format:</span></span>

    `https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345`

1. <span data-ttu-id="e03ab-166">Afritaðu og límdu slóðina í vafrann eða textaritilinn og settu í staðinn **\{AAD\_TENANT\_ID\}** með Azure AD-kenni leigjanda.</span><span class="sxs-lookup"><span data-stu-id="e03ab-166">Copy and paste the URL into your browser or text editor, and replace **\{AAD\_TENANT\_ID\}** with your Azure AD tenant ID.</span></span> <span data-ttu-id="e03ab-167">Opnaðu síðan slóðina.</span><span class="sxs-lookup"><span data-stu-id="e03ab-167">Then open the URL.</span></span>
1. <span data-ttu-id="e03ab-168">Í valmyndinni Azure AD skráirðu þig inn í og staðfestir að þú viljir veita **Dynamics 365 Commerce (Forskoðun)** aðgang að áskrift þinni.</span><span class="sxs-lookup"><span data-stu-id="e03ab-168">In the Azure AD sign-in dialog box, sign in, and confirm that you want to grant **Dynamics 365 Commerce (Preview)** access to your subscription.</span></span> <span data-ttu-id="e03ab-169">Þér verður beint á síðu sem segir hvort aðgerðin hafi tekist.</span><span class="sxs-lookup"><span data-stu-id="e03ab-169">You're redirected to a page that indicates whether the operation was successful.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="e03ab-170">Staðfestu að forskoðunaraðgerðir séu tiltækar og virkjaðar í LCS</span><span class="sxs-lookup"><span data-stu-id="e03ab-170">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="e03ab-171">Til að staðfesta að forskoðunaraðgerðir séu tiltækar og virkjaðar í LCS skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="e03ab-171">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="e03ab-172">Skráðu þig inn í [LCS-gáttina](https://lcs.dynamics.com) með því að nota sama LCS-reikning og þú notaðir til að biðja um aðgang að forskoðuninni.</span><span class="sxs-lookup"><span data-stu-id="e03ab-172">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="e03ab-173">Flettu alla leið til hægri á heimasíðu LCS og veldu reitinn **Forskoðun aðgerðastjórnunar**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-173">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![Stjórnun forskoðunarreits](./media/preview1.png)

1. <span data-ttu-id="e03ab-175">Skrunaðu niður að **Einkaforskoðunareiginleikar** og staðfestu að eftirfarandi aðgerðir séu tiltækar og virkjaðar:</span><span class="sxs-lookup"><span data-stu-id="e03ab-175">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="e03ab-176">Mat á rafrænum viðskipta</span><span class="sxs-lookup"><span data-stu-id="e03ab-176">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="e03ab-177">Forritsumhverfi forskoðunar á Commerce</span><span class="sxs-lookup"><span data-stu-id="e03ab-177">Commerce Preview Program Environments</span></span>

    ![Einkaforskoðunareiginleikar](./media/preview2.png)

1. <span data-ttu-id="e03ab-179">Ef þessir eiginleikar birtast ekki á listanum skaltu hafa samband við Microsoft og gefa upp vinnupóstfang þitt, LCS reikning og upplýsingar um leigjanda.</span><span class="sxs-lookup"><span data-stu-id="e03ab-179">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="e03ab-180">Sjá upplýsingar um tengilið í kaflanum [Stuðningur við forskoðunarumhverfi í Commerce](#commerce-preview-environment-support).</span><span class="sxs-lookup"><span data-stu-id="e03ab-180">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="e03ab-181">Stofna nýtt verk</span><span class="sxs-lookup"><span data-stu-id="e03ab-181">Create a new project</span></span>

<span data-ttu-id="e03ab-182">Til að stofna nýtt verk í LSC skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="e03ab-182">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="e03ab-183">Á heimasíðu LCS velurðu plúsmerkið (**+**) til að búa til verk.</span><span class="sxs-lookup"><span data-stu-id="e03ab-183">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="e03ab-184">Fylgdu einu af þessum skrefum á hægri glugganum:</span><span class="sxs-lookup"><span data-stu-id="e03ab-184">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="e03ab-185">Ef þú ert félagi skaltu velja **Flytja, búa til lausnir og læra**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-185">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="e03ab-186">Ef þú ert viðskiptavinur skaltu velja **Væntanleg forsala**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-186">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="e03ab-187">Færðu inn heiti, lýsingu og iðnað.</span><span class="sxs-lookup"><span data-stu-id="e03ab-187">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="e03ab-188">Í reitnum **Heiti afurðar** velurðu **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-188">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="e03ab-189">Í reitnum **Útgáfa afurðar** velurðu **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-189">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="e03ab-190">Í reitnum **Aðferð** velurðu **Dynamics Retail útfærsluaðferð**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-190">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="e03ab-191">Valfrjálst: Hægt er að flytja inn hlutverk og notendur úr fyrirliggjandi verki.</span><span class="sxs-lookup"><span data-stu-id="e03ab-191">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="e03ab-192">Velja **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-192">Select **Create**.</span></span> <span data-ttu-id="e03ab-193">Verksýnin birtist.</span><span class="sxs-lookup"><span data-stu-id="e03ab-193">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="e03ab-194">Bættu Azure-tengingunni við</span><span class="sxs-lookup"><span data-stu-id="e03ab-194">Add the Azure Connector</span></span>

<span data-ttu-id="e03ab-195">Fylgdu þessum skrefum til að bæta Azure Connector við LCS-verkið.</span><span class="sxs-lookup"><span data-stu-id="e03ab-195">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="e03ab-196">Fylgið einu af eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="e03ab-196">Follow one of these steps:</span></span>

    - <span data-ttu-id="e03ab-197">Ef þú ert félagi skaltu velja reitinn **Stillingar verks** lengst til hægri.</span><span class="sxs-lookup"><span data-stu-id="e03ab-197">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="e03ab-198">Ef þú ert viðskiptavinur velurðu **Stillingar verks** í efstu valmyndinni.</span><span class="sxs-lookup"><span data-stu-id="e03ab-198">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="e03ab-199">Velja **Azure-tengingar**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-199">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="e03ab-200">Veldu **Bæta við** til að bæta við Azure-tengingu.</span><span class="sxs-lookup"><span data-stu-id="e03ab-200">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="e03ab-201">Færið inn heiti.</span><span class="sxs-lookup"><span data-stu-id="e03ab-201">Enter a name.</span></span>
1. <span data-ttu-id="e03ab-202">Sláðu inn Azure-áskriftarkenni þitt.</span><span class="sxs-lookup"><span data-stu-id="e03ab-202">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="e03ab-203">Kveiktu á valkostinum **Skilgreina að nota Azure Resource Manager (ARM)**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-203">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="e03ab-204">Staðfestu að gildið **Azure áskrift AAD leigjandaléns (eða kenni)** sé rétt.</span><span class="sxs-lookup"><span data-stu-id="e03ab-204">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="e03ab-205">Hafðu samband við Azure áskriftarstjórann þinn, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="e03ab-205">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="e03ab-206">Veljið **Næst**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-206">Select **Next**.</span></span>
1. <span data-ttu-id="e03ab-207">Fylgdu leiðbeiningunum á síðunni til að veita nauðsynlegum forritum aðgang að áskriftinni þinni.</span><span class="sxs-lookup"><span data-stu-id="e03ab-207">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="e03ab-208">Hafðu samband við Azure áskriftarstjórann þinn, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="e03ab-208">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="e03ab-209">Skráðu þig inn á [Azure-gáttina](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="e03ab-209">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="e03ab-210">Gakktu úr skugga um að rétt skráarsafn sé valið og síðan, í valmyndinni til vinstri, velurðu **Áskrift**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-210">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="e03ab-211">Finndu rétta áskrift á listanum og veldu hana.</span><span class="sxs-lookup"><span data-stu-id="e03ab-211">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="e03ab-212">Notaðu leitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="e03ab-212">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="e03ab-213">Í valmyndinni velurðu **Aðgangsstýring (IAM)**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-213">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="e03ab-214">Til hægri, undir **Bæta við hlutverkaúthlutun** velurðu **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-214">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="e03ab-215">Glugginn **Bæta við hlutverki** birtist.</span><span class="sxs-lookup"><span data-stu-id="e03ab-215">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="e03ab-216">Á svæðinu **Hlutverk**, veljið **Þátttakandi**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-216">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="e03ab-217">Í reitnum **Úthluta aðgangi að** notarðu sjálfgefið gildi, **Azure AD notandi, hópur eða þjónustustjóri**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-217">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="e03ab-218">Undir **Velja** slærðu inn **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-218">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="e03ab-219">Veldu **Virkjunarþjónusta Dynamics \[wsfed-enabled\]** í listanum.</span><span class="sxs-lookup"><span data-stu-id="e03ab-219">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="e03ab-220">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-220">Select **Save**.</span></span>

1. <span data-ttu-id="e03ab-221">Veljið **Næst**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-221">Select **Next**.</span></span>
1. <span data-ttu-id="e03ab-222">Fylgdu leiðbeiningunum á síðunni til að veita nauðsynlegum forritum aðgang að áskriftinni þinni.</span><span class="sxs-lookup"><span data-stu-id="e03ab-222">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="e03ab-223">Hafðu samband við Azure áskriftarstjórann þinn, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="e03ab-223">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="e03ab-224">Veljið **Næst**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-224">Select **Next**.</span></span>
1. <span data-ttu-id="e03ab-225">Í reitnum **Azure-svæðið** velurðu **Austur-BNA**, **Austur-BNA 2**, **Vestur-BNA** eða **Vestur-BNA 2**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-225">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="e03ab-226">Veldu **Tengjast**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-226">Select **Connect**.</span></span> <span data-ttu-id="e03ab-227">Azure tengið þitt ætti að birtast á listanum.</span><span class="sxs-lookup"><span data-stu-id="e03ab-227">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="e03ab-228">Flytjið inn grunnviðbótina Forskoðunarsýnishorn af Commerce</span><span class="sxs-lookup"><span data-stu-id="e03ab-228">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="e03ab-229">Fylgdu þessum skrefum til að flytja grunnviðbótina Forskoðunarsýnishorn Commerce inn í verkið.</span><span class="sxs-lookup"><span data-stu-id="e03ab-229">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="e03ab-230">Opnaðu heimasíðu fyrir verkefnið með því að velja heiti verkefnis efst.</span><span class="sxs-lookup"><span data-stu-id="e03ab-230">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="e03ab-231">Fylgið einu af eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="e03ab-231">Follow one of these steps:</span></span>

    - <span data-ttu-id="e03ab-232">Ef þú ert félagi skaltu velja reitinn **Eignasafn** lengst til hægri.</span><span class="sxs-lookup"><span data-stu-id="e03ab-232">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="e03ab-233">Ef þú ert viðskiptavinur velurðu **Eignasafn** í efstu valmyndinni.</span><span class="sxs-lookup"><span data-stu-id="e03ab-233">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="e03ab-234">Í listanum til vinstri skaltu velja **Virkjanlegur hugbúnaðarpakki**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-234">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="e03ab-235">Velja **Innflutningur**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-235">Select **Import**.</span></span>
1. <span data-ttu-id="e03ab-236">Undir **Samnýtt eignasafn** velurðu **Grunnviðbótin Forskoðunarsýnishorn af Commerce** af eignalistanum.</span><span class="sxs-lookup"><span data-stu-id="e03ab-236">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="e03ab-237">Veldu **Tína til**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-237">Select **Pick**.</span></span> <span data-ttu-id="e03ab-238">Þér verður beint aftur í eignasafnið og þú ættir að sjá viðbótina á listanum.</span><span class="sxs-lookup"><span data-stu-id="e03ab-238">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="e03ab-239">Eftirfarandi mynd sýnir aðgerðir sem þarf að grípa til á LCS-síðunni **Eignasafn**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-239">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![Innflutningur á grunnviðbótinni Forskoðunarsýnishorn af Commerce](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="e03ab-241">Virkjaðu umhverfið</span><span class="sxs-lookup"><span data-stu-id="e03ab-241">Deploy the environment</span></span>

<span data-ttu-id="e03ab-242">Til að virkja umhverfið skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="e03ab-242">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="e03ab-243">Þú gætir ekki þurft að klára skref 6, 7 og / eða 8 því að síðum sem hafa einn valkost er sleppt.</span><span class="sxs-lookup"><span data-stu-id="e03ab-243">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="e03ab-244">Þegar þú ert í sýninni **Færibreytur umhverfis** skaltu staðfesta að textinn **Dynamics 365 Commerce (Forskoðun) - Demo (10.0.6 með verkvangsuppfærslu 30)** birtist beint fyrir ofan reitinn **Heiti umhverfis**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-244">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce (Preview) - Demo (10.0.6 with Platform update 30)** appears directly above the **Environment name** field.</span></span> <span data-ttu-id="e03ab-245">Sjá myndina sem birtist eftir 8. skref.</span><span class="sxs-lookup"><span data-stu-id="e03ab-245">See the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="e03ab-246">Í efstu valmyndinni velurðu **Umhverfi í skýi**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-246">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="e03ab-247">Veldu **Bæta við** til að bæta við umhverfi.</span><span class="sxs-lookup"><span data-stu-id="e03ab-247">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="e03ab-248">Í reitnum **Útgáfa forrits** velurðu **10.0.6**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-248">In the **Application version** field, select **10.0.6**.</span></span>
1. <span data-ttu-id="e03ab-249">Í reitnum **Útgáfa verkvangs** velurðu **Uppfærsla verkvangs 30**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-249">In the **Platform version** field, select **Platform Update 30**.</span></span>

    ![Val á forrita- og verkvangsútgáfum](./media/project1.png)

1. <span data-ttu-id="e03ab-251">Veljið **Næst**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-251">Select **Next**.</span></span>
1. <span data-ttu-id="e03ab-252">Veldu **Kynning** grannfræði umhverfis.</span><span class="sxs-lookup"><span data-stu-id="e03ab-252">Select **Demo** as the environment topology.</span></span>

    ![Val á grannfræði umhverfis 1](./media/project2.png)

1. <span data-ttu-id="e03ab-254">Veldu **Dynamics 365 Commerce (Forskoðun) - Kynning** sem grannfræði umhverfis.</span><span class="sxs-lookup"><span data-stu-id="e03ab-254">Select **Dynamics 365 Commerce (Preview) - Demo** as the environment topology.</span></span> <span data-ttu-id="e03ab-255">Ef þú stilltir upp eitt Azure-tengi áður verður það notað fyrir þetta umhverfi.</span><span class="sxs-lookup"><span data-stu-id="e03ab-255">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="e03ab-256">Ef þú stilltir mörg Azure-tengi geturðu valið hvaða tengi á að nota: **Austur-BNA**, **Austur-BNA 2**, **Vestur-BNA** eða **Vestur-BNA 2**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-256">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="e03ab-257">(Til að fá bestan heildarárangur mælum við með að þú veljir **Vestur-BNA 2**.)</span><span class="sxs-lookup"><span data-stu-id="e03ab-257">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![Val á grannfræði umhverfis 2](./media/project3.png)

1. <span data-ttu-id="e03ab-259">Á síðunni **Setja upp umhverfi** slærðu inn umhverfisheiti.</span><span class="sxs-lookup"><span data-stu-id="e03ab-259">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="e03ab-260">Hafðu ítarlegar stillingar óbreyttar.</span><span class="sxs-lookup"><span data-stu-id="e03ab-260">Leave the advanced settings as they are.</span></span>

    ![Setja upp umhverfissíðu](./media/project4.png)

1. <span data-ttu-id="e03ab-262">Stilltu VM stærð eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="e03ab-262">Adjust the VM size as required.</span></span> <span data-ttu-id="e03ab-263">(Við mælum með VM birgðaeiningunni \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="e03ab-263">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="e03ab-264">Skoðaðu verðlagningu og leyfisskilmála og veldu síðan gátreitinn til að gefa til kynna að þú samþykki þá.</span><span class="sxs-lookup"><span data-stu-id="e03ab-264">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="e03ab-265">Veljið **Næst**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-265">Select **Next**.</span></span>
1. <span data-ttu-id="e03ab-266">Á staðfestingarsíðunni staðfestirðu að upplýsingarnar séu réttar og smellir svo á **Setja upp**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-266">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="e03ab-267">Þú munt fara aftur í gluggann **Umhverfi í skýi** og umhverfi þitt ætti að birtast á listanum.</span><span class="sxs-lookup"><span data-stu-id="e03ab-267">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="e03ab-268">Umbeðið umhverfi þitt birtist í biðröð og síðan er það notað.</span><span class="sxs-lookup"><span data-stu-id="e03ab-268">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="e03ab-269">Það tekur nokkurn tíma að klára vinnuflæði umhverfisins.</span><span class="sxs-lookup"><span data-stu-id="e03ab-269">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="e03ab-270">Athugaðu því aftur eftir um það bil sex til níu tíma.</span><span class="sxs-lookup"><span data-stu-id="e03ab-270">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="e03ab-271">Áður en lengra er haldið skaltu ganga úr skugga um að staða umhverfisins sé **Uppsett**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-271">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-rcsu"></a><span data-ttu-id="e03ab-272">Frumstilla RCSU</span><span class="sxs-lookup"><span data-stu-id="e03ab-272">Initialize RCSU</span></span>

<span data-ttu-id="e03ab-273">Fylgið eftirfarandi skrefum til að hefja tilboðsbeiðnina.</span><span class="sxs-lookup"><span data-stu-id="e03ab-273">To initialize RCSU, follow these steps.</span></span>

1. <span data-ttu-id="e03ab-274">Í glugganum **Umhverfi í skýi** velurðu umhverfi þitt af listanum.</span><span class="sxs-lookup"><span data-stu-id="e03ab-274">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="e03ab-275">Í umhverfissýninni til hægri skaltu velja **Nánari upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-275">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="e03ab-276">Umhverfisupplýsingaskjárinn birtist.</span><span class="sxs-lookup"><span data-stu-id="e03ab-276">The environment details view appears.</span></span>
1. <span data-ttu-id="e03ab-277">Undir **Eiginleikar umhverfis** velurðu **Stjórna**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-277">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="e03ab-278">Á flipanum **Retail** velurðu **Frumstilla**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-278">On the **Retail** tab, select **Initialize**.</span></span> <span data-ttu-id="e03ab-279">Skjár RCSU frumstillingarifæribreyta birtist.</span><span class="sxs-lookup"><span data-stu-id="e03ab-279">The RCSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="e03ab-280">Í reitnum **Svæði** velurðu **Austur-BNA**, **Austur-BNA 2**, **Vestur-BNA** eða **Vestur-BNA 2**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-280">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="e03ab-281">Í reitnum **Útgáfa** velurðu **Tilgreina útgáfu** á listanum og tilgreinir síðan **9.16.19262.5** í reitnum sem birtist.</span><span class="sxs-lookup"><span data-stu-id="e03ab-281">In the **Version** field, select **Specify a version** in the list, and then specify **9.16.19262.5** in the field that appears.</span></span> <span data-ttu-id="e03ab-282">Vertu viss um að tilgreina nákvæma útgáfu sem er tilgreind hér.</span><span class="sxs-lookup"><span data-stu-id="e03ab-282">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="e03ab-283">Annars verður þú að uppfæra RCSU í réttri útgáfu síðar.</span><span class="sxs-lookup"><span data-stu-id="e03ab-283">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="e03ab-284">Kveiktu á valkostinum **Nota viðbót**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-284">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="e03ab-285">Á listanum yfir viðbætur velurðu **Grunnviðbótin Forskoðunarsýnishorn af Commerce**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-285">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="e03ab-286">Veldu **Frumstilla**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-286">Select **Initialize**.</span></span>
1. <span data-ttu-id="e03ab-287">Á staðfestingarsíðunni staðfestirðu að upplýsingarnar séu réttar og smellir svo á **Já**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-287">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="e03ab-288">Þér er snúið aftur á skjáinn **Smásölustjórnun** þar sem flipinn **Retail** er valinn.</span><span class="sxs-lookup"><span data-stu-id="e03ab-288">You're returned to the **Retail management** view, where the **Retail** tab is selected.</span></span> <span data-ttu-id="e03ab-289">RCSU þinn hefur verið í biðröð vegna úthlutunar.</span><span class="sxs-lookup"><span data-stu-id="e03ab-289">Your RCSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="e03ab-290">Áður en lengra er haldið skaltu ganga úr skugga um að staða RCSU sé **Tókst**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-290">Before you continue, make sure that the status of your RCSU is **Success**.</span></span> <span data-ttu-id="e03ab-291">Frumstilling tekur um það bil tvær til fimm klukkustundir.</span><span class="sxs-lookup"><span data-stu-id="e03ab-291">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="e03ab-292">Frumstilla rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="e03ab-292">Initialize e-Commerce</span></span>

<span data-ttu-id="e03ab-293">Fylgið eftirfarandi skrefum til að frumstilla e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="e03ab-293">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="e03ab-294">Á flipanum **e-Commerce (forskoðun)** skoðarðu samþykki fyrir forskoðun og velir síðan **Uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-294">On the **e-Commerce (Preview)** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="e03ab-295">Í reitnum **Leigjandaheiti í e-Commerce** færirðu inn heiti.</span><span class="sxs-lookup"><span data-stu-id="e03ab-295">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="e03ab-296">Hafðu þó í huga að þetta heiti mun birtast í sumum slóðum sem vísa til netverslunartilviksins.</span><span class="sxs-lookup"><span data-stu-id="e03ab-296">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="e03ab-297">Í reitnum **Heiti Retail Cloud Scale Unit** velurðu þitt RCSU á listanum.</span><span class="sxs-lookup"><span data-stu-id="e03ab-297">In the **Retail cloud scale unit name** field, select your RCSU in the list.</span></span> <span data-ttu-id="e03ab-298">(Listinn ætti aðeins að hafa einn valkost.)</span><span class="sxs-lookup"><span data-stu-id="e03ab-298">(The list should have only one option.)</span></span>

    <span data-ttu-id="e03ab-299">Reiturinn **Landafræði rafrænna viðskipta** er stilltur sjálfkrafa og ekki er hægt að breyta gildinu.</span><span class="sxs-lookup"><span data-stu-id="e03ab-299">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="e03ab-300">Veldu **Næst** til að halda áfram.</span><span class="sxs-lookup"><span data-stu-id="e03ab-300">Select **Next** to continue.</span></span>
1. <span data-ttu-id="e03ab-301">Í reitnum **Studd hýsilheiti** slærðu inn gilt lén, eins og `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="e03ab-301">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="e03ab-302">Í reitnum **AAD-öryggishópur fyrir kerfisstjóra** slærðu inn fyrstu stafina í nafni öryggishópsins sem þú vilt nota.</span><span class="sxs-lookup"><span data-stu-id="e03ab-302">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="e03ab-303">Veldu stækkunarglerstáknið til að birta leitarniðurstöður.</span><span class="sxs-lookup"><span data-stu-id="e03ab-303">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="e03ab-304">Velja öryggisflokk af listanum.</span><span class="sxs-lookup"><span data-stu-id="e03ab-304">Select a security group from the list.</span></span>
2.  <span data-ttu-id="e03ab-305">Í reitnum **AAD-öryggishópur stjórnanda fyrir einkunnir og umsagnir** slærðu inn fyrstu stafina í nafni öryggishópsins sem þú vilt nota.</span><span class="sxs-lookup"><span data-stu-id="e03ab-305">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="e03ab-306">Veldu stækkunarglerstáknið til að birta leitarniðurstöður.</span><span class="sxs-lookup"><span data-stu-id="e03ab-306">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="e03ab-307">Velja öryggisflokk af listanum.</span><span class="sxs-lookup"><span data-stu-id="e03ab-307">Select a security group from the list.</span></span>
1. <span data-ttu-id="e03ab-308">Hafðu kveikt á valkostinum **Virkja einkunna- og umsagnaþjónustu**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-308">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="e03ab-309">Ef þú hefur þegar lokið Microsoft Azure Active Directory (Azure AD) samþykkisskref eins og lýst er í hlutanum „Veita aðgang að forritum með rafræn viðskipti“ skaltu velja gátreitinn til að staðfesta samþykki þitt.</span><span class="sxs-lookup"><span data-stu-id="e03ab-309">If you have already completed the Microsoft Azure Active Directory (Azure AD) consent step as described in the "Grant access to e-Commerce applications" section, select the check box to confirm your consent.</span></span> <span data-ttu-id="e03ab-310">Ef þú hefur ekki enn lokið þessu skrefi þarftu að gera það áður en þú heldur áfram með frumstillinguna.</span><span class="sxs-lookup"><span data-stu-id="e03ab-310">If you have not yet completed this step, you need to do that before proceeding with the initialization.</span></span> <span data-ttu-id="e03ab-311">Veldu tengilinn í textanum við hliðina á gátreitnum til að opna samþykkisgluggann og ljúka skrefinu.</span><span class="sxs-lookup"><span data-stu-id="e03ab-311">Select the link within the text next to the check box to open the consent dialog box and complete the step.</span></span>
1. <span data-ttu-id="e03ab-312">Veldu **Frumstilla**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-312">Select **Initialize**.</span></span> <span data-ttu-id="e03ab-313">Þér er snúið aftur á skjáinn **Smásölustjórnun** þar sem flipinn **rafræn viðskipti (forsýning)** er valinn.</span><span class="sxs-lookup"><span data-stu-id="e03ab-313">You're returned to the **Retail management** view, where the **e-Commerce (Preview)** tab is selected.</span></span> <span data-ttu-id="e03ab-314">Frumstilling rafrænna viðskipta er hafin.</span><span class="sxs-lookup"><span data-stu-id="e03ab-314">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="e03ab-315">Áður en lengra er haldið skaltu bíða þar til staða frumstillingar í netverslun er **Frumstilling tókst**.</span><span class="sxs-lookup"><span data-stu-id="e03ab-315">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="e03ab-316">Undir **Krækjur** neðst til hægri, skrifaðu vefslóðirnar fyrir eftirfarandi tengla:</span><span class="sxs-lookup"><span data-stu-id="e03ab-316">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="e03ab-317">**rafræn viðskipti síða** - Hlekkurinn á rótina á netverslunarsíðunni þinni.</span><span class="sxs-lookup"><span data-stu-id="e03ab-317">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="e03ab-318">**stjórnunartæki fyrir e-verslun** - Hlekkurinn að stjórnunartólinu.</span><span class="sxs-lookup"><span data-stu-id="e03ab-318">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="e03ab-319">Stuðningur við forskoðunarumhverfi fyrir Commerce</span><span class="sxs-lookup"><span data-stu-id="e03ab-319">Commerce preview environment support</span></span>

<span data-ttu-id="e03ab-320">Ef þú lendir í vandræðum meðan þú lýkur úthlutunarskrefunum skaltu fara á [Microsoft Dynamics 365 Commerce Forskoðun Yammer hópur](https://aka.ms/Dynamics365CommercePreviewYammer) fyrir aðstoð.</span><span class="sxs-lookup"><span data-stu-id="e03ab-320">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

<span data-ttu-id="e03ab-321">Ef þú lendir í vandamálum þegar þú reynir að fá aðgang að Yammer-hóp geturðu haft samband við Microsoft með tölvupósti á <Dynamics365Commerce@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="e03ab-321">If you experience issues when you try to access the Yammer group, you can contact Microsoft by email at <Dynamics365Commerce@microsoft.com>.</span></span> <span data-ttu-id="e03ab-322">Ekki er fylgst með þessu netfangi með virkum hætti.</span><span class="sxs-lookup"><span data-stu-id="e03ab-322">This email address isn't actively monitored.</span></span> <span data-ttu-id="e03ab-323">Því má búast við seinkun á viðbrögðum.</span><span class="sxs-lookup"><span data-stu-id="e03ab-323">Therefore, expect a delay in the response.</span></span>

## <a name="next-steps"></a><span data-ttu-id="e03ab-324">Næstu skref</span><span class="sxs-lookup"><span data-stu-id="e03ab-324">Next steps</span></span>

<span data-ttu-id="e03ab-325">Til að halda áfram úthlutunar- og stillingarferli forskoðunarumhverfis Commerce eftir að því hefur verið úthlutað skal sjá [Stilla forskoðunarumhverfi Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="e03ab-325">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e03ab-326">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="e03ab-326">Additional resources</span></span>

[<span data-ttu-id="e03ab-327">Yfirlit yfir forskoðunarumhverfi Commerce</span><span class="sxs-lookup"><span data-stu-id="e03ab-327">Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="e03ab-328">Skilgreina forskoðunarumhverfi Commerce</span><span class="sxs-lookup"><span data-stu-id="e03ab-328">Configure a Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="e03ab-329">Stilltu valfrjálsa eiginleika fyrir forsýningarumhverfi Commerce</span><span class="sxs-lookup"><span data-stu-id="e03ab-329">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="e03ab-330">Algengar spurningar um forskoðunarumhverfi Commerce</span><span class="sxs-lookup"><span data-stu-id="e03ab-330">Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="e03ab-331">Microsoft Dynamics Lifecycle Services (LSC)</span><span class="sxs-lookup"><span data-stu-id="e03ab-331">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="e03ab-332">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="e03ab-332">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="e03ab-333">Microsoft Azure-gátt</span><span class="sxs-lookup"><span data-stu-id="e03ab-333">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="e03ab-334">Dynamics 365 Commerce vefsvæði</span><span class="sxs-lookup"><span data-stu-id="e03ab-334">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="e03ab-335">Hjálpartilföng fyrir Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="e03ab-335">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
