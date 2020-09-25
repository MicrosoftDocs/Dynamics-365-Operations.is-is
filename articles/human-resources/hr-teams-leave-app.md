---
title: Stjórna leyfisbeiðnum í Teams
description: Þetta efnisatriði sýnir hvernig á að biðja um frí í Dynamics 365 Human Resources forritinu í Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 09/03/2020
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
ms.openlocfilehash: 0fbf44fe35af3147fd5fb478b6cbfc5a5d0b109d
ms.sourcegitcommit: 5b620f670ac0f403a0fdcdeb9c3f970b163191ee
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/04/2020
ms.locfileid: "3766761"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="f6e1c-103">Stjórna leyfisbeiðnum í Teams</span><span class="sxs-lookup"><span data-stu-id="f6e1c-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="f6e1c-104">Microsoft Dynamics 365 Human Resources -forritið í Microsoft Teams gerir þér kleift að biðja um frí og skoða upplýsingar um stöðu frítíma í Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="f6e1c-105">Hægt er að hafa samband við þjarka til að óska eftir upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-105">You can interact with a bot to request information.</span></span> <span data-ttu-id="f6e1c-106">Finna má ítarlegri upplýsingar á flipanum **Frí**.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-106">The **Time off** tab provides more detailed information.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="f6e1c-107">Setja upp forritið</span><span class="sxs-lookup"><span data-stu-id="f6e1c-107">Install the app</span></span>

<span data-ttu-id="f6e1c-108">Hægt er að finna forritið Human Resources í Teams versluninni.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-108">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="f6e1c-109">Í Microsoft Teams skal velja sporbauginn.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-109">In Microsoft Teams, select the ellipses.</span></span>

   ![Sporbaugur fyrir Human Resources Teams-forrit fyrir leyfi](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="f6e1c-111">Leitið að Dynamics 365 Human Resources og veljið síðan reitinn **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-111">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![Human Resources-spjald fyrir Human Resources Teams-forrit fyrir leyfi](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="f6e1c-113">Veljið hnappinn **Bæta við** til að setja upp forritið.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-113">Select the **Add** button to install the app.</span></span>

   ![Uppsetning Human Resources Teams-forrits fyrir leyfi](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="f6e1c-115">Ef forritið skráir þig ekki sjálfkrafa inn skaltu velja flipann **Stillingar** til að skrá þig inn.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-115">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Stillingaflipi Human Resources Teams-forrits fyrir leyfi](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="f6e1c-117">Ef þú sérð ekki innskráningarglugga skaltu athuga vafrastillingarnar þínar til að leyfa sprettiglugga.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-117">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="f6e1c-118">Ef þú hefur aðgang að fleiri en einu tilviki af Human Resources er hægt að velja hvaða umhverfi á að tengja við á flipanum **Stillingar**.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-118">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!WARNING]
> <span data-ttu-id="f6e1c-119">Forritið styður ekki öryggishlutverk kerfisstjóra og sýnir villuboð ef þú skráir þig inn með kerfisstjórareikningi.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-119">The app doesn't currently support the System Administrator security role, and will display an error message if you sign in with a System Administrator account.</span></span> <span data-ttu-id="f6e1c-120">Þegar skrá á inn með öðrum reikningi skal, á flipanum **Stillingar**, velja hnappinn **Skipta um reikning** og skrá inn með notandareikningi sem er ekki með kerfisstjóraréttindi.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-120">To sign in with a different account, on the **Settings** tab, select the **Switch accounts** button, and then sign in with a user account that doesn’t have System Administrator privileges.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="f6e1c-121">Nota þjarkann</span><span class="sxs-lookup"><span data-stu-id="f6e1c-121">Use the bot</span></span>

<span data-ttu-id="f6e1c-122">Þegar forritið hefur verið sett upp birtast boð með upplýsingar um þær aðgerðir sem þjarkinn getur gripið til.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Opnunarkveðja Human Resources Teams-þjarkaforrits fyrir leyfi](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="f6e1c-124">Hugsanlega þarf að skrá sig inn við fyrstu samskipti við þjarkann.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="f6e1c-125">Ef þú sérð ekki innskráningarglugga skaltu athuga vafrastillingarnar þínar til að leyfa sprettiglugga.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="f6e1c-126">Hægt er að spyrja þjarkann um að:</span><span class="sxs-lookup"><span data-stu-id="f6e1c-126">You can ask the bot to:</span></span>

- <span data-ttu-id="f6e1c-127">Sýna upplýsingar um stöðu frís fyrir hverja leyfisgerð sem notandi ert skráður í.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![Sýna stöður Human Resources Teams-forrits fyrir leyfi](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="f6e1c-129">Sýna frekari upplýsingar um tiltekna leyfisgerð.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-129">Show additional details about a specific leave type.</span></span>

   ![Sýna upplýsingar Human Resources Teams -forrits fyrir leyfi](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="f6e1c-131">Hefja leyfisbeiðni fyrir notanda.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-131">Start a leave request for you.</span></span>

   ![Leyfisbeiðni fyrir Human Resources Teams-forrit fyrir leyfi](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="f6e1c-133">Eftir að beiðni um leyfi er hafin er hægt að leiðrétta dagana innan spjaldsins.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-133">After you start a leave request, you can adjust the days right within the card.</span></span>

![Breytingabeiðni Human Resources Teams-forrits fyrir leyfi](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="f6e1c-135">Þegar búið er að færa inn upplýsingar skal velja **Senda** til að senda þær til samþykkis.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-135">When you're done entering information, select **Submit** to submit it for approval.</span></span> <span data-ttu-id="f6e1c-136">Einnig er hægt að velja **Vista sem drög** til að gera þetta síðar.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-136">You can also select **Save as draft** to come back to it later.</span></span>

![Senda beiðni í Human Resources Teams-forriti fyrir leyfi](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="f6e1c-138">Stjórna leyfi í Teams</span><span class="sxs-lookup"><span data-stu-id="f6e1c-138">Manage your leave in Teams</span></span>

<span data-ttu-id="f6e1c-139">Flipinn **Frí** býður upp á skoðun:</span><span class="sxs-lookup"><span data-stu-id="f6e1c-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="f6e1c-140">Stöðuupplýsingar fyrir hverjar leyfisgerðir sem þú ert skráð(ur) í</span><span class="sxs-lookup"><span data-stu-id="f6e1c-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="f6e1c-141">Næstu leyfisbeiðnir</span><span class="sxs-lookup"><span data-stu-id="f6e1c-141">Upcoming leave requests</span></span>

- <span data-ttu-id="f6e1c-142">Fríbeiðnir</span><span class="sxs-lookup"><span data-stu-id="f6e1c-142">Time-off requests</span></span>

- <span data-ttu-id="f6e1c-143">Drög að leyfisbeiðnum</span><span class="sxs-lookup"><span data-stu-id="f6e1c-143">Draft leave requests</span></span>

![Fríflipi fyrir fríforrit Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="f6e1c-145">Búa til nýja beiðni</span><span class="sxs-lookup"><span data-stu-id="f6e1c-145">Create a new request</span></span>

1. <span data-ttu-id="f6e1c-146">Til að stofna nýja leyfisbeiðni skal velja **Ný beiðni**.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-146">To create a new leave request, select **New request**.</span></span>

   ![Ný beiðni fyrir Human Resources Teams-forrit fyrir leyfi](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="f6e1c-148">Sláðu inn daginn eða dagana þar sem þú vilt taka frí og veldu svo **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Bæta við fríi Human Resources Teams-forriti fyrir leyfi](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="f6e1c-150">Slá inn ástæðukóða, ef við á.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="f6e1c-151">Einnig skal færa inn athugasemdir og bæta við viðhengjum.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="f6e1c-152">Þegar búið er að færa inn upplýsingar skal slá inn **Senda** til að senda hana til samþykkis.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="f6e1c-153">Einnig er hægt að slá inn **Vista sem drög** til að gera þetta síðar.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="f6e1c-154">Stjórna dragabeiðnum</span><span class="sxs-lookup"><span data-stu-id="f6e1c-154">Manage draft requests</span></span>

1. <span data-ttu-id="f6e1c-155">Veljið flipann **Drög**.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-155">Select the **Drafts** tab.</span></span>

   ![Dragaflipi í Human Resources Teams-forriti fyrir leyfi](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="f6e1c-157">Veldu blýantinn til að breyta beiðninni eða ruslið til að eyða henni.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="f6e1c-158">Gerið nauðsynlegar breytingar.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-158">Make any necessary changes.</span></span> <span data-ttu-id="f6e1c-159">Þegar búið er að færa inn upplýsingar skal slá inn **Senda** til að senda hana til samþykkis.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="f6e1c-160">Einnig er hægt að velja **Vista sem drög** til að gera þetta síðar.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![Breyta drögum í Human Resources Teams-forriti fyrir leyfi](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="teams-notifications"></a><span data-ttu-id="f6e1c-162">Teams-tilkynningar</span><span class="sxs-lookup"><span data-stu-id="f6e1c-162">Teams notifications</span></span>

<span data-ttu-id="f6e1c-163">Þegar þú eða starfskraftur sem þú ert samþykktaraðili fyrir sendir beiðni um leyfi fyrir færðu senda tilkynningu í Human Resources forritinu í Teams.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-163">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="f6e1c-164">Hægt er að velja tilkynninguna til að skoða hana.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-164">You can select the notification to view it.</span></span> <span data-ttu-id="f6e1c-165">Tilkynningar birtast einnig á svæðinu **Spjall**.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-165">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="f6e1c-166">Ef notandi er samþykkjandi er hægt að velja **Samþykkja** eða **Neita** í tilkynningunni.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-166">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="f6e1c-167">Einnig er hægt að búa til valfrjáls skilaboð.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-167">You can also provide an optional message.</span></span>

![Senda beiðni um tilkynningar í forritinu Human Resources Teams](./media/hr-teams-leave-app-notification.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="f6e1c-169">Skoða frídagatal teymisins</span><span class="sxs-lookup"><span data-stu-id="f6e1c-169">View your team's leave calendar</span></span>

<span data-ttu-id="f6e1c-170">Ef þú ert yfirmaður með beina undirmenn getur þú skoðað samþykkt frí hópsins þíns og frí í bið.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-170">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="f6e1c-171">Í forritinu „Human Resources“ í Teams skal velja **Frí**.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-171">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="f6e1c-172">Veldu **Team dagatal**.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-172">Select **Team calendar**.</span></span>

   ![Skoða dagatal í Human Resources Teams-forriti](./media/hr-teams-leave-app-view-calendar.png)

<span data-ttu-id="f6e1c-174">Dagatalið birtir samþykkt frí og frí í bið fyrir beina undirmenn þína.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-174">The calendar displays your direct reports' approved and pending time off.</span></span>

![Frítímadagatal í Human Resources Teams forriti](./media/hr-teams-leave-app-calendar.png)

## <a name="privacy-notice"></a><span data-ttu-id="f6e1c-176">Tilkynning um persónuvernd</span><span class="sxs-lookup"><span data-stu-id="f6e1c-176">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="f6e1c-177">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="f6e1c-177">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="f6e1c-178">Með Dynamics 365 Human Resources þjarkanum í Microsoft Teams er texti notanda greindur til að skilja undirliggjandi fyrirspurn/ásetning.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-178">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="f6e1c-179">Inntak notanda á borð við „Leita í contoso reikningi“ er flutt í eina af Cognitive Service hjá Microsoft sem kallast LUIS (Language Understanding Intelligent Service).</span><span class="sxs-lookup"><span data-stu-id="f6e1c-179">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="f6e1c-180">Lesa meira um LUIS  [hér](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="f6e1c-180">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="f6e1c-181">LUIS-þjónustan ræður úr eða skilur ásetning notanda (í þessu tilviki er ætlunin að finna upplýsingar) og markeiningu (í þessu tilviki er tilgreinda einingin reikningur sem heitir Contoso).</span><span class="sxs-lookup"><span data-stu-id="f6e1c-181">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="f6e1c-182">Þessar upplýsingar eru svo sendar í Microsoft [Azure þjarkaramma](https://azure.microsoft.com/services/bot-service/) sem vinnur með gögn úr Dynamics 365 Human Resources og sækir æskilegar upplýsingum fyrir fyrirspurn notanda.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-182">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="f6e1c-183">Með því að setja upp og leyfa aðgang að þjarkanum samþykkir þú að leyfa LUIS-þjónustunni og Azure þjarkaramma að vinna úr ásetningi á bak við fyrirspurn, sem leiðir til betri notandaupplifunar.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-183">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="f6e1c-184">LUIS-þjónustan og Azure þjarkaramminn kunna að hafa mismikið samræmi samanborið við Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-184">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="f6e1c-185">LUIS-þjónustan hefur aðeins aðgang að fyrirspurnum notenda og er ekki hönnuð til að tengjast við Dynamics 365 Human Resources gögn eða reikning. Notandi Dynamics 365 Human Resources þjarkans gæti fært inn fyrirspurn sem inniheldur gögn viðskiptavinar, persónuleg gögn eða önnur gögn og slíkt fyrirspurnarefni gæti verið sent til LUIS-þjónustunnar og Azure þjarkarammans.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-185">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="f6e1c-186">Innihald fyrirspurna og skilaboða notanda er vistað í LUIS-kerfi í að hámarki 30 daga, er dulkóðað þegar ekki í notkun og er ekki notað fyrir þjálfun eða endurbætur á þjónustu.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-186">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="f6e1c-187">Lestu meira um Cognitive Services  [hér](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="f6e1c-187">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="f6e1c-188">Til að stjórna stjórnandastillingum fyrir forrit í Microsoft Teams er farið í [Microsoft Teams stjórnendamiðstöð](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="f6e1c-188">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a><span data-ttu-id="f6e1c-189">Microsoft Azure -Tilvikhnitanet og Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="f6e1c-189">Microsoft Azure Event Grid and Microsoft Teams</span></span>

<span data-ttu-id="f6e1c-190">Þegar tilkynningaeiginleiki er notaður fyrir Dynamics 365 Human Resources-forritið í Teams flæð tiltekin gögn um viðskiptavini út fyrir landsvæðið þar sem biðlari Human Resources þjónustunnar ern notaður.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-190">When using the notifications feature for the Dynamics 365 Human Resources app in Teams, certain customer data will flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span> <span data-ttu-id="f6e1c-191">Dynamics 365 Human Resources sendir upplýsingar um leyfisbeiðni og verkflæðisverk til Microsoft Azure tilviks hnitanets og Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-191">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="f6e1c-192">Þessi gögn kunna að vera geymd í allt að sólarhring og unnin í Bandaríkjunum, þau er dulkóðuð í flutningi og í hvíld, og eru ekki notuð af Microsoft eða meðhöndlunaraðilum fyrir þjálfun eða þjónustuúrbætur.</span><span class="sxs-lookup"><span data-stu-id="f6e1c-192">This data may be stored for up to 24 hours and processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span>

## <a name="see-also"></a><span data-ttu-id="f6e1c-193">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="f6e1c-193">See also</span></span>

[<span data-ttu-id="f6e1c-194">Sækja og setja upp Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="f6e1c-194">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="f6e1c-195">Microsoft Teams hjálparmiðstöð</span><span class="sxs-lookup"><span data-stu-id="f6e1c-195">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="f6e1c-196">Forritið „Human Resources“ í Teams</span><span class="sxs-lookup"><span data-stu-id="f6e1c-196">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
