---
title: Uppsetning á nýjum leigjanda rafrænna viðskipta
description: Þetta efni lýsir því hvernig nota á nýjan leigjanda í netverslun með því að nota Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 00f35b516dbf6ab4d4d9171c84a16b89f6afe832
ms.sourcegitcommit: adf196c51e2b6f532d99c177b4c6778cea8a2efc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/02/2020
ms.locfileid: "3533276"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="a1369-103">Uppsetning á nýjum leigjanda rafrænna viðskipta</span><span class="sxs-lookup"><span data-stu-id="a1369-103">Deploy a new e-Commerce tenant</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a1369-104">Þetta efni lýsir því hvernig nota á nýtt svæði í netverslun með því að nota Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="a1369-104">This topic describes how to deploy a new e-Commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="a1369-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="a1369-105">Overview</span></span>

<span data-ttu-id="a1369-106">Microsoft Dynamics Lifecycle Services (LCS) er skýjasamvinnuvinnusvæði sem samstarfsaðilar og viðskiptavinir geta notað til að stjórna verkum sínum og umhverfi, skoða nýjustu upplýsingarnar um vörur og aðgerðir Microsoft Dynamics og stofna, fylgjast með og vafra um stuðningsatvik.</span><span class="sxs-lookup"><span data-stu-id="a1369-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="a1369-107">Aðgerðir stjórnun rafrænna viðskipta eru samþættar LCS.</span><span class="sxs-lookup"><span data-stu-id="a1369-107">E-Commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="a1369-108">Til að læra meira um LCS, sjá [Notendahandbók um Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="a1369-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="a1369-109">Leiðsögn</span><span class="sxs-lookup"><span data-stu-id="a1369-109">Get started</span></span>

<span data-ttu-id="a1369-110">Áður en hægt er að frumstilla rafræn viðskipti verður þú að frumstilla verkefni, umhverfi og Retail Cloud Scale Unit (RCSU).</span><span class="sxs-lookup"><span data-stu-id="a1369-110">Before you can initialize e-Commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="a1369-111">Til að gera frumstillingu í LCS verður þú að hafa heimildir fyrir annað hvort verkefnaeiganda eða umhverfisstjóra.</span><span class="sxs-lookup"><span data-stu-id="a1369-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="a1369-112">Framleiðslu- og sandkassaumhverfisgrannfræði eru studd.</span><span class="sxs-lookup"><span data-stu-id="a1369-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="a1369-113">Nánari upplýsingar um umhverfi, sjá [Umhverfisskipulag](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="a1369-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="a1369-114">Frekari upplýsingar um RCSU er að finna í [Frumstilla Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="a1369-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="a1369-115">Frumstilla rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="a1369-115">Initialize e-Commerce</span></span>

<span data-ttu-id="a1369-116">Notaðu þessa aðferð til að frumstilla eiginleikann rafræn viðskipti í núverandi umhverfi.</span><span class="sxs-lookup"><span data-stu-id="a1369-116">Use this procedure to initialize the e-Commerce feature in an existing environment.</span></span>

<span data-ttu-id="a1369-117">Vertu viss um að hafa eftirfarandi nauðsynlegar upplýsingar áður en þú byrjar:</span><span class="sxs-lookup"><span data-stu-id="a1369-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="a1369-118">RCSU sem notað verður.</span><span class="sxs-lookup"><span data-stu-id="a1369-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="a1369-119">Microsoft Azure Active Directory öryggishópur sem notaður verður við kerfisstjórnendur e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="a1369-119">The Microsoft Azure Active Directory security group that will be used for e-Commerce system admins.</span></span>
- <span data-ttu-id="a1369-120">Microsoft Azure Active Directory öryggishópur sem notaður verður af gæslumönnum einkunna og umsagna.</span><span class="sxs-lookup"><span data-stu-id="a1369-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="a1369-121">Lénin sem verða tengd umhverfinu.</span><span class="sxs-lookup"><span data-stu-id="a1369-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="a1369-122">Að auki geturðu safnað eftirfarandi valfrjálsum upplýsingum:</span><span class="sxs-lookup"><span data-stu-id="a1369-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="a1369-123">Azure AD upplýsingar frá viðskiptum til neytenda (B2C):</span><span class="sxs-lookup"><span data-stu-id="a1369-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="a1369-124">Heiti leigjanda.</span><span class="sxs-lookup"><span data-stu-id="a1369-124">Tenant Name.</span></span>
    - <span data-ttu-id="a1369-125">Biðlarakenni.</span><span class="sxs-lookup"><span data-stu-id="a1369-125">Client ID.</span></span>
    - <span data-ttu-id="a1369-126">Sérstillt lén innskráninga.</span><span class="sxs-lookup"><span data-stu-id="a1369-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="a1369-127">Svarslóð.</span><span class="sxs-lookup"><span data-stu-id="a1369-127">Reply URL.</span></span>
    - <span data-ttu-id="a1369-128">Reglukenni skráningar og innskráningar.</span><span class="sxs-lookup"><span data-stu-id="a1369-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="a1369-129">Reglukenni endurstillingar aðgangsorðs.</span><span class="sxs-lookup"><span data-stu-id="a1369-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="a1369-130">Breyta auðkenni forstillingarreglu.</span><span class="sxs-lookup"><span data-stu-id="a1369-130">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="a1369-131">Þessum upplýsingum má bæta síðar með þjónustubeiðni.</span><span class="sxs-lookup"><span data-stu-id="a1369-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="a1369-132">Eftir að þú hefur safnað nauðsynlegum upplýsingum skaltu fylgja þessum skrefum til að frumstilla rafræn viðskipti.</span><span class="sxs-lookup"><span data-stu-id="a1369-132">After you've collected the required information, follow these steps to initialize e-Commerce.</span></span>

1. <span data-ttu-id="a1369-133">Skráðu þig inn í [LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="a1369-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="a1369-134">Opnaðu verkefnið sem inniheldur umhverfið þar sem þú vilt frumstilla rafræn viðskipti.</span><span class="sxs-lookup"><span data-stu-id="a1369-134">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="a1369-135">Í hlutanum **Umhverfi**, veldu umhverfið.</span><span class="sxs-lookup"><span data-stu-id="a1369-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="a1369-136">Undir **Eiginleikar umhverfis**, veldu tengilinn **Stjórnun smásölu**.</span><span class="sxs-lookup"><span data-stu-id="a1369-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="a1369-137">Á flipanum **rafræn viðskipti**, veldu **Uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="a1369-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="a1369-138">Gluggi birtist þar sem þú verður að slá inn upplýsingarnar sem þarf til úthlutunar.</span><span class="sxs-lookup"><span data-stu-id="a1369-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="a1369-139">Fylltu út nauðsynlegar upplýsingar og farðu síðan á næstu síðu.</span><span class="sxs-lookup"><span data-stu-id="a1369-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="a1369-140">Á næstu síðu fyllirðu út nauðsynlegar upplýsingar og sendir formið síðan.</span><span class="sxs-lookup"><span data-stu-id="a1369-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="a1369-141">Þú ert komin/n aftur á flipann **rafræn viðskipti** þar sem þú ættir að sjá að byrjað hefur verið á frumstillingu.</span><span class="sxs-lookup"><span data-stu-id="a1369-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="a1369-142">Til að skoða frumstillingarstöðuna skaltu annaðhvort **Endurnýja** eða fara aftur á flipann **e-Commerce** seinna.</span><span class="sxs-lookup"><span data-stu-id="a1369-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="a1369-143">Þegar rafræn viðskipti eru frumstill úr LCS, þá er kerfið með nokkra íhluti sem þarf til rafrænna viðskipta og tengir þá við umhverfið.</span><span class="sxs-lookup"><span data-stu-id="a1369-143">When e-Commerce is initialized from LCS, the system provisions several components that are required for e-Commerce and associates them with the environment.</span></span> <span data-ttu-id="a1369-144">Eftir að úthlutun er lokið er flipinn **rafræn viðskipti** á síðunni **Smásölustjórnun** uppfærð til að endurspegla úthlutunina.</span><span class="sxs-lookup"><span data-stu-id="a1369-144">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="a1369-145">Á síðunni birtast nýjustu dreifingaraðgerðirnar og staðan fyrir aðrar áframhaldandi dreifingar.</span><span class="sxs-lookup"><span data-stu-id="a1369-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="a1369-146">Það felur einnig í sér tengla á netverslunarsíðuna og vefsvæðishönnuð e-Commerce þar sem vefsvæði eru sett upp.</span><span class="sxs-lookup"><span data-stu-id="a1369-146">It also includes links to the e-Commerce site and the e-Commerce site builder where sites are authored.</span></span>

## <a name="access-site-builder"></a><span data-ttu-id="a1369-147">Aðgangur að vefsvæðishönnuði</span><span class="sxs-lookup"><span data-stu-id="a1369-147">Access site builder</span></span>

<span data-ttu-id="a1369-148">Farðu á flipann **e-Commerce** á síðunni **Verslunarstjórnun** í LCS og veldu tengilinn **Stjórnunartæki fyrir netverslun**.</span><span class="sxs-lookup"><span data-stu-id="a1369-148">To access site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="a1369-149">Áfangasíða byggingaraðila sýnir yfirlit leigjenda.</span><span class="sxs-lookup"><span data-stu-id="a1369-149">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="a1369-150">Af þessari síðu er hægt að:</span><span class="sxs-lookup"><span data-stu-id="a1369-150">From this page, you can:</span></span>

- <span data-ttu-id="a1369-151">Breyta stillingum leigjenda.</span><span class="sxs-lookup"><span data-stu-id="a1369-151">Modify tenant-level settings.</span></span>
- <span data-ttu-id="a1369-152">Fara á hvaða síðu sem þú hefur búið til og hefur heimild til að skoða.</span><span class="sxs-lookup"><span data-stu-id="a1369-152">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="a1369-153">Fara í umsögnir, eins og stjórnun og skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="a1369-153">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="a1369-154">Stofna nýtt svæði.</span><span class="sxs-lookup"><span data-stu-id="a1369-154">Create a new site.</span></span> <span data-ttu-id="a1369-155">Nánari upplýsingar um hvernig á að stofna nýtt svæði er að finna í [Stofna svæði fyrir rafræn viðskipti](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="a1369-155">For more information about how to create a new site, see [Create an e-Commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="a1369-156">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="a1369-156">Additional resources</span></span>

[<span data-ttu-id="a1369-157">Skilgreina lénsheiti</span><span class="sxs-lookup"><span data-stu-id="a1369-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="a1369-158">Stofna svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="a1369-158">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="a1369-159">Tengja netsvæði við rás</span><span class="sxs-lookup"><span data-stu-id="a1369-159">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="a1369-160">Vinna með skrárnar robots.txt</span><span class="sxs-lookup"><span data-stu-id="a1369-160">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="a1369-161">Hlaða upp mörgum slóðartilvísunum í einu</span><span class="sxs-lookup"><span data-stu-id="a1369-161">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="a1369-162">Setja upp B2C-leigjanda í Commerce</span><span class="sxs-lookup"><span data-stu-id="a1369-162">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="a1369-163">Setja upp sérsniðnar síður fyrir innskráningu notenda</span><span class="sxs-lookup"><span data-stu-id="a1369-163">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="a1369-164">Stilla marga B2C leigjendur í viðskiptaumhverfi</span><span class="sxs-lookup"><span data-stu-id="a1369-164">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="a1369-165">Bæta við stuðningi fyrir efnisbirtingarnet (CDN)</span><span class="sxs-lookup"><span data-stu-id="a1369-165">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="a1369-166">Virkja greiningu á verslun eftir staðsetningu</span><span class="sxs-lookup"><span data-stu-id="a1369-166">Enable location-based store detection</span></span>](enable-store-detection.md)
