---
title: Skoða verkflæðissögu
description: Notið þessa skref til að skoða stöðu skjals sem hefur verið sent inn í kerfi verkflæðis til vinnslu og samþykkis.
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: a40fe377322e2d64b751f6cace3eda20736cd321
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560453"
---
# <a name="view-workflow-history"></a><span data-ttu-id="cb322-103">Skoða verkflæðissögu</span><span class="sxs-lookup"><span data-stu-id="cb322-103">View workflow history</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cb322-104">Notið þessa skref til að skoða stöðu skjals sem hefur verið sent inn í kerfi verkflæðis til vinnslu og samþykkis.</span><span class="sxs-lookup"><span data-stu-id="cb322-104">Use these steps to view the status of a document that was submitted to the workflow system for processing and approval.</span></span> <span data-ttu-id="cb322-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="cb322-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="cb322-106">Fara á Almennt > Fyrirspurnir > Verkflæði > Verkflæðissaga.</span><span class="sxs-lookup"><span data-stu-id="cb322-106">Go to Common > Inquiries > Workflow > Workflow history.</span></span>
    * <span data-ttu-id="cb322-107">Notið þessa skjámynd til að skoða stöðu skjals sem hefur verið sent inn í kerfi verkflæðis til vinnslu og samþykkis.</span><span class="sxs-lookup"><span data-stu-id="cb322-107">Use this form to view the status of a document that was submitted to the workflow system for processing and approval.</span></span>  
    * <span data-ttu-id="cb322-108">Kenni tilviks er      auðkenniskóði verkflæðistilviks sem er að vinna eða hefur unnið skjalið.</span><span class="sxs-lookup"><span data-stu-id="cb322-108">The Instance ID is      the identification code of the workflow instance that is processing, or has processed the document.</span></span>  
    * <span data-ttu-id="cb322-109">Staða er verkflæðisstaða skjals.</span><span class="sxs-lookup"><span data-stu-id="cb322-109">The Status is the workflow status of the document.</span></span>  
    * <span data-ttu-id="cb322-110">Verkflæðiskenni er auðkenniskóði verkflæði sem er að vinna eða hefur unnið úr skjali.</span><span class="sxs-lookup"><span data-stu-id="cb322-110">The Workflow ID is the identification code of the workflow that is processing, or has processed the document.</span></span>  
    * <span data-ttu-id="cb322-111">Skjal er auðkenniskóði skjals.</span><span class="sxs-lookup"><span data-stu-id="cb322-111">The Document is the identification code of the document.</span></span>  
    * <span data-ttu-id="cb322-112">Gerð skjals er gerð skjals sem var sent inn í vinnslu.</span><span class="sxs-lookup"><span data-stu-id="cb322-112">The Document type is the type of document that was submitted for processing.</span></span>  
    * <span data-ttu-id="cb322-113">Verkflæði er heiti verkflæðisins sem er að vinna eða hefur unnið skjalið.</span><span class="sxs-lookup"><span data-stu-id="cb322-113">The Workflow is the name of the workflow that is processing, or has processed the document.</span></span>  
    * <span data-ttu-id="cb322-114">Útgáfa er útgáfunúmer verkflæðisins sem er að vinna eða er búið að vinna þetta skjal.</span><span class="sxs-lookup"><span data-stu-id="cb322-114">The Version is the version number of the workflow that is processing, or has processed the document.</span></span>  
    * <span data-ttu-id="cb322-115">Stofnuð dagsetning og tími er dagsetning og tími sem skjal var sent inn.</span><span class="sxs-lookup"><span data-stu-id="cb322-115">The Created date and time is the date and time that the document was submitted.</span></span>  
    * <span data-ttu-id="cb322-116">Liðinn tími er tími sem hefur liðið síðan skjal var sent inn.</span><span class="sxs-lookup"><span data-stu-id="cb322-116">The Elapsed time is the time that has passed since the document was submitted.</span></span>  
    * <span data-ttu-id="cb322-117">Hnappurinn Halda áfram hefur aftur verkflæðisvinnsluna fyrir valda skjalið.</span><span class="sxs-lookup"><span data-stu-id="cb322-117">The Resume button allows you to resume the workflow process for the selected document.</span></span>  
    * <span data-ttu-id="cb322-118">Afturköllunarhnappurinn gerir kleift að afturkalla valið skjal svo ekki unnið úr því.</span><span class="sxs-lookup"><span data-stu-id="cb322-118">The Recall button allows you to recall the selected document so that it is not processed.</span></span>   
2. <span data-ttu-id="cb322-119">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="cb322-119">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cb322-120">Gangið úr skugga um að hlutinn Vinnuliðir sé stækkaður.</span><span class="sxs-lookup"><span data-stu-id="cb322-120">Make sure the Work items section is expanded.</span></span>    <span data-ttu-id="cb322-121">Í þessum hluta er hægt að skoða vinnuliði sem tengist völdu skjali.</span><span class="sxs-lookup"><span data-stu-id="cb322-121">In this section you can view the work items that are associated with the selected document.</span></span> <span data-ttu-id="cb322-122">Til dæmis gæti þurft að ljúka við verkefni eða þá að samþykkja þarf skjal.</span><span class="sxs-lookup"><span data-stu-id="cb322-122">For example, a task may have to be completed, or the document may have to be approved.</span></span>  
    * <span data-ttu-id="cb322-123">Hnappurinn Endurúthluta opnar svarglugga þar sem hægt er að endurúthluta vinnulið til annars notanda.</span><span class="sxs-lookup"><span data-stu-id="cb322-123">The Reassign button will open a dialog box where you can reassign a work item to another user.</span></span>  
    * <span data-ttu-id="cb322-124">Gangið úr skugga um að hlutinn Rakningarupplýsingar sé stækkaður.</span><span class="sxs-lookup"><span data-stu-id="cb322-124">Make sure the Tracking details section is expanded.</span></span>    <span data-ttu-id="cb322-125">Í þessum hluta er hægt að skoða verkflæðissaga sem tengist völdu skjali.</span><span class="sxs-lookup"><span data-stu-id="cb322-125">In this section you can view the workflow history of the selected document.</span></span>  

