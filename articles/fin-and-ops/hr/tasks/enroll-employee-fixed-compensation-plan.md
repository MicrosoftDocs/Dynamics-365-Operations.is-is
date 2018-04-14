--- 
title: "Skrá starfsmann í launafyrirkomulag fastra launa"
description: "stjórnandi Launa og fríðindagetur tengja starfsmenn við launafyrirkomulög fastra launa til að stýra grunnlaunum þeirra."
author: kherr75
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: b8701c42f2477055eae9dba69da30cce1a122f71
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a><span data-ttu-id="1cd4d-103">Skrá starfsmann í launafyrirkomulag fastra launa</span><span class="sxs-lookup"><span data-stu-id="1cd4d-103">Enroll an employee in a fixed compensation plan</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1cd4d-104">stjórnandi Launa og fríðindagetur tengja starfsmenn við launafyrirkomulög fastra launa til að stýra grunnlaunum þeirra.</span><span class="sxs-lookup"><span data-stu-id="1cd4d-104">The compensation and benefits manager can assign employees to fixed compensation plans to manage their base pay.</span></span> <span data-ttu-id="1cd4d-105">Þessi aðferð gerir ráð fyrir fast launafyrirkomulag hefur verið stofnuð og sé virkur og að hæfnisreglur hafi verið stilltar fyrir áætlunina.</span><span class="sxs-lookup"><span data-stu-id="1cd4d-105">This procedure assumes that a fixed plan has been created and is active, and that eligibility rules have been set for the plan.</span></span> <span data-ttu-id="1cd4d-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="1cd4d-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="1cd4d-107">Til að hefja þetta ferli, farið í Mannauður > Starfsfólk > Starfsmenn > Laun > Föst áætlun</span><span class="sxs-lookup"><span data-stu-id="1cd4d-107">To begin the procedure, go to Human resources > Workers > Employees > Compensation > Fixed plan</span></span>

1. <span data-ttu-id="1cd4d-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="1cd4d-108">Click New.</span></span>
2. <span data-ttu-id="1cd4d-109">Veljið aðgerð Fastra launa af gerðinni Ráða/Endurráða til að lýsa breyting á launum starfsmanns í svæðinu Aðgerð.</span><span class="sxs-lookup"><span data-stu-id="1cd4d-109">In the Action field, select a Fixed compensation action of type Hire/Rehire to describe the change in the employee's compensation.</span></span>
3. <span data-ttu-id="1cd4d-110">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="1cd4d-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="1cd4d-111">Í reitnum staða skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="1cd4d-111">In the Position field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="1cd4d-112">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="1cd4d-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1cd4d-113">Stig sem birtist er úr Launastig vinnslu fyrir vinnslu á Stöðunni.</span><span class="sxs-lookup"><span data-stu-id="1cd4d-113">The level that's displayed is from the Compensation Level of the Job on the Position.</span></span> <span data-ttu-id="1cd4d-114">Verður að setja stig á Vinnslu áður en hægt er að úthluta laun til starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="1cd4d-114">The level must be set on the Job before compensation can be assigned to the employee.</span></span>  
6. <span data-ttu-id="1cd4d-115">Velja launafyrirkomulag fastra launa fyrir starfsmann í svæðinu Áætlun.</span><span class="sxs-lookup"><span data-stu-id="1cd4d-115">In the Plan field, select the fixed compensation plan for the employee.</span></span> <span data-ttu-id="1cd4d-116">Uppfletting Áætlunar er síuð til að sýna aðeins fyrirkomulaginu sem starfsmaðurinn á rétt á á grundvelli hæfnisreglur.</span><span class="sxs-lookup"><span data-stu-id="1cd4d-116">The Plan lookup is filtered to show only the plans that the employee is eligible for based on the Eligibility rules.</span></span>
7. <span data-ttu-id="1cd4d-117">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="1cd4d-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1cd4d-118">Gildis- og lokadagsetningum fyrir laun fást sjálfgefið frá upphafs- og lokadagsetninga fyrir stöðuverkefni starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="1cd4d-118">The Effective and Expiration dates for the compensation default from the start and end dates for the worker's position assignment.</span></span> <span data-ttu-id="1cd4d-119">Hægt er að leiðrétta dagsetningum eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="1cd4d-119">You can adjust these dates as needed.</span></span>  
    * <span data-ttu-id="1cd4d-120">Ef Fast launafyrirkomulag er áætlun með skrefi skal velja skrefið sem innihalda réttar launataxta starfsmannsins.</span><span class="sxs-lookup"><span data-stu-id="1cd4d-120">If the Fixed compensation plan is a step plan, select the step containing the correct pay rate for the employee.</span></span> <span data-ttu-id="1cd4d-121">Ef fast launafyrirkomulag er með stigi eða brautaráætlun, er fært inn launataxti starfsmannsins.</span><span class="sxs-lookup"><span data-stu-id="1cd4d-121">If the fixed compensation plan is a grade or a band plan, enter the pay rate for the employee.</span></span> <span data-ttu-id="1cd4d-122">Launataxtinn sem verður að villuleita gagnvart vikmörk stillingar fyrir áætlunarinnar og lágmarks- og hámarks og tilvísunarpunkta fyrir launastig í vinnslu.</span><span class="sxs-lookup"><span data-stu-id="1cd4d-122">The pay rate will be validated against the tolerance settings for the plan, and the minimum and maximum reference points for the job's compensation level.</span></span>  
8. <span data-ttu-id="1cd4d-123">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="1cd4d-123">Click OK.</span></span>


