---
title: "Fundið með LinkedIn ráðningaraðila"
description: "Þetta efnisatriði veitir upplýsingar um að vélnám til að fá ráðleggingar um störf og umsækjendur."
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: 
ms.author: josaw
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 2fc6bf25d303d7d8de8002a923a080b90dcfbeab
ms.openlocfilehash: 106103e2c3d8f3d89aac5140174e5794da22536f
ms.contentlocale: is-is
ms.lasthandoff: 10/24/2018

---

# <a name="sourcing-with-linkedin-recruiter"></a><span data-ttu-id="94eae-103">Fundið með LinkedIn ráðningaraðila</span><span class="sxs-lookup"><span data-stu-id="94eae-103">Sourcing with LinkedIn Recruiter</span></span>
[!include[banner](../includes/banner.md)]

<span data-ttu-id="94eae-104">LinkedIn er stærsti gagnagrunnur umsækjenda í heimiog oft aðalkerfið sem ráðningaraðilar nota til að finna, hafa samskipti við og finna umsækjendur fyrir þau störf sem ráðningaraðilar vilja ráða í.</span><span class="sxs-lookup"><span data-stu-id="94eae-104">LinkedIn is the world’s largest talent database and often the primary system that recruiters use to find, communicate with, and source candidates for the jobs that recruiters are looking to fill.</span></span> <span data-ttu-id="94eae-105">LinkedIn Recruiter samþætting með Dynamics 365 for Talent: Attract gerir það auðveldara fyrir notendur að ráða og að halda gögnunum í samstillingu milli kerfa tveggja.</span><span class="sxs-lookup"><span data-stu-id="94eae-105">LinkedIn Recruiter integration with Dynamics 365 for Talent: Attract makes it easier for users to hire, and to keep the data in sync between the two systems.</span></span>

> [!NOTE]
> <span data-ttu-id="94eae-106">Þú þarft Viðbót við alhliða ráðningar og LinkedIn Recruiter sæti til að geta notað LinkedIn Recruiter samþættingu með Attract.</span><span class="sxs-lookup"><span data-stu-id="94eae-106">You need the Comprehensive hiring add-on and LinkedIn Recruiter seats to be able to use LinkedIn Recruiter integration with Attract.</span></span>

## <a name="set-up-linkedin-recruiter-with-attract"></a><span data-ttu-id="94eae-107">Setja upp LinkedIn Recruiter með Attract</span><span class="sxs-lookup"><span data-stu-id="94eae-107">Set up LinkedIn Recruiter with Attract</span></span> 

<span data-ttu-id="94eae-108">Áður en þú getur notað LinkedIn Recruiter eiginleika þarftu að stilla samningsstig eða aðgang innan fyrirtækisins fyrir tilvikið í Attract.</span><span class="sxs-lookup"><span data-stu-id="94eae-108">Before you can use the LinkedIn Recruiter capabilities, you must configure contract-level or company-level access with your Attract instance.</span></span> <span data-ttu-id="94eae-109">Til að ljúka skilgreiningarferlinu verður þú að vinna með notandanum sem er stjórnandi á LinkedIn Recruiter samningnum þínum.</span><span class="sxs-lookup"><span data-stu-id="94eae-109">To complete the configuration process, you must work with the user who is an Admin on your LinkedIn Recruiter contract.</span></span> <span data-ttu-id="94eae-110">Ljúktu eftirfarandi skrefum til að skilgreina LinkedIn Recruiter með Attract.</span><span class="sxs-lookup"><span data-stu-id="94eae-110">Complete the following steps to configure LinkedIn Recruiter with Attract.</span></span>

1.  <span data-ttu-id="94eae-111">Skráðu þig inn í Attract sem stjórnanda og farðu í **Stjórnandastillingar**.</span><span class="sxs-lookup"><span data-stu-id="94eae-111">Sign in to Attract as an Admin and go to **Admin Settings**.</span></span>

2.  <span data-ttu-id="94eae-112">Smelltu á **LinkedIn-samþætting** flipann í vinstri glugganum.</span><span class="sxs-lookup"><span data-stu-id="94eae-112">On the left pane, click the **LinkedIn Integration** tab.</span></span>

<span data-ttu-id="94eae-113">[![Yfirlit Attract stjórnanda til að hefja LinkedIn Recruiter-samþættingu](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span><span class="sxs-lookup"><span data-stu-id="94eae-113">[![Attract Admin view to start LinkedIn Recruiter integration](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span></span>

3.  <span data-ttu-id="94eae-114">Smelltu á **Tengja** til að hefja uppsetninguna og fá leiðsögn fyrir LinkedIn innskráningu.</span><span class="sxs-lookup"><span data-stu-id="94eae-114">Click **Connect** to start the setup and be guided through the LinkedIn sign-in process.</span></span>

4.  <span data-ttu-id="94eae-115">Ef þú hefur sæti á mörgum LinkedIn samningum skaltu velja samninginn sem þú vilt tengja við Attract-kerfið.</span><span class="sxs-lookup"><span data-stu-id="94eae-115">If you have seats on multiple LinkedIn contracts, select the contract that you would like to connect to the Attract system.</span></span> <span data-ttu-id="94eae-116">Ef þú hefur aðeins sæti á einum LinkedIn samningi, verður þetta skref ekki þörf.</span><span class="sxs-lookup"><span data-stu-id="94eae-116">If you have a seat on only one LinkedIn contract, this step will not be needed.</span></span>

5.  <span data-ttu-id="94eae-117">LinkedIn græjan mun nú hlaða inn í stjórnandastillingar þínar með lista yfir samþættingar sem sýndar eru.</span><span class="sxs-lookup"><span data-stu-id="94eae-117">The LinkedIn widget will now load in your Admin settings with the list of integrations shown.</span></span> <span data-ttu-id="94eae-118">Fyrir neðan **Tengja kerfi ráðningaraðila**, smelltu á **Beiðni**.</span><span class="sxs-lookup"><span data-stu-id="94eae-118">Under **Recruiter System connect**, click **Request**.</span></span>

<span data-ttu-id="94eae-119">[![Yfirlit Attract stjórnanda til að biðja um LinkedIn Recruiter-samþættingu](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span><span class="sxs-lookup"><span data-stu-id="94eae-119">[![Attract Admin view to Request LinkedIn Recruiter integration](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span></span>

6.  <span data-ttu-id="94eae-120">Eftir að samþættingin er beðið frá Attract mun hún sýna sem **Samstarfsaðili tilbúinn** og er hægt að kveikja á með **Stjórnandastillingum ráðningaraðila**.</span><span class="sxs-lookup"><span data-stu-id="94eae-120">After the integration is requested from Attract, it will show as **Partner ready** and is ready to be turned on from **Recruiter Admin settings**.</span></span> <span data-ttu-id="94eae-121">Ef þú sérð **Tilkynna samstarfsaðila** á þessari síðu skaltu bíða í nokkrar sekúndur, smelltu á **Tilkynna samstarfsaðila** og endurnýja síðan síðuna.</span><span class="sxs-lookup"><span data-stu-id="94eae-121">If you see **Notify partner** on this page, wait a few seconds, click **Notify partner**, and then refresh the page.</span></span> <span data-ttu-id="94eae-122">Það ætti nú að sýna sem **Samstarfsaðili tilbúinn**.</span><span class="sxs-lookup"><span data-stu-id="94eae-122">It should now show as **Partner ready**.</span></span>

<span data-ttu-id="94eae-123">[![Yfirlit Attract-sjórnanda til að gefa til kynna beiðnum Attract megin hefur verið lokið](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span><span class="sxs-lookup"><span data-stu-id="94eae-123">[![Attract Admin view to indicate Attract side of requests have been completed](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span></span>

<span data-ttu-id="94eae-124">Til að ljúka næsta skrefi þarftu að hafa stjórnandaréttindi á LinkedIn Recruiter samningnum þínum.</span><span class="sxs-lookup"><span data-stu-id="94eae-124">To complete the next step, you need to have an Admin privilege on your LinkedIn Recruiter Contract.</span></span>

7.  <span data-ttu-id="94eae-125">Skráðu þig inn á LinkedIn með því að nota stjórnandareikninginn og farðu í LinkedIn Recruiter efst til hægri.</span><span class="sxs-lookup"><span data-stu-id="94eae-125">Sign in to LinkedIn using the Admin account and go to LinkedIn Recruiter on the top right.</span></span> 

8. <span data-ttu-id="94eae-126">Í **Fleira** valmyndinni efst á skjánum smellirðu á **stjórnandastillingar**, og smelltu síðan á **ATS** flipann.</span><span class="sxs-lookup"><span data-stu-id="94eae-126">On the **More** menu at the top of the screen, click **Admin Settings**, and then click the **ATS** Tab.</span></span>

<span data-ttu-id="94eae-127">Attract-kerfið verður skráð með nokkrum valkostum sem hægt er að kveikja á.</span><span class="sxs-lookup"><span data-stu-id="94eae-127">The Attract system will be listed with a couple of options that can be turned on.</span></span>

9. <span data-ttu-id="94eae-128">Ef þú vilt aðeins virkja útflutning með einum smell fyrir **IN-ATS-vísirinn** og **In-ATS Profile græjuna** skaltu velja **Aðgangur að fyrirtækinu**.</span><span class="sxs-lookup"><span data-stu-id="94eae-128">If you want to enable only 1-Click export for the **In-ATS indicator** and the **In-ATS Profile Widget**, select **Company-level access**.</span></span> <span data-ttu-id="94eae-129">Ef þú vilt virkja alla aðgangseiginleika að fyrirtækinu auk InMail-ferils, athugasemdaferils og InMail forstillingaraðgang, veldu **Aðgangur á samningsstigi**.</span><span class="sxs-lookup"><span data-stu-id="94eae-129">If you want to enable all of Company-level access features plus InMail history, Notes history, and the InMail stub profile access, select **Contract-level access**.</span></span>

10. <span data-ttu-id="94eae-130">Kveiktu á viðkomandi aðgangsstigi frá LinkedIn Recruiter **Admin-ATS** stillingunum.</span><span class="sxs-lookup"><span data-stu-id="94eae-130">Turn on the desired access level from your LinkedIn Recruiter **Admin-ATS** settings.</span></span>

<span data-ttu-id="94eae-131">[![Kveikja á Attract-samþættingu frá LinkedIn Recruiter yfirliti stjórnanda](./media/EnableRSC.png)](./media/EnableRSC.png)</span><span class="sxs-lookup"><span data-stu-id="94eae-131">[![Turn on Attract integration from LinkedIn Recruiter Admin view](./media/EnableRSC.png)](./media/EnableRSC.png)</span></span>

12. <span data-ttu-id="94eae-132">Farðu aftur í stjórnandastillingar Attract sem AttractAdmin og veldu **LinkedIn-samþættingu** flipann. Þú ættir nú að sjá LinkedIn græjurálagið sem sýnir **Virkt** með valið aðgangsstig kveikt.</span><span class="sxs-lookup"><span data-stu-id="94eae-132">Go back to Attract Admin Settings as an AttractAdmin and select the **LinkedIn integration** tab. You should now see the LinkedIn widget load showing **Enabled** with the selected access level turned on.</span></span>

<span data-ttu-id="94eae-133">[![LinkedIn Recruiter-samþættingu lokið](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span><span class="sxs-lookup"><span data-stu-id="94eae-133">[![LinkedIn Recruiter integration complete](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span></span>

## <a name="using-linkedin-recruiter-capabilities"></a><span data-ttu-id="94eae-134">Notkun LinkedIn Recruiter eiginleika</span><span class="sxs-lookup"><span data-stu-id="94eae-134">Using LinkedIn Recruiter capabilities</span></span>

<span data-ttu-id="94eae-135">Eftir að LinkedIn Recruiter eiginleiki hefur verið virkjaður af Attract-stjórnanda er hann opinn fyrir aðgang af mannauðsstjórum og umsækjendum.</span><span class="sxs-lookup"><span data-stu-id="94eae-135">After LinkedIn Recruiter capabilities has been enabled by the Attract Admin it is available for hiring managers and recruiters to access.</span></span> <span data-ttu-id="94eae-136">Til að nota þessa eiginleika skaltu tengja LinkedIn reikninginn þinn fyrir neðan **Notandastillingar**.</span><span class="sxs-lookup"><span data-stu-id="94eae-136">To use these capabilities, connect your LinkedIn account under **User Settings**.</span></span> <span data-ttu-id="94eae-137">Nokkrir eiginleikar verða tiltækir eftir að bæði stjórnanda- og notendastillingar hafa verið tengdir.</span><span class="sxs-lookup"><span data-stu-id="94eae-137">Several capabilities will be available after both the Admin and User settings have been connected.</span></span>

### <a name="in-ats-profile-widget"></a><span data-ttu-id="94eae-138">In-ATS forstillingargræjan</span><span class="sxs-lookup"><span data-stu-id="94eae-138">In-ATS profile widget</span></span>

<span data-ttu-id="94eae-139">Þú getur skoðað LinkedIn forstillingar umsækjanda í Attract.</span><span class="sxs-lookup"><span data-stu-id="94eae-139">You can view the candidate’s LinkedIn profile in Attract.</span></span> <span data-ttu-id="94eae-140">LinkedIn-græjan mun sýna forstillingar umsækjanda þegar ATS upplýsingar passa við LinkedIn upplýsingar notenda.</span><span class="sxs-lookup"><span data-stu-id="94eae-140">The LinkedIn widget will display the candidate profile when the ATS information matches the LinkedIn information of its users.</span></span>

<span data-ttu-id="94eae-141">Til að skoða forstillingu skaltu fara á forstillingar umsækjanda annaðhvort af starfi eða starfatorgi.</span><span class="sxs-lookup"><span data-stu-id="94eae-141">To view a profile, go the candidate profile either from a job or talent pool.</span></span> <span data-ttu-id="94eae-142">Í forstillingum umsækjanda skaltu velja **LinkedIn** flipann og forstillingargræjan verður hlaðið.</span><span class="sxs-lookup"><span data-stu-id="94eae-142">In the candidate profile, select the **LinkedIn** tab and the profile widget will load.</span></span> <span data-ttu-id="94eae-143">Notaðu forstillingargræjuna til að tilgreina hvort þetta sé rétt samsvörun.</span><span class="sxs-lookup"><span data-stu-id="94eae-143">Using the profile widget, indicate if this is the correct match.</span></span> <span data-ttu-id="94eae-144">Ef ekki skaltu finna rétta manneskju.</span><span class="sxs-lookup"><span data-stu-id="94eae-144">If it is not, find the correct person.</span></span> <span data-ttu-id="94eae-145">Þú getur einnig vistað umsækjandann í LinkedIn Recruiter verkefnum þínum frá þessari síðu.</span><span class="sxs-lookup"><span data-stu-id="94eae-145">You can also save the candidate to your LinkedIn Recruiter projects from this page.</span></span>

### <a name="1-click-export"></a><span data-ttu-id="94eae-146">Útflutningur með einum smell</span><span class="sxs-lookup"><span data-stu-id="94eae-146">1-click export</span></span> 

<span data-ttu-id="94eae-147">Á meðan leitað er að umsækjendum á LinkedIn getur þú flutt út með einum smelli umsækjandann í þau störf sem þú hefur nú þegar opnað.</span><span class="sxs-lookup"><span data-stu-id="94eae-147">While sourcing candidates in LinkedIn, you can 1-click export the candidate to the jobs that you currently have open.</span></span> <span data-ttu-id="94eae-148">Ljúktu eftirfarandi skrefum fyrir útflutning með einum smelli.</span><span class="sxs-lookup"><span data-stu-id="94eae-148">Complete the following steps for a 1-click export.</span></span> <span data-ttu-id="94eae-149">Áður en þú lýkur þessum skrefum skaltu ganga úr skugga um að þú sért úthlutað hlutverki mannauðsstjóra eða ráðningaraðila fyrir starfið og að starfið sé á **Viðfangs** stiginu.</span><span class="sxs-lookup"><span data-stu-id="94eae-149">Before you complete these steps, verify that you are a assigned the role of Hiring manager or Recruiter for the job and that the job has a **Prospect** stage.</span></span>

1.  <span data-ttu-id="94eae-150">Búðu til starfið, úthlutaðu viðeigandi hlutverkum og virkjaðu starfið.</span><span class="sxs-lookup"><span data-stu-id="94eae-150">Create the job, assign the appropriate roles, and activate the job.</span></span>

2.  <span data-ttu-id="94eae-151">Þegar verkið er virkjað skaltu fara í LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="94eae-151">When the job is activated, navigate to LinkedIn Recruiter.</span></span>

3.  <span data-ttu-id="94eae-152">Finndu umsækjandann sem þú ert að leita að og opnaðu forstillingar hans.</span><span class="sxs-lookup"><span data-stu-id="94eae-152">Find the candidate that you are looking for and go to their profile.</span></span>

4.  <span data-ttu-id="94eae-153">Notaðu leitarreitinn á tengiliðaspjaldinu, finndu starfið með starfstitlinum eða starfskenninu sem var virkjað í Attract.</span><span class="sxs-lookup"><span data-stu-id="94eae-153">Using the job search box in the contact card, find the job using the title or the Job ID that was activated in Attract.</span></span> <span data-ttu-id="94eae-154">Ef þú finnur ekki starfið skaltu smella á **Breyta ATS** til að finna rétta tilvikið í Attract.</span><span class="sxs-lookup"><span data-stu-id="94eae-154">If you don’t find the job, click **Change ATS** to find the correct Attract instance.</span></span>

5. <span data-ttu-id="94eae-155">Eftir að starfið er valið skaltu smella á **Flytja út**.</span><span class="sxs-lookup"><span data-stu-id="94eae-155">After the job is selected, click **Export**.</span></span> <span data-ttu-id="94eae-156">Umsækjandinn er nú sóttur af Attract.</span><span class="sxs-lookup"><span data-stu-id="94eae-156">The candidate is now fetched by Attract.</span></span>

6.  <span data-ttu-id="94eae-157">Farðu í Attract og opnaðu viðkomandi starf.</span><span class="sxs-lookup"><span data-stu-id="94eae-157">Go to Attract and open the respective job.</span></span> <span data-ttu-id="94eae-158">Þú finnur umsækjandann sem þú hefur flutt út á **Viðfanga** stigi starfsins.</span><span class="sxs-lookup"><span data-stu-id="94eae-158">You will find the candidate that you just exported in the **Prospect** stage of the job.</span></span>

### <a name="in-ats-indicator"></a><span data-ttu-id="94eae-159">In-ATS vísir</span><span class="sxs-lookup"><span data-stu-id="94eae-159">In-ATS indicator</span></span> 

<span data-ttu-id="94eae-160">Með því að nota LinkedIn recruiter getur þú fylgst með því hvort umsækjandi hafi sótt um önnur störf í fyrirtækinu þínu, skoðað hvar hann er á mismunandi stigum starfsumsókna og skoðað endurgjöf og athugasemdir frá Attract í LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="94eae-160">Using LinkedIn recruiter, you can track whether a candidate has applied to other jobs in your organization, look at where they are in different stages of job applications, and view the feedback and comments from Attract in LinkedIn Recruiter.</span></span>

1.  <span data-ttu-id="94eae-161">Opnaðu LinkedIn Recruiter og finndu forstillingar umsækjandans sem þú leitar að.</span><span class="sxs-lookup"><span data-stu-id="94eae-161">Open LinkedIn Recruiter and locate the candidate profile that you are looking for.</span></span>

2.  <span data-ttu-id="94eae-162">Flettu niður til að skoða **In-ATS** kafla á forstillingum umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="94eae-162">Scroll down to view the **In-ATS** section on the candidate’s profile.</span></span>

3.  <span data-ttu-id="94eae-163">Þú getur notað þessa græju til að skoða allar upplýsingar um umsækjandann sem er til staðar í Attract í yfirliti LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="94eae-163">You can use this widget to view all of the information about the candidate that’s present in Attract from within the LinkedIn Recruiter view.</span></span>

4.  <span data-ttu-id="94eae-164">Veldu **Störf og stöður** flipann til að sjá störf sem þeir eru hluti af, nýjasta stöðu og hvernig þau hafa verið að hreyfa sig að hverju starfi.</span><span class="sxs-lookup"><span data-stu-id="94eae-164">Select the **Jobs & Statuses** tab to see jobs they are part of, the latest status, and how they have been moving against each job.</span></span>

5.  <span data-ttu-id="94eae-165">Veldu flipann **endurgjöf viðtals** til að sjá endurgjöf sem spyrlar hafa lagt fram í Attract.</span><span class="sxs-lookup"><span data-stu-id="94eae-165">Select the **Interview Feedback** tab to see feedback that the interviewers have submitted in Attract.</span></span>

6.  <span data-ttu-id="94eae-166">Veldu **Athugasemdir** flipann til að sjá athugasemdir sem hafa verið teknar fyrir þennan umsækjanda í Attract.</span><span class="sxs-lookup"><span data-stu-id="94eae-166">Select the **Notes** tab to see notes that have been captured for this applicant in Attract.</span></span>

### <a name="inmail-history"></a><span data-ttu-id="94eae-167">InMail ferill</span><span class="sxs-lookup"><span data-stu-id="94eae-167">InMail history</span></span>

<span data-ttu-id="94eae-168">LinkedIn InMail-ferillinn er fáanlegur með aðgangi að samningi við LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="94eae-168">The LinkedIn InMail history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="94eae-169">Þegar það er virkt er hægt að skoða allan InMail-ferilinn þinn með umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="94eae-169">When it is enabled, you can view your entire InMail history with the candidate.</span></span> <span data-ttu-id="94eae-170">Þú getur líka séð hverjir aðrir í fyrirtækinu hafa skipst á InMail með umsækjanda, en þú getur ekki skoðað skilaboðin á milli þeirra.</span><span class="sxs-lookup"><span data-stu-id="94eae-170">You can also see who else from your organization has exchanged InMail with the candidate, however you can't view the messages between them.</span></span>

<span data-ttu-id="94eae-171">Til að skoða InMail-ferilinn skaltu fara í forstillingar umsækjanda, fara á **LinkedIn** flipann og flettu neðst á síðunni til að skoða ferilinn.</span><span class="sxs-lookup"><span data-stu-id="94eae-171">To view InMail history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="94eae-172">Þú getur aðeins skoðað InMail-ferilinn ef umsækjandi hefur svarað beiðni þinni og valið að deila forstillingum sínum með þér í LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="94eae-172">You can view the InMail history only if the candidate has responded to your request and chosen to share their profile with you in LinkedIn.</span></span> <span data-ttu-id="94eae-173">Skilaboðin frá InMail eru samstillt við Attract á nokkra klukkutíma fresti.</span><span class="sxs-lookup"><span data-stu-id="94eae-173">The messages from InMail sync with Attract every couple of hours.</span></span>

### <a name="notes-history"></a><span data-ttu-id="94eae-174">Athugasemdaferill</span><span class="sxs-lookup"><span data-stu-id="94eae-174">Notes history</span></span> 

<span data-ttu-id="94eae-175">LinkedIn athugasemdaferill er fáanlegur með aðgangi að samningi við LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="94eae-175">The LinkedIn notes history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="94eae-176">Þegar það er virkt er hægt að skoða athugasemdir sem hafa verið teknar um umsækjanda með mismunandi ráðningaraðilum frá fyrirtækinu þínu.</span><span class="sxs-lookup"><span data-stu-id="94eae-176">When it is enabled, you can view the notes that have been captured about the candidate by different recruiters from your organization.</span></span>

<span data-ttu-id="94eae-177">Til að skoða athugasemdaferilinn skaltu fara í forstillingar umsækjanda, fara á **LinkedIn** flipann og fletta að neðst á síðunni til að skoða ferilinn.</span><span class="sxs-lookup"><span data-stu-id="94eae-177">To view Notes history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="94eae-178">Þú getur skoðað allar athugasemdir um umsækjanda frá LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="94eae-178">You can view all the notes about the candidate from LinkedIn Recruiter.</span></span>

### <a name="inmail-stub-profile"></a><span data-ttu-id="94eae-179">Inmail stutt forstilling</span><span class="sxs-lookup"><span data-stu-id="94eae-179">InMail stub profile</span></span>

<span data-ttu-id="94eae-180">InMail stutt forstilling er fáanlegur með aðgangi að samningi við LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="94eae-180">The InMail stub profile is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="94eae-181">Ef umsækjendur samþykkja að deila LinkedIn forstillingum sínum með einhverjum notanda í fyrirtækinu þínu, getur þú fylgst með umsækjendum í Attract og ný umsækjendafærsla verður búin til fyrir hvern umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="94eae-181">If candidates agree to share their LinkedIn profiles with any user in your organization, you can track the candidates in Attract and a new candidate record will be created for each candidate.</span></span>

<span data-ttu-id="94eae-182">Til að skoða lista yfir umsækjendur farðu í **Hæfileikasöfn** til að sjá LinkedIn hæfileikasafn búið til af kerfinu.</span><span class="sxs-lookup"><span data-stu-id="94eae-182">To view the list of candidates, go to **Talent pools** to see a system-created LinkedIn talent pool.</span></span> <span data-ttu-id="94eae-183">Þessi hæfileikasafn inniheldur lista yfir umsækjendur og stutta forstillingu þeirra sem var fengin frá LinkedIn, sem sýnir umsækjanda fornafn og eftirnafn.</span><span class="sxs-lookup"><span data-stu-id="94eae-183">This talent pool contains the list candidates and their stub profiles as received from LinkedIn, showing the candidate's first name and last name.</span></span> <span data-ttu-id="94eae-184">Tölvupóstkenni umsækjandans verður birt ef umsækjandi hafði valið að deila netfanginu sínu.</span><span class="sxs-lookup"><span data-stu-id="94eae-184">The candidate’s email ID will be displayed if the candidate had chosen to share their email address.</span></span>

