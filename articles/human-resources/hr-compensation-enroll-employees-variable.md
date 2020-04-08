---
title: Skráið starfsmann inn í breytilega greiðsluáætlun
description: stjórnandi Launa og Fríðinda skrá starfsmenn í breytilegu launafyrirkomulagi til að reikna út reiðufés og ekki reiðufés umbun fyrir starfsmenn.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompVarEnrollEmpl
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2e591f471036c4b7f314155f1b56e87094ef1031
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009414"
---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a><span data-ttu-id="6838f-103">Skráið starfsmann inn í breytilega greiðsluáætlun</span><span class="sxs-lookup"><span data-stu-id="6838f-103">Enroll an employee in a variable compensation plan</span></span>

<span data-ttu-id="6838f-104">stjórnandi Launa og Fríðinda skrá starfsmenn í breytilegu launafyrirkomulagi til að reikna út reiðufés og ekki reiðufés umbun fyrir starfsmenn.</span><span class="sxs-lookup"><span data-stu-id="6838f-104">The Compensation and Benefits manager can enroll employees in variable compensation plans to calculate cash and non-cash awards for employees.</span></span> <span data-ttu-id="6838f-105">Þetta ferli gerir ráð fyrir að breytilega launafyrirkomulag hefur verið stofnuð með Virkja ráðningu svæðið stillt á Já og hæfnisreglur hafa verið stofnaðar fyrir breytilega launafyrirkomulag.</span><span class="sxs-lookup"><span data-stu-id="6838f-105">This procedure assumes that a variable compensation plan has been created with the Enable enrolment field set to Yes, and that eligibility rules have been created for that variable compensation plan.</span></span> <span data-ttu-id="6838f-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="6838f-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6838f-107">Til að hefja þetta ferli, farið í Mannauður > Starfsfólk > Starfsmenn > Laun > Skráning í breytilega áætlun</span><span class="sxs-lookup"><span data-stu-id="6838f-107">To begin this procedure, go to Human resources > Workers > Employees > Compensation > Variable plan enrolment</span></span>

1. <span data-ttu-id="6838f-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="6838f-108">Click New.</span></span>
2. <span data-ttu-id="6838f-109">Í reitnum Áætlun skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="6838f-109">In the Plan field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="6838f-110">Uppfletting áætlunar verður síuð til að sýna aðeins breytilegar áætlanir sem starfsmaðurinn á rétt á á grundvelli hæfnisreglur.</span><span class="sxs-lookup"><span data-stu-id="6838f-110">The plan lookup will be filtered to only show the variable compensation plans that the employee is eligible for based on the eligibility rules.</span></span>  
3. <span data-ttu-id="6838f-111">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="6838f-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="6838f-112">Víxla útvíkkun á liðnum Almennt.</span><span class="sxs-lookup"><span data-stu-id="6838f-112">Toggle the expansion of the General section.</span></span>
5. <span data-ttu-id="6838f-113">Í reitnum Gildisdagsetning skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="6838f-113">In the Effective date field, enter a date.</span></span>
6. <span data-ttu-id="6838f-114">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="6838f-114">Click Save.</span></span>
7. <span data-ttu-id="6838f-115">Víxla útvíkkun á liðnum Hnekkja.</span><span class="sxs-lookup"><span data-stu-id="6838f-115">Toggle the expansion of the Overrides section.</span></span>
    * <span data-ttu-id="6838f-116">Einnig er hægt að setja dagsetningu ráðningarreglu til að hnekkja ráðningardagsetningu fyrir starfsmann þegar ráðningarreglu er tilgreind fyrir valda breytilega áætlun er Prósent.</span><span class="sxs-lookup"><span data-stu-id="6838f-116">Optionally, a hire rule date can be set to override the hire date for an employee when the hire rule specified for the selected variable plan is Percent.</span></span>  
    * <span data-ttu-id="6838f-117">Ef breytileg áætlun er prósenta af grunniáætlun, er hægt að hnekkja umbunarprósentan fyrir starfsmanninn.</span><span class="sxs-lookup"><span data-stu-id="6838f-117">If the variable plan is a percent of basis plan, the award percentage can be overridden for the employee.</span></span> <span data-ttu-id="6838f-118">Ef breytilegrar launafyrirkomulag er fjöldi eininga áætlunar er hægt að hnekkja fjölda eininga fyrir starfsmanninn.</span><span class="sxs-lookup"><span data-stu-id="6838f-118">If the variable compensation plan is a number of units plan, the number of units can be overridden for the employee.</span></span>  
    * <span data-ttu-id="6838f-119">Ef starfsmaðurinn á að fá flöt upphæð fyrir sína umbun, upphæð er hægt að setja hér.</span><span class="sxs-lookup"><span data-stu-id="6838f-119">If the employee should be given a flat amount for their award, the amount can be set here.</span></span>  
8. <span data-ttu-id="6838f-120">Víxla útvíkkun á liðnum fyrirtækishnekking.</span><span class="sxs-lookup"><span data-stu-id="6838f-120">Toggle the expansion of the Organizational overrides section.</span></span>
    * <span data-ttu-id="6838f-121">Ef frammistöðu starfsmannsins á að hafa í huga, afköst mismunandi deildir eða deild sem er annað en það sem er úthlutað á stöðu starfsmannsins, hægt er að hnekkja deild.</span><span class="sxs-lookup"><span data-stu-id="6838f-121">If the employee's performance should take into consideration, the performance of different departments, or a department other than the one assigned on the employee's position, the department can be overridden.</span></span> <span data-ttu-id="6838f-122">dálkinn Prósenta ætti að vera samtals 100.</span><span class="sxs-lookup"><span data-stu-id="6838f-122">The Percent column should total 100.</span></span>  
