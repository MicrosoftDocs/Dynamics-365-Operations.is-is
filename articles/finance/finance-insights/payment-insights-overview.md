---
title: Greiðsluspár viðskiptavinar (forskoðun)
description: Þetta efnisatriði lýsir getu greiðsluspár sem geta hjálpað notendum við að skilja betur dæmigerðar greiðsluvenjur viðskiptavinar. Þessi eiginleiki getur einnig komið í veg fyrir aðstæður þar sem innheimtuferli er hafið fyrr en annars væri byrjað á því.
author: ShivamPandey-msft
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 4151b56b8b385e29d3926dc7e245728158cbcd34
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/14/2021
ms.locfileid: "5898013"
---
# <a name="customer-payment-predictions-preview"></a><span data-ttu-id="4039c-104">Greiðsluspár viðskiptavinar (forskoðun)</span><span class="sxs-lookup"><span data-stu-id="4039c-104">Customer payment predictions (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="4039c-105">Þetta efnisatriði lýsir getu greiðsluspár sem geta hjálpað notendum við að skilja betur dæmigerðar greiðsluvenjur viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="4039c-105">This topic describes the payment predictions capability that can help you better understand a customer's typical payment practices.</span></span> <span data-ttu-id="4039c-106">Þessi eiginleiki getur einnig komið í veg fyrir aðstæður þar sem innheimtuferli er hafið fyrr en annars væri byrjað á því.</span><span class="sxs-lookup"><span data-stu-id="4039c-106">This feature can also help identify circumstances that should cause you to start collections processes earlier than you might otherwise start them.</span></span>

## <a name="overview"></a><span data-ttu-id="4039c-107">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="4039c-107">Overview</span></span>

<span data-ttu-id="4039c-108">Fyrirtækjum finnst oft krefjandi að spá fyrir um hvenær viðskiptavinir greiða reikninga sína.</span><span class="sxs-lookup"><span data-stu-id="4039c-108">Organizations often find it challenging to predict when customers will pay their invoices.</span></span> <span data-ttu-id="4039c-109">Þessi skortur á innsæi getur valdið eftirfarandi vandamálum:</span><span class="sxs-lookup"><span data-stu-id="4039c-109">This lack of insight can cause the following issues:</span></span>

- <span data-ttu-id="4039c-110">Minna nákvæm sjóðstreymispá</span><span class="sxs-lookup"><span data-stu-id="4039c-110">Less accurate cash flow forecasts</span></span>
- <span data-ttu-id="4039c-111">Innheimtuferli sem byrja of seint</span><span class="sxs-lookup"><span data-stu-id="4039c-111">Collections processes that start too late</span></span>
- <span data-ttu-id="4039c-112">Pantanir sem eru losaðar til viðskiptavinna sem kunna að greiða ekki</span><span class="sxs-lookup"><span data-stu-id="4039c-112">Orders that are released to customers who might default on their payment</span></span>

<span data-ttu-id="4039c-113">Greiðsluspá viðskiptavinar (forskoðun) hjálpar fyrirtækjum að spá fyrir um hvenær reikningur viðskiptavinar verður greiddur.</span><span class="sxs-lookup"><span data-stu-id="4039c-113">Customer payment predictions (preview) helps organizations predict when a customer invoice will be paid.</span></span> <span data-ttu-id="4039c-114">Þess vegna er hægt að búa til innheimtuáætlanir sem þar sem líkurnar á greisðlu á réttum tíma eru auknar.</span><span class="sxs-lookup"><span data-stu-id="4039c-114">Therefore, they can create collections strategies that help increase the likelihood that they will be paid on time.</span></span>

## <a name="predictions"></a><span data-ttu-id="4039c-115">Spár</span><span class="sxs-lookup"><span data-stu-id="4039c-115">Predictions</span></span>

<span data-ttu-id="4039c-116">Greiðsluspár gera fyrirtækjum kleift að bæta viðskiptaferli sitt með því að hjálpa þeim að bera kennsl á reikninga sím líklegt er að séu greiddir seint.</span><span class="sxs-lookup"><span data-stu-id="4039c-116">Payment predictions let organizations improve their business processes by helping them identify the invoices that are likely to be paid late.</span></span> <span data-ttu-id="4039c-117">Fyrirtæki geta notað þessar upplýsingar til að grípa til aðgerða sem bæta líkurnar á því að reikningar verði greiddir á réttum tíma.</span><span class="sxs-lookup"><span data-stu-id="4039c-117">Organization can use that information to take actions that improve the chances that they will be paid on time.</span></span>

<span data-ttu-id="4039c-118">Greiðsluspár viðskiptavinar eiginleikinn notar vélnámslíkan til að spá betur fyrir um það hvenær viðskiptavinur mun greiða útistandandi reikning.</span><span class="sxs-lookup"><span data-stu-id="4039c-118">The Customer payment predictions feature uses a machine learning model to more accurately predict when a customer will pay an outstanding invoice.</span></span> <span data-ttu-id="4039c-119">Þetta vélnámslíkan inniheldur sögulega reikninga, greiðslur og gögn viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="4039c-119">This machine learning model includes historical invoices, payments, and customer data.</span></span>

<span data-ttu-id="4039c-120">Aðgerðin úthlutar þremur greiðslulíkum fyrir hvern opinn reikning:</span><span class="sxs-lookup"><span data-stu-id="4039c-120">For each open invoice, the feature assigns three payment probabilities:</span></span>

- <span data-ttu-id="4039c-121">Líkur á því að greiðslan berist á réttum tíma</span><span class="sxs-lookup"><span data-stu-id="4039c-121">The probability that the payment will be made on time</span></span>
- <span data-ttu-id="4039c-122">Líkur á því að greiðslan berist seint</span><span class="sxs-lookup"><span data-stu-id="4039c-122">The probability that the payment will be made late</span></span>
- <span data-ttu-id="4039c-123">Líkur á því að greiðslan berist mjög seint</span><span class="sxs-lookup"><span data-stu-id="4039c-123">The probability that the payment will be made very late</span></span>

<span data-ttu-id="4039c-124">Þessi eiginleiki veitir einnig samandregið yfirlit yfir áætlaðar greiðslur.</span><span class="sxs-lookup"><span data-stu-id="4039c-124">The feature also provides an aggregated view of expected payments.</span></span>

<span data-ttu-id="4039c-125">[![Samanlögð sýn á spá um greiðslur](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="4039c-125">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="4039c-126">Hverjum reikningi er úthlutað líkum á greiðslum á réttum tíma.</span><span class="sxs-lookup"><span data-stu-id="4039c-126">Each invoice is assigned a probability of on-time payment.</span></span> <span data-ttu-id="4039c-127">Reikningar þar sem líkur á greiðslu á réttum tíma eru undir 50 prósent hafa rauðan hring til að gefa til kynna að innheimtufulltrúi ætti að líta á þá.</span><span class="sxs-lookup"><span data-stu-id="4039c-127">Invoices that have a probability of on-time payment that is less than 50 percent are tagged with a red circle to indicate that they might require attention from a collections agent.</span></span>

<span data-ttu-id="4039c-128">[![Listi yfir greiðslulíkur](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="4039c-128">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="4039c-129">Greiðsluspá viðskiptavinar eiginleikinn veitir einnig samhengisupplýsingar til að útskýra spár.</span><span class="sxs-lookup"><span data-stu-id="4039c-129">The Customer payment predictions feature also provides contextual information to explain the prediction.</span></span> <span data-ttu-id="4039c-130">Þessar upplýsingar innihalda helstu þætti sem höfðu áhrif á spárnar, núverandi stöðu viðskipta við viðskiptavininn og upplýsingar um sögulega greiðsluhegðun viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="4039c-130">This information includes the top factors that influenced the prediction, the current state of business with the customer, and details about the customer's historical payment behavior.</span></span>

<span data-ttu-id="4039c-131">Í mörgum fyrirtækjum hefur innheimtuferlið verið viðbragðsþáttur.</span><span class="sxs-lookup"><span data-stu-id="4039c-131">In many businesses, the collections process has been a reactive activity.</span></span> <span data-ttu-id="4039c-132">Með öðrum orðum hefst innheimtuferlið ekki fyrr en reikningar eru gjaldfallnir.</span><span class="sxs-lookup"><span data-stu-id="4039c-132">In other words, the collections process doesn't start until invoices become due.</span></span> <span data-ttu-id="4039c-133">Greiðsluspá viðskiptavinar gerir fyrirtækjum kleift að grípa fyrr til aðgerða vegna innheimtu.</span><span class="sxs-lookup"><span data-stu-id="4039c-133">Customer payment predictions let organizations be more proactive about collections.</span></span> <span data-ttu-id="4039c-134">Þeir verða ekki lengur að bíða þess að færsla gjaldfalli til að hefja innheimtuferlið.</span><span class="sxs-lookup"><span data-stu-id="4039c-134">They no longer have to wait for a transaction to become due to start the collections process.</span></span> <span data-ttu-id="4039c-135">Í staðinn geta þeir notað greiðsluspárgetuna til að ákvarða hvort fyrirbyggjandi innheimta muni bæta líkurnar á því að fá greitt á réttum tíma.</span><span class="sxs-lookup"><span data-stu-id="4039c-135">Instead, they can use the payment predictions capability to determine whether proactive collections will improve the probability that they will be paid on time.</span></span>

## <a name="methodology"></a><span data-ttu-id="4039c-136">Aðferð</span><span class="sxs-lookup"><span data-stu-id="4039c-136">Methodology</span></span>

<span data-ttu-id="4039c-137">Það hefur yfirleitt reynst erfitt að þróa og nota gervigreindarlausn (AI).</span><span class="sxs-lookup"><span data-stu-id="4039c-137">In the past, it has typically been difficult to develop and deploy an artificial intelligence (AI) solution.</span></span> <span data-ttu-id="4039c-138">Þær hafa kallað á gagnavísindaVinnslan hefur krafist teymis sem inniheldur gögn vísindamanna, efnisorð (SMEs) og verkfræðinga, sem vinna með tíma til að móta, þróa, nota og viðhalda nothæfri AI-lausn.</span><span class="sxs-lookup"><span data-stu-id="4039c-138">The process has required a team that includes data scientists, subject matter experts (SMEs), and engineers, who work over time to formulate, develop, deploy, and maintain a usable AI solution.</span></span> <span data-ttu-id="4039c-139">Greiðsluspá viðskiptavinar auðveldar uppsetningu og notkun á AI lausn í Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="4039c-139">Customer payment predictions makes it easy to deploy and use an AI solution in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="4039c-140">Microsoft er með innifaldar AI-lausnir sem eru byggðar ofan á Microsoft AI Builder.</span><span class="sxs-lookup"><span data-stu-id="4039c-140">Microsoft is prepackaging AI solutions that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="4039c-141">Af þeim sökum geta notendur virkjað AI-lausnina með einum músarsmelli til að nýta kosti hugvitsamlegra spáa.</span><span class="sxs-lookup"><span data-stu-id="4039c-141">Therefore, users can deploy the AI solution in a single mouse click to take advantage of the benefits of intelligent predictions.</span></span> <span data-ttu-id="4039c-142">Ef notandi er ekki ánægður með nákvæmni spáa getur yfirnotandi (aftur með einum smelli) farið inn í viðbótina AI Builder og síðan valið eða afvalið reitina sem notaðir eru til að mynda spár.</span><span class="sxs-lookup"><span data-stu-id="4039c-142">If you aren't satisfied with the accuracy of predictions, a power user can (again, in a single mouse click) enter the AI Builder extension experience, and then select or clear the fields that are used to generate predictions.</span></span> <span data-ttu-id="4039c-143">Þegar þú ert tilbúinn getur þú „þjálfað“ líkanið og birt breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="4039c-143">When you're ready, you can "train" the model and publish the changes.</span></span> <span data-ttu-id="4039c-144">Nýþjálfaða líkanið verður sjálfkrafa valið til að mynda spár í Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="4039c-144">The newly trained model will automatically be picked up to generate predictions in Dynamics 365 Finance.</span></span>

## <a name="release-details"></a><span data-ttu-id="4039c-145">Upplýsingar um losun</span><span class="sxs-lookup"><span data-stu-id="4039c-145">Release details</span></span>

<span data-ttu-id="4039c-146">Almenn forskoðun Fjármálainnsýnar er í boði fyrir uppsetningar í Bandaríkjunum, Evrópu og Bretlandi.</span><span class="sxs-lookup"><span data-stu-id="4039c-146">Finance Insights public preview is available to try for deployments in the United States of America, Europe, and United Kingdom.</span></span> <span data-ttu-id="4039c-147">Microsoft er að bæta við stuðningi fyrir fleiri svæði.</span><span class="sxs-lookup"><span data-stu-id="4039c-147">Microsoft is incrementally adding support for additional regions.</span></span>

<span data-ttu-id="4039c-148">Aðeins ætti að kveikja á opinberum forskoðunaraðgerðum í sandkassaumhverfi í lagi 2.</span><span class="sxs-lookup"><span data-stu-id="4039c-148">Public preview features should be turned on only in Tier 2 sandbox environments.</span></span> <span data-ttu-id="4039c-149">Uppsetningar- og gervigreindarlíkön sem eru stofnuð í sandkassaumhverfi eru hugsanlega ekki hægt að flytja yfir í vinnsluumhverfi.</span><span class="sxs-lookup"><span data-stu-id="4039c-149">Setup and AI models that are created in a sandbox environment might not be migrated to the production environment.</span></span> <span data-ttu-id="4039c-150">Frekari upplýsingar er að finna í [Viðbótarnotkunarskilmálum fyrir Microsoft Dynamics 365 forskoðanir](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).</span><span class="sxs-lookup"><span data-stu-id="4039c-150">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="4039c-151">Tilkynning um persónuvernd</span><span class="sxs-lookup"><span data-stu-id="4039c-151">Privacy notice</span></span>

<span data-ttu-id="4039c-152">Forútgáfur (1) kunna að nota minni persónuverndar- og öryggisráðstafanir og þjónusta Dynamics 365 Finance and Operations, (2) eru ekki hluti af þjónustustigssamningi fyrir þessa þjónustu, (3) ættu ekki að vera notaðar til að vinna úr persónulegum gögnum eða öðrum gögnum sem falla undir lögboðnar kröfur eða reglur um samræmi og (4) hafa takmarkaðan stuðning.</span><span class="sxs-lookup"><span data-stu-id="4039c-152">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]