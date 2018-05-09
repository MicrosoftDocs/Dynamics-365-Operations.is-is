---
title: "Þjónustubil"
description: "Þjónustubil gefur til kynna þá tíðni sem þjónustupöntunarlínur eru stofnaðar fyrir þjónustusamningslínur þegar þjónustupantanir eru stofnaðar."
author: YuyuScheller
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 96443a8135a0a12ae23895c4ceac4da626fd96fa
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="service-intervals"></a><span data-ttu-id="3ce81-103">Þjónustubil</span><span class="sxs-lookup"><span data-stu-id="3ce81-103">Service intervals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3ce81-104">Þjónustusamningsbilið gefur til kynna þá tíðni sem þjónustupöntunarlínur eru stofnaðar fyrir þjónustusamningalínur þegar þjónustupantanir eru stofnaðar sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="3ce81-104">The service agreement interval indicates the frequency with which service order lines are created for service agreement lines when you create service orders automatically.</span></span>

<span data-ttu-id="3ce81-105">Þegar þjónustupantanir eru stofnaðar sjálfkrafa eru þjónustupöntunarlínur stofnaðar samkvæmt bilinu sem hefur verið tilgreint fyrir þjónustusamningslínurnar frá upphafsdagsetningu samningslínunnar.</span><span class="sxs-lookup"><span data-stu-id="3ce81-105">When you create service orders automatically, service order lines are created according to the interval that you have specified for the service agreement line from the start date of the agreement line.</span></span>

<span data-ttu-id="3ce81-106">Ef svæðið **Bil** fyrir þjónustusamningslínu á síðunni **Þjónustusamningar** er autt er línan einskiptis tilvik og hún er ekki notuð til að stofna þjónustupantanir í sífellu.</span><span class="sxs-lookup"><span data-stu-id="3ce81-106">If the **Interval** field of a service agreement line in the **Service agreements** page is blank, the line is a one-time event, and it is not used to create service orders repeatedly.</span></span>

## <a name="example"></a><span data-ttu-id="3ce81-107">Dæmi</span><span class="sxs-lookup"><span data-stu-id="3ce81-107">Example</span></span>

<span data-ttu-id="3ce81-108">Þetta dæmi sýnir hvernig þjónustubil hefur áhrif á þjónustusamningslínur og þjónustupöntunarlínur í þjónustupöntun.</span><span class="sxs-lookup"><span data-stu-id="3ce81-108">This example illustrates how a service interval will affect service agreement lines and service order lines on a service order.</span></span>

### <a name="create-a-service-agreement"></a><span data-ttu-id="3ce81-109">Stofna þjónustusamning</span><span class="sxs-lookup"><span data-stu-id="3ce81-109">Create a service agreement</span></span>

<span data-ttu-id="3ce81-110">Fyrst er stofnaður þjónustusamningur og valmöguleikinn **Sameina þjónustupantanir** stilltur á **Eftir þjónustusamning**.</span><span class="sxs-lookup"><span data-stu-id="3ce81-110">First, you create a service agreement and set the **Combine service orders** option to **By service agreement**.</span></span>

1. <span data-ttu-id="3ce81-111">Smellið á **Þjónustusamningar**</span><span class="sxs-lookup"><span data-stu-id="3ce81-111">Click **Service agreements**</span></span>
2. <span data-ttu-id="3ce81-112">Á **Aðgerðarrúðunni** í flipanum **Þjónustusamningur** í flokknum **Nýr** skal smella á **Þjónustusamning** til að stofna nýjan þjónustusamning.</span><span class="sxs-lookup"><span data-stu-id="3ce81-112">On the **Action Pane**, on the **Service agreement** tab, in the **New** group, click **Service agreement** to create a new service agreement.</span></span>
3. <span data-ttu-id="3ce81-113">Færið inn lýsingu, veljið verk í reitnum **Verkkenni** og færið inn dagsetningu í reitinn **Upphafsdagsetning**.</span><span class="sxs-lookup"><span data-stu-id="3ce81-113">Enter a description, select a project in the **Project ID** field, and enter a date in the **Start date** field.</span></span>
4. <span data-ttu-id="3ce81-114">Í reitnum **Sameina þjónustupantanir**, skal velja **Eftir þjónustusamning**.</span><span class="sxs-lookup"><span data-stu-id="3ce81-114">In the **Combine service orders** field, select **By service agreement**.</span></span>

<span data-ttu-id="3ce81-115">Nú er búið að stofna eftirfarandi þjónustusamninginn:</span><span class="sxs-lookup"><span data-stu-id="3ce81-115">You have now created the following service agreement:</span></span>

| <span data-ttu-id="3ce81-116">Verkefni</span><span class="sxs-lookup"><span data-stu-id="3ce81-116">Project</span></span>      | <span data-ttu-id="3ce81-117">Fyrsti vinnudagur</span><span class="sxs-lookup"><span data-stu-id="3ce81-117">Start date</span></span>                                                                         |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3ce81-118">Verkið</span><span class="sxs-lookup"><span data-stu-id="3ce81-118">Your project</span></span> | <span data-ttu-id="3ce81-119">Dagsetningin sem var tilgreind fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="3ce81-119">The date you specified for the project.</span></span> <span data-ttu-id="3ce81-120">Í þessu dæmi er núgildandi dagsetning notuð.</span><span class="sxs-lookup"><span data-stu-id="3ce81-120">In this example, the current date is used.</span></span> |

### <a name="create-a-service-agreement-line"></a><span data-ttu-id="3ce81-121">Stofna þjónustusamningslínu</span><span class="sxs-lookup"><span data-stu-id="3ce81-121">Create a service agreement line</span></span>

<span data-ttu-id="3ce81-122">Næst er þjónustusamningslína stofnuð sem er með færslugerðina **Klst.**.</span><span class="sxs-lookup"><span data-stu-id="3ce81-122">Next, you create a service agreement line that has the transaction type **Hour**.</span></span>

<span data-ttu-id="3ce81-123">Til að ljúka þessum hluta dæmisins þarf að stofna þjónustubil sem nemur 10 dögum á síðunni **Þjónustubil**.</span><span class="sxs-lookup"><span data-stu-id="3ce81-123">To complete this part of the example, you must create a service interval of 10 days in the **Service intervals** page.</span></span> 

1. <span data-ttu-id="3ce81-124">Veljið þjónustusamninginn sem var nýverið stofnaður.</span><span class="sxs-lookup"><span data-stu-id="3ce81-124">Select the service agreement that you just created.</span></span> 
2. <span data-ttu-id="3ce81-125">Á flýtiflipanum **Línur** skal smella á hnappinn **Bæta við** til að stofna nýja línu í neðri rúðu síðunnar **Þjónustusamningar**.</span><span class="sxs-lookup"><span data-stu-id="3ce81-125">On the **Lines** FastTab, click the **Add** button to create a new line in the lower pane of the **Service agreements** page.</span></span>
3. <span data-ttu-id="3ce81-126">Í reitnum **Færslugerð** skal velja **Klst.**.</span><span class="sxs-lookup"><span data-stu-id="3ce81-126">In the **Transaction type** field, select **Hour**.</span></span>
4. <span data-ttu-id="3ce81-127">Í reitnum **Starfskraftur** skal velja starfskraftinn sem mun afhenda þjónustuna.</span><span class="sxs-lookup"><span data-stu-id="3ce81-127">In the **Worker** field, select the worker who will deliver the service.</span></span>
5. <span data-ttu-id="3ce81-128">Í reitnum **Þjónustubil** skal velja 10-daga bil.</span><span class="sxs-lookup"><span data-stu-id="3ce81-128">In the **Service interval** field, select the 10 days interval.</span></span>

<span data-ttu-id="3ce81-129">Nú er búið að stofna þjónustusamningslínu með eftirfarandi upplýsingum:</span><span class="sxs-lookup"><span data-stu-id="3ce81-129">You have now created a service agreement line with the following information:</span></span>

| <span data-ttu-id="3ce81-130">Færslugerð</span><span class="sxs-lookup"><span data-stu-id="3ce81-130">Transaction type</span></span> | <span data-ttu-id="3ce81-131">Fyrsti vinnudagur</span><span class="sxs-lookup"><span data-stu-id="3ce81-131">Start date</span></span>                               | <span data-ttu-id="3ce81-132">Þjónustubil</span><span class="sxs-lookup"><span data-stu-id="3ce81-132">Service interval</span></span> |
|------------------|------------------------------------------|------------------|
| <span data-ttu-id="3ce81-133">Vinnustund</span><span class="sxs-lookup"><span data-stu-id="3ce81-133">Hour</span></span>             | <span data-ttu-id="3ce81-134">Núgildandi dagsetning.</span><span class="sxs-lookup"><span data-stu-id="3ce81-134">The current date.</span></span>                        | <span data-ttu-id="3ce81-135">Hverja 10 daga</span><span class="sxs-lookup"><span data-stu-id="3ce81-135">Every 10 days</span></span>    |
| <span data-ttu-id="3ce81-136">Starfsmaður</span><span class="sxs-lookup"><span data-stu-id="3ce81-136">Worker</span></span>           | <span data-ttu-id="3ce81-137">Starfskrafturinn sem framkvæmir þjónustuna.</span><span class="sxs-lookup"><span data-stu-id="3ce81-137">The worker who will perform the service.</span></span> |                  |

<span data-ttu-id="3ce81-138">Enginn tímagluggi er tilgreindur fyrir línuna.</span><span class="sxs-lookup"><span data-stu-id="3ce81-138">There is no time window specified for the line.</span></span> 

### <a name="create-planned-service-orders"></a><span data-ttu-id="3ce81-139">Stofna áætlaðar þjónustupantanir</span><span class="sxs-lookup"><span data-stu-id="3ce81-139">Create planned service orders</span></span>

<span data-ttu-id="3ce81-140">Nú er hægt að stofna áætlaðar þjónustupantanir og þjónustupöntunarlínur fyrir komandi mánuð.</span><span class="sxs-lookup"><span data-stu-id="3ce81-140">You can now create planned service orders and service order lines for the coming month.</span></span>

1. <span data-ttu-id="3ce81-141">Á síðunni **Þjónustusamningar**, í **Aðgerðarrúðunni**, í flipanum **Afhenda** skal smella á **Áætlaðar þjónustupantanir**.</span><span class="sxs-lookup"><span data-stu-id="3ce81-141">In the **Service agreements** page, on the **Action Pane**, on the **Deliver** tab, click **Planned service orders**.</span></span>
2. <span data-ttu-id="3ce81-142">Á síðunni **Stofna þjónustupantanir** skal færa inn núgildandi dagsetningu í reitinn **Dagsetning frá**. og dagsetningu sem er einum mánuði frá núgildandi dagsetningu í reitinn **Dagsetning til**.</span><span class="sxs-lookup"><span data-stu-id="3ce81-142">In the **Create service orders** page, enter the current date in the **From date** field and a date that is one month from the current date in the **To date** field.</span></span>
3. <span data-ttu-id="3ce81-143">Stillið sleðann **Klst.** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="3ce81-143">Set the **Hour** slider to **Yes**.</span></span> 
4. <span data-ttu-id="3ce81-144">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="3ce81-144">Click **OK**.</span></span>

<span data-ttu-id="3ce81-145">Ein þjónustupöntunarlína er stofnuð fyrir hverja þjónustupöntun vegna þess að engin flokkun í þjónustupöntuninni er til (skilgreind af valkostinum **Eftir þjónustusamning** í reitnum **Sameina þjónustupantanir**).</span><span class="sxs-lookup"><span data-stu-id="3ce81-145">Because there is no grouping on the service order (defined by the **By service agreement** option in the **Combine service orders** field), one service order line is created per service order.</span></span>

### <a name="service-orders-created"></a><span data-ttu-id="3ce81-146">Þjónustupantanir stofnaðar</span><span class="sxs-lookup"><span data-stu-id="3ce81-146">Service orders created</span></span>

<span data-ttu-id="3ce81-147">Þrjár þjónustupöntunarlínur hafa verið stofnaðar innan tímarammans sem var tilgreindur í svarglugganum **Stofna þjónustupantanir**.</span><span class="sxs-lookup"><span data-stu-id="3ce81-147">Three service order lines have been created within the time frame that you specified in the **Create service orders** dialog box.</span></span> <span data-ttu-id="3ce81-148">Hægt er að skoða þjónustupöntunarlínurnar á síðunni **Þjónustusamningar** (**Aðgerðarrúða** \> flipinn **Afhenda**\>, hnappurinn **Skoða**).</span><span class="sxs-lookup"><span data-stu-id="3ce81-148">You can view the service order lines in the **Service agreements** page (**Action Pane** \> **Deliver** tab \>**View** button).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ce81-149">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="3ce81-149">Related topics</span></span>

[<span data-ttu-id="3ce81-150">Setja upp þjónustubil</span><span class="sxs-lookup"><span data-stu-id="3ce81-150">Set up service intervals</span></span>](set-up-service-intervals.md)  


