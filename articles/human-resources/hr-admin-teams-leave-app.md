---
title: Forritið „Human Resources“ í Teams
description: Þetta efnisatriði kynnir Microsoft Dynamics 365 Human Resources forritið í Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 09/01/2020
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
ms.openlocfilehash: 33322b9b553076125695f257b201463e9d8275c6
ms.sourcegitcommit: e27510ba52623c801353eed4853f8c0aeea3bb2d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/22/2020
ms.locfileid: "3828915"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="2f7d8-103">Forritið „Human Resources“ í Teams</span><span class="sxs-lookup"><span data-stu-id="2f7d8-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="2f7d8-104">Microsoft Dynamics 365 Human Resources forritið í Microsoft Teams gerir starfsmönnum kleift að biðja um frí og skoða upplýsinga um frítíma á fljótlegan hátt í Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="2f7d8-105">Starsmenn geta haft samband við þjarka til að óska eftir upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="2f7d8-106">Flipinn **Frí** veitir ítarlegri upplýsingar. Að auki geta þeir sent fólki upplýsingar um frítíma framundan í hópum og spjalli utan forrits Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-106">The **Time off** tab provides more detailed information.In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![Human Resources Teams þjarkaforrit fyrir leyfi](./media/hr-admin-teams-leave-app-bot.png)

![Fríflipi fyrir fríforrit Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

![Leyfisbeiðnispjald Human Resources](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="2f7d8-110">Setja upp</span><span class="sxs-lookup"><span data-stu-id="2f7d8-110">Install and setup</span></span>

<span data-ttu-id="2f7d8-111">Hægt er að finna forritið Human Resources í Teams versluninni.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-111">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="2f7d8-112">Frekari upplýsingar um uppsetningu á Teams-forritinu má finna í [Stjórna leyfisbeiðnum í Teams](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="2f7d8-112">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="2f7d8-113">Frekari upplýsingar um stjórnun forritsheimilda í Teams er að finna í [Stjórna reglum forritaheimilda í Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="2f7d8-113">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="2f7d8-114">Kveikja á tilkynningum fyrir forritið „Human Resources“ í Teams</span><span class="sxs-lookup"><span data-stu-id="2f7d8-114">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="2f7d8-115">Ef notendur eiga að fá tilkynningar vegna leyfisbeiðna í Teams-forritinu verður að virkja tilkynningar í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-115">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="2f7d8-116">Aðeins notendur sem eru skráðir inn í Teams og nota Human Resources Teams-forritið fá tilkynningar.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-116">Only users who are signed into Teams and using the Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="2f7d8-117">Veldu í Human Resources **Kerfisstjórnun**.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-117">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="2f7d8-118">Veljið **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-118">Select **Links**.</span></span>

3. <span data-ttu-id="2f7d8-119">Undir **Uppsetning**, skal velja **Kerfisfæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-119">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="2f7d8-120">Á flipanum **Almennt** skal stilla **Kveikja á tilkynningum fyrir Teams-forritið** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-120">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Kveikja á tilkynningum fyrir Teams-forrit í kerfisfæribreytum](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="2f7d8-122">Til að kveikja á tilkynningum Teams fyrir alla notendur skal velja **Já** þegar spurt er um það.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-122">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Virkja hóptilkynningar fyrir alla notendur](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="2f7d8-124">Kveikja eða slökkva á hóptilkynningum fyrir einstaka notendur</span><span class="sxs-lookup"><span data-stu-id="2f7d8-124">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="2f7d8-125">Þegar búið er að virkja tilkynningar fyrir Human Resources Teams forritið er hægt að kveikja eða slökkva á tilkynningum fyrir einstaka notendur.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-125">After you've enabled notifications for the Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="2f7d8-126">Veldu í Human Resources **Kerfisstjórnun**.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="2f7d8-127">Veljið **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-127">Select **Links**.</span></span>

3. <span data-ttu-id="2f7d8-128">Undir **Notendur** skal velja **Notandavalkostir**.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-128">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="2f7d8-129">Veldu flipann **Verkflæði**.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-129">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="2f7d8-130">Stillið **Kveikja á tilkynningum fyrir Teams-forritið** á **Já** til að virkja tilkynningar fyrir notandann eða **Nei** til að gera tilkynningar óvirkar fyrir notandann.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-130">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Kveikja á tilkynningum Teams-forrits á verkflæðisflipanum Valkostir notanda](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="2f7d8-132">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-132">Select **Save**.</span></span>

## <a name="known-issues"></a><span data-ttu-id="2f7d8-133">Þekkt vandamál</span><span class="sxs-lookup"><span data-stu-id="2f7d8-133">Known issues</span></span>

| <span data-ttu-id="2f7d8-134">Úthreyfing</span><span class="sxs-lookup"><span data-stu-id="2f7d8-134">Issue</span></span> | <span data-ttu-id="2f7d8-135">Staða</span><span class="sxs-lookup"><span data-stu-id="2f7d8-135">Status</span></span> |
| --- | --- |
| <span data-ttu-id="2f7d8-136">Lárétt fletting virkar ekki í Android-símum</span><span class="sxs-lookup"><span data-stu-id="2f7d8-136">Horizontal scrolling doesn't work on Android phones</span></span> | <span data-ttu-id="2f7d8-137">Lárétt fletting eru ekki vandamál í iOS eða borðtölvum.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-137">Horizontal scrolling isn't an issue on iOS or desktop devices.</span></span> <span data-ttu-id="2f7d8-138">Unnið er að lagfæringu fyrir Android.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-138">We're working on a fix for Android.</span></span> |
| <span data-ttu-id="2f7d8-139">Staðan er röng þegar sendur er frítími fyrir dagsetningu í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-139">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="2f7d8-140">Spár eru ekki enn til staðar.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-140">Forecasting isn't yet available.</span></span> <span data-ttu-id="2f7d8-141">Staðan birtist fyrir núverandi dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-141">The balance displays for the current date.</span></span> |
| <span data-ttu-id="2f7d8-142">Ekki er hægt að hætta við beiðni með stöðuna **Í yfirferð**.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-142">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="2f7d8-143">Þessi eiginleiki er ekki studdur eins og er og honum verður bætt við í síðari tíma útgáfum.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-143">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="2f7d8-144">Upplýsingar um stöðu eru reiknaðar frá og með deginum í dag.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-144">Balance information is calculated as of today.</span></span> | <span data-ttu-id="2f7d8-145">Kerfið sýnir eins og er ekki stöður frá uppsöfnunartímabilinu, jafnvel þótt það sé skilgreint í færibreytum leyfis og fjarvista.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-145">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="2f7d8-146">Tilkynning um persónuvernd</span><span class="sxs-lookup"><span data-stu-id="2f7d8-146">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="2f7d8-147">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="2f7d8-147">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="2f7d8-148">Með Dynamics 365 Human Resources þjarkanum í Microsoft Teams er texti notanda greindur til að skilja undirliggjandi fyrirspurn/ásetning.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-148">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="2f7d8-149">Inntak notanda á borð við „Leita í contoso reikningi“ er flutt í eina af Cognitive Service hjá Microsoft sem kallast LUIS (Language Understanding Intelligent Service).</span><span class="sxs-lookup"><span data-stu-id="2f7d8-149">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="2f7d8-150">Lesa meira um LUIS  [hér](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="2f7d8-150">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="2f7d8-151">LUIS-þjónustan ræður úr eða skilur ásetning notanda (í þessu tilviki er ætlunin að finna upplýsingar) og markeiningu (í þessu tilviki er tilgreinda einingin reikningur sem heitir Contoso).</span><span class="sxs-lookup"><span data-stu-id="2f7d8-151">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="2f7d8-152">Þessar upplýsingar eru svo sendar í Microsoft [Azure þjarkaramma](https://azure.microsoft.com/services/bot-service/) sem vinnur með gögn úr Dynamics 365 Human Resources og sækir æskilegar upplýsingum fyrir fyrirspurn notanda.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-152">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="2f7d8-153">Með því að setja upp og leyfa aðgang að þjarkanum samþykkir þú að leyfa LUIS-þjónustunni og Azure þjarkaramma að vinna úr ásetningi á bak við fyrirspurn, sem leiðir til betri notandaupplifunar.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-153">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="2f7d8-154">LUIS-þjónustan og Azure þjarkaramminn kunna að hafa mismikið samræmi samanborið við Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-154">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="2f7d8-155">LUIS-þjónustan hefur aðeins aðgang að fyrirspurnum notenda og er ekki hönnuð til að tengjast við Dynamics 365 Human Resources gögn eða reikning. Notandi Dynamics 365 Human Resources þjarkans gæti fært inn fyrirspurn sem inniheldur gögn viðskiptavinar, persónuleg gögn eða önnur gögn og slíkt fyrirspurnarefni gæti verið sent til LUIS-þjónustunnar og Azure þjarkarammans.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-155">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="2f7d8-156">Innihald fyrirspurna og skilaboða notanda er vistað í LUIS-kerfi í að hámarki 30 daga, er dulkóðað þegar ekki í notkun og er ekki notað fyrir þjálfun eða endurbætur á þjónustu.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-156">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="2f7d8-157">Lestu meira um Cognitive Services  [hér](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="2f7d8-157">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="2f7d8-158">Til að stjórna stjórnandastillingum fyrir forrit í Microsoft Teams er farið í [Microsoft Teams stjórnendamiðstöð](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="2f7d8-158">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="2f7d8-159">Microsoft Teams, hnitanet Azure-tilviks og Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="2f7d8-159">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="2f7d8-160">Þegar Dynamics 365 Human Resources-forritið er notað í Microsoft Teams geta tiltekin gögn um viðskiptavini flætt út fyrir landsvæðið þar sem biðlari Human Resources þjónustunnar er notaður.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-160">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="2f7d8-161">Dynamics 365 Human Resources sendir upplýsingar um leyfisbeiðni og verkflæðisverk til Microsoft Azure tilviks hnitanets og Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-161">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="2f7d8-162">Þessi gögn má geyma í Microsoft Azure Event Grid í allt að sólarhring og verða unnin í Bandaríkjunum, þau er dulkóðuð í flutningi og í hvíld, og eru ekki notuð af Microsoft eða meðhöndlunaraðilum fyrir þjálfun eða þjónustuúrbætur.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-162">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="2f7d8-163">Til að skilja hvar gögnin þín eru geymd í Teams skaltu skoða: [Staðsetning gagna í Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="2f7d8-163">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="2f7d8-164">Í samskiptum við spjallarann í forriti Human Resources, er hægt að geyma innihald samtalsins í Azure Cosmos DB og flytja það yfir í Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-164">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="2f7d8-165">Þessi gögn má geyma í Azure Cosmos DB í allt að sólarhring og kunna að vera meðhöndluð utan staðsetningarinnar þar sem Human Resources-þjónusta leigjandans er uppsett, þau er dulkóðuð í flutningi og í hvíld, og eru ekki notuð af Microsoft eða meðhöndlunaraðilum fyrir þjálfun eða þjónustuúrbætur.</span><span class="sxs-lookup"><span data-stu-id="2f7d8-165">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="2f7d8-166">Til að skilja hvar gögnin þín eru geymd í Teams skaltu skoða: [Staðsetning gagna í Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="2f7d8-166">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="2f7d8-167">Til að takmarka aðgang að Human Resources í Microsoft Teams fyrir fyrirtækið þitt eða notendur innan fyrirtækisins skal skoða [Stjórna reglum um forritsheimildir í Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="2f7d8-167">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="2f7d8-168">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="2f7d8-168">See also</span></span> 

[<span data-ttu-id="2f7d8-169">Sækja og setja upp Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="2f7d8-169">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="2f7d8-170">Microsoft Teams hjálparmiðstöð</span><span class="sxs-lookup"><span data-stu-id="2f7d8-170">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="2f7d8-171">Stjórna leyfisbeiðnum í Teams</span><span class="sxs-lookup"><span data-stu-id="2f7d8-171">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

