---
title: "Uppsetning afurða sem hægt er að framleiða eða kaupa"
description: "Vörur geta verið virkjaðar á ýmsa vegu - Hægt er að búa þær til (framleiða) eða versla þær (kaupa). Þessi grein lýsir nokkrum dæmigerðum atriðum til að hafa í huga þegar vörur eru skilgreindar til að styðja fjöl-uppruna."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: a910b5782c8f15cfdd4cf93ea883bc28a5ce8e1a
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---

# <a name="set-up-products-that-can-be-produced-or-procured"></a><span data-ttu-id="27215-104">Uppsetning afurða sem hægt er að framleiða eða kaupa</span><span class="sxs-lookup"><span data-stu-id="27215-104">Set up products that can be produced or procured</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27215-105">Vörur geta verið virkjaðar á ýmsa vegu - Hægt er að búa þær til (framleiða) eða versla þær (kaupa).</span><span class="sxs-lookup"><span data-stu-id="27215-105">Products can be sourced in various ways -  they can be produced (manufactured) or procured (purchased).</span></span> <span data-ttu-id="27215-106">Þessi grein lýsir nokkrum dæmigerðum atriðum til að hafa í huga þegar vörur eru skilgreindar til að styðja fjöl-uppruna.</span><span class="sxs-lookup"><span data-stu-id="27215-106">This article describes some typical points to consider when you configure products to support multi-sourcing.</span></span> 

<span data-ttu-id="27215-107">Fjöl-uppruni er yfirleitt notað fyrir keypta vöru sem er stundum framleidd eða þegar vara var sem var upprunalega framleidd vara er breytt þannig að hún er nú aðallega keypt vara.</span><span class="sxs-lookup"><span data-stu-id="27215-107">Multi-sourcing is typically used for a purchased item that is occasionally manufactured, or when an item that was primarily a manufactured item is changed so that it's now primarily a purchased item.</span></span> <span data-ttu-id="27215-108">Varan er fyrst skilgreind sem framleidd vara svo hægt sé að skilgreina uppskrift (BOM)°og leiðarupplýsingar og til að styðja framleiðslupantanir fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="27215-108">The item is first designated as a manufactured item, so that bill of materials (BOM) and route information can be defined, and to support production orders for the item.</span></span> <span data-ttu-id="27215-109">Framleiðslugerðina ætti að stilla á **BOM** (eða, fyrir framleiðsluferli,°**Formúlu** eða **Aukaafurð**).</span><span class="sxs-lookup"><span data-stu-id="27215-109">The production type should be set to **BOM** (or, for process manufacturing, **Formula** or **Co-Product**).</span></span>

<span data-ttu-id="27215-110">Þegar staðlaður kostnaður er notaður er hægt að reikna vörukostnaðarfærslu fyrir framleiddu vöruna.</span><span class="sxs-lookup"><span data-stu-id="27215-110">When you use standard cost, the item cost record can be calculated for the manufactured item.</span></span> <span data-ttu-id="27215-111">Samt sem áður gæti vörukostnaðarfærsla ekki passað við staðalkostnaðinn sem óskað er eftir fyrir kaup.</span><span class="sxs-lookup"><span data-stu-id="27215-111">However, the item cost record might not match the standard cost that you want for purchasing purposes.</span></span> <span data-ttu-id="27215-112">Í því tilfelli þarf að færa staðalkostnaðinn inn handvirkt og hann þarf að vera virkjaður fyrir vörukostnaðarfærsluna.</span><span class="sxs-lookup"><span data-stu-id="27215-112">In this case, the standard cost must be manually entered and activated for the item cost record.</span></span> <span data-ttu-id="27215-113">Við útreikning kostnaðar ætti að íhuga að nota sérstaka Uppskrift og leið sem tákna blandað framboð afurðar yfir fjárhagstímabil til að lágmarka frávik yfir ákveðið tímabil.</span><span class="sxs-lookup"><span data-stu-id="27215-113">For the cost calculation, consider using a special BOM and route that represent the supply mix of the product over the course of a fiscal period, to minimize the variances over time.</span></span> <span data-ttu-id="27215-114">Þar að auki er hægt að flytja framleidda vöru á einu svæði yfir á annað.</span><span class="sxs-lookup"><span data-stu-id="27215-114">Additionally, a manufactured item at one site can be transferred to another site.</span></span> <span data-ttu-id="27215-115">Þess vegna verður að skrá kostnað vörunnar handvirkt inn og virkja fyrir svæðið sem varan er flutt til.</span><span class="sxs-lookup"><span data-stu-id="27215-115">Therefore, the item's cost must be manually entered and activated for the site that the item is transferred to.</span></span> <span data-ttu-id="27215-116">Þegar framleidda varan er notuð sem íhlutur í flóknari vörum skal fara með kostnað íhlutarins sem keypta vöru.</span><span class="sxs-lookup"><span data-stu-id="27215-116">When you use the manufactured item as a component in higher-level products, the component's costs should be treated as a purchased item.</span></span> <span data-ttu-id="27215-117">Þessi viðmið gilda óháð því°hvort kostnaður íhlutarins var reiknaður eða færður inn handvirkt.</span><span class="sxs-lookup"><span data-stu-id="27215-117">This guideline applies, regardless of whether the component’s costs were calculated or manually entered.</span></span> <span data-ttu-id="27215-118">Uppskriftarútreikningur ætti sem sagt að líta á kostnað vörunnar sem keyptan íhlut frekar en að reikna út kostnað sem°byggist°á uppskriftar- og leiðarupplýsingum hans.</span><span class="sxs-lookup"><span data-stu-id="27215-118">In other words, a BOM calculation should treat the item's costs as a purchased component instead of using the item's BOM and route information to calculate costs.</span></span> 

<span data-ttu-id="27215-119">Hægt er að koma í veg fyrir þennan útreikning með því að velja fánann **Stöðva niðurbrot** sem er felldur inn í flokk uppskriftarútreiknings sem er úthlutaður vörunni.</span><span class="sxs-lookup"><span data-stu-id="27215-119">To prevent the calculation from occurring, select the **Stop explosion** flag that is embedded in the BOM calculation group that is assigned to the item.</span></span> <span data-ttu-id="27215-120">Til°að koma í veg fyrir að útreikningar aðalröðunar brjóti kröfur niður í gegnum vöruna, skal stilla niðurbrotsmarkið á 0 (núll) daga í vöruþekju eða vöruþekjuflokki.</span><span class="sxs-lookup"><span data-stu-id="27215-120">To prevent master scheduling calculations from exploding requirements through the item, set the explosion fence to 0 (zero) days in item coverage or in the coverage group.</span></span> <span data-ttu-id="27215-121">Útreikningur aðalröðunarinnar mun síðan fara með vöruna sem keypta vöru og ekki framkvæma frekari útreikninga fyrir upplýsingar um leið og Uppskrift vörunnar.</span><span class="sxs-lookup"><span data-stu-id="27215-121">The master scheduling calculation will then treat the item as a purchased item and won't perform more calculations for the item's BOM and route information.</span></span>






