---
title: Búðu til verkefnalista og bættu við verkum
description: Þetta efnisatriði lýsir því hvernig á að stofna verkefnalista og bæta verkum við þá í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: f3fcfae9f4ab458b4f14f18859f22fc25bf98623
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027625"
---
# <a name="create-task-lists-and-add-tasks"></a><span data-ttu-id="8bf8b-103">Búa til verkefnalista og bæta við verkum</span><span class="sxs-lookup"><span data-stu-id="8bf8b-103">Create task lists and add tasks</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8bf8b-104">Þetta efnisatriði lýsir því hvernig á að stofna verkefnalista og bæta verkum við þá í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-104">This topic describes how to create task lists and add tasks to them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8bf8b-105">*Verk* skilgreinir tiltekið verk eða aðgerð sem einhver verður að ljúka á eða fyrir tiltekinn gjalddaga.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-105">A *task* defines a specific piece of work or an action that someone must complete on or before a specified due date.</span></span> <span data-ttu-id="8bf8b-106">Í Dynamics 365 Commerce getur verk innihaldið nákvæmar leiðbeiningar og upplýsingar um tengilið.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-106">In Dynamics 365 Commerce, a task can include detailed instructions and information about a contact person.</span></span> <span data-ttu-id="8bf8b-107">Það getur einnig falið í sér hlekki á bakvinnsluaðgerðir, sölustaði (POS) eða vefsíður til að bæta framleiðni og veita það samhengi sem eigandi verkefna þarf til að ljúka verkinu á skilvirkan hátt.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-107">It can also include links to back-office operations, point of sale (POS) operations, or site pages, to help improve productivity and provide the context that the task owner requires to complete the task efficiently.</span></span>

<span data-ttu-id="8bf8b-108">*Verkefnalisti* er safn verkefna sem þarf að ljúka sem hluta af viðskiptaferli.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-108">A *task list* is a collection of tasks that must be completed as part of a business process.</span></span> <span data-ttu-id="8bf8b-109">Til dæmis gæti verið til verkefnalisti sem nýr starfsmaður verður að fylla út í nýliðaþjálfun, verkefnalista fyrir gjaldkera sem vinna kvöldvaktir eða verkefnalista sem verður að ljúka til að undirbúa verslunina fyrir komandi frídaga.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-109">For example, there might be a task list that a new worker must complete during onboarding, a task list for cashiers who work evening shifts, or a task list that must be completed to prepare the store for an upcoming holiday season.</span></span> <span data-ttu-id="8bf8b-110">Í Commerce er hægt að úthluta öllum verkefnalistum sem eru með dagsetningu til hvaða fjölda verslana eða starfsmanna sem er og hægt er að stilla það svo að það endurtaki sig.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-110">In Commerce, every task list that has a target date can be assigned to any number of stores or employees, and it can be configured to recur.</span></span>

<span data-ttu-id="8bf8b-111">Bæði stjórnendur og starfsmenn geta búið til verkefnalista í bakvinnslu Commerce og síðan úthlutað þeim í safn verslana.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-111">Both managers and workers can create task lists in Commerce back office, and then assign them to a set of stores.</span></span>

## <a name="create-a-task-list"></a><span data-ttu-id="8bf8b-112">Búa til verklista</span><span class="sxs-lookup"><span data-stu-id="8bf8b-112">Create a task list</span></span>

<span data-ttu-id="8bf8b-113">Til að stofna verklista skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-113">To create a task list, follow these steps.</span></span>

1. <span data-ttu-id="8bf8b-114">Farðu í **Retail og Commerce \> Verkefnisstjórn \> Stjórnun verkefnisstjórnunar**.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-114">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="8bf8b-115">Veldu **Nýtt** og sláðu síðan inn gildi í reitunum **Nafn**, **Lýsing** og **Eigandi**.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-115">Select **New**, and then enter values in the **Name**, **Description**, and **Owner** fields.</span></span>
1. <span data-ttu-id="8bf8b-116">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-116">Select **Save**.</span></span>

## <a name="add-tasks-to-a-task-list"></a><span data-ttu-id="8bf8b-117">Bættu verkefnum við verkefnalista</span><span class="sxs-lookup"><span data-stu-id="8bf8b-117">Add tasks to a task list</span></span>

<span data-ttu-id="8bf8b-118">Til að bæta verki við verklista skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-118">To add tasks to a task list, follow these steps.</span></span>
 
1. <span data-ttu-id="8bf8b-119">Á flýtiflipanum **Verk** í fyrirliggjandi verkefnalista velurðu **Nýtt** til að bæta við verki.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-119">On the **Tasks** FastTab of an existing task list, select **New** to add a task.</span></span>
1. <span data-ttu-id="8bf8b-120">Í valmyndinni **Stofna nýtt verk** í reitnum **Heiti** er fært inn einkvæmt heiti fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-120">In the **Create a new task** dialog box, in the **Name** field, enter a name for the task.</span></span>
1. <span data-ttu-id="8bf8b-121">Í reitinn **Mótfærsla gjalddaga frá markdegi** slærðu inn jákvætt eða neikvætt heiltölugildi.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-121">In the **Due data offset from target date** field, enter a positive or negative integer value.</span></span> <span data-ttu-id="8bf8b-122">Til dæmis, sláðu inn **-2** ef verkefni ætti að vera lokið tveimur dögum fyrir gjalddaga verkefnalistans.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-122">For example, enter **-2** if the task should be completed two days before the task list's due date.</span></span>
1. <span data-ttu-id="8bf8b-123">Í reitinn **Athugasemdir** slærðu inn nákvæmar leiðbeiningar.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-123">In the **Notes** field, enter detailed instructions.</span></span>
1. <span data-ttu-id="8bf8b-124">Í reitinn **Tengiliður** slærðu inn heiti efnissérfræðings sem verkefnaeigandinn getur haft samband ef hann þarfnast hjálpar.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-124">In the **Contact person** field, enter the name of a subject matter expert that the task owner can contact if the task owner needs help.</span></span>
1. <span data-ttu-id="8bf8b-125">Í reitinn **Verktengill** slærðu inn tengil, samkvæmt á eðli verksins.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-125">In the **Task link** field, enter a link, based on the nature of the task.</span></span>

> [!TIP]
> <span data-ttu-id="8bf8b-126">Þó að þú getir notað reitinn **Úthlutað á** til að úthluta verkum á einhvers meðan þú ert að búa til verkefnalista, mælum við með að þú forðist að úthluta verkefnum meðan verkefnalistinn er búinn til.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-126">Although you can use the **Assigned to** field to assign tasks to someone while you're creating a task list, we recommend that you avoid assigning tasks during task list creation.</span></span> <span data-ttu-id="8bf8b-127">Í staðinn skaltu úthluta verkefnum þegar listinn hefur verið eintekinn fyrir stakar verslanir.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-127">Instead, assign the tasks after the list is instantiated for individual stores.</span></span>

## <a name="use-task-links-to-help-improve-worker-productivity"></a><span data-ttu-id="8bf8b-128">Notaðu verkefnatengla til að bæta framleiðni starfsmanna</span><span class="sxs-lookup"><span data-stu-id="8bf8b-128">Use task links to help improve worker productivity</span></span>

<span data-ttu-id="8bf8b-129">Commerce gerir þér kleift að tengja verk við sérstakar POS-aðgerðir, eins og að keyra söluskýrslu, skoða þjálfunarmyndband á netinu fyrir nýja stefnu starfsmanna eða framkvæma bakvinnsluaðgerð.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-129">Commerce lets you link tasks to specific POS operations, such as running a sales report, viewing an online training video for new employee orientation, or performing a back-office operation.</span></span> <span data-ttu-id="8bf8b-130">Þessi aðgerð hjálpar eigendum verkefna að fá þær upplýsingar sem þeir þurfa til að klára verkefni á skilvirkan hátt.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-130">This feature helps task owners get the information that they need to complete a task efficiently.</span></span>

<span data-ttu-id="8bf8b-131">Fylgdu þessum skrefum til að bæta við verkefnatenglum meðan þú býrð til verkefni.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-131">To add task links while you create a task, follow these steps.</span></span>

1. <span data-ttu-id="8bf8b-132">Á flýtiflipanum **Verk** í fyrirliggjandi verkefnalista velurðu **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-132">On the **Tasks** FastTab of an existing task list, select **Edit**.</span></span>
1. <span data-ttu-id="8bf8b-133">Í glugganum **Breyta verki** í reitnum **Verkefnatengill** velurðu einn eða fleiri af eftirfarandi valkostum:</span><span class="sxs-lookup"><span data-stu-id="8bf8b-133">In the **Edit task** dialog box, in the **Task link** field, select one or more of the following options:</span></span>

    - <span data-ttu-id="8bf8b-134">Veldu **Valmyndaratriði** til að stilla bakvinnslu, eins og „Vörusett”.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-134">Select **Menu item** to configure a back-office operation, such as "Product kits."</span></span>
    - <span data-ttu-id="8bf8b-135">Veldu **POS aðgerð** til að stilla POS aðgerð, eins og „Söluskýrslur”.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-135">Select **POS Operation** to configure a POS operation, such as "Sales reports."</span></span>
    - <span data-ttu-id="8bf8b-136">Veldu **Vefslóð** til að stilla fasta slóð.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-136">Select **URL** to configure an absolute URL.</span></span>

<span data-ttu-id="8bf8b-137">Eftirfarandi mynd sýnir val á verkstenglum í valmyndinni **Breyta verki**.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-137">The following illustration shows the selection of task links in the **Edit task** dialog box.</span></span>

![Val á verktenglum í glugganum Breyta verkefni](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a><span data-ttu-id="8bf8b-139">Stilltu POS-aðgerð svo hægt sé að tengja hana við verk</span><span class="sxs-lookup"><span data-stu-id="8bf8b-139">Configure a POS operation so that it can be linked to a task</span></span>

<span data-ttu-id="8bf8b-140">Til að stilla POS-aðgerð svo hægt sé að tengja hana við verk fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-140">To configure a POS operation so that it can be linked to a task, follow these steps.</span></span>

1. <span data-ttu-id="8bf8b-141">Farðu í **Retail og Commerce \> Uppsetningu rásar \> Uppsetning POS \> POS \> POS-aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-141">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="8bf8b-142">Veldu **Breyta**, finndu POS-aðgerðina og veldu síðan gátreitinn **Virkja verkefnisstjórnun** fyrir hana.</span><span class="sxs-lookup"><span data-stu-id="8bf8b-142">Select **Edit**, find the POS operation, and then select the **Enable Task Management** check box for it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8bf8b-143">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="8bf8b-143">Additional resources</span></span>

[<span data-ttu-id="8bf8b-144">Yfirlit verkefnastjórnunar</span><span class="sxs-lookup"><span data-stu-id="8bf8b-144">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="8bf8b-145">Skilgreina verkstýringu</span><span class="sxs-lookup"><span data-stu-id="8bf8b-145">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="8bf8b-146">Úthluta verkefnalistum til verslana eða starfsmanna</span><span class="sxs-lookup"><span data-stu-id="8bf8b-146">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="8bf8b-147">Verkstjórnun á sölustað</span><span class="sxs-lookup"><span data-stu-id="8bf8b-147">Task management in POS</span></span>](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
