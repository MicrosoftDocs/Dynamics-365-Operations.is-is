---
title: COLLECTEDLIST ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin COLLECTEDLIST í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ff48170247130a03b10dc8fe2973f8d774046944
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561399"
---
# <a name="collectedlist-er-function"></a><span data-ttu-id="df815-103">COLLECTEDLIST ER aðgerð</span><span class="sxs-lookup"><span data-stu-id="df815-103">COLLECTEDLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df815-104">Aðgerðin `COLLECTEDLIST` skilar *Skráalista*-gildi sem inniheldur lista yfir gildi sem skilað var af eiginleikanum **Gildi lykils fyrir söfnuð gögn** í sniðþáttum og safnað þegar sniðþættirnir voru notaðir til að búa til útleiðarskjöl við sniðkeyrsluna og sem fullnægir tilgreindum skilyrðum.</span><span class="sxs-lookup"><span data-stu-id="df815-104">The `COLLECTEDLIST` function a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate outbound documents during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="df815-105">Hvert skilyrði samanstendur af lykilsviði og lykilgildi.</span><span class="sxs-lookup"><span data-stu-id="df815-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="df815-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="df815-106">Syntax</span></span>

```vb
COLLECTEDLIST (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="df815-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="df815-107">Arguments</span></span>

<span data-ttu-id="df815-108">`condition 1 range`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="df815-108">`condition 1 range`: *String*</span></span>

<span data-ttu-id="df815-109">Gildi sem er skilað með segðinni sem hefur verið stillt í eiginleikanum **Heiti lykils fyrir söfnuð gögn** í sniðsíhluta rafrænnar skýrslugerðar (ER).</span><span class="sxs-lookup"><span data-stu-id="df815-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span> <span data-ttu-id="df815-110">Þessi frumbreyta er skylda.</span><span class="sxs-lookup"><span data-stu-id="df815-110">This argument is mandatory.</span></span>

<span data-ttu-id="df815-111">`condition 1 value`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="df815-111">`condition 1 value`: *String*</span></span>

<span data-ttu-id="df815-112">Gildi sem er skilað með segðinni sem hefur verið stillt í eiginleikanum **Gildi lykils fyrir söfnuð gögn** í ER-sniðsíhluta.</span><span class="sxs-lookup"><span data-stu-id="df815-112">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="df815-113">Þessi frumbreyta er skylda.</span><span class="sxs-lookup"><span data-stu-id="df815-113">This argument is mandatory.</span></span>

<span data-ttu-id="df815-114">`condition N range`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="df815-114">`condition N range`: *String*</span></span>

<span data-ttu-id="df815-115">Gildi sem er skilað með segðinni sem hefur verið stillt í eiginleikanum **Heiti lykils fyrir söfnuð gögn** í ER-sniðsíhluta.</span><span class="sxs-lookup"><span data-stu-id="df815-115">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="df815-116">Þessar viðbótarfrumbreytur eru valkvæðar.</span><span class="sxs-lookup"><span data-stu-id="df815-116">These additional arguments are optional.</span></span>

<span data-ttu-id="df815-117">`condition N value`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="df815-117">`condition N value`: *String*</span></span>

<span data-ttu-id="df815-118">Gildi sem er skilað með segðinni sem hefur verið stillt í eiginleikanum **Gildi lykils fyrir söfnuð gögn** í ER-sniðsíhluta.</span><span class="sxs-lookup"><span data-stu-id="df815-118">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="df815-119">Þessar viðbótarfrumbreytur eru valkvæðar.</span><span class="sxs-lookup"><span data-stu-id="df815-119">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="df815-120">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="df815-120">Return values</span></span>

<span data-ttu-id="df815-121">*Skráalisti*</span><span class="sxs-lookup"><span data-stu-id="df815-121">*Record list*</span></span>

<span data-ttu-id="df815-122">Sá listi yfir skrár sem er búinn til.</span><span class="sxs-lookup"><span data-stu-id="df815-122">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="df815-123">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="df815-123">Usage notes</span></span>

<span data-ttu-id="df815-124">Eiginleikana **Heiti lykils fyrir söfnuð gögn** og **Gildi lykils fyrir söfnuð gögn** er hægt að stilla fyrir annaðhvort íhlutinn **Röð** eða íhlutinn **XML-þáttur** í ER-sniði sem er að finna undir íhlutnum **Common\\File** þar sem kveikt er á valkostinum **Safna saman upplýsingum um framleiðslu**.</span><span class="sxs-lookup"><span data-stu-id="df815-124">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="df815-125">Þessi aðgerð skilar tómum lista þegar slökkt er á valkostinum **Safna saman upplýsingum um framleiðslu** í gildandi íhlutnum **Common\\File**.</span><span class="sxs-lookup"><span data-stu-id="df815-125">This function returns an empty list when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="df815-126">Í frumbreytunum `condition range` er hægt að nota algildisstafinn **"\*"** til að tákna hvaða marga stafi sem er.</span><span class="sxs-lookup"><span data-stu-id="df815-126">In `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="df815-127">Í frumbreytunum `condition value` er hægt að nota algildisstafinn **"\*"** til að tákna hvaða marga stafi sem er.</span><span class="sxs-lookup"><span data-stu-id="df815-127">In `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="df815-128">Dæmi</span><span class="sxs-lookup"><span data-stu-id="df815-128">Example</span></span>

<span data-ttu-id="df815-129">Nánari upplýsingar um hvernig á að nota þessa aðgerð er að finna í [Rafræn skýrslugerð nota gögn sniðúttaks til að telja og leggja saman](tasks/er-format-counting-summing-1.md) leiðarvísir, sem er hluti af **Veita/þróa IT þjónustu/þáttum** viðskiptaferli.</span><span class="sxs-lookup"><span data-stu-id="df815-129">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="df815-130">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="df815-130">Additional resources</span></span>

[<span data-ttu-id="df815-131">Gagnasöfnunaraðgerðir</span><span class="sxs-lookup"><span data-stu-id="df815-131">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]