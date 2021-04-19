---
title: Verkstjórnun á sölustað
description: Þetta efnisatriði lýsir verkstjórnun í Microsoft Dynamics 365 Commerce sölustaðarforritinu.
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
ms.openlocfilehash: 38ee9db94b3b222e8c0ce5d0883f47bd5d3e7d22
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796923"
---
# <a name="task-management-in-pos"></a><span data-ttu-id="3fa59-103">Verkstjórnun á sölustað</span><span class="sxs-lookup"><span data-stu-id="3fa59-103">Task management in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3fa59-104">Þetta efnisatriði lýsir verkstjórnun í Microsoft Dynamics 365 Commerce sölustaðarforritinu.</span><span class="sxs-lookup"><span data-stu-id="3fa59-104">This topic describes task management in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

<span data-ttu-id="3fa59-105">Dynamics 365 Commerce POS forritið er með verkstjórnunareiginleika sem láta verslunarstjóra og starfsmenn stjórna verkefnum og uppfæra stöðu verkefna.</span><span class="sxs-lookup"><span data-stu-id="3fa59-105">The Dynamics 365 Commerce POS application has task management features that let store managers and workers manage tasks and update task status.</span></span> <span data-ttu-id="3fa59-106">Verslunarmenn geta nálgast verk annaðhvort með því að velja reitinn **Verk** á heimasíðu POS eða með því að velja tilkynningar um verkefni.</span><span class="sxs-lookup"><span data-stu-id="3fa59-106">Store workers can access tasks either by selecting the **Tasks** tile on the POS home page or by selecting task notifications.</span></span> <span data-ttu-id="3fa59-107">Sjálfgefið er að starfsmenn verslunarinnar séu fluttir á flipann **Mín verk** þar sem þeir geta skoðað verkefnin sem þeim er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="3fa59-107">By default, store workers are taken to the **My tasks** tab, where they can view the tasks that are assigned to them.</span></span> <span data-ttu-id="3fa59-108">Hins vegar geta þeir auðveldlega skipt yfir á flipana **Verk í vanskilum**, **Opin verk** og **Verkefnalistar**.</span><span class="sxs-lookup"><span data-stu-id="3fa59-108">However, they can easily switch to the **Overdue tasks**, **Open tasks**, and **Task lists** tabs.</span></span>

## <a name="task-operations-for-store-managers"></a><span data-ttu-id="3fa59-109">Verkefni fyrir verslunarstjóra</span><span class="sxs-lookup"><span data-stu-id="3fa59-109">Task operations for store managers</span></span>

<span data-ttu-id="3fa59-110">Verslunarstjórar geta framkvæmt eftirfarandi verkefnaaðgerðir í POS forritinu með því að nota hnappana á stjórnstikunni:</span><span class="sxs-lookup"><span data-stu-id="3fa59-110">Store managers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="3fa59-111">**Úthluta** - Úthlutaðu völdum verkefnum á starfskrafta verslunar.</span><span class="sxs-lookup"><span data-stu-id="3fa59-111">**Assign** – Assign selected tasks to a store worker.</span></span>
- <span data-ttu-id="3fa59-112">**Staða verkefnis** - Breyta stöðu valinna verkefna.</span><span class="sxs-lookup"><span data-stu-id="3fa59-112">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="3fa59-113">**Sía** - Sjálfgefið er að aðeins virk verkefni eru sýnd.</span><span class="sxs-lookup"><span data-stu-id="3fa59-113">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="3fa59-114">Hins vegar með því að beita síum geta stjórnendur skoðað öll verkefni, jafnvel verkefni sem hefur verið lokið eða aflýst.</span><span class="sxs-lookup"><span data-stu-id="3fa59-114">However, by applying filters, managers can view all tasks, even tasks that have been completed or canceled.</span></span>
- <span data-ttu-id="3fa59-115">**Nýtt verkefni** - Búðu til verkefni undir fyrirliggjandi verkefnalista, eða búðu til eins tilgangs verkefni.</span><span class="sxs-lookup"><span data-stu-id="3fa59-115">**New task** – Create a task under an existing task list, or create an single-purpose task.</span></span>

<span data-ttu-id="3fa59-116">Starfsfólk verslunar getur framkvæmt eftirfarandi verkefnaaðgerðir í POS forritinu með því að nota hnappana á stjórnstikunni:</span><span class="sxs-lookup"><span data-stu-id="3fa59-116">Store workers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="3fa59-117">**Staða verkefnis** - Breyta stöðu valinna verkefna.</span><span class="sxs-lookup"><span data-stu-id="3fa59-117">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="3fa59-118">**Sía** - Sjálfgefið er að aðeins virk verkefni eru sýnd.</span><span class="sxs-lookup"><span data-stu-id="3fa59-118">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="3fa59-119">Hins vegar með því að beita síum getur starfsfólk skoðað öll verkefni, jafnvel verkefni sem hefur verið lokið eða aflýst.</span><span class="sxs-lookup"><span data-stu-id="3fa59-119">However, by applying filters, workers can view all tasks, even tasks that have been completed or canceled.</span></span>

<span data-ttu-id="3fa59-120">Eftirfarandi mynd sýnir flipann **Mín verk** í POS forritinu Commerce.</span><span class="sxs-lookup"><span data-stu-id="3fa59-120">The following illustration shows the **My tasks** tab in the Commerce POS application.</span></span>

![Flipinn Mín verk í POS forritinu Commerce](media/POS-task-management.png)

<span data-ttu-id="3fa59-122">Eftirfarandi skýringarmynd sýnir flipann **Verkefnalistar**.</span><span class="sxs-lookup"><span data-stu-id="3fa59-122">The following illustration shows the **Task lists** tab.</span></span>

![Flipinn Verkefnalistar í POS forritinu Commerce](media/POS-task-lists-management.png)

## <a name="additional-resources"></a><span data-ttu-id="3fa59-124">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="3fa59-124">Additional resources</span></span>

[<span data-ttu-id="3fa59-125">Yfirlit verkstjórnunar</span><span class="sxs-lookup"><span data-stu-id="3fa59-125">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="3fa59-126">Skilgreina verkstjórnun</span><span class="sxs-lookup"><span data-stu-id="3fa59-126">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="3fa59-127">Búa til verkefnalista og bæta við verkum</span><span class="sxs-lookup"><span data-stu-id="3fa59-127">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="3fa59-128">Úthluta verkefnalistum til verslana eða starfsmanna</span><span class="sxs-lookup"><span data-stu-id="3fa59-128">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
