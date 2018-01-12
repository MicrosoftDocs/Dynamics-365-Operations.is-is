---
title: "Númeraraðir"
description: "Númeraraðir eru notaðar til að mynda lesanleg, einkvæm kennimerki fyrir skýrslur aðalgagna og færslur sem krefjast kennimerkja."
author: MargoC
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 15461
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 63bf043124797b328116fd7951913eaeda6ff97b
ms.openlocfilehash: 8e3899e1ad5f4be754687c0e2d59348e7a773fd8
ms.contentlocale: is-is
ms.lasthandoff: 01/12/2018

---

# <a name="number-sequences"></a><span data-ttu-id="4630d-103">Númeraraðir</span><span class="sxs-lookup"><span data-stu-id="4630d-103">Number sequences</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="4630d-104">Númeraraðir eru notaðar til að mynda lesanleg, einkvæm kennimerki fyrir skýrslur aðalgagna og færslur sem krefjast kennimerkja.</span><span class="sxs-lookup"><span data-stu-id="4630d-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require identifiers.</span></span> <span data-ttu-id="4630d-105">færsla aðalgagna eða færsla sem krefst kennimerkis er vísað til sem *tilvísun*.</span><span class="sxs-lookup"><span data-stu-id="4630d-105">A master data record or transaction record that requires an identifier is referred to as a *reference*.</span></span>

<span data-ttu-id="4630d-106">Áður en hægt er að stofna nýjar færslur fyrir tilvísun verður að setja upp númeraröð og tengja hana við tilvísunina.</span><span class="sxs-lookup"><span data-stu-id="4630d-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="4630d-107">Mælt er með því að nota síðurnar í **Fyrirtækisstjórnun** til að setja upp númeraraðir.</span><span class="sxs-lookup"><span data-stu-id="4630d-107">We recommend that you use the pages in **Organization administration** to set up number sequences.</span></span> <span data-ttu-id="4630d-108">Ef Kerfiseining stillingar eru áskilin er hægt að nota síðuna færibreytur í kerfi til að tilgreina númeraröð fyrir tilvísanir í því kerfi.</span><span class="sxs-lookup"><span data-stu-id="4630d-108">If module-specific settings are required, you can use the parameters page in a module to specify number sequences for the references in that module.</span></span> <span data-ttu-id="4630d-109">Til dæmis í **viðskiptakröfur** og **viðskiptaskuldir** , er hægt að setja upp flokka númeraraða til að úthluta tilteknum númeraraðir til ákveðinna viðskiptavina eða lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="4630d-109">For example, in **Accounts receivable** and **Accounts payable**, you can set up number sequence groups to allocate specific number sequences to specific customers or vendors.</span></span> 

<span data-ttu-id="4630d-110">Þegar sett er upp númeraröð, verður að tilgreina svið, sem skilgreinir hvaða fyrirtæki notar númeraröðina.</span><span class="sxs-lookup"><span data-stu-id="4630d-110">When you set up a number sequence, you must specify a scope, which defines which organization uses the number sequence.</span></span> <span data-ttu-id="4630d-111">Umfang getur verið **Samnýtt**, **Fyrirtæki**, **lögaðila**, eða **rekstrareining**.</span><span class="sxs-lookup"><span data-stu-id="4630d-111">The scope can be **Shared**, **Company**, **Legal entity**, or **Operating unit**.</span></span> <span data-ttu-id="4630d-112">Umfang **lögaðila** og **fyrirtækja** má sameina við **tímabil fjárhagsdagatals** til að búa til enn sértækari númeraraðir.</span><span class="sxs-lookup"><span data-stu-id="4630d-112">**Legal entity** and **Company** scopes can be combined with **Fiscal calendar period** to create even more specific number sequences.</span></span> 

<span data-ttu-id="4630d-113">Talnarunu snið samanstanda af hluti.</span><span class="sxs-lookup"><span data-stu-id="4630d-113">Number sequence formats consist of segments.</span></span> <span data-ttu-id="4630d-114">Númeraraðir með annað umfang en **samnýtt** geta innihaldið hluti sem samsvara umfangi.</span><span class="sxs-lookup"><span data-stu-id="4630d-114">Number sequences with a scope other than **Shared** can contain segments that correspond to the scope.</span></span> <span data-ttu-id="4630d-115">Til dæmis getur talnaröð með umfangið **lögaðili** innihaldið hluta lögaðila.</span><span class="sxs-lookup"><span data-stu-id="4630d-115">For example, a number sequence with a scope of **Legal entity** can contain a legal entity segment.</span></span> <span data-ttu-id="4630d-116">Með því að hafa svið hluta í snið númeraraðar, er hægt að greina svið tiltekna færslu með því að líta á númeri þess.</span><span class="sxs-lookup"><span data-stu-id="4630d-116">By including a scope segment in the number sequence format, you can identify the scope of a particular record by looking at its number.</span></span> 

<span data-ttu-id="4630d-117">Auk hluta sem samsvara umfangi, geta sniðmát númeraraðar innihaldið **fasta** og **tölustafahluta** .</span><span class="sxs-lookup"><span data-stu-id="4630d-117">In addition to segments that correspond to scopes, number sequence formats can contain **Constant** and **Alphanumeric segments**.</span></span> <span data-ttu-id="4630d-118">Hlutinn **Fasti** inniheldur safn stafa, tölustafa eða tákn sem breytast ekki.</span><span class="sxs-lookup"><span data-stu-id="4630d-118">A **Constant** segment contains a set of letters, numbers, or symbols that does not change.</span></span> <span data-ttu-id="4630d-119">**Tölustafa** Hluti inniheldur safn af bókstöfum eða tölustöfum sem hækka í hvert skipti sem tala er notuð.</span><span class="sxs-lookup"><span data-stu-id="4630d-119">An **Alphanumeric** segment contains a set of letters or numbers that increment every time that a number is used.</span></span> <span data-ttu-id="4630d-120">Nota númerstákn (\#) til að tákna hækkandi tölustafi og og-merki (&) til að tilgreina hækkandi bókstafi.</span><span class="sxs-lookup"><span data-stu-id="4630d-120">Use a number sign (\#) to represent incrementing numbers and an ampersand (&) to represent incrementing letters.</span></span> <span data-ttu-id="4630d-121">Sniðið \#\#\#\#\#\_2017 stofnar t.d. röðina 00001\_2017, 00002\_2017 og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="4630d-121">For example, the format \#\#\#\#\#\_2017 creates the sequence 00001\_2017, 00002\_2017, and so on.</span></span>

<a name="number-sequence-examples"></a><span data-ttu-id="4630d-122">Talnarunu dæmi</span><span class="sxs-lookup"><span data-stu-id="4630d-122">Number sequence examples</span></span>
------------------------

<span data-ttu-id="4630d-123">Eftirfarandi dæmi sýna hvernig á að nota hluta til að stofna snið númeraraðar.</span><span class="sxs-lookup"><span data-stu-id="4630d-123">The following examples show how to use segments to create number sequence formats.</span></span> <span data-ttu-id="4630d-124">Sérstaklega, sýna dæmin áhrif þess að nota sviðshluta.</span><span class="sxs-lookup"><span data-stu-id="4630d-124">In particular, the examples demonstrate the effects of using scope segments.</span></span>

### <a name="expense-report-numbers"></a><span data-ttu-id="4630d-125">Númer kostnaðarskýrslu</span><span class="sxs-lookup"><span data-stu-id="4630d-125">Expense report numbers</span></span>

<span data-ttu-id="4630d-126">Í eftirfarandi dæmi eru kostnaðarskýrslutölur settar upp fyrir lögaðilann sem heitir **CS**.</span><span class="sxs-lookup"><span data-stu-id="4630d-126">In the following example, expense report numbers are set up for the legal entity that is titled **CS**.</span></span> 

- <span data-ttu-id="4630d-127">**Svið:** Ferðalög og kostnaður</span><span class="sxs-lookup"><span data-stu-id="4630d-127">**Area:** Travel and expense</span></span> 
- <span data-ttu-id="4630d-128">**Tilvísun:** Númer kostnaðarskýrslu</span><span class="sxs-lookup"><span data-stu-id="4630d-128">**Reference:** Expense report number</span></span> 
- <span data-ttu-id="4630d-129">**Umfang:**lögaðila</span><span class="sxs-lookup"><span data-stu-id="4630d-129">**Scope:** Legal entity</span></span> 
- <span data-ttu-id="4630d-130">**Lögaðili:** CS</span><span class="sxs-lookup"><span data-stu-id="4630d-130">**Legal entity:** CS</span></span>

| <span data-ttu-id="4630d-131">Hlutar</span><span class="sxs-lookup"><span data-stu-id="4630d-131">Segments</span></span>  | <span data-ttu-id="4630d-132">Hlutagerð</span><span class="sxs-lookup"><span data-stu-id="4630d-132">Segment type</span></span> | <span data-ttu-id="4630d-133">Gildi</span><span class="sxs-lookup"><span data-stu-id="4630d-133">Value</span></span>     |
|-----------|--------------|-----------|
| <span data-ttu-id="4630d-134">Hluti 1</span><span class="sxs-lookup"><span data-stu-id="4630d-134">Segment 1</span></span> | <span data-ttu-id="4630d-135">Lögaðili</span><span class="sxs-lookup"><span data-stu-id="4630d-135">Legal entity</span></span> | <span data-ttu-id="4630d-136">CS</span><span class="sxs-lookup"><span data-stu-id="4630d-136">CS</span></span>        |
| <span data-ttu-id="4630d-137">Hluti 2</span><span class="sxs-lookup"><span data-stu-id="4630d-137">Segment 2</span></span> | <span data-ttu-id="4630d-138">Fasti</span><span class="sxs-lookup"><span data-stu-id="4630d-138">Constant</span></span>     | <span data-ttu-id="4630d-139">-ÚTGJÖLD-</span><span class="sxs-lookup"><span data-stu-id="4630d-139">-EXPENSE-</span></span> |
| <span data-ttu-id="4630d-140">Hluti 3</span><span class="sxs-lookup"><span data-stu-id="4630d-140">Segment 3</span></span> | <span data-ttu-id="4630d-141">Bók- og tölustafir</span><span class="sxs-lookup"><span data-stu-id="4630d-141">Alphanumeric</span></span> | \#\#\#\#  |

<span data-ttu-id="4630d-142">**Dæmi um snið númer**: CS-kostnað - 0039</span><span class="sxs-lookup"><span data-stu-id="4630d-142">**Example of formatted number**: CS-EXPENSE-0039</span></span> 

<span data-ttu-id="4630d-143">Þú getur sett upp svipað talnarunusnið fyrir aðra lögaðila.</span><span class="sxs-lookup"><span data-stu-id="4630d-143">You can set up a similar number sequence format for other legal entities.</span></span> <span data-ttu-id="4630d-144">Til dæmis, fyrir lögaðila sem nefnist **RW**, ef aðeins gildið hluta lögaðila er breytt er forsniðið númer RW-EXPENSE-0039.</span><span class="sxs-lookup"><span data-stu-id="4630d-144">For example, for a legal entity that is named **RW**, if you change only the value of the legal entity segment, the formatted number is RW-EXPENSE-0039.</span></span> <span data-ttu-id="4630d-145">Einnig er hægt að breyta heiltölusniði númeraraðar fyrir aðra lögaðila.</span><span class="sxs-lookup"><span data-stu-id="4630d-145">You can also change the whole number sequence format for other legal entities.</span></span> <span data-ttu-id="4630d-146">Til dæmis er hægt að sleppa svið hluta lögaðila til að stofna forsniðið númer svo Lokagildistíma 0001.</span><span class="sxs-lookup"><span data-stu-id="4630d-146">For example, you can omit the legal entity scope segment to create a formatted number such as Exp-0001.</span></span>

### <a name="sales-order-numbers"></a><span data-ttu-id="4630d-147">Sölupöntunarnúmer</span><span class="sxs-lookup"><span data-stu-id="4630d-147">Sales order numbers</span></span>

<span data-ttu-id="4630d-148">Í eftirfarandi dæmi eru númer sölupöntunar sett upp fyrir fyrirtækjakennið **CEU**.</span><span class="sxs-lookup"><span data-stu-id="4630d-148">In the following example, sales order numbers are set up for the company ID **CEU**.</span></span> 

- <span data-ttu-id="4630d-149">**: Svæði** Sölu</span><span class="sxs-lookup"><span data-stu-id="4630d-149">**Area:** Sales</span></span> 
- <span data-ttu-id="4630d-150">**Tilvísun:** Sölupöntun</span><span class="sxs-lookup"><span data-stu-id="4630d-150">**Reference:** Sales order</span></span> 
- <span data-ttu-id="4630d-151">**Umfang:** Fyrirtækið</span><span class="sxs-lookup"><span data-stu-id="4630d-151">**Scope:** Company</span></span> 
- <span data-ttu-id="4630d-152">**Fyrirtæki:** CEU</span><span class="sxs-lookup"><span data-stu-id="4630d-152">**Company:** CEU</span></span>

| <span data-ttu-id="4630d-153">Hlutar</span><span class="sxs-lookup"><span data-stu-id="4630d-153">Segments</span></span>  | <span data-ttu-id="4630d-154">Gerð hluta</span><span class="sxs-lookup"><span data-stu-id="4630d-154">Segment type</span></span> | <span data-ttu-id="4630d-155">Virði</span><span class="sxs-lookup"><span data-stu-id="4630d-155">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="4630d-156">Hluti 1</span><span class="sxs-lookup"><span data-stu-id="4630d-156">Segment 1</span></span> | <span data-ttu-id="4630d-157">Fasti</span><span class="sxs-lookup"><span data-stu-id="4630d-157">Constant</span></span>     | <span data-ttu-id="4630d-158">SO-</span><span class="sxs-lookup"><span data-stu-id="4630d-158">SO-</span></span>      |
| <span data-ttu-id="4630d-159">Hluti 2</span><span class="sxs-lookup"><span data-stu-id="4630d-159">Segment 2</span></span> | <span data-ttu-id="4630d-160">Bók- og tölustafir</span><span class="sxs-lookup"><span data-stu-id="4630d-160">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="4630d-161">**Dæmi um snið númer**: SO-0029</span><span class="sxs-lookup"><span data-stu-id="4630d-161">**Example of formatted number**: SO-0029</span></span> 

<span data-ttu-id="4630d-162">Jafnvel þótt svið hluta er ekki tekið með í sniði endurræsir tölusetning fyrir hvert fyrirtækjakenni.</span><span class="sxs-lookup"><span data-stu-id="4630d-162">Even though a scope segment is not included in the format, numbering restarts for each company ID.</span></span> <span data-ttu-id="4630d-163">Ef notað er sama snið fyrir öll fyrirtækiskenni , eru sama númer notað í hverju fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="4630d-163">If you use the same format for all company IDs, the same numbers are used in each company.</span></span> <span data-ttu-id="4630d-164">Til dæmis sölupöntunarnúmer SO 0029 er notað í hverju fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="4630d-164">For example, sales order number SO-0029 is used in each company.</span></span> <span data-ttu-id="4630d-165">Einnig er hægt að breyta heiltölusniði númeraraðar fyrir önnur fyrirtækiskenni.</span><span class="sxs-lookup"><span data-stu-id="4630d-165">You can also change the whole number sequence format for other company IDs.</span></span>

### <a name="purchase-requisition-numbers"></a><span data-ttu-id="4630d-166">Númer innkaupabeiðna</span><span class="sxs-lookup"><span data-stu-id="4630d-166">Purchase requisition numbers</span></span>

<span data-ttu-id="4630d-167">Í eftirfarandi dæmi, eru númer innkaupabeiðna úr öllu fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="4630d-167">In the following example, purchase requisition numbers are organization-wide.</span></span> 

- <span data-ttu-id="4630d-168">**Svæði:** Innkaup</span><span class="sxs-lookup"><span data-stu-id="4630d-168">**Area:** Purchase</span></span> 
- <span data-ttu-id="4630d-169">**Tilvísun:** Innkaupabeiðni</span><span class="sxs-lookup"><span data-stu-id="4630d-169">**Reference:** Purchase requisition</span></span> 
- <span data-ttu-id="4630d-170">**Umfang:** Deilt</span><span class="sxs-lookup"><span data-stu-id="4630d-170">**Scope:** Shared</span></span>

| <span data-ttu-id="4630d-171">Hlutar</span><span class="sxs-lookup"><span data-stu-id="4630d-171">Segments</span></span>  | <span data-ttu-id="4630d-172">Gerð hluta</span><span class="sxs-lookup"><span data-stu-id="4630d-172">Segment type</span></span> | <span data-ttu-id="4630d-173">Virði</span><span class="sxs-lookup"><span data-stu-id="4630d-173">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="4630d-174">Hluti 1</span><span class="sxs-lookup"><span data-stu-id="4630d-174">Segment 1</span></span> | <span data-ttu-id="4630d-175">Fasti</span><span class="sxs-lookup"><span data-stu-id="4630d-175">Constant</span></span>     | <span data-ttu-id="4630d-176">Req</span><span class="sxs-lookup"><span data-stu-id="4630d-176">Req</span></span>      |
| <span data-ttu-id="4630d-177">Hluti 2</span><span class="sxs-lookup"><span data-stu-id="4630d-177">Segment 2</span></span> | <span data-ttu-id="4630d-178">Bók- og tölustafir</span><span class="sxs-lookup"><span data-stu-id="4630d-178">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="4630d-179">**Dæmi um snið númer**: Req0052</span><span class="sxs-lookup"><span data-stu-id="4630d-179">**Example of formatted number**: Req0052</span></span> 

<span data-ttu-id="4630d-180">Þar sem umfang er **Deilt** er sniðmát númeraraðar notað þvert yfir fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="4630d-180">Because the scope is **Shared**, the number sequence format is used across the organization.</span></span> <span data-ttu-id="4630d-181">Hægt er að setja upp mismunandi röð snið fyrir mismunandi hluta fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="4630d-181">You cannot set up different number sequence formats for different parts of the organization.</span></span> 

<a name="performance-considerations-for-number-sequences"></a><span data-ttu-id="4630d-182">Afkastaatriði fyrir númeraraðir</span><span class="sxs-lookup"><span data-stu-id="4630d-182">Performance considerations for number sequences</span></span>
-----------------------------------------------

<span data-ttu-id="4630d-183">Íhugið eftirfarandi upplýsingar um hvernig afbrigði númeraröðum geta haft áhrif á afköst kerfisins áður en hægt er að setja upp númeraraðir.</span><span class="sxs-lookup"><span data-stu-id="4630d-183">Consider the following information about how the configuration of number sequences can affect system performance before you set up number sequences.</span></span>

### <a name="continuous-and-non-continuous-number-sequences"></a><span data-ttu-id="4630d-184">Samfelld og ekki samfelld númeraraðir</span><span class="sxs-lookup"><span data-stu-id="4630d-184">Continuous and non-continuous number sequences</span></span>

<span data-ttu-id="4630d-185">Númeraraðir geta verið samfelldar eða ósamfelldar.</span><span class="sxs-lookup"><span data-stu-id="4630d-185">Number sequences can be continuous or non-continuous.</span></span> <span data-ttu-id="4630d-186">Samfelld númeraröð sleppir ekki neinum tölum en númer má ekki nota í númeraröð.</span><span class="sxs-lookup"><span data-stu-id="4630d-186">A continuous number sequence does not skip any numbers, but numbers may not be used sequentially.</span></span> <span data-ttu-id="4630d-187">Tölur úr ósamfelldri talnarunu eru notuð í röð, en talnarunan kann að sleppa tölum.</span><span class="sxs-lookup"><span data-stu-id="4630d-187">Numbers from a non-continuous number sequence are used sequentially, but the number sequence may skip numbers.</span></span> <span data-ttu-id="4630d-188">Til dæmis, ef notandi hættir færslu, númer er myndað en ekki notað.</span><span class="sxs-lookup"><span data-stu-id="4630d-188">For example, if a user cancels a transaction, a number is generated, but not used.</span></span> <span data-ttu-id="4630d-189">Í samfelldni númeraröð, það númer er endurnýtt síðar.</span><span class="sxs-lookup"><span data-stu-id="4630d-189">In a continuous number sequence, that number is recycled later.</span></span> <span data-ttu-id="4630d-190">Í ósamfelldri númeraröð, ernúmer ekki notað.</span><span class="sxs-lookup"><span data-stu-id="4630d-190">In a non-continuous number sequence, the number is not used.</span></span> 

<span data-ttu-id="4630d-191">Samfelld númeraraðir eru yfirleitt áskilin fyrir ytri skjöl, eins og innkaupapöntunum, sölupöntunum og reikningum.</span><span class="sxs-lookup"><span data-stu-id="4630d-191">Continuous number sequences are typically required for external documents, such as purchase orders, sales orders, and invoices.</span></span> <span data-ttu-id="4630d-192">Hins vegar samfelldri númeraröð getur haft neikvæð áhrif svartíma kerfi þar sem kerfið að biðja um númer úr gagnagrunninum í hvert skipti nýtt skjal eða færsla er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="4630d-192">However, continuous number sequences can adversely affect system response times because the system must request a number from the database every time that a new document or record is created.</span></span> 

<span data-ttu-id="4630d-193">Ef ósamfelld númeraröð er notuð, er hægt að virkja **forúthlutun** á **afkoma** flýtiflipa í **númeraröð** síðu.</span><span class="sxs-lookup"><span data-stu-id="4630d-193">If you use a non-continuous number sequence, you can enable **Preallocation** on the **Performance** FastTab of the **Number sequences** page.</span></span> <span data-ttu-id="4630d-194">Þegar tilgreindur er fjöldi til að forúthluta, velur kerfið þessar tölur og vistar þær í minni.</span><span class="sxs-lookup"><span data-stu-id="4630d-194">When you specify a quantity of numbers to preallocate, the system selects those numbers and stores them in memory.</span></span> <span data-ttu-id="4630d-195">Ný tölur eru beðnir úr gagnagrunninum aðeins eftir að fyrirframúthlutað magn hefur verið notað.</span><span class="sxs-lookup"><span data-stu-id="4630d-195">New numbers are requested from the database only after the preallocated quantity has been used.</span></span> 

<span data-ttu-id="4630d-196">Ef ekki eru fyrirliggjandi lagaskilyrði um að notaðar séu samfelldar númeraraðir er ráðlagt að nota ekki samfelldar númeraraðir fyrir betri afköst.</span><span class="sxs-lookup"><span data-stu-id="4630d-196">Unless there is a regulatory requirement that you use continuous number sequences, we recommend that you use non-continuous number sequences for better performance.</span></span>

### <a name="automatic-cleanup-of-number-sequences"></a><span data-ttu-id="4630d-197">Sjálfvirk tiltekt númeraraðir</span><span class="sxs-lookup"><span data-stu-id="4630d-197">Automatic cleanup of number sequences</span></span>

<span data-ttu-id="4630d-198">Ef rafmagnsleysi kemur upp, villa forrits eða önnur óvænt óhöpp getur kerfið ekki endurunnið númer sjálfkrafa fyrir samfelldri númeraröð.</span><span class="sxs-lookup"><span data-stu-id="4630d-198">In case of a power failure, an application error, or other unexpected failure, the system cannot recycle numbers automatically for continuous number sequences.</span></span> <span data-ttu-id="4630d-199">Hægt er að keyra tiltekt handvirkt eða sjálfvirkt til að endurheimta týnd númer.</span><span class="sxs-lookup"><span data-stu-id="4630d-199">You can run the cleanup process manually or automatically to recover the lost numbers.</span></span> 

<span data-ttu-id="4630d-200">Íhugaðu vandlega notkun þjóns þegar hreinsunarferli er áætlað.</span><span class="sxs-lookup"><span data-stu-id="4630d-200">Carefully consider server usage when you plan the cleanup process.</span></span> <span data-ttu-id="4630d-201">Mælt er með því að tiltektin sé keyrð sem runuvinnsla utan háannatíma.</span><span class="sxs-lookup"><span data-stu-id="4630d-201">We recommend that you perform the cleanup as a batch job during non-peak hours.</span></span>






