---
title: Úthluta forskoðunarumhverfi fyrir Dynamics 365 Commerce
description: Þetta efni útskýrir hvernig á að úthluta forskoðunarumhverfi Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 06/02/2020
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
ms.openlocfilehash: c109c2326cf01739255b49587c15aa34ad884f6a
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426466"
---
# <a name="provision-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="97f02-103">Úthluta forskoðunarumhverfi fyrir Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="97f02-103">Provision a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="97f02-104">Þetta efni útskýrir hvernig á að úthluta forskoðunarumhverfi Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="97f02-104">This topic explains how to provision a Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="97f02-105">Áður en þú byrjar, mælum við með að þú gríptir skjótt í gegnum þetta efni til að fá hugmynd um hvað ferlið krefst.</span><span class="sxs-lookup"><span data-stu-id="97f02-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="97f02-106">Ef þér hefur ekki verið veittur aðgangur að forskoðun Dynamics 365 Commerce ennþá geturðu beðið um forsýningaraðgang af vefsíðunni [Dynamics 365 Commerce](https://aka.ms/Dynamics365CommerceWebsite).</span><span class="sxs-lookup"><span data-stu-id="97f02-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Dynamics 365 Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="97f02-107">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="97f02-107">Overview</span></span>

<span data-ttu-id="97f02-108">Til að úthluta forskoðunarumhverfi Commerce með góðum árangri verður þú að búa til verk sem hefur tiltekið vöruheiti og tegund.</span><span class="sxs-lookup"><span data-stu-id="97f02-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="97f02-109">Umhverfið og Commerce Scale Unit (CSU) eru einnig með nokkrar ákveðnar færibreytur sem verður að nota þegar rafrænum viðskiptum er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="97f02-109">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="97f02-110">Leiðbeiningarnar í þessu efni lýsa öllum nauðsynlegum skrefum sem þarf til að ljúka úthlutun og breytunum sem þú verður að nota.</span><span class="sxs-lookup"><span data-stu-id="97f02-110">The instructions in this topic describe all the steps required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="97f02-111">Eftir árangursríka úthlutun á forskoðunarumhverfi Commerce þarf að ljúka nokkrum eftirúthlutunarskrefum til að undirbúa það.</span><span class="sxs-lookup"><span data-stu-id="97f02-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="97f02-112">Sum skref eru valkvæð, eftir þeim þáttum kerfisins þú vilt meta.</span><span class="sxs-lookup"><span data-stu-id="97f02-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="97f02-113">Þú getur alltaf klárað valfrjálsu skrefin seinna.</span><span class="sxs-lookup"><span data-stu-id="97f02-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="97f02-114">Fyrir upplýsingar um hvernig skuli stilla þér forskoðunarumhverfi Commerce eftir að því hefur verið úthlutað skal sjá [Stilla forskoðunarumhverfi Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="97f02-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="97f02-115">Upplýsingar um hvernig eigi að stilla valfrjálsa eiginleika fyrir forskoðunarumhverfi Commerce er að finna í [Stilla valfrjálsa eiginleika fyrir forskoðunarumhverfi Commerce](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="97f02-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="97f02-116">Láttu Microsoft vita ef þú hefur einhverjar spurningar um ráðstöfunarskrefin eða lendir í einhverjum vandræðum í [Microsoft Dynamics 365 Commerce forskoða Yammer hóp](https://aka.ms/Dynamics365CommercePreviewYammer).</span><span class="sxs-lookup"><span data-stu-id="97f02-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="97f02-117">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="97f02-117">Prerequisites</span></span>

<span data-ttu-id="97f02-118">Eftirfarandi forsendur verða að vera til áður en þú getur veitt forskoðunarumhverfi Commerce:</span><span class="sxs-lookup"><span data-stu-id="97f02-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="97f02-119">Þú hefur aðgang að Microsoft Dynamics Lifecycle Services (LCS)-gáttinni.</span><span class="sxs-lookup"><span data-stu-id="97f02-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="97f02-120">Þú ert fyrirliggjandi félagi eða viðskiptavinur Microsoft Dynamics 365 og getur stofnað Dynamics 365 Commerce verk.</span><span class="sxs-lookup"><span data-stu-id="97f02-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="97f02-121">Þú fékkst samþykkt inn í Dynamics 365 Commerce Forskoða kerfi.</span><span class="sxs-lookup"><span data-stu-id="97f02-121">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="97f02-122">Þú hefur nauðsynlegar heimildir til að búa til verk fyrir **Flytja, búa til lausnir og læra**.</span><span class="sxs-lookup"><span data-stu-id="97f02-122">You have the required permissions to create a project for **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="97f02-123">Þú ert meðlimur í hlutverkinu **Umhverfisstjóri** eða **Eigandi verks** í verkinu þar sem þú munt að sjá um umhverfið</span><span class="sxs-lookup"><span data-stu-id="97f02-123">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="97f02-124">Þú hefur stjórnandaaðgang að Microsoft Azure-áskriftinni þinni eða ert í sambandi við áskriftarstjórann sem getur lokið skrefunum tveimur sem krefjast stjórnunarheimilda fyrir þína hönd.</span><span class="sxs-lookup"><span data-stu-id="97f02-124">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="97f02-125">Þú hefur leigjandakenni þitt fyrir Azure Active Directory (Azure AD) í boði.</span><span class="sxs-lookup"><span data-stu-id="97f02-125">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="97f02-126">Þú hefur búið til Azure AD-öryggishóp sem hægt er að nota sem kerfisstjórahóp netverslunar og þú ert með kenni hans tiltækt.</span><span class="sxs-lookup"><span data-stu-id="97f02-126">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="97f02-127">Þú hefur búið til Azure AD-öryggishóp sem hægt er að nota sem stjórnandahóp einkunna og umsagna og þú ert með kenni hans tiltækt.</span><span class="sxs-lookup"><span data-stu-id="97f02-127">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="97f02-128">(Þessi öryggishópur getur verið sá sami og kerfisstjórinn fyrir netkerfi.)</span><span class="sxs-lookup"><span data-stu-id="97f02-128">(This security group can be the same as the e-Commerce system admin group.)</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="97f02-129">Úthluta forskoðunarumhverfi þínu fyrir Commerce</span><span class="sxs-lookup"><span data-stu-id="97f02-129">Provision your Commerce preview environment</span></span>

<span data-ttu-id="97f02-130">Þessar aðferðir útskýra hvernig á að bjóða upp á forskoðunarumhverfi Commerce.</span><span class="sxs-lookup"><span data-stu-id="97f02-130">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="97f02-131">Þegar þú hefur lokið við þau er forskoðunarumhverfi Commerce tilbúið til uppsetningar.</span><span class="sxs-lookup"><span data-stu-id="97f02-131">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="97f02-132">Allar þær aðgerðir sem er lýst hér fara fram í LCS-gáttinni.</span><span class="sxs-lookup"><span data-stu-id="97f02-132">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="97f02-133">Forskoðunaraðgangur er bundinn við LCS-reikninginn og -fyrirtækið sem þú tilgreindir í forskoðunarforriti Commerce.</span><span class="sxs-lookup"><span data-stu-id="97f02-133">Preview access is tied to the LCS account and organization that you specified in your Commerce preview application.</span></span> <span data-ttu-id="97f02-134">Þú verður að nota sama reikning til að veita forskoðunarumhverfi Commerce.</span><span class="sxs-lookup"><span data-stu-id="97f02-134">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="97f02-135">Ef þú þarft að nota annan LCS-reikning eða -leigjanda fyrir forskoðunarumhverfi Commerce verður þú að láta Microsoft í té þessar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="97f02-135">If you need to use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="97f02-136">Sjá upplýsingar um tengilið í kaflanum [Stuðningur við forskoðunarumhverfi í Commerce](#commerce-preview-environment-support) síðar í þessu efni.</span><span class="sxs-lookup"><span data-stu-id="97f02-136">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="97f02-137">Staðfestu að forskoðunaraðgerðir séu tiltækar og virkjaðar í LCS</span><span class="sxs-lookup"><span data-stu-id="97f02-137">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="97f02-138">Til að staðfesta að forskoðunaraðgerðir séu tiltækar og virkjaðar í LCS skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="97f02-138">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="97f02-139">Skráðu þig inn í [LCS-gáttina](https://lcs.dynamics.com) með því að nota sama LCS-reikning og þú notaðir til að biðja um aðgang að forskoðuninni.</span><span class="sxs-lookup"><span data-stu-id="97f02-139">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="97f02-140">Flettu alla leið til hægri á heimasíðu LCS og veldu reitinn **Forskoðun aðgerðastjórnunar**.</span><span class="sxs-lookup"><span data-stu-id="97f02-140">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![Stjórnun forskoðunarreits](./media/preview1.png)

1. <span data-ttu-id="97f02-142">Skrunaðu niður að **Einkaforskoðunareiginleikar** og staðfestu að eftirfarandi aðgerðir séu tiltækar og virkjaðar:</span><span class="sxs-lookup"><span data-stu-id="97f02-142">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="97f02-143">Mat á rafrænum viðskipta</span><span class="sxs-lookup"><span data-stu-id="97f02-143">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="97f02-144">Forritsumhverfi forskoðunar á Commerce</span><span class="sxs-lookup"><span data-stu-id="97f02-144">Commerce Preview Program Environments</span></span>

    ![Einkaforskoðunareiginleikar](./media/preview2.png)

1. <span data-ttu-id="97f02-146">Ef þessir eiginleikar birtast ekki á listanum skaltu hafa samband við Microsoft og gefa upp vinnupóstfang þitt, LCS reikning og upplýsingar um leigjanda.</span><span class="sxs-lookup"><span data-stu-id="97f02-146">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="97f02-147">Sjá upplýsingar um tengilið í kaflanum [Stuðningur við forskoðunarumhverfi í Commerce](#commerce-preview-environment-support).</span><span class="sxs-lookup"><span data-stu-id="97f02-147">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="97f02-148">Stofna nýtt verk</span><span class="sxs-lookup"><span data-stu-id="97f02-148">Create a new project</span></span>

<span data-ttu-id="97f02-149">Til að stofna nýtt verk í LSC skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="97f02-149">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="97f02-150">Á heimasíðu LCS velurðu plúsmerkið (**+**) til að búa til verk.</span><span class="sxs-lookup"><span data-stu-id="97f02-150">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="97f02-151">Fylgdu einu af þessum skrefum á hægri glugganum:</span><span class="sxs-lookup"><span data-stu-id="97f02-151">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="97f02-152">Ef þú ert félagi skaltu velja **Flytja, búa til lausnir og læra**.</span><span class="sxs-lookup"><span data-stu-id="97f02-152">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="97f02-153">Ef þú ert viðskiptavinur skaltu velja **Væntanleg forsala**.</span><span class="sxs-lookup"><span data-stu-id="97f02-153">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="97f02-154">Færðu inn heiti, lýsingu og iðnað.</span><span class="sxs-lookup"><span data-stu-id="97f02-154">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="97f02-155">Í reitnum **Heiti afurðar** velurðu **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="97f02-155">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="97f02-156">Í reitnum **Útgáfa afurðar** velurðu **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="97f02-156">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="97f02-157">Í reitnum **Aðferð** velurðu **Dynamics Retail útfærsluaðferð**.</span><span class="sxs-lookup"><span data-stu-id="97f02-157">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="97f02-158">Valfrjálst: Hægt er að flytja inn hlutverk og notendur úr fyrirliggjandi verki.</span><span class="sxs-lookup"><span data-stu-id="97f02-158">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="97f02-159">Velja **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="97f02-159">Select **Create**.</span></span> <span data-ttu-id="97f02-160">Verksýnin birtist.</span><span class="sxs-lookup"><span data-stu-id="97f02-160">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="97f02-161">Bættu Azure-tengingunni við</span><span class="sxs-lookup"><span data-stu-id="97f02-161">Add the Azure Connector</span></span>

<span data-ttu-id="97f02-162">Fylgdu þessum skrefum til að bæta Azure Connector við LCS-verkið.</span><span class="sxs-lookup"><span data-stu-id="97f02-162">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="97f02-163">Fylgið einu af eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="97f02-163">Follow one of these steps:</span></span>

    - <span data-ttu-id="97f02-164">Ef þú ert félagi skaltu velja reitinn **Stillingar verks** lengst til hægri.</span><span class="sxs-lookup"><span data-stu-id="97f02-164">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="97f02-165">Ef þú ert viðskiptavinur velurðu **Stillingar verks** í efstu valmyndinni.</span><span class="sxs-lookup"><span data-stu-id="97f02-165">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="97f02-166">Velja **Azure-tengingar**.</span><span class="sxs-lookup"><span data-stu-id="97f02-166">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="97f02-167">Veldu **Bæta við** til að bæta við Azure-tengingu.</span><span class="sxs-lookup"><span data-stu-id="97f02-167">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="97f02-168">Færið inn heiti.</span><span class="sxs-lookup"><span data-stu-id="97f02-168">Enter a name.</span></span>
1. <span data-ttu-id="97f02-169">Sláðu inn Azure-áskriftarkenni þitt.</span><span class="sxs-lookup"><span data-stu-id="97f02-169">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="97f02-170">Kveiktu á valkostinum **Skilgreina að nota Azure Resource Manager (ARM)**.</span><span class="sxs-lookup"><span data-stu-id="97f02-170">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="97f02-171">Staðfestu að gildið **Azure áskrift AAD leigjandaléns (eða kenni)** sé rétt.</span><span class="sxs-lookup"><span data-stu-id="97f02-171">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="97f02-172">Hafðu samband við Azure áskriftarstjórann þinn, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="97f02-172">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="97f02-173">Veljið **Næst**.</span><span class="sxs-lookup"><span data-stu-id="97f02-173">Select **Next**.</span></span>
1. <span data-ttu-id="97f02-174">Fylgdu leiðbeiningunum á síðunni til að veita nauðsynlegum forritum aðgang að áskriftinni þinni.</span><span class="sxs-lookup"><span data-stu-id="97f02-174">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="97f02-175">Hafðu samband við Azure áskriftarstjórann þinn, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="97f02-175">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="97f02-176">Skráðu þig inn á [Azure-gáttina](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="97f02-176">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="97f02-177">Gakktu úr skugga um að rétt skráarsafn sé valið og síðan, í valmyndinni til vinstri, velurðu **Áskrift**.</span><span class="sxs-lookup"><span data-stu-id="97f02-177">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="97f02-178">Finndu rétta áskrift á listanum og veldu hana.</span><span class="sxs-lookup"><span data-stu-id="97f02-178">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="97f02-179">Notaðu leitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="97f02-179">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="97f02-180">Í valmyndinni velurðu **Aðgangsstýring (IAM)**.</span><span class="sxs-lookup"><span data-stu-id="97f02-180">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="97f02-181">Til hægri, undir **Bæta við hlutverkaúthlutun** velurðu **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="97f02-181">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="97f02-182">Glugginn **Bæta við hlutverki** birtist.</span><span class="sxs-lookup"><span data-stu-id="97f02-182">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="97f02-183">Á svæðinu **Hlutverk**, veljið **Þátttakandi**.</span><span class="sxs-lookup"><span data-stu-id="97f02-183">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="97f02-184">Í reitnum **Úthluta aðgangi að** notarðu sjálfgefið gildi, **Azure AD notandi, hópur eða þjónustustjóri**.</span><span class="sxs-lookup"><span data-stu-id="97f02-184">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="97f02-185">Undir **Velja** slærðu inn **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span><span class="sxs-lookup"><span data-stu-id="97f02-185">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="97f02-186">Veldu **Virkjunarþjónusta Dynamics \[wsfed-enabled\]** í listanum.</span><span class="sxs-lookup"><span data-stu-id="97f02-186">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="97f02-187">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="97f02-187">Select **Save**.</span></span>

1. <span data-ttu-id="97f02-188">Veljið **Næst**.</span><span class="sxs-lookup"><span data-stu-id="97f02-188">Select **Next**.</span></span>
1. <span data-ttu-id="97f02-189">Fylgdu leiðbeiningunum á síðunni til að veita nauðsynlegum forritum aðgang að áskriftinni þinni.</span><span class="sxs-lookup"><span data-stu-id="97f02-189">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="97f02-190">Hafðu samband við Azure áskriftarstjórann þinn, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="97f02-190">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="97f02-191">Veljið **Næst**.</span><span class="sxs-lookup"><span data-stu-id="97f02-191">Select **Next**.</span></span>
1. <span data-ttu-id="97f02-192">Í reitnum **Azure-svæðið** velurðu **Austur-BNA**, **Austur-BNA 2**, **Vestur-BNA** eða **Vestur-BNA 2**.</span><span class="sxs-lookup"><span data-stu-id="97f02-192">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="97f02-193">Veldu **Tengjast**.</span><span class="sxs-lookup"><span data-stu-id="97f02-193">Select **Connect**.</span></span> <span data-ttu-id="97f02-194">Azure tengið þitt ætti að birtast á listanum.</span><span class="sxs-lookup"><span data-stu-id="97f02-194">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="97f02-195">Flytjið inn grunnviðbótina Forskoðunarsýnishorn af Commerce</span><span class="sxs-lookup"><span data-stu-id="97f02-195">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="97f02-196">Fylgdu þessum skrefum til að flytja grunnviðbótina Forskoðunarsýnishorn Commerce inn í verkið.</span><span class="sxs-lookup"><span data-stu-id="97f02-196">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="97f02-197">Opnaðu heimasíðu fyrir verkefnið með því að velja heiti verkefnis efst.</span><span class="sxs-lookup"><span data-stu-id="97f02-197">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="97f02-198">Fylgið einu af eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="97f02-198">Follow one of these steps:</span></span>

    - <span data-ttu-id="97f02-199">Ef þú ert félagi skaltu velja reitinn **Eignasafn** lengst til hægri.</span><span class="sxs-lookup"><span data-stu-id="97f02-199">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="97f02-200">Ef þú ert viðskiptavinur velurðu **Eignasafn** í efstu valmyndinni.</span><span class="sxs-lookup"><span data-stu-id="97f02-200">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="97f02-201">Í listanum til vinstri skaltu velja **Virkjanlegur hugbúnaðarpakki**.</span><span class="sxs-lookup"><span data-stu-id="97f02-201">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="97f02-202">Velja **Innflutningur**.</span><span class="sxs-lookup"><span data-stu-id="97f02-202">Select **Import**.</span></span>
1. <span data-ttu-id="97f02-203">Undir **Samnýtt eignasafn** velurðu **Grunnviðbótin Forskoðunarsýnishorn af Commerce** af eignalistanum.</span><span class="sxs-lookup"><span data-stu-id="97f02-203">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="97f02-204">Veldu **Tína til**.</span><span class="sxs-lookup"><span data-stu-id="97f02-204">Select **Pick**.</span></span> <span data-ttu-id="97f02-205">Þér verður beint aftur í eignasafnið og þú ættir að sjá viðbótina á listanum.</span><span class="sxs-lookup"><span data-stu-id="97f02-205">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="97f02-206">Eftirfarandi mynd sýnir aðgerðir sem þarf að grípa til á LCS-síðunni **Eignasafn**.</span><span class="sxs-lookup"><span data-stu-id="97f02-206">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![Innflutningur á grunnviðbótinni Forskoðunarsýnishorn af Commerce](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="97f02-208">Virkjaðu umhverfið</span><span class="sxs-lookup"><span data-stu-id="97f02-208">Deploy the environment</span></span>

<span data-ttu-id="97f02-209">Til að virkja umhverfið skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="97f02-209">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="97f02-210">Þú gætir ekki þurft að klára skref 6, 7 og / eða 8 því að síðum sem hafa einn valkost er sleppt.</span><span class="sxs-lookup"><span data-stu-id="97f02-210">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="97f02-211">Þegar þú ert í sýninni **Færibreytur umhverfis** skaltu staðfesta að textinn **Dynamics 365 Commerce - (Forskoðun) - Kynning (10.0.* x* með verkvangsuppfærslu *xx*)\*\* birtist beint fyrir ofan reitinn **Heiti umhverfis**.</span><span class="sxs-lookup"><span data-stu-id="97f02-211">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="97f02-212">Fyrir nánari upplýsingar, sjá myndina sem birtist eftir 8. skref.</span><span class="sxs-lookup"><span data-stu-id="97f02-212">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="97f02-213">Í efstu valmyndinni velurðu **Umhverfi í skýi**.</span><span class="sxs-lookup"><span data-stu-id="97f02-213">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="97f02-214">Veldu **Bæta við** til að bæta við umhverfi.</span><span class="sxs-lookup"><span data-stu-id="97f02-214">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="97f02-215">Í reitnum **Útgáfa forrits**, veldu nýjustu útgáfuna.</span><span class="sxs-lookup"><span data-stu-id="97f02-215">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="97f02-216">Ef þú hefur sérstaka þörf fyrir að velja aðra forritsútgáfu en nýjustu útgáfuna skaltu ekki velja útgáfu áður **10.0.8**.</span><span class="sxs-lookup"><span data-stu-id="97f02-216">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.8**.</span></span>
1. <span data-ttu-id="97f02-217">Í reitnum **Útgáfa verkvangs**, notarðu verkvangsútgáfuna sem er sjálfkrafa valin fyrir forritsútgáfuna sem þú valdir.</span><span class="sxs-lookup"><span data-stu-id="97f02-217">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Val á forrita- og verkvangsútgáfum](./media/project1.png)

1. <span data-ttu-id="97f02-219">Veljið **Næst**.</span><span class="sxs-lookup"><span data-stu-id="97f02-219">Select **Next**.</span></span>
1. <span data-ttu-id="97f02-220">Veldu **Kynning** grannfræði umhverfis.</span><span class="sxs-lookup"><span data-stu-id="97f02-220">Select **Demo** as the environment topology.</span></span>

    ![Val á grannfræði umhverfis 1](./media/project2.png)

1. <span data-ttu-id="97f02-222">Veldu **Dynamics 365 Commerce - Kynning** sem grannfræði umhverfis.</span><span class="sxs-lookup"><span data-stu-id="97f02-222">Select **Dynamics 365 Commerce - Demo** as the environment topology.</span></span> <span data-ttu-id="97f02-223">Ef þú stilltir upp eitt Azure-tengi áður verður það notað fyrir þetta umhverfi.</span><span class="sxs-lookup"><span data-stu-id="97f02-223">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="97f02-224">Ef þú stilltir mörg Azure-tengi geturðu valið hvaða tengi á að nota: **Austur-BNA**, **Austur-BNA 2**, **Vestur-BNA** eða **Vestur-BNA 2**.</span><span class="sxs-lookup"><span data-stu-id="97f02-224">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="97f02-225">(Til að fá bestan heildarárangur mælum við með að þú veljir **Vestur-BNA 2**.)</span><span class="sxs-lookup"><span data-stu-id="97f02-225">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![Val á grannfræði umhverfis 2](./media/project3.png)

1. <span data-ttu-id="97f02-227">Á síðunni **Setja upp umhverfi** slærðu inn umhverfisheiti.</span><span class="sxs-lookup"><span data-stu-id="97f02-227">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="97f02-228">Hafðu ítarlegar stillingar óbreyttar.</span><span class="sxs-lookup"><span data-stu-id="97f02-228">Leave the advanced settings as they are.</span></span>

    ![Setja upp umhverfissíðu](./media/project4.png)

1. <span data-ttu-id="97f02-230">Stilltu VM stærð eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="97f02-230">Adjust the VM size as required.</span></span> <span data-ttu-id="97f02-231">(Við mælum með VM birgðaeiningunni \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="97f02-231">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="97f02-232">Skoðaðu verðlagningu og leyfisskilmála og veldu síðan gátreitinn til að gefa til kynna að þú samþykki þá.</span><span class="sxs-lookup"><span data-stu-id="97f02-232">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="97f02-233">Veljið **Næst**.</span><span class="sxs-lookup"><span data-stu-id="97f02-233">Select **Next**.</span></span>
1. <span data-ttu-id="97f02-234">Á staðfestingarsíðunni staðfestirðu að upplýsingarnar séu réttar og smellir svo á **Setja upp**.</span><span class="sxs-lookup"><span data-stu-id="97f02-234">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="97f02-235">Þú munt fara aftur í gluggann **Umhverfi í skýi** og umhverfi þitt ætti að birtast á listanum.</span><span class="sxs-lookup"><span data-stu-id="97f02-235">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="97f02-236">Umbeðið umhverfi þitt birtist í biðröð og síðan er það notað.</span><span class="sxs-lookup"><span data-stu-id="97f02-236">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="97f02-237">Það tekur nokkurn tíma að klára vinnuflæði umhverfisins.</span><span class="sxs-lookup"><span data-stu-id="97f02-237">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="97f02-238">Athugaðu því aftur eftir um það bil sex til níu tíma.</span><span class="sxs-lookup"><span data-stu-id="97f02-238">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="97f02-239">Áður en lengra er haldið skaltu ganga úr skugga um að staða umhverfisins sé **Uppsett**.</span><span class="sxs-lookup"><span data-stu-id="97f02-239">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="97f02-240">Frumstilla Commerce Scale Unit (ský)</span><span class="sxs-lookup"><span data-stu-id="97f02-240">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="97f02-241">Fylgið eftirfarandi skrefum til að hefja CSU.</span><span class="sxs-lookup"><span data-stu-id="97f02-241">To initialize CSU, follow these steps.</span></span>

1. <span data-ttu-id="97f02-242">Í glugganum **Umhverfi í skýi** velurðu umhverfi þitt af listanum.</span><span class="sxs-lookup"><span data-stu-id="97f02-242">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="97f02-243">Í umhverfissýninni til hægri skaltu velja **Nánari upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="97f02-243">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="97f02-244">Umhverfisupplýsingaskjárinn birtist.</span><span class="sxs-lookup"><span data-stu-id="97f02-244">The environment details view appears.</span></span>
1. <span data-ttu-id="97f02-245">Undir **Eiginleikar umhverfis** velurðu **Stjórna**.</span><span class="sxs-lookup"><span data-stu-id="97f02-245">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="97f02-246">Á flipanum **Commerce** velurðu **Frumstilla**.</span><span class="sxs-lookup"><span data-stu-id="97f02-246">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="97f02-247">Skjár CSU frumstillingarifæribreyta birtist.</span><span class="sxs-lookup"><span data-stu-id="97f02-247">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="97f02-248">Í reitnum **Svæði** velurðu **Austur-BNA**, **Austur-BNA 2**, **Vestur-BNA** eða **Vestur-BNA 2**.</span><span class="sxs-lookup"><span data-stu-id="97f02-248">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="97f02-249">Í reitnum **Útgáfa** velurðu **Tilgreina útgáfu** á listanum og tilgreinir síðan **9.18.20014.4** í reitnum sem birtist.</span><span class="sxs-lookup"><span data-stu-id="97f02-249">In the **Version** field, select **Specify a version** in the list, and then specify **9.18.20014.4** in the field that appears.</span></span> <span data-ttu-id="97f02-250">Vertu viss um að tilgreina nákvæma útgáfu sem er tilgreind hér.</span><span class="sxs-lookup"><span data-stu-id="97f02-250">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="97f02-251">Annars verður þú að uppfæra RCSU í réttri útgáfu síðar.</span><span class="sxs-lookup"><span data-stu-id="97f02-251">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="97f02-252">Kveiktu á valkostinum **Nota viðbót**.</span><span class="sxs-lookup"><span data-stu-id="97f02-252">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="97f02-253">Á listanum yfir viðbætur velurðu **Grunnviðbótin Forskoðunarsýnishorn af Commerce**.</span><span class="sxs-lookup"><span data-stu-id="97f02-253">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="97f02-254">Veldu **Frumstilla**.</span><span class="sxs-lookup"><span data-stu-id="97f02-254">Select **Initialize**.</span></span>
1. <span data-ttu-id="97f02-255">Á staðfestingarsíðunni staðfestirðu að upplýsingarnar séu réttar og smellir svo á **Já**.</span><span class="sxs-lookup"><span data-stu-id="97f02-255">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="97f02-256">Skjárinn **Commerce-stjórnun** birtist aftur, þar sem flipinn **Commerce** er valinn.</span><span class="sxs-lookup"><span data-stu-id="97f02-256">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="97f02-257">CSU þinn hefur verið í biðröð vegna úthlutunar.</span><span class="sxs-lookup"><span data-stu-id="97f02-257">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="97f02-258">Áður en lengra er haldið skaltu ganga úr skugga um að staða CSU sé **Tókst**.</span><span class="sxs-lookup"><span data-stu-id="97f02-258">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="97f02-259">Frumstilling tekur um það bil tvær til fimm klukkustundir.</span><span class="sxs-lookup"><span data-stu-id="97f02-259">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="97f02-260">Frumstilla rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="97f02-260">Initialize e-Commerce</span></span>

<span data-ttu-id="97f02-261">Fylgið eftirfarandi skrefum til að frumstilla e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="97f02-261">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="97f02-262">Á flipanum **e-Commerce** skoðarðu samþykki fyrir forskoðun og velir síðan **Uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="97f02-262">On the **e-Commerce** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="97f02-263">Í reitnum **Leigjandaheiti í e-Commerce** færirðu inn heiti.</span><span class="sxs-lookup"><span data-stu-id="97f02-263">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="97f02-264">Hafðu þó í huga að þetta heiti mun birtast í sumum slóðum sem vísa til netverslunartilviksins.</span><span class="sxs-lookup"><span data-stu-id="97f02-264">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="97f02-265">Í reitnum **Heiti Commerce Scale Unit** skal velja CSU í listanum.</span><span class="sxs-lookup"><span data-stu-id="97f02-265">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="97f02-266">(Listinn ætti aðeins að hafa einn valkost.)</span><span class="sxs-lookup"><span data-stu-id="97f02-266">(The list should have only one option.)</span></span>

    <span data-ttu-id="97f02-267">Reiturinn **Landafræði rafrænna viðskipta** er stilltur sjálfkrafa og ekki er hægt að breyta gildinu.</span><span class="sxs-lookup"><span data-stu-id="97f02-267">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="97f02-268">Veldu **Næst** til að halda áfram.</span><span class="sxs-lookup"><span data-stu-id="97f02-268">Select **Next** to continue.</span></span>
1. <span data-ttu-id="97f02-269">Í reitnum **Studd hýsilheiti** slærðu inn gilt lén, eins og `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="97f02-269">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="97f02-270">Í reitnum **AAD-öryggishópur fyrir kerfisstjóra** slærðu inn fyrstu stafina í nafni öryggishópsins sem þú vilt nota.</span><span class="sxs-lookup"><span data-stu-id="97f02-270">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="97f02-271">Veldu stækkunarglerstáknið til að birta leitarniðurstöður.</span><span class="sxs-lookup"><span data-stu-id="97f02-271">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="97f02-272">Velja réttan öryggisflokk af listanum.</span><span class="sxs-lookup"><span data-stu-id="97f02-272">Select the correct security group from the list.</span></span>
2.  <span data-ttu-id="97f02-273">Í reitnum **AAD-öryggishópur stjórnanda fyrir einkunnir og umsagnir** slærðu inn fyrstu stafina í nafni öryggishópsins sem þú vilt nota.</span><span class="sxs-lookup"><span data-stu-id="97f02-273">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="97f02-274">Veldu stækkunarglerstáknið til að birta leitarniðurstöður.</span><span class="sxs-lookup"><span data-stu-id="97f02-274">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="97f02-275">Velja réttan öryggisflokk af listanum.</span><span class="sxs-lookup"><span data-stu-id="97f02-275">Select the correct security group from the list.</span></span>
1. <span data-ttu-id="97f02-276">Hafðu kveikt á valkostinum **Virkja einkunna- og umsagnaþjónustu**.</span><span class="sxs-lookup"><span data-stu-id="97f02-276">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="97f02-277">Veldu **Frumstilla**.</span><span class="sxs-lookup"><span data-stu-id="97f02-277">Select **Initialize**.</span></span> <span data-ttu-id="97f02-278">Skjárinn **Commerce-stjórnun** birtist aftur, þar sem flipinn **e-Commerce** er valinn.</span><span class="sxs-lookup"><span data-stu-id="97f02-278">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="97f02-279">Frumstilling rafrænna viðskipta er hafin.</span><span class="sxs-lookup"><span data-stu-id="97f02-279">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="97f02-280">Áður en lengra er haldið skaltu bíða þar til staða frumstillingar í netverslun er **Frumstilling tókst**.</span><span class="sxs-lookup"><span data-stu-id="97f02-280">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="97f02-281">Undir **Krækjur** neðst til hægri, skrifaðu vefslóðirnar fyrir eftirfarandi tengla:</span><span class="sxs-lookup"><span data-stu-id="97f02-281">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="97f02-282">**rafræn viðskipti síða** - Hlekkurinn á rótina á netverslunarsíðunni þinni.</span><span class="sxs-lookup"><span data-stu-id="97f02-282">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="97f02-283">**stjórnunartæki fyrir e-verslun** - Hlekkurinn að stjórnunartólinu.</span><span class="sxs-lookup"><span data-stu-id="97f02-283">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="97f02-284">Stuðningur við forskoðunarumhverfi fyrir Commerce</span><span class="sxs-lookup"><span data-stu-id="97f02-284">Commerce preview environment support</span></span>

<span data-ttu-id="97f02-285">Ef þú lendir í vandræðum meðan þú lýkur úthlutunarskrefunum skaltu fara á [Microsoft Dynamics 365 Commerce Forskoðun Yammer hópur](https://aka.ms/Dynamics365CommercePreviewYammer) fyrir aðstoð.</span><span class="sxs-lookup"><span data-stu-id="97f02-285">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

## <a name="next-steps"></a><span data-ttu-id="97f02-286">Næstu skref</span><span class="sxs-lookup"><span data-stu-id="97f02-286">Next steps</span></span>

<span data-ttu-id="97f02-287">Til að halda áfram úthlutunar- og stillingarferli forskoðunarumhverfis Commerce eftir að því hefur verið úthlutað skal sjá [Stilla forskoðunarumhverfi Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="97f02-287">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="97f02-288">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="97f02-288">Additional resources</span></span>

[<span data-ttu-id="97f02-289">Dynamics 365 Commerce yfirlit yfir forskoðunarumhverfi</span><span class="sxs-lookup"><span data-stu-id="97f02-289">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="97f02-290">Skilgreina Dynamics 365 Commerce forskoðunarumhverfi</span><span class="sxs-lookup"><span data-stu-id="97f02-290">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="97f02-291">Skilgreina valfrjálsa eiginleika fyrir Dynamics 365 Commerce forskoðunarumhverfi</span><span class="sxs-lookup"><span data-stu-id="97f02-291">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="97f02-292">Dynamics 365 Commerce yfirlitsumhverfi algengra spurninga</span><span class="sxs-lookup"><span data-stu-id="97f02-292">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="97f02-293">Microsoft Dynamics Lifecycle Services (LSC)</span><span class="sxs-lookup"><span data-stu-id="97f02-293">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="97f02-294">Commerce Scale Unit (ský)</span><span class="sxs-lookup"><span data-stu-id="97f02-294">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="97f02-295">Microsoft Azure-gátt</span><span class="sxs-lookup"><span data-stu-id="97f02-295">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="97f02-296">Dynamics 365 Commerce vefsvæði</span><span class="sxs-lookup"><span data-stu-id="97f02-296">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

