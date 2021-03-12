---
title: Bakfæra bókaðar leigufærslur
description: Þetta efnisatriði útskýrir hvernig á að bakfæra bókuð leiguviðskipti. Hægt er að bakfæra allar færslur sem eru stofnaðar í gegnum Eignaleigu.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3e4908ddab2650e5ff7e4a28bf916604d165d08c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969529"
---
# <a name="reverse-posted-lease-transactions"></a><span data-ttu-id="828a3-104">Bakfæra bókaðar leigufærslur</span><span class="sxs-lookup"><span data-stu-id="828a3-104">Reverse posted lease transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="828a3-105">Hægt er að bakfæra allar færslur sem eru stofnaðar í gegnum Eignaleigu.</span><span class="sxs-lookup"><span data-stu-id="828a3-105">Any transaction that is created through Asset leasing can be reversed.</span></span> <span data-ttu-id="828a3-106">Færslur sem eru bakfærðar gegnum Eignaleigu uppfæra gögn leigusamnings.</span><span class="sxs-lookup"><span data-stu-id="828a3-106">Transactions that are reversed through Asset leasing update your lease data.</span></span> <span data-ttu-id="828a3-107">Þar af leiðandi uppfæra þau einnig bókfært virði leiguskuldbindingarinnar og afnotarétt af eign.</span><span class="sxs-lookup"><span data-stu-id="828a3-107">Therefore, they also update the carrying values of the lease liability and right-of-use (ROU) asset.</span></span>

<span data-ttu-id="828a3-108">Til að stofna bakfærslu fyrir leigu skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="828a3-108">To create a reversing transaction for a lease, follow these steps.</span></span>

1. <span data-ttu-id="828a3-109">Á annað hvort **eignafærslur** síðu eða **skuldafærslum** síðu, veljið færsluna og veljið svo **Bakfæra**.</span><span class="sxs-lookup"><span data-stu-id="828a3-109">On either the **Asset transactions** page or the **Liability transactions** page, select the transaction, and then select **Reverse transaction**.</span></span>
2. <span data-ttu-id="828a3-110">Í svarglugganum sem birtist er hægt að breyta dagsetningunni þegar bakfærsla verður bókuð.</span><span class="sxs-lookup"><span data-stu-id="828a3-110">In the dialog box that appears, you can edit the date when the reversing entry will be posted.</span></span> <span data-ttu-id="828a3-111">Sjálfgefið er að reiturinn **Dagsetning** er stilltur á bókunardagsetningu færslunnar sem var valin.</span><span class="sxs-lookup"><span data-stu-id="828a3-111">By default, the **Date** field is set to the transaction posting date of the transaction that you selected.</span></span> <span data-ttu-id="828a3-112">Ekki er hægt að bóka bakfærsluna á undan upphaflegu bókunardagsetningu valdrar færslu.</span><span class="sxs-lookup"><span data-stu-id="828a3-112">The reversing entry can't be posted earlier than the original posting date of the selected transaction.</span></span>
3. <span data-ttu-id="828a3-113">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="828a3-113">Select **OK**.</span></span> <span data-ttu-id="828a3-114">Færslubókarfærsla er bókuð sem bakfærir færslunni sem var valin.</span><span class="sxs-lookup"><span data-stu-id="828a3-114">A journal entry is posted that reverses the entry that you selected.</span></span> <span data-ttu-id="828a3-115">Bakfærslan er sýnd í **Eignafærslum** eða **skuldafærslum** síðu og nettósamtala núverandi stöðu sem birtist á síðunni er uppfærð.</span><span class="sxs-lookup"><span data-stu-id="828a3-115">The reversal is shown on the **Asset transactions** or **Liability transactions** page, and the net total of the current balance that is shown on the page is updated.</span></span>

<span data-ttu-id="828a3-116">Þegar valið er **Rakning bakfærslu** birtist svargluggi sem sýnir bæði upprunalegu færslurnar og bakfærðu færslurnar ásamt tengdu númeri sem er þekkt sem *rakningarnúmer*.</span><span class="sxs-lookup"><span data-stu-id="828a3-116">When you select **Reverse tracing**, a dialog box appears that shows both the original transactions and the reversed transactions, together with a linked number that is known as a *trace number*.</span></span> <span data-ttu-id="828a3-117">Til að gera bakfærslurnar auðveldari að skilja og bæta sýnileika er einnig hægt að rekja bakfærslur með því að nota leiguáætlanir.</span><span class="sxs-lookup"><span data-stu-id="828a3-117">To make the reversals easier to understand and to improve visibility, you can also track reversals by using the lease schedules.</span></span>

<span data-ttu-id="828a3-118">**Nýjasta færslubókarnúmer** í reitnum **Áætlun** sýnir færslubókarnúmer færslna.</span><span class="sxs-lookup"><span data-stu-id="828a3-118">The **Latest journal number** field on the **Schedule** page shows the journal numbers of transactions.</span></span> <span data-ttu-id="828a3-119">Þegar færsla er bakfærð er þessi reitur uppfærður með færslubókarnúmeri bakfærslu.</span><span class="sxs-lookup"><span data-stu-id="828a3-119">When a transaction is reversed, this field is updated with the journal number of a reversing transaction.</span></span> <span data-ttu-id="828a3-120">Þar að auki er gátreiturinn **Bakfært** valinn til að gefa til kynna að færslan sé bakfærð og reiturinn **Bókað** er valinn.</span><span class="sxs-lookup"><span data-stu-id="828a3-120">Additionally, the **Reversed** check box is selected to indicate that the transaction is reversed, and the **Posted** field is selected.</span></span>

## <a name="revoke-a-reversed-transaction"></a><span data-ttu-id="828a3-121">Afturkalla bakfærða færslu</span><span class="sxs-lookup"><span data-stu-id="828a3-121">Revoke a reversed transaction</span></span>

<span data-ttu-id="828a3-122">Til að afturkalla bakfærða færslu skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="828a3-122">To revoke a reversed transaction, follow these steps.</span></span>

1. <span data-ttu-id="828a3-123">Á annaðhvort síðunni **Áætlun** eða **Færslur** skal velja upprunalegu færsluna.</span><span class="sxs-lookup"><span data-stu-id="828a3-123">On either the **Schedule** page or the **Transactions** page, select the original transaction.</span></span>
2. <span data-ttu-id="828a3-124">Fylgið einu af eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="828a3-124">Follow one of these steps:</span></span>

    - <span data-ttu-id="828a3-125">Ef færslan var valin á **Áætlun** síðu skal fylgja skrefunum til að stofna færslubók í [stofna mánaðarlegar færslubókarfærslur í runu](create-monthly-journals-batch.md).</span><span class="sxs-lookup"><span data-stu-id="828a3-125">If you selected the transaction on the **Schedule** page, follow the steps for creating a journal in [Create monthly journal entries in a batch](create-monthly-journals-batch.md).</span></span> <span data-ttu-id="828a3-126">Notandi þarf að bóka færslubókina handvirkt.</span><span class="sxs-lookup"><span data-stu-id="828a3-126">You must manually post the journal.</span></span>
    - <span data-ttu-id="828a3-127">Ef færslan var valin á **Færslur** síðunni skal velja **Bakfæra**.</span><span class="sxs-lookup"><span data-stu-id="828a3-127">If you selected the transaction on the **Transactions** page, select **Reverse transaction**.</span></span> <span data-ttu-id="828a3-128">Þú færð skilaboð sem segir til um að afturköllun sé afturkölluð fyrir fyrri bakfærslu og að þú getir breytt bókunardagsetningunni fyrir þessa afturköllun.</span><span class="sxs-lookup"><span data-stu-id="828a3-128">You receive a message that states that this revocation is a revocation of an earlier reversal, and that you can edit the posting date for this revocation.</span></span> <span data-ttu-id="828a3-129">Hins vegar hafa almennar viðskiptaprófanir áhrif á dagsetningarnar sem hægt er að færa inn í reitinn **Dagsetning**.</span><span class="sxs-lookup"><span data-stu-id="828a3-129">However, general business validations affect the dates that can be entered in the **Date** field.</span></span> 

3. <span data-ttu-id="828a3-130">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="828a3-130">Select **OK**.</span></span> <span data-ttu-id="828a3-131">Færslubókarfærsla er bókuð sem bakfærir færslunni sem var valin.</span><span class="sxs-lookup"><span data-stu-id="828a3-131">A journal entry is posted that reverses the entry that you selected.</span></span> <span data-ttu-id="828a3-132">Bakfærslan er sýnd á **Færslur** síðunni og núverandi staða nettósamtölu er endurheimt aftur í það sem hún var fyrir fyrstu bakfærsluna.</span><span class="sxs-lookup"><span data-stu-id="828a3-132">The reversal is shown on the **Transactions** page, and the net total current balance is restored to what it was before the first reversal.</span></span> <span data-ttu-id="828a3-133">Þess vegna hafa áhrifin sem bakfærslan hafði á stöðuna verið neituð.</span><span class="sxs-lookup"><span data-stu-id="828a3-133">Therefore, the impact that the reversal had on the balances is negated.</span></span>

<span data-ttu-id="828a3-134">Þegar valið er **Rekja bakfærslu** birtist svargluggi sem sýnir bæði upprunalegu færslurnar og bakfærðu færslurnar ásamt tengdu rakningarnúmeri.</span><span class="sxs-lookup"><span data-stu-id="828a3-134">When you select **Reverse tracing**, a dialog box appears that shows both the original transactions and the reversed transactions, together with a linked trace number.</span></span>

<span data-ttu-id="828a3-135">Einnig er hægt að rekja afturköllun með því að nota viðeigandi **Áætlanir** síðu.</span><span class="sxs-lookup"><span data-stu-id="828a3-135">You can also track revocations by using the appropriate **Schedules** page.</span></span> <span data-ttu-id="828a3-136">Reiturinn **Bakfæra** er hreinsaður, en reitnum **Bókuð færslubók** er valinn.</span><span class="sxs-lookup"><span data-stu-id="828a3-136">The **Reverse** field is cleared, whereas the **Journal posted** field is selected.</span></span> <span data-ttu-id="828a3-137">Þar að auki er reiturinn **Nýjasta færslubókarnúmerið** uppfærður með færslubókarnúmeri afturköllunar og **Færslubókarnúmer** reiturinn er uppfært með númeri bakfærslubókar.</span><span class="sxs-lookup"><span data-stu-id="828a3-137">Additionally, the **Latest journal number** field is updated with the journal number of the revocation transaction, and the **Journal number** field is updated with the reversal journal number.</span></span>
