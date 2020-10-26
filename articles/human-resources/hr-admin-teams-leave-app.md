---
title: Forritið „Human Resources“ í Teams
description: Þetta efnisatriði kynnir Microsoft Dynamics 365 Human Resources forritið í Microsoft Teams.
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: 51f04e553da822c4e09d31bcd72c71b674ad1f1b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930018"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="e53a6-103">Forritið „Human Resources“ í Teams</span><span class="sxs-lookup"><span data-stu-id="e53a6-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="e53a6-104">Microsoft Dynamics 365 Human Resources forritið í Microsoft Teams gerir starfsmönnum kleift að biðja um frí og skoða upplýsinga um frítíma á fljótlegan hátt í Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="e53a6-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="e53a6-105">Starsmenn geta haft samband við þjarka til að óska eftir upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="e53a6-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="e53a6-106">Finna má ítarlegri upplýsingar á flipanum **Frí**.</span><span class="sxs-lookup"><span data-stu-id="e53a6-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="e53a6-107">Að auki er hægt að senda fólki upplýsingar um væntanlegan frítíma í hópum og spjalli utan Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e53a6-107">In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![Human Resources Teams þjarkaforrit fyrir leyfi](./media/hr-admin-teams-leave-app-bot.png)

![Fríflipi fyrir fríforrit Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

![Leyfisbeiðnispjald Human Resources](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="e53a6-111">Setja upp</span><span class="sxs-lookup"><span data-stu-id="e53a6-111">Install and setup</span></span>

<span data-ttu-id="e53a6-112">Hægt er að finna forritið Human Resources í Teams versluninni.</span><span class="sxs-lookup"><span data-stu-id="e53a6-112">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="e53a6-113">Frekari upplýsingar um uppsetningu á Teams-forritinu má finna í [Stjórna leyfisbeiðnum í Teams](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="e53a6-113">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="e53a6-114">Frekari upplýsingar um stjórnun forritsheimilda í Teams er að finna í [Stjórna reglum forritaheimilda í Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="e53a6-114">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="e53a6-115">Kveikja á tilkynningum fyrir forritið „Human Resources“ í Teams</span><span class="sxs-lookup"><span data-stu-id="e53a6-115">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="e53a6-116">Ef notendur eiga að fá tilkynningar vegna leyfisbeiðna í Teams-forritinu verður að virkja tilkynningar í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e53a6-116">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="e53a6-117">Aðeins notendur sem eru skráðir inn í Teams og nota Human Resources Teams-forritið fá tilkynningar.</span><span class="sxs-lookup"><span data-stu-id="e53a6-117">Only users who are signed into Teams and using the Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="e53a6-118">Veldu í Human Resources **Kerfisstjórnun**.</span><span class="sxs-lookup"><span data-stu-id="e53a6-118">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="e53a6-119">Veljið **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="e53a6-119">Select **Links**.</span></span>

3. <span data-ttu-id="e53a6-120">Undir **Uppsetning**, skal velja **Kerfisfæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="e53a6-120">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="e53a6-121">Á flipanum **Almennt** skal stilla **Kveikja á tilkynningum fyrir Teams-forritið** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="e53a6-121">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Kveikja á tilkynningum fyrir Teams-forrit í kerfisfæribreytum](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="e53a6-123">Til að kveikja á tilkynningum Teams fyrir alla notendur skal velja **Já** þegar spurt er um það.</span><span class="sxs-lookup"><span data-stu-id="e53a6-123">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Virkja hóptilkynningar fyrir alla notendur](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="e53a6-125">Kveikja eða slökkva á hóptilkynningum fyrir einstaka notendur</span><span class="sxs-lookup"><span data-stu-id="e53a6-125">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="e53a6-126">Þegar búið er að virkja tilkynningar fyrir Human Resources Teams forritið er hægt að kveikja eða slökkva á tilkynningum fyrir einstaka notendur.</span><span class="sxs-lookup"><span data-stu-id="e53a6-126">After you've enabled notifications for the Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="e53a6-127">Veldu í Human Resources **Kerfisstjórnun**.</span><span class="sxs-lookup"><span data-stu-id="e53a6-127">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="e53a6-128">Veljið **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="e53a6-128">Select **Links**.</span></span>

3. <span data-ttu-id="e53a6-129">Undir **Notendur** skal velja **Notandavalkostir**.</span><span class="sxs-lookup"><span data-stu-id="e53a6-129">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="e53a6-130">Veldu flipann **Verkflæði**.</span><span class="sxs-lookup"><span data-stu-id="e53a6-130">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="e53a6-131">Stillið **Kveikja á tilkynningum fyrir Teams-forritið** á **Já** til að virkja tilkynningar fyrir notandann eða **Nei** til að gera tilkynningar óvirkar fyrir notandann.</span><span class="sxs-lookup"><span data-stu-id="e53a6-131">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Kveikja á tilkynningum Teams-forrits á verkflæðisflipanum Valkostir notanda](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="e53a6-133">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e53a6-133">Select **Save**.</span></span>

## <a name="known-issues"></a><span data-ttu-id="e53a6-134">Þekkt vandamál</span><span class="sxs-lookup"><span data-stu-id="e53a6-134">Known issues</span></span>

| <span data-ttu-id="e53a6-135">Úthreyfing</span><span class="sxs-lookup"><span data-stu-id="e53a6-135">Issue</span></span> | <span data-ttu-id="e53a6-136">Staða</span><span class="sxs-lookup"><span data-stu-id="e53a6-136">Status</span></span> |
| --- | --- |
| <span data-ttu-id="e53a6-137">Lárétt fletting virkar ekki í Android-símum</span><span class="sxs-lookup"><span data-stu-id="e53a6-137">Horizontal scrolling doesn't work on Android phones</span></span> | <span data-ttu-id="e53a6-138">Lárétt fletting eru ekki vandamál í iOS eða borðtölvum.</span><span class="sxs-lookup"><span data-stu-id="e53a6-138">Horizontal scrolling isn't an issue on iOS or desktop devices.</span></span> <span data-ttu-id="e53a6-139">Unnið er að lagfæringu fyrir Android.</span><span class="sxs-lookup"><span data-stu-id="e53a6-139">We're working on a fix for Android.</span></span> |
| <span data-ttu-id="e53a6-140">Staðan er röng þegar sendur er frítími fyrir dagsetningu í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="e53a6-140">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="e53a6-141">Spár eru ekki enn til staðar.</span><span class="sxs-lookup"><span data-stu-id="e53a6-141">Forecasting isn't yet available.</span></span> <span data-ttu-id="e53a6-142">Staðan birtist fyrir núverandi dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="e53a6-142">The balance displays for the current date.</span></span> |
| <span data-ttu-id="e53a6-143">Ekki er hægt að hætta við beiðni með stöðuna **Í yfirferð**.</span><span class="sxs-lookup"><span data-stu-id="e53a6-143">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="e53a6-144">Þessi eiginleiki er ekki studdur eins og er og honum verður bætt við í síðari tíma útgáfum.</span><span class="sxs-lookup"><span data-stu-id="e53a6-144">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="e53a6-145">Upplýsingar um stöðu eru reiknaðar frá og með deginum í dag.</span><span class="sxs-lookup"><span data-stu-id="e53a6-145">Balance information is calculated as of today.</span></span> | <span data-ttu-id="e53a6-146">Kerfið sýnir eins og er ekki stöður frá uppsöfnunartímabilinu, jafnvel þótt það sé skilgreint í færibreytum leyfis og fjarvista.</span><span class="sxs-lookup"><span data-stu-id="e53a6-146">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="e53a6-147">Úrræðaleit</span><span class="sxs-lookup"><span data-stu-id="e53a6-147">Troubleshooting</span></span>

<span data-ttu-id="e53a6-148">Ef notandi á í vandræðum með að skrá sig inn í eða nota forritið Human Resources Teams skal reyna að fylgja þessum leiðbeiningum úrræðaleitar.</span><span class="sxs-lookup"><span data-stu-id="e53a6-148">If a user is having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="e53a6-149">Ef þú átt enn í vandræðum eftir úrræðaleit skaltu hafa samband við notendaþjónustu.</span><span class="sxs-lookup"><span data-stu-id="e53a6-149">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="e53a6-150">Frekari upplýsingar er að finna í [Fá stuðning](hr-admin-troubleshooting-support.md).</span><span class="sxs-lookup"><span data-stu-id="e53a6-150">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="e53a6-151">Ekki er hægta að skrá inn í forritið „Human Resources“ í Teams</span><span class="sxs-lookup"><span data-stu-id="e53a6-151">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="e53a6-152">Ef notandi hefur samband við þig vegna þess að hann vill skrá sig inn í forritið, skaltu sannprófa að þessi notandi sé með tengda starfsmannafærslu í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e53a6-152">If a user contacts you because they can't sign into the app, verify that the user has an associated employee record in Human Resources.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="e53a6-153">Villa þegar leyfisbeiðnir eru samþykktar í forriti Human Resources í Teams</span><span class="sxs-lookup"><span data-stu-id="e53a6-153">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="e53a6-154">Ef notandi fær villu þegar reynt er að samþykkja beiðni um leyfi í Teams-forritinu skal framkvæma eftirfarandi villuleitarskref:</span><span class="sxs-lookup"><span data-stu-id="e53a6-154">If a user receives an error while trying to approve leave requests in the Teams app, perform the following troubleshooting steps:</span></span>

1. <span data-ttu-id="e53a6-155">Gangið úr skugga um að Teams-reikningurinn sé sá sami og hann notar til að fá aðgang að Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e53a6-155">Verify that their Teams account is the same one they use for accessing Human Resources.</span></span>

2. <span data-ttu-id="e53a6-156">Gangið úr skugga um að hann sé gildur samþykktaraðili fyrir beiðnina með því að athuga stillingar verkflæðis fyrir samþykkt leyfis.</span><span class="sxs-lookup"><span data-stu-id="e53a6-156">Verify that they're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="e53a6-157">Frekari upplýsingar um verkflæði leyfisbeiðna er að finna í [Búa til verkflæði leyfisbeiðni](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="e53a6-157">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="e53a6-158">Tilkynning um persónuvernd</span><span class="sxs-lookup"><span data-stu-id="e53a6-158">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="e53a6-159">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="e53a6-159">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="e53a6-160">Með Dynamics 365 Human Resources þjarkanum í Microsoft Teams er texti notanda greindur til að skilja undirliggjandi fyrirspurn/ásetning.</span><span class="sxs-lookup"><span data-stu-id="e53a6-160">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="e53a6-161">Inntak notanda á borð við „Leita í contoso reikningi“ er flutt í eina af Cognitive Service hjá Microsoft sem kallast LUIS (Language Understanding Intelligent Service).</span><span class="sxs-lookup"><span data-stu-id="e53a6-161">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="e53a6-162">Lesa meira um LUIS  [hér](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="e53a6-162">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="e53a6-163">LUIS-þjónustan ræður úr eða skilur ásetning notanda (í þessu tilviki er ætlunin að finna upplýsingar) og markeiningu (í þessu tilviki er tilgreinda einingin reikningur sem heitir Contoso).</span><span class="sxs-lookup"><span data-stu-id="e53a6-163">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="e53a6-164">Þessar upplýsingar eru svo sendar í Microsoft [Azure þjarkaramma](https://azure.microsoft.com/services/bot-service/) sem vinnur með gögn úr Dynamics 365 Human Resources og sækir æskilegar upplýsingum fyrir fyrirspurn notanda.</span><span class="sxs-lookup"><span data-stu-id="e53a6-164">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="e53a6-165">Með því að setja upp og leyfa aðgang að þjarkanum samþykkir þú að leyfa LUIS-þjónustunni og Azure þjarkaramma að vinna úr ásetningi á bak við fyrirspurn, sem leiðir til betri notandaupplifunar.</span><span class="sxs-lookup"><span data-stu-id="e53a6-165">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="e53a6-166">LUIS-þjónustan og Azure þjarkaramminn kunna að hafa mismikið samræmi samanborið við Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e53a6-166">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="e53a6-167">LUIS-þjónustan hefur aðeins aðgang að fyrirspurnum notenda og er ekki hönnuð til að tengjast við Dynamics 365 Human Resources gögn eða reikning. Notandi Dynamics 365 Human Resources þjarkans gæti fært inn fyrirspurn sem inniheldur gögn viðskiptavinar, persónuleg gögn eða önnur gögn og slíkt fyrirspurnarefni gæti verið sent til LUIS-þjónustunnar og Azure þjarkarammans.</span><span class="sxs-lookup"><span data-stu-id="e53a6-167">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="e53a6-168">Innihald fyrirspurna og skilaboða notanda er vistað í LUIS-kerfi í að hámarki 30 daga, er dulkóðað þegar ekki í notkun og er ekki notað fyrir þjálfun eða endurbætur á þjónustu.</span><span class="sxs-lookup"><span data-stu-id="e53a6-168">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="e53a6-169">Lestu meira um Cognitive Services  [hér](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="e53a6-169">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="e53a6-170">Til að stjórna stjórnandastillingum fyrir forrit í Microsoft Teams er farið í [Microsoft Teams stjórnendamiðstöð](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="e53a6-170">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="e53a6-171">Microsoft Teams, hnitanet Azure-tilviks og Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="e53a6-171">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="e53a6-172">Þegar Dynamics 365 Human Resources-forritið er notað í Microsoft Teams geta tiltekin gögn um viðskiptavini flætt út fyrir landsvæðið þar sem biðlari Human Resources þjónustunnar er notaður.</span><span class="sxs-lookup"><span data-stu-id="e53a6-172">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="e53a6-173">Dynamics 365 Human Resources sendir upplýsingar um leyfisbeiðni og verkflæðisverk til Microsoft Azure tilviks hnitanets og Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="e53a6-173">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="e53a6-174">Þessi gögn má geyma í Microsoft Azure Event Grid í allt að sólarhring og verða unnin í Bandaríkjunum, þau er dulkóðuð í flutningi og í hvíld, og eru ekki notuð af Microsoft eða meðhöndlunaraðilum fyrir þjálfun eða þjónustuúrbætur.</span><span class="sxs-lookup"><span data-stu-id="e53a6-174">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="e53a6-175">Til að skilja hvar gögnin þín eru geymd í Teams skaltu skoða: [Staðsetning gagna í Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="e53a6-175">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="e53a6-176">Í samskiptum við spjallarann í forriti Human Resources, er hægt að geyma innihald samtalsins í Azure Cosmos DB og flytja það yfir í Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="e53a6-176">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="e53a6-177">Þessi gögn má geyma í Azure Cosmos DB í allt að sólarhring og kunna að vera meðhöndluð utan staðsetningarinnar þar sem Human Resources-þjónusta leigjandans er uppsett, þau er dulkóðuð í flutningi og í hvíld, og eru ekki notuð af Microsoft eða meðhöndlunaraðilum fyrir þjálfun eða þjónustuúrbætur.</span><span class="sxs-lookup"><span data-stu-id="e53a6-177">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="e53a6-178">Til að skilja hvar gögnin þín eru geymd í Teams skaltu skoða: [Staðsetning gagna í Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="e53a6-178">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="e53a6-179">Til að takmarka aðgang að Human Resources í Microsoft Teams fyrir fyrirtækið þitt eða notendur innan fyrirtækisins skal skoða [Stjórna reglum um forritsheimildir í Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="e53a6-179">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="e53a6-180">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="e53a6-180">See also</span></span> 

[<span data-ttu-id="e53a6-181">Sækja og setja upp Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="e53a6-181">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="e53a6-182">Microsoft Teams hjálparmiðstöð</span><span class="sxs-lookup"><span data-stu-id="e53a6-182">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="e53a6-183">Stjórna leyfisbeiðnum í Teams</span><span class="sxs-lookup"><span data-stu-id="e53a6-183">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

