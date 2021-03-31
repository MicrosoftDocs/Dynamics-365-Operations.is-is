---
title: Innsýn í greiðslu viðskiptavinar (forútgáfa)
description: Í þessu efnisatriði er lýsing á greiðsluinnsýn sem getur aukið skilning á dæmigerðri greiðsluhegðun einstakra viðskiptavina. Þessi eiginleiki getur hjálpað til við að auðkenna aðstæður sem réttlæta innheimtuferli fyrr en annars hefði verið.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 21516cb7ef6e95dcef27638ddb72520f492958a5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207328"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="4416d-104">Innsýn í greiðslu viðskiptavinar (forútgáfa)</span><span class="sxs-lookup"><span data-stu-id="4416d-104">Customer payment insights (Preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="4416d-105">Í þessu efnisatriði er lýsing á greiðsluinnsýn sem getur aukið skilning á dæmigerðri greiðsluhegðun einstakra viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="4416d-105">This topic describes the payment insights capability that helps improve understanding of individual customers' typical payment practices.</span></span> <span data-ttu-id="4416d-106">Þessi eiginleiki getur hjálpað til við að auðkenna aðstæður sem réttlæta innheimtuferli fyrr en annars hefði verið.</span><span class="sxs-lookup"><span data-stu-id="4416d-106">The feature can help you identify circumstances that justify initiating collection processes earlier than you might have done otherwise.</span></span> 

## <a name="overview"></a><span data-ttu-id="4416d-107">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="4416d-107">Overview</span></span>

<span data-ttu-id="4416d-108">Það getur verið erfitt að spá fyrir um hvenær viðskiptavinir munu greiða reikninga sína.</span><span class="sxs-lookup"><span data-stu-id="4416d-108">It can be hard to predict when customers will pay their invoices.</span></span> <span data-ttu-id="4416d-109">Þessi skortur á innsæi leiðir til ónákvæmari spáa um sjóðstreymi, innheimtuferla sem hefjast of seint og pantana sem gefnar eru út til viðskiptavina sem kunna að standa ekki í skilum með greiðslu.</span><span class="sxs-lookup"><span data-stu-id="4416d-109">This lack of insight leads to less accurate cash flow forecasts, collections processes that start too late, and orders that are released to customers who may default on their payment.</span></span> <span data-ttu-id="4416d-110">Innsýn í greiðslur viðskiptavinar (forskoðun) hjálpar fyrirtækjum að spá fyrir um hvenær reikningur viðskiptavinar verður greiddur.</span><span class="sxs-lookup"><span data-stu-id="4416d-110">Customer payment insights (Preview) helps organizations predict when a customer invoice will be paid.</span></span> <span data-ttu-id="4416d-111">Þessar upplýsingar geta hjálpað fyrirtækjum að búa til innheimtuaðferðir sem auka líkurnar á því að fá greitt á réttum tíma.</span><span class="sxs-lookup"><span data-stu-id="4416d-111">This information can help organizations create collections strategies that improve the probability of being paid on time.</span></span> 

## <a name="predictions"></a><span data-ttu-id="4416d-112">Spár</span><span class="sxs-lookup"><span data-stu-id="4416d-112">Predictions</span></span>

<span data-ttu-id="4416d-113">Greiðsluspár gera fyrirtækjum kleift að bæta viðskiptaferli sín með því að hjálpa þeim að greina auðveldlega þá reikninga sem líklega verða greiddir seint og gera viðeigandi ráðstafanir sem bæta möguleika þeirra á að fá greitt á réttum tíma.</span><span class="sxs-lookup"><span data-stu-id="4416d-113">Payment predictions will enable organizations to improve their business processes by helping them easily identify the invoices that are likely to be paid late, and to take appropriate measures that improve their chances of getting paid on time.</span></span>

<span data-ttu-id="4416d-114">Með því að nota vélanámslíkan, sem nýtir sögulega reikninga, greiðslur og gögn viðskiptavina, spáir innsýn í greiðslu viðskiptavinar (forskoðun) nákvæmar hvenær viðskiptavinur muni greiða útistandandi reikning.</span><span class="sxs-lookup"><span data-stu-id="4416d-114">Using a machine learning model, which leverages historical invoices, payments and customer data, Customer payment insights (Preview) more accurately predicts when a customer will pay an outstanding invoice.</span></span>

<span data-ttu-id="4416d-115">Fyrir hvern opinn reikning getur innsýn spáð í greiðslu viðskiptavinar (forútgáfa) fyrir um þrjá greiðslumöguleika:</span><span class="sxs-lookup"><span data-stu-id="4416d-115">For each open invoice, Customer payment insights (Preview) can predict three payment probabilities:</span></span>

-   <span data-ttu-id="4416d-116">Líkur á að greiðsla fari fram á réttum tíma</span><span class="sxs-lookup"><span data-stu-id="4416d-116">Probability of payment being made on time</span></span> 
-   <span data-ttu-id="4416d-117">Líkur á að greiðsla fari seint fram</span><span class="sxs-lookup"><span data-stu-id="4416d-117">Probability of payment being made late</span></span>
-   <span data-ttu-id="4416d-118">Líkur á að greiðsla fari fram eftir gjalddaga</span><span class="sxs-lookup"><span data-stu-id="4416d-118">Probability of payment being made very late</span></span>

<span data-ttu-id="4416d-119">Innsýn í greiðslur viðskiptavinar (forskoðun) veitir einnig samandregið yfirlit yfir áætlaðar greiðslur sem geta hjálpað fyrirtækjum að skilja heildargreiðsluupphæðina sem þeir geta búist við að viðskiptavinur greiði í einum af þremur römmum; á réttum tíma, seint og mjög seint.</span><span class="sxs-lookup"><span data-stu-id="4416d-119">Customer payment insights (Preview) also provides an aggregated view of expected payments, which can help organizations understand the total payment amount they can expect from a customer in one of the three buckets, On time, Late and Very late.</span></span>

<span data-ttu-id="4416d-120">[![Samanlögð sýn á spá um greiðslur](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="4416d-120">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="4416d-121">Einnig er hverjum reikningi úthlutað líkum á greiðslu á réttum tíma.</span><span class="sxs-lookup"><span data-stu-id="4416d-121">Also, each invoice is assigned a probability of payment on time.</span></span> <span data-ttu-id="4416d-122">Ef líkurnar á greiðslu á réttum tíma eru undir 50% eru reikningarnir merktir með rauðum hring til að gefa til kynna að þessir reikningar geti þurft innheimtuathygli.</span><span class="sxs-lookup"><span data-stu-id="4416d-122">If the probability of payment on time is less than 50%, the invoices are tagged with a red circle to  indicate that these invoices may require collections attention.</span></span> 

<span data-ttu-id="4416d-123">[![Listi yfir greiðslulíkur](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="4416d-123">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="4416d-124">Innsýn greiðslu viðskiptavina (forskoðun) veitir einnig samhengisupplýsingar til að skýra spána, svo sem helstu þætti sem höfðu áhrif á spárnar, núverandi stöðu viðskipta við viðskiptavininn og upplýsingar um sögulega greiðsluhegðun viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="4416d-124">Customer Payment Insights (Preview) also provides contextual information to explain the prediction, such as the top factors that influenced the predictions, the current state of business with the customer, and details about the historical customer payment behavior.</span></span> <span data-ttu-id="4416d-125">Í mörgum fyrirtækjum hefur innheimtuferlið verið viðbragðsverkþáttur; innheimtu ferlið hefst ekki fyrr en innheimtuseðlar koma til gjalddaga.</span><span class="sxs-lookup"><span data-stu-id="4416d-125">In many businesses, the collections process has been a reactive activity; the collections process doesn’t start until invoices come due.</span></span> 

<span data-ttu-id="4416d-126">Með greiðslu innsýn viðskiptavina (forskoðun), geta fyrirtæki verið meira fyrirbyggjandi varðandi innheimtu.</span><span class="sxs-lookup"><span data-stu-id="4416d-126">With Customer payment insights (Preview), organizations can be more proactive about collections.</span></span> <span data-ttu-id="4416d-127">Þau þurfa ekki lengur að bíða eftir að færslur komi á gjalddaga til að hefja innheimtuferli.</span><span class="sxs-lookup"><span data-stu-id="4416d-127">They no longer have to wait for the transactions to become due to start the collection process.</span></span> <span data-ttu-id="4416d-128">Í staðinn geta þeir notað greiðsluspárgetuna til að ákvarða hvort fyrirbyggjandi innheimta muni bæta líkurnar á að fá greitt á réttum tíma.</span><span class="sxs-lookup"><span data-stu-id="4416d-128">Instead, they can use the payment prediction capability to determine whether proactive collections will improve the probability of being paid on time.</span></span> <span data-ttu-id="4416d-129">Greiðsluspá veitir fyrirtækjum einnig þær upplýsingar sem þarf til að réttlæta að hefja innheimtuferlið snemma.</span><span class="sxs-lookup"><span data-stu-id="4416d-129">Payment prediction also gives businesses the information needed to justify starting the collection process early.</span></span>

## <a name="methodology"></a><span data-ttu-id="4416d-130">Aðferð</span><span class="sxs-lookup"><span data-stu-id="4416d-130">Methodology</span></span>

<span data-ttu-id="4416d-131">Erfitt er að þróa og dreifa AI lausn.</span><span class="sxs-lookup"><span data-stu-id="4416d-131">Developing and deploying an AI solution is hard.</span></span> <span data-ttu-id="4416d-132">Fjöldi gagnasérfræðinga, sérfræðinga á viðkomandi sviði og verkfræðinga þarf að vinna lengi að mótun, þróun, uppsetningu og viðhaldi nothæfrar AI-lausnar.</span><span class="sxs-lookup"><span data-stu-id="4416d-132">It takes a team of data scientists, subject matter experts and engineers, working for an extended period of time to formulate, develop, deploy, and maintain a usable AI solution.</span></span> <span data-ttu-id="4416d-133">Við erum að auðvelda að dreifingu og notkun á AI lausnum í Finance.</span><span class="sxs-lookup"><span data-stu-id="4416d-133">We are making it easy to deploy and use AI solutions in Finance.</span></span> <span data-ttu-id="4416d-134">Við erum að forpakka AI lausnum í Finance sem eru byggðar ofan á Microsoft AI Builder.</span><span class="sxs-lookup"><span data-stu-id="4416d-134">We are prepackaging AI solutions in Finance that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="4416d-135">Með einum smelli á hnapp getur notandi beitt AI lausninni og byrjað að nýta ávinninginn af snjallspám.</span><span class="sxs-lookup"><span data-stu-id="4416d-135">An end user, with the single click of button, can deploy the AI solution and start leveraging the benefits of intelligent predictions.</span></span> <span data-ttu-id="4416d-136">Ef fyrirtæki er ekki ánægt með nákvæmni spáa getur yfirnotandi, aftur með einum smelli, farið inn í viðbótina AI Builder og síðan valið eða afvalið reitina sem notaðir eru til að mynda spár.</span><span class="sxs-lookup"><span data-stu-id="4416d-136">If an organization isn't satisfied with the accuracy of predictions, a power user, again using a single click, can enter the AI builder extension experience, and then select or deselect the fields used to generate predictions.</span></span> <span data-ttu-id="4416d-137">Þegar þeir eru tilbúnir geta þeir þjálfað og birt breytingarnar og nýþjálfaða líkanið verður sjálfkrafa sótt fyrir spár í Finance.</span><span class="sxs-lookup"><span data-stu-id="4416d-137">Once ready, they can train and publish the changes, and the newly trained model will be automatically picked up for predictions in Finance.</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="4416d-138">Hvernig skal nálgast innsýn í greiðslu viðskiptavinar (forútgáfa)</span><span class="sxs-lookup"><span data-stu-id="4416d-138">How to get Customer payment insights (Preview)</span></span>

<span data-ttu-id="4416d-139">Sendið tölvupóst til [Innsýn í greiðslur viðskiptavinar (forskoðun)](mailto:fiap@microsoft.com) ef áhugi er fyrir því að prófa „Innsýn í greiðslur viðskiptavinar (forskoðun)“.</span><span class="sxs-lookup"><span data-stu-id="4416d-139">Send email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in trying the Customer payment insights (Preview).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="4416d-140">Tilkynning um persónuvernd</span><span class="sxs-lookup"><span data-stu-id="4416d-140">Privacy Notice</span></span>

<span data-ttu-id="4416d-141">Forútgáfur (1) geta mögulega notað minni persónuverndar- og öryggisráðstafanir og þjónusta Dynamics 365 Finance and Operations, (2) eru ekki hluti af þjónustustigssamningi fyrir þessa þjónustu, (3) ættu ekki að vera notaðar til að vinna úr persónulegum gögnum eða öðrum gögnum sem falla undir lögboðnar kröfur eða reglur um samræmi og (4) hafa takmarkaðan stuðning.</span><span class="sxs-lookup"><span data-stu-id="4416d-141">Previews (1) may utilize less privacy and security measures than the Dynamics 365 Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]