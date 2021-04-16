---
title: Stofna upprunalega fjárhagsáætlun og bakfæra síðan færslur bráðabirgðafjárhagsáætlunar í opinbera geiranum
description: Í þessu efnisatriði er að finna upplýsingar um hvernig á að stofna og bakfæra upprunalega fjárhagsáætlunarfærslu með því að nota fjárhagsáætlunarlíkan og víddargildi sem eru með bráðabirgðaupphæðir.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af037db40b0df3eeea163953d27c211e609cc02b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811240"
---
# <a name="create-an-original-budget-and-then-reverse-preliminary-budget-entries-in-the-public-sector"></a><span data-ttu-id="582d9-103">Stofna upprunalega fjárhagsáætlun og bakfæra síðan færslur bráðabirgðafjárhagsáætlunar í opinbera geiranum</span><span class="sxs-lookup"><span data-stu-id="582d9-103">Create an original budget and then reverse preliminary budget entries in the public sector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="582d9-104">Þegar upprunaleg færsla fjárhagsáætlunar er stofnuð og nota fjárhagsáætlunarlíkan og víddargildi sem innihalda bráðabirgða upphæð fjárhagsáætlunar, má bakfæra upphæð fjárhagsáætlunar.</span><span class="sxs-lookup"><span data-stu-id="582d9-104">When you create an original budget entry and use the budget model and dimension values that contain preliminary budget amounts, the preliminary budget amounts can be reversed.</span></span> <span data-ttu-id="582d9-105">Þetta ferli var stofnuð með PSUS sýnigögn fyrirtæki í hlutanum opinberi geirinn.</span><span class="sxs-lookup"><span data-stu-id="582d9-105">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="582d9-106">Fara í Fjárhagsáætlun > Færslur í fjárhagsáætlunarskrá.</span><span class="sxs-lookup"><span data-stu-id="582d9-106">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="582d9-107">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="582d9-107">Click New.</span></span>
3. <span data-ttu-id="582d9-108">Í reitnum fjárhagsáætlunarlíkan skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="582d9-108">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="582d9-109">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="582d9-109">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="582d9-110">Í reitnum kóði fjárhagsáætlunar skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="582d9-110">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="582d9-111">Á listanum, smella á Upprunalegu fjárhagsáætlun.</span><span class="sxs-lookup"><span data-stu-id="582d9-111">In the list, click Original budget.</span></span>
7. <span data-ttu-id="582d9-112">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="582d9-112">Click Save.</span></span>
8. <span data-ttu-id="582d9-113">Smellið á „Bæta við línu“.</span><span class="sxs-lookup"><span data-stu-id="582d9-113">Click Add line.</span></span>
9. <span data-ttu-id="582d9-114">Valfrjálst: Ef óskað er að breyta dagsetningu en það sem er í hausnum, færa inn nýja dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="582d9-114">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="582d9-115">Dagsetning lykils ákvarðar fjárhagstímabilið sem fjárhagsáætlun verður skráð í.</span><span class="sxs-lookup"><span data-stu-id="582d9-115">This date determines the fiscal period that the budget will be recorded to.</span></span>
10. <span data-ttu-id="582d9-116">Í reitnum Bókhaldsskipulag skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="582d9-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="582d9-117">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="582d9-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="582d9-118">Í reitnum víddargildi skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="582d9-118">In the Dimension values field, specify the desired values.</span></span>
13. <span data-ttu-id="582d9-119">Í reitinn Upphæð skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="582d9-119">In the Amount field, enter a number.</span></span>
14. <span data-ttu-id="582d9-120">Í reitnum gjaldmiðill skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="582d9-120">In the Currency field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="582d9-121">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="582d9-121">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="582d9-122">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="582d9-122">Click Save.</span></span>
17. <span data-ttu-id="582d9-123">Smelltu á Uppfæra innistæður fjárhagsáætlunar</span><span class="sxs-lookup"><span data-stu-id="582d9-123">Click Update budget balances.</span></span>
    * <span data-ttu-id="582d9-124">Valfrjálst: Hægt er að velja valkostinn Bakfæra bráðabirgðafjárhagsáætlunar.</span><span class="sxs-lookup"><span data-stu-id="582d9-124">Optional: You can select the Reverse preliminary budget option.</span></span> <span data-ttu-id="582d9-125">Athugið að hægt er að bakfæra allar færslur bráðabirgðafjárhagsáætlunar, eða aðeins færslur bráðabirgðafjárhagsáætlunar sem hafa fjárhagsáætlunarkóða sem er tilgreint.</span><span class="sxs-lookup"><span data-stu-id="582d9-125">Note that you can reverse all preliminary budget entries, or only the preliminary budget entries that have the budget code that you specify.</span></span>  
    * <span data-ttu-id="582d9-126">Til þess að velja valfrjáls, smellið á táknið Aflæsa efst á síðunni.</span><span class="sxs-lookup"><span data-stu-id="582d9-126">To make optional selections, click the Unlock icon at the top of the page.</span></span>  
18. <span data-ttu-id="582d9-127">Smelltu á Uppfæra.</span><span class="sxs-lookup"><span data-stu-id="582d9-127">Click Update.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]