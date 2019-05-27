---
title: Vinna úr færslubók kostnaðarúthlutunar
description: Notaðu síðuna Vinna úr úthlutunarbeiðni til að stofna úthlutunarbók sem hægt er að yfirfara og samþykki áður en bókað er í Fjárhag eða bóka beint í Fjárhag.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d2046e25719c9023bee99736488a4ee6f22723fe
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550822"
---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="a3e60-103">Vinna úr færslubók kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="a3e60-103">Process ledger allocation journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a3e60-104">Notaðu síðuna Vinna úr úthlutunarbeiðni til að stofna úthlutunarbók sem hægt er að yfirfara og samþykki áður en bókað er í Fjárhag eða bóka beint í Fjárhag.</span><span class="sxs-lookup"><span data-stu-id="a3e60-104">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="a3e60-105">Áður en hægt er að stofna úthlutunarfærslubók verður að vera að minnsta kosti ein virk úthlutunarregla fjárhags.</span><span class="sxs-lookup"><span data-stu-id="a3e60-105">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="a3e60-106">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="a3e60-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="a3e60-107">Fara í Fjárhagur > Úthlutanir > Vinna beiðni um úthlutun.</span><span class="sxs-lookup"><span data-stu-id="a3e60-107">Go to General ledger > Allocations > Process allocation request.</span></span>
2. <span data-ttu-id="a3e60-108">Í reitnum Regla skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="a3e60-108">In the Rule field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="a3e60-109">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="a3e60-109">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="a3e60-110">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="a3e60-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="a3e60-111">Í reitnum Frá og með dagsetningu er dagsetning færð inn.</span><span class="sxs-lookup"><span data-stu-id="a3e60-111">In the As of date field, enter a date.</span></span>
    * <span data-ttu-id="a3e60-112">Frá og með dagsetningu er mjög mikilvægt þegar Fjárhagur er gagnagjafi fyrir regluna.</span><span class="sxs-lookup"><span data-stu-id="a3e60-112">The As of Date is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="a3e60-113">Þessi dagsetning stýrir hvaða fjárhagsstöðu á að taka með í úthlutun.</span><span class="sxs-lookup"><span data-stu-id="a3e60-113">This date controls which ledger balances to include for allocation.</span></span>     <span data-ttu-id="a3e60-114">Í reitnum Núll velurðu Stöðva.</span><span class="sxs-lookup"><span data-stu-id="a3e60-114">In the Zero source field select Stop.</span></span> <span data-ttu-id="a3e60-115">Þetta mun stöðva úthlutunarferlið og birta skilaboð um að núll upprunaupphæð sé valin.</span><span class="sxs-lookup"><span data-stu-id="a3e60-115">This will  Stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  
6. <span data-ttu-id="a3e60-116">Í reitnum Valkostir tillögu skal velja ‚Aðeins tillaga‘.</span><span class="sxs-lookup"><span data-stu-id="a3e60-116">In the Proposal options field, select 'Proposal only'.</span></span>
    * <span data-ttu-id="a3e60-117">Veldu Tillögu aðeins til að endurskoða og samþykkja niðurstöðu í úthlutunarbókum áður en úthlutunin er bókuð í Fjárhag.</span><span class="sxs-lookup"><span data-stu-id="a3e60-117">Select Proposal only to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
7. <span data-ttu-id="a3e60-118">Dagsetning er rituð í reitinn Bókunardagsetning fjárhags.</span><span class="sxs-lookup"><span data-stu-id="a3e60-118">In the GL posting date field, enter a date.</span></span>
8. <span data-ttu-id="a3e60-119">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a3e60-119">Click OK.</span></span>
9. <span data-ttu-id="a3e60-120">Fara í Fjárhagur > Úthlutanir > Úthlutunarbækur.</span><span class="sxs-lookup"><span data-stu-id="a3e60-120">Go to General ledger > Allocations > Allocation journals.</span></span>
10. <span data-ttu-id="a3e60-121">Smellið á „Línur“.</span><span class="sxs-lookup"><span data-stu-id="a3e60-121">Click Lines.</span></span>
11. <span data-ttu-id="a3e60-122">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="a3e60-122">Click Post.</span></span>
12. <span data-ttu-id="a3e60-123">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="a3e60-123">Click Post.</span></span>

