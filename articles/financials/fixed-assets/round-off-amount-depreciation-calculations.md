---
title: Sléttun upphæða fyrir afskriftaútreikninga.
description: Þessi grein fer yfir svæðið Sléttun afskriftar sem má finna á uppsetningarsíðunum bók.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7721e46a72e0f8133ed67c597a066a97ffd61669
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549128"
---
# <a name="round-off-amount-for-depreciation-calculations"></a><span data-ttu-id="5e263-103">Sléttun upphæða fyrir afskriftaútreikninga.</span><span class="sxs-lookup"><span data-stu-id="5e263-103">Round-off amount for depreciation calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e263-104">Þessi grein fer yfir svæðið Sléttun afskriftar sem má finna á uppsetningarsíðunum bók.</span><span class="sxs-lookup"><span data-stu-id="5e263-104">This article discusses the Round-off depreciation field that is found on the Book setup pages.</span></span>

<span data-ttu-id="5e263-105">Slétta afskriftarupphæðir eru sett fyrir hverja bók.</span><span class="sxs-lookup"><span data-stu-id="5e263-105">Round-off depreciation amounts are set for each book.</span></span> <span data-ttu-id="5e263-106">Sléttun afskriftarupphæða er notuð í afskriftareglu eigna sem sýnir afskriftina í framtíðinni og gildi fyrir eignina og einnig í afskriftartillögum.</span><span class="sxs-lookup"><span data-stu-id="5e263-106">Round-off depreciation amounts are used in the fixed asset depreciation profile that shows the future depreciation and value of the fixed asset, and also in depreciation proposals.</span></span> <span data-ttu-id="5e263-107">Færið inn lægstu leyfilegu upphæðina til afskriftar fyrir þetta bók.</span><span class="sxs-lookup"><span data-stu-id="5e263-107">Enter the lowest depreciation amount that is allowed for the book.</span></span> 

<span data-ttu-id="5e263-108">Óháð því hvaða sléttun er sett upp verður afskriftarupphæðin í síðasta afskriftartímabilinu ekki sléttuð.</span><span class="sxs-lookup"><span data-stu-id="5e263-108">Regardless of the rounding that is set up, the depreciation amount in the last depreciation period isn't rounded.</span></span> <span data-ttu-id="5e263-109">Við lok síðasta afskriftartímabilsins, verður virði eignar að vera 0 (núll) eða á rýrnunarvirði ef rýrnunarvirði er notað.</span><span class="sxs-lookup"><span data-stu-id="5e263-109">At the end of the last depreciation period, the value of the fixed asset must be 0 (zero) or the scrap value, if scrap value is used.</span></span>

### <a name="example"></a><span data-ttu-id="5e263-110">Dæmi</span><span class="sxs-lookup"><span data-stu-id="5e263-110">Example</span></span>

<span data-ttu-id="5e263-111">Afskrift án sléttunar er reiknuð sem 2.444,44.</span><span class="sxs-lookup"><span data-stu-id="5e263-111">Depreciation without rounding is calculated as 2,444.44.</span></span> <span data-ttu-id="5e263-112">Mismunandi upphæðir eru lagðar til eftir því hvaða sléttun er sett upp, eins og sýnt er í töflunni.</span><span class="sxs-lookup"><span data-stu-id="5e263-112">As the following table shows, the amounts that are suggested vary, depending on how rounding is set up.</span></span>

| <span data-ttu-id="5e263-113">Sléttunaraðferð</span><span class="sxs-lookup"><span data-stu-id="5e263-113">Rounding method</span></span> | <span data-ttu-id="5e263-114">Afskriftarupphæð</span><span class="sxs-lookup"><span data-stu-id="5e263-114">Depreciation amount</span></span> |
|-----------------|---------------------|
| <span data-ttu-id="5e263-115">Sléttun 0,1</span><span class="sxs-lookup"><span data-stu-id="5e263-115">Rounding 0.1</span></span>    | <span data-ttu-id="5e263-116">2.444,40</span><span class="sxs-lookup"><span data-stu-id="5e263-116">2,444.40</span></span>            |
| <span data-ttu-id="5e263-117">Sléttun 1,00</span><span class="sxs-lookup"><span data-stu-id="5e263-117">Rounding 1.00</span></span>   | <span data-ttu-id="5e263-118">2.444,00</span><span class="sxs-lookup"><span data-stu-id="5e263-118">2,444.00</span></span>            |
| <span data-ttu-id="5e263-119">Sléttun 10,00</span><span class="sxs-lookup"><span data-stu-id="5e263-119">Rounding 10.00</span></span>  | <span data-ttu-id="5e263-120">2.440,00</span><span class="sxs-lookup"><span data-stu-id="5e263-120">2,440.00</span></span>            |
| <span data-ttu-id="5e263-121">Sléttun 100,00</span><span class="sxs-lookup"><span data-stu-id="5e263-121">Rounding 100.00</span></span> | <span data-ttu-id="5e263-122">2.400,00</span><span class="sxs-lookup"><span data-stu-id="5e263-122">2,400.00</span></span>            |





