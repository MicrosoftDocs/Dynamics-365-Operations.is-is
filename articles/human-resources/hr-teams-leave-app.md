---
title: Stjórna leyfisbeiðnum í Teams
description: Þetta efnisatriði sýnir hvernig á að biðja um frí í Dynamics 365 Human Resources forritinu í Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: d24c257054578282f1a2eafa050094194a358aa0
ms.sourcegitcommit: 369639cd92e03fe792ed9d61a329d842aafa052f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/29/2020
ms.locfileid: "4419110"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="1a05f-103">Stjórna leyfisbeiðnum í Teams</span><span class="sxs-lookup"><span data-stu-id="1a05f-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="1a05f-104">Microsoft Dynamics 365 Human Resources -forritið í Microsoft Teams gerir þér kleift að biðja um frí og skoða upplýsingar um stöðu frítíma í Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="1a05f-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="1a05f-105">Hægt er að eiga samskipti við þjarka til að óska eftir upplýsingum og byrja leyfisbeiðni.</span><span class="sxs-lookup"><span data-stu-id="1a05f-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="1a05f-106">Finna má ítarlegri upplýsingar á flipanum **Frí**.</span><span class="sxs-lookup"><span data-stu-id="1a05f-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="1a05f-107">Einnig er hægt að senda fólki upplýsingar um væntanlegan frítíma í hópum og spjalli utan Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1a05f-107">You can also send people information about your upcoming time off in teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="1a05f-108">Setja upp forritið</span><span class="sxs-lookup"><span data-stu-id="1a05f-108">Install the app</span></span>

<span data-ttu-id="1a05f-109">Hægt er að finna forritið Human Resources í Teams versluninni.</span><span class="sxs-lookup"><span data-stu-id="1a05f-109">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="1a05f-110">Í Microsoft Teams skal velja sporbauginn.</span><span class="sxs-lookup"><span data-stu-id="1a05f-110">In Microsoft Teams, select the ellipses.</span></span>

   ![Sporbaugur fyrir Human Resources Teams-forrit fyrir leyfi](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="1a05f-112">Leitið að Dynamics 365 Human Resources og veljið síðan reitinn **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="1a05f-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![Human Resources-spjald fyrir Human Resources Teams-forrit fyrir leyfi](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="1a05f-114">Veljið hnappinn **Bæta við** til að setja upp forritið.</span><span class="sxs-lookup"><span data-stu-id="1a05f-114">Select the **Add** button to install the app.</span></span>

   ![Uppsetning Human Resources Teams-forrits fyrir leyfi](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="1a05f-116">Ef forritið skráir þig ekki sjálfkrafa inn skaltu velja flipann **Stillingar** til að skrá þig inn.</span><span class="sxs-lookup"><span data-stu-id="1a05f-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Stillingaflipi Human Resources Teams-forrits fyrir leyfi](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="1a05f-118">Ef þú sérð ekki innskráningarglugga skaltu athuga vafrastillingarnar þínar til að leyfa sprettiglugga.</span><span class="sxs-lookup"><span data-stu-id="1a05f-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="1a05f-119">Ef þú hefur aðgang að fleiri en einu tilviki af Human Resources er hægt að velja hvaða umhverfi á að tengja við á flipanum **Stillingar**.</span><span class="sxs-lookup"><span data-stu-id="1a05f-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="1a05f-120">Forritið styður nú öryggishlutverk kerfisstjóra.</span><span class="sxs-lookup"><span data-stu-id="1a05f-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="1a05f-121">Nota þjarkann</span><span class="sxs-lookup"><span data-stu-id="1a05f-121">Use the bot</span></span>

<span data-ttu-id="1a05f-122">Þegar forritið hefur verið sett upp birtast boð með upplýsingar um þær aðgerðir sem þjarkinn getur gripið til.</span><span class="sxs-lookup"><span data-stu-id="1a05f-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Opnunarkveðja Human Resources Teams-þjarkaforrits fyrir leyfi](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="1a05f-124">Hugsanlega þarf að skrá sig inn við fyrstu samskipti við þjarkann.</span><span class="sxs-lookup"><span data-stu-id="1a05f-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="1a05f-125">Ef þú sérð ekki innskráningarglugga skaltu athuga vafrastillingarnar þínar til að leyfa sprettiglugga.</span><span class="sxs-lookup"><span data-stu-id="1a05f-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="1a05f-126">Hægt er að spyrja þjarkann um að:</span><span class="sxs-lookup"><span data-stu-id="1a05f-126">You can ask the bot to:</span></span>

- <span data-ttu-id="1a05f-127">Sýna upplýsingar um stöðu frís fyrir hverja leyfisgerð sem notandi ert skráður í.</span><span class="sxs-lookup"><span data-stu-id="1a05f-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![Sýna stöður Human Resources Teams-forrits fyrir leyfi](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="1a05f-129">Sýna frekari upplýsingar um tiltekna leyfisgerð.</span><span class="sxs-lookup"><span data-stu-id="1a05f-129">Show additional details about a specific leave type.</span></span>

   ![Sýna upplýsingar Human Resources Teams -forrits fyrir leyfi](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="1a05f-131">Hefja leyfisbeiðni fyrir notanda.</span><span class="sxs-lookup"><span data-stu-id="1a05f-131">Start a leave request for you.</span></span>

   ![Leyfisbeiðni fyrir Human Resources Teams-forrit fyrir leyfi](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="1a05f-133">Eftir að beiðni um leyfi er hafin er hægt að leiðrétta dagana innan spjaldsins.</span><span class="sxs-lookup"><span data-stu-id="1a05f-133">After you start a leave request, you can adjust the days right within the card.</span></span>

![Breytingabeiðni Human Resources Teams-forrits fyrir leyfi](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="1a05f-135">Þegar búið er að færa inn upplýsingar skal velja **Senda** til að senda þær til samþykkis.</span><span class="sxs-lookup"><span data-stu-id="1a05f-135">When you're done entering information, select **Submit** to submit it for approval.</span></span> <span data-ttu-id="1a05f-136">Einnig er hægt að velja **Vista sem drög** til að gera þetta síðar.</span><span class="sxs-lookup"><span data-stu-id="1a05f-136">You can also select **Save as draft** to come back to it later.</span></span>

![Senda beiðni í Human Resources Teams-forriti fyrir leyfi](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="1a05f-138">Stjórna leyfi í Teams</span><span class="sxs-lookup"><span data-stu-id="1a05f-138">Manage your leave in Teams</span></span>

<span data-ttu-id="1a05f-139">Flipinn **Frí** býður upp á skoðun:</span><span class="sxs-lookup"><span data-stu-id="1a05f-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="1a05f-140">Stöðuupplýsingar fyrir hverjar leyfisgerðir sem þú ert skráð(ur) í</span><span class="sxs-lookup"><span data-stu-id="1a05f-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="1a05f-141">Næstu leyfisbeiðnir</span><span class="sxs-lookup"><span data-stu-id="1a05f-141">Upcoming leave requests</span></span>

- <span data-ttu-id="1a05f-142">Fríbeiðnir</span><span class="sxs-lookup"><span data-stu-id="1a05f-142">Time-off requests</span></span>

- <span data-ttu-id="1a05f-143">Drög að leyfisbeiðnum</span><span class="sxs-lookup"><span data-stu-id="1a05f-143">Draft leave requests</span></span>

![Fríflipi fyrir fríforrit Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="1a05f-145">Búa til nýja beiðni</span><span class="sxs-lookup"><span data-stu-id="1a05f-145">Create a new request</span></span>

1. <span data-ttu-id="1a05f-146">Til að stofna nýja leyfisbeiðni skal velja **Ný beiðni**.</span><span class="sxs-lookup"><span data-stu-id="1a05f-146">To create a new leave request, select **New request**.</span></span>

   ![Ný beiðni fyrir Human Resources Teams-forrit fyrir leyfi](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="1a05f-148">Sláðu inn daginn eða dagana þar sem þú vilt taka frí og veldu svo **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="1a05f-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Bæta við fríi Human Resources Teams-forriti fyrir leyfi](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="1a05f-150">Slá inn ástæðukóða, ef við á.</span><span class="sxs-lookup"><span data-stu-id="1a05f-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="1a05f-151">Einnig skal færa inn athugasemdir og bæta við viðhengjum.</span><span class="sxs-lookup"><span data-stu-id="1a05f-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="1a05f-152">Þegar búið er að færa inn upplýsingar skal slá inn **Senda** til að senda hana til samþykkis.</span><span class="sxs-lookup"><span data-stu-id="1a05f-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="1a05f-153">Einnig er hægt að slá inn **Vista sem drög** til að gera þetta síðar.</span><span class="sxs-lookup"><span data-stu-id="1a05f-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="1a05f-154">Stjórna dragabeiðnum</span><span class="sxs-lookup"><span data-stu-id="1a05f-154">Manage draft requests</span></span>

1. <span data-ttu-id="1a05f-155">Veljið flipann **Drög**.</span><span class="sxs-lookup"><span data-stu-id="1a05f-155">Select the **Drafts** tab.</span></span>

   ![Dragaflipi í Human Resources Teams-forriti fyrir leyfi](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="1a05f-157">Veldu blýantinn til að breyta beiðninni eða ruslið til að eyða henni.</span><span class="sxs-lookup"><span data-stu-id="1a05f-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="1a05f-158">Gerið nauðsynlegar breytingar.</span><span class="sxs-lookup"><span data-stu-id="1a05f-158">Make any necessary changes.</span></span> <span data-ttu-id="1a05f-159">Þegar búið er að færa inn upplýsingar skal slá inn **Senda** til að senda hana til samþykkis.</span><span class="sxs-lookup"><span data-stu-id="1a05f-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="1a05f-160">Einnig er hægt að velja **Vista sem drög** til að gera þetta síðar.</span><span class="sxs-lookup"><span data-stu-id="1a05f-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![Breyta drögum í Human Resources Teams-forriti fyrir leyfi](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="1a05f-162">Bregðast við tilkynningum Teams</span><span class="sxs-lookup"><span data-stu-id="1a05f-162">Respond to Teams notifications</span></span>

<span data-ttu-id="1a05f-163">Þegar þú eða starfskraftur sem þú ert samþykktaraðili fyrir sendir beiðni um leyfi fyrir færðu senda tilkynningu í Human Resources forritinu í Teams.</span><span class="sxs-lookup"><span data-stu-id="1a05f-163">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="1a05f-164">Hægt er að velja tilkynninguna til að skoða hana.</span><span class="sxs-lookup"><span data-stu-id="1a05f-164">You can select the notification to view it.</span></span> <span data-ttu-id="1a05f-165">Tilkynningar birtast einnig á svæðinu **Spjall**.</span><span class="sxs-lookup"><span data-stu-id="1a05f-165">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="1a05f-166">Ef notandi er samþykkjandi er hægt að velja **Samþykkja** eða **Neita** í tilkynningunni.</span><span class="sxs-lookup"><span data-stu-id="1a05f-166">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="1a05f-167">Einnig er hægt að búa til valfrjáls skilaboð.</span><span class="sxs-lookup"><span data-stu-id="1a05f-167">You can also provide an optional message.</span></span>

![Senda beiðni um tilkynningar í forritinu Human Resources Teams](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="1a05f-169">Senda upplýsingar um væntanlegt frí til samstarfsfólks</span><span class="sxs-lookup"><span data-stu-id="1a05f-169">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="1a05f-170">Eftir að Human Resources er sett upp fyrir Teams er auðveldlega hægt að senda upplýsingar um væntanlegt frí til samstarfsfólks í hópum og spjalli.</span><span class="sxs-lookup"><span data-stu-id="1a05f-170">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="1a05f-171">Í hópi eða spjalli í Teams skal velja hnapp Human Resources fyrir neðan spjallgluggann.</span><span class="sxs-lookup"><span data-stu-id="1a05f-171">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![Hnappur Human Resources fyrir neðan spjallglugga](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="1a05f-173">Veljið leyfisbeiðnina sem á að deila.</span><span class="sxs-lookup"><span data-stu-id="1a05f-173">Select the leave request you want to share.</span></span> <span data-ttu-id="1a05f-174">Ef óskað er eftir að deila drögum að leyfisbeiðni skal byrja á því að velja **Drög**.</span><span class="sxs-lookup"><span data-stu-id="1a05f-174">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![Velja beiðni um væntanlegt frí til að deila](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="1a05f-176">Leyfisbeiðnin mun birtast í spjallinu.</span><span class="sxs-lookup"><span data-stu-id="1a05f-176">Your leave request will display in the chat.</span></span>

![Leyfisbeiðnispjald Human Resources](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="1a05f-178">Ef drög að beiðni var deilt mun þau birtast sem drög:</span><span class="sxs-lookup"><span data-stu-id="1a05f-178">If you shared a draft request, it will display as a draft:</span></span>

![Drög að leyfisbeiðnispjaldi Human Resources](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="1a05f-180">Skoða frídagatal teymisins</span><span class="sxs-lookup"><span data-stu-id="1a05f-180">View your team's leave calendar</span></span>

<span data-ttu-id="1a05f-181">Ef þú ert yfirmaður með beina undirmenn getur þú skoðað samþykkt frí hópsins þíns og frí í bið.</span><span class="sxs-lookup"><span data-stu-id="1a05f-181">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="1a05f-182">Í forritinu „Human Resources“ í Teams skal velja **Frí**.</span><span class="sxs-lookup"><span data-stu-id="1a05f-182">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="1a05f-183">Veldu **Team dagatal**.</span><span class="sxs-lookup"><span data-stu-id="1a05f-183">Select **Team calendar**.</span></span>

   ![Skoða dagatal í Human Resources Teams-forriti](./media/hr-teams-leave-app-view-calendar.png)

<span data-ttu-id="1a05f-185">Dagatalið birtir samþykkt frí og frí í bið fyrir beina undirmenn þína.</span><span class="sxs-lookup"><span data-stu-id="1a05f-185">The calendar displays your direct reports' approved and pending time off.</span></span>

![Frítímadagatal í Human Resources Teams forriti](./media/hr-teams-leave-app-calendar.png)

## <a name="troubleshooting"></a><span data-ttu-id="1a05f-187">Úrræðaleit</span><span class="sxs-lookup"><span data-stu-id="1a05f-187">Troubleshooting</span></span>

<span data-ttu-id="1a05f-188">Ef þú átt í vandræðum með að skrá þig inn í eða nota forritið Human Resources Teams skaltu reyna að fylgja þessum leiðbeiningum úrræðaleitar.</span><span class="sxs-lookup"><span data-stu-id="1a05f-188">If you're having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="1a05f-189">Ef þú átt enn í vandræðum eftir úrræðaleit skaltu hafa samband við notendaþjónustu.</span><span class="sxs-lookup"><span data-stu-id="1a05f-189">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="1a05f-190">Frekari upplýsingar er að finna í [Fá stuðning](hr-admin-troubleshooting-support.md).</span><span class="sxs-lookup"><span data-stu-id="1a05f-190">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="1a05f-191">Ekki er hægta að skrá inn í forritið „Human Resources“ í Teams</span><span class="sxs-lookup"><span data-stu-id="1a05f-191">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="1a05f-192">Ef þú getur ekki skráð þig inn í forritið er hugsanlegt að reikningurinn sem þú notar til að skrá þig inn í Microsoft Teams sé ekki tengdur við starfsmannafærslu í Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1a05f-192">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="1a05f-193">Hafa skal samskipti við kerfisstjóra til að tryggja að starfsmannafærslan sé rétt tengd.</span><span class="sxs-lookup"><span data-stu-id="1a05f-193">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="1a05f-194">Villa þegar leyfisbeiðnir eru samþykktar í forriti Human Resources í Teams</span><span class="sxs-lookup"><span data-stu-id="1a05f-194">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="1a05f-195">Ef villa kemur upp þegar verið er að reyna að samþykkja leyfisbeiðnir í Teams, skal prófa að fara í gegnum eftirfarandi villuleitarskref:</span><span class="sxs-lookup"><span data-stu-id="1a05f-195">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="1a05f-196">Gangið úr skugga um að reikningurinn sem er notaður til að skrá sig inn í Microsoft Teams sé sá sami og notaður er til að fá aðgang að Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1a05f-196">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="1a05f-197">Vertu viss um að þú sért gildur samþykktaraðili fyrir beiðnina með því að athuga stillingar verkflæðis fyrir samþykkt leyfis.</span><span class="sxs-lookup"><span data-stu-id="1a05f-197">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="1a05f-198">Frekari upplýsingar um verkflæði leyfisbeiðna er að finna í [Búa til verkflæði leyfisbeiðni](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="1a05f-198">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="1a05f-199">Þekkta aðgengisvandamál</span><span class="sxs-lookup"><span data-stu-id="1a05f-199">Known accessibility issues</span></span>

<span data-ttu-id="1a05f-200">Human Resources-forritið í Teams er með eftirfarandi aðgengisvandamál sem við vinnum að lagfæringum á í síðari útgáfum.</span><span class="sxs-lookup"><span data-stu-id="1a05f-200">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="1a05f-201">Úthreyfing</span><span class="sxs-lookup"><span data-stu-id="1a05f-201">Issue</span></span> | <span data-ttu-id="1a05f-202">Hjáleið eða skýring</span><span class="sxs-lookup"><span data-stu-id="1a05f-202">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="1a05f-203">Ef 400% aðdráttur er notaður á skjáborði eru sumir aðgerðahnappar ekki sýnilegir.</span><span class="sxs-lookup"><span data-stu-id="1a05f-203">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="1a05f-204">Mælt er með því að notað sé stækkunargler þar til við styðjum þennan aðdrátt.</span><span class="sxs-lookup"><span data-stu-id="1a05f-204">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="1a05f-205">Á flipanum **Frí** tilkynnir upplestur hnappaaðgerð þegar hausinn hnitanetsins er lesinn fyrir fríið.</span><span class="sxs-lookup"><span data-stu-id="1a05f-205">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="1a05f-206">Haus og einingar innan hnitanetsins eru flokkaðar eftir árum og eru samanfellanlegar.</span><span class="sxs-lookup"><span data-stu-id="1a05f-206">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="1a05f-207">Upplestur skilur þetta sem aðgerðarhlut, sem það er ekki.</span><span class="sxs-lookup"><span data-stu-id="1a05f-207">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="1a05f-208">Ef strokið er þegar sprettigluggi eða valmynd er opin sleppir upplestur því að lesa efni sprettigluggans eða valmyndarinnar.</span><span class="sxs-lookup"><span data-stu-id="1a05f-208">If you swipe while a popup or menu is open, voiceover skips reading the popup or menu contents.</span></span> | <span data-ttu-id="1a05f-209">Skoðaðu efnið með fingraskönnun.</span><span class="sxs-lookup"><span data-stu-id="1a05f-209">Explore the content using finger scanning.</span></span> |
| <span data-ttu-id="1a05f-210">Á flipanum **Frí** er aukaleg strokhreyfing þegar verið er að fletta að **Ástæðukóði** í nýrri beiðni.</span><span class="sxs-lookup"><span data-stu-id="1a05f-210">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="1a05f-211">Engin falin stjórnun er til staðar sem storkufletting er að reyna að ná til.</span><span class="sxs-lookup"><span data-stu-id="1a05f-211">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="1a05f-212">Á flipanum **Frí**, ef strokið á meðan dagatalið er opið, er endað utan stýringar í stað upphafs nýrrar beiðni eða þegar beiðni er breytt.</span><span class="sxs-lookup"><span data-stu-id="1a05f-212">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="1a05f-213">Þegar komið er að **Fara á daginn í dag** er það síðasti hlutinn og strokið er í öfuga átt til að komast aftur efst.</span><span class="sxs-lookup"><span data-stu-id="1a05f-213">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="1a05f-214">Upplestur les ekki merkin fyrir dagsetningar.</span><span class="sxs-lookup"><span data-stu-id="1a05f-214">Voiceover doesn't read the labels for dates.</span></span> | <span data-ttu-id="1a05f-215">Dagsetningarnar sem eru í pörum eru alltaf **Upphafsdagur** og **Lokadagur**.</span><span class="sxs-lookup"><span data-stu-id="1a05f-215">The dates encountered in pairs are always **Start date** and **End date**.</span></span> |
| <span data-ttu-id="1a05f-216">Á flipanum **Spjall** er farið aftur á toppinn þegar dagsetningin er slegin inn á meðan verið er að nota hjálpartækið eða lyklaborðið.</span><span class="sxs-lookup"><span data-stu-id="1a05f-216">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="1a05f-217">Flipi þar til þú nærð innsláttarsvæðinu aftur.</span><span class="sxs-lookup"><span data-stu-id="1a05f-217">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="1a05f-218">Tilkynning um persónuvernd</span><span class="sxs-lookup"><span data-stu-id="1a05f-218">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="1a05f-219">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="1a05f-219">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="1a05f-220">Með Dynamics 365 Human Resources þjarkanum í Microsoft Teams er texti notanda greindur til að skilja undirliggjandi fyrirspurn/ásetning.</span><span class="sxs-lookup"><span data-stu-id="1a05f-220">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="1a05f-221">Inntak notanda á borð við „Leita í contoso reikningi“ er flutt í eina af Cognitive Service hjá Microsoft sem kallast LUIS (Language Understanding Intelligent Service).</span><span class="sxs-lookup"><span data-stu-id="1a05f-221">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="1a05f-222">Lesa meira um LUIS  [hér](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="1a05f-222">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="1a05f-223">LUIS-þjónustan ræður úr eða skilur ásetning notanda (í þessu tilviki er ætlunin að finna upplýsingar) og markeiningu (í þessu tilviki er tilgreinda einingin reikningur sem heitir Contoso).</span><span class="sxs-lookup"><span data-stu-id="1a05f-223">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="1a05f-224">Þessar upplýsingar eru svo sendar í Microsoft [Azure þjarkaramma](https://azure.microsoft.com/services/bot-service/) sem vinnur með gögn úr Dynamics 365 Human Resources og sækir æskilegar upplýsingum fyrir fyrirspurn notanda.</span><span class="sxs-lookup"><span data-stu-id="1a05f-224">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="1a05f-225">Með því að setja upp og leyfa aðgang að þjarkanum samþykkir þú að leyfa LUIS-þjónustunni og Azure þjarkaramma að vinna úr ásetningi á bak við fyrirspurn, sem leiðir til betri notandaupplifunar.</span><span class="sxs-lookup"><span data-stu-id="1a05f-225">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="1a05f-226">LUIS-þjónustan og Azure þjarkaramminn kunna að hafa mismikið samræmi samanborið við Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1a05f-226">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="1a05f-227">LUIS-þjónustan hefur aðeins aðgang að fyrirspurnum notenda og er ekki hönnuð til að tengjast við Dynamics 365 Human Resources gögn eða reikning. Notandi Dynamics 365 Human Resources þjarkans gæti fært inn fyrirspurn sem inniheldur gögn viðskiptavinar, persónuleg gögn eða önnur gögn og slíkt fyrirspurnarefni gæti verið sent til LUIS-þjónustunnar og Azure þjarkarammans.</span><span class="sxs-lookup"><span data-stu-id="1a05f-227">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="1a05f-228">Innihald fyrirspurna og skilaboða notanda er vistað í LUIS-kerfi í að hámarki 30 daga, er dulkóðað þegar ekki í notkun og er ekki notað fyrir þjálfun eða endurbætur á þjónustu.</span><span class="sxs-lookup"><span data-stu-id="1a05f-228">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="1a05f-229">Lestu meira um Cognitive Services  [hér](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="1a05f-229">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="1a05f-230">Til að stjórna stjórnandastillingum fyrir forrit í Microsoft Teams er farið í [Microsoft Teams stjórnendamiðstöð](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="1a05f-230">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="1a05f-231">Microsoft Teams, hnitanet Azure-tilviks og Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="1a05f-231">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="1a05f-232">Þegar Dynamics 365 Human Resources-forritið er notað í Microsoft Teams geta tiltekin gögn um viðskiptavini flætt út fyrir landsvæðið þar sem biðlari Human Resources þjónustunnar er notaður.</span><span class="sxs-lookup"><span data-stu-id="1a05f-232">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="1a05f-233">Dynamics 365 Human Resources sendir upplýsingar um leyfisbeiðni og verkflæðisverk til Microsoft Azure tilviks hnitanets og Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="1a05f-233">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="1a05f-234">Þessi gögn má geyma í Microsoft Azure Event Grid í allt að sólarhring og verða unnin í Bandaríkjunum, þau er dulkóðuð í flutningi og í hvíld, og eru ekki notuð af Microsoft eða meðhöndlunaraðilum fyrir þjálfun eða þjónustuúrbætur.</span><span class="sxs-lookup"><span data-stu-id="1a05f-234">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="1a05f-235">Til að skilja hvar gögnin þín eru geymd í Teams skaltu skoða: [Staðsetning gagna í Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="1a05f-235">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="1a05f-236">Í samskiptum við spjallarann í forriti Human Resources, er hægt að geyma innihald samtalsins í Azure Cosmos DB og flytja það yfir í Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="1a05f-236">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="1a05f-237">Þessi gögn má geyma í Azure Cosmos DB í allt að sólarhring og kunna að vera meðhöndluð utan staðsetningarinnar þar sem Human Resources-þjónusta leigjandans er uppsett, þau er dulkóðuð í flutningi og í hvíld, og eru ekki notuð af Microsoft eða meðhöndlunaraðilum fyrir þjálfun eða þjónustuúrbætur.</span><span class="sxs-lookup"><span data-stu-id="1a05f-237">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="1a05f-238">Til að skilja hvar gögnin þín eru geymd í Teams skaltu skoða: [Staðsetning gagna í Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="1a05f-238">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="1a05f-239">Til að takmarka aðgang að Human Resources í Microsoft Teams fyrir fyrirtækið þitt eða notendur innan fyrirtækisins skal skoða [Stjórna reglum um forritsheimildir í Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="1a05f-239">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="1a05f-240">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="1a05f-240">See also</span></span>

[<span data-ttu-id="1a05f-241">Sækja og setja upp Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="1a05f-241">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="1a05f-242">Microsoft Teams hjálparmiðstöð</span><span class="sxs-lookup"><span data-stu-id="1a05f-242">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="1a05f-243">Forritið „Human Resources“ í Teams</span><span class="sxs-lookup"><span data-stu-id="1a05f-243">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
