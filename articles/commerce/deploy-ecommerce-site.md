---
title: Uppsetning á nýjum leigjanda rafrænna viðskipta
description: Þetta efnisatriði lýsir því hvernig á að setja upp nýtt Dynamics 365 Commerce svæði fyrir rafræn viðskipti með því að nota Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3b750ee89a85688dcebe673f9c3ff13693e9fcad
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976739"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="56a49-103">Uppsetning á nýjum leigjanda rafrænna viðskipta</span><span class="sxs-lookup"><span data-stu-id="56a49-103">Deploy a new e-commerce tenant</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="56a49-104">Þetta efnisatriði lýsir því hvernig á að setja upp nýtt Dynamics 365 Commerce svæði fyrir rafræn viðskipti með því að nota Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="56a49-104">This topic describes how to deploy a new Dynamics 365 Commerce e-commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="56a49-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="56a49-105">Overview</span></span>

<span data-ttu-id="56a49-106">Microsoft Dynamics Lifecycle Services (LCS) er skýjasamvinnuvinnusvæði sem samstarfsaðilar og viðskiptavinir geta notað til að stjórna verkum sínum og umhverfi, skoða nýjustu upplýsingarnar um vörur og aðgerðir Microsoft Dynamics og stofna, fylgjast með og vafra um stuðningsatvik.</span><span class="sxs-lookup"><span data-stu-id="56a49-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="56a49-107">Eiginleikar E-Commerce Management eru samþættir við LCS.</span><span class="sxs-lookup"><span data-stu-id="56a49-107">E-commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="56a49-108">Til að læra meira um LCS, sjá [Notendahandbók um Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="56a49-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="56a49-109">Hafist handa</span><span class="sxs-lookup"><span data-stu-id="56a49-109">Get started</span></span>

<span data-ttu-id="56a49-110">Áður en hægt er að frumstilla rafræn viðskipti þarf að frumstilla verk, umhverfi og Retail Cloud Scale Unit (RCSU).</span><span class="sxs-lookup"><span data-stu-id="56a49-110">Before you can initialize e-commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="56a49-111">Til að gera frumstillingu í LCS verður þú að hafa heimildir fyrir annað hvort verkefnaeiganda eða umhverfisstjóra.</span><span class="sxs-lookup"><span data-stu-id="56a49-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="56a49-112">Framleiðslu- og sandkassaumhverfisgrannfræði eru studd.</span><span class="sxs-lookup"><span data-stu-id="56a49-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="56a49-113">Nánari upplýsingar um umhverfi, sjá [Umhverfisskipulag](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="56a49-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="56a49-114">Frekari upplýsingar um RCSU er að finna í [Frumstilla Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="56a49-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="56a49-115">Frumstilla rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="56a49-115">Initialize e-commerce</span></span>

<span data-ttu-id="56a49-116">Notið þetta ferli til að frumstilla eiginleika rafrænna viðskipta í umhverfi sem er til staðar.</span><span class="sxs-lookup"><span data-stu-id="56a49-116">Use this procedure to initialize the e-commerce feature in an existing environment.</span></span>

<span data-ttu-id="56a49-117">Vertu viss um að hafa eftirfarandi nauðsynlegar upplýsingar áður en þú byrjar:</span><span class="sxs-lookup"><span data-stu-id="56a49-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="56a49-118">RCSU sem notað verður.</span><span class="sxs-lookup"><span data-stu-id="56a49-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="56a49-119">Öryggisflokkur Microsoft Azure Active Directory sem verður notaður fyrir kerfisstjóra í rafrænum viðskiptum.</span><span class="sxs-lookup"><span data-stu-id="56a49-119">The Microsoft Azure Active Directory security group that will be used for e-commerce system admins.</span></span>
- <span data-ttu-id="56a49-120">Microsoft Azure Active Directory öryggishópur sem notaður verður af gæslumönnum einkunna og umsagna.</span><span class="sxs-lookup"><span data-stu-id="56a49-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="56a49-121">Lénin sem verða tengd umhverfinu.</span><span class="sxs-lookup"><span data-stu-id="56a49-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="56a49-122">Að auki geturðu safnað eftirfarandi valfrjálsum upplýsingum:</span><span class="sxs-lookup"><span data-stu-id="56a49-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="56a49-123">Azure AD upplýsingar frá viðskiptum til neytenda (B2C):</span><span class="sxs-lookup"><span data-stu-id="56a49-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="56a49-124">Heiti leigjanda.</span><span class="sxs-lookup"><span data-stu-id="56a49-124">Tenant Name.</span></span>
    - <span data-ttu-id="56a49-125">Biðlarakenni.</span><span class="sxs-lookup"><span data-stu-id="56a49-125">Client ID.</span></span>
    - <span data-ttu-id="56a49-126">Sérstillt lén innskráninga.</span><span class="sxs-lookup"><span data-stu-id="56a49-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="56a49-127">Svarslóð.</span><span class="sxs-lookup"><span data-stu-id="56a49-127">Reply URL.</span></span>
    - <span data-ttu-id="56a49-128">Reglukenni skráningar og innskráningar.</span><span class="sxs-lookup"><span data-stu-id="56a49-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="56a49-129">Reglukenni endurstillingar aðgangsorðs.</span><span class="sxs-lookup"><span data-stu-id="56a49-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="56a49-130">Breyta auðkenni forstillingarreglu.</span><span class="sxs-lookup"><span data-stu-id="56a49-130">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="56a49-131">Þessum upplýsingum má bæta síðar með þjónustubeiðni.</span><span class="sxs-lookup"><span data-stu-id="56a49-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="56a49-132">Eftir að þú hefur safnað nauðsynlegum upplýsingum skaltu fylgja þessum skrefum til að frumstilla rafræn viðskipti.</span><span class="sxs-lookup"><span data-stu-id="56a49-132">After you've collected the required information, follow these steps to initialize e-commerce.</span></span>

1. <span data-ttu-id="56a49-133">Skráðu þig inn í [LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="56a49-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="56a49-134">Opnið verkið sem inniheldur umhverfið þar sem á að ræsa rafræn viðskipti.</span><span class="sxs-lookup"><span data-stu-id="56a49-134">Open the project that contains the environment where you want to initialize e-commerce.</span></span>
1. <span data-ttu-id="56a49-135">Í hlutanum **Umhverfi**, veldu umhverfið.</span><span class="sxs-lookup"><span data-stu-id="56a49-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="56a49-136">Undir **Eiginleikar umhverfis**, veldu tengilinn **Stjórnun smásölu**.</span><span class="sxs-lookup"><span data-stu-id="56a49-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="56a49-137">Á flipanum **rafræn viðskipti**, veldu **Uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="56a49-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="56a49-138">Gluggi birtist þar sem þú verður að slá inn upplýsingarnar sem þarf til úthlutunar.</span><span class="sxs-lookup"><span data-stu-id="56a49-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="56a49-139">Fylltu út nauðsynlegar upplýsingar og farðu síðan á næstu síðu.</span><span class="sxs-lookup"><span data-stu-id="56a49-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="56a49-140">Á næstu síðu fyllirðu út nauðsynlegar upplýsingar og sendir formið síðan.</span><span class="sxs-lookup"><span data-stu-id="56a49-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="56a49-141">Þú ert komin/n aftur á flipann **rafræn viðskipti** þar sem þú ættir að sjá að byrjað hefur verið á frumstillingu.</span><span class="sxs-lookup"><span data-stu-id="56a49-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="56a49-142">Til að skoða frumstillingarstöðuna skaltu annaðhvort **Endurnýja** eða fara aftur á flipann **e-Commerce** seinna.</span><span class="sxs-lookup"><span data-stu-id="56a49-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="56a49-143">Þegar rafræn viðskipti eru ræst úr LCS úthlutar kerfið nokkrum hlutum sem eru nauðsynlegir fyrir rafræna viðskipti og tengir þá við umhverfið.</span><span class="sxs-lookup"><span data-stu-id="56a49-143">When e-commerce is initialized from LCS, the system provisions several components that are required for e-commerce and associates them with the environment.</span></span> <span data-ttu-id="56a49-144">Eftir að úthlutun er lokið er flipinn **rafræn viðskipti** á síðunni **Smásölustjórnun** uppfærð til að endurspegla úthlutunina.</span><span class="sxs-lookup"><span data-stu-id="56a49-144">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="56a49-145">Á síðunni birtast nýjustu dreifingaraðgerðirnar og staðan fyrir aðrar áframhaldandi dreifingar.</span><span class="sxs-lookup"><span data-stu-id="56a49-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="56a49-146">Þar er einnig að finna tengla á svæði fyrir rafræn viðskipti og smið rafrænna viðskipta þar sem svæði eru tengd.</span><span class="sxs-lookup"><span data-stu-id="56a49-146">It also includes links to the e-commerce site and the Commerce site builder where sites are authored.</span></span>

## <a name="access-commerce-site-builder"></a><span data-ttu-id="56a49-147">Access smiður rafrænna viðskipta</span><span class="sxs-lookup"><span data-stu-id="56a49-147">Access Commerce site builder</span></span>

<span data-ttu-id="56a49-148">Til að fá aðgang að Commerce Site Builder er farið á flipann **<Rafræn viðskipti** á flipanum **Smásölustjórnun** í LCS og tengillinn **Svæðisstjórnunarverkfæri rafrænna viðskipta** valinn.</span><span class="sxs-lookup"><span data-stu-id="56a49-148">To access Commerce site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="56a49-149">Áfangasíða byggingaraðila sýnir yfirlit leigjenda.</span><span class="sxs-lookup"><span data-stu-id="56a49-149">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="56a49-150">Af þessari síðu er hægt að:</span><span class="sxs-lookup"><span data-stu-id="56a49-150">From this page, you can:</span></span>

- <span data-ttu-id="56a49-151">Breyta stillingum leigjenda.</span><span class="sxs-lookup"><span data-stu-id="56a49-151">Modify tenant-level settings.</span></span>
- <span data-ttu-id="56a49-152">Fara á hvaða síðu sem þú hefur búið til og hefur heimild til að skoða.</span><span class="sxs-lookup"><span data-stu-id="56a49-152">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="56a49-153">Fara í umsögnir, eins og stjórnun og skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="56a49-153">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="56a49-154">Stofna nýtt svæði.</span><span class="sxs-lookup"><span data-stu-id="56a49-154">Create a new site.</span></span> <span data-ttu-id="56a49-155">Nánari upplýsingar um hvernig eigi að stofna nýja síðu er að finna í [Búa til nýtt svæði fyrir rafræn viðskipti](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="56a49-155">For more information about how to create a new site, see [Create an e-commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="56a49-156">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="56a49-156">Additional resources</span></span>

[<span data-ttu-id="56a49-157">Skilgreina lénsheiti</span><span class="sxs-lookup"><span data-stu-id="56a49-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="56a49-158">Stofna svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="56a49-158">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="56a49-159">Tengja svæði Dynamics 365 Commerce við netrás</span><span class="sxs-lookup"><span data-stu-id="56a49-159">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="56a49-160">Vinna með skrárnar robots.txt</span><span class="sxs-lookup"><span data-stu-id="56a49-160">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="56a49-161">Hlaða upp mörgum URL-framsendingum í einu</span><span class="sxs-lookup"><span data-stu-id="56a49-161">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="56a49-162">Setja upp B2C-leigjanda í Commerce</span><span class="sxs-lookup"><span data-stu-id="56a49-162">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="56a49-163">Setja upp sérsniðnar síður fyrir innskráningu notenda</span><span class="sxs-lookup"><span data-stu-id="56a49-163">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="56a49-164">Stilla marga B2C leigjendur í viðskiptaumhverfi</span><span class="sxs-lookup"><span data-stu-id="56a49-164">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="56a49-165">Bæta við stuðningi fyrir efnisbirtingarnet (CDN)</span><span class="sxs-lookup"><span data-stu-id="56a49-165">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="56a49-166">Virkja greiningu á verslun eftir staðsetningu</span><span class="sxs-lookup"><span data-stu-id="56a49-166">Enable location-based store detection</span></span>](enable-store-detection.md)
