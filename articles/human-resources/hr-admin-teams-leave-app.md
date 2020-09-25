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
ms.openlocfilehash: a022f8297066793080d254baa01410884a3fafd9
ms.sourcegitcommit: 55b729361ea852e38531c51972c6730e3d9c2b45
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/08/2020
ms.locfileid: "3776309"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="282c6-103">Forritið „Human Resources“ í Teams</span><span class="sxs-lookup"><span data-stu-id="282c6-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="282c6-104">Microsoft Dynamics 365 Human Resources forritið í Microsoft Teams gerir starfsmönnum kleift að biðja um frí og skoða upplýsinga um frítíma á fljótlegan hátt í Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="282c6-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="282c6-105">Starsmenn geta haft samband við þjarka til að óska eftir upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="282c6-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="282c6-106">Finna má ítarlegri upplýsingar á flipanum **Frí**.</span><span class="sxs-lookup"><span data-stu-id="282c6-106">The **Time off** tab provides more detailed information.</span></span>

![Human Resources Teams þjarkaforrit fyrir leyfi](./media/hr-admin-teams-leave-app-bot.png)

![Fríflipi fyrir fríforrit Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a><span data-ttu-id="282c6-109">Setja upp</span><span class="sxs-lookup"><span data-stu-id="282c6-109">Install and setup</span></span>

<span data-ttu-id="282c6-110">Hægt er að finna forritið Human Resources í Teams versluninni.</span><span class="sxs-lookup"><span data-stu-id="282c6-110">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="282c6-111">Frekari upplýsingar um uppsetningu á Teams-forritinu má finna í [Stjórna leyfisbeiðnum í Teams](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="282c6-111">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="282c6-112">Frekari upplýsingar um stjórnun forritsheimilda í Teams er að finna í [Stjórna reglum forritaheimilda í Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="282c6-112">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="282c6-113">Kveikja á tilkynningum fyrir forritið „Human Resources“ í Teams</span><span class="sxs-lookup"><span data-stu-id="282c6-113">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="282c6-114">Ef notendur eiga að fá tilkynningar vegna leyfisbeiðna í Teams-forritinu verður að virkja tilkynningar í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="282c6-114">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="282c6-115">Aðeins notendur sem eru skráðir inn í Teams og nota Human Resources Teams-forritið fá tilkynningar.</span><span class="sxs-lookup"><span data-stu-id="282c6-115">Only users who are signed into Teams and using the Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="282c6-116">Veldu í Human Resources **Kerfisstjórnun**.</span><span class="sxs-lookup"><span data-stu-id="282c6-116">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="282c6-117">Veljið **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="282c6-117">Select **Links**.</span></span>

3. <span data-ttu-id="282c6-118">Undir **Uppsetning**, skal velja **Kerfisfæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="282c6-118">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="282c6-119">Á flipanum **Almennt** skal stilla **Kveikja á tilkynningum fyrir Teams-forritið** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="282c6-119">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Kveikja á tilkynningum fyrir Teams-forrit í kerfisfæribreytum](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="282c6-121">Til að kveikja á tilkynningum Teams fyrir alla notendur skal velja **Já** þegar spurt er um það.</span><span class="sxs-lookup"><span data-stu-id="282c6-121">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Virkja hóptilkynningar fyrir alla notendur](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="282c6-123">Kveikja eða slökkva á hóptilkynningum fyrir einstaka notendur</span><span class="sxs-lookup"><span data-stu-id="282c6-123">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="282c6-124">Þegar búið er að virkja tilkynningar fyrir Human Resources Teams forritið er hægt að kveikja eða slökkva á tilkynningum fyrir einstaka notendur.</span><span class="sxs-lookup"><span data-stu-id="282c6-124">After you've enabled notifications for the Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="282c6-125">Veldu í Human Resources **Kerfisstjórnun**.</span><span class="sxs-lookup"><span data-stu-id="282c6-125">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="282c6-126">Veljið **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="282c6-126">Select **Links**.</span></span>

3. <span data-ttu-id="282c6-127">Undir **Notendur** skal velja **Notandavalkostir**.</span><span class="sxs-lookup"><span data-stu-id="282c6-127">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="282c6-128">Veldu flipann **Verkflæði**.</span><span class="sxs-lookup"><span data-stu-id="282c6-128">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="282c6-129">Stillið **Kveikja á tilkynningum fyrir Teams-forritið** á **Já** til að virkja tilkynningar fyrir notandann eða **Nei** til að gera tilkynningar óvirkar fyrir notandann.</span><span class="sxs-lookup"><span data-stu-id="282c6-129">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Kveikja á tilkynningum Teams-forrits á verkflæðisflipanum Valkostir notanda](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="282c6-131">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="282c6-131">Select **Save**.</span></span>

## <a name="known-issues"></a><span data-ttu-id="282c6-132">Þekkt vandamál</span><span class="sxs-lookup"><span data-stu-id="282c6-132">Known issues</span></span>

| <span data-ttu-id="282c6-133">Úthreyfing</span><span class="sxs-lookup"><span data-stu-id="282c6-133">Issue</span></span> | <span data-ttu-id="282c6-134">Staða</span><span class="sxs-lookup"><span data-stu-id="282c6-134">Status</span></span> |
| --- | --- |
| <span data-ttu-id="282c6-135">Lárétt fletting virkar ekki í Android-símum</span><span class="sxs-lookup"><span data-stu-id="282c6-135">Horizontal scrolling doesn't work on Android phones</span></span> | <span data-ttu-id="282c6-136">Lárétt fletting eru ekki vandamál í iOS eða borðtölvum.</span><span class="sxs-lookup"><span data-stu-id="282c6-136">Horizontal scrolling isn't an issue on iOS or desktop devices.</span></span> <span data-ttu-id="282c6-137">Unnið er að lagfæringu fyrir Android.</span><span class="sxs-lookup"><span data-stu-id="282c6-137">We're working on a fix for Android.</span></span> |
| <span data-ttu-id="282c6-138">Villa: Vandamál kom upp við að finna umhverfi til að tengjast við.</span><span class="sxs-lookup"><span data-stu-id="282c6-138">Error: There is an issue finding an environment to connect to.</span></span> | <span data-ttu-id="282c6-139">Þessi villa gæti komið upp jafnvel þótt búið sé að staðfesta að notandinn megi fá aðgang að einu eða fleiri mannauðsumhverfum.</span><span class="sxs-lookup"><span data-stu-id="282c6-139">You might receive this error even if you've verified that the user can access one or more Human Resources environments.</span></span> <span data-ttu-id="282c6-140">Að auki er ekki víst að öll umhverfin sjáist eins og vonast var eftir.</span><span class="sxs-lookup"><span data-stu-id="282c6-140">Also, you might not see all the environments you expect.</span></span> <span data-ttu-id="282c6-141">Þangað til leyst verður úr þessu vandamáli þarf að eyða notandanum og flytja hann síðan inn aftur til að komast hjá þessum vanda.</span><span class="sxs-lookup"><span data-stu-id="282c6-141">Until we fix this issue, delete the user and then import them in again to resolve the problem.</span></span> |
| <span data-ttu-id="282c6-142">Staðan er röng þegar sendur er frítími fyrir dagsetningu í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="282c6-142">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="282c6-143">Spár eru ekki enn til staðar.</span><span class="sxs-lookup"><span data-stu-id="282c6-143">Forecasting isn't yet available.</span></span> <span data-ttu-id="282c6-144">Staðan birtist fyrir núverandi dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="282c6-144">The balance displays for the current date.</span></span> |
| <span data-ttu-id="282c6-145">Ekki er hægt að hætta við beiðni með stöðuna **Í yfirferð**.</span><span class="sxs-lookup"><span data-stu-id="282c6-145">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="282c6-146">Þessi eiginleiki er ekki studdur eins og er og honum verður bætt við í síðari tíma útgáfum.</span><span class="sxs-lookup"><span data-stu-id="282c6-146">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="282c6-147">Upplýsingar um stöðu eru reiknaðar frá og með deginum í dag.</span><span class="sxs-lookup"><span data-stu-id="282c6-147">Balance information is calculated as of today.</span></span> | <span data-ttu-id="282c6-148">Kerfið sýnir eins og er ekki stöður frá uppsöfnunartímabilinu, jafnvel þótt það sé skilgreint í færibreytum leyfis og fjarvista.</span><span class="sxs-lookup"><span data-stu-id="282c6-148">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="282c6-149">Tilkynning um persónuvernd</span><span class="sxs-lookup"><span data-stu-id="282c6-149">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="282c6-150">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="282c6-150">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="282c6-151">Með Dynamics 365 Human Resources þjarkanum í Microsoft Teams er texti notanda greindur til að skilja undirliggjandi fyrirspurn/ásetning.</span><span class="sxs-lookup"><span data-stu-id="282c6-151">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="282c6-152">Inntak notanda á borð við „Leita í contoso reikningi“ er flutt í eina af Cognitive Service hjá Microsoft sem kallast LUIS (Language Understanding Intelligent Service).</span><span class="sxs-lookup"><span data-stu-id="282c6-152">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="282c6-153">Lesa meira um LUIS  [hér](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="282c6-153">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="282c6-154">LUIS-þjónustan ræður úr eða skilur ásetning notanda (í þessu tilviki er ætlunin að finna upplýsingar) og markeiningu (í þessu tilviki er tilgreinda einingin reikningur sem heitir Contoso).</span><span class="sxs-lookup"><span data-stu-id="282c6-154">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="282c6-155">Þessar upplýsingar eru svo sendar í Microsoft [Azure þjarkaramma](https://azure.microsoft.com/services/bot-service/) sem vinnur með gögn úr Dynamics 365 Human Resources og sækir æskilegar upplýsingum fyrir fyrirspurn notanda.</span><span class="sxs-lookup"><span data-stu-id="282c6-155">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="282c6-156">Með því að setja upp og leyfa aðgang að þjarkanum samþykkir þú að leyfa LUIS-þjónustunni og Azure þjarkaramma að vinna úr ásetningi á bak við fyrirspurn, sem leiðir til betri notandaupplifunar.</span><span class="sxs-lookup"><span data-stu-id="282c6-156">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="282c6-157">LUIS-þjónustan og Azure þjarkaramminn kunna að hafa mismikið samræmi samanborið við Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="282c6-157">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="282c6-158">LUIS-þjónustan hefur aðeins aðgang að fyrirspurnum notenda og er ekki hönnuð til að tengjast við Dynamics 365 Human Resources gögn eða reikning. Notandi Dynamics 365 Human Resources þjarkans gæti fært inn fyrirspurn sem inniheldur gögn viðskiptavinar, persónuleg gögn eða önnur gögn og slíkt fyrirspurnarefni gæti verið sent til LUIS-þjónustunnar og Azure þjarkarammans.</span><span class="sxs-lookup"><span data-stu-id="282c6-158">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="282c6-159">Innihald fyrirspurna og skilaboða notanda er vistað í LUIS-kerfi í að hámarki 30 daga, er dulkóðað þegar ekki í notkun og er ekki notað fyrir þjálfun eða endurbætur á þjónustu.</span><span class="sxs-lookup"><span data-stu-id="282c6-159">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="282c6-160">Lestu meira um Cognitive Services  [hér](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="282c6-160">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="282c6-161">Til að stjórna stjórnandastillingum fyrir forrit í Microsoft Teams er farið í [Microsoft Teams stjórnendamiðstöð](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="282c6-161">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a><span data-ttu-id="282c6-162">Microsoft Azure -Tilvikhnitanet og Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="282c6-162">Microsoft Azure Event Grid and Microsoft Teams</span></span>

<span data-ttu-id="282c6-163">Þegar tilkynningaeiginleiki er notaður fyrir Dynamics 365 Human Resources-forritið í Teams flæð tiltekin gögn um viðskiptavini út fyrir landsvæðið þar sem biðlari Human Resources þjónustunnar ern notaður.</span><span class="sxs-lookup"><span data-stu-id="282c6-163">When using the notifications feature for the Dynamics 365 Human Resources app in Teams, certain customer data will flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span> <span data-ttu-id="282c6-164">Dynamics 365 Human Resources sendir upplýsingar um leyfisbeiðni og verkflæðisverk til Microsoft Azure tilviks hnitanets og Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="282c6-164">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="282c6-165">Þessi gögn kunna að vera geymd í allt að sólarhring og unnin í Bandaríkjunum, þau er dulkóðuð í flutningi og í hvíld, og eru ekki notuð af Microsoft eða meðhöndlunaraðilum fyrir þjálfun eða þjónustuúrbætur.</span><span class="sxs-lookup"><span data-stu-id="282c6-165">This data may be stored for up to 24 hours and processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span>

## <a name="see-also"></a><span data-ttu-id="282c6-166">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="282c6-166">See also</span></span> 

[<span data-ttu-id="282c6-167">Sækja og setja upp Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="282c6-167">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="282c6-168">Microsoft Teams hjálparmiðstöð</span><span class="sxs-lookup"><span data-stu-id="282c6-168">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="282c6-169">Stjórna leyfisbeiðnum í Teams</span><span class="sxs-lookup"><span data-stu-id="282c6-169">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

