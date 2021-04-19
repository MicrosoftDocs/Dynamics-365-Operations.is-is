---
title: Úthlutaðu verkefnalistum til verslana eða starfsmanna
description: Þetta efnisatriði lýsir því hvernig á að úthluta verkefnalistum til verslana eða starfsmanna í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0c4f028367c894c54392963ffc4f6a0f0c04c03a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795262"
---
# <a name="assign-task-lists-to-stores-or-employees"></a><span data-ttu-id="8ad04-103">Úthluta verkefnalistum til verslana eða starfsmanna</span><span class="sxs-lookup"><span data-stu-id="8ad04-103">Assign task lists to stores or employees</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8ad04-104">Þetta efnisatriði lýsir því hvernig á að úthluta verkefnalistum til verslana eða starfsmanna í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8ad04-104">This topic describes how to assign task lists to stores or employees in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8ad04-105">Verkefnisstjórn í Dynamics 365 Commerce gerir þér kleift að úthluta verkefnalista til margra verslana eða starfsmanna, eða til samblanda verslana og starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="8ad04-105">Task management in Dynamics 365 Commerce lets you assign a task list to multiple stores or employees, or to a combination of stores and employees.</span></span> <span data-ttu-id="8ad04-106">Til dæmis gæti svæðisstjóri í 20 verslunum viljað úthluta verklistanum **Undirbúningur undir frídaga** á allar 20 verslanir.</span><span class="sxs-lookup"><span data-stu-id="8ad04-106">For example, a regional manager for 20 stores might want to assign the **Holiday season preparation** task list to all 20 stores.</span></span>

## <a name="start-the-task-list-assignment-process"></a><span data-ttu-id="8ad04-107">Ræstu úthlutunarferli verkefnalista</span><span class="sxs-lookup"><span data-stu-id="8ad04-107">Start the task list assignment process</span></span>

<span data-ttu-id="8ad04-108">Fylgdu þessum skrefum til að hefja úthlutun verkefnalista.</span><span class="sxs-lookup"><span data-stu-id="8ad04-108">To start the process of assigning a task list, follow these steps.</span></span>

1. <span data-ttu-id="8ad04-109">Farðu í **Retail og Commerce \> Verkefnisstjórn \> Stjórnun verkefnisstjórnunar**.</span><span class="sxs-lookup"><span data-stu-id="8ad04-109">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="8ad04-110">Veldu verkefnalistann sem á að úthluta.</span><span class="sxs-lookup"><span data-stu-id="8ad04-110">Select the task list to assign.</span></span>
1. <span data-ttu-id="8ad04-111">Veldu **Hefja ferli**.</span><span class="sxs-lookup"><span data-stu-id="8ad04-111">Select **Start process**.</span></span>
1. <span data-ttu-id="8ad04-112">Í valmyndinni **Hefja ferli**, á flipanum **Almennt**, í reitnum **Heiti vinnslu**, slærðu inn heiti (t.d. **Verslanir á Austurlandi**).</span><span class="sxs-lookup"><span data-stu-id="8ad04-112">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name (for example, **East region stores**).</span></span>
1. <span data-ttu-id="8ad04-113">Í reitnum **Markdagsetning** tilgreinirðu dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="8ad04-113">In the **Target date** field, specify a date.</span></span>
1. <span data-ttu-id="8ad04-114">Til að úthluta verkefnalistanum á verslanir, á flipanum **Verslanir** skaltu nota síuna **Stigveldi fyrirtækis** til að finna og velja verslanir.</span><span class="sxs-lookup"><span data-stu-id="8ad04-114">To assign the task list to stores, on the **Stores** tab, use the **Organization hierarchy** filter to find and select the stores.</span></span>

    <span data-ttu-id="8ad04-115">Til að úthluta verkefnalistanum á starfsmenn, á flipanum **Starfskraftar** skaltu finna og velja starfsmennina.</span><span class="sxs-lookup"><span data-stu-id="8ad04-115">To assign the task list to employees, on the **Workers** tab, find and select the employees.</span></span>

1. <span data-ttu-id="8ad04-116">Veldu **Í lagi** til að hefja ferlið.</span><span class="sxs-lookup"><span data-stu-id="8ad04-116">Select **OK** to start the process.</span></span> <span data-ttu-id="8ad04-117">Verkefnalistinn er úthlutað til valinna verslana eða starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="8ad04-117">The tasks list is assigned to the selected stores or employees.</span></span>

<span data-ttu-id="8ad04-118">Eftirfarandi mynd sýnir dæmi um hvernig á að finna og velja verslanir í valmyndinni **Hefja ferli**.</span><span class="sxs-lookup"><span data-stu-id="8ad04-118">The following illustration shows an example of how to find and select stores in the **Start process** dialog box.</span></span>

![Finndu og veldu verslanir í valmyndinni Hefja ferli](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a><span data-ttu-id="8ad04-120">Úthlutaðu verkefnalistum endurtekið</span><span class="sxs-lookup"><span data-stu-id="8ad04-120">Assign task lists on a recurring basis</span></span>

<span data-ttu-id="8ad04-121">Söluaðili hefur stundum endurtekin verkefni, eins og „Gátlista yfir lokun fimmtudags“ eða „Gátlista yfir fyrsta dag mánaðar“.</span><span class="sxs-lookup"><span data-stu-id="8ad04-121">Retailer sometimes have recurrent tasks, such as "Thursday closure checklist" or "First day of the month checklist."</span></span> <span data-ttu-id="8ad04-122">Þess vegna gætu þeir viljað úthluta verkefnalistanum ítrekað.</span><span class="sxs-lookup"><span data-stu-id="8ad04-122">Therefore, they might want to assign the task list on a recurring basis.</span></span>

1. <span data-ttu-id="8ad04-123">Farðu í **Retail og Commerce \> Verkefnisstjórn \> Stjórnun verkefnisstjórnunar**.</span><span class="sxs-lookup"><span data-stu-id="8ad04-123">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="8ad04-124">Veldu verkefnalistann sem á að úthluta.</span><span class="sxs-lookup"><span data-stu-id="8ad04-124">Select the task list to assign.</span></span>
1. <span data-ttu-id="8ad04-125">Veldu **Hefja ferli**.</span><span class="sxs-lookup"><span data-stu-id="8ad04-125">Select **Start process**.</span></span>
1. <span data-ttu-id="8ad04-126">Í valmyndinni **Hefja ferli**, á flipanum **Almennt**, í reitnum **Heiti vinnslu**, slærðu inn heiti.</span><span class="sxs-lookup"><span data-stu-id="8ad04-126">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name.</span></span>
1. <span data-ttu-id="8ad04-127">Stilltu valkostinn **Endurtekning** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="8ad04-127">Set the **Recurrence** option to **Yes**.</span></span>
1. <span data-ttu-id="8ad04-128">Í reitinn **Mótfærsla markdagsetningar endurtekningar í dögum** slærðu inn fjölda daga.</span><span class="sxs-lookup"><span data-stu-id="8ad04-128">In the **Recurrence target date offset in days** field, enter a number of days.</span></span> <span data-ttu-id="8ad04-129">Til dæmis ef þú slærð inn **4** er markdagurinn endurtekningardagur auk fjögurra daga.</span><span class="sxs-lookup"><span data-stu-id="8ad04-129">For example, if you enter **4**, the target date is the recurrence date plus four days.</span></span>
1. <span data-ttu-id="8ad04-130">Á flipanum **Keyra í bakgrunni** velurðu **Endurtekning**.</span><span class="sxs-lookup"><span data-stu-id="8ad04-130">On the **Run in the background** tab, select **Recurrence**.</span></span>
1. <span data-ttu-id="8ad04-131">Í valmyndinni **Skilgreina endurtekningu** slærðu inn tíðniviðmið og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="8ad04-131">In the **Define recurrence** dialog box, enter the frequency criteria, and then select **OK**.</span></span>

<span data-ttu-id="8ad04-132">Eftirfarandi mynd sýnir dæmi um hvernig á að færa inn tíðniviðmið í valmyndinni **Skilgreina endurtekningu**.</span><span class="sxs-lookup"><span data-stu-id="8ad04-132">The following illustration shows an example of how to enter frequency criteria in the **Define recurrence** dialog box.</span></span>

![Tíðniviðmið færð inn í valmyndina Skilgreina endurtekningu](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a><span data-ttu-id="8ad04-134">Rekja stöðu verkefnalista</span><span class="sxs-lookup"><span data-stu-id="8ad04-134">Track task list status</span></span>

<span data-ttu-id="8ad04-135">Ef þú ert svæðisstjóri eða verslunarstjóri gætirðu viljað fylgjast með stöðu verkefnalista sem hefur verið úthlutað til margra verslana eða starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="8ad04-135">If you're a regional manager or store manager, you might want to track the status of task lists that have been assigned to multiple stores or employees.</span></span> <span data-ttu-id="8ad04-136">Þú getur síðan fylgst með verslunum eða starfsmönnum sem luku ekki verkefnum sínum á réttum tíma.</span><span class="sxs-lookup"><span data-stu-id="8ad04-136">You can then follow up with stores or workers that didn't complete their assigned tasks on time.</span></span> <span data-ttu-id="8ad04-137">Bakvinnsla Commerce gerir þér kleift að skoða stöðu verkefnalista, endurúthluta verkefnum eða breyta stöðu verkefnis.</span><span class="sxs-lookup"><span data-stu-id="8ad04-137">Commerce back office lets you view the status of task lists, reassign tasks, or change the status of a task.</span></span>

<span data-ttu-id="8ad04-138">Fylgdu þessum skrefum til að fylgjast með stöðu verkefnalistans fyrir öll verkefni.</span><span class="sxs-lookup"><span data-stu-id="8ad04-138">To track the task list status for all tasks, follow these steps.</span></span>

1. <span data-ttu-id="8ad04-139">Farðu í **Retail og Commerce \> Verkefnisstjórn \> Ferli verkefnisstjórnunar**.</span><span class="sxs-lookup"><span data-stu-id="8ad04-139">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="8ad04-140">Veldu flipann **Allir verkefnalistar** til að skoða stöðu allra verkefnalista sem eru úthlutaðir til ýmissa verslana.</span><span class="sxs-lookup"><span data-stu-id="8ad04-140">Select the **All task lists** tab to view the status of all task lists that are assigned to various stores.</span></span>

<span data-ttu-id="8ad04-141">Til að rekja stöðu verkefnalista fyrir öll verk sem er úthluta á þig skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="8ad04-141">To track the task list status for all tasks that are assigned to you, follow these steps.</span></span>

1. <span data-ttu-id="8ad04-142">Farðu í **Retail og Commerce \> Verkefnisstjórn \> Ferli verkefnisstjórnunar**.</span><span class="sxs-lookup"><span data-stu-id="8ad04-142">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="8ad04-143">Veldu flipann **Mín verk** eða **Öll verk** til að skoða eða uppfæra stöðu verkefna sem þér er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="8ad04-143">Select the **My tasks** or **All tasks** tab to view or update the status of tasks that are assigned to you.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8ad04-144">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="8ad04-144">Additional resources</span></span>

[<span data-ttu-id="8ad04-145">Yfirlit verkefnastjórnunar</span><span class="sxs-lookup"><span data-stu-id="8ad04-145">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="8ad04-146">Skilgreina verkstýringu</span><span class="sxs-lookup"><span data-stu-id="8ad04-146">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="8ad04-147">Búa til verkefnalista og bæta við verkum</span><span class="sxs-lookup"><span data-stu-id="8ad04-147">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="8ad04-148">Verkstjórnun á sölustað</span><span class="sxs-lookup"><span data-stu-id="8ad04-148">Task management in POS</span></span>](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
