---
title: Staðsetning framleiðsluúttaks
description: Þetta efnisatriði lýsir stigveldi sem notað er til að auðkenna staðsetningu framleiðsluúttaks.
author: johanhoffmann
manager: tfehr
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e4002bf7dddb196edf306268ecc16e1bfa5d6d1e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211308"
---
# <a name="production-output-location"></a><span data-ttu-id="4d9fe-103">Staðsetning framleiðsluúttaks</span><span class="sxs-lookup"><span data-stu-id="4d9fe-103">Production output location</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d9fe-104">Þetta efnisatriði lýsir stigveldi sem notað er til að auðkenna staðsetningu framleiðsluúttaks.</span><span class="sxs-lookup"><span data-stu-id="4d9fe-104">This topic describes the hierarchy that is used to identify the production output location.</span></span>

<span data-ttu-id="4d9fe-105">Staðsetning frameiðsluúttaks er sú staðsetning þar sem fullunnin vara er fyrst geymd eftir að hún hefur verið framleidd.</span><span class="sxs-lookup"><span data-stu-id="4d9fe-105">The production output location is the location where a finished good is first stored after it's produced.</span></span> <span data-ttu-id="4d9fe-106">Yfirleitt, er þessi staðsetning nálægt framleiðsluferlinu sem framleiðir fullunna vöru.</span><span class="sxs-lookup"><span data-stu-id="4d9fe-106">Usually, this location is close to the production process that produces the finished good.</span></span> <span data-ttu-id="4d9fe-107">Staðsetning framleiðsluúttaks er notuð sem milligeymsla fyrir efni áður en það er fært á sendingarsvæði, geymslusvæði, staðsetningu framleiðsluinntaks fyrir framleiðsluferli forstreymis og o.s.frv.</span><span class="sxs-lookup"><span data-stu-id="4d9fe-107">The production output location is used as intermediate storage for the material before it's moved on to the shipment area, a storage location, a production input location for a downstream production process, and so on.</span></span> 

<span data-ttu-id="4d9fe-108">Sjálfgefin staðsetning framleiðsluúttaks er stillt þegar fullunnar vörur eru skráðar í framleiðslupöntun eða runupöntun.</span><span class="sxs-lookup"><span data-stu-id="4d9fe-108">A default production output location is set when finished goods are reported on a production order or batch order.</span></span> <span data-ttu-id="4d9fe-109">Eftirfarandi stigveldi er notað til að auðkenna þessa úttaksstaðsetningu:</span><span class="sxs-lookup"><span data-stu-id="4d9fe-109">The following hierarchy is used to identify this output location:</span></span>

1. <span data-ttu-id="4d9fe-110">Notaðu þá úttaksstaðsetningu sem er skilgreind í haus framleiðslupöntunar eða runupöntunar.</span><span class="sxs-lookup"><span data-stu-id="4d9fe-110">Use the output location that is defined on the production order or batch order header.</span></span>
2. <span data-ttu-id="4d9fe-111">Ef engin staðsetning fyrirfinnst hér, skal nota úttaksstaðsetninguna sem skilgreind er í því tilfangi sem notað var af síðustu aðgerð sem er skilgreind í framleiðsluleið.</span><span class="sxs-lookup"><span data-stu-id="4d9fe-111">If no location is found there, use the output location that is defined on the resource that is used by the last operation that is defined in the production route.</span></span>
3. <span data-ttu-id="4d9fe-112">Ef engin staðsetning fyrirfinnst hér, skal nota úttaksstaðsetninguna sem skilgreind er í þeim tilfangahópi sem notaður var af tilfanginu fyrir síðustu aðgerð sem er skilgreind í framleiðsluleið.</span><span class="sxs-lookup"><span data-stu-id="4d9fe-112">If no location is found there, use the output location that is defined on the resource group that is used by the resource for the last operation that is defined in the production route.</span></span>
4. <span data-ttu-id="4d9fe-113">Ef engin staðsetning finnst þar, skal nota þá úttaksstaðsetningu sem er skilgreind í því vöruhúsi sem er skilgreint fyrir framleiðslupöntunina.</span><span class="sxs-lookup"><span data-stu-id="4d9fe-113">If no location is found there, use the output location that is defined on the warehouse that is defined for the production order.</span></span>

<span data-ttu-id="4d9fe-114">Sjálfgefin staðsetning framleiðsluúttaks er aðeins skilgreind fyrir afurðir sem eru uppsettar með ítarlegum vöruhúsaferlum.</span><span class="sxs-lookup"><span data-stu-id="4d9fe-114">A default production output location is set only for products that are set up by using advanced warehouse processes.</span></span> <span data-ttu-id="4d9fe-115">Þegar þessi gerð vöru er skráð sem fullunnin er vöruhúsavinna af gerðinni **Frágangur á fullbúnum vörum** eða **Frágangur aukaafurða eða hliðarafurða** stofnuð.</span><span class="sxs-lookup"><span data-stu-id="4d9fe-115">When this type of item is reported as finished, warehouse work of the **Finished goods put away** or **Co-product and by-product put away** type is created.</span></span> <span data-ttu-id="4d9fe-116">Þessi gerð vinnu notast við staðsetningu framleiðsluúttaks sem tiltektarstaðsetningu.</span><span class="sxs-lookup"><span data-stu-id="4d9fe-116">This type of work uses the production output location as the pick location.</span></span> <span data-ttu-id="4d9fe-117">Frágangsstaðsetningin ákvarðast af staðsetningarleiðbeiningum.</span><span class="sxs-lookup"><span data-stu-id="4d9fe-117">The put-away location is determined by the location directives.</span></span>
