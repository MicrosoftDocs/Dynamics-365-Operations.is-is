---
title: Afturkalla pöntunaraðgerð á sölustað
description: Í þessu efnisatriði eru útskýrðir eiginleikar í boði fyrir bættar síður afturköllunar á pöntun á sölustað.
author: hhainesms
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 41944fb7819b5527f6bc023a60acd9450d9e43c2
ms.sourcegitcommit: 25909c6ad3616e4f75a2fe006057dda18d7cc856
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/09/2020
ms.locfileid: "3974839"
---
# <a name="recall-order-operation-in-pos"></a><span data-ttu-id="aebc3-103">Afturkalla pöntunaraðgerð á sölustað</span><span class="sxs-lookup"><span data-stu-id="aebc3-103">Recall order operation in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="aebc3-104">Afturköllun pöntunaraðgerðar á sölustað Commerce veitir uppfærða pöntunarleit og síunareiginleika og upplýsingar um tiltekna pöntun.</span><span class="sxs-lookup"><span data-stu-id="aebc3-104">The Recall order operation in the Commerce point of sale (POS) provides updated order search and filtering features and order-specific information.</span></span> <span data-ttu-id="aebc3-105">Þessi eiginleiki er tiltækur í Commerce-útgáfum 10.0.15 og nýrri.</span><span class="sxs-lookup"><span data-stu-id="aebc3-105">This feature is available in Commerce versions 10.0.15 and later.</span></span>

<span data-ttu-id="aebc3-106">Til að virkja þessa virkni þarf að kveikja á eiginleikanum **Bætt afturköllunaraðgerð pöntunar á sölustað** á vinnusvæðinu **Eiginleikastjórnun** í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="aebc3-106">To enable this functionality, turn the **Improved Recall order operation in POS** feature on in **Feature management** workspace in Commerce headquarters.</span></span> <span data-ttu-id="aebc3-107">Þegar búið er að virkja eiginleikann skal íhuga að uppfæra [skjáútlit](pos-screen-layouts.md) á sölustað til að nýta einhverjar af þessum breytingum.</span><span class="sxs-lookup"><span data-stu-id="aebc3-107">After you enable the feature, consider updating your [screen layouts](pos-screen-layouts.md) in POS to take advantage of some of the changed  capabilities.</span></span>

<span data-ttu-id="aebc3-108">Skilgreining á aðgerðarhnappnum **Endurkalla pöntun** gerir fyrirtækjum kleift að setja upp aðgerðina með fyrirframskilgreindri birtingu.</span><span class="sxs-lookup"><span data-stu-id="aebc3-108">The configuration of the **Recall order** operation button allows organizations to deploy the operation with a pre-defined display.</span></span>

![Grunnstilling hnappahnits](media/recallorderbuttongrid.png)

<span data-ttu-id="aebc3-110">Birtingarkostir eru eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="aebc3-110">The display options are as follows.</span></span>
- <span data-ttu-id="aebc3-111">**Ekkert** – Þessi valkostur setur upp aðgerðina án sérstakrar birtingar.</span><span class="sxs-lookup"><span data-stu-id="aebc3-111">**None** – This option deploys the operation with no specific display.</span></span> <span data-ttu-id="aebc3-112">Þegar notandi opnar aðgerðina með þessari skilgreiningu verða þeir beðnir um að leita og finna pantanir eða velja úr fyrirframskilgreindum pöntunarsíum.</span><span class="sxs-lookup"><span data-stu-id="aebc3-112">When a user opens the operation with this configuration, they will be prompted to search and find orders or choose from a pre-defined order filter.</span></span>
- <span data-ttu-id="aebc3-113">**Pantanir sem á að uppfylla** – Þegar notandi ræsir aðgerðina, keyrir fyrirspurn sjálfkrafa til að leita að og birta lista yfir pantanir sem á að uppfylla í versluninni.</span><span class="sxs-lookup"><span data-stu-id="aebc3-113">**Orders to fulfill** – When a user launches the operation, a query will run automatically to search and display a list of orders that are to be fulfilled by the store.</span></span> <span data-ttu-id="aebc3-114">Þessar pantanir eru skilgreindar fyrir sótt í verslun eða sendingu úr verslun og línur þessara pantana hafa enn ekki verið teknar til eða pakkaðar.</span><span class="sxs-lookup"><span data-stu-id="aebc3-114">These orders are configured for in-store pickup or store shipment and the lines of these orders have not yet been picked or packed.</span></span>
- <span data-ttu-id="aebc3-115">**Pantanir sem á að sækja** – Þegar notandi ræsir aðgerðina, keyrir fyrirspurn sjálfkrafa til að leita að og birta lista yfir pantanir sem eru skilgreindar að verði sóttar í verslun í núverandi verslun notandans.</span><span class="sxs-lookup"><span data-stu-id="aebc3-115">**Orders to pick up** – When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for in-store pickup at the user's current store.</span></span>
- <span data-ttu-id="aebc3-116">**Pantanir sem á að senda** – Þegar notandi ræsir aðgerðina, keyrir fyrirspurn sjálfkrafa til að leita að og birta lista yfir pantanir sem eru skilgreindar að verði sendar úr núverandi verslun notandans.</span><span class="sxs-lookup"><span data-stu-id="aebc3-116">**Orders to ship** - When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for shipment from the user's current store.</span></span>

<span data-ttu-id="aebc3-117">Þegar aðgerðin **Endurkalla pöntun** er ræst á sölustað, ef birtingin er stillt á **Ekkert**, getur notandi leitað að og sótt pantanir á einn af eftirfarandi hátt.</span><span class="sxs-lookup"><span data-stu-id="aebc3-117">When launching the **Recall order** operation from POS, if the display is configured to **None**, a user will be able to search and retrieve orders in one of the following ways.</span></span>
- <span data-ttu-id="aebc3-118">Skanna strikamerki pöntunar.</span><span class="sxs-lookup"><span data-stu-id="aebc3-118">Scan order barcodes.</span></span> <span data-ttu-id="aebc3-119">Þetta mun leita í reitum pöntunarnúmers, rásartilvísunar og innhreyfingarkennis að samsvörun.</span><span class="sxs-lookup"><span data-stu-id="aebc3-119">This will search order number, channel reference, and receipt ID fields for matches.</span></span>
- <span data-ttu-id="aebc3-120">Veljið táknið **Leita að pöntunum** eða **Leita og sía** í AppBar til að nota síunaraðferðina til að hafa upp á pöntunum sem uppfylla síuskilyrðið.</span><span class="sxs-lookup"><span data-stu-id="aebc3-120">Select **Search orders** or **Search and filter** icon on the AppBar to use the filtering mechanism to locate orders that meet the filter criteria.</span></span>
- <span data-ttu-id="aebc3-121">Velja skal úr forskilgreindri síu úr fellivalmyndinni **Sýna pantanir** (pantanir til að uppfylla, pantanir til að sækja eða pantanir til að senda).</span><span class="sxs-lookup"><span data-stu-id="aebc3-121">Choose from a pre-defined filter from the **Show Orders** drop-down menu (orders to fulfill, orders to pick up, or orders to ship).</span></span>

![RecallOrderMainMenu](media/recallordermain.png)

<span data-ttu-id="aebc3-123">Eftir að leitarskilyrði er notað, birtir forritið lista yfir samsvarandi sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="aebc3-123">After search criteria are applied, the application will display a list of matching sales orders.</span></span>

![RecallOrderDetail](media/orderrecalldetail.png)

<span data-ttu-id="aebc3-125">Notandi getur valið pöntun á listanum til að skoða frekari upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="aebc3-125">A user can select an order on the list to view additional details.</span></span> <span data-ttu-id="aebc3-126">Upplýsingaspjaldið hægra megin á skjánum sýnir atriði valdrar pöntunar, þ.m.t. upplýsingar pöntunarlínu, upplýsingar um afhendingu og upplýsingar um uppfyllingu.</span><span class="sxs-lookup"><span data-stu-id="aebc3-126">The information panel on the right side of the screen displays specifics on the selected order, including order line details, delivery details, and fulfillment details.</span></span>

<span data-ttu-id="aebc3-127">Í AppBar getur notandi valið aðgerð.</span><span class="sxs-lookup"><span data-stu-id="aebc3-127">From the AppBar, a user can select an operation.</span></span> <span data-ttu-id="aebc3-128">Það fer eftir stöðu pöntunarinnar hvort ákveðnar aðgerðir eru virkar eða ekki.</span><span class="sxs-lookup"><span data-stu-id="aebc3-128">Depending on the status of the order, certain operations may not be enabled.</span></span>

- <span data-ttu-id="aebc3-129">**Skila** – Keyrir skil fyrir einn eða fleiri reikninga sem tengjast valinni pöntun viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="aebc3-129">**Return** – Executes a return for one or more invoices related to the selected customer order.</span></span>

- <span data-ttu-id="aebc3-130">**Hætta við** – Gefa út fulla afturköllun á valinni sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="aebc3-130">**Cancel** – Issue a full cancellation of the selected sales order.</span></span>

- <span data-ttu-id="aebc3-131">**Uppfylla** – Flytur notandann yfir á uppfyllingarsíðu pöntunar sem verður fyrirframsíuð fyrir valda pöntun.</span><span class="sxs-lookup"><span data-stu-id="aebc3-131">**Fulfill** – Transfers the user to the order fulfillment page, which will be pre-filtered for the selected order.</span></span> <span data-ttu-id="aebc3-132">Aðeins pöntunarlínur sem verslun notanda má uppfylla fyrir valda pöntun eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="aebc3-132">Only order lines that are open for fulfillment by the user's store for the selected order will be displayed.</span></span>

- <span data-ttu-id="aebc3-133">**Breyta** – Leyfir notendum að gera breytingar á valinni pöntun viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="aebc3-133">**Edit** – Allows users to make changes to the selected customer order.</span></span>

- <span data-ttu-id="aebc3-134">**Taka til** – Ræsir tiltektarflæðið, sem gerir notandanum kleift að velja afurðirnar sem á að taka til og stofnar sölufærslu tiltektarinnar.</span><span class="sxs-lookup"><span data-stu-id="aebc3-134">**Pick up** – Launches the pickup flow, which allows the user to choose the products to be picked up and creates the pickup sales transaction.</span></span>
