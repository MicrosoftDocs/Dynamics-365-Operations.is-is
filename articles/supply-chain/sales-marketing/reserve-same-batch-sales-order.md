---
title: Taka frá í sömu runu fyrir sölupöntun
description: Í þessari grein er því lýst hvernig á að setja upp afurð til að leyfa frátekt birgða gagnvart einni runu í birgðum.
author: omulvad
manager: tfehr
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce750745d6f094a296b43827568ee1745179de2d
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017277"
---
# <a name="reserve-the-same-batch-for-a-sales-order"></a><span data-ttu-id="ec30f-103">Taka frá í sömu runu fyrir sölupöntun</span><span class="sxs-lookup"><span data-stu-id="ec30f-103">Reserve the same batch for a sales order</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec30f-104">Í þessari grein er því lýst hvernig á að setja upp afurð til að leyfa frátekt birgða gagnvart einni runu í birgðum.</span><span class="sxs-lookup"><span data-stu-id="ec30f-104">This article explains how to set up a product to allow reservation of inventory against a single batch of inventory.</span></span>

<span data-ttu-id="ec30f-105">Frátekning í sömu runu gerir kleift að taka frá birgðir fyrir sölupöntunarlínu gagnvart einni runu birgða.</span><span class="sxs-lookup"><span data-stu-id="ec30f-105">Same batch reservation lets you reserve inventory for a sales order line against a single batch of inventory.</span></span> <span data-ttu-id="ec30f-106">Til dæmis, viðskiptavinur sem pantar veggfóður getur beðið um að öll pöntunin sé fyllt úr sömu runu eða lotu til að forðast ósamræmi milli veggfóðursrúllanna.</span><span class="sxs-lookup"><span data-stu-id="ec30f-106">For example, a customer who orders wallpaper can request that the whole order be filled from the same batch or lot, to avoid inconsistencies among the rolls.</span></span> <span data-ttu-id="ec30f-107">Til að setja upp vöru sem nota á frátekningu úr sömu runu þurfa eftirfarandi°stillingar að vera virkar í vörulíkanaflokki, rakningarvíddarflokki og geymsluvíddaflokk sem er úthlutað á afurðina:</span><span class="sxs-lookup"><span data-stu-id="ec30f-107">To set up a product to use same batch reservation, the following settings must be active in the item model group, tracking dimension group, and storage dimension group that you assign to the product:</span></span>

- <span data-ttu-id="ec30f-108">**Vörulíkanaflokkar** – Vörulíkanaflokkurin verður að hafa **Val á sömu runu** og **Sameina kröfu** svæðin valin í **Frátekning** svæðaflokki fyrir birgðareglur.</span><span class="sxs-lookup"><span data-stu-id="ec30f-108">**Item model groups** – The item model group must have the **Same batch selection** and **Consolidate requirement** fields selected in the **Reservation** field group for inventory policies.</span></span>
- <span data-ttu-id="ec30f-109">**Flokkar rakningarvídda** – Rakningarvíddaflokkurinn verður að hafa **Þekjuáætlun eftir vídd** svæði valið fyrir rununúmerið.</span><span class="sxs-lookup"><span data-stu-id="ec30f-109">**Tracking dimensions groups** – The tracking dimension group must have the **Coverage plan by dimension** field selected for the batch number.</span></span>
- <span data-ttu-id="ec30f-110">**Flokkar geymsluvídda** – Geymsluvíddarflokkurinn verður að hafa **Þekjuáætlun eftir vídd** svæði valin fyrir **Svæði** og **Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="ec30f-110">**Storage dimensions groups** – The storage dimension group must have the **Coverage plan by dimension** field selected for **Site** and **Warehouse**.</span></span>

<span data-ttu-id="ec30f-111">Þegar teknar eru frá birgðir fyrir vöru á sölupöntunarlínu sem er sett upp fyrir val á sömu runu, reynir kerfið að taka pantaða magnið úr einni birgðarunu.</span><span class="sxs-lookup"><span data-stu-id="ec30f-111">When you reserve inventory for a product on a sales order line that is set up for same batch selection, the system tries to reserve the ordered quantity from a single inventory batch.</span></span> <span data-ttu-id="ec30f-112">Allar sértækar runueigindakröfur eru einnig skoðaðar.</span><span class="sxs-lookup"><span data-stu-id="ec30f-112">Any specific batch attribute requirements are also considered.</span></span> <span data-ttu-id="ec30f-113">Ef ekki er hægt að fylla magn úr einni runu birtist **Árekstrar í frátekningu sömu runu** síða°.</span><span class="sxs-lookup"><span data-stu-id="ec30f-113">If the quantity can't be filled from a single batch, the **Same batch reservation conflict** page appears.</span></span> <span data-ttu-id="ec30f-114">Þessi síða lýsir vandamálunum og einnig aðgerðunum sem hægt er að framkvæma°til að halda áfram með frátekningu.</span><span class="sxs-lookup"><span data-stu-id="ec30f-114">This page describes the issues and also the actions that you can take to continue with the reservation.</span></span> <span data-ttu-id="ec30f-115">Eftirfarandi aðstæður gætu komið í veg fyrir frátekningu runu:</span><span class="sxs-lookup"><span data-stu-id="ec30f-115">The following conditions might prevent the batch from being reserved:</span></span>

- <span data-ttu-id="ec30f-116">Ráðstöfunarkóði runu hefur **Hindra frátekningu** fyrir sölu merkt með flaggi sem **Hindra**.</span><span class="sxs-lookup"><span data-stu-id="ec30f-116">The batch disposition code has **Block reservation** for sales flagged as **Blocked**.</span></span>
- <span data-ttu-id="ec30f-117">Runuvinnslan er útrunnin, byggt á lokadegi og öllum viðeigandi seljanlegum dögum til viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="ec30f-117">The batch has expired, based on the expiration date and any applicable customer sellable days.</span></span> <span data-ttu-id="ec30f-118">Varan getur enn verið hugsanleg til frátekningar ef vörulíkanaflokkur fyrir vöruna er „Fyrsti Lokadagur Fyrst Út“ (FEFO) dagsetningarstýrður og ef best-fyrir dagsetningin er valin sem skilyrði í tiltekt.</span><span class="sxs-lookup"><span data-stu-id="ec30f-118">The item can still be considered for reservation if the item model group for the item is First Expiry First Out (FEFO) date–controlled, and if the best-before date is selected as the pick criterion.</span></span>
- <span data-ttu-id="ec30f-119">Runuvinnslan hefur ekki nægilega langan endingartíma eftir, á grundvelli lokadagsetningar og best-fyrir dagsetningar plús seljanlega daga til viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="ec30f-119">The batch doesn't have enough shelf-life days remaining, based on the expiration date and best-before date, plus any customer sellable days.</span></span>

<span data-ttu-id="ec30f-120">Fyrir hluti sem tengjast geymsluvíddarhóp sem hefur **Nota ferli vöruhúsastjórnunar** virkt geturðu pantað ákveðin rununúmer með því að nota pöntunarveldi með birgðafjölda rununúmersins skilgreint fyrir ofan staðsetningarvíddina.</span><span class="sxs-lookup"><span data-stu-id="ec30f-120">For items associated with a storage dimension group that has **Use warehouse management processes** enabled, you can reserve specific batch numbers by using a reservation hierarchy with the batch number inventory dimension defined above the location dimension.</span></span> <span data-ttu-id="ec30f-121">Síðan **Runufrátekt** fyrir sölu- og flutningspöntunarlínur gerir þér einnig kleift að velja og panta margar línur miðað við fyrirliggjandi rununúmer.</span><span class="sxs-lookup"><span data-stu-id="ec30f-121">The **Batch reservation** page for sales and transfer order lines also lets you select and reserve multiple lines based on the available batch numbers.</span></span> <span data-ttu-id="ec30f-122">Fyrir frekari upplýsingar um hvað á að gera ef þú notar frátekningarstigveldi sem hefur rununúmervíddina fyrir neðan staðsetningu, sjá [Sveigjanleg stefna fyrir vöruvíddarstærð fyrirvara](../warehousing/flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="ec30f-122">For more information about what to do if you are using a reservation hierarchy that has the batch number dimension below the location, see [Flexible warehouse-level dimension reservation policy](../warehousing/flexible-warehouse-level-dimension-reservation.md).</span></span>
