---
title: Virkni starfatorgs í Attract
description: Þessi efnisatriði veitir yfirlit yfir starfatorg sem snýr að umsækjendum í Attract.
author: josaw1
manager: AnnBe
ms.date: 02/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: 087ab4034a1e601e7f3514c77d56ef54b0c5c52d
ms.sourcegitcommit: 1ee613a88edddab036d145f27f19d071a4b8ad24
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/13/2019
ms.locfileid: "389968"
---
# <a name="career-site-functionality-in-attract"></a><span data-ttu-id="8fe0b-103">Virkni starfatorgs í Attract</span><span class="sxs-lookup"><span data-stu-id="8fe0b-103">Career site functionality in Attract</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8fe0b-104">Þetta efnisatriði veitir yfirlit um starfatorg sem snýr að umsækjendum í Microsoft Dynamics 365 for Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-104">This topic provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="8fe0b-105">Það útskýrir einnig hvernig á að setja upp þessa virkni.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-105">It also explains how to set up this functionality.</span></span>

<span data-ttu-id="8fe0b-106">Attract býður upp á eitt starfatorg fyrir hvert umhverfi í leigjanda.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-106">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="8fe0b-107">Til dæmis, ef fyrirtæki hefur þróunarumhverfi og prófunarumhverfi er eitt starfatorg búð til fyrir þróunarumhverfið og annað starfatorg búið til fyrir prófunarumhverfið.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-107">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="8fe0b-108">Hvert starfatorg er fullkomlega einangrað og hefur eigið sannvottunarkerfi.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-108">Each career site is completely isolated and has its own authentication mechanism.</span></span> <span data-ttu-id="8fe0b-109">Störf og síðum umsækjenda er ekki deilt á milli starfatorga.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-109">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="8fe0b-110">Sjálfgefið er að starfatorgið sé opinbert.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-110">By default, the career site is public.</span></span> <span data-ttu-id="8fe0b-111">Þar af leiðandi geta umsækjendur skoðað öll störf sem eru merkt sem ytri án þess að þurfa að skrá sig inn.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-111">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="8fe0b-112">Hins vegar kalla allar aðrar aðgerðir á að umsækjendur skrái sig inn.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-112">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="8fe0b-113">Stjórnun ferilssíðu</span><span class="sxs-lookup"><span data-stu-id="8fe0b-113">Career site management</span></span>

<span data-ttu-id="8fe0b-114">Til að stilla gildin fyrir eftirfarandi atriði, skráðu þig inn í Attract sem stjórnandi, veldu **Stjórnendamiðstöð** á **Stillingar** valmyndinni (gírtáknið) og veldu síðan flipann **Fyrirtækisupplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-114">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

-   <span data-ttu-id="8fe0b-115">**Heiti fyrirtækisins** - Heiti fyrirtækisins birtist á yfirlitsstikunni efst á starfatorginu.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-115">**Organization name** - The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="8fe0b-116">Með því að velja heiti fyrirtækisins, fara umsækjendur á síðu sem sýnir alla opna störf.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-116">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>

-   <span data-ttu-id="8fe0b-117">**Merki fyrirtækisins** - Mynd af merki fyrirtækisins birtist efst til vinstri á starfatorginu.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-117">**Organization logo** - An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="8fe0b-118">Með því að velja merkið fara umsækjendur á síðu sem sýnir alla opna störf.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-118">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

    >   [!NOTE] 
    >   <span data-ttu-id="8fe0b-119">Merkið sem birtist á starfatorginu hefur fastsetta hæð sem nemur 20 pixlum (px).</span><span class="sxs-lookup"><span data-stu-id="8fe0b-119">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="8fe0b-120">Myndin sem þú bætir við í stjórnendastöðinni er minnkuð til að passa.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-120">The image that you add in the Admin center is scaled to fit.</span></span> <span data-ttu-id="8fe0b-121">Þess vegna getur breiddin breyst, allt eftir myndinni.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-121">Therefore, depending on the image, the width might change.</span></span>
 
<span data-ttu-id="8fe0b-122">Til að stilla gildin fyrir eftirfarandi atriði, skráðu þig inn í Attract sem stjórnandi, veldu **Stjórnendamiðstöð** á **Stillingar** valmyndinni og veldu síðan flipann **Starfatorg umsækjanda**.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-122">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="8fe0b-123">**Leitarvélabestun** - Ef virkt verður hægt að leita að öllum almennum störfum sem birtast í starfatorgi Attract þegar leitarvélar eins og Bing og Google eru notaðar.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-123">**Search Engine Optimization** - When enabled, all public jobs posted to Attract career site will be searchable using search engines like Bing and Google.</span></span>

    >   [!NOTE] 
    >   <span data-ttu-id="8fe0b-124">Það gæti orðið tafir á milli þess að kveikja á þessari stillingu og leitarniðurstöður birtast, fer allt eftir leitarvélinni sem þú notar.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-124">There might be a delay between turning this setting on and search results appearing, depending on the search engine that you are using.</span></span>
         
## <a name="career-site-urls"></a><span data-ttu-id="8fe0b-125">Vefslóðir starfatorgs</span><span class="sxs-lookup"><span data-stu-id="8fe0b-125">Career site URLs</span></span>

<span data-ttu-id="8fe0b-126">Eftirfarandi listi inniheldur algengar vefslóðir starfatorga og hvernig skuli nálgast þau.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-126">The following list contains the commonly used career site URLs and how to access them.</span></span>

-   <span data-ttu-id="8fe0b-127">**Vefslóð á heimasíðu starfatorgs** - Til að sjá vefslóð á heimasíðu starfatorgs skaltu skrá þig inn í Attract sem stjórnandi, veldu **Stjórnendamiðstöð** á **Stillingar** valmyndinni og veldu síðan flipann **Starfatorg umsækjanda**.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-127">**Career site home page URL** - To view the career site home page URL, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="8fe0b-128">**Vefslóð til að sækja um auglýst starf** - Þegar þú [auglýsir ytra starf](Creating-jobs-Attract.md#postings) í fyrsta skipti getur þú afritað **Sækja um** tengilinn frá Attract-forritinu.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-128">**Individual job post apply URL** - When you [post an external job](Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from the Attract application.</span></span> <span data-ttu-id="8fe0b-129">Slóðin fyrir þennan tengil verður í eftirfarandi sniði: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span><span class="sxs-lookup"><span data-stu-id="8fe0b-129">The URL for this link will be in the following format: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span></span>

-   <span data-ttu-id="8fe0b-130">**Vefslóð fyrir auglýst starf** - Vefslóð auglýsts starfs er undirstrengur á Sækja um vefslóðinni.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-130">**Individual job post URL** - The URL of the job post is a substring of the Apply URL.</span></span> <span data-ttu-id="8fe0b-131">Hún samanstendur af öllu sem tengist númeri starfs.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-131">It consists of everything up through the job number.</span></span> <span data-ttu-id="8fe0b-132">Þar af leiðandi fyrir fyrri Sækja um vefslóðina er vefslóð auglýsta starfsins [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)</span><span class="sxs-lookup"><span data-stu-id="8fe0b-132">Therefore, for the preceding Apply URL, the job post URL is [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)</span></span>

## <a name="authentication-options"></a><span data-ttu-id="8fe0b-133">Valkostir sannvottunar</span><span class="sxs-lookup"><span data-stu-id="8fe0b-133">Authentication options</span></span>

<span data-ttu-id="8fe0b-134">Umsækjendur hafa eftirfarandi innskráningarmöguleika fyrir Attract-starfatorg:</span><span class="sxs-lookup"><span data-stu-id="8fe0b-134">Candidates have the following sign-in options for an Attract career site:</span></span>

-   <span data-ttu-id="8fe0b-135">Einkareikningur:</span><span class="sxs-lookup"><span data-stu-id="8fe0b-135">Personal account:</span></span>

    -   <span data-ttu-id="8fe0b-136">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="8fe0b-136">LinkedIn</span></span>

    -   <span data-ttu-id="8fe0b-137">Microsoft </span><span class="sxs-lookup"><span data-stu-id="8fe0b-137">Microsoft</span></span>

    -   <span data-ttu-id="8fe0b-138">Google</span><span class="sxs-lookup"><span data-stu-id="8fe0b-138">Google</span></span>

    -   <span data-ttu-id="8fe0b-139">Facebook</span><span class="sxs-lookup"><span data-stu-id="8fe0b-139">Facebook</span></span>

-   <span data-ttu-id="8fe0b-140">Vinnu- eða skólareikningur:</span><span class="sxs-lookup"><span data-stu-id="8fe0b-140">Work or school account:</span></span>

    -   <span data-ttu-id="8fe0b-141">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="8fe0b-141">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="8fe0b-142">Azure AD innskráning er aðeins ætluð fyrir innri umsækjendur.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-142">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="8fe0b-143">Þar af leiðandi virkar það aðeins fyrir innri umsækjendur sem nota Azure AD skilríki fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-143">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="8fe0b-144">Til dæmis, umsækjandi sem er nú starfsmaður Contoso Ltd vill sækja um starf í ótengdum fyrirtækjum, Alpine Ski House.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-144">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="8fe0b-145">Í þessu tilviki mun innskráningin ekki ná árangri ef starfsmaðurinn reynir að nota Azure AD skilríki frá Contoso Ltd.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-145">In this case, the sign-in will be unsuccessful if the employee tries to use Azure AD credentials from Contoso Ltd.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="8fe0b-146">Stofna og viðhalda síðu</span><span class="sxs-lookup"><span data-stu-id="8fe0b-146">Create and maintain a profile</span></span>

<span data-ttu-id="8fe0b-147">Eftir að umsækjendur hafa skráð sig inn á starfatorgið, geta þeir valið **Síðan mín** á yfirlitsstikunni efst á síðunni til að stofna og viðhalda síðunni sinni.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-147">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span>
<span data-ttu-id="8fe0b-148">Síðan inniheldur persónulegar upplýsingar, upplýsingar um starfsreynslu, upplýsingar um menntun, skjöl, tengla og upplýsingar um sérþekkingu.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-148">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="8fe0b-149">Eftir að síðan er stofnuð er hægt að nota hana til að sækja um störf sem umsækjandi hefur áhuga á.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-149">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="8fe0b-150">Síður hjálpa einnig Attract að mæla með rétt störfum fyrir umsækjendur.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-150">Profiles also help Attract recommend the right jobs to candidates.</span></span>

>   [!NOTE]
>   <span data-ttu-id="8fe0b-151">Ef umsækjandi notar tölvupóstsauðkenni til að skrá þig inn með því að nota eina af sannvottunarþjónustunum sem taldir eru upp hér að ofan, mun þetta tölvupóstsauðkenni verða sjálfgefið að tölvupóstsauðkenni tengiliðar sem tengist prófílnum.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-151">If a candidate uses an email ID to sign in using one of the authentication providers listed above, that email ID will default to the contact email ID associated with the profile.</span></span> <span data-ttu-id="8fe0b-152">Hins vegar er hægt að breyta seinni tölvupóstinum hvenær sem er og er algjörlega óháð fyrri tölvupóstinum.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-152">However, the latter can be changed at any time and is completely independent of the former.</span></span> <span data-ttu-id="8fe0b-153">Attract mun alltaf nota kenni tengiliðanetfangsins til að tengja við prófílinn þinn fyrir öll tölvupóstsamskipti.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-153">Attract will always use the contact email ID to associate with your profile for all email communications.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="8fe0b-154">Finndu rétta starfið</span><span class="sxs-lookup"><span data-stu-id="8fe0b-154">Find the right job</span></span>

<span data-ttu-id="8fe0b-155">Á starfassíðunni geta umsækjendur leitað að tilteknu starfi með því að slá inn leitarorð.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-155">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="8fe0b-156">Leitin finnur leitarorðin í starfsheiti og starfslýsingar og sýnir viðeigandi störf sem niðurstöður.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-156">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="8fe0b-157">Umsækjendur geta síað niðurstöðurnar hvenær sem er, byggt á staðsetningu starfs eða starfshlutverki.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-157">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="8fe0b-158">Umsækjendur geta einnig skoðað safn af ráðlögðum störfum á starfatorginu.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-158">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="8fe0b-159">Starfið sem mælt er með fyrir umsækjanda byggist á fyrri umsóknum umsækjenda, síðu hans og ferilsskrá.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-159">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

>   [!NOTE] 
>   <span data-ttu-id="8fe0b-160">Tillögur að störfum eru aðeins sýnd ef að minnsta kosti 10 störf eru birt á starfatorginu og ef umsækjandi hefur lokið við notandasíðu.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-160">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed a profile.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="8fe0b-161">Sækja um störf</span><span class="sxs-lookup"><span data-stu-id="8fe0b-161">Apply for jobs</span></span>

<span data-ttu-id="8fe0b-162">Eftir að umsækjendur hafa fundið rétt starf, þá geta þeir sótt um með því að nota **Sækja um** hnappinn á síðunni **Starfsupplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-162">After candidates find the right job, they can apply by using the **Apply** button on the **Job details** page.</span></span> <span data-ttu-id="8fe0b-163">Á þessum tímapunkti geta umsækjendur annaðhvort búið til nýja síðu eða endurskoðað upplýsingarnar á núverandi síðu.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-163">At this point, candidates can either create a new profile or review the information in their existing profile.</span></span>
<span data-ttu-id="8fe0b-164">Umsækjendur geta einnig hlaðið upp ferilskrá, eftir því sem þörf krefur, og síðan sent inn starfsumsóknina.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-164">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="8fe0b-165">Athuga stöðu umsóknar</span><span class="sxs-lookup"><span data-stu-id="8fe0b-165">Check application status</span></span>

<span data-ttu-id="8fe0b-166">Eftir að umsækjendur hafa sótt um eitt eða fleiri störf, geta þeir valið **Umsóknir** á yfirlitsstikunni efst á síðunni til að skoða opnar og lokaðar umsóknir sínar.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-166">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="8fe0b-167">Þegar umsækjendur opna eitt af umsóknunum sínum sjá þeir núverandi stig og aðgerðaratriði sem bíða eftir að þeir ljúki þeim.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-167">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="8fe0b-168">Til dæmis, ef umsækjandi verður að gefa upp hugsanlegar dagsetningar fyrir viðtal í eigin persónu, sýnir síðan tiltæka valkosti.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-168">For example, if a candidate must provide potential dates for an in-person interview, the page shows the available options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="8fe0b-169">Innri störf</span><span class="sxs-lookup"><span data-stu-id="8fe0b-169">Internal jobs</span></span>

<span data-ttu-id="8fe0b-170">Nú birtast störf sem eru merktar sem innri störf og sett fram á Attract-svæðinu ekki á starfatorginu.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-170">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="8fe0b-171">Þau eru aðeins aðgengileg með því að nota vefslóðina **Sækja um** beint sem hægt er að afrita úr Attract-forritinu.</span><span class="sxs-lookup"><span data-stu-id="8fe0b-171">They are only accessible using the direct **Apply** URL that can be copied from the Attract application.</span></span>
