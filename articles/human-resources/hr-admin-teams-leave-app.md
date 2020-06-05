---
title: Forritið „Human Resources“ í Teams
description: Þetta efnisatriði kynnir Microsoft Dynamics 365 Human Resources forritið í Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
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
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 423ec36a73e8af9d915c5cfe16bd4d552448e2b6
ms.sourcegitcommit: d1541831d556b722a71aed442043ffb4a4576d87
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/20/2020
ms.locfileid: "3388117"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="4913f-103">Forritið „Human Resources“ í Teams</span><span class="sxs-lookup"><span data-stu-id="4913f-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="4913f-104">Microsoft Dynamics 365 Human Resources forritið í Microsoft Teams gerir starfsmönnum kleift að biðja um frí og skoða upplýsinga um frítíma á fljótlegan hátt í Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="4913f-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="4913f-105">Starsmenn geta haft samband við þjarka til að óska eftir upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="4913f-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="4913f-106">Finna má ítarlegri upplýsingar á flipanum **Frí**.</span><span class="sxs-lookup"><span data-stu-id="4913f-106">The **Time off** tab provides more detailed information.</span></span>

![Human Resources Teams þjarkaforrit fyrir leyfi](./media/hr-admin-teams-leave-app-bot.png)

![Fríflipi fyrir fríforrit Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a><span data-ttu-id="4913f-109">Setja upp</span><span class="sxs-lookup"><span data-stu-id="4913f-109">Install and setup</span></span>

<span data-ttu-id="4913f-110">Hægt er að finna forritið Human Resources í Teams versluninni.</span><span class="sxs-lookup"><span data-stu-id="4913f-110">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="4913f-111">Frekari upplýsingar um uppsetningu á Teams-forritinu má finna í [Stjórna leyfisbeiðnum í Teams](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="4913f-111">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="4913f-112">Frekari upplýsingar um stjórnun forritsheimilda í Teams er að finna í [Stjórna reglum forritaheimilda í Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="4913f-112">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="known-issues"></a><span data-ttu-id="4913f-113">Þekkt vandamál</span><span class="sxs-lookup"><span data-stu-id="4913f-113">Known issues</span></span>

| <span data-ttu-id="4913f-114">Úthreyfing</span><span class="sxs-lookup"><span data-stu-id="4913f-114">Issue</span></span> | <span data-ttu-id="4913f-115">Staða</span><span class="sxs-lookup"><span data-stu-id="4913f-115">Status</span></span> |
| --- | --- |
| <span data-ttu-id="4913f-116">Staðan er röng þegar sendur er frítími fyrir dagsetningu í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="4913f-116">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="4913f-117">Spár eru ekki enn til staðar.</span><span class="sxs-lookup"><span data-stu-id="4913f-117">Forecasting isn't yet available.</span></span> <span data-ttu-id="4913f-118">Staðan birtist fyrir núverandi dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="4913f-118">The balance displays for the current date.</span></span> |
| <span data-ttu-id="4913f-119">Þegar tekinn fjöldi stunda er minnkaður í fyrirliggjandi beiðni fer **Eftirstandandi staða** niður í stað þess að fara upp.</span><span class="sxs-lookup"><span data-stu-id="4913f-119">When reducing the number of hours taken in an existing request, the **Remaining balance** goes down instead of up.</span></span> | <span data-ttu-id="4913f-120">Við munum leysa úr þessu vandamáli í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="4913f-120">We'll address this known issue in the future.</span></span> <span data-ttu-id="4913f-121">Birting er röng, en réttar upphæðir eru leiðréttar við sendingu.</span><span class="sxs-lookup"><span data-stu-id="4913f-121">The display is incorrect, but the correct amounts are adjusted upon submission.</span></span> |
| <span data-ttu-id="4913f-122">Tvö **Væntanlegt frí** kort birtast fyrir sömu dagsetningar.</span><span class="sxs-lookup"><span data-stu-id="4913f-122">Two **Upcoming time off** cards display for the same dates.</span></span> | <span data-ttu-id="4913f-123">Kortin tákna einstakar sendingar.</span><span class="sxs-lookup"><span data-stu-id="4913f-123">The cards represent individual submissions.</span></span> <span data-ttu-id="4913f-124">Við munum halda áfram að taka við ábendingum og gera breytingar.</span><span class="sxs-lookup"><span data-stu-id="4913f-124">We'll continue to take feedback and make adjustments.</span></span> |
| <span data-ttu-id="4913f-125">Ekki er hægt að hætta við beiðni með stöðuna **Í yfirferð**.</span><span class="sxs-lookup"><span data-stu-id="4913f-125">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="4913f-126">Þessi eiginleiki er ekki studdur eins og er og honum verður bætt við í síðari tíma útgáfum.</span><span class="sxs-lookup"><span data-stu-id="4913f-126">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="4913f-127">Upplýsingar um stöðu eru reiknaðar frá og með deginum í dag.</span><span class="sxs-lookup"><span data-stu-id="4913f-127">Balance information is calculated as of today.</span></span> | <span data-ttu-id="4913f-128">Kerfið sýnir eins og er ekki stöður frá uppsöfnunartímabilinu, jafnvel þótt það sé skilgreint í færibreytum leyfis og fjarvista.</span><span class="sxs-lookup"><span data-stu-id="4913f-128">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="4913f-129">Tilkynning um persónuvernd</span><span class="sxs-lookup"><span data-stu-id="4913f-129">Privacy notice</span></span>

<span data-ttu-id="4913f-130">Með Dynamics 365 Human Resources þjarkanum í Microsoft Teams er texti notanda greindur til að skilja undirliggjandi fyrirspurn/ásetning.</span><span class="sxs-lookup"><span data-stu-id="4913f-130">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="4913f-131">Inntak notanda á borð við „Leita í contoso reikningi“ er flutt í eina af Cognitive Service hjá Microsoft sem kallast LUIS (Language Understanding Intelligent Service).</span><span class="sxs-lookup"><span data-stu-id="4913f-131">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="4913f-132">Lesa meira um LUIS  [hér](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="4913f-132">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="4913f-133">LUIS-þjónustan ræður úr eða skilur ásetning notanda (í þessu tilviki er ætlunin að finna upplýsingar) og markeiningu (í þessu tilviki er tilgreinda einingin reikningur sem heitir Contoso).</span><span class="sxs-lookup"><span data-stu-id="4913f-133">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="4913f-134">Þessar upplýsingar eru svo sendar í Microsoft  [Azure þjarkaramma](https://azure.microsoft.com/services/bot-service/) sem vinnur með gögn úr Dynamics 365 Human Resources og sækir æskilegar upplýsingum fyrir fyrirspurn notanda.</span><span class="sxs-lookup"><span data-stu-id="4913f-134">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/) which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="4913f-135">Með því að setja upp og leyfa aðgang að þjarkanum samþykkir þú að leyfa LUIS-þjónustunni og Azure þjarkaramma að vinna úr ásetningi á bak við fyrirspurn, sem leiðir til betri notandaupplifunar.</span><span class="sxs-lookup"><span data-stu-id="4913f-135">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="4913f-136">LUIS-þjónustan og Azure þjarkaramminn kunna að hafa mismikið samræmi samanborið við Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4913f-136">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="4913f-137">LUIS-þjónustan hefur aðeins aðgang að fyrirspurnum notenda og er ekki hönnuð til að tengjast við Dynamics 365 Human Resources gögn eða reikning. Notandi Dynamics 365 Human Resources þjarkans gæti fært inn fyrirspurn sem inniheldur gögn viðskiptavinar, persónuleg gögn eða önnur gögn og slíkt fyrirspurnarefni gæti verið sent til LUIS-þjónustunnar og Azure þjarkarammans.</span><span class="sxs-lookup"><span data-stu-id="4913f-137">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="4913f-138">Innihald fyrirspurna og skilaboða notanda er vistað í LUIS-kerfi í að hámarki 30 daga, er dulkóðað þegar ekki í notkun og er ekki notað fyrir þjálfun eða endurbætur á þjónustu.</span><span class="sxs-lookup"><span data-stu-id="4913f-138">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="4913f-139">Lestu meira um Cognitive Services  [hér](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="4913f-139">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="4913f-140">Til að stjórna stjórnandastillingum fyrir forrit í Microsoft Teams er farið í [Microsoft Teams stjórnendamiðstöð](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="4913f-140">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span> 

## <a name="see-also"></a><span data-ttu-id="4913f-141">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="4913f-141">See also</span></span> 

[<span data-ttu-id="4913f-142">Sækja og setja upp Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="4913f-142">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="4913f-143">Microsoft Teams hjálparmiðstöð</span><span class="sxs-lookup"><span data-stu-id="4913f-143">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="4913f-144">Stjórna leyfisbeiðnum í Teams</span><span class="sxs-lookup"><span data-stu-id="4913f-144">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

