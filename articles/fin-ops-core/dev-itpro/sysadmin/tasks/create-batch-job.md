---
title: Stofna runuvinnslu
description: Runuvinnsla er flokkur verka sem er sendur til AOS-tilviksins (hugbúnaðarhlutarþjónstilviks) í sjálfvirka vinnslu.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e4360cd7068658a170f5b44c2ce7c71c39c44fa8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679889"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="e361e-103">Stofna runuvinnslu</span><span class="sxs-lookup"><span data-stu-id="e361e-103">Create a batch job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e361e-104">Runuvinnsla er flokkur verka sem er sendur til AOS-tilviksins (hugbúnaðarhlutarþjónstilviks) í sjálfvirka vinnslu.</span><span class="sxs-lookup"><span data-stu-id="e361e-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="e361e-105">Runuvinnslur er keyrðar með því að nota öryggis- og notendaheimildir þess notanda sem stofnaði verkið.</span><span class="sxs-lookup"><span data-stu-id="e361e-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="e361e-106">Fylgið eftirfarandi ferli ef stofna á runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="e361e-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="e361e-107">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="e361e-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="e361e-108">Stofna runuvinnslu</span><span class="sxs-lookup"><span data-stu-id="e361e-108">Create the batch job</span></span>
1. <span data-ttu-id="e361e-109">Farðu í **Skoðunarrúðu > Kerfiseiningar > Kerfisstjórnun > Fyrirspurnir > Runuvinnslur**.</span><span class="sxs-lookup"><span data-stu-id="e361e-109">Go to **Navigation pane > Modules > System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="e361e-110">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="e361e-110">Click **New**.</span></span>
3. <span data-ttu-id="e361e-111">Færðu inn gildi í reitnum **Starfslýsing**.</span><span class="sxs-lookup"><span data-stu-id="e361e-111">In the **Job description** field, type a value.</span></span>
4. <span data-ttu-id="e361e-112">Í reitinn **Áætluð upphafsdags./-tími** skráirðu dags. og tíma.</span><span class="sxs-lookup"><span data-stu-id="e361e-112">In the **Scheduled start date/time** field, enter a date and time.</span></span>
5. <span data-ttu-id="e361e-113">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e361e-113">Click **Save**.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="e361e-114">Stofna endurtekningu</span><span class="sxs-lookup"><span data-stu-id="e361e-114">Create a recurrence</span></span>
1. <span data-ttu-id="e361e-115">Í aðgerðasvæðinu er smellt á **Runuvinnsla**.</span><span class="sxs-lookup"><span data-stu-id="e361e-115">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="e361e-116">Smelltu á **Endurtekning**.</span><span class="sxs-lookup"><span data-stu-id="e361e-116">Click **Recurrence**.</span></span> <span data-ttu-id="e361e-117">Notið þessa valkosti til að færa inn afmörkun og mynstur fyrir endurtekninguna.</span><span class="sxs-lookup"><span data-stu-id="e361e-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="e361e-118">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="e361e-118">Click **OK**.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="e361e-119">Bæta við viðvaranir</span><span class="sxs-lookup"><span data-stu-id="e361e-119">Add alerts</span></span>
1. <span data-ttu-id="e361e-120">Í aðgerðasvæðinu er smellt á **Runuvinnsla**.</span><span class="sxs-lookup"><span data-stu-id="e361e-120">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="e361e-121">Smelltu á **Viðvaranir**.</span><span class="sxs-lookup"><span data-stu-id="e361e-121">Click **Alerts**.</span></span> <span data-ttu-id="e361e-122">Tilgreina hvort óskað sé eftir að viðvörunarboðin birtist þegar runuvinnsla lýkur, villa er til staðar eða hætt er við.</span><span class="sxs-lookup"><span data-stu-id="e361e-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="e361e-123">Tilgreinið síðan ef óskað er eftir að viðvaranir birtist sem sprettigluggar.</span><span class="sxs-lookup"><span data-stu-id="e361e-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="e361e-124">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="e361e-124">Click **OK**.</span></span>

## <a name="adjust-batch-job-status"></a><span data-ttu-id="e361e-125">Stilla stöðu runuvinnslu</span><span class="sxs-lookup"><span data-stu-id="e361e-125">Adjust batch job status</span></span>
1. <span data-ttu-id="e361e-126">Farðu í **Kerfisstjórnun > Fyrirspurnir> Runuvinnslur**.</span><span class="sxs-lookup"><span data-stu-id="e361e-126">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="e361e-127">Veldu viðeigandi runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="e361e-127">Select the appropriate batch job.</span></span>
3. <span data-ttu-id="e361e-128">Í aðgerðasvæðinu smellirðu á **Runuvinnsla > Aðgerðir > Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="e361e-128">On the Action Pane, click **Batch job > Functions > Change status**.</span></span>
4. <span data-ttu-id="e361e-129">Veldu viðeigandi stöðu:</span><span class="sxs-lookup"><span data-stu-id="e361e-129">Select the appropriate status:</span></span>
    - <span data-ttu-id="e361e-130">**Halda eftir**: Stilla runuvinnsluna sem **halda eftir** svo að henni er haldið eftir í verkraðara runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="e361e-130">**Withhold**: Set the batch job as **withhold** so it is withheld from the batch job scheduler.</span></span> <span data-ttu-id="e361e-131">Jafngildir *stöðva*.</span><span class="sxs-lookup"><span data-stu-id="e361e-131">Equivalent to *stop*.</span></span>
    - <span data-ttu-id="e361e-132">**Bið**: Stilla runuvinnsluna sem **bið** svo að hún bíður þess að verkraðari runuvinnslu taki hana til.</span><span class="sxs-lookup"><span data-stu-id="e361e-132">**Waiting**: Set the batch job as **waiting** so it is waiting to be picked up by the batch job scheduler.</span></span> <span data-ttu-id="e361e-133">Jafngildir *ræsa*.</span><span class="sxs-lookup"><span data-stu-id="e361e-133">Equivalent to *go*.</span></span>
5. <span data-ttu-id="e361e-134">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="e361e-134">Click **OK**.</span></span>
