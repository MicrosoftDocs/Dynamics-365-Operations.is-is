---
title: Flutningsstjórnunarstöður
description: Þetta efnisatriði útskýrir hvernig á að búa til flutningsstöðu og varpa þeirri stöðu á stöðu flutningsaðila.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 9d3ed4b73f909b50e97c971a37c548c8c4a9e620
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006467"
---
# <a name="transportation-management-statuses"></a><span data-ttu-id="09fd3-103">Flutningsstjórnunarstöður</span><span class="sxs-lookup"><span data-stu-id="09fd3-103">Transportation management statuses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="09fd3-104">Setja upp aðalkóða fyrir flutningsstöður til að túlka kóða sem farmflytjendur útvega.</span><span class="sxs-lookup"><span data-stu-id="09fd3-104">Set up master codes for transportation statuses to interpret codes that are provided by your shipping carriers.</span></span> <span data-ttu-id="09fd3-105">Þetta gerir notanda kleift að samþætta við farmflytjanda til að gefa upp stöðu.</span><span class="sxs-lookup"><span data-stu-id="09fd3-105">This lets you integrate with shipping carriers to provide a status.</span></span> <span data-ttu-id="09fd3-106">Flutningsstaða sem gefnar eru upp fyrir flutningsstöðukóða getur hjálpað við að rekja stöðu hleðslu, sending eða gám.</span><span class="sxs-lookup"><span data-stu-id="09fd3-106">The transportation status that you provide for a transportation master status code can help you track the status of a load, shipment, or container.</span></span> <span data-ttu-id="09fd3-107">Aðeins er hægt að uppfæra tiltekna flutningsstöðu fyrir farm, sendingu eða gám með gagnasamþættingu og ekki handvirkt á notandaviðmótinu.</span><span class="sxs-lookup"><span data-stu-id="09fd3-107">The specific transportation status for a load, shipment, or container can only be updated through data integration and not manually through the user interface.</span></span>

## <a name="create-a-transportation-status"></a><span data-ttu-id="09fd3-108">Býr til flutningsstöðu</span><span class="sxs-lookup"><span data-stu-id="09fd3-108">Create a transportation status</span></span>

<span data-ttu-id="09fd3-109">Fylgdu þessum skrefum til að búa til flutningsstöðu:</span><span class="sxs-lookup"><span data-stu-id="09fd3-109">To create a transportation status, follow these steps:</span></span>

1. <span data-ttu-id="09fd3-110">Opnið **Flutningsstjórnun \> Uppsetning \> Sniðmát flutningsstöðu**.</span><span class="sxs-lookup"><span data-stu-id="09fd3-110">Go to **Transportation management \> Setup \> Transportation status masters**.</span></span>
1. <span data-ttu-id="09fd3-111">Veldu **Nýtt** til að búa til sniðmát fyrir flutningsstöðu.</span><span class="sxs-lookup"><span data-stu-id="09fd3-111">Select **New** to create a transportation status master.</span></span>
1. <span data-ttu-id="09fd3-112">Í svæðinu **Sniðmát flutningsstöðu** er færður inn einkvæmur kóði fyrir flutningsstaða.</span><span class="sxs-lookup"><span data-stu-id="09fd3-112">In the **Transportation status master** field, enter a unique code for the transportation status.</span></span>
1. <span data-ttu-id="09fd3-113">Í reitnum **Flutningsgerð** skal velja annað hvort *Farmflytjandi* eða *Miðstöð* sem gerð flutnings.</span><span class="sxs-lookup"><span data-stu-id="09fd3-113">In the **Transportation type** field, select either *Shipping carrier* or *Hub* as the type of transportation.</span></span>
1. <span data-ttu-id="09fd3-114">Sláðu inn heiti og flutningsstöðu.</span><span class="sxs-lookup"><span data-stu-id="09fd3-114">Enter a name and transportation status.</span></span>
1. <span data-ttu-id="09fd3-115">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="09fd3-115">Close the page.</span></span>

## <a name="map-a-transportation-status-to-a-carrier-status"></a><span data-ttu-id="09fd3-116">Varpa flutningsstöðu í stöðu flutningsaðila</span><span class="sxs-lookup"><span data-stu-id="09fd3-116">Map a transportation status to a carrier status</span></span>

<span data-ttu-id="09fd3-117">Til að varpa flutningsstöðu á stöðu flutningsaðila skal fylgja eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="09fd3-117">To map a transportation status to a carrier status, follow these steps:</span></span>

1. <span data-ttu-id="09fd3-118">Opnið **Flutningsstjórnun \> Uppsetning \> Flutningsaðilar \> Flutningsstöður flutningsaðila**.</span><span class="sxs-lookup"><span data-stu-id="09fd3-118">Go to **Transportation management \> Setup \> Carriers \> Carrier transportation status**.</span></span>
1. <span data-ttu-id="09fd3-119">Veljið **Nýtt** til að varpa kóða frá farmflytjanda til aðalkóða flutningsstöðu.</span><span class="sxs-lookup"><span data-stu-id="09fd3-119">Select **New** to map a code from a shipping carrier to a transportation status master code.</span></span>
1. <span data-ttu-id="09fd3-120">Velja einkvæmt auðkenni fyrir flutningsþjónustuna og farmflytjanda.</span><span class="sxs-lookup"><span data-stu-id="09fd3-120">Select the unique ID for the shipping carrier and the carrier service.</span></span>
1. <span data-ttu-id="09fd3-121">Veljið kóða flutningsstöðu sem á að varpa kóðanum fyrir valda farmflytjanda fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="09fd3-121">Select the transportation status code that you want to map to the selected shipping carrier's code.</span></span>
1. <span data-ttu-id="09fd3-122">Færa skal inn ytri kóðann sem farmflytjandi notar.</span><span class="sxs-lookup"><span data-stu-id="09fd3-122">Enter the external code that is used by the shipping carrier.</span></span>
1. <span data-ttu-id="09fd3-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="09fd3-123">Close the page.</span></span>
