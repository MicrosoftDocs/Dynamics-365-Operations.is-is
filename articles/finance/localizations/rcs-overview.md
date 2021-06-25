---
title: Regulatory Configuration Service
description: Í þessu efnisatriði er sýnt yfirlit yfir möguleika Regulatory Configuration Service (RCS) og útskýrt hvernig á að nálgast þessa þjónustu.
author: JaneA07
ms.date: 06/04/2021
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
ms.openlocfilehash: 7f946988f124c814452e1774c700d5c7354f39b0
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216563"
---
# <a name="regulatory-configuration-service"></a><span data-ttu-id="dc6ab-103">Regulatory Configuration Service</span><span class="sxs-lookup"><span data-stu-id="dc6ab-103">Regulatory Configuration Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc6ab-104">Regulatory Configuration Service (RCS) sjálfstæður hönnuður þjónusta líftímastjórnunar fyrir altæka virkni án kóða/með litlum kóða.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-104">Regulatory Configuration Service (RCS) is a standalone designer and lifecycle management service for no-code/low-code globalization functionality.</span></span> <span data-ttu-id="dc6ab-105">RCS gerir altækum hagsmunaaðilum kleift að stækka og sérstilla altæk svæði skatts, rafrænnar reikningsfærslu, lögbundna skýrslugerð, bankaviðskipti og viðskiptaskjöl án þess að þróunaraðilar þurfi að koma við sögu.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-105">RCS lets globalization stakeholders extend and customize key globalization areas of tax, e-invoicing, regulatory reporting, banking, and business documents without having to involve developers.</span></span> <span data-ttu-id="dc6ab-106">Þessi altæka nálgun án kóða/með litlum kóða gerir sameininguna auðveldari, hraðvirkari og ekki eins kostnaðarsamt að búa til eða stækka.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-106">This no-code/low-code globalization approach makes globalization easier, faster, and more cost effective to create or extend.</span></span>

<span data-ttu-id="dc6ab-107">RCS býður upp á eftirfarandi möguleika:</span><span class="sxs-lookup"><span data-stu-id="dc6ab-107">RCS provides the following capabilities:</span></span>

- <span data-ttu-id="dc6ab-108">Stuðningur fyrir alla virkni sem rafræn skýrslugerð býður upp á.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-108">Support for all functionality that is provided by Electronic reporting (ER).</span></span>
- <span data-ttu-id="dc6ab-109">Frumskilyrði til að skilgreina nýja altæka örþjónustu.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-109">A prerequisite to configure new globalization microservices.</span></span>
- <span data-ttu-id="dc6ab-110">Stuðningur fyrir rafræna reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-110">Support for Electronic Invoicing.</span></span> <span data-ttu-id="dc6ab-111">Frekari upplýsingar eru í [Rafrænar reikningsfærslur](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span><span class="sxs-lookup"><span data-stu-id="dc6ab-111">For more information, see [Electronic Invoicing](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span></span>
- <span data-ttu-id="dc6ab-112">Stuðningur fyrir skattaútreikning.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-112">Supports for Tax Calculation.</span></span> <span data-ttu-id="dc6ab-113">Nánari upplýsingar eru í [Skattaþjónusta](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span><span class="sxs-lookup"><span data-stu-id="dc6ab-113">For more information, see [Tax service](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span></span>
- <span data-ttu-id="dc6ab-114">Stuðningur fyrir nýja virkni altæks eiginleika sem einfaldar líftímastjórnun fjölþátta eiginleika og veitir frekari möguleika til að skilgreina aðgerðir og setja upp færibreytur eiginleika.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-114">Support for new globalization feature functionality that simplifies the lifecycle management of multi-component features and provides extra capability to configure actions and set up feature parameters.</span></span> <span data-ttu-id="dc6ab-115">Frekari upplýsingar er að finna í [Regulatory Configuration Services – einfölduð altæk eiginleikastjórnun fyrir altækar þjónustur](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span><span class="sxs-lookup"><span data-stu-id="dc6ab-115">For more information, see [Regulatory Configuration Service – simplified globalization feature management for globalization services](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span></span>
- <span data-ttu-id="dc6ab-116">Stuðningur fyrir miðstýrða útgáfu, geymslu og deilingu á sérstilltum skilgreiningum í altækri geymslu til að einfalda skilgreiningarstjórnun án þess að þurfa að nota Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="dc6ab-116">Support for centralized publication, storage, and sharing of custom configurations in the Global repository to simplify configuration management without requiring the use of Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="access-rcs"></a><span data-ttu-id="dc6ab-117">Aðgangur að RCS</span><span class="sxs-lookup"><span data-stu-id="dc6ab-117">Access RCS</span></span>

<span data-ttu-id="dc6ab-118">Þú getur skráð þig fyrir eða skráð þig inn í RCS af síðunni [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="dc6ab-118">You can sign up for or sign in to RCS from the [Regulatory Configuration Service page](https://marketing.configure.global.dynamics.com/).</span></span>

![Nýskráning/innskráning í RCS](media/202103_RCS%20Marketing%20page_updated_1.jpg)

<span data-ttu-id="dc6ab-120">Á síðunni **Regulatory Configuration Service** skal yfirfara og samþykkja viðbótarskilmálana fyrir notkun á þjónustunni og síðan velja einn af eftirfarandi hnöppum:</span><span class="sxs-lookup"><span data-stu-id="dc6ab-120">On the **Regulatory Configuration Service** page, review and accept the supplemental terms and conditions for use of the service, and then select one of the following buttons:</span></span>

- <span data-ttu-id="dc6ab-121">**Nýskráðu** þig ef þú ert að nota þjónustuna í fyrsta skipti og ert að nota netfang fyrirtækis til að úthluta þjónustuumhverfi fyrirtækisins</span><span class="sxs-lookup"><span data-stu-id="dc6ab-121">**Sign up** if you're a first-time user of the service, and you're using a business email address to provision your organization a service environment</span></span>
- <span data-ttu-id="dc6ab-122">**Innskráðu** þig þú hefur skráð þig fyrir þjónustunni áður og vilt opna umhverfi fyrirtækisins</span><span class="sxs-lookup"><span data-stu-id="dc6ab-122">**Sign in** if you've previously signed up for the service, and you want to access your organization environment</span></span>

## <a name="regional-availability"></a><span data-ttu-id="dc6ab-123">Svæði í boði</span><span class="sxs-lookup"><span data-stu-id="dc6ab-123">Regional availability</span></span>

<span data-ttu-id="dc6ab-124">RCS er almennt í boði á eftirfarandi svæðum:</span><span class="sxs-lookup"><span data-stu-id="dc6ab-124">RCS is generally available in the following regions:</span></span>

- <span data-ttu-id="dc6ab-125">Bandaríkin</span><span class="sxs-lookup"><span data-stu-id="dc6ab-125">United States</span></span>
- <span data-ttu-id="dc6ab-126">Indland</span><span class="sxs-lookup"><span data-stu-id="dc6ab-126">India</span></span>
- <span data-ttu-id="dc6ab-127">Frakkland</span><span class="sxs-lookup"><span data-stu-id="dc6ab-127">France</span></span>
- <span data-ttu-id="dc6ab-128">Evrópa</span><span class="sxs-lookup"><span data-stu-id="dc6ab-128">Europe</span></span>

<span data-ttu-id="dc6ab-129">Fyrir heildarlista yfir svæði skal skoða [Dynamics 365 og Power Platform: Aðgengileiki, staðsetning gagna, tungumál og staðfærsla](https://aka.ms/dynamics_365_international_availability_deck).</span><span class="sxs-lookup"><span data-stu-id="dc6ab-129">For a complete list of regions, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/dynamics_365_international_availability_deck).</span></span>

## <a name="rcs-default-company"></a><span data-ttu-id="dc6ab-130">Sjálfgefið fyrirtæki RCS</span><span class="sxs-lookup"><span data-stu-id="dc6ab-130">RCS default company</span></span>

<span data-ttu-id="dc6ab-131">Virkni hönnunartíma sem er notuð í RCS er samnýtt í öllum fyrirtækjum.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-131">Design time functionality that is used in RCS is shared across all companies.</span></span> <span data-ttu-id="dc6ab-132">Engin virkni miðast við ákveðið fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-132">There is no company-specific functionality.</span></span> <span data-ttu-id="dc6ab-133">Þess vegna er mælt með að nota eitt fyrirtæki, **DAT**, sem RCS-umhverfi.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-133">Therefore, we recommend that you use one company, **DAT**, with your RCS environment.</span></span>

<span data-ttu-id="dc6ab-134">Í sumum aðstæðum gæti verið sniðugt að láta snið rafrænnar skýrslugerðar nota færibreytur sem tengjst tilteknum lögaðila.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-134">However, in some scenarios, you might want to make ER formats use parameters that are related to a specific legal entity.</span></span> <span data-ttu-id="dc6ab-135">Aðeins í þessum tilfellum ætti að nota val á sjálfgefnu fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-135">In these scenarios only, you should use the default company switcher.</span></span> <span data-ttu-id="dc6ab-136">Til dæmis sjá [Grunnstilla ER-snið til að nota færibreytur sem eru tilgreindar fyrir hvern lögaðila](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).</span><span class="sxs-lookup"><span data-stu-id="dc6ab-136">For an example, see [Configure ER format to use parameters that are specified per legal entity](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).</span></span>

## <a name="related-rcs-documentation"></a><span data-ttu-id="dc6ab-137">Tengd RCS-fylgigögn</span><span class="sxs-lookup"><span data-stu-id="dc6ab-137">Related RCS documentation</span></span>

<span data-ttu-id="dc6ab-138">Frekari upplýsingar um tengda þætti er að finna í eftirfarandi efnisatriðum:</span><span class="sxs-lookup"><span data-stu-id="dc6ab-138">For more information about related components, see the following topics:</span></span>

- <span data-ttu-id="dc6ab-139">**RCS:**</span><span class="sxs-lookup"><span data-stu-id="dc6ab-139">**RCS:**</span></span>

    - [<span data-ttu-id="dc6ab-140">Stofna skilgreiningar rafrænnar skýrslugerðar í RCS og hlaða þeim upp í altæka geymslu</span><span class="sxs-lookup"><span data-stu-id="dc6ab-140">Create ER configurations in RCS and upload them to the Global repository</span></span>](rcs-global-repo-upload.md)

- <span data-ttu-id="dc6ab-141">**Altæk geymsla:**</span><span class="sxs-lookup"><span data-stu-id="dc6ab-141">**Global repository:**</span></span>

    - [<span data-ttu-id="dc6ab-142">Búa til skilgreiningu rafrænnar skýrslugerðar og hlaða upp í altæka geymslu</span><span class="sxs-lookup"><span data-stu-id="dc6ab-142">Create ER configuration & upload to Global repo</span></span>](rcs-global-repo-upload.md)
    - [<span data-ttu-id="dc6ab-143">Deila skilgreiningum í altækri geymslu</span><span class="sxs-lookup"><span data-stu-id="dc6ab-143">Share configuration in Global repo</span></span>](rcs-global-repo-share-configuration.md)
    - [<span data-ttu-id="dc6ab-144">Aukin síun í altækri geymslu</span><span class="sxs-lookup"><span data-stu-id="dc6ab-144">Enhanced filtering in Global repo</span></span>](enhanced-filtering-global-repo.md)
    - [<span data-ttu-id="dc6ab-145">Sækja skilgreiningar rafrænnar skýrslugerðar úr altækri geymslu</span><span class="sxs-lookup"><span data-stu-id="dc6ab-145">Download ER configurations from the Global repository</span></span>](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [<span data-ttu-id="dc6ab-146">Hætta með skilgreiningar í altækri geymslu</span><span class="sxs-lookup"><span data-stu-id="dc6ab-146">Discontinuing configurations in Global repo</span></span>](discontinuing-configurations-rcs-global-repo.md)
    - [<span data-ttu-id="dc6ab-147">Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) úrelding á geymslu</span><span class="sxs-lookup"><span data-stu-id="dc6ab-147">Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation</span></span>](rcs-lcs-repo-dep-faq.md)

- <span data-ttu-id="dc6ab-148">**Altækur eiginleiki:**</span><span class="sxs-lookup"><span data-stu-id="dc6ab-148">**Globalization feature:**</span></span>

    - [<span data-ttu-id="dc6ab-149">Regulatory Configuration Service (RCS) – altækur eiginleiki</span><span class="sxs-lookup"><span data-stu-id="dc6ab-149">Regulatory Configuration Service (RCS) - Globalization feature</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)


## <a name="troubleshooting-rcs-sign-up"></a><span data-ttu-id="dc6ab-150">Úrræðaleit vegna RCS-nýskráningar</span><span class="sxs-lookup"><span data-stu-id="dc6ab-150">Troubleshooting RCS sign-up</span></span>

<span data-ttu-id="dc6ab-151">Þegar þú skráir þig fyrir RCS af þjónustusíðunni gæti komið upp vandamál sem tengist Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="dc6ab-151">When you sign up for RCS from the service page, you might encounter an issue that is related to Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="dc6ab-152">Villuboðin sem koma upp gefa til kynna að slökkt er á skráningu fyrir RCS og kveikja þarf á henni áður en hægt er að klára skráningarferlið.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-152">The error message that you receive indicates that sign-up for RCS is currently turned off and must be turned on before you can complete the sign-up process.</span></span>

![Villuboð RCS-skráningar](media/01_RCSSignUpError.jpg)

<span data-ttu-id="dc6ab-154">Vandamálið kemur upp vegna þess að lokað er fyrir skráningu á tilfallandi áskriftum og virkja þarf eiginleikann `AllowAdHocSubscriptions` í leigjandanum.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-154">The issue occurs because you're blocked from signing up for ad-hoc subscriptions, and the `AllowAdHocSubscriptions` property must be enabled in your tenant.</span></span> 

- <span data-ttu-id="dc6ab-155">Ef tæknideildin stjórnar Azure-leigjendum fyrirtækisins skal hafa samband við þá deild og láta vita af vandanum.</span><span class="sxs-lookup"><span data-stu-id="dc6ab-155">If your IT department manages your organization's Azure tenants, contact that department to report the issue.</span></span>
- <span data-ttu-id="dc6ab-156">Ef þú berð ábyrgð á umsjón leigjenda Azure getur þú leyst úr vandamálunum með því að fylgja skrefunum í [Hvað er nýskráning í sjálfsafgreiðslu fyrir Azure Active Directory](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).</span><span class="sxs-lookup"><span data-stu-id="dc6ab-156">If you're responsible for managing your Azure tenants, you can fix the issues by following the steps in [What is self-service sign-up for Azure Active Directory](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).</span></span>
