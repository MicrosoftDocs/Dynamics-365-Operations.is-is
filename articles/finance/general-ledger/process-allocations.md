---
title: Vinna úr úthlutunum
description: Þessi grein veitir upplýsingar um úthlutanir, valkosti fyrir vinnslu þeirra í Microsoft Dynamics 365 Finance og hvernig nota má þær í fjárhagsáætlunargerð. Úthlutanir eru notaðar til að dreifa upphæðum þvert á margar samsetningar fjárhagslykla. Þær auðvelda að tryggja að tekjur eða útgjöld séu innheimtar frá rétta viðfanginu í bókhaldi.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4c8216ebdd1f26601743e6b35849be0813d06b4a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444388"
---
# <a name="process-allocations"></a><span data-ttu-id="d2c23-105">Vinna úr úthlutunum</span><span class="sxs-lookup"><span data-stu-id="d2c23-105">Process allocations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d2c23-106">Þessi grein veitir upplýsingar um úthlutanir, valkosti fyrir vinnslu þeirra og hvernig nota má þær í fjárhagsáætlunargerð.</span><span class="sxs-lookup"><span data-stu-id="d2c23-106">This article provides information about allocations, the options for processing them, and how they can be used in budget planning.</span></span> <span data-ttu-id="d2c23-107">Úthlutanir eru notaðar til að dreifa upphæðum þvert á margar samsetningar fjárhagslykla.</span><span class="sxs-lookup"><span data-stu-id="d2c23-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="d2c23-108">Þær auðvelda að tryggja að tekjur eða útgjöld séu innheimtar frá rétta viðfanginu í bókhaldi.</span><span class="sxs-lookup"><span data-stu-id="d2c23-108">They help ensure that expenses or revenues are charged to the correct object in accounting.</span></span>

<span data-ttu-id="d2c23-109">Eftirfarandi getu styður þetta ferli:</span><span class="sxs-lookup"><span data-stu-id="d2c23-109">The following capabilities support this process:</span></span>

-   <span data-ttu-id="d2c23-110">Úthluta færsluupphæðum handvirkt með því að nota aðgerðina „Skipta“ í dreifingu fjárhagsupphæðar eða með því að nota sjálfgefin sniðmát fjárhagsvídda við skjal.</span><span class="sxs-lookup"><span data-stu-id="d2c23-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="d2c23-111">Frekari upplýsingar eru í [Dreifingar á fjárhagsupphæðir](../accounts-payable/accounting-distributions.md).</span><span class="sxs-lookup"><span data-stu-id="d2c23-111">For more information, see [Accounting distributions](../accounts-payable/accounting-distributions.md).</span></span>
-   <span data-ttu-id="d2c23-112">Úthluta sjálfkrafa færsluupphæðum á grundvelli úthlutunarskilmála sem eru tilgreindir á einstökum aðallyklum.</span><span class="sxs-lookup"><span data-stu-id="d2c23-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="d2c23-113">Úthlutun lykilfærslna verður mynduð fyrir hverja færslubók á grundvelli hlutfalls og áfangastaðar fjárhagsreikninga hvenær sem bókhaldsfærsla uppfyllir skilyrði sem eru skilgreind sem upprunafjárhagsreikningur.</span><span class="sxs-lookup"><span data-stu-id="d2c23-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span> <span data-ttu-id="d2c23-114">Nánari upplýsingar er að finna í [Úthlutunarskilmálar aðallykils](../general-ledger/main-account-allocation-terms.md)</span><span class="sxs-lookup"><span data-stu-id="d2c23-114">For more information, see [Main account allocation terms](../general-ledger/main-account-allocation-terms.md)</span></span>
-   <span data-ttu-id="d2c23-115">Úthluta sjálfkrafa fjárhagsstöður eða föstum upphæðum samkvæmt úthlutunarreglum fjárhags.</span><span class="sxs-lookup"><span data-stu-id="d2c23-115">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="d2c23-116">Úthlutunarreglur fjárhags eru unnar með úthlutunarbókum með reglulegu millibili.</span><span class="sxs-lookup"><span data-stu-id="d2c23-116">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> <span data-ttu-id="d2c23-117">Frekari upplýsingar er að finna í [Úthlutunarreglur](../general-ledger/ledger-allocation-rules.md).</span><span class="sxs-lookup"><span data-stu-id="d2c23-117">For more information, see [Allocation rules](../general-ledger/ledger-allocation-rules.md).</span></span>

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="d2c23-118">Úthlutun í fjárhagsáætlunargerð</span><span class="sxs-lookup"><span data-stu-id="d2c23-118">Allocations in budget planning</span></span>

<span data-ttu-id="d2c23-119">Hægt er að nota úthlutunarreglur fjárhags fyrir fjárhagsáætlunargerð.</span><span class="sxs-lookup"><span data-stu-id="d2c23-119">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="d2c23-120">Þegar notaðar eru úthlutunarreglur fjárhags í fjárhagsáætlunargerð virka úthlutunarreglur á sama hátt og þær myndu gera í fjárhag, en upprunagögn og áfangastaður gagna kemur úr fjárhagsáætlunargerð.</span><span class="sxs-lookup"><span data-stu-id="d2c23-120">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="d2c23-121">Hægt er að velja handvirkt úthlutunarreglur fjárhags til að nota fyrir fjárhagsáætlanir.</span><span class="sxs-lookup"><span data-stu-id="d2c23-121">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="d2c23-122">Einnig er hægt að nota úthlutunaráætlun sem keyrir sem hluti af verkflæðisferli.</span><span class="sxs-lookup"><span data-stu-id="d2c23-122">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="d2c23-123">Hægt er að nota úthlutunarreglur fjárhags innan samstæðu fyrir fjárhagsáætlunargerð.</span><span class="sxs-lookup"><span data-stu-id="d2c23-123">You can’t use intercompany ledger allocation rules for budget planning.</span></span>

