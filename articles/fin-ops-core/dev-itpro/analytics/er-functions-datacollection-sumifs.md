---
title: SUMIFS ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin SUMIFS í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a6815a8c9f4141649532f9cd56ac3bc442b48686
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743328"
---
# <a name="sumifs-er-function"></a><span data-ttu-id="5f639-103">SUMIFS ER aðgerð</span><span class="sxs-lookup"><span data-stu-id="5f639-103">SUMIFS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5f639-104">Aðgerðin `SUMIFS` skilar *Raungildi* sem táknar summu gilda sem var skilað af bindingum sniðaþátta og safnað þegar sniðþættirnir voru notaðir til að búa til útleiðarskjal við sniðkeyrsluna og sem fullnægir tilgreindum skilyrðum.</span><span class="sxs-lookup"><span data-stu-id="5f639-104">The `SUMIFS` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="5f639-105">Hvert skilyrði samanstendur af lykilsviði og lykilgildi.</span><span class="sxs-lookup"><span data-stu-id="5f639-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f639-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="5f639-106">Syntax</span></span>

```vb
SUMIFS (key name for summing, condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="5f639-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="5f639-107">Arguments</span></span>

<span data-ttu-id="5f639-108">`key name for summing`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="5f639-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="5f639-109">Gildi sem er skilað með tjáningunni sem hefur verið stillt í eiginleikanum **Heiti lykils fyrir söfnuð gögn** í sniðhluta rafrænnar skýrslugerðar (ER) sem nota verður gildi bindingarinnar fyrir í samanburðarskyni.</span><span class="sxs-lookup"><span data-stu-id="5f639-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="5f639-110">Eiginleikann **Heiti lykils fyrir söfnuð gögn** er hægt að stilla fyrir annaðhvort **tölulegan** íhlut eða íhlutinn **Strengur** í ER-sniði sem er að finna undir íhlutnum **Common\\File** þar sem kveikt er á valkostium **Safna saman upplýsingum um framleiðslu**.</span><span class="sxs-lookup"><span data-stu-id="5f639-110">The **Collected data key name** property can be configured for either a **Numeric** component or a **String** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="5f639-111">`condition 1 range`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="5f639-111">`condition 1 range`: *String*</span></span>

<span data-ttu-id="5f639-112">Gildi sem er skilað með segðinni sem hefur verið stillt í eiginleikanum **Heiti lykils fyrir söfnuð gögn** í ER-sniðsíhluta.</span><span class="sxs-lookup"><span data-stu-id="5f639-112">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="5f639-113">Þessi frumbreyta er skylda.</span><span class="sxs-lookup"><span data-stu-id="5f639-113">This argument is mandatory.</span></span>

<span data-ttu-id="5f639-114">Eiginleikann **Heiti lykils fyrir söfnuð gögn** er hægt að stilla fyrir annaðhvort íhlutinn **Röð** eða íhlutinn **XML-þáttur** í ER-sniði sem er að finna undir íhlutnum **Common\\File** þar sem kveikt er á valkostium **Safna saman upplýsingum um framleiðslu**.</span><span class="sxs-lookup"><span data-stu-id="5f639-114">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="5f639-115">`condition 1 value`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="5f639-115">`condition 1 value`: *String*</span></span>

<span data-ttu-id="5f639-116">Gildi sem er skilað með segðinni sem hefur verið stillt í eiginleikanum **Gildi lykils fyrir söfnuð gögn** í ER-sniðsíhluta.</span><span class="sxs-lookup"><span data-stu-id="5f639-116">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="5f639-117">Þessi frumbreyta er skylda.</span><span class="sxs-lookup"><span data-stu-id="5f639-117">This argument is mandatory.</span></span>

<span data-ttu-id="5f639-118">Eiginleikann **Gildi lykils fyrir söfnuð gögn** er hægt að stilla fyrir annaðhvort íhlutinn **Röð** eða íhlutinn **XML-þáttur** í ER-sniði sem er að finna undir íhlutnum **Common\\File** þar sem kveikt er á valkostium **Safna saman upplýsingum um framleiðslu**.</span><span class="sxs-lookup"><span data-stu-id="5f639-118">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="5f639-119">`condition N range`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="5f639-119">`condition N range`: *String*</span></span>

<span data-ttu-id="5f639-120">Gildi sem er skilað með segðinni sem hefur verið stillt í eiginleikanum **Heiti lykils fyrir söfnuð gögn** í ER-sniðsíhluta.</span><span class="sxs-lookup"><span data-stu-id="5f639-120">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="5f639-121">Þessar viðbótarfrumbreytur eru valkvæðar.</span><span class="sxs-lookup"><span data-stu-id="5f639-121">These additional arguments are optional.</span></span>

<span data-ttu-id="5f639-122">Eiginleikann **Heiti lykils fyrir söfnuð gögn** er hægt að stilla fyrir annaðhvort íhlutinn **Röð** eða íhlutinn **XML-þáttur** í ER-sniði sem er að finna undir íhlutnum **Common\\File** þar sem kveikt er á valkostium **Safna saman upplýsingum um framleiðslu**.</span><span class="sxs-lookup"><span data-stu-id="5f639-122">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="5f639-123">`condition N value`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="5f639-123">`condition N value`: *String*</span></span>

<span data-ttu-id="5f639-124">Gildi sem er skilað með segðinni sem hefur verið stillt í eiginleikanum **Gildi lykils fyrir söfnuð gögn** í ER-sniðsíhluta.</span><span class="sxs-lookup"><span data-stu-id="5f639-124">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="5f639-125">Þessar viðbótarfrumbreytur eru valkvæðar.</span><span class="sxs-lookup"><span data-stu-id="5f639-125">These additional arguments are optional.</span></span>

<span data-ttu-id="5f639-126">Eiginleikann **Gildi lykils fyrir söfnuð gögn** er hægt að stilla fyrir annaðhvort íhlutinn **Röð** eða íhlutinn **XML-þáttur** í ER-sniði sem er að finna undir íhlutnum **Common\\File** þar sem kveikt er á valkostium **Safna saman upplýsingum um framleiðslu**.</span><span class="sxs-lookup"><span data-stu-id="5f639-126">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="5f639-127">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="5f639-127">Return values</span></span>

<span data-ttu-id="5f639-128">*Rauntala*</span><span class="sxs-lookup"><span data-stu-id="5f639-128">*Real*</span></span>

<span data-ttu-id="5f639-129">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="5f639-129">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5f639-130">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="5f639-130">Usage notes</span></span>

<span data-ttu-id="5f639-131">Þessi aðgerð skilar gildinu **0** (núll) þegar slökkt er á valkostinum **Safna saman upplýsingum um framleiðslu** í gildandi íhlutnum **Common\\File**.</span><span class="sxs-lookup"><span data-stu-id="5f639-131">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="5f639-132">Í frumbreytunum `condition range` er hægt að nota algildisstafinn **"\*"** til að tákna hvaða marga stafi sem er.</span><span class="sxs-lookup"><span data-stu-id="5f639-132">In the `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="5f639-133">Í frumbreytunum `condition value` er hægt að nota algildisstafinn **"\*"** til að tákna hvaða marga stafi sem er.</span><span class="sxs-lookup"><span data-stu-id="5f639-133">In the `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="5f639-134">Dæmi</span><span class="sxs-lookup"><span data-stu-id="5f639-134">Example</span></span>

<span data-ttu-id="5f639-135">Nánari upplýsingar um hvernig á að nota þessa aðgerð er að finna í [Rafræn skýrslugerð nota gögn sniðúttaks til að telja og leggja saman](tasks/er-format-counting-summing-1.md) leiðarvísir, sem er hluti af **Veita/þróa IT þjónustu/þáttum** viðskiptaferli.</span><span class="sxs-lookup"><span data-stu-id="5f639-135">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5f639-136">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="5f639-136">Additional resources</span></span>

[<span data-ttu-id="5f639-137">Gagnasöfnunaraðgerðir</span><span class="sxs-lookup"><span data-stu-id="5f639-137">Data collection functions</span></span>](er-functions-category-data-collection.md)
