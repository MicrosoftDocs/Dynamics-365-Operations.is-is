---
title: Skilgreina verkstýringu
description: Þetta efnisatriði lýsir því hvernig á að stilla verkefnisstjórnunaraðgerðir í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 9a4775c2dba2b9aa8e671ab6c246000303b3a37e
ms.sourcegitcommit: 80cbb7d22267aa6a0ae0568d0063fb95556958a5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/11/2020
ms.locfileid: "3036856"
---
# <a name="configure-task-management"></a><span data-ttu-id="525e8-103">Skilgreina verkstýringu</span><span class="sxs-lookup"><span data-stu-id="525e8-103">Configure task management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="525e8-104">Þetta efnisatriði lýsir því hvernig á að stilla verkefnisstjórnunaraðgerðir í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="525e8-104">This topic describes how to configure task management features in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="525e8-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="525e8-105">Overview</span></span>

<span data-ttu-id="525e8-106">Áður en Dynamics 365 Commerce stjórnendur og starfsmenn geta notað verkstjórnunaraðgerðir í verslun verður að stilla verkstjórnun.</span><span class="sxs-lookup"><span data-stu-id="525e8-106">Before Dynamics 365 Commerce managers and employees can use the task management features in Commerce, task management must be configured.</span></span> <span data-ttu-id="525e8-107">Stillingarþrepin fela í sér að veita stjórnendum og starfsmönnum leyfi, dreifa heimildum til viðskiptavina á sölustað (POS), setja upp POS tilkynningar og stilla reitina **Verk** á heimasíðu POS forrita.</span><span class="sxs-lookup"><span data-stu-id="525e8-107">Configuration steps include granting permissions to managers and employees, distributing permissions to point of sale (POS) clients, setting up POS notifications, and configuring the **Tasks** tile on the home page of a POS application.</span></span>

## <a name="configure-permissions-for-store-managers"></a><span data-ttu-id="525e8-108">Stilla heimildir fyrir verslunarstjóra</span><span class="sxs-lookup"><span data-stu-id="525e8-108">Configure permissions for store managers</span></span>

<span data-ttu-id="525e8-109">Sérhver starfskraftur í tiltekinni verslun getur skoðað öll verk sem þeim er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="525e8-109">Every worker in a given store can view all tasks that are assigned to that store.</span></span> <span data-ttu-id="525e8-110">Þeir geta einnig uppfært stöðu verka sem þeim er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="525e8-110">They can also update the status of the tasks that are assigned to them.</span></span> <span data-ttu-id="525e8-111">Aðilar eins og verslunarstjórar verða þó að hafa heimildir fyrir verkefnisstjórnun til að stjórna verkefnum sem eru úthlutað í verslunina og til að búa til eins tilgangs verkefni.</span><span class="sxs-lookup"><span data-stu-id="525e8-111">However, personas such as store managers must have task management permissions to manage tasks that are assigned to the store and to create single-purpose tasks.</span></span>

<span data-ttu-id="525e8-112">Fylgdu þessum skrefum til að stilla verkefnastjórnunarheimildir fyrir verslunarstjóra.</span><span class="sxs-lookup"><span data-stu-id="525e8-112">To configure task management permissions for store managers, follow these steps.</span></span>

1. <span data-ttu-id="525e8-113">Farðu í **Retail og Commerce \> Starfsmenn \> Heimildaflokkar**.</span><span class="sxs-lookup"><span data-stu-id="525e8-113">Go to **Retail and Commerce \> Employees \> Permission groups**.</span></span>
1. <span data-ttu-id="525e8-114">Veldu sérstakan leyfishóp (til dæmis, **Stjórnandi**) og veldu síðan **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="525e8-114">Select a specific permission group (for example, **Manager**), and then select **Edit**.</span></span>
1. <span data-ttu-id="525e8-115">Á flýtiflipanum **Heimildir** stillirðu valkostinn **Leyfa verkefnastjórnun** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="525e8-115">On the **Permissions** FastTab, set the **Allow task management** option to **Yes**.</span></span>
1. <span data-ttu-id="525e8-116">Á flýtiflipanum **Tilkynningar** bætirðu við aðgerðinni **Verkefnisstjórn** og slærð inn gildi í reitinn **Sýna röð**.</span><span class="sxs-lookup"><span data-stu-id="525e8-116">On the **Notifications** FastTab, add the **Task management** operation, and enter a value in the **Display order** field.</span></span> <span data-ttu-id="525e8-117">Til dæmis, sláðu inn **2** ef aðgerðin **Uppfylling pöntunar** er þegar með gildi **Sýna röð** upp á **1**.</span><span class="sxs-lookup"><span data-stu-id="525e8-117">For example, enter **2** if the **Order fulfillment** operation already has a **Display order** value of **1**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="525e8-118">Ef aðili annar en stjórnandi verður að hafa heimildir fyrir verkefnisstjórnun í POS geturðu veitt einstaklingnum leyfi.</span><span class="sxs-lookup"><span data-stu-id="525e8-118">If a non-manager persona must have task management permissions in the POS, you can grant permission to the individual.</span></span> <span data-ttu-id="525e8-119">Einnig er hægt að búa til nýjan leyfishóp fyrir utan stjórnendur og stilla valkostinn **Leyfa verkefnastjórnun** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="525e8-119">Alternatively, you can create a new permission group for non-managers and set the **Allow task management** option to **Yes**.</span></span>

<span data-ttu-id="525e8-120">Eftirfarandi skýringarmynd sýnir hvernig á að stilla verkefnastjórnunarheimildir fyrir verslunarstjóra.</span><span class="sxs-lookup"><span data-stu-id="525e8-120">The following illustration shows how to configure task management permissions for store managers.</span></span>

![Stilling verkefnastjórnunarheimilda fyrir verslunarstjóra](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a><span data-ttu-id="525e8-122">Stilla heimildir fyrir starfsmenn</span><span class="sxs-lookup"><span data-stu-id="525e8-122">Configure permissions for employees</span></span>

<span data-ttu-id="525e8-123">Starfsmenn verða að hafa heimildir til að búa til verkefnalista, stjórna úthlutunarviðmiðum og stilla endurtekningu hvaða verkefnalista sem er.</span><span class="sxs-lookup"><span data-stu-id="525e8-123">Employees must have permissions to create task lists, manage assignment criteria, and configure the recurrence of any task list.</span></span> <span data-ttu-id="525e8-124">Til að stilla þessar heimildir úthlutar þú starfsmönnum á hlutverkið **Stjórnandi smásöluverks**.</span><span class="sxs-lookup"><span data-stu-id="525e8-124">To configure these permissions, you assign employees to the **Retail task manager** role.</span></span>

<span data-ttu-id="525e8-125">Til að skilgreina heimildir fyrir starfsmanns skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="525e8-125">To configure permissions for an employee, follow these steps.</span></span>

1. <span data-ttu-id="525e8-126">Farðu í **Retail og Commerce \> Starfsmenn \> Notendur**.</span><span class="sxs-lookup"><span data-stu-id="525e8-126">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="525e8-127">Velja starfsmann.</span><span class="sxs-lookup"><span data-stu-id="525e8-127">Select an employee.</span></span>
1. <span data-ttu-id="525e8-128">Á flýtiflipanum **Hlutverk notanda** velurðu **Úthluta hlutverkum**.</span><span class="sxs-lookup"><span data-stu-id="525e8-128">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="525e8-129">Í valmyndinni **Úthluta hlutverkum til notanda** velurðu hlutverkið **Stjórnandi smásöluverks** og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="525e8-129">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

## <a name="distribute-permissions-to-pos-clients"></a><span data-ttu-id="525e8-130">Dreifðu heimildum til POS viðskiptavina</span><span class="sxs-lookup"><span data-stu-id="525e8-130">Distribute permissions to POS clients</span></span>

<span data-ttu-id="525e8-131">Áður en starfsmenn geta notað POS viðskiptavini verður að dreifa heimildum og samstilla við þá viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="525e8-131">Before employees can use POS clients, permissions must be distributed and synced to those clients.</span></span>

<span data-ttu-id="525e8-132">Fylgdu þessum skrefum til að dreifa heimildum til POS viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="525e8-132">To distribute permissions to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="525e8-133">Farðu í **Retail og Commerce \> Upplýsingatækni í Retail og Commerce \> Dreifingaráætlun**.</span><span class="sxs-lookup"><span data-stu-id="525e8-133">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="525e8-134">Veldu dreifingaráætlunina **1060** (**Starfsfólk**) og veldu síðan **Keyra núna**.</span><span class="sxs-lookup"><span data-stu-id="525e8-134">Select the **1060** (**Staff**) distribution schedule, and then select **Run now**.</span></span>
1. <span data-ttu-id="525e8-135">Veldu dreifingaráætlunina **1070** (**Skilgreining rásar**) og veldu síðan **Keyra núna**.</span><span class="sxs-lookup"><span data-stu-id="525e8-135">Select the **1070** (**Channel configuration**) distribution schedule, and then select **Run now**.</span></span>

## <a name="configure-pos-notifications-for-tasks"></a><span data-ttu-id="525e8-136">Stilla POS tilkynningar fyrir verkefni</span><span class="sxs-lookup"><span data-stu-id="525e8-136">Configure POS notifications for tasks</span></span>

<span data-ttu-id="525e8-137">Verkefnisstjórnun verður að vera þannig stillt að tilkynningar séu tiltækar í POS forritinu.</span><span class="sxs-lookup"><span data-stu-id="525e8-137">Task management must be configured so that notifications are available in the POS application.</span></span>

<span data-ttu-id="525e8-138">Til að skilgreina POS-tilkynningar fyrir verk skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="525e8-138">To configure POS notifications for tasks, follow these steps.</span></span>

1. <span data-ttu-id="525e8-139">Farðu í **Retail og Commerce \> Uppsetningu rásar \> Uppsetning POS \> POS \> POS-aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="525e8-139">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="525e8-140">Finndu aðgerðina **1400** (**Verkefnisstjórn**) og veldu gátreitinn **Virkja tilkynningar** fyrir hana.</span><span class="sxs-lookup"><span data-stu-id="525e8-140">Find operation **1400** (**Task management**), and select the **Enable notifications** check box for it.</span></span>

<span data-ttu-id="525e8-141">Eftirfarandi mynd sýnir aðgerðina **Verkefnisstjórn** á síðunni **POS aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="525e8-141">The following illustration shows the **Task management** operation on the **POS operations** page.</span></span>

![Aðgerðastjórnunaraðgerð á POS aðgerðarsíðunni](media/HQ-POS-Tasks-Notifications.png)

<span data-ttu-id="525e8-143">Nánari upplýsingar um hvernig á að stilla POS tilkynningar, sjá [Sýna pöntunartilkynningar í sölustað (POS)](notifications-pos.md).</span><span class="sxs-lookup"><span data-stu-id="525e8-143">For more information about how to configure POS notifications, see [Show order notifications in the point of sale (POS)](notifications-pos.md).</span></span>

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a><span data-ttu-id="525e8-144">Stilltu verkefnisreit á heimasíðu POS forrita</span><span class="sxs-lookup"><span data-stu-id="525e8-144">Configure the Tasks tile on a POS application home page</span></span>

<span data-ttu-id="525e8-145">Áður en þú stillir reitinn **Verk** á heimasíðu POS forrits, sjá [Skjáútlit fyrir sölustað (POS)](pos-screen-layouts.md) til að fá upplýsingar um hvernig á að stilla og bæta við nýjum hnöppum við POS skjáútlit.</span><span class="sxs-lookup"><span data-stu-id="525e8-145">Before you configure the **Tasks** tile on the home page of a POS application, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information about how to configure and add new buttons to a POS screen layout.</span></span>

<span data-ttu-id="525e8-146">Til að stilla reitinn **Verk** á heimasíðu POS forrita fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="525e8-146">To configure the **Tasks** tile on a POS application home page, follow these steps.</span></span>

1. <span data-ttu-id="525e8-147">Farðu í **Retail og Commerce \> Uppsetningu rásar \> Uppsetning POS \> POS \> Skjáútlit**.</span><span class="sxs-lookup"><span data-stu-id="525e8-147">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> Screen layouts**.</span></span>
1. <span data-ttu-id="525e8-148">Veldu skjáskipulag, veldu skipulagstærð og veldu hnappanet.</span><span class="sxs-lookup"><span data-stu-id="525e8-148">Select a screen layout, select a layout size, and select a button grid.</span></span>
1. <span data-ttu-id="525e8-149">Á flýtiflipanum **Hnappanet** velurðu **Hönnuður** til að breyta völdu hnappaneti.</span><span class="sxs-lookup"><span data-stu-id="525e8-149">On the **Button grids** FastTab, select **Designer** to edit the selected button grid.</span></span>
1. <span data-ttu-id="525e8-150">Bættu við reitnum **Verk** á viðeigandi hluta heimasíðunnar.</span><span class="sxs-lookup"><span data-stu-id="525e8-150">Add a **Tasks** tile to the appropriate section of the home page.</span></span>

<span data-ttu-id="525e8-151">Eftirfarandi mynd sýnir dæmi um reitinn **Verk** á heimasíðu POS.</span><span class="sxs-lookup"><span data-stu-id="525e8-151">The following illustration shows an example of a **Tasks** tile on a POS home page.</span></span>

![Verkreitur á POS heimasíðu](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a><span data-ttu-id="525e8-153">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="525e8-153">Additional resources</span></span>

[<span data-ttu-id="525e8-154">Yfirlit verkefnastjórnunar</span><span class="sxs-lookup"><span data-stu-id="525e8-154">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="525e8-155">Búa til verkefnalista og bæta við verkum</span><span class="sxs-lookup"><span data-stu-id="525e8-155">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="525e8-156">Úthluta verkefnalistum til verslana eða starfsmanna</span><span class="sxs-lookup"><span data-stu-id="525e8-156">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="525e8-157">Verkstjórnun á sölustað</span><span class="sxs-lookup"><span data-stu-id="525e8-157">Task management in POS</span></span>](task-mgmt-POS.md)
