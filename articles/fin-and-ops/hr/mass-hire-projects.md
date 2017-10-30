---
title: "Fjöldaráðningarverk"
description: "Fjöldaráðningarverk leyfa mannauðssérfræðingum að búa til margar stöður og ráða starfsmenn á skilvirkan hátt í þær stöður."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HRMMassHireProject
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 7481
ms.assetid: 5f5eb271-76eb-4305-bd1c-5d171dafccc9
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e57db8f4b692aa9c27916625897e268f63031782
ms.openlocfilehash: ab074b3ad72ab96ffb9c95005f22dc023fc923e4
ms.contentlocale: is-is
ms.lasthandoff: 10/30/2017

---

# <a name="mass-hire-projects"></a><span data-ttu-id="678f9-103">Fjöldaráðningarverk</span><span class="sxs-lookup"><span data-stu-id="678f9-103">Mass hire projects</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="678f9-104">Fjöldaráðningarverk leyfa mannauðssérfræðingum að búa til margar stöður og ráða starfsmenn á skilvirkan hátt í þær stöður.</span><span class="sxs-lookup"><span data-stu-id="678f9-104">Mass hire projects allow human resources specialists to create multiple positions and efficiently hire workers into those positions.</span></span>

<a name="overview"></a><span data-ttu-id="678f9-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="678f9-105">Overview</span></span>
--------

<span data-ttu-id="678f9-106">Þegar margir starfsmenn eru ráðnir á sama tíma, eins og þegar fólk er ráðið til að mæta vertíðarálagi, er gagnlegt að stofna fjöldaráðningaverk.</span><span class="sxs-lookup"><span data-stu-id="678f9-106">Use mass hire projects when you hire multiple workers at one time, such as when you hire to meet a seasonal demand.</span></span> <span data-ttu-id="678f9-107">Að stofna fjöldaráðningarverk er gagnlegt þar sem hægt er að stofna stöðufærslur, starfsmannaskrár, og starfsmannaúthlutun fyrir stöður á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="678f9-107">Creating a mass hire project is useful because you can create position records, worker records, and worker assignments for positions at the same time.</span></span> <span data-ttu-id="678f9-108">Þegar stöður eru stofnaðar fyrir fjöldaráðningarverk er hægt að tilgreina eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="678f9-108">When you create positions for a mass hire project, you can specify the following information:</span></span>
-   <span data-ttu-id="678f9-109">Fjöldi staða sem á að stofna</span><span class="sxs-lookup"><span data-stu-id="678f9-109">The number of positions to create</span></span>
-   <span data-ttu-id="678f9-110">Gerð starfsmanns fyrir fólk sem verður ráðið í stöður</span><span class="sxs-lookup"><span data-stu-id="678f9-110">The worker type of the people that you will hire for the positions</span></span>
-   <span data-ttu-id="678f9-111">Starf og deild sem stöðurnar tengjast.</span><span class="sxs-lookup"><span data-stu-id="678f9-111">The department and the job that are associated with the positions</span></span>
-   <span data-ttu-id="678f9-112">Gildi fulls starfs fyrir stöðuna</span><span class="sxs-lookup"><span data-stu-id="678f9-112">The full-time equivalent value of the position</span></span>

## <a name="example"></a><span data-ttu-id="678f9-113">Dæmi</span><span class="sxs-lookup"><span data-stu-id="678f9-113">Example</span></span>
<span data-ttu-id="678f9-114">Á sumrin, er yfirleitt ráðnir 15 20 skólakrakkar í hlutastarf til að fylla tiltækar starfsnámsstöður í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="678f9-114">In the summer, you usually hire 15-20 part-time college students to fill available internships in your company.</span></span> <span data-ttu-id="678f9-115">Nú í ár, á að ráða fimm bókhaldara, fimm starfsmenn í pantanavinnslu og fimm gjaldkera.</span><span class="sxs-lookup"><span data-stu-id="678f9-115">This year, you want to hire five accountants, five order processors, and five cashiers.</span></span> <span data-ttu-id="678f9-116">Í stað þess að stofna hverja stöðufærslu og starfsmannafærslu sér, er stofnað eitt fjöldaráðningarverk sem kallast "SummerInterns".</span><span class="sxs-lookup"><span data-stu-id="678f9-116">Instead of creating each position record and worker record separately, you create one mass hire project called “SummerInterns”.</span></span> <span data-ttu-id="678f9-117">Upphafs- og lokadagsetningar verksins er í samræmi við upphags og lokadagsetningar tímalengdar fyrir stöðurnar sem þú stofnar fyrir fjöldaráðningarverkið.</span><span class="sxs-lookup"><span data-stu-id="678f9-117">The project start and end dates correlate with the start and end dates of the position durations for the positions you create for the mass hire project.</span></span> 

<span data-ttu-id="678f9-118">Í síðunni **fjöldaráðningarverk** , velja verkið "SummerInterns" og smellið síðan á **Opin verk**.</span><span class="sxs-lookup"><span data-stu-id="678f9-118">In the **Mass hire projects** page, select the “SummerInterns” project and then click **Open project**.</span></span> <span data-ttu-id="678f9-119">Í Opna fjöldaráðningarverk, er smellt **Stofna stöður** og færa inn upplýsingar um stöðu bókarans.</span><span class="sxs-lookup"><span data-stu-id="678f9-119">In the open mass hire project, click **Create positions** and enter information about the accountant position.</span></span> <span data-ttu-id="678f9-120">Hægt er að tilgreina að fimm bókarastöður ættu að vera stofnuð með því að nota sömu upplýsingar fyrir hverja og eina, og smellið svo á í lagi.</span><span class="sxs-lookup"><span data-stu-id="678f9-120">You can indicate that five accountant positions should be created using the same information for each one, and then click OK.</span></span> <span data-ttu-id="678f9-121">Endurtakið þetta ferli fyrir afgreiðslumaður pantana og gjaldkerastöður.</span><span class="sxs-lookup"><span data-stu-id="678f9-121">Repeat this process for the order processor and cashier positions.</span></span> 

<span data-ttu-id="678f9-122">Eftir val námsmanns til að ráða fyrir starfsnámsstöður, verður að færa inn upplýsingar hvers námsmanns á **Stöðuupplýsingar** fyrir stöðu sem verið er að ráða þá í.</span><span class="sxs-lookup"><span data-stu-id="678f9-122">After selecting students to hire for the internship positions, you'll enter each student’s information in the **Position details** for the position that you're hiring them for.</span></span> <span data-ttu-id="678f9-123">Þegar að hafa verið færðar inn allar upplýsingar um stöðu, veljið stöðuna í fjöldaráðningarverk síðu, og smellið síðan á **Ráða**.</span><span class="sxs-lookup"><span data-stu-id="678f9-123">When you have entered all of the position details, select the position in the Mass hire projects page, and then click **Hire**.</span></span> <span data-ttu-id="678f9-124">Stöðufærsla verður stofnuð fyrir hverja stöðu og skrá starfsmanns stofnuð og úthlutað á rétta stöðu fyrir hvern einstakling sem þú ræður.</span><span class="sxs-lookup"><span data-stu-id="678f9-124">A position record will be created for each position and a worker record will be created and assigned to the correct position for each person who you hire.</span></span>

## <a name="mass-hire-project-statuses"></a><span data-ttu-id="678f9-125">Stöður fjöldaráðningarverks</span><span class="sxs-lookup"><span data-stu-id="678f9-125">Mass hire project statuses</span></span>
<span data-ttu-id="678f9-126">ráðningarverk getur verið með eftirfarandi stöður:</span><span class="sxs-lookup"><span data-stu-id="678f9-126">A mass hire project can have the following statuses.</span></span>
-   <span data-ttu-id="678f9-127">Stofnaður</span><span class="sxs-lookup"><span data-stu-id="678f9-127">Created</span></span>
-   <span data-ttu-id="678f9-128">Opna</span><span class="sxs-lookup"><span data-stu-id="678f9-128">Open</span></span>
-   <span data-ttu-id="678f9-129">Lokað</span><span class="sxs-lookup"><span data-stu-id="678f9-129">Closed</span></span>

<span data-ttu-id="678f9-130">Á **fjöldaráðningarverk** síðunni er smellt á **Opna verk** eða **Loka verki** til að breyta stöðu fjöldaráðningarverks.</span><span class="sxs-lookup"><span data-stu-id="678f9-130">On the **Mass hire project** page, click **Open project** or **Close project** to change the status of a mass hire project.</span></span> <span data-ttu-id="678f9-131">Eftirfarandi tafla lýsir því hvað hægt er að gera við verk eftir því hver staða þess er.</span><span class="sxs-lookup"><span data-stu-id="678f9-131">The following table describes what you can do with a project according to its status.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="678f9-132">Staða</span><span class="sxs-lookup"><span data-stu-id="678f9-132">Status</span></span></th>
<th><span data-ttu-id="678f9-133">Lýsing</span><span class="sxs-lookup"><span data-stu-id="678f9-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="678f9-134">Stofnaður</span><span class="sxs-lookup"><span data-stu-id="678f9-134">Created</span></span></td>
<td><span data-ttu-id="678f9-135">Hægt er að stofna og breyta upplýsingum en ekki er hægt að stofna stöður fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="678f9-135">You can create and modify information, but cannot create positions for the project.</span></span> <span data-ttu-id="678f9-136">Þetta er sjálfgefin staða fyrir ný verk.</span><span class="sxs-lookup"><span data-stu-id="678f9-136">This is the default status for new projects.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="678f9-137">Opna</span><span class="sxs-lookup"><span data-stu-id="678f9-137">Open</span></span></td>
<td><span data-ttu-id="678f9-138">Hægt er að breyta upplýsingum um verk, stofna stöður fyrir fjöldaráðningarverk og ráða fólk í stöður.</span><span class="sxs-lookup"><span data-stu-id="678f9-138">You can modify the project details, create positions for the mass hire project, and hire people for the positions.</span></span> <span data-ttu-id="678f9-139">Þetta er staða virkra verka.</span><span class="sxs-lookup"><span data-stu-id="678f9-139">This is the status for active projects.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="678f9-140">Lokað</span><span class="sxs-lookup"><span data-stu-id="678f9-140">Closed</span></span></td>
<td><span data-ttu-id="678f9-141">Ekki er hægt að bæta stöðum við verkið.</span><span class="sxs-lookup"><span data-stu-id="678f9-141">You cannot add positions to the project.</span></span> <span data-ttu-id="678f9-142">Til að bæta stöðum við fjöldaráðningarverkið, opna verkið aftur.</span><span class="sxs-lookup"><span data-stu-id="678f9-142">To add positions to the mass hire project, open the project again.</span></span> <span data-ttu-id="678f9-143">Þetta er staða lokaðra verka.</span><span class="sxs-lookup"><span data-stu-id="678f9-143">This is the status for completed projects.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="678f9-144"><strong>Ábending </strong></span><span class="sxs-lookup"><span data-stu-id="678f9-144"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="678f9-145">Áður en hægt er að loka fjöldaráðningaverki, verða allar stöður í verkinu að hafa stöðu annað hvort Stofnuð eða Lokuð.</span><span class="sxs-lookup"><span data-stu-id="678f9-145">Before you can close a mass hire project, all positions in the project must have a status of either Created or Closed.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
</tbody>
</table>

 






