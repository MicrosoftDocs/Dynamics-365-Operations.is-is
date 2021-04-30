---
title: Ákvæði Microsoft Teams frá Dynamics 365 Commerce
description: Þetta efnisatriði lýsir því hvernig á að úthluta Microsoft Teams með því að nota fyrirtækisgögn frá Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ba7c74942735b723d1015dc4da0068fbb631bc6b
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908905"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a><span data-ttu-id="38a87-103">Ákvæði Microsoft Teams frá Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="38a87-103">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="38a87-104">Þetta efnisatriði lýsir því hvernig á að úthluta Microsoft Teams með því að nota fyrirtækisgögn frá Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="38a87-104">This topic describes how to provision Microsoft Teams by using organizational data from Dynamics 365 Commerce.</span></span>

<span data-ttu-id="38a87-105">Dynamics 365 Commerce býður upp á einfalda leið til að úthluta Teams ef ekki er enn búið að setja upp teymi fyrir smásöluverslanir.</span><span class="sxs-lookup"><span data-stu-id="38a87-105">Dynamics 365 Commerce offers an easy way to provision Teams if you haven't yet set up teams for your retail stores there.</span></span> <span data-ttu-id="38a87-106">Með því að nýta sér vel skilgreindar upplýsingar úr Commerce sem ætlunin er að nota í Teams er hægt að aðstoða starfsfólk verslunar að koma sér af stað í Teams.</span><span class="sxs-lookup"><span data-stu-id="38a87-106">By taking advantage of well-defined information from Commerce that you want to use in Teams, you can help your store employees get started in Teams.</span></span> <span data-ttu-id="38a87-107">Þessar upplýsingar fela í sér stigveldi fyrirtækis, heiti verslana, upplýsingar um starfsfólk og Azure Active Directory (Azure AD) reikninga.</span><span class="sxs-lookup"><span data-stu-id="38a87-107">This information includes the organizational hierarchy, store names, employee information, and Azure Active Directory (Azure AD) accounts.</span></span> 

<span data-ttu-id="38a87-108">Ferlið við að úthluta Teams felur í sér tvö meginskref:</span><span class="sxs-lookup"><span data-stu-id="38a87-108">The process of provisioning Teams has two main steps:</span></span>

1. <span data-ttu-id="38a87-109">Í Teams skal stofna teymi fyrir hverja smásöluverslun og bæta starfsfólki verslunar við sem meðlimum í viðeigandi teymi.</span><span class="sxs-lookup"><span data-stu-id="38a87-109">In Teams, create a team for each retail store, and add store workers as members of the appropriate team.</span></span> <span data-ttu-id="38a87-110">Ef starfsmaður tengist fleiri en einni smásöluverslun mun teymisaðild sýna þá staðreynd.</span><span class="sxs-lookup"><span data-stu-id="38a87-110">If an employee is associated with more than one retail store, team membership will reflect that fact.</span></span> <span data-ttu-id="38a87-111">Samskiptateymi sem inniheldur svæðisstjóra sem meðlimi verður stofnað til að stuðla að útgáfu verka úr Teams.</span><span class="sxs-lookup"><span data-stu-id="38a87-111">A communications team that includes regional managers as members will be created to help publish tasks from Teams.</span></span>
1. <span data-ttu-id="38a87-112">Hlaðið upp stigveldi fyrirtækis úr Commerce yfir í Teams.</span><span class="sxs-lookup"><span data-stu-id="38a87-112">Upload your organizational hierarchy from Commerce to Teams.</span></span>

## <a name="provision-teams-in-commerce-headquarters"></a><span data-ttu-id="38a87-113">Ráðstafa Teams í Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="38a87-113">Provision Teams in Commerce headquarters</span></span>

<span data-ttu-id="38a87-114">Áður en Microsoft Teams er úthlutað skal ljúka þessum verkum:</span><span class="sxs-lookup"><span data-stu-id="38a87-114">Before you provision Microsoft Teams, complete these tasks:</span></span>

- <span data-ttu-id="38a87-115">Gangið úr skugga um að allir svæðisstjórar hafi verið gerðir að samskiptastjórum.</span><span class="sxs-lookup"><span data-stu-id="38a87-115">Confirm that all regional managers have been made communications managers.</span></span>
- <span data-ttu-id="38a87-116">Staðfestið að Azure-reikningur allra verslunarstjóra og starfsfólks hafi verið tengdur við starfsmannaskrá yfirmanns eða starfsmanns í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="38a87-116">Confirm that the Azure account of every store manager and worker has been associated with that manager's or worker's worker record in Commerce headquarters.</span></span>

<span data-ttu-id="38a87-117">Til að úthluta Teams í Commerce Headquarters skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="38a87-117">To provision Teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="38a87-118">Opnið **Smásala og viðskipti \> Uppsetning rásar \> Microsoft Teams Samþættingarskilgreining**.</span><span class="sxs-lookup"><span data-stu-id="38a87-118">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="38a87-119">Á aðgerðasvæðinu skal velja **Úthluta teymum**.</span><span class="sxs-lookup"><span data-stu-id="38a87-119">On the Action Pane, select **Provision teams**.</span></span> <span data-ttu-id="38a87-120">Runuvinnsla sem kallast **Úthlutun Teams** er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="38a87-120">A batch job that is named **Teams provision** is created.</span></span>
1. <span data-ttu-id="38a87-121">Farið í **Kerfisstjórnun \> Fyrirspurnir \> Runuvinnslur** og finnið nýlegustu vinnuna sem er með lýsinguna **Úthlutun Teams**.</span><span class="sxs-lookup"><span data-stu-id="38a87-121">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="38a87-122">Bíðið þar til verkið hefur verið keyrt.</span><span class="sxs-lookup"><span data-stu-id="38a87-122">Wait until this job has finished running.</span></span>

> [!TIP]
> <span data-ttu-id="38a87-123">Ef engum svæðisstjóra, verslunarstjóra eða starfsmanni verslunar hefur verið tengdur við Teams-leyfi gæti komið upp eftirfarandi villuboð: „Ekki tókst að sækja viðeigandi Sku-flokk fyrir notanda.“</span><span class="sxs-lookup"><span data-stu-id="38a87-123">If none of your regional managers, store managers, and store workers have been associated with a Teams license, you might receive the following error message: "Failed to retrieve appliable Sku categories for the user."</span></span> <span data-ttu-id="38a87-124">Til að lagfæra vandamálið skal velja **Samstilla teymi og meðlimi** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="38a87-124">To correct the issue, select **Sync teams and members** on the Action Pane.</span></span>

<!-- ![Dynamics 365 Commerce - Teams integration configuration](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a><span data-ttu-id="38a87-125">Staðfesta úthlutun Teams í stjórnendamiðstöð Teams</span><span class="sxs-lookup"><span data-stu-id="38a87-125">Validate Teams provisioning in the Teams admin center</span></span>

<span data-ttu-id="38a87-126">Til að staðfesta úthlutun Microsoft Teams í stjórnendamiðstöð Microsoft Teams skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="38a87-126">To validate Microsoft Teams provisioning in the Microsoft Teams admin center, follow these steps.</span></span>
    
1. <span data-ttu-id="38a87-127">Farið í [Stjórnendamiðstöð Teams](https://admin.teams.microsoft.com/) og skráið ykkur inn sem stjórnandi leigjanda rafrænna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="38a87-127">Go to the [Teams admin center](https://admin.teams.microsoft.com/), and sign in as the administrator of your e-commerce tenant.</span></span>
1. <span data-ttu-id="38a87-128">Á svæðinu vinstra megin skal velja **Teymi** til að stækka það og velja því næst **Stjórna teymum**.</span><span class="sxs-lookup"><span data-stu-id="38a87-128">In the left navigation pane, select **Teams** to expand it, and then select **Manage teams**.</span></span>
1. <span data-ttu-id="38a87-129">Staðfestið að eitt teymi hafi verið stofnað fyrir hverja smásöluverslun Commerce.</span><span class="sxs-lookup"><span data-stu-id="38a87-129">Confirm that one team has been created for each Commerce retail store.</span></span>
1. <span data-ttu-id="38a87-130">Veljið teymi og staðfestið að starfsmönnum verslunar hafi verið bætt við sem meðlimum.</span><span class="sxs-lookup"><span data-stu-id="38a87-130">Select a team, and confirm that store workers have been added to it as members.</span></span>
1. <span data-ttu-id="38a87-131">Á svæðinu vinstra megin skal velja **Notendur** og staðfesta að öllum starfsmönnum verslunar í öllum verslunum hafi verið bætt við sem notendum.</span><span class="sxs-lookup"><span data-stu-id="38a87-131">In the left navigation pane, select **Users**, and confirm that all store employees in all stores have been added as users.</span></span>

<span data-ttu-id="38a87-132">Eftirfarandi mynd sýnir dæmi um síðuna **Stjórna teymum** í stjórnendamiðstöð Teams.</span><span class="sxs-lookup"><span data-stu-id="38a87-132">The following illustration shows an example of the **Manage teams** page in the Teams admin center.</span></span>

![Dæmi um síðuna Stjórna teymum í stjórnendamiðstöð Teams](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a><span data-ttu-id="38a87-134">Hlaða upp fyrirtækisstigveldi Commerce í Teams</span><span class="sxs-lookup"><span data-stu-id="38a87-134">Upload a Commerce organizational hierarchy to Teams</span></span>
    
<span data-ttu-id="38a87-135">Hægt er að nota fyrirtækisstigveldi Commerce í Microsoft Teams til að gefa verk út til allra eða valdra verslana sem nota sama fyrirtækisstigveldið.</span><span class="sxs-lookup"><span data-stu-id="38a87-135">The Commerce organizational hierarchy can be used in Microsoft Teams to publish tasks to all or selected stores that use the same hierarchy structure.</span></span>

<span data-ttu-id="38a87-136">Til að hlaða upp fyrirtækisstigveldi Commerce í Teams skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="38a87-136">To upload a Commerce organizational hierarchy to Teams, follow these steps.</span></span>
    
1. <span data-ttu-id="38a87-137">Í Commerce Headquarters skal fara í **Smásala og viðskipti \> Uppsetning rásar \> Microsoft Teams Samþættingarskilgreining**.</span><span class="sxs-lookup"><span data-stu-id="38a87-137">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="38a87-138">Veljið **Sækja markstigveldi** og veljið því næst **Smásöluverslanir eftir svæði** til að sækja CSV-skrá með gildum sem eru aðskilin með kommu fyrir stigveldi fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="38a87-138">Select **Download targeting hierarchy**, and then select **Retail Stores by Region** to download a comma-separated values (CSV) file of the organizational hierarchy.</span></span>
1. <span data-ttu-id="38a87-139">Setjið upp einingu Microsoft Teams PowerShell með því að fylgja skrefunum í [Setja upp Microsoft Teams PowerShell](https://docs.microsoft.com/microsoftteams/teams-powershell-install).</span><span class="sxs-lookup"><span data-stu-id="38a87-139">Install the Microsoft Teams PowerShell module by following the steps in [Install Microsoft Teams PowerShell](https://docs.microsoft.com/microsoftteams/teams-powershell-install).</span></span>
1. <span data-ttu-id="38a87-140">Þegar beðið er um það í glugga Teams PowerShell skal skrá sig inn í gegnum stjórnendareikninginn fyrir leigjanda Azure AD.</span><span class="sxs-lookup"><span data-stu-id="38a87-140">When you're prompted in the Teams PowerShell window, sign in by using the administrator account for your Azure AD tenant.</span></span>
1. <span data-ttu-id="38a87-141">Fylgið skrefunum í [Setja upp markstigveldi teymisins](https://docs.microsoft.com/microsoftteams/set-up-your-team-hierarchy) til að hlaða upp CSV-skránni fyrir markstigveldið.</span><span class="sxs-lookup"><span data-stu-id="38a87-141">Follow the steps in [Set up your team targeting hierarchy](https://docs.microsoft.com/microsoftteams/set-up-your-team-hierarchy) to upload the CSV file for the targeting hierarchy.</span></span>

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a><span data-ttu-id="38a87-142">Staðfesta að stigveldi fyrirtækisins hafi verið hlaðið upp í Teams</span><span class="sxs-lookup"><span data-stu-id="38a87-142">Verify that the organizational hierarchy was uploaded to Teams</span></span>

<span data-ttu-id="38a87-143">Til að staðfesta að stigveldi fyrirtækisins hafi verið hlaðið upp í Microsoft Teams skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="38a87-143">To verify that the organizational hierarchy was uploaded to Microsoft Teams, follow these steps.</span></span>

1. <span data-ttu-id="38a87-144">Skráðu þig inn á Teams sem samskiptastjóra.</span><span class="sxs-lookup"><span data-stu-id="38a87-144">Sign in to Teams as a communications manager.</span></span>
1. <span data-ttu-id="38a87-145">Á yfirlitssvæðinu vinstra megin skal velja **Verk eftir Planner**.</span><span class="sxs-lookup"><span data-stu-id="38a87-145">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="38a87-146">Í flipanum **Útgefnir listar** skal búa til nýjan lista sem er með prufuverk.</span><span class="sxs-lookup"><span data-stu-id="38a87-146">On the **Published lists** tab, create a new list that has a dummy task.</span></span>
1. <span data-ttu-id="38a87-147">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="38a87-147">Select **Publish**.</span></span> <span data-ttu-id="38a87-148">Stigveldi fyrirtækisins ætti að birtast í svarglugganum **Velja hverjum á að birta** eins og sýnt er í dæminu í eftirfarandi skýringarmynd.</span><span class="sxs-lookup"><span data-stu-id="38a87-148">The organizational hierarchy should appear in the **Select who to publish to** dialog box, as shown in the example in the following illustration.</span></span>

![Dæmi um stigveldi fyrirtækis í svarglugganum Velja hverjum á að birta](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a><span data-ttu-id="38a87-150">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="38a87-150">Additional resources</span></span>

[<span data-ttu-id="38a87-151">Dynamics 365 Commerce og Microsoft Teams samþættingaryfirlit</span><span class="sxs-lookup"><span data-stu-id="38a87-151">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="38a87-152">Gera Dynamics 365 Commerce og Microsoft Teams samþættingu virka</span><span class="sxs-lookup"><span data-stu-id="38a87-152">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="38a87-153">Samstilla verkstjórnun á milli Microsoft Teams og Dynamics 365 Commerce sölustaðar</span><span class="sxs-lookup"><span data-stu-id="38a87-153">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="38a87-154">Stjórna notandahlutverkum í Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="38a87-154">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="38a87-155">Varpa verslunum og teymum ef fyrirliggjandi teymi eru í Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="38a87-155">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="38a87-156">Algengar spurningar um samþættingu Dynamics 365 Commerce og Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="38a87-156">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
