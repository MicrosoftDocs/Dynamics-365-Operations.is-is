---
title: Verkflæði kostnaðar
description: Í þessu efnisatriði er útskýrt hvernig hægt er að nota verkflæðiskerfi í Microsoft Dynamics 365 for Finance and Operations til að setja upp endurskoðunarferli fyrir kostnaðarskýrslur í Kostnaðarstýringu.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 037a6ae00b7d559f79860901f0cb2ad6ddddd7aa
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "310117"
---
# <a name="expense-workflow"></a><span data-ttu-id="fcb29-103">Verkflæði kostnaðar</span><span class="sxs-lookup"><span data-stu-id="fcb29-103">Expense workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fcb29-104">Hægt er að nota verkflæðiskerfi í Microsoft Dynamics 365 for Finance and Operations til að setja upp endurskoðunarferli fyrir kostnaðarskýrslur í Kostnaðarstýringu.</span><span class="sxs-lookup"><span data-stu-id="fcb29-104">You can use the workflow system in Microsoft Dynamics 365 for Finance and Operations, to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="fcb29-105">Hægt er að setja upp verkflæði sem notar eftirfarandi viðmiðanir til að ákvarða hver samþykkir kostnaðarskýrslur:</span><span class="sxs-lookup"><span data-stu-id="fcb29-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="fcb29-106">Starfsmaðurinn sem sér um stigveldi og fyrirfram skilgreind samþykkistakmörk</span><span class="sxs-lookup"><span data-stu-id="fcb29-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="fcb29-107">Marglaga samþykki sem styður millisamþykktaraðila og lokasamþykktaraðila</span><span class="sxs-lookup"><span data-stu-id="fcb29-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="fcb29-108">Fjárhagsvíddir ábyrgð verka</span><span class="sxs-lookup"><span data-stu-id="fcb29-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="fcb29-109">Úthlutanir á tiltekna notendur og notendaflokka</span><span class="sxs-lookup"><span data-stu-id="fcb29-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="fcb29-110">Hægt er að stofna verkflæðissamþykki fyrir kostnaðarskýrslur, ferðabeiðnir, fyrirframgreiðslur og endurgreiðslu virðisaukaskatts.</span><span class="sxs-lookup"><span data-stu-id="fcb29-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="fcb29-111">**Dæmi**</span><span class="sxs-lookup"><span data-stu-id="fcb29-111">**Example**</span></span>

<span data-ttu-id="fcb29-112">Eftirfarandi ferli er dæmi um verkflæðisferli kostnaðarstýringar fyrir kostnaðarskýrslu.</span><span class="sxs-lookup"><span data-stu-id="fcb29-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="fcb29-113">Starfsmaður stofnar og vistar kostnaðarskýrslu.</span><span class="sxs-lookup"><span data-stu-id="fcb29-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="fcb29-114">Starfsmaðurinn sendir kostnaðarskýrslu til samþykktar.</span><span class="sxs-lookup"><span data-stu-id="fcb29-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="fcb29-115">Samþykktaraðili er auðkenndur á grundvelli reglna sem voru skilgreindar þegar verkflæðið var sett upp.</span><span class="sxs-lookup"><span data-stu-id="fcb29-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="fcb29-116">Samþykktaraðili fær tilkynningu um að kostnaðarskýrsla sé tilbúin til samþykktar.</span><span class="sxs-lookup"><span data-stu-id="fcb29-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="fcb29-117">Samþykktaraðili fer yfir kostnaðarskýrsluna og staðfestir að eftirfarandi skilyrði séu uppfyllt:</span><span class="sxs-lookup"><span data-stu-id="fcb29-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="fcb29-118">Kostnaðurinn brýtur ekki í bága við kostnaðarreglur.</span><span class="sxs-lookup"><span data-stu-id="fcb29-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="fcb29-119">Ef kostnaður brýtur gegn reglu staðfestir samþykktaraðilinn að kostnaðarskýrslan innihalda gilda réttlætingu viðskipta.</span><span class="sxs-lookup"><span data-stu-id="fcb29-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="fcb29-120">Rafrænar kvittanir fylgja með kostnaðarskýrslu.</span><span class="sxs-lookup"><span data-stu-id="fcb29-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="fcb29-121">Samþykktaraðili samþykkir kostnaðarskýrsluna.</span><span class="sxs-lookup"><span data-stu-id="fcb29-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="fcb29-122">Kostnaðarskýrslan er úthlutuð á gjaldkera til bókunar.</span><span class="sxs-lookup"><span data-stu-id="fcb29-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="fcb29-123">Eitt af eftirfarandi skrefum á sér stað, eftir því hvort sjálfvirk bókun sé stillt:</span><span class="sxs-lookup"><span data-stu-id="fcb29-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="fcb29-124">Ef sjálfvirk bókun er stillt er kostnaðarskýrslan meðhöndluð til greiðslu og staða kostnaðarskýrslunnar er uppfærð.</span><span class="sxs-lookup"><span data-stu-id="fcb29-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="fcb29-125">Ef sjálfvirk bókun er ekki stillt staðfestir gjaldkeri að allar upprunalega kvittanir hafi verið sendar og að kvittanir séu í samræmi við kostnaðinn á kostnaðarskýrslunni.</span><span class="sxs-lookup"><span data-stu-id="fcb29-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="fcb29-126">Allir skattkóðar sem eru færðar á kostnaðarskýrsluna verða einnig að vera staðfestir sem réttar.</span><span class="sxs-lookup"><span data-stu-id="fcb29-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="fcb29-127">Þegar þessar kröfur eru uppfylltar er kostnaðarskýrslan bókuð.</span><span class="sxs-lookup"><span data-stu-id="fcb29-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="fcb29-128">Eftir að kostnaðarskýrslan er bókuð er greiðsla heimiluð fyrir kostnaðarskýrsluna og starfsmaðurinn fær endurgreiðslu.</span><span class="sxs-lookup"><span data-stu-id="fcb29-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>
