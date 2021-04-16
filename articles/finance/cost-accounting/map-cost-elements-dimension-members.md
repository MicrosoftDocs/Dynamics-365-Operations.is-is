---
title: Varpa víddarstökum kostnaðareiningar á almennt safn víddarstaka
description: Vörpun mismunandi víddarstök kostnaðareiningar á almenn sett víddarstök kostnaðareiningar, þannig sameinar þú gögn í almennt snið í greiningartilgangi.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMDimensionMember, CAMDimensionMapping
audience: Application User
ms.reviewer: roschlom
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3ce207b74c9515c72f4fce7680ee9eea50edd0f8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810151"
---
# <a name="map-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a><span data-ttu-id="4e194-103">Varpa víddarstökum kostnaðareiningar á almennt safn víddarstaka</span><span class="sxs-lookup"><span data-stu-id="4e194-103">Map cost element dimension members to a common set of dimension members</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e194-104">Vörpun mismunandi víddarstök kostnaðareiningar á almenn sett víddarstök kostnaðareiningar, þannig sameinar þú gögn í almennt snið í greiningartilgangi.</span><span class="sxs-lookup"><span data-stu-id="4e194-104">By mapping different cost element dimension members to a common set of cost element dimension members, you merge data into a common format for analysis purposes.</span></span>

<span data-ttu-id="4e194-105">Ef þú ert alþjóðlegt fyrirtæki og uppfylli lögboðnar kröfur um bókhald, gætir þú notað margar bókhaldslykla.</span><span class="sxs-lookup"><span data-stu-id="4e194-105">If you're a global company and comply with statutory accounting requirements, you might use multiple charts of accounts.</span></span> <span data-ttu-id="4e194-106">Þegar þú flytur inn víddarstök kostnaðareiningar úr mismunandi bókhaldslyklum, geturðu endað með blöndu lykla.</span><span class="sxs-lookup"><span data-stu-id="4e194-106">When you import cost element dimension members from different charts of accounts, you can end up with a mix of accounts.</span></span> <span data-ttu-id="4e194-107">Hins vegar gætu þessir reikningar í raun hafa sömu náttúru, og þú gætir vilja greina og úthluta kostnaði fyrir þá með því að nota sameiginlegt snið.</span><span class="sxs-lookup"><span data-stu-id="4e194-107">However, these accounts might actually have the same nature, and you might want to analyze and allocate costs for them by using a common format.</span></span>

## <a name="map-cost-element-dimension-members-to-a-common-format"></a><span data-ttu-id="4e194-108">Varpa víddarstök kostnaðareiningar á almennt snið</span><span class="sxs-lookup"><span data-stu-id="4e194-108">Map cost element dimension members to a common format</span></span>
<span data-ttu-id="4e194-109">Eftirfarandi dæmi sýnir hvernig þú, sem fjármálastjóri, getur stofnað nýja vídd kostnaðareiningar í kostnaðarbókhaldi sem varpar víddarstök kostnaðareiningar úr Bandarísk skipulag bókhaldslykils og Franska skipulag bókhaldslykils í almenn sett víddarstaka kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="4e194-109">The following example shows how you, as a cost controller, can create a new cost element dimension in Cost accounting that maps cost element dimension members from the US chart of accounts structure and the French chart of accounts structure to a common set of cost element dimension members.</span></span> <span data-ttu-id="4e194-110">Síðan er hægt að nota almennt safn víddarstök kostnaðareiningar til að greina kostnaðargögn úr tveimur lögaðila í fjárhag kostnaðarbókhalds.</span><span class="sxs-lookup"><span data-stu-id="4e194-110">You can then use the common set of cost element dimension members to analyze cost data from the two legal entities in a cost accounting ledger.</span></span>

| <span data-ttu-id="4e194-111">Uppspretta: Bandaríkin bókhaldslykil</span><span class="sxs-lookup"><span data-stu-id="4e194-111">Source: US chart of accounts</span></span>                                          | <span data-ttu-id="4e194-112">Uppspretta: franska bókhaldslykil</span><span class="sxs-lookup"><span data-stu-id="4e194-112">Source: French chart of accounts</span></span>                                          | <span data-ttu-id="4e194-113">Ný almennt sett víddarstaka kostnaðareiningar</span><span class="sxs-lookup"><span data-stu-id="4e194-113">New common set of cost element dimension members</span></span>                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="4e194-114">Innflutt víddarstök kostnaðareiningar úr bandaríska bókhaldslykli</span><span class="sxs-lookup"><span data-stu-id="4e194-114">Imported cost element dimension members from the US chart of accounts</span></span> | <span data-ttu-id="4e194-115">Innflutt víddarstök kostnaðareiningar úr franska bókhaldslykli</span><span class="sxs-lookup"><span data-stu-id="4e194-115">Imported cost element dimension members from the French chart of accounts</span></span> | <span data-ttu-id="4e194-116">Varpa bandaríska og franska víddarstök kostnaðareiningar á almennt sett</span><span class="sxs-lookup"><span data-stu-id="4e194-116">Mapping of US and French cost element dimension members to a common set</span></span> |
| <span data-ttu-id="4e194-117">5001: Sala</span><span class="sxs-lookup"><span data-stu-id="4e194-117">5001: Sales</span></span>                                                           | <span data-ttu-id="4e194-118">5001: Sala og auglýsingar</span><span class="sxs-lookup"><span data-stu-id="4e194-118">5001: Sales and advertising</span></span>                                               | <span data-ttu-id="4e194-119">5000: Sala og auglýsingar</span><span class="sxs-lookup"><span data-stu-id="4e194-119">5000: Sales and advertising</span></span>                                             |
| <span data-ttu-id="4e194-120">5030: Auglýsingar</span><span class="sxs-lookup"><span data-stu-id="4e194-120">5030: Advertising</span></span>                                                     | <span data-ttu-id="4e194-121">6390: birgðakaup\*</span><span class="sxs-lookup"><span data-stu-id="4e194-121">6390: Stock purchase\*</span></span>                                                    | <span data-ttu-id="4e194-122">7000: Ræstikostnaður</span><span class="sxs-lookup"><span data-stu-id="4e194-122">7000: Cleaning expenses</span></span>                                                 |
| <span data-ttu-id="4e194-123">7001: Ræstikostnaður</span><span class="sxs-lookup"><span data-stu-id="4e194-123">7001: Cleaning expenses</span></span>                                               | <span data-ttu-id="4e194-124">7001: Ferðakostnaður</span><span class="sxs-lookup"><span data-stu-id="4e194-124">7001: Travel expense</span></span>                                                      | <span data-ttu-id="4e194-125">7001: Ferðakostnaður</span><span class="sxs-lookup"><span data-stu-id="4e194-125">7001: Travel expenses</span></span>                                                   |

<span data-ttu-id="4e194-126">\*Franska víddarstak kostnaðareiningar fyrir birgðakaup er ekki varpað.</span><span class="sxs-lookup"><span data-stu-id="4e194-126">\*The Stock purchase French cost element dimension member isn't mapped.</span></span>

## <a name="currency-conversion"></a><span data-ttu-id="4e194-127">Umreikningur gjaldmiðils</span><span class="sxs-lookup"><span data-stu-id="4e194-127">Currency conversion</span></span>
<span data-ttu-id="4e194-128">Mismunandi bókhaldslykil sem þú notar gætu setja upp til að nota aðra gjaldmiðla.</span><span class="sxs-lookup"><span data-stu-id="4e194-128">The various charts of accounts that you use might be set up to use different currencies.</span></span> <span data-ttu-id="4e194-129">Í þessu tilfelli gætið þess að tilgreina umreikningur fyrirtækisgjaldmiðils þannig að kostnaðargögn er unnin með réttum gjaldmiðli, eins og skilgreint er í fjárhag kostnaðarbókhalds þar sem víddarstök kostnaðareiningar eru notaðar.</span><span class="sxs-lookup"><span data-stu-id="4e194-129">In this case, be sure to specify a currency conversion, so that cost data is processed by using the correct currency, as defined in the cost accounting ledger where the cost element dimension members are used.</span></span> <span data-ttu-id="4e194-130">Í fyrrgreint dæmi, ef Bandarískum dollurum (USD) eru notaðar í fjárhag kostnaðarbókhalds verður að stofna gjaldmiðilsumreikning frá USD að evrur (EUR) til að vinna færslur fyrir varpaðar víddarstök kostnaðareiningar .</span><span class="sxs-lookup"><span data-stu-id="4e194-130">In the preceding example, if US dollars (USD) are used in the cost accounting ledger, you must create a currency conversion from USD to euros (EUR) to process transactions for the mapped cost element dimension members.</span></span>

## <a name="update-mappings-at-any-time"></a><span data-ttu-id="4e194-131">Uppfæra varpanir hvenær sem er.</span><span class="sxs-lookup"><span data-stu-id="4e194-131">Update mappings at any time</span></span>
<span data-ttu-id="4e194-132">Hægt er að uppfæra skilgreiningar vörpunar fyrir vídd kostnaðareiningar hvenær sem er.</span><span class="sxs-lookup"><span data-stu-id="4e194-132">You can update the mapping definitions for a cost element dimension at any time.</span></span> <span data-ttu-id="4e194-133">Þar sem varpanir eru ekki virkjaðar samkvæmt dagsetningum, eru breytingar notaðar í næsta sinn sem þú vinnur úr kostnaðarfærslur eða keyra kostnaðarútreikninga.</span><span class="sxs-lookup"><span data-stu-id="4e194-133">Because mappings aren't date-effective, changes are applied the next time that you process cost transactions or run cost calculations.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]