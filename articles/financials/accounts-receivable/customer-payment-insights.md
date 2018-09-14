---
title: "Innsýn í greiðslu viðskiptavinar (forútgáfa)"
description: "Þetta efnisatriði fjallar um það hvernig innsýn í greiðslu viðskiptavinar getur auðveldað að spá fyrir um hvenær reikningur verður greiddur og auðveldað fyrirtækjum að búa til fínstilltar aðferðir sem auka líkurnar á því að greitt sé á réttum tíma."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: 
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 841ea53f754f61c2930e77fdafc85eac72f47d7a
ms.openlocfilehash: 9e722db6302d7ef51c01601cde245d4f4a333eba
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2018

---

# <a name="customer-payment-insights-preview"></a><span data-ttu-id="e8730-103">Innsýn í greiðslu viðskiptavinar (forútgáfa)</span><span class="sxs-lookup"><span data-stu-id="e8730-103">Customer payment insights (preview)</span></span>

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="e8730-104">Þessi eiginleiki er hluti af markútgáfu og er aðeins í boði fyrir notendur sem hafa valið að taka þátt í einkaforútgáfu.</span><span class="sxs-lookup"><span data-stu-id="e8730-104">This feature is part of a targeted release and is only available to users who have opted into the Private Preview.</span></span> <span data-ttu-id="e8730-105">Þessi eiginleiki verður innifalinn í almennri útgáfu sem er væntanleg.</span><span class="sxs-lookup"><span data-stu-id="e8730-105">This feature will be included in an upcoming general availability release.</span></span>

# <a name="overview"></a><span data-ttu-id="e8730-106">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="e8730-106">Overview</span></span>

<span data-ttu-id="e8730-107">Fyrirtækjum finnst oft krefjandi að spá fyrir um hvenær viðskiptavinur greiðir reikninga sína.</span><span class="sxs-lookup"><span data-stu-id="e8730-107">Organizations often find it challenging to predict when a customer will pay their invoices.</span></span> <span data-ttu-id="e8730-108">Þessi skortur á innsýn getur leitt til ónákvæmra sjóðstreymisspáa, óhagkvæmra innheimtuferla og möguleika á því að pantanir verði afgreiddar viðskiptavinum sem kunna að fela í sér lánsáhættu.</span><span class="sxs-lookup"><span data-stu-id="e8730-108">This lack of insight can lead to inaccurate cash flow forecasts, inefficient collection processes, and the possibility of orders being released to customers who may pose a credit risk.</span></span> <span data-ttu-id="e8730-109">Innsýn í greiðslu viðskiptavinar (forútgáfa) notar vélnám til að spá fyrir um hvenær reikningur verður greiddur.</span><span class="sxs-lookup"><span data-stu-id="e8730-109">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="e8730-110">Hún veitir einnig fínstilltar aðferðir sem hægt er að stilla til að hámarka líkurnar á því að viðskiptavinir greiði á réttum tíma.</span><span class="sxs-lookup"><span data-stu-id="e8730-110">It also provides optimization strategies that can be tailored to maximize the probability of customers paying on time.</span></span>

## <a name="predictions"></a><span data-ttu-id="e8730-111">Spár</span><span class="sxs-lookup"><span data-stu-id="e8730-111">Predictions</span></span>

<span data-ttu-id="e8730-112">Greiðsluspár leyfa fyrirtækjum að bæta viðskiptaferla sína með því að auðvelda það að:</span><span class="sxs-lookup"><span data-stu-id="e8730-112">Payment predictions allow organizations to improve their business processes by helping to:</span></span>

-   <span data-ttu-id="e8730-113">Bera auðveldlega kennsl á reikninga sem spáð er að verði greiddir seint.</span><span class="sxs-lookup"><span data-stu-id="e8730-113">Easily identify the invoices that are predicted to be paid late.</span></span>
-   <span data-ttu-id="e8730-114">Gera viðeigandi ráðstafanir til að bæta líkurnar á að fá greitt á réttum tíma.</span><span class="sxs-lookup"><span data-stu-id="e8730-114">Take appropriate measures to improve chances of getting paid on time.</span></span>

<span data-ttu-id="e8730-115">Innsýn í greiðslu viðskiptavinar (forútgáfa) notar vélnám til að spá fyrir um hvenær reikningur verður greiddur.</span><span class="sxs-lookup"><span data-stu-id="e8730-115">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="e8730-116">Innsýnin notar eldri gögn reikninga, greiðslna og viðskiptavina til að búa til vélnámslíkan sem er notað til að spá fyrir um hvenær reikningur verður greiddur.</span><span class="sxs-lookup"><span data-stu-id="e8730-116">It uses historical invoice, payment, and customer data to create a machine learning model that is used to predict when an invoice will be paid.</span></span>

<span data-ttu-id="e8730-117">Fyrir hvern opinn reikning spáir innsýn í greiðslu viðskiptavinar (forútgáfa) fyrir um þrjá greiðslumöguleika:</span><span class="sxs-lookup"><span data-stu-id="e8730-117">For each open invoice, Customer payment insights (preview) predicts three payment probabilities:</span></span>

-  <span data-ttu-id="e8730-118">Líkur á að greiðsla sé á réttum tíma (innan gjalddaga reiknings).</span><span class="sxs-lookup"><span data-stu-id="e8730-118">Probability of payment being made on time (within the invoice due date).</span></span>
-  <span data-ttu-id="e8730-119">Líkur á að greiðsla sé greidd innan 30 daga frá gjalddaga reiknings.</span><span class="sxs-lookup"><span data-stu-id="e8730-119">Probability of payment being made within 30 days of the invoice due date.</span></span>
-  <span data-ttu-id="e8730-120">Líkur á að greiðsla sé greidd seinna en 30 dögum frá gjalddaga reiknings.</span><span class="sxs-lookup"><span data-stu-id="e8730-120">Probability of payment being made beyond 30 days of the invoice due date.</span></span>

<span data-ttu-id="e8730-121">Líkurnar á greiðslu er hægt er að skoða í spáhlutanum.</span><span class="sxs-lookup"><span data-stu-id="e8730-121">The probability of payments can be viewed in the prediction section.</span></span>

<span data-ttu-id="e8730-122">[![Greiðsluspár](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span><span class="sxs-lookup"><span data-stu-id="e8730-122">[![Payment predictions](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span></span>

<span data-ttu-id="e8730-123">Hverjum reikningi er einnig úthlutað bestu líkum á greiðslu með því að nota eina af atburðarásunum þremur um greiðsluspárlíkur skilgreindar hér að ofan.</span><span class="sxs-lookup"><span data-stu-id="e8730-123">Each invoice is also assigned a winning probability of payment using one of the three predicted payment probabilities scenarios defined above.</span></span> <span data-ttu-id="e8730-124">Atburðarásin með hæstu líkum á greiðslu er atburðarás sem stendur upp úr.</span><span class="sxs-lookup"><span data-stu-id="e8730-124">The scenario with the highest probability of payment is the winning scenario.</span></span>


<span data-ttu-id="e8730-125">Gefum okkur sem dæmi að spá fyrir reikning gefur 71% líkur á að hann verði greiddur á réttum tíma, 13% líkur á að hann verði greiddur innan 30 daga frá gjalddaga og 16% líkur á að hann verði greiddur seinna en 30 dögum frá gjalddaga.</span><span class="sxs-lookup"><span data-stu-id="e8730-125">For example, let’s assume for an invoice the prediction shows a 71 percent probability that the invoice will be paid on time, 13 percent probability that the invoice will be paid within 30 days of due date, and 16 percent probability that the invoice will be paid beyond 30 days of the due date.</span></span> <span data-ttu-id="e8730-126">Bestu líkurnar sýna að reikningurinn verði í atburðarás fyrir greiðslu á réttum tíma, þannig að reikningurinn verði merktur með líkum á því að hann verði greiddur á réttum tíma.</span><span class="sxs-lookup"><span data-stu-id="e8730-126">The highest probability shows that the invoice will be in the on-time scenario, so the invoice will be tagged with the probability of being paid on time.</span></span>

<span data-ttu-id="e8730-127">[![Greiðsluspár](./media/payment-predict.png)](./media/payment-predict.png)</span><span class="sxs-lookup"><span data-stu-id="e8730-127">[![Payment predictions](./media/payment-predict.png)](./media/payment-predict.png)</span></span>

## <a name="optimization-strategies"></a><span data-ttu-id="e8730-128">Fínstillingaraðferðir</span><span class="sxs-lookup"><span data-stu-id="e8730-128">Optimization strategies</span></span>

<span data-ttu-id="e8730-129">Ásamt greiðsluspám getur innsýn í greiðslu viðskiptavinar (forútgáfa) notað fínstillingaraðferðir til að bæta líkurnar á því að fá greitt á réttum tíma.</span><span class="sxs-lookup"><span data-stu-id="e8730-129">In addition to payment predictions, the Customer Payment Insights (preview) can use optimization strategies to improve the chances of getting paid on time.</span></span> <span data-ttu-id="e8730-130">Þetta gerir fyrirtækjum kleift að gera „Hvað ef“ greiningu með því að leyfa notendum að stilla færibreytur reikninga og viðskiptavina og svo bera saman samsvarandi áhrif á líkurnar á því að fá greiðslu á reikningum á réttum tíma.</span><span class="sxs-lookup"><span data-stu-id="e8730-130">This lets organizations do 'What if' analysis by allowing users to adjust invoice and customer parameters and then compare the corresponding effect on the probability of receiving payment on invoices on time.</span></span>

<span data-ttu-id="e8730-131">Fyrirtæki gæti til dæmis viljað meta áhrifin sem uppfærsla á staðgreiðsluafslætti á reikningum hefur á líkurnar á því að fá greiðsluna á réttum tíma.</span><span class="sxs-lookup"><span data-stu-id="e8730-131">For example, an organization may want to evaluate the effect of updating the cash discount on invoices on the probability of receiving the payment on time.</span></span> <span data-ttu-id="e8730-132">Þegar reikningar eru fínstilltir til að nota nýja afsláttinn, geta notendur farið yfir áhrifin við að nota afslættina hefur á líkurnar á því að fá greiðslur fyrir þessa reikninga á réttum tíma.</span><span class="sxs-lookup"><span data-stu-id="e8730-132">When the invoices are optimized to use the new discount, the users can review the effect of applying the discount on the probability of receiving payments for those invoices on time.</span></span> <span data-ttu-id="e8730-133">Ef kostnaðurinn við að nota afsláttinn er hverfandi í samanburði við ávinning þess að innheimta greiðsluna á réttum tíma, kann fyrirtækið að velja að nota valinn afslátt fyrir allar opnar pantanir í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="e8730-133">If the cost of applying the discount is minimal when compared to the benefit of collecting the payment on time, the organization may choose to apply the selected discount to all future open orders.</span></span>

> [!NOTE] 
> <span data-ttu-id="e8730-134">Eins og staðan er nú er afsláttur aðeins í boði sem fínstillingaraðferð fyrir innsýn í greiðslu viðskiptavinar (forútgáfa).</span><span class="sxs-lookup"><span data-stu-id="e8730-134">Currently, only discount is available as an optimization strategy for Customer payment insights (preview).</span></span>

<span data-ttu-id="e8730-135">[![Fínstilltar spár](./media/optimized-pay.png)](./media/optimized-pay.png)</span><span class="sxs-lookup"><span data-stu-id="e8730-135">[![Optimized predictions](./media/optimized-pay.png)](./media/optimized-pay.png)</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="e8730-136">Hvernig skal nálgast innsýn í greiðslu viðskiptavinar (forútgáfa)</span><span class="sxs-lookup"><span data-stu-id="e8730-136">How to get Customer payment insights (preview)</span></span>

<span data-ttu-id="e8730-137">Ef þú hefur áhuga á að prófa innsýn í greiðslu viðskiptavinar (forútgáfa) skaltu senda tölvupóst til [Hópur forútgáfu á fjármálainnsýn](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="e8730-137">If you are interested in trying Customer payment insights (preview), please email [Finance Insights Preview team](mailto:fiap@microsoft.com).</span></span> 

## <a name="privacy-statement"></a><span data-ttu-id="e8730-138">Yfirlýsing um persónuvernd</span><span class="sxs-lookup"><span data-stu-id="e8730-138">Privacy Statement</span></span>

<span data-ttu-id="e8730-139">Forútgáfur geyma gögn viðskiptavinar í Bandaríkjunum.</span><span class="sxs-lookup"><span data-stu-id="e8730-139">Previews store customer data in the United States.</span></span> <span data-ttu-id="e8730-140">Að auki, forútgáfur (1) geta mögulega notað eki eins miklar persónuverndar- og öryggisráðstafanir og þjónusta Dynamics 365 for Finance and Operations, (2) eru ekki hluti af þjónustustigssamningi fyrir þessa þjónustu, (3) ættu ekki að vera notaðar til að vinna úr persónulegum gögnum eða öðrum gögnum sem falla undir lögboðnar kröfur eða reglur um samræmi og (4) hafa takmarkaðan stuðning.</span><span class="sxs-lookup"><span data-stu-id="e8730-140">In addition, previews (1) may utilize less privacy and security measures than the Dynamics 365 for Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>
