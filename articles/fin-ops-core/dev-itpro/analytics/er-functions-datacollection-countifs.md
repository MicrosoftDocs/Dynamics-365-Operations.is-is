---
title: COUNTIFS ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin COUNTIFS í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 554750b2dae5ec1f0fcf6fdbdf439b4dbe4fa615
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681135"
---
# <a name="countifs-er-function"></a><span data-ttu-id="e273d-103">COUNTIFS ER aðgerð</span><span class="sxs-lookup"><span data-stu-id="e273d-103">COUNTIFS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e273d-104">Aðgerðin `COUNTIFS` skilar *Heiltölu*-gildi sem táknar fjölda sniðaþátta sem var safnað þegar sniðþættirnir voru notaðir til að búa til útleiðarskjal við sniðkeyrsluna og sem fullnægir tilgreindum skilyrðum.</span><span class="sxs-lookup"><span data-stu-id="e273d-104">The `COUNTIFS` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="e273d-105">Hvert skilyrði samanstendur af lykilsviði og lykilgildi.</span><span class="sxs-lookup"><span data-stu-id="e273d-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e273d-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="e273d-106">Syntax</span></span>

```vb
COUNTIFS (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="e273d-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="e273d-107">Arguments</span></span>

<span data-ttu-id="e273d-108">`condition 1 range`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="e273d-108">`condition 1 range`: *String*</span></span>

<span data-ttu-id="e273d-109">Gildi sem er skilað með segðinni sem hefur verið stillt í eiginleikanum **Heiti lykils fyrir söfnuð gögn** í sniðsíhluta rafrænnar skýrslugerðar (ER).</span><span class="sxs-lookup"><span data-stu-id="e273d-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span> <span data-ttu-id="e273d-110">Þessi frumbreyta er skylda.</span><span class="sxs-lookup"><span data-stu-id="e273d-110">This argument is mandatory.</span></span>

<span data-ttu-id="e273d-111">`condition 1 value`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="e273d-111">`condition 1 value`: *String*</span></span>

<span data-ttu-id="e273d-112">Gildi sem er skilað með segðinni sem hefur verið stillt í eiginleikanum **Gildi lykils fyrir söfnuð gögn** í ER-sniðsíhluta.</span><span class="sxs-lookup"><span data-stu-id="e273d-112">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="e273d-113">Þessi frumbreyta er skylda.</span><span class="sxs-lookup"><span data-stu-id="e273d-113">This argument is mandatory.</span></span>

<span data-ttu-id="e273d-114">`condition N range`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="e273d-114">`condition N range`: *String*</span></span>

<span data-ttu-id="e273d-115">Gildi sem er skilað með segðinni sem hefur verið stillt í eiginleikanum **Heiti lykils fyrir söfnuð gögn** í ER-sniðsíhluta.</span><span class="sxs-lookup"><span data-stu-id="e273d-115">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="e273d-116">Þessar viðbótarfrumbreytur eru valkvæðar.</span><span class="sxs-lookup"><span data-stu-id="e273d-116">These additional arguments are optional.</span></span>

<span data-ttu-id="e273d-117">`condition N value`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="e273d-117">`condition N value`: *String*</span></span>

<span data-ttu-id="e273d-118">Gildi sem er skilað með segðinni sem hefur verið stillt í eiginleikanum **Gildi lykils fyrir söfnuð gögn** í ER-sniðsíhluta.</span><span class="sxs-lookup"><span data-stu-id="e273d-118">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="e273d-119">Þessar viðbótarfrumbreytur eru valkvæðar.</span><span class="sxs-lookup"><span data-stu-id="e273d-119">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="e273d-120">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="e273d-120">Return values</span></span>

<span data-ttu-id="e273d-121">*Heiltala*</span><span class="sxs-lookup"><span data-stu-id="e273d-121">*Integer*</span></span>

<span data-ttu-id="e273d-122">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="e273d-122">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e273d-123">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="e273d-123">Usage notes</span></span>

<span data-ttu-id="e273d-124">Eiginleikana **Heiti lykils fyrir söfnuð gögn** og **Gildi lykils fyrir söfnuð gögn** er hægt að stilla fyrir annaðhvort íhlutinn **Röð** eða íhlutinn **XML-þáttur** í ER-sniði sem er að finna undir íhlutnum **Common\\File** þar sem kveikt er á valkostinum **Safna saman upplýsingum um framleiðslu**.</span><span class="sxs-lookup"><span data-stu-id="e273d-124">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="e273d-125">Þessi aðgerð skilar gildinu **0** (núll) þegar slökkt er á valkostinum **Safna saman upplýsingum um framleiðslu** í gildandi íhlutnum **Common\\File**.</span><span class="sxs-lookup"><span data-stu-id="e273d-125">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="e273d-126">Í frumbreytunum `condition range` er hægt að nota algildisstafinn **"\*"** til að tákna hvaða marga stafi sem er.</span><span class="sxs-lookup"><span data-stu-id="e273d-126">In `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="e273d-127">Í frumbreytunum `condition value` er hægt að nota algildisstafinn **"\*"** til að tákna hvaða marga stafi sem er.</span><span class="sxs-lookup"><span data-stu-id="e273d-127">In `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="e273d-128">Dæmi</span><span class="sxs-lookup"><span data-stu-id="e273d-128">Example</span></span>

<span data-ttu-id="e273d-129">Nánari upplýsingar um hvernig á að nota þessa aðgerð er að finna í [Rafræn skýrslugerð nota gögn sniðúttaks til að telja og leggja saman](tasks/er-format-counting-summing-1.md) leiðarvísir, sem er hluti af **Veita/þróa IT þjónustu/þáttum** viðskiptaferli.</span><span class="sxs-lookup"><span data-stu-id="e273d-129">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e273d-130">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="e273d-130">Additional resources</span></span>

[<span data-ttu-id="e273d-131">Gagnasöfnunaraðgerðir</span><span class="sxs-lookup"><span data-stu-id="e273d-131">Data collection functions</span></span>](er-functions-category-data-collection.md)
