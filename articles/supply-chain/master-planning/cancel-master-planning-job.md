---
title: Hætta við aðaláætlunarverk
description: Þetta efni útskýrir hvernig á að hætta við virka áætlunarvinnslu sem notar innbyggða áætlunarvirkni.
author: ChristianRytt
manager: AnnBe
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 66d5b10e1471b98274d4049df18a2e53873f789a
ms.sourcegitcommit: 92cd55028be556a0bd41b6972c9c6d14b695dfa0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/10/2020
ms.locfileid: "2947481"
---
# <a name="cancel-a-master-planning-job"></a><span data-ttu-id="48197-103">Hætta við aðaláætlunarverk</span><span class="sxs-lookup"><span data-stu-id="48197-103">Cancel a master planning job</span></span>

<span data-ttu-id="48197-104">Í Microsoft Dynamics 365 Supply Chain Management eru margir möguleikar til að hætta við aðaláætlunarverk.</span><span class="sxs-lookup"><span data-stu-id="48197-104">In Microsoft Dynamics 365 Supply Chain Management, there are multiple options for canceling a master planning job.</span></span> <span data-ttu-id="48197-105">Til dæmis gætirðu viljað hætta við aðaláætlunarverk ef það var hafið fyrir mistök eða keyrir lengur en áætlað var og þú vilt slíta því.</span><span class="sxs-lookup"><span data-stu-id="48197-105">For example, you may want to cancel a master planning job if it was started by mistake or is running longer than expected and you want to end it.</span></span> <span data-ttu-id="48197-106">Besta leiðin til að hætta við áætlunarvinnslu er af síðunni **Ólokin áætlunarferli**.</span><span class="sxs-lookup"><span data-stu-id="48197-106">The best way to cancel a planning job is from  the **Unfinished planning processes** page.</span></span> <span data-ttu-id="48197-107">Aðrir valkostir af síðunum **Runuvinnslur** og **Runuvinnslur auknar** ætti að nota ef afturköllun á aðaláætlunarvinnslunni af síðunni **Ólokin áætlunarferli** lauk ekki innan nokkurra mínútna.</span><span class="sxs-lookup"><span data-stu-id="48197-107">Alternative options from the **Batch jobs** and **Batch jobs enhanced** pages should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

## <a name="preferred-cancel-option"></a><span data-ttu-id="48197-108">Æskilegur hætta við valkost</span><span class="sxs-lookup"><span data-stu-id="48197-108">Preferred cancel option</span></span>
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a><span data-ttu-id="48197-109">Hætta við aðaláætlunarvinnslu af síðunni **Ólokin áætlunarferli**</span><span class="sxs-lookup"><span data-stu-id="48197-109">Cancel master planning job from **Unfinished planning processes** page</span></span>
1. <span data-ttu-id="48197-110">Farðu í **Aðaláætlanagerð > Fyrirspurnir og skýrslur > Aðaláætlanagerð > Ólokin áætlunarferli**.</span><span class="sxs-lookup"><span data-stu-id="48197-110">Go to **Master planning > Inquiries and reports > Master planning > Unfinished planning processes**.</span></span>
2. <span data-ttu-id="48197-111">Veldu línuna með áætlunarferlinu sem ætlunin er að afturkalla.</span><span class="sxs-lookup"><span data-stu-id="48197-111">Select the line with the planning process that you want to cancel.</span></span>
3. <span data-ttu-id="48197-112">Smelltu á **Hætta við**.</span><span class="sxs-lookup"><span data-stu-id="48197-112">Click **Cancel**.</span></span>

## <a name="additional-cancel-options"></a><span data-ttu-id="48197-113">Aukaafturköllunarvalkostir</span><span class="sxs-lookup"><span data-stu-id="48197-113">Additional cancel options</span></span>
<span data-ttu-id="48197-114">Þetta ætti aðeins að nota ef afturköllun á aðaláætlunarvinnslunni af síðunni **Ólokin áætlunarferli** lauk ekki innan nokkurra mínútna.</span><span class="sxs-lookup"><span data-stu-id="48197-114">These should only be used iif cancelin the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a><span data-ttu-id="48197-115">Eyða aðaláætlanavinnslu af síðunni **Runuvinnslur**</span><span class="sxs-lookup"><span data-stu-id="48197-115">Delete master planning job from the **Batch jobs** page</span></span>
1. <span data-ttu-id="48197-116">Farðu í **Kerfisstjórnun > Fyrirspurnir> Runuvinnslur**.</span><span class="sxs-lookup"><span data-stu-id="48197-116">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="48197-117">Veldu línuna með áætlunarvinnslunni sem ætlunin er að eyða.</span><span class="sxs-lookup"><span data-stu-id="48197-117">Select the line with the planning job that you want to delete.</span></span>
3. <span data-ttu-id="48197-118">Smellið á **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="48197-118">Click **Delete**.</span></span>

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a><span data-ttu-id="48197-119">Hætta við aðaláætlanavinnsluverk af síðunni **Runuvinnslur auknar**</span><span class="sxs-lookup"><span data-stu-id="48197-119">Abort master planning job task from the **Batch jobs enhanced** page</span></span>
1. <span data-ttu-id="48197-120">Farðu í **Kerfisstjórnun > Fyrirspurnir> Runuvinnslur**.</span><span class="sxs-lookup"><span data-stu-id="48197-120">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="48197-121">Ef vinnslukenni birtist ekki á listanum skaltu smella á **Skipta yfir í aukna skjámynd**, annars skalta halda áfram með næsta skref.</span><span class="sxs-lookup"><span data-stu-id="48197-121">If the job ID is not shown in the list, click **Switch to enhanced form**, otherwise proceed with the next step.</span></span>
3. <span data-ttu-id="48197-122">Opnaðu runuvinnsluna.</span><span class="sxs-lookup"><span data-stu-id="48197-122">Open the batch job.</span></span> <span data-ttu-id="48197-123">Smelltu á **Vinnslukenni** fyrir runuvinnsluna með verk sem þú vilt ljúka.</span><span class="sxs-lookup"><span data-stu-id="48197-123">Click the **Job ID** for the batch job with tasks that you want to end.</span></span>
4. <span data-ttu-id="48197-124">Í **Runuverk** velurðu verkin sem á að ljúka.</span><span class="sxs-lookup"><span data-stu-id="48197-124">In **Batch tasks**, select the tasks to end.</span></span>
5. <span data-ttu-id="48197-125">Á flýtiflipanum **Runuverk** smellirðu á **Hætta við**.</span><span class="sxs-lookup"><span data-stu-id="48197-125">On the **Batch tasks** FastTab, click **Abort**.</span></span>
