---
title: Verkstjórnun á sölustað
description: Þetta efni lýsir verkefnastjórnun í Microsoft Dynamics 365 Commerce sölustað (POS) forritinu.
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
ms.openlocfilehash: 889cc90b534de33ccd0e2bea367b2da42b5d72e0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006186"
---
# <a name="task-management-in-pos"></a><span data-ttu-id="d6265-103">Verkstjórnun á sölustað</span><span class="sxs-lookup"><span data-stu-id="d6265-103">Task management in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d6265-104">Þetta efni lýsir verkefnastjórnun í Microsoft Dynamics 365 Commerce sölustað (POS) forritinu.</span><span class="sxs-lookup"><span data-stu-id="d6265-104">This topic describes task management in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

## <a name="overview"></a><span data-ttu-id="d6265-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="d6265-105">Overview</span></span>

<span data-ttu-id="d6265-106">Dynamics 365 Commerce POS forritið er með verkstjórnunareiginleika sem láta verslunarstjóra og starfsmenn stjórna verkefnum og uppfæra stöðu verkefna.</span><span class="sxs-lookup"><span data-stu-id="d6265-106">The Dynamics 365 Commerce POS application has task management features that let store managers and workers manage tasks and update task status.</span></span> <span data-ttu-id="d6265-107">Verslunarmenn geta nálgast verk annaðhvort með því að velja reitinn **Verk** á heimasíðu POS eða með því að velja tilkynningar um verkefni.</span><span class="sxs-lookup"><span data-stu-id="d6265-107">Store workers can access tasks either by selecting the **Tasks** tile on the POS home page or by selecting task notifications.</span></span> <span data-ttu-id="d6265-108">Sjálfgefið er að starfsmenn verslunarinnar séu fluttir á flipann **Mín verk** þar sem þeir geta skoðað verkefnin sem þeim er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="d6265-108">By default, store workers are taken to the **My tasks** tab, where they can view the tasks that are assigned to them.</span></span> <span data-ttu-id="d6265-109">Hins vegar geta þeir auðveldlega skipt yfir á flipana **Verk í vanskilum**, **Opin verk** og **Verkefnalistar**.</span><span class="sxs-lookup"><span data-stu-id="d6265-109">However, they can easily switch to the **Overdue tasks**, **Open tasks**, and **Task lists** tabs.</span></span>

## <a name="task-operations-for-store-managers"></a><span data-ttu-id="d6265-110">Verkefni fyrir verslunarstjóra</span><span class="sxs-lookup"><span data-stu-id="d6265-110">Task operations for store managers</span></span>

<span data-ttu-id="d6265-111">Verslunarstjórar geta framkvæmt eftirfarandi verkefnaaðgerðir í POS forritinu með því að nota hnappana á stjórnstikunni:</span><span class="sxs-lookup"><span data-stu-id="d6265-111">Store managers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="d6265-112">**Úthluta** - Úthlutaðu völdum verkefnum á starfskrafta verslunar.</span><span class="sxs-lookup"><span data-stu-id="d6265-112">**Assign** – Assign selected tasks to a store worker.</span></span>
- <span data-ttu-id="d6265-113">**Staða verkefnis** - Breyta stöðu valinna verkefna.</span><span class="sxs-lookup"><span data-stu-id="d6265-113">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="d6265-114">**Sía** - Sjálfgefið er að aðeins virk verkefni eru sýnd.</span><span class="sxs-lookup"><span data-stu-id="d6265-114">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="d6265-115">Hins vegar með því að beita síum geta stjórnendur skoðað öll verkefni, jafnvel verkefni sem hefur verið lokið eða aflýst.</span><span class="sxs-lookup"><span data-stu-id="d6265-115">However, by applying filters, managers can view all tasks, even tasks that have been completed or canceled.</span></span>
- <span data-ttu-id="d6265-116">**Nýtt verkefni** - Búðu til verkefni undir fyrirliggjandi verkefnalista, eða búðu til eins tilgangs verkefni.</span><span class="sxs-lookup"><span data-stu-id="d6265-116">**New task** – Create a task under an existing task list, or create an single-purpose task.</span></span>

<span data-ttu-id="d6265-117">Starfsfólk verslunar getur framkvæmt eftirfarandi verkefnaaðgerðir í POS forritinu með því að nota hnappana á stjórnstikunni:</span><span class="sxs-lookup"><span data-stu-id="d6265-117">Store workers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="d6265-118">**Staða verkefnis** - Breyta stöðu valinna verkefna.</span><span class="sxs-lookup"><span data-stu-id="d6265-118">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="d6265-119">**Sía** - Sjálfgefið er að aðeins virk verkefni eru sýnd.</span><span class="sxs-lookup"><span data-stu-id="d6265-119">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="d6265-120">Hins vegar með því að beita síum getur starfsfólk skoðað öll verkefni, jafnvel verkefni sem hefur verið lokið eða aflýst.</span><span class="sxs-lookup"><span data-stu-id="d6265-120">However, by applying filters, workers can view all tasks, even tasks that have been completed or canceled.</span></span>

<span data-ttu-id="d6265-121">Eftirfarandi mynd sýnir flipann **Mín verk** í POS forritinu Commerce.</span><span class="sxs-lookup"><span data-stu-id="d6265-121">The following illustration shows the **My tasks** tab in the Commerce POS application.</span></span>

![Flipinn Mín verk í POS forritinu Commerce](media/POS-task-management.png)

<span data-ttu-id="d6265-123">Eftirfarandi skýringarmynd sýnir flipann **Verkefnalistar**.</span><span class="sxs-lookup"><span data-stu-id="d6265-123">The following illustration shows the **Task lists** tab.</span></span>

![Flipinn Verkefnalistar í POS forritinu Commerce](media/POS-task-lists-management.png)

## <a name="additional-resources"></a><span data-ttu-id="d6265-125">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="d6265-125">Additional resources</span></span>

[<span data-ttu-id="d6265-126">Yfirlit verkstjórnunar</span><span class="sxs-lookup"><span data-stu-id="d6265-126">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="d6265-127">Skilgreina verkstjórnun</span><span class="sxs-lookup"><span data-stu-id="d6265-127">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="d6265-128">Búa til verkefnalista og bæta við verkum</span><span class="sxs-lookup"><span data-stu-id="d6265-128">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="d6265-129">Úthluta verkefnalistum til verslana eða starfsmanna</span><span class="sxs-lookup"><span data-stu-id="d6265-129">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)
