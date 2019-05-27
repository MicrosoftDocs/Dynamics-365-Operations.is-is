---
title: Verkflæðiseiningar
description: Þetta efnisatriði lýsir hinum ýmsu þáttum sem verkflæði samanstendur af.
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 48fa9613b37fceeda1ea73c5fd5d4f7a7edc74cf
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571931"
---
# <a name="workflow-elements"></a><span data-ttu-id="72275-103">Verkflæðiseiningar</span><span class="sxs-lookup"><span data-stu-id="72275-103">Workflow elements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72275-104">Þetta efnisatriði lýsir hinum ýmsu þáttum sem verkflæði samanstendur af.</span><span class="sxs-lookup"><span data-stu-id="72275-104">This topic describes the various elements that make up a workflow.</span></span>

<span data-ttu-id="72275-105">Verkflæði samanstendur af einingum.</span><span class="sxs-lookup"><span data-stu-id="72275-105">A workflow consists of elements.</span></span> <span data-ttu-id="72275-106">Eftirfarandi hlutar útskýra hverja einingu gerð einingar.</span><span class="sxs-lookup"><span data-stu-id="72275-106">The sections that follow describe each type of element.</span></span>

## <a name="tasks"></a><span data-ttu-id="72275-107">Verk</span><span class="sxs-lookup"><span data-stu-id="72275-107">Tasks</span></span>

<span data-ttu-id="72275-108">*Verkefni* er vinnueining sem þarf að vinna.</span><span class="sxs-lookup"><span data-stu-id="72275-108">A *task* is a unit of work that must be performed.</span></span> <span data-ttu-id="72275-109">Tvær gerðir af verkum má bæta við verkflæði: handvirk verk og sjálfvirk verk.</span><span class="sxs-lookup"><span data-stu-id="72275-109">Two types of tasks can be added to a workflow: manual tasks and automated tasks.</span></span>

### <a name="manual-task"></a><span data-ttu-id="72275-110">Handvirk verk</span><span class="sxs-lookup"><span data-stu-id="72275-110">Manual task</span></span>

<span data-ttu-id="72275-111">*Handvirkt Verkefni* er vinnueining sem notandinn þarf að vinna.</span><span class="sxs-lookup"><span data-stu-id="72275-111">A *manual task* is a unit of work that must be performed by a user.</span></span> <span data-ttu-id="72275-112">Til dæmis getur verkflæði kostnaðarskýrslu haft handvirkt verk sem krefjast þess af skráðum notendum að ljúka eftirfarandi aðgerðum:</span><span class="sxs-lookup"><span data-stu-id="72275-112">For example, an expense report workflow can have manual tasks that require the assigned users to complete the following actions:</span></span>

- <span data-ttu-id="72275-113">Endurskoða innhreyfingarnar sem eru sendar með kostnaðarskýrslu.</span><span class="sxs-lookup"><span data-stu-id="72275-113">Review the receipts that are submitted together with an expense report.</span></span>
- <span data-ttu-id="72275-114">Hringjá í yfirmann starfsmanns</span><span class="sxs-lookup"><span data-stu-id="72275-114">Call an employee's manager.</span></span>

### <a name="automated-task"></a><span data-ttu-id="72275-115">Sjálfvirkt verk</span><span class="sxs-lookup"><span data-stu-id="72275-115">Automated task</span></span>

<span data-ttu-id="72275-116">*Sjálfvirkt Verkefni* er vinnueining sem kerfið þarf að vinna.</span><span class="sxs-lookup"><span data-stu-id="72275-116">An *automated task* is a unit of work that must be performed by the system.</span></span> <span data-ttu-id="72275-117">Engin mannleg samskipti eru nauðsynleg.</span><span class="sxs-lookup"><span data-stu-id="72275-117">No human interaction is required.</span></span> <span data-ttu-id="72275-118">Til dæmis getur verkflæði sölupöntunar haft sjálfvirkt verk sem krefjast þess af kerfinu að ljúka eftirfarandi aðgerðum:</span><span class="sxs-lookup"><span data-stu-id="72275-118">For example, a sales order workflow can have automated tasks that require the system to complete the following actions:</span></span>

- <span data-ttu-id="72275-119">Framkvæma athugun á lánamarki.</span><span class="sxs-lookup"><span data-stu-id="72275-119">Perform a credit check.</span></span>
- <span data-ttu-id="72275-120">Stofna færsla viðskiptavinar fyrir viðskiptavininn, ef færsla er ekki þegar til.</span><span class="sxs-lookup"><span data-stu-id="72275-120">Create a customer record for the customer, if a record doesn't already exist.</span></span>

## <a name="approval-processes"></a><span data-ttu-id="72275-121">samþykktarferli</span><span class="sxs-lookup"><span data-stu-id="72275-121">Approval processes</span></span>

<span data-ttu-id="72275-122">*Samþykktarferli* er ferli felur í sér nokkur skref.</span><span class="sxs-lookup"><span data-stu-id="72275-122">An *approval process* is a process that consists of separate steps.</span></span> <span data-ttu-id="72275-123">Notandinn á hverju samþykktarskrefi getur framkvæmt eftirfarandi aðgerðir:</span><span class="sxs-lookup"><span data-stu-id="72275-123">At each approval step, the user can perform the following actions:</span></span>

- <span data-ttu-id="72275-124">Samþykkja skjalið.</span><span class="sxs-lookup"><span data-stu-id="72275-124">Approve the document.</span></span>
- <span data-ttu-id="72275-125">Hafna skjalinu.</span><span class="sxs-lookup"><span data-stu-id="72275-125">Reject the document.</span></span>
- <span data-ttu-id="72275-126">Biðja um breytingu á skjalinu.</span><span class="sxs-lookup"><span data-stu-id="72275-126">Request a change to the document.</span></span>
- <span data-ttu-id="72275-127">Úthluta skjalinu til annars notanda til samþykktar.</span><span class="sxs-lookup"><span data-stu-id="72275-127">Assign the document to another user for approval.</span></span>

## <a name="line-item-workflow-elements"></a><span data-ttu-id="72275-128">Verkflæðiseining línuatriðis</span><span class="sxs-lookup"><span data-stu-id="72275-128">Line-item workflow elements</span></span>

<span data-ttu-id="72275-129">Hægt er að stofna verkflæði til að vinna annað hvort úr skjölum eða línuvörum á skjali.</span><span class="sxs-lookup"><span data-stu-id="72275-129">A workflow can be created to process either documents or the line items on a document.</span></span> <span data-ttu-id="72275-130">Til dæmis hefur verið stofnað samþykkisverkflæði fyrir vinnukort.</span><span class="sxs-lookup"><span data-stu-id="72275-130">For example, you've created an approval workflow for timesheets.</span></span> <span data-ttu-id="72275-131">(Vísað verður í þetta verkflæði sem *skjalaverkflæði*.) Hægt er að bæta við einingunni *verkflæði línuatriðis* í þetta skjalaverkflæði.</span><span class="sxs-lookup"><span data-stu-id="72275-131">(We will refer to this workflow as the *document workflow*.) You can add a *line-item workflow* element to that document workflow.</span></span> <span data-ttu-id="72275-132">Þegar eining línuatriðis er keyrt, er hvert línuatriði á skjalinu sent til vinnslu.</span><span class="sxs-lookup"><span data-stu-id="72275-132">When the line-item element is run, each line item on the document is submitted for processing.</span></span> <span data-ttu-id="72275-133">Þú gætir viljað að öll línuatriðin séu innin með sama verkflæði línuatriðis eða þú gætir viljað láta vinna hvert línuatriði af mismunandi verkflæði línuvöru.</span><span class="sxs-lookup"><span data-stu-id="72275-133">You might want all the line items to be processed by the same line-item workflow, or you might want each line item to be processed by a different line-item workflow.</span></span> <span data-ttu-id="72275-134">Hugsum hafi starfsmaður hefur senda vinnukort sem svipar eftirfarandi tala.</span><span class="sxs-lookup"><span data-stu-id="72275-134">Imagine that an employee has submitted a timesheet that resembles the following figure.</span></span>

![Verkflæði með línuatriði](./media/workflow_lineitemworkflow.gif)

<span data-ttu-id="72275-136">Í þessum aðstæðum gætirðu viljað stofna eftirfarandi verkflæði línuatriðis:</span><span class="sxs-lookup"><span data-stu-id="72275-136">In this scenario, you might want to create the following line-item workflows:</span></span>

- <span data-ttu-id="72275-137">**verkflæði línuatriðis 1** – Þetta verkflæði er notað til að vinna línuatriði þar sem verkkennið er 1111.</span><span class="sxs-lookup"><span data-stu-id="72275-137">**Line-item workflow 1** – This workflow is used to process line items where the project ID is 1111.</span></span>
- <span data-ttu-id="72275-138">**Verkflæði línuatriðis 2** – Þetta verkflæði er notað til að vinna línuatriði þar sem verkkennið er 2222.</span><span class="sxs-lookup"><span data-stu-id="72275-138">**Line-item workflow 2** – This workflow is used to process line items where the project ID is 2222.</span></span>
- <span data-ttu-id="72275-139">**Verkflæði línuatriðis 3** – Þetta verkflæði er notað til að vinna línuatriði þar sem verkkennið er 3333.</span><span class="sxs-lookup"><span data-stu-id="72275-139">**Line-item workflow 3** – This workflow is used to process line items where the project ID is 3333.</span></span>

## <a name="flow-control-elements"></a><span data-ttu-id="72275-140">Einingar flæðistýringar</span><span class="sxs-lookup"><span data-stu-id="72275-140">Flow-control elements</span></span>

<span data-ttu-id="72275-141">Eftirfarandi einingar gera þér kleift að hanna verkflæði sem hafa aðrar greinar eða greinar sem keyra á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="72275-141">The following elements let you design workflows that have alternate branches or branches that run at the same time.</span></span>

### <a name="manual-decision"></a><span data-ttu-id="72275-142">Handvirk ákvörðun</span><span class="sxs-lookup"><span data-stu-id="72275-142">Manual decision</span></span>

<span data-ttu-id="72275-143">*Handvirk ákvörðun* er punktur þar sem verkflæði skiptist í tvær greinar.</span><span class="sxs-lookup"><span data-stu-id="72275-143">A *manual decision* is a point where a workflow divides into two branches.</span></span> <span data-ttu-id="72275-144">Notandi verður að gera ákvörðun og þessi ákvörðun ákveður hvaða grein er notuð til að vinna úr skjali sem sent var inn.</span><span class="sxs-lookup"><span data-stu-id="72275-144">A user must make a decision, and this decision determines which branch is used to process the document that was submitted.</span></span>

### <a name="conditional-decision"></a><span data-ttu-id="72275-145">Skilyrt ákvörðun</span><span class="sxs-lookup"><span data-stu-id="72275-145">Conditional decision</span></span>

<span data-ttu-id="72275-146">*Skilyrt ákvörðun* er einnig punktur þar sem verkflæði skiptist í tvær greinar.</span><span class="sxs-lookup"><span data-stu-id="72275-146">A *conditional decision* is also a point where a workflow divides into two branches.</span></span> <span data-ttu-id="72275-147">Hinsvegar ákvarðar kerfið hvaða grein er notuð til að vinna úr skjali sem sent var inn.</span><span class="sxs-lookup"><span data-stu-id="72275-147">However, the system decides which branch is used to process the document that was submitted.</span></span> <span data-ttu-id="72275-148">Til að gera þetta ákvörðun, metur kerfið skjals til að ákvarða hvort það uppfyllir tilgreind skilyrði.</span><span class="sxs-lookup"><span data-stu-id="72275-148">To make this decision, the system evaluates the document to determine whether it meets specified conditions.</span></span>

### <a name="parallel-activity"></a><span data-ttu-id="72275-149">Hliðstæður verkþáttur</span><span class="sxs-lookup"><span data-stu-id="72275-149">Parallel activity</span></span>

<span data-ttu-id="72275-150">*hliðstæður verkþáttur* er verkflæðiseining sem inniheldur tvær eða fleiri verkflæðisgreinar sem eru keyrðar á sama tíma</span><span class="sxs-lookup"><span data-stu-id="72275-150">A *parallel activity* is a workflow element that includes two or more workflow branches that run at the same time.</span></span>

### <a name="subworkflow"></a><span data-ttu-id="72275-151">Undirverkflæði</span><span class="sxs-lookup"><span data-stu-id="72275-151">Subworkflow</span></span>

<span data-ttu-id="72275-152">*Undirverkflæði* er verkflæði sem keirir í samhengi við annað yfirverkflæði.</span><span class="sxs-lookup"><span data-stu-id="72275-152">A *subworkflow* is a workflow that runs in the context of another workflow.</span></span>
