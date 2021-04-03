---
title: Safnvista birgðafærslur
description: Þetta efnisatriði lýsir því hvernig á að safnvista birgðafærslugögn til að hjálpa við að auka afköst kerfisins.
author: sherry-zheng
manager: tfehr
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 3a0fa65eb728e4ce96bdfc3f7a0f04901551ccea
ms.sourcegitcommit: 70b1567d316f19c15a4b032b4897f15c8dcdca09
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2021
ms.locfileid: "5556425"
---
# <a name="archive-inventory-transactions"></a><span data-ttu-id="3e700-103">Safnvista birgðafærslur</span><span class="sxs-lookup"><span data-stu-id="3e700-103">Archive inventory transactions</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="3e700-104">Með tímanum mun birgðafærslutaflan (`InventTrans`) vaxa og nota meira pláss í gagnagrunni.</span><span class="sxs-lookup"><span data-stu-id="3e700-104">Over time, the inventory transactions table (`InventTrans`) will continue to grow and consume more database space.</span></span> <span data-ttu-id="3e700-105">Þess vegna verða fyrirspurnir þar sem sækja þarf upplýsingar úr töflunni smám saman hægari.</span><span class="sxs-lookup"><span data-stu-id="3e700-105">Therefore, queries that are made against the table will gradually become slower.</span></span> <span data-ttu-id="3e700-106">Þetta efnisatriði lýsir því hvernig hægt er að nota *Safnvistun á birgðafærslum* eiginleikann til að safnvista gögn um birgðafærslur til að aðstoða við að auka afköst kerfisins.</span><span class="sxs-lookup"><span data-stu-id="3e700-106">This topic describes how you can use the *Inventory transactions archive* feature to archive data about inventory transactions to help improve system performance.</span></span>

> [!NOTE]
> <span data-ttu-id="3e700-107">Aðeins er hægt að safnvista fjárhagslega uppfærðum birgðafærslum á völdu lokuðu fjárhagstímabili.</span><span class="sxs-lookup"><span data-stu-id="3e700-107">Only financially updated inventory transactions can be archived in a selected closed ledger period.</span></span> <span data-ttu-id="3e700-108">Til að vera safnvistað verða fjárhagslega uppfærðar birgðafærslur að vera með úthreyfingarstöðuna *Selt* og birgðafærslur á innleið verða að vera með nnhreyfingarstöðuna *Keypt*.</span><span class="sxs-lookup"><span data-stu-id="3e700-108">To be archived, financially updated outbound inventory transactions must have an issue status of *Sold*, and inbound inventory transactions must have a receipt status of *Purchased*.</span></span>

<span data-ttu-id="3e700-109">Þegar birgðafærslur eru safnvistaðar eru allar tengdar færslur færðar í `InventTransArchive`-töfluna.</span><span class="sxs-lookup"><span data-stu-id="3e700-109">When you archive inventory transactions, all related transactions are moved to the `InventTransArchive` table.</span></span> <span data-ttu-id="3e700-110">Úthreyfingarfærslur birgða og færslur á innhreyfingarskjali eru safnvistaðar sérstaklega, samkvæmt samsetningu vörukennisins (`itemId`) og birgðavíddaauðkenninu (`inventDimId`), og þær eru settar í samantektarfærslur og samanteknar innhreyfingarhreyfingar.</span><span class="sxs-lookup"><span data-stu-id="3e700-110">Inventory issue transactions and inventory receipt transactions are archived separately, based on the combination of the item ID (`itemId`) and inventory dimension ID (`inventDimId`), and they are put into the summarized issue and summarized receipt transactions.</span></span>

<span data-ttu-id="3e700-111">Ef `itemId` `inventDimId` samsetningin inniheldur aðeins eina kvittun eða úthreyfingafærslu, verður færslan ekki safnvistuð.</span><span class="sxs-lookup"><span data-stu-id="3e700-111">If an `itemId` and `inventDimId` combination contains only one receipt or issue transaction, the transaction won't be archived.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="3e700-112">Kveikja á eiginleikanum í kerfinu</span><span class="sxs-lookup"><span data-stu-id="3e700-112">Turn on the feature in your system</span></span>

<span data-ttu-id="3e700-113">Ef kerfið inniheldur ekki eiginleikana sem lýst er í þessu efnisatriði skal fara í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og kveikja á eiginleikanum *Safnvistun á birgðafærslum*.</span><span class="sxs-lookup"><span data-stu-id="3e700-113">If your system doesn't already include the features that is described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Inventory transactions archive* feature.</span></span>

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a><span data-ttu-id="3e700-114">Það sem þarf að hafa í huga áður en birgðafærslur eru safnvistaðar</span><span class="sxs-lookup"><span data-stu-id="3e700-114">Things to consider before you archive inventory transactions</span></span>

<span data-ttu-id="3e700-115">Áður en birgðafærslur eru safnvistaðar ætti að hafa í huga eftirfarandi viðskiptaaðstæður vegna þess að þær verða fyrir áhrifum af aðgerðinni:</span><span class="sxs-lookup"><span data-stu-id="3e700-115">Before you archive inventory transactions, you should consider the following business scenarios, because they will be affected by the operation:</span></span>

- <span data-ttu-id="3e700-116">Við endurskoðun á birgðafærslum úr tengdum skjölum, svo sem innkaupapöntunarlínum, birtast færslurnar sem safnvistaðar.</span><span class="sxs-lookup"><span data-stu-id="3e700-116">When you audit inventory transactions from related documents, such as purchase order lines, they will be shown as archived.</span></span> <span data-ttu-id="3e700-117">Til að yfirfara safnvistaðar færslur þarf að fara í **Birgðastjórnun \> Reglubundin verk \> Hreinsun \> Safnvistun á birgðafærslum**.</span><span class="sxs-lookup"><span data-stu-id="3e700-117">To review the archived transactions, you must go to **Inventory management \> Periodic tasks \> Clean up \> Inventory transactions archive**.</span></span>
- <span data-ttu-id="3e700-118">Ekki er hægt að hætta við birgðalokun fyrir safnvistuð tímabil.</span><span class="sxs-lookup"><span data-stu-id="3e700-118">Inventory closing can't be canceled for archived periods.</span></span> <span data-ttu-id="3e700-119">Áður en hægt er að hætta við birgðalokun verður að bakfæra birgðafærslusafnið fyrir viðkomandi tímabil.</span><span class="sxs-lookup"><span data-stu-id="3e700-119">Before you can cancel an inventory closing, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="3e700-120">Ekki er hægt að umreikna staðalkostnað fyrir safnvistuð tímabil.</span><span class="sxs-lookup"><span data-stu-id="3e700-120">Standard cost conversion can't be done for archived periods.</span></span> <span data-ttu-id="3e700-121">Áður en hægt er að umreikna staðalkostnað verður að bakfæra birgðafærslusafnið fyrir viðkomandi tímabil.</span><span class="sxs-lookup"><span data-stu-id="3e700-121">Before you can do standard cost conversion, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="3e700-122">Safnvistun hefur áhrif á birgðaskýrslur sem eru færðar úr birgðafærslum.</span><span class="sxs-lookup"><span data-stu-id="3e700-122">Inventory reports that are sourced from inventory transactions will be affected when you archive inventory transactions.</span></span> <span data-ttu-id="3e700-123">Þessar skýrslur innihalda aldursgreiningarskýrslu birgða og birgðavirðisskýrslur.</span><span class="sxs-lookup"><span data-stu-id="3e700-123">These reports include the inventory aging report and inventory value reports.</span></span>
- <span data-ttu-id="3e700-124">Þetta kann að hafa áhrif á birgðaspár ef þær eru keyrðar meðan hámarkstími safnvistaðar tímabila er í gangi.</span><span class="sxs-lookup"><span data-stu-id="3e700-124">Inventory forecasts might be affected if they are run during the time horizon of archived periods.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3e700-125">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="3e700-125">Prerequisites</span></span>

<span data-ttu-id="3e700-126">Aðeins er hægt að safnvista birgðafærslur á tímabilum þar sem eftirfarandi skilyrði eru uppfyllt:</span><span class="sxs-lookup"><span data-stu-id="3e700-126">Inventory transactions can be archived only during periods where the following conditions are met:</span></span>

- <span data-ttu-id="3e700-127">Fjárhagstímabilið verður að vera lokað.</span><span class="sxs-lookup"><span data-stu-id="3e700-127">The ledger period must be closed.</span></span>
- <span data-ttu-id="3e700-128">Keyra verður birgðalokun á eða eftir lokatímabils safnsins.</span><span class="sxs-lookup"><span data-stu-id="3e700-128">Inventory closing must be run on or after the to-period date of the archive.</span></span>
- <span data-ttu-id="3e700-129">Tímabilið verður að vera að minnsta kosti einu ári frá upphafsdagsetningu safnsins.</span><span class="sxs-lookup"><span data-stu-id="3e700-129">The period must be at least one year before the from-period date of the archive.</span></span>
- <span data-ttu-id="3e700-130">Engir endurútreikningar birgða mega vera til staðar.</span><span class="sxs-lookup"><span data-stu-id="3e700-130">There must not be any existing inventory recalculations.</span></span>

## <a name="archive-inventory-transactions"></a><span data-ttu-id="3e700-131">Safnvista birgðafærslur</span><span class="sxs-lookup"><span data-stu-id="3e700-131">Archive inventory transactions</span></span>

<span data-ttu-id="3e700-132">Fylgið eftirfarandi skrefum til að halda áfram að safnvista birgðafærslur.</span><span class="sxs-lookup"><span data-stu-id="3e700-132">To archive inventory transactions, follow these steps.</span></span>

1. <span data-ttu-id="3e700-133">Farið í **Birgðastjórnun** \> **Reglubundin verk** \> **Hreinsun** \> **Safnvistun á birgðafærslum**.</span><span class="sxs-lookup"><span data-stu-id="3e700-133">Go to **Inventory management** \> **Periodic tasks** \> **Clean up** \> **Inventory transaction archive**.</span></span>

    <span data-ttu-id="3e700-134">Síðan **Safnvistun á birgðafærslum** birtist og sýnir lista yfir eldri safnferlisfærslur.</span><span class="sxs-lookup"><span data-stu-id="3e700-134">The **Inventory transactions archive** page appears and shows a list of archived process records.</span></span>

    <span data-ttu-id="3e700-135">![Safnvistunarsíða birgðafærslna](media/archive-inventory-empty.png "Safnvistunarsíða birgðafærslna")</span><span class="sxs-lookup"><span data-stu-id="3e700-135">![Inventory transactions archive page](media/archive-inventory-empty.png "Inventory transactions archive page")</span></span>

1. <span data-ttu-id="3e700-136">Í aðgerðasvæði skal velja **Safnvistun á birgðafærslum** til að safnvista birgðafærslur.</span><span class="sxs-lookup"><span data-stu-id="3e700-136">On the Action Pane, select **Inventory transactions archive** to create an inventory transaction archive.</span></span>
1. <span data-ttu-id="3e700-137">Í svarglugganum **Safnvistun á birgðafærslum** á **Færibreytur** flýtiflipanum, skal stilla eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="3e700-137">In the **Inventory transactions archive** dialog box, on the **Parameters** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="3e700-138">**Upphafsdagsetning í lokuðu fjárhagstímabili** – Veljið fyrstu dagsetningu færslu sem á að taka með í safninu.</span><span class="sxs-lookup"><span data-stu-id="3e700-138">**From date in closed ledger period** – Select the earliest transaction date to include in the archive.</span></span>
    - <span data-ttu-id="3e700-139">**Lokadagsetning í lokuðu fjárhagstímabili** – Veljið síðustu dagsetningu færslu sem á að taka með í safninu.</span><span class="sxs-lookup"><span data-stu-id="3e700-139">**To date in closed ledger period** – Select the latest transaction date to include in the archive.</span></span>

    <span data-ttu-id="3e700-140">![Svargluggi safnvistunar á birgðafærslum](media/archive-inventory-dates.png "Svargluggi safnvistunar á birgðafærslum")</span><span class="sxs-lookup"><span data-stu-id="3e700-140">![Inventory transactions archive dialog box](media/archive-inventory-dates.png "Inventory transactions archive dialog box")</span></span>

    > [!NOTE]
    > <span data-ttu-id="3e700-141">Aðeins er hægt að velja tímabil sem uppfylla [Skilyrði](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="3e700-141">Only periods that meet the [prerequisites](#prerequisites) will be available for selection.</span></span>

1. <span data-ttu-id="3e700-142">Í flýtiflipanum **Keyra í bakgrunni** skal stilla upplýsingar runuvinnslu eins og þörf er á.</span><span class="sxs-lookup"><span data-stu-id="3e700-142">On the **Run in the background** FastTab, set up batch processing details as you require.</span></span> <span data-ttu-id="3e700-143">Fylgið venjulegum skrefum fyrir runuvinnslur í Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3e700-143">Follow the usual steps for batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="3e700-144">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="3e700-144">Select **OK**.</span></span>
1. <span data-ttu-id="3e700-145">Þú færð skilaboð þar sem þú þarft að staðfesta á að þú viljir halda áfram.</span><span class="sxs-lookup"><span data-stu-id="3e700-145">You receive a message that prompts you to confirm that you want to continue.</span></span> <span data-ttu-id="3e700-146">Lestu skilaboðin vandlega og veldu svo **Já** ef þú vilt halda áfram.</span><span class="sxs-lookup"><span data-stu-id="3e700-146">Read the message carefully, and then select **Yes** if you want to continue.</span></span>

    <span data-ttu-id="3e700-147">Þú færð skilaboð sem segja til um að safnvistun birgðafærsla hafi verið bætt við runubiðröðina.</span><span class="sxs-lookup"><span data-stu-id="3e700-147">You receive a message that states that your inventory transactions archive job has been added to the batch queue.</span></span> <span data-ttu-id="3e700-148">Vinnslan hefur nú safnvistun birgðafærsla á völdu tímabili.</span><span class="sxs-lookup"><span data-stu-id="3e700-148">The job will now start to archive inventory transactions from the selected period.</span></span>

## <a name="view-archived-inventory-transactions"></a><span data-ttu-id="3e700-149">Skoða safnvistaðar birgðafærslur</span><span class="sxs-lookup"><span data-stu-id="3e700-149">View archived inventory transactions</span></span>

<span data-ttu-id="3e700-150">**Safnvistun á birgðafærslum** sýnir allan safnvistunarferil þinn.</span><span class="sxs-lookup"><span data-stu-id="3e700-150">The **Inventory transactions archive** page shows your full archiving history.</span></span> <span data-ttu-id="3e700-151">Hver lína í hnitanetinu sýnir upplýsingar á borð við dagsetninguna þegar safnið var búið til, notandann sem stofnaði það og stöðu þess.</span><span class="sxs-lookup"><span data-stu-id="3e700-151">Each row in the grid shows information such as the date when the archive was created, the user who created it, and its status.</span></span>

<span data-ttu-id="3e700-152">![Safnvistunarferill á síðunni Safnvistun á birgðafærslum](media/archive-inventory-full.png "Safnvistunarferill á síðunni Safnvistun á birgðafærslum")</span><span class="sxs-lookup"><span data-stu-id="3e700-152">![Archiving history on the Inventory transactions archive page](media/archive-inventory-full.png "Archiving history on the Inventory transactions archive page")</span></span>

<span data-ttu-id="3e700-153">Í fellilistanum efst á síðunni skal velja eitt af eftirfarandi gildum til að sía safnvistanir sem eru sýndar í hnitanetinu:</span><span class="sxs-lookup"><span data-stu-id="3e700-153">In the drop-down list at the top of the page select one of the following values to filter the archives that are shown in the grid:</span></span>

- <span data-ttu-id="3e700-154">**Virkur** – Sýna aðeins virk söfn, ekki bakfærð söfn.</span><span class="sxs-lookup"><span data-stu-id="3e700-154">**Active** – Show only active archives, not reversed archives.</span></span>
- <span data-ttu-id="3e700-155">**Allt** – Sýna öll söfn, bæði virk og bakfærð.</span><span class="sxs-lookup"><span data-stu-id="3e700-155">**All** – Show all archives, both active and reversed.</span></span>

<span data-ttu-id="3e700-156">Fyrir hvert safn í hnitanetinu eru eftirfarandi upplýsingar veittar:</span><span class="sxs-lookup"><span data-stu-id="3e700-156">For each archive in the grid, the following information is provided:</span></span>

- <span data-ttu-id="3e700-157">**Virkt** – Gátmerki sýnir að safnið sé virkt.</span><span class="sxs-lookup"><span data-stu-id="3e700-157">**Active** – A check mark indicates that the archive is active.</span></span>
- <span data-ttu-id="3e700-158">**Dagsetning frá** – Dagsetning elstu færslunnar sem hægt er að taka með í safninu.</span><span class="sxs-lookup"><span data-stu-id="3e700-158">**From date** – The date of the oldest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="3e700-159">**Til dagsetningar** – Dagsetning nýjustu færslunnar sem hægt er að taka með í safninu.</span><span class="sxs-lookup"><span data-stu-id="3e700-159">**To date** – The date of the latest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="3e700-160">**Áætlað af** – Notandareikningurinn sem stofnaði safnið.</span><span class="sxs-lookup"><span data-stu-id="3e700-160">**Scheduled by** – The user account that created the archive.</span></span>
- <span data-ttu-id="3e700-161">**Keyrt** – Dagsetningin þegar safnið var stofnað.</span><span class="sxs-lookup"><span data-stu-id="3e700-161">**Executed** – The date when the archive was created.</span></span>
- <span data-ttu-id="3e700-162">**Bakfæra** – Gátmerki gefur til kynna að safnið hafi verið bakfært.</span><span class="sxs-lookup"><span data-stu-id="3e700-162">**Reverse** – A check mark indicates that the archive has been reversed.</span></span>
- <span data-ttu-id="3e700-163">**Stöðva gildandi uppfærslu** – Gátmerki gefur til kynna að safnið sé í vinnslu en að hlé hafi verið gert á henni.</span><span class="sxs-lookup"><span data-stu-id="3e700-163">**Stop current update** – A check mark indicates that the archive is in progress, but it has been paused.</span></span>
- <span data-ttu-id="3e700-164">**Staða** – Staða safnsins.</span><span class="sxs-lookup"><span data-stu-id="3e700-164">**State** – The processing status of the archive.</span></span> <span data-ttu-id="3e700-165">Möguleg gildi eru *Í bið*, *Í vinnslu* og *Lokið*.</span><span class="sxs-lookup"><span data-stu-id="3e700-165">The possible values are *Waiting*, *In progress*, and *Finished*.</span></span>

<span data-ttu-id="3e700-166">Tækjastikan fyrir ofan hnitanetið býður upp á eftirfarandi hnappa sem hægt er að nota til að vinna með valda safnvistun:</span><span class="sxs-lookup"><span data-stu-id="3e700-166">The toolbar above the grid provides the following buttons that you can use to work with a selected archive:</span></span>

- <span data-ttu-id="3e700-167">**Safnvistaðar færslur** – Skoða allar upplýsingar um valið safn.</span><span class="sxs-lookup"><span data-stu-id="3e700-167">**Archived transactions** – View the full details of the selected archive.</span></span> <span data-ttu-id="3e700-168">Síðan **Safnvistaðar færslur** sem birtist sýnir allar færslurnar í safninu.</span><span class="sxs-lookup"><span data-stu-id="3e700-168">The **Archived transactions** page that appears shows all the transactions in the archive.</span></span>

    <span data-ttu-id="3e700-169">![Síða safnvistaðra færslna](media/archive-inventory-transactions.png "Síða safnvistaðra færslna")</span><span class="sxs-lookup"><span data-stu-id="3e700-169">![Archived transactions page](media/archive-inventory-transactions.png "Archived transactions page")</span></span>

    <span data-ttu-id="3e700-170">Til að skoða frekari upplýsingar um tiltekna færslu á síðunni **Safnvistaðar færslur** skal velja hana í hnitanetinu og síðan á aðgerðasvæðinu skal velja **Upplýsingar um safnvistaða færslu**.</span><span class="sxs-lookup"><span data-stu-id="3e700-170">To view more information about a specific transaction on the **Archived transactions** page, select it in the grid, and then, on the Action Pane, select **Archived transaction details**.</span></span> <span data-ttu-id="3e700-171">Síðan **Upplýsingar um safnvistaða færslu** sem birtist sýnir upplýsingar á borð við fjárhagsbókun, tengdar tilvísanir undirbókar og fjárhagsvíddir.</span><span class="sxs-lookup"><span data-stu-id="3e700-171">The **Archived transaction details** page that appears shows information such as the ledger posting, related subledger references, and financial dimensions.</span></span>

- <span data-ttu-id="3e700-172">**Gera hlé á safnvistun** – Gera hlé á valdri safnvistun sem er verið að vinna úr.</span><span class="sxs-lookup"><span data-stu-id="3e700-172">**Pause archiving** – Pause a selected archive that is currently being processed.</span></span> <span data-ttu-id="3e700-173">Aðeins er gert hlé eftir að safnvistunarverk hefur verið myndað.</span><span class="sxs-lookup"><span data-stu-id="3e700-173">The pause takes effect only after the archiving task has been generated.</span></span> <span data-ttu-id="3e700-174">Þess vegna gæti liðið stuttur tíma áður en hlé er gert.</span><span class="sxs-lookup"><span data-stu-id="3e700-174">Therefore, there might be a short delay before the pause takes effect.</span></span> <span data-ttu-id="3e700-175">Þegar búið er að gera hlé birtist gátmerki í reitnum **Stöðva gildandi uppfærslu**.</span><span class="sxs-lookup"><span data-stu-id="3e700-175">If an archive has been paused, a check mark appears in its **Stop current update** field.</span></span>
- <span data-ttu-id="3e700-176">**Halda áfram safnvistun** – Halda áfram safnvistun fyrir valda safnvistun sem gert var hlé á.</span><span class="sxs-lookup"><span data-stu-id="3e700-176">**Resume archiving** – Resume processing for a selected archive that is currently paused.</span></span>
- <span data-ttu-id="3e700-177">**Bakfæra** – Bakfæra valið safn.</span><span class="sxs-lookup"><span data-stu-id="3e700-177">**Reverse** – Reverse the selected archive.</span></span> <span data-ttu-id="3e700-178">Aðeins er hægt að bakfæra safn ef **Staða** þess er stillt á *Lokið*.</span><span class="sxs-lookup"><span data-stu-id="3e700-178">You can reverse an archive only if its **State** field is set to *Finished*.</span></span> <span data-ttu-id="3e700-179">Ef safn hefur verið bakfært birtist gátmerki í reitnum **Bakfæra**.</span><span class="sxs-lookup"><span data-stu-id="3e700-179">If an archive has been reversed, a check mark appears in its **Reverse** field.</span></span>
