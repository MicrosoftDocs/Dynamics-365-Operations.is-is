--- 
title: "Búa til aðferð við stigagjöf fyrir tilboðsbeiðnir"
description: "Þessi verklýsing sýnir hvernig á að stofna aðferð við stigagjöf."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6d72678db60254801c6c899f4d405f1c59de8d65
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-scoring-method-for-rfqs"></a><span data-ttu-id="de3ee-103">Búa til aðferð við stigagjöf fyrir tilboðsbeiðnir</span><span class="sxs-lookup"><span data-stu-id="de3ee-103">Create a scoring method for RFQs</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="de3ee-104">Þessi verklýsing sýnir hvernig á að stofna aðferð við stigagjöf.</span><span class="sxs-lookup"><span data-stu-id="de3ee-104">This procedure shows you how to create a scoring method.</span></span> <span data-ttu-id="de3ee-105">Aðferð við Stigagjöf er safn skilyrða sem hægt er að nota til að bera saman tilboð sem eru send í svari við tilboðsbeiðni (RFQ).</span><span class="sxs-lookup"><span data-stu-id="de3ee-105">A scoring method is a set of criteria that can be used to compare bids that are sent in reply to a request for quotation (RFQ).</span></span> <span data-ttu-id="de3ee-106">Til dæmis gæti átt að meta lánardrottin eftir fyrri frammistöðu, eða meta hvort fyrirtækið er umhverfisvænn eða góður samstarfsaðili, eða bera saman tilboð sem er byggt á verði.</span><span class="sxs-lookup"><span data-stu-id="de3ee-106">For example, you might want to rate a vendor on past performance, or rate whether the company is environmentally friendly or a good collaborator, or you might want to compare bids based on price.</span></span> <span data-ttu-id="de3ee-107">Aðferð við stigagjöf getur verið tengt við gerð beiðni sem sjálfgefin aðferð við stigagjöf fyrir beiðnir um tilboð af þeirri gerð.</span><span class="sxs-lookup"><span data-stu-id="de3ee-107">The scoring method can be associated with a solicitation type as the default scoring method for RFQs of that type.</span></span> <span data-ttu-id="de3ee-108">Þessum verkefnum myndi venjulega að framkvæma af Innkaupastjóra.</span><span class="sxs-lookup"><span data-stu-id="de3ee-108">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="de3ee-109">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="de3ee-109">You can use this procedure in demo data company USMF or on your own data.</span></span>

1. <span data-ttu-id="de3ee-110">Farið í Innkaup og aðföng > Uppsetning > Tilboðsbeiðni > Aðferð við stigagjöf.</span><span class="sxs-lookup"><span data-stu-id="de3ee-110">Go to Procurement and sourcing > Setup > Request for quotation > Scoring method.</span></span>
2. <span data-ttu-id="de3ee-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="de3ee-111">Click New.</span></span>
3. <span data-ttu-id="de3ee-112">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="de3ee-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="de3ee-113">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="de3ee-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="de3ee-114">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="de3ee-114">Click Save.</span></span>
6. <span data-ttu-id="de3ee-115">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="de3ee-115">Click New.</span></span>
7. <span data-ttu-id="de3ee-116">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="de3ee-116">In the Name field, type a value.</span></span>
8. <span data-ttu-id="de3ee-117">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="de3ee-117">In the Description field, type a value.</span></span>
    * <span data-ttu-id="de3ee-118">Þessi lýsing er sýnd ásamt heiti aðferðar við stigagjöf þegar valinn er stigagjöf fyrir beiðni um TILBOÐ.</span><span class="sxs-lookup"><span data-stu-id="de3ee-118">This description is shown along with the scoring method name when a scoring method is selected for an RFQ.</span></span>  
9. <span data-ttu-id="de3ee-119">Í reitinn Svið frá skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="de3ee-119">In the Range from field, enter a number.</span></span>
    * <span data-ttu-id="de3ee-120">Sviðið takmarkar hvaða innkaupastjóra getur færa inn sem stig.</span><span class="sxs-lookup"><span data-stu-id="de3ee-120">The range limits what the procurement professional can enter as a score.</span></span> <span data-ttu-id="de3ee-121">Þegar mörg skilyrði fyrir stigagjöf eru á beiðni um TILBOÐ, eru stigin sem hafa verið færð inn lögð saman og útkoman er gerð tiltæk til að leyfa samanburð á tilboðunum.</span><span class="sxs-lookup"><span data-stu-id="de3ee-121">When there are multiple scoring criteria on an RFQ, the scores that have been entered are added to each other and the sum is made available to allow the bids to be compared.</span></span>  
10. <span data-ttu-id="de3ee-122">Í reitinn Svið til skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="de3ee-122">In the Range to field, enter a number.</span></span>
11. <span data-ttu-id="de3ee-123">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="de3ee-123">Click New.</span></span>
12. <span data-ttu-id="de3ee-124">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="de3ee-124">In the Name field, type a value.</span></span>
13. <span data-ttu-id="de3ee-125">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="de3ee-125">In the Description field, type a value.</span></span>
14. <span data-ttu-id="de3ee-126">Í reitinn Svið frá skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="de3ee-126">In the Range from field, enter a number.</span></span>
15. <span data-ttu-id="de3ee-127">Í reitinn Svið til skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="de3ee-127">In the Range to field, enter a number.</span></span>


