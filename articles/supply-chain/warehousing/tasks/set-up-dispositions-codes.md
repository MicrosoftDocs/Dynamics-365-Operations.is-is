---
title: Setja upp ráðstöfunarkóða
description: Þetta ferli leggur áherslu á uppsetningu ráðstöfunarkóða sem hægt er að nota í farsíma fyrir móttökuferli skilapöntunar.
author: ShylaThompson
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSDispositionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16458f709788e538d036cc4d3b3239f4ffa3c42e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830930"
---
# <a name="set-up-dispositions-codes"></a><span data-ttu-id="9ba6a-103">Setja upp ráðstöfunarkóða</span><span class="sxs-lookup"><span data-stu-id="9ba6a-103">Set up dispositions codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9ba6a-104">Þetta ferli leggur áherslu á uppsetningu ráðstöfunarkóða sem hægt er að nota í farsíma fyrir móttökuferli skilapöntunar.</span><span class="sxs-lookup"><span data-stu-id="9ba6a-104">This procedure focuses on the setup of a disposition code that can be used on a mobile device for the return order receiving process.</span></span> <span data-ttu-id="9ba6a-105">Ráðstöfunarkóðar eru safn reglna sem hægt er að nota þegar vörur eru mótteknar.</span><span class="sxs-lookup"><span data-stu-id="9ba6a-105">Disposition codes are a collection of rules that can be used when items are received.</span></span> <span data-ttu-id="9ba6a-106">Til dæmis þegar notandi vinnu notar fartæki til að taka á móti vörum sem var skemmt, verður notandi að skanna ráðstöfunarkóða fyrir skemmdar vörur.</span><span class="sxs-lookup"><span data-stu-id="9ba6a-106">For example, when a work user uses a mobile device to receive items that were damaged, the user must scan a disposition code for damaged items.</span></span> <span data-ttu-id="9ba6a-107">birgðastaða mótteknu varanna, vinnusniðmátið, og staðsetningarleiðbeininga er hægt að ákvarða úr skannaðs ráðstöfunarkóða.</span><span class="sxs-lookup"><span data-stu-id="9ba6a-107">The inventory status of the goods received, the work template, and the location directive can be determined from the scanned disposition code.</span></span> <span data-ttu-id="9ba6a-108">notkun ráðstöfunarkóða er valfrjáls fyrir móttökuferli innkaupapöntunar og ferlið við að skrá framleiðslupöntun sem lokinni.</span><span class="sxs-lookup"><span data-stu-id="9ba6a-108">For the purchase order receiving process and the production order report as finished process, the use of a disposition code is optional.</span></span> <span data-ttu-id="9ba6a-109">notkun ráðstöfunarkóða er skylda fyrir ferlið við móttöku sölupöntunar, ef vörur eru skráðar með fartæki.</span><span class="sxs-lookup"><span data-stu-id="9ba6a-109">For the sales order return receiving process, if the items are registered using a mobile device, the use of disposition code is mandatory.</span></span>  <span data-ttu-id="9ba6a-110">Þetta Leiðbeiningar var stofnuð með því að nota sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="9ba6a-110">This guide was created using the demo data company USMF.</span></span> <span data-ttu-id="9ba6a-111">Þetta ferli er ætluð fyrir stjórnanda í vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="9ba6a-111">This procedure is intended for the warehouse manager.</span></span> 

1. <span data-ttu-id="9ba6a-112">Fara í Vöruhúsakerfi > Uppsetning > Fartæki > Ráðstöfunarkóðar.</span><span class="sxs-lookup"><span data-stu-id="9ba6a-112">Go to Warehouse management > Setup > Mobile device > Disposition codes.</span></span>
2. <span data-ttu-id="9ba6a-113">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="9ba6a-113">Click New.</span></span>
    * <span data-ttu-id="9ba6a-114">Stofna nýjan ráðstöfunarkóða sem nota á fyrir skil viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="9ba6a-114">Create a new disposition code to use for customer returns.</span></span>  
3. <span data-ttu-id="9ba6a-115">Í reitnum Ráðstöfunarkóði skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9ba6a-115">In the Disposition code field, type a value.</span></span>
4. <span data-ttu-id="9ba6a-116">Í reitnum birgðastaða, velja birgðastöðu þar sem er birgðalæsing.</span><span class="sxs-lookup"><span data-stu-id="9ba6a-116">In the Inventory status field, select an inventory status where there is inventory blocking.</span></span>
    * <span data-ttu-id="9ba6a-117">Ef verið er að nota USMF, veldu ‚Læsing'.</span><span class="sxs-lookup"><span data-stu-id="9ba6a-117">If you're using USMF, select 'Blocking'.</span></span> <span data-ttu-id="9ba6a-118">Hægt er að bæta birgðastöðu við ráðstöfunarkóða til að hnekkja sjálfgefna stöðu sem er í pöntunarlínum.</span><span class="sxs-lookup"><span data-stu-id="9ba6a-118">You can add an inventory status to the disposition code to override the default status that's on the order lines.</span></span>  
5. <span data-ttu-id="9ba6a-119">Færa inn gildi í reitnum Vinnusniðmát.</span><span class="sxs-lookup"><span data-stu-id="9ba6a-119">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="9ba6a-120">Valfrjálst: Velja sniðmátskóða vinnu sem er tengd skilapöntun.</span><span class="sxs-lookup"><span data-stu-id="9ba6a-120">Optional: Select a work template code that is associated with a return order.</span></span> <span data-ttu-id="9ba6a-121">Ef ekkert gildi er gefið verður vinnusniðmátið leyst með því að nota staðlaða reglur sem skilgreind er í kerfinu þínu.</span><span class="sxs-lookup"><span data-stu-id="9ba6a-121">If no value is provided, the work template will be resolved using the standard rules configured in your system.</span></span> <span data-ttu-id="9ba6a-122">Val á vinnusniðmáti takmarkar þau ferli sem hægt er að nota með þessum ráðstöfunarkóða.</span><span class="sxs-lookup"><span data-stu-id="9ba6a-122">Selecting a work template will limit the processes this disposition code can be used with.</span></span> <span data-ttu-id="9ba6a-123">Til dæmis hafi ráðstöfunarkóða vinnusniðmát með vinnupöntun af gerðinni innkaupapöntun, er ekki hægt að nota það til að skrá vörur sem er skilað af viðskiptavinum.</span><span class="sxs-lookup"><span data-stu-id="9ba6a-123">For example, if a disposition code has a work template with a work order of type purchase order, it can't be used to register items that are returned by customers.</span></span>  
6. <span data-ttu-id="9ba6a-124">Í reitnum Ráðstöfunarkóði skila skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9ba6a-124">In the Return disposition code field, type a value.</span></span>
    * <span data-ttu-id="9ba6a-125">Ráðstöfunarkóði skila ákvarðar afgangur skilapöntunarferlis fyrir vörur sem eru skráðar.</span><span class="sxs-lookup"><span data-stu-id="9ba6a-125">The return disposition code determines the remainder of the return order process for the items registered.</span></span> <span data-ttu-id="9ba6a-126">Í þessu dæmi ætti viðskiptavinar að fá kreditnótu.</span><span class="sxs-lookup"><span data-stu-id="9ba6a-126">In this example, the customer should receive a credit note.</span></span> <span data-ttu-id="9ba6a-127">Bæta við ráðstöfunarkóða skila sem inniheldur lánsfé aðgerðar.</span><span class="sxs-lookup"><span data-stu-id="9ba6a-127">Add a returns disposition code that contains an action Credit.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]