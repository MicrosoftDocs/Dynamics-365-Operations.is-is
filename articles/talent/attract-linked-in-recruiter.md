---
title: Fundið með LinkedIn Recruiter
description: Þetta efnisatriði veitir upplýsingar um að vélnám til að fá ráðleggingar um störf og umsækjendur.
author: andreabichsel
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 4ac7a302e5bf589beb2b560b0ff5818e90c67139
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518236"
---
# <a name="sourcing-with-linkedin-recruiter"></a><span data-ttu-id="b7277-103">Fundið með LinkedIn Recruiter</span><span class="sxs-lookup"><span data-stu-id="b7277-103">Sourcing with LinkedIn Recruiter</span></span>
[!include[banner](../includes/banner.md)]

<span data-ttu-id="b7277-104">LinkedIn er stærsti gagnagrunnur umsækjenda í heimiog oft aðalkerfið sem ráðningaraðilar nota til að finna, hafa samskipti við og finna umsækjendur fyrir þau störf sem ráðningaraðilar vilja ráða í.</span><span class="sxs-lookup"><span data-stu-id="b7277-104">LinkedIn is the world’s largest talent database and often the primary system that recruiters use to find, communicate with, and source candidates for the jobs that recruiters are looking to fill.</span></span> <span data-ttu-id="b7277-105">LinkedIn Recruiter samþætting með Dynamics 365 for Talent: Attract gerir það auðveldara fyrir notendur að ráða og að halda gögnunum í samstillingu milli kerfanna tveggja.</span><span class="sxs-lookup"><span data-stu-id="b7277-105">LinkedIn Recruiter integration with Dynamics 365 for Talent: Attract makes it easier for users to hire, and to keep the data in sync between the two systems.</span></span>

> [!NOTE]
> <span data-ttu-id="b7277-106">Þú þarft viðbót við alhliða ráðningar og LinkedIn Recruiter sæti til að geta notað LinkedIn Recruiter samþættingu við Attract.</span><span class="sxs-lookup"><span data-stu-id="b7277-106">You need the Comprehensive hiring add-on and LinkedIn Recruiter seats to be able to use LinkedIn Recruiter integration with Attract.</span></span>

## <a name="set-up-linkedin-recruiter-with-attract"></a><span data-ttu-id="b7277-107">Setja upp LinkedIn Recruiter með Attract</span><span class="sxs-lookup"><span data-stu-id="b7277-107">Set up LinkedIn Recruiter with Attract</span></span> 

<span data-ttu-id="b7277-108">Áður en þú getur notað LinkedIn Recruiter eiginleika þarftu að stilla samningsstig eða aðgang innan fyrirtækisins fyrir tilvikið í Attract.</span><span class="sxs-lookup"><span data-stu-id="b7277-108">Before you can use the LinkedIn Recruiter capabilities, you must configure contract-level or company-level access with your Attract instance.</span></span> <span data-ttu-id="b7277-109">Til að ljúka skilgreiningarferlinu verður þú að vinna með notandanum sem er stjórnandi á LinkedIn Recruiter samningnum þínum.</span><span class="sxs-lookup"><span data-stu-id="b7277-109">To complete the configuration process, you must work with the user who is an Admin on your LinkedIn Recruiter contract.</span></span> <span data-ttu-id="b7277-110">Ljúktu eftirfarandi skrefum til að skilgreina LinkedIn Recruiter með Attract.</span><span class="sxs-lookup"><span data-stu-id="b7277-110">Complete the following steps to configure LinkedIn Recruiter with Attract.</span></span>

1.  <span data-ttu-id="b7277-111">Skráðu þig inn í Attract sem stjórnanda og farðu í **Stjórnandastillingar**.</span><span class="sxs-lookup"><span data-stu-id="b7277-111">Sign in to Attract as an Admin and go to **Admin Settings**.</span></span>

2.  <span data-ttu-id="b7277-112">Smelltu á **LinkedIn-samþætting** flipann í vinstri glugganum.</span><span class="sxs-lookup"><span data-stu-id="b7277-112">On the left pane, click the **LinkedIn Integration** tab.</span></span>

<span data-ttu-id="b7277-113">[![Yfirlit Attract stjórnanda til að hefja LinkedIn Recruiter-samþættingu](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span><span class="sxs-lookup"><span data-stu-id="b7277-113">[![Attract Admin view to start LinkedIn Recruiter integration](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span></span>

3.  <span data-ttu-id="b7277-114">Smelltu á **Tengja** til að hefja uppsetninguna og fá leiðsögn fyrir LinkedIn innskráningu.</span><span class="sxs-lookup"><span data-stu-id="b7277-114">Click **Connect** to start the setup and be guided through the LinkedIn sign-in process.</span></span>

4.  <span data-ttu-id="b7277-115">Ef þú hefur sæti á mörgum LinkedIn samningum skaltu velja samninginn sem þú vilt tengja við Attract-kerfið.</span><span class="sxs-lookup"><span data-stu-id="b7277-115">If you have seats on multiple LinkedIn contracts, select the contract that you would like to connect to the Attract system.</span></span> <span data-ttu-id="b7277-116">Ef þú hefur aðeins sæti á einum LinkedIn samningi, verður þetta skref ekki þörf.</span><span class="sxs-lookup"><span data-stu-id="b7277-116">If you have a seat on only one LinkedIn contract, this step will not be needed.</span></span>

5.  <span data-ttu-id="b7277-117">LinkedIn græjan mun nú hlaða inn í stjórnandastillingar þínar með lista yfir samþættingar sem sýndar eru.</span><span class="sxs-lookup"><span data-stu-id="b7277-117">The LinkedIn widget will now load in your Admin settings with the list of integrations shown.</span></span> <span data-ttu-id="b7277-118">Fyrir neðan **Tengja kerfi ráðningaraðila**, smelltu á **Beiðni**.</span><span class="sxs-lookup"><span data-stu-id="b7277-118">Under **Recruiter System connect**, click **Request**.</span></span>

<span data-ttu-id="b7277-119">[![Yfirlit Attract stjórnanda til að biðja um LinkedIn Recruiter-samþættingu](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span><span class="sxs-lookup"><span data-stu-id="b7277-119">[![Attract Admin view to Request LinkedIn Recruiter integration](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span></span>

6.  <span data-ttu-id="b7277-120">Eftir að samþættingin er beðið frá Attract mun hún sýna sem **Samstarfsaðili tilbúinn** og er hægt að kveikja á með **Stjórnandastillingum ráðningaraðila**.</span><span class="sxs-lookup"><span data-stu-id="b7277-120">After the integration is requested from Attract, it will show as **Partner ready** and is ready to be turned on from **Recruiter Admin settings**.</span></span> <span data-ttu-id="b7277-121">Ef þú sérð **Tilkynna samstarfsaðila** á þessari síðu skaltu bíða í nokkrar sekúndur, smelltu á **Tilkynna samstarfsaðila** og endurnýja síðan síðuna.</span><span class="sxs-lookup"><span data-stu-id="b7277-121">If you see **Notify partner** on this page, wait a few seconds, click **Notify partner**, and then refresh the page.</span></span> <span data-ttu-id="b7277-122">Það ætti nú að sýna sem **Samstarfsaðili tilbúinn**.</span><span class="sxs-lookup"><span data-stu-id="b7277-122">It should now show as **Partner ready**.</span></span>

<span data-ttu-id="b7277-123">[![Yfirlit Attract-sjórnanda til að gefa til kynna beiðnum Attract megin hefur verið lokið](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span><span class="sxs-lookup"><span data-stu-id="b7277-123">[![Attract Admin view to indicate Attract side of requests have been completed](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span></span>

<span data-ttu-id="b7277-124">Til að ljúka næsta skrefi þarftu að hafa stjórnandaréttindi á LinkedIn Recruiter samningnum þínum.</span><span class="sxs-lookup"><span data-stu-id="b7277-124">To complete the next step, you need to have an Admin privilege on your LinkedIn Recruiter Contract.</span></span>

7.  <span data-ttu-id="b7277-125">Skráðu þig inn á LinkedIn með því að nota stjórnandareikninginn og farðu í LinkedIn Recruiter efst til hægri.</span><span class="sxs-lookup"><span data-stu-id="b7277-125">Sign in to LinkedIn using the Admin account and go to LinkedIn Recruiter on the top right.</span></span> 

8. <span data-ttu-id="b7277-126">Í **Fleira** valmyndinni efst á skjánum smellirðu á **stjórnandastillingar**, og smelltu síðan á **ATS** flipann.</span><span class="sxs-lookup"><span data-stu-id="b7277-126">On the **More** menu at the top of the screen, click **Admin Settings**, and then click the **ATS** Tab.</span></span>

<span data-ttu-id="b7277-127">Attract-kerfið verður skráð með nokkrum valkostum sem hægt er að kveikja á.</span><span class="sxs-lookup"><span data-stu-id="b7277-127">The Attract system will be listed with a couple of options that can be turned on.</span></span>

9. <span data-ttu-id="b7277-128">Ef þú vilt aðeins virkja útflutning með einum smell fyrir **IN-ATS-vísirinn** og **In-ATS Profile græjuna** skaltu velja **Aðgangur að fyrirtækinu**.</span><span class="sxs-lookup"><span data-stu-id="b7277-128">If you want to enable only 1-Click export for the **In-ATS indicator** and the **In-ATS Profile Widget**, select **Company-level access**.</span></span> <span data-ttu-id="b7277-129">Ef þú vilt virkja alla aðgangseiginleika að fyrirtækinu auk InMail-ferils, athugasemdaferils og InMail-forstillingaraðgang, veldu **Aðgangur á samningsstigi**.</span><span class="sxs-lookup"><span data-stu-id="b7277-129">If you want to enable all of Company-level access features plus InMail history, Notes history, and the InMail stub profile access, select **Contract-level access**.</span></span>

10. <span data-ttu-id="b7277-130">Kveiktu á viðkomandi aðgangsstigi frá LinkedIn Recruiter **Admin-ATS** stillingunum.</span><span class="sxs-lookup"><span data-stu-id="b7277-130">Turn on the desired access level from your LinkedIn Recruiter **Admin-ATS** settings.</span></span>

<span data-ttu-id="b7277-131">[![Kveikja á Attract-samþættingu úr LinkedIn Recruiter yfirliti stjórnanda](./media/EnableRSC.png)](./media/EnableRSC.png)</span><span class="sxs-lookup"><span data-stu-id="b7277-131">[![Turn on Attract integration from LinkedIn Recruiter Admin view](./media/EnableRSC.png)](./media/EnableRSC.png)</span></span>

12. <span data-ttu-id="b7277-132">Farðu aftur í stjórnandastillingar Attract sem AttractAdmin og veldu **LinkedIn-samþættingu** flipann. Þú ættir nú að sjá LinkedIn græjurálagið sem sýnir **Virkt** með valið aðgangsstig kveikt.</span><span class="sxs-lookup"><span data-stu-id="b7277-132">Go back to Attract Admin Settings as an AttractAdmin and select the **LinkedIn integration** tab. You should now see the LinkedIn widget load showing **Enabled** with the selected access level turned on.</span></span>

<span data-ttu-id="b7277-133">[![LinkedIn Recruiter samþættingu lokið](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span><span class="sxs-lookup"><span data-stu-id="b7277-133">[![LinkedIn Recruiter integration complete](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span></span>

## <a name="using-linkedin-recruiter-capabilities"></a><span data-ttu-id="b7277-134">Notkun á LinkedIn Recruiter möguleikum</span><span class="sxs-lookup"><span data-stu-id="b7277-134">Using LinkedIn Recruiter capabilities</span></span>

<span data-ttu-id="b7277-135">Eftir að LinkedIn Recruiter möguleikar hafa verið virkjaðir af Attract-stjórnanda hafa ráðningarstjórar og ráðningaraðilar aðgang að þeim.</span><span class="sxs-lookup"><span data-stu-id="b7277-135">After LinkedIn Recruiter capabilities has been enabled by the Attract Admin it is available for hiring managers and recruiters to access.</span></span> <span data-ttu-id="b7277-136">Til að nota þessa eiginleika skaltu tengja LinkedIn reikninginn þinn fyrir neðan **Notandastillingar**.</span><span class="sxs-lookup"><span data-stu-id="b7277-136">To use these capabilities, connect your LinkedIn account under **User Settings**.</span></span> <span data-ttu-id="b7277-137">Nokkrir eiginleikar verða tiltækir eftir að bæði stjórnanda- og notendastillingar hafa verið tengdir.</span><span class="sxs-lookup"><span data-stu-id="b7277-137">Several capabilities will be available after both the Admin and User settings have been connected.</span></span>

### <a name="in-ats-profile-widget"></a><span data-ttu-id="b7277-138">In-ATS forstillingargræjan</span><span class="sxs-lookup"><span data-stu-id="b7277-138">In-ATS profile widget</span></span>

<span data-ttu-id="b7277-139">Þú getur skoðað LinkedIn forstillingar umsækjanda í Attract.</span><span class="sxs-lookup"><span data-stu-id="b7277-139">You can view the candidate’s LinkedIn profile in Attract.</span></span> <span data-ttu-id="b7277-140">LinkedIn-græjan mun sýna forstillingar umsækjanda þegar ATS upplýsingar passa við LinkedIn upplýsingar notenda.</span><span class="sxs-lookup"><span data-stu-id="b7277-140">The LinkedIn widget will display the candidate profile when the ATS information matches the LinkedIn information of its users.</span></span>

<span data-ttu-id="b7277-141">Til að skoða forstillingu skaltu fara á forstillingar umsækjanda annaðhvort af starfi eða starfatorgi.</span><span class="sxs-lookup"><span data-stu-id="b7277-141">To view a profile, go the candidate profile either from a job or talent pool.</span></span> <span data-ttu-id="b7277-142">Í forstillingum umsækjanda skaltu velja **LinkedIn** flipann og forstillingargræjan verður hlaðið.</span><span class="sxs-lookup"><span data-stu-id="b7277-142">In the candidate profile, select the **LinkedIn** tab and the profile widget will load.</span></span> <span data-ttu-id="b7277-143">Þú getur einnig vistað umsækjandann í LinkedIn Recruiter verkefnum þínum frá þessari síðu.</span><span class="sxs-lookup"><span data-stu-id="b7277-143">You can also save the candidate to your LinkedIn Recruiter projects from this page.</span></span>
1. <span data-ttu-id="b7277-144">Ef LinkedIn fann samsvörun sem byggist á netfangi eða LinkedIn-meðlimakenni (nákvæmri samsvörun) verða forstillingar umsækjanda sýndar.</span><span class="sxs-lookup"><span data-stu-id="b7277-144">If LinkedIn found the match based on email and LinkedIn member ID (exact match), the candidate's profile will be shown.</span></span> <span data-ttu-id="b7277-145">Notandi hefur enn möguleika á því að tengja/aftengja forstillingarnar.</span><span class="sxs-lookup"><span data-stu-id="b7277-145">The user still has an option to link/unlink the profile.</span></span>

2. <span data-ttu-id="b7277-146">Ef LinkedIn finnur ekki umsækjandann út frá netfangi eða meðlimakenni birtist listi yfir umsækjendur sem hugsanlega passa við nafn umsækjanda og notandinn getur valið einn af þeim og tengt forstillingarnar.</span><span class="sxs-lookup"><span data-stu-id="b7277-146">If LinkedIn cannot find the candidate based on their email or member ID, it will show a list of possible candidate matches based on candidate name and the user can choose one of them and link the profile.</span></span>  

3. <span data-ttu-id="b7277-147">Ef engin umsækjandi finnst út frá nafninu skilar LinkedIn því að leitin hafi ekki skilað neinum niðurstöðum.</span><span class="sxs-lookup"><span data-stu-id="b7277-147">If LinkedIn cannot find any candidate based on the name, it will return that no match was found.</span></span>

### <a name="1-click-export"></a><span data-ttu-id="b7277-148">Útflutningur með einum smell</span><span class="sxs-lookup"><span data-stu-id="b7277-148">1-click export</span></span> 

<span data-ttu-id="b7277-149">Á meðan leitað er að umsækjendum á LinkedIn getur þú flutt út með einum smelli umsækjandann í þau störf sem þú hefur nú þegar opnað.</span><span class="sxs-lookup"><span data-stu-id="b7277-149">While sourcing candidates in LinkedIn, you can 1-click export the candidate to the jobs that you currently have open.</span></span> <span data-ttu-id="b7277-150">Ljúktu eftirfarandi skrefum fyrir útflutning með einum smelli.</span><span class="sxs-lookup"><span data-stu-id="b7277-150">Complete the following steps for a 1-click export.</span></span> <span data-ttu-id="b7277-151">Áður en þú lýkur þessum skrefum skaltu ganga úr skugga um að þú sért úthlutað hlutverki mannauðsstjóra eða ráðningaraðila fyrir starfið og að starfið sé á **Viðfangs** stiginu.</span><span class="sxs-lookup"><span data-stu-id="b7277-151">Before you complete these steps, verify that you are a assigned the role of Hiring manager or Recruiter for the job and that the job has a **Prospect** stage.</span></span>

1.  <span data-ttu-id="b7277-152">Búðu til starfið, úthlutaðu viðeigandi hlutverkum og virkjaðu starfið.</span><span class="sxs-lookup"><span data-stu-id="b7277-152">Create the job, assign the appropriate roles, and activate the job.</span></span>

2.  <span data-ttu-id="b7277-153">Þegar verkið er virkjað skaltu fara í LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="b7277-153">When the job is activated, navigate to LinkedIn Recruiter.</span></span>

3.  <span data-ttu-id="b7277-154">Finndu umsækjandann sem þú ert að leita að og opnaðu forstillingar hans.</span><span class="sxs-lookup"><span data-stu-id="b7277-154">Find the candidate that you are looking for and go to their profile.</span></span>

4.  <span data-ttu-id="b7277-155">Notaðu leitarreitinn á tengiliðaspjaldinu, finndu starfið með starfstitlinum eða starfskenninu sem var virkjað í Attract.</span><span class="sxs-lookup"><span data-stu-id="b7277-155">Using the job search box in the contact card, find the job using the title or the Job ID that was activated in Attract.</span></span> <span data-ttu-id="b7277-156">Ef þú finnur ekki starfið skaltu smella á **Breyta ATS** til að finna rétta tilvikið í Attract.</span><span class="sxs-lookup"><span data-stu-id="b7277-156">If you don’t find the job, click **Change ATS** to find the correct Attract instance.</span></span>

5. <span data-ttu-id="b7277-157">Eftir að starfið er valið skaltu smella á **Flytja út**.</span><span class="sxs-lookup"><span data-stu-id="b7277-157">After the job is selected, click **Export**.</span></span> <span data-ttu-id="b7277-158">Umsækjandinn er nú sóttur af Attract.</span><span class="sxs-lookup"><span data-stu-id="b7277-158">The candidate is now fetched by Attract.</span></span>

6.  <span data-ttu-id="b7277-159">Farðu í Attract og opnaðu viðkomandi starf.</span><span class="sxs-lookup"><span data-stu-id="b7277-159">Go to Attract and open the respective job.</span></span> <span data-ttu-id="b7277-160">Þú finnur umsækjandann sem þú hefur flutt út á **Viðfanga** stigi starfsins.</span><span class="sxs-lookup"><span data-stu-id="b7277-160">You will find the candidate that you just exported in the **Prospect** stage of the job.</span></span>

### <a name="in-ats-indicator"></a><span data-ttu-id="b7277-161">In-ATS vísir</span><span class="sxs-lookup"><span data-stu-id="b7277-161">In-ATS indicator</span></span> 

<span data-ttu-id="b7277-162">Með því að nota LinkedIn recruiter getur þú fylgst með því hvort umsækjandi hafi sótt um önnur störf í fyrirtækinu þínu, skoðað hvar hann er á mismunandi stigum starfsumsókna og skoðað endurgjöf og athugasemdir úr Attract í LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="b7277-162">Using LinkedIn recruiter, you can track whether a candidate has applied to other jobs in your organization, look at where they are in different stages of job applications, and view the feedback and comments from Attract in LinkedIn Recruiter.</span></span>

1.  <span data-ttu-id="b7277-163">Opnaðu LinkedIn Recruiter og finndu forstillingar umsækjandans sem þú leitar að.</span><span class="sxs-lookup"><span data-stu-id="b7277-163">Open LinkedIn Recruiter and locate the candidate profile that you are looking for.</span></span>

2.  <span data-ttu-id="b7277-164">Flettu niður til að skoða **In-ATS** kafla á forstillingum umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="b7277-164">Scroll down to view the **In-ATS** section on the candidate’s profile.</span></span>

3.  <span data-ttu-id="b7277-165">Þú getur notað þessa græju til að skoða allar upplýsingar um umsækjandann sem er til staðar í Attract í yfirliti LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="b7277-165">You can use this widget to view all of the information about the candidate that’s present in Attract from within the LinkedIn Recruiter view.</span></span>

4.  <span data-ttu-id="b7277-166">Veldu **Störf og stöður** flipann til að sjá störf sem þeir eru hluti af, nýjasta stöðu og hvernig þau hafa verið að hreyfa sig að hverju starfi.</span><span class="sxs-lookup"><span data-stu-id="b7277-166">Select the **Jobs & Statuses** tab to see jobs they are part of, the latest status, and how they have been moving against each job.</span></span>

5.  <span data-ttu-id="b7277-167">Veldu flipann **endurgjöf viðtals** til að sjá endurgjöf sem spyrlar hafa lagt fram í Attract.</span><span class="sxs-lookup"><span data-stu-id="b7277-167">Select the **Interview Feedback** tab to see feedback that the interviewers have submitted in Attract.</span></span>

6.  <span data-ttu-id="b7277-168">Veldu **Athugasemdir** flipann til að sjá athugasemdir sem hafa verið teknar fyrir þennan umsækjanda í Attract.</span><span class="sxs-lookup"><span data-stu-id="b7277-168">Select the **Notes** tab to see notes that have been captured for this applicant in Attract.</span></span>

> [!NOTE]
> <span data-ttu-id="b7277-169">Umsækjandi og umsóknargögn verða samstillt við LinkedIn Recruiter ef umsækjandi komst ekki yfir viðfangsstigið.</span><span class="sxs-lookup"><span data-stu-id="b7277-169">Candidate and application data will not be synced to LinkedIn Recruiter if the candidate hasn't moved past the prospect stage.</span></span>

### <a name="inmail-history"></a><span data-ttu-id="b7277-170">InMail saga</span><span class="sxs-lookup"><span data-stu-id="b7277-170">InMail history</span></span>

<span data-ttu-id="b7277-171">LinkedIn InMail-ferillinn er fáanlegur með aðgangi að samningi við LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="b7277-171">The LinkedIn InMail history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="b7277-172">Þegar það er virkt er hægt að skoða allan InMail-ferilinn þinn með umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="b7277-172">When it is enabled, you can view your entire InMail history with the candidate.</span></span> <span data-ttu-id="b7277-173">Þú getur líka séð hverjir aðrir í fyrirtækinu hafa skipst á InMail með umsækjanda, en þú getur ekki skoðað skilaboðin á milli þeirra.</span><span class="sxs-lookup"><span data-stu-id="b7277-173">You can also see who else from your organization has exchanged InMail with the candidate, however you can't view the messages between them.</span></span>

<span data-ttu-id="b7277-174">Til að skoða InMail ferilinn skaltu fara í forstillingar umsækjanda, fara á **LinkedIn** flipann og fletta að neðst á síðunni til að skoða ferilinn.</span><span class="sxs-lookup"><span data-stu-id="b7277-174">To view InMail history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="b7277-175">Hægt er að skoða InMail feril ef þú hefur átt í umræðum við umsækjandann.</span><span class="sxs-lookup"><span data-stu-id="b7277-175">You can view InMail history if you have had a discussion with the candidate.</span></span> <span data-ttu-id="b7277-176">Skilaboðin frá InMail verða samstillt við Attract á nokkurra klukkutíma fresti.</span><span class="sxs-lookup"><span data-stu-id="b7277-176">The messages from InMail will sync with Attract every couple of hours.</span></span>

### <a name="notes-history"></a><span data-ttu-id="b7277-177">Athugasemdaferill</span><span class="sxs-lookup"><span data-stu-id="b7277-177">Notes history</span></span> 

<span data-ttu-id="b7277-178">LinkedIn athugasemdaferill er fáanlegur með aðgangi að samningi við LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="b7277-178">The LinkedIn notes history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="b7277-179">Þegar það er virkt er hægt að skoða athugasemdir sem hafa verið teknar um umsækjanda með mismunandi ráðningaraðilum frá fyrirtækinu þínu.</span><span class="sxs-lookup"><span data-stu-id="b7277-179">When it is enabled, you can view the notes that have been captured about the candidate by different recruiters from your organization.</span></span>

<span data-ttu-id="b7277-180">Til að skoða athugasemdaferilinn skaltu fara í forstillingar umsækjanda, fara á **LinkedIn** flipann og fletta að neðst á síðunni til að skoða ferilinn.</span><span class="sxs-lookup"><span data-stu-id="b7277-180">To view Notes history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="b7277-181">Þú getur skoðað allar athugasemdir um umsækjanda frá LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="b7277-181">You can view all the notes about the candidate from LinkedIn Recruiter.</span></span>

### <a name="inmail-stub-profile"></a><span data-ttu-id="b7277-182">InMail stutt forstilling</span><span class="sxs-lookup"><span data-stu-id="b7277-182">InMail stub profile</span></span>

<span data-ttu-id="b7277-183">InMail Stutt forstilling er fáanleg með aðgangi að samningi við LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="b7277-183">The InMail stub profile is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="b7277-184">Ef umsækjendur samþykkja að deila LinkedIn forstillingum sínum með einhverjum notanda í fyrirtækinu þínu, getur þú fylgst með umsækjendum í Attract og ný umsækjendafærsla verður búin til fyrir hvern umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="b7277-184">If candidates agree to share their LinkedIn profiles with any user in your organization, you can track the candidates in Attract and a new candidate record will be created for each candidate.</span></span> <span data-ttu-id="b7277-185">Hægt er að skoða netfang umsækjanda ef hann er þegar til staðar í kerfinu með netfang eða hann hefur kosið að deila netfanginu með ráðningaraðilanum.</span><span class="sxs-lookup"><span data-stu-id="b7277-185">You can view candidate's email address if the candidate already exists in the system with an email address or has chosen to share their address with the recruiter.</span></span>

<span data-ttu-id="b7277-186">Til að skoða lista yfir umsækjendur farðu í **Hæfileikasöfn** til að sjá LinkedIn hæfileikasafn búið til af kerfinu.</span><span class="sxs-lookup"><span data-stu-id="b7277-186">To view the list of candidates, go to **Talent pools** to see a system-created LinkedIn talent pool.</span></span> <span data-ttu-id="b7277-187">Þessi hæfileikasafn inniheldur lista yfir umsækjendur og stutta forstillingu þeirra sem var fengin frá LinkedIn, sem sýnir umsækjanda fornafn og eftirnafn.</span><span class="sxs-lookup"><span data-stu-id="b7277-187">This talent pool contains the list candidates and their stub profiles as received from LinkedIn, showing the candidate's first name and last name.</span></span> <span data-ttu-id="b7277-188">Tölvupóstkenni umsækjandans verður birt ef umsækjandi hafði valið að deila netfanginu sínu.</span><span class="sxs-lookup"><span data-stu-id="b7277-188">The candidate’s email ID will be displayed if the candidate had chosen to share their email address.</span></span>
