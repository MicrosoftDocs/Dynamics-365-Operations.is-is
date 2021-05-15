---
title: Ekki er hægt að staðfesta sendingu vegna þess að magnið er núll
description: Ekki er hægt að staðfesta sendingu vegna þess að magnið er núll
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
ms.openlocfilehash: 7a06f0651db741a867e1e9fe7dbab841a928c22b
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938489"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a><span data-ttu-id="266d4-103">Ekki er hægt að staðfesta sendingu vegna þess að magnið er núll</span><span class="sxs-lookup"><span data-stu-id="266d4-103">You can't confirm a shipment because there is zero quantity</span></span>

<span data-ttu-id="266d4-104">Villukóði: LoadLineWarningUpdatedToZero</span><span class="sxs-lookup"><span data-stu-id="266d4-104">Error code: LoadLineWarningUpdatedToZero</span></span>

## <a name="symptoms"></a><span data-ttu-id="266d4-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="266d4-105">Symptoms</span></span>

<span data-ttu-id="266d4-106">Þegar reynt er að staðfesta sendingu sýnir kerfið eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="266d4-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="266d4-107">Hleðslulína fyrir atriði %1 og sendingu %2 hefur verið uppfærð til að hafa núllmagn þar sem uppsetning vanafhendingar leyfir ekki sendingu magns fyrir þetta atriði.</span><span class="sxs-lookup"><span data-stu-id="266d4-107">Load line for item %1 and shipment %2 has been updated to have zero quantity due to underdelivery setup allowing not to ship any quantities for this item.</span></span>

<span data-ttu-id="266d4-108">Því er ekki hægt að staðfesta sendinguna fyrir farminn.</span><span class="sxs-lookup"><span data-stu-id="266d4-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="266d4-109">Orsök</span><span class="sxs-lookup"><span data-stu-id="266d4-109">Cause</span></span>

<span data-ttu-id="266d4-110">Kerfið metur hvort tiltektarmagnið sé innan væntanlegra marka út frá tiltektarmagni, magni hleðslulínu og prósentu vanafhendingar.</span><span class="sxs-lookup"><span data-stu-id="266d4-110">The system evaluates whether the picked quantity is within the expected limits, based on the picked quantity, load line quantity, and underdelivery percentage.</span></span> <span data-ttu-id="266d4-111">Ef kerfið finnur að valið magn í hleðslulínunni sé 0 (núll) er ekki hægt að staðfesta sendinguna.</span><span class="sxs-lookup"><span data-stu-id="266d4-111">If the system finds that the picked quantity on the load line is 0 (zero), you can't confirm the shipment.</span></span> <span data-ttu-id="266d4-112">Til dæmis gæti þetta vandamál komið upp ef hætt hefur verið við vinnu og prósenta vanafhendingar í hleðslulínunni er 100 prósent.</span><span class="sxs-lookup"><span data-stu-id="266d4-112">For example, this issue might occur if work has been canceled, and the underdelivery percentage on the load line is 100 percent.</span></span>

## <a name="resolution"></a><span data-ttu-id="266d4-113">Upplausn</span><span class="sxs-lookup"><span data-stu-id="266d4-113">Resolution</span></span>

<span data-ttu-id="266d4-114">Athugið hleðslulínurnar til að ganga úr skugga um að prósenta vanafhendingar og magn séu í samræmi við tiltektarvinnuna.</span><span class="sxs-lookup"><span data-stu-id="266d4-114">Check your load lines to make sure that the underdelivery percentage and quantities are aligned with the picked work.</span></span>

1. <span data-ttu-id="266d4-115">Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="266d4-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="266d4-116">Veljið hleðsluna sem ekki er hægt að staðfesta sendinguna fyrir.</span><span class="sxs-lookup"><span data-stu-id="266d4-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="266d4-117">Í flýtiflipanum **Hleðslulínur** skal velja hleðslulínu fyrir vöruna sem fer umfram prósentu vanafhendingar.</span><span class="sxs-lookup"><span data-stu-id="266d4-117">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="266d4-118">Breytið gildinu í reitnum **Vanafhending** eða reitnum **Magn** eins og þörf er á.</span><span class="sxs-lookup"><span data-stu-id="266d4-118">Adjust the value of the **Underdelivery** field or the **Quantity** field as required.</span></span>

> [!TIP]
> <span data-ttu-id="266d4-119">Ef vandamálið er enn til staðar gæti þurft að ljúka meira en einni tiltekt fyrir tengdar sölupantanir eða flutningspantanir þar til tiltækt magn er í samræmi vð hleðsluna eða sendinguna.</span><span class="sxs-lookup"><span data-stu-id="266d4-119">If the issue still isn't fixed, you might have to complete more picking work for the related sales orders or transfer orders until the available quantity is aligned with the load or shipment.</span></span>
