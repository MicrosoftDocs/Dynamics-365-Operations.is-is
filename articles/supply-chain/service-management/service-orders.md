---
title: "Þjónustupantanir"
description: "Þjónustupöntun táknar heimsókn sem þjónustutæknimaður fer í til viðskiptavinar á tilteknum degi."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
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
ms.openlocfilehash: 647bbe9cca0167d33048ad07e092708f90b41fc3
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="service-orders"></a><span data-ttu-id="9197c-103">Þjónustupantanir</span><span class="sxs-lookup"><span data-stu-id="9197c-103">Service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="9197c-104">Þjónustupöntun táknar heimsókn sem þjónustutæknimaður fer í til viðskiptavinar á tilteknum degi.</span><span class="sxs-lookup"><span data-stu-id="9197c-104">A service order represents a visit that a service technician makes to a customer site on a specific date.</span></span> <span data-ttu-id="9197c-105">Hver þjónustupöntun samanstendur af einni eða fleiri þjónustupöntunarlínum.</span><span class="sxs-lookup"><span data-stu-id="9197c-105">Each service order consists of one or more service order lines.</span></span> <span data-ttu-id="9197c-106">Þjónustupöntunarlínur tákna fjölda vinnustunda sem þjónustutæknar þurfa að inna af hendi, og tengda hluti, gjöld og þóknanir.</span><span class="sxs-lookup"><span data-stu-id="9197c-106">Service order lines represent the hours of work that must be performed by the service technician, and the related items, expenses, and fees.</span></span>

<span data-ttu-id="9197c-107">Þú getur tengt verkefni og hluti við þjónustupöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="9197c-107">You can attach tasks and objects to a service order line.</span></span> <span data-ttu-id="9197c-108">Þú getur síðan flokkað þjónustupöntunarlínur eftir verkefni eða hlut.</span><span class="sxs-lookup"><span data-stu-id="9197c-108">You can then group service order lines by task or by object.</span></span> <span data-ttu-id="9197c-109">Þú getur einnig tengt hluti sem eru skráðir í birgðum við þjónustupöntunarlínur.</span><span class="sxs-lookup"><span data-stu-id="9197c-109">You can also attach items that are listed in inventory to service order lines.</span></span>

## <a name="create-service-orders"></a><span data-ttu-id="9197c-110">Stofna þjónustupantanir</span><span class="sxs-lookup"><span data-stu-id="9197c-110">Create service orders</span></span>

<span data-ttu-id="9197c-111">Þú getur stofnað þjónustupantanir sem byggjast á þjónustusamningi og línunum sem eru í þeim samningi.</span><span class="sxs-lookup"><span data-stu-id="9197c-111">You can create service orders based on a service agreement and the lines that are contained in that agreement.</span></span> <span data-ttu-id="9197c-112">Þú getur hins vegar búið til þjónustupantanir sem tengjast þjónustusamningi aðeins á því tímabili sem tilgreint er í samningnum.</span><span class="sxs-lookup"><span data-stu-id="9197c-112">However, you can create service orders that are associated with a service agreement only in the period that is specified in the agreement.</span></span> <span data-ttu-id="9197c-113">Til dæmis, ef þjónustusamningur gildir fyrir almanaksárið 2011, getur þú stofnað þjónustupantanir fyrir samninginn frá 1. janúar 2011 til 31. desember 2011.</span><span class="sxs-lookup"><span data-stu-id="9197c-113">For example, if a service agreement is valid for the 2011 calendar year, you can create service orders for the agreement from January 1, 2011, and December 31, 2011.</span></span>

<span data-ttu-id="9197c-114">Þú getur einnig stofnað þjónustupantanir hverja fyrir sig, án þess að tengja þær við samning.</span><span class="sxs-lookup"><span data-stu-id="9197c-114">You can also create service orders individually, without associating them with an agreement.</span></span> <span data-ttu-id="9197c-115">Þessar þjónustupantanir geta verið notaðar til að meðhöndla óundirbúnar eða stakar þjónustuheimsóknir.</span><span class="sxs-lookup"><span data-stu-id="9197c-115">These service orders can be used to handle unscheduled or one-time service visits.</span></span> <span data-ttu-id="9197c-116">Til dæmis, í marsmánuði, vill viðskiptavinurinn að þjónusta sé framkvæmd á tveimur vélum, auk þeirra véla sem eru tilgreindar í þjónustusamningnum.</span><span class="sxs-lookup"><span data-stu-id="9197c-116">For example, in the month of March, your customer wants service to be performed on two machines, in addition to the machines that are specified in the service agreement.</span></span> <span data-ttu-id="9197c-117">Í þessu verkefni stofnar þú þjónustupantanir en tengir þær ekki við samning.</span><span class="sxs-lookup"><span data-stu-id="9197c-117">For this task, you create service orders but do not associate them with an agreement.</span></span>


> [!NOTE]
> <P><span data-ttu-id="9197c-118">Til að búa til þjónustubeiðnir sem ekki tengjast þjónustusamningi þarftu að velja gátreitinn <STRONG>Leyfa án þjónustusamnings</STRONG> í skjámyndinni <STRONG>Færibreytur þjónustustjórnunar</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="9197c-118">To create service orders that are not associated with a service agreement, you must select the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form.</span></span></P>

<span data-ttu-id="9197c-119">**Aðstæður**</span><span class="sxs-lookup"><span data-stu-id="9197c-119">**Scenario**</span></span>

<span data-ttu-id="9197c-120">Eftirfarandi atburðarás lýsir öðrum aðstæðum þar sem það er gagnlegt að stofna þjónustupöntun sem ekki er tengd þjónustusamningi.</span><span class="sxs-lookup"><span data-stu-id="9197c-120">The following scenario describes another situation where it is useful to create a service order that is not associated with a service agreement.</span></span>

<span data-ttu-id="9197c-121">Fyrirtækissendandinn fær símtal þar sem beðið er um neyðarþjónustu í lyftu.</span><span class="sxs-lookup"><span data-stu-id="9197c-121">The company dispatcher receives a call requesting emergency service on an elevator.</span></span> <span data-ttu-id="9197c-122">Það er ekki tími til að setja upp þjónustusamning og verkefni fyrir þjónustuna.</span><span class="sxs-lookup"><span data-stu-id="9197c-122">There is no time to set up a service agreement and a project for the service.</span></span> <span data-ttu-id="9197c-123">Þess vegna stofnar sendandinn þjónustupöntun beint í skjámyndinni **Þjónustupantanir**, tengir þjónustupöntunina við verkefni sem er til staðar og stofnar þjónustupöntunarlínur.</span><span class="sxs-lookup"><span data-stu-id="9197c-123">Therefore, the dispatcher creates a service order directly in the **Service orders** form, attaches the service order to an existing project, and creates the service order lines.</span></span> <span data-ttu-id="9197c-124">Sendandinn stofnar einnig verkefni eða hlutatengsl við þjónustupöntun sem er til staðar, til að skrá vinnu sem ekki tengist þjónustusamningnum.</span><span class="sxs-lookup"><span data-stu-id="9197c-124">The dispatcher also creates a task or object relation for an existing service order, to record work that is not related to the service agreement.</span></span> <span data-ttu-id="9197c-125">Nánari upplýsingar er að finna í: [Stofna þjónustupantanir handvirkt](create-service-orders-manually.md) og [Stofna tengsl þjónustuverks](create-service-task-relations.md).</span><span class="sxs-lookup"><span data-stu-id="9197c-125">For more information, see [Create service orders manually](create-service-orders-manually.md) and [Create service task relations](create-service-task-relations.md).</span></span>

## <a name="monitor-the-progress-of-service-orders"></a><span data-ttu-id="9197c-126">Fylgjast með framvindu þjónustupantana</span><span class="sxs-lookup"><span data-stu-id="9197c-126">Monitor the progress of service orders</span></span>

<span data-ttu-id="9197c-127">Til að fylgjast með framvindu þjónustupantana í gegnum mismunandi hópa og vinnuferla, er hægt að setja upp kerfi sem byggist á stigum og ástæðukóðum fyrir þjónustupantanir.</span><span class="sxs-lookup"><span data-stu-id="9197c-127">To monitor the progress of a sales order through the different teams and work processes, you can set up a system of stages and reason codes for service orders.</span></span> <span data-ttu-id="9197c-128">Fyrir hvert stig er hægt að tilgreina aðgerðir sem eru leyfðar.</span><span class="sxs-lookup"><span data-stu-id="9197c-128">For each stage, you can specify the actions that are allowed.</span></span> <span data-ttu-id="9197c-129">Nánari upplýsingar er að finna í [Stofna ástæðukóða](create-reason-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9197c-129">For more information, see [Create reason codes](create-reason-codes.md).</span></span>

<span data-ttu-id="9197c-130">**Dæmi**</span><span class="sxs-lookup"><span data-stu-id="9197c-130">**Example**</span></span>

<span data-ttu-id="9197c-131">Þjónustupöntun er samþykkt af sendanda.</span><span class="sxs-lookup"><span data-stu-id="9197c-131">A service order is approved by the dispatcher.</span></span> <span data-ttu-id="9197c-132">Sendandinn uppfærir stig þjónustupöntunar og tilgreinir ástæðukóða sem gefur til kynna að þjónustupöntunin hafi verið gefin út til þjónustutæknimanns.</span><span class="sxs-lookup"><span data-stu-id="9197c-132">The dispatcher updates the stage of the service order and specifies a reason code that indicates that the service order has been released to the service technician.</span></span> <span data-ttu-id="9197c-133">Tæknimaðurinn fer til viðskiptavinar og sinnir þjónustunni.</span><span class="sxs-lookup"><span data-stu-id="9197c-133">The technician goes to the customer site and performs the service.</span></span>

## <a name="specify-item-requirements-for-service-orders"></a><span data-ttu-id="9197c-134">Tilgreina vöruþarfir fyrir þjónustupantanir</span><span class="sxs-lookup"><span data-stu-id="9197c-134">Specify item requirements for service orders</span></span>

<span data-ttu-id="9197c-135">Þú getur tilgreint birgðavörurnar sem eru nauðsynlegar fyrir þjónustupöntunina.</span><span class="sxs-lookup"><span data-stu-id="9197c-135">You can specify the inventory items that are required for service orders.</span></span> <span data-ttu-id="9197c-136">Hins vegar verður þjónustan að tengjast verkefni.</span><span class="sxs-lookup"><span data-stu-id="9197c-136">However, the service order must be associated with a project.</span></span> <span data-ttu-id="9197c-137">Liður kröfur um þjónustu pantanir eru unnin í gegnum verkefni.</span><span class="sxs-lookup"><span data-stu-id="9197c-137">Item requirements for service orders are processed through a project.</span></span> 

<span data-ttu-id="9197c-138">**Dæmi**</span><span class="sxs-lookup"><span data-stu-id="9197c-138">**Example**</span></span>

<span data-ttu-id="9197c-139">Þjónustupantanir sem eru stofnaðar af þjónustusamningi eru unnar af sendanda.</span><span class="sxs-lookup"><span data-stu-id="9197c-139">The service orders that are created from the service agreement are processed by the dispatcher.</span></span> <span data-ttu-id="9197c-140">Fyrir fyrstu þjónustupöntunina áttar sendandinn sig á því að þjónustutæknimaðurinn þarfnast mikilvægs varahlutar sem er ekki til á lager.</span><span class="sxs-lookup"><span data-stu-id="9197c-140">For the first service order, the dispatcher realizes that the service technician requires an important spare part that is not in the on-hand inventory.</span></span> <span data-ttu-id="9197c-141">Af þeim sökum stofnar sendandinn vöruþörf fyrir varahlutinn beint frá þjónustupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="9197c-141">Therefore, the dispatcher creates an item requirement for the spare part directly from the service order.</span></span>

## <a name="move-and-post-lines"></a><span data-ttu-id="9197c-142">Hreyfa og bóka línur</span><span class="sxs-lookup"><span data-stu-id="9197c-142">Move and post lines</span></span>

<span data-ttu-id="9197c-143">Þjónustutæknimaður kemur úr þjónustuheimsókn og breytir þá og uppfærir þjónustupöntunarlínur.</span><span class="sxs-lookup"><span data-stu-id="9197c-143">A service technician returns from a service visit, and then modifies and updates the service order lines.</span></span> <span data-ttu-id="9197c-144">Á meðan á þjónustuheimsókn stóð framkvæmdi þjónustutæknimaðurinn þjónustuverk sem var áætlað fyrir næstu þjónustuheimsókn.</span><span class="sxs-lookup"><span data-stu-id="9197c-144">During the service visit, the technician performed a service job that was scheduled for the next service visit.</span></span> <span data-ttu-id="9197c-145">Þess vegna færir tæknimaðurinn línurnar frá næstu þjónustuheimsókn yfir á núverandi þjónustuheimsókn.</span><span class="sxs-lookup"><span data-stu-id="9197c-145">Therefore, the technician moves the lines from the next service visit to the current service visit.</span></span> <span data-ttu-id="9197c-146">Tæknimaðurinn bókar síðan þjónustupöntunina.</span><span class="sxs-lookup"><span data-stu-id="9197c-146">The technician then posts the service order.</span></span> <span data-ttu-id="9197c-147">Nánari upplýsingar er að finna í [Færa þjónustupöntunarlínur](move-service-order-lines.md).</span><span class="sxs-lookup"><span data-stu-id="9197c-147">For more information, see [Move service order lines](move-service-order-lines.md).</span></span>

## <a name="cancel-service-orders"></a><span data-ttu-id="9197c-148">Afturkalla þjónustupantanir</span><span class="sxs-lookup"><span data-stu-id="9197c-148">Cancel service orders</span></span>

<span data-ttu-id="9197c-149">Ein af hinum þjónustupöntununum sem voru búnar til fyrir janúarmánuð verður úrelt vegna þess að hætt er við verkið.</span><span class="sxs-lookup"><span data-stu-id="9197c-149">One of the other service orders that was generated for the month of January becomes obsolete, because the job is canceled.</span></span> <span data-ttu-id="9197c-150">Þess vegna hættir þjónustusendandi við þjónustupöntunina.</span><span class="sxs-lookup"><span data-stu-id="9197c-150">Therefore, the service dispatcher cancels the service order.</span></span> <span data-ttu-id="9197c-151">Nánari upplýsingar er að finna í [Hætta við þjónustupantanir](cancel-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="9197c-151">For more information, see [Cancel service orders](cancel-service-orders.md).</span></span>

## <a name="post-from-projects"></a><span data-ttu-id="9197c-152">Bóka frá verkefnum</span><span class="sxs-lookup"><span data-stu-id="9197c-152">Post from projects</span></span>

<span data-ttu-id="9197c-153">Í lok hverrar viku vill sendandinn bóka allar þjónustupantanir sem tengjast ákveðnu verkefni.</span><span class="sxs-lookup"><span data-stu-id="9197c-153">At the end of each week, the dispatcher wants to post all service orders that are attached to a specific project.</span></span> <span data-ttu-id="9197c-154">Afgreiðslustjórinn finnur þess vegna viðeigandi verkefni í skjámyndinni **Verkefni** og bókar þjónustupantanir sem er lokið.</span><span class="sxs-lookup"><span data-stu-id="9197c-154">Therefore, the dispatcher locates the relevant project in the **Projects** form and posts the service orders that have been completed.</span></span> <span data-ttu-id="9197c-155">Nánari upplýsingar er að finna í [Bóka þjónustupantanir (klasaskjámynd)](https://technet.microsoft.com/en-us/library/aa574685\(v=ax.60\)).</span><span class="sxs-lookup"><span data-stu-id="9197c-155">For more information, see [Post service orders (class form)](https://technet.microsoft.com/en-us/library/aa574685\(v=ax.60\)).</span></span>

## <a name="delete-service-orders"></a><span data-ttu-id="9197c-156">Eyða þjónustupöntunum</span><span class="sxs-lookup"><span data-stu-id="9197c-156">Delete service orders</span></span>

<span data-ttu-id="9197c-157">Á seinni hluta ársins ákveður viðskiptavinurinn að þjónustuheimsóknirnar séu of fáar.</span><span class="sxs-lookup"><span data-stu-id="9197c-157">During the second half of the year, your customer decides that the service visits are too infrequent.</span></span> <span data-ttu-id="9197c-158">Stofna þarf nýja og tíðari röð af þjónustuheimsóknum fyrir þann tíma sem eftir er í þjónustusamningnum.</span><span class="sxs-lookup"><span data-stu-id="9197c-158">You must create a new, more frequent series of service visits for the remaining time on the service agreement.</span></span> <span data-ttu-id="9197c-159">Þess vegna verður þú að eyða núverandi þjónustupöntunum og stofna nýjar í staðinn.</span><span class="sxs-lookup"><span data-stu-id="9197c-159">Therefore, you must delete the existing service orders and create new service orders.</span></span> <span data-ttu-id="9197c-160">Nánari upplýsingar er að finna í [Eyða þjónustupöntunum](delete-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="9197c-160">For more information, see [Delete service orders](delete-service-orders.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="9197c-161">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="9197c-161">See also</span></span>

<span data-ttu-id="9197c-162">[Þjónustupantanir (skjámynd)](https://technet.microsoft.com/en-us/library/aa554361\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="9197c-162">[Service orders (form)](https://technet.microsoft.com/en-us/library/aa554361\(v=ax.60\))</span></span>

  


