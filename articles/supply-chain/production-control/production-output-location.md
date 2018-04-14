---
title: "Staðsetning framleiðsluúttaks"
description: "Þetta efnisatriði lýsir stigveldi sem notað er til að auðkenna staðsetningu framleiðsluúttaks."
author: johanhoffmann
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
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
ms.openlocfilehash: 1235fe1db6663018c019322a7850cb428e3935d4
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="production-output-location"></a><span data-ttu-id="00111-103">Staðsetning framleiðsluúttaks</span><span class="sxs-lookup"><span data-stu-id="00111-103">Production output location</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="00111-104">Þetta efnisatriði lýsir stigveldi sem notað er til að auðkenna staðsetningu framleiðsluúttaks.</span><span class="sxs-lookup"><span data-stu-id="00111-104">This topic describes the hierarchy that is used to identify the production output location.</span></span>

<span data-ttu-id="00111-105">Staðsetning frameiðsluúttaks er sú staðsetning þar sem fullunnin vara er fyrst geymd eftir að hún hefur verið framleidd.</span><span class="sxs-lookup"><span data-stu-id="00111-105">The production output location is the location where a finished good is first stored after it's produced.</span></span> <span data-ttu-id="00111-106">Yfirleitt, er þessi staðsetning nálægt framleiðsluferlinu sem framleiðir fullunna vöru.</span><span class="sxs-lookup"><span data-stu-id="00111-106">Usually, this location is close to the production process that produces the finished good.</span></span> <span data-ttu-id="00111-107">Staðsetning framleiðsluúttaks er notuð sem milligeymsla fyrir efni áður en það er fært á sendingarsvæði, geymslusvæði, staðsetningu framleiðsluinntaks fyrir framleiðsluferli forstreymis og o.s.frv.</span><span class="sxs-lookup"><span data-stu-id="00111-107">The production output location is used as intermediate storage for the material before it's moved on to the shipment area, a storage location, a production input location for a downstream production process, and so on.</span></span> 

<span data-ttu-id="00111-108">Sjálfgefin staðsetning framleiðsluúttaks er stillt þegar fullunnar vörur eru skráðar í framleiðslupöntun eða runupöntun.</span><span class="sxs-lookup"><span data-stu-id="00111-108">A default production output location is set when finished goods are reported on a production order or batch order.</span></span> <span data-ttu-id="00111-109">Eftirfarandi stigveldi er notað til að auðkenna þessa úttaksstaðsetningu:</span><span class="sxs-lookup"><span data-stu-id="00111-109">The following hierarchy is used to identify this output location:</span></span>

1. <span data-ttu-id="00111-110">Notaðu þá úttaksstaðsetningu sem er skilgreind í haus framleiðslupöntunar eða runupöntunar.</span><span class="sxs-lookup"><span data-stu-id="00111-110">Use the output location that is defined on the production order or batch order header.</span></span>
2. <span data-ttu-id="00111-111">Ef engin staðsetning fyrirfinnst hér, skal nota úttaksstaðsetninguna sem skilgreind er í því tilfangi sem notað var af síðustu aðgerð sem er skilgreind í framleiðsluleið.</span><span class="sxs-lookup"><span data-stu-id="00111-111">If no location is found there, use the output location that is defined on the resource that is used by the last operation that is defined in the production route.</span></span>
3. <span data-ttu-id="00111-112">Ef engin staðsetning fyrirfinnst hér, skal nota úttaksstaðsetninguna sem skilgreind er í þeim tilfangahópi sem notaður var af tilfanginu fyrir síðustu aðgerð sem er skilgreind í framleiðsluleið.</span><span class="sxs-lookup"><span data-stu-id="00111-112">If no location is found there, use the output location that is defined on the resource group that is used by the resource for the last operation that is defined in the production route.</span></span>
4. <span data-ttu-id="00111-113">Ef engin staðsetning finnst þar, skal nota þá úttaksstaðsetningu sem er skilgreind í því vöruhúsi sem er skilgreint fyrir framleiðslupöntunina.</span><span class="sxs-lookup"><span data-stu-id="00111-113">If no location is found there, use the output location that is defined on the warehouse that is defined for the production order.</span></span>

<span data-ttu-id="00111-114">Sjálfgefin staðsetning framleiðsluúttaks er aðeins skilgreind fyrir afurðir sem eru uppsettar með ítarlegum vöruhúsaferlum.</span><span class="sxs-lookup"><span data-stu-id="00111-114">A default production output location is set only for products that are set up by using advanced warehouse processes.</span></span> <span data-ttu-id="00111-115">Þegar þessi gerð vöru er skráð sem fullunnin er vöruhúsavinna af gerðinni **Frágangur á fullbúnum vörum** eða **Frágangur aukaafurða eða hliðarafurða** stofnuð.</span><span class="sxs-lookup"><span data-stu-id="00111-115">When this type of item is reported as finished, warehouse work of the **Finished goods put away** or **Co-product and by-product put away** type is created.</span></span> <span data-ttu-id="00111-116">Þessi gerð vinnu notast við staðsetningu framleiðsluúttaks sem tiltektarstaðsetningu.</span><span class="sxs-lookup"><span data-stu-id="00111-116">This type of work uses the production output location as the pick location.</span></span> <span data-ttu-id="00111-117">Frágangsstaðsetningin ákvarðast af staðsetningarleiðbeiningum.</span><span class="sxs-lookup"><span data-stu-id="00111-117">The put-away location is determined by the location directives.</span></span>

