---
title: Innsýn í greiðslu viðskiptavinar (forútgáfa)
description: Þetta efni lýsir getu greiðsluinnsýna sem hjálpar til við að bæta skilning á dæmigerðum greiðsluaðferðum einstakra viðskiptavina og geta greint aðstæður sem réttlæta að hefja innheimtuferli fyrr en þú hefur gert annars.
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
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: f9f1e4ae4270380c88069723e768fd44ecf8c113
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773978"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="61eb2-103">Innsýn í greiðslu viðskiptavinar (forútgáfa)</span><span class="sxs-lookup"><span data-stu-id="61eb2-103">Customer payment insights (Preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="61eb2-104">Þetta efni lýsir getu greiðsluinnsýna sem hjálpar til við að bæta skilning á dæmigerðum greiðsluaðferðum einstakra viðskiptavina og geta greint aðstæður sem réttlæta að hefja innheimtuferli fyrr en þú gætir hafa annars gert.</span><span class="sxs-lookup"><span data-stu-id="61eb2-104">This topic describes the payment insights capability that helps improve understanding of individual customers' typical payment practices and that can identify circumstances that justify initiating collection processes earlier than you might have done otherwise.</span></span> 

## <a name="overview"></a><span data-ttu-id="61eb2-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="61eb2-105">Overview</span></span>

<span data-ttu-id="61eb2-106">Fyrirtækjum finnst oft krefjandi að spá fyrir um hvenær viðskiptavinir greiða reikninga sína.</span><span class="sxs-lookup"><span data-stu-id="61eb2-106">Organizations often find it challenging to predict when customers will pay their invoices.</span></span> <span data-ttu-id="61eb2-107">Þessi skortur á innsæi leiðir til ónákvæmari spáa um sjóðstreymi, innheimtuferla sem hefjast of seint og pantana sem gefnar eru út til viðskiptavina sem kunna að standa ekki í skilum með greiðslu.</span><span class="sxs-lookup"><span data-stu-id="61eb2-107">This lack of insight leads to less accurate cash flow forecasts, collections processes that start too late, and orders that are released to customers who may default on their payment.</span></span> <span data-ttu-id="61eb2-108">Innsýn í greiðslu viðskiptavinar (forskoðun) hjálpar fyrirtækjum að spá fyrir um hvenær reikningur viðskiptavinar verður greiddur, sem auðveldar fyrirtækjum að stofna innheimtustefnur sem auka líkurnar á því að greitt sé á réttum tíma.</span><span class="sxs-lookup"><span data-stu-id="61eb2-108">Customer payment insights (Preview) helps organizations predict when a customer invoice will be paid, helping organization create collections strategies that improve the probability of being paid on time.</span></span> 

## <a name="predictions"></a><span data-ttu-id="61eb2-109">Spár</span><span class="sxs-lookup"><span data-stu-id="61eb2-109">Predictions</span></span>

<span data-ttu-id="61eb2-110">Greiðsluspár gera fyrirtækjum kleift að bæta viðskiptaferli sín með því að hjálpa þeim að greina auðveldlega þá reikninga sem líklega verða greiddir seint og gera viðeigandi ráðstafanir sem bæta möguleika þeirra á að fá greitt á réttum tíma.</span><span class="sxs-lookup"><span data-stu-id="61eb2-110">Payment predictions will enable organizations to improve their business processes by helping them easily identify the invoices that are likely to be paid late, and to take appropriate measures that improve their chances of getting paid on time.</span></span>

<span data-ttu-id="61eb2-111">Með því að nota vélanámslíkan, sem nýtir sögulega reikninga, greiðslur og gögn viðskiptavina, spáir innsýn í greiðslu viðskiptavinar (forskoðun) nákvæmar hvenær viðskiptavinur muni greiða útistandandi reikning.</span><span class="sxs-lookup"><span data-stu-id="61eb2-111">Using a machine learning model, which leverages historical invoices, payments and customer data, Customer payment insights (Preview) more accurately predicts when a customer will pay an outstanding invoice.</span></span>

<span data-ttu-id="61eb2-112">Fyrir hvern opinn reikning spáir innsýn í greiðslu viðskiptavinar (forútgáfa) fyrir um þrjá greiðslumöguleika:</span><span class="sxs-lookup"><span data-stu-id="61eb2-112">For each open invoice, Customer payment insights (Preview) predicts three payment probabilities:</span></span>

-   <span data-ttu-id="61eb2-113">Líkur á að greiðsla fari fram á réttum tíma</span><span class="sxs-lookup"><span data-stu-id="61eb2-113">Probability of payment being made on time</span></span> 
-   <span data-ttu-id="61eb2-114">Líkur á að greiðsla fari seint fram</span><span class="sxs-lookup"><span data-stu-id="61eb2-114">Probability of payment being made late</span></span>
-   <span data-ttu-id="61eb2-115">Líkur á að greiðsla fari fram eftir gjalddaga</span><span class="sxs-lookup"><span data-stu-id="61eb2-115">Probability of payment being made very late</span></span>

<span data-ttu-id="61eb2-116">Til að hjálpa fyrirtækjum að skilja heildargreiðslufjárhæðina sem þeir geta búist við frá viðskiptavini í einu af þremur fötunum, á réttum tíma, seint og mjög seint, veitir greiðsla innsýn viðskiptavina (foskoðun) samansafn af væntanlegum greiðslum.</span><span class="sxs-lookup"><span data-stu-id="61eb2-116">To help Organizations understand the total payment amount they can expect from a customer in one of the three buckets, On time, Late and Very late, Customer payment insights (Preview) also provides an aggregated view of expected payments.</span></span>

<span data-ttu-id="61eb2-117">[![Samanlögð sýn á spá um greiðslur](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="61eb2-117">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="61eb2-118">Einnig er hverjum reikningi úthlutað líkum á greiðslu á réttum tíma.</span><span class="sxs-lookup"><span data-stu-id="61eb2-118">Also, each invoice is assigned a probability of payment on time.</span></span> <span data-ttu-id="61eb2-119">Ef líkurnar á greiðslu á réttum tíma eru undir 50% eru reikningarnir merktir með rauðum hring til að gefa til kynna að þessir reikningar geti þurft innheimtuathygli.</span><span class="sxs-lookup"><span data-stu-id="61eb2-119">If the probability of payment on time is less than 50%, the invoices are tagged with a red circle to  indicate that these invoices may require collections attention.</span></span> 

<span data-ttu-id="61eb2-120">[![Listi yfir greiðslulíkur](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="61eb2-120">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="61eb2-121">Innsýn greiðslu viðskiptavina (forskoðun) veitir einnig samhengisupplýsingar til að skýra spána, svo sem helstu þætti sem höfðu áhrif á spárnar, núverandi stöðu viðskipta við viðskiptavininn og upplýsingar um sögulega greiðsluhegðun viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="61eb2-121">Customer Payment Insights (Preview) also provides contextual information to explain the prediction, such as the top factors that influenced the predictions, the current state of business with the customer, and details about the historical customer payment behavior.</span></span> <span data-ttu-id="61eb2-122">Í mörgum fyrirtækjum hefur innheimtuferlið verið viðbragðsverkþáttur; innheimtu ferlið hefst ekki fyrr en innheimtuseðlar koma til gjalddaga.</span><span class="sxs-lookup"><span data-stu-id="61eb2-122">In many businesses, the collections process has been a reactive activity; the collections process doesn’t start until invoices come due.</span></span> 

<span data-ttu-id="61eb2-123">Með greiðslu innsýn viðskiptavina (forskoðun), geta fyrirtæki verið meira fyrirbyggjandi varðandi innheimtu.</span><span class="sxs-lookup"><span data-stu-id="61eb2-123">With Customer payment insights (Preview), organizations can be more proactive about collections.</span></span> <span data-ttu-id="61eb2-124">Þau þurfa ekki lengur að bíða eftir að færslur komi á gjalddaga til að hefja innheimtuferli.</span><span class="sxs-lookup"><span data-stu-id="61eb2-124">They no longer have to wait for the transactions to become due to start the collection process.</span></span> <span data-ttu-id="61eb2-125">Í staðinn geta þeir notað greiðsluspárgetuna til að ákvarða hvort fyrirbyggjandi innheimta muni bæta líkurnar á að fá greitt á réttum tíma.</span><span class="sxs-lookup"><span data-stu-id="61eb2-125">Instead, they can use the payment prediction capability to determine whether proactive collections will improve the probability of being paid on time.</span></span> <span data-ttu-id="61eb2-126">Greiðsluspá veitir fyrirtækjum einnig þær upplýsingar sem þarf til að réttlæta að hefja innheimtuferlið snemma.</span><span class="sxs-lookup"><span data-stu-id="61eb2-126">Payment prediction also gives businesses the information needed to justify starting the collection process early.</span></span>

## <a name="methodology"></a><span data-ttu-id="61eb2-127">Aðferð</span><span class="sxs-lookup"><span data-stu-id="61eb2-127">Methodology</span></span>

<span data-ttu-id="61eb2-128">Erfitt er að þróa og dreifa AI lausn.</span><span class="sxs-lookup"><span data-stu-id="61eb2-128">Developing and deploying an AI solution is hard.</span></span> <span data-ttu-id="61eb2-129">Það þarf hóp gagnafræðinga, fagaðila og verkfræðinga sem vinna í langan tíma til að móta, þróa, dreifa og viðhalda nothæfri AI lausn.</span><span class="sxs-lookup"><span data-stu-id="61eb2-129">It takes a team of data scientists, subject matter experts and engineers, working for an extended period of time to formulate, develop, deploy and maintain a usable AI solution.</span></span> <span data-ttu-id="61eb2-130">Við erum að auðvelda að dreifingu og notkun á AI lausnum í Finance.</span><span class="sxs-lookup"><span data-stu-id="61eb2-130">We are making it easy to deploy and use AI solutions in Finance.</span></span> <span data-ttu-id="61eb2-131">Við erum að forpakka AI lausnum í Finance sem eru byggðar ofan á Microsoft AI Builder.</span><span class="sxs-lookup"><span data-stu-id="61eb2-131">We are prepackaging AI solutions in Finance that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="61eb2-132">Með einum smelli á hnapp getur notandi beitt AI lausninni og byrjað að nýta ávinninginn af snjallspám.</span><span class="sxs-lookup"><span data-stu-id="61eb2-132">An end user, with the single click of button, can deploy the AI solution and start leveraging the benefits of intelligent predictions.</span></span> <span data-ttu-id="61eb2-133">Ef fyrirtæki er ekki ánægt með nákvæmni spáa getur yfirnotandi, aftur með einum smelli, farið inn í viðbótina AI Builder og síðan valið eða afvalið reitina sem notaðir eru til að mynda spár.</span><span class="sxs-lookup"><span data-stu-id="61eb2-133">If an organization isn't satisfied with the accuracy of predictions, a power user, again using a single click, can enter the AI builder extension experience, and then select or deselect the fields used to generate predictions.</span></span> <span data-ttu-id="61eb2-134">Þegar þeir eru tilbúnir geta þeir þjálfað og birt breytingarnar og nýþjálfaða líkanið verður sjálfkrafa sótt fyrir spár í Finance.</span><span class="sxs-lookup"><span data-stu-id="61eb2-134">Once ready, they can train and publish the changes, and the newly trained model will be automatically picked up for predictions in Finance.</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="61eb2-135">Hvernig skal nálgast innsýn í greiðslu viðskiptavinar (forútgáfa)</span><span class="sxs-lookup"><span data-stu-id="61eb2-135">How to get Customer payment insights (Preview)</span></span>

<span data-ttu-id="61eb2-136">Vinsamlegast sendu tölvupóst til [Innsýn í greiðslu viðskiptavinar (forútgáfa)](mailto:fiap@microsoft.com) ef þú hefur áhuga á að prófa innsýn í greiðslu viðskiptavinar (forútgáfu).</span><span class="sxs-lookup"><span data-stu-id="61eb2-136">Please send email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in trying the Customer payment insights (Preview).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="61eb2-137">Tilkynning um persónuvernd</span><span class="sxs-lookup"><span data-stu-id="61eb2-137">Privacy Notice</span></span>

<span data-ttu-id="61eb2-138">Forútgáfur (1) geta mögulega notað minni persónuverndar- og öryggisráðstafanir og þjónusta Dynamics 365 Finance and Operations, (2) eru ekki hluti af þjónustustigssamningi fyrir þessa þjónustu, (3) ættu ekki að vera notaðar til að vinna úr persónulegum gögnum eða öðrum gögnum sem falla undir lögboðnar kröfur eða reglur um samræmi og (4) hafa takmarkaðan stuðning.</span><span class="sxs-lookup"><span data-stu-id="61eb2-138">Previews (1) may utilize less privacy and security measures than the Dynamics 365 Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>


