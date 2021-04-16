---
title: Afskrift lækkandi stöðu eftir skipti
description: Þetta efnisatriði lýsir aðferðinni sem er notuð í eignum til að reikna afskriftir eftir skiptingu eignar með því að minnka bókfært virði.
author: moaamer
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-17
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 056808b7d4d490bc4d60aa058108d159c1d4867c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826252"
---
# <a name="reduce-balance-depreciation-after-a-split"></a><span data-ttu-id="90a49-103">Afskrift lækkandi stöðu eftir skipti</span><span class="sxs-lookup"><span data-stu-id="90a49-103">Reduce balance depreciation after a split</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90a49-104">Þetta efnisatriði lýsir aðferðinni sem er notuð í eignum til að reikna afskriftir eftir skiptingu eignar í aðra eign með því að minnka bókfært virði.</span><span class="sxs-lookup"><span data-stu-id="90a49-104">This topic describes the method that is used in Fixed assets to calculate depreciation after an asset is split to another asset by using the reduce balance method.</span></span> <span data-ttu-id="90a49-105">Afskriftarárið sem er skilgreint í eignabók er fjárhagsárið.</span><span class="sxs-lookup"><span data-stu-id="90a49-105">The depreciation year that is configured in the asset book is the fiscal year.</span></span> <span data-ttu-id="90a49-106">Frekari upplýsingar er að finna í [Minnka bókfært virði](reduce-balance-depreciation.md) og [Skipta eign](tasks/split-fixed-asset.md).</span><span class="sxs-lookup"><span data-stu-id="90a49-106">For more information, see [Reduce balance depreciation](reduce-balance-depreciation.md) and [Split a fixed asset](tasks/split-fixed-asset.md).</span></span>

<span data-ttu-id="90a49-107">Ef eign er skipt á fjárhagstímabil sem er síðar en tímabilið þegar eignin var keypt mun afskrift með minnkun bókfærðs virðis gilda fyrir bókað nettóvirði (BNV) fyrir fyrra ár.</span><span class="sxs-lookup"><span data-stu-id="90a49-107">If you split a fixed asset during a fiscal period that is later than the period when the asset was acquired, the reduced balance depreciation will account for the asset's net book value (NBV) for the previous year.</span></span> <span data-ttu-id="90a49-108">Hún mun einnig gilda fyrir leiðréttingafærslur kaupa og afskrifta sem myndaðar voru úr færslunni sem skipti eigninni.</span><span class="sxs-lookup"><span data-stu-id="90a49-108">It will also account for the acquisition and depreciation adjustment transactions that were generated from the transaction that split the asset.</span></span> <span data-ttu-id="90a49-109">Þessi hegðun gerir ráð fyrir því að eignin hafi verið keypt á einu fjárhagsári og skipt á seinna fjárhagsári.</span><span class="sxs-lookup"><span data-stu-id="90a49-109">This behavior assumes that the asset was acquired in one fiscal year and split in a later fiscal year.</span></span> <span data-ttu-id="90a49-110">Upphæðin sem verður að vera afskrifuð fyrir upprunalegu eignina eftir skiptin endurspeglar BNV eignarinnar, áður en henni var skipt, og leiðréttingarfærslu kaupa og afskriftar sem var bókuð fyrir skiptinguna.</span><span class="sxs-lookup"><span data-stu-id="90a49-110">The amount that must be depreciated for the original asset after the split reflects the asset's NBV before the asset was split, and the acquisition and depreciation adjustment transaction that was posted for the split.</span></span>

<span data-ttu-id="90a49-111">Eftirfarandi skilyrði eru til dæmis í gildi:</span><span class="sxs-lookup"><span data-stu-id="90a49-111">For example, the following conditions are in effect:</span></span>

- <span data-ttu-id="90a49-112">Fjárhagstímabilið er frá 30. júní til 1. júlí.</span><span class="sxs-lookup"><span data-stu-id="90a49-112">The fiscal period is from June 30 to July 1.</span></span>
- <span data-ttu-id="90a49-113">Prósenta lækkandi afskriftar er 18 prósent og eign er keypt í júní 2019 á kaupverðinu $10.000.</span><span class="sxs-lookup"><span data-stu-id="90a49-113">The reducing balance percentage is 18 percent, and an asset is acquired in June 2019 at an acquisition price of $10,000.</span></span>
- <span data-ttu-id="90a49-114">Afskrift fyrsta fjárhagsárs jafngildir $18.000, mánaðarleg afskrift samsvarar $150 og eignin er síðan afskrifuð fram í nóvember 2019 að upphæð $738,75.</span><span class="sxs-lookup"><span data-stu-id="90a49-114">The depreciation of the first fiscal year equals $18,000, the monthly depreciation equals $150, and the asset is then depreciated until November 2019, in the amount of $738.75.</span></span>
- <span data-ttu-id="90a49-115">Í nóvember 2019 er 80 prósentum af eigninni skipt í aðra eign.</span><span class="sxs-lookup"><span data-stu-id="90a49-115">In November 2019, 80 percent of the asset is split to another fixed asset.</span></span>

<span data-ttu-id="90a49-116">[![Afskrift lækkandi stöðu eftir skipti](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span><span class="sxs-lookup"><span data-stu-id="90a49-116">[![Reduce balance depreciation after a split](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span></span>

<span data-ttu-id="90a49-117">Upphæðin til afskriftar fyrir upprunalegu eignina er $1.822,25.</span><span class="sxs-lookup"><span data-stu-id="90a49-117">The amount to depreciate for the original asset is $1,822.25.</span></span> <span data-ttu-id="90a49-118">Þessi upphæð samsvarar BNV áður en skipt færsla er bókuð ($9111,25), auk kaupleiðréttingar sem er mynduð við bókun á skiptifærslunni (-$8000), auk afskriftarleiðréttingarinnar sem er mynduð við skiptifærsluna ($711).</span><span class="sxs-lookup"><span data-stu-id="90a49-118">This amount equals the NBV before the split transaction is posted ($9,111.25), plus the acquisition adjustment that is generated during posting of the split transaction (-$8,000), plus the depreciation adjustment that is generated during the split transaction ($711).</span></span> <span data-ttu-id="90a49-119">Þess vegna er afskriftin fyrir annað ár (1.822,25 × 18 prósent) ÷ 12 = $27,33.</span><span class="sxs-lookup"><span data-stu-id="90a49-119">Therefore, the depreciation for the second year is (1,822.25 × 18 percent) ÷ 12 = $27.33.</span></span>

<span data-ttu-id="90a49-120">Upphæðin til afskriftar fyrir nýju eignina á fyrsta árinu er (8.000 × 18 prósent) ÷ 12 = $120.</span><span class="sxs-lookup"><span data-stu-id="90a49-120">The amount to depreciate for the new fixed asset in the first year is (8,000 × 18 percent) ÷ 12 = $120.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]