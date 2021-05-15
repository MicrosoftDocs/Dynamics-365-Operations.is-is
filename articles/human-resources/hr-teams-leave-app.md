---
title: Stjórna leyfisbeiðnum í Teams
description: Þetta efnisatriði sýnir hvernig á að biðja um frí í Dynamics 365 Human Resources forritinu í Microsoft Teams.
author: andreabichsel
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2ea495259ba29f302753991e260d5a8fa990322b
ms.sourcegitcommit: e3f11fc9a9dae416a490437678bb482a0094f9a9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/27/2021
ms.locfileid: "5953413"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="b6cd2-103">Stjórna leyfisbeiðnum í Teams</span><span class="sxs-lookup"><span data-stu-id="b6cd2-103">Manage leave requests in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b6cd2-104">Dynamics 365 Human Resources -forritið í Microsoft Teams gerir þér kleift að biðja um frí og skoða upplýsingar um stöðu frítíma í Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-104">The Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="b6cd2-105">Hægt er að eiga samskipti við þjarka til að óska eftir upplýsingum og byrja leyfisbeiðni.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="b6cd2-106">Finna má ítarlegri upplýsingar á flipanum **Frí**.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="b6cd2-107">Einnig er hægt að senda fólki upplýsingar um væntanlegan frítíma í hópum og spjalli utan Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-107">You can also send people information about your upcoming time off in Teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="b6cd2-108">Setja upp forritið</span><span class="sxs-lookup"><span data-stu-id="b6cd2-108">Install the app</span></span>

<span data-ttu-id="b6cd2-109">Hægt er að finna Dynamics 365 Human Resources forritið í Teams versluninni.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-109">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="b6cd2-110">Í Microsoft Teams skal velja sporbauginn.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-110">In Microsoft Teams, select the ellipses.</span></span>

   ![Sporbaugur fyrir Human Resources Teams-forrit fyrir leyfi](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="b6cd2-112">Leitið að Dynamics 365 Human Resources og veljið síðan reitinn **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![Human Resources-spjald fyrir Human Resources Teams-forrit fyrir leyfi](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="b6cd2-114">Veljið hnappinn **Bæta við** til að setja upp forritið.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-114">Select the **Add** button to install the app.</span></span>

   ![Uppsetning Human Resources Teams-forrits fyrir leyfi](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="b6cd2-116">Ef forritið skráir þig ekki sjálfkrafa inn skaltu velja flipann **Stillingar** til að skrá þig inn.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Stillingaflipi Human Resources Teams-forrits fyrir leyfi](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="b6cd2-118">Ef þú sérð ekki innskráningarglugga skaltu athuga vafrastillingarnar þínar til að leyfa sprettiglugga.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="b6cd2-119">Ef þú hefur aðgang að fleiri en einu tilviki af Human Resources er hægt að velja hvaða umhverfi á að tengja við á flipanum **Stillingar**.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="b6cd2-120">Forritið styður nú öryggishlutverk kerfisstjóra.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="b6cd2-121">Nota þjarkann</span><span class="sxs-lookup"><span data-stu-id="b6cd2-121">Use the bot</span></span>

<span data-ttu-id="b6cd2-122">Þegar forritið hefur verið sett upp birtast boð með upplýsingar um þær aðgerðir sem þjarkinn getur gripið til.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Opnunarkveðja Human Resources Teams-þjarkaforrits fyrir leyfi](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="b6cd2-124">Hugsanlega þarf að skrá sig inn við fyrstu samskipti við þjarkann.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="b6cd2-125">Ef þú sérð ekki innskráningarglugga skaltu athuga vafrastillingarnar þínar til að leyfa sprettiglugga.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="b6cd2-126">Hægt er að spyrja þjarkann um að:</span><span class="sxs-lookup"><span data-stu-id="b6cd2-126">You can ask the bot to:</span></span>

- <span data-ttu-id="b6cd2-127">Hefja leyfisbeiðni fyrir notanda.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-127">Start a leave request for you.</span></span>

  ![Hefja beiðni um leyfi í Teams spjalli](./media/hr-teams-leave-app-initiate.png)

- <span data-ttu-id="b6cd2-129">Spjallarinn mun fylla út leyfibeiðni fyrir þig.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-129">The chat bot will populate a leave request for you.</span></span> <span data-ttu-id="b6cd2-130">Veljið **Biðja um frí** til að biðja um og breyta upplýsingum um beiðnina.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-130">Select **Request time off** and edit the details for your request.</span></span>

  ![Breyta upplýsingum leyfisbeiðni](./media/hr-teams-leave-app-details.png)

- <span data-ttu-id="b6cd2-132">Þegar búið er að breyta upplýsingunum um leyfisbeiðni skal velja **Senda** til að senda þær til samþykkis.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-132">When you're done editing your leave request details, select **Submit** to submit it for approval.</span></span>

  ![Staðfesta leyfisbeiðni](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="b6cd2-134">Stjórna leyfi í Teams</span><span class="sxs-lookup"><span data-stu-id="b6cd2-134">Manage your leave in Teams</span></span>

<span data-ttu-id="b6cd2-135">Flipinn **Frí** býður upp á skoðun:</span><span class="sxs-lookup"><span data-stu-id="b6cd2-135">The **Time off** tab allows you to view:</span></span> 

- <span data-ttu-id="b6cd2-136">Stöðuupplýsingar fyrir hverjar leyfisgerðir sem þú ert skráð(ur) í</span><span class="sxs-lookup"><span data-stu-id="b6cd2-136">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="b6cd2-137">Næstu leyfisbeiðnir</span><span class="sxs-lookup"><span data-stu-id="b6cd2-137">Upcoming leave requests</span></span>

- <span data-ttu-id="b6cd2-138">Fríbeiðnir</span><span class="sxs-lookup"><span data-stu-id="b6cd2-138">Time-off requests</span></span>

- <span data-ttu-id="b6cd2-139">Drög að leyfisbeiðnum</span><span class="sxs-lookup"><span data-stu-id="b6cd2-139">Draft leave requests</span></span>

![Fríflipi fyrir fríforrit Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="b6cd2-141">Búa til nýja beiðni</span><span class="sxs-lookup"><span data-stu-id="b6cd2-141">Create a new request</span></span>

1. <span data-ttu-id="b6cd2-142">Til að stofna nýja leyfisbeiðni skal velja **Ný beiðni**.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-142">To create a new leave request, select **New request**.</span></span>

   ![Ný beiðni fyrir Human Resources Teams-forrit fyrir leyfi](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="b6cd2-144">Sláðu inn daginn eða dagana þar sem þú vilt taka frí og veldu svo **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-144">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Bæta við fríi Human Resources Teams-forriti fyrir leyfi](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="b6cd2-146">Slá inn ástæðukóða, ef við á.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-146">If applicable, enter a reason code.</span></span> <span data-ttu-id="b6cd2-147">Einnig skal færa inn athugasemdir og bæta við viðhengjum.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-147">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="b6cd2-148">Þegar búið er að færa inn upplýsingar skal slá inn **Senda** til að senda hana til samþykkis.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-148">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="b6cd2-149">Einnig er hægt að slá inn **Vista sem drög** til að gera þetta síðar.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-149">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="b6cd2-150">Stjórna dragabeiðnum</span><span class="sxs-lookup"><span data-stu-id="b6cd2-150">Manage draft requests</span></span>

1. <span data-ttu-id="b6cd2-151">Veljið flipann **Drög**.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-151">Select the **Drafts** tab.</span></span>

   ![Dragaflipi í Human Resources Teams-forriti fyrir leyfi](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="b6cd2-153">Veldu blýantinn til að breyta beiðninni eða ruslið til að eyða henni.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-153">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="b6cd2-154">Gerið nauðsynlegar breytingar.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-154">Make any necessary changes.</span></span> <span data-ttu-id="b6cd2-155">Þegar búið er að færa inn upplýsingar skal slá inn **Senda** til að senda hana til samþykkis.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-155">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="b6cd2-156">Einnig er hægt að velja **Vista sem drög** til að gera þetta síðar.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-156">You can also select **Save as draft** to come back to it later.</span></span>

   ![Breyta drögum í Human Resources Teams-forriti fyrir leyfi](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="b6cd2-158">Bregðast við tilkynningum Teams</span><span class="sxs-lookup"><span data-stu-id="b6cd2-158">Respond to Teams notifications</span></span>

<span data-ttu-id="b6cd2-159">Þegar þú eða starfskraftur sem þú ert samþykktaraðili fyrir sendir beiðni um leyfi fyrir færðu senda tilkynningu í Human Resources forritinu í Teams.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-159">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="b6cd2-160">Hægt er að velja tilkynninguna til að skoða hana.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-160">You can select the notification to view it.</span></span> <span data-ttu-id="b6cd2-161">Tilkynningar birtast einnig á svæðinu **Spjall**.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-161">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="b6cd2-162">Ef notandi er samþykkjandi er hægt að velja **Samþykkja** eða **Neita** í tilkynningunni.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-162">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="b6cd2-163">Einnig er hægt að búa til valfrjáls skilaboð.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-163">You can also provide an optional message.</span></span>

![Senda beiðni um tilkynningar í forritinu Human Resources Teams](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="b6cd2-165">Senda upplýsingar um væntanlegt frí til samstarfsfólks</span><span class="sxs-lookup"><span data-stu-id="b6cd2-165">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="b6cd2-166">Eftir að Human Resources er sett upp fyrir Teams er auðveldlega hægt að senda upplýsingar um væntanlegt frí til samstarfsfólks í hópum og spjalli.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-166">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="b6cd2-167">Í hópi eða spjalli í Teams skal velja hnapp Human Resources fyrir neðan spjallgluggann.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-167">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![Hnappur Human Resources fyrir neðan spjallglugga](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="b6cd2-169">Veljið leyfisbeiðnina sem á að deila.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-169">Select the leave request you want to share.</span></span> <span data-ttu-id="b6cd2-170">Ef óskað er eftir að deila drögum að leyfisbeiðni skal byrja á því að velja **Drög**.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-170">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![Velja beiðni um væntanlegt frí til að deila](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="b6cd2-172">Leyfisbeiðnin mun birtast í spjallinu.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-172">Your leave request will display in the chat.</span></span>

![Leyfisbeiðnispjald Human Resources](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="b6cd2-174">Ef drög að beiðni var deilt mun þau birtast sem drög:</span><span class="sxs-lookup"><span data-stu-id="b6cd2-174">If you shared a draft request, it will display as a draft:</span></span>

![Drög að leyfisbeiðnispjaldi Human Resources](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="b6cd2-176">Skoða frídagatal teymisins</span><span class="sxs-lookup"><span data-stu-id="b6cd2-176">View your team's leave calendar</span></span>

<span data-ttu-id="b6cd2-177">Ef þú ert yfirmaður með beina undirmenn getur þú skoðað samþykkt frí hópsins þíns og frí í bið.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-177">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="b6cd2-178">Í forritinu „Human Resources“ í Teams skal velja **Frí**.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-178">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="b6cd2-179">Veldu **Team dagatal**.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-179">Select **Team calendar**.</span></span> <span data-ttu-id="b6cd2-180">Dagatalið birtir samþykkt frí og frí í bið fyrir beina undirmenn þína.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-180">The calendar displays your direct reports' approved and pending time off.</span></span>

   ![Skoða dagatal í Human Resources Teams-forriti](./media/hr-teams-leave-app-view-calendar.png)

   > [!NOTE]
   > <span data-ttu-id="b6cd2-182">Ef ekki er hægt að sjá hópdagatalið skal biðja kerfisstjóra um að virkja það.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-182">If you can't see the team calendar, ask your admin to enable it.</span></span> <span data-ttu-id="b6cd2-183">Frekari upplýsingar eru í [Setja upp](hr-admin-teams-leave-app.md#install-and-setup).</span><span class="sxs-lookup"><span data-stu-id="b6cd2-183">For more information, see [Install and setup](hr-admin-teams-leave-app.md#install-and-setup).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="b6cd2-184">Studd tungumál</span><span class="sxs-lookup"><span data-stu-id="b6cd2-184">Supported languages</span></span>

<span data-ttu-id="b6cd2-185"> Forritið Dynamics 365 Human Resources í Teams styður eftirfarandi tungumál:</span><span class="sxs-lookup"><span data-stu-id="b6cd2-185">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="b6cd2-186">Landstaðalskenni</span><span class="sxs-lookup"><span data-stu-id="b6cd2-186">Locale ID</span></span> | <span data-ttu-id="b6cd2-187">Tungumál</span><span class="sxs-lookup"><span data-stu-id="b6cd2-187">Language</span></span> |
| --- | --- |
| <span data-ttu-id="b6cd2-188">de-DE</span><span class="sxs-lookup"><span data-stu-id="b6cd2-188">de-DE</span></span> | <span data-ttu-id="b6cd2-189">Þýska (Þýskaland)</span><span class="sxs-lookup"><span data-stu-id="b6cd2-189">German (Germany)</span></span> |
| <span data-ttu-id="b6cd2-190">es-ES</span><span class="sxs-lookup"><span data-stu-id="b6cd2-190">es-ES</span></span> | <span data-ttu-id="b6cd2-191">Spænska (Spánn)</span><span class="sxs-lookup"><span data-stu-id="b6cd2-191">Spanish (Spain)</span></span> |
| <span data-ttu-id="b6cd2-192">es-MX</span><span class="sxs-lookup"><span data-stu-id="b6cd2-192">es-MX</span></span> | <span data-ttu-id="b6cd2-193">Spænska (Mexíkó)</span><span class="sxs-lookup"><span data-stu-id="b6cd2-193">Spanish (Mexico)</span></span> |
| <span data-ttu-id="b6cd2-194">fr-CA</span><span class="sxs-lookup"><span data-stu-id="b6cd2-194">fr-CA</span></span> | <span data-ttu-id="b6cd2-195">franska (Kanada)</span><span class="sxs-lookup"><span data-stu-id="b6cd2-195">French (Canada)</span></span> |
| <span data-ttu-id="b6cd2-196">fr-FR</span><span class="sxs-lookup"><span data-stu-id="b6cd2-196">fr-FR</span></span> | <span data-ttu-id="b6cd2-197">Franska (Frakkland)</span><span class="sxs-lookup"><span data-stu-id="b6cd2-197">French (France)</span></span> |
| <span data-ttu-id="b6cd2-198">it-IT</span><span class="sxs-lookup"><span data-stu-id="b6cd2-198">it-IT</span></span> | <span data-ttu-id="b6cd2-199">Ítalska (Ítalía)</span><span class="sxs-lookup"><span data-stu-id="b6cd2-199">Italian (Italy)</span></span> |
| <span data-ttu-id="b6cd2-200">nl-NL</span><span class="sxs-lookup"><span data-stu-id="b6cd2-200">nl-NL</span></span> | <span data-ttu-id="b6cd2-201">Hollenska (Holland)</span><span class="sxs-lookup"><span data-stu-id="b6cd2-201">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="b6cd2-202">pt-BR</span><span class="sxs-lookup"><span data-stu-id="b6cd2-202">pt-BR</span></span> | <span data-ttu-id="b6cd2-203">Portúgalska (Brasilía)</span><span class="sxs-lookup"><span data-stu-id="b6cd2-203">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="b6cd2-204">tr-TR</span><span class="sxs-lookup"><span data-stu-id="b6cd2-204">tr-TR</span></span> | <span data-ttu-id="b6cd2-205">Tyrkneska (Tyrkland)</span><span class="sxs-lookup"><span data-stu-id="b6cd2-205">Turkish (Turkey)</span></span> |
| <span data-ttu-id="b6cd2-206">zh-CN</span><span class="sxs-lookup"><span data-stu-id="b6cd2-206">zh-CN</span></span> | <span data-ttu-id="b6cd2-207">kínverska (einfölduð)</span><span class="sxs-lookup"><span data-stu-id="b6cd2-207">Chinese (Simplified)</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="b6cd2-208">Úrræðaleit</span><span class="sxs-lookup"><span data-stu-id="b6cd2-208">Troubleshooting</span></span>

<span data-ttu-id="b6cd2-209">Ef þú átt í vandræðum með að skrá þig inn í eða nota forritið Human Dynamics 365 Human Resources skaltu reyna að fylgja þessum leiðbeiningum úrræðaleitar.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-209">If you're having trouble signing into or using the Dynamics 365 Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="b6cd2-210">Ef þú átt enn í vandræðum eftir úrræðaleit skaltu hafa samband við notendaþjónustu.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-210">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="b6cd2-211">Frekari upplýsingar er að finna í [Fá stuðning](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="b6cd2-211">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="b6cd2-212">Ekki er hægta að skrá inn í forritið „Human Resources“ í Teams</span><span class="sxs-lookup"><span data-stu-id="b6cd2-212">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="b6cd2-213">Ef þú getur ekki skráð þig inn í forritið er hugsanlegt að reikningurinn sem þú notar til að skrá þig inn í Microsoft Teams sé ekki tengdur við starfsmannafærslu í Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-213">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="b6cd2-214">Hafa skal samskipti við kerfisstjóra til að tryggja að starfsmannafærslan sé rétt tengd.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-214">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="translations-dont-display-correctly"></a><span data-ttu-id="b6cd2-215">Þýðingar birtast ekki rétt</span><span class="sxs-lookup"><span data-stu-id="b6cd2-215">Translations don't display correctly</span></span>

<span data-ttu-id="b6cd2-216">Ef þýðingar birtast ekki eins og búist er við skal ganga úr skugga um tungumálið sem var valið í Teams passi við valið tungumál í **Valkostum notanda** í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-216">If translations don't display as expected, make sure the language you select in Teams matches the language selected in Human Resources **User options**.</span></span>

<span data-ttu-id="b6cd2-217">Í Teams skal skoða **Tungumál forrits** í **Stillingum**.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-217">In Teams, look at **App language** in **Settings**.</span></span>

![Teams stillingar](./media/hr-teams-leave-app-settings.png)

<span data-ttu-id="b6cd2-219">Í Human Resources skal velja **Stillingar** og síðan velja **Valkostir notanda**.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-219">In Human Resources, select **Settings** and then select **User options**.</span></span> <span data-ttu-id="b6cd2-220">Gangið úr skugga um að reiturinn **Tungumál** samsvari reitnum **Tungumál forrits** í Teams.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-220">Verify that the **Language** field matches the **App language** field in Teams.</span></span>

![Valkostir notenda mannauðs](./media/hr-teams-leave-app-user-options.png)

<span data-ttu-id="b6cd2-222">Láttu okkur vita ef vandamál vegna þýðinga er enn til staðar.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-222">If you still experience translation issues, let us know.</span></span> <span data-ttu-id="b6cd2-223">Frekari upplýsingar er að finna í [Fá stuðning fyrir Finance and Operations-forrit eða Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="b6cd2-223">For information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="b6cd2-224">Villa þegar leyfisbeiðnir eru samþykktar í forriti Human Resources í Teams</span><span class="sxs-lookup"><span data-stu-id="b6cd2-224">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="b6cd2-225">Ef villa kemur upp þegar verið er að reyna að samþykkja leyfisbeiðnir í Teams, skal prófa að fara í gegnum eftirfarandi villuleitarskref:</span><span class="sxs-lookup"><span data-stu-id="b6cd2-225">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="b6cd2-226">Gangið úr skugga um að reikningurinn sem er notaður til að skrá sig inn í Microsoft Teams sé sá sami og notaður er til að fá aðgang að Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-226">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="b6cd2-227">Vertu viss um að þú sért gildur samþykktaraðili fyrir beiðnina með því að athuga stillingar verkflæðis fyrir samþykkt leyfis.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-227">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="b6cd2-228">Frekari upplýsingar um verkflæði leyfisbeiðna er að finna í [Búa til verkflæði leyfisbeiðni](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="b6cd2-228">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a><span data-ttu-id="b6cd2-229">Samþykkisaðilar leyfis fá ekki spjallskilaboð úr Teams til að samþykkja leyfisbeiðnir</span><span class="sxs-lookup"><span data-stu-id="b6cd2-229">Leave approvers don't receive Teams chat messages to approve leave requests</span></span>

1. <span data-ttu-id="b6cd2-230">Gangið úr skugga um að tilkynningar séu virkar fyrir umhverfið og notandann.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-230">Ensure notifications are enabled for the environment and the user.</span></span> <span data-ttu-id="b6cd2-231">Frekari upplýsingar er að finna í [Virkja tilkynningar fyrir Human Resources-forritið í Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) og [Kveikja eða slökkva á tilkynningum Teams fyrir einstaka notendur](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span><span class="sxs-lookup"><span data-stu-id="b6cd2-231">For more information, see [Enable notifications for the Human Resources app in Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) and [Turn Teams notifications on or off for individual users](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span></span>

2. <span data-ttu-id="b6cd2-232">Gangið úr skugga um að notendur séu skráði inn í flipann **Spjall** með sömu innskráningarupplýsingunum og þeir nota til að samþykkja leyfisbeiðnir.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-232">Ensure users are signed into the **Chats** tab with the same credentials they use for approving leave requests.</span></span> <span data-ttu-id="b6cd2-233">Notið skilaboðin „skrá út“ og síðan „skrá inn“ til að skrá inn með réttum innskráningarupplýsingum.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-233">Use the messages "sign out" and then "sign in" to sign in with the correct credentials.</span></span>

3. <span data-ttu-id="b6cd2-234">Ef vandinn er enn til staðar skal athuga runuvinnslu kerfis í Business Events sem kerfisstjóri.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-234">If the issue persists, check the status of the Business Events system batch job as a system administrator.</span></span> <span data-ttu-id="b6cd2-235">Ef það er á biðstigi eða framkvæmdastigi skal athuga aftur eftir nokkrar mínútur.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-235">If it's in a waiting or executing stage, check back in a few minutes.</span></span> <span data-ttu-id="b6cd2-236">Ef staðan helst óbreytt skal skrá þjónustubeiðni svo teymið okkar geti hjálpað til við að leysa úr vandamálinu.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-236">If the status remains unchanged, log a support ticket so our team can help resolve the issue.</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="b6cd2-237">Þekkta aðgengisvandamál</span><span class="sxs-lookup"><span data-stu-id="b6cd2-237">Known accessibility issues</span></span>

<span data-ttu-id="b6cd2-238">Human Resources-forritið í Teams er með eftirfarandi aðgengisvandamál sem við vinnum að lagfæringum á í síðari útgáfum.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-238">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="b6cd2-239">Úthreyfing</span><span class="sxs-lookup"><span data-stu-id="b6cd2-239">Issue</span></span> | <span data-ttu-id="b6cd2-240">Hjáleið eða skýring</span><span class="sxs-lookup"><span data-stu-id="b6cd2-240">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="b6cd2-241">Ef 400% aðdráttur er notaður á skjáborði eru sumir aðgerðahnappar ekki sýnilegir.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-241">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="b6cd2-242">Mælt er með því að notað sé stækkunargler þar til við styðjum þennan aðdrátt.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-242">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="b6cd2-243">Á flipanum **Frí** tilkynnir upplestur hnappaaðgerð þegar hausinn hnitanetsins er lesinn fyrir fríið.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-243">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="b6cd2-244">Haus og einingar innan hnitanetsins eru flokkaðar eftir árum og eru samanfellanlegar.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-244">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="b6cd2-245">Upplestur skilur þetta sem aðgerðarhlut, sem það er ekki.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-245">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="b6cd2-246">Á flipanum **Frí** er aukaleg strokhreyfing þegar verið er að fletta að **Ástæðukóði** í nýrri beiðni.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-246">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="b6cd2-247">Engin falin stjórnun er til staðar sem storkufletting er að reyna að ná til.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-247">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="b6cd2-248">Á flipanum **Frí**, ef strokið á meðan dagatalið er opið, er endað utan stýringar í stað upphafs nýrrar beiðni eða þegar beiðni er breytt.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-248">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="b6cd2-249">Þegar komið er að **Fara á daginn í dag** er það síðasti hlutinn og strokið er í öfuga átt til að komast aftur efst.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-249">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="b6cd2-250">Á flipanum **Spjall** er farið aftur á toppinn þegar dagsetningin er slegin inn á meðan verið er að nota hjálpartækið eða lyklaborðið.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-250">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="b6cd2-251">Flipi þar til þú nærð innsláttarsvæðinu aftur.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-251">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="b6cd2-252">Tilkynning um persónuvernd</span><span class="sxs-lookup"><span data-stu-id="b6cd2-252">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="b6cd2-253">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="b6cd2-253">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="b6cd2-254">Með Dynamics 365 Human Resources þjarkanum í Microsoft Teams er texti notanda greindur til að skilja undirliggjandi fyrirspurn/ásetning.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-254">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="b6cd2-255">Inntak notanda á borð við „Leita í Contoso-reikningi“ er flutt í eina af Cognitive Service hjá Microsoft sem kallast LUIS (Language Understanding Intelligent Service).</span><span class="sxs-lookup"><span data-stu-id="b6cd2-255">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="b6cd2-256">Lesa meira um LUIS  [hér](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="b6cd2-256">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="b6cd2-257">LUIS-þjónustan ræður úr eða skilur ásetning notanda (í þessu tilviki er ætlunin að finna upplýsingar) og markeiningu (í þessu tilviki er tilgreinda einingin reikningur sem heitir Contoso).</span><span class="sxs-lookup"><span data-stu-id="b6cd2-257">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="b6cd2-258">Þessar upplýsingar eru svo sendar í Microsoft [Azure þjarkaramma](https://azure.microsoft.com/services/bot-service/) sem vinnur með gögn úr Dynamics 365 Human Resources og sækir æskilegar upplýsingum fyrir fyrirspurn notanda.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-258">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="b6cd2-259">Með því að setja upp og leyfa aðgang að þjarkanum samþykkir þú að leyfa LUIS-þjónustunni og Azure þjarkaramma að vinna úr ásetningi á bak við fyrirspurn, sem leiðir til betri notandaupplifunar.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-259">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="b6cd2-260">LUIS-þjónustan og Azure þjarkaramminn kunna að hafa mismikið samræmi samanborið við Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-260">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="b6cd2-261">LUIS-þjónustan hefur aðeins aðgang að fyrirspurnum notenda og er ekki hönnuð til að tengjast við Dynamics 365 Human Resources gögn eða reikning. Notandi Dynamics 365 Human Resources þjarkans gæti fært inn fyrirspurn sem inniheldur gögn viðskiptavinar, persónuleg gögn eða önnur gögn og slíkt fyrirspurnarefni gæti verið sent til LUIS-þjónustunnar og Azure þjarkarammans.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-261">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="b6cd2-262">Innihald fyrirspurna og skilaboða notanda er vistað í LUIS-kerfi í að hámarki 30 daga, er dulkóðað þegar ekki í notkun og er ekki notað fyrir þjálfun eða endurbætur á þjónustu.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-262">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="b6cd2-263">Lestu meira um Cognitive Services  [hér](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="b6cd2-263">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="b6cd2-264">Til að stjórna stjórnandastillingum fyrir forrit í Microsoft Teams er farið í [Microsoft Teams stjórnendamiðstöð](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="b6cd2-264">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="b6cd2-265">Microsoft Teams, hnitanet Azure-tilviks og Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b6cd2-265">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="b6cd2-266">Þegar Dynamics 365 Human Resources-forritið er notað í Microsoft Teams geta tiltekin gögn um viðskiptavini flætt út fyrir landsvæðið þar sem biðlari Human Resources þjónustunnar er notaður.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-266">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="b6cd2-267">Dynamics 365 Human Resources sendir upplýsingar um leyfisbeiðni og verkflæðisverk til Microsoft Azure tilviks hnitanets og Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-267">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="b6cd2-268">Þessi gögn má geyma í Microsoft Azure Event Grid í allt að sólarhring og verða unnin í Bandaríkjunum, þau er dulkóðuð í flutningi og í hvíld, og eru ekki notuð af Microsoft eða meðhöndlunaraðilum fyrir þjálfun eða þjónustuúrbætur.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-268">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="b6cd2-269">Til að skilja hvar gögnin þín eru geymd í Teams skaltu skoða: [Staðsetning gagna í Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="b6cd2-269">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>

<span data-ttu-id="b6cd2-270">Í samskiptum við spjallarann í forriti Human Resources, er hægt að geyma innihald samtalsins í Azure Cosmos DB og flytja það yfir í Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-270">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="b6cd2-271">Þessi gögn má geyma í Azure Cosmos DB í allt að sólarhring og kunna að vera meðhöndluð utan staðsetningarinnar þar sem Human Resources-þjónusta leigjandans er uppsett, þau er dulkóðuð í flutningi og í hvíld, og eru ekki notuð af Microsoft eða meðhöndlunaraðilum fyrir þjálfun eða þjónustuúrbætur.</span><span class="sxs-lookup"><span data-stu-id="b6cd2-271">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="b6cd2-272">Til að skilja hvar gögnin þín eru geymd í Teams skaltu skoða: [Staðsetning gagna í Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="b6cd2-272">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>
 
<span data-ttu-id="b6cd2-273">Til að takmarka aðgang að Human Resources í Microsoft Teams fyrir fyrirtækið þitt eða notendur innan fyrirtækisins skal skoða [Stjórna reglum um forritsheimildir í Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="b6cd2-273">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="b6cd2-274">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="b6cd2-274">See also</span></span>

[<span data-ttu-id="b6cd2-275">Sækja og setja upp Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b6cd2-275">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="b6cd2-276">Microsoft Teams hjálparmiðstöð</span><span class="sxs-lookup"><span data-stu-id="b6cd2-276">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="b6cd2-277">Forritið „Human Resources“ í Teams</span><span class="sxs-lookup"><span data-stu-id="b6cd2-277">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]