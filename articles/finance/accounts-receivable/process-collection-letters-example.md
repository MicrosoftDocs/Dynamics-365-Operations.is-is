---
title: Dæmi um úrvinnslu innheimtubréfs
description: Þetta efnisatriði fer í gegnum dæmi sem sýnir ferlið við stofnun, prentun og bókun innheimtubréfa.
author: JodiChristiansen
ms.date: 02/03/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 1b80532463d86dd59b867fca2ee24675396ce717
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826348"
---
# <a name="process-collection-letters-example"></a><span data-ttu-id="2ba32-103">Dæmi um úrvinnslu innheimtubréfs</span><span class="sxs-lookup"><span data-stu-id="2ba32-103">Process collection letters example</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2ba32-104">Þetta efnisatriði fer í gegnum dæmi sem sýnir ferlið við stofnun, prentun og bókun innheimtubréfa.</span><span class="sxs-lookup"><span data-stu-id="2ba32-104">This topic goes through an example that shows the process of creating, printing, and posting collection letters.</span></span> <span data-ttu-id="2ba32-105">Þetta dæmi byggist á valkostinum **Hunsa greiðslur og kreditnótur þegar kóði innheimtubréfs er reiknaður út** í Skuldir og innheimta.</span><span class="sxs-lookup"><span data-stu-id="2ba32-105">The example is based on the **Ignore payments and credit memos when calculating collection letter code** option in Credit and collections.</span></span> <span data-ttu-id="2ba32-106">Það notar gögn úr sýnifyrirtækinu USMF og nýjan viðskiptavin, US-045.</span><span class="sxs-lookup"><span data-stu-id="2ba32-106">It uses data in the USMF demo company and a new customer, US-045.</span></span>

<span data-ttu-id="2ba32-107">Til að hefjast handa skal fara í **Viðskiptakröfur \> Viðskiptavinir \> Allir viðskiptavinir**, velja **Nýr** og síðan færa inn nauðsynlegar upplýsingar til að stofna viðskiptavin US-045.</span><span class="sxs-lookup"><span data-stu-id="2ba32-107">To begin, go to **Accounts receivable \> Customers \> All customers**, select **New**, and then enter the required information to create customer US-045.</span></span>

<span data-ttu-id="2ba32-108">Þegar því er lokið skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="2ba32-108">When you've finished, follow these steps.</span></span>

1. <span data-ttu-id="2ba32-109">Farið í **Skuldir og innheimta \> Innheimtubréf \> Uppsetning innheimtubréfaraðar** og setjið upp innheimtubréfaröðina eins og sýnt er í eftirfarandi töflu sem er úthlutað á bókunarreglu viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="2ba32-109">Go to **Credit and collections \> Collection letter \> Setup collection letter sequence**, and set up the collection letter sequence as shown in the following table that is assigned to the customer posting profile.</span></span>

|     <span data-ttu-id="2ba32-110">Innheimtubréfaflokkur</span><span class="sxs-lookup"><span data-stu-id="2ba32-110">Collection   letter code</span></span>      |     <span data-ttu-id="2ba32-111">lýsing</span><span class="sxs-lookup"><span data-stu-id="2ba32-111">Description</span></span>                           |     <span data-ttu-id="2ba32-112">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="2ba32-112">Currency</span></span>      |     <span data-ttu-id="2ba32-113">Aðallykill</span><span class="sxs-lookup"><span data-stu-id="2ba32-113">Main   account</span></span>        |     <span data-ttu-id="2ba32-114">Gjald í gjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="2ba32-114">Fee   in currency</span></span>     |     <span data-ttu-id="2ba32-115">Lágmark yfir</span><span class="sxs-lookup"><span data-stu-id="2ba32-115">Minimum   over</span></span>        |     <span data-ttu-id="2ba32-116">Dagar útilokunar</span><span class="sxs-lookup"><span data-stu-id="2ba32-116">Days   Block</span></span>      |
|---------------------------------  |---------------------------------------    |-----------------  |-----------------------    |-------------------------- |-----------------------    |---------------------  |
|     <span data-ttu-id="2ba32-117">Innheimtubréf 1</span><span class="sxs-lookup"><span data-stu-id="2ba32-117">Collection   letter 1</span></span>         |     <span data-ttu-id="2ba32-118">Önnur tilkynning með þóknun</span><span class="sxs-lookup"><span data-stu-id="2ba32-118">Second   notification with fee</span></span>        |     <span data-ttu-id="2ba32-119">USD</span><span class="sxs-lookup"><span data-stu-id="2ba32-119">USD</span></span>           |                           |     <span data-ttu-id="2ba32-120">0,00</span><span class="sxs-lookup"><span data-stu-id="2ba32-120">0.00</span></span>                  |     <span data-ttu-id="2ba32-121">0,00</span><span class="sxs-lookup"><span data-stu-id="2ba32-121">0.00</span></span>                  |     <span data-ttu-id="2ba32-122">2</span><span class="sxs-lookup"><span data-stu-id="2ba32-122">2</span></span>                 |
|     <span data-ttu-id="2ba32-123">Innheimtubréf 2</span><span class="sxs-lookup"><span data-stu-id="2ba32-123">Collection   letter 2</span></span>         |     <span data-ttu-id="2ba32-124">Önnur tilkynning með þóknun</span><span class="sxs-lookup"><span data-stu-id="2ba32-124">Second   notification with fee</span></span>        |     <span data-ttu-id="2ba32-125">USC</span><span class="sxs-lookup"><span data-stu-id="2ba32-125">USC</span></span>           |     <span data-ttu-id="2ba32-126">403150</span><span class="sxs-lookup"><span data-stu-id="2ba32-126">403150</span></span>                |     <span data-ttu-id="2ba32-127">20.00</span><span class="sxs-lookup"><span data-stu-id="2ba32-127">20.00</span></span>                 |     <span data-ttu-id="2ba32-128">10,00</span><span class="sxs-lookup"><span data-stu-id="2ba32-128">10.00</span></span>                 |     <span data-ttu-id="2ba32-129">3</span><span class="sxs-lookup"><span data-stu-id="2ba32-129">3</span></span>                 |
|     <span data-ttu-id="2ba32-130">Innheimta</span><span class="sxs-lookup"><span data-stu-id="2ba32-130">Collection</span></span>                    |     <span data-ttu-id="2ba32-131">Lokatilkynning með þóknun</span><span class="sxs-lookup"><span data-stu-id="2ba32-131">Final   notification with fee</span></span>         |     <span data-ttu-id="2ba32-132">USD</span><span class="sxs-lookup"><span data-stu-id="2ba32-132">USD</span></span>           |     <span data-ttu-id="2ba32-133">403150</span><span class="sxs-lookup"><span data-stu-id="2ba32-133">403150</span></span>                |     <span data-ttu-id="2ba32-134">50.00</span><span class="sxs-lookup"><span data-stu-id="2ba32-134">50.00</span></span>                 |     <span data-ttu-id="2ba32-135">100.00</span><span class="sxs-lookup"><span data-stu-id="2ba32-135">100.00</span></span>                |     <span data-ttu-id="2ba32-136">15</span><span class="sxs-lookup"><span data-stu-id="2ba32-136">15</span></span>                |

<span data-ttu-id="2ba32-137">Eftirfarandi mynd sýnir upplýsingarnar sem eru í töflunni eins og þær myndu birtast á síðunni **Innheimtubréf**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-137">The following illustration shows the information that's in the table as it would appear on the **Collection letters** page.</span></span> 

<span data-ttu-id="2ba32-138">[![Innheimtubréfaröð sett upp](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span><span class="sxs-lookup"><span data-stu-id="2ba32-138">[![Setting up a collection letter sequence](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span></span>

 <span data-ttu-id="2ba32-139">Nú þarf að stilla þessar tvær færibreytur sem eru nauðsynlegar fyrir þetta dæmi.</span><span class="sxs-lookup"><span data-stu-id="2ba32-139">You must now set the two parameters that are required for this example.</span></span>

2. <span data-ttu-id="2ba32-140">Farið í **Skuldir og innheimta \> Uppsetning \> Færibreytur viðskiptakrafna** og fylgjið þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="2ba32-140">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and follow these steps:</span></span>

    1. <span data-ttu-id="2ba32-141">Í flipanum **Innheimtur** skal stilla valkostinn **Hunsa greiðslur og kreditnótur þegar kóði innheimtubréfs er reiknaður út** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-141">On the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **Yes**.</span></span>
    2. <span data-ttu-id="2ba32-142">Ganga skal úr skugga um að reiturinn **Stofna innheimtubréf eftir** sé stilltur á **Viðskiptavinur**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-142">Make sure that the **Create collection letter per** field is set to **Customer**.</span></span>

    <span data-ttu-id="2ba32-143">[![Færibreytur viðskiptakrafna settar upp fyrir innheimtu skulda](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span><span class="sxs-lookup"><span data-stu-id="2ba32-143">[![Setting Accounts receivable parameters for Credit collections](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span></span>

3. <span data-ttu-id="2ba32-144">Farið í **Viðskiptakröfur \> Reikningar \> Allir reikningar með frjálsum texta**, veljið **Nýr** og fylgið því næst þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="2ba32-144">Go to **Accounts receivable \> Invoices \> All free text invoices**, select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="2ba32-145">Í reitnum **Viðskiptavinalykill** skal velja **US-045**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-145">In the **Customer account** field select **US-045**.</span></span>
    2. <span data-ttu-id="2ba32-146">Í reitinn **Reikningsdagsetning** skal slá inn **1/15/2021**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-146">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="2ba32-147">Í reitinn **Gjalddagi** skal slá inn **1/16/2021**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-147">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="2ba32-148">Í flýtiflipann **Reikningslínur**, í reitinn **Aðallykill**, skal færa inn **401100**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-148">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="2ba32-149">Í reitinn **Einingarverð** skal slá inn **500.00**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-149">In the **Unit price** field, enter **500.00**.</span></span>
    6. <span data-ttu-id="2ba32-150">Veldu **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-150">Select **Post**.</span></span>

    <span data-ttu-id="2ba32-151">Nú skal færa inn tvær kreditnótur fyrir viðskiptavininn.</span><span class="sxs-lookup"><span data-stu-id="2ba32-151">You must now enter two credit notes for the customer.</span></span>

4. <span data-ttu-id="2ba32-152">Veljið **Ný** og fylgið síðan þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="2ba32-152">Select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="2ba32-153">Í reitnum **Viðskiptavinalykill** skal velja **US-045**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-153">In the **Customer account** field, select **US-045**.</span></span>
    2. <span data-ttu-id="2ba32-154">Í reitinn **Reikningsdagsetning** skal slá inn **1/15/2021**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-154">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="2ba32-155">Í reitinn **Gjalddagi** skal slá inn **1/16/2021**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-155">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="2ba32-156">Í flýtiflipann **Reikningslínur**, í reitinn **Aðallykill**, skal færa inn **401100**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-156">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="2ba32-157">Í reitinn **Einingarverð** skal slá inn **-100,00**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-157">In the **Unit price** field, enter **-100.00**.</span></span>
    6. <span data-ttu-id="2ba32-158">Veldu **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-158">Select **Post**.</span></span>

5. <span data-ttu-id="2ba32-159">Endurtakið skref 4, en færið inn **-200,00** í reitinn **Einingarverð**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-159">Repeat step 4, but enter **-200.00** in the **Unit price** field.</span></span>
6. <span data-ttu-id="2ba32-160">Farið í **Viðskiptakröfur \> Viðskiptavinir \> Allir viðskiptavinir** og veljið viðskiptavininn **US-045**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-160">Go to **Accounts receivable \> Customers \> All customers**, and select customer **US-045**.</span></span> <span data-ttu-id="2ba32-161">Á aðgerðasvæðinu skal síðan velja **Færslur \> Færslur** til að fara yfir færslur viðskiptavina sem voru bókaðar hér áður.</span><span class="sxs-lookup"><span data-stu-id="2ba32-161">Then, on the Action Pane, select **Transactions \> Transactions** to review the customer transactions that you posted earlier.</span></span>

    <span data-ttu-id="2ba32-162">[![Bókaðar færslur viðskiptavina yfirfarnar](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span><span class="sxs-lookup"><span data-stu-id="2ba32-162">[![Reviewing the posted customer transactions](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span></span>

    <span data-ttu-id="2ba32-163">Nú þarf að stofna innheimtubréf fyrir viðskiptavin US-045.</span><span class="sxs-lookup"><span data-stu-id="2ba32-163">You must now create collection letters for customer US-045.</span></span>

7. <span data-ttu-id="2ba32-164">Farið í **Skuldir og innheimta \> Innheimtubréf \> Stofna innheimtubréf** og fylgið þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="2ba32-164">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="2ba32-165">Stillið valkostina **Reikningur** og **Kreditnóta** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-165">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="2ba32-166">Sjálfgefið er að reiturinn **Innheimtubréf** sé stilltur á **Innheimta eftir viðskiptavini**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-166">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="2ba32-167">Í reitinn **Dagsetning innheimtubréfs** skal slá inn **1/19/2021**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-167">In the **Collection letter date** field, enter **1/19/2021**.</span></span>
    3. <span data-ttu-id="2ba32-168">Í flýtiflipanum **Færslur til að taka með** skal velja **Sía** og því næst, í reitnum **Viðskiptavinalykill**, skal bæta við viðskiptavini **US-045**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-168">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="2ba32-169">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-169">Select **OK**.</span></span>
    5. <span data-ttu-id="2ba32-170">Veljið **Í lagi** til að stofna innheimtubréf.</span><span class="sxs-lookup"><span data-stu-id="2ba32-170">Select **OK** to create collection letters.</span></span>

8. <span data-ttu-id="2ba32-171">Farið í **Skuldir og innheimta \> Innheimtubréf \> Yfirfara og vinna úr innheimtubréfum** og fylgið þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="2ba32-171">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="2ba32-172">Athugið að kóði innheimtubréfs í bæði haus og færslulínum er **Innheimtubréf 1** vegna þess að þetta er fyrsta innheimtubréfið í röðinni.</span><span class="sxs-lookup"><span data-stu-id="2ba32-172">Notice that the collection letter code on both the header and the transaction lines is **Collection letter 1**, because this collection letter is the first collection letter in the sequence.</span></span> <span data-ttu-id="2ba32-173">(Til að skoða færslulínur gæti þurft að velja flýtiflipann **Færslur**.)</span><span class="sxs-lookup"><span data-stu-id="2ba32-173">(To view the transaction lines, you might have to select the **Transactions** FastTab.)</span></span>

   <span data-ttu-id="2ba32-174">[![Staðfesting á því að sami kóði innheimtubréfs komi fram í haus og í línum](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span><span class="sxs-lookup"><span data-stu-id="2ba32-174">[![Verifying that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span></span>

    2. <span data-ttu-id="2ba32-175">Á aðgerðasvæðinu skal velja **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-175">On the Action Pane, select **Post**.</span></span>
    3. <span data-ttu-id="2ba32-176">Í reitinn **Bókunardagssetning** skal færa inn **1/19/2021**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-176">In the **Posting date** field, enter **1/19/2021**.</span></span>

    <span data-ttu-id="2ba32-177">Nú þarf að stofna innheimtubréf aftur fyrir viðskiptavin US-045.</span><span class="sxs-lookup"><span data-stu-id="2ba32-177">You must now create collection letters again for customer US-045.</span></span>

9. <span data-ttu-id="2ba32-178">Farið í **Skuldir og innheimta \> Innheimtubréf \> Stofna innheimtubréf** og fylgið þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="2ba32-178">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="2ba32-179">Stillið valkostina **Reikningur** og **Kreditnóta** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-179">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="2ba32-180">Sjálfgefið er að reiturinn **Innheimtubréf** sé stilltur á **Innheimta eftir viðskiptavini**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-180">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="2ba32-181">Í reitinn **Dagsetning innheimtubréfs** skal slá inn **1/23/2021**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-181">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="2ba32-182">Í flýtiflipanum **Færslur til að taka með** skal velja **Sía** og því næst, í reitnum **Viðskiptavinalykill**, skal bæta við viðskiptavini **US-045**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-182">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="2ba32-183">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-183">Select **OK**.</span></span>
    5. <span data-ttu-id="2ba32-184">Veljið **Í lagi** til að stofna innheimtubréf.</span><span class="sxs-lookup"><span data-stu-id="2ba32-184">Select **OK** to create collection letters.</span></span>

10. <span data-ttu-id="2ba32-185">Farið í **Skuldir og innheimta \> Innheimtubréf \> Yfirfara og vinna úr innheimtubréfum** og fylgið þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="2ba32-185">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="2ba32-186">Takið eftir að kóði innheimtubréfs í hausnum er **Innheimtubréf 1**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-186">Notice that the collection letter code on the header is **Collection letter 1**.</span></span> <span data-ttu-id="2ba32-187">Kóðinn í færslulínunum er hins vegar **Innheimtubréf 2**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-187">However, the code on the transaction lines is **Collection letter 2**.</span></span>

   <span data-ttu-id="2ba32-188">[![Staðfestir að mismunandi kóðar innheimtubréfs koma fram í haus og línum](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span><span class="sxs-lookup"><span data-stu-id="2ba32-188">[![Verifies that different collection letter codes appear on the header and the lines](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span></span>

  <span data-ttu-id="2ba32-189">Kóðarnir eru ólíkir vegna þess að valkosturinn **Hunsa greiðslur og kreditnótur þegar kóði innheimtubréfs er reiknaður út** er stilltur á **Já**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-189">The codes differ because the **Ignore payments and credit memos when calculating collection letter code** option is to **Yes**.</span></span>

  2. <span data-ttu-id="2ba32-190">Ekki bóka þetta innheimtubréf.</span><span class="sxs-lookup"><span data-stu-id="2ba32-190">Don't post this collection letter.</span></span>

11. <span data-ttu-id="2ba32-191">Farið í **Skuldir og innheimta \> Uppsetning \> Færibreytur viðskiptakrafna** og því næst í flipanum **Innheimtur** skal stilla valkostinn **Hunsa greiðslur og kreditnótur þegar kóði innheimtubréfs er reiknaður út** á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-191">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and then, on the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **No**.</span></span>

    <span data-ttu-id="2ba32-192">[![Hunsa greiðslur og kreditnótur stillt þegar valkostur fyrir útreikning innheimtubréfakóða er stilltur á nei](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span><span class="sxs-lookup"><span data-stu-id="2ba32-192">[![Setting the Ignore payments and credit memos when calculating collection letter code option to No](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span></span>

    <span data-ttu-id="2ba32-193">Nú þarf að stofna innheimtubréf aftur fyrir viðskiptavin US-045.</span><span class="sxs-lookup"><span data-stu-id="2ba32-193">You must now create collection letters again for customer US-045.</span></span>

12. <span data-ttu-id="2ba32-194">Farið í **Skuldir og innheimta \> Innheimtubréf \> Stofna innheimtubréf** og fylgið þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="2ba32-194">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="2ba32-195">Stillið valkostina **Reikningur** og **Kreditnóta** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-195">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="2ba32-196">Sjálfgefið er að reiturinn **Innheimtubréf** sé stilltur á **Innheimta eftir viðskiptavini**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-196">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="2ba32-197">Í reitinn **Dagsetning innheimtubréfs** skal slá inn **1/23/2021**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-197">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="2ba32-198">Í flýtiflipanum **Færslur til að taka með** skal velja **Sía** og því næst, í reitnum **Viðskiptavinalykill**, skal bæta við viðskiptavini **US-045**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-198">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="2ba32-199">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-199">Select **OK**.</span></span>
    5. <span data-ttu-id="2ba32-200">Veljið **Í lagi** til að stofna innheimtubréf.</span><span class="sxs-lookup"><span data-stu-id="2ba32-200">Select **OK** to create collection letters.</span></span>

13. <span data-ttu-id="2ba32-201">Farið í **Skuldir og innheimta \> Innheimtubréf \> Yfirfara og vinna úr innheimtubréfum** og takið eftir því að kóði innheimtubréfs bæði í haus og færslulínum er **Innheimtubréf 2**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-201">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and notice that the collection letter code on both the header and the transaction lines is **Collection letter 2**.</span></span>

    <span data-ttu-id="2ba32-202">[![Sýnir aftur að sami kóði innheimtubréfs komi fram í haus og í línum](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span><span class="sxs-lookup"><span data-stu-id="2ba32-202">[![Showing again that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span></span>

    <span data-ttu-id="2ba32-203">Sami kóðinn kemur fram á báðum stöðum vegna þess að valkosturinn **Hunsa greiðslur og kreditnótur þegar kóði innheimtubréfs er reiknaður út** er stilltur á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="2ba32-203">The same code appears in both places because the **Ignore payments and credit memos when calculating collection letter code** option is now set to **No**.</span></span>
