---
title: Skoða verkflæðissögu
description: Þetta efni lýsir skref til að skoða stöðu skjals sem hefur verið sent inn í kerfi verkflæðis til vinnslu og samþykkis.
author: jasongre
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16c6594161f1fecd36183a6b8f2c798f52d70a9c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189799"
---
# <a name="view-workflow-history"></a><span data-ttu-id="ca462-103">Skoða verkflæðissögu</span><span class="sxs-lookup"><span data-stu-id="ca462-103">View workflow history</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ca462-104">Þetta efni lýsir skref til að skoða stöðu skjals sem hefur verið sent inn í kerfi verkflæðis til vinnslu og samþykkis.</span><span class="sxs-lookup"><span data-stu-id="ca462-104">This topic describes the steps to view the status of a document that was submitted to the workflow system for processing and approval.</span></span> <span data-ttu-id="ca462-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="ca462-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="ca462-106">Fara til **Leiðsögn gluggi > Kerfiseiningar > Sameiginlegt > Fyrirspurnir >Verkflæði > Saga verkflæðis**.</span><span class="sxs-lookup"><span data-stu-id="ca462-106">Go to **Navigation pane > Modules > Common > Inquiries > Workflow > Workflow history**.</span></span>
    - <span data-ttu-id="ca462-107">Notið þessa skjámynd til að skoða stöðu skjals sem hefur verið sent inn í kerfi verkflæðis til vinnslu og samþykkis.</span><span class="sxs-lookup"><span data-stu-id="ca462-107">Use this form to view the status of a document that was submitted to the workflow system for processing and approval.</span></span>  
    - <span data-ttu-id="ca462-108">**Kenni tilviks** er auðkenniskóði verkflæðistilviks sem er að vinna eða hefur unnið skjalið.</span><span class="sxs-lookup"><span data-stu-id="ca462-108">The **Instance ID** is the identification code of the workflow instance that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="ca462-109">**Staða** er verkflæðisstaða skjals.</span><span class="sxs-lookup"><span data-stu-id="ca462-109">The **Status** is the workflow status of the document.</span></span>  
    - <span data-ttu-id="ca462-110">**Verkflæðiskenni** er auðkenniskóði verkflæði sem er að vinna eða hefur unnið úr skjali.</span><span class="sxs-lookup"><span data-stu-id="ca462-110">The **Workflow ID** is the identification code of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="ca462-111">**Skjal** er auðkenniskóði skjals.</span><span class="sxs-lookup"><span data-stu-id="ca462-111">The **Document** is the identification code of the document.</span></span>  
    - <span data-ttu-id="ca462-112">**Gerð skjals** er gerð skjals sem var sent inn í vinnslu.</span><span class="sxs-lookup"><span data-stu-id="ca462-112">The **Document type** is the type of document that was submitted for processing.</span></span>  
    - <span data-ttu-id="ca462-113">**Verkflæði** er heiti verkflæðisins sem er að vinna eða hefur unnið skjalið.</span><span class="sxs-lookup"><span data-stu-id="ca462-113">The **Workflow** is the name of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="ca462-114">**Útgáfa** er útgáfunúmer verkflæðisins sem er að vinna eða er búið að vinna þetta skjal.</span><span class="sxs-lookup"><span data-stu-id="ca462-114">The **Version** is the version number of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="ca462-115">**Stofnuð dagsetning og tími** er dagsetning og tími sem skjal var sent inn.</span><span class="sxs-lookup"><span data-stu-id="ca462-115">The **Created date and time** is the date and time that the document was submitted.</span></span>  
    - <span data-ttu-id="ca462-116">**Liðinn tími** er tími sem hefur liðið síðan skjal var sent inn.</span><span class="sxs-lookup"><span data-stu-id="ca462-116">The **Elapsed time** is the time that has passed since the document was submitted.</span></span>  
    - <span data-ttu-id="ca462-117">Hnappurinn **Halda áfram** hefur aftur verkflæðisvinnsluna fyrir valda skjalið.</span><span class="sxs-lookup"><span data-stu-id="ca462-117">The **Resume** button allows you to resume the workflow process for the selected document.</span></span>  
    - <span data-ttu-id="ca462-118">**Afturköllunarhnappurinn** gerir kleift að afturkalla valið skjal svo ekki unnið úr því.</span><span class="sxs-lookup"><span data-stu-id="ca462-118">The **Recall** button allows you to recall the selected document so that it is not processed.</span></span>   
2. <span data-ttu-id="ca462-119">Í listanum skal velja tengilinn í æskilegri línu.</span><span class="sxs-lookup"><span data-stu-id="ca462-119">In the list, select the link in the desired row.</span></span>
    - <span data-ttu-id="ca462-120">Gangið úr skugga um að hlutinn **Vinnuliðir** sé stækkaður.</span><span class="sxs-lookup"><span data-stu-id="ca462-120">Make sure the **Work items** section is expanded.</span></span> <span data-ttu-id="ca462-121">Í þessum hluta er hægt að skoða vinnuliði sem tengist völdu skjali.</span><span class="sxs-lookup"><span data-stu-id="ca462-121">In this section you can view the work items that are associated with the selected document.</span></span> <span data-ttu-id="ca462-122">Til dæmis gæti þurft að ljúka við verkefni eða þá að samþykkja þarf skjal.</span><span class="sxs-lookup"><span data-stu-id="ca462-122">For example, a task may have to be completed, or the document may have to be approved.</span></span>  
    - <span data-ttu-id="ca462-123">Hnappurinn **Endurúthluta** opnar svarglugga þar sem hægt er að endurúthluta vinnulið til annars notanda.</span><span class="sxs-lookup"><span data-stu-id="ca462-123">The **Reassign** button will open a dialog box where you can reassign a work item to another user.</span></span>  
    - <span data-ttu-id="ca462-124">Gangið úr skugga um að hlutinn **Rakningarupplýsingar** sé stækkaður.</span><span class="sxs-lookup"><span data-stu-id="ca462-124">Make sure the **Tracking details** section is expanded.</span></span> <span data-ttu-id="ca462-125">Í þessum hluta er hægt að skoða verkflæðissaga sem tengist völdu skjali.</span><span class="sxs-lookup"><span data-stu-id="ca462-125">In this section you can view the workflow history of the selected document.</span></span>  
