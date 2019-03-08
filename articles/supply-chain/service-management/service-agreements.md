---
title: Þjónustusamningar
description: Með þjónustusamningum er hægt að skilgreina tilföngin sem eru notuð í dæmigerðri þjónustuheimsókn og hvernig þessi tilföng eru reikningsfærð á viðskiptavininn.
author: ShylaThompson
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c6425dcf1c89f625d997be0dd4a52aaecb6e6d65
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "315039"
---
# <a name="service-agreements"></a><span data-ttu-id="e28aa-103">Þjónustusamningar</span><span class="sxs-lookup"><span data-stu-id="e28aa-103">Service agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e28aa-104">Með þjónustusamningum er hægt að skilgreina tilföngin sem eru notuð í dæmigerðri þjónustuheimsókn og hvernig þessi tilföng eru reikningsfærð á viðskiptavininn.</span><span class="sxs-lookup"><span data-stu-id="e28aa-104">Service agreements let you define the resources that are used in a typical service visit and how those resources are invoiced to the customer.</span></span>

<span data-ttu-id="e28aa-105">Allir þjónustusamningar eru tengdir við verk sem færslur eru bókaðar á og reikningsfærðar.</span><span class="sxs-lookup"><span data-stu-id="e28aa-105">Every service agreement is attached to a project through which transactions are posted and invoiced.</span></span> <span data-ttu-id="e28aa-106">Engu að síður er einnig hægt að reikningsfæra færslur þjónustupöntunar beint í gegnum verk án þess að þurfa fyrst að tengja þjónustupöntun við þjónustusamning.</span><span class="sxs-lookup"><span data-stu-id="e28aa-106">However, you can also invoice service order transactions directly through the project without first having to connect the service order to a service agreement.</span></span> <span data-ttu-id="e28aa-107">Þetta mætti til dæmis gera þegar þjónustupöntun hefur aðeins eina þjónustuheimsókn og mikilvægara er að vinna þjónustufærslur fljótt en að skrá nákvæmar upplýsingar um viðskiptavininn yfir langt tímabil fyrir þjónustusamninginn.</span><span class="sxs-lookup"><span data-stu-id="e28aa-107">You might decide to do this if the service order is for a one-time-only service visit and the need for processing the service transactions quickly outweighs the need for maintaining detailed service-agreement information about the customer over a period of time.</span></span>

## <a name="service-agreement"></a><span data-ttu-id="e28aa-108">Þjónustusamningur</span><span class="sxs-lookup"><span data-stu-id="e28aa-108">Service agreement</span></span>

<span data-ttu-id="e28aa-109">Tilgreina verður verk, kenni þjónustusamnings og flokk þjónustusamnings í öllum þjónustusamningum.</span><span class="sxs-lookup"><span data-stu-id="e28aa-109">In each service agreement, you must specify a project, a service-agreement ID, and a service-agreement group.</span></span> <span data-ttu-id="e28aa-110">Nota má flokk þjónustusamnings til að raða og skipuleggja þjónustusamninga.</span><span class="sxs-lookup"><span data-stu-id="e28aa-110">The service-agreement group can be used to sort and organize service agreements.</span></span>

<span data-ttu-id="e28aa-111">Haus þjónustusamnings inniheldur stillingar sem eiga við allar tengdar þjónustusamningslínur:</span><span class="sxs-lookup"><span data-stu-id="e28aa-111">A service agreement header contains settings that apply to all attached agreement lines:</span></span>

-  <span data-ttu-id="e28aa-112">Hvort þjónustusamningurinn sé ógildur.</span><span class="sxs-lookup"><span data-stu-id="e28aa-112">Whether the service agreement is suspended.</span></span> <span data-ttu-id="e28aa-113">Ef þjónustusamningurinn er ógildur er ekki hægt að mynda þjónustupantanir úr þjónustusamningnum.</span><span class="sxs-lookup"><span data-stu-id="e28aa-113">If the service agreement is suspended, you cannot generate service orders from the service agreement.</span></span>
-  <span data-ttu-id="e28aa-114">Lengd þjónustusamningsins.</span><span class="sxs-lookup"><span data-stu-id="e28aa-114">The duration of the service agreement.</span></span>
-  <span data-ttu-id="e28aa-115">Hvernig þjónustupantanalínur eru sameinaðar í þjónustupantanir.</span><span class="sxs-lookup"><span data-stu-id="e28aa-115">How service-order lines are to be combined into service orders.</span></span>
-  <span data-ttu-id="e28aa-116">Hvort þjónustusamningurinn sé sniðmát.</span><span class="sxs-lookup"><span data-stu-id="e28aa-116">Whether the service agreement is a template.</span></span>

<span data-ttu-id="e28aa-117">Allir þjónustuhlutir og þjónustuverk sem hægt er að nota með þjónustusamningnum eru einnig sett upp í haus þjónustusamningsins með því að færa inn þjónustuverk eða þjónustuhlut sem á að tengja við ýmsar línur samningsins.</span><span class="sxs-lookup"><span data-stu-id="e28aa-117">In the service-agreement header, you also set up all the service objects and service tasks that can be used with the service agreement by entering the specific service tasks or service objects that are to be attached to the various lines of the agreement.</span></span>

<span data-ttu-id="e28aa-118">Einnig er hægt að afrita línur þjónustusamnings eða þjónustusniðmáts úr haus þjónustusamnings í gildandi þjónustusamning.</span><span class="sxs-lookup"><span data-stu-id="e28aa-118">From the service-agreement header, you can also copy service-agreement lines or service-template lines into the current service agreement.</span></span>

<span data-ttu-id="e28aa-119">Hægt er að fresta þjónustusamningum og stöðva einstakar þjónustusamningslínur.</span><span class="sxs-lookup"><span data-stu-id="e28aa-119">You can suspend service agreements and stop individual service agreement lines.</span></span>

<span data-ttu-id="e28aa-120">Ef gátreiturinn **Frestað** er valinn fyrir þjónustusamning er ekki hægt að:</span><span class="sxs-lookup"><span data-stu-id="e28aa-120">If you select the **Suspended** check box on a service agreement, you cannot:</span></span>

-    <span data-ttu-id="e28aa-121">Stofna þjónustupantanir sjálfvirkt eða handvirkt út frá þjónustusamningnum.</span><span class="sxs-lookup"><span data-stu-id="e28aa-121">Create service orders automatically or manually from the service agreement.</span></span>

<span data-ttu-id="e28aa-122">Ef gátreiturinn **Stöðvað** er valinn fyrir þjónustusamningslínur er ekki hægt að:</span><span class="sxs-lookup"><span data-stu-id="e28aa-122">If you select the **Stopped** check box on a service agreement line, you cannot:</span></span>

-    <span data-ttu-id="e28aa-123">Stofna þjónustupantanir sjálfvirkt eða handvirkt út frá þjónustusamningslínuna.</span><span class="sxs-lookup"><span data-stu-id="e28aa-123">Create service orders automatically or manually from the service agreement line.</span></span>
-    <span data-ttu-id="e28aa-124">Afritið þjónustusamningslínuna í annan þjónustusamning eða þjónustupöntun.</span><span class="sxs-lookup"><span data-stu-id="e28aa-124">Copy the service agreement line into another service agreement or service order.</span></span>


> [!NOTE]
> <span data-ttu-id="e28aa-125">Ef þjónustusamning er frestað eru allar tengdar línur stöðvaðar óháð einstakri stöðu þeirra.</span><span class="sxs-lookup"><span data-stu-id="e28aa-125">If a service agreement is suspended, all the attached lines are stopped, regardless of their individual status.</span></span>

## <a name="service-agreement-lines"></a><span data-ttu-id="e28aa-126">Þjónustusamningslínur</span><span class="sxs-lookup"><span data-stu-id="e28aa-126">Service-agreement lines</span></span>

<span data-ttu-id="e28aa-127">Línur þjónustusamninga lýsa nákvæmlega efni umbeðinnar þjónustuvinnu.</span><span class="sxs-lookup"><span data-stu-id="e28aa-127">Each service-agreement line describes in detail the content of the proposed service work.</span></span> <span data-ttu-id="e28aa-128">Línurnar innihalda eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="e28aa-128">The lines contain the following settings:</span></span>

-  <span data-ttu-id="e28aa-129">Færslugerð og lýsing á færslugerð.</span><span class="sxs-lookup"><span data-stu-id="e28aa-129">The transaction type and the description of the transaction type.</span></span>
-  <span data-ttu-id="e28aa-130">Starfsmanninn sem framkvæmir vinnuna.</span><span class="sxs-lookup"><span data-stu-id="e28aa-130">The employee who performs the service work.</span></span>
-  <span data-ttu-id="e28aa-131">Hluti sem þarf að þjónusta fyrir þjónustusamninginn.</span><span class="sxs-lookup"><span data-stu-id="e28aa-131">The objects on which service must be performed for the service agreement.</span></span>
-  <span data-ttu-id="e28aa-132">Hve oft vinna er unnin og tengdar vöru-, kostnaðar- þóknanafærslur eru skráðar.</span><span class="sxs-lookup"><span data-stu-id="e28aa-132">The frequency with which work is performed and associated item, expense, and fee transactions are registered.</span></span>
-  <span data-ttu-id="e28aa-133">Tímagluggann sem sameina má þjónustupantanalínur í þjónustupöntun.</span><span class="sxs-lookup"><span data-stu-id="e28aa-133">The time window within which service-order lines can be grouped into a service order.</span></span>
-  <span data-ttu-id="e28aa-134">Þjónustuverkin sem eru notuð til að sameina margar samningslínur í verkefni og til að búa til samantekt fyrir tæknimenn og viðskiptavini um hvaða þjónustuverk eigi að veita.</span><span class="sxs-lookup"><span data-stu-id="e28aa-134">The service tasks that are used to group sets of agreement lines together into work tasks and to summarize for service technicians and customers what service task is to be provided.</span></span>
-  <span data-ttu-id="e28aa-135">Hvort lína hafi verið stöðvuð.</span><span class="sxs-lookup"><span data-stu-id="e28aa-135">Whether a line is stopped.</span></span> <span data-ttu-id="e28aa-136">Ef lína hefur verið stöðvuð er ekki hægt að stofna þjónustupantanir fyrir hana.</span><span class="sxs-lookup"><span data-stu-id="e28aa-136">If a line is stopped, you cannot create service orders for that individual line.</span></span>
-  <span data-ttu-id="e28aa-137">Verkstillingar á borð við tegund og línueiginleika.</span><span class="sxs-lookup"><span data-stu-id="e28aa-137">Project settings, such as the category and the line property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e28aa-138">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="e28aa-138">Related topics</span></span>

[<span data-ttu-id="e28aa-139">Þjónustusamningar stofnaðir</span><span class="sxs-lookup"><span data-stu-id="e28aa-139">Create service agreements</span></span>](create-service-agreements.md)
