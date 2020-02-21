---
title: Breyta og endurskoða færslur smásöluverslunar
description: Þetta efnisatriði lýsir virkni til að breyta og endurskoða færslur verslunar.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
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
ms.search.validFrom: 2019-09-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 97211ee36dbaa704d3a967e9b742ff1cae708707
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004390"
---
# <a name="edit-and-audit-retail-store-transactions"></a><span data-ttu-id="75fd9-103">Breyta og endurskoða færslur smásöluverslunar</span><span class="sxs-lookup"><span data-stu-id="75fd9-103">Edit and audit retail store transactions</span></span>

[!include [banner](includes/banner.md)]



<span data-ttu-id="75fd9-104">Viðskiptavinir Dynamics 365 Commerce nota forrit á sölustað bæði frá fyrsta og þriðja aðila.</span><span class="sxs-lookup"><span data-stu-id="75fd9-104">Dynamics 365 Commerce customers use first-party as well as third-party point of sale (POS) applications.</span></span> <span data-ttu-id="75fd9-105">Með forriti sölustaðar frá fyrsta aðila eru færslur verslunar teknar inn í höfuðstöðvar úr rásunum með runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="75fd9-105">With the first-party POS application, store transactions are pulled into Headquarters from the channels through a batch process.</span></span> <span data-ttu-id="75fd9-106">Með forritum frá þriðju aðilum eru færslurnar teknar inn í höfuðstöðvar með samþættingu.</span><span class="sxs-lookup"><span data-stu-id="75fd9-106">With third-party applications, transactions are pulled into Headquarters through integration.</span></span> <span data-ttu-id="75fd9-107">Þegar búið er að flytja færslurnar í höfuðstöðvar verður í báðum tilvikum að framkvæma samræmisathugun til að keyra margar villuleitir á færslunum í einu, til að taka einungis færslur sem tekist hefur að villuleita inn í uppgjörið sem á að bóka í höfuðstöðvunum.</span><span class="sxs-lookup"><span data-stu-id="75fd9-107">In both cases, after transactions are pulled into Headquarters, a consistency check process needs to be executed that runs multiple validations on the transactions so that only successfully validated transactions are pulled into the statement to be posted in Headquarters.</span></span> 

<span data-ttu-id="75fd9-108">Viðskiptafærslur standast ekki villuleit af ýmsum ástæðum.</span><span class="sxs-lookup"><span data-stu-id="75fd9-108">Commerce transactions fail validation for various reasons.</span></span> <span data-ttu-id="75fd9-109">Til dæmis gæti villa í samþættingarkóðanum eða villa í forriti sölustaðar valdið ósamkvæmum gögnum, eða notandavillu, eins og að eyða afurð eftir að hún hefur verið samstillt við rásina eða að loka fjárhagstímabili án þess að bóka færslur fyrir viðkomandi tímabil, sem getur valdið ósamkvæmum gögnum.</span><span class="sxs-lookup"><span data-stu-id="75fd9-109">For example, a bug in the integration code or a bug in the POS application may cause inconsistent data, or a user error, such as deleting a product after it was synchronized to the channel or closing a fiscal period without posting transactions for that period, can cause inconsistent data.</span></span>

<span data-ttu-id="75fd9-110">Þótt þessar færslur séu merktar og útilokaðar frá uppgjörunum geta þær truflað daglegt bókunarferli viðskiptavinar í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="75fd9-110">While these transactions get flagged and are excluded from the statements, the transactions can disrupt a customer’s daily process of posting daily sales to the financials.</span></span>

<span data-ttu-id="75fd9-111">Í Commerce er hægt að breyta tilgreindum færslum sem stóðust ekki villuleit á meðan unnið er að endurskoðun á öllum breytingunum.</span><span class="sxs-lookup"><span data-stu-id="75fd9-111">In Commerce, you can edit the specific transactions that fail validation while maintaining audit of all the changes.</span></span> 

## <a name="edit-and-audit-transactions"></a><span data-ttu-id="75fd9-112">Breyta og endurskoða færslur</span><span class="sxs-lookup"><span data-stu-id="75fd9-112">Edit and audit transactions</span></span>

<span data-ttu-id="75fd9-113">Í Retail, útgáfu 10.0.5, er aðeins hægt að breyta staðgreiddum færslum eins og sölu- og skilafærslum.</span><span class="sxs-lookup"><span data-stu-id="75fd9-113">In Retail version 10.0.5, cash and carry transactions like sales and returns are the only transactions that can be edited.</span></span> <span data-ttu-id="75fd9-114">Breytingar á pöntunum viðskiptavinar eða netpöntunum eru ekki studdar.</span><span class="sxs-lookup"><span data-stu-id="75fd9-114">Editing customer orders or online orders is not supported.</span></span> <span data-ttu-id="75fd9-115">Í Retail, útgáfu 10.0.6, og nýrri er einnig stuðningur við breytingar á umsjón með reiðufjárfærslum.</span><span class="sxs-lookup"><span data-stu-id="75fd9-115">In Retail version 10.0.6 and higher, editing cash management transactions is also supported.</span></span>

1. <span data-ttu-id="75fd9-116">Setja upp Dynamics Excel-innbótina.</span><span class="sxs-lookup"><span data-stu-id="75fd9-116">Install the Dynamics Excel Add-in.</span></span>

2. <span data-ttu-id="75fd9-117">Opna vinnusvæði **Fjármál verslunar**.</span><span class="sxs-lookup"><span data-stu-id="75fd9-117">Go to the **Store financials** workspace.</span></span> <span data-ttu-id="75fd9-118">Reiturinn **Bilanir við villuleit í færslu** býður upp á forsíað yfirlit yfir færsluskjámynd sem féll á einni eða fleiri villuleitarreglum.</span><span class="sxs-lookup"><span data-stu-id="75fd9-118">The **Transaction validation failures** tile provides a pre-filtered view of the transaction form that failed one or more of the validation rules.</span></span>
 
3. <span data-ttu-id="75fd9-119">Opnið skjámyndina.</span><span class="sxs-lookup"><span data-stu-id="75fd9-119">Open the form.</span></span> <span data-ttu-id="75fd9-120">Smellið á færsluna sem stóðst ekki villuleit, á **Office-innbót** og svo á **Breyta valinni færslu**.</span><span class="sxs-lookup"><span data-stu-id="75fd9-120">Click the record that failed validation, click **Office Add in**, and then click **Edit selected transaction**.</span></span> <span data-ttu-id="75fd9-121">Excel-skrá með upplýsingum um valda færslu opnast með eftirfarandi vinnublöðum:</span><span class="sxs-lookup"><span data-stu-id="75fd9-121">An Excel file with the details of the selected transaction opens, with the following worksheets:</span></span>

    - <span data-ttu-id="75fd9-122">Línur: Þetta vinnublað er með haus og afurðarlínur og tengd gögn fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="75fd9-122">Lines: This worksheet has the header and product lines and related data for the transaction.</span></span>
    - <span data-ttu-id="75fd9-123">Greiðslur: Þetta vinnublað er með upplýsingar um greiðslulínur fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="75fd9-123">Payments: This worksheet has the details of the payment lines for the transaction.</span></span>
    - <span data-ttu-id="75fd9-124">Afslættir: Þetta vinnublað er með afsláttartengdar upplýsingar fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="75fd9-124">Discounts: This worksheet has the discount-related details for the transaction.</span></span>
    - <span data-ttu-id="75fd9-125">Skattar: Þetta vinnublað er með upplýsingar um skatt sem tengist færslunni.</span><span class="sxs-lookup"><span data-stu-id="75fd9-125">Taxes: This worksheet has the tax-related details for the transaction.</span></span>
    - <span data-ttu-id="75fd9-126">Gjöld: Þetta vinnublað er með gjaldtengdar upplýsingar fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="75fd9-126">Charges: This worksheet has the charges-related data for the transaction.</span></span>

4. <span data-ttu-id="75fd9-127">Í Excel-skránni er viðeigandi reitum breytt og gögnunum svo hlaðið aftur upp í höfuðstöðvum með birtingaraðgerð Excel-innbótarinnar í Dynamics.</span><span class="sxs-lookup"><span data-stu-id="75fd9-127">In the Excel file, you modify the appropriate fields and then upload the data back into Headquarters using the Dynamics Excel Add-in publish functionality.</span></span> <span data-ttu-id="75fd9-128">Breytingarnar koma fram í kerfinu þegar búið er að birta þær.</span><span class="sxs-lookup"><span data-stu-id="75fd9-128">Once published, the changes will be reflected in the system.</span></span> <span data-ttu-id="75fd9-129">Meðan á birtingu stendur fer engin villuleit fram á breytingunum sem notendur gera.</span><span class="sxs-lookup"><span data-stu-id="75fd9-129">During publish, no validation is done on changes that users make.</span></span>

5. <span data-ttu-id="75fd9-130">Hægt er að skoða alla færsluslóð breytinganna með því að smella á **Skoða slóð endurskoðunar** í hausnum **Smásölufærsla** til að sjá breytingar á haus og í viðeigandi hluta og færslu á viðeigandi færslusíðu.</span><span class="sxs-lookup"><span data-stu-id="75fd9-130">A complete audit trail of the changes can be viewed by clicking **View audit trail** in the **Retail transaction** header for the header-level changes and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="75fd9-131">Til dæmis verða allar breytingar sem tengjast sölulínum sýnilegar á síðunni **Sölufærslur**, breytingar sem tengjast greiðslum verða sýnilegar á síðunni **Greiðslufærslur** o.s.frv. Upplýsingar um endurskoðun sem unnið er með fyrir breytingarnar eru eftirfarandi.</span><span class="sxs-lookup"><span data-stu-id="75fd9-131">For example, all changes relating to sales lines will be visible on the **Sales transactions** page, changes relating to payments will be visible on the **Payment transactions** page, etc. The audit details that are maintained for the changes are as follows.</span></span>

   - <span data-ttu-id="75fd9-132">Breytt dagsetning og tími</span><span class="sxs-lookup"><span data-stu-id="75fd9-132">Modified date and time</span></span>
   - <span data-ttu-id="75fd9-133">Svæði</span><span class="sxs-lookup"><span data-stu-id="75fd9-133">Field</span></span> 
   - <span data-ttu-id="75fd9-134">Gamalt gildi</span><span class="sxs-lookup"><span data-stu-id="75fd9-134">Old value</span></span>
   - <span data-ttu-id="75fd9-135">Nýtt gildi</span><span class="sxs-lookup"><span data-stu-id="75fd9-135">New value</span></span>
   - <span data-ttu-id="75fd9-136">Breytt af</span><span class="sxs-lookup"><span data-stu-id="75fd9-136">Modified by</span></span>

6. <span data-ttu-id="75fd9-137">Þegar breytingarnar hafa verið gerðar og birtar skal keyra valmöguleikann **Villuleita í færslum verslunar** aftur til að staðfesta að breytingarnar sem voru gerðar séu samræmdar og gildar.</span><span class="sxs-lookup"><span data-stu-id="75fd9-137">After your changes are made and published, run the **Validate store transactions** option again to validate that the changes you made are consistent and valid.</span></span>

> [!NOTE]
> <span data-ttu-id="75fd9-138">Aðeins er hægt að breyta færslum sem stóðust ekki villuleit.</span><span class="sxs-lookup"><span data-stu-id="75fd9-138">You can only edit transactions that failed validation.</span></span> <span data-ttu-id="75fd9-139">Ef óskað er eftir að breyta færslum sem staðist hafa villuleit skal breyta villuleitarstöðu færslunnar sem á að breyta í **Villa** eða **Engin** og þá er hægt að breyta henni.</span><span class="sxs-lookup"><span data-stu-id="75fd9-139">If you want to edit transactions that passed validation, change the validation status of the transaction you want to change to **Error** or **None** and then you will be able to edit it.</span></span> 


## <a name="bulk-edit-transactions"></a><span data-ttu-id="75fd9-140">Fjöldabreytingafærslur</span><span class="sxs-lookup"><span data-stu-id="75fd9-140">Bulk edit transactions</span></span>

<span data-ttu-id="75fd9-141">Í Retail, útgáfu 10.0.6, og nýrri er valkosturinn fyrir fjöldabreytingar á færslum á uppgjörsstigi studdur.</span><span class="sxs-lookup"><span data-stu-id="75fd9-141">In Retail version 10.0.6 and higher, the option to bulk edit transactions at a statement level is supported.</span></span> 

1. <span data-ttu-id="75fd9-142">Nota skal skref 1–3 hér að ofan í Excel-innbótinni til að opna færslur sem á að breyta.</span><span class="sxs-lookup"><span data-stu-id="75fd9-142">Use the Excel Add-in to open a statement that has transactions you want to modify using steps 1-3 above.</span></span>

2. <span data-ttu-id="75fd9-143">Veljið einn valkostanna hér að neðan.</span><span class="sxs-lookup"><span data-stu-id="75fd9-143">Choose one of the options below.</span></span>

    - <span data-ttu-id="75fd9-144">**Breyta staðgreiddum færslum**.</span><span class="sxs-lookup"><span data-stu-id="75fd9-144">**Edit cash and carry transactions**.</span></span> <span data-ttu-id="75fd9-145">Þessi valkostur gerir kleift að breyta öllum staðgreiddum færslum sem eru innifaldar í uppgjörinu.</span><span class="sxs-lookup"><span data-stu-id="75fd9-145">This option enables you to edit all the cash and carry transactions included in the statement.</span></span> <span data-ttu-id="75fd9-146">Eftirfarandi Excel-vinnublöð eru í boði.</span><span class="sxs-lookup"><span data-stu-id="75fd9-146">The following Excel worksheets are available.</span></span>
    
       - <span data-ttu-id="75fd9-147">**Færsla**: Þetta vinnublað er með allar upplýsingar á hausstigi fyrir sölufærslurnar.</span><span class="sxs-lookup"><span data-stu-id="75fd9-147">**Transaction**: This worksheet has all the header-level information for the sales transactions.</span></span>
       - <span data-ttu-id="75fd9-148">**Sölufærsla**: Þetta vinnublað er með allar upplýsingar á línustigi fyrir sölufærslurnar.</span><span class="sxs-lookup"><span data-stu-id="75fd9-148">**Sales transaction**: This worksheet has all the lines-level information for the sales transactions.</span></span>
       - <span data-ttu-id="75fd9-149">**Greiðslufærslur**: Þetta vinnublað er með allar upplýsingar um greiðslulínurnar fyrir sölufærslurnar.</span><span class="sxs-lookup"><span data-stu-id="75fd9-149">**Payment transactions**: This worksheet has all the payment lines information for the sales transactions.</span></span>
       - <span data-ttu-id="75fd9-150">**Afsláttarfærslur**: Þetta vinnublað er með allar upplýsingar um afsláttarlínur fyrir sölufærslurnar.</span><span class="sxs-lookup"><span data-stu-id="75fd9-150">**Discount transactions**: This worksheet has all the discount lines information for the sales transactions.</span></span>
       - <span data-ttu-id="75fd9-151">**Skattfærslur**: Þetta vinnublað er með allar upplýsingar um skattlínur fyrir sölufærslurnar.</span><span class="sxs-lookup"><span data-stu-id="75fd9-151">**Tax transactions**: This worksheet has all the tax lines information for the sales transactions.</span></span>
       - <span data-ttu-id="75fd9-152">**Gjaldfærslur**: Þetta vinnublað er með allar upplýsingar um gjaldlínur fyrir sölufærslurnar.</span><span class="sxs-lookup"><span data-stu-id="75fd9-152">**Charge transactions**: This worksheet has all the charge lines information for the sales transactions.</span></span>

    - <span data-ttu-id="75fd9-153">**Breyta reiðufjárstjórnunarfærslum**.</span><span class="sxs-lookup"><span data-stu-id="75fd9-153">**Edit cash management transactions**.</span></span> <span data-ttu-id="75fd9-154">Þessi valkostur gerir kleift að breyta öllum reiðufjárstjórnunarfærslum sem eru innifaldar í uppgjörinu.</span><span class="sxs-lookup"><span data-stu-id="75fd9-154">This option enables you to edit all the cash management transactions included in the statement.</span></span> <span data-ttu-id="75fd9-155">Eftirfarandi Excel-vinnublöð eru í boði.</span><span class="sxs-lookup"><span data-stu-id="75fd9-155">The following Excel worksheets are available.</span></span>
     
       - <span data-ttu-id="75fd9-156">**Færsla**: Þetta vinnublað er með allar upplýsingar á hausstigi fyrir reiðufjárstjórnunarfærslurnar.</span><span class="sxs-lookup"><span data-stu-id="75fd9-156">**Transaction**: This worksheet has all the header-level information for the cash management transactions.</span></span>
       - <span data-ttu-id="75fd9-157">**Greiðslufærslur á vörslureikningi**: Þetta vinnublað er með allar færsluupplýsingar um peningaflutning í banka.</span><span class="sxs-lookup"><span data-stu-id="75fd9-157">**Bank tender transactions**: This worksheet has all the bank drop transaction details.</span></span>
       - <span data-ttu-id="75fd9-158">**Greiðslufærslur í öryggisskáp**: Þetta vinnublað er með allar færsluupplýsingar um peningaflutning í öryggisskáp.</span><span class="sxs-lookup"><span data-stu-id="75fd9-158">**Safe tender transactions**: This worksheet has all the safe drop transaction details.</span></span>
       - <span data-ttu-id="75fd9-159">**Talning skiptimyntar**: Þetta vinnublað er með allar færsluupplýsingar um talningu skiptimyntar.</span><span class="sxs-lookup"><span data-stu-id="75fd9-159">**Tender declaration**: This worksheet has all the tender declaration transaction details.</span></span>
       - <span data-ttu-id="75fd9-160">**Tekju-/útgjaldafærsla**: Þetta vinnublað er með allar upplýsingar um tekju/-útgjaldafærslulínu.</span><span class="sxs-lookup"><span data-stu-id="75fd9-160">**Income-expense transaction**: This worksheet has all the income-expense transaction line details.</span></span>
       - <span data-ttu-id="75fd9-161">**Greiðslufærslur**: Þetta vinnublað er með allar greiðslutengdar upplýsingar fyrir aðgerðina **Greiða reikning**, sem og tekju/-kostnaðarfærsluna.</span><span class="sxs-lookup"><span data-stu-id="75fd9-161">**Payment transactions**: This worksheet has all the payment-related information for the **Pay invoice** operation as well as the income-expense transaction.</span></span>

3.  <span data-ttu-id="75fd9-162">Villuleitir eru ekki framkvæmdar þegar fjöldabreyttar færslur eru birtar.</span><span class="sxs-lookup"><span data-stu-id="75fd9-162">Validations are not performed when you publish bulk edited transactions.</span></span> <span data-ttu-id="75fd9-163">Tryggja verður að allar breytingar séu réttar og að gögnin séu samsvarandi á öllum vinnublöðunum.</span><span class="sxs-lookup"><span data-stu-id="75fd9-163">You must ensure that all your edits are accurate and the fidelity of data across the worksheets is maintained.</span></span> <span data-ttu-id="75fd9-164">Til dæmis, ef óskað er eftir að breyta færsludagsetningunni til að stjórna sviðsmyndum þar sem fjárhags- eða birgðahaldstíminn fyrir opnar færslur er lokaður þarf að breyta dagsetningunni á öllum Excel-vinnublöðunum sem eru með dálkinn **Viðskiptadagsetning**.</span><span class="sxs-lookup"><span data-stu-id="75fd9-164">For example, if you want to change the transaction date to manage the scenarios where the fiscal or inventory period for the open transactions is closed, you need to change the date on all the Excel worksheets that have the **Business date** column.</span></span> <span data-ttu-id="75fd9-165">Til að staðfesta færslur eftir að þeim hefur verið breytt er hægt að nota **Villuleita færslur aftur** á síðunni **Uppgjör**.</span><span class="sxs-lookup"><span data-stu-id="75fd9-165">To validate transactions after they have been edited, you can use **Revalidate transactions** on the **Statements** page.</span></span>
