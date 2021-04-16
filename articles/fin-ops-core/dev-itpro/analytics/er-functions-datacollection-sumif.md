---
title: SUMIF ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin SUMIF í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 04/27/2020
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
ms.openlocfilehash: 60cf85ac0ffcdb163c12670efa3dcc7e9f05cb16
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747108"
---
# <a name="sumif-er-function"></a><span data-ttu-id="a410d-103">SUMIF ER aðgerð</span><span class="sxs-lookup"><span data-stu-id="a410d-103">SUMIF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a410d-104">Aðgerðin `SUMIF` skilar *Raungildi* sem táknar summu gilda sem var skilað af bindingum sniðaþátta og safnað þegar sniðþættirnir voru notaðir til að búa til útleiðarskjal við sniðkeyrsluna og sem fullnægir tilgreindu skilyrði.</span><span class="sxs-lookup"><span data-stu-id="a410d-104">The `SUMIF` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="a410d-105">Skilyrðið samanstendur af lykilsviði og lykilgildi.</span><span class="sxs-lookup"><span data-stu-id="a410d-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a410d-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="a410d-106">Syntax</span></span>

```vb
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="a410d-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="a410d-107">Arguments</span></span>

<span data-ttu-id="a410d-108">`key name for summing`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="a410d-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="a410d-109">Gildi sem er skilað með tjáningunni sem hefur verið stillt í eiginleikanum **Heiti lykils fyrir söfnuð gögn** í sniðhluta rafrænnar skýrslugerðar (ER) sem nota verður gildi bindingarinnar fyrir í samanburðarskyni.</span><span class="sxs-lookup"><span data-stu-id="a410d-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="a410d-110">Eiginleikann **Gildi lykils fyrir söfnuð gögn** er hægt að stilla fyrir annaðhvort íhlutinn **Röð** eða íhlutinn **XML-þáttur** í ER-sniði sem er að finna undir íhlutnum **Common\\File** þar sem kveikt er á valkostium **Safna saman upplýsingum um framleiðslu**.</span><span class="sxs-lookup"><span data-stu-id="a410d-110">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="a410d-111">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="a410d-111">Return values</span></span>

<span data-ttu-id="a410d-112">*Rauntala*</span><span class="sxs-lookup"><span data-stu-id="a410d-112">*Real*</span></span>

<span data-ttu-id="a410d-113">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="a410d-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a410d-114">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="a410d-114">Usage notes</span></span>

<span data-ttu-id="a410d-115">Þessi aðgerð skilar gildinu **0** (núll) þegar slökkt er á valkostinum **Safna saman upplýsingum um framleiðslu** í gildandi íhlutnum **Common\\File**.</span><span class="sxs-lookup"><span data-stu-id="a410d-115">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="a410d-116">Í frumbreytunni `condition range` er hægt að nota algildisstafinn **"\*"** til að tákna hvaða marga stafi sem er.</span><span class="sxs-lookup"><span data-stu-id="a410d-116">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="a410d-117">Í frumbreytunni `condition value` er hægt að nota algildisstafinn **"\*"** til að tákna hvaða marga stafi sem er.</span><span class="sxs-lookup"><span data-stu-id="a410d-117">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="a410d-118">Dæmi</span><span class="sxs-lookup"><span data-stu-id="a410d-118">Example</span></span>

<span data-ttu-id="a410d-119">Nánari upplýsingar um hvernig á að nota þessa aðgerð er að finna í [Rafræn skýrslugerð nota gögn sniðúttaks til að telja og leggja saman](tasks/er-format-counting-summing-1.md) leiðarvísir, sem er hluti af **Veita/þróa IT þjónustu/þáttum** viðskiptaferli.</span><span class="sxs-lookup"><span data-stu-id="a410d-119">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

<span data-ttu-id="a410d-120">Frekari upplýsingar og dæmi um notkun þessarar aðgerðar er að finna í [Keyrslu raðeininga í sniði rafrænnar skýrslugerðar fresta](er-defer-sequence-element.md#Example) og [Keyrslu XML-eininga í sniði rafrænnar skýrslugerðar frestað](er-defer-xml-element.md#Example).</span><span class="sxs-lookup"><span data-stu-id="a410d-120">For more information and examples about using this function, see [Defer the execution of sequence elements in ER formats](er-defer-sequence-element.md#Example) and [Defer the execution of XML elements in ER formats](er-defer-xml-element.md#Example).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a410d-121">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="a410d-121">Additional resources</span></span>

[<span data-ttu-id="a410d-122">Gagnasöfnunaraðgerðir</span><span class="sxs-lookup"><span data-stu-id="a410d-122">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]