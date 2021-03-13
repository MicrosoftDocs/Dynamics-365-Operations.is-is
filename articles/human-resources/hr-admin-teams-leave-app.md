---
title: Forritið „Human Resources“ í Teams
description: Þetta efnisatriði kynnir Microsoft Dynamics 365 Human Resources forritið í Microsoft Teams.
author: andreabichsel
manager: tfehr
ms.date: 09/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ba520f873de5b20111f9134e87281bcdf4025785
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112969"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="556a9-103">Forritið „Human Resources“ í Teams</span><span class="sxs-lookup"><span data-stu-id="556a9-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="556a9-104">Microsoft Dynamics 365 Human Resources forritið í Microsoft Teams gerir starfsmönnum kleift að biðja um frí og skoða upplýsinga um frítíma á fljótlegan hátt í Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="556a9-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="556a9-105">Starsmenn geta haft samband við þjarka til að óska eftir upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="556a9-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="556a9-106">Finna má ítarlegri upplýsingar á flipanum **Frí**.</span><span class="sxs-lookup"><span data-stu-id="556a9-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="556a9-107">Að auki er hægt að senda fólki upplýsingar um væntanlegan frítíma í hópum og spjalli utan Human Resources.</span><span class="sxs-lookup"><span data-stu-id="556a9-107">In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![Human Resources Teams þjarkaforrit fyrir leyfi](./media/hr-admin-teams-leave-app-bot.png)

![Fríflipi fyrir fríforrit Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

![Leyfisbeiðnispjald Human Resources](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="556a9-111">Setja upp</span><span class="sxs-lookup"><span data-stu-id="556a9-111">Install and setup</span></span>

<span data-ttu-id="556a9-112">Hægt er að finna forritið Human Resources í Teams versluninni.</span><span class="sxs-lookup"><span data-stu-id="556a9-112">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="556a9-113">Frekari upplýsingar um uppsetningu á Teams-forritinu má finna í [Stjórna leyfisbeiðnum í Teams](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="556a9-113">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="556a9-114">Frekari upplýsingar um stjórnun forritsheimilda í Teams er að finna í [Stjórna reglum forritaheimilda í Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="556a9-114">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="556a9-115">Kveikja á tilkynningum fyrir forritið „Human Resources“ í Teams</span><span class="sxs-lookup"><span data-stu-id="556a9-115">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="556a9-116">Ef notendur eiga að fá tilkynningar vegna leyfisbeiðna í Teams-forritinu verður að virkja tilkynningar í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="556a9-116">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="556a9-117">Aðeins notendur sem eru skráðir inn í Teams og nota Human Resources Teams-forritið fá tilkynningar.</span><span class="sxs-lookup"><span data-stu-id="556a9-117">Only users who are signed into Teams and using the Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="556a9-118">Veldu í Human Resources **Kerfisstjórnun**.</span><span class="sxs-lookup"><span data-stu-id="556a9-118">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="556a9-119">Veljið **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="556a9-119">Select **Links**.</span></span>

3. <span data-ttu-id="556a9-120">Undir **Uppsetning**, skal velja **Kerfisfæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="556a9-120">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="556a9-121">Á flipanum **Almennt** skal stilla **Kveikja á tilkynningum fyrir Teams-forritið** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="556a9-121">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Kveikja á tilkynningum fyrir Teams-forrit í kerfisfæribreytum](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="556a9-123">Til að kveikja á tilkynningum Teams fyrir alla notendur skal velja **Já** þegar spurt er um það.</span><span class="sxs-lookup"><span data-stu-id="556a9-123">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Virkja hóptilkynningar fyrir alla notendur](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="556a9-125">Kveikja eða slökkva á hóptilkynningum fyrir einstaka notendur</span><span class="sxs-lookup"><span data-stu-id="556a9-125">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="556a9-126">Þegar búið er að virkja tilkynningar fyrir Human Resources Teams forritið er hægt að kveikja eða slökkva á tilkynningum fyrir einstaka notendur.</span><span class="sxs-lookup"><span data-stu-id="556a9-126">After you've enabled notifications for the Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="556a9-127">Veldu í Human Resources **Kerfisstjórnun**.</span><span class="sxs-lookup"><span data-stu-id="556a9-127">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="556a9-128">Veljið **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="556a9-128">Select **Links**.</span></span>

3. <span data-ttu-id="556a9-129">Undir **Notendur** skal velja **Notandavalkostir**.</span><span class="sxs-lookup"><span data-stu-id="556a9-129">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="556a9-130">Veldu flipann **Verkflæði**.</span><span class="sxs-lookup"><span data-stu-id="556a9-130">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="556a9-131">Stillið **Kveikja á tilkynningum fyrir Teams-forritið** á **Já** til að virkja tilkynningar fyrir notandann eða **Nei** til að gera tilkynningar óvirkar fyrir notandann.</span><span class="sxs-lookup"><span data-stu-id="556a9-131">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Kveikja á tilkynningum Teams-forrits á verkflæðisflipanum Valkostir notanda](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="556a9-133">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="556a9-133">Select **Save**.</span></span>

## <a name="known-issues"></a><span data-ttu-id="556a9-134">Þekkt vandamál</span><span class="sxs-lookup"><span data-stu-id="556a9-134">Known issues</span></span>

| <span data-ttu-id="556a9-135">Úthreyfing</span><span class="sxs-lookup"><span data-stu-id="556a9-135">Issue</span></span> | <span data-ttu-id="556a9-136">Staða</span><span class="sxs-lookup"><span data-stu-id="556a9-136">Status</span></span> |
| --- | --- |
| <span data-ttu-id="556a9-137">Staðan er röng þegar sendur er frítími fyrir dagsetningu í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="556a9-137">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="556a9-138">Spár eru ekki enn til staðar.</span><span class="sxs-lookup"><span data-stu-id="556a9-138">Forecasting isn't yet available.</span></span> <span data-ttu-id="556a9-139">Staðan birtist fyrir núverandi dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="556a9-139">The balance displays for the current date.</span></span> |
| <span data-ttu-id="556a9-140">Ekki er hægt að hætta við beiðni með stöðuna **Í yfirferð**.</span><span class="sxs-lookup"><span data-stu-id="556a9-140">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="556a9-141">Þessi eiginleiki er ekki studdur eins og er og honum verður bætt við í síðari tíma útgáfum.</span><span class="sxs-lookup"><span data-stu-id="556a9-141">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="556a9-142">Upplýsingar um stöðu eru reiknaðar frá og með deginum í dag.</span><span class="sxs-lookup"><span data-stu-id="556a9-142">Balance information is calculated as of today.</span></span> | <span data-ttu-id="556a9-143">Kerfið sýnir eins og er ekki stöður frá uppsöfnunartímabilinu, jafnvel þótt það sé skilgreint í færibreytum leyfis og fjarvista.</span><span class="sxs-lookup"><span data-stu-id="556a9-143">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="556a9-144">Úrræðaleit</span><span class="sxs-lookup"><span data-stu-id="556a9-144">Troubleshooting</span></span>

<span data-ttu-id="556a9-145">Ef notandi á í vandræðum með að skrá sig inn í eða nota forritið Human Resources Teams skal reyna að fylgja þessum leiðbeiningum úrræðaleitar.</span><span class="sxs-lookup"><span data-stu-id="556a9-145">If a user is having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="556a9-146">Ef þú átt enn í vandræðum eftir úrræðaleit skaltu hafa samband við notendaþjónustu.</span><span class="sxs-lookup"><span data-stu-id="556a9-146">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="556a9-147">Frekari upplýsingar er að finna í [Fá stuðning](hr-admin-troubleshooting-support.md).</span><span class="sxs-lookup"><span data-stu-id="556a9-147">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="556a9-148">Ekki er hægta að skrá inn í forritið „Human Resources“ í Teams</span><span class="sxs-lookup"><span data-stu-id="556a9-148">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="556a9-149">Ef notandi hefur samband við þig vegna þess að hann vill skrá sig inn í forritið, skaltu sannprófa að þessi notandi sé með tengda starfsmannafærslu í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="556a9-149">If a user contacts you because they can't sign into the app, verify that the user has an associated employee record in Human Resources.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="556a9-150">Villa þegar leyfisbeiðnir eru samþykktar í forriti Human Resources í Teams</span><span class="sxs-lookup"><span data-stu-id="556a9-150">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="556a9-151">Ef notandi fær villu þegar reynt er að samþykkja beiðni um leyfi í Teams-forritinu skal framkvæma eftirfarandi villuleitarskref:</span><span class="sxs-lookup"><span data-stu-id="556a9-151">If a user receives an error while trying to approve leave requests in the Teams app, perform the following troubleshooting steps:</span></span>

1. <span data-ttu-id="556a9-152">Gangið úr skugga um að Teams-reikningurinn sé sá sami og hann notar til að fá aðgang að Human Resources.</span><span class="sxs-lookup"><span data-stu-id="556a9-152">Verify that their Teams account is the same one they use for accessing Human Resources.</span></span>

2. <span data-ttu-id="556a9-153">Gangið úr skugga um að hann sé gildur samþykktaraðili fyrir beiðnina með því að athuga stillingar verkflæðis fyrir samþykkt leyfis.</span><span class="sxs-lookup"><span data-stu-id="556a9-153">Verify that they're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="556a9-154">Frekari upplýsingar um verkflæði leyfisbeiðna er að finna í [Búa til verkflæði leyfisbeiðni](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="556a9-154">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="556a9-155">Tilkynning um persónuvernd</span><span class="sxs-lookup"><span data-stu-id="556a9-155">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="556a9-156">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="556a9-156">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="556a9-157">Með Dynamics 365 Human Resources þjarkanum í Microsoft Teams er texti notanda greindur til að skilja undirliggjandi fyrirspurn/ásetning.</span><span class="sxs-lookup"><span data-stu-id="556a9-157">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="556a9-158">Inntak notanda á borð við „Leita í contoso reikningi“ er flutt í eina af Cognitive Service hjá Microsoft sem kallast LUIS (Language Understanding Intelligent Service).</span><span class="sxs-lookup"><span data-stu-id="556a9-158">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="556a9-159">Lesa meira um LUIS  [hér](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="556a9-159">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="556a9-160">LUIS-þjónustan ræður úr eða skilur ásetning notanda (í þessu tilviki er ætlunin að finna upplýsingar) og markeiningu (í þessu tilviki er tilgreinda einingin reikningur sem heitir Contoso).</span><span class="sxs-lookup"><span data-stu-id="556a9-160">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="556a9-161">Þessar upplýsingar eru svo sendar í Microsoft [Azure þjarkaramma](https://azure.microsoft.com/services/bot-service/) sem vinnur með gögn úr Dynamics 365 Human Resources og sækir æskilegar upplýsingum fyrir fyrirspurn notanda.</span><span class="sxs-lookup"><span data-stu-id="556a9-161">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="556a9-162">Með því að setja upp og leyfa aðgang að þjarkanum samþykkir þú að leyfa LUIS-þjónustunni og Azure þjarkaramma að vinna úr ásetningi á bak við fyrirspurn, sem leiðir til betri notandaupplifunar.</span><span class="sxs-lookup"><span data-stu-id="556a9-162">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="556a9-163">LUIS-þjónustan og Azure þjarkaramminn kunna að hafa mismikið samræmi samanborið við Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="556a9-163">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="556a9-164">LUIS-þjónustan hefur aðeins aðgang að fyrirspurnum notenda og er ekki hönnuð til að tengjast við Dynamics 365 Human Resources gögn eða reikning. Notandi Dynamics 365 Human Resources þjarkans gæti fært inn fyrirspurn sem inniheldur gögn viðskiptavinar, persónuleg gögn eða önnur gögn og slíkt fyrirspurnarefni gæti verið sent til LUIS-þjónustunnar og Azure þjarkarammans.</span><span class="sxs-lookup"><span data-stu-id="556a9-164">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="556a9-165">Innihald fyrirspurna og skilaboða notanda er vistað í LUIS-kerfi í að hámarki 30 daga, er dulkóðað þegar ekki í notkun og er ekki notað fyrir þjálfun eða endurbætur á þjónustu.</span><span class="sxs-lookup"><span data-stu-id="556a9-165">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="556a9-166">Lestu meira um Cognitive Services  [hér](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="556a9-166">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="556a9-167">Til að stjórna stjórnandastillingum fyrir forrit í Microsoft Teams er farið í [Microsoft Teams stjórnendamiðstöð](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="556a9-167">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="556a9-168">Microsoft Teams, hnitanet Azure-tilviks og Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="556a9-168">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="556a9-169">Þegar Dynamics 365 Human Resources-forritið er notað í Microsoft Teams geta tiltekin gögn um viðskiptavini flætt út fyrir landsvæðið þar sem biðlari Human Resources þjónustunnar er notaður.</span><span class="sxs-lookup"><span data-stu-id="556a9-169">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="556a9-170">Dynamics 365 Human Resources sendir upplýsingar um leyfisbeiðni og verkflæðisverk til Microsoft Azure tilviks hnitanets og Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="556a9-170">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="556a9-171">Þessi gögn má geyma í Microsoft Azure Event Grid í allt að sólarhring og verða unnin í Bandaríkjunum, þau er dulkóðuð í flutningi og í hvíld, og eru ekki notuð af Microsoft eða meðhöndlunaraðilum fyrir þjálfun eða þjónustuúrbætur.</span><span class="sxs-lookup"><span data-stu-id="556a9-171">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="556a9-172">Til að skilja hvar gögnin þín eru geymd í Teams skaltu skoða: [Staðsetning gagna í Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="556a9-172">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="556a9-173">Í samskiptum við spjallarann í forriti Human Resources, er hægt að geyma innihald samtalsins í Azure Cosmos DB og flytja það yfir í Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="556a9-173">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="556a9-174">Þessi gögn má geyma í Azure Cosmos DB í allt að sólarhring og kunna að vera meðhöndluð utan staðsetningarinnar þar sem Human Resources-þjónusta leigjandans er uppsett, þau er dulkóðuð í flutningi og í hvíld, og eru ekki notuð af Microsoft eða meðhöndlunaraðilum fyrir þjálfun eða þjónustuúrbætur.</span><span class="sxs-lookup"><span data-stu-id="556a9-174">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="556a9-175">Til að skilja hvar gögnin þín eru geymd í Teams skaltu skoða: [Staðsetning gagna í Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="556a9-175">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="556a9-176">Til að takmarka aðgang að Human Resources í Microsoft Teams fyrir fyrirtækið þitt eða notendur innan fyrirtækisins skal skoða [Stjórna reglum um forritsheimildir í Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="556a9-176">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="556a9-177">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="556a9-177">See also</span></span> 

[<span data-ttu-id="556a9-178">Sækja og setja upp Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="556a9-178">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="556a9-179">Microsoft Teams hjálparmiðstöð</span><span class="sxs-lookup"><span data-stu-id="556a9-179">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="556a9-180">Stjórna leyfisbeiðnum í Teams</span><span class="sxs-lookup"><span data-stu-id="556a9-180">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

