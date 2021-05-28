---
title: Regulatory Configuration Service
description: Í þessu efnisatriði er sýnt yfirlit yfir möguleika Regulatory Configuration Service (RCS) og útskýrt hvernig á að nálgast þessa þjónustu.
author: JaneA07
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 1eeac7217290e0583fcecdf5b4b5b9153d266240
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019395"
---
# <a name="regulatory-configuration-service"></a><span data-ttu-id="d64ce-103">Regulatory Configuration Service</span><span class="sxs-lookup"><span data-stu-id="d64ce-103">Regulatory Configuration Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d64ce-104">Regulatory Configuration Service (RCS) sjálfstæður hönnuður þjónusta líftímastjórnunar fyrir altæka virkni án kóða/með litlum kóða.</span><span class="sxs-lookup"><span data-stu-id="d64ce-104">Regulatory Configuration Service (RCS) is a standalone designer and lifecycle management service for no-code/low-code globalization functionality.</span></span> <span data-ttu-id="d64ce-105">RCS gerir altækum hagsmunaaðilum kleift að stækka og sérstilla altæk svæði skatts, rafrænnar reikningsfærslu, lögbundna skýrslugerð, bankaviðskipti og viðskiptaskjöl án þess að þróunaraðilar þurfi að koma við sögu.</span><span class="sxs-lookup"><span data-stu-id="d64ce-105">RCS lets globalization stakeholders extend and customize key globalization areas of tax, e-invoicing, regulatory reporting, banking, and business documents without having to involve developers.</span></span> <span data-ttu-id="d64ce-106">Þessi altæka nálgun án kóða/með litlum kóða gerir sameininguna auðveldari, hraðvirkari og ekki eins kostnaðarsamt að búa til eða stækka.</span><span class="sxs-lookup"><span data-stu-id="d64ce-106">This no-code/low-code globalization approach makes globalization easier, faster, and more cost effective to create or extend.</span></span>

<span data-ttu-id="d64ce-107">RCS býður upp á eftirfarandi möguleika:</span><span class="sxs-lookup"><span data-stu-id="d64ce-107">RCS provides the following capabilities:</span></span>

- <span data-ttu-id="d64ce-108">Stuðningur fyrir alla virkni sem rafræn skýrslugerð býður upp á.</span><span class="sxs-lookup"><span data-stu-id="d64ce-108">Support for all functionality that is provided by Electronic reporting (ER).</span></span>
- <span data-ttu-id="d64ce-109">Frumskilyrði til að skilgreina nýja altæka örþjónustu.</span><span class="sxs-lookup"><span data-stu-id="d64ce-109">A prerequisite to configure new globalization microservices.</span></span>
- <span data-ttu-id="d64ce-110">Stuðningur fyrir rafræna reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="d64ce-110">Support for Electronic Invoicing.</span></span> <span data-ttu-id="d64ce-111">Frekari upplýsingar eru í [Rafrænar reikningsfærslur](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span><span class="sxs-lookup"><span data-stu-id="d64ce-111">For more information, see [Electronic Invoicing](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span></span>
- <span data-ttu-id="d64ce-112">Stuðningur fyrir skattaútreikning.</span><span class="sxs-lookup"><span data-stu-id="d64ce-112">Supports for Tax Calculation.</span></span> <span data-ttu-id="d64ce-113">Nánari upplýsingar eru í [Skattaþjónusta](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span><span class="sxs-lookup"><span data-stu-id="d64ce-113">For more information, see [Tax service](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span></span>
- <span data-ttu-id="d64ce-114">Stuðningur fyrir nýja virkni altæks eiginleika sem einfaldar líftímastjórnun fjölþátta eiginleika og veitir frekari möguleika til að skilgreina aðgerðir og setja upp færibreytur eiginleika.</span><span class="sxs-lookup"><span data-stu-id="d64ce-114">Support for new globalization feature functionality that simplifies the lifecycle management of multi-component features and provides extra capability to configure actions and set up feature parameters.</span></span> <span data-ttu-id="d64ce-115">Frekari upplýsingar er að finna í [Regulatory Configuration Services – einfölduð altæk eiginleikastjórnun fyrir altækar þjónustur](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span><span class="sxs-lookup"><span data-stu-id="d64ce-115">For more information, see [Regulatory Configuration Service – simplified globalization feature management for globalization services](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span></span>
- <span data-ttu-id="d64ce-116">Stuðningur fyrir miðstýrða útgáfu, geymslu og deilingu á sérstilltum skilgreiningum í altækri geymslu til að einfalda skilgreiningarstjórnun án þess að þurfa að nota Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="d64ce-116">Support for centralized publication, storage, and sharing of custom configurations in the Global repository to simplify configuration management without requiring the use of Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="access-rcs"></a><span data-ttu-id="d64ce-117">Aðgangur að RCS</span><span class="sxs-lookup"><span data-stu-id="d64ce-117">Access RCS</span></span>

<span data-ttu-id="d64ce-118">Þú getur skráð þig fyrir eða skráð þig inn í RCS af síðunni [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="d64ce-118">You can sign up for or sign in to RCS from the [Regulatory Configuration Service page](https://marketing.configure.global.dynamics.com/).</span></span>

![Nýskráning/innskráning í RCS](media/202103_RCS%20Marketing%20page_updated_1.jpg)

<span data-ttu-id="d64ce-120">Á síðunni **Regulatory Configuration Service** skal yfirfara og samþykkja viðbótarskilmálana fyrir notkun á þjónustunni og síðan velja einn af eftirfarandi hnöppum:</span><span class="sxs-lookup"><span data-stu-id="d64ce-120">On the **Regulatory Configuration Service** page, review and accept the supplemental terms and conditions for use of the service, and then select one of the following buttons:</span></span>

- <span data-ttu-id="d64ce-121">**Nýskráðu** þig ef þú ert að nota þjónustuna í fyrsta skipti og ert að nota netfang fyrirtækis til að úthluta þjónustuumhverfi fyrirtækisins</span><span class="sxs-lookup"><span data-stu-id="d64ce-121">**Sign up** if you're a first-time user of the service, and you're using a business email address to provision your organization a service environment</span></span>
- <span data-ttu-id="d64ce-122">**Innskráðu** þig þú hefur skráð þig fyrir þjónustunni áður og vilt opna umhverfi fyrirtækisins</span><span class="sxs-lookup"><span data-stu-id="d64ce-122">**Sign in** if you've previously signed up for the service, and you want to access your organization environment</span></span>

## <a name="regional-availability"></a><span data-ttu-id="d64ce-123">Svæði í boði</span><span class="sxs-lookup"><span data-stu-id="d64ce-123">Regional availability</span></span>

<span data-ttu-id="d64ce-124">RCS er almennt í boði á eftirfarandi svæðum:</span><span class="sxs-lookup"><span data-stu-id="d64ce-124">RCS is generally available in the following regions:</span></span>

- <span data-ttu-id="d64ce-125">Bandaríkin</span><span class="sxs-lookup"><span data-stu-id="d64ce-125">United States</span></span>
- <span data-ttu-id="d64ce-126">Indland</span><span class="sxs-lookup"><span data-stu-id="d64ce-126">India</span></span>
- <span data-ttu-id="d64ce-127">Frakkland</span><span class="sxs-lookup"><span data-stu-id="d64ce-127">France</span></span>
- <span data-ttu-id="d64ce-128">Evrópa</span><span class="sxs-lookup"><span data-stu-id="d64ce-128">Europe</span></span>

<span data-ttu-id="d64ce-129">Fyrir heildarlista yfir svæði skal skoða [Dynamics 365 og Power Platform: Aðgengileiki, staðsetning gagna, tungumál og staðfærsla](https://aka.ms/dynamics_365_international_availability_deck).</span><span class="sxs-lookup"><span data-stu-id="d64ce-129">For a complete list of regions, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/dynamics_365_international_availability_deck).</span></span>

## <a name="related-rcs-documentation"></a><span data-ttu-id="d64ce-130">Tengd RCS-fylgigögn</span><span class="sxs-lookup"><span data-stu-id="d64ce-130">Related RCS documentation</span></span>

<span data-ttu-id="d64ce-131">Frekari upplýsingar um tengda þætti er að finna í eftirfarandi fylgigögnum:</span><span class="sxs-lookup"><span data-stu-id="d64ce-131">For more information about related components, see the following documentation:</span></span>

- <span data-ttu-id="d64ce-132">**Altæk geymsla:**</span><span class="sxs-lookup"><span data-stu-id="d64ce-132">**Global repository:**</span></span>

    - [<span data-ttu-id="d64ce-133">Búa til skilgreiningu rafrænnar skýrslugerðar og hlaða upp í altæka geymslu</span><span class="sxs-lookup"><span data-stu-id="d64ce-133">Create ER configuration & upload to Global repo</span></span>](rcs-global-repo-upload.md)
    - [<span data-ttu-id="d64ce-134">Deila skilgreiningum í altækri geymslu</span><span class="sxs-lookup"><span data-stu-id="d64ce-134">Share configuration in Global repo</span></span>](rcs-global-repo-share-configuration.md)
    - [<span data-ttu-id="d64ce-135">Aukin síun í altækri geymslu</span><span class="sxs-lookup"><span data-stu-id="d64ce-135">Enhanced filtering in Global repo</span></span>](enhanced-filtering-global-repo.md)
    - [<span data-ttu-id="d64ce-136">Sækja skilgreiningar rafrænnar skýrslugerðar úr altækri geymslu</span><span class="sxs-lookup"><span data-stu-id="d64ce-136">Download ER configurations from the Global repository</span></span>](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [<span data-ttu-id="d64ce-137">Hætta með skilgreiningar í altækri geymslu</span><span class="sxs-lookup"><span data-stu-id="d64ce-137">Discontinuing configurations in Global repo</span></span>](discontinuing-configurations-rcs-global-repo.md)

- <span data-ttu-id="d64ce-138">**Altækur eiginleiki:**</span><span class="sxs-lookup"><span data-stu-id="d64ce-138">**Globalization feature:**</span></span>

    - [<span data-ttu-id="d64ce-139">Regulatory Configuration Service (RCS) – altækur eiginleiki</span><span class="sxs-lookup"><span data-stu-id="d64ce-139">Regulatory Configuration Service (RCS) - Globalization feature</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)