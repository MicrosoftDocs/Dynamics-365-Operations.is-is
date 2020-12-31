---
title: Setja upp leigubækur
description: Þetta efnisatriði lýsir upplýsingum sem unnið er með í leigubókum. Leigubækur innihalda bókhaldsreglur sem ákvarða hvernig leigan er gjaldfærð í kerfinu.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 28518341544327f1983e563b719b0f455b6e1c43
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4444579"
---
# <a name="set-up-lease-books"></a><span data-ttu-id="89af2-104">Setja upp leigubækur</span><span class="sxs-lookup"><span data-stu-id="89af2-104">Set up lease books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89af2-105">Leigubækur innihalda bókhaldsreglur sem ákvarða hvernig leigan er gjaldfærð í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="89af2-105">Lease books contain the accounting policies that determine how a lease is accounted for in the system.</span></span> <span data-ttu-id="89af2-106">Til viðbótar við bókhald á grundvelli reiðufjár styður eignarleiga eftirfarandi staðla:</span><span class="sxs-lookup"><span data-stu-id="89af2-106">In addition to cash basis accounting, Asset leasing supports the following standards:</span></span>

- <span data-ttu-id="89af2-107">Almennt viðurkenndar reikningsskilareglur í Bandaríkjunum (US GAAP)</span><span class="sxs-lookup"><span data-stu-id="89af2-107">Generally Accepted Accounting Principles in the United States (US GAAP)</span></span>
- <span data-ttu-id="89af2-108">Efnisatriði um skráningarkerfi reikningsskilastaðla 842 (ASC 842)</span><span class="sxs-lookup"><span data-stu-id="89af2-108">Accounting Standards Codification Topic 842 (ASC 842)</span></span>
- <span data-ttu-id="89af2-109">ASC 840</span><span class="sxs-lookup"><span data-stu-id="89af2-109">ASC 840</span></span>
- <span data-ttu-id="89af2-110">Alþjóðlegum reikningsskilastaðli 16 (IFRS 16)</span><span class="sxs-lookup"><span data-stu-id="89af2-110">International Financial Reporting Standard 16 (IFRS 16)</span></span>
- <span data-ttu-id="89af2-111">Alþjóðlegum reikningsskilastaðli 17 (IAS 17)</span><span class="sxs-lookup"><span data-stu-id="89af2-111">International Accounting Standard 17 (IAS 17)</span></span>

<span data-ttu-id="89af2-112">Fylgdu þessum skrefum til að búa til leigubók.</span><span class="sxs-lookup"><span data-stu-id="89af2-112">To create a lease book, follow these steps.</span></span>

1. <span data-ttu-id="89af2-113">Opnið **Eignarleiga \> Uppsetning \> Leigubækur**.</span><span class="sxs-lookup"><span data-stu-id="89af2-113">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="89af2-114">Veljið **Nýtt** til að bæta við bók.</span><span class="sxs-lookup"><span data-stu-id="89af2-114">Select **New** to add a book.</span></span>
3. <span data-ttu-id="89af2-115">Stilltu eftirfarandi reiti.</span><span class="sxs-lookup"><span data-stu-id="89af2-115">Set the following fields.</span></span>

    | <span data-ttu-id="89af2-116">Nafn</span><span class="sxs-lookup"><span data-stu-id="89af2-116">Name</span></span>                                     | <span data-ttu-id="89af2-117">lýsing</span><span class="sxs-lookup"><span data-stu-id="89af2-117">Description</span></span> |
    |------------------------------------------|-------------|
    | <span data-ttu-id="89af2-118">Bókunarlag</span><span class="sxs-lookup"><span data-stu-id="89af2-118">Posting layer</span></span>                            | <span data-ttu-id="89af2-119">Veljið bókunarlagið sem á að nota.</span><span class="sxs-lookup"><span data-stu-id="89af2-119">Select the posting layer to use.</span></span> <span data-ttu-id="89af2-120">Sérver bók sem tengd er leigu er uppsett fyrir ákveðið bókunarlag.</span><span class="sxs-lookup"><span data-stu-id="89af2-120">Each book that is attached to a lease is set up for a specific posting layer.</span></span> <span data-ttu-id="89af2-121">Hvert bókunarlag er með mismunandi bókunartilgang.</span><span class="sxs-lookup"><span data-stu-id="89af2-121">Each posting layer has different posting purposes.</span></span> |
    | <span data-ttu-id="89af2-122">Gerð leigu</span><span class="sxs-lookup"><span data-stu-id="89af2-122">Lease type</span></span>                               | <span data-ttu-id="89af2-123">Veljið hvort gerð leigusamningsins verði flokkuð sjálfkrafa eða skilgreind fyrirfram sem fjármögnunar- eða rekstrarleigusamningur.</span><span class="sxs-lookup"><span data-stu-id="89af2-123">Select whether the lease should be classified automatically, or whether it should be predefined as a finance or operating lease.</span></span> |
    | <span data-ttu-id="89af2-124">Bókhaldsrammi</span><span class="sxs-lookup"><span data-stu-id="89af2-124">Accounting framework</span></span>                     | <span data-ttu-id="89af2-125">Velja rammann sem tengist bókinni.</span><span class="sxs-lookup"><span data-stu-id="89af2-125">Select the framework that is associated with the book.</span></span> |
    | <span data-ttu-id="89af2-126">Leigutími/Uppsetning nýtingartíma</span><span class="sxs-lookup"><span data-stu-id="89af2-126">Lease term/Useful life Set Up</span></span>          | <span data-ttu-id="89af2-127">Forritið flokkar leigusamninginn sem fjármögnunarleigusamning ef gerð leigusamnings er stillt á **Sjálfvirka stillingu** og ef leigutíminn á nýtingartíma eignar er lengri en eða jafnt og prósentuhlutfallið sem fært er inn í þetta svæði.</span><span class="sxs-lookup"><span data-stu-id="89af2-127">The system will classify the lease as a finance lease if the lease type is set to **Automatic**, and if the lease term over useful life of the asset is greater than or equal to the percentage entered in this field.</span></span>  |
    | <span data-ttu-id="89af2-128">Uppsetning á núvirði / gangvirði eignar</span><span class="sxs-lookup"><span data-stu-id="89af2-128">Present value / Asset fair value setup</span></span>   | <span data-ttu-id="89af2-129">Færið inn heiltölu til að skilgreina þröskuldinn sem mun ákvarða gerð leigunnar.</span><span class="sxs-lookup"><span data-stu-id="89af2-129">Enter a whole number to define the threshold that will determine the lease type.</span></span> <span data-ttu-id="89af2-130">Ef núvirði lágmarks leigugreiðslna í framtíðinni er hærra en skilgreint virði notanda í uppsetningu bókarinnar og ef flokkun leigusamnings bókarinnar er stillt á sjálfvirka stillingu flokkar kerfið leigusamninginn sem fjármögnunarleigusamning.</span><span class="sxs-lookup"><span data-stu-id="89af2-130">If the present value of future minimum lease payments is more than the user-defined value from the book setup, and if the book's lease classification is set to automatic, the system will classify the lease as a finance lease.</span></span> |
    | <span data-ttu-id="89af2-131">Skammtímaþröskuldur</span><span class="sxs-lookup"><span data-stu-id="89af2-131">Short-term threshold</span></span>                     | <span data-ttu-id="89af2-132">Sláið inn fjölda mánaða sem á að nota sem mörk fyrir skammtímaleigur.</span><span class="sxs-lookup"><span data-stu-id="89af2-132">Enter the number of months to use as a threshold for short-term leases.</span></span> <span data-ttu-id="89af2-133">Ef leigutíminn er styttri en eða jafnt og mánaðarfjöldinn sem færður er inn hér, flokkar kerfið leigusamninginn sem skammtímaleigusamning og aðferðin frestaðar leigugreiðslur verður notuð.</span><span class="sxs-lookup"><span data-stu-id="89af2-133">If the lease term is less than or equal to the number of months that you enter here, the system will classify the lease as a short-term lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="89af2-134">Mörk verðlítillar eignar</span><span class="sxs-lookup"><span data-stu-id="89af2-134">Low value threshold</span></span>                      | <span data-ttu-id="89af2-135">Færa skal inn upphæð sem á að nota sem þröskuld fyrir leigu verðlítillar eignar.</span><span class="sxs-lookup"><span data-stu-id="89af2-135">Enter an amount to use as a threshold for low-value leases.</span></span> <span data-ttu-id="89af2-136">Ef gangvirði eignar er jafnt og eða minna en gildi sem er slegið inn hér mun kerfið flokka leigusamninginn sem verðlítinn og frestaðar leigugreiðslur verða notaðar.</span><span class="sxs-lookup"><span data-stu-id="89af2-136">If the fair value of the asset is less than or equal or the value that you enter here, the system will classify the lease as a low-value lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="89af2-137">Greiða lánardrottni</span><span class="sxs-lookup"><span data-stu-id="89af2-137">Pay to vendor</span></span>                            | <span data-ttu-id="89af2-138">Stillið þennan valkost á **Yes** til að leyfa bókun leigugreiðslna sem reiknings á lánardrottnalykil sem tilgreindur er í hverjum leigusamningi.</span><span class="sxs-lookup"><span data-stu-id="89af2-138">Set this option to **Yes** to allow lease payments to be posted, as an invoice, to the vendor account that is specified on each lease.</span></span> <span data-ttu-id="89af2-139">Þegar leigugreiðsla er bókuð verður lánardrottnalykill kreditfærður.</span><span class="sxs-lookup"><span data-stu-id="89af2-139">When a lease payment is posted, the vendor account will be credited.</span></span> <span data-ttu-id="89af2-140">Ef þessi valkostur er stilltur á **Nei**, verður lykillinn sem er tilgreindur fyrir bókunargerðina **Leigugreiðsla** á síðunni **Færibreytur bókunargerðar** kreditfærður þess í stað.</span><span class="sxs-lookup"><span data-stu-id="89af2-140">If this option is set to **No**, the account that is specified for the **Lease payment** posting type on the **Lease posting parameters** page will be credited instead.</span></span> |
