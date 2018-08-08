---
title: "Yfirlit yfir uppfærslu afskriftarbókar"
description: "Í eldri útgáfum, voru tvö matshugtök fyrir eignir -  virðislíkön og afskriftabækur. Í Microsoft Dynamics 365 for Operations (1611) er aðgerðin virðislíkön og afskriftarbókar sameinaðar í eitt hugtak sem kallast bók. Þetta efnisatriði gefur einhverjar eftirfarandi gott að hafa í huga fyrir uppfærslu."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 805f6ab1cd1d0996e685278cc997f532213c76c3
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---

# <a name="depreciation-book-upgrade-overview"></a><span data-ttu-id="827cb-105">Yfirlit yfir uppfærslu afskriftarbókar</span><span class="sxs-lookup"><span data-stu-id="827cb-105">Depreciation book upgrade overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="827cb-106">Í eldri útgáfum, voru tvö matshugtök fyrir eignir -  virðislíkön og afskriftabækur.</span><span class="sxs-lookup"><span data-stu-id="827cb-106">In previous releases, there were two valuation concepts for fixed assets -  value models and depreciation books.</span></span> <span data-ttu-id="827cb-107">Í Microsoft Dynamics 365 for Operations (1611) er aðgerðin virðislíkön og afskriftarbókar sameinaðar í eitt hugtak sem kallast bók.</span><span class="sxs-lookup"><span data-stu-id="827cb-107">In Microsoft Dynamics 365 for Operations (1611), the value model functionality and depreciation book functionality have been merged into a single concept that is known as a book.</span></span> <span data-ttu-id="827cb-108">Þetta efnisatriði gefur einhverjar eftirfarandi gott að hafa í huga fyrir uppfærslu.</span><span class="sxs-lookup"><span data-stu-id="827cb-108">This topic provides some things to consider for the upgrade.</span></span> 

<span data-ttu-id="827cb-109">Uppfærsluferlið færir fyrirliggjandi uppsetningu og allar fyrirliggjandi færslur til uppbyggingar nýju bókarinnar.</span><span class="sxs-lookup"><span data-stu-id="827cb-109">The upgrade process will move your existing setup and all existing transactions to the new book structure.</span></span> <span data-ttu-id="827cb-110">Virðislíkön haldast eins og þau eru, sem bók sem bókar í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="827cb-110">Value models will remain as they currently are, as a book that posts to the general ledger.</span></span> <span data-ttu-id="827cb-111">Afskriftabækur verða flutt í bók sem hefur **Bóka í fjárhag** valkostur stilltur á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="827cb-111">Depreciation books will be moved to a book that has the **Post to general ledger** option set to **No**.</span></span> <span data-ttu-id="827cb-112">Færslubókaheiti afskriftabóka verði flutt í færslubókarheitið fjárhags sem er með bókunarlag stillt á **Ekkert**.</span><span class="sxs-lookup"><span data-stu-id="827cb-112">Depreciation book journal names will be moved to a general ledger journal name with the posting layer set to **None**.</span></span> <span data-ttu-id="827cb-113">Færslur afskriftarbókar verða fluttar í Eignafærsla.</span><span class="sxs-lookup"><span data-stu-id="827cb-113">Depreciation book transactions will be moved to Fixed asset transactions.</span></span> 

<span data-ttu-id="827cb-114">Áður en uppfærslu gagna er keyrð, þarf að skilja kostirnir tveir sem eru tiltækar til uppfærslu færslubókarlínur afskriftarbókar í fylgiskjöl færslu, og númeraröð sem verður notað fyrir fylgiskjalarunu.</span><span class="sxs-lookup"><span data-stu-id="827cb-114">Before running the data upgrade, you should understand the two options available for upgrading depreciation book journal lines to transaction vouchers, and the number sequence that will be used for the voucher series.</span></span> 

<span data-ttu-id="827cb-115">Valkostur 1: **kerfisskilgreind númeraröð** -Þetta er sjálfgefin stilling til að besta uppfærsluframkvæmd.</span><span class="sxs-lookup"><span data-stu-id="827cb-115">Option 1:  **System-defined number sequence** - This is the default option to optimize upgrade performance.</span></span> <span data-ttu-id="827cb-116">Uppfærslu notar ekki ramma fyrir númeraraðir, en mun í staðinn úthluta fyliskjölum með samstæðubyggð nálgun.</span><span class="sxs-lookup"><span data-stu-id="827cb-116">The upgrade will not use the number sequences framework, but instead will allocate vouchers with a set-based approach.</span></span> <span data-ttu-id="827cb-117">Eftir uppfærslu, verður nýja númeraröð stofnað með **Næsta númerasetti** og byggt upp í samræmi við uppfærða færslu.</span><span class="sxs-lookup"><span data-stu-id="827cb-117">After the upgrade, the new number sequence will be created with the **Next number set** appropriately based on the upgraded transactions.</span></span> <span data-ttu-id="827cb-118">Að sjálfgefnu, verður notuð númeraröð vera á FADBUpgr\#\#\#\#\#\#\#\#\# sniði.</span><span class="sxs-lookup"><span data-stu-id="827cb-118">By default, the number sequence used will be in the FADBUpgr\#\#\#\#\#\#\#\#\# format.</span></span> <span data-ttu-id="827cb-119">Nokkrar færibreytur eru tiltækar til að leiðrétta sniðið þegar þessi nálgun er notuð:</span><span class="sxs-lookup"><span data-stu-id="827cb-119">There are a few parameters available to you to adjust the format when using this approach:</span></span>

-   <span data-ttu-id="827cb-120">**Númeraraðarkóði** – Kóði til að auðkenna númeraröð.</span><span class="sxs-lookup"><span data-stu-id="827cb-120">**Number sequence code** – The code to identify the number sequence.</span></span> <span data-ttu-id="827cb-121">Þessi númeraraðarkóða getur ekki verið til þar sem hún verður stofnuð af uppfærslunni.</span><span class="sxs-lookup"><span data-stu-id="827cb-121">This number sequence code cannot exist since it will be created by the upgrade.</span></span>
    -   <span data-ttu-id="827cb-122">Heiti fasta: **NumberSequenceDefaultCode**</span><span class="sxs-lookup"><span data-stu-id="827cb-122">Constant name: **NumberSequenceDefaultCode**</span></span>
    -   <span data-ttu-id="827cb-123">Sjálfgefið gildi: "FADBUpgr"</span><span class="sxs-lookup"><span data-stu-id="827cb-123">Default value: "FADBUpgr"</span></span>
-   <span data-ttu-id="827cb-124">**Forskeyti** – Gildi fyrir streng fasta sem verður notað sem forskeyti fyrir fylgiskjalsnúmerin.</span><span class="sxs-lookup"><span data-stu-id="827cb-124">**Prefix** – The constant string value that will be used as a prefix for the voucher numbers.</span></span>
    -   <span data-ttu-id="827cb-125">Heiti fasta: **NumberSequenceDefaultParameterPrefix**</span><span class="sxs-lookup"><span data-stu-id="827cb-125">Constant name: **NumberSequenceDefaultParameterPrefix**</span></span>
    -   <span data-ttu-id="827cb-126">Sjálfgefið gildi: "FADBUpgr"</span><span class="sxs-lookup"><span data-stu-id="827cb-126">Default value: "FADBUpgr"</span></span>
-   <span data-ttu-id="827cb-127">**Lengd bókstafa og talna** – Lengd hluta sem notar bókstafi og tölur fyrir númeraröð.</span><span class="sxs-lookup"><span data-stu-id="827cb-127">**Alphanumeric length** – The length of the alphanumeric segment of the number sequence.</span></span>
    -   <span data-ttu-id="827cb-128">Heiti fasti: **NumberSequenceDefaultParameterAlpanumericLength**</span><span class="sxs-lookup"><span data-stu-id="827cb-128">Constant name: **NumberSequenceDefaultParameterAlpanumericLength **</span></span>
    -   <span data-ttu-id="827cb-129">Sjálfgildi: 9</span><span class="sxs-lookup"><span data-stu-id="827cb-129">Default value: 9</span></span>
-   <span data-ttu-id="827cb-130">**Upphafsnúmer** - fyrsta númer sem notað er í númeraröð.</span><span class="sxs-lookup"><span data-stu-id="827cb-130">**Start number** - The first number to be used in the number sequence.</span></span>
    -   <span data-ttu-id="827cb-131">Heiti fasta: **NumberSequenceDefaultParameterStartNumber**</span><span class="sxs-lookup"><span data-stu-id="827cb-131">Constant name: **NumberSequenceDefaultParameterStartNumber  **</span></span>
    -   <span data-ttu-id="827cb-132">Sjálfgildi: 1</span><span class="sxs-lookup"><span data-stu-id="827cb-132">Default value: 1</span></span>

<span data-ttu-id="827cb-133">Möguleiki 2: **Fyrirliggjandi notandaskilgreindur númeraröð** - Þennan valkost gerir þér kleift að skilgreina númeraröðina sem nota á fyrir uppfærslu.</span><span class="sxs-lookup"><span data-stu-id="827cb-133">Option 2: **Existing user-defined number sequence** - This option will allow you to define the number sequence to be used for the upgrade.</span></span> <span data-ttu-id="827cb-134">Íhuga að nota þennan valkost ef þú þarft ítarlega skilgreiningu númeraraðar.</span><span class="sxs-lookup"><span data-stu-id="827cb-134">Consider using this option if you need advanced number sequence configuration.</span></span> <span data-ttu-id="827cb-135">Til að nota númeraröð, verður að breyta uppfærsluflokk ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans með eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="827cb-135">To use a number sequence, you must modify the upgrade class ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans with the following information:</span></span>

-   <span data-ttu-id="827cb-136">**Númeraraðarkóði** – Kóði númeraraðar.</span><span class="sxs-lookup"><span data-stu-id="827cb-136">**Number sequence code** – The code of the number sequence.</span></span>
    -   <span data-ttu-id="827cb-137">Heiti fasti: **NumberSequenceExistingCode**</span><span class="sxs-lookup"><span data-stu-id="827cb-137">Constant name: **NumberSequenceExistingCode **</span></span>
    -   <span data-ttu-id="827cb-138">Sjálfgildi: Engin sjálfgefin, þetta þarf að uppfæra fyrir númeraraðakóða.</span><span class="sxs-lookup"><span data-stu-id="827cb-138">Default value: No default, this must be updated to the number sequence code.</span></span>
-   <span data-ttu-id="827cb-139">**Samnýttar númeraröð** – boole-gildi til að greina umfang númeraraðar.</span><span class="sxs-lookup"><span data-stu-id="827cb-139">**Shared number sequence** – A boolean value to identify the scope of the number sequence.</span></span> <span data-ttu-id="827cb-140">Notuð "satt" fyrir samnýttar númeraraðir þvert á öll fyrirtæki og "rangt" fyrir sviðs sem eru sértæk fyrir fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="827cb-140">Use "true" for shared number sequences across all companies, and "false" for a company-specific scope.</span></span> <span data-ttu-id="827cb-141">Þegar "rangt" er notað, verður númeraröð með tilgreindu heiti vera til staðar í hvert fyrirtæki sem inniheldur færslur í afskriftabók.lur í afskriftabók.</span><span class="sxs-lookup"><span data-stu-id="827cb-141">When using "false", the number sequence with the specified name must exist in every company that contains depreciation book transactions.</span></span> <span data-ttu-id="827cb-142">Samnýtt númeraraðir eru til í hverri deildaskiptingu sem inniheldur færslur í afskriftarbók.</span><span class="sxs-lookup"><span data-stu-id="827cb-142">Shared number sequences exist in every partition that contains depreciation book transactions.</span></span>
    -   <span data-ttu-id="827cb-143">Heiti fasti: **NumberSequenceExistingIsShared**</span><span class="sxs-lookup"><span data-stu-id="827cb-143">Constant name: **NumberSequenceExistingIsShared **</span></span>
    -   <span data-ttu-id="827cb-144">Sjálfgefið gildi: rétt</span><span class="sxs-lookup"><span data-stu-id="827cb-144">Default value: true</span></span>

<span data-ttu-id="827cb-145">Færibreyturnar eru staðsett í upphafi ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans flokks.</span><span class="sxs-lookup"><span data-stu-id="827cb-145">The parameters are located at the beginning of the ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans class.</span></span> 

<span data-ttu-id="827cb-146">*//Skilgreindu æskilega nálgun á úthlutun fylgiskjala* 
 *//satt ef óskað er að nota fyrirliggjandi kóða númeraraðar* 
 *// rangt ef ætlunin er að nota kerfisskilgreindar númeraröð (sjálfgefið)* const boolean NumberSequenceUseExistingCode = rangt;</span><span class="sxs-lookup"><span data-stu-id="827cb-146">*// Specify a preferable approach of vouchers allocation* 
 *// true, if you want to use an existing number sequence code* 
 *// false, if you intend to use the system-defined number sequence (default)* const boolean NumberSequenceUseExistingCode = false;</span></span>  

<span data-ttu-id="827cb-147">*// Ef nota á náglun kerfisskilgreindar númeraröð skal tilgreina færibreytur fyrir númeraröð.*
 *//Nýja númeraröð verður stofnuð með þessar færibreytur.*</span><span class="sxs-lookup"><span data-stu-id="827cb-147">*// If using the system-defined number sequence approach, specify the parameters for the number sequence.*
 *// A new number sequence will be created with these parameters.*</span></span> <span data-ttu-id="827cb-148">const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;</span><span class="sxs-lookup"><span data-stu-id="827cb-148">const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;</span></span>   

<span data-ttu-id="827cb-149">*// Ef á að nota nálgunina fyrirliggjandi númeraraðakóði, skal tilgreina fyrirliggjandi kóða númeraraðar.* 
 *//Úthlutun fylgiskjals mun fara röð eftir röð fyrir núverandi númeraröð.*</span><span class="sxs-lookup"><span data-stu-id="827cb-149">*// If using the existing number sequence approach, specify the existing number sequence code.* 
 *// Voucher allocation will go row-by-row for existing number sequences.*</span></span> <span data-ttu-id="827cb-150">const str NumberSequenceExistingCode = '‘; *// Tilgreina umfang fyrirliggjandi númeraraðakóða* 
 *//satt ef tilgreind númeraröð er samnýtt* 
*rangt ef tilgreind númeraröð er á hvert fyrirtæki* 
 *//Sjálfgefna kerfisskilgreindar númeraröðinni verður notaður ef númeraraðarkóða með tilgreindu umfangi fannst ekki.*</span><span class="sxs-lookup"><span data-stu-id="827cb-150">const str NumberSequenceExistingCode = ''; *// Specify the scope of the existing number sequence code* 
 *// true, if the specified number sequence is shared* 
 *// false, if the specified number sequence is per-company* 
 *// The default system-defined number sequence will be used if a number sequence code with the specified scope is not found.*</span></span> <span data-ttu-id="827cb-151">const boolean NumberSequenceExistingIsShared = satt;</span><span class="sxs-lookup"><span data-stu-id="827cb-151">const boolean NumberSequenceExistingIsShared = true;</span></span> 

<span data-ttu-id="827cb-152">Endurbyggja verksins sem inniheldur flokkinn eftir að fastarnir hafa verið breyttir.</span><span class="sxs-lookup"><span data-stu-id="827cb-152">Rebuild the project that contains the class after the constants have been modified.</span></span> 

<span data-ttu-id="827cb-153">Þegar notast er við nálgun sem byggist á kerfisskilgreindum númeraröðum, (valkosturinn 1), mun uppfærslan nota vinnslu sem byggist á settum til að úthluta númerum fylgiskjala eins og tilgreint er í færibreytum uppfærsluforskriftar.</span><span class="sxs-lookup"><span data-stu-id="827cb-153">When using the system-generated number sequence approach (option 1), the upgrade will use set-based processing to allocate the voucher numbers as specified in the upgrade script parameters.</span></span> <span data-ttu-id="827cb-154">Hún mun einnig stofna nýja númeraröð með tilgreinda færibreytur eftir úthlutunina.</span><span class="sxs-lookup"><span data-stu-id="827cb-154">It will also create a new number sequence with specified parameters after the allocation.</span></span> 

<span data-ttu-id="827cb-155">Þegar notast er við nálgunina notendaskilgreind fyrirliggjandi númeraröð (valkostur 2) athugar gagnauppfærslan hvort númeraröðið með tilgreindu umfangi er til staðar í gagnagrunni fyrir hverja deildaskiptingu og fyrirtæki með færslum afskriftarbókar.</span><span class="sxs-lookup"><span data-stu-id="827cb-155">When using the user-defined existing number sequence approach (option 2), the data upgrade checks whether the number sequence with the specified scope exists in the database for each partition and company with depreciation book transactions.</span></span> <span data-ttu-id="827cb-156">EF það er ekki til staðar, mun uppfærslan nota röð-eftir-röð vinnslu til að úthluta númerum fylgiskjala sem tilgreind eru í númeraröðinni með því að nota ramma númeraraða.</span><span class="sxs-lookup"><span data-stu-id="827cb-156">If it does exist, the upgrade will use row-by-row processing to allocate the voucher numbers as specified by the number sequence using the number sequence framework.</span></span> <span data-ttu-id="827cb-157">Ef númeraröð er ekki til staðar með tilgreindu umfangi, mun uppfærslan nota sjálfgefna kerfisskilgreindu nálgun á númeraraðir til að úthluta númer fylgiskjals, og mun stofna nýja númeraröð með tilgreindum sjálfgefnum færibreytum eftir úthlutunina.</span><span class="sxs-lookup"><span data-stu-id="827cb-157">If the number sequence does not exist with the specified scope, the upgrade will use the default system-defined number sequence approach to allocate the voucher numbers, and will create a new number sequence with specified default parameters after the allocation.</span></span>

<span data-ttu-id="827cb-158">Með hvorri nálguninni mun uppfærsluforskrift gagna einnig nota númeraröðina fyrir reitinn **fylgiskjalarunur** á nýjum heitum færslubók fjárhags sem voru stofnuð úr fyrri færslubókarheitum afskriftarbókar.</span><span class="sxs-lookup"><span data-stu-id="827cb-158">With either approach, the data upgrade script will also use the number sequence for the **Voucher series** field on the new general ledger journal names created for the former depreciation book journal names.</span></span>




