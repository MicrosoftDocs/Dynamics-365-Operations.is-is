---
title: "Setja upp verkflæði fyrir kostnað"
description: "Hægt er að setja upp verkflæði sem er notað til að skoða og samþykkja ferða- og kostnaðarskjöl."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 19d725f15f00afce1a2ae4b336226f1dafa94b41
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="dbb3b-103">Setja upp verkflæði fyrir kostnað</span><span class="sxs-lookup"><span data-stu-id="dbb3b-103">Set up workflows for expense</span></span>

[!include[banner](../includes/banner.md)]<span data-ttu-id="dbb3b-104"> Hægt er að setja upp verkflæði sem er notað til að skoða og samþykkja ferða- og kostnaðarskjöl.</span><span class="sxs-lookup"><span data-stu-id="dbb3b-104"> You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="dbb3b-105">Meðal annars er hægt að skilgreina verkflæði fyrir kostnaðarskýrslur, ferðabeiðnir og beiðni um fyrirframgreiðslu.</span><span class="sxs-lookup"><span data-stu-id="dbb3b-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="dbb3b-106">Verkflæði endurspeglar viðskiptaferli.</span><span class="sxs-lookup"><span data-stu-id="dbb3b-106">A workflow represents a business process.</span></span> <span data-ttu-id="dbb3b-107">Það skilgreinir flæði skjals í gegnum kerfið og gefur til kynna hver verður að ljúka við verk eða samþykkja skjal.</span><span class="sxs-lookup"><span data-stu-id="dbb3b-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="dbb3b-108">Nokkrir kostir eru við að nota verkflæðiskerfi í fyrirtækinu:</span><span class="sxs-lookup"><span data-stu-id="dbb3b-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="dbb3b-109">**Samræmt ferli** — Hægt er að skilgreina samþykktarferli fyrir einstök skjöl, eins og innkaupabeiðnir og kostnaðarskýrslur.</span><span class="sxs-lookup"><span data-stu-id="dbb3b-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="dbb3b-110">Með því að nota verkflæðiskerfi má betur ganga úr skugga um að skjölin séu unnin og samþykkt með samræmdum og skilvirkum hætti.</span><span class="sxs-lookup"><span data-stu-id="dbb3b-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="dbb3b-111">Sýnileiki ferlis — Hægt er að rekja stöðu, sögu og afkastamælikvarða tiltekins verkflæðistilviks.</span><span class="sxs-lookup"><span data-stu-id="dbb3b-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="dbb3b-112">Þetta auðveldar ákvörðun um hvort breyta þurfi verkflæðinu til að auka skilvirkni.</span><span class="sxs-lookup"><span data-stu-id="dbb3b-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="dbb3b-113">Miðlægur verkefnalisti — Notendur geta skoðað miðlægan verkefnalista og séð verkefni í verkflæðinu og samþykktir sem tilheyra þeim.</span><span class="sxs-lookup"><span data-stu-id="dbb3b-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="dbb3b-114">**Gerðir verkflæðis sem hægt er að stofna**</span><span class="sxs-lookup"><span data-stu-id="dbb3b-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="dbb3b-115">Í eftirfarandi töflu er listi yfir gerðir verkflæðis sem hægt er að stofna í **Kostnaður**.</span><span class="sxs-lookup"><span data-stu-id="dbb3b-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>

| <span data-ttu-id="dbb3b-116">**Gerð**</span><span class="sxs-lookup"><span data-stu-id="dbb3b-116">**Type**</span></span>                           | <span data-ttu-id="dbb3b-117">**Notið þessa gerð til að**</span><span class="sxs-lookup"><span data-stu-id="dbb3b-117">**Use this type to**</span></span>                                                 |     
|------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="dbb3b-118">**Kostnaðarskýrsla**</span><span class="sxs-lookup"><span data-stu-id="dbb3b-118">**Expense report**</span></span>                 | <span data-ttu-id="dbb3b-119">Stofna samþykkisverkflæði fyrir kostnaðarskýrslur.</span><span class="sxs-lookup"><span data-stu-id="dbb3b-119">Create approval workflows for expense reports.</span></span>                       |      
| <span data-ttu-id="dbb3b-120">**Sjálfvirk bókun á kostnaðarskýrslu**</span><span class="sxs-lookup"><span data-stu-id="dbb3b-120">**Expense report auto posting**</span></span>    | <span data-ttu-id="dbb3b-121">Búa sjálfkrafa til bókunarverkflæði fyrir kostnaðarskýrslur</span><span class="sxs-lookup"><span data-stu-id="dbb3b-121">Create automatic posting workflows for expense reports.</span></span>              |     
| <span data-ttu-id="dbb3b-122">**Kostnaðarlínuvara**</span><span class="sxs-lookup"><span data-stu-id="dbb3b-122">**Expense line item**</span></span>              | <span data-ttu-id="dbb3b-123">Búa til samþykkisverkflæði fyrir línuatriði fyrir kostnaðarskýrslur.</span><span class="sxs-lookup"><span data-stu-id="dbb3b-123">Create approval workflows for line items on expense reports.</span></span>         |     
| <span data-ttu-id="dbb3b-124">**Sjálfvirk bókun kostnaðarlínuatriða**</span><span class="sxs-lookup"><span data-stu-id="dbb3b-124">**Expense line item auto posting**</span></span> | <span data-ttu-id="dbb3b-125">Búa til sjálfvirk bókunarverkflæði fyrir línuatriði fyrir kostnaðarskýrslur.</span><span class="sxs-lookup"><span data-stu-id="dbb3b-125">Create automatic posting workflows for line items on expense reports.</span></span>|
| <span data-ttu-id="dbb3b-126">**Ferðabeiðni**</span><span class="sxs-lookup"><span data-stu-id="dbb3b-126">**Travel requisition**</span></span>             | <span data-ttu-id="dbb3b-127">Stofna samþykktarverkflæði fyrir ferðabeiðnir.</span><span class="sxs-lookup"><span data-stu-id="dbb3b-127">Create approval workflows for travel requisitions.</span></span>                   |    
| <span data-ttu-id="dbb3b-128">**Beiðni um fyrirframgreiðslu**</span><span class="sxs-lookup"><span data-stu-id="dbb3b-128">**Cash advance request**</span></span>           | <span data-ttu-id="dbb3b-129">Stofna samþykktarverkflæði fyrir beiðni um fyrirframgreiðslu.</span><span class="sxs-lookup"><span data-stu-id="dbb3b-129">Create approval workflows for cash advance requests.</span></span>                 |     
| <span data-ttu-id="dbb3b-130">**Endurgreiðsla VSK**</span><span class="sxs-lookup"><span data-stu-id="dbb3b-130">**VAT tax recovery**</span></span>               | <span data-ttu-id="dbb3b-131">Stofna samþykktarverkflæði fyrir endurgreiðslu virðisaukaskatts.</span><span class="sxs-lookup"><span data-stu-id="dbb3b-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span> |       

