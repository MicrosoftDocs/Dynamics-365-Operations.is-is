---
title: Ekki er hægt að staðfesta sendingu vegna þess að ekki er búið að taka vörurnar til
description: Ekki er hægt að staðfesta sendingu vegna þess að ekki er búið að taka vörurnar til
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938490"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="bf6b5-103">Ekki er hægt að staðfesta sendingu vegna þess að ekki er búið að taka vörurnar til</span><span class="sxs-lookup"><span data-stu-id="bf6b5-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="bf6b5-104">Villukóði: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="bf6b5-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="bf6b5-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="bf6b5-105">Symptoms</span></span>

<span data-ttu-id="bf6b5-106">Þegar reynt er að staðfesta sendingu sýnir kerfið eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="bf6b5-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="bf6b5-107">Sumar vörurnar sem þarf að nota fyrir farm %1 hafa ekki enn verið teknar til og færðar á endanlegan sendingarstað.</span><span class="sxs-lookup"><span data-stu-id="bf6b5-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="bf6b5-108">Því er ekki hægt að staðfesta sendinguna fyrir farminn.</span><span class="sxs-lookup"><span data-stu-id="bf6b5-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="bf6b5-109">Orsök</span><span class="sxs-lookup"><span data-stu-id="bf6b5-109">Cause</span></span>

<span data-ttu-id="bf6b5-110">Ekki er hægt að staðfesta hleðsluna eða sendinguna í núverandi stöðu vegna þess að eitt eftirfarandi skilyrða gæti verið til staðar:</span><span class="sxs-lookup"><span data-stu-id="bf6b5-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="bf6b5-111">Tengt verk hefur ekki enn verið tínt og fært yfir á lokastaðsetningu sendingar.</span><span class="sxs-lookup"><span data-stu-id="bf6b5-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="bf6b5-112">Tiltekið vinnumagn passar ekki við vinnumagn sem var búið til á farmlínunni.</span><span class="sxs-lookup"><span data-stu-id="bf6b5-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>

## <a name="resolution"></a><span data-ttu-id="bf6b5-113">Upplausn</span><span class="sxs-lookup"><span data-stu-id="bf6b5-113">Resolution</span></span>

<span data-ttu-id="bf6b5-114">Athugaðu tengdar sölupantanir eða flutningspantanir fyrir farminn eða sendinguna.</span><span class="sxs-lookup"><span data-stu-id="bf6b5-114">Check the related sales orders or transfer orders for the load or shipment.</span></span> <span data-ttu-id="bf6b5-115">Gangið úr skugga um að tengdu verki hafi verið lokið á lokastaðsetningu sendingar og að magnið stemmi.</span><span class="sxs-lookup"><span data-stu-id="bf6b5-115">Make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="bf6b5-116">Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="bf6b5-116">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="bf6b5-117">Veljið hleðsluna sem ekki er hægt að staðfesta sendinguna fyrir.</span><span class="sxs-lookup"><span data-stu-id="bf6b5-117">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="bf6b5-118">Í flýtiflipanum **Hleðslulínur** skal velja hleðslulínu.</span><span class="sxs-lookup"><span data-stu-id="bf6b5-118">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="bf6b5-119">Gera skal athugasemd um gildið í reitnum **Magn stofnaðs verks**.</span><span class="sxs-lookup"><span data-stu-id="bf6b5-119">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="bf6b5-120">Á aðgerðasvæðinu, í flipanum **Hleðslur**, í flokknum **Tengdar upplýsingar**, skal velja **Verk**.</span><span class="sxs-lookup"><span data-stu-id="bf6b5-120">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="bf6b5-121">Staðfestið að verkinu sé lokið á lokastaðsetningu sendingar og að tínt magn verksins stemmi við magn stofnaðs verks í hleðslulínunni.</span><span class="sxs-lookup"><span data-stu-id="bf6b5-121">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="bf6b5-122">Þetta ferli er endurtekið fyrir allar hleðslulínur til að ganga úr skugga um að öll viðmið séu uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="bf6b5-122">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>
