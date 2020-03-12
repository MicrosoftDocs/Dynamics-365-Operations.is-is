---
title: NUMBERFORMAT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin NUMBERFORMAT í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 41f48fb49b2d28acf69fe05fe87644a4c43e81fe
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070553"
---
# <span data-ttu-id="46198-103"><a name="NUMBERFORMAT">NUMBERFORMAT ER-aðgerð</a></span><span class="sxs-lookup"><span data-stu-id="46198-103"><a name="NUMBERFORMAT">NUMBERFORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="46198-104">Aðgerðin `NUMBERFORMAT` skilar *String*-gildi sem setur fram tilgreinda tölu á tilgreindu sniði og í valinni tiltekinni [menningu](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="46198-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="46198-105">Fyrir upplýsingar um studd snið skal sjá [staðlað](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) og [sérsniðna](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="46198-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="46198-106">Málskipun 1</span><span class="sxs-lookup"><span data-stu-id="46198-106">Syntax 1</span></span>

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="46198-107">Málskipun 2</span><span class="sxs-lookup"><span data-stu-id="46198-107">Syntax 2</span></span>

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="46198-108">Frumbreytur</span><span class="sxs-lookup"><span data-stu-id="46198-108">Arguments</span></span>

<span data-ttu-id="46198-109">`number`: *Heiltala* eða *Raun*</span><span class="sxs-lookup"><span data-stu-id="46198-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="46198-110">Tölugildi sem tilgreinir töluna sem verður að forsníða.</span><span class="sxs-lookup"><span data-stu-id="46198-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="46198-111">`format`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="46198-111">`format` : *String*</span></span>

<span data-ttu-id="46198-112">Gildið *Strengur* sem táknar sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="46198-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="46198-113">`culture`: *Strengur*</span><span class="sxs-lookup"><span data-stu-id="46198-113">`culture`: *String*</span></span>

<span data-ttu-id="46198-114">Gildið *Strengur* sem táknar menninguna sem á að nota til að forsníða.</span><span class="sxs-lookup"><span data-stu-id="46198-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="46198-115">Skilagildi</span><span class="sxs-lookup"><span data-stu-id="46198-115">Return values</span></span>

<span data-ttu-id="46198-116">*Strengur*</span><span class="sxs-lookup"><span data-stu-id="46198-116">*String*</span></span>

<span data-ttu-id="46198-117">Textagildið sem verður til.</span><span class="sxs-lookup"><span data-stu-id="46198-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="46198-118">Notkunarbréf</span><span class="sxs-lookup"><span data-stu-id="46198-118">Usage notes</span></span>

<span data-ttu-id="46198-119">Ef menningin er ekki skilgreind sem frumbreyta kallaðrar aðgerðar ákvarðar samhengið sem þessari aðgerð er keyrt í hvaða menning er notuð til að forsníða tölur.</span><span class="sxs-lookup"><span data-stu-id="46198-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="46198-120">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="46198-120">Example 1</span></span>

<span data-ttu-id="46198-121">Fyrir menninguna **EN-US** skilar `NUMBERFORMAT (0.45, "p")` **"45,00 %"** og `NUMBERFORMAT (10.45, "#")` skilar **"10"**.</span><span class="sxs-lookup"><span data-stu-id="46198-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="46198-122">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="46198-122">Example 2</span></span>

<span data-ttu-id="46198-123">`NUMBERFORMAT (10/3, "F2", "de")` skilar **3,33** en `NUMBERFORMAT (10/3, "F2", "en-us")` skilar **3,33**.</span><span class="sxs-lookup"><span data-stu-id="46198-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="46198-124">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="46198-124">Additional resources</span></span>

[<span data-ttu-id="46198-125">Textavirkni</span><span class="sxs-lookup"><span data-stu-id="46198-125">Text functions</span></span>](er-functions-category-text.md)
