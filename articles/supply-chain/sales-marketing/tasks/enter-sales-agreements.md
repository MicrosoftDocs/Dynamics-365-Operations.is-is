---
title: Færa inn sölusamninga
description: Þetta efni útskýrir hvernig stofna á sölusamning sem bindur sig einum viðskiptavini til að kaupa vöru fyrir samþykkta upphæð yfir tíma í skiptum fyrir sérstakan afslátt.
author: omulvad
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 06d251992c7facca471ac893e5a0fee333e0cbed
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148654"
---
# <a name="enter-sales-agreements"></a><span data-ttu-id="e1104-103">Færa inn sölusamninga</span><span class="sxs-lookup"><span data-stu-id="e1104-103">Enter sales agreements</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e1104-104">Þetta efni útskýrir hvernig stofna á sölusamning sem bindur sig einum viðskiptavini til að kaupa vöru fyrir samþykkta upphæð yfir tíma í skiptum fyrir sérstakan afslátt.</span><span class="sxs-lookup"><span data-stu-id="e1104-104">This topic explains how to create a sales agreement that commits one of your customers to buy a product for an agreed amount over time in exchange for special discounts.</span></span> <span data-ttu-id="e1104-105">Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum.</span><span class="sxs-lookup"><span data-stu-id="e1104-105">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-sales-agreement-header"></a><span data-ttu-id="e1104-106">Setja upp Haus sölusamnings</span><span class="sxs-lookup"><span data-stu-id="e1104-106">Set up sales agreement header</span></span>
1. <span data-ttu-id="e1104-107">Í skoðunarrúðunni ferðu í **Einingar > Sala og markaðssetning > Sölusamningar > Sölusamningar**.</span><span class="sxs-lookup"><span data-stu-id="e1104-107">In the navigation pane, go to **Modules > Sales and marketing > Sales agreements > Sales agreements**.</span></span>
2. <span data-ttu-id="e1104-108">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="e1104-108">Select **New**.</span></span>
3. <span data-ttu-id="e1104-109">Í reitnum **Viðskiptavinalykill** velurðu skrána sem óskað er eftir af fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="e1104-109">In the **Customer account** field, select the desired record from the drop-down menu.</span></span>
4. <span data-ttu-id="e1104-110">Í reitnum **Flokkun sölusamninga** velurðu skrána sem óskað er eftir af fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="e1104-110">In the **Sales agreement classification** field, select the desired record from the drop-down menu.</span></span>
5. <span data-ttu-id="e1104-111">Víkkaðu út hlutann **Almennt**.</span><span class="sxs-lookup"><span data-stu-id="e1104-111">Expand the **General** section.</span></span>
6. <span data-ttu-id="e1104-112">Í reitnum **Sjálfgefin ráðstöfun** skal velja **Ráðstöfunarvirði afurðar**.</span><span class="sxs-lookup"><span data-stu-id="e1104-112">In the **Default commitment** field, select **Product value commitment**.</span></span> <span data-ttu-id="e1104-113">Ráðstöfunargerð er áskilið skilyrði sem þarf að tengja við samninginn til að skilgreina hvernig verður að uppfylla samnings.</span><span class="sxs-lookup"><span data-stu-id="e1104-113">A commitment type is a mandatory criterion that you must assign to the agreement to define how the agreement contract will be fulfilled.</span></span> <span data-ttu-id="e1104-114">Fjögur áður skilgreindar gerðir gera þér kleift að setja upp markmið viðskiptavinarins um ráðstöfun, sýnt sem magn eða gildi.</span><span class="sxs-lookup"><span data-stu-id="e1104-114">The four predefined types let you set up the customer's commitment target, expressed as a quantity or a value.</span></span> <span data-ttu-id="e1104-115">Aðeins má nota magn ráðstöfunargerðar á tiltekinni vöru, en gerðir byggt á gildi á við um sölu á bæði tilteknar og ótilteknar vörur.</span><span class="sxs-lookup"><span data-stu-id="e1104-115">The quantity commitment type can only be applied to a specific product, but the value-based types are applicable to sales of both specific and non-specific products.</span></span>  
7. <span data-ttu-id="e1104-116">Í reitnum **Lokadagur** skal stilla dagsetninguna í framtíðardagsetningu þegar samningurinn er að renna út.</span><span class="sxs-lookup"><span data-stu-id="e1104-116">In the **Expiration date** field, set the date to a future date when you want the agreement to expire.</span></span>
8. <span data-ttu-id="e1104-117">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e1104-117">Select **OK**.</span></span>

## <a name="set-up-product-value-commitment-lines"></a><span data-ttu-id="e1104-118">Setja upp afurðargildi skuldbindingarlína</span><span class="sxs-lookup"><span data-stu-id="e1104-118">Set up product value commitment lines</span></span>
1. <span data-ttu-id="e1104-119">Veldu **Bæta við línu**.</span><span class="sxs-lookup"><span data-stu-id="e1104-119">Select **Add line**.</span></span>
2. <span data-ttu-id="e1104-120">Í reitnum **Vörunúmer** velurðu skrána sem óskað er eftir af fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="e1104-120">In the **Item number** field, select the desired record from the drop-down menu.</span></span> <span data-ttu-id="e1104-121">Gerð ráðstöfunar sem valin er fyrir samninginn hefur áhrif á þær upplýsingar sem þú getur fært inn fyrir samningslínur.</span><span class="sxs-lookup"><span data-stu-id="e1104-121">The type of commitment that you have chosen for the agreement affects the kind of information you can enter for the agreement lines.</span></span> <span data-ttu-id="e1104-122">Til dæmis, fyrir samning sem byggist á virði verður að tilgreina samtals nettóupphæð (í gjaldmiðli sem samið var um) sem viðskiptavinur bindur sig að kaupa vörur fyrir.</span><span class="sxs-lookup"><span data-stu-id="e1104-122">For example, for a value-based agreement you must specify the total net amount (in the agreed currency) for which the customer commits to buys goods from you.</span></span> <span data-ttu-id="e1104-123">Í þessu dæmi eru reitirnir **Magn** og **Eining** í línunni ótiltækir þar sem verið er að stofna samning fyrir viðskiptavin sem á að kaupa sérstakt gildi afurðar.</span><span class="sxs-lookup"><span data-stu-id="e1104-123">In this example the **Quantity** and **Unit** fields on the line are unavailable because you're creating an agreement for the customer to buy a specific value of a product.</span></span>   
3. <span data-ttu-id="e1104-124">Í reitnum **Nettóupphæð** skal slá inn peningaupphæð sem viðskiptavinurinn hefur ráðstafað í kaup.</span><span class="sxs-lookup"><span data-stu-id="e1104-124">In the **Net amount** field, enter the monetary amount that the customer has committed to buying.</span></span>
4. <span data-ttu-id="e1104-125">Í reitnum **Afsláttarprósenta** skal færa inn gildi prósentu sem á við sölupöntunarlínur viðskiptavinarins sem tengjast þessum samningi.</span><span class="sxs-lookup"><span data-stu-id="e1104-125">In the **Discount percent** field, enter a percentage value that will apply to the customer's sales order lines that are linked to this agreement.</span></span>
5. <span data-ttu-id="e1104-126">Útvíkkaðu hlutann **upplýsingar Línu**.</span><span class="sxs-lookup"><span data-stu-id="e1104-126">Expand the **Line details** section.</span></span>
6. <span data-ttu-id="e1104-127">Velja skal **Já** í reitinn **Hámarki er framfylgt**.</span><span class="sxs-lookup"><span data-stu-id="e1104-127">Select **Yes** in the **Max is enforced** field.</span></span>
    - <span data-ttu-id="e1104-128">Val á **Hámarki er framfylgt** þýðir að heildarupphæð allra sölupöntunarlínanna sem nota sérstakt verð ráðstöfunar, afslátt og/eða greiðsluskilmála má ekki fara yfir upphæðina sem er tilgreind í ráðstöfuninni.</span><span class="sxs-lookup"><span data-stu-id="e1104-128">Selecting **Max is enforced** means that the total amount of all the sales order lines that use the commitment's special prices, discounts and/or payment terms must not exceed the amount specified on the commitment.</span></span>  
    - <span data-ttu-id="e1104-129">Lágmarks- og hámarks losunarupphæðir tilgreina svið gilda sem verður selt á hverja sölupöntun sem notar valinn samning.</span><span class="sxs-lookup"><span data-stu-id="e1104-129">The minimum and maximum release amounts specify a range of values that must be sold on each sales order that uses the selected agreement.</span></span>   
7. <span data-ttu-id="e1104-130">Útvíkkaðu hlutann **Haus sölusamnings**.</span><span class="sxs-lookup"><span data-stu-id="e1104-130">Expand the **Sales agreement header** section.</span></span> <span data-ttu-id="e1104-131">Nema staða samnings sé stillt á **Gildur**, er ekki hægt að tengja sölupantanir við samning og þar af leiðandi ekki stuðla að uppfyllingu á þeim samningi.</span><span class="sxs-lookup"><span data-stu-id="e1104-131">Unless the status of the agreement is set to **Effective**, sales orders cannot be associated with the agreement and can therefore not contribute to the fulfilment of that agreement.</span></span> <span data-ttu-id="e1104-132">Hægt er að breyta stöðunni handvirkt á þessu stigi.</span><span class="sxs-lookup"><span data-stu-id="e1104-132">You can change the status manually at this stage.</span></span> <span data-ttu-id="e1104-133">Þó væri myndi yfirleitt breyta stöðu þegar samnings fyrir viðskiptavin er staðfest.</span><span class="sxs-lookup"><span data-stu-id="e1104-133">However, the status would normally be changed when you confirm the agreement for the customer.</span></span>  
8. <span data-ttu-id="e1104-134">Á Aðgerðasvæðinu skal velja **Sölusamningur**.</span><span class="sxs-lookup"><span data-stu-id="e1104-134">On the Action Pane, select **Sales agreement**.</span></span>
9. <span data-ttu-id="e1104-135">Veldu **Staðfesting**.</span><span class="sxs-lookup"><span data-stu-id="e1104-135">Select **Confirmation**.</span></span> <span data-ttu-id="e1104-136">Gangið úr skugga um að valkosturinn **Merkja samning sem gildan** sé stilltur á **Já**.</span><span class="sxs-lookup"><span data-stu-id="e1104-136">Make sure that the **Mark agreement as effective** option is set to **Yes**.</span></span>  
10. <span data-ttu-id="e1104-137">Velja skal **Já** í reitnum **Prenta skýrslu**.</span><span class="sxs-lookup"><span data-stu-id="e1104-137">Select **Yes** in the **Print report** field.</span></span>
11. <span data-ttu-id="e1104-138">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e1104-138">Select **OK**.</span></span>
12. <span data-ttu-id="e1104-139">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e1104-139">Close the page.</span></span> <span data-ttu-id="e1104-140">Samningurinn er nú gildur.</span><span class="sxs-lookup"><span data-stu-id="e1104-140">The agreement is now effective.</span></span> <span data-ttu-id="e1104-141">Hægt er að hefja tengingu á pöntunum viðskiptavina við samning til mótfærslu við skuldbindingarmarkið.</span><span class="sxs-lookup"><span data-stu-id="e1104-141">You can start linking the customer's orders to the agreement to offset against the committed target.</span></span>  

