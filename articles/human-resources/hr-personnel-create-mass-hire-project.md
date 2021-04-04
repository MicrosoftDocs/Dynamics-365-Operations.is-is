---
title: Stofna fjöldaráðningarverk
description: Þetta ferli fer í gegnum ferlið fyrir uppsetningu fjöldaráðningarverk.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMMassHireProject,  HRMMassHireLineCreate, HcmJobLookup, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6d553c5762dcb456bd7178858c09129bc154349
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467050"
---
# <a name="create-a-mass-hire-project"></a><span data-ttu-id="88050-103">Stofna fjöldaráðningarverk</span><span class="sxs-lookup"><span data-stu-id="88050-103">Create a mass hire project</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="88050-104">Þetta ferli fer í gegnum ferlið fyrir uppsetningu fjöldaráðningarverk.</span><span class="sxs-lookup"><span data-stu-id="88050-104">This procedure walks through the process of setting up a mass hire project.</span></span> <span data-ttu-id="88050-105">Ráðningaraðila er getur notað fjöldaráðningarverk til að stofna margar stöður auðveldlega og ráða fjöldi starfsmanna í þær stöður.</span><span class="sxs-lookup"><span data-stu-id="88050-105">A recruiter can use mass hire projects to easily create multiple positions and hire a number of workers into those positions.</span></span> <span data-ttu-id="88050-106">Til að hefja þetta ferli, farið í Mannauður > Ráðning > Fjöldaráðningarverk.</span><span class="sxs-lookup"><span data-stu-id="88050-106">To begin this procedure, go to Human resources > Recruitment > Mass hire projects.</span></span> <span data-ttu-id="88050-107">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="88050-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="88050-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="88050-108">Click New.</span></span>
2. <span data-ttu-id="88050-109">í svæðinu fjöldaráðningarverk, færið inn gildi.</span><span class="sxs-lookup"><span data-stu-id="88050-109">In the Mass hire project field, type a value.</span></span>
3. <span data-ttu-id="88050-110">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="88050-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="88050-111">Í reitinn upphaf verk skal færa inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="88050-111">In the Project start field, enter a date.</span></span>
5. <span data-ttu-id="88050-112">Í reitinn endir verk skal færa inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="88050-112">In the Project end field, enter a date.</span></span>
6. <span data-ttu-id="88050-113">Smella á Opna verk.</span><span class="sxs-lookup"><span data-stu-id="88050-113">Click Open project.</span></span>
7. <span data-ttu-id="88050-114">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="88050-114">Click Yes.</span></span>
8. <span data-ttu-id="88050-115">Smellt er á Stofna staða.</span><span class="sxs-lookup"><span data-stu-id="88050-115">Click Create positions.</span></span>
9. <span data-ttu-id="88050-116">Í reitinn Magn er fært inn hve fjöldi staða sem á að stofna</span><span class="sxs-lookup"><span data-stu-id="88050-116">In the Quantity field, enter the number of positions that you want to create</span></span>
    * <span data-ttu-id="88050-117">Upphafsdagsetning verða ráðningardagsetning fyrir nýja starfsmenn.</span><span class="sxs-lookup"><span data-stu-id="88050-117">The Start date will become the Hire date for the new workers.</span></span>  
    * <span data-ttu-id="88050-118">Lokadagur verður starfslokadagur fyrir nýja starfsmenn.</span><span class="sxs-lookup"><span data-stu-id="88050-118">The End date will be the Termination date for the new workers.</span></span>  
    * <span data-ttu-id="88050-119">Tilgreina hvort nýja starfsmenn verða Starfsmenn eða Verktaka.</span><span class="sxs-lookup"><span data-stu-id="88050-119">Specify whether the new workers will be Employees or Contractors.</span></span>  
10. <span data-ttu-id="88050-120">Í svæðinu Starf, Smellið á hnappinn fellilistanum til að velja starf til að stofna stöður fyrir.</span><span class="sxs-lookup"><span data-stu-id="88050-120">In the Job field, click the drop-down button to select the job to create the positions for.</span></span>
11. <span data-ttu-id="88050-121">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="88050-121">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="88050-122">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="88050-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="88050-123">Sjálfgefið gildi fulls starfs koma úr völdu vinnsluna.</span><span class="sxs-lookup"><span data-stu-id="88050-123">The default full-time equivalent value will come from the selected job.</span></span> <span data-ttu-id="88050-124">Þessu gildi má breyta ef þarf.</span><span class="sxs-lookup"><span data-stu-id="88050-124">You can change this if needed.</span></span>  
    * <span data-ttu-id="88050-125">Einnig er hægt að velja Deild fyrir nýjar stöður.</span><span class="sxs-lookup"><span data-stu-id="88050-125">Optionally, select the Department for the new positions.</span></span>  
13. <span data-ttu-id="88050-126">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="88050-126">Click OK.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]