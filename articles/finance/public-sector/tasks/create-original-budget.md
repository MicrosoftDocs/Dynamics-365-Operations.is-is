---
title: Stofna upprunalega fjárhagsáætlun og bakfæra síðan færslur bráðabirgðafjárhagsáætlunar í opinbera geiranum
description: Þegar upprunaleg færsla fjárhagsáætlunar er stofnuð og nota fjárhagsáætlunarlíkan og víddargildi sem innihalda bráðabirgða upphæð fjárhagsáætlunar, má bakfæra upphæð fjárhagsáætlunar.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32d89216d49a743729de8910f738276cbddcd8bb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444473"
---
# <a name="create-an-original-budget-and-then-reverse-preliminary-budget-entries-in-the-public-sector"></a><span data-ttu-id="b2cb2-103">Stofna upprunalega fjárhagsáætlun og bakfæra síðan færslur bráðabirgðafjárhagsáætlunar í opinbera geiranum</span><span class="sxs-lookup"><span data-stu-id="b2cb2-103">Create an original budget and then reverse preliminary budget entries in the public sector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b2cb2-104">Þegar upprunaleg færsla fjárhagsáætlunar er stofnuð og nota fjárhagsáætlunarlíkan og víddargildi sem innihalda bráðabirgða upphæð fjárhagsáætlunar, má bakfæra upphæð fjárhagsáætlunar.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-104">When you create an original budget entry and use the budget model and dimension values that contain preliminary budget amounts, the preliminary budget amounts can be reversed.</span></span> <span data-ttu-id="b2cb2-105">Þetta ferli var stofnuð með PSUS sýnigögn fyrirtæki í hlutanum opinberi geirinn.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-105">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="b2cb2-106">Fara í Fjárhagsáætlun > Færslur í fjárhagsáætlunarskrá.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-106">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="b2cb2-107">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-107">Click New.</span></span>
3. <span data-ttu-id="b2cb2-108">Í reitnum fjárhagsáætlunarlíkan skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-108">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b2cb2-109">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-109">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="b2cb2-110">Í reitnum kóði fjárhagsáætlunar skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-110">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="b2cb2-111">Á listanum, smella á Upprunalegu fjárhagsáætlun.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-111">In the list, click Original budget.</span></span>
7. <span data-ttu-id="b2cb2-112">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-112">Click Save.</span></span>
8. <span data-ttu-id="b2cb2-113">Smellið á „Bæta við línu“.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-113">Click Add line.</span></span>
9. <span data-ttu-id="b2cb2-114">Valfrjálst: Ef óskað er að breyta dagsetningu en það sem er í hausnum, færa inn nýja dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-114">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="b2cb2-115">Dagsetning lykils ákvarðar fjárhagstímabilið sem fjárhagsáætlun verður skráð í.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-115">This date determines the fiscal period that the budget will be recorded to.</span></span>
10. <span data-ttu-id="b2cb2-116">Í reitnum Bókhaldsskipulag skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="b2cb2-117">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="b2cb2-118">Í reitnum víddargildi skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-118">In the Dimension values field, specify the desired values.</span></span>
13. <span data-ttu-id="b2cb2-119">Í reitinn Upphæð skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-119">In the Amount field, enter a number.</span></span>
14. <span data-ttu-id="b2cb2-120">Í reitnum gjaldmiðill skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-120">In the Currency field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="b2cb2-121">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-121">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="b2cb2-122">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-122">Click Save.</span></span>
17. <span data-ttu-id="b2cb2-123">Smelltu á Uppfæra innistæður fjárhagsáætlunar</span><span class="sxs-lookup"><span data-stu-id="b2cb2-123">Click Update budget balances.</span></span>
    * <span data-ttu-id="b2cb2-124">Valfrjálst: Hægt er að velja valkostinn Bakfæra bráðabirgðafjárhagsáætlunar.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-124">Optional: You can select the Reverse preliminary budget option.</span></span> <span data-ttu-id="b2cb2-125">Athugið að hægt er að bakfæra allar færslur bráðabirgðafjárhagsáætlunar, eða aðeins færslur bráðabirgðafjárhagsáætlunar sem hafa fjárhagsáætlunarkóða sem er tilgreint.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-125">Note that you can reverse all preliminary budget entries, or only the preliminary budget entries that have the budget code that you specify.</span></span>  
    * <span data-ttu-id="b2cb2-126">Til þess að velja valfrjáls, smellið á táknið Aflæsa efst á síðunni.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-126">To make optional selections, click the Unlock icon at the top of the page.</span></span>  
18. <span data-ttu-id="b2cb2-127">Smelltu á Uppfæra.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-127">Click Update.</span></span>

