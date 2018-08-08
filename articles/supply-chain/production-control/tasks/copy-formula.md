--- 
title: "Afrita formúlu"
description: "Þetta ferli leggur áherslu á stofnun formúlu sem inniheldur sömu efni og fyrirliggjandi formúla, en með minniháttar breytingum."
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: dd87ded3bcc20b94fae723424d9cc6b94049a1a5
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---
# <a name="copy-a-formula"></a><span data-ttu-id="49ce9-103">Afrita formúlu</span><span class="sxs-lookup"><span data-stu-id="49ce9-103">Copy a formula</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="49ce9-104">Þetta ferli leggur áherslu á stofnun formúlu sem inniheldur sömu efni og fyrirliggjandi formúla, en með minniháttar breytingum.</span><span class="sxs-lookup"><span data-stu-id="49ce9-104">This procedure focuses on creating a formula that includes the same ingredients as an existing formula, but with minor differences.</span></span> <span data-ttu-id="49ce9-105">til að stofna línur í formúlu, er Hægt að nota afritunaraðgerðina til að afrita fyrirliggjandi formúlu sem inniheldur flest efnanna sem þarf </span><span class="sxs-lookup"><span data-stu-id="49ce9-105">To create the formula lines, you can use the Copy function to copy an existing formula that has most of the ingredients that you need.</span></span> <span data-ttu-id="49ce9-106">Síðan er hægt að gera nauðsynlegar breytingar á einstaka línur í nýju útgáfunni.</span><span class="sxs-lookup"><span data-stu-id="49ce9-106">You can then make any necessary changes to the individual lines in the new version.</span></span> <span data-ttu-id="49ce9-107">Með því að nota afritunaraðgerðina þarf ekki að stofna margar formúlur sem eru nánast eins.</span><span class="sxs-lookup"><span data-stu-id="49ce9-107">By using the Copy function, you do not have to create multiple formulas that are almost identical.</span></span> <span data-ttu-id="49ce9-108">Sýnigögn gögn fyrirtækisins til að stofna verkið er USP2.</span><span class="sxs-lookup"><span data-stu-id="49ce9-108">The demo data company used to create this task is USP2.</span></span>


## <a name="create-a-formula"></a><span data-ttu-id="49ce9-109">Stofna formúlu</span><span class="sxs-lookup"><span data-stu-id="49ce9-109">Create a formula</span></span>
1. <span data-ttu-id="49ce9-110">Fara í upplýsingar um afurðastjórnun > Uppskriftir efni og formúlur > Formúlur.</span><span class="sxs-lookup"><span data-stu-id="49ce9-110">Go to Product information management > Bills of materials and formulas > Formulas.</span></span>
2. <span data-ttu-id="49ce9-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="49ce9-111">Click New.</span></span>
3. <span data-ttu-id="49ce9-112">Í reitinn Formúla skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="49ce9-112">In the Formula field, type a value.</span></span>
4. <span data-ttu-id="49ce9-113">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="49ce9-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="49ce9-114">Færið inn merkingarríkt nafn fyrir formúluna.</span><span class="sxs-lookup"><span data-stu-id="49ce9-114">Type a meaningful name for the formula.</span></span>  
5. <span data-ttu-id="49ce9-115">Í reitnum svæði skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="49ce9-115">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="49ce9-116">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="49ce9-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="49ce9-117">Í reitnum Vöruflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="49ce9-117">In the Item group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="49ce9-118">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="49ce9-118">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="49ce9-119">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="49ce9-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="49ce9-120">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="49ce9-120">Click Save.</span></span>

## <a name="copy-formula-lines"></a><span data-ttu-id="49ce9-121">Afrita formúlulínur</span><span class="sxs-lookup"><span data-stu-id="49ce9-121">Copy formula lines</span></span>
1. <span data-ttu-id="49ce9-122">Á Aðgerðasvæðinu skal smellt á Formúla.</span><span class="sxs-lookup"><span data-stu-id="49ce9-122">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="49ce9-123">Smellið á Afrit.</span><span class="sxs-lookup"><span data-stu-id="49ce9-123">Click Copy.</span></span>
3. <span data-ttu-id="49ce9-124">Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="49ce9-124">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="49ce9-125">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="49ce9-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="49ce9-126">Í reitnum Formúluútgáfa skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="49ce9-126">In the Formula version field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="49ce9-127">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="49ce9-127">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="49ce9-128">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="49ce9-128">Click OK.</span></span>

## <a name="adjust-copied-formula-lines"></a><span data-ttu-id="49ce9-129">Leiðrétta afrituðar formúlulínur</span><span class="sxs-lookup"><span data-stu-id="49ce9-129">Adjust copied formula lines</span></span>
1. <span data-ttu-id="49ce9-130">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="49ce9-130">In the list, mark the selected row.</span></span>
2. <span data-ttu-id="49ce9-131">Smellið á Eyða.</span><span class="sxs-lookup"><span data-stu-id="49ce9-131">Click Delete.</span></span>
3. <span data-ttu-id="49ce9-132">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="49ce9-132">Click Yes.</span></span>

## <a name="approve-formula"></a><span data-ttu-id="49ce9-133">Samþykkja formúlu</span><span class="sxs-lookup"><span data-stu-id="49ce9-133">Approve formula</span></span>
1. <span data-ttu-id="49ce9-134">Á Aðgerðasvæðinu skal smellt á Formúla.</span><span class="sxs-lookup"><span data-stu-id="49ce9-134">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="49ce9-135">Smellið á Samþykkja formúluna.</span><span class="sxs-lookup"><span data-stu-id="49ce9-135">Click Approve formula.</span></span>
3. <span data-ttu-id="49ce9-136">Í reitnum Samþykkt skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="49ce9-136">In the Approved by field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="49ce9-137">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="49ce9-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="49ce9-138">Smellið á Velja.</span><span class="sxs-lookup"><span data-stu-id="49ce9-138">Click Select.</span></span>
6. <span data-ttu-id="49ce9-139">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="49ce9-139">Click OK.</span></span>


