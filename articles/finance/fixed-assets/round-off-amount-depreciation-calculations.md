---
title: Sléttun upphæða fyrir afskriftaútreikninga.
description: Þessi grein fer yfir svæðið Sléttun afskriftar sem má finna á uppsetningarsíðunum bók.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bf7cf68c98b14fb6c206c99673168153b32a449
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830424"
---
# <a name="round-off-amount-for-depreciation-calculations"></a><span data-ttu-id="03543-103">Sléttun upphæða fyrir afskriftaútreikninga.</span><span class="sxs-lookup"><span data-stu-id="03543-103">Round-off amount for depreciation calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03543-104">Þessi grein fer yfir svæðið Sléttun afskriftar sem má finna á uppsetningarsíðunum bók.</span><span class="sxs-lookup"><span data-stu-id="03543-104">This article discusses the Round-off depreciation field that is found on the Book setup pages.</span></span>

<span data-ttu-id="03543-105">Slétta afskriftarupphæðir eru sett fyrir hverja bók.</span><span class="sxs-lookup"><span data-stu-id="03543-105">Round-off depreciation amounts are set for each book.</span></span> <span data-ttu-id="03543-106">Sléttun afskriftarupphæða er notuð í afskriftareglu eigna sem sýnir afskriftina í framtíðinni og gildi fyrir eignina og einnig í afskriftartillögum.</span><span class="sxs-lookup"><span data-stu-id="03543-106">Round-off depreciation amounts are used in the fixed asset depreciation profile that shows the future depreciation and value of the fixed asset, and also in depreciation proposals.</span></span> <span data-ttu-id="03543-107">Færið inn lægstu leyfilegu upphæðina til afskriftar fyrir þetta bók.</span><span class="sxs-lookup"><span data-stu-id="03543-107">Enter the lowest depreciation amount that is allowed for the book.</span></span> 

<span data-ttu-id="03543-108">Óháð því hvaða sléttun er sett upp verður afskriftarupphæðin í síðasta afskriftartímabilinu ekki sléttuð.</span><span class="sxs-lookup"><span data-stu-id="03543-108">Regardless of the rounding that is set up, the depreciation amount in the last depreciation period isn't rounded.</span></span> <span data-ttu-id="03543-109">Við lok síðasta afskriftartímabilsins, verður virði eignar að vera 0 (núll) eða á rýrnunarvirði ef rýrnunarvirði er notað.</span><span class="sxs-lookup"><span data-stu-id="03543-109">At the end of the last depreciation period, the value of the fixed asset must be 0 (zero) or the scrap value, if scrap value is used.</span></span>

### <a name="example"></a><span data-ttu-id="03543-110">Dæmi</span><span class="sxs-lookup"><span data-stu-id="03543-110">Example</span></span>

<span data-ttu-id="03543-111">Afskrift án sléttunar er reiknuð sem 2.444,44.</span><span class="sxs-lookup"><span data-stu-id="03543-111">Depreciation without rounding is calculated as 2,444.44.</span></span> <span data-ttu-id="03543-112">Mismunandi upphæðir eru lagðar til eftir því hvaða sléttun er sett upp, eins og sýnt er í töflunni.</span><span class="sxs-lookup"><span data-stu-id="03543-112">As the following table shows, the amounts that are suggested vary, depending on how rounding is set up.</span></span>

| <span data-ttu-id="03543-113">Sléttunaraðferð</span><span class="sxs-lookup"><span data-stu-id="03543-113">Rounding method</span></span> | <span data-ttu-id="03543-114">Afskriftarupphæð</span><span class="sxs-lookup"><span data-stu-id="03543-114">Depreciation amount</span></span> |
|-----------------|---------------------|
| <span data-ttu-id="03543-115">Sléttun 0,1</span><span class="sxs-lookup"><span data-stu-id="03543-115">Rounding 0.1</span></span>    | <span data-ttu-id="03543-116">2.444,40</span><span class="sxs-lookup"><span data-stu-id="03543-116">2,444.40</span></span>            |
| <span data-ttu-id="03543-117">Sléttun 1,00</span><span class="sxs-lookup"><span data-stu-id="03543-117">Rounding 1.00</span></span>   | <span data-ttu-id="03543-118">2.444,00</span><span class="sxs-lookup"><span data-stu-id="03543-118">2,444.00</span></span>            |
| <span data-ttu-id="03543-119">Sléttun 10,00</span><span class="sxs-lookup"><span data-stu-id="03543-119">Rounding 10.00</span></span>  | <span data-ttu-id="03543-120">2.440,00</span><span class="sxs-lookup"><span data-stu-id="03543-120">2,440.00</span></span>            |
| <span data-ttu-id="03543-121">Sléttun 100,00</span><span class="sxs-lookup"><span data-stu-id="03543-121">Rounding 100.00</span></span> | <span data-ttu-id="03543-122">2.400,00</span><span class="sxs-lookup"><span data-stu-id="03543-122">2,400.00</span></span>            |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]