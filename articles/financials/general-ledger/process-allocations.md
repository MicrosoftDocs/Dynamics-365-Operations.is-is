---
title: "Vinna úr úthlutunum"
description: "Þessi grein veitir upplýsingar um úthlutanir, valkosti fyrir vinnslu þeirra í Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition og hvernig má nota þá í fjárhagsáætlunargerð. Úthlutanir eru notaðar til að dreifa upphæðum þvert á margar samsetningar fjárhagslykla. Þær auðvelda að tryggja að tekjur eða útgjöld séu innheimtar frá rétta viðfanginu í bókhaldi."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cb12e24fcb8e8c91f90b91e2fdb3039dd1735ca3
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="process-allocations"></a><span data-ttu-id="30d68-105">Vinna úr úthlutunum</span><span class="sxs-lookup"><span data-stu-id="30d68-105">Process allocations</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="30d68-106">Þessi grein veitir upplýsingar um úthlutanir, valkosti fyrir vinnslu þeirra í Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition og hvernig má nota þá í fjárhagsáætlunargerð.</span><span class="sxs-lookup"><span data-stu-id="30d68-106">This article provides information about allocations, the options for processing them in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, and how they can be used in budget planning.</span></span> <span data-ttu-id="30d68-107">Úthlutanir eru notaðar til að dreifa upphæðum þvert á margar samsetningar fjárhagslykla.</span><span class="sxs-lookup"><span data-stu-id="30d68-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="30d68-108">Þær auðvelda að tryggja að tekjur eða útgjöld séu innheimtar frá rétta viðfanginu í bókhaldi.</span><span class="sxs-lookup"><span data-stu-id="30d68-108">They help guarantee that expenses or revenue is charged to the correct object in accounting.</span></span>

<span data-ttu-id="30d68-109">Microsoft Dynamics 365 for Finance and Operations býður upp á eftirfarandi getu til að styðja þetta ferli:</span><span class="sxs-lookup"><span data-stu-id="30d68-109">Microsoft Dynamics 365 for Finance and Operations provides the following capabilities to support this process:</span></span>

-   <span data-ttu-id="30d68-110">Úthluta færsluupphæðum handvirkt með því að nota aðgerðina „Skipta“ í dreifingu fjárhagsupphæðar eða með því að nota sjálfgefin sniðmát fjárhagsvídda við skjal.</span><span class="sxs-lookup"><span data-stu-id="30d68-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="30d68-111">Frekari upplýsingar eru í [Dreifing á fjárhagsupphæð.](../accounts-payable/accounting-distributions.md)</span><span class="sxs-lookup"><span data-stu-id="30d68-111">For more information, see [Accounting distributions.](../accounts-payable/accounting-distributions.md)</span></span>
-   <span data-ttu-id="30d68-112">Úthluta sjálfkrafa færsluupphæðum á grundvelli úthlutunarskilmála sem eru tilgreindir á einstökum aðallyklum.</span><span class="sxs-lookup"><span data-stu-id="30d68-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="30d68-113">Úthlutun lykilfærslna verður mynduð fyrir hverja færslubók á grundvelli hlutfalls og áfangastaðar fjárhagsreikninga hvenær sem bókhaldsfærsla uppfyllir skilyrði sem eru skilgreind sem upprunafjárhagsreikningur.</span><span class="sxs-lookup"><span data-stu-id="30d68-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span>
-   <span data-ttu-id="30d68-114">Úthluta sjálfkrafa fjárhagsstöður eða föstum upphæðum samkvæmt úthlutunarreglum fjárhags.</span><span class="sxs-lookup"><span data-stu-id="30d68-114">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="30d68-115">Úthlutunarreglur fjárhags eru unnar með úthlutunarbókum með reglulegu millibili.</span><span class="sxs-lookup"><span data-stu-id="30d68-115">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> 

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="30d68-116">Úthlutun í fjárhagsáætlunargerð</span><span class="sxs-lookup"><span data-stu-id="30d68-116">Allocations in budget planning</span></span>

<span data-ttu-id="30d68-117">Hægt er að nota úthlutunarreglur fjárhags fyrir fjárhagsáætlunargerð.</span><span class="sxs-lookup"><span data-stu-id="30d68-117">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="30d68-118">Þegar notaðar eru úthlutunarreglur fjárhags í fjárhagsáætlunargerð virka úthlutunarreglur á sama hátt og þær myndu gera í fjárhag, en upprunagögn og áfangastaður gagna kemur úr fjárhagsáætlunargerð.</span><span class="sxs-lookup"><span data-stu-id="30d68-118">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="30d68-119">Hægt er að velja handvirkt úthlutunarreglur fjárhags til að nota fyrir fjárhagsáætlanir.</span><span class="sxs-lookup"><span data-stu-id="30d68-119">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="30d68-120">Einnig er hægt að nota úthlutunaráætlun sem keyrir sem hluti af verkflæðisferli.</span><span class="sxs-lookup"><span data-stu-id="30d68-120">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="30d68-121">Hægt er að nota úthlutunarreglur fjárhags innan samstæðu fyrir fjárhagsáætlunargerð.</span><span class="sxs-lookup"><span data-stu-id="30d68-121">You can’t use intercompany ledger allocation rules for budget planning.</span></span>






