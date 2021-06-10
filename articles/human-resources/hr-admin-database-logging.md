---
title: Skilgreina og stjórna gagnagrunnsskráningu
description: Hægt er að rekja breytingar til taflna og reita í Dynamics 365 Human Resources með gagnagrunnsskráningu.
author: andreabichsel
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ae974436469c00a3df6fd40d9d60521a0883a917
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054813"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="a31ea-103">Skilgreina og stjórna gagnagrunnsskráningu</span><span class="sxs-lookup"><span data-stu-id="a31ea-103">Configure and manage database logging</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a31ea-104">Hægt er að rekja breytingar til taflna og reita í Dynamics 365 Human Resources með gagnagrunnsskráningu.</span><span class="sxs-lookup"><span data-stu-id="a31ea-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="a31ea-105">Þetta efnisatriði lýsir hvernig á að:</span><span class="sxs-lookup"><span data-stu-id="a31ea-105">This topic describes how to:</span></span>

- <span data-ttu-id="a31ea-106">Stjórna öryggi og afköstum fyrir skráningu gagnagrunns</span><span class="sxs-lookup"><span data-stu-id="a31ea-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="a31ea-107">Setja upp gagnagrunnsskráningu</span><span class="sxs-lookup"><span data-stu-id="a31ea-107">Set up database logging</span></span>
- <span data-ttu-id="a31ea-108">Hreinsa upp gagnagrunnsskrár</span><span class="sxs-lookup"><span data-stu-id="a31ea-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="a31ea-109">Yfirlit gagnagrunnsskráningar</span><span class="sxs-lookup"><span data-stu-id="a31ea-109">Overview of database logging</span></span>

<span data-ttu-id="a31ea-110">Skráning gagnagrunns rekur sérstakar breytingar til taflna og reita Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a31ea-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="a31ea-111">Þessar breytingar fela í sér að setja inn, uppfæra eða eyða.</span><span class="sxs-lookup"><span data-stu-id="a31ea-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="a31ea-112">Gagnagrunnsskráning geymir færslur yfir breytingar á töflum í töflu gagnagrunnsskráar.</span><span class="sxs-lookup"><span data-stu-id="a31ea-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="a31ea-113">Notkun fyrirtækis á gagnagrunnsskráningu felur í sér:</span><span class="sxs-lookup"><span data-stu-id="a31ea-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="a31ea-114">Að búa til eftirlitsfærslu yfir breytinga á tilteknum töflum sem innihalda viðkvæmar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="a31ea-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="a31ea-115">Rakning einstakra færslna.</span><span class="sxs-lookup"><span data-stu-id="a31ea-115">Tracking single transactions.</span></span> <span data-ttu-id="a31ea-116">Gagnagrunnsskráning er ekki ætluð til þess að rekja sjálfvirkar færslur sem eru keyrðar í runuvinnslum.</span><span class="sxs-lookup"><span data-stu-id="a31ea-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="a31ea-117">Öryggi fyrir gagnagrunnsskráningu</span><span class="sxs-lookup"><span data-stu-id="a31ea-117">Security for database logging</span></span>

<span data-ttu-id="a31ea-118">Gagnagrunnskladdar geta innihaldið viðkvæm gögn.</span><span class="sxs-lookup"><span data-stu-id="a31ea-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="a31ea-119">Takmarkið aðgang til að hafa aðeins öryggishlutverk sem þurfa aðgang að skráningargögnum.</span><span class="sxs-lookup"><span data-stu-id="a31ea-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="a31ea-120">Gagnagrunnsskráning og afköst</span><span class="sxs-lookup"><span data-stu-id="a31ea-120">Database logging and performance</span></span>

<span data-ttu-id="a31ea-121">Þótt þetta sé mikilvægt fyrir fyrirtækið, getur gagnagrunnsskráning verið dýr í notkun á tilföngum og stjórnun.</span><span class="sxs-lookup"><span data-stu-id="a31ea-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="a31ea-122">Afköst vegna gagnagrunnsskráningar fela í sér:</span><span class="sxs-lookup"><span data-stu-id="a31ea-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="a31ea-123">Tafla gagnagrunnsskráar getur vaxið hratt og leitt til stækkunar á gagnagrunninum.</span><span class="sxs-lookup"><span data-stu-id="a31ea-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="a31ea-124">Vöxtur veltur á magni skráðra gagna sem þú ákveður að geyma.</span><span class="sxs-lookup"><span data-stu-id="a31ea-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="a31ea-125">Sjálfgefið er að tafla gagnagrunnsskráar haldi við aðeins 30 dögum af skráningargögnum.</span><span class="sxs-lookup"><span data-stu-id="a31ea-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="a31ea-126">Gagnagrunnsskráning getur haft neikvæð áhrif á sjálfvirk langtímaferli, t.d. langtíma gagnainnflutning.</span><span class="sxs-lookup"><span data-stu-id="a31ea-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="a31ea-127">Bestu venjur</span><span class="sxs-lookup"><span data-stu-id="a31ea-127">Best practices</span></span>

<span data-ttu-id="a31ea-128">Til að bæta afköst skal takmarka færslur skráar með því að velja tiltekna reiti til að skrá í stað heilla taflna.</span><span class="sxs-lookup"><span data-stu-id="a31ea-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="a31ea-129">Til að stuðla að betri heildarafköstum takmarkast gagnagrunnsskráningar við 20 töflur.</span><span class="sxs-lookup"><span data-stu-id="a31ea-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="a31ea-130">Aðeins er hægt að skrá uppfærslur fyrir einstaka reiti.</span><span class="sxs-lookup"><span data-stu-id="a31ea-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="a31ea-131">Setja upp gagnagrunnsskráningu</span><span class="sxs-lookup"><span data-stu-id="a31ea-131">Set up database logging</span></span>

<span data-ttu-id="a31ea-132">Hægt er að nota leiðsagnarforritið **Skrifa gagnagrunnsbreytingar í kladda** til að setja upp gagnagrunnsskráningu.</span><span class="sxs-lookup"><span data-stu-id="a31ea-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="a31ea-133">Leiðsagnarforritið býður upp á sveigjanlega leið til að setja upp kladdaskráningu fyrir töflur og reiti.</span><span class="sxs-lookup"><span data-stu-id="a31ea-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="a31ea-134">Farið í **Kerfisstjórnun > Tenglar > Gagnagrunnur > Uppsetning gagnagrunnskladda**.</span><span class="sxs-lookup"><span data-stu-id="a31ea-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="a31ea-135">Veljið **Nýr** til að hefja leiðsagnarforritið **Skrifa gagnagrunnsbreytingar í kladda**.</span><span class="sxs-lookup"><span data-stu-id="a31ea-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="a31ea-136">Veljið **Næst**.</span><span class="sxs-lookup"><span data-stu-id="a31ea-136">Select **Next**.</span></span> 
3. <span data-ttu-id="a31ea-137">Á síðunni **Töflur og svæði** í leiðsagnarforritinu skal velja töflurnar og reitina sem á að virkja gagnagrunnsinnskráningu fyrir og velja **Áfram**.</span><span class="sxs-lookup"><span data-stu-id="a31ea-137">On the **Tables and fields** page of the wizard, select the the tables and fields on which you want to enable database logging, and select **Next**.</span></span>

   > [!Note]
   > <span data-ttu-id="a31ea-138">Gagnagrunnsskráning er ekki tiltæk í öllum töflum í gagnagrunni mannauðs.</span><span class="sxs-lookup"><span data-stu-id="a31ea-138">Database logging is not available on all tables in the Human Resources database.</span></span> <span data-ttu-id="a31ea-139">Með því að velja **Sýna allar töflur** fyrir neðan listann stækkar listinn yfir töflur og reiti og sýnir allar gagnagrunnstöflur þar sem gagnagrunnsinnskráning er í boði, en þetta verður undirmengi á heildarlistanum yfir gagnagrunnstöflur.</span><span class="sxs-lookup"><span data-stu-id="a31ea-139">Selecting **Show all tables** below the list expands the list of tables and fields to show all database tables for which database logging is available, but this will be a subset of the full list of database tables.</span></span>

4. <span data-ttu-id="a31ea-140">Á **Gerðir breytinga** síðu leiðsagnarforritsins skal velja gagnaaðgerðirnar sem eigia að rekja breytingar fyrir hverja töflu og reiti og velja **Áfram**.</span><span class="sxs-lookup"><span data-stu-id="a31ea-140">On the **Types of change** page of the wizard, select the data operations for which you want to track changes for each of the tables and fields, and select **Next**.</span></span> <span data-ttu-id="a31ea-141">Sjá töfluna hér fyrir neðan fyrir lýsingu á gagnavirkni sem eru í boði fyrir skráningu.</span><span class="sxs-lookup"><span data-stu-id="a31ea-141">See the table below for a description of the data operations that are available for logging.</span></span>
5. <span data-ttu-id="a31ea-142">Á síðunni **Ljúka** skal fara yfir breytingarnar sem verða gerðar og velja **Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="a31ea-142">On the **Finish** page, review the changes that will be made, and select **Finish**.</span></span>

| <span data-ttu-id="a31ea-143">Aðgerð</span><span class="sxs-lookup"><span data-stu-id="a31ea-143">Operation</span></span> | <span data-ttu-id="a31ea-144">lýsing</span><span class="sxs-lookup"><span data-stu-id="a31ea-144">Description</span></span> |
| -- | -- |
| <span data-ttu-id="a31ea-145">Rekja nýjar færslur</span><span class="sxs-lookup"><span data-stu-id="a31ea-145">Track new transactions</span></span> | <span data-ttu-id="a31ea-146">Búa til kladda fyrir nýjar færslur sem eru búnar til í töflunni.</span><span class="sxs-lookup"><span data-stu-id="a31ea-146">Create a log for new records that are created in the table.</span></span> |
| <span data-ttu-id="a31ea-147">Update</span><span class="sxs-lookup"><span data-stu-id="a31ea-147">Update</span></span> | <span data-ttu-id="a31ea-148">Búa til kladda fyrir uppfærslur á töflufærslum eða uppfærslur á hvern sérvalinn reit í töflunni.</span><span class="sxs-lookup"><span data-stu-id="a31ea-148">Create a log for updates to table records, or updates to individually selected fields in the table.</span></span> <span data-ttu-id="a31ea-149">Ef valið er að skrá uppfærslur fyrir töfluna er kladdafærsla búin til í hvert skipti sem verið er að uppfæra hvaða reit sem er í hvaða færslu sem er í töflunni.</span><span class="sxs-lookup"><span data-stu-id="a31ea-149">If you select to log updates for the table, then a log record is created each time an update is made to any field of any record on the table.</span></span> <span data-ttu-id="a31ea-150">Ef valið er að skrá uppfærslur fyrir tiltekna reiti er kladdafærsla aðeins búin til þegar uppfærslur eru gerðar á þessum reitum í töflufærslum.</span><span class="sxs-lookup"><span data-stu-id="a31ea-150">If you select to log updates for specific fields, then a log record is created only when updates are made to those fields of table records.</span></span> |
| <span data-ttu-id="a31ea-151">Eyða</span><span class="sxs-lookup"><span data-stu-id="a31ea-151">Delete</span></span> | <span data-ttu-id="a31ea-152">Búa til kladda fyrir færslur sem er eytt úr töflunni.</span><span class="sxs-lookup"><span data-stu-id="a31ea-152">Create a log for records deleted from the table.</span></span> |
| <span data-ttu-id="a31ea-153">Endurnefna lykil</span><span class="sxs-lookup"><span data-stu-id="a31ea-153">Rename key</span></span> | <span data-ttu-id="a31ea-154">Búa til annálafærslu þegar töflulykill er endurnefndur.</span><span class="sxs-lookup"><span data-stu-id="a31ea-154">Create a log record when a table key is renamed.</span></span> |


## <a name="clean-up-database-logs"></a><span data-ttu-id="a31ea-155">Hreinsa upp gagnagrunnsskrár</span><span class="sxs-lookup"><span data-stu-id="a31ea-155">Clean up database logs</span></span>

<span data-ttu-id="a31ea-156">Hægt er að eyða öllum eða hluta af gagnagrunnsklöddunum með því að nota eftirfarandi valkosti:</span><span class="sxs-lookup"><span data-stu-id="a31ea-156">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="a31ea-157">Veljið alla kladda fyrir tiltekna töflu.</span><span class="sxs-lookup"><span data-stu-id="a31ea-157">Select all logs for a particular table.</span></span>
- <span data-ttu-id="a31ea-158">Veljið tiltekna gerð af gagnagrunnskladda.</span><span class="sxs-lookup"><span data-stu-id="a31ea-158">Select specific types of database log.</span></span>
- <span data-ttu-id="a31ea-159">Veljið dagsetningu og tíma sem kladdi var stofnaður á.</span><span class="sxs-lookup"><span data-stu-id="a31ea-159">Select a date and time that a log was created.</span></span>

<span data-ttu-id="a31ea-160">Til að setja upp hreinsun gagnagrunnskladda skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="a31ea-160">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="a31ea-161">Farið í **Kerfisstjórnun > Tenglar > Gagnagrunnur > Gagnagrunnskladdi**.</span><span class="sxs-lookup"><span data-stu-id="a31ea-161">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="a31ea-162">Veljið **Hreinsa kladda**.</span><span class="sxs-lookup"><span data-stu-id="a31ea-162">Select **Clean up log**.</span></span>

2. <span data-ttu-id="a31ea-163">Veljið aðferð við að velja kladda sem á að eyða með því að færa inn einn af eftirfarandi valmöguleikum:</span><span class="sxs-lookup"><span data-stu-id="a31ea-163">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="a31ea-164">Töflu-ID</span><span class="sxs-lookup"><span data-stu-id="a31ea-164">Table ID</span></span>
   - <span data-ttu-id="a31ea-165">Gerð kladda</span><span class="sxs-lookup"><span data-stu-id="a31ea-165">Type of log</span></span>
   - <span data-ttu-id="a31ea-166">Tími og dagsetning stofnunar</span><span class="sxs-lookup"><span data-stu-id="a31ea-166">Created date and time</span></span>

3. <span data-ttu-id="a31ea-167">Notið flipann **Hreinsun gagnagrunnskladda** til að ákveða hvenær keyra á hreinsunarverk kladdans.</span><span class="sxs-lookup"><span data-stu-id="a31ea-167">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="a31ea-168">Gagnagrunnskladdar eru í boði í 30 daga að sjálfgefnu.</span><span class="sxs-lookup"><span data-stu-id="a31ea-168">By default, database logs are available for 30 days.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
