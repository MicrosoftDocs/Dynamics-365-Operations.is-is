---
title: Skrá starfsmann í launafyrirkomulag fastra launa
description: stjórnandi Launa og fríðindagetur tengja starfsmenn við launafyrirkomulög fastra launa til að stýra grunnlaunum þeirra.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a129bf9a6cb6a3ef92597e2ff9d126e3e5ce973b
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468252"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a><span data-ttu-id="51e42-103">Skrá starfsmann í launafyrirkomulag fastra launa</span><span class="sxs-lookup"><span data-stu-id="51e42-103">Enroll an employee in a fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="51e42-104">stjórnandi Launa og fríðindagetur tengja starfsmenn við launafyrirkomulög fastra launa til að stýra grunnlaunum þeirra.</span><span class="sxs-lookup"><span data-stu-id="51e42-104">The compensation and benefits manager can assign employees to fixed compensation plans to manage their base pay.</span></span> <span data-ttu-id="51e42-105">Þessi aðferð gerir ráð fyrir fast launafyrirkomulag hefur verið stofnuð og sé virkur og að hæfnisreglur hafi verið stilltar fyrir áætlunina.</span><span class="sxs-lookup"><span data-stu-id="51e42-105">This procedure assumes that a fixed plan has been created and is active, and that eligibility rules have been set for the plan.</span></span> <span data-ttu-id="51e42-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="51e42-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="51e42-107">Til að hefja þetta ferli, farið í Mannauður > Starfsfólk > Starfsmenn > Laun > Föst áætlun</span><span class="sxs-lookup"><span data-stu-id="51e42-107">To begin the procedure, go to Human resources > Workers > Employees > Compensation > Fixed plan</span></span>

1. <span data-ttu-id="51e42-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="51e42-108">Click New.</span></span>
2. <span data-ttu-id="51e42-109">Veljið aðgerð Fastra launa af gerðinni Ráða/Endurráða til að lýsa breyting á launum starfsmanns í svæðinu Aðgerð.</span><span class="sxs-lookup"><span data-stu-id="51e42-109">In the Action field, select a Fixed compensation action of type Hire/Rehire to describe the change in the employee's compensation.</span></span>
3. <span data-ttu-id="51e42-110">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="51e42-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="51e42-111">Í reitnum staða skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="51e42-111">In the Position field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="51e42-112">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="51e42-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="51e42-113">Stig sem birtist er úr Launastig vinnslu fyrir vinnslu á Stöðunni.</span><span class="sxs-lookup"><span data-stu-id="51e42-113">The level that's displayed is from the Compensation Level of the Job on the Position.</span></span> <span data-ttu-id="51e42-114">Verður að setja stig á Vinnslu áður en hægt er að úthluta laun til starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="51e42-114">The level must be set on the Job before compensation can be assigned to the employee.</span></span>  
6. <span data-ttu-id="51e42-115">Velja launafyrirkomulag fastra launa fyrir starfsmann í svæðinu Áætlun.</span><span class="sxs-lookup"><span data-stu-id="51e42-115">In the Plan field, select the fixed compensation plan for the employee.</span></span> <span data-ttu-id="51e42-116">Uppfletting Áætlunar er síuð til að sýna aðeins fyrirkomulaginu sem starfsmaðurinn á rétt á á grundvelli hæfnisreglur.</span><span class="sxs-lookup"><span data-stu-id="51e42-116">The Plan lookup is filtered to show only the plans that the employee is eligible for based on the Eligibility rules.</span></span>
7. <span data-ttu-id="51e42-117">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="51e42-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="51e42-118">Gildis- og lokadagsetningum fyrir laun fást sjálfgefið frá upphafs- og lokadagsetninga fyrir stöðuverkefni starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="51e42-118">The Effective and Expiration dates for the compensation default from the start and end dates for the worker's position assignment.</span></span> <span data-ttu-id="51e42-119">Hægt er að leiðrétta dagsetningum eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="51e42-119">You can adjust these dates as needed.</span></span>  
    * <span data-ttu-id="51e42-120">Ef Fast launafyrirkomulag er áætlun með skrefi skal velja skrefið sem innihalda réttar launataxta starfsmannsins.</span><span class="sxs-lookup"><span data-stu-id="51e42-120">If the Fixed compensation plan is a step plan, select the step containing the correct pay rate for the employee.</span></span> <span data-ttu-id="51e42-121">Ef fast launafyrirkomulag er með stigi eða brautaráætlun, er fært inn launataxti starfsmannsins.</span><span class="sxs-lookup"><span data-stu-id="51e42-121">If the fixed compensation plan is a grade or a band plan, enter the pay rate for the employee.</span></span> <span data-ttu-id="51e42-122">Launataxtinn sem verður að villuleita gagnvart vikmörk stillingar fyrir áætlunarinnar og lágmarks- og hámarks og tilvísunarpunkta fyrir launastig í vinnslu.</span><span class="sxs-lookup"><span data-stu-id="51e42-122">The pay rate will be validated against the tolerance settings for the plan, and the minimum and maximum reference points for the job's compensation level.</span></span>  
8. <span data-ttu-id="51e42-123">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="51e42-123">Click OK.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]