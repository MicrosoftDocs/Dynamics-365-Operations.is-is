---
title: Setja upp verkflæði fyrir kostnað
description: Hægt er að setja upp verkflæði sem er notað til að skoða og samþykkja ferða- og kostnaðarskjöl.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86cadf7277fbb7e08dad4b5dc2a46e1c6ce5a888
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840962"
---
# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="bf2c4-103">Setja upp verkflæði fyrir kostnað</span><span class="sxs-lookup"><span data-stu-id="bf2c4-103">Set up workflows for expense</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf2c4-104">Hægt er að setja upp verkflæði sem er notað til að skoða og samþykkja ferða- og kostnaðarskjöl.</span><span class="sxs-lookup"><span data-stu-id="bf2c4-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="bf2c4-105">Meðal annars er hægt að skilgreina verkflæði fyrir kostnaðarskýrslur, ferðabeiðnir og beiðni um fyrirframgreiðslu.</span><span class="sxs-lookup"><span data-stu-id="bf2c4-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="bf2c4-106">Verkflæði endurspeglar viðskiptaferli.</span><span class="sxs-lookup"><span data-stu-id="bf2c4-106">A workflow represents a business process.</span></span> <span data-ttu-id="bf2c4-107">Það skilgreinir flæði skjals í gegnum kerfið og gefur til kynna hver verður að ljúka við verk eða samþykkja skjal.</span><span class="sxs-lookup"><span data-stu-id="bf2c4-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="bf2c4-108">Nokkrir kostir eru við að nota verkflæðiskerfi í fyrirtækinu:</span><span class="sxs-lookup"><span data-stu-id="bf2c4-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="bf2c4-109">**Samræmt ferli** — Hægt er að skilgreina samþykktarferli fyrir einstök skjöl, eins og innkaupabeiðnir og kostnaðarskýrslur.</span><span class="sxs-lookup"><span data-stu-id="bf2c4-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="bf2c4-110">Með því að nota verkflæðiskerfi má betur ganga úr skugga um að skjölin séu unnin og samþykkt með samræmdum og skilvirkum hætti.</span><span class="sxs-lookup"><span data-stu-id="bf2c4-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="bf2c4-111">Sýnileiki ferlis — Hægt er að rekja stöðu, sögu og afkastamælikvarða tiltekins verkflæðistilviks.</span><span class="sxs-lookup"><span data-stu-id="bf2c4-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="bf2c4-112">Þetta auðveldar ákvörðun um hvort breyta þurfi verkflæðinu til að auka skilvirkni.</span><span class="sxs-lookup"><span data-stu-id="bf2c4-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="bf2c4-113">Miðlægur verkefnalisti — Notendur geta skoðað miðlægan verkefnalista og séð verkefni í verkflæðinu og samþykktir sem tilheyra þeim.</span><span class="sxs-lookup"><span data-stu-id="bf2c4-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="bf2c4-114">**Gerðir verkflæðis sem hægt er að stofna**</span><span class="sxs-lookup"><span data-stu-id="bf2c4-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="bf2c4-115">Í eftirfarandi töflu er listi yfir gerðir verkflæðis sem hægt er að stofna í **Kostnaður**.</span><span class="sxs-lookup"><span data-stu-id="bf2c4-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="bf2c4-116"><strong>Gerð</strong></span><span class="sxs-lookup"><span data-stu-id="bf2c4-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="bf2c4-117"><strong>Notið þessa gerð til að</strong></span><span class="sxs-lookup"><span data-stu-id="bf2c4-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="bf2c4-118"><strong>Kostnaðarskýrsla</strong></span><span class="sxs-lookup"><span data-stu-id="bf2c4-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="bf2c4-119">Stofna samþykkisverkflæði fyrir kostnaðarskýrslur.</span><span class="sxs-lookup"><span data-stu-id="bf2c4-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="bf2c4-120"><strong>Sjálfvirk bókun á kostnaðarskýrslu</strong></span><span class="sxs-lookup"><span data-stu-id="bf2c4-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="bf2c4-121">Búa sjálfkrafa til bókunarverkflæði fyrir kostnaðarskýrslur</span><span class="sxs-lookup"><span data-stu-id="bf2c4-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="bf2c4-122"><strong>Kostnaðarlínuvara</strong></span><span class="sxs-lookup"><span data-stu-id="bf2c4-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="bf2c4-123">Búa til samþykkisverkflæði fyrir línuatriði fyrir kostnaðarskýrslur.</span><span class="sxs-lookup"><span data-stu-id="bf2c4-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="bf2c4-124"><strong>Sjálfvirk bókun kostnaðarlínuatriða</strong></span><span class="sxs-lookup"><span data-stu-id="bf2c4-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="bf2c4-125">Búa til sjálfvirk bókunarverkflæði fyrir línuatriði fyrir kostnaðarskýrslur.</span><span class="sxs-lookup"><span data-stu-id="bf2c4-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="bf2c4-126"><strong>Ferðabeiðni</strong></span><span class="sxs-lookup"><span data-stu-id="bf2c4-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="bf2c4-127">Stofna samþykktarverkflæði fyrir ferðabeiðnir.</span><span class="sxs-lookup"><span data-stu-id="bf2c4-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="bf2c4-128"><strong>Beiðni um fyrirframgreiðslu</strong></span><span class="sxs-lookup"><span data-stu-id="bf2c4-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="bf2c4-129">Stofna samþykktarverkflæði fyrir beiðni um fyrirframgreiðslu.</span><span class="sxs-lookup"><span data-stu-id="bf2c4-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="bf2c4-130"><strong>Endurgreiðsla VSK</strong></span><span class="sxs-lookup"><span data-stu-id="bf2c4-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="bf2c4-131">Stofna samþykktarverkflæði fyrir endurgreiðslu virðisaukaskatts.</span><span class="sxs-lookup"><span data-stu-id="bf2c4-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

