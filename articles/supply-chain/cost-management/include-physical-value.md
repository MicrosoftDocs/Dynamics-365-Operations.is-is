---
title: "Taka efnislegt virði með"
description: "Gátreiturinn Taka með efnislegt virði á flýtiflipanum Birgðalíkan í skjámyndinni Vörulíkanaflokkar er notaður til að tilgreina hvort efnislega uppfærðar færslur eru teknar með þegar meðaltal kostnaðarverðs er reiknað út fyrir vöru."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4ea8fe31588dd0768e0651c9e1e332212a00cde2
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="include-physical-value"></a><span data-ttu-id="870c6-103">Taka efnislegt virði með</span><span class="sxs-lookup"><span data-stu-id="870c6-103">Include physical value</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="870c6-104">Gátreiturinn Taka með efnislegt virði á flýtiflipanum Birgðalíkan í skjámyndinni Vörulíkanaflokkar er notaður til að tilgreina hvort efnislega uppfærðar færslur eru teknar með þegar meðaltal kostnaðarverðs er reiknað út fyrir vöru.</span><span class="sxs-lookup"><span data-stu-id="870c6-104">You use the Include physical value check box on the Inventory model FastTab of the Item model groups page to specify whether physically updated transactions are considered when the running average cost price is calculated for an item.</span></span>

<span data-ttu-id="870c6-105">Gátreiturinn **Taka með efnislegt virði** hefur eftirfarandi gildi.</span><span class="sxs-lookup"><span data-stu-id="870c6-105">The **Include physical value** check box has the following values.</span></span>

| <span data-ttu-id="870c6-106">Gildi</span><span class="sxs-lookup"><span data-stu-id="870c6-106">Value</span></span>    | <span data-ttu-id="870c6-107">Niðurstaða</span><span class="sxs-lookup"><span data-stu-id="870c6-107">Result</span></span>                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="870c6-108">Valið</span><span class="sxs-lookup"><span data-stu-id="870c6-108">Selected</span></span> | <span data-ttu-id="870c6-109">Bæði efnislega og fjárhagslega uppfærðar færslur eru notaðar til að reikna út meðalkostnaðarverðið.</span><span class="sxs-lookup"><span data-stu-id="870c6-109">Both physically updated transactions and financially updated transactions are used to calculate the running average cost price.</span></span> |
| <span data-ttu-id="870c6-110">Hreinsað</span><span class="sxs-lookup"><span data-stu-id="870c6-110">Cleared</span></span>  | <span data-ttu-id="870c6-111">Aðeins fjárhagslega uppfærðar færslur eru notaðar til að reikna meðalkostnaðarverðið.</span><span class="sxs-lookup"><span data-stu-id="870c6-111">Only financially updated transactions are used to calculate the running average cost price.</span></span>                                     |

<span data-ttu-id="870c6-112">Gátreiturinn hefur svolítið ólík áhrif eftir því hvaða birgðalíkan er notað.</span><span class="sxs-lookup"><span data-stu-id="870c6-112">The check box has slightly different effects, depending on the inventory model that you use.</span></span>

-   <span data-ttu-id="870c6-113">Ef valinn er gátreiturinn **Taka með efnislegt virði** þegar FIFO (Fyrst inn, fyrst út), LIFO (Síðast inn, fyrst út) eða LIFO birgðalíkanið er notað gerir birgðalokun líka leiðréttingar á efnislega uppfærðum færslum.</span><span class="sxs-lookup"><span data-stu-id="870c6-113">If you select the **Include physical value** check box when you use the FIFO (First in, first out), LIFO (Last in, first out), or LIFO date inventory model, inventory close also makes adjustments to physically updated transactions.</span></span>
-   <span data-ttu-id="870c6-114">Ef gátreiturinn **Taka með efnislegt virði** er ekki valinn þegar þessi birgðalíkön eru notuð mun birgðalokun aðeins gera uppgjör í þeim færslum sem hafa verið fjárhagslega uppfærðar.</span><span class="sxs-lookup"><span data-stu-id="870c6-114">If you don't select the **Include physical value** check box when you use these inventory models, inventory close makes settlements only to financially updated transactions.</span></span>
-   <span data-ttu-id="870c6-115">Þegar notuð eru birgðalíkön vegins meðaltals eða dagsetningarbirgðalíkön vegins meðaltals jafnar birgðalokun eingöngu fjárhagslega uppfærðar færslur hvort sem gátreiturinn **Taka með efnislegt virði** var valinn eða ekki.</span><span class="sxs-lookup"><span data-stu-id="870c6-115">When you use the weighted average or weighted average date inventory model, inventory close settles only financially updated transactions, regardless of whether you select the **Include physical value** check box.</span></span>

<span data-ttu-id="870c6-116">**Dæmi 1** Gátreiturinn **Taka með efnislegt virði** hefur verið valinn og eftirfarandi innkaupapantanir hafa verið mótteknar:</span><span class="sxs-lookup"><span data-stu-id="870c6-116">**Example 1** You've selected the **Include physical value** check box and receive the following purchase orders:</span></span>

-   <span data-ttu-id="870c6-117">Innkaupapöntun fyrir magnið 2 á kostnaðarverði 10,00 USD hefur verið uppfærð með fylgiseðli</span><span class="sxs-lookup"><span data-stu-id="870c6-117">A purchase order for a quantity of 2 and a cost price of USD 10.00 that has been packing slip–updated</span></span>
-   <span data-ttu-id="870c6-118">Innkaupapöntun fyrir magnið 3 á kostnaðarverði 12,00 USD hefur verið uppfærð með reikningi</span><span class="sxs-lookup"><span data-stu-id="870c6-118">A purchase order for a quantity of 3 and a cost price of USD 12.00 that has been invoice-updated</span></span>

<span data-ttu-id="870c6-119">Í þessu tilfelli verður meðalkostnaðarverð 11,20 USD af því að bæði efnislega og fjárhagslega uppfærðar færslur eru notaðar til að reikna út kostnaðarverðið.</span><span class="sxs-lookup"><span data-stu-id="870c6-119">In this case, the running average cost price will be USD 11.20, because both physically updated transactions and financially updated transactions are used to calculate the cost price.</span></span> <span data-ttu-id="870c6-120">**Dæmi 2** Gátreiturinn **Taka með efnislegt virði** hefur ekki verið valinn og kostnaðarverð uppsetningar vörunnar er 10,00 USD.</span><span class="sxs-lookup"><span data-stu-id="870c6-120">**Example 2** You haven't selected the **Include physical value** check box, and the cost price on the item setup is USD 10.00.</span></span> <span data-ttu-id="870c6-121">Innkaupapöntun fyrir magnið 20 á kostnaðarverði 12,00 USD hefur verið móttekin og uppfærð með fylgiseðli.</span><span class="sxs-lookup"><span data-stu-id="870c6-121">You receive a purchase order for a quantity of 20 and a cost price of USD 12.00 that has been packing slip–updated.</span></span> <span data-ttu-id="870c6-122">Þegar sölupöntun er bókuð mun kerfið bóka kostnaðarupphæðina 10,00 USD vegna þess að meðalkostnaðarverðið mun ekki innihalda efnislega bókaðar færslur.</span><span class="sxs-lookup"><span data-stu-id="870c6-122">When a sales order is posted, the posted cost amount is USD 10.00, because the running average cost price won't include physically posted transactions.</span></span> <span data-ttu-id="870c6-123">**Athugasemd:** Til samanburðar, ef gátreiturinn **Taka með efnislegt virði** er valinn þegar sölupöntun er bókuð, verður bókaða kostnaðarupphæðin 12,00 USD.</span><span class="sxs-lookup"><span data-stu-id="870c6-123">**Note:** For comparison, if you select the **Include physical value** check box for this item, when a sales order is posted, the posted cost amount will be USD 12.00.</span></span>




