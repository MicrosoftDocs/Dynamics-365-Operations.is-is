---
title: Losa framleiðslupantanir
description: Útgefin framleiðslupöntun er pöntun sem hefur verið samþykkt til framleiðslu. Hugtakið útgefið er notað til að lýsa stöðu í líftíma framleiðslupöntunar þar sem framleiðslupöntunin er tiltæk fyrir framkvæmd í framleiðsluvinnusal og fyrir ferli vöruhúss.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc6d53fc87bac2e23c0d1e67954be02749042004
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430611"
---
# <a name="release-production-orders"></a><span data-ttu-id="6b4f1-104">Losa framleiðslupantanir</span><span class="sxs-lookup"><span data-stu-id="6b4f1-104">Release production orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6b4f1-105">Útgefin framleiðslupöntun er pöntun sem hefur verið samþykkt til framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="6b4f1-105">A released production order is an order that has been authorized for production.</span></span> <span data-ttu-id="6b4f1-106">Hugtakið útgefið er notað til að lýsa stöðu í líftíma framleiðslupöntunar þar sem framleiðslupöntunin er tiltæk fyrir framkvæmd í framleiðsluvinnusal og fyrir ferli vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="6b4f1-106">The term Released is used to describe a state in the production order life cycle, where the production order is available for execution on the production shop floor and for warehouse processes.</span></span> 

<a name="characteristics-of-the-released-state"></a><span data-ttu-id="6b4f1-107">Einkennandi þættir Losunarstöðu</span><span class="sxs-lookup"><span data-stu-id="6b4f1-107">Characteristics of the Released state</span></span>
-------------------------------------

<span data-ttu-id="6b4f1-108">**Losað** staða er ein staða í lífsferli framleiðslupöntunar</span><span class="sxs-lookup"><span data-stu-id="6b4f1-108">The **Released** state is one state in the production order life cycle.</span></span> <span data-ttu-id="6b4f1-109">Framleiðslupantanir sem eru í **Losaðar** stöðu eru tiltækar fyrir framkvæmd á framleiðsluvinnusal og fyrir ferli vöruhúsa.</span><span class="sxs-lookup"><span data-stu-id="6b4f1-109">Production orders that are in the **Released** state are available for execution on the production shop floor and for warehouse processes.</span></span> <span data-ttu-id="6b4f1-110">**Losað** staða hefur eftirfarandi eiginleika:</span><span class="sxs-lookup"><span data-stu-id="6b4f1-110">The **Released** state has the following characteristics:</span></span>

-   <span data-ttu-id="6b4f1-111">Hægt er að breyta framleiðslupöntun í **Losaða** stöðu annað hvort úr framleiðslupöntun eða með því að nota runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="6b4f1-111">A production order can be changed to the **Released** state either from the production order or by using a batch process.</span></span> <span data-ttu-id="6b4f1-112">Framleiðslupöntunina má einnig uppfæra sjálfkrafa úr áætlaðar framleiðslupantanir sem eru festaar með því að nota í **tímamörk festingar** á í **aðaláætlun** síðu.</span><span class="sxs-lookup"><span data-stu-id="6b4f1-112">The production order can also be updated automatically from planned production orders that are firmed by using the **Firming time fence** field on the **Master plan** page.</span></span>
-   <span data-ttu-id="6b4f1-113">**Losað** staða er merki fyrir virknitákn vinnusals til að byrja að framkvæma framleiðsluverk í vinnusal.</span><span class="sxs-lookup"><span data-stu-id="6b4f1-113">The **Released** state is the signal for the shop floor operators (operators) to start executing the production jobs on the shop floor.</span></span>
-   <span data-ttu-id="6b4f1-114">framleiðsluskjöl eins og leiðarspjöld, leiðarvinnslur og verkspjöld veita upplýsingar um framleiðsluverk og má gefa út.</span><span class="sxs-lookup"><span data-stu-id="6b4f1-114">Production papers, such as route cards, route jobs, and jobs cards provide information about production jobs and can be issued.</span></span>
-   <span data-ttu-id="6b4f1-115">Fyrir Efni sem eru efnislega teknar frá, er  vöruhúsavinnu mynduð til að taka til efni fyrir framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="6b4f1-115">For materials that are physically reserved, warehouse work is generated to pick materials for the production order.</span></span>

## <a name="releasing-jobs-to-the-shop-floor"></a><span data-ttu-id="6b4f1-116">Losa vinnslu í vinnusal</span><span class="sxs-lookup"><span data-stu-id="6b4f1-116">Releasing jobs to the shop floor</span></span>
<span data-ttu-id="6b4f1-117">Eftir að framleiðslupöntun er losuð,eru framleiðsluverk sem eru tengd pöntuninni sýnileg og tilbúin fyrir skráningu.</span><span class="sxs-lookup"><span data-stu-id="6b4f1-117">After a production order is released, production jobs that are related to the order are visible and ready for registration.</span></span> <span data-ttu-id="6b4f1-118">Virknitákn geta framkvæmt vinnsluskráningar, eins og Hefja, Stöðva og Lokið, í annað hvort síðunni **Afgreiðslustöð verkspjalda** eða síðunni **Verkspjaldstæki**.</span><span class="sxs-lookup"><span data-stu-id="6b4f1-118">The operators can make job registrations, such as Start, Stop, and Completion, on either the **Job card terminal** page or the **Job card device** page.</span></span> <span data-ttu-id="6b4f1-119">Skráður tími og magn eru sjálfvirkt fluttar úr skráningasíðum í framleiðslubækur til að fylgjast með notuðum tíma og magni.</span><span class="sxs-lookup"><span data-stu-id="6b4f1-119">The registered time and quantity are automatically transferred from the registration pages to production journals to keep track of the consumed time and quantity.</span></span>

## <a name="route-cards"></a><span data-ttu-id="6b4f1-120">Leiðarspjöld</span><span class="sxs-lookup"><span data-stu-id="6b4f1-120">Route cards</span></span>
<span data-ttu-id="6b4f1-121">leiðarspjaldi veitir yfirlit yfir upplýsinga sem koma úr leið og uppsetningu aðgerða, og úr aðgerð og vinnsluröðunaraðferðum.</span><span class="sxs-lookup"><span data-stu-id="6b4f1-121">A route card provides an overview of information that comes from route and operation setups, and from operation and job scheduling methods.</span></span>

## <a name="route-jobs"></a><span data-ttu-id="6b4f1-122">Leiðarvinnslur</span><span class="sxs-lookup"><span data-stu-id="6b4f1-122">Route jobs</span></span>
<span data-ttu-id="6b4f1-123">Leiðarvinnsla er með lista yfir sérhverja vinnslu aðgerðar í smáatriðum, þar á meðal uppsetningu, ferli, röð, og flutningstíma.</span><span class="sxs-lookup"><span data-stu-id="6b4f1-123">A route job lists each job of an operation in detail, and includes setup, process, queue, and transportation times.</span></span> <span data-ttu-id="6b4f1-124">Til dæmis, Aðgerð eins og málun gæti til dæmis útheimt einstakar vinnslur, eins og uppsetningu tíma, keyrslutíma (fyrir málningarferlið) og biðtíma (fyrir þornun).</span><span class="sxs-lookup"><span data-stu-id="6b4f1-124">For example, an operation such as painting might require individual jobs, such as setup time, run time for the painting process, and queue time for drying.</span></span>

## <a name="job-cards"></a><span data-ttu-id="6b4f1-125">Vinnsluspjöld</span><span class="sxs-lookup"><span data-stu-id="6b4f1-125">Job cards</span></span>
<span data-ttu-id="6b4f1-126">vinnsluspjaldi er listi yfir einstök vinnslunúmer fyrir tiltekna aðgerð.</span><span class="sxs-lookup"><span data-stu-id="6b4f1-126">A job card lists the individual job numbers of a particular operation.</span></span> <span data-ttu-id="6b4f1-127">Eitt verk birtist í hverri síðu</span><span class="sxs-lookup"><span data-stu-id="6b4f1-127">One job appears on each page.</span></span> <span data-ttu-id="6b4f1-128">Vinnslurnar sem eru hafðar á vinnsluspjaldi, og áætlaður tími, koma úr upplýsingum um uppsetningu leiða og aðgerða.</span><span class="sxs-lookup"><span data-stu-id="6b4f1-128">The jobs that are included on a job card, and their estimated times, come from the route and operation setup information.</span></span> <span data-ttu-id="6b4f1-129">Frá vinnsluspjaldi er hægt að opna **framleiðslubókarlínur**, **vinnsluspjald** síðu.</span><span class="sxs-lookup"><span data-stu-id="6b4f1-129">From a job card, you can open the **Production journal lines**, **job card** page.</span></span> <span data-ttu-id="6b4f1-130">Einstaklingarnir sem keyra rekstrartilföng geta gefið svörun um framleiðsluferlið.</span><span class="sxs-lookup"><span data-stu-id="6b4f1-130">People who run operations resources can provide feedback about the production process.</span></span> <span data-ttu-id="6b4f1-131">Fyrirliggjandi eru svæði þar sem hægt er að færa inn talnagögn um notkun og upplýsingar eins og gallað magn.</span><span class="sxs-lookup"><span data-stu-id="6b4f1-131">There are fields where you can enter consumption statistics and information such as the error quantity.</span></span>

## <a name="warehouse-work-for-raw-material-picking"></a><span data-ttu-id="6b4f1-132">Vinna vöruhúss fyrir tiltekt hráefnis.</span><span class="sxs-lookup"><span data-stu-id="6b4f1-132">Warehouse work for raw material picking</span></span>
<span data-ttu-id="6b4f1-133">Vinnu fyrir tiltekt hráefnis er stofnuð á meðan á losun stendur.</span><span class="sxs-lookup"><span data-stu-id="6b4f1-133">Work for raw material picking is generated during release.</span></span> <span data-ttu-id="6b4f1-134">Vinna er mynduð aðeins fyrir magn efnis sem var efnislega tekin frá fyrir framleiðslupöntunina áður en pöntunin var losuð.</span><span class="sxs-lookup"><span data-stu-id="6b4f1-134">Work is generated only for the quantity of materials that was physically reserved for the production order before the order was released.</span></span> <span data-ttu-id="6b4f1-135">Eftirfarandi uppsetning er nauðsynleg til að mynda vöruhúsavinnu fyrir tiltekt hráefnis:</span><span class="sxs-lookup"><span data-stu-id="6b4f1-135">The following setup is required to generate warehouse work for raw material picking:</span></span>

-   <span data-ttu-id="6b4f1-136">Staðsetningarleiðbeiningar fyrir tiltekt hráefnis sem ákvarðar í hvaða staðsetningu innan vöruhúss á að taka til efni í</span><span class="sxs-lookup"><span data-stu-id="6b4f1-136">A location directive for raw materials picking that determines which warehouse location to pick the materials in</span></span>
-   <span data-ttu-id="6b4f1-137">Bylgjusniðmát furir hráefni, þar sem reglurnar fyrir framkvæmd vinnu vöruhúss eru skilgreindar.</span><span class="sxs-lookup"><span data-stu-id="6b4f1-137">A wave template for raw materials, where policies for the execution of warehouse work are configured</span></span>
-   <span data-ttu-id="6b4f1-138">Staðsetning framleiðsluinntaks sem ákvarðar hvar efni eru sett</span><span class="sxs-lookup"><span data-stu-id="6b4f1-138">A production input location that determines where materials are put</span></span>




