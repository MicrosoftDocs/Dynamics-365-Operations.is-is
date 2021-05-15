---
title: Uppsetning á nýjum leigjanda rafrænna viðskipta
description: Þetta efnisatriði lýsir því hvernig á að setja upp nýtt Dynamics 365 Commerce svæði fyrir rafræn viðskipti með því að nota Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6b228babfd32a4191eeed2a6d924a8b99f1a5311
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936707"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="9f69c-103">Uppsetning á nýjum leigjanda rafrænna viðskipta</span><span class="sxs-lookup"><span data-stu-id="9f69c-103">Deploy a new e-commerce tenant</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9f69c-104">Þetta efnisatriði lýsir því hvernig á að setja upp nýtt Dynamics 365 Commerce svæði fyrir rafræn viðskipti með því að nota Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="9f69c-104">This topic describes how to deploy a new Dynamics 365 Commerce e-commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="9f69c-105">Microsoft Dynamics Lifecycle Services (LCS) er skýjasamvinnuvinnusvæði sem samstarfsaðilar og viðskiptavinir geta notað til að stjórna verkum sínum og umhverfi, skoða nýjustu upplýsingarnar um vörur og aðgerðir Microsoft Dynamics og stofna, fylgjast með og vafra um stuðningsatvik.</span><span class="sxs-lookup"><span data-stu-id="9f69c-105">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="9f69c-106">Eiginleikar E-Commerce Management eru samþættir við LCS.</span><span class="sxs-lookup"><span data-stu-id="9f69c-106">E-commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="9f69c-107">Til að læra meira um LCS, sjá [Notendahandbók um Lifecycle Services](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="9f69c-107">To learn more about LCS, see the [Lifecycle Services User Guide](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="9f69c-108">Hafist handa</span><span class="sxs-lookup"><span data-stu-id="9f69c-108">Get started</span></span>

<span data-ttu-id="9f69c-109">Áður en hægt er að frumstilla rafræn viðskipti þarf að frumstilla verk, umhverfi og Retail Cloud Scale Unit (RCSU).</span><span class="sxs-lookup"><span data-stu-id="9f69c-109">Before you can initialize e-commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="9f69c-110">Til að gera frumstillingu í LCS verður þú að hafa heimildir fyrir annað hvort verkefnaeiganda eða umhverfisstjóra.</span><span class="sxs-lookup"><span data-stu-id="9f69c-110">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="9f69c-111">Framleiðslu- og sandkassaumhverfisgrannfræði eru studd.</span><span class="sxs-lookup"><span data-stu-id="9f69c-111">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="9f69c-112">Nánari upplýsingar um umhverfi, sjá [Umhverfisskipulag](/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="9f69c-112">For more information about environments, see [Environment planning](/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="9f69c-113">Frekari upplýsingar um RCSU er að finna í [Frumstilla Retail Cloud Scale Unit](/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="9f69c-113">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="9f69c-114">Frumstilla rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="9f69c-114">Initialize e-commerce</span></span>

<span data-ttu-id="9f69c-115">Notið þetta ferli til að frumstilla eiginleika rafrænna viðskipta í umhverfi sem er til staðar.</span><span class="sxs-lookup"><span data-stu-id="9f69c-115">Use this procedure to initialize the e-commerce feature in an existing environment.</span></span>

<span data-ttu-id="9f69c-116">Vertu viss um að hafa eftirfarandi nauðsynlegar upplýsingar áður en þú byrjar:</span><span class="sxs-lookup"><span data-stu-id="9f69c-116">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="9f69c-117">RCSU sem notað verður.</span><span class="sxs-lookup"><span data-stu-id="9f69c-117">The RCSU that will be used.</span></span>
- <span data-ttu-id="9f69c-118">Öryggisflokkur Microsoft Azure Active Directory sem verður notaður fyrir kerfisstjóra í rafrænum viðskiptum.</span><span class="sxs-lookup"><span data-stu-id="9f69c-118">The Microsoft Azure Active Directory security group that will be used for e-commerce system admins.</span></span>
- <span data-ttu-id="9f69c-119">Microsoft Azure Active Directory öryggishópur sem notaður verður af gæslumönnum einkunna og umsagna.</span><span class="sxs-lookup"><span data-stu-id="9f69c-119">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="9f69c-120">Lénin sem verða tengd umhverfinu.</span><span class="sxs-lookup"><span data-stu-id="9f69c-120">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="9f69c-121">Að auki geturðu safnað eftirfarandi valfrjálsum upplýsingum:</span><span class="sxs-lookup"><span data-stu-id="9f69c-121">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="9f69c-122">Azure AD upplýsingar frá viðskiptum til neytenda (B2C):</span><span class="sxs-lookup"><span data-stu-id="9f69c-122">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="9f69c-123">Heiti leigjanda.</span><span class="sxs-lookup"><span data-stu-id="9f69c-123">Tenant Name.</span></span>
    - <span data-ttu-id="9f69c-124">Biðlarakenni.</span><span class="sxs-lookup"><span data-stu-id="9f69c-124">Client ID.</span></span>
    - <span data-ttu-id="9f69c-125">Sérstillt lén innskráninga.</span><span class="sxs-lookup"><span data-stu-id="9f69c-125">Login Custom Domain.</span></span>
    - <span data-ttu-id="9f69c-126">Svarslóð.</span><span class="sxs-lookup"><span data-stu-id="9f69c-126">Reply URL.</span></span>
    - <span data-ttu-id="9f69c-127">Reglukenni skráningar og innskráningar.</span><span class="sxs-lookup"><span data-stu-id="9f69c-127">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="9f69c-128">Reglukenni endurstillingar aðgangsorðs.</span><span class="sxs-lookup"><span data-stu-id="9f69c-128">Reset password Policy ID.</span></span>
    - <span data-ttu-id="9f69c-129">Breyta auðkenni forstillingarreglu.</span><span class="sxs-lookup"><span data-stu-id="9f69c-129">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="9f69c-130">Þessum upplýsingum má bæta síðar með þjónustubeiðni.</span><span class="sxs-lookup"><span data-stu-id="9f69c-130">This information can be added later, through a service request.</span></span>

<span data-ttu-id="9f69c-131">Eftir að þú hefur safnað nauðsynlegum upplýsingum skaltu fylgja þessum skrefum til að frumstilla rafræn viðskipti.</span><span class="sxs-lookup"><span data-stu-id="9f69c-131">After you've collected the required information, follow these steps to initialize e-commerce.</span></span>

1. <span data-ttu-id="9f69c-132">Skráðu þig inn í [LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="9f69c-132">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="9f69c-133">Opnið verkið sem inniheldur umhverfið þar sem á að ræsa rafræn viðskipti.</span><span class="sxs-lookup"><span data-stu-id="9f69c-133">Open the project that contains the environment where you want to initialize e-commerce.</span></span>
1. <span data-ttu-id="9f69c-134">Í hlutanum **Umhverfi**, veldu umhverfið.</span><span class="sxs-lookup"><span data-stu-id="9f69c-134">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="9f69c-135">Undir **Eiginleikar umhverfis**, veldu tengilinn **Stjórnun smásölu**.</span><span class="sxs-lookup"><span data-stu-id="9f69c-135">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="9f69c-136">Á flipanum **rafræn viðskipti**, veldu **Uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="9f69c-136">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="9f69c-137">Gluggi birtist þar sem þú verður að slá inn upplýsingarnar sem þarf til úthlutunar.</span><span class="sxs-lookup"><span data-stu-id="9f69c-137">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="9f69c-138">Fylltu út nauðsynlegar upplýsingar og farðu síðan á næstu síðu.</span><span class="sxs-lookup"><span data-stu-id="9f69c-138">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="9f69c-139">Á næstu síðu fyllirðu út nauðsynlegar upplýsingar og sendir formið síðan.</span><span class="sxs-lookup"><span data-stu-id="9f69c-139">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="9f69c-140">Þú ert komin/n aftur á flipann **rafræn viðskipti** þar sem þú ættir að sjá að byrjað hefur verið á frumstillingu.</span><span class="sxs-lookup"><span data-stu-id="9f69c-140">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="9f69c-141">Til að skoða frumstillingarstöðuna skaltu annaðhvort **Endurnýja** eða fara aftur á flipann **e-Commerce** seinna.</span><span class="sxs-lookup"><span data-stu-id="9f69c-141">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="9f69c-142">Þegar rafræn viðskipti eru ræst úr LCS úthlutar kerfið nokkrum hlutum sem eru nauðsynlegir fyrir rafræna viðskipti og tengir þá við umhverfið.</span><span class="sxs-lookup"><span data-stu-id="9f69c-142">When e-commerce is initialized from LCS, the system provisions several components that are required for e-commerce and associates them with the environment.</span></span> <span data-ttu-id="9f69c-143">Eftir að úthlutun er lokið er flipinn **rafræn viðskipti** á síðunni **Smásölustjórnun** uppfærð til að endurspegla úthlutunina.</span><span class="sxs-lookup"><span data-stu-id="9f69c-143">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="9f69c-144">Á síðunni birtast nýjustu dreifingaraðgerðirnar og staðan fyrir aðrar áframhaldandi dreifingar.</span><span class="sxs-lookup"><span data-stu-id="9f69c-144">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="9f69c-145">Þar er einnig að finna tengla á svæði fyrir rafræn viðskipti og smið rafrænna viðskipta þar sem svæði eru tengd.</span><span class="sxs-lookup"><span data-stu-id="9f69c-145">It also includes links to the e-commerce site and the Commerce site builder where sites are authored.</span></span>

## <a name="access-commerce-site-builder"></a><span data-ttu-id="9f69c-146">Access smiður rafrænna viðskipta</span><span class="sxs-lookup"><span data-stu-id="9f69c-146">Access Commerce site builder</span></span>

<span data-ttu-id="9f69c-147">Til að fá aðgang að Commerce Site Builder er farið á flipann **<Rafræn viðskipti** á flipanum **Smásölustjórnun** í LCS og tengillinn **Svæðisstjórnunarverkfæri rafrænna viðskipta** valinn.</span><span class="sxs-lookup"><span data-stu-id="9f69c-147">To access Commerce site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="9f69c-148">Áfangasíða byggingaraðila sýnir yfirlit leigjenda.</span><span class="sxs-lookup"><span data-stu-id="9f69c-148">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="9f69c-149">Af þessari síðu er hægt að:</span><span class="sxs-lookup"><span data-stu-id="9f69c-149">From this page, you can:</span></span>

- <span data-ttu-id="9f69c-150">Breyta stillingum leigjenda.</span><span class="sxs-lookup"><span data-stu-id="9f69c-150">Modify tenant-level settings.</span></span>
- <span data-ttu-id="9f69c-151">Fara á hvaða síðu sem þú hefur búið til og hefur heimild til að skoða.</span><span class="sxs-lookup"><span data-stu-id="9f69c-151">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="9f69c-152">Fara í umsögnir, eins og stjórnun og skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="9f69c-152">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="9f69c-153">Stofna nýtt svæði.</span><span class="sxs-lookup"><span data-stu-id="9f69c-153">Create a new site.</span></span> <span data-ttu-id="9f69c-154">Nánari upplýsingar um hvernig eigi að stofna nýja síðu er að finna í [Búa til nýtt svæði fyrir rafræn viðskipti](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="9f69c-154">For more information about how to create a new site, see [Create an e-commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="9f69c-155">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="9f69c-155">Additional resources</span></span>

[<span data-ttu-id="9f69c-156">Skilgreina lénsheiti</span><span class="sxs-lookup"><span data-stu-id="9f69c-156">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="9f69c-157">Stofna svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="9f69c-157">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="9f69c-158">Tengja svæði Dynamics 365 Commerce við netrás</span><span class="sxs-lookup"><span data-stu-id="9f69c-158">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="9f69c-159">Vinna með skrárnar robots.txt</span><span class="sxs-lookup"><span data-stu-id="9f69c-159">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="9f69c-160">Hlaða upp mörgum URL-framsendingum í einu</span><span class="sxs-lookup"><span data-stu-id="9f69c-160">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="9f69c-161">Setja upp B2C-leigjanda í Commerce</span><span class="sxs-lookup"><span data-stu-id="9f69c-161">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="9f69c-162">Setja upp sérsniðnar síður fyrir innskráningu notenda</span><span class="sxs-lookup"><span data-stu-id="9f69c-162">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="9f69c-163">Stilla marga B2C leigjendur í viðskiptaumhverfi</span><span class="sxs-lookup"><span data-stu-id="9f69c-163">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="9f69c-164">Bæta við stuðningi fyrir efnisbirtingarnet (CDN)</span><span class="sxs-lookup"><span data-stu-id="9f69c-164">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="9f69c-165">Virkja greiningu á verslun eftir staðsetningu</span><span class="sxs-lookup"><span data-stu-id="9f69c-165">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]