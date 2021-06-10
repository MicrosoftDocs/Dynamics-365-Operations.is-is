---
title: Stjórna leyfisbeiðnum í Teams
description: Þetta efnisatriði sýnir hvernig á að biðja um frí í Dynamics 365 Human Resources forritinu í Microsoft Teams.
author: andreabichsel
ms.date: 05/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 661bb8369fe4dbe6cdf6ee0fb05d16f4350ecf5a
ms.sourcegitcommit: c5c8f19a696ad4a3d68dffd63bfe7b484b999d2b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/25/2021
ms.locfileid: "6097260"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="618cf-103">Stjórna leyfisbeiðnum í Teams</span><span class="sxs-lookup"><span data-stu-id="618cf-103">Manage leave requests in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="618cf-104">Dynamics 365 Human Resources -forritið í Microsoft Teams gerir þér kleift að biðja um frí og skoða upplýsingar um stöðu frítíma í Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="618cf-104">The Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="618cf-105">Hægt er að eiga samskipti við þjarka til að óska eftir upplýsingum og byrja leyfisbeiðni.</span><span class="sxs-lookup"><span data-stu-id="618cf-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="618cf-106">Finna má ítarlegri upplýsingar á flipanum **Frí**.</span><span class="sxs-lookup"><span data-stu-id="618cf-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="618cf-107">Einnig er hægt að senda fólki upplýsingar um væntanlegan frítíma í hópum og spjalli utan Human Resources.</span><span class="sxs-lookup"><span data-stu-id="618cf-107">You can also send people information about your upcoming time off in Teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="618cf-108">Setja upp forritið</span><span class="sxs-lookup"><span data-stu-id="618cf-108">Install the app</span></span>

<span data-ttu-id="618cf-109">Hægt er að finna Dynamics 365 Human Resources forritið í Teams versluninni.</span><span class="sxs-lookup"><span data-stu-id="618cf-109">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="618cf-110">Í Microsoft Teams skal fara á lista yfir forrit.</span><span class="sxs-lookup"><span data-stu-id="618cf-110">In Microsoft Teams, navigate to the list of apps.</span></span>
 
2. <span data-ttu-id="618cf-111">Leitið að Dynamics 365 Human Resources og veljið síðan reitinn **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="618cf-111">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

3. <span data-ttu-id="618cf-112">Veljið hnappinn **Bæta við** til að setja upp forritið.</span><span class="sxs-lookup"><span data-stu-id="618cf-112">Select the **Add** button to install the app.</span></span>

<span data-ttu-id="618cf-113">Ef forritið skráir þig ekki sjálfkrafa inn skaltu velja flipann **Stillingar** til að skrá þig inn.</span><span class="sxs-lookup"><span data-stu-id="618cf-113">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

> [!NOTE]
> <span data-ttu-id="618cf-114">Ef þú sérð ekki innskráningarglugga skaltu athuga vafrastillingarnar þínar til að leyfa sprettiglugga.</span><span class="sxs-lookup"><span data-stu-id="618cf-114">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="618cf-115">Ef þú hefur aðgang að fleiri en einu tilviki af Human Resources er hægt að velja hvaða umhverfi á að tengja við á flipanum **Stillingar**.</span><span class="sxs-lookup"><span data-stu-id="618cf-115">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="618cf-116">Forritið styður nú öryggishlutverk kerfisstjóra.</span><span class="sxs-lookup"><span data-stu-id="618cf-116">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="618cf-117">Nota þjarkann</span><span class="sxs-lookup"><span data-stu-id="618cf-117">Use the bot</span></span>

<span data-ttu-id="618cf-118">Þegar forritið hefur verið sett upp birtast boð með upplýsingar um þær aðgerðir sem þjarkinn getur gripið til.</span><span class="sxs-lookup"><span data-stu-id="618cf-118">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

> [!NOTE]
> <span data-ttu-id="618cf-119">Hugsanlega þarf að skrá sig inn við fyrstu samskipti við þjarkann.</span><span class="sxs-lookup"><span data-stu-id="618cf-119">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="618cf-120">Ef þú sérð ekki innskráningarglugga skaltu athuga vafrastillingarnar þínar til að leyfa sprettiglugga.</span><span class="sxs-lookup"><span data-stu-id="618cf-120">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="618cf-121">Hægt er að spyrja þjarkann um að:</span><span class="sxs-lookup"><span data-stu-id="618cf-121">You can ask the bot to:</span></span>

- <span data-ttu-id="618cf-122">Skoða núgildandi leyfisstöðu þína.</span><span class="sxs-lookup"><span data-stu-id="618cf-122">View your current leave balances.</span></span> <span data-ttu-id="618cf-123">Til dæmis er hægt að senda skilaboð sem segja „Skoða leyfisstöður“.</span><span class="sxs-lookup"><span data-stu-id="618cf-123">For example, send a message that says, "View leave balances."</span></span>

- <span data-ttu-id="618cf-124">Hefja leyfisbeiðni fyrir notanda.</span><span class="sxs-lookup"><span data-stu-id="618cf-124">Start a leave request for you.</span></span> <span data-ttu-id="618cf-125">Til dæmis geturðu sent skilaboð sem segja „Taka frí“ eða „Mig langar að taka frí næsta fimmtudag og föstudag“ til að vera nákvæmari þegar óskað er eftir leyfi fyrir leyfisgerðina frí.</span><span class="sxs-lookup"><span data-stu-id="618cf-125">For example, send a message that says, “Take time off” or “I want to take vacation time off next Thursday and Friday” to be more specific for requesting leave for the vacation leave type.</span></span> 

  ![Hefja beiðni um leyfi í Teams spjalli](./media/hr-teams-leave-app-initiate.png)

- <span data-ttu-id="618cf-127">Spjallarinn mun fylla út leyfibeiðni fyrir þig.</span><span class="sxs-lookup"><span data-stu-id="618cf-127">The chat bot will populate a leave request for you.</span></span> <span data-ttu-id="618cf-128">Veljið **Biðja um frí** til að biðja um og breyta upplýsingum um beiðnina.</span><span class="sxs-lookup"><span data-stu-id="618cf-128">Select **Request time off** and edit the details for your request.</span></span>

   <span data-ttu-id="618cf-129">Ef óskað er eftir að senda inn leyfisbeiðnir fyrir margar leyfisgerðir fyrir sömu dagsetninguna skal velja valkostinn **Degi skipt með** í valmyndinni **Fleiri valkostir**.</span><span class="sxs-lookup"><span data-stu-id="618cf-129">If you want to submit leave requests for multiple leave types for the same date, select the **Split day with** option from the **More options** menu.</span></span> 

   <span data-ttu-id="618cf-130">Ef þú velur leyfi í hálfan dag þegar eining leyfisbeiðni er í dögum er hægt að tilgreina hvort beðið sé um frí fyrri hluta dags eða þann seinni með því að velja valkostinn **Skilgreining á hálfum degi** í valmyndinni **Fleiri valkostir**.</span><span class="sxs-lookup"><span data-stu-id="618cf-130">If you select a half day leave when the leave request unit is in days, you can specify whether you want to request time off the first half day or the second half day by selecting the **Half day definition** option from the **More options** menu.</span></span>
   
   ![Skilgreiningar hálfs dags](./media/HalfDayDefinitions.png)

- <span data-ttu-id="618cf-132">Þegar búið er að breyta upplýsingunum um leyfisbeiðni skal velja **Senda** til að senda þær til samþykkis.</span><span class="sxs-lookup"><span data-stu-id="618cf-132">When you're done editing your leave request details, select **Submit** to submit it for approval.</span></span>

  ![Staðfesta leyfisbeiðni](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="618cf-134">Stjórna leyfi í Teams</span><span class="sxs-lookup"><span data-stu-id="618cf-134">Manage your leave in Teams</span></span>

<span data-ttu-id="618cf-135">Flipinn **Frí** býður upp á skoðun:</span><span class="sxs-lookup"><span data-stu-id="618cf-135">The **Time off** tab allows you to view:</span></span> 

- <span data-ttu-id="618cf-136">Stöðuupplýsingar fyrir hverjar leyfisgerðir sem þú ert skráð(ur) í</span><span class="sxs-lookup"><span data-stu-id="618cf-136">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="618cf-137">Næstu leyfisbeiðnir</span><span class="sxs-lookup"><span data-stu-id="618cf-137">Upcoming leave requests</span></span>

- <span data-ttu-id="618cf-138">Fríbeiðnir</span><span class="sxs-lookup"><span data-stu-id="618cf-138">Time-off requests</span></span>

- <span data-ttu-id="618cf-139">Drög að leyfisbeiðnum</span><span class="sxs-lookup"><span data-stu-id="618cf-139">Draft leave requests</span></span>
 
### <a name="create-a-new-request"></a><span data-ttu-id="618cf-140">Búa til nýja beiðni</span><span class="sxs-lookup"><span data-stu-id="618cf-140">Create a new request</span></span>

1. <span data-ttu-id="618cf-141">Til að stofna nýja leyfisbeiðni skal velja **Ný beiðni**.</span><span class="sxs-lookup"><span data-stu-id="618cf-141">To create a new leave request, select **New request**.</span></span>

2. <span data-ttu-id="618cf-142">Sláðu inn daginn eða dagana þar sem þú vilt taka frí og veldu svo **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="618cf-142">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Bæta við fríi Human Resources Teams-forriti fyrir leyfi](./media/TimeOffHours.png)

3. <span data-ttu-id="618cf-144">Slá inn ástæðukóða, ef við á.</span><span class="sxs-lookup"><span data-stu-id="618cf-144">If applicable, enter a reason code.</span></span> <span data-ttu-id="618cf-145">Einnig skal færa inn athugasemdir og bæta við viðhengjum.</span><span class="sxs-lookup"><span data-stu-id="618cf-145">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="618cf-146">Veljið valkostinn **Degi skipt með** úr valmyndinni **Fleiri valkostir** ef ætlunin er að senda inn margar færslur leyfisbeiðni fyrir sama daginn fyrir mismunandi leyfisgerðir.</span><span class="sxs-lookup"><span data-stu-id="618cf-146">Select the **Split day with** option from the **More options** menu if you want to submit multiple leave request entries for the same date for different leave types.</span></span>

5. <span data-ttu-id="618cf-147">Veljið valkostinn **Skilgreining á hálfum degi** til að tilgreina hvort ætlunin sé að biðja um frí fyrri hluta dags eða seinni hluta dags.</span><span class="sxs-lookup"><span data-stu-id="618cf-147">Select the **Half day definition** option to specify if you want to request the first half day off or the second half day off.</span></span> <span data-ttu-id="618cf-148">Þessi valkostur er í boði þegar eining leyfisbeiðni er í dögum og upphæðin sem beðið er um er 0,5 dagar.</span><span class="sxs-lookup"><span data-stu-id="618cf-148">This option is available when the leave request unit is in days and the amount requested is 0.5 days.</span></span>

6. <span data-ttu-id="618cf-149">Þegar upplýsingar hafa verið færðar inn skal ýta á **Senda inn** til að senda þetta inn til samþykktar.</span><span class="sxs-lookup"><span data-stu-id="618cf-149">When you're done entering information, enter **Submit** to submit it for approval.</span></span> <span data-ttu-id="618cf-150">Einnig er hægt að færa inn **Vista sem drög** til að koma aftur síðar.</span><span class="sxs-lookup"><span data-stu-id="618cf-150">You can also enter **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="618cf-151">Stjórna dragabeiðnum</span><span class="sxs-lookup"><span data-stu-id="618cf-151">Manage draft requests</span></span>

1. <span data-ttu-id="618cf-152">Veljið flipann **Drög**.</span><span class="sxs-lookup"><span data-stu-id="618cf-152">Select the **Drafts** tab.</span></span>

2. <span data-ttu-id="618cf-153">Veldu blýantinn til að breyta beiðninni eða ruslið til að eyða henni.</span><span class="sxs-lookup"><span data-stu-id="618cf-153">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="618cf-154">Gerið nauðsynlegar breytingar.</span><span class="sxs-lookup"><span data-stu-id="618cf-154">Make any necessary changes.</span></span> <span data-ttu-id="618cf-155">Þegar búið er að færa inn upplýsingar skal slá inn **Senda** til að senda hana til samþykkis.</span><span class="sxs-lookup"><span data-stu-id="618cf-155">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="618cf-156">Einnig er hægt að velja **Vista sem drög** til að gera þetta síðar.</span><span class="sxs-lookup"><span data-stu-id="618cf-156">You can also select **Save as draft** to come back to it later.</span></span>
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="618cf-157">Bregðast við tilkynningum Teams</span><span class="sxs-lookup"><span data-stu-id="618cf-157">Respond to Teams notifications</span></span>

<span data-ttu-id="618cf-158">Þegar þú eða starfskraftur sem þú ert samþykktaraðili fyrir sendir beiðni um leyfi fyrir færðu senda tilkynningu í Human Resources forritinu í Teams.</span><span class="sxs-lookup"><span data-stu-id="618cf-158">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="618cf-159">Hægt er að velja tilkynninguna til að skoða hana.</span><span class="sxs-lookup"><span data-stu-id="618cf-159">You can select the notification to view it.</span></span> <span data-ttu-id="618cf-160">Tilkynningar birtast einnig á svæðinu **Spjall**.</span><span class="sxs-lookup"><span data-stu-id="618cf-160">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="618cf-161">Ef notandi er samþykkjandi er hægt að velja **Samþykkja** eða **Neita** í tilkynningunni.</span><span class="sxs-lookup"><span data-stu-id="618cf-161">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="618cf-162">Einnig er hægt að búa til valfrjáls skilaboð.</span><span class="sxs-lookup"><span data-stu-id="618cf-162">You can also provide an optional message.</span></span>

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="618cf-163">Senda upplýsingar um væntanlegt frí til samstarfsfólks</span><span class="sxs-lookup"><span data-stu-id="618cf-163">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="618cf-164">Eftir að Human Resources er sett upp fyrir Teams er auðveldlega hægt að senda upplýsingar um væntanlegt frí til samstarfsfólks í hópum og spjalli.</span><span class="sxs-lookup"><span data-stu-id="618cf-164">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="618cf-165">Í hópi eða spjalli í Teams skal velja hnapp Human Resources fyrir neðan spjallgluggann.</span><span class="sxs-lookup"><span data-stu-id="618cf-165">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![Hnappur Human Resources fyrir neðan spjallglugga](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="618cf-167">Veljið leyfisbeiðnina sem á að deila.</span><span class="sxs-lookup"><span data-stu-id="618cf-167">Select the leave request you want to share.</span></span> <span data-ttu-id="618cf-168">Ef óskað er eftir að deila drögum að leyfisbeiðni skal byrja á því að velja **Drög**.</span><span class="sxs-lookup"><span data-stu-id="618cf-168">If you want to share a draft leave request, select **Drafts** first.</span></span>

<span data-ttu-id="618cf-169">Leyfisbeiðnin mun birtast í spjallinu.</span><span class="sxs-lookup"><span data-stu-id="618cf-169">Your leave request will display in the chat.</span></span>

<span data-ttu-id="618cf-170">Ef drög að beiðni var deilt mun þau birtast sem drög.</span><span class="sxs-lookup"><span data-stu-id="618cf-170">If you shared a draft request, it will display as a draft.</span></span>

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="618cf-171">Skoða frídagatal teymisins</span><span class="sxs-lookup"><span data-stu-id="618cf-171">View your team's leave calendar</span></span>

<span data-ttu-id="618cf-172">Ef þú ert yfirmaður með beina undirmenn getur þú skoðað samþykkt frí hópsins þíns og frí í bið.</span><span class="sxs-lookup"><span data-stu-id="618cf-172">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="618cf-173">Í forritinu „Human Resources“ í Teams skal velja **Frí**.</span><span class="sxs-lookup"><span data-stu-id="618cf-173">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="618cf-174">Veldu **Team dagatal**.</span><span class="sxs-lookup"><span data-stu-id="618cf-174">Select **Team calendar**.</span></span> <span data-ttu-id="618cf-175">Dagatalið birtir samþykkt frí og frí í bið fyrir beina undirmenn þína.</span><span class="sxs-lookup"><span data-stu-id="618cf-175">The calendar displays your direct reports' approved and pending time off.</span></span>

   > [!NOTE]
   > <span data-ttu-id="618cf-176">Ef ekki er hægt að sjá hópdagatalið skal biðja kerfisstjóra um að virkja það.</span><span class="sxs-lookup"><span data-stu-id="618cf-176">If you can't see the team calendar, ask your admin to enable it.</span></span> <span data-ttu-id="618cf-177">Frekari upplýsingar eru í [Setja upp](hr-admin-teams-leave-app.md#install-and-setup).</span><span class="sxs-lookup"><span data-stu-id="618cf-177">For more information, see [Install and setup](hr-admin-teams-leave-app.md#install-and-setup).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="618cf-178">Studd tungumál</span><span class="sxs-lookup"><span data-stu-id="618cf-178">Supported languages</span></span>

<span data-ttu-id="618cf-179">Forritið Dynamics 365 Human Resources í Teams styður eftirfarandi tungumál:</span><span class="sxs-lookup"><span data-stu-id="618cf-179">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="618cf-180">Landstaðalskenni</span><span class="sxs-lookup"><span data-stu-id="618cf-180">Locale ID</span></span> | <span data-ttu-id="618cf-181">Tungumál</span><span class="sxs-lookup"><span data-stu-id="618cf-181">Language</span></span> |
| --- | --- |
| <span data-ttu-id="618cf-182">de-DE</span><span class="sxs-lookup"><span data-stu-id="618cf-182">de-DE</span></span> | <span data-ttu-id="618cf-183">Þýska (Þýskaland)</span><span class="sxs-lookup"><span data-stu-id="618cf-183">German (Germany)</span></span> |
| <span data-ttu-id="618cf-184">es-ES</span><span class="sxs-lookup"><span data-stu-id="618cf-184">es-ES</span></span> | <span data-ttu-id="618cf-185">Spænska (Spánn)</span><span class="sxs-lookup"><span data-stu-id="618cf-185">Spanish (Spain)</span></span> |
| <span data-ttu-id="618cf-186">es-MX</span><span class="sxs-lookup"><span data-stu-id="618cf-186">es-MX</span></span> | <span data-ttu-id="618cf-187">Spænska (Mexíkó)</span><span class="sxs-lookup"><span data-stu-id="618cf-187">Spanish (Mexico)</span></span> |
| <span data-ttu-id="618cf-188">fr-CA</span><span class="sxs-lookup"><span data-stu-id="618cf-188">fr-CA</span></span> | <span data-ttu-id="618cf-189">franska (Kanada)</span><span class="sxs-lookup"><span data-stu-id="618cf-189">French (Canada)</span></span> |
| <span data-ttu-id="618cf-190">fr-FR</span><span class="sxs-lookup"><span data-stu-id="618cf-190">fr-FR</span></span> | <span data-ttu-id="618cf-191">Franska (Frakkland)</span><span class="sxs-lookup"><span data-stu-id="618cf-191">French (France)</span></span> |
| <span data-ttu-id="618cf-192">it-IT</span><span class="sxs-lookup"><span data-stu-id="618cf-192">it-IT</span></span> | <span data-ttu-id="618cf-193">Ítalska (Ítalía)</span><span class="sxs-lookup"><span data-stu-id="618cf-193">Italian (Italy)</span></span> |
| <span data-ttu-id="618cf-194">nl-NL</span><span class="sxs-lookup"><span data-stu-id="618cf-194">nl-NL</span></span> | <span data-ttu-id="618cf-195">Hollenska (Holland)</span><span class="sxs-lookup"><span data-stu-id="618cf-195">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="618cf-196">pt-BR</span><span class="sxs-lookup"><span data-stu-id="618cf-196">pt-BR</span></span> | <span data-ttu-id="618cf-197">Portúgalska (Brasilía)</span><span class="sxs-lookup"><span data-stu-id="618cf-197">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="618cf-198">tr-TR</span><span class="sxs-lookup"><span data-stu-id="618cf-198">tr-TR</span></span> | <span data-ttu-id="618cf-199">Tyrkneska (Tyrkland)</span><span class="sxs-lookup"><span data-stu-id="618cf-199">Turkish (Turkey)</span></span> |
| <span data-ttu-id="618cf-200">zh-CN</span><span class="sxs-lookup"><span data-stu-id="618cf-200">zh-CN</span></span> | <span data-ttu-id="618cf-201">kínverska (einfölduð)</span><span class="sxs-lookup"><span data-stu-id="618cf-201">Chinese (Simplified)</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="618cf-202">Úrræðaleit</span><span class="sxs-lookup"><span data-stu-id="618cf-202">Troubleshooting</span></span>

<span data-ttu-id="618cf-203">Ef þú átt í vandræðum með að skrá þig inn í eða nota forritið Human Dynamics 365 Human Resources skaltu reyna að fylgja þessum leiðbeiningum úrræðaleitar.</span><span class="sxs-lookup"><span data-stu-id="618cf-203">If you're having trouble signing into or using the Dynamics 365 Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="618cf-204">Ef þú átt enn í vandræðum eftir úrræðaleit skaltu hafa samband við notendaþjónustu.</span><span class="sxs-lookup"><span data-stu-id="618cf-204">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="618cf-205">Frekari upplýsingar er að finna í [Fá stuðning](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="618cf-205">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="618cf-206">Ekki er hægta að skrá inn í forritið „Human Resources“ í Teams</span><span class="sxs-lookup"><span data-stu-id="618cf-206">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="618cf-207">Ef þú getur ekki skráð þig inn í forritið er hugsanlegt að reikningurinn sem þú notar til að skrá þig inn í Microsoft Teams sé ekki tengdur við starfsmannafærslu í Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="618cf-207">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="618cf-208">Hafa skal samskipti við kerfisstjóra til að tryggja að starfsmannafærslan sé rétt tengd.</span><span class="sxs-lookup"><span data-stu-id="618cf-208">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="translations-dont-display-correctly"></a><span data-ttu-id="618cf-209">Þýðingar birtast ekki rétt</span><span class="sxs-lookup"><span data-stu-id="618cf-209">Translations don't display correctly</span></span>

<span data-ttu-id="618cf-210">Ef þýðingar birtast ekki eins og búist er við skal ganga úr skugga um tungumálið sem var valið í Teams passi við valið tungumál í **Valkostum notanda** í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="618cf-210">If translations don't display as expected, make sure the language you select in Teams matches the language selected in Human Resources **User options**.</span></span>

<span data-ttu-id="618cf-211">Í Teams skal skoða **Tungumál forrits** í **Stillingum**.</span><span class="sxs-lookup"><span data-stu-id="618cf-211">In Teams, look at **App language** in **Settings**.</span></span>

![Teams stillingar](./media/hr-teams-leave-app-settings.png)

<span data-ttu-id="618cf-213">Í Human Resources skal velja **Stillingar** og síðan velja **Valkostir notanda**.</span><span class="sxs-lookup"><span data-stu-id="618cf-213">In Human Resources, select **Settings** and then select **User options**.</span></span> <span data-ttu-id="618cf-214">Gangið úr skugga um að reiturinn **Tungumál** samsvari reitnum **Tungumál forrits** í Teams.</span><span class="sxs-lookup"><span data-stu-id="618cf-214">Verify that the **Language** field matches the **App language** field in Teams.</span></span>

![Valkostir notenda mannauðs](./media/hr-teams-leave-app-user-options.png)

<span data-ttu-id="618cf-216">Láttu okkur vita ef vandamál vegna þýðinga er enn til staðar.</span><span class="sxs-lookup"><span data-stu-id="618cf-216">If you still experience translation issues, let us know.</span></span> <span data-ttu-id="618cf-217">Frekari upplýsingar er að finna í [Fá stuðning fyrir Finance and Operations-forrit eða Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="618cf-217">For information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="618cf-218">Villa þegar leyfisbeiðnir eru samþykktar í forriti Human Resources í Teams</span><span class="sxs-lookup"><span data-stu-id="618cf-218">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="618cf-219">Ef villa kemur upp þegar verið er að reyna að samþykkja leyfisbeiðnir í Teams, skal prófa að fara í gegnum eftirfarandi villuleitarskref:</span><span class="sxs-lookup"><span data-stu-id="618cf-219">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="618cf-220">Gangið úr skugga um að reikningurinn sem er notaður til að skrá sig inn í Microsoft Teams sé sá sami og notaður er til að fá aðgang að Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="618cf-220">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="618cf-221">Vertu viss um að þú sért gildur samþykktaraðili fyrir beiðnina með því að athuga stillingar verkflæðis fyrir samþykkt leyfis.</span><span class="sxs-lookup"><span data-stu-id="618cf-221">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="618cf-222">Frekari upplýsingar um verkflæði leyfisbeiðna er að finna í [Búa til verkflæði leyfisbeiðni](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="618cf-222">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a><span data-ttu-id="618cf-223">Samþykkisaðilar leyfis fá ekki spjallskilaboð úr Teams til að samþykkja leyfisbeiðnir</span><span class="sxs-lookup"><span data-stu-id="618cf-223">Leave approvers don't receive Teams chat messages to approve leave requests</span></span>

1. <span data-ttu-id="618cf-224">Gangið úr skugga um að tilkynningar séu virkar fyrir umhverfið og notandann.</span><span class="sxs-lookup"><span data-stu-id="618cf-224">Ensure notifications are enabled for the environment and the user.</span></span> <span data-ttu-id="618cf-225">Frekari upplýsingar er að finna í [Virkja tilkynningar fyrir Human Resources-forritið í Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) og [Kveikja eða slökkva á tilkynningum Teams fyrir einstaka notendur](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span><span class="sxs-lookup"><span data-stu-id="618cf-225">For more information, see [Enable notifications for the Human Resources app in Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) and [Turn Teams notifications on or off for individual users](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span></span>

2. <span data-ttu-id="618cf-226">Gangið úr skugga um að notendur séu skráði inn í flipann **Spjall** með sömu innskráningarupplýsingunum og þeir nota til að samþykkja leyfisbeiðnir.</span><span class="sxs-lookup"><span data-stu-id="618cf-226">Ensure users are signed into the **Chats** tab with the same credentials they use for approving leave requests.</span></span> <span data-ttu-id="618cf-227">Notið skilaboðin „skrá út“ og síðan „skrá inn“ til að skrá inn með réttum innskráningarupplýsingum.</span><span class="sxs-lookup"><span data-stu-id="618cf-227">Use the messages "sign out" and then "sign in" to sign in with the correct credentials.</span></span>

3. <span data-ttu-id="618cf-228">Ef vandinn er enn til staðar skal athuga runuvinnslu kerfis í Business Events sem kerfisstjóri.</span><span class="sxs-lookup"><span data-stu-id="618cf-228">If the issue persists, check the status of the Business Events system batch job as a system administrator.</span></span> <span data-ttu-id="618cf-229">Ef það er á biðstigi eða framkvæmdastigi skal athuga aftur eftir nokkrar mínútur.</span><span class="sxs-lookup"><span data-stu-id="618cf-229">If it's in a waiting or executing stage, check back in a few minutes.</span></span> <span data-ttu-id="618cf-230">Ef staðan helst óbreytt skal skrá þjónustubeiðni svo teymið okkar geti hjálpað til við að leysa úr vandamálinu.</span><span class="sxs-lookup"><span data-stu-id="618cf-230">If the status remains unchanged, log a support ticket so our team can help resolve the issue.</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="618cf-231">Þekkta aðgengisvandamál</span><span class="sxs-lookup"><span data-stu-id="618cf-231">Known accessibility issues</span></span>

<span data-ttu-id="618cf-232">Human Resources-forritið í Teams er með eftirfarandi aðgengisvandamál sem við vinnum að lagfæringum á í síðari útgáfum.</span><span class="sxs-lookup"><span data-stu-id="618cf-232">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="618cf-233">Úthreyfing</span><span class="sxs-lookup"><span data-stu-id="618cf-233">Issue</span></span> | <span data-ttu-id="618cf-234">Hjáleið eða skýring</span><span class="sxs-lookup"><span data-stu-id="618cf-234">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="618cf-235">Ef 400% aðdráttur er notaður á skjáborði eru sumir aðgerðahnappar ekki sýnilegir.</span><span class="sxs-lookup"><span data-stu-id="618cf-235">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="618cf-236">Mælt er með því að notað sé stækkunargler þar til við styðjum þennan aðdrátt.</span><span class="sxs-lookup"><span data-stu-id="618cf-236">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="618cf-237">Á flipanum **Frí** tilkynnir upplestur hnappaaðgerð þegar hausinn hnitanetsins er lesinn fyrir fríið.</span><span class="sxs-lookup"><span data-stu-id="618cf-237">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="618cf-238">Haus og einingar innan hnitanetsins eru flokkaðar eftir árum og eru samanfellanlegar.</span><span class="sxs-lookup"><span data-stu-id="618cf-238">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="618cf-239">Upplestur skilur þetta sem aðgerðarhlut, sem það er ekki.</span><span class="sxs-lookup"><span data-stu-id="618cf-239">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="618cf-240">Á flipanum **Frí** er aukaleg strokhreyfing þegar verið er að fletta að **Ástæðukóði** í nýrri beiðni.</span><span class="sxs-lookup"><span data-stu-id="618cf-240">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="618cf-241">Engin falin stjórnun er til staðar sem storkufletting er að reyna að ná til.</span><span class="sxs-lookup"><span data-stu-id="618cf-241">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="618cf-242">Á flipanum **Frí**, ef strokið á meðan dagatalið er opið, er endað utan stýringar í stað upphafs nýrrar beiðni eða þegar beiðni er breytt.</span><span class="sxs-lookup"><span data-stu-id="618cf-242">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="618cf-243">Þegar komið er að **Fara á daginn í dag** er það síðasti hlutinn og strokið er í öfuga átt til að komast aftur efst.</span><span class="sxs-lookup"><span data-stu-id="618cf-243">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="618cf-244">Á flipanum **Spjall** er farið aftur á toppinn þegar dagsetningin er slegin inn á meðan verið er að nota hjálpartækið eða lyklaborðið.</span><span class="sxs-lookup"><span data-stu-id="618cf-244">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="618cf-245">Flipi þar til þú nærð innsláttarsvæðinu aftur.</span><span class="sxs-lookup"><span data-stu-id="618cf-245">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="618cf-246">Tilkynning um persónuvernd</span><span class="sxs-lookup"><span data-stu-id="618cf-246">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="618cf-247">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="618cf-247">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="618cf-248">Með Dynamics 365 Human Resources þjarkanum í Microsoft Teams er texti notanda greindur til að skilja undirliggjandi fyrirspurn/ásetning.</span><span class="sxs-lookup"><span data-stu-id="618cf-248">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="618cf-249">Inntak notanda á borð við „Leita í Contoso-reikningi“ er flutt í eina af Cognitive Service hjá Microsoft sem kallast LUIS (Language Understanding Intelligent Service).</span><span class="sxs-lookup"><span data-stu-id="618cf-249">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="618cf-250">Lesa meira um LUIS  [hér](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="618cf-250">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="618cf-251">LUIS-þjónustan ræður úr eða skilur ásetning notanda (í þessu tilviki er ætlunin að finna upplýsingar) og markeiningu (í þessu tilviki er tilgreinda einingin reikningur sem heitir Contoso).</span><span class="sxs-lookup"><span data-stu-id="618cf-251">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="618cf-252">Þessar upplýsingar eru svo sendar í Microsoft [Azure þjarkaramma](https://azure.microsoft.com/services/bot-service/) sem vinnur með gögn úr Dynamics 365 Human Resources og sækir æskilegar upplýsingum fyrir fyrirspurn notanda.</span><span class="sxs-lookup"><span data-stu-id="618cf-252">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="618cf-253">Með því að setja upp og leyfa aðgang að þjarkanum samþykkir þú að leyfa LUIS-þjónustunni og Azure þjarkaramma að vinna úr ásetningi á bak við fyrirspurn, sem leiðir til betri notandaupplifunar.</span><span class="sxs-lookup"><span data-stu-id="618cf-253">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="618cf-254">LUIS-þjónustan og Azure þjarkaramminn kunna að hafa mismikið samræmi samanborið við Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="618cf-254">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="618cf-255">LUIS-þjónustan hefur aðeins aðgang að fyrirspurnum notenda og er ekki hönnuð til að tengjast við Dynamics 365 Human Resources gögn eða reikning. Notandi Dynamics 365 Human Resources þjarkans gæti fært inn fyrirspurn sem inniheldur gögn viðskiptavinar, persónuleg gögn eða önnur gögn og slíkt fyrirspurnarefni gæti verið sent til LUIS-þjónustunnar og Azure þjarkarammans.</span><span class="sxs-lookup"><span data-stu-id="618cf-255">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="618cf-256">Innihald fyrirspurna og skilaboða notanda er vistað í LUIS-kerfi í að hámarki 30 daga, er dulkóðað þegar ekki í notkun og er ekki notað fyrir þjálfun eða endurbætur á þjónustu.</span><span class="sxs-lookup"><span data-stu-id="618cf-256">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="618cf-257">Lestu meira um Cognitive Services  [hér](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="618cf-257">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="618cf-258">Til að stjórna stjórnandastillingum fyrir forrit í Microsoft Teams er farið í [Microsoft Teams stjórnendamiðstöð](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="618cf-258">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="618cf-259">Microsoft Teams, hnitanet Azure-tilviks og Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="618cf-259">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="618cf-260">Þegar Dynamics 365 Human Resources-forritið er notað í Microsoft Teams geta tiltekin gögn um viðskiptavini flætt út fyrir landsvæðið þar sem biðlari Human Resources þjónustunnar er notaður.</span><span class="sxs-lookup"><span data-stu-id="618cf-260">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="618cf-261">Dynamics 365 Human Resources sendir upplýsingar um leyfisbeiðni og verkflæðisverk til Microsoft Azure tilviks hnitanets og Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="618cf-261">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="618cf-262">Þessi gögn má geyma í Microsoft Azure Event Grid í allt að sólarhring og verða unnin í Bandaríkjunum, þau er dulkóðuð í flutningi og í hvíld, og eru ekki notuð af Microsoft eða meðhöndlunaraðilum fyrir þjálfun eða þjónustuúrbætur.</span><span class="sxs-lookup"><span data-stu-id="618cf-262">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="618cf-263">Til að skilja hvar gögnin þín eru geymd í Teams skaltu skoða: [Staðsetning gagna í Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="618cf-263">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>

<span data-ttu-id="618cf-264">Í samskiptum við spjallarann í forriti Human Resources, er hægt að geyma innihald samtalsins í Azure Cosmos DB og flytja það yfir í Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="618cf-264">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="618cf-265">Þessi gögn má geyma í Azure Cosmos DB í allt að sólarhring og kunna að vera meðhöndluð utan staðsetningarinnar þar sem Human Resources-þjónusta leigjandans er uppsett, þau er dulkóðuð í flutningi og í hvíld, og eru ekki notuð af Microsoft eða meðhöndlunaraðilum fyrir þjálfun eða þjónustuúrbætur.</span><span class="sxs-lookup"><span data-stu-id="618cf-265">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="618cf-266">Til að skilja hvar gögnin þín eru geymd í Teams skaltu skoða: [Staðsetning gagna í Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="618cf-266">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>
 
<span data-ttu-id="618cf-267">Til að takmarka aðgang að Human Resources í Microsoft Teams fyrir fyrirtækið þitt eða notendur innan fyrirtækisins skal skoða [Stjórna reglum um forritsheimildir í Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="618cf-267">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="618cf-268">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="618cf-268">See also</span></span>

[<span data-ttu-id="618cf-269">Sækja og setja upp Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="618cf-269">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="618cf-270">Microsoft Teams hjálparmiðstöð</span><span class="sxs-lookup"><span data-stu-id="618cf-270">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="618cf-271">Forritið „Human Resources“ í Teams</span><span class="sxs-lookup"><span data-stu-id="618cf-271">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
