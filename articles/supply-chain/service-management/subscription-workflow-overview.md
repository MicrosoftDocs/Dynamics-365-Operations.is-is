---
title: Yfirlit yfir vinnuflæði áskrifta
description: Þetta efnisatriði veitir yfirlit yfir vinnuflæði áskrifta.
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b5cff6910dcb273fc081443546676426387f6625
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566411"
---
# <a name="subscription-workflow-overview"></a><span data-ttu-id="ba0e8-103">Yfirlit yfir vinnuflæði áskrifta</span><span class="sxs-lookup"><span data-stu-id="ba0e8-103">Subscription workflow overview</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="ba0e8-104">Þú ert umsjónarmaður áskrifta fyrir ljósafyrirtæki sem býður upp á áskriftir fyrir viðhald á ljósabúnaði.</span><span class="sxs-lookup"><span data-stu-id="ba0e8-104">You are the subscriptions administrator for a light company that offers subscriptions for lighting rig maintenance.</span></span> <span data-ttu-id="ba0e8-105">Viðskiptavinur hefur samband við fyrirtækið þitt til að kaupa árlega áskrift fyrir viðhald á ljósabúnaði.</span><span class="sxs-lookup"><span data-stu-id="ba0e8-105">A customer contacts your company to purchase a yearly subscription for lighting rig maintenance.</span></span>

## <a name="setting-up-subscriptions"></a><span data-ttu-id="ba0e8-106">Áskriftir settar upp</span><span class="sxs-lookup"><span data-stu-id="ba0e8-106">Setting up subscriptions</span></span>

<span data-ttu-id="ba0e8-107">Til að setja upp áskrift verður þú fyrst að búa til áskriftarflokk fyrir nýja þjónustusamninginn eða staðfesta að áskriftarflokkurinn sé til staðar.</span><span class="sxs-lookup"><span data-stu-id="ba0e8-107">To set up a subscription, you must first create a subscription group for the new service agreement or verify that a subscription group exists.</span></span> <span data-ttu-id="ba0e8-108">Ef áskriftarflokkur er til staðar verður þú að setja hann upp til að reikningsfæra viðskiptavininn árlega og til að safna upp sölutekjum fyrir hvern mánuð ársins.</span><span class="sxs-lookup"><span data-stu-id="ba0e8-108">If a subscription group exists, you must set it up to invoice the customer yearly and to accrue sales revenue every month of the year.</span></span> <span data-ttu-id="ba0e8-109">Nánari upplýsingar um hvernig á að setja upp áskriftir er að finna í [Setja upp áskriftarflokka](set-up-subscription-groups.md).</span><span class="sxs-lookup"><span data-stu-id="ba0e8-109">For more information about how to set up subscriptions, see [Set up subscription groups](set-up-subscription-groups.md).</span></span>

<span data-ttu-id="ba0e8-110">Þegar áskriftarhópur hefur verið stofnaður er hægt að stofna áskrift.</span><span class="sxs-lookup"><span data-stu-id="ba0e8-110">After the subscription group is created, you can create the subscription.</span></span> <span data-ttu-id="ba0e8-111">Nánari upplýsingar um hvernig á að búa til þjónustuáskriftir, sjá [Búa til þjónustuáskriftir út frá áskriftarflokki](create-service-subscriptions-from-subscription-group.md).</span><span class="sxs-lookup"><span data-stu-id="ba0e8-111">For more information about how to create service subscriptions, see [Create service subscriptions from a subscription group](create-service-subscriptions-from-subscription-group.md).</span></span>

## <a name="create-and-modify-subscription-transactions"></a><span data-ttu-id="ba0e8-112">Búðu til og breyttu áskriftarfærslum</span><span class="sxs-lookup"><span data-stu-id="ba0e8-112">Create and modify subscription transactions</span></span>

<span data-ttu-id="ba0e8-113">Eftir að þú hefur sett upp áskriftina stofnarðu færslu áskriftargjalds fyrir fyrsta reikningsfærslutímabilið, sem er eitt ár.</span><span class="sxs-lookup"><span data-stu-id="ba0e8-113">After you set up the subscription, you create the subscription fee transaction for the first invoicing period, which is one year.</span></span> <span data-ttu-id="ba0e8-114">Færslurnar eru af gerðinni **Venjulegt**.</span><span class="sxs-lookup"><span data-stu-id="ba0e8-114">The transactions are of the **Regular** type.</span></span> <span data-ttu-id="ba0e8-115">Þ.a.l. er aðeins hægt að búa til áskriftarfærslu þar sem dagsetning frá og dagsetning til samsvara tímabilunum sem áður voru búin til í skjámyndinni **Tímabilsgerðir**.</span><span class="sxs-lookup"><span data-stu-id="ba0e8-115">Therefore, you can only create subscription transactions where the from date and the to date correspond to periods that were previously created in the **Period types** form.</span></span> <span data-ttu-id="ba0e8-116">Nánari upplýsingar um þóknunarfærslur, sjá [Þóknunarfærslur áskriftar](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="ba0e8-116">For more information about fee transactions, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="ba0e8-117">Eftir að þú hefur sett upp áskriftina fyrir viðskiptavininn þinn, manstu eftir því að þeir hafa samið um 10 prósent afslátt á öllum listaverðum fyrir þjónustuframboð.</span><span class="sxs-lookup"><span data-stu-id="ba0e8-117">After you set up the subscription for your customer, you remember that they have negotiated a 10 percent discount on all list prices for service offerings.</span></span> <span data-ttu-id="ba0e8-118">Þess vegna verður þú að draga úr verði þóknunarfærslu sem þú bjóst til.</span><span class="sxs-lookup"><span data-stu-id="ba0e8-118">Therefore, you must reduce the price of the transaction fee that you created.</span></span>

<span data-ttu-id="ba0e8-119">Síðar um daginn hringir tengiliður viðskiptavinarins að þótt þeir vilji enn þjónustusamninginn fyrir ljósabúnaðinn er á stefnuskránni að kynna til sögunnar nýjan ljósabúnað seinna á árinu.</span><span class="sxs-lookup"><span data-stu-id="ba0e8-119">Later in the day, your customer contact calls to say that, although they still want the service agreement for the lighting rig, they plan to introduce a new lighting rig later in the year.</span></span> <span data-ttu-id="ba0e8-120">Þess vegna þurfa þeir aðeins að tryggja viðhald þar til í október 2013.</span><span class="sxs-lookup"><span data-stu-id="ba0e8-120">Therefore, they only need maintenance coverage until October 2013.</span></span> <span data-ttu-id="ba0e8-121">Til að draga úr fjölda mánaða fyrir áskrift viðskiptavinarins býrðu til nýja þóknunarfærslu áskriftar af gerðinni **Minnkunardagar**.</span><span class="sxs-lookup"><span data-stu-id="ba0e8-121">To reduce the number of months for the customer’s subscription, you create a new subscription fee transaction of the **Reduction days** type.</span></span> <span data-ttu-id="ba0e8-122">Nánari upplýsingar um hvernig á að fækka dögum, sjá [Fækka dögum á áskrifargjöldum](reduce-the-days-on-subscription-fees.md).</span><span class="sxs-lookup"><span data-stu-id="ba0e8-122">For more information about how to reduce days, see [Reduce the days on subscription fees](reduce-the-days-on-subscription-fees.md).</span></span>

## <a name="invoice-and-accrue-subscription-transactions"></a><span data-ttu-id="ba0e8-123">Reikningsfæra og safna saman áskriftarfærslum</span><span class="sxs-lookup"><span data-stu-id="ba0e8-123">Invoice and accrue subscription transactions</span></span>

<span data-ttu-id="ba0e8-124">Þú hefur nú lokið við að setja upp áskriftina og þú ert tilbúin(n) til að reikningsfæra viðskiptavininn fyrir henni.</span><span class="sxs-lookup"><span data-stu-id="ba0e8-124">You have now finished setting up the subscription, and you are ready to invoice your customer for it.</span></span> <span data-ttu-id="ba0e8-125">Frekari upplýsingar um hvernig á að reikningsfæra áskriftir er að finna í [Reikningsfæra áskriftarfærslur](invoice-subscription-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="ba0e8-125">For more information about how to invoice subscriptions, see [Invoice subscription transactions](invoice-subscription-transactions.md).</span></span>

<span data-ttu-id="ba0e8-126">Tveimur dögum síðar hringir viðskiptavinurinn að segja þér að áskriftin skuli reikningsfærð í Bandaríkjadölum, ekki evrum.</span><span class="sxs-lookup"><span data-stu-id="ba0e8-126">Two days later, your customer calls to say that the subscription should be invoiced in U.S. dollars, not Euros.</span></span> <span data-ttu-id="ba0e8-127">Þess vegna stofnarðu kreditnótu og einnig stofnarðu nýja áskriftarfærslu í réttum gjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="ba0e8-127">Therefore, you create a credit note, and you also create a new subscription transaction in the correct currency.</span></span> <span data-ttu-id="ba0e8-128">Nánari upplýsingar um hvernig á að fá kreditfæra áskriftarfærslur er að finna í [Kreditfæra áskriftarfærslur](credit-subscription-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="ba0e8-128">For more information about how to credit subscription transactions, see [Credit subscription transactions](credit-subscription-transactions.md).</span></span>

<span data-ttu-id="ba0e8-129">Í lok hvers mánaðar má safna upp mánaðartekjum frá áskrift viðskiptavinar yfir á rekstrarreikning og VÍV-reikning.</span><span class="sxs-lookup"><span data-stu-id="ba0e8-129">At the end of each month, one month's revenue can be accrued from the customer's subscription to the profit and loss account and the WIP accounts.</span></span> <span data-ttu-id="ba0e8-130">Nánari upplýsingar um hvernig á að safna tekjum vegna áskriftar er að finna í [Safna upp áskriftartekjum](accrue-subscription-revenue.md).</span><span class="sxs-lookup"><span data-stu-id="ba0e8-130">For more information about how to accrue revenue for subscriptions, see [Accrue subscription revenue](accrue-subscription-revenue.md).</span></span>

  


