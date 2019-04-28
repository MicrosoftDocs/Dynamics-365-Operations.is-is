---
title: Færa inn umsækjanda og umsóknargögn handvirkt
description: Þessi verklýsing sýnir hvernig á að viðhalda handvirkt upplýsingum um umsækjendur og umsóknina.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmApplicant, LogisticsContactInfoGrid, HRMApplication,  DirPartyTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea61e3c1d76ade6e0d694b4b521e4be76fc8799d
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/19/2019
ms.locfileid: "855868"
---
# <a name="enter-applicant-and-application-data-manually"></a><span data-ttu-id="62334-103">Færa inn umsækjanda og umsóknargögn handvirkt</span><span class="sxs-lookup"><span data-stu-id="62334-103">Enter applicant and application data manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="62334-104">Þessi verklýsing sýnir hvernig á að viðhalda handvirkt upplýsingum um umsækjendur og umsóknina.</span><span class="sxs-lookup"><span data-stu-id="62334-104">This procedure shows how to manually maintain information about applicants and their application.</span></span>   <span data-ttu-id="62334-105">Hægt er að færa inn og viðhalda persónulegum upplýsingum, viðtal dagsetningar og tilvísanir, hæfni og beiðnir um aðlögun fyrir umsækjendur.</span><span class="sxs-lookup"><span data-stu-id="62334-105">You can enter and maintain personal information, interview dates and times, references, competencies, and accommodation requests for applicants.</span></span> <span data-ttu-id="62334-106">Einnig er hægt að uppfæra stöðu starfsumsókna umsækjanda og stofna bréf eða tölvupóst til að eiga samskipti við umsækjendur.</span><span class="sxs-lookup"><span data-stu-id="62334-106">You can also update the status of applicants’ applications for employment and create letters or email messages to communicate with applicants.</span></span> <span data-ttu-id="62334-107">Þegar færsla umsækjanda er stofnuð, tengiliðafærslu fyrir umsækjanda er stofnuð í altæku aðsetursbókinni.</span><span class="sxs-lookup"><span data-stu-id="62334-107">When you create an applicant record, a person record for that applicant is created in the global address book.</span></span>       <span data-ttu-id="62334-108">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="62334-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-new-applicant-record"></a><span data-ttu-id="62334-109">Stofna nýja færslu umsækjanda</span><span class="sxs-lookup"><span data-stu-id="62334-109">Create a new applicant record</span></span>
1. <span data-ttu-id="62334-110">Farið í Mannauður > Ráðningar > Umsækjendur > Umsækjendur.</span><span class="sxs-lookup"><span data-stu-id="62334-110">Go to Human resources > Recruitment > Applicants > Applicants.</span></span>
2. <span data-ttu-id="62334-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="62334-111">Click New.</span></span>
3. <span data-ttu-id="62334-112">Í reitinn Eiginnafn skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="62334-112">In the First name field, type a value.</span></span>
4. <span data-ttu-id="62334-113">Í reitinn eftirnafn skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="62334-113">In the Last name field, type a value.</span></span>
    * <span data-ttu-id="62334-114">Hægt er að færa inn viðbótar upplýsingar um umsækjanda ef hún er tiltæk.</span><span class="sxs-lookup"><span data-stu-id="62334-114">You can enter additional applicant information if it's available.</span></span> <span data-ttu-id="62334-115">Til dæmis upplýsingar geta verið hæsta gráða umsækjanda, gildandi starfsheiti eða fyrri vinnuveitanda.</span><span class="sxs-lookup"><span data-stu-id="62334-115">For example, information can include the applicant's highest degree, current job title, or previous employer.</span></span>  
5. <span data-ttu-id="62334-116">Víxla útvíkkun á liðnum tengslaupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="62334-116">Toggle the expansion of the Contact information section.</span></span>
6. <span data-ttu-id="62334-117">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="62334-117">Click Add.</span></span>
7. <span data-ttu-id="62334-118">Færðu inn 'Samskiptum tölvupósti' í svæðinu Lýsingu.</span><span class="sxs-lookup"><span data-stu-id="62334-118">In the Description field, type 'Communications email'.</span></span>
8. <span data-ttu-id="62334-119">Veljið valkost í svæðinu tegund.</span><span class="sxs-lookup"><span data-stu-id="62334-119">In the Type field, select an option.</span></span>
9. <span data-ttu-id="62334-120">Færa inn gildi í svæðið númer/aðsetur Tengiliðar.</span><span class="sxs-lookup"><span data-stu-id="62334-120">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="62334-121">Þetta tölvupóstfang verður notuð til að mynda tölvupósti samskiptum við umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="62334-121">This email address will be used to generate email communication with the applicant.</span></span>  
10. <span data-ttu-id="62334-122">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="62334-122">Click Add.</span></span>
11. <span data-ttu-id="62334-123">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="62334-123">In the Description field, type a value.</span></span>
12. <span data-ttu-id="62334-124">Færa inn gildi í svæðið númer/aðsetur Tengiliðar.</span><span class="sxs-lookup"><span data-stu-id="62334-124">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="62334-125">Persónulegar upplýsingar um umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="62334-125">Applicant personal information.</span></span>  
    * <span data-ttu-id="62334-126">Hægt er að færa inn viðbótar persónuupplýsingar umsækjandans, ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="62334-126">You can enter additional personal information for the applicant, if needed.</span></span> <span data-ttu-id="62334-127">Til dæmis, þetta getur falið í sér fæðingardagur þjóðernisuppruna, kyn eða hjúskaparstöðu.</span><span class="sxs-lookup"><span data-stu-id="62334-127">For example, this can include birth date, ethnic origin, gender, or marital status.</span></span>  
13. <span data-ttu-id="62334-128">Í aðgerðasvæðinu er smellt á hæfni.</span><span class="sxs-lookup"><span data-stu-id="62334-128">On the Action Pane, click Competencies.</span></span>
    * <span data-ttu-id="62334-129">Hægt er að færa inn hæfniforstillingu umsækjandans , þar á meðal þeirra hæfni, faglega reynslu, menntun, prófanir eða skírteini.</span><span class="sxs-lookup"><span data-stu-id="62334-129">You can enter the applicant's competency profile, including their skills, professional experiences, education, tests, or certificates.</span></span>  
    * <span data-ttu-id="62334-130">Hægt er að nota þessar upplýsingar til að halda utan um hæfni umsækjandans sem tengist vinnslur sem eru skilgreindar í gögnin fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="62334-130">This information can be used to map the applicant's skills to the skills associated with the jobs defined in your company's data.</span></span>   

## <a name="create-an-application-for-the-applicant"></a><span data-ttu-id="62334-131">Stofna umsókn fyrir umsækjanda</span><span class="sxs-lookup"><span data-stu-id="62334-131">Create an application for the applicant</span></span>
1. <span data-ttu-id="62334-132">Smellt er á Umsóknir.</span><span class="sxs-lookup"><span data-stu-id="62334-132">Click Applications.</span></span>
2. <span data-ttu-id="62334-133">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="62334-133">Click New.</span></span>
3. <span data-ttu-id="62334-134">Í reitnum ráðningarverk skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="62334-134">In the Recruitment project field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="62334-135">Með því að velja ráðningarverk, umsækjanda mun tengjast við tiltekna opnun sem er innifalin í því ráðningarverk.</span><span class="sxs-lookup"><span data-stu-id="62334-135">By selecting a recruitment project, the applicant will be associated with a specific opening included in that recruitment project.</span></span>  
4. <span data-ttu-id="62334-136">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="62334-136">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="62334-137">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="62334-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="62334-138">Að sjálfgefnu er vinnsla og deild byggð á völdu ráðningarverki.</span><span class="sxs-lookup"><span data-stu-id="62334-138">By default, the job and department are based on the selected recruitment project.</span></span>  
6. <span data-ttu-id="62334-139">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="62334-139">Click Save.</span></span>
    * <span data-ttu-id="62334-140">eftir vistun umsóknar, Hægt er að tengja skjöl við það, þar á meðal umsækjandans reynslu, umbun og kynningarbréfi.</span><span class="sxs-lookup"><span data-stu-id="62334-140">After saving the application, you can attach documents to it, including the applicant's experience, awards, and cover letter.</span></span>  

