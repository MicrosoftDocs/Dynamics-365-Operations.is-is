---
title: Samstilla verkstjórnun á milli Microsoft Teams og Dynamics 365 Commerce sölustaðar
description: Þetta efnisatriði lýsir því hvernig á að samstilla verkstjórnun á milli Microsoft Teams og Dynamics 365 Commerce sölustaðar (POS).
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
ms.openlocfilehash: ca0cb32ac3ee508ddcd5346a895fb9904fa92517
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842685"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a><span data-ttu-id="fdaa6-103">Samstilla verkstjórnun á milli Microsoft Teams og Dynamics 365 Commerce sölustaðar</span><span class="sxs-lookup"><span data-stu-id="fdaa6-103">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="fdaa6-104">Þetta efnisatriði lýsir því hvernig á að samstilla verkstjórnun á milli Microsoft Teams og Dynamics 365 Commerce sölustaðar (POS).</span><span class="sxs-lookup"><span data-stu-id="fdaa6-104">This topic describes how to synchronize task management between Microsoft Teams and Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="fdaa6-105">Einn megintilgangur samþættingar Teams er að gera kleift að samstilla verkstjórnun milli forrits sölustaðar og Teams.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-105">One of the main purposes of Teams integration is to enable the synchronization of task management between the POS application and Teams.</span></span> <span data-ttu-id="fdaa6-106">Þannig geta starfsmenn verslunar notað annaðhvort forrit sölustaðar eða Teams til að stjórna verkum og þurfa ekki að skipta á milli forrita.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-106">In this way, store employees can use either the POS application or Teams to manage tasks, and don't have to switch applications.</span></span>

<span data-ttu-id="fdaa6-107">Þar sem Planner er notað sem gagnageymsla fyrir verk í Teams, þarf að vera tengill milli Teams og Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-107">Because Planner is used as a repository for tasks in Teams, there must be a link between Teams and Dynamics 365 Commerce.</span></span> <span data-ttu-id="fdaa6-108">Þessi tengill er settur á með því að nota tiltekið áætlunarkenni fyrir tiltekið teymi verslunar.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-108">This link is established by using a specific plan ID for a given store team.</span></span>

<span data-ttu-id="fdaa6-109">Eftirfarandi ferli sýna hvernig á að setja upp samstillingu verkstjórnunar á milli forrita sölustaðar og Teams.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-109">The following procedures show how to set up task management synchronization between the POS and Teams applications.</span></span>

## <a name="publish-a-test-task-list-in-teams"></a><span data-ttu-id="fdaa6-110">Birta lista yfir prufuverk í Teams</span><span class="sxs-lookup"><span data-stu-id="fdaa6-110">Publish a test task list in Teams</span></span>

<span data-ttu-id="fdaa6-111">Eftirfarandi ferli gerir ráð fyrir því að teymi verslunar séu að nota Microsoft Teams samþættingu verkstjórnunar við Commerce í fyrsta skipti.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-111">The following procedure assumes that your store teams are using Microsoft Teams task management integration with Commerce for the first time.</span></span>

<span data-ttu-id="fdaa6-112">Fylgið þessum skrefum til að birta prófunarverk í Teams.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-112">To publish a test task list in Teams, follow these steps.</span></span>

1. <span data-ttu-id="fdaa6-113">Skráðu þig inn á Teams sem samskiptastjóra.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-113">Sign in to Teams as a communications manager.</span></span> <span data-ttu-id="fdaa6-114">Yfirleitt eru samskiptastjórar notendur sem gegna hlutverki **Svæðisstjóra** í Commerce.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-114">Typically, communications managers are users who have the **Regional manager** role in Commerce.</span></span>
1. <span data-ttu-id="fdaa6-115">Á yfirlitssvæðinu vinstra megin skal velja **Verk eftir Planner**.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-115">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="fdaa6-116">Í flipanum **Útgefnir listar** skal velja **Nýr listi** niðri vinstra megin og gefa nýja listanum heitið **Prufuverklisti**.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-116">On the **Published lists** tab, select **New list** in the lower left, and name the new list **Test task list**.</span></span>
1. <span data-ttu-id="fdaa6-117">Velja **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-117">Select **Create**.</span></span> <span data-ttu-id="fdaa6-118">Nýi Listinn birtist undir **Drög**.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-118">The new list appears under **Drafts**.</span></span>
1. <span data-ttu-id="fdaa6-119">Undir **Verktitill** skal gefa fyrsta verkinu titilinn **Teams-samþætting prófuð**.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-119">Under **Task title**, give the first task the title **Testing Teams integration**.</span></span> <span data-ttu-id="fdaa6-120">Veljið síðan **Færa inn**.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-120">Then select **Enter**.</span></span>
1. <span data-ttu-id="fdaa6-121">Á listanum **Drög** skal velja verklistann.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-121">In the **Drafts** list, select the task list.</span></span> <span data-ttu-id="fdaa6-122">Veljið síðan  **Birta**  efst í hægra horninu.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-122">Then select **Publish** in the upper-right corner.</span></span>
1. <span data-ttu-id="fdaa6-123">Í svarglugganum **Velja hverjum á að birta** skal velja teymin sem eiga að taka á móti prufuverklista.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-123">In the **Select who to publish to** dialog box, select the teams that should receive the test task list.</span></span>
1. <span data-ttu-id="fdaa6-124">Veljið **Næst** til að fara yfir birtingaráætlunina.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-124">Select **Next** to review your publication plan.</span></span> <span data-ttu-id="fdaa6-125">Ef gera þarf breytingar skal velja  **Til baka**.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-125">If you must make changes, select **Back**.</span></span> 
1. <span data-ttu-id="fdaa6-126">Veljið **Staðfestið til að halda áfram** og veljið því næst **Birta**.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-126">Select **Confirm to proceed**, and then select **Publish**.</span></span>
1. <span data-ttu-id="fdaa6-127">Að birtingu lokinni gefa skilaboð efst í flipanum **Útgefnir listar** til kynna hvort tekist hafi að afhenta verklistann.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-127">After publishing is completed, a message at the top of the **Published lists** tab indicates whether your task list was successfully delivered.</span></span>

<span data-ttu-id="fdaa6-128">Frekari upplýsingar er að finna í [Birta verklista til að stofna og fylgjast með vinnu í fyrirtækinu](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).</span><span class="sxs-lookup"><span data-stu-id="fdaa6-128">For more information, see [Publish task lists to create and track work in your organization](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).</span></span>

## <a name="link-pos-and-teams-for-task-management"></a><span data-ttu-id="fdaa6-129">Tengja sölustaði og Teams fyrir verkefnastjórnun</span><span class="sxs-lookup"><span data-stu-id="fdaa6-129">Link POS and Teams for task management</span></span>

<span data-ttu-id="fdaa6-130">Til að tengja forrit sölustaðar og Microsoft Teams fyrir verkstjórnun í Commerce Headquarters skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-130">To link the POS and Microsoft Teams applications for task management in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="fdaa6-131">Farið í **Retail og Commerce \> Verkstjórnun \> Samþætting verka við Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-131">Go to **Retail and Commerce \> Task management \> Tasks integration with Microsoft Teams**.</span></span>
1. <span data-ttu-id="fdaa6-132">Á aðgerðarúðunni skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-132">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="fdaa6-133">Stillið **Virkja samþættingu verkstjórnunar** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-133">Set the **Enable Task Management Integration** option to **Yes**.</span></span>
1. <span data-ttu-id="fdaa6-134">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-134">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="fdaa6-135">Á aðgerðasvæðinu skal velja **Setja upp verkstjórnun**.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-135">On the Action Pane, select **Setup task management**.</span></span> <span data-ttu-id="fdaa6-136">Þú ættir að fá tilkynningu sem sýnir að verið sé að búa til runuvinnslu sem kallast **Úthlutun Teams**.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-136">You should receive a notification that indicates that a batch job that is named **Teams provision** is being created.</span></span>
1. <span data-ttu-id="fdaa6-137">Farið í **Kerfisstjórnun \> Fyrirspurnir \> Runuvinnslur** og finnið nýlegustu vinnuna sem er með lýsinguna **Úthlutun Teams**.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-137">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="fdaa6-138">Bíðið þar til verkið hefur verið keyrt.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-138">Wait until this job has finished running.</span></span>
1. <span data-ttu-id="fdaa6-139">Keyrið **CDX job 1070** til að birta auðkenni áætlunarinnar og tilvísanir í verslunar til Retail Server.</span><span class="sxs-lookup"><span data-stu-id="fdaa6-139">Run the **CDX job 1070** to publish the plan ID and store references to Retail Server.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fdaa6-140">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="fdaa6-140">Additional resources</span></span>

[<span data-ttu-id="fdaa6-141">Dynamics 365 Commerce og Microsoft Teams samþættingaryfirlit</span><span class="sxs-lookup"><span data-stu-id="fdaa6-141">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="fdaa6-142">Gera Dynamics 365 Commerce og Microsoft Teams samþættingu virka</span><span class="sxs-lookup"><span data-stu-id="fdaa6-142">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="fdaa6-143">Ákvæði Microsoft Teams frá Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="fdaa6-143">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="fdaa6-144">Stjórna notandahlutverkum í Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="fdaa6-144">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="fdaa6-145">Varpa verslunum og teymum ef fyrirliggjandi teymi eru í Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="fdaa6-145">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="fdaa6-146">Algengar spurningar um samþættingu Dynamics 365 Commerce og Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="fdaa6-146">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
