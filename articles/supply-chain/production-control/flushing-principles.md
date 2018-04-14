---
title: Losunarreglur
description: "Þetta efnisatriði lýsir losunarreglunum fjórum sem notaðar eru fyrir notkun á hráefni."
author: johanhoffmann
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgShopSupervisorReleaseOrders
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 818d7d21605ada63a29a41d3bf20ed9cbf21a178
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="controlling-raw-material-consumption-by-using-flushing-principles"></a><span data-ttu-id="0ff74-103">Stjórna notkun hráefnis með því að nota birgðareglur</span><span class="sxs-lookup"><span data-stu-id="0ff74-103">Controlling raw material consumption by using flushing principles</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="0ff74-104">Losunarreglurnar endurspegla mismunandi stefnur varðandi notkun hráefnis sem er notað í framleiðsluferlum.</span><span class="sxs-lookup"><span data-stu-id="0ff74-104">The flushing principles reflect different consumption strategies for raw materials that are used in production processes.</span></span> <span data-ttu-id="0ff74-105">Notkun er það ferli sem dregur efni úr lagerbirgðum og stillir gildi notaðs efni á **Verk í vinnslu** (WIP) fyrir framleiðslupantanir og runupantanir.</span><span class="sxs-lookup"><span data-stu-id="0ff74-105">Consumption is the process that deducts material from the on-hand inventory and sets the value of the consumed materials to **Work in progress** (WIP) for production orders and batch orders.</span></span> <span data-ttu-id="0ff74-106">Hráefni er vanalega notað frá staðsetningu sem er skilgreind fyrir ferlið sem notar efnið.</span><span class="sxs-lookup"><span data-stu-id="0ff74-106">Raw materials are usually consumed from a location that is configured for the process that consumes the material.</span></span> <span data-ttu-id="0ff74-107">Þessi staðsetning kallast inntaksstaðsetning framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="0ff74-107">This location is known as the production input location.</span></span>

<span data-ttu-id="0ff74-108">Áður en efni er notað er það flutt á inntaksstaðsetningu.</span><span class="sxs-lookup"><span data-stu-id="0ff74-108">Before material consumption, the materials are moved to the input location.</span></span> <span data-ttu-id="0ff74-109">Eftirfarandi mynd sýnir ferlið.</span><span class="sxs-lookup"><span data-stu-id="0ff74-109">The following illustration shows the process.</span></span>

<span data-ttu-id="0ff74-110">[![scenario4a](./media/scenario4a.png)](./media/scenario4a.png)</span><span class="sxs-lookup"><span data-stu-id="0ff74-110">[![scenario4a](./media/scenario4a.png)](./media/scenario4a.png)</span></span>

1. <span data-ttu-id="0ff74-111">Hráefnisvöruhús</span><span class="sxs-lookup"><span data-stu-id="0ff74-111">Material warehouse</span></span>
2. <span data-ttu-id="0ff74-112">Tiltekt hráefnis</span><span class="sxs-lookup"><span data-stu-id="0ff74-112">Raw material picking</span></span>
3. <span data-ttu-id="0ff74-113">Staðsetning framleiðsluinntaks</span><span class="sxs-lookup"><span data-stu-id="0ff74-113">Production input location</span></span>
4. <span data-ttu-id="0ff74-114">Hráefnisnotkun</span><span class="sxs-lookup"><span data-stu-id="0ff74-114">Raw material consumption</span></span>
5. <span data-ttu-id="0ff74-115">Framleiðsluferli</span><span class="sxs-lookup"><span data-stu-id="0ff74-115">Production process</span></span>

<span data-ttu-id="0ff74-116">Efnisnotkun stýrist af eftirfarandi fjórum losunarreglum:</span><span class="sxs-lookup"><span data-stu-id="0ff74-116">Material consumption is controlled by the following four flushing principles:</span></span>

- <span data-ttu-id="0ff74-117">Handvirkt</span><span class="sxs-lookup"><span data-stu-id="0ff74-117">Manual</span></span>
- <span data-ttu-id="0ff74-118">Byrja</span><span class="sxs-lookup"><span data-stu-id="0ff74-118">Start</span></span>
- <span data-ttu-id="0ff74-119">Ljúk.  </span><span class="sxs-lookup"><span data-stu-id="0ff74-119">Finish</span></span>
- <span data-ttu-id="0ff74-120">Tiltækt í staðsetningu</span><span class="sxs-lookup"><span data-stu-id="0ff74-120">Available at location</span></span>

<span data-ttu-id="0ff74-121">Losunarreglurnar eru skilgreindar í stigveldi sjálfgilda.</span><span class="sxs-lookup"><span data-stu-id="0ff74-121">The flushing principles are configured in a hierarchy of default values.</span></span> <span data-ttu-id="0ff74-122">Stigveldi byrjar á útgefinni afurð, þar sem losunarreglan hefur gildið **Ræsa**.</span><span class="sxs-lookup"><span data-stu-id="0ff74-122">The hierarchy starts at the released product, where the flushing principle has the value **Start**.</span></span> <span data-ttu-id="0ff74-123">Hægt er að hnekkja losunarreglunni frá afurðinni á uppskriftinni (BOM) eða formúlulínunni.</span><span class="sxs-lookup"><span data-stu-id="0ff74-123">On the bill of materials (BOM) or formula line, the flushing principle from the product can be overridden.</span></span> <span data-ttu-id="0ff74-124">Sjálfgefna losunarreglan á uppskriftarlínum framleiðslu eða formúlulínum runupantana er tekin frá vörunni eða hnekktu gildi á uppskriftinni eða formúlunum.</span><span class="sxs-lookup"><span data-stu-id="0ff74-124">The default flushing principle on the production BOM lines or batch order formula lines is taken from the product or the overridden value on the BOM or formulas.</span></span>

## <a name="description-of-the-flushing-principles"></a><span data-ttu-id="0ff74-125">Lýsing á losunarreglum</span><span class="sxs-lookup"><span data-stu-id="0ff74-125">Description of the flushing principles</span></span>

### <a name="manual"></a><span data-ttu-id="0ff74-126">Handvirkt</span><span class="sxs-lookup"><span data-stu-id="0ff74-126">Manual</span></span>
<span data-ttu-id="0ff74-127">Handvirka losunarregla gefur til kynna að skráning á efnisnotkun sé handvirk aðgerð.</span><span class="sxs-lookup"><span data-stu-id="0ff74-127">The Manual flushing principle indicates that the registration of material consumption is a manual operation.</span></span> <span data-ttu-id="0ff74-128">Þessi regla á við ef þú vilt til dæmis geta rakið tíma, og fjöldi notaðra rununúmera eða raðnúmera þarf að vera tekinn með í rakninguna.</span><span class="sxs-lookup"><span data-stu-id="0ff74-128">This principle is relevant if, for example, you want to be able to track time, and the quantity of consumed batch numbers or serial numbers must be accounted for, for tracking purposes.</span></span> <span data-ttu-id="0ff74-129">Handvirk notkun er skráð í tiltektarlista framleiðslubókar.</span><span class="sxs-lookup"><span data-stu-id="0ff74-129">Manual consumption is registered in a production picking list journal.</span></span> <span data-ttu-id="0ff74-130">Hægt er að nota flæði sem haldið er á fyrir atriði sem eru virkjuð fyrir ítarleg vöruhúsaferli.</span><span class="sxs-lookup"><span data-stu-id="0ff74-130">For items that are enabled for advanced warehouse processes, a hand-held flow can be applied.</span></span>

### <a name="start"></a><span data-ttu-id="0ff74-131">Byrja</span><span class="sxs-lookup"><span data-stu-id="0ff74-131">Start</span></span>
<span data-ttu-id="0ff74-132">Losunarreglan Ræsa gefur til kynna að efni verði sjálfkrafa notað þegar framleiðslupöntun er ræst.</span><span class="sxs-lookup"><span data-stu-id="0ff74-132">The Start flushing principle indicates that material will be automatically consumed when the production order is started.</span></span> <span data-ttu-id="0ff74-133">Magn efnis sem er notað er í hlutfalli við magnið sem er ræst.</span><span class="sxs-lookup"><span data-stu-id="0ff74-133">The amount of material that is consumed is proportional to the quantity that is started.</span></span> <span data-ttu-id="0ff74-134">Þegar losunarreglan Ræsa er notuð ásamt framleiðslukerfinu er einnig hægt að nota hana til að losa efni þegar aðgerð eða ferlisvinnsla er ræst.</span><span class="sxs-lookup"><span data-stu-id="0ff74-134">When the Start flushing principle is used together with the manufacturing execution system, it can also be used to flush materials when an operation or a process job is started.</span></span> <span data-ttu-id="0ff74-135">Þessi regla á til dæmis við ef frávik í notkuninni eru lítil, efnið er lágvirðisefni, það eru engar rakningarkröfur eða ef aðgerðir hafa stuttan keyrslutíma.</span><span class="sxs-lookup"><span data-stu-id="0ff74-135">This principle is relevant if, for example, the variance in the consumption is low, the materials are low-value materials, there are no tracking requirements, or there is a short run time on operations.</span></span> 

### <a name="finish"></a><span data-ttu-id="0ff74-136">Ljúk.  </span><span class="sxs-lookup"><span data-stu-id="0ff74-136">Finish</span></span>
<span data-ttu-id="0ff74-137">Losunarreglan Ljúka gefur til kynna að efni verði sjálfkrafa notað þegar tilkynnt er að framleiðslupöntun sé lokið, eða þegar skráð er að aðgerð sem ætlað er að nota efnið sé lokið.</span><span class="sxs-lookup"><span data-stu-id="0ff74-137">The Finish flushing principle indicates that material will be automatically consumed when the production order is reported as finished, or when an operation that is set up to consume the materials is registered as completed.</span></span> <span data-ttu-id="0ff74-138">Magn efnis sem er notað er í hlutfalli við magnið sem er skráð sem lokið.</span><span class="sxs-lookup"><span data-stu-id="0ff74-138">The amount of material that is consumed is proportional to the quantity that is reported as finished.</span></span> <span data-ttu-id="0ff74-139">Þegar losunarreglan Ljúka er notuð ásamt framleiðslukerfinu er einnig hægt að nota hana til að losa efni þegar aðgerð eða ferlisvinnslu er lokið.</span><span class="sxs-lookup"><span data-stu-id="0ff74-139">When the Finish flushing principle is used together with the manufacturing execution system, it can also be used to flush materials when an operation or a process job is completed.</span></span> <span data-ttu-id="0ff74-140">Þessi regla á við við sömu aðstæður og reglan Ræsa.</span><span class="sxs-lookup"><span data-stu-id="0ff74-140">This principle is relevant in the same situations as the Start principle.</span></span> <span data-ttu-id="0ff74-141">Aftur á móti er reglan Ljúka fyrir aðgerðir sem hafa lengri keyrslutíma, þar sem ekki ætti að stilla efni á VÍV áður en aðgerðinni er lokið.</span><span class="sxs-lookup"><span data-stu-id="0ff74-141">However, the Finish principle is for operations that have a longer run time, where materials should not be set to WIP before the operation is completed.</span></span> 

### <a name="available-at-location"></a><span data-ttu-id="0ff74-142">Tiltækt í staðsetningu</span><span class="sxs-lookup"><span data-stu-id="0ff74-142">Available at location</span></span>
<span data-ttu-id="0ff74-143">Losunarreglan Tiltækt í staðsetningu gefur til kynna að efnið verði sjálfkrafa notað þegar það er skráð sem tekið til fyrir framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="0ff74-143">The Available at location flushing principle indicates that the material will be automatically consumed when it's registered as picked for production.</span></span> <span data-ttu-id="0ff74-144">Efnið er skráð sem tekið til frá staðsetningu þegar vinnu við tiltekt á hráefni er lokið, eða þegar efni er tiltækt á staðsetningu framleiðsluinntaks og efnislínan er losuð til vöruhússins.</span><span class="sxs-lookup"><span data-stu-id="0ff74-144">The material is registered as picked from location when work for the raw material picking is completed, or when material is available on the production input location and the material line is released to the warehouse.</span></span> <span data-ttu-id="0ff74-145">Tiltektarlistinn sem verður til í ferlinu er birtur í runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="0ff74-145">The picking list that is generated during the process is posted in a batch job.</span></span> <span data-ttu-id="0ff74-146">Þessi regla á til dæmis við ef ert með marga tiltektarverkþætti á móti einni framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="0ff74-146">This principle is relevant if, for example, you have many picking activities against one production order.</span></span> <span data-ttu-id="0ff74-147">Í þessu tilfelli þarf ekki að uppfæra tiltektarlistann handvirkt, og þú færð núverandi yfirlit yfir VÍV-stöðuna.</span><span class="sxs-lookup"><span data-stu-id="0ff74-147">In this case, you don't have to update the picking list manually, and you can get a current view of the WIP balance.</span></span>

