---
title: Samræmisprófun smásölufærslna
description: Þetta efnisatriði lýsir virkni samræmisprófunar smásölufærslna í Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 05/30/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 0413c2b236e442fb56098f1902b4d5b247ed4649
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/24/2019
ms.locfileid: "2018415"
---
# <a name="retail-transaction-consistency-checker"></a><span data-ttu-id="a8b1c-103">Samræmisprófun smásölufærslna</span><span class="sxs-lookup"><span data-stu-id="a8b1c-103">Retail transaction consistency checker</span></span>


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

<span data-ttu-id="a8b1c-104">Þetta efnisatriði lýsir virkni samræmisprófunar smásölufærslna.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-104">This topic describes the retail transaction consistency checker functionality.</span></span> <span data-ttu-id="a8b1c-105">Í samræmisprófuninni eru færslur með ósamræmi greindar og einangraðar áður en þær eru teknar inn í bókunarferlið.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-105">The consistency checker identifies and isolates inconsistent transactions before they are picked up by the statement posting process.</span></span>

<span data-ttu-id="a8b1c-106">Þegar uppgjör er bókað í Retail getur birtingin mistekist vegna ósamstæðra gagna í færslutöflum.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-106">When a statement is posted in Retail, posting can fail due to inconsistent data in the retail transaction tables.</span></span> <span data-ttu-id="a8b1c-107">Gagnavillan getur orðið vegna ófyrirséðra vandamála í forritinu á sölustað (POS) eða vegna villu í flutningi á færslum úr sölustaðarkerfi þriðja aðila.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-107">The data issue may be caused by unforeseen issues in the point of sale (POS) application, or if transactions were incorrectly imported from third-party POS systems.</span></span> <span data-ttu-id="a8b1c-108">Dæmi um þessi ósamræmi eru meðal annars:</span><span class="sxs-lookup"><span data-stu-id="a8b1c-108">Examples of how these inconsistencies may appear include:</span></span> 

- <span data-ttu-id="a8b1c-109">Heildarfærsla í haustöflu er ekki í samræmi við heildarfærslu í línunum.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-109">The transaction total on the header table does not match the transaction total on the lines.</span></span>
- <span data-ttu-id="a8b1c-110">Línufjöldi í haustöflu er ekki í samræmi við fjölda lína í færslutöflunni.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-110">The line count on the header table does not match with the number of lines in the transaction table.</span></span>
- <span data-ttu-id="a8b1c-111">Skattar í haustöflu eru ekki í samræmi við skattupphæð í línunum.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-111">Taxes on the header table do not match the tax amount on the lines.</span></span> 

<span data-ttu-id="a8b1c-112">Þegar færslur með ósamræmi eru teknar inn í bókunarferlið verða til sölureikningar og greiðslubækur með ósamræmi og villa kemur upp í öllu bókunarferlinu.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-112">When inconsistent transactions are picked up by the statement posting process, inconsistent sales invoices and payment journals are created, and the entire statement posting process fails as a result.</span></span> <span data-ttu-id="a8b1c-113">Í því tilfelli þarf flóknar gagnaleiðréttingar í mörgum færslutöflum til að endurheimta færslurnar.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-113">Recovering the statements from such a state involves complex data fixes across multiple transaction tables.</span></span> <span data-ttu-id="a8b1c-114">Samræmisprófun smásölufærslna kemur í veg fyrir slík vandamál.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-114">The retail transaction consistency checker prevents such issues.</span></span>

<span data-ttu-id="a8b1c-115">Eftirfarandi tafla sýnir bókunarferli með samræmisprófun smásölufærslna.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-115">The following chart illustrates the posting process with the transaction consistency checker.</span></span>

<span data-ttu-id="a8b1c-116">![Bókunarferli uppgjörs með samræmisprófun smásölufærslna](./media/validchecker.png "Bókunarferli uppgjörs með samræmisprófun smásölufærslna")</span><span class="sxs-lookup"><span data-stu-id="a8b1c-116">![Statement posting process with retail transaction consistency checker](./media/validchecker.png "Statement posting process with retail transaction consistency checker")</span></span>

<span data-ttu-id="a8b1c-117">Með runuvinnslunni **Villuleita í færslum verslunar** er samræmi smásölufærslutaflna athugað við eftirfarandi aðstæður.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-117">The **Validate store transactions** batch process checks the consistency of the retail transaction tables for the following scenarios.</span></span>

- <span data-ttu-id="a8b1c-118">**Viðskiptamannalykill** – Staðfestir að viðskiptamannalykillinn í smásölufærslutöflunum sé til staðar í HQ-aðalgögnum viðskiptamanns.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-118">**Customer account** – Validates that the customer account in the retail transaction tables exists in the HQ customer master.</span></span>
- <span data-ttu-id="a8b1c-119">**Línufjöldi** – Staðfestir að línufjöldi, samkvæmt haustöflu færslna, sé í samræmi við fjölda lína í sölufærslutöflunum.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-119">**Line count** – Validates that the number of lines, as captured on the transaction header table, matches the number of lines in the sales transaction tables.</span></span>
- <span data-ttu-id="a8b1c-120">**Verð er með skatti** – Staðfestir að færibreytan **Verð er með skatti** er í samræmi við allar færslulínur.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-120">**Price includes tax** – Validates that the **Price includes tax** parameter is consistent across transaction lines.</span></span>
- <span data-ttu-id="a8b1c-121">**Greiðsluupphæð** – Staðfestir að greiðslufærsla samsvari greiðsluupphæð í haus.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-121">**Payment amount** - Validates that the payment records match the payment amount on header.</span></span>
- <span data-ttu-id="a8b1c-122">**Brúttóupphæð** – Staðfestir að brúttóupphæð í hausnum er summa nettóupphæða í línunum ásamt skattupphæðinni.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-122">**Gross amount** – Validates that the gross amount on the header is the sum of the net amounts on the lines plus the tax amount.</span></span>
- <span data-ttu-id="a8b1c-123">**Nettóupphæð** – Staðfestir að nettóupphæð í hausnum er summa nettóupphæða í línunum.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-123">**Net amount** – Validates that the net amount on the header is the sum of the net amounts on the lines.</span></span>
- <span data-ttu-id="a8b1c-124">**Vangreiðsla/ofgreiðsla** – Staðfestir að mismunur milli brúttóupphæðar í hausnum og greiðsluupphæðar fer ekki umfram skilgreiningu á hámarki fyrir vangreiðslu/ofgreiðslu.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-124">**Under / Over payment** – Validates that the difference between the gross amount on the header and the payment amount doesn't exceed the maximum underpayment/overpayment configuration.</span></span>
- <span data-ttu-id="a8b1c-125">**Afsláttarupphæð** – Staðfestir að samræmi er á afsláttarupphæð í afsláttartöflu og afsláttarupphæð í færslulínu í töflum smásölu og að afsláttarupphæð í hausnum er summa afsláttarupphæða í línunum.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-125">**Discount amount** – Validates that the discount amount on the discount tables and the discount amount on the retail transaction line tables are consistent, and that the discount amount on the header is the sum of the discount amounts on the lines.</span></span>
- <span data-ttu-id="a8b1c-126">**Línuafsláttur** – Staðfestir að línuafsláttur í færslulínunni er summa allra línanna í afsláttartöflunni sem eru í samræmi við færslulínuna.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-126">**Line discount** – Validates that the line discount on the transaction line is the sum of all the lines in the discount table that corresponds to the transaction line.</span></span>
- <span data-ttu-id="a8b1c-127">**Gjafakortsvara** – Retail styður ekki skil á gjafakortsvörum.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-127">**Gift card item** – Retail doesn't support the return of gift card items.</span></span> <span data-ttu-id="a8b1c-128">Hins vegar er hægt að leysa út stöðu á gjafakorti í reiðufé. Gjafakortsvara sem er meðhöndluð sem skilalína í stað línu reiðufjárúttektar kemst ekki í gegnum bókunarferli uppgjörs.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-128">However, the balance on a gift card can be cashed out. Any gift card item that is processed as a return line instead of a cash-out line fails the statement posting process.</span></span> <span data-ttu-id="a8b1c-129">Staðfestingarferlið fyrir gjafakortsvörur hjálpar til við að tryggja að skilalínur gjafakortsvara í smásölufærslutöflunum séu eingöngu línur reiðufjárúttektar fyrir gjafakort.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-129">The validation process for gift card items helps guarantee that the only return gift card line items on the retail transaction tables are gift card cash-out lines.</span></span>
- <span data-ttu-id="a8b1c-130">**Neikvætt verð** – Staðfestir að engar færslulínur með neikvæðu verði eru til staðar.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-130">**Negative price** – Validates that there are no negative price transaction lines.</span></span>
- <span data-ttu-id="a8b1c-131">**Vara og afbrigði** – Staðfestir að vörur og afbrigði í færslulínum eru til staðar í grunnskjali fyrir vöru og afbrigði.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-131">**Item & Variant** – Validates that items and variants on the transaction lines exist in the item and variant master file.</span></span>
- <span data-ttu-id="a8b1c-132">**Skattupphæð** – Staðfestir að skattafærsla samsvari skattupphæð í línum.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-132">**Tax amount** - Validate tax records match the tax amounts on the lines.</span></span> 

## <a name="set-up-the-consistency-checker"></a><span data-ttu-id="a8b1c-133">Setja upp samræmisprófun</span><span class="sxs-lookup"><span data-stu-id="a8b1c-133">Set up the consistency checker</span></span>

<span data-ttu-id="a8b1c-134">Skilgreina skal runuvinnsluna „Villuleita í færslum verslunar“ í **Smásölu \> Upplýsingatækni smásölu \> Sölustaðarbókun** til að keyra vinnsluna reglulega.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-134">Configure the "Validate store transactions" batch process, at **Retail \> Retail IT \> POS posting**, for periodic runs.</span></span> <span data-ttu-id="a8b1c-135">Hægt er að skipuleggja runuvinnsluna á grundvelli stigveldis verslunarinnar, svipað því hvernig ferlin „Reikna uppgjör í runu“ og „Bóka uppgjör í runu“ eru sett upp.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-135">The batch job can be scheduled based on store organization hierarchy, similar to how the "Calculate statement in batch" and "Post statement in batch" processes are set up.</span></span> <span data-ttu-id="a8b1c-136">Við mælum með að þú stillir runuvinnsluna þannig að hún sé keyrð oft á dag og að loknu hverju P-verki.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-136">We recommend that you configure this batch process to run multiple times in a day and schedule it so that it runs at the end of every P-job execution.</span></span>

## <a name="results-of-validation-process"></a><span data-ttu-id="a8b1c-137">Niðurstöður villuleitar</span><span class="sxs-lookup"><span data-stu-id="a8b1c-137">Results of validation process</span></span>

<span data-ttu-id="a8b1c-138">Niðurstöðum villuleitar er bætt við viðkomandi smásölufærslu.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-138">The results of the validation check by the batch process are tagged on the appropriate retail transaction.</span></span> <span data-ttu-id="a8b1c-139">Svæðið **Staða villuleitar** í viðkomandi uppgjörsfærslu er ýmist stillt á **Lokið** eða **Villa** og dagsetning síðustu villuleitar birtist á svæðinu **Tími síðustu villuleitar**.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-139">The **Validation status** field on the retail transaction record is either set to **Successful** or **Error**, and the date of the last validation run appears on the **Last validation time** field.</span></span>

<span data-ttu-id="a8b1c-140">Til að sjá nákvæmari villuboðatexta sem tengist villu í villuleit skal velja viðkomandi færsluskrá smásöluverslunar og smella á hnappinn **Villur við villuleit**.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-140">To view more descriptive error text relating to a validation failure, select the relevant retail store transaction record and click the **Validation errors** button.</span></span>

<span data-ttu-id="a8b1c-141">Færslur sem standast ekki villuleit og færslur sem enn á eftir að villuleita í eru ekki teknar inn í uppgjör.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-141">Transactions that fail the validation check and transactions that have not yet been validated will not be pulled into statements.</span></span> <span data-ttu-id="a8b1c-142">Í ferlinu „Reikna uppgjör“ fá notendur tilkynningu um færslur sem eru ekki með í uppgjörinu en hefðu getað verið það.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-142">During the "Calculate statement" process, users will be notified if there are transactions that could have been included in the statement but weren't.</span></span>

<span data-ttu-id="a8b1c-143">Ef villa finnst við villuleit er einungis hægt að lagfæra hana með því að hafa samband við notendaþjónustu Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-143">If a validation error is found, the only way to fix the error is to contact Microsoft Support.</span></span> <span data-ttu-id="a8b1c-144">Í síðari útgáfu munu notendur geta lagfært skrár með villum í notendaviðmótinu.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-144">In a future release, capability will be added so that users can fix the records that failed through the user interface.</span></span> <span data-ttu-id="a8b1c-145">Einnig bætast við endurskoðunar- og skráningareiginleikar til að rekja breytingarsöguna.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-145">Logging and auditing capabilities will also be made available to trace the history of the modifications.</span></span>

> [!NOTE]
> <span data-ttu-id="a8b1c-146">Frekari villuleitarreglum til að styðja við fleiri aðstæður verður bætt við í síðari útgáfu.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-146">Additional validation rules to support more scenarios will be added in a future release.</span></span>
