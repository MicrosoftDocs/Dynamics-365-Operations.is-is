---
title: Ekki er hægt að staðfesta sendingu vegna ólokinnar vinnu eða vinnu sem vantar
description: Ekki er hægt að staðfesta sendingu vegna ólokinnar vinnu eða vinnu sem vantar
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm, WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: beef0909d41e69f3e7bcc1021527be35b7e6fd44
ms.sourcegitcommit: c2c6d687a89bc1534c029109315c23e92865b63b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/31/2021
ms.locfileid: "6123844"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a><span data-ttu-id="66709-103">Ekki er hægt að staðfesta sendingu vegna ólokinnar vinnu eða vinnu sem vantar</span><span class="sxs-lookup"><span data-stu-id="66709-103">You can't confirm a shipment because of incomplete or missing work</span></span>

<span data-ttu-id="66709-104">Villukóði WAX515</span><span class="sxs-lookup"><span data-stu-id="66709-104">Error code: WAX515</span></span>

## <a name="symptoms"></a><span data-ttu-id="66709-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="66709-105">Symptoms</span></span>

<span data-ttu-id="66709-106">Þegar reynt er að staðfesta sendingu sýnir kerfið eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="66709-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="66709-107">Ekki var hægt að staðfesta sendinguna fyrir farm %1 vegna þess að ljúka þarf allri vinnu fyrir farminn.</span><span class="sxs-lookup"><span data-stu-id="66709-107">The shipment for load %1 could not be confirmed because all work for the load must be complete.</span></span>

<span data-ttu-id="66709-108">Því er ekki hægt að staðfesta sendinguna fyrir farminn.</span><span class="sxs-lookup"><span data-stu-id="66709-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="66709-109">Orsök</span><span class="sxs-lookup"><span data-stu-id="66709-109">Cause</span></span>

<span data-ttu-id="66709-110">Hleðslan eða sendingin er í stöðu þar sem staðfesting á sendingu mistókst.</span><span class="sxs-lookup"><span data-stu-id="66709-110">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="66709-111">Áður en þú getur staðfest sendinguna verður að minnsta kosti einhver vinna að vera til fyrir hleðsluna og öll sú vinna verður að vera með stöðuna *Lokuð* eða *Hætt við*.</span><span class="sxs-lookup"><span data-stu-id="66709-111">Before you can confirm the shipment, at least some work must exist for the load, and all that work must have a status of *Closed* or *Canceled*.</span></span>

## <a name="resolution"></a><span data-ttu-id="66709-112">Upplausn</span><span class="sxs-lookup"><span data-stu-id="66709-112">Resolution</span></span>

<span data-ttu-id="66709-113">Athugið tengdar sölupantanir eða flutningspantanir fyrir farminn eða sendinguna og gangið úr skugga um að öll tengd vinna sé lokið eða hætt við.</span><span class="sxs-lookup"><span data-stu-id="66709-113">Check the related sales orders or transfer orders for the load or shipment, and make sure that all the related work has been completed or canceled.</span></span>

<span data-ttu-id="66709-114">Hægt er að vinna með sendingar og hleðslur á nokkrum síðum.</span><span class="sxs-lookup"><span data-stu-id="66709-114">You can work with shipments and loads on several pages.</span></span> <span data-ttu-id="66709-115">Eftirfarandi undirhlutar sýna nokkur dæmi.</span><span class="sxs-lookup"><span data-stu-id="66709-115">The following subsections provide a few examples.</span></span>

### <a name="all-loads-page"></a><span data-ttu-id="66709-116">Síða fyrir allan farm</span><span class="sxs-lookup"><span data-stu-id="66709-116">All loads page</span></span>

1. <span data-ttu-id="66709-117">Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="66709-117">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="66709-118">Veljið hleðsluna sem ekki er hægt að staðfesta sendinguna fyrir.</span><span class="sxs-lookup"><span data-stu-id="66709-118">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="66709-119">Á aðgerðasvæðinu, í flipanum **Hleðslur**, í flokknum **Tengdar upplýsingar**, skal velja **Verk**.</span><span class="sxs-lookup"><span data-stu-id="66709-119">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="66709-120">Skoðaðu stöðu hvers vinnukennis.</span><span class="sxs-lookup"><span data-stu-id="66709-120">Inspect the status of each work ID.</span></span> <span data-ttu-id="66709-121">Fylgið eftir hverju vinnukenni sem er ekki með stöðuna *Lokið* eða *Hætt við*.</span><span class="sxs-lookup"><span data-stu-id="66709-121">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="66709-122">Þegar hvert vinnukenni er með stöðuna *Lokað* eða *Hætt við* skaltu aftur reyna að staðfesta sendinguna.</span><span class="sxs-lookup"><span data-stu-id="66709-122">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-shipments-page"></a><span data-ttu-id="66709-123">Síða fyrir allar sendingar</span><span class="sxs-lookup"><span data-stu-id="66709-123">All shipments page</span></span>

1. <span data-ttu-id="66709-124">Opnið **Vöruhúsakerfi \> Sendingar \> Allar sendingar**.</span><span class="sxs-lookup"><span data-stu-id="66709-124">Go to **Warehouse management \> Shipments\> All shipments**.</span></span>
1. <span data-ttu-id="66709-125">Veljið sendinguna sem ekki er hægt að staðfesta.</span><span class="sxs-lookup"><span data-stu-id="66709-125">Select the shipment that can't be confirmed.</span></span>
1. <span data-ttu-id="66709-126">Á aðgerðasvæðinu, í flipanum **Sendingar**, í flokknum **Vinna**, skal velja **Upplýsingar um verk**.</span><span class="sxs-lookup"><span data-stu-id="66709-126">On the Action Pane, on the **Shipments** tab, in the **Work** group, select **Work details**.</span></span>
1. <span data-ttu-id="66709-127">Skoðaðu stöðu hvers vinnukennis.</span><span class="sxs-lookup"><span data-stu-id="66709-127">Inspect the status of each work ID.</span></span> <span data-ttu-id="66709-128">Fylgið eftir hverju vinnukenni sem er ekki með stöðuna *Lokið* eða *Hætt við*.</span><span class="sxs-lookup"><span data-stu-id="66709-128">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="66709-129">Þegar hvert vinnukenni er með stöðuna *Lokað* eða *Hætt við* skaltu aftur reyna að staðfesta sendinguna.</span><span class="sxs-lookup"><span data-stu-id="66709-129">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-work-page"></a><span data-ttu-id="66709-130">Öll vinnusíða</span><span class="sxs-lookup"><span data-stu-id="66709-130">All work page</span></span>

1. <span data-ttu-id="66709-131">Farið í **Vöruhúsakerfi \> Vinna \> Öll vinna**.</span><span class="sxs-lookup"><span data-stu-id="66709-131">Go to **Warehouse management \> Work\> All work**.</span></span>
1. <span data-ttu-id="66709-132">Veljið verk fyrir pöntunarnúmerið sem ekki er hægt að staðfesta sendinguna fyrir.</span><span class="sxs-lookup"><span data-stu-id="66709-132">Select the work for the order number that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="66709-133">Á aðgerðasvæðinu, í flipanum **Sending**, í flokknum **Sending**, skal velja **Staðfesta sendingu**.</span><span class="sxs-lookup"><span data-stu-id="66709-133">On the Action Pane, on the **Shipment** tab, in the **Shipment** group, select **Confirm shipment**.</span></span>
1. <span data-ttu-id="66709-134">Skoðaðu stöðu hvers vinnukennis.</span><span class="sxs-lookup"><span data-stu-id="66709-134">Inspect the status of each work ID.</span></span> <span data-ttu-id="66709-135">Fylgið eftir hverju vinnukenni sem er ekki með stöðuna *Lokið* eða *Hætt við*.</span><span class="sxs-lookup"><span data-stu-id="66709-135">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="66709-136">Þegar hvert vinnukenni er með stöðuna *Lokað* eða *Hætt við* skaltu aftur reyna að staðfesta sendinguna.</span><span class="sxs-lookup"><span data-stu-id="66709-136">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>
