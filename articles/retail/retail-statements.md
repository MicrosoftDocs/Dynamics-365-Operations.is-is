---
title: Smásöluuppgjör
description: Þetta efnisatriði lýsir því hvernig uppgjör eru búin til og bókuð.
author: ashishmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 9e88a8b22b73aca5c2cee6984ecad3c62e597102
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568000"
---
# <a name="retail-statements"></a><span data-ttu-id="25bae-103">Smásöluuppgjör</span><span class="sxs-lookup"><span data-stu-id="25bae-103">Retail statements</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="25bae-104">Í Microsoft Dynamics 365 for Retail, er bókunarferli uppgjörs notað til að gera grein fyrir færslum sem koma upp í sölustað í skýi eða Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="25bae-104">In Microsoft Dynamics 365 for Retail, the statement posting process is used to account for the transactions that occur in Cloud point of sale (POS) or Modern POS (MPOS).</span></span> <span data-ttu-id="25bae-105">Uppgjörsbókunarferlið notast við dreifingaráætlunina til að sækja safn sölustaðarfærslna í höfuðbiðlara (HQ).</span><span class="sxs-lookup"><span data-stu-id="25bae-105">The statement posting process uses the distribution schedule to pull a set of POS transactions into the headquarters (HQ) client.</span></span> <span data-ttu-id="25bae-106">Færibreytur sem skilgreindar eru á síðunum **Smásölufæribreytur** og **Verslanir** eru notaðar til að velja færslurnar sem eru sóttar í einstök uppgjör.</span><span class="sxs-lookup"><span data-stu-id="25bae-106">The parameters that are defined on the **Retail parameters** and **Stores** pages are used to select the transactions that are pulled into individual statements.</span></span>

<span data-ttu-id="25bae-107">Eftirfarandi skýringarmynd sýnir uppgjörsbókunarferlið.</span><span class="sxs-lookup"><span data-stu-id="25bae-107">The following illustration shows the statement posting process.</span></span> <span data-ttu-id="25bae-108">Í þessu ferli eru færslur sem eru skráðar á sölustað sendar til biðlara með því að nota verkraðara smásölu.</span><span class="sxs-lookup"><span data-stu-id="25bae-108">In this process, transactions that are recorded in the POS are transmitted to the client by using the Retail scheduler.</span></span> <span data-ttu-id="25bae-109">Eftir að biðlari tekur við færslunum, er hægt að stofna, reikna og bóka færsluuppgjör fyrir verslunina.</span><span class="sxs-lookup"><span data-stu-id="25bae-109">After the client receives the transactions, you can create, calculate, and post the transaction statement for the store.</span></span>

<span data-ttu-id="25bae-110">[![Uppgjörsbókunarferli](./media/retail-statements.png)](./media/retail-statements.png)</span><span class="sxs-lookup"><span data-stu-id="25bae-110">[![Statement posting process](./media/retail-statements.png)](./media/retail-statements.png)</span></span>

## <a name="creating-and-posting-statements"></a><span data-ttu-id="25bae-111">Stofna og bóka uppgjör</span><span class="sxs-lookup"><span data-stu-id="25bae-111">Creating and posting statements</span></span>

<span data-ttu-id="25bae-112">Hægt er að stofna uppgjör handvirkt eða með því að nota runuvinnslur sem þú setur upp til að keyra reglubundið allan daginn.</span><span class="sxs-lookup"><span data-stu-id="25bae-112">You can create a statement manually or by using batch processes that you set up to run periodically throughout the day.</span></span> <span data-ttu-id="25bae-113">Í báðum tilvikum eftirfarandi skref eru notaðar til að stofna og bóka uppgjör.</span><span class="sxs-lookup"><span data-stu-id="25bae-113">In both cases, the following steps are used to create and post statements.</span></span>

### <a name="create-the-statement"></a><span data-ttu-id="25bae-114">Stofna yfirlitið</span><span class="sxs-lookup"><span data-stu-id="25bae-114">Create the statement</span></span>

<span data-ttu-id="25bae-115">Þetta skref auðkennir uppgjör er stofnað handvirkt fyrir verslun.</span><span class="sxs-lookup"><span data-stu-id="25bae-115">This step identifies the store that the statement is manually created for.</span></span> <span data-ttu-id="25bae-116">Ef skilgreina runuvinnslu sjálfvirkt er hægt að stofna uppgjör fyrir allar verslanir samkvæmt áætlun sem skilgreina.</span><span class="sxs-lookup"><span data-stu-id="25bae-116">If you configure a batch process, you can automatically create statements for all stores, based on a schedule that you define.</span></span>

### <a name="calculate-the-statement"></a><span data-ttu-id="25bae-117">Reikna yfirlitið</span><span class="sxs-lookup"><span data-stu-id="25bae-117">Calculate the statement</span></span>

<span data-ttu-id="25bae-118">Í þessu þrepi eru færslulínur valdar eftir skilyrðum sem eru skilgreind fyrir hverja verslun á síðunum **Smásölufæribreytur** og **Verslanir**.</span><span class="sxs-lookup"><span data-stu-id="25bae-118">In this step, the transaction lines are selected based on criteria that are defined for each store on the **Retail parameters** and **Stores** pages.</span></span> <span data-ttu-id="25bae-119">Á þessum síðum skilgreinir þú skilyrði og tilgreinir hvernig færslurnar eru reiknaðar.</span><span class="sxs-lookup"><span data-stu-id="25bae-119">On these pages, you define the criteria and specify how the transactions are calculated.</span></span> <span data-ttu-id="25bae-120">Til að skoða lista yfir færslur sem eru teknar með í uppgjörinu áður en uppgjör er reiknað út skal nota síðuna **Færslur**.</span><span class="sxs-lookup"><span data-stu-id="25bae-120">To view a list of the transactions that are included in the statement before you calculate the statement, use the **Transactions** page.</span></span>

<span data-ttu-id="25bae-121">Útreikningur uppgjörs notar skiptimyntartalningu frá afgreiðslukössunum sem talda upphæð.</span><span class="sxs-lookup"><span data-stu-id="25bae-121">Statement calculation uses tender declarations from the registers as the counted amount.</span></span> <span data-ttu-id="25bae-122">Einnig er hægt að færa talda upphæð inn handvirkt.</span><span class="sxs-lookup"><span data-stu-id="25bae-122">Alternatively, you can enter the counted amount manually.</span></span> <span data-ttu-id="25bae-123">Uppgjörið sýnir muninn á milli söluupphæðar fyrir færslur og raunverulegrar talinnar upphæðar í öllum greiðsluháttum.</span><span class="sxs-lookup"><span data-stu-id="25bae-123">The statement shows the difference between the sales amount for the transactions and the actual counted amount in all payment methods.</span></span> <span data-ttu-id="25bae-124">Uppgjörið bókast ef þessi mismunur er minna en hámarksbókunarmismunur sem er skilgreind fyrir verslunina.</span><span class="sxs-lookup"><span data-stu-id="25bae-124">The statement is posted only if this difference is less than the maximum posting difference that is defined for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="25bae-125">Útreikningur yfirlits ferlið notar altæka númeraröð.</span><span class="sxs-lookup"><span data-stu-id="25bae-125">The statement calculation process uses the global number sequence.</span></span>

<span data-ttu-id="25bae-126">Þegar þú reiknar út yfirlýsingu, felur útreikningurinn í sér eftirfarandi verkefni:</span><span class="sxs-lookup"><span data-stu-id="25bae-126">When you calculate a statement, the calculation includes the following tasks:</span></span>

- <span data-ttu-id="25bae-127">Merktu færslur fyrir valið tímabil sem voru ekki með í fyrri útreikningi uppgjörs.</span><span class="sxs-lookup"><span data-stu-id="25bae-127">For the selected date range, mark transactions that weren't included in a previous statement calculation.</span></span>
- <span data-ttu-id="25bae-128">Reiknaðu út heildarupphæðir sem tekið var við í völdum færslum.</span><span class="sxs-lookup"><span data-stu-id="25bae-128">Calculate the total amounts that were tendered in the selected transactions.</span></span> <span data-ttu-id="25bae-129">Niðurstöðurnar eru birtar á uppgjörslínum, eftir uppgjörsaðferðinni:</span><span class="sxs-lookup"><span data-stu-id="25bae-129">The results are shown on the statement lines, depending on the statement method:</span></span>

    - <span data-ttu-id="25bae-130">Ef uppgjörsaðferðin er **Samtala**, er lína stofnuð fyrir hvern greiðslumáta í völdum færslum.</span><span class="sxs-lookup"><span data-stu-id="25bae-130">If the statement method is **Total**, a line is created for each payment method in the selected transactions.</span></span>
    - <span data-ttu-id="25bae-131">Ef uppgjörsaðferðin er **Starfsmaður**, er lína stofnuð fyrir hvern greiðslumáta í færslum sem voru framkvæmdar af völdum starfsmönnum.</span><span class="sxs-lookup"><span data-stu-id="25bae-131">If the statement method is **Staff**, a line is created for each payment method in transactions that were performed by the selected staff member.</span></span>
    - <span data-ttu-id="25bae-132">Ef uppgjörsaðferðin er **Afgreiðslukassi**, er lína stofnuð fyrir hvern greiðslumáta í færslum sem voru framkvæmdar í völdum afgreiðslukössum.</span><span class="sxs-lookup"><span data-stu-id="25bae-132">If the statement method is **POS terminal**, a line is created for each payment method in transactions that were performed on the selected register.</span></span>
    - <span data-ttu-id="25bae-133">Ef uppgjörsaðferðin er **Vakt**, er lína stofnuð fyrir hvern greiðslumáta í færslum sem voru framkvæmdar á vakt.</span><span class="sxs-lookup"><span data-stu-id="25bae-133">If the statement method is **Shift**, a line is created for each payment method in transactions that were performed during a shift.</span></span>

<span data-ttu-id="25bae-134">Ef gátreiturinn **Skipta eftir uppgjörsaðferð** er valinn á síðunni **Verslanir**, er sérstakt uppgjör stofnað eftir gildinu sem valið er í reitnum **Uppgjörsaðferð**.</span><span class="sxs-lookup"><span data-stu-id="25bae-134">If the **Split by Statement method** check box is selected on the **Stores** page, a separate statement is created based on the value that is selected in the **Statement method** field.</span></span>

<span data-ttu-id="25bae-135">Ef afgreiðslutími verslunar þinnar er lengur en fram yfir miðnætti, er hægt að stilla uppgjörsbókun þannig að hún sé í lok viðskiptadags frekar en í lok almanaksdags.</span><span class="sxs-lookup"><span data-stu-id="25bae-135">If your store's operating hours extend past midnight, you can configure statement posting so that it's based on the end of the business day instead of the end of the calendar day.</span></span>

<span data-ttu-id="25bae-136">Á síðunni **Verslanir**, í flýtiflipanum **Uppgjör/lokun**, í reitnum **Lok viðskiptadags** skal færa inn tímann sem síðasta færslan verður að vera skráð til að vera tekin með í uppgjöri viðskiptadags.</span><span class="sxs-lookup"><span data-stu-id="25bae-136">On the **Stores** page, on the **Statement/closing** FastTab, in the **End of business day** field, enter the time that the last transaction must be recorded to be included in the business day's statement.</span></span> <span data-ttu-id="25bae-137">Veldu gátreitinn **Bóka sem viðskiptadag** til að bóka færsluna innan sama viðskiptadags.</span><span class="sxs-lookup"><span data-stu-id="25bae-137">Select the **Post as business day** check box to post the transactions within the same business day.</span></span> <span data-ttu-id="25bae-138">Þegar uppgjör er bókað, er hægt að hafa færslur sem skráðar eru innan sama viðskiptadags á sömu sölupöntun, þrátt fyrir að einhverjar færslur eigi sér stað fyrir miðnætti og aðrar færslur eigi sér stað eftir miðnætti.</span><span class="sxs-lookup"><span data-stu-id="25bae-138">When the statement is posted, transactions that are recorded within the same business day can be included on the same sales order, even if some transactions occur before midnight and other transactions occur after midnight.</span></span>

#### <a name="example-post-a-statement-for-a-business-day-that-extends-over-two-calendar-days"></a><span data-ttu-id="25bae-139">Dæmi: Bókaðu yfirlýsing fyrir viðskiptadag sem nær yfir tvö almanaksdagar</span><span class="sxs-lookup"><span data-stu-id="25bae-139">Example: Post a statement for a business day that extends over two calendar days</span></span>

<span data-ttu-id="25bae-140">Verslun er opin milli 8:00 og 3:00 og gátreiturinn **Bóka sem viðskiptadag** er valinn í stillingum verslunarinnar.</span><span class="sxs-lookup"><span data-stu-id="25bae-140">A store is open between 8:00 AM and 3:00 AM, and the **Post as business day** check box is selected in the store's configuration.</span></span> <span data-ttu-id="25bae-141">Þann 31. maí skráir verslunin færslur milli 8:00 og miðnættis.</span><span class="sxs-lookup"><span data-stu-id="25bae-141">On May 31, the store records transactions between 8:00 AM and midnight.</span></span> <span data-ttu-id="25bae-142">Verslunin skráir einnig færslur milli 0:01 og 3:00 þann 1. júní.</span><span class="sxs-lookup"><span data-stu-id="25bae-142">The store also records transactions between 12:01 AM and 3:00 AM on June 1.</span></span>

<span data-ttu-id="25bae-143">Þegar verslunin bókar uppgjör sitt fyrir lok viðskiptadagsins, inniheldur framkölluð sölupöntun allar færslur sem skráðar voru á opnunartímanum 8:00 til 3:00, þrátt fyrir að færslurnar hafi átt sér stað á tveimur dögum, 31. maí og 1. júní.</span><span class="sxs-lookup"><span data-stu-id="25bae-143">When the store posts its statement for the close of the business day, the sales order that is generated includes all transactions that were recorded between the business hours of 8:00 AM and 3:00 AM, even though the transactions occurred on two days, May 31 and June 1.</span></span>

<span data-ttu-id="25bae-144">Ef gátreiturinn **Bóka sem viðskiptadag** er hreinsaður fyrir sömu verslun, eru aðskildar sölupantanir framkallaðar þegar verslunin bókar uppgjör sitt fyrir lok viðskiptadagsins.</span><span class="sxs-lookup"><span data-stu-id="25bae-144">If the **Post as business day** check box is cleared for the same store, separate sales orders are generated when the store posts its statement for the close of the business day.</span></span> <span data-ttu-id="25bae-145">Ein sölupöntun inniheldur færslur sem voru skráðar á opnunartímanum 8:00 til miðnættis þann 31. maí og önnur sölupöntun inniheldur færslur sem skráðar voru á opnunartímanum 0:01 til 3:00 þann 1. júní.</span><span class="sxs-lookup"><span data-stu-id="25bae-145">One sales order includes the transactions that were recorded between the business hours of 8:00 AM and midnight on May 31, and the second sales order includes the transactions that were recorded between the business hours of 12:01 AM and 3:00 AM on June 1.</span></span>

> [!NOTE]
> <span data-ttu-id="25bae-146">Áður en hægt er að stofna uppgjör, ætti að loka vaktir á tímabili yfirlitsins.</span><span class="sxs-lookup"><span data-stu-id="25bae-146">Before you can create statements, you should close the shifts in the statement period.</span></span>

### <a name="post-the-statement"></a><span data-ttu-id="25bae-147">Bókið uppgjörið.</span><span class="sxs-lookup"><span data-stu-id="25bae-147">Post the statement</span></span>

<span data-ttu-id="25bae-148">Þegar yfirlit er bókað, eru sölupantanir og reikninga stofnaðir fyrir smásölu í yfirlitinu.</span><span class="sxs-lookup"><span data-stu-id="25bae-148">When you post a statement, sales orders and invoices are created for the retail sales in the statement.</span></span>

- <span data-ttu-id="25bae-149">Staðgreiddum sölum er safnað saman í eina sölupöntun og eru reikningsfærðar fyrir sjálfgefinn viðskiptavin sem úthlutaður er versluninni.</span><span class="sxs-lookup"><span data-stu-id="25bae-149">Cash and carry sales are aggregated onto one sales order, and are invoiced for the default customer who is assigned to the store.</span></span>
- <span data-ttu-id="25bae-150">Smásala þar sem viðskiptavinur var bætt við færslu í Microsoft Dynamics 365 for Retail sölustöðum mynda sérstaka sölupantanir og reikninga, einn fyrir hvert einkvæmt kenni viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="25bae-150">Retail sales for which a customer was added to the transaction in Microsoft Dynamics 365 for Retail POS generate separate sales orders and invoices, one for each unique customer.</span></span>

<span data-ttu-id="25bae-151">Greiðslubækur eru sjálfkrafa stofnaðar fyrir greiðslur í uppgjörinu og á birgðirnar eru uppfærðar fyrir verslun á sölustaður.</span><span class="sxs-lookup"><span data-stu-id="25bae-151">Payment journals are automatically created for the payments in the statement, and the inventory is updated for the POS store.</span></span>
