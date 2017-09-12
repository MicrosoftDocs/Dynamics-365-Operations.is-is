--- 
title: "Setja upp ráðstöfunarkóða"
description: "Þetta ferli leggur áherslu á uppsetningu ráðstöfunarkóða sem hægt er að nota í farsíma fyrir móttökuferli skilapöntunar."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c004543188656dfd53d7539717cd6e93d0b9f47a
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-dispositions-codes"></a><span data-ttu-id="8a6be-103">Setja upp ráðstöfunarkóða</span><span class="sxs-lookup"><span data-stu-id="8a6be-103">Set up dispositions codes</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8a6be-104">Þetta ferli leggur áherslu á uppsetningu ráðstöfunarkóða sem hægt er að nota í farsíma fyrir móttökuferli skilapöntunar.</span><span class="sxs-lookup"><span data-stu-id="8a6be-104">This procedure focuses on the setup of a disposition code that can be used on a mobile device for the return order receiving process.</span></span> <span data-ttu-id="8a6be-105">Ráðstöfunarkóðar eru safn reglna sem hægt er að nota þegar vörur eru mótteknar.</span><span class="sxs-lookup"><span data-stu-id="8a6be-105">Disposition codes are a collection of rules that can be used when items are received.</span></span> <span data-ttu-id="8a6be-106">Til dæmis þegar notandi vinnu notar fartæki til að taka á móti vörum sem var skemmt, verður notandi að skanna ráðstöfunarkóða fyrir skemmdar vörur.</span><span class="sxs-lookup"><span data-stu-id="8a6be-106">For example, when a work user uses a mobile device to receive items that were damaged, the user must scan a disposition code for damaged items.</span></span> <span data-ttu-id="8a6be-107">birgðastaða mótteknu varanna, vinnusniðmátið, og staðsetningarleiðbeininga er hægt að ákvarða úr skannaðs ráðstöfunarkóða.</span><span class="sxs-lookup"><span data-stu-id="8a6be-107">The inventory status of the goods received, the work template, and the location directive can be determined from the scanned disposition code.</span></span> <span data-ttu-id="8a6be-108">notkun ráðstöfunarkóða er valfrjáls fyrir móttökuferli innkaupapöntunar og ferlið við að skrá framleiðslupöntun sem lokinni.</span><span class="sxs-lookup"><span data-stu-id="8a6be-108">For the purchase order receiving process and the production order report as finished process, the use of a disposition code is optional.</span></span> <span data-ttu-id="8a6be-109">notkun ráðstöfunarkóða er skylda fyrir ferlið við móttöku sölupöntunar, ef vörur eru skráðar með fartæki.</span><span class="sxs-lookup"><span data-stu-id="8a6be-109">For the sales order return receiving process, if the items are registered using a mobile device, the use of disposition code is mandatory.</span></span>  <span data-ttu-id="8a6be-110">Þetta Leiðbeiningar var stofnuð með því að nota sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="8a6be-110">This guide was created using the demo data company USMF.</span></span> <span data-ttu-id="8a6be-111">Þetta ferli er ætluð fyrir stjórnanda í vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="8a6be-111">This procedure is intended for the warehouse manager.</span></span> 

1. <span data-ttu-id="8a6be-112">Fara í Vöruhúsakerfi > Uppsetning > Fartæki > Ráðstöfunarkóðar.</span><span class="sxs-lookup"><span data-stu-id="8a6be-112">Go to Warehouse management > Setup > Mobile device > Disposition codes.</span></span>
2. <span data-ttu-id="8a6be-113">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="8a6be-113">Click New.</span></span>
    * <span data-ttu-id="8a6be-114">Stofna nýjan ráðstöfunarkóða sem nota á fyrir skil viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="8a6be-114">Create a new disposition code to use for customer returns.</span></span>  
3. <span data-ttu-id="8a6be-115">Í reitnum Ráðstöfunarkóði skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="8a6be-115">In the Disposition code field, type a value.</span></span>
4. <span data-ttu-id="8a6be-116">Í reitnum birgðastaða, velja birgðastöðu þar sem er birgðalæsing.</span><span class="sxs-lookup"><span data-stu-id="8a6be-116">In the Inventory status field, select an inventory status where there is inventory blocking.</span></span>
    * <span data-ttu-id="8a6be-117">Ef verið er að nota USMF, veldu ‚Læsing'.</span><span class="sxs-lookup"><span data-stu-id="8a6be-117">If you're using USMF, select 'Blocking'.</span></span> <span data-ttu-id="8a6be-118">Hægt er að bæta birgðastöðu við ráðstöfunarkóða til að hnekkja sjálfgefna stöðu sem er í pöntunarlínum.</span><span class="sxs-lookup"><span data-stu-id="8a6be-118">You can add an inventory status to the disposition code to override the default status that’s on the order lines.</span></span>  
5. <span data-ttu-id="8a6be-119">Færa inn gildi í reitnum Vinnusniðmát.</span><span class="sxs-lookup"><span data-stu-id="8a6be-119">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="8a6be-120">Valfrjálst: Velja sniðmátskóða vinnu sem er tengd skilapöntun.</span><span class="sxs-lookup"><span data-stu-id="8a6be-120">Optional: Select a work template code that is associated with a return order.</span></span> <span data-ttu-id="8a6be-121">Ef ekkert gildi er gefið verður vinnusniðmátið leyst með því að nota staðlaða reglur sem skilgreind er í kerfinu þínu.</span><span class="sxs-lookup"><span data-stu-id="8a6be-121">If no value is provided, the work template will be resolved using the standard rules configured in your system.</span></span> <span data-ttu-id="8a6be-122">Val á vinnusniðmáti takmarkar þau ferli sem hægt er að nota með þessum ráðstöfunarkóða.</span><span class="sxs-lookup"><span data-stu-id="8a6be-122">Selecting a work template will limit the processes this disposition code can be used with.</span></span> <span data-ttu-id="8a6be-123">Til dæmis hafi ráðstöfunarkóða vinnusniðmát með vinnupöntun af gerðinni innkaupapöntun, er ekki hægt að nota það til að skrá vörur sem er skilað af viðskiptavinum.</span><span class="sxs-lookup"><span data-stu-id="8a6be-123">For example, if a disposition code has a work template with a work order of type purchase order, it can’t be used to register items that are returned by customers.</span></span>  
6. <span data-ttu-id="8a6be-124">Í reitnum Ráðstöfunarkóði skila skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="8a6be-124">In the Return disposition code field, type a value.</span></span>
    * <span data-ttu-id="8a6be-125">Ráðstöfunarkóði skila ákvarðar afgangur skilapöntunarferlis fyrir vörur sem eru skráðar.</span><span class="sxs-lookup"><span data-stu-id="8a6be-125">The return disposition code determines the remainder of the return order process for the items registered.</span></span> <span data-ttu-id="8a6be-126">Í þessu dæmi ætti viðskiptavinar að fá kreditnótu.</span><span class="sxs-lookup"><span data-stu-id="8a6be-126">In this example, the customer should receive a credit note.</span></span> <span data-ttu-id="8a6be-127">Bæta við ráðstöfunarkóða skila sem inniheldur lánsfé aðgerðar.</span><span class="sxs-lookup"><span data-stu-id="8a6be-127">Add a returns disposition code that contains an action Credit.</span></span>  


