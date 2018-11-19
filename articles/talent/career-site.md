---
title: "Virkni starfatorgs í Attract"
description: "Þessi grein veitir yfirlit um starfatorg sem snýr að umsækjendum í Microsoft Dynamics 365 for Talent - Attract. Það útskýrir einnig hvernig á að setja upp þessa virkni."
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 452e3e92ea32ab5f1e3720ab81ff2f7ea18b2a06
ms.contentlocale: is-is
ms.lasthandoff: 10/22/2018

---
# <a name="career-site-functionality-in-attract"></a><span data-ttu-id="475c6-104">Virkni starfatorgs í Attract</span><span class="sxs-lookup"><span data-stu-id="475c6-104">Career site functionality in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="475c6-105">Þessi grein veitir yfirlit um starfatorg sem snýr að umsækjendum í Microsoft Dynamics 365 for Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="475c6-105">This article provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="475c6-106">Það útskýrir einnig hvernig á að setja upp þessa virkni.</span><span class="sxs-lookup"><span data-stu-id="475c6-106">It also explains how to set up this functionality.</span></span>

## <a name="overview"></a><span data-ttu-id="475c6-107">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="475c6-107">Overview</span></span>

<span data-ttu-id="475c6-108">Attract býður upp á eitt starfatorg fyrir hvert umhverfi í leigjanda.</span><span class="sxs-lookup"><span data-stu-id="475c6-108">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="475c6-109">Til dæmis, ef fyrirtæki hefur þróunarumhverfi og prófunarumhverfi er eitt starfatorg búð til fyrir þróunarumhverfið og annað starfatorg búið til fyrir prófunarumhverfið.</span><span class="sxs-lookup"><span data-stu-id="475c6-109">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="475c6-110">Hvert starfatorg er **fullkomlega einangrað** og hefur eigið sannvottunarkerfi.</span><span class="sxs-lookup"><span data-stu-id="475c6-110">Each career site is **completely isolated** and has its own authentication mechanism.</span></span> <span data-ttu-id="475c6-111">Störf og síðum umsækjenda er ekki deilt á milli starfatorga.</span><span class="sxs-lookup"><span data-stu-id="475c6-111">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="475c6-112">Sjálfgefið er að starfatorgið sé opinbert.</span><span class="sxs-lookup"><span data-stu-id="475c6-112">By default, the career site is public.</span></span> <span data-ttu-id="475c6-113">Þar af leiðandi geta umsækjendur skoðað öll störf sem eru merkt sem ytri án þess að þurfa að skrá sig inn.</span><span class="sxs-lookup"><span data-stu-id="475c6-113">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="475c6-114">Hins vegar kalla allar aðrar aðgerðir á að umsækjendur skrái sig inn.</span><span class="sxs-lookup"><span data-stu-id="475c6-114">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="475c6-115">Stjórnun ferilssíðu</span><span class="sxs-lookup"><span data-stu-id="475c6-115">Career site management</span></span>

<span data-ttu-id="475c6-116">Eftirfarandi atriði á starfatorginu eru stjórnað af stillingum:</span><span class="sxs-lookup"><span data-stu-id="475c6-116">The following items on the career site are controlled by settings:</span></span>

- <span data-ttu-id="475c6-117">**Heiti fyrirtækisins:** Heiti fyrirtækisins birtist á yfirlitsstikunni efst á starfatorginu.</span><span class="sxs-lookup"><span data-stu-id="475c6-117">**Organization name:** The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="475c6-118">Með því að velja heiti fyrirtækisins, fara umsækjendur á síðu sem sýnir alla opna störf.</span><span class="sxs-lookup"><span data-stu-id="475c6-118">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>
- <span data-ttu-id="475c6-119">**Merki fyrirtæksins** Mynd af merki fyrirtækisins birtist efst til vinstri á starfatorginu.</span><span class="sxs-lookup"><span data-stu-id="475c6-119">**Organization logo:** An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="475c6-120">Með því að velja merkið fara umsækjendur á síðu sem sýnir alla opna störf.</span><span class="sxs-lookup"><span data-stu-id="475c6-120">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

<span data-ttu-id="475c6-121">Til að stilla gildin fyrir heiti og merki fyrirtæksins, skráðu þig inn í Attract sem stjórnandi, veldu **Stjórnendamiðstöð** á **Stillingar** valmyndinni (gírtáknið) og veldu síðan flipann **Fyrirtækisupplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="475c6-121">To set the values for the organization name and logo, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="475c6-122">Merkið sem birtist á starfatorginu hefur fastsetta hæð sem nemur 20 pixlum (px).</span><span class="sxs-lookup"><span data-stu-id="475c6-122">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="475c6-123">Myndin sem þú bætir við í stjórnendastöðinni er minnkuð til að passa.</span><span class="sxs-lookup"><span data-stu-id="475c6-123">The image that you add in the Admin center is scaled to fit.</span></span> <span data-ttu-id="475c6-124">Þess vegna getur breiddin breyst, allt eftir myndinni.</span><span class="sxs-lookup"><span data-stu-id="475c6-124">Therefore, depending on the image, the width might change.</span></span>

## <a name="career-site-url"></a><span data-ttu-id="475c6-125">Vefslóð starfatorgsins</span><span class="sxs-lookup"><span data-stu-id="475c6-125">Career site URL</span></span>

<span data-ttu-id="475c6-126">Þegar þú [auglýsir ytra starf](./Creating-jobs-Attract.md#postings) í fyrsta skipti getur þú afritað **Sækja um** tengilinn frá Attract-forritinu.</span><span class="sxs-lookup"><span data-stu-id="475c6-126">When you [post an external job](./Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from the Attract application.</span></span> <span data-ttu-id="475c6-127">Slóðin fyrir þennan tengil verður í eftirfarandi sniði: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span><span class="sxs-lookup"><span data-stu-id="475c6-127">The URL for this link will be in the following format: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span></span>

<span data-ttu-id="475c6-128">Vefslóð starfatorgsins er undirstrengur á **Sækja um** vefslóðinni.</span><span class="sxs-lookup"><span data-stu-id="475c6-128">The URL of the career site is a substring of the **Apply** URL.</span></span> <span data-ttu-id="475c6-129">Það samanstendur af öllu að heiti fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="475c6-129">It consists of everything up through the company name.</span></span> <span data-ttu-id="475c6-130">Þar af leiðandi fyrir fyrri **Sækja um** vefslóðina er vefslóð starfatorgsins `https://jobs.talent.dynamics.com/jobs/<company_name>/`.</span><span class="sxs-lookup"><span data-stu-id="475c6-130">Therefore, for the preceding **Apply** URL, the career site URL is `https://jobs.talent.dynamics.com/jobs/<company_name>/`.</span></span>

## <a name="authentication-options"></a><span data-ttu-id="475c6-131">Valkostir sannvottunar</span><span class="sxs-lookup"><span data-stu-id="475c6-131">Authentication options</span></span>

<span data-ttu-id="475c6-132">Umsækjendur hafa eftirfarandi innskráningarmöguleika fyrir Attract-starfatorg:</span><span class="sxs-lookup"><span data-stu-id="475c6-132">Candidates have the following sign-in options for an Attract career site:</span></span>

- <span data-ttu-id="475c6-133">Einkareikningur:</span><span class="sxs-lookup"><span data-stu-id="475c6-133">Personal account:</span></span>

    - <span data-ttu-id="475c6-134">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="475c6-134">LinkedIn</span></span>
    - <span data-ttu-id="475c6-135">Microsoft </span><span class="sxs-lookup"><span data-stu-id="475c6-135">Microsoft</span></span>
    - <span data-ttu-id="475c6-136">Google</span><span class="sxs-lookup"><span data-stu-id="475c6-136">Google</span></span>
    - <span data-ttu-id="475c6-137">Facebook</span><span class="sxs-lookup"><span data-stu-id="475c6-137">Facebook</span></span>

- <span data-ttu-id="475c6-138">Vinnu- eða skólareikningur:</span><span class="sxs-lookup"><span data-stu-id="475c6-138">Work or school account:</span></span>

    - <span data-ttu-id="475c6-139">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="475c6-139">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="475c6-140">Azure AD-innskráning er aðeins ætlað fyrir innri umsækjendur.</span><span class="sxs-lookup"><span data-stu-id="475c6-140">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="475c6-141">Þar af leiðandi virkar það aðeins fyrir innri umsækjendur sem Azure AD-skilríki fyrirtækisins síns.</span><span class="sxs-lookup"><span data-stu-id="475c6-141">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="475c6-142">Til dæmis, umsækjandi sem er nú starfsmaður Contoso Ltd vill sækja um starf í ótengdum fyrirtækjum, Alpine Ski House.</span><span class="sxs-lookup"><span data-stu-id="475c6-142">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="475c6-143">Í þessu tilviki mun innskráningin ekki ná árangri ef starfsmaðurinn reynir að nota Azure AD-skilríki sín frá Contoso Ltd.</span><span class="sxs-lookup"><span data-stu-id="475c6-143">In this case, the sign-in will be unsuccessful if the employee tries to use his or her Azure AD credentials from Contoso Ltd.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="475c6-144">Stofna og viðhalda síðu</span><span class="sxs-lookup"><span data-stu-id="475c6-144">Create and maintain a profile</span></span>

<span data-ttu-id="475c6-145">Eftir að umsækjendur hafa skráð sig inn á starfatorgið, geta þeir valið **Síðan mín** á yfirlitsstikunni efst á síðunni til að stofna og viðhalda síðunni sinni.</span><span class="sxs-lookup"><span data-stu-id="475c6-145">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span> <span data-ttu-id="475c6-146">Síðan inniheldur persónulegar upplýsingar, upplýsingar um starfsreynslu, upplýsingar um menntun, skjöl, tengla og upplýsingar um sérþekkingu.</span><span class="sxs-lookup"><span data-stu-id="475c6-146">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="475c6-147">Eftir að síðan er stofnuð er hægt að nota hana til að sækja um störf sem umsækjandi hefur áhuga á.</span><span class="sxs-lookup"><span data-stu-id="475c6-147">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="475c6-148">Síður hjálpa einnig Attract að mæla með rétt störfum fyrir umsækjendur.</span><span class="sxs-lookup"><span data-stu-id="475c6-148">Profiles also help Attract recommend the right jobs to candidates.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="475c6-149">Finndu rétta starfið</span><span class="sxs-lookup"><span data-stu-id="475c6-149">Find the right job</span></span>

<span data-ttu-id="475c6-150">Á starfassíðunni geta umsækjendur leitað að tilteknu starfi með því að slá inn leitarorð.</span><span class="sxs-lookup"><span data-stu-id="475c6-150">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="475c6-151">Leitin finnur leitarorðin í starfsheiti og starfslýsingar og sýnir viðeigandi störf sem niðurstöður.</span><span class="sxs-lookup"><span data-stu-id="475c6-151">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="475c6-152">Umsækjendur geta síað niðurstöðurnar hvenær sem er, byggt á staðsetningu starfs eða starfshlutverki.</span><span class="sxs-lookup"><span data-stu-id="475c6-152">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="475c6-153">Umsækjendur geta einnig skoðað safn af ráðlögðum störfum á starfatorginu.</span><span class="sxs-lookup"><span data-stu-id="475c6-153">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="475c6-154">Starfið sem mælt er með fyrir umsækjanda byggist á fyrri umsóknum umsækjenda, síðu hans og ferilsskrá.</span><span class="sxs-lookup"><span data-stu-id="475c6-154">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

> [!NOTE]
> <span data-ttu-id="475c6-155">Tillögur að störfum eru aðeins sýnd ef að minnsta kosti 10 störf eru settar fram á starfatorginu og ef umsækjandi hefur lokið við uppsetningu síðu sinnar.</span><span class="sxs-lookup"><span data-stu-id="475c6-155">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed his or her profile.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="475c6-156">Sækja um störf</span><span class="sxs-lookup"><span data-stu-id="475c6-156">Apply for jobs</span></span>

<span data-ttu-id="475c6-157">Eftir að umsækjendur hafa fundið rétt starf, þá geta þeir sótt um með því að nota **Sækja um** hnappinn á upplýsingasíðu starfsins.</span><span class="sxs-lookup"><span data-stu-id="475c6-157">After candidates find the right job, they can apply by using the **Apply** button on the job details page.</span></span> <span data-ttu-id="475c6-158">Á þessum tímapunkti geta umsækjendur annaðhvort búið til splunkunýja síðu eða endurskoðað upplýsingarnar í núverandi síðu.</span><span class="sxs-lookup"><span data-stu-id="475c6-158">At this point, candidates can either create a brand-new profile or review the information in their existing profile.</span></span> <span data-ttu-id="475c6-159">Umsækjendur geta einnig hlaðið upp ferilskrá, eftir því sem þörf krefur, og síðan sent inn starfsumsóknina.</span><span class="sxs-lookup"><span data-stu-id="475c6-159">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="475c6-160">Athuga stöðu umsóknar</span><span class="sxs-lookup"><span data-stu-id="475c6-160">Check application status</span></span>

<span data-ttu-id="475c6-161">Eftir að umsækjendur hafa sótt um eitt eða fleiri störf, geta þeir valið **Umsóknir** á yfirlitsstikunni efst á síðunni til að skoða opnar og lokaðar umsóknir sínar.</span><span class="sxs-lookup"><span data-stu-id="475c6-161">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="475c6-162">Þegar umsækjendur opna eitt af umsóknunum sínum sjá þeir núverandi stig og aðgerðaratriði sem bíða eftir að þeir ljúki þeim.</span><span class="sxs-lookup"><span data-stu-id="475c6-162">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="475c6-163">Til dæmis, ef umsækjandi verður að gefa upp hugsanlegar dagsetningar fyrir viðtal í eigin persónu, sýnir síðan valkostina hans.</span><span class="sxs-lookup"><span data-stu-id="475c6-163">For example, if a candidate must provide potential dates for an in-person interview, the page shows his or her options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="475c6-164">Innri störf</span><span class="sxs-lookup"><span data-stu-id="475c6-164">Internal jobs</span></span>

<span data-ttu-id="475c6-165">Nú birtast störf sem eru merktar sem innri störf og sett fram á Attract-svæðinu ekki á starfatorginu.</span><span class="sxs-lookup"><span data-stu-id="475c6-165">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="475c6-166">Þau eru aðeins aðgengileg í gegnum að **Sækja um** beint á vefslóðinni sem hægt er að afrita úr Attract-forritinu.</span><span class="sxs-lookup"><span data-stu-id="475c6-166">They are accessible only via the direct **Apply** URL that can be copied from the Attract application.</span></span>

