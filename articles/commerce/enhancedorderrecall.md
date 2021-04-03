---
title: Afturkalla pöntunaraðgerð á sölustað
description: Í þessu efnisatriði eru útskýrðir eiginleikar í boði fyrir bættar síður afturköllunar á pöntun á sölustað.
author: hhainesms
manager: annbe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 174821fce4baf81e4298da4b066f855bfec98ca5
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585131"
---
# <a name="recall-order-operation-in-pos"></a><span data-ttu-id="77728-103">Afturkalla pöntunaraðgerð á sölustað</span><span class="sxs-lookup"><span data-stu-id="77728-103">Recall order operation in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="77728-104">Aðgerðin **Afturköllun pöntunar** á sölustað Commerce veitir uppfærða pöntunarleit og síunareiginleika og upplýsingar um tiltekna pöntun.</span><span class="sxs-lookup"><span data-stu-id="77728-104">The **Recall order** operation in the Commerce point of sale (POS) provides updated order search and filtering features and order-specific information.</span></span> <span data-ttu-id="77728-105">Þessi eiginleiki er tiltækur í Commerce-útgáfum 10.0.15 og nýrri.</span><span class="sxs-lookup"><span data-stu-id="77728-105">This feature is available in Commerce versions 10.0.15 and later.</span></span>

<span data-ttu-id="77728-106">Til að virkja þessa virkni þarf að kveikja á eiginleikanum **Bætt afturköllunaraðgerð pöntunar á sölustað** á vinnusvæðinu **Eiginleikastjórnun** í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="77728-106">To enable this functionality, turn the **Improved Recall order operation in POS** feature on in **Feature management** workspace in Commerce headquarters.</span></span> <span data-ttu-id="77728-107">Þegar búið er að virkja eiginleikann skal íhuga að uppfæra [skjáútlit](pos-screen-layouts.md) á sölustað til að nýta einhverjar af þessum breytingum.</span><span class="sxs-lookup"><span data-stu-id="77728-107">After you enable the feature, consider updating your [screen layouts](pos-screen-layouts.md) in POS to take advantage of some of the changed  capabilities.</span></span>

<span data-ttu-id="77728-108">Skilgreining á aðgerðarhnappnum **Endurkalla pöntun** gerir fyrirtækjum kleift að setja upp aðgerðina með fyrirframskilgreindri birtingu.</span><span class="sxs-lookup"><span data-stu-id="77728-108">The configuration of the **Recall order** operation button allows organizations to deploy the operation with a pre-defined display.</span></span>

![Grunnstilling hnappahnits](media/recallorderbuttongrid.png)

<span data-ttu-id="77728-110">Birtingarkostir eru eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="77728-110">The display options are as follows.</span></span>
- <span data-ttu-id="77728-111">**Ekkert** – Þessi valkostur setur upp aðgerðina án sérstakrar birtingar.</span><span class="sxs-lookup"><span data-stu-id="77728-111">**None** – This option deploys the operation with no specific display.</span></span> <span data-ttu-id="77728-112">Þegar notandi opnar aðgerðina með þessari skilgreiningu verða þeir beðnir um að leita og finna pantanir eða velja úr fyrirframskilgreindum pöntunarsíum.</span><span class="sxs-lookup"><span data-stu-id="77728-112">When a user opens the operation with this configuration, they will be prompted to search and find orders or choose from a pre-defined order filter.</span></span>
- <span data-ttu-id="77728-113">**Pantanir sem á að uppfylla** – Þegar notandi ræsir aðgerðina, keyrir fyrirspurn sjálfkrafa til að leita að og birta lista yfir pantanir sem á að uppfylla í verslun notandans.</span><span class="sxs-lookup"><span data-stu-id="77728-113">**Orders to fulfill** – When a user launches the operation, a query will run automatically to search and display a list of orders that are to be fulfilled by the user's current store.</span></span> <span data-ttu-id="77728-114">Þessar pantanir eru skilgreindar fyrir sótt í verslun eða sendingu úr verslun og línur þessara pantana hafa enn ekki verið teknar til eða pakkaðar.</span><span class="sxs-lookup"><span data-stu-id="77728-114">These orders are configured for in-store pickup or store shipment and the lines of these orders have not yet been picked or packed.</span></span>
- <span data-ttu-id="77728-115">**Pantanir sem á að sækja** – Þegar notandi ræsir aðgerðina, keyrir fyrirspurn sjálfkrafa til að leita að og birta lista yfir pantanir sem eru skilgreindar að verði sóttar í verslun í núverandi verslun notandans.</span><span class="sxs-lookup"><span data-stu-id="77728-115">**Orders to pick up** – When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for in-store pickup at the user's current store.</span></span>
- <span data-ttu-id="77728-116">**Pantanir sem á að senda** – Þegar notandi ræsir aðgerðina, keyrir fyrirspurn sjálfkrafa til að leita að og birta lista yfir pantanir sem eru skilgreindar að verði sendar úr núverandi verslun notandans.</span><span class="sxs-lookup"><span data-stu-id="77728-116">**Orders to ship** - When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for shipment from the user's current store.</span></span>

<span data-ttu-id="77728-117">Þegar aðgerðin **Endurkalla pöntun** er ræst á sölustað, ef birtingin er stillt á **Ekkert**, getur notandi leitað að og sótt pantanir á einn af eftirfarandi hátt.</span><span class="sxs-lookup"><span data-stu-id="77728-117">When launching the **Recall order** operation from POS, if the display is configured to **None**, a user will be able to search and retrieve orders in one of the following ways.</span></span>
- <span data-ttu-id="77728-118">Skanna strikamerki pöntunar.</span><span class="sxs-lookup"><span data-stu-id="77728-118">Scan order barcodes.</span></span> <span data-ttu-id="77728-119">Þetta mun leita í reitum pöntunarnúmers, rásartilvísunar og innhreyfingarkennis að samsvörun.</span><span class="sxs-lookup"><span data-stu-id="77728-119">This will search order number, channel reference, and receipt ID fields for matches.</span></span>
- <span data-ttu-id="77728-120">Veljið táknið **Leita að pöntunum** eða **Leita og sía** í AppBar til að nota síunaraðferðina til að hafa upp á pöntunum sem uppfylla síuskilyrðið.</span><span class="sxs-lookup"><span data-stu-id="77728-120">Select **Search orders** or **Search and filter** icon on the AppBar to use the filtering mechanism to locate orders that meet the filter criteria.</span></span>
- <span data-ttu-id="77728-121">Velja skal úr forskilgreindri síu úr fellivalmyndinni **Sýna pantanir** (pantanir til að uppfylla, pantanir til að sækja eða pantanir til að senda).</span><span class="sxs-lookup"><span data-stu-id="77728-121">Choose from a pre-defined filter from the **Show Orders** drop-down menu (orders to fulfill, orders to pick up, or orders to ship).</span></span>

![RecallOrderMainMenu](media/recallordermain.png)

<span data-ttu-id="77728-123">Eftir að leitarskilyrði er notað, birtir forritið lista yfir samsvarandi sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="77728-123">After search criteria are applied, the application will display a list of matching sales orders.</span></span> <span data-ttu-id="77728-124">Mikilvægt er að hafa í huga að þegar leitar-/síuvalkostir eru notaðir þurfa sóttar pantanir ekki að vera pantanir sem tengdar eru við núverandi verslun notanda.</span><span class="sxs-lookup"><span data-stu-id="77728-124">It's important to note that when using the search/filter options, the orders retrieved do not have to be orders linked to the user's current store.</span></span> <span data-ttu-id="77728-125">Þetta leitarferli mun sækja og sýna allar pantanir viðskiptavina sem passa við leitarskilyrðið jafnvel þótt pöntunin hafi verið stofnuð eða stillt á að vera uppfyllt af annarri verslun/rás eða staðsetningu vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="77728-125">This search process will retrieve and display any customer order that matches the search criteria, even if the order was created or set to be fulfilled by another store/channel or warehouse location.</span></span>

![RecallOrderDetail](media/orderrecalldetail.png)

<span data-ttu-id="77728-127">Notandi getur valið pöntun á listanum til að skoða frekari upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="77728-127">A user can select an order on the list to view additional details.</span></span> <span data-ttu-id="77728-128">Upplýsingaspjaldið hægra megin á skjánum sýnir atriði valdrar pöntunar, þ.m.t. upplýsingar pöntunarlínu, upplýsingar um afhendingu og upplýsingar um uppfyllingu.</span><span class="sxs-lookup"><span data-stu-id="77728-128">The information panel on the right side of the screen displays specifics on the selected order, including order line details, delivery details, and fulfillment details.</span></span>

<span data-ttu-id="77728-129">Í AppBar getur notandi valið aðgerð.</span><span class="sxs-lookup"><span data-stu-id="77728-129">From the AppBar, a user can select an operation.</span></span> <span data-ttu-id="77728-130">Það fer eftir stöðu pöntunarinnar hvort ákveðnar aðgerðir eru virkar eða ekki.</span><span class="sxs-lookup"><span data-stu-id="77728-130">Depending on the status of the order, certain operations may not be enabled.</span></span>

- <span data-ttu-id="77728-131">**Skil** – Hefjið ferlið við að stofna skil fyrir einhverja reikningsfærða afurð í valdri pöntun viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="77728-131">**Return** – Initiates the process of creating a return for any of the invoiced products on the selected customer order.</span></span>

- <span data-ttu-id="77728-132">**Hætta við** – Gefa út fulla afturköllun á valinni sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="77728-132">**Cancel** – Issue a full cancellation of the selected sales order.</span></span> <span data-ttu-id="77728-133">Þessi valkostur verður ekki í boði fyrir pantanir sem settar eru í gang í gegnum símaversrás og er ekki hægt að nota til að hætta við pöntun að hluta til.</span><span class="sxs-lookup"><span data-stu-id="77728-133">This option will not be available for orders initiated through a call center channel and cannot be used to partially cancel an order.</span></span>

- <span data-ttu-id="77728-134">**Uppfylla** – Flytur notandann yfir á uppfyllingarsíðu pöntunar sem verður fyrirframsíuð fyrir valda pöntun.</span><span class="sxs-lookup"><span data-stu-id="77728-134">**Fulfill** – Transfers the user to the order fulfillment page, which will be pre-filtered for the selected order.</span></span> <span data-ttu-id="77728-135">Aðeins pöntunarlínur sem verslun notanda má uppfylla fyrir valda pöntun eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="77728-135">Only order lines that are open for fulfillment by the user's store for the selected order will be displayed.</span></span>

- <span data-ttu-id="77728-136">**Breyta** – Leyfir notendum að gera breytingar á valinni pöntun viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="77728-136">**Edit** – Allows users to make changes to the selected customer order.</span></span> <span data-ttu-id="77728-137">Pantanir eru aðeins breytilegar í [ákveðnum aðstæðum](customer-orders-overview.md#edit-an-existing-customer-order).</span><span class="sxs-lookup"><span data-stu-id="77728-137">Orders are only editable in [certain scenarios](customer-orders-overview.md#edit-an-existing-customer-order).</span></span>

- <span data-ttu-id="77728-138">**Sótt** – Þessi valkostur verður í boði ef pöntunin er með eina eða fleiri línur úthlutaðar sem sóttar í núverandi verslun notanda.</span><span class="sxs-lookup"><span data-stu-id="77728-138">**Pick up** – This option will be available if the order has one or more lines designated for pickup at the user's current store.</span></span> <span data-ttu-id="77728-139">Þessi aðgerð ræsir tiltektarflæðið, sem gerir notandanum kleift að velja afurðirnar sem á að taka til og stofnar sölufærslu tiltektarinnar.</span><span class="sxs-lookup"><span data-stu-id="77728-139">This operation launches the pickup flow, which allows the user to choose the products to be picked up and creates the pickup sales transaction.</span></span>

## <a name="add-notifications-to-the-recall-order-operation"></a><span data-ttu-id="77728-140">Bæta tilkynningum við endurköllunaraðgerð pöntunar</span><span class="sxs-lookup"><span data-stu-id="77728-140">Add notifications to the recall order operation</span></span>

<span data-ttu-id="77728-141">Í útgáfu 10.0.18 og nýrri er hægt að skilgreina tilkynningar sölustaðar og viðvaranir virkra reita fyrir aðgerðina **Endurköllun pöntunar** ef þess er óskað.</span><span class="sxs-lookup"><span data-stu-id="77728-141">In version 10.0.18 and later, you can configure POS notifications and live tile alerts for the **Order Recall** operation if desired.</span></span> <span data-ttu-id="77728-142">Frekari upplýsingar er að finna í [Sýna pöntunartilkynningar á sölustað (POS)](notifications-pos.md).</span><span class="sxs-lookup"><span data-stu-id="77728-142">For more information, see [Show order notifications in the point of sale (POS)](notifications-pos.md).</span></span>  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
