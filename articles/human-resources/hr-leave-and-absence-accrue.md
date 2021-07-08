---
title: Uppsöfnunaráætlanir fyrir leyfi og fjarvistir
description: Þú getur safnað orlofi og fjarveru í Dynamics 365 Human Resources fyrir marga starfsmenn eða einstakling.
author: andreabichsel
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ddd4c55f6ebfbe91fb949a92cb379f51d826c465
ms.sourcegitcommit: cee7887282d372c756c5c11f76684315f249bba5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/24/2021
ms.locfileid: "6303465"
---
# <a name="accrue-leave-and-absence-plans"></a><span data-ttu-id="b591e-103">Uppsöfnunaráætlanir fyrir leyfi og fjarvistir</span><span class="sxs-lookup"><span data-stu-id="b591e-103">Accrue leave and absence plans</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b591e-104">Þú getur safnað orlofi og fjarveru í Dynamics 365 Human Resources fyrir marga starfsmenn eða einstakling.</span><span class="sxs-lookup"><span data-stu-id="b591e-104">You can accrue leave and absence in Dynamics 365 Human Resources for multiple employees or for an individual.</span></span>

## <a name="accrue-leave-and-absence-for-multiple-employees"></a><span data-ttu-id="b591e-105">Uppsöfnun orlofs og fjarvista margra starfsmanna</span><span class="sxs-lookup"><span data-stu-id="b591e-105">Accrue leave and absence for multiple employees</span></span>

1. <span data-ttu-id="b591e-106">Á síðunni **Leyfi og fjarvera** velurðu flipann **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="b591e-106">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="b591e-107">Undir **Stjórna leyfi**, veldu **Safna orlofs- og fjarveruáætlunum**.</span><span class="sxs-lookup"><span data-stu-id="b591e-107">Under **Manage leave**, select **Accrue leave and absence plans**.</span></span>

3. <span data-ttu-id="b591e-108">Valmyndin **Uppsöfnunaráætlanir fyrir leyfi og fjarvistir** birtist.</span><span class="sxs-lookup"><span data-stu-id="b591e-108">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="b591e-109">Í **Safna upp frá og með** velurðu annaðhvort **Dagurinn í dag** eða **Sérsniðin dagsetning** og slærð inn sérsniðna dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="b591e-109">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="b591e-110">Ef ætlunin er að keyra uppsöfnun fyrir öll fyrirtæki skal velja **Öll fyrirtæki**.</span><span class="sxs-lookup"><span data-stu-id="b591e-110">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="b591e-111">Ef ætlunin er eftir að vinna úr uppsöfnun fyrir eina leyfisáætlun skal velja **Nei** fyrir **Allar áætlanir** og velja svo **Leyfisáætlun**.</span><span class="sxs-lookup"><span data-stu-id="b591e-111">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="b591e-112">Ef öll fyrirtæki eru valin er ekki hægt að velja staka leyfisáætlun.</span><span class="sxs-lookup"><span data-stu-id="b591e-112">If you select all companies, you can't select an individual leave plan.</span></span>

5. <span data-ttu-id="b591e-113">Ef þú vilt keyra uppsöfnunarferlið í bakgrunni skaltu velja **Keyra í bakgrunni** og framkvæma eftirfarandi verk:</span><span class="sxs-lookup"><span data-stu-id="b591e-113">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

    1. <span data-ttu-id="b591e-114">Færið inn upplýsingar fyrir uppsöfnunarferlið.</span><span class="sxs-lookup"><span data-stu-id="b591e-114">Enter information for the accrual process.</span></span>
    2. <span data-ttu-id="b591e-115">Til að setja upp endurtekið verk skal velja **Endurtekning**, slá inn upplýsingar um endurtekningu og velja síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b591e-115">To set up a recurring job, select **Recurrence**, enter the recurrence information, and then select **OK**.</span></span>
    3. <span data-ttu-id="b591e-116">Veldu til að setja upp atvinnuviðvörun **Viðvaranir**, veldu viðvaranir sem berast og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b591e-116">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>
    4. <span data-ttu-id="b591e-117">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b591e-117">Select **OK**.</span></span> <span data-ttu-id="b591e-118">Uppsöfnunarferlið keyrir með breytunum sem þú stillir.</span><span class="sxs-lookup"><span data-stu-id="b591e-118">The accrual process will run with the parameters you set.</span></span> 

## <a name="accrue-leave-and-absence-for-an-employee"></a><span data-ttu-id="b591e-119">Uppsöfnun orlofs og fjarvista fyrir starfsmann</span><span class="sxs-lookup"><span data-stu-id="b591e-119">Accrue leave and absence for an employee</span></span>

1. <span data-ttu-id="b591e-120">Veldu á skrá starfsmannsins **Leyfi**.</span><span class="sxs-lookup"><span data-stu-id="b591e-120">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="b591e-121">Veldu **Uppsöfnunaráætlanir fyrir leyfi og fjarvistir**.</span><span class="sxs-lookup"><span data-stu-id="b591e-121">Select **Accrue leave and absence**.</span></span>

3. <span data-ttu-id="b591e-122">Valmyndin **Uppsöfnunaráætlanir fyrir leyfi og fjarvistir** birtist.</span><span class="sxs-lookup"><span data-stu-id="b591e-122">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="b591e-123">Í **Safna upp frá og með** velurðu annaðhvort **Dagurinn í dag** eða **Sérsniðin dagsetning** og slærð inn sérsniðna dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="b591e-123">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="b591e-124">Ef ætlunin er að keyra uppsöfnun fyrir öll fyrirtæki skal velja **Öll fyrirtæki**.</span><span class="sxs-lookup"><span data-stu-id="b591e-124">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="b591e-125">Ef ætlunin er eftir að vinna úr uppsöfnun fyrir eina leyfisáætlun skal velja **Nei** fyrir **Allar áætlanir** og velja svo **Leyfisáætlun**.</span><span class="sxs-lookup"><span data-stu-id="b591e-125">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="b591e-126">Ef öll fyrirtæki eru valin er ekki hægt að velja staka leyfisáætlun.</span><span class="sxs-lookup"><span data-stu-id="b591e-126">If you select all companies, you can't select an individual leave plan.</span></span>

5. <span data-ttu-id="b591e-127">Ef þú vilt keyra uppsöfnunarferlið í bakgrunni skaltu velja **Keyra í bakgrunni** og framkvæma eftirfarandi verk:</span><span class="sxs-lookup"><span data-stu-id="b591e-127">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="b591e-128">Færið inn upplýsingar fyrir uppsöfnunarferlið.</span><span class="sxs-lookup"><span data-stu-id="b591e-128">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="b591e-129">Veldu til að setja upp endurtekið starf **Endurtekning**, sláðu inn upplýsingar um endurtekningu og veldu **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b591e-129">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="b591e-130">Veldu til að setja upp atvinnuviðvörun **Viðvaranir**, veldu viðvaranir sem berast og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b591e-130">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="b591e-131">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b591e-131">Select **OK**.</span></span> <span data-ttu-id="b591e-132">Uppsöfnunarferlið keyrir með breytunum sem þú stillir.</span><span class="sxs-lookup"><span data-stu-id="b591e-132">The accrual process will run with the parameters you set.</span></span>

## <a name="delete-leave-and-absence-accruals-for-multiple-employees"></a><span data-ttu-id="b591e-133">Eyða uppsöfnunum orlofs og fjarvista margra starfsmanna</span><span class="sxs-lookup"><span data-stu-id="b591e-133">Delete leave and absence accruals for multiple employees</span></span>

<span data-ttu-id="b591e-134">Eyða rekstrarreikningum fyrir ákveðna áætlun og tímabil.</span><span class="sxs-lookup"><span data-stu-id="b591e-134">Delete accrual records for a specific plan and date range.</span></span> <span data-ttu-id="b591e-135">Uppsöfnunardagsetningar verða að vera dagsettar í dag eða í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="b591e-135">Accrual dates must be dated today or in the future.</span></span>

1. <span data-ttu-id="b591e-136">Á síðunni **Leyfi og fjarvera** velurðu flipann **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="b591e-136">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="b591e-137">Undir **Stjórna leyfi**, veldu **Eyða uppsöfnunum á leyfis- og fjarvistaáætlunum**.</span><span class="sxs-lookup"><span data-stu-id="b591e-137">Under **Manage leave**, select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="b591e-138">Í valmyndinni **Eyða uppsöfnunum á leyfis- og fjarvistaáætlunum** veldurðu **Leyfisáætlun**.</span><span class="sxs-lookup"><span data-stu-id="b591e-138">In the **Delete leave and absence plan accruals** dialog box, select the **Leave plan**.</span></span>

4. <span data-ttu-id="b591e-139">Ef við á skaltu velja **Eyða leiðréttingum á stöðum**.</span><span class="sxs-lookup"><span data-stu-id="b591e-139">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="b591e-140">Sláðu inn eða veldu **Dagsetningu leyfisuppsöfnunar**.</span><span class="sxs-lookup"><span data-stu-id="b591e-140">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="b591e-141">Þessi dagsetning verður að vera annaðhvort í dag eða í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="b591e-141">This date has to be either today or in the future.</span></span>

6. <span data-ttu-id="b591e-142">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b591e-142">Select **OK**.</span></span> <span data-ttu-id="b591e-143">Uppsöfnunarferlið mun eyða uppsetningar með breytunum sem þú stillir.</span><span class="sxs-lookup"><span data-stu-id="b591e-143">The accrual process will delete accruals with the parameters you set.</span></span>

## <a name="delete-leave-and-absence-accruals-for-a-single-employee"></a><span data-ttu-id="b591e-144">Eyða uppsöfnunum orlofs og fjarvista eins starfsmanns</span><span class="sxs-lookup"><span data-stu-id="b591e-144">Delete leave and absence accruals for a single employee</span></span>

1. <span data-ttu-id="b591e-145">Veldu á skrá starfsmannsins **Leyfi**.</span><span class="sxs-lookup"><span data-stu-id="b591e-145">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="b591e-146">Veldu **Eyða uppsöfnunum fyrir leyfis- og fjarvistaáætlanir**.</span><span class="sxs-lookup"><span data-stu-id="b591e-146">Select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="b591e-147">Í valmyndinni **Eyða uppsöfnunum á leyfis- og fjarvistaáætlunum** veldurðu **Leyfisáætlun**.</span><span class="sxs-lookup"><span data-stu-id="b591e-147">In the **Delete leave and absence plan accruals** dialog box, select **Leave plan**.</span></span>

4. <span data-ttu-id="b591e-148">Ef við á skaltu velja **Eyða leiðréttingum á stöðum**.</span><span class="sxs-lookup"><span data-stu-id="b591e-148">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="b591e-149">Sláðu inn eða veldu **Dagsetningu leyfisuppsöfnunar**.</span><span class="sxs-lookup"><span data-stu-id="b591e-149">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="b591e-150">Þessi dagsetning verður að vera annaðhvort í dag eða í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="b591e-150">This date must be either today or in the future.</span></span>

6. <span data-ttu-id="b591e-151">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b591e-151">Select **OK**.</span></span> <span data-ttu-id="b591e-152">Uppsöfnunarferlið mun eyða uppsetningar með breytunum sem þú stillir.</span><span class="sxs-lookup"><span data-stu-id="b591e-152">The accrual process will delete accruals with the parameters you set.</span></span>

## <a name="review-leave-accrual-and-deletion-processes"></a><span data-ttu-id="b591e-153">Farið yfir uppsöfnunar- og eyðingarferli leyfis</span><span class="sxs-lookup"><span data-stu-id="b591e-153">Review leave accrual and deletion processes</span></span>

<span data-ttu-id="b591e-154">**Úttekt leyfisuppsöfnunar** birtist í hvert skipti sem þú keyrir eða eyðir uppsöfnun fyrir einn eða alla starfsmenn.</span><span class="sxs-lookup"><span data-stu-id="b591e-154">**Leave accrual audit** displays each time you run or delete an accrual for one or all employees.</span></span> <span data-ttu-id="b591e-155">Dagsetning og einstaklingur sem framkvæmdi aðgerðina eru einnig sýnd.</span><span class="sxs-lookup"><span data-stu-id="b591e-155">The date and person who performed the action also displays.</span></span>

1. <span data-ttu-id="b591e-156">Á síðunni **Leyfi og fjarvera** velurðu flipann **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="b591e-156">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="b591e-157">Undir **Stjórna leyfi**, veldu **Eyða úttekt leyfisuppsöfnunar**.</span><span class="sxs-lookup"><span data-stu-id="b591e-157">Under **Manage leave**, select **Delete leave accrual audit**.</span></span>

## <a name="leave-accrual-transaction-auditing"></a><span data-ttu-id="b591e-158">Endurskoðun færslu fyrir uppsafnað leyfi</span><span class="sxs-lookup"><span data-stu-id="b591e-158">Leave accrual transaction auditing</span></span>

<span data-ttu-id="b591e-159">Þessi eiginleiki hjálpar stjórnendum leyfis og fjarvista að skilja betur uppsafnaðar færslur leyfa og fjarvista sem tengjast frítímastöðu starfsmanns fyrir tiltekna leyfisgerð.</span><span class="sxs-lookup"><span data-stu-id="b591e-159">This feature helps leave and absence managers understand the leave and absence accrual transactions related to an employee’s time off balances for a specific leave type.</span></span>

<span data-ttu-id="b591e-160">Til að skoða færsluupplýsingar:</span><span class="sxs-lookup"><span data-stu-id="b591e-160">To view transaction details:</span></span>

1. <span data-ttu-id="b591e-161">Veldu á skrá starfsmannsins **Leyfi**.</span><span class="sxs-lookup"><span data-stu-id="b591e-161">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="b591e-162">Veldu **Skoða frí** og veldu svo flipann **Stöður**.</span><span class="sxs-lookup"><span data-stu-id="b591e-162">Select **View time off**, and then select the **Balances** tab.</span></span>

<span data-ttu-id="b591e-163">Til að skoða uppsafnaðar færslur sem tengjast tiltekinni leyfisgerð skal velja númeragildið í dálknum **Núverandi staða**.</span><span class="sxs-lookup"><span data-stu-id="b591e-163">To view the accrual transactions related to a specific leave type, select the numerical value in the **Current balance** column.</span></span>

<span data-ttu-id="b591e-164">Til að skoða færsluupplýsingar fyrir tiltekna uppsafnaða upphæð skal velja uppsöfnunarlínu, opna svæðið **Tengdar upplýsingar** hægra megin og síðan opna hlutann **Upplýsingar um færslu**.</span><span class="sxs-lookup"><span data-stu-id="b591e-164">To view the transaction details for a specific accrual amount, select an accrual row, open the **Related information** panel on the right, and then open the **Transaction details** section.</span></span> <span data-ttu-id="b591e-165">Hlutinn Færsluupplýsingar sýnir:</span><span class="sxs-lookup"><span data-stu-id="b591e-165">The Transaction details section displays:</span></span>

- <span data-ttu-id="b591e-166">Breytingar á eftirstöðvum leyfisgerðum starfsmannsins</span><span class="sxs-lookup"><span data-stu-id="b591e-166">Changes to the employee’s leave type balance</span></span>
- <span data-ttu-id="b591e-167">Upplýsingar um starf fyrir það tiltekna uppsöfnunartímabil</span><span class="sxs-lookup"><span data-stu-id="b591e-167">Employment details for that specified accrual period</span></span>
- <span data-ttu-id="b591e-168">Upplýsingar um uppsöfnunartímabil og taxta</span><span class="sxs-lookup"><span data-stu-id="b591e-168">Details about the accrual period and rates</span></span>
- <span data-ttu-id="b591e-169">Allar breytingar gerðar á stillingum leyfisáætlunar</span><span class="sxs-lookup"><span data-stu-id="b591e-169">Any changes made to leave plan configurations</span></span>

![Birta endurskoðun færslu fyrir uppsafnað leyfi](media/hr-leave-and-absence-accrue-audit.png)

## <a name="see-also"></a><span data-ttu-id="b591e-171">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="b591e-171">See also</span></span>

[<span data-ttu-id="b591e-172">Yfirlit yfir leyfi og fjarvistir</span><span class="sxs-lookup"><span data-stu-id="b591e-172">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="b591e-173">Búa til leyfis- og fjarvistaáætlun</span><span class="sxs-lookup"><span data-stu-id="b591e-173">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
