---
title: Stillingar og aðferð flutningsstjórnunar
description: Þetta efnisatriði sýnir hvernig setja á upp stillingar og aðferðir flutningsstjórnunar.
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
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b9b548212c6f1f3faac56cd7ca182d84cc339bd2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973911"
---
# <a name="transportation-management-modes-and-methods"></a><span data-ttu-id="02295-103">Stillingar og aðferð flutningsstjórnunar</span><span class="sxs-lookup"><span data-stu-id="02295-103">Transportation management modes and methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="02295-104">Flutningsaðferðina táknar flutningsmátastjórnun sem flutningsaðili notar fyrir fragtafhendingar eins og Minna en fullhlaðinn trukkur (LTL) eða Fullhlaðinn trukkur (TL) eða pakkning.</span><span class="sxs-lookup"><span data-stu-id="02295-104">The transportation management  mode represents the type of transport that the carrier uses for freight deliveries, such as less than load (LTL), truckload (TL), or parcel.</span></span> <span data-ttu-id="02295-105">Flutningsaðferðina táknar flutningsmátinn sem flutningsaðili notar fyrir fragtafhendingar eins og flug, landflutninga, sjóflutninga eða lest.</span><span class="sxs-lookup"><span data-stu-id="02295-105">The transportation method represents the form of transport that the carrier uses for freight deliveries, such as air, ground, ocean, or rail.</span></span>

<span data-ttu-id="02295-106">Snið og flutningsaðferðin eru notaðar í mismunandi samhengi.</span><span class="sxs-lookup"><span data-stu-id="02295-106">Modes and transportation methods are used in several contexts.</span></span> <span data-ttu-id="02295-107">Snið eru aðeins notuð í leiðaáætlunum, á meðan bæði snið og flutningsaðferðir eru notaðar við uppsetningu farmflytjanda og flutningsþjónustu.</span><span class="sxs-lookup"><span data-stu-id="02295-107">Only modes are used in route plans, while both modes and transportation methods are used when setting up shipping carriers and carrier services.</span></span> <span data-ttu-id="02295-108">Engin skýr tengsl eða stigveldi eru til staðar á milli stillinga og flutningsaðferða.</span><span class="sxs-lookup"><span data-stu-id="02295-108">No explicit relationship or hierarchy exists between modes and transportation methods.</span></span>

## <a name="create-a-mode"></a><span data-ttu-id="02295-109">Búa til stillingu</span><span class="sxs-lookup"><span data-stu-id="02295-109">Create a mode</span></span>

<span data-ttu-id="02295-110">Fylgdu þessum skrefum til að búa til stillingu:</span><span class="sxs-lookup"><span data-stu-id="02295-110">To create a mode, follow these steps:</span></span>

1. <span data-ttu-id="02295-111">Opnið **Flutningsstjórnun \> Uppsetning \> Flutningsaðilar \> Máti**.</span><span class="sxs-lookup"><span data-stu-id="02295-111">Go to **Transportation management \> Setup \> Carriers \> Mode**.</span></span>
1. <span data-ttu-id="02295-112">Velja skal **Nýtt** til að búa til nýja stillingu.</span><span class="sxs-lookup"><span data-stu-id="02295-112">Select **New** to create a new mode.</span></span>
1. <span data-ttu-id="02295-113">Færið inn einkvæmt kenni og lýsandi heiti fyrir mátann.</span><span class="sxs-lookup"><span data-stu-id="02295-113">Enter a unique ID and a descriptive name for the mode.</span></span>
1. <span data-ttu-id="02295-114">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="02295-114">Close the page.</span></span>

## <a name="create-a-transportation-method"></a><span data-ttu-id="02295-115">Stofna flutningsaðferð</span><span class="sxs-lookup"><span data-stu-id="02295-115">Create a transportation method</span></span>

<span data-ttu-id="02295-116">Til að stofna flutningsaðferð fyrir flytjanda, skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="02295-116">To create a transportation method, follow these steps:</span></span>

1. <span data-ttu-id="02295-117">Opnið **Flutningsstjórnun \> Uppsetning \> Flutningsaðilar \> Flutningsaðferðir**.</span><span class="sxs-lookup"><span data-stu-id="02295-117">Go to **Transportation management \> Setup \> Carriers \> Transportation methods**.</span></span>
1. <span data-ttu-id="02295-118">Veldu **Nýtt** til að stofna nýja flutningsaðferð.</span><span class="sxs-lookup"><span data-stu-id="02295-118">Select **New** to create a new transportation method.</span></span>
1. <span data-ttu-id="02295-119">Færið inn einkvæmt kenni og lýsandi heiti fyrir flutningsaðferðina.</span><span class="sxs-lookup"><span data-stu-id="02295-119">Enter a unique ID and descriptive name for the transportation method.</span></span>
1. <span data-ttu-id="02295-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="02295-120">Close the page.</span></span>
