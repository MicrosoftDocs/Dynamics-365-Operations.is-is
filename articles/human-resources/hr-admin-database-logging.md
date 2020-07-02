---
title: Skilgreina og stjórna gagnagrunnsskráningu
description: Hægt er að rekja breytingar til taflna og reita í Dynamics 365 Human Resources með gagnagrunnsskráningu.
author: Darinkramer
manager: AnnBe
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3dc4658a0a13af95978c66f5aab882902f754a2d
ms.sourcegitcommit: 88f38d584c5befb96e4d1daab4b28af5519ef125
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/11/2020
ms.locfileid: "3443581"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="8ecaa-103">Skilgreina og stjórna gagnagrunnsskráningu</span><span class="sxs-lookup"><span data-stu-id="8ecaa-103">Configure and manage database logging</span></span>

<span data-ttu-id="8ecaa-104">Hægt er að rekja breytingar til taflna og reita í Dynamics 365 Human Resources með gagnagrunnsskráningu.</span><span class="sxs-lookup"><span data-stu-id="8ecaa-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="8ecaa-105">Þetta efnisatriði lýsir hvernig á að:</span><span class="sxs-lookup"><span data-stu-id="8ecaa-105">This topic describes how to:</span></span>

- <span data-ttu-id="8ecaa-106">Stjórna öryggi og afköstum fyrir skráningu gagnagrunns</span><span class="sxs-lookup"><span data-stu-id="8ecaa-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="8ecaa-107">Setja upp gagnagrunnsskráningu</span><span class="sxs-lookup"><span data-stu-id="8ecaa-107">Set up database logging</span></span>
- <span data-ttu-id="8ecaa-108">Hreinsa upp gagnagrunnsskrár</span><span class="sxs-lookup"><span data-stu-id="8ecaa-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="8ecaa-109">Yfirlit gagnagrunnsskráningar</span><span class="sxs-lookup"><span data-stu-id="8ecaa-109">Overview of database logging</span></span>

<span data-ttu-id="8ecaa-110">Skráning gagnagrunns rekur sérstakar breytingar til taflna og reita Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="8ecaa-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="8ecaa-111">Þessar breytingar fela í sér að setja inn, uppfæra eða eyða.</span><span class="sxs-lookup"><span data-stu-id="8ecaa-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="8ecaa-112">Gagnagrunnsskráning geymir færslur yfir breytingar á töflum í töflu gagnagrunnsskráar.</span><span class="sxs-lookup"><span data-stu-id="8ecaa-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="8ecaa-113">Notkun fyrirtækis á gagnagrunnsskráningu felur í sér:</span><span class="sxs-lookup"><span data-stu-id="8ecaa-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="8ecaa-114">Að búa til eftirlitsfærslu yfir breytinga á tilteknum töflum sem innihalda viðkvæmar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="8ecaa-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="8ecaa-115">Rakning einstakra færslna.</span><span class="sxs-lookup"><span data-stu-id="8ecaa-115">Tracking single transactions.</span></span> <span data-ttu-id="8ecaa-116">Gagnagrunnsskráning er ekki ætluð til þess að rekja sjálfvirkar færslur sem eru keyrðar í runuvinnslum.</span><span class="sxs-lookup"><span data-stu-id="8ecaa-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="8ecaa-117">Öryggi fyrir gagnagrunnsskráningu</span><span class="sxs-lookup"><span data-stu-id="8ecaa-117">Security for database logging</span></span>

<span data-ttu-id="8ecaa-118">Gagnagrunnskladdar geta innihaldið viðkvæm gögn.</span><span class="sxs-lookup"><span data-stu-id="8ecaa-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="8ecaa-119">Takmarkið aðgang til að hafa aðeins öryggishlutverk sem þurfa aðgang að skráningargögnum.</span><span class="sxs-lookup"><span data-stu-id="8ecaa-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="8ecaa-120">Gagnagrunnsskráning og afköst</span><span class="sxs-lookup"><span data-stu-id="8ecaa-120">Database logging and performance</span></span>

<span data-ttu-id="8ecaa-121">Þótt þetta sé mikilvægt fyrir fyrirtækið, getur gagnagrunnsskráning verið dýr í notkun á tilföngum og stjórnun.</span><span class="sxs-lookup"><span data-stu-id="8ecaa-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="8ecaa-122">Afköst vegna gagnagrunnsskráningar fela í sér:</span><span class="sxs-lookup"><span data-stu-id="8ecaa-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="8ecaa-123">Tafla gagnagrunnsskráar getur vaxið hratt og leitt til stækkunar á gagnagrunninum.</span><span class="sxs-lookup"><span data-stu-id="8ecaa-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="8ecaa-124">Vöxtur veltur á magni skráðra gagna sem þú ákveður að geyma.</span><span class="sxs-lookup"><span data-stu-id="8ecaa-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="8ecaa-125">Sjálfgefið er að tafla gagnagrunnsskráar haldi við aðeins 30 dögum af skráningargögnum.</span><span class="sxs-lookup"><span data-stu-id="8ecaa-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="8ecaa-126">Gagnagrunnsskráning getur haft neikvæð áhrif á sjálfvirk langtímaferli, t.d. langtíma gagnainnflutning.</span><span class="sxs-lookup"><span data-stu-id="8ecaa-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="8ecaa-127">Bestu venjur</span><span class="sxs-lookup"><span data-stu-id="8ecaa-127">Best practices</span></span>

<span data-ttu-id="8ecaa-128">Til að bæta afköst skal takmarka færslur skráar með því að velja tiltekna reiti til að skrá í stað heilla taflna.</span><span class="sxs-lookup"><span data-stu-id="8ecaa-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="8ecaa-129">Til að stuðla að betri heildarafköstum takmarkast gagnagrunnsskráningar við 20 töflur.</span><span class="sxs-lookup"><span data-stu-id="8ecaa-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="8ecaa-130">Aðeins er hægt að skrá uppfærslur fyrir einstaka reiti.</span><span class="sxs-lookup"><span data-stu-id="8ecaa-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="8ecaa-131">Setja upp gagnagrunnsskráningu</span><span class="sxs-lookup"><span data-stu-id="8ecaa-131">Set up database logging</span></span>

<span data-ttu-id="8ecaa-132">Hægt er að nota leiðsagnarforritið **Skrifa gagnagrunnsbreytingar í kladda** til að setja upp gagnagrunnsskráningu.</span><span class="sxs-lookup"><span data-stu-id="8ecaa-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="8ecaa-133">Leiðsagnarforritið býður upp á sveigjanlega leið til að setja upp kladdaskráningu fyrir töflur og reiti.</span><span class="sxs-lookup"><span data-stu-id="8ecaa-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="8ecaa-134">Farið í **Kerfisstjórnun > Tenglar > Gagnagrunnur > Uppsetning gagnagrunnskladda**.</span><span class="sxs-lookup"><span data-stu-id="8ecaa-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="8ecaa-135">Veljið **Nýr** til að hefja leiðsagnarforritið **Skrifa gagnagrunnsbreytingar í kladda**.</span><span class="sxs-lookup"><span data-stu-id="8ecaa-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="8ecaa-136">Leiðsagnarforritinu er síðan fylgt til loka.</span><span class="sxs-lookup"><span data-stu-id="8ecaa-136">Complete the wizard.</span></span>

## <a name="clean-up-database-logs"></a><span data-ttu-id="8ecaa-137">Hreinsa upp gagnagrunnsskrár</span><span class="sxs-lookup"><span data-stu-id="8ecaa-137">Clean up database logs</span></span>

<span data-ttu-id="8ecaa-138">Hægt er að eyða öllum eða hluta af gagnagrunnsklöddunum með því að nota eftirfarandi valkosti:</span><span class="sxs-lookup"><span data-stu-id="8ecaa-138">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="8ecaa-139">Veljið alla kladda fyrir tiltekna töflu.</span><span class="sxs-lookup"><span data-stu-id="8ecaa-139">Select all logs for a particular table.</span></span>
- <span data-ttu-id="8ecaa-140">Veljið tiltekna gerð af gagnagrunnskladda.</span><span class="sxs-lookup"><span data-stu-id="8ecaa-140">Select specific types of database log.</span></span>
- <span data-ttu-id="8ecaa-141">Veljið dagsetningu og tíma sem kladdi var stofnaður á.</span><span class="sxs-lookup"><span data-stu-id="8ecaa-141">Select a date and time that a log was created.</span></span>

<span data-ttu-id="8ecaa-142">Til að setja upp hreinsun gagnagrunnskladda skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="8ecaa-142">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="8ecaa-143">Farið í **Kerfisstjórnun > Tenglar > Gagnagrunnur > Gagnagrunnskladdi**.</span><span class="sxs-lookup"><span data-stu-id="8ecaa-143">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="8ecaa-144">Veljið **Hreinsa kladda**.</span><span class="sxs-lookup"><span data-stu-id="8ecaa-144">Select **Clean up log**.</span></span>

2. <span data-ttu-id="8ecaa-145">Veljið aðferð við að velja kladda sem á að eyða með því að færa inn einn af eftirfarandi valmöguleikum:</span><span class="sxs-lookup"><span data-stu-id="8ecaa-145">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="8ecaa-146">Töflu-ID</span><span class="sxs-lookup"><span data-stu-id="8ecaa-146">Table ID</span></span>
   - <span data-ttu-id="8ecaa-147">Gerð kladda</span><span class="sxs-lookup"><span data-stu-id="8ecaa-147">Type of log</span></span>
   - <span data-ttu-id="8ecaa-148">Tími og dagsetning stofnunar</span><span class="sxs-lookup"><span data-stu-id="8ecaa-148">Created date and time</span></span>

3. <span data-ttu-id="8ecaa-149">Notið flipann **Hreinsun gagnagrunnskladda** til að ákveða hvenær keyra á hreinsunarverk kladdans.</span><span class="sxs-lookup"><span data-stu-id="8ecaa-149">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="8ecaa-150">Gagnagrunnskladdar eru í boði í 30 daga að sjálfgefnu.</span><span class="sxs-lookup"><span data-stu-id="8ecaa-150">By default, database logs are available for 30 days.</span></span>
