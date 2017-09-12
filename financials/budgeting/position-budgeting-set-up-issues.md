---
title: "Setja upp fjárhagsáætlunargerðar stöðu"
description: "Þetta efnisatriði veitir svör við spurningum sem gætu vaknað þegar verið er að skilgreina stöðu fjárhagsáætlunargerðar. Það svarar algengum spurningum um hvernig á að búa til kostnaðarþætti fjárhagsáætlunar, launaflokka og launahintanet."
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmBudgetPurposeType, HcmPositionForecast
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 88253
ms.assetid: c44df01b-8700-4022-b4c6-c4b1cb84d31d
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 421520fcd1b215a19c126ccea51b025977552448
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---

# <a name="position-budgeting-troubleshooting"></a><span data-ttu-id="a331a-104">Setja upp fjárhagsáætlunargerðar stöðu</span><span class="sxs-lookup"><span data-stu-id="a331a-104">Position budgeting troubleshooting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a331a-105">Þetta efnisatriði veitir svör við spurningum sem gætu vaknað þegar verið er að skilgreina stöðu fjárhagsáætlunargerðar.</span><span class="sxs-lookup"><span data-stu-id="a331a-105">This article provides answers to questions that you might have when you configure position budgeting.</span></span> <span data-ttu-id="a331a-106">Það svarar algengum spurningum um hvernig á að búa til kostnaðarþætti fjárhagsáætlunar, launaflokka og launahintanet.</span><span class="sxs-lookup"><span data-stu-id="a331a-106">It addresses frequently asked questions about how to create budget cost elements, compensation groups, and compensation grids.</span></span> 

<a name="why-cant-i-find-the-forecast-position-page-in-human-resources"></a><span data-ttu-id="a331a-107">Af hverju finnst ekki spástöðu síðan í mannauði?</span><span class="sxs-lookup"><span data-stu-id="a331a-107">Why can’t I find the forecast position page in Human resources?</span></span>
---------------------------------------------------------------

<span data-ttu-id="a331a-108">Spástöður hafa verið fluttar í Fjárhagsáætlun.</span><span class="sxs-lookup"><span data-stu-id="a331a-108">Forecast positions have been moved to Budgeting.</span></span>

## <a name="why-cant-i-delete-a-budget-cost-element"></a><span data-ttu-id="a331a-109">Af hverju get ég ekki eytt kostnaðareiningum fjárhagsáætlunar?</span><span class="sxs-lookup"><span data-stu-id="a331a-109">Why can’t I delete a budget cost element?</span></span>
<span data-ttu-id="a331a-110">Ekki er hægt að eyða kostnaðareiningum fjárhagsáætlunar sem er úthlutað á spástöðuna.</span><span class="sxs-lookup"><span data-stu-id="a331a-110">You can’t delete a budget cost element that is assigned to a forecast position.</span></span> <span data-ttu-id="a331a-111">Áður en hægt er að eyða kostnaðareiningu fjárhagsáætlunar þarf að fjarlægja hana úr öllum spástöðum.</span><span class="sxs-lookup"><span data-stu-id="a331a-111">Before you can delete a budget cost element, you must remove it from all forecast positions.</span></span> <span data-ttu-id="a331a-112">**Ábending:** Til að finna allar stöður sem kostnaðareiningu fjárhagsáætlunar er úthlutað til , veljið kostnaðareininguna á síðunni **Kostnaðareiningar Fjárhagsáætlunar** og smellið síðan á **Uppfæra stöður**.</span><span class="sxs-lookup"><span data-stu-id="a331a-112">**Tip:** To find all the positions that a budget cost element is assigned to, select the cost element on the **Budget cost elements** page, and then click **Update positions**.</span></span> <span data-ttu-id="a331a-113">Stöður sem nota á kostnaðareiningum eru talin upp í efra hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="a331a-113">The positions that use the cost element are listed in the upper grid.</span></span>

## <a name="how-can-i-remove-a-cost-element-from-multiple-forecast-positions-without-opening-each-one"></a><span data-ttu-id="a331a-114">Er einhver leið til að fjarlægja kostnaðarþátt úr mörgum spárstöðum án þess að opna hvern og einn?</span><span class="sxs-lookup"><span data-stu-id="a331a-114">How can I remove a cost element from multiple forecast positions without opening each one?</span></span>
<span data-ttu-id="a331a-115">Ekki er hægt að fjarlægja kostnaðareiningu.</span><span class="sxs-lookup"><span data-stu-id="a331a-115">You can’t remove a cost element.</span></span> <span data-ttu-id="a331a-116">Ef upphafs- og lokadagsetningum er breytt þannig að þær falli utan dagsetningar ferlis fjárhagsáætlunargerðar verður kostnaðareiningum ekki lengur úthlutað á spástöður í því ferli fjárhagsáætlunargerðar.</span><span class="sxs-lookup"><span data-stu-id="a331a-116">However, if you change the start and end dates so that they are outside the budget planning cycle dates, the cost element will no longer be assigned to the forecast positions in that budget planning cycle.</span></span> <span data-ttu-id="a331a-117">Til að gera þessa breytingu skal opna kostnaðareiningu fjárhagsáætlunar, og síðan, á flýtiflipanum **Kostnaðarútreikningur** skal smellt á **Breyta dagsetningum**, og breyta upphafsdagsetningu eða lokadegi.</span><span class="sxs-lookup"><span data-stu-id="a331a-117">To make this change, open the budget cost element, and then, on the **Cost calculation** FastTab, click **Change dates**, and change the effective date or expiration date.</span></span> <span data-ttu-id="a331a-118">Smellið á **Í lagi** til að uppfæra sjálfkrafa allar spástöður sem kostnaðareiningu er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="a331a-118">Then click **OK** to automatically update all forecast positions that the cost element is assigned to.</span></span> <span data-ttu-id="a331a-119">**Vísbending:** Ef þessi aðferð er notuð, skal hafa í huga að hún fjarlægir kostnaðareiningu fjárhagsáætlunar úr **öllum** spástöðum þar sem upphafs- og lokadagsetningarnar eru ekki lengur innan viðeigandi tímabils.</span><span class="sxs-lookup"><span data-stu-id="a331a-119">**Tip:** If you use this method, be aware that it removes the budget cost element from **all** forecast positions where the start and end dates are no longer within the appropriate range.</span></span> <span data-ttu-id="a331a-120">Ef þetta er ekki það sem til stóð þarf að opna hverja spástöðu sem á að fjarlægja kostnaðareiningu fjárhagsáætlunar úr og gera breytingar handvirkt.</span><span class="sxs-lookup"><span data-stu-id="a331a-120">If this effect isn't what you intend, you must open each forecast position that you want to remove the budget cost element from and manually make the change.</span></span>

## <a name="why-cant-i-enter-an-annual-amount-on-the-cost-calculation-fasttab-for-the-budget-cost-element"></a><span data-ttu-id="a331a-121">Af hverju get ég ekki slegið inn árlega upphæð í flýtiflipanum Útreikningur kostnaðar fyrir kostnaðareiningu fjárhagsáætlunar?</span><span class="sxs-lookup"><span data-stu-id="a331a-121">Why can’t I enter an annual amount on the Cost calculation FastTab for the budget cost element?</span></span>
<span data-ttu-id="a331a-122">Ekki er hægt að slá inn árlega upphæð ef það eru kostnaðareiningar fjárhagsáætlunar á flýtiflipanum **Grundvöllur útreikninga** því kerfið krefst prósentuhlutfalls til að reikna út gildi.</span><span class="sxs-lookup"><span data-stu-id="a331a-122">You can’t enter an annual amount if there are budget cost elements on the **Calculation basis** FastTab, because the system requires a percentage in order to calculate the value.</span></span> <span data-ttu-id="a331a-123">Til að breyta þessu gildi skal fjarlægja allar kostnaðareiningar fjárhagsáætlunar úr flýtiflipanum **Grundvöllur útreikninga**.</span><span class="sxs-lookup"><span data-stu-id="a331a-123">To change the value, remove all budget cost elements from the **Calculation basis** FastTab.</span></span>

## <a name="why-cant-i-change-the-budget-cost-type-from-earning-to-another-budget-cost-type"></a><span data-ttu-id="a331a-124">Af hverju get ég ekki breytt kostnaðargerð fjárhagsáætlunar úr tekjum í aðra kostnaðargerð fjárhagsáætlunar?</span><span class="sxs-lookup"><span data-stu-id="a331a-124">Why can’t I change the budget cost type from earning to another budget cost type?</span></span>
<span data-ttu-id="a331a-125">Sumar kostnaðargerðir fjárhagsáætlunar nota kostnaðarþáttinn tekjur sem reiknigrundvöll.</span><span class="sxs-lookup"><span data-stu-id="a331a-125">Some budget cost elements use the earning cost element as a calculation basis.</span></span> <span data-ttu-id="a331a-126">Til að breyta svæðinu **Kostnaðargerð fjárhagsáætlunar** skal fjarlægja kostnaðareiningu tekna úr flýtiflipanum **Grundvöllur útreikninga** í öllum einingum fjárhagsáætlunar.</span><span class="sxs-lookup"><span data-stu-id="a331a-126">To change the **Budget cost type** field, remove the earning cost element from the **Calculation basis** FastTab of all budget cost elements.</span></span>

## <a name="why-cant-i-change-the-date-on-budget-cost-element-lines-for-a-budget-cost-element"></a><span data-ttu-id="a331a-127">Af hverju get ég ekki breytt dagsetningu einingar kostnaðarlínu fjárhagsáætlunar fyrir kostnaðareiningu fjárhagsáætlunar?</span><span class="sxs-lookup"><span data-stu-id="a331a-127">Why can’t I change the date on budget cost element lines for a budget cost element?</span></span>
<span data-ttu-id="a331a-128">Ekki er hægt að breyta dagsetningunni á línu kostnaðareiningar fjárhagsáætlunar þegar kostnaðareining fjárhagsáætlunar er notuð með spástöðu.</span><span class="sxs-lookup"><span data-stu-id="a331a-128">You can’t change the date on the budget cost element line when a budget cost element is used by a forecast position.</span></span> <span data-ttu-id="a331a-129">Þessar takmarkanir eru til að tryggja að spástöður séu alltaf innan viðmiðunarreglna kostnaðareininga fjárhagsáætlunar.</span><span class="sxs-lookup"><span data-stu-id="a331a-129">This limitation helps guarantee that the forecast positions are always within the guidelines of the budget cost element.</span></span> <span data-ttu-id="a331a-130">Til að breyta dagsetningunni, skal á flýtiflipanum **Kostnaðarútreikningur** smella á **Breyta dagsetningum**, og færið inn nýja dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="a331a-130">To change the date, on the **Cost calculation** FastTab, click **Change dates**, and enter the new dates.</span></span> <span data-ttu-id="a331a-131">Smellið síðan á **Í lagi** til að uppfæra allar stöður sem kostnaðareiningunni er úthlutað sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="a331a-131">Then click **OK** to update the positions that the cost element is assigned to.</span></span>

## <a name="why-cant-i-change-the-costs-for-a-budget-cost-element-on-the-compensation-group-page"></a><span data-ttu-id="a331a-132">Af hverju get ég ekki breytt kostnaði fyrir kostnaðareiningu fjárhagsáætlunar í skjámyndinni Launaflokkur?</span><span class="sxs-lookup"><span data-stu-id="a331a-132">Why can’t I change the costs for a budget cost element on the Compensation group page?</span></span>
<span data-ttu-id="a331a-133">Aðeins er hægt að stofna og breyta kostnaðareiningum fjárhagsáætlunar á síðunni **Kostnaðareiningar Fjárhagsáætlunar**.</span><span class="sxs-lookup"><span data-stu-id="a331a-133">You can create and change budget cost elements only on the **Budget cost elements** page.</span></span>

## <a name="why-do-i-receive-an-error-message-when-i-change-the-dates-for-a-cost-element-on-a-forecast-position"></a><span data-ttu-id="a331a-134">Af hverju koma villuboð þegar ég breyti dagsetningum kostnaðareiningar á spástöðu?</span><span class="sxs-lookup"><span data-stu-id="a331a-134">Why do I receive an error message when I change the dates for a cost element on a forecast position?</span></span>
<span data-ttu-id="a331a-135">Dagsetningar á línu spástöðu kostnaðareiningarinnar verða að vera innan eftirfarandi afmarkana:</span><span class="sxs-lookup"><span data-stu-id="a331a-135">The dates on the forecast position cost element line must be within the following ranges:</span></span>

-   <span data-ttu-id="a331a-136">Virkjun og starfslok dagsetningarnar stöðunnar.</span><span class="sxs-lookup"><span data-stu-id="a331a-136">The activation and retirement dates of the position.</span></span>
-   <span data-ttu-id="a331a-137">Virkjun og gildistíma dagsetningar kostnaðareining fjárhagsáætlunar.</span><span class="sxs-lookup"><span data-stu-id="a331a-137">The activation and expiration dates of the budget cost element.</span></span>
-   <span data-ttu-id="a331a-138">Upphafs- og lokadagsetningu ferlis fjárhagsáætlunar sem er tengt fjárhagsáætlunargerð fyrir spástöðuna.</span><span class="sxs-lookup"><span data-stu-id="a331a-138">The start and end dates of the budget cycle that is associated with the budget planning process of the forecast position.</span></span>





