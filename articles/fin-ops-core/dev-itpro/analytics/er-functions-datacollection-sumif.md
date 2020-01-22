---
title: SUMIF ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin SUMIF í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 579b14c713bc5f9831c5e012d16bb3b6f97b1035
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916431"
---
# <span data-ttu-id="d40cd-103"><a name="SUMIF">SUMIF ER aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="d40cd-103"><a name="SUMIF">SUMIF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d40cd-104">Aðgerðin `SUMIF` skilar *Raungildi* sem táknar summu gilda sem var skilað af bindingum sniðaþátta og safnað þegar sniðþættirnir voru notaðir til að búa til útleiðarskjal við sniðkeyrsluna og sem fullnægir tilgreindu skilyrði.</span><span class="sxs-lookup"><span data-stu-id="d40cd-104">The `SUMIF` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="d40cd-105">Skilyrðið samanstendur af lykilsviði og lykilgildi.</span><span class="sxs-lookup"><span data-stu-id="d40cd-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d40cd-106">Málskipun</span><span class="sxs-lookup"><span data-stu-id="d40cd-106">Syntax</span></span>

```
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="d40cd-107">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="d40cd-107">Arguments</span></span>

<span data-ttu-id="d40cd-108">`key name for summing`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="d40cd-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="d40cd-109">Gildi sem er skilað með tjáningunni sem hefur verið stillt í eiginleikanum **Heiti lykils fyrir söfnuð gögn** í sniðhluta rafrænnar skýrslugerðar (ER) sem nota verður gildi bindingarinnar fyrir í samanburðarskyni.</span><span class="sxs-lookup"><span data-stu-id="d40cd-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="d40cd-110">Eiginleikann **Gildi lykils fyrir söfnuð gögn** er hægt að stilla fyrir annaðhvort íhlutinn **Röð** eða íhlutinn **XML-þáttur** í ER-sniði sem er að finna undir íhlutnum **Common\\File** þar sem kveikt er á valkostium **Safna saman upplýsingum um framleiðslu**.</span><span class="sxs-lookup"><span data-stu-id="d40cd-110">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="d40cd-111">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="d40cd-111">Return values</span></span>

<span data-ttu-id="d40cd-112">*Rauntala*</span><span class="sxs-lookup"><span data-stu-id="d40cd-112">*Real*</span></span>

<span data-ttu-id="d40cd-113">Tölugildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="d40cd-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d40cd-114">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="d40cd-114">Usage notes</span></span>

<span data-ttu-id="d40cd-115">Þessi aðgerð skilar gildinu **0** (núll) þegar slökkt er á valkostinum **Safna saman upplýsingum um framleiðslu** í gildandi íhlutnum **Common\\File**.</span><span class="sxs-lookup"><span data-stu-id="d40cd-115">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="d40cd-116">Í frumbreytunni `condition range` er hægt að nota algildisstafinn **"\*"** til að tákna hvaða marga stafi sem er.</span><span class="sxs-lookup"><span data-stu-id="d40cd-116">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="d40cd-117">Í frumbreytunni `condition value` er hægt að nota algildisstafinn **"\*"** til að tákna hvaða marga stafi sem er.</span><span class="sxs-lookup"><span data-stu-id="d40cd-117">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="d40cd-118">Dæmi</span><span class="sxs-lookup"><span data-stu-id="d40cd-118">Example</span></span>

<span data-ttu-id="d40cd-119">Nánari upplýsingar um hvernig á að nota þessa aðgerð er að finna í [Rafræn skýrslugerð nota gögn sniðúttaks til að telja og leggja saman](tasks/er-format-counting-summing-1.md) leiðarvísir, sem er hluti af **Veita/þróa IT þjónustu/þáttum** viðskiptaferli.</span><span class="sxs-lookup"><span data-stu-id="d40cd-119">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d40cd-120">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="d40cd-120">Additional resources</span></span>

[<span data-ttu-id="d40cd-121">Gagnasöfnunaraðgerðir</span><span class="sxs-lookup"><span data-stu-id="d40cd-121">Data collection functions</span></span>](er-functions-category-data-collection.md)
