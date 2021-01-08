---
title: Undirbúningur fyrir keyrslu á Human Resources
description: Á þessari síðu er að finna leiðbeiningar um hvernig á að undirbúa sig fyrir keyrslu á Dynamics 365 Human Resources.
author: rachel-profitt
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 59d7274c3b40e78209d90960c4514321b736876a
ms.sourcegitcommit: d66fd72342931fad25a696b251c05781280d36c4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/14/2020
ms.locfileid: "4011421"
---
# <a name="prepare-for-human-resources-go-live"></a><span data-ttu-id="2a986-103">Undirbúningur fyrir keyrslu á Human Resources</span><span class="sxs-lookup"><span data-stu-id="2a986-103">Prepare for Human Resources go-live</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a986-104">Í þessu efnisatriði er því lýst hvernig á að undirbúa keyrslu á Dynamics 365 Human Resources-verki með því að nota Microsoft Dynamics Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="2a986-104">This topic describes how to prepare to go live with a Dynamics 365 Human Resources project by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> 

<span data-ttu-id="2a986-105">Þessi mynd sýnir þrepin í keyrsluferlinu.</span><span class="sxs-lookup"><span data-stu-id="2a986-105">This graphic shows the phases of the go-live process.</span></span> 

![Ferli keyrslu](./media/hr-admin-go-live-prepare-process.png)

<span data-ttu-id="2a986-107">Í eftirfarandi töflu er listi yfir öll skrefin í ferlinu, væntanleg tímalengd og hver ber ábyrgð á aðgerðinni.</span><span class="sxs-lookup"><span data-stu-id="2a986-107">The following table lists all the steps in the process, the expected duration, and who is responsible for the action.</span></span>

| <span data-ttu-id="2a986-108">Áfangi</span><span class="sxs-lookup"><span data-stu-id="2a986-108">Phase</span></span> | <span data-ttu-id="2a986-109">Aðgerð</span><span class="sxs-lookup"><span data-stu-id="2a986-109">Action</span></span> | <span data-ttu-id="2a986-110">Tímalengd/hvenær</span><span class="sxs-lookup"><span data-stu-id="2a986-110">Duration/When</span></span> | <span data-ttu-id="2a986-111">Hver</span><span class="sxs-lookup"><span data-stu-id="2a986-111">Who</span></span> | <span data-ttu-id="2a986-112">Athugasemdir</span><span class="sxs-lookup"><span data-stu-id="2a986-112">Notes</span></span> |
| --- | --- | --- | --- |--- |
| <span data-ttu-id="2a986-113">1</span><span class="sxs-lookup"><span data-stu-id="2a986-113">1</span></span> | <span data-ttu-id="2a986-114">Uppfæra keyrsludagsetningu í LCS</span><span class="sxs-lookup"><span data-stu-id="2a986-114">Update go-live date in LCS</span></span> | <span data-ttu-id="2a986-115">Í síðasta lagi með 2-3 mánaða fyrirvara</span><span class="sxs-lookup"><span data-stu-id="2a986-115">At the latest 2-3 months in advance</span></span> | <span data-ttu-id="2a986-116">Samstarfsaðili/viðskiptavinur</span><span class="sxs-lookup"><span data-stu-id="2a986-116">Partner/Customer</span></span> | <span data-ttu-id="2a986-117">Áfangadagsetningum skal haldið uppfærðum með reglulegu millibili.</span><span class="sxs-lookup"><span data-stu-id="2a986-117">The milestone dates should be kept up to date on an ongoing basis.</span></span> |
| <span data-ttu-id="2a986-118">2</span><span class="sxs-lookup"><span data-stu-id="2a986-118">2</span></span> | <span data-ttu-id="2a986-119">Ljúka við og senda gátlista</span><span class="sxs-lookup"><span data-stu-id="2a986-119">Complete and send checklist</span></span> | <span data-ttu-id="2a986-120">Eftir að samþykkisprófun notanda er lokið</span><span class="sxs-lookup"><span data-stu-id="2a986-120">After user acceptance testing (UAT) is complete</span></span> | <span data-ttu-id="2a986-121">Samstarfsaðili/viðskiptavinur</span><span class="sxs-lookup"><span data-stu-id="2a986-121">Partner/Customer</span></span> | <span data-ttu-id="2a986-122">Fylgja skal leiðbeiningunum í [Keyrslumat FastTrack](hr-admin-go-live-prepare.md#fasttrack-go-live-assessment).</span><span class="sxs-lookup"><span data-stu-id="2a986-122">Follow the instructions provided in [FastTrack go-live assessment](hr-admin-go-live-prepare.md#fasttrack-go-live-assessment).</span></span> |
| <span data-ttu-id="2a986-123">3</span><span class="sxs-lookup"><span data-stu-id="2a986-123">3</span></span> | <span data-ttu-id="2a986-124">Verkmat (FastTrack)</span><span class="sxs-lookup"><span data-stu-id="2a986-124">Project assessment (FastTrack)</span></span> | <span data-ttu-id="2a986-125">Hönnuður FastTrack\*</span><span class="sxs-lookup"><span data-stu-id="2a986-125">FastTrack Architect\*</span></span> | <span data-ttu-id="2a986-126">Hönnuður kemur með mat þegar gátlisti er móttekin og heldur áfram yfirferð þar til spurningum hefur verið svarað og flutningar eru tilbúnir ef það á við.</span><span class="sxs-lookup"><span data-stu-id="2a986-126">Architect delivers assessment after checklist is received and continues review until questions are clarified and mitigations are in place, if applicable.</span></span> |
| <span data-ttu-id="2a986-127">4</span><span class="sxs-lookup"><span data-stu-id="2a986-127">4</span></span> | <span data-ttu-id="2a986-128">Vinnustofa verks (FastTrack)</span><span class="sxs-lookup"><span data-stu-id="2a986-128">Project workshop (FastTrack)</span></span> | <span data-ttu-id="2a986-129">Hönnuður FastTrack\*</span><span class="sxs-lookup"><span data-stu-id="2a986-129">FastTrack Architect\*</span></span> | |
| <span data-ttu-id="2a986-130">5</span><span class="sxs-lookup"><span data-stu-id="2a986-130">5</span></span> | <span data-ttu-id="2a986-131">Innflutningur gagnapakka</span><span class="sxs-lookup"><span data-stu-id="2a986-131">Data package imports</span></span> | <span data-ttu-id="2a986-132">Fer eftir verkinu</span><span class="sxs-lookup"><span data-stu-id="2a986-132">Depends on the project</span></span> | <span data-ttu-id="2a986-133">Samstarfsaðili/viðskiptavinur</span><span class="sxs-lookup"><span data-stu-id="2a986-133">Partner/Customer</span></span> | <span data-ttu-id="2a986-134">Fylgja skal leiðbeiningunum í [Yfirliti gagnastjórnunar](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages).</span><span class="sxs-lookup"><span data-stu-id="2a986-134">Follow the instructions in [Data management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages).</span></span>|
| <span data-ttu-id="2a986-135">6</span><span class="sxs-lookup"><span data-stu-id="2a986-135">6</span></span> | <span data-ttu-id="2a986-136">Vinnsla tilbúin</span><span class="sxs-lookup"><span data-stu-id="2a986-136">Production ready</span></span> | <span data-ttu-id="2a986-137">Þegar öllum fyrri skrefum er lokið</span><span class="sxs-lookup"><span data-stu-id="2a986-137">After all previous steps have been completed</span></span> | <span data-ttu-id="2a986-138">Samstarfsaðili/viðskiptavinur</span><span class="sxs-lookup"><span data-stu-id="2a986-138">Partner/Customer</span></span> | <span data-ttu-id="2a986-139">Samstarfsaðili/viðskiptavinur getur tekið við stjórn vinnsluumhverfisins.</span><span class="sxs-lookup"><span data-stu-id="2a986-139">Partner/Customer can take control of the production environment.</span></span>|
| <span data-ttu-id="2a986-140">7</span><span class="sxs-lookup"><span data-stu-id="2a986-140">7</span></span> | <span data-ttu-id="2a986-141">Flutningsaðgerðir</span><span class="sxs-lookup"><span data-stu-id="2a986-141">Cutover activities</span></span> | <span data-ttu-id="2a986-142">Fer eftir verkinu</span><span class="sxs-lookup"><span data-stu-id="2a986-142">Depends on the project</span></span> | <span data-ttu-id="2a986-143">Samstarfsaðili/viðskiptavinur</span><span class="sxs-lookup"><span data-stu-id="2a986-143">Partner/Customer</span></span> | |
| <span data-ttu-id="2a986-144">8</span><span class="sxs-lookup"><span data-stu-id="2a986-144">8</span></span> | <span data-ttu-id="2a986-145">Ljúka</span><span class="sxs-lookup"><span data-stu-id="2a986-145">Go live</span></span> | <span data-ttu-id="2a986-146">Fer eftir verkinu</span><span class="sxs-lookup"><span data-stu-id="2a986-146">Depends on the project</span></span> | <span data-ttu-id="2a986-147">Viðskiptavinur</span><span class="sxs-lookup"><span data-stu-id="2a986-147">Customer</span></span> | |

> [!IMPORTANT]
> <span data-ttu-id="2a986-148">\*Skrefum 3 og 4 er aðeins lokið fyrir viðskiptavini sem uppfylla skilyrði FastTrack.</span><span class="sxs-lookup"><span data-stu-id="2a986-148">\*Steps 3 and 4 are only completed for customers who qualify for FastTrack.</span></span>

## <a name="completing-the-lcs-methodology"></a><span data-ttu-id="2a986-149">Lokið við LCS-aðferðina</span><span class="sxs-lookup"><span data-stu-id="2a986-149">Completing the LCS methodology</span></span>

<span data-ttu-id="2a986-150">Stór áfangi í hverju innleiðingarverki fyrir sig er flutningur yfir í vinnsluumhverfið.</span><span class="sxs-lookup"><span data-stu-id="2a986-150">A major milestone in each implementation project is the cutover to the production environment.</span></span> 

<span data-ttu-id="2a986-151">Til að tryggja að vinnsluumhverfið sé notað fyrir virkar aðgerðir, úthlutar Microsoft aðeins vinnsluumhverfinu þegar innleiðingin nálgast áfangann **Stjórna** þegar áskildum aðgerðum í LCS-aðferðinni er lokið.</span><span class="sxs-lookup"><span data-stu-id="2a986-151">To help ensure the production environment is used for live operations, Microsoft provisions the production instance only when the implementation is approaching the **Operate** phase, after the required activities in the LCS methodology are completed.</span></span> <span data-ttu-id="2a986-152">Frekari upplýsingar um umhverfin í áskriftinni þinni er að finna í  [Leyfishandbók Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).</span><span class="sxs-lookup"><span data-stu-id="2a986-152">For more information about the environments in your subscription, see the [Dynamics 365 Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=866544).</span></span> 

<span data-ttu-id="2a986-153">Viðskiptavinir verða að ljúka við áfangana **Greining** , **Hanna og þróa** og **Prófa** í LCS-aðferðinni áður en  **Skilgreina** hnappurinn til að biðja um vinnsluumhverfið verður aðgengilegur.</span><span class="sxs-lookup"><span data-stu-id="2a986-153">Customers must complete the **Analysis** , **Design and Develop** , and **Test** phases in the LCS methodology before the **Configure** button for requesting the production environment becomes available.</span></span> <span data-ttu-id="2a986-154">Til að ljúka áfanga í LCS verður fyrst að ljúka öllum nauðsynlegum skrefum í þeim áfanga.</span><span class="sxs-lookup"><span data-stu-id="2a986-154">To complete a phase in LCS, you must first complete every required step in that phase.</span></span> <span data-ttu-id="2a986-155">Þegar öllum skrefum í áfanga er lokið er hægt að ljúka öllum áfanganum.</span><span class="sxs-lookup"><span data-stu-id="2a986-155">When all the steps in a phase are completed, you can complete the whole phase.</span></span> <span data-ttu-id="2a986-156">Alltaf er hægt að opna áfanga aftur síðar ef gera þarf breytingar.</span><span class="sxs-lookup"><span data-stu-id="2a986-156">You can always reopen a phase later if you must make changes.</span></span> <span data-ttu-id="2a986-157">Frekari upplýsingar er að finna í  [Viðskiptavinir Lifecycle Services (LCS) fyrir Finance and Operations forrit](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs).</span><span class="sxs-lookup"><span data-stu-id="2a986-157">For more information, see [Lifecycle Services (LCS) for Finance and Operations apps customers](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs).</span></span> 

<span data-ttu-id="2a986-158">Ferlið við að ljúka við skref er með tvo hluta:</span><span class="sxs-lookup"><span data-stu-id="2a986-158">The process of completing a step has two parts:</span></span> 

- <span data-ttu-id="2a986-159">Gerið raunverulega vinnu, svo sem greining á samsvörun og gloppum eða samþykkisprófun notanda.</span><span class="sxs-lookup"><span data-stu-id="2a986-159">Do the actual work, such as a fit-gap analysis or user acceptance testing (UAT).</span></span> 
- <span data-ttu-id="2a986-160">Merktu samsvarandi skref í LCS-aðferðinni sem lokið.</span><span class="sxs-lookup"><span data-stu-id="2a986-160">Mark the corresponding step in the LCS methodology as completed.</span></span> 

<span data-ttu-id="2a986-161">Gott er að ljúka við skrefin í aðferðinni eftir því sem innleiðingunni vindur fram.</span><span class="sxs-lookup"><span data-stu-id="2a986-161">It's a good practice to complete the steps in the methodology as you make progress with the implementation.</span></span> <span data-ttu-id="2a986-162">Ekki bíða þar til á síðustu stundu.</span><span class="sxs-lookup"><span data-stu-id="2a986-162">Don't wait until the last minute.</span></span> <span data-ttu-id="2a986-163">Ekki bara smella í gegnum öll skrefin til að fá vinnsluumhverfi.</span><span class="sxs-lookup"><span data-stu-id="2a986-163">Don't just click through all the steps so you can get a production environment.</span></span> <span data-ttu-id="2a986-164">Það er í hag viðskiptavinarins að fá áreiðanlega innleiðingu.</span><span class="sxs-lookup"><span data-stu-id="2a986-164">It's in the customer's best interest to have a solid implementation.</span></span> 

## <a name="uat-for-your-solution"></a><span data-ttu-id="2a986-165">Samþykkisprófun notanda (UAT) fyrir lausnina þína</span><span class="sxs-lookup"><span data-stu-id="2a986-165">UAT for your solution</span></span>

<span data-ttu-id="2a986-166">Í UAT-áfanganum þarf að prófa alla viðskiptaferla sem hafa verið innleiddir og allar sérstillingar sem gerðar hafa verið í sandkassaumhverfi í innleiðingarverkinu.</span><span class="sxs-lookup"><span data-stu-id="2a986-166">During the UAT phase, you must test all the business processes you've implemented, and any customizations you've made, in a Sandbox environment in the implementation project.</span></span> <span data-ttu-id="2a986-167">Til að tryggja vel heppnaða keyrslu ætti að íhuga eftirfarandi þegar lögð er lokahönd á UAT-áfangann:</span><span class="sxs-lookup"><span data-stu-id="2a986-167">To help ensure a successful go-live, you should consider the following as you complete the UAT phase:</span></span> 

- <span data-ttu-id="2a986-168">Prófunartilvik ná yfir allar kröfurnar.</span><span class="sxs-lookup"><span data-stu-id="2a986-168">Test cases cover the entire scope of requirements.</span></span> 
- <span data-ttu-id="2a986-169">Prófaðu með því að nota flutt gögn.</span><span class="sxs-lookup"><span data-stu-id="2a986-169">Test by using migrated data.</span></span> <span data-ttu-id="2a986-170">Þessi gögn ættu að innihalda aðalgögn, svo sem starfsmenn, störf og stöður.</span><span class="sxs-lookup"><span data-stu-id="2a986-170">This data should include master data such as workers, jobs, and positions.</span></span> <span data-ttu-id="2a986-171">Taktu einnig með opnunarstöður eins og uppsöfnuð leyfi og fjarvistir.</span><span class="sxs-lookup"><span data-stu-id="2a986-171">Also include opening balances, like leave and absence accruals.</span></span> <span data-ttu-id="2a986-172">Að lokum skal taka með opnar færslur eins og gildandi fríðindaskráningar.</span><span class="sxs-lookup"><span data-stu-id="2a986-172">Finally, include open transactions, such as current benefits enrollments.</span></span> <span data-ttu-id="2a986-173">Ljúkið prófun á öllum gagnagerðum, jafnvel þótt gagnasafninu sé ekki lokið.</span><span class="sxs-lookup"><span data-stu-id="2a986-173">Complete testing with all types of data, even if the data set isn't finalized.</span></span> 
- <span data-ttu-id="2a986-174">Prófið með því að nota rétt öryggishlutverk (sjálfgefin hlutverk og sérstillt hlutverk) sem er úthlutað á notendur.</span><span class="sxs-lookup"><span data-stu-id="2a986-174">Test by using the correct security roles (default roles and custom roles) that are assigned to users.</span></span> 
- <span data-ttu-id="2a986-175">Gakktu úr skugga um að lausnin samræmist öllum kröfum sem tengjast fyrirtæki og atvinnugrein.</span><span class="sxs-lookup"><span data-stu-id="2a986-175">Make sure that the solution complies with any company- and industry-specific regulatory requirements.</span></span> 
- <span data-ttu-id="2a986-176">Skjalfestu alla eiginleika og fáðu samþykki frá viðskiptavininum.</span><span class="sxs-lookup"><span data-stu-id="2a986-176">Document all features and obtain approval and sign-off from the customer.</span></span> 

## <a name="fasttrack-go-live-assessment"></a><span data-ttu-id="2a986-177">Keyrslumat FastTrack</span><span class="sxs-lookup"><span data-stu-id="2a986-177">FastTrack go-live assessment</span></span>

<span data-ttu-id="2a986-178">Viðskiptavinir sem uppfylla skilyrði FastTrack og eru í samvinnu við úrlausnarhönnuð FastTrack munu ljúka yfirferð á keyrslu með Microsoft FastTrack.</span><span class="sxs-lookup"><span data-stu-id="2a986-178">Customers who are qualified for FastTrack and are engaged with a FastTrack Solution Architect will complete a go-live review with Microsoft FastTrack.</span></span> <span data-ttu-id="2a986-179">Frekari upplýsingar er að finna í  [Microsoft FastTrack](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview).</span><span class="sxs-lookup"><span data-stu-id="2a986-179">For more information, see [Microsoft FastTrack](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview).</span></span> 

<span data-ttu-id="2a986-180">Um átta vikum fyrir keyrslu mun FastTrack-teymið biðja þig um að fylla út [Gátlisti fyrir keyrslu](https://go.microsoft.com/fwlink/?linkid=2146013).</span><span class="sxs-lookup"><span data-stu-id="2a986-180">About eight weeks before go-live, the FastTrack team will ask you to fill in a [Go-live checklist](https://go.microsoft.com/fwlink/?linkid=2146013).</span></span>

<span data-ttu-id="2a986-181">Verkefnisstjórinn eða helsti aðilinn að verkinu verður að ljúka við gátlisti fyrir keyrslu í áfanga forkeyrslu fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="2a986-181">The project manager or a key project member must complete the go-live checklist during the pre-go-live phase of the project.</span></span> <span data-ttu-id="2a986-182">Yfirleitt er gátlistanum lokið fjórum til sex vikum á undan uppgefinni keyrsludagsetningu, þegar samþykkisprófun notanda er lokið eða næstum lokið.</span><span class="sxs-lookup"><span data-stu-id="2a986-182">Typically, the checklist is completed four to six weeks before the proposed go-live date, when UAT is completed or almost completed.</span></span> 

<span data-ttu-id="2a986-183">Þegar þú hefur lokið við gátlista fyrir keyrslu skaltu senda hann til úrlausnarhönnuðar FastTrack í tölvupósti.</span><span class="sxs-lookup"><span data-stu-id="2a986-183">When you've completed the go-live checklist, email it to your FastTrack Solution Architect.</span></span> <span data-ttu-id="2a986-184">Láttu alltaf helsta hagsmunaaðila viðskiptavinarins og samstarfsaðila innleiðingarinnar fylgja með í tölvupóstinum.</span><span class="sxs-lookup"><span data-stu-id="2a986-184">Always include a key stakeholder from the customer and the implementation partner on the email.</span></span> 

<span data-ttu-id="2a986-185">Þegar búið er að senda inn gátlistann mun úrslausnarhönnuður FastTrack fara yfir verkið og leggja fram mat sem útlistar mögulegar áhættur, bestu starfsvenjur og ráðleggingar fyrir vel heppnaða keyrslu verksins.</span><span class="sxs-lookup"><span data-stu-id="2a986-185">After you submit the checklist, your FastTrack Solution Architect will review the project and provide an assessment that describes the potential risks, best practices, and recommendations for a successful go-live of the project.</span></span> <span data-ttu-id="2a986-186">Í sumum tilvikum gæti úrlausnarhönnuðurinn lagt áherslu á áhættuþætti og beðið um flutningsáætlun.</span><span class="sxs-lookup"><span data-stu-id="2a986-186">In some cases, the solution architect might highlight risk factors and ask for a mitigation plan.</span></span> 

## <a name="see-also"></a><span data-ttu-id="2a986-187">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="2a986-187">See also</span></span>

[<span data-ttu-id="2a986-188">Algengar spurningar um keyrslu</span><span class="sxs-lookup"><span data-stu-id="2a986-188">Go-live FAQ</span></span>](hr-admin-go-live-faq.md)