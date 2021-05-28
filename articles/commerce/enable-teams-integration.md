---
title: Gera Dynamics 365 Commerce og Microsoft Teams samþættingu virka
description: Þetta efnisatriði lýsir hvernig á að virkja Microsoft Dynamics 365 Commerce og Microsoft Teams samþættingu.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eb0b8b419b302fbd0bc107bca22f8b26774ba3c7
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019836"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a><span data-ttu-id="2159c-103">Gera Dynamics 365 Commerce og Microsoft Teams samþættingu virka</span><span class="sxs-lookup"><span data-stu-id="2159c-103">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2159c-104">Þetta efnisatriði lýsir hvernig á að virkja Microsoft Dynamics 365 Commerce og Microsoft Teams samþættingu.</span><span class="sxs-lookup"><span data-stu-id="2159c-104">This topic describes how to enable Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="2159c-105">Til að úthluta Teams með upplýsingum frá Dynamics 365 Commerce og samstilla eiginleika verkstjórnunar milli Teams og forrits sölustaðar, þarf að virkja samþættingareiginleikana í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="2159c-105">To provision Teams with information from Dynamics 365 Commerce and synchronize the task management features between Teams and the point of sale (POS) application, you must enable the integration features in Commerce headquarters.</span></span>

> [!NOTE]
> <span data-ttu-id="2159c-106">Með því að virkja Teams samþættingu samþykkir notandi að deila gögnum með Teams.</span><span class="sxs-lookup"><span data-stu-id="2159c-106">When you enable Teams integration, you consent to share your data with Teams.</span></span> <span data-ttu-id="2159c-107">Gögnum sem deilt er með Teams gætu verið geymd í öðru landi en gögnin í Commerce og gætu því fallið undir aðrar reglugerðir.</span><span class="sxs-lookup"><span data-stu-id="2159c-107">Data that is shared with Teams might reside in a different country than your Commerce data, and it might be subject to different compliance standards.</span></span> <span data-ttu-id="2159c-108">Frekari upplýsingar eru í [Öryggismiðstöð Microsoft](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="2159c-108">For more information, see the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="2159c-109">Upplýsingar um persónuverndarstefnur Microsoft er að finna í [Persónuverndaryfirlýsing Microsoft](https://aka.ms/privacy).</span><span class="sxs-lookup"><span data-stu-id="2159c-109">For information about Microsoft privacy policies, see the [Microsoft Privacy Statement](https://aka.ms/privacy).</span></span>

## <a name="enable-teams-integration"></a><span data-ttu-id="2159c-110">Virkja samþættingu Teams</span><span class="sxs-lookup"><span data-stu-id="2159c-110">Enable Teams integration</span></span>

<span data-ttu-id="2159c-111">Áður en hægt er að virkja samþættingu Microsoft Teams við Commerce þarf að skrá Teams-forritið með leigjandanum í Azure-gáttinni.</span><span class="sxs-lookup"><span data-stu-id="2159c-111">Before you can enable Microsoft Teams integration with Commerce, you must register the Teams application with your tenant in the Azure portal.</span></span>

<span data-ttu-id="2159c-112">Til að skrá Teams-forritið með leigjandanum í Azure-gáttinni skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="2159c-112">To register the Teams application with your tenant in the Azure portal, follow these steps.</span></span>

1. <span data-ttu-id="2159c-113">Fylgið skrefunum í [Stuttar leiðbeiningar: Skrá forrit á verkvangi Microsoft](/azure/active-directory/develop/quickstart-register-app) til að skrá Teams-forritið með leigjandanum í Azure-gáttinni.</span><span class="sxs-lookup"><span data-stu-id="2159c-113">Follow the steps in [Quickstart: Register an app in the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to register the Teams application with your tenant in the Azure portal.</span></span>
1. <span data-ttu-id="2159c-114">Afritið gildið **Forritskenni (biðlarakenni)** af síðunni **Yfirlit** fyrir skráð forrit.</span><span class="sxs-lookup"><span data-stu-id="2159c-114">Copy the **Application (client) ID** value from the **Overview** page for the registered app.</span></span> <span data-ttu-id="2159c-115">Þetta gildi er notað til að virkja Teams samþættingu í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="2159c-115">You will use this value to enable Teams integration in Commerce headquarters.</span></span>
1. <span data-ttu-id="2159c-116">Afritið gildi vottorðs sem slegið var inn þegar [vottorði var bætt við](/azure/active-directory/develop/quickstart-register-app#add-a-certificate) í skrefi 1.</span><span class="sxs-lookup"><span data-stu-id="2159c-116">Copy the certificate value that was entered when you [added a certificate](/azure/active-directory/develop/quickstart-register-app#add-a-certificate) in step 1.</span></span> <span data-ttu-id="2159c-117">Vottorðið er einnig þekkt sem almennur lykill eða forritalykill.</span><span class="sxs-lookup"><span data-stu-id="2159c-117">The certificate is also known as the public key or application key.</span></span> <span data-ttu-id="2159c-118">Þetta gildi er notað til að virkja Teams samþættingu í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="2159c-118">You will use this value to enable Teams integration in Commerce headquarters.</span></span>

<span data-ttu-id="2159c-119">Fylgja skal eftirfarandi skrefum til að óvirkja Teams samþættingu í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="2159c-119">To enable Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="2159c-120">Opnið **Retail og Commerce\> Uppsetning rásar \> Microsoft Teams Samþættingarskilgreining**.</span><span class="sxs-lookup"><span data-stu-id="2159c-120">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams integration configuration**.</span></span>
1. <span data-ttu-id="2159c-121">Á aðgerðarúðunni skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="2159c-121">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="2159c-122">Stillið **Virkja Microsoft Teams-samþættingu** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="2159c-122">Set the **Enable Microsoft Teams integration** option to **Yes**.</span></span>
1. <span data-ttu-id="2159c-123">Í reitina **Forritskenni** og **Forritslykill** skal slá inn gildin sem fengin voru þegar Teams-forritið var skráð í Azure-gáttinni.</span><span class="sxs-lookup"><span data-stu-id="2159c-123">In the **Application ID** and **Application key** fields, enter the values you obtained when you registered the Teams application in the Azure portal.</span></span>
1. <span data-ttu-id="2159c-124">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="2159c-124">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="2159c-125">Eftirfarandi mynd sýnir dæmi um skilgreiningar Teams samþættingar í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="2159c-125">The following illustration shows an example of the configuration of Teams integration in Commerce headquarters.</span></span>

![Samþættingarskilgreining Teams í Commerce Headquarters](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a><span data-ttu-id="2159c-127">Óvirkja samþættingu Teams</span><span class="sxs-lookup"><span data-stu-id="2159c-127">Disable Teams integration</span></span>

<span data-ttu-id="2159c-128">Fylgja skal eftirfarandi skrefum til að óvirkja Microsoft Teams samþættingu í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="2159c-128">To disable Microsoft Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="2159c-129">Opnið **Smásala og viðskipti \> Uppsetning rásar \> Microsoft Teams Samþættingarskilgreining**.</span><span class="sxs-lookup"><span data-stu-id="2159c-129">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="2159c-130">Á aðgerðarúðunni skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="2159c-130">On the Action Pane, select **Edit**.</span></span>
3. <span data-ttu-id="2159c-131">Stillið valkostinn **Virkja Microsoft Teams-samþættingu** á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="2159c-131">Set the **Enable Microsoft Teams integration** option to **No**.</span></span>
4. <span data-ttu-id="2159c-132">Hreinsið gildin í reitunum **Forritskenni** og **Forritslykill**.</span><span class="sxs-lookup"><span data-stu-id="2159c-132">Clear the values from the **Application ID** and **Application Key** fields.</span></span>
1. <span data-ttu-id="2159c-133">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="2159c-133">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="2159c-134">Þegar slökkt er á samþættingu Teams við Commerce sýna afgreiðslukassar ekki lengur verk sem Teams-forritið gefur út.</span><span class="sxs-lookup"><span data-stu-id="2159c-134">After you disable Teams integration with Commerce, POS terminals will no longer show tasks that are published from the Teams application.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2159c-135">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="2159c-135">Additional resources</span></span>

[<span data-ttu-id="2159c-136">Dynamics 365 Commerce og Microsoft Teams samþættingaryfirlit</span><span class="sxs-lookup"><span data-stu-id="2159c-136">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="2159c-137">Ákvæði Microsoft Teams frá Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="2159c-137">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="2159c-138">Samstilla verkstjórnun á milli Microsoft Teams og Dynamics 365 Commerce sölustaðar</span><span class="sxs-lookup"><span data-stu-id="2159c-138">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="2159c-139">Stjórna notandahlutverkum í Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="2159c-139">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="2159c-140">Varpa verslunum og teymum ef fyrirliggjandi teymi eru í Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="2159c-140">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="2159c-141">Algengar spurningar um samþættingu Dynamics 365 Commerce og Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="2159c-141">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)