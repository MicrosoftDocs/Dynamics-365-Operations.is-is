---
title: Úthlutaðu verkefnalistum til verslana eða starfsmanna
description: Þetta efni lýsir því hvernig á að úthluta verklista á verslanir eða starfsmenn í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: ee924f5bf95d47814e7ca09b392a3d10b5e9b9dc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006261"
---
# <a name="assign-task-lists-to-stores-or-employees"></a><span data-ttu-id="e17ca-103">Úthlutaðu verkefnalistum til verslana eða starfsmanna</span><span class="sxs-lookup"><span data-stu-id="e17ca-103">Assign task lists to stores or employees</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e17ca-104">Þetta efni lýsir því hvernig á að úthluta verklista á verslanir eða starfsmenn í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e17ca-104">This topic describes how to assign task lists to stores or employees in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e17ca-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="e17ca-105">Overview</span></span>

<span data-ttu-id="e17ca-106">Verkefnisstjórn í Dynamics 365 Commerce gerir þér kleift að úthluta verkefnalista til margra verslana eða starfsmanna, eða til samblanda verslana og starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="e17ca-106">Task management in Dynamics 365 Commerce lets you assign a task list to multiple stores or employees, or to a combination of stores and employees.</span></span> <span data-ttu-id="e17ca-107">Til dæmis gæti svæðisstjóri í 20 verslunum viljað úthluta verklistanum **Undirbúningur undir frídaga** á allar 20 verslanir.</span><span class="sxs-lookup"><span data-stu-id="e17ca-107">For example, a regional manager for 20 stores might want to assign the **Holiday season preparation** task list to all 20 stores.</span></span>

## <a name="start-the-task-list-assignment-process"></a><span data-ttu-id="e17ca-108">Ræstu úthlutunarferli verkefnalista</span><span class="sxs-lookup"><span data-stu-id="e17ca-108">Start the task list assignment process</span></span>

<span data-ttu-id="e17ca-109">Fylgdu þessum skrefum til að hefja úthlutun verkefnalista.</span><span class="sxs-lookup"><span data-stu-id="e17ca-109">To start the process of assigning a task list, follow these steps.</span></span>

1. <span data-ttu-id="e17ca-110">Farðu í **Retail og Commerce \> Verkefnisstjórn \> Stjórnun verkefnisstjórnunar**.</span><span class="sxs-lookup"><span data-stu-id="e17ca-110">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="e17ca-111">Veldu verkefnalistann sem á að úthluta.</span><span class="sxs-lookup"><span data-stu-id="e17ca-111">Select the task list to assign.</span></span>
1. <span data-ttu-id="e17ca-112">Veldu **Hefja ferli**.</span><span class="sxs-lookup"><span data-stu-id="e17ca-112">Select **Start process**.</span></span>
1. <span data-ttu-id="e17ca-113">Í valmyndinni **Hefja ferli**, á flipanum **Almennt**, í reitnum **Heiti vinnslu**, slærðu inn heiti (t.d. **Verslanir á Austurlandi**).</span><span class="sxs-lookup"><span data-stu-id="e17ca-113">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name (for example, **East region stores**).</span></span>
1. <span data-ttu-id="e17ca-114">Í reitnum **Markdagsetning** tilgreinirðu dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="e17ca-114">In the **Target date** field, specify a date.</span></span>
1. <span data-ttu-id="e17ca-115">Til að úthluta verkefnalistanum á verslanir, á flipanum **Verslanir** skaltu nota síuna **Stigveldi fyrirtækis** til að finna og velja verslanir.</span><span class="sxs-lookup"><span data-stu-id="e17ca-115">To assign the task list to stores, on the **Stores** tab, use the **Organization hierarchy** filter to find and select the stores.</span></span>

    <span data-ttu-id="e17ca-116">Til að úthluta verkefnalistanum á starfsmenn, á flipanum **Starfskraftar** skaltu finna og velja starfsmennina.</span><span class="sxs-lookup"><span data-stu-id="e17ca-116">To assign the task list to employees, on the **Workers** tab, find and select the employees.</span></span>

1. <span data-ttu-id="e17ca-117">Veldu **Í lagi** til að hefja ferlið.</span><span class="sxs-lookup"><span data-stu-id="e17ca-117">Select **OK** to start the process.</span></span> <span data-ttu-id="e17ca-118">Verkefnalistinn er úthlutað til valinna verslana eða starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="e17ca-118">The tasks list is assigned to the selected stores or employees.</span></span>

<span data-ttu-id="e17ca-119">Eftirfarandi mynd sýnir dæmi um hvernig á að finna og velja verslanir í valmyndinni **Hefja ferli**.</span><span class="sxs-lookup"><span data-stu-id="e17ca-119">The following illustration shows an example of how to find and select stores in the **Start process** dialog box.</span></span>

![Finndu og veldu verslanir í valmyndinni Hefja ferli](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a><span data-ttu-id="e17ca-121">Úthlutaðu verkefnalistum endurtekið</span><span class="sxs-lookup"><span data-stu-id="e17ca-121">Assign task lists on a recurring basis</span></span>

<span data-ttu-id="e17ca-122">Söluaðili hefur stundum endurtekin verkefni, eins og „Gátlista yfir lokun fimmtudags“ eða „Gátlista yfir fyrsta dag mánaðar“.</span><span class="sxs-lookup"><span data-stu-id="e17ca-122">Retailer sometimes have recurrent tasks, such as "Thursday closure checklist" or "First day of the month checklist."</span></span> <span data-ttu-id="e17ca-123">Þess vegna gætu þeir viljað úthluta verkefnalistanum ítrekað.</span><span class="sxs-lookup"><span data-stu-id="e17ca-123">Therefore, they might want to assign the task list on a recurring basis.</span></span>

1. <span data-ttu-id="e17ca-124">Farðu í **Retail og Commerce \> Verkefnisstjórn \> Stjórnun verkefnisstjórnunar**.</span><span class="sxs-lookup"><span data-stu-id="e17ca-124">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="e17ca-125">Veldu verkefnalistann sem á að úthluta.</span><span class="sxs-lookup"><span data-stu-id="e17ca-125">Select the task list to assign.</span></span>
1. <span data-ttu-id="e17ca-126">Veldu **Hefja ferli**.</span><span class="sxs-lookup"><span data-stu-id="e17ca-126">Select **Start process**.</span></span>
1. <span data-ttu-id="e17ca-127">Í valmyndinni **Hefja ferli**, á flipanum **Almennt**, í reitnum **Heiti vinnslu**, slærðu inn heiti.</span><span class="sxs-lookup"><span data-stu-id="e17ca-127">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name.</span></span>
1. <span data-ttu-id="e17ca-128">Stilltu valkostinn **Endurtekning** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="e17ca-128">Set the **Recurrence** option to **Yes**.</span></span>
1. <span data-ttu-id="e17ca-129">Í reitinn **Mótfærsla markdagsetningar endurtekningar í dögum** slærðu inn fjölda daga.</span><span class="sxs-lookup"><span data-stu-id="e17ca-129">In the **Recurrence target date offset in days** field, enter a number of days.</span></span> <span data-ttu-id="e17ca-130">Til dæmis ef þú slærð inn **4** er markdagurinn endurtekningardagur auk fjögurra daga.</span><span class="sxs-lookup"><span data-stu-id="e17ca-130">For example, if you enter **4**, the target date is the recurrence date plus four days.</span></span>
1. <span data-ttu-id="e17ca-131">Á flipanum **Keyra í bakgrunni** velurðu **Endurtekning**.</span><span class="sxs-lookup"><span data-stu-id="e17ca-131">On the **Run in the background** tab, select **Recurrence**.</span></span>
1. <span data-ttu-id="e17ca-132">Í valmyndinni **Skilgreina endurtekningu** slærðu inn tíðniviðmið og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e17ca-132">In the **Define recurrence** dialog box, enter the frequency criteria, and then select **OK**.</span></span>

<span data-ttu-id="e17ca-133">Eftirfarandi mynd sýnir dæmi um hvernig á að færa inn tíðniviðmið í valmyndinni **Skilgreina endurtekningu**.</span><span class="sxs-lookup"><span data-stu-id="e17ca-133">The following illustration shows an example of how to enter frequency criteria in the **Define recurrence** dialog box.</span></span>

![Tíðniviðmið færð inn í valmyndina Skilgreina endurtekningu](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a><span data-ttu-id="e17ca-135">Rekja stöðu verkefnalista</span><span class="sxs-lookup"><span data-stu-id="e17ca-135">Track task list status</span></span>

<span data-ttu-id="e17ca-136">Ef þú ert svæðisstjóri eða verslunarstjóri gætirðu viljað fylgjast með stöðu verkefnalista sem hefur verið úthlutað til margra verslana eða starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="e17ca-136">If you're a regional manager or store manager, you might want to track the status of task lists that have been assigned to multiple stores or employees.</span></span> <span data-ttu-id="e17ca-137">Þú getur síðan fylgst með verslunum eða starfsmönnum sem luku ekki verkefnum sínum á réttum tíma.</span><span class="sxs-lookup"><span data-stu-id="e17ca-137">You can then follow up with stores or workers that didn't complete their assigned tasks on time.</span></span> <span data-ttu-id="e17ca-138">Bakvinnsla Commerce gerir þér kleift að skoða stöðu verkefnalista, endurúthluta verkefnum eða breyta stöðu verkefnis.</span><span class="sxs-lookup"><span data-stu-id="e17ca-138">Commerce back office lets you view the status of task lists, reassign tasks, or change the status of a task.</span></span>

<span data-ttu-id="e17ca-139">Fylgdu þessum skrefum til að fylgjast með stöðu verkefnalistans fyrir öll verkefni.</span><span class="sxs-lookup"><span data-stu-id="e17ca-139">To track the task list status for all tasks, follow these steps.</span></span>

1. <span data-ttu-id="e17ca-140">Farðu í **Retail og Commerce \> Verkefnisstjórn \> Ferli verkefnisstjórnunar**.</span><span class="sxs-lookup"><span data-stu-id="e17ca-140">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="e17ca-141">Veldu flipann **Allir verkefnalistar** til að skoða stöðu allra verkefnalista sem eru úthlutaðir til ýmissa verslana.</span><span class="sxs-lookup"><span data-stu-id="e17ca-141">Select the **All task lists** tab to view the status of all task lists that are assigned to various stores.</span></span>

<span data-ttu-id="e17ca-142">Til að rekja stöðu verkefnalista fyrir öll verk sem er úthluta á þig skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="e17ca-142">To track the task list status for all tasks that are assigned to you, follow these steps.</span></span>

1. <span data-ttu-id="e17ca-143">Farðu í **Retail og Commerce \> Verkefnisstjórn \> Ferli verkefnisstjórnunar**.</span><span class="sxs-lookup"><span data-stu-id="e17ca-143">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="e17ca-144">Veldu flipann **Mín verk** eða **Öll verk** til að skoða eða uppfæra stöðu verkefna sem þér er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="e17ca-144">Select the **My tasks** or **All tasks** tab to view or update the status of tasks that are assigned to you.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e17ca-145">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="e17ca-145">Additional resources</span></span>

[<span data-ttu-id="e17ca-146">Yfirlit verkefnastjórnunar</span><span class="sxs-lookup"><span data-stu-id="e17ca-146">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="e17ca-147">Skilgreina verkstýringu</span><span class="sxs-lookup"><span data-stu-id="e17ca-147">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="e17ca-148">Búa til verkefnalista og bæta við verkum</span><span class="sxs-lookup"><span data-stu-id="e17ca-148">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="e17ca-149">Verkstjórnun á sölustað</span><span class="sxs-lookup"><span data-stu-id="e17ca-149">Task management in POS</span></span>](task-mgmt-POS.md)
