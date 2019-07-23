---
title: Uppsetning námskeiða
description: Mannauðsstjórar og stjórnendur geta notað eiginleika námskeiðsaðgerða til að viðhalda upplýsingum um þjálfun sem er í boði fyrir starfsmenn.
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 26e76d68c6d5c8bd965e65e65d57f239fb8a2918
ms.sourcegitcommit: 87e8b811680b1f87a973ce1680f07d657fa23046
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/24/2019
ms.locfileid: "1701391"
---
# <a name="set-up-training-courses"></a><span data-ttu-id="816b8-103">Uppsetning námskeiða</span><span class="sxs-lookup"><span data-stu-id="816b8-103">Set up training courses</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="816b8-104">Mannauðsstjórar og stjórnendur geta notað eiginleika námskeiðsaðgerða til að viðhalda upplýsingum um þjálfun sem er í boði fyrir starfsmenn.</span><span class="sxs-lookup"><span data-stu-id="816b8-104">Human resources administrators and managers can use the courses features to maintain information about the training that's offered to workers.</span></span>

 <a name="set-up-prerequisites"></a><span data-ttu-id="816b8-105">Uppsetningarforkröfur</span><span class="sxs-lookup"><span data-stu-id="816b8-105">Set up prerequisites</span></span>
---------------------

<span data-ttu-id="816b8-106">Eftirfarandi upplýsingar þarf og setja verður upp áður en hægt er að stofna námskeið.</span><span class="sxs-lookup"><span data-stu-id="816b8-106">The following information is required and must be set up before you create courses.</span></span>
-   <span data-ttu-id="816b8-107">**Námskeiðsgerðir**</span><span class="sxs-lookup"><span data-stu-id="816b8-107">**Course types**</span></span>

<span data-ttu-id="816b8-108">Eftirfarandi upplýsingar eru valfrjálsar upplýsingar sem hægt er að tilgreina fyrir námskeið.</span><span class="sxs-lookup"><span data-stu-id="816b8-108">The following information is optional information that you can specify for courses.</span></span> <span data-ttu-id="816b8-109">Ef þú veist að þú munt færa inn þessar upplýsingar fyrir námskeið, ætti að setja upp upplýsingarnar áður en myndaðar eru skráningar fyrir námskeiðið.</span><span class="sxs-lookup"><span data-stu-id="816b8-109">If you know that you will be entering this information for courses, you should set up this information before you create course records.</span></span>
-   <span data-ttu-id="816b8-110">**Kennslustofuflokkar**</span><span class="sxs-lookup"><span data-stu-id="816b8-110">**Classroom groups**</span></span>
-   <span data-ttu-id="816b8-111">**Námskeiðshópar**</span><span class="sxs-lookup"><span data-stu-id="816b8-111">**Course groups**</span></span>
-   <span data-ttu-id="816b8-112">**Námskeiðsstaðir**</span><span class="sxs-lookup"><span data-stu-id="816b8-112">**Course locations**</span></span>
-   <span data-ttu-id="816b8-113">**Kennslustofur**</span><span class="sxs-lookup"><span data-stu-id="816b8-113">**Classrooms**</span></span>
-   <span data-ttu-id="816b8-114">**Leiðbeinendur**</span><span class="sxs-lookup"><span data-stu-id="816b8-114">**Instructors**</span></span>

## <a name="course-types"></a><span data-ttu-id="816b8-115">Námskeiðsgerðir</span><span class="sxs-lookup"><span data-stu-id="816b8-115">Course types</span></span>
<span data-ttu-id="816b8-116">Hægt er að nota námskeiðsgerðir til að flokka námskeið samkvæmt skipan eða efni námskeiðsins.</span><span class="sxs-lookup"><span data-stu-id="816b8-116">You can use course types to categorize courses according to the structure or content of the course.</span></span> <span data-ttu-id="816b8-117">Hægt er að stofna námskeiðsgerðir á **Námskeiðsgerðir** síðu.</span><span class="sxs-lookup"><span data-stu-id="816b8-117">You can create course types on the **Course types** page.</span></span> <span data-ttu-id="816b8-118">Velja verður gerð námskeiðs þegar stofnuð er skrá á námskeið.</span><span class="sxs-lookup"><span data-stu-id="816b8-118">You must select a course type when you create a course record.</span></span>

## <a name="course-setup-type"></a><span data-ttu-id="816b8-119">Uppsetning námskeiðsgerðar</span><span class="sxs-lookup"><span data-stu-id="816b8-119">Course setup type</span></span>
<span data-ttu-id="816b8-120">Í eftirfarandi töflu er listi yfir þrjár gerðir uppsetningu fyrir námskeið.</span><span class="sxs-lookup"><span data-stu-id="816b8-120">The following table lists the three setup types for courses.</span></span> <span data-ttu-id="816b8-121">Uppsetningargerðir ákvarða skipan námskeiðs.</span><span class="sxs-lookup"><span data-stu-id="816b8-121">Setup types determine the structure of the course.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="816b8-122">Gerð uppsetningar</span><span class="sxs-lookup"><span data-stu-id="816b8-122">Setup type</span></span></th>
<th><span data-ttu-id="816b8-123">Lýsing</span><span class="sxs-lookup"><span data-stu-id="816b8-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="816b8-124"><strong>Staðlað</strong></span><span class="sxs-lookup"><span data-stu-id="816b8-124"><strong>Standard</strong></span></span></td>
<td><span data-ttu-id="816b8-125">Veljið þessa gerð fyrir námskeið sem hafa ekki dagskrá.</span><span class="sxs-lookup"><span data-stu-id="816b8-125">Select this type for courses that will not have a daily agenda.</span></span> <span data-ttu-id="816b8-126">Þetta er sjálfgefin gerð uppsetningu þegar nýtt námskeið er stofnað.</span><span class="sxs-lookup"><span data-stu-id="816b8-126">This is the default setup type when you create a new course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="816b8-127"><strong>Dagskrá</strong></span><span class="sxs-lookup"><span data-stu-id="816b8-127"><strong>Agenda</strong></span></span></td>
<td><span data-ttu-id="816b8-128">Veljið þessa gerð til að áætla upplýsingar um hvern dag á námskeiði sem á sér stað yfir marga daga.</span><span class="sxs-lookup"><span data-stu-id="816b8-128">Select this type to plan the details of each day of a course that takes place over multiple days.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="816b8-129"><strong>Dagskrá ‚+ lotur</strong></span><span class="sxs-lookup"><span data-stu-id="816b8-129"><strong>Agenda + session</strong></span></span></td>
<td><span data-ttu-id="816b8-130">Veljið þessa gerð fyrir flóknari námskeið.</span><span class="sxs-lookup"><span data-stu-id="816b8-130">Select this type for the more complex courses.</span></span> <span data-ttu-id="816b8-131">Til dæmis er hægt að skipta dagskrá fyrir námskeið í námskeiðshluta og lotur.</span><span class="sxs-lookup"><span data-stu-id="816b8-131">For example, you can divide the agenda for the course into tracks and sessions.</span></span>
<ul>
<li><span data-ttu-id="816b8-132"><strong>Skor</strong> - Skor eru ákveðin fagsvið fyrir námskeið.</span><span class="sxs-lookup"><span data-stu-id="816b8-132"><strong>Track</strong> – Tracks are specific subject areas for a course.</span></span></li>
<li><span data-ttu-id="816b8-133"><strong>Lotur</strong> - Lotur skipta upp skorum og geta aðstoðað við að bera kennsl á sérstakar aðferðir eða tækni sem eru viðeigandi fyrir hvert skor.</span><span class="sxs-lookup"><span data-stu-id="816b8-133"><strong>Sessions</strong> – Sessions divide up tracks and help identify specific processes or techniques that are relevant to the track.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a><span data-ttu-id="816b8-134">Verkefni námskeiðs</span><span class="sxs-lookup"><span data-stu-id="816b8-134">Course tasks</span></span>
<span data-ttu-id="816b8-135">Fyrir hvern tilgang er hægt að ljúka eftir farandi verkum.</span><span class="sxs-lookup"><span data-stu-id="816b8-135">For each course, you can complete the following tasks.</span></span>
- <span data-ttu-id="816b8-136">Skrá þátttakendur</span><span class="sxs-lookup"><span data-stu-id="816b8-136">Register participants</span></span>
- <span data-ttu-id="816b8-137">Tilgreina lokadagsetningu skráningar</span><span class="sxs-lookup"><span data-stu-id="816b8-137">Specify a registration deadline</span></span>
- <span data-ttu-id="816b8-138">Tilgreina hámarks- og lágmarksfjölda þátttakenda.</span><span class="sxs-lookup"><span data-stu-id="816b8-138">Define the minimum and maximum number of participants</span></span>
- <span data-ttu-id="816b8-139">Úthluta staðsetningu og kennslustofu á námskeið.</span><span class="sxs-lookup"><span data-stu-id="816b8-139">Assign a course location and classroom</span></span>
- <span data-ttu-id="816b8-140">Mæla með hótelum fyrir þátttakendur námskeiðs.</span><span class="sxs-lookup"><span data-stu-id="816b8-140">Recommend hotels to course participants</span></span>
- <span data-ttu-id="816b8-141">Stofna námskeiðslýsingu, sem síðan er hægt að auglýsa á sjálfsafgreiðslu°starfsmanna</span><span class="sxs-lookup"><span data-stu-id="816b8-141">Create a course description, which you can then advertise on Employee self service</span></span>

  ><span data-ttu-id="816b8-142">**Athugasemd** Aðeins er hægt að eyða námskeiði ef enginn hefur skráð sig á það.</span><span class="sxs-lookup"><span data-stu-id="816b8-142">**Note** You can delete a course only if no one has registered for it.</span></span> 

## <a name="course-statuses"></a><span data-ttu-id="816b8-143">Stöður námskeiðs</span><span class="sxs-lookup"><span data-stu-id="816b8-143">Course statuses</span></span>
<span data-ttu-id="816b8-144">Í eftirfarandi töflu er listi yfir stöður mögulegar námskeiðs og aðgerðir sem hægt er að ljúka við námskeið sem hefur tiltekna stöðu.</span><span class="sxs-lookup"><span data-stu-id="816b8-144">The following table lists the possible course statuses and the actions that you can complete when the course has a specific status.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="816b8-145">Staða</span><span class="sxs-lookup"><span data-stu-id="816b8-145">Status</span></span></th>
<th><span data-ttu-id="816b8-146">Aðgerðir</span><span class="sxs-lookup"><span data-stu-id="816b8-146">Actions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="816b8-147"><strong>Stofnaður</strong></span><span class="sxs-lookup"><span data-stu-id="816b8-147"><strong>Created</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="816b8-148">Færðu inn og breyttu upplýsingum námskeiðs.</span><span class="sxs-lookup"><span data-stu-id="816b8-148">Enter and modify course information.</span></span></li>
<li><span data-ttu-id="816b8-149">Breyta námskeiðsstöðunni í <strong>Opin</strong> svo að starfsmenn geta skráð sig í námskeiðið.</span><span class="sxs-lookup"><span data-stu-id="816b8-149">Change the course status to <strong>Open</strong> so that workers can register for the course.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="816b8-150"><strong>Opna</strong></span><span class="sxs-lookup"><span data-stu-id="816b8-150"><strong>Open</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="816b8-151">Skrá þátttakendur á námskeiðið</span><span class="sxs-lookup"><span data-stu-id="816b8-151">Register participants for the course.</span></span></li>
<li><span data-ttu-id="816b8-152">Fjarlægja þátttakendur úr námskeið.</span><span class="sxs-lookup"><span data-stu-id="816b8-152">Remove participants from the course.</span></span></li>
<li><span data-ttu-id="816b8-153">Staðfesta þátttakendur í námskeið.</span><span class="sxs-lookup"><span data-stu-id="816b8-153">Confirm participants for the course.</span></span></li>
<li><span data-ttu-id="816b8-154">Breyta námskeiðsstöðunni í <strong>Lokað</strong> eða <strong>Hætt við</strong>.</span><span class="sxs-lookup"><span data-stu-id="816b8-154">Change the course status to <strong>Closed</strong> or <strong>Canceled</strong>.</span></span></li>
<li><span data-ttu-id="816b8-155">Áætla spurningalista fyrir þátttakendur sem eru með stöðuna <strong>Staðfest</strong>.</span><span class="sxs-lookup"><span data-stu-id="816b8-155">Plan questionnaires for participants whose status is <strong>Confirmed</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="816b8-156"><strong>Lokað</strong></span><span class="sxs-lookup"><span data-stu-id="816b8-156"><strong>Closed</strong></span></span></td>
<td><span data-ttu-id="816b8-157">Hægt er að opna námskeiðið aftur.</span><span class="sxs-lookup"><span data-stu-id="816b8-157">You can reopen the course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="816b8-158"><strong>Hætt við</strong></span><span class="sxs-lookup"><span data-stu-id="816b8-158"><strong>Canceled</strong></span></span></td>
<td><span data-ttu-id="816b8-159">Hægt er að opna námskeiðið aftur.</span><span class="sxs-lookup"><span data-stu-id="816b8-159">You can reopen the course.</span></span></td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a><span data-ttu-id="816b8-160">Þátttakendur á námskeiði</span><span class="sxs-lookup"><span data-stu-id="816b8-160">Course participants</span></span>
<span data-ttu-id="816b8-161">Þátttakendur á námskeiði eru starfsmenn sem taka þátt í þjálfunarnámskeiði eða atburði.</span><span class="sxs-lookup"><span data-stu-id="816b8-161">Course participants are workers who participate in a training course or event.</span></span> <span data-ttu-id="816b8-162">Aðeins er hægt að skrá þátttakendur í opin námskeið.</span><span class="sxs-lookup"><span data-stu-id="816b8-162">You can only register participants for open courses.</span></span> <span data-ttu-id="816b8-163">Lágmarks og hámarksfjöldi þátttakenda sem hægt er að skrá á námskeið er skilgreindur á flýtiflipanum **Almennt** í skjámyndinni **Námskeið**.</span><span class="sxs-lookup"><span data-stu-id="816b8-163">The minimum and maximum number of participants that you can register for a course is defined on the **General** FastTab on the **Courses** page.</span></span>

<a name="workflow"></a><span data-ttu-id="816b8-164">Verkflæði</span><span class="sxs-lookup"><span data-stu-id="816b8-164">Workflow</span></span>
--------

<span data-ttu-id="816b8-165">Starfsmenn sem skrá sig á námskeið gegnum í **Starfsmanns sjálfsafgreiðsla** síðu geta verið með skráningu beint í gegnum verkflæði fyrir samþykki.</span><span class="sxs-lookup"><span data-stu-id="816b8-165">Employees who register for a course through the **Employee self service** page can have their registration routed through workflow for approval.</span></span> <span data-ttu-id="816b8-166">Þú getur úthlutað verkflæði fyrir námskeið í flýtiflipanum **Almennt** á síðunni **Námskeið**.</span><span class="sxs-lookup"><span data-stu-id="816b8-166">You can assign a workflow to a course on the **General** FastTab on the **Courses** page.</span></span>





