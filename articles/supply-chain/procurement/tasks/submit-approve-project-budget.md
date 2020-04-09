---
title: Senda og samþykkja fjárhagsáætlun verks
description: Þetta ferli sýnir hvernig stofna og senda inn fjárhagsáætlun fyrir verkefni.
author: mkirknel
manager: AnnBe
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7aa7c301946b92b956f4b1b0f92985451ffe917e
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149436"
---
# <a name="submit-and-approve-project-budget"></a><span data-ttu-id="61c33-103">Senda og samþykkja fjárhagsáætlun verks</span><span class="sxs-lookup"><span data-stu-id="61c33-103">Submit and approve project budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="61c33-104">Þetta ferli sýnir hvernig stofna og senda inn fjárhagsáætlun fyrir verkefni.</span><span class="sxs-lookup"><span data-stu-id="61c33-104">This procedure shows you how to create and submit the budget for a project.</span></span> 

<span data-ttu-id="61c33-105">Þegar fjárhagsáætlun verks er stofnuð er hægt að slá inn áætlaðar tekjur og kostnað fyrir verkefni og nota þær síðan til að stýra raunverulegt verkfærslum.</span><span class="sxs-lookup"><span data-stu-id="61c33-105">When you create a project budget, you can enter estimated revenues and costs for a project, and then use those to control actual project transactions.</span></span> <span data-ttu-id="61c33-106">Í fjárhagsáætlun verks verður að senda allar upprunalegar fjárhagsáætlanir og endurskoðanir til verkflæðis verksins til samþykkis.</span><span class="sxs-lookup"><span data-stu-id="61c33-106">In project budgeting, all original budgets and revisions must be sent to project workflow for approval.</span></span> <span data-ttu-id="61c33-107">Verkflæði veitir aukna stjórn á ferlinu og stofna færslusögu breytinga.</span><span class="sxs-lookup"><span data-stu-id="61c33-107">Workflow gives you increased control over the process and creates a change history record.</span></span>

<span data-ttu-id="61c33-108">Þetta verkefni var stofnuð með því að nota USSI-gagnasafn.</span><span class="sxs-lookup"><span data-stu-id="61c33-108">This task was created using the USSI data set.</span></span>

1. <span data-ttu-id="61c33-109">Í **skoðunarrúðunni** ferðu í **Kerfiseiningar > Verkefnastjórnun og bókhald > Uppsetning > Verk > Öll verk**.</span><span class="sxs-lookup"><span data-stu-id="61c33-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="61c33-110">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="61c33-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="61c33-111">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="61c33-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="61c33-112">Í **Aðgerðarrúðunni** er smellt á **Áætlun**.</span><span class="sxs-lookup"><span data-stu-id="61c33-112">On the **Action Pane**, click **Plan**.</span></span>
5. <span data-ttu-id="61c33-113">Smelltu á **Fjárhagsáætlun verks**.</span><span class="sxs-lookup"><span data-stu-id="61c33-113">Click **Project budget**.</span></span>
6. <span data-ttu-id="61c33-114">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="61c33-114">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="61c33-115">Útvíkkaðu flýtiflipann **Kostnaður**.</span><span class="sxs-lookup"><span data-stu-id="61c33-115">Expand the **Cost** fastTab.</span></span>
8. <span data-ttu-id="61c33-116">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="61c33-116">Click **New**.</span></span>
9. <span data-ttu-id="61c33-117">Í reitnum **Færslugerð** skal velja valkostur.</span><span class="sxs-lookup"><span data-stu-id="61c33-117">In the **Transaction type** field, select an option.</span></span>
10. <span data-ttu-id="61c33-118">Í reitnum **Flokkur** færirðu inn eða velur gildi.</span><span class="sxs-lookup"><span data-stu-id="61c33-118">In the **Category** field, enter or select a value.</span></span>
11. <span data-ttu-id="61c33-119">Í reitnum **Upprunaleg fjárhagsáætlun** skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="61c33-119">In the **Original budget** field, enter a number.</span></span>
12. <span data-ttu-id="61c33-120">Útvíkkaðu flýtiflipann **Tekjur**.</span><span class="sxs-lookup"><span data-stu-id="61c33-120">Expand the **Revenues** fastTab.</span></span>
13. <span data-ttu-id="61c33-121">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="61c33-121">Click **New**.</span></span>
14. <span data-ttu-id="61c33-122">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="61c33-122">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="61c33-123">Í reitnum **Færslugerð** skal velja valkostur.</span><span class="sxs-lookup"><span data-stu-id="61c33-123">In the **Transaction type** field, select an option.</span></span>
16. <span data-ttu-id="61c33-124">Í reitnum **Flokkur** færirðu inn eða velur gildi.</span><span class="sxs-lookup"><span data-stu-id="61c33-124">In the **Category** field, enter or select a value.</span></span>
17. <span data-ttu-id="61c33-125">Í reitnum **Upprunaleg fjárhagsáætlun** skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="61c33-125">In the **Original budget** field, enter a number.</span></span>
18. <span data-ttu-id="61c33-126">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="61c33-126">Click **Save**.</span></span>
19. <span data-ttu-id="61c33-127">Smelltu á **Verkflæði**.</span><span class="sxs-lookup"><span data-stu-id="61c33-127">Click **Workflow**.</span></span>
20. <span data-ttu-id="61c33-128">Smelltu á **Senda**.</span><span class="sxs-lookup"><span data-stu-id="61c33-128">Click **Submit**.</span></span>
21. <span data-ttu-id="61c33-129">Í reitinn **Athugasemd** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="61c33-129">In the **Comment** field, type a value.</span></span>
22. <span data-ttu-id="61c33-130">Smelltu á **Senda**.</span><span class="sxs-lookup"><span data-stu-id="61c33-130">Click **Submit**.</span></span>

