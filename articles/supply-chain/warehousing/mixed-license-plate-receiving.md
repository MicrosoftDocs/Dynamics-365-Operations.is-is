---
title: Móttaka blandaðrar númeraplötu
description: Þetta efnisatriði lýsir því hvernig á að nota móttöku á blandaðri númeraplötu til að skrá og stofna vinnu fyrir margar vörur með fartæki.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 15c058887da33b522c5d9a1a8d2c45a5d1566a5d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215770"
---
# <a name="mixed-license-plate-receiving"></a><span data-ttu-id="4620a-103">Móttaka blandaðrar númeraplötu</span><span class="sxs-lookup"><span data-stu-id="4620a-103">Mixed license plate receiving</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4620a-104">Móttaka á blönduðum númeraplötum gerir þér kleift að búa til númeraplötu sem samanstendur af mörgum vörum áður en þú skráir og stofnar frágangsvinnu.</span><span class="sxs-lookup"><span data-stu-id="4620a-104">Mixed license plate receiving allows you to build a license plate consisting of multiple items before you register and create put-away work.</span></span> 

<span data-ttu-id="4620a-105">Ekki þarf að skipta númeraplötu sem samanstendur af mörgum vörum á móttökusvæði, til að hægt sé að skrá hverja vöru.</span><span class="sxs-lookup"><span data-stu-id="4620a-105">A license plate that consists of multiple items does not have to be split at the receiving dock for you to register each item.</span></span> 

<span data-ttu-id="4620a-106">Þegar vörutengt flæði er notað til að auðkenna upprunaskjalslínur, getur þú skannað strikamerki í vörustjórnun.</span><span class="sxs-lookup"><span data-stu-id="4620a-106">When using an item-related flow to identify the source document lines, you can scan bar codes on the item control.</span></span> <span data-ttu-id="4620a-107">Ef strikamerki hefur skilgreint magn og mælieiningu (UOM), verður vörunni og magninu sjálfkrafa bætt við blandaða númeraplötu og svo ferðu aftur í skjámyndina til að skanna aðra vöru.</span><span class="sxs-lookup"><span data-stu-id="4620a-107">If the bar code has a quantity and a unit of measure (UOM) configured on it, the item and quantity will automatically be added to the mixed license plate, and you will be returned to the screen to scan another item.</span></span> <span data-ttu-id="4620a-108">Þetta gerir þér kleift að skanna á skjótan hátt allar vörurnar án þess að það þurfi að staðfesta í hverju skrefi.</span><span class="sxs-lookup"><span data-stu-id="4620a-108">This allows you to quickly scan all the items without having to make a confirmation at each step.</span></span> 

<span data-ttu-id="4620a-109">Í móttökuflæði fyrir blandaða númeraplötu getur þú birt lista yfir þær vörur sem hafa þegar verið skannaðar á númeraplötu og þar geturðu breytt eða leiðrétt magn vöru.</span><span class="sxs-lookup"><span data-stu-id="4620a-109">In the flow for mixed license plate receiving, you can display the list of items that are already scanned to the license plate and from here you can modify or correct the quantity of an item.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="4620a-110">Þar sem það á við</span><span class="sxs-lookup"><span data-stu-id="4620a-110">Where it applies</span></span>

<span data-ttu-id="4620a-111">Móttaka á blandaðri númeraplötu er móttökuflæði á fartæki til að skrá og stofna vinnu fyrir margar línur/vörur samtímis.</span><span class="sxs-lookup"><span data-stu-id="4620a-111">Mixed license plate receiving is a mobile device receiving flow to register and create work for multiple lines/items at the same time.</span></span> <span data-ttu-id="4620a-112">Þetta er gagnlegt ef þú tekur á móti númeraplötum á innleið með mörgum vörum.</span><span class="sxs-lookup"><span data-stu-id="4620a-112">This is useful if you receive inbound license plates with multiple items.</span></span> 

## <a name="how-to-set-up-mixed-license-plate-receiving"></a><span data-ttu-id="4620a-113">Uppsetning á móttöku blandaðrar númeraplötu</span><span class="sxs-lookup"><span data-stu-id="4620a-113">How to set up mixed license plate receiving</span></span>
<span data-ttu-id="4620a-114">Móttaka á blandaðri númeraplötu er sett upp sem valmyndaratriði á fartæki.</span><span class="sxs-lookup"><span data-stu-id="4620a-114">Mixed license plate receiving is set up as a mobile device menu item.</span></span>

<span data-ttu-id="4620a-115">Stofna þarf nýtt valmyndaratriði með vinnuham sem notast ekki við fyrirliggjandi vinnu og notast við eina af eftirtöldum aðferðum:</span><span class="sxs-lookup"><span data-stu-id="4620a-115">You need to create a new menu item with mode work that does not use existing work and use one of the following methods:</span></span>

- <span data-ttu-id="4620a-116">Móttaka blandaðrar númeraplötu</span><span class="sxs-lookup"><span data-stu-id="4620a-116">Mixed license plate receiving</span></span>
- <span data-ttu-id="4620a-117">Móttaka og frágangur blandaðrar númeraplötu</span><span class="sxs-lookup"><span data-stu-id="4620a-117">Mixed license plate receiving and put away</span></span>

<span data-ttu-id="4620a-118">Valkostir sem eru í boði til að auðkenna upprunaskjalslínur eru vara í innkaupapöntun, innkaupapöntunarlína, skilapöntun, vara í flutningspöntun og flutningspöntunarlína.</span><span class="sxs-lookup"><span data-stu-id="4620a-118">The options to identify the source document lines are purchase order item, purchase order line, return order, transfer order item, and transfer order line.</span></span> <span data-ttu-id="4620a-119">Þessir valkostir geta breytt móttökupöntun á einni númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="4620a-119">These options can change the receiving order on a single license plate.</span></span> <span data-ttu-id="4620a-120">Síðasti valkosturinn er eftir hleðsluvöru.</span><span class="sxs-lookup"><span data-stu-id="4620a-120">The last option is by load item.</span></span> <span data-ttu-id="4620a-121">Hægt er að bæta mörgum vörum við númeraplötu en ekki er hægt að skipta milli margra hleðsla.</span><span class="sxs-lookup"><span data-stu-id="4620a-121">You can add multiple items to a license plate, but you cannot switch between multiple loads.</span></span>
