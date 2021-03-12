---
title: Vinna úr færslubók kostnaðarúthlutunar
description: Þetta efni útskýrir hvernig á að vinna úr úthlutunarbeiðni í Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a7e8c3ef6fa85daec2a191b433b1ec4ece441ee
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968480"
---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="a65f2-103">Vinna úr færslubók kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="a65f2-103">Process ledger allocation journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a65f2-104">Þetta efni útskýrir hvernig á að vinna úr úthlutunarbeiðni.</span><span class="sxs-lookup"><span data-stu-id="a65f2-104">This topic explains how to process an allocation request.</span></span> <span data-ttu-id="a65f2-105">Notaðu síðuna Vinna úr úthlutunarbeiðni til að stofna úthlutunarbók sem hægt er að yfirfara og samþykki áður en bókað er í Fjárhag eða bóka beint í Fjárhag.</span><span class="sxs-lookup"><span data-stu-id="a65f2-105">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="a65f2-106">Áður en hægt er að stofna úthlutunarfærslubók verður að vera að minnsta kosti ein virk úthlutunarregla fjárhags.</span><span class="sxs-lookup"><span data-stu-id="a65f2-106">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="a65f2-107">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="a65f2-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="a65f2-108">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Fjárhagur > Úthlutanir > Vinna úthlutunarbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="a65f2-108">In the navigation pane, go to **Modules > General ledger > Allocations > Process allocation request**.</span></span>
2. <span data-ttu-id="a65f2-109">Í reitnum **Regla** velurðu skrána sem óskað er eftir af fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="a65f2-109">In the **Rule** field, select the desired record in the drop-down menu.</span></span>
3. <span data-ttu-id="a65f2-110">Í reitnum **Frá og með dagsetningu** er dagsetning færð inn.</span><span class="sxs-lookup"><span data-stu-id="a65f2-110">In the **As of date** field, enter a date.</span></span>

    - <span data-ttu-id="a65f2-111">**Frá og með dagsetningu** er mjög mikilvægt þegar Fjárhagur er gagnagjafi fyrir regluna.</span><span class="sxs-lookup"><span data-stu-id="a65f2-111">The **As of Date** is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="a65f2-112">Þessi dagsetning stýrir hvaða fjárhagsstöðu á að taka með í úthlutun.</span><span class="sxs-lookup"><span data-stu-id="a65f2-112">This date controls which ledger balances to include for allocation.</span></span>  
    - <span data-ttu-id="a65f2-113">Í reitnum **Núll** velurðu **Stöðva**.</span><span class="sxs-lookup"><span data-stu-id="a65f2-113">In the **Zero source** field select **Stop**.</span></span> <span data-ttu-id="a65f2-114">Þetta mun stöðva úthlutunarferlið og birta skilaboð um að núll upprunaupphæð sé valin.</span><span class="sxs-lookup"><span data-stu-id="a65f2-114">This will stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  

4. <span data-ttu-id="a65f2-115">Í reitnum **Valkostir tillögu** skal velja **Aðeins tillaga**.</span><span class="sxs-lookup"><span data-stu-id="a65f2-115">In the **Proposal options** field, select **Proposal only**.</span></span> <span data-ttu-id="a65f2-116">Veldu **Aðeins tillaga** til að endurskoða og samþykkja niðurstöðu í úthlutunarbókum áður en úthlutunin er bókuð í Fjárhag.</span><span class="sxs-lookup"><span data-stu-id="a65f2-116">Select **Proposal only** to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
5. <span data-ttu-id="a65f2-117">Dagsetning er rituð í reitinn Bókunardagsetning fjárhags.</span><span class="sxs-lookup"><span data-stu-id="a65f2-117">In the GL posting date field, enter a date.</span></span>
6. <span data-ttu-id="a65f2-118">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a65f2-118">Select **OK**.</span></span>
7. <span data-ttu-id="a65f2-119">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Fjárhagur > Úthlutanir > Úthlutunarbækur**.</span><span class="sxs-lookup"><span data-stu-id="a65f2-119">In the navigation pane, go to **Modules > General ledger > Allocations > Allocation journals**.</span></span>
8. <span data-ttu-id="a65f2-120">Veldu **Línur**.</span><span class="sxs-lookup"><span data-stu-id="a65f2-120">Select **Lines**.</span></span>
9. <span data-ttu-id="a65f2-121">Veldu **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="a65f2-121">Select **Post**.</span></span>
10. <span data-ttu-id="a65f2-122">Veldu **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="a65f2-122">Select **Post**.</span></span>

