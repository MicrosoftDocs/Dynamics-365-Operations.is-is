---
title: Fá skilavörur afhentar að hluta
description: Hlutaafhendingar eru skilgreindar í skilapöntunarlínum, ekki vöruskilasendingum.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2b7bfad1e0d80675848353d4118960d44f2dc01
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "363914"
---
# <a name="receive-partial-deliveries-of-returned-items"></a><span data-ttu-id="44778-103">Fá skilavörur afhentar að hluta</span><span class="sxs-lookup"><span data-stu-id="44778-103">Receive partial deliveries of returned items</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="44778-104">Hlutaafhendingar eru skilgreindar í skilapöntunarlínum, ekki vöruskilasendingum.</span><span class="sxs-lookup"><span data-stu-id="44778-104">Partial deliveries are defined in terms of return order lines, not return order shipments.</span></span>

<span data-ttu-id="44778-105">Þetta þýðir að afhendingin er ekki hlutaafhending ef tekið er á móti öllu magninu sem fram kemur í einni skilapöntunarlínu en engu úr öðrum línum í skilapöntuninni.</span><span class="sxs-lookup"><span data-stu-id="44778-105">This means that if you receive the full quantity that is indicated on one return order line, but you receive nothing from the other lines in the return order, the delivery is not a partial delivery.</span></span> <span data-ttu-id="44778-106">Hins vegar, ef skilapöntunarlína krefst tíu eininga af tiltekinni vöru sem á að skila, en einungis er tekið á móti fjórum, er um að ræða hlutaafhendingu.</span><span class="sxs-lookup"><span data-stu-id="44778-106">However, if a return order line requires 10 units of a particular item to be returned, but you receive only four, it is a partial delivery.</span></span>

<span data-ttu-id="44778-107">Ef vöruskilasending inniheldur minna en allt magnið í skilapöntunarlínu, er hægt að setja sendinguna til hliðar og bíða þess að afgangurinn af skiluðu magni berist eða skrá og bóka hluta af magninu.</span><span class="sxs-lookup"><span data-stu-id="44778-107">If a return shipment contains less than the full quantity of a return order line, you can set the shipment aside and wait for the rest of the returned quantity to arrive, or you can register and post the partial quantity.</span></span>

## <a name="register-and-post-a-partial-quantity"></a><span data-ttu-id="44778-108">Skrá og bóka hluta af magni</span><span class="sxs-lookup"><span data-stu-id="44778-108">Register and post a partial quantity</span></span>

1.  <span data-ttu-id="44778-109">Eftir að þú velur skilapöntun fyrir afhendingu í skjámyndinni **Komuyfirlit - Vöruhús: %1, dreifing: %2 Heiti færslubókar: %3** skal smella á **Upphafskoma** til að búa til komubók og smella síðan á **Færslubækur** \> **Sýna komur frá kvittunum** til að opna skjámyndina **Staðsetningarbók**.</span><span class="sxs-lookup"><span data-stu-id="44778-109">After you select a return order for arrival on the **Arrival overview - Warehouse: %1, Dock: %2, Journal name: %3** form, click **Start arrival** to create the arrival journal, and then click **Journals** \> **Show arrivals from receipts** to open the **Location journal** form.</span></span>

2.  <span data-ttu-id="44778-110">Veldu línu færslubókarinnar sem þú vilt vinna með og smelltu svo á **Línur** til að opna skjámyndina **Færslubókarlínur, staðsetningar**.</span><span class="sxs-lookup"><span data-stu-id="44778-110">Select the line of the journal that you want to work with, and then click **Lines** to open the **Journal lines, locations** form.</span></span>

3.  <span data-ttu-id="44778-111">Veldu línu vörunúmersins sem aðeins hluti magns hefur komið fyrir og smelltu síðan á **Aðgerðir** \> **Skipta** til að opna skjámyndina **Skipta**.</span><span class="sxs-lookup"><span data-stu-id="44778-111">Select the line of the item number for which only a partial quantity has arrived, and then click **Functions** \> **Split** to open the **Split** form.</span></span>

4.  <span data-ttu-id="44778-112">Sláðu inn magnið fyrir heildarfjölda varanna sem hafa borist í reitinn **Skipta magni** og smelltu síðan á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="44778-112">In the **Split quantity** field, enter the quantity for the total number of items that have been received, and then click **OK**.</span></span>

5.  <span data-ttu-id="44778-113">Í skjámyndinni **Færslubókarlínur, staðsetningar** skal velja línuna fyrir magnið af vörum sem hefur komið og smella síðan á **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="44778-113">On the **Journal lines, locations** form, select the line for the quantity of items that has arrived, and then click **Post**.</span></span> <span data-ttu-id="44778-114">Þú getur bókað línuna fyrir viðbótarmagnið eftir að vörurnar hafa skilað sér.</span><span class="sxs-lookup"><span data-stu-id="44778-114">You can post the line for the additional quantity after the items have arrived.</span></span>




