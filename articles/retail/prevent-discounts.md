---
title: Valkostir til að koma í veg afslætti á smásöluafurðir
description: Það eru ýmsar ástæður fyrir því að smásalar gætu viljað koma í veg fyrir afslætti á sumum vörum, annað hvort frá kynningu eða á meðan sölu á sölustað stendur.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c9d3e7af95dffddfddc34059d93a2a5a350d08e5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "346066"
---
# <a name="options-for-preventing-discounts-for-retail-products"></a><span data-ttu-id="ebc9c-103">Valkostir til að koma í veg afslætti á smásöluafurðir</span><span class="sxs-lookup"><span data-stu-id="ebc9c-103">Options for preventing discounts for retail products</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ebc9c-104">Það eru ýmsar ástæður fyrir því að smásalar gætu viljað koma í veg fyrir afslætti á sumum vörum, annað hvort frá kynningu eða á meðan sölu á sölustað stendur.</span><span class="sxs-lookup"><span data-stu-id="ebc9c-104">There are various reasons why retailers may want to prevent some products from being discounted, either from a promotion or during the sale at the POS.</span></span>

<span data-ttu-id="ebc9c-105">Eftirfarandi valmöguleikar, sem finna má á **Smásala** flipa útgefinna vara, gerir þér kleift að forða vörunni frá öllum afslætti eða handvirkum afslætti.</span><span class="sxs-lookup"><span data-stu-id="ebc9c-105">The following options, which can be found on the **Retail** tab of released products, will allow the product to be configured to prevent all or manual discounts.</span></span> <span data-ttu-id="ebc9c-106">Stillingarnar geta líka verið tilgreindar á stigi flokka frá stigveldi smásöluflokka.</span><span class="sxs-lookup"><span data-stu-id="ebc9c-106">The settings can also be specified at the category level from the retail category hierarchy.</span></span>

- <span data-ttu-id="ebc9c-107">**Engir afslættir leyfðir** – Veldu þennan valkost til að tryggja að engin tegund afsláttar verði sett á vöruna.</span><span class="sxs-lookup"><span data-stu-id="ebc9c-107">**Prevent all discounts** – Select this option to prevent all types of discounts from being applied to this product.</span></span> <span data-ttu-id="ebc9c-108">Þetta á við um kynningartilboð eins og blandað tilboð, magn- eða þröskuldaafslætti, sem og handvirka línu- og færsluafslætti sem eru settir á vöruna á meðan á sölu stendur hjá notanda sölustaðar.</span><span class="sxs-lookup"><span data-stu-id="ebc9c-108">This includes promotions such as mix and match, quantity and threshold discounts, as well as manual line and transaction discounts that are applied during a sale by a POS user.</span></span>
- <span data-ttu-id="ebc9c-109">**Engir handvirkir afslættir leyfðir** – Veldu þennan valkost aðeins til að koma í veg fyrir að handvirkir línu- eða færsluafslættir séu settir á vöruna á meðan á sölu stendur hjá notanda sölustaðar.</span><span class="sxs-lookup"><span data-stu-id="ebc9c-109">**Prevent manual discounts** – Select this option to only prevent the manual line or transaction discounts that are applied during a sale by a POS user.</span></span> <span data-ttu-id="ebc9c-110">Vörur með þennan valkost valinn eru samt sem áður tækar til kynningartilboðs, eins og blandað tilboð, magn- og þröskuldatilboð.</span><span class="sxs-lookup"><span data-stu-id="ebc9c-110">Products with this option selected are still eligible for promotions, such as mix and match and quantity and threshold discounts.</span></span>

> [!NOTE]
> <span data-ttu-id="ebc9c-111">Þessar stillingar takmarka ekki aðgerðina að hnekkja verði, vegna þess að hún setur grunnverð og er ekki meðhöndluð sem afsláttur.</span><span class="sxs-lookup"><span data-stu-id="ebc9c-111">These settings do not restrict the price override operation, because that sets the base price and is not treated as a discount.</span></span>

<span data-ttu-id="ebc9c-112">[![koma í veg fyrir afslætti reitur](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span><span class="sxs-lookup"><span data-stu-id="ebc9c-112">[![prevent discounts field](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span></span>
