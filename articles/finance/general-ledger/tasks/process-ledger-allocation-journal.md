---
title: Vinna úr færslubók kostnaðarúthlutunar
description: Þetta efni útskýrir hvernig á að vinna úr úthlutunarbeiðni í Dynamics 365 Finance.
author: aprilolson
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e89aa21f988d50bc1a922e053be0ff2dcd196268
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834418"
---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="cfead-103">Vinna úr færslubók kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="cfead-103">Process ledger allocation journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cfead-104">Þetta efni útskýrir hvernig á að vinna úr úthlutunarbeiðni.</span><span class="sxs-lookup"><span data-stu-id="cfead-104">This topic explains how to process an allocation request.</span></span> <span data-ttu-id="cfead-105">Notaðu síðuna Vinna úr úthlutunarbeiðni til að stofna úthlutunarbók sem hægt er að yfirfara og samþykki áður en bókað er í Fjárhag eða bóka beint í Fjárhag.</span><span class="sxs-lookup"><span data-stu-id="cfead-105">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="cfead-106">Áður en hægt er að stofna úthlutunarfærslubók verður að vera að minnsta kosti ein virk úthlutunarregla fjárhags.</span><span class="sxs-lookup"><span data-stu-id="cfead-106">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="cfead-107">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="cfead-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="cfead-108">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Fjárhagur > Úthlutanir > Vinna úthlutunarbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="cfead-108">In the navigation pane, go to **Modules > General ledger > Allocations > Process allocation request**.</span></span>
2. <span data-ttu-id="cfead-109">Í reitnum **Regla** velurðu skrána sem óskað er eftir af fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="cfead-109">In the **Rule** field, select the desired record in the drop-down menu.</span></span>
3. <span data-ttu-id="cfead-110">Í reitnum **Frá og með dagsetningu** er dagsetning færð inn.</span><span class="sxs-lookup"><span data-stu-id="cfead-110">In the **As of date** field, enter a date.</span></span>

    - <span data-ttu-id="cfead-111">**Frá og með dagsetningu** er mjög mikilvægt þegar Fjárhagur er gagnagjafi fyrir regluna.</span><span class="sxs-lookup"><span data-stu-id="cfead-111">The **As of Date** is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="cfead-112">Þessi dagsetning stýrir hvaða fjárhagsstöðu á að taka með í úthlutun.</span><span class="sxs-lookup"><span data-stu-id="cfead-112">This date controls which ledger balances to include for allocation.</span></span>  
    - <span data-ttu-id="cfead-113">Í reitnum **Núll** velurðu **Stöðva**.</span><span class="sxs-lookup"><span data-stu-id="cfead-113">In the **Zero source** field select **Stop**.</span></span> <span data-ttu-id="cfead-114">Þetta mun stöðva úthlutunarferlið og birta skilaboð um að núll upprunaupphæð sé valin.</span><span class="sxs-lookup"><span data-stu-id="cfead-114">This will stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  

4. <span data-ttu-id="cfead-115">Í reitnum **Valkostir tillögu** skal velja **Aðeins tillaga**.</span><span class="sxs-lookup"><span data-stu-id="cfead-115">In the **Proposal options** field, select **Proposal only**.</span></span> <span data-ttu-id="cfead-116">Veldu **Aðeins tillaga** til að endurskoða og samþykkja niðurstöðu í úthlutunarbókum áður en úthlutunin er bókuð í Fjárhag.</span><span class="sxs-lookup"><span data-stu-id="cfead-116">Select **Proposal only** to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
5. <span data-ttu-id="cfead-117">Dagsetning er rituð í reitinn Bókunardagsetning fjárhags.</span><span class="sxs-lookup"><span data-stu-id="cfead-117">In the GL posting date field, enter a date.</span></span>
6. <span data-ttu-id="cfead-118">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="cfead-118">Select **OK**.</span></span>
7. <span data-ttu-id="cfead-119">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Fjárhagur > Úthlutanir > Úthlutunarbækur**.</span><span class="sxs-lookup"><span data-stu-id="cfead-119">In the navigation pane, go to **Modules > General ledger > Allocations > Allocation journals**.</span></span>
8. <span data-ttu-id="cfead-120">Veldu **Línur**.</span><span class="sxs-lookup"><span data-stu-id="cfead-120">Select **Lines**.</span></span>
9. <span data-ttu-id="cfead-121">Veldu **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="cfead-121">Select **Post**.</span></span>
10. <span data-ttu-id="cfead-122">Veldu **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="cfead-122">Select **Post**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]