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
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 7c408068ece94d47c0f41e286a2ce0ae7efd23dd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972498"
---
# <a name="options-for-preventing-discounts-for-retail-products"></a><span data-ttu-id="7b2ed-103">Valkostir til að koma í veg afslætti á smásöluafurðir</span><span class="sxs-lookup"><span data-stu-id="7b2ed-103">Options for preventing discounts for retail products</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7b2ed-104">Það eru ýmsar ástæður fyrir því að smásalar gætu viljað koma í veg fyrir afslætti á sumum vörum, annað hvort frá kynningu eða á meðan sölu á sölustað stendur.</span><span class="sxs-lookup"><span data-stu-id="7b2ed-104">There are various reasons why retailers may want to prevent some products from being discounted, either from a promotion or during the sale at the POS.</span></span>

<span data-ttu-id="7b2ed-105">Eftirfarandi valmöguleikar, sem finna má á **Commerce** flipa útgefinna vara, gerir þér kleift að forða vörunni frá öllum afslætti eða handvirkum afslætti.</span><span class="sxs-lookup"><span data-stu-id="7b2ed-105">The following options, which can be found on the **Commerce** tab of released products, will allow the product to be configured to prevent all or manual discounts.</span></span> <span data-ttu-id="7b2ed-106">Stillingarnar geta líka verið tilgreindar á stigi flokka frá tegundastigveldi.</span><span class="sxs-lookup"><span data-stu-id="7b2ed-106">The settings can also be specified at the category level from the category hierarchy.</span></span>

- <span data-ttu-id="7b2ed-107">**Engir afslættir leyfðir** – Veldu þennan valkost til að tryggja að engin tegund afsláttar verði sett á vöruna.</span><span class="sxs-lookup"><span data-stu-id="7b2ed-107">**Prevent all discounts** – Select this option to prevent all types of discounts from being applied to this product.</span></span> <span data-ttu-id="7b2ed-108">Þetta á við um kynningartilboð eins og blandað tilboð, magn- eða þröskuldaafslætti, sem og handvirka línu- og færsluafslætti sem eru settir á vöruna á meðan á sölu stendur hjá notanda sölustaðar.</span><span class="sxs-lookup"><span data-stu-id="7b2ed-108">This includes promotions such as mix and match, quantity and threshold discounts, as well as manual line and transaction discounts that are applied during a sale by a POS user.</span></span>
- <span data-ttu-id="7b2ed-109">**Engir handvirkir afslættir leyfðir** – Veldu þennan valkost aðeins til að koma í veg fyrir að handvirkir línu- eða færsluafslættir séu settir á vöruna á meðan á sölu stendur hjá notanda sölustaðar.</span><span class="sxs-lookup"><span data-stu-id="7b2ed-109">**Prevent manual discounts** – Select this option to only prevent the manual line or transaction discounts that are applied during a sale by a POS user.</span></span> <span data-ttu-id="7b2ed-110">Vörur með þennan valkost valinn eru samt sem áður tækar til kynningartilboðs, eins og blandað tilboð, magn- og þröskuldatilboð.</span><span class="sxs-lookup"><span data-stu-id="7b2ed-110">Products with this option selected are still eligible for promotions, such as mix and match and quantity and threshold discounts.</span></span>

> [!NOTE]
> <span data-ttu-id="7b2ed-111">Þessar stillingar takmarka ekki aðgerðina að hnekkja verði, vegna þess að hún setur grunnverð og er ekki meðhöndluð sem afsláttur.</span><span class="sxs-lookup"><span data-stu-id="7b2ed-111">These settings do not restrict the price override operation, because that sets the base price and is not treated as a discount.</span></span>

<span data-ttu-id="7b2ed-112">[![Koma í veg fyrir afslætti reitur](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span><span class="sxs-lookup"><span data-stu-id="7b2ed-112">[![Prevent discounts field](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span></span>
