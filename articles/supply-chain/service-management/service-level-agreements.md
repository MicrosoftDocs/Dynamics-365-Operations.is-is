---
title: Yfirlit þjónustustigssamninga
description: Í þjónustustigssamningi samþykkir viðskiptavinurinn lágmarks svartíma sem byggir á því hvenær þjónustufyrirtækið skráir málið og hvenær málið er leyst.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f2cfa8b72e515b6237914499af626ff8262429d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974361"
---
# <a name="service-level-agreements-overview"></a><span data-ttu-id="9a83f-103">Yfirlit þjónustustigssamninga</span><span class="sxs-lookup"><span data-stu-id="9a83f-103">Service level agreements overview</span></span>       

[!include [banner](../includes/banner.md)]


<span data-ttu-id="9a83f-104">Þjónustustigssamningur (SLA) er samningur á milli þjónustufyrirtækis og þjónustuviðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="9a83f-104">A service level agreement (SLA) is an agreement between a service company and a service customer.</span></span> <span data-ttu-id="9a83f-105">Í SLA samþykkir viðskiptavinurinn lágmarks svartíma sem byggir á því hvenær þjónustufyrirtækið skráir málið og hvenær málið er leyst.</span><span class="sxs-lookup"><span data-stu-id="9a83f-105">In a SLA, the customer agrees to a minimum response time based on when the service company records the issue and when the issue is resolved.</span></span>

<span data-ttu-id="9a83f-106">SLA framfylgir stöðluðu þjónustustigi sem er boðið viðskiptavinum og gerir það einnig gagnsætt fyrir þjónustufyrirtæki þegar þjónustuverkefni skal lokið.</span><span class="sxs-lookup"><span data-stu-id="9a83f-106">A SLA enforces a standard level of service that is offered to customers, and also makes it transparent to a service company when a service job should be completed.</span></span>

<span data-ttu-id="9a83f-107">Hægt er að jafn marga þjónustustigssamninga og þörf er á til þess að bjóða þjónustuviðskiptavinum mismunandi þjónustustig.</span><span class="sxs-lookup"><span data-stu-id="9a83f-107">Any number of SLAs can be created to offer service customers different levels of service.</span></span>

## <a name="create-a-service-level-agreement"></a><span data-ttu-id="9a83f-108">Stofna þjónustustigssamning</span><span class="sxs-lookup"><span data-stu-id="9a83f-108">Create a service level agreement</span></span>

1.  <span data-ttu-id="9a83f-109">Smellið á **Þjónustustjórnun** \> **Uppsetning** \> **Þjónustusamningar** \> **Þjónustustigssamningar**.</span><span class="sxs-lookup"><span data-stu-id="9a83f-109">Click **Service management** \> **Setup** \> **Service agreements** \> **Service level agreements**.</span></span>

2.  <span data-ttu-id="9a83f-110">Sláðu inn nafn fyrir þjónustustigssamninginn í reitinn **Þjónustustigssamningur**.</span><span class="sxs-lookup"><span data-stu-id="9a83f-110">Type a name for the service level agreement in the **Service level agreement** field.</span></span>

3.  <span data-ttu-id="9a83f-111">Sláðu inn þann tíma sem þú vilt leyfa til að ljúka þjónustusímtölum sem fylgja með þjónustusamningnum.</span><span class="sxs-lookup"><span data-stu-id="9a83f-111">Type the time that you want to allow for completion of service calls that are attached to the service level agreement.</span></span> <span data-ttu-id="9a83f-112">Veldu síðan dagatal ef þú vilt byggja þjónustusamninginn á tilteknu dagatali.</span><span class="sxs-lookup"><span data-stu-id="9a83f-112">Then select a calendar if you want to base the service level agreement on a specific calendar.</span></span>

## <a name="apply-a-service-level-agreement"></a><span data-ttu-id="9a83f-113">Nota þjónustustigssamning</span><span class="sxs-lookup"><span data-stu-id="9a83f-113">Apply a service level agreement</span></span>

<span data-ttu-id="9a83f-114">Þjónustustigssamningurinn er notaður í þjónustusamningi.</span><span class="sxs-lookup"><span data-stu-id="9a83f-114">The SLA is applied directly to a service agreement.</span></span>

<span data-ttu-id="9a83f-115">Þjónustupantanir sem þú stofnar handvirkt og tengir við þjónustusamning sem hefur SLA eru mældar gagnvart SLA.</span><span class="sxs-lookup"><span data-stu-id="9a83f-115">Service orders that you create manually and attach to a service agreement that has an SLA are measured against that SLA.</span></span>

<span data-ttu-id="9a83f-116">Þjónustupantanir sem eru stofnaðar sjálfkrafa eru ekki tengdar við þjónustustigssamning.</span><span class="sxs-lookup"><span data-stu-id="9a83f-116">Service orders that you create automatically are not attached to an SLA.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a><span data-ttu-id="9a83f-117">Nota þjónustustigssamning í þjónustusamningi</span><span class="sxs-lookup"><span data-stu-id="9a83f-117">Apply the service level agreement to the service agreement</span></span>

1.  <span data-ttu-id="9a83f-118">Smellið á **Þjónustustjórnun** \> **Almennt** \> **Þjónustusamningar** \> **þjónustusamningar**.</span><span class="sxs-lookup"><span data-stu-id="9a83f-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="9a83f-119">Veldu þjónustusamning sem þú vilt nota SLA í og smelltu síðan á **Breyta** á **Aðgerðasvæðinu**.</span><span class="sxs-lookup"><span data-stu-id="9a83f-119">Select the service agreement that you want to apply the SLA to, and then click **Edit** on the **Action Pane**.</span></span>

2.  <span data-ttu-id="9a83f-120">Í reitnum **Þjónustustigssamningur** skal velja SLA sem á að úthluta.</span><span class="sxs-lookup"><span data-stu-id="9a83f-120">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a><span data-ttu-id="9a83f-121">Nota þjónustustigssamning í þjónustusamningsflokki</span><span class="sxs-lookup"><span data-stu-id="9a83f-121">Apply the service level agreement to the service agreement group</span></span>

1.  <span data-ttu-id="9a83f-122">Smellið á **Þjónustustjórnun** \> **Uppsetningu** \> **Þjónustusamningar** \> **Þjónustusamningsflokkar**.</span><span class="sxs-lookup"><span data-stu-id="9a83f-122">Click **Service management** \> **Setup** \> **Service agreements** \> **Service agreement groups**.</span></span>

2.  <span data-ttu-id="9a83f-123">Í reitnum **Þjónustustigssamningur** skal velja SLA sem á að úthluta.</span><span class="sxs-lookup"><span data-stu-id="9a83f-123">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="track-time-on-a-service-order-against-an-sla"></a><span data-ttu-id="9a83f-124">Rekja tíma á þjónustupöntun gegn SLA</span><span class="sxs-lookup"><span data-stu-id="9a83f-124">Track time on a service order against an SLA</span></span>

<span data-ttu-id="9a83f-125">Þegar þú stofnar nýja þjónustupöntun fyrir þjónustusamning sem SLA er úthlutað til, hefst tímabilið fyrir afhendingu þjónustunnar og kerfið byrjar að fylgjast með afhendingartímanum.</span><span class="sxs-lookup"><span data-stu-id="9a83f-125">When you create a new service order for a service agreement that an SLA is assigned to, the time interval for the delivery of the service is initiated, and the system starts to track the delivery time.</span></span> <span data-ttu-id="9a83f-126">Að auki getur þú stillt eftirfarandi valkosti:</span><span class="sxs-lookup"><span data-stu-id="9a83f-126">Additionally, you can set the following options:</span></span>

  - <span data-ttu-id="9a83f-127">Hægt er að ræsa og stöðva tímaskráningu í þjónustupöntun til þess að skrá heildartímann sem varið er í þjónustupantanir.</span><span class="sxs-lookup"><span data-stu-id="9a83f-127">You can start and stop time recording on the service order to register the total amount of time that is spent on service orders.</span></span>

  - <span data-ttu-id="9a83f-128">Þú getur fylgst með samræmi við tímabilið sem er stillt í þjónustustigssamningnum.</span><span class="sxs-lookup"><span data-stu-id="9a83f-128">You can monitor compliance with the time interval that is set in the service level agreement.</span></span>

  - <span data-ttu-id="9a83f-129">Þú getur skilgreint ástæðukóða sem þarf að stilla ef farið er fram úr tímabili þjónustustigssamnings.</span><span class="sxs-lookup"><span data-stu-id="9a83f-129">You can define reason codes that must be set if the time interval of the service level agreement is exceeded.</span></span>

## <a name="see-also"></a><span data-ttu-id="9a83f-130">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="9a83f-130">See also</span></span>

[<span data-ttu-id="9a83f-131">Skoða uppfyllingu á þjónustustigssamningum</span><span class="sxs-lookup"><span data-stu-id="9a83f-131">View compliance with service level agreements</span></span>](view-compliance-with-service-level-agreements.md)

  


