---
title: Breyta og endurskoða færslur staðgreiðslu við afhendingu og stjórnun reiðufjár
description: Þetta efnisatriði fjallar um hvernig á að breyta og endurskoða færslur staðgreiðslu við afhendingu og stjórnun reiðufjár í Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: c809f379dbd6824542d0b1768cfbf44f37461f4c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010200"
---
# <a name="edit-and-audit-cash-and-carry-and-cash-management-transactions"></a><span data-ttu-id="f0645-103">Breyta og endurskoða færslur staðgreiðslu við afhendingu og stjórnun reiðufjár</span><span class="sxs-lookup"><span data-stu-id="f0645-103">Edit and audit cash and carry and cash management transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0645-104">Þetta efnisatriði fjallar um hvernig á að breyta og endurskoða færslur staðgreiðslu við afhendingu og stjórnun reiðufjár í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f0645-104">This topic describes how to edit and audit cash and carry and cash management transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f0645-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="f0645-105">Overview</span></span>

<span data-ttu-id="f0645-106">Dynamics 365 Commerce-viðskiptavinir nota bæði forrit fyrir sölustað frá fyrsta aðila og forrit fyrir sölustað frá þriðja aðila.</span><span class="sxs-lookup"><span data-stu-id="f0645-106">Dynamics 365 Commerce customers use both a first-party point of sale (POS) application and third-party POS applications.</span></span> <span data-ttu-id="f0645-107">Þegar forrit sölustaðar frá fyrsta aðila er notað eru færslur verslunar teknar inn í Commerce Headquarters úr rásunum með runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="f0645-107">In the case of the first-party application, store transactions are pulled into Commerce headquarters from the channels through a batch process.</span></span> <span data-ttu-id="f0645-108">Þegar notuð eru forrit frá þriðju aðilum eru færslurnar teknar inn í Commerce Headquarters með samþættingu.</span><span class="sxs-lookup"><span data-stu-id="f0645-108">In the case of third-party applications, transactions are pulled into Commerce headquarters through integration.</span></span> <span data-ttu-id="f0645-109">Þegar færslurnar hafa verið teknar inn í Commerce Headquarters verður að framkvæma samræmisathugun í báðum tilvikum.</span><span class="sxs-lookup"><span data-stu-id="f0645-109">In both cases, after transactions are pulled into Commerce headquarters, a consistency check process must be performed.</span></span> <span data-ttu-id="f0645-110">Þetta ferli keyrir margar villuleitir á færslunum og aðeins færslur sem tekst að villuleita í eru teknar inn í uppgjörið til að hægt sé að birta færslurnar í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="f0645-110">This process runs multiple validations on the transactions, and only transactions that are successfully validated are pulled into the statement so that they can be posted in Commerce headquarters.</span></span>

<span data-ttu-id="f0645-111">Færslur Commerce standast mögulega ekki villuleit af ýmsum ástæðum.</span><span class="sxs-lookup"><span data-stu-id="f0645-111">Commerce transactions might fail validation for various reasons.</span></span> <span data-ttu-id="f0645-112">Villa í samþættingarkóðanum eða söluforritinu getur valdið ósamkvæmum gögnum.</span><span class="sxs-lookup"><span data-stu-id="f0645-112">A bug in the integration code or in the POS application might cause inconsistent data.</span></span> <span data-ttu-id="f0645-113">Einnig getur notandavilla valdið ósamkvæmum gögnum.</span><span class="sxs-lookup"><span data-stu-id="f0645-113">Alternatively, a user error might cause inconsistent data.</span></span> <span data-ttu-id="f0645-114">Þegar notandi t.d. eyðir afurð eftir að hún hefur verið samstillt við rásina eða notandi lokar fjárhagstímabili án þess að bóka færslur fyrir viðkomandi tímabil.</span><span class="sxs-lookup"><span data-stu-id="f0645-114">For example, a user deletes a product after it was synced to the channel, or a user closes a fiscal period without posting transactions for that period.</span></span> <span data-ttu-id="f0645-115">Þrátt fyrir að slíkar færslur séu merktar og útilokaðar frá uppgjörunum geta færslurnar truflað daglegt bókunarferli viðskiptavinar í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="f0645-115">Although these transactions are flagged and are excluded from the statements, they can disrupt a customer's daily process of posting daily sales to the financials.</span></span> <span data-ttu-id="f0645-116">Í Commerce er hægt að breyta færslum sem standast ekki villuleit á meðan unnið er að endurskoðun á öllum breytingunum.</span><span class="sxs-lookup"><span data-stu-id="f0645-116">In Commerce, you can edit the transactions that fail validation while you also maintain an audit of all the changes.</span></span>

## <a name="edit-transactions"></a><span data-ttu-id="f0645-117">Breyta færslum</span><span class="sxs-lookup"><span data-stu-id="f0645-117">Edit transactions</span></span>

<span data-ttu-id="f0645-118">Í Commerce-útgáfu 10.0.5 er aðeins hægt að breyta staðgreiddum færslum eins og sölu- og skilafærslum.</span><span class="sxs-lookup"><span data-stu-id="f0645-118">In Commerce version 10.0.5, the only transactions that can be edited are cash and carry transactions, such as sales and returns.</span></span> <span data-ttu-id="f0645-119">Ekki er hægt að breyta pöntunum viðskiptavina og pöntunum á netinu.</span><span class="sxs-lookup"><span data-stu-id="f0645-119">Customer orders and online orders can't be edited.</span></span> <span data-ttu-id="f0645-120">Í Commerce-útgáfu 10.0.6 og nýrri útgáfum er einnig hægt að breyta reiðufjárstjórnunarfærslum.</span><span class="sxs-lookup"><span data-stu-id="f0645-120">In Commerce version 10.0.6 and later, cash management transactions can also be edited.</span></span>

<span data-ttu-id="f0645-121">Fylgja skal eftirfarandi skrefum til að breyta pöntunarfærslum í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="f0645-121">To edit transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="f0645-122">Setjið upp [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span><span class="sxs-lookup"><span data-stu-id="f0645-122">Install the [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span></span>
1. <span data-ttu-id="f0645-123">Opnið vinnusvæðið **Fjármál verslunar** í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="f0645-123">In Commerce headquarters, open the **Store financials** workspace.</span></span> <span data-ttu-id="f0645-124">Reiturinn **Bilanir við villuleit færslu** sýnir forsíað yfirlit færslusíðunnar sem stóðst ekki eina eða fleiri villuleitarreglur.</span><span class="sxs-lookup"><span data-stu-id="f0645-124">The **Transaction validation failures** tile provides a prefiltered view of the transaction page that failed one or more validation rules.</span></span>
1. <span data-ttu-id="f0645-125">Opnið færslusíðuna, veljið færsluna sem stóðst ekki villuleit, því næst **Office-innbót** og síðan **Breyta valinni færslu**.</span><span class="sxs-lookup"><span data-stu-id="f0645-125">Open the transaction page, select the record that failed validation, select **Office Add in**, and then select **Edit selected transaction**.</span></span> <span data-ttu-id="f0645-126">Excel-skrá með upplýsingum um valda færslu opnast.</span><span class="sxs-lookup"><span data-stu-id="f0645-126">An Excel file that shows the details of the selected transaction is opened.</span></span> <span data-ttu-id="f0645-127">Þessi skrá inniheldur eftirfarandi vinnublöð:</span><span class="sxs-lookup"><span data-stu-id="f0645-127">This file contains the following worksheets:</span></span>

    - <span data-ttu-id="f0645-128">**Línur** – Þetta vinnublað er með haus og afurðarlínur og tengd gögn fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="f0645-128">**Lines** – This worksheet has the header and product lines for the transaction, and related data for the transaction.</span></span>
    - <span data-ttu-id="f0645-129">**Greiðslur** – Þetta vinnublað er með upplýsingar um greiðslulínur fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="f0645-129">**Payments** – This worksheet has the details of the payment lines for the transaction.</span></span>
    - <span data-ttu-id="f0645-130">**Afslættir** – Þetta vinnublað er með afsláttartengdar upplýsingar fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="f0645-130">**Discounts** – This worksheet has the discount-related details for the transaction.</span></span>
    - <span data-ttu-id="f0645-131">**Skattar** – Þetta vinnublað er með upplýsingar um skatt sem tengist færslunni.</span><span class="sxs-lookup"><span data-stu-id="f0645-131">**Taxes** – This worksheet has the tax-related details for the transaction.</span></span>
    - <span data-ttu-id="f0645-132">**Gjöld** – Þetta vinnublað er með gjaldtengdar upplýsingar fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="f0645-132">**Charges** – This worksheet has the charges-related data for the transaction.</span></span>

1. <span data-ttu-id="f0645-133">Í Excel-skránni er viðeigandi reitum breytt og gögnunum svo hlaðið aftur upp í Commerce Headquarters með birtingaraðgerð Excel-innbótarinnar í Dynamics.</span><span class="sxs-lookup"><span data-stu-id="f0645-133">In the Excel file, modify the appropriate fields, and then upload the data back into Commerce headquarters by using the publishing functionality of the Dynamics Excel Add-in.</span></span> <span data-ttu-id="f0645-134">Breytingarnar koma fram í kerfinu þegar búið er að birta gögnin.</span><span class="sxs-lookup"><span data-stu-id="f0645-134">After the data is published, the changes will be reflected in the system.</span></span> <span data-ttu-id="f0645-135">Meðan á birtingu stendur fer engin villuleit fram á breytingunum sem notendur gera.</span><span class="sxs-lookup"><span data-stu-id="f0645-135">During publication, no validation is done for changes that users make.</span></span>
1. <span data-ttu-id="f0645-136">Hægt er að skoða alla færsluslóð breytinganna með því að velja **Skoða slóð endurskoðunar** í hausnum **Smásölufærsla** til að sjá breytingar á haus og í viðeigandi hluta og færslu á viðeigandi færslusíðu.</span><span class="sxs-lookup"><span data-stu-id="f0645-136">You can view a complete audit trail of the changes by selecting **View audit trail** in the **Retail transaction** header for the header-level changes, and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="f0645-137">Til dæmis verða allar breytingar sem tengjast sölulínum sýnilegar á síðunni **Sölufærslur** og allar breytingar sem tengjast greiðslum verða sýnilegar á síðunni **Greiðslufærslur**.</span><span class="sxs-lookup"><span data-stu-id="f0645-137">For example, all changes that are related to sales lines will be shown on the **Sales transactions** page, and all changes that are related to payments will be shown on the **Payment transactions** page.</span></span> <span data-ttu-id="f0645-138">Eftirfarandi upplýsingum um endurskoðun er haldið við fyrir breytingarnar:</span><span class="sxs-lookup"><span data-stu-id="f0645-138">The following audit details are maintained for the changes:</span></span>

    - <span data-ttu-id="f0645-139">Breytt dagsetning og tími</span><span class="sxs-lookup"><span data-stu-id="f0645-139">Modified date and time</span></span>
    - <span data-ttu-id="f0645-140">Svæði</span><span class="sxs-lookup"><span data-stu-id="f0645-140">Field</span></span>
    - <span data-ttu-id="f0645-141">Gamalt gildi</span><span class="sxs-lookup"><span data-stu-id="f0645-141">Old value</span></span>
    - <span data-ttu-id="f0645-142">Nýtt gildi</span><span class="sxs-lookup"><span data-stu-id="f0645-142">New value</span></span>
    - <span data-ttu-id="f0645-143">Breytt af</span><span class="sxs-lookup"><span data-stu-id="f0645-143">Modified by</span></span>

1. <span data-ttu-id="f0645-144">Þegar breytingarnar hafa verið gerðar og birtar skal því næst keyra aftur **Villuleita í færslum verslunar** til að staðfesta að breytingarnar sem voru gerðar séu samræmdar og gildar.</span><span class="sxs-lookup"><span data-stu-id="f0645-144">After you've made and published your changes, run **Validate store transactions** to validate that those changes are consistent and valid.</span></span>

> [!NOTE]
> <span data-ttu-id="f0645-145">Eingöngu er hægt að breyta færslum sem stóðust ekki villuleit.</span><span class="sxs-lookup"><span data-stu-id="f0645-145">You can edit only transactions that failed validation.</span></span> <span data-ttu-id="f0645-146">Þegar breyta á færslu sem staðist hefur villuleit skal breyta villuleitarstöðu færslunnar í **Villa** eða **Engin** og síðan birta breytinguna.</span><span class="sxs-lookup"><span data-stu-id="f0645-146">If you want to edit a transaction that passed validation, change the validation status of the transaction to **Error** or **None**, and then publish the change.</span></span> <span data-ttu-id="f0645-147">Því næst er hægt að breyta gögnunum í hausnum eða undirskrám færslunnar og birta hausinn eða færslurnar.</span><span class="sxs-lookup"><span data-stu-id="f0645-147">You can then edit the data on the header or in any other child records of the transaction, and publish the header or records.</span></span>

## <a name="bulk-edit-transactions-that-are-linked-to-a-statement"></a><span data-ttu-id="f0645-148">Breyta mörgum færslum í einu sem tengjast uppgjöri</span><span class="sxs-lookup"><span data-stu-id="f0645-148">Bulk-edit transactions that are linked to a statement</span></span>

<span data-ttu-id="f0645-149">Commerce-útgáfa 10.0.6 og nýrri útgáfur styðja breytingar á fjölda færslna í einu á uppgjörsstigi.</span><span class="sxs-lookup"><span data-stu-id="f0645-149">Commerce version 10.0.6 and later support the option to bulk-edit transactions at the statement level.</span></span>

<span data-ttu-id="f0645-150">Fylgja skal eftirfarandi skrefum til að breyta mörgum færslum í einu sem tengjast uppgjöri í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="f0645-150">To bulk-edit transactions that are linked to a statement in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="f0645-151">Opnið síðuna **Uppgjör** og veljið uppgjörið sem inniheldur færslurnar sem skal breyta.</span><span class="sxs-lookup"><span data-stu-id="f0645-151">Open the **Statements** page, and select the statement that contains the transactions that must be edited.</span></span>
1. <span data-ttu-id="f0645-152">Veljið hnappinn **Opna í Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="f0645-152">Select the **Open in Microsoft Office** button.</span></span>
1. <span data-ttu-id="f0645-153">Veljið einn af eftirfarandi valkostum miðað við atriðin sem þarf að breyta:</span><span class="sxs-lookup"><span data-stu-id="f0645-153">Depending on what must be edited, select one of the following options:</span></span>

    - <span data-ttu-id="f0645-154">**Breyta staðgreiddum færslum** – Þessi valkostur gerir notanda kleift að breyta öllum staðgreiddum færslum sem eru innifaldar í uppgjörinu.</span><span class="sxs-lookup"><span data-stu-id="f0645-154">**Edit cash and carry transactions** – This option lets you edit all the cash and carry transactions that are included in the statement.</span></span> <span data-ttu-id="f0645-155">Eftirfarandi Excel-vinnublöð eru í boði:</span><span class="sxs-lookup"><span data-stu-id="f0645-155">The following Excel worksheets are available:</span></span>

        - <span data-ttu-id="f0645-156">**Færsla** – Þetta vinnublað er með allar upplýsingar á hausstigi fyrir sölufærslurnar.</span><span class="sxs-lookup"><span data-stu-id="f0645-156">**Transaction** – This worksheet has all the header-level information for the sales transactions.</span></span>
        - <span data-ttu-id="f0645-157">**Sölufærsla** – Þetta vinnublað er með allar upplýsingar á línustigi fyrir sölufærslurnar.</span><span class="sxs-lookup"><span data-stu-id="f0645-157">**Sales transaction** – This worksheet has all the line-level information for the sales transactions.</span></span>
        - <span data-ttu-id="f0645-158">**Greiðslufærslur** – Þetta vinnublað er með allar upplýsingar um greiðslulínurnar fyrir sölufærslurnar.</span><span class="sxs-lookup"><span data-stu-id="f0645-158">**Payment transactions** – This worksheet has all the payment line information for the sales transactions.</span></span>
        - <span data-ttu-id="f0645-159">**Afsláttarfærslur** – Þetta vinnublað er með allar upplýsingar um afsláttarlínur fyrir sölufærslurnar.</span><span class="sxs-lookup"><span data-stu-id="f0645-159">**Discount transactions** – This worksheet has all the discount line information for the sales transactions.</span></span>
        - <span data-ttu-id="f0645-160">**Skattfærslur** – Þetta vinnublað er með allar upplýsingar um skattlínur fyrir sölufærslurnar.</span><span class="sxs-lookup"><span data-stu-id="f0645-160">**Tax transactions** – This worksheet has all the tax line information for the sales transactions.</span></span>
        - <span data-ttu-id="f0645-161">**Gjaldfærslur** – Þetta vinnublað er með allar upplýsingar um gjaldlínur fyrir sölufærslurnar.</span><span class="sxs-lookup"><span data-stu-id="f0645-161">**Charge transactions** – This worksheet has all the charge line information for the sales transactions.</span></span>

    - <span data-ttu-id="f0645-162">**Breyta reiðufjárstjórnunarfærslum** – Þessi valkostur gerir notanda kleift að breyta öllum reiðufjárstjórnunarfærslum sem eru innifaldar í uppgjörinu.</span><span class="sxs-lookup"><span data-stu-id="f0645-162">**Edit cash management transactions** – This option lets you edit all the cash management transactions that are included in the statement.</span></span> <span data-ttu-id="f0645-163">Eftirfarandi Excel-vinnublöð eru í boði:</span><span class="sxs-lookup"><span data-stu-id="f0645-163">The following Excel worksheets are available:</span></span>

        - <span data-ttu-id="f0645-164">**Færsla** – Þetta vinnublað er með allar upplýsingar á hausstigi fyrir reiðufjárstjórnunarfærslurnar.</span><span class="sxs-lookup"><span data-stu-id="f0645-164">**Transaction** – This worksheet has all the header-level information for the cash management transactions.</span></span>
        - <span data-ttu-id="f0645-165">**Greiðslufærslur á vörslureikningi** – Þetta vinnublað er með allar færsluupplýsingar um peningaflutning í banka.</span><span class="sxs-lookup"><span data-stu-id="f0645-165">**Bank tender transactions** – This worksheet has all the bank drop transaction details.</span></span>
        - <span data-ttu-id="f0645-166">**Greiðslufærslur í öryggisskáp** – Þetta vinnublað er með allar færsluupplýsingar um peningaflutning í öryggisskáp.</span><span class="sxs-lookup"><span data-stu-id="f0645-166">**Safe tender transactions** – This worksheet has all the safe drop transaction details.</span></span>
        - <span data-ttu-id="f0645-167">**Talning skiptimyntar** – Þetta vinnublað er með allar færsluupplýsingar um talningu skiptimyntar.</span><span class="sxs-lookup"><span data-stu-id="f0645-167">**Tender declaration** – This worksheet has all the tender declaration transaction details.</span></span>
        - <span data-ttu-id="f0645-168">**Tekju-/útgjaldafærsla** – Þetta vinnublað er með allar upplýsingar um tekju/-útgjaldafærslulínu.</span><span class="sxs-lookup"><span data-stu-id="f0645-168">**Income-expense transaction** – This worksheet has all the income-expense transaction line details.</span></span>
        - <span data-ttu-id="f0645-169">**Greiðslufærslur** - Þetta vinnublað er með allar greiðslutengdar upplýsingar fyrir aðgerðina **Greiða reikning** og tekju/-kostnaðarfærsluna.</span><span class="sxs-lookup"><span data-stu-id="f0645-169">**Payment transactions** – This worksheet has all the payment-related information for the **Pay invoice** operation and the income-expense transaction.</span></span>

1. <span data-ttu-id="f0645-170">Gerið breytingar á áskildum færslum.</span><span class="sxs-lookup"><span data-stu-id="f0645-170">Edit the required transactions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f0645-171">Villuleit fer ekki fram þegar birtur er fjöldi færslna sem var breytt á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="f0645-171">Validations aren't done when you publish bulk-edited transactions.</span></span> <span data-ttu-id="f0645-172">Ganga þarf úr skugga um að breytingarnar sem gerðar eru séu réttar og að öll gögn á öllum vinnublöðunum samsvari sér.</span><span class="sxs-lookup"><span data-stu-id="f0645-172">You must make sure that all your edits are accurate, and that the fidelity of data across the worksheets is maintained.</span></span> <span data-ttu-id="f0645-173">Þegar t.d. á að breyta færsludagsetningunni til að stjórna sviðsmyndum þar sem fjárhags- eða birgðahaldstíminn fyrir opnar færslur er lokaður verður að breyta dagsetningunni á öllum Excel-vinnublöðunum sem eru með dálkinn **Viðskiptadagsetning**.</span><span class="sxs-lookup"><span data-stu-id="f0645-173">For example, if you want to change the transaction date, so that you can manage scenarios where the fiscal or inventory period for the open transactions is closed, you must change the date on all the Excel worksheets that have the **Business date** column.</span></span> <span data-ttu-id="f0645-174">Til að staðfesta færslur eftir að þeim hefur verið breytt er hægt að smella á **Villuleita færslur aftur** á síðunni **Uppgjör**.</span><span class="sxs-lookup"><span data-stu-id="f0645-174">To validate transactions after they have been edited, you can select **Revalidate transactions** on the **Statements** page.</span></span> <span data-ttu-id="f0645-175">Bíðið þar til villuleitarverkinu lýkur áður en yfirlitið er birt.</span><span class="sxs-lookup"><span data-stu-id="f0645-175">Wait for the validation job to finish running before you post the statement.</span></span>

1. <span data-ttu-id="f0645-176">Þegar uppsöfnun hefur þegar verið gerð skal opna síðuna **Uppsafnaðar færslur** og velja **Endurgera XML-skrá sölupöntunar**.</span><span class="sxs-lookup"><span data-stu-id="f0645-176">If the aggregation has already been generated, open the **Aggregated transactions** page, and select **Regenerate sales order xml**.</span></span>

## <a name="bulk-edit-transactions-that-arent-linked-to-a-statement"></a><span data-ttu-id="f0645-177">Breyta mörgum færslum í einu sem tengjast ekki uppgjöri</span><span class="sxs-lookup"><span data-stu-id="f0645-177">Bulk-edit transactions that aren't linked to a statement</span></span>

<span data-ttu-id="f0645-178">Commerce-útgáfa 10.0.10 og nýrri útgáfur styðja breytingar á fjölda færslna sem stóðust ekki villuleit en eru ekki tengdar við uppgjör.</span><span class="sxs-lookup"><span data-stu-id="f0645-178">Commerce version 10.0.10 and later support the option to bulk-edit transactions that fail validation but aren't linked to a statement.</span></span>

<span data-ttu-id="f0645-179">Fylgið eftirfarandi skrefum til að breyta mörgum færslum í einu sem ekki tengjast uppgjöri í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="f0645-179">To bulk-edit transactions that aren't linked to a statement in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="f0645-180">Opnið síðuna **Allar verslanir** og veljið verslunina sem skal breyta færslum fyrir.</span><span class="sxs-lookup"><span data-stu-id="f0645-180">Open the **All stores** page, and select the store that transactions must be edited for.</span></span>
1. <span data-ttu-id="f0645-181">Veljið hnappinn **Opna í Microsoft Office** og síðan **Breyta staðgreiddum færslum**.</span><span class="sxs-lookup"><span data-stu-id="f0645-181">Select the **Open in Microsoft Office** button, and then select **Edit cash and carry transactions**.</span></span>
1. <span data-ttu-id="f0645-182">Breytið áskildum færslum og birtið þær síðan.</span><span class="sxs-lookup"><span data-stu-id="f0645-182">Edit the required transactions, and then publish them.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f0645-183">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f0645-183">Additional resources</span></span>

[<span data-ttu-id="f0645-184">Breyta og endurskoða netpöntun og ósamstilltar færslur pöntunar viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="f0645-184">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="f0645-185">Breyta fjárhagsvíddum fyrir smásölufærslur</span><span class="sxs-lookup"><span data-stu-id="f0645-185">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="f0645-186">Stofna Excel-vinnubók til að breyta smásölufærslum</span><span class="sxs-lookup"><span data-stu-id="f0645-186">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="f0645-187">Bæta svæðum við Excel-vinnubók til að breyta smásölufærslum</span><span class="sxs-lookup"><span data-stu-id="f0645-187">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)