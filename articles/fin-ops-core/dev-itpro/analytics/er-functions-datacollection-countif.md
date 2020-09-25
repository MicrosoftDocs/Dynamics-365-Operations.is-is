---
title: COUNTIF ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin COUNTIF í rafrænni skýrslugerð (ER) er notuð.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cc857a004d988a421c32722b1f69e86b7fefeb36
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743616"
---
# <a name="countif-er-function"></a><span data-ttu-id="835ea-103">COUNTIF ER aðgerð</span><span class="sxs-lookup"><span data-stu-id="835ea-103">COUNTIF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="835ea-104">Aðgerðin `COUNTIF` skilar *Heiltölu*-gildi sem táknar fjölda sniðaþátta sem var safnað þegar sniðþættirnir voru notaðir til að búa til útleiðarskjal við sniðkeyrsluna og sem fullnægir tilgreindu skilyrði.</span><span class="sxs-lookup"><span data-stu-id="835ea-104">The `COUNTIF` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="835ea-105">Skilyrðið samanstendur af lykilsviði og lykilgildi.</span><span class="sxs-lookup"><span data-stu-id="835ea-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="835ea-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="835ea-106">Syntax</span></span>

```vb
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="835ea-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="835ea-107">Arguments</span></span>

<span data-ttu-id="835ea-108">`condition range`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="835ea-108">`condition range`: *String*</span></span>

<span data-ttu-id="835ea-109">Gildi sem er skilað með segðinni sem hefur verið stillt í eiginleikanum **Heiti lykils fyrir söfnuð gögn** í sniðsíhluta rafrænnar skýrslugerðar (ER).</span><span class="sxs-lookup"><span data-stu-id="835ea-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span>

<span data-ttu-id="835ea-110">`condition value`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="835ea-110">`condition value`: *String*</span></span>

<span data-ttu-id="835ea-111">Gildi sem er skilað með segðinni sem hefur verið stillt í eiginleikanum **Gildi lykils fyrir söfnuð gögn** í ER-sniðsíhluta.</span><span class="sxs-lookup"><span data-stu-id="835ea-111">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span>

## <a name="return-values"></a><span data-ttu-id="835ea-112">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="835ea-112">Return values</span></span>

<span data-ttu-id="835ea-113">*Heiltala*</span><span class="sxs-lookup"><span data-stu-id="835ea-113">*Integer*</span></span>

<span data-ttu-id="835ea-114">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="835ea-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="835ea-115">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="835ea-115">Usage notes</span></span>

<span data-ttu-id="835ea-116">Eiginleikana **Heiti lykils fyrir söfnuð gögn** og **Gildi lykils fyrir söfnuð gögn** er hægt að stilla fyrir annaðhvort íhlutinn **Röð** eða íhlutinn **XML-þáttur** í ER-sniði sem er að finna undir íhlutnum **Common\\File** þar sem kveikt er á valkostinum **Safna saman upplýsingum um framleiðslu**.</span><span class="sxs-lookup"><span data-stu-id="835ea-116">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="835ea-117">Þessi aðgerð skilar gildinu **0** (núll) þegar slökkt er á valkostinum **Safna saman upplýsingum um framleiðslu** í gildandi íhlutnum **Common\\File**.</span><span class="sxs-lookup"><span data-stu-id="835ea-117">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="835ea-118">Í frumbreytunni `condition range` er hægt að nota algildisstafinn **"\*"** til að tákna hvaða marga stafi sem er.</span><span class="sxs-lookup"><span data-stu-id="835ea-118">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="835ea-119">Í frumbreytunni `condition value` er hægt að nota algildisstafinn **"\*"** til að tákna hvaða marga stafi sem er.</span><span class="sxs-lookup"><span data-stu-id="835ea-119">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="835ea-120">Dæmi</span><span class="sxs-lookup"><span data-stu-id="835ea-120">Example</span></span>

<span data-ttu-id="835ea-121">Nánari upplýsingar um hvernig á að nota þessa aðgerð er að finna í [Rafræn skýrslugerð nota gögn sniðúttaks til að telja og leggja saman](tasks/er-format-counting-summing-1.md) leiðarvísir, sem er hluti af **Veita/þróa IT þjónustu/þáttum** viðskiptaferli.</span><span class="sxs-lookup"><span data-stu-id="835ea-121">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="835ea-122">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="835ea-122">Additional resources</span></span>

[<span data-ttu-id="835ea-123">Gagnasöfnunaraðgerðir</span><span class="sxs-lookup"><span data-stu-id="835ea-123">Data collection functions</span></span>](er-functions-category-data-collection.md)
