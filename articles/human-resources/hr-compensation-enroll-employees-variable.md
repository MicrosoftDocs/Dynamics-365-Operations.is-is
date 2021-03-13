---
title: Skráið starfsmann inn í breytilega greiðsluáætlun
description: stjórnandi Launa og Fríðinda skrá starfsmenn í breytilegu launafyrirkomulagi til að reikna út reiðufés og ekki reiðufés umbun fyrir starfsmenn.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompVarEnrollEmpl, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7a173403e79212be5e4aac36d99f349da159e08
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112974"
---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a><span data-ttu-id="52b59-103">Skráið starfsmann inn í breytilega greiðsluáætlun</span><span class="sxs-lookup"><span data-stu-id="52b59-103">Enroll an employee in a variable compensation plan</span></span>

<span data-ttu-id="52b59-104">stjórnandi Launa og Fríðinda skrá starfsmenn í breytilegu launafyrirkomulagi til að reikna út reiðufés og ekki reiðufés umbun fyrir starfsmenn.</span><span class="sxs-lookup"><span data-stu-id="52b59-104">The Compensation and Benefits manager can enroll employees in variable compensation plans to calculate cash and non-cash awards for employees.</span></span> <span data-ttu-id="52b59-105">Þetta ferli gerir ráð fyrir að breytilega launafyrirkomulag hefur verið stofnuð með Virkja ráðningu svæðið stillt á Já og hæfnisreglur hafa verið stofnaðar fyrir breytilega launafyrirkomulag.</span><span class="sxs-lookup"><span data-stu-id="52b59-105">This procedure assumes that a variable compensation plan has been created with the Enable enrolment field set to Yes, and that eligibility rules have been created for that variable compensation plan.</span></span> <span data-ttu-id="52b59-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="52b59-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="52b59-107">Til að hefja þetta ferli, farið í Mannauður > Starfsfólk > Starfsmenn > Laun > Skráning í breytilega áætlun</span><span class="sxs-lookup"><span data-stu-id="52b59-107">To begin this procedure, go to Human resources > Workers > Employees > Compensation > Variable plan enrolment</span></span>

1. <span data-ttu-id="52b59-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="52b59-108">Click New.</span></span>
2. <span data-ttu-id="52b59-109">Í reitnum Áætlun skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="52b59-109">In the Plan field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="52b59-110">Uppfletting áætlunar verður síuð til að sýna aðeins breytilegar áætlanir sem starfsmaðurinn á rétt á á grundvelli hæfnisreglur.</span><span class="sxs-lookup"><span data-stu-id="52b59-110">The plan lookup will be filtered to only show the variable compensation plans that the employee is eligible for based on the eligibility rules.</span></span>  
3. <span data-ttu-id="52b59-111">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="52b59-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="52b59-112">Víxla útvíkkun á liðnum Almennt.</span><span class="sxs-lookup"><span data-stu-id="52b59-112">Toggle the expansion of the General section.</span></span>
5. <span data-ttu-id="52b59-113">Í reitnum Gildisdagsetning skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="52b59-113">In the Effective date field, enter a date.</span></span>
6. <span data-ttu-id="52b59-114">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="52b59-114">Click Save.</span></span>
7. <span data-ttu-id="52b59-115">Víxla útvíkkun á liðnum Hnekkja.</span><span class="sxs-lookup"><span data-stu-id="52b59-115">Toggle the expansion of the Overrides section.</span></span>
    * <span data-ttu-id="52b59-116">Einnig er hægt að setja dagsetningu ráðningarreglu til að hnekkja ráðningardagsetningu fyrir starfsmann þegar ráðningarreglu er tilgreind fyrir valda breytilega áætlun er Prósent.</span><span class="sxs-lookup"><span data-stu-id="52b59-116">Optionally, a hire rule date can be set to override the hire date for an employee when the hire rule specified for the selected variable plan is Percent.</span></span>  
    * <span data-ttu-id="52b59-117">Ef breytileg áætlun er prósenta af grunniáætlun, er hægt að hnekkja umbunarprósentan fyrir starfsmanninn.</span><span class="sxs-lookup"><span data-stu-id="52b59-117">If the variable plan is a percent of basis plan, the award percentage can be overridden for the employee.</span></span> <span data-ttu-id="52b59-118">Ef breytilegrar launafyrirkomulag er fjöldi eininga áætlunar er hægt að hnekkja fjölda eininga fyrir starfsmanninn.</span><span class="sxs-lookup"><span data-stu-id="52b59-118">If the variable compensation plan is a number of units plan, the number of units can be overridden for the employee.</span></span>  
    * <span data-ttu-id="52b59-119">Ef starfsmaðurinn á að fá flöt upphæð fyrir sína umbun, upphæð er hægt að setja hér.</span><span class="sxs-lookup"><span data-stu-id="52b59-119">If the employee should be given a flat amount for their award, the amount can be set here.</span></span>  
8. <span data-ttu-id="52b59-120">Víxla útvíkkun á liðnum fyrirtækishnekking.</span><span class="sxs-lookup"><span data-stu-id="52b59-120">Toggle the expansion of the Organizational overrides section.</span></span>
    * <span data-ttu-id="52b59-121">Ef frammistöðu starfsmannsins á að hafa í huga, afköst mismunandi deildir eða deild sem er annað en það sem er úthlutað á stöðu starfsmannsins, hægt er að hnekkja deild.</span><span class="sxs-lookup"><span data-stu-id="52b59-121">If the employee's performance should take into consideration, the performance of different departments, or a department other than the one assigned on the employee's position, the department can be overridden.</span></span> <span data-ttu-id="52b59-122">dálkinn Prósenta ætti að vera samtals 100.</span><span class="sxs-lookup"><span data-stu-id="52b59-122">The Percent column should total 100.</span></span>  

