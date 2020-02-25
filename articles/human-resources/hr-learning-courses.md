---
title: Uppsetning námskeiða
description: Mannauðsstjórar og stjórnendur geta notað eiginleika námskeiðsaðgerða til að viðhalda upplýsingum um þjálfun sem er í boði fyrir starfsmenn.
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: c3c23ab6fca3f97fbca9edfe83c656e7ca8a2800
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009401"
---
# <a name="set-up-training-courses"></a><span data-ttu-id="2772d-103">Uppsetning námskeiða</span><span class="sxs-lookup"><span data-stu-id="2772d-103">Set up training courses</span></span>

<span data-ttu-id="2772d-104">Mannauðsstjórar og stjórnendur geta notað eiginleika námskeiðsaðgerða til að viðhalda upplýsingum um þjálfun sem er í boði fyrir starfsmenn.</span><span class="sxs-lookup"><span data-stu-id="2772d-104">Human resources administrators and managers can use the courses features to maintain information about the training that's offered to workers.</span></span>

 <a name="set-up-prerequisites"></a><span data-ttu-id="2772d-105">Uppsetningarforkröfur</span><span class="sxs-lookup"><span data-stu-id="2772d-105">Set up prerequisites</span></span>
---------------------

<span data-ttu-id="2772d-106">Eftirfarandi upplýsingar þarf og setja verður upp áður en hægt er að stofna námskeið.</span><span class="sxs-lookup"><span data-stu-id="2772d-106">The following information is required and must be set up before you create courses.</span></span>
-   <span data-ttu-id="2772d-107">**Námskeiðsgerðir**</span><span class="sxs-lookup"><span data-stu-id="2772d-107">**Course types**</span></span>

<span data-ttu-id="2772d-108">Eftirfarandi upplýsingar eru valfrjálsar upplýsingar sem hægt er að tilgreina fyrir námskeið.</span><span class="sxs-lookup"><span data-stu-id="2772d-108">The following information is optional information that you can specify for courses.</span></span> <span data-ttu-id="2772d-109">Ef þú veist að þú munt færa inn þessar upplýsingar fyrir námskeið, ætti að setja upp upplýsingarnar áður en myndaðar eru skráningar fyrir námskeiðið.</span><span class="sxs-lookup"><span data-stu-id="2772d-109">If you know that you will be entering this information for courses, you should set up this information before you create course records.</span></span>
-   <span data-ttu-id="2772d-110">**Kennslustofuflokkar**</span><span class="sxs-lookup"><span data-stu-id="2772d-110">**Classroom groups**</span></span>
-   <span data-ttu-id="2772d-111">**Námskeiðshópar**</span><span class="sxs-lookup"><span data-stu-id="2772d-111">**Course groups**</span></span>
-   <span data-ttu-id="2772d-112">**Námskeiðsstaðir**</span><span class="sxs-lookup"><span data-stu-id="2772d-112">**Course locations**</span></span>
-   <span data-ttu-id="2772d-113">**Kennslustofur**</span><span class="sxs-lookup"><span data-stu-id="2772d-113">**Classrooms**</span></span>
-   <span data-ttu-id="2772d-114">**Leiðbeinendur**</span><span class="sxs-lookup"><span data-stu-id="2772d-114">**Instructors**</span></span>

## <a name="course-types"></a><span data-ttu-id="2772d-115">Námskeiðsgerðir</span><span class="sxs-lookup"><span data-stu-id="2772d-115">Course types</span></span>
<span data-ttu-id="2772d-116">Hægt er að nota námskeiðsgerðir til að flokka námskeið samkvæmt skipan eða efni námskeiðsins.</span><span class="sxs-lookup"><span data-stu-id="2772d-116">You can use course types to categorize courses according to the structure or content of the course.</span></span> <span data-ttu-id="2772d-117">Hægt er að stofna námskeiðsgerðir á **Námskeiðsgerðir** síðu.</span><span class="sxs-lookup"><span data-stu-id="2772d-117">You can create course types on the **Course types** page.</span></span> <span data-ttu-id="2772d-118">Velja verður gerð námskeiðs þegar stofnuð er skrá á námskeið.</span><span class="sxs-lookup"><span data-stu-id="2772d-118">You must select a course type when you create a course record.</span></span>

## <a name="course-setup-type"></a><span data-ttu-id="2772d-119">Uppsetning námskeiðsgerðar</span><span class="sxs-lookup"><span data-stu-id="2772d-119">Course setup type</span></span>
<span data-ttu-id="2772d-120">Í eftirfarandi töflu er listi yfir þrjár gerðir uppsetningu fyrir námskeið.</span><span class="sxs-lookup"><span data-stu-id="2772d-120">The following table lists the three setup types for courses.</span></span> <span data-ttu-id="2772d-121">Uppsetningargerðir ákvarða skipan námskeiðs.</span><span class="sxs-lookup"><span data-stu-id="2772d-121">Setup types determine the structure of the course.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2772d-122">Gerð uppsetningar</span><span class="sxs-lookup"><span data-stu-id="2772d-122">Setup type</span></span></th>
<th><span data-ttu-id="2772d-123">Lýsing</span><span class="sxs-lookup"><span data-stu-id="2772d-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2772d-124"><strong>Staðlað</strong></span><span class="sxs-lookup"><span data-stu-id="2772d-124"><strong>Standard</strong></span></span></td>
<td><span data-ttu-id="2772d-125">Veljið þessa gerð fyrir námskeið sem hafa ekki dagskrá.</span><span class="sxs-lookup"><span data-stu-id="2772d-125">Select this type for courses that will not have a daily agenda.</span></span> <span data-ttu-id="2772d-126">Þetta er sjálfgefin gerð uppsetningu þegar nýtt námskeið er stofnað.</span><span class="sxs-lookup"><span data-stu-id="2772d-126">This is the default setup type when you create a new course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2772d-127"><strong>Dagskrá</strong></span><span class="sxs-lookup"><span data-stu-id="2772d-127"><strong>Agenda</strong></span></span></td>
<td><span data-ttu-id="2772d-128">Veljið þessa gerð til að áætla upplýsingar um hvern dag á námskeiði sem á sér stað yfir marga daga.</span><span class="sxs-lookup"><span data-stu-id="2772d-128">Select this type to plan the details of each day of a course that takes place over multiple days.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2772d-129"><strong>Dagskrá ‚+ lotur</strong></span><span class="sxs-lookup"><span data-stu-id="2772d-129"><strong>Agenda + session</strong></span></span></td>
<td><span data-ttu-id="2772d-130">Veljið þessa gerð fyrir flóknari námskeið.</span><span class="sxs-lookup"><span data-stu-id="2772d-130">Select this type for the more complex courses.</span></span> <span data-ttu-id="2772d-131">Til dæmis er hægt að skipta dagskrá fyrir námskeið í námskeiðshluta og lotur.</span><span class="sxs-lookup"><span data-stu-id="2772d-131">For example, you can divide the agenda for the course into tracks and sessions.</span></span>
<ul>
<li><span data-ttu-id="2772d-132"><strong>Skor</strong> - Skor eru ákveðin fagsvið fyrir námskeið.</span><span class="sxs-lookup"><span data-stu-id="2772d-132"><strong>Track</strong> – Tracks are specific subject areas for a course.</span></span></li>
<li><span data-ttu-id="2772d-133"><strong>Lotur</strong> - Lotur skipta upp skorum og geta aðstoðað við að bera kennsl á sérstakar aðferðir eða tækni sem eru viðeigandi fyrir hvert skor.</span><span class="sxs-lookup"><span data-stu-id="2772d-133"><strong>Sessions</strong> – Sessions divide up tracks and help identify specific processes or techniques that are relevant to the track.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a><span data-ttu-id="2772d-134">Verkefni námskeiðs</span><span class="sxs-lookup"><span data-stu-id="2772d-134">Course tasks</span></span>
<span data-ttu-id="2772d-135">Fyrir hvern tilgang er hægt að ljúka eftir farandi verkum.</span><span class="sxs-lookup"><span data-stu-id="2772d-135">For each course, you can complete the following tasks.</span></span>
- <span data-ttu-id="2772d-136">Skrá þátttakendur</span><span class="sxs-lookup"><span data-stu-id="2772d-136">Register participants</span></span>
- <span data-ttu-id="2772d-137">Tilgreina lokadagsetningu skráningar</span><span class="sxs-lookup"><span data-stu-id="2772d-137">Specify a registration deadline</span></span>
- <span data-ttu-id="2772d-138">Tilgreina hámarks- og lágmarksfjölda þátttakenda.</span><span class="sxs-lookup"><span data-stu-id="2772d-138">Define the minimum and maximum number of participants</span></span>
- <span data-ttu-id="2772d-139">Úthluta staðsetningu og kennslustofu á námskeið.</span><span class="sxs-lookup"><span data-stu-id="2772d-139">Assign a course location and classroom</span></span>
- <span data-ttu-id="2772d-140">Mæla með hótelum fyrir þátttakendur námskeiðs.</span><span class="sxs-lookup"><span data-stu-id="2772d-140">Recommend hotels to course participants</span></span>
- <span data-ttu-id="2772d-141">Stofna námskeiðslýsingu, sem síðan er hægt að auglýsa á sjálfsafgreiðslu°starfsmanna</span><span class="sxs-lookup"><span data-stu-id="2772d-141">Create a course description, which you can then advertise on Employee self service</span></span>

  ><span data-ttu-id="2772d-142">**Athugasemd** Aðeins er hægt að eyða námskeiði ef enginn hefur skráð sig á það.</span><span class="sxs-lookup"><span data-stu-id="2772d-142">**Note** You can delete a course only if no one has registered for it.</span></span> 

## <a name="course-statuses"></a><span data-ttu-id="2772d-143">Stöður námskeiðs</span><span class="sxs-lookup"><span data-stu-id="2772d-143">Course statuses</span></span>
<span data-ttu-id="2772d-144">Í eftirfarandi töflu er listi yfir stöður mögulegar námskeiðs og aðgerðir sem hægt er að ljúka við námskeið sem hefur tiltekna stöðu.</span><span class="sxs-lookup"><span data-stu-id="2772d-144">The following table lists the possible course statuses and the actions that you can complete when the course has a specific status.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2772d-145">Staða</span><span class="sxs-lookup"><span data-stu-id="2772d-145">Status</span></span></th>
<th><span data-ttu-id="2772d-146">Aðgerðir</span><span class="sxs-lookup"><span data-stu-id="2772d-146">Actions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2772d-147"><strong>Stofnaður</strong></span><span class="sxs-lookup"><span data-stu-id="2772d-147"><strong>Created</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="2772d-148">Færðu inn og breyttu upplýsingum námskeiðs.</span><span class="sxs-lookup"><span data-stu-id="2772d-148">Enter and modify course information.</span></span></li>
<li><span data-ttu-id="2772d-149">Breyta námskeiðsstöðunni í <strong>Opin</strong> svo að starfsmenn geta skráð sig í námskeiðið.</span><span class="sxs-lookup"><span data-stu-id="2772d-149">Change the course status to <strong>Open</strong> so that workers can register for the course.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2772d-150"><strong>Opna</strong></span><span class="sxs-lookup"><span data-stu-id="2772d-150"><strong>Open</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="2772d-151">Skrá þátttakendur á námskeiðið</span><span class="sxs-lookup"><span data-stu-id="2772d-151">Register participants for the course.</span></span></li>
<li><span data-ttu-id="2772d-152">Fjarlægja þátttakendur úr námskeið.</span><span class="sxs-lookup"><span data-stu-id="2772d-152">Remove participants from the course.</span></span></li>
<li><span data-ttu-id="2772d-153">Staðfesta þátttakendur í námskeið.</span><span class="sxs-lookup"><span data-stu-id="2772d-153">Confirm participants for the course.</span></span></li>
<li><span data-ttu-id="2772d-154">Breyta námskeiðsstöðunni í <strong>Lokað</strong> eða <strong>Hætt við</strong>.</span><span class="sxs-lookup"><span data-stu-id="2772d-154">Change the course status to <strong>Closed</strong> or <strong>Canceled</strong>.</span></span></li>
<li><span data-ttu-id="2772d-155">Áætla spurningalista fyrir þátttakendur sem eru með stöðuna <strong>Staðfest</strong>.</span><span class="sxs-lookup"><span data-stu-id="2772d-155">Plan questionnaires for participants whose status is <strong>Confirmed</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2772d-156"><strong>Lokað</strong></span><span class="sxs-lookup"><span data-stu-id="2772d-156"><strong>Closed</strong></span></span></td>
<td><span data-ttu-id="2772d-157">Hægt er að opna námskeiðið aftur.</span><span class="sxs-lookup"><span data-stu-id="2772d-157">You can reopen the course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2772d-158"><strong>Hætt við</strong></span><span class="sxs-lookup"><span data-stu-id="2772d-158"><strong>Canceled</strong></span></span></td>
<td><span data-ttu-id="2772d-159">Hægt er að opna námskeiðið aftur.</span><span class="sxs-lookup"><span data-stu-id="2772d-159">You can reopen the course.</span></span></td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a><span data-ttu-id="2772d-160">Þátttakendur á námskeiði</span><span class="sxs-lookup"><span data-stu-id="2772d-160">Course participants</span></span>
<span data-ttu-id="2772d-161">Þátttakendur á námskeiði eru starfsmenn sem taka þátt í þjálfunarnámskeiði eða atburði.</span><span class="sxs-lookup"><span data-stu-id="2772d-161">Course participants are workers who participate in a training course or event.</span></span> <span data-ttu-id="2772d-162">Aðeins er hægt að skrá þátttakendur í opin námskeið.</span><span class="sxs-lookup"><span data-stu-id="2772d-162">You can only register participants for open courses.</span></span> <span data-ttu-id="2772d-163">Lágmarks og hámarksfjöldi þátttakenda sem hægt er að skrá á námskeið er skilgreindur á flýtiflipanum **Almennt** í skjámyndinni **Námskeið**.</span><span class="sxs-lookup"><span data-stu-id="2772d-163">The minimum and maximum number of participants that you can register for a course is defined on the **General** FastTab on the **Courses** page.</span></span>

<a name="workflow"></a><span data-ttu-id="2772d-164">Verkflæði</span><span class="sxs-lookup"><span data-stu-id="2772d-164">Workflow</span></span>
--------

<span data-ttu-id="2772d-165">Starfsmenn sem skrá sig á námskeið gegnum í **Starfsmanns sjálfsafgreiðsla** síðu geta verið með skráningu beint í gegnum verkflæði fyrir samþykki.</span><span class="sxs-lookup"><span data-stu-id="2772d-165">Employees who register for a course through the **Employee self service** page can have their registration routed through workflow for approval.</span></span> <span data-ttu-id="2772d-166">Þú getur úthlutað verkflæði fyrir námskeið í flýtiflipanum **Almennt** á síðunni **Námskeið**.</span><span class="sxs-lookup"><span data-stu-id="2772d-166">You can assign a workflow to a course on the **General** FastTab on the **Courses** page.</span></span>





