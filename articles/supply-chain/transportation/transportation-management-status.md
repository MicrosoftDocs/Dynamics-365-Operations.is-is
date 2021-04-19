---
title: Flutningsstjórnunarstöður
description: Þetta efnisatriði útskýrir hvernig á að búa til flutningsstöðu og varpa þeirri stöðu á stöðu flutningsaðila.
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: f3a2b9e50dddf0f015cdd3f16d6d93fcc03d464d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807609"
---
# <a name="transportation-management-statuses"></a><span data-ttu-id="06fae-103">Flutningsstjórnunarstöður</span><span class="sxs-lookup"><span data-stu-id="06fae-103">Transportation management statuses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06fae-104">Setja upp aðalkóða fyrir flutningsstöður til að túlka kóða sem farmflytjendur útvega.</span><span class="sxs-lookup"><span data-stu-id="06fae-104">Set up master codes for transportation statuses to interpret codes that are provided by your shipping carriers.</span></span> <span data-ttu-id="06fae-105">Þetta gerir notanda kleift að samþætta við farmflytjanda til að gefa upp stöðu.</span><span class="sxs-lookup"><span data-stu-id="06fae-105">This lets you integrate with shipping carriers to provide a status.</span></span> <span data-ttu-id="06fae-106">Flutningsstaða sem gefnar eru upp fyrir flutningsstöðukóða getur hjálpað við að rekja stöðu hleðslu, sending eða gám.</span><span class="sxs-lookup"><span data-stu-id="06fae-106">The transportation status that you provide for a transportation master status code can help you track the status of a load, shipment, or container.</span></span> <span data-ttu-id="06fae-107">Aðeins er hægt að uppfæra tiltekna flutningsstöðu fyrir farm, sendingu eða gám með gagnasamþættingu og ekki handvirkt á notandaviðmótinu.</span><span class="sxs-lookup"><span data-stu-id="06fae-107">The specific transportation status for a load, shipment, or container can only be updated through data integration and not manually through the user interface.</span></span>

## <a name="create-a-transportation-status"></a><span data-ttu-id="06fae-108">Býr til flutningsstöðu</span><span class="sxs-lookup"><span data-stu-id="06fae-108">Create a transportation status</span></span>

<span data-ttu-id="06fae-109">Fylgdu þessum skrefum til að búa til flutningsstöðu:</span><span class="sxs-lookup"><span data-stu-id="06fae-109">To create a transportation status, follow these steps:</span></span>

1. <span data-ttu-id="06fae-110">Opnið **Flutningsstjórnun \> Uppsetning \> Sniðmát flutningsstöðu**.</span><span class="sxs-lookup"><span data-stu-id="06fae-110">Go to **Transportation management \> Setup \> Transportation status masters**.</span></span>
1. <span data-ttu-id="06fae-111">Veldu **Nýtt** til að búa til sniðmát fyrir flutningsstöðu.</span><span class="sxs-lookup"><span data-stu-id="06fae-111">Select **New** to create a transportation status master.</span></span>
1. <span data-ttu-id="06fae-112">Í svæðinu **Sniðmát flutningsstöðu** er færður inn einkvæmur kóði fyrir flutningsstaða.</span><span class="sxs-lookup"><span data-stu-id="06fae-112">In the **Transportation status master** field, enter a unique code for the transportation status.</span></span>
1. <span data-ttu-id="06fae-113">Í reitnum **Flutningsgerð** skal velja annað hvort *Farmflytjandi* eða *Miðstöð* sem gerð flutnings.</span><span class="sxs-lookup"><span data-stu-id="06fae-113">In the **Transportation type** field, select either *Shipping carrier* or *Hub* as the type of transportation.</span></span>
1. <span data-ttu-id="06fae-114">Sláðu inn heiti og flutningsstöðu.</span><span class="sxs-lookup"><span data-stu-id="06fae-114">Enter a name and transportation status.</span></span>
1. <span data-ttu-id="06fae-115">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="06fae-115">Close the page.</span></span>

## <a name="map-a-transportation-status-to-a-carrier-status"></a><span data-ttu-id="06fae-116">Varpa flutningsstöðu í stöðu flutningsaðila</span><span class="sxs-lookup"><span data-stu-id="06fae-116">Map a transportation status to a carrier status</span></span>

<span data-ttu-id="06fae-117">Til að varpa flutningsstöðu á stöðu flutningsaðila skal fylgja eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="06fae-117">To map a transportation status to a carrier status, follow these steps:</span></span>

1. <span data-ttu-id="06fae-118">Opnið **Flutningsstjórnun \> Uppsetning \> Flutningsaðilar \> Flutningsstöður flutningsaðila**.</span><span class="sxs-lookup"><span data-stu-id="06fae-118">Go to **Transportation management \> Setup \> Carriers \> Carrier transportation status**.</span></span>
1. <span data-ttu-id="06fae-119">Veljið **Nýtt** til að varpa kóða frá farmflytjanda til aðalkóða flutningsstöðu.</span><span class="sxs-lookup"><span data-stu-id="06fae-119">Select **New** to map a code from a shipping carrier to a transportation status master code.</span></span>
1. <span data-ttu-id="06fae-120">Velja einkvæmt auðkenni fyrir flutningsþjónustuna og farmflytjanda.</span><span class="sxs-lookup"><span data-stu-id="06fae-120">Select the unique ID for the shipping carrier and the carrier service.</span></span>
1. <span data-ttu-id="06fae-121">Veljið kóða flutningsstöðu sem á að varpa kóðanum fyrir valda farmflytjanda fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="06fae-121">Select the transportation status code that you want to map to the selected shipping carrier's code.</span></span>
1. <span data-ttu-id="06fae-122">Færa skal inn ytri kóðann sem farmflytjandi notar.</span><span class="sxs-lookup"><span data-stu-id="06fae-122">Enter the external code that is used by the shipping carrier.</span></span>
1. <span data-ttu-id="06fae-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="06fae-123">Close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]