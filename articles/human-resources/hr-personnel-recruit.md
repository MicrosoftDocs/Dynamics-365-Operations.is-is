---
title: Ráða umsækjendur
description: Þetta efnisatriði sýnir hvernig á að ráða umsækjendur í Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/03/2020
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
ms.author: anbichse
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9a35abcb8a2f6aa8031c8d84a44c2a8ad93883ac
ms.sourcegitcommit: 0354ca7e566fbd2eb0aabdd40000d4ac5c44ea78
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/04/2020
ms.locfileid: "4669173"
---
# <a name="recruit-job-candidates"></a><span data-ttu-id="c8837-103">Ráða umsækjendur</span><span class="sxs-lookup"><span data-stu-id="c8837-103">Recruit job candidates</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="c8837-104">Dynamics 365 Human Resources aðstoðar þig við að stjórna ráðningarbeiðnum.</span><span class="sxs-lookup"><span data-stu-id="c8837-104">Dynamics 365 Human Resources helps you to manage recruiting requests.</span></span> <span data-ttu-id="c8837-105">Aðstoðar þig einnig við að breyta umsækjendum í starfsmenn á einfaldan hátt.</span><span class="sxs-lookup"><span data-stu-id="c8837-105">It also helps you seamlessly transition job candidates to employees.</span></span> <span data-ttu-id="c8837-106">Þegar fyrirtækið þitt notar annað ráðningarforrit kann ráðningarferlið að fela í sér eftirfarandi skref:</span><span class="sxs-lookup"><span data-stu-id="c8837-106">If your organization uses a separate recruiting application, your recruiting process might include the following steps:</span></span>

- <span data-ttu-id="c8837-107">Sláðu inn ráðningarbeiðnina þína í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c8837-107">Enter your recruiting request in Human Resources.</span></span>
- <span data-ttu-id="c8837-108">Taktu á móti tilvísunum frá ráðningarforritinu í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c8837-108">Receive candidate referrals in Human Resources from the recruiting application.</span></span>
- <span data-ttu-id="c8837-109">Ljúktu samþykktarferli umsækjanda í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c8837-109">Complete the candidate approval process in Human Resources.</span></span>

<span data-ttu-id="c8837-110">Þegar þú notar ekki annað ráðningarforrit getur þú einnig haft umsjón með umsækjendum handvirkt í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c8837-110">If you aren't using a separate recruiting application, you can also manually manage candidates in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="c8837-111">Þegar þú ert stjórnandi eða þróunaraðili og vilt samþætta Human Resources við ráðningarforrit þriðja aðila er frekari upplýsingar að finna í [Grunnstilling Common Data Service Samþætting](hr-admin-integration-common-data-service.md) og [Grunnstilling Common Data Service sýndareininga](hr-admin-integration-common-data-service-virtual-entities.md)</span><span class="sxs-lookup"><span data-stu-id="c8837-111">If you're an admin or developer and want to integrate Human Resources with a third-party recruiting application, see [Configure Common Data Service integration](hr-admin-integration-common-data-service.md) and [Configure Common Data Service virtual entities](hr-admin-integration-common-data-service-virtual-entities.md)</span></span>
>
> <span data-ttu-id="c8837-112">Einnig er hægt að finna samþættingarforrit ráðninga á [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span><span class="sxs-lookup"><span data-stu-id="c8837-112">You can also find recruiting integration apps on [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span></span>
>
> <span data-ttu-id="c8837-113">Til að prófa eiginleikann fyrir samþættingu við LinkedIn Talent Hub skal skoða [Samþætting við LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="c8837-113">To try out our preview feature for integrating with LinkedIn Talent Hub, see [Integrate with LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span></span>

## <a name="enable-recruiting-requests"></a><span data-ttu-id="c8837-114">Virkja ráðningarbeiðnir</span><span class="sxs-lookup"><span data-stu-id="c8837-114">Enable recruiting requests</span></span>

<span data-ttu-id="c8837-115">Ef þú vilt senda ráðningarbeiðnir í Human Resources verður þú fyrst að virkja eiginleikann í **Færibreytur Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="c8837-115">If you want to submit recruiting requests in Human Resources, you must first enable the functionality in **Human resources parameters**.</span></span>

1. <span data-ttu-id="c8837-116">Á vinnusvæðinu **Starfsmannastjórnun** velur þú **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="c8837-116">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="c8837-117">Undir **Skipulag**, veldu **Færirbreytur Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="c8837-117">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="c8837-118">Á flipanum **Almennt**, fyrir neðan **RÁÐNINGAR** verður að stilla **Virkja ráðningarbeiðnir** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="c8837-118">On the **General** tab, under **RECRUITING**, set **Enable recruiting requests** to **Yes**.</span></span>

   ![Virkja ráðningarbeiðnir](./media/hr-recruit-0-enable-requests.png)

## <a name="add-a-recruiting-request-location"></a><span data-ttu-id="c8837-120">Bæta við staðsetningu í ráðningarbeiðni</span><span class="sxs-lookup"><span data-stu-id="c8837-120">Add a recruiting request location</span></span>

<span data-ttu-id="c8837-121">Ef fyrirtækið er með margar staðsetningar er hægt að bæta þeim við til að beiðendur geti valið staðsetningarnar þar sem nýi starfsmaðurinn á að starfa.</span><span class="sxs-lookup"><span data-stu-id="c8837-121">If your organization has multiple locations, you can add them so requestors can select a location where the new recruit will be working.</span></span> <span data-ttu-id="c8837-122">Staðsetningin verður höfð með í starfsauglýsingunni.</span><span class="sxs-lookup"><span data-stu-id="c8837-122">The location will be included in the job posting.</span></span>

1. <span data-ttu-id="c8837-123">Sláðu inn **staðsetning ráðningarbeiðni** í leitarstikuna.</span><span class="sxs-lookup"><span data-stu-id="c8837-123">In the search bar, enter **recruiting request location**.</span></span>

2. <span data-ttu-id="c8837-124">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="c8837-124">Select **New**.</span></span>

3. <span data-ttu-id="c8837-125">Sláðu inn heiti staðsetningarinnar í svæðið **Staðsetning ráðningarbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="c8837-125">In the **Recruiting request location** field, enter the location name.</span></span>

   ![Bæta við staðsetningu í ráðningarbeiðni](./media/hr-recruit-0a-add-location.png)

4. <span data-ttu-id="c8837-127">Sláðu inn lýsingu á staðsetningunni í svæðið **Lýsing**.</span><span class="sxs-lookup"><span data-stu-id="c8837-127">In the **Description**, enter a description for the location.</span></span>

5. <span data-ttu-id="c8837-128">Undir **Staðsetning** skal velja **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="c8837-128">Under **Location**, select **Add**.</span></span> <span data-ttu-id="c8837-129">Sláðu inn heimilisfang staðsetningarinnar ef sprettiglugginn **Nýtt heimilisfang** opnast.</span><span class="sxs-lookup"><span data-stu-id="c8837-129">If the **New address** popout appears, enter the address for the location.</span></span>

   ![Færa inn aðsetur](./media/hr-recruit-0b-address.png)

6. <span data-ttu-id="c8837-131">Færðu inn upplýsingar um tengilið staðsetningarinnar fyrir neðan **Tengiliðaupplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="c8837-131">Under **Contact information**, enter the information for the location's contact.</span></span>

7. <span data-ttu-id="c8837-132">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="c8837-132">Select **Save**.</span></span>

## <a name="add-a-recruiting-request"></a><span data-ttu-id="c8837-133">Bæta við ráðningarbeiðni</span><span class="sxs-lookup"><span data-stu-id="c8837-133">Add a recruiting request</span></span>

<span data-ttu-id="c8837-134">Stjórnendur geta sent inn ráðningarbeiðnir í mannauði.</span><span class="sxs-lookup"><span data-stu-id="c8837-134">Managers can submit recruiting requests in Human Resources.</span></span> <span data-ttu-id="c8837-135">Þegar annað ráðningarforrit er notað verður ráðningarbeiðni send um leið og þessum skrefum er lokið og ráðningarferlið hefst í áðurnefndu forriti.</span><span class="sxs-lookup"><span data-stu-id="c8837-135">If you use a separate recruiting application, completing these steps will send a recruiting request and start the recruiting process in that application.</span></span> <span data-ttu-id="c8837-136">Ljúktu að öðrum kost við þetta ferli til að hefja verkflæði fyrir eigið innra ráðningarferli.</span><span class="sxs-lookup"><span data-stu-id="c8837-136">Otherwise, complete this procedure to begin the workflow for your own internal recruiting process.</span></span>

1. <span data-ttu-id="c8837-137">Veljið **Sjálfsafgreiðsla starfsmanna**.</span><span class="sxs-lookup"><span data-stu-id="c8837-137">Select **Employee self service**.</span></span>

2. <span data-ttu-id="c8837-138">Smelltu á flipann **Teymið mitt**.</span><span class="sxs-lookup"><span data-stu-id="c8837-138">Select the **My team** tab.</span></span>

3. <span data-ttu-id="c8837-139">Veljið **Beiðni um að ráða**.</span><span class="sxs-lookup"><span data-stu-id="c8837-139">Select  **Request to recruit**.</span></span>

   ![Hefja ráðningarbeiðni](./media/hr-recruit-1-request-to-recruit.png)

4. <span data-ttu-id="c8837-141">Fylltu út svæðin **Lýsing**, **Starf** og **Áætlaður upphafsdagur**.</span><span class="sxs-lookup"><span data-stu-id="c8837-141">Complete the **Description**, **Job**, and **Estimated start date** fields.</span></span>

   ![Ljúka ráðningarbeiðninni](./media/hr-recruit-2-request-to-recruit.png)

5. <span data-ttu-id="c8837-143">Veldu **Haltu áfram**.</span><span class="sxs-lookup"><span data-stu-id="c8837-143">Select **Continue**.</span></span> <span data-ttu-id="c8837-144">Ráðningarbeiðnin fyrir stöðuna þína birtist.</span><span class="sxs-lookup"><span data-stu-id="c8837-144">The recruiting request for your position appears.</span></span>

6. <span data-ttu-id="c8837-145">Fyrir neðan flipann **Almennt** skal velja ráðningaraðila á fellilistanum **Ráðningaraðili** og síðan velja staðsetningu á fellilistanum **Staðsetning ráðningarbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="c8837-145">Under **General**, select a recruiter from the **Recruiter** dropdown, and then select a location from the **Recruiting request location** dropdown.</span></span>

7. <span data-ttu-id="c8837-146">Breyttu öllum upplýsingum eins og þörf krefur í svæðinu **Starf** veldu síðan **Búa til upplýsingar úr starfi**.</span><span class="sxs-lookup"><span data-stu-id="c8837-146">Under **Job**, change any information as needed, and then select **Create details from job**.</span></span>

   ![Stofna upplýsingar úr verki](./media/hr-recruit-3-create-details-from-job.png)

   <span data-ttu-id="c8837-148">Eftirstandandi svæði ráðningarbeiðninnar eru fyllt út með sjálfgefnum upplýsingum um starfið sem þú slóst inn.</span><span class="sxs-lookup"><span data-stu-id="c8837-148">The rest of the recruiting request will populate with the default information for the job you entered.</span></span>

8. <span data-ttu-id="c8837-149">Fyrir neðan **Ytri lýsing** skal færa inn ytri starfslýsingu.</span><span class="sxs-lookup"><span data-stu-id="c8837-149">Under **External description**, enter an external-facing job description.</span></span>

9. <span data-ttu-id="c8837-150">Fyrir neðan **Stöður** skal velja **Bæta við** og síðan velja staðsetningu fyrir þessa ráðningarbeiðni.</span><span class="sxs-lookup"><span data-stu-id="c8837-150">Under **Positions**, select **Add**, and then select a position for this recruiting request.</span></span>

   ![Bæta við stöðu](./media/hr-recruit-4-select-position.png)

10. <span data-ttu-id="c8837-152">Fyrir neðan **Hæfni** skal velja **Bæta við** og síðan bæta við hæfni.</span><span class="sxs-lookup"><span data-stu-id="c8837-152">Under **Skills**, select **Add**, and then select a skill.</span></span>

11. <span data-ttu-id="c8837-153">Fyrir neðan **Menntunarkröfur** skal velja **Bæta við** og síðan velja gildi á fellilistunum **Menntun** og **Menntunarstig**.</span><span class="sxs-lookup"><span data-stu-id="c8837-153">Under **Educational requirements**, select **Add**, and then select values from the **Education** and **Level of education** dropdowns.</span></span>

   ![Bæta við menntunarkröfum](./media/hr-recruit-5-select-educational-requirements.png)

12. <span data-ttu-id="c8837-155">Bættu við athugasemdum eftir þörfum fyrir neðan **Athugasemd**.</span><span class="sxs-lookup"><span data-stu-id="c8837-155">Under **Comment**, add comments as necessary.</span></span>

13. <span data-ttu-id="c8837-156">Fyrir neðan **Laun** skal velja stig á fellilistanum **Stig** og síðan stilla **Neðri mörk**, **Stýripunkt** og **Efri mörk** eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="c8837-156">Under **Compensation**, select a level from the **Level** dropdown, and then adjust **Low threshold**, **Control point**, and **High threshold** as necessary.</span></span>

14. <span data-ttu-id="c8837-157">Þegar ráðningarbeiðninni þinni er lokið og þú er til reiðu til að hefja ráðningarferlið skaltu velja **Virkja** á valmyndarstikunni.</span><span class="sxs-lookup"><span data-stu-id="c8837-157">When your recruiting request is complete and you're ready to start the recruiting process, select **Activate** in the menu bar.</span></span>

   ![Virkja ráðningarbeiðni](./media/hr-recruit-6-activate-recruit-request.png)

15. <span data-ttu-id="c8837-159">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="c8837-159">Select **Save**.</span></span>

## <a name="view-and-edit-your-recruiting-requests"></a><span data-ttu-id="c8837-160">Skoða og breyta ráðningarbeiðnum</span><span class="sxs-lookup"><span data-stu-id="c8837-160">View and edit your recruiting requests</span></span>

<span data-ttu-id="c8837-161">Ef þú ert yfirmaður og vilt skoða eigin beiðnir:</span><span class="sxs-lookup"><span data-stu-id="c8837-161">If you're a manager and want to view your own requests:</span></span>

1. <span data-ttu-id="c8837-162">Veljið **Sjálfsafgreiðsla starfsmanna**.</span><span class="sxs-lookup"><span data-stu-id="c8837-162">Select **Employee self service**.</span></span>

2. <span data-ttu-id="c8837-163">Smelltu á flipann **Teymið mitt**.</span><span class="sxs-lookup"><span data-stu-id="c8837-163">Select the **My team** tab.</span></span>

3. <span data-ttu-id="c8837-164">Fyrir neðan **Upplýsingar um teymi** skal velja flipann **Ráðningarbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="c8837-164">Under **My team information**, select the **Recruiting requests** tab.</span></span>

   ![Veldu flipann Ráðningarbeiðnir](./media/hr-recruit-7-recruiting-requests.png)

4. <span data-ttu-id="c8837-166">Veldu ráðningarbeiðni á hnitanetinu til að skoða eða breyta henni.</span><span class="sxs-lookup"><span data-stu-id="c8837-166">To view or edit a recruiting request, select it in the grid.</span></span>

<span data-ttu-id="c8837-167">Ef þú ert HR-Pro og vilt skoða allar ráðningarbeiðnir:</span><span class="sxs-lookup"><span data-stu-id="c8837-167">If you're an HR pro and want to view all recruiting requests:</span></span>

1. <span data-ttu-id="c8837-168">Veldu **Starfsmannastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="c8837-168">Select **Personnel management**.</span></span>

2. <span data-ttu-id="c8837-169">Veljið **Ráðningarbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="c8837-169">Select **Recruiting requests**.</span></span>

   ![Skoða ráðningarbeiðnir í Starfsmannastjórnun](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. <span data-ttu-id="c8837-171">Veldu ráðningarbeiðni á hnitanetinu til að skoða eða breyta henni.</span><span class="sxs-lookup"><span data-stu-id="c8837-171">To view or edit a recruiting request, select it in the grid.</span></span>

## <a name="add-or-edit-a-candidate-profile"></a><span data-ttu-id="c8837-172">Bæta við eða breyta notandaupplýsingum umsækjanda</span><span class="sxs-lookup"><span data-stu-id="c8837-172">Add or edit a candidate profile</span></span>

<span data-ttu-id="c8837-173">Þegar fyrirtækið hefur samþætt við annað forrit til að vinna úr ráðningarbeiðnum eru ráðningarbeiðnir áframsendar í umrætt forrit.</span><span class="sxs-lookup"><span data-stu-id="c8837-173">If your organization has integrated with another application to manage recruiting requests, recruiting requests are forwarded to that application.</span></span> <span data-ttu-id="c8837-174">Ráðningarumsóknin sendir síðan upplýsingar umsækjenda aftur til Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c8837-174">The recruiting application then sends candidate information back to Human Resources.</span></span> <span data-ttu-id="c8837-175">Að öðrum kosti er hægt að fylgja eigin innri ráðningarferlum og slá inn upplýsingar umsækjenda handvirkt.</span><span class="sxs-lookup"><span data-stu-id="c8837-175">Otherwise, you can follow your own internal recruiting processes and enter candidate information manually.</span></span>

1. <span data-ttu-id="c8837-176">Veldu **Starfsmannastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="c8837-176">Select **Personnel management**.</span></span>

2. <span data-ttu-id="c8837-177">Veljið **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="c8837-177">Select **Links**.</span></span>

3. <span data-ttu-id="c8837-178">Undir **Ráðning** skal velja **Umsækjendur**.</span><span class="sxs-lookup"><span data-stu-id="c8837-178">Under **Recruiting**, select **Candidates**.</span></span>

   ![Skoða umsækjendur](./media/hr-recruit-9-candidates.png)

4. <span data-ttu-id="c8837-180">Veldu **Nýr** til að bæta við umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="c8837-180">To add a candidate, select **New**.</span></span> <span data-ttu-id="c8837-181">Þegar breyta á fyrirliggjandi umsækjanda skal velja umsækjanda á listanum og síðan velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="c8837-181">To edit an existing candidate, select the candidate from the list and then select **Edit**.</span></span> <span data-ttu-id="c8837-182">Notandaupplýsingar umsækjanda birtast.</span><span class="sxs-lookup"><span data-stu-id="c8837-182">The candidate profile appears.</span></span>

5. <span data-ttu-id="c8837-183">Fyrir neðan **Samantekt á umsækjendum** skal færa inn eða breyta upplýsingum umsækjanda eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="c8837-183">Under **Candidate summary**, enter or edit the candidate information as necessary.</span></span>

6. <span data-ttu-id="c8837-184">Veljið ráðningarbeiðni sem á að tengja umsækjanda við undir **Ráðningarbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="c8837-184">Under **Recruiting request**, select a recruiting request to link the candidate to.</span></span> <span data-ttu-id="c8837-185">Fylltu síðan út svæðin **Áætluð upphafsdagsetning**, **Ráðningarstjóri**, **Staða** og **Lýsing** eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="c8837-185">Then complete the **Estimated start date**, **Hiring manager**, **Position**, and **Description fields** as appropriate.</span></span>

   ![Tengill í ráðningarbeiðni](./media/hr-recruit-10-link-to-recruiting-request.png)

7. <span data-ttu-id="c8837-187">Fyllið út allar upplýsingar á eftirfarandi svæðum sem á að hafa með í færslu umsækjanda:</span><span class="sxs-lookup"><span data-stu-id="c8837-187">Complete all the information in the following areas that you want to include in the candidate's record:</span></span>
   - <span data-ttu-id="c8837-188">**Athugasemdir**</span><span class="sxs-lookup"><span data-stu-id="c8837-188">**Comments**</span></span>
   - <span data-ttu-id="c8837-189">**Starfsreynsla**</span><span class="sxs-lookup"><span data-stu-id="c8837-189">**Professional experience**</span></span>
   - <span data-ttu-id="c8837-190">**Tengslaupplýsingar**</span><span class="sxs-lookup"><span data-stu-id="c8837-190">**Contact information**</span></span>
   - <span data-ttu-id="c8837-191">**Menntun**</span><span class="sxs-lookup"><span data-stu-id="c8837-191">**Education**</span></span>
   - <span data-ttu-id="c8837-192">**Hæfni**</span><span class="sxs-lookup"><span data-stu-id="c8837-192">**Skills**</span></span>
   - <span data-ttu-id="c8837-193">**Skírteini**</span><span class="sxs-lookup"><span data-stu-id="c8837-193">**Certificates**</span></span>
   - <span data-ttu-id="c8837-194">**Skoðanir**</span><span class="sxs-lookup"><span data-stu-id="c8837-194">**Screenings**</span></span>

8. <span data-ttu-id="c8837-195">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="c8837-195">Select **Save**.</span></span>

## <a name="hire-a-candidate"></a><span data-ttu-id="c8837-196">Ráða umsækjanda</span><span class="sxs-lookup"><span data-stu-id="c8837-196">Hire a candidate</span></span>

<span data-ttu-id="c8837-197">Þegar þú ert til reiðu að ráða umsækjanda skaltu fylgja þessu ferli til að breyta umsækjanda í starfsmann.</span><span class="sxs-lookup"><span data-stu-id="c8837-197">When you're ready to hire a candidate, follow this procedure to transition the candidate to an employee.</span></span>

1. <span data-ttu-id="c8837-198">Veldu **Ráða** á eyðublaði umsækjandans.</span><span class="sxs-lookup"><span data-stu-id="c8837-198">On the candidate form, select **Hire**.</span></span>

   ![Ráða umsækjanda](./media/hr-recruit-11-hire.png)

2. <span data-ttu-id="c8837-200">Fylltu út öll svæði eyðublaðsins **Ráða nýjan starfsmann** fyrir neðan **Frekari upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="c8837-200">On the **Hire new worker** form, under **Details**, complete all the fields.</span></span>

   ![Slá inn nýjar ráðningarupplýsingar](./media/hr-recruit-12-hire-new-worker.png)

3. <span data-ttu-id="c8837-202">Fyrir neðan **Frekari upplýsingar um stöðu** skaltu staðfesta og breyta upplýsingum eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="c8837-202">Under **Position details**, verify and change information as necessary.</span></span>

4. <span data-ttu-id="c8837-203">Í **Gátlisti fyrir nýliða** skal velja viðeigandi gátlista fyrir þennan starfsmann.</span><span class="sxs-lookup"><span data-stu-id="c8837-203">Under **Onboarding checklists**, select the relevant onboarding checklists for this employee.</span></span>

5. <span data-ttu-id="c8837-204">Veljið **Halda áfram** til að stofna starfsmannafærslu.</span><span class="sxs-lookup"><span data-stu-id="c8837-204">Select **Continue** to create the employee record.</span></span>

   >[!NOTE]
   ><span data-ttu-id="c8837-205">Færsla umsækjandans kann að fara í gegnum frekari samþykktarskref áður en henni er breytt í starfsmannsfærslu, allt eftir verkflæði fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="c8837-205">Depending on your organization's workflows, the candidate record may go through additional approval steps before becoming an employee record.</span></span>

## <a name="decide-not-to-hire-a-candidate"></a><span data-ttu-id="c8837-206">Ákveðið að ráða ekki umsækjanda</span><span class="sxs-lookup"><span data-stu-id="c8837-206">Decide not to hire a candidate</span></span>

<span data-ttu-id="c8837-207">Þegar ákveðið er að ráða ekki umsækjanda skaltu fylgja þessu ferli til að fjarlægja viðkomandi úr greiningarferlinu.</span><span class="sxs-lookup"><span data-stu-id="c8837-207">If you decide not to hire a candidate, follow this procedure to remove them from the vetting process.</span></span> 

1. <span data-ttu-id="c8837-208">Veldu **Ekki ráða** á eyðublaði umsækjandans.</span><span class="sxs-lookup"><span data-stu-id="c8837-208">On the candidate form, select **Do not hire**.</span></span>

   ![Ekki ráða umsækjanda](./media/hr-recruit-13-do-not-hire.png)

2. <span data-ttu-id="c8837-210">Veljið **Ástæðukóði** og takið með allar athugasemdir.</span><span class="sxs-lookup"><span data-stu-id="c8837-210">Select a **Reason code** and include any comments.</span></span>

3. <span data-ttu-id="c8837-211">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="c8837-211">Select **OK**.</span></span>

## <a name="dismiss-a-candidate"></a><span data-ttu-id="c8837-212">Hunsa umsækjanda</span><span class="sxs-lookup"><span data-stu-id="c8837-212">Dismiss a candidate</span></span>

<span data-ttu-id="c8837-213">Þú getur hunsað umsækjanda eftir ráðningu þeirra, ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="c8837-213">If needed, you can dismiss a candidate after hiring them.</span></span> <span data-ttu-id="c8837-214">Til dæmis gæti umsækjandi hafnað tilboðinu eða ekki mætt fyrsta daginn.</span><span class="sxs-lookup"><span data-stu-id="c8837-214">For example, a candidate might reject your offer or not show up on their first day.</span></span>

- <span data-ttu-id="c8837-215">Veldu **Hunsa umsækjanda** á eyðublaði umsækjandans.</span><span class="sxs-lookup"><span data-stu-id="c8837-215">On the candidate form, select **Dismiss candidate**.</span></span>

  ![Hunsa umsækjanda](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a><span data-ttu-id="c8837-217">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="c8837-217">See also</span></span>

[<span data-ttu-id="c8837-218">Skilgreina Common Data Service sýndareiningar</span><span class="sxs-lookup"><span data-stu-id="c8837-218">Configure Common Data Service virtual entities</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="c8837-219">Skipuleggja starfsfólk</span><span class="sxs-lookup"><span data-stu-id="c8837-219">Organize your workforce</span></span>](hr-personnel-departments-jobs-positions.md)<br>
[<span data-ttu-id="c8837-220">Setja upp íhluti verks</span><span class="sxs-lookup"><span data-stu-id="c8837-220">Set up the components of a job</span></span>](hr-personnel-jobs.md)