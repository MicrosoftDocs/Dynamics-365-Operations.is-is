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
ms.openlocfilehash: 72fa3309b77717d0291b8b6828ed5bc4c65e95ab
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790573"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="2c2d5-103">Stjórna leyfisbeiðnum í Teams</span><span class="sxs-lookup"><span data-stu-id="2c2d5-103">Manage leave requests in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="2c2d5-104">Dynamics 365 Human Resources -forritið í Microsoft Teams gerir þér kleift að biðja um frí og skoða upplýsingar um stöðu frítíma í Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-104">The Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="2c2d5-105">Hægt er að eiga samskipti við þjarka til að óska eftir upplýsingum og byrja leyfisbeiðni.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="2c2d5-106">Finna má ítarlegri upplýsingar á flipanum **Frí**.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="2c2d5-107">Einnig er hægt að senda fólki upplýsingar um væntanlegan frítíma í hópum og spjalli utan Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-107">You can also send people information about your upcoming time off in Teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="2c2d5-108">Setja upp forritið</span><span class="sxs-lookup"><span data-stu-id="2c2d5-108">Install the app</span></span>

<span data-ttu-id="2c2d5-109">Hægt er að finna Dynamics 365 Human Resources forritið í Teams versluninni.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-109">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="2c2d5-110">Í Microsoft Teams skal velja sporbauginn.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-110">In Microsoft Teams, select the ellipses.</span></span>

   ![Sporbaugur fyrir Human Resources Teams-forrit fyrir leyfi](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="2c2d5-112">Leitið að Dynamics 365 Human Resources og veljið síðan reitinn **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![Human Resources-spjald fyrir Human Resources Teams-forrit fyrir leyfi](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="2c2d5-114">Veljið hnappinn **Bæta við** til að setja upp forritið.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-114">Select the **Add** button to install the app.</span></span>

   ![Uppsetning Human Resources Teams-forrits fyrir leyfi](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="2c2d5-116">Ef forritið skráir þig ekki sjálfkrafa inn skaltu velja flipann **Stillingar** til að skrá þig inn.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Stillingaflipi Human Resources Teams-forrits fyrir leyfi](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="2c2d5-118">Ef þú sérð ekki innskráningarglugga skaltu athuga vafrastillingarnar þínar til að leyfa sprettiglugga.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="2c2d5-119">Ef þú hefur aðgang að fleiri en einu tilviki af Human Resources er hægt að velja hvaða umhverfi á að tengja við á flipanum **Stillingar**.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="2c2d5-120">Forritið styður nú öryggishlutverk kerfisstjóra.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="2c2d5-121">Nota þjarkann</span><span class="sxs-lookup"><span data-stu-id="2c2d5-121">Use the bot</span></span>

<span data-ttu-id="2c2d5-122">Þegar forritið hefur verið sett upp birtast boð með upplýsingar um þær aðgerðir sem þjarkinn getur gripið til.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Opnunarkveðja Human Resources Teams-þjarkaforrits fyrir leyfi](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="2c2d5-124">Hugsanlega þarf að skrá sig inn við fyrstu samskipti við þjarkann.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="2c2d5-125">Ef þú sérð ekki innskráningarglugga skaltu athuga vafrastillingarnar þínar til að leyfa sprettiglugga.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="2c2d5-126">Hægt er að spyrja þjarkann um að:</span><span class="sxs-lookup"><span data-stu-id="2c2d5-126">You can ask the bot to:</span></span>

- <span data-ttu-id="2c2d5-127">Hefja leyfisbeiðni fyrir notanda.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-127">Start a leave request for you.</span></span>

  ![Hefja beiðni um leyfi í Teams spjalli](./media/hr-teams-leave-app-initiate.png)

- <span data-ttu-id="2c2d5-129">Spjallarinn mun fylla út leyfibeiðni fyrir þig.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-129">The chat bot will populate a leave request for you.</span></span> <span data-ttu-id="2c2d5-130">Veljið **Biðja um frí** til að biðja um og breyta upplýsingum um beiðnina.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-130">Select **Request time off** and edit the details for your request.</span></span>

  ![Breyta upplýsingum leyfisbeiðni](./media/hr-teams-leave-app-details.png)

- <span data-ttu-id="2c2d5-132">Þegar búið er að breyta upplýsingunum um leyfisbeiðni skal velja **Senda** til að senda þær til samþykkis.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-132">When you're done editing your leave request details, select **Submit** to submit it for approval.</span></span>

  ![Staðfesta leyfisbeiðni](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="2c2d5-134">Stjórna leyfi í Teams</span><span class="sxs-lookup"><span data-stu-id="2c2d5-134">Manage your leave in Teams</span></span>

<span data-ttu-id="2c2d5-135">Flipinn **Frí** býður upp á skoðun:</span><span class="sxs-lookup"><span data-stu-id="2c2d5-135">The **Time off** tab allows you to view:</span></span> 

- <span data-ttu-id="2c2d5-136">Stöðuupplýsingar fyrir hverjar leyfisgerðir sem þú ert skráð(ur) í</span><span class="sxs-lookup"><span data-stu-id="2c2d5-136">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="2c2d5-137">Næstu leyfisbeiðnir</span><span class="sxs-lookup"><span data-stu-id="2c2d5-137">Upcoming leave requests</span></span>

- <span data-ttu-id="2c2d5-138">Fríbeiðnir</span><span class="sxs-lookup"><span data-stu-id="2c2d5-138">Time-off requests</span></span>

- <span data-ttu-id="2c2d5-139">Drög að leyfisbeiðnum</span><span class="sxs-lookup"><span data-stu-id="2c2d5-139">Draft leave requests</span></span>

![Fríflipi fyrir fríforrit Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="2c2d5-141">Búa til nýja beiðni</span><span class="sxs-lookup"><span data-stu-id="2c2d5-141">Create a new request</span></span>

1. <span data-ttu-id="2c2d5-142">Til að stofna nýja leyfisbeiðni skal velja **Ný beiðni**.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-142">To create a new leave request, select **New request**.</span></span>

   ![Ný beiðni fyrir Human Resources Teams-forrit fyrir leyfi](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="2c2d5-144">Sláðu inn daginn eða dagana þar sem þú vilt taka frí og veldu svo **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-144">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Bæta við fríi Human Resources Teams-forriti fyrir leyfi](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="2c2d5-146">Slá inn ástæðukóða, ef við á.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-146">If applicable, enter a reason code.</span></span> <span data-ttu-id="2c2d5-147">Einnig skal færa inn athugasemdir og bæta við viðhengjum.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-147">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="2c2d5-148">Þegar búið er að færa inn upplýsingar skal slá inn **Senda** til að senda hana til samþykkis.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-148">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="2c2d5-149">Einnig er hægt að slá inn **Vista sem drög** til að gera þetta síðar.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-149">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="2c2d5-150">Stjórna dragabeiðnum</span><span class="sxs-lookup"><span data-stu-id="2c2d5-150">Manage draft requests</span></span>

1. <span data-ttu-id="2c2d5-151">Veljið flipann **Drög**.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-151">Select the **Drafts** tab.</span></span>

   ![Dragaflipi í Human Resources Teams-forriti fyrir leyfi](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="2c2d5-153">Veldu blýantinn til að breyta beiðninni eða ruslið til að eyða henni.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-153">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="2c2d5-154">Gerið nauðsynlegar breytingar.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-154">Make any necessary changes.</span></span> <span data-ttu-id="2c2d5-155">Þegar búið er að færa inn upplýsingar skal slá inn **Senda** til að senda hana til samþykkis.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-155">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="2c2d5-156">Einnig er hægt að velja **Vista sem drög** til að gera þetta síðar.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-156">You can also select **Save as draft** to come back to it later.</span></span>

   ![Breyta drögum í Human Resources Teams-forriti fyrir leyfi](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="2c2d5-158">Bregðast við tilkynningum Teams</span><span class="sxs-lookup"><span data-stu-id="2c2d5-158">Respond to Teams notifications</span></span>

<span data-ttu-id="2c2d5-159">Þegar þú eða starfskraftur sem þú ert samþykktaraðili fyrir sendir beiðni um leyfi fyrir færðu senda tilkynningu í Human Resources forritinu í Teams.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-159">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="2c2d5-160">Hægt er að velja tilkynninguna til að skoða hana.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-160">You can select the notification to view it.</span></span> <span data-ttu-id="2c2d5-161">Tilkynningar birtast einnig á svæðinu **Spjall**.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-161">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="2c2d5-162">Ef notandi er samþykkjandi er hægt að velja **Samþykkja** eða **Neita** í tilkynningunni.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-162">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="2c2d5-163">Einnig er hægt að búa til valfrjáls skilaboð.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-163">You can also provide an optional message.</span></span>

![Senda beiðni um tilkynningar í forritinu Human Resources Teams](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="2c2d5-165">Senda upplýsingar um væntanlegt frí til samstarfsfólks</span><span class="sxs-lookup"><span data-stu-id="2c2d5-165">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="2c2d5-166">Eftir að Human Resources er sett upp fyrir Teams er auðveldlega hægt að senda upplýsingar um væntanlegt frí til samstarfsfólks í hópum og spjalli.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-166">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="2c2d5-167">Í hópi eða spjalli í Teams skal velja hnapp Human Resources fyrir neðan spjallgluggann.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-167">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![Hnappur Human Resources fyrir neðan spjallglugga](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="2c2d5-169">Veljið leyfisbeiðnina sem á að deila.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-169">Select the leave request you want to share.</span></span> <span data-ttu-id="2c2d5-170">Ef óskað er eftir að deila drögum að leyfisbeiðni skal byrja á því að velja **Drög**.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-170">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![Velja beiðni um væntanlegt frí til að deila](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="2c2d5-172">Leyfisbeiðnin mun birtast í spjallinu.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-172">Your leave request will display in the chat.</span></span>

![Leyfisbeiðnispjald Human Resources](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="2c2d5-174">Ef drög að beiðni var deilt mun þau birtast sem drög:</span><span class="sxs-lookup"><span data-stu-id="2c2d5-174">If you shared a draft request, it will display as a draft:</span></span>

![Drög að leyfisbeiðnispjaldi Human Resources](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="2c2d5-176">Skoða frídagatal teymisins</span><span class="sxs-lookup"><span data-stu-id="2c2d5-176">View your team's leave calendar</span></span>

<span data-ttu-id="2c2d5-177">Ef þú ert yfirmaður með beina undirmenn getur þú skoðað samþykkt frí hópsins þíns og frí í bið.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-177">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="2c2d5-178">Í forritinu „Human Resources“ í Teams skal velja **Frí**.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-178">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="2c2d5-179">Veldu **Team dagatal**.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-179">Select **Team calendar**.</span></span> <span data-ttu-id="2c2d5-180">Dagatalið birtir samþykkt frí og frí í bið fyrir beina undirmenn þína.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-180">The calendar displays your direct reports' approved and pending time off.</span></span>

   ![Skoða dagatal í Human Resources Teams-forriti](./media/hr-teams-leave-app-view-calendar.png)

   > [!NOTE]
   > <span data-ttu-id="2c2d5-182">Ef ekki er hægt að sjá hópdagatalið skal biðja kerfisstjóra um að virkja það.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-182">If you can't see the team calendar, ask your admin to enable it.</span></span> <span data-ttu-id="2c2d5-183">Frekari upplýsingar eru í [Setja upp](hr-admin-teams-leave-app.md#install-and-setup).</span><span class="sxs-lookup"><span data-stu-id="2c2d5-183">For more information, see [Install and setup](hr-admin-teams-leave-app.md#install-and-setup).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="2c2d5-184">Studd tungumál</span><span class="sxs-lookup"><span data-stu-id="2c2d5-184">Supported languages</span></span>

<span data-ttu-id="2c2d5-185"> Forritið Dynamics 365 Human Resources í Teams styður eftirfarandi tungumál:</span><span class="sxs-lookup"><span data-stu-id="2c2d5-185">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="2c2d5-186">Landstaðalskenni</span><span class="sxs-lookup"><span data-stu-id="2c2d5-186">Locale ID</span></span> | <span data-ttu-id="2c2d5-187">Tungumál</span><span class="sxs-lookup"><span data-stu-id="2c2d5-187">Language</span></span> |
| --- | --- |
| <span data-ttu-id="2c2d5-188">de-DE</span><span class="sxs-lookup"><span data-stu-id="2c2d5-188">de-DE</span></span> | <span data-ttu-id="2c2d5-189">Þýska (Þýskaland)</span><span class="sxs-lookup"><span data-stu-id="2c2d5-189">German (Germany)</span></span> |
| <span data-ttu-id="2c2d5-190">es-ES</span><span class="sxs-lookup"><span data-stu-id="2c2d5-190">es-ES</span></span> | <span data-ttu-id="2c2d5-191">Spænska (Spánn)</span><span class="sxs-lookup"><span data-stu-id="2c2d5-191">Spanish (Spain)</span></span> |
| <span data-ttu-id="2c2d5-192">es-MX</span><span class="sxs-lookup"><span data-stu-id="2c2d5-192">es-MX</span></span> | <span data-ttu-id="2c2d5-193">Spænska (Mexíkó)</span><span class="sxs-lookup"><span data-stu-id="2c2d5-193">Spanish (Mexico)</span></span> |
| <span data-ttu-id="2c2d5-194">fr-CA</span><span class="sxs-lookup"><span data-stu-id="2c2d5-194">fr-CA</span></span> | <span data-ttu-id="2c2d5-195">franska (Kanada)</span><span class="sxs-lookup"><span data-stu-id="2c2d5-195">French (Canada)</span></span> |
| <span data-ttu-id="2c2d5-196">fr-FR</span><span class="sxs-lookup"><span data-stu-id="2c2d5-196">fr-FR</span></span> | <span data-ttu-id="2c2d5-197">Franska (Frakkland)</span><span class="sxs-lookup"><span data-stu-id="2c2d5-197">French (France)</span></span> |
| <span data-ttu-id="2c2d5-198">it-IT</span><span class="sxs-lookup"><span data-stu-id="2c2d5-198">it-IT</span></span> | <span data-ttu-id="2c2d5-199">Ítalska (Ítalía)</span><span class="sxs-lookup"><span data-stu-id="2c2d5-199">Italian (Italy)</span></span> |
| <span data-ttu-id="2c2d5-200">nl-NL</span><span class="sxs-lookup"><span data-stu-id="2c2d5-200">nl-NL</span></span> | <span data-ttu-id="2c2d5-201">Hollenska (Holland)</span><span class="sxs-lookup"><span data-stu-id="2c2d5-201">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="2c2d5-202">pt-BR</span><span class="sxs-lookup"><span data-stu-id="2c2d5-202">pt-BR</span></span> | <span data-ttu-id="2c2d5-203">Portúgalska (Brasilía)</span><span class="sxs-lookup"><span data-stu-id="2c2d5-203">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="2c2d5-204">tr-TR</span><span class="sxs-lookup"><span data-stu-id="2c2d5-204">tr-TR</span></span> | <span data-ttu-id="2c2d5-205">Tyrkneska (Tyrkland)</span><span class="sxs-lookup"><span data-stu-id="2c2d5-205">Turkish (Turkey)</span></span> |
| <span data-ttu-id="2c2d5-206">zh-CN</span><span class="sxs-lookup"><span data-stu-id="2c2d5-206">zh-CN</span></span> | <span data-ttu-id="2c2d5-207">kínverska (einfölduð)</span><span class="sxs-lookup"><span data-stu-id="2c2d5-207">Chinese (Simplified)</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="2c2d5-208">Úrræðaleit</span><span class="sxs-lookup"><span data-stu-id="2c2d5-208">Troubleshooting</span></span>

<span data-ttu-id="2c2d5-209">Ef þú átt í vandræðum með að skrá þig inn í eða nota forritið Human Dynamics 365 Human Resources skaltu reyna að fylgja þessum leiðbeiningum úrræðaleitar.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-209">If you're having trouble signing into or using the Dynamics 365 Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="2c2d5-210">Ef þú átt enn í vandræðum eftir úrræðaleit skaltu hafa samband við notendaþjónustu.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-210">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="2c2d5-211">Frekari upplýsingar er að finna í [Fá stuðning](hr-admin-troubleshooting-support.md).</span><span class="sxs-lookup"><span data-stu-id="2c2d5-211">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="2c2d5-212">Ekki er hægta að skrá inn í forritið „Human Resources“ í Teams</span><span class="sxs-lookup"><span data-stu-id="2c2d5-212">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="2c2d5-213">Ef þú getur ekki skráð þig inn í forritið er hugsanlegt að reikningurinn sem þú notar til að skrá þig inn í Microsoft Teams sé ekki tengdur við starfsmannafærslu í Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-213">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="2c2d5-214">Hafa skal samskipti við kerfisstjóra til að tryggja að starfsmannafærslan sé rétt tengd.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-214">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="translations-dont-display-correctly"></a><span data-ttu-id="2c2d5-215">Þýðingar birtast ekki rétt</span><span class="sxs-lookup"><span data-stu-id="2c2d5-215">Translations don't display correctly</span></span>

<span data-ttu-id="2c2d5-216">Ef þýðingar birtast ekki eins og búist er við skal ganga úr skugga um tungumálið sem var valið í Teams passi við valið tungumál í **Valkostum notanda** í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-216">If translations don't display as expected, make sure the language you select in Teams matches the language selected in Human Resources **User options**.</span></span>

<span data-ttu-id="2c2d5-217">Í Teams skal skoða **Tungumál forrits** í **Stillingum**.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-217">In Teams, look at **App language** in **Settings**.</span></span>

![Teams stillingar](./media/hr-teams-leave-app-settings.png)

<span data-ttu-id="2c2d5-219">Í Human Resources skal velja **Stillingar** og síðan velja **Valkostir notanda**.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-219">In Human Resources, select **Settings** and then select **User options**.</span></span> <span data-ttu-id="2c2d5-220">Gangið úr skugga um að reiturinn **Tungumál** samsvari reitnum **Tungumál forrits** í Teams.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-220">Verify that the **Language** field matches the **App language** field in Teams.</span></span>

![Valkostir notenda mannauðs](./media/hr-teams-leave-app-user-options.png)

<span data-ttu-id="2c2d5-222">Láttu okkur vita ef vandamál vegna þýðinga er enn til staðar.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-222">If you still experience translation issues, let us know.</span></span> <span data-ttu-id="2c2d5-223">Frekari upplýsingar er að finna í [Fá stuðning fyrir Finance and Operations-forrit eða Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs-support?toc=/dynamics365/human-resources/toc.json).</span><span class="sxs-lookup"><span data-stu-id="2c2d5-223">For information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs-support?toc=/dynamics365/human-resources/toc.json).</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="2c2d5-224">Villa þegar leyfisbeiðnir eru samþykktar í forriti Human Resources í Teams</span><span class="sxs-lookup"><span data-stu-id="2c2d5-224">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="2c2d5-225">Ef villa kemur upp þegar verið er að reyna að samþykkja leyfisbeiðnir í Teams, skal prófa að fara í gegnum eftirfarandi villuleitarskref:</span><span class="sxs-lookup"><span data-stu-id="2c2d5-225">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="2c2d5-226">Gangið úr skugga um að reikningurinn sem er notaður til að skrá sig inn í Microsoft Teams sé sá sami og notaður er til að fá aðgang að Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-226">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="2c2d5-227">Vertu viss um að þú sért gildur samþykktaraðili fyrir beiðnina með því að athuga stillingar verkflæðis fyrir samþykkt leyfis.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-227">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="2c2d5-228">Frekari upplýsingar um verkflæði leyfisbeiðna er að finna í [Búa til verkflæði leyfisbeiðni](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="2c2d5-228">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="2c2d5-229">Þekkta aðgengisvandamál</span><span class="sxs-lookup"><span data-stu-id="2c2d5-229">Known accessibility issues</span></span>

<span data-ttu-id="2c2d5-230">Human Resources-forritið í Teams er með eftirfarandi aðgengisvandamál sem við vinnum að lagfæringum á í síðari útgáfum.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-230">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="2c2d5-231">Úthreyfing</span><span class="sxs-lookup"><span data-stu-id="2c2d5-231">Issue</span></span> | <span data-ttu-id="2c2d5-232">Hjáleið eða skýring</span><span class="sxs-lookup"><span data-stu-id="2c2d5-232">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="2c2d5-233">Ef 400% aðdráttur er notaður á skjáborði eru sumir aðgerðahnappar ekki sýnilegir.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-233">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="2c2d5-234">Mælt er með því að notað sé stækkunargler þar til við styðjum þennan aðdrátt.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-234">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="2c2d5-235">Á flipanum **Frí** tilkynnir upplestur hnappaaðgerð þegar hausinn hnitanetsins er lesinn fyrir fríið.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-235">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="2c2d5-236">Haus og einingar innan hnitanetsins eru flokkaðar eftir árum og eru samanfellanlegar.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-236">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="2c2d5-237">Upplestur skilur þetta sem aðgerðarhlut, sem það er ekki.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-237">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="2c2d5-238">Á flipanum **Frí** er aukaleg strokhreyfing þegar verið er að fletta að **Ástæðukóði** í nýrri beiðni.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-238">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="2c2d5-239">Engin falin stjórnun er til staðar sem storkufletting er að reyna að ná til.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-239">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="2c2d5-240">Á flipanum **Frí**, ef strokið á meðan dagatalið er opið, er endað utan stýringar í stað upphafs nýrrar beiðni eða þegar beiðni er breytt.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-240">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="2c2d5-241">Þegar komið er að **Fara á daginn í dag** er það síðasti hlutinn og strokið er í öfuga átt til að komast aftur efst.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-241">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="2c2d5-242">Á flipanum **Spjall** er farið aftur á toppinn þegar dagsetningin er slegin inn á meðan verið er að nota hjálpartækið eða lyklaborðið.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-242">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="2c2d5-243">Flipi þar til þú nærð innsláttarsvæðinu aftur.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-243">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="2c2d5-244">Tilkynning um persónuvernd</span><span class="sxs-lookup"><span data-stu-id="2c2d5-244">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="2c2d5-245">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="2c2d5-245">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="2c2d5-246">Með Dynamics 365 Human Resources þjarkanum í Microsoft Teams er texti notanda greindur til að skilja undirliggjandi fyrirspurn/ásetning.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-246">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="2c2d5-247">Inntak notanda á borð við „Leita í contoso reikningi“ er flutt í eina af Cognitive Service hjá Microsoft sem kallast LUIS (Language Understanding Intelligent Service).</span><span class="sxs-lookup"><span data-stu-id="2c2d5-247">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="2c2d5-248">Lesa meira um LUIS  [hér](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="2c2d5-248">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="2c2d5-249">LUIS-þjónustan ræður úr eða skilur ásetning notanda (í þessu tilviki er ætlunin að finna upplýsingar) og markeiningu (í þessu tilviki er tilgreinda einingin reikningur sem heitir Contoso).</span><span class="sxs-lookup"><span data-stu-id="2c2d5-249">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="2c2d5-250">Þessar upplýsingar eru svo sendar í Microsoft [Azure þjarkaramma](https://azure.microsoft.com/services/bot-service/) sem vinnur með gögn úr Dynamics 365 Human Resources og sækir æskilegar upplýsingum fyrir fyrirspurn notanda.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-250">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="2c2d5-251">Með því að setja upp og leyfa aðgang að þjarkanum samþykkir þú að leyfa LUIS-þjónustunni og Azure þjarkaramma að vinna úr ásetningi á bak við fyrirspurn, sem leiðir til betri notandaupplifunar.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-251">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="2c2d5-252">LUIS-þjónustan og Azure þjarkaramminn kunna að hafa mismikið samræmi samanborið við Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-252">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="2c2d5-253">LUIS-þjónustan hefur aðeins aðgang að fyrirspurnum notenda og er ekki hönnuð til að tengjast við Dynamics 365 Human Resources gögn eða reikning. Notandi Dynamics 365 Human Resources þjarkans gæti fært inn fyrirspurn sem inniheldur gögn viðskiptavinar, persónuleg gögn eða önnur gögn og slíkt fyrirspurnarefni gæti verið sent til LUIS-þjónustunnar og Azure þjarkarammans.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-253">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="2c2d5-254">Innihald fyrirspurna og skilaboða notanda er vistað í LUIS-kerfi í að hámarki 30 daga, er dulkóðað þegar ekki í notkun og er ekki notað fyrir þjálfun eða endurbætur á þjónustu.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-254">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="2c2d5-255">Lestu meira um Cognitive Services  [hér](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="2c2d5-255">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="2c2d5-256">Til að stjórna stjórnandastillingum fyrir forrit í Microsoft Teams er farið í [Microsoft Teams stjórnendamiðstöð](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="2c2d5-256">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="2c2d5-257">Microsoft Teams, hnitanet Azure-tilviks og Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="2c2d5-257">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="2c2d5-258">Þegar Dynamics 365 Human Resources-forritið er notað í Microsoft Teams geta tiltekin gögn um viðskiptavini flætt út fyrir landsvæðið þar sem biðlari Human Resources þjónustunnar er notaður.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-258">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="2c2d5-259">Dynamics 365 Human Resources sendir upplýsingar um leyfisbeiðni og verkflæðisverk til Microsoft Azure tilviks hnitanets og Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-259">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="2c2d5-260">Þessi gögn má geyma í Microsoft Azure Event Grid í allt að sólarhring og verða unnin í Bandaríkjunum, þau er dulkóðuð í flutningi og í hvíld, og eru ekki notuð af Microsoft eða meðhöndlunaraðilum fyrir þjálfun eða þjónustuúrbætur.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-260">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="2c2d5-261">Til að skilja hvar gögnin þín eru geymd í Teams skaltu skoða: [Staðsetning gagna í Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="2c2d5-261">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="2c2d5-262">Í samskiptum við spjallarann í forriti Human Resources, er hægt að geyma innihald samtalsins í Azure Cosmos DB og flytja það yfir í Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-262">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="2c2d5-263">Þessi gögn má geyma í Azure Cosmos DB í allt að sólarhring og kunna að vera meðhöndluð utan staðsetningarinnar þar sem Human Resources-þjónusta leigjandans er uppsett, þau er dulkóðuð í flutningi og í hvíld, og eru ekki notuð af Microsoft eða meðhöndlunaraðilum fyrir þjálfun eða þjónustuúrbætur.</span><span class="sxs-lookup"><span data-stu-id="2c2d5-263">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="2c2d5-264">Til að skilja hvar gögnin þín eru geymd í Teams skaltu skoða: [Staðsetning gagna í Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="2c2d5-264">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="2c2d5-265">Til að takmarka aðgang að Human Resources í Microsoft Teams fyrir fyrirtækið þitt eða notendur innan fyrirtækisins skal skoða [Stjórna reglum um forritsheimildir í Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="2c2d5-265">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="2c2d5-266">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="2c2d5-266">See also</span></span>

[<span data-ttu-id="2c2d5-267">Sækja og setja upp Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="2c2d5-267">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="2c2d5-268">Microsoft Teams hjálparmiðstöð</span><span class="sxs-lookup"><span data-stu-id="2c2d5-268">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="2c2d5-269">Forritið „Human Resources“ í Teams</span><span class="sxs-lookup"><span data-stu-id="2c2d5-269">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]