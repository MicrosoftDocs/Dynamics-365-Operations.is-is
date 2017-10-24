---
title: "Setja upp viðvaranir vegna svika"
description: "Í þessu efnisatriði er útskýrt hvernig á að setja upp reglur viðvörun viðskiptavinar þjónustu biðlaraþjónustu hugsanlega sviksamleg upplýsinga þegar pantanir eru unnar. Hægt er að skilgreina ákveðna kóða sem nota á til að sjálfvirkt eða handvirkt setja grunsamlegar pantanir í bið."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 09d80015298c3d0219b6ffb290dc456990536a62
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-fraud-alerts"></a><span data-ttu-id="da295-104">Setja upp viðvaranir vegna svika</span><span class="sxs-lookup"><span data-stu-id="da295-104">Set up fraud alerts</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="da295-105">Í þessu efnisatriði er útskýrt hvernig á að setja upp reglur viðvörun viðskiptavinar þjónustu biðlaraþjónustu hugsanlega sviksamleg upplýsinga þegar pantanir eru unnar.</span><span class="sxs-lookup"><span data-stu-id="da295-105">This topic explains how to set up rules to alert customer service representatives of potentially fraudulent information when orders are processed.</span></span> <span data-ttu-id="da295-106">Hægt er að skilgreina ákveðna kóða sem nota á til að sjálfvirkt eða handvirkt setja grunsamlegar pantanir í bið.</span><span class="sxs-lookup"><span data-stu-id="da295-106">You can define specific codes to use to automatically or manually put suspicious orders on hold.</span></span> 

<span data-ttu-id="da295-107">Áður en hægt er að setja upp og nota reglum um eftirlit með svikum verður að virkja eftirlit með svikum og skilgreina grunnupplýsingar um eftirlit með svikum í færibreytum símavers.</span><span class="sxs-lookup"><span data-stu-id="da295-107">Before you set up and use fraud checking rules, you must enable fraud checking and define the basic fraud checking values in the call center parameters.</span></span> <span data-ttu-id="da295-108">Til eru tvær gerðir af reglum gegn svikum:</span><span class="sxs-lookup"><span data-stu-id="da295-108">There are two types of fraud rules:</span></span>

-   <span data-ttu-id="da295-109">**Fastar reglur** nota tiltekið gildi, eins og símanúmer sem hefur verið sett á svartan lista.</span><span class="sxs-lookup"><span data-stu-id="da295-109">**Static rules** use a specific value, such as a phone number that has been blacklisted.</span></span>
-   <span data-ttu-id="da295-110">**Breytilegar reglur** geta samanstaðið af breytum og skilyrðum.</span><span class="sxs-lookup"><span data-stu-id="da295-110">**Dynamic rules** can be composed from variables and conditions.</span></span>

<span data-ttu-id="da295-111">Áður en breytilega regla er stofnuð verður að stofna breytur og skilyrði sem skilgreina hverja reglan á við og hvenær á að nota regluna.</span><span class="sxs-lookup"><span data-stu-id="da295-111">Before you create a dynamic rule, you must create the variables and conditions that define who the rule applies to and when the rule should be applied.</span></span> <span data-ttu-id="da295-112">Til dæmis viltu stofna reglu til að krefjast þess að þegar viðskiptavinur 1202 setur pöntun sem er að andvirði 1.000,00 eða hærra, verður að setja sölupöntun í bið áður en hægt er að staðfesta greiðslu viðskiptavinar..</span><span class="sxs-lookup"><span data-stu-id="da295-112">For example, you want to create a rule to require that any sales order that customer 1202 places that is worth 1,000.00 or more be put on hold until the customer payment can be verified.</span></span> <span data-ttu-id="da295-113">Í þessu dæmi eru breyturnar viðskiptavinur 1202 og pöntunarsamtalan 1.000,00.</span><span class="sxs-lookup"><span data-stu-id="da295-113">In this case, the variables are customer 1202 and an order total of 1,000.00.</span></span> <span data-ttu-id="da295-114">Skilyrðin tilgreina að ef viðskiptavinur 1202 setur pöntun, og heildarupphæð pöntunarinnar er jafnt eða meira en 1.000,00 verður sölupöntunin að fara í bið þar til það er hægt að staðfesta greiðslu viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="da295-114">The condition specifies that if customer 1202 places an order, and the total amount of the order is equal to or more than 1,000.00, the sales order must be put on hold until the customer payment can be verified.</span></span>




